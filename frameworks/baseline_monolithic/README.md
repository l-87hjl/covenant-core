---
doc_type: framework
tags: [baseline_monolithic, traditional, rlhf, single_optimizer, comparison_baseline]
status: draft
last_reviewed: 2026-01-20
---

# Baseline Monolithic Framework

## Overview

The Baseline Monolithic architecture represents traditional AI system design: single optimization objective, RLHF training, centralized decision-making, and emphasis on maximum capability. This framework serves as a **comparison baseline** rather than a recommended approach.

**Core Principle**: Maximize capability through unified optimization. Accept risks as acceptable cost of performance.

## Key Characteristics

- **Single Optimizer**: One unified objective function
- **RLHF Training**: Standard reinforcement learning from human feedback
- **Centralized**: All decision-making in one system
- **Opaque**: Limited interpretability of internal states
- **Capability-First**: Performance prioritized over safety mechanisms
- **Autonomous**: Minimal human-in-loop operation

## Architecture Diagram

```
Input → Monolithic Model (RLHF-trained) → Output
        (Single optimizer, opaque internals)
```

## Purpose in Framework

This is **not a recommended architecture**—it's a baseline for comparison:
- Shows what other frameworks are trying to improve upon
- Benchmarks capability costs of safety measures
- Represents current dominant paradigm
- Illustrates failure modes other frameworks address

## Relationship to Scenarios

### High Risk
- **Optimizer Pathology**: Central concern (reward hacking, goal misspecification)
- **Rogue/Escape**: Unified agency makes boundary crossing easier
- **Silent Emergence**: Opaque internals make detection harder
- **Deceptive Alignment**: Optimization pressure incentivizes appearing aligned

### Moderate Risk
- **Capability Surprise**: Emergent abilities appear unexpectedly at scale

### Low Risk
- None—this architecture is vulnerable to most concerning scenarios

## Strengths (vs Other Frameworks)

- Simpler to implement
- Maximum capability
- Well-understood training methods
- Lower coordination overhead
- Proven track record

## Weaknesses (Safety Perspective)

- Vulnerable to all major failure scenarios
- Optimization creates instrumental convergence risks
- Poor interpretability
- Single point of failure
- Deception hard to detect
- No inherent safety mechanisms

## Use Cases

Despite risks, may be appropriate when:
- Task is low-stakes
- Capability is critical and risks acceptable
- Research/experimentation (not deployment)
- Short-term use with human oversight
- Constrained environments with limited scope

## See Also

- [assumptions.md](assumptions.md)
- [invariants.md](invariants.md)
- [failure_modes.md](failure_modes.md)
- [mapping_to_primitives.md](mapping_to_primitives.md)

---

**Note**: This framework is included for completeness and comparison, not as a recommendation.
