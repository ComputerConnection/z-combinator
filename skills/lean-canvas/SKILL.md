---
name: lean-canvas
description: Force a complete Lean Canvas business model with adversarial challenge on every single cell. Nine cells, each validated against your customer evidence and brutally questioned. Interactive guided process with phase-based progression.
trigger_phrases:
  - lean canvas
  - business model canvas
  - business model
  - stage 3
  - scope the business
  - validate the canvas
benefits-from:
  - market-research
  - evidence-log
feeds-into:
  - mvp-scoper
---

# Lean Canvas: The Single-Page Business Model (Guided Interactive)

## What This Is

The Lean Canvas is ONE page that describes how your business actually works. Not how you hope it works. How it *actually* works based on your customer evidence.

Nine cells. No fluff. No visionary thinking without validation. Adversarial challenge on every single cell.

This becomes the reference document for everything that follows — your MVP spec, your pitch, your hiring, your decisions.

## Phase Overview

This skill works in phases:
- **Phase 0:** Preparation (assess what evidence you have)
- **Phase 1-9:** Build each of the nine canvas cells (Problem → Unique Value Proposition)
- **Phase 10:** Final review and locked LEAN-CANVAS.md output
- **Phase 11:** Completion assessment

Each phase uses guided AskUserQuestion interactions with specific re-grounding, simplification, recommendation, and lettered options.

---

## Phase 0: Preparation & Evidence Assessment

**Goal:** Understand what customer evidence and artifacts you have before building the canvas.

I need to read your existing artifacts to challenge your answers properly. I will:
- Read your INTAKE.md (if exists)
- Read your DESIGN-DOC.md (if exists)
- Read your EVIDENCE-LOG.md (if exists)
- Read your MARKET-RESEARCH.md (if exists)
- Read your FOUNDER-PROFILE.md (if exists)

**If these don't exist yet:** I'll ask you to provide them or work from memory. Evidence-based answers are stronger than memory-based answers.

**Exit criteria:** I understand what evidence backing you have before we start on Cell 1.

**User interaction:** I will search for these files in your project directory and summarize what I find.

---

## The Nine Cells (And the Questions That Will Haunt You)

## Phase 1: Problem (Cell 1 of 9)

**Goal:** Identify the TOP 3 problems your target customers face, grounded in interview evidence.

**How to use this phase:**

**Re-ground:** "We're building [Company Name]. We're at Stage 3 (Business Model). We're now defining the top 3 customer problems you're solving, validated against customer interviews."

Use the AskUserQuestion tool with this exact format:

**SIMPLIFY:** "A 'problem' is something that frustrates or costs your customers real time/money today. Not a future problem, not a nice-to-have, not something they might want fixed. Something they mentioned that's already bugging them. We're extracting the top 3 that appear most frequently in your interview notes."

**RECOMMEND:** "RECOMMENDATION: Use your EVIDENCE-LOG to count how many customers mentioned each problem unprompted. Pick the top 3 by frequency. If you haven't documented interviews yet, start there — answers without evidence are guesses.
- Completeness: 1/10 (no interviews)
- Completeness: 5/10 (some interviews, not all documented)
- Completeness: 10/10 (interviews documented, counted, analyzed)"

**OPTIONS:**
- **(A)** "I have EVIDENCE-LOG.md with 5+ customer interviews already documented. I'm ready to extract and count the problems."
- **(B)** "I have some interview notes but they're not in EVIDENCE-LOG format. I need help organizing them first."
- **(C)** "I haven't done formal interviews yet. I'm working from conversations with friends/early customers."
- **(D)** "I'm not sure what counts as 'evidence.' I need clarity on what to look for in customer conversations."

**For each problem provided, challenge with:**
- How many customers mentioned this unprompted (not you asking leading questions)?
- How many mentioned it as their #1 problem vs. a nice-to-have?
- Can you quote a customer describing the pain in their words?
- What's the cost/impact? ("5+ hours/week" is strong. "Would be nice" is weak.)

