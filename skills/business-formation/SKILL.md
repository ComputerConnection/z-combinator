---
name: business-formation
description: >
  Guide founders through operational fundamentals — entity setup, co-founder agreements, IP assignment, banking, bookkeeping, taxes, insurance, and contractor agreements. Most technical founders skip this and regret it.
trigger_phrases:
  - "business formation"
  - "set up my company"
  - "LLC or C-Corp"
  - "legal structure"
  - "operations setup"
  - "stage 5"
version: 1.0
---

# Business Formation & Legal Structure

You've been building for weeks or months. Code is shipping. But here's the uncomfortable question: **Who actually owns this company?** Who owns the code? If something goes wrong, what are you personally liable for?

Most technical founders skip this section entirely. Then at funding time — or worse, during a co-founder conflict — they discover they've built everything under a structure that was never set up. This skill ensures you've at least *thought* about these operational fundamentals and have a documented plan.

**DISCLAIMER:** This is NOT legal or tax advice. You should consult with a lawyer and accountant for decisions that are right for your specific situation. This skill ensures you've asked the right questions and documented your choices.

---

## 1. Entity Structure

### The Choice: LLC vs. C-Corporation

Before you can open a bank account, hire anyone, or take funding, you need a legal entity. There are two main paths:

#### LLC (Limited Liability Company)
- **Setup:** Simpler, cheaper (typically $100-500 in filing fees)
- **Taxes:** Pass-through by default (income flows to personal return, you pay self-employment tax)
- **Liability:** Personal assets somewhat protected, but not bulletproof
- **Funding:** VCs won't touch an LLC. If you plan to raise institutional funding, this is a dead end.
- **Best for:** Solo founders, bootstrapped projects, service businesses, early exploration phase

#### C-Corporation
- **Setup:** More complex, more expensive ($500-2000+ depending on state)
- **Taxes:** Corporate structure (you pay corporate + personal tax on dividends — double taxation)
- **BUT:** Allows preferred stock, option pools, investment structures VCs expect
- **Liability:** Strong personal asset protection
- **Funding:** Required for institutional investment (most angel/VC investments)
- **Best for:** Any founder who thinks they might raise funding, or wants that optionality

### State of Incorporation

If you form a C-Corp, you must choose a state:

- **Delaware:** The standard for funded startups (not for tax reasons — for legal precedent and investor preference). If you're in California and form a Delaware C-Corp, you'll pay California tax anyway due to "unitary tax" laws, but you get Delaware corporate law.
- **Your home state:** Simpler, cheaper, less corporate formality required. Totally fine for bootstrapped projects and early stage.

**Rule of thumb:** If you think you might raise funding → Delaware C-Corp. If you're bootstrapping and want simplicity → LLC or home-state C-Corp.

### The Founder's Dilemma

**If co-founders:** Do not skip this. Ownership and decision-making must be documented. The conversation is awkward. Do it anyway.

**Key decisions:**
- Equity split: what % does each founder own?
- Vesting schedule: over what period, with what cliff?
- IP assignment: who owns the code built before incorporation?
- Decision authority: who has veto rights? Who breaks ties?

---

## 2. Co-Founder Agreements (If Applicable)

### Equity Split

The "fair" split is NOT 50/50 if founders have different contributions.

**Common frameworks:**

| Scenario | Split | Reasoning |
|----------|-------|-----------|
| Equal skill, equal time commitment | 50/50 | Truly equal footing |
| One founder full-time, one part-time | 60/40 or 70/30 | Time commitment differs |
| One founder has existing audience/product | Negotiated | Pre-existing value |
| One founder is CEO/technical, one is business | Often equal or 60/40 | Different but complementary roles |
| One founder has no time for 12 months | Consider delayed equity | "Sweat equity" needs equal time investment |

**The mistake:** Doing 50/50 without vesting. Then one founder leaves month 3, still owns 50%, and the remaining founder is stuck.

### Vesting Schedules

**Standard:** 4-year vesting with 1-year cliff. Here's why:

- **4-year total:** Most startups take 3-4 years to know if the founding team is right. This horizon makes sense.
- **1-year cliff:** You don't vest a single share until you complete 1 full year. This weeds out people not committed to the journey. It's the reality check.
- **Monthly vesting after cliff:** After the cliff, you vest 1/48th of your equity each month. This is "quitting tax" — if you leave before 4 years, you forfeit unvested equity.

**Example:** Founder A gets 500,000 shares (50%), 4-year vesting, 1-year cliff.
- Month 12: Vests 125,000 shares (1/4 of total). If they quit now, they keep 125k.
- Month 24: Vests another 125,000 (now 250k total vested). Progress.
- Month 48: All 500k vested. They own it fully.

**Why this matters:** Without vesting, Founder B can leave day 30 and still own 50% of your company. You're stuck negotiating to buy back their shares (expensive, messy, sometimes impossible).

### IP Assignment

**Before incorporation:** Who owns the code you built on your laptop?

Technically, YOU do — the person who wrote it. But if you're co-founders building a company, the company should own the IP.

**Steps:**
1. Before or immediately after incorporation, sign an **IP Assignment Agreement** (fancy name for a document saying "I assign all IP related to this company to the company")
2. Include both code written *before* incorporation (important!) and going forward
3. If any founder has pre-existing projects or code they want to keep personal, carve that out explicitly in writing
4. Same applies to any contractor/consultant work — get written IP assignment

**Why:** If founder disputes arise or you take investment, investors will ask "Who owns the code?" If it's unclear, deal falls apart.

---

## 3. Banking

### Separate Business Account

This is non-negotiable, even as a solo founder:

- **Tax clarity:** Personal and business expenses stay separate (your accountant will thank you)
- **Legitimacy:** Lenders, investors, and partners take you seriously
- **Liability separation:** Mixing personal/business finances weakens liability protection

### Recommended Options for Startups

- **Traditional bank (Wells Fargo, Chase, etc.):** Full-featured but slowest, highest minimums, worst for startups
- **Stripe Treasury, Mercury, Ramp, etc.:** Built for startups, low friction, integrated accounting tools, good UX
- **Small business banks (Silicon Valley Bank, etc.):** Good service but closures have been common
- **Credit union:** Lower fees, better rates sometimes, but older tech

**Minimum recommendation:** Get a business checking account. You don't need a line of credit yet.

### What You'll Need

- EIN (Employer Identification Number — free from IRS)
- Business license (often automatic when you form the entity)
- Articles of Incorporation/Organization
- ID

---

## 4. Basic Bookkeeping

You don't need an accountant yet. But you need a system.

### What to Track

- **Income:** Every dollar that comes in, date, source
- **Expenses:** Every dollar that goes out, date, category, business purpose
- **Receipts:** Save them (digital or physical) for 7 years in case of audit
- **Payroll/equity:** If you're paying yourself or others, document it

### Tools (Pick One)

- **Wave:** Free, good enough for early stage
- **QuickBooks Online:** Industry standard, ~$30/month
- **Stripe or payment processor:** Integrates with your revenue
- **Spreadsheet:** Better than nothing, but annoying at scale

### When to Get an Accountant

- **Month 1-6:** You can DIY with discipline
- **Month 6+:** Get a CPA to do quarterly estimates and advise on tax strategy
- **After raising funding:** Required (investors demand it)

---

## 5. Tax Obligations

### Estimated Quarterly Taxes (If C-Corp or Self-Employed LLC)

If you're making money and paying yourself, the IRS expects payment 4x/year:
- April 15 (Q1: Jan-Mar)
- June 15 (Q2: Apr-Jun)
- September 15 (Q3: Jul-Sep)
- January 15 next year (Q4: Oct-Dec)

Miss these and you'll pay penalties. Get your accountant to calculate.

### Self-Employment Tax (If LLC Sole Proprietor)

If you're an LLC taxed as a sole proprietor, you pay self-employment tax (~15.3%) on net income. A C-Corp might be more efficient if you're profitable (but less so if you're losing money).

### State Requirements

- **Sales tax:** If you sell digital products or physical goods, most states require sales tax collection (varies wildly by state and product type)
- **Payroll tax:** If you hire anyone (including yourself as W-2), you need payroll tax setup
- **State income tax:** Some states (California, New York) tax residents; some don't (Texas, Florida, Nevada)

**Action:** Get a tax advisor to review your state's requirements. $500 in advice now saves thousands in penalties later.

---

## 6. Insurance

### Do You Need It?

**Short answer:** Probably yes. Here's the breakdown:

| Coverage | Cost | Need It? | Why |
|----------|------|----------|-----|
| General Liability | $400-1500/yr | Maybe | Covers accidents, injuries on your property, etc. If you have anyone visiting your workspace, YES. |
| Professional Liability | $500-2000/yr | Maybe | Covers if your product/service causes damage. Less critical early, matters later. |
| Cyber Liability | $600-2000/yr | Maybe | Covers data breaches, hacks. More important if handling customer data. |
| Workers Compensation | Required | If you hire | Required by law if you have employees (varies by state) |
| Founders Insurance | $5000-15000 | No, not yet | Covers founder death/disability. Maybe later if high-risk activity or co-founder dependency. |

**Recommendation:** Get basic general liability. It's cheap and gives you credibility. Revisit as you grow.

### Where to Get It

- **Online platforms:** Stride Health, Catch, Lemonade (faster, cheaper, simpler)
- **Insurance broker:** More personalized (and pricey)
- **Industry-specific:** Talk to other founders in your space

---

## 7. Contracts for Contractors & Consultants

If you hire a contractor (designer, engineer, marketer, etc.), you need a written agreement. Here's why:

- **Tax treatment:** Misclassifying an employee as a contractor triggers IRS penalties
- **IP ownership:** Without a contract, the contractor might own the work they did (especially code)
- **Scope clarity:** Reduces disputes about what was actually agreed to

### Minimum Agreement Should Cover

- Scope of work (what exactly are they building/doing?)
- Timeline and deliverables
- Payment (amount, schedule)
- IP assignment (contractor assigns work to you/company)
- Confidentiality (if applicable)
- Term (when does it end?)

### Templates

- **LawDepot, Rocket Lawyer, Fiverr:** $20-100 for templates
- **GitHub:** Search "contractor agreement template" — many founders share theirs
- **Lawyer:** $500-1500 for custom agreement (overkill for early stage, useful if complex work)

---

## 8. The Operational Checklist

This skill will now ask you about your current status across these areas and produce an **OPS-CHECKLIST.md** file with:

- [ ] Status on each area (Not Started / In Progress / Complete)
- [ ] Priority ordering (blocking items first)
- [ ] Flags for missing pieces
- [ ] Next concrete steps

Let's start the assessment.

---

## Next Steps

I'm going to ask you some direct questions about your current setup. Your answers will populate an OPS-CHECKLIST.md with your actual status and what needs attention.

**Ready?**

When you are, I'll ask about:
1. Your entity structure (or lack thereof)
2. Co-founder situation and equity
3. Banking setup
4. Your current financial tracking
5. Tax planning
6. Insurance
7. Any contractor/consultant agreements

Once done, you'll have a prioritized, honest checklist of what needs doing.
