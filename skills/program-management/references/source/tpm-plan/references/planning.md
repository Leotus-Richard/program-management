> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

# Plan management

A plan exists so the team spends its time on *how*, not on *what* and *when*.
Clarity in the requirements is cheaper than correcting bad estimates later.

The plan is built in four steps. Each step's output traces back to the
previous one.

```
requirements → use cases → tasks with estimates → project plan (with buffers,
predecessors, crash counts, dates)
```

## Step 1 — Requirements gathering and refinement

Take the raw requirements and probe each one:

- **Vague nouns and adjectives.** "Messaging-like UX" — which product? "Text"
  — plain or rich, which formatting, which character sets?
- **Missing constraints.** A "P2P system" may or may not permit relay servers;
  if the goal is no central overhead, say so.
- **Compound requirements.** One line asking for several features breaks
  traceability. Split it.
- **Implementation posing as requirement.** Keep the need; drop the prescribed
  solution.

Number the result with **outline numbering**: original requirements keep
their ordinal (1, 2, 3), refinements become sub-requirements (2.1, 2.2). The
originals stay visible so a stakeholder can see what changed.

Do not do this in a closed room. Different stakeholders see different gaps.

## Step 2 — Use cases

A use case tells a story about something a user can do and traces to the
requirements it satisfies:

> As a {{user / admin / operator}}, I can {{action}} so that {{outcome}}.

- One use case may cover several requirements; a use case that traces to a
  top-level requirement covers its sub-requirements too.
- Order by the story, not by requirement number; traceability is what
  guarantees coverage, not order.
- Group under themes (profiles, capabilities, operations) when the list is
  long.
- Each use case is also a test-plan item.

## Step 3 — Tasks with estimates

Break each use case into tasks. The level of breakdown depends on the team;
a task may be as coarse as "design and implement X" or as fine as "define the
key-value shape of the presence object". Note where you have prescribed a
design choice and where you have deliberately left it open.

Group tasks into **stories** (top-level items, outline-numbered: story 1,
tasks 1.1, 1.2). Stories usually map to use cases and become the **feature
list** later.

**Estimates come from the people who will do the work.** A developer's
estimate assumes ideal conditions and often includes only the coding. Ask:

- What does the estimate include — design, code review, testing, deployment?
- How familiar are you with this area?
- How confident are you (low / medium / high)?
- Anything new here — a technology, a framework, a team you have not worked
  with?
- Is anyone else changing these packages in the same window?

Put those questions in the task template so they stop feeling like
interrogation. Be explicit that the buffer you add is to protect the
developer's date, not to question their skill.

A task is not done when the code is written. It is done when it is written,
reviewed, and running in production and verified. Know the team's **time to
production** and budget for it.

## Step 4 — Assemble the plan

Fields every plan row needs:

| Field | Why |
|---|---|
| ID (outline) | Story/task grouping and traceability |
| Task | |
| Requirement(s) satisfied | Traceability back to step 1 |
| Estimate (effort) | From the team, before buffer |
| Buffer % | From the buffer matrix below |
| Duration | Estimate × (1 + buffer) |
| Predecessor(s) and type | fs (finish→start, the default), ss, ff, sf; note lags where implementation can start on a partial design (fast-tracking) |
| Crash count | Maximum people who can work it in parallel. Most granular tasks: 1. Multi-package implementation: 2+. Ask the dev manager |
| Resources | Planned people |
| Start / end | Calendar dates. Duration ÷ resources, adjusted for overhead and unavailability |
| Actuals | Actual start, actual end, actual resourcing — filled in during execution |

Recording crash count and fast-track opportunities *before* they are needed is
what lets you react in minutes when a priority cycle changes your headcount.

## Buffers

No estimate is right. Buffers protect the plan from reality. One way to size
them consistently is a matrix that adds three components:

| Component | Low | Medium | High |
|---|---|---|---|
| Team overhead | the team's measured overhead; 10% is modest, 30–40% is common | | |
| Ambiguity of the task | +5% | +10% | +15% |
| Confidence in the estimate | high: +5% | medium: +10% | low: +15% |

