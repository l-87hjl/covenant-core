# Covenant (Stone)

**Experimental Prototype — Trained Model Governance**

---

## What This Repository Is

This repository contains an **experimental implementation of Covenant** designed to operate on **already-trained ("stone") AI models**.

Covenant (Stone) assumes:
- Base models are pretrained using existing methods (e.g. supervised learning, RLHF, or equivalents)
- Alignment is enforced **post-training** through governance, not weight updates
- Safety and legitimacy are maintained through **structural separation and deterministic enforcement**, not incentives or punishment

This repository represents **one interpretation** of Covenant, focused on practical, testable governance over deployed models.

---

## Core Idea

Covenant (Stone) treats alignment as a **relationship problem**, not a training problem.

Rather than modifying model weights, it introduces a governance wrapper that:
- Separates proposal, evaluation, and enforcement roles
- Enforces versioned invariants
- Fails closed on ambiguity or schema violations
- Prevents silent drift

This makes defection from alignment locally attractive but **globally self-defeating**, without rewards or punishment.

---

## What This Repo Is *Not*

This repository is **not**:
- A definition of Covenant as a whole
- A moral philosophy
- A training method
- A frozen-model or pre-training system

Other interpretations of Covenant exist and are explored elsewhere.

---

## Related Repositories

- **ai-emergence-under-constraint**  
  Conceptual spine: emergence definitions, primitives, scenarios, and comparisons

- **covenant-pure**  
  Experimental research on Covenant applied to **untrained or frozen ("ice") models**

---

## Status

This codebase is an **experimental prototype**. Architecture, interfaces, and assumptions may change.

Historical note: parts of this implementation originated from early Claude-based experiments and were later consolidated here under a stable `main` branch.
