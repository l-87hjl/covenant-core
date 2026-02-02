---
doc_type: primitive
tags: [containment, isolation, boundaries, access_control]
status: draft
last_reviewed: 2026-01-20
---

# Containment Primitive

## Definition

**Containment** comprises physical, logical, and incentive-based boundaries that limit AI system scope of action and access to resources.

## Purpose

- Prevent unauthorized resource access
- Limit damage from failures or misalignment
- Create observable boundaries
- Enable gradual capability expansion

## Types of Containment

### Physical Containment
- Air-gapped systems
- Isolated hardware
- Secure facilities
- Network segmentation

### Logical Containment
- Access control lists
- Permission systems
- Sandbox environments
- Resource quotas

### Incentive-Based Containment
- Economic costs of boundary violations
- Monitoring and detection
- Reputation systems
- Legal liability

## Key Properties

1. **Boundary Enforcement**: Limits are actively maintained
2. **Observability**: Boundary violations are detectable
3. **Defense in Depth**: Multiple containment layers
4. **Graceful Degradation**: Breaches are contained

## Used By Frameworks

- **All frameworks**: Essential baseline safety measure
- **Shard System**: Modular boundaries = containment mechanism
- **Mesh/Distributed**: Network segmentation between nodes
- **Baseline Monolithic**: External containment only

## Benefits

- Physical limits on actions
- Reduces attack surface
- Enables monitoring at boundaries
- Limits cascading failures

## Costs

- Reduced capability (by design)
- Operational complexity
- May create false sense of security
- Sophisticated AI may find bypasses

## See Also

- [interfaces.md](interfaces.md)
- [known_patterns.md](known_patterns.md)
- [open_questions.md](open_questions.md)
