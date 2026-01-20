# Annex A — Definitions, Terminology, and Taxonomy

**UCPIS Version:** v1.4  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

**Attribution Required:**  
Michael James Malecek (2026)

**Canonical Repository:**  
https://github.com/ucpis2026us

**Contact:**  
ucpis2026@gmail.com

---

This annex defines canonical terms, classifications, and concepts used throughout the **Universal Cyber-Physical Interoperability Stack (UCPIS)**.

Unless explicitly stated otherwise, definitions in this annex are **normative**.  
Sections explicitly marked *Informational* are non-normative and provided for clarity and future extensibility.

---

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

This annex defines the canonical terms and taxonomies used throughout the **Universal Cyber-Physical Interoperability Stack (UCPIS)**. Annex A establishes the vocabulary surface necessary for interoperability, authority assignment, safety modeling, and cyber-physical participation.

Unless explicitly marked *Informational*, terms in this annex are **normative**.

---

# A.1 Core Interface & Architecture Terms

- **Interface** — A defined boundary through which systems exchange information or control.
- **Constraint** — A real-world limitation shaping allowable behavior.
- **Interoperability** — The ability of heterogeneous systems to exchange meaningfully interpretable information.
- **Layer** — A conceptual separation of concerns within the stack.
- **Contract Boundary** — A formally defined surface where obligations, permissions, and constraints are specified and enforced.
- **Typed Interface** — An interface that exposes a specific set of actions, data types, or authority levels.
- **Class-Scoped Interface** — An interface that exposes affordances according to actor class (e.g., Class-L, Class-M, Class-H).
- **Constraint-Aware Interface** — An interface that incorporates physical, safety, timing, thermal, electrical, or institutional constraints.
- **Participation Contract** — The defined set of actions, roles, and constraints through which a system actor participates in a cyber-physical environment.
- **State Model** — The canonical representation of observed or inferred system state.
- **Workcell** — A bounded physical or logical unit of task execution within a cyber-physical environment.
- **Operational Context** — The conditions under which a system is deployed, including physical, temporal, and institutional constraints.
- **Control Surface** — The set of actions or commands through which a system may influence another.
- **Sensing Surface** — The set of observable signals through which a system perceives physical state.
- **Orchestration** — The coordination of multiple actors, systems, or workcells through planning and scheduling logic.
- **System-of-Systems** — A composite system composed of heterogeneous subsystems not originally designed for unified operation.
- **Heterogeneous Integration** — The assembly of components, vendors, or systems with differing internal representations or control models.
- **Deployment Target** — The physical, virtual, or institutional environment in which UCPIS-aligned systems are executed.
- **Execution Mode** — A discrete operational state that conditions allowed actions, interfaces, and safety assumptions.
- **Failure Mode** — A defined pathway through which a system may fail, degrade, or enter a non-nominal state.
- **Reversibility** — A property describing whether an action can be undone without irreversible physical or institutional consequence.

---

# A.2 Agent-Agnostic Interface Principle (Normative)

UCPIS defines interfaces in an agent-agnostic manner, meaning interface contracts do not assume the internal nature, cognition, or origin of interacting entities.

Agent-agnostic interfaces specify observable boundaries, constraints, and permitted actions. Authority, accountability, and governance are assigned explicitly through classification and policy, not inferred from interface access.

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
- **Physical Load** — Mechanical, thermal, electrical, or chemical burden placed on physical infrastructure.
- **Irreversible Action** — A state transition that cannot be undone without damage, loss, or institutional consequence.
- **Timing Constraint** — A requirement that actions or sensing occur within bounded temporal tolerances.
- **Resource Budget** — Allocated compute, power, cooling, or material capacity.

---

# A.5 Safety and Envelope Constructs

