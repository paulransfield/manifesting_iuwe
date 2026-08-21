# From Curated Media to Federated Learning Event

## A Companion White Paper for the ī-puāwai Learning-Event Provenance JSON

**Status:** Discussion and operating-design paper; no implementation, publication, bulk ingestion, distribution, message dispatch, or learner-data operation is proposed by this document.

**Prepared for:** Consideration in the ī-puāwai Living Book

**AI++ co-design:** **Manus and Paul Ransfield**

**Co-design acknowledgement:** This paper is informed substantively by Paul Ransfield’s long-term media, language, operating-model, and community-design work, and by the human–AI R+D undertaken with Manus. This acknowledgement does not substitute for future kaitiaki, community, source-rights, language, or publication authority.

**Date:** 22 August 2026

## Executive proposition

The ī-puāwai Learning-Event Provenance JSON memorandum explains how one assembled learning event can be represented truthfully at a declared point in time: what was assembled, what evidence is available, what remains provisional or unknown, and what distribution invitation may belong with the event. [1] This companion paper describes the operating pathway that produces those event components without collapsing human judgement into either a filename, an AI output, or an export file.

The proposed workflow is deliberately hybrid. **Human curation establishes purpose, source boundaries, and cultural responsibility. OpenCLIP makes large local visual repositories discoverable. Eagle AI tests visual grounding and drafts age-specific teaching language. Several voice pathways can provision word and phrase audio under explicit review conditions. Python assembles approved components into deterministic media outputs. The federated `iho.{community}` network provides a community-specific publication context. SMS can provide a pinpointed invitation path only where the separate recipient, consent, and delivery controls are appropriate.**

### Public status legend

| Status | Meaning in this paper |
|---|---|
| **Operational local interface** | A reviewed local script or workflow exists. It is not necessarily publicly deployed or populated with every relational record. |
| **Local proof / under test** | A bounded cohort, workflow, or evidence path has been exercised or designed for a narrow purpose. It is not a general release claim. |
| **Designed next** | An explicit intended pattern awaiting a separate approval and implementation boundary. |
| **Community/Kaitiaki decision required** | Technical preparation does not establish authority to use, publish, teach, or invite. |

| Pathway | Public-facing status at this revision | Boundary |
|---|---|---|
| OpenCLIP discovery and readable-prefix workflow | **Local proof / under test** | Supports visual discovery and bounded production preparation; it does not confirm a word sense, licence, or release decision. |
| Eagle visual grounding and multi-register captions | **Local proof / under test** | Produces constrained candidate language and can reject an incorrect cue; it does not replace editorial, language, or kaitiaki review. |
| TTS and voice routes | **Designed next / Community/Kaitiaki decision required** | Technical routes may be researched or locally tested, but voice, language, and release suitability require their own authority and review. |
| Deterministic event assembler | **Designed next** | The event-script and manifest contract define the pattern; a separately approved implementation must establish its actual outputs and controls. |
| `iho.{community}` event context | **Designed next / Community/Kaitiaki decision required** | A destination does not imply that a community has accepted a specific event revision. |
| SMS linking layer | **Designed next / Community/Kaitiaki decision required** | The public event object can record intent only; consent, recipient data, dispatch, and delivery remain separate controlled matters. |

No stage is authoritative merely because it is automated. The event is strengthened by the fact that each stage leaves a bounded, reviewable record for the next stage. This is a practical form of collective advantage: communities can reuse shared operating patterns without surrendering their own language, source, voice, publication, or learner-relationship decisions.

The visual repository is the material foundation of this proposal. The relevant working collection is estimated at approximately **11,000 Adobe-derived source illustrations**, pending asset-level source and rights registration. The supplied Adobe account screenshot separately shows **9,035 assets** in one point-in-time licence-history view; the two figures have different scopes and neither is an authoritative rights inventory. Where a retained parent asset is an editable vector file, it may support derivative treatments—such as resizing, text cleaning, recolouring, cropping, card formatting, or animation—subject to applicable source terms, purpose, and review. Until recently, that abundance was chiefly latent potential: valuable source media whose opaque filenames and accumulated local duplicates made systematic selection prohibitively slow. The Python utility pathway—inventory, hashing, vocabulary sanitation, OpenCLIP discovery, manifest building, controlled queue movement, and Eagle output—turns that latent repository into a **curatable** resource without pretending that it is already fully mapped, semantically confirmed, or cleared for every future use. [2]

