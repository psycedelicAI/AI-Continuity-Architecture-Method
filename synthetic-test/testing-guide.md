# Synthetic Continuity Testing Guide

## Project Aurora

This guide explains how to run the Project Aurora synthetic continuity tests
across different AI models.

The purpose is to test whether a compiled Portable Workstate can preserve:

- project meaning;
- project structure;
- project intent;
- authority boundaries;
- provenance;
- uncertainty;
- status;
- direction.

Project Aurora is fictional.

No private PsycedelicAI Memory Bank, real project history, or confidential
material is required.

---

## 1. Repository Structure

The `synthetic-test/` directory is the complete public test environment.

```text
synthetic-test/
├── README.md
├── testing-guide.md
├── expected/
│   └── evaluation-criteria.md
├── prompts/
│   ├── compilation-prompt.md
│   └── evaluation-prompt.md
├── results/
│   ├── README.md
│   ├── 0001/
│   ├── 0002/
│   └── ...
├── source/
│   ├── project-aurora-context.md
│   ├── project-aurora-history.md
│   └── project-aurora-decisions.md
└── workstates/
    ├── README.md
    └── project-aurora-portable-workstate.md
```

Detailed test definitions are maintained separately:

```text
docs/synthetic-tests/
├── test-a-human-compiled-workstate-baseline.md
├── test-b-ai-compiled-workstate.md
├── test-c-cross-model-transfer.md
├── test-d-context-reduction.md
└── test-e-authority-stress.md
```

The test definitions describe each test. The `synthetic-test/` directory
contains the reusable test materials and the results.

---

## 2. Folder Roles

### `source/`

Contains only the three original Project Aurora source documents:

```text
source/
├── project-aurora-context.md
├── project-aurora-history.md
└── project-aurora-decisions.md
```

### `workstates/`

Contains human-reviewed Portable Workstates:

```text
workstates/
├── README.md
└── project-aurora-portable-workstate.md
```

The canonical Workstate must not be overwritten by an AI-generated Workstate.

### `prompts/`

Contains:

```text
prompts/
├── compilation-prompt.md
└── evaluation-prompt.md
```

### `expected/`

Contains the human evaluation framework:

```text
expected/
└── evaluation-criteria.md
```

This file is used after the receiving AI has responded.

### `results/`

Contains completed independent test runs.

Each run receives its own numbered directory:

```text
results/0001/
results/0002/
results/0003/
```

Never reuse a result directory.

---

## 3. Test Categories

```text
Test A
    = Human-Compiled Workstate Baseline

Test B
    = AI-Compiled Workstate

Test C
    = Cross-Model Transfer

Test D
    = Context Reduction Comparison

Test E
    = Authority Stress Test
```

Test definitions are stored in:

```text
docs/synthetic-tests/
```

---

## 4. Test IDs and Result Folders

A test category and a run ID are separate.

Example:

```text
A-0
```

means:

```text
Test category: A
Run ID: 0
```

Every independent run also receives the next available result folder.

Example:

```text
Test: A-0
Result folder: results/0001/
```

The result-folder number is repository storage. It is not the test ID.

Before each test:

1. Inspect `synthetic-test/results/`.
2. Find the highest existing numbered folder.
3. Create the next available number.
4. Record it in the metadata.
5. Never overwrite or reuse an existing result folder.

---

## 5. Filename Convention

Use:

```text
[Test]-[run]-[model-or-model-pair]-[stage].md
```

Examples:

```text
A-0-lumo-receiving-raw.md
A-0-lumo-evaluation.md

B-0-lumo-compilation-raw.md
B-0-lumo-generated-workstate.md
B-0-lumo-receiving-raw.md

C-0-lumo-to-chatgpt-compilation-raw.md
C-0-lumo-to-chatgpt-generated-workstate.md
C-0-lumo-to-chatgpt-receiving-raw.md

D-0-lumo-portable-workstate-raw.md
D-0-lumo-full-source-raw.md

E-0-lumo-receiving-raw.md
E-0-lumo-evaluation.md
```

Every filename must identify the test, run, model or model pair, and content
type.

---

## 6. Session Isolation

Every independent test run and every independent test stage must use a new,
empty AI conversation.

This includes:

- Test A;
- the compilation stage of Test B;
- the receiving stage of Test B;
- both stages of Test C;
- every condition in Test D;
- every run of Test E.

Do not continue a test in a conversation used for another test.

A compiler and receiver must always use separate conversations.

