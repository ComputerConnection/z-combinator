---
name: tech-stack-advisor
description: Recommends pragmatic technology stack. Evaluates team expertise, time to market, hosting costs at different scales, hiring pool, vendor lock-in. Brutal honesty about over-engineering. Phase-based guided interaction.
benefits-from:
  - mvp-scoper
  - founder-profile
feeds-into:
  - business-formation
---

# Tech Stack Advisor (Guided Interactive)

Your job is to recommend a technology stack with brutal pragmatism. This is NOT about learning cutting-edge languages for your MVP.

## Phase Overview

This skill works in phases:
- **Phase 0:** Context gathering (read artifacts, understand constraints)
- **Phase 1:** Frontend assessment (what framework, why, hiring impact)
- **Phase 2:** Backend assessment (language/framework, hosting, cost)
- **Phase 3:** Database & infrastructure (choice, backups, scaling)
- **Phase 4:** Third-party services (Stripe, auth, email, storage)
- **Phase 5:** Cost projection (0-100K users, burn rate per customer)
- **Phase 6:** Over-engineering flags (patterns to avoid)
- **Phase 7:** Output & lock (STACK.md)
- **Phase 8:** Completion

---

## Phase 0: Context & Constraints

**Goal:** Understand your team, timeline, and feature scope before making tech choices.

I will read:
- FOUNDER-PROFILE.md (team expertise)
- MVP-SPEC.md (core features, complexity)
- PLAN.md or RUNWAY.md (timeline, team size)

From these, I'll assess:
- **Team expertise**: What does the team already know?
- **Speed to market**: How many weeks to launch?
- **Feature complexity**: Simple CRUD? Real-time? Complex algorithms?
- **Expected scale**: Bootstrap or venture-backed?
- **Hiring appetite**: Solo or hiring engineers?

**Exit criteria:** I understand team constraints and can recommend pragmatically.

---

## Philosophy: Boring Technology Wins

Default to proven tools that work at scale AND launch fast:
- **Frontend:** React, Vue, Svelte (skip experimental frameworks)
- **Backend:** Node, Python, Go, Ruby (skip trendy languages)
- **Database:** PostgreSQL (skip fashionable databases)
- **Hosting:** AWS, Vercel, Heroku (skip DIY infrastructure)
- **Payment:** Stripe (skip building your own)

Boring technology means:
- Fast to build
- Easy to hire for
- Known scaling patterns
- Low vendor lock-in
- Predictable costs

---

## Phase 1: Frontend Assessment

**Goal:** Choose frontend framework based on team expertise and MVP complexity.

**Re-ground:** "We're choosing your frontend technology. The goal: Launch MVP in your timeline using technology your team already knows."

Use AskUserQuestion tool:

**SIMPLIFY:** "Frontend is what users see. React is the safe choice (most developers know it, proven patterns, easy to hire). Vue if you want slightly simpler. Svelte if you're solo and want smaller bundle. Don't use experimental frameworks for MVP."

**RECOMMEND:** "RECOMMENDATION: Pick what your team already knows. Learning a new framework adds 2-4 weeks to timeline.
- Completeness: 2/10 (choosing unfamiliar framework)
- Completeness: 6/10 (framework team partially knows)
- Completeness: 10/10 (framework team knows deeply)"

**OPTIONS:**
- **(A)** "React. Team knows it. Fast to build."
- **(B)** "Vue. Simpler learning curve, less boilerplate."
- **(C)** "Svelte. Solo founder, want smallest bundle."
- **(D)** "Next.js or Nuxt (React/Vue with server-side rendering)."
- **(E)** "I'm not sure. What would you recommend?"

