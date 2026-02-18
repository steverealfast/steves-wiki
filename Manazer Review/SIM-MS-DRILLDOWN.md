# SIM Managed Services — Drill-Down

**Review Date:** 2026-02-18 | **Data Source:** Manazer (live query) + ClickUp API fields | **Period:** Jan 1 — Feb 18, 2026
**Contract baseline:** 20h/month (confirmed)

---

## Q0. The contracted monthly budget is 20h. An internal report states 40h. Why?

The confirmed contract is **20h/month**. However, ClickUp ticket `86d201ebt` ("SIM Managed Services Report - Jan 1 to Feb 17, 2026"), created by geetha@realfast.ai on Feb 17, states:

> Contract hours: 40

This is the same author who correctly stated 20h/month in the work report (`86d1ztngf`) one day earlier on Feb 16.

**Question for the delivery head:** Why does an internal report double the contract ceiling? If the team is operating against a 40h mental model while the contract says 20h, every scope decision is based on a budget that doesn't exist. Is anyone on the delivery team aware the contract is 20h, not 40h?

### Additional Data Discrepancies

The work report (`86d1ztngf`) also contains ticket-level actuals that conflict with both ClickUp's `time_spent` field and the MS report's Manazer actuals:

| Ticket | ClickUp `time_spent` | Work Report (`86d1ztngf`) | MS Report (`86d201ebt`) |
|--------|:---:|:---:|:---:|
| Bot latency (`86d1p9d97`) | 11.61h | 18.38h | 0.00h |
| Query latency (`86d1xcuz4`) | 8.69h | 13.55h | 13.57h |
| Disconnection (`86d1uhjrf`) | 2.33h | 6.06h | 6.13h |
| Chatbot msg (`86d1mpjeq`) | 5.89h | 2.66h | 7.82h |

Four data sources, four different actuals for the same tickets. The bot latency ticket ranges from **0h to 18.38h** depending on which report you read.

The work report also includes ticket `86d1fu0ud` ([Prod] Excessive questioning — 12h estimate, 0.25h actual) which **does not appear in the SIM Managed Services project in Manazer at all**.

**Question for the delivery head:** Which system is the source of truth for actual hours — ClickUp time tracking, Manazer work sessions, or manually compiled reports? Until this is resolved, no variance analysis can be fully trusted. This review uses Manazer actuals as compiled in `86d201ebt`.

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

### January Tickets (20h available)

| Created | Ticket | ClickUp ID | Estimate |
|---------|--------|-----------|:---:|
| Jan 8 | [Bug] Lead Owner Not Updated | `86d1gwrg2` | 6.00h |
| Jan 8 | [CRITICAL] Report Count Discrepancies | `86d1gy43x` | 6.00h |
| Jan 9 | [CRITICAL] LE Staff Unable to Create Leads | `86d1h8v69` | 1.50h |
| Jan 19 | [BUG] Chatbot "transferred" msg | `86d1mpjeq` | 6.00h |
| Jan 22 | [Enhancement] Bot context understanding | `86d1p8qj5` | 6.00h |
| Jan 22 | [Spike] Bot response latency | `86d1p9d97` | 24.00h |
| Jan 29 | Bi-weekly call | `86d1rpzy9` | 6.00h |
| | **January total estimated** | | **55.50h** |
| | **January budget** | | **20.00h** |
| | **Over budget at estimate level** | | **+35.50h (278%)** |

By Jan 8, the first two tickets alone (12h) consumed 60% of the monthly budget at the estimate level. By Jan 22, cumulative estimates were at 49.50h — 248% of budget. The spike ticket (24h) was added that same day, pushing it to 55.50h. A single ticket estimated at more than the entire month's allocation. Nobody stopped.

### February Tickets (20h available)

| Created | Ticket | ClickUp ID | Estimate |
|---------|--------|-----------|:---:|
| Feb 3 | [INQ] Live Agent Disconnection | `86d1uhjrf` | 6.00h |
| Feb 10 | [TechTask] Reducing query latency | `86d1xcuz4` | 7.00h |
| Feb 17 | [Latency] Bot Initial Response Time | `86d200p64` | 2.00h |
| | **February total estimated** | | **15.00h** |
| | **February budget** | | **20.00h** |
| | **Under budget at estimate level** | | **-5.00h (75%)** |

*3 Feb tickets (`86d1u0zax`, `86d1ug4g8`, `86d201ebt`) are admin/process tickets with no estimates.*

### Carry-Forward View — February Was Never "Under Budget"

February's 15h of estimates against 20h looks like it fits. It doesn't. January's overrun carries forward.

**At the estimate level:**

| | Budget | Estimated | Overrun | Carry-Forward |
|--|:---:|:---:|:---:|:---:|
| **January** | 20.00h | 55.50h | **+35.50h** | -35.50h carried to Feb |
| **February (adjusted)** | -15.50h | 15.00h | n/a | **-30.50h deficit** |

