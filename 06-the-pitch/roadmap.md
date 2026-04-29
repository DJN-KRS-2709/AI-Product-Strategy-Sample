# Three-Horizon Roadmap & Board Pitch

## Roadmap

### Horizon 1 — Now (0-3 months)
*Quick wins. Ship with existing capabilities.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| Launch renewal-risk cockpit for 5 pilot customers | 70% weekly active CSM usage by week 6 | H |
| Add evidence-backed account summaries with CSM approval | 85% of summaries rated useful by CSMs | M |
| Build golden dataset and hallucination guardrail | Less than 5% unsupported claims | H |

### Horizon 2 — Next (3-9 months)
*Bets. Requires new capabilities or integrations.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| Launch save-plan recommendations and CRM task writeback | 60% of high-risk accounts receive approved action plan | M |
| Add team preference learning for playbook tone and escalation norms | 30% reduction in CSM edits per generated plan | M |
| Launch provider-neutral LLM gateway with quality-aware routing | AI COGS below $10 per CSM seat per month | M |

### Horizon 3 — Bet (9-18 months)
*Moonshots. High uncertainty, high potential.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| Build privacy-safe renewal benchmark layer across customers | 15% improvement in save-plan precision for new customers | L |
| Launch portfolio forecasting for VP Customer Success and CFO workflows | Forecast renewal variance within +/- 5% | M |
| Move from recommendations to governed orchestration for internal workflows | 40% reduction in manual renewal prep time | L |

## Board Pitch

**Thesis (1 sentence):** RenewalRadar turns scattered customer signals into a compounding renewal intelligence layer that helps Customer Success teams save more revenue without adding headcount.

**The case:**

1. **Why now:** Net retention is under pressure, CSM teams are carrying larger books, and customers already have the raw data but cannot convert it into timely intervention.
2. **What's defensible:** The moat is not the model. It is the closed loop from account signal to save plan to renewal outcome, with every edit and outcome improving future recommendations.
3. **The economics:** AI reduces gross margin from 82% to 68%, but price expansion and account overage more than offset cost if the product improves gross revenue retention by at least 1.5 percentage points.

**The risks:**

1. **Trust / failure modes:** False risk claims could damage credibility with CSMs. Mitigation: evidence citations, confidence tiers, golden dataset, and human approval.
2. **Scale / governance:** Shadow AI behavior could leak customer data or send unapproved messages. Mitigation: advisory-only agents, approval gates, audit logs, and governed integrations.
3. **Competitive:** Salesforce or Gainsight can copy summaries quickly. Mitigation: own the cross-system workflow and outcome learning loop before summaries become a commodity.

**The ask:** Fund a 9-month build with 1 product manager, 5 engineers, 1 designer, 1 data scientist, and 0.5 RevOps support to reach 20 design partners, prove renewal lift, and decide whether to scale in FY27.

## M1 Baseline vs. Now
*Your 3-sentence AI strategy from Module 1 vs. what you'd say now:*

**M1 baseline:**

RenewalRadar will use AI to predict renewal risk and help CSMs act earlier. It will differentiate through proprietary customer data and reduce churn by surfacing risks that traditional health scores miss. The first version will prove value by showing better risk detection in a pilot.

**Now:**

RenewalRadar is not a prediction feature; it is a renewal operating loop. The strategy is to own the workflow from signal ingestion to evidence-backed risk explanation, CSM-approved save plan, and measured renewal outcome. We will win only if every correction and outcome compounds into better playbooks while the architecture stays portable, governed, and profitable.
