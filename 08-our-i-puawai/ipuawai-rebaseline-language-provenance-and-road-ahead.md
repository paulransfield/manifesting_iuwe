# Ī-puāwai rebaseline: language, provenance, and the road ahead

**Status: a private clean foundation is operational; public source evidence is published; semantic, visual, and multilingual relationships remain deliberately governed work.**

Ī-puāwai is becoming a community-held language-and-provenance database. This document records where the work has recently been, what is now reliable, and the challenges that must be faced before the system can honestly present words, senses, images, translations, voice, and practice as connected learning relationships.

It is not a claim that the language bank is finished. It is a shared account of a transition: from a fast, informative minimum viable product to a more durable foundation where evidence is preserved, decisions are attributable, relationships can be reviewed, and future change does not need to begin from scratch.

> **A word form is not its meaning. A source occurrence is not curriculum authority. An available image is not an approved visual referent. A translation is not created by proximity. The relationships, their evidence, and the people authorised to review them are the living learning system.**

## Where we have recently been

The recent minimum viable product made Ī-puāwai visible quickly. It demonstrated that a local Flask, SQLite, Jinja, and Fomantic CSS application could show phonemes, words, a rotating visual carousel, and multilingual labels. That achievement matters. It gave the community and builders a working surface from which to learn.

At the same time, the MVP revealed the shortcuts that any rapid proof of architecture carries. The carousel’s English, Māori, Mandarin, and SVG associations were handwritten in route code. The legacy database combined older assumptions about identity, word records, phonemes, and media. A static image file could appear beside a word without an explicit record of whether the image was the right referent, whether the label was an approved language relationship, or whether the asset was ready for learning use.

The rebaseline does not dismiss the MVP. It treats it as **informative legacy evidence**. The visual interface, source material, early phoneme work, and practical lessons remain useful, but they are not allowed to become an unexamined design authority simply because they existed first.

## The rebaseline journey

The recent private work has followed one repeatable cycle:

```text
preserve → verify → test → change → inspect → local checkpoint → publish approved source evidence
```

This sequence is intentionally narrow. Before a database, parser, seed runner, or application boundary changed, the earlier state was copied into local evidence, hashed, and retained. Each change was tested twice where repeatability mattered. Earlier source material was preserved even where a later interpretation or curated successor was approved. Public Living Book publication followed the approved source lineage; the private application repository remained local.

| Rebaseline movement | What changed | What remained protected |
|---|---|---|
| Identity and clean schema | UUIDs, public references, foreign-key enforcement, and a disposable clean database baseline were established. | The legacy `ipuawai.db` remained untouched evidence. |
| Language and phoneme foundation | Three language records, five community records, and a transparent 689-record phoneme artifact were seeded. | Legacy scripts and their source evidence were retained. |
| Word-source provenance | Kākano 144, Dolch, raw Papawai v1, approved Papawai v2, and approved Papawai v3 were preserved as distinct source snapshots. | Earlier sources were not overwritten by later successors. |
| Papawai interpretation | The repeated final `category,word` row in raw v1 received a separate header-skip interpretation. | Raw v1 and its original historical membership record remained intact. |
| Curated successors | Papawai v2 added approved everyday transport coverage; v3 added an approved Health and Wellbeing boundary. | Decision ledgers, parent hashes, and earlier source snapshots remained visible. |
| Application proof | A read-only clean-schema Word Bank was added locally and tested. | Legacy routes, source artifacts, and persistent databases were not repurposed or rewritten. |

This is the practical change-control method now available to the community: a later improvement can be proposed, reviewed, attributed, tested, and recorded without making the past disappear.

## Where we are now

The private clean development database is at **schema version 4**. It has a UUID and public-reference identity foundation, enforced SQLite foreign keys, three language records (`eng`, `mri`, `cmn`), and five community records. Māori dialect records are intentionally not fabricated: recognised dialect relationships require their own language-scoped community authority and are not represented as country-code substitutes.

The present foundation contains a transparent 689-record phoneme seed and retained community associations. It also contains 1,909 canonical English word records, each with a stable UUID and `w-...` public reference. These canonical records resolve forms across five immutable source snapshots—Kākano 144, Dolch, raw Papawai v1, approved Papawai v2, and approved Papawai v3—while retaining 4,826 historical source memberships.

