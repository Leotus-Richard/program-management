> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

# Program or project?

A **project** delivers a bounded set of requirements toward one goal. A
**program** is a set of projects that together achieve one or more shared
goals; it exists to keep those projects aligned and to manage what crosses
their boundaries. Same key management areas — plan, risk, stakeholders — but at
program level the unit of concern shifts from *tasks* to *projects*.

## Two ideas that define a program

- **Scope** — the set of requirements satisfied when the goals are met. In a
  program the scope is split into smaller goals, each owned by a project. No
  single project holds the whole scope.
- **Impact** — every stakeholder and system affected by achieving the goals,
  including clients of the systems that change. Impact is what usually forces
  a program: when the people affected do not overlap, the work wants separate
  projects.

## Litmus test

Answering "yes" to any of these leans toward a program. None is decisive on
its own.

| Question | Leans toward a program when… |
|---|---|
| Are there multiple end goals (not features or milestones — goals)? | Yes: one project per goal, a program over them |
| Is the timeline fixed, or driven by achieving the goals? | Goal-driven, open-ended |
| How many organisations own a slice of the work? | More than one, each with a distinct deliverable |
| Do the stakeholders for different slices overlap? | Rarely — separate stakeholder sets |
| Is there shared work (a subsystem, a library) that several slices depend on? | Yes — it wants its own project and creates cross-project dependencies |

Counter-example: a regulatory change spanning two departments with a hard
deadline and concrete deliverables is usually still one project.

## Drawing boundaries

- **Project boundary** = its goal and the requirements it delivers. Inside it,
  milestones (phases every project has: design done, implementation done, UAT
  done, launch) and features (deliverable groups of requirements) mark
  progress.
- **Program boundary** = the shared goals. Each project is, at program level,
  a "feature" of the program.
- Cut along **impact cues**: where the affected stakeholders change, a project
  boundary usually belongs. Cut along **shared work**: anything several
  projects need becomes its own project, which removes duplication but adds a
  dependency every consumer now carries.

## Two ways a program is born

1. **From requirements, up front.** Clarify the requirements, group them into
   deliverable chunks, notice where scope and impact diverge, and create one
   project per chunk. If that yields more than one project, a program is
   needed.
2. **Mid-execution, from projects already in flight.** Several independent
   projects turn out to share an end state. Combine their requirements and
   look for the common goal; the program formalises it, exposes gaps
   (including unfunded work that the end state needs), and can span projects
   that also belong to other programs. Harder to see than case 1 because each
   project looks self-contained.

Write the program goal with room to adapt *how* it is achieved, but a clear
enough intent that projects can be measured against it.

## What changes at program level

| Area | Project | Program |
|---|---|---|
| Plan | Tasks, predecessors, buffers | Projects, cross-project dependencies, the composition of projects |
| Risk | Cross-task risks | Cross-project risks: shared subsystems, interoperability testing, API contract drift between projects. Project risks that threaten the program are *also* tracked at program level, still owned by the project |
| Stakeholders | One stand-up, one status report, one leadership review | One per project plus program-level; the program TPM is *accountable* for all of them even when project TPMs are *responsible* |
| Communication | Weekly status → leadership review | Add a leadership sync across project leads, and a senior leadership review; sequence project reports before the program report |
| Intervention | The TPM runs the project | The program TPM stays informed, delegates project issues, and steps in only when a risk crosses projects or is close to realised |

## Kickoff

Every program (and project) starts with a kickoff of all stakeholders: the
goals, each person's role, the communication plan and its expected
deliverables, and a first pass at risks and missing stakeholders. For a
program, the kickoff also shows each project lead how their project affects
the others.
