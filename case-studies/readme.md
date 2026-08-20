# Case Studies

This directory contains documented experiments related to the
AI Continuity Architecture Method.

The case studies examine how different AI systems interpret, continue, and
extend an existing project when provided with different context packages.

They are exploratory evidence—not claims of universal validation.

---

## Purpose

The purpose of these case studies is to investigate whether structured external
context can help an AI model:

- preserve project meaning across sessions;
- use established terminology;
- understand relationships between documents;
- continue an existing workflow;
- transfer context between models and platforms;
- distinguish confirmed decisions from model-generated proposals;
- reconstruct the project's intent and human meaning.

The experiments also document limitations, misunderstandings, formatting
differences, language behaviour, unsupported assumptions, and repair steps.

---

## Directory structure

```text
case-studies/
├── README.md
├── prompts/
│   └── standard-question-sequence.md
├── source/
└── analysis/
```

The exact filenames may change as the case-study collection develops.

---

## Shared question sequence

The same general working-session question sequence was used across multiple
test runs.

The complete sequence is preserved separately:

[View the standard question sequence](prompts/standard-question-sequence.md)

The sequence includes:

- context establishment;
- introduction of a new idea;
- design refinement;
- a documented repair step;
- file creation;
- repository placement;
- integration with existing documentation.

The prompts were written in Swedish.

This is an important test condition because the project context and technical
vocabulary were primarily written in English.

---

## Evidence layers

### `prompts/`

The questions and instructions given to the model.

This layer records what the human explicitly asked.

### `source/`

Raw model output preserved as closely as possible to the original response.

This material should not be silently corrected or rewritten.

### `analysis/`

Human-reviewed interpretation of the raw output.

Analysis documents may identify:

- successful context transfer;
- missing or distorted information;
- language behaviour;
- formatting failures;
- unsupported assumptions;
- repair steps;
- possible improvements;
- questions for future tests.

---

## Provenance

Every source and analysis file should identify:

- model;
- platform;
- date;
- supplied context;
- Memory Bank version;
- vocabulary or project documents supplied;
- intent prompt, if any;
- prompt language;
- response language;
- document language;
- raw-output location;
- canonical status;
- human-review status.

A result cannot be evaluated properly without knowing what the model actually
received.

---

## Language variables

The original experiments did not fully isolate language as a variable.

The prompts were written in Swedish, while much of the supplied project context
and technical vocabulary was written in English.

Future test runs should record:

| Variable | Description |
|---|---|
| Prompt language | Language used by the human |
| Response language | Language used by the model |
| Document language | Language used in created documents |
| Technical vocabulary | Language of project-specific terms |
| Language instruction | Whether output language was explicitly specified |
| Language drift | Whether the language changed during the run |

This allows semantic continuity and language behaviour to be evaluated separately.

---

## Limitations

These case studies do not constitute scientific proof.

The current evidence may be limited by:

- a small number of test runs;
- one primary model;
- one principal project context;
- changing context packages;
- mixed language conditions;
- lack of formal quantitative metrics;
- incomplete isolation of variables;
- human interpretation of model output;
- possible differences between platforms;
- model-generated content being mistaken for established project material.

The results should therefore be treated as exploratory and developmental.

---

## Future testing

Future experiments may compare:

- multiple AI models;
- the same question sequence across models;
- Swedish prompts versus English prompts;
- explicit versus implicit language instructions;
- different Memory Bank versions;
- monolithic versus modular context;
- semantic continuity versus formatting fidelity;
- document creation versus document placement;
- first-pass success versus repair-requiring workflows.

A future comparison should preserve the same question sequence wherever
possible and record all deviations.

---

> The raw output shows what the model produced.
>
> The prompts show what the human asked.
>
> The analysis shows what we think it means.
>
> The provenance shows what the result can actually prove.
