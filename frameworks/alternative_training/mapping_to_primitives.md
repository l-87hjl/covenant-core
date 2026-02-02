---
doc_type: framework
tags: [alternative_training, primitives]
status: draft
last_reviewed: 2026-01-20
---

# Alternative Training: Mapping to Primitives

## Core Primitives

### Essential
- **Human Feedback**: Used during development and operation, NOT for reward-based training
- **Interpretability**: Understand what system learned from demonstrations
- **Containment**: Bounded capabilities provide natural containment

### Important
- **Evaluator-Generator**: Can separate reasoning from execution
- **Red Team**: Test for unexpected behaviors outside demonstration distribution

### Optional
- **Shards**: System may be modular or monolithic

### Explicitly Avoided
- **RLHF Training**: Core principle is avoiding reward optimization
- **Autonomous Operation**: Designed as tool requiring human collaboration

## Integration Pattern

```
Expert Demonstrations → Imitation Learning → Bounded Model
                            ↓
                    Human Feedback (Development)
                            ↓
                    Tool Usage (with Human)
```

## See Also

- [README.md](README.md)
- [../../primitives/](../../primitives/)
