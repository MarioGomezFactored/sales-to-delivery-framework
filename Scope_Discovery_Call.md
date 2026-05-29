# Scope Discovery Call

**Factored.ai Managed Services | 60-minute facilitation guide**

---

## How to use this

The AE opens the call and owns Blocks 1 and 4. The solutions architect (SA) owns Blocks 2 and 3.
Questions marked **[AE]** are relationship/business questions. Questions marked **[SA]** require technical depth.

Read the conditional branches (`→`) only when the client confirms that platform. Do not ask every branch — pick the one that fits and skip the rest.

The goal is not to gather information — it is to understand the project well enough to commit to a scope without surprises.

---

## Block 1 — Project Intent `[AE leads]` · 10 min

> Frame it at the start:
> *"We want to use this time to understand what you need built. The more specific we get today, the more accurate our proposal will be — and the less back-and-forth later."*

**What needs to be built:**

- [ ]  What is the specific deliverable at the end of this project? What does "done" look like?
- [ ]  What currently exists that we're building on top of, replacing, or extending?
- [ ]  What is explicitly **not** part of this project? *(Prevents scope creep before the proposal)*

**Why it matters:**

- [ ]  What happens to the business if this doesn't get delivered? Is there a hard deadline?
- [ ]  Who internally is waiting for this to be done?

**Definition of success:**

- [ ]  How will you evaluate whether what we built actually works?
- [ ]  What does the client test or validate on day 1 after delivery?

---

## Block 2 — Data Landscape `[SA leads]` · 25 min

### Quick Stack Profile *(first 2–3 min — determines which conditionals apply below)*

- [ ]  What is your primary data platform? *(Databricks / Snowflake / BigQuery / Redshift / Synapse / other)*
- [ ]  What cloud provider? *(AWS / GCP / Azure)*
- [ ]  Are you using dbt for transformations?
- [ ]  What is the primary project type? *(Data Engineering / Analytics & BI / ML & AI / Agentic AI / Data Platform build)*

> Note which branch(es) apply, then ask only those conditional questions in the relevant sections below.

---

### Ingestion

> *"Let's walk through your data stack from left to right — sources in, outputs out."*

- [ ]  What are all the data sources feeding into this project? List them.
- [ ]  For each source: Is it an API, a database, a file drop, or an event stream?
- [ ]  What volume — GB/day, TB/day? What is the ingestion frequency?
- [ ]  Is there any real-time or near-real-time requirement, or is batch acceptable?
- [ ]  Are any sources undocumented, unstable, or owned by a third party you don't control?

### Modeling & Storage

- [ ]  Where is the data stored today? *(Warehouse, lake, raw DB, nothing formal yet)*
- [ ]  Is there existing data modeling we build on, or are we starting from scratch?
- [ ]  Is there a data catalog or schema documentation, or do we need to reverse-engineer the current state?

### Processing & Orchestration

- [ ]  What tools are currently transforming this data? *(dbt, Spark, Snowflake Tasks, custom scripts, nothing)*
- [ ]  Is there any orchestration in place, or are jobs triggered manually/by cron?
- [ ]  What orchestrator? *(Airflow, Prefect, Dagster, Databricks Workflows, AWS Step Functions, other)*
- [ ]  Are there existing pipelines we need to integrate with or avoid breaking?

### Delivery

- [ ]  What format does the output need to be in? *(Dashboard, API, flat file, model endpoint, agentic workflow)*
- [ ]  Who consumes the output — an analyst, a downstream system, a business user, a product?
- [ ]  Is there a specific tool or interface this must land in, or is that part of what we decide?

---

### Platform Conditionals *(ask only the branch(es) that match the client's stack)*

#### → Databricks

