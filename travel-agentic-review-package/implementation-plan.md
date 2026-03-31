# Implementation Plan

**Initiative:** Travel Production Agentic-First Pilot and Operating Model Redesign  
**Date:** 2026-03-31  
**Owner:** India senior leadership with a named pilot DRI

---

## Objective and Scope

**Desired outcome:**

> Prove that a capability-based agentic production system can materially reduce turnaround time and manual coordination for one travel workflow without degrading quality, compliance, or delivery reliability.

**In scope:**

- One high-volume or high-pain travel workflow
- Shared request schema and orchestration
- Source intelligence and knowledge capture for the pilot
- QA, compliance, and delivery controls for the pilot
- Baseline and evaluation instrumentation

**Out of scope:**

- Broad rollout across all travel sources
- Immediate replacement of all current teams and roles
- Fully autonomous exception handling
- Full org restructuring before pilot proof

---

## Delivery Strategy

**Core value claim to validate first:**

> A smaller capability-based architecture with durable state and explicit HITL can outperform the current manually coordinated flow for one travel workflow.

**Depth-before-breadth principle:**

> Validate one workflow end to end with real data, real telemetry, and real human approvals before scaling the model across functions or verticals.

**Highest-value first slice:**

> Intake → feasibility/source knowledge → extraction execution → QA → delivery for one recurring request pattern.

---

## Proposed Capability Model

Do not start with 14 autonomous agents. Start with these six capability domains:

1. **Intake and Request Normalization**
   - Ingest requests from Shop Manager, API, and email
   - Validate required fields
   - Normalize into one request schema

2. **Source Intelligence and Onboarding**
   - Maintain source-specific extraction knowledge
   - Determine reuse vs. new development
   - Track constraints, blockers, and known mitigations

3. **Execution Control Plane**
   - Orchestrate runs, queues, retries, checkpoints, and infrastructure
   - Persist task/run state
   - Capture logs and cost telemetry

4. **Transformation and QA**
   - Apply mappings and format conversions
   - Run validations, rule checks, and source cross-checks
   - Route anomalies back through structured exception handling

5. **Delivery and Support**
   - Package and deliver outputs
   - Confirm receipt and integrity
   - Manage delivery-side issues

6. **Governance and Compliance**
   - Enforce secret boundaries, approvals, auditability, and compliance rules
   - Human-gate high-risk actions

Treat “SME” as a **human edge function**, not a fully autonomous agent.

---

## Immediate / Soon / Later Plan

| Horizon | Goal | Key Work | Acceptance Criteria | Owner |
|---|---|---|---|---|
| Immediate (0-30 days) | Name the pilot and instrument the current state | Select one workflow, baseline current performance, define request schema, define capability map, define HITL gates, identify existing knowledge sources | Pilot scope, metrics, governance rules, and architectural slice approved by leadership | Pilot DRI |
| Soon (31-90 days) | Build and run the pilot | Implement control plane, source intelligence store, run ledger, QA checks, delivery validation, and weekly review cadence | Pilot handles real requests with measurable telemetry and stable operator oversight | Pilot DRI + capability leads |
| Later (91-180 days) | Decide whether to scale | Compare pilot vs. baseline, harden shared capabilities, redefine org roles, expand only if metrics justify it | Leadership has evidence-based scale / redesign decision | Leadership + DRIs |

---

## Workstreams

| Workstream | Why It Matters | Dependencies | Risk Level | Status |
|---|---|---|---|---|
| Pilot selection and baseline | Without this, everything else is theater | Leadership alignment | High | Not started |
| Shared request schema | Prevents intake chaos and downstream ambiguity | Pilot selection | Medium | Not started |
| Source intelligence repository | Converts tribal knowledge into reusable machine context | Access to scripts, checklists, and operator notes | High | Not started |
| Durable orchestration and run ledger | Required for reliability, audit, and learning | Infra and engineering capacity | High | Not started |
| QA and delivery controls | Prevents speed gains from creating bad outputs | Existing QA logic and delivery rules | High | Not started |
| Governance and secrets boundaries | Prevents unsafe autonomy | Compliance and security alignment | High | Not started |
| Operating cadence and DRI model | Required to prevent old hierarchy from resurfacing | Leadership sponsorship | Medium | Not started |

---

## Governance and Decision Points

| Decision | Trigger | Owner | Needed Evidence | Go / No-Go Rule |
|---|---|---|---|---|
| Approve pilot workflow | Before build starts | Senior leadership | Pain level, volume, baseline measurability | No pilot without measurable outcome |
| Approve autonomy boundaries | Before real requests are processed | Compliance + leadership | Approval matrix, audit design, secret boundaries | No high-risk autonomy without explicit controls |
| Continue beyond initial build | End of first 4 weeks of live pilot | Pilot DRI + leadership | Stable runs, basic telemetry, no severe compliance issues | Stop if system is unstable or unmeasured |
| Expand beyond one workflow | End of 90-day pilot | Leadership | Measured improvement vs. baseline | Do not scale if no clear improvement |

---

## Risks and Mitigations

| Risk | Likelihood | Impact | Mitigation | Escalation Trigger |
|---|---|---|---|---|
| Team tries to implement all 14 agents at once | High | High | Freeze scope to one workflow and six capabilities | New work requests outside pilot appear before Gate 1 |
| Shared state and telemetry are deferred | High | High | Make run ledger and instrumentation part of Phase 1 | Pilot runs cannot be replayed, traced, or measured |
| SME queue becomes the new bottleneck | Medium | High | Limit SME to edge cases and convert learnings into source intelligence updates | >20% of pilot requests require SME intervention |
| Compliance is treated as advisory instead of blocking | Medium | High | Define hard approval gates and secret isolation before live use | Any credential or sensitive-data incident |
| Leadership judges pilot by demo quality instead of metrics | Medium | High | Pre-agree primary metric, supporting metrics, and gates | Scale discussions start without baseline comparison |

---

## Definition of Done

1. One travel workflow is running through a shared capability-based pilot with durable state, QA, delivery validation, and governance controls.
2. The pilot has measured baseline vs. current performance on agreed outcome and leading metrics.
3. Leadership can make an evidence-based decision to scale, redesign, or stop.
