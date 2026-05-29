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
| 2 | Business context — where you are today | 10 min |
| 3 | The problem and the desired outcome | 15 min |
| 4 | Data landscape — ingestion to delivery | 40 min |
| 5 | Developer workflow and operations | 10 min |
| 6 | Open topics + pain point | 5 min |
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

### Block 3 — The Problem and the Desired Outcome (15 min)

Goal: Get to the root problem and a concrete definition of success before touching anything technical. Clients often describe what they want built, not what problem they need solved.

**Questions to ask:**

1. *"Describe what happens today when [the problem occurs]. Walk me through it like I've never seen your system."*
2. *"What does this cost you — in time, money, or opportunity? Can you quantify it?"*
3. *"Have you tried to solve this before? What happened?"*
4. *"Imagine it's 90 days from now and this worked perfectly. What changed in your team's day-to-day?"*
5. *"How will you know concretely that it's working? What will you measure?"*
6. *"What is the one thing that, if we got wrong, would make this project a failure?"*

**Facilitation tip:** If the client cannot answer question 5 (how will you measure it), flag it as a risk immediately. A project without measurable success criteria cannot be declared done — it will run forever or end in dispute.

**If the client has trouble articulating the root problem:**
Use the "5 Whys" technique (Toyota Production System / Lean): ask "why" to each answer until you reach a root cause, not a symptom.

> Example: "Our dashboards are slow." → Why? "The queries take too long." → Why? "We don't have indexes." → Why? "The data team doesn't own the warehouse schema." → *That's* the real problem.

---

### Block 4 — Data Landscape: Ingestion → Modeling → Processing → Delivery (40 min)

Goal: Map the client's full data value chain. This is the core technical scoping block. Work through each layer in order — they build on each other.

> **Framing line to open this block:**
> *"I want to understand how data flows through your organization — from where it comes in, to how it's structured, processed, and finally used. Let's go layer by layer."*

---

#### 4a — Ingestion (8 min)

*"Let's start at the beginning — where does your data come from?"*

1. *"What are all the sources you're ingesting from? (APIs, databases, files, event streams, SaaS tools, IoT sensors, etc.)"*
2. *"What volume of data are you ingesting, and at what frequency? (Batch / real-time / micro-batch)"*
3. *"What types of data are involved? (Structured tables, semi-structured JSON/XML, unstructured text, images, logs)"*
4. *"Who owns each ingestion pipeline today? Is it automated or manual?"*

**What to listen for:** Fragmented ownership (multiple teams managing different sources independently) is a common sign of a data platform problem, not a downstream problem.

---

#### 4b — Modeling (8 min)

*"Once the data is in — where does it live and how is it organized?"*

1. *"Where are you storing your data? (Relational DB, data lake, data warehouse, lakehouse, hybrid)"*
2. *"What structure do you follow? (Star schema, OBT, medallion architecture, ad hoc)"*
3. *"Is there a semantic layer or data catalog? (dbt models, Looker PDTs, Unity Catalog, etc.)"*
4. *"Who is responsible for modeling — is it centralized or distributed across teams?"*

**What to listen for:** If there is no modeling layer ("we query the raw tables directly"), that is a signal of significant technical debt and a scoping risk.

---

#### 4c — Processing (8 min)

*"How do you actually transform and process the data?"*

1. *"What tools or frameworks are you using to process and transform data? (Spark, dbt, Snowflake, Databricks, Airflow, custom scripts)"*
2. *"How is the processing orchestrated? (Airflow, Prefect, Dagster, cron jobs, manual triggers)"*
3. *"What does a typical pipeline failure look like and how is it handled today?"*
4. *"Are there any heavy compute workloads — ML training, large aggregations, real-time scoring?"*

**What to listen for:** "Cron jobs" and "manual triggers" are signals of fragile, unobservable pipelines. This often drives the core of what Factored gets hired to fix.

---

#### 4d — Delivery (8 min)

*"Now the end of the chain — how does processed data actually reach the people who use it?"*

1. *"What is the current output of your data pipeline? (Dashboards/reports, API endpoints, ML model outputs, agentic workflows, operationalized features in a product)"*
2. *"Who consumes this output — analysts, business users, downstream systems, end customers?"*
3. *"How satisfied are consumers with the current output? Are there recurring complaints?"*
4. *"Is the delivery real-time, scheduled, or on-demand?"*

