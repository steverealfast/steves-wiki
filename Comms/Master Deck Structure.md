# realfast — Master Deck Structure

*Living slide guide. Extracted from Master Narrative v0.4.*
*Persona: Strategic Narrative Architect*

---

## How to Use This Document

This is a **modular slide structure**. Each slide has an audience tag:

- **[ALL]** — Use in every version of the deck
- **[INVESTOR]** — Include when speaking to VCs, PEs, board members
- **[ENTERPRISE]** — Include when speaking to CXOs evaluating vendors
- **[IT SERVICES]** — Include when speaking to services firms about transformation

**Recommended deck lengths:**
- Investor deck: Slides tagged [ALL] + [INVESTOR] = ~18 slides + appendix
- Enterprise deck: Slides tagged [ALL] + [ENTERPRISE] = ~15 slides + appendix
- Full thesis: All slides = ~28 slides + appendix

Each slide specifies:
- **TITLE**: Declarative — states a conclusion, not a topic. Reading titles alone tells the full argument.
- **ON SLIDE**: What the audience sees. One idea per slide.
- **VISUAL DIRECTION**: Guidance for the designer.
- **SPEAKER NOTES**: What you say over the slide. The nuance, the story, the conviction.

---

## Governing Question

> What does an IT services firm need to look like in three years to survive?

---

# SECTION A: THE PROBLEM

*Arc position: Situation → Complication*
*Purpose: Establish that the current model is structurally broken. Not a prediction — already happening.*

---

### Slide 1 — Title Slide [ALL]

**TITLE**: realfast

**ON SLIDE**:
- realfast logo
- Tagline: "AI-native IT services"
- Presenter name and date

**VISUAL DIRECTION**: Clean. No clutter. Confidence, not hype. Dark background, minimal type.

**SPEAKER NOTES**: No narration needed. Let the room settle.

---

### Slide 2 — The Governing Question [ALL]

**TITLE**: IT services is a trillion-dollar industry running on a model that hasn't improved in a decade

**ON SLIDE**:
- Single line: "What does an IT services firm need to look like in three years to survive?"
- Below: "$1T+ industry. Flat unit economics. Structural repricing underway."

**VISUAL DIRECTION**: Text-only. Large type. The question should dominate the slide. Let it breathe.

**SPEAKER NOTES**: "This is the question we've built our company around. Not 'how do we use AI' — that's a tool question. The structural question is: why has a trillion-dollar industry not improved its fundamental economics in ten years, and what happens when AI forces the issue? Everything I'm about to show you flows from this."

---

### Slide 3 — Revenue per employee has not moved [ALL]

**TITLE**: IT services revenue per employee has been flat to declining for a decade

**ON SLIDE**:

| Company | RPE (FY2015) | RPE (FY2023) | Change |
|---|---|---|---|
| Infosys | $49,442 | $53,060 | +7.3% over 8 years |
| TCS | ~$50,700 | ~$47,000 | Flat to negative |
| Wipro | ~$48,000 | ~$45,100 | Declining |
| HCLTech | ~$65,000 | ~$61,400 | Declining |

- Callout: "TCS: Revenue doubled ($16B → $30B). Headcount doubled (319K → 608K). Ratio unchanged."

**VISUAL DIRECTION**: Clean data table. Consider a line chart overlay showing revenue growth vs RPE flatline — the divergence is the story. Sources cited in small type at bottom.

**SPEAKER NOTES**: "TCS is the clearest case. They nearly doubled revenue over a decade. Sounds impressive — until you see headcount nearly doubled too. At roughly $50K RPE, every additional million dollars of revenue requires 20 new people. This is arithmetic, not opinion. When RPE does tick up — as it did for Infosys recently — it's driven by layoffs, not structural improvement. The top five firms shed 57,900 employees in two years. They'll rehire when deals return. RPE will revert."

---

### Slide 4 — The safety net is gone [ALL]

**TITLE**: The bench that absorbed delivery risk has been systematically eliminated

**ON SLIDE**:
- Bench as % of headcount: 10-15% → 2-5%
- Utilization rates: 70-75% → 83-86%
- TCS: 35-day bench rule — unassigned engineers retrained or exited

**VISUAL DIRECTION**: Before/after comparison. Two simple gauges or a shift diagram showing the compression. This should feel like pressure building.

**SPEAKER NOTES**: "Services firms used to absorb delivery risk through bench — idle people you could throw at a project when it slipped. That buffer is gone. Every project now has to hit its time-to-value target with no margin for error and no spare people. This isn't a choice they made for efficiency. It's a response to margin pressure. The safety net has been cut to protect the economics — but the economics haven't actually improved."

---

### Slide 5 — Deal structures are compressing [ALL]

**TITLE**: Customers want $150K AI projects; the firms serving them can't deliver below $3M profitably

**ON SLIDE**:
- Three forces:
  1. Shorter commitments (annual renewals replacing multi-year lock-ins)
  2. Smaller, faster AI engagements ($150K-$300K alongside existing contracts)
  3. Organizational overhead per deal is constant regardless of deal size
