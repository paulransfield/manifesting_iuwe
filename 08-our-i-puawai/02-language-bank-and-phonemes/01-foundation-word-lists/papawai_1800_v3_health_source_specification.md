# Papawai 1800 v3 health-and-wellbeing successor source specification

**Status:** approved curated-successor source-evidence record. **Revision date:** 2026-08-18. **Scope:** this specification publishes a separately attributable Papawai v3 source and its approved Health and Wellbeing decision ledger. It does **not** replace, alter, or conceal the raw Papawai v1 artifact, the v1 repeated-header observation, the separate header-skip interpretation, or the approved Papawai v2 successor.

> **Community authority remains decisive.** Papawai v3 records an approved revision boundary at a point in time. It is not a closed curriculum or an authority over future membership, ordering, translation, dialect, subset, phrase, or media decisions.

## Lineage and integrity register

| Record | Public artifact | SHA-256 | Role |
|---|---|---|---|
| Preserved raw source | [papawai_1800_words.csv](papawai_1800_words.csv) | `3E38F0518A21C1B08A3D542596522F2FDBC586C8F528ED2C7B76BB3B0A5776D1` | Raw v1 evidence, including its supplied final repeated `category,word` row. |
| Approved v2 parent | [papawai_1800_words_v2.csv](papawai_1800_words_v2.csv) | `D6998085243C3CAA2A25C9A719BC1207A4095AA0574987B6DA47E08F98A25782` | The approved 1,330-row curated predecessor. |
| Approved v3 health ledger | [papawai_1800_v3_health_approved_decision_ledger.csv](papawai_1800_v3_health_approved_decision_ledger.csv) | `8996096C3E5C6D90F6CE5705C5A3E5FE19C27A19D7B5DA36FBCFB247FC41214E` | The attributable 75-entry Health and Wellbeing addition record. |
| Approved v3 successor | [papawai_1800_words_v3.csv](papawai_1800_words_v3.csv) | `C82058EAA567C4A71C2EDFCC6436C73ECB6CEA638105D64D83AFB4EDE47C4E1D` | The approved 1,405-row health-and-wellbeing successor. |

The v3 source preamble also records the v2 parent hash, the approved health-proposal hash (`E562E042…27144`), and the approved health sense-mapping hash (`C550677D…FB705`). Those review inputs guided the decision boundary; the published v3 ledger is the authoritative, row-level public record of the approved additions.

## Approved decision boundary

| Decision type | Count | Effect in v3 |
|---|---:|---|
| Retained v2 category-word occurrences | 1,330 | Preserves the entire approved v2 source in the same order. |
| Add approved `Health and Wellbeing` occurrences | 75 | Adds everyday body awareness, feelings, wellbeing, rest, hygiene, food/water, care, medicine, unwellness, symptoms, urgency, and access vocabulary. |
| Valid v3 category-word occurrences | 1,405 | The successor source size after the approved health addition. |

The health additions deliberately include plain-language terms such as `unwell`, `headache`, `dizzy`, `bleeding`, `rash`, `vomit`, and `ambulance`. They support general everyday communication and later phrase construction; they do not form a diagnostic curriculum, triage service, or substitute for professional care.

Some health word forms already occur in Kākano 144 or an earlier Papawai source. Those overlaps remain visible as category-specific source memberships. The clean database maintains one canonical word identity per normalised form while preserving the distinct reasons each source includes it.

## Sense-domain relationship

The v3 ledger records a primary and secondary sense-domain role for every health addition. These roles make links to the existing Eagle image-categorisation context visible without allowing pictionability to decide curriculum membership. The health additions use domains including `self_and_body`, `feelings_and_senses`, `safety_and_wellbeing`, `food_and_drink`, `time_and_routines`, `movement_and_position`, and `community_and_services`.

The word source remains the common Papawai floor. Later phrase construction, image categorisation, and faculty/domain-specific learning remain separate layers.

## Relationship to prior Papawai evidence

Papawai v1 remains raw-file evidence. Its database history retains the supplied repeated-header row and separately records a reviewed header-skip interpretation. Papawai v2 remains an approved transport-focused curated successor. Papawai v3 is a new source snapshot; it does not rewrite v1, v2, or the separate interpretation.

> **Raw source, interpreted source, and successive curated sources are different records.** Keeping them separate makes revision visible, reversible, and attributable.

## Deliberately deferred work

The following work is intentionally outside this publication: sentence patterns and care-encounter language in the phrase module; general interaction-word coverage; numeracy, digital-literacy, and wairuatanga sources; direct Eagle sense-table changes; clinical diagnosis or advice; and media selection. Each requires a separate review boundary and community-governed approval path.

## Integrity and review use

The SHA-256 values allow readers to verify that the published v1 source, v2 parent, v3 health ledger, and v3 successor are the exact approved byte sequences. These artifacts support curriculum, media, translation, and community-review work; they do not turn an algorithm, a historical source, or this publication into authority over living community decisions.
