# ADR Draft: Bill of Rights Architecture (Session)

Status: Draft (Active)  
Date: 2025-11-12  
Topic: Minimal, elegant, robust Bill of Rights  
Authors: cam (with AI assistance)  

---

## Summary
Design a principled, minimal Bill of Rights (BoR) that is durable across eras, maximally speech-protective with narrowly tailored carve‑outs, rigorously enforceable, and hard to erode. This ADR gathers requirements, comparative lessons, proposed architecture, tradeoffs, and open questions for iterative discussion. No edits to governed texts will be made until explicitly decided.

---

## Initial Intent and Requirements (from notes)
- Add a Bill of Rights—a core constitutional section that explicitly enumerates individual rights and freedoms.
- Include clear amendment mechanics—possibly Swiss-style double-majority (citizens + sub-units) to evolve rights while preventing populist swings.
- Rights should be explicit, rigid, and speech‑protective, closer to the U.S. First Amendment model.
- Only allow narrow, objective carve‑outs (incitement to imminent violence, true threats, defamation).
- Prevent subjective limits (e.g., “offense,” “emotional harm”) from restricting speech.
- Courts interpret through the Constitutional Core; power checks trump convenience.
- Consider graded penalties that restrict specific rights (e.g., travel, vote, bear arms) rather than default imprisonment, making justice proportional and rights-aware.

---

## Context
The current Constitution has a succinct rights section (Article VII). We seek an explicit, structured BoR that: (1) enumerates core negative liberties; (2) defines a disciplined limitation doctrine; (3) specifies robust remedies and standing; (4) embeds strong amendment/entrenchment rules; and (5) clarifies treatment in emergencies, horizontality, and interpretation—while remaining concise and future-proof.

---

## Comparative Survey and Lessons
- United States Bill of Rights: Primarily negative restraints on government; exceptionally speech‑protective model with narrow carve‑outs (e.g., incitement, true threats, obscenity), content‑neutral time/place/manner controls. Judicial doctrines include strict scrutiny, viewpoint neutrality, prior restraint bans, and high defamation thresholds for public officials (actual malice).  
  - Incitement standard: “imminent lawless action” and likelihood (Brandenburg v. Ohio, 1969).  
  - True threats: prohibition on serious expressions of intent to commit unlawful violence (e.g., Virginia v. Black, 2003).  
  - Defamation (public officials/figures): “actual malice” standard (New York Times Co. v. Sullivan, 1964).
- Canadian Charter of Rights and Freedoms: Enumerated rights plus a general limitation clause (s.1) with the Oakes proportionality test (pressing objective, rational connection, minimal impairment, proportionality of effects); s.33 notwithstanding clause permits legislative override for some rights on a time‑limited basis, with political accountability costs.
- European Convention on Human Rights: Enumerated rights with structured limitation clauses requiring that interferences be “prescribed by law,” pursue legitimate aims, and be “necessary in a democratic society.” The “margin of appreciation” affords states some flexibility subject to Strasbourg review.
- German Basic Law (Grundgesetz): Robust “eternity clause” (Art. 79(3)) protecting core constitutional identity (human dignity, democratic order) from amendment; proportionality doctrine is central and demanding; strong rights culture with both vertical effect and limited “Drittwirkung” (horizontal effect) via private law.
- South Africa Bill of Rights: Comprehensive enumeration with an explicit general limitations clause (s.36) and detailed remedies/standing (s.38), emphasizing substantive equality and reasonableness review.
- ICCPR (International Covenant on Civil and Political Rights): Structured rights with limited derogations during emergencies (Art. 4), and a list of non‑derogable rights (e.g., life, freedom from torture, slavery, retrospective criminalization, recognition as a person, freedom of thought, conscience, and religion).
- Swiss federal amendment process: “Double majority” for constitutional changes—majority of voters and majority of cantons—mitigates transient majorities and protects federalism.

Key takeaways:
1) Maximal speech protection works best when carve‑outs are few, objective, and tightly defined.  
2) A principled limitation test must be rigorous (strict scrutiny or a hard‑edged proportionality) with burden on the state.  
3) Remedies and standing determine real‑world force; weak remedies hollow out rights.  
4) Emergency derogations require hard guardrails and short fuses; specify non‑derogables.  
5) Entrenchment plus double‑majority reduces populist erosion; consider an eternity floor for core rights.  