January's estimate overrun was so large that February's entire 20h budget was already consumed before Feb 1. February started **15.50h in the red** at the estimate level. Adding 15h of February estimates pushes the cumulative deficit to **30.50h**.

**At the actuals level (Manazer):**

| | Budget | Manazer Actual | Overrun | Carry-Forward |
|--|:---:|:---:|:---:|:---:|
| **January** | 20.00h | 51.97h | **+31.97h** | -31.97h carried to Feb |
| **February (adjusted)** | -11.97h | 27.52h | n/a | **-39.49h deficit** |

January consumed **260% of the monthly budget** in actual hours. February started with a negative balance of 11.97h. Every hour worked in February deepened the deficit.

**The combined picture:**

| | Jan-Feb Budget | Estimated | Manazer Actual |
|--|:---:|:---:|:---:|
| **Total** | **40.00h** | **70.50h (176%)** | **79.49h (199%)** |

70.50h of estimated work was accepted against 40h of total budget across two months. 79.49h was actually consumed. The engagement has been operating at nearly **4x the monthly rate** — consuming in 7 weeks what the contract allocates for 4 months.

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

**Question for the delivery head:** Who owns estimation? Is it the ticket creator, the assigned developer, or the delivery lead? Is there a review step before estimates are committed? The estimates totalled 70.50h against a 40h total budget (2 months x 20h). The spike ticket alone (24h) exceeded the entire monthly allocation. Who approved that scope?

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

Against a **20h/month** contract:

| Source of Actuals | January Hours | vs 20h Budget | Overrun |
|---|:---:|:---:|:---:|
| ClickUp `time_spent` | 26.91h | **135%** | +6.91h |
| Manazer (Geetha Report) | 51.97h | **260%** | +31.97h |

Even the lowest actual number (ClickUp's 26.91h) exceeds the budget by 35%. The Manazer figure (51.97h) is 2.6x the budget.

**Questions:**

1. Against a 20h contract, January alone consumed between 135% and 260% of the monthly budget depending on which system you trust. Which is the source of truth?
2. The delta between ClickUp and Manazer on the same tickets is **25.06h**. Why are two systems producing different actuals?
3. Was the January overrun flagged to anyone?

---

## Q4b. Where is the blended billing rate for the managed services package?

**Not configured.** The Manazer project record shows:

| Field | Value |
|-------|-------|
| `budget_minutes` | nil |
| `budget_cents` | nil |
| `hourly_billing_rate` | nil |

There is no billing rate set on this project. Without it, Manazer cannot calculate revenue, contribution margin, or project economics.

**Question for the delivery head:** What is the client billing rate for this engagement? If it's a fixed 20h/month retainer, what is the monthly contract value?

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

**Without a billing rate, we cannot calculate margin.** We know the cost side. We don't know the revenue side. If the contract is 20h/month at $140/hr (implied from the delivery phase's $27K/193h):

- Revenue: 20h x $140 = $2,800/month
- Cost (at Manazer actual of 79.49h over 7 weeks, blended ~$35/hr): ~$2,782
- **7 weeks of cost consumed nearly the entire revenue for the same period — but at 4x the hours**

If the billing rate is lower than $140/hr, this is a loss-making engagement at the cost level alone.

---

## Q6. The contract is 20h/month. In 7 weeks the team burned 79.49h on completed tickets alone, with 5 tickets still open. At what point was the overrun flagged to the client or to management? If it wasn't — why not?

**What the data shows:**

- No budget configured in Manazer — so no automated alert could fire
- Ticket `86d1u0zax` ("Why the hours are more than estimated") was created Feb 2 by Geetha — suggesting the overrun was noticed internally around that date
- That ticket is in `prioritised` status — not resolved, not actioned
- The formal MS report (`86d201ebt`) wasn't created until Feb 17 — 5 weeks into the overrun
- That same report states the contract is 40h (double the actual), suggesting the team may not even know the real budget ceiling

**What the data doesn't show:** Whether the client was informed, whether management was briefed, or whether any commercial conversation happened before Feb 17.

**This is a question only the delivery head can answer.** The system has no record of an escalation. The team's own internal report uses the wrong budget figure. If the delivery team believes the contract is 40h when it's actually 20h, they may not think there's an overrun to flag — which means the commercial awareness gap is worse than the budget overrun itself.

---

## Q7. Manazer tracks 79.49h of actual work. ClickUp shows 38.50h of estimates. Is anyone reviewing the delta between these systems on a weekly basis?

**There are actually three numbers:**

