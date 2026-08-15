## Identity, provenance, and production naming

ī-puāwai uses a deliberately separated identity model so that a learning object can remain trustworthy while its language, curriculum placement, visual treatment, production file, or community use evolves.

Every core object—sound, word, idiom, practice event, lesson, media asset, source, evidence, and receipt—receives two stable identifiers:

| Identifier | Purpose | Example |
|---|---|---|
| **Canonical UUID** | Permanent internal record identity; generated once and never changed | `0199cbd6-f880-7a2e-9eef-5de50d176915` |
| **Prefixed public reference** | Short human-facing handle for URLs, CSVs, support, and community discussion | `w-2FQ8AX` |

The prefix is intentionally simple: `s` for sound/phoneme, `w` for word, `i` for idiom or phrase, `p` for practice event, `l` for lesson, `a` for media asset, `f` for asset family, `v` for asset variant, `x` for external source, `d` for description, `e` for evidence, and `r` for receipt.

Language, dialect, curricular sequence, word text, translation, source, and media version remain structured, reviewable fields. They are never packed into the permanent identity. This permits a community to correct a translation, resequence a lesson, replace a thumbnail, revise a statement, or add a new dialectal expression without breaking the provenance chain.

Human-readable filenames remain useful for production. A file such as `mri_w_000001_te_the_np_v01_classroom_adult_male_native.wav` can communicate context quickly, but its meaning is backed by relational records: source provenance, asset family, media variant, word sense, statement, and practice event.

> **The UUID is the seed of identity. The public reference is the handle. The filename is the production label. The relationships are the living learning system.**

This approach allows ī-puāwai to preserve unique local URLs and SHA-256-supported file provenance without requiring a community to memorise machine identifiers or adopt a blockchain wallet.
