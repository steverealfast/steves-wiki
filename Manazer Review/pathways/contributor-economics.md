# Pathway: Contributor Economics

**Created:** Feb 20, 2026
**Last Run:** Feb 20, 2026
**Last Outcome Matched:** "Employee productivity, daily output, FTE vs contractor comparison"

---

## Scope Match

This pathway activates when the /jongray Outcome matches:
- contributor economics
- contributor utilization
- contractor productivity
- FTE vs contractor
- employee productivity
- cost per contributor
- workforce efficiency
- team cost analysis

---

## Gap-Closing Prompts

These questions are asked at the start of analysis to close data gaps. Previous answers are shown as defaults — user confirms or updates each run.

### Prompt 1: Contributor Classification (FTE vs Contractor)

**Question:** "Manazer has no employment_type field. I need you to classify each contributor as FTE or Contractor. Here are all cost_contributors grouped by cost tier — please classify each."

**How to present:** Group contributors by cost_cents_per_hour tier. Present each tier as a list. Ask user to mark FTE or Contractor for each person.

**Also ask:**
- "Are there any system accounts to exclude?" (e.g., bots, admin accounts)
- "Are there any out-of-scope roles to exclude?" (e.g., security, HR)

**Last Answer (Feb 20, 2026):**
- $120/hr: Paulomi = FTE
- $80/hr: ALL FTE (Jewel James, Geetha, Sidu, Srini, Anirudh, Karthik, Rajnish, Rishi, Jeetal Shah)
- $50/hr: ALL FTE (Akhil, Saurav Shah, Aniket, Priyanshu Gaur, Harsh, Suraj, Sumanth)
- $30/hr FTE: Isaac, Saurabh, Das Animesh, Kaathyayani, Asarar Ahmed, Megha Bc, Rohit T
- $30/hr Contractor: Rakesh Poddar, Nikhil Galagali, Ganesh Hegde, Bharat, Paharlaya Basnet, Prabhat Ranjan, Shantanu, Manas, Animesh
- Excluded (system): Exo, It-admin
- Excluded (security): Piyush Sinha

**Purpose:** Determines the analysis population. Contractor economics is the primary lens — FTEs are absorbed cost. Contractors must justify their spend.

### Prompt 2: Cost Rate Interpretation

**Question:** "The cost tiers are $30/$50/$80/$120 per hour. Are these internal cost rates (what you pay) or billing rates (what you charge clients)?"

**Last Answer:** Internal cost rates — what the company pays. Billing rates are not in Manazer.

**Purpose:** Determines whether margin analysis is possible. If internal cost only, analysis focuses on cost efficiency and utilization, not margin.

### Prompt 3: Project Classification

**Question:** "I need rules to classify projects into cost buckets. Here are all projects with activity in the period. Can you provide classification rules?"

**How to present:** List all projects. Ask for rules first (e.g., "anything with starter-pack = Presales"), then present ambiguous projects for manual classification.

**Last Answer (Feb 20, 2026):**
- **Presales rule:** Any project with "starter-pack" or "presales" or "pre-sales" in the name + service-cloud-optimization
- **Client projects:** SIM Managed Services, TASC-Managed-Services, NUS-fin.-reporting-POC, nus-contract-generation, scientific-portfolio
- **Internal (ignored):** manazer, exo-sf-core-agent, exo-code-server, exo-agent-builder, exo-help, harvester, New-Website

**Purpose:** Maps activities to cost buckets for financial allocation.

### Prompt 4: Revenue Model

**Question:** "How should we define revenue-generating work vs cost?"

**Last Answer (Feb 20, 2026):**
- **Revenue (Client)** = Client projects ONLY — generates income
- **Cost of Sales (Presales)** = Presales projects — investment in future revenue, not current revenue
- **Internal (Absorbed)** = Internal projects — acceptable operational cost, do NOT flag
- **Untagged (Discipline Gap)** = Activities with no project attribution — unaccountable spend, FLAG this

**Purpose:** Defines the 4-bucket cost model. Critical distinction: presales is NOT revenue.

---

## Cost/Revenue Model

### Cost Estimation

```
Estimated Period Cost = Active Days x 8 hours x Cost Rate per Hour
```

- **Active Days** = distinct calendar dates with >= 1 recorded activity
- **8 hours** = assumed full working day (proxy — Manazer tracks activities, not hours)
- **Cost Rate** = from contributor.cost_cents_per_hour

### Cost Buckets

| Bucket | Definition | Financial Treatment |
|--------|-----------|-------------------|
| **Client (Revenue)** | Work on client projects | Generates income — pays for itself |
| **Presales (Cost of Sales)** | Work on presales/starter-pack projects | Investment in pipeline — justified only if it converts |
| **Internal (Absorbed)** | Work on internal tooling | Operational cost — acceptable if intentional |
| **Untagged (Discipline Gap)** | Activities not mapped to any classified project | Unaccountable spend — must be flagged |

### Allocation Method

For each contributor:
1. Get ALL project allocations with activity counts
2. Classify each project into the 4 buckets
3. Prorate period cost by activity proportion:

```
Bucket Cost = (Bucket Activities / Total Activities) x Period Cost
```

