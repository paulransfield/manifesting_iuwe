# Papawai 1800 v2 curated-successor source specification

**Status:** approved curated-successor source-evidence record. **Revision date:** 2026-08-17. **Scope:** this specification publishes a separately attributable Papawai v2 source artifact and its approved decision ledger. It does **not** replace, alter, or conceal the raw Papawai v1 source artifact, its repeated-header observation, or any earlier database interpretation.

> **Community authority remains decisive.** Papawai v2 records an approved revision boundary at a point in time. It is not a closed curriculum, a final word count, or an authority over future community membership, ordering, translation, dialect, or subset decisions.

## Lineage and integrity register

| Record | Public artifact | SHA-256 | Role |
|---|---|---|---|
| Preserved parent source | [papawai_1800_words.csv](papawai_1800_words.csv) | `3E38F0518A21C1B08A3D542596522F2FDBC586C8F528ED2C7B76BB3B0A5776D1` | Raw v1 evidence. It retains the supplied final repeated `category,word` row. |
| Approved decision ledger | [papawai_1800_v2_approved_decision_ledger.csv](papawai_1800_v2_approved_decision_ledger.csv) | `E03DA9BF0778FB4A643A8BF045827903D4CF60DA7F42ED8BEDCBA65F49C7DE36` | The attributable decision record used to construct v2. |
| Curated successor source | [papawai_1800_words_v2.csv](papawai_1800_words_v2.csv) | `D6998085243C3CAA2A25C9A719BC1207A4095AA0574987B6DA47E08F98A25782` | The approved v2 source artifact. |

The v2 source preamble records the parent-source hash and approved-ledger hash. A reader can therefore verify both the source itself and the decision record from which it was generated.

## Approved decision boundary

| Decision type | Count | Effect in v2 |
|---|---:|---|
| Remove existing category-word occurrences | 357 | Removes selected specialist, novelty, image-merge, or non-foundational occurrences from this foundation set. |
| Add broad everyday transport word forms | 54 | Adds familiar personal, public/service, water, air, and connected-route transport vocabulary. |
| Recategorise existing word forms into `Transport` | 5 | Preserves the word forms while making their v2 category treatment coherent. |
| Retain existing `Boat` representation | 1 | Confirms an already suitable transport occurrence without adding a duplicate word form. |
| Valid v2 category-word occurrences | 1,330 | The successor source size after approved removals and additions. |

The inherited `1800` filename is retained for lineage and recognisability. It is not a claim that either v1 or v2 contains exactly 1,800 valid vocabulary entries.

## Curriculum reading

The removal decisions do not declare excluded words valueless. They say that, at this foundation level, many specialist bird names, food preparations, geological terms, professions, sport variants, commercial labels, technical medical items, and novelty actions are better suited to later ecological, cultural, professional, movement, media, or interest-based corpora.

The transport additions are a broad everyday proposal already approved for this v2 revision. They include personal and local movement, public and service transport, watercraft, flight, and connected routes. Their inclusion is based on foundation-list purpose rather than image availability. The source remains category-based, so a word form can occur in more than one category; category-specific source occurrences are evidence, not a reason to create duplicate canonical word identities.

## Relationship to prior Papawai evidence

The parent v1 source remains publicly available unchanged. Its public specification records a final repeated header as raw-file evidence. In the private clean database, that raw v1 snapshot is retained alongside a separate header-skip interpretation; Papawai v2 then enters as a new source snapshot, not as a rewrite of either earlier layer.

> **Raw source, interpreted source, and curated successor are different records.** Keeping them separate makes revision visible, reversible, and attributable.

## Deliberately deferred work

Health and wellbeing is recognised as an important missing foundation domain. It is not inserted into Papawai v2 merely to offset removals. It remains a separate future 50–60-word foundation gate, requiring its own rationale, review ledger, approval process, source artifact, and provenance record.

## Integrity and review use

The SHA-256 values above allow readers to verify that the published v1 parent, approved ledger, and v2 successor are the exact approved byte sequences. These artifacts support curriculum, media, translation, and community-review work; they do not turn an algorithm, a historical source, or this publication into authority over living community decisions.

The related [Dolch and Papawai v1 specification](dolch_and_papawai_source_specification.md) records the original supplied source evidence, while the [Kākano 144 specification](kakano_144_source_specification.md) records the separately community-governed first-word foundation.
