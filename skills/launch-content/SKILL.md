---
name: launch-content
description: Generates launch announcement content for multiple channels. Product Hunt, Hacker News, Twitter thread, email to early users, LinkedIn, elevator pitch. Grounded in lean canvas and customer interview language.
benefits-from: launch-checklist
feeds-into: null
---

# Launch Content Generator

Create multi-channel launch content grounded in real customer language, not marketing fluff.

---

## Phase 0: Source Material & Strategy

**Purpose:** Load the inputs for content creation.

1. Read LEAN-CANVAS.md (positioning, unique value, target user)
2. Read EVIDENCE-LOG.md (customer interview quotes — these are gold)
3. Read MARKET-RESEARCH.md (competitive positioning, if exists)
4. Confirm launch date and channels to focus on

**Exit Criteria:** All source materials loaded, channel list confirmed.

**AI Instructions:**
Do not ask any questions. Load context silently. Proceed to Phase 1.

---

## Phase 1: Core Message & Positioning (AskUserQuestion)

**Purpose:** Lock in the core narrative before writing channel-specific content.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Launch content starts with one coherent story. We're about to create that story for [launch date]."

**Simplify:** "What's the core problem you solved? Who's struggling with it? How do you solve it differently than alternatives? Boil this down to 2-3 sentences."

**Recommend:** "RECOMMENDATION: Use a real customer quote if possible. 'I lose 2 hours a day to X' beats 'we built a productivity tool.'"

**Options:**
- A) Problem + your solution + who it's for (3-part narrative)
- B) Real customer quote + problem + solution (if quote available)
- C) Quick positioning statement from LEAN-CANVAS.md (use existing if available)

**Exit Criteria:** Core narrative confirmed. Store as reference for all channel content. Proceed to Phase 2.

---

## Phase 2: Product Hunt Content (AskUserQuestion)

**Purpose:** Create PH listing with title, tagline, and description.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Product Hunt is your biggest visibility play on launch day. Title and description must hook in 15 seconds."

**Simplify:** "Think catchy. 'Superhuman for email — keyboard-first. 0 inbox in 3 days.' That's a good title. Avoid generic adjectives (amazing, powerful, revolutionary)."

**Recommend:** "RECOMMENDATION: Lead with problem or customer quote. Show the product working. End with a clear CTA (free accounts, beta access, etc.)"

**Options:**
- A) Full PH description: title, tagline, 2-3 paragraph description, first comment
- B) Just the title and tagline (write description later)
- C) Use LEAN-CANVAS positioning as-is (not ideal for PH tone)

**If full description chosen:**
Use **AskUserQuestion** for first comment:

**Re-ground:** "First comment on your own PH post is where you add context. What did you learn building this? What's next?"

**Simplify:** "This is where skeptics ask questions. You answer: how is this different? What feedback are you getting? How can people contact you?"

**Recommend:** "RECOMMENDATION: Be humble and specific. 'We spent 6 months interviewing users' beats 'we're disrupting the market.'"

**Options:**
- A) Full first comment (learnings, comparison to alternatives, what's next, how to give feedback)
- B) Short version (just key differentiator and next feature)

**Exit Criteria:** PH content locked in. Proceed to Phase 3.

---

## Phase 3: Hacker News Content (Automated, No Question)

**Purpose:** Create HN "Show HN" post (if applicable).

**AI Instructions:**
Only create if the product is technical or has interesting technical depth.

If technical, create HN post with this format:

```
Show HN: [Product Name] – [One-line description]

[2-4 paragraphs]
- Paragraph 1: The problem and team background
- Paragraph 2: The insight you discovered
- Paragraph 3: Your solution and how it works
- Paragraph 4: Call-to-action + GitHub link (if applicable)

Tone: Direct, genuine, specific. No marketing language.
Example problems to highlight: technical challenge solved, inefficiency addressed, market gap identified.
Avoid: TAM claims, "disruption" language, hype.
```

If non-technical or HN is not a priority, skip this phase.

