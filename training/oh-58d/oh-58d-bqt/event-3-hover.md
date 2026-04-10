# Event 3 — Hover & Hover Taxi

> **Course:** OH-58D Kiowa Warrior Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Startup & Rotor Engagement](#part-1--startup--rotor-engagement)
5. [Part 2 — Stationary Hover](#part-2--stationary-hover)
6. [Part 3 — Power Check](#part-3--power-check)
7. [Part 4 — Pedal Turns](#part-4--pedal-turns)
8. [Part 5 — Hover Taxi](#part-5--hover-taxi)
9. [Part 6 — Hover Taxi — Sideward and Rearward](#part-6--hover-taxi--sideward-and-rearward)
10. [Part 7 — Shutdown](#part-7--shutdown)
11. [Completion Standards](#completion-standards)
12. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Maintain a stable stationary hover at 3–5 ft skid height for a minimum of 30 seconds with no more than 2 ft drift
- [ ] Identify and compensate for translating tendency (right cyclic) without prompting
- [ ] Perform a hover power check and state whether aircraft is operating within limits
- [ ] Execute pedal turns to cardinal headings within ±5° and ±2 ft altitude
- [ ] Hover taxi in a straight line at controlled speed (< 20 kts) and altitude (3–5 ft)
- [ ] Perform sideward hover taxi (left and right) and rearward hover taxi without exceeding 35 kts or drifting off intended track

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase 1 | Startup and rotor engagement (from cold-dark) |
| Phase 2 | Stationary hover — stabilize for 30+ seconds |
| Phase 3 | Power check — determine available power margin |
| Phase 4 | Pedal turns — 90°, 180°, 360° |
| Phase 5 | Forward hover taxi — straight line, S-turns |
| Phase 6 | Sideward and rearward hover taxi |
| Phase 7 | Shutdown |

### Key Numbers for This Event

| Item | Value |
|---|---|
| Target Hover Altitude | 3–5 ft skid height |
| Translating Tendency | Left drift — right cyclic required |
| ETL Airspeed | 16–24 KIAS |
| Max Hover Taxi Speed | 20 kts forward; 35 kts sideward/rearward |
| Power Check Torque | Note max available torque (not to exceed 100% continuous) |
| Nr (powered hover) | 98–100% |
| Torque Limit | 100% continuous; 110% for ≤ 10 sec |
| TOT Continuous | ≤ 737°C |

### Weather Requirements

| Requirement | Standard |
|---|---|
| Winds | < 15 kts (calm preferred; cross-check translating tendency against wind direction) |
| Visibility | ≥ 3 SM |
| Cloud ceiling | ≥ 1,500 ft AGL |

---

## Pre-Mission Setup

- [ ] Load DCS OH-58D; cold-and-dark spawn at a clear ramp or open taxiway area
- [ ] Use an area with a clear visual reference point for the stationary hover (taxiway centerline, parking spot marking, etc.)
- [ ] Weather: calm or light winds preferred for initial hover work
- [ ] HOTAS: confirm collective axis, cyclic, and anti-torque pedals functional

---

## Part 1 — Startup & Rotor Engagement

Follow the complete startup procedure from Event 2. This event begins with a full cold-dark startup — no shortcuts.

**Gate Check before lifting:**
- [ ] AHRS/GPS alignment complete
- [ ] Nr: 100%
- [ ] TOT: ≤ 737°C
- [ ] Torque: ground idle (< 15%)
- [ ] All cautions clear except expected items

---

## Part 2 — Stationary Hover

The stationary hover is the foundation of all helicopter airwork. Master this before proceeding. The OH-58D requires **continuous, active control input** to remain in a stable hover — it does not hover hands-off.

### Hover Technique

**Three simultaneous tasks:**
1. **Collective** — controls altitude; small adjustments maintain 3–5 ft
2. **Cyclic** — controls position (drift); tiny inputs prevent lateral/longitudinal movement
3. **Pedals** — controls heading; keep the nose pointed at the intended reference

**Pre-Hover Setup:**
- [ ] Select a visual reference at eye level (tree line, building corner, fence post) **directly ahead**
- [ ] Select a ground reference below (taxiway stripe, parking mark) to detect lateral/longitudinal drift
- [ ] Identify wind direction (check DCS weather or observe ground dust/smoke)

### Hover Pickup

| Step | Action | Cue |
|---|---|---|
| 1 | Pre-position **slight right cyclic** | Compensation for translating tendency |
| 2 | Slowly raise **collective** | Torque rises; aircraft lightens on skids |
| 3 | Apply **left pedal** as torque increases | Prevents right yaw |
| 4 | Aircraft reaches **light-on-skids** phase | Hold; assess drift direction |
| 5 | Continue collective — aircraft lifts to 3 ft | Do not rush through this phase |
| 6 | **Stabilize at 3 ft** | Reduce collective input rate; fine-tune |

### Stabilization Technique

Once airborne:
- Fix eyes on the **horizon reference** (not the ground — the ground will move and confuse spatial orientation)
- Use **peripheral vision** to detect ground drift
- Input corrections are **small** — think "ounces of pressure" not "degrees of movement"
- Corrections in one axis require corrections in others:
  - Raising collective (altitude) → adds torque → requires more left pedal
  - Forward cyclic (stop backward drift) → aircraft accelerates forward → add aft cyclic to stop

**The hover cross-check:**

```
Altitude (how high?) → Drift (moving where?) → Heading (nose pointed?) → Back to altitude
```

Cycle continuously. Each check should take < 1 second.

### Hover Standards for This Event

| Standard | Requirement |
|---|---|
| Altitude | ±2 ft from 3–5 ft target |
| Position (lateral) | ≤ 3 ft drift over any 30-second period |
| Position (longitudinal) | ≤ 3 ft drift over any 30-second period |
| Heading | ±5° of assigned heading |
| Duration | Minimum 30 seconds stable before proceeding |

---

## Part 3 — Power Check

The power check determines the aircraft's available power margin at the current density altitude. This is critical before any demanding hover maneuver (slope landing, pinnacle, max performance takeoff).

### Power Check Procedure

From a stable 3–5 ft hover:

| Step | Action | Record |
|---|---|---|
| 1 | Note current **torque** required to maintain hover | Example: 72% Q |
| 2 | Note **TOT** at this torque | Example: 680°C |
| 3 | Calculate **available margin**: 100% Q − current Q | Example: 100% − 72% = 28% margin |
| 4 | Calculate **TOT margin**: 737°C − current TOT | Example: 737° − 680° = 57°C margin |
| 5 | The **limiting margin** is whichever is smaller | Power or temperature limit |

### Interpreting the Power Check

| Available Margin | Interpretation |
|---|---|
| **> 25%** | Good margin; normal operations all phases |
| **15–25%** | Moderate; normal takeoffs/approaches; avoid confined areas requiring OGE hover |
| **10–15%** | Marginal; plan carefully; may not be able to hover OGE |
| **< 10%** | Critical — limit operations; no OGE-required maneuvers |

> *Power check results change with density altitude (temperature and pressure altitude). A hot day at a high-elevation airfield can dramatically reduce power margin compared to sea level on a standard day.*

---

## Part 4 — Pedal Turns

Pedal turns change heading while maintaining a stationary hover position. They test the student's ability to coordinate all three axes simultaneously while the visual references rotate.

### Pedal Turn Technique

| Step | Action |
|---|---|
| 1 | From stable hover, select a target heading (e.g., 90° turn to the right) |
| 2 | Apply **right pedal** to initiate right yaw |
| 3 | **Increase collective slightly** — turning adds rotor drag, requiring more power |
| 4 | Maintain cyclic position — the aircraft will try to drift as it turns |
| 5 | As approach 10° before the target heading, **reduce pedal** input to arrest the yaw |
| 6 | Stabilize on the new heading; adjust cyclic for any position drift |

### Pedal Turn Sequence (This Event)

1. 90° right turn
2. 180° right turn (to original heading + 180°)
3. 360° right turn (back to original heading)
4. 90° left turn
5. 360° left turn

### Pedal Turn Common Issues

| Problem | Cause | Fix |
|---|---|---|
| Overshooting the heading | Late pedal reduction | Reduce pedal input 10° early; anticipate |
| Altitude loss during turn | Not adding collective with yaw | Pre-load collective before starting turn |
| Drift away from point | Cyclic not compensating for turn | Continue active cyclic during turn; yaw doesn't fly itself |

---

## Part 5 — Hover Taxi

Hover taxi covers controlled movement of the aircraft at low speed and low altitude. The student must maintain a mental picture of the rotor disc clearance at all times.

### Forward Hover Taxi — Straight Line

| Step | Action |
|---|---|
| 1 | From stable hover, select a point 100–200 ft ahead on the taxiway |
| 2 | Apply **small forward cyclic** — aircraft begins to accelerate |
| 3 | Limit speed to **walking pace initially** (3–5 kts) |
| 4 | To maintain speed: hold cyclic slightly forward of neutral |
| 5 | To slow: **aft cyclic** to decelerate |
| 6 | As aircraft slows and stops, reduce aft cyclic to neutral; stabilize hover |
| 7 | Repeat at **10–15 kts** once comfortable at 3–5 kts |

**Speed Reference:** Use groundspeed from GPS/nav display or simply visual reference. At 3 kts you're walking pace; at 10 kts you're jogging. At 20 kts the visual blur of passing objects is obvious.

### Forward Hover Taxi — S-Turns

S-turns develop cyclic coordination and the ability to track a curved path at low altitude.

| Step | Action |
|---|---|
| 1 | Hover taxi forward at ~5–10 kts on the taxiway |
| 2 | Apply slight **right cyclic** to initiate a curving track to the right |
| 3 | After 30–45 ft of lateral displacement, reverse to **left cyclic** |
| 4 | Continue alternating — create sinusoidal track along taxiway centerline |
| 5 | Maintain constant altitude and airspeed throughout |

---

## Part 6 — Hover Taxi — Sideward and Rearward

### Sideward Hover Taxi

Sideward flight is used for positioning in tight areas where forward hover taxi is impractical.

| Step | Action | Monitor |
|---|---|---|
| 1 | From stationary hover, select a reference point to the side | — |
| 2 | Apply **lateral cyclic** in the direction of travel | Aircraft begins sliding sideways |
| 3 | Limit speed — **< 35 kts** (structural limit; 10–15 kts for precision) | Groundspeed |
| 4 | Maintain heading with pedals — the nose stays forward | Pedal inputs |
| 5 | To stop: **opposite lateral cyclic** | Arrest the slide |
| 6 | Stabilize | — |

**Left sideward** and **right sideward** both required in this event.

### Rearward Hover Taxi

Rearward taxi is used for backing into a parking spot or repositioning tail-first. Visual references are challenging since the direction of travel is behind the aircraft.

| Step | Action | Monitor |
|---|---|---|
| 1 | Turn head to look behind the aircraft before beginning | Confirm area is clear |
| 2 | Apply **aft cyclic** — aircraft begins rearward movement | Speed |
| 3 | Limit speed — **< 10 kts** (cautious; no rear visibility) | Groundspeed |
| 4 | Maintain heading with pedals | — |
| 5 | To stop: **forward cyclic** | — |

> *⚠ Rearward and sideward hover taxi must never be rushed. These are the most common maneuvers leading to tail rotor strike incidents in real operations. Continuously scan for obstacles in the direction of travel.*

---

## Part 7 — Shutdown

Follow the complete shutdown procedure from Event 2:
1. Throttle → IDLE
2. 2-minute engine cooldown
3. Avionics OFF (MFD, AHRS/GPS, Radios)
4. Throttle → OFF
5. Monitor spool-down (N1, TOT)
6. Generator → OFF → Inverter → OFF → Fuel Boost → OFF → Battery → OFF
7. Rotor brake below 40% Nr

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Startup | Completed per checklist; TOT < 843°C |
| Stationary hover — altitude | ±2 ft from 3–5 ft target for 30 sec |
| Stationary hover — position | ≤ 3 ft drift lateral/longitudinal over 30 sec |
| Translating tendency | Student compensates with right cyclic without prompting |
| Power check | Performed; torque and TOT margins correctly stated |
| Pedal turns — heading | ±5° of target; no overrotation |
| Pedal turns — altitude | ±2 ft throughout turn |
| Forward hover taxi | Speed < 20 kts; altitude 3–5 ft; smooth stop |
| Sideward hover taxi | Speed < 20 kts; no drift from intended track |
| Rearward hover taxi | Area checked before initiating; speed < 10 kts |

---

## Common Errors

| Error | Correction |
|---|---|
| **Chasing the aircraft with large inputs** | "Think small. The Kiowa responds to tiny inputs. Big corrections create oscillations. Ounces of pressure." |
| **Not pre-positioning right cyclic before lifting** | "Pre-position right before you pull. If you lift with the cyclic centered, you drift left immediately." |
| **Looking at the ground instead of the horizon** | "Eyes on the horizon. Use the ground in your peripheral to catch drift. Staring at the ground destroys your attitude reference." |
| **Not adding collective during pedal turns** | "Turning bleeds rotor efficiency. Add a touch of collective before every pedal turn or you'll sink." |
| **Over-controlling airspeed in hover taxi** | "Hover taxi is not a race. Walking pace until you can hold altitude and track simultaneously. Then add speed." |
| **Skipping area check before rearward taxi** | "You cannot see behind you. Look before you go. One tail rotor strike is the end of the flight." |
| **Forgetting to compensate heading during sideward taxi** | "The nose will drift as you move sideways. Active pedal to hold heading." |

---

[→ Proceed to Event 4: Familiarization Flight](event-4-fam-flight.md)

---

*Based on TM 1-1520-248-10, TC 3-04.4, and Eagle Dynamics / Polychop Simulations DCS OH-58D documentation. For simulation use only.*
