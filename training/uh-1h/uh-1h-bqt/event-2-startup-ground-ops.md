# Event 2 — Startup & Ground Operations

> **Course:** UH-1H Huey Basic Qualification Training | **Event Type:** Simulator
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents

1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — Electrical Power & Pre-Start](#part-1--electrical-power--pre-start)
4. [Part 2 — Engine Start](#part-2--engine-start)
5. [Part 3 — Post-Start Checks](#part-3--post-start-checks)
6. [Part 4 — Avionics Power-On](#part-4--avionics-power-on)
7. [Part 5 — Rotor Engagement to Flight RPM](#part-5--rotor-engagement-to-flight-rpm)
8. [Part 6 — Before-Takeoff Checks](#part-6--before-takeoff-checks)
9. [Part 7 — Hover Taxi](#part-7--hover-taxi)
10. [Part 8 — Normal Shutdown](#part-8--normal-shutdown)
11. [Completion Standards](#completion-standards)
12. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Perform a complete cold-and-dark startup from battery ON to engine running without checklist reference, in correct phase sequence, within limits at every step
- [ ] Recognize and correctly abort a hot start, hung start, and no-light-off condition, including the correct wait times and recheck actions before reattempting
- [ ] Demonstrate understanding of the throttle correlator and governor by performing the governor exercise (governor ON vs. governor OFF), verbally explaining Nr management in each condition
- [ ] Perform a before-takeoff check covering all engine instruments, flight controls, force trim, governor, RPM warning, caution panel, altimeter, radios, and transponder
- [ ] Advance the throttle through the idle stop to FLY and stabilize at flight RPM with collective full down
- [ ] Perform a stable hover at 3–5 ft skid height with no more than ±1 ft altitude deviation, ±5° heading deviation, and no more than 3 ft lateral drift over a 30-second stabilization period
- [ ] Execute a hover taxi for a minimum 200 ft along a taxiway with a ground track within 5 ft of centerline
- [ ] Perform a complete normal shutdown in correct sequence from flight RPM to engine off to battery off
- [ ] State all start abort criteria (hot start, hung start, no light-off) and the EGT starting limit (720°C) from memory

---

## Ground Brief

### Mission Profile

This is an **out-and-back simulator session** flown from the starting ramp position.

1. Cold-and-dark startup through all phases
2. Governor exercise (ground idle, no translational flight)
3. Advance to flight RPM
4. Before-takeoff checks
5. Hover at starting position — stabilization exercise
6. Hover taxi to holding short
7. Return hover taxi to starting position
8. Normal shutdown

**No departure from the airfield is planned for this event.** If the student is performing well and time permits, a confined-area liftoff/hover-OGE assessment may be added at IP discretion.

### Key Numbers Table

| Parameter | Value | Notes |
|---|---|---|
| **EGT starting limit** | **720°C (10 sec max)** | Throttle to CLOSED immediately if exceeded |
| **EGT continuous limit** | 610°C | Must be below this before advancing to FLY |
| **Nr normal (flight)** | 321–327 RPM | Governor maintains; dual tach needles married |
| **Nr low warning** | 294 RPM | Audio tone; lower collective / increase throttle |
| **Nr overspeed** | >345 RPM | Structural risk — reduce collective and throttle |
| **Torque continuous max** | 40 PSI | IGE hover typically 25–35 PSI |
| **Engine oil pressure** | 35–70 PSI | Must rise within 30 sec of start |
| **Engine oil temp** | <107°C | |
| **Trans oil pressure** | 30–70 PSI | |
| **Trans oil temp** | <110°C | |
| **N1 (ground idle)** | 58–62% | Engine stabilization point |
| **Hover altitude (hover taxi)** | 3–5 ft skid height | Higher = more power; more LTE exposure |
| **Starter fuel introduction** | ~15% N1 | Throttle to IDLE at this N1 value |

### DCS Keybind Reference

| Function | Keybind | Notes |
|---|---|---|
| Battery ON/OFF | `LShift + B` | First switch in startup |
| Inverter ON/OFF | `LShift + I` | Second switch; powers AC gyro instruments |
| Fuel Valve ON/OFF | `LShift + F` | Guarded — lift guard first |
| Fuel Boost Pump ON/OFF | `LCtrl + B` | Extinguishes FUEL BOOST caution |
| Starter Button (hold) | `LShift + Home` | Hold until ~15% N1, then throttle to IDLE |
| Throttle (mouse wheel on 3D grip) | Mouse wheel on twist-grip | CW = increase; CCW = decrease; no keyboard key |
| Idle Stop Release | `LShift + PgDn` | Must press before advancing past IDLE to FLY |
| Generator ON/OFF | `LShift + G` | Post-start; extinguishes GEN caution |
| Governor ON/OFF | `LCtrl + Home` | Post-start; do not turn ON until engine stabilized |
| RPM Warning ON/OFF | *(panel click)* | Overhead console — click to arm |
| Force Trim Release (hold) | `T` | Hold to reposition, release to latch |
| Set Force Trim | `LCtrl + T` | Latch current position |
| Engine Stop | `LShift + End` | Full shutdown / emergency stop |
| Landing Light | `LCtrl + L` | As required |
| Nav / Position Lights | `LShift + L` | As required |

---

## Part 1 — Electrical Power & Pre-Start

> **Starts with:** Aircraft cold-and-dark; all switches off; engine not running; rotor stationary.
>
> **All actions from the overhead console unless noted.**

| Step | Action | Location | Expected Result |
|---|---|---|---|
| 1 | **Battery** — ON (`LShift + B`) | Overhead — Electrical panel | Caution panel illuminates multiple lights; voltmeter ~24V (battery). Normal. |
| 2 | **Caution Panel** — scan | Instrument panel | Multiple lights ON (RPM, GEN, GOV EMER, FUEL BOOST, etc.) — normal on battery only. Verify no *unexpected* unusual indications |
| 3 | **Caution Light Test** — press and hold | Overhead — Test panel | ALL caution lights illuminate. Verify no dead bulbs. Release. |
| 4 | **Inverter** — ON (`LShift + I`) | Overhead — Electrical panel | AC bus powered; attitude indicator starts erecting (allow 2–3 min to fully stabilize) |
| 5 | **Fuel Valve** — OPEN (`LShift + F`) | Overhead — Fuel panel (guarded) | Lift guard; toggle switch. Fuel supply open to engine. No immediate cockpit indication other than valve position. |
| 6 | **Fuel Boost Pump** — ON (`LCtrl + B`) | Overhead — Fuel panel | **FUEL BOOST caution extinguishes** — fuel pressure established. If caution stays ON → stop and check fuel valve and plumbing. |
| 7 | **Fuel Quantity** — check | Instrument panel — Fuel qty gauge | Verify adequate fuel in pounds for planned mission. Note quantity. |
| 8 | **Throttle** — verify CLOSED (full CCW) | Collective grip — twist-grip | No fuel to engine. If not at CLOSED, rotate CCW until fully closed. |
| 9 | **Collective** — full DOWN (friction set) | Left hand | At bottom of travel; minimum blade pitch |
| 10 | **Cyclic** — centered | Right hand | Neutral |
| 11 | **Pedals** — centered | Feet | Neutral; slight left pedal anticipation is acceptable |
| 12 | **Governor (GOV)** — verify OFF | Overhead — Engine panel | Governor must be OFF before start; will be turned ON after stabilization |
| 13 | **Rotor arc** — clear | Visual scan out windows | No personnel or obstacles within rotor sweep (48 ft radius from mast) |

---

## Part 2 — Engine Start

> **Critical monitoring requirements during start: N1 % and EGT °C. Eyes on these two gauges from the moment the starter button is pressed until the engine stabilizes at idle.**

| Step | Action | Location | Expected Result | Critical Monitoring |
|---|---|---|---|---|
| 14 | **Starter Button** — press and HOLD (`LShift + Home`) | Overhead — Engine panel | Starter engages; N1 begins to climb from 0% | Watch N1 — should increase steadily |
| 15 | Monitor **N1 increasing** | Instrument panel — N1 gauge | N1 climbs: 5% → 10% → 15%... | Smooth, continuous increase. If stagnation → abort |
| 16 | At **~15% N1** — advance **Throttle to IDLE** | Collective grip — twist clockwise to IDLE detent | Fuel introduced to combustion chamber | Watch for EGT rise (light-off) within a few seconds |
| 17 | Monitor **EGT** for light-off confirmation | Instrument panel — EGT gauge | EGT begins rising from ambient — confirms ignition | **If no EGT rise by ~25% N1 → ABORT** |
| 18 | Monitor **EGT** during N1 acceleration | EGT gauge | EGT rises, peaks, then settles as N1 reaches idle | **720°C is the hard limit.** If EGT trend exceeds this → ABORT immediately |
| 19 | Monitor **N1 acceleration** to idle | N1 gauge | N1 accelerates steadily toward ~58–62% | **If N1 stagnates below ~55% with rising EGT → ABORT** (hung start) |
| 20 | When **N1 ~58-62%** — **release Starter Button** | Overhead — Engine panel | Starter disengages; N1 holds at idle RPM | N1 should hold stable at ground idle |
| 21 | **Stabilize at ground idle** — wait 30–60 sec | All engine instruments | N1: 58–62%, EGT: settling <610°C, rotor spinning up slowly | Do not advance throttle or governor until engine is thermally stable |

### Start Abort Decision Matrix

| Condition | Recognition | Immediate Action | Before Reattempt |
|---|---|---|---|
| **No light-off** | No EGT rise by ~25% N1 | Throttle to CLOSED immediately; release starter; motor 30 sec to purge | Check fuel valve ON, boost pump ON; wait 30 sec |
| **Hot start** | EGT trending toward or exceeding **720°C** | Throttle to CLOSED **immediately**; motor 30 sec to purge exhaust | Wait **2 minutes** for turbine cooling |
| **Hung start** | N1 stagnates below ~55% with rising EGT | Throttle to CLOSED; release starter; motor to clear | Check battery voltage (may need GPU); wait 2 min |

> *If three consecutive start attempts fail — stop. Brief the IP and troubleshoot cause before attempting again.*

---

## Part 3 — Post-Start Checks

> **Complete this phase before advancing to FLY or engaging the governor. Engine at ground idle, rotor windmilling at low RPM.**

| Step | Action | Location | Expected Result |
|---|---|---|---|
| 22 | **Generator (GEN)** — ON (`LShift + G`) | Overhead — Electrical panel | **GEN caution extinguishes**; voltmeter shows ~28V (generator output). Generator now powering the bus; battery begins charging. |
| 23 | **Governor (GOV)** — ON (`LCtrl + Home`) | Overhead — Engine panel | Governor engages; small Nr adjustment may be noted as governor takes authority. |
| 24 | **RPM Warning Audio** — ON | Overhead — Engine panel | Low-RPM audio warning system armed. Verify by briefly reducing throttle below ~294 Nr threshold and listening for tone (optional — do not allow Nr to drop dangerously). |
| 25 | **Engine Oil Pressure** — check | Instrument panel — Eng oil press gauge | Must be **35–70 PSI** within 30 seconds of start. If not rising → shut down and investigate. |
| 26 | **Engine Oil Temperature** — check | Instrument panel — Eng oil temp gauge | Rising toward operating range. Will take several minutes to reach steady state. No action required if rising trend confirmed. |
| 27 | **Transmission Oil Pressure** — check | Instrument panel — Trans oil press gauge | **30–70 PSI** |
| 28 | **Transmission Oil Temperature** — check | Instrument panel — Trans oil temp gauge | Rising toward operating range. No action required if trend is rising. |
| 29 | **EGT** — verify below continuous limit | Instrument panel — EGT gauge | **<610°C** and stable or decreasing. If above this at idle → investigate before continuing. |
| 30 | **Caution Panel** — verify normal | Instrument panel — Caution panel | All caution lights **extinguished** (GEN, FUEL BOOST lights should now be out). Any remaining lights require investigation before continuing. |

### Governor Exercise (Instructor-Directed)

Perform at ground idle, collective full down, before advancing to FLY:

**Exercise A — Governor ON:**
1. Slowly raise collective 1–2 inches.
2. Observe: Nr remains stable; EGT and torque increase.
3. Lower collective back down.
4. Observe: Nr remains stable; EGT and torque decrease.
5. **Lesson:** Governor holds Nr regardless of collective position.

**Exercise B — Governor OFF (`LCtrl + Home` to disengage):**
1. Turn GOV switch OFF.
2. Slowly raise collective 1–2 inches.
3. Observe: Nr begins to drop; must add throttle to recover.
4. Lower collective. Observe: Nr rises; must reduce throttle to prevent overspeed.
5. Turn GOV switch back ON; observe governor recapture of Nr.
6. **Lesson:** Without governor, pilot must manually manage Nr with every collective change.

---

## Part 4 — Avionics Power-On

| Step | Action | Location | Notes |
|---|---|---|---|
| 31 | **VHF-AM (AN/ARC-134)** — ON, tune | Pedestal — top radio | Tune to ATIS, Ground, or appropriate frequency. Set volume. |
| 32 | **UHF-AM (AN/ARC-51BX)** — ON, set GUARD or assigned | Pedestal — middle radio | Set to GUARD mode (243.0 MHz) or manual-tune to assigned UHF freq. |
| 33 | **FM (AN/ARC-131)** — ON, tune if required | Pedestal — bottom radio | Tune to assigned tactical frequency if required. |
| 34 | **Audio Control Panel** — configure | Pedestal — audio panels | Set receive volumes for all radios; select VHF-AM for transmit (typical). |
| 35 | **ADF (AN/ARN-83)** — ON if required | Navigation panel | Tune to NDB frequency if ADF navigation is planned. |
| 36 | **VOR/ILS (AN/ARN-82)** — ON if required | Navigation panel | Tune to VOR frequency if planned. |
| 37 | **Transponder** — STANDBY | Pedestal | Set squawk code per clearance. Leave in STANDBY until cleared for takeoff. |
| 38 | **Radar Altimeter** — ON, bug set | Instrument panel | Set low-altitude warning bug to desired value (50 ft typical for training). |
| 39 | **Barometric Altimeter** — set QNH | Instrument panel — altimeter | Rotate Kollsman window to current altimeter setting. Verify reading within ±75 ft of known field elevation. |
| 40 | **Heading Indicator (DG)** — align to compass | Instrument panel — DG | Uncage gyro; align DG to magnetic compass with aircraft stationary. |

---

## Part 5 — Rotor Engagement to Flight RPM

> **Prerequisites:** Engine at ground idle; post-start checks complete; all caution lights out; collective FULL DOWN.**
>
> **Keep collective full down throughout this phase.**

| Step | Action | Location | Expected Result | Critical Monitoring |
|---|---|---|---|---|
| 41 | **Collective** — confirm FULL DOWN | Left hand | At bottom stop; minimum blade pitch | |
| 42 | **Idle Stop Release** — press and HOLD (`LShift + PgDn`) | Collective grip — idle stop button | Mechanical stop released; allows throttle to advance beyond IDLE | Hold the button throughout throttle advance |
| 43 | While holding idle stop release — **Throttle** — advance to **FLY** detent (CW, mouse wheel) | Collective grip — twist-grip | Throttle moves from IDLE to FLY; engine power increases | Nr begins to climb; EGT rises moderately |
| 44 | **Release Idle Stop Release** button | Collective grip | Throttle locked in FLY range; cannot accidentally slip back to IDLE | |
| 45 | Monitor **Nr increasing** toward 324 RPM | Instrument panel — Dual tach | Nr climbs smoothly; N2 also rising; governor engages and holds 324 ±3 RPM | EGT must stay <610°C throughout |
| 46 | Dual tach **needles "married"** at 324 RPM | Instrument panel | Nr and N2 overlapping at 100% / 324 RPM — governor holding | Normal indication |
| 47 | Verify **low RPM warning audio** — ON | Overhead — RPM Warning | Audio warning system armed; confirm switch ON | |
| 48 | **Wait 30 seconds** — rotor stabilization | All instruments | Rotor vibration settles; Nr steady; EGT, torque, oil P&T stable | Check all instruments are within limits |

---

## Part 6 — Before-Takeoff Checks

> **Final check before lifting to a hover. Engine at flight RPM, rotor at 324 RPM.**

| Check Item | Action | Expected Result |
|---|---|---|
| **Engine instruments** | Scan all engine gauges | N1 governing normally; Nr 321–327 RPM; EGT <610°C; torque at idle value (<10 PSI); engine oil 35–70 PSI and temp trending normally |
| **Transmission instruments** | Trans oil P&T | Within limits (30–70 PSI; <110°C) |
| **Hydraulic pressure** | Hydraulic gauge | 1,000–1,500 PSI |
| **Flight controls** | Full cyclic deflection (all directions), collective full up/full down, pedals full left/right | Smooth response throughout range; no binding, no resistance beyond normal hydraulic feel |
| **Force trim** | Release trim (`T`); reposition cyclic; re-engage | Magnetic brake holds new position; controls return to neutral effort when held |
| **Governor** | GOV switch — verify ON | Nr stable at 324 RPM |
| **RPM Warning** | Audio — verify ON | |
| **Caution panel** | Verify CLEAR | All lights extinguished |
| **Altimeter** | Cross-check with field elevation | Reading within ±75 ft of known field elevation |
| **Transponder** | Set to ON or ALT (altitude reporting) | Squawk code confirmed |
| **Radios** | Verify tuned and volume set | Comm check complete if required |
| **Mission brief** | Confirm departure intention, abort criteria, emergency plan | Crew/IP acknowledgment |

---

## Part 7 — Hover Taxi

> **Hover altitude: 3–5 ft skid height. Ground speed: walking pace (~5–10 knots) in ramp/congested areas.**

### Pick-Up to Hover

| Step | Action | Expected Result | Common Error |
|---|---|---|---|
| 1 | Slowly raise collective | Torque increases; helicopter gets light on skids | Too rapid — helicopter bounces off or shoots up |
| 2 | Add left pedal as collective rises | Heading maintained; yaw trend countered | Insufficient left pedal — nose yaws right |
| 3 | Apply slight right cyclic | Left drift (translating tendency) countered | Over-correction — helicopter slides right |
| 4 | Continue collective until 3–5 ft skid height | Stable hover IGE | Not holding altitude — see common errors |
| 5 | Stabilize hover for 30 seconds | ±1 ft altitude; ±5° heading; ±3 ft lateral drift | Establish before beginning taxi |

### Hover Taxi Maneuver

| Phase | Pilot Action | Key Technique |
|---|---|---|
| **Begin forward taxi** | Slight forward cyclic | Nose dips ~2–3°; maintain altitude with small collective increase; heading maintained with pedals |
| **Maintain track** | Cyclic to steer along centerline; pedals for heading | Look ahead — not at the ground immediately below |
| **Speed control** | Cyclic pitch angle controls speed; aft cyclic to slow | Smooth, small inputs; allow stabilizer bar to dampen oscillations |
| **Stop** | Aft cyclic to arrest motion | Expect nose pitch-up; slight collective reduction to prevent climb; left pedal as torque increases |
| **Set down** | Slowly lower collective to ground | Maintain heading and track as skids touch; do not drop onto the skids |

### Hover Power Check

Before departing on a full-power maneuver:
1. Establish stable hover at 3–5 ft IGE.
2. Read torque gauge. Note **current hover torque (PSI)**.
3. **Power margin** = Max continuous (40 PSI) − Current hover torque.
4. If margin <5 PSI → marginal power; reconsider OGE operations or reduce weight.
5. If OGE is required (>24 ft AGL): expect 10–15% more torque than IGE reading.

---

## Part 8 — Normal Shutdown

> **From flight RPM, engine running, collective full down, at the parking spot.**

| Step | Action | Location | Expected Result |
|---|---|---|---|
| 1 | **Collective** — full DOWN (hold through entire shutdown) | Left hand | Minimum blade pitch; minimum rotor thrust |
| 2 | **Governor (GOV)** — OFF (`LCtrl + Home`) | Overhead — Engine panel | Governor disengaged; RPM will begin to drop with next step |
| 3 | **Throttle** — retard to IDLE (CCW to IDLE detent) | Collective grip — twist-grip | Engine power reduces; N1 drops toward idle; Nr begins to reduce |
| 4 | **Stabilize at ground idle** — 1–2 minutes | All engine instruments | N1: 58–62%; EGT settling and cooling; Nr at idle/ground idle RPM. Allow engine to cool before shutdown. |
| 5 | **Avionics** — OFF (radios, ADF, VOR, transponder) | Pedestal | All avionics powered off |
| 6 | **RPM Warning** — OFF | Overhead | Audio warning disarmed |
| 7 | **Pitot Heat** — OFF (if on) | Overhead | As required |
| 8 | **Throttle** — CLOSE (full CCW to fuel cutoff) (`LShift + End`) | Collective grip / keyboard | Engine fuel cutoff; N1 and EGT begin to drop toward zero |
| 9 | Monitor **Nr decreasing** | Dual tach | Nr and N2 decreasing and separating (freewheeling unit decouples as N2 drops below Nr); Nr coasts down freely |
| 10 | **Fuel Boost Pump** — OFF (`LCtrl + B`) | Overhead — Fuel panel | Boost pump off |
| 11 | **Fuel Valve** — CLOSED (`LShift + F`) | Overhead — Fuel panel | Fuel system secured |
| 12 | When **Nr below ~30 RPM** — **Generator** — OFF (`LShift + G`) | Overhead — Electrical panel | GEN caution illuminates (expected) |
| 13 | **Inverter** — OFF (`LShift + I`) | Overhead — Electrical panel | AC bus de-powered; AI and DG will cage |
| 14 | **Battery** — OFF (`LShift + B`) | Overhead — Electrical panel | All electrical power removed; caution panel dark |
| 15 | Verify **rotor fully stopped** | Visual | All movement ceased before conducting a walk-around |

---

## Completion Standards

| Standard | Requirement |
|---|---|
| **Startup phase order** | Complete all phases (Electrical → Fuel → Pre-start → Start → Post-start → Avionics → FLY RPM) in correct sequence, no phases transposed |
| **EGT during start** | Never exceed 720°C. If student exceeds this without immediate abort → **unsatisfactory** |
| **Start abort** | Correctly identify and abort any IP-induced start abnormality (hot start, hung start, no light-off) |
| **Governor exercise** | Correctly demonstrate and verbally explain correlator/governor operation, both with governor ON and OFF |
| **Post-start checks** | All engine and transmission instruments verified within limits before advancing to FLY |
| **Before-takeoff check** | All items completed; no items skipped |
| **Hover stability** | Maintain ±1 ft altitude, ±5° heading, ±3 ft lateral over 30-sec evaluation period |
| **Hover taxi track** | Ground track within 5 ft of centerline for minimum 200 ft |
| **Shutdown sequence** | All steps in correct order; engine cooled before cutoff; battery last switch off |
| **EPs recitation** | Recite "Engine Failure" and "Hot Start" boldface procedures correctly before debrief signoff |

> **IP Discretion:** A student who commits a **hot start** without immediate abort action, or who advances the throttle to FLY with collective NOT at the bottom, will receive a **Task Failure** for that element and must repeat it before progressing to Event 3.

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| Throttle advanced before ~15% N1 | Hot start — excessive EGT spike; potential engine damage | Enforce: count N1 up to 15% before touching throttle. Say "fifteen percent" aloud |
| Forgetting fuel valve or boost pump | No light-off; wasted start attempt and starter duty cycle | Mnemonic: **"Fuel First"** — Fuel Valve → Boost Pump before starter |
| Advancing throttle to FLY with collective up | Unexpected thrust — aircraft becomes light on skids or lifts off uncontrolled | Enforce: collective FULL DOWN before touching idle stop release. Verify by feel before every FLY advancement |
| Governor ON before engine stabilized | Governor may hunt or overshoot Nr during stabilization | Wait for N1 stable at 58–62% before engaging governor |
| Jerky collective during hover | Altitude oscillations; pilot-induced oscillation develops | Smooth, incremental inputs; wait for aircraft response before correcting |
| Insufficient left pedal during hover pick-up | Nose yaws right; heading lost | Anticipate torque with left pedal as collective rises; pre-position pedal before the yaw starts |
| Looking directly below during hover taxi | Loss of spatial awareness; over-controlling | Eyes on a distant reference; anticipate corrections earlier |
| Not cooling engine before shutdown throttle cutoff | Thermal stress to turbine components | Follow 1–2 minute idle cool-down before closing throttle |

---

*Based on TM 55-1520-210-10, TM 55-1520-210-CL, TC 3-04.4, and Eagle Dynamics / Belsimtek DCS UH-1H Huey module documentation. For simulation use only.*
