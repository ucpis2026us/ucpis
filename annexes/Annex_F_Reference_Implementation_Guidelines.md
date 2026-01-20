# Annex F — Reference Implementation Guidelines (Deferred)
**UCPIS Version:** v1.4  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

**Attribution Required:**  
Michael James Malecek (2026)

**Canonical Repository:**  
https://github.com/ucpis2026us

**Contact:**  
ucpis2026@gmail.com

---

**Document:** Universal Cyber-Physical Interoperability Stack (UCPIS)  
**Annex:** F  
**Title:** Reference Implementation Guidelines  
**Status:** **DEFERRED / RESERVED** (to be published after “UCPIS-Executable” artifacts exist)  
**Normative Level:** **INFORMATIVE (NON-NORMATIVE)**  
**Security Note:** This annex specifies **no normative security controls**. Any security guidance, if later produced, is out of scope for this annex and must be published separately.

---

## F.0 Purpose and Rationale

This annex defines **non-normative reference implementation guidelines** for UCPIS—intended to prove that UCPIS interfaces can be **executed, tested, and evolved** without prescribing a full factory stack or endorsing specific vendors or products.

UCPIS reference implementations are designed to be:

- **Minimal:** demonstrate interfaces with the smallest viable executable artifacts
- **Replaceable:** support multiple independent implementations
- **Vendor-neutral:** avoid reliance on proprietary stacks
- **Testable:** enable deterministic testing, replay, and conformance checks
- **Non-binding:** educational and illustrative, not required for adoption

> **Key boundary condition:** Reference implementations are **not a full factory stack**—only “enough code to make the architecture testable.”

---

## F.1 Scope

This annex covers:

- A definition of **Minimum Viable UCPIS-Executable (MVUE)**
- Canonical **reference harness** concepts
- Example **interface categories** and illustrative message-field conventions
- Versioning and lifecycle guidelines for interfaces and artifacts
- Publication gating: when and how reference code should be released
- 
- Reference implementations MAY include environmental or biological interaction
signals (e.g., presence detection, exclusion zone events) as external inputs.

Such inputs are treated as non-agent environmental conditions, consistent with
Annex A.13 and Annex C, and do not imply authority, intent, or accountability.


This annex does **not** cover:

- Normative security controls, assurance levels, or compliance mandates
- Performance SLAs or production hardening requirements
- Full robotics/PLC firmware, full MES/ERP implementations, or AI controllers
- Vendor-specific deployment recipes

---

## F.2 Relationship to the UCPIS Reference Architecture

UCPIS reference implementations must reflect the canonical UCPIS stack model:

- **Layer 1 — Physical:** machines, robots, sensors, actuators, energy/logistics interfaces
- **Layer 2 — Human Interface / Mediation:** constrained HMIs, guided flows, task confirmation surfaces
- **Layer 3 — Cyber / Control / Governance:** orchestration, policy, scheduling, audit, coordination logic

Reference implementations SHOULD reflect that UCPIS systems operate within a broader
environmental context. Non-human biological entities and environmental conditions,
where modeled, are treated as external, non-deterministic inputs rather than actors
or participants in control logic.

### F.2.1 Human-Class–Aware Interface Binding

UCPIS reference implementations must preserve the architecture’s human participation constraints:

- **Class-L (Low-Autonomy Operators):** Layer 2 only; constrained actions and guided steps
- **Class-M (Mid-Autonomy Technicians / Supervisors):** Layer 2 plus bounded Layer 3 consoles
- **Class-H (High-Autonomy Architects / Leaders):** deep Layer 3 (policy, governance, architecture)

Reference code should demonstrate that **interfaces are capability-scoped** and that **UI surfaces are constrained by class** (e.g., a Class-L HMI cannot expose unrestricted actuations).

---

## F.3 Minimum Viable UCPIS-Executable (MVUE)

### F.3.1 Definition

**MVUE** (Minimum Viable UCPIS-Executable) is:

> The smallest executable artifact (or set of artifacts) that exercises UCPIS interfaces end-to-end across at least two layers, producing observable, testable behavior, without implementing a full factory stack.

### F.3.2 Minimum Criteria

An artifact qualifies as MVUE if it:

1. **Implements at least one UCPIS interface contract** (field requirements + semantics)
2. Demonstrates at least one **round-trip flow** (e.g., command → state change → acknowledgement)
3. Produces **logs/events** sufficient for replay and audit
4. Is runnable in a minimal environment (local container or simple host runtime)
5. Is **clearly labeled non-normative** and includes a “what this proves / what it does not” section

### F.3.3 Recommended Starter MVUEs

- **MVUE-A:** Simulated device (L1) + orchestrator (L3) + event log replay
- **MVUE-B:** Task assignment (L3→L2) + Class-L constrained acknowledgement (L2→L3)
- **MVUE-C:** Multi-cell orchestration mock (L3↔L3) demonstrating policy propagation
- **MVUE-D (Optional):** Environmental interaction mock (e.g., simulated presence
  event) triggering a safe-state transition or task pause, demonstrating that
  biological or environmental signals influence system behavior without introducing
  agency or authority.

---

## F.4 Canonical Interface Categories (Illustrative)

UCPIS is interface-first. Reference implementations should organize interfaces into a small set of categories.

| Category | Direction | Layer(s) | Purpose |
|---|---:|---|---|
| **Physical State** | L1 → L3 | 1→3 | Telemetry and status of devices/cells |
| **Command / Actuation** | L3 → L1 | 3→1 | Controlled actuation requests |
| **Task Assignment** | L3 → L2 | 3→2 | Human-mediated work instruction |
| **Acknowledgement / Completion** | L2 → L3 | 2→3 | Human feedback (confirm/abort/escalate) |
| **Policy / Governance** | L3 ↔ L3 | 3↔3 | Constraints, roles, permissions, audit framing |
| **Audit / Event Log** | All → Log | all | Replayable events and traceability |

