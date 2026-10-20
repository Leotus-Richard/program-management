> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: tpm-stakeholders
description: "Use when a program or project needs its stakeholders identified and a communication plan — who receives which update on what cadence, a RACI, a kickoff agenda, and (for a program) a leadership sync — or when reporting is inconsistent, stakeholders are being surprised, or roles are unclear. Normally reached via /tpm; can be invoked directly."
metadata:
  author: L. Richard
  version: "0.1.0"
---

# TPM stakeholders

Produce the stakeholder list, communication plan, and roles chart — the
artifact a TPM looks at more often than any other.

Offline: use only `references/` and `assets/` here and in `../tpm/`. No
rag-mcp calls, no URLs.

## Inputs

- The charter (sponsor, owner, stakeholder groups) and the plan (which
  systems and teams the tasks touch).
- The risk log (risks with named owners; risks that need a subject-matter
  expert).
- Whatever the repo says about people and channels: README, CODEOWNERS,
  contributing guide, existing meeting notes.
- From the user, when the repo cannot say: names and roles, which channels
  they read, the organisation's reporting norms (day of week, review
  cadence, who presents to whom).

## Produce

1. Read `references/stakeholders.md`.
2. Copy `assets/comms-plan.md` to `docs/tpm/comms-plan.md` (or the user's
   path) and fill it in this order:
   - **Communication types** — keep only the types this program needs,
     but decide explicitly; give each a cadence *and* a slot (day of week /
     week of month), a channel, and an owner. Write the report sequence so
     each report feeds the next. State the pre-communication rule.
   - **Stakeholder list** — one row per person or group, with role,
     organisation, project(s), a tick per communication type received,
     any SME area, and preferred channel. Include everyone impacted down
     the chain; mark unknown names as open questions rather than leaving
     them out.
   - **RACI** — one A per activity; no blank cells (use (C)/(I) for
     optional). Note the date it was, or will be, discussed with the team.
   - **Kickoff agenda** with a date (or an open question for the date).
   - **Leadership sync** format when it is a program.
   - **Escalation** rows: at minimum blocked team, risk reaching score 5–6,
     cross-project impact.
3. Run the "Clarity questions for this artifact" at the end of
   `references/stakeholders.md`. Unanswered questions go in the Open
   questions table.

## Report

Path of the plan, the communication types chosen with their slots, the
number of stakeholders listed and how many are still unnamed, and the open
questions with owners.
