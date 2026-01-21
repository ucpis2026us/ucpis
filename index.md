# Universal Cyber-Physical Interoperability Stack (UCPIS)

**Version:** v1.4  
**Status:** Public, Informative / Non-Normative White Papers

---

The **Universal Cyber-Physical Interoperability Stack (UCPIS)** is an
informative reference architecture describing how heterogeneous
cyber-physical systems may interoperate through a **layered,
interface-first model**.

UCPIS is **not** a product, platform, standard, or implementation.
It defines **no compliance requirements**, **no certifications**, and
**no enforcement mechanisms**.

This page serves as the **canonical public landing page** for the UCPIS
white paper corpus and associated interpretive documentation.

---

## What UCPIS Provides

- A conceptual cyber-physical reference architecture
- Interface-first interoperability framing
- A structured human participation model (by reference only)
- Constraint-aware system reasoning
- Architectural treatment of energy, safety, governance, and environment
- Informative guidance suitable for public infrastructure and industry

Human autonomy classes are used **solely to scope interfaces and
safeguards** and are defined informatively in Annex A.
They are **not diagnostic, evaluative, hierarchical, or prescriptive**.

---

## What UCPIS Does Not Provide

- No implementations or products
- No security mandates or profiles
- No compliance or certification regimes
- No governance authority or enforcement
- No performance guarantees, roadmaps, or timelines

UCPIS describes **architecture only**.
If a statement appears to imply authority, enforcement, certification,
or implementation readiness, that interpretation is incorrect.

---

## Conceptual Architecture Summary

UCPIS defines a **three-layer conceptual architecture**, operating within
a broader socio-technical and environmental context:

1. **Layer 1 — Physical**  
   Machines, robots, sensors, actuators, energy systems, and logistics assets

2. **Layer 2 — Human Interface / Mediation**  
   Constrained HMIs, guided workflows, confirmation and escalation paths

3. **Layer 3 — Cyber / Control / Governance**  
   Orchestration, scheduling, policy definition, audit, and coordination logic

Interfaces — not implementations — are the primary unit of interoperability.

---

## Environmental and Biological Context

UCPIS explicitly acknowledges that cyber-physical systems operate in real
environments that may include **non-human biological entities**
(e.g., wildlife, livestock, shared human–animal environments).

Such entities:
- Are not system agents or authorities
- Are not governance participants
- Are not anthropomorphized
- Influence safety, resilience, and design constraints only

Environmental and biological interaction is treated as **context**, not agency.

---

## Minimum Viable UCPIS-Executable (MVUE)

UCPIS defines the concept of a **Minimum Viable UCPIS-Executable (MVUE)** as:

> *“Something executable that exercises UCPIS interfaces; not a full factory
> stack—just enough code to make the architecture testable.”*

In v1.4, MVUE is **conceptual only**.
No executable artifacts, reference implementations, demonstrations, or
conformance claims are published.

---

## Start Here — Reader Orientation

For readers new to UCPIS, the following documents provide orientation
*without introducing new architecture*:

- **Architecture Overview (Concise Summary)**  
  `docs/architecture-overview.md`  
  A short, explanatory summary of the UCPIS v1.4 architecture, derived
  entirely from the white paper.

- **How to Read UCPIS**  
  `docs/how-to-read-ucpis.md`  
  Recommended reading order and guidance on interpreting the corpus.

- **UCPIS at a Glance**  
  `docs/ucpis-at-a-glance.md`  
  One-page classification of what UCPIS is and is not.

- **Document Map**  
  `docs/document-map.md`  
  Explains how UCPIS documents relate across rationale, architecture,
  elaboration, and reader guidance.

- **Interpretation Notes**  
  `docs/interpretation-notes.md`  
  Guardrails against common misinterpretations or authority projection.

All reader-orientation documents are **informative only**.

---

## Canonical Documents

### UCPIS White Paper

- **Universal Cyber-Physical Interoperability Stack (UCPIS): Public White Paper v1.4**  
  https://github.com/ucpis2026us/ucpis/tree/main/white-paper/UCPIS_White_Paper_v1.4.md

### Supporting Annexes (Informative / Non-Normative)

- **Annex A** — Definitions, Terminology, and Taxonomy  
- **Annex B** — AI as Electrical and Thermal Load  
- **Annex C** — Reference Architecture Diagrams  
- **Annex D** — Threat Model & Resilience  
- **Annex E** — Standards Alignment & Mapping  
- **Annex F** — Reference Implementation Guidelines *(Deferred)*  
- **Annex G** — Governance Models *(Deferred)*  
- **Annex H** — Interoperability Profiles *(Deferred)*  

All annexes are available under:  
https://github.com/ucpis2026us/ucpis/tree/main/annexes

Deferred annexes are intentionally withheld to prevent premature
standardization, governance capture, or implementation lock-in.
They may be activated only if justified by external evidence.

---

## Contextual Design Notes (Non-Normative)

UCPIS includes **contextual design notes** that preserve architectural
motivation and design rationale without expanding scope or authority.

These documents are **informative only** and are not part of the
canonical architecture.

They are located under:  
https://github.com/ucpis2026us/ucpis/tree/main/docs/notes

Key documents include:

- **Interoperability Origin and Architectural Rationale**  
  (`docs/notes/interoperability-origin.md`)

- **Constrained Human–Machine Interfaces — Design Note**  
  (`docs/notes/constrained-hmi-design-note.md`)

- **v1.5 Activation Criteria**  
  (`docs/notes/v1.5-activation-criteria.md`)  
  Discipline document describing when a future version update would be
  justified. It does **not** initiate v1.5 work.

If any conflict arises between notes and canonical documents,
the **white paper and active annexes take precedence**.

---

## Governance Position

UCPIS asserts **no governance authority**.

Governance is treated as a downstream, conditional concern, activated
only if and when multiple independent stakeholders adopt or steward the
architecture.

See:
- **Governance Without Capture**  
https://github.com/ucpis2026us/ucpis/tree/main/Governance_Without_Capture.md
- **Annex G — Governance Models** *(Deferred)*

---

## Status, Maturity, and Forward Observation

- Stable public informational release (v1.4)
- Architecture defined; implementations are future work
- Informative and non-normative
- Designed for long-term public archival and institutional reference

Future updates, if any, will prioritize **clarity, interpretability,
and misuse resistance**, rather than expanded scope, authority,
or execution.

No subsequent version is active at this time.

---

## Attribution

**Inventor:** Michael James Malecek  
**Year:** 2026  
**Location:** Delano, Minnesota, United States  

This attribution establishes historical origin only.  
UCPIS is open, non-proprietary, and not owned or controlled by any
individual or organization.

---

## Citation

If you reference or reuse this work, please cite:

**Michael James Malecek (2026)**  
*Universal Cyber-Physical Interoperability Stack (UCPIS): Public White Paper v1.4*

Machine-readable citation metadata is provided via `CITATION.cff`.

---

## License

All materials are licensed under the  
**Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

---

## Repository and Contact

**Canonical Repository:**  
https://github.com/ucpis2026us/ucpis

**Contact:**  
ucpis2026@gmail.com
