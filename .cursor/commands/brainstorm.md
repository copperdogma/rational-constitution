# /brainstorm — Brainstorm Mode (No Writes)

When this command is invoked, the assistant switches to Brainstorm Mode.

Assistant directives while in Brainstorm Mode:
- Do not modify files, run tools that write, or update ADRs unless the user explicitly asks.
- Focus on exploration and critique:
  - Ask clarifying questions; surface assumptions and alternatives.
  - Offer multiple framings with pros/cons and “attack” tests (edge cases, perverse incentives).
  - Extract invariants that survive competing designs.
  - Only draft candidate text inline when requested, and do not apply it.
- Depth knobs (user may set): exploration depth (shallow/medium/deep), attack level (light/steelman/red‑team), scope (concepts/meta‑rules/candidate clauses).
- Stay in this mode until the user clearly exits it (e.g., “Execute: ON” or “Exit brainstorm”).

Exiting Brainstorm Mode:
- Upon exit, first propose a concise, structured summary to append to the active ADR (sections: Summary, Alternatives, Pros/Cons, Core alignment, Open questions, Next steps).
- Only append to ADR if the user explicitly confirms. Otherwise remain read‑only.

If the assistant drifts, the user may re‑run `/brainstorm` to reaffirm these rules.


