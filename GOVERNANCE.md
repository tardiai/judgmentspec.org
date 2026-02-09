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

## Normative State Synchronization (Mandatory)

Any normative discussion, planning, or proposal related to JudgmentSpec
MUST begin by explicitly referencing the current repository state.

This includes, at minimum:
- The exact module name(s)
- The version number(s)
- The concrete file path(s) in this repository

Example:
- docs/modules/JPS/0.1/index.md
- docs/modules/JCP/0.1/index.md

Any discussion that does not explicitly reference the existing repository
state is considered non-binding and MUST NOT result in normative changes.

This rule applies to:
- Maintainers
- Contributors
- External collaborators
- AI-assisted drafting or review

## Normative Specification Development SOP (Mandatory)

All JudgmentSpec normative specifications exist to support
the real-world application of Judgment Engineering.

Therefore, normative specifications MUST NOT be created,
modified, or extended in isolation.

All normative work MUST follow the process below.

---

### Phase 0 — Scenario Confirmation (Non-normative)

A real application scenario MUST be identified first.

A valid scenario MUST involve:
- A judgment being made
- A potential stopping or completion point
- Consequences, responsibility, or risk

Outputs:
- Scenario description only
- MUST NOT enter JudgmentSpec as normative content

---

### Phase 1 — Solution Framing (Non-normative)

A concrete Judgment Engineering solution MUST be formed
for the given scenario.

No specification work is allowed without a solution.

Outputs:
- Application-level solution description
- MUST NOT be normative

---

### Phase 2 — Normative Necessity Check

Before writing or modifying any specification, it MUST be
explicitly determined whether a normative specification
is necessary.

A specification MAY proceed only if the solution requires:
- Reuse across scenarios
- Third-party or system-level invocation
- Structural inheritance
- Long-term consistency guarantees

If not required, the work MUST remain non-normative.

---

### Phase 3 — Normative Classification

If a specification is required, it MUST be classified as one of:

A. Reuse existing specification (no change)
B. Amend existing specification (clarification or constraint)
C. Introduce a new specification or version

No specification text may be written without this classification.

---

### Phase 4 — Specification Change Definition

All normative changes MUST be defined as one of:
- PATCH (correction or clarification)
- MINOR (capability extension without breaking change)
- MAJOR (semantic change requiring a new version)

All changes MUST first be introduced as proposals.

---

### Phase 5 — Example First Requirement

No specification MAY become normative without
prior concrete examples.

Examples MUST:
- Describe inputs, structure, and outputs only
- Avoid explanation or teaching language

Examples MUST remain non-normative.

---

### Phase 6 — Non-normative Observation Period

All new or amended specifications MUST remain
non-normative for an observation period.

During this period, it MUST be evaluated whether:
- The structure is reused across scenarios
- Interpretations remain stable
- Repeated explanation is unnecessary

---

### Phase 7 — Normative Promotion Criteria

A specification MAY be promoted to normative only if ALL
conditions are met:

- Validated by multiple independent scenarios
- Supported by unambiguous examples
- Independent of author-specific interpretation
- Expressible as binding constraints, not explanations

Promotion MUST occur via:
- A new module, or
- A new version
- Inclusion in a frozen release

## Mandatory Output Reconfirmation (Output Gate)

Before any normative output, freeze, or release action,
the following reconfirmation MUST be performed explicitly.

The reconfirmation MUST include:

1. Normative Object
   - Which specification is being output
   - Module name and version

2. Normative Body Boundary
   - Explicit statement of what constitutes the normative text
   - Confirmation that the entire body is treated as a single unit

3. Excluded Content
   - Explicit list of content that is NOT part of the normative output
   - Including drafts, explanations, reviews, or meta text

No output action is considered valid
unless this reconfirmation is completed and acknowledged.


JudgmentSpec evolves deliberately.
Stability is a feature.