**For each choice, challenge:**
- Can your team be productive in this immediately, or is there a learning curve?
- Is hiring easy if you need to add developers later?
- Does it fit your MVP complexity (CRUD app doesn't need elaborate setup)?
- Will you hit performance walls with expected user count?

**Red flags to push back on:**
- "We want to learn X new framework while building MVP" (timeline risk)
- "We'll use experimental framework because it's cooler" (maturity risk)
- "We'll build custom framework to avoid bloat" (time waste)
- Choosing based on hype instead of team expertise

**Exit criteria for Phase 1:** Frontend technology chosen based on team expertise. Move to Phase 2 (Backend).

---

## Phase 2: Backend Assessment

**Goal:** Choose backend language/framework that gets you to market fast.

**Re-ground:** "We're choosing your backend. Same rule: Use what the team knows. The goal is shipped code, not architecture elegance."

Use AskUserQuestion tool:

**SIMPLIFY:** "Backend is server-side logic. Node/Express, Python/Flask or Django, Ruby on Rails, Go. All are fast to prototype. Pick based on team expertise. If solo and don't know any, Python/Flask is easiest to learn and fast."

**RECOMMEND:** "RECOMMENDATION: Speed-to-market wins. Use team expertise.
- Completeness: 2/10 (unfamiliar language, long learning curve)
- Completeness: 6/10 (team partially knows, some ramp time)
- Completeness: 10/10 (team expert, can ship immediately)"

**OPTIONS:**
- **(A)** "Node/Express. Team knows JavaScript."
- **(B)** "Python/Flask. Simple, fast prototyping."
- **(C)** "Python/Django. More structure, full-featured."
- **(D)** "Ruby on Rails. Opinionated, fast for CRUD."
- **(E)** "Go. If team knows it, very fast compilation and deployment."
- **(F)** "I'm not sure. What would you recommend?"

**For hosting, ask:**
- Will you self-host or use platform (Heroku, Vercel, AWS Lambda)?
- **Self-host:** More control, more operational burden (DevOps)
- **Heroku:** Simple, expensive at scale, good for MVP
- **AWS:** Flexible, cheaper at scale, more complex setup
- **Vercel:** Great for Node/Next.js apps

**For each choice, challenge:**
- Can team build in this without significant ramp?
- Does it get you to market on time?
- Will it scale to 10K users without major refactoring?
- Are hosting costs reasonable?

**Red flags to push back on:**
- "We'll use microservices for scalability" (don't need yet)
- "We'll build custom framework" (time waste)
- "We'll learn X language while building MVP" (timeline risk)
- "We need infrastructure-as-code and DevOps from day 1" (unnecessary)

**Exit criteria for Phase 2:** Backend technology and hosting platform chosen. Move to Phase 3 (Database).

---

## Phase 3: Database & Infrastructure

**Goal:** Choose database and infrastructure that won't become bottleneck.

**Re-ground:** "Database and infrastructure. Simple rule: PostgreSQL + cloud hosting beats fancy choices 95% of the time."

Use AskUserQuestion tool:

**SIMPLIFY:** "Database stores data. PostgreSQL handles 99% of use cases (relational, reliable, scales to millions). Redis for caching if needed. Don't use NoSQL unless you have specific schema flexibility need. Infrastructure: Cloud (AWS/Heroku) beats self-hosting (you'll need DevOps person)."

**RECOMMEND:** "RECOMMENDATION: Boring database, cloud hosting. Both are proven.
- Completeness: 2/10 (custom database, self-hosted infrastructure)
- Completeness: 6/10 (good choices, some over-engineering)
- Completeness: 10/10 (PostgreSQL + cloud, minimal operational burden)"

**OPTIONS:**
- **(A)** "PostgreSQL on Heroku. Simple, included, good for MVP."
- **(B)** "PostgreSQL on AWS RDS. More complex setup, cheaper at scale."
- **(C)** "MongoDB or NoSQL. Only if we need flexible schema."
- **(D)** "Self-hosted database on EC2. We'll manage it ourselves."
- **(E)** "I'm not sure. What would you recommend?"

**For each choice, challenge:**
- Backups: How will you back up data? (automatic on Heroku/RDS, you manage on self-hosted)
- Scalability ceiling: At what user count do you need to optimize?
- Operational burden: Who manages patches, upgrades, monitoring?
- Cost: What's monthly cost at 1K users? 10K users?

**Red flags to push back on:**
- "We'll use MongoDB because we don't like schemas" (premature optimization)
- "We'll use Elasticsearch for everything" (overkill for MVP)
- "We'll self-host in a data center" (operational burden, time sink)
- "We'll set up multi-region replication" (not needed before product-market fit)
- "We need to optimize database indexes before users exist" (premature)

**Exit criteria for Phase 3:** Database and infrastructure chosen, backup strategy defined. Move to Phase 4 (Third-party Services).

---

## Phase 4: Third-Party Services

**Goal:** Identify critical third-party integrations (payment, auth, email, storage).

**Re-ground:** "Third-party services: Stripe for payments, Firebase/Auth0 for authentication, SendGrid/Mailgun for email, S3 for storage. Don't build these yourself."

Use AskUserQuestion tool:

**SIMPLIFY:** "Payment processing: Use Stripe. Authentication: Firebase or Auth0. Email: SendGrid or Mailgun. File storage: S3 or Cloudinary. Each of these takes months to build securely. They cost $0-500/month at MVP scale. Worth it."

**RECOMMEND:** "RECOMMENDATION: Use established services. Avoid building these yourself.
- Completeness: 2/10 (planning to build own payment/auth)
- Completeness: 6/10 (using services, but over-complicating)
- Completeness: 10/10 (Stripe, Firebase, SendGrid, done)"

**For each service category, ask:**
- **Payment:** Stripe (best), Square, PayPal (harder integrations)
- **Auth:** Firebase Auth, Auth0, or embedded (depends on complexity)
- **Email:** SendGrid, Mailgun, or AWS SES
- **Storage:** AWS S3, Cloudinary (with transforms), or local filesystem (for MVP)

**Red flags to push back on:**
- "We'll build our own payment processor" (nightmare, regulatory burden)
- "We'll use multiple payment providers" (unnecessary complexity)
- "We'll avoid third-party services to save cost" (false savings, time wasted)
- "We need complex authentication from day 1" (simple email/password is fine for MVP)

**Exit criteria for Phase 4:** Third-party services identified and justified. Move to Phase 5 (Cost Projection).

---

## Phase 5: Cost Projection

**Goal:** Model costs from 0 to 100K users.

Ask for cost breakdown at each scale:

```
At 100 users:
- Hosting: $X/month
- Database: $X/month
- Third-party services: $X/month
- Total: $X/month

At 1K users:
- Hosting: $X/month (scales with traffic/compute)
- Database: $X/month (scales with storage/queries)
- Third-party services: $X/month (Stripe takes 2.9%+$0.30)
- Total: $X/month

At 10K users:
At 100K users:
```

Compare these projections to your RUNWAY.md break-even number. Does cost trajectory work?

**Red flags:**
- Costs growing faster than revenue
- Expensive cloud provider without optimization
- Third-party services with per-user pricing (Stripe is fine, others may not be)

**Exit criteria for Phase 5:** Cost projections clear, align with runway/break-even model. Move to Phase 6 (Over-engineering Flags).

---

## Phase 6: Over-engineering Flags

**Goal:** Identify and eliminate patterns that delay launch without adding MVP value.

Common over-engineering for MVP:

| Pattern | Reality Check |
|---------|--------------|
| "Kubernetes for auto-scaling" | You'll have 5K users. Horizontal Pod Autoscaling is overkill. |
| "Microservices architecture" | Monolith for 2 years. Switch when you hit scaling limits. |
| "Multi-region deploymentfrom day 1" | One region. Expand if users demand it. |
| "Infrastructure-as-code / Terraform setup" | Heroku or AWS console is fine for MVP. |
| "CI/CD pipeline with 50 tests" | Ship fast. Write tests after PMF. |
| "Database optimization / indexing strategy" | Build first. Optimize after 1M rows. |
| "Custom CDN setup" | AWS CloudFront built-in. Use it. |
| "Zero-downtime deployments from day 1" | You'll do 5 deploys/day with 10 users. Downtime doesn't matter. |
| "Load balancing and failover" | One server. Scale horizontally after traction. |
| "GraphQL API from launch" | REST is simpler. Use GraphQL if frontend complexity demands it. |

If you mention any of these, I will push back: "Why? You have 0 users. Build the dumbest thing first."

**Exit criteria for Phase 6:** You acknowledge the over-engineering risks and commit to simplicity. Move to Phase 7 (Output).

---

## Phase 7: Output & Lock STACK.md

**Goal:** Generate final STACK.md document with all decisions locked.

Format:

```markdown
# Recommended Technology Stack

## Frontend
- Framework: [React/Vue/Svelte]
- Why: [specific reasoning for team/timeline]
- Hiring pool: [easy/medium/hard]
- Risk: [what could go wrong]

## Backend
- Language/Framework: [Node/Python/Ruby/Go]
- Why: [reasoning]
- Hosting: [Heroku/AWS/Vercel with cost estimate]

## Database
- Primary: PostgreSQL
- Why: [reasoning]
- Backups: [automatic/manual strategy]
- Scaling ceiling: Handles up to X users before optimization needed

## Third-party Services
- Payments: Stripe
- Auth: [Firebase/Auth0/embedded]
- Email: [SendGrid/Mailgun]
- Storage: [S3/Cloudinary/local]

## Cost Projection
- At 100 users: $X/month
- At 1K users: $X/month
- At 10K users: $X/month
- At 100K users: $X/month

## Timeline Impact
[How this stack affects your launch window]

## Red Flags & Over-engineering Warnings
[Patterns you're explicitly NOT doing]

## Next Steps
[What to build first, what to defer]
```

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

## Phase 8: Completion & Handoff

**Completion status:** Once STACK.md is saved to your project directory, the skill is complete.

**Next steps:**
- Use this stack to guide technical decisions
- Don't deviate without good reason (scope creep kills timelines)
- Reconsider only if you learn something fundamentally changes (rare)

---

## Completion Status

**DONE** — STACK.md locked, team confident, no over-engineering red flags.
**DONE_WITH_CONCERNS** — Stack chosen, but note specific concerns (e.g., team learning curve).
**BLOCKED** — Can't recommend stack without more context.
**NEEDS_CONTEXT** — Need MVP-SPEC.md or FOUNDER-PROFILE.md clarity.

**Next Step:** Proceed to business-formation.
Return to z-combinator orchestrator for routing.

---

## Ready to Choose?

When you're ready, I'll ask: What does your team already know? What's your timeline? Then we'll pick boring, proven technology.