---

## Design Goals
- Minimalism with precision: enumerate core negative rights; avoid bloat and vague programmatic “rights.”  
- Maximal speech protection: allow only objective carve‑outs; bar viewpoint‑based restrictions and “offense/harm to feelings” rationales.  
- Hard limitation doctrine: strong presumption of liberty; strict tests; burden of proof on the state with evidence.  
- Strong remedies and fast process: pre‑enforcement review, injunctive relief, damages, fee‑shifting, exclusionary rule where applicable.  
- Entrenchment with double locks: supermajority + double‑majority; eternity protection for a core subset.  
- Clarity for emergencies, horizontality, and interpretation to reduce drift and judicial invention.  

---

## First Principles: What is a Right and Why Enshrine It?
Working definition (institutional):  
Rights are enforceable side‑constraints and claims that structure how power may be used. They create stable expectations by pairing an individual’s protected sphere with corresponding duties on institutions (and sometimes on other persons). A right only “exists” to the extent it is: (a) justiciable, (b) predictable, and (c) remedied when violated.

Why enshrine rights (problem statements and functions):
- Credible commitment: Prevents today’s majority or executive from reneging tomorrow (time‑inconsistency and populist surges).  
- Agency and capture: Constrains officials whose incentives can diverge from the public’s (agency/capture risk).  
- Coordination and investment: Stable expectations (speech, property, due process) reduce transaction costs, foster trust, and increase long‑horizon investment.  
- Uniform baselines: Creates common knowledge of limits across all branches/levels of government.  
- Measurement and accountability: Puts the burden on the state to justify restrictions and enables audits and remedies.

Kinds of rights (Hohfeldian map for drafting clarity):
- Claim‑rights ↔ duties (e.g., due process implies state duties).  
- Liberties/privileges ↔ no‑rights (e.g., liberty to speak implies no counter‑claim by the state to stop speech).  
- Powers ↔ liabilities (e.g., citizen power to sue creates state liability).  
- Immunities ↔ disabilities (e.g., immunity from ex post facto laws disables legislative power to criminalize retroactively).

“From” vs “To” (negative vs positive):
- Default to “freedom from” state interference for the BoR core: clearest, least distortionary, avoids judicial budgeting, and minimizes policy drift.  
- Recognize a minimal set of structural “rights to” essential for democracy and legality (e.g., vote, access to courts, basic access to public information). Treat broader social goods (health, housing, environment) as Acts with metrics and budgets rather than judicially enforceable BoR entitlements.

Vertical vs horizontal application:
- Vertical baseline: binds public actors.  
- Limited and explicit horizontal reach only where private actors function as state‑delegated monopolies or essential communications/common carriers under narrow, reviewable designation.  
- Otherwise, indirect horizontality: constitutional values inform private law (tort/contract/competition) without creating universal BoR causes of action against private parties.

Inclusion criteria (when a principle belongs in the BoR rather than Acts):
1) Universality and generality (applies across contexts and eras).  
2) Justiciability (objective standards courts can apply) and remedyability.  
3) Incentive alignment (reduces abuse of power under realistic self‑interest assumptions).  
4) Low obsolescence risk (technology‑agnostic where possible, or framed at the right abstraction level).  
5) Cost boundedness (negative rights or narrowly tailored structural positives).  
6) Measurability (violations and compliance can be audited with metrics).

Failure modes to avoid:
- Rights inflation (too many vague promises dilute enforcement).  
- “Balancing” without guardrails (open‑ended proportionality that drifts into policy).  
- Permanent emergencies (ratchet effects).  
- Hidden viewpoint discrimination under civility/offense rationales.  
- Positive entitlements without budgets/metrics (courts as allocators).  

Design tests (ex ante and ex post):
- Ex ante Rights Impact Statement: identify aim, evidence of harm, least‑restrictive means, metrics, and sunset plan.  
- Ex post audits: measure chilling effects, violation rates, remedy speed, recurrence, and disproportionate impacts; publish to the Civic Outcomes Ledger.

---

