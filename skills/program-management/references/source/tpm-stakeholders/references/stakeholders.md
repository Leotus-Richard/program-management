> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

# Stakeholder management

Stakeholder management is managing expectations. Each stakeholder wants
something different from the project; the communication plan is how you meet
all of those needs on a schedule people can rely on. Stakeholders are also
your best source of information when requirements or solutions are ambiguous
— treat them as partners, not as a distribution list.

A communication plan has three parts, built in this order:

1. **Communication types** — mostly static, reused across projects.
2. **Stakeholder list** — specific to this project; revisited constantly.
3. **Roles and responsibilities (RACI)** — by role, mostly static.

## 1. Communication types

Each type serves an audience at a different altitude. Each one builds on the
one below it.

| Type | Audience | Cadence | Content | Owner |
|---|---|---|---|---|
| **Stand-up** | Development team | Daily / per sprint norms | What was done, what is next, blockers | Scrum master or lead dev — *not* the TPM (attend to unblock; do not run it beyond a short transition) |
| **Status update** | People actively working on the project: devs, managers, product, vendors | Weekly or bi-weekly | Current and upcoming milestones/features, blockers, high-score risks, open issues. Technical. Street level | TPM, with input from all active stakeholders |
| **Leadership review (LR)** | Leadership with resourcing in the project, upper management | Monthly | Direction, major milestones, issues with milestone impact, business value delivered. Highlights, lowlights, learnings. Neighbourhood level | TPM (sometimes co-owned with dev manager or PM) |
| **Senior leadership review (SLR)** | Senior leadership, executive sponsor | Quarterly | The quarter's LRs distilled: end-goal trajectory, major steps, wins, misses, ROI. City level | Whoever owns the LR (TPM); a director may present it |
| **Leadership sync** (program) | Project TPMs / leads across the program | Weekly-ish | Round-robin per project: status, blockers, cross-project impacts; park new issues for after the round | Program TPM |
| **Kickoff** | All stakeholders | Once at start (and when a program forms mid-flight) | Goals, each person's role, the communication plan and its deliverables, first pass at risks and missing stakeholders | TPM |

Not every project needs every type. A small project may need only stand-up
and status; a program will usually use all of them. Some companies do reviews
verbally or in slides instead of written reports — the intent is the same.

**Metrics** live at LR and SLR level, not in weekly status: program metrics
do not move weekly, and if one does it is probably measuring the wrong
thing. Put the program's key metrics at the very top of the LR/SLR, before
the status.

### Timing

Sequence reports so each feeds the next without a scramble:

- Weekly status on a fixed mid-week day (avoid Mondays — holidays — and
  Fridays — nobody reads them).
- LR the day after a status in a fixed week of the month, so the freshest
  status folds into it.
- SLR replaces every third LR, same slot.
- In a program: every project's status is published *before* the program
  status; every project's LR before the program's LR.

Consistency is the point. A late or missed report reads as disorganisation
even when the reason is good, and it invites micromanagement.

### Pre-communication

Before any report names an issue involving a stakeholder, tell that
stakeholder first. They get to respond or prepare; the relationship stays
healthy; nobody is ambushed in front of leadership. A reviewed report should
never be the first time someone hears about their own problem. Likewise, an
LR or SLR is not where blockers get raised — those are resolved when they
happen; the review only records them.

## 2. Stakeholder list

Anyone impacted by the project, however far down the chain, is a
stakeholder. Finding them is cyclical, not a one-time step:

- Requirements refinement reveals service owners and their clients.
- Each stakeholder you talk to knows others you have not.
- Low-level design surfaces teams you did not know were affected.
- People join and leave; someone new represents a vacated seat.
- In your first 90 days somewhere: ask your manager for the need-to-know
  list, meet each person, ask each who else matters.

For each stakeholder record: name, role, organisation, which project(s) in
the program they touch, and which communication types they receive.
Communication levels are inclusive downward — the dev team sees how the
project is represented upward.

Look for **subject-matter experts** hiding in the list: a networking
specialist in one project may unblock a risk in another. Cross-project
co-op groups form from exactly this.

Note the **channel** each stakeholder actually uses (chat tool, ticket
system, email); pick one per purpose and say so in the plan. Check tool
permissions — both that stakeholders can get in and that non-stakeholders
cannot.

Meet non-technical stakeholders where they are: know their technical
proficiency and business acumen before drafting for them. Re-articulating a
problem for a different audience usually sharpens your own understanding of
it.

## 3. Roles and responsibilities (RACI)

For each recurring activity, who is:

- **R — Responsible**: delivers it (may have contributors).
- **A — Accountable**: answers for it if it does not happen. One per row.
- **C — Consulted**: contributes input (devs in sprint planning; business in
  requirement clarification). "Participated" can mark an SME.
- **I — Informed**: told the outcome, via status or meeting.
- **(C)/(I)** — optional; never leave a cell blank.

The TPM is typically R and A for the project plan and the status report; A
for milestones while developers are R; C for sprint planning when a service
team runs its own sprint. At program level: program TPM A for every project's
status report while project TPMs are R; program TPM R+A for the SLR with
project TPMs C.

Discuss the RACI with the team every project. Do not assume roles carry over
from the last project — the overlap between TPM and dev manager shifts with
the project's shape.

## Program level

Scale, not kind: more stakeholders, more concurrent communication plans (one
stand-up and status per project), the program TPM accountable for all of
them. Add the leadership sync and expect the SLR to matter. Delegate
project-level issues to project TPMs; step in when a risk crosses projects or
is close to realised — to speed communication, not to take control.

## Clarity questions for this artifact

- Who is impacted, all the way down the chain? Who have we not asked?
- What role does each play: decides, delivers, consulted, informed?
- Which communication type does each receive?
- Which SMEs are in the list, and which risks could they help with?
- Which channel does each audience actually read?
- On which day/week does each report go out, and does the sequence let each
  one feed the next?
- Who is A for each activity? Is any cell blank?
