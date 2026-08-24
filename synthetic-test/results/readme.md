# Test Results

This directory contains documented results from the Project Aurora synthetic
continuity tests.

The results preserve:

- raw AI outputs;
- generated Portable Workstates;
- test metadata;
- evaluation scores;
- human analysis;
- procedural deviations;
- archived revisions.

The results are exploratory evidence. They are not, by themselves, proof of
general model capability or universal validation of the AI Continuity
Architecture Method.

---

## Result Folder Policy

Folders `0001` through `0010` are reserved working slots for iterative
Project Aurora testing performed by Psycedelic.

```text
0001/
0002/
0003/
...
0010/
```

These folders may be updated and reused while:

- prompts are being refined;
- file placement is being corrected;
- test procedures are being clarified;
- model runs are being repeated;
- evaluation files are being improved;
- repository structure is being developed.

They are working slots, not immutable one-time result folders.

---

## Current Working Slots

A working slot represents the latest current version of one test run or test
development cycle.

Example:

```text
0001/
    = current working version of the baseline test

0002/
    = current working version of a cross-model transfer test
```

The exact test identity must be recorded in the metadata and README inside the
folder.

---

## Archive Before Replacement

Before replacing any current result file:

1. Create the folder's `older/` directory if necessary.
2. Copy the existing file into `older/`.
3. Add a timestamped archive prefix.
4. Replace the current file with the revised version.
5. Record any meaningful procedural change in the metadata.

Do not silently overwrite an existing working result.

Do not delete archived files.

---

## Archive Naming

Use the following format:

```text
YYYY-MM-DD-HHMMSS-[test-name]-[original-filename]
```

Use the Europe/Stockholm timezone.

Examples:

```text
2026-08-24-134500-A-0-lumo-receiving-raw.md
2026-08-24-134500-A-0-lumo-evaluation.md
2026-08-24-142210-C-0-lumo-to-chatgpt-generated-workstate.md
2026-08-24-142210-C-0-lumo-to-chatgpt-receiving-raw.md
```

Example archive structure:

```text
0001/
├── A-0-lumo-receiving-raw.md
├── A-0-lumo-evaluation.md
└── older/
    ├── 2026-08-24-134500-A-0-lumo-receiving-raw.md
    └── 2026-08-24-134500-A-0-lumo-evaluation.md
```

The archived filename must preserve the original test-specific filename after
the timestamp.

---

## Current and Archived Files

Current files represent the latest working version:

```text
0001/A-0-lumo-receiving-raw.md
```

Archived files represent previous versions:

```text
0001/older/2026-08-24-134500-A-0-lumo-receiving-raw.md
```

Files inside `older/` may be:

- incomplete;
- superseded;
- corrected;
- procedurally invalid;
- experimental;
- retained for historical reference.

Archived files must not be treated as the current result.

---

## Result Naming Convention

Use:

```text
[Test]-[run]-[model-or-model-pair]-[stage].md
```

Examples:

```text
A-0-lumo-receiving-raw.md
A-0-lumo-evaluation.md
A-0-lumo-analysis.md

B-0-lumo-compilation-raw.md
B-0-lumo-generated-workstate.md
B-0-lumo-receiving-raw.md

C-0-lumo-to-chatgpt-compilation-raw.md
C-0-lumo-to-chatgpt-generated-workstate.md
C-0-lumo-to-chatgpt-receiving-raw.md
```

Do not use generic filenames such as:

```text
answer.md
output.md
receiving-raw.md
evaluation.md
```

A result filename should identify the test, run, model or model pair, and
content type.

---

## Recommended Result Contents

### Single-stage test

```text
0001/
├── A-0-lumo-README.md
├── A-0-lumo-metadata.md
├── A-0-lumo-receiving-raw.md
├── A-0-lumo-evaluation.md
└── A-0-lumo-analysis.md
```

### Two-stage test

```text
0002/
├── C-0-lumo-to-chatgpt-README.md
├── C-0-lumo-to-chatgpt-metadata.md
├── C-0-lumo-to-chatgpt-compilation-raw.md
├── C-0-lumo-to-chatgpt-generated-workstate.md
├── C-0-lumo-to-chatgpt-receiving-raw.md
├── C-0-lumo-to-chatgpt-evaluation.md
└── C-0-lumo-to-chatgpt-analysis.md
```

### Optional archive

```text
0002/
└── older/
    ├── 2026-08-24-150000-C-0-lumo-to-chatgpt-generated-workstate.md
    └── 2026-08-24-150000-C-0-lumo-to-chatgpt-receiving-raw.md
```

---

## Metadata Requirements

Each working result should record:

- test category;
- run ID;
- result folder;
- test name;
- compiler, if applicable;
- receiving model;
- platform;
- model version, if visible;
- Workstate version;
- prompt versions;
- date and time;
- language;
- web access;
- tools available;
- conversation status;
- human intervention;
- deviations;
- revision status.

Example:

```markdown
# Test Metadata

| Field | Value |
|---|---|
| Test category | `A` |
| Run ID | `0` |
| Test ID | `A-0` |
| Result folder | `results/0001/` |
| Test name | Human-Compiled Workstate Baseline |
| Receiving model | Lumo |
| Workstate version | `1.0.0` |
| Evaluation Prompt version | |
| Test date | `2026-08-24` |
| Conversation | New empty conversation |
| Human intervention | None |
| Revision status | Working |
| Archived previous version | No |
| Deviations | None |
```

---

## Raw Output Rules

Raw AI output must be preserved exactly as produced.

Do not silently correct:

- wording;
- spelling;
- grammar;
- formatting;
- incorrect status labels;
- invented facts;
- unsupported assumptions;
- missing sections;
- model errors.

If a response is corrected, the original must remain in `older/`.

Corrections and interpretations belong in separate evaluation or analysis files.

---

## Human Evaluation

Evaluation criteria are stored in:

```text
../expected/evaluation-criteria.md
```

They are used by the human evaluator after the receiving AI has completed its
response.

The evaluation criteria must not be sent to the receiving AI during a clean
test.

Evaluation files should record:

- category scores;
- total score;
- critical failures;
- evidence;
- human analysis;
- uncertainties;
- proposed follow-up actions.

---

## Working Status

A result may be marked as:

```text
Working
Revised
Repeated
Evaluated
Finalized
Archived
```

Example:

```markdown
| Result status | Revised |
| Revision count | 2 |
| Current version | Yes |
| Archived versions | 3 |
| Human evaluation | Pending |
```

A result marked `Working` or `Revised` must not be presented as a final
validated result.

---

## Folders Beyond `0010`

Folders above `0010` may be used for:

- independent test runs;
- external submissions;
- comparative model runs;
- published results;
- finalized evidence.

Their reuse and archival policy must be defined before use.

Unless explicitly documented otherwise, folders above `0010` should not be
overwritten.

---

## Evidence Boundaries

The contents of this directory do not establish:

- general intelligence;
- universal AI continuity;
- production readiness;
- engineering safety;
- operational reliability;
- security certification;
- guaranteed portability between all AI systems.

The results document bounded synthetic test runs.

Interpret every result within its exact:

- test category;
- run ID;
- Workstate version;
- prompt version;
- model;
- context condition;
- session conditions;
- human procedure;
- revision history.

---

## Final Principle

The current file shows the latest working state.

The `older/` directory preserves how that state developed.

```text
Current result
    = latest working version

Older archive
    = preserved previous versions

Metadata
    = conditions and provenance

Evaluation
    = human judgment

Analysis
    = interpretation
```

> Improve the test without losing its history.
