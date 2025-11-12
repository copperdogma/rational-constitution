# Validate Changes

Thoroughly analyze what was done and how it compares to the original instructions and our constitutional framework. Report results back in chat (not as a file edit).

## 1. Review Changes
```bash
git diff --name-only
git diff --stat
git log --oneline -5

2. Examine Modified Files
	•	Open each changed file and review contents.
	•	Compare changes against:
	•	the approved ADR(s)
	•	requirements in AGENTS.md (standards, core tenets)
	•	previous version of the document (if applicable)
	•	Check for completeness, style, formatting, numbering consistency.
	•	Provenance policy compliance:
		- No inline provenance markers in governed texts (`constitution.md`, `acts/*.md`).
		- ADR includes “Changed Sections” mapping files/sections.
		- Changelog entry prepared (not inserted) referencing ADR(s).
		- `log/provenance.md` updated/generated at `/record` with planned commit timestamp + subject (no SHA).
	•	Check-in readiness:
		- Only intended files (constitution/acts/ADRs/tooling + changelog) will be staged.
		- No unintended files are present; list and confirm intended set.

3. Score Each Requirement / Tenet

Use scoring for each key item addressed by the change. Typical grades:
	•	A: Fully implemented, high quality, exceeds expectations
	•	B: Implemented well, minor improvements possible
	•	C: Implemented but has notable issues
	•	D: Partial implementation, significant gaps
	•	F: Not implemented or incorrect

For each requirement or core tenet, provide:
	•	Requirement: [Description]
	•	Status: [Implemented / Partially / Not]
	•	Grade: [A/B/C/D/F]
	•	Evidence: [Files/lines showing it]
	•	Quality: [Assessment of implementation]
	•	Improvement Suggestions: [If grade < A]

4. Overall Assessment
	•	Core Compliance: For each constitutional tenet (Assume human nature, Power diffused…, etc) state Pass/Fail with one-liner justification.
	•	Metrics Defined: Confirm “Measurement over assertion” – did the change define metrics/audit window where required?
	•	Risks & Reversibility: Identify any new risk or coupling; note rollback path.
	•	Outstanding Questions: List any open issues now added to log/open-questions.md, with IDs.

5. Final Verdict

Give one of:
	•	✅ Ready – All requirements met, core compliance ok, minimal risks.
	•	⚠️ Needs Work – Some gaps, must fix those before /check-in.
	•	❌ Not Ready – Major issues, apply /record and revise.

Output

Respond with:
	•	Summary of changed files and high-level changes (5-10 bullets)
	•	Scoring table of top requirements or tenets
	•	Overall verdict + next steps

---

If you like this, I’ll update the repo with it.