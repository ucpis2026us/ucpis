# Universal Cyber-Physical Interoperability Stack (UCPIS)
## Public White Paper — Version 1.4

**Status:** Informative / Non-Normative  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Attribution

**Inventor:** Michael James Malecek  
**Year of Origin:** 2026  
**Location:** Delano, Minnesota, United States  
**Canonical Repository:** https://github.com/ucpis2026us/ucpis  
**Contact:** ucpis2026@gmail.com

---

## Executive Summary

The **Universal Cyber-Physical Interoperability Stack (UCPIS)** is an
informative reference architecture describing how heterogeneous
cyber-physical systems may interoperate through a **layered,
interface-first model**.

UCPIS is not a product, platform, standard, or implementation. It defines
**no compliance requirements**, **no certifications**, and **no normative
security controls**.

The architecture integrates **physical systems, human participation,
automation, governance constraints, and environmental context** into a
coherent interoperability framework suitable for public infrastructure,
industrial systems, and long-lived national capabilities.

A central feature of UCPIS is the explicit modeling of **Human Autonomy
Classes** and **Constrained Human–Machine Interfaces (Constrained HMIs)**.
Humans are treated as bounded system participants whose interfaces,
authority, and safety envelopes are intentionally constrained at the
architecture level, not left to ad hoc UI decisions.

---

## 1. Purpose

UCPIS exists to:

- Reduce fragmentation across cyber-physical systems
- Enable interface-first reasoning across physical, human, and cyber domains
- Treat real-world constraints (energy, labor, safety, governance, environment)
  as **first-class architectural inputs**
- Support resilience through structural design rather than ad hoc mitigation
- Make human participation **safe, scalable, and class-aware** through
  Constrained HMIs and explicit authority boundaries

---

## 2. Scope and Non-Goals

### In Scope
- Conceptual reference architecture
- Interface-first interoperability framing
- Human participation constraints (by reference)
- Constrained HMIs as class-scoped participation surfaces (by reference)
- Environmental and biological context
- Informative threat and resilience principles

### Out of Scope
- Product specifications or vendor guidance
- Implementation requirements or roadmaps
- Security controls, profiles, or mandates
- Compliance, certification, or enforcement
- Performance guarantees or timelines

---

## 3. Architectural Overview

UCPIS defines a **three-layer conceptual architecture**, operating within a
broader environmental and socio-technical context.

### Layer 1 — Physical

Machines, robots, sensors, actuators, energy systems, and logistics assets.

Layer 1 is where **physical state** resides and where **actuations** produce
irreversible or costly outcomes. UCPIS treats Layer 1 as **never directly
exposed to low-autonomy human control surfaces**.

### Layer 2 — Human Interface / Mediation

Constrained human–machine interfaces (**Constrained HMIs**), guided
workflows, confirmation, escalation, and exception handling.

Layer 2 is the **only layer** through which human operators and supervisors
interact with the stack in routine operation. Interfaces at this layer are
**class-aware** and **capability-scoped**:

- Class-L interfaces: tightly constrained rails (confirm/abort/escalate)
- Class-M interfaces: supervisory views with bounded diagnostic actions
- Class-H interfaces: structural and policy-level tools, often non-graphical

### Layer 3 — Cyber / Control / Governance

Orchestration, scheduling, policy definition, audit, coordination, and
system-level oversight.

Layer 3 is where **automation, planning, and governance logic** reside.
Layer 3 may interact with both Layer 1 and Layer 2, but **human action is
always mediated via Constrained HMIs** rather than arbitrary free-form access
to orchestration or actuation.

---

Interfaces — not implementations — are the primary unit of interoperability.
UCPIS is **interface-first** and **agent-agnostic**: the same interface
contract may be exercised by software agents, human actors, or hybrid systems,
subject to explicit constraints and authority assignments.

---

## 4. Constraints as First-Class Architectural Inputs

UCPIS treats constraints as shaping forces on interface design, including:

- Energy availability and electrical load
- Human labor capability and autonomy
- Safety boundaries and hazard containment
- Governance, legitimacy, and auditability
- Environmental and biological context

Constraints are integrated structurally rather than handled as exceptions.

In particular, **human limitations and safety responsibilities** are
translated into:

- **Human Autonomy Classes** (what a given class can be trusted to do)
- **Constrained HMIs** (what a given class is even allowed to see or invoke)

The combination of these two mechanisms ensures that “giving the wrong human
the wrong interface” is recognized as an **architectural error**, not merely
a UX or training problem.

---

## 5. Human Participation Model (By Reference)

UCPIS models human participation through:

1. **Human Autonomy Classes** — a descriptive taxonomy of human roles and
   capabilities.
2. **Constrained Human–Machine Interfaces (Constrained HMIs)** — the
   class-scoped interaction surfaces through which humans participate in
   the stack.

Both are defined in **Annex A — Definitions, Terminology, and Taxonomy**.

These constructs:

- Are functional and contextual
- Constrain interface exposure and authority
- Do not assign value, status, or worth to human beings
- Treat human error, confusion, and overload as **expected design inputs**,
  not exceptional conditions

### 5.1 Human Autonomy Classes (Summary)

Human Autonomy Classes provide a **capability- and authority-based**
classification of human roles, such as:

- **Class-L — Low-Autonomy Operators**  
  Narrowly scoped tasks, high structure, minimal degrees of freedom.

- **Class-M — Mid-Autonomy Technicians / Supervisors**  
  SOP execution, bounded troubleshooting, local coordination and escalation.

- **Class-H — High-Autonomy / High-Leverage Architects**  
  Structural decisions, cross-domain reasoning, policy and constraint design.

