# PR #192 — Call Guide

**Call with:** Geetha
**Context:** Follow-up on PR #192 review comments and replies
**Tone:** Direct, constructive, outcome-focused. Not punitive — but clear that the bar needs to move.

---

## Call Flow

1. **Open:** "I want to talk through the PR 192 review and your responses. I appreciate the engagement — the action items show you've understood the issues. But there are three things I need to address."

2. **Point 1** (~5 min): The report needs to surface the diagnosis, not just the data. Future reports must include root cause and recommendation.

3. **Point 2** (~10 min): The open items — who approved the scope (walk through the estimation timeline), the January scoping question, the confidence scoring correction.

4. **Point 3** (~5 min): Request the RCA. Define the three questions. Set a deadline for delivery.

5. **Close:** "The engagement is recoverable. But only if we have clear controls in place before March starts. The RCA is how we get there."

---

## Point 1: The Report Didn't Surface the Problem

**Say this:**

- "The report told me 204.5% utilization. What it didn't tell me was that January's 51.97h overrun carried forward into February, that the team may be operating against a 40h mental model instead of the contracted 20h, that three design defects from the build phase consumed 2.5 months of MS budget, or that Manazer has no budget configured so no alert could ever fire."

- "Those aren't observations I should be making in a PR review. Those are observations the delivery manager should be surfacing in the report before it reaches me."

- "I appreciate the responses to each comment — the action items are the right framework. But those action items prove the point: the report needed to contain the analysis, not just the numbers."

**If she pushes back, reference these — none were in the report:**
- 55h of estimates accepted against a 20h budget
- January carry-forward making February negative before it started
- No budget configured in Manazer
- The 20h vs 40h discrepancy across internal documents
- The estimation problem ticket (`86d1u0zax`) sitting in backlog since Feb 2

**Land this point:** Future reports must include diagnosis and recommendation, not just data. A report that surfaces a 204.5% overrun without explaining the root cause or proposing corrective action is incomplete.

---

## Point 2: Outstanding Questions

### 2a — Who approved the scope?

**Say this:**

- "Walk me through the estimation process for this engagement. When a ticket is created and an estimate is set — who approves that? Is there a step where someone checks the cumulative commitment against the 20h ceiling?"

**Then walk through the timeline:**

| Date | Ticket Added | Estimate | Cumulative | vs 20h Budget |
|------|-------------|:--------:|:----------:|:-------------:|
| Jan 8 | Lead Owner bug | 6h | 6h | 30% |
| Jan 8 | Report Discrepancies | 6h | 12h | 60% |
| Jan 9 | LE Staff Permissions | 1.5h | 13.5h | 68% |
| Jan 19 | Chatbot "transferred" | 6h | 19.5h | 98% |
| **Jan 22** | **Bot context understanding** | **6h** | **25.5h** | **128%** — over |
| **Jan 22** | **Bot response latency (spike)** | **24h** | **49.5h** | **248%** |
| Jan 29 | Bi-weekly call | 6h | 55.5h | 278% |

**Say this:**

- "By January 19, the team was at 98% of the monthly budget in estimates. On January 22, two tickets were added in the same day pushing it to 248%. The spike alone was 24h — 120% of the monthly budget on one ticket. Did anyone flag that?"

- "Was it because nobody was tracking, or because the team thought the budget was 40h?"

- "I'm not asking this to assign blame. I'm asking because the RCA needs to answer whether the estimation process broke down, or whether there was no estimation process to begin with. Those require different fixes."

**Three things you need to hear:**
1. A name — who owns estimation approval on this engagement
2. A clear answer — was there a review step, or were estimates committed directly
3. Whether the cumulative position was being tracked against the budget at any point during January

**Additional context if needed:**
- ClickUp doesn't log who set the `time_estimate` field
- Ticket creators: Shantanu (6), Geetha (3), Bharat (2), Ganesh (1)
- Creating a ticket isn't the same as approving its estimate
- Manazer had no budget configured, the team's own report states "40h" — if nobody knew the real ceiling, scope control was structurally impossible

---

### 2b — The January hours scoping

**Say this:**

- "The January section you added scopes to Bharat, Ganesh, and Shantanu only. Why were Geetha and Sidu excluded? If they worked on these tickets, those hours still count against the 20h budget — and they're higher-cost resources."

**Our numbers vs hers on the same three tickets:**
- Our analysis (all contributors): **50.65h**
- Her Section 1a (three contributors only): **43.10h**
- Gap: **7.55h**

**If she says they didn't work on those tickets:** "Then the numbers should match ours. Can we reconcile?"

**If she says they're excluded because they're not 'delivery':** "Hours are hours against the budget ceiling. The contract doesn't distinguish."

**Keep this brief.** The main point is that the RCA should include all contributor hours, not a subset.

---

### 2c — kaiwren's contradiction on confidence scoring

**Say this:**

- "kaiwren has flagged that the explanation of 47% confidence isn't accurate. If the person who built the system says it's wrong, we need to understand what 47% actually means and whether the hours data for this engagement can be relied on."

**Don't belabor this one.** Mention it once, establish the explanation needs correction, move on. The point connects to the broader data trust issue from Comment 2 (four sources, four different actuals).

---

## Point 3: Request a Formal RCA

**Say this:**

- "I'd like you to put together a formal RCA for the SIM Managed Services overrun. Not a long document — a one-pager. But it needs to answer three questions clearly."

### Question 1: What went wrong?

- How did 70.50h of estimates get accepted against a 40h total budget without escalation?
- Why was there no budget configured in Manazer for 7 weeks?
- Why was the January overrun (260% of monthly budget) not flagged before February started?
- How did the 20h vs 40h discrepancy exist in internal documents?
- Why are three design defects from the build phase being absorbed by the MS budget?

### Question 2: What specific changes are being made?

- Each change needs an **owner** and a **completion date**
- The 6 action items from her Comment 8 reply are a starting point — but they need names and dates
- Examples: "Budget configured in Manazer by [name] by [date]." "Weekly variance review owned by [name] starting [date]." "Estimation gate: no ticket exceeding monthly budget without [name]'s sign-off, effective [date]."

### Question 3: How will those changes be audited?

- Action items without verification become intentions, not controls
- "How will we know in April that March's controls are actually working? What's the cadence? Who reviews? What's the escalation if the budget is trending over?"

**Close with:**

- "I'm not looking for a 20-page document. I'm looking for a one-pager that I can hold the team accountable against in March. Root cause, corrective actions with owners and dates, and a verification mechanism."

- Set a deadline — suggest end of this week or early next week, given March 1 is when controls need to be live.

---

*Prepared through Jon Gray CFO persona. All data points traceable to PR #192 comment thread and Manazer project f7ec5128-ab9a-40c0-99b5-ad1a9d453e71.*
