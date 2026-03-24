# Z-Combinator Pipeline Map

Complete reference for the Z-Combinator bootcamp pipeline, including all stages, skills, artifacts, gates, and routing logic.

---

## Pipeline Overview

```
FOUNDER-ONBOARDING
        ↓
    STAGE 1: Is This Worth Building?
        ↓
    STAGE 2: Will Anyone Pay?
        ↓
    STAGE 3: What's the MVP?
        ↓
    STAGE 4: Architecture
        ↓
    STAGE 5: Operations
        ↓
    STAGE 6: Build
        ↓
    STAGE 7: Quality
        ↓
    STAGE 8: Launch
        ↓
    STAGE 9: Measure
        ↓
    STAGE 10: Scale
```

---

## Detailed Stage Breakdown

### FOUNDER-ONBOARDING (Entry Point)

**Trigger**: First-time user OR FOUNDER-PROFILE.md missing or incomplete

**Skill**: founder-onboarding

**Artifacts Created**:
- FOUNDER-PROFILE.md
  - Founder name, background, experience level
  - Technical vs. business orientation
  - Known strengths and weaknesses
  - Risk tolerance and ambition level
  - Time commitment and resources available

**Output**: Complete founder profile ready for Stage 1

**Next**: Route to Stage 1: idea-intake

---

### STAGE 1: Is This Worth Building?

**Question**: Does the world need this? Is there a real problem?

**Estimated Duration**: 1-2 weeks

**Skills (In Order)**:
1. **idea-intake** — Define the core idea, problem statement, initial hypothesis
2. **office-hours** (existing gstack) — Workshop the idea with expert feedback
3. **market-research** — Validate market size, trends, and opportunity
4. **plan-shark-tank** (existing gstack) — Prepare pitch for Stage 1 gate evaluation

**Artifacts**:
- IDEA-STATEMENT.md (problem, solution, core hypothesis)
- MARKET-ANALYSIS.md (market size, growth rate, trends)
- COMPETITIVE-LANDSCAPE.md (existing solutions, differentiation)
- PITCH-NOTES.md (talking points for gate evaluation)

**Quality Gate**: Gate Evaluator (Stage 1)
- Evaluates: Problem clarity, market size, competitive differentiation
- Pass Criteria: Problem is real, market exists, solution shows potential
- Fail Outcomes: Iterate on idea, pivot to different problem, or kill

**Gate Scoring**:
- Problem Statement: 1-5
- Market Opportunity: 1-5
- Differentiation: 1-5
- Founder Understanding: 1-5
- Overall: Pass/Fail/Retry

**Next Routing**:
- **Pass**: Proceed to Stage 2: customer-discovery
- **Retry**: Restart Stage 1 or pivot idea
- **Kill**: Sunset project OR save idea for later

---

### STAGE 2: Will Anyone Pay?

**Question**: Can you find customers? Will they spend money?

**Estimated Duration**: 2-4 weeks

**Skills (In Order)**:
1. **customer-discovery** — Identify target customer, initial outreach, interview prep
2. **[PAUSE FOR REAL INTERVIEWS]** — Founder does real customer interviews (documented)
3. **evidence-review** — Analyze interview notes, extract validation signals
4. **plan-shark-tank** (existing gstack, round 2) — Prepare Stage 2 gate pitch with demand evidence

**Artifacts**:
- CUSTOMER-INTERVIEWS.md (raw interview notes, 10+ conversations)
- DEMAND-EVIDENCE.md (analysis of willingness to pay, use cases, timeline)
- CUSTOMER-SEGMENT.md (refined target customer profile)
- PRICING-STRATEGY.md (pricing hypothesis based on interviews)
- PITCH-NOTES-2.md (updated talking points with evidence)

**Quality Gate**: Gate Evaluator (Stage 2)
- Evaluates: Customer validation, demand signals, willingness to pay
- Pass Criteria: Clear demand signal, customers willing to pay, repeatable customer acquisition path visible
- Fail Outcomes: Pivot customer segment, redesign value proposition, or kill

**Gate Scoring**:
- Customer Demand Signal: 1-5
- Willingness to Pay: 1-5
- Customer Acquisition Clarity: 1-5
- Founder Customer Understanding: 1-5
- Overall: Pass/Fail/Retry

