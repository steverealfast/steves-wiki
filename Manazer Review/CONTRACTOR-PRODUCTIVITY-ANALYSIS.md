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
| Total Estimated Period Spend | $27,600 |
| Revenue-Generating (Client) | $7,340 (26.6%) |
| Cost of Sales (Presales) | $13,698 (49.6%) |
| Internal (Absorbed) | $4,642 (16.8%) |
| Zero Output (Animesh) | $1,920 (7.0%) |

**The bottom line:** For every dollar spent on contractors in this period, 27 cents produced client revenue, 50 cents went to presales pipeline investment, 17 cents was absorbed internal cost, and 7 cents produced zero output. Project tagging discipline is clean — every activity is attributed to a project. The real question is whether 50% presales investment will convert, and whether contractors should be doing internal tooling work.

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
| **Zero Output** | Contractor on payroll with no recorded activities | Animesh (contractor) — data mapping issue + no output |

**Methodology Exception — Animesh (Contractor):** Joined Feb 9. Manazer has a contributor mapping error where his record contains activities belonging to another person (Das Animesh, FTE). His cost is calculated using employment days (8 business days) rather than Active Days, since his Manazer data is unreliable. All 6 activities under the "Animesh" record are misattributed.

---

## 3. Contractor Roster — Ranked by Revenue Contribution

**What this table shows:** All 9 contractors ranked by the proportion of their work that directly generates client revenue. Higher revenue utilization = the contractor is paying for themselves. Zero = we are paying them but getting no client output.

| Rank | Contractor | Est. Period Cost | Total Activities | Active Days | Revenue Util. | Effective $/hr |
|---:|---|---:|---:|---:|---:|---:|
| 1 | Prabhat Ranjan | $3,360 | 250 | 14 | 100.0% | $30.00 |
| 2 | Rakesh Poddar | $3,600 | 934 | 15 | 27.6% | $108.70 |
| 3 | Bharat | $3,360 | 367 | 14 | 26.7% | $112.36 |
| 4 | Ganesh Hegde | $3,120 | 454 | 13 | 25.3% | $118.58 |
| 5 | Shantanu | $3,120 | 246 | 13 | 20.3% | $147.78 |
| 6 | Nikhil Galagali | $3,360 | 475 | 14 | 19.8% | $151.52 |
| 7 | Paharlaya Basnet | $2,880 | 351 | 12 | 0.0% | N/A |
| 8 | Manas | $2,880 | 190 | 12 | 0.0% | N/A |
| 9 | Animesh | $1,920 | 0* | 8** | 0.0% | N/A |
| | **TOTAL** | **$27,600** | **3,267** | | | |

\* Manazer data misattributed — see Data Caveats
\** Employment days since joining Feb 9, not Manazer Active Days

---

## 4. Cost Allocation Summary

**What this table shows:** How each contractor's estimated cost breaks down across cost buckets. Calculated by mapping each contractor's project activities to the bucket classification, then prorating their period cost by activity proportion. Full project breakdowns from MCP refresh — all activities are project-attributed (zero nil-project records).

| Contractor | Period Cost | Client ($) | Presales ($) | Internal ($) | Zero Output ($) |
|---|---:|---:|---:|---:|---:|
| Prabhat Ranjan | $3,360 | $3,360 (100%) | $0 | $0 | |
| Rakesh Poddar | $3,600 | $994 (28%) | $2,606 (72%) | $0 | |
| Bharat | $3,360 | $897 (27%) | $2,445 (73%) | $18 (<1%) | |
| Ganesh Hegde | $3,120 | $790 (25%) | $2,330 (75%) | $0 | |
| Shantanu | $3,120 | $634 (20%) | $926 (30%) | $1,560 (50%) | |
| Nikhil Galagali | $3,360 | $665 (20%) | $2,511 (75%) | $184 (5%) | |
| Paharlaya Basnet | $2,880 | $0 | $2,880 (100%) | $0 | |
| Manas | $2,880 | $0 | $0 | $2,880 (100%) | |
| Animesh | $1,920 | $0 | $0 | $0 | $1,920 (100%) |
| **TOTAL** | **$27,600** | **$7,340 (27%)** | **$13,698 (50%)** | **$4,642 (17%)** | **$1,920 (7%)** |

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
| Animesh | 0 | 0 | 0 | N/A | N/A | N/A |

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

### 6.9 Animesh (Contractor)

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 0 (correctly attributed)* |
| Joined | Feb 9, 2026 |
| Available Business Days | 8 (Feb 9–20) |
| Commits | 0 |
| Tickets Completed | 0 |
| Tickets Created | 0 |
| Est. Period Cost | $1,920 |

\* The "Animesh" record in Manazer (ID: 6f38b3c0) contains 6 activities, but these are misattributed: 4 activities on Feb 2 (before contractor joined) and 2 Boardroom activities belonging to Das Animesh (FTE). See Action Items.