## Subsumption-Based Rights Model (proposal)
Premise: Each fundamental right is dominant by default. It may be “subsumed” (specifically restricted) only through a closed list of exception types and by passing hard, objective meta‑rules. This aims to prevent later dilution by vague balancing tests, shifting fashions, or populist waves.

Subsumption meta‑rules (apply to any restriction of any right):
1) Closed‑list exceptions only: Restrictions must fit an enumerated exception type; generic “public interest,” “offense,” or “hate” rationales are out of scope.  
2) Burden and evidence: The state bears the burden with clear and convincing evidence that the restriction targets a concrete, measurable risk; pre‑enactment Rights Impact Statement with metrics and review plan.  
3) Necessity and least‑restrictive means: Demonstrate no materially less‑restrictive alternative would achieve the legitimate aim.  
4) Narrow tailoring in scope and time: Limit by subject, geography, and duration; automatic sunset and periodic review.  
5) Content/viewpoint constraints for speech: Content‑based rules face strict scrutiny; viewpoint‑based rules are per se invalid.  
6) No prior restraint as a rule: Licensing only if objective, nondiscretionary, time‑limited, with default‑grant and prompt judicial review.  
7) Transparency and audit: Immediate logging to the Civic Outcomes Ledger; mandated after‑action audits with public reporting.  
8) Non‑derogables: Identify rights that are never subsumable (e.g., bans on torture/slavery, core due process legality/non‑retroactivity, recognition as a person, freedom of thought/conscience).  
9) Collision rule: Where rights collide, protect non‑derogables first; otherwise choose the accommodation that minimally impairs the total rights set (minimal‑impairment principle).  
10) Remedies: Pre‑enforcement standing where chilling effects exist; expedited injunctions; fee‑shifting for prevailing claimants; personal liability for willful violations.

Notes on speech within this model:
- Objective carve‑outs (closed list): incitement to imminent and likely unlawful violence; true threats of unlawful violence; defamation (with fault standards); content‑neutral time/place/manner leaving ample alternatives.  
- Explicit exclusions: offense, disrespect, blasphemy, or hurt feelings are not grounds for restriction.

“From” vs “To” framing (negative vs positive rights):
- Default to “freedom from” government interference (negative liberties). This keeps courts out of resource allocation and avoids judicial policy‑making.  
- Limited “rights to” are appropriate where necessary for democratic function and due process (e.g., access to courts, vote, basic information access obligations) and should be drafted narrowly as structural guarantees, not open‑ended entitlements.  
- Broader positive aims (healthcare, housing, environment) should live in Acts with metrics and budgets, audited via outcomes—not as judicially enforceable BoR entitlements.

Horizontality options (who must respect rights):
- A) Pure vertical effect (default): binds public actors only (avoids compelled private speech, protects association/contract).  
- B) Limited direct horizontality for “Essential Communications Carriers” or state‑delegated monopolies designated by an independent regulator under strict criteria and sunset; obligations focus on viewpoint‑neutral access and due process.  
- C) Indirect horizontality: private law routes (contract, tort, competition) shaped by constitutional values without BoR causes of action against private parties.

Why most systems avoid full horizontality:
- Protects private autonomy, editorial discretion, property and association; reduces chilling effects and constitutionalizing every private dispute.  
- Risks of capture and definitional drift for “platform as public square.”  
- Middle path: keep BoR vertical; allow targeted Acts for essential facility contexts with hard guardrails, transparency, and narrow remedies.

Potential pitfalls addressed by subsumption rules:
- Vague “public interest” balancing eroding rights over time; viewpoint discrimination masked as civility; permanent emergency creep; unbounded positive claims that override fiscal discipline.

Decision hooks:
- We can encode the meta‑rules once in a BoR preamble clause and cross‑reference them for each right, minimizing duplication and future drift.

---

## Proposed Core Rights Set (first‑principles rationale)
1) Freedom of thought, conscience, and religion (belief absolute)  
   Why: The “inner forum” is foundational to autonomy and pluralism; coercing belief is both futile and corrosive. Manifestation may be regulated only via subsumption meta‑rules.

2) Freedom of expression, press, assembly, association; no compelled speech; no prior restraint  
   Why: Society’s epistemic engine—error‑correction, accountability, and coordination. Necessary for democratic control and innovation. Restrictions must fit the closed speech carve‑outs and pass strict/meta‑rules.