Use **AskUserQuestion**:

**Re-ground:** "Hacker News: should we create a 'Show HN' post? HN users have high BS detectors."

**Simplify:** "If your product has interesting technical depth, HN is valuable. If it's a UI-focused consumer app, skip HN."

**Recommend:** "RECOMMENDATION: HN posts that mention open-source components or interesting engineering challenges do well."

**Options:**
- A) Create full HN post (prioritize technical details and challenges solved)
- B) Mention code/component + get feedback from HN (lighter version)
- C) Skip HN entirely (not a good fit for this product)

**Exit Criteria:** HN content created (or skipped). Proceed to Phase 4.

---

## Phase 4: Twitter Launch Thread (AskUserQuestion)

**Purpose:** Create 5-7 tweet thread for launch day.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Twitter is your real-time channel. A launch thread reaches your audience and creates shareable moments."

**Simplify:** "Structure: hook (what you shipped) → problem (why it matters) → solution (how it works) → proof (user quotes) → CTA (try it)."

**Recommend:** "RECOMMENDATION: Use a real customer quote. Include a screenshot or GIF if possible. End with a question to drive engagement."

**Options:**
- A) Full 7-tweet thread with all elements (hook, problem, solution, proof, features, CTA, engagement question)
- B) 5-tweet thread (shorter, focuses on essentials)
- C) Just the hook tweet (post more later)

**Exit Criteria:** Twitter thread content locked in. Proceed to Phase 5.

---

## Phase 5: Email to Early Users (AskUserQuestion)

**Purpose:** Create personalized email to your beta testers and early advocates.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Early users shaped your product. This email is a personal note saying 'we're live, and thanks for the feedback.'"

**Simplify:** "Tone: personal, specific (reference their feedback), grateful. This isn't a broadcast — it's 1-to-1."

**Recommend:** "RECOMMENDATION: Mention a specific pain point they mentioned in interviews. Show you listened. Give them free/special access."

**Options:**
- A) Full personalized email template (with placeholders for name, feedback, feature request)
- B) Mass email version (less personal, but faster to send)
- C) Skip email (rely on Twitter and PH)

**Exit Criteria:** Email template locked in. Proceed to Phase 6.

---

## Phase 6: LinkedIn Post (Automated, No Question)

**Purpose:** Create a LinkedIn post for B2B/network reach.

**AI Instructions:**
Create LinkedIn post (different tone from PH and Twitter — more professional, less hype).

Format:

```
I usually don't post about work, but this one matters.

We spent [timeframe] building [Product] because every [user type] we talked to was struggling with [problem].

Today we're live.

It's designed for [specific persona]. It does [core value] in [timeframe/cost].

Early users are saying: "[Real quote]"

If this sounds relevant to you, try it: [Link]

[Optional] We're hiring [role] if you know someone.
```

Tone: Authentic, not salesy. Personal perspective. Specific outcomes.

**Exit Criteria:** LinkedIn content created. Proceed to Phase 7.

---

## Phase 7: Elevator Pitch (Automated, No Question)

**Purpose:** Create a 30-second in-person pitch for networking.

**AI Instructions:**
Create natural-sounding elevator pitch:

```
"We built [Product]. It's for [target user]. The big problem is [pain point].
We solve it by [core mechanism].

Instead of [old way which takes X time/costs Y], you can [new way which takes A time/costs B].
We're live now."

Then ask: "Does this resonate with anyone you know?"
```

Tone: Natural conversation, not robotic. Be comfortable saying this to a stranger at a conference.

**Exit Criteria:** Elevator pitch created. Proceed to Phase 8.

---

## Phase 8: Authenticity Audit & Final Review (AskUserQuestion)

**Purpose:** Verify all content passes authenticity check before publishing.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Before you publish, let's audit the content. Marketing language dies. Real problems resonate."

**Simplify:** "Does your content pass the dinner test? Would you say it naturally to a friend? Or does it feel like corporate fluff?"

