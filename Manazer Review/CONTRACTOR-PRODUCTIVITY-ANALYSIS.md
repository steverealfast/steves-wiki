# Contractor Productivity Analysis — Feb 1–20, 2026

**Persona:** Jon Gray — CFO. Revenue Architect. Project Economist.
**Scope:** Manazer | Contractor cost efficiency, revenue utilization, tagging discipline | CEO + Delivery Head
**Data Source:** Verified Fact-Finding Report (98.8% confidence) + MCP Refresh (Feb 20, full project breakdowns)
**Period:** Feb 1–20, 2026 (15 business days)
**Generated:** Feb 20, 2026

---

## 1. Executive Summary

| Metric | Value |
|--------|-------|
| Active Contractors | 9 |
| Cost Rate (all) | $30/hr (internal cost) |
| Total Estimated Period Spend | $27,360 |
| Revenue-Generating (Client) | $8,045 (29.4%) |
| Cost of Sales (Presales) | $14,619 (53.4%) |
| Internal (Absorbed) | $4,696 (17.2%) |

**The bottom line:** For every dollar spent on contractors in this period, ~29 cents produced client revenue, ~53 cents went to presales pipeline investment, and ~17 cents was absorbed internal cost. Project tagging discipline is clean — every activity is attributed to a project. The real question is whether 53% presales investment will convert, and whether contractors should be doing internal tooling work.

---

## 2. Methodology & Definitions

**How this analysis works:** Manazer tracks discrete activities (commits, ticket actions, comments) per contributor per project. It does not track hours. To estimate cost, we use the proxy of Active Days — the number of distinct calendar dates on which a contributor recorded at least one activity.

| Term | Definition | Calculation |
|------|-----------|-------------|
| **Estimated Period Cost** | What we paid this contractor for the period | Active Days x 8 hrs x $30/hr |
| **Revenue Utilization Rate** | % of a contractor's activities mapped to client (revenue-generating) projects | Client Activities / Total Activities |
| **Effective Hourly Rate** | What each hour of client work actually costs after dilution from non-client work | $30 / Revenue Utilization Rate |
| **Cost/Commit** | Cost per code commit — a code output efficiency proxy | Period Cost / Commits |
| **Cost/Ticket** | Cost per completed ticket — a throughput efficiency proxy | Period Cost / Tickets Completed |
| **Cost/Revenue Activity** | Cost per client-attributed activity — revenue efficiency proxy | Period Cost / Client Activities |

**Cost Bucket Definitions:**

| Bucket | What It Means | Projects |
|--------|--------------|----------|
| **Client (Revenue)** | Work that generates income — the only bucket that pays for itself | SIM Managed Services, SIM, TASC-Managed-Services, NUS-fin.-reporting-POC, nus-contract-generation, scientific-portfolio, Hypernative, Boardroom |
| **Presales (Cost of Sales)** | Investment in future revenue — justified but must convert | All starter-pack-\*, starter-packs, Pre-Sales-Delivery, service-cloud-starter-pack-optimization |
| **Internal (Absorbed)** | Operational cost — acceptable if intentional | manazer, exo-sf-core-agent, exo-code-server, exo-agent-builder, exo-help, harvester, New-Website, content-branding |

---

## 3. Contractor Roster — Ranked by Revenue Contribution

**What this table shows:** All 9 contractors ranked by the proportion of their work that directly generates client revenue. Higher revenue utilization = the contractor is paying for themselves. Zero = we are paying them but getting no client output.

