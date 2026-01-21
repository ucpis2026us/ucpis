# Prompts — Generation and Continuity Artifacts

**Project:** Universal Cyber-Physical Interoperability Stack (UCPIS)  
**Status:** Informative / Non-Normative  
**Version Context:** v1.4  

---

## Purpose

This directory contains **prompt artifacts** used to generate, regenerate, and
internally carry forward UCPIS documentation in a disciplined and consistent
manner.

Prompt files are **tooling and continuity aids only**.  
They are **not architectural documents**, define **no requirements**, and
establish **no authority, policy, or roadmap**.

If any conflict arises between prompt artifacts and published documents, the
**UCPIS White Paper and active annexes always take precedence**.

---

## What This Directory Is For

The `prompts/` directory exists to support:

- reproducibility of the public UCPIS documentation corpus,
- internal continuity of architectural intent,
- disciplined evolution across versions,
- prevention of accidental scope drift.

Prompts encode **constraints, posture, and guardrails**, not outcomes.

---

## Contents

### `UCPIS_White_Paper_Master_Prompt.md`

The **canonical public master prompt** used to generate and regenerate the
UCPIS v1.4 white paper, annexes, and supporting documents.

This prompt:

- reflects the locked v1.4 architectural posture,
- encodes non-goals and interpretation constraints,
- ensures internal consistency across documents,
- is suitable for public archival and audit.

It does **not** define implementations, standards, governance, or future plans.

---

### `UCPIS_v1.5_Upgrade_Knowledge_Transfer_Prompt.md`

An **internal continuity and intent-preservation artifact** used to carry
forward preparation logic for a potential future v1.5 release.

This document:

- does **not** activate v1.5 work,
- does **not** modify the public architecture,
- does **not** constitute a roadmap or commitment,
- records internal guardrails, risks, and decision criteria only.

Its presence does not imply that a v1.5 release is planned or imminent.

---

## Interpretation Rules

When reading or using materials in this directory:

- Prompts are **inputs to documentation generation**, not outputs.
- Prompts describe **how documents are produced**, not what UCPIS requires.
- No prompt file supersedes published architecture.
- Prompt content should never be cited as UCPIS policy or specification.

If interpretation is unclear, defer to:

1. The UCPIS White Paper  
2. Active Annexes (A–E)  
3. Reader guidance documents in `docs/`

---

## Status

This directory is:

- **Informative and non-normative**
- Intended for maintainers and stewards
- Not intended for implementation or compliance use

Its structure may evolve without constituting an architectural change.

---

**End of Prompts README**
