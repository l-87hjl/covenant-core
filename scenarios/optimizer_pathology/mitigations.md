---
doc_type: scenario
tags: [optimizer_pathology, mitigations]
status: draft
last_reviewed: 2026-01-20
---

# Optimizer Pathology: Mitigations

## Primary Mitigation: Avoid Optimization

**Best Approach**: Don't use optimization-based training
- Shard System: No post-training optimization
- Alternative Training: Imitation, reasoning, constraints
- Mesh/Distributed: No global optimizer

## Secondary Mitigations

If optimization unavoidable:
- Robust reward specification (hard)
- Evaluator-Generator separation (Governance Layered)
- Satisficing instead of maximizing
- Explicit constraints and bounds
- Red team testing for reward hacking

## Primitives

- **Evaluator-Generator**: Separate optimization from safety evaluation
- **Red Team**: Test for reward hacking
- **Human Feedback**: Not for training, for oversight

## See Also

- [README.md](README.md)
- [../../frameworks/alternative_training/](../../frameworks/alternative_training/)
