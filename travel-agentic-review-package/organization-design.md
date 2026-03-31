# Organization Design Recommendation

**Subject:** How to reorganize the India travel production organization for an agentic-first model

---

## Executive Position

The organization should not reorganize by replacing each current team or role with a same-named “agent.”

That approach will preserve:

- the current silo structure
- the current coordination tax
- the current exception bottlenecks
- the current ambiguity around ownership

Instead, the organization should reorganize around **shared capabilities**, **problem ownership**, and **human edge judgment**.

---

## What the Current Proposal Gets Right

The document correctly recognizes that these functions matter:

- intake
- feasibility
- scripting
- extraction
- monitoring
- transformation
- QA
- delivery
- support
- compliance

These are real responsibilities. The problem is not the list. The problem is treating each one as an autonomous agent/team boundary by default.

---

## Design Principles for the New Organization

1. Build around reusable capabilities, not vertical silos.
2. Keep humans at the edge for novel, high-risk, and ambiguous cases.
3. Use DRIs for cross-cutting business problems, not permanent managerial relays.
4. Make the company’s operational memory machine-readable so agents can coordinate through state, not meetings.
5. Scale only what is measurable.

---

## Proposed Human Role Model

### 1. Individual Contributors

Deep specialists who build and operate one capability area:

- source intelligence
- orchestration and infra
- QA and transformation
- delivery and support
- governance and compliance

### 2. Directly Responsible Individuals

Time-boxed owners of cross-cutting outcomes, for example:

- reduce request lead time for Workflow A by 50%
- cut extraction failures for critical sources by 30%
- reduce manual interventions in onboarding

DRIs should have pull authority across capability teams.

### 3. Player-Coaches

Senior builders who both ship and develop people:

- lead pilot design
- mentor ICs
- teach agentic literacy
- review exceptions and architecture decisions

### 4. Human Edge Reviewers

Humans who remain in the loop for:

- source onboarding with uncertainty
- stealth / anti-bot / regulatory-sensitive methods
- client-specific exceptions
- unusual quality anomalies
- sensitive data and secret boundary decisions

This is where SMEs belong.

---

## Proposed Team Structure

### A. Intake and Orchestration Team

Owns:

- request normalization
- queueing
- prioritization
- workflow orchestration
- run ledger and observability

This is not a “Master Agent team.” It is the control plane.

### B. Source Intelligence and Onboarding Team

Owns:

- source feasibility
- script reuse vs. new development decisions
- source-specific knowledge base
- onboarding rules and runbooks

This team converts tribal knowledge into reusable system memory.

### C. Execution Platform and Reliability Team

Owns:

- extraction runtime
- scaling
- proxies
- infra automation
- retries
- recovery
- reliability engineering

This combines parts of Extraction, Production, and Sentinel.

### D. Quality, Transformation, and Delivery Team

Owns:

- schema mapping
- data transformation
- QA checks
- delivery packaging
- delivery confirmation
- delivery-side issue handling

This combines Transformation, QA, Delivery, and some Support functions.

### E. Governance, Compliance, and Human Edge Team

Owns:

- approval matrix
- compliance policies
- audit and secret boundaries
- exception review
- sensitive-case escalation
- training and awareness

This team should be small but authoritative.

---

## How the Proposed 14 Agents Should Be Reframed

| Proposed Agent | Better Interpretation |
|---|---|
| Master Agent | Control plane / orchestration service, not a human-like master role |
| Assessment Agent | Intake capability |
| Scheduling Agent | Queueing / scheduling service inside control plane |
| Onboarding Agent | Source intelligence and onboarding workflow |
| Scripting Agent | Source intelligence + engineering capability |
| Extraction Agent | Execution runtime capability |
| Production Agent | Too broad; split between execution control, infra, and exception routing |
| Sentinel Agent | Monitoring and reliability capability |
| Specialist / SME Agent | Human edge function, not a broad autonomous agent |
| Transformation Agent | Post-processing capability |
| QA Agent | Quality rules and exception routing capability |
| Delivery Agent | Delivery pipeline capability |
| Support Agent | Human + tooling support function |
| Compliance Agent | Governance and approval function |

---

## Recommended Transition

### First 30 Days

- Name one pilot DRI
- Keep current org in place
- Stand up a cross-functional pilot squad from the proposed five capability groups
- Do not announce a broad org flattening yet

### 31-90 Days

- Run the pilot with weekly evidence reviews
- Start shifting recurring work into shared capability ownership
- Start using DRI rotations for defined business problems

### 90-180 Days

- If the pilot works, move from vertical-silo management to capability leadership
- Convert some managers into player-coaches or DRIs
- Narrow purely coordinative roles that no longer add differentiated value

---

## What Leadership Should Say Clearly

1. This is not a headcount relabeling exercise.
2. We are not automating every role as-is.
3. We are building shared intelligence and reducing coordination waste.
4. Human judgment remains mandatory for sensitive, novel, and ambiguous work.
5. Promotions and role evolution will favor builders, owners, and coaches.

---

## Bottom Line

The India organization should reorganize around **capabilities + DRIs + player-coaches**, not around a one-to-one mapping of today’s teams into 14 agents.

That is the difference between:

- digitizing the current hierarchy

and

- building a genuinely agentic operating system.
