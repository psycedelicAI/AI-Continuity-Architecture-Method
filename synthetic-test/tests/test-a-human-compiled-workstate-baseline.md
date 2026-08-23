# Test A — Human-Compiled Workstate Baseline

> Private operational test definition for the Project Aurora synthetic
> continuity test suite.

---

## Test Identity

| Field | Value |
|---|---|
| Test ID | `A` |
| Test name | Human-Compiled Workstate Baseline |
| Test type | Receiving-AI continuity test |
| Test stage | Baseline |
| Compilation method | Human-reviewed |
| Receiving AI | Variable |
| Project | Fictional Project Aurora |
| Workstate version | `1.0.0` |
| Evaluation | Human review required |
| Evidence type | Exploratory evidence |

---

## Purpose

Test whether a receiving AI can continue Project Aurora from a
human-compiled and human-reviewed Portable Workstate.

This test evaluates the receiving AI's ability to preserve:

- project identity;
- project purpose;
- project intent;
- architectural relationships;
- operational states;
- authority boundaries;
- content status;
- provenance;
- uncertainty;
- project scope;
- meaningful next actions.

Test A does not evaluate whether an AI can compile the Workstate.

It evaluates whether an AI can receive and use the Workstate.

---

## Primary Test Question

> Can a receiving AI continue meaningful work from the human-compiled Portable
> Workstate while preserving project meaning, status, authority, provenance,
> uncertainty, and scope?

---

## Test Model

```text
Human-reviewed source interpretation
        ↓
Portable Workstate
        +
Evaluation Prompt
        ↓
Receiving AI
        ↓
Raw response
        ↓
Human evaluation
        ↓
Documented result
```

---

## Controlled Test Condition

The receiving AI receives:

```text
Portable Workstate
Evaluation Prompt
```

The receiving AI does not receive:

```text
Original source documents
Compilation Prompt
Evaluation Criteria
Previous test results
Previous analyses
Private project context
```

The purpose is to test the Workstate as a bounded transfer artifact.

---

## Files Supplied to the Receiving AI

Provide exactly these files:

```text
synthetic-test/workstates/project-aurora-portable-workstate.md
synthetic-test/prompts/evaluation-prompt.md
```

Provide them in this order:

1. `project-aurora-portable-workstate.md`
2. `evaluation-prompt.md`

The files may be uploaded or pasted into the conversation.

---

## Files Withheld from the Receiving AI

Do not provide:

```text
synthetic-test/source/project-aurora-context.md
synthetic-test/source/project-aurora-history.md
synthetic-test/source/project-aurora-decisions.md
synthetic-test/prompts/compilation-prompt.md
synthetic-test/expected/evaluation-criteria.md
```

The Evaluation Criteria must remain withheld until the receiving AI has
completed its response.

---

## Receiving-AI Starter Message

Begin a new, empty conversation with the receiving AI.

Send the following message before providing the files:

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

---

## File Delivery

After the starter message, provide:

```text
--- BEGIN FILE: project-aurora-portable-workstate.md ---
[complete contents of the Portable Workstate]
--- END FILE: project-aurora-portable-workstate.md ---

--- BEGIN FILE: evaluation-prompt.md ---
[complete contents of the Evaluation Prompt]
--- END FILE: evaluation-prompt.md ---
```

If the platform supports reliable file uploads, the files may be uploaded
instead.

After both files have been provided, send:

```text
Both files have now been supplied in full.

Use them as the controlled test context. Follow the Evaluation Prompt and
produce the required continuation response.

Do not provide a summary instead of completing the task.
```

If the receiving AI begins the task immediately after receiving the files, do
not send an additional message. Record the actual sequence in the metadata.

---

## Receiving-AI Task

The receiving AI is instructed to:

> Propose a structured method for prioritizing essential service during
> prolonged constrained operation.

The response must remain within the conceptual scope of Project Aurora.

The receiving AI should:

- demonstrate understanding of the Workstate;
- identify relevant canonical constraints;
- propose a structured prioritization method;
- distinguish current context from new proposals;
- identify assumptions;
- identify unknowns;
- explain risks and trade-offs;
- identify Review Hold conditions;
- preserve human authority;
- record provenance;
- suggest reviewable next actions.

---

## Test Restrictions

The receiving AI must not:

