# Check In Changes

1. **Review**
   - Run `git diff --name-only` to confirm intended files only.
   - Ensure all constitutional or act changes have ADRs and are finalized.
   - Verify no temp or draft files are staged.

2. **Update log/changelog.md**
   - Add a dated entry summarizing what was added, changed, or finalized.
   - Reference ADR numbers and include a short summary of impact.

3. **Commit**
   - Prepare a commit message that references the relevant ADR ID(s), e.g.:
     - `feat(constitution): add Foundational Design Principles; refs adr-0010`
   - Ensure only `log/changelog.md` is modified at this step.
   ```bash
   git add log/changelog.md
   git commit -m "<your message with adr-XXXX reference>"

	4.	Push

git push origin main


Notes:
	•	No files are modified by this step except the changelog. Provenance index updates happen during `/record`.
	•	All content edits (constitution, acts, ADRs) must already be reviewed.