# 📺 Prime Video — Turning Operational Complexity Into Self-Service Products

**Self-Service Product · Technical Product Management · Operational UX · Analytics · Product Strategy · Scale**

> This case study describes my work using only generalized, non-confidential information. Proprietary architecture, internal systems, datasets, workflows, screenshots, metrics, and implementation details have intentionally been omitted.

## The Context

Prime Video operates at a scale where a seemingly simple customer expectation—

**“This title should be available to watch.”**

—can depend on a complicated set of processes happening behind the scenes.

As the catalog and business grew, so did the operational complexity.

Teams responsible for getting content ready for customers often needed to understand questions like:

- Is this title ready?
- If not, what is missing?
- Where does the issue appear to be?
- Who needs to act?
- Which problems are urgent?
- Is this one isolated issue or part of a larger pattern?

Answering those questions often required pulling information together from multiple places or asking a specialist to investigate.

I worked on turning that operational problem into a self-service product problem.

---

## The Problem

The problem was not a lack of data.

There was plenty of data.

The problem was that the information people needed to make a decision was fragmented across different systems, workflows, and operational processes.

That creates a very different kind of bottleneck.

A user might know:

**“This content isn't available when I expect it to be.”**

But getting from that observation to:

**“I understand what's wrong and what needs to happen next.”**

could require significant investigation.

When every investigation depends on an analyst or specialist, the expert becomes part of the workflow.

That works at small scale.

It becomes much harder as the business grows.

---

## The Product Question

I started thinking about the problem as:

**How do we give the people closest to the operational problem enough visibility and context to investigate it themselves?**

That is different from asking:

**“What dashboard should we build?”**

A dashboard gives someone information.

A self-service product helps someone complete a job.

The job here was closer to:

**Find the problem → understand its status → determine what needs attention → take the next action.**

---

## Example: Investigating Content Availability

A recurring operational question was why a title wasn't available when or where it was expected to be.

From the user's perspective, the question sounds simple:

**“Why isn't this live?”**

But answering it could require understanding several pieces of information about the title and its current state.

The old workflow could look something like:

**Availability issue → operations asks a specialist → specialist investigates → context is assembled → operations acts**

I worked on self-service reporting and operational products that moved more of that investigation directly into the hands of operations teams.

The target workflow became:

**Availability issue → operations investigates → likely problem becomes visible → operations acts**

The important product decision was not simply displaying more information.

It was identifying which information helped someone answer:

- What is the current state?
- What appears to be incomplete?
- Is action required?
- How urgent is it?
- What should I investigate next?

That is what turns analytics into a product.

---

## Product Principle: Organize Around the Decision

It is very easy for internal tools to mirror the systems underneath them.

System A owns one piece of data.

System B owns another.

System C contains something else.

But the user does not care which system owns the information.

They care about completing their job.

So the useful product view was not:

**“Here is everything System A knows.”**

It was closer to:

**“Here is what you need to understand about this title.”**

That shift—from system-oriented information to task-oriented information—is one of the most important lessons I took from the work.

---

## Product Principle: Turn Repeated Investigations Into Capabilities

Recurring analytical questions are often product discovery in disguise.

If an expert repeatedly has to answer variations of:

**“What's happening with this title?”**

the opportunity isn't necessarily to make the expert answer faster.

It may be to turn the investigation into a reusable capability.

The workflow moves from:

**Question → analyst → investigation → answer**

toward:

**Question → product → investigation → action**

That creates leverage on both sides.

Operations teams gain more independence.

Specialists get more time to work on problems that actually require specialist judgment.

---

## Product Principle: Prioritize Exceptions, Not Everything

At scale, not every item deserves equal human attention.

One of the most important product ideas was helping operators distinguish between:

**things progressing normally**

and

**things that may require intervention.**

That meant designing around exceptions and prioritization rather than asking humans to manually inspect everything.

The product should help answer:

**“What deserves my attention right now?”**

rather than:

**“Can I see every possible data point?”**

That distinction becomes increasingly important as operational volume grows.

---

## Product Principle: Build for Investigation, Not Just Monitoring

Monitoring tells someone that something happened.

Investigation helps them understand what to do about it.

For self-service tooling, I wanted users to be able to move from a high-level signal into progressively more specific context.

Conceptually:

**Portfolio view → problem area → individual title → relevant details → next action**

That creates an investigation path instead of a wall of metrics.

