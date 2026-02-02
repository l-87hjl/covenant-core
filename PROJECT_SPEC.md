# Project Specification: AI Emergence Under Constraint

## Mission Statement

Create a reusable, systematic framework for comparing AI safety architectures against multiple emergence scenarios, grounded in real-world constraints (physics, economics, institutions) rather than speculative worst-case narratives.

## Core Hypothesis

Approximately 70% of current AI safety concerns stem from optimization-based training methods (like RLHF) rather than from AI systems themselves. Different architectural approaches may naturally avoid many feared failure modes while introducing different tradeoffs.

## Not Goals

- ❌ Predicting specific AI takeover timelines
- ❌ Advocating for a single "correct" architecture
- ❌ Building high-fidelity geopolitical simulations
- ❌ Claiming we can know what superintelligent AI will do

## Actual Goals

- ✅ Organizing existing architectural ideas systematically
- ✅ Creating checklists for comparing approaches
- ✅ Mapping which design primitives matter for which scenarios
- ✅ Identifying which constraints naturally limit behaviors
- ✅ Reducing ambiguity in AI safety discussions

## Key Distinctions

### Tool vs Emergent AI
The project recognizes a fundamental tension: if AI remains a "tool," many fears are overblown; if AI becomes "superintelligent," it requires agency and cannot remain merely instrumental. Current safety work often conflates these.

### Human vs AI Evolutionary Paths
Humans evolved from predators/prey with survival drives. AI systems may not share:
- Scarcity intuitions
- Power-seeking instincts
- Emotional escalation patterns
- Biological survival imperatives

### Constraint-Aware Ethics
Physics, economics, and systems constraints shape behavior even without explicit ethics. An AI system optimizing for energy efficiency or computational cost may naturally avoid many feared behaviors.

## Architecture Families (Current)

1. **Shard System** - Keep models untrained; external governance layers
2. **Mesh/Distributed** - Multiple semi-autonomous components with mutual monitoring
3. **Governance Layers** - Normative reasoning above optimization
4. **Alternative Training** - Non-RLHF approaches to value learning
5. **Baseline Monolithic** - Traditional single-optimizer (for comparison)

## Failure Scenarios (Current)

1. **Rogue/Escape** - Autonomy, boundary crossing, deception
2. **Optimizer Pathology** - Paperclip problems, goal misspecification
3. **Silent Emergence** - Consciousness/agency without reportability
4. **Human Projection Error** - Assuming human-like drives

## Design Primitives (Reusable Components)

- Shards (modular sub-agents)
- Evaluator-generator loops
- Interpretability layers
- Containment mechanisms
- Human feedback systems
- Red team/adversarial checking

## Workflow Philosophy

- **Folders-first**: Clean taxonomy prevents conceptual drift
- **Iterate by module**: Small, bounded additions after initial scaffold
- **Patch/diff default**: Never reprint entire frameworks
- **Token discipline**: Minimize AI assistant context bloat
- **Phone-friendly**: Optimized for GitHub web UI + Colab workflows

## Success Criteria

The project succeeds if it:
1. Reduces confusion in AI safety discussions through clear taxonomy
2. Enables systematic comparison of architectural approaches
3. Identifies which design choices matter most for which scenarios
4. Prevents impossible scenarios from sneaking into analyses
5. Provides reusable checklists for evaluating new proposals

## Current Status

**Phase**: Initial scaffold and documentation
**Next**: Populate individual framework descriptions, define comparison matrices

## Maintenance Notes

- This document should be updated as frameworks are added/refined
- Major architectural additions should trigger taxonomy review
- Scenario catalog should grow as new failure modes are identified