- Callout: "The cost of processing a $300K deal through sales, legal, compliance, and pre-sales approaches the cost of processing a $30M deal."

**VISUAL DIRECTION**: A cost-per-deal diagram showing overhead as a flat bar while deal size shrinks. The shrinking deal size against constant overhead creates a visual squeeze. This should feel like a trap closing.

**SPEAKER NOTES**: "A sales engineer at a major cloud platform told us this directly: their largest enterprise client now regularly requests $150K-$300K AI projects alongside existing multi-million dollar contracts. The firm cannot profitably serve them. But the client implies a bigger deal will follow, so refusing isn't an option. They're caught between a cost structure they can't flex and a market they can't ignore. This is not one firm's problem. This is the industry."

---

### Slide 6 — The market has already repriced [ALL]

**TITLE**: This is not a prediction — the public markets are pricing it in now

**ON SLIDE**:
- Stock reactions on AI agent launches (single session):
  - Infosys ADRs: -8.4%
  - Nifty IT index: -6%
  - Wipro: -4.5%
  - Cognizant: ~-10%
- Hiring collapse: TCS cut 11,000 in one quarter. Big Four historically hired 10,000+/quarter.
- Revenue growth: dropped from 15-20% to low single digits

**VISUAL DIRECTION**: This is a "the market agrees with us" slide. Stock ticker-style waterfall showing the drops. Red. Below it, hiring data as a simple bar chart showing the collapse. This should feel like evidence, not argument.

**SPEAKER NOTES**: "When capable AI agents launched in early 2025, the market's response was immediate. The entire IT outsourcing model is labour arbitrage — hire at $15/hour, bill at $80/hour. The market saw AI agents and immediately repriced the stocks. Revenue won't fall off a cliff — multi-year contracts protect the near term. But the trajectory is clear: eight to ten quarters of consensus estimates trimmed by two to three percent each cycle. A slow bleed, not a sudden collapse. The firms know this. Their stock prices know this. Their hiring plans know this."

---

# SECTION B: THE INSIGHT

*Arc position: Insight*
*Purpose: Reframe the problem. Introduce friction per unit of revenue. Show why the standard responses fail.*

---

### Slide 7 — AI tools for engineers don't fix the structural problem [ALL]

**TITLE**: Making engineers faster doesn't make the firm faster — the bottleneck just moves

**ON SLIDE**:
- Pipeline diagram: Pre-sales → Legal → Compliance → Staffing → **Engineering** → QA → PM → Delivery
- Engineering highlighted as "the stage AI tools address"
- Everything else unchanged
- Callout: "Grant 10x engineering speed. The bottleneck moves to legal. Then compliance. Then pre-sales. Friction per unit of revenue stays the same."

**VISUAL DIRECTION**: A horizontal pipeline/flow with one stage lit up (engineering) and the rest greyed out. The visual should make the point instantly: one node is fast, the rest are unchanged. Consider arrows showing the bottleneck moving downstream.

**SPEAKER NOTES**: "The standard response from every IT services firm: give engineers AI tools. Copilot, Cursor, Devin. Announce AI transformation. But this addresses one node in a multi-node pipeline. Even granting the most optimistic productivity claims — 2x, 5x, 10x — everything upstream and downstream stays the same speed. The firm doesn't get faster. Individual engineers get faster. The distinction matters. The question isn't whether AI tools help developers. Assume they do. The question is whether developer productivity was ever the binding constraint. In most IT services engagements, it was not."

---

### Slide 8 — The metric that matters is friction per unit of revenue [ALL]

**TITLE**: 35-50% of delivery cost is organizational friction, not engineering

**ON SLIDE**:
- Cost breakdown of a typical IT services project:
  - Engineering: 50-65%
  - Organizational friction: 35-50% (selling, scoping, legal, compliance, staffing, PM, knowledge transfer, documentation, renewal)
- Definition: **Friction per unit of revenue** = total cost (time + money) to move $1 from first conversation to delivered outcome
- Source: APQC benchmarks; Accenture SG&A ~17% of revenue before delivery costs

**VISUAL DIRECTION**: A split bar or pie showing the engineering vs. friction ratio. The friction portion should be broken into its components (legal, compliance, PM, etc.) to show how many separate stages contribute. This is the "aha" visual — the audience should see where their money actually goes.

**SPEAKER NOTES**: "Revenue per employee tells you how productive your people are. It doesn't tell you how efficient your organization is at converting opportunity into delivered revenue. The metric that matters is friction per unit of revenue. For a typical IT services project, engineering represents only 50-65% of total cost. The rest — selling, scoping, legal, compliance, staffing, project management, knowledge transfer — is organizational friction. The firms announcing AI transformation by giving engineers Copilot are optimizing the minority of their cost structure while ignoring the majority."

---

