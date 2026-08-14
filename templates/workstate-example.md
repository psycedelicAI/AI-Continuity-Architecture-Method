workstate:
  id: high-security-facility
  version: 0.4.2
  created: 2026-08-15
  status: active

project:
  purpose: >
    Develop a conceptual high-security facility architecture
    based on trust, contextual authorization, observation,
    recovery, and accountable human control.

completed:
  - core architecture
  - trust model
  - watcher architecture
  - surveillance concept
  - degraded operations

current_focus:
  - cross-model continuity testing

canonical_decisions:
  - id: decision-001
    statement: AI supports accountable operators
    status: canonical
    source: human-confirmed

proposals:
  - id: proposal-001
    statement: mobile camera movement may carry operational meaning
    status: proposed
    requires_review: true

open_questions:
  - How should provenance be preserved across model transfers?
  - How can continuity be measured consistently?
  - Which context is necessary for another model to continue the work?

next_action:
  - compare the same Workstate across multiple AI models
