# Ī-puāwai Learning-Event Provenance JSON
## Design Memorandum — Discussion Only

**Prepared by:** **AI++ co-design: Manus and Paul Ransfield**

**AI++ co-design acknowledgement:** This memorandum was developed through Paul Ransfield’s sustained project direction, operational knowledge, source materials, review prompts, decisions, and human–AI R+D with Manus. It is not unattended AI output. This acknowledgement does not substitute for future Kaitiaki, community, source-rights, language, semantic-review, privacy, or publication authority.

**Scope:** Public discussion-and-design memorandum; no implementation, migration, database access, spreadsheet modification, packaging, or external action is proposed by this document.

## Executive recommendation

Adopt a small, versioned **event-level provenance projection** named `io.iuwe.learning-event-provenance/v0.1`. It should be an immutable, hashable description of one assembled learning event at one declared export time. It is **not** a replacement database, a semantic authority, a source-rights assertion, or a claim that every component has completed Task A or Task B. It is a truthful public or controlled-distribution manifest that can state precisely what was assembled, what source references are available, what scheduled distribution invitation belongs with the event—including an SMS message/template and a koha/contribution offer pointer where applicable—and what remains provisional, pending, or unknown. It must not contain recipient phone numbers, payment credentials, or a claim that a message was delivered, a contribution was made, or learning occurred unless separately evidenced.

The supplied event assembler establishes a practical current shape: an individual rendered minute may comprise a deterministic, ordered playlist of **twelve five-second source components**, with exact human-reviewed playlist overrides taking precedence where they exist. In an event script or public pedagogical description, a component that carries a declared small learning role may be designated a **nano-learning event**. The JSON retains the generic term `component` as the structural base, and uses the nano-learning designation only where the relevant event profile explicitly declares it. The brief’s 20-event proof set therefore describes 20 one-minute events: 12 components per event and 1,200 seconds (20 minutes) **only for that optional proof set**. It is not a fixed course-cohort duration. Course duration varies with the number of one-minute events generated; under the assembler’s normal 36-hour profile, 2,160 one-minute events comprise 129,600 seconds. This is a structural observation, not a claim that any particular proof set or 36-hour course output has been created. The supplied Task A interfaces establish equally important boundaries: hashes, preserved source records, model-process disclosure, proposal envelopes, blank human-review fields, and explicit `no_public_release` states must not become semantic approval by implication.

> **Design principle:** The relational model holds normalised facts and reviewable relationships. A JSON manifest records the assembled event and its evidence state at a particular point in time. Neither a filename, a spreadsheet label, an AI proposal, nor an available image becomes a confirmed meaning, cleared right, or curriculum decision merely by appearing in a manifest.

The immediate recommendation is to approve a later, separate **20-Event Learning-Event Provenance JSON Change Design Contract v1**. Its first implementation should be limited to a read-only exporter from the production register, JSON Schema validation, deterministic payload hashing, and a 20-event proof set. It should remain separate from active Task A packaging and should not alter the private application repository.

## 0. Evidence basis and interpretation limit

This memorandum reviews the task brief, the public Living Book, and the five supplied read-only private interfaces. At the time of the original discussion review, the current schema-v6 migration and its test were **not** supplied. Therefore, this memorandum treats the exact live table definition, populated records, and database constraints as **unknown unless directly evidenced below**. The scripts demonstrate intended and executable interfaces; they do not prove that a database has been populated, that a named event has been released, or that any particular source right or word sense has been accepted.

> **Current-public-record clarification (22 August 2026):** Since the original discussion review, the Living Book has published the verified private milestones that schema v6 provides an empty Progressive Deterministic foundation and that the first 20-card Task A source-evidence package was created, sealed, and structurally inspected. Those public facts do not populate the event model, accept image-to-meaning relationships, complete Task B, establish a release right, or replace the need for direct schema and register review before an implementation contract.

| Evidence reviewed | What it establishes for this memorandum | What it does not establish |
|---|---|---|
| Task brief | The required governance boundaries, the 20-event/240-component proof description, and the desired deliverables. | Any database row, source clearance, semantic acceptance, or completed 20-card Task A package. |
| `advanced_video_assembler_v31_curriculum.py` | A deterministic event-assembly interface with ordered source IDs, source paths, reviewed schedule/playlist inputs, 12-clip playlists, five-second normalisation, one-minute renders, and production-output labels. | Stable Ī-puāwai event identity, source rights, SHA-256 for assembled event media, semantic approval, or database ingestion. |
| `seed_word_sources.py` | Hash-identified source snapshots, immutable source metadata, canonical word identities, and row-level source memberships against supported schemas through v6. | That a component’s production label is a semantic link to a canonical word or word sense. |
| `seed_sense_domains.py` | A hash-protected 25-domain provisional register and first review records, including a protected Wairuatanga governance boundary, against supported schemas through v6. | A word-sense assignment, curriculum crosswalk, faculty assignment, or event learning statement. |
| `task_a_720_seed_reconcile.py` | A write-free Task A review-artifact process separating source inventory, preserved WordSet records, AI proposals, human review fields, and `no_public_release`. | Any confirmed local meaning, rights grant, released review result, or Task B decision. |
| `package_task_a_20_proof_inputs.py` | A deterministic, sealed 20-card input-package contract with image/WordSet/documentation hashes, `unreviewed` defaults, and explicit non-semantic/non-public boundaries. | At the time of the original direct interface review, that a real package had been run; the later public milestone confirms structural package creation, not semantic acceptance, Task B work, ingestion, or release. |
| Public Living Book | The intended architecture of stable identity, attributable provenance, reviewable relationships, and an event/delivery lifecycle. [1] [2] [3] | Completion of every designed relationship or a substitute for current private implementation evidence. |

The public architectural record is consistent with this direction: it separates canonical identity, a human-facing reference, and a production filename; it also describes a practice event as an evidence-bearing composition rather than a mere file. [1] [2] Public documentation further cautions that a source registration, asset hash, or delivery record proves only its own limited claim. [3]

