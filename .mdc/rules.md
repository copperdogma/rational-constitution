# MDC Rules — Clean-Text Provenance and ADR Discipline

Purpose: Keep governed texts pristine while ensuring full, auditable provenance.

Checks
- No inline provenance markers:
  - Forbid `<!-- provenance:` and `History: updated per adr-` in:
    - `constitution.md`
    - `acts/*.md`
- ADR finals must include “Changed Sections”:
  - File: `log/ideas/adr-*.md`
  - Must contain a header “Changed Sections” and at least one bullet listing `path: section` (section may be brief text if unnumbered).
- Commit messages must reference an ADR:
  - At `/check-in`, commit subject contains `adr-` followed by digits (e.g., `refs adr-0010`).
- Provenance index maintenance:
  - `log/provenance.md` is generated/updated during `/record` from ADR “Changed Sections” and git metadata; it must not be hand-edited during `/check-in`.

Guidance (non-failing)
- Keep changelog entries concise and link to ADR IDs.
- Prefer small, atomic diffs; avoid bundling unrelated constitutional/act edits.


