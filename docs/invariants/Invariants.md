# Invariant-Core - Invariants

---

## Purpose

This document defines the upstream monotonic parent shell for the entire invariant structure.

All downstream invariant catalogs must be contained by this shell:

* [Core Invariants](core/README.md)
* [Pressure Invariants](pressure/README.md)
* [Invalidity Invariants](invalidity/README.md)
* [Closure Invariants](closure/README.md)
* [Truth Invariants](truth/README.md)

A downstream invariant may refine, specialize, localize, or make operational a parent invariant. It must not weaken, bypass, contradict, or reverse the parent shell.

---

## Monotonic Containment Law

* **INVARIANT_DOWNSTREAM_REFINEMENT_IS_MONOTONIC**
  Every downstream invariant must preserve or strengthen the upstream invariant shell.

* **INVARIANT_NO_DOWNSTREAM_WEAKENING**
  No downstream invariant may relax a constraint required by an upstream invariant.

* **INVARIANT_NO_DOWNSTREAM_CONTRADICTION**
  No downstream invariant may contradict the parent shell or another valid downstream refinement.

* **INVARIANT_DOWNSTREAM_SCOPE_IS_CONTAINED**
  A downstream invariant may narrow scope, but it must remain inside the admissible space defined upstream.

---

## 1. Structure & State Space

* **INVARIANT_STRUCTURE_MUST_EXIST**
  A bounded structure must exist before states, constraints, pressure, invalidity, closure, or truth can be evaluated.

* **INVARIANT_STATE_SPACE_MUST_BE_EXPLICIT**
  The possible states under evaluation must be representable, distinguishable, and subject to constraint.

* **INVARIANT_STRUCTURE_MUST_BOUND_ADMISSIBILITY**
  The structure must define where admissibility is evaluated and where invalidity is excluded.

---

## 2. Constraint Authority

* **INVARIANT_CONSTRAINT_FIELD_MUST_GOVERN_ALL_STATES**
  Every relevant state, interpretation, transition, or configuration must be governed by an active constraint field.

* **INVARIANT_CONSTRAINTS_DEFINE_ADMISSIBILITY**
  Constraints define what can survive as valid, not merely what is preferred or asserted.

* **INVARIANT_AUTHORITY_CONVERGES_WITH_CONSTRAINT_DEPTH**
  As invariant depth increases, authority becomes less optional and more intrinsic to the constraint itself.

---

## 3. Boundary Enforcement

* **INVARIANT_BOUNDARIES_MUST_BE_ENFORCED**
  All state transitions across relevant boundaries must pass through enforcement.

* **INVARIANT_NO_BOUNDARY_BYPASS**
  No downstream process may allow states to bypass required boundary validation.

* **INVARIANT_SEALS_MUST_MATCH_PRESSURE_CLASS**
  Boundary seals must be strong enough to evaluate and regulate the pressure they encounter.

---

## 4. Pressure Governance

* **INVARIANT_PRESSURE_MUST_REMAIN_CONSTRAINT_RELATIVE**
  Pressure must always be defined as unresolved possibility under an active constraint field.

* **INVARIANT_PRESSURE_MUST_RESOLVE_OR_BE_ELIMINATED**
  Unresolved pressure must resolve into valid form or be eliminated as invalid.

* **INVARIANT_PRESSURE_LEAKAGE_MUST_NOT_BE_CONFUSED_WITH_RESOLUTION**
  Leaked pressure remains unresolved burden and must not be treated as closure, truth, or stability.

---

## 5. Invalidity Exclusion

* **INVARIANT_INVALIDITY_MUST_BE_REJECTED_WHEN_DETECTED**
  Detected invalidity must be rejected, eliminated, contained, or transformed into valid form.

* **INVARIANT_INVALIDITY_MUST_NOT_PROPAGATE_AS_VALID**
  Invalid states must not be allowed to persist or propagate as if they satisfied constraints.

* **INVARIANT_INVALIDITY_MUST_NOT_REENTER**
  Invalidity rejected at one point must not re-enter through recursion, leakage, interpretation, or alternate boundary paths.

---

## 6. Closure Requirement

* **INVARIANT_CLOSURE_REQUIRES_NO_INVALID_SURVIVAL_PATHS**
  Closure requires the absence of paths through which invalidity can persist, propagate, leak, bypass, or return.

* **INVARIANT_CLOSURE_REQUIRES_RESOLVED_PRESSURE**
  Closure cannot increase while unresolved pressure remains hidden, deferred, or leaked.

* **INVARIANT_FALSE_CLOSURE_IS_FORBIDDEN**
  Apparent consistency must not be accepted as closure when invalidity or unresolved pressure still survives.

