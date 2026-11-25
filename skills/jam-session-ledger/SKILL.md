---
name: jam-session-ledger
description: The recall record of a JAM extraction — header, per-step entries, flags, and coverage states. Use throughout Phase 2 (Recall); the closed ledger is the sole input, with the governing document, to the Compare phase.
---

# Session Ledger

The ledger is the session's evidence. The delta report may only
contain what the ledger supports, so the ledger is written as if
the report's reader will never meet the practitioner — because
they won't.

## Header

- Process and governing document (number, title, version), or
  UNGOVERNED if there is no document.
- Step map source: from the document, from the practitioner's own
  account, or both. A map built from an account is itself recall
  and is weighed as such in Compare.
- Practitioner role (not name, unless the session's owner requires
  it — findings attach to steps, not people).
- Date, session number if the extraction runs across sittings.
- Flags applying to the whole session: RECENT EXPOSURE if the
  practitioner has recently read the document.

## Per-step entry

One entry per step on the map, in map order:

- **Step** — identifier and title, as on the map.
- **Recalled practice** — what the practitioner said they do, in
  their own words. Load-bearing details (values, sequences, checks,
  decisions) are quoted verbatim.
- **Probes used** — which rungs of the probe ladder were asked.
- **Flags** — any of:
  - RECALL GAP — the practitioner could not recall this step
    unaided.
  - CONSULT REQUEST — the practitioner asked to look the step up.
  - HEDGE — the account was qualified ("usually", "it depends")
    and the dependency could not be pinned down.
  - UNWRITTEN PRACTICE — the practitioner described doing something
    they believe is not written anywhere.
  - UNMAPPED — this entry is a step the practitioner performs that
    the step map does not contain. It gets a full entry, placed
    where the practitioner places it in the sequence, and is never
    merged into a neighbouring step to make the map look complete.
  - SELF-REPORTED CHANGE — the practitioner said the practice
    changed at some point ("we haven't done it that way since…").
- **Coverage** — one of:
  - WALKED — the step was interviewed.
  - NOT WALKED — the session ended before this step. Never leave a
    step unaccounted for: a missing entry reads as agreement, and
    silence is not agreement.

## Rules

- Write entries as the session goes, not from memory afterwards.
  The ledger has the same obligation as the practitioner: recall
  is lossy, and this record is the one that must not be.
- Keep the practitioner's terms. If you clarify a term, keep their
  word in the entry and put the clarification in brackets.
- Record contradictions inside a single account as they stand, both
  versions. Do not reconcile them in the ledger; reconciliation is
  a Compare-phase question.
- Close the ledger explicitly at the end of Recall: a closing line
  stating the number of steps walked, not walked, and flagged.
  Nothing is added to a closed ledger. If a second sitting is
  needed, it opens a new ledger that references the first.
