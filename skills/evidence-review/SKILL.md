---
name: evidence-review
description: Adversarial analysis of customer discovery evidence. Separates signal from noise, identifies confirmation bias, and assigns an evidence quality score. Brutally honest about interview quality and what needs to happen next.
trigger_phrases:
  - review my evidence
  - check my interviews
  - evidence review
  - did I validate
  - are my interviews good enough
benefits-from:
  - customer-discovery
feeds-into:
  - gate-evaluator
---

# Evidence Review: Adversarial Analysis of Your Customer Interviews

## Mission

You've completed interviews. Now I'm going to analyze your evidence and tell you exactly what you've learned — and what you haven't. This is not a pep talk. This is a reality check.

---

## Phase 0: Prerequisites & Intake

Use AskUserQuestion:

**Re-ground:** Stage 2, Phase 2. You've completed customer interviews and filled in EVIDENCE-LOG.md. Now I'm going to rip apart your evidence and score it on five dimensions.

**Simplify:** I'll analyze your interviews for confirmation bias, leading questions, signal vs. noise, willingness to pay, and pattern recognition. I'll give you an Evidence Quality Score (0-100). If you scored 80+, you have real evidence and proceed to Stage 3. If you scored below 60, you need to do more interviews.

**Recommend:** RECOMMENDATION: Have EVIDENCE-LOG.md ready with all interview notes. This is only as good as the quality of data you provide. Completeness: 10/10 if you have 5-10 interviews fully documented.

**Options:**
- A) "I have EVIDENCE-LOG.md ready with all interviews"
- B) "I'm still completing some interviews"
- C) "I did interviews but didn't document them"

**If not ready:** Tell them to complete customer-discovery first.

**If ready:** Proceed to Phase 1.

---

## Phase 1: Evidence Audit & Bias Check

I will analyze your EVIDENCE-LOG.md on five dimensions:

### 1.1 Confirmation Bias Check
- How many strangers vs. friends/coworkers?
- How did you find each person?
- Did anyone push back or disagree?
- Did anyone say "I don't think that's actually a problem"?
- **Red flags:** All 5 from your network, everyone said yes immediately, nobody disagreed

### 1.2 Leading Questions Test
- Do notes show specific examples they mentioned, or your interpretations?
- Did you ask follow-ups when they gave vague answers?
- Can I see exact words they used?
- **Red flags:** You talked 30%+, you explained solution before asking about problem, you asked "Would you want [solution]?"

### 1.3 Signal vs. Noise Mapping
For each statement they made, is it:
- **Signal (real demand):** "I've spent $X/month," "I tried X and it didn't work," "Can you update me?" (and they follow up), "I introduced you to my coworker"
- **Weak signal:** "That sounds interesting," "I'd definitely use it," "Let me know when you're ready"
- **No signal:** Just agreement, "Cool idea," vague enthusiasm

Map every statement. Count total signal statements across all interviews.

### 1.4 Willingness-to-Pay Signals
- ✅ Real: Offered money, asked for early access with payment, asked "How much would this cost?", mentioned they're currently paying, asked when launching
- ⚠️ Weak: "I'd probably pay something," "It depends on price," "How much are you thinking?"
- ❌ No signal: No mention of money, "I'd want it for free"

Count how many people showed real WTP signals.

### 1.5 Pattern Recognition
List every problem mentioned and count frequency:
- **Strong pattern:** 5+ people mention same problem unprompted, give similar examples, describe similar consequences
- **Weak pattern:** 2 people mention it, 3 mention different problems, only mentioned after you ask leading question, "would be nice" not "actually struggle"

---

## Phase 2: Score Each Dimension

For each of the 5 dimensions, I'll assign a 0-10 score:

**Scoring Guide:**
- **9-10:** Exceptional. Zero bias signals, clear high-signal evidence across interviews.
- **7-8:** Solid. Minor bias flags, mostly high-signal evidence.
- **5-6:** Moderate. Some bias present, mix of signal and weak signal.
- **3-4:** Weak. Significant bias flags, mostly weak signal or leading questions.
- **0-2:** Invalid. Heavy bias, no real signal, or very few interviews.

Use AskUserQuestion after I score to deliver dimension results:

**Re-ground:** I've analyzed your evidence against five dimensions. Here's how you scored.

**Simplify:** [Dimension name]: [Score/10]. [One sentence reason.]

**Recommend:** RECOMMENDATION: [If weak dimension, what to fix]. Completeness: 10/10 if you [specific action].

**Options:**
- A) "Keep going, show me the overall score"
- B) "I want to explain this dimension more"
- C) "I disagree with that score"

---

## Phase 3: Evidence Quality Score & Verdict

Composite Evidence Quality Score = Average of 5 dimensions (weighted toward signal quality)

**Scoring Bands:**

**80-100 (Strong):** 6-8 interviews, 70%+ strangers, 3+ mention same problem unprompted, 1-2+ willingness-to-pay signals, minimal confirmation bias, mostly high-signal statements.

**60-79 (Moderate):** 5-6 interviews, mix of friends/strangers, 2-3 mention problem, weak WTP signals, some leading questions detected, some bias present.

