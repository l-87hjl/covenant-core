---
doc_type: framework
tags: [baseline_monolithic, primitives]
status: draft
last_reviewed: 2026-01-20
---

# Baseline Monolithic: Mapping to Primitives

## Core Primitives

### Used Minimally
- **RLHF Training**: Core training methodology (but this is what creates risks)
- **Containment**: External only (physical servers, access controls)
- **Human Feedback**: During training via RLHF (creates reward proxy problems)

### Used Externally
- **Red Team**: Adversarial testing before deployment
- **Human Oversight**: External monitoring, not architectural feature

### Not Used
- **Shards**: Monolithic by definition
- **Interpretability**: Minimal (opaque internals)
- **Evaluator-Generator Separation**: Single unified system
- **Alternative Training**: Explicitly uses RLHF/optimization
- **Distributed Governance**: Centralized by definition

## Anti-Pattern Recognition

This framework **does not incorporate** most safety primitives:
- No modular boundaries (shards)
- No separation of concerns (evaluator/generator)
- No interpretability by design
- No governance layers
- No alternative to optimization

This is **by design** - it represents the traditional approach that other frameworks try to improve upon by adding these primitives.

## Integration Pattern

```
Input → Single Monolithic Model → Output
        (RLHF-trained, opaque)
           ↓
   External Monitoring (if any)
```

## Comparison Table

| Primitive | Baseline Monolithic | Other Frameworks |
|-----------|---------------------|------------------|
| Shards | No | Shard, Mesh, (optional in others) |
| Interpretability | Minimal | High priority |
| Evaluator-Generator | No separation | Governance, optional in others |
| Alternative Training | No (uses RLHF) | Alternative Training framework |
| Distributed Governance | No | Mesh framework |
| Governance Layers | No | Governance Layered framework |

## Why So Few Primitives?

**Simplicity**: Fewer components means:
- Faster development
- Lower complexity
- Easier to achieve high capability
- Fewer integration challenges

**Tradeoff**: Simplicity comes at cost of safety properties that primitives provide.

## See Also

- [README.md](README.md)
- [../../primitives/](../../primitives/) - Primitives this framework doesn't use
- [../](../) - Comparison to frameworks that do use safety primitives
