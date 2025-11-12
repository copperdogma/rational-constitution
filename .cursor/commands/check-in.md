# Check In Changes

1. **Review**
   - Run:
     - `git diff --name-only` (working tree)
     - `git diff --name-only --cached` (staged)
   - Preconditions:
     - All intended edits (constitution/acts/ADRs/tooling) have been applied and validated.
     - Stage ALL intended files. Unstage or revert anything unintended.
     - ADRs are finalized; changelog entry is prepared.

2. **Update log/changelog.md**
   - Add a dated entry summarizing what was added, changed, or finalized.
   - Reference ADR numbers and include a short summary of impact.

3. **Commit**
   - Prepare a commit message that references the relevant ADR ID(s), e.g.:
     - `feat(constitution): add Foundational Design Principles; refs adr-0010`
   - Ensure only intended files (including `log/changelog.md`) are staged.
   ```bash
   git add .
   git status
   # If OK:
   git commit -m "<your message with adr-XXXX reference>"

	4.	Push

git push origin main


Notes:
	•	Provenance index updates happen during `/record` (do not modify it during `/check-in`).
	•	All content edits (constitution, acts, ADRs) must already be reviewed and validated prior to committing.