# Technical Discovery Playbook
## Enriched DTC + Meeting Agenda for the Delivery Team
**Factored.ai | S2D Framework — Phase 2 Artifact**  
**Version 1.0 | May 2026**

---

## How to Use This Document

This playbook is for the **Delivery Manager or Solution Architect** who will run the client discovery meeting after Gate 2 is passed. It has three parts:

1. **Pre-Meeting Prep** — what to review and prepare before the call.
2. **Meeting Agenda** — a structured 90-minute session with time blocks and facilitation notes.
3. **Enriched DTC** — the complete discovery template to fill during and after the meeting.

Fill the DTC as you go during the meeting. Do not wait until after — context fades fast.

The output of this playbook is a completed Enriched DTC that becomes the single source of truth for the engagement. Every team member who joins the project later should read this document before their first interaction with the client.

---

---

# PART 1 — PRE-MEETING PREPARATION
**Complete before the discovery meeting. Estimated time: 30–45 minutes.**

---

### 1.1 Review the Commercial DTC from Sales

Before the meeting, read the basic DTC filled by the Account Executive. Extract and note:

- [ ] What pain did Sales validate? Is it specific or vague?
- [ ] What was promised in terms of timeline and team?
- [ ] Who is the champion vs. who is the economic buyer?
- [ ] Any red flags or risks flagged by Sales?
- [ ] What was *not* promised but may be expected?

> **Signal to watch:** If the commercial DTC is thin or missing answers, flag it with the Account Executive before the meeting. Going into discovery without Sales context means you'll be re-covering ground the client already covered — that erodes trust immediately.

---

### 1.2 Research the Client

Spend 15 minutes on:

- [ ] Company website — understand their product, revenue model, and market position.
- [ ] LinkedIn — identify the people who will be in the meeting. Understand their roles and tenure.
- [ ] If the client is a SaaS company: look at their product. If they're B2B, understand who their customers are.
- [ ] Any public technical content (engineering blogs, GitHub orgs, job postings) — job postings reveal the tech stack and current team gaps better than any direct question.

> **Why job postings?** If a company is actively hiring for "Senior ML Engineer" and "Data Platform Lead," they likely have gaps in exactly the areas where Factored can deliver. This is insight you can use to frame your value.

---

### 1.3 Prepare Your Hypothesis

Before walking into a discovery meeting, form a hypothesis about what the client's real problem is. You won't know if it's right until you ask — but having a hypothesis makes your questions sharper.

Write it here before the meeting:

```
My hypothesis about the core technical problem:
___________________________________________________

My hypothesis about why they haven't solved it internally:
___________________________________________________

The thing I'm most uncertain about going in:
___________________________________________________
```

