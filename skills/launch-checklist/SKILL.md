---
name: launch-checklist
description: Comprehensive pre-launch verification across infrastructure, analytics, legal, SEO, email, payment, support. Every item GREEN/YELLOW/RED. All reds must resolve before launch. Use 2 weeks before target launch.
benefits-from: performance-audit, ux-walkthrough
feeds-into: launch-content
---

# Launch Checklist

Systematic pre-launch verification. Two weeks before target launch, every item must be GREEN. RED items block launch. No exceptions.

---

## Phase 0: Scope & Planning

**Purpose:** Define launch scope and timeline.

1. Confirm launch date (target go-live date)
2. Confirm which checklist items apply:
   - Is this a paid product? (affects Payment section)
   - Do you have EU users? (affects GDPR section)
   - Is this a public-facing product? (affects all sections)
3. Identify owners for each category

**Exit Criteria:** Launch date confirmed, scope defined, owners assigned.

**AI Instructions:**
Do not ask any questions. Load context silently. Proceed to Phase 1.

---

## Phase 1: Infrastructure (AskUserQuestion)

**Purpose:** Verify ops readiness.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Launch target: [DATE]. Infrastructure readiness: we need DNS, SSL, CDN, monitoring, backups, and rollback plan."

**Simplify:** "Can your users reach your site? Is it secure? If something breaks, can you fix it? Will you know if it breaks?"

**Recommend:** "RECOMMENDATION: Use a checklist as you go. Mark GREEN (done), YELLOW (in progress), RED (not done). RED items block launch."

**Options:**
- A) Go through each infrastructure item and report status (with evidence)
- B) Quick summary: "DNS: GREEN, SSL: GREEN, error tracking: YELLOW, backups: RED"
- C) Just the RED items (skip GREEN/YELLOW for speed)

**AI then checks:**
For each item, status:

| Item | Status | Evidence |
|------|--------|----------|
| DNS configured and propagated | GREEN/YELLOW/RED | [URL / DNS provider] |
| SSL certificate valid (HTTPS everywhere) | G/Y/R | [Certificate info] |
| CDN configured for static assets | G/Y/R | [CDN provider + config] |
| Error tracking (Sentry/Rollbar) live | G/Y/R | [Dashboard link] |
| Uptime monitoring alerts configured | G/Y/R | [Monitoring provider + alert details] |
| Database backups automated and tested | G/Y/R | [Backup provider + test date] |
| Staging environment mirrors production | G/Y/R | [Staging URL] |
| Database migrations tested on staging | G/Y/R | [Test results] |
| Rollback plan documented | G/Y/R | [Rollback steps] |

If any RED, use **AskUserQuestion**:

**Re-ground:** "Infrastructure has RED items: [list]."

**Simplify:** "These are critical. You can't launch without them. What's the blocker for each?"

**Recommend:** "RECOMMENDATION: Assign an owner and deadline for each RED item. Escalate if blocked."

**Options:**
- A) Assign owners and deadlines to each RED item
- B) Defer some items to post-launch (risky but possible for some)
- C) Escalate (something is blocked)

**Exit Criteria:** All items assessed, RED items have owners and deadlines. Proceed to Phase 2.

---

## Phase 2: Analytics & Tracking (AskUserQuestion)

**Purpose:** Verify measurement infrastructure.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Analytics: you need to track user behavior so you know if launch works."

**Simplify:** "Can you see who's signing up? Which features they use? Where they drop off? This data drives decisions after launch."

**Recommend:** "RECOMMENDATION: Even a basic setup (GA4 + funnel events) is better than nothing. Don't over-engineer — start simple."

**Options:**
- A) Go through each analytics item and report status
- B) Quick summary: "GA4: GREEN, events: YELLOW, dashboards: RED"
- C) Just the RED items

**AI then checks:**

| Item | Status | Evidence |
|------|--------|----------|
| Event tracking configured (Amplitude/Mixpanel/GA4) | G/Y/R | [Event list] |
| Critical funnel events defined | G/Y/R | [Funnel: landing → signup → first value] |
| Analytics dashboards created | G/Y/R | [Dashboard URLs] |
| Goal/conversion tracking set up | G/Y/R | [Tracked conversions] |
| UTM parameters documented | G/Y/R | [UTM naming convention] |

If RED, ask for owners and deadlines (same pattern as Phase 1).

**Exit Criteria:** Analytics assessed, RED items owned. Proceed to Phase 3.

---

