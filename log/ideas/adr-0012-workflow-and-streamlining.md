# ADR-0012 — Workflow and Streamlining (Converge vs. Validate)
Status: Rejected  
Date: 2025-11-12

## Context
We discussed streamlining the authoring workflow in this repository, specifically whether to combine the `\converge` and `\validate` steps. The conversation was meta-process (tooling within Cursor) rather than constitutional text. Prior ADRs have covered process/policy topics when they affect governance authoring discipline (e.g., clean-text provenance).

## Decision
Reject the proposal to combine `\converge` and `\validate`. Keep them separate:
- `\converge` remains a deliberative summary and readiness recommendation.
- `\validate` remains the mechanical, file-diff-based quality and provenance check.

Optionally, consider future convenience chaining (e.g., `\review` alias to run both; `\record` auto-runs `\validate`) without merging semantics.

## Rationale
- Separation of concerns: preserves clarity between human judgment (deliberation) and automated verification (quality checks).
- Performance and ergonomics: keeps `\converge` fast during ideation; avoids imposing full validation overhead on early discussion.
- Auditability: maintains a clear boundary for what updates ADR drafts versus what certifies concrete changes for `/check-in`.
- Scope hygiene: respects the original intent to keep process/tooling choices distinct from constitutional content while still documenting reasoning.

## Alternatives Considered
1) Fully merge `\converge` and `\validate` — rejected for coupling deliberation to heavier checks.  
2) Convenience chaining (`\review`: Converge→Validate; `\record` auto-validate) — acceptable later without policy change.  
3) No action (status quo) — chosen; behavior remains unchanged.

## Consequences
- No change to command semantics or workflow.  
- Future convenience wrappers may be added without policy impact.  
- Documentation remains consistent: deliberation precedes validation.

## Changed Sections
- None (no governed text changes).

## Links
- `AGENTS.md` (Workflow Overview; Automatic ADR Handling)  
- `.cursor/commands/converge.md`  
- `.cursor/commands/validate.md`