**Next Routing**:
- **Pass**: Proceed to Stage 3: lean-canvas
- **Retry**: Run more customer interviews, pivot messaging
- **Kill**: Idea not viable or founder not committed

---

### STAGE 3: What's the MVP?

**Question**: What's the minimum product that proves the core hypothesis?

**Estimated Duration**: 1-2 weeks

**Skills (In Order)**:
1. **lean-canvas** — Map business model, key assumptions, success metrics
2. **mvp-scoper** — Define MVP scope, core features, non-features (what's NOT included)
3. **plan-ceo-review** (existing, SCOPE REDUCTION mode) — CEO review focused on ruthless scope discipline
4. **plan-cfo-review** (existing) — Financial review of MVP build costs, timeline, runway impact
5. **plan-sales-review** (existing) — Sales review of go-to-market strategy for MVP launch

**Artifacts**:
- LEAN-CANVAS.md (business model snapshot)
- MVP-SPEC.md (features, acceptance criteria, non-features)
- SCOPE-CONSTRAINTS.md (what's out of scope, why, for later)
- RESOURCE-PLAN.md (people, budget, timeline for MVP build)
- COST-ANALYSIS.md (build costs, burn rate projection)
- GTM-STRATEGY.md (how you'll get first customers)

**Quality Gate**: Gate Evaluator (Stage 3)
- Evaluates: MVP scope discipline, feasibility, resource alignment
- Pass Criteria: Scope is truly minimal, buildable in 6-12 weeks, clear GTM for MVP
- Fail Outcomes: Reduce scope further, extend timeline, or kill

**Gate Scoring**:
- Scope Discipline: 1-5
- Build Feasibility: 1-5
- Resource Alignment: 1-5
- GTM Clarity: 1-5
- Overall: Pass/Fail/Retry

**Next Routing**:
- **Pass**: Proceed to Stage 4: tech-stack-advisor
- **Retry**: Reduce scope further or adjust resources
- **Kill**: Scope can't go lower without losing core hypothesis

---

### STAGE 4: Architecture

**Question**: How will you build it? What are the technical, design, security, and operational foundations?

**Estimated Duration**: 2-3 weeks

**Skills (In Order)**:
1. **tech-stack-advisor** — Define technology stack, infrastructure, platform choices
2. **design-consultation** (existing) — Visual design, UX, product design decisions
3. **plan-eng-review** (existing) — Engineering feasibility review
4. **plan-design-review** (existing) — Design quality and UX review
5. **plan-security-review** (existing) — Security architecture and data protection review
6. **plan-legal-review** (existing) — Legal and compliance architecture
7. **plan-ops-review** (existing) — Operational and deployment architecture

**Artifacts**:
- TECH-STACK.md (language, framework, database, infrastructure choices and rationale)
- ARCHITECTURE.md (system design, components, data flow)
- DESIGN-SYSTEM.md (visual design, component library, design standards)
- SECURITY-PLAN.md (data protection, encryption, compliance requirements)
- LEGAL-STRUCTURE.md (entity type, IP ownership, regulatory requirements)
- OPS-PLAN.md (deployment strategy, monitoring, scaling plan)
- DEPLOYMENT-ROADMAP.md (timeline for infrastructure setup)

**Quality Gate**: Gate Evaluator (Stage 4)
- Evaluates: Technical soundness, design maturity, security awareness, operational readiness
- Pass Criteria: Architecture is sound, no major security gaps, design is cohesive, ops plan is realistic
- Fail Outcomes: Redesign architecture, defer non-critical features, or kill

**Gate Scoring**:
- Technical Soundness: 1-5
- Design Maturity: 1-5
- Security Awareness: 1-5
- Operational Readiness: 1-5
- Overall: Pass/Fail/Retry

**Next Routing**:
- **Pass**: Proceed to Stage 5: business-formation
- **Retry**: Redesign architecture or defer non-MVP features
- **Kill**: Technical or security risk is too high to proceed

---

### STAGE 5: Operations

**Question**: Can you actually run this business? Legal, financial, and founder wellness.

**Estimated Duration**: 2-4 weeks

**Skills (In Order)**:
1. **business-formation** — Legal entity setup, IP registration, contracts, founder agreements
2. **runway-calculator** — Financial modeling, burn rate, runway analysis, fundraising strategy
3. **founder-wellness** — Founder health check, support structure, sustainability plan
4. **plan-support-review** (existing) — Support infrastructure, customer success planning

**Artifacts**:
- BUSINESS-FORMATION.md (entity type, location, IP assignment, founder agreements)
- RUNWAY-ANALYSIS.md (monthly burn rate, runway in months, cash needs)
- FINANCIAL-FORECAST.md (12-month P&L projection, break-even analysis)
- FUNDRAISE-STRATEGY.md (bootstrap vs. funding timeline, target raise amount)
- FOUNDER-HEALTH-CHECK.md (founder capacity, support needs, wellness plan)
- SUPPORT-STRUCTURE.md (advisors, mentors, peer support, therapy/wellness resources)

**Quality Gate**: Gate Evaluator (Stage 5)
- Evaluates: Legal readiness, financial reality, founder sustainability
- Pass Criteria: Legal structure in place, runway understood, founder has support and can sustain effort
- Fail Outcomes: Adjust financial model, reduce costs, bring in co-founder, or kill

**Gate Scoring**:
- Legal Readiness: 1-5
- Financial Realism: 1-5
- Founder Capacity: 1-5
- Support Structure: 1-5
- Overall: Pass/Fail/Retry

**Next Routing**:
- **Pass**: Proceed to Stage 6: sprint-planner
- **Retry**: Restructure finances, bring in co-founder, or reduce scope
- **Kill**: Runway is too short, founder is not sustainable

---

### STAGE 6: Build

**Question**: Can you execute? Does the team move fast and with quality?

**Estimated Duration**: 8-16 weeks (one MVP sprint cycle)

**Skills (In Order)**:
1. **sprint-planner** — Break MVP into sprints, prioritize, estimate, commit
2. **daily-standup** — Daily standups, progress tracking, blocker removal
3. **careful/guard/investigate** (existing) — Code review, quality assurance, risk management
4. **review/codex** (existing) — Code review, documentation, architectural alignment
5. **sprint-retro** — Sprint retrospective, learnings, process improvement

**Artifacts**:
- SPRINT-PLANS.md (sprints 1-N, stories, estimates, capacity)
- DAILY-LOGS.md (daily standup notes, progress, blockers)
- BUILD-PROGRESS.md (feature completion %, technical debt, risks)
- CODE-QUALITY.md (test coverage, code review notes, quality metrics)
- SPRINT-RETROS.md (learnings from each sprint, process improvements)

**Quality Gate**: Gate Evaluator (Stage 6)
- Evaluates: MVP completion, code quality, team velocity, technical decision quality
- Pass Criteria: MVP is feature-complete and tested, team velocity is predictable, code is maintainable
- Fail Outcomes: Extend timeline, reduce features, improve process, or kill

**Gate Scoring**:
- Feature Completion: 1-5
- Code Quality: 1-5
- Team Velocity: 1-5
- Technical Debt Management: 1-5
- Overall: Pass/Fail/Retry

**Next Routing**:
- **Pass**: Proceed to Stage 7: qa
- **Retry**: Continue building, fix quality issues, or reduce scope
- **Kill**: MVP can't reach shippable quality

---

### STAGE 7: Quality

**Question**: Does it work? Is it usable? Can it survive real users?

**Estimated Duration**: 2-4 weeks

**Skills (In Order)**:
1. **qa** (existing) — QA testing, bug reports, test plan execution
2. **design-review** (existing) — Design quality review, visual polish
3. **ux-walkthrough** — User experience testing, usability feedback, flow validation
4. **performance-audit** — Performance testing, load testing, optimization
5. **plan-security-review** (existing, round 2) — Security testing, penetration review, final security audit

**Artifacts**:
- QA-RESULTS.md (test results, critical bugs, known issues, fixes)
- DESIGN-REVIEW.md (visual polish feedback, consistency review)
- UX-FEEDBACK.md (user testing notes, usability issues, fixes)
- PERFORMANCE-REPORT.md (load testing results, optimization opportunities)
- SECURITY-AUDIT.md (penetration test results, vulnerabilities, remediation plan)
- LAUNCH-READY-CHECKLIST.md (all systems verified, no blockers)

**Quality Gate**: Gate Evaluator (Stage 7)
- Evaluates: Product quality, usability, performance, security maturity
- Pass Criteria: No critical bugs, usable by target customer, performs under expected load, no security gaps
- Fail Outcomes: Fix bugs, improve UX, optimize performance, or delay launch

**Gate Scoring**:
- Critical Bugs Fixed: 1-5
- Usability Validated: 1-5
- Performance Acceptable: 1-5
- Security Verified: 1-5
- Overall: Pass/Fail/Retry

**Next Routing**:
- **Pass**: Proceed to Stage 8: launch-checklist
- **Retry**: Fix bugs, improve quality, retest
- **Kill**: Quality gaps are too fundamental to fix before launch

---

### STAGE 8: Launch

**Question**: Ship it. Make it real.

**Estimated Duration**: 1-2 weeks

**Skills (In Order)**:
1. **launch-checklist** — Final launch prep, go/no-go decision, launch day plan
2. **launch-content** — Marketing content, announcements, customer communication
3. **ship** (existing) — Deploy to production, monitor, incident response
4. **document-release** (existing) — Release notes, documentation, changelog

**Artifacts**:
- LAUNCH-CHECKLIST.md (all launch criteria verified, no blockers)
- LAUNCH-CONTENT.md (pitch, landing page copy, email announcements)
- GO-LIVE-PLAN.md (deployment timeline, rollback plan, incident response)
- RELEASE-NOTES.md (features, known issues, support contact)
- POST-LAUNCH-PLAN.md (customer support plan, monitoring, early customer outreach)

**Quality Gate**: Gate Evaluator (Stage 8)
- Evaluates: Launch readiness, content quality, go/no-go decision
- Pass Criteria: All systems ready, content is compelling, team is prepared
- Fail Outcomes: Delay launch, fix issues, or pivot

**Gate Scoring**:
- Launch Readiness: 1-5
- Content Quality: 1-5
- Team Preparedness: 1-5
- Customer Onboarding: 1-5
- Overall: Pass/Fail/Retry

**Next Routing**:
- **Pass**: Deploy to production, initiate Stage 9
- **Retry**: Fix launch blockers, improve content
- **Kill**: Idea is no longer viable or team can't execute launch

---

### STAGE 9: Measure

**Question**: What did we learn? Who's using it? What's the retention, growth, and actual demand?

**Estimated Duration**: 4-8 weeks (post-launch observation period)

**Skills (In Order)**:
1. **metrics-review** — Set up analytics, track key metrics, measure progress
2. **retro** (existing) — Post-launch retrospective, what worked, what didn't
3. **customer-feedback** — Gather customer feedback, interviews, support tickets
4. **plan-support-review** (existing) — Support infrastructure review, customer success

**Artifacts**:
- METRICS-DASHBOARD.md (daily active users, retention, growth, revenue metrics)
- RETENTION-ANALYSIS.md (day-1, day-7, day-30 retention, churn analysis)
- CUSTOMER-INTERVIEWS-2.md (post-launch customer feedback, learnings)
- LEARNINGS.md (what we got right, what we got wrong, pivots needed)
- NEXT-ITERATION-PLAN.md (features to add, bugs to fix, pivots to consider)

**Quality Gate**: Gate Evaluator (Stage 9)
- Evaluates: Market traction, product-market fit signals, customer satisfaction
- Pass Criteria: Positive user retention, clear product-market fit signals, sustainable path to scale
- Fail Outcomes: Pivot product, pivot customer segment, extend runway and try again, or sunset

**Gate Scoring**:
- User Adoption: 1-5
- Retention Metrics: 1-5
- Customer Satisfaction: 1-5
- Market Feedback: 1-5
- Overall: Pass/Fail/Retry

**Next Routing**:
- **Pass**: Proceed to Stage 10: growth-playbook
- **Retry**: Iterate on product, optimize metrics, try again
- **Sunset**: Idea has not achieved product-market fit, close the company

---

### STAGE 10: Scale

**Question**: You've proven the model. Now grow it.

**Estimated Duration**: Ongoing (6+ months)

**Skills (In Order)**:
1. **growth-playbook** — Document repeatable growth channels, playbook, metrics
2. **fundraise-prep** — Pitch deck, financial model, investor outreach, due diligence prep
3. **hiring-plan** — Build the team, hiring plan, culture, roles
4. **plan-ceo-review** (existing, EXPANSION mode) — CEO review focused on scaling strategy
5. **plan-cfo-review** (existing, round 2) — Financial review for scaled operation

**Artifacts**:
- GROWTH-STRATEGY.md (repeatable growth channels, CAC, LTV, payback period)
- FUNDRAISE-DECK.md (pitch deck, financial model, investor information)
- HIRING-PLAN.md (organizational structure, roles, compensation plan)
- FINANCIAL-FORECAST.md (3-5 year P&L, revenue projections, funding needs)
- TEAM-CULTURE.md (company values, culture, working principles)
- QUARTERLY-PLAN.md (OKRs, growth targets, resource allocation)

**Quality Gate**: Continuous evaluation cycle
- No hard gate at Stage 10
- Continuous evaluation of traction, retention, growth, and fundraising success
- Decision points: Fundraise vs. bootstrap, accelerate vs. maintain, pivot growth channels

**Gate Scoring** (Continuous):
- Revenue Growth: 1-5
- Unit Economics: 1-5
- Team Quality: 1-5
- Fundraising Success (if applicable): 1-5

**Next Routing**:
- **Success Path**: Achieve growth targets, fundraise, scale
- **Pivot Path**: Growth stalling, try new channels, pivot business model
- **Maintenance Path**: Sustainable but slow growth, profitability focus
- **Exit Path**: Acquire, merge, or strategic partnership

---

## Routing Logic

### First-Time Entry

```
USER INITIATES: "start the bootcamp"
    ↓
CHECK: Does FOUNDER-PROFILE.md exist?
    ├─ NO → Route to: founder-onboarding
    │        (Create profile, then move to Stage 1)
    └─ YES → Is profile complete?
             ├─ NO → Route to: founder-onboarding (completion)
             └─ YES → Route to: Stage 1 (idea-intake)
```

### Returning User

```
USER INITIATES: Any trigger ("status", "next", "where am i", etc.)
    ↓
READ: PIPELINE-STATE.md
    ↓
DETERMINE: Current stage and position
    ↓
ROUTE: To next skill in current stage
    OR show status if user asked for it
```

### Gate Evaluation

```
USER INITIATES: "evaluate" or "gate check"
    ↓
RUN: Gate Evaluator for current stage
    ↓
DECISION:
    ├─ PASS → Advance to next stage
    ├─ RETRY → Repeat current stage or pivot
    └─ KILL → Sunset or major pivot
```

### Command-Based Navigation

```
"next" → Advance to next skill in current stage
"status" → Show current stage, artifacts, gate scores
"go back" → Return to previous stage (with reflection)
"restart stage" → Restart current stage from beginning
"kill check" → Honest assessment: continue, pivot, or kill
"show me the map" → Display this pipeline map
```

---

## Artifact Taxonomy

All artifacts follow consistent naming and structure:

### Stage 1 Artifacts
- `IDEA-STATEMENT.md` — Problem, solution, hypothesis
- `MARKET-ANALYSIS.md` — Market size, growth, TAM
- `COMPETITIVE-LANDSCAPE.md` — Competitors, differentiation

### Stage 2 Artifacts
- `CUSTOMER-INTERVIEWS.md` — Raw interview notes
- `DEMAND-EVIDENCE.md` — Analysis of willingness to pay
- `PRICING-STRATEGY.md` — Pricing hypothesis

### Stage 3 Artifacts
- `LEAN-CANVAS.md` — Business model
- `MVP-SPEC.md` — Feature list, acceptance criteria
- `SCOPE-CONSTRAINTS.md` — Out of scope, rationale

### Stage 4 Artifacts
- `TECH-STACK.md` — Technology choices
- `ARCHITECTURE.md` — System design
- `SECURITY-PLAN.md` — Data protection, compliance

### Stage 5 Artifacts
- `BUSINESS-FORMATION.md` — Legal entity, IP
- `RUNWAY-ANALYSIS.md` — Financial projections
- `FOUNDER-HEALTH-CHECK.md` — Wellness assessment

### Stage 6 Artifacts
- `SPRINT-PLANS.md` — Sprint breakdown
- `BUILD-PROGRESS.md` — Completion status
- `CODE-QUALITY.md` — Quality metrics

### Stage 7 Artifacts
- `QA-RESULTS.md` — Test results, bugs
- `UX-FEEDBACK.md` — Usability findings
- `PERFORMANCE-REPORT.md` — Performance metrics

### Stage 8 Artifacts
- `LAUNCH-CHECKLIST.md` — Go/no-go criteria
- `LAUNCH-CONTENT.md` — Marketing content
- `GO-LIVE-PLAN.md` — Deployment plan

### Stage 9 Artifacts
- `METRICS-DASHBOARD.md` — Key metrics
- `RETENTION-ANALYSIS.md` — User retention
- `LEARNINGS.md` — Post-launch insights

### Stage 10 Artifacts
- `GROWTH-STRATEGY.md` — Growth playbook
- `FUNDRAISE-DECK.md` — Investor pitch
- `HIRING-PLAN.md` — Team building

---

## Gate Scoring System

Every gate uses a consistent 1-5 scoring framework:

**5: Excellent** — This is exceeds expectations, no concerns, ready to move forward

**4: Strong** — This is solid work, minor gaps that won't block progress

**3: Acceptable** — This meets minimum standards, some gaps but manageable

**2: Weak** — This has significant gaps, needs iteration before proceeding

**1: Critical** — This is fundamentally flawed, blocks progress, needs major rework

**Overall Decision**:
- **Average 4+**: PASS — Move to next stage
- **Average 3-3.9**: RETRY — Iterate and resubmit for same stage
- **Average < 3**: KILL or PIVOT — Idea or approach needs fundamental change

---

## Pipeline State File (PIPELINE-STATE.md)

The orchestrator maintains a PIPELINE-STATE.md file:

```yaml
---
pipeline_version: "1.0"
startup_name: "Company Name"
founder: "Founder Name"
current_stage: 1-10
current_skill: "skill-name"
overall_health: "green | yellow | red"

founder_profile_complete: true/false

stages_completed: [1, 2, 3]  # Which stages have passed gates
current_stage_attempts: 1-N
current_stage_started: "YYYY-MM-DD"

gate_history:
  - stage: 1
    date: "YYYY-MM-DD"
    result: "PASS | RETRY | KILL"
    scores:
      criterion_1: 4
      criterion_2: 3
      overall: 3.5
    notes: "..."
  # ... more gates

artifacts:
  stage_1:
    - IDEA-STATEMENT.md: exists/missing
    - MARKET-ANALYSIS.md: exists/missing
  # ... all artifacts tracked

active_warnings:
  - "Type: KILL | PIVOT"
    message: "..."
    since: "YYYY-MM-DD"

next_skill: "skill-name"
last_updated: "YYYY-MM-DD HH:MM"
---
```

---

## Founder Profile File (FOUNDER-PROFILE.md)

The onboarding skill creates FOUNDER-PROFILE.md:

```yaml
---
name: "Founder Name"
background: "..."
experience_level: "first-time | serial | experienced"
technical_background: "high | medium | low"
business_background: "high | medium | low"

known_strengths:
  - "..."

known_weaknesses:
  - "..."

risk_tolerance: "conservative | moderate | aggressive"
ambition_level: "lifestyle | growth | scale"

time_commitment: "full-time | part-time | hours_per_week"
available_capital: "bootstrap | angel | pre-seed | larger"

support_structure:
  co_founder: true/false
  team: "..."
  advisors: "..."

blind_spots_identified: ["..."]
---
```

---

## Bootstrap Process

When first launched, the orchestrator:

1. **Checks** for FOUNDER-PROFILE.md in the project directory
2. **If missing**: Sends founder to founder-onboarding
3. **If exists**: Reads PIPELINE-STATE.md
4. **If PIPELINE-STATE.md missing**: Creates it with current_stage: 1
5. **Routes** to appropriate skill based on state

---

## Tone & Challenge Model

The orchestrator adjusts its challenge level based on founder profile:

**Technical Founder** → Pushes harder on:
- Market validation
- Customer discovery
- Business model clarity
- Sales and marketing reality

**Business Founder** → Pushes harder on:
- Technical feasibility
- Engineering reality
- Product quality
- Execution risk

**No Experience** → Emphasizes:
- Structured thinking
- Systematic validation
- Pace and incremental progress
- Support and mentorship

**Serial Entrepreneur** → Expects:
- Fast thinking and iteration
- Bold assumptions
- Pattern recognition
- Healthy skepticism

---

## Success Metrics for the Pipeline

The bootcamp succeeds when:

1. **Ideas are validated or killed early** — Before wasting time on non-viable ideas
2. **Founders think rigorously** — About customers, market, product, execution
3. **Teams are aligned** — Everyone understands the MVP and why
4. **Execution is fast** — From idea to MVP in < 6 months
5. **Product-market fit is clear** — Before scaling

The bootcamp fails when:

1. **Ideas proceed without validation** — Founders skip customer discovery
2. **Scope creep prevents shipping** — MVP becomes a full product
3. **Founders aren't challenged** — They avoid hard questions
4. **Teams burn out** — Unsustainable pace or lack of support
5. **Success is undefined** — No clear metrics for moving to next stage

---

## Reference: All Skills

### Orchestration
- **z-combinator** (this skill) — Master orchestrator

### Onboarding
- **founder-onboarding** — Set up founder profile

### Stage 1
- **idea-intake** — Define problem and solution
- **office-hours** (existing) — Expert feedback
- **market-research** — Validate market opportunity
- **plan-shark-tank** (existing) — Pitch preparation

### Stage 2
- **customer-discovery** — Find and talk to customers
- **evidence-review** — Analyze customer feedback
- **plan-shark-tank** (existing, round 2) — Updated pitch

### Stage 3
- **lean-canvas** — Business model definition
- **mvp-scoper** — Define MVP scope
- **plan-ceo-review** (existing) — CEO challenge
- **plan-cfo-review** (existing) — Financial review
- **plan-sales-review** (existing) — Sales/GTM review

### Stage 4
- **tech-stack-advisor** — Technology choices
- **design-consultation** (existing) — Design review
- **plan-eng-review** (existing) — Engineering review
- **plan-design-review** (existing) — Design quality
- **plan-security-review** (existing) — Security review
- **plan-legal-review** (existing) — Legal review
- **plan-ops-review** (existing) — Operations review

### Stage 5
- **business-formation** — Legal setup
- **runway-calculator** — Financial modeling
- **founder-wellness** — Founder health check
- **plan-support-review** (existing) — Support infrastructure

### Stage 6
- **sprint-planner** — Sprint planning
- **daily-standup** — Daily progress tracking
- **careful/guard/investigate** (existing) — Code review
- **review/codex** (existing) — Code quality
- **sprint-retro** — Retrospective

### Stage 7
- **qa** (existing) — Quality assurance
- **design-review** (existing) — Design quality
- **ux-walkthrough** — User experience testing
- **performance-audit** — Performance testing
- **plan-security-review** (existing, round 2) — Security audit

### Stage 8
- **launch-checklist** — Launch preparation
- **launch-content** — Marketing content
- **ship** (existing) — Deployment
- **document-release** (existing) — Documentation

### Stage 9
- **metrics-review** — Analytics and metrics
- **retro** (existing) — Post-launch retrospective
- **customer-feedback** — Customer research
- **plan-support-review** (existing) — Support review

### Stage 10
- **growth-playbook** — Growth strategy
- **fundraise-prep** — Investor pitch
- **hiring-plan** — Team building
- **plan-ceo-review** (existing, expansion mode) — Scaling review
- **plan-cfo-review** (existing, round 2) — Financial scaling

### Gates
- **gate-evaluator** — Quality gate runner (all stages)

---

*Last updated: 2026-03-24*
