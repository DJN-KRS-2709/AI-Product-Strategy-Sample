# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | 3/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | 4/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | 3/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | 2/5 |

### Correction Loop — 3/5
**What you capture today:** CSM edits to generated risk rationales, accepted/rejected save-plan actions, false-positive flags, and the final renewal outcome.

**How it compounds:** Edits improve future rationale templates and intervention playbooks. The loop is only a 3 because corrections are reviewed weekly, not yet fed automatically into model fine-tuning or retrieval rules.

### Preference Loop — 4/5
**What you capture today:** Team-specific thresholds for "high risk," preferred playbook tone, escalation rules, renewal stage definitions, and CSM feedback on which evidence is persuasive.

**How it compounds:** The product learns that enterprise CSMs prefer executive-ready narratives while SMB CSMs prefer tactical action lists. This makes outputs feel more native to each team over time.

### Domain Context Loop — 3/5
**What you capture today:** SaaS renewal patterns by segment, implementation delays, sponsor change events, usage decay curves, support severity, and contract term history.

**How it compounds:** Signals from support, product usage, and CRM combine into better renewal explanations. This is a 3 because cross-domain transfer works inside one customer instance but is still weak across customers.

### Network Loop — 2/5
**What you capture today:** Aggregated playbook performance by segment and anonymized patterns around which interventions work for which renewal risks.

**How it compounds:** The system can suggest better playbooks as more customers use it, but privacy constraints limit how much learning can move across tenants. This is the weakest loop.

**Total Flywheel Score: 12/20**
**Weakest Loop:** Network
**Fix for weakest loop:** Build a privacy-safe benchmark layer that shares aggregate intervention performance by segment without exposing customer data.

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:** Salesforce
**Vector:** Native Einstein renewal-risk assistant embedded in CRM, Slack, and account planning.
**Time-to-threat:** 6-9 months
**% of value at risk:** 45%

### 2. Vertical Competitor
**Attacker:** Gainsight
**Vector:** Adds generative save plans and outcome learning to existing customer success workflows.
**Time-to-threat:** 3-6 months
**% of value at risk:** 55%

### 3. Adjacent Expansion
**Attacker:** Gong
**Vector:** Expands from call intelligence into renewal-risk prediction using customer conversation data.
**Time-to-threat:** 9-12 months
**% of value at risk:** 30%

---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:** Salesforce Einstein

**Attack vector (target the weakest loop):** Use native CRM distribution and aggregated Salesforce benchmark data to attack RenewalRadar's weak network loop.

**Weeks 1-4 — what they ship:** Launch "Renewal Risk Summary" in Salesforce account pages with AI-generated risk drivers from opportunities, cases, activity history, and Slack messages.

**Weeks 5-8 — how they poach users:** Bundle it into Sales Cloud Enterprise at no extra cost for the first year and run webinars for Customer Success leaders on "AI retention from your CRM data."

**Weeks 9-12 — why users don't come back:** Add automated Salesforce tasks and executive briefing drafts. Customers decide RenewalRadar is another tab unless it proves better save-rate lift.

**Your defense:** Move from summaries to workflow ownership: closed-loop save-plan tracking, outcome-based playbook learning, and cross-tool evidence Salesforce cannot fully see without deep product-usage and support integrations.
