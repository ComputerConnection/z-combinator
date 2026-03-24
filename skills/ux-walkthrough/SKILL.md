---
name: ux-walkthrough
description: First-time user simulation through critical path. Evaluates time to first value, confusion points, onboarding, error handling, mobile experience, accessibility. "If your mom couldn't figure this out in 3 minutes, it's not ready." Use before launch readiness.
benefits-from: performance-audit
feeds-into: launch-checklist
---

# UX Walkthrough

Simulate a first-time user with zero context. Brutal honesty about friction.

---

## Phase 0: Setup & Prep

**Purpose:** Load the product and critical path definition.

1. Read MVP-SPEC.md to identify the critical path (primary user journey)
2. Access the live product or staging environment
3. Verify environment: staging or production?
4. Have a way to capture issues (notes, screenshots, or video if possible)

**Exit Criteria:** Product loaded, critical path identified, ready to walk through.

**AI Instructions:**
Do not ask any questions. Load context silently. Proceed to Phase 1.

---

## Phase 1: Critical Path Walkthrough (Automated, No Question)

**Purpose:** Simulate first-time user experience from landing to first value.

**AI Instructions:**
Start from cold. No prior knowledge. No hand-holding.

Walk through the critical path:
1. Land on homepage
2. Understand what the product does (no reading docs)
3. Understand who it's for (no reading docs)
4. Sign up or log in (whichever is required)
5. Reach the core feature
6. Get value (complete the primary action)

**Document every decision point, click, and moment of confusion:**

```
CRITICAL PATH WALKTHROUGH
==========================

Critical User Story: [From MVP-SPEC.md]

Timeline:
- [0:00] Landed on [URL]
  - First impression: [What did user see?]

- [0:15] [Action taken] → [Observed outcome]
  - Clarity: [Obvious / Somewhat clear / Confusing]

- [1:00] [Action taken] → [Observed outcome]
  - Clarity: [Obvious / Somewhat clear / Confusing]

- [2:30] [Action taken] → [Reached first value]
  - Clarity: [Was it obvious that they got value?]

TOTAL TIME TO FIRST VALUE: [X minutes]
```

**Evaluate against standards:**

| Metric | Standard | Actual | Status |
|--------|----------|--------|--------|
| Time to first value | <3 min | [X min] | [GREEN/YELLOW/RED] |
| Clicks to value | <5 | [X] | [GREEN/YELLOW/RED] |
| Confusion points | 0 | [X] | [GREEN/YELLOW/RED] |

If time > 3 minutes or confusion detected, proceed to Phase 2.
If time < 3 minutes and no confusion, skip Phase 2 and go to Phase 3.

---

## Phase 2: Confusion Points Deep Dive (AskUserQuestion)

**Purpose:** Identify and document friction moments.

Only run if Phase 1 found confusing moments or slow time-to-value.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "You took [X minutes] to reach first value. The standard is 3 minutes. Let's identify where the friction was."

**Simplify:** "Think like your mom trying your product for the first time. Where did she get stuck? Where did she ask 'why am I here?' or 'what do I click?' Be specific about the moment and what was confusing."

**Recommend:** "RECOMMENDATION: Every confusion point is a fix priority. Specific examples help: 'I clicked the profile icon expecting account settings but got the help center' beats 'the UI is confusing.'"

**Options:**
- A) List confusion points with specifics: action → expected outcome vs actual outcome
- B) Video or screenshot walk-through of confusing moments (if possible)
- C) Summary: "3 confusion points: onboarding unclear, button labels vague, error message cryptic"

**Exit Criteria:** Confusion points documented. Proceed to Phase 3.

---

## Phase 3: Error State Testing (Automated, No Question)

**Purpose:** Test how the product fails gracefully.

**AI Instructions:**
Deliberately trigger errors. Document what the user sees:

```
ERROR STATE TESTING
===================

Scenarios tested:
1. [Invalid input] → Error message: [What did user see?]
   - Clarity: [Clear next step / Generic / Cryptic]
   - Example: "Password too short" vs generic "Error"

2. [Network timeout] → Error message: [What?]
   - Clarity: [Helpful / Vague]

3. [Missing required field] → Error message: [What?]
   - Clarity: [Specific / Generic]

Quality Assessment:
- Error messages: [Good / Poor / Inconsistent]
- Do users know what to do next? [Yes / No / Sometimes]
- Example of worst error: [Describe]

Status: [GREEN / YELLOW / RED]
```

**Status Rules:**
- **GREEN**: All error messages are clear, specific, and guide user to fix
- **YELLOW**: Some error messages are vague; most are fixable
- **RED**: Error messages are cryptic or don't explain how to recover

If RED, use **AskUserQuestion**:

**Re-ground:** "Error messages are [RED / YELLOW]. Users don't know how to recover."

**Simplify:** "When something breaks, do users know what happened and what to do next? Or are they stuck?"

**Recommend:** "RECOMMENDATION: Every error message must say: 'What went wrong' and 'How to fix it.' Bad: 'Error 500.' Good: 'Password must be 8+ characters.'"

