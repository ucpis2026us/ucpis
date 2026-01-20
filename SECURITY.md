# Security Statement

**UCPIS Version:** v1.4  
**Status:** Informative / Non-Normative  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)  
**Attribution Required:** Michael James Malecek (2026)

---

## Scope and Position

The Universal Cyber-Physical Interoperability Stack (UCPIS) v1.4 defines
**no normative security controls**.

UCPIS is an **informative reference architecture**, not a security standard,
certification program, or compliance framework. No security requirements,
assurance claims, or enforcement mechanisms are mandated or implied by
this work.

---

## Security as a Design Constraint

Within UCPIS, security is treated as a **context-dependent constraint**
that must be addressed by implementers, operators, regulators, or
independent standards bodies appropriate to the deployment environment.

Security considerations vary by:
- Operational domain
- Jurisdiction and regulatory regime
- Threat environment
- System criticality
- Human participation model
- Environmental and biological context

UCPIS does not prescribe how these factors are resolved.

---

## Relationship to Threat Modeling and Resilience

UCPIS addresses risk at the **architectural level**, not the control level.

As described in **Annex D — Threat Model & Resilience**, UCPIS assumes:
- Human variability
- Automation and system failure
- Environmental and biological interaction
- Organizational and governance risk

Resilience is achieved through **structural design principles**
(e.g., bounded authority, interface constraints, separation of concerns),
not through specified security mechanisms.

---

## Non-Human Biological Context

UCPIS architectures may operate in environments that include non-human
biological entities (e.g., wildlife), as described in Annex A and Annex C.

Such entities:
- Are not threat actors
- Are not accountable agents
- Do not participate in security or governance

Their presence informs **safety, resilience, and environmental constraints**,
not security policy or enforcement.

---

## Explicit Non-Claims

UCPIS does **not**:
- Define security profiles
- Specify threat mitigations
- Mandate authentication, authorization, or cryptographic controls
- Establish assurance levels or certifications
- Replace or supersede existing security standards or regulations

Any security guidance, if produced in the future, would be published
separately and explicitly scoped.

---

## Reporting and Disclosure

UCPIS does not operate a vulnerability disclosure or incident response
program.

Security issues related to specific implementations should be reported
to the relevant implementers, operators, vendors, or regulatory authorities.

---

## Summary

UCPIS v1.4 intentionally limits its role in security to **architectural
awareness and boundary-setting**.

Security remains the responsibility of those who design, deploy, regulate,
and operate systems built using UCPIS concepts.

---

### End of Security Statement
