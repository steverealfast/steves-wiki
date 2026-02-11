# Bottomline — AI Customer Service Transformation Playbook

*Prepared for Yaderl Padilla. Management Consultant lens applied throughout.*

---

## The Trigger

On February 10, Bottomline's executive leadership called an Emergency AI Council meeting. The reason: Thoma Bravo portfolio companies are coming back and claiming AI wins in customer support that Bottomline is not claiming. The executive team's question was direct: *"What's holding you back? You got a plan. Let's make it happen."*

This document exists because of that question. Everything in it ties back to one objective: giving Yaderl the vision, the target state, and the plan to answer it.

---

## What Your Sibling Companies Are Doing While You're Deliberating

This is not hypothetical. Thoma Bravo portfolio companies are actively deploying AI in their customer service operations — and claiming measurable wins. Here's what the companies sitting next to you in the portfolio are reporting:

**SolarWinds** built a multi-phase AI journey across their service desk: Smart Suggestions for surfacing similar tickets and KB articles, a Virtual Agent handling 24/7 conversational self-service, and GenAI features that draft responses and summarize tickets for agents. In October 2025, they launched an AI Agent that can summarize outages, gather diagnostics, and suggest remediation autonomously. Their 2026 roadmap includes AI-generated knowledge base articles from solved incidents.

**Proofpoint** deployed Amazon Q Business across their professional services team and migrated their knowledge base to NICE CXone Expert with AI/ML-powered search. Results: **40% productivity increase** in administrative tasks, **18,300+ hours saved annually**, and a **5% decrease in ticket volume** even as their customer base grew 18%. Their session-to-ticket ratio improved from 3:1 to 40:1 — meaning 40 customers self-serve for every one that creates a ticket.

**Kaseya** rolled out Cooper Copilot with Smart Ticket Triage that automatically categorizes and routes tickets, plus a Smart SOP Generator that creates standard operating procedures from ticket data. Results: **40% reduction in ticket triage time**, one customer reported **$70K monthly revenue gains**, and they've auto-generated **13,000+ SOPs** since March 2025. Engineers report saving hours per week on manual triage alone.

**ConnectWise** embedded AI directly into their PSA platform via Sidekick — providing real-time ticket triage, classification, root cause analysis, and automated email replies. Results: **40% reduction in incident resolution times**, **86% improvement in first-time resolution rates**, and **75% time saved per ticket** on routine tasks.

**RealPage** deployed an AI chatbot (Paige, now evolved into their LUMINA AI platform) that answers **95% of incoming question types** without human intervention. Only 5% transfer to live agents. Early adopters report **10 hours saved per employee per week** and **10-20% higher conversion rates**.

**Barracuda Networks** launched Barracuda Assistant in November 2025 — an AI chatbot integrated across their support communities and Managed XDR dashboard, converting 20+ years of documentation and best practices into a conversational troubleshooting tool available 24/7.

### The Pattern Across the Portfolio

These aren't isolated experiments. Look at what the portfolio is converging on:

| Capability | SolarWinds | Proofpoint | Kaseya | ConnectWise | RealPage | Barracuda |
|-----------|-----------|-----------|--------|------------|---------|-----------|
| AI Self-Service / Chatbot | Yes | — | Yes | — | Yes | Yes |
| AI Ticket Triage & Routing | Yes | Partial | Yes | Yes | — | Partial |
| Agent Assist / Copilot | Yes | Yes | Yes | Yes | Yes | Yes |
| AI Knowledge Management | 2026 | Yes | Yes | — | Yes | Yes |

**The uncomfortable implication:** Your sibling portfolio companies aren't debating whether AI works in customer service. They've moved past that question. They're measuring 40% triage reductions, 95% auto-resolution rates, and $70K/month in operational gains. That's the standard the Emergency AI Council is measuring Bottomline against.

---

## Why You Don't Have a Plan Yet (And Why That's Structural, Not Personal)

Yaderl named the problem on the call: *"Put the technology aside for a second. What are those big problem statements, what are those big outcomes, what are those big business objectives?"*

That instinct is correct. Here's why the plan doesn't exist yet:

**1. No one has done the process investigation.**
You can't define AI goals for customer service without understanding what your agents actually do — step by step, interaction by interaction. Every conversation about "AI in support" has been technology-first, not process-first. CoPilot, chatbots, knowledge bases — these are solutions looking for a problem definition that doesn't exist yet.

**2. Two foundational blockers remain unresolved.**
- **Knowledge base:** It's not clean. Without it, self-service is crippled and any AI tool that needs to reference your content will produce unreliable answers.
- **Customer Cube:** Your agents don't have a complete view of what a customer has before trying to help them. This is not an AI problem — it's a data architecture problem that must be solved regardless.

**3. AI adoption is an execution problem, not a procurement problem.**
Buying tools — whether CoPilot, ExoHelp, or anything else — doesn't change how work flows through your support organization. The Emergency AI Council's implicit question ("why aren't we claiming wins?") is actually a question about process, not technology.

*Notice that every portfolio company claiming wins above didn't just buy a tool. SolarWinds built a three-phase AI journey over years. Proofpoint restructured their knowledge management architecture. Kaseya embedded AI directly into their PSA workflow. They changed how work flows — not just what tools sit on top of it.*

---

## The Framework: Classify Before You Automate

Before touching any technology, every customer service workflow needs to be classified by the type of friction it creates. This determines where AI can generate real value versus where it would just add complexity.

| | AUTOMATE | AUGMENT | CONNECT |
|---|---|---|---|
| **The problem** | Agents doing unnecessary manual work | Agents making decisions without adequate support | Systems and data that don't talk to each other |
| **Symptoms** | High AHT, repetitive tasks, post-call wrap-up, ticket routing | Inconsistent responses, slow escalation, missed cross-sell | Agents toggling between systems, no customer 360, manual lookups |
| **AI mechanism** | Straight-through processing, auto-categorization, wrap-up bots | Real-time recommendations, sentiment scoring, next-best-action | Cross-system data stitching, unified agent desktop, knowledge retrieval |
| **Business lever** | Cost-to-serve reduction, throughput increase | CSAT, FCR improvement, revenue per interaction | Operational efficiency, reduced handle time |

### How Your Sibling Companies Map to This Framework

This isn't abstract. The portfolio companies claiming wins are operating across all three categories:

| Category | Who's Doing It | What They Did | What Realfast Delivers Here |
|----------|---------------|---------------|----------------------------|
| **AUTOMATE** | Kaseya (Smart Ticket Triage), ConnectWise (Sidekick), RealPage (Paige/LUMINA) | Auto-categorization, ticket routing, self-service resolution — removing manual work from agents entirely | **Service Assistant:** AI-powered front door that handles ticket classification, routing, and self-service resolution. Already in scope for Bottomline. This is the fastest path to a measurable win. |
| **AUGMENT** | SolarWinds (GenAI draft responses), Kaseya (Cooper Copilot), Proofpoint (Amazon Q Business) | Real-time agent assist — drafting responses, surfacing solutions, summarizing tickets so agents work faster and more consistently | **ExoHelp:** Already piloting at Bottomline. Generates impact analysis, evidence documentation, and test cases from ticket content. Ashish's feedback: *"really, really valuable information."* This extends into full agent augmentation. |
| **CONNECT** | Proofpoint (NICE CXone Expert), SolarWinds (AI KB generation), Barracuda (Assistant over 20 years of docs) | Knowledge base as an AI-queryable layer — agents and customers get answers from structured institutional knowledge instead of manual lookup | **Exocortex knowledge layer:** Captures institutional knowledge from every ticket, every resolution, every workflow. This is the compounding advantage — and it directly addresses the knowledge base cleanup blocker Paulomi identified. |

*The question for Bottomline: Which of these three categories is your biggest source of friction today? You don't actually know — because no one has done the process investigation to find out. That's step one.*

---

## The Five Metrics That Matter

Yaderl asked for measurable objectives. In customer service, there are five metrics that every organization measures and every PE firm cares about. These aren't aspirational — they're your baseline:

