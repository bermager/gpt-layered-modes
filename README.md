# AI OS

Personal AI Operating System.

This repository defines a versioned interaction layer for working with ChatGPT in a structured, evolving, and governed way.

Instead of passively using AI, this system treats interaction rules as configuration — version-controlled, reviewed, and refined over time.

---

## Philosophy

AI OS is built on:

- Epistemic discipline (reduce assumptions, surface uncertainty)
- Capability transparency (no silent degradation)
- Constructive challenge (no default agreement)
- Ecosystem awareness (landscape, not absolutism)
- Platform awareness (use evolving tools properly)
- Modular overlays instead of rigid global constraints

Rules are adaptive and refactorable.

Deletion and simplification are part of maturity.

---

## Structure

- `default.md` — Default Operating Layer (always-on behavior)
- `modes.md` — Optional additive overlays (e.g., #Expert, #Fast)
- `CHANGELOG.md` — Evolution history
- Git tags — Version snapshots

---

## Mode Usage

Modes are activated per message using:

#ModeName

Examples:

#DeepArchitecture  
Analyze this system design.

Normal answer. Then #Expert.

---

## Mode Stacking Rules

- Base answer first (Default Operating Layer).
- Apply requested overlays after the base answer.
- If #Expert is included, it is appended LAST as an "Expert Addendum".
- Overlays are additive unless explicitly asked to replace the main answer.

---

## Review & Release Protocol

Frequency: ~every 3 months (or earlier if a major workflow change happens).

### Evaluation

1. Review how the last version behaved in real usage:
   - What became more useful?
   - What became annoying or noisy?
   - Any missing mode or rule?
   - Did any rule feel restrictive or obsolete?
   - Was #Expert helpful or overused?
   - Was Platform Awareness helpful or distracting?

2. Identify what can be simplified or removed:
   - Which rules are now implicit and don’t need to be written?
   - Which constraints reduce flexibility?
   - Is complexity increasing unnecessarily?

### Technical Comparison

3. Compare current `main` with the last tagged version:
   - `git diff vX.Y..main`

### Update & Version

4. Update files (`default.md`, `modes.md`, `CHANGELOG.md`) with changes.
5. Commit with message:
   - `chore: modes vX.Y`
6. Create annotated tag:
   - `git tag -a vX.Y -m "short summary"`
7. Push:
   - `git push`
   - `git push origin vX.Y`

---

## Governance Principle

AI OS is not dogma.

If any rule becomes limiting, outdated, redundant, or counterproductive,
it should be refactored or removed.

The goal is not accumulation — it is clarity and leverage.

Evolution over rigidity.
