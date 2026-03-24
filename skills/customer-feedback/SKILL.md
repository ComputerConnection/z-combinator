---
name: customer-feedback
description: Aggregates and analyzes early customer feedback from all sources. Top 5 feature requests (frequency + value), top 5 complaints, churn reasons, NPS estimate, desperate users. Understand "nice to have" vs "I'll leave if you don't fix."
benefits-from: metrics-review
feeds-into: growth-playbook, hiring-plan
---

# Customer Feedback Aggregator

Collect feedback from every source: emails, support tickets, user interviews, Twitter, Discord, in-app surveys. Your job is to synthesize it into actionable priorities.

---

## Phase 0: Grounding and Setup

**Purpose:** Identify all feedback sources and confirm access

**Exit criteria:** You have inventory of all places where customer feedback lives

### What This Skill Does

You're going to listen to what customers actually say — not what you think they say. Then rank their requests by whether they'll leave if you don't fix it (must-have) vs nice-to-have. This determines what you build next.

**Key principle:** "Nice to have" requests don't kill you. Missing a must-have does. Your job is to know the difference.

---

## Phase 1: Locate All Feedback Sources (One Question at a Time)

Use **AskUserQuestion** for each source.

### Question 1A: Email and Support Channels

**Re-ground:** We're collecting customer feedback from all sources. Phase 1 is finding where the feedback lives.

**Simplify:** Think of it like fishing — we need to know all the fishing holes where customer opinions live. Email, support tickets, Discord, Twitter, in-app surveys, etc.

**Recommend:** Start with the obvious channels that have recorded conversations.

**Options:**

A) I have support tickets (Zendesk/Intercom/Freshdesk) with hundreds of customer interactions
B) I have email threads with customers but they're scattered
C) I have a mix of channels but no good central place for feedback
D) I'm doing direct calls and taking notes, but nothing automated

**If A:** "Perfect. Those tickets are our source of truth. We'll pull feedback from there."

**If B or C:** "OK, we'll need to consolidate. Do you have time to export these into one document?"

---

### Question 1B: Interview and Research Data

**Re-ground:** Support tickets captured. Now: interview notes.

**Simplify:** One-on-one calls with customers are gold. They tell you the *why* behind feature requests. What interview data do you have?

**Recommend:** List any customer interview recordings, transcripts, or detailed notes.

**Options:**

A) I have 10+ customer interviews with notes/recordings
B) I have 3-5 interviews with some notes
C) I have a few ad-hoc conversations but nothing formal
D) I haven't done customer interviews yet

**If D:** "You need to fix this immediately. Feedback from support is reactive. Interviews let you hear the *why*. Can you do 5 quick calls this week?"

---

### Question 1C: Social and Community

**Re-ground:** Formal feedback sources captured. Now: social/community signals.

**Simplify:** Where do customers hang out? Twitter? Discord? Product Hunt comments? Reddit? This feedback is less filtered — you see raw emotion.

**Recommend:** Which social channels have meaningful customer conversation?

**Options:**

A) Twitter mentions, Product Hunt discussions, and/or active Discord
B) Reddit or niche community forums
C) A little bit of social noise but nothing organized
D) No social presence / no community

---

### Question 1D: In-App Feedback

**Re-ground:** External sources captured. Now: in-app signals.

**Simplify:** Do users have a way to leave feedback inside your product? Those responses are gold — users take 5 seconds to tell you they're frustrated.

**Recommend:** Any in-app feedback widget, NPS surveys, or feature request buttons?

**Options:**

A) Yes, I have an in-app feedback widget with responses
B) I ask for feedback sometimes but it's not systematic
C) No in-app feedback mechanism yet
D) Users email me but I don't have a formal channel

---

## Phase 2: Read All Feedback (No Sampling!)

### Question 2A: Confidence in Complete Data

**Re-ground:** We've identified all sources. Phase 2 is making sure we've read EVERYTHING, not just sampling.

**Simplify:** Bad samples bias you. If you only read the angry emails, you miss the happy ones. We need to make sure you've gone through all the data.

**Recommend:** Have you reviewed all feedback from the past 3 months end-to-end?

**Options:**

A) Yes, I've read through all of it and taken notes on themes
B) I've skimmed most of it but probably missed some
C) No, it's too much data — I've only read a sample
D) I'm going to do this now; I haven't reviewed it yet

**If A:** "Good. Now let's extract the patterns."

**If C:** "We need to do this right. Sampling biases your product roadmap. Can you block 2-3 hours to read through everything?"

---

## Phase 3: Tag and Categorize Feedback

