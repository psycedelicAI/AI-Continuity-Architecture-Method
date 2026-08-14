# Memory Bank Method

## Purpose

The Memory Bank Method is a practical process for building and maintaining
structured AI context.

It helps preserve the information, decisions, terminology, and intent required
to continue meaningful work across separate AI sessions.

> Build for continuity. Maintain for accuracy. Audit for drift.

---

## What Is a Memory Bank?

A Memory Bank is not simply a collection of notes.

It is a structured and maintained context system that allows an AI to recover
the relevant background of an ongoing project without starting from zero after
a session break.

A Memory Bank may preserve:

- Project identity
- Purpose and scope
- Core concepts
- Important decisions
- Canonical terminology
- Writing and working preferences
- Open questions
- Known contradictions
- Current project status
- Historical context

---

## The Memory Bank Lifecycle

### 1. Identify

Determine what information must survive between AI sessions.

This may include:

- Decisions that affect future work
- Definitions that must remain consistent
- Project goals and boundaries
- Important relationships between concepts
- Human intent behind the project
- Unresolved questions

Not every conversation detail belongs in the Memory Bank.

---

### 2. Collect

Gather relevant information from available sources, such as:

- Previous AI conversations
- Project documents
- Decision records
- User-provided notes
- Repository files
- Existing templates
- Meeting summaries

Each item should retain its source whenever possible.

---

### 3. Classify

Organize information according to its purpose, stability, and sensitivity.

Possible categories include:

- Identity
- Project context
- Core principles
- Decisions
- Terminology
- Working preferences
- Open questions
- Temporary notes
- Historical records
- Sensitive information

Classification prevents unrelated information from being treated as equally
important or equally permanent.

---

### 4. Consolidate

Combine related information into clear, canonical sections.

During consolidation:

- Remove unnecessary duplication
- Preserve important distinctions
- Resolve contradictory definitions
- Link related concepts
- Separate decisions from ideas
- Keep historical material available without letting it override current state

The goal is not to preserve every sentence. The goal is to preserve meaning.

---

### 5. Validate

Review the consolidated Memory Bank for:

- Accuracy
- Relevance
- Internal consistency
- Outdated information
- Unclear terminology
- Missing context
- Accidental disclosure of sensitive information

A Memory Bank should not be considered reliable merely because it is
well-written.

---

### 6. Prime

Create a focused context package for a new AI session.

The priming context should provide:

- The project identity
- The current objective
- Relevant terminology
- Important previous decisions
- Current constraints
- Known uncertainties
- The specific task for the new session

Only relevant context should be included. More context is not always better.

---

### 7. Maintain

Update the Memory Bank when meaningful changes occur.

Maintenance may include:

- Recording new decisions
- Updating definitions
- Removing obsolete instructions
- Adding newly discovered relationships
- Updating project status
- Revising the priming context
- Marking unresolved contradictions

Maintenance should happen throughout the project, not only at the end.

---

### 8. Audit

Periodically inspect the Memory Bank for semantic drift.

An audit should look for:

- The same concept using different names
- Different concepts using the same name
- Duplicate or overlapping sections
- Old decisions still presented as current
- Contradictory instructions
- Missing source information
- Assumptions presented as facts

If a contradiction cannot be resolved, it should be recorded explicitly rather
than silently hidden.

---

### 9. Archive

Move obsolete or historical material to an archive instead of deleting it
immediately.

Archived material should not normally be used as active context, but it may
remain valuable for:

- Understanding how the project developed
- Recovering earlier decisions
- Comparing changes over time
- Identifying recurring failure patterns

---

## Recommended Metadata

Important entries should include metadata such as:

```yaml
status: proposed
confidence: medium
source: conversation
last_reviewed: YYYY-MM-DD
sensitivity: internal
