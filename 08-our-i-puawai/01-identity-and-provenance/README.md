# 01 — identity and provenance

**Status: operational in part; schema migration and source registration in progress.**

This folder describes how ī-puāwai keeps a learning resource connected to its source, rights, asset family, derivative treatments, and review history. The system separates stable identity from descriptive production naming: an internal UUID and short public reference remain fixed, while language, curricular order, filename, visual treatment, and delivery context remain reviewable fields.

The source boundary begins in EspoCRM. A `Media Source` record holds the accountable source relationship, licence evidence, attribution requirements, Memorandum of Wishes status, reciprocity status, dispute-prevention status, and source-contact pathway. The local provenance manifest carries that source identity to observed files. ī-puāwai then records the relationship among source master, display derivative, thumbnail, card, audio, and video variants.

## Current commitments

| Commitment | Meaning |
|---|---|
| Source records precede retained ingestion | An asset is registered or visibly held for review; provenance is never silently invented. |
| SHA-256 supports binary identity | Copies and renamed files can be recognised without using filenames as truth. |
| Asset families preserve variants | PNG and SVG siblings, master and thumbnail, and production derivatives remain related rather than destructively deduplicated. |
| Rights and reciprocity are distinct | Existing licence compliance remains primary; future wishes, koha, or resolution pathways are recorded without creating invented debt. |

## Identity policy documents

The two documents below establish the UUID approach before any seed migration takes place:

| Document | Role |
|---|---|
| [ī-puāwai Identity Policy](ipuawai-identity-policy.md) | The authoritative policy: UUIDs, short public references, entity prefixes, migration rules, seed-script requirements, and asset/derivative relationships. |
| [Identity, provenance, and production naming](identity-provenance-and-production-naming.md) | The concise explanation for the living book: why a stable identity is kept separate from language, curricular order, source, and human-readable production filenames. |

> **The UUID is the seed of identity. The public reference is the handle. The filename is the production label. The relationships are the living learning system.**

See the repository-level schema review for the evolving table design: `external_sources`, `asset_source_links`, `asset_families`, `asset_variants`, `source_wishes`, `reciprocity_commitments`, and `source_resolution_cases`.