**What to listen for:** A gap between the sophistication of the infrastructure and the quality of the output (e.g., a complex pipeline producing unreliable reports) often points to a modeling or orchestration issue that is being masked.

---

#### 4e — Pending Topics (8 min)

Cover these after the main pipeline walk-through. They often get forgotten but are critical for scoping.

1. **Data Quality:** *"Do you have any data quality checks in place? Are there known data quality issues today? What is the impact when bad data reaches downstream consumers?"*
2. **SLAs:** *"Do you have formal or informal SLAs for your pipelines? (e.g., dashboards must be refreshed by 8am, model must score within 200ms)"*
3. **Costs:** *"Do you have visibility into your data infrastructure costs? Is cost optimization a concern or constraint for this engagement?"*
4. **Bottlenecks:** *"Where does your pipeline break or slow down most often? What is your biggest operational pain right now?"*
5. **Monitoring and Alerting:** *"How do you know when something breaks? Do you have observability tooling in place? (data contracts, anomaly detection, alerting on freshness/volume)"*

---

### Block 5 — Developer Workflow and Operations (10 min)

Goal: Understand how the client's engineering team works so Factored can integrate without disruption.

**Questions to ask:**

1. *"How do your developers work? Walk me through how a change goes from an engineer's laptop to production."*
2. *"Do you have CI/CD pipelines in place? (GitHub Actions, Jenkins, CircleCI, etc.)"*
3. *"Are you using Infrastructure as Code? (Terraform, Pulumi, CDK)"*
4. *"What cloud provider(s) are you on, and are there constraints on adding new services or tools?"*
5. *"Are there security or compliance requirements we need to design around? (SOC2, HIPAA, GDPR)"*
6. *"Who on your side will work with our team day-to-day? What is their technical background?"*
7. *"Is there any internal resistance or skepticism about this project we should know about?"*

**Facilitation tip:** Question 7 is politically sensitive — frame it as preparation: *"Knowing about any internal dynamics early helps us calibrate our approach and avoid stepping on toes."*

---

### Block 6 — Open Topics + Main Pain Point (5 min)

Always end the technical section with this question. It catches everything you didn't think to ask.

> *"We've covered a lot of ground. Before we close — what is your main pain point today? If you had to pick the one thing keeping your team up at night, what is it?"*

This question, asked after the detailed pipeline walk-through, produces much more specific answers than if asked cold at the start. The client has had 40 minutes to think about their system — their answer here is usually the most honest and actionable thing in the whole session.

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

## SECTION 3 — Problem, Outcome, and Success Criteria

### 3.1 What is the problem as the client describes it?
*(Their words, not your interpretation)*

```
___________________________________________________________
___________________________________________________________
```

### 3.2 What is the root problem?
*(After applying 5 Whys — this may differ from 3.1)*

```
___________________________________________________________
___________________________________________________________
```

### 3.3 What has been tried before?
*(Prior attempts, vendors, internal initiatives — and why they failed)*

```
___________________________________________________________
___________________________________________________________
```

### 3.4 What is the quantified cost of the problem today?
*(Time per week, revenue lost, error rate, manual hours)*

```
___________________________________________________________
___________________________________________________________
```

### 3.5 What does success look like at 30 days?
*(Minimum viable outcome — what must be true for the client to feel the project is on track)*

```
___________________________________________________________
___________________________________________________________
```

### 3.6 What does success look like at 90 days?
*(Full outcome — what the client will point to as the measure of success)*

```
___________________________________________________________
___________________________________________________________
```

