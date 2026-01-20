# Universal Cyber-Physical Interoperability Stack (UCPIS)

**Version:** v1.4  
**Status:** Public White Papers (Informative / Non-Normative)

The **Universal Cyber-Physical Interoperability Stack (UCPIS)** is an
informative interoperability framework describing how heterogeneous
cyber-physical systems—machines, software, humans, and real-world
constraints—may interoperate through a layered, interface-first
architecture.

UCPIS is **not** a product, platform, standard, or implementation.
It defines **no compliance requirements**, **no certifications**, and
**no enforcement mechanisms**.

---

## Purpose

UCPIS exists to:

- Reduce fragmentation across cyber-physical systems
- Enable interface-first reasoning across physical, human, and cyber domains
- Support safe, scalable interaction among humans, automation, and environment
- Treat real-world constraints (energy, labor, safety, governance, biology)
  as **first-class architectural inputs**
- Resist premature institutionalization or vendor capture

UCPIS is designed to be **compatible with open systems, public infrastructure,
and long-standing civic principles**, while remaining technically neutral.

---

## Architecture Summary

UCPIS describes a **three-layer conceptual architecture**, operating within a
broader environmental and socio-technical context.

### Layer 1 — Physical
- Machines, robots, sensors, actuators
- Energy, material handling, and logistics interfaces
- Physical state, actuation, and telemetry

### Layer 2 — Human Interface / Mediation
- Constrained human–machine interfaces (HMIs)
- Guided workflows and task mediation
- Confirmation, escalation, and exception handling

### Layer 3 — Cyber / Control / Governance
- Orchestration, scheduling, coordination
- Policy definition and constraint modeling
- Audit, oversight, and system-level reasoning

The architecture is **interface-first**, **vendor-neutral**, and designed to
operate safely in environments that may include non-human biological entities.

---

## Human Participation Model (Informational)

UCPIS models human participation using **Human Autonomy Classes**, defined in
Annex A.

- **Class-L — Low-Autonomy Operators**  
  Execute narrowly defined, guided tasks through constrained interfaces

- **Class-M — Mid-Autonomy Technicians / Supervisors**  
  Maintain operational continuity with bounded authority and escalation duties

- **Class-H — High-Autonomy Architects / Leaders**  
  Define policy, architecture, and system-level constraints

- **Class-X — Augmented / Composite Actors** *(Informational)*  
  Documented for awareness only; no normative requirements defined in v1.4

These classes impose **interface and authority constraints**, not value judgments
about human worth or status.

---

## Environmental and Biological Context

UCPIS explicitly acknowledges that cyber-physical systems operate within real
environments that may include **non-human biological entities** (e.g., wildlife).

Such entities:
- Are not system agents or authorities
- Are not governance participants
- Are treated as environmental and biological context

Their presence informs **design constraints, safety behavior, and resilience**
without assigning agency or responsibility.

---

## Governance Position

UCPIS asserts **no governance authority**.

Governance is treated as a **downstream, conditional concern**, activated only
if and when multiple independent stakeholders adopt or steward the framework
in real-world contexts.

UCPIS is intentionally designed to resist premature or centralized capture.
See **Annex G — Governance Models** and `/governance/governance-without-capture.md`
for details.

---

## Annexes (v1.4)

- **Annex A:** Definitions, Terminology, and Taxonomy  
- **Annex B:** Interfaces & Data Model  
- **Annex C:** Reference Architecture  
- **Annex D:** Threat Model & Resilience *(Informative)*  
- **Annex E:** Standards Alignment & Mapping *(Informative)*  

- **Annex F:** Reference Implementation Guidelines  
  *(Authored; deferred until executable “UCPIS-Executable” artifacts exist)*

- **Annex G:** Governance Models  
  *(Authored deferral; no governance authority defined)*

- **Annex H:** Interoperability Profiles  
  *(Authored deferral; pending empirical evidence from pilots)*

---

## License & Attribution

- **License:** Creative Commons Attribution 4.0 International (CC BY 4.0)  
- **Inventor:** Michael James Malecek  
- **Year:** 2026  
- **Location:** Delano, Minnesota, United States  

---

## Canonical Repository

https://github.com/ucpis2026us/ucpis

**Contact:** ucpis2026@gmail.com
