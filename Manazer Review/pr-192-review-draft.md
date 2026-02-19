# PR #192 Review Draft — SIM Managed Services

**Target:** `ontic-in/manazer` PR #192
**Method:** Single `gh api` review with `event=COMMENT`
**Commit:** `c10b4ccd2ab3ffd41a6b6a6ec398c7b87d1d7ea3`

---

## Overall Review Body

> This report surfaces critical data that needs to be addressed before merge. The comments below are grounded in Manazer project data (`f7ec5128-ab9a-40c0-99b5-ad1a9d453e71`) and ClickUp ticket records.
>
> **Cross-cutting issues not tied to specific lines:**
>
> **Estimation Ownership:** ClickUp doesn't track who set the `time_estimate` field. Of the 13 MS tickets, Shantanu created 6, Geetha 3, Bharat 2, Ganesh 1. Who owns estimation sign-off? Is there a review step before estimates are committed against the 20h monthly budget? The estimates totalled 70.50h against a 40h total budget (2 months x 20h). The spike ticket alone (24h) exceeded the entire monthly allocation.
>
> **Delivery Handover:** The SIM delivery phase completed 345 of 564 tickets (61.2%). Three of the top MS overruns trace to design-quality issues from the build phase: Bot context understanding (19.92h), Report discrepancies (15.49h), Lead owner not updated (15.24h). Combined: 50.65h — 2.5 months of MS budget on three tickets. These are not support incidents. They are design defects. What handover process existed between build and managed services? Were the 219 incomplete delivery tickets reviewed to determine which would surface as MS support burden?
>
> **March Targets:** Feb 2026 is Month 2. Budget utilization is 199% (cumulative). No budget is configured in the tracking tool. The team's own internal report uses the wrong budget figure. The self-identified estimation problem is in backlog. What specific, measurable changes will be in place by March 1?

---

## Line-Specific Comments

### Comment 1 — `sim-managed-services-report-Feb1toFeb16-2026.md` line 3

**Target line:** `**Contributors: Bharat, Ganesh, Shantanu** | **Customer Budget: 20.00h**`

**Comment:**

> This report states 20h. However, ClickUp ticket `86d201ebt` ("SIM MS Report - Jan 1 to Feb 17"), created by the same author one day later on Feb 17, states "Contract hours: 40."
>
> Two internal documents by the same person, one day apart, with a 2x discrepancy on the contract ceiling. The confirmed contract is 20h/month.
>
> If the delivery team is operating against a 40h mental model, every scope decision — estimation, ticket acceptance, escalation threshold — is based on a budget that doesn't exist. Is anyone on the delivery team aware the contract is 20h, not 40h? If the team doesn't know the real budget, the commercial awareness gap is worse than the budget overrun itself.

---

### Comment 2 — `sim-managed-services-report-Feb1toFeb16-2026.md` line 5

**Target line:** `*Estimates: ClickUp | Actuals: Manazer (inferred from activity signals)*`

**Comment:**

> Four data sources produce four different actuals for the same tickets:
>
> | Ticket | ClickUp `time_spent` | This Report (Manazer) | MS Report `86d201ebt` |
> |--------|:---:|:---:|:---:|
> | Bot latency (`86d1p9d97`) | 11.61h | 18.38h | 0.00h |
> | Query latency (`86d1xcuz4`) | 8.69h | 13.55h | 13.57h |
> | Disconnection (`86d1uhjrf`) | 2.33h | 6.06h | 6.13h |
> | Chatbot msg (`86d1mpjeq`) | 5.89h | 2.66h | 7.82h |
>
> The bot latency ticket ranges from 0h to 18.38h depending on which report you read. Which system is the source of truth for actual hours? Until this is resolved, no variance analysis can be fully trusted.

---

### Comment 3 — `sim-managed-services-report-Feb1toFeb16-2026.md` line 8

**Target line:** `## 1. Ticket Summary`

**Comment:**

> This report covers 5 tickets from February. The SIM Managed Services project has **13 tickets total** since inception (Jan 8, 2026). The 8 tickets not shown here span both months and include the three largest budget consumers in the engagement:
>
> - `86d1p8qj5` — Bot context understanding: **19.92h** (100% of a monthly budget)
> - `86d1gy43x` — Report count discrepancies: **15.49h** (77% of a monthly budget)
> - `86d1gwrg2` — Lead owner not updated: **15.24h** (76% of a monthly budget)
>
> These three tickets alone consumed **50.65h — 2.5 months of the 20h/month budget.** January's 51.97h of actual work is the reason February started in deficit (see TOTAL comment below). Any assessment of February's performance requires visibility into what January delivered and at what cost.
>
> If these are design defects from the build phase, why is the 20h/month MS budget absorbing the remediation cost? Was the client charged for these under MS, or were they acknowledged as warranty/defect fixes? If MS is absorbing build-phase defects, the engagement is structurally unprofitable before a single new incident arrives.

---

### Comment 4 — `sim-managed-services-report-Feb1toFeb16-2026.md` line 12

**Target line:** `| 86d1p9d97 | [Spike] Bot response latency | in qa | 24.00h | 18.38h | -5.62h |`

**Comment:**

> A single ticket estimated at 24h against a 20h monthly budget. The estimate alone exceeds the entire month's allocation by 20%. Who approved scoping this?
>
> At 18.38h actual, this one spike consumed 92% of the monthly budget. Combined with query latency below (13.55h), two tickets account for 31.93h — 160% of the monthly ceiling.

