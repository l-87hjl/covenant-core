---
doc_type: framework
tags: [baseline_monolithic, invariants]
status: draft
last_reviewed: 2026-01-20
---

# Baseline Monolithic: Invariants

## Core Invariants

1. **Single Optimization Target**: One unified objective function maintained
2. **Continuous Training**: Model updated via RLHF or similar methods
3. **Centralized Decision-Making**: No distributed governance or modularity
4. **Performance Priority**: Capability improvements prioritized over safety measures
5. **Minimal Human-in-Loop**: System operates largely autonomously
6. **External Oversight**: Safety relies on external monitoring, not architectural features

## Critical Note

These invariants are **descriptive** (what characterizes this architecture) not **prescriptive** (what should be maintained for safety). In fact:
- Single optimizer creates risks
- Continuous training enables reward hacking
- Lack of modularity reduces interpretability
- Performance priority may sacrifice safety
- Minimal human oversight reduces control

This framework's invariants represent the **status quo** being questioned, not validated safe design.

## See Also

- [README.md](README.md)
- [failure_modes.md](failure_modes.md)