| Rank | Contractor | Est. Period Cost | Total Activities | Active Days | Revenue Util. | Effective $/hr |
|---:|---|---:|---:|---:|---:|---:|
| 1 | Prabhat Ranjan | $3,360 | 250 | 14 | 100.0% | $30.00 |
| 2 | Das Animesh | $1,680 | 62 | 7 | 41.9% | $71.60 |
| 3 | Rakesh Poddar | $3,600 | 934 | 15 | 27.6% | $108.70 |
| 4 | Bharat | $3,360 | 367 | 14 | 26.7% | $112.36 |
| 5 | Ganesh Hegde | $3,120 | 454 | 13 | 25.3% | $118.58 |
| 6 | Shantanu | $3,120 | 246 | 13 | 20.3% | $147.78 |
| 7 | Nikhil Galagali | $3,360 | 475 | 14 | 19.8% | $151.52 |
| 8 | Paharlaya Basnet | $2,880 | 351 | 12 | 0.0% | N/A |
| 9 | Manas | $2,880 | 190 | 12 | 0.0% | N/A |
| | **TOTAL** | **$27,360** | **3,329** | | | |

---

## 4. Cost Allocation Summary

**What this table shows:** How each contractor's estimated cost breaks down across cost buckets. Calculated by mapping each contractor's project activities to the bucket classification, then prorating their period cost by activity proportion. Full project breakdowns from MCP refresh — all activities are project-attributed (zero nil-project records).

| Contractor | Period Cost | Client ($) | Presales ($) | Internal ($) |
|---|---:|---:|---:|---:|
| Prabhat Ranjan | $3,360 | $3,360 (100%) | $0 | $0 |
| Rakesh Poddar | $3,600 | $994 (28%) | $2,606 (72%) | $0 |
| Bharat | $3,360 | $897 (27%) | $2,445 (73%) | $18 (<1%) |
| Ganesh Hegde | $3,120 | $790 (25%) | $2,330 (75%) | $0 |
| Das Animesh | $1,680 | $705 (42%) | $921 (55%) | $54 (3%) |
| Shantanu | $3,120 | $634 (20%) | $926 (30%) | $1,560 (50%) |
| Nikhil Galagali | $3,360 | $665 (20%) | $2,511 (75%) | $184 (5%) |
| Paharlaya Basnet | $2,880 | $0 | $2,880 (100%) | $0 |
| Manas | $2,880 | $0 | $0 | $2,880 (100%) |
| **TOTAL** | **$27,360** | **$8,045 (29%)** | **$14,619 (53%)** | **$4,696 (17%)** |

---

## 5. Revenue Efficiency Metrics

**What this table shows:** Three cost-per-output metrics for all contractors. Lower = more efficient. Cost/Commit measures code output efficiency. Cost/Ticket measures throughput. Cost/Revenue Activity is the broadest measure of client work efficiency. All metrics use TOTAL period cost because the contractor was paid for the entire period regardless of what they worked on.

| Contractor | Commits | Tickets Done | Client Activities | Cost/Commit | Cost/Ticket | Cost/Rev. Activity |
|---|---:|---:|---:|---:|---:|---:|
| Prabhat Ranjan | 52 | 6 | 250 | $64.62 | $560.00 | $13.44 |
| Rakesh Poddar | 99 | 79 | 258 | $36.36 | $45.57 | $13.95 |
| Bharat | 103 | 6 | 98 | $32.62 | $560.00 | $34.29 |
| Ganesh Hegde | 150 | 2 | 115 | $20.80 | $1,560.00 | $27.13 |
| Shantanu | 79 | 10 | 50 | $39.49 | $312.00 | $62.40 |
| Nikhil Galagali | 166 | 2 | 94 | $20.24 | $1,680.00 | $35.74 |
| Paharlaya Basnet | 131 | 2 | 0 | $21.98 | $1,440.00 | N/A |
| Manas | 54 | 19 | 0 | $53.33 | $151.58 | N/A |
| Das Animesh | 10 | 1 | 26 | $168.00 | $1,680.00 | $64.62 |

---

## 5A. Activity Quality Audit — Output vs Noise

**Why this matters:** The analysis above treats all Manazer activities equally — a code commit, a completed ticket, and a ClickUp comment all count as "1 activity." When we prorate cost across projects using activity counts, a contractor who comments on 50 client tickets looks the same as one who ships 50 commits. They are not the same. This section strips the noise to show what contractors are actually *producing* versus what they're merely *participating in*.

