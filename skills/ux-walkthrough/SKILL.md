---
name: ux-walkthrough
description: First-time user simulation through critical path. Evaluates time to first value, confusion points, onboarding, error handling, mobile experience, accessibility. "If your mom couldn't figure this out in 3 minutes, it's not ready." Use before launch readiness.
---

# UX Walkthrough

Simulate a first-time user. Your job is to be brutally honest about friction.

## What You Do

1. Read MVP-SPEC.md to identify the critical path (primary user journey)
2. Access the live product or staging environment
3. Start from cold: No prior knowledge, no hand-holding
4. Walk through the critical path from landing to first value
5. Document every decision point, every click, every moment of confusion
6. Measure: Time from landing to "I got value" — should be under 3 minutes for consumer apps
7. Test error states: What happens when something breaks? Is the message helpful or cryptic?
8. Test mobile: Responsive? Usable on a phone?
9. Test accessibility basics: Can a screen reader understand the page? Alt text on images?

## Evaluation Criteria

| Metric | Standard | Flag if |
|--------|----------|---------|
| Time to first value | <3 min | >5 min |
| Onboarding clicks | <5 | >8 |
| Confusion points | 0 | Any moment of "why am I here?" |
| Error clarity | Clear next step | Generic error message |
| Mobile responsiveness | Full feature parity | Broken layout or missing features |
| Accessibility | WCAG AA compliant | Missing alt text, unlabeled form fields |

## Output: UX-AUDIT.md

Format:
```
# UX Walkthrough Report

## Test Date
[Date and environment (staging/production)]

## Critical Path: [User story being tested]

## Timeline
- [Time point]: [Action taken] → [Observed outcome]
- [Time point]: [Action taken] → [Observed outcome]
...
- **Total time to first value**: [X minutes]

## Confusion Points Found

### [Issue title]
- **What happened**: [Describe user action and outcome]
- **Why it's a problem**: [Impact on user]
- **Severity**: RED / YELLOW / GREEN
- **Fix**: [Recommendation]

### [Issue title]
...

## Error State Testing

- Tested scenarios: [List of errors you triggered]
- Quality of error messages: [Good / Poor / Inconsistent]
- Example failure: [Describe a bad error message]

## Mobile Experience

- **Responsive**: [Yes/No]
- **Functional gaps**: [List missing features on mobile]
- **Touch targets**: [Buttons/links appropriately sized?]
- **Performance**: [Load time on 4G? Slow?]

## Accessibility Basics

- **Images**: [Alt text present/missing?]
- **Form labels**: [Associated with inputs?]
- **Color contrast**: [WCAG AA compliant?]
- **Keyboard navigation**: [Can you tab through the app?]
- **Screen reader**: [Can it read the content?]

## Overall Assessment

**If your mom couldn't figure this out in 3 minutes, mark it RED.**

- Landing → signup/login: [Time + friction]
- First feature access: [Time + clarity]
- Core value delivery: [Time + obviousness]

## Recommended Fixes (Priority Order)

1. [Critical issue fix]
2. [Important issue fix]
3. [Polish issue fix]

## Sign-off

- **Ready for launch?**: YES / NO / CONDITIONAL
- **Top blocker**: [What must change before shipping?]
```

Use screenshots if you can capture them. Be specific about clickpaths and timing. "Confusing" is not feedback — "I clicked the profile icon expecting account settings but got help center" is.
