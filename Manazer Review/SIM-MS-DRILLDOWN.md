# SIM Managed Services — Drill-Down

**Review Date:** 2026-02-18 | **Data Source:** Manazer (live query) + ClickUp API fields | **Period:** Jan 1 — Feb 18, 2026

---

## Q1. What are the total number of tickets serviced since the start of managed services?

**13 tickets created.** Breakdown:

| Created | Ticket | ClickUp ID | Status |
|---------|--------|-----------|--------|
| Jan 8 | [Bug] Lead Owner Not Updated on Agent Transfer | `86d1gwrg2` | complete |
| Jan 8 | [CRITICAL] Report Count Discrepancies Across Multiple Reports | `86d1gy43x` | complete |
| Jan 9 | [CRITICAL] LE Staff Unable to Create Leads | `86d1h8v69` | complete |
| Jan 19 | [BUG] Chatbot "transferred" non-business hours | `86d1mpjeq` | complete |
| Jan 22 | [Enhancement] Bot context understanding | `86d1p8qj5` | complete |
| Jan 22 | [Spike] Bot response latency | `86d1p9d97` | deployed to uat |
| Jan 29 | Bi-weekly call | `86d1rpzy9` | in progress |
| Feb 2 | Why the hours are more than estimated | `86d1u0zax` | prioritised |
| Feb 3 | Conduct weekly IPM with Poker Planning | `86d1ug4g8` | prioritised |
| Feb 3 | [INQ] Live Agent Disconnection Handling | `86d1uhjrf` | complete |
| Feb 10 | [TechTask] Reducing latency for specific queries | `86d1xcuz4` | complete |
| Feb 17 | [Latency] Bot Initial Response Time Too Slow | `86d200p64` | complete |
| Feb 17 | SIM MS Report - Jan 1 to Feb 17 | `86d201ebt` | backlog |

**7 completed. 1 deployed to UAT. 2 in progress/prioritised. 2 administrative. 1 backlog.**

All 13 tickets created by 3 people: Shantanu (6), Geetha (3), Bharat (2), Ganesh (1), and 1 unattributed.

---

## Q2. What was the original estimation for the tickets?

| Ticket | ClickUp ID | ClickUp Estimate |
|--------|-----------|:---:|
| Lead Owner Not Updated | `86d1gwrg2` | 6.00h |
| Report Count Discrepancies | `86d1gy43x` | 6.00h |
| LE Staff Unable to Create Leads | `86d1h8v69` | 1.50h |
| Chatbot "transferred" msg | `86d1mpjeq` | 6.00h |
| Bot context understanding | `86d1p8qj5` | 6.00h |
| Bot response latency (spike) | `86d1p9d97` | 24.00h |
| Bi-weekly call | `86d1rpzy9` | 6.00h |
| Live Agent Disconnection | `86d1uhjrf` | 6.00h |
| Reducing query latency | `86d1xcuz4` | 7.00h |
| Bot Initial Response Time | `86d200p64` | 2.00h |
| **Total estimated (10 tickets with estimates)** | | **70.50h** |

Three tickets (`86d1u0zax`, `86d1ug4g8`, `86d201ebt`) have no estimates — they're administrative/process tickets.

**70.50h estimated against a 40h/month contract.** The estimates alone exceed the budget by 76% before a single hour of work starts. The spike ticket alone (24h) consumes 60% of a month's allocation.

---

## Q3. Who is responsible for the estimates?

**The data doesn't tell us who entered the estimates.** ClickUp doesn't track who set the `time_estimate` field.

What the data does show is who **created** the tickets:

| Ticket Creator | Tickets Created |
|----------------|:-:|
| shantanu@realfast.ai | 6 |
| geetha@realfast.ai | 3 |
| bharat@realfast.ai | 2 |
| ganesh.hegde@realfast.ai | 1 |

**Question for the delivery head:** Who owns estimation? Is it the ticket creator, the assigned developer, or the delivery lead? Is there a review step before estimates are committed? If the estimates totalled 70.50h against a 40h budget and nobody flagged the gap — the estimation process either doesn't include a budget check, or the budget check was overridden.

---

## Q4. What was the January estimate vs actual?

**January completed 5 tickets.** But there are **three different "actual" numbers** depending on the source:

| Ticket | ClickUp Est | ClickUp `time_spent` | Manazer Actual (Geetha Report) |
|--------|:---:|:---:|:---:|
| Lead Owner (`86d1gwrg2`) | 6.00h | 7.78h | 15.24h |
| Report Discrepancies (`86d1gy43x`) | 6.00h | 5.89h | 15.49h |
| LE Staff Permissions (`86d1h8v69`) | 1.50h | 1.24h | 1.32h |
| Bot context understanding (`86d1p8qj5`) | 6.00h | 12.00h | 19.92h |
| Bi-weekly call (`86d1rpzy9`) | 6.00h | nil | 0.00h |
| **Totals** | **25.50h** | **26.91h** | **51.97h** |

**Three questions emerge:**

1. Against a 40h/month contract, January's completed work was either 26.91h (ClickUp) or 51.97h (Manazer). Which is the source of truth?
2. The delta between ClickUp and Manazer on the same tickets is **25.06h**. Why are two systems producing different actuals? Is someone logging time in one system but not the other? Is Manazer capturing time that ClickUp isn't?
3. If Manazer's 51.97h is correct, January alone exceeded the monthly budget by 30%. Was this flagged?

---

## Q4b. Where is the blended billing rate for the managed services package?

**Not configured.** The Manazer project record shows:

| Field | Value |
|-------|-------|
| `budget_minutes` | nil |
| `budget_cents` | nil |
| `hourly_billing_rate` | nil |

There is no billing rate set on this project. Without it, Manazer cannot calculate revenue, contribution margin, or project economics. The dashboard shows activity volume but not financial performance.

**Question for the delivery head:** What is the client billing rate for this engagement? If it's a fixed 40h/month retainer, what is the monthly contract value?

---

## Q5. What are the cost rates for the individuals on this?

Manazer has cost data for the MS contributors:

| Contributor | Cost Rate | Feb 2026 Activity | Role Signal |
|-------------|:---------:|:-:|---|
| Bharat (bharat@realfast.ai) | $30/hr | 80 activities | Primary developer |
| Ganesh Hegde (ganesh.hegde@realfast.ai) | $30/hr | 86 activities | Primary developer |
| Shantanu (shantanu@realfast.ai) | $30/hr | 17 activities | Ticket creator / coordination |
| Geetha (geetha@realfast.ai) | $80/hr | 21 activities | PM / review / reporting |
| Sidu (sidu@realfast.ai) | $80/hr | 5 activities | Oversight |

**Blended internal cost rate:** Dominated by Bharat ($30) and Ganesh ($30), with lighter touches from Geetha ($80) and Sidu ($80).

**Without a billing rate, we cannot calculate margin.** We know the cost side. We don't know the revenue side. If the contract is 40h/month at (for example) $140/hr (implied from the delivery phase's $27K/193h), the margin math would be:

- Revenue: 40h x $140 = $5,600/month
- Cost (at Manazer actual of 79.49h, blended ~$35/hr): ~$2,782
- Gross margin: ~$2,818 (50%)

But if the billing rate is lower, or if the contract is fixed-fee, this changes entirely. **The delivery head needs to provide the contract economics.**

---

## Q6. The contract is 40h/month. In 7 weeks the team burned 79.49h on completed tickets alone, with 5 tickets still open. At what point was the overrun flagged to the client or to management? If it wasn't — why not?

**What the data shows:**

- No budget configured in Manazer — so no automated alert could fire
- Ticket `86d1u0zax` ("Why the hours are more than estimated") was created Feb 2 by Geetha — suggesting the overrun was noticed internally around that date
- That ticket is in `prioritised` status — not resolved, not actioned
- The formal MS report (`86d201ebt`) wasn't created until Feb 17 — 5 weeks into the overrun

**What the data doesn't show:** Whether the client was informed, whether management was briefed, or whether any commercial conversation happened before Feb 17.

**This is a question only the delivery head can answer.** The system has no record of an escalation. If one happened offline, it should be documented. If it didn't happen — 79.49h was consumed against a 40h ceiling with no flag raised for 5 weeks.

---

## Q7. Manazer tracks 79.49h of actual work. ClickUp shows 38.50h of estimates. The variance is 106%. Is anyone reviewing the delta between these two systems on a weekly basis?

