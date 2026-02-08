# JudgmentSpec Governance

This document defines how JudgmentSpec evolves.

---

## Authority

JudgmentSpec has a **maintainer-led governance model**.

- Maintainers have final authority over:
  - normative content
  - versioning decisions
  - compatibility guarantees

Public discussion is encouraged.
Final decisions are centralized.

---

## Scope Control

JudgmentSpec scope is frozen to the following domains:

1. Structure
2. Protocol
3. Routing & Composition

Proposals outside this scope will be rejected.

---

## Normative Changes

A change is considered **normative** if it:
- alters required fields or semantics
- changes protocol states or transitions
- affects compatibility or validation rules

Normative changes require:
- a documented proposal (Issue or RFC-style doc)
- explicit maintainer approval
- version impact declaration

---

## Versioning Policy

JudgmentSpec uses **module-level semantic versioning**.

- **MAJOR**: breaking change
- **MINOR**: backward-compatible extension
- **PATCH**: editorial or clarification only

Modules evolve independently.

---

## Spec Sets (Releases)

Stable compatibility is provided through **Spec Set releases**.

A Spec Set:
- pins specific module versions
- is immutable once published
- serves as a stable reference for implementers

---

## Immutability Rule

Once published:
- normative specifications MUST NOT be altered retroactively
- changes require a new version

This ensures long-term reference stability.

---

## Decision Principle

When ambiguity arises, decisions prioritize:
1. Implementability
2. Testability
3. Long-term stability

Elegance and completeness are secondary.

---

JudgmentSpec evolves deliberately.
Stability is a feature.
