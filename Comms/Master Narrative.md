# realfast — Master Narrative

*v0.4 — February 2026. Living document.*

---

## The Governing Question

What does an IT services firm need to look like in three years to survive?

This document lays out our thesis on why the current model is breaking, what replaces it, and where realfast sits. It is not a pitch. It is the reasoning underneath every pitch. Two audiences read different implications from the same argument: investors see the scale opportunity; customers see the operational urgency.

---

## Part 1: The Structural Problem

### 1.1 Revenue Per Employee Has Not Moved

The IT services industry runs on a linear growth model: more revenue requires proportionally more people. This has been true for a decade.

| Company | RPE (FY2015) | RPE (FY2023) | Change |
|---|---|---|---|
| Infosys | $49,442 | $53,060 | +7.3% over 8 years |
| TCS | ~$50,700 | ~$47,000 | Flat to negative |
| Wipro | ~$48,000 | ~$45,100 | Declining |
| HCLTech | ~$65,000 | ~$61,400 | Declining |

Sources: Bullfincher, StockAnalysis, Pathfinders Training, Communications Today.

TCS is the clearest illustration. Revenue nearly doubled from $16B to $30B over the decade. Headcount also nearly doubled, from ~319,000 to ~608,000. The ratio did not change. At ~$50K RPE, every additional million dollars of revenue requires approximately 20 new employees. This is arithmetic, not opinion.

When RPE does tick up — as it did for Infosys in FY24-FY25 — it is driven by headcount reduction, not structural improvement. The top five Indian IT firms shed ~57,900 employees in a two-year period. RPE rose. They will rehire when deals return. RPE will revert.

### 1.2 The Safety Net Is Gone

IT services firms historically absorbed delivery risk through bench strength — idle employees who could be thrown at projects when they slipped. This buffer has been systematically eliminated.

Bench as a percentage of headcount has dropped from 10-15% to 2-5% across the industry. TCS introduced a 35-day bench rule: unassigned engineers are retrained or exited. Utilization rates have converged at 83-86%, up from 70-75% during peak hiring periods.

Sources: Trak.in, Economic Times, NiftyTrader.

Every project now has to hit its time-to-value target with less margin for error and fewer spare people to deploy when things go wrong.

### 1.3 Deal Structures Are Under Pressure

*This section is hypothesis. No firm will publicly state that their deal sizes are shrinking. The following is based on observable signals and private conversations.*

The model that sustained IT services — large contracts, long durations, infrequent renegotiation — was designed for a world where switching costs were high and alternatives were scarce. Three forces are compressing this:

1. **Customers are demanding shorter commitments.** Cloud-native architectures reduce switching costs. Procurement teams push for annual or biannual renewals rather than multi-year lock-ins.

2. **AI creates demand for smaller, faster engagements.** Enterprise customers increasingly want $150K-$300K AI projects delivered in weeks, alongside their existing multi-million dollar contracts. The firms serving them are not designed to do both profitably.

3. **The organizational structure doesn't flex.** Sales, legal, compliance, pre-sales, security assessment — all built for high-value, low-frequency deals. The cost of processing a $300K deal through these functions approaches the cost of processing a $30M deal. Friction per deal is roughly constant regardless of deal size.

This is not hypothetical. In a recent conversation with a sales engineer at a major cloud data platform, the dynamic was described plainly: their largest enterprise client now regularly requests $150K-$300K AI projects alongside existing multi-million dollar contracts. The firm cannot profitably serve them — requirements gathering, configuration, testing, and deployment are all built for $3M-$30M engagements. But the client implies a larger deal will follow, so refusing is not an option. The firm is caught between a cost structure it cannot flex and a market it cannot ignore.

The result: firms must serve deals ranging from $30K to $300M, but their cost structure makes them unprofitable below a certain threshold. Most do not know what that threshold is.

### 1.4 The Market Has Already Moved

This is no longer a forward-looking thesis. The public markets are pricing it in now.

The entire IT outsourcing model is labour arbitrage — hire in India at $15/hour, bill American clients at $80/hour. When capable AI agents began shipping in early 2025, the market's response was immediate. Indian IT stocks dropped sharply in a single session: Infosys ADRs fell 8.4%, the Nifty IT index dropped 6%, Wipro fell 4.5%, Cognizant dropped approximately 10%.

