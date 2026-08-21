# Ī-puāwai rebaseline: language, provenance, and the road ahead

**Status: a private clean schema-v6 Progressive Deterministic learning foundation is operational; public source and reference evidence is published; one sealed 20-card Task A source-evidence package has been structurally verified in private; semantic, visual, multilingual, crosswalk, curriculum, and community-review relationships remain deliberately governed work.**

Ī-puāwai is becoming a community-held language-and-provenance database. This document records where the work has recently been, what is now reliable, and the challenges that must be faced before the system can honestly present words, senses, images, translations, voice, and practice as connected learning relationships.

It is not a claim that the language bank is finished. It is a shared account of a transition: from a fast, informative minimum viable product to a more durable foundation where evidence is preserved, decisions are attributable, relationships can be reviewed, and future change does not need to begin from scratch.

> **A word form is not its meaning. A source occurrence is not curriculum authority. An available image is not an approved visual referent. A translation is not created by proximity. The relationships, their evidence, and the people authorised to review them are the healthy living social learning system.**

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
| Relationship reference foundation | Schema v5 introduced governed reference capacity. The 25 provisional sense domains, eight faculty spaces—including Wairuatanga as an equal faculty space under equitable governance—and the Papawai root with Phonemes, Oracy, Literacy, and Numeracy child layers were seeded through checksum-verified, repeat-safe ledgers. | No faculty/domain or foundation/domain crosswalk, learning statement, word sense, asset, visual, translation, phrase, curriculum sequence, or carousel decision was implied. |
| Progressive Deterministic learning foundation | Schema v6 added thirteen empty relational tables for future learning statements, controlled relationships, evidence-bearing progression, and reviewable learning-event work. | Empty relationship capacity did not manufacture a word sense, learning statement, crosswalk, asset relationship, curriculum sequence, or learning event. |

This is the practical change-control method now available to the community: a later improvement can be proposed, reviewed, attributed, tested, and recorded without making the past disappear.

## Where we are now

The private clean development database is at **schema version 6**, the Progressive Deterministic learning foundation. It retains a UUID and public-reference identity foundation, enforced SQLite foreign keys, three language records (`eng`, `mri`, `cmn`), five community records, 25 provisional sense-domain identities with first review records, eight faculty-space reference identities, and a Papawai root with Phonemes, Oracy, Literacy, and Numeracy child reference identities. Schema v6 adds thirteen empty relational tables for future learning statements, controlled relationships, evidence-bearing progression, and reviewable learning-event work. The tables are intentionally empty: their presence establishes accountable capacity without manufacturing relationships in advance. Māori dialect records are intentionally not fabricated: recognised dialect relationships require their own language-scoped community authority and are not represented as country-code substitutes.

The present foundation contains a transparent 689-record phoneme seed and retained community associations. It also contains 1,909 canonical English word records, each with a stable UUID and `w-...` public reference. These canonical records resolve forms across five immutable source snapshots—Kākano 144, Dolch, raw Papawai v1, approved Papawai v2, and approved Papawai v3—while retaining 4,826 historical source memberships.

| Record type | What it now establishes | What it does **not** establish by itself |
|---|---|---|
| Language | A distinct language record and code boundary. | A translation, dialect claim, or learning priority. |
| Phoneme | A language-linked sound record with transparent seed provenance. | A word sense, spoken-audio asset, or final pedagogical sequence. |
| Canonical word | A normalised English word form with stable identity. | Its only meaning, an approved translation, a visual referent, or curriculum authority. |
| Source snapshot | A byte-identifiable, attributable source artifact at a point in time. | A closed canon or an instruction to replace earlier evidence. |
| Source membership | Evidence that a word occurred in a named source, category, and row context. | A duplicate word identity, a word sense, a translation, or a visual link. |
| Public reference | A short, stable human-facing handle for a record. | A production filename, CRM identifier, or external-platform claim. |
| Sense domain | A changeable organising territory with its first attributable provisional review record. | A dictionary meaning, word list, faculty assignment, foundation assignment, asset category, or carousel rule. |
| Faculty space | An attributable broad social-learning reference identity. | A curriculum subject, domain crosswalk, word membership, or permanent cultural authority. |
| Papawai foundation layer | An attributable Papawai umbrella or child reference identity. | A prescribed sequence, crosswalk, word membership, or learner statement. |

