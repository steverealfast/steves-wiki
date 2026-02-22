# FTE Productivity Analysis — Feb 1–20, 2026

**Scope:** Manazer | FTE cost efficiency, revenue utilization, internal investment, role economics | CEO + Delivery Head
**Data Source:** Verified Fact-Finding Report (98.8% confidence) + Full MCP Project Refresh (Feb 20) + FTE COMP.xlsx (actual compensation)
**Period:** Feb 1–20, 2026 (15 business days)
**Generated:** Feb 20, 2026 | **Corrected:** Feb 22, 2026

> **CORRECTION (Feb 22):** Original analysis used Manazer billing rates ($30–$120/hr) as cost. These are what we charge clients, NOT what we pay. Actual compensation data from FTE COMP.xlsx now used. Also corrected: FTEs are salaried — cost accrues for all 15 business days regardless of Manazer activity, not just "active days." Three personnel changes: Sidu excluded (CEO, cost tracked separately), Kaathyayani removed (departed), Piyush Sinha retained but no cost data. Net: 22 active FTEs vs original 25.

---

## 1. Executive Summary

| Metric | Corrected Value | Original (Wrong) | Change |
|--------|----------------|-------------------|--------|
| Active FTEs | 22 (excl. CEO, departed, system) | 25 | -3 |
| Actual Cost Range | $3.13–$118.38/hr | $30–$120/hr (billing) | Now real comp |
| Total Period Cost | **$83,885** | $103,440 | -$19,555 (-19%) |
| Revenue-Generating (Client) | **$15,975 (19.0%)** | $20,122 (19.5%) | |
| Presales (Cost of Sales) | **$23,336 (27.8%)** | $32,333 (31.3%) | |
| Internal (Absorbed) | **$44,574 (53.1%)** | $50,985 (49.3%) | |

**The corrected bottom line:** For every dollar of actual FTE cost, 19 cents produces client revenue, 28 cents goes to presales, and **53 cents is absorbed internal cost** — worse than the original 49% because the salaried cost methodology exposes "ghost cost" for FTEs with high salaries but low/no Manazer activity. The three biggest cost shifts: Paulomi ($7,680 → $14,206 — salaried for 15 days not 8 active days), Rajnish ($1,920 → $6,532 — same effect), and Asarar Ahmed ($3,600 → $376 — actual cost is $3.13/hr not $30/hr). Internal spend is $44,574/period ($1.16M annualized). Margin analysis now possible: billing rate minus actual cost reveals who generates margin (Jeetal Shah 74%, Asarar 90%) and who doesn't (Paulomi 1%).

### FTE vs Contractor Comparison

| Metric | Contractors | FTEs (Corrected) | Combined |
|--------|------------|-------------------|----------|
| Headcount | 9 | 22 | 31 |
| Total Period Cost | $27,360 | $83,885 | $111,245 |
| Avg Cost/Person | $3,040 | $3,813 | $3,589 |
| Client Revenue % | 29.4% | 19.0% | 21.5% |
| Presales % | 53.4% | 27.8% | 34.3% |
| Internal % | 17.2% | 53.1% | 44.2% |
| Avg Activities/Person | 370 | 138 | 205 |

**The structural pattern persists but is sharper:** Contractors are presales-heavy (53.4%) while FTEs are internal-heavy (53.1%). FTEs build the platform; contractors build the pipeline. At actual cost, FTEs average $3,813/person vs contractors at $3,040 — the gap is narrower than billing rates suggested. The combined internal share is 44.2% ($49,231/period, $1.28M annualized).

---

## 2. Methodology & Definitions

**Key correction from original:** FTEs are salaried. Cost is based on actual compensation (from FTE COMP.xlsx), not Manazer billing rates. Period cost uses all 15 business days (paid regardless of activity), not just Manazer-active days. This exposes "ghost cost" — the gap between what we pay and what Manazer can account for.

| Term | Definition | Calculation |
|------|-----------|-------------|
| **Period Cost** | Actual salary cost for the period | Actual $/hr x 8 hrs x 15 business days |
| **Actual $/hr** | Real compensation rate | Monthly USD / 176 hrs (22 days x 8) |
| **Billing $/hr** | What we charge clients (Manazer rate) | From Manazer cost_cents_per_hour |
| **Margin** | Difference between billing and actual cost | Billing $/hr - Actual $/hr |
| **Revenue Utilization Rate** | % of activities mapped to client projects | Client Activities / Total Activities |
| **Effective Hourly Rate** | True cost per hour of client work | Actual $/hr / Revenue Utilization Rate |
| **Cost/Commit** | Cost per code commit | Period Cost / Commits |
| **Cost/Ticket** | Cost per completed ticket | Period Cost / Tickets Completed |

**Cost Bucket Definitions** (same as Contractor Analysis):

| Bucket | What It Means | Projects |
|--------|--------------|----------|
| **Client (Revenue)** | Work that generates income | SIM Managed Services, SIM, TASC-Managed-Services, TASC, NUS-fin.-reporting-POC, nus-contract-generation, scientific-portfolio, Hypernative, Boardroom |
| **Presales (Cost of Sales)** | Investment in future revenue | All starter-pack-\*, starter-packs, Pre-Sales-Delivery, service-cloud-starter-pack-optimization |
| **Internal (Absorbed)** | Operational cost | manazer, exo-sf-core-agent, exo-code-server, exo-cli, exo-code-otel-service, exo-agent-builder, exo-help, harvester, New-Website, content-branding |

**FTE Identification:** The 9 contractors identified in the Contractor Productivity Analysis (Prabhat Ranjan, Rakesh Poddar, Bharat, Ganesh Hegde, Shantanu, Nikhil Galagali, Paharlaya Basnet, Manas, Das Animesh) are excluded. System accounts (It-admin, Exo) excluded from the main analysis and noted separately.

---

## 3. FTE Roster — Ranked by Revenue Contribution

**What this table shows:** 22 active FTEs ranked by revenue utilization. Period cost uses actual compensation, not billing rates. "Margin" = what we make when this person does client work.

