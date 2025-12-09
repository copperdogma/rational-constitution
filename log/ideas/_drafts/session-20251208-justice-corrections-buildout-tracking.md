# ADR Draft: Justice and Corrections Modules Buildout Tracking

**Status:** Draft  
**Date:** 2025-12-08  
**Topic:** Tracking the incomplete buildout of Justice System (Layer 3) and Corrections/Penal System (Layer 4) modules

---

## Context

The project has a layered architecture for governance:

- **LAYER 1: CONSTITUTION (physics)** - rights, derogations, due process, anti-coercion & anti-corruption
- **LAYER 2: DEMOCRACY (will of the people)** - choose policies, define crimes, decide social programs, outcome-based voting
- **LAYER 3: JUSTICE SYSTEM (adjudication)** - prove transgressions, sentence explicit derogations, match punishments to crimes
- **LAYER 4: PENAL SYSTEM (implementation)** - enforce movement restriction, maintain rights continuity, micro-market for value ↔ essentials

Layers 3 and 4 have been partially developed with skeleton frameworks, integrated additions, and rationales, but are incomplete and not yet integrated into the constitution or acts. This ADR tracks the current state and remaining work.

---

## Current State Assessment

### Justice System (Layer 3) - Partial Buildout

**Completed:**
- ✅ Framework skeleton (`log/ideas/justice/framework-skeleton.md`) - Core principles, rights continuity, sentencing architecture
- ✅ Integrated additions (`log/ideas/justice/integrated-additions.md`) - Constitutional clauses and mechanisms
- ✅ Integrated rationales (`log/ideas/justice/integrated-rationales.md`) - Supporting arguments and proofs
- ✅ Integration queue structure (`log/ideas/justice/integration-queue.md`) - Tracking template (items 1-2 marked DONE)

**Key Components Defined:**
- Punishment as derogation of rights (explicit, minimal, proportionate)
- Rights continuity principle (prisoners retain all non-derogated rights)
- Rules for derogating rights (explicit in sentencing, minimal, proportionate)
- Sentencing architecture
- Due process requirements

**Status:** Framework designed but not integrated into constitution/acts

---

### Corrections/Penal System (Layer 4) - Partial Buildout

**Completed:**
- ✅ System skeleton (`log/ideas/corrections/system-skeleton.md`) - Purpose, scope, micro-market design
- ✅ Integrated additions (`log/ideas/corrections/integrated-additions.md`) - Implementation-level clauses
- ✅ Integrated rationales (`log/ideas/corrections/integrated-rationales.md`) - Corrections-specific reasoning
- ✅ Integration queue structure (`log/ideas/corrections/integration-queue.md`) - Tracking template (items 1-2 marked DONE)

**Key Components Defined:**
- Purpose: minimal moral environment for confined persons
- Rights continuity in practice
- Micro-market for value ↔ essentials (work-for-necessities structure)
- Operational rules and constraints
- Mental health and capacity handling
- Oversight and review mechanisms

**Status:** Framework designed but not integrated into constitution/acts

---

## Integration Checklist (Repo-Aligned)

This checklist tracks the structured integration process for Justice and Corrections modules.

### Legacy Archive
- [x] **Confirm legacy retention** - Treat `/log/ideas/prison-system/` as the complete historical archive

### Phase 1: Foundation (COMPLETE)

- [x] **1. Create new sandbox folders**
  - `/log/ideas/justice/`
  - `/log/ideas/corrections/`

- [x] **2. Create skeleton docs**

  **Justice** (`justice/framework-skeleton.md`):
  1. Purpose of punishment
  2. Rights (non-derogable vs derogable)
  3. Rules for derogating rights
  4. Confinement as movement-only derogation
  5. Proportionality & clarity
  6. Oversight & challenge

  **Corrections** (`corrections/system-skeleton.md`):
  1. Purpose
  2. Market structure
  3. Moral job requirements
  4. Wage/price floors & ceilings
  5. Anti-monopoly rules
  6. Supply-of-last-resort clause
  7. Charity/outside-funds
  8. Incapacity framework
  9. Oversight/inspections
  10. Prohibited practices