| Source | Total Hours (Completed Tickets) | vs 20h/month (40h total) |
|--------|:---:|:---:|
| ClickUp estimates | 38.50h | **96%** |
| ClickUp `time_spent` (logged in ClickUp) | 53.54h | **134%** |
| Manazer actuals (from Geetha's report) | 79.49h | **199%** |

The delta between ClickUp's own time tracking and Manazer is **25.95h** — a 48% gap on the same tickets.

At 20h/month, even ClickUp's estimates alone (38.50h) nearly exhaust the total 2-month budget. The ClickUp `time_spent` figure (53.54h) is already 34% over. The Manazer actuals (79.49h) are 99% over.

**Question for the delivery head:** Which system is the source of truth for hours — ClickUp or Manazer? Why do they diverge by 48%? And regardless of which is authoritative — is anyone reviewing either of them against the **20h** contract ceiling on a weekly basis? If the team is working against a 40h mental model (per the MS report), the overrun is invisible to them because it doesn't exist under their assumed budget.

---

## Q8. The delivery phase completed 345 of 564 tickets (61%). Three of the top MS overruns trace to design-quality issues from the build. What was the handover process, and how was the remaining 39% accounted for?

**What the data shows:**

- SIM delivery: 564 tickets created, 345 completed (61.2%)
- SIM MS top overruns by hours:
  - Bot context understanding — 19.92h (agent can't maintain conversation state)
  - Report discrepancies — 15.49h (data flow/integration errors)
  - Lead owner not updated — 15.24h (agent transfer architecture)

These are not incident-response patterns. They are design defects — problems in how the agent was built, not how the agent is being supported.

At 20h/month, a single design defect ticket (Bot context at 19.92h) **consumes an entire month's allocation by itself**.

**Question for the delivery head:** What handover process existed between build and managed services? Was there a punch list of known issues? Were the 219 incomplete delivery tickets reviewed to determine which would surface as MS support burden? If so — where is that assessment? If not — the MS scope was set without understanding the inherited technical debt.

---

## Q9. Bot context (19.92h), Report discrepancies (15.49h), Lead owner (15.24h) — these three tickets account for 64% of all MS hours. Are these support incidents or design defects?

**What the data shows:**

- `86d1p8qj5` (Bot context) — **[Enhancement]** tag. The agent doesn't repeat program info after follow-up questions. This is a conversation design gap, not a production incident. **19.92h = 100% of a monthly budget.**
- `86d1gy43x` (Report discrepancies) — **[CRITICAL]** tag. Report counts don't match across multiple reports. This is a data integrity issue from the build. **15.49h = 77% of a monthly budget.**
- `86d1gwrg2` (Lead owner) — **[Bug]** tag. Lead owner not updated on agent transfer. This is an integration logic defect. **15.24h = 76% of a monthly budget.**

One is tagged as an enhancement (design gap). One is a critical data issue. One is a bug. All three trace to how the system was architected and built. Combined, they consumed **50.65h — 2.5 months of budget** on three tickets.

**Question for the delivery head:** If these are design defects from the build phase, why is the 20h/month MS budget absorbing the remediation cost? Was the client charged for these under MS, or were they acknowledged as warranty/defect fixes? A single design defect consumes an entire month. Three of them consumed a quarter's worth of budget. If the MS budget is absorbing build-phase defects, managed services is structurally unprofitable before a single new incident arrives.

---

## Q10. Feb 2026 is Month 2. Budget utilization is 397%. Estimation misses run 3.5x. No budget in the tracking tool. A self-identified estimation problem is in backlog. What is the plan for March — and what does "improvement" mean in measurable terms?

**What the data provides as a baseline:**

| Metric | Jan-Feb 2026 (Baseline) |
|--------|:-:|
| Contract hours | 20h/month (40h total for 2 months) |
| Actual hours (Manazer) | 79.49h in ~7 weeks |
| **Budget utilization** | **199% of 2-month total / 397% per month avg** |
| Estimate-to-budget ratio (Jan) | 55.50h estimated vs 20h = **278%** |
| Actual-to-budget ratio (Jan) | 51.97h actual vs 20h = **260%** |
| Budget configured in Manazer | No |
| Billing rate configured | No |
| Correct budget known by team | No evidence (internal report states 40h) |
| Weekly variance review documented | No evidence |
| Estimation retrospective actioned | No (ticket `86d1u0zax` in backlog) |

**Question for the delivery head:** Given this baseline, what specific changes will be in place by March 1, and what measurable targets will March be evaluated against? For example:

- Will the budget be configured in Manazer as 20h/month (1,200 minutes) by March 1?
- Will the team be informed the contract is 20h, not 40h?
- Will estimate-to-actual ratio improve from 2.06x to below 1.5x?
- Will total March hours stay within the 20h contract ceiling?
- Will the ClickUp vs Manazer time tracking discrepancy (48% gap) be resolved?
- Will there be a weekly review cadence comparing actuals to the 20h budget?

Without defined targets, there is no way to evaluate whether March improved over February. And without that evaluation, there is no iteration discipline.

---

*Data extracted from Manazer project f7ec5128-ab9a-40c0-99b5-ad1a9d453e71 (SIM Managed Services) and ClickUp API fields via Manazer ingestion. All ticket IDs are traceable in ClickUp. Budget baseline: 20h/month (confirmed).*