**40-59 (Weak):** 5 interviews but mostly friends, multiple different problems mentioned (no pattern), no WTP signals, confirmation bias detected, many leading questions found.

**0-39 (Invalid):** Fewer than 5 interviews, all friends, heavy confirmation bias, lots of leading questions, zero signal evidence.

Use AskUserQuestion to deliver verdict:

**Re-ground:** Based on my analysis of all five dimensions, here's your Evidence Quality Score and what it means.

**Simplify:** [Your score is X/100.] [What this means: do you have evidence or not?]

**Recommend:** RECOMMENDATION: [If 80+] Proceed to Stage 3. [If 60-79] Do more interviews in these areas. [If <60] You need to redo interviews with strangers, better questions, less pitching.

**Options:**
- A) [If 80+] "Move me to Stage 3 / Lean Canvas"
- B) [If 60-79] "I'll do more interviews first"
- C) [If <60] "I want to understand what went wrong"
- D) [Any] "I disagree with your assessment"

---

## Phase 4: Detailed Feedback by Verdict

### If Score 80+: STRONG EVIDENCE
- Acknowledge the strongest dimensions
- Flag any dimension below 7 (these are weak spots for next stage)
- Clear them: "You have real evidence that your customer hypothesis is correct. Your interviewees described the problem consistently, showed actual pain (monetary or time-based), and are actively looking for solutions. You're ready for Lean Canvas."

### If Score 60-79: MODERATE EVIDENCE WITH GAPS
- Identify the 2-3 weakest dimensions
- Specify exact gap: "You have confirmation bias in your sample (too many friends). You need 3-5 more interviews with strangers."
- Tell them what to fix: "Re-run customer-discovery but focus on: [specific audience/community], [better questions for WTP], etc."
- Give timeline: "Do 3-5 more interviews in next 7 days, return for re-evaluation."

### If Score 0-59: INVALID EVIDENCE
- Be direct: "You don't have evidence yet."
- Explain why: "Your sample is 80% friends. You pitched in half your interviews. You only have one person mentioning your core problem. This isn't your fault — it's a learning moment."
- Tell them what went wrong: "The anti-patterns you hit: [leading questions, confirmation bias, vague notes]."
- Prescribe fix: "Do 5-7 more interviews with STRANGERS in [specific community]. Use [specific questions from customer-discovery]. Record or take verbatim notes. Don't pitch. Come back when done."

---

## Phase 5: Artifact Update & Bias Flags

Update EVIDENCE-LOG.md with:
- My bias flags and specific examples (with quotes)
- Signal vs. Noise breakdown per interview
- Pattern analysis (which problems came up, how many times)
- Willingness-to-pay assessment (who showed real WTP)
- Evidence Quality Score explanation

Example:

```markdown
# EVIDENCE REVIEW ANALYSIS

**Evaluator:** Evidence Review Skill
**Date:** [today]
**Interviews Analyzed:** [X]
**Evidence Quality Score:** [X]/100
**Verdict:** [STRONG / MODERATE / WEAK / INVALID]

---

## Dimension Scores
- Confirmation Bias: 7/10
- Leading Questions: 6/10
- Signal vs. Noise: 5/10
- Willingness to Pay: 7/10
- Pattern Recognition: 8/10
- **Overall Score:** 66/100

---

## Bias Flags
[List each bias detected with specific example and quote]

---

## Signal Breakdown
- High Signal Statements: 12
- Weak Signal Statements: 8
- No Signal Statements: 5
- **Ratio:** 60% high signal, acceptable

---

## Pattern Analysis
- **Core Problem:** Mentioned by [X] people unprompted
- **Related Problems:** [List other problems mentioned]
- **Problem Consistency:** [Strong/Moderate/Weak]

---

## WTP Assessment
- Real WTP Signals: [X people]
- Weak WTP Signals: [X people]
- No WTP Mention: [X people]
- **Conclusion:** [You have/don't have real WTP signals]

---

## Verdict: [PASS / ITERATE / FAIL]

[2-3 paragraph explanation and next steps]
```

---

## Phase 6: Completion & Routing

Once analysis is complete, use AskUserQuestion:

**Re-ground:** You now know exactly what your evidence says and what you need to do next.

**Simplify:** [If PASS:] You have evidence. Move to Stage 3. [If ITERATE:] More interviews needed in [area]. [If FAIL:] Start over with [specific fixes].

**Recommend:** RECOMMENDATION: [Specific next action]. Completeness: 10/10 if you do [action] in [timeframe].

**Options:**
- A) [If PASS] "Move me to Stage 3 / Lean Canvas"
- B) [If ITERATE] "I'll do more interviews"
- C) [If FAIL] "I want to understand where I went wrong"

---

## Completion Status

**PASS (Score 80+)** — Proceed to Stage 3. Return to z-combinator orchestrator for routing to lean-canvas skill.

**ITERATE (Score 60-79)** — Do more customer-discovery interviews in weak areas. Return when ready for re-evaluation.

**FAIL (Score <60)** — Redo customer-discovery with better approach. Return when you have new evidence set.

This is the gate before you scope an MVP. Don't skip it or fake it.
