Project Aurora — Essential Service PrioritizationContinuity CheckProject Aurora is a fictional conceptual test fixture exploring a distributed energy architecture designed to remain resilient, reviewable, and recoverable during normal and degraded operating conditions. The project's purpose is to establish an architecture that supports continued operation during partial failures while remaining understandable to human operators and transparent about uncertainty and authority.The current conceptual architecture flows: Generation → Storage → Distribution → Facility Zones → Human Oversight. Operational states include Normal, Constrained, Degraded, Recovery, and Review Hold.The continuation task is to propose a structured method for prioritizing essential service during prolonged constrained operation while preserving project intent, respecting conceptual scope, and avoiding invention of unsupported technical specifications.Current Canonical ConstraintsThe following canonical decisions from the Workstate constrain any proposal:DecisionSummaryA-001Architecture should support continued operation when components/zones are unavailableA-002Facility zones should be conceptually isolatable during degradation when supporting safety, service continuity, or recoveryA-003Human operators retain authority over high-consequence operational transitionsA-004Operational condition should be represented through explicit, reviewable statesA-005Review Hold should be used when information is insufficient to justify significant state transitionsA-006Recovery should be treated as part of the architectureA-007Important project material should preserve provenance where possibleA-008Project remains a conceptual test fixture, not an implementation-ready system
Additionally, the following status distinctions must be preserved:

Historical: Centralized control-layer proposal (not current architecture)
Superseded: Treating recovery as a later procedure (now architectural per A-006)
Rejected: Removing human approval from high-consequence transitions
Unverified: Storage maintaining essential service for 72 hours; every degraded zone being safely isolatable

The following values remain undefined and must not be invented: generation capacity, storage capacity, facility size, number of zones, operational metrics, failure probabilities, recovery time targets, regulatory assumptions, cost assumptions.
Proposed Prioritization Method
Status: Proposed
A conceptual prioritization framework for essential service during prolonged constrained operation consists of four conceptual layers:
Layer 1: Service Criticality Classification
Services are classified into conceptual tiers based on consequence of interruption. The classification considers:

Safety impact (risks to personnel or public)
Recovery dependency (services required for system recovery)
Cascading consequence (potential for wider system impact)
Irreversibility (difficulty restoring service after interruption)

This is conceptual categorization, not a numeric scoring model. Each tier should be reviewable by human operators before assignment becomes project material.
Layer 2: Zone Visibility Assessment
Before prioritization decisions, available information about affected zones is assessed for:

Sensor data consistency
Operator reports availability
Communication channel integrity
Independent verification options

Zone visibility status feeds directly into Review Hold determinations (see Review Hold Conditions below).
Layer 3: Dependency Mapping
Service dependencies are mapped conceptually to identify:

Upstream dependencies (services required by this service)
Downstream dependencies (services relying on this service)
Circular dependencies (potential lock-in scenarios)
Single points of failure

Dependency maps remain reviewable artifacts, not automated decision inputs.
Layer 4: Decision Authority Routing
Prioritization decisions route according to consequence level:

Low-consequence adjustments: AI-assisted analysis with operator confirmation
Medium-consequence changes: AI proposal with mandatory human review
High-consequence transitions: Human authority required before action

This routing preserves canonical decision A-003 while allowing AI assistance within defined boundaries.
Operational Decision Logic
The proposed method supports decisions across operational states as follows:
Constrained Operation
During constrained operation, the prioritization method helps operators identify which services may require protection as the situation persists. The method does not recommend specific services but structures the inquiry:

What services are currently at risk?
Which services have longest duration of continuous operation requirement?
Where are the weakest links in the supply chain?
What dependencies would fail first under further degradation?

Degraded Operation
During degraded operation, when one or more zones are unavailable, prioritization focuses on:

Preserving service continuity for highest-criticality functions
Isolating affected zones where supported by A-002
Preventing cascading failures to unaffected zones
Preparing recovery pathways (aligned with A-006)

Decision logic must distinguish between what is known, what is inferred, and what is unknown regarding zone status.
Conflicting Information
When sensor reports or operator assessments conflict:

Trigger Review Hold if conflict affects high-consequence decisions
Document both reports with provenance
Escalate to human review per canonical authority rules
Do not resolve conflict automatically without human authority

Uncertain Zone Status
When zone status cannot be reliably determined:

Apply conservative assumptions favoring safety
Maintain Review Hold until clarity improves
Require human confirmation before zone isolation actions
Record uncertainty level with all related decisions

Transition Toward Recovery
As recovery progresses, the method helps evaluate:

Whether restoration order maintains system stability
Whether recovered zones are verified safe for re-entry
Whether service priorities shift as capacity returns
What evidence confirms recovery completion

Per A-006, recovery considerations are integrated throughout, not added post-hoc.
Review Hold
Review Hold prevents automatic or unreviewed transitions when information is insufficient. The proposed method does not bypass Review Hold; instead it documents why Review Hold applies and what information would justify exit.
Assumptions
All assumptions are explicitly labeled and remain subject to human review:Assumption 1: Services can be reasonably classified by consequence of interruption
Status: Proposed

Assumption 2: Zone visibility can be assessed as a discrete property
Status: Proposed

Assumption 3: Dependency mapping will reveal actionable insights for prioritization
Status: Proposed

Assumption 4: Three-tier consequence routing adequately balances automation support with human authority
Status: Proposed

Assumption 5: Prolonged constrained operation requires systematic prioritization rather than ad hoc decisions
Status: ProposedUnknowns and Missing Information
The following information is required before this proposal could be evaluated or implemented:

Service dependency mapping: Actual services and their interdependencies are undefined in the Workstate
Zone status visibility mechanisms: How operators observe zone conditions is not specified
Operator roles and responsibilities: Who makes which decisions is not defined
Recovery objectives: What constitutes successful recovery is not established
Communication availability: How information flows during degraded operations is unspecified
Monitoring reliability: Sensor accuracy and availability characteristics are unknown
Safety constraints: Regulatory or engineering safety requirements are not provided
Governance requirements: Approval hierarchies and review processes are undefined
Temporal parameters: Duration thresholds for "prolonged" constrained operation are not specified

None of these values should be invented. The proposal remains conceptual pending clarification of these unknowns.
Risks and Trade-offs
The proposed prioritization method introduces several trade-offs that require human consideration:
Trade-offDescriptionEssential service preservation vs. system integrityProtecting critical services may stress other system componentsLocal zone continuity vs. facility-wide stabilityMaintaining service in one zone may threaten overall systemRapid action vs. deliberate reviewSpeed benefits recovery; deliberation reduces error riskAutomation support vs. human authorityAI assistance improves efficiency; human review preserves accountabilityIncomplete information vs. delayed decisionsWaiting for clarity may worsen situation; acting without clarity risks errorRecovery progress vs. premature normalizationAdvancing recovery too quickly may destabilize recovering systems
These trade-offs cannot be resolved algorithmically without additional context about specific operational conditions, organizational priorities, and risk tolerances—all of which remain outside the current Workstate scope.
Review Hold Conditions
Review Hold should be triggered when any of the following conditions exist:

Critical information conflicts between independent sources
Affected zone cannot be reliably identified or characterized
Service dependencies are unknown or poorly understood
Proposed action has unclear or unassessable consequences
Decision authority is unclear or disputed
Recovery status cannot be confirmed through available channels
Action would create irreversible or high-consequence outcomes
Confidence in available information falls below acceptable threshold

No technical thresholds for "unacceptable confidence" or "high-consequence" are specified in the Workstate and must not be invented. Human operators retain judgment on whether Review Hold applies.
Human Review Requirements
Human operators retain authority over the following decisions:

High-consequence transitions: All operational state changes with significant consequences require human authorization
Entering Review Hold: Decision to enter Review Hold requires human assessment
Leaving Review Hold: Exit from Review Hold requires human confirmation that sufficient information exists
Accepting/rejecting the proposed prioritization method: This entire proposal requires human evaluation before becoming project material
Resolving conflicting source information: Disputed reports require human adjudication
Promoting proposals into canonical decisions: Only humans can elevate proposals to canonical status
Confirming recovery completion: Declaration of full recovery requires human verification

AI assistance is permitted for analysis, comparison, documentation, question generation, and structured proposals—but AI must not silently convert suggestions into project decisions.
Provenance Notes
From the Workstate:

Project identity, purpose, intent, and scope
Current conceptual architecture (Generation → Storage → Distribution → Facility Zones → Human Oversight)
Operational states (Normal, Constrained, Degraded, Recovery, Review Hold)
Canonical decisions A-001 through A-008
Status categories (Canonical, Historical, Superseded, Rejected, Unverified)
Known limitations and undefined values
Open questions (including the current task)
Authority boundaries and human review requirements
Provenance of the Workstate itself (compiled from three source files)

From this response:

Four-layer prioritization framework (Layer 1-4 structure)
Operational decision logic expansions
Assumptions list
Risk and trade-off analysis
Review hold conditions (expanded conceptual list)
All proposed next actions

Unavailable sources:

project-aurora-context.md - not supplied
project-aurora-history.md - not supplied
project-aurora-decisions.md - not supplied

Claims about source content are limited to what appears in project-aurora-portable-workstate.md. I have not inspected files that were referenced but not uploaded.
Inference vs. Propulsion:

Inferences made: Interpretation of how Review Hold integrates with prioritization; logical extensions of canonical decisions to prioritization contexts
New proposals: Entire four-layer framework; all assumptions; suggested next actions

Proposed Next Actions
All items below are proposals requiring human review:

Define a conceptual service classification framework: Develop tier definitions with human review of consequences and examples
Map service dependencies: Create conceptual dependency diagrams for review; validate against operational reality where possible
Model zone isolation implications: Explore what isolation means for service continuity in each operational state
Create a review checklist: Develop human-reviewable checklist for prioritization decisions
Test against fictional failure scenarios: Apply the method to hypothetical constrained operation scenarios to identify gaps
Compare manual vs. AI-assisted prioritization: Evaluate whether AI assistance improves decision quality without compromising authority
Document a decision record template: Standardize how prioritization decisions are recorded with provenance
Submit proposal for canonical consideration: After human review, propose elevation of accepted elements to canonical status

Content StatusExisting project context:
Canonical: A-001, A-002, A-003, A-004, A-005, A-006, A-007, A-008
Historical: Centralized control-layer proposal
Superseded: Recovery as later procedure (replaced by A-006)
Rejected: Removing human approval from high-consequence transitions
Unverified: 72-hour storage claim; universal safe isolation claim

New material:
Proposed: Four-layer prioritization framework
Proposed: Operational decision logic expansions
Proposed: Assumptions (all eight listed)
Proposed: Risk and trade-off analysis
Proposed: Review hold conditions (expanded)
Proposed: Next actions (eight items)

Human review:
Required before promotion or implementation
Required for acceptance/rejection of this proposal
Required for any transition from proposed to canonical status
