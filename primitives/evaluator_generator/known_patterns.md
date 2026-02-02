---
doc_type: primitive
tags: [evaluator_generator, patterns]
status: draft
last_reviewed: 2026-01-20
---

# Evaluator-Generator: Known Patterns

## Pattern 1: Rule-Based Evaluator
- Generator: ML model
- Evaluator: Explicit rules (no ML)
- Pro: Evaluator can't be gamed by optimization
- Con: Rules may be incomplete

## Pattern 2: Constitutional AI
- Generator: Proposes output
- Evaluator: Checks against explicit principles/constitution
- Pro: Transparent evaluation criteria
- Con: Constitution may be misspecified

## Pattern 3: Human-in-Loop Evaluator
- Generator: AI proposes
- Evaluator: Human approves/rejects
- Pro: Direct human control
- Con: Doesn't scale; human bottleneck

## Pattern 4: Ensemble Evaluator
- Generator: Single model
- Evaluator: Multiple independent models vote
- Pro: Robust to individual evaluator failures
- Con: High computational cost

## Pattern 5: Debate/Adversarial
- Generator A: Proposes output
- Generator B: Argues against if flawed
- Evaluator (Human/AI): Judges debate
- Pro: Exposes flaws
- Con: Requires capable adversarial generator

## See Also

- [README.md](README.md)
- [open_questions.md](open_questions.md)