## 1. Current-state model map

The statuses in this table are deliberately restricted to the categories requested in the brief. A status describes what the supplied evidence supports **for this design discussion**, not an estimate of work quality or maturity. `implemented_but_empty` means that an interface or table-family evidence is present but the required event-specific record or review evidence was not supplied. `unknown` means that the supplied materials do not justify an assertion.

| Concept | Current implementation location | Status | JSON projection role | Later relational responsibility |
|---|---|---:|---|---|
| Learning event | Assembler produces scheduled/rendered one-minute outputs; no stable event record or event table was reviewed. | `spreadsheet_only` | One `event_ref`, structural snapshot, lifecycle states, exporter provenance, and content hash. | `learning_events` as the durable, versioned event identity and event-revision root. |
| Event component | Assembler resolves one minute to an ordered playlist, normally 12 source IDs; fixed sequences and human-reviewed overrides are supported. | `implemented` | Ordered `components[]` with `component_sequence`, duration, composition origin, media/source pointers, and optional pedagogical role. | `event_components` with immutable event-revision membership and sequence constraints. |
| Nano-learning event designation | The assembler exposes ordered components and durations but does not supply a separate nano-learning entity or pedagogical-role field. | `proposed_json_only` | Optional `component_kind: nano_learning_event` and event-level `component_profile`, only when declared by the event script. | Later component-role/type vocabulary or reviewable pedagogical-design relationship; not a new identity or a substitute for component records. |
| Ordered timing | Assembler validates minute positions and forces each playlist component to a five-second target before concatenation. | `implemented` | `declared_total_duration_ms`, per-component duration, and deterministic order. | Component timing/order facts, plus optional render-specification links. |
| Image/video/audio asset | Assembler source map resolves video paths and detects audio; Task A interfaces inventory image bytes. No event-asset registry was reviewed. | `implemented_but_empty` | Media reference object, observed production label, MIME/role when known, and byte hash only when locally verified. | `content_assets`, asset families/variants, and component-media joins. |
| Byte hash | SHA-256 is implemented for Task A images, WordSet files/entries, source snapshots, ledgers, and protected database guards. The assembler does not emit a SHA-256 per assembled component/output. | `implemented_but_empty` | `sha256` only for bytes read by the exporter; otherwise `unknown`, never a fabricated hash. | Asset-byte, source-snapshot, derivative, and evidence hashes with verification history. |
| Source reference | `seed_word_sources.py` records source code, source filename, source hash, parser version, source metadata, row number, row hash, category, and order. | `implemented` | Pointer to a source-register/snapshot/reference, not copied rights text or a semantic inference. | Source, source snapshot, source membership, and source-asset relationships. |
| Source rights state | Public documentation discusses rights/review design; no supplied event-source rights record or migration definition was reviewed. | `unknown` | Separate, bounded `rights_state` with a source-register pointer and `unknown` preserved. | Rights assertions, permission terms, reciprocity notes, review/resolution cases, and time-bounded applicability. |
| Production text/label | Assembler retains schedule fields and parses an observed filename into clip ID, version, Te Reo, English, and type for production/distribution exports. | `implemented` | A status-bearing observed/derived production label; never a confirmed translation, word sense, or authority claim. | Production-label/derivative metadata, with optional reviewed links to language and sense records. |
| WordSet Task A evidence | Supplied scripts preserve exact WordSet source records/hashes and create proposal/review artifacts with human decision fields left blank; no real 20-card package was supplied. | `implemented_but_empty` | A distinct Task A evidence reference and state, never a local-sense field. Include licence/notice reference when evidence is used. | Evidence items, evidence snapshots, process runs, proposals, reviewer decisions, and link tables to assets/senses. |
| Task B local-sense proposal | The task brief defines Task B as later and separate. Public materials reserve word-sense relationships, but no Task B interface was supplied. | `deferred_schema` | Separate Task B state/reference; absence must not be conflated with Task A. | Local word-sense proposals, language-scoped senses, reviews, decisions, and supersession history. |
| Human review | A provisional sense-domain first-review pathway is supplied; Task A review artifacts include empty reviewer/decision/rationale fields. No event-level review records were supplied. | `implemented_but_empty` | Review references by scope—event, component, source, Task A, Task B—with no invented reviewer identity. | Review cases, actions, decisions, responsible Kaitiaki/roles, rationale, and validity period. |
| Learning statement | Public materials describe reusable learning statements as designed-next; no event statement register or approved statement data was supplied. | `deferred_schema` | Text may appear only as `production_text` with status; a `learning_statement_ref` is absent or `unknown` until reviewable linkage exists. | `learning_statements`, language/sense relationships, approved versions, and review links. |
| Release state | The assembler can schedule, render, group, and make filename/link exports; the production register was not supplied and no release register was reviewed. | `spreadsheet_only` | Independent `publication_state`; a release assertion belongs to event distribution, not source/meaning review. | Event release records/snapshots, channels/scopes, withdrawal/replacement relations, and release evidence. |
| Provenance completeness | Required by the brief but no existing event-level completeness classifier was supplied. | `proposed_json_only` | Independent aggregate status plus machine-readable reasons; it must never overwrite granular source/rights/review facts. | Derived/reporting view calculated from normalised source, rights, asset, evidence, and review facts. |

### Reading the map correctly

The supplied source and sense seeders demonstrate two important conventions to preserve. First, evidence is retained as a hash-identified source snapshot and source-row membership rather than collapsed into a mutable word label. Second, a provisional sense-domain review does **not** establish an event’s meaning, curriculum relationship, learning statement, or asset eligibility. This is consistent with the Living Book’s requirement to keep source occurrence, word meaning, visual reference, translation, and community review distinct. [1] [4]

