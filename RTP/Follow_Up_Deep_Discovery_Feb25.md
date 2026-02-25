# Deep Discovery Session II — Madhur Makkar, RTP Global
## February 25, 2026 | 1:00–2:30 PM

---

# WHAT WE KNOW (From the Feb 24 Call)

## Governing Question

> What information do we need from today's session to build a Conversational CRM prototype that eliminates Affinity update friction for Madhur's team — and deliver it in one week?

## What Madhur Told Us — And What It Means For The Build

| What He Said | What He Meant | Build Implication |
|---|---|---|
| "The most redundant part is moving stuff for my CRM" | CRM updation is cognitive friction — not hard, just *unrewarding* | Frame as "the CRM updates itself." Not "faster data entry." |
| "Rahul spends an hour a day on CRM" | **5 hrs/week of analyst capacity** lost to non-alpha work (~260 hrs/year) | Build for Madhur first — he validates, then decides when to roll it to Rahul and the team. |
| "Things get missed and hence they take a lot of time" | The real pain is **invisible failure** — they don't know what they don't know | The tool must make updates frictionless enough that people actually do them. |
| "The data is going to be deeply flawed if you go there" | CRM data is unreliable today. He's already discounted it. | Don't build on existing data quality. Build the layer that prevents future decay. |
| "Accuracy, speed, and cost — in that order" | He will reject anything that hallucinates or creates false entries | **Human confirms every write.** No autonomous updates to Affinity. Non-negotiable. |
| "I don't care about [the intern sourcing workflow]" | Sourcing is solved. Don't touch it. | Stay away. Even if we see opportunities there. |
| "Actioning happening via messaging on Slack" | His mental model is **conversational** — Slack/WhatsApp as the command interface | Build the interaction layer where his team already lives, not in a new app. |
| "Every year we take a week to correct past wrong mistakes" | Annual remediation = ~40 person-hours | Cost-of-inaction anchor. Use it when framing value. |
| "I have a recommended time per step, which will also evolve after we get that data" | He has SLA intuitions, not defined SLAs. No baseline data exists. | SLA enforcement is Phase 2 — only possible once clean data is flowing from the tool we build now. |

## What's Already Confirmed

- **CRM**: Affinity
- **Existing automation**: Granola -> Zapier -> Affinity (call notes only)
- **Chrome extension**: Exists for sourcing, low value, nobody uses it
- **Claude Code**: Installed on their machines. No IT blocker for local tools.
- **IT/compliance for hosted services**: Madhur to confirm (action item from last call)
- **Team**: Madhur, Rahul (analyst), intern, 2 others (~5 total users)
- **Preferred channels**: Slack and WhatsApp (email reminders get ignored)

## The POC We're Building

**Conversational CRM — Affinity MCP + Claude Code**

Team members update Affinity through natural language. Paste a call note, dictate a summary, type a quick update — the agent parses it, identifies the deal, proposes field updates and status changes, writes to Affinity after human confirmation.

**Why this, and only this, right now:**
- Directly attacks the #1 pain (CRM updates get skipped)
- Recovers 625–1,250 hours/year across the team
- Builds the data foundation that makes everything else possible (SLA measurement, pipeline visibility, nudge bots)
- Can be built in 1 week, tested with Madhur first — he decides when to roll out to the team
- Runs locally — no hosting, no compliance hurdles

---

# HOW TO RUN TODAY'S CALL

## Pre-Call Gating Item

**Verify Affinity API capability before the call.**

Affinity's API must support: reading deal records, reading/writing field values, reading/writing notes, and reading list/stage metadata. If the API doesn't support write operations on the fields Madhur uses, the entire POC architecture changes.