The hiring data tells the same story. India's Big Four IT firms — TCS, Infosys, Wipro, HCL — historically hired 10,000+ people per quarter. TCS cut 11,000 employees in a single quarter. HCL remained flat. Revenue growth across the sector dropped to low single digits, down from the historical 15-20% annual growth that justified the hiring machine.

The revenue will not fall off a cliff. Multi-year enterprise contracts with high switching costs protect the near-term top line. But as contracts come up for renewal, headcount requirements will be renegotiated downward. The trajectory is eight to ten quarters of consensus estimates being trimmed by two to three percent each cycle — a slow bleed, not a sudden collapse. The firms know this. Their stock prices know this. Their hiring plans know this.

What the market is telling us: the labour arbitrage model is not facing disruption in five years. It is being repriced today.

---

## Part 2: The New Metric

### 2.1 Friction Per Unit of Revenue

Revenue per employee tells you how productive your people are. It does not tell you how efficient your organization is at converting opportunity into delivered revenue.

The metric that matters is **friction per unit of revenue**: the total cost — time and money — required to move one dollar from first customer conversation through to delivered outcome.

This includes selling, scoping, legal review, compliance, staffing, delivery, project management, documentation, and renewal. For a typical IT services project, engineering represents only 50-65% of total delivery cost. The remaining 35-50% is organizational friction.

Source: APQC benchmarks; Accenture's SG&A alone runs ~17% of revenue before delivery costs are counted.

A firm that minimizes friction per unit of revenue can profitably serve a $30K deal and a $30M deal. A firm that has only optimized delivery speed cannot — because the overhead per deal stays constant regardless of size.

The implication is a fundamental reorientation: optimize for deal velocity, not deal size. The economics of the old model — optimize delivery cost on a large, stable contract — do not transfer to a world where deal frequency is rising and deal size is falling. The firm that can move a $30K deal through its full pipeline at the same speed and margin as a $3M deal has a structural advantage that compounds with every deal closed.

### 2.2 Why AI Tools Don't Fix This

The standard response: give engineers AI tools. Cursor, Copilot, Devin. Measure developer productivity. Announce AI transformation.

This addresses one node in a multi-node pipeline. Grant the most optimistic claim — engineering gets 2x, 5x, even 10x faster. Everything upstream and downstream stays the same speed. The constraint relocates.

Making one stage faster while every other stage stays manual does not reduce friction. It moves the bottleneck from engineering to legal, from legal to compliance, from compliance to pre-sales. The firm does not get faster. Individual engineers get faster. The distinction matters.

The question is not whether AI tools improve developer productivity. Assume they do. The question is whether developer productivity was ever the binding constraint on friction per unit of revenue. In most IT services engagements, it was not. Engineering represents 50-65% of delivery cost. The remaining 35-50% — selling, scoping, legal, compliance, staffing, project management, knowledge transfer — is untouched by a better code editor. The firms announcing AI transformation by giving engineers Copilot are optimizing the minority of their cost structure while ignoring the majority.

### 2.3 Why Incumbents Cannot Buy Their Way Out

The natural counterargument: if the big firms see this problem, why can't they just invest their way to a solution? Accenture has committed $3B to AI capabilities and acquires 31+ companies per year. Surely scale and capital can close this gap.

It cannot, because the problem is structural, not financial.

An IT outsourcing operation built to sell 10,000 junior developers at $30/hour is a volume business. The entire organizational infrastructure — campuses, training pipelines, bench management, hierarchical delivery structures — exists to support labour arbitrage at scale. This infrastructure cannot be repurposed into high-leverage AI-native delivery any more than a container shipping company can pivot to same-day drone delivery by buying drones. The logistics, the talent model, the cost structure, and the culture are all optimized for a different game.

When these firms announce AI transformations, they are typically doing one of three things: procuring AI tools for their existing workforce (which relocates the bottleneck, per 2.2), rebranding existing consulting revenue as "AI consulting," or acquiring smaller firms and attempting to integrate them into operating structures designed for a fundamentally different delivery model. None of these address friction per unit of revenue. They address optics.

The firms that will crack this are not the ones with the most capital. They are the ones with no legacy infrastructure to protect.

---

## Part 3: What Replaces the Current Model

### 3.1 The Value Migration

The enterprise technology stack is restructuring into three layers, and the economics of each are diverging rapidly.

**Layer 1 — Infrastructure.** Databases, APIs, authentication, monitoring, event streams. These are becoming consumption-based utilities. As AI agents proliferate, infrastructure usage scales dramatically — a single AI agent generates hundreds of API calls per minute versus a human generating dozens per hour. Infrastructure becomes cheaper per unit and higher in total volume. This layer commoditizes.