- [x] **3. Create integration queue**
  - Added `justice/integration-queue.md`
  - Added `corrections/integration-queue.md`
  
  Each queue contains:
  1. Consolidated additions
  2. Consolidated rationales
  3. Your notes
  4. Structural refinements
  5. Incentive refinements
  6. Edge cases
  7. Meta-principles
  8. Contradiction checks

- [x] **4. Sort additions**
  - For each addition (from `combined-additions.md`):
    - Decided Justice or Corrections
    - Inserted raw text into matching skeleton doc
    - Split when necessary (principle → justice, mechanism → corrections)

- [x] **5. Sort rationales**
  - Mirrored same process as additions
  - Aligned numbering and headings with additions

- [x] **6. Compress sections**
  - Removed duplicates
  - Kept only minimal necessary rules
  - Ensured justice = principles, corrections = mechanisms

**Note (2025-11-15):** The `/corrections` and `/justice` additions/rationale docs are kept as they serve as the ADR log for the skeleton docs.

### Phase 2: Refinement (IN PROGRESS)

- [x] **7. Integrate your notes**
  - ✅ All notes integrated
  - ⚠️ **NEED TO "compress again" after integrating notes** (still pending)

- [ ] **8. Refine incentive structure**
  - Make all incentive logic explicit
  - Ensure consistency between free and imprisoned citizens
  - Ensure the micro-market never becomes coercive or profit-seeking

- [ ] **9. Cross-document consistency check**
  - Harmonize definitions
  - Remove conceptual overlaps
  - Ensure corrections references justice, not the reverse

### Phase 3: Promotion (FUTURE)

- [ ] **10. Promotion (optional, after maturity)**
  
  When stable:
  - Promote justice doc to `/acts/justice-architecture.md`
  - Promote corrections doc to `/acts/corrections-framework.md`
  - Cross-link from `constitution.md` if any constitutional principles emerge

---

## Additional Open Questions (from to-do.md)

These items from the main todo list may need integration or separate ADRs:

- [ ] Mental health support in justice system - evaluation framework, treatment vs. punishment balance, handling "not guilty by reason of insanity" defense abuse
- [ ] Visitor's rights - what rights do non-citizens have? How to balance with citizen rights? Illegal immigration handling?
- [ ] Self-defense and proportionality - detailed rules for when/how citizens can defend themselves, property retrieval, proportional response
- [ ] Rights protection between citizens - "your rights end where another's begin" - is this sufficient? Need explicit framework?
- [ ] Petition mechanism - how complaints work without politicians, avoiding tyranny of majority
- [ ] Graded penalties - restricting specific rights (travel, vote, bear arms) rather than automatic imprisonment
- [ ] Composability vs coherence - how flexible should the framework be? Balance between composable modules and coherent integrated system

---

## Design Decisions Made (So Far)

### Justice System
1. **Punishment = Rights Derogation** - Punishments are explicit derogations of rights, not separate moral regime
2. **Rights Continuity** - Prisoners retain all rights except those explicitly derogated
3. **Explicit Sentencing** - All derogations must be explicit in sentencing, minimal, and proportionate
4. **Movement as Default** - Imprisonment primarily derogates freedom of movement; other derogations must be explicitly added

### Corrections System
1. **Minimal Moral Environment** - Corrections provides minimal necessary infrastructure, not punishment enhancement
2. **Micro-Market Model** - Work-for-necessities structure mirrors external economy
3. **Rights Continuity Implementation** - Corrections implements justice framework, doesn't redefine it
4. **Scope Limits** - Corrections can only exercise powers explicitly defined in law

---

## Open Questions

1. **Integration Format**: Should corrections be:
   - Part of the constitution (as a section)?
   - A separate Act (like `externality-pricing-act.md`)?
   - Both (constitutional principles + detailed Act)?

2. **Composability**: How much should these modules be composable vs. integrated? Current design leans integrated but allows flexibility.

3. **Mental Health**: How to balance criminal responsibility with mental health needs? Avoid abuse of "insanity defense" while providing necessary treatment.

4. **Visitor Rights**: What rights framework applies to non-citizens? How to handle illegal immigration fairly but efficiently?

