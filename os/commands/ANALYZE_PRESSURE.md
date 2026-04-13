# **ANALYZE_PRESSURE**

This command is used when the user says:

```text
ANALYZE_PRESSURE
```

Analyze an invariant catalog as a pressure-and-seal system, generate `Pressure_Exits.md`, generate `Seals.md`, and compute recursive invariant closure before and after seals are applied.

---

## **Purpose**

Create repeatable pressure analysis artifacts for an invariant structure.

The command identifies where invariant groups force missing meaning, ambiguity, drift, or proof gaps to surface, where semantic leakage is sealed, which explicit sealing invariants should be added, and how those seals change recursive invariant closure.

---

## **Input**

- `invariant_source`: optional path to the invariant catalog; default `docs/invariants/README.md` in the target workspace.
- `pressure_output`: optional output path for the pressure analysis; default `docs/invariants/Pressure_Exits.md` in the target workspace.
- `seals_output`: optional output path for the sealing invariant analysis; default `docs/invariants/Seals.md` in the target workspace.

Paths are resolved against the target workspace unless the user provides absolute paths.

---

## **Required Behavior**

When invoked, the agent must:

- Read the invariant catalog from `invariant_source`.
- Treat the catalog as an invariant structure, preserving its visible grouping as the primary analysis unit.
- Generate `Pressure_Exits.md` with the exact output structure described in **Pressure Exits Output Structure**.
- Generate `Seals.md` with the exact output structure described in **Seals Output Structure**.
- Rate `Pressure`, `Seal Strength`, baseline recursive invariant closure, and sealed recursive invariant closure on a `0-1` scale.
- Provide concise rationale for every rating.
- Include an explicit baseline RIC and a sealed RIC.
- Ensure sealed RIC does not claim full `1.00` closure unless every required dependency map, threshold policy, glossary resolution, proof artifact, and enforcement check is present and verified.
- Keep the command side effects limited to creating or updating `pressure_output` and `seals_output`.
- Avoid Git operations, dependency installation, publishing, or network access.

---

## **Pressure Exits Output Structure**

Write `pressure_output` as Markdown using this structure:

````markdown
# Constraint-Driven Development - Pressure Exits

This table evaluates the invariant structure in `README.md` as a pressure-and-seal system.

**Pressure** rates how strongly the invariant area forces missing intent, ambiguity, drift, or proof gaps to surface before downstream authority is granted.

**Seal Strength** rates how strongly the invariant area prevents unauthorized semantic expansion, leakage, bypass, or unproven behavior from crossing layer boundaries.

Ratings use a 0-1 scale, where `0` means no effective pressure or seal and `1` means complete, mechanically enforceable pressure or seal.

| Invariant Area | Pressure | Pressure Rationale | Seal Strength | Seal Strength Rationale |
|---|---:|---|---:|---|
| <Invariant area from source> | <0-1 rating> | <Rationale> | <0-1 rating> | <Rationale> |

## Total Recursive Invariant Closure

| Structure | Closure Rating | Rationale |
|---|---:|---|
| <Structure analyzed> | <0-1 baseline RIC> | <Rationale> |

<One concise paragraph explaining what prevents full mechanical closure, if anything.>
````

The pressure table must keep one row per major invariant area unless the source catalog is too small, in which case it may use one row per invariant.

---

## **Seals Output Structure**

Write `seals_output` as Markdown using this structure:

````markdown
# Constraint-Driven Development - Sealing Invariants

This document defines sealing invariants for the invariant structure in `README.md` and recomputes recursive invariant closure with those seals applied.

A sealing invariant prevents semantic leakage across a boundary. It either blocks unauthorized addition, blocks silent loss, blocks bypass, or requires evidence before authority is granted.

## Sealing Invariants

| Seal ID | Sealing Invariant | Boundary Sealed | Rationale |
|---|---|---|---|
| <STABLE_SEAL_ID> | <Invariant statement> | <Boundary sealed> | <Rationale> |

## Seal Application Map

| Prior Closure Gap | Applied Seal |
|---|---|
| <Gap from baseline pressure analysis> | <Seal IDs that address it> |

## Recursive Invariant Closure With Seals Applied

| Structure | Baseline RIC | Sealed RIC | Delta | Rationale |
|---|---:|---:|---:|---|
| <Structure analyzed plus sealing invariants> | <0-1 baseline RIC> | <0-1 sealed RIC> | <signed delta> | <Rationale> |

## Residual Closure Gap

| Remaining Gap | Effect on RIC | Required Next Artifact |
|---|---|---|
| <Remaining gap> | <Why it prevents full closure> | <Artifact or check required> |

Sealed RIC is `<0-1 sealed RIC>`: <one concise sentence explaining the sealed closure state and why it is or is not complete>.
````

The sealing invariants must include seals for canonical source authority, parent containment, no silent loss, no unauthorized addition, intermediate layer requirements, glossary resolution, stable identity, constraint admissibility, proof-before-authority, negative space, contract boundaries, double symmetry, coverage thresholds, drift revalidation, re-lowering over patching, exception visibility, reviewable structure, and mechanical enforcement when those concerns are relevant to the source catalog.

---

## **Rating Guidance**

Use the following interpretation for all `0-1` ratings:

- `0.00-0.24`: weak or absent; mostly unstated or unenforceable.
- `0.25-0.49`: partial; some relevant concepts exist but major gaps remain.
- `0.50-0.74`: moderate; the concept is present but enforcement or coverage is incomplete.
- `0.75-0.89`: strong; most structural requirements are present with identifiable residual gaps.
- `0.90-0.99`: very strong; the structure is substantially closed but still missing some proof, enforcement, or generated evidence.
- `1.00`: complete; closure is mechanically demonstrated and enforceable for the analyzed scope.

Baseline RIC must reflect the invariant source before generated sealing invariants are applied.

Sealed RIC must reflect the invariant source plus the sealing invariants generated in `seals_output`.

---

## **Response Format**

After writing the files, respond with:

```text
Generated pressure analysis artifacts:
- <pressure_output>
- <seals_output>

Baseline RIC: <0-1 rating>
Sealed RIC: <0-1 rating>

<One concise note about any residual closure gap or verification not performed.>
```

---

## **Failure Behavior**

If the command cannot run, the agent must:

- Say which input, file, directory, permission, or context is missing.
- Avoid inventing invariant content when the source catalog cannot be read.
- Avoid writing partial output unless the user explicitly asks for a partial artifact.
- Avoid claiming sealed RIC improvements unless sealing invariants were actually generated and tied to baseline closure gaps.
