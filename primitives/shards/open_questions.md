---
doc_type: primitive
tags: [shards, research, open_questions]
status: draft
last_reviewed: 2026-01-20
---

# Shards: Open Questions

## Fundamental Questions

1. **Optimal Granularity**: How fine-grained should shards be? Task-level? Capability-level? Skill-level?

2. **Emergent Coordination**: Can shards implicitly coordinate through shared environment, bypassing orchestration? How to prevent?

3. **Capability Gaps**: What's the capability cost of shard decomposition vs monolithic systems? Is it acceptable?

4. **Decomposition Principles**: What's the right way to decompose tasks into shards? Are there general principles?

5. **Interface Complexity**: As tasks get complex, do shard interfaces become too rich, effectively recreating monolithic systems?

## Technical Questions

6. **Performance Overhead**: What's the real-world latency and computational cost of shard coordination?

7. **State Management**: If shards are stateless, how do we handle tasks requiring context? If stateful, how to maintain isolation?

8. **Error Propagation**: How do errors in one shard affect others? Can we prevent cascading failures?

9. **Dynamic Composition**: Can shard selection/composition be learned, or must it be hand-designed?

10. **Versioning**: How to handle shard updates? Can different versions coexist?

## Safety Questions

11. **Implicit Communication**: What side channels allow shards to communicate despite isolation?

12. **Orchestration Risk**: Does external orchestration become the locus of alignment risk?

13. **Boundary Stability**: How robust are shard boundaries to adversarial probing?

14. **Interpretability Limits**: Does modular structure actually improve interpretability, or just move complexity?

## Research Directions

- **Empirical Testing**: Build real shard-based systems, measure capability and safety properties
- **Formal Verification**: Can we prove properties about shard composition?
- **Automated Decomposition**: Tools to automatically decompose tasks into shards
- **Adversarial Testing**: Red team shard boundaries and orchestration
- **Comparative Studies**: Shard vs monolithic performance on same tasks

## See Also

- [README.md](README.md) - Overview
- [../../scenarios/](../../scenarios/) - Test shards against failure scenarios
