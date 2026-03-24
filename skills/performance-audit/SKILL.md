---
name: performance-audit
description: >
  Technical performance evaluation. Tests Core Web Vitals (LCP, FID, CLS), page load times, API response times, bundle size, database query performance. Thresholds: LCP <2.5s, FID <100ms, CLS <0.1. Use before launch.
benefits-from: ux-walkthrough
feeds-into: launch-checklist
---

# Performance Audit

Technical performance is not optional. Users hate slow products. At 100K users, small delays compound into abandonment.

---

## Phase 0: Setup & Tools

**Purpose:** Prepare testing environment and tools.

1. Access live product or staging environment
2. Have these tools ready:
   - Chrome DevTools (Lighthouse tab)
   - WebPageTest (webpagetest.org) optional but helpful
   - Network tab in DevTools for API timing
   - Database profiler access (if applicable: PostgreSQL EXPLAIN ANALYZE, MySQL EXPLAIN)

3. Identify critical endpoints for testing (from MVP-SPEC.md):
   - Login/auth endpoint
   - User data fetch
   - Core feature query

**Exit Criteria:** Environment loaded, tools ready, critical endpoints identified.

**AI Instructions:**
Do not ask any questions. Load context silently. Proceed to Phase 1.

---

## Phase 1: Core Web Vitals (Automated, No Question)

**Purpose:** Test Google's three metrics for user experience.

**AI Instructions:**
Run Lighthouse in Chrome DevTools (or WebPageTest).

Test three metrics:

```
CORE WEB VITALS
===============

Metric 1: Largest Contentful Paint (LCP)
- Target: <2.5s
- What it measures: How long until main content is visible?
- Actual: [X.Xs]
- Status: [GREEN / YELLOW / RED]
- If slow, analysis: [What's blocking render? Images? CSS? JavaScript?]

Metric 2: First Input Delay (FID)
- Target: <100ms
- What it measures: How fast does the app respond to user clicks/taps?
- Actual: [Xms]
- Status: [GREEN / YELLOW / RED]
- If slow, analysis: [Heavy JavaScript? Unresponsive framework? Main thread blocked?]

Metric 3: Cumulative Layout Shift (CLS)
- Target: <0.1
- What it measures: Does content jump around while loading?
- Actual: [X.X]
- Status: [GREEN / YELLOW / RED]
- If high, analysis: [Ads, images, or fonts causing jumps? Unset image dimensions?]
```

**Status Rules:**
- **GREEN**: Metric within target range
- **YELLOW**: Metric 20% above target (e.g., LCP 3.0s when target is 2.5s)
- **RED**: Metric significantly above target (e.g., LCP > 4s, FID > 200ms, CLS > 0.25)

If any metric is RED or YELLOW, use **AskUserQuestion**:

**Re-ground:** "Core Web Vitals: [metric name] is [RED / YELLOW]. Your app feels slow or janky."

**Simplify:** "[Metric] measures [plain English]. Your actual: [X]. Target: [Y]. If it's slow, users bounce. If it's janky, users get confused."

**Recommend:** "RECOMMENDATION: LCP is the biggest blocker (users see nothing). Start there. CLS is second (annoying but less critical). FID is third."

**Options:**
- A) Identify root causes: What's making this metric slow?
- B) List quick wins to improve this metric
- C) Accept the current performance (risky)

Proceed to Phase 2.

---

## Phase 2: Page Load Performance (Automated, No Question)

**Purpose:** Test real-world load times on fast and slow connections.

**AI Instructions:**
Test three scenarios:

```
PAGE LOAD PERFORMANCE
====================

Scenario 1: Fast Connection (Desktop Broadband)
- First contentful paint: [Xs]
- Time to interactive: [Xs]
- Total load time: [Xs]
- Status: [GREEN / YELLOW / RED]

Scenario 2: Slow Connection (4G Throttled)
- First contentful paint: [Xs]
- Time to interactive: [Xs]
- Total load time: [Xs]
- Critical issue: [Does app feel broken or unusable on 4G?]
- Status: [GREEN / YELLOW / RED]

Scenario 3: Cached Load (Return visit)
- Time to interactive: [Xs]
- Status: [GREEN / YELLOW / RED]

Analysis:
- Time to interactive: <3 seconds? [Yes / No]
- On 4G, does app feel responsive? [Yes / No]
```

