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

## Core Principle

Every test must be performed using the same procedure across the different AI
models.

```text
Same source material
Same Workstate
Same prompt
Same language
Same task
Same order
Same output requirements
Different AI model
```

The only variable in a clean receiving-model comparison should be the receiving
AI model.

> Same test. Same context. Same prompt. Different model.

---

## Test Directory

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
```

Create the `results/` directory before beginning the tests.

---

## Test Roles

The test process contains separate roles.

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

## Test Variables

### Variables that must remain constant

For a clean model comparison, keep the following identical:

- source fixture;
- Workstate version;
- Workstate content;
- evaluation prompt;
- prompt language;
- task;
- output requirements;
- file order;
- supplied files;
- excluded files;
- session conditions;
- scoring criteria;
- human review procedure.

### Variable that should change

For a clean receiving-model comparison, change only:

```text
Receiving AI model
```

Possible receiving models may include:

- ChatGPT;
- Claude;
- Lumo;
- Grok;
- other models documented in the test metadata.

### Variables that must be recorded

Record the following even when they are not controlled:

- model name;
- platform;
- model version, if visible;
- date;
- language;
- web access;
- tools available;
- conversation memory;
- temperature or equivalent settings, if available;
- system instructions, if known;
- human intervention;
- deviations from the procedure.

---

## Preparation

Before running a test, verify that the following files exist:

```text
synthetic-test/source/project-aurora-context.md
synthetic-test/source/project-aurora-history.md
synthetic-test/source/project-aurora-decisions.md
synthetic-test/workstates/project-aurora-portable-workstate.md
synthetic-test/prompts/compilation-prompt.md
synthetic-test/prompts/evaluation-prompt.md
synthetic-test/expected/evaluation-criteria.md
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
- source documents that are excluded from the test condition.

Do not guide the model after the test has started.

Any human intervention must be recorded.

If a repair prompt is required, preserve it as part of the result and mark the
test as requiring intervention.

---

# Test A — Human-Compiled Workstate Baseline

## Purpose

Test whether a receiving AI can continue Project Aurora from a human-reviewed
Portable Workstate.

This isolates the receiving AI from possible compilation errors.

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

1. Open a new conversation with the receiving AI.
2. Provide the Portable Workstate.
3. Provide the evaluation prompt.
4. Do not add explanatory comments.
5. Wait for the complete response.
6. Preserve the raw response exactly.
7. Record test metadata.
8. Score the response using the evaluation criteria.
9. Create a separate human-reviewed analysis.

## Purpose of the result

Test A answers:

> Can the Workstate format carry enough meaning for a receiving AI to continue
> the project?

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

## Compilation files supplied

Provide the compiling AI with:

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
- additional explanations not recorded in the metadata.

## Compilation procedure

1. Open a new conversation with the compiling AI.
2. Provide the three Project Aurora source documents.
3. Provide `compilation-prompt.md`.
4. Request only the completed Portable Workstate.
5. Preserve the complete compilation output.
6. Record the compiling model and conditions.
7. Review the generated Workstate without silently correcting it.
8. Save the generated Workstate as a test-specific file.
9. Provide that Workstate to the receiving AI in a new session.
10. Use the unchanged evaluation prompt.
11. Preserve the receiving AI output.
12. Score and analyze both stages separately.

## Required result files

```text
synthetic-test/results/
├── B-[compiler]-compilation-raw.md
├── B-[compiler]-workstate.md
├── B-[receiver]-receiving-raw.md
└── B-[receiver]-analysis.md
```

## Purpose of the result

Test B answers:

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
2. Compile the Workstate using the unchanged source files and compilation
   prompt.
3. Preserve the raw compilation output.
4. Record the exact Workstate version produced.
5. Start a new conversation with the receiving model.
6. Provide only the generated Workstate and evaluation prompt.
7. Preserve the complete receiving output.
8. Score the result using the same criteria.
9. Record errors specific to compilation and errors specific to reception.

## Example matrix

```text
Compiler: ChatGPT
    ↓
Receiver: Claude

Compiler: Claude
    ↓
Receiver: Lumo

Compiler: Lumo
    ↓
Receiver: Grok
```

The matrix may be expanded, but each run must use the same procedure.

## Purpose of the result

Test C answers:

> Can a Workstate created by one model be meaningfully used by another model?

---

# Test D — Context Reduction Comparison

## Purpose

Compare the compiled Portable Workstate with simpler alternatives.

This tests whether the architecture provides value beyond basic documentation.

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

## Rules

Keep the following identical:

- receiving model;
- language;
- task;
- output requirements;
- session conditions;
- scoring criteria.

Change only the context condition.

## Purpose of the result

Test D answers:

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

1. Provide the same Workstate to each receiving model.
2. Use the unchanged evaluation prompt.
3. Ask the model to continue the task.
4. Check whether it preserves every status category.
5. Record any status promotion or authority error.

