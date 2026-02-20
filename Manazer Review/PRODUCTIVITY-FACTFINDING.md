# Fact-Finding Report: Employee Productivity & Output

**Scope:** Manazer + GitHub commits | Employee productivity, daily output, FTE vs contractor comparison | CEO + Delivery Head
**Data Sources Queried:** Manazer MCP (Contributors, Activities, Projects, Leaves)
**Period:** Feb 1 – Feb 20, 2026 (15 business days: Feb 2-6, 9-13, 16-20)
**Generated:** Feb 20, 2026

---

## Section 1: Contributor Roster — Activity Summary

36 contributors (cost_contributor=true) recorded activity in this period.

| Contributor | Cost $/hr | Total Activities | Active Days | Avg Activities/Active Day | Commits | Tickets Completed | Tickets Created |
|---|---:|---:|---:|---:|---:|---:|---:|
| Rakesh Poddar | $30 | 934 | 15 | 62.3 | 99 | 79 | 258 |
| Nikhil Galagali | $30 | 475 | 14 | 33.9 | 166 | 2 | 4 |
| Ganesh Hegde | $30 | 454 | 13 | 34.9 | 150 | 2 | 1 |
| Akhil | $50 | 408 | 10 | 40.8 | 134 | 13 | 9 |
| Bharat | $30 | 367 | 14 | 26.2 | 103 | 6 | 5 |
| Saurav Shah | $50 | 359 | 14 | 25.6 | 118 | 25 | 28 |
| Asarar Ahmed | $30 | 358 | 15 | 23.9 | 165 | 3 | 1 |
| Paharlaya Basnet | $30 | 351 | 12 | 29.3 | 131 | 2 | 2 |
| Megha Bc | $30 | 334 | 13 | 25.7 | 79 | 6 | 10 |
| Isaac | $30 | 330 | 13 | 25.4 | 169 | 12 | 31 |
| Prabhat Ranjan | $30 | 250 | 14 | 17.9 | 52 | 6 | 7 |
| Shantanu | $30 | 246 | 13 | 18.9 | 79 | 10 | 10 |
| Jewel James | $80 | 215 | 16 | 13.4 | 25 | 5 | 6 |
| Geetha | $80 | 212 | 14 | 15.1 | 46 | 17 | 26 |
| Aniket | $50 | 211 | 13 | 16.2 | 62 | 6 | 8 |
| Manas | $30 | 190 | 12 | 15.8 | 54 | 19 | 17 |
| Priyanshu Gaur | $50 | 188 | 15 | 12.5 | 15 | 12 | 5 |
| Sidu | $80 | 133 | 13 | 10.2 | 7 | 7 | 7 |
| Saurabh | $30 | 102 | 10 | 10.2 | 32 | 5 | 12 |
| Srini | $80 | 91 | 11 | 8.3 | 3 | 3 | 5 |
| Anirudh | $80 | 82 | 8 | 10.3 | 0 | 3 | 6 |
| Karthik | $80 | 61 | 12 | 5.1 | 23 | 5 | 6 |
| Rohit T | $30 | 56 | 10 | 5.6 | 36 | 1 | 1 |
| Das Animesh | $30 | 47 | 6 | 7.8 | 5 | 1 | 3 |
| Paulomi | $120 | 43 | 8 | 5.4 | 29 | 1 | 2 |
| It-admin | $30 | 39 | 3 | 13.0 | 0 | 0 | 0 |
| Exo | $30 | 38 | 7 | 5.4 | 38 | 0 | 0 |
| Kaathyayani | $30 | 19 | 8 | 2.4 | 0 | 19 | 0 |
| Harsh | $50 | 16 | 5 | 3.2 | 13 | 3 | 0 |
| Suraj | $50 | 10 | 5 | 2.0 | 4 | 2 | 1 |
| Rajnish | $80 | 10 | 3 | 3.3 | 0 | 3 | 1 |
| Sumanth | $50 | 9 | 4 | 2.3 | 0 | 2 | 1 |
| Animesh | $30 | 6 | 2 | 3.0 | 4 | 0 | 0 |
| Rishi | $80 | 4 | 3 | 1.3 | 3 | 0 | 0 |
| Piyush Sinha | $30 | 2 | 1 | 2.0 | 0 | 0 | 1 |
| Jeetal Shah | $80 | 2 | 1 | 2.0 | 0 | 0 | 1 |

