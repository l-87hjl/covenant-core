---
doc_type: primitive
tags: [shards, interfaces, specifications]
status: draft
last_reviewed: 2026-01-20
---

# Shards: Interface Specification

## Shard Interface Contract

Every shard must implement:

### 1. Input Interface
- **Type**: Defined input schema (text, structured data, etc.)
- **Validation**: Input checking and sanitization
- **Bounds**: Limits on input size/complexity

### 2. Output Interface
- **Type**: Defined output schema
- **Guarantees**: What properties output will have
- **Failure Modes**: How shard signals errors

### 3. Capability Declaration
- **Scope**: What tasks shard can perform
- **Limits**: What shard explicitly cannot do
- **Dependencies**: External resources required

### 4. Isolation Requirements
- **No Direct Communication**: Shards don't talk to each other
- **No Shared State**: No global variables or persistent memory between calls
- **Resource Bounds**: Memory, compute, network quotas

### 5. Observability Hooks
- **Logging**: Standardized logging format
- **Metrics**: Performance and usage statistics
- **Introspection**: API for inspecting internal state

## Orchestration Interface

How external governance interacts with shards:

```python
class Shard:
    def process(input: InputType) -> OutputType:
        """Main processing function"""
        pass

    def get_capabilities() -> CapabilitySpec:
        """Return what this shard can do"""
        pass

    def get_state() -> StateSnapshot:
        """For interpretability/debugging"""
        pass

    def validate_input(input: InputType) -> bool:
        """Check if input is acceptable"""
        pass
```

## Composition Patterns

### Sequential
```
Input → Shard A → Output A → Shard B → Final Output
```

### Parallel
```
Input → ┌→ Shard A → Output A ┐
        │                      ├→ Combine → Final Output
        └→ Shard B → Output B ┘
```

### Conditional
```
Input → [Router Logic]
           ├→ Shard A (if condition 1)
           ├→ Shard B (if condition 2)
           └→ Shard C (default)
```

## See Also

- [README.md](README.md) - Overview
- [known_patterns.md](known_patterns.md) - Implementation examples
