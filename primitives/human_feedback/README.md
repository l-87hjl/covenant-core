---
doc_type: primitive
tags: [human_feedback, oversight, control, approval]
status: draft
last_reviewed: 2026-01-20
---

# Human Feedback Primitive

## Definition

**Human Feedback** encompasses processes for incorporating human judgment into AI operation, distinct from RLHF training which uses feedback as optimization signal.

## Purpose

- Maintain human control over critical decisions
- Incorporate human values and judgment
- Provide oversight and error correction
- Enable human-AI collaboration

## Types of Human Feedback

### Approval Gates
- Human approves/rejects AI proposals
- Used for high-stakes decisions
- Real-time intervention

### Oversight Monitoring
- Humans review AI actions
- Post-hoc evaluation
- Pattern detection

### Collaborative Operation
- AI assists human (tool mode)
- Human has final decision
- Continuous interaction

### Value Specification
- Humans provide examples/preferences during development
- Not used as training signal (contrast with RLHF)
- Explicit criteria definition

## Used By Frameworks

- **Shard System**: Governance layer incorporates human oversight
- **Governance Layered**: Humans oversee governance layer
- **Mesh/Distributed**: Distributed human oversight
- **Alternative Training**: Development guidance, operational collaboration
- **Baseline Monolithic**: RLHF training (problematic use)

## Benefits

- Direct human control
- Incorporates human judgment
- Catches failures
- Maintains accountability

## Costs

- Human time and attention
- Latency bottleneck
- Doesn't scale to full automation
- Alert fatigue
- Humans can make mistakes

## See Also

- [interfaces.md](interfaces.md)
- [known_patterns.md](known_patterns.md)
- [open_questions.md](open_questions.md)
