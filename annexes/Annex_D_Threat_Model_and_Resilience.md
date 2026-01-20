# Annex D — Threat Model & Resilience

**Status:** Informative / Non-Normative  
**UCPIS Version:** v1.4  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

**Attribution Required:**  
Michael James Malecek (2026)

**Canonical Repository:**  
https://github.com/ucpis2026us

**Contact:**  
ucpis2026@gmail.com

---

This annex documents threat assumptions, failure modes, and resilience principles
for systems built using the Universal Cyber-Physical Interoperability Stack (UCPIS).

UCPIS treats human variability, technical failure, and environmental interaction
as **design inputs**, not exceptional fault conditions. Resilience is achieved
structurally through layered constraints, bounded authority, and adaptive response.

---

## D.1 Threat Model Scope

UCPIS threat modeling encompasses:
- Human-in-the-loop variability
- Automation and system faults
- Environmental and biological interaction
- Organizational and governance risks

Threats are assumed to arise from **normal operation under real-world conditions**,
not only from malicious intent or misuse.

---

## D.5 Environmental and Biological Risk Factors (Informational)

Cyber-physical systems may operate in environments containing non-human biological
entities, including wildlife and domesticated animals, as defined in Annex A.13.

Such entities are **not threat actors**, **not accountable agents**, and **not
participants in governance or control**, but they may introduce risk through
unpredictable interaction with physical systems.

Examples include:
- Unexpected movement into operational zones
- Interference with sensors, infrastructure, or logistics
- Behavioral responses to noise, light, or mechanical motion

Resilient systems assume:
- Non-symbolic behavior
- Lack of compliance or predictability
- No corrective intent

Mitigation focuses on **design adaptation**, not deterrence or punishment.

---

## D.6 Human-in-the-Loop Failure Modes by Class

UCPIS anticipates human error and variability as inherent system properties.
Human-in-the-loop failure modes are classified by Human Autonomy Class
(see Annex A.12) and mitigated structurally.

Human actors remain the **only biological entities** assigned authority,
responsibility, and accountability within the system.

---

### D.6.1 Class-L Failure Modes

**Failure Modes**
- Task omission
- Incorrect task sequencing
- Unsafe action under stress or confusion

**Mitigations**
- Physical and logical interlocks
- Forced sequencing and confirmation
- Elimination of discretionary unsafe actions
- Environmental safeguards that prevent hazardous interaction
  regardless of operator behavior

---

### D.6.2 Class-M Failure Modes

**Failure Modes**
- Misdiagnosis of system state
- Delayed or inappropriate escalation
- Improper override attempts

**Mitigations**
- Escalation thresholds and timers
- Authority boundaries enforced by design
- Mandatory logging and audit trails
- Environmental anomaly alerts routed for supervisory review

---

### D.6.3 Class-H Failure Modes

**Failure Modes**
- Policy or architectural misdesign
- Ethical or strategic misalignment
- Over-concentration of authority
- Failure to account for environmental or biological interaction

**Mitigations**
- Multi-review design and governance processes
- Explicit constraint and assumption modeling
- Separation of design authority and execution control
- Inclusion of environmental and biological risk scenarios
  in architectural review and simulation

---

### D.6.4 Class-X Failure Modes (Informational / Future)

**Failure Modes**
- Amplified error propagation
- Human–AI misalignment
- Automation bias
- Misinterpretation of environmental signals by composite systems

**Status**
Documented for awareness only. No formal controls are defined in UCPIS v1.4.

---

## D.7 Resilience Principles

Across all classes and environments, UCPIS resilience is grounded in the following
principles:

- **Assume fallibility:** Human, machine, and environment are all imperfect
- **Bound authority:** No single actor can induce catastrophic failure
- **Design for absorption:** Systems degrade safely under stress
- **Separate blame from design:** Failure informs architecture, not punishment
- **Prioritize safety over throughput:** Especially in mixed human–biological environments

These principles apply regardless of whether humans, automated systems, or
non-human biological entities are present in the operational context.

---

### End of Annex D