> **The script is the pivot.** Once a reviewed event script identifies its visual, word, phrase, language form, voice route, component order, and delivery intent, the same learning intention can be assembled across languages, platforms, schedules, and community contexts without rebuilding the event from placeholders each time.

## 1. Relationship to the provenance JSON memorandum

The two documents have separate responsibilities.

| Document | Primary question | Main output | What it does not do |
|---|---|---|---|
| **Learning-Event Provenance JSON memorandum** | “What can be truthfully asserted about this assembled event at this export time?” | Immutable, hashable event-level projection with component, review, publication, and invitation states. [1] | It does not generate media, decide meaning, send SMS, assert delivery, or replace the relational database. |
| **This workflow paper** | “How do people and systems prepare reviewable components for such an event?” | A repeatable human–AI operating pathway with gates, roles, and evidence hand-offs. | It does not define a final schema, automate community approval, or grant release authority. |

The provenance JSON should remain a **read-only projection** of a declared event revision. The workflow described here is the preceding operational chain. Its purpose is to make it possible for an exporter to say, accurately, which media, text, sound, review references, and delivery intent were assembled—without asserting that every production label is a confirmed word sense, every source is cleared for every use, or every invitation was delivered. [1]

> **The event-provenance JSON is intentionally rich enough to resemble a working model of a learning event. Its authority is nevertheless narrow:** it is an immutable, versioned projection of one declared event revision at one export time. It may carry component, publication, invitation, and contribution-offer context, but it does not become the mutable system of record for rights, kaitiaki decisions, local word senses, recipient consent, recipient data, payment or receipt records, or later corrections. Those relationships remain normalised, reviewable, and access-controlled in their appropriate systems. [1]

## 2. The operational problem: visualising concepts at scale

In this project space, text and sound can usually be drafted, translated, rendered, or rerecorded comparatively quickly once the intended learning relationship is known. The slow, scarce, provenance-heavy layer is the visual: finding an appropriate asset, understanding what it shows, connecting it to its parent source, checking whether it belongs in a teaching event, and preserving enough context that it can be found again.

This is the recurrent sticking point in learner-facing media. A book, card, video minute, or mobile learning screen may carry few words, but a substantial share of its available space, attention, design labour, and memory is carried by the image. A word list can be extended quickly; a suitable visual must be found or made, checked for its visible meaning, related to a source and derivative history, and made available in the right production form. The challenge is not merely “add pictures to text.” It is to give thousands of concepts enough appropriate visual treatments that the teaching experience is varied, memorable, and reusable.

The workflow therefore begins with the visual archive, not because the visual is the only learning component, but because it is the constraint that most often prevents a script from becoming a reusable event.

### 2.1 The “free” visual-licence conundrum

The practical issue is illustrated by a supplied Adobe Creative Cloud licence-history view. It shows an extensive history of assets presented as `Free` in the Adobe interface, while also showing the operational gap that begins after download: a local working file may retain an `AS_…`-style production reference and a parent-source relationship without retaining a human-readable clue to what an individual illustration depicts. The screenshot supports the R+D question of relating local production references to an Adobe asset-ID and licence-history context; it does not prove a one-to-one mapping for any depicted item. It is collection and workflow context only, not evidence of the scope, duration, derivative rights, attribution requirements, territory, account terms, or suitability of any particular asset for a particular future use. Each selected learning asset still requires its own source-register pointer, parent/derivative relationship, and applicable rights/review state. [5]

![Adobe Creative Cloud licence-history interface, August 2026, showing asset identifiers and a `Free` display label. The figure is operational context only.](../../images/evidence/adobe-license-history-free-assets-context-2026-08.png)

> **Figure 1 — Adobe licence-history R+D context, August 2026.** This point-in-time account-interface capture records Adobe asset-ID and `Free` display context while R+D investigates how local `AS_…`-style production references may be related to parent-source records. It does **not** assert a one-to-one mapping, identify files selected for Ī-puāwai use, prove the scope or duration of any asset right, establish derivative permission or attribution requirements, or determine suitability for learning use. Each selected asset requires its own source-register pointer, parent/derivative relationship, and applicable rights and review state. [5]

The manual burden is large even before any semantic, provenance, or educational review begins. As an illustrative planning allowance, **11,000 derivatives at 3.27 minutes each equal approximately 600 hours**:

```text
11,000 images × 3.27 minutes per image ÷ 60 = 599.5 hours (approximately 600)
```

