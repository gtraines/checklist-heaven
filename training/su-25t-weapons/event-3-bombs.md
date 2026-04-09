# Event 3 — Gravity Bombs (CCIP & CCRP)

> **Course:** Su-25T Weapons Employment | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — CCIP Delivery (Dive)](#part-1--ccip-delivery-dive)
5. [Part 2 — CCRP Delivery (Level)](#part-2--ccrp-delivery-level)
6. [Part 3 — RBK Cluster Bombs](#part-3--rbk-cluster-bombs)
7. [Completion Standards](#completion-standards)
8. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Deliver FAB-250 gravity bombs in CCIP mode from a 30° dive, impacting within 50 m of the target
- [ ] Designate a ground target using the Shkval and execute a CCRP level bomb delivery with automatic release
- [ ] Describe the minimum arming altitude for FAB-series bombs
- [ ] Deliver RBK cluster munitions against an area target

---

## Ground Brief

### Two Modes, Two Situations

| Mode | Profile | When to Use |
|---|---|---|
| **CCIP** | Diving attack | Target is visually acquired, accurate placement needed |
| **CCRP** | Level flight | Target under cloud/smoke, stand-off delivery, area bombing |

CCIP is more accurate but exposes you to ground fire during the dive. CCRP allows delivery from level flight and longer stand-off but is less accurate due to INS drift.

### Bomb Arming

FAB bombs use pyrotechnic fuzes. There is a **minimum arming distance** before the fuze activates.

| Bomb | Min Safe Release Alt |
|---|---|
| FAB-100 | 200 m AGL |
| FAB-250 | 400 m AGL |
| FAB-500 | 600 m AGL |
| RBK cluster | 300 m AGL (for submunition scatter) |

> **Warning:** Releasing below minimum altitude risks **CFIT** (Controlled Flight Into Terrain) — you will fly through your own frag pattern. DCS will simulate aircraft damage from your own munitions.

---

## Pre-Mission Setup

- [ ] Place 1 area target (vehicle park or building complex) and 1 point target (single building)
- [ ] Weather: Day VMC
- [ ] **Loadout:**
  - 4× FAB-250 (inner and outer wing pylons)
  - 2× RBK-250 (centerline and wing stations)
- [ ] Fuel: 60%
- [ ] Note target elevation for CCRP altitude calculations

---

## Part 1 — CCIP Delivery (Dive)

CCIP uses the aircraft's navigation computer and laser rangefinder to project a continuously updated impact point (the "pipper") onto the HUD. Place the pipper on the target and release.

### Switchology
1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Mode** — A-G (`7`)
3. - [ ] **Select** — FAB-250 pylon
4. - [ ] **Laser** — ON (`RShift + O`) — improves pipper accuracy
5. - [ ] Confirm CCIP pipper on HUD

### Attack Procedure

**Entry:** 4,000 m MSL, 550 km/h. Target at 12 o'clock, 5–7 km.

1. - [ ] Roll in: push over to **25–35° dive**
2. - [ ] Slew Shkval toward target — laser ranging updates pipper
3. - [ ] Track: place CCIP pipper on target, let it stabilize
4. - [ ] At **2,000–2,500 m slant range** (or pipper on target at appropriate altitude):
   - [ ] **Release** (`Space`) — single bomb
5. - [ ] **Immediate pull-off**: > 4 G pull, minimum **800 m AGL** (FAB-250 frag envelope)
6. - [ ] Egress

### CCIP Dive Parameters

| Parameter | Standard |
|---|---|
| Entry altitude | 3,500–4,500 m MSL |
| Dive angle | 25–35° |
| Airspeed at release | 500–600 km/h |
| Release slant range | 1,500–2,500 m |
| Min pull-off altitude | 800 m AGL (FAB-250) |

**Instructor Note:** The most common CCIP failure is releasing too early (pipper still short of target) or too late (too low for safe escape). Brief the student: "When the pipper is on the target, release — then pull."

---

## Part 2 — CCRP Delivery (Level)

CCRP uses the Shkval to designate a ground point. The aircraft's computer then calculates the exact moment to release the bomb during a level fly-over, accounting for bomb ballistics.

### Switchology
1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Mode** — A-G (`7`)
3. - [ ] **Select** — FAB-250 pylon
4. - [ ] **Laser** — ON (`RShift + O`)
5. - [ ] Confirm CCRP mode is active (vertical steering line appears on HUD)

### Target Designation
1. - [ ] At 8–10 km from target, slew Shkval onto target point
2. - [ ] Zoom in (numpad `*`) to confirm target identification
3. - [ ] **Lock ground point** (`Enter`) — Shkval stabilizes on terrain point
4. - [ ] HUD shows vertical steering line and range-to-release cue

### Attack Procedure

1. - [ ] Establish level flight at **2,500–3,500 m MSL**, 550 km/h
2. - [ ] Fly to align with the vertical steering line (fly toward the line until centered)
3. - [ ] When aligned — hold **Weapon Release** (`Space`) continuously
4. - [ ] Do **not** release and re-press — hold the button until the bomb releases automatically
5. - [ ] The computer releases at the calculated release point — you will hear/feel the release
6. - [ ] Continue wings-level for 3–4 seconds after release (improves tracking accuracy)
7. - [ ] Master Arm — SAFE after delivery

### CCRP Key Numbers

| Parameter | Value |
|---|---|
| Designation range | 8–15 km |
| Delivery altitude | 2,000–5,000 m MSL |
| Airspeed | 500–600 km/h |
| Expected CEP | 30–100 m |

**Instructor Note:** Students often release and immediately maneuver. The CCRP computer needs a consistent flight path during the release window. Brief: "Set it up, hold the button, fly straight, let the jet do the work."

> **Realism Note:** CCRP in the Su-25T is notably less precise than Western equivalents. There is no GPS or inertial navigation update mechanism. Drift accumulates with distance. For accurate CCRP, designate within 10 km of the target.

---

## Part 3 — RBK Cluster Bombs

The RBK-250 releases hundreds of PTAB submunitions over an area. Devastating against massed armor or vehicle parks. Ineffective against hardened single points.

| Parameter | Value |
|---|---|
| Weight | 250 kg |
| Submunitions | PTAB anti-tank bomblets |
| Pattern | 100–200 m wide |
| Min safe alt | 300 m AGL (submunition scatter) |

### Employment
- Same switchology as FAB bombs
- **CCIP** (preferred for area targets): dive at 20–25°, release at 1,500–2,000 m range
- **CCRP:** works but the area pattern makes precision less important
- **Do not use against single point targets** — submunitions scatter; use FAB or guided weapons instead

### Cluster Pattern Visualization

```
  Release point
       ↓
   ● ●   ● ●
  ●   ●●●   ●
 ●  ●●●●●●  ●       ← ~100–200 m scatter pattern
  ●   ●●●   ●
   ● ●   ● ●
       ↑
   Center of impact
```

**Instructor Note:** Students sometimes use cluster bombs against single vehicles expecting concentrated effect. Explain: "If it's one tank, use the Vikhr. If it's a tank park with 15 vehicles, use the RBK."

---

## Completion Standards

| Standard | Requirement |
|---|---|
| CCIP bomb delivery | Impact within 50 m of target on ≥ 2 of 3 passes |
| CCIP pull-off alt | Never below 800 m AGL (FAB-250) |
| CCRP designation | Shkval locked on target before attack run |
| CCRP delivery | Bomb impacts within 100 m of designated point |
| Weapon release | Hold button until auto-release in CCRP mode |
| RBK delivery | Area target substantially engaged (≥ 50% coverage) |

---

## Common Errors

| Error | Correction |
|---|---|
| CCIP pipper not settling | Slew Shkval onto target earlier — laser ranging needs time to stabilize |
| Releasing too low (CCIP) | Start pull at 1,000 m AGL — bomb was already away; do not wait to observe |
| CCRP — releasing and re-pressing | Hold the button continuously from alignment through release |
| CCRP — maneuvering after designation | Fly straight — the Shkval loses ground-lock during bank > 30° |
| Using cluster bombs on single vehicles | Wrong weapon for the job — use guided munitions |
| Not accounting for bomb arming altitude | Brief the limits before every pass |

---

[← Event 2: Guns & Rockets](event-2-guns-rockets.md) | [→ Event 4: Vikhr](event-4-vikhr.md)

---

*Based on Eagle Dynamics DCS World documentation. For simulation use only.*
