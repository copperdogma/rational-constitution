# ADR Draft — Surface the Constitutional Core in Article I
Timestamp: 2025-11-12 12:10

## Summary
Elevate the seven Constitutional Core tenets (currently in `AGENTS.md`) into `I. Foundations` as “Foundational Design Principles,” plus an “Interpretive Use” clause clarifying they guide interpretation and amendment but are not independently justiciable.

## Proposed Change
- Edit `constitution.md` Article I to add:
  - 5. Foundational Design Principles (7 items enumerating the Core)
  - 6. Interpretive Use (non-self-executing; ties to Ledger/audits and established processes)

Illustrative wording:
- 5. Foundational Design Principles
  1) Assume human nature — individuals and corporations act in self‑interest; design incentives accordingly.  
  2) Harness, don’t hope — channel ambition toward public good; avoid dark incentives.  
  3) Power diffused, checked — minimize concentration; ensure retroactive accountability.  
  4) Radical transparency — data, models, and actions open by default.  
  5) Democracy on outcomes — citizens vote for goals; technocrats execute; measure results.  
  6) Market where possible — price externalities; prefer performance competition.  
  7) Measurement over assertion — every mandate defines metrics and audit windows.  

- 6. Interpretive Use  
  In cases of ambiguity, institutions shall prefer readings consistent with 5(1)–5(7). These principles guide interpretation and amendment but are not, by themselves, grounds to invalidate law; compliance is ensured through the Civic Outcomes Ledger, audits, and processes defined by this Constitution and Acts.

## Rationale
- Lens for future decisions; transparency of values; consistent checks on new Acts/amendments.  
- Mirrors comparative practice (preambles/principles) while avoiding judicial overreach via explicit non‑self‑executing language.  
- Minimal textual diff; preserves current article numbering.

## Options (Justiciability)
- A. Interpretive only (recommended): guiding, not strike‑down grounds; aligns with Article IX limits.  
- B. Soft trigger: require “Core Compliance Statements” for major Acts in the Civic Outcomes Ledger; courts may cite but not void on Core alone.  
- C. Hard test (not recommended): would expand judicial power contrary to Article IX.

## Pros
- Clarity and coherence across institutions.  
- Stable anchor for amendments and Acts.  
- Minimal change surface; high interpretive value.

## Cons / Risks
- Too abstract if verbose; keep terse.  
- Potential judicial creep—mitigated by explicit non‑self‑executing clause.  
- Possible redundancy with Articles IV and X—requires tight phrasing.

## Core Alignment Check
1. Assume human nature — explicit.  
2. Harness, don’t hope — explicit.  
3. Power diffused, checked — explicit.  
4. Radical transparency — explicit; ties to Ledger.  
5. Democracy on outcomes — explicit.  
6. Market where possible — explicit; externality pricing.  
7. Measurement over assertion — explicit; mandates define metrics and audit windows.

## Open Questions
- Require a statutory “Core Compliance Statement” for major Acts, published in the Civic Outcomes Ledger?  
- Any phrasing tweaks to avoid overlap with `IV. Economic Order` and `X. Transparency`?  
- Placement: separate article vs. nested under `I. Foundations`?

## Links
- Source principles: `AGENTS.md` → “Constitutional Core (Decision Filter)”  
- Target sections: `constitution.md` → `I. Foundations` (new items 5–6)

## Next Steps
1) Socialize draft language; decide on Options A/B/C.  
2) If consensus → integrate text into `constitution.md`.  
3) Option B: draft a light‑weight protocol or Act section for “Core Compliance Statements.”  
4) Run `/validate`, then `/record`, then `/check-in` with updated changelog and provenance.

---

## Analysis and Refinement (2025‑11‑12 12:20)

### Do the seven principles capture the current Constitution and Acts?
- Assume human nature / Harness, don’t hope → Explicit in Preamble; reinforced by XIII (Balance of Fear and Ambition) and XIV (Continuity).
- Power diffused, checked → Article I (Foundations), II (institutions), III (integrity), IX (limits), XI (self‑correction).
- Radical transparency → Article X (Transparency and Public Data Integrity), VIII.4 (executive logs), III.4 (public contracts).
- Democracy on outcomes → II (elections/representation) + X (Civic Outcomes Ledger) + XI (review cycles); Acts publish metrics and audits.
- Market where possible (externality pricing, competition) → IV (Economic Order), IV.6 (Externality Principle), Acts (Externality Pricing Act), VI (Public Goods Principle via competitive allocation).
- Measurement over assertion (metrics, audits) → X (ledger), XI (sunset, audits), XII (incentive enforcement), Acts (verification, audits).

