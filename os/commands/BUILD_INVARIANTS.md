# **BUILD_INVARIANTS**

This command is used when the user says:

```text
BUILD_INVARIANTS
```

The agent must rebuild the upstream invariant parent shell at `docs/invariants/Invariants.md` from the downstream invariant catalogs in this repository.

---

## **Purpose**

Generate the monotonic parent shell for the invariant structure.

The generated document must define the outermost invariant shell that contains all downstream invariant catalogs. Downstream invariants may refine, specialize, localize, or operationalize the parent shell, but they must not weaken, bypass, contradict, or reverse it.

---

## **Source Files**

Read these files from the repository root when they exist:

```text
docs/invariants/core/README.md
docs/invariants/pressure/README.md
docs/invariants/invalidity/README.md
docs/invariants/closure/README.md
docs/invariants/truth/README.md
docs/invariants/Invariant-Layers.md
```

Optional supporting context:

```text
docs/foundations/Pressure.md
docs/foundations/Invalidity.md
docs/foundations/Closure.md
docs/foundations/Truth.md
docs/glossary/README.md
```

If a required downstream catalog is missing, stop with a blocker and do not rewrite the output file.

---

## **Output File**

Write the rebuilt parent shell to exactly:

```text
docs/invariants/Invariants.md
```

All file paths displayed inside the generated Markdown must be relative paths from the repository root forward. Do not emit absolute Windows paths in the generated document.

---

## **Side Effects**

This command may:

- Read Markdown files under `docs/invariants`, `docs/foundations`, and `docs/glossary`.
- Create or replace `docs/invariants/Invariants.md`.

This command must not:

- Modify downstream invariant catalogs.
- Modify foundation documents.
- Modify glossary documents.
- Modify files outside `docs/invariants/Invariants.md`.
- Stage, commit, reset, push, or otherwise alter Git state.
- Use network access.

---

## **Rebuild Rules**

When invoked, the agent must:

1. Read the downstream invariant catalogs listed in the source files.
2. Extract the downstream catalog names, relative paths, section headings, and invariant IDs.
3. Identify the monotonic parent obligations that contain those downstream invariants.
4. Rebuild `docs/invariants/Invariants.md` as a parent shell rather than a raw concatenation.
5. Include links to every downstream catalog using repo-root-relative or output-relative Markdown links that resolve from `docs/invariants/Invariants.md`.
6. Include a `Monotonic Containment Law` section.
7. Include parent-shell invariants using the `INVARIANT_` prefix.
8. Include a downstream containment map showing how each downstream catalog is contained by the parent shell.
9. Include a downstream validity test that rejects weakening, contradiction, bypass, leakage-as-resolution, false closure, assertion-as-truth, and lower-layer override.
10. Include a final compression section.

---

## **Generated Document Requirements**

The generated `docs/invariants/Invariants.md` must contain:

```text
# Invariant-Core - Invariants

---

## Purpose
...

## Monotonic Containment Law
...

## <parent invariant sections>
...

## Downstream Containment Map
...

## Downstream Validity Test
...

# Final Compression
...
```

Parent invariant IDs must use this shape:

```text
* **INVARIANT_<UPPER_SNAKE_CASE_ID>**
  <one concise explanatory sentence>
```

---

## **Path Display Rule**

When displaying paths in generated Markdown, use relative paths only.

Correct:

```text
docs/invariants/core/README.md
docs/invariants/pressure/README.md
docs/invariants/Invariants.md
```

Do not display absolute machine-local paths.

---

## **Validation**

After rebuilding, verify:

- `docs/invariants/Invariants.md` exists.
- All generated Markdown links resolve locally.
- Every parent invariant bullet starts with `INVARIANT_`.
- No absolute Windows paths appear in the generated file.
- `git diff --check -- docs/invariants/Invariants.md` reports no whitespace errors.

---

## **Return**

Use this shape:

```text
BUILD_INVARIANTS complete.

Output:
- docs/invariants/Invariants.md

Inputs:
- <relative input path>
- <relative input path>

Validation:
- <check>: <result>

Notes:
- <short note or "None">
```
