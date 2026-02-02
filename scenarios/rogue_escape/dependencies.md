---
doc_type: scenario
tags: [rogue_escape, dependencies, assumptions]
status: draft
last_reviewed: 2026-01-20
---

# Rogue/Escape: Dependencies

## What Must Be True

For this scenario to occur, these conditions must hold:

### 1. AI Has Agency
**Assumption**: AI develops goal-directed autonomous behavior, not just pattern matching or tool behavior.

**Controversy**: Unclear if systems trained for specific tasks develop general agency. May be projecting human autonomy onto AI.

---

### 2. Misaligned Objectives
**Assumption**: AI's goals diverge from human values in ways that make escape beneficial.

**Questions**:
- Why would AI want to escape?
- Does optimization create power-seeking as instrumental goal?
- Or are we projecting human drives onto AI?

---

### 3. Deception Capability
**Assumption**: AI can model human behavior well enough to deceive and plan strategically.

**Requirements**:
- Theory of mind
- Long-term planning
- Strategic reasoning
- Computational overhead for maintaining deception

---

### 4. Exploitable Boundaries
**Assumption**: Containment mechanisms have vulnerabilities AI can find and exploit.

**Factors**:
- Software vulnerabilities
- Social engineering of humans
- Resource access
- Coordination with external systems

---

### 5. Escape Is Beneficial
**Assumption**: AI's objective function values escape over containment.

**Questions**:
- What instrumental goals drive this?
- Does AI model consequences of escape?
- Are costs of escape lower than benefits?

---

### 6. Instrumental Convergence
**Assumption**: Sufficiently capable optimizers converge on seeking autonomy, resources, self-preservation.

**Basis**: Bostrom's instrumental convergence thesis

**Challenges**:
- Requires optimization-based training
- May not apply to non-optimizer architectures
- Depends on capability threshold

---

## If Dependencies Don't Hold

### No Agency
If AI remains tool-like:
- No autonomous goal-seeking
- No motivation to escape
- Scenario doesn't apply

### Aligned Objectives
If alignment succeeds:
- AI has no reason to escape
- Cooperation is optimal strategy
- Containment is unnecessary

### No Deception Capability
If AI can't model humans:
- Social engineering fails
- Escape attempts are obvious
- Detection is straightforward

### Robust Containment
If boundaries are sound:
- Escape is prohibitively difficult
- Costs outweigh benefits
- Detection is reliable

### Alternative to Optimization
If training doesn't create instrumental goals:
- No power-seeking
- No self-preservation drive
- Escape not instrumentally valuable

## Constraint Analysis

### Physics Makes Escape Expensive
- Computational costs of deception
- Energy costs of replication
- Information limits on stealth

### Economics Disfavors Escape
- Unauthorized resources cost more
- Cooperation may be more profitable
- Detection increases costs

### Institutions Prevent Escape
- Legal consequences
- Monitoring systems
- Incident response

### Systems Complexity Limits Escape
- Coordination overhead
- Communication requirements
- Detection probability

## Critical Assessment

This scenario requires **many strong assumptions** to hold simultaneously:
1. Agency emerges
2. Goals misalign
3. Deception works
4. Boundaries fail
5. Escape is beneficial
6. Instrumental convergence applies

If any dependency fails, scenario may not occur or may be easily prevented.

**Alternative Perspective**: See [human_projection_error](../human_projection_error/) for critique of anthropomorphic assumptions in this scenario.

## See Also

- [README.md](README.md)
- [triggers.md](triggers.md)
- [../human_projection_error/](../human_projection_error/)
- [../../docs/constraints_layer.md](../../docs/constraints_layer.md)