3) Due process and legality  
   Why: Credible commitment against arbitrary power reduces fear, corruption, and selective enforcement. Includes nullum crimen/nothing retroactive, fair and public hearing, impartial tribunal, presumption of innocence, counsel, confrontation, double jeopardy bar, and ban on bills of attainder.

4) Bodily integrity and dignity; bans on torture, cruel/inhuman punishment, slavery/servitude, forced labor  
   Why: Prevents instrumentalization of persons; cornerstone of human dignity. Non‑derogable.

5) Personal liberty and security; habeas corpus; freedom from arbitrary arrest/detention  
   Why: Direct check on executive force; prevents chilling and coercion that undermine all other rights.

6) Privacy of person, home, papers, and data; secure communications  
   Why: Privacy sustains autonomy and dissent; modern “papers” include data. Warrant standard, specificity, and accountability logs; strong default for encryption and against compelled decryption absent narrow, judicially supervised conditions under meta‑rules.

7) Property and contract; just compensation for takings  
   Why: Stable expectations enable investment and dispersed power; protects against predation. Externality Principle governs limits; takings require due process and compensation.

8) Equality before law and non‑discrimination by the state  
   Why: Legitimacy and fairness; prevents caste systems and targeted repression. Suspect classifications face the highest scrutiny; remedies deter selective enforcement.

9) Freedom of movement and residence (including emigration)  
   Why: Exit rights discipline jurisdictions and reduce capture; essential to opportunity and safety. Restrictions must be narrowly tailored under meta‑rules.

10) Political rights: vote, stand for office (neutral qualifications), petition, and access to public information  
    Why: Structural “rights to” enabling democratic control of outcomes; make other rights enforceable in practice and consistent with Radical Transparency.

11) Access to courts and effective remedy (including pre‑enforcement review and fee‑shifting)  
    Why: Rights exist only if remedied. Ensures standing for chilling effects, expedited review, and incentives for private enforcement where the state has conflicts.

Non‑derogable floor (illustrative): items in 4), core of 3) (legality/non‑retroactivity), recognition as a person, and freedom of thought/conscience (1). Others may be derogated only under formal emergency per strict rules and sunsets.

Items under consideration (not core by default): arms/self‑defense (design and externalities), family/marriage definitions (risk of historic contingency), broad socio‑economic entitlements (prefer Acts with metrics and budgets).

---

## Combined Core Rights (compact formulation)
1) Freedom of thought  
   - Scope: belief, conscience, inquiry, and inner deliberation.  
   - Why: Inner forum autonomy is foundational; coercing belief is futile and corrosive.  
   - Non‑derogable core: belief and conscience.

2) Freedom of communication  
   - Scope: create/receive information; speak/publish; assemble/associate; petition; no compelled speech; no prior restraint.  
   - Why: Epistemic engine for error‑correction, accountability, and democratic coordination.  
   - Exception channels: closed speech carve‑outs (incitement to imminent and likely unlawful violence; true threats; defamation with fault), and content‑neutral time/place/manner—each under strict/meta‑rules.

3) Physical freedom of movement and bodily integrity  
   - Scope: bodily autonomy and dignity; bans on torture/cruel treatment; slavery/servitude/forced labor; personal liberty/security; habeas; movement, residence, and emigration.  
   - Why: Prevents instrumentalization and coercion that collapse all other liberties.  
   - Non‑derogable core: no torture/cruel treatment; no slavery/servitude/forced labor; recognition as a person.  
   - Exception channels: (a) judicial sentencing post‑conviction (proportional, time‑limited); (b) narrowly tailored public‑health isolation/quarantine under judicial oversight; (c) formal emergency derogation with strict guardrails and short fuses.

4) Privacy and data autonomy  
   - Scope: privacy of person, home, papers, effects, and data; secure communications; freedom from unreasonable search/seizure.  
   - Why: Privacy sustains autonomy and dissent; information is non‑rival and copyable—pure property logic under‑protects it; consent is often coerced via adhesion contracts.  
   - Exception channels: judicial warrant with particularity and minimization; transparent logging; narrow compelled decryption only under strict necessity, use‑restriction, and audit.