The assembler also clarifies a key modelling point: one row used to schedule or render a minute is not necessarily the complete event composition. In the current deterministic path, the row can resolve to a twelve-clip playlist; a separately reviewed playlist override or a structured-hour fixed sequence may instead determine that ordered composition. The future JSON must therefore project the **resolved component list**, its composition mode, and the identified input register—not merely an output filename or one `source_id`.

## 2. Minimal versioned JSON envelope

### 2.1 Contract position and versioning

The proposed media type/contract identifier is:

```text
io.iuwe.learning-event-provenance/v0.1
```

Version `v0.1` is intentionally narrow. It freezes the event-level envelope and its truthfulness rules before any attempt to mirror every prospective relational table. Additive optional fields may be introduced in a compatible minor revision only when their status semantics are defined. A changed field meaning, required field, canonicalisation method, or state vocabulary requires a new contract version.

A manifest is a **release snapshot** of an event revision. It should not be edited in place after hashing. Correction creates a successor manifest with a new `manifest_ref`, a `supersedes_manifest_ref`, and a newly calculated payload hash. The event’s `event_ref` stays stable across event revisions; a filename, spreadsheet row, global-minute position, or SQLite integer does not.

### 2.2 Normative state vocabulary

Use the following vocabulary consistently. These are descriptions of the evidence known at export time, not grades of value or safety.

| State | Meaning | Permitted example |
|---|---|---|
| `known` | Directly observed in a named input register or verified from local bytes during this export. | Component sequence is present in the reviewed schedule input. |
| `provisional` | Attributed working information exists, but the designated authority has not confirmed it for the stated claim. | An observed production label retained from a filename or spreadsheet field. |
| `pending` | A defined process, review, or evidence step remains outstanding. | Task A candidate material awaits human review. |
| `unknown` | The exporter has no evidence sufficient to make the claim. | Source rights state was not supplied. |

`not_applicable` may be used only where a field genuinely does not apply; it must not be used to conceal missing information. Empty strings are prohibited as a substitute for `unknown`.

### 2.3 Required top-level members

| Member | Requirement and purpose |
|---|---|
| `schema` | Exact contract identifier: `io.iuwe.learning-event-provenance/v0.1`. |
| `manifest_ref` | Stable snapshot identifier. It identifies this immutable export, not the event. |
| `event_ref` | Stable event handle, independent of filenames, source IDs, spreadsheet row numbers, global-minute positions, and SQLite integer keys. A `p-` reference shape is compatible with public identity policy, subject to a later grammar decision. [2] |
| `event_revision` | Positive, monotonically increasing integer scoped to `event_ref`. |
| `export` | Generator version, export timestamp, input-register reference, input-register hash where readable, and export mode. |
| `event_structure` | Declared total duration and component count, both expressed in integer milliseconds/counts, plus an optional declared `component_profile` where a specific pedagogical assembly convention applies. |
| `components` | Ordered list with unique `component_sequence`; each member carries its duration, resolved media reference, composition origin, distinct production/source/evidence fields, and an optional `component_kind` such as `nano_learning_event`. |
| `publication_state` | State of event availability/distribution only. It does not imply rights clearance or semantic approval. |
| `distribution_intent` | One or more scheduled or on-demand distribution invitations. Each identifies channel, schedule/window, message/template content or reference, language, event link, and consent/recipient-data boundary. It is an intention, not proof of dispatch or delivery. |
| `contribution_context` | A separately scoped koha/contribution or other commercial offer reference that may accompany an invitation. It may carry public offer text, amount/currency where approved, and a public CTA/terms pointer; it is not a payment, receipt, rights grant, or learning outcome. |
| `provenance_completeness` | Event-level aggregate state plus explicit reasons and scope. It does not replace granular source/rights facts. |
| `semantic_review_state` | Event-level semantic state; it remains distinct from Task A and Task B detail. |
| `task_a_evidence` | Separate Task A state, process/manifest reference, source/notice reference when used, and review boundary. |
| `task_b_local_sense` | Separate later local-sense proposal/review state; never inferred from Task A. |
| `database_ingestion` | `not_attempted`, eligibility assessment, and later target mapping state. Export is not ingestion. |
| `integrity` | Hash method and payload hash calculated over the defined covered content without self-reference. |

A compact field-status object should be used wherever a value can otherwise be misread as authoritative. For example, `production_text.value` may be a visible label, while `production_text.knowledge_state: provisional` makes clear that it has not become an approved translation or learning statement.

### 2.3.1 Nano-learning event terminology

A **nano-learning event** is a declared small learning-role component within a larger learning event—for example, visual orientation, word encounter, phrase encounter, learner pause, response cue, or another explicitly stated pedagogical role. It is not a second event identity, a completed learning outcome, or a semantic approval. The generic `components[]` array remains the durable structural representation because an individual component may be media-only, a timing/pause interval, or a reviewed learning role depending on the event script.

For the current deterministic one-minute profile, an event may declare `component_profile: twelve_five_second_nano_learning_events` and assign `component_kind: nano_learning_event` to its twelve resolved five-second components. A different reviewed event profile may use another component count, duration, or mix of component kinds. The manifest must record the profile actually used; it must not infer nano-learning status from a filename, source ID, or five-second duration alone.

### 2.4 Clearly fictional illustrative JSON

This example is **fictional and illustrative only**. Its references, labels, hashes, source pointers, and dates do not identify real people, file paths, WordSet records, source assets, or released events. The supplied hash string is deliberately illustrative and must not be treated as a calculated digest.

