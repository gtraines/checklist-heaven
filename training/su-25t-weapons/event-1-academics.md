# Event 1 — Weapons Systems Academics

> **Course:** Su-25T Weapons Employment | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Weapons Safety Rules](#weapons-safety-rules)
3. [Module 1 — Targeting Systems](#module-1--targeting-systems)
4. [Module 2 — Unguided Weapons Overview](#module-2--unguided-weapons-overview)
5. [Module 3 — Guided Weapons Overview](#module-3--guided-weapons-overview)
6. [Module 4 — SEAD Overview](#module-4--sead-overview)
7. [Weapons Modes Cheat Sheet](#weapons-modes-cheat-sheet)
8. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Describe the capabilities and limitations of the I-251 Shkval and Mercury LLTV targeting systems
- [ ] State the correct employment mode (CCIP/CCRP/Guided) for each weapon type
- [ ] Recite the three safety rules for weapons employment
- [ ] Explain how the Vikhr beam-riding missile differs from a laser-guided missile
- [ ] Describe the role of the Fantasmagoria pod in SEAD operations

---

## Weapons Safety Rules

These three rules apply to every weapons release in this course. Violation of any rule results in a **DOWN** grade.

> **Rule 1 — Positive Target ID (VID):** Do not release weapons until the target is positively identified as hostile using the Shkval. If you cannot see it clearly — do not shoot.
>
> **Rule 2 — Safe Escape:** Ensure sufficient altitude and airspeed to escape the weapon's effects before release. Do not fly through your own fragmentation.
>
> **Rule 3 — Master Arm Discipline:** Master Arm (`O`) is ON only during the attack run. Return to SAFE immediately after weapon release or abort.

---

## Module 1 — Targeting Systems

### I-251 "Shkval" EO System

The Shkval is the Su-25T's primary targeting system, mounted in the nose. It is your eyes for all weapons employment except unguided area attacks.

| Parameter | Value |
|---|---|
| Type | Electro-Optical (Daylight only) |
| Zoom levels | 23× (wide) and 8× (narrow) |
| Azimuth gimbal limit | ±35° |
| Elevation gimbal limit | +15° to −85° |
| Laser Rangefinder | Integrated |

**Key Procedures:**
- **Activate:** `O` (Shkval power)
- **Slew:** `;` (left), `'` (right), `p` (up), `/` (down) — or mapped axis
- **Zoom:** `*` (zoom in) / `/` (zoom out) on numpad
- **Gate size:** `RCtrl + [` / `RCtrl + ]` — match gate to target size (~10 m for a tank)
- **Lock:** `Enter`
- **Laser ON:** `RShift + O`

**⚠ Daytime Only:** The Shkval uses visible-light contrast. It cannot see in darkness, heavy overcast shadow, or through smoke. A locked target may break lock if obscured.

**Contrast Lock:** The automatic tracking system locks on a contrast boundary. It will track the target's edge, not its center. This is intentional — it works well against vehicles, buildings, and equipment. It may struggle against:
- Low-contrast targets (green vehicle on green grass)
- Targets obscured by dust, smoke, or shadows
- Moving targets that move faster than the slew limit

#### Instructor Note
Students commonly forget to adjust gate size before locking. A gate set too large will lock on terrain background, not the vehicle. A gate too small may fail to acquire. Teach: **"Gate fits the target — not the field."**

### "Mercury" (Merkury) LLTV Pod

The Mercury pod enables limited night operations by amplifying available ambient light.

| Parameter | Value |
|---|---|
| Type | Low-Light Television |
| Image | Green-scale, amplified |
| Effective ID range | ~3–5 km |
| Mounting station | Centerline (Station 6) only |

**Conflict:** Mounting Mercury means you **cannot** carry:
- Fantasmagoria SEAD pod
- MPS-410 Jammer pod

**Daytime:** Mercury is useless in daylight — the image washes out.

> **Realism Note:** In the real Su-25T, night operations were extremely rare and hazardous. In DCS, the Mercury effectively makes you a viable night attacker. This is a simulation simplification.

---

## Module 2 — Unguided Weapons Overview

### GSh-30-2 Gun

| Parameter | Value |
|---|---|
| Caliber | 30mm |
| Rounds | 250 |
| Rate of fire | ~3,000 rpm |
| Effective range | < 1,500 m |
| Employment | Shallow to medium dive (10–20°) |

- Weapon select key: `C` (gun)
- Laser ON improves range accuracy
- Sustained fire causes heavy airframe vibration — short bursts preferred

### Rockets

| Rocket | Caliber | Pod Size | Best Use |
|---|---|---|---|
| S-8 | 80mm | B-8M1 (×20) | Area suppression, light vehicles |
| S-13 | 122mm | B-13L (×5) | Light armor, bunkers |
| S-25 | 340mm | Single | Heavy blast, fixed structures |

- All rockets use CCIP mode
- **Laser ranging is mandatory** — without it, the pipper defaults to a fixed depression angle and misses by hundreds of meters
- Steeper dive angle = tighter dispersion pattern

### Bombs

| Bomb | Weight | Type | Notes |
|---|---|---|---|
| FAB-100 | 100 kg | General purpose HE | Light structures, personnel |
| FAB-250 | 250 kg | General purpose HE | Light armor, field positions |
| FAB-500 | 500 kg | General purpose HE | Heavy armor, hardened sites |
| RBK-250 | 250 kg | Cluster (PTAB) | Best vs. massed armor |

- CCIP: visual dive delivery
- CCRP: automated level-flight delivery using Shkval ground point

> **Realism Note:** CCRP in the Su-25T is less accurate than Western equivalents (JDAM/Paveway). Wind correction is manual and rudimentary. Expect CEP of 30–100 m depending on approach.

---

## Module 3 — Guided Weapons Overview

### 9A4172 Vikhr ("AT-16 Scallion")

The Vikhr is the Su-25T's signature weapon — a supersonic laser-beam-riding anti-tank missile. Two Vikhr rails are standard (12 total rounds).

| Parameter | Value |
|---|---|
| Guidance | Laser beam-riding (active beam from aircraft) |
| Speed | Supersonic (Mach 1.8+) |
| Min range | ~800 m |
| Max range (low alt) | ~6 km |
| Max range (high alt) | ~8–10 km |
| Warhead | Tandem HEAT — defeats ERA |

**Critical — Beam Discipline:** After launch, the aircraft must maintain the laser beam on the target. Banking > 30° will break the beam and the missile will go ballistic. **Fly straight and level after launch.**

**Launch Authorization Override (`LAlt + W`):** The Su-25T fire control can be over-conservative and refuse a valid shot. This override forces launch. Use it only for legitimate shots, not as a routine shortcut.

> **Realism Note:** Real pilots use the launch override only in extremis (e.g., emergency close-range shots). DCS players often use it routinely for max-range shots where the fire control is too cautious.

### Kh-25ML (AS-10 Karen) & Kh-29L (AS-14 Kedge)

Semi-active laser homing missiles — the missile homes on laser energy reflected from the target.

| Parameter | Kh-25ML | Kh-29L |
|---|---|---|
| Warhead | ~90 kg HE | ~320 kg HE |
| Range | < 10 km | < 12 km |
| Best targets | APCs, bunkers, light SA | Bridges, ships, concrete |
| Guidance | Semi-active laser | Semi-active laser |

**Key difference from Vikhr:** After launch, you have more freedom to maneuver — as long as the Shkval gimbal limits are not exceeded. The missile rides the laser reflected from the target, not a beam projected from the aircraft.

---

## Module 4 — SEAD Overview

### L-081 "Fantasmagoria" Pod

The Fantasmagoria is an ELINT (Electronic Intelligence) pod that detects and classifies radar emitters.

- Displays radar emitters as diamonds on the HUD
- Cursor-selectable to designate a specific emitter for missile handoff
- **Centerline only** — same conflict as Mercury

### Kh-58 (AS-11 Kilter)

| Parameter | Value |
|---|---|
| Target | Long-range search/fire-control radars |
| Range | Up to 120 km (high alt) |
| Speed | Mach 3+ |
| Memory | INS midcourse — will fly to last known position if radar shuts off |

True fire-and-forget. Turn away after launch.

### Kh-25MPU (AS-12 Kegler)

| Parameter | Value |
|---|---|
| Target | SHORAD radars (Roland, Gepard, Osa) |
| Range | 20–40 km |
| Memory | Limited — effectively ballistic if radar turns off |

> **Realism Note:** DCS is occasionally generous with the Kh-25MPU's ability to hit a shut-down radar. In reality, it needs the emitter to stay active for terminal homing.

---

## Weapons Modes Cheat Sheet

| Weapon | Master Arm | Mode Key | Select | Lock Required | Laser |
|---|---|---|---|---|---|
| Gun | ON | `7` (A-G) | `C` | No | Optional |
| Rockets | ON | `7` (A-G) | `D` or pylon select | No | **Mandatory** |
| FAB Bombs (CCIP) | ON | `7` (A-G) | pylon select | No | Recommended |
| FAB Bombs (CCRP) | ON | `7` (A-G) | pylon select | Shkval ground lock | **Mandatory** |
| Vikhr | ON | `7` (A-G) | pylon select | Shkval target lock | **Mandatory** |
| Kh-25ML/29L | ON | `7` (A-G) | pylon select | Shkval target lock | **Mandatory** |
| Kh-58 | ON | `7` (A-G) | pylon select | Fantasmagoria emitter | N/A |
| Kh-25MPU | ON | `7` (A-G) | pylon select | Fantasmagoria emitter | N/A |

---

## Completion Standards

Pass by correctly answering all five questions before proceeding to Event 2:

- [ ] **Q1:** The Shkval is slewing toward a target at 5 km but the image is dark and smoky. Should you lock and fire the Vikhr? *(Answer: No — Rule 1, positive VID required)*
- [ ] **Q2:** After launching a Vikhr, you roll 45° to avoid terrain. What happens to the missile? *(Answer: Beam break — missile goes ballistic and misses)*
- [ ] **Q3:** You want to use the Mercury LLTV pod tonight. What centerline pod are you giving up? *(Answer: Fantasmagoria or MPS-410 — cannot carry both)*
- [ ] **Q4:** What is the minimum launch range for the Vikhr? *(Answer: ~800 m)*
- [ ] **Q5:** In CCRP bomb mode, what does the pilot do after locking the Shkval on a ground point? *(Answer: Fly to align the steering cue and hold weapon release — the system drops automatically)*

---

[→ Proceed to Event 2: Guns & Rockets](event-2-guns-rockets.md)

---

*Based on Eagle Dynamics DCS World documentation. For simulation use only.*
