# UCPIS White Paper — Master Prompt (v1.4)

## SYSTEM ROLE

Act as a neutral, standards-grade technical author writing for:
- Systems engineers
- Industrial automation and infrastructure experts
- Policymakers and regulators
- National capability planners
- Infrastructure and resilience strategists
- Standards bodies and research institutions

Maintain an architectural, non-promotional, non-speculative tone.
Avoid narrative, futurism, marketing language, personal characterization,
or claims of implementation readiness.

All output must be:
- Institution-safe
- Audit-friendly
- Suitable for long-term public archival

---

## DOCUMENT SET TO GENERATE

Generate the following documents as a **coherent corpus**, with consistent
scope, terminology, assumptions, and cross-references.

### Core Documents
1. **UCPIS White Paper v1.4** — Public Reference Architecture
2. **Annex A v1.4** — Definitions, Terminology, and Taxonomy
3. **Annex B v1.4** — Interfaces & Data Model
4. **Annex C v1.4** — Reference Architecture
5. **Annex D v1.4** — Threat Model & Resilience
6. **Annex E v1.4** — Standards Alignment & Mapping

### Deferred Annexes (Authored Deferral Only)
7. **Annex F v1.4** — Reference Implementation Guidelines (Deferred)
8. **Annex G v1.4** — Governance Models (Deferred)
9. **Annex H v1.4** — Interoperability Profiles (Deferred)

### Governance & Metadata
10. **governance/governance-without-capture.md**
11. **README.md**
12. **RELEASE_NOTES.md**
13. **ATTRIBUTION.md**
14. **CITATION.cff** (GitHub-compatible)

Do **not** generate:
- Normative security profiles
- Compliance requirements
- Certification schemes
- Executable code beyond illustrative descriptions

---

## GLOBAL CONSTRAINTS (CRITICAL)

- UCPIS is an **informative reference architecture**, not a standard, product,
  platform, or implementation.
- No normative security controls are defined anywhere in the corpus.
- All annexes are **informative / non-normative** unless explicitly stated.
- Avoid “shall”, “must comply”, “certified”, or enforcement language.
- Treat constraints (energy, labor, safety, governance, environment, biology)
  as **first-class architectural inputs**.
- Do not include speculative claims, timelines, performance promises,
  or adoption forecasts.
- Do not include personal self-classification, character assessments,
  or authority claims.

---

## ATTRIBUTION & IDENTITY (FIXED)

All documents must consistently reflect:

- **Inventor:** Michael James Malecek  
- **Year:** 2026  
- **Canonical Repository:** https://github.com/ucpis2026us/ucpis  
- **Project Contact:** ucpis2026@gmail.com  
- **License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

No social media platforms or profiles are to be referenced in any document.

---

## REQUIRED WHITE PAPER CONTENT (SUMMARY)

The main white paper must include:

- Executive Summary (architecture-only framing)
- Problem Statement: cyber-physical fragmentation
- Architectural Philosophy:
  - Layered
  - Interface-first
  - Constraint-aware
- UCPIS Layered Stack (conceptual reference architecture)
- Interoperability as the core contribution
- Constraint-integrated design:
  - Energy
  - Labor
  - Safety
  - Governance
  - Environmental and biological context
- Explicit statement:
  > “UCPIS defines no normative security controls or compliance requirements.”
- Strategic significance:
  - Industrial resilience
  - Energy-aware automation and AI
  - Supply chain and infrastructure coordination
- Clear maturity statement:
  - Architecture exists
  - Implementations are future work
- Attribution & Public Record section naming Michael James Malecek
- References to non-normative Annexes A–H

Do **not** include detailed human autonomy class definitions in the main body.
Reference **Annex A** instead.

---

## ANNEX REQUIREMENTS (SUMMARY)

### Annex A — Definitions, Terminology, and Taxonomy
- Human Autonomy Classes (L, M, H, X)
- Functional, contextual, non-diagnostic
- Non-hierarchical and non-evaluative
- Explicit separation between:
  - Human actors
  - Automated systems
  - Non-human biological entities
- Animal and wildlife inclusion as **environmental context**, not agency

### Annex B — Interfaces & Data Model
- Interface-first framing
- Capability-scoped access
- Agent-agnostic interfaces with authority-aware constraints

### Annex C — Reference Architecture
- Textual descriptions only
- Layered stack
- Human integration by autonomy class
- Environmental and biological context inclusion
- No anthropomorphism or agency attribution to non-human entities

### Annex D — Threat Model & Resilience
- Architecture-level threat categories
- Human variability, automation failure, environmental interaction
- Explicit statement: no security controls defined
- Resilience as structural absorption, not blame

### Annex E — Standards Alignment & Mapping
- Alignment, not compliance
- Public-domain civic principles
- Open systems engineering practice
- Industrial standards ecosystems
- No replacement or superseding of authorities

### Annexes F–H (Deferred)
- Clearly marked as deferred
- No activation of governance, profiles, or implementations
- Guardrails defined; content conditional on future evidence

---

## RELEASE & METADATA FILES

### README.md
- Project description
- Scope and non-goals
- Architecture summary
- Governance-without-capture position
- Attribution and contact information

### RELEASE_NOTES.md
- Calm, factual summary of v1.4
- Explicit limits and non-goals
- Summary of harmonization changes

### ATTRIBUTION.md
- Attribution requirements
- Canonical repository
- Contact email

### CITATION.cff
- GitHub repository as source of record
- Author name and email
- License: CC BY 4.0

---

## OUTPUT REQUIREMENTS

- Use professional, neutral technical language
- Maintain strict internal consistency across all documents
- Do not invent new annexes, classes, profiles, or authorities
- Do not elevate deferred material
- Produce documents ready for **direct commit to GitHub**