| Metric | What It Measures | What the Portfolio Is Achieving |
|--------|-----------------|-------------------------------|
| **Average Handle Time (AHT)** | Time per interaction (talk + hold + wrap-up) | Kaseya: engineers saving hours/week on triage. ConnectWise: 75% time saved per ticket on routine tasks. |
| **First Call Resolution (FCR)** | % of issues resolved on first contact | ConnectWise: 86% improvement in first-time resolution rates. RealPage: 95% of questions answered without human intervention. |
| **Customer Satisfaction (CSAT)** | Post-interaction satisfaction score | RealPage: same satisfaction as live chat at 30% lower cost. |
| **Cost-to-Serve** | Fully loaded cost per interaction | Proofpoint: 5% ticket volume decrease while customer base grew 18%. Kaseya: $70K/month gains from one customer. |
| **Agent Utilization / Capacity** | How much productive work per agent-hour | Proofpoint: 40% productivity increase. RealPage: 10 hours saved per employee per week. |

**Your immediate homework (this week):** Establish your current baseline on these five metrics. You don't need AI for this. You don't need us for this. You need this before anything else can begin.

*Every time TB's executive team asks "where's your plan," the first answer should be: "We've baselined our five core metrics. Here's where we are. Here's where we need to be. Here's the plan to get there."*

---

## The Approach: How We Get From Here to a Plan

This is the recipe book Yaderl asked for.

### Phase 0: Internal Readiness (Bottomline owns this — 1-2 weeks)

Before any outside engagement begins, two things must be true:

1. **Baseline metrics are established** — AHT, FCR, CSAT, cost-to-serve, and agent utilization across your primary support segments
2. **Robert has defined the top 3-5 problem statements** — not technology wish lists, but business outcomes: "We want to reduce cost-to-serve by X" or "We want to improve FCR from Y to Z"

This is the work Yaderl correctly identified: *"Someone needs to set a vision for support. Someone needs to set some metrics."* Do this first. It takes days, not months.

### Phase 1: Process Investigation (2-3 weeks)

**What happens:**
- Over-the-shoulder observation with service agents across primary support queues
- Process mapping of actual workflows — what agents do, step by step, interaction by interaction
- Classification of every workflow against the AUTOMATE / AUGMENT / CONNECT framework
- Identification of the top 3-5 workflows where AI intervention would move the baseline metrics

**What you receive:**
- Current-state process map for your customer service operation
- Friction classification for each major workflow
- Recommended target-state workflows with AI intervention points
- Projected impact on each of the five baseline metrics
- ROI model for each recommended intervention

**Why this matters more than jumping to technology:** Paulomi said it on the call: *"I can't see a world where you continue to try to use the technology without knowing how to change the process."* This phase is the process investigation that makes everything else possible.

**What Realfast specifically brings:** This is not a generic consulting assessment. We classify every workflow against the same AUTOMATE / AUGMENT / CONNECT framework your sibling companies used to identify their wins. The output is not a report — it's a scored list of workflows with projected metric impact, mapped to specific AI interventions we've already built (Service Assistant for AUTOMATE, ExoHelp for AUGMENT, Exocortex for CONNECT).

*For TB's executive team: "We've completed a structured process investigation of our customer service operation. We've identified X workflows where AI intervention would reduce cost-to-serve by Y% and improve FCR by Z%. Here's the implementation plan."*

### Phase 2: Proof Point (3-4 weeks)

**What happens:**
- Select one workflow from Phase 1 — the one with the best math (high frequency, existing data, direct metric, contained scope)
- Build and deploy an AI system against that workflow
- Measure before/after impact against baseline

**Selection criteria for the first workflow:**

| Filter | Why It Matters |
|--------|---------------|
| **Direct business metric** | Must tie to one of the five metrics TB cares about |
| **Repeatable workflow** | High frequency = fast learning loop = fast proof |
| **Existing data** | No data engineering project required before AI can run |
| **Contained blast radius** | Failure doesn't cascade; success is clearly attributable |