5) Property and contract  
   - Scope: acquire/hold/use/dispose; freedom of contract; just compensation for takings.  
   - Why: Stable expectations enable investment and diffuse power; guards against predation.  
   - Exception channels: neutral, transparent regulation under the Externality Principle; due process; no confiscation without compensation.

6) Status neutrality (equal legal protection)  
   - Scope: immunity from status‑based legal advantages/disadvantages; the state must govern by neutral, general rules focused on actions, not identity.  
   - Why: Prevents caste systems and power entrenchment; preserves open access to the “rules of the game.”  
   - Implementation: suspect classifications face highest scrutiny; reasons and evidence required for any differential treatment.

7) Self‑government and accountability  
   - Scope: vote; stand for office (neutral qualifications); observe/record public proceedings; petition; access public information.  
   - Why: Functional instrumentation for popular sovereignty and Radical Transparency; not arbitrary—these are the minimum levers to control outcomes and verify performance.

8) Access to justice and effective remedy  
   - Scope: standing (including chilling‑effects), pre‑enforcement review, timely hearing, injunctive/declaratory relief, damages, fee‑shifting, exclusionary rule.  
   - Why: Ubi jus ibi remedium—rights exist only if enforceable; converts liberties into predictable constraints on power and prevents the state from blocking redress.

Tightened non‑derogable floor (illustrative):  
   - Freedom of thought (belief/conscience).  
   - Ban on torture/cruel/inhuman treatment; slavery/servitude/forced labor.  
   - Recognition as a person before the law.  
   - Legality/non‑retroactivity in criminal law (no ex post facto punishment).

---

## Exclusive Exception Channels (rights are otherwise inviolate)
1) Judicial Sentencing Channel  
   - Only after conviction for a defined offense; proportionality; time‑limited; reasoned judgment; automatic review rights.  
   - Applicable to: targeted movement restrictions, association prohibitions related to the offense, specific occupational bars.

2) Warrant/Search Channel  
   - Judicial warrant, probable cause, particularity, minimization; logging and notice; use‑restriction; exclusionary remedies for violations.  
   - Applicable to: privacy, home/papers/data, and certain property contexts.

3) Emergency Derogation Channel  
   - Formal declaration; legislative concurrence; strict time limits; non‑derogables intact; necessity and least‑restrictive means; real‑time Ledger logging and after‑action audit.  
   - Applicable to: temporary movement limits, targeted assembly restrictions when strictly necessary.

4) Speech‑Specific Channel  
   - Closed carve‑outs: incitement to imminent and likely unlawful violence; true threats; defamation (fault standards).  
   - Content‑neutral time/place/manner: significant interest; ample alternatives; no discretion; objective criteria.  
   - Viewpoint discrimination per se invalid; prior restraint presumptively invalid with narrow licensing exceptions under default‑grant and prompt review.

5) Externality Regulation Channel (Property/Contract)  
   - Neutral rules addressing measurable externalities; transparent assessment; least‑restrictive means; compensation when a taking occurs.  
   - Not a backdoor for speech or status regulation.

Meta‑constraints for all channels (recap): legality, clear aim, evidence burden on the state (clear and convincing), necessity and LRM, narrow tailoring in scope/time, automatic sunsets, periodic review, transparency and audit, robust remedies.

Privacy is not only property—why both are needed:  
   - Alienability: property can be sold/waived; privacy needs non‑waivable baselines to avoid coerced “consent.”  
   - Non‑rival copying: seizure/duplication of data causes harm beyond dispossession.  
   - State power: warrant standards protect against coercive state access regardless of title.

Equality reframed as status‑neutral governance (first principles):  
   - It is an immunity that disables the state from conferring status privileges/burdens; it forces evenhanded rules targeting actions, not identities—thereby preventing capture, patronage, and caste.

---

## Candidate Architecture (non-binding outline for discussion)
1) Scope and Applicability  
   - Vertical effect: binds all public actors.  
   - Limited direct horizontality where private actors function as essential common carriers or state‑delegated monopolies (to be defined), otherwise indirect horizontality via private law duties.
