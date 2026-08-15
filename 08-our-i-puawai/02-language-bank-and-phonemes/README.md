# 02 — language bank and phonemes

**Status: phoneme CRUD and seed data are operational; identity migration is designed next.**

The language bank treats a phoneme, word, idiom, and practice event as related but distinct records. A phoneme is not merely a character; it carries a language, IPA expression where appropriate, learner description, frequency, pedagogical position, examples, and community review context. A word may contain multiple phonemes, and `word_phonemes` records their sequence and pedagogical role.

The 1,967 seeded words include Kākano, Dolch, and Papawai material. They are a starting corpus, not a closed canon. The planned identity layer adds stable UUIDs and short public references without freezing curriculum order, translation, dialect, or production filenames.

## Working principle

> **A language resource becomes stronger when sound, word, image, spoken form, learner statement, and community correction remain connected to the same referent.**

The Fomantic rotating phoneme cube is a compact interface to this wider record: phonetic form, word/sense use, media/practice use, and provenance/community status can be made visible without requiring a user to navigate a database schema.
