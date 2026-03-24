---
name: launch-checklist
description: Comprehensive pre-launch verification across infrastructure, analytics, legal, SEO, email, payment, support. Every item GREEN/YELLOW/RED. All reds must resolve before launch. Use 2 weeks before target launch.
---

# Launch Checklist

Two weeks before launch, work through this systematically. Every RED item blocks launch.

## What You Do

1. Go through each category below
2. For each item, determine: GREEN (done), YELLOW (in progress), RED (not done)
3. RED items require immediate action with clear deadline
4. All items must be GREEN before launch day
5. Document evidence (URLs, configs, screenshots) for each

## Infrastructure

| Item | Status | Evidence | Due Date |
|------|--------|----------|----------|
| DNS configured and propagated | G/Y/R | [URL] | |
| SSL certificate valid (HTTPS everywhere) | G/Y/R | [Certificate info] | |
| CDN configured for static assets | G/Y/R | [CDN provider + config] | |
| Error tracking (Sentry/Rollbar) live | G/Y/R | [Dashboard link] | |
| Uptime monitoring alerts configured | G/Y/R | [Monitoring provider + alert details] | |
| Database backups automated and tested | G/Y/R | [Backup provider + test date] | |
| Staging environment mirrors production | G/Y/R | [Staging URL] | |
| Database migrations tested on staging | G/Y/R | [Test results] | |
| Rollback plan documented | G/Y/R | [Rollback steps] | |

## Analytics & Tracking

| Item | Status | Evidence | Due Date |
|------|--------|----------|----------|
| Event tracking configured (Amplitude/Mixpanel/GA4) | G/Y/R | [Event list] | |
| Critical funnel events defined | G/Y/R | [Funnel: landing → signup → first value] | |
| Analytics dashboards created | G/Y/R | [Dashboard URLs] | |
| Goal/conversion tracking set up | G/Y/R | [Tracked conversions] | |
| UTM parameters documented | G/Y/R | [UTM naming convention] | |

## Legal & Compliance

| Item | Status | Evidence | Due Date |
|------|--------|----------|----------|
| Privacy policy published | G/Y/R | [Live URL] | |
| Terms of Service published | G/Y/R | [Live URL] | |
| Cookie consent banner live | G/Y/R | [Banner visible on site] | |
| GDPR compliance reviewed (if EU users) | G/Y/R | [Compliance checklist] | |
| DMCA takedown process documented | G/Y/R | [Process + contact info] | |

## SEO Basics

| Item | Status | Evidence | Due Date |
|------|--------|----------|----------|
| Page titles optimized (compelling, keyword-rich) | G/Y/R | [Sample titles] | |
| Meta descriptions present on key pages | G/Y/R | [Sample meta descriptions] | |
| OG images present (for social sharing) | G/Y/R | [OG image URLs] | |
| XML sitemap generated and submitted | G/Y/R | [Sitemap URL] | |
| Robots.txt configured | G/Y/R | [Robots.txt content] | |
| Canonical tags present where needed | G/Y/R | [Sample pages checked] | |
| Mobile responsiveness verified | G/Y/R | [Mobile test results] | |

## Email

| Item | Status | Evidence | Due Date |
|------|--------|----------|----------|
| Transactional email templates created | G/Y/R | [Template list] | |
| Signup confirmation email working | G/Y/R | [Test email received] | |
| Password reset email working | G/Y/R | [Test email received] | |
| Payment receipt email working | G/Y/R | [Test email received] | |
| Email service provider configured (SendGrid/Mailgun) | G/Y/R | [Provider + API keys] | |
| Unsubscribe link present in all marketing emails | G/Y/R | [Email sample] | |

## Payment (if applicable)

| Item | Status | Evidence | Due Date |
|------|--------|----------|----------|
| Payment processor integrated (Stripe/PayPal) | G/Y/R | [Processor dashboard] | |
| Test transactions working | G/Y/R | [Test charge receipt] | |
| Refund flow tested | G/Y/R | [Refund test complete] | |
| Receipt generation working | G/Y/R | [Sample receipt] | |
| PCI DSS compliance verified | G/Y/R | [Compliance status] | |
| Billing email sent on purchase | G/Y/R | [Test email received] | |
| Subscription renewal logic tested | G/Y/R | [Test results] (if applicable) | |

## Support & Documentation

| Item | Status | Evidence | Due Date |
|------|--------|----------|----------|
| Contact page live with response time commitment | G/Y/R | [Contact URL + commitment] | |
| FAQ or help docs created | G/Y/R | [FAQ URL] | |
| Support email account monitoring | G/Y/R | [Assigned person + hours] | |
| Status page created | G/Y/R | [Status page URL] | |
| Incident response plan documented | G/Y/R | [Incident playbook] | |

## Product Readiness

| Item | Status | Evidence | Due Date |
|------|--------|----------|----------|
| All MVP features working | G/Y/R | [Feature checklist] | |
| Critical bugs fixed | G/Y/R | [Bug list cleared] | |
| Performance audit passed | G/Y/R | [Performance report] | |
| UX walkthrough passed | G/Y/R | [UX audit] | |
| Staging environment user testing complete | G/Y/R | [User test results] | |

## Communications Ready

| Item | Status | Evidence | Due Date |
|------|--------|----------|----------|
| Launch announcement drafted | G/Y/R | [Announcement draft] | |
| Social media copy ready | G/Y/R | [Copy + scheduling platform] | |
| Press contacts identified | G/Y/R | [Contact list] | |
| Early user notification list prepared | G/Y/R | [Email list count] | |

## Output: LAUNCH-CHECKLIST.md

Create a document with:
- All items from above with current status
- RED items with action owner and deadline
- Sign-off by founder: "I have personally verified every RED item is cleared and we're shipping."

```
# Launch Readiness Checklist

## Summary
- Total items: [X]
- GREEN: [X]
- YELLOW: [X]
- RED: [X]

**Status: READY_TO_LAUNCH / BLOCKED**

[Detailed table from above with current status]

## RED Items Requiring Action

| Item | Owner | Deadline | Status |
|------|-------|----------|--------|
| [Item] | [Person] | [Date] | [Action plan] |

## Founder Sign-off

I have personally verified every item above. All RED items will be cleared by [date].

Signature: _________________ Date: _______
```

RED items block launch. Period. No exceptions, no "we'll fix it after launch."
