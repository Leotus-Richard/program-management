> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

# Risk management

A **risk** is something that *might* happen and would affect timeline, scope,
or resourcing. An **issue** is something that *is* happening. A realised risk
becomes an issue — and, if you did the work, one with a strategy already
attached. Do not treat the two as synonyms: a risk log full of active issues
means nothing was anticipated.

Risk assessment starts as soon as there is enough to assess — a paragraph of
goal in a familiar domain is enough; an unfamiliar or vague domain may need a
full requirements document first (and that need is itself a risk).

## The cycle

```
identify → analyse → plan (strategy + update the project plan) → track → document
                ↑                                                        │
                └────────────────── new information ─────────────────────┘
```

Every pass adds detail. The first pass finds the obvious risks; those uncover
more. It is continuous for the life of the project.

### 1. Identify

Sources, in order of cost:

- **The plan itself.** Look at the Gantt: parallel work that assumes nothing
  fails (ten integration tests in the same two weeks), a single task every
  other task waits on, tasks touching services with known deployment trouble.
- **The organisation's risk register** — risks from past projects, tagged by
  system, team, client, complexity. If none exists, start one; even a
  thematic list (networking, cross-platform, app-store approval) is a
  shortcut.
- **Stakeholders and the team.** A kickoff working session with everyone in
  the room is the highest-value hour in risk identification. People see the
  same plan from different experience; the team you forgot to talk to is the
  classic finding.
- **Your own technical read.** A requirement that forces a refactor in a
  package another project is also changing; a new architectural pattern for
  this team; a dependency on another organisation's change.

Break a coarse risk into sub-risks with outline numbering (1, 1.1, 1.2) the
same way you split a story into tasks. "Cross-platform tooling issues" is
three risks: new IDE, new language for some teams, cross-team coordination —
each with different probability and impact per project.

### 2. Analyse

Score **probability** and **impact** separately on a three-tier scale
(Low = 1, Medium = 2, High = 3). **Risk score = probability + impact**
(2–6). Three tiers because four or five invite arguing about High versus
Very High; summing two honest answers is harder to bias than picking a
single severity.

| Score | Attention |
|---|---|
| 2–3 | Log it; check it at review time |
| 4 | Watch it; strategy ready |
| 5–6 | Track closely; be ready to act now; report it above the fold |

Where a metric exists (deployment failure rate × tasks in that pipeline),
use it. Where it does not (attrition), say the score is a judgement.
Re-score when context changes — the same risk in a new project is not the
same risk.

If a risk is not understood well enough to score, add a **deep-dive task**
(proof of concept, spike, training) to the plan to understand it.

### 3. Plan — the four strategies

| Strategy | What it means | When |
|---|---|---|
| **Avoid** | Change the plan so the risk cannot occur (different vendor, training before the work, buffer in the schedule) | First choice whenever possible; often done unconsciously — log it anyway |
| **Mitigate** | Let it happen, reduce the impact (crash / swarm the remaining tasks, pre-built fallback) | Reactive; a middle path when probability is low or avoidance is too costly |
| **Transfer** | Move it to another party (contract a team that knows the framework) | When expertise exists elsewhere; note the risk usually survives at program level and a vendor dependency appears |
| **Accept** | Take the hit, adjust dates | When nothing else is available or costs more than the impact |

**List every strategy available for each risk, in the order you would try
them.** Strategies fall back on one another: avoid → if that fails, mitigate
→ if resourcing is not there, accept. The strategy in use changes over the
life of the risk. Being able to see all the options is a core TPM skill.

Then **update the project plan**: avoidance strategies usually mean new
tasks or moved dates; mitigation strategies mean recorded crash options.

### 4. Track

For each risk define a **signal** — something observable that shows it
materialising *before* it hits: pipeline deploys per day, merge lead time,
other projects' launch dates on the same pipeline, sprint velocity in the
new tooling. Watch it. Probability and impact drift; risks close; new ones
appear (a published vulnerability, a mandatory upgrade).

Any change to a risk's status, strategy, or score goes into the next status
update so nobody is surprised.

### 5. Document

Closed risks, realised risks, and what actually worked go into the
organisation's risk register at project close (or your own if there is none).
Memory does not scale; a written risk triggers the recollection when you
need it.

## Where risk lives in a software project

| Phase | Typical risks |
|---|---|
| Requirements | Ambiguity → scope creep in design and implementation |
| Design | Technical issues with requirements surface here; latency and availability targets add work; API and release strategy decisions |
| Implementation | Buffer consumed by overhead; "done" ≠ "in production" (time to production, pipeline congestion); security / InfoSec certification — treat like a vendor dependency, longer for new services |
| Testing | Unknown unknowns in edge cases; distributed systems with untestable state spaces; test framework maturity |
| Evaluation | Vague feedback becoming vague requirements for the next cycle |
| Cross-phase | On-call and unplanned leave shifting rotations; mandatory version upgrades; industry-wide vulnerabilities (all hands, no negotiation — buffer is the only defence) |

## Project versus program

The process is identical; the unit of analysis changes from **cross-task**
to **cross-project**:

- A shared subsystem removes duplication and creates a dependency for every
  consumer — one delay cascades to all.
- Interoperability testing between projects means one project's slip blocks
  every other project's tests. Options: reorder tests, or cut the slow
  project out of scope and launch it later.
- API contract drift between the shared piece and its consumers.

Program-level risks are owned by the program TPM. A project risk that
threatens the program is *also* tracked at program level — owner stays with
the project, visibility rises, and the program TPM watches closely. Track
program risks in a program-level log (or a "program project" in tooling).

## When it has to be quick

- Copy identification from the register; re-score for this context; reuse
  strategies where the risk is specific enough.
- Use thematic buckets or project-type tags if there is no searchable
  register.
- One working session with stakeholders: identify, analyse, plan strategies,
  update the plan, in a single pass.

Some risk capture is better than running blind.

## Clarity questions for this artifact

- Is this a risk or an issue?
- What exactly happens, to which task or dependency, and what does it block?
- Probability? Impact? Scored separately?
- What signal shows it coming?
- Which of avoid / mitigate / transfer / accept apply, and in what order?
- What does the plan need to change to reflect the chosen strategy?
- Is this a project risk, a program risk, or a project risk the program must
  also see?
- Who owns it?