**The problem is worse than stated.** There are actually three numbers:

| Source | Total Hours (Completed Tickets) |
|--------|:---:|
| ClickUp estimates | 38.50h |
| ClickUp `time_spent` (logged in ClickUp) | 53.54h |
| Manazer actuals (from Geetha's report) | 79.49h |

The delta between ClickUp's own time tracking and Manazer is **25.95h** — a 48% gap on the same tickets. This means:

1. Time is being tracked in two places with different results
2. Neither system is the acknowledged source of truth
3. Any review based on one system alone is working from incomplete data

**Question for the delivery head:** Which system is the source of truth for hours — ClickUp or Manazer? Why do they diverge by 48%? And regardless of which is authoritative — is anyone reviewing either of them against the 40h contract ceiling on a weekly basis?

---

## Q8. The delivery phase completed 345 of 564 tickets (61%). Three of the top MS overruns trace to design-quality issues from the build. What was the handover process, and how was the remaining 39% accounted for?

**What the data shows:**

- SIM delivery: 564 tickets created, 345 completed (61.2%)
- SIM MS top overruns by hours:
  - Bot context understanding — 19.92h (agent can't maintain conversation state)
  - Report discrepancies — 15.49h (data flow/integration errors)
  - Lead owner not updated — 15.24h (agent transfer architecture)

These are not incident-response patterns. They are design defects — problems in how the agent was built, not how the agent is being supported.

**Question for the delivery head:** What handover process existed between build and managed services? Was there a punch list of known issues? Were the 219 incomplete delivery tickets reviewed to determine which would surface as MS support burden? If so — where is that assessment? If not — the MS scope was set without understanding the inherited technical debt.

---

## Q9. Bot context (19.92h), Report discrepancies (15.49h), Lead owner (15.24h) — these three tickets account for 64% of all MS hours. Are these support incidents or design defects?

**What the data shows:**

- `86d1p8qj5` (Bot context) — **[Enhancement]** tag. The agent doesn't repeat program info after follow-up questions. This is a conversation design gap, not a production incident.
- `86d1gy43x` (Report discrepancies) — **[CRITICAL]** tag. Report counts don't match across multiple reports. This is a data integrity issue from the build.
- `86d1gwrg2` (Lead owner) — **[Bug]** tag. Lead owner not updated on agent transfer. This is an integration logic defect.

One is tagged as an enhancement (design gap). One is a critical data issue. One is a bug. All three trace to how the system was architected and built.

**Question for the delivery head:** If these are design defects from the build phase, why is the 40h/month MS budget absorbing the remediation cost? Was the client charged for these under MS, or were they acknowledged as warranty/defect fixes? If the MS budget is absorbing build-phase defects, every month of managed services starts with a structural deficit before a single new incident arrives.

---

## Q10. Feb 2026 is Month 2. Budget utilization is 199%. Estimation misses 2:1. No budget in the tracking tool. A self-identified estimation problem is in backlog. What is the plan for March — and what does "improvement" mean in measurable terms?

**What the data provides as a baseline:**

| Metric | Jan-Feb 2026 (Baseline) |
|--------|:-:|
| Contract hours | 40h/month |
| Actual hours (Manazer) | 79.49h in ~7 weeks |
| Estimate accuracy | 2.06x (actual/estimate) |
| Budget configured in Manazer | No |
| Billing rate configured | No |
| Weekly variance review documented | No evidence |
| Estimation retrospective actioned | No (in backlog) |

**Question for the delivery head:** Given this baseline, what specific changes will be in place by March 1, and what measurable targets will March be evaluated against? For example:

- Will the budget be configured in Manazer by March 1?
- Will estimate-to-actual ratio improve from 2.06x to below 1.5x?
- Will total March hours stay within the 40h contract ceiling?
- Will the ClickUp vs Manazer time tracking discrepancy (48% gap) be resolved?
- Will there be a weekly review cadence comparing actuals to budget?

Without defined targets, there is no way to evaluate whether March improved over February. And without that evaluation, there is no iteration discipline.

---

*Data extracted from Manazer project f7ec5128-ab9a-40c0-99b5-ad1a9d453e71 (SIM Managed Services) and ClickUp API fields via Manazer ingestion. All ticket IDs are traceable in ClickUp.*