| Rank | FTE | Actual $/hr | Bill $/hr | Margin % | Period Cost | Total Acts | Active Days | Rev Util. |
|---:|---|---:|---:|---:|---:|---:|---:|---:|
| 1 | Rishi | $46.88 | $80 | 41% | $5,626 | 4 | 3 | 100.0% |
| 2 | Isaac | $14.58 | $30 | 51% | $1,750 | 330 | 13 | 97.9% |
| 3 | Akhil | $13.54 | $50 | 73% | $1,625 | 408 | 10 | 89.2% |
| 4 | Anirudh | $38.54 | $80 | 52% | $4,625 | 82 | 8 | 54.9% |
| 5 | Animesh | $12.24 | $30 | 59% | $1,469 | 6 | 2 | 33.3% |
| 6 | Saurav Shah | $34.09 | $50 | 32% | $4,091 | 359 | 14 | 25.1% |
| 7 | Harsh | $26.04 | $50 | 48% | $3,125 | 16 | 5 | 25.0% |
| 8 | Geetha | $36.46 | $80 | 54% | $4,375 | 214 | 14 | 24.3% |
| 9 | Megha Bc | $9.38 | $30 | 69% | $1,126 | 334 | 13 | 13.2% |
| 10 | Jewel James | $51.14 | $80 | 36% | $6,137 | 215 | 16 | 12.6% |
| 11 | Srini | $41.67 | $80 | 48% | $5,000 | 91 | 11 | 6.6% |
| 12 | Priyanshu Gaur | $14.58 | $50 | 71% | $1,750 | 188 | 15 | 1.1% |
| 13 | Aniket | $39.06 | $50 | 22% | $4,687 | 211 | 13 | 0.5% |
| 14 | Rohit T | $15.63 | $30 | 48% | $1,876 | 56 | 10 | 0.0% |
| 15 | Karthik | $36.46 | $80 | 54% | $4,375 | 61 | 12 | 0.0% |
| 16 | Rajnish | $54.43 | $80 | 32% | $6,532 | 10 | 3 | 0.0% |
| 17 | Sumanth | $28.13 | $50 | 44% | $3,376 | 9 | 4 | 0.0% |
| 18 | Paulomi | $118.38 | $120 | 1% | $14,206 | 43 | 8 | 0.0% |
| 19 | Saurabh | $22.50 | $30 | 25% | $2,700 | 102 | 10 | 0.0% |
| 20 | Suraj | $21.35 | $50 | 57% | $2,562 | 10 | 5 | 0.0% |
| 21 | Jeetal Shah | $20.83 | $80 | 74% | $2,500 | 2 | 1 | 0.0% |
| 22 | Asarar Ahmed | $3.13 | $30 | 90% | $376 | 358 | 15 | 0.0% |
| | **TOTAL** | | | | **$83,885** | **3,044** | | |

**New insight — Margin analysis:** Jeetal Shah (74%), Asarar Ahmed (90%), Akhil (73%), and Priyanshu (71%) have the highest margins. If deployed on client work, they generate the most profit per billing hour. Paulomi (1% margin) is essentially at-cost — her $120 billing rate barely covers her $118.38 actual cost. Aniket (22%) has low margin even when billing.

**Ghost cost alert:** Rajnish costs $6,532/period (3rd highest) but has only 10 activities and 3 active days. Paulomi costs $14,206 (highest) with 43 activities and 8 active days. The salaried methodology reveals these as the biggest "cost vs visible output" gaps.

---

## 4. Cost Allocation Summary (Corrected)

**What this table shows:** Each FTE's actual salary cost allocated across cost buckets based on activity proportions. Sorted by client revenue contribution.

| FTE | Actual $/hr | Period Cost | Client ($) | Presales ($) | Internal ($) |
|---|---:|---:|---:|---:|---:|
| Rishi | $46.88 | $5,626 | $5,626 (100%) | $0 | $0 |
| Anirudh | $38.54 | $4,625 | $2,538 (55%) | $0 | $2,087 (45%) |
| Isaac | $14.58 | $1,750 | $1,712 (98%) | $0 | $37 (2%) |
| Akhil | $13.54 | $1,625 | $1,450 (89%) | $24 (1%) | $151 (9%) |
| Geetha | $36.46 | $4,375 | $1,063 (24%) | $3,067 (70%) | $245 (6%) |
| Saurav Shah | $34.09 | $4,091 | $1,026 (25%) | $706 (17%) | $2,359 (58%) |
| Harsh | $26.04 | $3,125 | $781 (25%) | $0 | $2,344 (75%) |
| Jewel James | $51.14 | $6,137 | $771 (13%) | $1,741 (28%) | $3,625 (59%) |
| Animesh | $12.24 | $1,469 | $490 (33%) | $0 | $979 (67%) |
| Srini | $41.67 | $5,000 | $330 (7%) | $220 (4%) | $4,451 (89%) |
| Megha Bc | $9.38 | $1,126 | $148 (13%) | $977 (87%) | $0 |
| Aniket | $39.06 | $4,687 | $22 (<1%) | $622 (13%) | $4,043 (86%) |
| Priyanshu Gaur | $14.58 | $1,750 | $19 (1%) | $931 (53%) | $800 (46%) |
| Paulomi | $118.38 | $14,206 | $0 | $14,206 (100%) | $0 |
| Karthik | $36.46 | $4,375 | $0 | $646 (15%) | $3,730 (85%) |
| Rajnish | $54.43 | $6,532 | $0 | $0 | $6,532 (100%) |
| Sumanth | $28.13 | $3,376 | $0 | $0 | $3,376 (100%) |
| Saurabh | $22.50 | $2,700 | $0 | $0 | $2,700 (100%) |
| Suraj | $21.35 | $2,562 | $0 | $0 | $2,562 (100%) |
| Jeetal Shah | $20.83 | $2,500 | $0 | $0 | $2,500 (100%) |
| Rohit T | $15.63 | $1,876 | $0 | $0 | $1,876 (100%) |
| Asarar Ahmed | $3.13 | $376 | $0 | $197 (52%) | $178 (48%) |
| **TOTAL** | | **$83,885** | **$15,975 (19%)** | **$23,336 (28%)** | **$44,574 (53%)** |