**Project Allocation**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| None | — | 0 | — |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $0 | 0% |
| Presales | $0 | 0% |
| Internal | $0 | 0% |
| **Zero Output** | **$1,920** | **100%** |

**Assessment:** Joined Feb 9 — 8 business days with zero recorded output. $1,920 spent with nothing to show. This is the most expensive per-output contractor in the roster because there is no output. Whether this is an onboarding delay, a data capture issue (work happening but not tracked), or genuine inactivity — management needs to investigate immediately. Additionally, his Manazer contributor record has a mapping error mixing his data with an FTE, which means even if he starts producing, his work may not be correctly attributed.

---

## 7. Action Items

### For Geetha (Delivery Head)

**A. Animesh Contributor Mapping Fix**

The "Animesh" Manazer contributor record (ID: 6f38b3c0) contains misattributed activities:
- Feb 2 activities (manazer: 4) pre-date the contractor's Feb 9 start — these belong to the FTE
- Feb 12 activities (Boardroom: 2) belong to Das Animesh (FTE), not the contractor

**Action:** Separate the two Animesh contributors in Manazer. Reassign misattributed activities to the correct contributor. Verify the contractor's Manazer profile is correctly configured to capture his actual work going forward.

**B. Animesh (Contractor) Output Review**

Zero activities in 8 business days since joining. Determine:
- Is this an onboarding issue? (Training period, access setup)
- Is work happening but not being captured in Manazer? (Missing integrations)
- Is this genuine inactivity? (Performance issue)

**Action:** Investigate immediately. At $30/hr, every week of zero output is $1,200.

**C. Ticket Completion Discipline**

Four contractors show high commit counts but extremely low ticket completion:

| Contractor | Commits | Tickets Completed | Ratio |
|---|---:|---:|---|
| Nikhil Galagali | 166 | 2 | 83:1 |
| Ganesh Hegde | 150 | 2 | 75:1 |
| Paharlaya Basnet | 131 | 2 | 65:1 |
| Bharat | 103 | 6 | 17:1 |

Compare to Rakesh (99 commits, 79 tickets = 1.3:1) and Manas (54 commits, 19 tickets = 2.8:1). The gap suggests either: tickets are not being broken down properly, tickets are not being moved to "complete" status, or there's no ticket workflow discipline.

**Action:** Audit ClickUp workflow for these contractors. Ensure tickets are created, tracked, and completed — not just code pushed.

**D. Internal Contractor Allocation Review**

Two contractors are spending significant time on internal tooling:

| Contractor | Internal $ | Internal % | Internal Project |
|---|---:|---:|---|
| Manas | $2,880 | 100% | manazer |
| Shantanu | $1,560 | 50% | exo-sf-core-agent |
| **Total** | **$4,440** | | |

$4,440/period ($115K annualized) of contractor spend on internal projects. **Decision needed:** Is contractor staffing the right model for ongoing internal platform work, or should these be FTE roles?

### For Sidu (Tech Lead)

**E. PR Author Mapping**

446 GitHub PR activities exist in the period but 0 map to cost_contributor=true records. GitHub noreply emails are not being matched to the contributor roster.

**Action:** Map GitHub identities to Manazer contributors so PR data can be included in productivity analysis.

**F. Project Budget Configuration**

Only 4 of 29 active projects have budget_cents configured in Manazer. Without budgets, we cannot calculate budget variance or overrun metrics.

**Action:** Configure budgets for all active client and presales projects.

---

## 8. Data Caveats

1. **Activity does not equal Hours.** Manazer counts discrete events (commits, ticket actions). A complex 4-hour code change and a 30-second ticket comment both count as 1 activity. Cost estimation uses Active Days x 8 hrs as a proxy.

2. **PR Data Excluded.** 446 PR activities cannot be attributed to contributors due to GitHub email mismatch. This underrepresents code review and merge activity for all contributors.

3. **Cost Rates Are Internal.** The $30/hr rate is what the company pays, not what clients are billed. Revenue margin analysis requires billing rates (not available in Manazer).

4. **Animesh Data Unreliable.** The "Animesh" Manazer contributor record mixes two different people's activities. Cost for the contractor is estimated using employment days (8), not Manazer Active Days. His 0-activity count may be partially a data capture issue rather than purely zero output.

5. **Project Tagging Is Clean.** Full MCP refresh confirmed zero nil-project activities across all contractors. Every activity is attributed to a project. Earlier analysis (pre-MCP refresh) showed apparent "unaccounted" activities — this was a data visibility limitation (top-2 project view), not a tagging discipline failure.

---

*Analysis prepared under the Jon Gray CFO Persona. All data points sourced from the Verified Fact-Finding Report (Feb 20, 2026) with full project breakdowns from MCP refresh.*
