---
name: metrics-review
description: Post-launch honest measurement of AARRR metrics. Acquisition, Activation, Retention, Revenue, Referral. Compares against lean canvas. No spinning bad numbers. "3% activation = emergency."
---

# Metrics Review

After launch, measure ruthlessly. Don't spin bad numbers — understand them and fix the root cause.

## What You Do

1. Read LEAN-CANVAS.md to see what you predicted for each metric
2. Gather actual data from analytics, payment processor, usage logs
3. Calculate AARRR metrics below
4. Compare actuals to lean canvas predictions
5. For any metric below target: diagnose root cause
6. Be brutally honest about what the numbers mean

## AARRR Metrics

### 1. Acquisition (How do people find you?)

**Key questions:**
- Where do your first 100 users come from?
- What's your Customer Acquisition Cost (CAC)?
- Is it sustainable?

**Calculate:**
```
Total marketing spend / New customers acquired = CAC

Example: Spent $5K on launch, got 200 users = $25 CAC
```

**By channel:**
| Channel | Users | Spend | CAC | Cost sustainability |
|---------|-------|-------|-----|-------------------|
| Product Hunt | [X] | $0 (time) | N/A | One-time |
| Hacker News | [X] | $0 | N/A | One-time |
| Twitter organic | [X] | $0 | N/A | One-time |
| Direct (friends/referral) | [X] | $0 | N/A | Best |
| Paid ads | [X] | $[Y] | $[CAC] | Check sustainability |

**Red flag:** If you're not tracking this per channel, you're blind. You don't know what works.

### 2. Activation (What % complete the critical path?)

**Key question:**
- Of everyone who lands on your site, how many get value?

**Calculate:**
```
Users who completed [critical action] / Total users who signed up = Activation rate

Examples:
- Email app: Users who connected email account / signup = activation
- SaaS: Users who created first project / signup = activation
- Marketplace: Buyers who made first purchase / signup = activation
```

**Red flag threshold:**
- >40% = Good (top 10% of apps)
- 20-40% = Acceptable, but fixable
- 10-20% = You have a problem. Users don't get value quickly enough.
- <10% = Emergency. 90% of people find you, try you, and leave.

**Example diagnostic:**
"3% activation means 97% of people who find you leave without getting value. That's an emergency. Every user who drops is a failure. What's the friction point?"

Possible causes:
- Onboarding is confusing
- Core feature doesn't work as advertised
- Value takes too long to show up
- Wrong traffic source (attracting wrong users)

### 3. Retention (Do people come back?)

**Key questions:**
- Day 1 retention (logged in again next day)
- Day 7 retention (still using after 1 week)
- Day 30 retention (still using after 1 month)
- Churn rate (% who stop using monthly)

**Calculate:**
```
Day 1 retention: Users active on day N+1 / Users active on day N

Example: 100 users signup Monday. 40 come back Tuesday = 40% D1 retention.

Typical benchmarks (be honest):
- B2C free: 20-30% D1, 5-10% D7, 2-3% D30
- B2B SaaS: 60-80% D1, 40-50% D7, 20-40% D30
- Marketplace: 30-50% D1, 10-20% D7, 5-10% D30
```

**Churn calculation (monthly):**
```
Users lost in month / Starting users = Monthly churn

Example: Started with 500 users, ended with 425 = 15% monthly churn
Sustainable churn: <5% monthly (losing 5% of users, but gaining >5% in new users)
```

**Red flag:** <20% D1 retention = core experience is broken. Even if features are cool, if people don't come back immediately, something is wrong.

### 4. Revenue (Are people paying?)

**Key questions:**
- How many customers are paying?
- What's average revenue per user (ARPU)?
- How much are we making monthly (MRR)?

**Calculate:**
```
MRR = Sum of all recurring revenue from paid customers

ARPU = Total MRR / Total customers (paying + free)

Payback period = CAC / Monthly profit per customer
Example: $25 CAC, $10 profit per customer = 2.5 months payback (need <12 months to be sustainable)
```