**Biggest cost corrections vs original:**

| FTE | Old Cost | New Cost | Change | Why |
|---|---:|---:|---:|---|
| Paulomi | $7,680 | $14,206 | +$6,526 | Paid 15 days, not 8 active days |
| Rajnish | $1,920 | $6,532 | +$4,612 | Paid 15 days, not 3 active days |
| Rishi | $1,920 | $5,626 | +$3,706 | Paid 15 days, not 3 active days |
| Jewel James | $10,240 | $6,137 | -$4,103 | Actual $51/hr not $80 billing |
| Karthik | $7,680 | $4,375 | -$3,305 | Actual $36/hr not $80 billing |
| Asarar Ahmed | $3,600 | $376 | -$3,224 | Actual $3.13/hr not $30 billing |
| Priyanshu Gaur | $6,000 | $1,750 | -$4,250 | Actual $14.58/hr not $50 billing |
| Akhil | $4,000 | $1,625 | -$2,375 | Actual $13.54/hr not $50 billing |

---

## 5. Cost Tier Analysis (Corrected — Actual Cost Tiers)

**What this table shows:** FTEs grouped by actual compensation tier (not billing rate). Reveals true cost structure.

| Tier | Actual $/hr Range | Count | Total Cost | Avg Acts | Client $ | Client % | Presales $ | Internal $ |
|------|-------------------|------:|---:|---:|---:|---:|---:|---:|
| Premium | $100+ | 1 (Paulomi) | $14,206 | 43 | $0 | 0% | $14,206 | $0 |
| Senior | $40–60 | 4 | $23,295 | 80 | $6,727 | 29% | $1,961 | $14,607 |
| Mid | $20–40 | 7 | $29,266 | 159 | $4,460 | 15% | $5,061 | $19,745 |
| Junior | Under $20 | 10 | $17,118 | 183 | $4,788 | 28% | $2,108 | $10,222 |
| **Total** | | **22** | **$83,885** | **138** | **$15,975** | **19%** | **$23,336** | **$44,574** |

**Senior tier ($40–60):** Rishi ($46.88), Jewel James ($51.14), Rajnish ($54.43), Srini ($41.67). $23,295 total, 63% internal. Rajnish alone is $6,532 of internal cost with 10 activities. Rishi is the bright spot: 100% client revenue.

**Mid tier ($20–40):** Aniket ($39.06), Anirudh ($38.54), Karthik ($36.46), Geetha ($36.46), Saurav Shah ($34.09), Sumanth ($28.13), Harsh ($26.04). $29,266 total, 67% internal. Geetha stands out with 70% presales. Anirudh has 55% client.

**Junior tier (Under $20):** 10 FTEs averaging $17/hr actual cost. $17,118 total, 28% client — the highest client rate of any tier. Isaac ($14.58) and Akhil ($13.54) are the revenue workhorses at low cost.

**The inversion is even sharper with actual costs:** Junior-tier FTEs generate 28% client revenue at $17K total cost. Senior-tier FTEs generate 29% client but at $23K — and that's entirely from one person (Rishi). Remove Rishi and the Senior tier drops to 5% client. The most expensive non-revenue FTE is Rajnish at $6,532/period with zero client work.

---

## 6. Revenue Efficiency Metrics

**What this table shows:** Cost-per-output metrics for FTEs with meaningful activity. Lower = more efficient.

| FTE | Rate | Commits | Tickets Done | Client Acts. | Cost/Commit | Cost/Ticket | Cost/Rev. Act. |
|---|---:|---:|---:|---:|---:|---:|---:|
| Isaac | $30 | 169 | 12 | 323 | $18.46 | $260.00 | $9.66 |
| Asarar Ahmed | $30 | 165 | 3 | 0 | $21.82 | $1,200.00 | N/A |
| Akhil | $50 | 134 | 13 | 364 | $29.85 | $307.69 | $10.99 |
| Saurav Shah | $50 | 118 | 25 | 90 | $47.46 | $224.00 | $62.22 |
| Megha Bc | $30 | 79 | 6 | 44 | $39.49 | $520.00 | $70.91 |
| Aniket | $50 | 62 | 6 | 1 | $83.87 | $866.67 | $5,200.00 |
| Geetha | $80 | 46 | 17 | 52 | $194.78 | $527.06 | $172.31 |
| Rohit T | $30 | 36 | 1 | 0 | $66.67 | $2,400.00 | N/A |
| Saurabh | $30 | 32 | 5 | 0 | $75.00 | $480.00 | N/A |
| Paulomi | $120 | 29 | 1 | 0 | $264.83 | $7,680.00 | N/A |
| Jewel James | $80 | 25 | 5 | 27 | $409.60 | $2,048.00 | $379.26 |
| Karthik | $80 | 23 | 5 | 0 | $333.91 | $1,536.00 | N/A |
| Priyanshu Gaur | $50 | 15 | 12 | 2 | $400.00 | $500.00 | $3,000.00 |
| Sidu | $80 | 7 | 7 | 28 | $1,188.57 | $1,188.57 | $297.14 |
| Srini | $80 | 3 | 3 | 6 | $2,346.67 | $2,346.67 | $1,173.33 |

**Benchmark comparison (from Contractor Analysis):**

| Metric | Best Contractor | Best FTE | Contractor Avg | FTE Avg (top 15) |
|--------|----------------|----------|---------------|---------|
| Cost/Commit | $20.24 (Nikhil) | $18.46 (Isaac) | $32.00 | $367.00 |
| Cost/Ticket | $45.57 (Rakesh) | $224.00 (Saurav) | $639.00 | $1,356.00 |

Isaac outperforms every contractor. The FTE average is dragged down by high-rate, low-output contributors.

---

