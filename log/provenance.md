# Provenance Index (out-of-band)

This index maps governed files to the ADRs and commits that changed them. It is updated during `/record` and referenced in the changelog. It keeps constitutional and act texts clean (no inline markers).

Format:
- File path
  - ADR(s): adr-XXXX-title (and/or draft session link while pending)
  - Commits: short SHAs and messages
  - Sections changed: brief notes for human scan

Current entries:
- constitution.md
  - ADRs: adr-0010-foundational-design-principles-in-preamble (Accepted)
  - Commits: (to be added at `/check-in`)
  - Sections changed: Preamble (Foundational Design Principles; Interpretive Use); Article I chapeau

- acts/ (no changes in this session)