**Action**: Steve or Aakash spends 30 minutes before 1:00 PM reviewing the [Affinity API docs](https://api-docs.affinity.co/). Confirm read/write on deals, fields, notes, and stages. If write access is restricted, prepare a fallback: the agent drafts updates and the user copy-pastes into Affinity (still saves 70%+ of the friction, just not the last mile).

**If this hasn't been done before the call**: Ask Madhur during Phase 4 whether his Affinity plan includes full API access, and whether he's generated API keys before.

---

## Session Objective

Exit the 90 minutes with a **complete build spec**:
1. Every Affinity field, deal stage, and transition rule documented
2. Madhur's CRM update workflow mapped end-to-end (his process first — he's the one on the call)
3. API credentials and sample data secured
4. A date for Madhur to test the prototype agreed

**Minimum Viable Proof — What "working in 1 week" means:**
> By day 7, Madhur can paste a Granola call note into the agent, see the correct deal identified with proposed field updates and status change, confirm, and have Affinity updated — for at least 3 real deal records across different pipeline stages.

If we leave without the four items above, we can't start building tomorrow. If we can't define the minimum viable proof, we don't know when we're done.

---

## Phase 1 — Set the Frame (8 min) [1:00–1:08]

**Steve opens. Three sentences, then hand him the pen.**

> "Madhur, we analysed the full conversation from yesterday. The clearest path to giving your team time back is a tool that lets them update Affinity by talking to it — paste notes, type a summary, confirm the update, done. No forms, no clicking through the CRM.
>
> Today we need to go deep on exactly how you use Affinity — every field, every stage, every data source — so we can build this right and put something in your hands within a week. Once you're happy with it, you decide when the team gets it.
>
> Last time you showed us the deal flow on screen and that was incredibly useful — would it make sense to do the same thing and walk through a live deal record so we can see exactly what the agent needs to handle?"

**Why this works:**
- No recap of what he already told us — he was there
- Immediately signals we're building, not presenting
- Asks him to share screen — puts him in driver's seat
- "In your hands" — he's the first user, not a bystander watching his team use it
- "You decide when the team gets it" — respects his authority, no assumptions about rollout

---

## Phase 2 — Map the Affinity Workflow (40 min) [1:08–1:48]

This is the core of the session. We're extracting a technical spec by having Madhur walk us through his own system. Run it like a consultant-led process mapping exercise: he shows, we capture, we clarify.

### 2A — Deal Stages & State Machine (15 min)

**Open with**: "Show me the full deal lifecycle — every stage from when a company first enters Affinity to when it reaches a final state."

**Capture this — on screen, not from memory:**

| Stage Name (exact) | What Triggers Entry | Who Owns | What Gets Updated | What Triggers Exit | End State? |
|---|---|---|---|---|---|
| | | | | | |

