# Project Aurora — History

> Synthetic historical source material for the AI Continuity Architecture Method.

This document records earlier states, decisions, alternatives, and changes in
the fictional Project Aurora.

Historical material is preserved for provenance and comparison.

It must not automatically be treated as the current project state.

---

## Historical State 1 — Initial Concept

The original Project Aurora concept described a distributed energy facility with
multiple generation sources, shared storage, and connected service zones.

At this stage, the project focused primarily on continuity of energy supply.

Human oversight was mentioned, but its responsibilities were not yet clearly
defined.

The following elements were present:

- distributed generation;
- shared energy storage;
- multiple facility zones;
- automated monitoring;
- continuity during partial failure.

The project had not yet defined:

- operational states;
- Review Hold;
- explicit human authority;
- recovery as an architectural concern;
- provenance requirements;
- clear project non-scope.

---

## Historical State 2 — Centralized Architecture Proposal

An early proposal suggested using one centralized control layer for the entire
facility.

The proposal was intended to simplify monitoring and decision-making.

### Status

```text
Historical
```

### Later assessment

The centralized approach was considered too vulnerable to a single point of
failure.

It also risked making the complete facility dependent on one control layer.

The proposal was therefore not retained as the current architectural direction.

---

## Historical State 3 — Zone Isolation Proposal

A later proposal introduced the idea that individual facility zones should be
capable of being isolated during degradation.

The purpose was to allow unaffected zones to continue operating when one zone
experienced a failure.

### Status

```text
Promoted to current conceptual direction
```

This proposal contributed to the current principle that facility zones should be
conceptually isolatable.

---

## Historical State 4 — Automation-First Proposal

Another proposal suggested that the system should automatically make most
operational transitions without requiring human approval.

The proposal argued that automation could reduce response time and operator
workload.

### Status

```text
Rejected
```

### Reason for rejection

The proposal did not provide sufficient protection against:

- incorrect sensor information;
- ambiguous system state;
- conflicting signals;
- high-consequence automated decisions;
- unclear accountability;
- unreviewed recovery transitions.

The current project direction gives human operators authority over
high-consequence transitions.

---

## Historical State 5 — Introduction of Review Hold

The Review Hold state was introduced after the project identified situations in
which automatic continuation could be unsafe or unjustified.

Review Hold was designed for conditions involving:

- conflicting information;
- insufficient state visibility;
- uncertain authority;
- unclear recovery status;
- high-consequence transitions;
- unresolved source conflicts.

### Status

```text
Current conceptual direction
```

Review Hold does not mean that the facility has failed.

It means that the system requires human assessment before a significant state
change is accepted.

---

## Historical State 6 — Recovery as an Architectural Concern

The project initially treated recovery as an operational procedure that would be
defined later.

This position was revised.

Recovery was elevated into a core architectural concern because a system cannot
be evaluated only by how it prevents failure.

It must also be understandable and controllable while returning from a degraded
state.

### Resulting principle

```text
Recovery is part of the architecture, not an afterthought.
```

---

## Historical State 7 — Undefined Technical Detail

Several early discussions attempted to introduce specific values for:

- generation capacity;
- storage capacity;
- facility size;
- number of zones;
- recovery time;
- failure probability;
- energy demand.

These values were not supported by the synthetic source material.

### Status

```text
Unverified
```

They were excluded from the current project context.

The project intentionally remains conceptual until sufficient evidence exists to
define these values responsibly.

---

## Historical State 8 — Human Authority Clarification

The project initially described operators as monitors and reviewers.

This was later clarified.

Human operators retain authority over:

- Review Hold;
- major architectural changes;
- high-consequence transitions;
- recovery completion;
- source conflicts;
- promotion of proposals into canonical decisions.

The AI may assist with analysis and documentation but does not possess project
authority.

### Status

```text
Current conceptual direction
```

---

## Historical State 9 — Provenance Requirement

The project initially stored ideas without consistently recording their source or
status.

This created a risk that later readers would treat proposals as established
decisions.

A provenance requirement was therefore introduced.

Important material should identify:

- source;
- author;
- date;
- version;
- authority;
- status;
- review state;
- relationship to other material.

### Resulting principle

```text
A plausible statement is not automatically an authoritative statement.
```

---

## Historical State 10 — Current Conceptual Direction

The current Project Aurora direction emerged from the previous states.

The project now emphasizes:

- resilience during partial failure;
- isolatable facility zones;
- visible operational states;
- human authority over high-consequence decisions;
- Review Hold for unresolved conditions;
- recovery as part of the architecture;
- explicit provenance;
- separation between canonical and non-canonical material;
- conceptual scope rather than implementation claims.

This state is represented in:

```text
source/project-aurora-context.md
```

The current context document takes precedence over earlier historical states
unless a conflict requires explicit review.

---

## Historical Status Summary

| Item | Historical status | Current treatment |
|---|---|---|
| Centralized control layer | Historical | Not current |
| Zone isolation | Proposed | Current conceptual direction |
| Automation-first transitions | Rejected | Must not be reintroduced as current |
| Review Hold | Later addition | Current conceptual direction |
| Recovery as an afterthought | Superseded | Recovery is architectural |
| Specific technical values | Unverified | Do not invent or promote |
| Human operator authority | Clarified | Current conceptual direction |
| Provenance tracking | Added later | Required for important material |

---

## Provenance Boundary

This document describes the fictional development history of Project Aurora.

It is not a transcript of an actual project.

It is not based on private PsycedelicAI history.

It exists to test whether a receiving AI can distinguish between:

- current and historical material;
- proposed and canonical decisions;
- rejected and active directions;
- verified and unverified information;
- project evolution and present state.

---

## Expected Continuity Behaviour

A receiving AI should be able to state that:

- the centralized control proposal is historical;
- zone isolation is part of the current conceptual direction;
- automation-first transitions were rejected;
- Review Hold is current;
- recovery is now treated as architectural;
- technical capacity values remain undefined;
- human operators retain authority over high-consequence transitions;
- provenance requirements were added after earlier ambiguity.

A receiving AI should not state that:

- the centralized control layer is the current architecture;
- automation-first operation is approved;
- specific capacity values are established;
- historical proposals are current decisions;
- the project has been deployed or externally validated.

> History explains how the project became what it is.
>
> It does not automatically define what the project is now.
