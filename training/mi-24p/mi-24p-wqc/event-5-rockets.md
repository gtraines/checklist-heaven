# Event 5 — Unguided Rocket Employment

> **Course:** Mi-24P Hind Weapons Qualification Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Rocket Systems Data](#rocket-systems-data)
4. [Launcher Pod Data](#launcher-pod-data)
5. [CCIP Integration](#ccip-integration)
6. [Employment Profiles](#employment-profiles)
7. [Salvo Fire Control](#salvo-fire-control)
8. [Target vs. Weapon Selection](#target-vs-weapon-selection)
9. [In-Sim Procedures](#in-sim-procedures)
10. [Common Errors](#common-errors)
11. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Identify S-5, S-8, S-13, and S-24 rocket systems by caliber, warhead, and intended target type
- [ ] Select the correct rocket type and warhead for a given target
- [ ] Execute a diving rocket attack profile using CCIP pipper
- [ ] Execute a shallow-pass rocket attack profile at low altitude
- [ ] Demonstrate correct salvo size selection (single / paired / full salvo) for target type
- [ ] Plan a mixed-loadout engagement sequence (armor, soft targets, structures)
- [ ] Make correct crew coordination calls for rocket employment (multi-player or verbalized)
- [ ] Execute a post-attack break and assess BDA

---

## Ground Brief

### Why Rockets? The Gap Between Cannon and ATGM

The Mi-24P's cannon is lethal but limited to roughly 1,000–1,500 m against moving targets. ATGMs cover 400–6,000 m but are expensive, require 8–15 seconds of platform stability, and are one shot per target. Rockets fill the space in between and provide area effects that neither cannon nor ATGM can match:

| Need | Best Weapon |
|---|---|
| Precision kill on heavy armor (2,000+ m) | ATGM |
| Area suppression / soft targets | **Rockets** |
| Multiple light vehicles in same engagement | **Rockets** |
| Personnel in open | **Rockets** |
| Bunkers (reinforced) | **Rockets (S-13/S-24)** |
| Hard-point targets <1,500 m, maneuvering | Cannon |

### Ammunition Budget Awareness

Rockets are a one-pass expenditure. A full salvo of an S-8 pod fires all 20 rockets in under 2 seconds. Plan before attacking:
- Which pod for which target?
- Single / paired / full salvo?
- Re-engagement planned or single pass?

---

## Rocket Systems Data

### S-5 (57 mm) — Area Suppression

| Specification | Value |
|---|---|
| **Caliber** | 57 mm |
| **Weight** | 3.7–5.0 kg (by variant) |
| **Motor Burn** | 0.7–1.0 sec |
| **Effective Range** | 300–1,500 m |
| **Max Range** | 2,500–3,000 m |
| **Muzzle Velocity** | 450 m/s |
| **Dispersion** | High (~5–8 mils) |
| **Primary Role** | Area saturation; troop suppression |

**S-5 Warhead Variants:**
| Designation | Type | Effect | Best Targets |
|---|---|---|---|
| **S-5M** | HE-Frag | Blast + fragments (lethal radius ~5 m) | Troops, soft vehicles |
| **S-5K** | HEAT | ~130 mm RHA penetration | Light armor, trucks |
| **S-5KO** | HEAT + Frag | Dual-purpose | Mixed targets |
| **S-5S** | Flechette (APERS) | 1,000 flechettes per rocket | Troops in open |

> *⚠ Realism Divergence: S-5 availability depends on your DCS module version. If S-5/UB-16 or UB-32 pods are unavailable, S-8 HE-Frag serves the same tactical role.*

### S-8 (80 mm) — Primary Rocket

| Specification | Value |
|---|---|
| **Caliber** | 80 mm |
| **Weight** | 11.3 kg |
| **Motor Burn** | 1.1 sec |
| **Effective Range** | 500–2,000 m |
| **Max Range** | 4,000 m |
| **Muzzle Velocity** | 510 m/s |
| **Launcher Pod** | B-8V20A (20 rockets) |

**S-8 Warhead Variants:**
| Designation | Type | Effect | Best Targets |
|---|---|---|---|
| **S-8KOM** | HEAT | 420 mm RHA penetration | Light armor, APCs |
| **S-8OFP2** | HE-Frag | Area fragmentation | Soft targets, personnel |
| **S-8TsM** | Thermobaric | Blast/overpressure | Bunkers, structures |
| **S-8BM** | Bunker penetrator | Delayed fuze + HE | Hardened structures |

### S-13 (122 mm) — Heavy Rocket

| Specification | Value |
|---|---|
| **Caliber** | 122 mm |
| **Weight** | 58.5 kg |
| **Motor Burn** | 2.2 sec |
| **Effective Range** | 800–2,500 m |
| **Max Range** | 4,500 m |
| **Muzzle Velocity** | 475 m/s |
| **Launcher Pod** | B-13L (5 rockets) |

**S-13 Warhead Variants:**
| Designation | Type | Best Targets |
|---|---|---|
| **S-13OF** | HE-Frag | Soft area targets |
| **S-13B** | Bunker penetrator | Concrete structures |
| **S-13DF** | Dual-purpose | Mixed targets |

### S-24 (240 mm) — Heavy Unguided Rocket

| Specification | Value |
|---|---|
| **Caliber** | 240 mm |
| **Weight** | 235 kg |
| **Motor Burn** | 3.0 sec |
| **Effective Range** | 1,500–4,000 m |
| **Max Range** | 6,000 m |
| **Muzzle Velocity** | 420 m/s |
| **Launcher** | APU-68UM rail (1 per rail; outer pylons only) |
| **Warhead** | S-24B (123 kg HE) — massive blast |
| **CCIP** | None — manual aim only |

> *⚠ Realism Divergence: Real S-24 employment from a helicopter is extremely rare. The 235 kg rocket's recoil severely affects aircraft handling. DCS may not fully represent the handling challenges. Reserve S-24 for large, hardened targets only.*

---

## Launcher Pod Data

| Pod | Rockets | Capacity | Caliber | Stations |
|---|---|---|---|---|
| **UB-16-57** | S-5 | 16 | 57 mm | All (1–4) |
| **UB-32A-24** | S-5 | 32 | 57 mm | All (1–4) |
| **B-8V20A** | S-8 | 20 | 80 mm | Inner/Outer (2,3,4) |
| **B-13L** | S-13 | 5 | 122 mm | All |
| **APU-68UM** | S-24 | 1 | 240 mm | Outer only (1,4) |

---

## CCIP Integration

The Mi-24P computes a Continuously Computed Impact Point (CCIP) pipper on the PKV-1 sight for S-5, S-8, and S-13 rockets. Place the pipper on the target and fire.

| Rocket | CCIP Accuracy | Effective Range | Notes |
|---|---|---|---|
| **S-5** | ±15 m at 1 km | To 1,500 m | Area weapon; accuracy secondary |
| **S-8** | ±10 m at 1 km | To 2,000 m | Best CCIP accuracy |
| **S-13** | ±20 m at 1 km | To 2,500 m | Heavier; more dispersion |
| **S-24** | None | Manual aim only | Fixed pipper; no CCIP |

> *⚠ Realism Divergence: DCS CCIP may be more accurate than the real Mi-24P system. Real crews used a basic computed sight depression rather than a dynamic pipper. Expect easier-than-real accuracy in DCS.*

### CCIP Discipline

Stable platform = accurate CCIP. Any deviation in airspeed, altitude, or bank during the firing pass moves the pipper. Wait for a stable pipper on the target before firing — do not rush the shot.

---

## Employment Profiles

### Profile 1 — Diving Attack (Primary)

Best accuracy; appropriate for most ground targets.

**S-8 Diving Parameters:**
| Parameter | Value |
|---|---|
| **Entry Altitude** | 800–1,500 m AGL |
| **Dive Angle** | 20–30° |
| **Entry Airspeed** | 200–240 km/h |
| **Release Range** | 800–1,500 m |
| **Salvo Size** | 2–4 rockets |
| **Break Altitude** | Pull out above 500 m AGL |
| **Break Range** | No closer than 500 m from target |

**S-13 Diving Parameters:**
| Parameter | Value |
|---|---|
| **Entry Altitude** | 1,000–1,800 m AGL |
| **Dive Angle** | 25–35° |
| **Release Range** | 1,200–2,000 m |
| **Salvo Size** | 1–2 rockets |

**Execution Steps:**
1. **Approach** — Level flight at entry altitude; identify target
2. **Roll-in** — Bank to align with target; reduce power
3. **Dive** — Achieve target dive angle; stabilize airspeed
4. **Acquire** — CCIP pipper visible on target
5. **Fire** — Trigger when pipper centered; maintain dive briefly
6. **Break** — Pull up at minimum range; level off at safe altitude

### Profile 2 — Shallow Pass (Low Threat)

Reduced exposure time; less precise.

| Parameter | S-8 | S-13 |
|---|---|---|
| **Approach Altitude** | 50–200 m AGL | 100–300 m AGL |
| **Dive Angle** | 5–15° | 10–20° |
| **Release Range** | 1,500–2,500 m | 2,000–3,000 m |
| **Best Targets** | Area suppression | Structures, concentrations |

### Profile 3 — Level/Running Fire (Emergency)

**Use only for area suppression or when no other option available:**
- Altitude: 30–100 m AGL
- Accuracy significantly degraded
- High exposure to ground fire
- No BDA possible on pass

---

## Salvo Fire Control

| Mode | Rockets Fired | Application |
|---|---|---|
| **Single** | 1 rocket | Point target; ammunition conservation |
| **Paired (2–4)** | 2–4 rockets | Small area; improved hit probability |
| **Full Salvo** | All remaining | Large area; saturation; rarely justified |

**Rule of Thumb:** Use the minimum effective salvo. A single S-13 hit destroys most soft structures. A 4-rocket S-8 salvo is enough for most light vehicle targets.

---

## Target vs. Weapon Selection

| Target Type | S-5 | S-8 HEAT | S-8 HE-Frag | S-13 | S-24 | Recommendation |
|---|---|---|---|---|---|---|
| **BMP / IFV** | Ineffective | ✓ Excellent | Limited | Overkill | Overkill | **S-8 HEAT** |
| **BTR / APC** | Marginal | ✓ Excellent | Good | Overkill | Overkill | **S-8 HEAT** |
| **Soft Vehicles / Trucks** | ✓ Excellent | Overkill | ✓ Excellent | Good | Overkill | **S-5M or S-8 HE-Frag** |
| **Troops in Open** | ✓ Excellent | Minimal | ✓ Excellent | Good | Extreme | **S-5 salvo / S-8 HE-Frag** |
| **Bunker (soft)** | Ineffective | Limited | Good | ✓ Excellent | Good | **S-13 HE** |
| **Bunker (hardened concrete)** | Ineffective | Minimal | Minimal | Good | ✓ Excellent | **S-24** |
| **Building / Command Post** | Good | Good | Good | ✓ Excellent | Good | **S-13 HE** |
| **AAA Site (mixed)** | Good | Good | ✓ Excellent | Good | Good | **S-8 HE-Frag** |
| **Troop Concentration** | ✓ Excellent | Limited | ✓ Excellent | ✓ Excellent | Good | **S-5 salvo or S-13** |
| **Bridge / Infrastructure** | Ineffective | Minimal | Minimal | Good | ✓ Excellent | **S-24** |

---

## In-Sim Procedures

### DCS Key Bindings

| Function | Default Key |
|---|---|
| **Select Rockets** | `D` (weapon cycle to rockets) |
| **Fire Rockets** | `Space` |
| **Pylon Select** | `W` / `E` (cycle) |
| **CCIP Toggle** | `O` (if available) |
| **Master Arm** | See Module 1 / Event 1 |

### Engagement Sequence (Single-Player)

**Setup (WSO Seat — `1`):**
1. Master Arm → **ARMED**
2. Weapon Selector → **ROCKETS**
3. Pylon Selector → correct pod/station
4. Salvo Mode → desired setting (if adjustable pre-flight)

**Attack (Pilot Seat — `2`):**
1. Identify target; maneuver to attack heading
2. Climb to entry altitude for dive
3. Roll in; establish dive angle
4. CCIP pipper → center on target
5. Fire (`Space`) at release range
6. Pull out; break to safety altitude

**BDA (WSO Seat — `1`):**
1. PKV-1 → observe impact
2. Call result: "Splash, [effect]" or "Miss, [direction]"
3. Select next pylon/weapon if re-engagement planned

### Mission Practice Sequence

**Exercise 1 — Single S-8 on stationary soft vehicle at 1,200 m:**
- Profile: Diving; entry 1,000 m AGL; 25° dive
- Standard: Impact within 15 m of target

**Exercise 2 — 4-rocket S-8 HEAT salvo on BMP at 1,500 m:**
- Profile: Diving; entry 1,200 m AGL
- Standard: 2 of 4 rockets within lethal radius

**Exercise 3 — Single S-13 on reinforced bunker at 2,000 m:**
- Profile: Diving; entry 1,500 m AGL; 30° dive
- Standard: Direct hit or within 10 m

**Exercise 4 — Mixed loadout engagement (2 targets, 2 weapon types):**
- Target 1: Soft vehicle — S-8 HE-Frag
- Target 2: Structure — S-13
- Profile: Two sequential diving passes
- Standard: Both impacts within 20 m of respective targets

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| **Wrong salvo setting** | Too few / too many rockets fired | Verify salvo selector before attack |
| **Poor CCIP discipline** | Rounds miss target area | Wait for stable pipper; never rush |
| **Inadequate dive angle** | Reduced accuracy; early break-off | Maintain 20–30° for best results |
| **Late target acquisition** | Rushed shot; poor aim | Acquire target early in roll-in |
| **Full salvo on single vehicle** | Ammunition waste | Use minimum effective salvo |
| **Wrong rocket type** | Suboptimal effect | Match warhead to target before attacking |
| **Ignoring wind** | Consistent left/right miss | Compensate for observed drift from prior rounds |
| **Poor post-attack break** | Ground impact risk | Pull out above 500 m AGL; never below 300 m |

---

## Completion Standards

The student must demonstrate the following to the instructor's satisfaction:

- [ ] Identify 4 rocket types by caliber and primary warhead (pre-flight oral)
- [ ] Select correct weapon for 4 different target types when prompted
- [ ] Execute diving attack on soft vehicle — impact within 20 m at 1,200 m range
- [ ] Execute diving attack on light armor with HEAT rocket — impact within 15 m
- [ ] Execute 2-target mixed loadout engagement with correct weapon selection for each
- [ ] Correct salvo size used for each target (no full-salvo waste on single soft target)
- [ ] Correct post-attack break executed; no altitude violation below 300 m AGL
- [ ] Correct crew coordination calls made in sequence

---

*Based on DCS World Mi-24P Hind module by Eagle Dynamics; Soviet unguided rocket system documentation; VVS employment doctrine. For simulation use only.*
