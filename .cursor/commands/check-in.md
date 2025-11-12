# Check In Changes

1. **Review**
   - Run `git diff --name-only` to confirm intended files only.
   - Ensure all constitutional or act changes have ADRs and are finalized.
   - Verify no temp or draft files are staged.

2. **Update log/changelog.md**
   - Add a dated entry summarizing what was added, changed, or finalized.
   - Reference ADR numbers and include a short summary of impact.

3. **Commit**
   ```bash
   git add .
   git commit -m "feat(constitution): integrate executive reforms; refs adr-0009"

	4.	Push

git push origin main


Notes:
	•	No files are modified by this step except the changelog.
	•	All content edits (constitution, acts, ADRs) must already be reviewed.