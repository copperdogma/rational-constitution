# ADR-0010 — Foundational Design Principles in the Preamble
Status: Accepted  
Date: 2025-11-12

## Context
The project’s Constitutional Core existed in `AGENTS.md` but was not explicit in the Constitution. We sought to expose these principles as a clear interpretive anchor while avoiding judicial overreach and redundancy with operational articles.

## Decision
Adopt the minimized set (Option M‑5), titled “Foundational Design Principles,” placed in the Preamble as the first explicit list, followed by an “Interpretive Use” clause (non‑self‑executing). Add a chapeau under Article I explicitly linking structure to these Principles. Keep governed texts clean of inline provenance markers.

## Rationale
- Clear interpretive anchor at the start of the Constitution.  
- Limits judicial creep with explicit non‑self‑executing language.  
- Harmonizes with existing Articles IV, X, XI without renumbering.  
- Preserves clean-text policy.

## Alternatives Considered
- Keep only in `AGENTS.md` (insufficient as a constitutional anchor).  
- Place under Article I (felt tacked-on; now resolved via Preamble).  
- Hard justiciability test (rejected; expands judicial power).

## Changed Sections
- File: `constitution.md`
  - Preamble: added “Foundational Design Principles” (M‑5) and “Interpretive Use”.
  - I. Foundations: added chapeau line tying structure to Principles.

## Links
- Related policy: ADR-0011 (Clean-Text Provenance Policy)

## Notes
- Acts and amendments shall be drafted to adhere to the Principles and interpreted to further them, consistent with Article IX.  
- Provenance is tracked via ADRs, commit messages referencing ADR IDs, `log/changelog.md`, and the generated `log/provenance.md`.

## Follow-up Considerations
- **Constitutional Core as judicial guide**: Should this be explicit in the constitution? A strong "spirit of the law" that can both be used as a litmus test for new proposals AND as a guide for the judiciary? Has that ever been done before? Does it work? Is it a good idea?


