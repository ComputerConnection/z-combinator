---
name: customer-discovery
description: Generate a customer interview playbook using The Mom Test methodology to extract truth about customer problems. Conducts adversarial challenge on interview plan and forces evidence collection before proceeding.
trigger_phrases:
  - customer discovery
  - interview prep
  - the mom test
  - customer interviews
  - stage 2
  - validate with customers
benefits-from:
  - idea-intake
  - market-research
feeds-into:
  - evidence-review
---

# Customer Discovery: The Mom Test Interview Playbook

## Mission

You've articulated your idea and researched the market. Now you need to talk to real customers and extract the truth about whether they actually have the problem you think they have.

The core principle: **Never ask someone if your idea is good — they'll lie to be nice.** Instead, ask about their life, their problems, and their actual behavior.

---

## Phase 0: Prerequisites & Intake

Use AskUserQuestion:

**Re-ground:** Stage 2, customer discovery. You've done idea intake and market research. Now you're going to interview 5-10 real customers using The Mom Test methodology — structured interviews designed to extract truth, not validation.

**Simplify:** You'll talk to customers about their actual problems, current workarounds, and pain points. Not about whether your idea is good. Your job is to listen for patterns and evidence of real demand.

**Recommend:** RECOMMENDATION: Have INTAKE.md and MARKET-RESEARCH.md ready. These shape your interview approach. Completeness: 10/10 if you have both artifacts.

**Options:**
- A) "I have my artifacts ready, let's build the interview plan"
- B) "I want to refresh on The Mom Test first"
- C) "I'm not sure how to find customers"

**If artifacts missing:** Route back to idea-intake or market-research first.

**If ready:** Proceed to Phase 1.

---

## Phase 1: The Mom Test Principle & Anti-Patterns

**The Core Rule:** Never ask if your idea is good. They'll say yes to be nice.

Instead:
- Ask about their actual behavior: "Tell me about the last time you hit this problem."
- Ask what they currently do: "What did you do to solve it?"
- Ask for specifics: "How much time/money did you spend?"
- Ask about alternatives: "Did you try anything else?"

**Bad questions (BANNED):**
- "Would you use this?" → Leads to "yes"
- "How much would you pay?" → Before they believe in the problem
- "Is this a good idea?" → Everyone's polite
- "Do you have this problem?" → Too leading

**Good questions (REQUIRED):**
- "Tell me about the last time you [experienced the problem]."
- "What did you do to solve it?"
- "How much time/money/effort did you spend?"
- "Did you try anything else? What happened?"
- "Are you still looking for a solution?"
- "What would the perfect solution look like?"
- "Why haven't you solved this yet?"

---

## Phase 2: Generate Interview Questions

Use AskUserQuestion:

**Re-ground:** I'm going to generate 10 specific interview questions tailored to YOUR problem and target customer (from INTAKE.md). These are behavioral questions that extract truth, not leading questions that get you validation.

**Simplify:** For each question, I'll explain why it extracts truth (not opinion) and what signals to listen for. You'll use these in real interviews.

**Recommend:** RECOMMENDATION: These are starting points. You'll adapt them based on the conversation. Good interviews follow a loose flow, not a rigid script. Completeness: 10/10 if you can follow the question logic and improvise follow-ups.

**Options:**
- A) "Generate the questions"
- B) "I want to customize some questions first"
- C) "I'm worried these won't work"

**Then generate:**

```markdown
# Customer Discovery Interview Questions

## Your Target Customer
[From INTAKE.md: name, title, problem they have]

## 10 Truth-Extracting Questions

1. **Opening & Rapport**
   - "How did you end up in [their role]?"
   - Why: Builds trust, gets them talking naturally, reveals context

2. **Past Behavior (Critical)**
   - "Tell me about the last time you struggled with [problem]."
   - Why: Reveals if problem is real, how acute, and when it happened
   - Listen for: Specific stories, emotions, frequency

3. **Current Workaround**
   - "What did you do to handle it?"
   - Why: Shows their current solution. Everyone has one.
   - Listen for: Tools, manual processes, effort required

4. **Effort & Cost**
   - "How much time/money did you spend on solving it?"
   - Why: Quantifies pain. Big pain = they'd pay to solve it.
   - Listen for: Specific numbers (not "a lot")

5. **Alternatives Tried**
   - "Did you try anything else? What happened?"
   - Why: Reveals what they've already tested
   - Listen for: Why existing solutions don't work perfectly

6. **Ongoing Search**
   - "Are you still looking for a better solution?"
   - Why: Reveals if this is active pain or solved pain
   - Listen for: "Yes, constantly" vs. "nah, it's fine"

7. **Ideal Solution**
   - "What would the perfect solution look like?"
   - Why: Without leading, asks about their dream state
   - Listen for: Specific features vs. vague wishes

8. **Why Unsolved**
   - "Why do you think nobody's solved this yet?"
   - Why: Reveals what they think is hard about the problem
   - Listen for: Market dynamics, technical barriers, timing

9. **Introduce Your Idea (CAREFULLY)**
   - "We're exploring [vague description]. What would make this valuable to you?"
   - Why: Now you can test if your solution fits, without leading
   - Listen for: Specific feedback, not "that sounds cool"

10. **Close & Follow-up**
    - "Would I be able to check in with you in a few weeks?"
    - Why: Keeps the door open for next conversation
    - Listen for: Willingness. Real interest = yes without hesitation

## Interview Flow
- Don't follow this as a script. It's a conversation flow.
- Questions 1-8 are about THEM and their current situation.
- Only introduce your idea in Question 9, after you understand them.
- Record or take verbatim notes.
- Each interview: 20-30 minutes.
```

**Move to Phase 3.**

---

## Phase 3: Build Target Interview List

