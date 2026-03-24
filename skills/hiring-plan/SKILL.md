---
name: hiring-plan
description: When to hire, who, and why. Bottleneck analysis, first 3 hires with job profiles, compensation benchmarking, cultural values with behavioral examples, interview question bank. Warns against mistakes like hiring VP Sales with 10 customers.
---

# Hiring Plan

Hiring too early kills startups. Hiring too late leaves money on the table. This is the analysis to do it right.

## What You Do

1. Read METRICS-REPORT.md to understand current traction
2. Read LEAN-CANVAS.md to understand growth strategy
3. Identify the bottleneck — what constrains growth?
4. Determine if the bottleneck is people (yes, hire) or process (no, fix it first)
5. Recommend first 3 hires with specific profiles
6. Define compensation with market benchmarks
7. Document cultural values with behavioral examples (not platitudes)
8. Build interview question bank
9. Flag common hiring mistakes

## Bottleneck Analysis

What's stopping you from growing?

```
Is it:
- Engineering: "Product has bugs, we can't ship fast enough"? → Hire engineer
- Sales: "We have demand but can't close fast enough"? → Hire sales person
- Customer support: "Users are churning from bad support"? → Hire CS
- Product/Design: "Users don't understand the product"? → Better design/product

If it's a PROCESS problem disguised as people:
- "We can't ship fast" — Maybe your architecture is broken, not your engineering
- "We can't close deals" — Maybe your sales process is broken, not your sales
- "Users are confused" — Maybe your onboarding sucks, not your design skills

Fix process first. Hiring won't solve broken systems.
```

**Decision tree:**
```
Do you have >100 customers?
  No → You don't need most hires yet. Focus on founder doing everything.
  Yes → Is growth constrained by a specific function?
    No → Build better systems first
    Yes → Hire for that function
```

## First 3 Hires: When and Who

### Hire #1: Usually an Engineer (if you're not technical co-founder)

**When:** 50+ paying customers OR $5K+ MRR
**Why:** Product work accelerates. You need someone who can ship features while you sell/recruit

**Job Profile:**

```
Title: Senior Engineer (full-stack or backend, depending on product)

Background needed:
- Built products at [stage] before (Series A startup, scale-up, or senior IC at bigger company)
- NOT a fresh bootcamp grad (unless you have experienced co-founder to mentor)
- Has opinions about tech decisions (can push back on overengineering)

Compensation (SF market):
- Salary: $150-180K
- Equity: 0.5-1.0% (not 0.1%)
- Bonus: 10-20%

Why this person:
- Can mentor junior engineers if you hire more
- Understands startup constraints (move fast, pragmatism)
- Won't waste months on architecture porn

Red flags:
- "I want to use Rust/Elixir/etc for this" (wrong person for MVP mode)
- Wants to rewrite everything
- Obsessed with perfect code, not shipping code
```

### Hire #2: Usually Sales or BD (if you've proven product-market fit)

**When:** $5K+ MRR with >20% paying customers
**Why:** You can't sell forever. Hiring sales person frees you to build/raise

**Job Profile:**

```
Title: Account Executive or Business Development Lead

Background needed:
- Sold B2B SaaS before (understands sales cycle)
- Comfortable with early-stage rejection rate (50-70% of outreach converts to meetings, 5-10% of meetings close)
- NOT a "VP of Sales" (you have 10 customers, not 100 deals in pipeline)

Compensation:
- Salary: $80-120K (lower than engineer, but...)
- Commission: 10-15% of deals they close
- Ramp: 3 months to productive (slow at first, then ramp)

Why this person:
- Closes deals faster than you would
- Gives feedback on positioning from customers
- Won't get demoralized by early-stage sales reality

Red flags:
- "I expect a management team immediately" (you have 10 customers, not 100)
- Wants commission only, no salary (won't work, needs to eat)
- Never sold at this deal size before (big company sales ≠ startup sales)
```

### Hire #3: Usually Customer Success or Product