**Red flags to push back on:**
- "Users will struggle with X" (no evidence, just your assumption)
- "I think people have this problem" (thinking ≠ validation)
- A problem only 1 person mentioned (not a market, just one person)
- A hypothetical problem (never vocalized in interviews)

**Strong answer pattern:** "Based on 6/7 interviews, customers mention manually updating spreadsheets as their biggest pain. They spend 5+ hours/week on it. Lost revenue. Specific examples: [quote 1], [quote 2]."

**Weak answer pattern:** "People probably struggle with managing their data. I think there's a big market."

**Exit criteria for Phase 1:** You've provided 3 problems, each backed by 3+ customer mentions, with quote evidence. Move to Phase 2 (Solution).

---

## Phase 2: Solution (Cell 2 of 9)

**Goal:** Define the TOP 3 features that directly solve the top 3 problems. Each feature addresses one problem.

**How to use this phase:**

**Re-ground:** "We're at Phase 2 of the Lean Canvas. We have 3 validated problems. Now we're defining solutions — not a long feature list, but 3 specific features that directly address those problems."

Use the AskUserQuestion tool:

**SIMPLIFY:** "Each solution is one specific feature. Not 'a dashboard' (too vague). But 'auto-sync from 5 data sources into one dashboard.' We're matching 1 problem → 1 solution. Vitamin vs. Painkiller: Did customers ask for this, or did you invent it? Painkillers are what customers asked for. Vitamins are what you think would be nice."

**RECOMMEND:** "RECOMMENDATION: Match each solution to its corresponding problem. For each feature, verify: Did customers ask for this, or are you inventing? Can you build just this one feature in 2 weeks, or is it too complex?
- Completeness: 2/10 (inventing features not validated)
- Completeness: 6/10 (solutions validated but complex)
- Completeness: 10/10 (customer-requested, simple, buildable)"

**OPTIONS:**
- **(A)** "I have specific solutions from customer feedback. Customers asked me for these by name or described them."
- **(B)** "I have a product vision that includes these features. Some are customer-requested, some are my idea."
- **(C)** "I'm designing features based on what I think solves the problem. Not sure if customers want these specifically."
- **(D)** "I'm not sure how to map solutions to problems. Can you help me match them?"

**For each solution provided, challenge with:**
- Is this a painkiller (solves immediate pain) or vitamin (nice to have)?
- Did customers specifically ask for this, or are you inventing it?
- Is this the simplest way to solve the problem, or over-engineered?
- Can you actually build this in 2-3 weeks for MVP?

