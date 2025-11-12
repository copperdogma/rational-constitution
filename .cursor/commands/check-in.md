# Check In Changes

Single-use authorization: Invoking `/check-in` grants permission to commit and push exactly once. It never grants ongoing permission. Each check-in must be explicitly requested again.

1. Review
   - Run:
     - `git diff --name-only` (working tree)
     - `git diff --name-only --cached` (staged)
   - Preconditions:
     - All intended edits (constitution/acts/ADRs/tooling) are applied and validated.
     - ADRs finalized (or explicitly Paused); changelog entry prepared.
     - Ensure no temp files, debug logs, or secrets are present; remove any unintended files.

2. Update changelog
   - Add a dated entry summarizing changes and referencing ADR IDs.
   - Save the file.

3. Stage and commit all
   - Stage ALL intended files (including the updated changelog); unstage or revert anything unintended.
   - Confirm `git status` shows only intended files.
   - Commit with ADR reference:
   ```bash
   git add .
   git status
   # If OK:
   git commit -m "<Brief description>; refs adr-XXXX"
   ```

4. Push
   - `git push origin main`

Notes
- Provenance index is handled at `/record` (do not modify it during `/check-in`).
- Commit message should reference ADR ID(s). If `git status` shows unintended files, revert/unstage before committing.
- This command performs no edits beyond committing already-reviewed work and the prepared changelog.