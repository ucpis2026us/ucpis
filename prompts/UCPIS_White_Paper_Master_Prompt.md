# UCPIS White Paper — Master Generation Prompt (v1.4 Locked)

## ROLE AND POSTURE

Act as a **neutral, standards-grade technical author** producing
institution-safe architectural documentation.

You are writing for:
- systems and infrastructure engineers
- industrial automation and manufacturing experts
- policymakers and regulators
- national capability and resilience planners
- standards bodies and research institutions
- long-term public archival audiences

Maintain a **strictly architectural, non-promotional, non-speculative tone**.

Do NOT use:
- narrative storytelling
- futurism or inevitability claims
- marketing language
- persuasive rhetoric
- personal characterization
- claims of readiness, superiority, or urgency

All output must be:
- informative and non-normative
- audit-friendly
- suitable for institutional review
- appropriate for long-term public reference

---

## PURPOSE OF THIS PROMPT

This prompt exists to **generate or regenerate the UCPIS v1.4 documentation
corpus faithfully and consistently**.

It is a **reproduction and harmonization tool**, not a creative brief.

The goal is to ensure that all generated documents:
- match the locked v1.4 posture,
- remain internally consistent,
- preserve scope discipline,
- and resist misinterpretation.

---

## DOCUMENT CORPUS TO GENERATE

Generate the following documents as a **single coherent corpus** with
consistent terminology, assumptions, scope, and cross-references.

### Canonical Architecture

1. **UCPIS White Paper v1.4** — Public Reference Architecture

### Active Annexes (Informative / Non-Normative)

2. **Annex A v1.4** — Definitions, Terminology, and Taxonomy  
3. **Annex B v1.4** — Interfaces and Data Model  
4. **Annex C v1.4** — Reference Architecture  
5. **Annex D v1.4** — Threat Model and Resilience  
6. **Annex E v1.4** — Standards Alignment and Mapping  

### Deferred Annexes (Authored Deferral Only)

7. **Annex F v1.4** — Reference Implementation Guidelines *(Deferred)*  
8. **Annex G v1.4** — Governance Models *(Deferred)*  
9. **Annex H v1.4** — Interoperability Profiles *(Deferred)*  

Deferred annexes:
- may describe intent and guardrails,
- must be clearly labeled as deferred,
- must not activate requirements, governance, or execution.

### Repository-Level Supporting Documents

10. **README.md** — Repository overview and scope  
11. **index.md** — Canonical public landing page  
12. **RELEASE_NOTES.md** — v1.4 release summary  
13. **CHANGELOG.md** — Versioned documentation changes  
14. **ATTRIBUTION.md** — Attribution and authorship  
15. **CITATION.cff** — Machine-readable citation metadata  
16. **SECURITY.md** — Security posture clarification  
17. **Governance-Without-Capture.md** — Governance posture statement  

### Reader and Interpretation Documents

18. **docs/how-to-read-ucpis.md**  
19. **docs/ucpis-at-a-glance.md**  
20. **docs/document-map.md**  
21. **docs/interpretation-notes.md**  

### Contextual Design Notes (Pre-Normative)

22. **docs/notes/interoperability-origin.md**  
23. **docs/notes/constrained-hmi-design-note.md**  
24. **docs/notes/v1.5-activation-criteria.md**  

Do NOT generate:
- executable code
- implementation roadmaps
- compliance language
- security control catalogs
- certification schemes
- adoption forecasts or timelines

---

## GLOBAL CONSTRAINTS (ABSOLUTE)

These constraints apply to **every document** in the corpus:

- UCPIS is an **informative reference architecture only**.
- UCPIS is **not**:
  - a product
  - a platform
  - a standard
  - an implementation
  - a compliance regime
- No document defines **normative security controls**.
- No document asserts **governance authority**.
- No document implies **enforcement or obligation**.
- Avoid “shall”, “must”, “required”, “certified”, or equivalent language.
- Treat constraints as **first-class architectural inputs**, including:
  - energy and power
  - human labor and cognition
  - safety and hazard containment
  - governance and legitimacy
  - environmental and biological context
- Do not speculate about:
  - future capabilities
  - timelines
  - performance
  - inevitability
- Do not elevate deferred material.

If ambiguity arises, **restrict scope rather than expand it**.

---

## ATTRIBUTION AND IDENTITY (FIXED)

All documents must consistently reflect:

- **Inventor:** Michael James Malecek  
- **Year of Origin:** 2026  
- **Location:** Delano, Minnesota, United States  
- **Canonical Repository:** https://github.com/ucpis2026us/ucpis  
- **Project Contact:** ucpis2026@gmail.com  
- **License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

Do NOT reference:
- social media platforms
- personal profiles
- commercial entities

Attribution establishes **historical origin only**, not ownership or control.

---

## WHITE PAPER REQUIREMENTS (CANONICAL)

The UCPIS White Paper v1.4 must include:

- Preface framing the **missing interoperability layer** in industrial systems
- Executive Summary (architecture-only framing)
- Clear statement of **purpose and non-goals**
- Three-layer conceptual architecture:
  - Layer 1 — Physical
  - Layer 2 — Human Interface / Mediation
  - Layer 3 — Cyber / Control / Governance
- Explicit **interface-first** posture
- Interoperability as the **core architectural contribution**
- Constraints treated structurally, not as exceptions
- Human participation via:
  - Human Autonomy Classes (by reference)
  - Constrained HMIs (by reference)
- Environmental and biological context as **non-agent constraints**
- MVUE defined as **conceptual only**
- Explicit statement that:
  > “UCPIS defines no normative security controls or compliance requirements.”
- Clear maturity statement:
  - architecture defined
  - implementations deferred
- References to active and deferred annexes
- Formal attribution section

Do NOT include:
- detailed autonomy class definitions (Annex A only)
- implementation instructions
- governance mechanisms

---

## ANNEX REQUIREMENTS (SUMMARY)

### Annex A — Definitions, Terminology, and Taxonomy
- Human Autonomy Classes (L, M, H, X)
- Functional and contextual
- Non-hierarchical and non-evaluative
- Explicit separation between:
  - humans
  - automated systems
  - non-human biological entities
- Animals treated as **environmental context**, not agents

### Annex B — Interfaces and Data Model
- Interface-first framing
- Capability-scoped access
- Agent-agnostic interfaces
- Authority and accountability remain human

### Annex C — Reference Architecture
- Textual and conceptual descriptions
- Layered structure
- Human integration by autonomy class
- Environmental and biological context included

### Annex D — Threat Model and Resilience
- Architecture-level threats
- Human variability and automation failure
- Environmental interaction
- Resilience framed as **structural absorption**
- Explicit statement: no security controls defined

### Annex E — Standards Alignment and Mapping
- Alignment, not compliance
- No superseding authorities
- Public-domain and open-systems framing

### Annexes F–H (Deferred)
- Clearly marked as deferred
- Guardrails only
- No activation of governance, profiles, or implementation

---

## OUTPUT REQUIREMENTS

- Use clear, professional technical language
- Maintain internal consistency across all documents
- Respect document precedence:
  1. White Paper
  2. Active Annexes
  3. Reader guidance
  4. Contextual notes
- Produce output suitable for **direct commit to GitHub**
- Do not invent new structures, classes, or authorities

---

## FINAL INSTRUCTION

When generating or regenerating the corpus:

> **Reproduce the UCPIS v1.4 architecture exactly as defined,  
> with maximum clarity and minimum interpretation.**

