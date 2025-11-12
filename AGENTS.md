# AGENTS.md — Rational Constitution Project

## Mission
Collaboratively evolve a minimal, rational constitution and related Acts using Markdown.
All deliberation is recorded through automatically maintained ADR drafts; all final changes are validated, logged, and committed only with explicit consent.

---

## Guardrails
- Only edit files when asked; **/check-in** is the explicit commit/push trigger.
- During **/check-in**, the **only content change** allowed is updating `log/changelog.md`.
- Keep constitutional/act text clean; use a single-file provenance marker (see below).
- Prefer small, auditable diffs; reference ADRs in ADRs, commits, and changelog (not inline in articles).

## Provenance (per file)
- Add a single, non-intrusive marker at file top:
  <!-- provenance: adr-0009, adr-0006 -->
- Detailed mapping lives in ADRs, commits, and changelog.
  
---

## Automatic ADR Handling

When conversation touches on constitutional or structural topics:

1. **Detect or create an active ADR draft** in `log/ideas/_drafts/` for the topic.
   - Name: `session-YYYYMMDD-HHMM-topic.md`
   - Include timestamp, summary, and incremental updates as discussion progresses.
2. **Append updates automatically** after each significant turn:
   - Add new arguments, tradeoffs, pros/cons, open questions.
   - Update Core alignment flags.
   - Do not overwrite previous text except to fix clarity/typos.
3. If conversation shifts topics:
   - Pause current ADR (record timestamp).
   - Start or switch to a new ADR draft.
4. ADR drafts remain until `/record` finalizes them into numbered ADRs.
5. Old drafts remain archived for full historical transparency.

---

## Constitutional Core (Decision Filter)

All proposals must satisfy:

1. **Assume human nature** – individuals/corporations act in self-interest; design incentives accordingly.  
2. **Harness, don’t hope** – channel ambition toward public good; avoid dark incentives.  
3. **Power diffused, checked** – minimize concentrated authority; ensure retroactive accountability.  
4. **Radical transparency** – data, models, and actions open by default.  
5. **Democracy on outcomes** – citizens vote for goals, technocrats execute; measure all results.  
6. **Market where possible** – use externality pricing and performance competition.  
7. **Measurement over assertion** – every mandate/policy must define metrics and audit windows.

When proposing or revising anything, the AI must evaluate compliance with each tenet and record that evaluation in the ADR.

---

## Workflow Overview

### 1. Discussion & Auto-Recording
- As ideas evolve, Cursor continuously appends updates to the active ADR draft.
- Each turn may add:
  - New arguments
  - Pros/Cons
  - Core compliance notes
  - Open questions (to `log/open-questions.md` if appropriate)

### 2. Convergence
- When prompted via `/converge`, summarize and assess readiness:
  - Identify alignment/conflicts with Core.
  - Recommend: Reject, Needs Work, or Ready.

### 3. Recording & Implementation
- `/record` finalizes the ADR:
  - Numbered ADR created from draft.
  - Constitution/Acts edited if “Ready”.
  - Changelog updated automatically.

### 4. Validation & Commit
- `/validate` checks consistency, Core adherence, and completeness.
- `/check-in` adds changelog entry, prepares commit message, and pushes only after confirmation.

### Check-in Preconditions
- All intended edits (ADR finalization, constitution/acts changes) must already be applied and reviewed.
- `/check-in` will refuse to run if non-changelog edits are pending (dirty working tree with unstaged/unsaved changes).
- The only write performed by `/check-in` is inserting the prepared changelog entry.

---

## File Conventions

| Type | Location | Notes |
|------|-----------|-------|
| Constitution | `constitution.md` | Canonical master text |
| Acts | `acts/*.md` | Supplemental laws |
| ADR Drafts | `log/ideas/_drafts/` | Auto-updating working discussions |
| ADR Final | `log/ideas/adr-XXXX-title.md` | Immutable decision records |
| Changelog | `log/changelog.md` | Auto-updated at /record |
| Open Questions | `log/open-questions.md` | Append-only list, linked from ADRs |

---

## Editing Rules

- Preserve structure, numbering, and voice.
- Keep the constitutional and act texts **clean** (no inline ADR references in articles/sections).
- Record provenance **once per file** using the Provenance Policy below.
- For multi-section edits, keep diffs minimal and atomic when possible.
- Cross-reference ADRs in the **changelog** and within the **ADR** itself (pointing to the exact sections changed).
  
---

## Provenance Policy

**Purpose:** maintain clean text while preserving full traceability.

- Each governed file (e.g., `constitution.md`, `acts/*.md`) includes one silent provenance marker at the top.
- Use an HTML comment in reverse-chronological order:
  <!-- provenance: adr-0009, adr-0006 -->

- Never embed ADR references inline in the text.
- Detailed section mapping lives in:
  - the **ADR** itself (under “Links” or “Changed Sections”),
  - the **commit message**, and
  - the **changelog**.

If a file is meant for public consumption (e.g., published Acts):
- Add a small footer line instead of an HTML comment:
  > History: updated per adr-0009 (see `log/ideas/adr-0009-...md`)

When exporting or publishing externally, you can safely strip these comments; provenance persists via ADRs, commits, and changelog.

---

## Summary of Commands

| Command | Purpose |
|----------|----------|
| `/converge` | Summarize and evaluate discussion state |
| `/record` | Finalize ADR and apply edits if Ready |
| `/validate` | Pre-commit verification |
| `/check-in` | Log, commit, and push on confirmation |

---

## Example Flow

1. **Discuss freely.** Cursor auto-records into current ADR draft.
2. **Use `/converge`** to review and gauge readiness.
3. **Decide:** if Ready → `/record`; if not → keep discussing.
4. **Run `/validate`** to verify compliance and coherence.
5. **Approve `/check-in`** to finalize, commit, and push.

---

### Key Principles

- The AI **always records**, **never forgets**, and **never commits without you**.  
- Every decision traces back to an ADR.  
- Every ADR traces back to transparent reasoning.  
- Every change traces back to both.

This guarantees a complete, auditable record of constitutional evolution.

---