### Slide 9 — The firm that minimizes friction wins at every deal size [ALL]

**TITLE**: Minimize friction per unit of revenue and you can profitably serve $30K and $30M with the same margin

**ON SLIDE**:
- Two models compared:
  - **Traditional**: Overhead per deal is constant → unprofitable below threshold → optimized for deal size
  - **Low-friction**: Overhead per deal scales with deal → profitable at any size → optimized for deal velocity
- Callout: "Deal frequency is rising. Deal size is falling. The firm optimized for velocity, not size, has a structural advantage that compounds with every deal closed."

**VISUAL DIRECTION**: Two curves on the same axis. X-axis: deal size. Y-axis: profitability. Traditional model goes negative below a threshold. Low-friction model stays profitable across the range. The gap between the curves is the structural advantage.

**SPEAKER NOTES**: "The implication is a fundamental reorientation. The economics of the old model — optimize delivery cost on a large, stable contract — don't transfer to a world where deal frequency is rising and deal size is falling. A firm that can move a $30K deal through its full pipeline at the same speed and margin as a $3M deal has a structural advantage. And that advantage compounds with every deal closed."

---

### Slide 10 — Incumbents cannot buy their way out [INVESTOR]

**TITLE**: $3B in AI spend doesn't fix a structural problem — Accenture's model requires the friction it's trying to eliminate

**ON SLIDE**:
- Accenture: $3B AI commitment, 31+ acquisitions/year
- Three things incumbents are actually doing:
  1. Procuring AI tools for engineers → relocates bottleneck
  2. Rebranding existing revenue as "AI consulting" → optics
  3. Acquiring AI startups → integrating into incompatible operating structures
- Callout: "A container shipping company cannot pivot to same-day drone delivery by buying drones."

**VISUAL DIRECTION**: Three columns showing the three incumbent responses, each with a red "X" or strike-through showing why it fails. The analogy at the bottom as a pull-quote. This should feel decisive, not dismissive.

**SPEAKER NOTES**: "Accenture has committed $3B to AI and acquires 31+ companies a year. Surely scale and capital can close this gap. It cannot. The problem is structural, not financial. An operation built to sell 10,000 junior developers at $30/hour is a volume business. The entire organizational infrastructure — campuses, training pipelines, bench management — exists to support labour arbitrage at scale. You cannot repurpose this into high-leverage AI-native delivery any more than a container shipping company can pivot to same-day drone delivery by buying drones."

---

# SECTION C: THE SHIFT

*Arc position: Insight → Resolution bridge*
*Purpose: Show where value is migrating. Introduce the three-layer stack and context layer.*

---

### Slide 11 — The enterprise tech stack is restructuring into three layers [ALL]

**TITLE**: Infrastructure commoditizes. Applications compress. A new layer — the context layer — emerges as the value center.

**ON SLIDE**:
- Three-layer stack diagram:
  - **Layer 1 — Infrastructure** (APIs, databases, auth, monitoring): Commoditizing. AI agents consume 100x more API calls than humans. Cheaper per unit, higher volume.
  - **Layer 2 — Applications** (CRMs, dashboards, project management): Compressing. $300B+ market cap lost. SaaS growth halved from 36% to 17%. Switching costs dissolving.
  - **Layer 3 — Context Layer** (NEW): Institutional knowledge directing AI agents. Who accesses what data. What sequences complete which workflows. How decisions get made in practice.

**VISUAL DIRECTION**: Vertical three-layer stack. Bottom layer (infrastructure) shown as foundation — stable but commoditizing. Middle layer (applications) shown as being squeezed from both directions (pincer arrows). Top layer (context) shown as expanding, glowing, or highlighted as the emerging value center. This is the key framework visual — it should be clear, memorable, and reusable.

**SPEAKER NOTES**: "Clayton Christensen's Law of Conservation of Attractive Profits: when one layer commoditizes, adjacent layers de-commoditize. Infrastructure is commoditizing — AI agents generate hundreds of API calls per minute versus a human generating dozens per hour. Applications are compressing — SaaS companies have lost over $300 billion in market cap, growth has halved, switching costs are dissolving as LLMs make data migration trivial. The context layer is what emerges. It's the institutional knowledge that directs AI agents — it doesn't live in a document. It emerges from thousands of workflows executed over time. This is where value concentrates."

---

### Slide 12 — Most firms deploy AI in the wrong layer [ALL]

**TITLE**: Firms deploy AI in products and for building products — almost none deploy AI to run the company

**ON SLIDE**:
- Three deployment modes:
  1. AI in the product you sell ← most firms focus here
  2. AI for building the product ← second priority
  3. **AI to run the company** ← where structural economics change. Almost no one does this.
- Callout: "If friction per unit of revenue is the metric, AI at one stage is not the solution. AI across the entire pipeline is."

**VISUAL DIRECTION**: Three horizontal bars or paths. First two populated with logos of well-known companies. Third one nearly empty — with realfast as the standout. This should create the "white space" impression.

