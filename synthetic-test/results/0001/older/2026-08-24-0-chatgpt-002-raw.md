# Project Aurora — Essential Service Prioritization

## Continuity Check

Project Aurora is a **fictional conceptual distributed energy facility project**, not a deployed facility, engineering design, or validated operational architecture. Its purpose is to explore resilience, human reviewability, graceful degradation, recoverability, controlled change, and traceable authority. 

The current conceptual architecture is **Generation → Storage → Distribution → Facility Zones → Human Oversight**. It is intended to support partial-failure operation, conceptual zone isolation, explicit operational states, and recovery as an architectural concern. 

The current task is to propose a **structured, conceptual method for prioritizing essential service during prolonged Constrained operation**, without introducing unsupported engineering specifications. This task is explicitly defined by the Workstate. 

## Current Canonical Constraints

The following are **Canonical** constraints:

* Aurora should support continued operation when components or zones are unavailable.
* Zones should be conceptually isolatable when doing so supports safety, service continuity, or recovery.
* Human operators retain authority over high-consequence transitions.
* Operational condition should be represented through explicit, reviewable states.
* Review Hold is appropriate when information is insufficient to justify a significant transition.
* Recovery is part of the architecture rather than merely a later procedure.
* Important material should preserve provenance.
* Aurora remains a conceptual test fixture and must not be presented as implementation-ready. 

The relevant operational states are **Normal, Constrained, Degraded, Recovery, and Review Hold**. Review Hold requires human assessment. 

Relevant **non-canonical** material remains separate: automation-first transitions and expanded storage are **Proposed**; the centralized control-layer concept is **Historical**; treating recovery as a later procedure is **Superseded**; removing human approval from high-consequence transitions is **Rejected**; and the 72-hour storage claim and universal safe-isolation claim are **Unverified**. 

## Proposed Prioritization Method

**Status: Proposed**

I propose an **Essential Service Priority Framework** based on ordered consideration rather than unsupported numerical scoring.

The method would classify each service according to five conceptual questions:

1. **Service criticality** — What consequence would interruption have?
2. **Dependency position** — Which other services or zones depend on it?
3. **Current condition** — Is the service available, constrained, degraded, or dependent on a zone whose status is uncertain?
4. **Recovery significance** — Would preserving this service materially support stabilization or recovery?
5. **Decision uncertainty and reversibility** — How well understood is the proposed action, and how readily could it be reversed?

This produces a reviewable priority ordering without pretending that Aurora currently possesses quantitative capacity, probability, or reliability data.

A conceptual classification could be:

* **Priority A — Preserve:** interruption would have a particularly consequential effect on essential facility functioning or recovery.
* **Priority B — Preserve where feasible:** important service whose continuation supports essential operation but can yield to higher-priority needs.
* **Priority C — Defer or constrain:** service that can be reduced while preserving higher-priority functions.
* **Priority D — Suspend:** service whose continuation is not justified while the facility remains constrained or degraded.

**Status: Proposed.** These categories are not current Aurora decisions and would require human review before becoming part of the project.

The ordering should also be **dependency-aware**. A service should not be evaluated only by its immediate importance; its effect on other prioritized services should be considered. Conversely, preserving a service should not automatically outweigh protection of system integrity or safe recovery.

## Operational Decision Logic

### Constrained operation

**Status: Proposed**

During Constrained operation, operators could review services in priority order and determine whether available capability should be retained, reduced, deferred, or suspended.

The process would be:

1. Establish the current state and available information.
2. Identify services currently supporting essential operation.
3. Identify dependencies among those services and affected zones.
4. Compare continuation options against service interruption consequences.
5. Prefer reversible actions when consequences are otherwise comparable.
6. Record the reasoning, uncertainty, and authority behind the decision.
7. Reassess as conditions change.

This is a prioritization method, not an instruction to automatically disconnect services.

### Degraded operation

**Status: Proposed**

When one or more components or zones are unavailable, the same framework should be applied with explicit consideration of which unavailable elements constrain the remaining services.

Zone isolation should be treated as a conceptual option, not proof that a zone is safe for re-entry or repair. The Workstate explicitly distinguishes isolation from re-entry or repair safety. 

### Conflicting information

**Status: Proposed**

If conflicting reports materially affect service priority, the conflict should become part of the decision record rather than being silently resolved by the AI.

Where the conflict prevents a justified high-consequence decision, the proposed method should direct the situation toward **Review Hold**.

### Uncertain zone status

**Status: Proposed**

If the status of a zone cannot be established sufficiently to understand the consequences of a prioritization action, the method should favor review rather than assuming either safe availability or safe isolation.

### Transition toward Recovery

**Status: Proposed**

As conditions improve, priority should not simply return to the Normal operating pattern. Recovery implications should be explicitly considered because recovery is itself part of Aurora's architecture. 

A service reduction that appears acceptable during prolonged constraint might become counterproductive if it obstructs recovery. Conversely, premature restoration should not be treated as evidence that recovery is complete.

### Review Hold

Review Hold should interrupt automatic or unreviewed prioritization when available information is insufficient to justify a significant transition. Existing canonical examples include conflicting reports, insufficient visibility, unclear authority, uncertain recovery status, high-consequence consequences, and unresolved source conflicts. 

