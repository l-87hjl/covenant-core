---
doc_type: primitive
tags: [interpretability, interfaces]
status: draft
last_reviewed: 2026-01-20
---

# Interpretability: Interfaces

## Inspection API

```python
class InterpretableModel:
    def get_activations(layer: str) -> np.array:
        """Access internal activations"""
        pass

    def explain_prediction(input: Input, output: Output) -> Explanation:
        """Why this input produced this output"""
        pass

    def get_attention(input: Input) -> AttentionWeights:
        """What input parts were important"""
        pass

    def get_reasoning_trace() -> List[ReasoningStep]:
        """Step-by-step decision process"""
        pass
```

## Explanation Format

```python
class Explanation:
    decision: str
    reasoning: List[str]  # Human-readable steps
    influential_features: List[Tuple[str, float]]  # Feature, importance
    confidence: float
    alternatives_considered: List[str]
```

## See Also

- [README.md](README.md)
- [known_patterns.md](known_patterns.md)
