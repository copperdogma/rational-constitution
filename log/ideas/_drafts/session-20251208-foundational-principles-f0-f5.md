# ADR Draft: Foundational Principles (F0-F5) — Human Nature and Structural Principles

**Status:** Draft  
**Date:** 2025-12-08  
**Topic:** Refined foundational principles (F0-F5) for human nature assumptions and structural design

---

## Context

Foundations: Human Nature and Structural Principles
from: https://chatgpt.com/c/691dea36-d0a0-8330-8d75-20daafa113c8

F0 — Humans as They Are
This order is designed for humans as they are, not as they ought to be. It assumes that agents:
	•	favour their own welfare and that of close circles,
	•	will exploit advantages where possible,
	•	are cognitively limited and use heuristics,
	•	are sensitive to perceived unfairness and visible double standards,
	•	and naturally form coalitions and hierarchies that tend to entrench power.

Institutions must therefore rely on rules, incentives, and transparency, not on widespread altruism or exceptional virtue.

⸻

F1 — Self-Interest, Asymmetries, and Incentives

Premise.
Agents often prioritize themselves and their allies, and will exploit structural or informational asymmetries when doing so is low-risk and beneficial.

Principle.
The system shall:
	•	avoid institutional designs that depend on impartial concern for strangers;
	•	minimize structural loopholes and low-risk avenues for rent-seeking; and
	•	steer behaviour primarily through incentive and constraint design rather than moral exhortation.

⸻

F2 — Bounded Cognition and Rule Legibility

Premise.
Agents have limited attention and understanding and operate under uncertainty.

Principle.
Core constitutional rights, duties, and processes must be expressible in terms reasonably understandable by laypersons. The enjoyment of basic rights must not depend on mastery of obscure or needlessly complex rules.

⸻

F3 — Fairness, Relative Comparison, and Symmetric Rules

Premise.
Agents are highly sensitive to perceived unfairness, especially when:
	•	rules or their enforcement visibly differ between groups; or
	•	some gain by violating what is understood as the shared social contract.
In an open-information world, agents also compare their situation with visible alternative systems; persistent underperformance and visible rule-level bias are experienced as systemic unfairness.

Principle.
Accordingly:
	•	Legal and regulatory rules shall be general and symmetric: for agents in the same relevant position following the same plan of action, the law shall not distinguish between them in rights, obligations, or access to public processes.
	•	Where harmful behaviour cannot be positively channeled, it must at least be priced or punished in a way that keeps “playing by the rules” rational and emotionally acceptable.

⸻

F4 — Transparency of Rules, Outcomes, and External Conditions

Premise.
Fairness judgments and system legitimacy depend on agents’ ability to see how rules operate and how outcomes compare, both internally and against other systems.

Principle.
	•	All constitutional rules, ordinary laws, and administrative procedures shall be public.
	•	Aggregated information about key economic, social, and civic outcomes, including reasonable comparisons with peer jurisdictions, shall be collected and published by independent statistical bodies.
	•	Public authorities may not suppress or distort such information for the purpose of preserving their own reputation, authority, or convenience, except for narrow, public, and reviewable security exceptions defined by law.

⸻

F5 — Coalitions, Hierarchies, and Collective Power

Premise.
Agents naturally form coalitions and hierarchies; holders of concentrated power tend to preserve and expand it.

Principle.
	•	Agents are free to form associations, parties, unions, corporations, and other collective bodies to coordinate their actions and voice.
	•	Such bodies may exercise only those powers available in principle to the same number of agents acting individually under general rules.
	•	No office, organization, or class of person may be granted permanent legal exemptions, special economic privileges, or procedural advantages that are unavailable in principle to other agents similarly situated.

⸻

That’s the “everything important, no redundancy” version:
	•	F0 is the Madison-style “men are not angels” meta.
	•	F1–F5 compress your HNPs, the fairness/comparison theory, symmetric rules, no castes, and radical transparency into five clean clauses.

The ladder (Design → Channel → Price → Hard Constraint) and policy-judge mandate can sit in a separate "Policy Implementation Principles" section without needing any of this repeated.

---

## Decision

[Pending decision: Should F0-F5 replace, supplement, or inform the current Foundational Design Principles in the Preamble?]

**Key Questions:**
- Should F0 (meta-assumption) be made explicit in the Preamble or remain implicit?
- Should F2 (Bounded Cognition) and F3 (Fairness/Symmetric Rules) be added as explicit principles?
- Should the current M-5 principles be restructured to align with F0-F5?
- Or should F0-F5 serve as the underlying rationale/commentary while keeping M-5 as the operational principles?

---

## Rationale

**F0-F5 Strengths:**
- **F0** makes the human nature assumption explicit (currently implicit in Preamble opening and ADR-0001)
- **F2** (Bounded Cognition) addresses a gap: current principles don't explicitly require rule legibility for laypersons
- **F3** (Fairness/Symmetric Rules) makes fairness sensitivity explicit, which is currently implied but not stated
- **F1, F4, F5** align well with existing principles but are more structured (Premise + Principle format)
- The Premise/Principle structure provides clearer reasoning chains

