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

## Preface — The Missing Interoperability Layer in Industrial Civilization

Modern civilization depends on complex industrial systems: factories, logistics
networks, energy infrastructure, transportation systems, and large-scale
automation. These systems underpin economic activity, public infrastructure,
and national capability. Yet despite their centrality, they lack a shared
interoperability foundation comparable to what exists in the digital world.

Computing systems interoperate across vendors, environments, and use cases
because they are built atop open, layered protocols. A computer can connect to
any compliant network, exchange information with unknown systems, and evolve
independently of the applications it runs. This interoperability is not
accidental; it is the result of decades of interface-first architectural
thinking that treats protocols and contracts as more durable than individual
implementations.

Industrial systems never received an equivalent foundation.

Robotic arms do not “plug in” to factories the way computers plug into networks.
Manufacturing equipment, control systems, safety mechanisms, and logistics
infrastructure are typically integrated through bespoke, proprietary
interfaces. Interoperability, when it exists, is achieved through custom
engineering rather than shared architectural assumptions. As a result,
industrial systems are brittle, difficult to adapt, and slow to evolve.

This absence is not primarily a hardware limitation. It is an architectural one.

What is missing is a common way to describe, connect, constrain, and govern
heterogeneous cyber-physical systems—systems that combine software, machines,
humans, energy flows, governance requirements, and environmental context.
Without such a layer, industrial progress accumulates complexity rather than
capability, and coordination costs grow faster than system value.

As cyber-physical systems become more autonomous and more interconnected,
these limitations shift from being operational inconveniences to becoming
structural risks. Lock-in, fragility, safety hazards, and governance challenges
emerge not because individual components fail, but because the systems
themselves were never designed to interoperate coherently.

The Universal Cyber-Physical Interoperability Stack (UCPIS) exists to clarify
this architectural gap. It does not propose a single solution, product, or
standard. Instead, it provides a reference architecture for reasoning about how
diverse cyber-physical systems might interoperate safely, transparently, and
durably over long time horizons.

This preface provides context only. The sections that follow define UCPIS as an
informative, non-normative architectural reference.

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

1. **Human Autonomy Classes**
2. **Constrained Human–Machine Interfaces (Constrained HMIs)**

Both are defined in **Annex A — Definitions, Terminology, and Taxonomy**.

These constructs:

- Are functional and contextual
- Constrain interface exposure and authority
- Do not assign value, status, or worth to human beings
- Treat human error, confusion, and overload as **expected design inputs**

### 5.1 Human Autonomy Classes (Summary)

- **Class-L — Low-Autonomy Operators**
- **Class-M — Mid-Autonomy Technicians / Supervisors**
- **Class-H — High-Autonomy / High-Leverage Architects**
- **Class-X — Augmented / Composite Actors (Informational in v1.4)**

Formal definitions appear in **Annex A**.

### 5.2 Constrained HMIs (Summary)

Constrained HMIs are class-scoped, safety-bounded, audit-ready, and
escalation-enabled interaction surfaces. Definitions appear in **Annex A**
and examples in **Annex F (Deferred)**.

---

## 6. Environmental and Biological Context

UCPIS explicitly acknowledges real-world environmental and biological context,
including non-human biological entities.

Such entities are treated as **context, not agents**.

Further detail is provided in **Annex A**.

---

## 7. Minimum Viable UCPIS-Executable (MVUE)

The **Minimum Viable UCPIS-Executable (MVUE)** is a conceptual definition of
the smallest executable artifact capable of exercising UCPIS interfaces.

MVUEs are illustrative only and are not implementations or recommendations.

---

## 8. Interoperability as the Core Contribution

Interoperability in UCPIS is architectural, not contractual.

It includes interface-level substitution, event-based coordination,
cross-domain composability, and graceful degradation under constraint.

---

## 9. Threat Model and Resilience (By Reference)

Threat modeling and resilience principles are defined in **Annex D**.
No normative security controls are defined in v1.4.

---

## 10. Governance Position

UCPIS asserts **no governance authority**.

Governance considerations are deferred and non-binding.

---

## 11. Annex Structure

Annexes A–H are informative and versioned independently.

---

## 12. Status

UCPIS v1.4 represents a **stable, public, informational release**.

---

**End of White Paper v1.4**