**Layer 2 — Applications.** Dashboards, CRMs, project management tools, analytics platforms. This is where destruction is concentrated. When AI can generate interfaces and automate point solutions, the value of human-facing software built for manual workflows collapses. Per-seat licensing models break when the number of human seats shrinks. SaaS companies in this layer have lost over $300 billion in market capitalization. Public SaaS growth has halved from 36% to 17% since 2023. Switching costs — once the moat that protected these businesses — are dissolving as large language models make data migration trivial.

**Layer 3 — The Context Layer.** This is new. It is the institutional knowledge that directs AI agents: who accesses what data, what sequences complete which workflows, how decisions get made in practice versus on paper. This layer does not live in a document. It emerges from thousands of workflows executed over time. It captures things no one writes down — which deals stall at legal review, which clients need hand-holding during UAT, which compliance requirements are pro forma and which are genuinely blocking.

The economic logic follows Clayton Christensen's Law of Conservation of Attractive Profits: when one layer commoditizes, adjacent layers de-commoditize. Infrastructure is commoditizing. Applications are commoditizing. The context layer — the intelligence that connects them — is where value concentrates.

This creates a pincer dynamic. The bottom of the stack gets cheaper. The top of the stack gets more valuable. Everything in the middle — human-operated SaaS, labour arbitrage delivery firms — gets squeezed from both directions.

### 3.2 End-to-End AI Infrastructure

There are three ways a company can deploy AI: AI in the product it sells, AI for building the product, and AI to run the company. Most firms are focused on the first two. Very few are addressing the third — and that is where the structural economics change.

If friction per unit of revenue is the metric, then AI at one stage is not the solution. AI across the entire pipeline is.

Sales must move faster. Pre-sales must scope in days, not weeks. Legal must review contracts in hours. Compliance must clear in a single pass. Delivery must execute with fewer roles and less coordination overhead. Knowledge must transfer automatically, not through meetings.

No IT services firm is structured to build this. Their teams are organized by function, not by flow. Their tooling is procured per function. There is no connective tissue.

The connective tissue is the context layer. It is what converts a collection of AI-augmented functions into an integrated operating system.

### 3.3 The realfast Operating Model

realfast is built on this thesis. Every function in the company — pre-sales, delivery, operations, recruitment — runs on Exocortex, an AI operating system that spans the full pipeline.

Exocortex is our implementation of the context layer. It does three things:
- **Extracts** institutional knowledge from people, contracts, past projects, and domain expertise
- **Maintains** that knowledge as the business evolves — continuously reengineering processes as we learn what works and what does not
- **Applies** it across workflows — whoever needs it, whenever they need it

This is not a set of AI tools bolted onto existing processes. It is the operating infrastructure that allows us to piece together a customer's workflow faster, deliver against it faster, and improve the process with every engagement.

The economic mechanism is specific. Coordination overhead in a typical IT services project — project management, status alignment, knowledge transfer, cross-timezone handoffs, role-dependency wait times — represents 35-50% of total delivery cost. These are not engineering costs. They are organizational costs. They show up in payroll budgets, not IT budgets. Exocortex does not optimize this overhead. It structurally eliminates it. Consultants who previously required dedicated developers can now deliver independently. Knowledge that previously lived in people's heads is available to anyone in the system. The result is not a 10% efficiency gain. It is a 2-3x margin improvement on transformed workflows.

Every project completed makes the next one faster. Domain knowledge, workflow patterns, delivery playbooks, and client-specific context compound in Exocortex rather than dissipating when the project team disbands. Each engagement generates execution traces — granular records of what worked, what failed, what took longer than expected, what the client actually needed versus what the SOW described. These traces feed the next engagement. The system gets smarter by doing work, not by being trained.

The claim we are testing: realfast can profitably deliver at price points where traditional IT services firms cannot operate. Not because we charge less. Because our friction per unit of revenue is structurally lower.

The proof must hold at multiple price points. A $30K engagement delivered at 70% margin. A $3M engagement delivered at 70% margin. Same operating model, same infrastructure, same economics. If the model only works at one end of the spectrum, it is an optimization. If it works across the full range, it is a structural shift.

### 3.4 The Client-Side Thesis

There is a second-order opportunity embedded in this model.

