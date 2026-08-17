# Kākano 144: Reviewed Source Specification

## Verification outcome

The revised proposal is ready to become the intended Kākano successor source.

| Check | Result |
|---|---|
| Listed rows | 144 |
| Distinct word forms | 144 |
| Order values | Complete sequence from 1 through 144 |
| Duplicate word forms | None |
| Historical Kākano 42 words retained | All 42 |
| First word | `now` |
| Last word | `always` |

The intentional opening with `now` is pedagogically coherent. It creates an immediate call to attention and leaves a small pause for call-and-response before the familiar function-word foundation begins with `the`, `I`, `you`, and `we`.

## Reviewed teaching groups

These groups are a **review and teaching aid**, not a required new CSV column. The source file should remain minimal—`order,word`—while the grouping can be retained in this specification and later connected through a curriculum layer.

| Positions | Teaching / linguistic role | Vocabulary |
|---:|---|---|
| 1 | **Attention and oral-entry cue** | `now` |
| 2–42 | **Historical relational core** | The retained Kākano foundation: determiners, personal and possessive pronouns, whānau/community relationships, care/action, literacy/numeracy/art/building, soul, basic pronouns, sky/earth, and god. |
| 43–50 | **Grammar, relation, direction, and sequence** | `do`, `and`, `in`, `to`, `for`, `up`, `down`, `then` |
| 51–63 | **Ability, perception, speech, movement, and call-response control** | `can`, `have`, `hear`, `see`, `look`, `are`, `say`, `play`, `is`, `go`, `stop`, `start`, `come` |
| 64–69 | **Description, response, uncertainty, and near-time orientation** | `big`, `little`, `yes`, `no`, `maybe`, `soon` |
| 70–81 | **People, accompaniment, place, and inquiry** | `me`, `us`, `him`, `out`, `at`, `with`, `there`, `what`, `how`, `who`, `where`, `when` |
| 82–88 | **Intergenerational relation, landscape, water world, and evaluation** | `grandfather`, `grandmother`, `ancestor`, `mountain`, `river`, `ocean`, `good` |
| 89–101 | **Reference, courtesy, nourishment, expression, desire, and imagining** | `like`, `this`, `that`, `please`, `of`, `eat`, `drink`, `laugh`, `sing`, `into`, `want`, `dream`, `some` |
| 102–115 | **Inquiry, thought, action, life stage, reciprocity, reason, and daily time** | `ask`, `know`, `put`, `take`, `old`, `new`, `young`, `give`, `live`, `thank`, `because`, `call`, `day`, `night` |
| 116–127 | **Living beings and visible qualities** | `animal`, `bird`, `fish`, `cat`, `dog`, `red`, `green`, `black`, `brown`, `blue`, `yellow`, `white` |
| 128–139 | **Finding, home, nourishment, growth, and elemental ecology** | `find`, `after`, `home`, `food`, `seed`, `plant`, `grow`, `water`, `air`, `wind`, `fire`, `cloud` |
| 140–144 | **Object relation, persistence, effort, practical agency, and care** | `them`, `try`, `tool`, `pet`, `always` |

## Source file to create

Create a new source file and leave the historical 42-word file untouched:

```text
app/seed_bank/kakano_144_seed_words.csv
```

Use this attribution-aware preamble followed by the reviewed list:

```text
# Source: paul ransfield (ordered for reciprocity)
# Attribution: paul ransfield, Kapai Group
# haporiCRM_ID: to be supplied
# List: kākano 144 — The Core Foundation Words
# Revision: 2026-08-17
# Selection rationale: first-word foundation for call-and-response, relational community sense making, practical agency, inquiry, intergenerational connection, and ecological life-world language.
order,word
```

The new word-source importer will parse all leading `#` lines as immutable snapshot metadata. It will retain the raw file hash, the 144 source occurrences, their ordering, and the selection rationale. It will not infer or fabricate the pending CRM reference.

## Relationship to Kākano 42

The Kākano 42 file remains a historical source snapshot. Kākano 144 is its successor, not a rewrite. The database will therefore be able to show the lineage of the foundation list, preserve earlier evidence, and seed the 144-word revision as the intended current Kākano source when the provenance-aware word layer is implemented.