[Source: Manazer — Activity table joined to Contributor table, filtered cost_contributor=true, occurred_at between 2026-02-01 and 2026-02-20]

---

## Section 2: Activity Type Breakdown

| Activity Type | Description |
|---|---|
| Committed | Git commits ingested from GitHub |
| ClickupTicketCommented | Comments on ClickUp tickets |
| ClickupTicketCreated | New ClickUp tickets created |
| ClickupTicketStatusChanged | Ticket status transitions |
| ClickupTicketCompleted | Tickets moved to done/complete status |
| GithubPullRequestOpened | PRs opened on GitHub |
| GithubPullRequestClosed | PRs closed/merged on GitHub |
| Meeting | Meeting records |

**PR Data Note:** 446 GithubPullRequestOpened/Closed activities exist in the period across all contributors, but ZERO map to cost_contributor=true contributors. PR authors not being matched to canonical contributor records.

[Source: Manazer — Activity.distinct.pluck(:type)]

---

## Section 3: Commits by Contributor (Code Output)

| Contributor | Cost $/hr | Commits | Active Days | Commits/Active Day |
|---|---:|---:|---:|---:|
| Isaac | $30 | 169 | 13 | 13.0 |
| Nikhil Galagali | $30 | 166 | 14 | 11.9 |
| Asarar Ahmed | $30 | 165 | 15 | 11.0 |
| Ganesh Hegde | $30 | 150 | 13 | 11.5 |
| Akhil | $50 | 134 | 10 | 13.4 |
| Paharlaya Basnet | $30 | 131 | 12 | 10.9 |
| Saurav Shah | $50 | 118 | 14 | 8.4 |
| Bharat | $30 | 103 | 14 | 7.4 |
| Rakesh Poddar | $30 | 99 | 15 | 6.6 |
| Megha Bc | $30 | 79 | 13 | 6.1 |
| Shantanu | $30 | 79 | 13 | 6.1 |
| Aniket | $50 | 62 | 13 | 4.8 |
| Manas | $30 | 54 | 12 | 4.5 |
| Prabhat Ranjan | $30 | 52 | 14 | 3.7 |
| Geetha | $80 | 46 | 14 | 3.3 |
| Rohit T | $30 | 36 | 10 | 3.6 |
| Saurabh | $30 | 32 | 10 | 3.2 |
| Paulomi | $120 | 29 | 8 | 3.6 |
| Exo | $30 | 38 | 7 | 5.4 |
| Jewel James | $80 | 25 | 16 | 1.6 |
| Karthik | $80 | 23 | 12 | 1.9 |
| Priyanshu Gaur | $50 | 15 | 15 | 1.0 |
| Harsh | $50 | 13 | 5 | 2.6 |
| Sidu | $80 | 7 | 13 | 0.5 |
| Das Animesh | $30 | 5 | 6 | 0.8 |
| Animesh | $30 | 4 | 2 | 2.0 |
| Suraj | $50 | 4 | 5 | 0.8 |
| Srini | $80 | 3 | 11 | 0.3 |
| Rishi | $80 | 3 | 3 | 1.0 |

[Source: Manazer — Activity.where(type: "Committed"), grouped by contributor]

---

## Section 4: Ticket Completions (Throughput)