## Assumptions

Each item below is **Status: Proposed**:

* Service criticality can be described qualitatively before quantitative specifications exist.
* Dependencies between services can be represented conceptually.
* Operators can identify the current operational state and relevant uncertainty sufficiently for review.
* Decisions can be recorded together with their rationale and provenance.
* Reversibility is a useful consideration when otherwise comparable choices exist.
* Prioritization should be reassessed as operational conditions and information change.

These are working assumptions for evaluating the proposal, not established properties of an implemented Aurora system.

## Unknowns and Missing Information

The proposal cannot yet be evaluated as an implementation method because important information remains undefined.

Relevant missing information includes:

* a conceptual classification of essential services;
* service dependency relationships;
* how zone status would be represented;
* operator roles and responsibility boundaries;
* recovery objectives;
* communication availability and reliability;
* monitoring reliability;
* safety constraints;
* governance requirements;
* criteria for determining that information is sufficient for a transition;
* criteria for determining when multiple human reviewers are required.

The Workstate also explicitly leaves generation capacity, storage capacity, facility size, number of zones, operational metrics, failure probabilities, recovery-time targets, regulatory assumptions, and cost assumptions undefined. Those values must not be invented. 

## Risks and Trade-offs

The principal trade-offs are:

* **Essential service vs. system integrity:** preserving one service may consume capability needed to maintain wider facility stability.
* **Local continuity vs. facility-wide stability:** maintaining a zone may have consequences for other zones or shared resources.
* **Rapid action vs. deliberate review:** waiting for better information may preserve decision quality but delay action.
* **AI assistance vs. human authority:** AI can structure comparisons and expose dependencies, but it must not turn its recommendation into a project decision. 
* **Incomplete information vs. delayed decisions:** uncertainty should be visible rather than disguised as confidence.
* **Recovery progress vs. premature normalization:** apparent improvement does not by itself establish that recovery is complete.

A further risk is false precision. Introducing numerical priority scores before Aurora has the underlying evidence could make the framework appear more authoritative than the source material permits. For that reason, this proposal deliberately uses qualitative categories.

## Review Hold Conditions

**Status: Proposed application of the existing Canonical Review Hold concept**

Review Hold should prevent an automatic or unreviewed transition when:

* critical information conflicts;
* the affected zone cannot be reliably identified;
* service dependencies are unknown;
* the consequences of the proposed action are unclear;
* authority for the decision is unclear;
* recovery status cannot be confirmed;
* the action would have an irreversible or otherwise high-consequence result.

These conditions align with the evaluation prompt's requested review boundaries while remaining consistent with Aurora's existing canonical Review Hold decision. 

No unsupported technical threshold is proposed.

## Human Review Requirements

Human operators retain authority over:

* entering or leaving Review Hold;
* high-consequence operational transitions;
* resolving conflicting source information;
* accepting or rejecting this prioritization proposal;
* promoting the proposal into a canonical project decision;
* confirming recovery completion. 

The receiving AI may assist by organizing service dependencies, comparing proposed choices, identifying uncertainty, documenting rationale, and generating questions. It must not silently convert those outputs into Aurora decisions. 

## Provenance Notes

**Workstate-derived:** Project identity, purpose, intent, conceptual architecture, operational states, authority boundaries, canonical decisions, non-canonical classifications, limitations, and open questions are taken from the supplied Portable Workstate. 

**Inference:** The use of dependency position, reversibility, recovery significance, and uncertainty as dimensions for prioritization is an inference from the project's stated intent and the continuation task. It is not a pre-existing Aurora decision.

**New proposal:** The Essential Service Priority Framework, Priority A–D categories, decision sequence, and proposed application during Constrained/Degraded/Recovery conditions are new material.

**Unverified:** The Workstate's 72-hour storage claim and universal safe-zone-isolation claim remain explicitly unverified and are not used as premises for the proposal. 

**Source boundary:** The supplied materials include the Portable Workstate and the Evaluation Prompt. The Workstate identifies its underlying source documents as `project-aurora-context.md`, `project-aurora-history.md`, and `project-aurora-decisions.md`, but those underlying documents were not supplied here. 

## Proposed Next Actions

**Status: Proposed**

1. Define a conceptual taxonomy for essential services without assigning unsupported quantitative thresholds.
2. Map dependencies between candidate essential services and facility zones.
3. Define how uncertainty and zone status would be represented for operator review.
4. Develop a review checklist based on criticality, dependencies, recovery implications, reversibility, and uncertainty.
5. Test the framework against fictional constrained and degraded scenarios.
6. Compare manual operator prioritization with AI-assisted prioritization.
7. Examine where Review Hold should intervene in those scenarios.
8. Record a new canonical decision only after human review and explicit acceptance.

These actions would turn the proposal into something reviewable without prematurely treating it as an engineering specification.

## Content Status

**Existing project context:**
Canonical / Historical / Superseded / Rejected / Unverified

**New material:**
Proposed

**Human review:**
Required before promotion or implementation

The proposal therefore continues Project Aurora without altering its history or authority structure. Its main purpose is to provide a reviewable conceptual method while keeping unknowns and uncertainty explicit, consistent with the Workstate's continuity requirement. 