> These categories are **illustrative** and may evolve; they are used here to structure MVUE artifacts.

---

## F.5 Interface Contract Conventions (Recommended)

Reference implementations should adopt lightweight, consistent conventions.

### F.5.1 Recommended Message Envelope Fields

All messages SHOULD include:

- `ucpis_version` — semantic version of the UCPIS envelope
- `interface_id` — stable identifier (example: `task.assignment.v1`)
- `message_id` — unique identifier for traceability
- `timestamp` — ISO-8601 time
- `source` — component identifier (device/orchestrator/hmi)
- `target` — intended recipient identifier (optional for pub/sub)
- `correlation_id` — links related message chains (optional but recommended)

### F.5.2 Capability Scoping

Interfaces SHOULD include explicit capability constraints:

- `human_class` where relevant (Class-L / Class-M / Class-H)
- `allowed_actions` for constrained UIs
- `constraints` blocks (timeouts, interlocks, prerequisites)
- explicit “escalate” paths rather than unconstrained overrides

---

## F.6 Illustrative Message Patterns (Non-Normative)

This section provides **field-level patterns** without embedding full structured examples.

### F.6.1 Task Assignment (L3 → L2)

A task assignment message SHOULD include:

- `task_id`
- `workcell_id` (or `location_id`)
- `human_class` (when routed to human mediation)
- `instructions` as an ordered list of steps
- `constraints` including:
  - `timeout_sec`
  - `allowed_actions` (for Class-L: typically confirm/abort/escalate)
  - any required preconditions (interlocks, required device state)

### F.6.2 Acknowledgement / Completion (L2 → L3)

An acknowledgement message SHOULD include:

- `task_id`
- `actor` (role- or class-based identifier)
- `result` (confirm / abort / escalate)
- optional `notes`
- optional `observations` (e.g., anomaly flag, assistance required)

### F.6.3 Physical State (L1 → L3)

A device state message SHOULD include:

- `device_id`
- `workcell_id`
- `state` (ready / running / fault / offline, etc.)
- optional `mode` (manual / auto / maintenance)
- optional `telemetry` (key-value)
- optional `faults` list

### F.6.4 Command / Actuation (L3 → L1)

A command message SHOULD include:

- `device_id`
- `command` name
- `params` (command parameters)
- `constraints` (required state, timeout, safety interlocks, etc.)

---

## F.7 Reference Harness Architecture (Recommended)

Reference implementations SHOULD be structured as a small harness with clear seams.

### F.7.1 Recommended Components

- **L1 Simulator(s):** deterministic device and sensor simulators (seedable)
- **L3 Orchestrator Stub:** minimal scheduler / state machine / dispatcher
- **L2 HMI Stub:** constrained UI surfaces with action rails (confirm/abort/escalate)
- **Event Bus (Optional):** in-memory or lightweight broker
- **Event Log:** append-only record of message envelopes (for replay/testing)
- **Test Runner:** executes scripted scenarios and checks assertions

### F.7.2 Required Test Properties (Recommended)

- **Determinism:** repeatable scenarios using fixed seeds
- **Replayability:** ability to replay event logs and reproduce outcomes
- **Observability:** structured logs with correlation IDs
- **Failure injection:** at least one fault scenario (timeouts, invalid state, operator abort)

---

## F.8 Versioning and Lifecycle Guidelines

### F.8.1 Interface Versioning

- Interface identifiers SHOULD embed major version: `*.v1`, `*.v2`
- Backward compatible changes SHOULD increment minor versions (if used)
- Breaking changes SHOULD create a new interface ID or major version

### F.8.2 Experimental Interfaces

- Experimental interfaces MUST be clearly labeled (example: `*.exp.v1`)
- Experimental interfaces MUST include migration notes (even if brief)

### F.8.3 Deprecation

- Interfaces SHOULD specify a deprecation window and replacement interface
- Reference implementations SHOULD keep at least one scenario demonstrating migration

---

## F.9 Conformance Position (Non-Normative)

This annex does not define formal conformance requirements. However, reference artifacts SHOULD include:

- A statement of which interface IDs are exercised
- A list of scenarios and expected outcomes
- A machine-readable event log output for each scenario
- A mapping of scenarios to layers (L1/L2/L3)

---

## F.10 Publication and Governance Gate

Because reference implementations can prematurely “lock in” assumptions, publication SHOULD occur only after:

1. **At least two independent implementations exist** OR one implementation plus an independent review
2. Interfaces have documented semantics (not only field lists)
3. Governance review confirms the implementation is non-normative and vendor-neutral
4. The artifacts clearly state: “This proves interface viability; it is not a production reference stack.”

---

## F.11 What This Annex Enables (and What It Prevents)

### Enables

- Fast, low-risk pilot demonstrations
- Early ecosystem tooling (schemas, simulators, harnesses)
- Clear interface discussions without vendor lock-in
- Repeatable validation for adopters and reviewers

### Prevents

- Premature standard capture by a single reference codebase
- “Accidental productization” of UCPIS
- Security or safety mandates creeping in informally

---

## F.12 Appendix — Glossary

- **UCPIS:** Universal Cyber-Physical Interoperability Stack
- **Reference Architecture:** the canonical layer model and interface-first approach
- **MVUE:** Minimum Viable UCPIS-Executable (smallest runnable proof)
- **Interface Contract:** field requirements + semantics + versioning identity
- **Harness:** minimal environment used to execute and test scenarios

---
**End of Annex F**