**Recommend:** "RECOMMENDATION: If you see buzzwords (revolutionary, cutting-edge, game-changing, disrupt), rewrite. Use customer language instead."

**Options:**
- A) Audit all content against checklist (provided below)
- B) Just spot-check key pieces (PH + Twitter)
- C) Proceed as-is (risky)

**Authenticity Checklist (for each piece of content):**
- Does any quote come from a real customer interview? (If you claim a quote, it must be real)
- Would you say this at dinner with friends? (No corporate speak)
- Does it explain the WHY, not just the WHAT? (Problem + solution)
- Zero buzzwords: revolutionary, cutting-edge, game-changing, disruptive, innovative? (Check)
- Clear ask: try it, give feedback, apply, tell a friend? (Check)

If any "NO," rewrite that content.

**Exit Criteria:** All content passes authenticity audit. Proceed to Phase 9.

---

## Phase 9: Distribution Schedule & Output (AskUserQuestion)

**Purpose:** Plan timing for each channel.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "You have content for 5+ channels. Timing matters. Launch day morning, Product Hunt goes first."

**Simplify:** "Which channels matter most for your audience? When should you post to each?"

**Recommend:** "RECOMMENDATION: Product Hunt (early Tuesday morning) → Twitter thread (same morning) → Email (immediately after launch) → LinkedIn (same day) → Press (if you have contacts, give them 24-hour heads up)."

**Options:**
- A) Full schedule with posting times for each channel (exact timestamps)
- B) General order (PH first, Twitter second, email third)
- C) Just the channels you'll use (skip ones not applicable)

**Exit Criteria:** Distribution schedule confirmed. Proceed to Phase 10.

---

## Phase 10: Output & Archive

**Purpose:** Create the launch content kit document.

**AI Instructions:**
Create LAUNCH-CONTENT.md with this format:

```markdown
# Launch Content Kit

**Launch Date**: [Date]
**Channels**: [List of channels being used]

---

## Core Message (For All Channels)

**Problem**: [What are users struggling with?]
**Solution**: [How do you solve it?]
**Target User**: [Who is this for?]
**Why Now**: [Why should they care today?]

**Key Quote** (from customer interviews):
"[Real quote from EVIDENCE-LOG]"

---

## Product Hunt

**Title**:
[One-line hook, <10 words, specific not generic]

Example good titles:
- "Superhuman for email—keyboard-first. 0 inbox in 3 days."
- "Cold email at scale, without the spam score hit."

**Tagline**:
[One sentence. The core problem you solve.]

**Description**:
[2-3 paragraphs. Lead with problem or customer quote. Describe experience. End with CTA.]

---

[Insert full description here]

---

**First Comment** (expanded context):
[Public comment on your own product]

---

[Insert first comment here]

---

## Hacker News "Show HN" Post

(Include only if applicable — product has technical depth)

**Title**:
Show HN: [Product Name] – [One-line description]

**Body**:

---

[Insert HN post here]

---

---

## Twitter/X Launch Thread

**Platform**: Twitter/X
**Timing**: Launch day morning (for maximum visibility)
**Format**: 5-7 tweets

**Tweet 1 (Hook)**:
[Problem + core promise + link]

**Tweet 2 (Problem)**:
[Specific frustration users face]

**Tweet 3 (Solution)**:
[How you solve it, with screenshot if possible]

**Tweet 4 (Social Proof)**:
[Real customer quote from beta users]

**Tweet 5 (Features)**:
[What you get, time to value]

**Tweet 6 (CTA)**:
[Offer: free accounts, beta access, discount]

**Tweet 7 (Engagement)**:
[Question to drive replies]

---

[Insert all tweets here]

---

## Email to Early Users

**Subject Line**:
[Name], we're live — [Product] is ready (and you get free access)

**Body**:

---

[Insert email here]

---

**Send timing**: Immediately after launch goes live
**Personalization**: Customize [Name] and specific feedback reference for each recipient

---

## LinkedIn Post

**Tone**: Personal, authentic, specific outcomes
**Timing**: Same day as launch

---

[Insert LinkedIn post here]

---

## 30-Second Elevator Pitch

(In-person, at conferences, to investors, to potential users)

**Say this naturally:**

"We built [Product]. It's for [target user]. The big problem is [pain point]. We solve it by [core mechanism]. Instead of [old way], you can [new way]. We're live now."

**Then ask:**
"Does this resonate with anyone you know?"

---

## Distribution Checklist

**Week Before Launch:**
- [ ] All content drafted
- [ ] Authenticity audit passed
- [ ] Early users list prepared for email
- [ ] PH account ready (hunter profile ready if doing community launch)
- [ ] Social media accounts linked and tested
- [ ] Links finalized and tested

**Launch Day Morning:**
- [ ] Product live and tested (all links work)
- [ ] PH post scheduled (early Tuesday morning)
- [ ] Twitter thread scheduled or ready to post manually
- [ ] Email template loaded into email service
- [ ] LinkedIn post ready
- [ ] You're available for live engagement (PH comments, Twitter replies, email)

**Launch Day Execution:**
- [ ] 8 AM PT: Post to Product Hunt
- [ ] 8:05 AM PT: Post Twitter thread (or schedule if early)
- [ ] 8:15 AM: Start monitoring Product Hunt comments
- [ ] 9:00 AM PT: Send email to early users
- [ ] 10:00 AM PT: Post to LinkedIn
- [ ] Throughout day: Engage with comments/questions

**If applicable:**
- [ ] Press outreach (24-hour heads up if you have journalist contacts)
- [ ] Slack/Discord announcement (if you have a community)
- [ ] Reddit post (if applicable and if rules allow)

---

## Authenticity Checklist

Before publishing, confirm:
- [ ] Every quote comes from a real customer interview (EVIDENCE-LOG)
- [ ] No buzzwords: revolutionary, cutting-edge, game-changing, disrupt, innovative
- [ ] Every piece explains the WHY (problem) not just the WHAT (solution)
- [ ] Would you say this to a friend at dinner? (No corporate speak)
- [ ] Clear ask in every piece: try it, give feedback, apply, refer someone

If any checked items fail, rewrite before publishing.

---

## Archive Notes

- **PH Page URL**: [URL once live]
- **Launch Metrics**: [Update after launch day — upvotes, comments, signups]
- **Key Feedback**: [Themes from user comments, questions, issues]
- **Next Actions**: [Features people asked for, support patterns]
```

**Tone Guidance:**
- Customer language > marketing language
- Specific > vague
- Authentic > polished
- "Real problems resonate. Marketing language dies."

---

## Escape Hatches

**If user is impatient ("just do it"):**
- Skip Phases 1-2. Use LEAN-CANVAS directly.
- Create PH content and Twitter thread only (skip HN, LinkedIn, email).
- Output a condensed content kit.

**If launch is in < 3 days:**
- Focus on top 3 channels (PH, Twitter, Email).
- Skip HN and LinkedIn (require more lead time).

**If no customer quotes available:**
- Use problem statements from EVIDENCE-LOG instead of direct quotes.
- Focus on specificity: "Our users lose 2 hours a day to X" beats "productivity tool."

**If non-technical product:**
- Skip HN entirely.
- Focus on PH, Twitter, Email, LinkedIn.

---

## When to Run

- **1 week before launch** (gives time to refine and gather feedback)
- **3-4 days before launch** (finalize and schedule posts)
- **Launch day morning** (go live with execution)

---

## Completion Status

At the end of the skill, report one of:
- **DONE**: All content created, authenticity audit passed, distribution schedule confirmed
- **DONE_WITH_CONCERNS**: Content created but some rewrites needed (buzzwords, vague claims)
- **BLOCKED**: Missing LEAN-CANVAS.md or EVIDENCE-LOG.md
- **NEEDS_CONTEXT**: Unclear which channels to prioritize; ask user for audience profile
