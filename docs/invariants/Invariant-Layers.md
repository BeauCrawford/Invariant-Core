# Invariant-Core - Invariant Layers

Here is the invariant layer stack for `Invariant-Core`, ordered from highest-level external governance to lowest-level irreducible truth conditions.

---

## Invariant Layer Influence (High → Low)

|   # | Layer | Name                   | Structure (What it Stabilizes)          | Pressure Exit (What is Expelled)               | Seals (What is Enforced)            | Constraint (What is Forbidden)           | Authority (Source of Control)        |
| --: | ----- | ---------------------- | --------------------------------------- | ---------------------------------------------- | ----------------------------------- | ---------------------------------------- | ------------------------------------ |
|  10 | PPL   | Process / Governance   | System evolution, oversight             | Drift, misuse, non-compliance                  | Policy, audit, review gates         | Unauthorized change, unvalidated actions | Social / organizational authority    |
|   9 | IMP   | Implementation         | Runtime systems, infrastructure         | Bugs, crashes, undefined behavior              | Type systems, runtime checks        | Invalid execution states                 | System/runtime enforcement           |
|   8 | ALG   | Algorithmic            | Execution logic, optimization           | Non-termination, invalid paths                 | Correctness, convergence rules      | Ineffective or incorrect procedures      | Procedural / computational authority |
|   7 | PRC   | Protocol / Contract    | Valid interactions                      | Invalid inputs, contract violations            | Validation, schemas, access control | Unauthorized or malformed interaction    | Contractual / interface authority    |
|   6 | ARC   | Architectural          | Component structure, relationships      | Broken dependencies, miscomposition            | Interfaces, modular boundaries      | Invalid system composition               | Structural / design authority        |
|   5 | DOM   | Domain-Structural      | Problem decomposition, domain integrity | Cross-domain leakage, misapplied models        | Domain boundaries, scope control    | Invalid abstraction mapping              | Domain / model authority             |
|   4 | PHY   | Physical / Ontological | Real-world feasibility                  | Impossible states, unrealizable configurations | Causality, physical laws            | Violations of reality                    | Natural law / ontological authority  |
|   3 | MAT   | Mathematical           | Formal consistency, computability       | Undefined, non-computable forms                | Proof, formal validation            | Logical inconsistency in formal systems  | Mathematical necessity               |
|   2 | SEM   | Semantic               | Meaning coherence, interpretation       | Ambiguity, incoherence                         | Consistent interpretation rules     | Meaning contradiction                    | Interpretive / semantic authority    |
|   1 | MLI   | Meta-Logical           | Fundamental truth conditions            | Contradictions, paradoxes                      | Absolute invariants                 | Self-negation, logical impossibility     | Intrinsic / irreducible authority    |

---

## Interpretation

The stack expresses a descending gradient of constraint and authority.

As the layers descend:

- constraints become less negotiable
- authority becomes less external
- enforcement shifts from assigned control to unavoidable necessity

At the highest layers, enforcement is social, procedural, and organizational.  
At the lowest layers, enforcement is intrinsic: contradiction cannot survive regardless of preference, policy, or implementation. This means the lower the layer, the less optional its invariants become.

---

## Core Pattern

**Constraints define what cannot happen.**  
**Authority determines what enforces that.**

Across the stack, these begin as separate concepts, but they converge as you descend. At the deepest layer, constraint and authority become functionally identical:

> what is forbidden cannot occur

This convergence is strongest at the **Meta-Logical (MLI)** layer, where self-negation, contradiction, and logical impossibility are excluded by intrinsic necessity rather than external control.

---

## Layer Dynamics

Each layer stabilizes a different mode of structure and expels a different class of failure:

- **PPL** expels governance drift and misuse
- **IMP** expels invalid runtime behavior
- **ALG** expels non-convergent or incorrect procedure
- **PRC** expels malformed interaction
- **ARC** expels invalid composition
- **DOM** expels abstraction leakage
- **PHY** expels impossible states
- **MAT** expels formal inconsistency
- **SEM** expels incoherent meaning
- **MLI** expels contradiction itself

Together, these form a full-stack invalidity model spanning governance, software, formalism, semantics, and truth conditions.

---

## Governing Principle

A higher layer may refine, organize, or enforce a lower layer, but it may not violate it.

This implies a monotonic constraint order:

- process cannot override implementation truth
- implementation cannot override algorithmic correctness
- algorithmic procedure cannot override mathematical consistency
- semantic interpretation cannot override meta-logical necessity

Therefore:

> **No higher layer may violate a lower layer invariant.**

This is the vertical sealing law of the stack.

---

## Repository Role

Within `invariant-core`, these layers serve as the canonical frame for locating invariants by depth, type, and authority source.

They provide the basis for:

- layer-specific invariant definition
- cross-layer validation
- downward constraint alignment
- failure classification
- seal design and enforcement strategy

---

## Compressed Form

> The invariant layer stack orders structure by depth of necessity.
> Higher layers govern behavior through assigned authority.
> Lower layers govern possibility through intrinsic constraint.
> As depth increases, authority and constraint converge,
> until contradiction is excluded by necessity itself.