**Status Rules:**
- **GREEN**: Time to interactive < 3s on broadband, < 5s on 4G
- **YELLOW**: Time to interactive 3-5s on broadband, 5-8s on 4G
- **RED**: Time to interactive > 5s on broadband or > 8s on 4G

If RED on 4G, use **AskUserQuestion**:

**Re-ground:** "4G performance is slow. [X% of your target users] are on slower connections. They're abandoning."

**Simplify:** "If it takes 8+ seconds for your app to be usable on 4G, users won't wait. This kills conversion."

**Recommend:** "RECOMMENDATION: Test on real 4G if possible (not just emulation). 4G is your baseline, not broadband."

**Options:**
- A) Identify bottlenecks: large images, unoptimized bundles, slow API?
- B) List optimization priorities
- C) Accept the slow load (very risky)

Proceed to Phase 3.

---

## Phase 3: Bundle Size Analysis (Automated, No Question)

**Purpose:** Audit JavaScript, CSS, and asset sizes.

**AI Instructions:**
Open Chrome DevTools Network tab. Measure sizes:

```
BUNDLE ANALYSIS
===============

JavaScript:
- Main bundle: [XXkB]
- Total JS: [XXkB]
- Target: <100kB initial load
- Status: [GREEN / YELLOW / RED]

CSS:
- Total CSS: [XXkB]
- Target: <50kB
- Status: [GREEN / YELLOW / RED]

Images/Assets:
- Total: [XXkB]
- Unoptimized images: [Any large PNGs when WebP would work?]
- Status: [GREEN / YELLOW / RED]

Total Page Weight:
- [XXkB]
- Target: <300kB total
- Status: [GREEN / YELLOW / RED]

Analysis:
- Are there unused dependencies? [Yes / No / Unknown]
- Is code-splitting used? [Yes / No]
- Are images optimized? [Yes / No]
```

**Status Rules:**
- **GREEN**: JS < 100kB, CSS < 50kB, total < 300kB
- **YELLOW**: JS 100-150kB or CSS 50-75kB
- **RED**: JS > 150kB or CSS > 75kB or total > 300kB

If RED, use **AskUserQuestion**:

**Re-ground:** "Bundle size: [XXkB]. That's bloated. On 4G, users wait [Y seconds] for code to download."

**Simplify:** "Every kilobyte matters on mobile. Big bundles = slow page loads. Can you remove unused libraries or split code?"

**Recommend:** "RECOMMENDATION: Unused dependencies are quick wins. Check for old libraries you're not using."

**Options:**
- A) List unused dependencies or large libraries that could be removed
- B) Implement code-splitting (load features on-demand, not upfront)
- C) Accept current size (risky on mobile)

Proceed to Phase 4.

---

## Phase 4: API Response Times (Automated, No Question)

**Purpose:** Test critical endpoint performance.

**AI Instructions:**
Use Chrome DevTools Network tab. Call critical endpoints 5-10 times each. Measure 90th percentile response time (not average).

```
API PERFORMANCE
===============

Endpoint 1: /api/login (Authentication)
- 90th percentile: [Xms]
- Target: <500ms
- Status: [GREEN / YELLOW / RED]

Endpoint 2: /api/user (Fetch user data)
- 90th percentile: [Xms]
- Target: <500ms
- Status: [GREEN / YELLOW / RED]

Endpoint 3: [Core feature query]
- 90th percentile: [Xms]
- Target: <500ms (simple) or <1000ms (complex)
- Status: [GREEN / YELLOW / RED]

[Any additional critical endpoints]

Analysis:
- Any endpoints consistently >1000ms? [List]
- Are there timeouts? [Yes / No]
```

**Status Rules:**
- **GREEN**: 90th percentile < 500ms for normal ops, < 1000ms for complex queries
- **YELLOW**: 90th percentile 500-800ms
- **RED**: 90th percentile > 1000ms

If RED, use **AskUserQuestion**:

**Re-ground:** "API endpoint [name] is slow: [Xms]. Users wait, then bounce."

**Simplify:** "Slow APIs kill user experience. Are you missing database indexes? Are you fetching related data inefficiently (N+1 problem)?"

**Recommend:** "RECOMMENDATION: Check database query performance (Phase 5). Missing indexes are common culprits."

**Options:**
- A) Investigate database (Phase 5)
- B) Cache API responses (if data doesn't change often)
- C) Accept the slow endpoint (risky)

Proceed to Phase 5.

---

## Phase 5: Database Query Performance (Optional, Automated)

**Purpose:** Identify slow queries and missing indexes.

**Only run if you have database access. If not, skip to Phase 6.**

**AI Instructions:**
Access database profiler (PostgreSQL EXPLAIN ANALYZE, MySQL EXPLAIN):

```
DATABASE PERFORMANCE
====================

Slow Queries (>1s):
- [Query 1]: [Duration]ms. Reason: [Full table scan? Missing index?]
- [Query 2]: [Duration]ms. Reason: [Joined tables inefficiently?]

Missing Indexes:
- [Table.column]: Missing index on frequently queried column
- [Table.column]: Helps with this query: [Query name]

N+1 Problems:
- [Example]: Fetching user list, then fetching profile for each user (N+1 calls)
- Impact: [Could be reduced to 1 batched query]

Connection Health:
- Connection pooling: [Configured? Size OK?]
- Timeout settings: [Reasonable?]

Recommendations:
1. [Add index to Table.column]
2. [Fix N+1 query]
3. [Increase connection pool]
```

If slow queries found, use **AskUserQuestion**:

**Re-ground:** "Found slow queries in the database. This is why API endpoint [name] is slow."

**Simplify:** "Missing indexes are the most common culprit. Adding one index can 10x query speed."

**Recommend:** "RECOMMENDATION: Start with EXPLAIN ANALYZE to find missing indexes. Cheap quick win."

**Options:**
- A) List missing indexes with expected impact
- B) Review N+1 queries and prioritize fixes
- C) No database access, skip this phase

Proceed to Phase 6.

---

## Phase 6: Critical Issues & Sign-off (AskUserQuestion)

**Purpose:** Summarize findings and make launch decision.

The AI must use the **AskUserQuestion tool**:

**Re-ground:** "Performance audit complete. Core Web Vitals: [summary]. Load times: [summary]. APIs: [summary]. Database: [summary]."

**Simplify:** "Are there any RED issues that would make users abandon? Slow load times on mobile, unresponsive clicks, janky animations?"

**Recommend:** "RECOMMENDATION: Fix all RED items before launch. YELLOW items can wait until post-launch."

**Options:**
- A) Ready for launch (no RED issues)
- B) Fix critical issues first (list RED items, estimate time to fix)
- C) Not ready (too many blockers)

**Exit Criteria:** Launch decision made. Proceed to Phase 7.

---

## Phase 7: Output & Roadmap

**Purpose:** Create the audit report and optimization roadmap.

**AI Instructions:**
Create PERFORMANCE-AUDIT.md with this format:

