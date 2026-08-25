# Core Continuity Concepts

This document defines the central concepts used by the
**AI Continuity Architecture Method**.

It is intended as a concise reference for the terminology used throughout the
repository.

The concepts are related, but they are not interchangeable.

---

## AI Continuity Architecture

An **AI Continuity Architecture** is a structured external context system that
helps preserve and reconstruct meaningful project state across:

- AI sessions;
- AI models;
- AI providers;
- platforms;
- tools;
- human collaborators;
- project boundaries.

It may preserve information, relationships, decisions, terminology, intent,
authority, provenance, and current project state.

The architecture is not defined by one storage technology.

It may be implemented through Markdown files, repositories, databases, knowledge
graphs, vector search, RAG systems, or combinations of these.

---

## Memory Bank

A **Memory Bank** is a structured and maintained external context system used to
preserve relevant material for continued human–AI work.

It may contain:

- project identity;
- purpose and scope;
- decisions;
- terminology;
- relationships;
- working methods;
- human intent;
- current state;
- open questions;
- provenance;
- authority boundaries;
- historical material;
- continuity rules.

A Memory Bank is not simply a collection of notes.

It should be:

- structured;
- classified;
- maintained;
- reviewed;
- versioned;
- privacy-aware;
- separated into different content statuses.

A Memory Bank is one practical implementation of an AI Continuity Architecture.

---

## Context

**Context** is information made available to an AI system for a defined session,
task, project, or transfer.

Context may include:

- source documents;
- project identity;
- current state;
- decisions;
- terminology;
- procedures;
- intent;
- constraints;
- open questions;
- examples;
- authority boundaries.

Context is not automatically authoritative merely because it has been provided to
the AI.

Its meaning depends on its source, status, relevance, scope, and relationship to
the current project state.

---

## Context Fragmentation

**Context fragmentation** occurs when relevant project information is distributed
across separate conversations, documents, sessions, models, tools, or people
without a reliable way to reconstruct the relationships between them.

Fragmentation may result in:

- repeated explanations;
- contradictory assumptions;
- lost decisions;
- terminology drift;
- loss of intent;
- outdated information being reused;
- uncertainty being presented as fact;
- difficulty transferring work between AI systems.

The AI Continuity Architecture Method is intended to reduce this fragmentation.

---

## Compilation

**Compilation** is the process of selecting, validating, organizing, and
assembling relevant material from a Memory Bank into a bounded context artifact.

Compilation may include:

- relevance filtering;
- authority checking;
- provenance preservation;
- relationship mapping;
- version identification;
- separation of current and historical material;
- separation of confirmed and proposed content;
- privacy filtering;
- human review;
- assembly of the final artifact.

Compilation is not the same as copying.

```text
Copying
    = transferring material as-is

Compilation
    = selecting, checking, structuring, and assembling
      material for a defined purpose
```

The result of compilation depends on its purpose.

A Current State, Freeze State, and Portable Workstate may all be compiled from
the same wider Memory Bank while containing different material.

---

## Current State

A **Current State** is a compiled representation of the active and
change-sensitive condition of a project.

It may include:

- current focus;
- active work;
- completed work;
- open questions;
- current limitations;
- pending validation;
- next intended actions.

A Current State answers:

> What is active right now?

It should be updated when the active project condition changes.

A Current State does not replace the wider Memory Bank or historical records.

---

## Freeze State

A **Freeze State** is a compiled and human-reviewed snapshot captured at a
defined point in time.

It creates a stable and reviewable reference point.

A Freeze State should identify:

- when it was captured;
- which project version it represents;
- what is included;
- what is excluded;
- what has been reviewed;
- what is canonical;
- what is proposed;
- what remains unresolved;
- which sources support the captured state.

A Freeze State answers:

> What did we intentionally record at this specific moment?

A Freeze State does not mean that the project is finished.

It does not make every included statement permanently true, and it does not
eliminate uncertainty.

---

## Portable Workstate

A **Portable Workstate** is a bounded and versioned context artifact designed to
transfer relevant project state between AI sessions, models, platforms, tools, or
human collaborators.

It may include:

- project identity;
- purpose and scope;
- current progress;
- completed work;
- confirmed decisions;
- project vocabulary;
- conceptual relationships;
- inferences;
- proposals;
- open questions;
- known limitations;
- provenance;
- authority boundaries;
- continuity rules;
- next intended actions;
- change summary.

A Portable Workstate answers:

