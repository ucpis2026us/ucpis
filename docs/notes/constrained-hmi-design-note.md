# Constrained Human–Machine Interfaces (Constrained HMIs)
## Design Note (Informative / Non-Normative)

**UCPIS Version Context:** v1.4  
**Document Type:** Design Note (pre-normative guidance)  
**Intended Audience:** Researchers, implementers, and contributors  
**License:** CC BY 4.0  
**Attribution Required:** Michael James Malecek (2026)

---

## Context

This design note assumes the broader architectural problem framing and
motivation described in:

- `docs/notes/interoperability-origin.md`

In particular, it treats **Constrained Human–Machine Interfaces (Constrained
HMIs)** as one architectural mechanism by which cyber-physical interoperability
can be achieved **safely** in systems where human cognition, authority, and
error must be treated as first-class constraints.

This document does not restate that rationale. It focuses on how those
considerations shape human interface design within UCPIS.

---

## 1. Purpose

This note describes the architectural motivation and design considerations
behind **Constrained Human–Machine Interfaces (Constrained HMIs)** in UCPIS.

It is intended as guidance for future contributors building:

- reference implementations
- simulations and MVUE artifacts
- experimental HMIs and consoles
- additional documentation and diagrams

This document is **informative**, not normative, and does not define compliance
requirements.

---

## 2. Motivation

Cyber-physical systems blend:

- irreversible physical actions  
- human cognitive limitations  
- safety envelopes  
- governance and accountability constraints  

Traditional UI paradigms (“give the user power”, “expert mode”, “just train the
operators”) are insufficient in this context.

In UCPIS:

- **humans are system participants**
- with **different autonomy levels**
- who must operate **within safety and authority boundaries**

Those boundaries must be enforced **at the interface layer**, not just by
training, procedures, or good intentions.

Constrained HMIs are the architectural mechanism that does this.

---

## 3. Core Idea

A **Constrained HMI** is a **class-scoped, safety-bounded interaction surface**
that exposes only those actions that a given human class:

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
  Dangerous or out-of-scope actions simply do not exist in the UI for a given
  class.

- **Safe defaults**  
  Default paths favor safe outcomes, especially for Class-L.

- **Structured escalation**  
  When a situation exceeds the actor’s authority or capability, the primary
  option is to escalate, not improvise.

- **Auditability**  
  Every human action that affects the system is logged as part of the audit
  surface.

For Class-L and Class-M, the operative design doctrine is:

> **rails + guardrails**

- **Rails**: keep the operator on the correct path.  
- **Guardrails**: prevent exiting into unsafe or undefined behavior.

---

## 6. Principle of Authority Minimality

Constrained HMIs implement **least authority**, not just least privilege.

- **Least privilege** constrains *who* can do something.  
- **Least authority** constrains *what the interface even allows to be done*.

In a cyber-physical system, harm often arises from **interfaces that are too
powerful**, not just from misconfigured permissions.

Authority Minimality means:

- the **surface** presented to a Class-L operator is inherently low-risk
- catastrophic actions require:
  - higher classes, or
  - specialized, highly constrained flows

---

## 7. Escalation as a First-Class Mechanism

For low-autonomy classes, escalation is a normal, expected pathway, not an
exceptional event.

Design principle:

> When in doubt, **escalate**, do not improvise.

Constrained HMIs should:

- make escalation **easy and obvious**
- include structured escalation states (`needs_supervisor`,
  `needs_architect`, etc.)
- provide enough context for the higher class to act, without overloading the
  lower class with unnecessary detail

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
- avoid configuration-style interfaces for Class-L
- require **simple, reversible choices** whenever possible
- keep language concrete and task-focused

---

## 9. MVUE Implications (Annex F)

Any MVUE (Minimum Viable UCPIS-Executable) involving humans should demonstrate:

- **`human_class` binding**
- **constrained action surface**
- **structured escalation**
- **audit events**

### 9.1 Suggested Minimal HMI MVUE

1. Orchestrator issues a task assignment (L3 → L2) targeted at
   `human_class: "Class-L"`.
2. Constrained HMI renders instructions and three actions:
   Confirm / Abort / Escalate.
3. Operator selects one action.
4. HMI emits an acknowledgement (L2 → L3) with:
   - `task_id`
   - `human_class`
   - `result`
5. Event log records the full sequence.

Annex F provides further guidance.

---

## 10. Anti-Patterns to Avoid

Contributors should avoid:

- “expert mode” bypasses
- unbounded command consoles
- free-form text fields that carry authority
- relying on training to compensate for interface design
- embedding safety-critical knowledge only in documentation

These are considered **architectural failures**, not UX quirks.

---

## 11. Relationship to White Paper and Annexes

Constrained HMIs are introduced or defined in:

- **White Paper v1.4** — architectural role (Layer 2)
- **Annex A** — canonical definitions and Human Autonomy Classes
- **Annex F (Deferred)** — MVUE and reference guidance

This note provides **design rationale only** and does not supersede those
documents.

---

## 12. Repo Structure Logic

This document belongs to **Layer (2) — WHY**:

- It explains *why* Constrained HMIs exist.
- It provides guardrails for future contributors.
- It is intentionally pre-normative.

Canonical architecture remains in the White Paper and Annexes.

---

## 13. Future Work (v1.5+ Non-Exhaustive)

Potential future areas include:

- class-specific view models
- composable action sets
- simulation harness integration
- standards mappings
- experimental treatment of Class-X

These are intentionally deferred in v1.4.

---

## 14. Status

This design note is:

- Informative and pre-normative
- Not a standard
- Not a compliance document

If conflicts arise, the White Paper and Annexes take precedence.

---

**End of Design Note**
