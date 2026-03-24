---
name: metrics-review
description: Post-launch honest measurement of AARRR metrics. Acquisition, Activation, Retention, Revenue, Referral. Compares against lean canvas. No spinning bad numbers. "3% activation = emergency."
benefits-from: lean-canvas
feeds-into: growth-playbook, customer-feedback
---

# Metrics Review

After launch, measure ruthlessly. Don't spin bad numbers — understand them and fix the root cause.

---

## Phase 0: Grounding and Setup

**Purpose:** Understand what we're measuring, gather sources of truth

**Exit criteria:** You have identified all data sources (analytics, payment processor, usage logs) and access to LEAN-CANVAS.md predictions

### What This Skill Does

You're going to collect real data from your product and compare it to what you predicted before launch. This isn't about making yourself look good — it's about understanding exactly what's working and what's broken so you can fix the broken parts.

**Key principle:** Bad metrics are valuable. They tell you where to focus. The only useless metric is one you ignore.

---

## Phase 1: Gather All Metrics (One Question at a Time)

Use **AskUserQuestion** for each metric category. One question per answer.

### Question 1A: Acquisition Data Sources

**Re-ground:** We're reviewing your post-launch metrics. Phase 1 is gathering the raw data.

**Simplify:** We need to understand where your first customers came from and how much it cost to get them. Think of it as tracking which fishing holes caught the most fish, and how much you spent per fish.

**Recommend:** List every channel that brought users (Product Hunt, Twitter, ads, friends, etc.) with real numbers if you have them.

**Options:**

A) I have detailed analytics by channel (GA, Mixpanel, custom tracking) with spend data
B) I have rough estimates for channels and some spend data, but it's not complete
C) I'm still tracking this — don't have organized numbers yet
D) I have no idea where users came from

**If user chooses D:** "That's a crisis. We need to solve this immediately. Without knowing where users come from, every marketing decision is a guess. Let's audit your data sources first before we continue."

---

### Question 1B: Activation Data

**Re-ground:** We're on Acquisition. Now moving to Activation — tracking what % of users actually get value.

**Simplify:** Of everyone who signed up, how many completed the core action that shows they got value? For a note-taking app, that's "created first note." For a CRM, it's "created first contact." This number determines if your product works.

**Recommend:** Define the critical action — the one thing users must do to realize value.

**Options:**

A) I know exactly which action = activation and have the % who completed it
B) I have some data but I'm not sure if I'm measuring the right action
C) I haven't defined what "activation" means yet
D) I'm not tracking this at all

**If user chooses C:** "This is your emergency metric. Until you know what % of users get value, you're flying blind. Let's define it now."

---

### Question 1C: Retention Data

**Re-ground:** Activation is sorted. Now Retention — do people come back?

**Simplify:** You need three numbers: % who came back after 1 day, 1 week, and 1 month. These tell you if the product is actually sticky or if it's a one-time thing.

**Recommend:** Pull Day 1, Day 7, Day 30 retention. If you have churn rate by month, that's even better.

**Options:**

A) I have D1, D7, D30 retention from my analytics
B) I have some retention data but it's incomplete
C) I'm not tracking retention yet
D) Users don't really "come back" — it's more continuous usage

**If user chooses D:** "OK, then what's your engagement metric? Daily active users? Time spent per week? We need something to measure stickiness."

---

### Question 1D: Revenue Data

**Re-ground:** Retention captured. Now Revenue — is anyone actually paying?

**Simplify:** We need to know: how many customers are paying, how much per month (MRR), and whether this economics make sense long-term.

**Recommend:** Get your payment processor data (Stripe, etc.) and calculate total MRR.

**Options:**

A) I have MRR, customer count, and breakdown of paying vs free
B) I have some revenue numbers but they're fuzzy
C) I have zero revenue yet
D) Revenue is complicated in my model (usage-based, tiered, free trial, etc.)

**If user chooses D:** "That's fine. Just translate it into a monthly equivalent. Usage-based? Tell me average monthly spend per customer."

---

### Question 1E: Referral Data

**Re-ground:** Revenue captured. Final metric: Referral — are happy users telling others?

**Simplify:** What % of your new users came because an existing user told them about you? This determines if your growth is sustainable or if you're always hunting for customers.

**Recommend:** Check your analytics for "source = referral" or ask customers directly "who told you about us?"

**Options:**

A) I can track referral rate from my analytics
B) I know roughly what % is referral vs new
C) I have no idea, but I can ask customers
D) Referral doesn't really apply to my product

---

## Phase 2: Deep Analysis of AARRR Metrics

### Question 2A: Acquisition Bottleneck?

**Re-ground:** We have the raw data. Phase 2 is diagnosing what the numbers mean.

**Simplify:** Your CAC (cost per customer) tells you if your acquisition is sustainable. If you spent $5K and got 100 users, that's $50 CAC. Is it worth it?

