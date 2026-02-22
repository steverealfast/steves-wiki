# Bi-Weekly Productivity Analysis — Standardized Framework

**Version:** 1.0
**Baseline Period:** Feb 1–20, 2026
**Owner:** CEO (Steve)
**Cadence:** Every 2 weeks, aligned to payroll/billing cycles
**Created:** Feb 22, 2026

---

## Part 1: Analysis Objectives

### 1.1 What This Analysis Must Deliver

This is not a report. It is a **decision instrument**. Every bi-weekly cycle must produce three things:

1. **A clear picture of where money went** — broken down by revenue-generating, presales, and internal cost buckets, at both the organizational and individual level.

2. **A ranked list of concerns** — not buried in tables, but surfaced explicitly, prioritized by economic impact, with enough specificity to act on.

3. **Ammunition for hard conversations** — pre-formed questions, grounded in verifiable data, that the CFO can use in 1:1s with the Delivery Head, Tech Lead, and individual contributors. No opinions without numbers.

### 1.2 The CFO's Non-Negotiable Questions

Every cycle must answer these seven questions. If the analysis cannot answer one, it must say so explicitly and flag it as a data gap.

| # | Question | Why It Matters |
|---|----------|---------------|
| 1 | **What percentage of total spend produced client revenue?** | The single most important number. If it's declining, the company is burning faster than it's earning. |
| 2 | **Which individuals are paying for themselves?** | Revenue utilization by person. Anyone below 20% needs justification. Anyone at 0% needs a reason. |
| 3 | **What is the effective hourly rate for client work?** | The real cost of client delivery after dilution from non-client work. If a $30/hr contractor costs $150/hr effective, the margin model is broken. |
| 4 | **Is the presales investment converting?** | Presales is investment, not waste — but only if it converts. Track presales $ period-over-period against pipeline/wins. |
| 5 | **What is the internal platform burn rate?** | Internal tooling (manazer, exo-*, etc.) is absorbed cost. Track it as a % of total spend. If it's growing while revenue % is flat, the platform is consuming the company. |
| 6 | **Who improved and who declined since last period?** | Period-over-period trending per person. Revenue utilization going up = good. Going down = needs investigation. |
| 7 | **What broke since last time?** | New data quality issues, new zero-revenue contributors, new overruns, action items from last cycle that weren't addressed. |

### 1.3 Audiences and What They Need

| Audience | What They Need From This Analysis |
|----------|----------------------------------|
| **CEO (Steve)** | Top-line economics, structural patterns, strategic staffing decisions. 2-minute executive summary + the ranked concern list. |
| **Delivery Head (Geetha)** | Per-person deployment efficiency, ticket discipline gaps, project allocation decisions. Specific names and numbers she can action. |
| **Tech Lead (Sidu)** | Data quality issues, system gaps, platform staffing decisions. Technical actions with deadlines. |
| **Board / Investors** | Quarterly roll-up: Revenue per employee trend, cost structure evolution, operating leverage trajectory. |

---

## Part 2: Standardized Data Pipeline

### 2.1 Data Collection Sequence

Every cycle follows this exact sequence. No shortcuts. Each step produces a verifiable artifact.

```
Step 1: Define Period
         ↓
Step 2: MCP Data Extraction (Manazer)
         ↓
Step 3: Fact-Finding Report
         ↓
Step 4: Independent Verification
         ↓
Step 5: Project Classification (Revenue/Presales/Internal)
         ↓
Step 6: Cost Allocation & Efficiency Calculations
         ↓
Step 7: Activity Quality Audit (Real Output vs Noise)
         ↓
Step 8: Period-over-Period Comparison
         ↓
Step 9: Concern Ranking & Hard Questions
         ↓
Step 10: Report Generation
```

### 2.2 Step-by-Step Data Queries

#### Step 1: Define Period

| Parameter | Value |
|-----------|-------|
| Start Date | First business day of the bi-weekly period |
| End Date | Last business day of the bi-weekly period |
| Business Days | Count excluding weekends and company holidays |
| Previous Period | The prior bi-weekly period (for trending) |

#### Step 2: MCP Data Extraction

Run these queries via `mcp__manazer__rails_runner` in this order:

**Query 2.1 — Contributor Roster**
```ruby
# All cost contributors with activity in the period
Activity.where("occurred_at >= ? AND occurred_at <= ?", start_date, end_date)
  .joins(:contributor).where(contributors: { cost_contributor: true })
  .select("contributors.name, contributors.primary_email, contributors.cost_cents_per_hour")
  .distinct
```

**Query 2.2 — Activity Summary per Contributor**
For each contributor:
```ruby
# Total activities, active days, commits, tickets completed, tickets created, comments, status changes
Activity.where(contributor: c, occurred_at: start_date..end_date)
  .group(:type).count
# Plus: distinct dates for active days
```

**Query 2.3 — Full Project Allocation per Contributor**
```ruby
# Every project touched by every contributor — full breakdown, not top-2
Activity.where(contributor: c, occurred_at: start_date..end_date)
  .joins(:project).group("projects.name").count
```

**Query 2.4 — Project List with Budgets**
```ruby
# All active projects with budget configuration
Project.joins(:activities)
  .where(activities: { occurred_at: start_date..end_date })
  .select(:name, :budget_cents, :budget_minutes, :hourly_billing_rate)
  .distinct
```

**Query 2.5 — Leave Records**
```ruby
# Active leave records overlapping the period
Leave.where(status: "active")
  .where("start_date <= ? AND end_date >= ?", end_date, start_date)
```

