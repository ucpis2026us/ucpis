# Universal Cyber-Physical Interoperability Stack (UCPIS)

**Version:** v1.4  
**Status:** Public White Papers (Informative / Non-Normative)

---

The **Universal Cyber-Physical Interoperability Stack (UCPIS)** is an
informative reference architecture describing how heterogeneous
cyber-physical systems—machines, software, humans, and real-world
constraints—may interoperate through a **layered, interface-first
architecture**.

UCPIS is **not** a product, platform, standard, or implementation.
It defines **no compliance requirements**, **no certifications**, and
**no enforcement mechanisms**.

This document provides a **high-level architectural overview**.
The canonical definition of UCPIS resides in the public white paper and
associated annexes.

---

## Purpose

UCPIS exists to:

- Reduce fragmentation across cyber-physical systems
- Enable interface-first reasoning across physical, human, and cyber domains
- Support safe, scalable interaction among humans, automation, and environment
- Treat real-world constraints (energy, labor, safety, governance, biology)
  as **first-class architectural inputs**
- Resist premature institutionalization, standard capture, or vendor lock-in

UCPIS is designed to be compatible with **open systems, public infrastructure,
and long-standing civic principles**, while remaining technically neutral and
non-prescriptive.

---

## Architectural Context

Industrial civilization lacks a shared interoperability foundation comparable
to what open protocol stacks provide in the digital domain.

UCPIS addresses this gap by framing interoperability as an **architectural
problem**, not a contractual, organizational, or vendor-specific one.

This context is discussed informatively (and non-normatively) in:

- `docs/notes/interoperability-origin.md`

That document provides rationale only and does not define UCPIS behavior,
requirements, or authority.

---

## Architecture Summary

UCPIS describes a **three-layer conceptual architecture**, operating within a
broader environmental and socio-technical context.

### Layer 1 — Physical
- Machines, robots, sensors, actuators
- Energy, material handling, and logistics interfaces
- Physical state, actuation, and telemetry

### Layer 2 — Human Interface / Mediation
- Constrained human–machine interfaces (Constrained HMIs)
- Guided workflows and task mediation
- Confirmation, escalation, and exception handling

### Layer 3 — Cyber / Control / Governance
- Orchestration, scheduling, and coordination
- Policy definition and constraint modeling
- Audit, oversight, and system-level reasoning

Interfaces — not implementations — are the primary unit of interoperability.

The architecture is **interface-first**, **vendor-neutral**, and designed to
operate safely in environments that may include non-human biological entities.

---

## Human Participation Model (Informational)

UCPIS models human participation using **Human Autonomy Classes**, defined
informatively in **Annex A**.

- **Class-L — Low-Autonomy Operators**  
  Execute narrowly defined, guided tasks through constrained interfaces

- **Class-M — Mid-Autonomy Technicians / Supervisors**  
  Maintain operational continuity with bounded authority and escalation duties

- **Class-H — High-Autonomy Architects / Leaders**  
  Define policy, architecture, and system-level constraints

- **Class-X — Augmented / Composite Actors** *(Informational)*  
  Documented for awareness only; no normative requirements defined in v1.4

These classes impose **interface and authority constraints**, not value
judgments about human worth, role, or status.

Design rationale for constrained human participation is discussed
informatively in:

- `docs/notes/constrained-hmi-design-note.md`

---

## Environmental and Biological Context

UCPIS explicitly acknowledges that cyber-physical systems operate within real
environments that may include **non-human biological entities**
(e.g., wildlife, shared human–animal environments).

Such entities:
- Are not system agents or authorities
- Are not governance participants
- Are treated strictly as environmental and biological context

Their presence informs **design constraints, safety behavior, and resilience**
without assigning agency or responsibility.

---

## Governance Position

UCPIS asserts **no governance authority**.

Governance is treated as a **downstream, conditional concern**, activated only
if and when multiple independent stakeholders adopt or steward the architecture.

UCPIS is intentionally designed to resist premature or centralized capture.

See:
- **Annex G — Governance Models** *(Deferred)*  
- **Governance-Without-Capture.md**

---

## Canonical Documents (v1.4)

- **UCPIS Public White Paper v1.4**
- **Annex A:** Definitions, Terminology, and Taxonomy  
- **Annex B:** Interfaces & Data Model  
- **Annex C:** Reference Architecture  
- **Annex D:** Threat Model & Resilience *(Informative)*  
- **Annex E:** Standards Alignment & Mapping *(Informative)*  

Deferred annexes (F–H) are authored but intentionally inactive to prevent
premature standardization or implementation claims.

---

## License & Attribution

- **License:** Creative Commons Attribution 4.0 International (CC BY 4.0)  
- **Inventor:** Michael James Malecek  
- **Year:** 2026  
- **Location:** Delano, Minnesota, United States  

This attribution establishes historical origin only.
UCPIS is open, non-proprietary, and not owned or controlled by any individual
or organization.

---

## Canonical Repository

https://github.com/ucpis2026us/ucpis  

**Contact:** ucpis2026@gmail.com