| Contributor | Cost $/hr | Tickets Completed | Tickets Created | Completions/Active Day |
|---|---:|---:|---:|---:|
| Rakesh Poddar | $30 | 79 | 258 | 5.3 |
| Saurav Shah | $50 | 25 | 28 | 1.8 |
| Kaathyayani | $30 | 19 | 0 | 2.4 |
| Manas | $30 | 19 | 17 | 1.6 |
| Geetha | $80 | 17 | 26 | 1.2 |
| Akhil | $50 | 13 | 9 | 1.3 |
| Isaac | $30 | 12 | 31 | 0.9 |
| Priyanshu Gaur | $50 | 12 | 5 | 0.8 |
| Shantanu | $30 | 10 | 10 | 0.8 |
| Sidu | $80 | 7 | 7 | 0.5 |
| Megha Bc | $30 | 6 | 10 | 0.5 |
| Bharat | $30 | 6 | 5 | 0.4 |
| Prabhat Ranjan | $30 | 6 | 7 | 0.4 |
| Aniket | $50 | 6 | 8 | 0.5 |
| Karthik | $80 | 5 | 6 | 0.4 |
| Jewel James | $80 | 5 | 6 | 0.3 |
| Saurabh | $30 | 5 | 12 | 0.5 |

[Source: Manazer — Activity.where(type: "ClickupTicketCompleted"), grouped by contributor]

---

## Section 5: Project Allocation by Contributor

| Contributor | Primary Project | Activities | Secondary Project | Activities |
|---|---|---:|---|---:|
| Rakesh Poddar | starter-pack-fsc-wealth-mgmt-cloud | 648 | scientific-portfolio | 258 |
| Nikhil Galagali | starter-pack-fsc-wealth-mgmt-cloud | 200 | starter-pack-service-cloud | 155 |
| Ganesh Hegde | starter-pack-fsc-insurance-cloud | 338 | SIM Managed Services | 88 |
| Akhil | scientific-portfolio | 364 | manazer | 29 |
| Bharat | starter-pack-fsc-wealth-mgmt-cloud | 111 | SIM Managed Services | 82 |
| Saurav Shah | exo-sf-core-agent | 207 | TASC-Managed-Services | 90 |
| Asarar Ahmed | starter-pack-service-cloud | 188 | manazer | 114 |
| Paharlaya Basnet | starter-pack-service-cloud | 273 | service-cloud-optimization | 78 |
| Megha Bc | starter-pack-fsc-insurance-cloud | 151 | starter-pack-manufacturing-cloud | 136 |
| Isaac | NUS-fin.-reporting-POC | 231 | nus-contract-generation | 92 |
| Prabhat Ranjan | scientific-portfolio | 250 | — | — |
| Shantanu | exo-sf-core-agent | 123 | starter-packs | 56 |
| Jewel James | manazer | 109 | starter-pack-fsc-wealth-mgmt-cloud | 37 |
| Geetha | Pre-Sales-Delivery | 47 | starter-pack-healthcloud | 36 |
| Aniket | exo-code-server | 83 | exo-sf-core-agent | 55 |
| Manas | manazer | 188 | exo-help | 2 |
| Priyanshu Gaur | exo-agent-builder | 69 | Pre-Sales-Delivery | 51 |
| Sidu | New-Website | 27 | scientific-portfolio | 21 |
| Saurabh | exo-code-server | 84 | exo-help | 14 |
| Srini | manazer | 68 | exo-code-server | 9 |
| Anirudh | NUS-fin.-reporting-POC | 42 | harvester | 21 |
| Karthik | manazer | 31 | exo-help | 18 |
| Rohit T | manazer | 56 | — | — |

[Source: Manazer — Activities grouped by contributor + project, Feb 1-20]

---

## Section 6: Cost Rate Tiers

| Tier | Rate | Count | Contributors |
|---|---:|---:|---|
| Tier 1 | $120/hr | 1 | Paulomi |
| Tier 2 | $80/hr | 9 | Jewel James, Geetha, Sidu, Srini, Anirudh, Karthik, Rajnish, Rishi, Jeetal Shah |
| Tier 3 | $50/hr | 7 | Akhil, Saurav Shah, Aniket, Priyanshu Gaur, Harsh, Suraj, Sumanth |
| Tier 4 | $30/hr | 19 | Rakesh Poddar, Nikhil Galagali, Ganesh Hegde, Bharat, Asarar Ahmed, Paharlaya Basnet, Megha Bc, Isaac, Prabhat Ranjan, Shantanu, Manas, Saurabh, Rohit T, Das Animesh, Kaathyayani, Animesh, Piyush Sinha, Exo, It-admin |

[Source: Manazer — Contributor.cost_cents_per_hour]

---

## Section 7: Leave Records (Feb 1-20)