Even an unrealistically clean three-minute process would still require 550 hours. Neither estimate includes source registration, duplicate resolution, rights/MoW context, category choice, sense review, captioning, translation, sound, video assembly, or any later community review. The role of the Python/OpenCLIP/Eagle pathway is therefore not to claim that the visual work disappears; it is to reduce blind manual searching and naming into a bounded review task with retained source evidence.

```text
source parent and derivative
        ↓
findable visual candidate
        ↓
truthful visual grounding
        ↓
reviewed word and phrase
        ↓
word sound + phrase sound
        ↓
assembled learning event
        ↓
federated publication context
        ↓
SMS invitation to an eligible learner relationship
```

The result is not a claim that an archive has been completely cleaned, that a model has decided meaning, or that a community has approved every component. It is a way to make selected media **available for deliberate learning design** while preserving the parent source, model evidence, review boundaries, and later ī-puāwai relationships.

| From latent repository | Through the Python-supported workflow | To curatable learning media |
|---|---|---|
| Unnamed vector parent sources and opaque derivative exports | Inventory and hash preservation; controlled candidate vocabulary; OpenCLIP top-five evidence; editable manifest; dry-run-first queue move | Searchable visual candidates with readable labels, parent-source continuity, a provisional work category, and a defined review route |
| Large local collections with duplicates and uncertain reuse history | Source-family boundaries, manifests, parent/derivative distinctions, and exception logs | Bounded cohorts that can be selected without claiming that the whole repository has been resolved |
| Concepts lacking a usable visual treatment | Human selection, category queues, Eagle visual grounding, and later word–sound/event assembly | A chosen visual can become part of a reviewable learning-event script |

## 3. The learning-event script as the primary design object

A learning-event script is not merely narration. It is a structured declaration of a small teachable moment. It should be capable of being read by a human, prepared by local utilities, rendered into a one-minute event, and later projected into an event-level provenance manifest.

A minimal script may declare:

| Script element | Purpose | Illustrative status boundary |
|---|---|---|
| `event_ref` and revision | Stable event handle independent of filenames and spreadsheet rows. | Assigned only under an approved identity rule. |
| Learning intention | The human purpose of the event. | May be provisional until curriculum or kaitiaki review. |
| Visual component(s) | Selected derivative(s) and their parent/source references. | Source identity can be known while semantic appropriateness remains pending. |
| Core word | The learner-facing word or concept label. | A production word is not automatically a confirmed local word sense. |
| Phrase / teaching statement | Adult, Child, Grandparent, OET, or other declared register. | Eagle draft text remains candidate language until selected or edited. |
| Language form and script | Language code, approved text, transcription, and phoneme relation where applicable. | Must not be inferred from a filename or generic translation. |
| Word sound and phrase sound | Voice route, audio assets, model/human source, and review status. | Placeholder audio must be visibly provisional where appropriate. |
| Component timing | Ordered duration and event composition rule. | Deterministic assembly can be known without asserting learning outcome. |
| Publication and invitation intent | Intended community, platform, schedule, and SMS template/reference. | Intent is not proof of dispatch, delivery, payment, or learning. |

This structure supports both direct instruction and open discussion. A simple script can start with a relational question such as, “Now, friend, what is the most important thing in the world?” and then be realised as a visual, spoken prompt, learner response invitation, phoneme exercise, or community discussion. The script is stable enough to support repeated assembly; the community context remains free to determine what answer, language, and relationship matter.

## 4. Formalised end-to-end workflow

### 4.1 The workflow at a glance

```text
Human curation and source care
        ↓
OpenCLIP archive discovery
        ↓
Manifested readable prefix + provisional category queue
        ↓
Eagle visual grounding + teaching-language candidates
        ↓
Kaitiaki / editorial / language review
        ↓
word sound + phrase sound through an appropriate voice route
        ↓
Python event assembly from approved component references
        ↓
immutable learning-event provenance JSON export
        ↓
federated iho.{community} publication context
        ↓
SMS invitation linking enablers and consenting learners
        ↓
practice, feedback, correction, and successor event revision
```

The arrows are not claims of automatic approval. They are controlled hand-offs. An item can be stopped, corrected, held, replaced, or excluded at every boundary.

### 4.2 Stage register

