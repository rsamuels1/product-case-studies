# 👟 Nike — Building an Automated Replenishment System for a DTC Supply Chain

**Product Strategy · Forecasting · Optimization · Automation · Supply Chain · Data Products · Global Scale**

## Context

When I joined Nike in May 2020, the company was in the middle of a major shift toward direct-to-consumer commerce.

The original transformation had been expected to happen over several years.

COVID changed the timeline almost overnight.

As consumer demand shifted rapidly toward Nike.com, the supply chain needed to support a much larger direct-to-consumer business without simply shipping every individual order from a small number of major distribution centers across the country.

I had been hired to build a replenishment optimization product to support that future state.

By the time I arrived, the future state was already here.

There was no existing product, mature team, or established roadmap—just an early hypothesis about what might be needed, an intern assigned to help, and a problem that suddenly needed to be solved much faster.

## The Problem

Direct-to-consumer growth created a deceptively simple logistics problem:

**How do we put the right products closer to consumers before they order them?**

Shipping individual orders long distances from major distribution centers was expensive and could increase delivery time.

Regional service centers offered another model.

Instead of waiting for a customer to order a pair of shoes and then shipping that individual pair across the country, Nike could move inventory in bulk from major distribution centers to regional facilities closer to anticipated demand.

Then, when the customer actually ordered the product, it would already be nearby.

That created a much harder product question:

> **Before an order exists, how do we decide which SKUs should be moved, how many units should move, where they should come from, and which regional facility should receive them?**

Getting that wrong had real costs.

Move too little inventory and customers would still be served from distant distribution centers.

Move too much—or move the wrong products—and inventory could sit unused at regional facilities.

The product therefore needed to predict demand well enough to make physical inventory decisions before customers made purchases.

## Start With the Entire Supply Chain

Before designing the product, I needed to understand how inventory actually moved through Nike.

I talked with people across the global supply chain, shadowed inventory planners, analyzed existing workflows, and built reporting to understand where consumer orders were being fulfilled from versus where they potentially could have been fulfilled.

The underlying data was fragmented.

To understand whether a product should move, we needed to connect information including:

- historical consumer demand
- Nike.com behavior
- current inventory positions
- product and SKU attributes
- seasonality and promotions
- geographic demand
- inventory ordered from manufacturers
- expected arrival timing
- distribution-center inventory
- regional-service-center inventory
- retail-store inventory
- product availability on Nike.com
- lead times and supply constraints

The challenge wasn't simply forecasting demand.

It was creating a sufficiently complete picture of **demand + availability + location + time** to make a physical inventory decision.

## Build a Forecast for the Decision We Actually Needed to Make

Nike already had many forecasting teams and forecasting systems.

That created one of the hardest organizational problems of the project.

The natural question was:

> **Why does Nike need another forecast?**

Rather than assume an existing model would work, we evaluated the forecasts already available and the decisions they had been designed to support.

None exactly matched our use case.

Our product needed a forecast specifically suited to predicting near-term consumer demand at the level required to decide which inventory should be positioned closer to consumers.

We borrowed useful inputs and thinking from existing forecasting work, but built a demand model around the replenishment decision itself.

That distinction mattered.

**The goal wasn't to build the most universally correct forecast. It was to build the forecast that best supported this particular decision.**

That also meant earning trust.

Forecasting was a mature and highly scrutinized discipline inside Nike, and teams understandably challenged whether a new model was necessary.

We had to demonstrate through performance that ours was better suited to this specific operational use case.

## V1: Put the Decision in Front of a Human

We didn't begin with a fully automated global system.

The first version was much simpler.

We built a dashboard for inventory planners supporting the first regional service center.

The product generated the information planners needed to determine what inventory should move. Planners reviewed that output and manually assembled the "shopping lists" used to load trucks.

Conceptually:

**Demand forecast → inventory availability → planner recommendation → truck load → regional service center**

This gave us something extremely valuable before investing in full automation:

**a way to test whether the underlying decision was actually good.**

## Measure the Inventory After We Move It

A forecast alone wasn't enough to tell us whether the product worked.

We needed to measure what happened to the physical inventory after our recommendation.

One of our most important measures was how long inventory remained at a regional service center before a consumer ordered it.

If products consistently moved through the facility quickly, we were positioning useful inventory closer to real demand.

If products sat too long, we had moved inventory that wasn't needed.

By the mature version of the product, approximately **97% of positioned inventory met our target window for consumer demand**, with roughly 3% aging beyond that threshold and becoming "stale" inventory that needed to be handled through other channels or opportunities.

That created a direct feedback signal for improving the system.

## From Decision Support to Automated Decision-Making

Once the pilot demonstrated that the approach worked, we received funding to build the team, integrate the product into existing supply-chain systems, and expand the model.

We gradually removed manual steps.

The dashboard became components.

Components became services.

The forecast became an input to a replenishment engine.

We built an API that could send replenishment decisions downstream into the systems responsible for moving inventory.

Eventually, the process became automated.

Every morning before trucks were loaded, the system could determine:

- which SKUs should move
- how many units should move
- which distribution center should supply them
- which regional service center should receive them

The output flowed into the operational systems responsible for loading and routing inventory.

The product had evolved from:

**"Here is information a planner can use to make a decision."**

to:

**"Here is the decision."**

Humans increasingly managed the system through performance targets and operating parameters rather than manually creating individual replenishment orders.

## Build the Feedback Loop

Automation didn't mean setting the algorithm once and walking away.

We created standardized metrics across regional service centers so we could understand both the decisions the system made and their downstream consequences.

Those included measures such as:

- inventory the algorithm wanted but couldn't obtain
- time inventory spent at a regional service center before consumer purchase
- fulfillment and shipping time through regional facilities
- shipping time for orders that still had to be fulfilled through major distribution centers
- differences between regions and facilities

Those metrics gave us levers for changing the product.

If a region needed faster delivery, we could adjust the system toward that goal.

Around periods such as the holidays, we could change timing and inventory-positioning behavior to prepare earlier for expected demand.

The product became a continuous decision system rather than a static forecast.

## Scale the System Across Geographies

We began with a single regional service center.

From there, the system expanded across North America, eventually supporting multiple regional facilities across the United States.

We also expanded into Europe.

Global expansion wasn't simply a matter of copying the US implementation.

Regional infrastructure, operational requirements, and external conditions differed.

At one point, plans for a UK deployment were disrupted around Brexit, requiring us to adjust the rollout strategy and support a different European location.

China presented another challenge entirely.

Its underlying systems were sufficiently different that the US/European implementation couldn't simply be plugged in. Instead, the China team adapted the model and approach for its environment.

That reinforced an important lesson:

**Global product strategy doesn't necessarily mean identical implementation.**

The product needs a common decision framework while allowing regional systems and constraints to shape how that framework gets implemented.

## Expand Beyond Ecommerce

The regional network initially solved a direct-to-consumer fulfillment problem.

But once inventory was positioned intelligently throughout the network, the same infrastructure could support more than Nike.com orders.

Retail stores could also be replenished from regional service centers.

What began as a response to rapidly changing ecommerce demand became a broader capability for positioning inventory across Nike's distribution network.

## Connect Product Performance to Business Performance

This product didn't necessarily create demand for Nike products.

That made measuring its value more interesting.

Its value came from enabling Nike to support growing direct-to-consumer demand **more efficiently**.

We compared outcomes such as:

- fulfillment through regional service centers versus major distribution centers
- shipping costs
- delivery times
- inventory utilization
- stale inventory
- consumer delivery experience

That allowed us to translate supply-chain performance into financial impact.

By the time I left Nike, the product was delivering **meaningful, measurable quarterly EBITDA impact** through lower fulfillment costs and a more efficient direct-to-consumer supply chain.

We also investigated second-order effects.

For example:

> **If getting an order to a customer faster improves their experience, does that change future purchasing behavior?**

Our analysis indicated that faster fulfillment was associated with increased repeat ordering.

That connected what initially looked like an internal supply-chain optimization problem back to the consumer experience.

## What Made This Hard

The technical system was only part of the challenge.

We were simultaneously dealing with:

**A compressed timeline.**  
A transformation expected to unfold over years suddenly needed to happen much faster.

**Forecast credibility.**  
Nike already had sophisticated forecasting teams. We needed to demonstrate why this particular decision required a forecast optimized for a different purpose.

**Fragmented inventory data.**  
Making a replenishment decision required connecting information across manufacturing, ports, distribution centers, regional facilities, retail stores, and digital availability.

**Stakeholder alignment.**  
Supply chain, planning, engineering, analytics, data science, finance, geography teams, and leadership all had different perspectives on the problem.

**Global variation.**  
A product that worked in one geography couldn't always be copied directly into another.

**Physical consequences.**  
This wasn't simply software displaying the wrong number. Our decisions caused actual products to be loaded onto actual trucks and moved to another location.

That made measurement, trust, and controlled rollout especially important.

## How My Role Evolved

I owned the product from early problem definition through global expansion.

My responsibilities included:

- product strategy and roadmap
- customer and stakeholder discovery
- workflow analysis
- requirements and prioritization
- demand-forecast product strategy
- data and metric definitions
- model requirements
- engineering and data-science partnership
- stakeholder alignment
- pilot design
- launch and adoption
- system integration
- global expansion
- performance measurement
- business-impact measurement

My direct team included data scientists and data analysts, while the broader product required close collaboration across engineering, data engineering, supply chain, planning, operations, finance, geography teams, leadership, and other product organizations.

The job changed significantly over time.

At the beginning, I was trying to answer:

> **Can we predict what inventory should be closer to the consumer?**

Eventually, I was managing a global decision system that automatically acted on that prediction.

## What I'd Do Today

The system already had the beginnings of a feedback loop:

**forecast → replenish → observe consumer demand → measure performance → adjust model**

But humans still played an important role in interpreting performance and deciding how different operating parameters should change.

With today's AI tooling, I'd explore closing more of that loop.

An intelligent control layer could continuously evaluate performance across regions, identify changing conditions, recommend or make bounded adjustments to operating parameters, and explain why those adjustments were being proposed.

I wouldn't remove human oversight from high-impact supply-chain decisions.

But I would reduce the amount of manual interpretation required to keep the system optimized as conditions change.

## What This Taught Me

This was my first product role centered on a physical rather than purely digital supply chain.

It changed how I think about product management.

A product doesn't have to end at a screen.

The "user" can be a planner, an API, an automated ordering system, a warehouse operation, or ultimately a truck being loaded with physical inventory.

It also taught me to think about business impact differently.

Our product didn't need to make someone buy another pair of shoes to create value.

Sometimes the product opportunity is:

> **The customer is already buying the shoe. How do we build a system that gets it to them faster and at dramatically lower cost?**

That combination of customer experience, operational efficiency, data, automation, and measurable financial impact became one of the most important product lessons of my career.

## Confidentiality

This case study describes my product approach and experience at a high level.

Internal system names, architecture, proprietary forecasting methodology, detailed operating parameters, datasets, and other confidential implementation details have intentionally been omitted.