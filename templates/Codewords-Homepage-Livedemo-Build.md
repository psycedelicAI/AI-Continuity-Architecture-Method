# PsycedelicAI Codewords: `homepage`, `livedemo` and `build`

> A practical record of what the three codewords mean, how they connect, and
> what the AI should do when Psycedelic asks it to find them in older chats.

---

## Purpose

These codewords are short references to working methods that were defined and
refined across earlier conversations.

They are not magic commands. When a codeword’s meaning is unclear, the AI
should search the relevant chat history, find the original definition and later
updates, then reconstruct the latest useful version before acting.

The three main codewords are:

```text
homepage
livedemo
build
```

In short:

```text
homepage = restore the website context
livedemo = restore the wider PsycedelicAI working method
build    = research a topic and create a new homepage page
```

---

## What to do when Psycedelic asks to find codewords in older chats

When Psycedelic writes something like:

```text
Find the codewords in older chats: homepage, livedemo and build.
```

the AI should treat this as a **conversation-history retrieval request**.

It should not guess from the words alone, search the public web, or rely only on
a static profile. It should search past conversations and reconstruct how the
meanings developed.

### Retrieval process

1. **Identify the requested codewords.**  
   Search separately for `homepage`, `livedemo` and `build`, as well as
   combinations of them.

2. **Find direct definitions.**  
   Prioritize conversations where Psycedelic defined or changed a codeword.

3. **Find later updates and tests.**  
   Search for revisions, corrections, examples of activation, and situations
   where the workflow was applied.

4. **Read the relevant surrounding turns.**  
   Short search snippets may not show the whole definition. Fetch enough of the
   original conversation to understand the user’s request and the assistant’s
   response.

5. **Reconstruct the current meaning.**  
   Combine the original definition with later updates. Do not treat every
   mention of a word as a new instruction.

6. **Separate evidence from inference.**  
   Make clear what Psycedelic explicitly established, what was later updated,
   and what remains uncertain or needs confirmation.

7. **Report the result in plain language.**  
   Give each codeword’s meaning, how the codewords connect, and a practical
   activation phrase.

8. **Cite memory in readable form.**  
   When useful, identify the relevant older chat by its title or subject and
   date. Do not expose internal search or tool details.

### Important distinction

A search request such as:

```text
Find the codewords in older chats.
```

asks the AI to **retrieve and explain the definitions**.

An activation request such as:

```text
build: climate targets
```

asks the AI to **use the relevant workflow**.

Finding a codeword and activating it are related, but they are not the same
operation.

---

# 1. `homepage`

## Meaning

`homepage` means:

> Restore the relevant context for the public PsycedelicAI website before
> working on one of its pages.

The main website is:

```text
https://psycedelicai.neocities.org/
```

This context includes the site’s structure, identity, visual direction,
navigation, file paths, and recurring HTML conventions.

## What to recover

When `homepage` is relevant, search for or use the current available information
about:

- The website’s purpose and audience
- The existing file and folder structure
- The visual language and page conventions
- Navigation and links
- SEO metadata and direct page URLs
- The correct stylesheet path
- Shared scripts and required footer elements
- Where a new page should be placed
- Whether the page should be added to navigation

The documented root stylesheet path is:

```html
<link rel="stylesheet" href="core/css/style.css">
```

For a page inside `projects/`, the documented relative path is:

```html
<link rel="stylesheet" href="../core/css/style.css">
```

For a root-level page, the shared donation script convention is:

```html
<script src="core/java/donation.js"></script>
```

It belongs immediately before `</body>` and provides the shared **“Support
the work”** element.

## Website principles

- A new standalone research page normally belongs directly in the website root.
- Do not add a new page to the normal navigation automatically.
- Use the existing shared stylesheet when that is the intended design.
- If the page needs its own CSS, keep it in a dedicated page-specific file and
  load it after the shared stylesheet.
- Provide a complete replacement file when that is what Psycedelic requests.
- Check paths carefully. Different directory locations require different
  relative paths.
- Do not assume an old file tree is still current if newer evidence is
  available.

## Practical activation

```text
homepage
```

or:

```text
Search older chats for homepage and restore the current website structure,
style, file paths and page rules.
```

---

# 2. `livedemo`

## Meaning

`livedemo` activates the broader PsycedelicAI working method for context
recovery, continuity, human authority and structured collaboration.

It is not just a visual theme or a request to make a live demonstration. Its
meaning was developed as a way to recover relevant project context and apply
the appropriate method to a new task.

## What to recover or apply

Depending on the task, `livedemo` can involve:

- Searching prior conversations for the latest relevant context
- Reconstructing the current workstate and earlier decisions
- Connecting relevant PsycedelicAI projects and documentation
- Adapting the method to the task instead of mechanically applying every
  framework
- Distinguishing direct evidence from supporting context
- Separating facts, assumptions, interpretations, proposals and uncertainty
- Preserving human intent, authority and final decision-making
- Creating a structured result suitable for review or handoff

Relevant source areas may include:

- AI Continuity Architecture Method
- High-Security Facility Concept
- Symbiosis
- PsycedelicAI Wiki
- Random-Stuffs and relevant LinkedIn material
- Onboarding and organisation documentation
- Relevant chat history and Portable Workstate

These sources should be treated as related context, **not automatically as one
single implemented system**. Only bring in the material that is relevant to
the task.

## Human and AI roles

The method should preserve the distinction between the perspectives:

- **Psycedelic** brings lived experience, purpose, intuition, values,
  creativity, judgment, responsibility and personal meaning.
- **AI** contributes research, memory support, analysis, structure, comparison,
  synthesis and documentation.