| Stage | Human responsibility | System assistance | Required artefact | Gate / exception route |
|---:|---|---|---|---|
| 0. Curate and preserve | Select a source family or a bounded visual cohort; maintain source and rights context. | File inventory and hashing utilities. | Source-register reference and parent/derivative rule. | Rights uncertainty, duplicate concern, or absent source context routes to hold; it is not silently released. |
| 1. Make visuals findable | Decide which archive area is worth preparing. | OpenCLIP ranks images against a controlled vocabulary and retains top candidates. | Discovery index with candidate scores, model/prompt/version, source path and parent reference. | Low-margin or unhelpful result remains a candidate/review item, not a false semantic decision. |
| 2. Establish production labels and queues | Inspect and correct proposed readable words and broad category context. | Manifest builder proposes `{word}_{queue_category}_{source_uuid}` labels; dry run validates paths, hashes, and collisions. | Editable manifest, apply log, derivative hash continuity. | Parent source inclusion, hash mismatch, duplicate hash, or target collision blocks the row. |
| 3. Ground the selected image | Choose one coherent category cohort and maintain a draft or canonical sense catalogue. | Eagle compares the actual image with allowed senses and drafts teaching registers. | Caption CSV with validation, visual/teaching sense, four registers, keywords, reason, raw output, runtime. | `MISMATCH` becomes a correction task; no invented captions are retained as clear evidence. |
| 4. Review language and learning purpose | Confirm, correct, or hold the selected visual–word–phrase relationship. | Editorial views, catalogue lookup, later ī-puāwai review records. | Kaitiaki/editorial decision, correction note, selected event-script fields. | AI proposals remain provisional until the designated review has occurred. |
| 5. Provision word and phrase sound | Select an ethical, technically suitable voice route. | Local TTS, MMS-TTS where supported, local cloned/permitted voice, premium TTS, or community recording. | Voice manifest, exact text, language/script, model or human source, file hash, listening-review state. | Absent model coverage or unapproved voice routes lead to `pending`, not simulated authority. |
| 6. Assemble the event | Declare component order, timing, on-screen text, visuals, word audio, phrase audio, and render profile. | Python assembles deterministic media outputs from reviewed component references. | Render specification, component playlist, output media reference and hash where verified. | A missing input, unknown source ID, or unreviewed required component blocks assembly or marks it appropriately. |
| 7. Project provenance | Decide what can truthfully be exported for a particular event revision. | Read-only exporter creates versioned JSON, canonicalises payload, and hashes declared content. | `io.iuwe.learning-event-provenance/v0.1` manifest. [1] | Unknown, pending, and provisional states remain explicit; export is not database ingestion. |
| 8. Publish in federation | Select the appropriate community/hub and publication posture. | `iho.{community}` destination, public information pages, community discussion endpoints. | Publication intent or release record scoped to the event revision. | Publication state never implies source-rights clearance or semantic approval. |
| 9. Invite and learn | Decide whether an SMS invitation is suitable and lawful for the learner relationship. | SMS template, event URL, schedule, opt-in/consent process, delivery-provider record. | Distribution-intent record excluding recipient data from the public event manifest. | Invitation intent is not dispatch, delivery, payment, or learning evidence. [1] |

## 5. Human, AI, and utility roles

The workflow works because it distinguishes the things a person must decide from the things a model or utility can prepare quickly.

| Role | Primary responsibility | Must not be treated as |
|---|---|---|
| **Curator / source custodian** | Establishes bounded cohorts, protects parent sources, corrects practical labels, and preserves source context. | A substitute for kaitiaki language or cultural authority. |
| **Kaitiaki** | Confirms, corrects, holds, or declines meaningful relationships in the appropriate community context. | A rubber stamp for AI proposals. |
| **OpenCLIP** | Provides rapid visual retrieval against a controlled vocabulary, with scores and alternatives. | A source-rights decision-maker, final category authority, or word-sense resolver. |
| **Eagle AI** | Tests visual grounding within an allowed sense set and drafts multi-register teaching language. | A curriculum authority, translator, or final reviewer. |
| **TTS / voice pathway** | Provisions a technical sound candidate from approved text under a declared voice route. | A community-authoritative speaker or proof of pronunciation quality. |
| **Python utilities** | Apply deterministic transforms, hash files, build manifests, assemble media, and produce repeatable reports. | A semantic authority or a release decision. |
| **ī-puāwai** | Holds durable identity, source, asset, sense, language, voice, review, and practice-event relationships. | A dumping ground for all unreviewed archive data. |
| **Federated iho community** | Provides the community-specific publication and learning context. | A statement that every community has accepted the same event. |
| **SMS enabler** | Offers a targeted, consent-aware invitation link between enabler and learner. | Proof that a learner received, opened, watched, learned from, or paid for an event. |