If Exocortex gives realfast structurally different operating leverage, the same logic applies to any services organization. IT services firms, consulting practices, and managed service providers all suffer from the same friction problem. Their coordination overhead is the same 35-50% of delivery cost. Their knowledge dissipates after every engagement the same way.

The long-term thesis: over time, we embed a version of Exocortex on the client side. Not as a product sale — as an operational transformation. The client does not buy software. They gain the same operating leverage that realfast runs on, tuned to their domain, their workflows, their institutional knowledge.

This shifts realfast's commercial model from subcontracting at better margins to transforming how services organizations operate. The initial proof point is our own delivery economics. The scale opportunity is proving that those economics transfer.

### 3.5 Why This Cannot Be Easily Replicated

Four structural barriers:

1. **The extraction problem.** Tokenizing institutional expertise into a usable system is continuous and deeply technical. Most firms do not have the capability to build this infrastructure. The context layer does not come from a document or a data migration. It emerges from thousands of workflows actually executed — it must be built through doing, not through buying.

2. **The adoption problem.** Transformation requires top-down mandate and willingness to change who you hire and how they work. We have experienced this internally — some people refuse to use the tooling. Conviction drives adoption, not training. You deliver undeniable results first, then adoption follows.

3. **The compounding problem.** Every engagement generates execution traces — not just data, but operational intelligence about how workflows actually behave in practice. Which deals stall at legal review. Which client stakeholders need early alignment. Which compliance requirements are blocking versus procedural. A competitor starting today is not just behind on technology — they are behind on thousands of accumulated workflow traces that encode the organizational decision logic of every domain we have operated in. This gap widens with every project.

4. **The infrastructure mismatch.** Incumbents cannot build this without dismantling the organizational infrastructure that generates their current revenue. Their campuses, training pipelines, bench management systems, and hierarchical delivery structures are all optimized for labour arbitrage at scale. Building a context layer requires a fundamentally different talent model, cost structure, and operating philosophy. The firms with the most to gain from this transition are the ones least able to execute it.

---

## Part 4: Audience Implications

### For Investors (VC / PE)

IT services is a trillion-dollar industry running on a model that has not improved its fundamental unit economics in a decade. RPE is flat. Bench is gone. Deal structures are compressing. The public markets are already repricing these firms — Indian IT stocks dropped sharply on the first credible AI agent launches, and hiring across the sector has collapsed from 10,000+ per quarter to net reductions.

Firms are responding with capital allocation that does not address the structural problem. Procuring AI tools for engineers relocates the bottleneck. Announcing AI consulting revenue rebrands existing work. Acquiring AI startups imports capability into operating structures that cannot absorb it. The incumbents are spending billions to avoid the organizational transformation that would actually matter.

The first firm to crack friction per unit of revenue across the full pipeline captures a disproportionate share of the restructuring. realfast has built the operating model and is proving it in market.

The enterprise technology stack is restructuring into three layers: infrastructure (commoditizing), applications (compressing), and the context layer (emerging as the new value center). Exocortex is an operational implementation of the context layer — built through actual service delivery, not through SaaS product development. This is a differentiated path that pure software companies cannot replicate, because the context layer must be built by executing workflows, not by selling seats.

The scale question is not "can this firm grow revenue?" It is "can this operating model transform existing IT services firms?" If yes, the relevant comparison is not a startup revenue multiple. It is the delta in enterprise value created by transforming a $1B+ revenue firm's cost structure. The acquisition market for proven AI operating models is real and accelerating.

### For Customers (Enterprises)

You are about to spend money on an implementation, an AI transformation, or both. The firms you would normally hire for this work — Accenture, TCS, Wipro, Cognizant, Deloitte — are built on a model that has not improved its fundamental economics in a decade. They will staff your project with a team structured for coordination overhead: project managers, business analysts, architects, developers, QA engineers, each handing off to the next, each adding time and cost. 35-50% of what you pay them is not engineering. It is the organizational friction required to move work through their system.

You will not see this on their invoice. It shows up as timeline — the months between kickoff and go-live that feel longer than they should. It shows up as rework — requirements lost in translation between the person who understood your problem and the person who wrote the code. It shows up as cost — the $3M price tag for a project that, if you could see the actual engineering hours, represents $1.5M of productive work and $1.5M of coordination tax.

This is not incompetence. It is architecture. Their delivery model requires this overhead. They cannot remove it without dismantling the organizational structure that generates their revenue.