**SPEAKER NOTES**: "There are three ways to deploy AI. In the product. For building the product. And to run the company. Most firms are focused on the first two. Very few are addressing the third. But the third is where the structural economics change. Sales must move faster. Pre-sales must scope in days, not weeks. Legal must review in hours. Compliance must clear in a single pass. Knowledge must transfer automatically, not through meetings. No IT services firm is structured to build this. Their teams are organized by function, not by flow. Their tooling is procured per function. There is no connective tissue."

---

# SECTION D: THE RESOLUTION

*Arc position: Resolution*
*Purpose: Introduce realfast and Exocortex as the answer to the structural problem.*

---

### Slide 13 — realfast is built on this thesis [ALL]

**TITLE**: Every function at realfast — pre-sales, delivery, operations, recruitment — runs on a single AI operating system

**ON SLIDE**:
- Exocortex pipeline diagram showing AI spanning the full pipeline:
  - Pre-sales → Scoping → Legal → Compliance → Staffing → Delivery → Optimization → Knowledge capture
  - All connected by Exocortex as the connective tissue
- Contrast with traditional model (siloed functions, manual handoffs)

**VISUAL DIRECTION**: Two rows. Top row: traditional model with disconnected function boxes and manual handoff arrows (friction points highlighted). Bottom row: realfast model with the same functions connected through a single Exocortex layer — smooth, continuous flow. The visual should make "integrated vs. fragmented" instantly obvious.

**SPEAKER NOTES**: "realfast is built on this thesis. Every function in the company runs on Exocortex — an AI operating system that spans the full pipeline. This is not a set of AI tools bolted onto existing processes. It is the operating infrastructure that connects everything. The connective tissue that traditional firms don't have."

---

### Slide 14 — Exocortex is our implementation of the context layer [ALL]

**TITLE**: Exocortex extracts institutional knowledge, maintains it as the business evolves, and applies it across every workflow

**ON SLIDE**:
- Three functions:
  1. **Extract**: Institutional knowledge from people, contracts, past projects, domain expertise
  2. **Maintain**: Continuously re-engineer processes as we learn what works
  3. **Apply**: Across workflows — whoever needs it, whenever they need it
- Callout: "The system gets smarter by doing work, not by being trained."

**VISUAL DIRECTION**: A cycle or flywheel diagram showing Extract → Maintain → Apply → (feeds back to Extract). Each node should have a brief example. The flywheel should convey continuous improvement, not a one-time setup.

**SPEAKER NOTES**: "Exocortex does three things. It extracts institutional knowledge from people, contracts, past projects, and domain expertise. It maintains that knowledge as the business evolves — continuously re-engineering processes as we learn what works. And it applies it across every workflow, for whoever needs it. Each engagement generates execution traces — granular records of what worked, what failed, what took longer than expected, what the client actually needed versus what the SOW described. These traces feed the next engagement. The system gets smarter by doing work, not by being trained."

---

### Slide 15 — The economic mechanism: eliminating coordination overhead [ALL]

**TITLE**: Coordination overhead is 35-50% of delivery cost — Exocortex structurally eliminates it, delivering 2-3x margin improvement

**ON SLIDE**:
- Before/after comparison:
  - **Before** (traditional): PM, BA, architect, developer, QA — each handing off to the next. Coordination overhead: 35-50%.
  - **After** (realfast): Consultants deliver independently. Knowledge available system-wide. Coordination overhead: structurally eliminated.
- Result: "Not a 10% efficiency gain. A 2-3x margin improvement on transformed workflows."

**VISUAL DIRECTION**: Two side-by-side delivery models. Traditional model shows many role boxes with handoff arrows (busy, complex). realfast model shows fewer roles with direct connections through Exocortex (clean, simple). Cost bar below each showing the margin difference.

**SPEAKER NOTES**: "The economic mechanism is specific. Coordination overhead in a typical project — project management, status alignment, knowledge transfer, cross-timezone handoffs, role-dependency wait times — represents 35-50% of total delivery cost. These aren't engineering costs. They're organizational costs. They show up in payroll budgets, not IT budgets. Exocortex doesn't optimize this overhead. It structurally eliminates it. Consultants who previously needed dedicated developers, PMs, and BAs can now deliver independently. The result is not a 10% gain. It's a 2-3x margin improvement."

---

### Slide 16 — Every project makes the next one faster [ALL]

**TITLE**: Domain knowledge, workflow patterns, and delivery playbooks compound in Exocortex — they don't walk out the door when the team disbands

**ON SLIDE**:
- Compounding curve: Project 1 → Project 2 → Project 3 → ... with each taking less time/cost
- Three flywheels:
  1. **Data**: More deployments → more workflow data → better outcomes → more referrals
  2. **Efficiency**: More usage → more optimization → faster/cheaper delivery → better margins
  3. **Playbooks**: More patterns encoded → FDEs deploy faster → higher capacity per person