**When:** >100 customers or shipping product becomes bottleneck
**Why:** Support/onboarding scales exponentially. Product roadmap management becomes critical

**Job Profile:**

```
Title: Customer Success Manager (if support is bottleneck)
        OR Product Manager (if shipping is bottleneck)

Customer Success:
- Compensation: $90-120K salary + small bonus
- Background: Managed customer relationships at SaaS company
- Why: Reduces churn, improves activation, finds feature requests

Product Manager:
- Compensation: $120-150K + equity 0.25-0.5%
- Background: Worked as PM or senior designer at startup
- Why: Owns roadmap, prioritization, talks to customers regularly
```

## Compensation Benchmarking

**By role and stage (SF/NYC - adjust down 20-30% for non-tech hubs):**

| Role | Startup stage | Salary | Equity | |
|------|---------------|--------|--------|---|
| Engineer | Pre-seed/Seed | $130-160K | 0.5-1% | 1st-2nd engineer |
| Engineer | Seed | $150-180K | 0.25-0.5% | 3rd+ engineer |
| Sales | Seed | $80-120K | 0.25-0.5% + 10% commission | 1st sales |
| CS/Support | Seed | $70-100K | 0.15-0.25% | 1st CS hire |
| PM | Seed | $120-150K | 0.25-0.5% | 1st PM (if you're not the PM) |

**Equity rules:**
- Don't give away >15-20% before Series A (you need room for future employees)
- Early stage = higher %age, lower salary
- Each subsequent hire of same role = lower equity
- First engineer gets more than 5th engineer

## Cultural Values (Behavioral, Not Platitudes)

Don't say "we value transparency." Say what it means:

```
VALUE: Speed > Perfection

Behavioral example:
- Launches feature with 80% design quality rather than waiting for perfection
- Ships with tech debt if it unlocks customer value
- Questions 2-week project timelines that could be 1 week

Not this behavior:
- Demands perfect code before shipping
- Opposes "MVP mindset"

---

VALUE: Bias toward action

Behavioral example:
- Tests assumption with customer before debating in meetings
- Makes decision with 70% information if waiting costs time
- Asks "what can we learn?" before saying "that won't work"

Not this behavior:
- Analysis paralysis (endless debating)
- Waiting for perfect data before acting

---

VALUE: Customer obsession (if true)

Behavioral example:
- Talks to 5+ customers monthly
- Remembers individual customer frustrations, not abstract "segments"
- Pushes back on feature requests if customer doesn't validate pain

Not this behavior:
- Ignores feedback because "we know better"
- Treats customers as account numbers

---

VALUE: No ego, high feedback tolerance

Behavioral example:
- Openly says "I was wrong" or "I don't know"
- Asks for feedback regularly
- Pivots based on evidence, not pride

Not this behavior:
- Defensive when questioned
- Doubles down on bad decisions to save face
```

## Interview Question Bank

**For engineers:**
1. "Tell me about a product you shipped that you're proud of. What was your role? What would you do differently?"
2. "We have [X] paying customers. Our API response is [Yms]. Should we optimize? Why/why not?"
3. "Describe a time when you disagreed with your manager on technical approach. How was it resolved?"
4. "What's your biggest pet peeve about code/systems? Tell me about a time you fixed it."
5. "You see a customer complaint about performance. How do you prioritize this vs other work?"

**For sales:**
1. "Tell me about your hardest close. How did you do it? How long did it take?"
2. "We're a [stage] startup with [product]. Who's our ideal customer? Who's hardest to sell to?"
3. "You call a prospect. They say 'no thanks, we use [competitor].' What do you do?"
4. "What's your close rate? How long is sales cycle? What's your average deal size?"
5. "Tell me about a deal you lost. Why? What would you do differently?"

**For CS:**
1. "Customer is angry their feature request isn't prioritized. How do you respond?"
2. "You notice 40% of new signups don't activate. What do you investigate?"
3. "Tell me about a customer you saved from churning. How?"
4. "How do you decide if something is a bug or user error?"

**For everyone:**
1. "Why this startup? What attracted you?"
2. "What scares you about early-stage? How do you handle ambiguity?"
3. "Tell me about a time you failed. What did you learn?"

## Common Hiring Mistakes (And Why They Kill You)

### Mistake 1: "We'll hire a VP of Sales when we have 10 customers"

**Why it fails:**
- VP of Sales manages salespeople and process (you have neither)
- VPs want titles and teams
- You need someone who closes deals with their own hands

**Fix:** Hire Account Executive or Sales person who sells AND manages themselves

### Mistake 2: "Let's hire a PM so we can stop talking to customers"

**Why it fails:**
- Early stage, you (founder) ARE the PM
- Hiring PM before you have proof of product-market fit = hiring overhead
- PM can't make decisions about your product better than you (yet)

**Fix:** Hire PM when you have >500 customers or shipping becomes bottleneck

### Mistake 3: "Hire junior developers to save money"

**Why it fails:**
- You don't have time to mentor
- Junior dev generates technical debt faster
- You pay for it later in slowdown

**Fix:** Hire 1 strong senior engineer, not 2-3 juniors

### Mistake 4: "Hire contractor/part-time to save costs"

**Why it fails:**
- Part-time people get less context
- Contractor loyalty is weak
- You can't move fast with part-time

**Fix:** Full-time employee. If you can't afford it, don't hire yet.

### Mistake 5: "Hire your friend because it's easier"

**Why it fails:**
- Working with friends = relationship risk if it doesn't work out
- Lower performance standard because friendship
- Will you fire them if they're not working? Doubt.

**Fix:** Hire best person regardless of friendship

## Output: HIRING-PLAN.md

Format:

```
# Hiring Plan

## Current State
- Revenue: $[X] MRR
- Customers: [X]
- Team: [You describe team: "2 co-founders, full-time"]
- Runway: [X months]

## Bottleneck Analysis

**Current constraint:** [What stops growth?]
- Evidence: [Metrics showing this is the bottleneck]
- Is it people or process? [People = hire, Process = fix it]

**Decision:** [Do we need to hire right now?]

## Hiring Timeline

**Next 90 days:** [Hire #1 or wait for more traction?]
**Months 4-6:** [Hire #2]
**Months 7-12:** [Hire #3]

[Alternative timeline if traction accelerates or decelerates]

## Hire #1: [Role]

**When:** [Trigger: MRR / customers / timeline]
**Why:** [Problem this person solves]

**Job Profile:**
- Title: [Exact title]
- Salary: $[X]
- Equity: [X]%
- Background: [Experience needed]
- Key traits: [What they must be good at]

**Interview process:**
1. [Phone screen topics]
2. [Technical/task evaluation]
3. [Culture fit interview]
4. [Reference calls]

## Hire #2: [Role]

[Same format]

## Hire #3: [Role]

[Same format]

## Compensation Summary

| Role | Salary | Equity | Rationale |
|------|--------|--------|-----------|
| [Hire #1] | $[X] | [X]% | [Why this person is worth it] |
| [Hire #2] | $[X] | [X]% | [Why this person is worth it] |
| [Hire #3] | $[X] | [X]% | [Why this person is worth it] |

## Cultural Values

[For each value: behavioral examples]

## Red Flags to Avoid

1. [Mistake 1]: [Why it kills startups]
2. [Mistake 2]: [Why it kills startups]
3. [Mistake 3]: [Why it kills startups]

## Interview Question Bank

[Organized by role]

## Onboarding Plan (First 30 days)

- Week 1: [What does new hire learn?]
- Week 2: [First shipping goal?]
- Week 3: [Independent project?]
- Week 4: [Full productivity?]

## Sign-off

Before hiring, answer:
- [ ] Is this person solving the real bottleneck?
- [ ] Do we have runway to afford them?
- [ ] Can we commit to mentoring/feedback?
- [ ] Will this person level up the team?

If no to any: Don't hire yet.
```

Remember: Early hires make or break a startup. Hire slow, hire right. A bad early hire costs 10x more than waiting 3 months for the right person.