| Record type | What it now establishes | What it does **not** establish by itself |
|---|---|---|
| Language | A distinct language record and code boundary. | A translation, dialect claim, or learning priority. |
| Phoneme | A language-linked sound record with transparent seed provenance. | A word sense, spoken-audio asset, or final pedagogical sequence. |
| Canonical word | A normalised English word form with stable identity. | Its only meaning, an approved translation, a visual referent, or curriculum authority. |
| Source snapshot | A byte-identifiable, attributable source artifact at a point in time. | A closed canon or an instruction to replace earlier evidence. |
| Source membership | Evidence that a word occurred in a named source, category, and row context. | A duplicate word identity, a word sense, a translation, or a visual link. |
| Public reference | A short, stable human-facing handle for a record. | A production filename, CRM identifier, or external-platform claim. |

The local read-only Word Bank now provides a small but important proof: canonical English words and retained source memberships can be displayed from the clean schema without using the legacy Word ORM or modifying the database. This is an application proof, not yet a public deployment claim.

## What the source lineage means

The public [foundation-word artifacts](02-language-bank-and-phonemes/01-foundation-word-lists/) preserve Kākano, Dolch, and Papawai evidence rather than presenting a single final list. Kākano 144 remains a community-governed ordered source, with `now` as its intentional opening attention cue and `always` as its intentional continuity signal. Dolch remains an attributable source corpus. Raw Papawai v1 remains preserved even though its final repeated `category,word` row required a separate, attributable header-skip interpretation.

Papawai v2 and v3 are separate approved successors. They do not rewrite v1. V2 records reviewed removals, broad everyday transport additions, recategorisations, and retained `Boat`. V3 retains v2 occurrences and adds the separately approved Health and Wellbeing boundary. The decision ledgers and source specifications make each transition inspectable.

An overlapping word form therefore appears once as a canonical identity while retaining many source memberships. This preserves continuity and revision without asking a later list to erase the lived history of an earlier one.

## The live challenges ahead

The difficult work is no longer primarily about making a page render. It is about recording relationships honestly enough that a page can be trusted.

### 1. From word form to reviewed sense

A word is not enough to identify a learning object. `bat`, for example, may name a flying animal, a cricket implement, or a baseball implement. The clean schema already reserves separate records for `word_senses`, sense relations, dialect associations, and links to visual treatments. The task ahead is to populate these relationships through a controlled, reviewable catalogue rather than infer them from a word list.

### 2. From available file to accountable asset

The project currently holds legacy carousel SVGs and a large local OpenMoji collection. These are useful **asset evidence**. They are not automatically approved content assets, correct referents, translations, or curriculum choices.

A trustworthy visual relationship requires its own path: source and rights context, stable asset identity, family and variant relationships, description or review, and an explicit link to the sense it is intended to support. This is why an asset filename, a nearby emoji, an image-search result, or the local availability of an OpenMoji file must never decide what belongs in Papawai, Kākano, or another learning collection.

### 3. From legacy carousel to governed presentation

The present hard-coded carousel is legacy display evidence, not a translation catalogue, sense catalogue, approved visual inventory, or curriculum authority. Its handwritten English, Māori, Mandarin, and SVG associations need separate review before they become clean records.

The next carousel path must read only from an approved relationship chain:

```text
canonical word
    → reviewed language-specific word sense
        → reviewed visual or media relationship
            → governed carousel eligibility and presentation
```

Words without approved visuals remain valid language-bank records. Visual availability must never decide curriculum membership. Carousel eligibility must be a reviewable and reversible presentation decision, not an image-led filter on what counts as worth learning.

### 4. Multilingual relationships without mechanical equivalence

The system already distinguishes English, Te Reo Māori, and Mandarin language records. It must now avoid collapsing them. A translation relationship, a sense relationship, a dialect relationship, a learner statement, and a voice rendering are different records with different review needs. The bilingual sense-link proof and later translation work therefore remain governed stages, not automatic transformations of English source words.

### 5. Voice, phrase, practice, and delivery remain later layers

Future voice work must distinguish a voice model/provider/version from the identity of the audio asset it produces. Phrase patterns belong to the phrase module, not an overextended word record. Practice events, scheduled delivery, evidence, receipts, CRM integration, and automatic Discourse links remain deliberately deferred until their own relationship and governance boundaries are ready.