## 6. The visual pathway: from repository to truthful teaching candidate

The successful Adobe and OpenMoji work establishes the visual hand-off that the event workflow requires. The parent source remains stable; the derivative becomes discoverable and production-ready in controlled steps. [2]

```text
parent .ai / original source
        ↓
derivative working set
        ↓
OpenCLIP top-five retrieval evidence
        ↓
editable rename-and-queue manifest
        ↓
readable production label + category folder
        ↓
Eagle allowed-sense grounding
        ↓
four teaching registers + keywords + mismatch route
```

The readable file name is intentionally useful but modest. For example:

```text
trumpet_music_sound_AS_138048305.png
```

The word improves human search. The queue category prepares an Eagle cohort. The source UUID retains a production connection. None of those strings independently prove a final word sense, rights state, community authority, or curriculum decision.

The `trombone`/trumpet mismatch provides the critical proof behaviour. A filename cue said `trombone`; Eagle assessed the visual as a trumpet and returned `MISMATCH` with no fabricated learner statements. The correct response is to amend the production label and sense catalogue, retain the prior evidence, and rerun only the corrected asset. [2]

## 7. The word–sound layer

Once a visual relationship is selected, two compact sound assets complete the essential media triangle.

| Asset | Learner role | Minimum record |
|---|---|---|
| **Word sound** | Supports phoneme-first recognition, recall, pronunciation practice, and concept anchoring. | Exact text, language/script, voice route, file hash, permission/review state. |
| **Phrase sound** | Places the word in a teachable statement, question, instruction, or call-and-response event. | Exact phrase, declared register, language/script, voice route, file hash, listening-review state. |

The voice route should be selected by suitability and evidence rather than loyalty to one tool.

| Voice route | Appropriate use | Required boundary |
|---|---|---|
| Community or approved human recording | Preferred route where a community voice, dialect, relationship, or pronunciation standard is required. | Obtain and record appropriate permission, reviewer, scope, and replacement conditions. |
| Locally cloned or permitted project voice | A useful route where the voice relationship is explicitly authorised and technically maintained. | Retain consent/permission evidence and the exact source text. |
| TTSAutomate or similar desktop TTS | Rapid placeholders for languages supported by the local tool. | Label as placeholder where it is not the final approved voice. |
| Premium cloud TTS | Higher-quality temporary or production option where terms and voice fit are approved. | Record provider/model/voice, terms, exact text, and output hash. |
| MMS-TTS | Local model route for a supported language checkpoint. | Model availability is not community authority; retain checkpoint, text, language/script, and review state. [3] |

If there is no appropriate model or approved voice route, the event can retain a `voice_state: pending` rather than inventing sound. This is an operationally useful state: the visual, word, phrase, and learning intention remain available for a future community recording or voice decision.

## 8. Python as the repeatability layer

Python is acknowledged here not as a substitute for cultural, semantic, or educational judgement, but as the layer that makes a reviewed decision reproducible.

The current and planned utility family can perform bounded work such as:

```text
sanitise vocabulary
index images against prompts
create and validate manifests
hash parent and derivative bytes
move approved derivatives into controlled queues
run/resume Eagle batches
prepare voice manifests
assemble declared media components
export read-only event provenance JSON
```

The deterministic video assembler described in the provenance memorandum supplies the relevant event pattern: ordered source components, declared timing, human-reviewed overrides where present, and one-minute rendering based on a resolved component list. [1] Python can make the render repeatable; it cannot determine whether the selected visual, phrase, voice, or community publication decision is appropriate.

A production script should therefore be versioned and recorded in the event’s export context. A helpful rule is:

> **A script may transform approved inputs. It may not silently create approval.**

## 9. Video assembly and event revision

The objective is not a generic MP4. It is an assembled learning event whose media and intent can later be described at event level.

A simple one-minute event might contain a visual, text, word sound, phrase sound, learner pause, and a brief response or invitation. A more complex event can use the current deterministic twelve five-second component profile or another reviewed component arrangement. The key requirement is that the event render resolves an explicit ordered list, not merely a filename or an assumed source ID. [1]

```text
approved event script
        ↓
resolved component playlist
        ↓
visual / text / word sound / phrase sound / timing assets
        ↓
Python render specification
        ↓
MP4 and verified output hash where locally calculated
        ↓
learning-event provenance JSON snapshot
```

