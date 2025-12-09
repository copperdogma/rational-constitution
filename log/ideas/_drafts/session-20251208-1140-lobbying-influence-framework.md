# ADR Draft: Lobbying and Influence Framework

**Status:** Draft  
**Date:** 2025-12-08  
**Topic:** Constitutional framework for handling lobbying and corporate influence
**Source**: https://chatgpt.com/c/693708d4-f0a0-8328-8f0c-69efda972583

---

## Context

In a libertarian, outcome-driven constitutional system, the question of how to handle lobbying and corporate influence is critical. Traditional systems are vulnerable to regulatory capture, backroom deals, and asymmetric information advantages. This ADR establishes a framework that:

1. Does not prohibit lobbying (preserving free speech)
2. Removes structural leverage points that make lobbying dangerous
3. Ensures all influence is transparent, contestable, and empirically testable

The framework aligns with the Constitutional Core principles, particularly:
- **Radical transparency** (Principle 4)
- **Power diffused, checked** (Principle 3)
- **Measurement over assertion** (Principle 7)
- **Harness, don't hope** (Principle 2)

---

## Decision

Establish a comprehensive constitutional framework for lobbying and influence that:

1. **Allows persuasion lobbying** but makes it structurally weak through outcome-based voting
2. **Mandates symmetric access and transparency by default** for all policymaker interactions
3. **Creates a public data commons** (Department of Data) as the default ground truth
4. **Requires transparent private data frameworks** when private data is submitted
5. **Implements basket-of-indicators requirements** to prevent metric gaming
6. **Establishes periodic metric audits** to detect gaming and drift
7. **Enforces threshold integrity clauses** preventing proprietary data from driving thresholds
8. **Maintains an influence ledger** logging all policymaker interactions
9. **Constitutionalizes open-by-default principle** for all non-personal government information

---

## Rationale

### Core Strategy

Rather than banning lobbying (which would violate free speech principles), the framework removes the structural leverage points that make lobbying dangerous:

- **No law-writing legislatures to buy** — citizens vote on outcomes, not policies
- **No regulatory carveouts to slip in** — policies are executed by technocrats within outcome mandates
- **No opaque agencies to capture** — all data, metrics, and processes are transparent
- **No single-point metrics to game** — basket-of-indicators requirement prevents manipulation
- **No private thresholds** — all thresholds must be explainable and verifiable
- **No secret influence channels** — influence ledger makes all interactions public
- **No undisclosed data inputs** — public data commons is the default ground truth

### Key Mechanisms

1. **Outcome-Based Voting**: Because citizens vote on outcomes rather than policies, persuasion can only distort priorities, not create special privileges. Empirical measurement and citizen experience create self-correcting feedback loops.

2. **Transparency by Default**: Any information shared with policymakers becomes part of the public record. This eliminates backroom influence, asymmetric information flow, and quiet capture. Corporations must assume everything they say will be visible.

3. **Public Data Commons**: The biggest capture vector is data control. A public data infrastructure ensures independent measurement, verifiable thresholds, transparent metrics, and reproducible results. Corporations may contribute data, but public data remains the backbone.

4. **Transparent Private Data**: If private data is submitted, it must be either published in aggregated/auditable form or independently verified by a neutral third party. This solves the "truth is expensive, verification rare" problem while maintaining libertarian principles (withholding data is allowed but strategically costly).

5. **Basket-of-Indicators**: No major policy domain can be evaluated on a single scalar metric. This is the strongest anti-Goodhart safeguard — no single metric can be gamed without being contradicted by others.

6. **Periodic Metric Audits**: Metrics lose validity over time. Regular audits refresh measurement tools, reduce manipulative optimization, and ensure metrics still measure what citizens actually care about.

7. **Threshold Integrity**: No thresholds may rely primarily on proprietary or unverifiable data. All thresholds must be explainable in plain language and supported by public or independently verifiable metrics.

8. **Influence Ledger**: All policymaker meetings, communications, and submissions are logged publicly (who, when, topic, whether data was exchanged). This makes influence observable, discourages bad behavior, and eliminates asymmetric access advantages.

9. **Open by Default**: All non-personal government information is open by default. Exceptions require narrow justification and periodic review. Transparency becomes the immune system of the governance model.

---

## Alternatives Considered

1. **Ban lobbying entirely** — Rejected: violates free speech principles and is impractical to enforce. Would drive influence underground.

2. **Heavy regulation of lobbying** — Rejected: creates regulatory capture opportunities and enforcement complexity. Still allows structural leverage points.

3. **Status quo (traditional disclosure requirements)** — Rejected: insufficient. Disclosure alone doesn't remove leverage points or ensure symmetric access.

4. **Structural approach (chosen)** — Removes leverage points rather than regulating behavior. Aligns with libertarian principles while ensuring influence is transparent and contestable.

---

## Consequences

### Positive

