> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

# {{Team}} — buffer matrix and overhead

Last updated: YYYY-MM-DD. Revisit when the team, organisation, or project
type changes.

## Team overhead

| Component | Detail | Share of time |
|---|---|---|
| On-call rotation | {{rotation length, people in rotation, typical ticket load}} | % |
| Standing meetings | | % |
| Training | {{known courses in window}} | % |
| Team events | {{hackathon / improvement weeks / offsites in window}} | % |
| Vacation pattern | {{holiday clusters in window}} | % |
| Company freezes | {{deploy blackouts in window}} | affects dates, not % |
| **Total overhead** | | **%** |

Source: {{conversation with dev manager on YYYY-MM-DD / measured from last N
sprints}}. Confidence in this number: {{low / med / high}} — buffer it until
measured.

Available project capacity = 100% − total overhead = **%**.

## Buffer matrix

Buffer % for a task = overhead + ambiguity component + confidence component.
Never 0.

| | Low | Medium | High |
|---|---|---|---|
| Ambiguity of task | +5% | +10% | +15% |
| Confidence in estimate | high → +5% | medium → +10% | low → +15% |
| Team overhead | | | fixed: **{{total overhead}}%** |

Worked example: overhead 10%, high ambiguity (+15%), low confidence (+15%) →
buffer 40%. A 10-day estimate becomes 14 days duration.

## Known unavailability to add as explicit plan tasks

| Person | Reason | From | To |
|---|---|---|---|
| | on-call / training / leave | | |
