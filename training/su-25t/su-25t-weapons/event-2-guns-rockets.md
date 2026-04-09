# Event 2 — Guns & Rockets

> **Course:** Su-25T Weapons Employment | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Gun Employment (GSh-30-2)](#part-1--gun-employment-gsh-30-2)
5. [Part 2 — Rocket Employment (S-8)](#part-2--rocket-employment-s-8)
6. [Part 3 — Rocket Employment (S-13 & S-25)](#part-3--rocket-employment-s-13--s-25)
7. [Completion Standards](#completion-standards)
8. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Employ the GSh-30-2 gun against a stationary vehicle target from a diving attack, achieving at least one hit per pass
- [ ] Select and fire S-8 rockets with Laser Ranging active, impacting within 50 m of the target
- [ ] Demonstrate correct dive angle and pull-off technique for rocket delivery
- [ ] Execute a safe escape maneuver after each attack run

---

## Ground Brief

### Unguided Weapons Philosophy
Unguided weapons require the pilot to position the aircraft precisely before release. Unlike guided munitions, there is no correction after leaving the aircraft. The three variables you control are:

1. **Dive angle** — steeper is more accurate; shallower trades accuracy for range
2. **Airspeed** — too fast increases dispersion; too slow reduces time on target
3. **Range** — use the Laser Rangefinder to confirm, not guess

### Attack Profile: The Diving Attack
For all unguided weapons in this course, you will use the standard dive delivery:

```
       Entry: 3,000–4,000 m MSL, 500 km/h
              ↓
       Push over to dive angle
              ↓
    [Laser ON] [Pipper on target]
              ↓
         Release / Fire
              ↓
    Immediate pull-off (> 4 G)
              ↓
       Egress: Turn off threat axis
```

**Minimum pull-off altitudes:**
| Weapon | Min Release Alt |
|---|---|
| Gun | 500 m AGL |
| S-8 rockets | 500 m AGL |
| S-13 rockets | 600 m AGL |
| S-25 rocket | 800 m AGL |

> **Warning:** The Su-25T is not fast. A shallow dive at 500 km/h covers ground quickly. Do not delay pull-off — the aircraft has poor zoom climb energy at low altitude.

---

## Pre-Mission Setup

- [ ] Place 4–6 stationary vehicle targets (T-72 or similar) on the range — spread 200 m apart
- [ ] Weather: Day VMC, calm
- [ ] **Loadout:**
  - 2× B-8M1 pods (S-8 rockets) — inner wing pylons
  - 2× B-13L pods (S-13 rockets) — outer wing pylons
  - 1× S-25 single rocket — centerline
  - Gun: 250 rounds (always loaded)
- [ ] Fuel: 60%
- [ ] Altitude for work: Entry at 3,500 m MSL; target elevation should be noted

---

## Part 1 — Gun Employment (GSh-30-2)

### Switchology
1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Mode** — A-G (`7`)
3. - [ ] **Weapon** — GUN (`C`)
4. - [ ] **Laser** — ON (`RShift + O`) — improves ranging and pipper accuracy
5. - [ ] **HUD** — confirm gun cross/pipper is displayed

### Attack Procedure

**Set-up:** Enter the target area at 3,500 m MSL, 500 km/h. Position to place target at 12 o'clock, ~5 km.

1. - [ ] Push over: aim ~20° nose-low dive
2. - [ ] Slew Shkval briefly to target area — not required for gun but helps range data
3. - [ ] Place the gun pipper on the target vehicle
4. - [ ] At 1,200–1,500 m slant range — fire: **2–3 second burst** (`Space`)
5. - [ ] At 600 m AGL minimum — **pull off**: > 4 G pull, wings level or slight bank away from target
6. - [ ] **Master Arm** — SAFE (`O`) after egress

### Gun Technique Notes
- **Burst discipline:** 250 rounds runs out very quickly at 3,000 rpm. Use 1–2 second bursts, no more than 3 per pass.
- **Vibration:** The GSh-30-2 vibrates the airframe heavily. If firing while trying to read instruments, expect difficulty.
- **Convergence:** The gun is fixed forward. There is no convergence adjustment — just dive angle and pipper placement.

> **Realism Note:** The real GSh-30-2 has a selectable rate of fire: 3,000 rpm (high) and 300 rpm (low). DCS models the high rate by default. In real ops, low ROF is used for precise ground attack to avoid burning through ammo.

---

## Part 2 — Rocket Employment (S-8)

The S-8 is an area-suppression weapon. Fire entire pods against vehicle concentrations, troop positions, or lightly armored targets.

### Switchology
1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Mode** — A-G (`7`)
3. - [ ] **Select** — S-8 pylon (weapons select page)
4. - [ ] **Laser** — ON (`RShift + O`) — **MANDATORY for accurate CCIP**
5. - [ ] Confirm CCIP pipper appears on HUD (moves with range)

### Attack Procedure

1. - [ ] Enter at 3,000 m MSL, 500 km/h
2. - [ ] Push over to **15–20° dive**
3. - [ ] Slew Shkval to target — let laser range update
4. - [ ] Place CCIP pipper on target
5. - [ ] At 1,500–2,000 m slant range — **fire** (`Space`): hold for 1–2 seconds (salvo ~5–10 rockets)
6. - [ ] At 600 m AGL — **hard pull-off**, exit threat axis

### S-8 Range and Accuracy Table

| Dive Angle | Release Range | Expected CEP |
|---|---|---|
| 10° | 1,800 m | ~80 m |
| 20° | 1,500 m | ~40 m |
| 30° | 1,200 m | ~20 m |

**Instructor Note:** Students who do not turn on the laser will see the pipper fixed at a default depression angle. The rockets will always impact at the same ground range regardless of target position — usually hundreds of meters short or long. Confirm laser ON before the run.

---

## Part 3 — Rocket Employment (S-13 & S-25)

### S-13 (122mm — Light Armor & Bunkers)

Same technique as S-8 but slightly longer minimum release range due to larger warhead.

| Parameter | Value |
|---|---|
| Pod size | 5 rounds (B-13L) |
| Effective range | 500 m – 4 km |
| Min pull-off alt | 600 m AGL |
| Best target | Light armor, field bunkers, SAM launchers |

- **Dive angle:** 20–30°
- **Salvo:** 2–3 round burst for accuracy; full pod for saturation

### S-25 (340mm — Single Heavy Rocket)

The S-25 is a massive unguided rocket. Single round. Extremely loud. Large warhead.

| Parameter | Value |
|---|---|
| Quantity | 1 per pylon |
| Effective range | 500 m – 3 km |
| Min pull-off alt | 800 m AGL |
| Best target | Fixed structures, gun emplacements, hardened positions |

- **Dive angle:** 20–35°
- **Technique:** You only get one shot per pylon — make it count. Ensure pipper is settled before firing.

#### Switchology (S-25)
1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Mode** — A-G (`7`)
3. - [ ] **Select** — S-25 pylon
4. - [ ] **Laser** — ON (`RShift + O`)
5. - [ ] Attack as per S-8 procedure

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Gun employment | At least 1 confirmed hit per pass (2 passes minimum) |
| Laser active | Laser ON for all rocket passes — no "cold laser" failures |
| CCIP accuracy (S-8) | ≥ 1 pass with rockets impacting within 50 m of target |
| S-25 delivery | Impacts within 100 m of target |
| Pull-off altitude | Never below minimum pull-off altitude |
| Master Arm discipline | SAFE after every pass |

---

## Common Errors

| Error | Correction |
|---|---|
| Laser not ON during rocket runs | Brief at every run: Laser is first thing ON after weapon select |
| Releasing too far (pipper short) | Reduce range — release at 1,200–1,500 m not 2,500 m |
| Shallow dive (<10°) | At least 15° dive for S-8; rockets will scatter badly at shallow angles |
| Late pull-off | Brief the minimum altitude; set 600 m AGL as a hard deck |
| Full pod fire on every pass | Practice burst control — partial salvos build consistency |
| Master Arm left ON after pass | Build the habit: pickle off, safety on, egress |

---

[← Event 1: Academics](event-1-academics.md) | [→ Event 3: Gravity Bombs](event-3-bombs.md)

---

*Based on Eagle Dynamics DCS World documentation. For simulation use only.*
