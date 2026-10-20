> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: tpm-charter
description: "Draft a local program/project charter with measurable goals, scope, definitions and roadmap choices; not an implementation spec."
license: Apache-2.0
metadata:
  version: "1.1.0"
  profile: "local-task-toolkit"
  invocation: "task-specific"
  integration-status: "portable-instructions-host-untested"
---

# TPM charter

## Scope

Read `references/local-execution-contract.md` and `references/tpm-integration-rules.md` at task start. Work only from local files and supplied context. Produce drafts, not external communications, automatic implementation or persistent modes.

## Workflow

1. Read the existing local spec, PRD, README and decisions. Resolve the problem, who experiences it, business case, goal and constraints.
2. Classify program versus project. Reuse domain vocabulary; consult domain-modeling only when terms/invariants need to change.
3. Fill the charter template: one measurable goal, load-bearing term definitions, baseline/target/measurement method, scope and exclusions.
4. For a program, name project contributions and real cross-project dependencies. Record roadmap alternatives and why the chosen one fits.
5. Mark the charter draft unless approval was actually supplied. Unknown metrics, sponsors, owners and dates remain explicit open questions.
6. Run the charter and shared clarity checklists; write docs/tpm/charter.md or the requested local path.

## Reference and template map

| Bundled file | Read or use when |
|---|---|
| `references/charter.md` | before drafting or assessing a charter |
| `references/tpm-common/program-vs-project.md` | when deciding program versus project or project boundaries |
| `references/tpm-common/clarity.md` | for the closing clarity checks |
| `assets/charter.md` | copy and fill when creating the local charter |

## Default output

Assign stable goal and project IDs that the work-tracking graph can reuse in requirement/task traceability. Do not create implementation blockers from charter outline order or assume every task requires a new charter.

Local charter, classification, measurement/definition gaps, assumptions and owned or unassigned open questions.

## Failure boundary

Keep missing estimates, capacity, names, approvals and dates as explicit unknowns. Repair only the failing artifact within the shared bounds, then escalate unresolved decisions. A populated template is not evidence that work, notification, approval or delivery occurred.

## Conditional skill dependencies

- `domain-modeling`: read its installed sibling hub only for the named stage or discipline selected by this workflow.

Install the declared closure from manifest.json. These are conditional workflow/resource availability requirements, not evidence that every stage must run serially.

## Provenance and changes

Adapted from [BittahCriminal/tpm-plugin](https://github.com/BittahCriminal/tpm-plugin/blob/cb7d3efabc807136e17d5146184f1e95ddbee5a4/skills/tpm-charter/SKILL.md) at `cb7d3efabc807136e17d5146184f1e95ddbee5a4`. The original Apache-2.0 license is included. `references/ORIGINAL-SKILL.md` preserves the original hub for provenance comparisons only; its sibling/plugin syntax does not override this portable hub. Changes: local-only task scope, explicit resource paths, honest unknowns, dependency-aware routing, schedule safeguards and no network refresh. Native host behavior remains untested.