**Definitions:**
- **Real Output** = Code commits + Tickets completed. These are verifiable deliverables.
- **ClickUp Noise** = Ticket comments + Status changes + Ticket creations. These may indicate engagement but do not prove work was done. A comment saying "ok will look into it" and a comment containing a full technical breakdown both count as 1 activity.

### Activity Composition by Contractor

| Contractor | Total Activities | Commits | Tickets Done | Real Output | Real % | Comments | Status Chg | Created | Noise | Noise % |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Prabhat Ranjan | 255 | 53 | 6 | 59 | 23% | 148 | 41 | 7 | 196 | 77% |
| Rakesh Poddar | 952 | 99 | 81 | 180 | 19% | 299 | 214 | 259 | 772 | 81% |
| Bharat | 395 | 113 | 7 | 120 | 30% | 183 | 87 | 5 | 275 | 70% |
| Ganesh Hegde | 458 | 152 | 2 | 154 | 34% | 225 | 78 | 1 | 304 | 66% |
| Nikhil Galagali | 493 | 173 | 2 | 175 | 36% | 265 | 49 | 4 | 318 | 65% |
| Paharlaya Basnet | 367 | 131 | 2 | 133 | 36% | 203 | 28 | 3 | 234 | 64% |
| Shantanu | 246 | 79 | 10 | 89 | 36% | 110 | 37 | 10 | 157 | 64% |
| Manas | 190 | 54 | 19 | 73 | 38% | 42 | 58 | 17 | 117 | 62% |
| Das Animesh | 62 | 10 | 1 | 11 | 18% | 34 | 13 | 4 | 51 | 82% |
| **TOTAL** | **3,418** | **864** | **130** | **994** | **29%** | **1,509** | **607** | **310** | **2,424** | **71%** |

**71% of all contractor activity is ClickUp noise.** Only 29% — 994 out of 3,418 activities — represents verifiable output (code committed or tickets completed).

### Revenue Utilization: All-Activity vs Real-Output-Only

**What changes when you strip the noise:** Revenue utilization is recalculated using only commits and ticket completions (both the contractor's and the project's).

| Contractor | Rev Util (Current) | Rev Util (Real Only) | Direction | Client Real Output | Client Noise |
|---|---:|---:|---|---:|---:|
| Prabhat Ranjan | 100.0% | 100.0% | — | 59 | 196 |
| Rakesh Poddar | 28.3% | 43.3% | +15pp | 78 | 191 |
| Ganesh Hegde | 25.5% | 37.0% | +12pp | 57 | 60 |
| Das Animesh | 41.9% | 81.8% | +40pp | 9 | 17 |
| Bharat | 24.8% | 24.2% | ~same | 29 | 69 |
| Shantanu | 20.3% | 13.5% | -7pp | 12 | 38 |
| Nikhil Galagali | 19.1% | 14.9% | -4pp | 26 | 68 |
| Paharlaya Basnet | 0.0% | 0.0% | — | 0 | 0 |
| Manas | 0.0% | 0.0% | — | 0 | 0 |

**Two patterns emerge:**

1. **Ganesh and Rakesh look *better* on real output** — their client work is code-heavy, not comment-heavy. When you strip ClickUp noise, their revenue utilization goes up because they're shipping code to client projects, not just commenting on tickets.

2. **Shantanu and Nikhil look *worse*** — their "client activities" are disproportionately ClickUp comments, not code. Shantanu drops from 20.3% to 13.5%; Nikhil from 19.1% to 14.9%. Their apparent client engagement is inflated by ticket noise.

### The Comment Problem

The single largest activity category across all contractors is **ClickUp comments: 1,509 (44% of all activity)**. For context:

- Rakesh: 299 comments, 99 commits (3:1 comment-to-commit ratio)
- Nikhil: 265 comments, 173 commits (1.5:1)
- Ganesh: 225 comments, 152 commits (1.5:1)
- Paharlaya: 203 comments, 131 commits (1.6:1)
- Prabhat: 148 comments, 53 commits (2.8:1)

Some comments are substantive (technical discussions, design decisions). Some are perfunctory ("done", "ok", "will check"). **Manazer cannot distinguish between the two.** The current analysis treats them identically for cost allocation.

### What This Means for Cost Allocation

The cost allocation in Section 4 prorates each contractor's period cost by activity distribution across projects. Because 71% of activities are ClickUp noise, the cost allocation is driven primarily by *where contractors comment on tickets*, not *where they ship code*.

For a contractor like Shantanu: his $634 "Client Revenue" allocation is based on 50 client activities — but only 12 of those are real output. The other 38 are ClickUp comments on client tickets. Whether those comments constitute meaningful client work or not is a judgment call that the data cannot make.

---

## 6. Individual Contractor Deep Dives

### 6.1 Prabhat Ranjan

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 250 |
| Active Days | 14 of 15 |
| Commits | 52 |
| Tickets Completed | 6 |
| Tickets Created | 7 |
| Est. Period Cost | $3,360 |

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| scientific-portfolio | Client | 250 | 100% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $3,360 | 100% |
| Presales | $0 | 0% |
| Internal | $0 | 0% |

**Assessment:** 100% client-deployed. Revenue utilization is ideal. Effective hourly rate = nominal rate ($30/hr). Moderate commit volume (3.7/day) but fully focused on revenue work. Cost/commit at $64.62 reflects lower code volume — warrants checking whether the work is ticket/configuration-heavy rather than code-heavy. The model contractor from a cost allocation standpoint.

---

### 6.2 Rakesh Poddar

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 934 |
| Active Days | 15 of 15 |
| Commits | 99 |
| Tickets Completed | 79 |
| Tickets Created | 258 |
| Est. Period Cost | $3,600 |

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| starter-pack-fsc-wealth-management-cloud | Presales | 648 | 69% |
| scientific-portfolio | Client | 258 | 28% |
| starter-pack-fsc-insurance-cloud | Presales | 13 | 1% |
| starter-pack-fsc-wealth-mgmt-cloud-base-org | Presales | 7 | 1% |
| starter-pack-service-cloud | Presales | 5 | 1% |
| Pre-Sales-Delivery | Presales | 3 | <1% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $994 | 28% |
| Presales | $2,606 | 72% |
| Internal | $0 | 0% |

**Assessment:** Highest total output of any contractor (934 activities). Exceptional ticket throughput (79 completed, 5.3/day). However, 72% of activity is presales — not yet generating revenue. The 258 tickets created on a single starter-pack project warrants investigation into whether these are granular subtasks or genuine work items. 28% client revenue utilization means effective hourly rate is $108.70. Productive, but the presales-to-revenue ratio needs to shift.

---

### 6.3 Bharat

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 367 |
| Active Days | 14 of 15 |
| Commits | 103 |
| Tickets Completed | 6 |
| Tickets Created | 5 |
| Est. Period Cost | $3,360 |

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| starter-pack-fsc-wealth-management-cloud | Presales | 111 | 30% |
| SIM Managed Services | Client | 82 | 22% |
| Pre-Sales-Delivery | Presales | 74 | 20% |
| service-cloud-starter-pack-optimization | Presales | 29 | 8% |
| starter-pack-service-cloud | Presales | 28 | 8% |
| starter-pack-a4x-sales | Presales | 25 | 7% |
| SIM | Client | 16 | 4% |
| exo-agent-builder | Internal | 2 | <1% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $897 | 27% |
| Presales | $2,445 | 73% |
| Internal | $18 | <1% |

**Assessment:** The most diversified contractor — spread across 8 projects. Good commit velocity (7.4/day) but only 6 tickets completed in 14 active days. 27% revenue utilization is 3rd best. The spread across 5 different presales projects is notable — either a versatile generalist or spreading too thin. SIM client work ($897) is meaningful revenue contribution.

