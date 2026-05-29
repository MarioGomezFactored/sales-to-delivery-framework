# External Kickoff — Facilitation Guide
**Factored.ai | S2D Framework — Phase 3**

---

## Before the Call (5 min)

- [ ] Read the DTC from Sales — know the client's pain and what was promised before you ask a single question.
- [ ] Confirm who is attending from the client side and their roles.
- [ ] Have this document open during the call.
- [ ] Ask for recording consent at the start if you plan to record.

---

## Agenda (share with client 24h before)

| # | Topic | Time |
|---|---|---|
| 1 | Introductions | 5 min |
| 2 | Why we're here — alignment on goals | 5 min |
| 3 | Their data landscape | 40 min |
| 4 | How their team works | 10 min |
| 5 | Open topics | 10 min |
| 6 | Next steps | 5 min |

**Total: ~75 min**

> Ask the client to bring anyone closest to the data infrastructure — an engineer, data lead, or architect.

---

## Questions

### Opening
> *"Before we dive in — can you give us a quick picture of what your company does and what brought this project to the table right now?"*

---

### 1. Ingestion
> *"Let's start at the beginning — where does your data come from?"*

- What sources are you ingesting from? What volume of data are you ingesting?
- What types of data do you work with? (structured tables, semi-structured, unstructured, event streams)

---

### 2. Modeling
> *"Once the data is in — where does it live and how is it organized?"*

- Where are you storing your data?
- What structure do you follow to do that? (Lake, Warehouse, Lakehouse)

---

### 3. Processing
> *"How do you transform and move data through your stack?"*

- What are you using to process your data? (Snowflake, dbt, Spark, custom scripts)
- How are you orchestrating all of this?

---

### 4. Delivery
> *"Now the output side — what does the pipeline actually produce?"*

- What's the current output? Reports? Agentic workflows? Operationalized data?
- Who consumes it and how?

---

### 5. Developer Workflow
> *"Last piece — how does your engineering team operate around all this?"*

- How do your developers work?
- Do you have CI/CD in place?
- Are you using IaC?

---

### Final Question *(ask this last, after everything else)*
> *"We've covered a lot of ground. What is your main pain point today — the one thing keeping your team up at night?"*

---

## Topics to Cover if Time Allows

If the conversation flows there, probe on:

- **Data quality** — Do you have DQ checks in place? Are there known data quality issues?
- **SLAs** — Do you have any formal or informal SLAs on your pipelines?
- **Costs** — Is infrastructure cost a concern or constraint?
- **Bottlenecks** — Where does your pipeline break or slow down most often?
- **Monitoring / Alerting** — How do you know when something breaks?

---

## Closing

> *"This has been really helpful. I'll send you a summary of what we covered within 24 hours — please flag anything that's off. We'll use this to put together the detailed plan, which we'll share with you by [date]."*

Confirm before ending:
- [ ] Who receives the summary on their side?
- [ ] Date for the next touchpoint?

---

## After the Call (within 24h)

- [ ] Send notes to the client and ask them to correct anything.
- [ ] Log any open questions that need a follow-up answer.
- [ ] Flag any risks or misaligned expectations to the Account Executive.

---

## Sources Consulted

- S2D_Framework.md — Factored.ai Sales-to-Delivery Framework v1.0. — Phase 3 (External Kickoff) definition and context.
- theory.txt — Internal notes on Sales-to-Delivery Handoff techniques. — Original question list and scoping structure for data pipeline discovery.