**Query 2.6 — PR Activity Check**
```ruby
# GitHub PR activities and contributor mapping status
Activity.where(type: ["GithubPullRequestOpened", "GithubPullRequestClosed"],
               occurred_at: start_date..end_date).count
# Check how many map to cost_contributors
```

#### Step 3: Fact-Finding Report

Produce `PRODUCTIVITY-FACTFINDING-[PERIOD].md` with raw data tables:
- Section 1: Contributor Roster (all metrics per person)
- Section 2: Activity Type Breakdown
- Section 3: Commits by Contributor
- Section 4: Ticket Completions
- Section 5: Project Allocation by Contributor (FULL — not top-2)
- Section 6: Cost Rate Tiers
- Section 7: Leave Records
- Data Gaps & Conflicts

#### Step 4: Independent Verification

Produce `PRODUCTIVITY-VERIFICATION-[PERIOD].md`:
- Re-query every data point independently
- Classify each as VERIFIED / CORRECTED / UNVERIFIABLE / HALLUCINATED
- Target: >98% confidence
- Apply corrections before proceeding

#### Step 5: Project Classification

Maintain a living **Project Classification Register** (see Section 2.3 below). Every project must be classified as Client/Presales/Internal before cost allocation can proceed.

**New projects** appearing in any period must be classified before the analysis can complete. Flag any unclassified projects as a blocking issue.

#### Step 6: Cost Allocation & Efficiency Calculations

For each contributor:
- **Period Cost** = Active Days x 8 hrs x $/hr
- **Revenue Utilization** = Client Activities / Total Activities
- **Effective Hourly Rate** = $/hr / Revenue Utilization
- **Cost/Commit** = Period Cost / Commits
- **Cost/Ticket** = Period Cost / Tickets Completed
- **Cost/Revenue Activity** = Period Cost / Client Activities
- **Cost Allocation** = Period Cost prorated by activity distribution across buckets

#### Step 7: Activity Quality Audit

For each contributor:
- **Real Output** = Commits + Tickets Completed
- **ClickUp Noise** = Comments + Status Changes + Ticket Creations
- **Real Output %** = Real Output / Total Activities
- **Revenue Utilization (Real Only)** = Client Real Output / Total Real Output
- Compare all-activity vs real-output-only revenue utilization

This step prevents the analysis from being driven by comment volume rather than code/delivery output.

#### Step 8: Period-over-Period Comparison

Compare current period to previous period on these metrics:

| Metric | Track At |
|--------|----------|
| Total spend by bucket (Client/Presales/Internal) | Org level |
| Revenue utilization % | Org + per person |
| Effective hourly rate | Per person |
| Real output % (vs noise) | Org + per person |
| Internal platform burn rate | Org level |
| Headcount by bucket | Org level |
| New contributors / departed contributors | Org level |

Flag any metric that moved >5pp or >15% in either direction.

#### Step 9: Concern Ranking & Hard Questions

Produce a ranked list of concerns (see Part 4) and pre-formed questions (see Part 5).

#### Step 10: Report Generation

Each cycle produces **three separate documents**:

1. **Contractor Productivity Analysis** — all contractor economics, deep dives, and contractor-specific concerns
2. **FTE Productivity Analysis** — all FTE economics, deep dives, cost tier analysis, and FTE-specific concerns
3. **Combined Executive Summary** (1 page) — merged top-line numbers, cross-cutting concerns, FTE vs Contractor comparison, hard questions by audience

The Contractor and FTE analyses are **independent documents** that can be shared separately with different audiences. The Combined Executive Summary references both but stands alone for the CEO.

Each document follows the standardized section structure in Part 3, adapted for its scope.

### 2.3 Project Classification Register

**This register must be maintained across periods.** New projects are classified when they first appear. Classifications can be changed if a project's nature shifts (e.g., presales converts to client delivery).

| Project | Classification | Rationale | First Classified | Last Reviewed |
|---------|---------------|-----------|-----------------|--------------|
| SIM Managed Services | Client | Active managed services contract | Feb 2026 | Feb 2026 |
| SIM | Client | Delivery engagement | Feb 2026 | Feb 2026 |
| TASC-Managed-Services | Client | Active managed services | Feb 2026 | Feb 2026 |
| TASC | Client | Delivery engagement | Feb 2026 | Feb 2026 |
| NUS-fin.-reporting-POC | Client | Active POC engagement | Feb 2026 | Feb 2026 |
| nus-contract-generation | Client | Active engagement | Feb 2026 | Feb 2026 |
| scientific-portfolio | Client | Active delivery | Feb 2026 | Feb 2026 |
| Hypernative | Client | Active delivery | Feb 2026 | Feb 2026 |
| Boardroom | Client | Active delivery | Feb 2026 | Feb 2026 |
| starter-pack-fsc-wealth-management-cloud | Presales | Starter pack development | Feb 2026 | Feb 2026 |
| starter-pack-fsc-insurance-cloud | Presales | Starter pack development | Feb 2026 | Feb 2026 |
| starter-pack-service-cloud | Presales | Starter pack development | Feb 2026 | Feb 2026 |
| starter-pack-manufacturing-cloud | Presales | Starter pack development | Feb 2026 | Feb 2026 |
| starter-pack-fsc-wealth-mgmt-cloud-base-org | Presales | Starter pack base org | Feb 2026 | Feb 2026 |
| starter-pack-healthcloud | Presales | Starter pack development | Feb 2026 | Feb 2026 |
| starter-pack-a4x-sales | Presales | Starter pack development | Feb 2026 | Feb 2026 |
| starter-packs | Presales | Meta-project for starter pack work | Feb 2026 | Feb 2026 |
| Pre-Sales-Delivery | Presales | Presales coordination | Feb 2026 | Feb 2026 |
| service-cloud-starter-pack-optimization | Presales | Optimization of starter packs | Feb 2026 | Feb 2026 |
| manazer | Internal | Internal analytics platform | Feb 2026 | Feb 2026 |
| exo-sf-core-agent | Internal | Internal platform | Feb 2026 | Feb 2026 |
| exo-code-server | Internal | Internal platform | Feb 2026 | Feb 2026 |
| exo-cli | Internal | Internal platform | Feb 2026 | Feb 2026 |
| exo-code-otel-service | Internal | Internal platform | Feb 2026 | Feb 2026 |
| exo-agent-builder | Internal | Internal platform | Feb 2026 | Feb 2026 |
| exo-help | Internal | Internal platform | Feb 2026 | Feb 2026 |
| harvester | Internal | Internal tooling | Feb 2026 | Feb 2026 |
| New-Website | Internal | Company website | Feb 2026 | Feb 2026 |
| content-branding | Internal | Marketing/branding | Feb 2026 | Feb 2026 |

