# 05 — translation and voice

**Status: existing translation and XTTS workflows proven; MMS-TTS extension designed next.**

The translation and voice layer converts an approved source statement into a reviewed target-language statement and spoken form. It must not ask a text model to guess what an image contains when a visual model and curated sense already provide a grounded source record. Translation is a distinct task: preserve intended referent, register, learner level, and character constraint while giving language kaitiaki a visible approval pathway.

The existing local pipeline has demonstrated Mistral translation and XTTS-v2 voice generation. Meta MMS-TTS provides a further route for languages underserved by commercial speech systems, including te reo Māori and many Pacific, indigenous, and endangered languages. The availability of a model does not remove the need for community review of the words being spoken.

## Required links

```text
approved source statement
    → translation version and reviewer
    → voice model or speaker record
    → audio asset variant
    → practice event and delivery record
```

The language bank stores the relationship so corrected translations or recordings can replace a working variant without losing the underlying asset, sense, or history.
