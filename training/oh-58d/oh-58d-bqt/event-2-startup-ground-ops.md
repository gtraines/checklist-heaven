# Event 2 — Startup & Ground Operations

> **Course:** OH-58D Kiowa Warrior Basic Qualification Training | **Event Type:** Flight (Ground Operations Focus)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Cold-and-Dark to Engine Running](#part-1--cold-and-dark-to-engine-running)
5. [Part 2 — Post-Start Checks](#part-2--post-start-checks)
6. [Part 3 — AHRS/GPS Alignment](#part-3--ahrsgps-alignment)
7. [Part 4 — Rotor Engagement](#part-4--rotor-engagement)
8. [Part 5 — Pre-Hover-Taxi Checks](#part-5--pre-hover-taxi-checks)
9. [Part 6 — Hover Taxi](#part-6--hover-taxi)
10. [Part 7 — Shutdown](#part-7--shutdown)
11. [Completion Standards](#completion-standards)
12. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Complete a full cold-and-dark startup without exceeding TOT limits (843°C) or missing any start abort criterion
- [ ] Power on all avionics and systems in the correct sequence
- [ ] Complete a full AHRS/GPS alignment and verify navigation solution before hover taxi
- [ ] Engage the rotor system safely from engine idle
- [ ] Perform all pre-hover-taxi and pre-takeoff checks
- [ ] Hover taxi the aircraft using proper cross-check and speed control (< 20 kts, < 3 ft AGL)
- [ ] Perform a complete shutdown from engine running to cold-and-dark

> **This event does not include takeoff or flight.** The student performs hover taxi to a designated point and back, then shuts down. Emphasis is entirely on procedural accuracy and TOT monitoring during start.

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase 1 | Cold-and-dark startup (all switches) |
| Phase 2 | Post-start systems checks |
| Phase 3 | AHRS/GPS alignment — wait for full navigation solution |
| Phase 4 | Rotor engagement |
| Phase 5 | Pre-hover-taxi checks |
| Phase 6 | Hover taxi to a designated point and back |
| Phase 7 | Hover to touchdown; shutdown cold-and-dark |

### Key Numbers for This Event

| Item | Value |
|---|---|
| TOT Start Abort Limit | **843°C** |
| TOT Continuous Limit | 737°C |
| Ground Idle Nr (target) | ~62–65% |
| Nr Engagement (rotor) | Smoothly 0% → 100% |
| AHRS Alignment Time | ~3–5 minutes (typical) |
| Max Hover Taxi Speed | 20 kts |
| Hover Taxi Altitude | 3–5 ft skid height |
| Engine Cooldown (IDLE) | 2 minutes minimum |
| Throttle → OFF Cooldown | After 2-min idle cooldown |

---

## Pre-Mission Setup

- [ ] Load DCS World; select **OH-58D Kiowa Warrior** on a prepared airfield
  - Caucasus: Batumi or Kobuleti (clear ramp area)
  - NTTR: Nellis or Indian Springs
  - Persian Gulf: Al Minhad or Khasab
- [ ] Set spawn: **cold and dark** (no hot start / no ramp start)
- [ ] Set weather: **good VMC, calm winds or < 10 kts, day**
- [ ] Confirm HOTAS: collective axis, pitch/roll axes, anti-torque pedals or twist-rudder
- [ ] Confirm mouse functionality: hover over battery switch — verify tooltip appears
- [ ] Briefed on abort criteria: TOT **843°C** = throttle OFF immediately

---

## Part 1 — Cold-and-Dark to Engine Running

Work through these steps in sequence. **Do not rush the engine start.** The throttle must be advanced smoothly and the TOT gauge monitored continuously.

### Phase 1A: Electrical Power On

| Step | Switch / Action | Location | Expected Result |
|---|---|---|---|
| 1 | **Battery** — **ON** | Overhead console | DC power on; caution panel illuminates briefly |
| 2 | **Fuel Boost Pump** — **ON** | Overhead console — fuel panel | FUEL BOOST PUMP caution extinguishes |
| 3 | **Avionics Master** — **ON** (if equipped) | Overhead console | Avionics bus powered |

### Phase 1B: Pre-Start Checks

| Step | Check | Expected |
|---|---|---|
| 4 | Throttle | Confirm at **IDLE** or **OFF** detent — not FLY |
| 5 | Collective | Full DOWN |
| 6 | Cyclic and Pedals | Centered / neutral |
| 7 | Caution panel | Note any pre-existing cautions (GEN, FADEC) |
| 8 | Engine instruments | TOT at ambient; N1 at 0% |

### Phase 1C: Engine Start

| Step | Action | Monitor |
|---|---|---|
| 9 | **Starter** — **ENGAGE** (or battery start switch per DCS OH-58D) | N1 begins rising; starter motoring |
| 10 | At **15% N1** — **Throttle to IDLE detent** (fuel introduction) | TOT begins rising — **MONITOR TOT CONTINUOUSLY** |
| 11 | Monitor **TOT during light-off** | TOT rises rapidly during combustion; must stay **below 843°C** |
| 12 | Monitor **N1 rising** | N1 should accelerate past 60% toward ground idle |
| 13 | At **~62–65% N1** — engine stabilizes at ground idle | Starter disengages (auto or manual); check: TOT ≤ 737°C, N1 stable, Oil pressure rising |
| 14 | Verify **Engine Oil Pressure** — 90–130 PSI | If < 60 PSI after 30 seconds → shutdown |

> *⚠ Abort Action: If TOT approaches 843°C at any point during start — **Throttle to OFF immediately**. Do not wait. Do not hesitate. A hot start is a maintenance event; a burned turbine is an expensive and dangerous outcome.*

### Phase 1D: Generator and Inverter On

| Step | Switch | Location | Expected |
|---|---|---|---|
| 15 | **Generator** — **ON** | Overhead console — electrical panel | GEN caution extinguishes; voltmeter shows ~28V |
| 16 | **Inverter** — **ON** | Overhead console — electrical panel | AC bus powered; attitude indicator begins erecting |

---

## Part 2 — Post-Start Checks

With engine running and electrical power established, verify all systems before proceeding.

| System | Check | Standard |
|---|---|---|
| **TOT** | Stable at ground idle | ≤ 737°C |
| **N1** | Ground idle | ~62–65% |
| **Torque** | Ground idle | < 15% (low power) |
| **Engine Oil Pressure** | Normal | 90–130 PSI |
| **Engine Oil Temperature** | Normal | 70–107°C |
| **Transmission Oil Pressure** | Normal | 30–60 PSI |
| **Transmission Oil Temperature** | Normal | < 110°C |
| **Generator Voltage** | Normal | ~28V DC |
| **Caution Panel** | Scan for abnormal cautions | Only ROTOR BRK (rotor not yet engaged) expected |
| **FADEC** | Auto mode confirmed | FADEC caution not illuminated |

---

## Part 3 — AHRS/GPS Alignment

The AHRS/GPS must complete its alignment sequence before accurate navigation is available. Do not hover taxi until alignment is complete — the navigation solution will be inaccurate.

| Step | Action | Expected |
|---|---|---|
| 1 | **AHRS Power** — **ON** | Right console — AHRS/GPS controller |
| 2 | **MFD** — **ON** | MFD power switch |
| 3 | Select **NAV page** on MFD | Observe AHRS alignment progress |
| 4 | **Wait for full alignment** | Alignment progress indicator moves to complete; heading stabilizes |
| 5 | Verify **GPS solution** | GPS satellites acquired; position displayed |
| 6 | Cross-check **indicated position** with known position | Aircraft should be at the airfield spawn coordinates |

**Alignment Time:** Typically 3–5 minutes for a full AHRS alignment. The AHRS uses GPS-aided initialization. Do not rush. Use this time to complete radio setup and review the pre-hover-taxi checklist.

> *⚠ Realism Divergence: In the real OH-58D, a full AHRS alignment requires the aircraft to be stationary and takes 3–5 minutes minimum. Hovering or taxiing before alignment degrades the navigation solution. DCS models the alignment requirement functionally — the heading indication may be unstable before alignment completes. Wait for a stable heading before moving.*

---

## Part 4 — Rotor Engagement

| Step | Action | Location | Monitor |
|---|---|---|---|
| 1 | Confirm **Nr at 0%** | Rotor stationary | — |
| 2 | **Throttle** — **smoothly advance to FLY detent** | Collective grip | Nr begins rising; FADEC schedules fuel to drive rotor |
| 3 | Monitor **Nr rising** | Nr gauge | Rotor accelerates toward 100% |
| 4 | Monitor **TOT** during power increase | TOT gauge | Should remain ≤ 737°C |
| 5 | Monitor **Torque** | Torque gauge | Rises as rotor accelerates |
| 6 | Nr reaches **100%** | Nr gauge at 100% | FADEC governing; Nr stable |
| 7 | Verify **ROTOR BRAKE** — **OFF/disengaged** | Caution panel — ROTOR BRK caution extinguishes | — |

**Rotor Engagement Cues:**
- The aircraft will rock slightly as the rotor accelerates (gyroscopic precession)
- Vibration increases then stabilizes as Nr reaches 100%
- Tail rotor noise changes character at full Nr

> *Do not rush the throttle to FLY. Smooth, deliberate advancement gives the FADEC time to schedule fuel properly and prevents a torque spike.*

---

## Part 5 — Pre-Hover-Taxi Checks

Before lifting to a hover, complete these checks at full operating Nr.

| Item | Check | Standard |
|---|---|---|
| **Nr** | 98–100% | Stable at 100% |
| **TOT** | ≤ 737°C | No exceedance |
| **Torque** | Ground idle reading | Low; will spike on collective pickup |
| **Engine Oil** | Pressure and temperature | Normal range |
| **Transmission Oil** | Pressure and temperature | Normal range |
| **FADEC** | Auto mode | FADEC caution not illuminated |
| **AHRS/GPS** | Alignment complete | Heading stable; GPS acquired |
| **Controls** | Check — cyclic, collective, pedals full range | No binding; full range of motion |
| **Force Trim** | Set — center position | Press-hold, center controls, release |
| **Radios** | Set for airfield frequency | Communication established |
| **Area clear** | Visual check — rotor arc clear of obstacles | Confirm with ground crew if available |

**Control Check:** With Nr at 100%, gently check full cyclic deflection in all four quadrants and full pedal. This confirms the controls are free, have no binding, and that the hydraulic servos are responsive.

---

## Part 6 — Hover Taxi

### Lifting to a Hover

| Step | Action | Monitor |
|---|---|---|
| 1 | Apply **right cyclic** pre-position (slight) | Compensate for translating tendency |
| 2 | **Slowly raise collective** | Torque rises; TOT rises |
| 3 | Add **left pedal** as torque increases | Prevent right yaw |
| 4 | **Light on skids** — aircraft near weightless | Adjust cyclic for balance |
| 5 | Aircraft lifts to 3 ft skid height | Collective: just enough for stable 3 ft hover |
| 6 | Stabilize hover | Nr 98–100%; TOT ≤ 737°C; Torque ≤ 100% |

**Common Hover Issues at Pickup:**
- Left drift: add more right cyclic pre-position
- Right yaw: add left pedal faster as collective rises
- Climbing through 3 ft: collective coming up too fast — ease it
- Nose pitching up: ETL beginning — forward cyclic

### Hover Taxi to Designated Point

| Item | Standard |
|---|---|
| **Altitude** | 3–5 ft skid height |
| **Speed** | < 20 kts groundspeed |
| **Heading** | Maintain intended track; use pedals for small heading changes |
| **Cross-check** | Horizon, airspeed, torque, Nr — continuous scan |
| **Clearance** | Continuously monitor rotor clearance from obstacles |

**Hover taxi technique:** Apply **small cyclic inputs** in the direction of travel. The aircraft responds slowly at walking speed — anticipate the movement and apply small corrections early. Larger inputs lead to pendulum oscillations that are difficult to arrest.

### Setting Down

| Step | Action |
|---|---|
| 1 | Over the designated parking spot, stabilize at 3 ft hover |
| 2 | Slowly reduce collective — aircraft begins to descend |
| 3 | Control descent rate — slow and smooth |
| 4 | Skids contact ground — continue lowering collective |
| 5 | Both skids firmly on ground — collective to full DOWN |
| 6 | Verify no ground resonance |

---

## Part 7 — Shutdown

With both skids on the ground and engine running:

| Step | Action | Location | Notes |
|---|---|---|---|
| 1 | **Throttle** — **IDLE** | Collective grip | Nr decays to ground idle; engine at minimum power |
| 2 | **Wait 2 minutes** | — | Engine cooldown — mandatory |
| 3 | **MFD** — **OFF** | MFD power | Avionics down |
| 4 | **AHRS/GPS** — **OFF** | Right console | Navigation system off |
| 5 | **Radios** — **OFF** | Right console | Comms off |
| 6 | **Throttle** — **OFF** | Collective grip | Engine fuel cut; spool-down begins |
| 7 | Monitor **N1** decreasing | — | Should decrease smoothly to 0% |
| 8 | Monitor **TOT** decreasing | — | Should decrease; rising TOT during shutdown = fuel leak risk |
| 9 | **Generator** — **OFF** | Overhead console | Electrical primary power off |
| 10 | **Inverter** — **OFF** | Overhead console | AC bus off |
| 11 | **Fuel Boost Pump** — **OFF** | Overhead console | Fuel boost off |
| 12 | **Battery** — **OFF** | Overhead console | All power off; cockpit dark |
| 13 | Rotor coasts to stop | — | ~1–3 minutes depending on conditions |
| 14 | Apply **Rotor Brake** (below 40% Nr) if desired | — | Expedites rotor stop |

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Engine start | TOT never exceeded 843°C; no abort criteria triggered |
| Generator/Inverter | Both ON within 30 sec of engine stabilizing at ground idle |
| AHRS/GPS alignment | Full alignment completed before hover taxi |
| Rotor engagement | Nr reached 100%; no torque spike > 110%; no TOT exceedance |
| Pre-hover-taxi checks | All items completed without prompting |
| Hover pickup | Aircraft lifts to 3 ft without excessive yaw, climbing, or lateral drift |
| Hover taxi | Speed maintained < 20 kts; altitude 3–5 ft throughout |
| Shutdown sequence | All switches OFF in correct order; cooldown completed before throttle OFF |

---

## Common Errors

| Error | Correction |
|---|---|
| **Advancing throttle too fast during start** | "Slow down. Give the FADEC time to schedule fuel. A fast throttle advance spikes TOT. Smooth and deliberate." |
| **Not watching TOT during start light-off** | "TOT is the only instrument that matters during start. Eyes on TOT. Everything else can wait." |
| **Skipping the 2-minute cooldown** | "Two minutes at idle. Every time. The turbine is at temperature — thermal shock cracks blades. Build the habit." |
| **Hovering before AHRS alignment complete** | "If your heading is wrong, your navigation is wrong. Wait for the AHRS. It takes 3–5 minutes. Use that time." |
| **Pulling collective without right cyclic pre-position** | "Right cyclic before you pull. If you lift with the cyclic centered, you'll drift left immediately. Pre-position right." |
| **Over-controlling in hover** | "Small inputs. The Kiowa is sensitive. If you chase the aircraft with big inputs, you'll oscillate. Tiny corrections." |
| **Not doing a control check before hover taxi** | "Every time. Full cyclic travel, full pedal, confirm free and clear before you lift." |

---

[→ Proceed to Event 3: Hover & Hover Taxi](event-3-hover.md)

---

*Based on TM 1-1520-248-10, TM 1-1520-248-CL, and Eagle Dynamics / Polychop Simulations DCS OH-58D documentation. For simulation use only.*