Conclusion: The seven match the existing architecture; some are already instantiated as operational articles (IV, X, XI), so the Core should be framed as interpretive rather than duplicative or self‑executing.

### Risk: Over‑prescription / Redundancy
- “Market where possible” overlaps Article IV; keep principle but soften to “prefer market mechanisms where they best achieve goals, with externality pricing.”
- “Radical transparency” overlaps Article X; keep principle, note narrowly tailored exceptions.
- “Democracy on outcomes” should avoid implying judicially enforceable management; anchor it as goal‑setting, with measurement and review done through the Ledger.
- “Assume human nature” and “Harness, don’t hope” can be merged into a single “Incentive compatibility by design” to reduce verbosity.

### Minimized alternatives (exact text proposals)

Option M‑7 (polished seven — least change)
1) Incentive compatibility — design for self‑interest; channel ambition toward public good.  
2) Distributed, accountable power — minimize concentration; ensure retroactive accountability and subsidiarity.  
3) Radical transparency — data, methods, and actions open by default, with narrow, reviewable exceptions.  
4) Outcomes democracy — citizens set goals; administration executes within law and metrics.  
5) Market mechanisms when fit — internalize externalities; prefer performance competition where effective.  
6) Measurement and audit — every mandate defines metrics, uncertainty bounds, and audit windows.  
7) Open adaptation — iterate via sunset, review, and public evidence.

Option M‑5 (compressed to five — recommended)
1) Incentive‑compatible design — assume self‑interest; harness it toward public good.  
2) Distributed accountability — power diffused with checks, subsidiarity, and retroactive liability.  
3) Transparency by default — open data, models, and actions; exceptions are narrow and time‑bound.  
4) Outcomes and evidence — citizens set goals; institutions measure, audit, and adapt.  
5) Markets with priced externalities — use competition and externality pricing where they best achieve goals.

Option M‑4 (core canon — most compact)
1) Incentive‑compatible architecture.  
2) Distributed and accountable power.  
3) Transparency by default.  
4) Outcomes measured and adapted.

Notes:
- Option M‑5 preserves the spirit of all seven, reduces redundancy, and reads cleanly alongside Articles IV, X, and XI.  
- Option M‑4 is elegant but risks being too high‑level for consistent interpretive use.

### Prescriptiveness adjustments (language tweaks)
- Replace “Market where possible” with “Markets with priced externalities — use competition and externality pricing where they best achieve goals,” to avoid categorical mandates.  
- Replace “technocrats execute” with “administration executes within law and metrics” to avoid value‑laden terminology and judicial creep.  
- Add “narrow and time‑bound” to transparency exceptions to align with X.2 periodic reviews.  
- Fold “Harness, don’t hope” into “Incentive‑compatible design.”

### Naming alternatives
- Constitutional Design Axioms (concise; signals foundational role)  
- Interpretive Canon (legal clarity; emphasizes guidance)  
- Principles of Constitutional Architecture (descriptive; neutral)  
- Governance Canon  
- Core Design Commitments  
- Structural Axioms  
- Foundational Governance Principles  
- Constitutional Ethos

Shortlist (recommended): Constitutional Design Axioms; Interpretive Canon; Principles of Constitutional Architecture.

### Recommendation
- Adopt Option M‑5 and label the section “Constitutional Design Axioms,” followed by the Interpretive Use clause (non‑self‑executing).  
- If stronger brevity is desired, consider Option M‑4 but supplement with commentary in ADR and Acts.

---

## Decision Update (2025‑11‑12 12:28)

Decision: Adopt Option M‑5, titled “Foundational Design Principles,” and integrate under `I. Foundations` with an Interpretive Use clause. Language choices confirmed:
- “Markets with priced externalities … where they best achieve goals.”
- “administration executes within law and metrics.”
- Transparency exceptions are “narrow and time‑bound.”

Integrated constitutional text:
- 5. Foundational Design Principles  
  1) Incentive‑compatible design — assume self‑interest; harness it toward public good.  
  2) Distributed accountability — power diffused with checks, subsidiarity, and retroactive liability.  
  3) Transparency by default — open data, models, and actions; exceptions are narrow and time‑bound.  
  4) Outcomes and evidence — citizens set goals; administration executes within law and metrics.  
  5) Markets with priced externalities — use competition and externality pricing where they best achieve goals.  

