# Event 3 — Hover & Takeoff

> **Course:** Mi-24P Hind Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [In-Sim Procedures](#in-sim-procedures)
4. [Completion Standards](#completion-standards)
5. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Perform a hover power check and correctly interpret the result
- [ ] Establish and maintain a 3–5 m stationary hover for 30 seconds within tolerances
- [ ] Execute pedal turns in hover to target headings
- [ ] Conduct hover taxi at a safe pace with controlled altitude and heading
- [ ] Perform a running takeoff — the Mi-24P standard takeoff
- [ ] Perform a hover takeoff when directed (awareness of power requirements)
- [ ] Climb to altitude using the appropriate speed profile

---

## Ground Brief

### The Mi-24P Is Not a Hover Platform

This cannot be overstated. The Mi-24P weighs 10,000–11,500 kg. At those weights, the engine power required to hover out of ground effect (OGE) is close to — or exceeds — the engines' continuous limits. In real operations, Soviet doctrine emphasized:

- **Running takeoff and running landing** as the standard technique
- **Minimize hover time** — use it only for specific tactical requirements
- **OGE hover** should be attempted only after confirming hover power is available

In DCS, at training weight (~10,000 kg) with both engines healthy, OGE hover is possible but demanding. Be ready for high torque values (75–85%).

### Power Check — The Go/No-Go Decision

Before committing to any hover operation (especially a hover takeoff or hover landing), the pilot must perform a **hover power check**:

| Step | Action |
|---|---|
| 1 | Lift to 3–5 m wheel height |
| 2 | Stabilize in a hover — note torque |
| 3 | **If torque ≤ 80%** → Hover operations feasible |
| 4 | **If torque 80–85%** → Hover operations possible but marginal; use caution |
| 5 | **If torque > 85%** → OGE hover power not available; **running takeoff and landing required** |

### Running Takeoff vs. Hover Takeoff

| Technique | When Used | Power Required | Preferred? |
|---|---|---|---|
| **Running takeoff** | Standard; always when runway available | Less (wing lift assists) | **Yes — always preferred** |
| **Hover takeoff** | Confined areas; no runway; specific tactical requirement | More (pure rotor lift) | No — use only when needed |

The running takeoff is safer, more fuel-efficient, and more comfortable for the aircraft. It is the **default** Mi-24P departure technique.

### Transition Through ETL

During the running takeoff and takeoff run acceleration, the aircraft passes through Effective Translational Lift at approximately **50 km/h**. During this transition:
- Rotor efficiency increases noticeably
- Aircraft wants to pitch up and climb
- Power demand reduces
- Small forward cyclic may be needed to prevent nose-high attitude

---

## In-Sim Procedures

### Exercise 1 — Stationary Hover

Start from the parking spot (from Event 2 startup is assumed complete, Nr = 95%, pre-takeoff check done).

| Step | Action | Notes |
|---|---|---|
| 1 | **Collective** — smooth, gradual increase | Expect light on wheels at 65–70% torque |
| 2 | At **3–5 m** wheel height — **stop collective** | Stabilize altitude |
| 3 | Torque check — note value | This is the hover power check |
| 4 | **Cyclic** — small corrections to hold position | Anticipate — do not chase |
| 5 | **Pedals** — maintain heading | Right tail rotor = left pedal is anti-torque |
| 6 | Hold hover for **30 seconds** | Altitude ±1 m, drift ±3 m |

**Expected hover torque:** 70–80% at training weight in mild conditions.

**Tips:**
- Think of the cyclic as pointing the nose of the rotor disc, not flying the nose of the aircraft.
- Small inputs. The Mi-24P is heavy and has significant inertia — it responds slowly to small inputs and aggressively to large ones.
- The aircraft will drift slightly into wind. Anticipate and correct early.

### Exercise 2 — Pedal Turns in Hover

From the stationary hover:

| Step | Action | Standard |
|---|---|---|
| 1 | Select a target heading 90° right of current | e.g., if heading 360°, target 090° |
| 2 | Apply **right pedal** — nose moves right | Gentle, smooth pressure |
| 3 | As approaching target heading — reduce pedal to stop the turn | Anticipate by ~10° |
| 4 | Hold new heading in hover | ±5° tolerance |
| 5 | Repeat for 90° left turn | Left pedal |
| 6 | Return to original heading | |

### Exercise 3 — Hover Taxi

Hover taxi from parking to the runway holding point (or from point A to point B as briefed).

| Step | Action | Notes |
|---|---|---|
| 1 | From hover — apply slight forward cyclic | Gentle application |
| 2 | Target taxi speed: **5–10 km/h** | Walking pace |
| 3 | Maintain **3–5 m** altitude | No altitude changes during taxi |
| 4 | Maintain heading with pedals | Crosswind correction as needed |
| 5 | Stop at designated point | Rearward cyclic to arrest forward motion |
| 6 | Return to stationary hover | Re-stabilize before any landing attempt |

**Note:** The Mi-24P's nosewheel steering is not available in hover. Direction is controlled entirely by pedals.

### Exercise 4 — Running Takeoff (Primary Technique)

The running takeoff uses a portion of runway to accelerate before becoming airborne. It is the **standard Mi-24P departure**.

| Step | Action | Notes |
|---|---|---|
| 1 | From hover — nose into runway, confirm clearance | Align with runway centerline |
| 2 | **Collective** — maintain hover height (3–5 m) | Do not climb; taxi into position |
| 3 | At the runway threshold — **forward cyclic** | Begin acceleration run |
| 4 | Aircraft accelerates along runway | Altitude should stay 3–5 m — use collective to hold |
| 5 | Through **50 km/h (ETL)** — nose wants to pitch up | Light forward cyclic to hold attitude |
| 6 | At **80–100 km/h** — aircraft is safely airborne | Wing lift supplements rotor; power demand reduces |
| 7 | **Allow aircraft to climb** — reduce forward cyclic slightly | Positive rate of climb established |
| 8 | **Gear UP** | After confirmed positive rate of climb |
| 9 | Climb at **120–140 km/h (Vy)** | Best rate of climb speed |
| 10 | Continue climb to assigned altitude | |

**Running Takeoff Power Profile:**

| Phase | Torque | Notes |
|---|---|---|
| Hover (start) | 75–80% | Initial lift |
| Acceleration (0–50 km/h) | 80–85% | Maximum demand in transition |
| ETL transition (50–80 km/h) | 70–75% | Power reduces as wing lift develops |
| Climb (100+ km/h) | 70–80% | Sustained climb power |

### Exercise 5 — Hover Takeoff (Secondary Technique)

Hover takeoff is used when no runway run is available (confined area).

| Step | Action | Notes |
|---|---|---|
| 1 | Hover power check complete — torque ≤ 80% | Confirm OGE hover available |
| 2 | From ground — **collective UP** smoothly to lift | Expect torque up to 80–85% |
| 3 | Establish hover at 3–5 m | Stabilize — do not rush climb |
| 4 | **Forward cyclic** — smooth acceleration | Not a jump — a controlled transition |
| 5 | Through ETL (50 km/h) — power demand reduces | Hold altitude with collective |
| 6 | At 80–100 km/h — aircraft is flying efficiently | |
| 7 | **Gear UP** — positive rate confirmed | |
| 8 | Climb at 120–140 km/h | |

### Exercise 6 — Climb Profiles

Practice each climb profile twice:

| Profile | Airspeed | Rate of Climb | Use |
|---|---|---|---|
| **Best Rate (Vy)** | 120–140 km/h | Max available | Standard departure |
| **Best Angle (Vx)** | 100–110 km/h | Steeper angle | Obstacle clearance |
| **Cruise Climb** | 160–180 km/h | Moderate | Long transit climb |

For each profile:
1. Establish entry speed on runway heading at low altitude
2. Apply climb power (70–80% torque)
3. Climb to 500 m, maintain assigned airspeed
4. Level off at 500 m
5. Note torque, airspeed, and rate of climb achieved

---

## Completion Standards

| Standard | Requirement |
|---|---|
| **Hover power check** | Correctly performed and result interpreted before any hover operation |
| **Stationary hover** | ±1 m altitude, ±3 m drift, 30 seconds |
| **Pedal turn** | Within ±5° of target heading; altitude ±1 m throughout |
| **Hover taxi** | Speed ≤ 10 km/h; altitude maintained ±1 m; no abrupt inputs |
| **Running takeoff** | Smooth acceleration; airborne before 200 m; ETL transition smooth; no bounce |
| **Gear retraction** | Completed after positive rate of climb confirmed |
| **Climb airspeed** | Within ±10 km/h of Vy (120–140 km/h) |
| **Hover takeoff (if attempted)** | Smooth lift; no excessive torque (≤ 90% transient); controlled transition |

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| Skipping hover power check | Attempting hover landing with insufficient power margin | "Power check is not optional. Torque > 85% = running landing required" |
| Large cyclic inputs in hover | Pendulum effect; altitude excursions | "Tiny inputs. Think about where you want the disc, not where you want the nose" |
| Climbing during takeoff roll (hover takeoff from taxi) | Excess altitude on takeoff roll; risks hitting obstacles or losing energy | "Stay at 3–5 m until ETL. The temptation to climb early is strong. Don't" |
| Pulling collective aggressively through ETL | Torque spike; control surprise | "ETL is a reward — the aircraft wants to fly. Accept the free energy" |
| Forgetting gear retraction | Gear remains down in flight; drag penalty | "Gear check: positive rate, gear UP. Every time" |
| Riding the pedals during acceleration | Directional oscillations during takeoff roll | "Set heading, add pedal trim, make corrections — don't ride the pedals" |
| Over-correcting heading in hover taxi | Heading oscillations; yaw porpoise | "Anticipate heading change. Put in pedal then wait. Correct to stop" |

---

*Based on Mi-24P RLE and Eagle Dynamics DCS World Mi-24P Hind module documentation. For simulation use only.*
