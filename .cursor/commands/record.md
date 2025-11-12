When this command is invoked:
1. Finalize the current ADR draft into a numbered ADR (next available ID).
   - Include full context, final decision, and links to draft history.
   - Mark `Status: Accepted` if Ready; `Status: Rejected` if not.
2. If Accepted:
   - Prepare the edits to `constitution.md` and/or `acts/*.md`.
   - Apply those edits with a note at top: “Updated per adr-XXXX”.
3. Append a summary to `log/changelog.md` automatically.
4. Respond with the diff summary and confirmation request before committing.