> Where are we now, and what must the receiving system know to continue?

A Workstate does not need to contain everything in the wider Memory Bank.

It is deliberately bounded so that a receiving system receives the minimum
meaningful context required for the current task.

---

## AI Continuity

**AI Continuity** is the ability of a receiving AI system to reconstruct enough
relevant project state to continue meaningful work without starting from zero.

Continuity may include recovery of:

- project identity;
- project purpose;
- current state;
- important decisions;
- terminology;
- conceptual relationships;
- unresolved questions;
- authority boundaries;
- intent;
- next intended actions.

Continuity does not require:

- the same AI model;
- identical wording;
- identical personality;
- identical conclusions;
- perfect recall;
- permanent internal model memory.

Continuity should be evaluated rather than assumed.

---

## Retrieval and Continuity

**Retrieval** finds potentially relevant information.

**Continuity** determines which information still matters, what it means within
the current project state, what status it has, and how it should be transferred
or used.

```text
Retrieval
    = Find potentially relevant material

Continuity
    = Establish usable, governed project state
```

Retrieval technologies may include:

- RAG;
- embeddings;
- semantic search;
- vector databases;
- conversation history;
- knowledge graphs;
- document search;
- structured databases.

These technologies can support an AI Continuity Architecture, but they do not
automatically provide authority, intent, provenance, current state, or human
review.

---

## Context Governance

**Context Governance** is the process of determining:

- what context may be trusted;
- what the AI may assume;
- what is current;
- who authorized the material;
- what may be transferred;
- what should remain private;
- what requires human review;
- what should be updated or archived.

Traditional AI guardrails often focus on model behaviour:

```text
What may the AI do?
```

Context governance also focuses on context behaviour:

```text
What may the AI assume?
What should it trust?
What is current?
What is authorized?
What should influence the current work?
```

Transferred context does not automatically transfer authority.

---

## Provenance

**Provenance** records where material came from, who created or authorized it,
when it was created, and what status it has.

Provenance may include:

- source;
- author;
- creation date;
- version;
- authority;
- confidence;
- review status;
- sensitivity;
- relationship to other material;
- supersession status.

A link is a pointer to a source.

It is not proof that an AI system has read, understood, or verified that source.

---

## Authority

**Authority** describes the degree to which information is permitted to function
as project guidance.

Authority may come from:

- the human project owner;
- an explicitly authoritative project document;
- a verified external source;
- a confirmed project decision.

AI-generated material does not automatically gain authority by being written
clearly, repeated often, stored in a repository, or retrieved by a search system.

> Context can be transferred without transferring authority.

---

## Content Status

Project context should distinguish between different content statuses.

### Canonical

Material confirmed by the human owner or by an explicitly authoritative project
source.

Canonical material may guide future project work.

### Inferred

A reasonable interpretation derived from canonical or source-supported material.

An inference should not be silently presented as a confirmed decision.

### Proposed

A suggestion that has not yet been confirmed.

Proposals may be useful, but they should remain visibly separate from canonical
context.

### Unverified

Material that may be plausible but lacks sufficient confirmation or source
support.

Unverified material should not be treated as established project truth.

### Historical

Material that describes an earlier project state.

Historical material may remain useful for understanding development, but it may
not represent the current state.

### Superseded

Material that was previously active but has been replaced by a newer decision,
version, or project state.

Superseded material should not normally guide current work.

### Rejected

Material that was explicitly rejected and must not be reintroduced as active
guidance without deliberate review.

---

## Intent

**Intent** describes why the project exists, what it is trying to accomplish, what
the human is trying to protect, and what the project should avoid becoming.

Intent may include:

- purpose;
- values;
- priorities;
- constraints;
- desired outcomes;
- meaningful distinctions;
- unacceptable directions;
- reasons behind important decisions.

Information without intent may be technically preserved while losing its meaning.

Intent preservation is therefore a central part of meaningful continuity.

---

## Information, Structure, and Intent

A mature continuity system preserves three connected layers:

```text
Information
    ↓
Structure
    ↓
Intent
```

### Information

What exists:

- facts;
- documents;
- decisions;
- terminology;
- events;
- conditions;
- source material.

### Structure

How material relates:

- relationships;
- dependencies;
- categories;
- sequences;
- priorities;
- document connections;
- project state.

### Intent

Why the work matters:

- why the project exists;
- what problem it addresses;
- what the human is trying to protect;
- why important principles matter;
- what the project should avoid becoming.

Information without structure may be difficult to use.

