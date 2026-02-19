# SIM Managed Services Review — Process Log

**Period:** Feb 18–19, 2026
**Persona:** Jon Gray — CFO. Revenue Architect. Project Economist. Compounding Operator.
**Target:** PR #192 on `ontic-in/manazer` — SIM Managed Services work report (Feb 1-16, 2026)
**Author of PR:** geetha-realfast
**Reviewer:** steverealfast

---

## Phase 0: Establishing the Analytical Framework

### The Persona

Before any data was touched, the Jon Gray CFO persona was defined in `PERSONA.md`. This wasn't cosmetic — it set the lens through which every number would be evaluated:

- **Equal weight** on revenue quality and project-level economics
- **No tolerance** for recurring estimate slippage
- **Fully-loaded economic view** — all margin calculations must include direct labor, overhead, idle capacity, ramp inefficiency
- **Iteration governance** — every completed project triggers estimate vs actual variance analysis, margin reconciliation, utilization review
- **Non-negotiable questions:** What is the revenue trajectory? What is revenue per employee? What is project-level contribution margin? What is estimate vs actual variance? Is each iteration improving?

The persona operates in four communication modes: Boardroom (strategic), Operator (diagnostic), PE Diligence (forensic), and Founder Confrontation (direct, equity-protective). The SIM review primarily used **Operator** and **PE Diligence** modes.

### Why a Persona Matters

The persona isn't role-playing. It's a decision filter. When confronted with ambiguous data — like four different actual-hour figures for the same ticket — the Jon Gray lens asks: "Which number do I trust for margin calculation, and what does the spread tell me about process maturity?" A delivery-focused lens would ask: "Which number is closest to reality?" The CFO lens asks both, but leads with the economic consequence.

---

## Phase 1: Data Extraction (Feb 18)

### Step 1.1 — Manazer MCP Queries

The first analytical step was querying the Manazer system directly via MCP (`mcp__manazer__rails_runner`) to establish ground truth before reading any reports.

**Queries executed:**

1. **Project identification** — Located the SIM Managed Services project: `f7ec5128-ab9a-40c0-99b5-ad1a9d453e71`
2. **Budget configuration** — Discovered `budget_minutes: nil`, `budget_cents: nil`, `hourly_billing_rate: nil`. No budget had ever been set.
3. **Activity counts** — Total activities, commits, ClickUp comments, tickets created/completed, PRs opened/closed
4. **Contributor data** — Names, cost rates, activity counts per contributor
5. **Monthly activity profiles** — Activity distribution by month for both delivery and MS phases
6. **SIM Delivery project** — Cross-referenced against the parent delivery project for context (564 tickets, 345 completed, $27K budget, 193h)
7. **ClickUp ticket details** — All 13 MS tickets with IDs, statuses, estimates, creators, creation dates

### Step 1.2 — ClickUp Cross-Reference

ClickUp data was extracted through Manazer's ingested fields:
- `time_estimate` — original estimates per ticket
- `time_spent` — ClickUp's own logged time
- Ticket creators, statuses, creation dates
- The critical discovery: ClickUp ticket `86d201ebt` stating "Contract hours: 40" vs the confirmed 20h/month contract

### Step 1.3 — Report Analysis

Geetha's work report (the PR #192 content) was read and compared against the Manazer/ClickUp ground truth. This is where the gaps became visible — the report contained numbers but no diagnosis.

**Key finding at this stage:** The report was descriptive, not analytical. It presented a 204.5% utilization figure without explaining root cause, carry-forward impact, or corrective recommendation.

---

## Phase 2: Multi-Dimensional Analysis (Feb 18)

### Step 2.1 — SIM-REVIEW.md (Broad CFO Lens)

The first analytical document covered both phases of the SIM engagement:

