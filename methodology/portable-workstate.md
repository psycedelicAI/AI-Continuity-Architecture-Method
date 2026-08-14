# Portable Workstate

## A Save-State for Human–AI Work

> The AI model can change.  
> The work should not have to start over.

When people work with an AI, important context often becomes trapped inside
one conversation, one account, or one provider.

The AI may understand the project today.

A different AI may know nothing about it tomorrow.

**AI Continuity** explores a different approach:

> Capture the state of the work at a particular point in time, then make that
> state portable between AI systems.

---

## The Basic Idea

A Portable Workstate is a structured snapshot of a project.

It describes:

- what the project is
- why it exists
- where the work currently stands
- what has already been decided
- which terms have special meaning
- how the concepts relate to one another
- what remains unresolved
- what is proposed but not yet approved
- what should happen next
- where important information came from

It is not a copy of a human mind.

It is not an attempt to give every AI access to a person's entire memory.

It is the **minimum meaningful context required to continue a body of work**.

---

## The Handover Analogy

Imagine working on a large project with one colleague.

At the end of the day, that colleague leaves and a new colleague arrives.

You do not need to explain your entire life to the new person.

You give them a useful handover:

- the purpose of the project
- the work already completed
- the important decisions
- the vocabulary used by the team
- the unresolved questions
- the next intended step

The new colleague is different, but the work can continue.

> **AI Continuity is that handover document for AI systems.**

---

## The Continuity Cycle

```text
┌──────────────────────────────┐
│  Human–AI work               │
│  ideas, decisions, progress  │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│  Validate and structure       │
│  separate fact from proposal │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│  Freeze a Workstate           │
│  create a versioned snapshot │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│  Transfer to another AI      │
│  ChatGPT, Lumo, or another   │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│  Reconstruct project context  │
│  continue from the snapshot  │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│  Human validation             │
│  approve, reject, or revise  │
└──────────────┬───────────────┘
               │
               ▼
        Next Workstate