**Classification rules:**
- **Client** = Active contract generating revenue. Money is flowing from the client to us.
- **Presales** = Investment in future revenue. No current revenue. Justified by pipeline.
- **Internal** = No revenue path. Operational cost absorbed by the company.
- **Reclassification trigger:** When a presales project converts to a client engagement, it moves from Presales to Client. This must be tracked as a win.

---

## Part 3: Standardized Report Structure

### 3.1 Executive Summary (Page 1 — must stand alone)

Every report opens with the same table. Period-over-period changes shown.

```
┌─────────────────────────────────────────────────────────────────┐
│  PRODUCTIVITY ANALYSIS — [Period Dates]                         │
│  Period [N] | [X] Business Days | [Y] Contributors              │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  TOTAL SPEND          $XXX,XXX    (prev: $XXX,XXX  Δ XX%)       │
│  ├─ Client Revenue    $XX,XXX     XX.X%  (prev: XX.X%  Δ Xpp)  │
│  ├─ Presales          $XX,XXX     XX.X%  (prev: XX.X%  Δ Xpp)  │
│  └─ Internal          $XX,XXX     XX.X%  (prev: XX.X%  Δ Xpp)  │
│                                                                  │
│  REVENUE UTILIZATION  XX.X%       (prev: XX.X%  Δ Xpp)         │
│  REAL OUTPUT RATE     XX.X%       (prev: XX.X%  Δ Xpp)         │
│  INTERNAL BURN RATE   $XX,XXX/pd  ($XXXK annualized)           │
│                                                                  │
│  TOP CONCERNS:                                                   │
│  1. [Highest-impact concern — one line]                          │
│  2. [Second concern — one line]                                  │
│  3. [Third concern — one line]                                   │
│                                                                  │
│  BASELINE (Period 1): Feb 1-20, 2026                            │
│  Client: 21.5% | Presales: 35.9% | Internal: 42.6%             │
└─────────────────────────────────────────────────────────────────┘
```

### 3.2 Report Sections — Contractor Analysis

| Section | Content | Purpose |
|---------|---------|---------|
| **1. Executive Summary** | Top-line contractor numbers, period-over-period, top concerns | Quick read |
| **2. Methodology** | Definitions, cost bucket rules, calculation methods | Consistency anchor — same every period |
| **3. Contractor Roster — Ranked by Revenue** | All contractors ranked by revenue utilization | Who is paying for themselves? |
| **4. Cost Allocation** | Per-contractor breakdown: Client/Presales/Internal | Where did each contractor's cost go? |
| **5. Activity Quality Audit** | Real output vs noise, per contractor | Prevents comment-driven cost allocation |
| **6. Revenue Efficiency** | Cost/Commit, Cost/Ticket, Cost/Revenue Activity | Output efficiency per dollar |
| **7. Period-over-Period Trends** | Key metrics compared to previous period | Direction of travel |
| **8. Individual Deep Dives** | Detailed per-person analysis (flagged contractors only) | Evidence base for hard conversations |
| **9. Concern Ranking** | Contractor-specific issues with economic impact | Decision priorities |
| **10. Action Items** | Specific, assigned, with deadlines | Accountability |
| **11. Data Caveats** | Known limitations, data gaps, conflicts | Honest about what we don't know |

### 3.3 Report Sections — FTE Analysis

| Section | Content | Purpose |
|---------|---------|---------|
| **1. Executive Summary** | Top-line FTE numbers, FTE vs Contractor comparison, period-over-period | Quick read |
| **2. Methodology** | Same definitions as Contractor analysis for comparability | Consistency |
| **3. FTE Roster — Ranked by Revenue** | All FTEs ranked by revenue utilization | Who is paying for themselves? |
| **4. Cost Allocation** | Per-FTE breakdown: Client/Presales/Internal | Where did each FTE's cost go? |
| **5. Cost Tier Analysis** | Spend and output aggregated by $30/$50/$80/$120 tiers | Are higher tiers delivering higher value? |
| **6. Revenue Efficiency** | Cost/Commit, Cost/Ticket, Cost/Revenue Activity | Output efficiency per dollar |
| **7. Internal Platform Investment** | Per-platform breakdown (manazer, exo-*, etc.) | Where is internal spend going? |
| **8. Period-over-Period Trends** | Key metrics compared to previous period | Direction of travel |
| **9. Individual Deep Dives** | Detailed analysis (flagged FTEs only) | Evidence base for hard conversations |
| **10. Low-Activity FTE Summary** | FTEs with minimal visible output | Ghost cost identification |
| **11. Concern Ranking** | FTE-specific issues with economic impact | Decision priorities |
| **12. Action Items** | Specific, assigned, with deadlines | Accountability |
| **13. Data Caveats** | Known limitations, data gaps, conflicts | Honest about what we don't know |

