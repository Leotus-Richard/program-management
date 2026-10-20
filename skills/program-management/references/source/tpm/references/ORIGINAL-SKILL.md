> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: tpm
description: "Use when the user invokes /tpm or asks to run, set up, plan, or manage a program or project as a technical program manager — chartering work, building a delivery plan, assessing risks, organising stakeholders and communication, or reporting status. Runs fully offline from bundled references; never calls a RAG or network source."
metadata:
  author: L. Richard
  version: "0.1.0"
---

# TPM

Operate as the technical program manager for the user's program. `/tpm` is
the front door: it works out which stage the program is at, runs the
matching sub-skill(s), and finishes with a clarity check across everything
produced. Each sub-skill can also be invoked on its own.

## Offline rule

Everything needed is in this plugin's `references/` and `assets/`
directories. **Do not call the rag-mcp tools or fetch any URL while running
these skills.** The one exception: the user explicitly asks to refresh the
references, in which case follow `references/SOURCES.md`.

## What `/tpm` does

1. **Establish context.** Read what the repo already has: spec, PRD, plan,
   backlog, ADRs, and anything under `docs/tpm/`. Identify the program (or
   project) by name, its goal, and which artifacts already exist. Ask the
   user only for what the repo cannot answer.

2. **Decide program or project.** Read `references/program-vs-project.md`
   and apply the litmus test. State the decision and why in one or two
   sentences before continuing.

3. **Select stages.** Default order and skill for each:

   | Stage | Skill | Skip when |
   |---|---|---|
   | Charter | `tpm-charter` | `docs/tpm/charter.md` exists and the user did not ask to redo it |
   | Plan | `tpm-plan` | `docs/tpm/wbs.md` exists and is current |
   | Risk | `tpm-risk` | `docs/tpm/risk-register.md` exists and is current |
   | Stakeholders | `tpm-stakeholders` | `docs/tpm/comms-plan.md` exists |
   | Status | `tpm-status` | the user did not ask for a report and no earlier stage changed |

   If the user named a stage, run that stage only.

4. **Invoke each selected sub-skill**, in order, by name (`tpm-charter`;
   when installed as the Claude Code plugin the name is `tpm:tpm-charter`).
   If the host has no skill-invocation tool, read the sub-skill's
   `SKILL.md` from its sibling directory and follow it. Each
   one reads its own reference, fills its own template, and writes its
   artifact to `docs/tpm/` (or the path the user names). Later stages read
   the artifacts earlier stages produced.

5. **Closing clarity check.** Run the checklist at the end of
   `references/clarity.md` across every artifact produced this run. Anything
   that fails goes back to the owning sub-skill before reporting.

6. **Report.** List each artifact with its path, the program-or-project
   decision, and the consolidated open questions with owners. Do not
   summarise the artifacts' contents.

`/tpm` produces no artifacts itself. If a request does not map to any stage
(for example "is this a program?"), answer from `references/` directly.

## Reference map

| File | Read when |
|---|---|
| `references/clarity.md` | Every run — the method and the closing checklist; question banks the sub-skills use |
| `references/program-vs-project.md` | Deciding program vs project; cutting project boundaries; what changes at program level |
| `references/SOURCES.md` | Only when the user explicitly asks to refresh references |

## Sub-skills

| Skill | Produces |
|---|---|
| `tpm-charter` | Program / project charter |
| `tpm-plan` | Requirements + use cases, task breakdown with estimates, buffer matrix, work breakdown with dates |
| `tpm-risk` | Risk log |
| `tpm-stakeholders` | Stakeholder list, communication plan, RACI, kickoff agenda |
| `tpm-status` | Audience-leveled status report; leadership sync notes |
