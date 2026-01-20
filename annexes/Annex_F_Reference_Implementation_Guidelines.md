# Annex F — Reference Implementation Guidelines (Deferred)

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
- Example **interface categories** and illustrative message schemas
- Versioning and lifecycle guidelines for interfaces and artifacts
- Publication gating: when and how reference code should be released

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

1. **Implements at least one UCPIS interface contract** (schema + semantics)
2. Demonstrates at least one **round-trip flow** (e.g., command → state change → ack)
3. Produces **logs/events** sufficient for replay and audit
4. Is runnable in a minimal environment (local container or simple host runtime)
5. Is **clearly labeled non-normative** and includes a “what this proves / what it does not” section

### F.3.3 Recommended Starter MVUEs

- **MVUE-A:** Simulated device (L1) + orchestrator (L3) + event log replay
- **MVUE-B:** Task assignment (L3→L2) + Class-L constrained acknowledgement (L2→L3)
- **MVUE-C:** Multi-cell orchestration mock (L3↔L3) demonstrating policy propagation

---

## F.4 Canonical Interface Categories (Illustrative)

UCPIS is interface-first. Reference implementations should organize interfaces into a small set of categories.

| Category | Direction | Layer(s) | Purpose |
|---|---:|---|---|
| **Physical State** | L1 → L3 | 1→3 | Telemetry and status of devices/cells |
| **Command / Actuation** | L3 → L1 | 3→1 | Controlled actuation requests |
| **Task Assignment** | L3 → L2 | 3→2 | Human-mediated work instruction |
| **Acknowledgement / Completion** | L2 → L3 | 2→3 | Human feedback, confirm/abort/escalate |
| **Policy / Governance** | L3 ↔ L3 | 3↔3 | Constraints, roles, permissions, audit framing |
| **Audit / Event Log** | All → Log | all | Replayable events and traceability |

> These categories are **illustrative** and may evolve; they are used here to structure MVUE artifacts.

---

## F.5 Interface Contract Conventions (Recommended)

Reference implementations should adopt lightweight, consistent conventions.

### F.5.1 Required Envelope Fields (Recommended)

All messages SHOULD include:

- `ucpis_version`: semantic version of UCPIS interface envelope
- `interface_id`: stable identifier, e.g., `task.assignment.v1`
- `message_id`: UUID for traceability
- `timestamp`: ISO-8601
- `source`: component identifier (device/orchestrator/hmi)
- `target`: intended recipient identifier (optional for pub/sub)
- `correlation_id`: links related message chains (optional but recommended)

### F.5.2 Capability Scoping

Interfaces SHOULD include explicit capability constraints:

- `human_class` where relevant (Class-L / Class-M / Class-H)
- `allowed_actions` for constrained UIs
- `constraints` blocks (timeouts, interlocks, prerequisites)
- explicit “escalate” paths rather than unconstrained overrides

---

## F.6 Illustrative Schemas (Non-Normative Examples)

The following examples are **illustrative**. Implementers may choose JSON Schema, OpenAPI, AsyncAPI, Protobuf, or other formats.

### F.6.1 Task Assignment (L3 → L2) — Class-L Constrained

```json
{
  "ucpis_version": "1.0.0",
  "interface_id": "task.assignment.v1",
  "message_id": "uuid",
  "timestamp": "2026-01-19T00:00:00Z",
  "correlation_id": "uuid",
  "human_class": "Class-L",
  "task_id": "uuid",
  "workcell_id": "cell-01",
  "instructions": [
    {"step": 1, "text": "Pick part from bin A"},
    {"step": 2, "text": "Place part on fixture"},
    {"step": 3, "text": "Press CONFIRM when seated"}
  ],
  "constraints": {
    "timeout_sec": 300,
    "allowed_actions": ["confirm", "abort", "escalate"],
    "safety_interlocks_required": true
  }
}
