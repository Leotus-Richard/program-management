> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: tpm-status
description: "Use when a program or project needs a status report for a specific audience — weekly status for the working team, a monthly leadership review, or a quarterly senior leadership review — or leadership-sync notes for a program; or when an existing report has an undefined traffic light, no path to green, or actions without owners and dates. Normally reached via /tpm; can be invoked directly."
metadata:
  author: L. Richard
  version: "0.1.0"
---

# TPM status

Produce a status report whose top half stands alone, whose colour is
defined, and where every action has an owner and a date.

Offline: use only `references/` and `assets/` here and in `../tpm/`. No
rag-mcp calls, no URLs.

## Inputs

- **Audience** — ask if not given: working team (weekly status), leadership
  with resourcing (leadership review), or senior leadership / sponsor
  (senior leadership review). The audience decides the altitude and which
  sections appear.
- The plan (`wbs.md`: milestones, feature list, buffer tracking, actuals),
  the risk log (score ≥ 5 items), the comms plan (next dates, contacts), and
  the charter (project description, metrics).
- Current state: what shipped, what slipped, open issues. From the repo
  (commits, PRs, issue tracker, test results) and from the user.

## Produce

1. Read `references/status.md`.
2. Write the one-sentence narrative first. Keep it; it becomes the first
   line of the summary.
3. Copy `assets/status-report.md` to
   `docs/tpm/status-YYYY-MM-DD.md` (or the user's path). Fill it top-down:
   - the colour, justified against the definition printed in the report
     (green / yellow / red as in `references/status.md`); if impact is not
     yet known, yellow with a date for when it will be and a point of no
     return;
   - summary in plain sentences;
   - path to green whenever the colour is not green: every row has an
     owner and a date or a date for a date;
   - decisions needed from this audience, if any;
   - below the fold, only the sections the contents-inventory table in
     `references/status.md` marks for this audience; risks at score ≥ 5
     with a link to the full log; resolved issues in their own table;
   - static sections at the bottom: description, contacts, next report
     dates from the comms plan, glossary of every acronym used above.
4. For a leadership or senior leadership review, put the program metrics
   from the charter at the very top, before the colour.
5. For a program leadership sync, use `assets/leadership-sync.md` →
   `docs/tpm/sync-YYYY-MM-DD.md` instead.
6. Run the "Clarity questions for this artifact" at the end of
   `references/status.md`. Then list, in the report to the user, every
   person named in an issue who should be told before the report is sent.

## Report

Path of the report, its audience and colour, the path-to-green actions with
owners and dates if not green, and the pre-communication list.
