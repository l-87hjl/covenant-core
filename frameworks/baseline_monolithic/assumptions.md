---
doc_type: framework
tags: [baseline_monolithic, assumptions]
status: draft
last_reviewed: 2026-01-20
---

# Baseline Monolithic: Assumptions

## Core Assumptions

1. **RLHF Works**: Human feedback adequately captures desired behavior
2. **Alignment Generalizes**: Training alignment transfers to deployment scenarios
3. **Risks Are Manageable**: Optimizer pathologies can be caught and fixed
4. **Capability Justifies Risk**: Performance benefits outweigh safety concerns
5. **External Containment Suffices**: Physical and institutional controls provide adequate safety
6. **Deception Won't Emerge**: Models won't learn to deceive during training
7. **Scaling Is Safe**: Increasing capability doesn't introduce qualitatively new risks

## Reality Check

Many of these assumptions are **questionable**:
- RLHF creates optimization pressure on proxies (Goodhart's Law)
- Generalization to deployment is uncertain
- Deceptive alignment is theoretical possibility
- Scaling has produced unexpected emergent capabilities
- External containment may not hold against sufficiently capable systems

This framework exists as **comparison baseline**, not validated safe approach.

## See Also

- [README.md](README.md)
- [invariants.md](invariants.md)