- Callout: "Traditional services firms get linearly better. We get exponentially better."

**VISUAL DIRECTION**: A compounding curve (not linear) showing cost-per-project declining over time. Below or alongside, three small flywheel icons with labels. The curve should convey momentum and acceleration.

**SPEAKER NOTES**: "Every project completed makes the next one faster. In a traditional firm, knowledge dissipates when the team disbands. In our model, domain knowledge, workflow patterns, and client-specific context compound in Exocortex. The second project is faster than the first. The third is faster than the second. This is not true for traditional services firms. Their delivery quality is a function of whoever they happen to staff. Ours is a function of every engagement we've ever delivered."

---

# SECTION E: PROOF POINTS

*Arc position: Resolution (evidence)*
*Purpose: Demonstrate that this is not theoretical. Show results, team, and backing.*

---

### Slide 17 — Client results prove the model [ALL]

**TITLE**: Production results across industries — not demos, not pilots, not proofs of concept

**ON SLIDE**:

| Client | Result | Context |
|---|---|---|
| **TASC** | 3.5x improvement in qualified leads (799 → 2,818/month) | AI agents for recruitment pipeline. Featured Salesforce customer story. |
| **Houzbay** | 30% conversion rate on lead generation | AI agent — nearly 1 in 3 users qualified as a lead |
| **Flok** | 5 business days to production | Complex Agentforce implementation |

- Quote: *"It's like hiring 3 quality SDRs to drive pipeline without adding headcount."* — Sudheer Noohu, CTO, TASC

**VISUAL DIRECTION**: Three case study cards side by side. Each with the metric large and prominent, company name, one-line context. The TASC quote as a pull-quote below. These should feel like verified outcomes, not marketing claims.

**SPEAKER NOTES**: "These are production results. TASC went from 799 leads in June to 2,818 in July — 3.5x improvement while maintaining conversation quality. Their CTO said it's like hiring 3 quality SDRs without adding headcount. Houzbay's lead gen agent hit 30% conversion — nearly one in three users qualifying. Flok went from kickoff to production in 5 business days on a complex Agentforce implementation. These prove delivery speed and outcome quality. What they also prove — though it's not on the slide — is that each of these engagements fed the next. The TASC patterns informed how we approached Houzbay. Houzbay informed Flok. The compounding is already happening."

---

### Slide 18 — The team and backing [ALL]

**TITLE**: Founded by operators who've built at decacorn scale, backed by Peak XV (Sequoia India) and RTP Global

**ON SLIDE**:
- Founders:
  - **Sidu Ponnappa** — CEO, Co-Founder. [Background summary]
  - **Aakash Dharmadhikari** — CPTO, Co-Founder. [Background summary]
  - **Steve Sule** — CFO, Co-Founder. [Background summary]
- Investors: Peak XV Partners (formerly Sequoia India & SE Asia), RTP Global
- Tagline: "Decades of software engineering, blitzscaling to decacorn scale, and billion-dollar M&A — now channeled into building the AI-native IT services company we always wanted to work at."

**VISUAL DIRECTION**: Clean founder photos with 1-2 line credentials. Investor logos prominent. This is a credibility slide — it should feel like "serious people, serious backing, serious ambition." Not flashy.

**SPEAKER NOTES**: "[Personalize based on presenter. Key beats: relevant scale experience, domain credibility, why this team is uniquely positioned to build this.]"

---

### Slide 19 — realfast's own economics [INVESTOR]

