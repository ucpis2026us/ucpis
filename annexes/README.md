# UCPIS Annexes

**Project:** Universal Cyber-Physical Interoperability Stack (UCPIS)  
**Version Context:** v1.4  
**Status:** Informative / Non-Normative (unless explicitly stated otherwise)  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Purpose of the Annexes

The annexes accompanying the Universal Cyber-Physical Interoperability Stack
(UCPIS) white paper provide **structured elaboration and depth** on specific
architectural topics.

They exist to:
- clarify terminology and architectural concepts,
- expand on particular dimensions of the reference architecture,
- document alignment, threat framing, and design considerations,
- and reserve space for future work that must be evidence-driven.

The annexes **do not redefine the core architecture** described in the UCPIS
white paper. If any conflict arises, the white paper takes precedence.

---

## Normative Status

Unless explicitly stated otherwise, annexes are **informative and
non-normative**.

- Annexes may introduce **definitions, taxonomies, or conceptual frameworks**
  for clarity.
- Annexes **do not** define compliance requirements, certifications,
  enforcement mechanisms, or product specifications.
- “Normative” within UCPIS means *architecturally definitive*, not legally or
  institutionally binding.

Only **Annex A** contains canonical definitions that other documents reference.
Even there, no compliance or enforcement authority is asserted.

---

## Active Annexes (v1.4)

The following annexes are **active, published, and applicable** to UCPIS v1.4.

### **Annex A — Definitions, Terminology, and Taxonomy**
Provides the canonical vocabulary for UCPIS, including:
- core architectural terms,
- Human Autonomy Classes,
- Constrained Human–Machine Interfaces (Constrained HMIs),
- treatment of environmental and non-human biological context.

Annex A establishes shared language but does **not** impose requirements or
value judgments.

---

### **Annex B — AI as Electrical and Thermal Load**
Treats AI computation as a **physical infrastructure load**, not an abstract
software concern.

This annex frames AI systems in terms of:
- energy consumption,
- heat dissipation,
- physical capacity constraints,
- and infrastructure planning implications.

It is informative and non-prescriptive.

---

### **Annex C — Reference Architecture**
Provides illustrative diagrams and mappings that visualize:
- the three-layer UCPIS architecture,
- interface boundaries,
- human participation by class,
- environmental and biological context.

Diagrams are explanatory only and do not constitute implementations.

---

### **Annex D — Threat Model & Resilience**
Frames threat modeling and resilience as **architectural properties** rather
than control checklists.

This annex:
- treats human error, automation failure, and environmental interaction as
  expected operating conditions,
- emphasizes structural resilience and graceful degradation,
- defines no normative security controls.

---

### **Annex E — Standards Alignment & Mapping**
Maps UCPIS concepts to existing standards and frameworks for **alignment and
interpretation only**.

This annex:
- makes no compliance claims,
- asserts no authority over standards bodies,
- exists to support cross-domain understanding and dialogue.

---

## Deferred Annexes (Authored, Intentionally Inactive)

The following annexes are **authored but explicitly deferred** in v1.4.

Deferral does **not** mean incomplete. It is a deliberate architectural choice
to prevent premature standardization, governance capture, or implementation
lock-in.

### **Annex F — Reference Implementation Guidelines** *(Deferred)*
Reserved for non-normative guidance on:
- Minimum Viable UCPIS-Executable (MVUE) artifacts,
- reference harnesses,
- interface exercise patterns.

This annex will be activated only when executable artifacts exist that warrant
documentation.

---

### **Annex G — Governance Models** *(Deferred)*
Explores possible governance and stewardship structures **if and only if**
multi-stakeholder adoption occurs.

UCPIS asserts no governance authority in v1.4. This annex remains inactive
until real-world conditions justify its use.

---

### **Annex H — Interoperability Profiles** *(Deferred)*
Reserved for future definition of **interoperability profiles** derived from
empirical evidence.

Profiles will be authored only after:
- pilot deployments or high-fidelity simulations exist,
- cross-system interoperability is demonstrated,
- limitations and failure modes are documented.

Profiles are descriptive artifacts, not standards.

---

## What Annexes Do Not Do

Across all annexes, UCPIS explicitly does **not**:

- define products, platforms, or implementations,
- mandate security controls or assurance regimes,
- establish compliance or certification programs,
- grant governance authority,
- assign agency to non-human biological entities,
- override or supersede the white paper.

Annexes deepen understanding; they do not expand scope.

---

## Relationship to Other Documentation

Within the UCPIS repository, documentation is intentionally layered:

- **White Paper** — Canonical reference architecture (WHAT)
- **Annexes** — Architectural elaboration and depth
- **`docs/notes/`** — Contextual rationale and design intent (WHY)
- **Deferred annexes** — Evidence-gated future material

This separation preserves clarity, interpretability, and long-term stability.

---

## Summary

The annexes are an integral part of the UCPIS architectural corpus, providing
depth without authority and clarity without prescription.

They are designed to support serious technical review, institutional
interpretation, and long-term public reference—while resisting premature
claims, capture, or overreach.

---

**End of Annexes README**