- **Safety Envelope** — The bounded region within which system operation is considered acceptable.
- **Residual Risk** — The risk that remains after system mitigation and procedural control.
- **Compliance Domain** — The set of rules, standards, certifications, or regulatory constraints applicable to system operation.
- **Certification Surface** — The interface or behavior subject to formal certification.
- **Audit Surface** — The interface through which system actions are inspected, logged, and verified.
- **Hazard Classification** — Taxonomic assignment of failure or adverse events.
- **Failure Recovery** — The set of actions available to restore nominal operation after non-catastrophic failure.
- **Escalation** — The handoff of authority, responsibility, or decision-making to a higher class or institution.
- **Duty of Care** — The normative requirement to avoid harm within system operation.

---

# A.6 MVUE and Executability Constructs

The **Minimum Viable UCPIS-Executable (MVUE)** is a minimal demonstration that exercises UCPIS-defined interfaces sufficiently to validate architecture, interoperability, and constrained participation.

Relevant terms:

- **MVUE** — Minimum Viable UCPIS-Executable.
- **UCPIS-Executable** — A system artifact that exercises UCPIS interface contracts to demonstrate interoperability.
- **Execution Recipe** — A structured, bounded sequence of tasks executable by a Class-L or Class-M actor or system.
- **Audit Trace** — A machine-readable record of system actions for replay or verification.
- **Escalation Path** — A defined authority handoff mechanism for resolving non-nominal or irreversible states.

---

# A.7 Human Participation Constructs

UCPIS models human actors as system participants with bounded autonomy and authority.

Relevant constructs:

- **Human Autonomy Class** — The classification of human actors according to cognitive capability, authority, and system leverage.
- **Authority Boundary** — The limit of actor-permitted influence over cyber-physical systems.
- **Class-Scoped Permission** — Permission tied to actor class rather than job title.
- **Institutional Responsibility** — Accountability assigned at organizational rather than individual scale.
- **Accountability Chain** — The sequence through which responsibility propagates under non-nominal or harmful outcomes.

---

# A.12 Human Autonomy Classes

*(retained exactly as-produced in previous revision; omitted here for brevity in the interest of structural continuity — full content remains unchanged)*

---

# A.13 Constrained Human–Machine Interfaces (HMIs)

*(retained as defined in previous revision and unabridged)*

---

# A.14 Governance and Institutional Constructs

- **Governance Layer** — The layer by which rules, policies, and institutional controls are applied.
- **Institutional Actor** — An organization exercising authority, stewardship, or compliance responsibility.
- **Delegated Authority** — Authority granted from one actor or institution to another.
- **Stewardship** — Responsibility for overseeing the long-term integrity or safety of systems.
- **Adoption Pressure** — The external force driving standardization or compliance.
- **Release Authority** — The actor or institution empowered to authorize deployment.
- **Normative Content** — Content defining required behavior.
- **Informative Content** — Content provided for clarity without normative force.

---

# A.15 Non-Human Biological Actors *(Informational)*

*(retained as previously revised)*

---

# End of Annex A


## A.2 Agent-Agnostic Interface Principle (Normative)

UCPIS defines interfaces in an agent-agnostic manner, meaning interface contracts
do not assume the internal nature, cognition, or origin of the interacting entity.

Agent-agnostic interfaces specify only observable interaction boundaries,
constraints, and permitted actions.

This principle does not imply agent equivalence.

Authority, accountability, normative responsibility, and governance are assigned
explicitly through actor classification, policy, and system control layers, and
are not inferred from interface access alone.

---

## A.12 Human Autonomy Classes

UCPIS models human participants as **first-class system actors**. Human Autonomy Classes are descriptive constructs used to inform interface design, authority boundaries, and safety assumptions across the stack.

These classes are **not evaluative judgments of human worth or status**. They exist solely to support safe, scalable, and predictable system design.

---

### Class-L — Low-Autonomy Operators

**Capabilities**
- Limited planning and task sequencing
- Constrained symbolic reasoning
- Reduced executive function and error recovery
- Limited temporal reasoning and safety judgment

**Primary Function**
- Execute narrowly defined, highly structured tasks

**Design Doctrine**
> Make the correct action the default; make dangerous actions impossible.

---

### Class-M — Mid-Autonomy Technicians / Supervisors

