# ADR Draft — Clean-Text Provenance Policy
Status: Finalized — See ADR-0011 (`log/ideas/adr-0011-clean-text-provenance-policy.md`)
Timestamp: 2025-11-12 13:00

## Summary
Adopt a clean-text provenance policy: remove inline markers/footers from governed texts and maintain provenance via ADRs, commit messages, changelog, and an out-of-band index at `log/provenance.md`.

## Proposed Change
- Update `AGENTS.md`:
  - Guardrails: “Keep constitutional/act text clean; no inline provenance markers or footers.”
  - Provenance Policy: remove inline comment markers; define provenance sources (ADRs, commits, changelog) and add a `log/provenance.md` index updated at `/record`.
- Create `log/provenance.md` with format and initial entry for current session.

## Rationale
- Preserve the readability and ceremonial nature of governed texts.
|- Ensure full traceability through ADRs and version control without embedding metadata.
- Provide a single index file for quick lookup and external publication.

## Pros
- Clean public documents; avoids “cruft.”  
- Clear, centralized mapping for auditors.  
- Compatible with existing ADR/changelog workflows.

## Cons / Risks
- Requires discipline to keep index in sync at `/record`.  
- One more file to maintain (mitigated by automation later).

## Links
- Edited: `AGENTS.md` (Provenance and Guardrails)  
- Added: `log/provenance.md`

## Next Steps
1) Socialize policy and confirm.  
2) If approved, include in `/record` flow that the index is updated and cross-referenced in `log/changelog.md`.  
3) Optionally add a CI check to ensure new governed edits reference an ADR in commit message and update the index.


