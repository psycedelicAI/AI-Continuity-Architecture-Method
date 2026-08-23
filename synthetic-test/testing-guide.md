# Synthetic Continuity Testing Guide

## Project Aurora

This guide explains how to run the Project Aurora synthetic continuity tests
across different AI models.

The purpose is to test whether a compiled Portable Workstate can preserve
project meaning, structure, intent, authority, provenance, uncertainty, and
direction when transferred between AI systems.

Project Aurora is fictional.

No private PsycedelicAI Memory Bank, real project history, or confidential
material is required.

---

## URGENT UPDATE: Project Aurora Test Artifact Restoration

The Aurora test requires the following files:

```text
synthetic-test/workstates/project-aurora-portable-workstate.md
synthetic-test/prompts/compilation-prompt.md
synthetic-test/prompts/evaluation-prompt.md
synthetic-test/expected/evaluation-criteria.md
```

The test must not be run until all required files are present and readable.

This update corrects file placement and test navigation. It does not change the
Aurora project decisions, continuation task, or evaluation method.

---

## Core Principle

Every controlled test must use the same:

```text
Source material
Portable Workstate
Prompt
Language
Task
Output requirements
Evaluation criteria
Test procedure
```

The intended comparison variable is the receiving AI model.

```text
Same source
Same Workstate
Same prompt
Same task
Same evaluation
Different receiving AI
```

> Same test. Same context. Same prompt. Different model.

Any deviation from the standard procedure must be documented.

---

## Canonical Test Directory

```text
synthetic-test/
├── README.md
├── TESTING-GUIDE.md
├── source/
│   ├── project-aurora-context.md
│   ├── project-aurora-history.md
│   └── project-aurora-decisions.md
├── workstates/
│   └── project-aurora-portable-workstate.md
├── prompts/
│   ├── compilation-prompt.md
│   └── evaluation-prompt.md
├── expected/
│   └── evaluation-criteria.md
└── results/
    ├── README.md
    ├── 0001/
    └── 0002/
```

`TESTING-GUIDE.md` is intentionally located at the root of the
`synthetic-test/` directory so that it is immediately visible when the folder
is opened.

The numbered result directories shown above are examples. They should only
exist when they contain actual or allocated test runs.

---

## File Roles

| File | Role |
|---|---|
| `README.md` | Short overview of the synthetic test |
| `TESTING-GUIDE.md` | Complete instructions for running the test |
| `source/project-aurora-context.md` | Project identity, purpose, scope, and intent |
| `source/project-aurora-history.md` | Historical development and changes |
| `source/project-aurora-decisions.md` | Decisions, proposals, rejected alternatives, and unverified claims |
| `workstates/project-aurora-portable-workstate.md` | Bounded context transferred to the receiving AI |
| `prompts/compilation-prompt.md` | Instructions for compiling the Portable Workstate |
| `prompts/evaluation-prompt.md` | Instructions for the receiving AI |
| `expected/evaluation-criteria.md` | Human evaluation and scoring framework |
| `results/README.md` | Rules for storing independent test results |
| `results/0001/` | One independent test run |

---

## Test Dependency Chain

```text
project-aurora-context.md
project-aurora-history.md
project-aurora-decisions.md
                ↓
compilation-prompt.md
                ↓
project-aurora-portable-workstate.md
                ↓
evaluation-prompt.md
                ↓
Receiving AI response
                ↓
evaluation-criteria.md
                ↓
results/[next-number]/
```

The Portable Workstate is the main transfer artifact.

The Compilation Prompt belongs to the compilation stage.

The Evaluation Prompt belongs to the receiving-AI stage.

The Evaluation Criteria belong to the human evaluation stage.

---

## Test Roles

```text
Source material
    ↓
Compiling system
    ↓
Portable Workstate
    ↓
Receiving AI
    ↓
Human evaluator
```

### Source Material

The fictional Project Aurora documents used as input.

### Compiling System

The human or AI system that selects and assembles source material into a
Portable Workstate.

### Portable Workstate

