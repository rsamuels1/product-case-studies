# 👟 Nike — Building a Global Inventory Replenishment Product

**Product Strategy · Forecasting · Optimization · Automation · Supply Chain · Global Scale**

> **From a planner dashboard to an automated decision system positioning inventory against predicted consumer demand.**

## At a Glance

**Role:** Product lead, Replenishment Optimization  
**Scope:** Owned the product from early problem definition and pilot through automation and global expansion, leading data science and analytics while partnering across engineering, supply chain, planning, operations, finance, and regional teams.  
**Product:** A forecasting and optimization system that determined which Nike inventory should move, how much should move, and where it should go before consumer orders occurred.  
**Scale:** Expanded from a single regional service center across North America and Europe, with the approach adapted for additional geographies.  
**Outcome:** Approximately **97% of positioned inventory met its target window for consumer demand**, while the product delivered **measurable quarterly EBITDA impact** through more efficient fulfillment.

---

## The Problem

When I joined Nike in May 2020, the company was in the middle of a major shift toward direct-to-consumer commerce.

That transformation had been expected to unfold over several years. COVID changed the timeline almost overnight.

As demand shifted rapidly toward Nike.com, the supply chain needed to support a much larger DTC business without shipping every individual order long distances from a small number of major distribution centers.

Regional service centers offered another model: move inventory in bulk closer to anticipated demand *before* a customer orders it.

That created the core product question:

> **Before an order exists, how do we decide which SKUs should move, how many units should move, where they should come from, and which regional facility should receive them?**

Getting that decision wrong had physical and financial consequences. Move too little and customers would still be served from distant distribution centers. Move too much — or move the wrong products — and inventory could sit unused.

There was no existing product, mature team, or established roadmap when I arrived. There was an early hypothesis, an intern assigned to help, and a problem that suddenly needed to be solved much faster.

---

## Discovery: Understand the Decision Before Building the Product

I started by shadowing inventory planners, talking with stakeholders across Nike's global supply chain, analyzing existing workflows, and building reporting to understand where consumer orders were being fulfilled versus where they potentially could have been fulfilled.

The decision required connecting fragmented signals across consumer demand, product attributes, inventory availability, geography, inbound supply, seasonality, and lead times.

The challenge wasn't simply forecasting demand.

It was creating a sufficiently complete picture of:

**demand + availability + location + time**

to make a physical inventory decision.

---

## Build the Forecast for the Decision We Actually Needed to Make

Nike already had sophisticated forecasting teams and systems.

That created an important product and organizational question:

> **Why does Nike need another forecast?**

Rather than assume an existing model would work, we evaluated available forecasts and the decisions they had been designed to support.

None exactly matched our use case.

We needed to predict near-term consumer demand at the level required to decide which physical inventory should be positioned closer to consumers. We borrowed useful inputs and thinking from existing forecasting work, but built the demand model around the replenishment decision itself.

**The goal wasn't to build the most universally correct forecast. It was to build the forecast that best supported this particular decision.**

That meant earning trust from teams with deep forecasting expertise and demonstrating through performance why this use case required a different approach.

---

## V1: Put the Decision in Front of a Human

We didn't start by automating the supply chain.

The first version was a dashboard for inventory planners supporting the first regional service center.

The system generated the information planners needed to decide what inventory should move. Planners reviewed the output and manually assembled the "shopping lists" used to load trucks.

The initial workflow looked roughly like this:

**Demand forecast → Inventory availability → Planner recommendation → Truck load → Regional service center**

Keeping a human in the loop gave us something extremely valuable before investing in full automation:

> **A way to test whether the underlying decision was actually good.**

### The Product Evolution

**V1 — Decision support**  
*"Here's the information you need."*

↓

**V2 — Recommendation engine**  
*"Here's what we think you should do."*

↓

**Mature product — Automated decision system**  
*"Here's the decision."*

---

## Measure What Happened to the Inventory

Forecast accuracy alone couldn't tell us whether the product worked.

We needed to measure what happened to the **physical inventory after we moved it**.

One of our most important measures was how long positioned inventory remained at a regional service center before a consumer ordered it.

If products consistently moved through the facility quickly, we were positioning useful inventory close to real demand.

If they sat too long, we had moved inventory that wasn't needed.

### ~97% of positioned inventory met its target demand window

By the mature version of the product, approximately **97% of positioned inventory met our target window for consumer demand**, with roughly 3% aging beyond the threshold and becoming stale inventory that needed to be handled through other channels or opportunities.

