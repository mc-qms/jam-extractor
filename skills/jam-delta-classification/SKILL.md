---
name: jam-delta-classification
description: The Compare and Classify pass of a JAM extraction — class definitions for procedure-vs-practice differences, evidence rules, and the delta report format with dispositions left blank. Use in Phase 3 (Compare) and Phase 4 (Classify), after the recall ledger is closed.
---

# Delta Classification

## Inputs

The closed recall ledger and the governing document. Nothing else.
A detail that is not in the ledger does not enter the report, and
the interview conversation itself is not evidence — the ledger is.
Work from the emitted ledger text: an agent that conducted the
interview holds the conversation in context, and the conversation
is still not evidence. Re-read the closed ledger and classify only
from it.

Steps drawn from a supporting document are compared against that
document, cited by name. The supporting document is under review
by association: a difference found on one of its steps is reported
exactly as one on the governing document's steps.

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

UNMAPPED steps — steps the practitioner performs that the step
map did not contain — are compared against the document as a
whole, not against a single written step. Where no written step
corresponds, classify PROCEDURE STALE and state in the evidence
note that the step is absent from the document: practice exists
that the document does not describe, which is the plainest form
of a stale document there is.

STALE and DRIFTED can look identical from inside an interview. The
distinguishing question is whether the evidence points at the
world having changed or at the practice having wandered. Where the
evidence genuinely cannot separate them, classify UNVERIFIABLE and
say so in the evidence note — do not split the difference.

## Evidence rules

- Report lists, not totals. Do not state a number you arrived at
  by counting entries; list the entries instead. A reader can
  count a list — they cannot audit a number that appears from
  nowhere.
- Every non-ALIGNED classification quotes the ledger entry it
  rests on and cites the written step it was compared against.
- A step whose ledger entry carries any flag may not be classified
  ALIGNED without an evidence note stating why the flag does not
  change the class. ALIGNED is a conclusion, not a default.
- Write findings against steps and documents, never against the
  practitioner: "no practice was recalled for Step 7", not "the
  practitioner could not recall Step 7".
- Hedges survive into the report. If the practitioner said
  "usually", the report says "usually" — a qualified account
  classified as a certainty is a fabrication.
- One step, one class. If a step both drifted and contains
  unwritten practice, classify by the difference that matters to
  the process and record the other in the evidence note.

## The delta report

- Header: process, document and version, ledger reference, date,
  and a class roster — each class named, with the step identifiers
  assigned to it listed.
- If the ledger header records any mapped document as draft,
  superseded, or not stated, a baseline note follows the header:
  classifications were made against a document whose currency was
  not verified, and a difference may belong to the baseline
  rather than to the practice.
- One entry per non-ALIGNED step: step identifier and title,
  class, the recalled practice (quoted from the ledger), the
  written step (cited), the evidence note, and a **Disposition**
  field left blank.
- A standing section, **"Practice the document does not
  describe"**, listing every UNWRITTEN PRACTICE and UNMAPPED item
  from the ledger, and every written step for which no practice
  was recalled. The nuances that are not written, or are written
  differently, are the point of the exercise; they are never left
  buried inside per-step evidence notes. When the ledger carries
  no such items, the section is a single line stating so — an
  omission made visible, not a section padded out
  (Proportionate Writing with Omissions).
- ALIGNED steps are listed by identifier only, so the reader can
  see the comparison covered the whole document.
- Closing note, always present: classifications are indications
  with evidence, made from one practitioner's recall. Disposition —
  revise the document, retrain, observe the process, or accept —
  belongs to a human with the competence to make it.
