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

- the **surface** presented t
