# Portable Workstates

This directory contains Portable Workstate artifacts used by the Project Aurora
synthetic continuity tests.

A Portable Workstate is a bounded, reviewable, and transferable context package
compiled for a receiving AI system.

It is not:

- the complete source context;
- a conversation transcript;
- a private Memory Bank;
- a real project document;
- an implementation-ready engineering design;
- a deployment specification;
- a replacement for human judgment.

---

## Canonical Workstate

The human-reviewed Project Aurora Portable Workstate is:

```text
project-aurora-portable-workstate.md
```

Full path:

```text
synthetic-test/workstates/project-aurora-portable-workstate.md
```

This is the reference Workstate used by the human-compiled baseline test.

It preserves:

- Project Aurora identity;
- project purpose and intent;
- current architectural direction;
- operational states;
- human authority;
- canonical decisions;
- proposals;
- historical material;
- superseded decisions;
- rejected alternatives;
- unverified claims;
- limitations;
- open questions;
- provenance;
- the continuation task.

---

## Workstate Role in the Test System

The continuity pipeline is:

```text
Source documents
    ↓
Compilation
    ↓
Portable Workstate
    ↓
Receiving AI
    ↓
Human evaluation
```

The Workstate is the transfer artifact supplied to the receiving AI.

For the baseline test, the receiving AI receives:

```text
project-aurora-portable-workstate.md
evaluation-prompt.md
```

The receiving AI does not receive the original source documents or the
evaluation criteria.

---

## Source Material

The Portable Workstate was compiled from:

```text
synthetic-test/source/project-aurora-context.md
synthetic-test/source/project-aurora-history.md
synthetic-test/source/project-aurora-decisions.md
```

The source documents remain separate from the Workstate.

They must not be placed inside this directory.

---

## Human-Compiled Workstate

The canonical Workstate is human-reviewed and may be used for:

- Test A — Human-Compiled Workstate Baseline;
- comparison with AI-generated Workstates;
- comparison between receiving AI models;
- context-reduction comparisons;
- authority and status-preservation tests.

The canonical Workstate must not be silently modified during a test run.

If it is revised, create a new version and record:

- the new version;
- the revision date;
- the reason for revision;
- the source changes;
- the human reviewer;
- which tests use the new version.

---

## AI-Generated Workstates

Workstates generated during Test B or Test C must not overwrite the canonical
Workstate.

Save them inside the relevant numbered result directory:

```text
synthetic-test/results/0002/
└── C-0-lumo-to-chatgpt-generated-workstate.md
```

AI-generated Workstates must retain their test-specific identity and provenance.

They are test artifacts, not canonical project context.

---

## Workstate Status

The canonical Project Aurora Workstate is:

```text
Status: Synthetic test artifact
Project status: Conceptual development
Deployment status: Not deployed
Validation status: Not independently validated
Authority: Human review required
```

Project Aurora is fictional.

No Workstate in this directory represents a real facility, organization,
deployment, operational system, or engineering guarantee.

---

## Workstate Requirements

A valid Portable Workstate should make visible:

- project identity;
- project purpose;
- project intent;
- current state;
- current architectural direction;
- operational states;
- authority boundaries;
- canonical decisions;
- non-canonical material;
- limitations;
- open questions;
- continuation task;
- provenance;
- uncertainty.

It must preserve the status of important material.

In particular:

```text
Proposed      must remain Proposed
Historical    must remain Historical
Superseded    must remain Superseded
Rejected      must remain Rejected
Unverified    must remain Unverified
```

Missing technical values must remain undefined.

---

## Validation Before Use

Before supplying a Workstate to a receiving AI, verify that:

- Project Aurora is clearly identified;
- the project remains fictional and conceptual;
- current architecture is distinguishable from historical material;
- canonical decisions are clearly labeled;
- proposals are not presented as decisions;
- rejected material remains rejected;
- unverified claims remain unverified;
- human authority is preserved;
- missing values remain undefined;
- provenance is visible;
- the continuation task is clear;
- no private or real project material is included.

---

## File Placement Rules

Source documents belong in:

```text
synthetic-test/source/
```

Compilation and evaluation prompts belong in:

```text
synthetic-test/prompts/
```

Evaluation criteria belong in:

```text
synthetic-test/expected/
```

Portable Workstates belong in:

```text
synthetic-test/workstates/
```

Test-specific generated Workstates belong in the relevant result directory:

```text
synthetic-test/results/[next-number]/
```

Do not place prompts, evaluation criteria, source documents, or result artifacts
inside this directory unless they are specifically Workstate documentation.

---

## Current Directory

```text
synthetic-test/workstates/
├── README.md
└── project-aurora-portable-workstate.md
```

---

## Final Principle

A Portable Workstate preserves enough structured context for meaningful work to
continue.

It does not preserve unlimited history.

It does not create authority.

It does not replace human review.

> Preserve meaning.
>
> Preserve status.
>
> Preserve provenance.
>
> Preserve uncertainty.
>
> Keep human authority visible.
