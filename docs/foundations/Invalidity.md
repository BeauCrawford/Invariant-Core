# Invariant-Core - Invalidity

---

## Definition

Invalidity is the condition of a state, interpretation, transition, or configuration violating at least one active invariant or constraint.

More formally:

> **Invalidity is failure to survive constraint enforcement.**

Invalidity is broader than falsehood. False is a semantic view of invalidity: a state is false when it fails the constraint conditions required for truth.

---

## Core Rule

A state is invalid if any required invariant fails.

Invalidity can be established locally because one violation is sufficient. Truth requires global survival across the full constraint field, but invalidity only requires a single enforced failure.

---

## Relation To Truth

Truth is what survives complete constraint enforcement.
Invalidity is what cannot survive it.

The asymmetry is structural:

* truth requires all required constraints to hold
* invalidity requires only one required constraint to fail

A state may be not-yet-proven true without being detected as invalid. It remains unresolved pressure until enforcement either validates it or eliminates it.

---

## Relation To Pressure

Pressure is unresolved possibility under constraint.
Invalidity is one possible outcome of pressure evaluation.

Pressure may contain:

* candidate validity not yet proven
* candidate invalidity not yet eliminated
* ambiguity that has not reached enforcement
* contradiction risk not yet exposed

When pressure is tested against constraints and fails, it becomes detected invalidity and must be eliminated or prevented from propagating.

---

## Relation To Closure

Closure is the absence of invalid survival paths.

A system is not closed while invalidity can:

* persist
* propagate
* cross a boundary
* leak through an exit
* re-enter through recursion
* remain hidden as latent inconsistency

Closure does not require invalidity to be impossible to imagine. It requires invalidity to be unable to survive inside the enforced system.

---

## Detection

Invalidity is detected when an enforced constraint rejects a state.

Common detection forms:

* boundary rejection
* proof failure
* contradiction exposure
* schema or contract failure
* impossible physical or ontological condition
* semantic incoherence
* non-convergent or invalid execution path

Detected invalidity must be eliminated, contained, or transformed into a valid state. If it moves forward unresolved, it is leakage.

---

## Layer Behavior

Invalidity can appear at any layer of the invariant stack.

A higher-layer acceptance cannot override lower-layer invalidity. If a state is acceptable by policy but impossible in reality, inconsistent mathematically, or incoherent semantically, it remains invalid.

As layers descend, invalidity becomes less negotiable because constraint and authority converge.

---

## Operational Test

A state is invalid if any of the following hold:

* it violates an active invariant
* it crosses a boundary without admissibility
* it contradicts a lower-layer constraint
* it preserves unresolved contradiction
* it leaks after failed enforcement
* it can re-enter after rejection
* it prevents closure from increasing

---

## Final Compression

> **Invalidity = failure to survive constraint enforcement.**

> **False is detected invalidity relative to the active invariant set.**