### 3.7 How will success be measured?
*(Specific metrics, thresholds, KPIs — if they couldn't answer this, note it as a risk)*

| Metric | Current Baseline | Target | Measurement Method |
|---|---|---|---|
| | | | |
| | | | |
| | | | |

### 3.8 What is explicitly out of scope?
*(Things that came up in conversation that are NOT part of this engagement)*

```
___________________________________________________________
___________________________________________________________
```

### 3.9 Main pain point (closing question)
*(Answer to: "If you had to pick the one thing keeping your team up at night, what is it?")*

```
___________________________________________________________
___________________________________________________________
```

---

## SECTION 4 — Data Landscape

*Map the full pipeline: Ingestion → Modeling → Processing → Delivery. Fill each layer in order.*

---

### 4.1 Ingestion

```
Data sources (list all):
___________________________________________________________

Ingestion frequency: (Real-time / Micro-batch / Daily batch / Manual)
___________________________________________________________

Data volume (GB/day or records/day):
___________________________________________________________

Data types: (Structured / Semi-structured / Unstructured / Mixed)
___________________________________________________________

Who owns each ingestion pipeline today?
___________________________________________________________

Is any ingestion currently manual or fragile?
___________________________________________________________
```

---

### 4.2 Modeling

```
Where is data stored? (Data warehouse / Data lake / Lakehouse / Raw DB / Hybrid)
Tool(s): ___________________________________________________

Data structure followed: (Star schema / OBT / Medallion / Ad hoc / None)
___________________________________________________________

Is there a semantic or transformation layer? (dbt / Looker PDTs / Unity Catalog / None)
___________________________________________________________

Is modeling centralized (one team) or distributed (each team models their own)?
___________________________________________________________

Known modeling debt or "query the raw tables" situations:
___________________________________________________________
```

---

### 4.3 Processing

```
Transformation tools: (dbt / Spark / Snowflake / Databricks / custom scripts / other)
___________________________________________________________

Orchestration tool: (Airflow / Prefect / Dagster / cron / manual / none)
___________________________________________________________

Are there heavy compute workloads? (ML training / large aggregations / real-time scoring)
___________________________________________________________

How are pipeline failures handled today?
___________________________________________________________

Is processing observable? (Logs, alerts, SLA tracking in place?)
___________________________________________________________
```

---

### 4.4 Delivery

```
What is the current output of the pipeline?
  ☐ Reports / Dashboards (tool: ___________________________)
  ☐ API endpoints / data products
  ☐ ML model outputs / predictions
  ☐ Agentic / automated workflows
  ☐ Operationalized features in a product
  ☐ Other: _______________________________________________

Who consumes the output? (Analysts / Business users / Engineers / End customers)
___________________________________________________________

Is delivery real-time, scheduled, or on-demand?
___________________________________________________________

Known complaints or recurring failures from consumers:
___________________________________________________________
```

---

### 4.5 Pending Topics

```
DATA QUALITY
Are DQ checks in place? (Great Expectations / dbt tests / custom / none)
___________________________________________________________
Known data quality issues and their downstream impact:
___________________________________________________________

SLAs
Are there formal or informal SLAs? (e.g., dashboard by 8am, model latency < 200ms)
___________________________________________________________
What happens today when an SLA is missed?
___________________________________________________________

COSTS
Is infrastructure cost visibility in place?
___________________________________________________________
Is cost optimization a constraint or goal for this engagement?
___________________________________________________________

BOTTLENECKS
Where does the pipeline break or slow down most often?
___________________________________________________________
What is the biggest operational pain right now?
___________________________________________________________

MONITORING AND ALERTING
How does the team know when something breaks?
___________________________________________________________
Observability tooling in place: (data contracts / anomaly detection / freshness alerts / none)
___________________________________________________________
```

---

### 4.6 Developer Workflow and Operations

```
Cloud provider(s): ________________________________________
Constraints on adding new services or tools: ______________

CI/CD in place? (GitHub Actions / Jenkins / CircleCI / none)
___________________________________________________________

Infrastructure as Code? (Terraform / Pulumi / CDK / none)
___________________________________________________________

Compliance requirements: (SOC2 / HIPAA / GDPR / PCI / internal policy)
___________________________________________________________

Data residency requirements:
___________________________________________________________

Systems off-limits (cannot be touched or modified):
___________________________________________________________
```

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
- [ ] DTC Sections 1–7 filled completely
- [ ] Any open questions listed and assigned to a follow-up owner
- [ ] Access & Tools Checklist sent to client IT contact (use Section 4.6 as source)
- [ ] Operational SOW drafted based on Section 3 (Problem + Success Criteria) and Section 4 (Data Landscape)
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