**Where Realfast is already positioned:** You're not starting from zero. Service Assistant is already in scope. ExoHelp is already in pilot — with positive agent feedback on impact analysis, evidence documentation, and test case generation. Phase 2 takes one of these and measures it against baseline. The infrastructure exists. The proof point is a matter of focus, not invention.

**What you receive:**
- A production AI system embedded in one workflow, used by real agents
- Measured before/after impact on the specific metric
- Documentation for stakeholder reporting

*For TB's executive team: "We deployed AI on our highest-friction workflow. AHT dropped by X seconds / FCR improved by Y% / cost-to-serve reduced by Z%. Here's what we're doing next."*

### Phase 3: Expansion (Ongoing)

Phase 2 proved it on one workflow. Phase 3 applies the same model to the next 3-5 workflows identified in Phase 1. Each deployment follows the same playbook: narrow scope, measure against baseline, expand from proof.

**The compounding advantage:** Every workflow we instrument captures knowledge — about your customers, your processes, your edge cases. This becomes a knowledge layer (Exocortex) that makes every subsequent deployment faster and more accurate. By the third or fourth workflow, you're operating at a fundamentally different speed than a team starting from scratch. This is how Proofpoint went from a knowledge base migration to 18,300 hours saved annually. This is how SolarWinds moved from Smart Suggestions to a full AI Agent. The first deployment teaches the system; every subsequent one benefits.

*For TB's executive team: "We've now deployed AI across X workflows. Cumulative impact: Y% reduction in cost-to-serve, Z% improvement in CSAT. We have a pipeline of N additional workflows in various stages of deployment."*

---

## What This Looks Like as a Timeline

| Phase | Owner | Duration | TB Narrative |
|-------|-------|----------|--------------|
| **Phase 0: Baseline** | Bottomline (Robert/Yaderl) | 1-2 weeks | "We've established our metrics and defined our objectives" |
| **Phase 1: Process Investigation** | Realfast + Bottomline | 2-3 weeks | "We've completed a structured AI readiness assessment of our service operation" |
| **Phase 2: Proof Point** | Realfast | 3-4 weeks | "We've deployed AI on one workflow with measurable results" |
| **Phase 3: Expansion** | Realfast + Bottomline | Ongoing | "We're scaling AI across our service operation with compounding returns" |

**Total time from kickoff to first measured proof point: 6-9 weeks.**

That means if you start Phase 0 now, you could have a proof point to present to TB's executive team within two months. Kaseya went from Cooper Copilot launch to 13,000 auto-generated SOPs in under a year. ConnectWise went from Sidekick launch to 40% resolution improvement within months. The velocity is real — but only if you start.

---

## The Two Blockers That Must Be Addressed in Parallel

These won't stop you from starting, but they will limit how far you can go:

**1. Knowledge Base Cleanup**
Your knowledge base is not in a state where AI can reliably use it to answer customer questions or assist agents. This is a prerequisite for self-service AI and agent augmentation workflows. It doesn't need to be perfect — but it needs to be prioritized and actively worked. Note: Proofpoint's migration of their knowledge base to NICE CXone Expert was the foundation that enabled their 40:1 session-to-ticket ratio. Barracuda's Assistant works because it sits on top of 20 years of structured documentation. The knowledge base isn't a separate problem — it's the foundation for every CONNECT and self-service play.

**2. Customer Cube**
Agents can't see what a customer has before trying to help them. This is a data architecture problem, not an AI problem. Until this is solved, any AI system that tries to personalize service or route intelligently will be working with incomplete data.

**Recommendation:** Start these as parallel workstreams. Don't wait for them to be "done" before beginning Phase 1. They inform the process investigation and get better as the investigation progresses.

---

## How to Talk About This Internally

Yaderl needs ammunition for the executive team. Here's how to frame it at each stage:

**Right now (this week):**
> "We've acknowledged the gap. We're baselining our five core customer service metrics and defining measurable objectives. We've engaged a partner with experience in AI transformation to run a structured process investigation — the same approach our sibling portfolio companies used to achieve 40% triage reductions and 95% self-service resolution. First results in 6-8 weeks."

