# Constitution Analysis

This folder contains the analysis of eight real-world constitutions to analyze them as follows:

1. Constitutional Primitives
2. Analysis of Primitives and how well they work in the real world

The eight conisttutions are here: /references/constitutions/

The initial analysis was done with GPT5.1 guiding the prompts for NotebookLM.

## Methodology

This is the process used:

1. Created new NotebookLM notebook: https://notebooklm.google.com/notebook/80d714a3-e1d0-4779-95b4-adb9a8279a27

2. Explained what we want to do to GPT5.1 which created the "Consitutional Comparison Categories" and three prompts, output below.

3. Got GPT5.1 to identify the most successful conistutitons in the world, ensuring not too much overlap in basic approach.

4. Got GPT5.1 to find a copy of each, which I downloaded and uploaded into NotebookLM as sources. NotebookLM actually has the ability to do this and I should have used it and saved myself 15 mins.

5. Added GPT5.1's "Consitutional Comparison Categories" to NotebookLM as a source.

6. Ran each of the three prompts GPT5.1 gave me (detailed below) and saved the outputs in NotebookLM as sources, named:
   - 01_Constitution_Outlines
   - 02_Comparative_Matrix
   - 03_Common_Patterns_and_Outliers
   I've saved the full outputs in this folder under the same names.


## Prompts

Here are clean, explicit, schema-aligned versions of Prompts 1–3.
They assume you have a fresh NotebookLM notebook and have uploaded:
	•	The eight constitutions
	•	Your “Constitutional Comparison Categories” schema
	•	Your axioms doc (optional but recommended)
	•	Your property/privacy framework (optional)

These prompts fix all earlier issues:
✔ explicitly reference the schema
✔ force NotebookLM to align its internal model to your categories
✔ avoid drift
✔ produce clean, structured, comparable outputs

⸻

Prompt 1 — Constitution Ingestion & Alignment

Purpose: Force NotebookLM to internalize the schema before doing any analysis.

You have access to a set of eight constitutions and one document titled
“Constitutional Comparison Categories.” This categories document defines the
required structure for all future analysis.

First, read and internalize the “Constitutional Comparison Categories.”
This schema is the authoritative organizing framework.

Now, for each constitution uploaded, produce a clean structural outline that
maps ONLY to the categories in the schema, using the same section headings,
ordering, and terminology.

Do NOT summarize yet. Do NOT analyze. Do NOT compare.

Your output per constitution should be a bare structural mapping such as:

- Sovereignty & Foundational Principles → [list applicable clauses]
- Separation of Powers → [list applicable clauses]
- Rights & Liberties Framework → [list applicable clauses]
- Justice System Architecture → [list applicable clauses]
- Electoral System & Democratic Mechanics → [list applicable clauses]
- Executive Function & Constraints → [list applicable clauses]
- Legislative Function & Constraints → [list applicable clauses]
- Judiciary Structure & Constraints → [list applicable clauses]
- Federalism / Unitary Structure → [list applicable clauses]
- Amendment Mechanisms → [list applicable clauses]
- Military, Emergency Powers, & National Security → [list applicable clauses]
- Administrative State & Public Service → [list applicable clauses]
- Constitutional Review / Guardianship Mechanisms → [list applicable clauses]
- Local Autonomy & Subsidiarity → [list applicable clauses]
- Fiscal & Budgetary Rules → [list applicable clauses]
- Digital Governance / Technology Provisions → [list applicable clauses] (if any)
- Cultural, Indigenous, or Historic Provisions → [list applicable clauses]
- Transitional or Founding Clauses → [list applicable clauses]

If a constitution does not address a category, explicitly write:
“Not addressed.”

If a constitution uses different terminology, normalize it.

Do NOT add interpretation. Do NOT generalize. Extract only what is present.


⸻

Prompt 2 — Per-Category Comparison

Purpose: Produce one comparison per category, across all constitutions.

Using ONLY the structured outlines you created and the schema, perform a
cross-constitution comparison *category by category*.

For each category in the “Constitutional Comparison Categories,” produce:

1. A neutral description of how each constitution implements that category.
2. Key common patterns across the constitutions.
3. Key divergences.
4. Any notable omissions.
5. One-sentence functional insight: “What this category is doing in each system.”

