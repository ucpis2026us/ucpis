# Notes and Contextual Documents

**Status:** Informative / Non-Normative  
**Authority:** Contextual only  
**Applies To:** Universal Cyber-Physical Interoperability Stack (UCPIS)

---

## Purpose of This Directory

The `docs/notes/` directory contains **contextual, pre-normative documents**
that preserve architectural motivation, design rationale, and explanatory
material related to UCPIS.

Documents in this directory are intentionally **not part of the canonical
UCPIS white paper or annex corpus**.

They exist to support:
- interpretation and review,
- contributor alignment,
- long-term architectural stewardship,

without expanding the scope, authority, or obligations of UCPIS.

---

## Normative Status

All documents in this directory:

- define **no requirements**
- specify **no interfaces**
- establish **no governance, compliance, or enforcement posture**
- introduce **no implementation mandates**

If any conflict arises between documents in this directory and the UCPIS
white paper or annexes, the **white paper takes precedence**.

---

## Intended Use

Documents in `docs/notes/` may be useful to:

- contributors seeking architectural context,
- reviewers evaluating design intent,
- readers questioning why certain architectural boundaries exist,
- future stewards responsible for interpretation rather than implementation.

They are **not** intended for:
- compliance use,
- certification,
- design substitution,
- implementation authority.

---

## Contents

### `interoperability-origin.md`
Contextual document capturing the **architectural motivation and problem
framing** that led to the development of UCPIS.

This note explains:
- the civilizational interoperability gap UCPIS addresses,
- why interoperability is treated as an architectural concern,
- why UCPIS is framed as a reference architecture rather than a product or
  standard.

---

### `constrained-hmi-design-note.md`
Design note describing the motivation, principles, and design considerations
for **Constrained Human–Machine Interfaces (Constrained HMIs)**.

This note:
- connects HMIs to Human Autonomy Classes,
- explains safety-bounded interface exposure,
- supports MVUE and reference implementation reasoning.

---

## Relationship to the White Paper

The canonical definition of UCPIS resides exclusively in:

- the UCPIS Public White Paper, and
- its associated annexes.

Documents in this directory provide **context only** and must not be cited as
defining UCPIS behavior, scope, or obligations.

---

## Summary

The `docs/notes/` directory exists to preserve **architectural memory without
architectural authority**.

By separating rationale from specification, UCPIS remains interpretable,
adaptable, and resistant to scope drift over time.

---

**End of Notes README**