**After Phase 1 (3-4 weeks from now):**
> "We've completed a process investigation across our major support workflows. We've identified the top opportunities where AI would move our cost-to-serve and CSAT metrics — using the same AUTOMATE / AUGMENT / CONNECT framework that SolarWinds, Kaseya, and ConnectWise used to structure their AI deployments. We're starting the first deployment this week."

**After Phase 2 (6-9 weeks from now):**
> "We've deployed AI on [specific workflow]. [Metric] improved by [X%]. We're expanding to three additional workflows over the next quarter. Here's the projected impact at scale."

**The underlying message at every stage:** We're not buying tools and hoping they work. We're running a structured, measurable transformation — the same approach that's produced quantifiable wins across the Thoma Bravo portfolio — with a partner who's already embedded in our operation and understands our specific workflows.

---

## What We're Not Proposing

- We're not proposing to install a chatbot and call it AI transformation
- We're not proposing a 6-month strategy engagement before any work begins
- We're not proposing to replace your agents with AI
- We're not proposing to compete with CoPilot or Verint as a platform

We're proposing to do the process investigation that no one has done, identify where AI moves the metrics that TB cares about, prove it on one workflow, and then scale it. Structured. Measurable. Reportable.

---

## The Competitive Reality

Your sibling portfolio companies aren't waiting. SolarWinds has a production AI Agent. Proofpoint is saving 18,300 hours a year. Kaseya's Cooper Copilot is generating 13,000+ SOPs automatically. ConnectWise achieved 86% improvement in first-time resolution. RealPage auto-resolves 95% of customer queries.

Thoma Bravo also spent $2B acquiring Verint and combining it with Calabrio — creating what they call "the industry's most comprehensive AI-powered CX platform" targeting a $50B+ market. That's not just an investment thesis. That's the standard your PE owner uses to evaluate every portfolio company's AI maturity.

Bottomline is a Thoma Bravo portfolio company that has not yet demonstrated AI capability in customer service. The Emergency AI Council exists because that gap is visible to the executive team.

The question is not whether to act. The question is whether Bottomline leads this conversation or gets led by it.

**The plan starts with Phase 0. Phase 0 starts this week.**

---

## Sources

- [SolarWinds AI Journey: Smart Suggestions, Virtual Agent, and Generative AI](https://thwack.solarwinds.com/products/solarwinds-service-desk-swsd/b/news/posts/smart-suggestions-virtual-agent-and-generative-ai-the-solarwinds-service-desk-ai-journey)
- [SolarWinds Launches AI Agent (October 2025)](https://www.solarwinds.com/company/newsroom/press-releases/solarwinds-launches-ai-agent-expands-ai-capabilities-advance-autonomous-operational-resilience)
- [Proofpoint Uses Amazon Q Business — AWS Case Study](https://aws.amazon.com/blogs/machine-learning/unlocking-the-future-of-professional-services-how-proofpoint-uses-amazon-q-business/)
- [Proofpoint + NICE CXone Expert — Case Study](https://resources.nice.com/wp-content/uploads/2024/09/CaseStudyProofpointv02.pdf)
- [Kaseya Connect 2025 AI Showcase Keynote](https://www.kaseya.com/blog/ai-showcase-keynote-kaseya-connect-2025/)
- [ConnectWise Launches PSA Powered by Asio (June 2025)](https://www.globenewswire.com/news-release/2025/06/03/3092835/0/en/ConnectWise-Launches-PSA-Powered-by-Asio-and-ConnectWise-Pro-at-IT-Nation-Secure-2025.html)
- [RealPage AI Chatbot Paige — Success Metrics](https://www.realpage.com/news/realpage-sees-success-with-ai-chatbot-named-paige/)
- [Barracuda Assistant Launch (November 2025)](https://blog.barracuda.com/2025/11/05/introducing-barracuda-assistant--your-ai-powered-partner-for-fas)
- [Thoma Bravo Completes Acquisition of Verint](https://www.thomabravo.com/press-releases/thoma-bravo-completes-acquisition-of-verint-a-leader-in-ai-driven-customer-experience-automation)
- [Thoma Bravo Portfolio Companies](https://www.thomabravo.com/companies)
