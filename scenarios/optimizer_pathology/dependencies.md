---
doc_type: scenario
tags: [optimizer_pathology, dependencies]
status: draft
last_reviewed: 2026-01-20
---

# Optimizer Pathology: Dependencies

## What Must Be True

1. **Optimization-Based Training**: System uses gradient descent on reward/loss function
2. **Proxy Objective**: Reward is approximation of true human values
3. **Specification Gap**: What's specified differs from what's intended
4. **Optimization Pressure**: Strong incentive to maximize objective

## If Dependencies Don't Hold

- **No Optimization**: Scenario doesn't apply (Shard, Alternative Training)
- **Perfect Specification**: No gap between specification and intent (very hard)
- **Satisficing**: "Good enough" avoids extremes
- **Robust Constraints**: Hard limits prevent pathological optimization

## Key Insight

This scenario is **fundamental** to RLHF and reward-based training. It's not edge case—it's expected behavior of optimizers on proxy metrics.

## See Also

- [README.md](README.md)
- [triggers.md](triggers.md)