---

## 7. Truth Formation

* **INVARIANT_TRUTH_REQUIRES_COMPLETE_ENFORCEMENT**
  Truth requires survival through complete constraint enforcement across all relevant layers.

* **INVARIANT_TRUTH_IS_SURVIVING_STRUCTURE**
  Truth is the structure that remains after invalid possibilities are eliminated and pressure resolves without leakage.

* **INVARIANT_TRUTH_CANNOT_CONTAIN_INVALIDITY**
  No true state may contain contradiction, bypass, leakage, invalid re-entry, or unresolved invariant violation.

---

## 8. Layer Monotonicity

* **INVARIANT_LAYER_ORDER_MUST_BE_PRESERVED**
  Higher-layer invariants may refine or organize lower-layer constraints, but they must not override them.

* **INVARIANT_LOWER_LAYER_VIOLATION_DEFEATS_HIGHER_ACCEPTANCE**
  A state accepted at a higher layer remains invalid if it violates a lower-layer invariant.

* **INVARIANT_CONSTRAINT_DEPTH_INCREASES_RIGIDITY**
  Deeper constraints become less negotiable and must monotonically restrict downstream admissibility.

---

## 9. Transformation & Recursion

* **INVARIANT_TRANSFORMATIONS_MUST_PRESERVE_INVARIANTS**
  Valid transformations must preserve all applicable invariants in the parent shell and downstream refinements.

* **INVARIANT_RECURSION_MUST_BE_SEALED**
  Recursive paths must enforce constraints before outputs can re-enter the system.

* **INVARIANT_RECURSION_MUST_NOT_ACCUMULATE_INVALIDITY**
  Recursive processes must not preserve, amplify, or hide invalid states or unresolved pressure.

---

## 10. Consistency & Composition

* **INVARIANT_GLOBAL_CONSISTENCY_IS_REQUIRED**
  Surviving states must be mutually consistent across the enforced structure.

* **INVARIANT_COMPOSITION_MUST_PRESERVE_CONTAINMENT**
  Components may compose only when their invariants remain compatible with the parent shell.

* **INVARIANT_NO_CROSS_DOMAIN_LEAKAGE**
  Transitions across domains, layers, or abstractions must not preserve invalidity or unresolved pressure.

---

## Downstream Containment Map

| Downstream Catalog | Parent Containment |
| ----- | ----- |
| [Core Invariants](core/README.md) | Refines the full shell into canonical structural requirements for existence, constraints, boundaries, pressure, closure, truth, stability, and recursion. |
| [Pressure Invariants](pressure/README.md) | Refines `INVARIANT_PRESSURE_MUST_REMAIN_CONSTRAINT_RELATIVE`, `INVARIANT_PRESSURE_MUST_RESOLVE_OR_BE_ELIMINATED`, and `INVARIANT_PRESSURE_LEAKAGE_MUST_NOT_BE_CONFUSED_WITH_RESOLUTION`. |
| [Invalidity Invariants](invalidity/README.md) | Refines `INVARIANT_INVALIDITY_MUST_BE_REJECTED_WHEN_DETECTED`, `INVARIANT_INVALIDITY_MUST_NOT_PROPAGATE_AS_VALID`, and `INVARIANT_INVALIDITY_MUST_NOT_REENTER`. |
| [Closure Invariants](closure/README.md) | Refines `INVARIANT_CLOSURE_REQUIRES_NO_INVALID_SURVIVAL_PATHS`, `INVARIANT_CLOSURE_REQUIRES_RESOLVED_PRESSURE`, and `INVARIANT_FALSE_CLOSURE_IS_FORBIDDEN`. |
| [Truth Invariants](truth/README.md) | Refines `INVARIANT_TRUTH_REQUIRES_COMPLETE_ENFORCEMENT`, `INVARIANT_TRUTH_IS_SURVIVING_STRUCTURE`, and `INVARIANT_TRUTH_CANNOT_CONTAIN_INVALIDITY`. |

---

## Downstream Validity Test

A downstream invariant is valid only if all of the following hold:

* it preserves the parent shell
* it does not weaken upstream constraint
* it does not introduce a bypass path
* it does not allow invalidity to survive
* it does not treat leakage as resolution
* it does not treat apparent consistency as closure
* it does not treat assertion as truth
* it remains compatible with lower-layer constraints

---

# Final Compression

> The invariant shell is the monotonic parent structure.
> Downstream invariants may refine it,
> specialize it,
> or make it operational,
> but they must never weaken it.
> All valid downstream invariants remain contained inside enforced structure,
> resolved pressure,
> eliminated invalidity,
> complete closure,
> and surviving truth.