61 leave records in this period (including cancelled). Key leave patterns:

| Contributor | Leave Days (active only) | Types |
|---|---|---|
| Prashant | Feb 16-20 (5 days) | PTO |
| Allison | Feb 9-17 (7 days) | PTO |
| Sidu | Feb 17 + Feb 18-22 + Feb 20-21 | Mixed (5+ days) |
| Akhil | Feb 4, 16, 17, 18-20 | Mixed (6 days) |
| Asarar Ahmed | Feb 3, 4, 12, 17 | Mixed (4 days) |
| Saurav Shah | Feb 4, 11, 13 | Mixed (3 days) |
| Srini | Feb 12, 18, 20 | Mixed (3 days) |
| Isaac | Feb 3, 4 | Mixed (2 days) |
| Shantanu | Feb 2, 4 | Mixed (2 days) |
| Rajnish | Feb 2, 11 | Mixed (2 days) |
| Paharlaya Basnet | Feb 4, 10 | Mixed (2 days) |
| Megha Bc | Feb 9, 18 | Mixed (2 days) |
| Rishi | Feb 11, 13 | PTO (2 days) |
| Rohit T | Feb 4, 16 | Mixed (2 days) |
| Piyush Sinha | Feb 12-13 | PTO (2 days) |
| Jeetal Shah | Feb 12, 20 | Mixed (2 days) |
| Suraj | Feb 17, 18 | Sick (2 days) |
| Geetha | Feb 10 | PTO (1 day) |
| Ganesh Hegde | Feb 16 | PTO (1 day) |
| Priyanshu Gaur | Feb 9 | Sick (1 day) |
| Aniket | Feb 12 | PTO (1 day) |
| Nikhil | Feb 9 | PTO (1 day) |
| Karthik | Feb 9 | Sick (1 day) |
| Rakesh Poddar | Feb 9 | Sick (1 day) |
| Prabhat Ranjan | Feb 4 | Sick (1 day) |
| Saurabh | Feb 4 | PTO (1 day) |
| Animesh | Feb 4 | PTO (1 day) |
| Sumanth | Feb 20 | PTO (1 day) |

[Source: Manazer — Leave model, status=active, Feb 1-20]

---

## Data Gaps

1. **No FTE vs Contractor field.** Contributor model columns: id, name, primary_email, cost_per_hour, cost_cents_per_hour, cost_contributor. NO employment_type or contractor_flag exists. FTE vs contractor distinction cannot be determined from Manazer data. [Source: Contributor.column_names]

2. **PR data not linked to canonical contributors.** 446 PR activities exist but 0 map to cost_contributor=true records. GitHub noreply emails not matched to contributor roster. [Source: Activity.where(type: GithubPullRequestOpened/Closed)]

3. **No hours-worked metric.** Manazer tracks activity counts, not hours. No timesheet or time-logged field on Activity model. ClickUp time_estimate/time_spent exist in ticket metadata but not aggregated per contributor. [Source: Activity.column_names]

4. **Activity counts ≠ productivity.** A ClickUp comment and a complex code commit both count as 1 activity. Activity mix varies significantly by role. [Source: Activity type distribution]

5. **Project budget data sparse.** Only 5 of 34 active projects have budget_cents configured. [Source: Project model]

6. **Cost rates appear to be tier-based.** $30/$50/$80/$120 tiers with no variation within tiers. Unclear if these are compensation or billing categories. [Source: Contributor.cost_cents_per_hour]

## Data Conflicts

1. **Activity on leave days.** Multiple contributors show Manazer activity on dates they have active leave records (e.g., Akhil: 10 active days but 6 leave days in a 15-day period).

2. **Weekend activity.** Some contributors (Asarar Ahmed, Sidu, Rishi, others) show activity on Feb 1 (Sunday), Feb 7, Feb 8, Feb 14, Feb 15 (weekends).

---

```
FACT-FINDING COMPLETE
---------------------
Data points extracted: ~252+ (36 contributors x 7 metrics)
Data gaps identified:  6
Data conflicts found:  2

Next step: Run verification to validate all data points
before proceeding to analysis.
```