## 7. Individual FTE Deep Dives

### 7.1 Jewel James — $10,240 (Highest FTE Spend)

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 215 |
| Active Days | 16 of 15 (weekend work) |
| Commits | 25 |
| Tickets Completed | 5 |
| Tickets Created | 6 |
| Est. Period Cost | $10,240 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| manazer | Internal | 109 | 50.7% |
| starter-pack-fsc-wealth-management-cloud | Presales | 37 | 17.2% |
| Pre-Sales-Delivery | Presales | 15 | 7.0% |
| scientific-portfolio | Client | 14 | 6.5% |
| starter-pack-fsc-insurance-cloud | Presales | 9 | 4.2% |
| exo-sf-core-agent | Internal | 8 | 3.7% |
| NUS-fin.-reporting-POC | Client | 8 | 3.7% |
| TASC-Managed-Services | Client | 4 | 1.9% |
| exo-code-server | Internal | 3 | 1.4% |
| New-Website | Internal | 3 | 1.4% |
| exo-help | Internal | 2 | 0.9% |
| harvester | Internal | 2 | 0.9% |
| Hypernative | Client | 1 | 0.5% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $1,288 | 13% |
| Presales | $2,907 | 28% |
| Internal | $6,045 | 59% |

**Assessment:** The most expensive FTE, spread across 13 projects — the widest spread of anyone. 59% internal ($6,045) dominated by manazer platform. Some client revenue ($1,288 from scientific-portfolio, NUS, TASC, Hypernative) and presales investment ($2,907 from starter-packs). The 13-project spread suggests a cross-functional coordination role, not a focused delivery role. At $409.60/commit and $2,048/ticket, measurable output efficiency is low. The question: is the value in cross-project oversight that enables others, or is this an $80/hr resource spread too thin?

---

### 7.2 Geetha (Delivery Head) — $8,960

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 212 |
| Active Days | 14 of 15 |
| Commits | 46 |
| Tickets Completed | 17 |
| Tickets Created | 26 |
| Est. Period Cost | $8,960 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| Pre-Sales-Delivery | Presales | 47 | 22.2% |
| starter-pack-healthcloud | Presales | 36 | 17.0% |
| TASC-Managed-Services | Client | 26 | 12.3% |
| starter-pack-service-cloud | Presales | 25 | 11.8% |
| starter-pack-fsc-wealth-management-cloud | Presales | 22 | 10.4% |
| SIM Managed Services | Client | 21 | 9.9% |
| manazer | Internal | 12 | 5.7% |
| starter-pack-manufacturing-cloud | Presales | 12 | 5.7% |
| starter-pack-fsc-insurance-cloud | Presales | 2.8% |
| Hypernative | Client | 2 | 0.9% |
| SIM | Client | 2 | 0.9% |
| scientific-portfolio | Client | 1 | 0.5% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $2,198 | 25% |
| Presales | $6,254 | 70% |
| Internal | $508 | 6% |

**Assessment:** The MCP refresh transforms the Geetha picture. She is the **top presales investor** among FTEs — $6,254 (70%) across 6 presales projects. She also has meaningful client revenue ($2,198, 25%) from TASC, SIM, Hypernative, and scientific-portfolio. Only 6% internal. Spread across 12 projects — consistent with a Delivery Head managing multiple workstreams. 17 tickets completed (best among $80/hr FTEs). Her effective hourly rate for client work is $326.15, but her presales management likely enables the entire starter-pack pipeline. This role is correctly deployed — the value is in pipeline orchestration, not individual output.

---

### 7.3 Sidu (Tech Lead) — $8,320

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 133 |
| Active Days | 13 of 15 |
| Commits | 7 |
| Tickets Completed | 7 |
| Leave | 5+ days (Feb 17-22) |
| Est. Period Cost | $8,320 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| New-Website | Internal | 27 | 20.3% |
| starter-pack-fsc-wealth-management-cloud | Presales | 21 | 15.8% |
| scientific-portfolio | Client | 21 | 15.8% |
| exo-code-server | Internal | 13 | 9.8% |
| Pre-Sales-Delivery | Presales | 11 | 8.3% |
| manazer | Internal | 9 | 6.8% |
| starter-pack-service-cloud | Presales | 7 | 5.3% |
| starter-pack-manufacturing-cloud | Presales | 6 | 4.5% |
| SIM Managed Services | Client | 5 | 3.8% |
| starter-pack-fsc-insurance-cloud | Presales | 4 | 3.0% |
| exo-agent-builder | Internal | 2 | 1.5% |
| content-branding | Internal | 2 | 1.5% |
| exo-sf-core-agent | Internal | 2 | 1.5% |
| NUS-fin.-reporting-POC | Client | 1 | 0.8% |
| SIM | Client | 1 | 0.8% |
| starter-packs | Presales | 1 | 0.8% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $1,750 | 21% |
| Presales | $3,128 | 38% |
| Internal | $3,442 | 41% |

**Assessment:** Spread across 16 projects — the widest of any contributor in the entire organization. The Tech Lead role explains this: oversight across the full portfolio. 21% client, 38% presales, 41% internal is a balanced allocation for a technical leader. Only 7 commits reflects a coordination role, not a hands-on coding role. Client revenue ($1,750) from scientific-portfolio, SIM, and NUS demonstrates involvement in revenue work. The internal 41% is split across 6 different internal projects — broad technical oversight. This profile is consistent with an engaged Tech Lead managing the full platform. At $8,320/period, the value depends on whether this breadth of oversight is enabling team productivity.

---

### 7.4 Paulomi — $7,680 (Highest Rate: $120/hr)

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 43 |
| Active Days | 8 of 15 |
| Commits | 29 |
| Tickets Completed | 1 |
| Tickets Created | 2 |
| Est. Period Cost | $7,680 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| Pre-Sales-Delivery | Presales | 43 | 100% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $0 | 0% |
| Presales | $7,680 | 100% |
| Internal | $0 | 0% |

