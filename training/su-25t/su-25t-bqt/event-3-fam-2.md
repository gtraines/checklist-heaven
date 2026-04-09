# Event 3 — Familiarization Flight 2 (Fam-2)

> **Course:** Su-25T Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Departure & Setup](#part-1--departure--setup)
5. [Part 2 — Stall Series](#part-2--stall-series)
6. [Part 3 — Spin Awareness & Recovery](#part-3--spin-awareness--recovery)
7. [Part 4 — Advanced Trim Technique](#part-4--advanced-trim-technique)
8. [Part 5 — ACS Modes Familiarization](#part-5--acs-modes-familiarization)
9. [Part 6 — Return & Landing](#part-6--return--landing)
10. [Completion Standards](#completion-standards)
11. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Identify and correctly recover from an approach-to-stall condition (wings-level and turning)
- [ ] State the conditions that lead to a flat spin and demonstrate spin avoidance technique
- [ ] Demonstrate proper trim management across a full speed range (300–600 km/h)
- [ ] Engage and disengage each ACS mode and describe its effect on aircraft control
- [ ] Execute a second full-stop landing with improved precision over Event 2

---

## Ground Brief

### Mission Profile
This is a high-altitude airwork mission. The student will perform stalls, practice trim technique, and explore ACS modes before returning for landing.

**Minimum safe altitude for all stall and spin recovery work: 3,000 m AGL.**

### Stall Characteristics Review

The Su-25T provides clear pre-stall cues:

| Phase | Indication | Action |
|---|---|---|
| Approach to stall | Airframe buffet begins | Relax back pressure, add power |
| Stall break | Nose drops sharply | Standard recovery |
| Post-stall / departure | Yaw combined with high AoA | Rudder neutral, full power, recover |

> **Flat Spin Warning:** If the aircraft enters a high-AoA state **combined with yaw** (usually from uncoordinated rudder during a slow-speed turn), it can enter a flat spin. Recovery below 2,000 m AGL is often impossible. The DCS model simulates this accurately.

---

## Pre-Mission Setup

- [ ] Same airfield as Event 2 (Caucasus — Kobuleti or Batumi recommended)
- [ ] **Fuel:** 70% (to simulate slightly heavier handling than Event 2)
- [ ] **Stores:** Clean
- [ ] Weather: Day VMC, calm winds
- [ ] Set a rescue waypoint at high altitude (5,000–6,000 m) in the mission editor or use built-in waypoints

---

## Part 1 — Departure & Setup

- [ ] Complete cold start per Event 2 procedures (reference: [Su-25T Checklist](../../checklists/aircraft/su-25t.md))
- [ ] Taxi and take off per Event 2 standard (rotation at ~215 km/h for slightly heavier fuel)
- [ ] Climb to **6,000 m MSL** — this provides adequate recovery altitude for all stall work
- [ ] Establish **cruise at 500 km/h** — trim for hands-off straight and level
- [ ] Confirm: no stick pressure required, ball centered, altitude steady

---

## Part 2 — Stall Series

Perform all stalls at **≥ 4,000 m AGL** to ensure recovery altitude.

### Exercise A: Wings-Level Power-Off Stall

1. - [ ] Reduce throttle to **idle** (`Z` axis or `PgDn` to min)
2. - [ ] Maintain wings level with aileron — use rudder to stay coordinated
3. - [ ] Apply back pressure to maintain altitude as speed bleeds off
4. - [ ] **At buffet onset** (airframe shudder, typically 200–220 km/h): note the indication
5. - [ ] Allow stall to break naturally — nose drops
6. - [ ] **Recovery:** Release back pressure → add full power → establish climb attitude
7. - [ ] Do **not** use aggressive aileron during recovery — roll only after nose is below horizon

**Standard:** Recover to level flight within 500 m altitude loss.

### Exercise B: Turning Stall (30° Bank)
1. - [ ] Establish a 30° banked turn, reduce power to idle
2. - [ ] Maintain altitude with back pressure — feel the increasing stick force
3. - [ ] At buffet onset, note that buffet arrives sooner than in wings-level (load factor effect)
4. - [ ] Recovery: **wings level first**, then release back pressure, add power
5. - [ ] Do **not** attempt recovery while still in bank — wing rock risk

**Standard:** Recover wings-level within 500 m altitude loss; no secondary stall.

### Exercise C: Approach-to-Stall Recognition (No Break)
1. - [ ] Configure aircraft as for landing: gear down, flaps landing, 260 km/h, idle power
2. - [ ] Add back pressure — induce buffet without allowing stall break
3. - [ ] **At first buffet:** full power, nose to 5° pitch, gear up, flaps up on schedule
4. - [ ] This is the **go-around drill** — practice this until the response is automatic

**Instructor Note:** The most common student failure in this exercise is hesitating to add power at the buffet. The buffet **is the warning** — act on it immediately.

---

## Part 3 — Spin Awareness & Recovery

### Spin Entry Conditions (Awareness Only)

The Su-25T will enter a flat spin if:
- AoA exceeds ~20 units (past buffet, approaching full stall), AND
- Significant yaw is introduced (from uncoordinated rudder or asymmetric thrust)

**Recovery — if spin develops:**
1. - [ ] **Throttle — IDLE** (both engines)
2. - [ ] **Rudder — NEUTRAL** (center rudder)
3. - [ ] **Stick — NEUTRAL** (release all inputs)
4. - [ ] Allow rotation to slow — aircraft will recover if sufficient altitude exists
5. - [ ] If below **2,000 m AGL with no recovery in progress** — **EJECT** (`RShift + E`)

> **Instructor Note:** In DCS, demonstrate a spin entry at 8,000 m MSL so the student can observe the motion and attempted recovery. Do not attempt to induce spins below 5,000 m AGL.

### Spin Avoidance Technique (Practice)
- [ ] Slow the aircraft to 250 km/h, enter a 30° bank turn
- [ ] Deliberately use **opposite rudder** to induce skid — feel the yaw
- [ ] **Before** stall: release rudder, center ball, recover
- [ ] Lesson: The Su-25T will depart from controlled flight quickly if yaw is combined with low speed. Keep the ball centered at all times near the stall.

---

## Part 4 — Advanced Trim Technique

The purpose of this exercise is to make trim management instinctive.

### Exercise: Speed Range Trim Sweep

Start at cruise altitude, 500 km/h, trimmed for level flight (hands-off).

| Step | Action | Expected Trim Change |
|---|---|---|
| 1 | Accelerate to 650 km/h (partial power) | Nose-heavy → trim forward (nose down) |
| 2 | Return to 500 km/h | Return trim to neutral |
| 3 | Slow to 350 km/h (reduce power) | Nose-light → trim back (nose up) |
| 4 | Slow to 250 km/h (approach config, gear/flaps) | Significant nose-up trim required |
| 5 | Return to 500 km/h cruise | Reset trim — full sweep |

> **Trim Keys:** Pitch trim up `]` / down `[`

**Standard:** At each stabilized speed, student can release stick and maintain altitude ± 100 m without control input.

**Instructor Note:** Students who have not internalized trim management will struggle on every subsequent event. If this exercise is not passed cleanly, repeat it before proceeding.

---

## Part 5 — ACS Modes Familiarization

Conduct at 3,000 m MSL, clear area, cruise speed.

### Mode 1: Emergency Level (`LAlt + 3`)
- [ ] Roll to 60° bank, release controls
- [ ] Press `LAlt + 3` — aircraft will return to wings-level
- [ ] **This is your emergency recovery command** — practice until it is reflex

### Mode 2: Route Following
- [ ] Ensure waypoints are programmed (use mission editor or built-in route)
- [ ] Engage Route mode via NAV panel
- [ ] Observe aircraft tracking toward waypoint
- [ ] Override: any stick input disengages autopilot in most modes

### Mode 3: Coupled Landing (Academic Demo)
- [ ] Requires ILS/PRMG approach — set up on a compatible airfield
- [ ] Engage Landing ACS mode
- [ ] Observe glidepath coupling — system flies the approach
- [ ] Student must be able to disconnect and fly manually: disengage mode, take controls

**Instructor Note:** Do not allow students to rely on ACS for landing. It is a backup system. All landings in this course are flown manually.

---

## Part 6 — Return & Landing

- [ ] Descend to pattern altitude, establish 400 km/h on downwind
- [ ] Configure: gear down, flaps landing, trimmed for 260 km/h approach
- [ ] Fly a stabilized final — no speed below 250 km/h
- [ ] Touchdown at ~240 km/h, deploy drag chute immediately (`P`)
- [ ] Progressive braking after < 200 km/h

### Improvement Goals from Event 2
Focus on these two improvements over the Event 2 landing:

| Item | Event 2 Minimum | Event 3 Goal |
|---|---|---|
| Final approach stability | Stabilized by 300 m | Stabilized by 500 m |
| Touchdown speed deviation | ± 25 km/h | ± 15 km/h |

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Wings-level stall | Recovery within 500 m altitude loss; no secondary stall |
| Turning stall | Wings level before recovery; no secondary stall |
| Approach-to-stall (go-around drill) | Power added at first buffet; no stall break |
| Trim sweep | Hands-off flight ± 100 m at each test speed |
| ACS Emergency Level | Correctly activates `LAlt + 3` on first attempt |
| Landing | Stabilized ≥ 500 m on final; touchdown 230–260 km/h |

---

## Common Errors

| Error | Correction |
|---|---|
| Hesitating at stall buffet | The buffet **is** the warning — act immediately |
| Attempting recovery in banked turn | Level wings first, then recover nose |
| Using opposite aileron at the stall break | Stick neutral; use rudder only to stop rotation |
| Uncoordinated rudder near the stall | Keep the ball centered at all times — spin risk |
| Not trimming during speed changes | After every significant throttle change, re-trim |

---

[← Event 2: Fam-1](event-2-fam-1.md) | [→ Event 4: Traffic Pattern](event-4-traffic-pattern.md)

---

*Based on Eagle Dynamics DCS World documentation. For simulation use only.*
