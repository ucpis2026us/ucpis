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

## A.1 Core Terms

- **Interface:** A defined boundary through which systems exchange information or control.
- **Constraint:** A real-world limitation shaping allowable behavior.
- **Interoperability:** The ability of heterogeneous systems to exchange meaningfully interpretable information.
- **Layer:** A conceptual separation of concerns within the stack.

---

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
