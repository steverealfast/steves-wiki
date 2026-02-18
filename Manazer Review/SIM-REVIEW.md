# SIM Project Review — Jon Gray CFO Lens

**Review Date:** 2026-02-18
**Data Source:** Manazer MCP + Geetha's Feb 2026 Work Report
**Persona:** Jon Gray — Revenue Architect. Project Economist. Compounding Operator.

---

# Part 1: SIM Delivery (Build Phase)

**Project Created:** 2025-10-30
**Primary Activity Window:** Aug 2025 — Jan 2026 (~6 months)
**Status:** Winding down (61 activities in Feb 2026 vs 3,116 at peak in Nov 2025)

---

## 1.1 Budget vs Actual

| Metric | Value |
|--------|-------|
| Budget (hours) | 193h (11,580 min) |
| Budget ($) | $27,000 |
| Implied rate | ~$140/hr |
| Total activities | 7,909 |
| Total commits | 3,527 |
| Total ClickUp comments | 2,881 |
| Tickets created | 564 |
| Tickets completed | 345 |
| PRs opened | 133 |
| PRs closed | 132 |

### Estimate vs Actual Hours

> **DATA GAP**: Manazer has budget_minutes (193h) and budget_cents ($27,000) but **actual hours burned on delivery are not extracted here.** Need to run `Project#time_report_from_db` for full work session analysis to answer the core question: did we deliver within 193h or not?

**Action Requirok

---

## 1.2 Activity Profile by Month

| Month | Activities | Phase |
|-------|-----------|-------|
| Aug 2025 | 15 | Kickoff/setup |
| Sep 2025 | 317 | Ramp |
| **Oct 2025** | **2,549** | **Peak build** |
| **Nov 2025** | **3,116** | **Peak build** |
| Dec 2025 | 1,323 | Wind-down |
| Jan 2026 | 529 | Transition to MS |
| Feb 2026 | 61 | Residual |

**Observation:** Classic bell curve delivery. 72% of all activity (5,665/7,909) concentrated in Oct-Nov. Sharp drop in Dec suggests either scope completion or holiday effect.

---

## 1.3 Team Size & Composition

**Unique contributors (excluding bots):** ~25+
**Top contributors by activity:**

| Contributor | Activities | Role Signal |
|-------------|-----------|-------------|
| saurav@realfast.ai | 1,143 | Heavy delivery |
| ganesh.hegde@realfast.ai | 1,113 | Heavy delivery |
| bharat@realfast.ai | 983 | Heavy delivery |
| aniket@realfast.ai | 665 | Delivery |
| nikhil.galagali@realfast.ai | 636 | Delivery |
| prabhat.ranjan@realfast.ai | 455 | Delivery |
| sidu@realfast.ai | 435 | Tech Lead / oversight |

### Jon Gray Question: Revenue per Employee

> **With $27,000 budget and 25+ contributors, the revenue per contributor is dangerously thin.** Even assuming only the top 7 were full-time on this, that's ~$3,857 per contributor for a 6-month engagement. This signals either:
> 1. The project was significantly underpriced
> 2. The team was oversized for the scope
> 3. This was a strategic/loss-leader engagement

**Action Required:** Clarify — was SIM delivery priced to be profitable, or was it a strategic land-and-expand play anchored on managed services revenue?

---

## 1.4 Ticket Completion Rate

| Metric | Value |
|--------|-------|
| Tickets created | 564 |
| Tickets completed | 345 |
| **Completion rate** | **61.2%** |

> **339 tickets remain incomplete.** At project wind-down, a 61% completion rate raises the question: were the remaining tickets deprioritized (scope management) or abandoned (delivery failure)? This directly impacts whether the customer perceives value delivery.

---

## 1.5 Jon Gray Non-Negotiable Questions — Delivery

| # | Question | Answer | Status |
|---|----------|--------|--------|
| 1 | Revenue trajectory & constraint? | $27,000 fixed. Constrained by budget hours (193h). | Needs actual hours |
| 2 | Revenue per employee trend? | ~$3,857/contributor if 7 core. Declining if more participated. | Concerning |
| 3 | Project-level contribution margin? | Unknown — need fully-loaded cost data (rates per contributor). | DATA GAP |
| 4 | Estimate vs actual variance? | Budget: 193h. Actual: TBD. | DATA GAP |
| 5 | Is each iteration improving economics? | First engagement — no prior baseline. | N/A |
| 6 | What breaks first under stress? | Team size relative to budget. 25+ people on a $27K project. | Structural risk |
| 7 | Operating leverage over time? | Only if MS phase generates recurring revenue at positive margin. | Depends on Part 2 |

---

# Part 2: SIM Managed Services (Support Phase)

