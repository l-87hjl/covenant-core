---
doc_type: primitive
tags: [evaluator_generator, research, open_questions]
status: draft
last_reviewed: 2026-01-20
---

# Evaluator-Generator: Open Questions

## Key Questions

1. **Evaluator Robustness**: Can generator learn to fool evaluator despite separation?

2. **Evaluation Criteria**: How to specify robust evaluation criteria that don't Goodhart?

3. **Scalable Oversight**: Can evaluator scale to judge superhuman generator outputs?

4. **Feedback Leakage**: Does knowing why outputs were rejected leak gradient signal to generator?

5. **Evaluator Training**: What's the best way to train evaluators? Human feedback? Rules? Debate?

6. **Performance Cost**: What's the latency/compute overhead of two-stage processing?

7. **Recursive Application**: Can evaluator-generator pattern apply recursively (evaluate the evaluator)?

8. **Failure Modes**: What happens when evaluator is uncertain? Conservative (reject) or permissive (approve)?

## See Also

- [README.md](README.md)
- [../../scenarios/](../../scenarios/)