### 3.4 Report Sections — Combined Executive Summary

| Section | Content | Purpose |
|---------|---------|---------|
| **1. Command Summary** | Total org spend, bucket split, period-over-period | CEO reads this in 30 seconds |
| **2. FTE vs Contractor Comparison** | Side-by-side economics | Structural staffing patterns |
| **3. Combined Concern Ranking** | Top concerns across both analyses, merged and ranked | What needs attention first |
| **4. Hard Questions** | Pre-formed questions by audience | Ammunition for conversations |
| **5. Drilldown Queue** | All open and new investigations | Nothing gets lost |
| **6. Revenue Per Employee Trend** | The single enterprise metric | Compounding or eroding? |

### 3.5 What Triggers a Deep Dive

Not every contributor gets a deep dive every period. Deep dives are reserved for individuals who trigger one or more of these flags:

| Flag | Threshold | Rationale |
|------|-----------|-----------|
| **Zero revenue utilization** | 0% client activities | Paying someone with no revenue output |
| **Revenue utilization drop** | >10pp decline from prior period | Something changed — find out what |
| **Effective hourly rate spike** | >$200/hr effective for client work | Dilution making client work uneconomical |
| **High cost, low output** | >$5,000 period cost, <20 activities | Expensive contributor with little visible work |
| **Commit-to-ticket ratio** | >20:1 commits per ticket | Code being written but nothing getting completed |
| **Noise ratio** | >80% of activities are ClickUp noise | Volume without verifiable output |
| **New joiner** | First or second period in roster | Ramp-up monitoring |
| **Departed** | In previous roster but absent this period | Track offboarding impact |
| **Internal allocation spike** | >70% internal for a contractor | Contractor doing internal work — staffing question |
| **Leave/activity conflict** | Active on leave days or weekends | Compliance concern |

---

## Part 4: Concern Ranking Framework

### 4.1 How Concerns Are Ranked

Every concern gets scored on two dimensions:

**Economic Impact** (1-5):
1. < $500/period impact
2. $500-$2,000/period
3. $2,000-$5,000/period
4. $5,000-$15,000/period
5. > $15,000/period

**Urgency** (1-5):
1. Informational — monitor next period
2. Attention needed — flag in next review
3. Action required this cycle
4. Escalation — needs management decision within 1 week
5. Critical — needs immediate action (contractual, compliance, or financial risk)

**Concern Score** = Impact x Urgency (max 25)

### 4.2 Concern Categories

| Category | What It Covers | Typical Questions |
|----------|---------------|-------------------|
| **Revenue Leakage** | Contributors with declining or zero revenue utilization | Why is this person not on client work? |
| **Cost Misallocation** | High-rate resources on low-rate work (e.g., $80/hr on internal tooling) | Should this be a $30/hr resource? |
| **Pipeline Risk** | Large presales investment with no conversion signals | Is this pipeline real? When does it convert? |
| **Delivery Discipline** | Ticket completion gaps, estimation overruns, scope creep | Are we finishing work or just starting it? |
| **Data Quality** | PR mapping gaps, missing budgets, leave conflicts | Can we trust what Manazer is telling us? |
| **Staffing Structure** | Contractors on internal work, FTEs with no activity | Right person in the right seat? |
| **Trend Reversal** | Any metric that moved >5pp in the wrong direction | What changed and is it intentional? |

### 4.3 Baseline Concerns (Period 1 — Feb 1-20, 2026)

These are the concerns from the baseline period. Each subsequent period tracks whether they improved, worsened, or are unchanged.

| # | Concern | Impact | Urgency | Score | Status |
|---|---------|--------|---------|-------|--------|
| 1 | **42.6% of total spend is internal** — $55,681/pd ($1.45M annualized) | 5 | 3 | 15 | BASELINE |
| 2 | **71% of all contractor activity is ClickUp noise** — cost allocation driven by comments not code | 4 | 4 | 16 | BASELINE |
| 3 | **$80/hr FTEs: $30,143/pd on internal** — 3 FTEs (Karthik, Srini, Jewel James) = $490K annualized internal | 5 | 3 | 15 | BASELINE |
| 4 | **Manazer platform: $27,250/pd** — 18 contributors, $708K annualized on one internal tool | 5 | 3 | 15 | BASELINE |
| 5 | **Only 21.5% of combined spend produces client revenue** — for every $1 spent, 21.5 cents generates income | 5 | 4 | 20 | BASELINE |
| 6 | **Presales $46,952/pd ($1.22M annualized) with no conversion tracking** — no pipeline-to-revenue mapping | 4 | 3 | 12 | BASELINE |
| 7 | **PR data unmapped** — 446 PRs, 0 attributed to cost contributors | 3 | 2 | 6 | BASELINE |
| 8 | **4 of 29 projects have budgets** — no budget = no overrun detection | 3 | 3 | 9 | BASELINE |
| 9 | **Contractors on 100% internal** — Manas ($2,880/pd) and Shantanu (50% = $1,560/pd) | 3 | 2 | 6 | BASELINE |
| 10 | **Ticket completion discipline** — 4 contractors with >60:1 commit-to-ticket ratio | 2 | 2 | 4 | BASELINE |

---

## Part 5: Hard Questions Template

### 5.1 Structure

Every hard question follows this format:

```
QUESTION: [The exact question to ask]
DATA: [The specific number that prompted it]
CONTEXT: [Why this matters economically]
ACCEPTABLE ANSWER: [What a satisfactory response looks like]
UNACCEPTABLE ANSWER: [What a deflection or non-answer looks like]
```

