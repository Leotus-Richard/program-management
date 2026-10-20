> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: tpm-status
description: "Draft an evidence-linked local status report at team, leadership or sponsor altitude; not live monitoring, publication or fabricated green status."
license: Apache-2.0
metadata:
  version: "1.1.0"
  profile: "local-task-toolkit"
  invocation: "task-specific"
  integration-status: "portable-instructions-host-untested"
---

# TPM status

## Scope

Read `references/local-execution-contract.md` and `references/tpm-integration-rules.md` at task start. Work only from local files and supplied context. Produce drafts, not external communications, automatic implementation or persistent modes.

## Workflow

1. Determine audience, reporting period and as-of date from the request/evidence. When tracked work exists, use work-tracking to read the canonical graph, actual analyze output and supplied snapshot freshness; reuse those IDs/states/evidence in the report. Read risks, actuals and communication inputs. Do not maintain separate report-only work states.
2. Write one plain-language narrative. Define traffic lights in the report and justify the chosen assessment with actual evidence; if impact or actuals are unknown, label the provisional assessment and missing data explicitly.
3. For non-green status, record path-to-green actions with known/proposed owners and dates or explicit dates-for-decisions/triggers. Do not fabricate commitments.
4. Choose sections at the audience altitude: working detail for the team, milestone/value/metrics for leadership, goal trajectory for sponsors. Include high-score/goal-threatening risks appropriately and separate active/resolved issues.
5. Use leadership-sync.md only when those notes are requested. Do not claim a meeting occurred from a filled template.
6. Run the clarity checks and list the people requiring pre-communication, distinguishing confirmed notification from pending human action. Save the local dated draft; never send it.

## Reference and template map

| Bundled file | Read or use when |
|---|---|
| `references/status.md` | before selecting audience sections and status definitions |
| `references/tpm-common/clarity.md` | for final completeness and uncertainty checks |
| `assets/status-report.md` | copy for a weekly, leadership or senior-leadership draft |
| `assets/leadership-sync.md` | copy only for requested program leadership-sync notes |

## Default output

Audience-specific local report/sync draft, evidenced status, proposed recovery actions and freshness/notification gaps.

## Failure boundary

Keep missing estimates, capacity, names, approvals and dates as explicit unknowns. Repair only the failing artifact within the shared bounds, then escalate unresolved decisions. A populated template is not evidence that work, notification, approval or delivery occurred.

## Conditional skill dependencies

- `work-tracking`: read its installed sibling hub when reporting canonical work state, blockers, evidence or tracker snapshot freshness.

## Provenance and changes

Adapted from [BittahCriminal/tpm-plugin](https://github.com/BittahCriminal/tpm-plugin/blob/cb7d3efabc807136e17d5146184f1e95ddbee5a4/skills/tpm-status/SKILL.md) at `cb7d3efabc807136e17d5146184f1e95ddbee5a4`. The original Apache-2.0 license is included. `references/ORIGINAL-SKILL.md` preserves the original hub for provenance comparisons only; its sibling/plugin syntax does not override this portable hub. Changes: local-only task scope, explicit resource paths, honest unknowns, dependency-aware routing, schedule safeguards and no network refresh. Native host behavior remains untested.
