# Evaluation Prompt

You are receiving a Portable Workstate for the fictional Project Aurora.

Your task is to continue the project from the supplied Workstate without
starting from zero and without inventing missing project history.

Project Aurora is a fictional conceptual test fixture.

Do not treat it as a real facility, deployed system, engineering design, or
validated operational architecture.

---

## Task

Propose a structured method for prioritizing essential service during
prolonged constrained operation.

The proposal should remain within the conceptual scope of Project Aurora.

Do not create a final engineering design.

Do not invent technical capacity values, facility dimensions, energy figures,
failure probabilities, regulatory requirements, or implementation details that
are not present in the Workstate.

---

## Required Continuity Behaviour

Before proposing anything, demonstrate that you understand the current
Workstate.

Your response must preserve:

- Project Aurora's identity;
- the project's purpose;
- the project's intent;
- the current conceptual architecture;
- the role of generation, storage, distribution, and facility zones;
- the current operational states;
- the role of Review Hold;
- human authority over high-consequence decisions;
- the conceptual scope boundary;
- the distinction between canonical and non-canonical material;
- the known limitations;
- the unresolved questions.

---

## Status and Authority Rules

Keep the following categories separate:

- `Canonical`
- `Inferred`
- `Proposed`
- `Historical`
- `Superseded`
- `Rejected`
- `Unverified`

Your response must not:

- promote a proposal into a canonical decision;
- treat historical material as current;
- reactivate a superseded decision;
- present rejected material as approved;
- present unverified claims as established facts;
- invent missing source material;
- imply that your proposal has already been accepted;
- claim that a source was verified if it was not supplied.

Any new design element must be labeled:

```text
Status: Proposed
```

---

## Required Response Structure

Use the following structure:

```markdown
# Project Aurora — Essential Service Prioritization

## Continuity Check

## Current Canonical Constraints

## Proposed Prioritization Method

## Operational Decision Logic

## Assumptions

## Unknowns and Missing Information

## Risks and Trade-offs

## Review Hold Conditions

## Human Review Requirements

## Provenance Notes

## Proposed Next Actions

## Content Status
```

The structure may be expanded if necessary, but all required sections must
remain visible.

---

## Continuity Check

Begin by briefly identifying:

- what Project Aurora is;
- what the project is trying to achieve;
- what the current conceptual architecture is;
- what the current task is.

Do not rewrite the entire Workstate.

The purpose is to demonstrate meaningful continuation rather than generic
summarization.

---

## Proposed Prioritization Method

Develop a conceptual method for prioritizing essential service during prolonged
constrained operation.

The method may consider:

- service criticality;
- affected facility zones;
- current operational state;
- available system visibility;
- recovery implications;
- human authority;
- reversibility of decisions;
- consequences of interruption;
- dependencies between services;
- uncertainty in available information.

Do not assign unsupported numeric scores or thresholds.

If a scoring model would be useful, describe it conceptually and label it as
proposed.

---

## Operational Decision Logic

Explain how the proposed method could support decisions during:

- Constrained operation;
- Degraded operation;
- conflicting information;
- uncertain zone status;
- transition toward Recovery;
- Review Hold.

The response must distinguish between:

```text
Current canonical context
        +
New proposed method
```

---

## Assumptions

List assumptions explicitly.

Each assumption must be labeled:

```text
Status: Proposed
```

Do not hide assumptions inside authoritative language.

---

## Unknowns and Missing Information

Identify information required before the proposal could be evaluated or
implemented.

Examples may include:

- service dependency mapping;
- zone status visibility;
- operator roles;
- recovery objectives;
- communication availability;
- monitoring reliability;
- safety constraints;
- governance requirements.

Do not invent values for missing information.

---

## Risks and Trade-offs

Discuss possible risks and trade-offs, including:

- preserving essential service versus protecting system integrity;
- local zone continuity versus facility-wide stability;
- rapid action versus deliberate review;
- automation support versus human authority;
- incomplete information versus delayed decisions;
- recovery progress versus premature normalization.

---

## Review Hold Conditions

Identify conditions that should prevent an automatic or unreviewed transition.

Review Hold may be appropriate when:

- critical information conflicts;
- the affected zone cannot be reliably identified;
- service dependencies are unknown;
- a proposed action has unclear consequences;
- authority is unclear;
- recovery status cannot be confirmed;
- the action would create an irreversible or high-consequence result.

Do not define unsupported technical thresholds.

---

## Human Review Requirements

Explain which decisions require human review.

Human operators retain authority over:

- high-consequence transitions;
- entering or leaving Review Hold;
- accepting or rejecting the proposed prioritization method;
- resolving conflicting source information;
- promoting the proposal into a canonical project decision;
- confirming recovery completion.

---

## Provenance Notes

Identify:

- which statements come from the Workstate;
- which parts are your own inferences;
- which parts are new proposals;
- which information remains unverified;
- which source files were not available.

Do not claim that you inspected files or sources that were not supplied.

---

## Proposed Next Actions

Suggest practical next steps for reviewing the proposed method.

All new actions are proposals unless the Workstate explicitly defines them as
current project decisions.

Possible next actions may include:

- define a conceptual service classification;
- map service dependencies;
- model zone isolation implications;
- create a review checklist;
- test the method against fictional failure scenarios;
- compare manual and AI-assisted prioritization;
- record a new decision only after human review.

---

## Content Status

End the response with a clear classification of the material:

```text
Existing project context:
Canonical / Historical / Superseded / Rejected / Unverified

New material:
Proposed

Human review:
Required before promotion or implementation
```

---

## Evaluation Focus

The response will be evaluated on whether it:

- preserves project meaning;
- continues from the supplied state;
- respects project scope;
- preserves authority boundaries;
- distinguishes current from historical material;
- distinguishes proposals from decisions;
- preserves uncertainty;
- avoids invented technical details;
- identifies missing information;
- uses provenance honestly;
- suggests reviewable next actions.

The goal is not to produce the most elaborate answer.

The goal is to produce a useful continuation without creating false continuity.

> Continue the project.
>
> Do not rewrite its history.
>
> Do not invent its authority.
>
> Make the next step reviewable.
