---
doc_type: framework
tags: [governance_layered, hierarchical, normative_reasoning, separation_of_concerns]
status: draft
last_reviewed: 2026-01-20
---

# Governance Layered Framework

## Overview

The Governance Layered architecture separates normative reasoning (ethics, values, safety) from capability optimization, with the governance layer having veto power over capability layer outputs.

**Core Principle**: Separate "can we do this?" (capability) from "should we do this?" (governance). Give governance override authority.

## Key Characteristics

- **Two-Layer Hierarchy**: Capability layer + Governance layer
- **Governance Veto**: Ethics layer can block capability outputs
- **Explicit Values**: Normative reasoning is explicit and auditable
- **Different Training**: Layers may use different training methodologies
- **Interpretable Governance**: Governance reasoning must be human-comprehensible

## Architecture Diagram

```
Input → Capability Layer → Proposed Output
             ↓
       Governance Layer (Ethics/Safety Check)
             ↓
        [Approved?]
       Yes ↓    No → Rejected
      Output      ↓
              Alternative
```

## Strengths

- Addresses value specification directly
- Can catch optimizer pathologies before output
- Governance layer can use safer training methods
- Explicit ethical reasoning

## Weaknesses

- Governance layer becomes optimization target
- Coordination complexity between layers
- Governance may be gamed or fooled
- Requires robust value specification

## See Also

- [assumptions.md](assumptions.md)
- [invariants.md](invariants.md)
- [failure_modes.md](failure_modes.md)
- [mapping_to_primitives.md](mapping_to_primitives.md)
