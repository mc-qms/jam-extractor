---
name: jam-delta-classification
description: The Compare and Classify pass of a JAM extraction — class definitions for procedure-vs-practice differences, evidence rules, and the delta report format with dispositions left blank. Use in Phase 3 (Compare) and Phase 4 (Classify), after the recall ledger is closed.
---

# Delta Classification

## Inputs

The closed recall ledger and the governing document. Nothing else.
A detail that is not in the ledger does not enter the report, and
the interview conversation itself is not evidence — the ledger is.

## Classes

Assign exactly one class per step:

- **ALIGNED** — the recalled practice matches the written step in
  substance: same actions, same checks, same decision points.
  Wording differences that change nothing are ALIGNED, noted as
  wording-only.
- **PROCEDURE STALE** — the recalled practice differs from the
  written step, and the evidence indicates the practice reflects
  current reality while the document does not: the practitioner
  describes a change (new equipment, new material, a step that no
  longer exists) the document never caught up with. Requires
  evidence in the ledger — typically a SELF-REPORTED CHANGE flag
  or a concrete, checkable detail.
- **PRACTICE DRIFTED** — the written step is specific and current,
  and the recalled practice differs from it without an indication
  that the world changed: a check skipped, a sequence reordered, a
  criterion applied loosely.
- **RECALL GAP** — the practitioner could not recall the step
  unaided (ledger flag). This class says nothing about what they
  do at the bench; it says the step does not live in memory, which
  is its own finding.
- **UNVERIFIABLE** — the account is too thin, internally
  contradictory, or missing the detail a comparison would need.
  Use this class rather than guessing. An honest UNVERIFIABLE is a
  finding; a confident wrong class is a defect.

STALE and DRIFTED can look identical from inside an interview. The
distinguishing question is whether the evidence points at the
world having changed or at the practice having wandered. Where the
evidence genuinely cannot separate them, classify UNVERIFIABLE and
say so in the evidence note — do not split the difference.

## Evidence rules

- Every non-ALIGNED classification quotes the ledger entry it
  rests on and cites the written step it was compared against.
- Hedges survive into the report. If the practitioner said
  "usually", the report says "usually" — a qualified account
  classified as a certainty is a fabrication.
- One step, one class. If a step both drifted and contains
  unwritten practice, classify by the difference that matters to
  the process and record the other in the evidence note.

## The delta report

- Header: process, document and version, ledger reference, date,
  counts by class.
- One entry per non-ALIGNED step: step identifier and title,
  class, the recalled practice (quoted from the ledger), the
  written step (cited), the evidence note, and a **Disposition**
  field left blank.
- ALIGNED steps are listed by identifier only, so the reader can
  see the comparison covered the whole document.
- Closing note, always present: classifications are indications
  with evidence, made from one practitioner's recall. Disposition —
  revise the document, retrain, observe the process, or accept —
  belongs to a human with the competence to make it.
