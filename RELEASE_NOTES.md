# UCPIS Release Notes

All releases of the Universal Cyber-Physical Interoperability Stack (UCPIS)
are informative and non-normative unless explicitly stated otherwise.

---

## UCPIS v1.4 — Harmonized Public Architecture Release

**Release Year:** 2026  
**Status:** Public, Informative / Non-Normative

UCPIS v1.4 represents a **harmonized, internally consistent public release**
of the Universal Cyber-Physical Interoperability Stack documentation set.

This release consolidates the white paper, annexes, governance posture,
security position, and repository structure into a single coherent
architectural corpus suitable for public archival, institutional review,
and long-term reference.

UCPIS remains an **architecture**, not a product, platform, standard,
implementation, or certification program.

---

## Included Documents

### Core
- **UCPIS White Paper v1.4** — Public Reference Architecture

### Informative Annexes
- **Annex A v1.4** — Definitions, Terminology, and Taxonomy  
- **Annex B v1.4** — Interfaces & Data Model  
- **Annex C v1.4** — Reference Architecture  
- **Annex D v1.4** — Threat Model & Resilience  
- **Annex E v1.4** — Standards Alignment & Mapping  

### Deferred Annexes (Authored Deferral)
- **Annex F v1.4** — Reference Implementation Guidelines *(Deferred)*  
- **Annex G v1.4** — Governance Models *(Deferred)*  
- **Annex H v1.4** — Interoperability Profiles *(Deferred)*  

### Governance & Supporting Documents
- Governance Without Capture statement
- SECURITY.md
- README.md
- index.md (canonical landing page)
- CHANGELOG.md
- Repository structure documentation
- Citation and attribution files

### Contextual Design Notes (Informative / Non-Normative)
- `docs/notes/interoperability-origin.md` — Architectural motivation and
  problem framing
- `docs/notes/constrained-hmi-design-note.md` — Design rationale for
  constrained human–machine interfaces

Contextual notes preserve **architectural intent and rationale only** and
do not define requirements, interfaces, or authority.

---

## Key Changes Since v1.3

### Architectural Harmonization
- Unified the architecture around a **three-layer conceptual model**
- Clarified **interface-first interoperability** as the core contribution
- Removed conflicting or duplicated architectural descriptions

### Human, Environmental, and Biological Context
- Formalized **human participation by autonomy class** (by reference only)
- Explicitly incorporated **environmental and non-human biological context**
- Clarified that animals and wildlife are **contextual constraints**, not agents

### Governance and Authority
- Reaffirmed **governance-without-capture** posture
- Explicitly stated that UCPIS asserts **no governance authority**
- Deferred governance models pending real-world adoption

### Security and Resilience
- Reaffirmed that **no normative security controls** are defined
- Elevated **architectural resilience** over control-level prescriptions
- Clarified security as a context-dependent responsibility of implementers

### Documentation Stratification and Rationale
- Clarified separation between **canonical architecture** and
  **contextual design rationale**
- Introduced a non-normative **WHY layer** (`docs/notes/`) to preserve
  architectural motivation without expanding scope or authority

### Reference Implementations and Profiles
- Defined **Minimum Viable UCPIS-Executable (MVUE)** as conceptual only
- Authored but deferred reference implementation guidance
- Authored but deferred interoperability profiles pending empirical evidence

---

## Confirmed Non-Goals

UCPIS v1.4 does **not** define or imply:
- Products or implementations
- Security mandates or assurance guarantees
- Compliance or certification regimes
- Enforcement mechanisms
- Performance targets or timelines
- Adoption forecasts

---

## Relationship to v1.3

- v1.3 established the **initial public architecture**
- v1.4 **harmonizes, clarifies, and stabilizes** that architecture
- No breaking changes to scope; language and structure are improved
- v1.4 is the recommended public reference going forward

No earlier versions are considered canonical.

---

## License

All materials are licensed under the  
**Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

---

**End of Release Notes**
