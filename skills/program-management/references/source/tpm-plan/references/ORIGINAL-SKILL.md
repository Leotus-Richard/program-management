> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: tpm-plan
description: "Use when a program or project needs a delivery plan from its requirements — refined requirements and use cases, a task breakdown with estimates, buffers and team overhead, predecessors, and a dated work breakdown — or when an existing plan has no buffers, no traceability, or has to be re-planned after a resourcing change. Normally reached via /tpm; can be invoked directly."
metadata:
  author: L. Richard
  version: "0.1.0"
---

# TPM plan

Turn requirements into a plan the team can execute and the TPM can re-plan
in minutes when headcount changes. Four artifacts, each traceable to the one
before:

```
requirements.md → tasks.md → buffer-matrix.md → wbs.md
```

Offline: use only `references/` and `assets/` here and in `../tpm/`. No
rag-mcp calls, no URLs.

## Inputs

- The charter (`docs/tpm/charter.md`) or, failing that, the goal.
- Raw requirements: spec, PRD, backlog, issue list.
- Any existing estimates and who made them.
- The team: who, their overhead (on-call, meetings, training, leave), and
  the dev manager to confirm it. If the user cannot supply overhead, use the
  matrix defaults and mark the number as an assumption.

**If no team is assigned yet** (no names, no estimates): still build all
four artifacts. Fill structure — requirements, use cases, stories, tasks,
predecessors, crash options, milestones, feature list — from the inputs.
Leave Estimate, Duration, Start, End, and Resources as open questions with
"team assigned" as the needed-by trigger; put the buffer matrix's overhead
in as the default with confidence "low". The plan is then ready to
re-plan in one pass the day a team exists.

## Produce

Read `references/planning.md` first. Then, in order:

1. **`docs/tpm/requirements.md`** from `assets/requirements.md`.
   Outline-number the requirements; keep originals visible and add
   refinements beneath them; split compound lines; add the non-functional
   work the change forces. Write use cases as "As a …, I can … so that …",
   each tracing to requirement IDs. Complete when every requirement ID
   appears in at least one use case and the coverage line says so.

2. **`docs/tpm/tasks.md`** from `assets/tasks.md`. Stories map to use
   cases; tasks are outline-numbered under stories. Every task row carries:
   what the estimate includes, estimator familiarity, confidence, ambiguity,
   new-tech flag, and who else touches the same code. Add the always-present
   tasks (review, integration test, e2e test, security review, deploy,
   launch). List the design choices the breakdown made and the ones it left
   open. If estimates came from the user or the repo rather than the team,
   say so in the Estimate review section.

3. **`docs/tpm/buffer-matrix.md`** from `assets/buffer-matrix.md`. Fill
   the overhead table (on-call, meetings, training, events, leave, freezes),
   its source and confidence, and the resulting matrix. Add known
   unavailability as rows to be placed in the plan.

4. **`docs/tpm/wbs.md`** from `assets/wbs.md`. One row per task with
   requirement IDs, estimate, buffer % from the matrix, duration,
   predecessor(s) with type (fs/ss/ff/sf and lags), crash count, resources,
   start and end. Add explicit unavailability rows. Fill the fast-track and
   crash options table, the milestones (design / implementation / UAT /
   launch), the feature list (top-level stories), and — for a program — the
   cross-project dependencies table. Every assumption the schedule rests on
   (uniform estimates, fs-only, no resource constraints) goes in the
   Assumptions section.

5. Run the "Clarity questions for this artifact" at the end of
   `references/planning.md`. Unanswered questions go in the Open questions
   table of the artifact they affect.

## Report

Paths of the four files, the total buffered duration and the critical
sequence in one or two sentences, the overhead figure and whether it is
measured or assumed, and the open questions with owners.