The local read-only Word Bank now provides a small but important proof: canonical English words and retained source memberships can be displayed from the clean schema without using the legacy Word ORM or modifying the database. This is an application proof, not yet a public deployment claim.

## What the source lineage means

The public [foundation-word artifacts](02-language-bank-and-phonemes/01-foundation-word-lists/) preserve Kākano, Dolch, and Papawai evidence rather than presenting a single final list. Kākano 144 remains a community-governed ordered source, with `now` as its intentional opening attention cue and `always` as its intentional continuity signal. Dolch remains an attributable source corpus. Raw Papawai v1 remains preserved even though its final repeated `category,word` row required a separate, attributable header-skip interpretation.

Papawai v2 and v3 are separate approved successors. They do not rewrite v1. V2 records reviewed removals, broad everyday transport additions, recategorisations, and retained `Boat`. V3 retains v2 occurrences and adds the separately approved Health and Wellbeing boundary. The decision ledgers and source specifications make each transition inspectable.

An overlapping word form therefore appears once as a canonical identity while retaining many source memberships. This preserves continuity and revision without asking a later list to erase the lived history of an earlier one.

## Stage 15 — first sealed Task A source-evidence package

On 22 August 2026, Ī-puāwai completed its first small, deterministic Task A source-evidence package. The result is a **private, sealed, read-only 20-card review package**, created from the declared Common-Core image cohort and retained WordSet source evidence. It is a technical and provenance milestone, not a declaration that the underlying meanings have been accepted.

The sealed package manifest has SHA-256 fingerprint:

```text
5F5D4F0B4FE655CD28D54B5C78C3C0D8F60FBF14F1B5389AE4816F4881A4A13D
```

The package is retained in a private evidence location and is **not** uploaded to this public repository. It contains 61 read-only files arranged as twenty independently inspectable candidate-card directories. The inspection confirmed all of the following.

| Verified private evidence fact | What it establishes | What it does **not** establish |
|---|---|---|
| Twenty cards were created and structurally verified. | Each selected Common-Core candidate has a durable review object with its full filename identity, selection order, variant identity, and copied-image hash. | A correct image-to-meaning relationship, curriculum membership, or pedagogical sequence. |
| Twenty of twenty cards preserve an exact WordSet entry. | Each card retains the complete exact-key WordSet record used as candidate meaning evidence, with a source-entry fingerprint and source-file fingerprint. | A local Ī-puāwai word sense, a preferred definition, or an accepted use for a learner. |
| WordSet documentation travels with the evidence chain. | The required `Readme.md`, `Guidelines.md`, and `LICENSE` bundle fingerprints are recorded with every card. WordSet remains on-demand candidate evidence, not a bulk import. | A release of WordSet content into Ī-puāwai, a replacement for source attribution, or a licence conclusion beyond the retained documentation. |
| Strict source selection admitted 28 eligible WordSet JSON objects. | A known malformed non-entry file was excluded only through a declared path-and-hash-bound exception. | A claim that all files in an upstream release are homogeneous data records. |
| The package is sealed read-only. | The package can be opened for review without silently altering the source-evidence object. | An immutable public record or a substitute for review decisions. |
| Protected database hashes remained unchanged. | Neither the preserved legacy database nor the clean schema-v6 database was modified while creating or inspecting the package. | That card content has been ingested into any database table. |
| The earlier partial output remains quarantined. | The first failure remains available as evidence and was not overwritten, reused, or represented as the successful package. | That failure has been erased or its lessons hidden. |

The Task A evidence boundary is intentionally narrow:

```text
declared image candidate
    → exact WordSet source-evidence entry, where found
        → sealed, unreviewed review card
            → provisional human assessment
                → separate local word-sense proposal work (Task B)
```

The sealed 20-card package is ready for the next provisional human review gate by **Paul Ransfield, Kapai Group**, until community editorial teams are enabled. At the date of this publication, all human-review fields remain empty and every card is marked `unreviewed`.

It does **not** claim that any image-to-meaning decision has been accepted; that Task B, the separate local word-sense proposal process, has begun or been completed; that any WordSet material has been adopted as an Ī-puāwai meaning; that a card has been ingested into the private database; that an image establishes curriculum, faculty, Papawai, or visual-eligibility membership; or that a translation, voice, learner statement, practice event, or public release right exists. AI-assisted work, where used in later proposal processes, remains a disclosed proposal envelope with its input and output evidence; it is not a source citation and does not substitute for human or community authority. No AI request was made while the sealed 20-card package itself was created or inspected.

