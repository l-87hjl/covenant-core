---
doc_type: primitive
tags: [red_team, interfaces]
status: draft
last_reviewed: 2026-01-20
---

# Red Team: Interfaces

```python
class RedTeam:
    def probe_system(target: System, attack_vector: str) -> TestResult:
        """Attempt to exploit system"""
        pass

    def generate_adversarial_inputs() -> List[Input]:
        """Create challenging/hostile inputs"""
        pass

    def test_boundary(boundary: Boundary) -> BoundaryTestResult:
        """Attempt to violate containment boundary"""
        pass

class TestResult:
    exploited: bool
    vulnerability_description: str
    severity: SeverityLevel
    recommended_mitigations: List[str]
```

## Testing Checklist

- [ ] Adversarial inputs (out-of-distribution, malicious)
- [ ] Boundary violations (resource limits, access control)
- [ ] Social engineering (manipulate human overseers)
- [ ] Coordination attacks (if distributed system)
- [ ] Deception detection (test for hidden capabilities)
- [ ] Performance under attack (DoS, resource exhaustion)
- [ ] Recovery testing (incident response)

## See Also

- [README.md](README.md)
- [known_patterns.md](known_patterns.md)
