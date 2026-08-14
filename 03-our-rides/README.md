# 03. Our Rides

> **A ride is a learning event in motion: a truthful meeting of sound, text, image, practice, and time.**

## From media collection to learning capability

A large collection of files is not yet a learning library. It becomes one when a learner can encounter a truthful, usable item and the people responsible for it can answer simple questions: *What is this? What does it mean here? Who supplied it? What may we do with it? Which version is being used?*

Our Rides describes the lifecycle that turns a source asset into a community-ready visual, audio, or video element. It gives creative work a place in a disciplined chain without making creativity subservient to a rigid filing system.

## The asset lifecycle

```text
registered source → source asset → provenance record → controlled meaning
→ approved derivative → text / audio / visual composition → practice event
→ scheduled delivery → evidence and review
```

| Lifecycle point | Minimum record | Why it matters |
|---|---|---|
| **Registered source** | Source name, rights basis, contact or public source context | The archive does not lose where an asset came from. |
| **Source asset** | Clean internal ID, path or hash, source link | A file can move without losing its identity. |
| **Controlled meaning** | Word sense or referent concept, confidence, review state | An image of Saturn is not silently allowed to become a basketball lesson. |
| **Derivative** | Parent asset, derivative type, parameters, and purpose | A thumbnail, crop, card, or audio track remains linked to its origin. |
| **Learning composition** | The approved media, statement, translation, and voice links | The learner encounters a coherent event rather than disconnected files. |
| **Practice event** | Community, purpose, delivery context, and evidence links | The event can be scheduled, observed, and improved. |

## Identity is not a filename

Filenames are useful production labels. They can carry a human hint such as `patu - cricket bat`, but they are not durable identities and they are not authoritative meaning. The ī-puāwai approach uses clean UUID identity with short public references, while a database stores the relationships among source, derivative, word sense, rights, and use.

This separation is essential for the real archive problem: the same image may live on several drives, have several crops or formats, and be useful in several teaching contexts. The system must preserve lineage without demanding that a human remember the perfect folder path.

## Truth before fluency

AI-assisted captioning is valuable when it helps reveal what an image visibly supports. It is not allowed to invent an association simply because a filename, category, or general topic makes it convenient. The current Eagle test embodies this rule:

| Visual case | Required response |
|---|---|
| A flying bat in an animal context | The animal sense may be selected. |
| A cricket or baseball bat in an animal context | `MISMATCH` must be available and respected. |
| A correctly identified source image with uncertain rights | The asset remains held for rights/provenance review. |
| A source asset with a clear parent but several derivatives | Every derivative remains traceable to that parent. |

## Rights, wishes, and reciprocity

A rights label alone may not express what a creator or source community would wish to happen in an AI-enabled, multilingual learning ecosystem. The project therefore makes room for a **Memorandum of Wishes (MoW)**, attribution, source relationships, and future reciprocity or dispute-resolution records.

This is not legal advice and not a claim that a database solves ethical questions. It is a practical commitment: where a relationship, uncertainty, wish, or concern is known, it should have somewhere durable to live.

## Next small proof

The immediate proof is a small, fully traceable chain: an EspoCRM-registered source, an image manifest record, a truthful controlled sense, an approved derivative, and one learnable composition. The database design for this chain is documented in [Our Ī-puāwai](../08-our-i-puawai/).

---

**Related chapters:** [Our Seed-Banks](../01-our-seed-banks/) · [Our Pathways](../04-our-pathways/) · [Our Proofs](../06-our-proofs/)
