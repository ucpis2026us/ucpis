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
do not define requirements, interfaces, or authority.

Their role is to:
- help readers orient themselves,
- prevent misinterpretation of scope or intent,
- explain how to read and navigate the UCPIS corpus,
- preserve clarity as the project ages.

---

## Normative Status

All materials in `docs/` are **informative and non-normative**.

They:
- define no compliance obligations,
- specify no implementations,
- assert no governance authority,
- and must not be treated as architectural requirements.

If any conflict arises between documents in this directory and the UCPIS White
Paper or Annexes, the **White Paper and Annexes take precedence**.

---

## Contents of This Directory

### Reader Guides

These documents assist readers in interpreting and navigating UCPIS:

- **`how-to-read-ucpis.md`**  
  Explains how to approach the UCPIS documentation set, recommended reading
  order, and common misreadings to avoid.

- **`ucpis-at-a-glance.md`**  
  A one-page classification artifact describing what UCPIS is and is not.

- **`document-map.md`**  
  Visual and conceptual map of how UCPIS documents relate to one another.

- **`interpretation-notes.md`**  
  Explicit guardrails against common misinterpretations.

---

### Contextual Notes

The `docs/notes/` subdirectory contains **architectural rationale and design
intent** that is intentionally kept separate from canonical definitions.

See:
- `docs/notes/README.md`

Documents in `docs/notes/` explain *why* certain architectural choices were
made, but do not define UCPIS behavior or scope.

---

## Relationship to Other Repository Areas

Within the UCPIS repository, documentation is intentionally layered:

- **`index.md`**  
  Canonical public landing page.

- **`white-paper/`**  
  Canonical architectural reference.

- **`annexes/`**  
  Architectural elaboration and depth.

- **`docs/`**  
  Reader guidance, interpretation, and context.

This separation ensures clarity, durability, and resistance to scope creep.

---

## What Does Not Belong Here

The `docs/` directory must not contain:
- implementation guidance,
- reference code,
- schemas or APIs,
- performance claims,
- examples framed as recommendations,
- future roadmaps.

Such material, if ever appropriate, belongs in explicitly scoped locations and
only after versioned architectural changes.

---

## Summary

The `docs/` directory exists to support **correct reading**, not to expand the
architecture.

By separating interpretation from definition, UCPIS remains understandable,
reviewable, and stable over long time horizons.

---

**End of Docs README**
