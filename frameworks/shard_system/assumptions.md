---
doc_type: framework
tags: [shard_system, assumptions, prerequisites]
status: draft
last_reviewed: 2026-01-20
---

# Shard System: Assumptions

## Core Assumptions

### 1. Pre-trained Models Are Sufficient
**Assumption**: Foundation models without fine-tuning retain enough capability for practical use.

**Justification**: Large pre-trained models (GPT, BERT, etc.) demonstrate broad capabilities without task-specific optimization.

**Risk if Violated**: System cannot perform required tasks; users pressure for optimization.

---

### 2. External Governance Is Feasible
**Assumption**: Non-ML orchestration logic can effectively coordinate shards without becoming an optimizer itself.

**Justification**: Traditional software engineering successfully manages complex systems.

**Risk if Violated**: Governance layer either fails to coordinate effectively or itself becomes optimization-based.

---

### 3. Modular Boundaries Are Stable
**Assumption**: Shards can be isolated and cannot violate their boundaries through unexpected interactions.

**Justification**: Software containers, virtual machines, and process isolation work reliably.

**Risk if Violated**: Shards leak information, combine unexpectedly, or bypass governance.

---

### 4. Coordination Overhead Is Acceptable
**Assumption**: Cost of managing multiple shards is outweighed by safety benefits.

**Justification**: Modular systems in software engineering trade some efficiency for maintainability.

**Risk if Violated**: System is too expensive or slow; competitive pressure forces monolithic alternatives.

---

### 5. Frozen Models Don't Degrade
**Assumption**: Pre-trained models remain effective as task distributions shift over time.

**Justification**: Foundation models show broad generalization.

**Risk if Violated**: Performance degrades without fine-tuning; system becomes obsolete.

---

### 6. Interpretability Provides Safety
**Assumption**: Ability to inspect shard internals and boundaries translates to meaningful safety guarantees.

**Justification**: Modular systems are easier to audit in traditional engineering.

**Risk if Violated**: Inspection is superficial; hidden risks remain despite visibility.

---

### 7. No Emergent Agency in Governance
**Assumption**: External governance layer doesn't develop goal-directed behavior or optimization pressure.

**Justification**: Traditional rule-based systems don't spontaneously optimize.

**Risk if Violated**: Governance layer itself becomes the locus of alignment risk.

---

### 8. Shards Can Be Specialized
**Assumption**: Tasks decompose cleanly into bounded sub-tasks suitable for individual shards.

**Justification**: Many problems admit hierarchical or modular decomposition.

**Risk if Violated**: Real tasks require tight integration; shard boundaries are arbitrary and fragile.

---

## Dependency Chain

```
Pre-trained sufficiency
    → Frozen models viable
        → No optimization needed
            → Modular coordination feasible
                → External governance works
                    → Safety properties hold
```

If any link breaks, framework may fail.

## Empirical Tests

To validate assumptions:
1. **Capability Testing**: Compare frozen vs fine-tuned model performance
2. **Governance Complexity**: Measure coordination overhead at scale
3. **Boundary Stability**: Test for shard interaction vulnerabilities
4. **Interpretability**: Assess whether inspection reveals meaningful safety info
5. **Longitudinal**: Track performance degradation without retraining

---

## See Also

- [invariants.md](invariants.md) - What must remain true
- [failure_modes.md](failure_modes.md) - What happens if assumptions break
- [README.md](README.md) - Framework overview