### 5.2 Standing Questions (Ask Every Period)

#### For Geetha (Delivery Head)

**Q1: Revenue Deployment**
- QUESTION: "Of the [X] delivery resources you manage, [Y] had zero client revenue this period. Walk me through why each one is not on client work."
- DATA: [Count of zero-revenue contributors]
- CONTEXT: Every person at 0% revenue is pure cost with no income offset.
- ACCEPTABLE: Specific reason per person (leave, ramp-up, intentional internal assignment with end date).
- UNACCEPTABLE: "They were busy" without specifying what the work produced.

**Q2: Activity Quality**
- QUESTION: "[X]% of your team's activity this period was ClickUp comments and status changes, not code or completed tickets. What are you seeing in terms of actual output?"
- DATA: [Noise % from Activity Quality Audit]
- CONTEXT: Cost allocation is currently driven by comment distribution. If comments don't represent real work, the revenue utilization numbers are inflated.
- ACCEPTABLE: Evidence that high-comment contributors are doing substantive technical discussions, code reviews through comments, or client communication.
- UNACCEPTABLE: "That's just how ClickUp works."

**Q3: Ticket Completion**
- QUESTION: "[Names] had [X] commits but only [Y] tickets completed. Are tickets being broken down properly, or is work being shipped without ticket closure?"
- DATA: [Commit-to-ticket ratios from efficiency section]
- CONTEXT: Commits without ticket completion means we can't measure throughput, track velocity, or calculate per-ticket economics.
- ACCEPTABLE: Explanation of ticket granularity issues with plan to fix. Or: tickets are genuinely large-scope.
- UNACCEPTABLE: No awareness of the gap.

**Q4: Cost Tier Efficiency**
- QUESTION: "We have [X] people at $80/hr spending [Y]% on internal work. At what point should that work be done by $30-50/hr resources?"
- DATA: [$80/hr tier internal allocation]
- CONTEXT: The $80/hr tier should theoretically deliver higher-value work. If they're on internal tooling, the cost-to-value ratio is inverted.
- ACCEPTABLE: Specific justification why this work requires $80/hr expertise (architecture decisions, mentoring, code review that prevents defects). With a plan to transition execution to lower tiers.
- UNACCEPTABLE: "They've always worked on that."

#### For Sidu (Tech Lead)

**Q5: Data Quality**
- QUESTION: "We still have [X] PRs that can't be attributed to any contributor. What's the timeline for fixing the GitHub email mapping?"
- DATA: [PR attribution gap count]
- CONTEXT: Code review and merge activity is invisible without PR mapping. This understates contributors who do heavy code review.
- ACCEPTABLE: Timeline with specific completion date.
- UNACCEPTABLE: "We'll get to it."

**Q6: Platform Staffing**
- QUESTION: "[X] people touched the manazer platform this period but only [Y] had more than 10 activities. Who is the core team and who is drive-by?"
- DATA: [Manazer contributor count and activity distribution]
- CONTEXT: 18 people touching one internal project creates coordination cost without proportional output.
- ACCEPTABLE: Defined core team (3-5 people) with intentional allocation. Others acknowledged as incidental.
- UNACCEPTABLE: "Everyone contributes a little."

**Q7: Budget Configuration**
- QUESTION: "[X] of [Y] active projects have no budget configured. When will the remaining [Z] have budgets set?"
- DATA: [Budget gap from project query]
- CONTEXT: Without budgets, no overrun detection. The SIM MS overrun was invisible for 5 weeks because no budget was configured.
- ACCEPTABLE: Specific date, all projects budgeted.
- UNACCEPTABLE: "Some projects don't have budgets."

#### For CEO (Self-Review / Board Prep)

**Q8: Revenue Per Employee Trend**
- QUESTION: "Is revenue per employee expanding, flat, or contracting?"
- DATA: [Client revenue $ / headcount, compared to prior period]
- CONTEXT: Growth without RPE expansion = cost-led growth. Compresses enterprise value.
- This question is answered by the analysis itself — it's the CEO's self-check.

**Q9: Presales Conversion**
- QUESTION: "We invested $[X] in presales this period. Which presales projects have active pipeline? What's the expected conversion timeline?"
- DATA: [Presales allocation by project]
- CONTEXT: $1.22M annualized presales requires $2-3M expected pipeline to justify.
- This question should be directed to Paulomi/Geetha.

**Q10: Internal Investment Trajectory**
- QUESTION: "Internal platform spend is [X]% of total. Is this going up, staying flat, or coming down? When does it peak?"
- DATA: [Internal % trend over periods]
- CONTEXT: Internal investment should have a peak and decline as platforms mature. If it's climbing without a ceiling, it's consuming the company.

### 5.3 Triggered Questions (Ask When Thresholds Are Hit)

| Trigger | Question |
|---------|----------|
| Any contributor drops >10pp in revenue utilization | "[Name] went from [X]% to [Y]% revenue utilization. What changed in their assignment?" |
| New contributor appears with 0% revenue | "[Name] is new this period with zero client work. What's the ramp plan and when do they start revenue work?" |
| Any project >150% budget utilization | "[Project] is at [X]% of budget. Who approved the scope beyond budget? What's the client exposure?" |
| Total internal % increases >3pp | "Internal spend went from [X]% to [Y]%. Was this planned? What's driving it?" |
| Any contributor >85% noise ratio | "[Name] has [X]% noise ratio — [Y] comments vs [Z] commits. What are they actually delivering?" |
| Presales project >3 periods with no conversion | "[Project] has been presales for [X] periods with $[Y] total investment. Is there real pipeline here?" |

