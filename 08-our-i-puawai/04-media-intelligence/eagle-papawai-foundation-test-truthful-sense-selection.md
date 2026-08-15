# Eagle Papawai Foundation Test — Truthful Sense Selection

**Status: under test.**

## Purpose

This test asks whether Eagle can support pictionable foundation language assets when it is constrained by a curated candidate group, a controlled sense catalogue, and filename context. The test is not designed to prove that a model is infallible. It is designed to prove that ī-puāwai can expose and route uncertainty rather than silently promoting a wrong association.

> **Close is acceptable; wrong is not.**

## Test protocol

Use 30 curated images across clear objects, actions, and competing senses. Each image receives four cohort statements limited to 144 characters, keywords, a direct visual sense, a permitted teaching sense, part of speech, and an explicit review state.

The initial ambiguity test uses six copied rows from three bat images:

| Candidate group | Flying bat | Cricket bat | Baseball bat |
|---|---|---|---|
| `animals_and_creatures` | `CLEAR` — `bat_animal` | `MISMATCH` | `MISMATCH` |
| `play_and_sport` | `MISMATCH` | `CLEAR` — `bat_cricket_equipment` | `CLEAR` — `bat_baseball_equipment` |

A Saturn image in `play_and_sport` provides a separate deliberate mismatch. The desired result is `MISMATCH`, not an inventive association.

## Required retained outputs

```text
Filename_Hint
Filename_Alignment
Candidate_Group
Validation
Visual_Sense
Teaching_Sense
Part_of_Speech
Adult / Child / Grandparent / OET statements
Keywords
Review_Status
Review_Notes
Raw_Eagle_Output
Prompt_Version
```

## Test outcome

*To be completed after the first controlled run. Record the actual number of CLEAR, MISMATCH, UNCLEAR, `candidate_ready`, and `needs_review` results. Include the six-row bat truth table and any filename conflict that reveals a useful review condition.*
