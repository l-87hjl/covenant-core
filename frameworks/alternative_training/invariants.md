---
doc_type: framework
tags: [alternative_training, invariants]
status: draft
last_reviewed: 2026-01-20
---

# Alternative Training: Invariants

## Core Invariants

1. **No Gradient Optimization on Rewards**: Never use RLHF or similar reward-based training
2. **Explicit Constraints**: Safety constraints are represented explicitly, not learned implicitly
3. **Bounded Scope**: System capabilities remain limited to demonstrated/programmed behaviors
4. **Human-in-Loop**: Significant human involvement in operation (tool, not agent)
5. **Uncertainty Representation**: System explicitly represents what it doesn't know
6. **Demonstration Quality**: Training demonstrations maintain safety properties
7. **No Autonomous Goal-Seeking**: System doesn't develop instrumental goals

## See Also

- [README.md](README.md)
- [failure_modes.md](failure_modes.md)
