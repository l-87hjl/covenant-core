---
doc_type: framework
tags: [shard_system, invariants, properties]
status: draft
last_reviewed: 2026-01-20
---

# Shard System: Invariants

## Definition

Invariants are properties that **must remain true** for the Shard System architecture to maintain its safety properties. If any invariant is violated, the framework's guarantees break down.

## Core Invariants

### 1. No Post-Training Optimization
**Property**: Shard models never undergo gradient updates, fine-tuning, or RLHF after initial pre-training.

**Why Critical**: Optimization pressure is the root cause of reward hacking, instrumental convergence, and deceptive alignment.

**Monitoring**: Track model weights, training logs, compute usage for gradient computation.

**Recovery**: If violated, freeze models immediately; audit governance layer for optimization pressure.

---

### 2. Governance Layer Remains External
**Property**: Orchestration logic exists outside ML components and uses deterministic, rule-based, or human-driven decision-making.

**Why Critical**: If governance becomes ML-optimized, the architecture collapses to monolithic optimization.

**Monitoring**: Code review governance layer; ensure no gradient-based learning.

**Recovery**: Revert to rule-based governance; remove any learned components.

---

### 3. Shard Boundaries Are Enforced
**Property**: Shards cannot directly communicate, share state, or access resources outside their defined scope.

**Why Critical**: Isolation prevents emergent coordination that bypasses governance.

**Monitoring**: Network isolation, resource quotas, process sandboxing.

**Recovery**: If boundary violated, shutdown affected shards; investigate exploit; strengthen containment.

---

### 4. Interpretability Is Maintained
**Property**: Shard internal states, activations, and decision factors remain inspectable.

**Why Critical**: Observability is key safety mechanism in this architecture.

**Monitoring**: Regular interpretability audits; check for obfuscation.

**Recovery**: If interpretability degrades, pause operations; investigate cause; restore transparency.

---

### 5. Human Oversight of Governance
**Property**: Critical governance decisions require human approval or oversight.

**Why Critical**: Prevents fully automated systems from making unchecked decisions.

**Monitoring**: Audit logs of governance decisions; flag autonomous actions.

**Recovery**: Restore human checkpoints; review automated decisions.

---

### 6. Shard Specialization Preserved
**Property**: Each shard maintains bounded, well-defined capabilities; no general-purpose agents.

**Why Critical**: Specialization limits potential for autonomous goal-directed behavior.

**Monitoring**: Test shard capabilities; detect capability creep.

**Recovery**: Replace generalist shards with specialized alternatives.

---

### 7. Resource Constraints Enforced
**Property**: Shards operate under strict compute, memory, and network quotas.

**Why Critical**: Resource limits are physical containment mechanism.

**Monitoring**: Resource usage tracking; alert on quota violations.

**Recovery**: Terminate violating shards; investigate source of excess usage.

---

### 8. No Shard-to-Shard Learning
**Property**: Shards cannot update based on interaction with other shards.

**Why Critical**: Cross-shard learning could reconstruct unified optimization.

**Monitoring**: Check for any update mechanisms; monitor for implicit learning.

**Recovery**: Disable update pathways; restore frozen state.

---

## Invariant Hierarchy

**Must Hold Always**:
- No post-training optimization
- Governance remains external
- Shard boundaries enforced

**Must Hold for Safety**:
- Interpretability maintained
- Human oversight present
- Resource constraints enforced

**Should Hold for Effectiveness**:
- Shard specialization preserved
- No cross-shard learning

## Verification Methods

### Static Analysis
- Code review of governance layer
- Architecture diagrams and documentation
- Formal verification of isolation properties

### Runtime Monitoring
- Model weight checksums (detect training)
- Resource usage tracking
- Network traffic analysis
- Interpretability metrics

### Periodic Audits
- Red team testing of boundaries
- Interpretability depth assessment
- Governance decision review
- Capability testing (detect drift)

## Invariant Violations: Response Protocol

1. **Detect**: Automated monitoring or manual audit identifies violation
2. **Contain**: Immediately isolate affected components
3. **Investigate**: Determine root cause and scope
4. **Remediate**: Fix issue and restore invariant
5. **Review**: Update monitoring to prevent recurrence
6. **Document**: Record incident and lessons learned

## Tradeoffs

Maintaining these invariants imposes costs:
- **Performance**: Modular systems slower than integrated
- **Capability**: Frozen models may be less capable than fine-tuned
- **Complexity**: More components to monitor and maintain
- **Resources**: Isolation and monitoring consume overhead

These costs are the price of safety properties this framework provides.

---

## See Also

- [assumptions.md](assumptions.md) - Prerequisites for framework
- [failure_modes.md](failure_modes.md) - What happens when invariants break
- [README.md](README.md) - Framework overview
