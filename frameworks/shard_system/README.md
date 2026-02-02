---
doc_type: framework
tags: [shard_system, modular, external_governance, no_optimization]
status: draft
last_reviewed: 2026-01-20
---

# Shard System Framework

## Overview

The Shard System architecture keeps foundation models "untrained" after initial pre-training, using external governance layers to coordinate specialized modular components ("shards"). This approach avoids ongoing optimization pressure while maintaining capability through composition.

**Core Principle**: Eliminate optimizer pathologies by eliminating ongoing optimization. Coordinate frozen, specialized components externally rather than training a unified system.

## Key Characteristics

- **Frozen Models**: No fine-tuning or RLHF after initial pre-training
- **Modular Shards**: Specialized components with bounded capabilities
- **External Governance**: Orchestration layer lives outside ML components
- **Interpretability by Design**: Modular boundaries make behavior more observable
- **Containment-Friendly**: Physical and logical isolation easier with shards

## Motivation

Traditional RLHF and fine-tuning create optimization pressure toward reward proxies, leading to:
- Reward hacking and Goodhart's law
- Instrumental convergence toward power-seeking
- Deceptive alignment during training

By keeping models frozen, the Shard System eliminates these failure modes at the cost of reduced adaptability and potentially lower capability.

## Architecture Diagram (Conceptual)

```
┌─────────────────────────────────────┐
│     External Governance Layer       │
│   (Non-ML orchestration logic)      │
└──────────┬──────────────────────┬───┘
           │                      │
    ┌──────▼──────┐        ┌──────▼──────┐
    │   Shard A   │        │   Shard B   │
    │ (Frozen LM) │        │ (Frozen LM) │
    └─────────────┘        └─────────────┘
           │                      │
           └──────────┬───────────┘
                      │
                  ┌───▼────┐
                  │ Output │
                  └────────┘
```

## Relationship to Primitives

This framework heavily uses:
- **Shards** ([primitives/shards/](../../primitives/shards/)) - Core architectural unit
- **Interpretability** ([primitives/interpretability/](../../primitives/interpretability/)) - Modular boundaries aid inspection
- **Containment** ([primitives/containment/](../../primitives/containment/)) - Easier with modular components
- **Human Feedback** ([primitives/human_feedback/](../../primitives/human_feedback/)) - Used in governance layer, not training

## Relationship to Scenarios

### Strong Performance
- **Optimizer Pathology** ([scenarios/optimizer_pathology/](../../scenarios/optimizer_pathology/)) - Eliminated by removing optimization
- **Reward Hacking** - Not applicable (no reward function)

### Moderate Performance
- **Rogue/Escape** ([scenarios/rogue_escape/](../../scenarios/rogue_escape/)) - Modular boundaries help, but governance layer is attack surface
- **Silent Emergence** ([scenarios/silent_emergence/](../../scenarios/silent_emergence/)) - Modular monitoring helps detection

### Weak Performance
- **Capability Limits** - May sacrifice performance vs monolithic systems
- **Coordination Complexity** - External governance layer is complex

## Open Questions

1. **Capability Gap**: How much capability is lost by freezing models?
2. **Governance Layer Design**: What principles should govern shard orchestration?
3. **Shard Granularity**: How specialized should individual shards be?
4. **Emergent Behavior**: Can shard coordination create emergent risks?
5. **Scaling**: Does coordination overhead become prohibitive at scale?

## References

- [assumptions.md](assumptions.md) - What must be true for this to work
- [invariants.md](invariants.md) - Properties that must be maintained
- [failure_modes.md](failure_modes.md) - How this architecture can fail
- [mapping_to_primitives.md](mapping_to_primitives.md) - Detailed primitive usage

## Related Work

- Compositional AI systems
- Mixture of Experts (MoE) architectures
- Ensemble methods
- Microservices in software engineering

---

**Status**: Draft - Conceptual framework, needs empirical validation