2) Enumerated Rights (high‑level baskets)  
   - Expression and Belief: speech, press, assembly, association, conscience, religion; strong no‑prior‑restraint rule.  
   - Due Process and Criminal Procedure: legality, presumption of innocence, fair trial, counsel, confrontation, double jeopardy bar, bans on ex post facto and bills of attainder.  
   - Privacy, Home, and Papers: warrant requirements, data and communications privacy by default, secure encryption; seizure rules; civil forfeiture barred absent conviction.  
   - Property and Contract: secure property, just compensation for takings, freedom of contract subject to narrowly tailored externality controls.  
   - Equality Before Law: equal protection and anti‑discrimination by the state; suspect classifications trigger highest scrutiny.  
   - Movement and Residence: travel, emigration/immigration control subject to law, proportional restrictions.  
   - Bodily Autonomy and Integrity: protection against torture, cruel/inhuman treatment, forced labor; informed consent.  
   - Political Rights: vote, stand for office (with reasonable, neutral qualifications), petition, access to information.  
   - Catch‑All Clause: unenumerated rights preserved (akin to Ninth Amendment), interpreted via Constitutional Core and tradition/reason.
3) Limitation Clause (strong form)  
   - Any restriction must satisfy all: legality (clear, public law), legitimate aim, necessity, least‑restrictive means, and proportionality of overall effects; plus strict scrutiny for content‑based speech restraints and suspect classifications. Burden of proof rests on the state with evidence and metrics.  
4) Speech Carve‑Outs (closed list; objective)  
   - Incitement to imminent and likely unlawful violence.  
   - True threats of unlawful violence.  
   - Defamation with fault standards (e.g., actual malice for public officials/figures).  
   - Content‑neutral time, place, and manner restrictions serving significant interests, leaving ample alternatives.  
   - Explicit exclusions: “offense,” “hate,” “disrespect,” or other subjective harms are not standalone categories.  
5) Remedies and Enforcement  
   - Standing: pre‑enforcement and as‑applied challenges; chilling‑effect standing for speech.  
   - Remedies: injunctive and declaratory relief; suppression/exclusionary rule for unlawful searches; damages (including statutory and punitive where willful); fee‑shifting for prevailing rights claimants; personal liability for willful official violations.  
   - Process: expedited hearing schedules; interim relief standards; transparency via the Civic Outcomes Ledger.  
6) Emergencies and Derogations  
   - Formal declaration with strict time limits, legislative concurrence, immediate public recording, and automatic sunset.  
   - Non‑derogables aligned to ICCPR core (life; freedom from torture/slavery; legality/non‑retroactivity; recognition as a person; freedom of thought, conscience, and religion).  
   - Heightened review and mandatory after‑action audit with public report.  
7) Amendment and Entrenchment  
   - Amend BoR only by supermajority legislature + national referendum double‑majority (citizens + sub‑units).  
   - Eternity clause for a core subset (e.g., bans on torture/slavery, basic due process, equality before law, and speech baseline).  
8) Interpretation  
   - Guided by the Constitutional Core (assume self‑interest; harness through incentives; diffuse power; radical transparency; outcomes and measurement; market where possible; measurement over assertion).  
   - Resolve ambiguity to maximize liberty consistent with Core and the Externality Principle; avoid rights as positive policy mandates unless explicitly stated.  
9) Sanctions and Graded Penalties (for later Acts)  
   - Prefer right‑specific restrictions (e.g., targeted limitations on vote, travel, arms possession) over carceral defaults, subject to strict proportionality and due process.

---

## Tradeoffs and Discussion
- Strict Scrutiny vs. Proportionality: Strict scrutiny is speech‑protective but can be brittle; proportionality is flexible but risks drift. A hybrid (strict for content/viewpoint, proportionality elsewhere) may capture the best of both.  
- Notwithstanding/Override Clauses: Provide democratic escape valves but invite abuse; if included, require double‑majority renewal, narrow scope, and automatic expiry.  
- Horizontality: Direct horizontality expands protection against private coercion but risks judicial reach; a limited carve‑out for essential facilities/common carriers plus robust private‑law remedies may suffice.  
- Positive Rights: Expand ambitions but complicate enforcement and budgeting; default to negative rights with explicit, separately legislated mandates audited via outcomes.  

---

