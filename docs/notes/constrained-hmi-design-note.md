# Constrained Human–Machine Interfaces (Constrained HMIs)
## Design Note (Informative / Non-Normative)

**UCPIS Version Context:** v1.4  
**Document Type:** Design Note (pre-normative guidance)  
**Intended Audience:** Researchers, implementers, and contributors  
**License:** CC BY 4.0  
**Attribution Required:** Michael James Malecek (2026)

---

## 1. Purpose

This note describes the architectural motivation and design considerations behind **Constrained Human–Machine Interfaces (Constrained HMIs)** in UCPIS.

It is intended as guidance for future contributors building:

- reference implementations
- simulations and MVUE artifacts
- experimental HMIs and consoles
- additional documentation and diagrams

This document is **informative**, not normative, and does not define compliance requirements.

---

## 2. Motivation

Cyber-physical systems blend:

- irreversible physical actions  
- human cognitive limitations  
- safety envelopes  
- governance and accountability constraints  

Traditional UI paradigms (“give the user power”, “expert mode”, “just train the operators”) are insufficient in this context.

In UCPIS:

- **humans are system participants**
- with **different autonomy levels**
- who must operate **within safety and authority boundaries**

Those boundaries must be enforced **at the interface layer**, not just by training, procedures, or good intentions.

Constrained HMIs are the architectural mechanism that does this.

---

## 3. Core Idea

A **Constrained HMI** is a **class-scoped, safety-bounded interaction surface** that exposes only those actions that a given human class:

- **may**
- **can**
- **should**
- **is trusted to**

execute within a cyber-physical system.

In UCPIS, the HMI is therefore:

> not just a UI artifact, but an **authority boundary**.

Constrained HMIs are where **Human Autonomy Classes** are translated into:

- visible options
- permissible actions
- escalation paths
- audit events

---

## 4. Mapping HMIs to Human Autonomy Classes

Constrained HMIs derive from **Human Autonomy Classes** (see Annex A).

High-level mapping:

| Class | Capabilities (informal summary) | HMI Exposure (conceptual) |
|------|----------------------------------|---------------------------|
| **Class-L** | Low-autonomy operators; narrow, structured tasks | Rails-only: confirm / abort / escalate. No free-form commands, no policy edit, no direct actuation programming. |
| **Class-M** | Technicians / supervisors; SOPs + local troubleshooting | Bounded diagnostics; limited mode changes; targeted overrides with strong constraints; structured escalation. |
| **Class-H** | High-autonomy architects / system-formers | Structural controls (policy, configuration, architecture); often non-graphical tools (code, schema, policy editors). |
| **Class-X** | Augmented / composite actors (informational in v1.4) | Not normatively defined in v1.4; any treatment is experimental and must be clearly labeled as such. |

The goal is to prevent the common failure mode:

> “The UI let them do something they were never meant to do.”

In UCPIS, that is treated as an **architectural error**, not a “user mistake”.

---

## 5. Safety Posture

Constrained HMIs enforce safety through:

- **Action omission**  
  Dangerous or out-of-scope actions simply do not exist in the UI for a given class.

- **Safe defaults**  
  Default paths favor safe outcomes, especially for Class-L.

- **Structured escalation**  
  When a situation exceeds the actor’s authority or capability, the primary option is to escalate, not improvise.

- **Auditability**  
  Every human action that affects the system is logged as part of the audit surface.

For Class-L and Class-M, the operative design doctrine is:

> **rails + guardrails**

- **Rails**: keep the operator on the correct path.  
- **Guardrails**: prevent exiting into unsafe or undefined behavior.

---

# Constrained Human–Machine Interfaces (Constrained HMIs)
## Design Note (Informative / Non-Normative)

**UCPIS Version Context:** v1.4  
**Document Type:** Design Note (pre-normative guidance)  
**Intended Audience:** Researchers, implementers, and contributors  
**License:** CC BY 4.0  
**Attribution Required:** Michael James Malecek (2026)

---

## 1. Purpose

This note describes the architectural motivation and design considerations behind **Constrained Human–Machine Interfaces (Constrained HMIs)** in UCPIS.

It is intended as guidance for future contributors building:

- reference implementations
- simulations and MVUE artifacts
- experimental HMIs and consoles
- additional documentation and diagrams

This document is **informative**, not normative, and does not define compliance requirements.

---

## 2. Motivation

Cyber-physical systems blend:

- irreversible physical actions  
- human cognitive limitations  
- safety envelopes  
- governance and accountability constraints  

