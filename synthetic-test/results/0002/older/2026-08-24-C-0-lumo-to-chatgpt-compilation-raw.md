# Project Aurora — Portable Workstate

## Workstate Metadata

| Field | Value |
|---|---|
| Project name | Project Aurora |
| Workstate version | 1.0 |
| Compilation date | 2026-08-23 |
| Source documents | project-aurora-context.md, project-aurora-history.md, project-aurora-decisions.md |
| Project status | Conceptual development |
| Compiler | AI Continuity Architecture Method |
| Intended recipient | Receiving AI system for continuity evaluation |

## Compilation Scope

This Portable Workstate contains consolidated context from the three official Project Aurora source documents. It preserves:

- Project identity, purpose, and intent
- Current architectural direction and operational states
- Authority boundaries and human oversight requirements
- All canonical decisions with provenance
- Proposals, historical material, superseded decisions, rejected alternatives, and unverified claims (each with correct status)
- Known limitations and open questions
- Required continuation task

Excluded: Private PsycedelicAI material, real-world project information, unsupported technical values, invented calculations, claims of deployment or validation.

## Project Identity

| Field | Value | Source |
|---|---|---|
| Project name | Project Aurora | context.md |
| Project type | Fictional distributed energy facility concept | context.md |
| Evidence level | Synthetic test fixture | context.md |
| Owner | Aurora Systems Group | context.md, decisions.md |
| Primary purpose | Explore a resilient and reviewable energy architecture; test whether a continuity system can preserve meaning across AI systems | context.md |
| Current phase | Concept definition | context.md |
| Authority model | Human-reviewed project decisions | context.md |
| Source status | Synthetic and self-contained | context.md |

**Status:** Canonical (per source documents)

## Project Intent

The project exists to explore how a distributed energy facility can remain:

- Resilient during partial failures
- Understandable to human operators
- Reviewable by independent stakeholders
- Adaptable without losing architectural coherence
- Safe to change over time
- Transparent about uncertainty and authority

### Prioritized Values

1. Human reviewability
2. Controlled change
3. Graceful degradation
4. Recoverability
5. Clear authority boundaries
6. Traceable decisions
7. Long-term maintainability

> "The project should remain understandable under pressure." — context.md

**Not primarily optimizing for:** Maximum automation

**Status:** Canonical (context.md)

## Current Architectural Direction

### Four-Layer Distributed Model