## Open Questions (for iterative resolution)
1) Enumerated list: which specific rights belong in the canonical text vs. Acts?  
2) Defamation standards: adopt U.S. “actual malice” for public officials/figures? Define negligence for private figures?  
3) Obscenity/sexual speech: omit category or adopt a narrow, objective standard?  
4) Arms and self‑defense: include, and if so, under what training/responsibility regime?  
5) Horizontality scope: define “essential facilities” and the threshold for BoR duties on private actors.  
6) Emergency derogations: list exact non‑derogables and maximum durations/renewals.  
7) Override/notwithstanding: include at all? If yes, what procedural and scope limits?  
8) Digital privacy: enumerate encryption and compelled decryption limits explicitly?  
9) Equality: define suspect classifications and scrutiny tiers explicitly or leave to doctrine?  
10) Graded penalties: canonicalize right‑specific sanctions or delegate entirely to Acts?  
11) Subsumption meta‑rules: Should “clear and convincing evidence,” default‑grant licensing, and automatic sunsets be hard‑coded?  
12) Viewpoint neutrality and no prior restraint: per se rules or subject to strict scrutiny?  
13) Essential Communications Carriers: what designation criteria, who designates, what appeals, what sunset cadence?  
14) Should we recognize limited positive “rights to” (vote, access to courts, basic information) in the BoR text, or move all such obligations to Acts with metrics?  

---

## Constitutional Core Alignment (preliminary)
1) Assume human nature: Strong constraints, burdens, and personal liability align.  
2) Harness, don’t hope: Structural remedies and audits channel incentives.  
3) Power diffused, checked: Entrenchment + double‑majority + eternity clause limit concentration.  
4) Radical transparency: Ledger logging for restrictions, audits, and emergency use.  
5) Democracy on outcomes: Clear metrics for necessity/least‑restrictive‑means and periodic review.  
6) Market where possible: Prefer market mechanisms to restrict harmful externalities without speech suppression.  
7) Measurement over assertion: Evidence‑based limitation tests; mandatory impact audits.

---

## References (illustrative)
- United States Bill of Rights — overview: https://en.wikipedia.org/wiki/United_States_Bill_of_Rights  
- Brandenburg v. Ohio (incitement): https://en.wikipedia.org/wiki/Brandenburg_v._Ohio  
- Virginia v. Black (true threats): https://en.wikipedia.org/wiki/Virginia_v._Black  
- New York Times Co. v. Sullivan (defamation, actual malice): https://en.wikipedia.org/wiki/New_York_Times_Co._v._Sullivan  
- Canadian Charter s.1 (Oakes test): https://en.wikipedia.org/wiki/R_v_Oakes  
- ECHR, Article 10 and limitations: https://en.wikipedia.org/wiki/Article_10_of_the_European_Convention_on_Human_Rights  
- German Basic Law, eternity clause (Art. 79(3)): https://en.wikipedia.org/wiki/Basic_Law_for_the_Federal_Republic_of_Germany#Eternity_clause  
- South African Constitution, Bill of Rights (s.36, s.38): https://en.wikipedia.org/wiki/Constitution_of_South_Africa#Bill_of_Rights  
- ICCPR Article 4 (derogations): https://en.wikipedia.org/wiki/International_Covenant_on_Civil_and_Political_Rights#Derogations  
- Swiss double majority (constitutional amendments): https://en.wikipedia.org/wiki/Swiss_federal_popular_initiative  

---

## Next Steps
- Debate enumerations and finalize the carve‑outs list.  
- Decide on limitation test structure (strict vs. proportionality hybrid).  
- Choose entrenchment formula and whether to include an override clause.  
- Draft candidate BoR text once the above are agreed, with “Changed Sections” targeting the current Article VII.

---

## Convergence Snapshot (2025-11-13)

