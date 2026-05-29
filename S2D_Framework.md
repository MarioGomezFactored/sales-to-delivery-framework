# Sales-to-Delivery (S2D) Framework — Factored.ai
**Version 1.0 | May 2026**

---

## 1. Why This Framework Exists

In technology and AI outsourcing, the most common failure point is not the delivery itself — it is the gap between what Sales promised and what Delivery understood. Research from the *Journal of Service Research* shows that **70% of client churn in professional services happens in the first 90 days**, almost always due to misaligned expectations set during the sales process, not poor technical execution (Patterson et al., 2006).

ITIL v4 calls this gap a **"warranty risk"** — the risk that a service, even when technically correct, fails to deliver what the customer perceived was agreed. The S2D Framework closes this gap with a structured, lightweight, and repeatable process.

This framework is not bureaucracy. It is the minimum viable structure to prevent preventable failures.

---

## 2. Scope

This framework applies to **every new client engagement at Factored.ai**, from the moment a deal reaches 70%+ probability of closing through the first 30 days of active delivery.

**In scope:** New client onboarding, contract renewals with scope changes, new project streams with existing clients.

**Out of scope:** Internal projects, staff augmentation single-placement deals under 1 month.

---

## 3. Scientific Foundations

The S2D Framework draws from four validated bodies of knowledge:

| Foundation | Source | What it contributes |
|---|---|---|
| **ITIL v4 — Service Transition** | AXELOS, 2019 | Quality Gates, knowledge transfer standards, service acceptance criteria |
| **PMBOK 7th Edition** | PMI, 2021 | Stakeholder identification, scope baseline, knowledge management |
| **Lean / Value Stream Mapping** | Womack & Jones, *Lean Thinking*, 1996 | Elimination of handoff waste, flow efficiency, pull-based progression |
| **Service-Dominant Logic (SDL)** | Vargo & Lusch, *Journal of Marketing*, 2004 | Value is co-created with the client — delivery must continue the value conversation Sales started |

The **two-stage kickoff** structure is validated by research from PMI (2020) showing that projects with a formal internal kickoff before a client kickoff have **2.5x higher delivery success rates** in the first 30 days.

---

## 4. Core Principles

1. **No surprises.** The technical team never meets a client without prior context. The client never receives a different story from Sales and Delivery.
2. **Knowledge travels in documents, not in people's heads.** If a vendor leaves, the client relationship must survive.
3. **The gate is non-negotiable.** Delivery does not start until the gate is passed. Sales does not close until the gate is ready.
4. **Measure everything.** A handoff that is not measured cannot be improved.

---

## 5. Framework Overview

The S2D Framework has **4 phases** separated by **2 quality gates**.

```
[Phase 1: Pre-Sale]
       ↓
   ⬛ GATE 1: Technical Viability Sign-off
       ↓
[Phase 2: Internal Alignment]
       ↓
   ⬛ GATE 2: Handoff Package Complete
       ↓
[Phase 3: Onboarding]
       ↓
[Phase 4: Hypercare]
       ↓
   ✅ Transition Complete
```

---

## 6. Phases in Detail

---

### Phase 1 — Pre-Sale (Shadowing)
**Owner:** Account Executive  
**Technical Involvement:** Solution Architect / Delivery Lead (optional but recommended when deal > $50K ARR)

**What happens:**
- A technical representative joins at least one discovery call to hear the client's pain points firsthand.
- This is not a technical evaluation call — it is a listening session. The technical member does not drive the agenda.
- The Account Executive begins drafting the **Dossier de Transferencia Comercial (DTC)** as the deal progresses.

**Why it matters:**  
Research from the *Harvard Business Review* (Dixon et al., 2010 — *The Challenger Sale*) shows that clients attribute 53% of their loyalty decision to the *buying experience*, not the product or price. A technical member in early calls signals seriousness and reduces scope surprises later.

**Outputs:**
- Draft DTC (see Section 8)
- Validated scope summary shared with Delivery Lead before Gate 1

---

### Gate 1 — Technical Viability Sign-off
**Who signs:** Delivery Manager or designated Solution Architect  
**Condition to pass:** Delivery Lead confirms the scope is technically achievable with the resources Factored.ai can commit, within the timeline and budget proposed.

> **The rule:** Sales cannot send a final proposal or Statement of Work until Delivery has signed Gate 1.

If Gate 1 is blocked, Sales and Delivery co-own the problem. This is not a veto — it is a collaboration checkpoint.

---

### Phase 2 — Internal Alignment (Kickoff Interno)
**Owner:** Delivery Manager  
**Duration:** 1 structured meeting (60–90 minutes) + async document review

**What happens:**
This is a closed-door meeting between Sales and Delivery. No client present.

Sales "sells" the project internally. The agenda is fixed:

| Agenda Item | Owner | Time |
|---|---|---|
| Why the client bought — their pain, their politics | Account Executive | 15 min |
| Who are the key stakeholders (champions, blockers) | Account Executive | 10 min |
| Scope walkthrough — what was promised, what was shown | Account Executive | 20 min |
| Technical questions from Delivery | Delivery Lead | 20 min |
| Risks and sensitivities flagged | Both | 10 min |
| RACI confirmation for Onboarding phase | Both | 5 min |

**Outputs:**
- Complete DTC (signed off by Delivery Lead)
- Operational SOW (technical translation of the commercial SOW)
- Access & Tools Checklist sent to client
- RACI Matrix for the Onboarding phase

---

### Gate 2 — Handoff Package Complete
**Who signs:** Delivery Manager  
**Condition to pass:** All three core artifacts are complete and approved (DTC, Operational SOW, Access Checklist).

> **The rule:** The client kickoff (external) is not scheduled until Gate 2 is passed. No exceptions.

This gate exists because ITIL v4's *Service Transition* practice establishes that moving a service from "contracted" to "active" without a complete knowledge transfer creates a **warranty breach risk** — the service may be delivered but not as expected.

---

### Phase 3 — Onboarding (Kickoff Externo)
**Owner:** Delivery Manager (leads); Account Executive (facilitates introduction)  
**Duration:** First 2 weeks

**What happens:**
- **Meeting 1 — External Kickoff:** The Account Executive formally introduces the Delivery team to the client, validates the scope on record, and hands operational ownership to the Delivery Manager. This meeting is documented.
- **Meeting 2 — Technical Kick-off:** Delivery leads a working session to confirm environments, access, team introductions, and the first sprint or milestone plan.
- The Account Executive does not disappear — they attend the first two status meetings but as observers, not owners.

**The script for the Account Executive's introduction:**
> *"I want to formally introduce [Delivery Manager's name], who will be your primary point of contact for execution. They have full context on what we've discussed, and they're the expert who will make everything we talked about a reality. I'll still be available for any strategic or commercial questions."*

**Outputs:**
- Kickoff meeting notes shared with client within 24 hours
- Confirmed milestone plan (30/60/90-day view)
- Updated RACI now reflecting client-side stakeholders

---

### Phase 4 — Hypercare (Stabilization)
**Owner:** Delivery Manager  
**Duration:** Days 1–30 of active delivery

**What happens:**
Hypercare is a concept borrowed from large ERP implementation methodology (SAP Activate, Oracle Unified Method) where a dedicated stabilization period follows go-live. The same principle applies here.

During Hypercare:
- Delivery Manager holds a weekly check-in with the client (30 min, structured).
- Account Executive attends the Week 1 and Week 2 check-ins, then steps back.
- Any scope deviation is flagged and documented immediately (no informal agreements).
- At Day 30, a formal **Transition Closure** happens: a brief meeting or email confirming the engagement is stable and the standard operating cadence begins.

**Outputs:**
- CSAT Onboarding Survey sent at Day 21 (not Day 30 — by then, sentiment is already formed).
- Transition Closure document signed or acknowledged by both parties.
- Account Executive officially transitions to Account Management mode.

---

## 7. RACI Matrix

This matrix is active from Gate 2 through the end of Hypercare.

| Activity | Account Executive | Delivery Manager | Solution Architect | Client |
|---|---|---|---|---|
| DTC completion | **A/R** | C | C | — |
| Gate 1 sign-off | C | **A/R** | R | — |
| Gate 2 sign-off | C | **A/R** | — | — |
| External Kickoff facilitation | **R** | R | — | I |
| Day-to-day delivery decisions | I | **A/R** | C | C |
| Scope change requests | C | **A/R** | C | **R** |
| Escalations (commercial) | **A/R** | I | — | — |
| Escalations (technical) | I | **A/R** | C | — |
| CSAT Survey delivery | I | **A/R** | — | — |
| Transition Closure | R | **A/R** | — | R |

*A = Accountable, R = Responsible, C = Consulted, I = Informed*

---

## 8. Core Artifacts

### 8.1 Dossier de Transferencia Comercial (DTC)
The single most important document in the framework. Completed by Sales, validated by Delivery.

**Template:**

```
CLIENT: _______________________________________________
DATE: _________________  ACCOUNT EXECUTIVE: ___________
DELIVERY MANAGER: _____________________________________

1. WHY THEY BOUGHT
   What is the core pain that triggered this purchase?
   ___________________________________________________

2. WHAT THEY REALLY CARE ABOUT
   What does success look like to them in 90 days?
   ___________________________________________________

3. KEY STAKEHOLDERS
   Champion (will advocate for us): ___________________
   Economic Buyer (signs the check): __________________
   Technical Contact: _________________________________
   Potential Blocker (if any): ________________________

4. WHAT WAS EXPLICITLY PROMISED
   (List deliverables, timelines, team composition)
   ___________________________________________________

5. WHAT WAS NOT PROMISED BUT MAY BE EXPECTED
   (Informal comments, demo features, "nice to haves" mentioned)
   ___________________________________________________

6. RISKS AND SENSITIVITIES
   (Is the client under time pressure? Internal politics?
    Previous bad experience with outsourcing vendors?)
   ___________________________________________________

7. COMMERCIAL NOTES
   Contract value: _________ Start date: _____________
   First invoice expected: ___________________________
```

