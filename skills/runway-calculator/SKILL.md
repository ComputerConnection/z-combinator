---
name: runway-calculator
description: Forces honest financial planning. Calculate monthly burn rate, runway in months, revenue milestones needed to survive, and decision deadlines. Phase-based guided interaction.
trigger_phrases:
  - "runway calculator"
  - "how long can I survive"
  - "burn rate"
  - "financial planning"
  - "when will I run out of money"
  - "stage 5 finances"
benefits-from:
  - business-formation
feeds-into:
  - founder-wellness
version: 2.0
---

# Runway Calculator (Guided Interactive)

This is the skill that makes founders confront reality.

Most founders know roughly how much money they have. Most have no idea how much they're spending. And almost none have honestly modeled what happens when the two collide.

This skill forces the math. It's uncomfortable. But it's the math that determines whether you have 2 months or 18 months to make something work.

## Phase Overview

This skill works in phases:
- **Phase 0:** Context gathering (savings, team size, timeline)
- **Phase 1:** Monthly burn rate calculation (3 scenarios)
- **Phase 2:** Runway calculation (months until out of money)
- **Phase 3:** Decision deadline (the hard deadline)
- **Phase 4:** Revenue milestones (what revenue extends runway)
- **Phase 5:** Ramen profitability threshold (minimum to sustain)
- **Phase 6:** Financial reality check (blunt assessment)
- **Phase 7:** Day job question (when to quit)
- **Phase 8:** Output & lock (RUNWAY.md)
- **Phase 9:** Completion

Each phase uses AskUserQuestion guided interactions.

---

## Why This Matters

**Hope is not a financial plan.**

If your runway calculation requires everything going perfectly, all timelines accurate, no unexpected costs, immediate traction... you don't have a plan. You have a hope.

This skill forces honest math to:
1. Calculate real runway (not hopeful runway)
2. Show decision deadline (the date constraints force a choice)
3. Identify revenue milestones needed
4. Expose timeline realism
5. Make you confront opportunity cost

---

## Phase 0: Context & Constraints

**Goal:** Understand current financial position before calculations.

I will ask:
- How much money do you have (savings/funding)?
- Are you solo or founding team of N?
- Are you full-time or part-time on this?
- What's your expected timeline to MVP/traction?

**Exit criteria:** I understand your financial starting point. Move to Phase 1 (Monthly Burn).

---

## Phase 1: Monthly Burn Rate Calculation

Burn rate is simple: **monthly spending - monthly revenue = monthly burn.**

But most founders miscalculate because they forget opportunity cost.

**Goal:** Itemize all monthly costs and calculate burn rate in 3 scenarios.

**Re-ground:** "We're calculating monthly burn rate. All costs: hosting, tools, marketing, salaries, opportunity cost. Three scenarios: optimistic, realistic, pessimistic."

Use AskUserQuestion tool:

**SIMPLIFY:** "Burn = what you spend minus what you make. Most founders forget opportunity cost (your salary if you worked elsewhere). Calculate 3 versions: best case, realistic, worst case. See the range."

**RECOMMEND:** "RECOMMENDATION: Include opportunity cost. It's real money you're giving up.
- Completeness: 3/10 (guessing, no itemization)
- Completeness: 6/10 (itemized, missing opportunity cost)
- Completeness: 10/10 (all costs itemized, three scenarios calculated)"