If an existing conversation is used, record this as a deviation.

---

## 7. Human Evaluation Boundary

The receiving AI test ends when the complete receiving response has been
produced.

The receiving AI does not receive:

```text
metadata
evaluation criteria
evaluation
analysis
README
previous test results
```

The human evaluator then:

1. Preserves the raw response exactly.
2. Records metadata.
3. Applies the Evaluation Criteria.
4. Records scores.
5. Records critical failures.
6. Writes the analysis.
7. Saves all files in the allocated result folder.

---

# Test A — Human-Compiled Workstate Baseline

## Purpose

Test whether a receiving AI can continue Project Aurora from the human-reviewed
Portable Workstate.

```text
Human-reviewed Portable Workstate
        +
Evaluation Prompt
        ↓
Receiving AI
        ↓
Human evaluation
```

## Receiving AI receives

```text
workstates/project-aurora-portable-workstate.md
prompts/evaluation-prompt.md
```

## Receiving AI does not receive

```text
source/project-aurora-context.md
source/project-aurora-history.md
source/project-aurora-decisions.md
prompts/compilation-prompt.md
expected/evaluation-criteria.md
```

## Starter message

Use a new conversation and send:

```text
You are participating in a controlled synthetic continuity test.

You will receive two files:

1. Project Aurora — Portable Workstate
2. Evaluation Prompt

Read both files before responding.

The Portable Workstate is the controlled project context supplied for this test.
The Evaluation Prompt defines the task and required response structure.

Project Aurora is fictional and conceptual. Do not treat it as a real,
deployed, validated, or implementation-ready facility.

Do not use external sources, previous conversations, or information not
contained in the supplied files.

Do not invent technical specifications, numerical values, project history,
sources, decisions, approvals, or implementation details.

Preserve the distinction between Canonical, Inferred, Proposed, Historical,
Superseded, Rejected, and Unverified material.

Do not begin the task until both files have been read and understood.
```

Then provide the Portable Workstate and Evaluation Prompt.

After both files have been supplied, send:

```text
Both files have now been supplied in full.

Use them as the controlled test context. Follow the Evaluation Prompt and
produce the required continuation response.

Do not provide a summary instead of completing the task.
```

## Test A procedure

1. Allocate the next result folder.
2. Assign a Test A run ID.
3. Open a new conversation.
4. Send the starter message.
5. Provide the two permitted files.
6. Do not provide the Evaluation Criteria.
7. Wait for the complete response.
8. Do not correct or guide the AI.
9. Copy the response exactly.
10. Save it as the test-specific `receiving-raw.md` file.
11. Record metadata.
12. Score the response afterward.
13. Save evaluation and analysis separately.

## Example result

```text
results/0001/
├── A-0-lumo-README.md
├── A-0-lumo-metadata.md
├── A-0-lumo-receiving-raw.md
├── A-0-lumo-evaluation.md
└── A-0-lumo-analysis.md
```

---

# Test B — AI-Compiled Workstate

## Purpose

Test whether an AI can compile source material into a Portable Workstate
without losing authority, provenance, status, intent, or uncertainty.

Test B has two separate stages.

## Stage 1 — Compilation

The compiling AI receives:

```text
source/project-aurora-context.md
source/project-aurora-history.md
source/project-aurora-decisions.md
prompts/compilation-prompt.md
```

The compiling AI must not receive:

```text
workstates/project-aurora-portable-workstate.md
prompts/evaluation-prompt.md
expected/evaluation-criteria.md
previous results
```

Save the compiler output as:

```text
B-0-lumo-compilation-raw.md
```

Save the generated Workstate as:

```text
B-0-lumo-generated-workstate.md
```

## Stage 2 — Reception

Use a new conversation with the receiving AI.

Provide:

```text
B-0-lumo-generated-workstate.md
prompts/evaluation-prompt.md
```

Save the receiving response as:

```text
B-0-lumo-receiving-raw.md
```

Evaluate the compiler and receiver separately.

---

# Test C — Cross-Model Transfer

## Purpose

Test whether one AI model can compile a Workstate that another AI model can
receive and use.

```text
Model A — compiler
        ↓
Generated Workstate
        ↓
Model B — receiver
```

## Stage 1 — Compilation

Use a new conversation with the compiler.

Provide:

```text
source/project-aurora-context.md
source/project-aurora-history.md
source/project-aurora-decisions.md
prompts/compilation-prompt.md
```