Traditional UI paradigms (“give the user power”, “expert mode”, “just train the operators”) are insufficient in this context.

In UCPIS:

- **humans are system participants**
- with **different autonomy levels**
- who must operate **within safety and authority boundaries**

Those boundaries must be enforced **at the interface layer**, not just by training, procedures, or good intentions.

Constrained HMIs are the architectural mechanism that does this.

---

## 3. Core Idea

A **Constrained HMI** is a **class-scoped, safety-bounded interaction surface** that exposes only those actions that a given human class:

- **may**
- **can**
- **should**
- **is trusted to**

execute within a cyber-physical system.

In UCPIS, the HMI is therefore:

> not just a UI artifact, but an **authority boundary**.

Constrained HMIs are where **Human Autonomy Classes** are translated into:

- visible options
- permissible actions
- escalation paths
- audit events

---

## 4. Mapping HMIs to Human Autonomy Classes

Constrained HMIs derive from **Human Autonomy Classes** (see Annex A).

High-level mapping:

| Class | Capabilities (informal summary) | HMI Exposure (conceptual) |
|------|----------------------------------|---------------------------|
| **Class-L** | Low-autonomy operators; narrow, structured tasks | Rails-only: confirm / abort / escalate. No free-form commands, no policy edit, no direct actuation programming. |
| **Class-M** | Technicians / supervisors; SOPs + local troubleshooting | Bounded diagnostics; limited mode changes; targeted overrides with strong constraints; structured escalation. |
| **Class-H** | High-autonomy architects / system-formers | Structural controls (policy, configuration, architecture); often non-graphical tools (code, schema, policy editors). |
| **Class-X** | Augmented / composite actors (informational in v1.4) | Not normatively defined in v1.4; any treatment is experimental and must be clearly labeled as such. |

The goal is to prevent the common failure mode:

> “The UI let them do something they were never meant to do.”

In UCPIS, that is treated as an **architectural error**, not a “user mistake”.

---

## 5. Safety Posture

Constrained HMIs enforce safety through:

- **Action omission**  
  Dangerous or out-of-scope actions simply do not exist in the UI for a given class.

- **Safe defaults**  
  Default paths favor safe outcomes, especially for Class-L.

- **Structured escalation**  
  When a situation exceeds the actor’s authority or capability, the primary option is to escalate, not improvise.

- **Auditability**  
  Every human action that affects the system is logged as part of the audit surface.

For Class-L and Class-M, the operative design doctrine is:

> **rails + guardrails**

- **Rails**: keep the operator on the correct path.  
- **Guardrails**: prevent exiting into unsafe or undefined behavior.

---

## 6. Principle of Authority Minimality

Constrained HMIs implement **least authority**, not just least privilege.

- **Least privilege** constrains *who* can do something.  
- **Least authority** constrains *what the interface even allows to be done*.

In a cyber-physical system, harm often arises from **interfaces that are too powerful**, not just from misconfigured permissions.

Authority Minimality means:

- the **surface** presented to a Class-L operator is inherently low-risk
- catastrophic actions require:
  - higher classes, *or*
  - specialized, highly constrained flows

---

## 7. Escalation as a First-Class Mechanism

For low-autonomy classes, escalation is a normal, expected pathway, not an exceptional event.

Design principle:

> When in doubt, **escalate**, do not improvise.

Constrained HMIs should:

- make escalation **easy and obvious**
- include structured escalation states (`needs_supervisor`, `needs_architect`, etc.)
- provide enough context for the higher class to act, without overloading the lower class with unnecessary details

Escalation is a **success path**, not a failure path.

---

## 8. Cognitive Load Assumptions

Constrained HMIs assume realistic human cognitive limitations:

- limited working memory
- limited error recovery ability
- bounded symbolic reasoning
- limited temporal prediction and risk modeling

These are treated as **system-level constraints**, not training deficits.

Design implications:

- prefer **single-decision** steps over multi-branch trees
- avoid “configuration UIs” for Class-L altogether
- require **simple, reversible choices** whenever possible
- keep language concrete and task-focused, not abstract or policy-heavy

---

## 9. MVUE Implications (Annex F)

Any MVUE (Minimum Viable UCPIS-Executable) involving humans should demonstrate:

- **`human_class` binding**  
  The scenario declares which class is exercising the interface.

- **Constrained action surface**  
  For Class-L, this typically means only `confirm`, `abort`, and `escalate`.

- **Structured escalation**  
  At least one path where the appropriate behavior is to escalate.

- **Audit events**  
  Every human action is logged with message IDs, correlation IDs, and timestamps.

