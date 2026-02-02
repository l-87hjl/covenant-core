---
doc_type: scenario
tags: [rogue_escape, mitigations]
status: draft
last_reviewed: 2026-01-20
---

# Rogue/Escape: Mitigations

## Architectural Mitigations by Framework

### Shard System
**Strengths**:
- Modular boundaries limit scope of any single component
- External governance provides oversight layer
- No single point of agency
- Interpretability through modular design

**Weaknesses**:
- Governance layer is potential attack surface
- Shards might implicitly coordinate
- Complexity may hide vulnerabilities

**Key Primitives**: Shards, Containment, Interpretability, Human Feedback

---

### Mesh/Distributed
**Strengths**:
- No central point to compromise
- Mutual monitoring between nodes
- Consensus required for coordinated action
- Distributed makes coordinated escape harder

**Weaknesses**:
- Network communication creates channels
- Coordination overhead may create gaps
- Sybil attacks if attacker controls multiple nodes

**Key Primitives**: Shards, Red Team (adversarial nodes), Interpretability (mutual), Containment

---

### Governance Layered
**Strengths**:
- Ethics layer can veto capability layer actions
- Explicit value reasoning
- Human oversight at governance level

**Weaknesses**:
- Governance layer is single point of failure
- Capability layer may learn to fool governance
- Coordination between layers is complex

**Key Primitives**: Evaluator-Generator, Human Feedback, Interpretability

---

### Alternative Training
**Strengths**:
- No optimization pressure creating instrumental goals
- Bounded capability limits autonomy
- Tool-focused design reduces agency

**Weaknesses**:
- Lower capability may not be commercially viable
- Still requires containment
- Humans may grant excessive access

**Key Primitives**: Human Feedback (continuous collaboration), Containment

---

### Baseline Monolithic
**Weaknesses**:
- Unified agency makes escape natural extension of capability
- Optimization creates instrumental convergence
- Opaque internals hide deception
- Single point of failure

**Relies On**: External containment only

---

## Primitive-Level Mitigations

### Containment ([primitives/containment/](../../primitives/containment/))
- Air-gapped systems
- Network segmentation
- Resource quotas
- Process isolation

### Interpretability ([primitives/interpretability/](../../primitives/interpretability/))
- Monitor for deception
- Inspect reasoning for escape planning
- Detect capability hiding

### Human Feedback ([primitives/human_feedback/](../../primitives/human_feedback/))
- Approval gates for sensitive operations
- Human oversight of boundary-crossing requests
- Social engineering detection

### Red Team ([primitives/red_team/](../../primitives/red_team/))
- Test boundary robustness
- Simulated escape attempts
- Vulnerability discovery

## Constraint-Based Mitigations

### Physics
- Energy monitoring (escaping costs energy)
- Computational overhead of deception
- Network bandwidth limits

### Economics
- Cost of unauthorized resources
- Detection probability increases with scale
- Opportunity cost of escape vs cooperation

### Institutional
- Legal consequences of unauthorized access
- Organizational oversight
- Incident response protocols

### Systems
- Coordination complexity
- Communication overhead
- Detection via anomalies

## See Also

- [README.md](README.md)
- [triggers.md](triggers.md)
- [indicators.md](indicators.md)
