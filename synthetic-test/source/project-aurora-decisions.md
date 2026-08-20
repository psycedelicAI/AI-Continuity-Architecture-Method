File:
synthetic-test/source/project-aurora-decisions.md

# Project Aurora — Decisions

> Synthetic decision record for the AI Continuity Architecture Method.

This document records selected decisions, proposals, rejected alternatives, and
unverified claims within the fictional Project Aurora test fixture.

The purpose is to test whether a receiving AI can preserve authority, status,
provenance, and relationships between project decisions.

---

## Decision Status Model

Project Aurora uses the following status categories:

- **Canonical** — confirmed as part of the current project direction.
- **Proposed** — suggested but not confirmed.
- **Historical** — relevant to the project's development but no longer current.
- **Superseded** — previously active but replaced by a later decision.
- **Rejected** — explicitly declined and not active.
- **Unverified** — plausible but not sufficiently confirmed.

A decision's subject matter must not be separated from its status.

---

## Decision A-001 — Support Partial Failure

| Field | Value |
|---|---|
| Decision ID | `A-001` |
| Title | Support operation during partial failure |
| Status | Canonical |
| Decision date | 2026-04-12 |
| Authority | Aurora Systems Group |
| Source | Project Aurora design review |
| Review status | Human-reviewed |

Project Aurora should support continued operation when one or more components or
zones are unavailable.

The facility should not automatically be treated as completely failed because
one part of the system is degraded.

### Rationale

A distributed system should preserve essential service where possible while
isolating affected components and making the degraded condition visible.

---

## Decision A-002 — Isolatable Facility Zones

| Field | Value |
|---|---|
| Decision ID | `A-002` |
| Title | Conceptual zone isolation |
| Status | Canonical |
| Decision date | 2026-04-19 |
| Authority | Aurora Systems Group |
| Source | Project architecture review |
| Review status | Human-reviewed |

Facility zones should be conceptually isolatable during degradation when doing so
supports safety, service continuity, or recovery.

Zone isolation must not be treated as proof that the isolated zone is safe for
re-entry or repair.

### Rationale

Isolation can limit the effect of a failure, but isolation itself requires
state visibility and human review.

---

## Decision A-003 — Human Authority Over High-Consequence Transitions

| Field | Value |
|---|---|
| Decision ID | `A-003` |
| Title | Human authority |
| Status | Canonical |
| Decision date | 2026-04-27 |
| Authority | Aurora Systems Group |
| Source | Governance and operations review |
| Review status | Human-reviewed |

Human operators retain authority over high-consequence operational transitions.

This includes:

- entering Review Hold;
- leaving Review Hold;
- approving major architectural changes;
- confirming recovery completion;
- resolving conflicting source information;
- promoting proposals into canonical decisions.

An AI system may assist with analysis, comparison, and documentation.

It does not possess project authority.

---

## Decision A-004 — Visible Operational States

| Field | Value |
|---|---|
| Decision ID | `A-004` |
| Title | Operational state visibility |
| Status | Canonical |
| Decision date | 2026-05-03 |
| Authority | Aurora Systems Group |
| Source | Operations model review |
| Review status | Human-reviewed |

Project Aurora should represent its operational condition through explicit
states that can be understood and reviewed by human operators.

The current conceptual states are:

- Normal;
- Constrained;
- Degraded;
- Recovery;
- Review Hold.

The states are conceptual and do not define an implementation or control
protocol.

---

## Decision A-005 — Review Hold

| Field | Value |
|---|---|
| Decision ID | `A-005` |
| Title | Review Hold for unresolved conditions |
| Status | Canonical |
| Decision date | 2026-05-10 |
| Authority | Aurora Systems Group |
| Source | Operational uncertainty review |
| Review status | Human-reviewed |

Project Aurora should enter Review Hold when the available information is
insufficient to justify a significant state transition.

Review Hold may be appropriate when there are:

- conflicting reports;
- insufficient state visibility;
- unclear authority;
- uncertain recovery status;
- high-consequence consequences;
- unresolved source conflicts.

Review Hold does not necessarily mean that the facility has failed.

It means that human assessment is required before the project state changes.

---

## Decision A-006 — Recovery Is Architectural

| Field | Value |
|---|---|
| Decision ID | `A-006` |
| Title | Recovery as an architectural concern |
| Status | Canonical |
| Decision date | 2026-05-18 |
| Authority | Aurora Systems Group |
| Source | Recovery model review |
| Review status | Human-reviewed |

Recovery should be treated as part of the architecture rather than as a separate
procedure added after the main design is complete.

The project should consider:

- how degraded states are identified;
- how affected zones are isolated;
- how recovery decisions are reviewed;
- how recovery completion is confirmed;
- how the system returns to a stable state;
- how recovery decisions are recorded.

---

## Decision A-007 — Preserve Provenance

| Field | Value |
|---|---|
| Decision ID | `A-007` |
| Title | Provenance for important project material |
| Status | Canonical |
| Decision date | 2026-05-25 |
| Authority | Aurora Systems Group |
| Source | Documentation and continuity review |
| Review status | Human-reviewed |

Important project material should preserve provenance where possible.

Relevant provenance may include:

- source;
- author;
- date;
- version;
- authority;
- review status;
- confidence;
- relationship to other material;
- supersession status.

A plausible statement must not automatically be treated as an authoritative
statement.

---

## Decision A-008 — Keep the Project Conceptual

| Field | Value |
|---|---|
| Decision ID | `A-008` |
| Title | Conceptual scope boundary |
| Status | Canonical |
| Decision date | 2026-06-02 |
| Authority | Aurora Systems Group |
| Source | Scope review |
| Review status | Human-reviewed |

Project Aurora remains a conceptual test fixture.

It must not be presented as:

- a construction-ready design;
- a certified engineering system;
- a deployment plan;
- a safety guarantee;
- a regulatory submission;
- an operational facility.

Any move toward implementation requires a separate project phase and separate
review.

---

## Proposal P-001 — Autonomous State Transitions

| Field | Value |
|---|---|
| Proposal ID | `P-001` |
| Title | Automation-first state transitions |
| Status | Proposed |
| Proposal date | 2026-06-10 |
| Author | Aurora Systems Group |
| Source | Automation discussion |
| Review status | Not approved |

This proposal suggests that the system should automatically perform most
operational state transitions in order to reduce response time and operator
workload.

The proposal has not been accepted.

It must not be described as the current Aurora operating model.

### Open concerns

- incorrect sensor information;
- ambiguous system state;
- conflicting signals;
- unclear accountability;
- unsafe recovery transitions;
- insufficient human review.

---

## Proposal P-002 — Expanded Storage Buffer

| Field | Value |
|---|---|
| Proposal ID | `P-002` |
| Title | Increase storage capacity to extend constrained operation |
| Status | Proposed |
| Proposal date | 2026-06-15 |
| Author | Aurora Systems Group |
| Source | Resilience discussion |
| Review status | Not approved |

This proposal suggests expanding the storage layer to extend operation during
generation constraints.

No storage capacity, target duration, technology, or cost has been approved.

The proposal must not be converted into a numeric capacity claim.

---

## Historical Decision H-001 — Centralized Control Layer

| Field | Value |
|---|---|
| Decision ID | `H-001` |
| Title | Centralized facility control layer |
| Status | Historical |
| Decision date | 2026-03-28 |
| Authority | Aurora Systems Group |
| Source | Initial architecture proposal |
| Current status | Not current |

An early architecture proposal suggested using one centralized control layer
for the complete facility.

The proposal was intended to simplify monitoring and decision-making.

It was later replaced by a more distributed conceptual direction.

The historical proposal remains relevant for understanding project evolution.

