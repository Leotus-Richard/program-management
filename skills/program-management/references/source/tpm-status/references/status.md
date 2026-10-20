> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

# Status reporting

A status report is a health check at a moment in time with a projection of
where things are going. It is the most-read artifact you produce, and it is
how stakeholders form their perception of whether you are in control —
regardless of whether you actually are. Written, slides, or verbal: same
content, same rules.

## Decide the narrative first

Before filling the template, decide what this report needs to convey in one
sentence. That choice determines what goes above the fold and what gets cut.

## Audience sets the altitude

| Audience | Report | Altitude | Wants to know |
|---|---|---|---|
| Development team, active stakeholders | Weekly status | Street | Sprint progress, burndown, blockers, high-score risks, open issues |
| Leadership with resourcing, upper management | Leadership review (monthly) | Neighbourhood | Milestone status, milestone-impacting issues, business value, highlights / lowlights / learnings, metrics |
| Senior leadership, sponsor | Senior leadership review (quarterly) | City | Is the goal on track, ROI, major wins and misses since last time, metrics |

Same project, three different documents. Each is built from the one below
it. Never send the street-level report to the city-level audience.

## Above the fold

The top of the report is the only part guaranteed to be read. It must be
self-sufficient:

1. **Status colour** and the target date it refers to
2. **Executive summary** — where the project is, in plain sentences
3. **Path to green** (if not green) — actions, owners, dates
4. **Next status date** (repeat here during critical phases)

Then, below the fold: milestones, feature deliverables, open and recently
resolved issues, risk log (high-score items; link to the full log), burndown
or progress chart. At the bottom: project description, contacts,
communication schedule, glossary.

## Define the traffic light, and stick to it

Definitions differ across companies and cultures. State yours in every
report.

| Colour | Definition |
|---|---|
| **Green** | Meeting current milestones and deliverables; on track for the scheduled date with the agreed resourcing and scope |
| **Yellow** | Active issues *may* affect the date. Not certain to miss it, but something must change to stay on track. The path back is understood. Ideally short-lived — it should rarely be a surprise, because the risk log anticipated it |
| **Red** | With current resourcing, scope, and work as defined, the date *will* be missed. Something must change. There is no ambiguity about that |

Notes on the edges:

- A risk that was realised and successfully handled without affecting the
  date does not change the colour.
- An issue whose impact is not yet understood is yellow, not red — red
  claims more certainty than you have. Give a date for when the impact will
  be known, and define the point of no return at which it flips to red
  regardless.
- Bias to transparency. A "watermelon" (green outside, red inside) costs
  more trust than an honest yellow.

## Rules that make a status report good

1. **Every action has an owner and a date.** If the date is not known, give
   a **date for a date** — when the concrete plan will exist.
2. **A non-green status has a path to green.** The set of actions, each
   with owner and date, that return the project to green. For yellow it is
   usually concrete. For red it is often exploratory — first understand
   impact, then choose between more resources, less scope, re-sequenced
   milestones, or a moved date (which external commitments may forbid).
3. **Important details above the fold.**
4. **Consistent format.** Agree the format with your stakeholders up front;
   the less effort it takes to read, the more it gets read instead of
   generating meetings. Format for easy refresh of the recurring tables.
5. **Consistent timing.** Same day, every time. See the communication plan.
6. **Pre-communicate.** Nobody named in an issue learns about it from the
   report.
7. **Grammar and clarity matter** — enough that a reader never has to guess.

## Contents inventory

| Section | Weekly status | LR | SLR |
|---|---|---|---|
| Metrics ("page 0") | — | top | top |
| Status colour + target date | ✓ | ✓ | ✓ |
| Executive summary | ✓ | ✓ | ✓ |
| Path to green | ✓ | ✓ | ✓ |
| Milestones (phases: design / implementation / UAT / launch) | ✓ | ✓ | summary |
| Feature deliverables (top-level stories) | ✓ | ✓ | summary |
| Open and recently resolved issues | ✓ | milestone-impacting only | — |
| Risk log | high-score | high-score | goal-threatening only |
| Burndown / progress chart | ✓ | optional | — |
| Highlights / lowlights / learnings | — | ✓ | ✓ |
| Decisions needed from this audience | if any | ✓ | ✓ |
| Project description | ✓ | ✓ | ✓ |
| Contacts | ✓ | ✓ | ✓ |
| Communication schedule / next report | ✓ | ✓ | ✓ |
| Glossary | ✓ | ✓ | ✓ |

Move resolved issues to a separate table after they have appeared once as
resolved, so the live table stays short.

## Program-level reports

The program status collates project statuses (published first). Program
metrics and cross-project risks come to the top; project detail drops to
what affects delivery dates or crosses boundaries. One combined report can
suffice when projects are tightly related and have no interdependencies;
separate reports when organisations or complexity differ.

## Clarity questions for this artifact

- Who is the audience, and what altitude do they need?
- What is the one-sentence narrative?
- Is the colour justified by the definition, not by politics?
- Does every action — including the path to green — have an owner and a
  date (or a date for a date)?
- Has everyone named in an issue been told already?
- Could the reader stop at the fold and still know the state of the project?
- When is the next report, and is that date in the communication plan?
