# Annex C — Reference Architecture

**Status:** Informative / Non-Normative  
**UCPIS Version:** v1.4  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

**Attribution Required:**  
Michael James Malecek (2026)

**Canonical Repository:**  
https://github.com/ucpis2026us

**Contact:**  
ucpis2026@gmail.com

---

This annex describes the reference architecture for the Universal Cyber-Physical
Interoperability Stack (UCPIS), including system layers, interfaces, and integration
principles. It is technology-agnostic and intended to guide implementation without
mandating specific vendors or products.

UCPIS models cyber-physical systems as operating within a broader **socio-technical
and ecological environment**, where human actors, automated systems, and biological
entities coexist and interact through defined constraints and interfaces.

---

## C.3 Environmental and Biological Context (Informational)

UCPIS architectures may operate in environments containing non-human biological
entities, including wildlife and domesticated animals. These entities form part of
the operational context in which cyber-physical systems must function safely and
predictably.

Non-human biological actors are defined in Annex A.13 and are treated within the
architecture as **environmental participants**, not system agents.

Architectural considerations include:
- Presence detection and monitoring
- Safety zoning and exclusion boundaries
- Adaptive behavior in response to biological movement
- Non-deterministic environmental interaction

No authority, decision rights, or accountability are assigned to non-human biological
entities.

---

## C.4 Human Integration by Autonomy Class

UCPIS explicitly defines how human actors integrate into the stack based on
demonstrated autonomy and responsibility. Human Autonomy Classes are defined in
Annex A.12.

Human actors remain the **only biological entities** granted system authority,
policy influence, or governance roles.

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
Class-X integration is documented for awareness only in UCPIS v1.4.
No normative architectural or governance requirements are defined.

---

## C.5 Non-Human Biological Interaction Model (Informational)

Non-human biological actors, including wildlife, may interact with UCPIS-enabled
systems through proximity, movement, or environmental impact.

Within the reference architecture:
- Wildlife is treated as a **dynamic environmental factor**
- Interactions are mediated through sensing, containment, or adaptive control
- Behavioral unpredictability is assumed by default

**Architectural Principles**
- Systems SHALL NOT assume symbolic intent or compliance from animals
- Systems SHALL prioritize safety and avoidance over optimization
- All responses to biological interaction are governed by human-defined policy
  and automated control logic

**Examples (Non-Exhaustive)**
- Wildlife detection triggering safe slow-down or shutdown states
- Exclusion zones enforced through physical or behavioral deterrence
- Environmental monitoring informing system scheduling or routing

This model preserves biological dignity by avoiding coercive control while ensuring
human safety and system integrity.

---

### End of Annex C
