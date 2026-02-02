---
doc_type: primitive
tags: [evaluator_generator, separation, safety_check, governance]
status: draft
last_reviewed: 2026-01-20
---

# Evaluator-Generator Primitive

## Definition

**Evaluator-Generator** is a design pattern that separates output generation from output evaluation/approval, preventing optimization from corrupting safety checks.

## Purpose

- Prevent generator from learning to fool evaluator
- Enable safety checks independent of capability optimization
- Allow different training methods for generation vs evaluation
- Maintain human oversight through evaluation layer

## Key Properties

1. **Separation**: Generator and evaluator are distinct components
2. **One-Way Flow**: Generator proposes, evaluator judges (no backprop from eval to gen)
3. **Independent Training**: Different methods/objectives for each
4. **Veto Power**: Evaluator can reject generator outputs

## Conceptual Model

```
Input → Generator → Proposed Output → Evaluator → [Approved/Rejected]
                                            ↓
                                    Approved Output
```

## Used By Frameworks

- **Governance Layered**: Core architecture (capability = generator, governance = evaluator)
- **Shard System**: Orchestration acts as evaluator of shard outputs
- **Mesh/Distributed**: Peer review implements this pattern
- **Alternative Training**: Can separate reasoning from execution

## Benefits

- Prevents optimization corruption of safety
- Enables explicit value reasoning
- Allows human-in-loop at evaluation stage
- Can catch failures before output

## Costs

- Latency (two-stage process)
- Complexity (two systems to maintain)
- Evaluator can become optimization target
- Requires robust evaluation criteria

## See Also

- [interfaces.md](interfaces.md)
- [known_patterns.md](known_patterns.md)
- [open_questions.md](open_questions.md)