**Part 1 — Delivery Phase:**
- $27K budget / 193h allocation / 25+ contributors
- Revenue per contributor: ~$3,857 for a 6-month engagement — dangerously thin
- 564 tickets created, 345 completed (61.2%) — 219 incomplete at handover
- Activity bell curve: 72% of work in Oct-Nov 2025
- Structural question: was this priced to profit or was it a loss-leader for MS revenue?

**Part 2 — Managed Services Phase:**
- 20h/month contract, no budget configured in Manazer
- Feb 1-16: 40.90h actual against 20h budget = 204.5% utilization
- 55h of ClickUp estimates accepted against 20h budget
- Two contributors (Bharat + Ganesh) consumed 96.7% of hours
- Agent design identified as the margin lever — bot latency consumed 92% of monthly budget

**Part 3 — Summary Findings:**
- No budget configured
- Scoping discipline breakdown (55h accepted against 20h)
- Agent design driving disproportionate support burden
- 7 action items defined

### Step 2.2 — SIM-MS-DRILLDOWN.md (Forensic Deep-Dive)

Ten structured questions, each answered with Manazer data:

**Q0 — The 20h vs 40h discrepancy.** Two internal documents by the same person, one day apart, with a 2x discrepancy on the contract ceiling. This became the opening comment on the PR review.

**Q1 — Total tickets.** 13 tickets since inception. 7 completed, 1 in UAT, 2 in progress, 2 admin, 1 backlog.

**Q2 — Estimation analysis.** This is where the cumulative estimation timeline was first built:
- January estimates: 55.50h against 20h budget (278%)
- February estimates: 15.00h against 20h budget (75%) — but with January carry-forward, February was already in deficit
- Combined: 70.50h estimated against 40h total budget (176%)

**Q3 — Estimation ownership.** ClickUp doesn't log who set estimates. Ticket creators identified but creator ≠ estimator.

