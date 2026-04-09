# Event 5 — Emergency Procedures

> **Course:** A-10A Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [EP 1 — Single Engine Failure In Flight](#ep-1--single-engine-failure-in-flight)
5. [EP 2 — Engine Failure on Takeoff](#ep-2--engine-failure-on-takeoff)
6. [EP 3 — Hydraulic System Failure](#ep-3--hydraulic-system-failure)
7. [EP 4 — Engine Fire](#ep-4--engine-fire)
8. [EP 5 — Ejection Criteria Review](#ep-5--ejection-criteria-review)
9. [Event Profile](#event-profile)
10. [Completion Standards](#completion-standards)
11. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Identify a simulated single-engine failure and execute the correct immediate action items
- [ ] Perform a single-engine approach and landing
- [ ] Describe hydraulic failure indications and demonstrate degraded-control flight
- [ ] State the engine fire immediate action items in correct sequence from memory
- [ ] State the ACES II ejection decision criteria and minimum altitude thresholds

---

## Ground Brief

### About This Event
Emergency procedures in DCS are simulated by the instructor or the student "failing" systems via keyboard and mission editor. Some emergencies are fully modeled (engine shutdown, hydraulic degradation); others (fire) are partially modeled.

**All EPs in this event use simulated failures only — the student will not cause real aircraft damage as part of this curriculum.** The student practices identifying the emergency and executing the response. The instructor "calls" the emergency or sets up a pre-planned failure in the mission editor.

### A-10A Emergency Philosophy
The A-10A was specifically engineered to bring the pilot home from situations that would be fatal in any other aircraft:
- **Single-engine flight** is a routine recovery scenario, not a catastrophic emergency
- **Manual reversion** is a controlled landing capability, not a last resort
- **Ejection** is the last resort — the ACES II is zero-zero capable, but it is irreversible

**The correct response to any emergency is:** Fly the aircraft → Identify the problem → Execute the procedure → Land when practical.

### "Dead Foot, Dead Engine"

| Aircraft yaws toward... | The failed engine is... | Apply rudder to... |
|---|---|---|
| Left | Left engine | Right (push right rudder) |
| Right | Right engine | Left (push left rudder) |

*The foot that is relaxed (requires no pressure) is on the dead engine side.*

---

## Pre-Mission Setup

- [ ] Load DCS World; A-10A; day VMC; adequate fuel (75% internal)
- [ ] Student performs startup and taxi from memory
- [ ] Depart and climb to **10,000 ft MSL** for all EP airwork
- [ ] Instructor brief: "I will call emergency types. You will execute the correct response."

---

## EP 1 — Single Engine Failure In Flight

### Setup
- [ ] Cruise altitude: 10,000 ft MSL, 250 KIAS, clean configuration
- [ ] Instructor (or student self-): **shut down one engine** (`RAlt + End` for left; `RCtrl + End` for right)

### Immediate Action Response

The student executes from memory:

1. **Identify** — note yaw direction; "right engine yaw — right engine failure"
2. **Throttle (failed)** — IDLE (verify it's the correct engine before shutting down)
3. **Rudder** — apply to maintain wings-level, ball centered
4. **Confirm** — RPM and EGT on affected side dropping; good engine remains normal
5. **Throttle (failed)** — OFF (`RAlt + End` or `RCtrl + End`)
6. **Trim** — rudder trim into the good engine side to relieve pedal pressure
7. **Configure** — maintain level flight or gentle descent; no aggressive maneuvering
8. **Declare** — (simulated) "Mayday, Mayday, single engine"
9. **Plan** — identify nearest airfield; set up for a single-engine approach

> **Warning:** In DCS FC3, if you shut down the wrong engine, you can restart it. But build the discipline: verify before shutting down. In the real aircraft, shutting down the wrong engine is a potentially fatal error.

### Single-Engine Performance

| Condition | Approximate Value |
|---|---|
| Max continuous thrust (one engine) | ~9,065 lbf |
| Single-engine climb (light weight) | ~500–1,500 ft/min |
| Single-engine climb (heavy) | May be negative above 15,000 ft |
| Minimum control speed (Vmca) | ~120 KIAS |
| Single-engine approach speed | Normal approach speed + 10 KIAS |

- **Do NOT slow below 130 KIAS** on a single-engine approach — go-around may be impossible
- Add 10 KIAS to all approach speeds (+10 to the green donut target)

### Single-Engine Approach & Landing

1. Fly a wide, long final — minimize maneuvering on one engine
2. Gear down early; flaps DN as normal
3. Final approach speed: **normal + 10 KIAS** (~145 KIAS vs. normal 135)
4. **Commit** to the approach — single-engine go-around is high-risk and may not succeed
5. Land normally; rollout with speed brakes and progressive braking

### Single-Engine Engine Restart (Air Restart)
If the failure was not a fire or confirmed mechanical failure, an air restart may be attempted:
1. Throttle to IDLE
2. Engine start key (`RAlt + Home` / `RCtrl + Home`) — depends on windmilling RPM
3. **Best success:** above 200 KIAS; altitude above 5,000 ft AGL
4. If no restart within 30 sec, secure the engine and continue single-engine

---

## EP 2 — Engine Failure on Takeoff

> **Note:** This is a briefed scenario; the instructor does not actually fail the engine during a real takeoff roll. The student "flies" the scenario from memory in a verbalized walk-through, then flies a simulated version from 200 ft AGL (engine failed just after liftoff).

### Scenario A: Engine Failure on the Roll (Below Vr)

**Briefed response (verbalized):**
1. **Throttles** — IDLE (both)
2. **Wheel Brakes** — MAX (`W`)
3. **Speed Brakes** — OPEN (`LShift + B`)
4. **Jettison stores** — if runway remaining is insufficient (`LCtrl + W`)

**Key decision:** If below 100 KIAS, **abort**. Above 100 KIAS with more than half the runway — performance dictates; generally **continue** unless there is fire or flight control failure.

### Scenario B: Engine Failure After Liftoff (Above Vr)

This is simulated by the student climbing to 200 ft AGL and then the instructor calling "Engine failure right / left":

1. **Maintain directional control** — immediate rudder into good engine
2. **Climb** — if positive rate, continue climbing; gear up on positive rate
3. **Assess** — confirm engine failure; do not retard good engine
4. **Below 500 ft AGL:** do NOT attempt to turn back to the runway ("the impossible turn")
5. **Above 500 ft AGL, 150+ KIAS:** may attempt a downwind or crosswind return
6. **Single-engine climb-out** and return to landing

---

## EP 3 — Hydraulic System Failure

### Setup
- [ ] Cruise altitude: 8,000 ft MSL; instructor describes the failure verbally ("your left hydraulic system has failed")

### Dual Hydraulic System Review

| System | Failure Indication | Effect |
|---|---|---|
| **Single system failure** | HYD PRESS caution one side | Full control via remaining system; increased forces |
| **Dual system failure** | Both HYD PRESS cautions | Manual reversion — very heavy controls; aircraft remains flyable |

### Simulating Degraded Control Flight

In DCS FC3, hydraulic failure can be approximated by practicing large-input sluggishness. The student:
1. Reduces control sensitivity settings (if available) to simulate heavy controls
2. Practices flying with reduced stick deflection authority
3. Demonstrates a long, straight-in approach using gentle inputs only

### Manual Reversion Approach Profile

| Item | Value |
|---|---|
| Pattern type | Straight-in (no pattern turns) |
| Final approach distance | ≥ 5 nm for gentle alignment |
| Approach speed | Normal + 10 KIAS |
| Turn rate | ≤ 20° bank; avoid aggressive maneuvering |
| Emergency gear extend | `LShift + LCtrl + G` if normal extend fails |

### Emergency Gear Extension
If the gear does not extend normally:
1. **Normal Gear** — `G` (attempt twice)
2. **Emergency Gear** — `LShift + LCtrl + G`
3. Verify three green indicators
4. If still uncertain: assume gear is down; land on main gear; accept nosewheel collapse risk

---

## EP 4 — Engine Fire

### Setup
- [ ] Cruise altitude: 8,000 ft MSL
- [ ] Instructor calls: "You have an engine fire warning — right engine"

### Immediate Action Response

1. **Throttle (affected)** — IDLE
2. **Identify** — right engine (confirmed by fire warning; note yaw)
3. **Throttle (affected)** — OFF (`RCtrl + End`)
4. **Fire Handle** — PULL (if modeled — verify keybind in controls)
5. **Agent** — DISCHARGE (first shot; wait 30 sec)
6. **If fire persists** — DISCHARGE second shot
7. **Maintain control** — rudder trim; configure for single-engine flight
8. **Land ASAP** — do not delay; declare emergency; priority landing

> *⚠ Realism Divergence: The real A-10A has a two-shot Halon fire suppression system per engine with dedicated fire handles in the cockpit. DCS FC3 provides a simplified fire warning but may not fully model the two-shot suppression system. Verify fire-related keybinds before flying this event.*

### Post-Fire Landing Considerations
- Assume the engine will not be restarted after a fire
- Land with single-engine configuration
- If structural damage is suspected (fire burned through), fly conservatively — avoid turbulence and high G

---

## EP 5 — Ejection Criteria Review

> **This is academic — do NOT practice ejections in training aircraft.** The ACES II seat ejection is simulated as a last resort in DCS.

### ACES II Seat Characteristics

| Parameter | Value |
|---|---|
| Seat Type | Advanced Concept Ejection Seat II (ACES II) |
| Capability | Zero-zero (0 altitude / 0 airspeed) |
| Mode 1 | 0–250 KEAS — drogue then main parachute |
| Mode 2 | 250–600 KEAS — delayed opening; windblast protection |
| Initiators | Dual face-curtain or handle; automatic mode selection |
| DCS Ejection | `LCtrl + E` × 3 |

### Decision Criteria

| Condition | Decision |
|---|---|
| Aircraft controllable; airfield reachable | Fly it home |
| Aircraft uncontrollable; above 2,000 ft AGL | Eject |
| Aircraft uncontrollable; below 2,000 ft AGL | **Eject immediately** (no delay) |
| Fire that cannot be extinguished; above 2,000 ft | Eject |
| Structural failure; aircraft departure from controlled flight | Eject |
| Both engines failed; no restart; no suitable landing area | Eject when fuel state dictates (glide to altitude threshold) |

**The "2,000-foot rule":** Below 2,000 ft AGL with an uncontrollable aircraft, the decision is already made. Every second of delay is altitude you cannot recover.

### Student Knowledge Check (Verbalized)
Before completing this event, the instructor asks:
- "You are at 1,500 ft AGL. The aircraft has departed controlled flight in a spin. What do you do?" *(Answer: Eject immediately — below 2,000 ft floor; no time for recovery attempt)*
- "You are at 8,000 ft AGL. You have a right engine fire that is not going out. The left engine is good. What do you do?" *(Answer: Secure right engine; fly single-engine; assess; if fire continues and structural integrity is at risk, eject well above 2,000 ft)*

---

## Event Profile

| Exercise | Method | Standard |
|---|---|---|
| EP 1a: Engine ID & secure | Instructor calls failure; student responds | Correct engine identified; correct immediate actions |
| EP 1b: Single-engine approach | Fly actual single-engine approach in DCS | Stable approach; appropriate speed; full stop |
| EP 2a: Takeoff RTO (verbalized) | Walk-through scenario | Correct response stated in order |
| EP 2b: Engine failure after liftoff | Simulated from 200 ft AGL | Control maintained; no "impossible turn" |
| EP 3: Hydraulic (verbalized) | Walk-through scenario | Correct degraded-control approach profile described |
| EP 4: Engine fire (verbalized) | Walk-through scenario | Correct immediate actions in order |
| EP 5: Ejection criteria | Knowledge check | All criteria correctly stated |

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Engine identification | Correct engine identified in < 5 sec (verbal/stick response) |
| Single-engine immediate actions | All steps in correct order without reference |
| Single-engine approach | Stable; ≥ 130 KIAS on final; landed safely |
| Ejection decision criteria | All four conditions correctly stated from memory |
| EP verbalized walk-throughs | All immediate actions stated in correct sequence |

---

## Common Errors

| Error | Correction |
|---|---|
| Shutting down the wrong engine | "Dead foot, dead engine" — verify yaw direction before action |
| Pulling throttle on good engine | Always IDLE first; then identify; then OFF |
| Single-engine go-around attempt from short final | Brief clearly: commit to a single-engine approach; go-around is high-risk |
| Forgetting rudder trim after engine shutdown | Rudder trim is not automatic; the foot gets tired; trim it |
| Attempting "impossible turn" after engine failure at low altitude | Hard rule: below 500 ft AGL, land straight ahead or field ahead |
| Delaying ejection decision below 2,000 ft | The 2,000-ft rule is not a guideline — it is a floor |

---

[← Event 4: Traffic Pattern](event-4-traffic-pattern.md) | [→ Event 6: Check Ride](event-6-check-ride.md)

---

*Based on T.O. 1A-10A-1 and Eagle Dynamics DCS World documentation. For simulation use only.*