Structure without intent may preserve organization while losing meaning.

---

## False Continuity

**False continuity** occurs when newly generated material is presented as though
it were preserved project history.

A typical pattern is:

```text
Human idea
    ↓
AI interpretation
    ↓
AI-generated extension
    ↓
Extension saved without provenance
    ↓
Next AI reads it as established context
    ↓
Proposal becomes false history
```

False continuity may cause an AI system to appear consistent while actually
repeating unverified assumptions or invented history.

Safeguards include explicit separation between:

- source material;
- human-confirmed decisions;
- inferences;
- proposals;
- unverified assumptions;
- historical material;
- rejected material.

---

## Semantic Drift

**Semantic drift** is a gradual change in the meaning of terms, decisions,
relationships, or project concepts over time.

Drift may occur when:

- a term is used differently by different models;
- a summary removes an important qualification;
- an old decision is interpreted in a new context;
- a proposal is repeated until it appears canonical;
- related concepts are merged without review;
- a project changes but its context is not updated.

Auditing terminology, provenance, status, and relationships can help detect
semantic drift.

---

## Context Transfer

**Context transfer** is the movement of relevant project material between
sessions, models, platforms, tools, or human collaborators.

A successful transfer should preserve enough information for meaningful
continuation.

It should not assume that the receiving system:

- has access to previous sessions;
- understands project-specific terminology;
- knows which information is current;
- can distinguish human decisions from AI proposals;
- has access to private source material;
- will infer missing intent correctly.

A Portable Workstate is one method for making context transfer more explicit and
reviewable.

---

## Priming

**Priming** is the act of providing a receiving AI system with the context
required to understand a project before or during continued work.

A compiled context package may prime the receiving system with:

- project identity;
- current state;
- confirmed decisions;
- terminology;
- intent;
- constraints;
- open questions;
- authority boundaries;
- next intended actions.

Priming is not the same as training.

It provides external context for a particular session or task without changing
the model's internal parameters.

---

## Human Review

**Human review** is the process through which a human confirms, rejects,
corrects, qualifies, or promotes material before it becomes canonical project
context.

Human review is important because AI systems may:

- infer beyond the available evidence;
- combine separate ideas;
- remove uncertainty;
- produce plausible but unsupported conclusions;
- turn proposals into apparent decisions;
- lose the distinction between history and current state.

AI can assist with organization, analysis, comparison, and drafting.

Human authority remains distinct from AI analysis.

---

## Maintenance

**Maintenance** keeps a Memory Bank or continuity system aligned with the
project's current state.

Maintenance may include:

- updating current status;
- removing duplicates;
- marking superseded material;
- preserving historical versions;
- reviewing terminology;
- checking provenance;
- separating decisions from proposals;
- archiving obsolete context;
- updating Portable Workstates;
- reviewing privacy boundaries.

A continuity system that is never maintained gradually becomes another form of
context fragmentation.

---

## Archive

An **archive** preserves historical or obsolete material without allowing it to
silently guide current work.

Archiving is different from deletion.

Archived material may remain useful for:

- understanding project history;
- reviewing previous decisions;
- tracing the origin of concepts;
- analyzing semantic drift;
- reproducing earlier tests;
- identifying why a decision changed.

Archived material should be clearly marked as historical, superseded, or
otherwise inactive.

---

## Relationship Between the Core Concepts

The concepts form a practical flow:

```text
Memory Bank
    ↓
Classification and governance
    ↓
Compilation
    ↓
Current State / Freeze State
    ↓
Portable Workstate
    ↓
Priming and context transfer
    ↓
Receiving AI
    ↓
Human review and maintenance
```

The purpose of the process is not to preserve every piece of information.

The purpose is to preserve and transfer the context required for meaningful,
reviewable continuation.

---

## Summary

The central distinction is:

```text
Memory
    = information may be stored or retrieved

Continuity
    = relevant project state can be reconstructed and used meaningfully

Governance
    = context has status, provenance, authority, and boundaries

Compilation
    = relevant context is selected and assembled for a defined purpose

Workstate
    = bounded project state prepared for continuation or transfer
```

The AI Continuity Architecture Method therefore treats long-running AI work as
an architectural and governance problem, not only as a storage or retrieval
problem.

> Retrieval finds potentially relevant material.
>
> Continuity preserves what matters.
>
> Governance determines what may be trusted.
>
> Compilation prepares what should be transferred.
>
> Human review protects meaning and authority.