- **Preserves free speech**: Persuasion lobbying remains legal and protected
- **Eliminates structural leverage**: No backroom deals, regulatory carveouts, or opaque capture
- **Creates public goods**: Transparency and public data become shared resources
- **Self-correcting**: Bad policies fail empirically; manipulation is detectable
- **Strengthens trust**: Open processes build citizen confidence
- **Enables competition**: Fair marketplace of ideas with symmetric access

### Implementation Requirements

- **Constitutional amendments**: Add explicit transparency and data commons provisions
- **Legislative acts**: Establish Department of Data, influence ledger system, metric audit processes
- **Infrastructure**: Build public data infrastructure, influence logging systems, audit mechanisms
- **Cultural shift**: Policymakers and corporations must adapt to open-by-default environment

### Risks and Mitigations

- **Risk**: Corporations may withhold helpful data
  - **Mitigation**: Allowed by libertarian principles, but becomes strategically costly and non-influential

- **Risk**: Metric audits may be captured
  - **Mitigation**: Independent third parties, public methods, citizen oversight

- **Risk**: Influence ledger may be gamed with volume
  - **Mitigation**: Quality matters more than quantity; public scrutiny and watchdog detection

- **Risk**: Implementation complexity
  - **Mitigation**: Phased rollout, clear standards, automated systems where possible

---

## Constitutional Core Compliance

### ✅ Assume human nature
- Framework assumes corporations act in self-interest and will attempt to influence policy
- Design channels this toward transparent, contestable persuasion rather than hidden capture

### ✅ Harness, don't hope
- Doesn't rely on corporate virtue or self-restraint
- Structural design removes leverage points and makes bad behavior detectable

### ✅ Power diffused, checked
- No single point of capture (no law-writing legislatures, no opaque agencies)
- Multiple oversight mechanisms (audits, citizen watchdogs, influence ledger)

### ✅ Radical transparency
- Open-by-default principle constitutionalized
- All influence, data, and metrics are public
- Transparency becomes the immune system

### ✅ Democracy on outcomes
- Citizens vote on outcomes, not policies
- Persuasion can only shape priorities, not create special privileges
- Empirical measurement ensures accountability

### ✅ Market where possible
- Transparent marketplace of ideas
- Symmetric access ensures fair competition
- Public data commons prevents information monopolies

### ✅ Measurement over assertion
- Basket-of-indicators prevents gaming
- Periodic audits ensure metric validity
- Public data is default ground truth
- All thresholds must be explainable and verifiable

---

## Changed Sections

*To be determined upon finalization. Potential sections:*

- **Article II (Representation and Elections)**: Expand lobbying disclosure requirements
- **Article X (Transparency and Public Data Integrity)**: Add explicit influence ledger, public data commons, basket-of-indicators, metric audit requirements
- **New Article or Section**: Threshold integrity clause, transparent private data framework
- **Acts**: May require new Act establishing Department of Data and influence ledger infrastructure

---

## Links

- Related to ADR-0001 (Human Nature Assumption) — assumes self-interest
- Related to ADR-0004 (Externality Pricing) — transparent data and metrics
- Related to ADR-0006 (Transparency Ledger) — influence ledger extends transparency
- Related to ADR-0007 (Mandate vs Politician) — outcome-based voting removes policy leverage
- Related to ADR-0010 (Foundational Design Principles) — transparency and measurement principles
- Constitution Article X (Transparency and Public Data Integrity)
- Constitution Article II.5 (Lobbying Disclosure)

---

## Open Questions

1. What specific technical infrastructure is needed for the influence ledger? (Real-time logging? Searchable database? API access?)

2. How to define "major policy domain" for basket-of-indicators requirement? (Thresholds? Scope?)

3. What is the audit frequency for periodic metric audits? (Annual? Biennial? Domain-specific?)

4. How to handle national security exceptions to open-by-default? (Narrow definition? Review process?)

5. What constitutes "independently verifiable" for private data submissions? (Third-party standards? Certification process?)

6. How to prevent influence ledger from becoming a volume game? (Quality metrics? Relevance filters?)

7. **Goodhart's Law**: Take Goodhart's Law's into account for policymakers/data collection bureau. How do we ensure that the basket-of-indicators and metric audit mechanisms prevent metric gaming and ensure metrics continue to measure what citizens actually care about?

8. **Citizen bounty hunters**: Can we incentivize citizens to report corruption or fraud? We already outlined a way they can compete with policymakers for the best policy solution that suits the outcome. How can we extend this to corruption detection and reporting?

9. **Petition/complaint mechanism**: "Petition" -- this gets interesting when there are no politicians... We have a kickstarter system of policies. Who addresses complaints? That's feedback into the metrics of dissatisfaction with some aspect, isn't it? We already have a channel for that. However, that also opens it to the tyranny of the majority. Complaints about no wheelchair access are ignored if the satisfaction metric among people who don't need them is high enough. How do we ensure minority concerns are heard and addressed in a system without politicians?

---

## Notes

This framework represents a structural approach to influence management that aligns with libertarian principles while ensuring robust safeguards. The key insight is that removing leverage points is more effective than regulating behavior.

The framework is designed to be self-reinforcing: transparency enables detection, detection enables correction, correction maintains trust, trust strengthens the system.