When an event component, phrase, voice, or publication setting changes, create a successor revision rather than silently replacing the existing event evidence. The `event_ref` can remain stable while `event_revision`, media references, manifests, and payload hashes change. [1]

### 9.1 Nano-learning events within a one-minute learning event

For the current deterministic assembler profile, a one-minute learning event is composed as a resolved sequence of **twelve five-second nano-learning events**. Each nano-learning event is a deliberately small, timed component: it may introduce a visual, present a word, play a word sound, offer a phrase, create a learner pause, or provide a response cue. Together, the twelve components create a one-minute learning event with an inspectable order and declared timing. [1]

```text
12 × 5-second nano-learning events
        ↓
1 deterministic one-minute learning event
        ↓
one event script, event revision, and provenance snapshot
```

| Nano-learning component | Typical five-second role | What remains reviewable |
|---|---|---|
| Visual orientation | Presents the selected image or visual treatment. | Source/derivative relationship and visual-sense suitability. |
| Word encounter | Displays or speaks the core word. | Word form, language/script, pronunciation and phoneme relation. |
| Phrase encounter | Presents an age-appropriate teaching statement or question. | Register, language, translation, voice, and pedagogical wording. |
| Learner pause | Creates space for recall, imitation, gesture, or response. | Intended interaction and accessibility decision. |
| Response or connection | Offers a related cue, prompt, repetition, or next-step link. | Learning relation, review status, and event position. |

The twelve-by-five-second profile is a **current deterministic assembly convention**, not a universal duration rule for every future course, platform, or community. A different reviewed event profile may use a different number of components or durations. What remains invariant is that the event script must resolve an ordered component list before rendering, and that the provenance manifest must describe the actual resolved composition rather than infer it from a filename or schedule row. [1]

Course duration is calculated separately from the number of emitted one-minute events. The optional twenty-event provenance proof set is **twenty minutes**, not a fixed cohort duration. A normal thirty-six-hour course profile contains **2,160 one-minute events**. Different reviewed events may use different resolved component counts or durations, provided their manifest states the actual composition. [1]

## 10. Federated publication through `iho.{community}`

The federation does not mean a centrally controlled feed copied without context. It gives each community a recognisable publication and learning destination, while allowing the same underlying learning-event script to be adapted with different language forms, visual decisions, voice routes, schedules, and review records.

```text
shared operating pattern
        ↓
community-specific event revision
        ↓
iho.{community} publication context
        ↓
community-specific information, discussion, and learner invitation
```

A platform destination must therefore be recorded as a **publication or distribution context**. It does not convert a pending semantic review into approval, nor does it convert a source reference into a rights clearance. The provenance JSON’s independent `publication_state`, `provenance_completeness`, Task A, Task B, and semantic-review fields are designed to keep those claims separate. [1]

Public information pages can carry stable event context, notes, references, and links. Community discussion can sit in a community-facing discussion space where non-linear questions, corrections, and later ITIL-style change, incident, or release relationships can be managed. Publication and discussion are related but not identical responsibilities.

## 11. SMS as the pinpointed invitation layer

SMS is not the learning event itself. It is a narrow linking layer between an enabler and a learner relationship that has the appropriate consent and policy context.

```text
approved event URL
        +
reviewed invitation wording
        +
declared local schedule/window
        +
consent-aware recipient relationship
        ↓
SMS invitation
        ↓
learner chooses whether to follow the link
```

The event-provenance JSON records `distribution_intent`: channel, approved local schedule or window with IANA timezone, language, message/template reference or canonical content hash, public event link, and explicit recipient-data exclusion. It must not contain phone numbers, delivery-provider credentials, payment credentials, or a claim that an invitation was dispatched, delivered, opened, or acted upon. Those facts, where policy permits their retention, belong only in an appropriately controlled delivery system. [1]

A separate `contribution_context` may identify an approved koha or other contribution offer, including a CTA/terms pointer and, where approved, display amount/currency. It is not a payment, receipt, licence, source-rights settlement, allocation, or evidence of learning. Any payment/receipt record remains separate and access-controlled. [1]

## 12. Evidence and decision gates

The workflow should use a small, repeated state vocabulary: `known`, `provisional`, `pending`, and `unknown`. These words describe the evidence available for a specific claim; they do not grade the worth of a visual, language, community, or learner. [1]

