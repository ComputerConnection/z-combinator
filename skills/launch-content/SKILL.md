---
name: launch-content
description: Generates launch announcement content for multiple channels. Product Hunt, Hacker News, Twitter thread, email to early users, LinkedIn, elevator pitch. Grounded in lean canvas and customer interview language.
---

# Launch Content Generator

Create launch announcement content tailored to each channel. Use authentic language from customer interviews, not marketing fluff.

## What You Do

1. Read LEAN-CANVAS.md to understand positioning and unique value
2. Read EVIDENCE-LOG.md to find customer interview quotes
3. Read MARKET-RESEARCH.md to understand competitive positioning
4. Create content for each channel below
5. All content should answer: "Why should I care? Why now?"
6. Use direct quotes from customers where possible
7. Avoid hype language — be specific about what you built and who it's for

## Output: LAUNCH-CONTENT.md

Format:

```
# Launch Content Kit

## Product Hunt

**Title:**
[One-line hook. Should fit in social media preview. Examples: "Superhuman for email—keyboard-first. 0 inbox in 3 days." or "Cold email at scale, without the spam score hit."]

**Tagline:**
[One sentence. The core problem you solve. Example: "Find product opportunities without spending hours on Reddit."]

**Description:**
[2-3 paragraphs. Lead with customer quote or problem. Describe the core experience. End with call-to-action.]

Example structure:
---
[Customer quote from EVIDENCE-LOG: "I was losing 2 hours a day to X and nobody had solved it."]

We built [Product] because [founding story - max 1 sentence].

You get [core feature 1], [core feature 2], [core feature 3]. Setup takes 5 minutes.

We're giving 100 free accounts to the Product Hunt community. Go grab one.
---

**First Comment (expanded context):**
[Public comment on your own product. This is where you add:
- What you learned building this
- Honest comparison to alternatives (if any)
- What you're building next
- How to get feedback
- Your Slack/Discord/Twitter for questions]

Example:
---
Hey everyone! Grateful to be here. Quick context:

We spent 6 months interviewing [target user] and found that [insight]. Existing tools require [pain point], so we built [your solution] instead.

The core workflow: [How someone uses your product in 15 seconds]

We know this isn't for everyone. It's designed for [specific persona], not [what you're NOT trying to do].

Next sprint: [Feature people are asking for]. We're also open to feedback — reply here or ping us on Twitter @[handle].

We've reserved 100 free accounts for PH users if you want to try it.

Thanks for all the questions!
---

## Hacker News "Show HN" Post

**Title:**
Show HN: [Product] – [One-line description]

**Body:**
[2-4 paragraphs. Lead with problem, describe solution, include link. HN users hate fluff.]

Example structure:
---
Hey HN. We built [Product] to solve [problem].

We're a team of [background]. We spent [timeframe] talking to [user type] and noticed [insight]. Every solution we found required [pain point], so we built [our solution].

The core idea: [How it works in 2 sentences].

We've open-sourced [component if applicable]. We'd love feedback on [specific question]. The code is at [GitHub link].

[Product link]
---

**Remember:** HN users can smell marketing from a mile away. Be genuine. Be specific. Talk about the technical challenge, not the TAM.

## Twitter/X Launch Thread (5-7 tweets)

Tweet 1 (hook):
We just shipped [Product]. It does [core promise] in [timeframe/cost/effort reduction].

This solves the worst part of [job to be done].

[Link to product]

Tweet 2 (problem):
Background: We were frustrated with [specific pain]. The existing options either...

Tweet 3 (solution):
So we built a [category] that [unique approach].

[Details or screenshot]

Tweet 4 (social proof):
Early feedback from beta users: [Quote from customer interview]

Tweet 5 (features):
You get [feature 1], [feature 2], [feature 3]. Setup is 5 minutes.

Tweet 6 (CTA):
[Offer: free accounts, discount, beta access, etc.]

Try it: [Link]

Tweet 7 (engagement):
What's the biggest pain point you face with [related tool/process]? We're collecting feedback for our roadmap.

**Thread tone:** Direct, specific, authentic. Not "excited to announce." Say "we built this because X sucked."

## Email to Early Users

**Subject line:**
[Name], we're live — [Product] is ready (and you get free access)

**Body:**

Dear [Name],

Remember when we talked about [problem they mentioned]? We finally built it.

[Product] is live today. You helped shape the early version, so you're getting free access for [timeframe] as our way of saying thanks.

[Screenshot or 15-second description of how it works]

The core workflow:
1. [Step 1]
2. [Step 2]
3. [Step 3]

You mentioned you were struggling with [specific mention from conversation]. This is where you'd do [how your product solves it].

Your feedback from the beta was critical. We're planning [feature they asked for] next sprint based on what you shared.

Go try it here: [Link]

Questions? Hit reply. I'm personally monitoring responses.

[Your name]

---

## LinkedIn Post

**Format: Short + authentic**

I usually don't post about work, but this one matters.

We spent 6 months building [Product] because every [user type] we talked to was struggling with [problem].

Today we're live.

It's designed for [specific persona]. It does [core value] in [timeframe/cost].

We've got [number] early users already saying things like [quote].

If this sounds relevant to you or someone you know, try it: [Link]

We're also hiring [role] if you know someone.

---

## 30-Second Elevator Pitch (In-person)

**Say this naturally (not robotic):**

"We built [Product]. It's for [target user]. The big problem is [pain point]. We solve it by [core mechanism]. Instead of [old way which takes X time/costs Y], you can [new way which takes A time/costs B]. We're live now."

**Then ask:** "Does this resonate with anyone you know?"

## Distribution Notes

- **Product Hunt**: Launch early Tuesday morning (more visibility)
- **Hacker News**: Post at 8-9 AM PT on weekday (peak traffic)
- **Twitter**: Thread on launch day morning, then retweet throughout week
- **Email**: Send immediately after launch goes live
- **LinkedIn**: Post same day
- **Press**: If you have journalist contacts, give them 24-hour heads up

## Authenticity Check

Before publishing anything, ask:
- Does this quote come from a real customer interview? ✓
- Would I say this at dinner with friends? ✓
- Does it explain the *why* not just the *what*? ✓
- Did I avoid buzzwords (revolutionary, cutting-edge, game-changing)? ✓
- Is there a specific ask (try it, give feedback, apply)? ✓

If no to any: rewrite.
```

Use actual customer language. If someone in EVIDENCE-LOG said "Ugh, I lose 2 hours a day to X," use that phrasing. Real problems resonate. Marketing language dies.