Use AskUserQuestion:

**Re-ground:** Now you need to find 5-10 real customers. Not your friends. Not coworkers. Not people who owe you favors.

**Simplify:** Where do these people congregate? Online communities? LinkedIn groups? Industry conferences? How do you reach them credibly? What's your honest opening line that isn't a pitch?

**Recommend:** RECOMMENDATION: Start with 3-5 specific people or communities you'll reach out to this week. Prioritize strangers over friends (70% should be strangers). Completeness: 10/10 if you have specific names/communities and a credible outreach angle.

**Options:**
- A) "I have a target list ready"
- B) "I need help finding where they congregate"
- C) "I'm worried I won't find enough people"

**Then create:**

```markdown
# Customer Interview Target List

## Primary Target Customer
[From INTAKE.md]

## Where They Congregate
1. [Online community/forum/Slack group] - How to join/access?
2. [LinkedIn groups or searches] - How to find and filter?
3. [Conferences or events] - Which ones? When?
4. [Direct references] - Who can introduce you?

## Prioritized Outreach List

### Tier 1: First Interviews (Warm up interviews)
[3 people you find via online communities, easier to reach cold]
- [Name/Profile] — Where you found them, cold outreach angle

### Tier 2: Key Interviews (Best leads)
[2-3 people who are highest quality matches for your customer definition]
- [Name/Profile] — How to reach them, mutual connection angle

### Tier 3: Backup Interviews (If you need more)
[Additional people if patterns aren't clear]
- [Name/Profile] — Alternative outreach

## Cold Outreach Template
"Hi [Name], I noticed your post about [X], and I'm researching [problem]. Would you have 20 minutes this week to chat about how you handle [specific challenge]?"

[Not: "I'm building something cool, want to chat?"]

## Interview Logistics
- Target: 5-10 interviews minimum
- At least 70% should be strangers/cold outreach
- Each: 20-30 minutes
- Record or take verbatim notes
- Spread over 2-3 weeks
```

**Move to Phase 4.**

---

## Phase 4: Anti-Patterns & Scorecard

Show anti-patterns that destroy evidence:

```markdown
# Common Interview Anti-Patterns

| Anti-Pattern | Why It Fails | Fix |
|---|---|---|
| Only friends | They want to be nice, agree with everything | 70% strangers minimum |
| Pitching during interviews | You talk 30 mins, they listen politely, you learn nothing | Talk 10%, listen 90%, ask follow-ups |
| Asking hypotheticals | "Would you use this?" → They say yes to be polite | Ask about past behavior: "Have you...?" not "Would you...?" |
| Long interviews | You get tired, they get bored, signals get missed | 20-30 minutes max |
| No note-taking | You forget what they said, remember your interpretation | Record (with permission) or verbatim notes |
| Interviewing competitor users | They might switch for free, that's not demand | Interview people who haven't solved it yet |
| Feeling good after each interview | Confirmation bias, you hear what you want | Wait for patterns across 5+ interviews before celebrating |
```

Show evidence scorecard:

```markdown
# Evidence Scorecard: What Counts?

## Real Evidence of Demand ✅ (High Signal)
- Someone offered to pay or asked for early access (unsolicited)
- Someone is actively trying to solve this problem (spending time/money on existing solutions)
- Someone introduced you to other people with the same problem
- Someone asked YOU follow-up questions about how you'd solve it
- Same core problem mentioned by 3+ strangers unprompted
- Someone changed their behavior or workflow based on talking to you

## Weak Evidence ⚠️ (Polite Interest)
- "That sounds interesting"
- "I'd love to stay updated"
- "That could be useful"
- "Let me know when you launch"
- "I'll definitely check it out"
- Only 1 person mentioned the problem, nobody else did

## No Evidence ❌ (Sounds Polite)
- "Cool idea"
- General enthusiasm without specifics
- Just agreeing with you
```

Use AskUserQuestion:

**Re-ground:** You now understand the anti-patterns that destroy evidence and the signal vs. noise scorecard. This is how you'll evaluate each interview as you conduct them.

**Simplify:** As you interview people, you'll track what they say in EVIDENCE-LOG.md. You'll mark each statement as high signal, weak signal, or no signal. By interview 5, you'll see patterns.

**Recommend:** RECOMMENDATION: Create EVIDENCE-LOG.md now and fill it in after each interview. This trains you to listen for signal vs. noise in real-time. Completeness: 10/10 if you update it within hours of each interview while memory is fresh.

**Options:**
- A) "I understand, I'm ready to start interviews"
- B) "I want to do a practice interview first"
- C) "I'm worried my questions will be too leading"

**Move to Phase 5.**

---

## Phase 5: The Hard Stop

**This is where the pipeline STOPS until you complete interviews and evidence collection.**

Use AskUserQuestion:

**Re-ground:** Before you proceed to the next stage (MVP scoping), you MUST complete 5-10 real customer interviews and document what you learned in EVIDENCE-LOG.md.

**Simplify:** You do interviews. You fill in EVIDENCE-LOG.md. You come back when done. Then evidence-review will analyze what you found and either green-light you to Stage 3 or tell you to do more interviews.

**Recommend:** RECOMMENDATION: Block out this week. Schedule interviews for the next 10-14 days. Hit the goal of 5+ strangers before you come back. Completeness: 10/10 if you have 5-10 interviews completed and logged.

**Options:**
- A) "I'm ready, I'll go do the interviews"
- B) "Can I do this asynchronously?"
- C) "I need help reaching out to people"

---

## Completion Status

**RETURN WHEN:** You have completed 5-10 customer interviews and documented them in EVIDENCE-LOG.md.

**Next Step:** Proceed to evidence-review skill for adversarial analysis of your interview quality and evidence.

Return to z-combinator orchestrator for routing.
