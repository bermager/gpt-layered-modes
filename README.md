# Personal Mode System (Versioned)

This repository stores versioned snapshots of:

- Default operating layer
- Optional cognitive overlays (modes)
- Change history

Goal:
Track evolution of reasoning discipline and interaction design over time.

Usage Examples:

#DeepArchitecture
Analyze this system design.

Normal answer. Then #Expert.

Modes are additive overlays.
#Expert appends an Expert Addendum and may critique gaps in the main answer.


## Review & Release Protocol

Frequency: ~every 3 months (or earlier if a major workflow change happens).

Steps:
1. Review how the last version behaved in real usage:
   - What became more useful?
   - What became annoying/noisy?
   - Any missing mode or rule?
2. Compare current `main` with the last tagged version:
   - `git diff vX.Y..main`
3. Update files (`default.md`, `modes.md`, `CHANGELOG.md`) with changes.
4. Commit with message: `chore: modes vX.Y`
5. Create annotated tag:
   - `git tag -a vX.Y -m "short summary"`
6. Push:
   - `git push`
   - `git push origin vX.Y`
