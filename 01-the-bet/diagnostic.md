# Three-Axis Vulnerability Diagnostic

## Product

**Product:** RenewalRadar AI
**Your Role:** Group Product Manager, Customer Success Platform

RenewalRadar AI helps B2B Customer Success teams identify renewal risk earlier by combining CRM data, product usage, support tickets, call notes, stakeholder sentiment, and contract history into a ranked account risk view. The product then drafts account-specific save plans for CSM approval.

---

## Scores

### Contextual Moat — 3/5
*Workflow depth x switching cost. Would users leave in a weekend if a competitor showed up?*

**Score rationale:** RenewalRadar sits in the weekly account review workflow and writes back to Salesforce, Gainsight, Slack, and the customer health dashboard. That creates switching cost once a team has adopted it. The moat is not yet deep because early users still treat it as an analysis layer, not the system of record for renewal action.

**Named attacker (from partner challenge):** Gainsight could add AI-generated renewal-risk summaries directly inside its customer success platform.

---

### Data Advantage — 4/5
*Proprietary signal that compounds with usage. What do you see that OpenAI doesn't?*

**Score rationale:** We see account-level renewal outcomes, CSM edits to risk rationales, sales exceptions, product usage trends, and support escalation histories. The most valuable signal is whether a recommended intervention actually changed the renewal outcome. OpenAI and generic model providers do not see this closed-loop commercial result.

**Named attacker (from partner challenge):** Salesforce could use CRM, Slack, support, and contract data to train a native Einstein renewal assistant.

---

### Platform Exposure — 2/5
*Encroachment risk x pivot speed. If Apple/Google/OpenAI ships your hero feature native, then what?*

**Score rationale:** The exposed layer is high. Salesforce, HubSpot, Gainsight, Zendesk, and Microsoft all sit closer to key systems of record. If they ship a good-enough embedded assistant, RenewalRadar loses the lightweight "AI summary" value. The defensible part must become workflow orchestration, outcome learning, and cross-tool context.

**Named attacker (from partner challenge):** Salesforce Einstein for Revenue Retention.

---

## Top Vulnerability

The biggest strategic risk is becoming a renewal-risk wrapper that summarizes CRM data but does not own the intervention workflow or the outcome learning loop.

## Confidence Level

**M.** The problem is painful and measurable, and the data advantage is credible. Confidence stays medium because platform encroachment risk is real and the first version must prove it improves gross revenue retention, not just CSM productivity.
