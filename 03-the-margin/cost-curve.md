# Cost Curve & Pricing Strategy

## Cost Model

Assumption: one CSM manages 45 monitored accounts and regenerates full risk narratives twice per month. High-risk accounts receive deeper analysis and save-plan drafts.

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $3.90 | Frontier model for high-risk accounts, board-ready summaries, and save-plan drafts. |
| Inference (cascading/triage) | $0.85 | Small model classifies routine accounts and detects whether a full refresh is needed. |
| Infrastructure | $1.10 | Vector search, orchestration, observability, and secure job queues. |
| Data/storage | $0.65 | CRM snapshots, usage aggregates, support ticket embeddings, and audit logs. |
| Human-in-the-loop | $2.25 | QA review for sampled outputs and customer onboarding calibration. |
| **Total AI COGS** | **$8.75** | Target ceiling is $10 per CSM seat per month. |

## Cascading Strategy

**Triage model:** GPT-4.1 mini or equivalent small model

**Frontier model:** GPT-4.1 / Claude Sonnet for high-risk enterprise narratives

**Routing rule:** Small model scores every account weekly. Only accounts with risk score above 70, executive sponsor change, renewal within 120 days, or contradictory signals get frontier-model analysis.

**Expected cascade ratio:** 72% small model / 28% frontier model

## Pricing Model

**Current pricing:** Non-AI customer health dashboard at $49 per CSM seat per month.

**Proposed AI pricing:** $89 per CSM seat per month plus $0.20 per monitored account over 50 accounts per CSM.

**Model:** Hybrid seat-based + monitored-account pricing

**Why this model:** Seat-based pricing maps to the buyer's budget owner, while monitored-account pricing protects margin for unusually large portfolios.

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | AI COGS rises from $8.75 to about $18.40 per seat; gross margin drops from 68% to 57%. | Tighten frontier routing to top 15% of accounts and cache unchanged account narratives for 14 days. |
| Heaviest segment doubles | Enterprise CSMs with 90+ accounts exceed the cost ceiling and create noisy refresh volume. | Add account-volume tiers and charge $0.35 per monitored account above 75 accounts per CSM. |
| Model provider raises prices 50% | Gross margin drops 4-6 points depending on frontier usage. | Shift routine summaries to fallback provider and require eval pass before routing enterprise narratives. |

## Board One-Pager

**Before (traditional SaaS):** $49 per CSM seat, 82% gross margin, value framed as reporting and visibility.

**After (AI-enabled):** $89 per CSM seat + account overage, 68% gross margin at planned usage, value framed as saved revenue and CSM leverage.

**Net margin shift:** Gross margin falls 14 points, but average revenue per account expands by 82%. The bet works if RenewalRadar improves gross revenue retention by at least 1.5 percentage points for mid-market customers and 0.7 percentage points for enterprise customers.

## Break-Even Math

- Average customer: 25 CSM seats
- Average monthly revenue: $2,225 base + $475 account overage = $2,700
- Average AI COGS: $219 per month
- Fully loaded monthly cost to serve: $1,540
- Break-even: 18 average customers, or about 11,000 monitored accounts
