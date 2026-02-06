# Engineering Context Brief: Sam Steele Client

**Source:** Kickoff call transcript (February 6)
**Status:** Pre-engagement
**Purpose:** Provide context for engineering team to develop solution approach

---

## 1. What We Heard

Sam described a client engagement during the kickoff call. The following is extracted directly from that conversation.

### The Client

- Recruitment company in the aged care space
- Operates as intermediary between aged care homes and contractors (nurses)
- Onboards candidates to build a pool of nurses for deployment into contracts won across aged care facilities

### The Problem (Sam's Words)

> *"They have a flow that when you get a candidate, they come through, you have to vet them, check them, talk to them. And then there's a list of compliance documents that need to be checked. Like, do they have their nursing degree? Do they have their qualifications? Have they got certain vaccines? And that's a very time-consuming manual activity at the moment."*

> *"That challenge is something that they spend ages on at the moment. And they're wondering whether that can be automated."*

### Engagement Status

- Budget exists for this problem
- Sam has a working session with them early next week

---

## 2. Information We Have

| Item | Detail | Source |
|------|--------|--------|
| Industry | Aged care recruitment | Transcript |
| Business model | Intermediary between aged care facilities and nurse contractors | Transcript |
| Core function | Onboard candidates into deployment-ready pool | Transcript |
| Identified bottleneck | Compliance document verification | Transcript |
| Known checklist items | Nursing degree, qualifications, vaccines | Transcript |
| Process characteristic | Manual, time-consuming | Transcript |
| Budget | Exists | Transcript |

---

## 3. Information We Do Not Have

| Gap |
|-----|
| Complete compliance checklist |
| Document formats |
| Current time per candidate |
| Current throughput volume |
| Cost of current process |
| Error/rejection rates |
| Systems in use |
| Whether verification requires external sources |

---

## 4. Business Context (External Research)

### Role of Aged Care Staffing Intermediary

An aged care staffing agency operates as a compliance-wrapped talent supply chain:

- **Source** candidates (nurses)
- **Vet** credentials and compliance
- **Supply** deployment-ready candidates to facilities on demand

The value to aged care facilities: *"We handle sourcing, vetting, compliance. You get qualified nurses when you need them."*

### Recruitment Agency Value Drivers

| Metric | Description |
|--------|-------------|
| Fill Rate | % of roles successfully filled |
| Time to Fill | Speed from request to placement |
| Cost Per Hire | Efficiency of placement process |
| Quality of Hire | Placement success over time |
| Gross Margin | Revenue minus direct costs (industry: 20-30%) |

Compliance verification sits between sourcing and deployment. A bottleneck here impacts Time to Fill and Fill Rate — both directly tied to revenue.

---

## 5. The Objective

From our discussion:

| Metric | Target |
|--------|--------|
| **Verification quality** | >= Current human standard |
| **Processing speed** | > Current human speed |

The goal is not automation for its own sake. The goal is:
1. Maintain or exceed current verification rigor (no compliance gaps)
2. Reduce time per candidate

---

## 6. How We Think About AI Opportunities

### Diagnostic Framework: Automate / Augment / Connect

Before applying AI, we classify *why* execution slows down. This helps identify where AI is likely to deliver value.

| Category | Indicator |
|----------|-----------|
| **AUTOMATE** | Humans doing repetitive, rules-based, high-volume tasks |
| **AUGMENT** | Humans lack decision support — incomplete info, manual analysis |
| **CONNECT** | Systems/data don't talk — manual reconciliation, slow handoffs |

This is a classification lens, not a prescriptive solution. The problem dictates the approach.

### Guiding Principles

How we approach engagements:

- Start narrow, prove value, expand what works
- No speculative pilots — measurable outcomes required
- No scale without proof

### Where We Prioritize

We look for initiatives with:

| Criteria | This Problem |
|----------|--------------|
| **Direct business metrics** | Time to Fill, Fill Rate — both directly tied to placement revenue |
| **Repeatable workflows** | Same compliance checklist applied to every candidate |
| **Existing data** | Documents already submitted; checklist already defined |

**Assessment:** This problem fits our prioritization criteria. The workflow is repeatable, the data exists, and the business metric link is clear.

---

## 7. What Engineering Needs to Produce

Using this context and our diagnostic framework:

1. **Classification** — Where does this problem sit in Automate/Augment/Connect?
2. **Proposed approach** — How would we tackle this?
3. **Metric selection** — What single metric would we target to prove value?
4. **Proof mechanism** — How would we demonstrate success?
5. **What we need from the client** — To move from assessment to pilot

This will form the basis of the external plan we share with Sam.

---

**End of Context Brief**