**For monthly costs, ask:**
- Hosting/infrastructure? (AWS, Heroku, etc.)
- Tools/subscriptions? (Stripe, GitHub, project mgmt, etc.)
- Marketing/acquisition spend?
- Salaries (if paying anyone)?
- Operating costs (insurance, legal, accounting)?
- Founder opportunity cost? (What you'd earn elsewhere)

**Build 3 scenarios:**

**Optimistic:**
- Timeline to MVP: 4 weeks
- Customer acquisition: smooth
- No surprises
- Total: $X/month

**Realistic:**
- Timeline takes 1.5x longer (6 weeks)
- Customer acquisition: harder than expected
- 1-2 surprises
- Total: $X/month

**Pessimistic:**
- Timeline takes 2x longer (8 weeks)
- Customer acquisition: slow
- Multiple surprises, extra costs
- Total: $X/month

**Exit criteria for Phase 1:** You've calculated monthly burn in 3 scenarios with itemized costs. Move to Phase 2 (Runway).

---

## Phase 2: Runway Calculation

**Goal:** Calculate months of runway for each scenario.

**Formula:** Runway (months) = (Savings + Funding) / Monthly Burn

**Example:**
- Savings: $100,000
- Optimistic burn ($13k/mo): 7.7 months runway
- Realistic burn ($16k/mo): 6.25 months runway
- Pessimistic burn ($23k/mo): 4.3 months runway

**Translation:** You have 4-8 months depending on how things go.

**Exit criteria for Phase 2:** You've calculated runway in months for all scenarios. Move to Phase 3 (Decision Deadline).

---

## Phase 3: Decision Deadline

**Goal:** Identify the hard deadline when constraints force a decision.

**Rule:** Take realistic runway and subtract 1 month as buffer.

**Example:** Realistic runway is 6 months → Decision deadline is 5 months from today.

**Mark this on your calendar.** This is not an estimate. This is the date you must decide:
- Raise funding?
- Hit revenue milestone?
- Pivot?
- Shut down?

**Exit criteria for Phase 3:** You have a calendar date for your decision deadline. Move to Phase 4 (Revenue Milestones).

---

## Phase 4: Revenue Milestones

**Goal:** Identify what revenue would extend runway.

**Question:** At what monthly revenue does burn = revenue? That's ramen profitable.

**Example (realistic scenario: $16k/month burn, $100k savings):**
- $5k MRR → extends runway to 9+ months
- $8k MRR → extends runway indefinitely (ramen profitable)
- $12k MRR → very sustainable

**Challenge:** Are these realistic?
- Can you hit $5k MRR by month 3? (Sometimes)
- Can you hit $8k MRR by month 5? (Harder)
- Can you hit $12k MRR? (Rare without traction)

If you can't hit any of these, your business model might not work at your burn rate.

**Exit criteria for Phase 4:** You've identified realistic revenue milestones. Move to Phase 5 (Ramen Profitability).

---

## Phase 5: Ramen Profitability Threshold

**Goal:** Identify the minimum revenue to sustain indefinitely.

**Real ramen profitability** = burn - (market-rate founder salary) + (lower salary you'd accept)

**Example:**
- Burn: $16k/month
- Market salary (lost opportunity): $10k/month
- Salary you'd accept: $5k/month
- Ramen profitable MRR: $16k - $10k + $5k = $11k

At $11k MRR, you're covering costs and paying yourself something to survive.

**Exit criteria for Phase 5:** You've calculated true ramen profitability threshold. Move to Phase 6 (Reality Check).

---

## Phase 6: Financial Reality Check

**Goal:** Get blunt assessment of what numbers mean.

I will write a one-paragraph reality check addressing:
- Are you in decent shape or tight?
- What decision deadline means for your planning?
- Is your timeline realistic or fantasy?
- What needs to happen to survive?

**Examples:**

"You have 7 months. That's enough to build MVP, find initial traction, and decide next steps. You're OK."

"You have 5 months to hit $8k MRR or raise. Tight but doable if customer acquisition works. You need traction, not polish."

"If things get harder, you're out in 4 months. Your decision deadline is upon you. Plan your next move now."

"Your burn and timeline don't align. Building enterprise product in 4 months solo is optimistic. Reconsider."

**Exit criteria for Phase 6:** You have a blunt reality assessment. Move to Phase 7 (Day Job).

---

## Phase 7: Day Job Question

**Goal:** Model when to quit your job (if applicable).

**Re-ground:** "Should you quit your job? Decision depends on runway, confidence, and signal."

Use AskUserQuestion tool:

**SIMPLIFY:** "Don't quit into <2 months runway with zero revenue. That's panic. Do quit once you have 12+ months runway or revenue covering burn or co-founder sharing risk."

**RECOMMEND:** "RECOMMENDATION: Transition gradually if possible.
- Completeness: 2/10 (all-in with low runway)
- Completeness: 6/10 (still working, reducing hours)
- Completeness: 10/10 (full-time with safety net in place)"

**Framework:**
- **Phase 1 (0-3 months):** Part-time, build side project, get signal
- **Phase 2 (3-6 months):** If good signal, negotiate flex hours, reduce day job
- **Phase 3 (6+ months):** Only quit when you have 12+ months runway OR revenue covering burn OR co-founder sharing risk

**Exit criteria for Phase 7:** You've decided whether to keep day job. Move to Phase 8 (Output).

---

## Phase 8: Output & Lock RUNWAY.md

**Goal:** Generate final runway document.

I will produce **RUNWAY.md** containing:

```markdown
# Runway Analysis

## Monthly Burn Rate (3 Scenarios)

### Optimistic Scenario
[Itemized costs, total burn]

### Realistic Scenario
[Itemized costs, total burn]

### Pessimistic Scenario
[Itemized costs, total burn]

## Runway in Months

- Optimistic: X months (Decision date: YYYY-MM-DD)
- Realistic: X months (Decision date: YYYY-MM-DD)
- Pessimistic: X months (Decision date: YYYY-MM-DD)

## Revenue Milestones

To extend runway indefinitely:
- $X MRR by Month Y (probability: realistic/stretch)

## Ramen Profitability Threshold

$X MRR covers burn + minimum salary to survive

## Financial Reality Check

[One paragraph blunt assessment]

## Day Job Timeline

[When to quit, if applicable]
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

## Phase 9: Completion & Handoff

**Completion status:** Once RUNWAY.md is saved, skill is complete.

**Recalculation:** Update monthly as circumstances change (revenue, cost changes, new funding).

**Next steps:** Use decision deadline to drive urgency. Hit revenue milestones or prepare next decision.

---

## Completion Status

**DONE** — RUNWAY.md written and saved.
**DONE_WITH_CONCERNS** — Runway tight, decision deadline is soon.
**BLOCKED** — Numbers don't work, need to reconsider approach.
**NEEDS_CONTEXT** — Need cost structure clarity from LEAN-CANVAS.

**Next Step:** Proceed to founder-wellness.
Return to z-combinator orchestrator for routing.

---

## Key Principle

**Hope is not a financial plan.** Founders who know their constraints make better decisions than founders in denial. This is not pessimism. This is realism.