> **Backing principle:** The *Hypothesis-Driven Discovery* approach (rooted in Design Thinking and validated in McKinsey's problem-solving methodology) leads to 40% more focused discovery sessions than open-ended exploration (Liedtka, 2018).

---

### 1.4 Logistics Checklist

- [ ] Meeting invite sent with agenda attached (use the agenda in Part 2).
- [ ] Recording consent confirmed if recording (always ask).
- [ ] Collaboration tool ready (Miro / Notion / shared doc) if needed.
- [ ] Confirm who from Factored attends: Delivery Manager (required) + Solution Architect (if deal > $75K or technically complex).
- [ ] Account Executive briefed — they may attend the first 10 minutes to introduce but should not run the technical portion.

---

---

# PART 2 — MEETING AGENDA
**Duration: 90 minutes | Format: Video call or in-person**

---

## Agenda Template (shareable with the client)

> Send this to the client 24 hours before the meeting. Transparency about the agenda builds confidence.

---

**Subject:** Discovery Session Agenda — [Client Name] × Factored.ai

Hi [Name],

Looking forward to our session on [Date] at [Time]. Here's what we'll cover:

| # | Topic | Time |
|---|---|---|
| 1 | Introductions + session goals | 5 min |
| 2 | Business context — where you are today | 15 min |
| 3 | The problem in depth — root causes and impact | 20 min |
| 4 | The desired future state — what success looks like | 15 min |
| 5 | Technical landscape — current stack and constraints | 20 min |
| 6 | Team and process context | 10 min |
| 7 | Next steps | 5 min |

**What we'll ask you to bring:**
- Anyone on your team who is closest to the technical problem (engineer, architect, or data lead).
- Any existing documentation, architecture diagrams, or prior attempts at solving this (don't worry if they're rough).

The goal of this session is for our team to have enough context to propose an approach that is genuinely tailored to your situation — not a generic pitch.

---

## Facilitator Notes (internal — do not share)

---

### Block 1 — Introductions + Session Goals (5 min)

**You say:**
> "Thank you for making time. Our goal today is not to sell you anything — we've already agreed to work together. Our goal is to understand your situation deeply enough that when our team starts working, they start with full context, not assumptions. Everything you share will be captured in a document that travels with the engagement."

> "We'll ask some questions that might feel basic — please bear with us. The details that seem obvious to you are often the ones that matter most to us."

**Set the norm:** Let them know you'll take notes and share a summary within 24 hours.

---

### Block 2 — Business Context (15 min)

Goal: Understand the business problem before the technical problem. Technical solutions that ignore business context are expensive and often wrong.

**Questions to ask:**

1. *"Before we go technical — can you walk me through what your company does and who your customers are? I want to understand what this project means in the context of the business."*

2. *"What's happening in your business right now that made this project a priority today, as opposed to six months ago?"*

3. *"If this project delivers exactly what you hope — what changes in the business? Is it revenue, cost, risk, or something else?"*

4. *"Who internally is most affected by this problem today?"*

**Facilitation tip:** The answer to question 2 is often the most revealing. Urgency always has a cause — a new competitor, a board ask, a failed internal attempt, a compliance deadline. The cause shapes the entire engagement.

---

### Block 3 — The Problem in Depth (20 min)

Goal: Get to the root problem, not the symptom. Clients often describe what they want built, not what problem they need solved.

**Questions to ask:**

1. *"Describe what happens today, step by step, when [the problem occurs]. Walk me through it like I've never seen your system."*

2. *"What does this cost you — in time, money, or opportunity — when it happens? Can you quantify it?"*

3. *"Have you tried to solve this before? What happened?"*

4. *"What is the one thing that, if we got wrong, would make this project a failure?"*

5. *"What are you most worried about in terms of how this could go wrong?"*

**Facilitation tip:** Question 3 is critical. Prior attempts reveal constraints, political landmines, and what has already been ruled out. Never propose something a client has already tried and abandoned without understanding why it failed.

**If the client has trouble articulating the problem:**
Use the "5 Whys" technique (Toyota Production System / Lean methodology): ask "why" to each answer until you reach a root cause, not a symptom.

> Example: "Our dashboards are slow." → Why? "The queries take too long." → Why? "We don't have indexes on the main tables." → Why? "The data team doesn't have ownership of the warehouse schema." → *That's* the real problem.

---

### Block 4 — The Desired Future State (15 min)

Goal: Establish what "done" looks like with enough specificity to build success criteria. Vague goals produce vague delivery.

**Questions to ask:**

1. *"Imagine it's 90 days from now and this project has gone perfectly. What does a day in the life look like for your team?"*

2. *"How will you know — concretely — that this is working? What will you measure?"*

3. *"Is there a specific benchmark or standard you're trying to reach? (Latency, accuracy, uptime, user adoption rate, etc.)"*

4. *"Are there any constraints on the solution — things it must not do, or must integrate with, or must avoid?"*

5. *"What does a minimum viable success look like at 30 days vs. full success at 90 days?"*

**Facilitation tip:** If the client can't answer question 2 (how will you measure it), that is a risk. A project without measurable success criteria cannot be declared done — it will run forever or end in dispute. Surface this now, not at week 8.

---

### Block 5 — Technical Landscape (20 min)

Goal: Understand the technical environment the solution will live in. This section feeds directly into the Operational SOW and the Access & Tools Checklist.

**Questions to ask:**

**On current state:**
1. *"Walk me through your current tech stack — what are the main systems involved in this problem?"*
2. *"Where does your data live today? (Databases, warehouses, lakes, files, APIs)"*
3. *"What cloud provider(s) are you on? Are there constraints on adding new services?"*
4. *"What does your deployment pipeline look like? (CI/CD, environments, release cadence)"*

**On constraints:**
5. *"Are there security or compliance requirements we need to design around? (SOC2, HIPAA, GDPR, internal infosec policies)"*
6. *"Are there systems or services that are off-limits for us to touch or modify?"*
7. *"What are the scalability expectations? (Volume, users, data growth over 12 months)"*

**On team:**
8. *"Who on your side will be working with our team day-to-day? What's their technical background?"*
9. *"Is there any internal resistance or skepticism about this project we should know about?"*

**Facilitation tip:** Question 9 is the most politically sensitive — frame it as preparation, not concern: *"We've found that knowing about any internal dynamics early helps us calibrate our communication style and avoid stepping on toes."*

---

### Block 6 — Team and Process Context (10 min)

Goal: Understand how the client team works so Factored.ai can integrate smoothly, not disrupt.

**Questions to ask:**

1. *"How does your team currently manage work? (Jira, Linear, Notion, etc.)"*
2. *"What communication tools do you use? (Slack, Teams, email)"*
3. *"How often do you expect to sync with our team? (Daily standups, weekly reviews)"*
4. *"Who is the decision-maker for technical questions? For business/scope questions? Are they the same person?"*
5. *"Is there anything about how your team works that we should adapt to?"*

---

### Block 7 — Next Steps (5 min)

**Always close a discovery session with explicit next steps. Never end with "we'll be in touch."**

**Script:**
> "Thank you — this has been incredibly helpful. Here's what happens next: I'll send you a summary of what we discussed within 24 hours. Please review it and flag anything that's missing or misrepresented — it will become the foundation of our engagement plan. Our team will use it to prepare the detailed approach and timeline, which we'll share with you by [specific date]."

**Confirm:**
- [ ] Who receives the summary on their side?
- [ ] Date and format of next interaction (proposal review, technical deep-dive, etc.)?
- [ ] Any blockers to getting us access (procurement, legal, IT provisioning)?

---

---

# PART 3 — ENRICHED DTC
**Complete during and immediately after the discovery meeting.**  
**Owner:** Delivery Manager | **Reviewed by:** Solution Architect (if applicable)

---

## SECTION 0 — Header

```
CLIENT NAME: _____________________________________________
INDUSTRY / VERTICAL: _____________________________________
ACCOUNT EXECUTIVE: ______________________________________
DELIVERY MANAGER: _______________________________________
SOLUTION ARCHITECT: ______________________________________
DISCOVERY DATE: _________________________________________
CONTRACT VALUE (ARR): ____________________________________
CONTRACT START DATE: _____________________________________
DOCUMENT VERSION: _______________________________________
```

---

## SECTION 1 — Business Context

### 1.1 What does this company do?
*(In two sentences — product, market, revenue model)*

```
___________________________________________________________
___________________________________________________________
```

### 1.2 Why is this project a priority now?
*(What triggered the urgency — competitive pressure, board ask, compliance, failed prior attempt)*

```
___________________________________________________________
___________________________________________________________
```

### 1.3 What is the business impact of solving this?
*(Quantify if possible: revenue unlocked, cost reduced, risk mitigated, time saved)*

```
___________________________________________________________
___________________________________________________________
```

### 1.4 Who inside the client organization is most affected by this problem?
*(Name the teams or personas, not just job titles)*

```
___________________________________________________________
___________________________________________________________
```

---

## SECTION 2 — Problem Definition

### 2.1 What is the problem as the client describes it?
*(Their words, not your interpretation)*

```
___________________________________________________________
___________________________________________________________
```

### 2.2 What is the root problem?
*(After applying 5 Whys or your own analysis — this may differ from 2.1)*

```
___________________________________________________________
___________________________________________________________
```

### 2.3 What has been tried before?
*(Prior attempts, vendors, internal initiatives — and why they failed)*

```
___________________________________________________________
___________________________________________________________
```

### 2.4 What is the quantified cost of the problem today?
*(Time per week, revenue lost, error rate, manual hours, etc.)*

```
___________________________________________________________
___________________________________________________________
```

### 2.5 What is the single thing that would make this project a failure?
*(Their biggest fear)*

```
___________________________________________________________
___________________________________________________________
```

---

## SECTION 3 — Success Criteria

### 3.1 What does success look like at 30 days?
*(Minimum viable outcome — what must be true for the client to feel the project is on track)*

```
___________________________________________________________
___________________________________________________________
```

### 3.2 What does success look like at 90 days?
*(Full outcome — what the client will point to as the measure of success)*

```
___________________________________________________________
___________________________________________________________
```

### 3.3 How will success be measured?
*(Specific metrics, thresholds, KPIs — if they couldn't answer this, note it as a risk)*

| Metric | Current Baseline | Target | Measurement Method |
|---|---|---|---|
| | | | |
| | | | |
| | | | |

### 3.4 What is explicitly out of scope?
*(Things that came up in conversation that are NOT part of this engagement)*

```
___________________________________________________________
___________________________________________________________
```

---

## SECTION 4 — Technical Landscape

### 4.1 Current Tech Stack

| Layer | Technology / Tool | Notes |
|---|---|---|
| Frontend | | |
| Backend / API | | |
| Database(s) | | |
| Data Warehouse / Lake | | |
| ML / AI Platform | | |
| Cloud Provider | | |
| CI/CD Pipeline | | |
| Monitoring / Observability | | |
| Authentication / Identity | | |
| Other critical systems | | |

### 4.2 Data Landscape
*(Especially relevant for AI/ML and data engineering engagements)*

```
Where does the relevant data live?
___________________________________________________________

What is the data volume / velocity?
___________________________________________________________

Is the data labeled / structured / clean? (Be honest here)
___________________________________________________________

Who owns the data pipeline today?
___________________________________________________________

Are there known data quality issues?
___________________________________________________________
```

### 4.3 Compliance and Security Requirements

```
Regulatory frameworks in scope: (HIPAA / SOC2 / GDPR / PCI / internal policy)
___________________________________________________________

Data residency requirements:
___________________________________________________________

Access control constraints (can we use cloud services freely?):
___________________________________________________________

Penetration testing or security review required before go-live?
___________________________________________________________
```

### 4.4 Systems Off-Limits
*(List any systems Factored cannot touch, modify, or access)*

```
___________________________________________________________
___________________________________________________________
```

### 4.5 Scalability Expectations

```
Current load (users / records / requests per day):
___________________________________________________________

Expected load in 12 months:
___________________________________________________________

Peak load scenarios (if any):
___________________________________________________________
```

### 4.6 Integration Points
*(List every external system this solution must connect to)*

| System | Type | Owner | Complexity Estimate |
|---|---|---|---|
| | API / DB / File / Event | | Low / Med / High |
| | API / DB / File / Event | | Low / Med / High |
| | API / DB / File / Event | | Low / Med / High |

---

## SECTION 5 — Stakeholder Map

### 5.1 Client-Side Stakeholders

| Name | Role | Type | Notes |
|---|---|---|---|
| | | Champion | Advocates for the project internally |
| | | Economic Buyer | Signs the invoices, measures ROI |
| | | Technical Lead | Day-to-day technical contact |
| | | End User | Uses what we build |
| | | Blocker / Skeptic | May resist the project |
| | | Influencer | Opinion matters but not a decision-maker |

### 5.2 Key Relationships to Manage

```
Who will Factored communicate with daily?
___________________________________________________________

Who needs to be kept informed but not consulted for decisions?
___________________________________________________________

Who should NOT be bypassed on technical decisions?
___________________________________________________________

Is there any tension between stakeholders we should know about?
___________________________________________________________
```

### 5.3 Client Decision-Making Model

```
How are technical decisions made? (One person / committee / consensus)
___________________________________________________________

How are scope changes approved? (Who needs to sign off)
___________________________________________________________

What is the typical response time for approvals?
___________________________________________________________
```

---

## SECTION 6 — Working Model

### 6.1 Communication

```
Primary channel: (Slack / Teams / Email)          ___________
Meeting cadence agreed: (Daily / Weekly / Biweekly) ___________
Status report format expected: (Written / Verbal / Dashboard) ___________
Time zone of primary contacts:                    ___________
Core hours overlap with Factored team:            ___________
```

### 6.2 Project Management

```
Client's PM tool: ___________________________________________
Will Factored manage the board or will client? ________________
Sprint cadence (if agile): __________________________________
Demo cadence: ______________________________________________
```

### 6.3 Definition of Done (agreed with client)

```
What does "task complete" mean to them?
(Unit tested? Reviewed? Deployed to staging? In production?)
___________________________________________________________

Who does acceptance testing on their side?
___________________________________________________________

What is the approval process for each deliverable?
___________________________________________________________
```

---

## SECTION 7 — Risks and Flags

Rate each risk: 🔴 High / 🟡 Medium / 🟢 Low

| # | Risk | Level | Mitigation |
|---|---|---|---|
| 1 | Scope creep (success criteria not measurable) | | |
| 2 | Data quality (data is not ready for what was sold) | | |
| 3 | Access delays (provisioning may block Day 1) | | |
| 4 | Key-man risk (one client contact knows everything) | | |
| 5 | Political resistance (internal skeptic not identified) | | |
| 6 | Timeline pressure (deadline was set before scope was defined) | | |
| 7 | Tech debt (existing system harder to integrate than expected) | | |
| 8 | [Custom risk from this engagement] | | |

### 7.1 Risk Summary

```
The single biggest risk to this engagement right now:
___________________________________________________________

What must happen in the first 2 weeks to de-risk this:
___________________________________________________________
```

---

## SECTION 8 — Factored.ai Team Recommendation

*To be completed by the Delivery Manager after the meeting.*

### 8.1 Recommended Team Composition

| Role | Seniority | Dedication | Rationale |
|---|---|---|---|
| | | Full / Part | |
| | | Full / Part | |
| | | Full / Part | |

### 8.2 Technical Approach (initial hypothesis)

```
Recommended architectural approach (1 paragraph):
___________________________________________________________
___________________________________________________________

Technologies / frameworks recommended:
___________________________________________________________

Alternatives considered and rejected (with reasons):
___________________________________________________________
```

### 8.3 Delivery Risk Assessment

```
Confidence level in current scope: (Low / Medium / High)
___________________________________________________________

Items that need a spike or PoC before committing to an approach:
___________________________________________________________

What must be true for the 30-day milestone to be achievable:
___________________________________________________________
```

---

## SECTION 9 — Document Control

```
Completed by: ____________________________________________
Date completed: __________________________________________
Reviewed by (Delivery Lead): _____________________________
Date reviewed: ___________________________________________
Shared with Account Executive: (Yes / No) ________________
Stored in: (location in Drive / Notion / CRM) ___________
```

---

## SECTION 10 — Post-Meeting Checklist

Complete within 24 hours of the discovery session:

- [ ] Summary email sent to client (using Block 7 close from the meeting agenda)
- [ ] DTC Sections 1–8 filled completely
- [ ] Any open questions listed and assigned to a follow-up owner
- [ ] Access & Tools Checklist sent to client IT contact
- [ ] Operational SOW drafted based on Section 3 (Success Criteria) and Section 4 (Technical Landscape)
- [ ] Gate 2 sign-off meeting scheduled with Delivery Lead
- [ ] Risk flags communicated to Account Executive

---

## Open Questions Log

*Use this to track anything that came up but wasn't answered during the meeting.*

| # | Question | Owner to Answer | Due Date | Status |
|---|---|---|---|---|
| 1 | | | | Open |
| 2 | | | | Open |
| 3 | | | | Open |

---

---

## Sources Consulted

- AXELOS. (2019). *ITIL Foundation: ITIL 4 Edition*. TSO. — Knowledge transfer standards, Service Transition, discovery documentation practices.
- Project Management Institute. (2021). *PMBOK Guide — 7th Edition*. PMI. — Stakeholder identification, requirements elicitation, scope management.
- Liedtka, J. (2018). Why Design Thinking Works. *Harvard Business Review*, Sept–Oct 2018. — Hypothesis-driven discovery methodology; 40% more focused sessions statistic.
- Ohno, T. (1988). *Toyota Production System: Beyond Large-Scale Production*. Productivity Press. — The 5 Whys root-cause analysis technique.
- Womack, J. P., & Jones, D. T. (1996). *Lean Thinking*. Simon & Schuster. — Waste in handoffs, value stream thinking applied to service delivery.
- Maister, D. H., Green, C. H., & Galford, R. M. (2000). *The Trusted Advisor*. Free Press. — Trust Equation; discovery as a trust-building mechanism.
- Patton, J. (2014). *User Story Mapping*. O'Reilly Media. — Definition of Done, outcome-based vs. output-based success criteria.
- SAP SE. (2021). *SAP Activate Methodology: Fit-Gap Analysis and Discovery Phase Guide*. SAP. — Structured discovery session design for complex technical engagements.
- S2D_Framework.md — Factored.ai Sales-to-Delivery Framework v1.0 (internal). — Gates, RACI, artifact definitions that this playbook operationalizes.
- theory.txt — Internal notes on Sales-to-Delivery Handoff techniques. — Original source material for the Factored.ai S2D system.
