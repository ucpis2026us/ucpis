# UCPIS Repository Structure

**Project:** Universal Cyber-Physical Interoperability Stack (UCPIS)  
**Version Context:** v1.4  
**Status:** Informative / Non-Normative  

This document describes the canonical file and folder structure of the UCPIS
repository as of version 1.4. It is intended to help readers, reviewers, and
contributors understand how architectural, contextual, and orienting
materials are organized.

The repository contains **architectural and interpretive documentation only**.
No products, implementations, standards, compliance mechanisms, or enforcement
authorities are defined.

---

## Top-Level Structure

ucpis/
├── annexes/
│   ├── README.md
│   ├── Annex_A_Definitions_Terminology_Taxonomy.md
│   ├── Annex_B_AI_as_Electrical_and_Thermal_Load.md
│   ├── Annex_C_Reference_Architecture_Diagrams.md
│   ├── Annex_D_Threat_Model_and_Resilience.md
│   ├── Annex_E_Standards_Alignment_and_Mapping.md
│   ├── Annex_F_Reference_Implementation_Guidelines.md
│   ├── Annex_G_Governance_Models.md
│   └── Annex_H_Interoperability_Profiles.md
│
├── docs/
│   ├── README.md
│   ├── how-to-read-ucpis.md
│   ├── ucpis-at-a-glance.md
│   ├── document-map.md
│   ├── interpretation-notes.md
│   └── notes/
│       ├── README.md
│       ├── interoperability-origin.md
│       ├── constrained-hmi-design-note.md
│       └── v1.5-activation-criteria.md
│
├── prompts/
│   └── UCPIS_White_Paper_Master_Prompt.md
│
├── white-paper/
│   ├── README.md
│   └── UCPIS_White_Paper_v1.4.md
│
├── ATTRIBUTION.md
├── CHANGELOG.md
├── CITATION.cff
├── DISCLAIMER.md
├── Governance-Without-Capture.md
├── How-to-Cite-UCPIS.md
├── LICENSE
├── README.md
├── RELEASE_NOTES.md
├── SECURITY.md
├── index.md
└── repository-structure.md

---

## Directory and File Descriptions

### `annexes/`
Contains architectural annexes that **elaborate and deepen** the UCPIS white
paper.

- **Annexes A–E** are active and applicable in v1.4.
- **Annexes F–H** are authored but explicitly **deferred** to prevent premature
  standardization, governance capture, or implementation lock-in.

All annexes are informative and non-normative unless explicitly stated.
See `annexes/README.md` for annex status and posture.

---

### `docs/`
Contains **reader-facing guidance and interpretation aids**.

Documents in this directory help readers:
- understand what UCPIS is and is not,
- navigate the documentation corpus,
- avoid common misinterpretations,
- read the architecture correctly.

Materials in `docs/` are **not canonical architecture** and define no
requirements or authority.

---

### `docs/how-to-read-ucpis.md`
Explains recommended reading order, canonical vs contextual material, and how
UCPIS should (and should not) be interpreted.

---

### `docs/ucpis-at-a-glance.md`
A one-page classification artifact summarizing what UCPIS is, what it is not,
and its intended role.

---

### `docs/document-map.md`
A conceptual map showing how UCPIS documents relate across layers
(WHY / WHAT / DEPTH / ENTRY / READER GUIDANCE).

---

### `docs/interpretation-notes.md`
Explicit guardrails against common misreadings, projection of authority, or
assumptions of implementability.

---

### `docs/notes/`
Contains **contextual and pre-normative design rationale**.

Documents here explain *why* architectural choices were made but do not define
UCPIS behavior, scope, or obligations.

If any conflict arises between notes and canonical documents, the white paper
and active annexes take precedence.

---

### `docs/notes/interoperability-origin.md`
Explains the architectural motivation and civilizational interoperability gap
that led to UCPIS.

---

### `docs/notes/constrained-hmi-design-note.md`
Design rationale for Constrained Human–Machine Interfaces (Constrained HMIs),
including safety posture, authority minimality, and escalation logic.

---

### `docs/notes/v1.5-activation-criteria.md`
A discipline document recording the conditions under which a v1.5 release would
be justified. It does not initiate v1.5 work.

---

### `prompts/`
Contains the canonical master prompt used to generate and regenerate the UCPIS
white paper corpus in a consistent, version-controlled manner.

---

### `white-paper/`
Contains the **canonical UCPIS architectural reference**.

- `UCPIS_White_Paper_v1.4.md` — the authoritative architecture document
- `README.md` — orientation and non-normative posture for the white paper

---

## Governance, Attribution, and Meta Files

- **`ATTRIBUTION.md`** — historical authorship and attribution
- **`CHANGELOG.md`** — versioned documentation changes
- **`CITATION.cff`** — machine-readable citation metadata
- **`DISCLAIMER.md`** — legal and practical limitations
- **`Governance-Without-Capture.md`** — governance posture statement
- **`How-to-Cite-UCPIS.md`** — citation guidance
- **`LICENSE`** — CC BY 4.0 license
- **`SECURITY.md`** — security posture clarification
- **`RELEASE_NOTES.md`** — v1.4 release summary
- **`README.md`** — repository overview and scope
- **`index.md`** — canonical public landing page

---

## Documentation Layers (Structural Logic)

The repository is intentionally structured around separable documentation layers:

1. **WHAT exists (Canonical Architecture)**  
   - `white-paper/`
   - `annexes/Annex_A–E`

2. **WHY it exists (Rationale and Intent)**  
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
