# Event 3 — Gravity Bombs (CCIP & CCRP)

> **Course:** A-10A Weapons Employment | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — CCIP Delivery (Mk-82 Dive)](#part-1--ccip-delivery-mk-82-dive)
5. [Part 2 — CCRP Delivery (Mk-82 Level)](#part-2--ccrp-delivery-mk-82-level)
6. [Part 3 — Low-Level Delivery (Mk-82AIR)](#part-3--low-level-delivery-mk-82air)
7. [Part 4 — Heavy Bomb Delivery (Mk-84)](#part-4--heavy-bomb-delivery-mk-84)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Deliver Mk-82 gravity bombs in CCIP mode from a 30° dive, impacting within 50 m of the target
- [ ] Execute a CCRP level-flight bomb delivery using HUD steering and auto-release cues
- [ ] Deliver Mk-82AIR high-drag bombs from low altitude (500–1,000 ft AGL)
- [ ] Deliver Mk-84 heavy bombs with correct frag-avoidance pull-off altitude
- [ ] Describe the minimum safe release altitude for each bomb type

---

## Ground Brief

### Two Modes, Two Situations

| Mode | Profile | When to Use |
|---|---|---|
| **CCIP** | Diving attack | Target visually acquired; accurate placement needed |
| **CCRP** | Level flight | Stand-off delivery; target obscured or SAM threat prevents diving |

CCIP is more accurate but exposes you to ground fire during the dive. CCRP allows delivery from level flight at stand-off range but is less precise.

### Bomb Types Available

| Bomb | Weight | Drag | Frag Radius | Min Safe Release Alt |
|---|---|---|---|---|
| Mk-82 | 500 lb | Low (slick) | ~300 m | 2,000 ft AGL |
| Mk-82AIR | 500 lb | High (ballute) | ~300 m | 500 ft AGL* |
| Mk-84 | 2,000 lb | Low (slick) | ~600 m | 3,000 ft AGL |

*Mk-82AIR ballute retards the bomb, allowing safe low-level delivery — but the bomb must have time to decelerate. Do not release below 500 ft AGL.

### Frag Avoidance

> **Warning:** Flying through your own fragmentation pattern will damage or destroy your aircraft. DCS models self-damage from your own weapons. Plan pull-off altitude based on the largest bomb in your loadout.

```
Release ────→  Bomb falls  ────→  Impact  ────→  Frag pattern expands
    ↑                                                    ↑
 You are HERE                              Do NOT be HERE
    Pull off ≥ 4 G immediately after release
```

---

## Pre-Mission Setup

- [ ] Place 1 point target (single building or hardened vehicle) for CCIP
- [ ] Place 1 area target (vehicle park) for CCRP
- [ ] Place 1 "low-level target" near flat terrain for Mk-82AIR work
- [ ] Weather: Day VMC
- [ ] **Loadout:**
  - 4× Mk-82 (slick) — inner wing pylons
  - 2× Mk-82AIR — outer wing pylons
  - 2× Mk-84 — fuselage stations
- [ ] Fuel: 65%
- [ ] Note target field elevation for CCRP altitude calculations

---

## Part 1 — CCIP Delivery (Mk-82 Dive)

CCIP (Continuously Computed Impact Point) projects a pipper on the HUD that shows where the bomb will impact based on current aircraft state. Place the pipper on the target and release.

### Switchology
1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Weapon Select** — cycle to Mk-82 (`D`)
3. - [ ] Confirm CCIP pipper displayed on HUD (pipper moves with dive angle and airspeed)

### Attack Procedure

**Entry:** 10,000–12,000 ft MSL, 350 kts. Target at 12 o'clock, 3–4 NM.

1. - [ ] Roll in: push over to **25–35° dive**, wings level
2. - [ ] Track: place CCIP pipper on target, let it stabilize
3. - [ ] At **6,000–8,000 ft slant range** — pipper settles on target:
   - [ ] **Release** (`Space`) — single bomb
4. - [ ] **Immediate pull-off**: ≥ 4 G pull, minimum **2,000 ft AGL**
5. - [ ] Egress: turn off threat axis
6. - [ ] **Master Arm** — SAFE

### CCIP Dive Parameters

| Parameter | Standard |
|---|---|
| Entry altitude | 10,000–12,000 ft MSL |
| Dive angle | 25–35° |
| Airspeed at release | 350–400 kts |
| Release slant range | 5,000–8,000 ft |
| Min pull-off altitude | 2,000 ft AGL (Mk-82 frag) |

**Instructor Note:** The most common CCIP failure is releasing too early (pipper still short of target) or too late (dangerously low). Brief the student: "When the pipper is on the target, release — then pull. Do not wait to observe impact."

---

## Part 2 — CCRP Delivery (Mk-82 Level)

CCRP (Continuously Computed Release Point) calculates the exact moment to release the bomb during a level fly-over. The HUD provides a vertical steering line and a release cue.

### Switchology
1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Weapon Select** — cycle to Mk-82 (`D`)
3. - [ ] Confirm CCRP mode is active — HUD shows vertical steering line and range-to-release cue

> **FC3 Note:** The A-10A switches between CCIP and CCRP based on aircraft attitude. In a dive, the HUD shows CCIP. In level flight, it transitions to CCRP. You do not manually select the mode.

### Attack Procedure

1. - [ ] Establish level flight at **8,000–12,000 ft MSL**, 350 kts
2. - [ ] Align with the vertical steering line on HUD (fly toward the line until centered)
3. - [ ] When aligned — hold **Weapon Release** (`Space`) continuously
4. - [ ] Do **not** release and re-press — hold the button until the bomb releases automatically
5. - [ ] The computer releases at the calculated release point — you will see/hear the release
6. - [ ] Continue wings-level for 3–4 seconds after release
7. - [ ] **Master Arm** — SAFE after delivery

### CCRP Key Numbers

| Parameter | Value |
|---|---|
| Delivery altitude | 5,000–15,000 ft MSL |
| Airspeed | 300–400 kts |
| Expected accuracy (CEP) | 50–150 m |

**Instructor Note:** Students often tap and release the pickle button. Brief: "Press and hold from alignment through release. Let the jet do the math."

---

## Part 3 — Low-Level Delivery (Mk-82AIR)

The Mk-82AIR deploys a ballute (balloon-parachute) after release that retards the bomb, creating separation between the aircraft and the impact point. This allows safe delivery from altitudes as low as 500 ft AGL at high speed.

### When to Use Mk-82AIR
- SAM threat requires low-altitude ingress below the radar horizon
- Terrain masking approach — pop up is too dangerous
- Target on a road or in a valley where dive delivery is impractical

### Switchology
1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Weapon Select** — cycle to Mk-82AIR (`D`)
3. - [ ] Confirm CCIP pipper on HUD

### Attack Procedure (Low-Level)

**Entry:** 500–1,000 ft AGL, **400–450 kts** (high speed for survivability).

1. - [ ] Acquire target visually — plan the run so target passes under the nose
2. - [ ] Align for a **level or shallow (5–10°) attack**
3. - [ ] Place CCIP pipper on target
4. - [ ] **Release** (`Space`) at pipper-on-target
5. - [ ] **Continue straight and level** for 2–3 seconds after release (bomb needs clean separation)
6. - [ ] Turn off target — do not overfly the impact point
7. - [ ] Ballute deploys — bomb decelerates behind and below the aircraft

### Mk-82AIR Delivery Diagram

```
  ═══════►  Aircraft at 500 ft, 420 kts  ═══════►
                    |
               [Bomb release]
                    |
                    ↓  ← Ballute deploys
                    ·
                    ·  ← Bomb retards and falls
                    ·
                   💥  ← Impact ~1,000–2,000 ft behind release point
```

> **Warning:** If the ballute fails to deploy (rare in DCS), the Mk-82AIR behaves like a slick Mk-82 and you may fly through the frag pattern. Maintain awareness of your escape flight path.

---

## Part 4 — Heavy Bomb Delivery (Mk-84)

The Mk-84 is a 2,000 lb general-purpose bomb. It has an enormous blast radius and is reserved for high-value hardened targets — bridges, bunkers, command posts, concrete shelters.

### Key Differences from Mk-82

| Parameter | Mk-82 | Mk-84 |
|---|---|---|
| Weight | 500 lb | 2,000 lb |
| Blast radius | ~300 m | ~600 m |
| Min pull-off alt | 2,000 ft AGL | **3,000 ft AGL** |
| Best targets | General purpose | Hardened structures, bridges |

### Delivery

Same CCIP procedure as Mk-82, with two critical changes:
1. **Higher pull-off altitude:** 3,000 ft AGL minimum — the frag envelope is massive
2. **Steeper dive recommended:** 30–45° — the Mk-84 needs accuracy (one bomb, one target)

### Attack Procedure (CCIP)

1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Weapon Select** — cycle to Mk-84 (`D`)
3. - [ ] Roll in: **30–45° dive**, 350 kts
4. - [ ] Place CCIP pipper on target — let it stabilize
5. - [ ] **Release** at pipper-on-target
6. - [ ] **Immediate pull-off**: ≥ 4 G, minimum **3,000 ft AGL**
7. - [ ] Egress away from target
8. - [ ] **Master Arm** — SAFE

> **Instructor Note:** Students underestimate the Mk-84's frag envelope. A 600 m blast radius means if you release at 2,500 ft AGL in a 30° dive, fragments will reach your altitude. Brief: "Treat the Mk-84 like a small area weapon. Give it respect."

---

## Completion Standards

| Standard | Requirement |
|---|---|
| CCIP bomb delivery (Mk-82) | Impact within 50 m of target on ≥ 2 of 3 passes |
| CCIP pull-off alt (Mk-82) | Never below 2,000 ft AGL |
| CCRP delivery | Bomb impacts within 150 m of intended target |
| CCRP technique | Held pickle button through auto-release (no tap) |
| Mk-82AIR delivery | Delivered from ≤ 1,000 ft AGL; bomb impacts within 100 m |
| Mk-84 pull-off alt | Never below 3,000 ft AGL |
| Master Arm discipline | SAFE after every pass |

---

## Common Errors

| Error | Correction |
|---|---|
| CCIP pipper not settling | Stabilize the dive — reduce bank and pitch oscillations before release |
| Releasing too low (CCIP) | Set hard deck: start pull at min alt regardless of pipper position |
| CCRP — tapping pickle button | Hold continuously from alignment through auto-release |
| CCRP — maneuvering during release | Fly straight and level — wings-level flight required for accurate computation |
| Mk-82AIR — releasing below 500 ft | Ballute needs time to deploy; minimum 500 ft AGL |
| Mk-84 — treating it like a Mk-82 | Increase pull-off altitude to 3,000 ft; respect the larger frag envelope |
| Not noting target field elevation | Compute AGL from MSL altitude minus field elevation before each pass |

---

[← Event 2: Gun & Rockets](event-2-guns-rockets.md) | [→ Event 4: Cluster Munitions](event-4-cluster-munitions.md)

---

*Based on T.O. 1A-10A-34-1-1 and Eagle Dynamics DCS World documentation. For simulation use only.*
