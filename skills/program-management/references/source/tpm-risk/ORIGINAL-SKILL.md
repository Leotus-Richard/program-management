> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: tpm-risk
description: "Create a local risk register with separate probability/impact scores, strategy order, signals and owners; not an issue triage or automatic mitigation action."
license: Apache-2.0
metadata:
  version: "1.1.0"
  profile: "local-task-toolkit"
  invocation: "task-specific"
  integration-status: "portable-instructions-host-untested"
---

# TPM risk

## Scope

Read `references/local-execution-contract.md` and `references/tpm-integration-rules.md` at task start. Work only from local files and supplied context. Produce drafts, not external communications, automatic implementation or persistent modes.

## Workflow

1. Inspect the local charter, requirements, plan and supplied team/stakeholder input. Risk discovery can start before a full schedule if threatened work is known.
2. Distinguish potential risks from active issues. Name the threatened task/dependency/phase and downstream effect for each risk.
3. Score ordinal probability and impact separately as 1, 2 or 3; use P+I=2..6 and flag 5..6 for close tracking. Record scoring as judgment unless data supports it.
4. List applicable avoid, mitigate, transfer and accept strategies in proposed order, current strategy, early signal, owner and project/program visibility.
5. Create deep-dive proposals for unscorable risks. Record the plan impact; change a local WBS only when the current task authorizes that edit, otherwise propose the delta.
6. Sweep lifecycle and cross-project risk categories, then run clarity checks. Write risk-register.md with realised/closed risks separated.

## Reference and template map

| Bundled file | Read or use when |
|---|---|
| `references/risk.md` | before identifying and scoring risks |
| `references/tpm-common/clarity.md` | for final traceability and ownership checks |
| `assets/risk-register.md` | copy and fill the local register |

## Default output

For risks or active issues affecting tracked work, use work-tracking to reference impacted canonical IDs. Create follow-up work once in the shared graph, with explicit contracts; render register links from those IDs. A risk association is not a blocker unless the downstream work actually needs its data or authority.

Local risk register, score-band counts, high-score risks, proposed plan deltas and uncertainty/ownership gaps.

## Failure boundary

Keep missing estimates, capacity, names, approvals and dates as explicit unknowns. Repair only the failing artifact within the shared bounds, then escalate unresolved decisions. A populated template is not evidence that work, notification, approval or delivery occurred.

## Conditional skill dependencies

- `work-tracking`: read its installed sibling hub when linking risks/issues to work or creating accepted mitigation tasks.

## Provenance and changes

Adapted from [BittahCriminal/tpm-plugin](https://github.com/BittahCriminal/tpm-plugin/blob/cb7d3efabc807136e17d5146184f1e95ddbee5a4/skills/tpm-risk/SKILL.md) at `cb7d3efabc807136e17d5146184f1e95ddbee5a4`. The original Apache-2.0 license is included. `references/ORIGINAL-SKILL.md` preserves the original hub for provenance comparisons only; its sibling/plugin syntax does not override this portable hub. Changes: local-only task scope, explicit resource paths, honest unknowns, dependency-aware routing, schedule safeguards and no network refresh. Native host behavior remains untested.