| Gate | Required question | Continue when | Hold or correct when |
|---|---|---|---|
| Source gate | Do we know enough about the source and parent/derivative relationship for this local purpose? | Source pointer and operational boundary are recorded. | Rights, provenance, duplicate, or source relationship is unclear. |
| Discovery gate | Does the derivative have a useful candidate label or a recorded review route? | A visible production candidate exists. | Candidate is misleading or unusable; preserve top alternatives and defer. |
| Grounding gate | Does the visual match an allowed sense? | Eagle returns a clear candidate or a human corrects the relation. | Eagle returns `MISMATCH`, `UNCLEAR`, or a conflicting visual result. |
| Language gate | Is the word/phrase appropriate for the named language, script, register, and intended learner event? | Relevant reviewer or authorised process has supplied the required decision. | Translation, dialect, phoneme, or cultural relation remains pending. |
| Voice gate | Is the voice source suitable for the declared scope? | Text, voice route, output hash, and listening review are recorded. | Sound is technically available but not reviewed or permitted. |
| Assembly gate | Are all required components resolvable, ordered, and versioned? | Render specification and component list are complete. | Any required source ID, component, or required boundary is unresolved. |
| Publication gate | Is the event authorised for this community destination and stated availability? | A scoped publication decision or transparent permitted provisional state exists. | Publication would imply a stronger semantic/source claim than evidence supports. |
| Invitation gate | Is SMS appropriate, consent-aware, and correctly scoped? | Message template, event link, schedule, and recipient-data boundary are recorded. | Consent, target relationship, or delivery policy is unavailable. |

## 13. A staged adoption pathway

This workflow can be established without waiting for a perfect final stack.

### Stage A — Bounded local proof

Use one visual category cohort, such as `music_sound`, to complete the full path from source-preserving discovery through Eagle captions and a single selected word/phrase sound pair. The immediate goal is not to categorise all approximately 11,000 Adobe source illustrations. It is to demonstrate that a previously unnamed, difficult-to-retrieve vector repository can yield small, coherent, source-linked visual cohorts for real learning events. Create one or two event scripts. Do not imply public release or semantic completeness merely because the render works.

### Stage B — Twenty-event reviewed proof

Apply the approved learning-event provenance JSON Change Design Contract to a limited twenty-event proof set. Use a read-only exporter, deterministic validation, payload hashes, and explicit statuses. Retain the boundary between Task A evidence, later Task B local-sense work, semantic review, and publication state. [1]

### Stage C — Federated pilot

With the relevant community agreements and technical delivery safeguards in place, create a limited `iho.{community}` publication context and a consent-aware invitation path. Begin with transparent states, small cohorts, and reviewable correction loops. The system should demonstrate what is possible without claiming that every relationship or language pathway has been completed.

## 14. Decision request

This paper recommends that the ī-puāwai Living Book recognise the workflow as a **candidate operating pattern** alongside the event-provenance JSON design, subject to the following constraints:

1. The human reviewer and kaitiaki role remains explicit at every semantic, language, voice, source, and community boundary.
2. OpenCLIP, Eagle, TTS tools, and Python utilities are documented as bounded support systems, not decision-making authorities.
3. The event-provenance JSON remains a read-only, status-bearing projection; it does not replace the relational database or create approval by export.
4. Parent sources remain protected; derivatives move only through hash-backed, dry-run-first manifests.
5. SMS remains a scoped invitation mechanism with recipient data excluded from public event manifests.
6. Each federation member retains the ability to determine its own event revision, language, voice, review, publication, and invitation posture.

## Conclusion

A federation of learning events becomes plausible when the system stops treating media, language, voice, scheduling, and delivery as unrelated placeholders. The event script brings them into one deliberate composition. Human curation protects source and purpose. OpenCLIP makes visual abundance findable. Eagle makes selected images speak in structured teaching registers while preserving the right to reject a mismatch. Voice routes make word and phrase sound provisionable without pretending that every technical voice is community-authoritative. Python makes the assembly repeatable. The provenance JSON makes the resulting event describable with honest boundaries. `iho.{community}` gives the event a community context, while SMS offers a pinpointed invitation to the learner relationship.

The achievement is not a fully automated teaching system, nor a claim that every stored visual has become a confirmed curriculum asset. It is a **repeatable, reviewable pathway** that transforms a large visual repository from latent local potential into a curatable supply of source-linked concept visuals. A community can then turn a carefully chosen visual into a multilingual, multichannel, multischedule learning event without losing track of what is known, provisional, pending, or unknown.

## 15. Glossary of terms