### Question 3A: Feature Request Themes

**Re-ground:** We've read all the feedback. Phase 3 is organizing it into themes.

**Simplify:** Group similar requests together. If 12 customers asked for "bulk export" and 3 asked for "dark mode," that's a pattern. Which feature request shows up the most?

**Recommend:** What are the top 5 feature requests you're hearing repeatedly?

**Options:**

A) I can list clear top 5 with number of customers asking for each
B) I have some repeated requests but not a clean ranking
C) It's all over the place — hard to see patterns
D) Most customers want different things (no clear pattern)

**After user answers, ask:** For each request, how many customers asked? And for each — would they leave if you don't build it, or is it nice-to-have?

---

### Question 3B: Complaint Themes

**Re-ground:** Feature requests captured. Now: complaints.

**Simplify:** Complaints are different from feature requests. These are things that are BROKEN or PAINFUL. "Your upload is slow" or "onboarding is confusing." What are the top complaints?

**Recommend:** What's frustrating your customers right now?

**Options:**

A) I have clear top 5 complaints with severity levels
B) I have some pain points but they're mixed with feature requests
C) Hard to tell what's truly painful vs just nitpicking
D) Mostly positive feedback; not many complaints

**After user answers, ask:** For each complaint, what's the impact? Does it prevent them from using the product, or just slow them down?

---

### Question 3C: Churn Signals

**Re-ground:** Complaints captured. Now: who's leaving?

**Simplify:** When customers cancel or stop using you, do they tell you why? That's pure gold. Churn reasons tell you what to fix before it kills you.

**Recommend:** Do you know why customers are churning?

**Options:**

A) Yes, I ask at cancellation and have documented reasons
B) I have some clues but nothing systematic
C) I don't know — customers just disappear
D) Not enough churn yet to see patterns

**If C:** "You need to fix this. Add a one-question cancellation survey. 'What could we have done to keep your business?' That one answer is worth more than any focus group."

---

### Question 3D: "Desperate User" Identification

**Re-ground:** Churn reasons captured. Now: identify your power users.

**Simplify:** Some customers don't just like your product — they'd be devastated if it disappeared. They've built their workflow around it. These are your north stars. Who are they?

**Recommend:** Can you name 3-5 customers who'd be heartbroken if you shut down?

**Options:**

A) Yes, I can name them and I know why they're desperate for us
B) I have a few that seem very engaged
C) Hard to say — most customers seem lukewarm
D) I haven't thought about this yet

**After answer:** These are your case study candidates and your advisory board. Make sure you talk to them monthly.

---

## Phase 4: Calculate Feature Request Priority Score

### Question 4A: Scoring Model

**Re-ground:** We've tagged everything. Phase 4 is scoring what matters.

**Simplify:** Feature priority isn't just "how many people asked?" It's: frequency + business impact / effort. A feature 10 people want that takes 2 weeks matters less than one 8 people want that blocks deals and takes 3 days.

**Recommend:** Ready to score your top requests using (Frequency × Value) / Effort?

**Options:**

A) Yes, I can estimate frequency, impact, and effort for each
B) I can guess frequency but impact/effort is unclear
C) I need examples of how to think about impact vs effort
D) Let's do this right — I'll gather estimates

**If C:** Provide these examples:

```
Request: "Dark mode" (5 customers asked) × (nice to have) / (2 days) = Lower priority
Request: "Bulk export" (12 customers asked) × (saves 5 hours/month) / (3 days) = Higher priority
Request: "API access" (8 enterprise customers asked) × (blocks $500K deals) / (2 weeks) = Highest priority
```

---

### Question 4B: Must-Have vs Nice-to-Have

**Re-ground:** Scoring is clear. Now: separate must-haves from nice-to-haves.

**Simplify:** Some requests are "I'll leave if you don't build this." Others are "it would be cool but I'll survive without it." Which requests fall into which bucket?

**Recommend:** For your top 5 feature requests, classify each:

**Options:**

A) I can clearly separate must-haves (deal blockers) from nice-to-haves
B) Some are in the middle — I'm not sure
C) Hard to tell without asking customers directly
D) Everything feels important

**If C:** "Good instinct. You should call 3 customers and ask: 'If I don't build [feature], will you keep paying?' Their answer = must-have or nice-to-have."

---

## Phase 5: NPS and Sentiment Analysis

### Question 5A: Net Promoter Score

**Re-ground:** Must-haves prioritized. Phase 5 is sentiment: how happy are customers overall?

**Simplify:** If you've asked "How likely to recommend us?" (0-10 scale), you can calculate NPS. NPS tells you if you have product-market fit signals. Typical early startup: 20-40.

