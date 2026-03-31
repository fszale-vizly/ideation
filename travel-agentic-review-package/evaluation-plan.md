# Evaluation Plan

**Initiative:** Travel Production Agentic-First Pilot  
**Date:** 2026-03-31  
**Owner:** Pilot DRI with leadership review

---

## Outcome Thesis

**If we replace one manually coordinated travel workflow with a capability-based agentic pilot that has durable state, source intelligence, QA checks, and human-gated exception handling, we expect request-to-delivery lead time and manual coordination burden to fall materially within 12 weeks without harming quality, delivery reliability, or compliance.**

---

## Baseline

| Metric | Baseline Value | Measurement Method | Source | Baseline Date |
|---|---|---|---|---|
| Primary outcome metric: median request-to-delivery lead time | To be measured before pilot | Request open timestamp to successful delivery timestamp | Existing request and delivery logs | Week 0 |
| Leading indicator 1: manual touches per request | To be measured before pilot | Count human interventions / handoffs per request | Workflow logs + operator tagging | Week 0 |
| Leading indicator 2: first-pass QA pass rate | To be measured before pilot | Requests passing QA without rework | QA records | Week 0 |
| Leading indicator 3: new source onboarding lead time | To be measured before pilot | Start of feasibility to source live | Onboarding logs | Week 0 |
| Supporting metric: extraction success rate | To be measured before pilot | Successful runs / total runs | Run telemetry | Week 0 |
| Supporting metric: cost per successful delivery | To be measured before pilot | Total infra and model cost / successful deliveries | Billing + run telemetry | Week 0 |

---

## Success Measures

### Primary Outcome Metric

| Metric | Why It Matters | Target | Direction | Review Cadence |
|---|---|---|---|---|
| Median request-to-delivery lead time | Best operational expression of speed and coordination quality | 40-60% improvement for pilot workflow by Week 12 | Lower is better | Weekly |

### Leading Indicators

| Metric | Signal Type | Target | Why It Predicts Success |
|---|---|---|---|
| Manual touches per request | Adoption / process | 30-50% reduction | Shows coordination burden is falling |
| First-pass QA pass rate | Quality | Improve or remain stable while speed improves | Prevents “faster but worse” failure mode |
| New source onboarding lead time | Throughput | 25-40% reduction after initial stabilization | Shows system is becoming more reusable |
| Extraction success rate | Reliability | Improve week over week | Indicates orchestration and source knowledge are working |

### Failure Signals

| Signal | Threshold | What It Means | Required Response |
|---|---|---|---|
| QA pass rate drops materially | >5-10% degradation vs. baseline | Speed is being bought with lower quality | Stop scaling and redesign checks |
| Compliance or credential incident | Any material incident | Governance model is not safe | Immediate halt and root-cause review |
| Manual touches stay flat | <10% improvement by Gate 2 | The system is still coordinating like the old hierarchy | Revisit capability split and control plane |
| Pilot requires heavy SME rescue | >20% of requests | Knowledge system is insufficient | Narrow scope and strengthen source intelligence |
| Lead time does not improve | <15% by Week 8 | Value claim is weak or poorly implemented | Rework pilot before expansion |

---

## Instrumentation and Evidence

| Question | Evidence Needed | Source System | Owner |
|---|---|---|---|
| Are we improving the primary metric? | End-to-end lead time per request | Request + run + delivery ledger | Pilot DRI |
| Are humans intervening less? | Human touch counts, exception tags | Workflow logs and operator annotations | Operations lead |
| Are outputs still good? | QA pass/fail, rework loops, anomaly classes | QA system | QA lead |
| Are we learning from failures? | Failure reason codes, source knowledge updates, incident reviews | Run ledger + knowledge repo | Source intelligence lead |
| Are we staying compliant? | Approval logs, secret access logs, audit checks | Governance tooling | Compliance lead |

---

## Review Cadence

| Cadence | Review Focus | Participants | Decisions |
|---|---|---|---|
| Weekly | Metric movement, incidents, blocked work, top failure modes | Pilot DRI, capability leads, QA, compliance | Continue / adjust / narrow |
| Monthly | Trend vs. baseline, org implications, next investment decision | Leadership + pilot team | Fund next phase / hold / redesign |
| Stage gate | Formal go/no-go decision | Leadership, DRI, compliance, QA | Scale / redesign / stop |

---

## Go / No-Go Gates

| Gate | Date / Trigger | Pass Criteria | Fail Response |
|---|---|---|---|
| Gate 1 | End of Week 4 live pilot | Stable request flow, telemetry works, no major compliance issues, repeatable run history exists | Stop expansion, fix substrate and governance |
| Gate 2 | End of Week 8 | Primary metric improving, manual touches declining, QA stable, exception handling manageable | Narrow scope, redesign capability split |
| Gate 3 | End of Week 12 | Clear baseline improvement, leadership confidence, acceptable reliability and compliance profile | Do not scale beyond pilot |

---

## Rate of Improvement Tracking

| Period | Metric Value | Improvement vs. Baseline | Notes |
|---|---|---|---|
| Baseline | TBD | — | Measure before any pilot changes |
| Week 1 | | | |
| Week 2 | | | |
| Week 4 | | | Gate 1 review |
| Week 8 | | | Gate 2 review |
| Week 12 | | | Gate 3 review |

---

## Open Evaluation Risks

1. The current organization may not have clean enough baseline data to measure the pilot without an upfront instrumentation sprint.
2. If the pilot scope is too broad, evaluation signals will be noisy and leadership will not learn the right lesson.
3. If management behavior does not change, the new system may still inherit the old coordination delays even with agents in the loop.
