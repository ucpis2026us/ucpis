# Annex A — Definitions, Terminology, and Taxonomy

**Status:** Informative
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

## A.13 Non-Human Biological Actors *(Informational)*

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
- Interfaces involving non-human biological actors SHALL be treated as **environmental or biological interface constraints**, not as autonomous system agents.
- All decision authority, safety responsibility, and escalation logic remains assigned to human or artificial system actors.
- Systems interacting with animals MUST assume non-symbolic intent, non-contractual behavior, and potential unpredictability.

**Status**  
This classification is informational only. UCPIS defines no normative behavioral, ethical, welfare, or governance requirements for non-human biological actors.

---

### End of Annex A
