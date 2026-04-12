# Invariant-Core - Pressure Invariants

---

## 1. Existence & Constraint

* **PRESSURE_EXISTS_UNDER_CONSTRAINT**
  Pressure exists only where possibility and active constraints overlap without full resolution.

* **PRESSURE_REQUIRES_UNRESOLVED_POSSIBILITY**
  Pressure requires at least one unresolved state, interpretation, transition, or configuration.

* **PRESSURE_IS_CONSTRAINT_RELATIVE**
  Pressure is defined relative to the constraint field that determines admissibility.

---

## 2. State Burden

* **PRESSURE_IS_UNRESOLVED_ADMISSIBILITY_BURDEN**
  Pressure is the burden carried by possibilities not yet proven admissible or eliminated.

* **PRESSURE_CAN_CONTAIN_CANDIDATE_VALIDITY**
  Pressure may include states that could become valid after enforcement.

* **PRESSURE_CAN_CONTAIN_CANDIDATE_INVALIDITY**
  Pressure may include states that will be eliminated once constraints are enforced.

---

## 3. Resolution

* **PRESSURE_MUST_RESOLVE_OR_BE_ELIMINATED**
  Pressure must either resolve into invariant-preserving form or be eliminated as invalid.

* **PRESSURE_RESOLUTION_REDUCES_UNRESOLVED_BURDEN**
  Valid resolution reduces pressure by proving admissibility under active constraints.

* **PRESSURE_ELIMINATION_REMOVES_INVALID_POSSIBILITY**
  Elimination reduces pressure by removing states that fail enforcement.

---

## 4. Leakage

* **PRESSURE_LEAKAGE_PRESERVES_BURDEN**
  Leaked pressure survives in relocated form rather than disappearing.

* **PRESSURE_CANNOT_COUNT_AS_RESOLVED_WHEN_LEAKED**
  Pressure that moves across a boundary without validation or elimination remains unresolved.

* **PRESSURE_LEAKAGE_PREVENTS_CLOSURE**
  Closure cannot complete while pressure can leak into another layer, component, abstraction, interpretation, or future state.

---

## 5. Field Behavior

* **PRESSURE_IS_FIELD_DISTRIBUTED**
  Pressure is distributed across locations, layers, boundaries, and interpretations rather than isolated to a single event.

* **PRESSURE_HAS_MAGNITUDE_AND_DENSITY**
  Pressure can vary by amount and concentration of unresolved burden.

* **PRESSURE_HAS_DIRECTION_AND_GRADIENT**
  Pressure tends to move along gradients toward weaker seals, wider exits, or less constrained regions.

---

## 6. Boundary Behavior

* **PRESSURE_IS_REGULATED_BY_SEALS**
  Seals determine whether pressure is contained, transformed, validated, eliminated, or leaked.

* **PRESSURE_CANNOT_BYPASS_BOUNDARY_ENFORCEMENT**
  Pressure must not cross an enforced boundary without admissibility being evaluated.

* **PRESSURE_EXPOSES_WEAK_SEALS**
  Weak seals are revealed by pressure that passes forward without resolution.

---

## 7. Accumulation & Compression

* **PRESSURE_ACCUMULATES_UNDER_DEFERRAL**
  Pressure accumulates when unresolved burden is admitted faster than it resolves or is eliminated.

* **PRESSURE_COMPRESSES_AS_STATE_SPACE_NARROWS**
  Pressure becomes denser when admissible state space narrows while unresolved burden remains.

* **PRESSURE_INCREASES_WITH_UNRESOLVED_OPTIONALITY**
  Unresolved optionality increases pressure when possible paths remain unvalidated under constraints.

---

## 8. Recursion

* **PRESSURE_CAN_REENTER_THROUGH_RECURSION**
  Recursion can reintroduce unresolved burden unless recursive paths are sealed.

* **PRESSURE_AMPLIFIES_WHEN_UNDERSEALED**
  Undersealed recursion can preserve, hide, distribute, or magnify pressure.

* **PRESSURE_REFINES_WHEN_RECURSION_IS_SEALED**
  Properly sealed recursion can reduce pressure by eliminating invalid survivability on each pass.

---

## 9. Layer Transformation

* **PRESSURE_TRANSFORMS_ACROSS_LAYERS**
  Pressure changes form as it descends the invariant stack while remaining unresolved admissibility burden.

* **PRESSURE_CONVERTS_TO_CONSEQUENCE_UNDER_ENFORCEMENT**
  Pressure becomes consequence when constraints are enforced against unresolved possibility.

* **PRESSURE_BECOMES_LESS_DEFERRABLE_AT_DEEPER_LAYERS**
  Deeper layers permit fewer disguises and fewer unresolved survival paths.

---

## 10. Truth & Closure

* **PRESSURE_PRECEDES_TRUTH_SELECTION**
  Pressure is the unresolved region from which truth is selected through constraint enforcement.

* **PRESSURE_BLOCKS_CLOSURE_WHILE_UNRESOLVED**
  Closure cannot increase while unresolved pressure remains hidden, leaked, or unvalidated.

* **PRESSURE_RESOLUTION_DRIVES_STABILITY**
  Stability increases when pressure resolves rather than leaking or accumulating.

---

# Final Compression

> Pressure is unresolved possibility under constraint.
> It must resolve into invariant-preserving form,
> be eliminated as invalid,
> or leak as preserved burden.
> Closure increases only when pressure resolves without leakage.