**Recommend:** Calculate CAC by channel. Which channels are actually efficient?

**Options:**

A) My CAC is under $20 across all channels — looks good
B) My CAC is $20-50 per channel — sustainable but could improve
C) My CAC is over $50 — expensive, needs optimization
D) I have free channels only (Product Hunt, organic) — CAC is $0

**If A or D:** "Good. Now the question is: can you scale it? Free channels are often one-time. What's your plan for repeat acquisition?"

**If B:** "Solid foundation. Let's look at retention — are these users worth the cost? If D30 retention is 3%, your CAC doesn't matter."

**If C:** "This is a problem. Your payback period is likely >12 months. Before you spend more on acquisition, fix activation and retention first."

---

### Question 2B: Activation Crisis Check

**Re-ground:** Acquisition assessed. Activation is where 90% of startups fail.

**Simplify:** Your activation rate tells you if the product works. >40% is exceptional. <10% is an emergency (meaning 90% of users try and leave immediately).

**Recommend:** What's your activation rate?

**Options:**

A) Activation is >40% — excellent, top 10% of products
B) Activation is 20-40% — acceptable, but fixable
C) Activation is 10-20% — we have a real problem
D) Activation is <10% — emergency, users don't get value

**If D:** "This is your fire. Everything else pauses. Why do 90% of users try and leave? Is onboarding confusing? Does the core feature not work? We need to diagnose this in the next conversation."

**If C:** "Clear problem, but solvable. What do you think the friction point is? Onboarding? Feature doesn't work as advertised? Value takes too long?"

**If A or B:** "Good sign. Let's keep moving through the metrics."

---

### Question 2C: Retention Benchmark

**Re-ground:** Activation is clear. Now Retention — do people actually use this repeatedly?

**Simplify:** Compare your actual D1, D7, D30 retention to industry benchmarks. If you're a B2C free app and you have 15% D1 retention, that's low. If you're B2B SaaS and you have 60% D1, that's expected.

**Recommend:** What's your actual D7 retention? (This is the most telling metric)

**Options:**

A) D7 retention is >40% — strong retention, product is sticky
B) D7 retention is 20-40% — acceptable, needs improvement
C) D7 retention is 10-20% — weak, users aren't finding value repeatedly
D) D7 retention is <10% — broken, almost nobody comes back

**If D or C:** "This is the second-order crisis. Even if acquisition is good, if people don't stay, you're leaking money. What's the feature they DON'T use on day 7?"

---

### Question 2D: Revenue Model Reality

**Re-ground:** Retention assessed. Now Revenue — is the business sustainable?

**Simplify:** You need to know payback period: How many months of profit per customer until you break even on the CAC? If it's >12 months, the economics don't work.

**Recommend:** What's your payback period (CAC divided by monthly profit per customer)?

**Options:**

A) Payback period is <6 months — excellent unit economics
B) Payback period is 6-12 months — good but tight
C) Payback period is >12 months — unsustainable long-term
D) Can't calculate yet (no revenue or unclear unit economics)

---

## Phase 3: Compare to Lean Canvas Predictions

### Question 3A: Major Surprises

**Re-ground:** We have the actuals. Phase 3 is comparing to what you predicted.

**Simplify:** Look at your LEAN-CANVAS.md. You made assumptions about how many users you'd get, what activation would be, etc. Which assumptions were wildly wrong?

**Recommend:** What was your biggest surprise — something that underperformed or outperformed your predictions?

**Options:**

A) One metric massively outperformed (users 2x what we predicted)
B) One metric massively underperformed (activation is 50% of prediction)
C) Everything is roughly on track
D) Results are all over the place, no clear pattern

---

## Phase 4: Output Generation

### Question 4A: Prepare Report

**Re-ground:** We've analyzed everything. Phase 4 is turning this into a decision-making document.

**Simplify:** I'm going to build a METRICS-REPORT.md that shows your actual vs predicted numbers, with honest analysis of what to fix next.

**Recommend:** Ready to finalize the report?

**Options:**

A) Yes, generate the full report
B) Wait, I have more data to add first
C) I want to focus on the biggest problem first

**If C:** "Smart. Which metric is the emergency: Acquisition, Activation, Retention, or Revenue?"

---

## AARRR Metrics Deep Dive (Reference)

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

---

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

---

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

---

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

---

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

---

## Output Template: METRICS-REPORT.md

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

---

## Completion Status

When you've finished:

- [ ] Gathered all AARRR metrics from actual data sources
- [ ] Compared actuals to LEAN-CANVAS predictions
- [ ] Generated METRICS-REPORT.md with honest analysis
- [ ] Identified the one critical metric to fix next
- [ ] Shared report with co-founders / advisors for reality check

**Exit with:** DONE | DONE_WITH_CONCERNS | BLOCKED | NEEDS_CONTEXT

---

## Key Principle

Bad metrics are actually valuable information. They tell you where to focus. The only useless metric is one you ignore.
