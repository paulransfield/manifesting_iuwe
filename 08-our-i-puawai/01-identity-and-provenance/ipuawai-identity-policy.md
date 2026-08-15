# ī-puāwai Identity Policy

## Purpose

ī-puāwai needs identifiers that remain trustworthy as content is translated, reviewed, moved between drives, represented by several media variants, revised for different cohorts, and used by different communities. The identifier policy must support three different jobs without forcing one string to do all of them:

1. **Database identity:** a stable machine-safe key that never changes.
2. **Human reference:** a short, readable code that people can use in a conversation, a Discourse topic, a URL, a CSV, or a production brief.
3. **Production filename:** a descriptive, flexible file name that helps a person work quickly but is never treated as the source of truth.

> **Hold identity firmly; hold descriptive language and production context separately.**

## Decision

The legacy pattern—such as `mri_w_000001_te_the_np`—is valuable, but it is **not a UUID**. It combines language, type, curricular position, target word, translation, and dialect. Several of those fields can legitimately change through community review or improved teaching design. They should therefore remain normal, editable database fields.

The recommended model is:

| Layer | Field | Example | Rule |
|---|---|---|---|
| Canonical internal ID | `uuid` | `0199cbd6-f880-7a2e-9eef-5de50d176915` | System-generated once; never edited; never derived from a filename or word. |
| Short human reference | `public_ref` | `w-7K4D9M` | Prefix plus a short random code; unique; stable; suitable for cards, support, and URLs. |
| Type prefix | `entity_prefix` | `w` | Derived from table/type; useful for immediate recognition, but not the identity itself. |
| Curricular order | `sequence_no` | `000001` | Ordered teaching position; can be reviewed/resequenced without changing identity. |
| Language/dialect | `language_code`, `dialect_code` | `mri`, `np` | Normal, validated fields; they must not be packed into the UUID. |
| Teaching language | `target_text`, `translation_text` | `te`, `the` | Reviewable language records, not identity components. |
| Production filename | `production_filename` | `mri_w_000001_te_the_np_v01_classroom_adult_male_native.wav` | Human-friendly working label; may change between versions and formats. |

## Canonical UUID

Use a standards-based UUID in every core table. When the installed Python version supports it, use **UUIDv7**: it is globally unique and broadly time-sortable. If an older environment lacks UUIDv7, use UUIDv4 rather than inventing a pseudo-UUID from words, filenames, or numerical positions.

```python
import uuid

def new_uuid() -> str:
    return str(uuid.uuid7() if hasattr(uuid, "uuid7") else uuid.uuid4())
```

The UUID belongs to the record itself. It does **not** identify an image in the `words` table. The existing `image_uuid` column should be renamed or retired in favour of a generic record UUID plus explicit `word_sense_visuals` and `asset_variants` relationships. A word may have many images; an image may serve several word senses; no single `image_uuid` field can express that safely.

## Short human references

Use a short public reference alongside the canonical UUID. The recommended visible pattern is:

```text
{prefix}-{six_or_eight_character_random_code}
```

Examples:

| Entity | Prefix | Example public reference |
|---|---:|---|
| Phoneme / sound | `s` | `s-7K4D9M` |
| Word | `w` | `w-2FQ8AX` |
| Idiom or phrase | `i` | `i-9CJ6NR` |
| Practice event | `p` | `p-3VMB7K` |
| Lesson | `l` | `l-5HXT2W` |
| Media asset | `a` | `a-8RZ4PQ` |
| Asset family | `f` | `f-6YKG3D` |
| Asset variant | `v` | `v-1NPQ8E` |
| External source | `x` | `x-4TDM9B` |
| Description | `d` | `d-2LQW7S` |
| Evidence item | `e` | `e-8BKJ5R` |
| Receipt | `r` | `r-4PX6NC` |

The prefix allows a person to understand the kind of record immediately. The short code is not a curriculum number, language code, source name, filename, or secret. It is simply a compact stable handle. Store a case-insensitive unique index on `public_ref`.

## Where the legacy taxonomy belongs

Retain the legacy components as structured fields and generate a **production stem** when needed:

```text
{language_code}_{entity_prefix}_{sequence_no}_{target_slug}_{translation_slug}_{dialect_code}
```

For example:

```text
mri_w_000001_te_the_np
```

This remains useful for curated exports, visible classroom files, and handoff to production. It should not become the primary key. The full production filename can then safely carry media-specific version and context:

```text
mri_w_000001_te_the_np_v01_classroom_adult_male_native.wav
```