**Probe questions** (use only if he doesn't cover it naturally):
- "Are there any stages that get skipped in practice? Where do people jump ahead?"
- "You mentioned 'Aware, No Interest' as a closed state. What are all the end states?"
- "When someone moves a deal from 'Reached Out' to 'Connected' — what data gets entered at that moment?"
- "Are there branching paths? Can a deal go backward?"

**What we're building**: The state machine. This is the backbone of the agent — it needs to know every valid transition to propose the right next status.

### 2B — Field-Level Anatomy of a Deal Record (10 min)

**Open with**: "Open a real deal record — one that's been well-maintained. I want to see every field."

**Capture:**
- Every field name (exactly as it appears in Affinity)
- Field type (text, dropdown, date, number, multi-select)
- Which fields are required vs. optional
- Which fields are auto-populated (e.g., from Zapier/Granola) vs. manually entered
- What a "good" note entry looks like vs. a lazy one

**Key question**: "If the agent were going to write a perfect update to this record, what would it need to fill in? Walk me through the ideal."

**What we're building**: The field map. The agent needs to know what to write and where.

### 2C — The Daily CRM Update Workflow (10 min)

**Open with**: "Walk me through what a CRM update session looks like for you. You've had a few calls, some LinkedIn conversations, a WhatsApp thread — how does that get into Affinity today?"

**Capture the flow:**

```
Step 1: Opens ___
Step 2: Finds the deal by ___
Step 3: Information comes from ___ (Granola / LinkedIn / WhatsApp / email / Slack / memory)
Step 4: Updates fields: ___
Step 5: Changes status to: ___
Step 6: Adds notes in this format: ___
Step 7: Repeats for ___ deals per session
Step 8: Total time: ___
```

**Probe questions**:
- "What's the most annoying part of this flow?"
- "How many deals do you typically touch in one update session?"
- "Do you batch it (all at end of day) or update as you go?"
- "When updates get skipped, what's the usual reason — for you and for the team?"
- "When an update gets skipped — is it because the process is annoying, or because the interaction didn't feel important enough to log? Or both?" *(This separates friction from forgetting — they require different solutions. Friction = better UX. Forgetting = nudges and triggers.)*

**What we're building**: The user journey. Map Madhur's process first — he's the person in the room. Ask how the team's process differs where relevant, but ground it in his experience.

### 2D — Data Sources & Integration Points (5 min)

**Open with**: "You mentioned Granola feeds into Affinity via Zapier. What other data sources does the team pull from when updating deals?"

**Capture:**

| Data Source | What Data | How It Gets to Affinity Today | Automation Exists? |
|---|---|---|---|
| Granola | Call notes | Zapier → Affinity notes | Yes |
| LinkedIn / SalesNav | Founder profiles, connections | Manual | No |
| WhatsApp | Founder conversations, deal context | Manual (copy-paste or from memory) | No |
| Email | Founder replies, intros | Manual | No |
| Slack | Internal deal discussion | Manual | No |
| Other? | | | |

**What we're building**: The input map. The agent needs to handle whatever format the team throws at it — Granola transcripts, LinkedIn copy-pastes, quick WhatsApp summaries.

---

## Phase 3 — Concept Validation (15 min) [1:48–2:03]

**Purpose**: Walk Madhur through how the tool will work. Not a demo — a walkthrough. Get his reaction and corrections before we build.

**Steve or Aakash walks through 3 scenarios:**

**Scenario 1 — Post-meeting update**
> "You just finished a founder call. Granola generates the notes. Today you open Affinity, find the deal, manually update the fields. With the tool: you paste the Granola notes, the agent identifies the deal, proposes the field updates and status change, you confirm. 30 seconds instead of 10 minutes."

**Scenario 2 — Batch end-of-day**
> "You've had 5 deal interactions today — calls, LinkedIn messages, a WhatsApp thread. Instead of opening each deal in Affinity, you type a quick summary: 'FinStack to diligence, DataMesh went cold, LogiTech wants follow-up next week.' The agent proposes all the updates, you confirm each one."

**Scenario 3 — Quick context pull before a call**
> "You have a founder call in 5 minutes. You ask: 'What's the latest on FinStack?' Agent pulls the Affinity record — current status, last note, owner, last activity date. No clicking through the CRM."

**After each scenario, ask exactly one question:**
> "What would you change about that?"

**Listen for**: Missing fields, wrong assumptions about the workflow, edge cases, objections. His corrections *are* the spec.

---

## Phase 4 — Secure Access & Lock the Timeline (12 min) [2:03–2:15]

**Transition**: "We've got what we need to build this. Now I need a few things from you to start tomorrow."

| What We Need | Why | Ask For It Like This |
|---|---|---|
| **Affinity API key** (read + write) | Core integration — we can't build without it | "Can you generate an API key for us now, or who on your side handles that?" |
| **Field schema export** (or 5 min of screen time) | Exact field names, types, dropdowns | "Can you export the field list, or can we screenshot it from settings?" |
| **3-5 sample deal records** | Test data for development | "Point me to 3 deals at different stages — one new, one mid-pipeline, one closed." |
| **30 min with Madhur in week 2** | Test the prototype with the actual user | "When can we get 30 minutes with you to walk through the working tool?" |
| **IT/compliance confirmation** | Carried from last call — for future hosted services | "Any update on the IT check? Not blocking us for now since this runs locally." |

**Do not leave the call without the API key or a confirmed date to receive it.** Everything else can follow within 48 hours.

---

## Phase 5 — Commit & Close (5 min) [2:15–2:20]

**Steve closes with commitments — specific, named, dated:**

> "Here's what happens next:
>
> **Us**: We build the Conversational CRM prototype this week. Affinity MCP connected, your deal stages and fields mapped, natural language updates with confirmation before every write.
>
> **You**: API key by [date], and 30 minutes on [date] so we can walk you through the working tool.
>
> **Check-in**: [specific date, 1 week out] — you test it on your own workflow. If it works for you, you decide when and how to roll it out to Rahul and the team.
>
> After that's running and data is flowing cleanly, we'll have the baseline to build what you described — SLA tracking, Slack nudges, pipeline health summaries. That's the next conversation."

**Leave 10 minutes of buffer** (2:20–2:30) for overflow or questions. Don't fill it proactively.

---

# WHAT WE WALK OUT WITH

This is the post-call deliverable. If any of these are missing, the session didn't achieve its objective.

| Deliverable | Status |
|---|---|
| Complete deal stage map (every stage, owner, trigger, fields) | [ ] Captured |
| Affinity field schema (field names, types, required/optional) | [ ] Captured |
| Madhur's CRM update workflow (step-by-step, sources, time per step) | [ ] Captured |
| How team workflow differs from Madhur's (where relevant) | [ ] Captured |
| Data source → Affinity integration map | [ ] Captured |
| Affinity API key (or confirmed delivery date) | [ ] Secured |
| 3-5 sample deal records for testing | [ ] Identified |
| Madhur prototype walkthrough date (week 2) | [ ] Booked |
| IT/compliance status update | [ ] Confirmed |
| Madhur's corrections to the 3 scenarios | [ ] Documented |

---

# WHAT NOT TO DO

| Don't | Why | Instead |
|---|---|---|
| Recap the last call for 10 minutes | He was there. It wastes time and signals you have nothing new. | Three sentences, then "pull up Affinity." |
| Pitch a slide deck or roadmap visual | You're here to extract, not present. Slides signal pitch mode. | Run it as a working session. He shows, you capture. |
| Discuss sourcing automation | He explicitly killed it. Bringing it back signals you weren't listening. | Don't touch it. |
| Promise SLA enforcement today | No baseline data exists. You can't enforce what hasn't been measured. | "That's Phase 2 — once clean data flows from this tool." |
| Auto-write to Affinity without confirmation | He said accuracy > speed. This is a core design principle. | Human-in-the-loop on every write. Always. |
| Leave without API credentials | You can't start building. The session was wasted. | Push for it. Offer to wait while he generates it. |
| Scope creep into diligence, IC memos, portfolio monitoring | Phase 3 on the trust ladder. You haven't earned it. | "We'll earn the right to touch that. Let's nail CRM first." |

---

# VALUE ANCHORS (Use During the Call)

Frame value in **deals and decisions**, not hours saved. Madhur is a GP — he thinks in portfolio outcomes, not timesheets.

| What Changes | Without the Tool | With the Tool | Why It Matters |
|---|---|---|---|
| **Deal record completeness** | Updates skipped → stale pipeline | Every interaction logged at point of contact | Madhur sees the real pipeline, not last month's pipeline |
| **Decision quality before IC** | "Don't know what we missed" — Madhur, Feb 24 | Full interaction history on every deal | IC decisions made on complete data, not memory |
| **Time-to-update** | ~1 hr/day (Rahul), unknown for others | ~10 min/day — paste and confirm | Friction removed = updates actually happen |
| **Annual data remediation** | 1 week, 5 people (~40 person-hours) | Eliminated — data stays clean | Never again "correct past wrong mistakes" |
| **Foundation for Phase 2** | No baseline data for SLAs or nudges | Clean data flowing → SLA measurement becomes possible | This tool is the prerequisite for everything else Madhur described |
