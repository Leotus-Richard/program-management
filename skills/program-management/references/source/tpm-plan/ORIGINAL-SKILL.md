> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: tpm-plan
description: "Build a traceable local delivery plan with estimates, buffers, capacity and predecessor constraints; not remote ticket publication or a proven scheduler."
license: Apache-2.0
metadata:
  version: "1.1.0"
  profile: "local-task-toolkit"
  invocation: "task-specific"
  integration-status: "portable-instructions-host-untested"
---

# TPM plan

## Scope

Read `references/local-execution-contract.md` and `references/tpm-integration-rules.md` at task start. Work only from local files and supplied context. Produce drafts, not external communications, automatic implementation or persistent modes.

## Workflow

1. Read the charter or stated goal, local requirements, existing estimates and supplied team availability. Follow the scheduling safeguards.
2. Produce requirements.md with originals retained, outline-numbered refinements, nonfunctional needs and use cases tracing to goal/requirement IDs.
3. Produce tasks.md with story/use-case links, estimate units, what is included, estimator/source, familiarity, confidence, ambiguity and concurrent code ownership. Mark applicable review/test/security/deploy/launch obligations as planned work only.
4. Produce buffer-matrix.md with measured versus assumed overhead, confidence and explicit unavailability. Do not invent a numerical default if no single source default is specified; record the missing parameter.
5. Use work-tracking to create or update work-graph.json with stable work IDs, goal/requirement/use-case traceability, explicit contracts, sourced estimates, and separate hierarchy/dependency/schedule relationships. Run its validate and analyze commands; retain the actual results.
6. Produce wbs.md as a view of those same IDs with typed schedule constraints/lags, feasible crash counts, resources, milestones, actuals and program dependencies. Leave absent estimates, dates and resources open. Use graph-engineering-skill for nontrivial runtime/routing analysis and to-tickets only for a requested slice handoff; do not create a second backlog.
7. Check requirement-to-use-case-to-task coverage, schedule units, no double-counted overhead and no unsupported headcount speedup. Report the computed dependency sequence separately from any resource-validated forecast.

## Reference and template map

| Bundled file | Read or use when |
|---|---|
| `references/planning.md` | before decomposing requirements and assembling a plan |
| `references/tpm-common/program-vs-project.md` | for program-level project boundaries |
| `references/tpm-common/clarity.md` | for final traceability and assumptions checks |
| `assets/requirements.md` | copy for requirement refinement and use cases |
| `assets/tasks.md` | copy for the estimate-source/task breakdown |
| `assets/buffer-matrix.md` | copy for assumptions, overhead and buffer convention |
| `assets/wbs.md` | copy for the local schedule/actuals/constraint record |

## Default output

Canonical work-graph.json plus four local plan views, actual validation/frontier results, traceability check, assumptions, estimate provenance and forecast limitations.

## Failure boundary

Keep missing estimates, capacity, names, approvals and dates as explicit unknowns. Repair only the failing artifact within the shared bounds, then escalate unresolved decisions. A populated template is not evidence that work, notification, approval or delivery occurred.

## Conditional skill dependencies

- `work-tracking`: read its installed sibling hub when assembling canonical tasks, dependencies, WBS views or tracker exports.
- `to-tickets`: read its installed sibling hub only for the named stage or discipline selected by this workflow.
- `graph-engineering-skill`: read its installed sibling hub only for the named stage or discipline selected by this workflow.

Install the declared closure from manifest.json. These are conditional workflow/resource availability requirements, not evidence that every stage must run serially.

## Provenance and changes

Adapted from [BittahCriminal/tpm-plugin](https://github.com/BittahCriminal/tpm-plugin/blob/cb7d3efabc807136e17d5146184f1e95ddbee5a4/skills/tpm-plan/SKILL.md) at `cb7d3efabc807136e17d5146184f1e95ddbee5a4`. The original Apache-2.0 license is included. `references/ORIGINAL-SKILL.md` preserves the original hub for provenance comparisons only; its sibling/plugin syntax does not override this portable hub. Changes: local-only task scope, explicit resource paths, honest unknowns, dependency-aware routing, schedule safeguards and no network refresh. Native host behavior remains untested.
