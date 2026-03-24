---
name: daily-standup
description: >
  Quick daily check-in summarizing what shipped, what's planned, blockers. Key feature: scope creep detection vs MVP-SPEC. Runway tracking. Use daily during build phase to keep team aligned.
benefits-from: build-phase-kickoff
feeds-into: sprint-retro
---

# Daily Standup

A ruthless daily health check on progress, scope, and runway burn. Run every day during build phase.

---

## Phase 0: Setup & Context

**Purpose:** Gather the inputs needed to assess progress.

1. Read recent git log (commits since last standup)
2. Read PLAN.md to understand the 90-day sprint roadmap
3. Read MVP-SPEC.md to lock down what "done" means
4. Locate and read STANDUP-LOG.md if it exists (to add new entry)

**Exit Criteria:** All four files read and context loaded.

**AI Instructions:**
Do not ask any questions in this phase. Load all context silently. Proceed to Phase 1.

---

## Phase 1: Shipped Features & Progress (AskUserQuestion)

**Purpose:** Get honest data on what actually shipped since yesterday.

The AI must use the **AskUserQuestion tool** with this exact 4-part format:

**Re-ground:** "We're in the build phase of [PROJECT_NAME]. Today is Day N of M. Your job is to report what actually shipped."

**Simplify:** "Think of this like a commit log in plain English. What features, fixes, or integrations did the team complete since yesterday? Don't worry about polish — just: what's done? This is the basis for runway calculations."

**Recommend:** "RECOMMENDATION: Give specific feature names, not vague summaries. Completeness: 10/10 if you say 'User authentication via OAuth' vs 3/10 if you say 'backend work.'"

**Options:**
- A) List shipped features with component/scope (e.g., "Auth: OAuth login", "API: User endpoint", "UI: Dashboard v1")
- B) Summary with git commit hashes for reference (e.g., "Shipped: auth-oauth (commit a1b2c3d), user-api (commit e4f5g6h)")
- C) Just the high-level count (e.g., "3 features shipped, 1 API endpoint, 0 bugs fixed")

**Exit Criteria:** Clear list of shipped features. Proceed to Phase 2.

---

## Phase 2: Planned & Blockers (AskUserQuestion)

**Purpose:** Understand what's in flight and what's stopping progress.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Day N of M. We've shipped [recap from Phase 1]. Now let's look forward."

**Simplify:** "What are you planning to finish today? And what's getting in the way? Blockers can be technical (API limits, database schema), external (waiting on third-party), or human (unclear requirements)."

**Recommend:** "RECOMMENDATION: Name the blocker AND the mitigation. Don't just say 'API limits' — say 'API limits. Workaround: cache responses locally.'"

**Options:**
- A) Planned features today + list of active blockers with mitigations
- B) Planned features + blockers + estimated time each blocker will take
- C) Quick summary: "Plan: feature X, Y. Blocker: Z (waiting on response from vendor)"

**Exit Criteria:** Clear blockers list. Proceed to Phase 3.

---

## Phase 3: Scope Creep Check (Automated, No Question)

**Purpose:** Catch drift from MVP-SPEC before it balloons.

**AI Instructions:**
Compare work-in-progress and shipped features against MVP-SPEC.md.

If any feature exists that is **not in MVP-SPEC**, flag it immediately. Examples of scope creep:

| Drift | Red Flag |
|------|----------|
| "Building admin dashboard" | That's Stage 8. MVP is Stage 3. ALARM. |
| "Optimizing database queries" | Good engineering, but Stage 4 timeline says launch in 20 days. Are we behind? |
| "Adding dark mode" | Nice-to-have. Not in MVP-SPEC. Cut or defer. |

If flagged, use **AskUserQuestion**:

**Re-ground:** "Scope check found [ITEM] in progress. That's not in MVP-SPEC.md."

**Simplify:** "This feature was not planned for this sprint. Either it's important enough to delay launch, or it should be cut. Which is it?"

**Recommend:** "RECOMMENDATION: If it's not in the spec, cut it or reschedule for post-launch. Scope creep is the #1 killer of launch timelines."

**Options:**
- A) Cut this feature entirely
- B) Move it to post-launch (Phase 2 roadmap)
- C) Add it to MVP-SPEC (and confirm team alignment on new timeline)

If no scope creep detected, skip this question. Proceed to Phase 4.

---

