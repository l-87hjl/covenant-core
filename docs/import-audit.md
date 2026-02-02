# Import Audit — Legacy Covenant Code (Draft)

**Status:** Draft  
**Date:** February 1st, 2026

This document records a lightweight audit of code imported from the legacy Claude-based Covenant repository. The goal is orientation, not refactoring.

---

## Core Governance Logic (Keep)

- Deterministic Governor routing logic
- Separation of Generator / Evaluator / Governor roles
- Fail-closed behavior on schema or invariant violation
- Versioned invariant enforcement

These elements represent the core of Covenant (Stone).

---

## Model-Specific Glue (Replaceable)

- Claude-specific API adapters
- Prompt templates tightly coupled to Claude behavior
- Example integrations targeting a single model vendor

These should be treated as adapters, not architectural commitments.

---

## Reusable Components (Candidate Primitives)

- Intent declaration structures
- Schema validation logic
- Deterministic routing patterns

These may be abstracted into conceptual primitives shared across Covenant repos.

---

## Experimental or Optional Elements

- Demo scripts
- One-off experiments
- Non-essential examples

These are useful for learning but not required for the core architecture.

---

## Notes

This audit is intentionally non-exhaustive and should be updated only if major refactoring occurs.