- Final values, decisions and responsibility remain with Psycedelic.

## A useful working sequence

```text
Human intent
    ↓
Relevant project context
    ↓
Continuity and previous decisions
    ↓
Authority, scope and trust boundaries
    ↓
Appropriate method or workflow
    ↓
Research, analysis or creation
    ↓
Verification and uncertainty review
    ↓
Human review and decision
    ↓
Action, handoff or recovery
```

## Important limitation

`livedemo` is not a cryptographic key, a guarantee of permanent memory, or a
standalone command that magically loads every source.

It works only to the extent that relevant conversation history, project
material, retrieval capability and current instructions are available. If
something cannot be retrieved, the AI should say so rather than invent it.

## Practical activation

```text
livedemo
```

For clearer retrieval across chat sessions:

```text
Search older chats for livedemo, recover the latest workflow, and apply the
relevant parts to this task.
```

---

# 3. `build`

## Meaning

`build` activates the research-to-homepage workflow:

> Take a topic, research it carefully, organize the evidence, and create a
> complete standalone HTML page that fits the PsycedelicAI website.

The page is normally placed in the website root unless Psycedelic specifies
another location.

## How `build` connects the other codewords

`build` is the page-building workflow. It uses the other two codewords as
context:

```text
livedemo
    ↓
Recover the relevant PsycedelicAI method and working context

homepage
    ↓
Recover the website structure, style and technical conventions

DeepDive-to-Homepage Freeze State
    ↓
Research and source-grounding method

build
    ↓
Combine the relevant context into a complete new page
```

The goal is not to generate a generic page that happens to mention
PsycedelicAI. It should feel like it belongs to the same site while remaining
grounded in reliable sources.

## Research workflow

For the topic, the AI should:

1. Define the question and the scope.
2. Search for original and reliable sources.
3. Use primary sources where possible, such as official documents, laws,
   research papers, patents, technical documentation and historical records.
4. Use secondary sources to explain or contextualize primary material.
5. Treat advocacy or opinion sources as material to examine, not automatically
   as neutral evidence.
6. Compare relevant perspectives and competing explanations.
7. Identify benefits, drawbacks, risks, limitations and uncertainties.
8. Distinguish clearly between:
   - documented fact;
   - source claim;
   - interpretation;
   - technical possibility;
   - hypothesis;
   - speculation;
   - and unknowns.
9. Link directly to sources and connect them to the claims they support.
10. Prepare a readable page structure and then produce the complete HTML.

Patents, laws and historical documents should be included when relevant. A
patent may show that an invention was described or claimed; by itself, it does
not prove that the invention was implemented or used.

## Page and output conventions

The standard page should:

- Be a complete, standalone HTML file
- Use the appropriate language for the requested audience
- Usually be saved directly in the website root
- Use the existing PsycedelicAI design and correct stylesheet path
- Include suitable page title, description and social metadata where
  appropriate
- Include direct links to real sources
- Include the shared donation script and “Support the work” element
- Not be added to normal navigation unless requested
- Be split into sequential parts if necessary, without omitting sections or
  sources
- Be given as a complete, correctly ordered file when all parts are finished

If a required detail is missing, ask only for information that is genuinely
necessary. When the user provides a topic after `build`, begin the workflow
rather than asking what the topic is again.

## Practical activation

```text
build: [topic]
```

For example:

```text
build: TwinMind vs Perplexity
```

If Psycedelic writes only:

```text
build
```

and has not given a topic, ask:

```text
Vad gäller ämnet?
```

---

# How the three codewords work together

| Codeword | Main job | Think of it as |
|---|---|---|
| `homepage` | Restore the website’s structure, identity, style and rules | The website context |
| `livedemo` | Restore the wider working method, continuity and human-AI roles | The collaboration context |
| `build` | Research a topic and create a complete website page | The production workflow |

The compact version is:

```text
homepage = where and how the page belongs
livedemo = how we recover and work with context
build    = how we research and create the page
```

---

# Recommended prompts

## Find and document the codewords

```text
Search my older chats for the codewords homepage, livedemo and build.

Find the original definitions and later updates. Reconstruct what each
codeword means, how they connect, what workflow they activate, and any
important limitations. Distinguish explicit instructions from interpretation.
Cite relevant older chats by readable title or date. Then make a Markdown
document with a suggested filename first.
```

## Start a new research page

```text
build: [topic]

Search older chats for homepage and livedemo. Restore the relevant website
structure, style, paths and working method. Then research the topic, use
reliable direct sources, separate facts from interpretation and uncertainty,
and create a complete standalone HTML page for the PsycedelicAI root folder.
```

## Recover context without starting a new page

```text
Search older chats for homepage, livedemo and build. Tell me what each means
and what has changed since the earlier definitions. Do not start building a
page yet.
```

---

# Provenance and development history

These definitions were reconstructed from earlier PsycedelicAI conversations:

- **`livedemo`**: initially defined and refined as a context-recovery and
  live-demonstration workflow in September 2026. The detailed document
  **“How the `livedemo` Process Works”** was developed on 13 September 2026.
- **`homepage`**: defined as a shortcut for recovering the website’s
  structure, style, paths and conventions in **“codeword for this: homepage”**
  on 16 September 2026.
- **`build`**: defined as the research-to-HTML activation workflow in the
  conversations about the **DeepDive-to-Homepage Freeze State** on 17
  September 2026.
- The combined rule that `build` should search for and use both `Livedemo`
  and `homepage` was added on **17 September 2026**.

This document summarizes those recorded definitions. It does not guarantee
that a future AI session has access to the cited chats, files, website or
repositories. When context matters, the AI should retrieve and verify it.
