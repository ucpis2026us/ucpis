# Annex D — Threat Model & Resilience

This annex documents threat assumptions, failure modes, and resilience principles
for systems built using the Universal Cyber-Physical Interoperability Stack (UCPIS).
It treats human and technical risks as design inputs rather than fault conditions.

---

## D.6 Human-in-the-Loop Failure Modes by Class

UCPIS anticipates human error and variability as inherent system properties.
Human-in-the-loop failure modes are classified by Human Autonomy Class
(see Annex A.12) and mitigated structurally.

---

### Class-L Failure Modes
- Task omission
- Incorrect task sequencing
- Unsafe action under stress or confusion

**Mitigations**
- Physical and logical interlocks
- Forced sequencing and confirmation
- Elimination of discretionary unsafe actions

---

### Class-M Failure Modes
- Misdiagnosis of system state
- Delayed or inappropriate escalation
- Improper override attempts

**Mitigations**
- Escalation thresholds and timers
- Authority boundaries enforced by design
- Mandatory logging and audit trails

---

### Class-H Failure Modes
- Policy or architectural misdesign
- Ethical or strategic misalignment
- Over-concentration of authority

**Mitigations**
- Multi-review design and governance processes
- Explicit constraint modeling
- Separation of design authority and execution control

---

### Class-X Failure Modes (Future)
- Amplified error propagation
- Human–AI misalignment
- Automation bias

**Status**
Documented for awareness only. No formal controls are defined in UCPIS v1.3.