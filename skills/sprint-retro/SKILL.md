---
name: sprint-retro
description: End-of-sprint retrospective for startups. Evaluates velocity vs plan, scope changes, technical debt (intentional vs accidental), runway consumed vs progress. Forces honest evaluation. Use at sprint end.
benefits-from: daily-standup
feeds-into: launch-checklist
---

# Sprint Retrospective

End-of-sprint brutal honesty. Not a feel-good session. Is the project on track?

---

## Phase 0: Gather Input & Context

**Purpose:** Load sprint data for analysis.

1. Read PLAN.md (sprint goals and timeline)
2. Review git log for the sprint period (what shipped?)
3. Read STANDUP-LOG.md (planned vs actual across the sprint)
4. Get sprint dates from user if not in PLAN.md

**Exit Criteria:** All data loaded, sprint period defined (e.g., "Sprint 3: March 3-16").

**AI Instructions:**
Do not ask any questions. Load context silently. Proceed to Phase 1.

---

## Phase 1: Sprint Goals vs Actual Shipped (AskUserQuestion)

**Purpose:** Get clear data on planned vs delivered.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Sprint [N] is complete. You set [X] goals at the start. Now let's see what you actually shipped."

**Simplify:** "What features, fixes, and integrations actually made it across the finish line? How close are you to sprint goals? This is not about excuses — it's about pattern recognition."

**Recommend:** "RECOMMENDATION: If you hit all goals, great. If you hit 60-70%, that's your true velocity. That's what we plan future sprints around."

**Options:**
- A) List shipped features with estimated vs actual hours/story points
- B) Shipped features with quick notes on what slipped and why
- C) Percentage of planned work completed (e.g., "65% of sprint goals shipped")

**Exit Criteria:** Clear picture of goals vs actual. Proceed to Phase 2.

---

## Phase 2: Scope Changes (AskUserQuestion)

**Purpose:** Audit what changed mid-sprint and why.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Sprint [N]: you planned [X], shipped [Y]. But something probably changed mid-sprint."

**Simplify:** "Scope creep is when new features sneak in (or planned features sneak out). Both matter. Tell me: what got added that wasn't planned, and what got cut?"

**Recommend:** "RECOMMENDATION: Flag additions as distractions unless they were emergencies (critical bug, customer blocker). Flag removals — if you're cutting work, you're behind."

**Options:**
- A) List features added during sprint (with reason: emergency, customer request, nice-to-have, distraction)
- B) List features removed (with reason: deprioritized, too complex, blocker)
- C) Summary: "Added: 2 small tasks. Removed: 1 feature (too complex). Scope neutral."

**Exit Criteria:** Clear audit of scope delta. Proceed to Phase 3.

---

## Phase 3: Technical Debt Audit (AskUserQuestion)

**Purpose:** Separate smart shortcuts from future pain.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Scope changed. But there's another hidden cost: technical debt. Did you cut corners deliberately or accidentally?"

**Simplify:** "Intentional debt is smart: 'We shipped auth without password recovery because we're launching in 14 days. We'll fix it week 5.' Accidental debt kills you: 'Our database schema is a mess but we didn't document it, so next sprint we're stuck.'"

**Recommend:** "RECOMMENDATION: Document ALL debt (intentional and accidental) and assign a fix date. Untracked debt compounds into technical bankruptcy."

**Options:**
- A) Intentional debt with fix dates + accidental debt with impact estimates
- B) Just intentional debt (and admit if you don't know about accidental debt yet)
- C) Summary: "Took 3 days of intentional debt (auth shortcut, fix week 5). Discovered 2 accidental issues (slow queries, schema gaps)."

**Exit Criteria:** Debt audit complete. Proceed to Phase 4.

---

## Phase 4: Runway & Velocity Analysis (Automated, No Question)

**Purpose:** The scariest metric: runway consumed vs progress made.

**AI Instructions:**
Calculate and display:

```
RUNWAY & VELOCITY ANALYSIS
===========================

Timeline Analysis:
- Sprint duration: [N] days
- Total runway (from PLAN.md): [M] days
- Runway consumed so far: [X] days ([%] of total)
- Runway remaining: [M - X] days

Feature Velocity:
- Planned for sprint: [A] must-haves
- Completed in sprint: [B] must-haves
- Velocity rate: [B/A = %]

Cumulative Progress:
- Must-haves target (total): [Y]
- Must-haves completed (all sprints): [Z]
- Completion rate: [Z/Y = %]
- Should have completed by now: [Y * (days_elapsed / total_days)]

Pace Assessment:
- Expected vs actual: [ON_TRACK / AT_RISK / BEHIND]

Example: "Sprint 3 of 6. You planned 5 must-haves, shipped 3.
Your velocity: 60%. At this rate, you'll ship 18 of 20 must-haves.
You're 2 features behind. You have 3 sprints left to catch up."
```

**Pace Status Rules:**
- **ON_TRACK**: Actual velocity ≥ 90% of planned
- **AT_RISK**: Actual velocity 70-89% of planned
- **BEHIND**: Actual velocity < 70% of planned

If status is not ON_TRACK, use **AskUserQuestion**:

**Re-ground:** "Velocity analysis: you're [BEHIND / AT_RISK]. At this pace, you'll complete [X] features, but you need [Y]."

**Simplify:** "This is a forcing function. Sprint 3 is the time to adjust, not sprint 6. What's the move: cut more features, find more hours, or extend timeline?"

**Recommend:** "RECOMMENDATION: If you're behind, cut features NOW. Every sprint of delay compounds. It's easier to replan this week than to panic in week 6."

**Options:**
- A) Cut [N] must-haves from remaining sprints (name them, get confirmation)
- B) Extend launch timeline by [N] sprints (accept consequence: more runway burned)
- C) Stay the course (and accept risk of missing launch targets)

