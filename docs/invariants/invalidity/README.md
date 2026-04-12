# Invariant-Core - Invalidity Invariants

---

## 1. Existence & Scope

* **INVALIDITY_EXISTS_BY_CONSTRAINT_VIOLATION**
  Invalidity exists when a state, interpretation, transition, or configuration violates an active invariant or constraint.

* **INVALIDITY_IS_CONSTRAINT_RELATIVE**
  Invalidity is defined relative to the active constraint field that governs admissibility.

* **INVALIDITY_IS_BROADER_THAN_FALSEHOOD**
  Falsehood is a semantic form of detected invalidity, not the full scope of invalidity.

---

## 2. Detection

* **INVALIDITY_IS_DETECTABLE_BY_SINGLE_FAILURE**
  One required invariant failure is sufficient to establish invalidity.

* **INVALIDITY_DOES_NOT_REQUIRE_GLOBAL_KNOWLEDGE**
  Invalidity can be detected locally even when truth has not been globally proven.

* **INVALIDITY_REQUIRES_ENFORCED_REJECTION**
  Detected invalidity must be rejected by an enforced constraint rather than merely suspected.

---

## 3. Truth Asymmetry

* **INVALIDITY_IS_NOT_TRUTH_ABSENCE_ALONE**
  A state not yet proven true is unresolved pressure unless an invariant failure has been detected.

* **INVALIDITY_DEFEATS_TRUTH**
  A state cannot be true if it contains any required invariant violation.

* **INVALIDITY_CAN_BE_LOCAL_WHILE_TRUTH_IS_GLOBAL**
  Invalidity can be established by local failure, while truth requires complete constraint survival.

---

## 4. Pressure Evaluation

* **INVALIDITY_CAN_EXIST_WITHIN_PRESSURE**
  Unresolved pressure may contain candidate invalidity before enforcement exposes it.

* **INVALIDITY_EMERGES_WHEN_PRESSURE_FAILS_CONSTRAINTS**
  Pressure becomes detected invalidity when tested against constraints and rejected.

* **INVALIDITY_MUST_NOT_REMAIN_UNRESOLVED_AFTER_DETECTION**
  Once detected, invalidity must be eliminated, contained, or transformed into validity.

---

## 5. Closure Blocking

* **INVALIDITY_PREVENTS_CLOSURE_WHILE_SURVIVING**
  Closure cannot hold while invalidity can persist, propagate, leak, or return.

* **INVALIDITY_MUST_HAVE_NO_SURVIVAL_PATHS**
  Closure requires invalidity to have no path through the enforced system.

* **INVALIDITY_CANNOT_HIDE_UNDER_APPARENT_CONSISTENCY**
  Apparent consistency is not closure when latent invalidity remains.

---

## 6. Boundary Behavior

* **INVALIDITY_MUST_NOT_CROSS_BOUNDARIES_UNVALIDATED**
  Invalidity must not pass through boundaries without rejection, containment, or valid transformation.

* **INVALIDITY_LEAKAGE_PRESERVES_FAILURE**
  Leaked invalidity survives as unresolved or displaced failure.

* **INVALIDITY_EXPOSES_WEAK_BOUNDARIES**
  Boundaries are weak when they allow invalidity to propagate as if it were admissible.

---

## 7. Recursion & Re-Entry

* **INVALIDITY_MUST_NOT_REENTER_AFTER_REJECTION**
  Rejected invalidity must not return through recursive or indirect paths.

* **INVALIDITY_CAN_AMPLIFY_THROUGH_RECURSION**
  Undersealed recursion can preserve, distribute, or amplify invalidity.

* **INVALIDITY_REQUIRES_RECURSIVE_ELIMINATION**
  Recursive processes must eliminate invalidity on every pass where it can reappear.

---

## 8. Layer Integrity

* **INVALIDITY_CAN_APPEAR_AT_ANY_LAYER**
  Invalidity may occur at governance, implementation, algorithmic, protocol, architectural, domain, physical, mathematical, semantic, or meta-logical layers.

* **INVALIDITY_AT_LOWER_LAYERS_OVERRIDES_HIGHER_ACCEPTANCE**
  Higher-layer acceptance cannot make a lower-layer violation valid.

* **INVALIDITY_BECOMES_LESS_NEGOTIABLE_WITH_DEPTH**
  Invalidity becomes less deferrable as constraints become more intrinsic in deeper layers.

---

## 9. Consequence & Elimination

* **INVALIDITY_REQUIRES_CONSEQUENCE_UNDER_ENFORCEMENT**
  Enforced constraints must convert detected invalidity into rejection, elimination, or valid transformation.

* **INVALIDITY_MUST_NOT_PROPAGATE_AS_VALID**
  Invalid states must not continue through the system as if they satisfied constraints.

* **INVALIDITY_ELIMINATION_REDUCES_PRESSURE**
  Eliminating invalidity reduces unresolved burden and supports closure.

---

## 10. Operational Validity

* **INVALIDITY_EXISTS_WHEN_ADMISSIBILITY_FAILS**
  A state is invalid when it fails the admissibility conditions that govern it.

* **INVALIDITY_EXISTS_WHEN_LOWER_CONSTRAINTS_ARE_VIOLATED**
  A state is invalid when it contradicts lower-layer constraints, regardless of higher-layer approval.

* **INVALIDITY_EXISTS_WHEN_CLOSURE_CANNOT_INCREASE**
  A state remains invalid when its survival prevents closure from increasing.

---

# Final Compression

> Invalidity is failure to survive constraint enforcement.
> It requires only one enforced invariant failure,
> defeats truth,
> blocks closure while it survives,
> and must be eliminated, contained, or transformed before pressure can resolve.
