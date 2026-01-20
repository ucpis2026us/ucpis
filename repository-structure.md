# UCPIS Repository Structure

**Project:** Universal Cyber-Physical Interoperability Stack (UCPIS)  
**Version:** v1.4  
**Status:** Informative / Non-Normative  

This document describes the canonical file and folder structure of the
UCPIS repository as of version 1.4. It is intended to help readers,
reviewers, and contributors understand how the white paper corpus,
annexes, and governance materials are organized.

The repository contains **informative architectural documentation only**.
No products, implementations, standards, or compliance mechanisms are
defined.

---

## Top-Level Structure

ucpis/
├── README.md
├── index.md
├── CHANGELOG.md
├── DISCLAIMER.md
├── SECURITY.md
├── GOVERNANCE.md
├── How-to-Cite-UCPIS.md
├── CITATION.cff
├── white-paper/
│ └── UCPIS_White_Paper_v1.4.md
├── annexes/
│ ├── Annex_A_Definitions_Terminology_Taxonomy.md
│ ├── Annex_B_Interfaces_and_Data_Model.md
│ ├── Annex_C_Reference_Architecture.md
│ ├── Annex_D_Threat_Model_and_Resilience.md
│ ├── Annex_E_Standards_Alignment_and_Mapping.md
│ ├── Annex_F_Reference_Implementation_Guidelines.md
│ ├── Annex_G_Governance_Models.md
│ └── Annex_H_Interoperability_Profiles.md
├── governance/
│ └── governance-without-capture.md
└── docs/
└── repository-structure.md


---

## Root-Level Files

### `README.md`
Primary project overview.  
Summarizes UCPIS purpose, scope, architecture, governance posture, and
links to the white paper and annexes.

---

### `index.md`
Canonical public landing page (GitHub Pages–compatible).  
Provides a concise, regulator-safe introduction to UCPIS v1.4 and links
to all authoritative documents.

---

### `CHANGELOG.md`
Versioned record of public releases and material changes.  
Includes v1.4 harmonization notes and explicit non-goals.

---

### `DISCLAIMER.md`
Clarifies that UCPIS is not a product, standard, certification, or legal
instrument, and provides standard liability disclaimers.

---

### `SECURITY.md`
States that UCPIS defines **no normative security controls**.  
Explains the architectural treatment of security as a context-dependent
constraint and refers readers to Annex D for threat and resilience
framing.

---

### `GOVERNANCE.md`
High-level governance statement.  
Explains that UCPIS asserts no governance authority and defers all
governance models pending real-world adoption.

---

### `How-to-Cite-UCPIS.md`
One-page citation guide for researchers, policymakers, and institutions.

---

### `CITATION.cff`
Machine-readable citation metadata for GitHub and archival systems.
Defines authorship, version, license, and canonical repository.

---

## White Paper

### `white-paper/UCPIS_White_Paper_v1.4.md`

The primary public white paper.

Defines:
- Purpose and scope
- Three-layer conceptual architecture
- Interface-first interoperability model
- Constraint-aware design philosophy
- Environmental and biological context
- Governance-without-capture posture
- Relationship to non-normative annexes

The white paper does **not** define implementations, security controls,
or compliance requirements.

---

## Annexes (`/annexes`)

All annexes are **informative / non-normative** unless explicitly stated.
They elaborate on specific aspects of the architecture without asserting
authority or requirements.

### `Annex_A_Definitions_Terminology_Taxonomy.md`
- Canonical terms and classifications
- Human Autonomy Classes (by reference)
- Explicit treatment of non-human biological entities as environmental context

---

### `Annex_B_Interfaces_and_Data_Model.md`
- Interface-first architectural principles
- Capability-scoped access
- Agent-agnostic interfaces with authority-aware constraints

---

### `Annex_C_Reference_Architecture.md`
- Textual reference architecture
- Human integration by autonomy class
- Environmental and biological interaction model

---

### `Annex_D_Threat_Model_and_Resilience.md`
- Architectural threat assumptions
- Human variability, automation failure, and environmental interaction
- Structural resilience principles
- Explicit statement: no normative security controls

---

### `Annex_E_Standards_Alignment_and_Mapping.md`
- Conceptual alignment with public-domain civic principles
- Open systems engineering practices
- Industrial and infrastructure standards ecosystems
- Alignment only; no compliance claims

---

### `Annex_F_Reference_Implementation_Guidelines.md` *(Deferred)*
- Non-normative guidance for future executable artifacts
- Definition of Minimum Viable UCPIS-Executable (MVUE)
- Explicitly deferred until code exists

---

### `Annex_G_Governance_Models.md` *(Deferred)*
- Conditions under which governance may be discussed
- Anti-capture principles
- Human-only accountability and authority
- No governance activated in v1.4

---

### `Annex_H_Interoperability_Profiles.md` *(Deferred)*
- Future, evidence-derived interoperability profiles
- Profiles constrain interfaces, not authority or actors
- Deferred pending pilots and empirical validation

---

## Governance Folder

### `governance/governance-without-capture.md`

Standalone governance statement reinforcing that:
- UCPIS asserts no governance authority
- Governance is downstream and conditional
- Power must be constrained, not centralized
- Non-human entities do not participate in governance

---

## Documentation Folder

### `docs/repository-structure.md`

Describes repository layout and document roles.
Intended to support onboarding, review, and archival clarity.

---

## Summary

The UCPIS v1.4 repository is organized to:

- Separate **core architecture** from **supporting detail**
- Clearly distinguish **active content** from **deferred material**
- Prevent premature governance, security, or implementation claims
- Support long-term public reference and institutional review

All documents are authored to be read independently while remaining
internally consistent as a single architectural corpus.

---

### End of Repository Structure Document