**Comparison with Current M-5:**
- Current: "Incentive-compatible design" → maps to F1
- Current: "Distributed accountability" → maps to F5
- Current: "Transparency by default" → maps to F4
- Current: "Outcomes and evidence" → not explicitly in F0-F5 (but implied in F4's outcome comparisons)
- Current: "Market test with priced externalities" → not in F0-F5 (note says this belongs in "Policy Implementation Principles")

**Gaps/Additions:**
- F2 (Bounded Cognition) is new and valuable
- F3 (Fairness/Symmetric Rules) is new and valuable
- F0 makes human nature assumption explicit (currently only in Preamble opening line)

---

## Alternatives Considered

1. **Replace M-5 with F0-F5** — More comprehensive, but loses "Outcomes and evidence" and "Market test" as explicit principles
2. **Keep M-5, add F2 and F3** — Incremental, but doesn't address F0's meta-assumption or F1/F4/F5 restructuring
3. **Hybrid: F0 as meta, F1-F5 as principles** — Clean structure, but need to decide where "Outcomes/evidence" and "Market test" go
4. **F0-F5 as underlying rationale, keep M-5 as operational** — Preserves current structure while enriching understanding
5. **Restructure: F0 + expanded set** — Combine F0-F5 with outcomes/evidence and market test into unified set

---

## Core Alignment

**Constitutional Core Evaluation:**

1. ✅ **Assume human nature** — F0 and F1 explicitly address this
2. ✅ **Harness, don't hope** — F1's "steer behaviour primarily through incentive and constraint design" aligns
3. ✅ **Power diffused, checked** — F5 addresses this directly
4. ✅ **Radical transparency** — F4 addresses this
5. ⚠️ **Democracy on outcomes** — Not explicit in F0-F5 (but F4 mentions outcome comparisons)
6. ⚠️ **Market where possible** — Explicitly excluded from F0-F5 per note (belongs in "Policy Implementation Principles")
7. ⚠️ **Measurement over assertion** — Not explicit in F0-F5 (but implied in F4's outcome tracking)

**Assessment:** F0-F5 strongly align with Core tenets 1-4, but don't explicitly cover tenets 5-7. This suggests F0-F5 may be foundational assumptions/principles, while tenets 5-7 belong in operational/implementation principles.

---

## Consequences

**If adopted as replacement for M-5:**
- More explicit human nature foundation (F0)
- Adds bounded cognition requirement (F2) — important for accessibility
- Adds fairness/symmetric rules requirement (F3) — important for legitimacy
- May need to preserve "Outcomes/evidence" and "Market test" elsewhere (e.g., in Article I or separate section)

**If adopted as supplement:**
- Enriches understanding without disrupting current structure
- Could inform future amendments or interpretations
- May create redundancy if not carefully integrated

**If adopted as underlying rationale:**
- Provides deeper foundation for M-5
- Could be referenced in ADRs and commentary
- Keeps Preamble concise while preserving full reasoning

---

## Changed Sections

[To be determined based on decision above]

**Potential changes:**
- `constitution.md` Preamble: May replace or supplement Foundational Design Principles
- May require updates to Article I Foundations if F2 (bounded cognition) or F3 (symmetric rules) need explicit implementation

---

## Links

- Related: ADR-0010 (Foundational Design Principles in the Preamble)
- Source: `log/to-do.md` (lines 124-206)

---

## Notes

**Relationship to Existing ADRs:**
- **ADR-0001** (Human Nature Assumption) — F0 makes this explicit in constitutional text
- **ADR-0010** (Foundational Design Principles) — F0-F5 may refine or replace the M-5 principles adopted there
- The note mentions "Policy Implementation Principles" as a separate section for the ladder (Design → Channel → Price → Hard Constraint) and policy-judge mandate

**Structural Observations:**
- F0-F5 use a Premise/Principle structure that provides clear reasoning chains
- F0 serves as meta-assumption; F1-F5 are operational principles
- The set is described as "everything important, no redundancy" — a compressed version of existing HNPs, fairness theory, symmetric rules, no castes, and radical transparency

**Integration Considerations:**
- Current Preamble opening line already states human nature assumption ("humans act from self-interest, that power seeks concentration")
- F0 would make this more explicit and structured
- F2 and F3 add new dimensions not currently explicit in the Constitution
- Need to determine if "Outcomes/evidence" and "Market test" principles should be preserved alongside F0-F5 or moved to implementation section

**Source:** External conversation (ChatGPT) that refined and compressed existing principles into this structured format.

---

## Open Questions

1. **World modelling assumptions**: What assumptions should we include? Basic rights, human nature/psychology, incentives... I think there are three domains of human nature we need to address:
   - Needs (address/protect); Low Maslow's hierarchy? Agency, rights, etc.
   - Wants (understand these): Mid-high Maslow's hierarchy? Fairness, etc.
   - Negative traits (defend against): Greed, status/power-seeking, tribalism, etc.

2. **Rights framework sufficiency**: So it's important to protect the rights of citizens from the state. We also need to work on protecting the rights of citizens from other citizens. I like the core tenet of "your rights end where another's begin" because it takes care of most of it. Is that sufficient?

