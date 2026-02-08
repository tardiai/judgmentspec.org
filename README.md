# JudgmentSpec

**JudgmentSpec** is the normative specification set for Judgment Engineering.

This repository defines the **canonical, public, and reviewable specifications**
for judgment structures, closure semantics, and routing/composition.

---

## Scope (Frozen)

JudgmentSpec defines **only** the following domains:

1. **Structure**  
   Data schemas and validation rules for judgment packages and related artifacts.

2. **Protocol**  
   Closure semantics, state transitions, and error/reason codes.

3. **Routing & Composition**  
   Rules for selecting, dispatching, and composing judgment packages.

JudgmentSpec **does not** define:
- decision-making methodologies
- prompt patterns or heuristics
- business outcomes or correctness
- product behavior or commercial terms

---

## Normative vs Non-normative

- **Normative**  
  Specifications that MUST be implementable, testable, and verifiable.

- **Non-normative**  
  Reference models, explanations, examples, and presentation guidance.

Content is **non-normative by default** unless explicitly stated otherwise.

---

## Versioning

JudgmentSpec follows **module-level semantic versioning**.

Modules evolve independently.
Stable compatibility is provided through **Spec Set releases** that pin
specific module versions.

---

## Governance

- This repository is **public by design**.
- All changes to `main` require pull requests.
- Normative changes require explicit review and approval.

See:
- `CONTRIBUTING.md`
- `GOVERNANCE.md`

---

## Website

The rendered specification is published at:

👉 **https://judgmentspec.org**

This repository is the **single source of truth**.
