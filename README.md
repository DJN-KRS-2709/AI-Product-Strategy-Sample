# RenewalRadar AI Product Strategy

> A fictional completed strategy repo for students. RenewalRadar AI is a copilot for B2B Customer Success teams that predicts renewal risk, explains the drivers, and drafts intervention plans before accounts churn.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, why now.**

- **Product:** RenewalRadar AI
- **AI Value Archetype:** Copilot + Oracle
- **Vulnerability Scores:** Moat 3/5 · Data 4/5 · Platform 2/5
- **Top Risk:** Salesforce or Gainsight ships an embedded renewal-risk assistant with native CRM distribution.
- **Confidence:** M
- **Prototype:** `https://renewalradar.example/demo`
- **Kill Criteria:** Stop if pilot teams cannot improve save-rate on flagged accounts by at least 8 percentage points within 90 days.

Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:** 12/20
- **Weakest Loop:** Network loop, because one customer's data improves that customer today but only weakly improves the system for others.
- **Encroachment Defense:** Own the renewal workflow end-to-end: ingest signals, explain risk, draft plays, capture outcomes, and feed win/loss learning back into account models.
- **Vendor Portability:** Partial

Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** 82% for non-AI CS analytics
- **Gross Margin (AI-adjusted):** 68% at planned usage
- **Pricing Model:** Hybrid seat + monitored-account pricing
- **Cascading Strategy:** Small model classifies routine accounts; frontier model handles high-risk enterprise accounts and executive-ready narratives.
- **Break-even at:** 18 customers with 25 CSM seats each, or about 11,000 monitored accounts.

Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** 85% precision on top-risk accounts, less than 5% unsupported claims in generated narratives.
- **Golden Dataset:** 120 rows, 25 adversarial
- **Confidence UX:** Risk score plus evidence panel, confidence tier, and human approval before customer-facing messages.
- **HITL Architecture:** CSM approves every renewal play before it enters CRM or email.
- **Failure Mode Coverage:** Missing product usage, contradictory sentiment, late-stage executive escalation, and renewal date drift.

Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

- **Compounding System:** Every accepted, edited, or rejected save plan improves account-risk labeling and playbook recommendations.
- **Governance Posture:** Advisory only for first 6 months; no autonomous outreach without CSM approval.
- **Shadow AI Status:** 6 tools found, 3 triaged into governed workflows
- **Agent Boundaries:** Agents may summarize, score, and draft. They may not send external messages, update commercial terms, or mark an account as churned.
- **Regulatory Exposure:** Low to medium. Main exposure is customer data handling, confidentiality, and automated decision transparency.

Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):** Risk scoring and evidence summaries for existing CSM workflow.
- **Horizon 2 (Next):** Playbook recommendations, CRM writeback, and team preference learning.
- **Horizon 3 (Bet):** Renewal operating system with portfolio-level forecasting and automated save-plan orchestration.
- **Board Narrative:** RenewalRadar turns scattered customer signals into a compounding renewal intelligence layer that improves save-rate while protecting margin.
- **Key Metric:** Incremental gross revenue retained from AI-flagged accounts.

Details: [`06-the-pitch/`](06-the-pitch/)