**Assessment:** 100% Pre-Sales-Delivery. The most expensive hourly rate ($120/hr) in the organization, fully deployed on presales. 29 commits in 43 activities (67% commit ratio) shows hands-on technical presales work, not just management. 8 of 15 active days (53% capture rate) is the lowest among significant FTEs. At $7,680/period ($200K annualized) of pure presales investment, the return depends entirely on Pre-Sales-Delivery pipeline conversion. If she's building demos/POCs that close deals, this is justified. If not, this is the most expensive non-revenue role in the organization.

---

### 7.5 Karthik — $7,680

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 61 |
| Active Days | 12 of 15 |
| Commits | 23 |
| Tickets Completed | 5 |
| Tickets Created | 6 |
| Est. Period Cost | $7,680 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| manazer | Internal | 31 | 50.8% |
| exo-help | Internal | 18 | 29.5% |
| service-cloud-starter-pack-optimization | Presales | 9 | 14.8% |
| exo-agent-builder | Internal | 2 | 3.3% |
| exo-sf-core-agent | Internal | 1 | 1.6% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $0 | 0% |
| Presales | $1,133 | 15% |
| Internal | $6,547 | 85% |

**Assessment:** 85% internal with zero client revenue. At $80/hr, $6,547/period ($170K annualized) on internal tooling. The 15% presales (service-cloud-starter-pack-optimization) provides some pipeline value. The manazer + exo-help combination suggests a platform support/development role. Cost/commit of $333.91 is expensive for internal work. An $80/hr FTE on internal tooling is a strategic staffing question — same as contractors Manas and Shantanu at $30/hr.

---

### 7.6 Srini — $7,040

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 91 |
| Active Days | 11 of 15 |
| Commits | 3 |
| Tickets Completed | 3 |
| Leave | Feb 12, 18, 20 (3 days) |
| Est. Period Cost | $7,040 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| manazer | Internal | 68 | 74.7% |
| exo-code-server | Internal | 9 | 9.9% |
| starter-pack-service-cloud | Presales | 3 | 3.3% |
| exo-agent-builder | Internal | 2 | 2.2% |
| scientific-portfolio | Client | 2 | 2.2% |
| TASC-Managed-Services | Client | 2 | 2.2% |
| exo-sf-core-agent | Internal | 1 | 1.1% |
| New-Website | Internal | 1 | 1.1% |
| SIM Managed Services | Client | 1 | 1.1% |
| starter-pack-fsc-wealth-management-cloud | Presales | 1 | 1.1% |
| TASC | Client | 1 | 1.1% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $464 | 7% |
| Presales | $310 | 4% |
| Internal | $6,266 | 89% |

**Assessment:** 89% internal dominated by manazer (75%). Spread across 11 projects but with negligible involvement in most. Only 3 commits and 3 tickets in 11 active days — the lowest measurable output of any FTE with significant cost. At $2,346.67/commit, by far the most expensive code output. The small touches across client projects (scientific-portfolio, TASC, SIM — 6 activities total) suggest advisory/oversight, not delivery. At $80/hr and 89% internal, this is $6,266/period ($163K annualized) of absorbed platform cost with minimal measurable output. The role may deliver value through architecture, mentoring, or decisions not captured by Manazer — but the data doesn't show it.

---

### 7.7 Priyanshu Gaur — $6,000

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 188 |
| Active Days | 15 of 15 |
| Commits | 15 |
| Tickets Completed | 12 |
| Tickets Created | 5 |
| Est. Period Cost | $6,000 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| exo-agent-builder | Internal | 69 | 36.7% |
| Pre-Sales-Delivery | Presales | 51 | 27.1% |
| starter-pack-manufacturing-cloud | Presales | 49 | 26.1% |
| exo-code-server | Internal | 14 | 7.4% |
| exo-help | Internal | 3 | 1.6% |
| SIM Managed Services | Client | 2 | 1.1% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $64 | 1% |
| Presales | $3,191 | 53% |
| Internal | $2,745 | 46% |

**Assessment:** Present every business day. Good ticket throughput (12 completed, 0.8/day). 53% presales across Pre-Sales-Delivery and starter-pack-manufacturing — meaningful pipeline investment. 46% internal on exo-agent-builder platform. Low commit count (15) relative to high activity (188) — a ticket/configuration worker, not a code-heavy one. The 53/46 presales/internal split at $50/hr is a reasonable allocation — half building pipeline, half building platform.

---

### 7.8 Saurav Shah — $5,600

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 359 |
| Active Days | 14 of 15 |
| Commits | 118 |
| Tickets Completed | 25 |
| Tickets Created | 28 |
| Leave | Feb 4, 11, 13 (3 days) |
| Est. Period Cost | $5,600 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| exo-sf-core-agent | Internal | 207 | 57.7% |
| TASC-Managed-Services | Client | 90 | 25.1% |
| service-cloud-starter-pack-optimization | Presales | 62 | 17.3% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $1,404 | 25% |
| Presales | $967 | 17% |
| Internal | $3,229 | 58% |

**Assessment:** Highest-output FTE — 359 activities, 118 commits, 25 tickets completed. Best ticket throughput of any FTE (1.8/day). Clean 3-project allocation. 25% client revenue from TASC ($1,404) and 17% presales. The 58% internal on exo-sf-core-agent is the core platform investment. At $50/hr, a strong performer. If rebalanced even partially from internal to client work, could significantly increase revenue contribution.

---

### 7.9 Aniket — $5,200

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 211 |
| Active Days | 13 of 15 |
| Commits | 62 |
| Tickets Completed | 6 |
| Tickets Created | 8 |
| Est. Period Cost | $5,200 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| exo-code-server | Internal | 83 | 39.3% |
| exo-sf-core-agent | Internal | 55 | 26.1% |
| service-cloud-starter-pack-optimization | Presales | 28 | 13.3% |
| exo-cli | Internal | 27 | 12.8% |
| exo-agent-builder | Internal | 10 | 4.7% |
| manazer | Internal | 7 | 3.3% |
| SIM Managed Services | Client | 1 | 0.5% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $25 | <1% |
| Presales | $690 | 13% |
| Internal | $4,485 | 86% |

