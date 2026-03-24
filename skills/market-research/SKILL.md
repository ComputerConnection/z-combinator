---
name: market-research
description: Adversarial competitive intelligence. Find every existing solution, map the graveyard, size the market honestly, and challenge the founder on why they'll win where others lost.
triggers:
  - market research
  - competitive analysis
  - who else does this
  - market size
  - stage 1 research
benefits-from:
  - idea-intake
feeds-into:
  - gate-evaluator
---

# Market Research: Adversarial Competitive Intelligence

You've articulated your idea. Now comes the hard truth: **the market is probably saying NO until proven otherwise.**

This skill will:
1. Map every existing solution (direct competitors, adjacent plays, DIY alternatives)
2. Explain why each competitor hasn't already won
3. Dig through the graveyard — find companies that tried and died, and learn why
4. Size the market with brutal honesty (not "1% of trillion-dollar market" math)
5. Identify regulatory or legal landmines
6. Challenge you directly on every finding

Output: **MARKET-RESEARCH.md** — a competitive matrix, graveyard analysis, honest TAM/SAM/SOM, and a verdict.

---

## Phase 0: Prerequisites & Intake Review

Use AskUserQuestion:

**Re-ground:** Stage 1, Phase 2. You've articulated your idea. Now we're going to stress-test it against the real market.

**Simplify:** I need to read your INTAKE.md from idea-intake — that's where you articulated the problem, customer, timing, and advantage. Then I'll research competitors, the graveyard of failed attempts, market sizing, and regulatory issues. Then I'll challenge you on all of it.

**Recommend:** RECOMMENDATION: Have INTAKE.md ready. If you don't, run idea-intake first. This only works if we have clarity on the problem. Completeness: 10/10 if you have the artifact ready.

**Options:**
- A) "I have INTAKE.md ready"
- B) "I haven't done idea-intake yet"
- C) "I want to update my INTAKE.md first"

**If NO INTAKE.md:** Route back to idea-intake. Return here after completion.

**If YES:** Proceed to Phase 1.

---

## Phase 1: Competitive Research

I will systematically research:

### 1.1 Direct Competitors
- Companies solving this exact problem
- Pricing, feature set, go-to-market, founding story
- Why they have (or don't have) traction

### 1.2 Adjacent Solutions
- Different approach to the same problem
- Tooling that partially solves it
- Industries using similar solutions

### 1.3 DIY Alternatives
- Spreadsheets, manual processes, open-source tools
- Why customers might build it themselves instead of buying

### 1.4 The Graveyard
- Companies that tried this and failed
- Timing, funding, exit (if any), and lessons
- Key question: What's different now?

### 1.5 Market Dynamics
- Pricing landscape — what people actually pay today
- Market consolidation — are big players already winning?
- Regulatory barriers — licenses, compliance, data residency
- Macro headwinds — is the market shrinking?

**As I research, I'll note:**
- Every competitor I find with founding story and current status
- Pricing for each solution
- Why each one might not have won (product gaps? timing? market dynamics?)
- Whether I find any clear "winner" already owning this space

---

## Phase 2: Honest Market Sizing

For TAM/SAM/SOM, I'll calculate and challenge:

**TAM (Total Addressable Market):**
- Bottom-up: How many people/companies actually have this problem?
- NOT: "1% of $1 trillion SaaS market = $50B" (lazy)
- YES: "There are 500K mid-market companies. 30% use this workflow. Average deal $50K. = $7.5B TAM"

**SAM (Serviceable Addressable Market):**
- Which geographic markets can you realistically reach first? (Start with one)
- Which customer segments can your GTM actually serve?
- Realistic = 5-10% of TAM, not 50%

**SOM (Serviceable Obtainable Market):**
- Year 1-3: What's your realistic market capture?
- Don't lie to yourself here

**Pushback I'll apply:**
- Inflated TAM numbers based on industry reports with zero specificity
- Assumptions without data backing them
- Market-wide claims without customer count evidence

---

## Phase 3: Challenge Findings (Interactive)

For every major finding, I'll ask you directly and expect real answers:

Use AskUserQuestion to deliver each finding:

**Re-ground:** [Finding about a competitor, the graveyard, or market dynamics].

**Simplify:** [Explain why this matters for your idea].

**Recommend:** RECOMMENDATION: [How you should respond to this finding]. Completeness: 10/10 if you have a concrete answer, not deflection.

**Options:**
- A) "[Response A]"
- B) "[Response B]"
- C) "I need to think about this"

