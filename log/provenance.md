# Provenance Index (out-of-band)

This index maps governed files to the ADRs and commits that changed them. It is updated during `/record` and referenced in the changelog. It keeps constitutional and act texts clean (no inline markers).

Format:
- File path
  - ADR(s): adr-XXXX-title (and/or draft session link while pending)
  - Commit: ISO timestamp and commit subject
  - Sections changed: brief notes for human scan

Current entries:
- constitution.md
  - ADRs: adr-0010-foundational-design-principles-in-preamble (Accepted)
  - Commit: 2025-11-12 feat(preamble): add Foundational Design Principles + Interpretive Use; link Article I; refs adr-0010
  - Sections changed: Preamble (Foundational Design Principles; Interpretive Use); Article I chapeau

- acts/ (no changes in this session)


