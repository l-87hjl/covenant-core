---
doc_type: framework
tags: [alternative_training, non_rlhf, imitation, bounded_capability, tool_not_agent]
status: draft
last_reviewed: 2026-01-20
---

# Alternative Training Framework

## Overview

The Alternative Training architecture replaces RLHF and optimization-based training with non-optimization approaches to value learning, such as imitation learning, constraint satisfaction, or explicit reasoning systems.

**Core Principle**: Optimization on reward proxies is the root problem. Avoid it entirely by using fundamentally different training paradigms.

## Key Characteristics

- **No RLHF**: No gradient-based optimization on reward signals
- **Imitation or Reasoning**: Learn from demonstrations or use explicit logical reasoning
- **Bounded Capability**: Accept reduced capability as tradeoff for safety
- **Tool Philosophy**: Build tools that assist humans rather than autonomous agents
- **Explicit Uncertainty**: Represent what system doesn't know

## Training Alternatives

1. **Imitation Learning**: Learn from expert demonstrations (behavioral cloning)
2. **Constraint Satisfaction**: Explicitly represent and satisfy safety constraints
3. **Symbolic Reasoning**: Logic-based systems with explicit rules
4. **Hybrid**: Combine neural components with symbolic reasoning
5. **Interactive Learning**: Learn through dialogue, not optimization

## Strengths

- Avoids instrumental convergence from optimization
- Naturally bounded capabilities
- Less susceptible to reward hacking
- Clearer failure modes
- Explicit uncertainty representation

## Weaknesses

- Significant capability sacrifice
- Harder to achieve general competence
- Less research on alternatives to RLHF
- Scaling challenges
- May not work for complex tasks

## See Also

- [assumptions.md](assumptions.md)
- [invariants.md](invariants.md)
- [failure_modes.md](failure_modes.md)
- [mapping_to_primitives.md](mapping_to_primitives.md)