- 6. Interpretive Use  
  In cases of ambiguity, institutions shall prefer readings consistent with 5(1)–5(5). These principles guide interpretation and amendment but are not, by themselves, grounds to invalidate law; compliance is ensured through the Civic Outcomes Ledger, audits, and processes defined by this Constitution and Acts.

Status: Text integrated into `constitution.md`. Pending: `/converge` → `/record` → `/validate` → `/check-in`.

### Placement Adjustment (2025‑11‑12 12:35)
- Change: Move “Foundational Design Principles” and “Interpretive Use” from Article I into the Preamble as explicit sub‑sections, so the principles are the first substantive elements of the Constitution.  
- Rationale: Avoid “tacked‑on” feel; signal primacy; keep Article I focused on structural foundations that derive from the principles.  
- Impact: No renumbering of Articles; Article I retains items 1–4; duplication removed.

### Linkage Clarification (2025‑11‑12 12:39)
- Added a chapeau line under `I. Foundations`: “These Foundations implement the Foundational Design Principles stated in the Preamble.”  
- Purpose: Explicitly tie structure to principles without repeating the list; improves interpretability for courts and drafters.

---

## Convergence (2025‑11‑12 12:42)

### Current Proposal (≤10 bullets)
- Elevate “Foundational Design Principles” (Option M‑5) into the Preamble as the first explicit list.  
- Include “Interpretive Use” clause: guiding, non‑self‑executing; relies on Ledger/audits/processes.  
- Add chapeau under Article I linking Foundations to the Principles in the Preamble.  
- Language refinements: “markets with priced externalities … where they best achieve goals”; “administration executes within law and metrics”; transparency exceptions “narrow and time‑bound.”  
- Keep Article I focused on structural foundations (Rule of Law, separation of powers, open governance, subsidiarity).  
- Preserve article numbering; avoid redundancy.  
- Maintain judiciary limits per Article IX.

### Core Alignment (Foundational Design Principles)
1) Incentive‑compatible design — satisfied; embedded throughout incentives/articles XI–XII.  
2) Distributed accountability — satisfied; separation of powers, audits, retroactive liability.  
3) Transparency by default — satisfied; Article X and related provisions.  
4) Outcomes and evidence — satisfied; Ledger, audits, sunset/review cycles.  
5) Markets with priced externalities — satisfied; Article IV and Externality Pricing Act.

### Pros (≤6)
- Clear interpretive anchor at the very start of the Constitution.  
- Minimizes judicial creep via explicit non‑self‑executing clause.  
- Harmonizes with existing articles without renumbering.  
- Improves coherence for drafters, auditors, and courts.  
- Future‑proof: principles stable even as acts evolve.

### Cons (≤6)
- Principles remain abstract; application still relies on institutions and metrics.  
- Possible perceived redundancy with Articles IV and X (mitigated by concise phrasing).  
- Courts may still cite principles broadly; disciplined interpretive practice required.

### Outstanding Questions
1) Should major Acts include a published “Core Compliance Statement” in the Civic Outcomes Ledger (scope, verifier, threshold)?  
2) Any additional phrasing tweaks to further reduce overlap with `IV. Economic Order` and `X. Transparency`?

### Recommendation
Ready.  
Rationale: Text is integrated with placement optimized (Preamble), explicit interpretive limits, and structural linkage in Article I. Residual questions concern optional statutory process (compliance statements) and minor phrasing polish, which need not block recording.

---

## Core Compliance Statement (CCS) — Spec Proposal (2025‑11‑12 12:46)

### Purpose
Ensure every “major Act” explicitly demonstrates alignment with the Foundational Design Principles, with measurable commitments recorded in the Civic Outcomes Ledger.

### Scope / Triggers (“Major Act”)
An Act is “major” if any condition holds:
1) Fiscal impact: projected net budget impact ≥ 0.5% of the enacted national budget in any single fiscal year, or ≥ 1.0% cumulatively over a three‑year medium‑term framework.  
2) Compliance burden: estimated net compliance costs ≥ $250M/year or ≥ 5 million person‑hours/year nationwide.  
3) Institutional change: creates/abolishes a national‑level agency or reallocates constitutional powers among branches or independent bodies.  
4) Rights impact: places non‑trivial limitations on Rights and Liberties (Article VII) or creates new surveillance regimes.  
5) Metrics/ledger impact: adds, removes, or materially alters top‑level performance metrics, targets, or the Civic Outcomes Ledger schema.  
6) Externalities pricing: introduces or modifies nationwide externality pricing or market‑wide constraint systems.