**Options:**
- A) List error messages that need improvement (with better message suggestions)
- B) Summary: "2 critical errors need better messaging before launch"
- C) All error messages are good (proceed to Phase 4)

Proceed to Phase 4.

---

## Phase 4: Mobile Experience (Automated, No Question)

**Purpose:** Test responsiveness and mobile usability.

**AI Instructions:**
Access the product on a phone (or use browser mobile emulation).

Walk through the critical path again on mobile:

```
MOBILE EXPERIENCE TEST
======================

Device: [Phone / Emulation]
Screen size: [Dimensions]

Critical Path on Mobile:
- [0:00] Landing page
  - Layout: [Responsive / Broken]
  - Text readable: [Yes / No]
  - Touch targets (buttons): [Good size / Too small]

- [Time] Core feature access
  - Full feature parity: [Yes / No / Gaps]
  - If gaps: [List missing features or UI elements]

- [Time] First value on mobile
  - Works: [Yes / No]
  - Performance: [Fast / Slow]
  - 4G experience: [Tested / Not tested]

Summary:
- Responsive: [Yes / No]
- Functional gaps: [List if any]
- Performance: [Good / Slow on 4G]
- Touch targets appropriate: [Yes / No]

Status: [GREEN / YELLOW / RED]
```

**Status Rules:**
- **GREEN**: Full feature parity, responsive, fast on mobile
- **YELLOW**: Responsive but slow on 4G, or 1-2 minor features missing on mobile
- **RED**: Broken layout, missing critical features on mobile, unusable on 4G

If RED or YELLOW, use **AskUserQuestion**:

**Re-ground:** "Mobile experience: [RED / YELLOW]. Users on phones will struggle."

**Simplify:** "Is your product usable on a phone? Can someone complete the core task, or is it broken/slow?"

**Recommend:** "RECOMMENDATION: Test on real 4G if possible (not just WiFi). Slow mobile = user abandonment. Common issues: unoptimized images, no lazy loading, font too small."

**Options:**
- A) List mobile issues with fix priority (critical vs nice-to-have)
- B) Summary: "2 critical gaps on mobile (missing feature X, slow load on 4G)"
- C) Mobile experience is good (proceed to Phase 5)

Proceed to Phase 5.

---

## Phase 5: Accessibility Basics (Automated, No Question)

**Purpose:** Test basic WCAG AA compliance.

**AI Instructions:**
Run accessibility checks:

```
ACCESSIBILITY BASICS
====================

Test 1: Images
- Alt text present on all images? [Yes / No / Partial]
- Is alt text descriptive? [Yes / Generic / Missing]

Test 2: Form Labels
- All input fields have associated labels? [Yes / No]
- Can you understand what each field is for? [Yes / No]

Test 3: Color Contrast
- Text vs background sufficient (WCAG AA)? [Yes / No / Not sure]
- Red/green colors used to convey meaning? [Yes / No]

Test 4: Keyboard Navigation
- Can you tab through the app? [Yes / No]
- Can you click buttons with keyboard? [Yes / No]

Test 5: Screen Reader
- Can a screen reader understand the page? [Yes / No / Partial]

Summary:
- Missing alt text: [Count and locations]
- Missing form labels: [Count and locations]
- Keyboard issues: [Count and locations]

Status: [GREEN / YELLOW / RED]
```

**Status Rules:**
- **GREEN**: WCAG AA compliant, alt text present, labels clear, keyboard navigable
- **YELLOW**: Minor gaps (1-2 images missing alt text, one form field unlabeled)
- **RED**: Significant accessibility barriers (no alt text, unlabeled form fields, not keyboard navigable)

If RED or YELLOW, use **AskUserQuestion**:

**Re-ground:** "Accessibility: [RED / YELLOW]. Some users cannot access your product."

**Simplify:** "Accessibility isn't just moral — it's legal. If you get users with screen readers or who use keyboard only, they're stuck. What accessibility issues do you know about?"

**Recommend:** "RECOMMENDATION: Start with alt text (quick win) and form labels (critical). WCAG AA is the standard for public products."

**Options:**
- A) List accessibility gaps with fix effort (quick wins vs larger effort)
- B) Summary: "3 quick wins: alt text on 5 images, label 2 form fields, etc."
- C) Accessibility is good (proceed to Phase 6)

Proceed to Phase 6.

---

## Phase 6: Overall Assessment & Sign-off (AskUserQuestion)

**Purpose:** Make the launch-readiness call.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "You completed the walkthrough. Time to first value: [X min]. Confusion points: [X]. Mobile: [Status]. Accessibility: [Status]."

**Simplify:** "Put yourself in your mom's shoes. If she landed on this product with zero context, could she get value in 3 minutes without being confused? Is she blocked by mobile or accessibility issues?"

**Recommend:** "RECOMMENDATION: If time > 3 min AND there are confusion points, it's not ready. If mobile is RED, it's not ready. Mark CONDITIONAL if there are quick wins to fix before launch."

**Options:**
- A) Ready for launch (time < 3 min, zero confusion, mobile OK, accessibility OK)
- B) Conditional (quick fixes needed: [list them, with time estimates])
- C) Not ready (major UX work required before launch)