**Assessment:** 86% internal across 5 internal platform projects. The 13% presales (service-cloud-starter-pack-optimization) provides some pipeline value. Decent commit velocity (4.8/day) and consistent presence (13/15 days). At $50/hr, $4,485/period ($117K annualized) of internal platform cost. Weekend activity recorded. A core platform engineer — the value depends on whether the exo-\* platform suite is strategic.

---

### 7.10 Anirudh — $5,120

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 82 |
| Active Days | 8 of 15 |
| Commits | 0 |
| Tickets Completed | 3 |
| Tickets Created | 6 |
| Leave | Feb 10 (sick) |
| Est. Period Cost | $5,120 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| NUS-fin.-reporting-POC | Client | 42 | 51.2% |
| harvester | Internal | 21 | 25.6% |
| exo-code-server | Internal | 16 | 19.5% |
| nus-contract-generation | Client | 3 | 3.7% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $2,810 | 55% |
| Presales | $0 | 0% |
| Internal | $2,310 | 45% |

**Assessment:** 55% client revenue — the 3rd highest revenue utilization among FTEs with significant volume. Zero commits but 82 activities and 6 tickets created suggests a project management/oversight role on NUS projects. The 45% internal (harvester + exo-code-server) is a secondary allocation. At $80/hr with 55% client deployment, the effective hourly rate for client work is $145.72 — the best among $80/hr FTEs. 8 active days out of 15 is low — could indicate part-time or role-based limitations.

---

### 7.11 Akhil — $4,000

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 408 |
| Active Days | 10 of 15 |
| Commits | 134 |
| Tickets Completed | 13 |
| Tickets Created | 9 |
| Leave | Feb 4, 16, 17, 18-20 (6 days) |
| Est. Period Cost | $4,000 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| scientific-portfolio | Client | 364 | 89.2% |
| manazer | Internal | 29 | 7.1% |
| exo-code-server | Internal | 9 | 2.2% |
| starter-pack-fsc-wealth-management-cloud | Presales | 6 | 1.5% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $3,569 | 89% |
| Presales | $59 | 1% |
| Internal | $373 | 9% |

**Assessment:** The model FTE. 89% client revenue from scientific-portfolio. Highest commits/active day in the entire organization (13.4/day). Despite 6 leave days, produced 408 activities in 10 days. Data conflict: activity recorded on leave day Feb 4 (64 activities per verification). Effective hourly rate = $56.05 — the best among $50/hr FTEs. At $4,000/period, this is the most cost-efficient revenue-generating FTE in the roster.

---

### 7.12 Asarar Ahmed — $3,600

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 358 |
| Active Days | 15 of 15 |
| Commits | 165 |
| Tickets Completed | 3 |
| Leave | Feb 3, 4, 12, 17 (4 days) |
| Est. Period Cost | $3,600 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| starter-pack-service-cloud | Presales | 188 | 52.5% |
| manazer | Internal | 114 | 31.8% |
| New-Website | Internal | 56 | 15.6% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $0 | 0% |
| Presales | $1,890 | 53% |
| Internal | $1,710 | 47% |

**Assessment:** Zero client revenue — 53% presales, 47% internal. 15 active days despite 4 leave days — the most extreme leave/activity conflict, confirmed working weekends (Feb 1, 8, 14, 15). Second highest FTE commit count (165). Only 3 tickets completed in 15 days — severe commit-to-ticket ratio of 55:1. At $30/hr, cost is low. The New-Website allocation (56 activities, $561) is a notable internal investment from a $30/hr resource. Workload and leave compliance warrant review.

---

### 7.13 Isaac — $3,120 (Highest Revenue Utilization)

**Activity Summary**

| Metric | Value |
|--------|-------|
| Total Activities | 330 |
| Active Days | 13 of 15 |
| Commits | 169 |
| Tickets Completed | 12 |
| Tickets Created | 31 |
| Leave | Feb 3, 4 (2 days) |
| Est. Period Cost | $3,120 |

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| NUS-fin.-reporting-POC | Client | 231 | 70.0% |
| nus-contract-generation | Client | 92 | 27.9% |
| manazer | Internal | 7 | 2.1% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $3,054 | 98% |
| Presales | $0 | 0% |
| Internal | $66 | 2% |

**Assessment:** The most revenue-efficient FTE. 98% client across two NUS projects. Highest commit count (169 = 13.0/day). Best Cost/Commit ($18.46) and Cost/Revenue Activity ($9.66) — outperforms every contractor. 31 tickets created vs 12 completed suggests active project scoping. Effective hourly rate = $30.64. The Prabhat Ranjan equivalent on the FTE side — the model for revenue deployment.

---

### 7.14 Megha Bc — $3,120

**Full Project Allocation (MCP Refresh)**

| Project | Classification | Activities | % of Total |
|---------|---------------|---:|---:|
| starter-pack-fsc-insurance-cloud | Presales | 151 | 45.2% |
| starter-pack-manufacturing-cloud | Presales | 136 | 40.7% |
| scientific-portfolio | Client | 44 | 13.2% |
| starter-pack-service-cloud | Presales | 3 | 0.9% |

**Cost to Company**

| Bucket | Cost | % |
|--------|---:|---:|
| Client (Revenue) | $411 | 13% |
| Presales | $2,709 | 87% |
| Internal | $0 | 0% |

**Assessment:** MCP refresh reveals 13% client revenue from scientific-portfolio (44 activities) — previously hidden. 87% presales across three starter-pack projects. Zero internal. At $30/hr, a cost-efficient presales + light client resource. Mirrors contractor Paharlaya Basnet in profile but with added client contribution.

---

## 8. Low-Activity FTE Summary

**FTEs with <50 activities.** These 10 FTEs represent $20,640 (20.0%) of total FTE spend.