```markdown
# Performance Audit Report

## Test Date
[Date] | Environment: [Staging / Production]

## Summary

| Metric | Target | Actual | Status |
|--------|--------|--------|--------|
| LCP | <2.5s | [X.Xs] | [GREEN/YELLOW/RED] |
| FID | <100ms | [Xms] | [GREEN/YELLOW/RED] |
| CLS | <0.1 | [X.X] | [GREEN/YELLOW/RED] |
| Load time (4G) | <5s | [Xs] | [GREEN/YELLOW/RED] |
| API 90th p | <500ms | [Xms] | [GREEN/YELLOW/RED] |

**Overall status**: [GREEN / YELLOW / RED]

---

## Core Web Vitals

### Largest Contentful Paint (LCP)
- **Target**: <2.5s
- **Actual**: [X.Xs]
- **Status**: [GREEN / YELLOW / RED]
- **Analysis**: [What's slow? Images? CSS? JS rendering?]

### First Input Delay (FID)
- **Target**: <100ms
- **Actual**: [Xms]
- **Status**: [GREEN / YELLOW / RED]
- **Analysis**: [Main thread blocked? Heavy JS?]

### Cumulative Layout Shift (CLS)
- **Target**: <0.1
- **Actual**: [X.X]
- **Status**: [GREEN / YELLOW / RED]
- **Analysis**: [Images without dimensions? Ads? Fonts?]

---

## Page Load Performance

### Fast Connection (Desktop Broadband)
- First contentful paint: [Xs]
- Time to interactive: [Xs]
- Total load time: [Xs]

### Slow Connection (4G Throttled)
- First contentful paint: [Xs]
- Time to interactive: [Xs]
- Total load time: [Xs]
- **Critical issue**: [Does app feel broken on 4G?]

### Cached Load (Return Visit)
- Time to interactive: [Xs]

---

## Bundle Analysis

```
JavaScript:
- Main bundle: [XXkB]
- Total: [XXkB]
- Unused code: [Any large unused libraries?]

CSS:
- Total: [XXkB]

Images/Assets:
- Total: [XXkB]

Total page weight: [XXkB] (Target: <300kB)

Recommendation: [Is this bloated? What can be removed?]
```

---

## API Performance

| Endpoint | Purpose | 90th Percentile | Status |
|----------|---------|-----------------|--------|
| /api/login | Authentication | [Xms] | [GREEN/YELLOW/RED] |
| /api/user | Fetch user | [Xms] | [GREEN/YELLOW/RED] |
| [Critical endpoint] | [Purpose] | [Xms] | [GREEN/YELLOW/RED] |

---

## Database Performance

### Query Analysis
- Slow queries (>1s): [List with analysis]
- Missing indexes: [List identified]
- N+1 problems: [List detected]

### Connection Health
- Connection pooling: [Configured?]
- Timeout settings: [Reasonable?]

---

## Critical Issues (Must Fix Before Launch)

1. [Issue and user impact]
2. [Issue and user impact]

(If none, write "No critical issues found.")

---

## Important Issues (Fix in next sprint)

1. [Issue]
2. [Issue]

(If none, write "No important issues found.")

---

## Optimization Roadmap

### Quick Wins (< 2 hours each)
- [Optimization 1]
- [Optimization 2]

### Medium Effort (2-8 hours each)
- [Optimization 1]

### Larger Effort (> 8 hours each)
- [Optimization 1]

---

## Sign-off

- **Performance ready for launch?**: YES / NO / CONDITIONAL
- **Top blocker**: [What's the worst performance issue?]
- **User impact**: [At 100K users, slow performance = abandonment. What % of users affected?]
- **Recommendation**: [Fix all RED items before launch. YELLOW items can wait.]

**Auditor**: [Name]
**Date**: [Date]
```

**Tone Guidance:**
- Don't hide behind "it's fast enough."
- At 100K users, small delays compound into real abandonment.
- Be honest: "LCP 4s means 20% of users bounce before seeing anything."
- Celebrate wins: "4G load time is 3.5s. That's good."

---

## Escape Hatches

**If user is impatient ("just do it"):**
- Skip details. Run Phase 1 (Core Web Vitals) only.
- Output: "LCP: [X], FID: [X], CLS: [X]. Status: [color]."
- Jump to sign-off.

**If all metrics are GREEN:**
- Skip detailed explanations. Confirm green status and proceed to output.

**If database access is unavailable:**
- Skip Phase 5 entirely.
- Note in output: "Database profiling not available. Recommend DBA review before launch."

---

## When to Run

- **Before launch readiness** (2-4 weeks before target launch)
- **After major code changes** (new framework, refactor, feature additions)
- **If UX testing revealed slowness** (run performance audit to diagnose)

---

## Completion Status

At the end of the skill, report one of:
- **DONE**: Audit complete, all metrics GREEN, ready for launch
- **DONE_WITH_CONCERNS**: Audit complete, YELLOW metrics identified, fix before launch
- **BLOCKED**: Cannot access environment or tools (staging/production down)
- **NEEDS_CONTEXT**: Unclear which endpoints are critical; ask user for list
