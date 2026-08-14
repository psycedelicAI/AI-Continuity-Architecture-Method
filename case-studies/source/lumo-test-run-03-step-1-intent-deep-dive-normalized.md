> **Transformation:** Markdown formatting normalized from the raw Lumo output.
> No intentional semantic changes were made.
>
> **Source:** [Raw Lumo output](lumo-test-run-03-step-1-intent-deep-dive-raw.md)



# Dynamic Surveillance Model – High-Security Facility Concept

> A conceptual model describing how movable camera systems combine automated patrol behavior with operator-controlled tracking in a governed trust architecture.

## Document Information

| Field | Value |
|---|---|
| Document | Dynamic Surveillance Model |
| Subject | High-Security Facility Concept |
| Type | Trust Architecture & Surveillance |
| Status | Draft |
| Scope | Movable camera systems, patrol logic, operator control, gaze-to-motion interface |
| Audience | Security architects, governance designers, surveillance operators |
| Provenance | Exploratory model output for PsycedelicAI project |
| Test Metadata | Concept draft for review and validation |

---

## Purpose

This document defines how movable surveillance cameras should be understood within the trust architecture framework. Unlike static CCTV, movable cameras introduce **intentional observation** — they can patrol autonomously, respond to trust-state changes, and be controlled by operators whose intent becomes part of the surveillance signal.

The purpose is to ensure that movable surveillance remains:

- **Governed** — with clear authority boundaries for automated vs. manual control
- **Reviewable** — decisions to track, zoom, or redirect are attributed and reconstructable
- **Contextual** — camera behavior responds to operational state and trust conditions
- **Compatible** — with life-safety requirements and degraded operations

---

## Core Principle

> Camera movement carries operational meaning. Patrol behavior signals routine monitoring, while manual override signals heightened attention or investigation. The architecture must preserve this distinction and make it reviewable.

A camera that moves automatically is not the same as a camera that moves by command. Both must be visible, attributable, and governed differently.

---

## Why This Topic Matters

### Trust-State Implications

Camera behavior should reflect the facility's current trust state:

| Trust State | Camera Behavior |
|---|---|
| Established trust | Automated patrol only, no intervention |
| Conditional trust | Increased patrol frequency, logged deviations |
| Narrowed trust | Operator may engage manual control with justification |
| Degraded trust | Manual control prioritized, automated patrol suspended |
| Suspended trust | Limited observation, high-review requirement |
| Recovery-pending | Focused verification of zone transitions |

The camera system itself becomes a **trust-state indicator** — its mode reveals something about the facility's confidence level.

### Movement Meaning

Patrol patterns themselves carry meaning:

- A camera moving along a predictable route signals **normalcy**
- A camera pausing unexpectedly signals **uncertainty**
- A camera being manually redirected signals **investigation**
- A camera following an actor signals **elevated scrutiny**

These signals must be interpretable by operators and auditors alike.

### Privilege and Control

Taking manual control of a camera is a **privileged action**. It requires:

- Role-based authorization
- Attribution (who took control, when, why)
- Time limits or auto-return conditions
- Review after the fact

An operator watching a feed is different from an operator commanding camera movement. The latter changes the facility's state and must be treated accordingly.

---

## Main Model or Structure

### Three Operational Modes

The movable camera system operates in three distinct modes:

#### 1. Patrol Mode (Automated)

The camera moves along predefined rails in predictable patterns that simulate human patrolling behavior.

**Characteristics:**

- Predefined waypoints and routes
- Regular speed and timing
- No target-following
- Low privilege requirement (system autonomous)
- Logged as routine operation

**Purpose:** Signal continuous coverage, deter unauthorized activity, maintain baseline awareness.

#### 2. Manual Override Mode (Operator-Controlled)

A watcher operator takes direct control of the camera via interface commands.

**Characteristics:**

- Requires privileged access authorization
- Operator selects pan, tilt, zoom independently
- Session is time-limited or requires periodic renewal
- Full attribution: who, when, duration, zone
- Logged as exceptional activity

**Purpose:** Targeted observation, incident verification, elevated scrutiny.

#### 3. Gaze-to-Motion Mode (Intent-Driven)

Operator directs attention via interface focus/zoom, and the camera responds by moving toward that focus.

**Mechanism:**

- Operator zooms or centers frame on specific area
- Camera interprets this as directional intent
- Rail system physically repositions camera toward indicated zone
- Maintains continuous feedback loop between operator focus and camera position

**Characteristics:**

- Bridges patrol and manual control
- Lower friction than full manual override
- Still requires attribution and review
- Creates tighter coupling between operator intent and physical system

**Purpose:** Naturalistic control interface while preserving governance boundaries.

### Mode Transitions

Transitions between modes must be explicit and recorded:

- **Patrol Mode → Manual Override:** requires privilege escalation + reason
- **Patrol Mode → Gaze-to-Motion:** requires authenticated operator + session start
- **Manual Override → Patrol Mode:** automatic timeout or manual release
- **Gaze-to-Motion → Manual Override:** same authority level, continuous session

Each transition is a **governance event** requiring reconstruction capability.

---

## Contextual Interpretation

### Integration with Trust-State Model

The surveillance system must respond to trust-state changes:

- **Normal conditions:** Patrol mode dominant, minimal manual intervention
- **Heightened awareness:** Increased patrol density, ready manual override capacity
- **Incident response:** Manual override prioritized, gaze-to-motion for tracking
- **Recovery phase:** Return to patrol mode with verification logging

The camera system should not remain in patrol mode during degraded trust without explicit authorization.

### Integration with Zone Model

Zones affect camera authority:

| Zone Sensitivity | Camera Policy |
|---|---|
| Low sensitivity | Patrol-only, no manual override |
| Medium sensitivity | Patrol + authorized manual override |
| High sensitivity | Manual override default, patrol secondary |
| Restricted | No automated patrol, operator-controlled only |

Movement between zones triggers different camera behaviors. A camera crossing from low to high sensitivity zone may require additional authentication or logging.

### Integration with Privileged-Access Model

Manual camera control is a privileged action with the following characteristics:

- **Separation from ordinary access:** Having zone entry rights ≠ having camera control rights
- **Stronger attribution:** Identity + role + timestamp + justification
- **Review requirement:** All manual sessions subject to audit
- **Time boundaries:** Automatic expiration unless renewed

The system must enforce that privileged control cannot persist indefinitely without governance confirmation.

### Integration with Operational State

Different facility states enable different camera capabilities:

| Operational State | Camera Capability |
|---|---|
| Normal | Full capability (all modes available) |
| Heightened | Manual override prioritized, patrol continues |
| Incident | Manual control active, patrol suspended if conflicting |
| Partial failure | Degraded patrol, manual fallback if possible |
| Communication loss | Local patrol only, no remote override |

During degraded operations, the architecture narrows what can be trusted. Remote camera control may become unreliable; local patrol may continue as compensating control.

---

## Relationship to Other Parts of the Concept

This document connects to:

### Surveillance Model

Foundation for all observation logic. Defines how surveillance supports interpretation rather than just recording.

### Trust-State Model

Determines when manual intervention is warranted vs. when patrol suffices.

### Zone Model

Defines which areas cameras may observe and what permissions are required for each zone.

### Privileged-Access Model

Defines authority requirements for manual override and gaze-to-motion control.

### Governance Model

Determines who may authorize camera control, review sessions, and define patrol patterns.

### Audit-and-Review Model

All camera mode transitions and manual sessions must be reconstructable with context.

### Degraded-Operations Model

Defines fallback behavior when rail system fails or communication degrades.

### Alarm-and-Signaling Model

Operators must see clear signals indicating camera mode (patrol/manual/tracking).

---

## What This Model Rejects

This model explicitly rejects the following assumptions:

| Rejected Assumption | Alternative Principle |
|---|---|
| All surveillance is equal | Patrol surveillance ≠ investigative surveillance |
| Operator control is always permissible | Manual override requires privilege and attribution |
| Camera movement is purely technical | Movement carries governance meaning |
| Automated = safer than manual | Automation reduces human involvement but does not eliminate accountability |
| Surveillance can be invisible to operators | Operators must see camera mode and control state |
| Tracking is inherently suspicious | Tracking under governance is legitimate scrutiny |
| Technology replaces policy | Rails and cameras do not absolve governance responsibility |

---

## Design Implications

### 1. Interface Visibility

Operators must see at all times:

- Current camera mode (patrol / manual / gaze-to-motion)
- Who last controlled the camera (if not in patrol mode)
- Duration of current session
- Zone being observed

### 2. Attribution Logging

Every camera action generates log entries including:

- Mode transitions
- Manual control start/stop
- Gaze-to-motion activations
- Zoom/pan/tilt commands
- Justification codes for manual override

Logs must support reconstruction of:

- What happened
- When it happened
- Who authorized it
- Why it was done

### 3. Timeout and Auto-Recovery

Manual sessions must have boundaries:

- Maximum duration without renewal (e.g., 15 minutes)
- Automatic return to patrol mode on timeout
- Notification on mode change to relevant observers
- Review flag on extended sessions

### 4. Fail-Safe Behavior

On rail system failure:

- Camera parks in neutral position (does not block egress)
- Signals degrade to fault status
- Operators notified of unavailability
- Compensating surveillance activated if available

### 5. Life-Safety Compatibility

Camera positioning must never:

- Block evacuation routes
- Obscure emergency signage
- Create confusion during fire alarms
- Prevent responder access

Rail routes must respect compartmentation boundaries per passive fire resilience requirements.

---

## Summary

Movable camera systems are not merely technical upgrades to surveillance. They introduce **intentional observation** into the facility's trust architecture — the ability to move attention, shift focus, and direct scrutiny in response to operational needs.

The key distinctions are:

- **What:** Patrol vs. manual vs. gaze-to-motion
- **Why:** Routine monitoring vs. investigation vs. targeted observation
- **Who:** System autonomy vs. privileged operator vs. authenticated controller
- **How long:** Continuous vs. time-bound vs. auto-expiring
- **Review:** Routine logs vs. enhanced attribution vs. post-session analysis

Without explicit governance, these capabilities become risks — unattributed tracking, indefinite surveillance, and blurred accountability. With proper architecture, they become **meaningful tools for contextual security** that support interpretation without eroding trust.

This model ensures that camera movement remains a governed, reviewable, and interpretable element of the wider trust architecture.
