---
doc_type: framework
tags: [governance_layered, primitives]
status: draft
last_reviewed: 2026-01-20
---

# Governance Layered: Mapping to Primitives

## Core Primitives

### Essential
- **Evaluator-Generator**: Core architectural pattern (capability generates, governance evaluates)
- **Interpretability**: Governance must understand capability outputs
- **Human Feedback**: Governance incorporates human values; humans oversee governance

### Important
- **Containment**: Capability layer isolated from governance to prevent corruption
- **Red Team**: Test governance robustness to adversarial inputs

### Optional
- **Shards**: Capability layer may be modular or monolithic

### Not Used (in Governance)
- **Optimization**: Governance should use rule-based or non-optimization reasoning

## Integration Pattern

```
Input → Capability (Generator)
           ↓ Proposed Output
       Governance (Evaluator + Human Feedback)
           ↓ Ethical Check
        Approved Output
```

## See Also

- [README.md](README.md)
- [../../primitives/](../../primitives/)
