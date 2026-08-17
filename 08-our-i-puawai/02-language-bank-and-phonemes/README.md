# 02 — language bank and phonemes

**Status: the private rebaseline has verified the UUID/public-reference foundation, clean schema, controlled reference seed, phoneme source path, Kākano 144 successor source, provenance-preserving word-source import, and an approved Papawai v2 curated-successor snapshot. The public source-artifact record now includes separate foundation-word and phoneme evidence; application and deployment work remains future work.**

The language bank treats a phoneme, word, idiom, and practice event as related but distinct records. A phoneme is not merely a character; it carries a language, IPA expression where appropriate, learner description, frequency, pedagogical position, examples, and community review context. A word may contain multiple phonemes, and `word_phonemes` records their sequence and pedagogical role.

The language sources include Kākano, Dolch, and Papawai material. They are starting corpora, not closed canons. The clean identity layer provides stable UUIDs and short public references without freezing curriculum order, translation, dialect, production filenames, or community review.

## Foundation-word source artifacts

The [Kākano 144](01-foundation-word-lists/kakano_144_seed_words.csv), [Dolch](01-foundation-word-lists/dolch_sight_words.csv), and preserved raw [Papawai v1](01-foundation-word-lists/papawai_1800_words.csv) artifacts are published as attributable source evidence. The accompanying [source specification](01-foundation-word-lists/dolch_and_papawai_source_specification.md) records their supplied hashes, row structure, provenance statements, and the Papawai repeated-header observation.

The approved [Papawai v2 curated successor](01-foundation-word-lists/papawai_1800_words_v2.csv) is a separate, attributable source artifact—not a replacement for raw v1 evidence. Its [approved decision ledger](01-foundation-word-lists/papawai_1800_v2_approved_decision_ledger.csv) records 357 reviewed removals, 54 broad-everyday transport additions, five recategorisations, and retained `Boat`; its [v2 source specification](01-foundation-word-lists/papawai_1800_v2_source_specification.md) records the source and decision hashes, lineage, and review boundary. Health and wellbeing remains a deliberately separate later foundation gate.

Publication does not elevate any list into a closed curriculum or replace community authority over later membership, ordering, translation, or subset decisions.

## Phoneme source artifact

The [phonemes v1 artifact](02-phoneme-source-artifacts/phonemes_v1.json) is a byte-preserved, 689-record source artifact generated through static extraction of the legacy phoneme seed script without executing that script. Its [source specification](02-phoneme-source-artifacts/phonemes_v1_source_specification.md) records the artifact and legacy-source hashes, language and community-code coverage, Mandarin pinyin/Hanzi fields, and the intended meaning of the `sound_production_group` field. The artifact is transparent seed evidence, not an audio asset, a voice-model attribution, or a final curriculum authority.

## Working principle

> **A language resource becomes stronger when sound, word, image, spoken form, learner statement, and community correction remain connected to the same referent.**

The Fomantic rotating phoneme cube is a compact interface to this wider record: phonetic form, word/sense use, media/practice use, and provenance/community status can be made visible without requiring a user to navigate a database schema.