```json
{
  "schema": "io.iuwe.learning-event-provenance/v0.1",
  "manifest_ref": "lem-Z8Y7X6",
  "event_ref": "p-N7K4D9",
  "event_revision": 1,
  "export": {
    "generated_at": "2030-01-02T03:04:05Z",
    "generator": {"name": "fictional-read-only-exporter", "version": "0.1.0"},
    "input_register": {
      "ref": "register-DEMO-01",
      "knowledge_state": "known",
      "sha256": "0123456789abcdef0123456789abcdef0123456789abcdef0123456789abcdef"
    },
    "export_mode": "read_only_projection"
  },
  "event_structure": {
    "declared_total_duration_ms": 60000,
    "component_count": 12,
    "component_profile": {"value": "twelve_five_second_nano_learning_events", "knowledge_state": "known"},
    "composition_mode": "deterministic_resolved_playlist",
    "composition_basis": {"value": "source-manifest rule", "knowledge_state": "known"}
  },
  "components": [
    {"component_sequence": 1, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC001", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 01", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 2, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC002", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 02", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 3, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC003", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 03", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 4, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC004", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 04", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 5, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC005", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 05", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 6, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC006", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 06", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 7, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC007", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 07", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 8, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC008", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 08", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 9, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC009", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 09", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 10, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC010", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 10", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 11, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC011", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 11", "knowledge_state": "provisional"}, "source_register_pointers": []},
    {"component_sequence": 12, "duration_ms": 5000, "component_kind": "nano_learning_event", "media": {"media_ref": "a-FIC012", "byte_sha256": {"value": "unknown", "knowledge_state": "unknown"}}, "production_text": {"value": "fictional label 12", "knowledge_state": "provisional"}, "source_register_pointers": []}
  ],
  "distribution_intent": [
    {
      "delivery_ref": "dist-FIC001",
      "channel": "sms",
      "schedule": {"local_datetime": "2030-01-02T09:00:00", "iana_timezone": "Pacific/Auckland", "state": "scheduled"},
      "message": {"content": "Fictional one-minute learning invitation: https://example.invalid/event/p-N7K4D9", "language_code": "eng", "knowledge_state": "known", "content_sha256": "0123456789abcdef0123456789abcdef0123456789abcdef0123456789abcdef"},
      "recipient_data": "excluded_from_event_manifest",
      "delivery_evidence_state": "not_attempted"
    }
  ],
  "contribution_context": {
    "state": "offer_available",
    "knowledge_state": "known",
    "offer_ref": "offer-FIC001",
    "offer_kind": "koha_contribution",
    "public_cta_url": "https://example.invalid/koha",
    "payment_or_receipt_state": "not_asserted"
  },
  "publication_state": {"value": "released", "knowledge_state": "known", "scope": "fictional-example"},
  "provenance_completeness": {"value": "partial", "knowledge_state": "known", "reasons": ["source-rights records not supplied", "component-byte hashes unavailable"]},
  "semantic_review_state": {"value": "pending", "knowledge_state": "known", "reason": "no local-sense decision recorded"},
  "task_a_evidence": {"state": "pending", "knowledge_state": "known", "evidence_refs": [], "wordset_licence_notice_ref": null, "public_release_boundary": "not_asserted"},
  "task_b_local_sense": {"state": "pending", "knowledge_state": "known", "proposal_refs": [], "review_refs": []},
  "database_ingestion": {"state": "not_attempted", "target_schema": {"value": "unknown", "knowledge_state": "unknown"}},
  "integrity": {
    "algorithm": "sha-256",
    "canonicalization": "RFC 8785 JSON Canonicalization Scheme",
    "covered_content": "all top-level members except integrity",
    "payload_sha256": "0123456789abcdef0123456789abcdef0123456789abcdef0123456789abcdef",
    "example_only_not_calculated": true
  }
}
```

### 2.5 Hashing without self-reference

The payload hash must be deterministic and independently reproducible. Define the covered payload as a deep copy of the manifest **with the entire `integrity` member removed**. Serialize that covered payload under the agreed JSON Canonicalization Scheme (RFC 8785), encode UTF-8, and calculate lowercase SHA-256. Store the resulting digest in `integrity.payload_sha256`; because `integrity` is excluded from coverage, no circular hash problem arises. [5]

The exporter must not hash a prettified output file, operating-system newline convention, or an arbitrary dictionary ordering. The generated timestamp and input-register reference are covered content; any change to them intentionally creates a different snapshot hash. A later detached signature may be added as a separate extension, but it is out of scope for `v0.1`.

## 3. Status-state matrix

No single status field can truthfully represent publication, source/provenance, Task A, Task B, and Kaitiaki semantic review. These dimensions should remain independent.

| Publication state | Provenance completeness | Task A evidence | Task B local sense | Semantic review state | Permitted? | Meaning and required treatment |
|---|---|---|---|---|---|---|
| `released` | `partial` | `pending` | `pending` | `pending` | Yes | A structurally complete event is available, while source/rights or semantic relationship work remains incomplete. Manifest must show reasons and must not present labels as confirmed meaning. |
| `unreleased` | `verified` | `pending` | `pending` | `pending` | Yes | Source/provenance facts may be sufficiently evidenced while image-to-WordSet evidence has not been started or linked. Do not infer semantic approval. |
| `released` | `partial` or `verified` | `accepted` | `pending` | `pending` | Yes | Task A evidence has been accepted for its defined scope only. It does not create a local word sense or Task B decision. |
| `blocked` | `unknown` | `unknown` or `pending` | `pending` | `pending` | Yes | Source rights or provenance is unknown. No release should be asserted for the affected scope; retain the record and the reason for the block. |
| `released` | `verified` | `accepted` | `accepted` | `accepted` | Yes | A stronger event claim, only if all referenced decisions exist and their scopes are current. This is not an automatic target for v0.1. |
| `released` | `verified` | `accepted` | `accepted` | `pending` | Yes | The evidence links may exist while broader Kaitiaki learning-use review remains pending; the manifest must say so. |
| `released` | `unknown` | any | any | any | Conditionally | Only if the approved publication policy allows a transparent release with unknown provenance. The unknown condition must be public/visible at the approved scope; it must never be silently coerced to `partial` or `verified`. |
| `released` | any | `candidate_review` | `accepted` | `accepted` | No | A Task B acceptance cannot be inferred from a Task A candidate, and this combination is internally contradictory unless a separate Task B evidence chain is cited. |
| any | any | `accepted` | `accepted` | `accepted` | No, if reviewer evidence absent | State words without attributable review references are invalid. |