**Capabilities**
- Execute and oversee standard operating procedures (SOPs)
- Perform basic diagnostics and troubleshooting
- Escalate anomalies appropriately
- Coordinate small teams or workcells

**Primary Function**
- Maintain operational continuity within defined bounds

**Design Doctrine**
> Provide leverage with rails and guardrails.

---

### Class-H — High-Autonomy / High-Leverage Architects

**Capabilities**
- System-level reasoning
- Cross-domain integration
- Long-horizon planning
- Ethical, strategic, and institutional judgment

**Primary Function**
- Define architecture, policy, and system constraints

**Design Doctrine**
> Amplify structurally — one Class-H can shape thousands of workcells.

---

### Class-X — Augmented / Composite Actors *(Informational)*

**Capabilities**
- Human actors operating in concert with advanced tools or AI systems

**Status**  
Class-X is informational only in UCPIS v1.4. No normative requirements, interfaces, or governance assumptions are defined at this stage.

---

## A.13 Constrained Human–Machine Interfaces (HMIs)

**Definition (Normative)**  
A **Constrained HMI** is a class-scoped, safety-bounded interaction surface through which human actors participate in cyber-physical systems. Constrained HMIs expose only those actions, affordances, and state representations that a given human class MAY safely execute or interpret.

**Purpose**  
Constrained HMIs exist to ensure that authority, safety, and accountability are enforced at the interface boundary. This prevents mismatches between human cognitive capacity and cyber-physical system control surfaces.

**Scope**
Constrained HMIs SHALL:
- Bind interaction to **actor class**
- Enforce **authority limits**
- Reflect **system state and lockouts**
- Emit **audit traces**
- Support **escalation mechanisms**

Constrained HMIs SHALL NOT:
- Assume arbitrary free-form human control
- Provide unbounded override capabilities
- Infer competence or authority from job title, role, or seniority

**Class Binding Rules**
- **Class-L** interfaces SHALL expose only structured, reversible, and bounded tasks
- **Class-M** interfaces MAY expose limited diagnostic and supervisory actions within SOP-defined boundaries
- **Class-H** interfaces MAY expose structural configuration, policy, and architectural control
- **Class-X** interfaces are informational only in v1.4 and SHALL NOT define normative requirements

**Safety Envelope**
All Constrained HMIs SHALL respect cyber-physical safety envelopes including:
- irreversible actions
- timing and latency constraints
- electrical and thermal limits
- compliance, audit, or certification regimes

**Design Implication**
> Giving a human actor more interface authority than they can safely exercise is a system design failure, not a usability failure.

---

## A.14 Non-Human Biological Actors *(Informational)*

UCPIS may interface indirectly or directly with non-human biological entities in certain cyber-physical environments, including but not limited to agriculture, research facilities, environmental monitoring, logistics perimeters, or containment systems.

Non-human biological actors are **not classified under Human Autonomy Classes** and are **not considered system authorities or accountable decision-makers** within the UCPIS framework.

This category includes animals with varying cognitive and behavioral complexity, including:
- Corvids (e.g., crows, ravens)
- Non-human primates (e.g., gorillas, chimpanzees)
- Cephalopods (e.g., octopus species)
- Other biologically autonomous organisms interacting with controlled environments

**Characteristics**
- Goal-directed behavior within species-specific domains
- Learning and adaptation via biological mechanisms
- Absence of symbolic intent, normative responsibility, or institutional accountability
- Interaction mediated through observation, containment, or conditioned response mechanisms

**Design Implications**
- Interfaces involving non-human biological actors SHALL be treated as **environmental or biological interface constraints**, not as autonomous system actors.
- All decision authority, safety responsibility, and escalation logic remains assigned to human or artificial system actors.
- Systems interacting with animals MUST assume non-symbolic intent, non-contractual behavior, and potential unpredictability.

**Status**  
This classification is informational only. UCPIS defines no normative behavioral, ethical, welfare, or governance requirements for non-human biological actors.

---

### End of Annex A