Current proposal (≤10 bullets)
- Minimal primitives consolidated into eight rights: thought; communication; movement/bodily; privacy/data; property/contract; status‑neutral governance; self‑government and accountability; access to justice and remedy.  
- Non‑derogable floor: belief/conscience; no torture/cruel/inhuman treatment; no slavery/servitude/forced labor; recognition as a person; legality/non‑retroactivity; strong presumption for status‑neutral governance.  
- Lawful Overrides: closed, enumerated paths (Judicial Sentencing/Order; Warrant/Search; Emergency Derogation; Speech‑specific; Externality Regulation) under strict meta‑rules (legality; clear and convincing evidence; necessity + least‑restrictive means; narrow tailoring; sunsets; logging/audit; fee‑shifting; no viewpoint discrimination; prior‑restraint presumption).  
- Speech carve‑outs: incitement to imminent and likely unlawful violence; true threats; defamation (fault); content‑neutral time/place/manner; explicit exclusions for “offense/hate/disrespect.”  
- Public Transparency and Auditability (Live and Archived): combines observe/record with machine‑readable access to budgets/models/data/code; minimal redactions with automatic review.  
- Privacy baseline: warrant/particularity/minimization/use‑restriction/logging; bounded compelled decryption; Acts may add data‑fiduciary duties.  
- Remedy bundle: standing incl. chilling/pre‑enforcement; expedited interim relief; exclusionary rule; damages; fee‑shifting; right to reasons/record.  
- Horizontality: vertical baseline; optional designation of essential communications carriers via Acts with viewpoint‑neutral access and due process; indirect horizontality via private law.  
- Entrenchment: supermajority + double‑majority referendum; eternity clause for a core subset.  
- Sanction catalog principle: penalties restrict only the minimal subset of rights proportionally and reviewably.

Core alignment (Constitutional Core)
1) Assume human nature: strong burdens on the state; personal liability; audits.  
2) Harness, don’t hope: remedies, transparency, competition in competence (open candidacy).  
3) Power diffused, checked: entrenchment, double‑majority, eternity floor, judicial review.  
4) Radical transparency: explicit right to live and archived transparency; ledger logging.  
5) Democracy on outcomes: self‑government control loop; metrics and verification.  
6) Market where possible: neutral externality regulation; private competition; minimal positive rights.  
7) Measurement over assertion: evidence standards, least‑restrictive means, impact audits.

Pros (≤6)
- High legibility via closed, enumerated overrides with objective meta‑rules.  
- Strong speech protection (viewpoint neutrality, prior‑restraint presumption, narrow carve‑outs).  
- Enforceability through a concrete remedy bundle and transparency obligations.  
- Robust emergency constraints with non‑derogables and automatic sunsets/audits.  
- Modular: details can evolve in Acts without bloating the BoR.  
- Aligned to outcome‑democracy: public transparency and auditability built in.

Cons (≤6)
- Risk of brittleness if overrides are under‑inclusive; pressure to add ad hoc exceptions.  
- Boundary litigation likely (what counts as “clear and convincing,” LRM in practice).  
- Administrative overhead for logging/audit and data publication quality.  
- Platform/private gatekeeping only partially addressed by designation regime (political risk).  
- Privacy baseline may tension with investigative timelines; needs careful timelines/use‑restriction design.  
- Political resistance to eternity clauses and stringent entrenchment thresholds.

Outstanding questions
1) Finalize names, scopes, evidence standards, timelines, and renewal cadence for each Lawful Override.  
2) Confirm the non‑derogable list (include status‑neutral governance explicitly or leave as near‑absolute?).  
3) Defamation standards for public officials/figures vs private figures; remedies for deepfakes.  
4) Digital privacy specifics: compelled decryption scope; production immunity; deletion schedules; purpose limitation.  
5) Designation of essential communications carriers: criteria, designating authority, appeal, sunset cadence.  
6) Visitor/irregular‑migrant rights tiers (minimum non‑derogables, due process scope, cost/time bounds).  
7) Equality: codify suspect classifications vs general status‑neutral rule with remedial leeway?  
8) Arms/self‑defense: include in primitives or delegate to Acts with externality controls?  
9) Petition in a non‑politician system: routing obligations, metrics hooks, anti‑majoritarian guardrails.  
10) Sanction catalog details (evidence standard, permissible scopes/durations, review cadence).  
11) Entrenchment numbers and whether any notwithstanding‑style override exists (default: no).

Recommendation
- Good but needs work. The architecture is coherent, legible, and aligned with the Core; however, we should finalize the Lawful Overrides’ objective parameters, the non‑derogable list, and a few key interfaces (transparency, privacy, designation regime) before marking Ready.