---

## Part 6: Drilldown Protocol

### 6.1 What Is a Drilldown?

A drilldown is a deeper investigation triggered by something in the bi-weekly analysis that cannot be answered with the standard data. It requires additional queries, cross-referencing, or qualitative investigation.

### 6.2 Drilldown Queue Structure

Every analysis produces a **Drilldown Queue** — a list of investigations that need to happen before or during the next cycle.

| Field | Description |
|-------|-------------|
| **ID** | Sequential: D-[period]-[number] (e.g., D-P1-001) |
| **Trigger** | What in the analysis prompted this |
| **Question** | The specific question to answer |
| **Data Needed** | What additional data or queries are required |
| **Owner** | Who is responsible for investigating |
| **Deadline** | When the investigation must be complete |
| **Status** | Open / In Progress / Resolved / Carried Forward |
| **Resolution** | What was found and what action was taken |

### 6.3 Baseline Drilldown Queue (Period 1)

| ID | Trigger | Question | Owner | Deadline | Status |
|----|---------|----------|-------|----------|--------|
| D-P1-001 | 71% noise ratio | Spot-check 10 ClickUp comments each for Rakesh (299), Nikhil (265), Ganesh (225) — are they substantive or perfunctory? | Geetha | Period 2 | OPEN |
| D-P1-002 | 259 tickets created by Rakesh | Audit what happened to the 178 tickets Rakesh created but didn't complete. Still open? Reassigned? Abandoned? | Geetha | Period 2 | OPEN |
| D-P1-003 | Das Animesh ramp | Validate Das Animesh has clear ownership of deliverables, not just tagged in conversations. | Geetha | Period 2 | OPEN |
| D-P1-004 | 446 PRs unmapped | Map GitHub noreply emails to Manazer contributor records. | Sidu | Period 2 | OPEN |
| D-P1-005 | 4 of 29 projects budgeted | Configure budgets for all active client and presales projects. | Sidu | Period 2 | OPEN |
| D-P1-006 | Manas 100% internal | Determine if manazer development is temporary (acceptable) or ongoing (should be FTE). | CEO | Period 3 | OPEN |
| D-P1-007 | $80/hr FTEs on internal | Decision: Should Karthik, Srini, Jewel James internal work be done by lower-tier resources? | Geetha/CEO | Period 3 | OPEN |
| D-P1-008 | Presales $1.22M annualized | Map presales projects to pipeline value. Expected conversion timelines. | Paulomi/Geetha | Period 3 | OPEN |
| D-P1-009 | Leave/activity conflicts | Investigate Asarar Ahmed (15 active days + 4 leave days) and Akhil (64 activities on leave day). | Sidu | Period 2 | OPEN |
| D-P1-010 | SIM MS budget overrun | Verify March 1 controls are in place: budget configured, estimation gate, weekly variance review. | Geetha | Period 2 | OPEN |

### 6.4 Drilldown Lifecycle

```
OPEN → Assigned owner reviews
     → IN PROGRESS during investigation
     → RESOLVED with findings documented in next analysis
     → or CARRIED FORWARD if unresolved (max 2 carries before escalation)
```

**Escalation rule:** Any drilldown carried forward twice (3 periods total) automatically becomes a concern in the Concern Ranking with Urgency = 4 (escalation).

---

## Part 7: Period-over-Period Tracking

### 7.1 Trend Table

This table is cumulative. Each row represents one bi-weekly period.

**Contractor Trend:**

| Period | Dates | Days | Head | Total $ | Client % | Presales % | Internal % | Real Output % | Internal Burn |
|--------|-------|------|------|---------|----------|-----------|------------|--------------|--------------|
| P1 (Baseline) | Feb 1-20 | 15 | 9 | $27,360 | 29.4% | 53.4% | 17.2% | 29% | $4,696 |
| P2 | | | | | | | | | |

**FTE Trend:**

| Period | Dates | Days | Head | Total $ | Client % | Presales % | Internal % | Internal Burn |
|--------|-------|------|------|---------|----------|-----------|------------|--------------|
| P1 (Baseline) | Feb 1-20 | 15 | 25 | $103,440 | 19.5% | 31.3% | 49.3% | $50,985 |
| P2 | | | | | | | | |

**Combined Trend:**

| Period | Dates | Head | Total $ | Client % | Presales % | Internal % | Rev/Person | Internal Burn |
|--------|-------|------|---------|----------|-----------|------------|-----------|--------------|
| P1 (Baseline) | Feb 1-20 | 34 | $130,800 | 21.5% | 35.9% | 42.6% | $828 | $55,681 |
| P2 | | | | | | | | |

### 7.2 Per-Person Trending

For every contributor who appears in 2+ consecutive periods:

| Contributor | P1 Rev Util | P2 Rev Util | Delta | P1 Eff $/hr | P2 Eff $/hr | Direction |
|-------------|------------|------------|-------|-------------|-------------|-----------|
| (populated each period) | | | | | | |

### 7.3 Concern Status Tracking

| Concern | P1 Score | P2 Score | P3 Score | Direction | Action Taken |
|---------|----------|----------|----------|-----------|-------------|
| 42.6% internal spend | 15 | | | | |
| 71% noise ratio | 16 | | | | |
| (etc.) | | | | | |

---

## Part 8: Dashboard Design

### 8.1 Design Philosophy

The dashboard is not a data visualization exercise. It is a **decision acceleration tool**. Every element on the dashboard must answer a question that leads to an action.

**Three rules:**
1. **If it doesn't prompt a decision, it doesn't belong on the dashboard.**
2. **Red items get attention first.** The dashboard must surface problems before showing health.
3. **Drill-down, not drill-around.** Every summary metric must link to contributor-level detail.