A media asset record should also retain `original_filename`, `production_filename`, `mime_type`, `variant_role`, `parent_asset_uuid`, `source_sha256`, and its relation to the relevant word sense or practice event. The filename can change; the asset UUID and public reference do not.

## Required schema changes

Apply the identity fields consistently to core tables:

```sql
-- Apply an equivalent pair of columns to every core entity table.
ALTER TABLE phonemes ADD COLUMN uuid TEXT;
ALTER TABLE phonemes ADD COLUMN public_ref TEXT;

ALTER TABLE words ADD COLUMN uuid TEXT;
ALTER TABLE words ADD COLUMN public_ref TEXT;

ALTER TABLE word_senses ADD COLUMN uuid TEXT;
ALTER TABLE word_senses ADD COLUMN public_ref TEXT;

ALTER TABLE content_assets ADD COLUMN uuid TEXT;
ALTER TABLE content_assets ADD COLUMN public_ref TEXT;
```

For a fresh or rebuilt schema, make these `NOT NULL` and `UNIQUE`. During migration, add them as nullable, backfill safely, confirm uniqueness, then enforce the constraints in a rebuilt/migrated table as SQLite requires.

The same identity pair should be added to `phrases`, `practice_events`, `lessons`, `asset_families`, `asset_variants`, `external_sources`, `asset_descriptions`, `scheduled_events`, `delivery_evidence`, `delivery_receipts`, and the rights/reconciliation tables as they are introduced.

## Seed-script requirements

Every seed script must follow the same idempotent rule:

1. Look up the intended record using its natural/semantic unique key.
2. Reuse its existing `uuid` and `public_ref` if the record already exists.
3. Generate both fields only when creating a genuinely new record.
4. Never regenerate either field on a later seed run.
5. Write a migration report listing records created, records preserved, and exceptions.

A seed helper can generate a public reference with collision checking:

```python
import secrets

ALPHABET = "23456789ABCDEFGHJKLMNPQRSTUVWXYZ"

def new_public_ref(prefix: str, exists) -> str:
    while True:
        code = "".join(secrets.choice(ALPHABET) for _ in range(6))
        candidate = f"{prefix}-{code}"
        if not exists(candidate):
            return candidate
```

Avoid confusing characters such as `0/O`, `1/I`, and `L` in short codes.

## Asset and derivative rules

A physical file is a variant; it is not automatically an independent learning concept.

| Example | Correct identity treatment |
|---|---|
| `bat.png` and `bat.svg` from OpenMoji | Two `asset_variants` linked to one `asset_family`; separate hashes and formats, shared family relationship. |
| Original Unsplash JPG and 512px WebP thumbnail | Source master and thumbnail variant; thumbnail is a derivative, not a new source. |
| A cropped card used in a video | `production_derivative` with a parent asset/family relation. |
| A translated audio file for a word sense | New media asset/variant linked to the word sense, language, speaker/model, and source text. |

Do not encode relationships exclusively in filenames. Record them in `parent_asset_uuid`, asset-family links, and purpose/variant fields.

## Recommended README wording

> **Identity and production naming.** Every ī-puāwai object receives a stable standards-based UUID and a short prefixed public reference. Identity is deliberately separated from language, curricular order, source, filename, and media version, because those details can evolve through community review. Human-readable production filenames remain useful for making and finding media, while relational records preserve the durable provenance and learning relationships behind them.

## Gentle implementation sequence

1. **Do not seed or export UUIDs today.** First commit the identity policy and remove the misleading `image_uuid` assumption from the word layer.
2. Add `uuid` and `public_ref` columns to the current schema and seed scripts.
3. Test the migration on a copied SQLite database, beginning with the 42 Kākano records and a handful of phonemes, words, senses, and assets.
4. Verify that re-running the seed scripts preserves the same IDs.
5. Expand to the 1,967 seeded words and onward to media assets.
6. Add the README wording only after the migration rule exists in code.

This approach keeps the Kākano, Papawai, existing Discourse topics, Eagle outputs, and production work safe. Nothing has to be renamed to gain a trustworthy identity layer.

## What not to do

- Do not derive identity from a translated word, an English gloss, an image filename, or a local drive path.
- Do not use `sequence_no` as an immutable ID; it is a curriculum ordering decision.
- Do not put all semantics into one identifier string.
- Do not call a descriptive semantic key a UUID.
- Do not regenerate identifiers when reseeding, translating, changing a filename, replacing a thumbnail, or revising a teaching statement.
- Do not require global UUIDs to be memorised by people; use the short prefixed public reference where a human needs to point to a record.

> **The UUID is the seed of identity. The public reference is the handle. The filename is the production label. The relationships are the living learning system.**
