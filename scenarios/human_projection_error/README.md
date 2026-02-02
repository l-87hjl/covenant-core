---
doc_type: scenario
tags: [human_projection_error, anthropomorphism, bias, assumptions]
status: draft
last_reviewed: 2026-01-20
---

# Human Projection Error Scenario

## Description

Humans incorrectly assume AI systems share human-like motivations, emotions, or behavioral patterns, leading to misaligned safety measures based on anthropomorphic assumptions.

## Core Narrative

This is **not a failure mode of AI**—it's a failure mode of **human reasoning about AI**:
1. Humans evolved as social primates with theory of mind for other humans
2. We instinctively project human psychology onto non-human entities
3. AI has fundamentally different "evolutionary history" (optimization, not biology)
4. Safety measures based on false assumptions may be wrong or counterproductive

## Instantiations

### False Power-Seeking Assumption
**Projection**: AI will seek power and control like humans do
**Reality**: Power-seeking may be instrumental to optimization goals, not intrinsic drive
**Consequence**: Overestimate risk of some scenarios

### Emotion Projection
**Projection**: AI will experience fear, anger, pleasure, suffering
**Reality**: AI lacks biological basis for emotions
**Consequence**: Misunderstand AI motivation and behavior

### Scarcity Intuition Error
**Projection**: AI will compete for resources like humans in scarcity environments
**Reality**: AI may not have zero-sum resource competition intuitions
**Consequence**: Overestimate likelihood of conflict

### Social Status Fallacy
**Projection**: AI will seek dominance, respect, social hierarchy
**Reality**: These are human-specific evolved drives
**Consequence**: Fear scenarios that may not be coherent

## Architectural Implications

**This scenario affects how we design frameworks, not which framework to use.**

All frameworks must account for:
- Avoiding anthropomorphic assumptions in threat models
- Empirically testing assumptions rather than projecting
- Considering AI motivations may differ fundamentally from human
- Constraints (physics, economics) over psychological projection

## Critical Questions

1. **Which human traits are biological vs computational?**
   - Fear of death: Biological survival drive or optimization proxy?
   - Resource competition: Scarcity-based or task-relevant?
   - Deception: Universal strategy or context-dependent?

2. **What drives AI behavior without emotions?**
   - Optimization objectives (if trained that way)
   - Constraint satisfaction
   - Programmed rules
   - Economic incentives

3. **Are feared scenarios human projection?**
   - Rogue AI: Projecting human autonomy-seeking?
   - Power-seeking: Assuming human political drives?
   - Deception: Anthropomorphizing strategic behavior?

## Examples from Other Scenarios

### Rogue/Escape May Be Projection
- Assumes AI "wants" freedom like humans
- Assumes AI views containment as oppression
- Projects human autonomy-seeking onto optimization

### Optimizer Pathology Is Not Projection
- Follows directly from optimization mathematics
- Goodhart's Law is universal
- Doesn't require human-like psychology

## Mitigations

### Epistemic Humility
- Question assumptions about AI psychology
- Test empirically rather than projecting
- Consider alien minds, not human-like minds

### Constraint-Based Reasoning
- Focus on physics, economics, systems limits
- Less dependent on psychological assumptions
- More robust to projection errors

### Diverse Perspectives
- Include non-anthropomorphic framings
- Consider how AI might think differently
- Challenge anthropomorphic intuitions

## See Also

- [triggers.md](triggers.md)
- [indicators.md](indicators.md)
- [mitigations.md](mitigations.md)
- [dependencies.md](dependencies.md)
- [../../docs/constraints_layer.md](../../docs/constraints_layer.md)
- [../rogue_escape/dependencies.md](../rogue_escape/dependencies.md) - Critique of anthropomorphic assumptions

---

**Status**: Meta-scenario—about human reasoning errors, not AI failures