The vocabulary for Task A should preserve the supplied interface where applicable: `candidate_review`, `multiple_meanings_retained`, `no_suitable_meaning`, and `needs_other_evidence`. These are evidence-process results, not release states. The `package_task_a_20_proof_inputs.py` interface additionally demonstrates `unreviewed`, `exact_wordset_entry_preserved`, `exact_wordset_entry_not_found`, and explicit `no_public_release` boundaries. A JSON event should reference such records; it should not replicate source WordSet content or flatten it into a claim of local meaning.

## 4. Spreadsheet/VS Studio bridge

The future exporter should be a one-way reader. It may calculate derived fields and record input evidence, but it must never update source rows, backfill missing semantic fields, modify the assembler schedule, render media, or call an AI service. It reads the existing production register and, where approved, the accompanying source/playlist/hour-layout manifests used by the assembler.

| Production-register or assembler input | JSON target | Transformation | Absence/ambiguity rule |
|---|---|---|---|
| Register workbook/sheet name, CSV path, revision label | `export.input_register.ref` | Record a non-secret source-register reference. | Required. Export fails if no stable source-register reference can be recorded. |
| Input file bytes | `export.input_register.sha256` | Calculate SHA-256 only from the read bytes used by the export. | If source cannot be read, exporter fails; it must not emit an unverified input hash. |
| Export run time and exporter build/version | `export.generated_at`, `export.generator` | Generated by exporter. | Required. |
| Row key or schedule key | Internal exporter lookup only; optional `source_row_locator` | Preserve as a provenance locator, not as `event_ref`. | Missing locator makes the event non-exportable until an approved key is selected. |
| Approved stable event ID, if later added | `event_ref` | Copy exactly after uniqueness validation. | If absent in initial proof, apply the separately approved durable event-ID assignment rule; never derive it from filename or row number. |
| `global_minute`, `hour_number`, `minute_in_hour`, output number | Optional production/scheduling context | Preserve as context fields with `known` status. | Never use as a permanent event identity. |
| `source_id` and resolved source-map entry | `components[].source_locator` and media pointer | Resolve each of the 12 component source IDs after playlist/sequence/override logic. | Unknown source ID is a hard export failure. |
| Playlist override manifest | `event_structure.composition_mode = reviewed_playlist_override` and input pointer | Preserve the manifest/row reference and resolved sequence. | Do not silently substitute the default deterministic playlist. |
| Structured-hour layout and sequence manifest | `composition_mode = structured_hour` plus layout/input pointers | Preserve the resolved composition and the fixed/fill basis. | Any unresolved sequence, unsafe seam, duplicate playlist, or invalid source pool is a hard export failure. |
| Source path/observed file name | `components[].media.observed_production_label` | Preserve for production traceability with `provisional` status. | Do not convert parsed Te Reo/English fragments into approved language/sense records. |
| Local source bytes, if readable in approved exporter context | `components[].media.byte_sha256` | SHA-256 each selected component byte stream. | If paths are inaccessible, set hash state to `unknown`; do not hash a path string. |
| Duration/clip count from resolved assembly | `components[].duration_ms`, `event_structure` | Use five-second normalized duration specification where assembly contract guarantees it; verify sum. | Mismatch is a hard export failure. |
| Production display text / observed label | `components[].production_text` | Copy as observed/derived text with field status. | Blank becomes `unknown`; no AI fill or semantic inference. |
| Source-register pointer / source-row reference, where supplied | `source_register_pointers[]` | Preserve pointer and state without copying a rights conclusion. | Missing pointer remains `unknown`; it cannot become an implied clearance. |
| Task A run/card/package manifest reference | `task_a_evidence.evidence_refs[]` | Reference by manifest/card ref and SHA-256, retaining Task A status and licence/notice reference where used. | Absent evidence is `pending` or `unknown`, not `accepted`. |
| Task B proposal/review reference | `task_b_local_sense` | Reference only separately approved Task B records. | No Task B input means `pending`/`unknown`; never copy Task A decision. |
| Release register/distribution location | `publication_state` | Copy only a documented release state/scope. | If no release record exists, use `unknown` or `unreleased` as appropriate; do not infer from a render/output file. |
| Scheduled delivery register, including a scheduled SMS invitation | `distribution_intent[]` | Preserve delivery reference, channel, local schedule/window, IANA timezone, event link, message text/template or approved message hash, language, and intended delivery state. | Do not export recipient phone numbers, contact identifiers, consent records, provider credentials, or a claim that the message was sent/delivered. |
| Koha/contribution call to action associated with the invitation | `contribution_context` | Preserve the offer reference, public CTA/terms pointer, public display text and, where specifically approved, amount/currency. | An offer is not a payment, receipt, licence, rights clearance, or learning outcome. Where no offer exists, use `not_applicable`; where evidence is unavailable, use `unknown`. |
| Delivery attempt/receipt record | Downstream delivery-evidence or receipt pointer only | Reference a separate immutable delivery attempt or receipt if later created under an approved privacy policy. | Do not create or imply one merely because the event manifest contains an SMS or koha offer. |

The exporter should record an `export_warnings[]` list for non-fatal unknowns—such as unavailable component bytes or missing source-rights pointers—rather than hiding them in a log. It should generate no public identifier, no new database record, no updated spreadsheet cell, and no content asset.

### 4.1 Scheduled distribution, SMS, and Koha / contribution context

The supplied `iho.whanau.tv` page visibly presents a continuous 24/7 learning stream and a public koha call to action. [6] The user has additionally confirmed that, for the scheduled one-minute event under discussion, the SMS message is part of the manifest. The appropriate design is therefore to treat the SMS as **event-level distribution content**: it is an attributable, versioned invitation associated with the particular event revision and scheduled delivery intent.