---

### Comment 5 — `sim-managed-services-report-Feb1toFeb16-2026.md` line 13

**Target line:** `| 86d1xcuz4 | [TechTask] Reducing query latency | complete | 7.00h | 13.55h | +6.55h |`

**Comment:**

> Worst estimate-to-actual variance in the set: 93% overrun (13.55h vs 7h). This ticket and the bot latency ticket above account for 31.93h combined — 78% of all Feb hours and 160% of the monthly budget on two tickets alone.

---

### Comment 6 — `sim-managed-services-report-Feb1toFeb16-2026.md` line 16

**Target line:** `| 86d1fu0ud | [Prod] Excessive questioning | complete | 12.00h | 0.25h | -11.75h |`

**Comment:**

> This ticket does not appear in the SIM Managed Services project in Manazer (`f7ec5128-ab9a-40c0-99b5-ad1a9d453e71`). Where is it being tracked?
>
> 12h estimate, 0.25h actual. Either massively over-estimated, or work was abandoned/moved elsewhere. If the estimate was genuine, it added 12h to the scope commitment against a 20h budget — 60% of the monthly ceiling for a single ticket that delivered 15 minutes of work.

---

### Comment 7 — `sim-managed-services-report-Feb1toFeb16-2026.md` line 18

**Target line:** `| **TOTAL** | | | **55.00h** | **40.90h** | |`

**Comment:**

> 55h of estimates in this report against a 20h monthly budget — the scope was 2.75x the ceiling before any work began.
>
> This report covers February, but it cannot be read in isolation. January's performance cascades directly into this month. January consumed 51.97h actual (Manazer) against the same 20h budget — a 31.97h overrun that carried forward into February. February started with a negative balance of 11.97h before a single hour was worked.
>
> The combined Jan-Feb picture:
>
> | Month | Budget | Manazer Actual | Carry-Forward |
> |---|:---:|:---:|:---:|
> | January | 20h | 51.97h | -31.97h carried to Feb |
> | February (adjusted) | -11.97h | 27.52h | -39.49h deficit |
> | **Combined** | **40h** | **79.49h (199%)** | |
>
> Including January, 70.50h of estimated work was accepted against 40h of total 2-month budget. 79.49h was actually consumed. The engagement consumed in 7 weeks what the contract allocates for 4 months.

---

### Comment 8 — `sim-managed-services-report-Feb1toFeb16-2026.md` line 57

**Target line:** `| Budget Utilization | | **204.5%** |`

**Comment:**

> At 204.5% utilization (Feb only — cumulative is 199% of 2-month total). Manazer actuals show 79.49h consumed against 40h of total budget across Jan-Feb. The contract allocates 20h/month. Why are we nearly 4x over?
>
> - Manazer has no budget configured for this project (`budget_minutes: nil`, `budget_cents: nil`) — so no automated alert could fire
> - No billing rate configured (`hourly_billing_rate: nil`) — so no margin visibility exists
> - The estimation problem ticket (`86d1u0zax` — "Why the hours are more than estimated") was created Feb 2 and is sitting in `prioritised` status — not resolved
> - This formal report wasn't created until Feb 17 — 5 weeks into the overrun
> - Is anyone reviewing Manazer actuals against the 20h contract ceiling on a weekly basis?
>
> What specific changes will be in place by March 1? Will the budget be configured in Manazer? Will the team be informed the contract is 20h? Will there be a weekly review cadence comparing actuals to budget?

---

### Comment 9 — `team-work-sessions-report-Feb1toFeb18-2026.md` line 4

**Target line:** `| Ganesh Hegde | 87.81h | 12 | 85% |`

**Comment:**

> Ganesh: 87.81h total across all projects (12 days). SIM MS actuals: 18.51h (Manazer). Internal cost rate: $30/hr.
>
> No billing rate is configured on the SIM MS project. The full cost picture across all MS contributors (Manazer cost rates): Bharat $30/hr, Ganesh $30/hr, Shantanu $30/hr, Geetha $80/hr, Sidu $80/hr. At a blended rate of ~$35/hr across 79.49h (Jan-Feb combined), total internal cost is ~$2,782.
>
> If the contract is 20h/month at $140/hr (implied from the delivery phase's $27K/193h), revenue is $2,800/month. Seven weeks of internal cost ($2,782) nearly equals a single month's revenue ($2,800) — while the team delivered 4x the contracted hours. If the billing rate is lower than $140/hr, this is a loss-making engagement at the cost level alone.

---

### Comment 10 — `team-work-sessions-report-Feb1toFeb18-2026.md` line 6

**Target line:** `| Bharat | 71.62h | 13 | 47% |`

**Comment:**

> Bharat: 71.62h total (13 days) at **47% confidence**. SIM MS actuals: 21.04h (Manazer). Internal cost rate: $30/hr.
>
> 47% confidence means Manazer's work session clustering has low certainty on these hours. The actual time may be significantly different. Combined with the ClickUp vs Manazer discrepancy (Comment 2), the hours data for this engagement has no reliable single source. This makes any margin calculation speculative.

---

*10 line-specific comments + 1 overall review body. All data traceable to Manazer project `f7ec5128-ab9a-40c0-99b5-ad1a9d453e71` and ClickUp ticket IDs.*
