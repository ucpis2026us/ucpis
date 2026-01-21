# UCPIS Repository Structure

**Project:** Universal Cyber-Physical Interoperability Stack (UCPIS)  
**Version Context:** v1.4  
**Status:** Informative / Non-Normative  

This document describes the canonical file and folder structure of the UCPIS
repository as of version 1.4. It is intended to help readers, reviewers, and
contributors understand how architectural, contextual, and orienting materials
are organized.

The repository contains **architectural and interpretive documentation only**.
No products, implementations, standards, compliance mechanisms, or enforcement
authorities are defined.

---

## Top-Level Structure

The repository is organized into clearly separated directories and files,
each serving a distinct interpretive role.

---

### `annexes/` — Architectural Elaboration

Architectural annexes that elaborate and deepen the UCPIS white paper.

- `README.md` — Annex scope, status, and non-normative posture
- `Annex_A_Definitions_Terminology_Taxonomy.md`
- `Annex_B_AI_as_Electrical_and_Thermal_Load.md`
- `Annex_C_Reference_Architecture_Diagrams.md`
- `Annex_D_Threat_Model_and_Resilience.md`
- `Annex_E_Standards_Alignment_and_Mapping.md`
- `Annex_F_Reference_Implementation_Guidelines.md` *(Deferred)*
- `Annex_G_Governance_Models.md` *(Deferred)*
- `Annex_H_Interoperability_Profiles.md` *(Deferred)*

Annexes A–E are active in v1.4. Annexes F–H are intentionally deferred to prevent
premature standardization, governance capture, or implementation lock-in.

---

### `docs/` — Reader Guidance and Interpretation

Reader-facing documentation that supports correct interpretation and navigation
of the UCPIS corpus.

- `README.md` — Scope and purpose of reader-guidance materials
- `how-to-read-ucpis.md` — Recommended reading order and interpretive guidance
- `ucpis-at-a-glance.md` — One-page classification of what UCPIS is and is not
- `document-map.md` — Conceptual map of document relationships
- `interpretation-notes.md` — Guardrails against common misinterpretations

#### `docs/notes/` — Contextual Rationale (WHY)

Contextual and pre-normative design rationale explaining *why* architectural
choices were made.

- `README.md` — Notes posture and non-authoritative status
- `interoperability-origin.md` — Civilizational interoperability motivation
- `constrained-hmi-design-note.md` — Rationale for Constrained HMIs
- `v1.5-activation-criteria.md` — Discipline document for future versioning

If conflicts arise, the white paper and active annexes take precedence.

---

### `white-paper/` — Canonical Architecture (WHAT)

The authoritative architectural definition of UCPIS.

- `README.md` — Orientation and non-normative posture
- `UCPIS_White_Paper_v1.4.md` — Canonical reference architecture

---

### `prompts/` — Generation Artifacts

Artifacts used to generate and regenerate the UCPIS documentation corpus.

- `UCPIS_White_Paper_Master_Prompt.md`

These files support reproducibility but are not part of the architecture itself.

---

### Repository Root Files — Governance, Attribution, and Metadata

- `ATTRIBUTION.md` — Historical authorship and attribution
- `CHANGELOG.md` — Versioned documentation changes
- `CITATION.cff` — Machine-readable citation metadata
- `DISCLAIMER.md` — Legal and practical limitations
- `Governance-Without-Capture.md` — Governance posture statement
- `How-to-Cite-UCPIS.md` — Human-readable citation guidance
- `LICENSE` — CC BY 4.0 license
- `README.md` — Repository overview and scope
- `RELEASE_NOTES.md` — v1.4 release summary
- `SECURITY.md` — Security posture clarification
- `index.md` — Canonical public landing page
- `repository-structure.md` — This document

---

## Documentation Layers (Structural Logic)

The repository is intentionally structured around separable documentation layers:

1. **WHAT exists — Canonical Architecture**  
   - `white-paper/`  
   - `annexes/Annex_A–E`

2. **WHY it exists — Rationale and Intent**  
   - `docs/notes/`

3. **DEPTH and ELABORATION**  
   - `annexes/` (including deferred annexes)

4. **READER ORIENTATION**  
   - `index.md`  
   - `docs/`  
   - `README.md` files at major boundaries

This separation prevents scope confusion, premature claims, and accidental
institutionalization.

---

## Summary

The UCPIS v1.4 repository structure is designed to:

- preserve architectural clarity,
- separate canon from context,
- resist premature standardization or governance,
- and support long-term public reference.

Each directory boundary is intentional. Each README establishes scope and
authority limits. Together, they form a durable, interpretable architectural
corpus.

---

**End of Repository Structure Document**
