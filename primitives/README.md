# Design Primitives

## Purpose

This folder catalogs reusable design components ("primitives") that can be incorporated across multiple AI architecture frameworks. Primitives are modular building blocks that address specific safety concerns or provide specific capabilities.

## The Six Primitives

### 1. [Shards](shards/)
**Definition**: Modular sub-components with bounded capabilities and explicit interfaces.

**Purpose**: Decompose monolithic systems into manageable, isolated units.

**Used By**: Shard System (essential), Mesh/Distributed (essential), others (optional)

---

### 2. [Evaluator-Generator](evaluator_generator/)
**Definition**: Separation of output generation from output evaluation/approval.

**Purpose**: Prevent optimization from corrupting safety checks.

**Used By**: Governance Layered (core), Shard System (governance pattern), Mesh/Distributed (peer review)

---

### 3. [Interpretability](interpretability/)
**Definition**: Mechanisms to make AI internal states, reasoning, and decisions observable.

**Purpose**: Enable human understanding and oversight of AI behavior.

**Used By**: Shard System (critical), Mesh/Distributed (mutual inspection), Governance Layered (important)

---

### 4. [Containment](containment/)
**Definition**: Physical, logical, and incentive-based boundaries limiting AI scope of action.

**Purpose**: Prevent unauthorized access to resources or boundary violations.

**Used By**: All frameworks (importance varies)

---

### 5. [Human Feedback](human_feedback/)
**Definition**: Processes for incorporating human judgment into AI operation.

**Purpose**: Maintain human control and value alignment.

**Used By**: All frameworks (different integration patterns)

---

### 6. [Red Team](red_team/)
**Definition**: Adversarial testing and monitoring for failures, exploits, and misalignments.

**Purpose**: Discover vulnerabilities before they're exploited.

**Used By**: All frameworks (recommended)

---

## Primitive Structure

Each primitive folder contains:

- **README.md** - Overview and definition
- **interfaces.md** - How other components interact with this primitive
- **known_patterns.md** - Common implementation patterns and examples
- **open_questions.md** - Unresolved issues and research directions

## Using Primitives

### Composition
Frameworks combine primitives to achieve safety properties:
- **Shard System**: Shards + Interpretability + Containment + External governance
- **Mesh/Distributed**: Shards + Mutual interpretability + Distributed consensus
- **Governance Layered**: Evaluator-Generator + Human feedback + Interpretability

### Selection Criteria
Choose primitives based on:
1. **Threat Model**: Which scenarios are most concerning?
2. **Framework**: Which architecture are you implementing?
3. **Constraints**: What are physics/economics/institutional limits?
4. **Integration**: How do primitives interact in your system?

### Implementation
For each primitive:
1. Review interface specification
2. Study known patterns
3. Adapt to your framework
4. Test integration with other primitives
5. Validate safety properties

## Primitive Interactions

Primitives are not independent—they interact:

**Reinforcing Interactions**:
- Shards + Interpretability: Modular boundaries aid inspection
- Containment + Red Team: Testing validates boundary strength
- Evaluator-Generator + Human Feedback: Governance with human oversight

**Tension Interactions**:
- Shards + Performance: Modularity adds overhead
- Interpretability + Capability: Transparency may limit representation power
- Human Feedback + Autonomy: Oversight reduces automation

## Comparison Matrix

| Primitive | Complexity | Cost | Safety Benefit | Capability Impact |
|-----------|------------|------|----------------|-------------------|
| Shards | High | Medium-High | High (modular containment) | Medium (overhead) |
| Evaluator-Generator | Medium | Medium | High (prevents corruption) | Low (separation cost) |
| Interpretability | High | High | High (enables oversight) | Medium (may limit models) |
| Containment | Medium | Low-Medium | Medium (boundaries) | Low (resource limits) |
| Human Feedback | Medium | High (human time) | High (human control) | Medium (latency) |
| Red Team | Medium | Medium | Medium (finds issues) | None (testing only) |

## Extension

When adding new primitives:
1. Create new folder with standard structure
2. Define clear interface specification
3. Document known implementation patterns
4. Identify which frameworks could use it
5. Analyze interactions with existing primitives
6. Update this README

## Cross-References

- **Frameworks**: [frameworks/](../frameworks/) - How primitives compose into architectures
- **Scenarios**: [scenarios/](../scenarios/) - Which primitives address which failure modes
- **Docs**: [docs/taxonomy_overview.md](../docs/taxonomy_overview.md) - Conceptual relationships

---

Last Updated: 2026-01-20