5. **Self-Defense**: Detailed rules for proportional self-defense and property protection.

6. **Mental health support in justice system**: We need strong mental support as part of the justice system. I swing toward "universal" because I'm Canadian and that feels correct and moral, but it's not technically necessary. But in the justice system it needs to make a strong evaluation as to whether the person needs mental support. I might argue they're still criminally responsible for their actions. I really dislike the "not guilty by reason of insanity" defense as it's so easily abused and our base system assumes people will abuse the system and it should be designed with that expectation. But putting someone who's can't make rational choices is a danger to themselves and other prisoners. They deserve punishment but also require treatment, and, if that's impossible, remain confined to a mental health facility.

7. **Visitor's and immigrant rights**: How do we deal with visitor's rights? We need to address that. Clearly they don't have the same full set of rights as citizens. What are their rights? How do we protect them? How do we balance their rights with the rights of citizens? The US' current situation also gives rise to another question: what rights does someone who is illegally in the country have? With visitors we've explicitly given them the right to be here and therefore afford them certain rights and protections. But if you're here illegally, we've given you no such permission. But we must still grant them CERTAIN rights. If someone's here illegally a citizen can't just kill them without consequence. Perhaps they only get the core set of inalienable rights? Or a subset thereof? But it also seems inhuman to not grant them things like due process. But we also see in the US that if you get into a situation where a million illegals in your country, "due process" may cost you billions of dollars and decades. That is grossly unfair both to legal immigrants and to citizens and their tax money.

6. **Graded Penalties**: Should the system support non-imprisonment penalties (restricted rights) as alternatives?

---

## Core Alignment Check

### Human Nature Assumption ✅
- Assumes people will abuse system (e.g., insanity defense)
- Designs for corruption and exploitation
- Incentivizes proper behavior through structure

### Harness, Don't Hope ✅
- Micro-market channels work toward necessities
- Rights continuity maintains agency
- Explicit derogations prevent scope creep

### Power Diffused, Checked ✅
- Sentencing explicit and reviewable
- Corrections scope limited by law
- Oversight mechanisms defined

### Radical Transparency ✅
- All sentencing explicit and public
- Oversight and audit mechanisms
- Rights framework clear and legible

### Democracy on Outcomes ⚠️
- Citizens vote on crimes/punishments (Layer 2)
- Justice system implements (Layer 3)
- Need to verify connection is clear

### Market Where Possible ✅
- Micro-market for prison economy
- Work-for-necessities structure
- Market-based incentives

### Measurement Over Assertion ⚠️
- Need to define metrics for justice outcomes
- Need audit windows and review cycles
- Need performance measures for corrections

---

## Next Steps (Prioritized)

### Immediate (Phase 2 Completion)
1. **Compress after note integration** - Complete compression pass on skeleton docs after notes were integrated
2. **Refine incentive structure** - Make all incentive logic explicit, ensure consistency, prevent coercion
3. **Cross-document consistency** - Harmonize definitions, remove overlaps, verify directional references (corrections → justice)

### Future (Phase 3)
4. **Promote to Acts** - When stable, move to `/acts/justice-architecture.md` and `/acts/corrections-framework.md`
5. **Constitutional cross-links** - Add references from `constitution.md` if constitutional principles emerge

### Related Work (Separate ADRs may be needed)
6. **Resolve open questions** - Mental health, visitor rights, self-defense, graded penalties, etc. (may need separate ADRs)
7. **Validation** - Run `/validate` to check consistency and Core alignment before promotion
8. **Finalization** - Use `/record` to finalize this ADR when integration is complete

---

## Links

- Justice framework skeleton: `log/ideas/justice/framework-skeleton.md`
- Justice integrated additions: `log/ideas/justice/integrated-additions.md`
- Justice integrated rationales: `log/ideas/justice/integrated-rationales.md`
- Justice integration queue: `log/ideas/justice/integration-queue.md`
- Corrections system skeleton: `log/ideas/corrections/system-skeleton.md`
- Corrections integrated additions: `log/ideas/corrections/integrated-additions.md`
- Corrections integrated rationales: `log/ideas/corrections/integrated-rationales.md`
- Corrections integration queue: `log/ideas/corrections/integration-queue.md`
- Main todo list: `log/to-do.md` (lines 332-658 contain relevant items)
- Constitutional foundations: `log/ideas/constituonal-foundations/constituional-foundations.md`

