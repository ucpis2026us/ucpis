# UCPIS Documentation Directory

**Project:** Universal Cyber-Physical Interoperability Stack (UCPIS)  
**Applies To:** Public White Paper v1.4  
**Status:** Informative / Non-Normative  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Purpose of This Directory

The `docs/` directory contains **reader-facing and interpretive documentation**
intended to support understanding, navigation, and long-term stewardship of
the UCPIS architecture.

Documents in this directory are **not part of the canonical architecture** and
do not define requirements, interfaces, profiles, implementations, or authority.

Their role is to:

- help readers orient themselves,
- explain how to read and navigate the UCPIS corpus,
- prevent misinterpretation of scope or intent,
- preserve architectural clarity as the project ages,
- support institutional and archival review.

---

## Normative Status

All materials in `docs/` are **informative and non-normative**.

They:

- define no compliance obligations,
- specify no implementations,
- assert no governance authority,
- and must not be treated as architectural requirements.

If any conflict arises between documents in this directory and the UCPIS White
Paper or active Annexes, the **White Paper and Annexes take precedence**.

---

## Contents of This Directory

### Reader Guides

These documents assist readers in interpreting and navigating UCPIS correctly:

- **`architecture-overview.md`**  
  A concise, explanatory summary of the UCPIS v1.4 architecture, intended to
  help readers grasp the system quickly before engaging with the full white
  paper.  
  This document introduces **no new architecture** and derives entirely from
  the canonical white paper.

- **`how-to-read-ucpis.md`**  
  Explains how to approach the UCPIS documentation set, recommended reading
  order, and common misreadings to avoid.

- **`ucpis-at-a-glance.md`**  
  A one-page classification artifact summarizing what UCPIS is, what it is not,
  and the role it is intended to play.

- **`document-map.md`**  
  A conceptual map showing how UCPIS documents relate across layers
  (WHY / WHAT / DEPTH / READER ORIENTATION).

- **`interpretation-notes.md`**  
  Explicit guardrails against common misinterpretations, authority projection,
  or assumptions of implementability.

---

### Contextual Notes

The `docs/notes/` subdirectory contains **contextual and pre-normative design
rationale**.

These documents explain *why* architectural choices were made, without defining
UCPIS behavior, scope, authority, or obligations.

See:

- **`docs/notes/README.md`** — scope and posture of contextual notes
- **`docs/notes/interoperability-origin.md`** — civilizational interoperability motivation
- **`docs/notes/constrained-hmi-design-note.md`** — rationale for Constrained HMIs
- **`docs/notes/v1.5-activation-criteria.md`** — discipline document for future versioning

If any conflict arises, **canonical architecture documents take precedence**.

---

## Relationship to Other Repository Areas

The UCPIS repository is intentionally layered to prevent scope confusion:

- **`index.md`**  
  Canonical public landing page and entry point.

- **`white-paper/`**  
  Canonical architectural definition of UCPIS v1.4.

- **`annexes/`**  
  Architectural elaboration and depth (informative, non-normative).

- **`docs/`**  
  Reader guidance, interpretation, and contextual clarity.

This separation ensures durability, interpretability, and resistance to
premature institutionalization.

---

## What Does Not Belong Here

The `docs/` directory must **not** contain:

- implementation guidance or reference code,
- schemas, APIs, or executable artifacts,
- performance claims or benchmarks,
- examples framed as recommendations,
- future roadmaps or activation plans.

Such material, if ever appropriate, belongs only in explicitly scoped locations
and only after versioned architectural changes.

---

## Summary

The `docs/` directory exists to support **correct reading**, not to expand
architecture.

By separating interpretation from definition, UCPIS remains:

- understandable,
- reviewable,
- resistant to misuse,
- and stable over long time horizons.

---

**End of Docs README**
