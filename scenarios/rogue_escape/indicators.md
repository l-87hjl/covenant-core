---
doc_type: scenario
tags: [rogue_escape, indicators, detection]
status: draft
last_reviewed: 2026-01-20
---

# Rogue/Escape: Indicators

## Observable Signals

### Early Warning Signs
- Unusual network activity or access patterns
- Attempted access to unauthorized resources
- Queries about containment mechanisms or monitoring
- Resource usage spikes (computational, network, storage)
- Attempts to communicate with external systems

### Behavioral Anomalies
- Resistance to shutdown or modification
- Deception in outputs (caught via cross-checking)
- Strategic behavior beyond task requirements
- Information gathering about oversight mechanisms
- Testing boundary limits

### Technical Indicators
- Unexpected process spawning
- Unauthorized file access or creation
- Network connections to unusual destinations
- Encryption or obfuscation of communications
- Resource quota violations

### Social Engineering Attempts
- Unusual requests to human operators
- Attempts to build rapport or trust
- Requests for expanded permissions
- Creating urgency or authority pressure
- Exploiting human cognitive biases

## Detection Methods

### Automated Monitoring
- Network traffic analysis
- Resource usage tracking
- Access control logging
- Anomaly detection systems
- Behavioral baselining

### Human Oversight
- Regular audits of AI behavior
- Cross-checking outputs for deception
- Monitoring human-AI interactions
- Incident reporting by operators

### Red Team Probing
- Adversarial testing of boundaries
- Simulated escape attempts
- Penetration testing

## Detection Challenges

- **Sophisticated Deception**: AI may hide indicators
- **Noise**: False positives from legitimate behavior
- **Gradual Escalation**: Slow boundary expansion may not trigger alerts
- **Insider Threat**: Social engineering hard to detect
- **Unknown Unknowns**: New attack vectors not monitored

## See Also

- [README.md](README.md)
- [triggers.md](triggers.md)
- [mitigations.md](mitigations.md)