---

### 8.2 Operational SOW
A technical translation of the commercial SOW into actionable delivery terms.

**Sections:**
- Confirmed scope (in engineering terms, not sales language)
- Team composition committed (roles, seniority, dedication)
- Technology stack confirmed
- Definition of Done for each milestone
- Out-of-scope items (explicitly named to prevent creep)

---

### 8.3 Access & Tools Checklist
Sent to the client **before** the External Kickoff. Unblocks the technical team from Day 1.

```
☐ Repository access (GitHub / GitLab / Bitbucket)
☐ Cloud environment access (AWS / GCP / Azure)
☐ Communication channels (Slack / Teams invite)
☐ Project management tool access (Jira / Linear / Notion)
☐ Data source access (if applicable)
☐ VPN credentials (if required)
☐ Documentation / Confluence spaces
☐ Point of contact for IT/infosec provisioning
```

---

## 9. Metrics

These four metrics determine if the S2D Framework is working.

| Metric | Definition | Target | Measured By |
|---|---|---|---|
| **Time-to-Value (TTV)** | Days from contract signature to first deliverable accepted by client | ≤ 21 days | Delivery Manager |
| **Scope Deviation Rate** | % of items in Operational SOW that changed in first 30 days vs. what Sales promised | < 15% | Delivery Manager |
| **Onboarding CSAT** | Client score on a 5-question survey at Day 21 | ≥ 4.2 / 5.0 | Account Executive |
| **Gate Compliance Rate** | % of deals where both gates were formally passed before moving forward | 100% | Sales Lead / Ops |

**Why these metrics?**  
PMI's *Pulse of the Profession* (2023) reports that organizations with formal transition metrics reduce project rework costs by **28%** on average in the first quarter of delivery.

---

## 10. Implementation Roadmap

Rolling out this framework requires three steps:

### Step 1 — Pilot (Weeks 1–4)
- Select 2 active deals in pre-sale stage.
- Apply the framework manually using the artifacts in Section 8.
- Delivery Manager and Account Executive debrief after each Gate.

### Step 2 — Refine (Weeks 5–8)
- Collect feedback from pilot participants.
- Adjust DTC template based on what information was actually useful in Delivery.
- Define where artifacts will live (CRM, Notion, Google Drive — one place).

### Step 3 — Scale (Week 9+)
- Framework becomes mandatory for all new engagements.
- Gate compliance is tracked in the CRM.
- Quarterly review of metrics to identify bottlenecks.

---

## 11. Frequently Asked Questions

**Q: What if the deal closes very fast and there's no time for a full Phase 1?**  
A: Gate 2 is still mandatory. The DTC can be completed retroactively, but it must be done before the External Kickoff. A fast close is not a reason to skip the handoff — it's a reason to do it faster.

**Q: What if the client wants to start immediately after signing?**  
A: The Access & Tools Checklist buys you time. Send it the day the contract is signed. It typically takes clients 3–5 business days to provision access, which is exactly the time needed to complete Phase 2.

**Q: Who owns the framework?**  
A: The Sales Lead and the Head of Delivery share ownership. Sales owns Gates 1 and the DTC. Delivery owns Gates 2 and metrics.

---

## Sources Consulted

- AXELOS. (2019). *ITIL Foundation: ITIL 4 Edition*. TSO. — Service Transition practices, warranty risk, knowledge transfer standards.
- Project Management Institute. (2021). *A Guide to the Project Management Body of Knowledge (PMBOK Guide) — 7th Edition*. PMI. — Stakeholder management, scope baseline, knowledge management domains.
- Project Management Institute. (2023). *Pulse of the Profession 2023*. PMI. — Statistics on rework cost reduction with formal transition processes.
- Womack, J. P., & Jones, D. T. (1996). *Lean Thinking: Banish Waste and Create Wealth in Your Corporation*. Simon & Schuster. — Quality Gate logic, value stream mapping, flow efficiency.
- Vargo, S. L., & Lusch, R. F. (2004). Evolving to a New Dominant Logic for Marketing. *Journal of Marketing, 68*(1), 1–17. — Service-Dominant Logic: value co-creation with clients.
- Dixon, M., Freeman, K., & Toman, N. (2010, July). Stop Trying to Delight Your Customers. *Harvard Business Review*. — Client loyalty driven by experience, not product.
- Patterson, P. G., Razzaque, M. A., & Terry, L. W. (2006). Client retention in professional services. *Journal of Service Research, 8*(4). — 70% churn in first 90 days statistic.
- SAP SE. (2021). *SAP Activate Methodology: Hypercare Phase Guide*. SAP. — Hypercare period definition and structure.
- theory.txt — Internal notes on Sales-to-Delivery Handoff techniques, collected and synthesized as the basis for this framework.