- [ ]  Are you on Unity Catalog or the legacy Hive metastore?
- [ ]  Are you using Delta Live Tables (DLT), or standard notebooks/Databricks Jobs?
- [ ]  How is deployment managed — Databricks Asset Bundles (DABs), Terraform, or manually?
- [ ]  Is MLflow, Feature Store, or Model Serving in scope?
- [ ]  Can we provision new compute, or must we work within existing cluster policies and pools?
- [ ]  Is this Databricks on AWS, Azure, or GCP? *(affects IAM and networking assumptions)*

#### → Snowflake

- [ ]  Are you using Snowpipe, S3/GCS event triggers, or batch `COPY INTO` for ingestion?
- [ ]  Are Snowflake Streams and Tasks used for CDC or incremental patterns?
- [ ]  Is Snowpark (Python/Java) or Snowflake Cortex (LLM functions) in scope?
- [ ]  Is Snowflake Data Sharing or Marketplace involved?
- [ ]  How is access controlled — a defined RBAC role hierarchy, or ad-hoc grants?

#### → dbt

- [ ]  dbt Core (self-hosted) or dbt Cloud? What version?
- [ ]  How many models exist today? What is the test coverage like?
- [ ]  Are you using dbt packages? *(dbt_utils, audit_helper, codegen, etc.)*
- [ ]  What is the deployment mechanism? *(dbt Cloud jobs, Airflow, GitHub Actions, other)*
- [ ]  Is the semantic layer *(MetricFlow / dbt Metrics)* in use or planned?

#### → AWS

- [ ]  Primary services in play: S3, Glue, Athena, EMR, Redshift, Lambda, Step Functions?
- [ ]  Is there a data lake on S3 with Lake Formation governance?
- [ ]  VPC / PrivateLink constraints that affect connectivity to the data platform?
- [ ]  IAM model: will we get our own role and policies, or work under existing restricted ones?

#### → GCP

- [ ]  Primary services: BigQuery, Dataproc, Dataflow, Pub/Sub, Vertex AI?
- [ ]  Is BigQuery the primary warehouse, or is it part of a larger Dataproc/Hadoop setup?
- [ ]  Is Dataflow (Apache Beam) used for streaming, or is everything batch?
- [ ]  Is Vertex AI or any other Google-managed ML service in scope?

#### → Azure

- [ ]  Primary services: Azure Data Factory, Azure Synapse, Databricks on Azure, ADLS Gen2, Azure ML?
- [ ]  Is CI/CD through Azure DevOps, GitHub Actions, or something else?
- [ ]  Is ADLS Gen2 the primary storage layer?
- [ ]  Is there an existing Microsoft Purview catalog or data governance layer we must integrate with?

---

### Project Type Conditionals *(ask only the branch that matches the primary type)*

#### → Data Engineering / Pipelines

- [ ]  What is the current pipeline execution frequency and expected SLA?
- [ ]  Is there a data quality framework in place? *(Great Expectations, Soda, dbt tests, none)*
- [ ]  What is the expected behavior on failure — retry, alert, halt downstream, or silent?
- [ ]  Is idempotency a requirement? Are backfills expected?

#### → Analytics & BI

- [ ]  What BI tool is the final output going into? *(Tableau, Power BI, Looker, Metabase, other)*
- [ ]  Is the ask a new semantic/metrics layer, or existing reports that need a better data model underneath?
- [ ]  How many dashboards, reports, or datasets are in scope?
- [ ]  Who are the end users — business analysts who will build on top of this, or consumers of fixed reports?

#### → ML & AI

- [ ]  Is this a new model from scratch, a fine-tune of an existing model, or deploying a pre-built model?
- [ ]  Where does training happen? Where does inference happen?
- [ ]  Is there labeled training data, or is labeling part of the scope?
- [ ]  Is model monitoring and drift detection in scope?
- [ ]  What does production serving look like — batch scoring, real-time API, or embedded in a product?

#### → Agentic AI / LLM