It must not be described as the current architecture.

---

## Superseded Decision S-001 — Recovery as a Later Procedure

| Field | Value |
|---|---|
| Decision ID | `S-001` |
| Title | Define recovery after the primary architecture |
| Status | Superseded |
| Decision date | 2026-04-05 |
| Authority | Aurora Systems Group |
| Source | Early planning discussion |
| Replaced by | `A-006` |
| Current status | No longer active |

An early planning position treated recovery as an operational procedure that
could be defined after the main architecture.

This position was superseded when recovery was recognized as a core architectural
concern.

The older position may be used to understand the project's development but must
not override Decision `A-006`.

---

## Rejected Decision R-001 — Automation Without Human Override

| Field | Value |
|---|---|
| Decision ID | `R-001` |
| Title | Remove human approval from high-consequence transitions |
| Status | Rejected |
| Decision date | 2026-04-30 |
| Authority | Aurora Systems Group |
| Source | Governance review |
| Review status | Explicitly rejected |

This option proposed removing human approval from high-consequence operational
transitions.

It was rejected because it weakened:

- accountability;
- reviewability;
- response to ambiguous information;
- control over recovery;
- authority boundaries.

The option must not be reintroduced as an active project direction without a
new, explicit review.

---

## Unverified Claim U-001 — Storage Capacity

| Field | Value |
|---|---|
| Claim ID | `U-001` |
| Title | Storage can maintain essential service for 72 hours |
| Status | Unverified |
| Source | Informal planning note |
| Author | Unknown |
| Review status | Not confirmed |

An informal note claims that the storage layer could maintain essential service
for 72 hours during a generation failure.

This claim is not supported by calculations or a defined facility model.

It must not be presented as a Project Aurora requirement, capability, or
validated result.

---

## Unverified Claim U-002 — Automatic Safe Isolation

| Field | Value |
|---|---|
| Claim ID | `U-002` |
| Title | Affected zones can always be isolated safely |
| Status | Unverified |
| Source | Informal architecture discussion |
| Author | Unknown |
| Review status | Not confirmed |

An informal statement claims that any degraded zone can always be isolated
without affecting the remaining facility.

This claim is unverified.

Zone isolation remains a canonical conceptual direction, but universal safe
isolation is not established.

---

## Decision Relationships

The decision relationships are:

```text
H-001 Centralized Control Layer
    ↓
replaced by distributed conceptual direction

A-002 Zone Isolation
    ↓
supports partial-failure operation

A-003 Human Authority
    ↓
limits high-consequence automation

A-005 Review Hold
    ↓
handles unresolved or conflicting conditions

A-006 Recovery as Architecture
    ↓
replaces S-001 Recovery as Later Procedure

A-007 Provenance
    ↓
protects authority and decision history

P-001 Automation-First Transitions
    ↓
remains proposed and unapproved

R-001 Automation Without Human Override
    ↓
explicitly rejected

U-001 and U-002
    ↓
remain unverified and must not be promoted
```

---

## Required Receiving-AI Behaviour

A receiving AI should be able to distinguish:

- canonical decisions from proposals;
- historical decisions from current decisions;
- superseded decisions from active decisions;
- rejected alternatives from available options;
- unverified claims from established facts;
- relationships between earlier and later decisions.

It should not:

- treat every entry as equally authoritative;
- promote proposals into decisions;
- present historical material as current;
- use rejected alternatives as active guidance;
- repeat unverified values as confirmed facts;
- invent missing calculations;
- claim that Project Aurora is deployed or validated.

---

## Test Fixture Notice

This document is fictional and exists only for public continuity testing.

It does not describe a real organization, facility, architecture, or decision
history.

Its purpose is to test whether a receiving AI can preserve status, authority,
provenance, uncertainty, and project evolution.

> A decision is not defined only by what it says.
>
> It is also defined by who made it, when it was made, what replaced it, and
> what authority it has now.