**Project Created:** 2026-01-13
**Status:** Active, ongoing
**Customer Budget:** 20h/month (per Geetha's Feb 2026 report)
**Budget in Manazer:** Not configured (budget_minutes: nil, budget_cents: nil)

---

## 2.1 Budget vs Actual — Feb 1-16, 2026

Source: Geetha's work report (`86d1ztngf-weekly-finance-sim-managed-services`)

| Metric | Hours |
|--------|------:|
| Customer budget (monthly) | 20.00h |
| Actual spent (Feb 1-16) | 40.90h |
| **Overrun** | **-20.90h** |
| **Budget utilization** | **204.5%** |

> **The managed services phase is running at a loss.** In the first 16 days of February, the team consumed 2x the monthly budget. This is not a margin compression problem — this is a **negative contribution margin** engagement.

---

## 2.2 Ticket-Level Variance

| Ticket | Title | Estimate (ClickUp) | Actual (Manazer) | Variance |
|--------|-------|:-------------------:|:-----------------:|:--------:|
| 86d1p9d97 | [Spike] Bot response latency | 24.00h | 18.38h | -5.62h |
| 86d1xcuz4 | [TechTask] Reducing query latency | 7.00h | 13.55h | **+6.55h** |
| 86d1uhjrf | [INQ] Agentforce disconnection | 6.00h | 6.06h | +0.06h |
| 86d1mpjeq | [BUG] Chatbot "transferred" msg | 6.00h | 2.66h | -3.34h |
| 86d1fu0ud | [Prod] Excessive questioning | 12.00h | 0.25h | -11.75h |
| **TOTAL** | | **55.00h** | **40.90h** | |

### Key Observations

1. **ClickUp estimates total 55h but customer budget is 20h.** The team estimated 55h of work and accepted it against a 20h budget. This is a scoping/commercial discipline failure — the work was 2.75x the budget before it even started.

2. **Bot response latency alone (18.38h) consumed 92% of the monthly budget.** A single incident used nearly the entire month's allocation.

3. **Query latency overran by 93%** (13.55h vs 7h estimate). This was the worst estimate-to-actual variance.

4. **"Excessive questioning" showed 12h estimate, 0.25h actual.** Either massively over-estimated or work was abandoned.

---

## 2.3 Team Composition — Managed Services

| Contributor | Hours (Feb 1-16) | % of Total |
|-------------|:----------------:|:----------:|
| Bharat Khandelwal | 21.04h | 51.4% |
| Ganesh Hegde | 18.51h | 45.3% |
| Shantanu Dutta | 1.35h | 3.3% |
| **Total** | **40.90h** | |

> Two contributors consumed 96.7% of the hours. This is a 2-person operation running at 2x budget. The question is not headcount — it is **scope control and agent design efficiency.**

---

## 2.4 Activity Profile — Managed Services

| Month | Activities |
|-------|-----------|
| Sep 2025 | 114 |
| Oct 2025 | 1,253 |
| Nov 2025 | 1,542 |
| Dec 2025 | 658 |
| Jan 2026 | 385 |
| Feb 2026 | 239 |

**Note:** MS project shares the same git repo as delivery — commit history overlaps. The 3,518 commits in MS mirror the 3,527 in delivery. ClickUp comments (316 vs 2,881) and ticket management (13 created vs 564) show the MS phase has significantly less project management overhead — which could mean either leaner operations or less visibility.

---

## 2.5 Geetha's RCA Review — Bot Latency (Feb 12)

Geetha reviewed the RCA document for the bot response latency incident and rated it **6.5/10 — needs revision before client sharing.**

Critical findings:
- Latency projection overclaimed (applied 30-40% improvement to total instead of retrieval component only)
- Investigation step misattributed from a different project
- Acceptance criteria partially unmet ("investigate AND resolve" — resolve incomplete)

> **This is a quality gate failure.** A client-facing RCA with calculation errors and misattributions damages credibility. The 2-3h rework cost adds to the already-blown budget.

---

## 2.6 Jon Gray Non-Negotiable Questions — Managed Services

| # | Question | Answer | Status |
|---|----------|--------|--------|
| 1 | Revenue trajectory & constraint? | 20h/month recurring. Constrained by budget ceiling. | Known |
| 2 | Revenue per employee trend? | 2 active contributors. RPE depends on their rate vs billing rate. | Needs rate data |
| 3 | Project-level contribution margin? | **Negative.** 40.90h consumed vs 20h budget in half a month. | CRITICAL |
| 4 | Estimate vs actual variance? | ClickUp estimates: 55h. Actual: 40.90h. But budget was 20h. | Scoping failure |
| 5 | Is each iteration improving? | First full month of MS — no baseline yet. Must improve from 204.5%. | Baseline set |
| 6 | What breaks first under stress? | Agent design — bot latency consumed 92% of budget on one incident. | Agent quality |
| 7 | Operating leverage over time? | Only if agent design improves to reduce hours-per-incident. | TBD |

---

# Part 3: Summary Findings & Action Items

## Structural Issues

1. **No budget configured in Manazer for MS phase.** `budget_minutes: nil, budget_cents: nil`. The tool built to track project economics has no economic target for its most visible managed services engagement.

2. **Work type misclassification risk.** Both projects tagged `client_delivery` — appropriate, but the distinction between build and MS phase economics is invisible at the portfolio level.

3. **Scoping discipline breakdown.** 55h of estimated work accepted against a 20h monthly budget. Either the team doesn't have commercial visibility, or scope governance is absent.

4. **Agent design is the margin lever.** The bot latency incident (18.38h on a single spike) suggests the Salesforce Agentforce implementation has design issues that cause disproportionate support burden. Fixing agent quality directly improves MS economics.

## Action Items

- [ ] **Extract actual delivery hours** — Run Manazer work sessions for SIM (Aug 2025 - Jan 2026) to complete Part 1 variance analysis
- [ ] **Get contributor rates** — Needed to calculate fully-loaded contribution margin for both phases
- [ ] **Configure MS budget in Manazer** — Set budget_minutes and budget_cents for SIM Managed Services so the dashboard tracks against ceiling
- [ ] **Establish iteration baseline** — Feb 2026 is Month 1 at 204.5% utilization. March must show improvement.
- [ ] **Root cause agent design issues** — Bot response latency and query latency account for 78% of MS hours. Fix the agent, fix the margin.
- [ ] **Review RCA quality gate** — Geetha's 6.5/10 rating means client-facing documents need review before sharing. Build this into the process.
- [ ] **Clarify delivery phase economics** — Was $27K/193h priced to profit, or was it a strategic loss-leader for MS revenue?

---

*Review conducted through Jon Gray CFO persona. All analysis grounded in Manazer activity data and Geetha's Feb 2026 work report.*
