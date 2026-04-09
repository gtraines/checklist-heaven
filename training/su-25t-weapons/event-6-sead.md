# Event 6 — SEAD (Suppression of Enemy Air Defenses)

> **Course:** Su-25T Weapons Employment | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Fantasmagoria Pod Setup & Emitter Detection](#part-1--fantasmagoria-pod-setup--emitter-detection)
5. [Part 2 — Kh-25MPU Employment (Short/Medium Range)](#part-2--kh-25mpu-employment-shortmedium-range)
6. [Part 3 — Kh-58 Employment (Long Range)](#part-3--kh-58-employment-long-range)
7. [Part 4 — SEAD Tactical Considerations](#part-4--sead-tactical-considerations)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Mount and activate the Fantasmagoria pod for radar emitter detection
- [ ] Identify and classify radar emitters using the Fantasmagoria HUD display
- [ ] Execute a Kh-25MPU employment against a SHORAD radar target
- [ ] Execute a Kh-58 long-range launch against a search/fire-control radar
- [ ] Explain the limitations of SEAD against radar-silent air defense systems

---

## Ground Brief

### Why SEAD?

The Su-25T operates at low-to-medium altitude, directly in the engagement envelope of most SHORAD (Short-Range Air Defense) and medium-range SAM systems. Without SEAD, every attack run is potentially suicidal against a defended target.

SEAD does not destroy the air defense — it suppresses it. A destroyed radar means the SAM is temporarily blind. The window may be only minutes, but that is enough for your attack element to complete the mission.

### The SEAD Kill Chain

```
  1. DETECT:   Fantasmagoria pod detects radar emissions → HUD diamond
  2. ID:       Classify emitter type (SHORAD vs. search vs. tracking)
  3. TARGET:   Cursor select the emitter → weapon handoff
  4. LAUNCH:   Fire Kh-25MPU or Kh-58 depending on target type
  5. EGRESS:   Turn away; monitor for radar shut-down
```

### Weapon Selection for SEAD

| Threat | Weapon |
|---|---|
| SHORAD (Roland, Gepard, Osa, Tunguska) | Kh-25MPU |
| Medium SAM fire control (SA-6, SA-11) | Kh-58 |
| Long-range SAM search radar (SA-10, SA-3) | Kh-58 |

> **Realism Note:** In reality, SEAD against an SA-10 (S-300) system is an extremely dangerous and complex multi-ship, multi-weapon coordinated attack. DCS simplifies this. A single Kh-58 from medium altitude will not realistically disable a well-defended S-300 battery.

---

## Pre-Mission Setup

- [ ] Place 1× Roland SAM (short-range, active radar) at 15 km
- [ ] Place 1× SA-6 "Gainful" (medium-range) with radar active at 40 km
- [ ] Weather: Day VMC
- [ ] **Loadout:**
  - Centerline: Fantasmagoria pod (L-081)
  - 2× Kh-25MPU on inner wing pylons
  - 2× Kh-58 on outer wing pylons
- [ ] Fuel: 75%

> **Note:** The Fantasmagoria mounts **centerline only**. This means no Mercury LLTV and no MPS-410 jammer on this mission.

---

## Part 1 — Fantasmagoria Pod Setup & Emitter Detection

### Activation

1. - [ ] **Fantasmagoria Pod** — ensure mounted (set in mission editor loadout)
2. - [ ] On SEAD page — **activate pod** (DCS usually activates automatically in A-G mode)
3. - [ ] Look for **diamond symbols** on HUD — each diamond is a detected radar emitter

### Reading the HUD

| Symbol | Meaning |
|---|---|
| Diamond (◇) | Radar emitter detected — direction indicated |
| Filled diamond (◆) | Designated/selected emitter (weapon handoff active) |
| Diamond with line | Direction and approximate bearing to emitter |

**Distance:** The HUD diamonds indicate direction but not precise distance. Use the F10 map for range estimation during training.

### Emitter Selection

1. - [ ] Identify the target emitter diamond on HUD
2. - [ ] Slew cursor (available in some DCS modes) or maneuver toward the emitter
3. - [ ] **Designate** the target emitter — diamond fills (◆)
4. - [ ] Weapon system receives emitter data

**Instructor Note:** Students often see multiple emitter diamonds and become confused. Brief: "One target at a time. Select the most immediate threat — SHORAD first, long-range second."

---

## Part 2 — Kh-25MPU Employment (Short/Medium Range)

### Weapon Specifications

| Parameter | Value |
|---|---|
| Target | SHORAD radars (Roland, Gepard, Osa, Tunguska) |
| Range | 20–40 km |
| Speed | Subsonic |
| Guidance | Passive anti-radiation (homes on radar emission) |
| Memory | Limited — effectively ballistic if radar shuts off |

### Switchology

1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Mode** — A-G (`7`)
3. - [ ] **Select** — Kh-25MPU pylon
4. - [ ] Confirm Fantasmagoria is active and emitter is designated (◆)
5. - [ ] Wait for **LA** cue
6. - [ ] **Launch** (`Space`)
7. - [ ] **Monitor:** if radar shuts down before impact, missile will likely miss

### Attack Profile

**Entry:** 2,000–3,000 m MSL, 500 km/h, approaching Roland at 25 km.

1. - [ ] Detect Roland on Fantasmagoria (diamond appears at bearing to target)
2. - [ ] Designate Roland emitter
3. - [ ] Close to 25–30 km range
4. - [ ] Confirm LA — fire Kh-25MPU
5. - [ ] **Turn away immediately** — you are now within Roland's engagement range
6. - [ ] Monitor: if Roland radar stays on, missile homes in
7. - [ ] If Roland shuts down: missile will likely go ballistic and miss

**Instructor Note:** The "shoot and scoot" technique is essential for the Kh-25MPU. At 25 km, the Roland can engage you. Launch and turn cold (away from threat) immediately.

> **Realism Note:** In DCS, the Kh-25MPU occasionally still hits a shut-down radar due to simulation logic. In reality, if the emitter goes silent before terminal homing, the missile goes unguided. Do not rely on this in tactical planning.

---

## Part 3 — Kh-58 Employment (Long Range)

The Kh-58 is the Su-25T's heavy SEAD weapon. It is supersonic, long-ranged, and has INS memory to fly toward a shut-down radar's last known location.

### Weapon Specifications

| Parameter | Value |
|---|---|
| Target | SA-6, SA-3, SA-10 fire control/search radars |
| Range | Up to 120 km (high altitude launch) |
| Speed | Mach 3+ |
| Guidance | Passive anti-radiation + INS midcourse |
| Memory | INS — flies to last known position if radar shuts off |

### Kh-58 vs. Kh-25MPU: Key Advantage

The Kh-58's INS memory means: even if the radar operator shuts down the radar, the Kh-58 will continue flying to where the radar was. It may still hit the radar vehicle.

### Switchology

Same as Kh-25MPU with one critical addition:

1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Mode** — A-G (`7`)
3. - [ ] **Select** — Kh-58 pylon
4. - [ ] Designate SA-6 radar emitter with Fantasmagoria
5. - [ ] Wait for LA
6. - [ ] **Altitude:** Climb to at least 3,000 m MSL before launch — maximizes range
7. - [ ] **Launch** (`Space`)
8. - [ ] Turn cold — **true fire and forget**

### Kh-58 Range Table

| Launch Altitude | Effective Range |
|---|---|
| 500 m MSL | ~30–40 km |
| 2,000 m MSL | ~60–80 km |
| 5,000 m MSL | ~100–120 km |

**Launch from altitude for maximum range.** Flying at 500 m for SEAD wastes the Kh-58's primary advantage.

**Instructor Note:** Students often launch the Kh-58 from low altitude in the traffic pattern. They are throwing away 80 km of stand-off range. Brief: "Climb first, then launch from altitude."

---

## Part 4 — SEAD Tactical Considerations

### The Radar Shoot-Down Problem

SEAD is a cat-and-mouse game. The radar operator knows that an anti-radiation missile is in the air when their RWR spikes. They will shut down. The question is: did they shut down early enough?

**Tactics to improve SEAD effectiveness:**
1. **Suppress multiple threats simultaneously** — a two-ship with synchronized attacks forces the operator to choose which radar to shut off
2. **Use Kh-58 for high-value, long-range targets** — INS memory helps
3. **Follow up immediately** — the window after a successful radar kill is short; your strike package must be in the area

### Limitations of SEAD

| Limitation | Implication |
|---|---|
| Optical/passive SAMs (MANPADS, IR-guided) | Fantasmagoria cannot detect — SEAD is ineffective |
| Short-range visual SAMs (ZU-23, ZSU-23-4) | Anti-radiation missiles are overkill; need strafing runs |
| Radar-off SAMs | If they don't radiate, you cannot SEAD them |

**Instructor Note:** Students sometimes believe SEAD eliminates all air defenses. Debrief the specific limitation: "A threat that doesn't radiate is invisible to your pod. You still need flight leaders to mark MANPADS positions visually."

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Pod identification | Correctly identifies Fantasmagoria emitter diamonds on 3 of 3 displays |
| Emitter designation | Designates correct threat (SHORAD first) |
| Kh-25MPU employment | Radar destroyed or suppressed on ≥ 2 of 3 passes |
| Kh-58 employment | Launches from ≥ 3,000 m MSL; fire-and-forget correctly demonstrated |
| Radar-off scenario | Student correctly explains missile will likely miss if Kh-25MPU target shuts off |
| Self-protection | Turns cold after Kh-25MPU launch (within Roland engagement range) |

---

## Common Errors

| Error | Correction |
|---|---|
| Fantasmagoria not mounted | Pre-flight loadout check — centerline must be Fantasmagoria |
| Selecting wrong emitter | Brief priorities: SHORAD first (immediate threat), long-range second |
| Low-altitude Kh-58 launch | Emphasize: altitude = range; climb to 3,000+ m before Kh-58 launch |
| Not turning cold after Kh-25MPU | You are inside the Roland's engagement range — launch and immediately turn away |
| Thinking SEAD eliminates all threats | IR/passive threats are immune; debrief explicitly |

---

[← Event 5: Laser-Guided Missiles](event-5-laser-guided.md) | [→ Event 7: Check Ride](event-7-check-ride.md)

---

*Based on Eagle Dynamics DCS World documentation. For simulation use only.*