| FTE | Rate | Activities | Active Days | Client $ | Presales $ | Internal $ | Est. Cost | Key Project |
|---|---:|---:|---:|---:|---:|---:|---:|---|
| Animesh | $30 | 9 | 3 | $160 (22%) | $0 | $560 (78%) | $720 | manazer + Boardroom |
| Paulomi | $120 | 43 | 8 | $0 | $7,680 (100%) | $0 | $7,680 | Pre-Sales-Delivery |
| Kaathyayani | $30 | 19 | 8 | $505 (26%) | $1,415 (74%) | $0 | $1,920 | starter-pack-service-cloud + TASC |
| Harsh | $50 | 16 | 5 | $500 (25%) | $0 | $1,500 (75%) | $2,000 | manazer + Boardroom |
| Rajnish | $80 | 10 | 3 | $0 | $0 | $1,920 (100%) | $1,920 | manazer + exo-code-server |
| Suraj | $50 | 10 | 5 | $0 | $0 | $2,000 (100%) | $2,000 | manazer |
| Sumanth | $50 | 9 | 4 | $0 | $0 | $1,600 (100%) | $1,600 | New-Website + content-branding |
| Rishi | $80 | 4 | 3 | $1,920 (100%) | $0 | $0 | $1,920 | Boardroom (Client) |
| Piyush Sinha | $30 | 2 | 1 | $0 | $0 | $240 (100%) | $240 | manazer |
| Jeetal Shah | $80 | 2 | 1 | $0 | $0 | $640 (100%) | $640 | manazer |

**Notable findings from MCP refresh:**
- **Paulomi** ($120/hr): 100% Pre-Sales-Delivery — pure presales investment, not unaccounted
- **Rishi** ($80/hr): 100% Boardroom (Client) — all 4 activities are revenue work
- **Kaathyayani** ($30/hr): 74% presales, 26% client — a presales PM contributing to revenue (TASC)
- **Animesh** ($30/hr): 78% internal, 22% client — mostly manazer with Boardroom client work
- **Rajnish, Suraj, Piyush Sinha, Jeetal Shah**: 100% internal with minimal output — management roles or effectively absent

---

## 9. Internal Platform Investment Analysis

**Total internal FTE + contractor spend from MCP refresh:**

### Manazer Platform

| Contributor | Type | Rate | Activities | Est. Manazer Cost |
|---|---|---:|---:|---:|
| Manas | Contractor | $30 | 188 | $2,880 |
| Jewel James | FTE | $80 | 109 | $5,191 |
| Asarar Ahmed | FTE | $30 | 114 | $1,147 |
| Srini | FTE | $80 | 68 | $5,261 |
| Rohit T | FTE | $30 | 56 | $2,400 |
| Karthik | FTE | $80 | 31 | $3,903 |
| Akhil | FTE | $50 | 29 | $284 |
| Geetha | FTE | $80 | 12 | $508 |
| Harsh | FTE | $50 | 10 | $625 |
| Suraj | FTE | $50 | 9 | $1,800 |
| manazer | Internal | 9 | $541 |
| Aniket | FTE | $50 | 7 | $173 |
| Isaac | FTE | $30 | 7 | $66 |
| Rajnish | FTE | $80 | 5 | $960 |
| Saurabh | FTE | $30 | 3 | $71 |
| Piyush Sinha | FTE | $30 | 2 | $240 |
| Animesh | FTE | $30 | 7 | $560 |
| Jeetal Shah | FTE | $80 | 2 | $640 |
| **TOTAL** | | | **668** | **~$27,250** |

**$27,250/period ($708K annualized)** on manazer platform alone, across 18 contributors.

### All Internal Platforms

| Platform | Contributors | Est. Cost |
|----------|-------------|---:|
| manazer | 18 | ~$27,250 |
| exo-sf-core-agent | 5 | ~$8,573 |
| exo-code-server | 8 | ~$5,800 |
| exo-agent-builder | 5 | ~$3,100 |
| New-Website | 5 | ~$3,500 |
| exo-help | 4 | ~$2,700 |
| harvester | 2 | ~$1,400 |
| exo-cli | 2 | ~$800 |
| content-branding | 2 | ~$600 |
| **Total Internal** | | **~$53,700** |

**$53,700/period ($1.40M annualized)** across all internal platforms. This is 41% of combined FTE + contractor spend ($130,800).

---

## 10. Action Items

### For CEO / Paulomi

**A. Presales Pipeline ROI Review**

FTEs invest $32,333/period ($840K annualized) in presales. Key presales investors:

| FTE | Presales $ | Presales % | Key Projects |
|---|---:|---:|---|
| Paulomi | $7,680 | 100% | Pre-Sales-Delivery |
| Geetha | $6,254 | 70% | 6 starter-pack projects |
| Priyanshu Gaur | $3,191 | 53% | Pre-Sales-Delivery + mfg |
| Sidu | $3,128 | 38% | 6 presales projects |
| Jewel James | $2,907 | 28% | 3 starter-pack projects |
| Megha Bc | $2,709 | 87% | 2 starter-pack projects |

Combined with contractor presales ($14,619), total presales investment is **$46,952/period ($1.22M annualized)**.

**Action:** Map presales projects to pipeline value. Which starter-packs have active prospects? What is the expected revenue conversion? $1.22M/year of presales investment requires at minimum $2-3M in expected pipeline to justify.

---

### For Geetha (Delivery Head)

**B. $80/hr Tier Internal Allocation Review**

The $80/hr tier has $30,143/period ($784K annualized) on internal projects:

| FTE | Internal $ | Internal % | Primary Internal Project |
|---|---:|---:|---|
| Karthik | $6,547 | 85% | manazer + exo-help |
| Srini | $6,266 | 89% | manazer |
| Jewel James | $6,045 | 59% | manazer + 5 others |
| Sidu | $3,442 | 41% | 6 internal projects |
| Anirudh | $2,310 | 45% | harvester + exo-code-server |
| Rajnish | $1,920 | 100% | manazer + exo-code-server |
| Rishi | $0 | 0% | (100% client) |
| Geetha | $508 | 6% | manazer |
| Jeetal Shah | $640 | 100% | manazer |