realfast operates on a structurally different model. Our delivery runs on Exocortex — an AI operating system that spans the full pipeline from pre-sales through delivery through ongoing optimization. Institutional knowledge that would normally live in people's heads and dissipate when the team disbands is captured, maintained, and applied across every engagement. Consultants who would normally require dedicated developers, project managers, and business analysts can deliver independently. The coordination overhead that inflates your bill is structurally eliminated, not optimized.

The result is not a marginal improvement. It is the same outcome — production-grade, enterprise-quality delivery — at fundamentally different speed and cost. A workflow that takes a traditional firm 12 weeks and $500K takes us 3-6 weeks at a fraction of the cost. Not because we cut corners. Because our operating model does not carry the friction theirs does.

We start narrow. One workflow. One business metric. 3-6 weeks to production. We prove the delta against what you would have gotten from the firm you were about to hire. If we fail, you know quickly and cheaply. If we succeed, you have a measurable gap — time, cost, quality — and a decision to make about your next project.

Every engagement we deliver compounds. Domain knowledge, workflow patterns, and the specific context of your business accumulate in Exocortex rather than walking out the door when the project ends. The second project is faster than the first. The third is faster than the second. Over time, what you are building with us is not a series of disconnected implementations — it is an operational intelligence layer tuned to your business, your workflows, your institutional knowledge. The end state is not a permanent dependency on realfast. It is your organization running on the same operating leverage we do.

Your competitors will hire Accenture. They will get Accenture's cost structure, Accenture's timeline, and Accenture's coordination overhead. Nobody gets fired for that decision. But the firm that moves first on a structurally better model compounds the advantage with every project. The gap between you and your competitors does not stay constant. It widens.

### For IT Services Firms (The Transformation Opportunity)

There is a second audience for this thesis: IT services firms themselves.

If you run a services organization — implementation, consulting, managed services — your economics are governed by the same friction problem described in this document. Your RPE has not moved. Your bench is gone. Your cost structure makes you unprofitable below a certain deal size, and your customers are asking for smaller, faster engagements.

The operating leverage that realfast runs on is not proprietary to our domain. It applies to any services organization where coordination overhead represents a significant portion of delivery cost. Over time, as we prove the model through direct client delivery, we will extend it to services firms seeking to transform their own operations — embedding the same context layer infrastructure inside your organization, tuned to your domain expertise and delivery methodology.

This is not a software sale. It is an operational transformation: proving the delta on your own work, then scaling it across your teams and verticals. The initial proof point is our delivery economics. The scale opportunity is proving that those economics transfer.

---

## Part 5: Open Questions

These are unresolved. They will be closed through execution, not analysis.

1. **Can the model extend beyond Salesforce?** The initial proof point is Salesforce delivery. Extension to consulting, healthcare, financial services is the hypothesis being tested.

2. **Can friction per unit of revenue be quantified?** The concept is strong. The formula is not yet defined. This needs to become a calculable number before it is investor-grade.

3. **What is realfast's own RPE?** If we are making this argument, we need to show ours. This is the most powerful proof point available.

4. **What is the right commercial model?** Subcontracting, licensing, or transformation. Each has different economics and lock-in. Early engagements will inform which path to pursue. The client-side embedding thesis opens a fourth option that may subsume the others.

5. **The convergence hypothesis.** Will consulting RPE and IT implementation RPE converge as AI commoditizes implementation? Directionally plausible. Not yet provable. Monitor but do not lead with this claim externally.

6. **Who owns the context layer?** The enterprise technology stack is restructuring. Infrastructure and applications are commoditizing. The context layer — institutional knowledge that directs AI agents — is emerging as the new value center. The open question is whether this layer gets owned by incumbents who already hold the data (ServiceNow, enterprise platforms) or by firms that build the most capable operational intelligence through actual workflow execution. realfast's bet is that the context layer cannot be bought or aggregated from existing data — it must be built through doing the work. If this is correct, the first-mover advantage compounds indefinitely.

---

## Appendix: Data Sources

- Bullfincher — Infosys RPE historical
- StockAnalysis — TCS revenue and headcount
- Pathfinders Training / Communications Today — FY25 RPE comparison
- Trak.in / Economic Times / NiftyTrader — Bench reduction data
- APQC — Professional services overhead benchmarks
- Accenture IR — SG&A, acquisition volume, $3B AI investment
- Public market data — Indian IT stock price reactions, Nifty IT index, ADR movements
- Industry hiring data — Big Four quarterly headcount filings
