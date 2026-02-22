# FTE Cost Register

**Source:** FTE COMP.xlsx (uploaded Feb 22, 2026)
**Conversion Rate:** 1 INR = 0.011 USD
**Hourly Calc:** USD Monthly / 176 (22 business days x 8 hrs)

---

## Active FTEs — Matched to Manazer

| Manazer Name | Comp Name | INR/yr | USD/mo | Actual $/hr | Billing $/hr | Margin $/hr | Margin % |
|---|---|---:|---:|---:|---:|---:|---:|
| Aniket | Aniket Hendre | 7,500,000 | $6,875 | $39.06 | $50 | $10.94 | 22% |
| Karthik | S Aravind Karthik | 7,000,000 | $6,417 | $36.46 | $80 | $43.54 | 54% |
| Saurav Shah | Saurav Shah | — | $6,000 | $34.09 | $50 | $15.91 | 32% |
| Sumanth | Sumanth Raj Urs | 5,400,000 | $4,950 | $28.13 | $50 | $21.88 | 44% |
| Suraj | Suraj Chandola | 4,100,000 | $3,758 | $21.35 | $50 | $28.65 | 57% |
| Jeetal Shah | Jeetal Shah | 4,000,000 | $3,667 | $20.83 | $80 | $59.17 | 74% |
| Harsh | Harsh Jain | 5,000,000 | $4,583 | $26.04 | $50 | $23.96 | 48% |
| Rajnish | Rajnish Dashora | 10,450,000 | $9,579 | $54.43 | $80 | $25.57 | 32% |
| Asarar Ahmed | Asarar Ahmed | 600,000 | $550 | $3.13 | $30 | $26.88 | 90% |
| Animesh | Animesh Das | 2,350,000 | $2,154 | $12.24 | $30 | $17.76 | 59% |
| Anirudh | Anirudh Vyas | 7,400,000 | $6,783 | $38.54 | $80 | $41.46 | 52% |
| Priyanshu Gaur | Priyanshu Gaur | 2,800,000 | $2,567 | $14.58 | $50 | $35.42 | 71% |
| Rishi | Rishi Ayyer | 9,000,000 | $8,250 | $46.88 | $80 | $33.13 | 41% |
| Srini | Srinivas Satyanarayana | 8,000,000 | $7,333 | $41.67 | $80 | $38.33 | 48% |
| Saurabh | Saurabh Nandedkar | 4,320,000 | $3,960 | $22.50 | $30 | $7.50 | 25% |
| Geetha | Geetha Doraiswamy | 7,000,000 | $6,417 | $36.46 | $80 | $43.54 | 54% |
| Akhil | Akhil Chandran | 2,600,000 | $2,383 | $13.54 | $50 | $36.46 | 73% |
| Isaac | Isaac Sanctis | 2,800,000 | $2,567 | $14.58 | $30 | $15.42 | 51% |
| Rohit T | Rohit T | 3,000,000 | $2,750 | $15.63 | $30 | $14.38 | 48% |
| Megha Bc | Megha B C | 1,800,000 | $1,650 | $9.38 | $30 | $20.63 | 69% |
| Jewel James | Jewel James | — | $9,000 | $51.14 | $80 | $28.86 | 36% |
| Paulomi | Paulomi Gudka | — | $20,834 | $118.38 | $120 | $1.62 | 1% |

**Total Active FTE Monthly Cost: $123,027**

---

## Special Cases

| Name | Status | Notes |
|---|---|---|
| **Sidu** | CEO | Not on comp sheet. Exclude from FTE cost analysis — CEO cost is separate. Still tracked for activity/project allocation. |
| **Kaathyayani** | Departed | Left the company. Remove from active FTE roster. |
| **Piyush Sinha** | Active — no cost data | Security compliance (100% internal). Not on comp sheet. **Need cost from Steve.** |

---

## On Comp Sheet — No Manazer Activity

| Name | USD/mo | Status | Action |
|---|---:|---|---|
| Prashant Mittal | $8,708 | **INVESTIGATE** | On PTO Feb 16–20 (sister's wedding). But zero activity Feb 1–15 AND all of Jan was ClickUp noise only (status changes, no code). Last GitHub PR: Dec 15, 2025. 4th highest paid FTE with no code output in 2+ months. |
| Akash K Mohan | $3,483 | **PARTIAL** | Has 2 Manazer contributor records (fragmented identity — see Data Hygiene section). Combined: 1 commit in Feb (Feb 13, exo-work-releases), ClickUp activity stopped Jan 20. Low output relative to cost. |
| Amul Badjatya | $5,500 | **ACTIVE** | Actually has 26 commits in Feb (all Boardroom, Feb 5–7). Not showing in original analysis because contributor email is local machine address (amulbadjatya@Amuls-MacBook-Pro.local) — was not matched. **Remove from concern list.** |
| Saurabh Kamboj | $2,108 | Not yet started | — |
| Shashwath | $2,200 | Not yet started | — |
| Ankita Kodoli | $2,933 | Not yet started | — |
| Noel Mathew | $2,750 | Not yet started | — |

**Revised findings:**
- **Amul ($5,500/mo)**: Actually active — 26 commits on Boardroom in Feb. Was missed due to local machine email in Manazer. **Cleared.**
- **Akash ($3,483/mo)**: Fragmented across 3 contributor identities. Only 1 commit in all of Feb. Low output but not zero. **Needs attention.**
- **Prashant ($8,708/mo)**: On leave Feb 16–20 but zero activity Feb 1–15 and no code since Dec 2025. **Biggest concern.**
- **Remaining concern: $12,191/mo ($146K annualized)** for Prashant + Akash with near-zero productive output.

---

## Manazer Data Hygiene — Action Required

These issues affect reporting accuracy. They need to be fixed in Manazer directly (contributor merge/email linking).

| Person | Issue | Accounts | Impact | Fix |
|---|---|---|---|---|
| **Akash K Mohan** | Fragmented identity | `Akash K Mohan98` (akash.k.mohan98@gmail.com, 339 acts) + `Akash Mohan` (akash.mohan@realfast.ai, 195 acts, cost_contributor=true) | 534 total activities split across 2 records. Dashboard/reports undercount his work on either view. | Merge into single contributor under realfast.ai email. |
| **Amul Badjatya** | Local machine email | `Amulbadjatya` (amulbadjatya@Amuls-MacBook-Pro.local, 26 acts) | Not matched to any known team member in reporting. Invisible in analysis. | Update primary email to corporate/real address. Link to proper identity. |
| **Prashant Mittal** | Split GitHub identity | `Prashant` (prashant@realfast.ai, 156 acts) + `Prashant3863` (prashant3863@users.noreply.github.com, 8 acts) | Minor — most activity on main account. But GitHub commits go to wrong record. | Merge GitHub noreply into main account. |

**Note:** Database is read-only via MCP. These fixes must be done through the Manazer UI or by the engineering team with write access.

---

*Register created Feb 22, 2026. Updated Feb 22 with investigation results and data hygiene findings. Source: FTE COMP.xlsx + CEO clarifications + Manazer MCP queries.*
