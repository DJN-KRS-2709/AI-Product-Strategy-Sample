# RenewalRadar AI

> Customer Success teams will pay for an AI renewal copilot that converts scattered customer signals into evidence-backed save plans because renewal risk is rising, CSM teams are overloaded, and existing health scores are too shallow to drive action.

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
- **Top Risk:** The biggest strategic risk is becoming a renewal-risk wrapper that summarizes CRM data but does not own the intervention workflow or the outcome learning loop.
- **Confidence:** M
- **Prototype:** https://renewalradar.example/demo
- **Kill Criteria:** Stop or materially pivot if any of these are true after the first 90-day pilot:

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:**
- **Weakest Loop:** Network
- **Top Encroachment Threat:** Salesforce
- **Encroachment Defense:** Build a privacy-safe benchmark layer that shares aggregate intervention performance by segment without exposing customer data.
- **Vendor Portability:** Partial

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** 82%
- **Gross Margin (AI-adjusted):** 68%
- **Pricing Model:** Hybrid seat-based + monitored-account pricing
- **Pricing Today → Tomorrow:** Non-AI customer health dashboard at $49 per CSM seat per month. → $89 per CSM seat per month plus $0.20 per monitored account over 50 accounts per CSM.
- **Total AI COGS / unit:** $8.75
- **Cascading Strategy:** Triage: GPT-4.1 mini or equivalent small model; frontier: GPT-4.1 / Claude Sonnet for high-risk enterprise narratives; ratio 72% small model / 28% frontier model
- **Net Margin Shift:** Gross margin falls 14 points, but average revenue per account expands by 82%. The bet works if RenewalRadar improves gross revenue retention by at least 1.5 percentage points for mid-market customers …
- **Break-even at:** 18 average customers, or about 11,000 monitored accounts

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** 85% precision on top-risk decile
- **Golden Dataset:** 5 rows, 25 adversarial
- **Confidence UX:** Tiered confidence with an evidence panel and human-in-loop trigger. The UI always separates "observed evidence" from "model interpretation."
- **HITL Architecture:** RenewalRadar is advisory by default. A human CSM must approve every save plan before it updates CRM tasks, creates Slack escalation messages, or drafts customer-facing email.
- **Failure Mode Coverage:** The red team found that RenewalRadar over-weighted negative support tickets for customers who had already received service credits and were satisfied with the recovery.…

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales — and what compounds.**

- **Compounding System:** | Loop | Input | Output | Compounds? | Status | |------|-------|--------|-----------|--------| | Save-plan correction loop | CSM edits, rejects, and approved actions | Better playbook recommendations by risk pattern | Y …
- **Governance Posture:** RenewalRadar may analyze customer data, score risk, summarize evidence, draft save plans, and recommend internal actions.
- **Autonomy Boundaries:** The system may not send customer-facing messages, change CRM stages, alter commercial terms, mark an account as churned, or trigger executive escalation without human approval.
- **Escalation Triggers:** Low confidence, unsupported claims, contract concessions, legal language, executive outreach, or ARR above $250K.
- **Audit Cadence:** Weekly QA sample for generated narratives, monthly golden dataset review, quarterly privacy and security review.
- **Shadow AI Status:** 6 tools found · 3 governed, 2 killed, 1 migrated · est. spend $4,800 per month across personal AI subscriptions and duplicate summarization tools
- **Agent Boundaries:** **Risk Agent:** Scores renewal risk and cites evidence. It can read connected systems but cannot write to them.
- **Regulatory Exposure:** Low to medium. The system supports business decisions but does not make legally binding decisions about individuals. Primary risks are confidentiality, data minimization, and automated decision transparency.

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):** Launch renewal-risk cockpit for 5 pilot customers · Add evidence-backed account summaries with CSM approval · Build golden dataset and hallucination guardrail
- **Horizon 2 (Next):** Launch save-plan recommendations and CRM task writeback · Add team preference learning for playbook tone and escalation norms · Launch provider-neutral LLM gateway with quality-aware routing
- **Horizon 3 (Bet):** Build privacy-safe renewal benchmark layer across customers · Launch portfolio forecasting for VP Customer Success and CFO workflows · Move from recommendations to governed orchestration for internal workflows
- **Board Narrative:** RenewalRadar turns scattered customer signals into a compounding renewal intelligence layer that helps Customer Success teams save more revenue without adding headcount.
- **Ask:** Fund a 9-month build with 1 product manager, 5 engineers, 1 designer, 1 data scientist, and 0.5 RevOps support to reach 20 design partners, prove renewal lift, and decide whether to scale in FY27.
- **Key Strategic Change:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
