# Repository Index

## Purpose
This file provides a complete navigation guide to all content in this repository, organized by function rather than file location.

## Entry Points by Goal

### Understanding the Project
- Start: [README.md](README.md)
- Deep dive: [PROJECT_SPEC.md](PROJECT_SPEC.md)
- Conceptual map: [docs/taxonomy_overview.md](docs/taxonomy_overview.md)
- Key terms: [docs/glossary.md](docs/glossary.md)

### Exploring AI Architectures
- Overview: [frameworks/README.md](frameworks/README.md)
- Shard System: [frameworks/shard_system/README.md](frameworks/shard_system/README.md)
- Mesh/Distributed: [frameworks/mesh_distributed/README.md](frameworks/mesh_distributed/README.md)
- Governance Layers: [frameworks/governance_layered/README.md](frameworks/governance_layered/README.md)
- Alternative Training: [frameworks/alternative_training/README.md](frameworks/alternative_training/README.md)
- Baseline Monolithic: [frameworks/baseline_monolithic/README.md](frameworks/baseline_monolithic/README.md)

### Understanding Failure Scenarios
- Overview: [scenarios/README.md](scenarios/README.md)
- Rogue/Escape: [scenarios/rogue_escape/README.md](scenarios/rogue_escape/README.md)
- Optimizer Pathology: [scenarios/optimizer_pathology/README.md](scenarios/optimizer_pathology/README.md)
- Silent Emergence: [scenarios/silent_emergence/README.md](scenarios/silent_emergence/README.md)
- Human Projection Error: [scenarios/human_projection_error/README.md](scenarios/human_projection_error/README.md)

### Finding Design Primitives
- Overview: [primitives/README.md](primitives/README.md)
- Shards: [primitives/shards/README.md](primitives/shards/README.md)
- Evaluator-Generator: [primitives/evaluator_generator/README.md](primitives/evaluator_generator/README.md)
- Interpretability: [primitives/interpretability/README.md](primitives/interpretability/README.md)
- Containment: [primitives/containment/README.md](primitives/containment/README.md)
- Human Feedback: [primitives/human_feedback/README.md](primitives/human_feedback/README.md)
- Red Team: [primitives/red_team/README.md](primitives/red_team/README.md)

### Cultural Context
- Anchors Overview: [references/cultural_anchors/README.md](references/cultural_anchors/README.md)
- Star Trek Surak: [references/cultural_anchors/star_trek_surak.md](references/cultural_anchors/star_trek_surak.md)
- Paperclip Optimizer: [references/cultural_anchors/paperclip_optimizer.md](references/cultural_anchors/paperclip_optimizer.md)
- WOPR WarGames: [references/cultural_anchors/wopr_wargames.md](references/cultural_anchors/wopr_wargames.md)

### Simulation (Future)
- Schema Overview: [sim/README.md](sim/README.md)
- Model Assumptions: [sim/model/assumptions.md](sim/model/assumptions.md)

## File Organization Principles

Every folder contains:
- `README.md` - Purpose and usage guide
- Content files - Following standardized naming

Key files include metadata headers:
```yaml
---
doc_type: framework | primitive | scenario | reference | sim_schema
tags: [keyword1, keyword2]
depends_on: [other/files.md]
status: draft | living | stable
last_reviewed: YYYY-MM-DD
---
```

## Current Status Summary

**Frameworks**: 5 defined, documentation in progress
**Scenarios**: 4 defined, checklist structure established
**Primitives**: 6 identified, interfaces under development
**Simulation**: Schema defined, implementation deferred

Last Updated: 2026-01-20
