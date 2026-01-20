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
│   ├── Annex_A_Definitions_Terminology_Taxonomy.md  
│   ├── Annex_B_Interfaces_and_Data_Model.md  
│   ├── Annex_C_Reference_Architecture.md  
│   ├── Annex_D_Threat_Model_and_Resilience.md  
│   ├── Annex_E_Standards_Alignment_and_Mapping.md  
│   ├── Annex_F_Reference_Implementation_Guidelines.md  
│   ├── Annex_G_Governance_Models.md  
│   └── Annex_H_Interoperability_Profiles.md  
├── docs/  
│   └── notes/  
│       └── constrained-hmi-design-note.md  
├── prompts/  
│   └── UCPIS_White_Paper_Master_Prompt.md  
├── white-paper/  
│   └── UCPIS_White_Paper_v1.4.md  
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

### `docs/`
Contains supporting documentation that explains the **design rationale**,
conceptual intent, and pre-normative thinking behind UCPIS.  

The `docs/` directory is used for:

- design notes  
- MVUE and harness notes  
- implementation-facing guidance that is **not part of the core white paper
  or annex corpus**

These materials are informative and may evolve as experience accumulates.

---

### `docs/notes/`
Contains **design notes** and other pre-normative explanatory artifacts
intended for contributors and implementers.

Design notes clarify the *why* behind architectural choices without
changing the core white paper or annex definitions.

---

### `docs/notes/constrained-hmi-design-note.md`
Design note describing the motivation, principles, and implementation
considerations for **Constrained Human–Machine Interfaces (Constrained HMIs)**.

This file:

- explains why Constrained HMIs exist in UCPIS  
- connects HMIs to Human Autonomy Classes  
- outlines safety posture, authority minimality, and escalation patterns  
- provides guidance for MVUE and reference implementation authors  

It is **informative / pre-normative** and may evolve independently of the
white paper and annexes.

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

## Documentation Layers (Repository Structure Logic)

In open technical projects, documentation naturally separates into four
conceptual layers:

1. **WHAT exists**  
   - Architecture, vocabulary, and conceptual model.  
   - For UCPIS, this is primarily:  
     - `white-paper/UCPIS_White_Paper_v1.4.md`  
     - `annexes/Annex_*.md`  

2. **WHY it exists**  
   - Design rationale, tradeoffs, and intent behind architectural choices.  
   - For UCPIS, this includes:  
     - `docs/notes/constrained-hmi-design-note.md`  
     - future design notes documenting major concepts and decisions.  

3. **HOW to use or implement it**  
   - Implementation guidance, MVUE examples, harness descriptions, and
     reference patterns (informative only).  
   - For UCPIS v1.4, this is mostly scoped to:  
     - `annexes/Annex_F_Reference_Implementation_Guidelines.md`  
     - future materials under `docs/` related to MVUEs and harnesses.  

4. **WHERE it applies**  
   - Domain-specific profiles, standards mappings, and sector-oriented
     interpretations.  
   - For UCPIS, this is expected to live in:  
     - `annexes/Annex_E_Standards_Alignment_and_Mapping.md`  
     - `annexes/Annex_H_Interoperability_Profiles.md` (deferred).  

The repository structure is designed so that these layers are **visible and
separable**, allowing future contributors and institutions to understand:

- which documents describe the architecture,
- which document explain design intent,
- which documents explore implementation patterns, and
- which documents apply UCPIS to specific domains.

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
