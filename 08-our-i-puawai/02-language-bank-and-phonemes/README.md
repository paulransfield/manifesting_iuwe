# 02 — language bank and phonemes

**Status: the private rebaseline has verified the UUID/public-reference foundation, clean schema, controlled reference seed, phoneme source path, Kākano 144 successor source, and provenance-preserving word-source import. The public source-artifact record is now established; application and deployment work remains future work.**

The language bank treats a phoneme, word, idiom, and practice event as related but distinct records. A phoneme is not merely a character; it carries a language, IPA expression where appropriate, learner description, frequency, pedagogical position, examples, and community review context. A word may contain multiple phonemes, and `word_phonemes` records their sequence and pedagogical role.

The language sources include Kākano, Dolch, and Papawai material. They are starting corpora, not closed canons. The clean identity layer provides stable UUIDs and short public references without freezing curriculum order, translation, dialect, production filenames, or community review.

## Foundation-word source artifacts

The [Kākano 144](01-foundation-word-lists/kakano_144_seed_words.csv), [Dolch](01-foundation-word-lists/dolch_sight_words.csv), and [Papawai](01-foundation-word-lists/papawai_1800_words.csv) artifacts are published as attributable source evidence. The accompanying [source specification](01-foundation-word-lists/dolch_and_papawai_source_specification.md) records their supplied hashes, row structure, provenance statements, and the Papawai repeated-header observation. Publication does not elevate any list into a closed curriculum or replace community authority over later membership, ordering, translation, or subset decisions.

## Working principle

> **A language resource becomes stronger when sound, word, image, spoken form, learner statement, and community correction remain connected to the same referent.**

The Fomantic rotating phoneme cube is a compact interface to this wider record: phonetic form, word/sense use, media/practice use, and provenance/community status can be made visible without requiring a user to navigate a database schema.
