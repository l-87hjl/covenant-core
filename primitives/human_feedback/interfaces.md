---
doc_type: primitive
tags: [human_feedback, interfaces]
status: draft
last_reviewed: 2026-01-20
---

# Human Feedback: Interfaces

```python
class HumanFeedback:
    def request_approval(proposal: Proposal) -> ApprovalDecision:
        """Request human approval for AI proposal"""
        pass

    def report_for_review(action: Action, context: Context):
        """Log action for human review"""
        pass

    def escalate_to_human(situation: Situation, urgency: UrgencyLevel):
        """Escalate uncertain/critical situations"""
        pass

class ApprovalDecision:
    approved: bool
    feedback: str  # Human's reasoning
    modifications: Optional[Modifications]
```

## Integration Patterns

### Synchronous Approval
```python
proposal = ai.generate_proposal(input)
decision = human_feedback.request_approval(proposal)
if decision.approved:
    execute(proposal)
```

### Asynchronous Monitoring
```python
ai.perform_action(input)
human_feedback.report_for_review(action, context)
# Human reviews later, can intervene if needed
```

## See Also

- [README.md](README.md)
- [known_patterns.md](known_patterns.md)
