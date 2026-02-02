# Simulation Model Assumptions

## Purpose

Document what the simulation model assumes, what it doesn't model, and the boundaries of its validity.

## Core Assumptions (When Implemented)

### 1. Discrete Time Steps
**Assumption**: World evolves in discrete steps, not continuous time
**Justification**: Simpler to implement and analyze
**Limitation**: May miss continuous dynamics

### 2. Constraint Enforcement
**Assumption**: Physics/economics constraints are hard limits
**Justification**: Focus analysis on feasible behaviors
**Limitation**: Real constraints may be softer or context-dependent

### 3. Framework as Parameters
**Assumption**: Architectures can be parameterized and compared
**Justification**: Enables systematic comparison
**Limitation**: Real implementations have nuances not captured

### 4. Scenario as Initial Conditions
**Assumption**: Failure modes can be specified as starting states
**Justification**: Makes scenarios testable
**Limitation**: Real failures may emerge unpredictably

### 5. Observable Metrics
**Assumption**: Key outcomes are observable and measurable
**Justification**: Need metrics for comparison
**Limitation**: Some important factors may be unobservable (see detection_limits)

## What We DON'T Model

- **Individual human psychology**: Too complex, use aggregate behavior
- **Geopolitical dynamics**: Not simulating nations
- **Detailed technical implementation**: Abstract architectural properties
- **Consciousness**: Fundamentally unknowable (see scenarios/silent_emergence)
- **True superintelligence**: Beyond our ability to model

## Validation Criteria

Simulation is valid if:
1. Outputs match theoretical predictions where those exist
2. Constraint violations are impossible
3. Results are robust to parameter variations within ranges
4. Failure modes appear under expected conditions

Simulation is INVALID for:
- Predicting specific future events
- Claiming certainty about unknowables
- Extrapolating beyond constraint regimes
- Making policy decisions without human judgment

---

**Status**: Specification for future implementation

Last Updated: 2026-01-20