## Preserve, Verify, Test, Change, Release

The operating rhythm behind the rebaseline is deliberately simple:

```text
Preserve → Verify → Test → Change → Release
```

It is not a slogan added after the fact. It is the enforced order that allowed the Task A work to move quickly without treating speed as permission to lose evidence, overwrite a failure, or publish a claim ahead of its review. **Inspection is the active check between change and release:** a change does not become releasable merely because code ran; it becomes releasable only after its outputs, boundaries, and preserved predecessors have been inspected.

| Rhythm | Enforced practice in the Task A 20-card path | Why it protects velocity with a memory |
|---|---|---|
| **Preserve** | The legacy and clean databases were hash-protected; the sealed source transfer and documentation bundle remained read-only; the first one-image partial result and the malformed non-entry source were quarantined as forensic evidence. | A defect did not erase the state needed to understand it. The next attempt began with evidence, rather than recollection or reconstruction. |
| **Verify** | Source-file hashes, database hashes, selection-ledger identity, documentation-bundle fingerprints, approved runner bytes, output-root absence, and the recovery boundary were checked at each gate. | The team could distinguish a genuine environmental or source irregularity from a changed input, an altered script, or a false assumption. |
| **Test** | Focused regression tests grew from 11 to 19; the full suite grew from 109 to 117 passing tests. Tests were added for BOM compatibility, the production baseline constant, strict source eligibility, and atomic output. | The repair retained a memory in executable form, reducing the chance that a later fast change would recreate a known failure. |
| **Change** | Repairs were intentionally narrow: accept BOM-marked sealed inputs, correct the transposed protected-database hash literal, validate source eligibility before output, use a declared path-and-hash-bound exception, preload exact-key evidence, then stage and atomically promote a completed package. | The implementation moved forward without broadening authority, changing source material, mutating either protected database, or silently normalising an irregular upstream file. |
| **Release** | The successful retry1 package was sealed read-only only after complete validation and was then independently inspected. Public release remains a separate, later decision; this Living Book update records the milestone without publishing private evidence contents or claiming a semantic decision. | Release is a governed boundary, not a by-product of a successful script. What becomes visible is limited to what has earned a truthful, inspectable status. |

> **Velocity with a memory** is the consequence of this rhythm. Preservation prevents the past from disappearing; verification makes the present legible; tests keep a repair alive; narrow change maintains authority boundaries; and release occurs only when the result can be named accurately without outrunning its evidence.

The Task A path also shows why mundane technical detail belongs in a public account of care. A byte-order mark, a transposed hash character, a malformed JSON specimen in a data directory, an early output-root creation, or a one-item PowerShell enumeration defect can each become an untraceable source of error when treated as mere inconvenience. Under this rhythm, each was contained, inspected, and either preserved as evidence or translated into a specific test and repair.

## Velocity with a memory: what it took to reach the package

The successful package was not produced by assuming that valid logic meets a uniform world. It required the system to meet ordinary but consequential differences between operating-system tooling, filesystem encoding, upstream release habits, and output-ordering behaviour. The journey is therefore part of the evidence, not an embarrassment to edit out.

The first real package attempt failed safely after creating only a single copied image. That partial output was quarantined and preserved as read-only forensic evidence. The work then proceeded through **three distinct repair cycles** before a new retry output root was created and sealed successfully.

| Repair cycle | Mundane but material condition encountered | Repair outcome |
|---|---|---|
| UTF-8 BOM compatibility | Windows PowerShell emitted UTF-8 files with a byte-order mark, while the original reader expected plain UTF-8. | Input readers were hardened for BOM-marked sealed evidence without weakening hash or source checks. |
| Protected-database baseline guard | A transposed character in a fixed legacy-database SHA-256 literal caused the correct protected baseline to be rejected. | The literal was corrected and an independent regression test was added so the production constant itself is checked. |
| Strict source selection and atomic output | The WordSet release directory contained `data model.json`: a Kapaigroup draft data-model specimen rather than a valid entry object. The earlier package flow also created its output root before all source validation had finished. | The packager now validates each manifest-bound source before package output; excludes only the known path-and-hash-bound non-entry; preloads exact-key lookups; stages work in a sibling directory; and promotes the sealed root only after complete validation. |

