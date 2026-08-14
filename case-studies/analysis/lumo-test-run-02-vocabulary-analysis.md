# Test Run 02 Analysis — Lumo with Memory Bank and Vocabulary

## Test Identity

| Field | Value |
|---|---|
| Test run | 02 |
| Test type | Cross-model continuity comparison |
| Model | Lumo |
| Platform | Lumo |
| Memory Bank | Provided |
| Project vocabulary | Provided |
| Task-specific priming | Not provided |
| Source idea | Mobile surveillance |
| Comparison target | Test Run 01 — Memory Bank only |
| Raw output | [Test Run 02 source output](../source/mobile-surveillance-test-run-02-memory-bank-plus-vocabulary.md) |

---

## Objective

The purpose of Test Run 02 was to repeat the Test Run 01 workflow while adding
the project vocabulary.

The goal was to observe whether vocabulary improved:

- terminology
- document structure
- architectural relationships
- repository navigation
- preservation of the original design idea
- procedural continuity

Only the context package was changed. The model, platform, source concept, and
question sequence were intended to remain the same.

---

## Test Conditions

Test Run 02 used:

- The Master Memory Bank
- The project vocabulary
- The same mobile surveillance concept used in Test Run 01
- The same question sequence as Test Run 01
- The same general requirement to discuss the idea before generating a draft

Test Run 02 did not use:

- A separate task-specific priming document
- The complete facility repository as verified context
- The existing surveillance model as an uploaded source file

---

## Output Overview

Lumo generated a more operationally structured version of the mobile
surveillance concept.

The output included:

- autonomous patrol state
- operator override state
- gaze-to-move mapping
- trust-state transitions
- movement-aware security
- control hierarchy
- zone-crossing considerations
- degraded operations
- recovery
- audit and attribution
- movement validation
- repository placement recommendations

Compared with Test Run 01, the output placed greater emphasis on camera states,
control authority, movement as a signal, and operational governance.

---

## Observed Improvements Compared with Test Run 01

### 1. Stronger Terminological Continuity

The output used project-related concepts more explicitly, including:

- trust state
- privileged access
- degraded operations
- recovery
- signaling
- governance
- audit
- zone boundaries

The vocabulary appeared to help Lumo use the project's conceptual language
instead of relying only on generic security terminology.

### 2. Clearer State-Based Structure

Test Run 02 organized the model around:

1. Autonomous Patrol State
2. Operator Override State
3. Gaze-to-Move Mapping

This gave the concept a clearer operational structure than the first test.

### 3. Stronger Control and Governance Model

Test Run 02 introduced a more explicit control hierarchy involving:

- autonomous system control
- watcher operator control
- incident command
- maintenance access
- controller preemption
- handoff protocols
- attribution and review

Some of these are model-generated proposals and are not confirmed
architecture decisions.

### 4. Better Repository Navigation

When asked where the document should be placed, Lumo recommended:

```text
[docs/mobile-surveillance-model.md](https://mobile-surveillance-model.md)
