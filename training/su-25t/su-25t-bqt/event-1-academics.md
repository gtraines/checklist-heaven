# Event 1 — Aircraft Systems & Academics

> **Course:** Su-25T Basic Qualification Training | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Aircraft Overview](#aircraft-overview)
3. [Propulsion — R-195 Engines](#propulsion--r-195-engines)
4. [Flight Control System](#flight-control-system)
5. [Avionics — ACS Modes](#avionics--acs-modes)
6. [Operating Limitations](#operating-limitations)
7. [Emergency Procedures (Academic)](#emergency-procedures-academic)
8. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] State the key aerodynamic differences between the Su-25A and Su-25T
- [ ] Explain the R-195 engine spool-up lag and its operational implications
- [ ] Identify the four ACS modes and when each is used
- [ ] Recite the three most critical operating limitations from memory
- [ ] State the correct response to a dual engine flameout below 2,000 m

---

## Aircraft Overview

### Su-25T vs. Su-25A — Key Differences

The Su-25T "Frogfoot-B" is a substantially modified variant of the base Su-25A. While it shares the same airframe and engines, the "T" variant carries significant additional weight and drag from its advanced avionics suite.

| Parameter | Su-25A | Su-25T | Delta |
|---|---|---|---|
| Empty Weight | ~9,500 kg | ~10,740 kg | +1,240 kg |
| Dorsal Hump | None | Large avionics bay | +Drag |
| Nose Sensor | Small RSBN fairing | I-251 Shkval EO pod | +Drag |
| Max TO Weight | ~17,600 kg | ~19,500 kg | +1,900 kg |

**Instructor Note:** The "Hump Penalty." The avionics dorsal hump and Shkval nose sensor add meaningful parasitic drag. The Su-25T bleeds energy significantly faster in sustained turns than the base Su-25A. It is a dedicated attack aircraft, not a maneuvering fighter.

---

## Propulsion — R-195 Engines

### Engine Specifications

| Parameter | Value |
|---|---|
| Engine | 2× Tumansky R-195 Turbojet |
| Max Thrust (each) | 4,500 kgf |
| Idle RPM (N1 / N2) | ~36–40% / ~60–65% |
| Max RPM | 100% N1 |

### ⚠ Critical: Engine Spool-Up Lag

The R-195 takes **9–12 seconds** to spool from idle to maximum thrust. This is the single most dangerous characteristic of the aircraft for new pilots.

**Operational implications:**
- On final approach, never allow airspeed to decay below final approach speed without anticipating a power correction well in advance
- A go-around initiated below 200 m AGL at idle may not produce useful thrust before runway contact
- Practice the throttle-to-max sequence on the ramp before the first flight: advance to max, count seconds aloud, observe RPM stabilization

**Instructor Note:** Students frequently crash on approach because they are behind the power curve. The common failure is: "I added power" — but they added it too late. The jet was already committed to impact.

---

## Flight Control System

The Su-25T uses a **purely hydro-mechanical flight control system**. There is no fly-by-wire (FBW) computer, no auto-trim, and no angle-of-attack protection.

**Implications for the student:**
- Every significant speed change requires a corresponding pitch trim input
- Stall and departure from controlled flight are entirely the pilot's responsibility
- Hydraulic failure (simulated in DCS) makes the controls extremely heavy

### Trim System
- **Pitch Trim Up:** `]` (right bracket)
- **Pitch Trim Down:** `[` (left bracket)
- **Roll Trim Left/Right:** `RCtrl + [` / `RCtrl + ]`
- **Rudder Trim Left/Right:** `RShift + [` / `RShift + ]`

**Instructor Note:** Students who "fight the stick" without trimming will fly imprecise profiles and fatigue quickly. The mantra for this aircraft is: **Trim for speed. Trim early. Trim often.**

---

## Avionics — ACS Modes

The Automatic Control System (ACS) provides flight guidance assistance. It does **not** replace pilot inputs; it augments them.

| Mode | Activation | Function |
|---|---|---|
| Route Following | Via NAV page | Follows programmed waypoints |
| Combat Steering | Via weapons panel | Stabilizes aiming for gun/rocket passes |
| Coupled Landing | Via ACS Landing | ILS/PRMG instrument approach coupling |
| **Emergency Level** | `LAlt + 3` | Returns aircraft to straight and level — use any time control is lost |

**Instructor Note:** Teach `LAlt + 3` as the first emergency response for spatial disorientation or loss of control in IMC. It is a life-saving command.

---

## Operating Limitations

Memorize these three limitations before your first flight:

| Limitation | Value | Consequence of Violation |
|---|---|---|
| Max Takeoff Weight | 19,500 kg | Tire failure during roll |
| Max Landing Weight | 13,300 kg | Structural damage on touchdown |
| Max AoA (sustained) | 20 units | Flat spin — often unrecoverable below 2,000 m |

### Airspeed Limitations

| Limit | Speed |
|---|---|
| Vne (Never Exceed) | 970 km/h |
| Gear Extension | < 400 km/h |
| Flap Extension (T/O) | < 400 km/h |
| Flap Extension (Landing) | < 350 km/h |

---

## Emergency Procedures (Academic)

These procedures are academic review only. Memorize responses; do not attempt to execute them in simulation without a full briefing.

### Dual Engine Flameout
1. **If above 2,000 m AGL:** Attempt airstart — both throttles to idle, then advance smoothly past 60% N1
2. **If below 2,000 m AGL:** Eject immediately (`RShift + E` hold 1 sec, then `RShift + E` hold 3 sec)

### Single Engine Failure
1. Maintain directional control with rudder
2. Identify failed engine (dead foot = dead engine)
3. Verify failed throttle — do not shut down a good engine
4. Land at nearest suitable airfield

### Hydraulic Failure
1. Trim the aircraft to maintain level flight (controls become heavy)
2. Declare emergency; fly a straight-in approach
3. Avoid aggressive maneuvering — control response is degraded

---

## Completion Standards

This is an academic event. The student passes by correctly answering the following questions before proceeding to Event 2:

- [ ] **Q1:** What is the R-195 spool-up time from idle to max thrust? *(Answer: 9–12 seconds)*
- [ ] **Q2:** What is the maximum AoA before entering a potentially unrecoverable flat spin? *(Answer: 20 units)*
- [ ] **Q3:** What key command returns the aircraft to straight and level in an emergency? *(Answer: `LAlt + 3`)*
- [ ] **Q4:** What is the max landing weight? *(Answer: 13,300 kg)*
- [ ] **Q5:** You are on final approach and airspeed drops below target. You add full power. What should you expect? *(Answer: 9–12 second lag before thrust is useful — a go-around at low altitude may not be possible)*

---

[→ Proceed to Event 2: Familiarization Flight 1](event-2-fam-1.md)

---

*Based on Eagle Dynamics DCS World documentation. For simulation use only.*
