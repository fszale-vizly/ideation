# Gap Analysis

**Review Target:** Travel Production Pipeline / Proposed Agentic Framework  
**Date:** 2026-03-31  
**Owner / Team:** Senior leadership and travel production organization in India

---

## Desired Outcome

**Outcome statement:**

> Create an agentic-first travel production system that cuts lead time and manual coordination materially, increases first-pass quality, improves resilience, and preserves strong human control over exceptions, client commitments, and compliance-sensitive actions.

**Primary metric:** Median request-to-delivery lead time  
**Target value:** 40-60% reduction for the pilot workflow  
**Time horizon:** 90 days for pilot proof, 180 days for broader operating-model decision

---

## Current State

### Workflow / Product Today

The current production process is organized into requirement, production, and delivery phases. Responsibilities are distributed across human teams handling request intake, scheduling, feasibility checks, scripting, extraction, monitoring, QA, delivery, support, and compliance. The proposed future state mostly maps each responsibility to a corresponding “agent.”

### Current Baseline

| Metric | Current Value | Evidence Source | Confidence |
|---|---|---|---|
| Median request-to-delivery lead time | Not instrumented in the proposal | Missing from source document | Low |
| First-pass QA pass rate | Not instrumented in the proposal | Missing from source document | Low |
| Manual touches per request | Not instrumented in the proposal | Missing from source document | Low |
| New source onboarding lead time | Not instrumented in the proposal | Missing from source document | Low |
| Extraction success / retry rate | Not instrumented in the proposal | Missing from source document | Low |

### Real vs. Assumed vs. Simulated

| Area | Real | Assumed | Simulated | Notes |
|---|---|---|---|---|
| Current human workflow | Yes | No | No | Clearly described in the PDF |
| 14-agent future-state system | No | Yes | No | Conceptual only |
| Shared company world model | No | Yes | No | Not described as a concrete system |
| Customer / usage world model | No | Yes | No | Not described |
| Self-improvement loop | No | Yes | No | Implied but not designed |
| Governance / autonomy model | No | Yes | No | Compliance is named, but the control system is not defined |

---

## Target State

| Dimension | Target State | Acceptance Signal |
|---|---|---|
| Outcome | Faster, lower-toil, higher-quality delivery for a pilot workflow | Lead time and manual touches fall materially without quality drop |
| Process | Capability-based, not silo-based, with explicit exception routing | Shared control plane and repeatable flow across pilot requests |
| Technology | Durable orchestration, shared state, knowledge repos, retrieval, audit, and eval | Runs are traceable, restartable, measurable, and reviewable |
| Governance | HITL gates, approvals, secrets boundaries, compliance controls, kill switches | High-risk actions remain gated and auditable |
| Measurement | Baseline, leading indicators, review cadence, go/no-go gates | Leadership can decide whether to scale the pilot with evidence |

---

## Gap Map

| Gap Area | Current State | Target State | Gap | Severity | What Must Change |
|---|---|---|---|---|---|
| Outcome clarity | “Optimize cost / scale / efficiency” is implied | One explicit 90-day pilot outcome with measurable targets | No decision-grade objective exists yet | Critical | Define one pilot value claim and tie it to 3-5 metrics |
| Stakeholder alignment | Roles are listed, but not future decision rights | IC / DRI / player-coach model with explicit authority | Org change model is absent | High | Define who owns pilot decisions, approvals, and operating cadence |
| Process readiness | Current process is documented | Future-state process should be redesigned around capabilities | Proposed agents mostly mirror current teams | Critical | Collapse role-mirroring into a smaller set of reusable capabilities |
| Technical readiness | Script repos, checklists, and process knowledge likely exist, but are fragmented | Shared control plane, run ledger, source knowledge, retrieval, evals | Core substrate is undefined | Critical | Build durable orchestration, state, and knowledge systems before broad autonomy |
| Data / memory readiness | “Knowledge repo” is mentioned for some agents | Company world model and usage/customer signals should drive learning | No cross-system memory or retrieval design exists | Critical | Define what artifacts become machine-readable memory and how agents retrieve them |
| Evaluation readiness | No baseline or stage gates | Evidence-based pilot with go/no-go checkpoints | Leadership cannot distinguish success from motion | Critical | Add an evaluation plan before implementation |
| Governance / HITL | Compliance is named as an agent | Approval matrix, autonomy ladder, audit, kill switches, secrets boundaries | Control system is missing | High | Define hard boundaries for source onboarding, credentials, stealth methods, sensitive data, and client-impacting delivery |
| Reliability / durability | Monitoring and retries are mentioned | Crash recovery, state persistence, replayability, root-cause feedback | The design is operationally incomplete | High | Add a durable task/run store, checkpoints, and incident feedback loop |
| Exception handling | SME agent is a catch-all | Human-edge handling should be narrow, structured, and learnable | Exceptions risk becoming a new bottleneck | High | Treat SME as a human edge function and feed exception learnings back into the system |
| Organization design | Article context suggests flattening and capability teams | Capability platform with rotating DRIs and player-coaches | Current proposal leaves the existing silo model mostly intact | High | Reorganize around shared capabilities and problem ownership, not vertical queues |

---

## Existing Assets to Reuse

| Asset | Why It Matters | Reuse Recommendation |
|---|---|---|
| Existing script repository | Encodes source-specific extraction knowledge | Convert into a source intelligence catalog with versioning and failure history |
| Current process checklists | Already capture business logic and QA expectations | Turn into machine-readable validation rules and onboarding checklists |
| Delivery summaries / billing logs | Early operational telemetry | Use as seeds for run-level metrics and cost tracking |
| Existing request channels (Shop Manager, API, email) | Real intake surface already exists | Normalize them through one request schema instead of replacing them immediately |
| Senior operators / SMEs | Carry tacit exception knowledge | Treat them as human-edge reviewers and trainers during the pilot |

---

## Assumptions, Unknowns, and Risks

### Assumptions

1. The organization already has enough historical run/log/checklist data to seed a useful company world model.
2. Leadership is willing to validate one workflow deeply before pursuing a broad org-wide rollout.

### Unknowns Blocking Confidence

1. Which pilot workflow has the cleanest measurable value claim.
2. How much of current operational knowledge is actually codified versus held by people.
3. What compliance, contract, and client restrictions apply to stealth techniques, credentials, and data handling.

### Material Risks

1. The org implements a 14-agent architecture without solving shared state, measurement, and governance first.
2. “Master Agent” becomes a central decision bottleneck and single point of operational fragility.
3. The pilot is judged on excitement or demos rather than operational improvement and reliability.

---

## Highest-Value Gap to Close First

> Define one pilot workflow, baseline its current performance, and redesign it around 5-6 shared capabilities plus explicit HITL gates instead of implementing all 14 proposed agents.
