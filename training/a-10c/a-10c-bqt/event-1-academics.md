# Event 1 — Aircraft Systems & Academics

> **Course:** A-10C Basic Qualification Training | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [A-10C vs. A-10A — Key Differences](#a-10c-vs-a-10a--key-differences)
3. [Propulsion — TF34-GE-100A Engines](#propulsion--tf34-ge-100a-engines)
4. [Flight Control System — SAS & EAC](#flight-control-system--sas--eac)
5. [Fuel, Hydraulic & Electrical Systems](#fuel-hydraulic--electrical-systems)
6. [Cockpit Orientation](#cockpit-orientation)
7. [AoA Indexer & Stall Characteristics](#aoa-indexer--stall-characteristics)
8. [Operating Limitations](#operating-limitations)
9. [Boldface Emergency Procedures](#boldface-emergency-procedures)
10. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Explain the key differences between the A-10A (FC3) and A-10C (full-fidelity) DCS modules
- [ ] State TF34-GE-100A engine characteristics: thrust, spool-up time, ITT limits, and start abort criteria
- [ ] Describe the SAS and EAC systems: what each does, how they differ, and what happens when they fail
- [ ] Explain the dual-hydraulic system (A and B), what each powers, and manual reversion capability
- [ ] Locate and identify all major cockpit panels by name and position
- [ ] Describe AoA indexer indications and the stall onset sequence
- [ ] Recite all critical operating limitations from memory (G-limits, V-speeds, ITT limits, crosswind)
- [ ] Recite all five boldface emergency procedures verbatim, in sequence, without reference to notes

---

## A-10C vs. A-10A — Key Differences

| Characteristic | A-10A (FC3) | A-10C (Full Fidelity) | Implication |
|---|---|---|---|
| **Cockpit** | Simplified — no clickable controls | Full clickable cockpit — every switch interactive | A-10C requires physical cockpit interaction for every procedure |
| **Startup** | Two keystrokes per engine | Full switch-by-switch startup (~20 steps) | A-10C startup takes 10–15 minutes done correctly |
| **Navigation** | HUD steerpoint cue only | CDU, EGI, MFCDs, TACAN, ILS — full suite | Much more powerful, but requires active management |
| **EGI/INS** | Not present | Full Embedded GPS/INS requiring alignment | Must align before taxi; takes 3–5 minutes |
| **SAS/EAC** | Not present | Full SAS (rate damping) + EAC (attitude hold) | Significantly easier to fly precisely — but must be set up |
| **Weapons** | Keybind-only | Full avionics: MFCD WPN page, DSMS, TGP | Weapons employment course required |
| **Engine Instruments** | HUD overlay display | Full analog gauge panel (ITT, N1, N2, FF, Oil) | Student reads physical gauges on right instrument panel |
| **DCS Key Difference** | Keyboard-centric | Mouse + HOTAS — keyboard as backup | The student must be comfortable clicking in the cockpit |

---

## Propulsion — TF34-GE-100A Engines

### Engine Specifications

| Parameter | Value | Notes |
|---|---|---|
| Engine Model | General Electric TF34-GE-100A | High-bypass turbofan, 6.2:1 bypass ratio |
| Thrust (per engine) | 9,065 lbf (40.32 kN) | Sea level static |
| Total Installed Thrust | ~18,130 lbf | Both engines |
| Ground Idle (N1) | 62–65% | Post-start stabilized value |
| Flight Idle (N1) | ~70% | Engages automatically when airborne |
| Max N1 | 98% | Primary thrust indicator |
| Max N2 | 99% | Core speed |
| ITT Limit — Start | **860°C** | Abort start if exceeded |
| ITT Limit — Max Continuous | **810°C** | Normal operations |
| ITT Limit — Transient (takeoff) | 900°C | 5-minute limit only |
| Min Oil Pressure | 15 PSI | Below = caution; 0 PSI = shutdown |
| Fuel Flow (cruise, both) | ~1,800–2,200 lbs/hr | Medium altitude |
| Fuel Flow (max power, both) | ~3,000–3,500 lbs/hr | Full military power, low altitude |

### Spool-Up Characteristics

The TF34's high-bypass design spools from idle to military power in **4–6 seconds** — faster than a turbojet, but the delay is operationally significant. On final approach, power corrections must be **anticipatory**, not reactive. A pilot who waits until the aircraft is sinking to add power will still be sinking 5 seconds later when that power finally arrives.

### Start Abort Criteria

| Condition | Indication | Required Action |
|---|---|---|
| **Hot Start** | ITT exceeds 860°C and continues rising during start | Throttle to CUTOFF immediately; Engine Operate to MOTOR (dry crank 30 sec) |
| **Hung Start** | N2 stagnates below 55%; ITT rising without N2 progress | Throttle to CUTOFF; Engine Operate to OFF |
| **No Light-Off** | No ITT rise within 30 seconds of fuel introduction | Throttle to CUTOFF; investigate ignition and fuel |
| **Low Oil Pressure** | Oil pressure below 15 PSI after idle stabilization | Shutdown engine; investigate |

---

## Flight Control System — SAS & EAC

### SAS (Stability Augmentation System)

SAS provides **rate damping** — it resists uncommanded aircraft motion in pitch, yaw, and roll. SAS does NOT hold attitude; it simply reduces the tendency of the aircraft to diverge from its current state.

| SAS Feature | Detail |
|---|---|
| **Channels** | Pitch, Yaw, Roll — three independent switches on SAS Panel (left console) |
| **Behavior** | Dampens oscillations and aircraft response to turbulence/asymmetric thrust |
| **Flying without SAS** | Aircraft is controllable but requires significantly more pilot input; dutch-roll tendency without Yaw SAS |
| **Channel tripping** | Individual channels can trip off due to transients (weapon release, heavy turbulence); must be manually reset |
| **Check before takeoff** | All three channels must be confirmed ON before departing; this is a **gate item** |

### EAC (Enhanced Attitude Control)

EAC provides **attitude hold and turn coordination**. When the pilot releases the stick with EAC engaged, the aircraft maintains its current bank angle and pitch attitude.

| EAC Feature | Detail |
|---|---|
| **Requires SAS** | EAC operates through the SAS servos — if a SAS channel is off, EAC cannot function on that axis |
| **Arm** | EAC ARM switch on SAS Panel → engaged via paddle switch on HOTAS stick |
| **What it holds** | Current pitch attitude and bank angle — NOT heading, altitude, or route |
| **Turn coordination** | Reduces need for active rudder input in turns |
| **Disengage** | Paddle switch (back of stick grip) disengages both EAC and autopilot functions |

> *⚠ Realism Divergence: DCS models SAS and EAC with high fidelity. The real A-10C has separate left and right Yaw SAS channels — DCS combines these into a single Yaw SAS switch. SAS channel trips are modeled accurately. EAC attitude hold and turn coordination work correctly.*

### Trim

| Method | Control | Notes |
|---|---|---|
| **Electric trim (pitch/roll)** | 4-way hat on HOTAS stick | Primary method — trim continuously as speed changes |
| **Rudder trim** | Rotary knob on left console | Set once for each cruise configuration |
| **When to trim** | After every speed change, configuration change, and power change | The A-10C will not fly itself without trimming |

**Mantra:** If you are holding constant stick pressure, you are out of trim. Trim for speed. Trim early. Trim often.

---

## Fuel, Hydraulic & Electrical Systems

### Fuel System — Key Facts

| Parameter | Value |
|---|---|
| Internal Fuel | ~10,700 lbs (~1,644 US gal) |
| External Tanks | 2 × 600 US gal (Stations 3 and 9, optional) |
| Low Fuel Warning | ~1,500 lbs — Master Caution + FUEL LOW caution |
| Bingo Fuel (RTB planning) | ~2,500–3,000 lbs (mission dependent) |
| Crossfeed | Left console — Fuel Panel; open for single-engine ops |
| No fuel dump | Cannot dump fuel — burn or jettison stores if overweight |

### Hydraulic System — Key Facts

| System | Pressure | Powers |
|---|---|---|
| **System A** (left engine) | 3,000 PSI | Left elevator, left aileron, left rudder, NWS, normal brakes |
| **System B** (right engine) | 3,000 PSI | Right elevator, right aileron, right rudder, speed brakes, utility |
| **Combined** | Both | Landing gear, flaps |

**Manual Reversion:** With BOTH hydraulic systems failed, the pilot engages manual reversion (Pitch and Roll switches on left console to MAN REVERT). Stick forces increase to ~60–80 lbs. The aircraft remains flyable but sluggish — no flaps, no speed brakes, emergency gear only, differential braking for directional control.

### Electrical System — Key Facts

| Component | Function |
|---|---|
| **Battery** | 24V DC — ~30 min endurance on essential bus |
| **APU Generator** | Powers AC and DC buses on the ground / emergency in flight (< 15,000 ft) |
| **Left/Right Generators** | Primary power — both required for normal operations |
| **Essential Bus** | Standby ADI, engine instruments, fire warning — always powered if any source available |
| **Double Gen Failure** | Non-essential bus shed; battery + APU only; HUD, MFCDs, CDU, UFC all fail |

---

## Cockpit Orientation

The student must be able to locate each panel **by name** before Event 2. Use the DCS cockpit view and the A-10C checklist for visual reference.

| Panel / System | Location | Key Functions |
|---|---|---|
| **Electrical Panel** | Left console, forward | Battery, APU, L/R Generator, Inverter |
| **Fuel Panel** | Left console, mid-forward | Boost pumps, Crossfeed |
| **ECS Panel** | Left console, mid | Pitot Heat, Engine Anti-Ice, Defog |
| **SAS Panel** | Left console, mid-aft | Pitch/Yaw/Roll SAS, EAC ARM |
| **Flight Control Panel** | Left console, aft | Manual Pitch/Roll Reversion, Flap Switch, Speed Brake |
| **Engine Panel** | Left console, aft-lower | Engine Operate (IGN/MOTOR/NORM); Fire T-handle area |
| **Throttle Quadrant** | Left console, lower | Dual throttles, CUTOFF detent |
| **CDU** | Right console, forward | Primary navigation computer |
| **Lighting Panel** | Right console, mid | Cockpit and exterior lights |
| **TACAN Panel** | Right console, mid | Channel, mode (T/R / A/A) |
| **IFF Panel** | Right console, mid-aft | Mode 1/2/3/4, IDENT |
| **UFC (Upfront Controller)** | Glareshield, center | Radios, IFF, steerpoint, Master Caution acknowledge |
| **AHCP** | Glareshield, left | Master Arm, TGP, Laser Arm, IFFCC — **SAFE during BQT** |
| **CMSC** | Right of right MFCD | RWR threat display, missile warning |
| **Fire T-Handles** | Glareshield | L/R engine fire handle — PULL to shut off fuel/hydraulic |
| **Left MFCD** | Instrument panel, left | TAD, TGP, system pages |
| **Right MFCD** | Instrument panel, right | HSD, WPN, status pages |
| **Engine Gauges (ITT, N1, N2, FF, Oil)** | Lower instrument panel | Right side — analog gauges, read-only |
| **Hydraulic Gauges** | Lower right instrument panel | HYD A and HYD B pressure (normal: 3,000 PSI) |
| **AoA Indexer** | Left canopy rail | Three lights — primary approach speed reference |
| **Standby ADI** | Right glareshield | Pull knob to uncage — backup attitude reference |

---

## AoA Indexer & Stall Characteristics

### AoA Indexer

The AoA indexer is mounted on the left canopy rail and is visible in peripheral vision during approach. It is the **primary approach speed reference** — not the airspeed indicator.

| Indication | Symbol | AoA (Units) | Meaning | Action |
|---|---|---|---|---|
| Upper chevron only | ▲ | < 8 | FAST | Reduce power; allow nose to rise slightly |
| Upper chevron + donut | ▲● | 8–10 | Slightly fast | Minor power reduction |
| **Green donut only** | **●** | **~11** | **ON-SPEED — TARGET** | Maintain |
| Donut + lower chevron | ●▼ | 12–14 | Slightly slow | Add power smoothly |
| Lower chevron only | ▼ | 15–18 | SLOW | Add power; do NOT raise nose further |
| Lower chevron flashing | ▼▼ | > 18 | DANGEROUSLY SLOW | Go around / recover immediately |

**Key Point:** The green donut corresponds to ~11 AoA units **regardless of aircraft weight**. As weight increases, the KIAS at which the donut illuminates rises automatically. This is why the indexer is superior to a fixed target airspeed.

### Stall Sequence

| Phase | AoA (Units) | Indication |
|---|---|---|
| Light buffet onset | ~18 | Airframe vibration; lower chevron showing |
| Stall warning | ~20 | Audio warning; indexer flashing |
| Full stall | ~22–24 | Wing stall; nose drops |

**Stall Recovery:** Nose down (reduce AoA first) → Power to Military → Wings level → Recover. Altitude loss: 200–500 ft depending on entry conditions. Never pull through the buffet.

---

## Operating Limitations

Memorize these before Event 2. They will be tested verbally at the start of the check ride.

### Structural / G-Limits

| Limit | Value | Consequence |
|---|---|---|
| **Max Takeoff Weight** | ~51,000 lbs structural | Tire/structural overload |
| **Max Landing Weight** | 46,000 lbs structural; recommend < 40,000 lbs | Hard landing damage |
| **G-Limit (clean)** | +7.33 G / −3.0 G | Structural failure |
| **G-Limit (stores)** | +5.0 G | Stores asymmetry reduces limit further |

### Airspeed Limits

| Limit | Speed (KIAS) |
|---|---|
| Vr (Rotation) | 135–150 (weight dependent) |
| Vy (Best Climb) | 200–220 |
| Vfe (Flap Limit) | 200 |
| Vlo (Gear Limit) | 200 |
| Vne (Never Exceed) | 450 |
| Corner Speed | 280–320 |
| Approach (On-Speed) | 130–140 (AoA indexer: green donut) |

### Engine Limits

| Limit | Value |
|---|---|
| ITT Start Limit | **860°C** (abort if exceeded) |
| ITT Max Continuous | **810°C** |
| ITT Transient | 900°C (5-minute limit) |
| N1 Max | 98% |
| N2 Max | 99% |
| APU Max Altitude | 15,000 ft |

### Crosswind Limits

| Surface | Max Crosswind |
|---|---|
| Dry runway | 30 kts |
| Wet runway | 20 kts |
| Max tailwind | 10 kts |

---

## Boldface Emergency Procedures

These five procedures must be **committed to memory** and recited verbatim before Event 2. They will be tested at the start of Event 7 and the Check Ride. Incorrect boldface = no flight.

### 1. ABORT (Engine Failure/Fire on Takeoff)

| Step | Action |
|---|---|
| 1 | **THROTTLES** — **IDLE** |
| 2 | **WHEEL BRAKES** — **MAX** |
| 3 | **SPEED BRAKES** — **OPEN** |
| *(If fire exists:)* | |
| 4 | **FIRE HANDLE (Affected)** — **PULL** |
| 5 | **EXTINGUISHER SWITCH** — **FWD/AFT as required** |

### 2. ENGINE FIRE IN FLIGHT

| Step | Action |
|---|---|
| 1 | **THROTTLE (Affected Engine)** — **IDLE** |
| 2 | **FIRE HANDLE (Affected Engine)** — **PULL** |
| 3 | **EXTINGUISHER SWITCH** — **FWD/AFT as required** |
| 4 | **LAND ASAP** |

### 3. DOUBLE ENGINE FAILURE

| Step | Action |
|---|---|
| 1 | **THROTTLES** — **IDLE** |
| 2 | **APU SWITCH** — **START** |
| 3 | **ENGINE OPERATE SWITCHES** — **IGN** |
| *(Proceed to crossbleed/APU restart logic)* | |

### 4. MANUAL REVERSION (Dual Hydraulic Failure)

| Step | Action |
|---|---|
| 1 | **FLIGHT CONTROLS** — **MAN REVERSION** (Pitch and Roll switches) |
| 2 | **Fly conservatively** — limited control authority |
| 3 | **LAND ASAP** — no flaps; emergency gear extension |

### 5. EJECTION

| Step | Action |
|---|---|
| 1 | **EJECTION HANDLE** — **PULL** |

**ACES II Seat Limits:**
- Zero-zero capable (0 speed, 0 altitude)
- Minimum altitude in a dive: 2,000 ft AGL
- Minimum altitude inverted: 6,000 ft AGL
- Maximum speed: 450 KIAS
- DCS command: `LCtrl + E` (hold 1 second)

---

## Completion Standards

This is an academic event. The student passes by correctly answering the following questions without reference to notes. All answers must be recited, not read.

- [ ] **Q1:** What is the ITT abort limit during engine start? *(860°C)*
- [ ] **Q2:** You advance the throttle to CUTOFF first on startup. At what N2 percentage do you introduce fuel? *(12–15% N2)*
- [ ] **Q3:** What does SAS do, and what does EAC add? *(SAS = rate damping; EAC = attitude hold and turn coordination via SAS servos)*
- [ ] **Q4:** Hydraulic System A fails. What is lost? What is retained? *(Lost: left elevator, aileron, rudder, NWS, normal brakes. Retained: System B covers right-side controls — aircraft is still flyable)*
- [ ] **Q5:** What does the green donut on the AoA indexer represent? *(On-speed — optimal approach AoA, ~11 units, regardless of weight)*
- [ ] **Q6:** Recite the ABORT boldface verbatim. *(Throttles idle / Wheel brakes max / Speed brakes open / Fire handle pull if fire / Extinguisher FWD or AFT)*
- [ ] **Q7:** Recite ENGINE FIRE IN FLIGHT boldface verbatim. *(Throttle idle / Fire handle pull / Extinguisher FWD or AFT / Land ASAP)*
- [ ] **Q8:** What is the minimum ejection altitude for an uncontrolled aircraft in level flight? In a dive? *(Level: zero-zero capable. Dive: 2,000 ft AGL minimum)*

---

[→ Proceed to Event 2: Startup & Ground Operations](event-2-startup-taxi.md)

---

*Based on T.O. 1A-10C-1, AFMAN 11-2A-10C Vol 3, and Eagle Dynamics DCS A-10C documentation. For simulation use only.*
