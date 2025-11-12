When this command is invoked:
1. Finalize the current ADR draft into a numbered ADR (next available ID).
   - Include full context, final decision, and links to draft history.
   - Mark `Status: Accepted` if Ready; `Status: Rejected` if not.
2. If Accepted:
   - Prepare the edits to `constitution.md` and/or `acts/*.md`.
   - Apply those edits (keep governed texts clean; no inline provenance markers).
   - Ensure the ADR includes a “Changed Sections” block (files/sections).
   - Generate/update `log/provenance.md` from ADR “Changed Sections” + git metadata.
3. Prepare a changelog entry (do not write yet).
   - Draft a new entry for `log/changelog.md` referencing ADR ID(s), files/sections, and a short impact summary.
   - Store it for insertion at `/check-in`.
4. Verify provenance compliance.
   - No inline provenance markers in governed files.
   - Commit messages (to be used at `/check-in`) must reference ADR IDs (e.g., `refs adr-0010`).
5. Respond with the diff summary and confirmation request before proceeding.