Proceed to Phase 5.

---

## Phase 5: The Hard Question (AskUserQuestion)

**Purpose:** Founder gut-check on project viability.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "You've shipped [X%] of planned work. You're [ON_TRACK / AT_RISK / BEHIND]. Now the hard question."

**Simplify:** "If this sprint cost you [runway spent], and you got [progress made], would you write a check for another sprint? Or do you need to change something before you commit more time/money?"

**Recommend:** "RECOMMENDATION: If you'd fund another sprint, you have confidence. If not, something is broken. Say what it is: poor planning, wrong product direction, team velocity, or scope bloat. Then fix it before sprint 4."

**Options:**
- A) Yes, fund another sprint (and explain: momentum, progress, or team execution looks good)
- B) Only if we fix [X] (scope creep, velocity, planning accuracy) — specify the change
- C) No — this project isn't on track (and trigger escalation to founder)

**Exit Criteria:** Hard decision made. Proceed to Phase 6.

---

## Phase 6: Adjustments for Next Sprint (AskUserQuestion)

**Purpose:** Lock in the plan for next sprint.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Based on everything above, what's different for sprint [N+1]?"

**Simplify:** "You learned something this sprint. Maybe your estimates are off, or scope keeps slipping, or a blocker appeared. Use those learnings to plan better next time."

**Recommend:** "RECOMMENDATION: If velocity was 60%, plan for 60% in sprint 4. Don't plan for 100% and hope. Realistic plans beat optimistic ones."

**Options:**
- A) New priorities for sprint [N+1] (list features, in order)
- B) Velocity adjustment + new priority list (e.g., "Plan for 60% velocity. Reprioritize around [X].")
- C) Major replanning needed (e.g., "Cut 3 must-haves from scope, push them to Phase 2")

**Exit Criteria:** Next sprint plan confirmed. Proceed to Phase 7.

---

## Phase 7: Output & Archive

**Purpose:** Create the sprint retro document.

**AI Instructions:**
Create SPRINT-[N]-RETRO.md with this format:

```markdown
# Sprint [N] Retrospective

## Sprint Dates
[Start date] to [End date]

## Original Goals
- [Goal 1]
- [Goal 2]
- [Goal 3]

## What Actually Shipped
- [Feature/task 1]: [Estimated hours] / [Actual hours]
- [Feature/task 2]: [Est] / [Actual]
- [Count]: [A of B planned features shipped]

## Scope Changes During Sprint

### Added
- [Feature/reason]: [Impact on timeline]
- [Feature/reason]: [Impact on timeline]

### Removed
- [Feature/reason]: [Why cut]
- [Feature/reason]: [Why cut]

## Technical Debt Audit

### Intentional
- [Debt item]: Plan to fix by [Date]
- [Debt item]: Plan to fix by [Date]

### Accidental (Unplanned)
- [Debt item]: [Impact on future velocity]
- [Debt item]: [Impact on future velocity]

## Metrics

**Velocity**
- Planned: [X] must-haves
- Actual: [Y] must-haves
- Variance: [X - Y] ([% completion])

**Runway Impact**
- Sprint duration: [N] days
- Total runway (from PLAN.md): [M] days
- Runway consumed to date: [X] days
- Runway remaining: [M - X] days
- Progress: [Z] of [T] must-haves complete ([%])

**Pace Evaluation**
- Status: [ON_TRACK / AT_RISK / BEHIND]
- At this velocity, launch on schedule: [YES / NO]
- Required adjustment: [Cut scope / Extend timeline / Accelerate]

## The Hard Question

**Would I fund another sprint of this?**

[YES / NO / ONLY IF...]

[Reasoning]

[If NO or ONLY IF: What needs to change?]

## Adjustments for Sprint [N+1]

- New priorities: [Feature list, in order]
- Velocity assumption: [X% of planned]
- Key change: [What's different?]

## Owner Sign-off
- Retro completed by: [Name]
- Date: [Date]
- Status for next sprint: [ON_TRACK / AT_RISK / NEEDS_ESCALATION]
```

**Tone Guidance:**
- Keep it real. If velocity is dropping, say why.
- If scope keeps slipping, that's the problem — not poor estimation.
- Celebrate wins: "Shipped 4 of 5. Good velocity."
- Flag risks: "We're 2 features behind. That's 1 sprint of delay at this velocity."

**Exit Criteria:** SPRINT-[N]-RETRO.md created, filed in project folder.

---

## Escape Hatches

**If user is impatient ("just do it"):**
- Ask only Phase 1 (shipped vs planned), Phase 4 (runway analysis), and Phase 5 (hard question).
- Skip Phase 2 (scope changes), Phase 3 (debt audit), Phase 6 (next sprint plan).
- Output a condensed retro.

**If velocity is clearly off:**
- Jump straight to Phase 5 (hard question) and Phase 6 (adjustments).
- Spend minimal time on details; focus on the forcing function.

**If this is sprint 1:**
- Skip the "cumulative progress" metrics (nothing to accumulate yet).
- Focus on establishing a velocity baseline.

---

## When to Run

- **End of each sprint** (typically weekly or bi-weekly during build phase)
- **Before starting next sprint planning**
- **When velocity changes significantly** (mid-sprint, if team speed suddenly drops)

---

## Completion Status

At the end of the skill, report one of:
- **DONE**: Retro complete, next sprint plan locked in, trajectory clear
- **DONE_WITH_CONCERNS**: Retro complete, but AT_RISK or BEHIND status flagged for founder review
- **BLOCKED**: Missing PLAN.md, STANDUP-LOG.md, or git history
- **NEEDS_CONTEXT**: Unclear what sprint number this is; ask user for sprint label