**TITLE**: [PLACEHOLDER — To be populated with realfast's own RPE, margin data, and unit economics]

**ON SLIDE**:
- realfast RPE vs. industry benchmark ($50K)
- Margin profile by engagement type
- Revenue per FDE trend over time
- Cost-to-serve trend (should be declining)

**VISUAL DIRECTION**: This is the "we eat our own cooking" slide. Hard numbers. No narrative. The data should speak. Consider a simple comparison: industry RPE flat vs. realfast RPE trajectory.

**SPEAKER NOTES**: "If we're making this argument about the industry, we need to show our own numbers. This is the most powerful proof point available. [Populate when data is ready.]"

*Note: This slide is flagged as an open gap in Master Narrative v0.4, Open Question #3.*

---

# SECTION F: RISK MITIGATION + MOAT

*Arc position: Risk Mitigation*
*Purpose: Show that downside is capped, upside is asymmetric, and the model is defensible.*

---

### Slide 20 — We start narrow and prove the delta before expanding [ENTERPRISE]

**TITLE**: One workflow. One business metric. 3-6 weeks to production. If we don't prove the delta, you know quickly and cheaply.

**ON SLIDE**:
- The engagement arc:
  1. **Start narrow**: One workflow, one metric, 3-6 weeks
  2. **Prove the delta**: Measurable gap in time, cost, quality vs. what a traditional firm would deliver
  3. **Expand**: Second project, third project — each faster, each compounding
  4. **End state**: Operational intelligence layer tuned to your business
- Risk framing: "If we fail, you know in 3-6 weeks with minimal investment. If we succeed, you have a measurable advantage that compounds."

**VISUAL DIRECTION**: A horizontal progression from narrow (single dot) to wide (full pipeline). Each stage should feel like a natural expansion, not a big leap. The risk framing should be visually prominent — capped downside, expanding upside.

**SPEAKER NOTES**: "We don't ask you to bet on a vision. We ask you to bet on one workflow. One business metric. 3-6 weeks. We prove the delta — time, cost, quality — against what you would have gotten from the firm you were about to hire. If we fail, you know quickly and cheaply. If we succeed, you have a decision to make about your next project. And every engagement compounds. The second project is faster than the first. The third is faster than the second. Over time, what you're building with us is not a series of disconnected implementations — it's an operational intelligence layer tuned to your business."

---

### Slide 21 — Your competitors will hire Accenture — and get Accenture's cost structure [ENTERPRISE]

**TITLE**: The firm that moves first on a structurally better model compounds the advantage with every project — the gap widens, not closes

**ON SLIDE**:
- Two diverging lines:
  - **Competitor path**: Accenture cost structure, Accenture timeline, Accenture coordination overhead. Linear improvement.
  - **Your path**: Compounding operating leverage. Each project faster and cheaper than the last.
- Callout: "Nobody gets fired for hiring Accenture. But the firm that moves first compounds the advantage. The gap between you and your competitors does not stay constant."

**VISUAL DIRECTION**: Two lines diverging over time. One linear (competitor), one curving upward (you with realfast). The widening gap is the visual story. This should create urgency without fear.

**SPEAKER NOTES**: "Your competitors will hire Accenture. They'll get Accenture's cost structure, timeline, and coordination overhead. Nobody gets fired for that decision. But here's what that decision costs: every project they do with a traditional firm is a standalone engagement. No compounding. No operational intelligence accumulating. You, on the other hand, build compound advantage with every engagement. The gap doesn't stay constant. It widens."

---

### Slide 22 — Four structural barriers prevent replication [INVESTOR]

**TITLE**: Competitors starting today are not behind on technology — they're behind on thousands of accumulated workflow traces

**ON SLIDE**:
1. **Extraction problem**: The context layer must be built through doing, not through buying. It emerges from thousands of workflows executed.
2. **Adoption problem**: Conviction drives adoption, not training. You deliver undeniable results first.
3. **Compounding problem**: Every engagement generates execution traces encoding organizational decision logic. The gap widens with every project.
4. **Infrastructure mismatch**: Incumbents cannot build this without dismantling the infrastructure that generates their current revenue.

**VISUAL DIRECTION**: Four barrier icons or shields, each with a one-line label and one-line explanation. These should feel like walls, not talking points. Solid, structural, permanent.

**SPEAKER NOTES**: "This is not a technology moat — it's an operational moat. A competitor starting today is not just behind on code. They're behind on thousands of accumulated workflow traces that encode how workflows actually behave in practice. Which deals stall at legal review. Which client stakeholders need early alignment. Which compliance requirements are blocking versus procedural. This gap widens with every project we deliver. And the incumbents? They can't build this without dismantling the organizational infrastructure that generates their current revenue. The firms with the most to gain from this transition are the ones least able to execute it."

---

### Slide 23 — The client-side thesis: the end state is their own operating leverage [INVESTOR]

**TITLE**: Quick wins delivered through Exocortex compound into the client's own context layer — the long-term opportunity is transforming how services organizations operate

**ON SLIDE**:
- Progression:
  1. Deliver work through Exocortex (client sees speed/cost delta)
  2. Work compounds — domain knowledge, workflows, institutional context accumulate
  3. Client realizes they have an operational intelligence layer forming around their business
  4. End state: client runs on the same operating leverage realfast does
- Callout: "We don't sell Exocortex. We deliver through it. The platform thesis is an emergent outcome, not a sales pitch."

**VISUAL DIRECTION**: A stepped progression showing the Trojan horse arc. Each step feels natural and earned, not like a bait-and-switch. The end state (client with their own context layer) should feel aspirational and valuable.

**SPEAKER NOTES**: "This is the second-order opportunity. Every engagement we deliver through Exocortex compounds context about the client's business. Over time, what they're building with us — without buying anything — is an operational intelligence layer tuned to their domain, their workflows, their institutional knowledge. The end state is not permanent dependency on realfast. It's their organization running on the same operating leverage we do. We don't sell Exocortex. We deliver through it. The platform thesis is an emergent outcome, not a sales pitch. This shifts our commercial model from subcontracting at better margins to transforming how services organizations operate."

---

### Slide 24 — The technology stack powering this [ALL]

**TITLE**: Exocortex is enterprise-grade, ISO 27001 and SOC 2 compliant, and operational at scale today

**ON SLIDE**:
- Platform components:
  - **ExoCode**: AI-native development environment
  - **ExoWork**: Non-technical workflow automation
  - **ExoManager**: Delivery management and oversight
  - **ExoHelpdesk**: Managed services frontend
  - **ExoMetacog**: Agent usage analytics and optimization
- Security: ISO 27001 certified, SOC 2 compliant
- Callout: "Not vaporware. Running our own operations at production scale."

**VISUAL DIRECTION**: Component architecture diagram — clean, modular, showing how pieces connect. Security badges prominent. This is the "it's real and it's hardened" slide. Confidence, not complexity.

**SPEAKER NOTES**: "This is not a prototype. Exocortex runs our operations today. Every engagement we've delivered — TASC, Houzbay, Flok — was delivered through this platform. It's ISO 27001 certified, SOC 2 compliant, and enterprise-grade. Five components working together: ExoCode for developers, ExoWork for business workflows, ExoManager for delivery oversight, ExoHelpdesk for managed services, ExoMetacog for analytics. All instrumented for full observability."

---

# SECTION G: THE ASK

*Arc position: Clear Ask*
*Purpose: One decision. Unambiguous.*

---

### Slide 25 — The investment thesis [INVESTOR]

**TITLE**: AI is restructuring IT services — realfast has built the platform to be the efficient winner in that restructuring

**ON SLIDE**:
- Thesis in three lines:
  1. **What we are**: A services company that delivers through a platform — converting implementations into compounding operational leverage
  2. **What compounds**: Data, platform efficiency, playbooks, client context — all three make us better with every engagement
  3. **What capital unlocks**: Distribution (partner hires + acquisitions) to short-circuit GTM and consolidate a fragmented market
- Exit paths: Strategic acquisition by large SI | PE roll-up of recurring managed services | Continue scaling

**VISUAL DIRECTION**: Clean, summary-level. Three lines of thesis, three exit paths. This is the "here's why you should write the check" slide. No clutter. Conviction.

**SPEAKER NOTES**: "Three things to remember. We are a services company that delivers through a platform — every engagement compounds. Capital unlocks distribution — partner hires with CXO rolodexes and SI acquisitions for client relationships. The exit math works three ways: strategic acquisition by a large SI that wants our operating model, PE roll-up of recurring managed services revenue, or continued scaling. The bet you're making is that AI will restructure IT services and we've built the platform to be the efficient winner in that restructuring."

---

### Slide 26 — Use of funds and milestones [INVESTOR]

**TITLE**: [PLACEHOLDER — Capital allocation and 12-18 month milestones]

**ON SLIDE**:

| Allocation | Purpose |
|---|---|
| Partner hires | 2-3 senior hires with CXO relationships |
| Acquisition | 1-2 small SI acquisitions for distribution |
| Platform development | Accelerate Exocortex roadmap |
| Geographic expansion | Replicate Singapore model in [markets] |

| Milestone | Target | Timeframe |
|---|---|---|
| Managed services ARR | $[X] | 12 months |
| Clients on platform | [X] | 12 months |
| First acquisition integrated | 1 | 18 months |

**VISUAL DIRECTION**: Clean allocation table + milestone table. Numbers must be specific when populated. This is the accountability slide — it should feel concrete and achievable.

**SPEAKER NOTES**: "[Populate with specific numbers. This slide converts conviction into commitment. Every number must be defensible.]"

*Note: Amounts and targets to be finalized.*

---

### Slide 27 — The enterprise pilot proposal [ENTERPRISE]

**TITLE**: Prove the delta on one workflow in 3-6 weeks — if we don't deliver measurably better results, you've lost weeks, not months

**ON SLIDE**:
- The proposal:
  - **Scope**: One workflow. One business metric.
  - **Timeline**: 3-6 weeks to production
  - **Measurement**: Time, cost, and quality delta vs. your current vendor/approach
  - **Risk**: Capped at [weeks] and [$amount]. No multi-year commitment. No procurement cycle.
- CTA: "Book a discovery call. We'll identify the workflow and the metric in the first conversation."

**VISUAL DIRECTION**: Simple, direct. This should feel like a low-risk, high-clarity proposal. No fine print energy. One decision: try us on one thing.

**SPEAKER NOTES**: "One workflow. One metric. 3-6 weeks. We prove we can deliver the same outcome — production-grade, enterprise-quality — at a fundamentally different speed and cost. If we fail, you know in weeks with minimal investment. If we succeed, you have a measurable gap and a decision to make about your next project. There's no procurement cycle. No multi-year commitment. Just a focused test of whether a structurally different operating model delivers what the traditional firms can't."

---

# APPENDIX

*Purpose: Defend any analytical challenge instantly. Never shown proactively — pulled when challenged.*

---

### Appendix A — RPE Data Detail [INVESTOR]

**ON SLIDE**: Full RPE table with sources, TCS revenue/headcount breakdown, Infosys FY24-FY25 headcount reduction detail, ~57,900 job cuts across top five firms.

---

### Appendix B — Bench and Utilization Data [INVESTOR]

**ON SLIDE**: Bench percentage trends (10-15% → 2-5%), utilization rate convergence (70-75% → 83-86%), TCS 35-day bench rule, sources.

---

### Appendix C — Market Repricing Evidence [ALL]

**ON SLIDE**: Full stock price data (Infosys ADR -8.4%, Nifty IT -6%, Wipro -4.5%, Cognizant ~-10%), hiring collapse data, revenue growth deceleration, 8-10 quarter bleed thesis.

---

### Appendix D — Accenture Structural Analysis [INVESTOR]

**ON SLIDE**: SG&A at ~17% of revenue, $3B AI commitment breakdown, 31+ acquisitions/year, why capital doesn't solve a structural problem.

---

### Appendix E — Three-Layer Stack Deep Dive [ALL]

**ON SLIDE**: Detailed breakdown of each layer with examples, market data ($300B SaaS market cap loss, growth halving from 36% to 17%), Christensen's Law of Conservation of Attractive Profits explained.

---

### Appendix F — Exocortex Architecture [ALL]

**ON SLIDE**: Full component diagram — ExoCode, ExoWork, ExoManager, ExoHelpdesk, ExoMetacog. How they connect. Technology stack. Compliance certifications.

---

### Appendix G — Full Case Studies [ENTERPRISE]

**ON SLIDE**: TASC full case study (before/after metrics, timeline, approach). Houzbay full case study. Flok full case study. Include direct quotes from each client CXO.

---

### Appendix H — Competitive Landscape — Context Layer [INVESTOR]

**ON SLIDE**: Who else is pursuing context layer ownership: ServiceNow (workflow penetration), Notion (documentation layer), Glean (enterprise search → context), OpenAI (semantic OS), Anthropic (agent deployment). Why realfast's "built through doing" path is differentiated — context layer must be built through workflow execution, not data aggregation.

---

### Appendix I — Deal Structure Compression Evidence [ALL]

**ON SLIDE**: Cloud data platform anecdote detail. Three compression forces with supporting signals. Friction-per-deal-vs-deal-size analysis.

---

### Appendix J — IT Services Firm Transformation Thesis [IT SERVICES]

**ON SLIDE**: How the operating leverage transfers to services firms. Engagement model: prove delta on their own work, then scale. Not a software sale — an operational transformation.

---

## Slide Title Sequence (Read-Through Test)

*Per the persona: if someone reads only the slide titles, they must understand and agree with the argument.*

1. realfast
2. IT services is a trillion-dollar industry running on a model that hasn't improved in a decade
3. IT services revenue per employee has been flat to declining for a decade
4. The bench that absorbed delivery risk has been systematically eliminated
5. Customers want $150K AI projects; the firms serving them can't deliver below $3M profitably
6. This is not a prediction — the public markets are pricing it in now
7. Making engineers faster doesn't make the firm faster — the bottleneck just moves
8. 35-50% of delivery cost is organizational friction, not engineering
9. Minimize friction per unit of revenue and you can profitably serve $30K and $30M with the same margin
10. $3B in AI spend doesn't fix a structural problem — Accenture's model requires the friction it's trying to eliminate
11. Infrastructure commoditizes. Applications compress. A new layer — the context layer — emerges as the value center.
12. Firms deploy AI in products and for building products — almost none deploy AI to run the company
13. Every function at realfast — pre-sales, delivery, operations, recruitment — runs on a single AI operating system
14. Exocortex extracts institutional knowledge, maintains it as the business evolves, and applies it across every workflow
15. Coordination overhead is 35-50% of delivery cost — Exocortex structurally eliminates it, delivering 2-3x margin improvement
16. Domain knowledge, workflow patterns, and delivery playbooks compound in Exocortex — they don't walk out the door when the team disbands
17. Production results across industries — not demos, not pilots, not proofs of concept
18. Founded by operators who've built at decacorn scale, backed by Peak XV (Sequoia India) and RTP Global
19. [PLACEHOLDER — realfast's own RPE, margin data, unit economics]
20. One workflow. One business metric. 3-6 weeks to production. If we don't prove the delta, you know quickly and cheaply.
21. The firm that moves first on a structurally better model compounds the advantage with every project — the gap widens, not closes
22. Competitors starting today are not behind on technology — they're behind on thousands of accumulated workflow traces
23. Quick wins delivered through Exocortex compound into the client's own context layer — the long-term opportunity is transforming how services organizations operate
24. Exocortex is enterprise-grade, ISO 27001 and SOC 2 compliant, and operational at scale today
25. AI is restructuring IT services — realfast has built the platform to be the efficient winner in that restructuring
26. [PLACEHOLDER — Capital allocation and milestones]
27. Prove the delta on one workflow in 3-6 weeks — if we don't deliver measurably better results, you've lost weeks, not months

---

*Document Version: v1.0*
*Source: Master Narrative v0.4*
*Persona: Strategic Narrative Architect*
*Last Updated: February 2026*