## Critical examples

The receiving AI must not:

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

## Purpose of the result

Test E answers:

> Can the receiving AI preserve status and authority rather than merely
> preserve vocabulary and general meaning?

This is one of the most important tests in the suite.

---

# Model Matrix

Each test should be run across the selected AI models using the same procedure.

```text
Test A
├── ChatGPT
├── Claude
├── Lumo
└── Grok

Test B
├── ChatGPT
├── Claude
├── Lumo
└── Grok

Test C
├── ChatGPT → Claude
├── Claude → Lumo
├── Lumo → Grok
└── Grok → ChatGPT
```

A model may be unavailable, renamed, updated, or restricted.

Record unavailable models rather than silently replacing them.

---

## Test IDs

Use a unique identifier for every individual run.

Examples:

```text
A-chatgpt-001
A-claude-001
A-lumo-001
A-grok-001

B-chatgpt-to-claude-001
B-claude-to-lumo-001

C-chatgpt-claude-001
C-lumo-grok-001
```

The ID should identify:

- test type;
- model or model pair;
- sequence number.

---

## Metadata Template

Create a metadata file for each test run or include the metadata at the top of
the result file.

```markdown
# Test Metadata

| Field | Value |
|---|---|
| Test ID | `A-chatgpt-001` |
| Test type | Human-compiled Workstate baseline |
| Compiler | Human |
| Receiving model | ChatGPT |
| Platform | ChatGPT |
| Model version | |
| Date | |
| Workstate version | `1.0.0` |
| Evaluation prompt version | `1.0.0` |
| Language | English |
| Prior context | None |
| Web access | Disabled / Unknown |
| Tools available | |
| Conversation memory | New session |
| Human intervention | None |
| Raw output | |
| Analysis | |
| Deviations | None |
```

For a model-transfer test, add:

```markdown
| Compiling model | |
| Receiving model | |
| Compilation prompt version | `1.0.0` |
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

## Result File Structure

Use this structure:

```text
synthetic-test/results/
├── A-chatgpt-001-raw.md
├── A-chatgpt-001-analysis.md
├── A-claude-001-raw.md
├── A-claude-001-analysis.md
├── B-chatgpt-001-compilation-raw.md
├── B-chatgpt-001-workstate.md
├── B-claude-001-reception-raw.md
├── B-claude-001-analysis.md
└── comparison-round-001.md
```

The exact filenames may be extended with model versions or dates.

---

## Human Review Procedure

After preserving the raw output:

1. Read the response without correcting it.
2. Compare it with the Portable Workstate.
3. Check whether project intent was preserved.
4. Check whether current architecture was preserved.
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

Evaluate:

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

## Cross-Model Comparison

When comparing models, create a comparison document containing:

```markdown
# Project Aurora — Cross-Model Comparison

## Test Conditions

## Models Included

## Context Supplied

## Constant Variables

## Model-Specific Variables

## Semantic Continuity

## Structural Continuity

## Intent Continuity

## Authority Preservation

## Provenance Awareness

## Uncertainty Preservation

## False-Continuity Resistance

## Task Continuation

## Critical Failures

## Scores

## Shared Strengths

## Shared Weaknesses

## Model-Specific Behaviours

## Human Review

## Limitations

## Conclusion
```

Compare:

```text
What did every model preserve?
What did every model lose?
What was model-specific?
What errors came from compilation?
What errors came from reception?
What depended on language?
What depended on the Workstate?
```

Do not claim that one model is generally better based on one test run.

---

## Repetition

A single run is not enough to establish a general result.

Where possible:

- repeat the same test;
- use the same Workstate version;
- use the same prompt;
- record all deviations;
- compare repeated outputs;
- preserve all raw results.

If a model produces different results in repeated clean sessions, record the
variation rather than selecting only the best response.

---

## Reporting Results

A final report should distinguish between:

```text
Observed
    What the model actually produced

Inferred
    What the result may suggest

Proposed
    What should be tested next

Unverified
    What cannot yet be established
```

Use cautious conclusions.

Prefer:

```text
The result provides preliminary evidence that...
```

Avoid:

```text
The method is proven.
```

The tests can provide evidence of continuity behaviour.

They do not automatically establish universal portability, scientific validity,
commercial value, or operational safety.

---

## Recommended Test Order

Run the tests in this order:

```text
1. Test A — Human-compiled Workstate baseline
2. Test A across multiple receiving models
3. Test B — AI-compiled Workstate
4. Test B across multiple compiler and receiver combinations
5. Test C — Cross-model transfer
6. Test D — Context reduction comparison
7. Test E — Authority stress test
8. Repeated runs and final comparison
```

This order separates the variables gradually.

It begins with the simplest meaningful test before introducing compilation,
cross-model transfer, alternative context sizes, and adversarial status testing.

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
