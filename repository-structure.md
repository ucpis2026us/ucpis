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
├── annexes/
│ ├── Annex_A_Definitions_Terminology_Taxonomy.md
│ ├── Annex_B_Interfaces_and_Data_Model.md
│ ├── Annex_C_Reference_Architecture.md
│ ├── Annex_D_Threat_Model_and_Resilience.md
│ ├── Annex_E_Standards_Alignment_and_Mapping.md
│ ├── Annex_F_Reference_Implementation_Guidelines.md
│ ├── Annex_G_Governance_Models.md
│ └── Annex_H_Interoperability_Profiles.md
├── prompts/
│ └── UCPIS_White_Paper_Master_Prompt.md
├── white-paper/
│ └── UCPIS_White_Paper_v1.4.md
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
Contains all non-normative annex documents (Annexes A–H).  
Each annex elaborates on a specific aspect of the UCPIS architecture
without asserting compliance, authority, or implementation requirements.

Deferred annexes are clearly labeled and intentionally inactive.

---

### `prompts/`
Contains the canonical master prompt used to generate and regenerate the
UCPIS white paper corpus in a consistent, version-controlled manner.

---

### `white-paper/`
Contains the primary public white paper document for UCPIS v1.4.

---

### `ATTRIBUTION.md`
Defines attribution requirements and establishes historical authorship
without asserting ownership or control.

---

### `CHANGELOG.md`
Records versioned changes to the UCPIS documentation set, including
harmonization updates and clarified non-goals.

---

### `CITATION.cff`
Provides machine-readable citation metadata for GitHub, archival systems,
and academic reference tools.

---

### `DISCLAIMER.md`
Clarifies legal and practical limitations, including that UCPIS is not a
product, standard, certification, or legal instrument.

---

### `Governance-Without-Capture.md`
Standalone governance statement affirming that UCPIS asserts no governance
authority and is designed to resist premature or centralized capture.

---

### `How-to-Cite-UCPIS.md`
Human-readable guidance for citing the UCPIS white paper and annexes in
academic, policy, or technical contexts.

---

### `LICENSE`
Specifies the Creative Commons Attribution 4.0 International (CC BY 4.0)
license governing all UCPIS materials.

---

### `README.md`
Primary repository overview describing purpose, scope, architecture,
governance posture, and contact information.

---

### `RELEASE_NOTES.md`
Summarizes changes and clarifications introduced in UCPIS v1.4.

---

### `SECURITY.md`
States explicitly that UCPIS defines no normative security controls and
frames security as a context-dependent architectural concern.

---

### `index.md`
Canonical public landing page (GitHub Pages–compatible) for the UCPIS
documentation set.

---

### `repository-structure.md`
This document. Describes repository layout to support onboarding,
review, and long-term archival clarity.

---

## Summary

The UCPIS v1.4 repository structure is designed to:

- Separate **core architecture** from **supporting elaboration**
- Clearly distinguish **active content** from **deferred material**
- Prevent premature governance, security, or implementation claims
- Support institutional review and long-term public reference

All documents are authored to be readable independently while remaining
internally consistent as a single architectural corpus.

---

### End of Repository Structure Document
