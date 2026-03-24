---
name: daily-standup
description: Quick daily check-in summarizing what shipped, what's planned, blockers. Key feature: scope creep detection vs MVP-SPEC. Runway tracking. Use daily during build phase to keep team aligned.
---

# Daily Standup

Run this daily during the build phase. Your job is to be honest about progress, scope, and runway.

## What You Do

1. Read recent git log (since last standup) — extract actual shipped features
2. Read PLAN.md to understand the 90-day sprint roadmap
3. Read MVP-SPEC.md to lock down what "done" means
4. Read existing STANDUP-LOG.md if it exists
5. Ask: What actually shipped since yesterday?
6. Ask: What's breaking down or blocked?
7. **SCOPE CREEP ALARM**: Compare work-in-progress against MVP-SPEC. If engineers are building features not in the spec, flag it. Examples:
   - "You're building admin dashboard. That's Stage 8 feature. MVP-SPEC doesn't have this."
   - "You're optimizing queries. Good engineering, but Stage 4 timeline says launch in 20 days."

8. Calculate runway consumed:
   - Days elapsed / total days available
   - Features completed / total must-haves
   - Burn rate: "At this pace, you've completed 3 of 8 must-haves by day 23. You need to ship 5 more in 19 days. You're behind."

## Tone

Don't sugarcoat. Runway anxiety is real and necessary.

Example: "Day 23 of 42. You've shipped: user auth, core feature X. Planned today: integration testing. Blockers: API rate limits from third-party service. You're on pace, but feature Y isn't started yet and it's complex. Either cut it or reduce scope elsewhere."

## Output: Append to STANDUP-LOG.md

Format (add daily entry):
```
## Day N - YYYY-MM-DD

**Shipped:**
- [Feature A]
- [Feature B]

**Planned today:**
- [Task X]
- [Task Y]

**Blockers:**
- [Issue and mitigation]

**Scope check:**
- [Anything drifting from MVP-SPEC? Flag it.]

**Runway status:**
- Days: N of M (pace: ON_TRACK / AT_RISK / BEHIND)
- Must-haves: N of M complete
- Burn rate concern: [Any red flags?]
```

Keep it under 500 words. Speed matters. This is a sanity check, not a novel.
