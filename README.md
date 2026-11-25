# JAM Extractor — Judgement And Memory

Tribal-knowledge extraction for critical processes.

## The term

**JAM — Judgement And Memory.** A person in whom a critical process
actually resides. The written procedure exists, but the working
knowledge of how the process is really performed — the checks, the
workarounds, the judgement calls at each step — lives only in that
person's judgement and memory.

When a JAM is unavailable, the process is unavailable, whatever the
document says. Most organizations find their JAMs by losing one.

## What this is

An agent package — instructions and skill files, no application —
that interviews a JAM and produces a **procedure-vs-practice delta
report**:

1. **Seal.** The agent reduces the governing document (an SOP, a
   test method, a batch record) to a step map: step identifiers and
   titles only. The content is set aside.
2. **Recall.** The agent walks the step map with the practitioner,
   one step at a time, and asks how they perform it — from memory.
   The practitioner does not consult the document. That rule is the
   method: the moment they can read the step, you are testing
   reading, not practice.
3. **Compare.** Only after the recall record is closed does the
   document's content come back in. Each step's recalled practice is
   compared against the written step.
4. **Classify.** Each difference is classified — procedure stale,
   practice drifted, recall gap, unverifiable — with the evidence
   quoted. The disposition field is left blank. What to do about a
   gap is a human decision; the agent's job ends at finding and
   naming it.

The gaps are the deliverable. Each one is either a procedure that no
longer describes reality or practice that has drifted from the
procedure, and a quality system wants both kinds found by an agent
instead of by an inspector.

## Why memory only

There are two versions of every process: the one in the document and
the one in the person. Audits sample the first. Incidents reveal the
second. An interview that lets the practitioner read the procedure
collapses the two into one and finds nothing — it measures whether
they can recognise the step, not whether the step is what they do.

A step the practitioner cannot recall unaided is not a failed
interview. It is a finding, and it is recorded as one.

## Running a session

This package deliberately does not prescribe how sessions are
administered — scheduling, selection, and setting belong to the
organization adopting it. Two things, though, are not optional,
because the method stands on them.

**Honesty without consequences.** Recall is only honest when the
practitioner believes the truth is safe. Before a session, someone
with the standing to make it true should say so plainly: this is
to improve the process, complete honesty is what is needed, and
nothing provided will affect the practitioner's position or
standing. The agent repeats the assurance in its opening; the
organization has to be the one that keeps it. The obligation runs
in both directions — procedures should be followed, and procedures
should also reflect actual practice — and a delta report that only
ever produces corrections for people, never for documents, teaches
the next practitioner to perform instead of recall.

**Recall before preparation.** The session measures practice as it
lives in memory. A practitioner who has just re-read the document
for the occasion hands the document back to you, and the delta
disappears. Sessions work best when they begin when they begin,
with no preparation interval in between.

Shapes with the right properties, offered as examples rather than
instructions: a facilitated group session — practitioners in a
room, told to download the governing documents, load them into the
chat, and follow the prompts, everyone starting together — or an
individual session opened by a senior person's explicit
no-consequences framing.

## Contents

- `agent-instructions.md` — the interviewer agent's instruction set:
  role, phases, hard rules, and outputs.
- `skills/jam-interview-conduct/` — how a recall session runs: the
  opening framing, the per-step probe ladder, and verbatim capture.
- `skills/jam-memory-only-guard/` — the memory-only constraint and
  how the agent holds it, including when the practitioner asks to
  look something up.
- `skills/jam-session-ledger/` — the recall record: format, coverage
  tracking, and flags.
- `skills/jam-delta-classification/` — the compare-and-classify pass:
  class definitions, evidence rules, and the delta report format.

The package is platform-neutral. It was written for declarative
agent builders that accept an instruction set plus skill files, and
the design follows one rule throughout: the structure carries the
discipline, so the model only has to be literate.

## Honest limits

- The memory-only guard is behavioural, not cryptographic. The agent
  works from a step map and is instructed never to reveal step
  content during recall; a platform that cannot withhold the source
  text from the model relies on that instruction being followed.
- A classification is an indication with evidence, not a conclusion.
  "Procedure stale" and "practice drifted" can look identical from
  inside an interview; the report says which way the evidence leans
  and leaves the disposition blank on purpose.
- This package extracts and compares. It does not revise procedures,
  assess risk, or decide anything. Those remain human work, done by
  someone competent to catch the failure modes.

## License

MIT — see `LICENSE`. Use it, adapt it, and if you find the JAMs in
your own building before they leave, it did its job.