## Boundaries that protect the work

The following constraints are active design commitments, not temporary inconveniences.

| Boundary | Meaning |
|---|---|
| Preserve source evidence | Source CSVs and the legacy database are never silently edited to make them look tidier. |
| Keep identities distinct | UUID/public reference, source row, filename, asset identity, sense, translation, and production label do not substitute for one another. |
| Prefer successors to overwrites | Later curation creates a new attributable source or relationship record while earlier evidence remains inspectable. |
| Do not let images choose curriculum | Picturability, OpenMoji availability, or an existing SVG cannot decide membership in a foundation collection. |
| Do not auto-link community systems | Discourse remains staging-only until reviewed; missing EspoCRM information does not block transparent local seeding. |
| Keep kaitiaki authority visible | Language, cultural, rights, pedagogical, and Wairuatanga questions remain subject to appropriate community review. |
| Keep operational tables deferred | Billing, receipts, schedules, ITIL structures, and wider delivery operations are not smuggled into a language-foundation change. |

## What is operational, under test, and deliberately deferred

| Status | Present scope |
|---|---|
| **Operational private foundation** | UUID/public references; foreign-key protection; clean schema version 4; language/community reference seed; phoneme seed; immutable word-source snapshots and memberships; Papawai interpretation and successor lineage; repeat-safe seed runners; local read-only Word Bank proof. |
| **Under test** | Controlled word-sense catalogue; sense-to-visual relationships; governed carousel data path; asset registration and review workflow; bilingual relationship proofs. |
| **Designed next** | Approved translations and learner statements; voice and TTS attribution; phrase patterns; production agreements; practice-event and delivery relationships. |
| **Deferred by design** | Automatic Discourse linking, CRM dependency during seeding, billing/receipts, scheduled-event operations, image-led curriculum selection, and unreviewed Wairuatanga vocabulary proposals. |

The source CSV artifacts remain immutable. The legacy `ipuawai.db` remains preserved evidence and is not a target for this rebaseline. The current `ipuawai_next.db` is a disposable, rebuildable clean development database; it is not itself published as an authoritative public artifact.

## How change can remain healthy

Ī-puāwai is relational rather than transactional. It provides a technical structure for reciprocity, correction, and continuity, but it does not replace the people who hold language, rights, pedagogical, and cultural authority.

Community kaitiaki may review, correct, approve, defer, or decline relationships. A later decision creates an attributable successor or relationship record; it does not silently rewrite source evidence. The Living Book records enough context for a future whānau member, developer, researcher, or AI to distinguish source from interpretation, proposal from approval, historical evidence from current use, and technical capability from community authority.

This is the practical value of the rebaseline: not that change becomes slow, but that change becomes **legible**. A community can make a narrow decision while the lived reason for it is still present, retain the evidence, and let future people understand how and why the system moved.

## Reading the public record

The practical record is distributed deliberately:

| Living Book location | Purpose |
|---|---|
| [01 — identity and provenance](01-identity-and-provenance/) | Stable identity, source, rights, derivative, and production relationship principles. |
| [02 — language bank and phonemes](02-language-bank-and-phonemes/) | Phoneme evidence, foundation-word sources, and approved Papawai successor lineage. |
| [03 — senses and concept domains](03-senses-and-concept-domains/) | The distinction between word form, referent, language-specific sense, and teachable use. |
| [04 — media intelligence](04-media-intelligence/) | Asset review, descriptions, and the pathway from media evidence to accountable content assets. |
| [07 — community review and resolution](07-community-review-and-resolution/) | The review, correction, pause, and resolution pathways that keep the system responsive. |

The [main Living Book](../README.md) provides the wider operating context: the public operating manual, the dated Hau progress archive, and the architectural map. Together they should be read as a time-aware evidence set, not a prospectus claiming that every designed relationship is already operational.

> **The UUID is the seed of identity. The public reference is the handle. The source membership is the historical trace. The reviewed relationships are the living learning system.**

---

## Publication note

This account describes the August 2026 private rebaseline evidence and public source-artifact lineage. It is not a curriculum decision, language authority, translation approval, asset licence statement, or substitute for community review. It records the recent journey, present foundation, live challenges, and working boundaries so that later technical and community decisions can remain explicit, attributable, and revisable.