Do NOT evaluate or praise. Do NOT invoke international bodies or norms.
Stay strictly descriptive and function-oriented.
Avoid moral or political judgment.

Your output must be formatted as:

## [Category Name]
### Implementation by Constitution
- Constitution A → …
- Constitution B → …
…

### Common Patterns
- …

### Divergences
- …

### Omissions
- …

### Functional Insight
- …

Repeat for EVERY category in the schema.


⸻

Prompt 3 — Deep Structural Distillation for Design

Purpose: Extract design primitives and governance patterns that can be reused.

Now synthesize all of the category-by-category comparisons into a set of
“constitutional design primitives.”

A design primitive is a fundamental governance mechanism that can be reused
independently of its specific implementation. Examples include:
- bicameralism
- judicial review
- independent central bank
- proportional representation
- ombudsman systems
- bill of rights models
- parliamentary fusion vs separation-of-powers models
- fiscal restraint mechanisms
- emergency-power limitations

Your goals:

1. Identify all recurring structural patterns across the eight constitutions.
2. Identify all powerful but uncommon mechanisms (e.g., NZ’s flexibility,
   Estonia’s digital identity layer).
3. For each pattern or mechanism, describe:
   - The core purpose it serves.
   - The conditions where it performs best.
   - Known failure modes (if any).
   - What prerequisites it assumes (e.g., digital infrastructure, political culture).
4. Output the result as modular “building blocks” a new constitution could adopt.

DO NOT recommend which model is "best."
DO NOT combine patterns yet.
Stay purely analytical: identify, extract, and describe the building blocks.


⸻

## Prompts 4-6: Constitutional Skeleton Design Workflow

After completing Prompts 1-3 in NotebookLM, the next phase involves designing the constitutional skeleton using AI chat sessions. This workflow uses separate chats for each stage to avoid context truncation.

### Workflow Overview

Here's the clean sequence to follow:

**Step 0 — Start a new chat**
Title it something like:
"Constitution Project — Constitutional Skeleton (Prompt 4)"

⸻

**Starter Message for New Chat — Constitution Project (Step 4)**

I'm starting Step 4 of a multi-step constitutional design workflow.
This chat should focus only on Step 4.

You have long-term memory of my philosophical framework, property/privacy axioms, prison model, and meta-preferences. Use that memory when relevant, but do NOT assume you know the details of the constitutional comparison: I will paste all relevant materials below.

**Your Role**

You are my analytical collaborator.
Your task is to read the documents I provide in full and then run Prompt 4, which will come after the pasted materials.

Do NOT start analyzing until I explicitly send:
"RUN PROMPT 4"

**Materials I Will Paste Next**
1. Comparative extracts from eight national constitutions, generated by NotebookLM.
2. My first-principles documents:
   • Axioms
   • Property/Privacy Framework
   • Foundational rights structure
3. The "Constitutional Comparison Categories" schema.

Once all materials are pasted, I will write: RUN PROMPT 4.
Then you execute Prompt 4 exactly.

Do not respond yet.

Wait for all documents and my explicit instruction.
Only acknowledge receipt of this starter message.

**Step 1 — Paste the following into the new chat:**
• The NotebookLM comparative outputs
(all of them, including the distilled categories and extracted clauses)

Do NOT paste your penal system or corrections system—they are separate from the constitution.

**Step 2 — Paste your first-principles documents:**
• Axioms
• Property/Privacy Framework
• Any other foundational docs needed for constitutional design

**Step 3 — Paste Prompt 4 exactly as written**
Then hit enter.

**After Prompt 4 completes**

You'll open two MORE brand-new chats:
• Chat 2 for Prompt 5 (stress test)
• Chat 3 for Prompt 6 (red-team + hardened skeleton)

Each will be cleaner, more predictable, and easier to manage.

**Why separate chats for each stage?**

Because each stage is:
• long
• dense
• contains dozens of cross-references
• requires the model to hold its entire output in working memory
• needs full context window availability

Putting all three stages into one chat risks catastrophic context truncation.

**Summary (very short)**
• YES: Start a new chat
• NO: Don't continue here
• YES: The model will still use your saved memory
• YES: Do one chat per step (4, 5, 6)
• Paste the NotebookLM outputs + foundational docs at the start of step 4

⸻