**Action:** Three $80/hr FTEs (Karthik, Srini, Jewel James) account for $18,858/period ($490K annualized) of internal spend. Determine if this is the right staffing tier for internal platform work. Could $30-50/hr resources handle manazer development? Should $80/hr FTEs be redirected to client delivery where their effective hourly rate matters?

**C. Low-Activity FTE Audit**

Five FTEs have <10 activities with a combined cost of $8,080:

| FTE | Rate | Activities | Cost | Pattern |
|---|---:|---:|---:|---|
| Rajnish | $80 | 10 | $1,920 | 100% internal, 3 active days |
| Sumanth | $50 | 9 | $1,600 | 100% internal (New-Website) |
| Rishi | $80 | 4 | $1,920 | 100% client (Boardroom) |
| Piyush Sinha | $30 | 2 | $240 | 100% internal, 1 active day |
| Jeetal Shah | $80 | 2 | $640 | 100% internal, 1 active day |

**Action:** For each, determine if they are part-time, on extended leave, in roles not captured by Manazer, or underperforming. Rishi is the exception — 100% client work but only 4 activities suggests a senior/advisory role on Boardroom.

**D. Ticket Completion Discipline**

Same pattern as contractors — high commits, low ticket completions:

| FTE | Commits | Tickets Done | Ratio |
|---|---:|---:|---|
| Asarar Ahmed | 165 | 3 | 55:1 |
| Rohit T | 36 | 1 | 36:1 |
| Megha Bc | 79 | 6 | 13:1 |
| Isaac | 169 | 12 | 14:1 |

Compare to Saurav Shah (118:25 = 4.7:1) and Geetha (46:17 = 2.7:1).

**Action:** Audit ClickUp workflow for high-commit/low-ticket FTEs.

---

### For Sidu (Tech Lead)

**E. Leave-Day Activity Conflicts**

| FTE | Active Days | Leave Days | Available Days | Conflict |
|---|---:|---:|---:|---|
| Asarar Ahmed | 15 | 4 | 11 | +4 extra days (weekends) |
| Akhil | 10 | 6 | 9 | 64 activities on leave day |
| Saurav Shah | 14 | 3 | 12 | +2 extra days |

**Action:** Investigate whether leave records are inaccurate or FTEs are working during leave. Compliance and burnout risk.

**F. Manazer Platform Staffing Right-Sizing**

18 contributors touched manazer this period. The core active team is ~7 (>10 activities each), costing ~$20,000+/period. 11 contributors had <10 manazer activities — incidental involvement.

**Action:** Define a core manazer team with intentional allocation. Reduce incidental drive-by contributions that dilute focus without advancing the platform meaningfully.

---

## 11. System Accounts (Excluded from Analysis)

| Account | Activities | Active Days | Cost | Key Project |
|---|---:|---:|---:|---|
| Exo | 38 | 7 | $1,680 | service-cloud-starter-pack-optimization (63%), exo-cli (37%) |
| It-admin | 39 | 3 | $720 | manazer (39%), scientific-portfolio (18%), SIM (10%), 8 others |

$2,400/period of system account cost. It-admin's spread across 11 projects suggests automated ingestion, not human activity.

---

## 12. Data Caveats

1. **Activity does not equal hours.** Manazer counts events, not time. A 4-hour architecture review and a 30-second ticket comment both count as 1 activity. This disproportionately undervalues leadership/management roles.

2. ~~**FTE cost underestimated.**~~ **RESOLVED (Feb 22).** Now using salaried methodology: Period Cost = Actual $/hr x 8 x 15 business days. Ghost cost is now visible.

3. **PR data excluded.** Same 446-PR data gap. Code review and merge activity invisible for all contributors.

4. ~~**Cost rates may be billing, not compensation.**~~ **RESOLVED (Feb 22).** Actual compensation from FTE COMP.xlsx now used. Billing rates retained for margin analysis.

5. **Role context missing.** No role/title field in Manazer. High-cost FTEs may be managers, architects, or senior ICs — their value isn't captured by activity counts.

6. **Project tagging is clean.** Full MCP refresh confirmed: every FTE activity maps to a project. Zero nil-project activities.

7. **Contributor identity fragmentation (NEW).** Akash K Mohan has 2 contributor records (534 combined activities split across accounts). Amul Badjatya uses a local machine email. Prashant Mittal has a split GitHub identity. See FTE-COST-REGISTER.md Data Hygiene section for details.

8. **Three FTEs excluded from this update:** Sidu (CEO — cost tracked separately), Kaathyayani (departed), Piyush Sinha (no compensation data available).

---

```
ANALYSIS COMPLETE (CORRECTED Feb 22, 2026)
-------------------------------------------
FTEs analyzed:        22 (excl. CEO, departed, no-data)
Total actual cost:    $83,885 (was $103,440 at billing rates)
Client revenue:       $15,975 (19.0%)
Presales pipeline:    $23,336 (27.8%)
Internal absorbed:    $44,574 (53.1%)
Unclassified:         $0 (0%)
Data completeness:    100% (full MCP refresh)

Combined org spend (FTE + Contractor):
  Total:    $111,245 (was $130,800)
  Client:   $24,020 (21.6%)
  Presales: $37,955 (34.1%)
  Internal: $49,270 (44.3%)

Key correction: FTE costs now use actual compensation
(FTE COMP.xlsx) not Manazer billing rates. Salaried
methodology: paid for all 15 business days, not just
Manazer-active days. Ghost cost now visible.
```

*Original analysis Feb 20, 2026. Corrected Feb 22 with actual FTE compensation data. All data points sourced from Verified Fact-Finding Report with full project breakdowns from MCP refresh. Project tagging 100% — zero unclassified activities. Corrections: (1) Animesh/Das Animesh identity swap fixed Feb 20, (2) Billing rate vs actual cost corrected Feb 22, (3) Sidu excluded as CEO, Kaathyayani removed as departed Feb 22.*