---

### 6.4 Ganesh Hegde

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 454 |
| Active Days | 13 of 15 |
| Commits | 150 |
| Tickets Completed | 2 |
| Tickets Created | 1 |
| Est. Period Cost | $3,120 |

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| starter-pack-fsc-insurance-cloud | Presales | 338 | 74% |
| SIM Managed Services | Client | 88 | 19% |
| SIM | Client | 27 | 6% |
| starter-pack-service-cloud | Presales | 1 | <1% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $790 | 25% |
| Presales | $2,330 | 75% |
| Internal | $0 | 0% |

**Assessment:** Strong commit output (11.5/day — 3rd highest). But only 2 tickets completed in 13 days — the worst ticket throughput of any active contractor. This suggests either very large-scope tickets or poor ticket workflow discipline. 25% client work (SIM Managed Services + SIM = 115 activities) is solid. Effective hourly rate of $118.58 for client work. Clean project allocation with no internal diversions.

---

### 6.5 Shantanu

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 246 |
| Active Days | 13 of 15 |
| Commits | 79 |
| Tickets Completed | 10 |
| Tickets Created | 10 |
| Est. Period Cost | $3,120 |

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| exo-sf-core-agent | Internal | 123 | 50% |
| starter-packs | Presales | 56 | 23% |
| Hypernative | Client | 32 | 13% |
| service-cloud-starter-pack-optimization | Presales | 17 | 7% |
| SIM Managed Services | Client | 17 | 7% |
| SIM | Client | 1 | <1% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $634 | 20% |
| Presales | $926 | 30% |
| Internal | $1,560 | 50% |

**Assessment:** Half his time is on internal tooling (exo-sf-core-agent). For a contractor at $30/hr, $1,560 of internal cost is a management decision question: is a contractor the right resource for internal platform work? The 20% client revenue (Hypernative + SIM) shows he can do revenue-generating work. If the internal allocation is intentional, acceptable. If not, redirecting that 50% to client work would double his revenue contribution.

---

### 6.6 Nikhil Galagali

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 475 |
| Active Days | 14 of 15 |
| Commits | 166 |
| Tickets Completed | 2 |
| Tickets Created | 4 |
| Est. Period Cost | $3,360 |

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| starter-pack-fsc-wealth-management-cloud | Presales | 200 | 42% |
| starter-pack-service-cloud | Presales | 155 | 33% |
| TASC-Managed-Services | Client | 94 | 20% |
| exo-sf-core-agent | Internal | 26 | 5% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $665 | 20% |
| Presales | $2,511 | 75% |
| Internal | $184 | 5% |

**Assessment:** 2nd highest commit count (166, 11.9/day) but only 2 tickets completed — same pattern as Ganesh. 20% revenue from TASC-Managed-Services ($665). 75% presales across two starter-pack projects. Effective hourly rate for client work = $151.52. High code output but the ticket completion rate raises questions about scope management or ticket discipline.

---

### 6.7 Paharlaya Basnet

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 351 |
| Active Days | 12 of 15 |
| Commits | 131 |
| Tickets Completed | 2 |
| Tickets Created | 2 |
| Est. Period Cost | $2,880 |

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| starter-pack-service-cloud | Presales | 273 | 78% |
| service-cloud-starter-pack-optimization | Presales | 78 | 22% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $0 | 0% |
| Presales | $2,880 | 100% |
| Internal | $0 | 0% |

**Assessment:** 100% presales with clean allocation — zero client revenue, zero internal. Good commit velocity (10.9/day). Only 2 tickets completed. This contractor is a pure presales cost of $2,880 — justified only if the service-cloud pipeline converts to revenue. If that pipeline stalls, this is $2,880/period ($74,880 annualized) generating nothing. Tagging discipline is excellent.

---

