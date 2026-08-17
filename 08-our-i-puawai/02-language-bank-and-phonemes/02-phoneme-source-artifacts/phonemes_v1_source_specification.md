# Ī-puāwai phonemes v1: source specification

**Status:** public source-evidence record. **Publication date:** 2026-08-17. **Scope:** this record publishes a byte-preserved JSON seed artifact and documents what the artifact says. It does **not** execute the legacy seed script, amend the source records, declare a final curriculum, or create audio, model, or media attribution.

> **Community review remains decisive.** The artifact is a transparent starting point for phoneme, language, learner-support, and community-link work. It is not an authority over future language review, dialect representation, pronunciation guidance, or learning sequence.

## Artifact register

| Field | Recorded value |
|---|---|
| Public artifact | [phonemes_v1.json](phonemes_v1.json) |
| Artifact name | `ipuawai_phonemes_v1` |
| Artifact version | `1` |
| Artifact SHA-256 | `222989A84C3E87C4CAC8E77A3707F87E8884BBD683643B76F1D27C540C18541E` |
| Artifact size | 285,879 bytes |
| Source kind | `safe_ast_extraction_of_legacy_seed_script` |
| Legacy source filename | `seed_phonemes.py` |
| Legacy source SHA-256 | `8E78BF21D3B94C4722676B080FF61FBDDF5582E45E9ECD2B1E0AAFE22BCA4853` |
| Legacy-script execution | Not performed to create this artifact |
| Record count | 689 |
| Unique `asset_code` values | 689 |

## Record structure and observed coverage

Each source record includes the fields `asset_code`, `language_code`, `symbol`, `description`, `learner_description`, `parent_asset_code`, `pinyin`, `hanzi`, `sound_production_group`, and `community_codes`. These are source-artifact fields. The clean database later assigns separate UUID and `s-...` public-reference identities when a phoneme record is first seeded; source `asset_code` must not be treated as that database identity.

| Measure | Result |
|---|---:|
| Māori (`mri`) records | 255 |
| English (`eng`) records | 44 |
| Mandarin (`cmn`) records | 390 |
| Mandarin records with non-blank pinyin | 390 |
| Mandarin records with non-blank Hanzi | 390 |
| Total community-code occurrences | 1,199 |
| Duplicate `asset_code` values | 0 |

| Community code | Linked record occurrences |
|---|---:|
| `anana` | 255 |
| `bestpractice` | 44 |
| `papatuanuku` | 255 |
| `whanau` | 255 |
| `xueyong` | 390 |

## Sound-production grouping

The `sound_production_group` field describes a broad **production-difficulty grouping**, not word frequency, learner worth, intelligence, age, or a fixed sequence of instruction.

| Group | Source-record count | Intended reading |
|---|---:|---|
| `common` | 643 | A broadly accessible production grouping in this source artifact. |
| `essential` | 31 | A grouping marked as foundational for production in this source artifact. |
| `difficult` | 15 | A grouping marked as potentially more challenging in production for some learners. |

These labels support later learner aids and reviewed pedagogical design. They do not diagnose an individual learner or replace community and specialist review.

## Boundary of this publication

This source artifact makes the original phoneme seed data inspectable without running the legacy script. It does not establish or attribute a spoken recording, a text-to-speech provider, a voice model, a speaker, an image, or a media asset. Future voice and media records must carry their own distinct provider, model, version, speaker, asset, consent, and provenance information.

The JSON copy uses its supplied CRLF line endings. A directory-scoped `.gitattributes` rule preserves those bytes during Git review and publication. Any future source revision must be a new attributable artifact with its own hash; it must not overwrite this v1 evidence record.
