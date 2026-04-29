# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Primary: OpenAI GPT-4.1 for account narratives. Secondary: Anthropic Claude for evaluation and fallback drafting. | M | Route all new high-risk account summaries to Claude while limiting OpenAI to existing cached accounts. |
| **Abstraction** | All model calls go through an internal `llm_gateway` service, but prompt templates still include provider-specific formatting. | M | Remove provider-specific prompt syntax from the top 5 production templates. |
| **Routing** | Simple rules route by account tier: SMB to small model, enterprise to frontier model. No live quality-aware routing yet. | M | Freeze enterprise generation to frontier fallback and shift SMB summaries to cheaper small model. |
| **Eval** | 120-row golden dataset with weekly manual review and automated claim-support checks. | L | Run full eval against fallback provider before shifting more than 25% of traffic. |

## Portability Score

**Partial**

RenewalRadar can survive a provider outage or price spike, but it cannot yet swap providers invisibly in 48 hours. The main blocker is prompt portability and eval coverage for nuanced renewal narratives.

## If OpenAI doubles pricing tomorrow:

The 48-hour response is:

1. Move low-risk and medium-risk account summaries to the small-model cascade.
2. Route enterprise drafts through Claude only after the golden dataset passes the 85% precision threshold.
3. Disable auto-regeneration for unchanged accounts and rely on cached summaries until the next risk-state change.
4. Notify Finance that AI COGS may rise from $5.85 to $8.40 per CSM seat for one billing cycle.

## If OpenAI ships a competing product:

The defensible layer is not model access. The defensible layer is the renewal workflow and outcome data:

- RenewalRadar tracks whether a save plan was accepted, edited, executed, and tied to a renewal result.
- It combines product usage, support, CRM, call notes, and contract metadata across systems.
- It learns customer-specific renewal definitions, playbook preferences, and escalation norms.
- It gives VP Customer Success teams a portfolio-level operating rhythm, not just an account summary.

## Portability Actions

**This week:** Move the five highest-volume prompt templates into provider-neutral YAML and add snapshot tests for output schema.

**This month:** Add Gemini as a third provider in the gateway and run the golden dataset weekly across all three providers.

**This quarter:** Implement quality-aware routing that chooses provider by account tier, cost ceiling, latency, and eval performance.