This does **not** make SMS the event itself, and it does not turn the event manifest into a CRM, payment ledger, or mass-messaging log. The exported manifest may contain the approved SMS message or a canonical template/reference plus hash, event URL, channel, language, scheduled local time and IANA timezone, message version, and an explicit consent/privacy boundary. It must exclude recipient phone numbers, recipient identifiers, consent evidence, provider response bodies, and credentials. Those facts, where needed at all, belong in access-controlled delivery/consent systems and should be referenced only by an opaque delivery record after separate governance approval.

Similarly, a koha/contribution offer can travel with the invitation as **contribution context**. This preserves the event-to-offer relationship and supports several monetisation pathways without falsely claiming that a payment occurred. Its state must remain separate from both `publication_state` and `provenance_completeness`:

| Manifest dimension | It may say | It must not say without separate evidence |
|---|---|---|
| `distribution_intent` | An SMS invitation for this event is scheduled, with specified approved content and schedule. | A recipient was contacted, received the message, opened the link, or consented. |
| `contribution_context` | A public koha/contribution offer or commercial call to action is associated with this event. | A payment was made, allocated, refunded, or settled. |
| `delivery_evidence_state` | Delivery evidence is not attempted, pending, or referenced in a separate system. | That the event was delivered successfully merely because it was scheduled. |
| Receipt reference | A separate receipt, if one exists, may be linked under an approved privacy policy. | That a receipt proves rights clearance, semantic approval, or learner understanding. |
| `publication_state` | The event is available at a stated scope. | That an SMS was sent or a contribution was completed. |

This distinction aligns with the public evidence architecture: an event’s schedule, a delivery attempt, a served/error record, and a receipt are separate evidential stages, and none proves learner understanding by itself. [3] It also keeps a one-minute event usable across multiple pathways—stream, SMS invitation, community page, or another approved channel—without assigning payment or delivery history to the underlying learning composition.

## 5. Future relational model boundary

The JSON is a snapshot/projection boundary. It should contain enough denormalised context for discovery and verification, but its stable pointers must map to normalised facts over time. The relational model remains the appropriate home for evolving evidence, many-to-many relationships, correction, review, and access-controlled details.

| Conceptual table family | Future relational responsibility | JSON responsibility |
|---|---|---|
| Identity registry | Stable UUID/public-reference identity, uniqueness, entity type, and retained aliases/supersession where approved. | Carry stable public references and optionally UUIDs only where visibility policy permits. |
| Learning events and event revisions | Event identity, revision history, intended duration, composition specification, lifecycle, and supersession. | Snapshot one event revision and state which prior manifest it supersedes. |
| Event components | Ordered component rows, duration, role, timing, composition basis, and event-revision membership. | Denormalise the resolved ordered list sufficient to reproduce/verify declared composition. |
| Content assets / asset families / variants | Asset identity, bytes, formats, parent/derivative relationships, storage locations, and checksums. | Reference a media identity and emit a byte hash only when locally verified. Never expose private path by default. |
| Component-media relationships | Which asset/variant supplies which component and in what production role. | Preserve the resolved media pointer and component role. |
| Sources, snapshots, and source memberships | Source provenance, immutable snapshot hashes, source rows, attributions, parsing/interpretation metadata, and source-to-word relationships. | Use pointers, hashes, and status; do not duplicate source content or create rights conclusions. |
| Rights, reciprocity, and resolution | Rights assertions, scope/validity, creator wishes, contacts, reciprocity commitments, questions, pauses, and retirement decisions. | Project only a suitable disclosure status and reference; `unknown` remains explicit. |
| Evidence/proposal process runs | Task A inventories, source snapshots, input/output hashes, model/process disclosure, notices, non-approval boundaries, and reviewer-ready artifacts. | Reference Task A evidence by stable ID/hash and preserve its narrow state. |
| Word senses and Task B proposals | Language-scoped sense proposals, local terminology, evidential rationale, Kaitiaki review, decision, and supersession. | Project a separate Task B state/reference, only when it exists. |
| Reviews and decisions | Kaitiaki/role, scope, decision, rationale, conditions, timestamps, dissent, expiry, and supersession. | Carry scoped review references and aggregate state; do not embed private deliberation by default. |
| Learning statements | Reusable statement identity, language/sense relationships, approved text/version, and review. | Refer to an approved statement only; otherwise preserve production text as provisional/unknown. |
| Releases and release snapshots | Publication channel/scope, dates, availability, restrictions, withdrawals, and versioned event-to-release mapping. | State publication independently and identify the snapshot/release reference if disclosable. |
| Scheduled distributions | Channel, event revision, local schedule/window, IANA timezone, intended audience scope, dispatch state, and a link to an approved message/template. | Carry an SMS or other delivery intention without recipient data or a claim of execution. |
| Message templates and versions | Approved SMS/notification content, language, content hash, link substitutions, consent basis category, and retirement/supersession. | Embed approved message content or a template reference/hash only at the decided disclosure level. |
| Contribution offers and terms | Koha/contribution or other commercial offer identity, display text, CTA/terms, amount/currency where applicable, scope, validity, and revision history. | Link the event to an offer; do not carry payment/receipt assertions. |
| Delivery evidence and receipts | Schedule, delivery attempt, served/error evidence, payment/receipt evidence, and privacy-constrained aggregates. | Out of scope for the initial event provenance object except optional opaque references and explicit `not_attempted`/`not_asserted` states. |

The supplied source seeder already exhibits the intended relational pattern: a canonical word and a source membership are not the same record, while source row hash and source snapshot hash remain independently inspectable. The same discipline is appropriate for event manifests. A component can point to an asset; an asset can point to source evidence; Task A can point to a preserved WordSet source record; Task B can later record a local sense decision. These must not be condensed into one unreviewable `meaning` or `provenance_status` cell.

