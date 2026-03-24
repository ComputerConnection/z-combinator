---
name: customer-feedback
description: Aggregates and analyzes early customer feedback from all sources. Top 5 feature requests (frequency + value), top 5 complaints, churn reasons, NPS estimate, desperate users. Understand "nice to have" vs "I'll leave if you don't fix."
---

# Customer Feedback Aggregator

Collect feedback from every source: emails, support tickets, user interviews, Twitter, Discord, in-app surveys. Your job is to synthesize it into actionable priorities.

## What You Do

1. Gather all feedback sources:
   - Support emails and tickets
   - User interviews (1-1 calls)
   - In-app feedback widgets or surveys
   - Social media mentions
   - Discord/Slack community
   - Product review sites
   - Support Intercom/Zendesk/Freshdesk
2. Read through everything. Don't sample — read all of it.
3. Tag feedback by category:
   - Feature request (want something new)
   - Complaint (something broken or bad)
   - Churn reason (why they left)
   - Praise (what they love)
4. Identify "desperate users" — people for whom your product solves a critical pain
5. Distinguish between "nice to have" (would be cool) and "I'll leave if you don't fix" (must-have)
6. Calculate NPS (Net Promoter Score) from sentiment if available

## Feature Requests: Frequency + Value Analysis

Don't just count. Evaluate impact.

```
Frequency = How many customers asked for this?
Value = How much would this matter to their business/workflow?
Effort = How hard is it to build?

Priority Score = Frequency × Value / Effort

High priority: High frequency + high value + lower effort
Low priority: Low frequency OR low value
```

Example:
- Request: "Dark mode" (5 customers asked) × (nice to have) / (2 days) = Lower priority
- Request: "Bulk export" (12 customers asked) × (saves 5 hours/month) / (3 days) = Higher priority
- Request: "API access" (8 enterprise customers asked) × (blocks deals) / (2 weeks) = Highest priority (different tier)

## Top 5 Feature Requests

Rank by (Frequency × Business Impact) / Effort

| # | Feature | # asking | Impact | Blocker? | Effort | Status |
|---|---------|----------|--------|----------|--------|--------|
| 1 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |
| 2 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |
| 3 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |
| 4 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |
| 5 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |

**Key distinction:**
- "Nice to have": Customers would like it, but won't leave without it
- "Blocker": Without this, customers can't use your product for their core need
- "Deal killer": This is preventing them from paying or referring others

## Top 5 Complaints (Most Painful Issues)

Rank by severity and impact

| # | Issue | # complaining | Severity | Impact | Workaround? |
|---|-------|---------------|----------|--------|-------------|
| 1 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |
| 2 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |
| 3 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |
| 4 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |
| 5 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |

## Churn Reasons

Why are people leaving?

```
Segment by churn reason:
- [Reason 1]: [# customers] [Example quote]
- [Reason 2]: [# customers] [Example quote]
- [Reason 3]: [# customers] [Example quote]

Pattern: Is there a common thread? (price, missing feature, performance, support)
```

## Desperate Users

These are your most important customers. Identify people for whom your product is *essential*.

```
Desperate user signals:
- "I would be devastated if this disappeared"
- "I've built my workflow around this"
- "I've convinced my team to use it"
- "I'm paying for this even though it's early"
- "I tell people about this constantly"

List desperate users:
1. [Name/company] — [Why they're desperate] — [What they'd use it for]
2. [Name/company] — [Why they're desperate] — [What they'd use it for]
...

Why this matters: These users are your product advisors and potential case studies. If they leave, you've lost your north star.
```

## NPS Estimate (from sentiment)

If you've asked "How likely to recommend?" on a 0-10 scale:

```
NPS = (% Promoters 9-10) - (% Detractors 0-6)

Industry benchmarks:
- Below 0: You're in trouble
- 0-30: Acceptable
- 30-50: Good
- 50+: Excellent (rare for early products)

Typical early startup: 20-40 if you have product-market fit signals
```

If you haven't asked explicitly, estimate from tone:

```
Enthusiastic feedback (9-10 language): "I love this, tell my friends"
Satisfied feedback (7-8 language): "This is useful, but..."
Neutral (6 language): "It works"
Critical (0-5 language): "This is broken" or "I'm leaving"
```

## Output: CUSTOMER-FEEDBACK.md

Format:

```
# Customer Feedback Report

## Summary
- Total feedback collected: [N sources, M pieces of feedback]
- Response rate: [% of customers who gave feedback]
- Compilation date: [Today]

## Top 5 Feature Requests

[Table from above with ranking]

### Request #1: [Feature Name]
**Why it matters:** [Business impact. Who needs it and why?]
**Quotes:**
- [Customer quote 1]
- [Customer quote 2]

**Our assessment:** [Will we build this? When? Why/why not?]

### Request #2: [Feature Name]
[Same format]

...

## Top 5 Complaints

[Table from above with severity]

### Complaint #1: [Issue]
**Who complained:** [# of customers and severity]
**Quotes:**
- [Customer quote]

**Impact:** [What does this break?]
**Workaround:** [Do we have one?]
**Fix status:** [Are we fixing? Timeline?]

### Complaint #2: [Issue]
[Same format]

...

## Churn Analysis

**Why people are leaving:**
- [Reason 1]: [# customers] [Example quote]
- [Reason 2]: [# customers] [Example quote]

**Pattern:** [Is there a common theme?]

**Prevention strategy:** [What do we do about it?]

## Desperate Users (Our North Stars)

These customers would be devastated if we disappeared. They're using us for critical work.

| Name/Company | Core Use Case | Why Desperate | Next action |
|--------------|---------------|---------------|-------------|
| [User] | [How they use product] | [Why essential to them] | [Get case study / deeper feedback / etc] |
| [User] | [How they use product] | [Why essential to them] | [Get case study / deeper feedback / etc] |

## NPS & Sentiment

**Estimated NPS:** [Score]
- [X]% Promoters (9-10): "I love this and tell people"
- [X]% Passive (7-8): "It's useful, but..."
- [X]% Detractors (0-6): "Disappointed / leaving"

**Sentiment trend:** [Improving / Stable / Declining]

## What NOT to Build (Yet)

Requests that sound cool but don't move the needle:
- [Request]: [Why it's lower priority]
- [Request]: [Why it's lower priority]

Keep a backlog for later, but don't distract yourself. Focus on the must-haves.

## Key Insights

**1. Biggest win in feedback:** [What are people happiest about?]

**2. Biggest problem:** [What's hurting adoption/retention?]

**3. Most surprising feedback:** [What did we learn that contradicts our assumptions?]

**4. One thing to fix this sprint:** [The single issue or request that matters most right now]

## Action Items

| Item | Priority | Owner | Timeline |
|------|----------|-------|----------|
| [Feature/fix] | P0 | [Person] | [Date] |
| [Feature/fix] | P1 | [Person] | [Date] |
| [Feature/fix] | P2 | [Person] | [Date] |

## Follow-up Interviews

List customers you need to talk to deeper:
- [Name/company] — [Question to ask]
- [Name/company] — [Question to ask]
```

Key principle: "Nice to have" requests don't kill you. Missing a must-have does. Your job is to know the difference.
