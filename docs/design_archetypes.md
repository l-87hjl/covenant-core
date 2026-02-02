---
doc_type: reference
tags: [frameworks, architectures, patterns]
status: living
last_reviewed: 2026-01-20
---

# Design Archetypes

## Purpose

This document provides an overview of the major AI system architecture families analyzed in this project. Each archetype represents a distinct design philosophy with different assumptions, tradeoffs, and failure mode responses.

## The Five Archetypes

### 1. Shard System
**Core Idea**: Keep foundation models untrained; use external governance layers to coordinate specialized components.

**Key Characteristics**:
- Models remain frozen after initial training
- External orchestration layer makes decisions
- Specialized shards handle bounded tasks
- No single optimization objective
- Interpretability through modular boundaries

**Primary Primitives**:
- Shards (modular sub-agents)
- External governance
- Interpretability layers
- Containment mechanisms

**Strengths**:
- Avoids optimizer pathologies (no ongoing optimization)
- Modular boundaries aid detection
- Failures are localized to shards
- Easier to inspect and audit

**Weaknesses**:
- Higher coordination overhead
- May sacrifice capability for safety
- Complex governance layer required
- Scaling challenges with many shards

**See**: [frameworks/shard_system/](../frameworks/shard_system/)

---

### 2. Mesh/Distributed
**Core Idea**: Multiple semi-autonomous AI components monitor and constrain each other through distributed governance.

**Key Characteristics**:
- No central authority or optimizer
- Peer-to-peer monitoring
- Redundant capability across nodes
- Consensus mechanisms for decisions
- Mutual interpretability requirements

**Primary Primitives**:
- Distributed shards
- Mutual monitoring
- Interpretability (for peers)
- Red team (adversarial nodes)
- Consensus protocols

**Strengths**:
- Resilient to single-point failures
- Natural checks and balances
- Harder to coordinate deception
- Emergent robustness

**Weaknesses**:
- Communication overhead
- Coordination problems at scale
- May deadlock on novel situations
- Harder to upgrade uniformly

**See**: [frameworks/mesh_distributed/](../frameworks/mesh_distributed/)

---

### 3. Governance Layered
**Core Idea**: Separate normative reasoning (ethics, values) from optimization, with governance layer having veto power.

**Key Characteristics**:
- Capability layer optimizes for tasks
- Governance layer evaluates ethics/safety
- Hierarchical decision structure
- Governance can override capability
- Explicit value representation

**Primary Primitives**:
- Evaluator-generator separation
- Governance/normative layer
- Interpretability (for governance)
- Human feedback (to governance)

**Strengths**:
- Addresses value specification directly
- Can catch optimizer pathologies
- Governance layer can use different training
- Explicit ethical reasoning

**Weaknesses**:
- Governance layer becomes optimization target
- Coordination between layers complex
- Governance may be gamed or exploited
- Requires robust value specification

**See**: [frameworks/governance_layered/](../frameworks/governance_layered/)

---

### 4. Alternative Training
**Core Idea**: Replace RLHF and optimization-based training with non-optimization approaches to value learning.

**Key Characteristics**:
- Avoids gradient-based optimization on proxies
- May use imitation, reasoning, or constraint satisfaction
- Explicit uncertainty representation
- Bounded capability by design
- Focus on tools over agents

**Primary Primitives**:
- Non-RLHF training (imitation, reasoning)
- Human feedback (during development, not training)
- Interpretability (for understanding, not optimization)
- Containment (by limited capability)

**Strengths**:
- Avoids instrumental convergence from optimization
- Naturally bounded capabilities
- Less susceptible to reward hacking
- Clearer failure modes

**Weaknesses**:
- May sacrifice capability significantly
- Harder to achieve general competence
- Unclear how to scale to complex tasks
- Less research on alternatives

**See**: [frameworks/alternative_training/](../frameworks/alternative_training/)

---

### 5. Baseline Monolithic
**Core Idea**: Traditional single-optimizer architecture with RLHF training and unified decision-making. (Comparison baseline)

**Key Characteristics**:
- Single optimization objective
- RLHF or similar training
- Centralized decision-making
- Opaque internal states
- Maximize capability

**Primary Primitives**:
- Single optimizer
- RLHF training
- Minimal interpretability
- External containment only

**Strengths**:
- Simpler to implement
- Proven capability
- Lower coordination overhead
- Well-understood training

**Weaknesses**:
- Vulnerable to optimizer pathologies
- Instrumental convergence risks
- Poor interpretability
- Single point of failure
- Deception harder to detect

**See**: [frameworks/baseline_monolithic/](../frameworks/baseline_monolithic/)

---

## Comparative Matrix

| Archetype | Optimizer Risk | Rogue Risk | Silent Emergence | Complexity | Capability |
|-----------|----------------|------------|------------------|------------|------------|
| Shard System | Low | Medium | Low | High | Medium |
| Mesh/Distributed | Low | Low | Low | Very High | Medium |
| Governance Layered | Medium | Medium | Medium | High | High |
| Alternative Training | Very Low | Low | Low | Medium | Low |
| Baseline Monolithic | High | High | High | Low | Very High |

## Design Tensions

### Safety vs Capability
- Safer architectures often sacrifice raw capability
- Coordination overhead reduces efficiency
- Interpretability may limit representation power
- Tradeoff is context-dependent

### Simplicity vs Robustness
- Simpler systems easier to analyze but more vulnerable
- Complex systems more robust but harder to verify
- Emergent properties cut both ways

### Detection vs Prevention
- Some architectures prevent failures (no optimization)
- Others detect failures (interpretability, monitoring)
- Prevention may limit capability more than detection

### Modularity vs Integration
- Modular systems easier to inspect, harder to coordinate
- Integrated systems more capable, harder to interpret
- Boundary placement matters

## Hybrid Approaches

Real implementations may combine archetypes:
- **Shard + Governance**: Modular shards with normative oversight
- **Mesh + Alternative Training**: Distributed system without optimization
- **Governance + Baseline**: Ethics layer on top of traditional model

Hybrids inherit both benefits and costs of constituent approaches.

## Constraint Sensitivity

Different archetypes respond differently to constraints:

### Physics Constraints
- Mesh systems pay high communication overhead
- Shard systems pay coordination overhead
- Baseline systems most energy-efficient

### Economic Constraints
- Complex architectures cost more to develop and run
- Baseline systems cheaper but riskier
- Tradeoff depends on risk tolerance

### Institutional Constraints
- Governance layers easier to audit
- Distributed systems harder to regulate
- Alternative training may require new standards

## Selection Criteria

Choose archetype based on:
1. **Threat model**: Which scenarios are most concerning?
2. **Constraints**: What physics/economics/institutions apply?
3. **Capability needs**: How much performance can be sacrificed?
4. **Verification needs**: What detection guarantees are required?
5. **Context**: Deployment environment and risk tolerance

## Evolution Path

Archetypes may evolve:
- Start simple (baseline) for research
- Add safety layers as capabilities grow
- Transition to modular/distributed as risks increase
- Hybrid approaches as understanding improves

## Limitations

These archetypes are **idealized patterns**:
- Real systems will have hybrid characteristics
- Implementation details matter enormously
- New archetypes may emerge
- Constraints shift with technology

Use as **organizing framework**, not rigid categories.

---

## See Also

- [taxonomy_overview.md](taxonomy_overview.md) - How archetypes fit into framework
- [threat_narratives.md](threat_narratives.md) - Failure modes each addresses
- [constraints_layer.md](constraints_layer.md) - Boundary conditions
- [frameworks/](../frameworks/) - Detailed archetype documentation
