# Annex A — Definitions Terminology Taxonomy

This annex defines key terms used throughout UCPIS.

- **Interface:** A defined boundary through which systems exchange
  information or control.
- **Constraint:** A real-world limitation shaping allowable behavior.
- **Interoperability:** The ability of heterogeneous systems to exchange
  meaningfully interpretable information.
- **Layer:** A conceptual separation of concerns within the stack.

All definitions are informational and non-normative.

This annex defines canonical terms, classifications, and concepts used throughout
the Universal Cyber-Physical Interoperability Stack (UCPIS). Definitions in this
annex are normative unless explicitly stated otherwise.

---

## A.12 Human Autonomy Classes

UCPIS models human participants as first-class system actors. Human Autonomy Classes
are descriptive constructs used to inform interface design, authority boundaries,
and safety assumptions across the stack.

These classes are not evaluative judgments of human worth or status. They exist
solely to support safe, scalable, and predictable system design.

---

### Class-L — Low-Autonomy Operators

**Capabilities**
- Limited planning and task sequencing
- Constrained symbolic reasoning
- Reduced executive function and error recovery
- Limited temporal reasoning and safety judgment

**Primary Function**
- Execute narrowly defined, highly structured tasks

**Design Doctrine**
> Make the correct action the default; make dangerous actions impossible.

---

### Class-M — Mid-Autonomy Technicians / Supervisors

**Capabilities**
- Execute and oversee standard operating procedures (SOPs)
- Perform basic diagnostics and troubleshooting
- Escalate anomalies appropriately
- Coordinate small teams or workcells

**Primary Function**
- Maintain operational continuity within defined bounds

**Design Doctrine**
> Provide leverage with rails and guardrails.

---

### Class-H — High-Autonomy / High-Leverage Architects

**Capabilities**
- System-level reasoning
- Cross-domain integration
- Long-horizon planning
- Ethical, strategic, and institutional judgment

**Primary Function**
- Define architecture, policy, and system constraints

**Design Doctrine**
> Amplify structurally — one Class-H can shape thousands of workcells.

---

### Class-X — Augmented / Composite Actors (Informational)

**Capabilities**
- Human actors operating in concert with advanced tools or AI systems

**Status**
Class-X is informational only in UCPIS v1.3. No normative requirements,
interfaces, or governance assumptions are defined at this stage.
