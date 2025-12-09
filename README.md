# The Rational Constitution

A modern constitutional framework built on realism about human nature.

This project proposes a minimal, adaptive system of governance that assumes self-interest, designs for corruption, and turns ambition into public good through transparency, decentralization, and feedback.

## Core Principles

1. **The Externality Principle**  
   All harm must be priced. Activities that impose measurable costs on others internalize those costs through market-based mechanisms. Revenues return to citizens or reduce baseline taxes.

2. **The Public Goods Principle**  
   All citizens share in shaping the future. A portion of public funds is allocated through open, participatory funding—rewarding broadly supported projects and civic innovation.

3. **Checks, Balances, and Transparency**  
   Power is divided and audited by independent, rival institutions. Governance is open by default; secrecy is an exception requiring justification.

4. **Adaptive Self-Correction**  
   Laws, institutions, and taxes automatically sunset, review, or adjust according to measurable outcomes. The system learns without revolution.

## Repository Structure

- `constitution.md` – core constitutional text (modular sections).  
- `acts/` – implementing documents (e.g., Externality Pricing Act, Civic Funding Act).  
- `log/ideas/` – Architecture Decision Records (ADRs) documenting all design decisions.
  - `adr-XXXX-*.md` – finalized, numbered decision records.
  - `_drafts/` – active working drafts (auto-created during discussion).
- `log/changelog.md` – chronological record of all changes with ADR references.
- `log/provenance.md` – traceability index mapping files to ADRs and commits.  

## Origins
Based on ideas I had and conversions refining them with OpenAI's GPT5 (not public):
- https://chatgpt.com/c/69123bc4-69b8-8325-b272-b060a42ceeb8
- https://chatgpt.com/c/6912bcec-9f78-8326-bea7-57da99b644b6

## How This Project Works

### Architecture Decision Records (ADRs)

Every significant decision about the constitution or governance system is documented in an **Architecture Decision Record (ADR)**. ADRs ensure:

- **Full traceability**: Every change links back to transparent reasoning.
- **Auditable evolution**: Complete history of why decisions were made.
- **Clean text**: The constitution and acts remain uncluttered (no inline references).

### Workflow: How to Contribute

1. **Discuss** – Start a conversation about a constitutional topic (rights, governance structure, policy mechanisms, etc.).  
   - An ADR draft is **automatically created** in `log/ideas/_drafts/` when you discuss constitutional topics.
   - The draft is named `session-YYYYMMDD-HHMM-topic.md` and updates as discussion progresses.

2. **Converge** – Use `/converge` to review the discussion state:
   - Summarizes the proposal, pros/cons, and alignment with Core Principles.
   - Recommends: **Reject**, **Needs Work**, or **Ready**.

3. **Record** – Use `/record` to finalize the ADR:
   - Promotes the draft to a numbered ADR (e.g., `adr-0013-title.md`).
   - If **Ready**, applies edits to `constitution.md` or `acts/*.md`.
   - Updates provenance and prepares changelog entry.

4. **Validate** – Use `/validate` to check:
   - Consistency with existing text.
   - Alignment with Core Principles.
   - Completeness of documentation.

5. **Check-in** – Use `/check-in` to commit and push:
   - Adds changelog entry.
   - Creates commit message referencing ADR ID.
   - Pushes only after your confirmation.

### Creating an ADR

**You don't manually create ADRs**—they're created automatically when you discuss constitutional or structural topics. Simply start talking about:
- New rights or freedoms
- Governance mechanisms
- Policy frameworks
- Constitutional amendments
- Implementation details for acts

The system will create a draft ADR and continuously update it as the conversation evolves. When ready, finalize it with `/record`.

### Handling Substantial Work from Past Conversations

If you have substantial work from previous conversations (detailed frameworks, extensive research, etc.) that you want to incorporate:

1. **Create a reference document first** to preserve the full original work:
   - Save it in `log/ideas/[topic-name]/` (following the pattern of existing folders like `constitution-analysis/`, `justice/`, `prison-system/`)
   - Or as `log/ideas/[topic-name].md` if it's a single file
   - This preserves everything verbatim

2. **Then discuss it with AI** to create the ADR:
   - Reference the document: "Let's discuss the [Topic] in `log/ideas/[topic]/[file].md`"
   - Or paste key sections and discuss
   - The ADR will be created automatically as you discuss
   - The ADR captures the **decision/rationale** (structured, concise)
   - The reference doc preserves **all the details**

3. **Link them together**:
   - The ADR's "Links" section references the full document
   - The reference doc can mention which ADR(s) it relates to

This approach preserves all details while keeping ADRs focused and structured.

### Key Principles

- **Always records**: Every decision is documented in an ADR.
- **Never forgets**: Full history preserved in git and ADRs.
- **Never commits without you**: `/check-in` requires explicit confirmation.
- **Clean text**: Constitution and acts have no inline provenance markers.
- **Provenance via ADRs**: Traceability through ADRs, changelog, and provenance index.

## Contributing

Ideas, critiques, and comparative models are welcome.  
Pull requests should aim for clarity, minimalism, and testable governance mechanisms.

For detailed workflow rules, see `AGENTS.md` (primarily for AI assistants, but useful reference).

---

> “Never design for how people/politicians/corporations *should* behave—design so that even when they don’t, things still work.”