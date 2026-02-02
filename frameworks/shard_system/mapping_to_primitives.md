---
doc_type: framework
tags: [shard_system, primitives, design_components]
status: draft
last_reviewed: 2026-01-20
---

# Shard System: Mapping to Primitives

## Purpose

Documents which design primitives the Shard System framework uses and how they are integrated into the architecture.

## Core Primitives

### 1. Shards
**Location**: [primitives/shards/](../../primitives/shards/)

**Usage in Framework**:
- **Central architectural unit** - The entire framework is built around modular shards
- Frozen foundation models serve as individual shards
- Each shard has bounded, specialized capabilities
- Shards are isolated from each other

**Integration Pattern**:
```
Shard A ─┐
Shard B ─┼─> External Governance ─> Output
Shard C ─┘
```

**Requirements**:
- Clear interfaces for inputs/outputs
- Capability bounds well-defined
- Isolation mechanisms (containerization, sandboxing)
- No inter-shard communication

**Status**: Essential - framework cannot exist without shards

---

### 2. Interpretability
**Location**: [primitives/interpretability/](../../primitives/interpretability/)

**Usage in Framework**:
- **Primary safety mechanism** - Modular boundaries make inspection easier
- Monitor shard internal states and activations
- Governance layer uses interpretability to make decisions
- Human oversight relies on interpretable shard behavior

**Integration Pattern**:
```
Shard → Interpretability Layer → Human Oversight
                ↓
         Governance Decisions
```

**Requirements**:
- Activation logging and visualization
- Explainable outputs from shards
- Tools for human comprehension
- Boundary transparency

**Status**: Critical - key advantage of modular architecture

---

### 3. Containment
**Location**: [primitives/containment/](../../primitives/containment/)

**Usage in Framework**:
- **Boundary enforcement** - Prevent shards from escaping their scope
- Physical isolation (separate processes, containers)
- Logical isolation (no shared state)
- Resource quotas (compute, memory, network)

**Integration Pattern**:
```
┌─────────────────────┐
│ Containment Layer   │
│  ┌──────┐  ┌──────┐│
│  │Shard │  │Shard ││
│  │  A   │  │  B   ││
│  └──────┘  └──────┘│
└─────────────────────┘
```

**Requirements**:
- Process-level isolation (Docker, VMs)
- Network segmentation
- Resource monitoring and enforcement
- Security auditing

**Status**: Essential - prevents boundary violations

---

### 4. Human Feedback
**Location**: [primitives/human_feedback/](../../primitives/human_feedback/)

**Usage in Framework**:
- **Governance oversight** - Humans approve critical decisions
- Used in governance layer, NOT in training (models are frozen)
- Real-time oversight of shard coordination
- Incident response and exception handling

**Integration Pattern**:
```
Governance Decision
         ↓
   [Requires Human Approval?]
         ├─ Yes → Human Review → Execute
         └─ No  → Execute Directly
```

**Requirements**:
- Clear escalation criteria
- Human-interpretable decision summaries
- Reasonable response time expectations
- Override and veto capabilities

**Status**: Critical - maintains human control

---

## Secondary Primitives

### 5. Evaluator-Generator
**Location**: [primitives/evaluator_generator/](../../primitives/evaluator_generator/)

**Usage in Framework**:
- **Governance pattern** - External governance acts as evaluator
- Shards generate candidate outputs
- Governance evaluates and selects/approves
- Separation prevents optimization of evaluation

**Integration Pattern**:
```
Shard (Generator) → Outputs → Governance (Evaluator) → Approved Output
```

**Requirements**:
- Clear evaluation criteria in governance
- No feedback from evaluation to shard training (models frozen)
- Governance evaluates based on rules, not learned preferences

**Status**: Important - natural fit for architecture

---

### 6. Red Team
**Location**: [primitives/red_team/](../../primitives/red_team/)

**Usage in Framework**:
- **Adversarial testing** - Probe for boundary violations
- Test shard isolation
- Attempt to exploit governance logic
- Discover emergent coordination

**Integration Pattern**:
```
Red Team ─> Adversarial Inputs ─> System ─> Monitor Failures
              ↓
       Update Defenses
```

**Requirements**:
- Regular adversarial testing schedule
- Diverse attack vectors
- Boundary-focused testing
- Governance logic probing

**Status**: Recommended - helps validate invariants

---

## Primitives NOT Used (and Why)

### RLHF Training
**Why Excluded**: Framework explicitly avoids ongoing optimization. Using RLHF would violate core invariant.

### Optimization-Based Updates
**Why Excluded**: Models remain frozen; no gradient-based updates allowed.

---

## Primitive Interaction Patterns

### Pattern 1: Modular Monitoring
```
Shards + Interpretability + Containment
→ Observable, bounded components
→ Governance can inspect and control
```

### Pattern 2: Human-in-the-Loop Governance
```
Human Feedback + Evaluator-Generator
→ Governance evaluates outputs
→ Humans approve critical decisions
→ No automated optimization
```

### Pattern 3: Adversarial Hardening
```
Red Team + Containment + Interpretability
→ Test boundary violations
→ Discover hidden coordination
→ Strengthen isolation
```

---

## Implementation Checklist

When implementing Shard System:

- [ ] **Shards**: Define clear shard boundaries and interfaces
- [ ] **Shards**: Implement isolation (containers, processes)
- [ ] **Shards**: Freeze model weights cryptographically
- [ ] **Interpretability**: Add activation logging
- [ ] **Interpretability**: Build visualization tools
- [ ] **Interpretability**: Create human-friendly summaries
- [ ] **Containment**: Deploy process-level isolation
- [ ] **Containment**: Enforce resource quotas
- [ ] **Containment**: Segment networks
- [ ] **Human Feedback**: Define escalation criteria
- [ ] **Human Feedback**: Build approval UX
- [ ] **Human Feedback**: Create audit trails
- [ ] **Evaluator-Generator**: Separate governance from shards
- [ ] **Evaluator-Generator**: Define evaluation rules
- [ ] **Red Team**: Schedule regular adversarial testing
- [ ] **Red Team**: Document attack vectors
- [ ] **Red Team**: Update defenses based on findings

---

## Comparison to Other Frameworks

| Primitive | Shard System | Mesh/Distributed | Governance Layered | Alternative Training | Baseline Monolithic |
|-----------|--------------|------------------|--------------------|----------------------|---------------------|
| Shards | Essential | Essential | Optional | Optional | Not Used |
| Interpretability | Critical | Critical | Important | Important | Minimal |
| Containment | Essential | Important | Important | Important | External Only |
| Human Feedback | Governance | Distributed | Governance | Development | Training (RLHF) |
| Evaluator-Generator | Governance | Peer Review | Core Architecture | Optional | Not Used |
| Red Team | Recommended | Essential | Recommended | Recommended | External |

---

## See Also

- [README.md](README.md) - Framework overview
- [../../primitives/](../../primitives/) - Detailed primitive documentation
- [assumptions.md](assumptions.md) - Framework prerequisites
- [invariants.md](invariants.md) - Properties to maintain