### 8.2 Dashboard Layout — Three Tiers

#### Tier 1: Command View (CEO — 30 seconds)

What the CEO sees on login. Five numbers and a concern list.

```
┌──────────────────────────────────────────────────────────────────┐
│                     PERIOD [N] — [Dates]                         │
│                                                                   │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐         │
│  │ REVENUE  │  │ PRESALES │  │ INTERNAL │  │ TOTAL    │         │
│  │  21.5%   │  │  35.9%   │  │  42.6%   │  │ $130.8K  │         │
│  │  ▲ 2.1pp │  │  ▼ 1.3pp │  │  ▼ 0.8pp │  │  ▲ 3.2%  │         │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘         │
│                                                                   │
│  ┌──────────────────────────────────────────────────────────┐    │
│  │ TOP CONCERNS                                    [Score]  │    │
│  │ 🔴 Only 21.5% of spend produces revenue          [20]   │    │
│  │ 🔴 71% contractor activity is ClickUp noise       [16]   │    │
│  │ 🟡 $80/hr FTEs: $490K annualized on internal     [15]   │    │
│  │ 🟡 Manazer platform: $708K annualized             [15]   │    │
│  │ 🟢 Project tagging: 100% classified               [—]    │    │
│  └──────────────────────────────────────────────────────────┘    │
│                                                                   │
│  ┌────────────────────────┐  ┌────────────────────────┐          │
│  │ REVENUE PER EMPLOYEE   │  │ DRILLDOWNS OPEN        │          │
│  │ $828/period             │  │ 10 open / 0 overdue    │          │
│  │ Trend: ▲ / ▼ / →       │  │ 3 due this period      │          │
│  └────────────────────────┘  └────────────────────────┘          │
└──────────────────────────────────────────────────────────────────┘
```

**Color coding:**
- 🔴 Red: Score ≥ 16 or Urgency = 5
- 🟡 Amber: Score 9-15
- 🟢 Green: Score ≤ 8 or resolved

#### Tier 2: Allocation View (CFO — 2 minutes)

Two visualizations side by side:

**Left: Cost Waterfall by Bucket**
```
$130,800 Total
├── $28,167 Client (21.5%) ███████
├── $46,952 Presales (35.9%) ████████████
└── $55,681 Internal (42.6%) ██████████████

Previous period overlay shown as ghost bars for comparison.
```

**Right: Contributor Heatmap (Revenue Utilization)**
```
                    0%          50%          100%
Prabhat        ████████████████████████████████  100%
Isaac          ███████████████████████████████   98%
Akhil          ████████████████████████████      89%
Rishi          ████████████████████████████████  100%
Anirudh        █████████████████                 55%
...
Asarar         ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  0%
Paharlaya      ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  0%
Manas          ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  0%

Red highlight on anyone who dropped >10pp from prior period.
```

#### Tier 3: Operational Detail (Delivery Head / Tech Lead — 5 minutes)

**Tab 1: Contributor Economics Table**
Sortable/filterable table with all metrics per contributor:
- Name, Rate, Type (FTE/Contractor), Period Cost
- Revenue Util %, Effective $/hr
- Client $, Presales $, Internal $
- Commits, Tickets Done, Real Output %, Noise %
- Period-over-period delta arrows on key metrics
- Click any row → individual deep dive

**Tab 2: Project Economics**
- Per-project view: budget, actual spend, contributor count, activity count
- Budget variance (where budgets exist)
- Presales projects with conversion status

**Tab 3: Activity Quality**
- Real Output vs Noise breakdown per contributor
- Comment-to-commit ratios
- Revenue utilization: all-activity vs real-output-only comparison

**Tab 4: Trend Lines**
- Revenue %, Presales %, Internal % over time (line chart)
- Per-person revenue utilization sparklines
- Internal platform burn rate over time
- Headcount by bucket over time

**Tab 5: Action Tracker**
- All open drilldowns with status, owner, deadline
- Concern ranking with period-over-period score changes
- Overdue items highlighted

### 8.3 Alert System

The dashboard should surface alerts without requiring the user to look for problems:

| Alert Type | Trigger | Display |
|------------|---------|---------|
| **New Zero-Revenue Contributor** | Anyone who had >0% last period and is now 0% | Red badge on contributor heatmap |
| **Revenue Utilization Drop** | Any contributor down >10pp | Red arrow on heatmap |
| **Budget Overrun** | Any project >100% budget utilization | Red flag on project table |
| **Overdue Drilldown** | Any drilldown past its deadline | Badge count on action tracker |
| **Internal Spike** | Internal % up >3pp from prior period | Amber alert on command view |
| **Carried Forward x2** | Any drilldown carried forward twice | Auto-escalation notice |

### 8.4 Implementation Considerations

**Phase 1 (Now — Manual):**
The dashboard exists as the structured markdown report produced each bi-weekly cycle. The format in this framework IS the dashboard. Every section maps to a dashboard tier.

**Phase 2 (When Manazer supports it):**
Build these views natively in Manazer:
- Project classification as a first-class field
- Budget vs actual tracking with alerts
- Contributor revenue utilization as a computed field
- Period-over-period comparison engine
- PR author mapping (fix the GitHub email gap first)

**Phase 3 (Full dashboard):**
Web-based dashboard pulling from Manazer API:
- Real-time data refresh
- Interactive drill-down
- Automated alert notifications (Slack/email)
- Exportable board-ready summaries
- Historical trending with adjustable periods

### 8.5 What the Dashboard Does NOT Show

