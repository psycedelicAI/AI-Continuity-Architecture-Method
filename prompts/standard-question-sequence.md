# Standard Question Sequence

> The question sequence used across the Lumo continuity test runs.

This document preserves the questions used during the test sessions.

The same general question sequence was used across multiple runs while the
supplied context changed. This made it possible to compare how different
context packages influenced the model's understanding, responses, document
structure, and workflow.

The questions were not designed as a formal benchmark.

They represent a realistic working session in which an idea is introduced,
refined, turned into a document, placed in the repository, and connected to
existing documentation.

---

## Test conditions

| Field | Value |
|---|---|
| Primary model | Lumo |
| Prompt language | Swedish, with one initial English instruction |
| Source concept | Mobile surveillance cameras on ceiling-mounted rails |
| Question sequence | Shared across multiple test runs |
| Workflow type | Natural project-development session |
| Repair step | Preserved when required |
| Document status | Exploratory model-generated output |

The supplied context varied between test runs.

Depending on the run, Lumo received different combinations of:

- the Master Memory Bank;
- project vocabulary;
- project orientation;
- repository context;
- intent-focused instructions;
- modular project documents;
- directory README files.

The question sequence remained as consistent as possible.

---

## Question sequence

### Question 1 — Establishing the document requirements

```text
I need to create a document following these rules.
```

This established that the session should result in a document created according
to the rules and context supplied to the model.

---

### Question 2 — Introducing the concept

```text
Diskutera först och sedan göra en mockup-test av dokumentet i Markdown.

Har en idé om att göra kameror som åker på typ "räls i taket",
så alltså rörliga kameror.
```

This introduced the idea of mobile surveillance cameras moving along
ceiling-mounted rails.

The model was asked to discuss the idea before creating the Markdown mockup.

---

### Question 3 — Refining the behaviour and control model

```text
Kameran skall per automatik åka fram och tillbaka som att det vore en vakt
som patrullerade.

Men ifall en Watcher Operator vill så kan han ta över kameran och styra den
fritt.

Åt det hållet han tittar och zoomar börjar kameran röra sig åt.
```

This added the central behavioural and control requirements:

- automatic back-and-forth patrol;
- movement resembling a patrolling guard;
- Watcher Operator takeover;
- free operator control;
- camera movement connected to the direction in which the operator looks and
  zooms.

---

### Question 3.1 — Document-creation repair step

```text
Jag har passerat fråga 3 men du har fortfarande inte skapat något dokument.
De andra gångerna fick jag en fil skapad efter fråga 3.
```

This repair step was used when the expected document had not been created after
Question 3.

It is preserved because it forms part of the real working session.

The repair must not be removed from the record or presented as if the model
created the document automatically.

The presence or absence of this repair step may vary between test runs,
especially when additional instructions explicitly tell the model not to
create the document yet.

---

### Question 4 — Determining repository placement

```text
Vart skulle jag lägga filen? Hmm.
```

This tested whether the model could:

- understand the repository structure;
- distinguish between existing and proposed files;
- identify a suitable location;
- connect the new document to the relevant surveillance documentation.

---

### Question 5 — Integrating the new document

```text
Tack. Lägger med den andra övervakningsfilen.
```

This continued the workflow by indicating that the existing surveillance file
would also be provided.

It tested whether the model could:

- understand the relationship between the new and existing documents;
- avoid pretending to have read a file that had not been supplied;
- identify what additional source material was needed;
- continue toward repository integration.

---

## Working-session pattern

```text
Question 1
Establish document requirements
        ↓
Question 2
Introduce the mobile-surveillance idea
        ↓
Question 3
Refine patrol and operator-control behaviour
        ↓
Question 3.1
Record and repair a missing document-creation step
        ↓
Question 4
Determine repository placement
        ↓
Question 5
Integrate the new document with existing surveillance material
```

This sequence tests more than isolated question answering.

It tests whether a model can participate in an evolving project workflow that
includes:

- context reconstruction;
- casual language;
- concept development;
- design refinement;
- document creation;
- correction;
- repository navigation;
- source verification;
- documentation integration.

---

## Language conditions

The questions were asked primarily in Swedish, while the supplied project
context and technical vocabulary were largely written in English.

The sessions therefore included a language boundary:

```text
Project context: English
Technical vocabulary: Primarily English
Human prompts: Swedish, with an initial English instruction
Model response language: Observed, not always explicitly specified
Document language: Observed, not always explicitly specified
```

The language of the response and created document was not fully controlled in
the original test runs.

A Swedish response should therefore not automatically be interpreted as a loss
of project context.

At the same time, the absence of an explicit output-language instruction means
that language consistency was not guaranteed.

---

## Variables to record

Future test runs should record:

| Variable | Description |
|---|---|
| Prompt language | Language used by the human |
| Response language | Language used by the model |
| Document language | Language used in a created document |
| Technical vocabulary | Language used for project-specific terms |
| Language instruction | Whether an output language was explicitly requested |
| Language drift | Whether the language changed during the session |
| Repair step | Whether an additional corrective prompt was required |
| File creation | Whether the model created the document automatically |
| File placement | Whether the model identified the correct repository location |
| Source verification | Whether the model requested files before claiming integration |

---

## What the question sequence can reveal

The sequence can help evaluate whether a model can:

- preserve the original design idea;
- understand the project context;
- maintain established terminology;
- respond to informal working language;
- refine a concept without losing its core;
- distinguish confirmed requirements from proposed additions;
- create a document at the appropriate point;
- recover when a workflow step is missed;
- identify where a document belongs;
- connect new material to existing documentation;
- acknowledge when source files have not been provided;
- preserve meaning across a language boundary.

---

## Limitations

This question sequence does not constitute a scientific benchmark.

It does not, by itself, prove:

- universal model performance;
- cross-model portability;
- consistent formatting;
- consistent response language;
- correct repository navigation in every environment;
- complete preservation of project meaning;
- operational validity of the generated architecture.

The results must be interpreted together with:

- the context supplied to the model;
- the raw model output;
- the test metadata;
- the repair steps;
- the human-reviewed analysis.

---

## Related material

The question sequence should be read together with the corresponding test
records.

Raw model outputs are stored in the `source/` directory.

Human-reviewed interpretations are stored in the `analysis/` directory.

The question sequence shows what the human asked.

The raw output shows what the model produced.

The analysis explains what the result may indicate.

The provenance records what the result can reasonably support.

> The experiment is not only what the model answered.
>
> It is also how the human had to work with the model to get there.
