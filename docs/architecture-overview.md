# UCPIS v1.4 — Architecture Overview

**Status:** Informative / Non-Normative  
**Version Context:** v1.4  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)  

---

## Overview

The **Universal Cyber-Physical Interoperability Stack (UCPIS)** is an
**informative reference architecture** describing how heterogeneous
**cyber-physical systems** may interoperate through a **layered,
interface-first model** that treats real-world constraints as
first-class architectural inputs.

UCPIS is **not** a product, platform, standard, or implementation.
It defines **no compliance requirements**, **no certifications**, and
**no normative security controls**.

This document provides a concise, canonical explanation of the UCPIS
architecture as defined in **v1.4**, without expanding scope or authority.

---

## Core Architectural Claim

Industrial systems lack an interoperability foundation analogous to the
layered protocol architectures that enabled computing systems to scale,
interoperate, and evolve across vendors and environments.

UCPIS identifies the missing element as an **interface discipline** that
allows machines, software, and humans to be composed and substituted
safely across domains.

The primary unit of interoperability in UCPIS is the **interface
contract**, not the implementation.

---

## Three-Layer Conceptual Stack

UCPIS defines a **three-layer conceptual architecture** operating within
environmental and socio-technical context.

### Layer 1 — Physical

**Contains:**
Machines, robots, sensors, actuators, energy systems, material handling,
and logistics assets.

**Represents:**
Where **physical state** exists and where actions become **irreversible
or costly**.

**Architectural rule:**
Layer 1 is not exposed to low-autonomy human free-form control.
Physical actuation is mediated through constrained interaction surfaces
and governance-aware orchestration.

---

### Layer 2 — Human Interface / Mediation

**Contains:**
Constrained human–machine interfaces (**Constrained HMIs**), guided
workflows, confirmation, escalation, and exception handling.

**Represents:**
The **only routine participation surface** for humans in the stack.

**Architectural rule:**
All human actions are **class-scoped** and **authority-bounded**.
Humans interact exclusively through explicit interface contracts that
limit exposure, enforce safety envelopes, and provide structured
escalation when conditions exceed scope.

---

### Layer 3 — Cyber / Control / Governance

**Contains:**
Orchestration, scheduling, planning, policy definition, audit surfaces,
and system-level coordination logic.

**Represents:**
Where automation and governance logic reside and where constraints are
enforced structurally.

**Architectural rule:**
Humans do not receive arbitrary access to Layer 3.
Human participation is always mediated via Layer 2, producing
audit-ready events rather than free-form command authority.

---

Interfaces — not implementations — are the primary unit of
interoperability.

---

## Interface-First and Agent-Agnostic Design

UCPIS is **interface-first**:

- Systems interoperate by conforming to explicit, stable interface
  contracts.
- Implementations may vary, evolve, or be replaced without altering the
  architecture.

UCPIS is **agent-agnostic**:

- The same interface may be exercised by software agents, human actors,
  or hybrid systems.
- **Authority and accountability are human-only** and must be assigned
  explicitly through constraints and governance posture.

---

## Constraints as First-Class Architectural Inputs

UCPIS treats real-world constraints as structural shaping forces,
including:

- Energy and electrical/thermal load
- Human labor, cognition, and autonomy limitations
- Safety envelopes and hazard containment
- Governance, legitimacy, and auditability
- Environmental and biological context

Constraints are integrated architecturally rather than handled as
exceptions, enabling graceful degradation under stress.

---

## Human Participation Model (By Reference)

Humans are treated as **bounded system participants**, not generic
operators.

UCPIS models human participation through:

- **Human Autonomy Classes** (Annex A) — capability and authority scoping
- **Constrained HMIs** (Annex A; design rationale in `docs/notes/`) —
  class-bound interaction surfaces

Key posture:

- Classes are **informational**, **non-hierarchical**, and
  **non-diagnostic**
- They exist solely to scope interface exposure and safeguard design

---

## Environmental and Biological Context

UCPIS explicitly acknowledges that cyber-physical systems operate in
environments that may include non-human biological entities.

Such entities:

- Are **not agents**
- Hold **no authority**
- Are **not governance participants**
- Are treated as **contextual constraints** affecting safety and
  resilience

---

## MVUE — Minimum Viable UCPIS-Executable (Conceptual Only)

UCPIS defines an **MVUE** as the smallest executable artifact capable of
exercising UCPIS interfaces across layers.

In v1.4:

- MVUE is **conceptual only**
- No executable artifacts are required or endorsed
- Reference implementation guidance is authored but deferred (Annex F)

---

## Deferred Materials and Activation Discipline

To prevent premature capture, UCPIS includes authored-but-deferred
annexes:

- **Annex F** — Reference Implementation Guidelines (Deferred)
- **Annex G** — Governance Models (Deferred)
- **Annex H** — Interoperability Profiles (Deferred)

These remain inactive until justified by external evidence and adoption.
Their presence does not imply activation, authority, or readiness.

---

## One-Sentence Definition

**UCPIS v1.4 is a three-layer, interface-first reference architecture that
describes how cyber-physical systems—including humans and environmental
context—may interoperate safely through explicit interface contracts and
constraint-aware mediation, without asserting governance, compliance, or
implementation authority.**

---

**End of Architecture Overview**
