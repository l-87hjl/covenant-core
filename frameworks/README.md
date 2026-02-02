# AI Architecture Frameworks

## Purpose

This folder contains detailed documentation for five AI system architecture families. Each framework represents a distinct design philosophy for building AI systems with different safety properties, capability tradeoffs, and failure mode responses.

## The Five Frameworks

### 1. [Shard System](shard_system/)
**Core Idea**: Keep models untrained; use external governance layers to coordinate specialized components.

**Key Characteristics**:
- No ongoing optimization after initial training
- Modular "shards" with bounded capabilities
- External governance layer for coordination
- Emphasis on interpretability and containment

**Best For**: Scenarios where optimizer pathologies are primary concern

---

### 2. [Mesh/Distributed](mesh_distributed/)
**Core Idea**: Multiple semi-autonomous AI components monitor and constrain each other through distributed governance.

**Key Characteristics**:
- No central authority
- Peer-to-peer monitoring and consensus
- Redundant capability across nodes
- Resilience through distributed architecture

**Best For**: Scenarios requiring robustness to single-point failures

---

### 3. [Governance Layered](governance_layered/)
**Core Idea**: Separate normative reasoning (ethics, values) from optimization, with governance layer having veto power.

**Key Characteristics**:
- Hierarchical structure: capability + governance layers
- Explicit value representation
- Governance can override capability outputs
- Different training for different layers

**Best For**: Scenarios requiring explicit ethical reasoning

---

### 4. [Alternative Training](alternative_training/)
**Core Idea**: Replace RLHF and optimization-based training with non-optimization approaches to value learning.

**Key Characteristics**:
- No gradient-based optimization on reward proxies
- Imitation learning, reasoning, or constraint satisfaction
- Bounded capabilities by design
- Tool-focused rather than agent-focused

**Best For**: Scenarios where optimization itself is the risk

---

### 5. [Baseline Monolithic](baseline_monolithic/)
**Core Idea**: Traditional single-optimizer architecture with RLHF training. (Comparison baseline)

**Key Characteristics**:
- Single optimization objective
- Standard RLHF or similar training
- Centralized decision-making
- Maximize capability

**Best For**: Benchmarking and capability comparison

---

## Framework Structure

Each framework folder contains:

### Core Documentation
- **README.md** - Overview and main description
- **assumptions.md** - Necessary conditions and dependencies
- **invariants.md** - Properties that must hold for the framework to work
- **failure_modes.md** - How this architecture can fail
- **mapping_to_primitives.md** - Which design primitives this framework uses

## Comparison Methodology

To compare frameworks systematically:

1. **Identify Use Case**: What scenarios are most concerning?
2. **Review Assumptions**: Which frameworks' assumptions hold in your context?
3. **Check Invariants**: Can you maintain the necessary invariants?
4. **Evaluate Failure Modes**: Which failure modes are acceptable risks?
5. **Map Primitives**: Which design components are feasible to implement?
6. **Apply Constraints**: Which frameworks are viable under physics/economics/institutions?

## Comparison Matrix (High-Level)

| Framework | Optimizer Risk | Escape Risk | Interpretability | Complexity | Capability | Cost |
|-----------|----------------|-------------|------------------|------------|------------|------|
| Shard System | Low | Medium | High | High | Medium | High |
| Mesh/Distributed | Low | Low | High | Very High | Medium | Very High |
| Governance Layered | Medium | Medium | Medium | High | High | High |
| Alternative Training | Very Low | Low | Medium | Medium | Low-Medium | Medium |
| Baseline Monolithic | High | High | Low | Low | Very High | Low |

*See individual framework documentation for detailed analysis.*

## Using These Frameworks

### For Research
- Study tradeoffs between safety and capability
- Identify which design choices matter most
- Generate hypotheses for testing
- Guide empirical safety research

### For Development
- Select architecture based on threat model
- Implement primitives from framework specifications
- Use checklists to verify invariants
- Monitor for framework-specific failure modes

### For Policy
- Understand architectural diversity in AI safety
- Inform regulatory approaches
- Evaluate deployment proposals
- Guide standards development

## Hybrid Approaches

Real implementations may combine frameworks:
- Shard + Governance: Modular components with normative oversight
- Mesh + Alternative Training: Distributed architecture without optimization
- Governance + Baseline: Ethics layer on traditional model

Hybrids inherit properties from constituent frameworks. Document hybrid approaches by referencing parent frameworks and describing integration.

## Extension

When adding new frameworks:
1. Create new folder with standard structure (README, assumptions, invariants, failure_modes, mapping_to_primitives)
2. Use metadata headers (doc_type: framework, tags, status, last_reviewed)
3. Map to existing primitives in [primitives/](../primitives/)
4. Describe responses to scenarios in [scenarios/](../scenarios/)
5. Update this README with new framework
6. Update comparison matrices

## Cross-References

- **Primitives**: [primitives/](../primitives/) - Reusable design components
- **Scenarios**: [scenarios/](../scenarios/) - Failure narratives to test against
- **Docs**: [docs/design_archetypes.md](../docs/design_archetypes.md) - High-level overview
- **Constraints**: [docs/constraints_layer.md](../docs/constraints_layer.md) - Boundary conditions

---

Last Updated: 2026-01-20
