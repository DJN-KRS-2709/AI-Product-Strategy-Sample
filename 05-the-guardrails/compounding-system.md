# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Save-plan correction loop | CSM edits, rejects, and approved actions | Better playbook recommendations by risk pattern | Y | active |
| Renewal outcome loop | Won, saved, downsold, churned, delayed renewal | Stronger account-risk labels and benchmark calibration | Y | active |
| Evidence quality loop | CSM marks evidence as missing, stale, or misleading | Better data-quality checks and connector priorities | Y | active |
| Cross-customer benchmark loop | Aggregated segment-level intervention performance | Better playbook defaults for new customers | Y | broken |

**Broken loop identified by partner:** The cross-customer benchmark loop is strategically important but weak because customer data sharing rules are not yet clear enough.

**Fix plan:** Create an anonymized benchmark layer with privacy review, minimum aggregation thresholds, and opt-in controls. Start with non-sensitive metrics: intervention type, segment, renewal stage, and outcome category.

## Context Connectivity

RenewalRadar connects context across five systems:

- Salesforce for account ownership, renewal date, ARR, opportunity stage, and executive sponsor.
- Product analytics for seat activation, feature adoption, usage decay, and admin activity.
- Support desk for unresolved tickets, severity, time-to-resolution, and post-resolution sentiment.
- Call intelligence for stakeholder concerns, objections, and champion strength.
- Contract system for term length, pricing exceptions, and procurement constraints.

The biggest silo is implementation history. Early churn risk often starts during onboarding, but implementation data lives in project tools that are not always connected to Customer Success workflows.

## Governance Policy

**Scope:** RenewalRadar may analyze customer data, score risk, summarize evidence, draft save plans, and recommend internal actions.

**Autonomy boundaries:** The system may not send customer-facing messages, change CRM stages, alter commercial terms, mark an account as churned, or trigger executive escalation without human approval.

**Escalation triggers:** Low confidence, unsupported claims, contract concessions, legal language, executive outreach, or ARR above $250K.

**Audit cadence:** Weekly QA sample for generated narratives, monthly golden dataset review, quarterly privacy and security review.

**Regulatory exposure (EU AI Act / other):** Low to medium. The system supports business decisions but does not make legally binding decisions about individuals. Primary risks are confidentiality, data minimization, and automated decision transparency.

## Agent Topology

**Risk Agent:** Scores renewal risk and cites evidence. It can read connected systems but cannot write to them.

**Narrative Agent:** Drafts the risk explanation and save-plan summary. It must cite account evidence for each claim.

**Playbook Agent:** Recommends next-best actions based on segment, risk pattern, and historical outcomes. It can create draft tasks but cannot assign them without CSM approval.

**QA Agent:** Checks whether claims are supported, whether confidence labels match evidence quality, and whether recommended actions violate policy.

**Approval Owner:** The assigned CSM approves account-level actions. The CS Director approves enterprise escalations and concessions.

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| CSMs using ChatGPT to summarize call notes | Customer Success | H | govern |
| RevOps spreadsheet with manually generated churn-risk prompts | Revenue Operations | M | migrate into RenewalRadar |
| Slack bot that drafts executive escalation messages | Customer Success Ops | H | kill until approval workflow exists |
| Gong AI summaries | Sales / CS | M | keep as source input |
| Support sentiment classifier | Support Ops | L | keep |
| Unapproved browser extension for CRM summarization | Individual users | H | kill |

**Total tools found:** 6
**Tools after triage:** 3 governed, 2 killed, 1 migrated
**Estimated hidden spend:** $4,800 per month across personal AI subscriptions and duplicate summarization tools