**Example challenges:**
- "Company X raised $50M and does exactly this. What's your response?"
- "Three companies tried this in 2019-2021. All folded. What's different now?"
- "People aren't paying more than $500/month for this category. How does your unit economics work?"
- "Regulation has killed three startups in this space. How do you navigate it?"

These aren't rhetorical. You need real answers — not deflection.

---

## Phase 4: Synthesis & Market Verdict

After research and challenge round, use AskUserQuestion to frame verdict:

**Re-ground:** I've researched competitors, the graveyard, market sizing, and regulatory issues. Here's my verdict on this market.

**Simplify:** [Is this a blue ocean, crowded, dominated, or graveyard?] [Why?]

**Recommend:** RECOMMENDATION: Based on market conditions, here's what needs to be true for you to win: [specific conditions]. Completeness: 10/10 if you have a realistic thesis for competitive advantage.

**Options:**
- A) "I accept this verdict and want to proceed"
- B) "I want to challenge your research on [specific finding]"
- C) "This makes me want to pivot"

---

## Phase 5: Artifact Generation

Write MARKET-RESEARCH.md:

```markdown
# Market Research: [Your Problem Statement]

**Research Date:** [today]
**Problem:** [From INTAKE.md]
**Founder's Advantage:** [From INTAKE.md]

---

## Competitive Landscape

### Direct Competitors
| Company | Founded | Problem Solved | Pricing | Strengths | Weaknesses | Current Status |
| --- | --- | --- | --- | --- | --- | --- |
| [Company] | [Year] | [What problem?] | [Price] | [What's good?] | [What's bad?] | [Alive/Dead] |

### Adjacent Solutions
| Solution | How It Compares | Why It's Not Perfect | Willingness to Upgrade |
| --- | --- | --- | --- |
| [Solution] | [What does it do?] | [Why is it partial?] | [Would customers pay for better?] |

### DIY Alternatives
(What are people using instead of a paid solution? Spreadsheets? Manual processes? Open-source?)

---

## The Graveyard: Failed Attempts

| Company | Founded | Funding | What Failed | Why | Lessons for You |
| --- | --- | --- | --- | --- | --- |
| [Company] | [Year] | [$X] | [What didn't work] | [Why] | [What's different?] |

---

## Market Sizing

### TAM (Total Addressable Market)
**Calculation:** [Bottom-up method]
**Size:** $[X] billion
**Breakdown:** [X companies/people × $Y average spend]

### SAM (Serviceable Addressable Market)
**Geographic Scope:** [Start with what? US? Europe? Specific cities?]
**Customer Segment:** [Which segment can you actually GTM to?]
**Size:** $[X] million
**Rationale:** [Why this is realistic for you]

### SOM (Serviceable Obtainable Market)
**Year 1 Target:** $[X] revenue
**Year 3 Target:** $[X] revenue
**Rationale:** [How you get there]

---

## Regulatory & Legal Landscape

[Licenses? Compliance? Data residency? Industry-specific barriers?]

---

## Pricing Landscape

- **Current WTP:** [What do people currently pay for similar solutions?]
- **Pricing Models:** [Per-seat? Per-transaction? Flat? Usage-based?]
- **Price Range:** [From $X/month to $Y/month for similar categories]

---

## Market Verdict

**Status:** [Blue Ocean / Crowded / Dominated / Graveyard]

**Rationale:**
- Is this solvable? [Yes/No and why]
- Why would you win where others lost (or are winning)? [Your advantage]
- What's the real blocker? [The hardest part]

---

## Founder Challenge Round

**Finding 1:** [Major competitive or market finding]
Your answer: [What you said]
My pushback: [Why that's insufficient or strong]

[Repeat for all major findings]

---

## Recommendations for Next Stage

[What you should validate in customer discovery? What risks are highest?]
```

---

## Completion Status

**DONE** — MARKET-RESEARCH.md is written and verdict is delivered.

**Next Step:** Proceed to customer-discovery skill to talk to real customers and validate (or invalidate) your hypothesis.

Return to z-combinator orchestrator for routing.