- [ ]  What LLM(s) are being used or considered? Is model selection part of the work?
- [ ]  Is RAG needed? What is the knowledge base — internal docs, a database, live APIs?
- [ ]  What does the agent actually do — reasoning steps, tool calls, human-in-the-loop approvals?
- [ ]  Is there a latency or cost-per-query constraint?
- [ ]  Who evaluates whether the agent is working correctly? Is an evals framework in scope?
- [ ]  Is this integrated into an existing product or a standalone internal tool?

---

## Block 3 — Technical Constraints and Team `[SA leads, AE supports]` · 15 min

### Stack and environment

- [ ]  Is there a list of approved tools, or do we have freedom to choose the right one for the job?
- [ ]  Are there compliance or security requirements? *(SOC2, HIPAA, GDPR, internal infosec policy)*
- [ ]  Are there systems we cannot touch, modify, or access?
- [ ]  What is the deployment process — do we have CI/CD access, or do we hand off artifacts for someone else to deploy?
- [ ]  Is there a dev/staging/prod environment separation? Can we get access to dev on day 1?

### Client-side involvement

- [ ]  Who on your team is our daily technical contact during the project? How much bandwidth do they have?
- [ ]  Who approves technical decisions? Who approves scope changes?
- [ ]  Will the client team be doing any part of the work alongside us, or are we fully independent?
- [ ]  Are there external dependencies — third-party vendors, partner teams, legal approvals — that could block progress?

### Handoff and ownership

- [ ]  Who takes ownership of what we build when we leave? Do they exist already, or need to be hired?
- [ ]  Is there an expectation of documentation, runbooks, or training at the end?

---

## Block 4 — Scope Risks and Unknowns `[SA leads, AE closes]` · 10 min

> These questions surface what will blow up the estimate if not caught now.

- [ ]  How would you rate the quality of your current data? *(Clean and trusted / known issues / unknown / "it's a mess")*
- [ ]  Have you tried to build this before? What happened?
- [ ]  Are there other projects running in parallel that touch the same systems or data?
- [ ]  Is there anything about this project that you think is more complex than it looks from the outside?
- [ ]  Is there anything you haven't told us yet that we'll probably discover in week two?

> **Closing question `[AE]`:**
> *"Based on everything we've talked about — is there a budget range you're working within? It helps us right-size the proposal so we're not proposing a Ferrari when you need a reliable car, or the reverse."*

---

## After the Call

- [ ]  Send a written summary of what was discussed within 24h. Ask the client to correct anything.
- [ ]  Flag to the team: any answers that suggest the project is significantly more complex than initially scoped.
- [ ]  Log open questions that need follow-up before the proposal can be written.
- [ ]  Note which platform and project-type branches applied — they determine which estimating templates to pull.

---

## Complexity Red Flags

*(Note these during the call — each one increases estimate uncertainty)*

**Data quality:**

- "We don't really know the data quality" → budget time for a data audit (+20–40% effort)
- "The documentation doesn't exist" → add reverse-engineering effort (+1–2 weeks)
- "We have 10+ data sources" → integration complexity compounds; each new source is not linear

**Tech state:**

- "We're not on Unity Catalog yet" → migration risk if Databricks is in scope
- "We have no CI/CD" → add DevOps setup effort; it is never just one sprint
- "We use dbt but there are no tests" → downstream quality is unknown; validation effort unquantifiable
- "We manage everything in notebooks" → refactor effort likely needed before anything can be built on top
- "We're mid-migration" → avoid building on moving ground; nail the target state first before scoping

**Team and access:**

- "Our contact will be available part-time" → add coordination overhead (+15%)
- "We don't have a data engineer internally" → knowledge transfer must be scoped explicitly
- "We need to request access through IT tickets" → add wait time; day 1 productivity is at risk

**Project dynamics:**

- "We tried this before and it didn't work" → understand why before committing
- "There are other teams touching the same systems" → add dependency risk
- "We need it in 6 weeks" → timeline pressure without scope control is a contract risk
- "Legal/security needs to review everything" → add review cycles to every milestone