**Exit Criteria:** Launch-readiness call made. Proceed to Phase 7.

---

## Phase 7: Output & Recommendations

**Purpose:** Create the audit report.

**AI Instructions:**
Create UX-AUDIT.md with this format:

```markdown
# UX Walkthrough Report

## Test Date
[Date] | Environment: [Staging / Production]

## Critical Path Tested
[User story from MVP-SPEC.md]

## Timeline & Key Moments

| Time | Action | Outcome | Clarity |
|------|--------|---------|---------|
| 0:00 | Landed on home page | Saw headline + CTA | Clear |
| 0:30 | Clicked [button] | Taken to [page] | Somewhat clear |
| [time] | [action] | [outcome] | [Clear / Confused] |

**Total time to first value: [X minutes]** (Standard: <3 min)

## Confusion Points Found

[If none, write "No confusion points detected."]

### [Issue #1]
- **What happened**: [Specific action and unexpected outcome. E.g., "Clicked the profile icon expecting account settings but got the help center"]
- **Why it's a problem**: [User impact. E.g., "User wasted 30 seconds and thought the feature was broken"]
- **Severity**: [RED / YELLOW / GREEN]
- **Recommended fix**: [E.g., "Relabel icon or move settings to correct place"]

### [Issue #2]
...

## Error State Testing

**Scenarios tested:**
- [Invalid input]
- [Network timeout]
- [Missing required field]
- [etc.]

**Quality assessment:**
- Error message clarity: [Good / Poor / Inconsistent]
- Do users know what to do next? [Yes / No]

**Example of worst error:**
[Describe: "When I entered a weak password, the app said 'Error 500.' I didn't know what went wrong or how to fix it."]

**Status**: [GREEN / YELLOW / RED]

## Mobile Experience

- **Responsive**: [Yes / No]
- **Load time on 4G**: [Tested: X sec / Not tested]
- **Functional gaps on mobile**: [List if any]
- **Touch targets**: [Good size / Too small]
- **Status**: [GREEN / YELLOW / RED]

## Accessibility Basics

- **Images**: Alt text present? [Yes / No / Partial]. If no, list missing.
- **Form labels**: Associated with inputs? [Yes / No / Partial]. If no, list missing fields.
- **Keyboard navigation**: Can you tab through? [Yes / No]
- **Color contrast**: WCAG AA compliant? [Yes / No / Not sure]
- **Screen reader**: Readable? [Yes / No / Partial]
- **Status**: [GREEN / YELLOW / RED]

## Overall Assessment: Mom Test

**If your mom couldn't figure this out in 3 minutes, it's not ready.**

- Landing → signup/login: [X min, Y clicks, friction level]
- First feature access: [X min, Y clicks, clarity level]
- Core value delivery: [X min, obvious? Y/N]

## Critical Issues (Must Fix Before Launch)

1. [Issue + impact + fix]
2. [Issue + impact + fix]

(If none, write "No critical issues found.")

## Important Issues (Fix in next sprint)

1. [Issue]
2. [Issue]

(If none, write "No important issues found.")

## Recommended Fixes (Priority Order)

### Quick Wins (< 2 hours each)
- [Fix 1]
- [Fix 2]

### Medium Effort (2-8 hours each)
- [Fix 1]
- [Fix 2]

### Larger Effort (> 8 hours)
- [Fix 1]

## Sign-off

- **Ready for launch?**: YES / NO / CONDITIONAL
- **Top blocker (if any)**: [What must change before shipping?]
- **Quick wins to do before launch**: [List if CONDITIONAL]
- **Severity if shipped as-is**: [User impact if shipped with issues]

**Tester**: [Name]
**Date**: [Date]
```

**Tone Guidance:**
- Specific > vague. "I clicked the profile icon expecting account settings but got the help center" beats "the UI is confusing."
- Be honest. If someone would bounce in 30 seconds, say it.
- Celebrate wins: "Time to first value: 1.5 minutes. That's good."
- Flag blockers: "Mobile is broken on 4G. Users will abandon."

---

## Escape Hatches

**If user is impatient ("just do it"):**
- Skip detailed confusion analysis (Phase 2).
- Run Phase 1, Phase 3 (error testing), Phase 6 (sign-off).
- Output a condensed audit.

**If product is obviously not ready:**
- Stop after Phase 1. If time > 5 min and confusion > 3 points, mark RED and escalate.
- Don't waste time on fine-grained analysis.

**If product is mobile-first:**
- Prioritize Phase 4 (mobile). Phase 5 (accessibility) is secondary.

---

## When to Run

- **Before launch readiness** (2-4 weeks before target launch)
- **After major UX changes** (redesign, flow change)
- **When NPS or user feedback suggests friction**

---

## Completion Status

At the end of the skill, report one of:
- **DONE**: Audit complete, ready for launch (no critical issues)
- **DONE_WITH_CONCERNS**: Audit complete, conditional launch (quick fixes needed)
- **BLOCKED**: Cannot access product (staging/production down)
- **NEEDS_CONTEXT**: Unclear what critical path to test; ask user for user story