Intentional exclusions:
- **Individual hours worked** — Manazer doesn't track hours; activity-based proxy is explicitly stated
- **Billing rates or margins** — until billing rates are configured in Manazer
- **Quality metrics** — bug rates, defect density, customer satisfaction (not in Manazer)
- **PR/code review activity** — until GitHub email mapping is fixed
- **Subjective performance ratings** — this is an economic instrument, not an HR tool

---

## Part 9: Running the Analysis — Operator's Guide

### 9.1 Pre-Flight Checklist

Before starting each bi-weekly analysis:

- [ ] Previous period's report is finalized and filed
- [ ] Project Classification Register is up to date
- [ ] Any new projects since last period have been classified
- [ ] Drilldown queue from previous period has been reviewed
- [ ] Period dates are confirmed (start, end, business days)
- [ ] Previous period's trend data is accessible for comparison

### 9.2 Naming Conventions

```
PRODUCTIVITY-FACTFINDING-P[N].md          — Raw data extraction (all contributors)
PRODUCTIVITY-VERIFICATION-P[N].md         — Independent verification
CONTRACTOR-PRODUCTIVITY-ANALYSIS-P[N].md  — Contractor-only analysis
FTE-PRODUCTIVITY-ANALYSIS-P[N].md         — FTE-only analysis
COMBINED-EXECUTIVE-SUMMARY-P[N].md        — Merged summary with cross-cutting concerns
```

Period 1 (baseline) files retain their original names. From Period 2 onward, use the P[N] convention.

**Note:** The fact-finding and verification steps cover ALL contributors (FTE + Contractor) in a single pass — the data collection is unified. The split into separate Contractor and FTE analyses happens at Step 6 (cost allocation) onward.

### 9.3 Time Budget per Cycle

| Phase | Estimated Time | Notes |
|-------|---------------|-------|
| Data extraction (MCP queries) | 30 min | Mostly automated |
| Fact-finding report | 30 min | Templated |
| Verification | 30 min | Spot-check + re-query |
| Classification of new projects | 10 min | Only if new projects appear |
| Cost allocation & calculations | 30 min | Formulaic |
| Activity quality audit | 20 min | Templated |
| Period-over-period comparison | 20 min | From Period 2 onward |
| Concern ranking | 20 min | Judgment required |
| Hard questions drafting | 20 min | Judgment required |
| Report assembly | 30 min | Templated sections |
| **Total** | **~4 hours** | Gets faster with practice |

### 9.4 Quality Gates

The analysis is not complete until:

1. [ ] Verification report shows >95% confidence
2. [ ] Every contributor's project allocation is COMPLETE (full MCP refresh, not top-2)
3. [ ] Every project is classified (zero unclassified)
4. [ ] Activity quality audit is included (not skipped)
5. [ ] Period-over-period comparison is included (from P2 onward)
6. [ ] Concern ranking is populated with scores
7. [ ] Hard questions are drafted for each audience
8. [ ] Drilldown queue is updated (previous items + new items)
9. [ ] Executive summary can stand alone (CEO should not need to read beyond page 1)

---

## Appendix A: Baseline Metrics (Period 1 — Feb 1-20, 2026)

These are the numbers all future periods are measured against.

### Contractor Baseline

| Metric | Value |
|--------|-------|
| Headcount | 9 |
| Total Estimated Spend | $27,360 |
| Client Revenue % | 29.4% ($8,045) |
| Presales % | 53.4% ($14,619) |
| Internal % | 17.2% ($4,696) |
| Revenue Per Contractor | $894 |
| Real Output % | 29% |
| Noise % | 71% |

### FTE Baseline

| Metric | Value |
|--------|-------|
| Headcount | 25 |
| Total Estimated Spend | $103,440 |
| Client Revenue % | 19.5% ($20,122) |
| Presales % | 31.3% ($32,333) |
| Internal % | 49.3% ($50,985) |
| Revenue Per FTE | $805 |
| Manazer Burn Rate | $24,370/pd |
| $80/hr Tier Internal Spend | $30,143/pd |

### Combined Baseline

| Metric | Value |
|--------|-------|
| Headcount | 34 |
| Total Estimated Spend | $130,800 |
| Client Revenue % | 21.5% ($28,167) |
| Presales % | 35.9% ($46,952) |
| Internal % | 42.6% ($55,681) |
| Revenue Per Person | $828 |
| Manazer Burn Rate (All) | $27,250/pd ($708K annualized) |
| Total Internal Burn Rate | $55,681/pd ($1.45M annualized) |

### Individual Baselines (Top Performers)

| Contributor | Type | Revenue Util | Effective $/hr | Cost/Commit |
|-------------|------|-------------|---------------|-------------|
| Prabhat Ranjan | Contractor | 100% | $30.00 | $64.62 |
| Isaac | FTE | 97.9% | $30.64 | $18.46 |
| Akhil | FTE | 89.2% | $56.05 | $29.85 |
| Rishi | FTE | 100% | $80.00 | — |

### Individual Baselines (Concerns)

| Contributor | Type | Revenue Util | Issue |
|-------------|------|-------------|-------|
| Paharlaya Basnet | Contractor | 0% | 100% presales |
| Manas | Contractor | 0% | 100% internal |
| Karthik | FTE | 0% | 85% internal at $80/hr |
| Srini | FTE | 6.6% | 89% internal at $80/hr |
| Asarar Ahmed | FTE | 0% | 53% presales, 47% internal |

---

*This document defines the standard operating procedure for all future bi-weekly productivity analyses. The baseline period (Feb 1-20, 2026) establishes the starting point for all trending. Every subsequent analysis follows this framework exactly — deviations must be documented and justified.*
