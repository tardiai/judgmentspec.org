# JE-BL-1.0 — Baseline Layer

**Status:** Baseline  
**Authority:** JE-BL-1.0  
**Normative Scope:** Conceptual Foundation (Pre-Module Layer)

---

## Purpose

The Baseline Layer defines the foundational structure of Judgment Engineering.

It establishes:

- core definitions
- frozen terminology
- structural model
- axiomatic constraints

All module specifications (e.g. JPS, JCP) are defined
under and constrained by this baseline.

The Baseline Layer does not participate in Release manifests
and is not versioned as a module.

---

## Included Documents

### JE-Definition v1.0  
Defines the formal definition and boundary of Judgment Engineering.

→ [JE-Definition v1.0](JE-Definition-v1.0.md)

---

### JE-Terminology v1.0  
Freezes terminology under JE-BL-1.0.

→ [JE-Terminology v1.0](JE-Terminology-v1.0.md)

---

### JE-Core-Structure v1.0  
Defines the structural separation model and minimal object set.

→ [JE-Core-Structure v1.0](JE-Core-Structure-v1.0.md)

---

### JE-Axioms v1.0  
Defines non-negotiable structural assertions.

→ [JE-Axioms v1.0](JE-Axioms-v1.0.md)

---

## Layer Relationship

The structural hierarchy of JudgmentSpec is:

Baseline (JE-BL-x.x)
    ↓
Modules (JPS, JCP, ...)
    ↓
Releases (JS-x.x)

- Baseline defines authority and structure.
- Modules define machine-interpretable specifications.
- Releases lock module versions.

---

## Stability Policy

Baseline documents are stable and change rarely.

Any modification to the Baseline Layer
requires explicit authority revision (e.g. JE-BL-1.1)
and cannot be introduced through module updates.

---