## Phase 3: Legal & Compliance (AskUserQuestion)

**Purpose:** Verify legal readiness.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Legal: privacy policy, terms, cookie consent. These aren't optional."

**Simplify:** "You collect user data (emails, IPs, behavior). You must tell users how you use it and give them control. Legal liability is real."

**Recommend:** "RECOMMENDATION: Don't overthink this. Use templates (e.g., Termly, iubenda) as a starting point. Have a lawyer review if you can."

**Options:**
- A) Go through each legal item and report status
- B) Quick summary: "Privacy: RED, Terms: YELLOW, GDPR: GREEN"
- C) Just the RED items

**AI then checks:**

| Item | Status | Evidence |
|------|--------|----------|
| Privacy policy published | G/Y/R | [Live URL] |
| Terms of Service published | G/Y/R | [Live URL] |
| Cookie consent banner live | G/Y/R | [Banner visible on site] |
| GDPR compliance reviewed (if EU users) | G/Y/R | [Compliance checklist] |
| DMCA takedown process documented | G/Y/R | [Process + contact info] |

If RED, ask for owners and deadlines.

**Exit Criteria:** Legal assessed, RED items owned. Proceed to Phase 4.

---

## Phase 4: SEO Basics (Automated, No Question)

**Purpose:** Optimize for search and social sharing.

**AI Instructions:**
No question needed. Check:

| Item | Status | Evidence |
|------|--------|----------|
| Page titles optimized (compelling, keyword-rich) | G/Y/R | [Sample titles] |
| Meta descriptions present on key pages | G/Y/R | [Sample meta descriptions] |
| OG images present (for social sharing) | G/Y/R | [OG image URLs] |
| XML sitemap generated and submitted | G/Y/R | [Sitemap URL] |
| Robots.txt configured | G/Y/R | [Robots.txt content] |
| Canonical tags present where needed | G/Y/R | [Sample pages checked] |
| Mobile responsiveness verified | G/Y/R | [Mobile test results] |

If RED items, use **AskUserQuestion**:

**Re-ground:** "SEO: [list RED items]. These affect discoverability and social sharing."

**Simplify:** "Good page titles and meta descriptions help people find you on Google. OG images help on social media."

**Recommend:** "RECOMMENDATION: Titles and descriptions are quick wins. Do these first. XML sitemap submission is easy and valuable."

**Options:**
- A) List quick SEO wins (titles, descriptions, OG images)
- B) Defer SEO to post-launch (okay but suboptimal)
- C) Accept current state

Proceed to Phase 5.

---

## Phase 5: Email (AskUserQuestion)

**Purpose:** Verify transactional email setup.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Email: signup confirmations, password resets, payment receipts. These are critical workflows."

**Simplify:** "When users sign up or buy something, they need to hear from you. Email provider (SendGrid, Mailgun) + templates."

**Recommend:** "RECOMMENDATION: Test every email flow before launch. Nothing worse than users signing up and not getting confirmation."

**Options:**
- A) Go through each email item and report status
- B) Quick summary: "Emails: YELLOW (templates done, not tested)"
- C) Just the RED items

**AI then checks:**

| Item | Status | Evidence |
|------|--------|----------|
| Transactional email templates created | G/Y/R | [Template list] |
| Signup confirmation email working | G/Y/R | [Test email received] |
| Password reset email working | G/Y/R | [Test email received] |
| Payment receipt email working | G/Y/R | [Test email received] (if applicable) |
| Email service provider configured | G/Y/R | [Provider + API keys] |
| Unsubscribe link in marketing emails | G/Y/R | [Email sample] |

If RED, ask for owners and deadlines.

**Exit Criteria:** Email assessed, RED items owned. Proceed to Phase 6.

---

## Phase 6: Payment (If Applicable, AskUserQuestion)

**Purpose:** Verify payment processing readiness.

Only run if product is paid. Ask upfront:

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Payment: is this a paid product?"

**Simplify:** "If you're charging users, this section applies. If free, skip it."

**Recommend:** "RECOMMENDATION: If paid, payment is critical. Don't cut corners here."

**Options:**
- A) Yes, paid product (proceed with payment checklist)
- B) No, free product (skip this phase)
- C) Freemium (some features paid)

If paid, check:

| Item | Status | Evidence |
|------|--------|----------|
| Payment processor integrated (Stripe/PayPal) | G/Y/R | [Processor dashboard] |
| Test transactions working | G/Y/R | [Test charge receipt] |
| Refund flow tested | G/Y/R | [Refund test complete] |
| Receipt generation working | G/Y/R | [Sample receipt] |
| PCI DSS compliance verified | G/Y/R | [Compliance status] |
| Billing email sent on purchase | G/Y/R | [Test email received] |
| Subscription renewal logic tested | G/Y/R | [Test results] (if applicable) |

If RED, ask for owners and deadlines.

**Exit Criteria:** Payment assessed (or skipped), RED items owned. Proceed to Phase 7.

---

## Phase 7: Support & Documentation (AskUserQuestion)

**Purpose:** Verify support readiness.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Support: users will have questions. How will you answer them?"

**Simplify:** "Contact page, FAQ, help docs. And someone needs to monitor support email on day 1."

**Recommend:** "RECOMMENDATION: Assign a person to monitor support during launch week. Don't let user questions go unanswered."

**Options:**
- A) Go through each support item and report status
- B) Quick summary: "Contact: GREEN, FAQ: YELLOW, support assignment: RED"
- C) Just the RED items

**AI then checks:**

| Item | Status | Evidence |
|------|--------|----------|
| Contact page live with response time commitment | G/Y/R | [Contact URL + commitment] |
| FAQ or help docs created | G/Y/R | [FAQ URL] |
| Support email account monitoring | G/Y/R | [Assigned person + hours] |
| Status page created | G/Y/R | [Status page URL] |
| Incident response plan documented | G/Y/R | [Incident playbook] |

If RED, ask for owners and deadlines.

**Exit Criteria:** Support assessed, RED items owned. Proceed to Phase 8.

---

## Phase 8: Product Readiness (Automated, No Question)

**Purpose:** Verify product quality.

**AI Instructions:**
Reference results from prior skills: performance-audit, ux-walkthrough.

| Item | Status | Evidence |
|------|--------|----------|
| All MVP features working | G/Y/R | [Feature checklist] |
| Critical bugs fixed | G/Y/R | [Bug list cleared] |
| Performance audit passed | G/Y/R | [Performance report] |
| UX walkthrough passed | G/Y/R | [UX audit] |
| Staging environment user testing complete | G/Y/R | [User test results] |

If RED, use **AskUserQuestion**:

**Re-ground:** "Product readiness: [RED items]. These are showstoppers."

**Simplify:** "Broken features, slow performance, confusing UX. Users will leave."

**Recommend:** "RECOMMENDATION: You can't launch with RED product issues. Fix these first."

**Options:**
- A) Fix RED items before launch
- B) Defer low-priority RED items to post-launch (unlikely to be acceptable)

**Exit Criteria:** Product readiness assessed, RED items assigned. Proceed to Phase 9.

---

## Phase 9: Communications Ready (AskUserQuestion)

**Purpose:** Verify launch announcement readiness.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Communications: launch announcement, social media, press. How will people hear about you?"

**Simplify:** "You're launching. You need to tell people. Announcement, social posts, press outreach."

**Recommend:** "RECOMMENDATION: Prepare launch content 1 week before. You'll be busy on launch day."

**Options:**
- A) Go through each communications item and report status
- B) Quick summary: "Announcement: YELLOW, social: RED, press: GREEN"
- C) Just the RED items

**AI then checks:**

| Item | Status | Evidence |
|------|--------|----------|
| Launch announcement drafted | G/Y/R | [Announcement draft] |
| Social media copy ready | G/Y/R | [Copy + scheduling platform] |
| Press contacts identified | G/Y/R | [Contact list] |
| Early user notification list prepared | G/Y/R | [Email list count] |

If RED, ask for owners and deadlines.

**Exit Criteria:** Communications assessed, RED items owned. Proceed to Phase 10.

---

## Phase 10: Consolidation & Sign-off (AskUserQuestion)

**Purpose:** Final consolidation and founder sign-off.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "All sections assessed. Summary: [X GREEN], [X YELLOW], [X RED]."

**Simplify:** "RED items are blockers. Can you clear them all by launch day?"

**Recommend:** "RECOMMENDATION: Founder reviews RED items. If you think it's too risky, escalate now."

**Options:**
- A) Confirm all RED items will be cleared by [launch date] (proceed to Phase 11)
- B) Some RED items cannot be fixed in time — reassess launch date
- C) Cancel or postpone launch (escalation)

**Exit Criteria:** Founder confidence in launch readiness confirmed. Proceed to Phase 11.

---

## Phase 11: Output & Archive

