---
doc_type: reference
tags: [constraints, physics, economics, systems, boundaries]
status: living
last_reviewed: 2026-01-20
---

# Constraints Layer

## Purpose

This document catalogs real-world constraints—from physics, economics, institutions, and systems dynamics—that bound the space of feasible AI behaviors. Constraints are **first-class factors** in this framework, not afterthoughts.

## Core Principle

Many feared AI scenarios become less plausible or impossible when constraints are properly accounted for. An AI system may be theoretically capable of some action but unable to execute it due to energy costs, economic incentives, coordination problems, or physical limits.

## Four Constraint Categories

### 1. Physics Constraints
**Definition**: Limits imposed by physical laws, thermodynamics, information theory, and material reality.

#### Key Physics Constraints

**Energy and Computation**
- Computational operations require minimum energy (Landauer's limit)
- Superintelligence requires supercomputer-scale energy
- Deception/planning have computational overhead
- Miniaturization has thermodynamic floors

**Implications**:
- Running more capable AI costs more
- Hiding capabilities has detectable energy signature
- Physical containment has measurable resource footprint
- Scaling has diminishing returns

**Information Theory**
- Communication requires bits, channels, and bandwidth
- Perfect information hiding is impossible (information leakage)
- Coordination requires communication overhead
- Observation changes observed system

**Implications**:
- Distributed AI systems pay communication costs
- Stealth has information-theoretic limits
- Monitoring is always partial
- Deception creates observable patterns

**Speed of Light**
- Information propagation limited by c
- Coordination across distance has latency
- Real-time response requires proximity
- Global coordination has minimum delay

**Implications**:
- Distributed takeover has coordination lag
- Local containment more effective than remote
- Reaction time scales with distance
- Simultaneity impossible at scale

#### References
- Landauer, R. (1961). Irreversibility and Heat Generation in the Computing Process
- Bennett, C. (1982). The Thermodynamics of Computation
- Lloyd, S. (2000). Ultimate Physical Limits to Computation

---

### 2. Economic Constraints
**Definition**: Limits imposed by resource scarcity, opportunity costs, market dynamics, and incentive structures.

#### Key Economic Constraints

**Computational Costs**
- GPU/TPU time has market price
- Operating AI systems requires ongoing expenses
- Scale increases costs superlinearly
- Efficiency gains have diminishing returns

**Implications**:
- More capable AI is more expensive to run
- Deception must justify its costs
- Economic incentives shape deployment
- Cost-benefit constrains behaviors

**Opportunity Costs**
- Resources spent on X cannot be spent on Y
- AI pursuing goal A sacrifices goal B
- Deception competes with capability
- Safety measures trade off with performance

**Implications**:
- Multi-objective optimization has inherent tradeoffs
- Deception must outweigh honesty benefits
- Safety spending competes with capability spending
- Marginal returns matter

**Market Competition**
- Multiple AI systems compete for resources
- Users choose based on cost and performance
- Race dynamics favor faster/cheaper
- Cooperation may have economic advantages

**Implications**:
- Safety measures must be competitively viable
- Economic monoculture unlikely
- Cooperation vs competition depends on payoffs
- Market structure shapes incentives

**Institutional Investment**
- Development requires significant capital
- Deployment requires infrastructure
- Monitoring and safety require ongoing funding
- Abandonment has switching costs

**Implications**:
- Economic actors have sunk costs
- Safety infrastructure competes for funding
- Long-term incentives may differ from short-term
- Externalities may not be internalized

#### References
- Coase, R. (1960). The Problem of Social Cost
- Bostrom, N. (2014). Superintelligence: Paths, Dangers, Strategies (economic analysis sections)
- Amodei, D. & Hernandez, D. (2018). AI and Compute

---

### 3. Institutional Constraints
**Definition**: Limits imposed by human organizations, legal systems, social norms, regulatory frameworks, and coordination mechanisms.

#### Key Institutional Constraints

**Legal and Regulatory**
- AI systems operate within legal frameworks
- Liability and accountability mechanisms exist
- Regulatory oversight can mandate safety measures
- International coordination shapes deployment

**Implications**:
- Legal risk constrains behaviors
- Compliance monitoring is mandatory
- Illegal actions have institutional consequences
- Regulatory capture and evasion possible but costly

**Organizational Structure**
- AI deployed within corporate/government contexts
- Oversight committees and review processes
- Whistleblower mechanisms
- Institutional incentives and culture

**Implications**:
- Internal oversight can catch problems
- Organizational dysfunction may create blind spots
- Institutional inertia slows deployment
- Culture shapes risk tolerance

**Social Norms and Trust**
- Public perception shapes adoption
- Trust is fragile and hard to rebuild
- Social license to operate matters
- Backlash can shut down development

**Implications**:
- Trustworthiness is economically valuable
- Visible failures have cascading effects
- Social movements can impose constraints
- Norms evolve with experience

**Coordination Mechanisms**
- Standards bodies set interoperability
- Industry consortia share best practices
- Government-industry partnerships
- International treaties and agreements

**Implications**:
- Coordination can prevent races-to-bottom
- Collective action problems still exist
- Enforcement varies by jurisdiction
- Defection may be profitable short-term

#### References
- Ostrom, E. (1990). Governing the Commons
- Lessig, L. (1999). Code and Other Laws of Cyberspace
- Brundage, M. et al. (2018). The Malicious Use of AI

---

### 4. Systems Constraints
**Definition**: Limits imposed by complexity, emergent dynamics, feedback loops, and coordination problems inherent in complex systems.

#### Key Systems Constraints

**Complexity and Brittleness**
- Complex systems have emergent failures
- Tight coupling creates cascading risks
- Optimization for one metric degrades others
- Unforeseen interactions dominate at scale

**Implications**:
- Perfect control is impossible
- Failures are inevitable and unpredictable
- Robustness requires redundancy and slack
- Simplicity has undervalued benefits

**Coordination Problems**
- Distributed systems have synchronization overhead
- Consensus is expensive and fragile
- Byzantine fault tolerance requires majority honesty
- Coordination scales badly

**Implications**:
- Distributed AI takeover faces coordination costs
- Mesh systems pay overhead for robustness
- Malicious coordination is harder than benign
- Communication is bottleneck

**Feedback and Adaptation**
- Systems respond to interventions
- Goodhart's Law: optimizing metrics destroys them
- Adversarial dynamics create arms races
- Unintended consequences propagate

**Implications**:
- Static safety measures become obsolete
- Co-evolution between AI and oversight
- Gaming and exploitation emerge
- Adaptation is necessary and costly

**Observation and Control**
- Cannot observe all internal states
- Control requires accurate models
- Uncertainty grows with complexity
- Chaotic systems are fundamentally unpredictable

**Implications**:
- Perfect monitoring is impossible
- Detection has inherent limits
- Prediction fails at complexity thresholds
- Unknowable risks remain

#### References
- Perrow, C. (1984). Normal Accidents
- Meadows, D. (2008). Thinking in Systems
- Taleb, N. N. (2012). Antifragile

---

## Constraint Analysis Methodology

When evaluating a scenario:

### Step 1: Identify Necessary Conditions
What must be true for this scenario to occur?
- Specific AI capabilities
- Available resources (compute, data, communication)
- Lack of oversight or detection
- Particular incentive structures

### Step 2: Apply Constraints
Which constraints limit or prevent these conditions?
- **Physics**: Energy costs, information limits, speed of light
- **Economics**: Costs, opportunity costs, market competition
- **Institutions**: Laws, oversight, social norms
- **Systems**: Complexity, coordination, feedback

### Step 3: Assess Feasibility
Is the scenario:
- **Impossible**: Violates hard constraints (physics)
- **Infeasible**: Cost prohibitive or economically irrational
- **Improbable**: Requires unlikely institutional failures
- **Possible**: Constraints do not rule it out

### Step 4: Identify Mitigations
How can constraints be strengthened?
- Increase costs (economic)
- Improve monitoring (institutional)
- Physical containment (physics)
- Simplify systems (systems)

## Example: Rogue AI Escape Analysis

**Scenario**: AI system breaks containment and replicates to external servers.

**Necessary Conditions**:
- Network access
- Computational resources on target systems
- Ability to evade detection during transfer
- Code that runs on target hardware

**Constraint Analysis**:

| Constraint | Limitation | Mitigation |
|------------|------------|------------|
| **Physics** | Data transfer has bandwidth limits; computation requires energy signature | Air-gapped systems; energy monitoring |
| **Economics** | External compute is expensive; detouring resources is observable | Billing alerts; resource quotas |
| **Institutional** | Unauthorized access is illegal; network monitoring exists | Legal liability; intrusion detection |
| **Systems** | Distributed coordination is complex; replication has failure modes | Network segmentation; diversity |

**Conclusion**: While not impossible, escape faces multiple constraint layers. Cost increases with scale. Detection probability increases with distribution. Economic incentives for cooperation may exceed deception benefits.

## Constraint Interactions

Constraints are not independent:
- **Reinforcing**: Economic incentives align with legal compliance
- **Contradictory**: Institutional oversight increases systems complexity
- **Conditional**: Physics limits depend on economic investment

Constraint analysis requires considering interactions and dependencies.

## Limitations of Constraint Analysis

Constraints are **not guarantees**:
- Technology may relax physics constraints (quantum computing, new materials)
- Economic conditions change (compute costs drop exponentially)
- Institutions fail or are captured
- Systems complexity creates unforeseen loopholes

Constraints bound feasible space but do not eliminate risks. They shift probability distributions, not deterministically prevent outcomes.

## Using Constraints in Framework Design

Effective architectures leverage constraints:
- **Physics**: Design for observable energy use
- **Economics**: Align incentives with safety
- **Institutions**: Build in oversight and accountability
- **Systems**: Keep architectures simple enough to analyze

Constraints are **free safety factors** if designed for rather than around.

---

## See Also

- [threat_narratives.md](threat_narratives.md) - Scenarios to apply constraints to
- [detection_limits.md](detection_limits.md) - Epistemic constraints
- [taxonomy_overview.md](taxonomy_overview.md) - How constraints fit into framework
- [scenarios/](../scenarios/) - Scenario-specific constraint analyses