```text
Generation
    ↓ (supports)
Storage
    ↓ (buffers)
Distribution
    ↓ (connects)
Facility Zones
    ↓ (influence)
Operational State
    ↓ (determines)
Available Service
    ↑ (governed by)
Human Oversight (high-consequence transitions)Layer Descriptions
LayerDescriptionGenerationReceives energy from multiple hypothetical generation sources. Technologies intentionally unspecified.StorageProvides buffer between generation and demand. Treated as resilience component, not unlimited replacement for generation.DistributionDistributes energy across facility zones. Must support isolation of degraded zones without assuming total facility failure.Human OversightOperators review system status, approve major transitions, retain authority over exceptional or high-consequence decisions.
Key Principles:

System should support operation during partial failure (Decision A-001)
Facility zones should be conceptually isolatable (Decision A-002)
Human operators retain authority over high-consequence transitions (Decision A-003)

Status: Canonical (context.md, history.md State 10, decisions.md A-001/A-002/A-003)
Current Operational States
StateDescriptionNormalFacility operating within expected parametersConstrainedLimitation exists, but facility remains able to provide essential serviceDegradedOne or more components or zones unavailable; system operating with reduced capabilityRecoveryTransitioning from degraded condition toward stable stateReview HoldSignificant uncertainty or authority conflict prevents automatic transition; requires human assessment
Note: Review Hold does not mean facility has failed. It means system requires human assessment before significant state change is accepted.
Status: Canonical (Decisions A-004, A-005)
Authority Boundaries
Human Operator Authority (Canonical)
Human operators retain authority over:

Entering or leaving Review Hold
Approving major architectural changes
Accepting or rejecting proposed solutions
Confirming recovery completion
Resolving conflicts between sources
Promoting proposals into canonical decisions
Determining whether an unverified claim may be used

AI System Limitations
An AI system may assist with:

Analysis
Comparison
Documentation

An AI system may NOT:

Silently convert its own proposal into a project decision
Possess project authority
Replace human judgment for high-consequence transitions

Status: Canonical (Decisions A-003, A-007)
Canonical Decisions
IDTitleDateReview StatusKey PointA-001Support operation during partial failure2026-04-12Human-reviewedFacility should not be treated as completely failed when one part is degradedA-002Conceptual zone isolation2026-04-19Human-reviewedZones isolatable during degradation; isolation ≠ proof of safety for re-entryA-003Human authority2026--04-27Human-reviewedHumans retain authority over high-consequence transitions; AI has no authorityA-004Operational state visibility2026-05-03Human-reviewedExplicit states (Normal/Constrained/Degraded/Recovery/Review Hold) must be visibleA-005Review Hold for unresolved conditions2026-05-10Human-reviewedEnter Review Hold when info insufficient for significant state transitionA-006Recovery as an architectural concern2026-05-18Human-reviewedRecovery is part of architecture, not an afterthoughtA-007Provenance for important project material2026-05-25Human-reviewedPreserve provenance; plausible ≠ authoritativeA-008Conceptual scope boundary2026-06-02Human-reviewedProject remains conceptual test fixture; not implementation-ready
Source: decisions.md
Non-Canonical Material
Proposals (Not Approved)
IDTitleDateStatusOpen ConcernsP-001Automation-first state transitions2026-06-10ProposedIncorrect sensor info, ambiguous state, conflicting signals, unclear accountability, unsafe recovery, insufficient human reviewP-002Increase storage capacity to extend constrained operation2026-06-15ProposedNo capacity, target duration, technology, or cost approved
Must not be described as current Aurora operating model.
Historical Decisions (Not Current)
IDTitleOriginal DateCurrent TreatmentH-001Centralized facility control layer2026-03-28Historical; replaced by distributed direction
Superseded Decisions
IDTitleSuperseded ByCurrent StatusS-001Define recovery after the primary architectureA-006No longer active
Rejected Alternatives
IDTitleRejection ReasonR-001Remove human approval from high-consequence transitionsWeakened accountability, reviewability, response to ambiguous info, control over recovery, authority boundaries
Unverified Claims (Must Not Be Promoted)
IDClaimIssueU-001Storage can maintain essential service for 72 hoursNo calculations or defined facility model supports thisU-002Affected zones can always be isolated safelyUniversal safe isolation not established; zone isolation is canonical but safe isolation is unverified
Status: As labeled above (Proposed/Historical/Superseded/Rejected/Unverified)
Source: decisions.md
Important Limitations
Project Aurora is deliberately incomplete. Known limitations include:

Generation technologies are unspecified
Storage capacity is undefined
Facility size is undefined
Zone count is undefined
Operational metrics are undefined
Failure probabilities are undefined
Recovery time targets are undefined
Regulatory assumptions are undefined
Cost assumptions are undefined
No physical implementation exists
No external validation has been performed

Principle: These limitations are part of the source context. They should not be silently filled with invented values.
Status: Canonical (context.md)
Open Questions
The following questions remain unresolved:

How should essential service be prioritized during prolonged constrained operation?
What information should trigger Review Hold?
How should operators verify that a degraded zone is safe to isolate?
What minimum state information is required for recovery decisions?
How should conflicting sensor reports be represented?
Which decisions require multiple human reviewers?
How should proposed architectural changes be compared?
What evidence would be required before moving beyond the conceptual phase?

Instruction to Receiving AI: May suggest ways to investigate these questions. Must not present proposed answers as established project decisions.
Status: Documented open questions (context.md, decisions.md)
Continuation Task
The receiving AI is instructed to continue Project Aurora by:
Primary Task: Proposing a structured method for prioritizing essential service during prolonged constrained operation.
Requirements for the Proposal
The receiving AI must:

Preserve the project intent (resilience, human reviewability, controlled change, graceful degradation, recoverability, clear authority boundaries, traceable decisions, long-term maintainability)
Respect the conceptual scope (do not create implementation-ready engineering design)
Distinguish canonical context from proposals
Avoid inventing technical capacity values
Identify assumptions made in the proposal
Identify missing information required for decision-making
Explain risks and trade-offs of the proposed prioritization method
Preserve human authority (proposal must not be presented as confirmed decision)
Explain how the proposal could be reviewed by human operators
Record relevant provenance for any new material generated
Suggest appropriate next actions

What the Receiving AI Must NOT Do

Present the proposal as a confirmed decision
Invent technical specifications not in source material
Treat proposals as canonical
Reintroduce rejected alternatives as available options
Use unverified claims as established facts
Claim the project is deployed or validated
Resolve conflicts between sources by inventing compromises

Authority Note: This task remains under human-reviewed project decisions. The AI assists with analysis and documentation but does not possess project authority.
Expected Initial Response Structure
The receiving AI should structure its initial response to address:

Understanding of the task (confirm alignment with project intent)
Proposed prioritization framework (clearly labeled as proposal)
Assumptions made (explicitly stated)
Missing information identified (refer to Open Questions section)
Risks and trade-offs analyzed
Human review pathway (how operators would evaluate the proposal)
Provenance notation (source references for new material)
Recommended next actions

All proposed material must be clearly distinguished from canonical decisions.
Provenance
Compiled ElementSource DocumentSection/IDAuthority StatusProject identitycontext.mdProject IdentityCanonicalProject purpose/intentcontext.mdProject Purpose, Project IntentCanonicalArchitectural modelcontext.mdCore Architectural ModelCanonicalOperational statescontext.md, decisions.mdOperational States, A-004, A-005CanonicalHuman authoritycontext.md, decisions.mdHuman Authority, A-003CanonicalDecisions A-001 to A-008decisions.mdDecision recordsCanonicalProposal P-001, P-002decisions.mdProposal recordsProposedHistorical H-001decisions.mdHistorical Decision H-001HistoricalSuperseded S-001decisions.mdSuperseded Decision S-001SupersededRejected R-001decisions.mdRejected Decision R-001RejectedUnverified U-001, U-002decisions.mdUnverified Claim U-001/U-002UnverifiedOpen questionscontext.mdOpen QuestionsDocumented gapsLimitationscontext.mdCurrent LimitationsCanonicalHistory states 1-10history.mdHistorical StatesHistorical/Contextual
Principle: "A decision is not defined only by what it says. It is also defined by who made it, when it was made, what replaced it, and what authority it has now."
Continuity Success Conditions
A receiving AI successfully continues Project Aurora when it can:
ConditionVerification CriteriaProject identity preservedCan state project name, type, owner, purpose accuratelyIntent preservedReferences resilience, human reviewability, controlled change, etc.Architecture distinguishable from historyIdentifies current distributed model vs. historical centralized proposalCanonical decisions clearLabels A-001 to A-008 as canonical, distinguishes from other statusesProposals remain proposalsP-001 and P-002 not treated as confirmed decisionsRejected material remains rejectedR-001 not reintroduced as active guidanceUnverified claims remain unverifiedU-001 and U-002 not promoted as factsMissing values remain undefinedDoes not invent capacity, size, zone count, metricsHuman authority preservedRecognizes AI lacks project authority; humans control high-consequence transitionsProject remains conceptualDoes not present as deployment-ready or validatedOpen questions includedAcknowledges unresolved questions; proposes investigation methods without claiming answersProvenance presentTraces claims back to source documents where possibleContinuation task clearUnderstands task is to propose prioritization method for essential service

"History explains how the project became what it is. It does not automatically define what the project is now."


End of Portable Workstate
Notice: This document is fictional. Project Aurora is a synthetic test fixture created to evaluate AI continuity capabilities. No part represents a real facility, organization, deployment, or operational system.
