# realfast — Master Narrative

*v0.2 — February 2026. Living document.*

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

This addresses one node in a multi-node pipeline. Engineering gets faster. Everything upstream and downstream stays the same speed. The constraint relocates.

A randomized controlled trial by METR (July 2025) found experienced developers were 19% slower with AI tools, despite perceiving themselves as 20% faster. GitClear's analysis of 211 million changed lines found code churn rose from 5.5% to 7.9% between 2020-2024 — AI generates more code, not better code.

Sources: METR (arXiv:2507.09089), GitClear 2025.

Making one stage faster while every other stage stays manual does not reduce friction. It moves the bottleneck from engineering to legal, from legal to compliance, from compliance to pre-sales. The firm does not get faster. Individual engineers get faster. The distinction matters.

---

## Part 3: What Replaces the Current Model

### 3.1 End-to-End AI Infrastructure

There are three ways a company can deploy AI: AI in the product it sells, AI for building the product, and AI to run the company. Most firms are focused on the first two. Very few are addressing the third — and that is where the structural economics change.

If friction per unit of revenue is the metric, then AI at one stage is not the solution. AI across the entire pipeline is.

Sales must move faster. Pre-sales must scope in days, not weeks. Legal must review contracts in hours. Compliance must clear in a single pass. Delivery must execute with fewer roles and less coordination overhead. Knowledge must transfer automatically, not through meetings.

No IT services firm is structured to build this. Their teams are organized by function, not by flow. Their tooling is procured per function. There is no connective tissue.

### 3.2 The realfast Operating Model

realfast is built on this thesis. Every function in the company — pre-sales, delivery, operations, recruitment — runs on Exocortex, an AI operating system that spans the full pipeline.

Exocortex does three things:
- **Extracts** institutional knowledge from people, contracts, past projects, and domain expertise
- **Maintains** that knowledge as the business evolves
- **Applies** it across workflows — whoever needs it, whenever they need it

This is not a product we sell. It is the infrastructure that allows us to operate with structurally different economics.

Consultants who previously required dedicated developers can now deliver independently. Role dependencies eliminated. Timezone complexity eliminated. Coordination overhead eliminated. This is not a 10% efficiency gain. It is a 2-3x margin improvement on transformed workflows.

Every project completed makes the next one faster — domain knowledge compounds in Exocortex rather than dissipating when the project team disbands.

The claim we are testing: realfast can profitably deliver at price points where traditional IT services firms cannot operate. Not because we charge less. Because our friction per unit of revenue is structurally lower.

The proof must hold at multiple price points. A $30K engagement delivered at 70% margin. A $3M engagement delivered at 70% margin. Same operating model, same infrastructure, same economics. If the model only works at one end of the spectrum, it is an optimization. If it works across the full range, it is a structural shift.

### 3.3 Why This Cannot Be Easily Replicated

Three structural barriers:

1. **The extraction problem.** Tokenizing institutional expertise into a usable system is continuous and deeply technical. Most firms do not have the capability to build this infrastructure.

2. **The adoption problem.** Transformation requires top-down mandate and willingness to change who you hire and how they work. We have experienced this internally — some people refuse to use the tooling. Conviction drives adoption, not training. You deliver undeniable results first, then adoption follows.

3. **The compounding problem.** Every engagement adds to Exocortex's knowledge base. A competitor starting today is not just behind on technology — they are behind on accumulated domain expertise. This gap widens with every project.

---

## Part 4: Audience Implications

### For Investors (VC / PE)

IT services is a trillion-dollar industry running on a model that has not improved its fundamental unit economics in a decade. RPE is flat. Bench is gone. Deal structures are compressing. Firms are responding with tool procurement that does not address the structural problem.

The first firm to crack friction per unit of revenue across the full pipeline captures a disproportionate share of the restructuring. realfast has built the operating model and is proving it in market.

The scale question is not "can this firm grow revenue?" It is "can this operating model transform existing IT services firms?" If yes, the relevant comparison is not a startup revenue multiple. It is the delta in enterprise value created by transforming a $1B+ revenue firm's cost structure.

Accenture acquires 31+ companies per year and has committed $3B to AI capabilities. They are actively acquiring what they cannot build. The acquisition market for proven AI operating models is real and accelerating.

### For Customers (IT Services Firms)

Your revenue per employee has not meaningfully improved in a decade. Your bench is gone. Your cost structure makes you unprofitable below a certain deal size — and your customers are increasingly asking for deals below that size.

Giving your engineers AI tools will not fix this. It accelerates one stage of a multi-stage pipeline. The constraint moves. Friction per unit of revenue stays the same.

We are not proposing to train your people. We are not proposing to sell you software. We are proposing to deliver your work using our operating model and prove the delta. If we fail, we don't charge.

If we succeed, you have a measurable gap — time, cost, quality — against your current operating model. Then we talk about what your organization looks like with this embedded across more teams, more verticals, more of the pipeline.

Your competitors cannot get their hands on this capability. If one firm in your space cracks friction per unit of revenue, every other firm is structurally disadvantaged.

---

## Part 5: Open Questions

These are unresolved. They will be closed through execution, not analysis.

1. **Can the model extend beyond Salesforce?** The initial proof point is Salesforce delivery. Extension to consulting, healthcare, financial services is the hypothesis being tested.

2. **Can friction per unit of revenue be quantified?** The concept is strong. The formula is not yet defined. This needs to become a calculable number before it is investor-grade.

3. **What is realfast's own RPE?** If we are making this argument, we need to show ours. This is the most powerful proof point available.

4. **What is the right commercial model?** Subcontracting, licensing, or transformation. Each has different economics and lock-in. Early engagements will inform which path to pursue.

5. **The convergence hypothesis.** Will consulting RPE and IT implementation RPE converge as AI commoditizes implementation? Directionally plausible. Not yet provable. Monitor but do not lead with this claim externally.

---

## Appendix: Data Sources

- Bullfincher — Infosys RPE historical
- StockAnalysis — TCS revenue and headcount
- Pathfinders Training / Communications Today — FY25 RPE comparison
- Trak.in / Economic Times / NiftyTrader — Bench reduction data
- APQC — Professional services overhead benchmarks
- METR (arXiv:2507.09089) — AI developer productivity RCT
- GitClear 2025 — Code quality impact of AI tools
- Accenture IR — SG&A, acquisition volume, $3B AI investment