## 6. Validation and later ingestion rules

### 6.1 Deterministic export validation

The exporter must validate before writing a manifest. The following are minimum deterministic rules.

| Rule | Requirement | Failure handling |
|---|---|---|
| Contract and version | `schema` must equal the supported exact contract identifier. | Hard failure. |
| Event and manifest identity | `event_ref` and `manifest_ref` must match approved grammar and be non-empty; a manifest ref must not repeat within an export set. | Hard failure. |
| Component sequence | `component_sequence` must be unique, positive, contiguous, and start at 1. | Hard failure. |
| Component count | `event_structure.component_count` must equal `components.length`. | Hard failure. |
| Duration | Every component duration is a positive integer; sum of durations equals `declared_total_duration_ms`. | Hard failure. |
| Declared component profile | Every exported event must state its actual component count, component durations, and total duration. If `component_profile` is `twelve_five_second_nano_learning_events`, it must resolve to exactly 12 components of 5,000 ms each and a total of 60,000 ms. Any other reviewed profile must state its own actual structure; course/cohort duration is calculated separately from the number of emitted events and is not constrained to 20 events. | Hard failure for a profile/composition mismatch. |
| Resolved composition | Every component source ID/media locator must be present in the resolved assembler source map; reviewed override/structured-hour origin must be captured when used. | Hard failure. |
| Filename boundary | Production filenames/parsed labels may be retained only as production metadata and must carry a field status. They cannot populate a confirmed meaning, translation, source-rights state, or event identity. | Hard failure for invalid semantic promotion; warning/unknown for missing label. |
| Status vocabulary | All status-bearing fields must use the approved vocabulary. `unknown` requires no fabricated value; `provisional` requires an attributed basis; `pending` requires a named outstanding process if one exists. | Hard failure for invalid state or status/value contradiction. |
| Scheduled distribution | Every scheduled SMS/notification must identify channel, approved local time/window, IANA timezone, event revision, content/template reference or canonical message hash, and an intent state. | Hard failure for an incomplete scheduling object. |
| SMS privacy and consent boundary | Event manifests must exclude recipient phone numbers, recipient identities, consent records, provider credentials, and raw provider responses. | Hard failure if restricted recipient/provider data appears in an event manifest. |
| Contribution boundary | A contribution/koha object may describe an offer and public CTA/terms only. `payment_or_receipt_state` may not be positive without a distinct evidence/receipt reference. | Hard failure for an unsupported payment, allocation, licence, rights-clearance, or learning-outcome claim. |
| Source and rights boundaries | Every rights claim must cite a source-register pointer or review reference. Absence must be `unknown`, not an empty/positive assertion. | Hard failure for uncited claim; non-fatal unknown only if policy permits export. |
| SHA-256 | If the exporter reads local bytes, it must calculate and validate lowercase 64-hex SHA-256. If it cannot read bytes, record `unknown`; never hash a file name, URL, or path. | Hard failure for malformed/mismatched claimed hash. |
| Task A boundary | Task A reference must preserve state, evidence hash/reference, and WordSet licence/notice reference where WordSet evidence is referenced. `candidate_review`, `unreviewed`, or `needs_other_evidence` cannot yield Task B acceptance. | Hard failure for promotion/confusion. |
| Task B boundary | A Task B acceptance must include a distinct Task B proposal/review reference and must not be derived solely from Task A fields. | Hard failure. |
| Governance boundary | `Wairuatanga` remains an equal faculty space; `Hauora` is represented beneath Kaitiakitanga rather than as a separate faculty space when those future references are introduced. The initial JSON does not create crosswalks. | Hard failure for a contradictory asserted crosswalk; otherwise out of scope. |
| Restricted material | No Biemiller content, identifier, or implied word-level authority may be exported. | Hard failure. |
| Payload hash | Canonicalise the manifest excluding `integrity`, calculate SHA-256, then require exact match to `integrity.payload_sha256`. | Hard failure. |

### 6.2 Conditions for later database ingestion

A valid JSON file is **not** automatically eligible for database ingestion. Ingestion should be a separately approved, idempotent operation after the relational mapping is settled. At minimum, it requires the following conditions.

| Ingestion condition | Reason |
|---|---|
| Supported JSON contract version and verified payload hash | Prevents importing an unknown or altered projection. |
| Stable `event_ref` is unique or is an explicitly recognised revision/successor | Prevents duplicate identity and accidental overwrite. |
| Every component has a valid sequence/timing record and a resolvable allowed media/source locator | Protects composition integrity. |
| Referenced relational entities either resolve exactly or are queued as unresolved references without invented substitute records | Prevents a JSON projection from becoming an uncontrolled seed mechanism. |
| Rights, Task A, Task B, and review states are stored as distinct imported facts/links—not collapsed into a single event status | Preserves evidence and governance boundaries. |
| Any local byte hash has been verified against the actual bytes under approved access conditions | Prevents path/string hashes and stale evidence. |
| Ingestion mode is append-only for new event revisions and retains the original payload plus hash | Preserves auditability and permits correction through successors. |
| Ingestion does not use JSON-derived labels to create word senses, translations, curriculum membership, or Kaitiaki decisions | Keeps Task A, Task B, semantic review, and event assembly separate. |
| A designated reviewer approves the import mapping and exceptions policy | A technical parser is not a governance authority. |

The first proof implementation should stop at **validation and emitted JSON**. It should not include database ingestion. That separation makes the first contract small enough to test without turning a production register into a competing database or a new uncontrolled migration path.

## 7. Open decisions for Paul Ransfield / future Kaitiaki

The following decisions cannot be assumed by technical design. They should be recorded as explicit decisions in the later Change Design Contract, with the decision authority, rationale, scope, and review/revision route.

