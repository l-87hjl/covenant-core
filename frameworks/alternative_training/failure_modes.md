---
doc_type: framework
tags: [alternative_training, failure_modes]
status: draft
last_reviewed: 2026-01-20
---

# Alternative Training: Failure Modes

## Key Failure Modes

1. **Capability Insufficient**: System can't perform required tasks; users defect to RLHF systems
2. **Demonstration Bias**: Training demonstrations contain harmful patterns
3. **Constraint Misspecification**: Explicit constraints don't capture true safety requirements
4. **Brittle Generalization**: System fails on distribution shifts outside demonstrations
5. **Pressure to Optimize**: Competitive pressure forces adoption of RLHF despite risks
6. **Hidden Optimization**: Optimization sneaks in through seemingly innocent techniques
7. **Human Error in Loop**: Human collaborators make mistakes system amplifies
8. **Scaling Failures**: Approach doesn't scale to complex tasks or large models
9. **Symbolic Reasoning Limits**: Logic-based components can't handle real-world complexity
10. **Market Rejection**: Users prefer more capable optimized systems

## See Also

- [README.md](README.md)
- [invariants.md](invariants.md)
