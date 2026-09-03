# 🏙️ WISP — Using Housing Data to Prioritize Affordable-Housing Investment

**Decision Modeling · Geospatial Analysis · Public Data · Resource Allocation · Housing**

> A time-boxed interview case where I used Philadelphia property data to build a decision model for prioritizing vacant-property redevelopment — and the work ultimately resulted in an offer.

## At a Glance

**Context:** Interview case  
**Domain:** Affordable housing / urban development  
**Scope:** Exploratory analysis, feature selection, geospatial analysis, multi-criteria decision modeling, cost modeling, prioritization  
**Outcome:** The interview process resulted in an offer

The prompt centered on a hypothetical public investment in affordable housing.

The practical question was:

> **If Philadelphia had a fixed budget for affordable-housing development, which vacant properties should it prioritize?**

I was given a large Philadelphia property dataset and a limited amount of time to turn it into a defensible recommendation.

Rather than treating the exercise as a pure prediction problem, I framed it as a **resource-allocation decision**:

**Which properties appear to offer the strongest redevelopment opportunity, and how far could a fixed budget go?**

---

## The Problem

Philadelphia has a significant affordable-housing shortage, but available public funding is finite.

At the same time, the city has thousands of vacant or underutilized properties with very different characteristics:

- location
- market value
- parcel shape
- property condition
- land value
- zoning context
- topography
- surrounding neighborhood economics

Simply choosing the cheapest properties would ignore redevelopment potential.

Choosing the properties with the highest expected market value would risk concentrating investment in already-expensive neighborhoods.

So the harder problem was:

> **How do you turn a broad policy goal into a transparent decision framework that balances cost, redevelopment potential, and neighborhood context?**

---

## Start With the Decision, Not the Model

My first instinct was to explore whether I could build a more traditional predictive model.

I initially attempted a hedonic model to estimate property value using property characteristics.

But this was a time-boxed interview exercise, and I realized I would not have enough time to build, validate, and explain that model to a standard I was comfortable defending.

So I changed approaches.

Instead of forcing a more sophisticated model into the available time, I built a **multi-criteria decision model**.

That let me focus on the actual question:

> **Which properties should be prioritized?**

The important shift was from:

**“Can I predict property value?”**

to:

**“Can I build a reasonable, explainable ranking that supports a real allocation decision?”**

---

## Explore the Property Market First

Before scoring vacant properties, I explored the broader residential dataset to understand which property characteristics appeared associated with market value.

I investigated variables including:

- property type
- location
- zip code
- tree coverage
- basement type
- central air
- interior and exterior condition
- rooms, bedrooms, and bathrooms
- fuel type
- garage type
- parcel shape
- topography
- view type
- fireplaces
- quality grade
- taxable land value

That analysis surfaced several useful patterns.

For example, higher-value residential properties were concentrated in areas like Center City and Chestnut Hill. Multifamily properties generally skewed higher in market value. Properties near parks or green space also tended to have higher median values.

The purpose wasn't to prove causation.

It was to identify which attributes were potentially useful signals when evaluating vacant properties for redevelopment.

---

## Narrow the Model to Decision-Relevant Features

I then focused specifically on vacant properties and selected a smaller set of attributes that seemed useful for redevelopment prioritization.

The model included factors such as:

- market value
- taxable land value
- quality grade
- zip code
- parcel shape
- topography
- view type
- property condition

Each attribute was transformed into a usable score, normalized, and assigned a weight.

The final weighted model emphasized:

- taxable land value
- quality grade
- neighborhood economics
- physical feasibility
- redevelopment potential

This created a single **performance score** for each candidate property.

The score wasn't intended to be a perfect prediction of future value.

It was a transparent way to rank properties against the goals of the exercise.

---

## A Model Isn't Neutral

One of the most important judgment calls was how to treat neighborhood value.

If I simply rewarded properties located in the highest-value zip codes, the model would naturally prioritize areas where real estate was already expensive.

That would conflict with the affordable-housing objective.

So I treated zip-code value as a **non-beneficial attribute**:

Properties in lower-median-value areas received a higher redevelopment-priority score.

That was a deliberate choice.

> **The objective you choose determines what the model considers “good.”**

A technically correct optimization can still produce the wrong outcome if the scoring function rewards the wrong thing.

For me, this was the most important lesson in the exercise.

The model should reflect the decision we actually want to make — not simply maximize whatever variable is easiest to predict.

---

## Build an Illustrative Cost Model

A ranked list alone wasn't enough.

The next question was:

> **How many of these properties could actually be developed within the available budget?**

I built a simplified cost model using each property's market value and performance score to estimate:

- purchase cost
- redevelopment cost
- total project cost
- estimated housing-unit capacity

I then ranked the candidate properties by performance score and selected them until the hypothetical budget was exhausted.

The model produced an illustrative scenario of:

### 214 candidate properties

with approximately:

### $65.1M in estimated purchase costs

and:

### $234.3M in estimated development costs

for a total of approximately:

### $299.4M

The scenario produced an estimated:

# ~2,197 affordable-housing units

within the hypothetical $300M budget.

Those figures were **model outputs, not forecasts**.

The cost assumptions were intentionally simplified for the time available, and I explicitly documented where the model would need additional validation before being used for a real investment decision.

---

## Make the Tradeoffs Visible

A useful model shouldn't hide uncertainty.

I documented several limitations and next steps rather than presenting the output as more precise than it was.

The most important improvements would include:

- replacing the multi-criteria model with a better-validated hedonic or other predictive model where appropriate
- using cross-validation and regression to improve parameter selection
- improving estimates of redevelopment cost
- building more accurate multifamily unit-capacity estimates
- adding crime and neighborhood-vulnerability data
- incorporating redevelopment ROI
- distinguishing between affordable rental development and affordable homeownership opportunities

I also identified potential complementary investments such as tree coverage and bike infrastructure, because the exploratory analysis suggested broader neighborhood conditions might matter alongside the individual property.

The point wasn't that every idea belonged in the final model.

It was to show what evidence I would want next before increasing confidence in the recommendation.

---

## The Result

The final recommendation was a prioritized portfolio of vacant Philadelphia properties that fit within a hypothetical $300M affordable-housing investment.

The model suggested that approximately 214 selected properties could support an illustrative estimate of roughly 2,200 affordable-housing units under the assumptions used in the exercise.

More important than the exact number, the work turned an ambiguous policy question into a repeatable decision process:

**Define the objective**

↓

**Explore the available evidence**

↓

**Choose decision-relevant attributes**

↓

**Make the tradeoffs explicit**

↓

**Score and prioritize opportunities**

↓

**Apply budget constraints**

↓

**Produce an actionable recommendation**

The interview process ultimately resulted in an **offer**.

---

## What I Actually Demonstrated

Although the output was a housing-development proposal, the deeper product skills were more general.

### 1. Turning ambiguity into a decision

The original problem was broad.

I translated it into a specific question that a model could support.

### 2. Knowing when to simplify

I abandoned a more sophisticated modeling approach when I realized I couldn't validate it adequately within the interview timeframe.

A simpler model I could explain and defend was more useful than a technically impressive model I couldn't trust.

### 3. Designing the objective carefully

The zip-code treatment forced an important question:

> Are we optimizing predicted value, or are we optimizing the actual policy goal?

That distinction applies to recommendation systems, ranking systems, AI products, marketplaces, supply-chain optimization, and many other data products.

### 4. Connecting analysis to constraints

The exercise didn't end with an interesting correlation.

I translated the ranking into a budget-constrained investment scenario.

### 5. Communicating uncertainty

I separated model output from real-world forecast and documented where stronger data and validation would be required.

---

## What I Learned

The most useful lesson from this case wasn't about Philadelphia real estate.

It was about optimization.

A model can be mathematically correct and still recommend the wrong thing.

Everything depends on what you've told it to optimize.

That means the product work starts before the model:

- define the decision
- understand who benefits
- identify the constraints
- choose the objective
- understand the tradeoffs
- make the assumptions visible

Only then should you optimize.

> **The quality of a decision system depends as much on the question it is asked to answer as on the sophistication of the model underneath it.**

That principle has continued to shape how I think about forecasting, ranking, recommendations, experimentation, and AI-enabled decision products.

---

## Why This Case Is Here

This was an interview project rather than a shipped production system.

I include it because it demonstrates a different part of my product toolkit than my other case studies:

- housing and geospatial data
- exploratory modeling
- explicit objective design
- resource allocation
- cost-constrained prioritization
- decision science
- knowing when a simpler model is the better product choice

It also shows how I approach an unfamiliar domain under time pressure:

**learn quickly, make the assumptions explicit, find the signal, build something usable, and be clear about what I would improve next.**

The work resulted in an offer, which gave me an external signal that the approach was useful and persuasive.

---

## Confidentiality & Context

This case study is based on an interview exercise using public or provided Philadelphia property data.

The $300M investment scenario was hypothetical.

Model outputs, redevelopment costs, property availability, development feasibility, and estimated unit counts were based on simplifying assumptions made for the interview and should not be interpreted as real-world forecasts or policy recommendations.

The portfolio version focuses on the analytical and product decision-making process rather than advocating for any particular public-budget allocation.
