# Event 3 — GSh-30K Cannon Employment

> **Course:** Mi-24P Hind Weapons Qualification Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [System Data](#system-data)
4. [Employment Profiles](#employment-profiles)
5. [Recoil Management](#recoil-management)
6. [Target Type Matrix](#target-type-matrix)
7. [Cannon vs. ATGM Decision](#cannon-vs-atgm-decision)
8. [Crew Coordination](#crew-coordination)
9. [In-Sim Procedures](#in-sim-procedures)
10. [Common Errors](#common-errors)
11. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] State GSh-30K specifications including effective range, rate of fire, and ammunition types
- [ ] Execute a diving strafe attack with correct entry altitude, dive angle, and break-off range
- [ ] Demonstrate burst discipline (1–2 second bursts) and manage 250-round ammunition budget
- [ ] Apply correct pedal and cyclic inputs to compensate for cannon recoil
- [ ] Select appropriate attack profile for each target type
- [ ] Execute the cannon employment crew coordination calls in correct sequence
- [ ] Perform post-engagement BDA and determine need for re-attack

---

## Ground Brief

### The Cannon as Last Resort — and First Weapon

The GSh-30K is simultaneously the Mi-24P's most limited weapon and its most readily available. It cannot be jettisoned, it is always loaded, and it requires zero setup time — pull the trigger and it fires. But it has hard limits: **fixed-forward mount** means the pilot aims the aircraft at the target, and **250 rounds** limits the pilot to roughly 5–6 engagements before the gun runs dry.

**The cannon is best used:**
- Against soft targets and light armor at close range (<1,500 m)
- For suppression of AAA while the WSO engages with ATGMs
- When ATGMs have been exhausted
- For time-critical engagements requiring immediate fires

**The cannon should not be used:**
- As a primary weapon against MBT frontal armor
- At ranges exceeding 1,500 m (effect is area suppression only)
- When heavy AAA threat makes diving attacks suicidal
- Against targets in defilade that the pilot cannot see

### The Fixed-Mount Problem

Because the GSh-30K is bolted to the starboard fuselage and does not traverse, **the pilot is the gun mount**. Every bullet goes where the nose points. This makes cannon employment a piloting exercise, not just a weapons exercise.

---

## System Data

| Specification | Value | Notes |
|---|---|---|
| **Designation** | GSh-30K (Gryazev-Shipunov) | Soviet 9A623K |
| **Mount** | Fixed forward, starboard fuselage pod | Non-traversing |
| **Caliber** | 30×165 mm | Same family as GSh-30-1 (Su-25) |
| **Barrel Configuration** | Twin-barrel, side-by-side | Parallel bore axes |
| **Rate of Fire** | 2,600–3,000 RPM combined | ~43–50 rounds/second |
| **Ammunition** | 250 rounds standard (DCS) | ~5–6 seconds continuous fire |
| **Muzzle Velocity** | 890 m/s (APHE) / 900 m/s (HE-Frag) | High velocity; flat to 1,000 m |
| **Effective Range** | 800 m (armor) / 1,500 m (soft targets) | Accuracy degrades beyond 1,500 m |
| **Max Ballistic Range** | 4,000 m | Area suppression only |
| **Dispersion** | 2–3 mils (stationary) / 4–6 mils (in flight) | |
| **Recoil Force** | ~5,000 N average per barrel | Produces yaw moment |

### Ammunition Types

| Round | Warhead | Penetration | Best Targets |
|---|---|---|---|
| **3UOF8 APHE** | Armor-piercing HE (steel core + HE filler) | 65 mm RHA @ 500 m / 40 mm @ 1,000 m | Light armor, APCs, IFVs, SPAAGs |
| **3UOR8 HE-Frag** | HE fragmentation (pre-fragmented sleeve) | Area effect (~5 m lethal radius) | Soft targets, troops, trucks, light structures |

**DCS Standard Belt:** Mixed (~60% APHE, ~40% HE-Frag). Tracers every 5th round for burst observation. Ammunition type cannot be selected in flight.

### Penetration vs. Range

| Range | APHE Penetration (RHA) | Notes |
|---|---|---|
| 200 m | ~80 mm | Point-blank; maximum penetration |
| 500 m | ~65 mm | Optimal engagement range for armor |
| 1,000 m | ~40 mm | Marginal against IFV frontal armor |
| 1,500 m | ~25 mm | Effective only against thin-skinned vehicles |
| 2,000 m | ~15 mm | Soft targets only |

---

## Employment Profiles

### Profile 1 — Diving Strafe Attack (Primary)

The preferred cannon attack profile provides the best combination of accuracy, pilot visibility of target, and ammunition effectiveness.

| Parameter | Value |
|---|---|
| **Entry Altitude** | 800–1,200 m AGL |
| **Entry Airspeed** | 220–260 km/h |
| **Dive Angle** | 15–25° |
| **Firing Range** | 800–1,200 m |
| **Break-Off Range** | 400–600 m |
| **Minimum Recovery Altitude** | 100 m AGL |
| **Burst Duration** | 1–2 seconds |

**Execution Steps:**
1. **Approach:** Level flight at entry altitude, target bearing 2–4 km
2. **Roll-In:** 30–45° bank to align with target; reduce collective
3. **Dive Establish:** Lower nose to achieve 15–25° dive angle
4. **Acquisition:** Pilot acquires target through sight; WSO confirms target
5. **Firing Pass:** Steady dive; trigger squeeze at 800–1,200 m
6. **Break-Off:** Pull up at 400–600 m range; level off at 100 m+ AGL minimum
7. **BDA:** WSO reports BDA; pilot holds egress heading

### Profile 2 — Shallow Strafe Pass (Secondary)

Used for low-level approach under threat radar, or against area targets.

| Parameter | Value | Application |
|---|---|---|
| **Entry Altitude** | 200–400 m AGL | Low-level approach from terrain masking |
| **Dive Angle** | 5–10° | Reduced target exposure time |
| **Firing Range** | 1,000–1,500 m | Extended range for soft targets |
| **Target Types** | Soft vehicles, troops, structures | Not effective against armor |
| **Burst Duration** | 2–3 seconds | Longer burst compensates for shallower angle |

### Profile 3 — Level Run (Suppression Only)

Emergency / suppression profile only. Not a precision engagement tool.

| Parameter | Value | Limitations |
|---|---|---|
| **Altitude** | 50–200 m AGL | High exposure to AAA and MANPADS |
| **Firing Range** | 1,500–2,000 m | Reduced accuracy; suppression only |
| **Target Types** | Area suppression | Not for precision engagement |
| **Burst Duration** | 3–4 seconds | Longer burst compensates for reduced accuracy |

---

## Recoil Management

### Effects on Aircraft

| Effect | Description | Pilot Response |
|---|---|---|
| **Yaw (left)** | Starboard-mounted gun produces left yaw moment | Pre-load right pedal before trigger |
| **Pitch (nose-up slight)** | Mount position below CG | Slight forward cyclic during firing |
| **Deceleration** | ~1–2 km/h speed loss per second | Insignificant in dive; notable level flight |
| **Vibration** | Airframe shakes during burst | Accept it; do not chase the aim |

### Recoil Compensation Technique

1. Anticipate left yaw — apply slight right pedal before squeezing trigger
2. Maintain constant pedal pressure throughout burst
3. Release pedal smoothly as firing stops
4. Accept minor dispersion — do not try to correct aim mid-burst

### Ammunition Conservation

| Situation | Budget | Burst | Rationale |
|---|---|---|---|
| **Single high-value target** | 40–60 rounds (1–1.5 sec) | Short, precise | Conserve for re-attack |
| **Multiple soft targets** | 30–40 rounds per target | Short | One burst per target, move on |
| **Area suppression** | 80–100 rounds (2–3 sec) | Medium | Wider area requires longer burst |
| **Emergency self-defense reserve** | 50–60 rounds minimum | — | Always retain some for self-defense |
| **Total sortie (250 rounds)** | Plan for 4–6 engagements | — | Think before each trigger pull |

**Ammunition Counting:** Each 1-second burst ≈ 40–50 rounds. After 3 engagements, assume ~50% remaining. After 5 engagements, consider RTB for rearm.

---

## Target Type Matrix

| Target | Profile | Range | Burst | Expected Effect |
|---|---|---|---|---|
| **MBT (frontal)** | Steep dive, APHE | 600–800 m | 1–2 sec | Optics/tracks damage; unlikely kill |
| **MBT (flank/rear)** | Diving strafe | 800–1,000 m | 2–3 sec | Engine/fuel fire possible |
| **Light Armor (BMP)** | Diving strafe | 800–1,200 m | 1–2 sec | High kill probability |
| **APCs** | Diving / shallow | 1,000–1,500 m | 1–2 sec | High kill probability |
| **Trucks / Soft Vehicles** | Shallow / level | 1,000–2,000 m | 2–3 sec | Destruction likely |
| **AAA Sites** | Diving strafe | 600–1,000 m | 2–3 sec | Crew suppression / equipment damage |
| **Troops in Open** | Shallow pass | 1,500–2,000 m | 3–4 sec | Area suppression |
| **Bunkers / Structures** | Diving strafe | 800–1,000 m | 2–4 sec | Damage; unlikely destruction |

---

## Cannon vs. ATGM Decision

| Use Cannon When | Use ATGM When |
|---|---|
| Range < 1,500 m and soft/light armor | Range > 1,500 m |
| Multiple small targets in close proximity | Heavy armor requiring guaranteed kill |
| Time-critical engagement (no ATGM setup time) | Standoff required due to heavy AAA |
| Need to suppress area targets or troops | Precision required (minimize collateral damage) |
| ATGM inventory depleted | Target is stationary with SACLOS time available |
| Target inside ATGM minimum range (<400 m) | Target is in defilade — pilot cannot see it |

---

## Crew Coordination

### Single-Player Workflow

1. **WSO seat (`1`):** Select cannon mode; verify Master Arm ARMED; identify target
2. **Switch to Pilot seat (`2`):** Maneuver to attack heading; acquire target
3. **Remain in Pilot seat:** Execute attack profile; fire cannon; break off
4. **Return to WSO seat (`1`):** Conduct BDA; select next weapon if required

### Multi-Crew Calls

| Sequence | Pilot | WSO |
|---|---|---|
| Target call | "Tally" or "No joy" | "Target, [type], [bearing], [range], ready for cannon" |
| Engage | "Rolling in" | "Cleared to fire" |
| Firing | "Firing" | (Monitors flight path; calls abort if needed) |
| Break | "Breaking [direction]" | "[BDA call]" |

---

## In-Sim Procedures

### Mission Setup

1. Load a practice mission with:
   - 4–6 soft vehicle targets (trucks, APCs) at 1–2 km range
   - 2–3 armor targets (tanks) at 800 m range
   - Open terrain; no significant AAA threat for initial practice
2. Loadout: Cannon only (no external stores) — isolates cannon practice from other distractors
3. Starting position: Aircraft running, 3 km from target range

### Practice Sequence

**Pass 1–2: Soft Vehicle Targets (Diving Strafe)**
- Entry: 800 m AGL, 240 km/h
- Dive: 15–20°
- Fire: 1–2 second burst at 1,000–1,200 m
- Break: Pull up at 600 m; level at 100 m AGL
- BDA: WSO calls result

**Pass 3–4: Light Armor (Optimal Range)**
- Entry: 1,000 m AGL, 250 km/h
- Dive: 20°
- Fire: 1–2 second burst at 800–1,000 m
- Break: Pull up at 500 m

**Pass 5: Area Suppression (Shallow Profile)**
- Entry: 300 m AGL, 220 km/h
- Dive: 5–8°
- Fire: 2–3 second burst at 1,500 m
- Break: Climbing turn away from target area

### DCS Key Bindings

| Function | Default Key |
|---|---|
| **Fire (Cannon / Primary)** | `Space` |
| **Master Arm Toggle** | `O` |
| **Weapon Mode Cycle** | `D` |

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| **Too steep dive angle** | Excessive altitude loss; terrain impact risk | Limit to 25° maximum; watch altimeter |
| **Firing too early (>1,200 m)** | Rounds fall short; wasted ammunition | Wait for 800–1,200 m firing range |
| **Excessive burst (>2 sec)** | Ammunition wastage; barrel overheating | Practice 1–2 sec burst discipline |
| **Poor pedal coordination** | Rounds scatter left/right | Pre-load right pedal before trigger |
| **Late break-off** | AAA exposure; terrain impact | Break at 400–600 m regardless of BDA |
| **Using cannon against MBT frontal** | Ineffective; wasted ammunition | Use ATGM for frontal MBT engagement |
| **No BDA** | Cannot assess re-engagement need | Keep visual on target through break |

---

## Completion Standards

The student must meet the following standards in at least 4 of 6 practice passes:

- [ ] Correct entry altitude (800–1,200 m AGL) and airspeed (220–260 km/h)
- [ ] Dive angle maintained 15–25° throughout firing pass
- [ ] Firing initiated at 800–1,200 m range
- [ ] Break-off initiated at 400–600 m; minimum recovery altitude 100 m AGL
- [ ] Burst duration 1–2 seconds (demonstrated by tracer pattern or audio cue)
- [ ] Correct crew coordination calls made in sequence
- [ ] BDA reported within 15 seconds of weapon impact
- [ ] No ammunition exhaustion before completing all assigned targets (demonstrate budget management)

---

*Based on DCS World Mi-24P Hind module by Eagle Dynamics and Mi-24P RLE. For simulation use only.*
