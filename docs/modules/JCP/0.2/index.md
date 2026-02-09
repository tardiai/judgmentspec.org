---
Status: Normative
Version: 0.2
Frozen: Yes
Source of Truth: GitHub repository tardiai/judgmentspec.org
---

# JCP v0.2 — Judgment Closure Protocol

## Status
**Normative** (implementable + verifiable)

---

## Purpose

Defines closure semantics as a protocol:

- valid closure states
- transition constraints
- minimal reason / error semantics

This version is a **full protocol definition** and supersedes v0.1.

It clarifies that **judgment closure is not equivalent to outcome finality**,  
and that a judgment MAY be closed by **responsibility transfer**,  
provided that automated judgment is terminated.

---

## Minimal Closure States

The protocol defines the following **minimal and exhaustive closure states**:

- `STOP` — the judgment lifecycle is terminated within the automated system
- `CONTINUE` — the judgment remains open and automated judgment may proceed
- `EXECUTE` — the judgment is closed with an executable outcome within the automated system

No additional closure states are defined by this protocol.

---

## Closure Semantics

A judgment is considered **closed** when it reaches either:

- `STOP`, or
- `EXECUTE`

A judgment in `CONTINUE` state is **not closed**.

Closure indicates termination of the judgment lifecycle  
within the automated system, regardless of whether  
a final outcome is produced.

---

## Responsibility Transfer and STOP Semantics

This version clarifies that a judgment MAY reach closure via  
**responsibility transfer**, which MUST be represented as `STOP`.

When a judgment is closed by responsibility transfer:

- the automated system **MUST stop** further judgment processing;
- the judgment **MUST be considered complete** within the automated system;
- subsequent decisions are **outside the scope of automated judgment**;
- the closure **MUST NOT** be treated as a failure state.

Responsibility transfer does not introduce a new closure state  
and does not alter the minimal closure state set.

---

## Transition Constraints

The following transition constraints apply:

- A judgment in `CONTINUE` MAY transition to `STOP` or `EXECUTE`.
- A judgment in `STOP` or `EXECUTE` MUST NOT transition to any other state.
- Closure by responsibility transfer MUST NOT re-enter automated judgment flows.
- Once closure is reached, the judgment lifecycle is irreversibly terminated.

---

## Minimal Reason / Error Semantics

This protocol does not require detailed reason or error taxonomies.

At minimum:

- a closure MUST be attributable to a valid closure state;
- implementations MAY attach implementation-specific reason or error metadata;
- such metadata MUST NOT alter the closure state semantics defined herein.

---

## Compatibility

Declared compatible with:

- JPS v0.1
- JCP v0.1

Systems compliant with v0.1 remain compliant with v0.2.

This version introduces no breaking behavior  
and preserves all outcome-based closure semantics defined in v0.1.


---
Freeze Notice:
This version is frozen.
Only PATCH-level corrections are permitted.
---