It also reduces the need to leave the product and manually piece together context elsewhere.

---

## Internal Users Are Still Customers

A major lesson from Prime Video was that internal products deserve the same customer thinking as external products.

Operations users have:

- jobs they're trying to complete;
- varying levels of technical expertise;
- repetitive workflows;
- time pressure;
- information overload;
- and frustrations with existing tools.

Giving them access to data does not automatically solve their problem.

You still have to understand:

**What are they trying to decide?**

**What information do they need at that moment?**

**What can the product remove from their workflow?**

That is product discovery, even when the customer works for the same company.

---

## Using Data to Challenge the Original Question

Analytics was valuable not only because it could answer operational questions.

It could also reveal that the original question was framed incorrectly.

Sometimes:

**“Why did this happen?”**

became:

**“Why does a human need to investigate this every time?”**

Or:

**“Can we make this report faster?”**

became:

**“Why does this process require a report at all?”**

I regularly used data to identify root causes, challenge assumptions, and turn ambiguous operational problems into clearer product priorities.

That is the part of analytics work that has always interested me most:

**using data to decide what should change.**

---

## From Hands-On Builder to Product Leader

My role at Prime Video evolved over time.

I started as a Senior BI Engineer doing hands-on analytical and product work.

I was later promoted into analytics management.

My scope expanded to leading a cross-functional team that included:

- product managers;
- program managers;
- data scientists;
- data engineers;
- and developers.

The team supported Prime Video's digital supply chain and its first expansion into live sports.

That changed the way I had to operate.

The question was no longer:

**“Can I solve this problem?”**

It became:

**“Can I create the priorities, systems, and context that allow a team to solve many problems without me?”**

---

## Scaling Through Systems Instead of Heroics

One of the themes running through the work was reducing dependence on individual experts.

That applied both to our users and to my own team.

For users:

**Build products that let them answer more questions themselves.**

For teams:

**Build mechanisms that make priorities, ownership, and decisions clearer.**

The more successful the system becomes, the less often someone should need to find the one person who “knows how everything works.”

That idea has shaped how I think about product leadership ever since.

---

## What I Measured

For self-service internal products, usage alone isn't enough.

The more interesting questions are behavioral:

- Are users able to complete investigations independently?
- Are fewer recurring questions being routed to specialists?
- Can teams identify issues earlier?
- Is time-to-understanding improving?
- Are users focusing their attention on the problems that actually require intervention?
- Is the product replacing manual work rather than creating another layer of it?

I think of success as **increased decision-making capability**, not simply dashboard adoption.

---

## What I'd Do Today

The central product strategy would remain the same.

I would still start with the user's investigative workflow rather than the available data.

But today I would prototype the experience much faster.

AI-assisted development makes it possible to move quickly from:

**workflow observation → proposed interaction → working prototype → user feedback**

before investing heavily in the final implementation.

I would also make product instrumentation part of the experience from the beginning so we could measure:

- where investigations start;
- where users get stuck;
- which paths resolve problems;
- where they leave the self-service experience;
- and which questions still require expert help.

Those unresolved questions are themselves a product backlog.

---

## What This Taught Me

Prime Video changed how I think about self-service products.

**Self-service isn't primarily about giving users access to information.**

It's about moving capability closer to the person who needs it.

A successful self-service product changes the organization from:

**“I need someone to answer this for me.”**

to:

**“I know how to figure this out.”**

And the best version goes one step further:

**“The product already knows what deserves my attention.”**

That principle has followed me into every data product, internal tool, and operational system I've worked on since.

---

## My Role

**Prime Video / Amazon — Senior BI Engineer → Analytics Manager**

My work included:

- self-service product development;
- operational analytics;
- problem discovery;
- product requirements;
- prioritization;
- data-driven root-cause analysis;
- stakeholder discovery;
- cross-functional leadership;
- team leadership;
- and scalable decision systems.

I later led product managers, program managers, data scientists, data engineers, and developers supporting Prime Video's digital supply chain and expansion into live sports.

---

## Confidentiality

The underlying work was completed inside Amazon and involved proprietary systems and operational processes.

This case study intentionally does **not** include:

- original internal documents;
- screenshots;
- system or tool names;
- architecture diagrams;
- proprietary workflows;
- internal operating metrics;
- partner information;
- unreleased product details;
- or non-public implementation specifics.

The case study focuses only on the product problem, my approach, the generalized capabilities I worked on, and the lessons I carried forward