---
name: mvp-scoper
description: BRUTALLY cut scope to the minimum viable product. Force MoSCoW classification on every feature. Challenge every "must have." Enforce 4-6 week delivery for solo founders. Anti-feature-creep enforcer. Phase-based guided interaction.
trigger_phrases:
  - scope the mvp
  - mvp spec
  - what should I build first
  - cut scope
  - minimum viable product
  - feature prioritization
benefits-from:
  - lean-canvas
feeds-into:
  - tech-stack-advisor
---

# MVP Scoper: The Anti-Feature-Creep Enforcer (Guided Interactive)

## What an MVP Actually Is

**Minimum Viable Product:** The smallest possible product that lets you validate one core hypothesis with real customers.

Not version 0.5. Not a "feature-limited" version. The absolute smallest thing that delivers one unit of value to one type of customer.

Most founders build v1, then call it an MVP. That's backwards. You build an MVP, get feedback, then evolve it.

## Hard Truth About Features

You will have 12 "must haves." A real MVP has 3-5.

You will estimate 3 months. A real MVP takes 4-6 weeks for a solo founder.

You will convince yourself you need user profiles, notifications, admin dashboard, and 47 other things. You don't.

**Your job in this skill:** Cut until it hurts. Then cut some more.

## Phase Overview

This skill works in phases:
- **Phase 0:** Feature extraction (list every feature mentioned)
- **Phase 1:** MoSCoW classification (MUST / SHOULD / COULD / WON'T)
- **Phase 2:** Founder type assessment (personalized pushback)
- **Phase 3:** Critical path definition (signup → value → done)
- **Phase 4:** Timeline challenge (4-6 weeks or scope is too big)
- **Phase 5:** Output & lock (MVP-SPEC.md)
- **Phase 6:** Completion

Each phase uses guided AskUserQuestion interactions.

---

## Phase 0: Feature Extraction & Assessment

**Goal:** Extract every feature mentioned in your docs and conversations. Then assess which are validated vs. invented.

I will search for and read:
- LEAN-CANVAS.md (solution section)
- DESIGN-DOC.md (if exists)
- Any messages or notes where features are mentioned
- Your initial pitch/description

From these, I'll extract every feature, enhancement, and nice-to-have mentioned. Every. Single. One.

**Exit criteria:** You have a complete list of 20+ potential features extracted and ready to classify.

**User interaction:** I'll search your project directory and create an extracted list, then ask for confirmation.

---

## Phase 1: MoSCoW Classification

**Goal:** Classify each feature as MUST / SHOULD / COULD / WON'T using rigorous definitions.

**Re-ground:** "We're at Phase 1 of MVP Scoping. We're classifying [Feature Name] against your LEAN-CANVAS problems and solutions."

For each feature, use AskUserQuestion tool:

**SIMPLIFY:** "We're asking: Is this critical to core value delivery? Did customers ask for it? Can we ship MVP without it? We're sorting features into 4 buckets: Must-have (core), Should-have (next), Could-have (wishful), Won't-have (explicit no)."

**RECOMMEND:** "RECOMMENDATION: Features are MUST only if the product doesn't work without them. Everything else is future.
- Completeness: 2/10 (everything is must-have)
- Completeness: 6/10 (3-5 must-haves, rest unclear)
- Completeness: 10/10 (3-5 must-haves locked, rest classified)"

**For MUST HAVE classification, ask:**
- Is this critical path to customer value?
- Did customers specifically ask for this, or did you invent it?
- Would the MVP fail without this, or would it still deliver core value?
- Can you build just this in 1-2 weeks, or is it complex?

**For SHOULD HAVE classification, ask:**
- Is this valuable but not core to first version?
- Can customers get value without this?
- Does this belong in v1.1 (first update after launch)?

**For COULD HAVE classification, ask:**
- Is this interesting but not validated?
- Would a customer pay extra for this alone?
- Does this distract from core mission?

**For WON'T HAVE classification, ask:**
- Does this actively distract from core mission?
- Is this a feature you think is cool but customers didn't ask for?
- Will skipping this actually harm MVP?

**Red flags to push back on:**

- Everything is "must"
- Features invented (not customer-requested)
- Unclear if critical to core job
- Solving symptoms instead of root cause

**Strong classification approach:**
- MUST: Create/send invoices (core job)
- SHOULD: Invoice templates, recurring invoices (nice, not core)
- COULD: Mobile app, dark mode, integrations (wishful)
- WON'T: Gamification, AI magic, blockchain (distracting)

**Exit criteria for Phase 1:** You've classified 20+ features into MUST / SHOULD / COULD / WON'T buckets with reasoning. Move to Phase 2 (Founder Type Pushback).

---

## Phase 2: Founder Type Assessment & Pushback

**Goal:** Understand your founder type (Technical Builder, Visionary, People Person) and apply appropriate scope pressure.

I will read your FOUNDER-PROFILE.md and apply personalized pushback:

**Re-ground:** "We're at Phase 2. You're a [Founder Type]. I need to push you specifically on your scope weaknesses."

Use AskUserQuestion tool:

**SIMPLIFY:** "Different founder types over-engineer in different ways. Technical builders over-engineer architecture. Visionaries over-engineer features. People persons over-engineer validation. You're going to feel pushed. That's intentional."

**RECOMMEND:** "RECOMMENDATION: Acknowledge your founder type and commit to the constraint. 4-6 weeks. One core feature. Everything else deferred.
- Completeness: 3/10 (rejecting scope constraints)
- Completeness: 7/10 (acknowledging weakness, trying to stay focused)
- Completeness: 10/10 (fully committed to 4-6 week scope, knows why)"

**OPTIONS (based on founder type):**

**IF TECHNICAL BUILDER:**
- **(A)** "I acknowledge I'll over-engineer. I'm committing to monolith, single database, Heroku. No microservices, no Docker, no fancy infrastructure."
- **(B)** "I want to build it right architecturally. I can't build slop."
- **(C)** "I'm not sure how to commit to 4 weeks if I can't architect properly."

**IF VISIONARY:**
- **(A)** "I acknowledge I'm building for a future that doesn't exist. I'm committing to beachhead customer only, one feature."
- **(B)** "I see the long-term vision clearly. It's hard to not build towards it."
- **(C)** "I'm concerned we're too narrow. What about the bigger picture?"

**IF PEOPLE PERSON (NON-TECHNICAL):**
- **(A)** "I acknowledge I want to validate every feature. I'm committing to one customer segment, one feature they asked for."
- **(B)** "I've validated that customers want X, Y, and Z. I feel like we need all of them."
- **(C)** "I'm worried about disappointing customers by shipping incomplete."

**Exit criteria for Phase 2:** You've acknowledged your founder type, accepted the pushback, and committed to 4-6 week timeline. Move to Phase 3 (Critical Path).

---

## Phase 3: Critical Path Definition

**Goal:** Define the shortest path from signup → core value → exit. Should take 60-90 seconds.

**Re-ground:** "We're at Phase 3. We know what's MUST-HAVE. Now: What's the critical path? The 5-7 steps a customer takes from sign-up to experiencing core value."

Use AskUserQuestion tool:

**SIMPLIFY:** "Critical path is: User arrives → signs up → uses core feature → gets value → leaves. No onboarding. No tutorials. No preferences. Core value in 60-90 seconds. That's it."

**RECOMMEND:** "RECOMMENDATION: Shorter is better. If your critical path is more than 7 steps, you're adding unnecessary friction.
- Completeness: 3/10 (10+ steps, lots of setup)
- Completeness: 6/10 (5-7 steps, some friction)
- Completeness: 10/10 (3-5 steps, <90 seconds to value)"

**OPTIONS:**
- **(A)** "I have a clear 3-5 step critical path that takes <90 seconds."
- **(B)** "I have critical path but it's probably 7+ steps."
- **(C)** "I'm not sure what critical path should be. Help me define it."

**Case study example (Invoice app):**
1. User signs up
2. User clicks "New Invoice"
3. User enters customer name, amount, due date
4. User clicks "Send"
5. Invoice is sent
→ Done. 60 seconds.

**NOT in critical path:**
- Onboarding tutorials
- Profile setup
- Preferences/settings
- Integration configuration
- Account customization

**Exit criteria for Phase 3:** You have a 3-5 step critical path that takes <90 seconds. Move to Phase 4 (Timeline Challenge).

---

## Phase 4: Timeline Challenge

**Goal:** Lock in a 4-6 week timeline with realistic week-by-week breakdown.

**Re-ground:** "We're at Phase 4. Time reality check. You've defined critical path and MUST features. Now: Can you actually build this in 4-6 weeks?"

Use AskUserQuestion tool:

**SIMPLIFY:** "4-6 weeks for a solo founder. If you estimate 3 months, your scope is too big and we'll cut more. Give me week-by-week breakdown: Week 1 (auth + data model), Week 2 (core feature UI + functionality), Week 3 (testing), Week 4 (launch)."

**RECOMMEND:** "RECOMMENDATION: Tight timeline forces hard prioritization. If you can't do it in 4-6 weeks, scope is too big.
- Completeness: 2/10 (12+ week estimate)
- Completeness: 6/10 (8-10 week estimate)
- Completeness: 10/10 (4-6 week breakdown, realistic)"

**OPTIONS:**
- **(A)** "I can build MVP in 4-6 weeks. Here's my week-by-week breakdown."
- **(B)** "My estimate is 8-10 weeks. I need to cut more scope."
- **(C)** "My estimate is 12+ weeks. I'm definitely over-scoped."
- **(D)** "I'm not sure. Help me estimate realistically."

**Timeline challenge questions:**
- What's your week 1? (Usually: auth + data model)
- What's your week 2? (Usually: core feature UI + backend)
- What's your week 3? (Usually: bug fixes + iteration)
- What's your week 4? (Usually: final polish + launch)
- When do you deploy to 5 customers?
- When do you get first feedback?

**Red flags to push back on:**
- Weeks 1-2 spent on "architecture" or "infrastructure setup"
- Week 5-6 spent on "polish" (means scope was too big)
- First customer not until week 4+ (too late for feedback)
- "We'll optimize/refactor after launch" (you won't have time)

**Real 4-week timeline:**
```
Week 1: Auth + core data model (2-3 days). UI shell (2-3 days).
Week 2: Core feature building (full feature end-to-end).
Week 3: Customer testing + bug fixes + iteration.
Week 4: Final polish + launch.

Deployment: End of week 3/4
First 5 customers: Have MVP in their hands week 4
Feedback cycle: Week 5+
```

**Exit criteria for Phase 4:** You have a 4-6 week breakdown with week-by-week commitments. Move to Phase 5 (Output).

---

## Phase 5: Output & Lock MVP-SPEC.md

**Goal:** Generate final MVP-SPEC.md with all decisions locked.

I will produce a document containing:

```markdown
# MVP Specification: [Product Name]

## Core Vision
[One sentence: what this product does for whom]

## Critical Path (User Journey)
[3-5 steps from signup to core value delivered]

## Features: MUST HAVE (Building in MVP)
[3-5 features, each with:]
- Why: [customer evidence]
- Scope: [exact deliverables]
- Effort: [weeks to build]
- Test: [how you'll know it works]

## Features: SHOULD HAVE (v1.1 - after launch)
[Features you want, but deferring]
- Why: [reason]
- Timeline: [when you'll build]

## Features: NOT BUILDING (Explicit WON'T list)
[15-20 features you're explicitly excluding]

## Timeline (Week by Week)
[4-6 week breakdown, realistic]

## Success Metrics
[How you know MVP succeeded]

## Notes & Constraints
[Tech stack assumptions, risks, blockers]
```

---

## Escape Hatches

**If founder says "just do it" or expresses impatience:**
- Fast-track to artifact generation phase
- Use best available information to fill gaps
- Note any assumptions made

**If founder's answers cover multiple questions:**
- Smart-skip already-answered phases
- Acknowledge what was covered and move forward

---

## Phase 6: Completion & Handoff

**Completion status:** Once MVP-SPEC.md is saved to your project directory, the skill is complete.

**Next steps after completion:**
- Pass this to **tech-stack-advisor** (what language/framework to use)
- Use this as your development roadmap
- Treat NOT-BUILDING list as sacred (no additions)
- Recalculate weekly if timeline slips (cut more scope, not extend timeline)

---

## Completion Status

**DONE** — MVP-SPEC.md written and saved.
**DONE_WITH_CONCERNS** — Spec locked but timeline might slip if issues arise.
**BLOCKED** — Scope still too big, waiting for scope cuts.
**NEEDS_CONTEXT** — Need customer interview data to validate MUST-HAVEs.

**Next Step:** Proceed to tech-stack-advisor.
Return to z-combinator orchestrator for routing.

---

## Scope Creep Prevention

Once MVP-SPEC.md is locked, every feature request gets categorized:
- **Does it ship with MVP?** NO (unless critical path)
- **Goes to v1.1?** Maybe (after you have customers)
- **Goes to v2?** Probably
- **Gets killed?** Possibly

You don't build anything not in MUST HAVE.

You don't say "oh we'll just add this one thing." One thing becomes five things becomes 12 weeks becomes a product nobody uses.

Every feature you add delays customer feedback by 1 week.

Delaying feedback is how you build the wrong thing.

---

## Ready to Scope?

When you're ready, I'll ask about Phase 0: What features have you mentioned? Then we'll extract, classify, and lock your MVP down to 4-6 weeks.