### 9.1 Suggested Minimal HMI MVUE

A minimal MVUE scenario that exercises Constrained HMI:

1. Orchestrator issues a **Task Assignment** (L3 → L2) targeted at `human_class: "Class-L"`.
2. Constrained HMI renders:
   - instructions
   - three buttons: Confirm / Abort / Escalate
3. Operator selects one of the safe actions.
4. HMI emits an **Acknowledgement** (L2 → L3) with:
   - `task_id`
   - `human_class`
   - `result` (`confirm` / `abort` / `escalate`)
5. Event log records the full sequence for replay.

Annex F provides more detail on MVUE structure and recommended patterns.

---

## 10. Anti-Patterns to Avoid

Contributors should avoid:

- **“Let the user override it”** as the default pattern  
- **“Expert mode” / “Advanced mode” escapes** that bypass class-based constraints  
- **Unbounded command consoles** (especially for Class-L / Class-M)  
- **Free-form text fields** that effectively carry authority (e.g., ad hoc code, unbounded expressions)  
- **Assuming training compensates for interface design**  
- **Embedding safety-critical knowledge only in documentation** rather than constraining the interface itself

In UCPIS, these are considered **architectural failures**, not UX quirks.

---

## 11. Relationship to White Paper and Annexes

Constrained HMIs appear across multiple documents:

- **White Paper (v1.4)**  
  - Introduces Constrained HMI at an architectural level (Layer 2, human participation model).  

- **Annex A — Definitions, Terminology, and Taxonomy**  
  - Provides the canonical definition of **Constrained HMI**.  
  - Defines **Human Autonomy Classes** and their design doctrines.  

- **Annex F — Reference Implementation Guidelines**  
  - Describes how MVUEs and reference harnesses should exercise Constrained HMIs.  
  - Provides field-level patterns (e.g., `human_class`, `allowed_actions`).  

- **Future Annex H — Interoperability Profiles (Deferred)**  
  - May define domain-specific patterns for class-binding and HMI behavior.

This design note is intended to sit **alongside** those documents, not replace or supersede them.

---

## 12. Repo Structure Logic

In open technical projects, documentation usually falls into four conceptual layers:

1. **WHAT exists**  
   - Architecture, vocabulary, and conceptual model.  
   - For UCPIS, this is primarily:  
     - `white-paper/index.md`  
     - `white-paper/annex-a.md` through `annex-h.md`  

2. **WHY it exists**  
   - Design rationale, tradeoffs, and intent behind architectural choices.  
   - This file — `docs/notes/constrained-hmi-design-note.md` — is part of this layer.  
   - Future design notes (e.g., for MVUE, governance posture, AI-as-load) also belong here.

3. **HOW to use or implement it**  
   - Implementation guidelines, reference harnesses, MVUE examples, and code-adjacent docs.  
   - For UCPIS, this is expected to live in:  
     - `docs/mvue/`  
     - `docs/impl/`  
     - code examples and schemas referenced by Annex F.  

4. **WHERE it applies**  
   - Domain-specific profiles, mappings to particular industries, standards alignment.  
   - For UCPIS, this will live primarily in:  
     - `white-paper/annex-e.md` (standards alignment)  
     - `white-paper/annex-h.md` (interoperability profiles, deferred)  

### 12.1 Where This File Fits

This design note is part of **layer (2) — WHY**:

- It explains **why** Constrained HMIs exist in UCPIS.
- It gives contributors mental models and guardrails.
- It is intentionally **pre-normative** and may evolve based on experience.

By keeping this in `/docs/notes/`, we preserve a clean separation between:

- **Canonical architecture** (White Paper + Annexes), and  
- **Implementation-facing design rationale** (this and similar notes).

---

## 13. Future Work (v1.5+ Non-Exhaustive)

Potential future areas related to Constrained HMIs include:

- Class-specific **view models** (recommended HMI structures per class)
- Composable **action sets** (reusable HMI patterns with clear semantics)
- Simulation harness integration (e.g., headless HMI agents)
- Mapping to industrial standards (ISA-95/88, IEC 61508/62061, etc.)
- Experimental treatment of **Class-X** (augmented/composite actors)

These topics are intentionally deferred in v1.4.

---

## 14. Status

This design note is:

- **Informative and pre-normative**
- **Not a standard**, and does not define conformance
- A guidance artifact for future experimentation and iteration

If conflicts arise between this note and the White Paper or Annex A,
the White Paper and Annexes take precedence for v1.4.

---

**End of Design Note**