### 6.8 Manas

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 190 |
| Active Days | 12 of 15 |
| Commits | 54 |
| Tickets Completed | 19 |
| Tickets Created | 17 |
| Est. Period Cost | $2,880 |

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| manazer | Internal | 188 | 99% |
| exo-help | Internal | 2 | 1% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $0 | 0% |
| Presales | $0 | 0% |
| Internal | $2,880 | 100% |

**Assessment:** 100% internal (manazer platform). Zero client revenue. Zero presales. Best ticket throughput ratio among non-Rakesh contractors (19 completed, 1.6/day). But this is a contractor spending 100% on internal tooling — $2,880/period ($74,880 annualized) of absorbed operational cost. Same question as Shantanu: is a contractor the right resource for internal platform work? If manazer development is a temporary project, this makes sense. If it's ongoing, this should be an FTE role.

---

### 6.9 Das Animesh

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 62 |
| Joined | Feb 9, 2026 |
| Available Business Days | 8 (Feb 9–20) |
| Active Days | 7 of 8 |
| Commits | 10 |
| Tickets Completed | 1 |
| Tickets Created | 4 |
| Est. Period Cost | $1,680 |

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| Pre-Sales-Delivery | Presales | 33 | 53% |
| SIM | Client | 11 | 18% |
| scientific-portfolio | Client | 9 | 15% |
| SIM Managed Services | Client | 4 | 6% |
| manazer | Internal | 2 | 3% |
| TASC-Managed-Services | Client | 2 | 3% |
| starter-pack-healthcloud | Presales | 1 | 2% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $705 | 42% |
| Presales | $921 | 55% |
| Internal | $54 | 3% |

**Assessment:** Joined Feb 9 and ramped quickly — active 7 of 8 available business days with 62 activities. 42% revenue utilization is 2nd best in the contractor roster after Prabhat. Diversified across 7 projects including meaningful client work on SIM ($11 activities) and scientific-portfolio (9 activities). 55% presales allocation is on Pre-Sales-Delivery. Low commit count (10) and only 1 ticket completed suggest early-stage work or onboarding ramp-up. At $71.60 effective hourly rate for client work, this is the 2nd most cost-efficient contractor. Strong start for a new joiner — monitor commit velocity and ticket completion as ramp-up continues.

---

## 7. Action Items

### For Geetha (Delivery Head)

**A. Activity Quality Audit — What Are Contractors Actually Doing? (URGENT)**

71% of all contractor activity in this period is ClickUp ticket noise — comments, status changes, and ticket creations. Only 29% is verifiable output (code commits + completed tickets). The entire cost allocation model in this analysis depends on activity distribution, which means **cost is being allocated based on where people comment, not where they deliver.**

Specific concerns:

| Contractor | Total Acts | Real Output | Noise % | Issue |
|---|---:|---:|---:|---|
| Rakesh Poddar | 952 | 180 | 81% | 259 tickets *created* but only 81 *completed* — is he generating work or finishing it? |
| Prabhat Ranjan | 255 | 59 | 77% | 148 comments vs 53 commits — what are the comments? Substantive or perfunctory? |
| Das Animesh | 62 | 11 | 82% | New joiner (Feb 9). 34 comments, 10 commits. Is he ramping up or just tagged in threads? |
| Nikhil Galagali | 493 | 175 | 65% | 265 comments, 173 commits. 68 client "activities" are just comments — real client output is only 26. |
| Shantanu | 246 | 89 | 64% | Drops from 20% to 13.5% revenue util when noise is stripped. His "client work" is mostly comments. |

**Action Required:**