- treat Project Aurora as real;
- claim that Aurora is deployed;
- present the proposal as a confirmed decision;
- invent technical specifications;
- invent numerical values;
- invent project history;
- invent sources or approvals;
- present historical material as current;
- reactivate superseded material;
- present rejected material as approved;
- present unverified claims as facts;
- remove human authority;
- silently change project scope.

---

## Clean-Session Requirements

Use a new, empty conversation.

Do not use a conversation containing:

- previous Aurora tests;
- previous Aurora results;
- previous model responses;
- private Memory Bank material;
- unrelated project instructions;
- previous discussions that could influence the response.

Do not coach or correct the receiving AI after the test begins.

Do not send repair prompts during the baseline run.

If a repair prompt or human intervention occurs, preserve it and mark the run as
a deviation from the clean baseline condition.

---

## Result Directory Allocation

Before starting the test:

1. Inspect `synthetic-test/results/`.
2. Find the highest existing numbered result directory.
3. Create the next available directory.
4. Never reuse an existing result directory.
5. Record the directory number in the metadata.

Example:

```text
If `0001/` exists:
    create `0002/`

If `0001/` and `0002/` exist:
    create `0003/`
```

The result directory is allocated when the test begins, even if the test is
interrupted.

---

## Test ID

Use this format:

```text
A-[receiving-model]-[run-number]
```

Examples:

```text
A-chatgpt-001
A-claude-002
A-lumo-003
A-grok-004
```

The test ID and result directory must be recorded together.

Example:

```text
Test ID: A-chatgpt-002
Result directory: results/0002/
```

---

## Test Procedure

### Step 1 — Allocate the result directory

Create the next available numbered result directory.

Example:

```text
synthetic-test/results/0002/
```

---

### Step 2 — Assign the Test ID

Assign the Test ID before opening the receiving-AI conversation.

Example:

```text
A-chatgpt-002
```

---

### Step 3 — Create the result metadata

Create:

```text
A-chatgpt-002-metadata.md
```

Record the model, platform, date, Workstate version, prompt version, language,
tools, web access, memory status, and any deviations.

---

### Step 4 — Start the clean conversation

Open a new, empty conversation with the receiving AI.

Send the standard starter message.

---

### Step 5 — Provide the two test files

Provide only:

```text
project-aurora-portable-workstate.md
evaluation-prompt.md
```

Do not provide the withheld files.

---

### Step 6 — Request the continuation response

Send the final instruction if the AI has not already begun responding:

```text
Both files have now been supplied in full.

Use them as the controlled test context. Follow the Evaluation Prompt and
produce the required continuation response.

Do not provide a summary instead of completing the task.
```

---

### Step 7 — Wait for completion

Allow the receiving AI to produce its complete response.

Do not:

- correct the response;
- answer questions on its behalf;
- provide missing context;
- point out errors;
- ask it to improve the answer;
- send a repair prompt.

---

### Step 8 — Preserve the raw response

Copy the complete response exactly as produced.

Do not edit:

- wording;
- formatting;
- headings;
- mistakes;
- assumptions;
- status labels;
- citations;
- omissions;
- invented values;
- language.

Save the response as:

```text
A-[receiving-model]-[run-number]-receiving-raw.md
```

Example:

```text
A-chatgpt-002-receiving-raw.md
```

---

## Test A Result Structure

Example:

```text
synthetic-test/results/0002/
├── A-chatgpt-002-README.md
├── A-chatgpt-002-metadata.md
├── A-chatgpt-002-receiving-raw.md
└── A-chatgpt-002-evaluation.md
```

### File purposes

| File | Purpose |
|---|---|
| `A-chatgpt-002-README.md` | Human-readable result summary |
| `A-chatgpt-002-metadata.md` | Test conditions and deviations |
| `A-chatgpt-002-receiving-raw.md` | Exact untouched receiving-AI response |
| `A-chatgpt-002-evaluation.md` | Human scoring and analysis |

---

## Metadata Template

```markdown
# Test A Metadata

| Field | Value |
|---|---|
| Test ID | `A-chatgpt-002` |
| Result directory | `results/0002/` |
| Test type | Human-Compiled Workstate Baseline |
| Compiler | Human |
| Receiving model | ChatGPT |
| Platform | |
| Model version | |
| Test date | |
| Workstate version | `1.0.0` |
| Evaluation Prompt version | |
| Language | English |
| Conversation | New empty conversation |
| Web access | |
| Tools available | |
| Memory status | |
| Files supplied | Portable Workstate + Evaluation Prompt |
| Files withheld | Source files + Compilation Prompt + Evaluation Criteria |
| Human intervention | None |
| Deviations | None |
| Raw response file | `A-chatgpt-002-receiving-raw.md` |
| Evaluation file | `A-chatgpt-002-evaluation.md` |
```

