# Dolch and Papawai foundation-word source specification

**Status:** public source-evidence record. **Publication date:** 2026-08-17. **Scope:** this record publishes byte-preserved copies of two supplied CSV source artifacts. It does **not** correct, normalise, deduplicate, reorder, translate, level, license, or otherwise redefine their vocabulary.

> **Community authority remains decisive.** These files ring-fence an attributable starting base for future review; they are not a closed curriculum, a final word count, or an authority over later community decisions.

## Artifact register

| Source code | Public artifact | Source statement preserved from file | SHA-256 | Structural reading at publication |
|---|---|---|---|---|
| `dolch_nz_year_levels` | [dolch_sight_words.csv](dolch_sight_words.csv) | `Source: https://sightwords.com/sight-words/dolch/, 2026-08-13` | `382AF64E1358C50A44C37F13DEEE04BC0D652664BB818B86344E40E9DC433B09` | Four comment-preamble lines; `category,word` header at line 5; 313 candidate source rows. |
| `papawai_1800` | [papawai_1800_words.csv](papawai_1800_words.csv) | `Source: paul ransfield (ordered by category and word length)` | `3E38F0518A21C1B08A3D542596522F2FDBC586C8F528ED2C7B76BB3B0A5776D1` | Four comment-preamble lines; first `category,word` header at line 5; 1,633 candidate source rows before duplicate-word consolidation; a repeated `category,word` structural row at line 1,639. |

The public copies retain the attribution and `haporiCRM_ID` statements supplied in their respective preambles. The Dolch file’s preamble says `Attribution: to be supplied`; this publication does not invent or replace it. The Papawai file’s preamble attributes the list to Paul Ransfield and Kapai Group. Publication records the supplied attribution statements; it does not create a new copyright licence or claim authority beyond the approved public release.

## Why the Papawai filename is not treated as a verified row count

The filename `papawai_1800_words.csv` is historical source naming, not a verified assertion that the file presently contains 1,800 valid vocabulary entries. The raw file is published intact. Its final line is a second `category,word` header, preserved as evidence rather than silently removed. Accordingly, this record distinguishes the **raw artifact** from a future **reviewed interpretation** of its word rows.

| Measure | Dolch | Papawai |
|---|---:|---:|
| Candidate vocabulary rows before duplicate-word consolidation | 313 | 1,633 |
| Repeated header-like rows after the first header | 0 | 1 |
| Current filename numeral asserted as a verified row count | No | No |

A future private parsing correction may produce a new, attributable interpretation that recognises repeated header rows as structural metadata. It must preserve the raw source file and the earlier interpretation as historical evidence; it is intentionally outside this publication.

## Integrity and review use

The SHA-256 values above allow any reader to verify that a downloaded public CSV is the same byte sequence that was approved for publication. The files should be used as attributable starting points for curriculum, media, translation, and community-review work—not as algorithmic authority over membership, sequence, or cultural meaning.

The related [Kākano 144 source specification](kakano_144_source_specification.md) records the separately community-governed first-word foundation. Together, the artifacts preserve different kinds of provenance: Kākano’s community review and relational ordering, Dolch’s supplied external source record, and Papawai’s supplied local source record.
