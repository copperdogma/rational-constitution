# ADR-0011 — Clean-Text Provenance Policy
Status: Accepted  
Date: 2025-11-12

## Context
We want governed texts (`constitution.md`, `acts/*.md`) to remain pristine with no inline markers. Provenance should be traceable through ADRs, commits, and the changelog, with a convenient out-of-band index.

## Decision
Adopt a clean-text provenance policy:
- No inline provenance markers or footers in governed texts.
- Maintain provenance via ADRs (with “Changed Sections”), commit messages referencing ADR IDs, and `log/changelog.md`.
- Keep a non-invasive index at `log/provenance.md` mapping files to ADRs and the commit timestamp + subject. The index is generated/updated at `/record`.

## Rationale
- Preserves the readability and ceremonial nature of governed texts.
- Keeps full traceability via ADRs and version control.
- Provides a quick reverse lookup without modifying governed texts.

## Changed Sections
- File: `AGENTS.md`
  - Guardrails and Provenance Policy updated to remove inline marker guidance; define clean-text policy and index.
- File: `.cursor/commands/record.md`
  - Generate/update `log/provenance.md` at `/record`; use timestamp + commit subject (no SHA).
- File: `.cursor/commands/validate.md`
  - Validation checks provenance compliance and the presence of ADR “Changed Sections.”
- File: `.cursor/commands/check-in.md`
  - Clarify committing all intended files; no provenance edits at `/check-in`.
- File: `log/provenance.md`
  - Added index file and standardized format (timestamp + subject).
- File: `.mdc/rules.md`
  - Added rules to enforce clean-text provenance and ADR discipline.

## Links
- Draft history: `log/ideas/_drafts/_archived/session-20251112-1300-provenance-policy-clean-text.md`
- Related change: ADR-0010 (Foundational Design Principles in the Preamble)

## Notes
- The provenance index can be regenerated from ADRs and git history; it is safe to publish and does not affect governed texts.


