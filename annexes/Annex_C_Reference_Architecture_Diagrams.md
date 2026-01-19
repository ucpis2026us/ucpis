# Annex C — Reference Architecture

This annex describes the reference architecture for the Universal Cyber-Physical
Interoperability Stack (UCPIS), including system layers, interfaces, and integration
principles. It is technology-agnostic and intended to guide implementation without
mandating specific vendors or products.

---

## C.4 Human Integration by Autonomy Class

UCPIS explicitly defines how human actors integrate into the stack based on
demonstrated autonomy and responsibility. Human Autonomy Classes are defined in
Annex A.12.

---

### C.4.1 Class-L Integration

**Primary Layer**
- Layer 2 — Interaction & Coordination

**Interface Characteristics**
- Checklist-driven workflows
- Highly constrained user interfaces
- Guided task execution
- No discretionary access to unsafe system states

**Architectural Rule**
Class-L actors must not be relied upon for hazard detection, policy judgment,
or system recovery.

---

### C.4.2 Class-M Integration

**Primary Layers**
- Layer 2, with constrained access to Layer 3

**Interface Characteristics**
- Supervisory dashboards
- Escalation and exception-handling consoles
- Limited override authority
- Strong logging and auditability

**Architectural Rule**
Class-M actors may intervene operationally but may not redefine system policy
or architectural constraints.

---

### C.4.3 Class-H Integration

**Primary Layer**
- Layer 3 — Policy, Architecture, and Governance

**Interface Characteristics**
- System modeling and simulation tools
- Policy definition and constraint-design interfaces
- Governance and oversight surfaces
- Non-real-time interaction with execution layers

**Architectural Rule**
Class-H authority shapes downstream system behavior through structure and policy,
not through continuous direct control.

---

### C.4.4 Class-X Integration (Reserved)

**Layer Coverage**
- Cross-layer, subject to UCPIS constraints

**Status**
Class-X integration is documented for awareness only in v1.3.
No normative architectural or governance requirements are defined.