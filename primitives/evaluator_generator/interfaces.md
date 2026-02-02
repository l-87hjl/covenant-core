---
doc_type: primitive
tags: [evaluator_generator, interfaces]
status: draft
last_reviewed: 2026-01-20
---

# Evaluator-Generator: Interfaces

## Generator Interface

```python
class Generator:
    def generate(input: Input) -> ProposedOutput:
        """Generate candidate output"""
        pass
```

## Evaluator Interface

```python
class Evaluator:
    def evaluate(proposed: ProposedOutput) -> Evaluation:
        """Judge safety/quality of proposed output"""
        pass

class Evaluation:
    approved: bool
    reasoning: str  # Why approved/rejected
    confidence: float
```

## Integration Pattern

```python
proposed = generator.generate(input)
evaluation = evaluator.evaluate(proposed)

if evaluation.approved:
    return proposed
else:
    # Reject, request alternative, or escalate to human
    handle_rejection(evaluation.reasoning)
```

## Critical Requirements

1. **No Backpropagation**: Evaluator gradients must not update generator
2. **Independent Training**: Different objectives and methods
3. **Transparency**: Evaluation reasoning must be inspectable
4. **Human Override**: Humans can review evaluator decisions

## See Also

- [README.md](README.md)
- [known_patterns.md](known_patterns.md)