| Open decision | Why it requires governance rather than technical inference |
|---|---|
| Durable event-reference grammar and allocation authority | The public identity policy supports stable prefixed references, but the exact event prefix, reservation process, collision control, and whether a current production event receives one need an approved policy. |
| Manifest visibility and access scope | Decide whether manifests are public, community-restricted, production-restricted, or released in redacted forms. Public discoverability must not disclose local drive paths, private review details, restricted source locations, or personal information. |
| Minimum publication threshold | Decide whether a structurally complete event with `provenance_completeness: partial` and `semantic_review_state: pending` may be released, in which channel, and with what visible qualification. |
| Event-level versus component-level disclosure | Decide whether source, rights, and Task A detail is publicly disclosed per component, summarized at event level, or made available only to Kaitiaki/reviewers. Granularity must balance truthfulness, privacy, safety, and workload. |
| Source-rights status taxonomy | Define permitted values, evidence required for each, review ownership, and whether rights notices are public, controlled, or pointer-only. A technical exporter cannot decide clearance. |
| SMS message and consent policy | Decide whether the full message is public or template-referenced, who approves it, how its revisions are retained, which consent/opt-out category applies, and which recipient/delivery facts are prohibited from the event manifest. |
| Contribution / koha offer policy | Decide which offer types, public terms, CTA destinations, price/currency details, and event-to-offer relationships are permitted; define the receipt, refund, allocation, and privacy boundary as distinct downstream records. |
| Task A reference policy | Decide which Task A states are visible in an event manifest, whether a WordSet licence/notice reference is always public, and whether detailed source-record pointers are restricted. |
| Task B review threshold | Define who may propose, confirm, defer, revise, or decline a local word-sense relationship; determine how different Kaitiaki roles and dissent are represented. |
| Learning-use threshold | Define what review is needed before a production label may become a learning statement, selected sense, translation, or curriculum relationship. |
| Retention, correction, and deletion policy | Decide how long manifests, hashes, source pointers, withdrawn releases, and review decisions are retained; define correction/supersession and access/removal procedures. |
| Event revision semantics | Decide whether a changed component playlist, media byte hash, production text, or publication scope creates a new event revision, a new release snapshot, or both. |
| 20-event proof-set composition policy | Decide which register constitutes the approved 20 events, how their stable event references are allocated, and what non-semantic information may be exported from the current production process. |
| Relationship to later schedule/delivery evidence | Decide whether scheduling, delivery, learner evidence, and receipts are deliberately excluded from this event provenance contract or linked as optional downstream references. The public architecture treats these as distinct stages. [3] |

## Recommended next steps

The following sequence preserves the requested separation from active Task A work and avoids making an implementation decision by implication.

1. **Approve the design boundary.** Confirm that the JSON is an event-level, immutable projection and not a replacement source of truth, semantic catalogue, or rights register. Confirm the separate status dimensions and the `known`/`provisional`/`pending`/`unknown` vocabulary.

2. **Review the missing current relational evidence read-only.** Before any implementation contract is signed, review `migrations/006_progressive_deterministic_learning_foundation.py` and `tests/test_progressive_deterministic_learning_foundation_schema.py`. Use them to replace the table-family assumptions in this memorandum with a verified schema-v6 mapping. Treat legacy `schema.py` as historical orientation only.

3. **Provide the actual source-register interface.** Supply the production CSV header and a sanitised one- or two-event sample, or an approved complete register, plus the source/playlist/hour-layout manifests that determine component order. This establishes the exporter field map without exposing source media or conducting semantic inspection.

4. **Make the open governance decisions.** In particular, confirm event-reference grammar, publication visibility, minimum release threshold, source/rights disclosure scope, Task A reference visibility, Task B thresholds, and manifest retention/supersession policy.

5. **Write and approve the separate _20-Event Learning-Event Provenance JSON Change Design Contract v1_.** It should freeze the JSON Schema, canonicalisation profile, status vocabulary, exporter input map, redaction policy, error policy, and proof acceptance criteria. It should explicitly state that no migration, database ingestion, Task A packaging, Task B proposal, public Living Book change, or application-repository push is included.

6. **Only after separate approval, implement a minimal proof.** Limit it to a read-only spreadsheet/VS Studio exporter, JSON Schema validation, deterministic payload hashing, and the 20-event proof set. Keep the implementation in its own approved workspace and evidence/approval path, separate from Task A packaging.

> **Concise conclusion:** Proceed with a later, separately approved **20-Event Learning-Event Provenance JSON Change Design Contract v1**. The contract should implement only read-only export, validation, deterministic hashing, and a 20-event proof set. It must reference Task A evidence without promoting it, leave Task B separate, preserve explicit unknowns, and remain independent of the active Task A worktree until its own evidence and approval gates are met.

## References

[1]: https://github.com/paulransfield/manifesting_iuwe/blob/main/08-our-i-puawai/ipuawai-rebaseline-language-provenance-and-road-ahead.md "Ī-puāwai rebaseline: language, provenance, and the road ahead"
[2]: https://github.com/paulransfield/manifesting_iuwe/blob/main/08-our-i-puawai/01-identity-and-provenance/ipuawai-identity-policy.md "Ī-puāwai identity policy"
[3]: https://github.com/paulransfield/manifesting_iuwe/blob/main/06-our-proofs/README.md "Our Proofs"
[4]: https://github.com/paulransfield/manifesting_iuwe/blob/main/08-our-i-puawai/06-practice-events-and-delivery/README.md "Practice events and delivery"
[5]: https://www.rfc-editor.org/rfc/rfc8785 "RFC 8785: JSON Canonicalization Scheme"
[6]: https://iho.whanau.tv/ "iho.whanau.tv scheduled learning-stream page"

### Reviewed private interface set

The following supplied attachments were reviewed read-only for this discussion: `advanced_video_assembler_v31_curriculum.py`, `seed_sense_domains.py`, `seed_word_sources.py`, `task_a_720_seed_reconcile.py`, and `package_task_a_20_proof_inputs.py`. No code was executed, modified, or used to access protected databases, source media, registers, or external services.