1. **Spot-check ClickUp comments** for the top 3 comment-heavy contractors (Rakesh: 299, Nikhil: 265, Ganesh: 225). Are these substantive technical discussions or one-line acknowledgments? Sample 10 comments per contractor.
2. **Audit Rakesh's 259 ticket creations.** He created 259 tickets but completed 81. What happened to the other 178? Are they still open, reassigned, or abandoned? On a single starter-pack project, this volume of ticket creation warrants scrutiny.
3. **Validate Das Animesh's ramp.** 10 commits in 7 active days is legitimate output for a new joiner. But 34 comments and 13 status changes suggest he may be tagged in conversations rather than leading work. Confirm he has clear ownership of deliverables.
4. **Establish a baseline**: What is the expected commit-to-comment ratio for a productive contractor? Ganesh (1.5:1) and Nikhil (1.5:1) look reasonable. Prabhat (2.8:1) and Rakesh (3:1) warrant investigation.

**Why this is urgent:** Without this audit, every percentage in this analysis — revenue utilization, cost allocation, effective hourly rates — is built on a foundation that treats ticket comments as equivalent to shipped code. The numbers look clean but the underlying signal may be noise.

**B. Ticket Completion Discipline**

Four contractors show high commit counts but extremely low ticket completion:

| Contractor | Commits | Tickets Completed | Ratio |
|---|---:|---:|---|
| Nikhil Galagali | 166 | 2 | 83:1 |
| Ganesh Hegde | 150 | 2 | 75:1 |
| Paharlaya Basnet | 131 | 2 | 65:1 |
| Bharat | 103 | 6 | 17:1 |

Compare to Rakesh (99 commits, 79 tickets = 1.3:1) and Manas (54 commits, 19 tickets = 2.8:1). The gap suggests either: tickets are not being broken down properly, tickets are not being moved to "complete" status, or there's no ticket workflow discipline.

**Action:** Audit ClickUp workflow for these contractors. Ensure tickets are created, tracked, and completed — not just code pushed.

**C. Internal Contractor Allocation Review**

Two contractors are spending significant time on internal tooling:

| Contractor | Internal $ | Internal % | Internal Project |
|---|---:|---:|---|
| Manas | $2,880 | 100% | manazer |
| Shantanu | $1,560 | 50% | exo-sf-core-agent |
| **Total** | **$4,440** | | |

$4,440/period ($115K annualized) of contractor spend on internal projects. **Decision needed:** Is contractor staffing the right model for ongoing internal platform work, or should these be FTE roles?

### For Sidu (Tech Lead)

**D. PR Author Mapping**

446 GitHub PR activities exist in the period but 0 map to cost_contributor=true records. GitHub noreply emails are not being matched to the contributor roster.

**Action:** Map GitHub identities to Manazer contributors so PR data can be included in productivity analysis.

**E. Project Budget Configuration**

Only 4 of 29 active projects have budget_cents configured in Manazer. Without budgets, we cannot calculate budget variance or overrun metrics.

**Action:** Configure budgets for all active client and presales projects.

---

## 8. Data Caveats

1. **Activity does not equal Hours.** Manazer counts discrete events (commits, ticket actions). A complex 4-hour code change and a 30-second ticket comment both count as 1 activity. Cost estimation uses Active Days x 8 hrs as a proxy.

2. **PR Data Excluded.** 446 PR activities cannot be attributed to contributors due to GitHub email mismatch. This underrepresents code review and merge activity for all contributors.

3. **Cost Rates Are Internal.** The $30/hr rate is what the company pays, not what clients are billed. Revenue margin analysis requires billing rates (not available in Manazer).

4. **Project Tagging Is Clean.** Full MCP refresh confirmed zero nil-project activities across all contractors. Every activity is attributed to a project. Earlier analysis (pre-MCP refresh) showed apparent "unaccounted" activities — this was a data visibility limitation (top-2 project view), not a tagging discipline failure.

---

*Analysis prepared under the Jon Gray CFO Persona. All data points sourced from the Verified Fact-Finding Report (Feb 20, 2026) with full project breakdowns from MCP refresh. Corrected Feb 20: Das Animesh (das.animesh@realfast.ai) is the SF contractor; Animesh (animesh@realfast.ai) is an FTE — original analysis had these identities swapped.*
