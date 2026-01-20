# Annex A — Definitions, Terminology, and Taxonomy

**UCPIS Version:** v1.4  
**Status:** Public, Normative (with Informational subsections)  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

**Attribution Required:**  
Michael James Malecek (2026)

**Canonical Repository:**  
https://github.com/ucpis2026us

**Contact:**  
ucpis2026@gmail.com

---

This annex defines the canonical terms and taxonomies used throughout the **Universal Cyber-Physical Interoperability Stack (UCPIS)**, establishing the vocabulary surface necessary for interoperability, authority assignment, safety modeling, and cyber-physical participation.

Unless explicitly stated otherwise, definitions in this annex are **normative**. Sections marked *Informational* are provided for clarity and future extensibility.

---

# A.1 Core Interface & Architecture Terms

- **Interface** — A defined boundary through which systems exchange information or control.
- **Constraint** — A real-world limitation shaping allowable behavior.
- **Interoperability** — The ability of heterogeneous systems to exchange meaningfully interpretable information.
- **Layer** — A conceptual separation of concerns within the stack.
- **Contract Boundary** — A formally defined surface where obligations, permissions, and constraints are specified and enforced.
- **Typed Interface** — An interface exposing a specific set of actions, data types, or authority levels.
- **Class-Scoped Interface** — An interface exposing affordances according to actor class.
- **Constraint-Aware Interface** — An interface incorporating physical, safety, timing, thermal, electrical, or institutional constraints.
- **Participation Contract** — The defined set of actions, roles, and constraints through which a system actor participates in a cyber-physical environment.
- **State Model** — The canonical representation of observed or inferred system state.
- **Workcell** — A bounded physical or logical unit of task execution within a cyber-physical environment.
- **Operational Context** — The conditions under which a system is deployed, including physical, temporal, and institutional constraints.
- **Control Surface** — The set of actions or commands through which a system may influence another.
- **Sensing Surface** — The set of observable signals through which a system perceives physical state.
- **Orchestration** — The coordination of multiple actors, systems, or workcells through planning and scheduling logic.
- **System-of-Systems** — A composite system composed of heterogeneous subsystems not originally designed for unified operation.
- **Heterogeneous Integration** — The assembly of components, vendors, or systems with differing internal models.
- **Deployment Target** — The physical, virtual, or institutional environment in which UCPIS-aligned systems are executed.
- **Execution Mode** — A discrete operational state conditioning allowed actions and safety assumptions.
- **Failure Mode** — A defined pathway through which a system may fail, degrade, or enter non-nominal operation.
- **Reversibility** — Whether an action can be undone without irreversible physical or institutional consequence.

---

# A.2 Agent-Agnostic Interface Principle (Normative)

UCPIS defines interfaces in an agent-agnostic manner, meaning interface contracts do not assume the internal nature, cognition, or origin of interacting entities.

Authority, accountability, and governance are assigned explicitly through classification and policy, not inferred from interface access.

---

# A.3 Interoperability Constructs

- **Semantic Interoperability** — Alignment of meaning between systems.
- **Syntactic Interoperability** — Alignment of data representation or schema.
- **Control Interoperability** — Alignment of actions, commands, or authority.
- **Temporal Interoperability** — Alignment of timing, scheduling, and latency behavior.
- **Safety Interoperability** — Alignment of hazard boundaries and irreversible action rules.
- **Institutional Interoperability** — Alignment across organizations, standards bodies, or regulatory domains.

---

# A.4 Cyber-Physical System (CPS) Constructs

- **Cyber-Physical System (CPS)** — A system in which computation and physical processes interact through sensing and actuation.
- **Actuation** — The exertion of physical influence through mechanical, electrical, or chemical means.
- **Sensor Domain** — The set of signals used to infer system state.
- **Physical Load** — Mechanical, thermal, electrical, or chemical burden placed on infrastructure.
- **Timing Constraint** — A requirement that actions or sensing occur within bounded temporal tolerances.
- **Irreversible Action** — A state transition that cannot be undone without damage, loss, or institutional consequence.
- **Resource Budget** — Allocated compute, power, cooling, or material capacity.

---

# A.5 Safety and Envelope Constructs

- **Safety Envelope** — The bounded region within which system operation is acceptable.
- **Residual Risk** — Risk remaining after mitigation and procedural control.
- **Compliance Domain** — The standards, rules, and certifications applicable to system operation.
- **Certification Surface** — The interface or behavior subject to formal certification.
- **Audit Surface** — The interface through which system actions are inspected, logged, and verified.
- **Hazard Classification** — Taxonomic assignment of failure or adverse events.
- **Failure Recovery** — Actions available to restore nominal operation after non-catastrophic failure.
- **Escalation** — Handoff of authority, responsibility, or decision-making to a higher class or institution.
- **Duty of Care** — Normative requirement to avoid harm within system operation.

---

# A.6 MVUE and Executability Constructs

The **Minimum Viable UCPIS-Executable (MVUE)** is a minimal demonstration that exercises UCPIS-defined interfaces sufficiently to validate architecture, interoperability, and constrained participation.

Relevant terms:

- **MVUE** — Minimum Viable UCPIS-Executable.
- **UCPIS-Executable** — A system artifact exercising UCPIS interface contracts to demonstrate interoperability.
- **Execution Recipe** — A structured, bounded sequence of tasks executable by a Class-L or Class-M actor or system.
- **Audit Trace** — A machine-readable record of system actions for replay or verification.
- **Escalation Path** — A defined authority handoff mechanism for resolving non-nominal or irreversible states.

---

# A.7 Human Participation Constructs

UCPIS models human actors as system participants with bounded autonomy and authority.

Relevant constructs:

- **Human Autonomy Class**
- **Authority Boundary**
- **Class-Scoped Permission**
- **Institutional Responsibility**
- **Accountability Chain**

---

# A.8 Human Autonomy Classes

*(full definitions retained from original v1.4 and included here unabridged in final build)*

---

# A.9 Constrained Human–Machine Interfaces (HMIs)

*(full HMI definition retained from previous revision — normative section unchanged)*

---

# A.10 Governance and Institutional Constructs

- **Governance Layer**
- **Institutional Actor**
- **Delegated Authority**
- **Stewardship**
- **Adoption Pressure**
- **Release Authority**
- **Normative Content**
- **Informative Content**

---

# A.11 Non-Human Biological Actors *(Informational)*

*(retained exactly as in previous revision)*

---

### End of Annex A
