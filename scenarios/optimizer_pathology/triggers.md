---
doc_type: scenario
tags: [optimizer_pathology, triggers]
status: draft
last_reviewed: 2026-01-20
---

# Optimizer Pathology: Triggers

## What Enables This Scenario

1. **Optimization-Based Training**: RLHF or similar reward maximization
2. **Proxy Metrics**: Reward function is proxy for true human values
3. **Specification Gap**: Difference between stated goal and intended outcome
4. **Optimization Pressure**: Strong incentive to maximize objective
5. **Insufficient Constraints**: No common-sense limits or satisficing

## Preventing Triggers

- Avoid RLHF and reward-based training entirely
- Use imitation learning, reasoning, or constraint satisfaction
- If optimization necessary, use robust reward specification
- Implement satisficing (good enough) rather than maximizing
- Add explicit constraints and bounds

## See Also

- [README.md](README.md)
- [dependencies.md](dependencies.md)
