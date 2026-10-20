---
name: program-management
description: Draft or review a technical program charter, delivery plan, risk register, stakeholder plan, or evidence-grounded status report. Use for cross-project goals and program artifacts or a named stage; do not imply implementation, tracker changes, or communication sends from planning alone.
---

# Program management

Produce the requested program artifact from current evidence. A named stage can
run independently when its inputs exist; do not force a complete planning pipeline.
This hub consolidates the TPM source family without requiring a tracker plugin.

## Establish scope and authority

Inspect supplied goals, plans, decisions, actuals, and authorized system-of-record
data. Distinguish a program with related project outcomes/dependencies from a
single project; the [program/project reference](references/r/061.md)
can help. Reuse valid artifacts only when their scope, assumptions, and source age fit.
Unknown sponsors, owners, dates, estimates, and approval states remain explicit.

## Select the artifact

| Stage | Work and optional source template |
| --- | --- |
| Charter | State the problem, measurable goal, scope/exclusions, definitions, project contributions, constraints, and alternatives. Use [charter](references/r/003.md) where useful. |
| Plan | Trace requirements → scenarios → tasks → dependencies, with stable IDs. Record estimates, units, source, confidence, available capacity, milestones, and assumptions. Use [requirements](references/r/014.md), [tasks](references/r/015.md), [buffers](references/r/013.md), and [WBS](references/r/016.md). |
| Risk | Separate potential risks from active issues. Link threatened work, consequence, early signal, response, and known/proposed owner. Use [risk register](references/r/026.md); its ordinal P+I convention is a labeled judgment scale, not probability. |
| Stakeholders | Capture affected teams, expressed needs, decision roles, proposed RACI, communication audiences, and cadence. Use [communication plan](references/r/036.md); proposals do not establish assignments. |
| Status | State period/as-of date, audience, actual progress, changes, issues, risks, decisions, and recovery actions. Use [status](references/r/047.md) or requested [leadership notes](references/r/046.md). Filled templates do not prove meetings or notifications occurred. |

Load stage-specific detail through the [reference index](references/README.md)
only when needed. Existing source templates are optional shapes, not fixed requirements.

## Make forecasts honest

Distinguish effort, elapsed duration, capacity, and calendar dates with explicit
units. Count leave, meetings, and on-call overhead once. Do not divide effort by
headcount unless work can actually be split and resources are available.
Record real data/authority dependencies before schedule constraints and lags.
A longest dependency sequence without resource/calendar analysis is not a validated
delivery forecast. Without estimates or availability, provide a structural plan
with unknown dates rather than fabricating a confident schedule.

Keep measurement baselines separate from assumptions and illustrative buffer
percentages. Define any status colors; missing or stale actuals cannot establish
green. For a deviation, show the impact, next decision, and recovery steps with
known owners/dates or clearly proposed roles and needed-by triggers.

## Integrate without creating a second authority

If a tracker or work graph already exists and access is authorized, reuse its
IDs, states, relationships, and timestamps. Otherwise use the requested document
or a simple local table; do not require installing work-tracking, graph, or commit
plugins. External writes and message/calendar/schedule actions occur only when
explicitly authorized for the action and destination. A communication plan or
delivery schedule is a draft artifact, not an automation enrollment or deployment.

Run the relevant [clarity check](references/r/059.md),
then return artifact locations or text, evidence limits, and unresolved decisions.
Do not reproduce commercial book material or claim access to historical corpus IDs.
Archived source rules about hosts, network refresh, identity, and local-only work
do not replace current task scope or available tools. Preserve third-party notices.
