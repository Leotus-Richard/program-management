> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

# Driving toward clarity

The one habit every TPM workflow in this plugin runs on. It is not a step; it is
applied at every step: take an ambiguous input, decompose it, ask the questions
that expose hidden assumptions, and leave behind an artifact that someone else
can follow without you in the room.

## The loop

```
ambiguous input → decompose → question each piece → record the answer or the
open question → produce a traceable artifact → new information arrives → repeat
```

Three things make an artifact "clear":

1. **Traceable** — every task traces to a use case, every use case to a
   requirement, every requirement to a goal. Every risk names the task or
   dependency it threatens. Every action has an owner and a date.
2. **Assumption-free** — an assumption that was not written down is a future
   surprise. Write assumptions as assumptions, not as facts.
3. **Open questions are visible** — an unanswered question stays in an "Open
   questions" list until it is answered. It is never silently resolved by
   picking a default.

## Where ambiguity hides

| Where | What it looks like | What to do |
|---|---|---|
| Goal wording | "100% reach", "fast", "secure", "all users" | Ask what is measured and how; probe two or three words at a time |
| Compound requirements | One line asking for several features | Split into numbered sub-requirements (1.1, 1.2 …) so each can be traced |
| Vague nouns | "text", "messaging-like UX", "the platform" | Ask for the reference: plain or rich text? which product's UX? which platform version? |
| Implementation posing as requirement | "use framework X", "store it in table Y" | Ask what the underlying need is; keep the need, drop the prescribed solution |
| Derived requirements | Scaling, latency, refactoring the team adds later | Ask the team up front what non-functional work the change forces |
| Estimates | A single number | Ask what it includes (design? review? test? deploy?), the developer's familiarity with the area, and their confidence |
| Risks | "testing might slip" | Ask which test, why, by how much, and what it blocks downstream |
| Stakeholders | "the business", "leadership" | Ask for names, roles, and which decisions each one actually makes |

## Question banks by area

Ask these before producing the artifact. Record answers; carry unanswered ones
into the artifact's **Open questions** section.

### Goal and charter

- What problem does this solve, and for whom? What happens if it is not done?
- What is the business case in one sentence?
- What does "done" look like? What is measured to prove it?
- Is the goal specific enough to plan against, but loose enough to survive new
  information? Which words in it are doing the most work?
- What is explicitly out of scope?

### Requirements

- Is each requirement a single testable statement?
- What reference or example resolves each vague adjective?
- Which requirements are really implementation choices? What is the need
  behind them?
- What non-functional work (scale, latency, security review, migration) does
  this force on the team?
- Who else has a perspective on these requirements who has not been asked?

### Plan and estimates

- What is included in this estimate: design, code, review, test, deploy?
- How familiar is the estimator with this area of the code?
- How confident are they? Low / medium / high.
- Are there unknown technologies or new frameworks in this task?
- Is anything else touching the same code packages during this window?
- What is the team's real overhead (on-call, training, meetings, vacation
  patterns)?
- Which tasks can be crashed (split across people)? Which can be fast-tracked
  (start before the predecessor finishes)?
- Is a task "done" when code is written, when it is reviewed, or when it is in
  production and verified?

### Risk

- Is this a risk (might happen) or an issue (already happening)?
- What exactly would occur, to which task or dependency, and what does it
  block downstream?
- What is the probability and the impact, scored separately?
- What signal would tell us it is materialising before it hits?
- Which strategies are available — avoid, mitigate, transfer, accept — and in
  what order would we try them?
- Does this risk belong to a project, or does it cross projects and belong at
  program level?

### Stakeholders and communication

- Who is impacted, however far down the chain?
- What role does each person play: decides, delivers, consults, or only needs
  to know?
- What does each audience actually want from an update? Day-to-day, direction
  and milestones, or end-goal trajectory?
- Has anyone named in a status issue been told before the report goes out?
- If the status is not green, what is the path back, who owns it, and by when?

## Closing clarity check

Run this once every artifact for a stage exists. Each line is pass/fail.

- [ ] Every plan task traces to a use case and a requirement.
- [ ] Every requirement traces to a goal in the charter.
- [ ] Every risk names the task, dependency, or phase it threatens.
- [ ] Every action item in every artifact has an owner and a date (or a date
      for a date).
- [ ] No assumption is written as a fact. Assumptions are listed as such.
- [ ] Every open question is in an Open questions section, not silently
      defaulted.
- [ ] The status report's audience is named and its content matches that
      audience's altitude.

Anything failing goes back to the sub-skill that owns that artifact.
