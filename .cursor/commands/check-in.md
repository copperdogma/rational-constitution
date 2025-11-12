# Check In Changes

Single-use authorization: Invoking `/check-in` grants permission to commit and push exactly once. It never grants ongoing permission. Each check-in must be explicitly requested again.

1. Review
   - Run:
     - `git diff --name-only` (working tree)
     - `git diff --name-only --cached` (staged)
   - Preconditions:
     - All intended edits (constitution/acts/ADRs/tooling) are applied and validated.
     - ADRs finalized (or explicitly Paused); changelog entry prepared.

2. Stage intended files
   - Stage ALL intended files; unstage or revert anything unintended.
   - Confirm:
     - `git status` shows only intended files.

3. Update changelog
   - Add a dated entry summarizing changes and referencing ADR IDs.

4. Commit
   - Message references ADR ID(s), e.g.:
     - `feat(constitution): add Foundational Design Principles; refs adr-0010`
   ```bash
   git add .
   git status
   # If OK:
   git commit -m "<your message with adr-XXXX reference>"
   ```

5. Push
   - `git push origin main`

Notes
- Provenance index is handled at `/record` (do not modify it during `/check-in`).
- This command performs no edits beyond committing already-reviewed work and the prepared changelog.