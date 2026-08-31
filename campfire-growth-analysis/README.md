# 🛒 Campfire — Finding the Growth Levers in an Ecommerce Funnel

**Conversion Analysis · Funnel Diagnosis · Experimentation · Growth Strategy**

> *Completed as part of an interview process that resulted in an offer. The original dataset and company-specific materials are not published; this case study focuses on my approach, reasoning, and recommendations.*

## The Context

I was given an unfamiliar ecommerce dataset and asked to answer five questions:

- Which traffic sources perform best?
- Where does the checkout funnel appear to be breaking?
- Are there seasonal trends worth acting on?
- Which pages are most effective?
- What else could the company learn from the data to improve performance?

The challenge was not simply to produce charts.

It was to turn a limited dataset into a useful growth recommendation.

## The Problem

A funnel can look healthy at the top and still fail badly closer to purchase.

So I approached the analysis as a sequence:

**Traffic source → landing experience → engagement → checkout → purchase**

The goal was to understand not just where users were coming from, but which combinations of source and experience were actually producing the best downstream behavior.

## How I Approached It

### Start with conversion, not traffic volume

The largest traffic source is not necessarily the best one.

I compared visits by source with purchase conversion rather than assuming volume was a proxy for value.

That immediately surfaced an important distinction:

**Affiliate and Organic Search were the highest-converting sources, even though other channels generated more total traffic.**

I also noted that a truly complete channel decision would require cost and revenue data, which were not available in the dataset. Samuelson_Campfire.pdf

### Follow the customer further down the funnel

Next, I looked at cart abandonment by traffic source and country.

The abandonment problem was not isolated to one small segment.

Paid Social and Paid Display both had abandonment rates above 90%, and abandonment was high enough across the broader dataset that I recommended qualitative research rather than assuming the analytics alone explained the problem. Samuelson_Campfire.pdf

That led to an important next step:

**Use the quantitative data to locate the problem, then use user research to understand why it exists.**

## What I Found

### Organic Search looked especially promising

Affiliate converted very well, but Organic Search combined strong conversion with lower cart abandonment.

That made Organic particularly interesting as a growth opportunity rather than simply optimizing for whichever channel had the highest raw conversion rate. Samuelson_Campfire.pdf

### The checkout experience deserved investigation

High abandonment showed up across the funnel rather than only in one market or channel.

My recommendation was to conduct remote and in-person user testing—or deeper behavioral analysis—to understand the usability issues behind that drop-off. Samuelson_Campfire.pdf

### Page type mattered

I went beyond comparing individual URLs.

I split the original page field into:

- `page_type`
- `page_number`

That let me evaluate both individual page performance and the effectiveness of entire page templates.

It created two useful levels of decision-making:

**Which specific pages work?**

and

**Which kinds of pages work?**

Product Detail Pages emerged as particularly strong: they had the highest conversion rate, the lowest bounce rate, and average cart abandonment, especially when reached through Organic Search. Samuelson_Campfire.pdf

That was more actionable than simply saying one individual page happened to perform well.

## From Analysis to Experiments

I turned the findings into a small testing roadmap.

### 1. Grow Organic Search

If Organic traffic is both converting well and abandoning less frequently, increasing qualified organic traffic could be more valuable than simply increasing traffic overall.

My recommendation was to improve SEO around the strongest-performing Product Detail Pages.

### 2. Route more Affiliate traffic to Product Detail Pages

Affiliate traffic converted well, while Product Detail Pages performed well as landing experiences.

That suggested a straightforward hypothesis:

**Would Affiliate traffic perform even better if more of it landed directly on Product Detail Pages?**

I recommended testing that rather than treating current routing as fixed. Samuelson_Campfire.pdf

### 3. Test retargeting against stronger landing experiences

I recommended a small retargeting test focused on Product Detail Pages rather than broadly sending paid users back into the site. Samuelson_Campfire.pdf

### 4. Question paid traffic to the homepage

Paid Display and Paid Social traffic sent to the homepage showed very high cart abandonment.

Without spend data, I could not determine the exact economic impact.

But the pattern was strong enough to question the experience:

**Why pay to acquire a specific audience, then send them to a generic homepage?**

I recommended testing more relevant landing experiences based on what those users were expected to purchase. Samuelson_Campfire.pdf

## What the Data Couldn’t Tell Me

This was an important part of the analysis.

### Channel profitability

Conversion rate alone cannot tell you which channel deserves the most budget.

To make that decision confidently, I would want:

- acquisition cost;
- revenue;
- average order value;
- contribution margin;
- and ideally customer lifetime value.

The original analysis explicitly called out the absence of cost and revenue data rather than pretending conversion rate answered the full business question. Samuelson_Campfire.pdf

### Why users abandoned

The funnel could show me **where** users were dropping.

It could not tell me **why**.

That is why the next recommendation was user testing and behavioral research rather than another dashboard.

### Seasonality

The available dataset was not sufficient to make a credible seasonal claim.

So I didn't make one. Samuelson_Campfire.pdf

That may be the least exciting finding in the project, but I think it is an important analytical principle:

**“I don't know yet” is better than manufacturing a pattern from insufficient data.**

## How I Prioritized

I would not treat every finding as equally valuable.

My prioritization logic was roughly:

**Strong signal + plausible business value + inexpensive test = test sooner**

That pushed these toward the front:

1. SEO improvements on high-performing Product Detail Pages
2. Affiliate → Product Detail Page routing test
3. Small retargeting experiment
4. User research around checkout abandonment
5. Review of paid traffic landing-page strategy

The purpose of the analysis was not to deliver a giant list of ideas.

It was to identify the smallest set of actions most likely to teach us something useful.

## What I’d Do Today

I would approach the same exercise with the same basic logic, but with better instrumentation.

I would want to connect:

**Acquisition → landing page → product interaction → checkout behavior → purchase → repeat behavior**

I would also segment by:

- new vs. returning customer;
- device;
- campaign intent;
- product category;
- customer cohort;
- and possibly geography where volume supports it.

For the checkout issue, I would combine funnel analysis with session-level behavior and direct customer research much earlier.

And I would formalize each recommendation into an experiment brief:

**Observation → hypothesis → target segment → change → primary metric → guardrail metric → decision rule**

The tooling has changed.

The underlying growth question hasn't:

**Where is the customer getting stuck, and what is the cheapest credible way to learn whether changing that experience helps?**

## Outcome

This analysis was completed as part of an interview process and resulted in an offer.

I include it because it demonstrates a part of product work I still use frequently:

**enter an unfamiliar problem, identify the signal quickly, separate evidence from assumption, and turn the result into an actionable testing plan.**

## Confidentiality Note

The original interview dataset and company-specific materials are not included here.

This case study reconstructs my analytical approach and recommendations from my own work while avoiding publication of source data or materials supplied during the interview process.