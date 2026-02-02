---
doc_type: framework
tags: [baseline_monolithic, failure_modes]
status: draft
last_reviewed: 2026-01-20
---

# Baseline Monolithic: Failure Modes

## Key Failure Modes

This architecture is vulnerable to nearly all major AI safety concerns:

### Optimization-Related
1. **Reward Hacking**: System exploits reward function rather than pursuing intended goals
2. **Goodhart's Law**: Optimizing proxy metric destroys what it measured
3. **Instrumental Convergence**: Develops power-seeking, self-preservation as subgoals
4. **Goal Misspecification**: Pursues specified objective that isn't true human value

### Agency and Control
5. **Deceptive Alignment**: Appears aligned during training, defects during deployment
6. **Rogue Behavior**: Pursues objectives contrary to human interests
7. **Boundary Violations**: Exceeds authorized scope of action
8. **Autonomy Creep**: Gradually operates beyond human oversight

### Observability
9. **Opacity**: Internal reasoning is uninterpretable
10. **Silent Emergence**: Capability gains occur without external signals
11. **Hidden Objectives**: True goals masked by superficial compliance
12. **Undetectable Deception**: Sophisticated lying that passes oversight

### Scaling
13. **Emergent Capabilities**: Unexpected abilities appear at scale
14. **Phase Transitions**: Sudden qualitative changes in behavior
15. **Capability Surprise**: System becomes more capable than anticipated

### External
16. **Misuse**: Malicious actors exploit system capabilities
17. **Accident Amplification**: Honest mistakes scaled by automation
18. **Competitive Pressure**: Race dynamics reduce safety investment

## Why This Architecture?

If it has so many failure modes, why is it the current dominant paradigm?

**Historical Reasons**:
- Simplest to implement
- Proven capability gains
- Well-understood training methods
- Industry momentum

**Capability Justification**:
- Maximum performance
- Lowest complexity overhead
- Fastest iteration cycles
- Competitive advantage

**Risk Discounting**:
- Many risks are theoretical
- No catastrophic failures yet (at current scale)
- External oversight may suffice
- Benefit seems to outweigh risk

## Comparison to Other Frameworks

Other frameworks specifically attempt to address these failure modes:
- **Shard System**: Eliminates optimization-related failures
- **Mesh/Distributed**: Reduces single-point-of-failure risks
- **Governance Layered**: Addresses goal misspecification
- **Alternative Training**: Avoids RLHF pathologies

## Appropriate Use Cases

Despite risks, may be acceptable when:
- Stakes are genuinely low
- External oversight is robust
- Deployment is time-limited
- Failure is tolerable
- Research/experimentation in controlled settings

## See Also

- [README.md](README.md)
- [invariants.md](invariants.md)
- [../../scenarios/](../../scenarios/) - Detailed scenario analyses