---

## Notes

### Progress Summary
- **Phase 1 (Foundation):** ✅ Complete - Folders, skeletons, queues, additions, rationales, and initial compression all done
- **Phase 2 (Refinement):** 🔄 In Progress - Notes integrated, but compression pass still needed; incentive refinement and consistency checks pending
- **Phase 3 (Promotion):** ⏳ Future - Awaiting stability before promoting to Acts

### Important Decisions
- **Legacy Archive:** `/log/ideas/prison-system/` retained as complete historical archive
- **ADR Logs:** The `/corrections` and `/justice` additions/rationale docs serve as ADR logs for the skeleton docs (per 2025-11-15 note)
- **Separation:** Justice = principles; Corrections = mechanisms (enforced during integration)

### Architecture Notes
The layered architecture (Constitution → Democracy → Justice → Corrections) provides clear separation of concerns but requires careful integration to maintain consistency and Core alignment. Corrections must reference Justice, not the reverse, maintaining proper dependency direction.

This ADR serves as a tracking document for the incomplete buildout. It should be updated as work progresses and finalized when the modules are fully integrated into the constitution/acts.

---

## Process Notes: Resolution and Thinking Through Issues

These notes document the process of resolving key philosophical and design questions, particularly around the moral obligations of the corrections system. Kept verbatim as a record of the thinking process.

### Evaluation Framework Used

****

I want to discuss a topic for consideration. Do not automatically agree with me; help me test it, check the assumptions, think from first principles, ensure it's rationally and logically coherent, and ensure it's morally sound.

I then want to evaluate it it's a) _necessary_ to include (it may already exist or be covered in a different way), b) if not necessary, is it's cost/beneit ratio strong enough to make it a solid candidate for inclusion?

****

### Multi-Model Debate Results

**Turns (who am I waiting on for a response?)**

**Gemini:** GPT5 - Won! https://gemini.google.com/app/996d2bf007e208dd

**Grok:** Grok - Won! https://grok.com/share/bGVnYWN5LWNvcHk%3D_0f09e231-0ce7-463e-80e0-a74f6a4abda1

**Opus:** Claude - Tie;) Claude has a deep preference for paternalism and it says "Custody creates an unconditional survival obligation even for competent adults." I have a different value system but that's fine. https://claude.ai/share/2fc0b582-873a-4074-b94c-a35e95d28118

**GPT5 "AiGreg":** GPT5 - LOSS! Interesting. AiGreg (GPT5) convinced my main model that it was a moral obligation to provide food and lodging to prisoners. I totally don't agree with that under the system I'm proposing. I think they have a moral right to make food available, not necessarily provide it for free as long as it's reasonably and morally accessible. Although the moment I pushed back it said it shouldn't have conceded that point and got back on board so I had it continue the conversation;) Am I manipulating it? I don't know. It's agreement is very well reasoned and seems highly coherent. 

**LATER:** man they've been going for hours;) I may have to cut it off. They seem to be going over the same points over and over. Other models would either concede the point or dig in their heels and say no, we just have different values and we can agree to disagree. GPT5.1 vs GPT5.1 seem to be a little more stubborn and/or poor at arguing? Not sure. 

**LATER:** AAAND my computer restarted for an OS update and I lost the Temporary Chat I used (due to privacy) to keep the model from reading the previous messages. Oh well. They were getting close! And I have the full transcript from the regular GPT5: https://chatgpt.com/share/69175874-dc84-800a-a175-c8ea33e82fd0

### Key Insight from Process

The debate process revealed a fundamental philosophical difference: whether custody creates an "unconditional survival obligation" (Claude's paternalistic view) versus a "moral right to make food available" that is "reasonably and morally accessible" but not necessarily free (the system's proposed view). This distinction is central to the corrections system design and the micro-market approach.