**Pricing feedback:**
- Is anyone actually buying?
- Did you test pricing with customers before launch?
- Are you leaving money on the table (customers want to pay more)?
- Is price the only objection to buying?

### 5. Referral (Are happy users telling others?)

**Key questions:**
- What % of new users come from existing users?
- What's your viral coefficient (how many new users does each customer bring)?

**Calculate:**
```
Viral coefficient = (# of invites sent per user) × (% who accept invite)

Example: Average user sends 3 invites, 20% accept = 0.6 viral coefficient
(Sustainable growth: >1.0 means exponential growth; <1.0 means you need paid acquisition)
```

**Signals of viral potential:**
- "Can't help mentioning this to friends" (organic word-of-mouth)
- Product naturally creates reason to share (invite link, collab, sharing results)
- Strong NPS (Net Promoter Score) — ask "how likely to recommend?" (0-10 scale)

## Output: METRICS-REPORT.md

Format:

```
# Metrics Review Report

## Review Period
[Dates after launch] — [Today]

## Acquisition

| Metric | Target | Actual | Status |
|--------|--------|--------|--------|
| Total users | [Lean canvas prediction] | [X] | G/Y/R |
| CAC (blended) | [Budget/assumption] | $[X] | G/Y/R |
| CAC payback period | <12 months | [X months] | G/Y/R |

### By Channel
[Table of channels with users, spend, CAC]

**Analysis:**
[What worked? What didn't? Why?]

## Activation

| Metric | Target | Actual | Status |
|--------|--------|--------|--------|
| Signup to critical action % | [Lean canvas] | [X%] | G/Y/R |

**Activation rate interpretation:**
- [Your rate] means [what it actually means to users]
- Diagnosed blockers: [Friction points preventing users from getting value]
- Fix priority: [What needs to change immediately?]

## Retention

| Metric | Target | Actual | Status |
|--------|--------|--------|--------|
| Day 1 retention | [Industry benchmark] | [X%] | G/Y/R |
| Day 7 retention | [Industry benchmark] | [X%] | G/Y/R |
| Day 30 retention | [Industry benchmark] | [X%] | G/Y/R |
| Monthly churn rate | <5% | [X%] | G/Y/R |

**Retention analysis:**
[Why are people staying or leaving? What's the feature they come back for?]

## Revenue

| Metric | Target | Actual | Status |
|--------|--------|--------|--------|
| Paying customers | [Prediction] | [X] | G/Y/R |
| MRR | $[Prediction] | $[X] | G/Y/R |
| ARPU | $[Prediction] | $[X] | G/Y/R |
| Payback period | <12 months | [X months] | G/Y/R |

**Revenue findings:**
[Are you charging? Is pricing right? Do customers see value?]

## Referral

| Metric | Target | Actual | Status |
|--------|--------|--------|--------|
| % new users from referral | [Prediction] | [X%] | G/Y/R |
| Viral coefficient | >1.0 | [X] | G/Y/R |
| NPS (recommend likelihood) | [Target] | [Score] | G/Y/R |

**Virality assessment:**
[Do users love it enough to tell others? Or is it just a tool they tolerate?]

## The Hard Truth

**Biggest surprise:**
[What didn't go as planned?]

**Biggest win:**
[What exceeded expectations?]

**Most critical fix (next 30 days):**
[The one metric that must improve or the company dies]

## Lean Canvas vs Reality

| Assumption | Lean Canvas | Reality | Variance |
|-----------|------------|---------|----------|
| [Assumption 1] | [Prediction] | [Actual] | [Analysis] |
| [Assumption 2] | [Prediction] | [Actual] | [Analysis] |

## Path Forward

**1. Double down on:**
[What's actually working? Invest more here.]

**2. Fix urgently:**
[What's broken and killing growth?]

**3. Kill or defer:**
[What isn't working and isn't core?]

**4. Next metric to focus on:**
[Pick one. Don't optimize everything at once.]

## Founder's Honest Assessment

[Your take: Are we on track? Ahead? Behind? What needs to change?]
```

Remember: Bad metrics are actually valuable information. They tell you where to focus. The only useless metric is one you ignore.