**Purpose:** Create the launch checklist document.

**AI Instructions:**
Create LAUNCH-CHECKLIST.md with this format:

```markdown
# Launch Readiness Checklist

## Launch Target
**Date**: [Launch date]
**Environment**: [Staging / Production]

## Summary
- Total items: [X]
- GREEN: [X]
- YELLOW: [X]
- RED: [X]

**Status**: [READY_TO_LAUNCH / BLOCKED_ON_REDS]

---

## Infrastructure
| Item | Status | Owner | Deadline |
|------|--------|-------|----------|
| DNS configured | GREEN/YELLOW/RED | [Person] | [Date] |
| SSL certificate | G/Y/R | [Person] | [Date] |
| [etc.] | | | |

---

## Analytics & Tracking
| Item | Status | Owner | Deadline |
|------|--------|-------|----------|
| Event tracking | G/Y/R | [Person] | [Date] |
| [etc.] | | | |

---

## Legal & Compliance
| Item | Status | Owner | Deadline |
|------|--------|-------|----------|
| Privacy policy | G/Y/R | [Person] | [Date] |
| [etc.] | | | |

---

## SEO Basics
| Item | Status | Owner | Deadline |
|------|--------|-------|----------|
| Page titles | G/Y/R | [Person] | [Date] |
| [etc.] | | | |

---

## Email
| Item | Status | Owner | Deadline |
|------|--------|-------|----------|
| Transactional templates | G/Y/R | [Person] | [Date] |
| [etc.] | | | |

---

## Payment
(Only if applicable)

| Item | Status | Owner | Deadline |
|------|--------|-------|----------|
| Stripe integration | G/Y/R | [Person] | [Date] |
| [etc.] | | | |

---

## Support & Documentation
| Item | Status | Owner | Deadline |
|------|--------|-------|----------|
| Contact page | G/Y/R | [Person] | [Date] |
| [etc.] | | | |

---

## Product Readiness
| Item | Status | Owner | Deadline |
|------|--------|-------|----------|
| MVP features | G/Y/R | [Person] | [Date] |
| [etc.] | | | |

---

## Communications Ready
| Item | Status | Owner | Deadline |
|------|--------|-------|----------|
| Announcement | G/Y/R | [Person] | [Date] |
| [etc.] | | | |

---

## RED Items Requiring Action

| Item | Owner | Deadline | Action Plan |
|------|-------|----------|-------------|
| [Item 1] | [Person] | [Date] | [What to do] |
| [Item 2] | [Person] | [Date] | [What to do] |

(If no RED items, write "No RED items — on track for launch.")

---

## Founder Sign-off

**I have personally verified every item above. All RED items will be cleared by [deadline].**

I understand that RED items block launch. I will not ship with outstanding RED items.

**Signature**: ________________________ **Date**: ____________

**Name**: _________________________

---

## Launch Day Checklist

- [ ] All RED items cleared and verified GREEN
- [ ] Staging environment final smoke test passed
- [ ] Support team standing by
- [ ] Monitoring alerts active
- [ ] Rollback plan reviewed and ready
- [ ] Announcement scheduled and ready
- [ ] Go / No-go decision: ________
```

**Tone Guidance:**
- RED items block launch. No exceptions, no "we'll fix it after launch."
- Founder must personally verify RED items are cleared.
- This is a forcing function for accountability.

---

## Escape Hatches

**If user is impatient ("just do it"):**
- Skip detailed section-by-section walkthrough.
- Ask Phase 10 directly: "RED items status? Can you clear them by launch?"
- Jump to sign-off.

**If launch is in < 1 week:**
- Assume most items are either GREEN or RED (no time for YELLOW).
- Focus only on RED items.
- Escalate if any RED items cannot be cleared.

**If using a commercial launch checklist tool:**
- Import those results here.
- Map tool statuses to GREEN/YELLOW/RED.

---

## When to Run

- **2 weeks before target launch** (gives time to fix RED items)
- **1 week before launch** (final verification)
- **Launch day morning** (final smoke test and go/no-go decision)

---

## Completion Status

At the end of the skill, report one of:
- **DONE**: Checklist complete, all items GREEN, founder sign-off obtained, ready for launch
- **DONE_WITH_CONCERNS**: Checklist complete, RED items have owners and deadlines, on track to clear
- **BLOCKED**: Launch blocked until RED items resolved (escalate to founder)
- **NEEDS_CONTEXT**: Unclear launch date or scope; ask user for confirmation
