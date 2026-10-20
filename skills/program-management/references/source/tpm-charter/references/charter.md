> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

# Charter

A charter bounds a program or project and brings a newcomer up to speed in one
read. In tech companies it rarely carries formal authority (nobody is granted
hiring power by it), so its value is the three statements that answer *why*:

1. **Problem statement** — what is broken or missing, for whom.
2. **Business case** — why solving it is worth the investment now.
3. **Goal** — the end state, written so it can be measured.

Everything else in the charter is a pointer to where the detail lives.

## Writing the goal

The goal is the guiding principle every project is measured against. It should
be:

- **Specific enough to plan against.** "Reach 100% of the user base" needs a
  definition of *user base* and of *reach* before projects can be cut from it.
- **Loose enough to survive new information.** Prescribing *how* (which
  platforms, which framework) in the goal makes the goal wrong the moment the
  approach changes.
- **Refinable.** When execution shows the goal was too vague (for example, it
  hid a large customer-facing change), refine the wording with the
  stakeholders present rather than pausing the work. Narrow the *project*
  goal for the period, keep the *program* goal honest.

Probe the goal's load-bearing words. Two words ("user base", "no central
server") can hide months of work.

## Scope

- **In scope** — the requirements the goal covers, at the level of deliverable
  chunks (features for a project; projects for a program).
- **Out of scope** — what a reasonable reader might assume is included but is
  not. This is the main defence against scope creep.
- For a program: the **project structure** — which projects, each project's
  goal, how each contributes to the program goal, and the dependencies
  between them (none, shared subsystem, sequential).

## Roadmap

For a program, the roadmap is the end-to-end plan that achieves the charter's
goals: the projects, their boundaries, their interdependencies, and rough
timing. It is derived from the goal; different readings of the goal give
different roadmaps (for example, mobile-only versus all platforms versus
enterprise-only). Pick one, record why, and record the alternatives rejected.

## Metrics

The problem statement and business case usually name the metrics worth
tracking. Write them down here so the status reports have something to report
against. For a program these become the "page 0" metrics at the top of every
leadership review.

## Team and stakeholders

Name the owner (the TPM), the sponsor, and the key stakeholder groups. Full
stakeholder list and RACI live in the communication plan; the charter links to
them.

## Constraints

Timeline (fixed date, or goal-driven), budget or headcount, and any hard
external constraint (regulatory date, customer promise, platform release
window).

## Clarity questions for this artifact

- What problem, for whom, and what if we do nothing?
- What is the one-sentence business case?
- What is measured to declare the goal met?
- Which words in the goal need a definition before planning can start?
- What would a reader wrongly assume is in scope?
- Is this one project, or several projects needing a program? (See
  `../../tpm/references/program-vs-project.md`.)
- What alternatives to the chosen roadmap were considered, and why rejected?
