> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: tpm-charter
description: "Use when a program or project needs a charter — a problem statement, business case, measurable goal, scope boundaries, and (for a program) its project structure — or when an existing goal is too vague to plan against. Normally reached via /tpm; can be invoked directly."
metadata:
  author: L. Richard
  version: "0.1.0"
---

# TPM charter

Produce the charter for a program or project: the document that tells a
newcomer *why* this exists, *what* done looks like, and *where the edges
are*.

Offline: use only `references/` and `assets/` here and in `../tpm/`. No
rag-mcp calls, no URLs.

## Inputs

Look in the repo first: spec, PRD, PDR/ADR, existing plan, README. Ask the
user only for what is missing from: the problem, who has it, the business
reason, the intended end state, any hard constraint (date, budget, external
commitment).

## Produce

1. Read `references/charter.md`.
2. If not already decided this run, read `../tpm/references/program-vs-project.md`
   and decide program or project. Record the decision in the charter.
3. Copy `assets/charter.md` to `docs/tpm/charter.md` (or the user's path)
   and fill every section. The charter is complete when:
   - the problem statement names who has the problem and what happens if
     nothing is done;
   - the goal is one measurable sentence, and every load-bearing term in it
     has a row in the definitions table;
   - the success-metrics table has at least one row with baseline, target,
     and how it is measured (or an open question saying which is unknown);
   - out-of-scope lists at least the things a reader would wrongly assume
     are in;
   - for a program, the project-structure table has one row per project
     with its contribution to the program goal and its dependencies;
   - the roadmap names the alternatives considered and why this one was
     chosen;
   - assumptions are listed as assumptions; open questions have an owner
     and a needed-by date.
4. Run the "Clarity questions for this artifact" list at the end of
   `references/charter.md`. Put any unanswered question in the charter's
   Open questions table rather than choosing a default silently.

## Report

Path of the charter, the program-or-project decision in one sentence, and
the open questions with owners.