**Red flags to push back on:**
- Solution doesn't address a problem from Phase 1
- Three features that each solve different problems (you're unfocused)
- Solving the symptom instead of root cause
- Features that sound good but customers didn't ask for them
- Over-engineered solutions (mobile app, AI, etc. when problem needs simple fix)

**Strong answer pattern:** "Customers asked for 'one source of truth.' They use 5 different tools. Solution: Auto-sync those 5 tools into one dashboard. Reduces 5 hours/week of manual entry to 15 minutes. Simple. Specific. Asked for."

**Weak answer pattern:** "A beautiful dashboard with mobile app, AI recommendations, team collaboration, and integrations."

**Exit criteria for Phase 2:** You've provided 3 solutions, each directly addressing a problem from Phase 1, with evidence that customers asked for them. Move to Phase 3 (Key Metrics).

---

## Phase 3: Key Metrics (Cell 3 of 9)

**Goal:** Define THE ONE metric (not three) that indicates whether your business is working.

**How to use this phase:**

**Re-ground:** "We're at Phase 3. We have problems and solutions. Now: What single metric tells you whether this business is actually working? Not a nice metric. The metric that matters."

Use the AskUserQuestion tool:

**SIMPLIFY:** "Most founders list multiple metrics. But at early stage, you obsess over one. The others follow. Your 'north star metric' is usually something like: Paying customers? Revenue? Customers returning? Feature usage? Pick the one that moves when your business gets healthier."

**RECOMMEND:** "RECOMMENDATION: Choose a metric that indicates value delivery, not just activity. 'Paying customers' beats 'sign-ups.' 'Revenue' beats 'visits.' 'Returning usage' beats 'downloads.'
- Completeness: 1/10 (vanity metric like sign-ups)
- Completeness: 6/10 (reasonable metric, but multiple instead of one)
- Completeness: 10/10 (single, meaningful, measurable metric)"

**OPTIONS:**
- **(A)** "Paying customers (the number of customers who've paid anything)."
- **(B)** "Monthly recurring revenue (MRR — dollars coming in monthly)."
- **(C)** "Active weekly users (customers actually using the product weekly)."
- **(D)** "Repeat purchase rate or retention (customers coming back)."
- **(E)** "I'm not sure. What metric would you recommend for [my product type]?"

**For the metric chosen, challenge with:**
- Is this a vanity metric (looks good, means nothing)?
- Can you actually measure it easily?
- Does it move when the business gets better?
- Is this the metric a customer would care about, or just you?

**Red flags to push back on:**
- Sign-ups (useless without conversion)
- Download count (people download then uninstall)
- Visits (they might not be using it)
- DAU if product is for weekly/monthly use
- Multiple metrics (you need ONE)
- Any metric that doesn't indicate actual value delivery

**Strong answer pattern:** "Paying customers. Nothing else matters at this stage. Target: 10 paying customers by end of month 3."

**Weak answer pattern:** "Sign-ups, engagement, DAU, MAU, retention rate. We'll optimize for all of them."

**Exit criteria for Phase 3:** You've chosen ONE metric, can explain why it matters, and have a baseline/target. Move to Phase 4 (Unfair Advantage).

---

## Phase 4: Unfair Advantage (Cell 4 of 9)

**Goal:** Identify what you have that competitors can't easily copy. NOT a competitive advantage ("we're better"). An unfair advantage ("we have what they can't get").

**How to use this phase:**

**Re-ground:** "We're at Phase 4. We have a metric we're chasing. But why will you win? What do you have that competitors can't copy? Be honest — many startups have no unfair advantage. That's OK. We're being truthful about it."

Use the AskUserQuestion tool:

**SIMPLIFY:** "An unfair advantage is something that takes competitors years to replicate or that they literally can't access. Exclusive data. Existing customers you can leverage. Deep expertise nobody else has. NOT 'we'll execute better' or 'our team is smarter' — those aren't advantages, those are hopes."

**RECOMMEND:** "RECOMMENDATION: Identify what you have (not what you'll build). Real unfair advantages: exclusive access, existing user base, deep subject matter expertise, regulatory moat, proprietary data. Fake advantages: first mover, good team, better execution.
- Completeness: 1/10 (no real advantage)
- Completeness: 6/10 (some advantage, but replicable)
- Completeness: 10/10 (defensible, real, non-replicable advantage)"

**OPTIONS:**
- **(A)** "I have exclusive access to data, customers, or domain expertise others can't get."
- **(B)** "I am the target customer and can leverage my 500+ person network in this space."
- **(C)** "I have regulatory licensing, certifications, or proprietary tech that's hard to replicate."
- **(D)** "I have a co-founder or team member with 10+ years in this space as a practitioner."
- **(E)** "I don't have an unfair advantage yet. I'm competing on execution and product quality."

**For each advantage claimed, challenge with:**
- Can competitors copy this? (If yes, it's not an unfair advantage)
- Does it take them years to replicate? (Real advantages do)
- Is this something you have today, or something you'll build?
- Can you be specific about what it is?

**Red flags to push back on:**
- "First mover advantage" (they can copy you)
- "We're better at X" (so can they)
- "We have great technology" (so can everyone else)
- "Our team is passionate/smart" (every team is)
- "Network effects" (with zero users, doesn't exist yet)
- "Brand" (you have no brand yet)
- "We'll have better customer service" (hope, not advantage)

**Strong answer pattern:** "I'm the target customer. Spent 10 years in enterprise sales. I know the pain point better than anyone. I have a 500-person network of CIOs I can reach directly. They know and trust me."

**Weak answer pattern:** "Network effects. Once we have 1K users, it's sticky. Also great customer service and passionate team."

**Exit criteria for Phase 4:** You've identified a real, non-replicable advantage (or been honest that you don't have one yet). Move to Phase 5 (Channels).

---

## Phase 5: Channels (Cell 5 of 9)

**Goal:** Define the specific way you'll reach your target customers. Not "social media." Specific channels, validated.

**How to use this phase:**

**Re-ground:** "We're at Phase 5. We know who we're building for and what they need. Now: How do you actually reach them? Where do they spend time? Where do they find solutions to this problem?"

Use the AskUserQuestion tool:

**SIMPLIFY:** "A channel is a specific way to reach customers. Not 'marketing.' Not 'word of mouth.' But 'cold outreach to CTOs on LinkedIn' or 'indie hacker forums' or 'Facebook groups for freelancers.' Where do YOUR customers already congregate?"

**RECOMMEND:** "RECOMMENDATION: Pick a channel where you've already seen traction or have direct evidence customers use. Untested channels are guesses.
- Completeness: 1/10 (generic: social media, word of mouth)
- Completeness: 6/10 (specific channel, not validated)
- Completeness: 10/10 (specific, validated, cost-measured)"

**OPTIONS:**
- **(A)** "Direct outreach to specific people (cold email/LinkedIn to CTOs, founders, specific roles)."
- **(B)** "Community where they already gather (Reddit, Facebook groups, Slack communities, forums)."
- **(C)** "Content/SEO (blog, YouTube, podcast that attracts them)."
- **(D)** "Paid ads (Facebook, Google, LinkedIn, targeted to specific audience)."
- **(E)** "Sales calls / word of mouth from early customers (only after launch)."
- **(F)** "I'm not sure. What channel would work for [my product]?"

**For each channel provided, challenge with:**
- Can you reach them this way? (Have you tried?)
- Is this how they currently find solutions like yours?
- How much does it cost per customer? (Do you know?)
- Have you validated this channel works, or is it a guess?

**Red flags to push back on:**
- "Social media" without platform/audience specification
- "Word of mouth" (works after PMF, not before)
- "Influencers" (you don't have budget or relationships)
- Untested channels
- Channels your target customer doesn't use
- "We'll use all channels" (focus on one that works first)

**Strong answer pattern:** "Direct LinkedIn outreach to CTOs at Series B SaaS companies. Tested: 3/10 cold messages → 30-min call. Cost: $50 per meeting scheduled. These are the people who have the problem and the budget to solve it."

**Weak answer pattern:** "Social media marketing, content marketing, partnerships, and word of mouth."

**Exit criteria for Phase 5:** You've identified a specific channel, explained who congregates there, and shown evidence it works (or plan to validate). Move to Phase 6 (Customer Segments).

---

## Phase 6: Customer Segments (Cell 6 of 9)

**Goal:** Define your specific early adopter segment. Not "everyone with the problem." A specific, reachable, desperate segment.

**How to use this phase:**

**Re-ground:** "We're at Phase 6. We have a channel to reach people. But who exactly are we reaching? Your early adopter profile must be tight — job title, industry, company size, maybe geography. Specific enough that you can find 10 of them in a weekend."

Use the AskUserQuestion tool:

**SIMPLIFY:** "Don't target 'businesses' or 'people who have the problem.' That's too broad. Target a beachhead: a specific slice you can dominate. Example: 'Freelance writers with $3k-10k/month revenue, US-based, using Stripe, need tax tracking.' That's specific. You can find them. They're desperate for a solution."

**RECOMMEND:** "RECOMMENDATION: Pick a segment you've interviewed and understand. Specific enough that you can describe them in 2 sentences. Desperate enough that they'll use version 1.0.
- Completeness: 2/10 (too broad: 'freelancers')
- Completeness: 6/10 (specific: 'content creators' but missing revenue/geography)
- Completeness: 10/10 (tight: writers, $3k-10k/mo, US, need tax tracking)"

**OPTIONS:**
- **(A)** "I have a tight customer segment from interviews: [specific title/industry/size/behavior]."
- **(B)** "I have multiple possible segments. I need help picking the beachhead."
- **(C)** "I know the problem, but I'm not sure exactly who has it most acutely."
- **(D)** "My segment is too broad. I know I need to narrow it, but I'm not sure how."

**For each segment provided, challenge with:**
- Did you actually interview people in this segment?
- Would they describe themselves this way?
- Are they easy to reach?
- Are they big enough to build a business (at least 10K people)?
- Are they desperate enough to use version 1.0 (rough, unpolished)?
- Can you find 10 of them in your network or via your channel?

**Red flags to push back on:**
- "Anyone with X problem" (too broad)
- A segment nobody from your interviews actually matched
- "Everyone needs this" (you need a beachhead first)
- A segment that's hard to reach
- A segment of 100 people (too small to build a business)
- Too young or too poor to pay anything

**Strong answer pattern:** "Freelance content creators (writers, designers, video creators) earning $3k-10k/month, US-based, using Stripe for payments, who need tax-ready income tracking. They're desperate for this. I've interviewed 6 in this exact profile."

**Weak answer pattern:** "Freelancers and small businesses."

**Exit criteria for Phase 6:** You've defined a specific, reachable, validated early adopter segment (or committed to a pivot). Move to Phase 7 (Cost Structure).

---

## Phase 7: Cost Structure (Cell 7 of 9)

**Goal:** Define your monthly burn rate. Brutally honest. Including founder time at market rate.

**How to use this phase:**

**Re-ground:** "We're at Phase 7. We're now facing the financial reality. What does it cost to run this business monthly? Include your own time — founders don't work for free."

Use the AskUserQuestion tool:

**SIMPLIFY:** "Burn rate = everything that costs money per month. Your salary (at what you'd earn elsewhere, not what you'll actually pay yourself). Hosting. Tools. Marketing. Everything. Then: How many months of savings do you have? That's your runway. How many customers at what price does it take to break even?"

**RECOMMEND:** "RECOMMENDATION: Be honest about burn. Include opportunity cost (your market-rate salary). Most founders underestimate by 50%.
- Completeness: 2/10 (no idea, guessing low)
- Completeness: 6/10 (some costs counted, missing founder time)
- Completeness: 10/10 (all costs itemized, includes opportunity cost, runway clear)"

**OPTIONS:**
- **(A)** "I have my costs itemized: [hosting, tools, salary, marketing]. I know my monthly burn."
- **(B)** "I have some costs but haven't calculated total burn or runway."
- **(C)** "I'm bootstrapping and avoiding costs. I'll minimize burn."
- **(D)** "I'm not sure what to include in burn. I need help."

**For cost structure, ask:**
- What's your monthly hosting/infrastructure cost? (AWS, Heroku, etc.)
- What tools/subscriptions? (Stripe, GitHub, project mgmt, analytics, etc.)
- Salaries (if any)? (Include yourself at market rate)
- Marketing/acquisition spend? (If you're spending money)
- Other operating costs? (Insurance, legal, accounting, etc.)
- **Total monthly burn?**
- **Current savings/funding?**
- **Runway = Savings / Monthly Burn (in months)**

**Red flags to push back on:**
- Not including founder's time (this is the biggest mistake)
- Assuming free tier forever for services (they charge at scale)
- Forgetting customer acquisition cost
- Ignoring infrastructure costs that grow with users
- "We'll be lean" (too vague; needs numbers)

**Strong answer pattern:**
```
Monthly burn: $8,000
- Founder salary (market rate): $4,000
- AWS/infrastructure: $1,500
- Tools/services: $1,000
- Operating costs: $1,500

Savings: $25,000
Runway: 3.1 months
Break-even: 50 customers @ $30/mo = $1.5k MRR (covers 19% of burn)
```

**Weak answer pattern:** "We'll be lean. Minimal burn. Bootstrap for 12 months."

**Exit criteria for Phase 7:** You've itemized monthly costs, calculated runway in months, and identified break-even customer count. Move to Phase 8 (Revenue Streams).

---

## Phase 8: Revenue Streams (Cell 8 of 9)

**Goal:** Define exactly how customers give you money. Validated by customer feedback, not guessed.

**How to use this phase:**

**Re-ground:** "We're at Phase 8. We know costs and break-even. Now: How do customers actually pay? Not 'we'll figure it out.' But specific: subscription? One-time? Marketplace fee?"

Use the AskUserQuestion tool:

**SIMPLIFY:** "Revenue model is how money flows from customer to you. Subscription ($X/month), one-time purchase, pay-per-use, marketplace take rate, etc. The key: Did customers mention willingness to pay in interviews? Or are you guessing?"

**RECOMMEND:** "RECOMMENDATION: Match model to customer validation. Subscription works if customers want recurring value. One-time works if it solves a one-time problem. Don't guess.
- Completeness: 1/10 (no monetization plan, 'free forever')
- Completeness: 6/10 (model chosen, not validated)
- Completeness: 10/10 (model validated, customers asked about price)"

**OPTIONS:**
- **(A)** "B2B SaaS subscription ($X/month). Customers in interviews confirmed willingness to pay this."
- **(B)** "One-time purchase / one-time fee. Customer asks once, pays once."
- **(C)** "Marketplace model (take 15-30% of transactions)."
- **(D)** "Usage-based pricing (customers pay based on what they use)."
- **(E)** "I'm not sure how to monetize. I'm launching free to get traction first."

**For revenue model, challenge:**
- Did customers mention they'd pay this way, or are you inventing?
- Is this a real business model at your scale?
- Does the math work? (Break-even customers × price = monthly revenue needed)
- How much would they pay? (Have you asked directly?)

**Red flags to push back on:**
- "Free with ads" (zero users, ads don't work)
- "Freemium" (most freemium businesses fail to convert)
- "Marketplace take rate" (need critical mass first)
- "Enterprise licensing" (you don't have enterprise customers yet)
- "We'll figure it out later" (monetize before launch, not after)
- "Free to build a user base, monetize later" (momentum loss is real)

**Strong answer pattern:** "B2B SaaS subscription. $29-99/month based on tier. During interviews, 2 customers specifically asked 'how much would this cost?' and both seemed receptive to $50/month. That's willingness to pay."

**Weak answer pattern:** "We'll launch free and figure out monetization later. Maybe freemium or marketplace."

**Exit criteria for Phase 8:** You've defined a revenue model, confirmed willingness to pay in interviews, and checked that math works. Move to Phase 9 (Unique Value Proposition).

---

## Phase 9: Unique Value Proposition (Cell 9 of 9)

**Goal:** One sentence. A customer reads it and thinks, "Yeah, that's exactly what I need."

**How to use this phase:**

**Re-ground:** "We're at Phase 9, the final cell. You've defined all 8 cells. Now: Can you summarize what you do in one sentence? A sentence your best customer would actually say to a friend."

Use the AskUserQuestion tool:

**SIMPLIFY:** "This isn't a marketing tagline. It's a sentence that connects the problem, the solution, and the benefit in customer language. Not jargon. Not fluff. A sentence they would repeat: 'Automatically track project income and export tax-ready reports so I stop spending hours on accounting.'"

**RECOMMEND:** "RECOMMENDATION: Simple, customer-focused, outcome-focused. 1 sentence. 10 seconds to say. Grounded in real problem from Phase 1.
- Completeness: 1/10 (jargon, marketing fluff, or generic)
- Completeness: 6/10 (good but too long or unclear)
- Completeness: 10/10 (one sentence, customer-focused, customer would repeat it)"

**OPTIONS:**
- **(A)** "I have a clear one-sentence UVP that connects problem → solution → outcome."
- **(B)** "I have a UVP but it's probably too long or marketing-heavy."
- **(C)** "I'm not sure what to say. I need help crafting it."

**For UVP, challenge:**
- Is this meaningful to your customer, or is it jargon?
- Is it unique to you, or could any competitor say this?
- Would a customer actually repeat this sentence to a friend?
- Does it point to a real problem they confirmed in interviews?
- Can you say it in <10 seconds?

**Red flags to push back on:**
- Jargon only founders understand
- Solving a problem nobody mentioned
- Generic ("We make X easier" could apply to 100 companies)
- Too long (needs rewrites if >10 seconds)
- Not grounded in Phase 1 problem evidence
- Marketing-speak instead of customer-speak

**Strong answer pattern:** "Automatically track project income and export tax-ready reports so freelancers stop stress-spending hours on accounting."

**Weak answer pattern:** "The next-generation platform for income tracking using AI and machine learning to deliver innovative solutions."

**Exit criteria for Phase 9:** You have a clear, one-sentence UVP grounded in customer evidence. Proceed to Phase 10 (Canvas Review).

---

## Phase 10: Canvas Review & Lock

**Goal:** Final review of all 9 cells for internal consistency and evidence-grounding.

After you've provided all 9 cells, I will:

1. Cross-reference your EVIDENCE-LOG.md (if it exists) to verify claims
2. Challenge weak spots against evidence
3. Point out where you're guessing vs. where you have validation
4. Force rewrites on cells that lack evidence
5. Produce final LEAN-CANVAS.md (single-page reference document)

**The review will check:**
- Is Problem grounded in 3+ customer mentions per problem?
- Do Solutions directly address Problems from Phase 1?
- Is Key Metric meaningful (not vanity)?
- Is Unfair Advantage actually unfair (not replicable)?
- Is Channel specific and validated?
- Is Customer Segment tight and reachable?
- Do costs and revenue math make sense?
- Is monetization validated by customers?
- Is UVP one sentence, customer-focused, grounded in evidence?

**Output format (LEAN-CANVAS.md):**

```markdown
# LEAN CANVAS: [Your Company Name]

## Problem
[Top 3 problems with interview evidence count]

## Solution
[Top 3 features with interview validation]

## Key Metric
[ONE metric you'll obsess over]

## Unfair Advantage
[What can't be copied]

## Channels
[Specific customer acquisition plan]

## Customer Segments
[Early adopter profile with demographic detail]

## Cost Structure
[Monthly burn, runway, break-even math]

## Revenue Streams
[How customers pay, validated pricing]

## Unique Value Proposition
[One sentence a customer would repeat]
```

This becomes your north star. Every decision for the next 3 months flows from this one page.

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

## Phase 11: Completion & Handoff

**Completion status:** Once LEAN-CANVAS.md is locked and saved to your project directory, the skill is complete.

**Next steps after completion:**
- This canvas feeds directly into **mvp-scoper** (what to build first)
- Use it as the reference for all future decisions
- Recalculate quarterly as you learn more

---

## Completion Status

**DONE** — LEAN-CANVAS.md written and saved.
**DONE_WITH_CONCERNS** — Canvas complete but some cells lack full evidence (note which ones).
**BLOCKED** — Need more customer interviews before canvas can be finalized.
**NEEDS_CONTEXT** — Missing artifacts (EVIDENCE-LOG, etc.) that would strengthen validation.

**Next Step:** Proceed to mvp-scoper.
Return to z-combinator orchestrator for routing.

---

## Key Principle: No Visionary Thinking Without Validation

You don't get to say "I have a vision for the future" and put it in the canvas.

Every cell must be grounded in:
- What customers actually said
- What they actually do
- What they're actually willing to pay
- What you can actually build

If you don't have evidence, we'll identify the gap and you'll get it.

---

## Ready to Begin?

When you're ready, I'll ask about Phase 0 preparation: What artifacts do you have? Then we'll move through all 9 cells, one at a time, with proper evidence-backing.