Buffer % = overhead + ambiguity + (inverse of) confidence. It is never 0.
Tune the percentages per team and revisit them whenever the team or
organisation changes.

Alternatives, for context:

- **PERT** — three estimates per task (optimistic, most likely, pessimistic),
  weighted average. Rigorous, but asking for three numbers per task gets
  tedious.
- **Critical chain** — buffers only on the critical path, on the argument
  that per-task padding gets consumed anyway (work expands to fill it). Worth
  knowing; whether it beats per-task buffers depends on the team's culture.

Whichever you use, **track buffer consumption** during implementation and
rebase the plan as it is eaten. Rebasing shows the trajectory; it does not
automatically move the dates.

## Team overhead — what to count

Tech teams do not get 100% of their hours for project work. Overhead of
10–40% is typical, made of:

- **On-call rotations** — usually a week at a time; the developer is
  effectively unavailable. Worse than vacation because it rotates, hits
  multiple people, and people forget it is coming. Ask for the rotation
  schedule and either add it as a task or as a buffer.
- **Training** — bursts when a popular course runs.
- **Team events** — hackathons, improvement weeks, offsites.
- **Company-wide freezes** — deployment blackouts around reliability events,
  sales events, launches.
- **Standing meetings.**
- **Vacation patterns** — holidays padded into long weekends.

A ten-minute conversation with the dev manager walking down this list gives a
usable overhead number. Treat it as an estimate and buffer it until you have
data. If overhead is "wishful thinking", the plan will reveal it — use that as
a process-improvement signal.

Prefer adding known unavailability (an on-call week) as an explicit task in the
plan over hiding it in a resourcing tool: it explains the gap in the Gantt.

## Capacity-constrained prioritisation

Tech companies rarely fund a project and leave it alone. They run
prioritisation cycles (monthly, quarterly, yearly) and re-allocate existing
capacity to the most strategic work. Your headcount can go up or down
mid-project. Plan for it:

- Front-load crash counts, buffers, and predecessor types so you can re-plan
  fast.
- When asked "what dates can you hit with N people?", answer from the plan by
  moving tasks, not from instinct. Keep a Gantt-style view you can manipulate.
- Most tools do not model crashing (adding people shortens calendar time);
  they spread hours and keep duration. Expect to adjust durations by hand.

## Milestones and feature list

- **Milestones** — phases every project passes through: design complete,
  implementation complete, UAT complete, launch. Same across projects, so
  they let you compare project health across a program.
- **Feature list** — the project-specific deliverables that can ship
  independently; usually the top-level stories in the plan. This is what
  stakeholders mean when they say "milestone" in conversation.

List the feature list separately from the plan: it is the concise snapshot
most stakeholders want, and it feeds the status report.

## When planning has to be quick

Reduce repeated work:

- **Repeatable estimates** — keep a list of tasks that recur across projects
  (config, data modelling, a new type from an abstract base) with a range
  estimate. Use the top of the range when the instance looks harder.
- **Management checklist** — the recurring management actions per area
  (review requirements, build use cases, analyse risks, build comms plan) as a
  checklist you run down.
- **Plan templates** — always-present tasks (requirements verification,
  functional spec, deployment, integration test, end-to-end test, launch
  plan) pre-populated.
- **Buffer matrix** — apply it mechanically.

## Program-level planning

The same steps apply, one level up: refine the program *goals* the way you
refine project requirements, cut the goals into projects along impact and
shared-work lines (see `../../tpm/references/program-vs-project.md`), and
plan each project. What is new is **cross-project dependencies** — a shared
subsystem, interoperability testing between projects — which need explicit
tracking and are the first place to look for both efficiencies (shared code)
and risk (one delay cascades).

## Clarity questions for this artifact

- Is every requirement single, testable, and traceable to a goal?
- Does every use case trace to requirements, and every task to a use case?
- For every estimate: what is included, how familiar, how confident, anything
  new, anyone else in the same code?
- Is the team's overhead a measured number or a guess? Is on-call in it?
- Which tasks can be crashed? Which can be fast-tracked?
- What are the always-present tasks (deploy, integration test, security
  review) and are they in the plan?
- What crosses project boundaries?
