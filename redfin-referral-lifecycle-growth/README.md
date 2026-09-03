# Redfin — Building a Closed-Loop Referral & Lifecycle Growth System

**Role:** Data Analyst → Senior Digital Marketing Specialist  
**Company:** Redfin  
**Period:** 2013–2015  
**Focus:** Product Analytics · Growth · Experimentation · Customer Lifecycle · Revenue Measurement

## The Problem

Redfin had a large and growing digital audience, but understanding what happened between an online interaction and an eventual real-estate transaction was difficult.

A click, registration, referral, tour request, or agent contact could happen well before a customer bought or sold a home. That made traditional acquisition metrics incomplete: traffic and leads mattered, but the real question was whether those behaviors ultimately created customers and revenue.

My work focused on connecting those pieces.

I built analyses and experiments that followed customer behavior through the funnel, connected acquisition and referral activity to closed transactions, and used the findings to recommend changes to Redfin's customer experience and growth systems.

## Building the Measurement System

Rather than stopping at top-of-funnel metrics, I used Redfin's behavioral and transactional data to connect:

**Traffic → Registration → Contact → Referral → Transaction → Revenue**

This included working in Redshift to connect customer and referral activity with downstream outcomes.

One referral analysis examined nearly **13,000 first tour or agent requests** and found an approximately **11% referral-response rate**.

For customers captured through the referral lightbox, the analysis ultimately identified:

- **123 verified closed-client referrals**
- **12 resulting buy-side transactions**
- **$127,550 in generated revenue**
- **$10,629 average revenue per transaction**

A separate referral landing-page funnel showed:

**2,086 views → 200 registrations → 33 contacts → 9 transactions**

Those nine transactions generated approximately **$79,279 in revenue**, or **$8,808 per transaction**.

The important shift was treating referral activity as a measurable product funnel rather than simply a marketing channel.

## Turning Analysis Into Product Recommendations

The referral analysis also exposed a product problem: reliably identifying the relationship between the person referring a customer and the eventual customer was unnecessarily difficult.

I proposed several changes to make that relationship easier to capture and measure:

- Improve identifying information collected through the referral experience
- Expand Advanced Customer Profile data
- Semi-automate referral matching using text matching
- Create unique referral links that could persist attribution through the customer journey

I discussed implementation with engineering and scoped an initial version of the referral-link concept at roughly **3–4 development days**.

This was an early example of a pattern that would recur throughout my career:

**instrument the system → identify friction → quantify the opportunity → design a mechanism → partner with engineering → measure the result**

## Experimentation at Scale

I also designed and analyzed customer lifecycle experiments using large treatment and control populations.

One listing-recommendation experiment included:

- **152,448 experiment users**
- **29,999 control users**

Over the first 21 days, contact conversion increased from:

**0.79% → 0.93%**

That translated to approximately **215 incremental customer contacts** during the first three weeks.

Another long-term re-engagement experiment increased re-engagement from:

**4.33% → 5.95%**

with **98.5% statistical confidence**.

A CMA-focused reactivation experiment produced:

**1.75% brokerage re-engagement vs. 0.24% in control**

These experiments helped move lifecycle marketing away from engagement metrics alone and toward measurable customer behavior.

## Finding Growth Opportunities in Social

Social acquisition was another area where I combined channel analysis with experimentation.

During this period:

- Social referrals increased **75%**
- Social's share of Redfin traffic increased **53%**
- Social sessions exceeded the Q3 goal by **48%**
- Year-end performance was projected to exceed goal by **35%**

But I was more interested in whether that traffic could produce actual business outcomes.

One paid listing experiment generated:

| Metric | Result |
| --- | ---: |
| Spend | $5,308 |
| Visits | 28,972 |
| Contacts | 32 |
| Deals | 5 |
| Projected margin | $16,657 |
| Projected profit | $11,349 |

That worked out to approximately **$1,061 in spend per resulting deal**.

The internal characterization of the experiment was simple:

**Low volume, high yield.**

## What I Learned

This work changed how I thought about analytics.

The useful question was rarely:

> "Did the metric go up?"

It was:

> "What customer behavior changed, why did it change, what economic outcome did it create, and what should we change in the product because of it?"

That distinction became foundational to my later work.

At Galvanize, I built analytics infrastructure and experimentation systems.

At Prime Video, I built BI products and operational decision mechanisms.

At Nike, I led data products that turned demand, inventory, location, and time signals into automated supply-chain decisions.

The scale and domains changed.

The underlying product approach did not.

## Outcome

The Redfin work demonstrated an early version of the product discipline I would continue developing throughout my career:

**behavioral data + experimentation + economic measurement + product mechanisms**

Instead of treating analytics as reporting, I used it to understand customer behavior, quantify opportunities, and recommend what the business should build or change next.

---

*This case study is reconstructed from my contemporaneous analyses, presentations, and working materials. Metrics are aggregated and the case has been sanitized to exclude proprietary data, customer information, internal code, and confidential implementation details.*
