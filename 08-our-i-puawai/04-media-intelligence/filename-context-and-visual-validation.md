# Filename Context and Visual Validation

**Status: operational in the Papawai test script.**

A well-named file can provide useful semantic context, especially when an image is a minimal icon or a line drawing. OpenMoji filenames provide English labels and hex codes. Noun Project files usually place a readable concept before numerical identifier and size suffixes. Existing IUWE curation can provide te reo Māori and English labels in the same filename.

The filename-aware Papawai workflow extracts a readable hint and asks Eagle to report one of four states:

| State | Meaning |
|---|---|
| `ALIGNED` | The filename context supports the visible referent. |
| `PARTIAL` | The hint is broadly related but not exact. |
| `CONFLICT` | The hint contradicts the image; the row must be reviewed. |
| `NO_HINT` | No usable human-readable filename context exists. |

The filename never overrides the image. It is an additional clue for sense selection, not a label to be blindly repeated. This separation lets a bilingual or production-friendly filename remain useful while visual truth remains visible and reviewable.