**Recommend:** Have you asked customers their recommend likelihood?

**Options:**

A) Yes, I have NPS scores from surveys or interviews
B) I haven't asked formally, but I can estimate from tone
C) No NPS data at all
D) Usage patterns tell me sentiment, not survey data

**If A:** Calculate and report NPS = (% Promoters 9-10) - (% Detractors 0-6)

**If B:** "Let's estimate from tone. Review your feedback: What % sounds like 'I love this'? vs 'I tolerate it'? vs 'I hate it'?"

---

## Phase 6: Desperate User Mapping

### Question 6A: Power Users

**Re-ground:** NPS captured. Now: identify your power users explicitly.

**Simplify:** For each desperate user, document:
1. Their name/company
2. Why they're desperate (what problem do you solve for them?)
3. What would they use you for long-term?

**Recommend:** Create a 1-page profile for each of your 3-5 power users.

**Options:**

A) I have clear profiles for my power users
B) I can do this now if you give me a template
C) I need to do customer interviews to identify them
D) I don't have enough users to have "power users"

---

## Phase 7: Output Generation

### Question 7A: Report Assembly

**Re-ground:** All feedback analyzed and prioritized. Phase 7 is generating your decision document.

**Simplify:** I'm going to compile this into CUSTOMER-FEEDBACK.md with your top 5 feature requests, top 5 complaints, churn analysis, NPS, and next actions.

**Recommend:** Ready to generate the report?

**Options:**

A) Yes, let's build it
B) I need to fill in some gaps first
C) Just focus on the top 1-2 issues first
D) I want to review my raw feedback one more time

---

## Key Metrics and Scoring Rules (Reference)

### Feature Request Scoring

```
Frequency = How many customers asked for this?
Value = How much would this matter to their business/workflow?
Effort = How hard is it to build?

Priority Score = Frequency × Value / Effort

High priority: High frequency + high value + lower effort
Low priority: Low frequency OR low value
```

### NPS Calculation

```
NPS = (% Promoters 9-10) - (% Detractors 0-6)

Industry benchmarks:
- Below 0: You're in trouble
- 0-30: Acceptable
- 30-50: Good
- 50+: Excellent (rare for early products)

Typical early startup with product-market fit signals: 20-40
```

### Must-Have vs Nice-to-Have Distinction

- **Nice to have:** Customers would like it, but won't leave without it
- **Blocker:** Without this, customers can't use your product for their core need
- **Deal killer:** This is preventing them from paying or referring others

---

## Output Template: CUSTOMER-FEEDBACK.md

```
# Customer Feedback Report

## Summary
- Total feedback collected: [N sources, M pieces of feedback]
- Response rate: [% of customers who gave feedback]
- Compilation date: [Today]

## Top 5 Feature Requests

| # | Feature | # asking | Impact | Blocker? | Effort | Status |
|---|---------|----------|--------|----------|--------|--------|
| 1 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |
| 2 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |
| 3 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |
| 4 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |
| 5 | [Feature] | [N] | [Impact] | [Y/N] | [Effort] | [In backlog/Building] |

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

| # | Issue | # complaining | Severity | Impact | Workaround? |
|---|-------|---------------|----------|--------|-------------|
| 1 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |
| 2 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |
| 3 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |
| 4 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |
| 5 | [Issue] | [N] | [Critical/High/Medium] | [What breaks] | [Is there one?] |

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
- [Reason 3]: [# customers] [Example quote]

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

**1. Biggest win in feedback:**
[What are people happiest about?]

**2. Biggest problem:**
[What's hurting adoption/retention?]

**3. Most surprising feedback:**
[What did we learn that contradicts our assumptions?]

**4. One thing to fix this sprint:**
[The single issue or request that matters most right now]

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

---

## Completion Status

When you've finished:

- [ ] Inventoried all feedback sources
- [ ] Read ALL feedback (no sampling!)
- [ ] Tagged feedback by category (request / complaint / churn / praise)
- [ ] Identified 3-5 desperate users
- [ ] Ranked top 5 feature requests by (Frequency × Value) / Effort
- [ ] Ranked top 5 complaints by severity and impact
- [ ] Calculated NPS or estimated from sentiment
- [ ] Generated CUSTOMER-FEEDBACK.md with action items

**Exit with:** DONE | DONE_WITH_CONCERNS | BLOCKED | NEEDS_CONTEXT

---

## Key Principle

"Nice to have" requests don't kill you. Missing a must-have does. Your job is to know the difference.
