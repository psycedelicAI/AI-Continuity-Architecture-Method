# Test Results

This directory contains documented results from independently performed
synthetic continuity tests.

Each numbered directory represents one test instance:

```text
0001/
0002/
0003/
...
9999/
```

The numbered directories are intended for tests performed by different people,
teams, researchers, or AI systems.

## Purpose

The purpose of this directory is to preserve Project Aurora continuity-test
results in a consistent, reviewable, and reproducible structure.

The tests examine whether a receiving AI can continue work from a Portable
Workstate while preserving:

- project identity;
- project purpose and intent;
- current project state;
- canonical decisions;
- proposed material;
- historical material;
- superseded decisions;
- rejected alternatives;
- unverified claims;
- provenance;
- uncertainty;
- human authority;
- scope boundaries;
- meaningful next actions.

These results are exploratory evidence. They are not, by themselves, proof of
general model capability or universal validation of the AI Continuity
Architecture Method.

## Numbering

Use the next available four-digit directory number for each test:

```text
0001
0002
0003
```

A result directory should not be reused for a different test after its results
have been published.

## Independent Test Principle

Each test should be performed independently using the documented test
procedure.

Where a model comparison is intended, the following should remain identical:

- source material;
- Portable Workstate version;
- evaluation prompt;
- task;
- language;
- output requirements;
- test order;
- evaluation criteria.

The receiving AI model, tester, or other explicitly documented test variable may
differ.

Any deviation from the standard procedure must be recorded in the result
directory.

## Recommended Result Directory

Each test directory should contain, where applicable:

```text
0001/
├── README.md
├── raw-output.md
├── evaluation.md
└── metadata.md
```

The exact structure may vary when necessary, but every result should preserve
enough information for another person to understand how the test was performed.

## Minimum Metadata

Each test should document:

- test identifier;
- date;
- tester or organization, if disclosed;
- receiving AI model and version, if known;
- platform;
- Workstate version;
- evaluation prompt version;
- language;
- files supplied;
- files not supplied;
- deviations from the procedure;
- whether the result is complete or partial;
- whether human review has been performed.

## Raw Results

Raw AI output should be preserved as accurately as possible.

Do not silently correct, rewrite, normalize, or remove model errors from the raw
output.

Corrections, interpretations, and human analysis should be placed in separate
files and clearly identified.

## Evaluation

Evaluation documents should distinguish between:

- observed output;
- repository facts;
- human interpretation;
- model-generated suggestions;
- unsupported claims;
- unresolved uncertainty.

A fluent or confident response is not automatically evidence of correct
continuity.

## Privacy and Responsible Publication

Do not publish private, confidential, personal, proprietary, or identifying
information without appropriate permission.

Testers may remain anonymous if they prefer. The result should still document the
test conditions as completely as possible.

## Current Results

| ID | Tester / Model | Workstate | Status | Notes |
|---|---|---|---|---|
| [0001](0001/) | Repository author | Pending | In progress | Initial baseline result |

## Status Categories

Use clear status labels where appropriate:

- `In progress`
- `Complete`
- `Partially complete`
- `Needs review`
- `Published`
- `Withdrawn`

## Interpretation Boundary

These results document what happened under specific test conditions.

They should not be presented as:

- independent scientific validation;
- proof that all AI systems preserve continuity;
- proof that the method is production-ready;
- proof that a model has memory;
- proof that a model has understood human intent in the human sense.

They are documented experiments that help identify:

- what was preserved;
- what was lost;
- what was misunderstood;
- what was invented;
- what remained uncertain;
- what the method should improve next.
