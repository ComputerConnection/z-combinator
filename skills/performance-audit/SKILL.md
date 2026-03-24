---
name: performance-audit
description: Technical performance evaluation. Tests Core Web Vitals (LCP, FID, CLS), page load times, API response times, bundle size, database query performance. Thresholds: LCP <2.5s, FID <100ms, CLS <0.1. Use before launch.
---

# Performance Audit

Test the technical performance of your app. Users hate slow products. This isn't optional.

## What You Do

1. Access the live product or staging environment
2. Test Core Web Vitals (Google's user experience metrics):
   - **LCP (Largest Contentful Paint)**: How long until main content is visible? Target: <2.5s
   - **FID (First Input Delay)**: How fast does the app respond to user input? Target: <100ms
   - **CLS (Cumulative Layout Shift)**: Does content jump around while loading? Target: <0.1
3. Test page load times:
   - On fast connection (desktop broadband)
   - On slow connection (4G / 3G if possible)
   - First load vs cached load
4. Test API response times:
   - Critical endpoints (login, fetch user data, core feature queries)
   - Threshold: <500ms for normal operations, <1s for complex queries
5. Analyze bundle size:
   - JavaScript bundle: Should be <100KB for initial load
   - CSS: <50KB
   - Total page: <300KB
   - Flag: Does it have unused dependencies?
6. Database performance:
   - Are queries indexed? Run slow query logs.
   - N+1 problem: Are you fetching related data inefficiently?
   - Connection pooling: Is it configured?

## Tools

- **Lighthouse** (built into Chrome DevTools) for Core Web Vitals and performance scoring
- **WebPageTest** (webpagetest.org) for detailed waterfall analysis
- **Chrome DevTools** Network tab for API timing
- **Database profiler** (PostgreSQL: EXPLAIN ANALYZE, MySQL: EXPLAIN)

## Output: PERFORMANCE-AUDIT.md

Format:
```
# Performance Audit Report

## Test Date
[Date and environment]

## Core Web Vitals

### Largest Contentful Paint (LCP)
- **Target**: <2.5s
- **Actual**: [X.Xs]
- **Status**: GREEN / YELLOW / RED
- **Analysis**: [If above target, what's slow?]

### First Input Delay (FID)
- **Target**: <100ms
- **Actual**: [Xms]
- **Status**: GREEN / YELLOW / RED
- **Analysis**: [Heavy JavaScript? Unresponsive framework?]

### Cumulative Layout Shift (CLS)
- **Target**: <0.1
- **Actual**: [X.X]
- **Status**: GREEN / YELLOW / RED
- **Analysis**: [Ads, images, or fonts causing jumps?]

## Page Load Performance

### Fast Connection (Broadband)
- First contentful paint: [Xs]
- Time to interactive: [Xs]
- Total load time: [Xs]

### Slow Connection (4G throttled)
- First contentful paint: [Xs]
- Time to interactive: [Xs]
- Total load time: [Xs]
- **Critical issue**: [Does app feel broken on slow connections?]

### Cached Load
- Time to interactive: [Xs]

## Bundle Analysis

```
JavaScript: [XXkB]
- Main bundle: [XXkB]
- Unused code: [Any large unused libraries?]

CSS: [XXkB]

Images/Assets: [XXkB]

Total: [XXkB]

Recommendation: [Is this bloated? What can be removed?]
```

## API Performance

| Endpoint | Purpose | 90th percentile | Status |
|----------|---------|-----------------|--------|
| /api/login | Authentication | [Xms] | GREEN/YELLOW/RED |
| /api/user | Fetch user | [Xms] | GREEN/YELLOW/RED |
| [Critical endpoint] | [Purpose] | [Xms] | GREEN/YELLOW/RED |

## Database Performance

### Query Analysis
- Slow queries (>1s): [List and analysis]
- Missing indexes: [List identified]
- N+1 problems: [Any detected?]

### Connection Health
- Connection pooling: [Configured?]
- Timeout settings: [Reasonable?]

## Critical Issues (Must Fix Before Launch)

1. [Issue and impact]
2. [Issue and impact]

## Important Issues (Fix in next sprint)

1. [Issue]
2. [Issue]

## Optimization Recommendations (Priority Order)

- [Quick win 1]
- [Quick win 2]
- [Larger optimization 3]

## Sign-off

- **Performance ready for launch?**: YES / NO
- **Top blocker**: [What's the worst performance issue?]
- **User impact**: [How many users affected by slow performance?]
```

Don't hide behind "it's fast enough." At 100K users, small delays compound. Slow products die.