## Phase 4: Runway Calculation (Automated, No Question)

**Purpose:** Quantify how fast you're burning runway and whether you're on track.

**AI Instructions:**
No user question needed. Calculate and display:

```
RUNWAY ANALYSIS
================

Timeline Pace:
- Days elapsed: [N] / [M] total ([%] of runway spent)
- Days remaining: [M - N]

Feature Completion:
- Must-haves completed: [X] / [Y]
- Completion rate: [X/Y = %]
- Should have completed by now: [Y * (days_elapsed / total_days)]

Burn Rate Assessment:
- Expected pace: [Y * (days_elapsed / total_days)] must-haves completed
- Actual pace: [X] must-haves completed
- Delta: [AHEAD / ON_TRACK / AT_RISK / BEHIND]

Example: "Day 23 of 42. You've shipped 3 of 8 must-haves (38%).
At this pace, you'll complete 6.5 must-haves by launch.
You need 8. You're 1.5 features behind. Either cut scope or accelerate."
```

**Pace Status Rules:**
- **ON_TRACK**: Actual ≥ Expected - 1 feature
- **AT_RISK**: Actual = Expected - 2 to 3 features
- **BEHIND**: Actual < Expected - 3 features

If status is not ON_TRACK, use **AskUserQuestion**:

**Re-ground:** "Runway analysis shows you're [BEHIND / AT_RISK]. At this pace, you'll ship [X] features, but you need [Y]."

**Simplify:** "This is a forcing function. You have three levers: cut features, extend timeline, or add resources. What's the move?"

**Recommend:** "RECOMMENDATION: Cut scope now while you have time to replan. Cutting scope in week 2 is easy. Cutting scope in week 6 is chaos."

**Options:**
- A) Cut [N] features from MVP-SPEC (name them, get confirmation on new scope)
- B) Extend launch timeline by [N] days (confirm with stakeholders)
- C) Bring in additional resources (if possible; detail the role and duration)

Proceed to Phase 5.

---

## Phase 5: Output & Archive

**Purpose:** Create the daily log entry.

**AI Instructions:**
Append a new entry to STANDUP-LOG.md with this format:

```markdown
## Day N - YYYY-MM-DD

**Shipped:**
- [Feature A] - [scope/component]
- [Feature B] - [scope/component]

**Planned today:**
- [Task X]
- [Task Y]

**Blockers:**
- [Issue]: [mitigation]
- [Issue]: [mitigation]

**Scope check:**
- [Any drift from MVP-SPEC?]
- [Any scope creep flagged?]

**Runway status:**
- Pace: [ON_TRACK / AT_RISK / BEHIND]
- Days: [N] of [M] ([%] spent)
- Must-haves: [X] of [Y] complete
- Burn rate concern: [One-line assessment]

**Owner decision:**
[If Phase 3 or 4 required a decision, document what was chosen]
```

**Tone Guidance:**
- No sugarcoating. Runway anxiety is real and necessary.
- Be direct: "You're 1.5 features behind. This is fixable if you cut scope now."
- Celebrate on-track progress: "Day 15, right on pace. Shipping at expected velocity."

Keep the log entry under 500 words. This is a sanity check, not a novel.

**Exit Criteria:** Entry appended to STANDUP-LOG.md. Daily standup complete.

---

## Escape Hatches

**If user is impatient ("just do it"):**
- Skip the AskUserQuestion in Phases 1 & 2. Infer from git log and ask only about scope drift (Phase 3).
- Jump to runway calculation (Phase 4).
- Output the log entry (Phase 5).

**If user provides shipping details immediately:**
- Skip Phase 1 question. Use the details provided.
- Ask only about blockers (Phase 2).

**If scope is locked and no creep detected:**
- Skip Phase 3 entirely.

---

## When to Run

- **Daily**: Every morning or end-of-day, same time each day
- **During**: Build phase only (pre-launch)
- **Skip if**: No commits since last standup (log "no progress" and investigate why)

---

## Completion Status

At the end of the skill, report one of:
- **DONE**: Log entry appended, runway clear, scope locked
- **DONE_WITH_CONCERNS**: Log entry appended, but scope drift or behind-pace flagged
- **BLOCKED**: Cannot assess runway (missing PLAN.md, MVP-SPEC.md, or STANDUP-LOG.md)
- **NEEDS_CONTEXT**: Unclear what "yesterday's standup" was; ask user for starting point