- Activities with nil project_id → Untagged bucket
- Activities on unclassified projects → present to user or flag as Unaccounted

---

## Metrics

### Tier 1: Aggregate Cost Metrics

| Metric | Calculation | What It Measures |
|--------|------------|-----------------|
| Total Period Spend | Sum of all Period Costs | Total contractor investment |
| Revenue $ | Sum of Client bucket costs | How much went to income-generating work |
| Revenue % | Revenue $ / Total Period Spend | Revenue efficiency of the contractor pool |
| Cost of Sales $ | Sum of Presales bucket costs | Pipeline investment |
| Internal $ | Sum of Internal bucket costs | Operational overhead from contractors |
| Unaccounted $ | Sum of Untagged bucket costs | Discipline gap — money with no attribution |
| Annualized Unaccounted | Unaccounted $ x (260 / Business Days in Period) | Annual cost of tagging failure |

### Tier 2: Revenue Utilization (per contributor)

| Metric | Calculation | What It Measures |
|--------|------------|-----------------|
| Revenue Utilization Rate | Client Activities / Total Activities | % of work that generates revenue |
| Effective Hourly Rate | Nominal Rate / Revenue Utilization Rate | True cost per hour of client work |

- If Revenue Utilization = 0%, Effective Hourly Rate = N/A
- Rank contributors by Revenue Utilization descending

### Tier 3: Output Efficiency (per contributor)

| Metric | Calculation | What It Measures |
|--------|------------|-----------------|
| Cost/Commit | Period Cost / Commits | Code output efficiency |
| Cost/Ticket | Period Cost / Tickets Completed | Throughput efficiency |
| Cost/Revenue Activity | Period Cost / Client Activities | Revenue work efficiency |

- Uses TOTAL period cost (not just client cost) — the contractor was paid regardless
- If denominator = 0, show N/A

---

## Output Structure

```
# [Analysis Title] — [Period]

**Persona:** Jon Gray — CFO. Revenue Architect. Project Economist.
**Scope:** [From /jongray scope]
**Data Source:** Verified Fact-Finding Report ([confidence]%, [data points])
**Period:** [dates]
**Generated:** [timestamp]

---

## 1. Executive Summary
- Key metrics summary table (Active Contractors, Total Spend, Revenue %, Unaccounted %, Annualized Unaccounted)
- 1-2 sentence bottom line (Jon Gray voice — direct, financial, consequence-oriented)

## 2. Methodology & Definitions
- Table of term definitions with calculations
- Cost bucket definitions table with project mappings
- Brief note on the Activity ≠ Hours proxy

## 3. Contractor Roster — Ranked by Revenue Contribution
- All contractors ranked by Revenue Utilization (descending)
- Columns: Rank, Name, Period Cost, Total Activities, Active Days, Revenue Util., Effective $/hr
- Description before table explaining what it shows
- Totals row

## 4. Cost Allocation Summary
- Per-contractor breakdown across 4 buckets ($ and %)
- Description explaining how proration works
- Totals row with aggregate percentages

## 5. Revenue Efficiency Metrics
- Cost/Commit, Cost/Ticket, Cost/Revenue Activity per contractor
- Description explaining these use TOTAL period cost
- Note on why this matters

## 6. Untagged Cost Analysis
- 6a. Summary table (total spend, attributed %, unaccounted %, annualized)
- 6b. Per-contractor unaccounted breakdown (ranked by unaccounted $)
- Description explaining this is a tagging discipline measurement

## 7. Individual Deep Dives
- One subsection per contractor, each containing:
  - Activity Summary table
  - Project Allocation table (with classification column)
  - Cost to Company table (4 buckets)
  - Assessment paragraph (Jon Gray voice)
- Order: ranked by revenue contribution (highest first)

## 8. Action Items
- A. Contributors with zero project mapping (table with cost impact)
- B. Unclassified activity remainder (quantified)
- C. System/data issues (PR mapping, budget config, etc.)
- Organized by owner (Delivery Head, Tech Lead, etc.)

## 9. Data Caveats
- Only include caveats that actually apply
- Standard candidates: Activity≠Hours, project visibility limits, PR exclusions, cost vs billing rates, MCP availability
```

---

## Document Rules

1. **Every table gets a description.** 1-2 sentences before each table explaining what it shows and how numbers were calculated.
2. **Show the math.** Formulas in methodology. Explicit arithmetic where helpful.
3. **No hedging.** "This costs $X" not "This may cost around $X."
4. **Rank everything.** Tables sorted by the most important metric.
5. **Jon Gray voice in assessments.** Lead with the revenue question. Flag anomalies. State cost implications directly. Ask the management question.
6. **Present for review before saving.** Never write the analysis file without user approval.

---

## Assessment Guidelines (for Individual Deep Dives)

When writing the 2-3 sentence assessment for each contractor:

1. **Lead with revenue:** Is this person paying for themselves?
2. **Flag anomalies:** High commits but low tickets? Large unaccounted %? 100% internal for a contractor?
3. **State cost implications:** "The entire $X period cost produced zero revenue."
4. **Ask the management question:** "Should a contractor be spending X% on internal tooling?"
5. **Do NOT soften.** Facts and financial consequences. No euphemisms.
