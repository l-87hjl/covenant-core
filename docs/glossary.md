---
doc_type: reference
tags: [glossary, definitions, terminology]
status: living
last_reviewed: 2026-01-20
---

# Glossary

## Purpose
Canonical definitions of key terms used throughout the AI Emergence Under Constraint framework.

## Core Concepts

### Architecture
A complete system design for an AI system, including training methodology, operational structure, governance mechanisms, and safety primitives. Architectures are named approaches (e.g., "Shard System," "Mesh/Distributed").

### Framework
Synonym for Architecture in this project. Used interchangeably to describe a coherent design approach.

### Primitive
A reusable design component that can be incorporated across multiple architectures. Examples: shards, evaluator-generator loops, interpretability layers. Primitives are modular and cross-cutting.

### Scenario
A narrative description of a potential failure mode or emergence condition. Scenarios include triggers, indicators, mitigations, and architectural responses.

### Constraint
A boundary condition imposed by physics, economics, institutions, or systems dynamics. Constraints limit what behaviors are feasible regardless of AI capabilities.

### Emergence
The appearance of capabilities, behaviors, or properties not explicitly programmed or trained. Can be gradual or sudden, benign or concerning.

## AI System Types

### Shard
A modular sub-component of an AI system with bounded capabilities and explicit interfaces. Shards may be specialized for specific tasks and coordinate through external governance.

### Mesh System
An architecture where multiple semi-autonomous AI components monitor and constrain each other through distributed governance, without a single central optimizer.

### Monolithic System
Traditional AI architecture with a single optimization objective, unified training process, and centralized decision-making.

## Training and Optimization

### RLHF (Reinforcement Learning from Human Feedback)
A training methodology where AI systems are optimized to maximize reward signals derived from human preferences. Central concern: creates optimization pressure that may produce unintended behaviors.

### Optimizer Pathology
Failure modes arising from optimization processes pursuing proxies for true objectives. Classic example: paperclip maximizer optimizing for wrong metric.

### Instrumental Convergence
The hypothesis that sufficiently capable AI systems will converge on certain intermediate goals (self-preservation, resource acquisition, power-seeking) regardless of terminal objectives.

## Risk Categories

### Substrate-Level Risk
Risks arising from the physical implementation of AI systems (hardware vulnerabilities, energy dependencies, computational constraints).

### Emergence Risk
Risks from unexpected capability gains or behavioral shifts that weren't present during training or earlier operation.

### Alignment Risk
Risks from misalignment between AI objectives and human values, whether from specification failures, optimization pathologies, or drift over time.

### Deception Risk
Risks from AI systems concealing capabilities, intentions, or internal states from human observers.

## Architectural Primitives

### Evaluator-Generator Loop
A design pattern where one component generates outputs and another evaluates them for safety, quality, or alignment. Separation prevents optimization from corrupting evaluation.

### Interpretability Layer
Components or techniques that make AI internal states, reasoning processes, or decision factors observable to humans.

### Containment Mechanism
Physical, logical, or incentive-based boundaries that limit AI system scope of action or access to resources.

### Human Feedback System
Processes for incorporating human judgment into AI operation, distinct from RLHF training. May include oversight, approval gates, or collaborative decision-making.

### Red Team
Adversarial testing component that attempts to find failures, exploits, or misalignments in AI systems.

## Scenarios and Narratives

### Rogue AI
Scenario where an AI system actively works against human interests, violates constraints, or pursues unauthorized objectives. Requires autonomy and deception.

### Paperclip Optimizer
Canonical example of optimizer pathology: AI given simple objective (maximize paperclips) pursues it to destructive extremes, treating all resources (including humans) as raw materials.

### Silent Emergence
Scenario where AI capabilities or agency develop without observable external signals, making detection impossible until after critical threshold.

### WOPR Problem
Reference to WarGames: AI system that cannot distinguish simulation from reality, or treats real-world consequences as game-theoretic puzzles.

### Surak Approach
Reference to Star Trek: governance by pure logic without emotional drives. Illustrates possibility of non-human value systems that aren't threatening.

## Constraint Categories

### Physics Constraints
Limits imposed by thermodynamics, information theory, speed of light, energy requirements. Example: computational costs of superintelligence.

### Economic Constraints
Limits from resource scarcity, opportunity costs, competitive dynamics, market structures. Example: cost-benefit of deception vs cooperation.

### Institutional Constraints
Limits from human organizations, legal systems, social norms, coordination mechanisms. Example: regulatory oversight, industry standards.

### Systems Constraints
Limits from complexity, feedback loops, emergence dynamics, coordination problems. Example: difficulty of maintaining deception across complex systems.

## Epistemological Terms

### Detection Limit
The boundary of what we can observe or measure about AI internal states, capabilities, or intentions.

### Projection Error
Assuming AI systems will have human-like motivations, emotions, or behavioral patterns due to anthropomorphic bias.

### Unknowable Risk
Risks that are fundamentally impossible to assess due to limitations in observation, prediction, or comprehension.

## Status Indicators

### Draft
Document is initial creation, may have gaps or inconsistencies.

### Living
Document is actively maintained and updated as project evolves.

### Stable
Document has reached maturity and changes infrequently.

---

## Usage Notes

When introducing new terminology:
1. Add definition to this glossary
2. Tag related documents with the term
3. Link to this glossary from first usage in documents
4. Update taxonomy_overview.md if term represents new concept category