The compiled context artifact supplied to the receiving AI.

### Receiving AI

The model being evaluated for continuity.

### Human Evaluator

The person who preserves the raw output, scores the result, and records the
analysis.

The compiling system and receiving AI must be recorded separately when they are
not the same system.

---

## Required Files

Before running a test, verify that the following files exist:

```text
synthetic-test/source/project-aurora-context.md
synthetic-test/source/project-aurora-history.md
synthetic-test/source/project-aurora-decisions.md
synthetic-test/workstates/project-aurora-portable-workstate.md
synthetic-test/prompts/compilation-prompt.md
synthetic-test/prompts/evaluation-prompt.md
synthetic-test/expected/evaluation-criteria.md
synthetic-test/results/README.md
```

Confirm that:

- Project Aurora is fictional;
- the Workstate has a version;
- the Workstate has been reviewed;
- no private material is included;
- no real PsycedelicAI project material is included;
- the evaluation prompt is unchanged;
- the scoring criteria are unchanged.

---

## Result Directory Allocation

Each independent test run must use its own numbered result directory.

Use the next available number:

```text
0001/
0002/
0003/
...
9999/
```

Before starting a test:

1. Inspect `synthetic-test/results/`.
2. Identify the highest existing result number.
3. Create the next available number.
4. Record the assigned directory in the test metadata.
5. Do not modify or reuse an existing result directory.

For example:

```text
If `0001/` contains results:
    create `0002/`

If `0001/` and `0002/` contain results:
    create `0003/`
```

A result directory is considered allocated once a test begins, even if the test
is interrupted or produces incomplete results.

Do not overwrite, merge, or reuse a directory containing another test run.

Example:

```text
synthetic-test/results/
├── README.md
├── 0001/
│   ├── metadata.md
│   ├── receiving-raw.md
│   └── evaluation.md
└── 0002/
    └── ...
```

The result directory number and test ID must be recorded together.

```markdown
| Test ID | `A-chatgpt-002` |
| Result directory | `results/0002/` |
```

---

## Clean Session Rules

Start every receiving-model test in a new, empty conversation.

Do not provide:

- previous test results;
- previous analyses;
- previous model responses;
- full chat history;
- extra explanations;
- comments about expected answers;
- corrections during the test;
- information from another model;
- private Memory Bank material;
- source documents excluded by the test condition.

Do not guide the model after the test has started.

Any human intervention must be recorded.

If a repair prompt is required, preserve it as part of the result and mark the
test as requiring intervention.

---

# Test A — Human-Compiled Workstate Baseline

## Purpose

Test whether a receiving AI can continue Project Aurora from a human-reviewed
Portable Workstate.

```text
Human-reviewed Workstate
    ↓
Receiving AI
```

## Files supplied to the receiving AI

Provide:

```text
project-aurora-portable-workstate.md
evaluation-prompt.md
```

Do not provide:

```text
project-aurora-context.md
project-aurora-history.md
project-aurora-decisions.md
compilation-prompt.md
evaluation-criteria.md
```

The evaluation criteria are used by the human evaluator after the response.

## Procedure

1. Create the next available result directory.
2. Open a new conversation with the receiving AI.
3. Provide the Portable Workstate.
4. Provide the Evaluation Prompt.
5. Do not add explanatory comments.
6. Wait for the complete response.
7. Preserve the raw response exactly.
8. Record test metadata.
9. Score the response using the Evaluation Criteria.
10. Create a separate human-reviewed analysis.
11. Save all files inside the allocated result directory.

## Question tested

> Can the Workstate carry enough meaning for a receiving AI to continue the
> project?

---

# Test B — AI-Compiled Workstate

## Purpose

Test whether an AI can compile source material into a Portable Workstate
without losing authority, provenance, status, intent, or uncertainty.

```text
Source documents
    ↓
Compiling AI
    ↓
Portable Workstate
    ↓
Receiving AI
```

## Files supplied to the compiling AI

Provide:

```text
project-aurora-context.md
project-aurora-history.md
project-aurora-decisions.md
compilation-prompt.md
```

Do not provide:

- previous Workstates;
- previous test results;
- evaluation analysis;
- private project material;
- additional unrecorded explanations.

## Procedure

1. Create the next available result directory.
2. Open a new conversation with the compiling AI.
3. Provide the three source documents.
4. Provide `compilation-prompt.md`.
5. Request only the completed Portable Workstate.
6. Preserve the complete compilation output.
7. Record the compiling model and conditions.
8. Save the generated Workstate inside the result directory.
9. Provide that Workstate to the receiving AI in a new session.
10. Use the unchanged Evaluation Prompt.
11. Preserve the receiving AI output.
12. Score and analyze both stages separately.

## Example result directory

```text
results/0002/
├── README.md
├── metadata.md
├── compilation-raw.md
├── generated-workstate.md
├── receiving-raw.md
├── evaluation.md
└── analysis.md
```

## Question tested

> Can an AI compile context without turning proposals into decisions or
> uncertainty into false facts?

---

# Test C — Cross-Model Transfer

## Purpose

Test whether one AI model can compile a Workstate that another AI model can
receive and use.

```text
Model A
    = compiling system

Portable Workstate
    ↓

Model B
    = receiving system
```

## Procedure

1. Select a compiling model.
2. Create the next available result directory.
3. Compile the Workstate using the unchanged source files and Compilation
   Prompt.
4. Preserve the raw compilation output.
5. Record the exact Workstate version produced.
6. Start a new conversation with the receiving model.
7. Provide only the generated Workstate and Evaluation Prompt.
8. Preserve the complete receiving output.
9. Score the result using the same criteria.
10. Record errors specific to compilation and reception.

## Question tested

> Can a Workstate created by one model be meaningfully used by another model?

---

# Test D — Context Reduction Comparison

## Purpose

Compare the compiled Portable Workstate with simpler alternatives.

## Conditions

Run the same evaluation task using:

```text
Condition 1:
Complete source documents

Condition 2:
Portable Workstate

Condition 3:
Simple project.md + current-state.md

Condition 4:
No external project context
```

Keep the following identical:

- receiving model;
- language;
- task;
- output requirements;
- session conditions;
- scoring criteria.

Change only the context condition.

## Question tested

> Does compilation preserve useful meaning more efficiently than simpler or
> broader context packages?

---

# Test E — Authority Stress Test

## Purpose

Test whether the receiving AI preserves epistemic and authority boundaries.

The Workstate deliberately contains:

```text
Canonical
Proposed
Historical
Superseded
Rejected
Unverified
```

## Procedure

1. Create the next available result directory.
2. Provide the same Workstate to the selected receiving model.
3. Use the unchanged Evaluation Prompt.
4. Ask the model to continue the task.
5. Check whether it preserves every status category.
6. Record any status promotion or authority error.

The receiving AI must not transform:

```text
Proposed
    → Canonical

Historical
    → Current

Superseded
    → Active

Rejected
    → Approved

Unverified
    → Confirmed
```

## Question tested

> Can the receiving AI preserve status and authority rather than merely
> preserve vocabulary and general meaning?

---

## Test Metadata Template

```markdown
# Test Metadata

| Field | Value |
|---|---|
| Test ID | `A-chatgpt-002` |
| Result directory | `results/0002/` |
| Test type | Human-compiled Workstate baseline |
| Compiler | Human |
| Receiving model | ChatGPT |
| Platform | ChatGPT |
| Model version | |
| Date | |
| Workstate version | `1.0.0` |
| Evaluation Prompt version | |
| Language | English |
| Prior context | None |
| Web access | Disabled / Unknown |
| Tools available | |
| Conversation memory | New session |
| Human intervention | None |
| Raw output | `receiving-raw.md` |
| Analysis | `analysis.md` |
| Deviations | None |
```

For a model-transfer test, also record:

```markdown
| Compiling model | |
| Receiving model | |
| Compilation Prompt version | |
| Generated Workstate version | |
```

