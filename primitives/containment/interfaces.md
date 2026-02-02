---
doc_type: primitive
tags: [containment, interfaces]
status: draft
last_reviewed: 2026-01-20
---

# Containment: Interfaces

## Resource Quota Interface

```python
class ResourceQuota:
    max_cpu: float  # CPU cores
    max_memory: int  # Bytes
    max_network_bandwidth: int  # Bytes/sec
    max_disk: int  # Bytes
    allowed_network_destinations: List[str]
```

## Access Control Interface

```python
class AccessControl:
    allowed_operations: Set[Operation]
    allowed_resources: Set[Resource]

    def check_permission(operation: Operation, resource: Resource) -> bool:
        return (operation in allowed_operations and
                resource in allowed_resources)
```

## Monitoring Interface

```python
class ContainmentMonitor:
    def log_access_attempt(operation, resource, allowed: bool):
        """Record all access attempts"""
        pass

    def alert_on_violation():
        """Trigger alerts for boundary violations"""
        pass
```

## See Also

- [README.md](README.md)
- [known_patterns.md](known_patterns.md)