| Term | Working meaning in this paper |
|---|---|
| **AI++ co-design** | A working relationship in which people and AI systems contribute distinct forms of research, drafting, testing, and iteration; it does not transfer community, cultural, source-rights, or release authority to an AI model. |
| **Category queue** | A broad, provisional production folder such as `music_sound` or `animals_creatures`. It helps select a coherent cohort for work; it is not a final word sense. |
| **Component playlist** | The resolved ordered list of media components used to assemble an event. It must be recorded rather than inferred from a filename. |
| **Contribution context** | A bounded public description of an approved koha or other contribution offer, such as a CTA/terms pointer and, where approved, display amount/currency. It is not payment, receipt, allocation, licence, or rights settlement evidence. |
| **Distribution intent** | A bounded declaration of intended channel, local schedule/window with IANA timezone, language, message/template reference or canonical content hash, public event link, and recipient-data exclusion. It is not dispatch, delivery, consent, or learning evidence. |
| **Derivative** | A production asset derived from a parent source, such as a PNG, SVG, thumbnail, card, audio file, or video clip. It can change while retaining its parent relationship. |
| **Eagle** | The locally operated vision-language model used here to test visual grounding against allowed senses and to draft multi-register teaching language. |
| **Event revision** | A successor version of a stable learning event when its components, voice, text, or publication settings change. A revision creates new evidence rather than silently replacing the prior event state. |
| **Federated `iho.{community}` publication** | A community-specific context for presenting an event, its information, and its learning relationship. It does not imply that every community has accepted the same event revision. |
| **Kaitiaki** | The appropriate people or roles who confirm, correct, hold, or decline culturally and educationally meaningful relationships. |
| **Known / provisional / pending / unknown** | Evidence states. They describe what is supported at a given point in time, not the worth of an asset, language, community, or learner. |
| **Learning-event provenance JSON** | A versioned, immutable, hashable projection describing one assembled event at one declared export time, with explicit evidence and status boundaries. |
| **Learning-event script** | The reviewed design object that identifies the visual, word, phrase, language form, voice route, ordered components, timing, and delivery intent for a teachable event. |
| **Nano-learning event** | A small timed component of a larger event. Under the current assembler profile, twelve five-second nano-learning events form one deterministic one-minute learning event. |
| **OpenCLIP** | The local image–text retrieval model used to make a large visual repository findable through ranked readable candidate labels. It proposes candidates; it does not determine final meaning or rights. |
| **Parent source** | The durable original source object, such as an Adobe Illustrator `.ai` file, from which derivatives may be generated. It is protected from production renaming and queue movement. |
| **Phrase sound** | An audio rendering or recording of a reviewed learning phrase, question, instruction, or statement. |
| **Production label** | A readable operational filename element, such as `trumpet_music_sound`, used for search and queueing. It is not a database identity or final word-sense claim. |
| **TTS / voice route** | The declared technical or human route used to produce word and phrase audio, including local/community recording, TTSAutomate, premium TTS, MMS-TTS, or another approved source. |
| **Word sound** | An audio rendering or recording of the selected core word, used for phoneme-first recognition, repetition, and recall. |
| **Word sense** | A durable, reviewed relationship connecting a word form to a specific meaning, language, visual treatment, and learning context. It belongs in ī-puāwai, not solely in a filename. |
| **SMS invitation** | A scoped planned message that may link an enabler and learner relationship to an event URL only where separate recipient, consent, and delivery controls are appropriate. Event provenance records `distribution_intent`, not recipient phone numbers or a claim of dispatch, delivery, or learning. |

## References

[1]: [Ī-puāwai Learning-Event Provenance JSON — Design Memorandum](learning-event-provenance-json-design-memorandum.md), public discussion-and-design memorandum.

[2]: *ī-puāwai Visual Discovery and Readable-Prefix Utility*, internal R+D paper and bounded local proof. It is cited as non-public background until an approved public version is committed.

[3]: *Local MMS-TTS Provisioning for the ī-puāwai Word–Sound Pathway*, internal R+D paper. It is cited as non-public background until an approved public version with its official model-coverage references is committed.

[4]: [Manifesting īuwe Living Book](https://github.com/paulransfield/manifesting_iuwe) (public architectural context; link to the relevant committed chapter when this paper is placed).

[5]: User-supplied Adobe Creative Cloud licence-history screenshot, August 2026. It is R+D operating context only, not a licence statement or evidence that any depicted file has been selected for Ī-puāwai use.
