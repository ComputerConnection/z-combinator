---
name: sprint-retro
description: End-of-sprint retrospective for startups. Evaluates velocity vs plan, scope changes, technical debt (intentional vs accidental), runway consumed vs progress. Forces honest evaluation. Use at sprint end.
---

# Sprint Retrospective

At the end of each sprint (typically 1-2 weeks during build phase), run this. This isn't a feel-good session. It's brutal honesty about whether you're on track.

## What You Do

1. Read PLAN.md to understand sprint goals and timeline
2. Review git log for the sprint period — what actually shipped?
3. Read STANDUP-LOG.md to see planned vs actual
4. List all scope changes during sprint:
   - What got added? Why? Was it necessary or distraction?
   - What got removed? Why?
5. Evaluate technical debt taken:
   - **Intentional**: "We shipped auth quickly without full password recovery because deadline. Plan to fix week 5." ✓ This is smart.
   - **Accidental**: "Our database schema is a mess and queries are slow, but we didn't document this anywhere." ✗ This kills you.
6. Calculate the scariest metric: **Runway consumed vs progress made**
   - If you're in a 12-week sprint (or used 3 of 12), did you advance proportionally?
   - Example: "Week 3 of 12 (25% runway spent). You've completed 15% of must-have features. You're behind."
7. Ask the hard question: "Would I fund another sprint of this?" If no, what needs to change?

## Output: SPRINT-{N}-RETRO.md

Format:
```
# Sprint {N} Retrospective

## Dates
[Start] to [End]

## Sprint Goals
- [Goal 1]
- [Goal 2]
- [What was planned?]

## What Actually Shipped
- [Feature/task 1] - [estimated hours] / [actual hours]
- [Feature/task 2]
...

## Scope Changes During Sprint

### Added
- [What + why + impact on timeline]

### Removed
- [What + why]

## Technical Debt Audit

### Intentional
- [Debt item]: [Plan to fix by when]

### Accidental (Unplanned)
- [Debt item]: [Impact on future velocity]

## Metrics

**Velocity**
- Planned: [X points/features]
- Actual: [Y points/features]
- Variance: [Analysis]

**Runway Impact**
- Sprint duration: N days
- Total runway: M days remaining
- Progress against must-haves: X of Y
- **Pace evaluation**: [Are you on track? Behind? Ahead?]

## The Hard Question

**Would I fund another sprint of this?**

[Yes / No / Only if...]

[Reasoning and required changes]

## Adjustments for Next Sprint

- [What needs to change in the plan?]
- [What's the new priority?]
- [What should we NOT do next sprint?]
```

Keep it real. If velocity is dropping, say why. If scope keeps slipping, that's the problem, not poor estimation.