**Q4 — January estimate vs actual.** Three different "actual" numbers discovered:
- ClickUp `time_spent`: 26.91h (135% of budget)
- Manazer actuals (Geetha's report): 51.97h (260% of budget)
- Delta: 25.06h — two systems producing fundamentally different actuals

**Q4b — Billing rate.** Not configured. Without it, no margin calculation possible.

**Q5 — Cost rates.** Bharat $30/hr, Ganesh $30/hr, Shantanu $30/hr, Geetha $80/hr, Sidu $80/hr. Blended ~$35/hr. At 79.49h actual, total internal cost ~$2,782 — nearly equaling a single month's implied revenue ($2,800).

**Q6 — Escalation timeline.** No budget in Manazer (no automated alerts possible). Estimation problem ticket created Feb 2 but not actioned. Formal report not created until Feb 17 — 5 weeks into the overrun. No evidence of client or management notification.

**Q7 — System discrepancies.** Three numbers for the same engagement: ClickUp estimates (38.50h), ClickUp time_spent (53.54h), Manazer actuals (79.49h). 48% gap between ClickUp and Manazer on the same tickets.

**Q8 — Delivery handover.** 345 of 564 delivery tickets completed (61.2%). Three of the top MS overruns trace to design-quality issues from the build phase. 50.65h consumed on three design defects — 2.5 months of MS budget.

**Q9 — Design defects vs support incidents.** Bot context (19.92h) tagged as Enhancement — conversation design gap. Report discrepancies (15.49h) tagged as Critical — data integrity from build. Lead owner (15.24h) tagged as Bug — integration logic defect. All three trace to how the system was architected.

**Q10 — March targets.** The baseline established: 199% utilization, no budget configured, wrong budget figure in team documents, estimation problem in backlog. Six specific measurable targets proposed for March 1.

---

## Phase 3: PR Review Drafting (Feb 18)

### The Algorithmic Process

The PR review was not written as general feedback. It was engineered as a structured review with specific design choices:

**1. One overall review body + 10 line-specific comments.**
The overall body covered cross-cutting issues (estimation ownership, delivery handover, March targets) that couldn't be anchored to a single line. The 10 line comments each targeted a specific data point in the report.

**2. Every comment grounded in verifiable data.**
No opinions without numbers. Every assertion referenced either a Manazer query result, a ClickUp ticket ID, or a calculation derived from the report's own figures. This makes the comments impossible to dismiss as subjective.

**3. Comments escalate in severity.**
- Comments 1-2: Data integrity issues (budget discrepancy, conflicting actuals)
- Comments 3-6: Ticket-level analysis (missing context, estimation failures, missing tickets)
- Comment 7: Cumulative budget impact (the Jan-Feb carry-forward table)
- Comment 8: Systemic failures (no budget configured, no review cadence)
- Comments 9-10: Economic consequences (cost/margin, confidence scoring)

**4. Each comment ends with a question.**
Not accusatory — diagnostic. "Who approved scoping this?" "Which system is the source of truth?" "What specific changes will be in place by March 1?" This forces a response rather than allowing a passive acknowledgment.

### Step 3.1 — pr-192-review-draft.md (First Draft)

The initial draft was created with all 10 comments + overall body. Each comment structured as:
- **Target file and line number** — exact location in the PR
- **Target line content** — what the comment anchors to
- **Comment body** — analysis with data, ending with a question

### Step 3.2 — Review Refinement

The draft went through a revision pass before posting:
- Comment 1: Added "If the team doesn't know the real budget, the commercial awareness gap is worse than the budget overrun itself"
- Comment 3: New comment inserted — January context showing the 8 missing tickets and the three largest budget consumers (50.65h on three tickets)
- Comment 4: Tightened to "exceeds the entire month's allocation by 20%" and added the combined impact with query latency (31.93h = 160% of ceiling)
- Comment 7: Restructured to lead with "cannot be read in isolation" and the carry-forward table
- Comment 8: Added "Is anyone reviewing Manazer actuals against the 20h contract ceiling on a weekly basis?"
- Comments renumbered 1-10 after insertion
- Old Comment 7 (duplicate of TOTAL analysis) removed — consolidated into the revised Comment 7

### Step 3.3 — Review Posted to GitHub

The review was submitted via `gh api` as a single batch:
- Method: `POST /repos/ontic-in/manazer/pulls/192/reviews`
- Event: `COMMENT` (not `REQUEST_CHANGES` — diagnostic, not blocking)
- Commit: `c10b4ccd2ab3ffd41a6b6a6ec398c7b87d1d7ea3`
- 10 line-specific comments + 1 overall body
- Steve also posted a separate issue-level comment directly on the PR summarizing the three key concerns

---

## Phase 4: Response Analysis (Feb 19)

### Step 4.1 — Fetching the Comment Thread

After authenticating `gh` CLI (device code flow, steverealfast), all 21 comments were pulled from PR #192:
- 10 original review comments (steverealfast)
- 10 replies (geetha-realfast) — responded to every comment within ~1 hour
- 1 reply (kaiwren) — contradicted Geetha's confidence scoring explanation

### Step 4.2 — Thread Archived

All 21 comments saved verbatim to `PR-192-review2.md` with authors, timestamps, file/line references, and threading (in_reply_to). This preserves the complete record regardless of what happens to the PR.

### Step 4.3 — Response Assessment (Jon Gray Lens)

Each of Geetha's 10 replies was evaluated on three dimensions:
1. **Did it answer the question?**
2. **Did it introduce new data?**
3. **Did it change the economic picture?**

**Assessment summary:**

| Comment | Question Answered? | New Data? | Economic Impact? |
|:---:|:---:|:---:|:---:|
| C1 (20h vs 40h) | Partially — arithmetic explanation plausible but original doc didn't qualify "2-month" | Yes — escalation commitment | Neutral — commitment to configure budget is right action |
| C2 (Four actuals) | Partially — methodology section added | Yes — designated Manazer as source of truth | Neutral — explains divergence but doesn't resolve 0h-to-18.38h spread |
| C3 (January context) | Partially — January section added but scoped to 3 contributors only | Yes — different numbers (43.10h vs our 50.65h) | **Understates** — excluding $80/hr contributors makes overrun look smaller |
| C4 (24h spike) | **No** — action item for future, didn't answer who approved | Yes — estimation gate proposed | Neutral — right action, wrong timeline (future vs past) |
| C5 (93% overrun) | Yes — acknowledged | No | Neutral |
| C6 (Missing ticket) | Yes — ticket exists in both projects | Yes — activity split clarified (33 delivery, 11 MS) | Helpful — explains 0.25h as MS-scoped only |
| C7 (Jan-Feb totals) | Partially — added Section 1b but numbers differ | Yes — January at 67.44h (vs our 51.97h), combined 108.34h = 270.9% | **Worse than our analysis** — her own numbers show higher overrun |
| C8 (No budget) | Yes — confirmed nil values, 6 action items | Yes — March 1 targets | Positive — substantive commitment if executed |
| C9 (Cost/margin) | Acknowledged | No new data | Neutral — billing rate to be configured |
| C10 (47% confidence) | **Wrong** — explanation contradicted by system builder | No valid data | **Negative** — undermines credibility of methodology section |

**Three critical findings from the response analysis:**

1. **The January numbers shifted.** Geetha's Section 1a reports 43.10h on the top 3 tickets (scoped to Bharat/Ganesh/Shantanu). Our all-contributor analysis showed 50.65h. The 7.55h gap is the cost of excluding Geetha ($80/hr) and Sidu ($80/hr). Whether intentional or not, it understates the overrun.

2. **The "who approved" questions remain unanswered.** Comment 4 and the overall review both asked who owns estimation sign-off. Geetha added a future-facing action item but did not answer who approved the existing 55h+ of estimates against a 20h budget.

3. **kaiwren's intervention is significant.** The Manazer developer directly contradicted Geetha's explanation of 47% confidence scoring: "There is no such thing as comment-heavy work pattern, and 47% confidence is not expected for any workflow. This is hallucinated and wrong." This undermines the data source methodology section Geetha added in response to Comment 2.

---

## Phase 5: Call Preparation (Feb 19)

### The Strategic Decision

Rather than posting a second round of PR comments, the decision was made to prepare talking points for a live conversation. Rationale:

- Written comments had already established the analytical foundation
- The remaining issues (scope approval process, scoping exclusion, RCA request) are better resolved in dialogue than in a comment thread
- A call allows real-time follow-up on evasive or incomplete answers
- The RCA request is a deliverable assignment, not a comment reply

### Step 5.1 — Call Guide Created

`PR-192-call-guide.md` structured as a live reference document:

**Call Flow at the top** — 5-step structure with timing (~20 min total):
1. Open — acknowledge engagement, set agenda
2. Point 1 — report quality (descriptive vs diagnostic)
3. Point 2 — open questions (scope approval, January scoping, confidence scoring)
4. Point 3 — RCA request (three questions: what went wrong, what changes, how to audit)
5. Close — recoverable engagement, controls before March

**Each point leads with exact language** — "Say this:" blocks give the reviewer precise phrasing to use without improvising under pressure.

**Supporting data sits underneath** — available if needed, skippable if the point lands without resistance.

### Step 5.2 — Scope Approval Timeline (Expanded)

Section 2a was expanded with the cumulative estimation timeline — the most powerful visual in the entire review:

| Date | Ticket | Estimate | Cumulative | vs 20h |
|------|--------|:--------:|:----------:|:------:|
| Jan 8 | Lead Owner | 6h | 6h | 30% |
| Jan 8 | Report Discrepancies | 6h | 12h | 60% |
| Jan 9 | LE Staff Permissions | 1.5h | 13.5h | 68% |
| Jan 19 | Chatbot msg | 6h | 19.5h | 98% |
| **Jan 22** | **Bot context** | **6h** | **25.5h** | **128%** |
| **Jan 22** | **Bot latency (spike)** | **24h** | **49.5h** | **248%** |
| Jan 29 | Bi-weekly call | 6h | 55.5h | 278% |

This table shows the budget was at 98% on January 19. On January 22, two tickets added 30h in a single day. The table makes it impossible to argue this was a sudden, unforeseeable overrun — it accumulated over three weeks with multiple opportunities to intervene.

### Step 5.3 — RCA Framework

The RCA request was structured around three questions with specific examples:

1. **What went wrong?** — 5 specific root cause questions
2. **What changes are being made?** — Each change needs an owner and completion date. The 6 action items from Comment 8 reply are a starting point.
3. **How will those changes be audited?** — The missing piece. Action items without verification become intentions, not controls.

Deliverable format: one-pager. Deadline: before March 1 (when controls need to be live).

---

## Analytical Point of View — Jon Gray Summary

### What the Data Says

The SIM Managed Services engagement is consuming in 7 weeks what the contract allocates for 4 months. The combined Jan-Feb picture:

- **Budget:** 40h (2 months x 20h)
- **Estimated:** 70.50h (176% of budget)
- **Actual (Manazer):** 79.49h (199% of budget)
- **Internal cost:** ~$2,782 (blended ~$35/hr)
- **Implied monthly revenue:** $2,800 (at $140/hr for 20h)
- **Result:** 7 weeks of cost nearly equals 1 month of revenue while delivering 4x the contracted hours

### What the Process Says

The overrun is not the primary problem. The primary problem is that the systems designed to prevent an overrun were either absent or misconfigured:

1. **No budget in Manazer** — no automated alerts possible
2. **Wrong budget figure in team documents** — scope decisions made against a ceiling that doesn't exist
3. **No estimation gate** — 55h+ of estimates committed against 20h without review
4. **No weekly variance review** — actual vs budget comparison not happening
5. **No escalation record** — no evidence the January overrun was flagged to client or management
6. **Design defects absorbed by MS budget** — structural unprofitability before any new incidents arrive

### What Needs to Happen

1. **Immediate:** Budget configured in Manazer (20h/month = 1,200 minutes). Billing rate configured. Team informed the contract is 20h, not 40h.

2. **By March 1:** Estimation gate (no ticket exceeding monthly budget without sign-off). Weekly variance review cadence. Estimation problem ticket resolved. Warranty/defect charging clarified for January tickets.

3. **Ongoing:** Monthly iteration review comparing actuals to budget. Audit mechanism to verify controls are in place. Escalation threshold defined (e.g., 75% budget consumption triggers review).

4. **Strategic:** Determine whether MS is priced to be profitable or is absorbing build-phase technical debt. If the latter, the engagement economics need restructuring, not just operational controls.

### The Core Principle

> Revenue builds value. Project discipline protects value. Iteration compounds value.

The SIM MS engagement has revenue (20h/month recurring). It does not have project discipline (no budget configured, no estimation gate, no variance review). Without discipline, the revenue is eroding value rather than compounding it. The RCA and March controls are the path from erosion to iteration.

---

## Files Produced

| File | Purpose | Created |
|------|---------|---------|
| `PERSONA.md` | Jon Gray CFO persona definition | Feb 18 |
| `SIM-REVIEW.md` | Broad two-part review (delivery + MS) | Feb 18 |
| `SIM-MS-DRILLDOWN.md` | 10-question forensic deep-dive | Feb 18 |
| `pr-192-review-draft.md` | 10 PR review comments + overall body | Feb 18 |
| `PR-192-review2.md` | Raw archive of all 21 PR comments | Feb 19 |
| `PR-192-call-guide.md` | Call talking points for Geetha conversation | Feb 19 |
| `PROCESS-LOG.md` | This document — full methodology record | Feb 19 |

---

*Process documented through Jon Gray CFO persona. All data points traceable to Manazer project f7ec5128-ab9a-40c0-99b5-ad1a9d453e71, ClickUp ticket IDs, and PR #192 on ontic-in/manazer.*