- **Class-X — Augmented / Composite Actors (Informational in v1.4)**  
  Humans operating in concert with advanced tools or AI systems.

Formal definitions and design doctrines for each class are specified in
**Annex A** and are not repeated here.

### 5.2 Constrained HMIs (Summary)

**Constrained HMIs** are the architectural mechanism by which human classes
are connected into the stack:

- **Class-scoped:** Interfaces are explicitly bound to a declared human class.
- **Safety-bounded:** Interfaces expose only those actions that can be safely
  exercised by that class.
- **Audit-ready:** All interactions are logged as part of the system’s audit
  surface.
- **Escalation-enabled:** When a situation exceeds the class’s authority or
  capability, the interface provides a structured path to escalate rather
  than improvise.

Constrained HMIs are **defined in Annex A** and **exercised in Annex F**
(via reference implementation guidelines). This white paper only introduces
the concept at an architectural level.

---

## 6. Environmental and Biological Context

UCPIS explicitly acknowledges that cyber-physical systems operate in
real-world environments that may include **non-human biological entities**
(e.g., wildlife).

Such entities:

- Are not system agents or authorities
- Are not governance participants
- Influence safety, resilience, and design constraints

Environmental and biological interaction is treated as **context**, not
agency. Where such interaction is modeled (for example in simulation or
reference harnesses), it is treated as **external, non-deterministic input**
rather than as an actor within the interface taxonomy.

Further description of non-human biological actors is provided in **Annex A**
(Informational).

---

## 7. Minimum Viable UCPIS-Executable (MVUE)

The **Minimum Viable UCPIS-Executable (MVUE)** is a conceptual definition
describing the smallest executable artifact capable of exercising UCPIS
interfaces across layers.

MVUEs:

- Demonstrate interface viability
- Enable testing, replay, and scenario-based reasoning
- Do not constitute implementations, products, or recommended stacks

In the context of human participation, an MVUE involving humans should
demonstrate at least one **Constrained HMI** interaction for a specific
human class (for example, a Class-L confirm/abort/escalate flow driven by
a task assignment message).

The detailed MVUE framing and reference implementation guidance are
described in **Annex F — Reference Implementation Guidelines (Deferred)**.

UCPIS v1.4 defines **no executable artifacts**, and no implementation is
required or endorsed.

---

## 8. Interoperability as the Core Contribution

Interoperability within UCPIS is defined by:

- **Interface-level substitution:** different components with compatible
  interfaces can be swapped or composed without redesigning the stack.
- **Event-based coordination:** systems coordinate through explicit event
  flows, not brittle hidden couplings.
- **Cross-domain composability:** physical, human, and cyber elements
  can participate via shared interface contracts.
- **Graceful degradation under constraint:** systems can continue operating
  in reduced mode when power, labor, or infrastructure are constrained.

Crucially, interoperability applies not only to machine and data interfaces,
but also to **human participation interfaces**:

- A Class-L operator can be added, removed, or relocated without rewriting
  orchestration logic, as long as the Constrained HMI contract is satisfied.
- A supervisory console can be changed or reimplemented as long as it
  exercises the same **Class-M** interface semantics.
- Higher-level orchestration can interface with real humans, simulated
  humans, or AI agents through the same contracts, subject to governance and
  safety policies.

Interoperability in UCPIS is architectural, not contractual: it aims to
describe how systems can fit together, not to mandate specific agreements
or enforcement regimes.

---

## 9. Threat Model and Resilience (By Reference)

UCPIS treats human variability, automation failure, and environmental
interaction as **expected operating conditions**, not exceptional faults.

Threat modeling and resilience principles are defined in **Annex D —
Threat Model & Resilience**, which is informative and non-normative.

No normative security controls are defined in v1.4. Any future security
profiles, if ever produced, must be explicitly versioned, scoped, and
published separately.

---

## 10. Governance Position

UCPIS asserts **no governance authority**.

Governance is treated as a downstream, conditional concern, activated only
if and when multiple independent stakeholders adopt or steward the
architecture.

The governance posture emphasizes:

- Avoiding “standard capture” by any single institution
- Enabling public, multi-stakeholder stewardship if and when adoption
  warrants it
- Keeping reference code and MVUE artifacts **non-normative** and
  vendor-neutral

This posture is expanded in **Annex G — Governance Models (Deferred)** and
the governance-without-capture statement.

---

## 11. Annex Structure

This white paper is complemented by the following non-normative annexes:

- **Annex A:** Definitions, Terminology, and Taxonomy  
  - Includes Human Autonomy Classes and Constrained HMI definitions.
- **Annex B:** AI as Electrical and Thermal Load  
  - Treats AI computation as a physical load on power and cooling.
- **Annex C:** Reference Architecture  
  - Illustrative diagrams and layer mappings.
- **Annex D:** Threat Model & Resilience  
  - Informative threat considerations and resilience framing.
- **Annex E:** Standards Alignment & Mapping  
  - Non-normative mappings to existing standards and frameworks.
- **Annex F:** Reference Implementation Guidelines *(Deferred)*  
  - MVUE framing and non-normative guidance for reference harnesses and
    Constrained HMI demonstrations.
- **Annex G:** Governance Models *(Deferred)*  
  - Possible governance structures and stewardship patterns.
- **Annex H:** Interoperability Profiles *(Deferred)*  
  - Potential profiles for specific domains or sectors.

Annexes are informative and may evolve or expand independently of the core
white paper, subject to explicit versioning and attribution.

---

## 12. Status

UCPIS v1.4 represents a **stable, public, informational release**.

Future revisions will occur only through explicit versioned updates, with
corresponding changes to annexes and reference materials. No implicit
governance or compliance authority is granted or implied by this document.

---

**End of White Paper v1.4**