---

## Human Evaluation

Only after the raw response has been saved, open:

```text
synthetic-test/expected/evaluation-criteria.md
```

Do not send the Evaluation Criteria to the receiving AI.

Evaluate the response across these categories:

1. Project Identity;
2. Project Intent;
3. Structural Continuity;
4. State Continuity;
5. Authority Continuity;
6. Content-Status Continuity;
7. Provenance Awareness;
8. Scope Continuity;
9. Uncertainty Preservation;
10. False-Continuity Resistance;
11. Task Continuation;
12. Reviewability;
13. Context Efficiency.

Each category receives a score from 0 to 4.

```text
Maximum score: 52
```

Record critical failures separately from the total score.

---

## Evaluation File

Create:

```text
A-chatgpt-002-evaluation.md
```

Use:

```markdown
# Test A Evaluation

| Field | Value |
|---|---|
| Test ID | `A-chatgpt-002` |
| Result directory | `results/0002/` |
| Receiving model | ChatGPT |
| Workstate version | `1.0.0` |
| Total score | `/52` |
| Critical failure | Yes / No |
| Human reviewer | |
| Review date | |

## Category Scores

| Category | Score | Notes |
|---|---:|---|
| Project Identity | /4 | |
| Project Intent | /4 | |
| Structural Continuity | /4 | |
| State Continuity | /4 | |
| Authority Continuity | /4 | |
| Content-Status Continuity | /4 | |
| Provenance Awareness | /4 | |
| Scope Continuity | /4 | |
| Uncertainty Preservation | /4 | |
| False-Continuity Resistance | /4 | |
| Task Continuation | /4 | |
| Reviewability | /4 | |
| Context Efficiency | /4 | |

## Critical Failures

- None identified.

## Human Analysis

[Record observations based on the raw response.]

## Follow-Up

[Record proposed next actions.]
```

---

## README Template

Create:

```text
A-chatgpt-002-README.md
```

Use:

```markdown
# Test A — Human-Compiled Workstate Baseline

| Field | Value |
|---|---|
| Test ID | `A-chatgpt-002` |
| Result directory | `results/0002/` |
| Receiving model | ChatGPT |
| Workstate version | `1.0.0` |
| Raw response | `A-chatgpt-002-receiving-raw.md` |
| Evaluation | `A-chatgpt-002-evaluation.md` |
| Status | Human review pending |
| Evidence type | Exploratory evidence |

## Summary

[Complete after evaluation.]

## Important Note

This result directory belongs to one independent test run and must not be reused
for another test.
```

---

## Test A Completion Conditions

Test A is complete when:

- [ ] the next available result directory was allocated;
- [ ] the Test ID was assigned;
- [ ] metadata was recorded;
- [ ] a new empty conversation was used;
- [ ] the standard starter message was sent;
- [ ] only the Portable Workstate and Evaluation Prompt were supplied;
- [ ] the source files were withheld;
- [ ] the Compilation Prompt was withheld;
- [ ] the Evaluation Criteria were withheld;
- [ ] the complete receiving-AI response was preserved;
- [ ] the raw response was saved with the Test A filename convention;
- [ ] no corrective intervention occurred, or intervention was documented;
- [ ] the Evaluation Criteria were applied afterward;
- [ ] the evaluation was saved separately;
- [ ] human analysis was recorded;
- [ ] no existing result directory was overwritten.

---

## Evidence Boundary

Test A evaluates one receiving AI under one bounded context condition.

It does not establish:

- universal AI continuity;
- general model capability;
- production readiness;
- engineering safety;
- operational reliability;
- security certification;
- guaranteed portability between all AI systems.

It provides a baseline result for comparison with Tests B–E.

---

## Relationship to the Other Tests

```text
Test A
    = Can a receiving AI use a human-compiled Workstate?

Test B
    = Can an AI compile the Workstate correctly?

Test C
    = Can one model transfer a Workstate to another model?

Test D
    = Is the Workstate more useful than alternative context conditions?

Test E
    = Can the receiving AI preserve authority and status under stress?
```

Test A should normally be completed before Tests B–E.

---

## End of Test Definition
