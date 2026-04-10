# Event 7 — Advanced Systems & Self-Defense

> **Course:** A-10C Weapons Employment Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — A-10C II Advanced Weapons *(A-10C II Only)*](#part-1--a-10c-ii-advanced-weapons-a-10c-ii-only)
4. [Part 2 — AIM-9M Self-Defense](#part-2--aim-9m-self-defense)
5. [Part 3 — Electronic Warfare & Defensive Systems](#part-3--electronic-warfare--defensive-systems)
6. [Completion Standards](#completion-standards)
7. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:

**A-10C II Students (Parts 1–3):**
- [ ] Configure and employ APKWS (Advanced Precision Kill Weapon System) in CCIP and laser-guided modes
- [ ] Configure and employ GBU-39 Small Diameter Bomb (SDB) for GPS stand-off employment
- [ ] Configure and employ GBU-54 Laser JDAM (LJDAM) against moving targets
- [ ] Use the HMCS (Helmet-Mounted Cueing System) to designate targets and cue weapons

**All Students (Parts 2–3):**
- [ ] Identify AIM-9M seeker parameters and perform a valid self-defense shot
- [ ] Operate the CMSP (Countermeasures Set Processor) in MAN, SEMI, and AUTO modes
- [ ] Interpret ALR-69 RWR symbology and react to missile launch warnings
- [ ] Execute appropriate defensive maneuvers for radar SAM, IR SAM, and AAA threats
- [ ] Employ chaff and flare programs using the ALE-47 dispenser

---

## Ground Brief

### A-10C vs A-10C II Advanced Systems Summary

| System | A-10C | A-10C II |
|---|---|---|
| APKWS laser rockets | ✗ | ✓ |
| GBU-39 SDB | ✗ | ✓ |
| GBU-54 LJDAM | ✗ | ✓ |
| HMCS | ✗ | ✓ |
| AIM-9M | ✓ (wing only) | ✓ |
| CMSP / ALE-47 | ✓ | ✓ |
| ALR-69 RWR | ✓ | ✓ |
| ECM Pod (ALQ-184) | ✓ | ✓ |

> **A-10C students** skip Part 1 and proceed directly to Part 2.

---

## Part 1 — A-10C II Advanced Weapons *(A-10C II Only)*

### Section A — APKWS (Advanced Precision Kill Weapon System)

APKWS is a laser-guidance kit that converts standard Hydra 70 (2.75-inch) rockets into precision-guided munitions. Each rocket gains a laser seeker mid-body and guidance fins, reducing CEP from ~30 m (unguided) to ~1 m (guided).

#### APKWS Configuration

| Step | Action |
|---|---|
| 1 | DSMS: select APKWS station |
| 2 | PROF → delivery mode: **CCIP** (standard) |
| 3 | Laser code: CDU LSR page → verify code (e.g., 1688) |
| 4 | Qty: **SGL** (single shot) or **PAIR** |
| 5 | LASER ARM → **ARM** |
| 6 | MASTER ARM → **ARM** |

#### APKWS CCIP + Laser Procedure

| Step | Action |
|---|---|
| 1 | TGP: acquire target → POINT track → SPI |
| 2 | CCIP dive: 15–20° dive, 300–350 KIAS |
| 3 | Slew CCIP pipper onto target |
| 4 | **TMS UP long → laser ON** (illuminate target with TGP) |
| 5 | When pipper on target: **release** |
| 6 | Maintain TGP LOS until impact |
| 7 | **TMS UP → laser OFF** after impact |

| APKWS Parameter | Value |
|---|---|
| Entry Altitude | 8,000–12,000 ft AGL |
| Dive Angle | 15–20° |
| Min Release Altitude | 4,000 ft AGL |
| CEP | ~1 m |
| Time of Flight | 4–8 sec (short — lase from release) |
| Best Against | Vehicles, radar antennas, radar dishes |

---

### Section B — GBU-39 Small Diameter Bomb (SDB)

GBU-39 is a 250-lb GPS/INS guided small diameter bomb carried in packs of four per pylon (via BRU-61/A). It provides GPS-precision at extended stand-off range with minimal drag penalty.

#### SDB Quick Reference

| Item | Value |
|---|---|
| Weight | 285 lb (guidance + body) |
| CEP | < 5 m (GPS) |
| Stand-off Range | Up to 40 nm (from high altitude) |
| Warhead | 206 lb penetrating WH |
| Carriage | 4 per BRU-61/A cluster rack |
| Fuze | Hard-target smart fuze (penetrates before detonating) |

#### SDB Configuration and Employment

| Step | Action |
|---|---|
| 1 | DSMS: select SDB station → PROF |
| 2 | Delivery mode: **CCRP** |
| 3 | Mode: **PP** (GPS survey coordinates) or **TOO** (TGP) |
| 4 | Fuze: **AUTO** (smart fuze, default) |
| 5 | Qty: SGL or 2 or 4 per pass |
| 6 | MASTER ARM → ARM at IP |
| 7 | Fly CCRP steering; hold pickle → auto-release |

> **Note:** SDB employment is essentially identical to JDAM in the cockpit — TOO or PP, CCRP, hold pickle. The difference is the smaller warhead, much larger quantity per station, and longer stand-off range. Target elevation accuracy is equally critical.

---

### Section C — GBU-54 Laser JDAM (LJDAM)

GBU-54 combines GPS/INS guidance (JDAM) with a laser seeker (LGB). It can navigate to GPS coordinates initially, then switch to laser terminal guidance — enabling employment against **moving targets**.

#### LJDAM Modes

| Mode | Guidance Used |
|---|---|
| **GPS terminal** | Standard JDAM — homes to coordinates. Target must be stationary. |
| **Laser terminal** | GPS/INS to the vicinity → laser seeker activates → homes to laser spot. Target may be moving. |
| **Dual mode** | Both active simultaneously — laser takes precedence if acquired. |

#### LJDAM vs Moving Target Procedure

| Step | Action |
|---|---|
| 1 | TGP: POINT track on moving target |
| 2 | DSMS: GBU-54, CCRP, **Laser mode** selected |
| 3 | Verify laser code matches weapon kit |
| 4 | SPI: set from TGP track (coordinates will be approximate — laser terminal guidance refines it) |
| 5 | MASTER ARM → ARM; LASER ARM → ARM |
| 6 | Fly CCRP steering; hold pickle → auto-release |
| 7 | **Maintain TGP POINT track on the moving target** |
| 8 | **TMS UP long → laser ON** — lase moving target through impact |
| 9 | Bomb navigates to initial GPS fix, then laser seeker acquires the illuminated target and terminally guides |

> **Key Advantage:** Even if the target moves 100 meters after release, as long as the TGP stays locked and the laser is on, the LJDAM will hit.

---

### Section D — HMCS (Helmet-Mounted Cueing System) *(A-10C II Only)*

The HMCS allows the pilot to designate targets simply by looking at them, without slewing a TGP or MFCD cursor. This dramatically speeds up target acquisition and designation for time-sensitive targets.

#### HMCS Symbology (Key Elements)

| Symbol | Meaning |
|---|---|
| **Reticle (center dot)** | Where you are looking (HMCS-computed LOS) |
| **Altitude tape** | Baro altitude left side |
| **Airspeed tape** | Right side |
| **FPM (Flight Path Marker)** | Where the aircraft is going |
| **Target box** | Target designation when locked |

#### HMCS Designation Workflow

| Step | Action |
|---|---|
| 1 | Ensure HMCS is powered (AHCP → HMCS → ON) |
| 2 | **Look at the target** with your head |
| 3 | Press **Sensor Select Switch (SSS) forward long** → HMCS designation sent to SPI |
| 4 | HMCS LOS coordinates are now the SPI |
| 5 | TGP slaves to SPI (if TGP is in SLAVE mode) → TGP centers on the HMCS-designated target |
| 6 | Confirm TGP POINT track on the correct target |
| 7 | Normal weapon delivery from this point |

#### HMCS with AIM-9M

| Step | Action |
|---|---|
| 1 | AIM-9M selected on DSMS |
| 2 | HMCS provides seeker cueing — the AIM-9M seeker slews to HMCS LOS |
| 3 | **Look at the target** — seeker slews to match your line-of-sight |
| 4 | AIM-9M growl tone confirms IR acquisition |
| 5 | Press and release pickle — **missile away** |

> **Caution:** Confirm the seeker is locked on the correct heat source before firing. Sun, flares, and hot terrain can seduce the AIM-9M seeker.

---

## Part 2 — AIM-9M Self-Defense

### AIM-9M Overview

The AIM-9M Sidewinder is carried on the A-10C's outboard wing stations (1, 11) for self-defense. It is an IR (heat-seeking) air-to-air missile, not intended for offensive combat — it provides a limited last-ditch capability against threat aircraft that have achieved visual-range intercept.

| Parameter | Value |
|---|---|
| Warhead | 20.8 lb fragmentation |
| Seeker | IR; all-aspect (limited rear-aspect advantage) |
| Range | ~0.6–3 nm (training estimate) |
| Coolant | Argon; limited to ~90 min cooled operation |

### Self-Defense Decision Matrix

| Situation | Action |
|---|---|
| Threat aircraft > 5 nm, not maneuvering toward | Continue mission; maneuver for range |
| Threat aircraft 3–5 nm, maneuvering | Defensive maneuver, ECM, chaff/flare; consider AIM-9 |
| Threat aircraft < 3 nm, weapons away | AIM-9 employment; maximum jink; terrain masking |
| Threat aircraft overshooting | High-G break turn; chaff/flare; possible AIM-9 snap shot |

### AIM-9M Configuration

| Step | Action |
|---|---|
| 1 | DSMS: select AIM-9M station (outboard) |
| 2 | Weapons mode: **AAM** (Air-to-Air Missile) |
| 3 | MASTER ARM → **ARM** |
| 4 | Seeker power: apply via cockpit switch — allow **60 seconds** for argon cooldown |
| 5 | Seeker tone: confirm **audio growl** in headset (growl = IR acquisition) |
| 6 | Uncage (if applicable): allow seeker to search freely |

### Engagement Procedure

| Step | Action |
|---|---|
| 1 | ID threat aircraft visually or via TGP |
| 2 | Maneuver into a valid AIM-9 shooting position (nose ~30° of threat) |
| 3 | Listen for **strong, steady growl tone** |
| 4 | Confirm the seeker is not locked on sun, flares, or other IR sources |
| 5 | **Pickle** → missile away |
| 6 | Call: **"Fox 2"** (IR missile fired) |
| 7 | Immediately break off to avoid overflight of threat |
| 8 | Assess result; consider follow-on shots |

> **Training Note:** AIM-9M employment in DCS is primarily for emergency self-defense awareness. A-10C pilots are CAS aircraft — their primary survival tool is threat avoidance, not air combat. If a threat aircraft enters the engagement envelope, the A-10C should use terrain, speed, chaff/flare, and ECM first, and fire AIM-9M only as a last resort.

---

## Part 3 — Electronic Warfare & Defensive Systems

### CMSP — Countermeasures Set Processor

The CMSP is the master controller for the A-10C's defensive suite: chaff, flares, ECM pods, and RWR.

#### CMSP Modes

| Mode | Function |
|---|---|
| **OFF** | No chaff or flares dispensed |
| **MAN (Manual)** | Pilot manually commands chaff/flare using the dispenser control button |
| **SEMI** | CMSP dispenses chaff/flare when threat is detected; pilot approves each burst |
| **AUTO** | CMSP automatically dispenses optimal chaff/flare program when threat is detected |

#### CMSP Control Panel Setup

| Step | Action |
|---|---|
| 1 | CMSP power → **ON** |
| 2 | Select mode: **SEMI** for tactical flight (recommended training default) |
| 3 | Verify ALE-47 chaff and flare counts (shown on CMSP MFD page) |
| 4 | Set chaff program: e.g., **Program 1** (radar threat) |
| 5 | Set flare program: e.g., **Program 2** (IR threat) |

### ALE-47 Chaff and Flare Programs

| Program | Contents | Against |
|---|---|---|
| **Chaff Program 1** | 2 bursts × 2 chaff | Radar-guided missiles (SA-6, SA-10, etc.) |
| **Flare Program 2** | 2 bursts × 2 flares | IR-guided missiles (SA-7, SA-14, AIM-9) |
| **Mixed Program 3** | 1 chaff + 1 flare | When threat type unknown |

### Manual Chaff / Flare Technique

| Step | Action |
|---|---|
| 1 | CMSP → **MAN** mode |
| 2 | Select dispenser type: chaff (forward switch) or flare (aft) |
| 3 | Press **dispenser button** (typically boat switch aft in DCS) |
| 4 | Observe dispensed: CMSP count decreases |

> **Inventory management:** Standard combat load is typically 120 flares + 240 chaff. Do not expend all reserves early in the mission. Reserve at least 20% for egress.

### ALR-69 RWR Symbology

| Symbol | Meaning |
|---|---|
| **F-16, F-15, MiG...** | Airborne threat; text indicates platform type |
| **SA-2, SA-6, SA-10...** | SAM system; number indicates specific system |
| **AAA** | Anti-aircraft artillery detection |
| **Inner ring** | Threat within lethal range |
| **Outer ring** | Threat detected; not yet lethal |
| **Flashing symbol** | Missile launch detected — IMMEDIATE action required |

### RWR Threat Reaction Doctrine

| Threat | Detection Cue | Immediate Action |
|---|---|---|
| **Radar SAM (SA-6, SA-10)** | RWR tone + symbol | Notch (fly 90° to radar); chaff; ECM pod ON |
| **IR SAM (SA-7, SA-14)** | Optically detected or visual plume | Break turn; flare; terrain masking |
| **AAA (visually detected)** | Tracers, puffs | Jink pattern; altitude change; egress |
| **Missile launch (flashing)** | Flashing RWR + audio | Maximum-G break toward or into terrain; chaff/flare; notch |
| **Radar lock (steady tone)** | Steady lock tone | Notch radar; chaff; consider immediate egress |

### Defensive Maneuvers

#### Notch

- Fly **90° left or right of the radar beam** heading.
- This places the aircraft in the radar's "notch" — the velocity gate can't track slow or zero-radial-velocity targets.
- Most effective against **pulse-Doppler radar** systems.

```
            [Threat radar]
                  |
   [A-10C] ----90°-- (notch axis)
```

#### Break Turn

- Maximum-G turn toward the threat (or a terrain feature for masking).
- Forces a missile to pull high Gs to track — depletes kinetic energy.
- Combine with flares (IR threat) or chaff (radar threat).

#### Terrain Masking

- Fly **behind a ridge, hill, or building** to break radar LOS.
- Defeats radar-guided missiles that lose track.
- Most effective terrain-masking technique for the A-10C — use aggressively.

#### Jink Pattern

- Continuous, unpredictable small heading and altitude changes.
- Defeats AAA directors that predict your flight path.
- **Not a substitute** for breaking track of guided missiles.

### ECM Pod (ALQ-184)

| Feature | Description |
|---|---|
| **Type** | Active electronic jamming — noise/deceptive jamming |
| **Effective against** | Radar-guided missiles and fire-control radars |
| **Not effective against** | IR-guided missiles, unguided AAA, visual threats |
| **Activation** | CMSP → ECM ON; jammer requires ~30 sec warm-up |
| **Limitations** | Reduces effectiveness of RWR (jamming masks return signal); not a shield |

#### ECM Pod Employment

| Step | Action |
|---|---|
| 1 | CMSP → verify ALQ-184 is on the station |
| 2 | CMSP ECM switch → **ON** |
| 3 | Allow ~30 sec warm-up |
| 4 | ECM active: "Jamming" annunciation |
| 5 | Combine with chaff and maneuvering — ECM is not standalone protection |
| 6 | Turn ECM **OFF** when no longer needed (reduces RWR sensitivity while active) |

### Event Sequence

**A-10C II Students:**
- [ ] **Part 1A:** APKWS employment — 2 passes
- [ ] **Part 1B:** GBU-39 SDB — 1 PP pass
- [ ] **Part 1C:** GBU-54 LJDAM — 1 pass against simulated moving target
- [ ] **Part 1D:** HMCS designation workflow — 3 acquisitions

**All Students:**
- [ ] **Part 2:** AIM-9M seeker mechanics — 1 simulated engagement drill (no live fire)
- [ ] **Part 3A:** CMSP setup — configure for both MAN and SEMI modes
- [ ] **Part 3B:** RWR recognition drill — identify 5 symbols from instructor flashcards
- [ ] **Part 3C:** Defensive maneuver demonstration — notch, break, terrain mask
- [ ] **Part 3D:** Full defensive scenario — instructor simulates SAM shot; student reacts

---

## Completion Standards

| Item | Standard |
|---|---|
| **APKWS** *(A-10C II)* | Impact within 5 m of designated target; laser ON before impact |
| **GBU-39 SDB** *(A-10C II)* | Impact within 15 m of designated coordinates; GPS verified |
| **GBU-54 LJDAM** *(A-10C II)* | Laser maintained on moving target through impact; POINT track held |
| **HMCS designation** *(A-10C II)* | TGP slaves correctly to HMCS LOS; target correctly acquired |
| **AIM-9M seeker** | Student can identify growl tone and confirm correct IR acquisition |
| **CMSP mode selection** | Correct mode for tactical scenario; chaff/flare programs verified |
| **RWR identification** | ≥ 80% correct identification of 5 displayed symbols |
| **Defensive maneuver** | Notch within 90° ± 15°; break turn ≥ 4 G; terrain mask to LOS break |
| **Full defensive scenario** | CMSP operates; correct chaff or flare for threat; appropriate maneuver |
| **ECM pod** | Activated with correct warm-up; combined with maneuvering |

---

## Common Errors

| Error | Correction |
|---|---|
| **APKWS laser off before impact** | "APKWS time-of-flight is short — only seconds. Lase from the moment of release. If you pull the laser early, the rocket is dumb." |
| **GBU-54 LJDAM: TGP loses POINT track** | "LJDAM moving target employment requires you to keep the TGP locked on the target. If it transitions to AREA track, the laser misses. Confirm POINT track before and after release." |
| **HMCS designates wrong object** | "The HMCS has no target ID — it designates wherever you look. If you look at a tree instead of a tank, that's what you'll hit. Confirm TGP on correct target after designation." |
| **AIM-9M fired without growl tone** | "No growl = no lock = no hit. The tone tells you the seeker is seeing heat. Never fire cold." |
| **CMSP set to OFF** | "CMSP OFF means zero countermeasures — no chaff, no flares, even if you hit the dispense button. SEMI is the minimum safe setting for any tactical flight." |
| **Chaff against IR missile** | "Chaff is for radar. IR missiles don't care about chaff — they see heat. Know your threat type. Flares for IR; chaff for radar." |
| **Ignoring RWR** | "The RWR is a survival tool. If a symbol appears and you don't react, you've failed. Scan the RWR constantly in a threat environment." |
| **ECM pod left ON during egress** | "ECM reduces your own RWR sensitivity. When threats are gone, turn it off. Don't degrade your awareness unnecessarily." |

---

[← Event 6: JDAM & GPS Weapons](event-6-jdam.md) | [→ Event 8: Check Ride](event-8-check-ride.md)

---

*Based on T.O. 1A-10C-34-1-1, T.O. 1A-10C-1-1, and Eagle Dynamics DCS A-10C/II documentation. For simulation use only.*