### Verifiers (division of remit)
- Auditor‑General: certifies fiscal impact estimates, compliance‑cost methodology, and publication completeness.  
- Metrics Board: validates metrics design, data sources, uncertainty bounds, audit windows, and review cadence.  
- Citizen Panel by sortition (24–36 members): clarity, accessibility, and proportionality review; issues non‑binding report published alongside CCS.  
- When applicable: Externality Registry Board co‑signs sections related to externality definitions and price paths.

Minimum publication requirement: All verifier reports must be published in the Civic Outcomes Ledger at least 14 days before the final legislative vote.

### Workflow and Timing
1) Draft CCS published with first reading; 21‑day public comment window.  
2) Revised CCS published before second reading; verifier reviews run in parallel.  
3) Final CCS and verifier reports posted ≥14 days before final vote; machine‑readable (JSON) plus human‑readable.  
4) Post‑implementation updates: 12‑month initial update; annually thereafter until sunset/review.

### Acceptance Standard
Each verifier issues “meets standard”, “meets with reservations”, or “does not meet”. Final vote may proceed only if all verifier reports are published; reservations must be summarized in the Act’s rationale. “Does not meet” does not automatically bar passage but triggers mandatory reasons disclosure and a scheduled 12‑month remediation review in the Ledger.

### Required CCS Contents (concise schema)
- Alignment table: per‑principle rationale (incentive‑compatible design; distributed accountability; transparency; outcomes and evidence; markets with priced externalities).  
- Metrics: KPIs, definitions, data sources, uncertainty bounds, audit windows, publication cadence.  
- Externalities (if any): pricing approach, incidence (upstream/downstream), dividend/rebate rules, equity safeguards.  
- Power & subsidiarity: concentration risks, checks, retroactive liability, lowest‑effective‑level justification.  
- Transparency plan: open data/models, exceptions (narrow and time‑bound), redaction review schedule.  
- Incentives analysis: intended and dark‑pattern incentives; mitigation.  
- Fiscal & compliance: net budget impact, compliance‑cost methodology, distributional/equity impacts.  
- Sunset/review: expiry or formal review schedule; red‑team plan.  
- Implementation risks and fail‑safes.  
- Sign‑offs and contacts; Ledger URLs; machine‑readable bundle.

### Enforcement
- Procedural prerequisite: publication of Final CCS and verifier reports (≥14 days pre‑vote).  
- Post‑enactment: missed update deadlines must be logged in the Ledger; Auditor‑General schedules a public remedial hearing within 90 days.  
- Courts may not invalidate laws solely for CCS defects but may order cure and disclosure.

### Notes
- Implement via a short General Governance Process Act; keep the Constitution lean.  
- Thresholds are adjustable by supermajority statute as measurement improves.

### Simplified Constitutional Directive (2025‑11‑12 12:52)
- Decision: Keep the Constitution lean. Rather than embedding CCS process/thresholds, add a single directive clarifying adherence and interpretation.  
- Implemented text (Preamble → Interpretive Use):  
  “Acts and amendments shall be drafted to adhere to these Principles and interpreted to further them, consistent with Article IX.”

### Phrasing Refinements to Reduce Overlap (2025‑11‑12 12:54)
- Principle 3 updated: “Transparency by default — public information and decision‑making rationales are open by default; exceptions are narrow and time‑bound.”  
- Principle 5 updated: “Market test with priced externalities — use competitive mechanisms and price externalities where they best achieve goals.”  
- Rationale: Keep principles high‑level; leave implementation specifics to Articles IV and X and Acts.

---

## Changed Sections (for /record)
- File: `constitution.md`
  - Preamble: add “Foundational Design Principles” (M‑5) and “Interpretive Use”.
  - I. Foundations: add chapeau line linking to Principles in Preamble.

## ADR Header Schema (example for finals)
```yaml
adr:
  id: TBD
  title: Surface the Foundational Design Principles in the Preamble
  status: Accepted
  date: 2025-11-12
  changed_sections:
    - file: constitution.md
      sections:
        - "Preamble: Foundational Design Principles; Interpretive Use"
        - "I. Foundations: chapeau linkage to Principles"
```