That created a direct feedback signal for improving the system.

---

## From Recommendation to Automation

Once the pilot demonstrated that the approach worked, we received funding to build the team, integrate the product into Nike's existing supply-chain systems, and expand it.

We gradually removed manual steps.

The dashboard became components. Components became services. The forecast became an input to a replenishment engine.

We built an API that could send replenishment decisions downstream into the systems responsible for moving inventory.

Eventually, every morning before trucks were loaded, the system could determine:

- which SKUs should move
- how many units should move
- which distribution center should supply them
- which regional service center should receive them

Those decisions flowed into the operational systems responsible for loading and routing inventory.

The product had evolved from:

> **"Here is information a planner can use to make a decision."**

to:

> **"Here is the decision."**

Humans increasingly managed the system through performance targets and operating parameters rather than manually creating individual replenishment orders.

---

## Build the Feedback Loop

Automation didn't mean setting the algorithm once and walking away.

We standardized performance metrics across regional service centers to understand both the decisions the system made and their downstream consequences.

The basic loop became:

**Predict → Move → Observe → Measure → Adjust**

That allowed us to tune the product as conditions changed. Different regions could have different operating needs, and periods such as the holidays could require earlier or different inventory-positioning behavior.

The result was a continuous decision system rather than a static forecast.

---

## Scale Globally

We began with a single regional service center and expanded across North America, eventually supporting multiple regional facilities across the United States.

We then expanded into Europe.

Global expansion wasn't simply a matter of copying the US implementation. Regional infrastructure and operating requirements differed, and China had sufficiently different underlying systems that the model and approach needed to be adapted for its environment.

That reinforced an important product lesson:

> **Global product strategy doesn't necessarily mean identical implementation.**

The product needed a common decision framework while allowing regional systems and constraints to shape how that framework was implemented.

The capability also expanded beyond its original Nike.com fulfillment use case. Once inventory was intelligently positioned throughout the regional network, the same infrastructure could support retail replenishment.

---

## Business Impact

This product didn't need to create additional demand for Nike products to create value.

Its job was to help Nike serve existing and growing direct-to-consumer demand **more efficiently**.

We connected operational performance — including fulfillment location, shipping costs, delivery time, inventory utilization, and stale inventory — to financial outcomes.

### Measurable quarterly EBITDA impact

By the time I left Nike, the product was delivering **meaningful, measurable quarterly EBITDA impact** through lower fulfillment costs and a more efficient direct-to-consumer supply chain.

We also investigated second-order consumer effects.

Our analysis indicated that faster fulfillment was associated with increased repeat ordering, connecting what initially looked like an internal supply-chain optimization problem back to the consumer experience.

---

## What Made This Hard

**Forecast credibility.**  
Nike already had sophisticated forecasting organizations. We needed to demonstrate why this operational decision required a forecast optimized for a different purpose.

**Cross-functional complexity.**  
The product crossed engineering, data science, analytics, supply chain, planning, operations, finance, regional teams, leadership, and other product organizations. Alignment was as important as the model itself.

**Physical consequences.**  
This wasn't software simply displaying the wrong number. Our decisions caused actual products to be loaded onto actual trucks and moved to another location.

That made measurement, trust, and controlled rollout especially important.

---

## My Role

I owned the product from early problem definition through global expansion.

I started with an intern, an undefined problem, and a hypothesis. Over four years, my role evolved into leading a global decision product spanning data science, analytics, engineering, planning, operations, finance, and regional supply-chain organizations.

My direct team included data scientists and data analysts, while the broader product required close partnership across Nike's technology and supply-chain organizations.

At the beginning, I was trying to answer:

> **Can we predict what inventory should be closer to the consumer?**

Eventually, I was managing a global decision system that automatically acted on that prediction.

---

## What I Learned

This product fundamentally changed how I think about product management.

**A product doesn't have to end at a screen.**

The user can be a planner, an API, an automated ordering system, a warehouse operation — or ultimately a truck being loaded with physical inventory.

It also changed how I think about business impact. A product doesn't always need to generate new demand to create enormous value.

Sometimes the opportunity is:

> **The customer is already buying the shoe. How do we build a system that gets it to them faster and at dramatically lower cost?**

That intersection of customer experience, operational efficiency, data, automation, and measurable financial impact became one of the most important product lessons of my career.

---

## Confidentiality

This case study describes my product approach and experience at a high level.

Internal system names, architecture, proprietary forecasting methodology, detailed operating parameters, datasets, and other confidential implementation details have intentionally been omitted.
