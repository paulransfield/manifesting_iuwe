# Eagle Wonder Captioning

**Status: operational local proof.**

The Wonder workflow uses NVIDIA Eagle 2.5-8B locally to create structured first descriptions for curated visual media. Each image receives an Adult description, Child description, Grandparent shared-reading prompt, OET-register description, and keywords. The output is resumable and is retained as raw model text plus editable working fields.

Wonder captioning is designed for visually rich content: landscape, wildlife, portraiture, texture, weather, architecture, light, and emotional atmosphere. It is not a substitute for foundation-sense selection. Its contribution is an abundant, consistent description layer that later connects to translation, audio, video, search, and community review.

## Operational lessons

- Local processing is deliberately slow on the available 8 GB GPU, but the quality of the description is more valuable than speed.
- Blank generation was resolved by decoding Eagle’s full returned sequence rather than trimming it by input-token length.
- The model can produce occasional repeated words or keywords. ī-puāwai retains raw output and makes the working fields editable rather than pretending every output is final.
- Source and provenance fields must travel with a retained caption batch before it becomes part of the language bank.
