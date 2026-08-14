# 06. Our Proofs

> **Proof is not surveillance. It is the minimum truthful record needed to honour a promise, correct an error, and learn what should happen next.**

## What must be provable

A community-operated learning system makes several different promises. It promises that a source is not lost, that an approved asset was actually delivered, that a contribution was directed as agreed, and that a learner or community can question what happened. These promises need different kinds of evidence.

The purpose is not to create a totalising record of every person. The purpose is to make the system **answerable** at the points where it has made a claim.

## Evidence is layered

| Claim | Evidence that may support it | What it does **not** prove by itself |
|---|---|---|
| An asset came from a stated source | Source registration, manifest path, hash, attribution, and rights note | That every future use is appropriate. |
| A derivative came from a parent asset | Parent ID, derivative type, parameters, and hash | That the derivative is pedagogically suitable. |
| An event was scheduled | Timezone-aware schedule record | That it was actually served. |
| An event was delivered | Attempt, served, and error records with timestamps and evidence links | That a learner understood it. |
| A learner engaged | Consent-aware completion or practice signal | That learning has permanently occurred. |
| A contribution was allocated | Koha, receipt, and linked delivery evidence | That all community benefit has been captured in a number. |

This distinction matters. A receipt should not overclaim educational impact. A completion should not be treated as a complete account of a person’s learning. Evidence should be proportionate to the promise.

## From scheduled event to receipt

```text
scheduled practice event
        ↓
delivery attempt → served record or error record
        ↓
evidence hash / durable reference
        ↓
delivery receipt linked to enabler and event
        ↓
optional, consent-aware practice-completion aggregate
        ↓
community review, renewal, correction, or retirement
```

Each stage should be able to say what it knows and what it does not know. Where evidence is missing, a system should be able to state that honestly rather than silently filling the gap with optimism.

## Review and resolution

Proof becomes useful when it supports correction. The repository’s emerging pattern includes review queues and resolution cases for issues such as a wrong image-to-word-sense match, uncertain source rights, inaccurate attribution, a community concern, delivery failure, or a request to retire material.

| Event | Required response |
|---|---|
| Image does not truthfully support the selected word sense | Mark `MISMATCH` or `needs_review`; do not release automatically. |
| Source terms or creator wishes are unclear | Hold the asset, record the uncertainty, and seek an appropriate relationship. |
| Delivery fails | Keep the error evidence, retry where agreed, and make the receipt truthful. |
| Community reviewer raises a concern | Create a review or resolution case with clear status and ownership. |
| Material is no longer appropriate | Retire or restrict the asset while preserving a traceable record of the decision. |

## Evidence with restraint

Learner dignity is a design boundary. Where learning progress is recorded, use the least identifiable and least intrusive evidence that meets the agreed purpose. Community councils and learners should be able to understand what is being counted, what is being kept, and what is not being claimed.

## Next small proof

The next proof should be humble and complete: one registered media source, one controlled asset, one scheduled event, one delivery log, and one human-readable receipt. The architecture becomes credible by showing the full chain at small scale before claiming global scale.

---

**Related chapters:** [Our Rides](../03-our-rides/) · [Our Pathways](../04-our-pathways/) · [Our Tickets](../05-our-tickets/) · [Our Ī-puāwai](../08-our-i-puawai/)
