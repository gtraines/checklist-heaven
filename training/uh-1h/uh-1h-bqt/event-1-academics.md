# Event 1 — Aircraft Systems & Academics

> **Course:** UH-1H Huey Basic Qualification Training | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [The UH-1H — Aircraft Overview](#the-uh-1h--aircraft-overview)
3. [Powerplant — T53-L-13B Turboshaft Engine](#powerplant--t53-l-13b-turboshaft-engine)
4. [Rotor System](#rotor-system)
5. [Transmission System](#transmission-system)
6. [Fuel System](#fuel-system)
7. [Hydraulic System](#hydraulic-system)
8. [Electrical System](#electrical-system)
9. [Force Trim System](#force-trim-system)
10. [Rotary-Wing Aerodynamics](#rotary-wing-aerodynamics)
11. [Cockpit Orientation](#cockpit-orientation)
12. [Operating Limitations — Quick Reference](#operating-limitations--quick-reference)
13. [Boldface Emergency Procedures](#boldface-emergency-procedures)
14. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Describe the T53-L-13B turboshaft engine operating cycle, correlator/governor system, start sequence, and all engine limitations (continuous, transient, starting)
- [ ] Explain the two-blade, semi-rigid (teetering) main rotor system, stabilizer bar function, teetering hinge dynamics, Nr governing range, and autorotation RPM range
- [ ] Identify transmission system components (main gearbox, freewheeling unit, tail rotor driveshaft and gearbox) and state torque, oil temperature, and oil pressure limits
- [ ] Describe the fuel system architecture, capacity, boost pump function, and low-fuel warnings
- [ ] Explain the single hydraulic system, what it powers, and the flight characteristics when hydraulics are lost
- [ ] Describe the electrical system (DC starter-generator, battery, inverter, bus architecture) and state battery endurance with generator offline
- [ ] Explain the throttle correlator and governor interaction, recognize governor failure indications, and describe manual throttle management technique
- [ ] Describe the force trim (magnetic brake) system and its operation
- [ ] Define and explain the following aerodynamic phenomena specific to the UH-1H: translating tendency, ETL, transverse flow effect, dissymmetry of lift, retreating blade stall, ground effect (IGE vs. OGE), settling with power (vortex ring state), LTE, mast bumping (with emphasis on the teetering rotor), pendular action, and dynamic rollover
- [ ] Locate and identify all major cockpit panels, instruments, and caution lights by name and position
- [ ] Recite all critical operating limitations from memory (EGT, Nr, torque, oil P&T, Vne)
- [ ] Recite all boldface emergency procedures verbatim, in sequence, without reference to notes

---

## The UH-1H — Aircraft Overview

| Characteristic | Value |
|---|---|
| **Type** | Single-engine medium utility helicopter |
| **Manufacturer** | Bell Helicopter Textron |
| **Engine** | Lycoming T53-L-13B turboshaft |
| **Main Rotor** | 2-blade, semi-rigid (teetering); 48 ft diameter |
| **Tail Rotor** | 2-blade, semi-rigid; 8.5 ft diameter; left side of tail boom |
| **Max Gross Weight** | 9,500 lbs |
| **Vne (Sea Level)** | 124 KIAS (decreases with altitude and weight) |
| **Crew** | Pilot (right seat) + Copilot (left seat) |
| **Primary Mission** | Utility transport, medevac, light attack |
| **DCS Module** | Belsimtek / Eagle Dynamics — full-fidelity, clickable cockpit, AFM |

The UH-1H is a **single-engine helicopter**. Engine failure procedures must be automatic and immediate. In a low-altitude engine failure, the time from loss of power to unrecoverable Nr decay can be as little as 2–3 seconds. Boldface drills are not optional.

> **Key Training Emphasis — Analog Cockpit:** The UH-1H has no MFDs, no GPS, no digital displays, and no FADEC. The pilot monitors individual steam gauges for all engine health, navigates via ADF/VOR/dead reckoning, and manually manages engine RPM via the correlator and governor. This demands a disciplined instrument scan and higher procedural workload than any glass-cockpit DCS aircraft.

---

## Powerplant — T53-L-13B Turboshaft Engine

### Engine Type and Architecture

The UH-1H is powered by a single **Lycoming T53-L-13B** turboshaft engine producing 1,400 shaft horsepower (SHP). It is a **free-turbine design**: the gas producer section (N1) is mechanically independent of the power turbine (N2). This means the rotors can spin freely in autorotation while the engine is at idle or zero output — the freewheeling unit decouples them.

### Engine Operating Parameters

| Parameter | Value | Notes |
|---|---|---|
| **Rated Power** | 1,400 SHP | Maximum at sea level, standard day |
| **Max Continuous Power** | ~1,100 SHP | Corresponds to ~40 PSI torque at sea level |
| **Gas Producer (N1)** | Idle: ~58–62% / Max: ~100% | Responds to fuel flow via correlator |
| **Power Turbine RPM (N2)** | 100% = 6,600 RPM | Drives rotor at 324 RPM through main gearbox |
| **Rotor RPM (Nr)** | Normal: 324 ±3 RPM | Dual tachometer shows Nr and N2 together |
| **EGT Continuous Max** | 610°C | Primary engine health indicator |
| **EGT Transient (5 sec)** | 625°C | Brief exceedance only |
| **EGT Starting Limit (10 sec)** | **720°C** | Exceed this during start → HOT START; throttle CLOSED immediately |
| **Engine Oil Pressure** | 35–70 PSI normal | < 35 PSI = caution; < 25 PSI = warning |
| **Engine Oil Temperature** | < 107°C | > 107°C = land as soon as practicable |

### Throttle Correlator and Governor System

The UH-1H does **not** have a FADEC. RPM management uses a two-part mechanical/hydromechanical system:

**1. Throttle Correlator** — "rough trim" for RPM:
- Mechanical linkage between the collective lever and the engine fuel control.
- Automatically increases/decreases fuel flow proportionally as the pilot raises/lowers collective.
- Provides approximate compensation only — not precise enough to hold Nr within limits alone.

**2. Governor** — "fine trim" for RPM:
- Hydromechanical device that senses Nr and makes fine adjustments to fuel flow to hold 324 RPM.
- Acts on top of the correlator, correcting the error between approximate and exact fuel flow.
- Enabled by the **GOV switch** on the overhead console — must be ON for normal flight.

**Combined operation:** Raise collective → correlator opens fuel roughly → governor fine-tunes to hold 324 RPM. Continuous, automatic when functioning normally.

| Mode | Correlator | Governor | Pilot Throttle Required | Nr Management |
|---|---|---|---|---|
| **Normal (GOV ON)** | Active | Active | None normally | Automatic — 324 RPM maintained |
| **Governor OFF / Failed** | Active | Inactive | Must actively twist to maintain Nr | Pilot responsibility — continuous monitoring |

> *⚠ Realism Divergence: Real FCU malfunctions can present as partial authority loss or intermittent hunting — more nuanced than the DCS clean "governor off." DCS also does not enforce the 60-second starter duty cycle limit (real: max 60 sec crank, 2-min cooldown between attempts).*

### Engine Start Sequence

| Step | Action | Key Indication |
|---|---|---|
| 1 | Battery ON, Inverter ON | Caution panel illuminates normally |
| 2 | Fuel Valve ON, Boost Pump ON | FUEL BOOST caution extinguishes |
| 3 | Throttle CLOSED, Collective full down | Fuel cutoff confirmed |
| 4 | Hold Starter Button (`LShift + Home`) | N1 begins rising from 0% |
| 5 | At ~15% N1 → Throttle to IDLE (mouse wheel CW on grip) | Fuel introduced to combustion |
| 6 | EGT rises → light-off confirmed | 200–400°C at light-off |
| 7 | Monitor EGT — must not exceed **720°C** | Continuous monitoring required |
| 8 | N1 accelerates to 58–62% (ground idle) | Rotor begins spinning up |
| 9 | Release Starter Button | Starter disengages |
| 10 | Stabilize at ground idle 30–60 sec | EGT settles, oil pressure rises |

### Start Abort Criteria

| Condition | Recognition | Action |
|---|---|---|
| **Hot Start** | EGT exceeds 720°C | Throttle to CLOSED immediately; motor 30 sec to purge; wait 2 min |
| **Hung Start** | N1 stagnates below ~55% with rising EGT | Throttle to CLOSED; motor to clear; check battery and fuel supply |
| **No Light-Off** | No EGT rise by ~25% N1 | Throttle to CLOSED; motor to purge; check fuel valve and boost pump |

---

## Rotor System

### Main Rotor

| Parameter | Value | Notes |
|---|---|---|
| **Configuration** | 2-blade, semi-rigid (teetering) | Defining UH-1H characteristic |
| **Diameter** | 48 ft (14.63 m) | |
| **Nr (Power On)** | 324 ±3 RPM (6,600 N2) | Governor maintains; dual tach shows Nr + N2 |
| **Nr (Autorotation)** | 294–324 RPM | Min 294 RPM for safe autorotation flare/cushion |
| **Nr Low Warning** | Audio tone + RPM caution light at ~294 RPM | Immediate: lower collective OR increase throttle |
| **Nr Overspeed** | > 345 RPM | Structural risk — mast and blade root stress |
| **Rotor Direction** | Counterclockwise viewed from above | Determines translating tendency and tail rotor requirements |

### Teetering Rotor — Key Characteristics

The two-blade teetering rotor is the most safety-critical system characteristic of the UH-1H:

- **Teetering hinge:** Both blades are rigidly connected; the entire rotor head pivots on a single hinge. One blade goes up, the other goes down. This is the flapping mechanism.
- **No individual flapping or lead-lag hinges:** Unlike 3+ blade fully articulated systems, all flapping is symmetric.
- **Underslung rotor:** Hub mounted slightly below the teeter axis — reduces Coriolis-induced lead-lag forces.
- **Stabilizer bar (Bell bar):** Weighted bar at 90° to the blades, acting as a mechanical gyroscope. Resists disc attitude changes, smooths gusty inputs, and adds a slight lag (~0.5–1 sec) to cyclic response. In DCS this is modeled — controls feel more sluggish than helicopters without a stabilizer bar (e.g., Mi-24, Ka-50).

### Mast Bumping — **CRITICAL HAZARD**

> **This is the most dangerous condition unique to the teetering rotor. There is no recovery once the mast is struck.**

**Mechanism:**
1. Low-G or negative-G unloads the rotor disc.
2. With the disc unloaded, the teetering hinge can flap to its mechanical stops.
3. If cyclic is displaced while unloaded, the rotor head contacts the mast.
4. Mast contact → **mast separation → immediate catastrophic loss of aircraft.**

**Critical triggers:** Abrupt forward cyclic pushover, aggressive bunting, turbulence at light weight, wake turbulence, aggressive sideslip correction.

**Prevention rules (memorize):**
1. **Never push forward cyclic aggressively** — especially at low airspeed or in turbulence.
2. **Maintain positive G at all times.**
3. **If low-G is sensed:** Apply gentle aft cyclic to reload the disc. Do NOT apply lateral cyclic.
4. **In autorotation:** Do not push the nose over aggressively during entry.

> *⚠ Realism Divergence: DCS models mast bumping and can destroy the aircraft. Real UH-1H mast bumping can occur with as little as a 0.5G reduction from 1G with cyclic displacement — the margin is narrower than DCS may suggest.*

### Tail Rotor

| Parameter | Value | Notes |
|---|---|---|
| **Configuration** | 2-blade, semi-rigid | Left side of tail boom (viewed from behind) |
| **Diameter** | 8.5 ft (2.59 m) | |
| **Function** | Anti-torque and yaw control | Left pedal = more tail rotor thrust (nose left); right pedal = less (nose right) |
| **Drive** | Driveshaft through 42° and 90° gearboxes | Loss of drive = loss of anti-torque |

---

## Transmission System

| Component | Function | Key Limits |
|---|---|---|
| **Main Transmission (42° Gearbox)** | Reduces 6,600 engine RPM to 324 rotor RPM; also drives tail rotor driveshaft, hydraulic pump, generator, and accessories | Torque: ≤40 PSI continuous |
| **Tail Rotor Driveshaft** | Transmits power from main transmission to tail rotor gearbox | Vibration or unusual noise = possible impending failure |
| **Tail Rotor Gearbox (90°)** | Converts driveshaft rotation to tail rotor rotation | Oil level, chip detector |
| **Freewheeling Unit (Sprag Clutch)** | Decouples engine from rotor when Nr > N2 — allows free-spinning rotor in autorotation | Must disengage cleanly; failure to disengage means engine drag slows rotor |

### Transmission Limits

| Parameter | Normal | Caution | Warning |
|---|---|---|---|
| **Torque (Q)** | ≤40 PSI continuous | 40–48 PSI (30-min limit) | >50 PSI structural limit |
| **Trans Oil Pressure** | 30–70 PSI | <30 PSI | XMSN OIL PRESS caution |
| **Trans Oil Temperature** | <110°C | 110–120°C | >120°C = land immediately |
| **Chip Detector** | Clear | — | CHIP DET light = land as soon as possible |

> **Torque Note:** Unlike modern helicopters displaying torque as a percentage, the UH-1H torque gauge reads in **PSI**. The student must memorize the PSI limits — there is no "100%" reference marked as the continuous limit.

---

## Fuel System

| Parameter | Value | Notes |
|---|---|---|
| **Internal Fuel Capacity** | ~210 US gal (~1,390 lbs JP-8) | Crashworthy, self-sealing cells under cabin floor |
| **Fuel Boost Pump** | Electric, overhead console | Must be ON before start and during all flight |
| **Fuel Quantity Indicator** | Pounds — instrument panel | Single gauge; less accurate at low fuel states |
| **Low Fuel Warning** | Caution light at ~200 lbs remaining | ~40–50 min at cruise; plan recovery immediately |
| **Fuel Consumption (Hover IGE)** | ~300–350 lbs/hr | Sea level, mid gross weight |
| **Fuel Consumption (Cruise ~90 KIAS)** | ~220–260 lbs/hr | Sea level, mid gross weight |

**Critical rules:** Always confirm boost pump ON before start. Monitor fuel quantity — there is no automated fuel management. Plan for a minimum 20-minute reserve.

---

## Hydraulic System

| Parameter | Value | Notes |
|---|---|---|
| **Configuration** | Single system; no backup | Loss of hydraulics = significantly heavier controls, not loss of control |
| **Pump** | Engine-driven via main transmission | Operates whenever rotor is turning |
| **Function** | Powers flight control servo actuators (cyclic, collective, pedals) | |

**Hydraulic failure flight characteristics:**
- Cyclic becomes very heavy — can require 40–50 lbs of force for inputs.
- Collective becomes heavy but manageable.
- Pedals become heavy.
- **Recommended technique:** Fly at 60–80 KIAS (most manageable control forces); execute a **run-on landing** — avoid hover, which is exhausting and dangerous without hydraulics.

---

## Electrical System

| Component | Description |
|---|---|
| **DC Starter-Generator** | 28V DC, 200 amp — serves as starter during engine start, then as generator |
| **Main Battery** | 24V nickel-cadmium — emergency backup; ~30 min endurance under normal electrical load |
| **AC Inverter** | Converts 28V DC to 115V AC (400 Hz) — powers attitude indicator, heading gyros, some radio components |
| **Essential Bus** | Powered whenever battery is ON — caution panel, fire warning, critical instruments |
| **Non-Essential Bus** | Generator-powered — avionics, lighting; shed-able in emergency |

**Startup power sequence:**
1. **Battery ON** → Essential bus powered; caution panel illuminates (normal)
2. **Inverter ON** → AC power for gyro instruments (allow 2–3 min to stabilize)
3. **Engine start** → Starter-generator draws high current
4. **Post-start Generator ON** → Generator takes over bus; battery begins charging; GEN caution extinguishes
5. **Generator failure** → GEN caution illuminates; battery provides ~30 min backup; shed non-essential loads; land as soon as practicable

**DCS Keybinds:**

| Function | Key |
|---|---|
| Battery ON/OFF | `LShift + B` |
| Generator ON/OFF | `LShift + G` |
| Inverter ON/OFF | `LShift + I` |

---

## Force Trim System

The UH-1H uses a **magnetic brake force trim system** — fundamentally different from electric trim or trim tabs:

- **Electromagnetic brakes** hold cyclic and pedals at whatever position the pilot sets.
- To change trim: press and hold **Force Trim Release** (cyclic grip button, `T` key in DCS), reposition controls, release the button. Brakes re-engage and hold the new position.
- **Out-of-trim forces:** If flight conditions change without re-trimming, the magnetic brakes resist, creating stick forces the pilot must work against.
- **Trimming cadence:** Must re-trim with every significant change in airspeed, power, altitude, or configuration. Higher workload than electric trim systems.

| Control | Trim Type | Notes |
|---|---|---|
| **Cyclic (lateral and longitudinal)** | Magnetic brake | Re-trim with every speed/power change |
| **Pedals** | Magnetic brake | Pedal trim changes with power/torque changes |
| **Collective** | Friction adjustment | Pilot sets desired friction resistance manually |

**DCS Keybinds:**

| Function | Key |
|---|---|
| Force Trim Release (hold) | `T` |
| Set Force Trim (latch position) | `LCtrl + T` |

> The UH-1H has **no SAS/SCAS**. All stability is from rotor dynamics, the stabilizer bar, and pilot input. Workload is higher than SAS-equipped helicopters (Mi-24P, Ka-50).

---

## Rotary-Wing Aerodynamics

### Translating Tendency (Left Drift in Hover)

In hover, tail rotor thrust pushes the aircraft right. To compensate, the rotor disc tilts slightly left. Compensation is imperfect — the UH-1H has a natural **left drift tendency** in hover requiring constant right cyclic. This is normal and expected.

### Effective Translational Lift (ETL)

As the helicopter accelerates through **~16–24 KIAS**, the rotor enters undisturbed air and lift efficiency increases markedly.

| Phase | Airspeed | Pilot Indications | Required Inputs |
|---|---|---|---|
| ETL onset (accelerating) | ~16–24 KIAS | Aircraft "gets light," nose pitches up, left yaw tendency | Forward cyclic, slight right pedal, minor collective reduction |
| Below ETL (decelerating) | <16–24 KIAS | Aircraft "gets heavy," power demand increases | More collective needed; more left pedal for increased torque |

### Transverse Flow Effect

At ~10–20 KIAS, the aft rotor disc produces more downwash than the forward disc, causing a lateral vibration and slight roll tendency. Correct with lateral cyclic as needed. Brief and self-limiting.

### Dissymmetry of Lift

In forward flight, the advancing blade (right side) sees higher airspeed than the retreating blade (left). The teetering hinge equalizes lift: advancing blade flaps up (reducing AoA), retreating blade flaps down (increasing AoA). Because both blades are rigidly connected, flapping is symmetric.

### Retreating Blade Stall

At high airspeeds, the retreating blade cannot increase AoA enough to produce equal lift, and it stalls. The teetering rotor is **more susceptible** than fully articulated systems due to fewer blades sharing the load.

**Symptoms:** 2-per-rev vibration becoming irregular; uncommanded pitch-up and/or left roll; heavy stick forces.

**Recovery:** Reduce airspeed (aft cyclic), reduce collective (lower blade loading), reduce G-load, descend to lower altitude.

| Factor | Effect on Vne |
|---|---|
| Increased altitude | Vne **decreases** |
| Increased gross weight | Vne **decreases** |
| Increased G-load (steep turns) | Effective Vne **decreases** |

### Ground Effect (IGE vs. OGE)

| Condition | Height | Performance Impact |
|---|---|---|
| **In Ground Effect (IGE)** | Within ~24 ft AGL (½ rotor diameter) | ~10–15% less torque required vs. OGE |
| **Out of Ground Effect (OGE)** | Above ~24 ft AGL | Maximum power required for hover |

A UH-1H that can hover IGE may **not** be able to hover OGE at the same weight. Always verify OGE hover capability before committing to pinnacle, confined area, or slope departures.

### Settling with Power (Vortex Ring State)

**Entry conditions (all three must be present simultaneously):**
- Airspeed below ~30 KIAS
- Rate of descent > ~300 fpm
- Moderate to high power applied (attempting to arrest the descent)

**Recognition:** High rate of descent that does NOT respond to collective; aircraft shuddering; random pitch/roll excursions.

**Recovery:** Aggressively apply forward cyclic to gain airspeed above 30 KIAS and fly out of the vortex. Momentarily reduce collective to break the vortex. Only then arrest descent normally.

### Loss of Tail Rotor Effectiveness (LTE)

Three critical wind azimuth regions:

| Wind Azimuth (Relative) | Mechanism | Risk |
|---|---|---|
| **285°–315°** (left rear quarter) | Main rotor vortex blown into tail rotor disc | Turbulent, reduced anti-torque effectiveness |
| **120°–240°** (rear half) | Weathercock instability — wind pushes tail, aircraft yaws into wind | Common hover LTE scenario |
| **210°–330°** (left rear arc) | Tail rotor vortex ring state — tailwind causes tail rotor to enter its own VRS | Sudden uncommanded right yaw, little warning |

**Recovery:** Forward cyclic to gain airspeed — speed cures LTE. If altitude permits, reduce collective to reduce torque demand. **Do not** add excessive left pedal if tail rotor is in vortex ring state.

### Mast Bumping

*(See [Rotor System — Mast Bumping](#mast-bumping----critical-hazard) above.)*

### Dynamic Rollover

Occurs when the helicopter pivots around a ground contact point (one skid, an obstacle) and develops a roll rate exceeding ~10°/sec — at which point full opposite cyclic cannot stop the roll.

**Prevention:** During slope landings and liftoffs, keep upslope skid on the ground as long as possible. If roll begins during liftoff, **lower collective** (if below 10°/sec roll rate). Never allow a steady roll rate to develop near the ground.

### Pendular Action

The fuselage hangs below the rotor like a pendulum and swings during attitude changes. Over-correcting amplifies the swing. **Correction:** Make small, smooth inputs; wait for the aircraft to stabilize before correcting again. In hover, this is where pilot-induced oscillation most commonly develops.

---

## Cockpit Orientation

### Panel Locations

| Panel | Location | Key Contents |
|---|---|---|
| **Overhead Console** | Above both crew members | Battery, Generator, Inverter, Fuel Valve, Boost Pump, Governor (GOV), Starter, RPM Warning, Pitot Heat, De-ice, Caution Light Test |
| **Main Instrument Panel — Pilot (Right)** | Forward right | Flight instruments (AI, ASI, ALT, VSI, DG, T&S), Radar Altimeter |
| **Main Instrument Panel — Engine (Center)** | Forward center | Torque (PSI), EGT (°C), N1 (%), Dual Tach (Nr/N2), Engine Oil P/T, Trans Oil P/T, Fuel Qty |
| **Caution/Advisory Panel** | Instrument panel — center-left | MASTER CAUTION, RPM, GEN, GOV EMER, FUEL BOOST, CHIP DET, XMSN OIL, ENG OIL, FIRE |
| **Center Pedestal** | Between seats | AN/ARC-134 (VHF-AM), AN/ARC-51BX (UHF-AM), AN/ARC-131 (FM), Transponder, Audio Panels |
| **Pilot's Subpanel (Right Lower)** | Below pilot's instruments | Circuit breakers (pilot side), armament panel (if equipped) |

### Engine Instruments — Priority Reference

| Instrument | Display | Normal Range | Never Exceed |
|---|---|---|---|
| **Torque** | PSI | <40 PSI continuous | >50 PSI |
| **EGT** | °C | <610°C | 720°C (start), 625°C (5 sec transient) |
| **N1** | % | 58–100% | >101% |
| **Dual Tach (Nr/N2)** | RPM | 321–327 RPM (needles married) | <294 or >345 RPM |
| **Engine Oil Pressure** | PSI | 35–70 PSI | <25 PSI |
| **Engine Oil Temperature** | °C | <107°C | >120°C |
| **Trans Oil Pressure** | PSI | 30–70 PSI | XMSN OIL PRESS caution |
| **Trans Oil Temperature** | °C | <110°C | >120°C |

### Instrument Scan Pattern (Radial Scan)

```
        ASI ←── AI ──→ ALT
                │
         T&S ←──┼──→ VSI
                │
               DG
```

Always return to the AI between each instrument. In VFR flight, the outside horizon is the primary attitude reference; the instruments are the cross-check.

### Dual Tachometer — Split Needle Indications

| Indication | Meaning |
|---|---|
| Needles **married** (overlapping) at 324 RPM | Normal — engine driving rotor at governed speed |
| **Nr higher than N2** | Engine not keeping up; possible governor failure or power loss |
| **Nr and N2 split with Nr falling** | Engine failure or freewheeling unit engaged — enter autorotation |
| **Nr higher than N2 (autorotation)** | Normal in autorotation — rotor freewheeling, engine disconnected |

### Caution Panel Lights

| Light | Meaning | Immediate Action |
|---|---|---|
| **MASTER CAUTION** | A system caution has illuminated | Check individual lights; press to reset after acknowledging |
| **RPM** | Nr below ~294 RPM or governor issue | Check Nr; adjust throttle/collective; check GOV switch |
| **GEN** | Generator failure | Check GEN switch; shed non-essential loads; ~30 min on battery |
| **GOV EMER** | Governor malfunction | Switch to manual throttle if not governing |
| **FUEL BOOST** | Boost pump off or fuel pressure low | Check BOOST PUMP switch; gravity feed available in level flight |
| **CHIP DET** | Metallic particles in oil | Land as soon as possible |
| **ENGINE OIL PRESS** | Oil pressure <35 PSI | Reduce power; land as soon as practicable |
| **XMSN OIL PRESS** | Trans oil pressure <30 PSI | Land as soon as possible; transmission failure risk |
| **FIRE** | Fire detected in engine compartment | Execute engine fire boldface immediately |

### Radio Stack (Center Pedestal, Top to Bottom)

| Radio | Designation | Band | Primary Use | Transmit Key |
|---|---|---|---|---|
| **VHF-AM** (top) | AN/ARC-134 | 116.0–149.975 MHz | ATC, tower, ground, ATIS | `V` |
| **UHF-AM** (middle) | AN/ARC-51BX | 225.0–399.975 MHz | Military ATC, GUARD (243.0 MHz) | `Y` |
| **FM** (bottom) | AN/ARC-131 | 30.0–75.975 MHz | Tactical, ground forces, SRS nets | `C` |

All radios are **manually tuned via rotary knobs** in DCS (left-click increase, right-click decrease, scroll wheel fine adjust). No digital frequency presets on VHF or FM. UHF has 20 preset channels plus manual mode.

---

## Operating Limitations — Quick Reference

### Engine Limits

| Parameter | Normal | Caution | Limit |
|---|---|---|---|
| **EGT** | <610°C | 610–625°C (5 sec) | **720°C** starting (10 sec) |
| **N1** | 58–100% | — | >101% |
| **Nr** | 321–327 RPM | 294–321 / 327–339 | <294 or >345 RPM |
| **Torque** | <40 PSI | 40–48 PSI (time-limited) | >50 PSI |
| **Engine Oil Pressure** | 35–70 PSI | <35 PSI | <25 PSI |
| **Engine Oil Temperature** | <107°C | 107–120°C | >120°C |
| **Trans Oil Pressure** | 30–70 PSI | <30 PSI | XMSN OIL PRESS light |
| **Trans Oil Temperature** | <110°C | 110–120°C | >120°C |

### Aircraft Limits

| Parameter | Limit | Notes |
|---|---|---|
| **Max Gross Weight** | 9,500 lbs | |
| **Vne** | 124 KIAS | Sea level; decreases with altitude, weight, G |
| **Low-G / Pushovers** | **PROHIBITED** | Teetering rotor — mast bumping risk |
| **LTE Risk Window** | Wind 210°–330° relative | Most dangerous in low-speed hover |

### V-Speeds

| Speed | Value | Usage |
|---|---|---|
| **Vy (Best Rate of Climb)** | 60 KIAS | Normal climb |
| **Best Range Cruise** | ~100 KIAS | Maximum distance per pound of fuel |
| **Normal Cruise** | 90–100 KIAS | Transit operations |
| **Autorotation Best Glide** | 65 KIAS | Maximum range in autorotation |
| **Vne** | 124 KIAS | Never exceed (sea level) |

---

## Boldface Emergency Procedures

Boldface procedures are memory items — executed without reference to a checklist. They must be recited verbatim.

### Engine Failure (Unintended Power Loss)

> *Execute immediately. Every second of delay costs rotor RPM.*

1. **Collective** — LOWER (immediately — enter autorotation; do not hesitate)
2. **Throttle** — Confirm IDLE or as required
3. **Nr** — Maintain 294–324 RPM (adjust collective as needed)
4. **Airspeed** — Establish **65 KIAS** (best glide)
5. **Mayday** — Transmit if time permits
6. **Landing area** — Select immediately
7. **At ~40 ft AGL** — Flare (aft cyclic) to reduce airspeed and rate of descent
8. **At ~8–10 ft AGL** — Level aircraft; collective up to cushion touchdown

### Engine Fire in Flight

1. **Throttle** — CLOSED (fuel cutoff position, full CCW)
2. **Fuel Valve** — OFF (`LShift + F`)
3. **Boost Pump** — OFF (`LCtrl + B`)
4. **Land** — IMMEDIATELY (do not attempt to restart)

### Engine Fire on Ground (During Start)

1. **Throttle** — CLOSED
2. **Starter Button** — HOLD (motor to purge)
3. **Fuel Valve** — OFF (`LShift + F`)
4. **Boost Pump** — OFF (`LCtrl + B`)
5. **Battery** — OFF (`LShift + B`)
6. **Evacuate** aircraft

### Low RPM (Nr Warning Tone / RPM Caution)

1. **Collective** — LOWER (reduce power demand immediately)
2. **Nr** — Check on dual tachometer
3. **Throttle** — Advance as required (increase fuel flow)
4. **Governor** — Verify ON (`LCtrl + Home`)
5. If Nr continues to fall → initiate **autorotation**

### Tail Rotor Failure (Loss of Anti-Torque)

**Complete loss of tail rotor drive:**
1. **Collective** — LOWER (reduce torque immediately; reduces yaw tendency)
2. **Autorotate** — enter immediately; the rotor will align with the wind during descent
3. **Land** — straight-ahead if altitude is insufficient; no hover possible

**Tail rotor stuck (pedals bound / no yaw response):**
1. Maintain **60–70 KIAS** (vertical fin provides directional stability above ~30 KIAS)
2. Perform a **run-on landing** — do not hover
3. Reduce power smoothly as airspeed bleeds; accept heading deviation during rollout

### Governor Failure (GOV EMER Light or Loss of RPM Control)

1. **Manual throttle** — Take immediate control with twist-grip
2. **Governor switch** — OFF (`LCtrl + Home`) (prevent conflicting inputs)
3. **Nr** — Maintain 321–327 RPM manually; adjust throttle with every collective change
4. **Land** — as soon as practicable; manual throttle is high workload

### Hydraulic Failure

1. **HYD caution light** — note
2. **Airspeed** — Establish **60–80 KIAS** (most manageable control forces)
3. **Avoid hovering** — if hover is required, expect heavy controls and rapid pilot fatigue
4. **Land** — **run-on landing** preferred; approach and land without coming to a hover

---

## Completion Standards

This is a **ground event** — no simulator time required. Completion standards are oral/written:

- [ ] **Engine Limits:** State all EGT, N1, Nr, torque, oil pressure, and temperature limits from memory without reference. Zero errors permitted on EGT starting limit (720°C) and Nr low warning (294 RPM).
- [ ] **Correlator/Governor:** Explain the difference between correlator and governor; describe what happens when the governor fails; describe correct manual throttle technique.
- [ ] **Mast Bumping:** Describe the mechanism, list three triggering scenarios, and state the prevention rules without reference.
- [ ] **Aerodynamics:** Define and explain ETL, LTE, settling with power, retreating blade stall, and dynamic rollover. State recovery procedures for each.
- [ ] **Cockpit:** Locate and identify by name all instruments, caution lights, and major switches in the cockpit orientation diagram without reference.
- [ ] **Boldface EPs:** Recite all boldface emergency procedures verbatim and in correct sequence, without notes, within a reasonable pace. Self-corrections permitted on first repetition; zero errors on final evaluation.
- [ ] **V-Speeds and Aircraft Limits:** State Vne, autorotation airspeed, and max gross weight from memory.

> **Instructor Note:** Do not allow the student to progress to Event 2 until boldface EPs are verbatim-correct and engine limits are solid. A student who hesitates on "lower collective" for engine failure during Event 7 will lose rotor RPM before correcting. The time to learn this is now.

---

*Based on TM 55-1520-210-10, TM 55-1520-210-CL, TC 3-04.4, FM 1-240, and Eagle Dynamics / Belsimtek DCS UH-1H Huey module documentation. For simulation use only.*