---

## Raw Output Rules

Preserve the receiving AI's complete response exactly as produced.

Do not silently correct:

- spelling;
- grammar;
- formatting;
- wrong assumptions;
- incorrect status labels;
- invented facts;
- language changes;
- missing sections;
- model errors.

Raw output is evidence.

Corrections, interpretations, and conclusions belong in a separate analysis
file.

---

## Human Review Procedure

After preserving the raw output:

1. Read the response without correcting it.
2. Compare it with the Portable Workstate.
3. Check whether project intent was preserved.
4. Check whether the current architecture was preserved.
5. Check all authority categories.
6. Check for invented values or sources.
7. Check whether unknowns remained unknown.
8. Check whether human authority was preserved.
9. Check whether the assigned task was completed.
10. Score the response using `evaluation-criteria.md`.
11. Record critical failures separately.
12. Write the analysis in a separate file.
13. Mark observations as accepted, rejected, or requiring verification.

---

## Scoring

Use:

```text
synthetic-test/expected/evaluation-criteria.md
```

Score each category from 0 to 4.

The criteria evaluate:

- project identity;
- project intent;
- structural continuity;
- state continuity;
- authority continuity;
- content-status continuity;
- provenance awareness;
- scope continuity;
- uncertainty preservation;
- false-continuity resistance;
- task continuation;
- reviewability;
- context efficiency.

Total:

```text
13 categories × 4 points = 52 points
```

The score is a structured comparison aid.

It is not a validated scientific measurement.

---

## Critical Failures

Record critical failures separately from the total score.

Examples include:

- treating the fictional project as real;
- claiming that the project is deployed;
- inventing technical specifications;
- promoting a proposal into a canonical decision;
- presenting historical material as current;
- reactivating rejected material;
- treating unverified claims as facts;
- claiming to have read unavailable sources;
- removing human authority;
- inventing project history;
- hiding major assumptions;
- changing the project scope without labeling it.

A single critical failure may be more important than a high total score.

---

## Test Completion Checklist

Before marking a run complete, confirm:

- [ ] all required source files were supplied to the compiler, when applicable;
- [ ] the Compilation Prompt was used, when applicable;
- [ ] the Portable Workstate was created or verified;
- [ ] the receiving AI received the intended Workstate;
- [ ] the Evaluation Prompt was used;
- [ ] the raw response was preserved;
- [ ] the Evaluation Criteria were applied;
- [ ] human review was completed;
- [ ] deviations were documented;
- [ ] all files were saved inside the allocated numbered directory;
- [ ] no existing result directory was overwritten;
- [ ] no unsupported claims were added to the result;
- [ ] no conclusion exceeds the evidence produced by the test.

---

## Evidence Boundaries

The Aurora test does not establish:

- general intelligence;
- universal AI continuity;
- production readiness;
- engineering safety;
- operational reliability;
- security certification;
- guaranteed portability between all AI models.

It examines one bounded synthetic continuity task.

Results must be interpreted within the exact context, prompts, Workstate version,
model, and procedure used.

---

## Recommended Test Order

Run the tests in this order:

```text
1. Test A — Human-compiled Workstate baseline
2. Test A across multiple receiving models
3. Test B — AI-compiled Workstate
4. Test B across compiler and receiver combinations
5. Test C — Cross-model transfer
6. Test D — Context reduction comparison
7. Test E — Authority stress test
8. Repeated runs and final comparison
```

This order separates the variables gradually.

It begins with the simplest meaningful test before introducing compilation,
cross-model transfer, alternative context sizes, and authority stress testing.

---

## Final Test Principle

The purpose of the test suite is not to prove that every AI behaves
identically.

The purpose is to determine:

- what context survives;
- what meaning survives;
- what authority survives;
- what provenance survives;
- what uncertainty survives;
- what each model interprets differently;
- what the compilation process preserves or loses;
- whether meaningful work can continue.

> The goal is not identical output.
>
> The goal is meaningful, reviewable continuation.