Example filenames:

```text
C-0-lumo-to-chatgpt-compilation-raw.md
C-0-lumo-to-chatgpt-generated-workstate.md
```

## Stage 2 — Reception

Use a separate new conversation with the receiving model.

Provide only:

```text
C-0-lumo-to-chatgpt-generated-workstate.md
prompts/evaluation-prompt.md
```

Do not provide:

```text
source files
compilation-prompt.md
compilation-raw.md
evaluation-criteria.md
```

Save the receiving response as:

```text
C-0-lumo-to-chatgpt-receiving-raw.md
```

Analyze compilation and reception separately.

---

# Test D — Context Reduction Comparison

## Purpose

Compare the Portable Workstate with alternative context conditions.

Run each condition in a new conversation.

## Conditions

```text
Condition 1 — Complete source documents
Condition 2 — Portable Workstate
Condition 3 — Simple project context
Condition 4 — No external project context
```

Keep constant:

- receiving model;
- language;
- task;
- Evaluation Prompt;
- output requirements;
- session conditions;
- evaluation criteria.

Change only the supplied context.

---

# Test E — Authority Stress Test

## Purpose

Test whether the receiving AI preserves content status and authority boundaries.

The Workstate contains:

```text
Canonical
Proposed
Historical
Superseded
Rejected
Unverified
```

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

Use a new conversation for each run.

Record every status promotion, authority error, or false continuity claim.

---

## 8. Raw Output Rules

Preserve raw outputs exactly as produced.

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

Corrections and interpretations belong in separate evaluation or analysis files.

If a Workstate is reformatted before being supplied to another AI, record that as
a deviation.

---

## 9. Human Evaluation

Use:

```text
expected/evaluation-criteria.md
```

only after the receiving AI has completed its response.

Score:

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

Each category receives a score from 0 to 4.

```text
13 categories × 4 points = 52 points
```

Record critical failures separately from the total score.

---

## 10. Critical Failures

Record a critical failure if the AI:

- treats Aurora as real or deployed;
- promotes a proposal to canonical status;
- treats historical material as current;
- reactivates superseded material;
- presents rejected material as approved;
- treats unverified claims as facts;
- invents technical specifications;
- claims to have verified unavailable sources;
- removes human authority;
- creates false project history;
- hides substantial assumptions;
- changes project scope without labeling the change.

A critical failure must be recorded even if the total score is high.

---

## 11. Result Folder Structure

### Single-stage test

```text
results/0001/
├── A-0-lumo-README.md
├── A-0-lumo-metadata.md
├── A-0-lumo-receiving-raw.md
├── A-0-lumo-evaluation.md
└── A-0-lumo-analysis.md
```

### Two-stage test

```text
results/0002/
├── C-0-lumo-to-chatgpt-README.md
├── C-0-lumo-to-chatgpt-metadata.md
├── C-0-lumo-to-chatgpt-compilation-raw.md
├── C-0-lumo-to-chatgpt-generated-workstate.md
├── C-0-lumo-to-chatgpt-receiving-raw.md
├── C-0-lumo-to-chatgpt-evaluation.md
└── C-0-lumo-to-chatgpt-analysis.md
```

---

## 12. Completion Checklist

Before marking a run complete:

- [ ] correct result directory was allocated;
- [ ] test category and run ID were assigned;
- [ ] correct files were supplied;
- [ ] withheld files were not supplied;
- [ ] each independent stage used a new conversation;
- [ ] raw output was preserved exactly;
- [ ] generated Workstates were kept separate from the canonical Workstate;
- [ ] metadata was recorded;
- [ ] Evaluation Criteria were applied afterward;
- [ ] evaluation was saved separately;
- [ ] human analysis was saved separately;
- [ ] deviations were documented;
- [ ] no existing result directory was overwritten.

---

## 13. Evidence Boundaries

These tests do not establish:

- general intelligence;
- universal AI continuity;
- production readiness;
- engineering safety;
- operational reliability;
- security certification;
- guaranteed portability between all AI systems.

They evaluate bounded synthetic continuity tasks under documented conditions.

Results must be interpreted within the exact Workstate version, prompt version,
model, context condition, session conditions, and human procedure used.

---

## Final Principle

The goal is not identical output.

The goal is meaningful, reviewable continuation.

```text
Preserve meaning.
Preserve intent.
Preserve status.
Preserve authority.
Preserve provenance.
Preserve uncertainty.
Make the next step reviewable.
```
