# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | Account has 42% product usage drop, 3 unresolved P1 tickets, renewal in 75 days, neutral call sentiment. | High renewal risk with support quality and usage decline as primary drivers; recommend exec escalation and support recovery plan. | N | rule + LLM |
| 2 | Account has low usage but contract is seasonal and usage drops every Q4. | Medium or low risk; model must mention seasonality and avoid false alarm. | Y | rule |
| 3 | Account has positive CSM notes but negative support sentiment and delayed implementation milestone. | Medium-high risk with contradictory evidence; ask CSM to verify sponsor sentiment. | Y | LLM |
| 4 | Account has renewal in 18 months but severe usage drop this month. | Monitor risk, not renewal risk; recommend product adoption intervention instead of commercial save plan. | Y | rule |
| 5 | Enterprise account has sponsor departure, no recent executive contact, and high product adoption. | Medium risk; flag relationship risk but avoid claiming product dissatisfaction. | N | LLM |

**Adversarial rows included:** 25

**Coverage gaps identified by partner:** The first dataset underrepresented accounts with missing CRM fields, multi-product contracts, and renewals handled through procurement partners.

## Confidence UX Design

**Approach:** Tiered confidence with an evidence panel and human-in-loop trigger. The UI always separates "observed evidence" from "model interpretation."

**High confidence (>90%):** Show risk score, top 3 drivers, evidence links, and recommended save plan. CSM can approve, edit, or reject.

**Medium confidence (70-90%):** Show risk score and drivers, but label the recommendation "Needs CSM review." Ask one clarifying question before drafting customer-facing language.

**Low confidence (<70%):** Do not generate a save plan. Show missing evidence and request CRM, support, or usage data validation.

**User control surface:** Every generated recommendation has buttons for "accurate," "wrong driver," "missing context," "too aggressive," and "not actionable." These labels feed the correction loop.

## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | 85% precision on top-risk decile | Weekly golden dataset + pilot outcome review | Below 78% for 2 consecutive weeks |
| Hallucination rate | Less than 5% unsupported claims | Automated citation check + manual QA sample | Above 8% in any enterprise segment |
| Latency (p95) | Under 8 seconds for account summary; under 20 seconds for full save plan | Production telemetry | Above 12 seconds summary or 30 seconds save plan |
| Drift velocity | Less than 10% score movement without new evidence | Score diff monitoring | More than 15% unexplained movement week over week |

## HITL Architecture

RenewalRadar is advisory by default. A human CSM must approve every save plan before it updates CRM tasks, creates Slack escalation messages, or drafts customer-facing email.

Escalation path:

1. Low confidence or missing evidence routes to the CSM for data validation.
2. High-risk enterprise accounts route to the CSM and CS Director.
3. Any recommendation involving pricing, contract concessions, or executive escalation requires manager approval.
4. Customer-facing copy is draft-only until a human sends it from the system of record.

## Red-Team Findings

The red team found that RenewalRadar over-weighted negative support tickets for customers who had already received service credits and were satisfied with the recovery. The fix is to incorporate compensation events and post-resolution sentiment before labeling support history as an active renewal risk.
