---
doc_type: reference
tags: [taxonomy, conceptual_map, structure]
status: living
last_reviewed: 2026-01-20
---

# Taxonomy Overview

## Purpose

This document provides a high-level conceptual map of how the AI Emergence Under Constraint framework organizes knowledge. It explains the relationships between frameworks, primitives, scenarios, and constraints.

## Four-Layer Structure

The project organizes AI safety analysis into four interconnected layers:

### 1. Frameworks (Architectures)
**Location**: `frameworks/`
**Definition**: Complete, named approaches to AI system design

**Examples**:
- Shard System
- Mesh/Distributed
- Governance Layered
- Alternative Training
- Baseline Monolithic

**Properties**:
- Each framework is a coherent design philosophy
- Frameworks compose multiple primitives
- Frameworks make specific architectural tradeoffs
- Each framework has different responses to scenarios

### 2. Primitives (Design Components)
**Location**: `primitives/`
**Definition**: Reusable building blocks that appear across multiple frameworks

**Examples**:
- Shards (modular sub-agents)
- Evaluator-generator loops
- Interpretability layers
- Containment mechanisms
- Human feedback systems
- Red team adversarial testing

**Properties**:
- Primitives are modular and composable
- Same primitive may serve different purposes in different frameworks
- Primitives have defined interfaces and integration patterns
- Primitives are implementation-agnostic

### 3. Scenarios (Failure Narratives)
**Location**: `scenarios/`
**Definition**: Descriptions of potential failure modes or emergence conditions

**Examples**:
- Rogue/Escape (autonomy, deception, boundary violation)
- Optimizer Pathology (paperclip problems, goal misspecification)
- Silent Emergence (undetectable capability gains)
- Human Projection Error (anthropomorphic assumptions)

**Properties**:
- Scenarios describe what could go wrong
- Each scenario has triggers, indicators, and mitigations
- Scenarios test frameworks differentially
- Scenarios may be impossible under certain constraints

### 4. Constraints (Boundary Conditions)
**Location**: `docs/constraints_layer.md`
**Definition**: Real-world limits that shape feasible behaviors

**Categories**:
- Physics (energy, computation, thermodynamics)
- Economics (costs, incentives, opportunity costs)
- Institutions (laws, norms, coordination)
- Systems (complexity, feedback, emergence)

**Properties**:
- Constraints apply regardless of AI capability
- Constraints may make some scenarios infeasible
- Constraints vary by context and scale
- Constraints are empirically grounded

## Relationship Map

```
Frameworks
    ↓ (compose)
Primitives
    ↓ (implement)
Mitigations
    ↓ (respond to)
Scenarios
    ↑ (bounded by)
Constraints
```

### How Components Interact

1. **Frameworks → Primitives**
   - Each framework selects and composes specific primitives
   - Example: Shard System heavily uses shards + external governance
   - Example: Mesh/Distributed uses distributed monitoring + interpretability

2. **Primitives → Scenarios**
   - Primitives provide mitigations for specific scenarios
   - Example: Evaluator-generator loops help prevent optimizer pathology
   - Example: Containment mechanisms address rogue/escape risks

3. **Scenarios → Constraints**
   - Constraints determine which scenarios are physically possible
   - Example: Deception requires certain computational overhead (physics constraint)
   - Example: Coordination requires communication channels (systems constraint)

4. **Constraints → Frameworks**
   - Constraints favor certain architectural approaches
   - Example: Energy limits favor modular (shard) over monolithic
   - Example: Economic costs favor interpretable over opaque systems

## Comparison Methodology

To compare two frameworks:

1. **Identify primitives**: Which design components does each use?
2. **Map to scenarios**: How does each respond to failure narratives?
3. **Apply constraints**: Which scenarios are feasible under real-world limits?
4. **Evaluate tradeoffs**: What does each framework sacrifice for its benefits?

## Example: Shard System vs Baseline Monolithic

| Dimension | Shard System | Baseline Monolithic |
|-----------|--------------|---------------------|
| **Primitives** | Shards, external governance, interpretability | Single optimizer, RLHF, minimal interpretability |
| **Optimizer Pathology** | Reduced (no single optimizer) | High risk (optimization pressure) |
| **Rogue/Escape** | Harder (modular boundaries) | Easier (unified agency) |
| **Silent Emergence** | More detectable (modular monitoring) | Less detectable (opaque internals) |
| **Physics Constraints** | Higher energy (coordination overhead) | Lower energy (unified process) |
| **Economic Constraints** | Higher cost (complexity) | Lower cost (simplicity) |

## Using This Taxonomy

### For New Frameworks
When adding a framework:
1. Document which primitives it uses
2. Describe how it responds to each scenario
3. Identify which constraints it assumes or violates
4. Compare explicitly to existing frameworks

### For New Primitives
When adding a primitive:
1. Define clear interface and purpose
2. Show which frameworks could incorporate it
3. Identify which scenarios it addresses
4. Document integration patterns

### For New Scenarios
When adding a scenario:
1. Specify triggers and indicators
2. Map architectural responses (all frameworks)
3. Apply constraint analysis (which are feasible)
4. Identify relevant primitives

### For New Constraints
When adding a constraint:
1. Ground in physics, economics, institutions, or systems
2. Identify which scenarios it rules out
3. Determine which frameworks it favors
4. Document empirical evidence

## Conceptual Boundaries

### What This Taxonomy Does
- Organizes existing ideas systematically
- Enables structured comparison
- Reduces ambiguity in safety discussions
- Identifies gaps and blind spots

### What This Taxonomy Does Not Do
- Predict future AI behavior with certainty
- Advocate for specific architectures
- Simulate complex geopolitical dynamics
- Resolve fundamental unknowables

## Evolution

This taxonomy is **living documentation**. As new frameworks, primitives, scenarios, or constraints are identified:
- Update this overview
- Add cross-references
- Revise comparison matrices
- Document rationale for changes

---

## See Also

- [glossary.md](glossary.md) - Definitions of terms used here
- [design_archetypes.md](design_archetypes.md) - Detailed framework patterns
- [threat_narratives.md](threat_narratives.md) - Detailed scenario catalog
- [constraints_layer.md](constraints_layer.md) - Constraint categories and evidence
