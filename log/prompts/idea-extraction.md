# Idea Extraction Prompt

Use case: You've just finished a long conversatio with AI on a topic and think some of the ideas should be added to the proposal.


--------------------------------


We’ve now completed a long, detailed conversation about the prison/penal system proposal. The conversation may have involved multiple AIs; any contribution that met the analytical constraints counts. I want you to extract only what genuinely matters.

Your task is to produce two documents, and the final output of both must be in Markdown.

Do NOT rewrite the proposal.
Do NOT summarize the whole conversation.
Do NOT add new ideas that were never discussed.
Do NOT include optional elaborations or rhetorical restatements.

Focus strictly on what the conversation showed must be changed, clarified, or made explicit.

---

### Document 1 (Markdown) — Essential additions to the proposal

Title it:

# Essential Additions to the [Prison Proposal]

List only the changes that are genuinely required to keep the proposal:
- logically consistent,
- practically coherent,
- aligned with its own moral axioms.

For each essential item, use this structure:

1. **Label:** short name
   - **Type:** (clarification | new safeguard | constraint | definitional fix | structural change)
   - **Change Needed:**
     - A concrete, succinct statement of what must be added/adjusted in the proposal.
     - Mention where it fits (e.g., Rights section, Market section, Sentencing section).
   - **Minimal Rationale (1–3 sentences):**
     - Only why this change is structurally necessary.

Keep this document lean. If something does not materially affect the architecture of the system, leave it out. Ensure it's formatted as Markdown.

---

### Document 2 (Markdown) — Full reasoning behind each essential addition

Title it:

# Reasoning Behind Essential Additions

Use the **same labels and numbering** as in Document 1.

For each item:

1. **Label:** (must match)
   - **Problem Exposed:**
     - What tension, inconsistency, or ambiguity the conversation revealed.
   - **Resolution:**
     - How the change (from Document 1) addresses it without altering the core framework.
   - **Key Arguments / Tradeoffs:**
     - Summarize the relevant reasoning that led to the conclusion.
   - **Status:** (resolved | partially resolved, needs future refinement)

This document can be longer, but keep it analytic and tightly tied to the conversation. Ensure it's formatted as Markdown.