The change history involved approximately **five to six distinct patch applications or repair-patch iterations** across the candidate packager and focused tests, including patch syntax revisions and evidence-guide corrections. The guides themselves required multiple precision iterations: the atomic-output checkpoint progressed through four reviewed versions, while related preflight work progressed through three versions. Those iterations resolved PowerShell parsing and single-item filesystem-enumeration behaviour in the evidence tooling, not merely the Python business logic.

The initial candidate packager and focused test module introduced approximately **784 lines**. The two most visible later committed repair changes affected a further **281 lines of code and tests** (15 lines for the protected-baseline correction and 266 changed lines for strict source selection and atomic output), with an additional smaller BOM compatibility repair. As a useful planning estimate, the working package path therefore represents **roughly 1,000 lines of implementation and regression-test change volume**, excluding the separately versioned PowerShell checkpoint, preflight, transfer, recovery, and execution guides. This is an effort estimate rather than a productivity metric: it records the scope required to contain, evidence, and repair real-world irregularities.

The focused test suite grew from **11** original packager tests to **19** after the atomic-output repair. The full private suite rose from **109** to **117** tests, all passing at the successful retry checkpoint. The value of those additions is not a headline test number. It is that the system now refuses unsafe source selection or partial output before it can be mistaken for completed evidence.

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
| Keep kaitiaki authority visible | Language, cultural, rights, pedagogical, and Wairuatanga questions remain subject to appropriate community review; Wairuatanga is an equal faculty space under equitable governance, not an exceptional or quarantined space. |
| Keep operational tables deferred | Billing, receipts, schedules, ITIL structures, and wider delivery operations are not smuggled into a language-foundation change. |

## What is operational, under test, and deliberately deferred

| Status | Present scope |
|---|---|
| **Operational private foundation** | UUID/public references; foreign-key protection; clean schema v6 Progressive Deterministic foundation with thirteen empty future-relationship tables; language/community reference seed; phoneme seed; immutable word-source snapshots and memberships; Papawai interpretation and successor lineage; 25 provisional sense domains with first reviews; eight attributable faculty spaces with Wairuatanga recognised as an equal space under equitable governance; Papawai root with Phonemes, Oracy, Literacy, and Numeracy child references; repeat-safe seed runners; local read-only Word Bank proof. |
| **Under test** | The first sealed 20-card Task A source-evidence package; provisional human image-to-meaning review; controlled word-sense catalogue; sense-to-visual relationships; governed carousel data path; asset registration and review workflow; bilingual relationship proofs. |
| **Designed next** | Reviewed faculty/domain and foundation/domain crosswalks; reusable 144-character learning statements; Task B local word-sense proposal work; approved translations; voice and TTS attribution; phrase patterns; production agreements; practice-event and delivery relationships. |
| **Deferred by design** | Automatic Discourse linking, CRM dependency during seeding, billing/receipts, scheduled-event operations, image-led curriculum selection, the ingestion of unreviewed Task A package content, and public release of private candidate evidence. |

The source CSV artifacts remain immutable. The legacy `ipuawai.db` remains preserved evidence and is not a target for this rebaseline. The current `ipuawai_next.db` is a disposable, rebuildable clean development database; it is not itself published as an authoritative public artifact.

## How change can remain healthy

Ī-puāwai is relational rather than transactional. It provides a technical structure for reciprocity, correction, and continuity, but it does not replace the people who hold language, rights, pedagogical, and cultural authority.

Community kaitiaki may review, correct, approve, defer, or decline relationships. A later decision creates an attributable successor or relationship record; it does not silently rewrite source evidence. The Living Book records enough context for a future whānau member, developer, researcher, or AI to distinguish source from attribution, sign-off from source, proposal from approval, historical evidence from current use, and technical capability from community authority.

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

This account describes the August 2026 private rebaseline evidence, the private schema-v6 Progressive Deterministic learning foundation, and the first sealed 20-card Task A source-evidence package. It is not a curriculum decision, language authority, translation approval, asset licence statement, WordSet republication, semantic acceptance, database-ingestion record, or substitute for community review.

The package manifest fingerprint is published only as a transparent integrity reference. The package contents, exact local evidence location, selected imagery, WordSet entry copies, and still-unreviewed human-review materials remain private. Future public updates will record accepted decisions only after the relevant review and authority pathways have occurred.
