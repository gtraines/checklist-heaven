# UH-1H Iroquois "Huey" — Basic Qualification Training Research Dossier

> **Aircraft:** Bell UH-1H Iroquois ("Huey") | **Role:** Utility Transport Helicopter
> **Course Level:** Basic Qualification (Level 100)
> **Primary Reference:** TM 55-1520-210-10 (Operator's Manual), TM 55-1520-210-CL (Checklists)
> **Supplementary References:** AR 95-1 (Flight Regulations), TC 3-04.4 (Fundamentals of Flight), FM 1-240 (Utility and Cargo Helicopter Operations)
> **DCS Module:** Belsimtek / Eagle Dynamics UH-1H Huey — Full-fidelity, clickable cockpit module. Every switch, dial, circuit breaker, and instrument is interactive. The module uses an advanced flight model (AFM) providing realistic rotor dynamics, autorotation, and retreating blade stall behavior. This was one of the first high-fidelity helicopter modules released for DCS World.

---

## Overview

### Purpose

This document is the technical research foundation for a UH-1H Iroquois Basic Qualification Training (BQT) course in DCS World. It compiles systems knowledge, aerodynamic data, cockpit procedures, and emergency procedures into a single reference that will be converted into structured training events and checklists.

### Scope

**Covered:** Cold-and-dark startup through safe aircraft recovery in day VMC conditions — including hover work, basic flight maneuvers, radio communications, analog radio-aid navigation, traffic pattern operations, emergency procedures (academic and practice autorotations), and shutdown.

**Not Covered:** Weapons employment (door guns, rocket pods), sling load operations, NVG operations, tactical flight (NOE/contour/low-level), multi-ship formations, or instrument flight procedures. Weapons panels and armament switches are identified at a familiarization level only. Sling load and cargo hook controls are identified but not employed.

### Aircraft Background

The Bell UH-1H Iroquois — universally known as the "Huey" — is a single-engine, medium utility helicopter that became the iconic aircraft of the Vietnam War and one of the most produced helicopters in history. First flown in 1956 as the XH-40 and entering U.S. Army service in 1959, the UH-1 series evolved through numerous variants. The UH-1H, introduced in 1967, was the definitive utility model, featuring the upgraded Lycoming T53-L-13B turboshaft engine producing 1,400 shaft horsepower.

The UH-1H's most distinctive feature is its **two-blade, semi-rigid (teetering) main rotor system**. This design — inherited from early Bell helicopter technology — produces the characteristic low-frequency "Huey thump" blade slap and has specific handling qualities that differ significantly from fully articulated rotor systems. The teetering rotor is mechanically simple and reliable, but is susceptible to **mast bumping** under low-G or negative-G conditions, making this a critical training emphasis.

The cockpit is **fully analog** — there are no digital displays, MFDs, glass instruments, or computerized navigation systems. All engine monitoring, flight reference, and navigation is performed via steam gauges and manually tuned analog radios. The pilot navigates using ADF, VOR/ILS, and dead reckoning rather than GPS or digital waypoints. This represents a fundamentally different operating environment from modern glass-cockpit helicopters and demands thorough instrument scan discipline and manual radio management skills.

The UH-1H served with the U.S. Army, Marine Corps, Air Force, and over 40 allied nations. While largely retired from U.S. frontline service (replaced by the UH-60 Black Hawk), the Huey remains in service worldwide and continues to fly in civilian, law enforcement, and firefighting roles.

### Analog Cockpit — Key Training Emphasis

The absence of digital systems means the student must develop skills that are not required in glass-cockpit aircraft:

| Skill | Why It Matters |
|---|---|
| **Analog instrument scan** | No EICAS, no caution advisory computer — the pilot must visually scan each gauge individually using a radial scan pattern |
| **Manual radio tuning** | Three radios (VHF-AM, UHF-AM, FM) tuned by physical frequency knobs — no preset digital channels, no frequency recall |
| **Radio-aid navigation** | ADF bearing pointer and VOR CDI are the primary navigation tools — no GPS, no moving map, no waypoints |
| **Engine health monitoring** | Individual analog gauges for EGT, torque, N1, Nr/N2, oil pressure/temperature — the pilot is the engine monitor |
| **Throttle/RPM management** | Correlator + governor (no FADEC) — the pilot must understand the mechanical relationship and be ready for manual throttle |

### Primary Real-World Sources

| Source | Description |
|---|---|
| TM 55-1520-210-10 | Operator's Manual — systems, limitations, normal/emergency procedures |
| TM 55-1520-210-CL | Operator's and Crewmember's Checklist — condensed procedures, boldface items |
| AR 95-1 | Army Flight Regulations — general operating rules |
| TC 3-04.4 | Fundamentals of Flight — rotary-wing aerodynamics, weather, ADM |
| FM 1-240 | Utility and Cargo Helicopter Operations — UH-1 doctrine and procedures |
| USAACE Training Circulars | Fort Rucker/Novosel training standards and maneuver descriptions |

### Source Priority Rule

Real-world documentation is the **primary truth** for systems knowledge, limitations, aerodynamic behavior, and procedural structure. Where the DCS Belsimtek module diverges from real-world procedures or behavior, **the DCS procedure is what the student will actually execute** and is documented as the primary instruction. All divergences are footnoted:

> *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

---

## Module 1: Aircraft Systems & Aerodynamics

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Describe the T53-L-13B turboshaft engine's operating cycle, throttle correlator/governor system, start sequence, and all engine limitations (continuous, transient, starting).
2. Explain the two-blade, semi-rigid (teetering) main rotor system, including the stabilizer bar, teetering hinge dynamics, Nr governing, and autorotation RPM range.
3. Identify the transmission system components (main gearbox, freewheeling unit, tail rotor driveshaft and gearbox) and state torque, oil temperature, and oil pressure limits.
4. Describe the fuel system architecture, capacity, boost pump function, and low-fuel warnings.
5. Explain the single hydraulic system, what it powers, and the flight characteristics when hydraulics are lost.
6. Describe the electrical system (DC starter-generator, battery, inverter, bus architecture) and state battery endurance with generator offline.
7. Explain the throttle correlator and governor interaction, recognize governor failure indications, and describe manual throttle management technique.
8. Describe the force trim (magnetic brake) system and its operation.
9. Define and explain the following rotary-wing aerodynamic phenomena specific to the UH-1H: translating tendency, translational lift (ETL), transverse flow effect, dissymmetry of lift, retreating blade stall, ground effect (IGE vs. OGE), settling with power, LTE, mast bumping (with special emphasis on the teetering rotor), pendular action, and dynamic rollover.

---

### 1.1 Powerplant — T53-L-13B Lycoming Turboshaft Engine

The UH-1H is powered by a single Lycoming T53-L-13B turboshaft engine. It is a **free-turbine design**: the gas producer section (N1) is mechanically independent of the power turbine (N2), which drives the main transmission and rotor system. The free-turbine architecture means the compressor and power turbine can operate at different speeds — critically important for autorotation, where the power turbine freewheels while the gas producer may be at zero output.

#### Engine Operating Parameters

| Parameter | Value | Notes |
|---|---|---|
| **Engine Type** | Lycoming T53-L-13B | Free-turbine turboshaft |
| **Rated Power** | 1,400 SHP (shaft horsepower) | Maximum at sea level, standard day |
| **Military Power (30-min)** | 1,400 SHP | Time-limited; used for takeoff and max performance |
| **Max Continuous Power** | 1,100 SHP (approx) | Sustained operations; corresponds to ~42 PSI torque at sea level |
| **Gas Producer (N1)** | Idle: ~58-62% / Max: ~100% | N1 responds to fuel flow; governed indirectly through correlator/governor |
| **Power Turbine / Engine RPM (N2)** | 100% = 6,600 RPM | Drives main rotor at 324 RPM through 42° gearbox |
| **Rotor RPM (Nr)** | Normal operating: 324 ± 3 RPM (6,600 engine RPM) | Displayed on dual-needle tachometer with N2 |
| **Exhaust Gas Temperature (EGT)** | Continuous max: 610°C / Transient (5 sec): 625°C / Starting (10 sec): 720°C | EGT is the primary engine health and limit indicator |
| **Idle RPM (Ground)** | N1 ~58%, Nr ~59-62% | Throttle at IDLE; rotor turns but below flight governing range |
| **Flight Idle / FLY** | N1 increases, Nr governed to 324 RPM | Throttle advanced past idle stop to FLY detent |
| **Spool-Up Time** | ~5-8 seconds (idle to max power) | Free turbine responds to collective/correlator input; requires anticipation |
| **Engine Oil Pressure** | Normal: 35-70 PSI / Min: 35 PSI | Below 35 PSI = caution; below 25 PSI = warning |
| **Engine Oil Temperature** | Normal: -40°C to 107°C / Max: 107°C | Above 107°C = land as soon as practicable |
| **Fuel Flow (Cruise ~90 KIAS)** | ~220-260 lbs/hr | Varies with altitude, temperature, gross weight |
| **Fuel Flow (Hover IGE)** | ~300-350 lbs/hr | Higher power demand in hover |

#### Throttle Correlator and Governor System

The UH-1H does **not** have a FADEC. Instead, engine RPM management uses a two-part mechanical/hydromechanical system:

**1. Throttle Correlator:**
- A mechanical linkage between the collective lever and the engine fuel control.
- When the pilot raises the collective (demanding more power), the correlator **automatically increases fuel flow** to the engine proportionally.
- When the pilot lowers the collective, the correlator decreases fuel flow.
- The correlator provides **approximate** RPM compensation — it is not precise enough to maintain Nr within limits by itself.
- Think of it as "rough trim" for RPM.

**2. Governor:**
- A hydromechanical device that senses Nr (rotor RPM) and makes **fine adjustments** to fuel flow to maintain Nr at the governed speed (324 RPM / 6,600 N2).
- The governor acts on top of the correlator, correcting for the error between the correlator's approximate setting and the exact fuel flow needed.
- Enabled by the **GOV switch** on the overhead console (must be ON for normal flight).
- Think of it as "fine tune" for RPM.

**Combined operation:** Pilot raises collective → correlator opens fuel flow roughly → Nr begins to change → governor fine-tunes fuel flow to hold Nr at 324 RPM. The process is continuous and automatic when the governor is functioning.

**Manual throttle (governor OFF or failed):** The pilot must use the twist-grip throttle on the collective to manually manage fuel flow and maintain Nr. The correlator still functions (collective movement still changes fuel flow roughly), but without the governor's fine correction, Nr will wander with every collective change, gust, or maneuver. Manual throttle management is a critical emergency skill.

| Mode | Correlator | Governor | Pilot Throttle Action | Nr Management |
|---|---|---|---|---|
| **Normal (GOV ON)** | Active | Active | Normally no twist-grip adjustment needed | Automatic — governor maintains 324 RPM |
| **Governor OFF / Failed** | Active | Inactive | Must actively twist throttle to maintain Nr | Pilot responsibility — constant monitoring |
| **Throttle full manual** | Active | Inactive | Full manual RPM management | Pilot responsibility — critical workload |

> *⚠ Realism Divergence: The real UH-1H T53-L-13B has a complex hydromechanical fuel control unit (FCU) with acceleration/deceleration limiters and compressor bleed scheduling. DCS models the correlator and governor behavior accurately in feel, but the internal FCU logic is simplified. Real-world FCU malfunctions can present as partial authority loss, fuel scheduling errors, or intermittent RPM hunting that are more nuanced than the DCS "governor off" failure mode. In DCS, governor failure typically results in a clean loss of governing requiring immediate manual throttle — which is realistic for a total governor failure but does not replicate partial-authority degradation.*

#### Engine Start Cycle

1. Battery **ON**, inverter **ON** — electrical power available.
2. Fuel valve **ON**, fuel boost pump **ON** — fuel pressure indicated.
3. Throttle at **CLOSED** (full counterclockwise on twist-grip, fuel cutoff), collective **full down**.
4. Press and hold **starter button** — the starter-generator motors the N1 gas producer section.
5. At approximately **15% N1** — advance throttle to **IDLE** (clockwise to idle stop). This introduces fuel to the combustion chamber.
6. **Light-off indication:** EGT begins to rise. If no EGT rise by ~25% N1, **abort** (throttle to CLOSED, motor to purge).
7. Monitor **EGT** during acceleration — must not exceed **720°C** (10-second starting limit).
8. N1 accelerates through to **ground idle** (~58-62% N1). Nr begins to increase as the rotor spins up.
9. **Stabilize** at ground idle: verify EGT settling below continuous limit (610°C), N1 stable, oil pressure within range, Nr building.
10. Release starter button once N1 reaches idle (starter disengages automatically on most starts).

**Abort Criteria:**

| Condition | Indication | Action |
|---|---|---|
| **Hot start** | EGT exceeds 720°C during start | Throttle to CLOSED immediately; motor to purge; allow 30-second cool-down before reattempt |
| **Hung start** | N1 stagnates below idle, EGT stabilizes high | Throttle to CLOSED; motor to clear; verify fuel supply and battery voltage |
| **No light-off** | No EGT rise by ~25% N1 | Throttle to CLOSED; motor to purge unburned fuel; check fuel valve, boost pump, circuit breakers |
| **Over-temp start** | EGT rises above limits but engine accelerates | Throttle to CLOSED; may have caused engine damage — inspect before re-start |

> *⚠ Realism Divergence: The real T53-L-13B start cycle includes a mandatory 2-minute starter duty cycle limitation (crank for max 60 seconds, then 2-minute cool-down before reattempt). DCS models the start sequence but does not strictly enforce starter duty cycle limitations — the student can crank repeatedly without burning out the starter motor. In reality, exceeding starter duty limits can overheat and damage the starter-generator. Real-world starts also require monitoring of N1 acceleration rate against a time schedule (typically N1 should reach idle within 40-60 seconds); DCS acceleration profiles are close but may differ slightly in timing.*

#### Compressor Stall

The T53-L-13B can experience compressor stall under certain conditions:
- **Causes:** Foreign object damage (FOD), rapid throttle advancement, high-altitude thin-air operation, deteriorated compressor blades, or operation in heavy rain/icing.
- **Symptoms:** Loud bang or series of bangs, EGT spike, possible power loss, airframe vibration.
- **Recovery:** Reduce throttle (lower collective), allow compressor to restabilize, slowly re-advance power. If stall persists, land as soon as practicable.

> *⚠ Realism Divergence: DCS does not model compressor stall as a dynamic event with realistic onset conditions. Engine damage from FOD or deterioration is not simulated. However, the student should understand compressor stall academically as it is a real-world hazard for the T53 engine, particularly in dusty/sandy environments.*

---

### 1.2 Rotor System

#### Main Rotor

| Parameter | Value | Notes |
|---|---|---|
| **Configuration** | 2-blade, semi-rigid (teetering) | The defining characteristic of the UH-1H — teetering hinge at the mast |
| **Diameter** | 48 ft (14.63 m) | |
| **Blade Chord** | 21 inches (0.53 m) | |
| **Nr (Power On)** | 324 ± 3 RPM (6,600 N2) | Governor maintains; dual tachometer shows Nr and N2 |
| **Nr (Autorotation)** | 294-324 RPM | Min 294 RPM for safe autorotation; below = insufficient energy for flare/cushion |
| **Nr Low Warning** | Audio tone + caution light at ~294 RPM | Immediate action: lower collective (autorotation) or increase throttle (powered flight) |
| **Nr Transient High** | ~339 RPM (momentary) | Brief excursion during rapid collective reduction; governor corrects |
| **Nr Overspeed** | 345+ RPM | Structural risk — mast and blade root stress exceedance |
| **Rotor Direction** | Counterclockwise (viewed from above) | Standard U.S. configuration; determines translating tendency and yaw coupling |

**Teetering Rotor Characteristics:**

The two-blade teetering rotor is the most critical system characteristic of the UH-1H and differentiates it from all fully articulated rotor systems:

- **Teetering hinge:** The two blades are rigidly connected to each other and the entire rotor head pivots (teeters) on a single hinge perpendicular to the blade span. One blade goes up, the opposite blade goes down. This is the mechanism by which the rotor accommodates dissymmetry of lift.
- **No individual blade flapping hinges:** Unlike fully articulated rotors (3+ blades with individual flap/lag hinges), the teetering rotor uses the single teeter as both blades' flapping solution. This means blade flapping is always symmetric — if the advancing blade flaps up, the retreating blade must flap down an equal amount.
- **No lead-lag hinges:** The teetering rotor has no lead-lag articulation. Chordwise (in-plane) loads are absorbed through blade flexibility and the underslung rotor design.
- **Underslung rotor:** The rotor head is mounted slightly below the teeter axis, which reduces Coriolis effects (the tendency of the blade CG to shift as it flaps, causing lead-lag forces). This is a deliberate design feature.
- **Stabilizer bar (Bell bar):** A weighted bar mounted at 90° to the main rotor blades, acting as a mechanical gyroscope. The stabilizer bar resists changes in rotor disc attitude, providing:
  - Improved stability in gusty conditions
  - A damping effect on pilot cyclic inputs (the rotor responds more gradually)
  - A slight lag in control response compared to helicopters without stabilizer bars
  - In DCS, the stabilizer bar effect is modeled — the pilot will notice the rotor disc does not respond instantaneously to cyclic inputs

**Mast Bumping — CRITICAL HAZARD:**

Mast bumping is the **most dangerous flight condition unique to the teetering rotor**. It occurs when the rotor disc tilts so far that the static stop (droop stop) on the underside of the hub contacts the rotor mast. The sequence:

1. Low-G or negative-G condition occurs (aggressive forward cyclic, turbulence-induced unloading, abrupt pushover).
2. With reduced or negative G on the rotor disc, the rotor is no longer loaded — it is free to teeter to its mechanical limits.
3. The teetering angle exceeds the designed range and the hub contacts the mast.
4. **Mast separation** — the mast can be severed by the rotor hub contact, which is immediately catastrophic and unrecoverable.

**Prevention:** Never aggressively push forward cyclic. Never abruptly unload the rotor disc. In turbulence, maintain positive G at all times. During autorotation, do not push the nose over aggressively after power loss. The mantra is: **"Aft cyclic is always safe; forward cyclic under low-G is lethal."**

> *⚠ Realism Divergence: DCS models mast bumping and it can result in catastrophic mast separation and loss of the aircraft. The DCS implementation is a good training tool for understanding the danger. However, the exact G threshold and teetering angle limits may differ slightly from the real aircraft. In the real UH-1H, mast bumping can occur with as little as 0.5G sustained — the margin is narrower than most students expect. DCS may be slightly more forgiving in its onset threshold.*

#### Stabilizer Bar (Bell Bar) Detail

| Parameter | Detail |
|---|---|
| **Function** | Mechanical gyroscope — resists attitude changes of the rotor disc |
| **Effect on handling** | Smooths out gusty inputs, adds a ~0.5-1 second lag to cyclic response |
| **Pilot consideration** | Must anticipate cyclic inputs slightly; the helicopter does not respond as crisply as a helicopter without a stabilizer bar |
| **DCS modeling** | Modeled — the student will feel the delayed cyclic response compared to other DCS helicopters (e.g., the Mi-8/Mi-24 feel more immediately responsive) |

#### Tail Rotor

| Parameter | Value | Notes |
|---|---|---|
| **Configuration** | 2-blade, semi-rigid | Mounted on left side of tail boom (viewed from behind) |
| **Diameter** | 8.5 ft (2.59 m) | |
| **Function** | Anti-torque (counteracts main rotor torque), yaw control | Left pedal increases tail rotor thrust (nose left); right pedal decreases (nose right) |
| **Drive** | Driveshaft from main transmission through 42° and 90° gearboxes | Loss of tail rotor drive = loss of anti-torque; the most demanding rotary-wing emergency |
| **Pusher configuration** | Tail rotor pushes the tail to the right (thrust to the right) | This means the tail rotor produces a right-pointing force in normal hover, which is balanced by left pedal input |

#### Droop Compensator

The droop compensator is a mechanical device that automatically adjusts engine fuel flow during rapid collective changes to prevent Nr droop (RPM sag when collective is raised rapidly). It supplements the correlator and governor to reduce transient Nr excursions during aggressive power demands. In DCS, this is modeled as part of the engine/governor system behavior.

---

### 1.3 Transmission System

| Component | Function | Key Limits |
|---|---|---|
| **Main Transmission (42° Gearbox)** | Reduces engine output RPM (6,600) to main rotor RPM (324); also drives tail rotor driveshaft, hydraulic pump, generator, and accessories | Torque: continuous and transient limits per chart |
| **Tail Rotor Driveshaft** | Transmits power from main transmission to tail rotor gearbox through segmented driveshaft sections | Vibration or unusual noise = possible impending failure |
| **Tail Rotor Gearbox** | 90° gearbox converting driveshaft rotation to tail rotor rotation | Oil level, temperature, chip detector |
| **Freewheeling Unit (Sprag Clutch)** | One-way clutch that disengages the engine from the transmission when Nr exceeds N2 — allows the rotor to spin freely in autorotation | Must disengage cleanly; failure to disengage means engine drag slows rotor in autorotation |

#### Transmission Limits

| Parameter | Normal | Caution | Warning |
|---|---|---|---|
| **Torque (Q)** | ≤ 40 PSI (continuous) | 40-50 PSI (transient, 5 min) | > 50 PSI exceeds structural limit |
| **Trans Oil Pressure** | 30-70 PSI | < 30 PSI | XMSN OIL PRESS caution light |
| **Trans Oil Temperature** | < 110°C (230°F) | 110-120°C | > 120°C = land immediately |
| **Chip Detector** | Clear | — | CHIP DET light = metallic particles; land as soon as possible |

**Torque Interpretation:**

Torque in the UH-1H is displayed in **PSI (pounds per square inch)** on the torque pressure gauge, not as a percentage. This differs from many modern helicopters that display torque as a percentage. The pilot must memorize the continuous and transient PSI limits for the current conditions.

| Condition | Torque Limit (Approx) | Duration |
|---|---|---|
| **Continuous (MCP)** | ~40 PSI | Unlimited |
| **Takeoff (Military Power)** | ~48 PSI | 30 minutes (5 min at some conditions) |
| **Transient** | ~50 PSI | Momentary — avoid exceeding |

> *⚠ Realism Divergence: Real UH-1H torque limits vary with altitude, temperature, and rotor RPM per performance charts in TM 55-1520-210-10 Chapter 5. DCS models torque limits but the performance planning charts (power available vs. power required at various conditions) are simplified. The student should use the DCS torque gauge as the primary reference and avoid exceeding ~48 PSI except momentarily.*

---

### 1.4 Fuel System

| Parameter | Value | Notes |
|---|---|---|
| **Internal Fuel Capacity** | ~210 US gallons (~1,390 lbs JP-4/JP-8) | Crashworthy, self-sealing fuel cells located beneath the cabin floor |
| **Fuel Type** | JP-4 (primary, Vietnam era), JP-8 (current standard), Jet-A acceptable | DCS uses generic jet fuel |
| **Fuel Boost Pump** | Electric, pilot-controlled (overhead console) | Must be ON before start and during flight |
| **Fuel Filter Bypass** | Caution light indicates filter contamination | FUEL FILTER caution = fuel bypassing filter; land as soon as practicable |
| **Fuel Quantity Indicator** | Instrument panel — calibrated in pounds | Single gauge; accuracy varies with fuel cell deformation and attitude |
| **Low Fuel Warning** | Caution light at approximately 200 lbs (~30 US gal) remaining | Approximately 40-50 minutes at cruise; immediate recovery planning required |
| **Fuel Consumption (Hover IGE)** | ~300-350 lbs/hr | Sea level, mid gross weight (~8,000 lbs) |
| **Fuel Consumption (Cruise ~90 KIAS)** | ~220-260 lbs/hr | Sea level, mid gross weight |
| **Endurance (No Reserve)** | ~4.5-5.5 hours cruise | Varies significantly with weight, altitude, temperature, mission profile |

The fuel system uses crashworthy, self-sealing cells located beneath the cabin floor. The electric boost pump provides positive pressure to the engine fuel control; loss of the boost pump triggers the FUEL BOOST caution light. Gravity feed is available as emergency backup but is unreliable in certain flight attitudes (negative G, steep bank, extreme nose-up/down).

**Fuel Management Notes:**
- Always start with boost pump ON and verify fuel pressure before engine start.
- Monitor fuel quantity regularly — the UH-1H has no automated fuel management or transfer system.
- The fuel quantity gauge can be inaccurate at low fuel states and in non-level flight attitudes.
- Plan for a 20-minute fuel reserve minimum (IFR reserve is higher per AR 95-1).

> *⚠ Realism Divergence: The real UH-1H fuel system has more complex failure modes including fuel cell leaks, fuel contamination (water/sediment), and cross-feed issues in multi-cell configurations. DCS models fuel quantity and boost pump failure but does not simulate fuel contamination, cell leakage, or attitude-dependent gravity feed limitations in detail. The fuel quantity gauge in DCS is more accurate than the real aircraft's gauge, which could be significantly off at low fuel states.*

---

### 1.5 Hydraulic System

| Parameter | Value | Notes |
|---|---|---|
| **Configuration** | Single hydraulic system | No backup/redundant hydraulic system |
| **Pump** | Engine-driven (mounted on main transmission) | Operates whenever rotor is turning |
| **Pressure** | Normal: 1,000-1,500 PSI | Hydraulic pressure gauge on instrument panel |
| **Function** | Powers irreversible flight control servo actuators (cyclic, collective, tail rotor) | Without hydraulics, flight controls require significantly more force |
| **Accumulator** | Small hydraulic accumulator | Provides brief residual pressure after pump failure; not sustained flight capability |

**Hydraulic Failure Characteristics:**

Loss of hydraulics in the UH-1H does **not** mean loss of control — but it dramatically increases control forces:

- **Cyclic:** Becomes very heavy — requires both hands and significant arm force to make control inputs. Feedback forces can exceed 40-50 lbs.
- **Collective:** Becomes heavy but manageable — requires deliberate, forceful inputs.
- **Pedals:** Become heavy — anti-torque pedal forces increase substantially.
- **Flight characteristic:** The helicopter is still flyable, but the pilot will fatigue rapidly. Small, frequent corrections become exhausting. The recommended technique is to fly at 60-80 KIAS (where control forces are most manageable) and execute a **run-on landing** (avoid hover — hovering without hydraulics is extremely demanding and dangerous due to the constant control corrections required).

> *⚠ Realism Divergence: DCS models hydraulic failure and the resulting heavy controls accurately. The force feedback through the cyclic is well-represented if the student uses a force-sensing or spring-loaded stick. Students using desktop joysticks with light centering springs will not fully appreciate the difficulty of hydraulic-off flight. The real aircraft requires genuine physical strength to control without hydraulics; DCS can only approximate this through increased control sensitivity/dead zone changes.*

---

### 1.6 Electrical System

| Component | Description | Notes |
|---|---|---|
| **DC Starter-Generator** | 28V DC, 200 amp | Serves as starter during engine start, then as generator once engine is running |
| **Main Battery** | 24V nickel-cadmium | Provides power for start and emergency backup; located in fuselage nose compartment |
| **AC Inverter** | Converts 28V DC to 115V AC (400 Hz) | Powers AC instruments (attitude indicator, gyros, some radio components) |
| **Essential Bus** | Always powered when battery is ON | Critical instruments, caution panel, fire warning, some radios |
| **Non-Essential Bus** | Powered through generator; shed-able in emergency | Non-critical avionics, lighting, some radios |
| **External Power** | 28V DC external power receptacle | For ground operations without draining battery |
| **Generator Failure** | GEN caution light, voltage drop | Battery-only endurance: ~30 minutes (varies with electrical load) |

**Electrical System Sequence:**

1. **Battery ON** → Essential bus powered, caution panel illuminates for test
2. **Inverter ON** → AC power available for gyro instruments (they require warm-up time)
3. **Engine start** → Starter-generator draws high current from battery
4. **Post-start** → Generator switch ON → generator takes over bus load, battery begins charging
5. **Generator failure** → GEN caution light → shed non-essential loads, land as soon as practicable (battery provides ~30 min backup)

**Circuit Breaker Panels:**

The UH-1H has circuit breaker panels on both the pilot side and copilot side of the cockpit. Individual circuit breakers are labeled and can be pulled manually to isolate malfunctioning systems. In DCS, each circuit breaker is clickable.

> *⚠ Realism Divergence: The real UH-1H has specific circuit breaker collaring procedures (maintenance action) and certain CBs that should never be pulled in flight per the -10. DCS models all CBs as freely pullable without restriction. The student should learn which CBs are relevant to specific systems but should not experiment with pulling CBs in flight except for documented emergency procedures.*

---

### 1.7 Force Trim and SAS

#### Force Trim (Magnetic Brake)

The UH-1H uses a **magnetic brake force trim system** on the cyclic and pedals. This is fundamentally different from a traditional trim tab or electric trim system:

- **How it works:** Electromagnetic brakes hold the cyclic and pedals in whatever position the pilot sets. When the pilot presses the **force trim release button** (on the cyclic grip), the brakes release and the controls move freely. When the button is released, the brakes re-engage and hold the current position.
- **Setting trim:** Fly to the desired airspeed/attitude → press and hold force trim release → move cyclic/pedals to the position that maintains the desired flight condition → release force trim button. The brakes lock the controls in place.
- **Out-of-trim forces:** If the aircraft's trim condition changes (airspeed, power, CG shift) and the pilot has not re-trimmed, the magnetic brakes resist the change, creating stick forces that the pilot feels. These forces can be significant and must be trimmed out regularly.
- **Trimming cadence:** The UH-1H pilot must re-trim frequently — any change in airspeed, power, altitude, or configuration requires a trim update. This is a much higher workload than aircraft with electric trim systems.

| Control | Force Trim | Notes |
|---|---|---|
| **Cyclic (lateral and longitudinal)** | Magnetic brake, released by cyclic button | Must re-trim with every speed/power change |
| **Pedals** | Magnetic brake, released simultaneously with cyclic | Pedal trim changes with torque/power changes |
| **Collective** | Friction adjustment (not magnetic brake) | Pilot adjusts collective friction lock to desired resistance |

#### SAS (Stability Augmentation System)

The UH-1H in its base configuration does **not** have a SAS/SCAS (Stability/Control Augmentation System). Some late-production or modified UH-1H aircraft were retrofitted with limited SAS capability, but the DCS module represents the standard UH-1H without SAS.

This means:
- The UH-1H has **no artificial stability enhancement** — all stability comes from the rotor dynamics, stabilizer bar, and pilot input.
- The aircraft requires **constant pilot attention** to maintain heading, altitude, and attitude.
- The stabilizer bar provides some gyroscopic stability, but it is not a substitute for SAS.
- In gusty conditions or turbulence, the pilot workload is significantly higher than in SAS-equipped helicopters.

> *⚠ Realism Divergence: The DCS UH-1H models the aircraft without SAS, which is correct for the standard UH-1H configuration. Some real-world UH-1H aircraft in later service received SAS modifications, but the DCS module represents the unaugmented flight control system. The student should expect a more demanding flying experience compared to DCS helicopters with SAS/SCAS (Mi-24P, Ka-50).*

---

### 1.8 Rotary-Wing Aerodynamics — UH-1H Specific

This section covers aerodynamic phenomena that affect the UH-1H, with emphasis on behaviors unique to or particularly pronounced in the two-blade teetering rotor system.

#### Translating Tendency (Left Drift in Hover)

In hover, the tail rotor produces a lateral thrust (pushing the tail to the right) to counteract main rotor torque. This lateral force also pushes the entire aircraft to the right. To compensate, the UH-1H hovers with a **slight left tilt** of the rotor disc, which produces a small left translation force. However, this compensation is imperfect, and the aircraft exhibits a natural **left drift tendency** in hover that the pilot must correct with right cyclic.

**DCS Manifestation:** The student will notice that in a no-wind hover, the aircraft drifts left if the pilot does not apply a small amount of right cyclic. This is normal and expected.

#### Translational Lift (Effective Translational Lift — ETL)

As the helicopter accelerates from hover through approximately **16-24 knots** of airspeed, the rotor disc moves into undisturbed air, increasing the efficiency of lift production. This is **Effective Translational Lift (ETL)**.

| Phenomenon | Airspeed | Pilot Indications | Required Control Inputs |
|---|---|---|---|
| **ETL onset** | ~16-24 KIAS | Vibration decreases, aircraft "gets light," nose pitches up, left yaw tendency | Forward cyclic to counteract nose-up pitch, right pedal to counteract left yaw, slight collective reduction (more lift at same power) |
| **Through ETL (accelerating)** | 24+ KIAS | Vibration further decreases, aircraft climbs if collective not adjusted | Continue forward cyclic, adjust collective and pedals as needed |
| **Through ETL (decelerating)** | Below ~16-24 KIAS | Vibration increases, aircraft "gets heavy," nose dips, power required increases | More collective needed, left pedal to compensate for reduced torque demand... wait, actually: more collective = more torque = more left pedal |

**Correction:** During deceleration below ETL, the pilot needs more collective (power) to compensate for the loss of translational lift. More collective = more engine torque = more left yaw tendency = more left pedal required.

#### Transverse Flow Effect

As the helicopter transitions through 10-20 knots, the air flowing through the aft portion of the rotor disc is deflected downward (induced velocity is higher at the back than the front due to the flow pattern). This creates a differential in angle of attack: the aft blades operate at a lower angle of attack (reduced lift) while the forward blades produce more lift. The result is a lateral vibration and a tendency for the helicopter to roll slightly. This is felt as a brief vibration or shudder during the transition through low airspeeds. The pilot corrects with lateral cyclic as needed.

#### Dissymmetry of Lift

In forward flight, the advancing blade (right side for counterclockwise rotor) sees a higher relative airspeed than the retreating blade (left side). Without compensation, this would cause the aircraft to roll left. The **teetering hinge** is the UH-1H's solution: the advancing blade flaps up (reducing its angle of attack) and the retreating blade flaps down (increasing its angle of attack), equalizing lift across the disc. Because the two blades are rigidly connected, this flapping is perfectly symmetric — one blade up equals the other blade down.

#### Retreating Blade Stall

At high airspeeds, the retreating blade cannot increase its angle of attack enough to compensate for low relative airspeed, and it stalls. The teetering rotor is **more susceptible** to retreating blade stall than fully articulated systems because:
- The two-blade rotor has less disc area per blade to spread the lift production.
- The teetering hinge does not allow individual blade pitch adjustments beyond the cyclic input.
- Blade loading is higher per blade than a 4 or 5-blade system of similar thrust.

**Symptoms:** Vibration (initially 2-per-rev, becoming irregular), uncommanded pitch-up and/or left roll, increased stick forces.

**Recovery:** Reduce airspeed (aft cyclic), reduce collective (lower blade loading), reduce G-load (avoid steep turns), and descend to lower altitude (denser air = higher retreating blade airspeed).

**Vne Relationship:** The UH-1H's Vne (124 KIAS at sea level) is set primarily by retreating blade stall onset. Vne decreases with altitude, gross weight, and increased G-loading.

| Condition | Effect on Vne |
|---|---|
| Increased altitude | Vne **decreases** (lower air density = less retreating blade lift margin) |
| Increased gross weight | Vne **decreases** (higher blade loading = closer to stall) |
| Increased G-load (turns) | Effective Vne **decreases** (higher blade loading) |
| Turbulence | Can trigger blade stall at speeds below published Vne |

#### Ground Effect (IGE vs. OGE)

| Condition | Description | Performance Impact |
|---|---|---|
| **In Ground Effect (IGE)** | Hovering within approximately 1/2 rotor diameter of the ground (~24 ft for UH-1H) | Reduced induced drag — less power required to hover (typically 10-15% less torque than OGE) |
| **Out of Ground Effect (OGE)** | Hovering above ~24 ft AGL or over water/sloping terrain where ground effect is disrupted | Full induced drag — maximum power required to hover |

**Practical implication:** A UH-1H that can hover IGE may **not** be able to hover OGE at the same weight/altitude/temperature. The pilot must check hover power OGE before committing to departures, pinnacle operations, or confined area work where ground effect may be lost.

#### Settling with Power (Vortex Ring State)

| Factor | Threshold |
|---|---|
| **Airspeed** | Below ~30 knots |
| **Rate of Descent** | Exceeding ~300 ft/min |
| **Power** | Moderate to high (attempting to arrest descent with collective) |

**What happens:** The helicopter descends into its own rotor downwash, creating a turbulent doughnut-shaped vortex around the rotor disc. The rotor recirculates its own disturbed air, and increasing collective only worsens the condition (pumping more air into the vortex). Rate of descent increases despite power application.

**Recognition:** High rate of descent that does not respond to collective, aircraft shuddering/vibrating, random pitch and roll excursions.

**Recovery:** Forward cyclic to gain airspeed (fly out of the vortex), reduce collective momentarily to break the vortex pattern, then climb away. If altitude permits, the standard recovery is to push the cyclic forward to accelerate to above 30 knots, then arrest the descent normally.

#### Loss of Tail Rotor Effectiveness (LTE)

LTE is a critical rotary-wing hazard that affects all single-rotor helicopters. For the UH-1H, three wind azimuth regions are particularly dangerous:

| Wind Azimuth (Relative to Nose) | Mechanism | Danger |
|---|---|---|
| **285°-315°** (left rear quarter) | Main rotor vortex interference — vortex from the main rotor is blown into the tail rotor disc | Tail rotor encounters turbulent, disturbed air; reduced anti-torque effectiveness |
| **120°-240°** (rear half) | Weathercock instability — wind pushes the tail, causing the aircraft to yaw into the wind; if the tail rotor cannot overcome this, a spin develops | Most common LTE scenario during hovering turns |
| **210°-330°** (left rear arc) | Tail rotor vortex ring state — a tailwind causes the tail rotor to enter its own vortex ring state, dramatically reducing thrust | Sudden, uncommanded right yaw with little or no warning |

**Recognition:** Uncommanded right yaw (nose swings right), inability to maintain heading with left pedal, increasing yaw rate.

**Recovery:**
1. Forward cyclic immediately — gain airspeed. Airspeed is the cure for LTE (the vertical fin provides directional stability at speed).
2. If altitude permits, lower collective to reduce torque demand (less anti-torque needed).
3. Do NOT add excessive left pedal if the tail rotor is in vortex ring state — this can worsen the condition.
4. If a spin develops and altitude is insufficient for recovery — autorotate (reducing collective removes torque, eliminating the need for anti-torque).

#### Mast Bumping — Teetering Rotor Specific

*This is the most critical aerodynamic hazard unique to the UH-1H's rotor system.*

**Mechanism:**
1. In normal flight, the rotor disc is loaded (positive G) and the teetering hinge allows controlled flapping within design limits.
2. Under low-G or negative-G conditions (pushover, abrupt forward cyclic, turbulence-induced unloading), the rotor disc becomes unloaded.
3. With an unloaded disc, the teetering hinge can flap to its mechanical stops. If cyclic is displaced while the disc is unloaded, the rotor head can contact the mast.
4. **Mast contact → mast separation → catastrophic unrecoverable failure.**

**Critical scenarios:**
- Abrupt forward cyclic pushover (especially at low airspeed or during autorotation)
- Turbulence encounter at light gross weight
- Bunting (pushing over the top of a climb)
- Aggressive sideslip corrections
- Wake turbulence from another aircraft

**Prevention rules:**
1. **Never push forward cyclic aggressively.** All forward cyclic inputs should be smooth and progressive.
2. **Maintain positive G at all times.** If you feel light in the seat, you are at risk.
3. **In turbulence:** Slow down, increase gross weight awareness, maintain positive G.
4. **In autorotation:** Do not push over aggressively after entry. Establish autorotation airspeed with smooth control movements.
5. **If you feel low-G:** Immediately apply gentle aft cyclic to reload the disc. Do NOT attempt to correct with lateral cyclic under low-G conditions.

> *⚠ Realism Divergence: DCS models mast bumping and it can destroy the aircraft in simulation. This is an excellent training tool. However, the exact G threshold for mast bumping onset in DCS may differ slightly from the real aircraft. In the real UH-1H, the margin between normal flight and mast bumping under low-G is extremely narrow — as little as 0.5G reduction from 1G can allow the teetering hinge to reach stops if cyclic is displaced. The real-world accident record shows mast bumping fatalities occurred in conditions that felt like routine flight to the pilot until the instant of mast separation. DCS may be slightly more forgiving, but the student should treat the hazard with maximum respect.*

#### Dynamic Rollover

Dynamic rollover occurs when the helicopter pivots around a ground contact point (a skid, a tiedown, an obstacle) and reaches a roll rate that exceeds the pilot's ability to correct with lateral cyclic.

**Conditions:**
- One skid on the ground during liftoff or landing (especially slope operations)
- Lateral drift at touchdown
- Crosswind pushing the aircraft over during hover
- Sling load or external force pulling laterally

**Critical roll rate:** If the roll rate exceeds approximately **10°/second** around the pivot point, the pilot cannot stop the roll even with full opposite cyclic. The helicopter will roll over.

**Prevention:**
- During slope operations, always approach hover height cautiously and keep the upslope skid in contact as long as possible.
- If lateral roll begins during liftoff, **lower collective** if still in early phase (below 10°/sec roll rate).
- Maintain awareness of crosswind effects during liftoff and landing.
- Never allow a steady roll rate to develop near the ground.

#### Pendular Action

The UH-1H exhibits pendular action because the fuselage hangs below the rotor disc like a pendulum. The fuselage swings beneath the rotor disc during attitude changes, and this swinging can be amplified by poorly timed or over-corrected cyclic inputs. The student must learn to:
- Make small, smooth corrections rather than large abrupt ones
- Allow the fuselage to settle after a correction before making another
- Recognize the "pilot-induced oscillation" pattern (over-correcting back and forth)

**In hover:** Pendular action is most pronounced and most dangerous. The student will commonly over-control in hover, causing a growing oscillation. The correction is to relax inputs and let the helicopter stabilize, rather than chasing each swing with an opposite input.

---

### 1.9 Key Data Summary — Module 1

#### Engine Limits Quick Reference

| Parameter | Normal | Caution | Emergency/Limit |
|---|---|---|---|
| **EGT** | < 610°C | 610-625°C (5 sec) | > 625°C / 720°C starting |
| **N1 (Gas Producer)** | 58-100% | — | > 101% (overspeed) |
| **Nr (Rotor RPM)** | 321-327 RPM | 294-321 or 327-339 | < 294 or > 339 RPM |
| **Torque** | < 40 PSI | 40-48 PSI (time-limited) | > 50 PSI |
| **Engine Oil Pressure** | 35-70 PSI | < 35 PSI | < 25 PSI |
| **Engine Oil Temperature** | < 107°C | 107-120°C | > 120°C |
| **Trans Oil Pressure** | 30-70 PSI | < 30 PSI | XMSN OIL PRESS light |
| **Trans Oil Temperature** | < 110°C | 110-120°C | > 120°C |

#### V-Speeds Quick Reference

| Speed | Value | Usage |
|---|---|---|
| **Vy (Best Rate of Climb)** | 60 KIAS | Maximum altitude gain per unit time |
| **Cruise** | 90-100 KIAS | Normal transit speed; best range ~100 KIAS |
| **Autorotation** | 65 KIAS | Best glide speed for autorotation |
| **Vne (Never Exceed)** | 124 KIAS | Sea level; decreases with altitude, weight, G |
| **Min Autorotation Nr** | 294 RPM | Below this = insufficient energy for flare/cushion |

#### Instructor Notes — Module 1

| Common Student Error | Correction |
|---|---|
| **Ignoring Nr during collective changes** | Emphasize that Nr is life — teach the dual-needle tach scan as the most critical instrument check during power changes |
| **Not understanding correlator/governor** | Use a ground exercise: raise/lower collective slowly and observe Nr, EGT, torque. Then turn governor OFF and repeat — the difference is dramatic and instructive |
| **Underestimating mast bumping danger** | Brief extensively, show accident case studies, emphasize "never push forward cyclic aggressively" as a core habit |
| **Confusing EGT and torque limits** | Create a limits card (knee-board reference) with all engine and transmission limits; quiz regularly |
| **Not appreciating the teetering rotor difference** | Compare to other DCS helicopters — fly the Mi-8 or Ka-50 back-to-back with the UH-1H to feel the stabilizer bar lag and the different control response |
| **Over-controlling in hover (pendular action)** | Start hover training in zero wind; emphasize small inputs and patience; let the stabilizer bar do its job |

---

## Module 2: Cockpit Familiarization

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Identify every major panel and control group in the UH-1H cockpit by name and location.
2. Locate and identify all engine instruments and state their normal operating ranges from memory.
3. Locate and identify all flight instruments and describe the radial scan pattern.
4. Identify all caution/advisory panel lights and associate each with its corresponding system.
5. Operate the audio control panel and select radios for transmit and receive.
6. Identify the three radio systems (VHF-AM, UHF-AM, FM) by physical location and function.
7. Identify the navigation radio equipment (ADF, VOR/ILS) and their cockpit indications.
8. Describe the collective grip controls (throttle, idle stop, radio triggers) and cyclic grip controls (force trim release, cargo release).
9. Locate cockpit and exterior lighting controls and set appropriate configurations for day and night operations.

---

### 2.1 Cockpit Layout — General Arrangement

The UH-1H cockpit seats two crew members side-by-side: **pilot (right seat)** and **copilot (left seat)**. Both stations have full flight controls (cyclic, collective, pedals), but the primary instruments and many switches are oriented toward the pilot's position. In DCS, the player occupies the **pilot (right seat)** by default.

| Area | Location | Primary Contents |
|---|---|---|
| **Overhead Console** | Above and between both crew members | Engine controls, governor switch, fuel system switches, electrical switches (battery, generator, inverter), pitot heat, engine anti-ice, RPM warning, caution light test |
| **Main Instrument Panel** | Forward, divided into pilot (right) and copilot (left) sections | Flight instruments, engine instruments, caution/advisory panel, clock, radar altimeter |
| **Center Pedestal** | Between pilot and copilot seats, below instrument panel | Radio stack (VHF-AM, UHF-AM, FM), audio control panels, transponder, ICS panel |
| **Pilot's Subpanel (Right)** | Lower right instrument panel area | Circuit breaker panel (pilot side), armament panel (if equipped), miscellaneous switches |
| **Copilot's Subpanel (Left)** | Lower left instrument panel area | Circuit breaker panel (copilot side), additional switches |
| **Pilot's Collective (Right)** | Left hand of pilot (right seat) | Twist-grip throttle, idle stop, landing light switch, searchlight control, radio trigger positions |
| **Pilot's Cyclic (Right)** | Right hand of pilot (right seat) | Force trim release button, weapons/cargo release, ICS/radio keying |
| **Pedals** | Foot controls at both stations | Anti-torque pedals with adjustment mechanism |

#### Cockpit Diagram — Panel Layout (Simplified)

```
┌─────────────────────────────────────────────────────────────┐
│                    OVERHEAD CONSOLE                          │
│  [FUEL VLV] [BOOST PMP] [GOV] [BATT] [GEN] [INV] [DEICE]  │
│  [PITOT HT] [RPM WARN] [START BTN] [CAUTION TEST]          │
├──────────────────────┬──────────────────────────────────────┤
│   COPILOT PANEL (L)  │         PILOT PANEL (R)              │
│                      │                                       │
│  ┌───┐ ┌───┐ ┌───┐  │  ┌───┐ ┌───┐ ┌───┐                  │
│  │ATT│ │ASI│ │ALT│  │  │ATT│ │ASI│ │ALT│                  │
│  └───┘ └───┘ └───┘  │  └───┘ └───┘ └───┘                  │
│  ┌───┐ ┌───┐ ┌───┐  │  ┌───┐ ┌───┐ ┌───┐                  │
│  │VSI│ │HDG│ │T&S│  │  │VSI│ │HDG│ │T&S│                  │
│  └───┘ └───┘ └───┘  │  └───┘ └───┘ └───┘                  │
│                      │                                       │
│  ┌──────────────────────────────────────┐                   │
│  │  ENGINE INSTRUMENTS (CENTER)          │                   │
│  │  [TRQ] [EGT] [N1] [Nr/N2] [FF]      │                   │
│  │  [ENG OIL P/T] [XMSN OIL P/T]       │                   │
│  └──────────────────────────────────────┘                   │
│                                                              │
│  ┌──────────────────┐  ┌──────────────────┐                 │
│  │  CAUTION PANEL    │  │  FUEL QTY / MISC  │                │
│  │  [Master Caution] │  │                    │                │
│  │  [RPM] [ENG OIL]  │  │                    │                │
│  │  [XMSN] [FUEL]    │  │                    │                │
│  └──────────────────┘  └──────────────────┘                 │
├──────────────────────────────────────────────────────────────┤
│                    CENTER PEDESTAL                            │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐       │
│  │ AN/ARC-134│ │AN/ARC-51BX│ │AN/ARC-131│ │ XPNDR   │       │
│  │ (VHF-AM) │ │ (UHF-AM) │ │  (FM)    │ │          │       │
│  └──────────┘ └──────────┘ └──────────┘ └──────────┘       │
│  ┌──────────────────┐  ┌──────────────────┐                 │
│  │ AUDIO PANEL (L)  │  │ AUDIO PANEL (R)  │                 │
│  └──────────────────┘  └──────────────────┘                 │
├──────────────────────────────────────────────────────────────┤
│ [COPILOT CB PANEL]                    [PILOT CB PANEL]       │
└──────────────────────────────────────────────────────────────┘
```

---

### 2.2 Overhead Console

The overhead console is the primary location for engine and electrical system management. Switches are organized in functional groups.

#### Engine / Fuel Controls

| Switch/Control | Location | Function | DCS Interaction |
|---|---|---|---|
| **Fuel Valve** | Overhead — Fuel panel | Opens/closes fuel supply to engine | Left-click toggle (guarded) |
| **Fuel Boost Pump** | Overhead — Fuel panel | Activates electric fuel boost pump | Left-click toggle |
| **Governor (GOV) Switch** | Overhead — Engine panel | Enables/disables RPM governor | Left-click toggle; critical for normal ops |
| **Engine De-Ice** | Overhead — Engine panel | Activates engine inlet anti-ice | Left-click toggle |
| **Pitot Heat** | Overhead — Misc panel | Heats pitot tube for ASI accuracy | Left-click toggle |
| **Starter Button** | Overhead — Engine panel | Engages starter-generator in motor mode | Left-click and hold during start |
| **RPM Warning Audio** | Overhead — Engine panel | Enables/disables low-RPM audio warning | Left-click toggle; should be ON at all times in flight |
| **Idle Stop Release** | On collective grip | Allows throttle to advance past IDLE to FLY | Mechanical button on collective; click or key |

#### Electrical Controls

| Switch/Control | Location | Function | DCS Interaction |
|---|---|---|---|
| **Battery** | Overhead — Electrical panel | Master battery ON/OFF | Left-click toggle; first switch in startup |
| **Generator (GEN)** | Overhead — Electrical panel | Connects starter-generator to bus as generator | Left-click toggle; ON after engine reaches idle |
| **Inverter** | Overhead — Electrical panel | Activates DC-to-AC inverter for AC instruments | Left-click toggle; required for gyro instruments |
| **Caution Light Test** | Overhead — Test panel | Illuminates all caution panel lights for bulb check | Left-click and hold |

> *⚠ Realism Divergence: In the real UH-1H, several overhead switches have guard covers that must be lifted before the switch can be toggled. DCS models some guards but may not require guard lifting for every protected switch. The student should develop the habit of checking guard position before toggling critical switches, even if DCS does not enforce it.*

---

### 2.3 Instrument Panel — Flight Instruments

The UH-1H uses **standard "six-pack" steam gauge arrangement** for flight instruments, duplicated on both pilot and copilot sides. The pilot (right seat) instruments are the primary reference.

#### Pilot's Flight Instruments (Right Side)

| Instrument | Position | Function | Key Notes |
|---|---|---|---|
| **Attitude Indicator (AI)** | Top center of T-arrangement | Displays aircraft pitch and roll attitude | AC powered (requires inverter); cages for erection; ~3 min warm-up |
| **Airspeed Indicator (ASI)** | Top left | Indicates airspeed in knots (KIAS) | Pitot-static system; affected by pitot blockage; range typically 0-150+ knots |
| **Barometric Altimeter** | Top right | Indicates altitude MSL based on barometric pressure | Kollsman window for altimeter setting (in. Hg); must be set before each flight |
| **Vertical Speed Indicator (VSI)** | Bottom right | Shows rate of climb/descent in feet per minute | Static pressure instrument; has inherent lag of 6-9 seconds |
| **Heading Indicator / Directional Gyro (DG)** | Bottom center | Displays magnetic heading | Gyroscopic; precesses over time — must be reset to magnetic compass every ~15 min |
| **Turn-and-Slip Indicator** | Bottom left | Shows rate of turn (needle) and slip/skid (ball) | The slip ball is critical: centered ball = coordinated flight; ball displacement = sideslip. In tail rotor failure, the ball indicates yaw. |

#### Instrument Scan Pattern

The UH-1H pilot uses a **radial scan** centered on the attitude indicator:

```
        ASI ←── AI ──→ ALT
                │
         T&S ←── ──→ VSI
                │
               DG
```

1. Start at the **Attitude Indicator** (center reference)
2. Scan to **Airspeed** — verify speed trend
3. Return to **AI**
4. Scan to **Altimeter** — verify altitude trend
5. Return to **AI**
6. Scan to **VSI** — verify climb/descent rate
7. Return to **AI**
8. Scan to **DG** — verify heading
9. Return to **AI**
10. Scan to **Engine instruments** — verify limits
11. Return to **AI**

**Key principle:** Always return to the AI between each instrument check. The AI tells you the aircraft's attitude, which is the most critical piece of information for maintaining control.

**Outside reference integration:** In VFR flight (the BQT standard), the pilot primarily uses **outside visual references** (horizon, ground features) and cross-checks with instruments. The scan pattern above is for instrument cross-check during VFR, and becomes the primary reference in IMC (not covered in this BQT course).

---

### 2.4 Instrument Panel — Engine Instruments

Engine instruments are located in the **center of the instrument panel**, visible to both pilot and copilot.

| Instrument | Display | Normal Range | Critical Limits | Notes |
|---|---|---|---|---|
| **Torque Pressure Gauge** | PSI (0-50+ range) | < 40 PSI continuous | > 48 PSI time-limited, > 50 PSI structural | Primary power indicator; the pilot's "throttle gauge" |
| **Exhaust Gas Temperature (EGT)** | Degrees Celsius | < 610°C | 625°C (5 sec transient), 720°C (starting) | Primary engine health indicator; most common limit to hit |
| **Gas Producer Tachometer (N1)** | Percentage (0-110%) | 58-100% | > 101% overspeed | Shows compressor speed; indicates engine power demand |
| **Dual Tachometer (Nr/N2)** | RPM or percentage — two needles | Nr: 324 ±3 RPM (100%); N2: 6,600 RPM (100%) | Nr < 294 = RPM warning; Nr > 339 = overspeed | **Most critical instrument** — two needles should be "married" (overlapping) in normal flight; split needles = governor not holding or engine/rotor disconnect |
| **Fuel Flow Indicator** | Pounds per hour | 220-350 lbs/hr typical | Varies with power | Cross-reference with fuel quantity for endurance calculation |
| **Engine Oil Pressure** | PSI | 35-70 PSI | < 35 PSI caution; < 25 PSI warning | Check during start and continuously in flight |
| **Engine Oil Temperature** | Degrees Celsius | < 107°C | > 107°C = land as soon as practicable | Increases during high-power operations; slow to respond |
| **Transmission Oil Pressure** | PSI | 30-70 PSI | < 30 PSI = XMSN OIL PRESS caution | Indicates main gearbox lubrication |
| **Transmission Oil Temperature** | Degrees Celsius | < 110°C | > 120°C = land immediately | Slower to respond than engine oil temp |

#### Dual Tachometer — Special Emphasis

The dual tachometer is the **single most important instrument** in the UH-1H. It displays two needles:

- **Nr (rotor RPM):** Outer needle — shows main rotor speed
- **N2 (engine/power turbine RPM):** Inner needle — shows power turbine speed

**Normal indication:** Both needles overlapping ("married") at 324 RPM / 100%. This means the engine is driving the rotor at the correct speed.

**Split needles:**
- Nr higher than N2 → engine is not keeping up (power loss, correlator issue, governor failing)
- N2 higher than Nr → unusual; may indicate transmission issue or tachometer malfunction
- In autorotation: Nr will be higher than N2 because the freewheeling unit has disconnected and the rotor is being driven by airflow, not the engine

---

### 2.5 Caution/Advisory Panel

The caution/advisory panel is located on the **instrument panel, typically pilot's side center-left area**. It contains individual warning lights for each monitored system.

| Light | System | Meaning | Immediate Action |
|---|---|---|---|
| **MASTER CAUTION** | All systems | Any individual caution light has illuminated | Check individual caution lights, take appropriate action |
| **RPM** | Rotor/Engine | Nr has dropped below ~294 RPM or governor anomaly detected | Verify Nr on tach; adjust throttle/collective; check governor |
| **ENGINE OIL PRESS** | Engine | Oil pressure below minimum (< 35 PSI) | Land as soon as practicable; monitor temp |
| **XMSN OIL PRESS** | Transmission | Trans oil pressure below minimum (< 30 PSI) | Land as soon as possible; transmission failure risk |
| **ENGINE OIL TEMP** | Engine | Oil temperature exceeding limit (> 107°C) | Reduce power; land as soon as practicable |
| **XMSN OIL TEMP** | Transmission | Trans oil temperature exceeding limit (> 120°C) | Reduce power; land immediately |
| **FUEL BOOST** | Fuel | Fuel boost pump inoperative or fuel pressure low | Check boost pump switch; gravity feed backup available in level flight |
| **FUEL FILTER** | Fuel | Fuel filter bypassed due to contamination | Land as soon as practicable; fuel contamination |
| **CHIP DET** | Transmission/Engine | Metallic particles detected in oil (chip detector) | Land as soon as possible; potential component failure |
| **GEN** | Electrical | Generator failure — DC bus on battery power only | Check GEN switch; shed non-essential loads; battery endurance ~30 min |
| **GOV EMER** | Engine | Governor malfunction or emergency mode activated | Switch to manual throttle if governor is non-functional |
| **FIRE** | Engine | T-handle fire warning — fire detected | Engine fire boldface: Emergency shutdown procedure |

**Master Caution Reset:** After acknowledging a caution, the master caution light can be reset by pressing it. Individual system caution lights remain illuminated as long as the condition persists.

> *⚠ Realism Divergence: The real UH-1H caution panel has additional lights for systems not fully modeled in DCS (e.g., specific hydraulic system cautions, cargo hook warnings, auxiliary fuel system lights). DCS presents the most operationally relevant caution lights. The student should learn all DCS caution lights and understand that the real aircraft has a more extensive caution panel.*

---

### 2.6 Center Pedestal — Radio Stack

The center pedestal houses the three primary communication radios, the transponder, and the audio control panels. All radios are **manually tuned** using physical frequency selector knobs — there are no digital presets (with one exception: the UHF has preset channels).

#### Communication Radios

| Radio | Designation | Band | Frequency Range | Primary Use | DCS Keybind (Default) |
|---|---|---|---|---|---|
| **VHF-AM** | AN/ARC-134 | VHF Amplitude Modulation | 116.000-149.975 MHz | ATC communications, common traffic advisory frequency (CTAF) | `V` key (transmit) |
| **UHF-AM** | AN/ARC-51BX | UHF Amplitude Modulation | 225.000-399.975 MHz | Military ATC, inter-aircraft, GUARD (243.0 MHz) | `Y` key (transmit) |
| **FM** | AN/ARC-131 | VHF Frequency Modulation | 30.000-75.975 MHz | Tactical/inter-flight communication, ground units | `C` key (transmit) |

**AN/ARC-134 (VHF-AM):**
- Tuned via four frequency selector knobs (100s, 10s, 1s, 0.1s MHz)
- Volume knob on the radio face
- Used for civilian and military ATC, CTAF, approach, tower, ground, ATIS
- In DCS: most airfield ATC communication uses this radio

**AN/ARC-51BX (UHF-AM):**
- Dual mode: **Manual** (tuned via frequency selector knobs) or **Preset** (20 preset channels selectable by channel knob)
- Mode switch: OFF / MANUAL / PRESET / GUARD
- GUARD position monitors 243.0 MHz (international military emergency frequency)
- In DCS: used for military communication, awacs, inter-flight coordination

**AN/ARC-131 (FM):**
- Tuned via frequency selector knobs
- Volume knob and squelch control
- Primary tactical radio for ground force communication and inter-flight
- In DCS: used for SRS (SimpleRadio Standalone) tactical nets when multiplayer

**Physical Location in Cockpit:**

The radios are stacked vertically on the center pedestal, typically:
1. **VHF-AM (top)** — most frequently used, easiest to reach
2. **UHF-AM (middle)** — preset channel knob is prominent
3. **FM (bottom)** — less frequently adjusted in BQT operations

Each radio face has its own ON/OFF/volume knob and frequency selection mechanism. In DCS, all knobs are clickable — left-click to increase, right-click to decrease, scroll wheel for fine adjustment.

---

### 2.7 Audio Control Panel

Each crew station (pilot and copilot) has its own **audio control panel** that determines which radios are heard and which radio is selected for transmit.

| Control | Function | Notes |
|---|---|---|
| **VHF volume knob** | Sets receive volume for VHF-AM radio | Turn to desired volume; affects headset audio only |
| **UHF volume knob** | Sets receive volume for UHF-AM radio | |
| **FM volume knob** | Sets receive volume for FM radio | |
| **NAV volume knob** | Sets volume for navigation audio (VOR ident, ADF, marker beacon) | Turn up to hear Morse code ident signals |
| **ICS volume knob** | Sets intercom volume | For crew communication |
| **Transmit selector switch** | Selects which radio transmits when the cyclic trigger is keyed | Positions: VHF / UHF / FM / ICS |

**Keying the radio in DCS:**
- Default keyboard shortcuts: `V` (VHF), `Y` (UHF), `C` (FM), or use the cyclic trigger (mapped to joystick button) to transmit on the currently selected radio.
- For realistic operation: Set the transmit selector switch to the desired radio and use the cyclic trigger button.

> *⚠ Realism Divergence: The real UH-1H audio panel has a more nuanced hot-mic/cold-mic configuration for the ICS and specific radio-disable switches. DCS simplifies the audio routing — the student selects a radio and keys it. In reality, crew communication discipline (who monitors which frequency, hot-mic procedures for crew coordination) is a significant training topic. DCS players in multiplayer with SRS will experience more realistic radio management.*

---

### 2.8 Navigation Equipment

#### AN/ARN-83 ADF (Automatic Direction Finder)

| Parameter | Detail |
|---|---|
| **Function** | Receives NDB (Non-Directional Beacon) signals and displays bearing to station |
| **Frequency Range** | 190-1,799.5 kHz |
| **Tuning** | Manual frequency selector knobs on the ADF control head (center pedestal or lower instrument panel) |
| **Display** | ADF bearing pointer on the compass card (instrument panel) — pointer indicates relative bearing to the NDB |
| **Modes** | ADF (active bearing), ANT (antenna/audio only, no bearing), OFF |

#### AN/ARN-82 VOR/ILS Receiver

| Parameter | Detail |
|---|---|
| **Function** | Receives VOR and ILS (localizer + glideslope) signals for navigation and approaches |
| **Frequency Range** | 108.0-117.95 MHz (VOR/ILS) |
| **Tuning** | Manual frequency selector knobs on the VOR control head |
| **Display** | Course Deviation Indicator (CDI) — vertical needle shows left/right deviation from selected course; TO/FROM flag; glideslope needle (for ILS) |
| **OBS (Omni-Bearing Selector)** | Knob on the CDI to select desired course/radial |

#### Marker Beacon Receiver

- Receives 75 MHz marker beacon signals (outer, middle, inner markers for ILS approaches)
- Indicator lights on instrument panel: blue (outer), amber (middle), white (inner)
- Audio tones through headset

#### Radar Altimeter

| Parameter | Detail |
|---|---|
| **Function** | Displays absolute altitude above ground level (AGL) via radar pulse |
| **Range** | 0-5,000 ft AGL (typical) |
| **Low-Altitude Warning Bug** | Set by the pilot — triggers audio/visual warning when descending below set altitude |
| **Location** | Instrument panel |
| **Usage** | Critical for low-level flight, approach minimums, terrain clearance |

#### Transponder

| Parameter | Detail |
|---|---|
| **Designation** | AN/APX-72 (or similar) |
| **Modes** | OFF / STANDBY / ON (Mode A) / ALT (Mode A+C, altitude reporting) |
| **Squawk Code** | Set via four digit selector wheels (0000-7777 octal) |
| **IDENT** | Button that highlights the aircraft on ATC radar for 15-30 seconds |

---

### 2.9 Pilot Controls — Collective and Cyclic

#### Collective Grip

The collective lever is operated by the pilot's **left hand** (right seat). It moves up and down to change the pitch of all main rotor blades simultaneously (increasing/decreasing total rotor thrust).

| Control | Location on Collective | Function | DCS Interaction |
|---|---|---|---|
| **Twist-Grip Throttle** | Grip end — rotates CW (increase) / CCW (decrease) | Controls engine fuel flow; works with correlator/governor | Axis mapped to throttle; or keyboard for fine adjust |
| **Idle Stop Release** | Grip — button/latch | Allows throttle to advance past IDLE detent to FLY | Must be pressed to enter flight RPM range |
| **Landing Light Switch** | Grip — toggle | Extends/retracts and activates landing light | Left-click or mapped key |
| **Searchlight Control** | Grip — directional switch | Controls external searchlight direction (if installed) | Clickable or mapped |
| **Radio Trigger (1st Detent)** | Grip — trigger | Keys ICS (intercom) | Squeeze lightly for ICS |
| **Radio Trigger (2nd Detent)** | Grip — trigger (full squeeze) | Keys selected radio (per audio panel transmit selector) | Full squeeze for radio transmit |
| **Collective Friction** | Friction lock on collective lever | Adjusts resistance to collective movement — set to prevent collective creep while allowing deliberate changes | Adjust to preference; too tight = hard to change power; too loose = collective drifts |

#### Cyclic Grip

The cyclic stick is operated by the pilot's **right hand** (right seat). It tilts the rotor disc in the desired direction of movement.

| Control | Location on Cyclic | Function | DCS Interaction |
|---|---|---|---|
| **Force Trim Release Button** | Grip — prominent button (usually thumb) | Releases magnetic brake force trim; press and hold to reposition cyclic, release to lock | Mapped to joystick button — most used button in flight |
| **Cargo Release** | Grip — guarded button | Releases external sling load from cargo hook | Guarded; not used in BQT except familiarization |
| **Weapons Release** | Grip — button (if equipped) | Fires selected weapon | Not used in BQT; familiarization only |

#### Pedals

Anti-torque pedals control tail rotor pitch (and thus yaw):
- **Left pedal:** Increases tail rotor thrust → nose yaws LEFT (counters increased torque when collective is raised)
- **Right pedal:** Decreases tail rotor thrust → nose yaws RIGHT (counters decreased torque when collective is lowered)
- Pedals have an adjustment mechanism to accommodate different pilot leg lengths.

---

### 2.10 Lighting

#### Cockpit Lighting

| Control | Function | Notes |
|---|---|---|
| **Instrument Panel Lights** | Illuminates steam gauges (rheostat-controlled brightness) | Use minimum brightness necessary; avoid glare |
| **Console Lights** | Illuminates overhead console and pedestal | Separate rheostat from instrument lights |
| **Dome Light (Utility Light)** | Overhead white light for cabin illumination | For map reading, pre-flight checks; turn off before flight |
| **Caution Panel Brightness** | Adjusts brightness of caution/advisory lights | Dim for night; bright for day |

#### Exterior Lighting

| Light | Function | Switch Location | Notes |
|---|---|---|---|
| **Position/Nav Lights** | Red (left), green (right), white (tail) | Overhead or lighting panel | Required for night flight and when required by regulations |
| **Anti-Collision Beacon** | Red rotating beacon on top and bottom of fuselage | Overhead or lighting panel | Typically ON whenever rotor is turning |
| **Landing Light** | High-intensity forward light (retractable) | Collective grip switch | For final approach and landing; retract for cruise to reduce drag and avoid blinding other pilots |
| **Searchlight** | Directional light (if installed) | Collective grip directional control | For ground illumination; not standard on all UH-1H |

> *⚠ Realism Divergence: DCS models the UH-1H cockpit lighting with adjustable rheostats and clickable light switches. NVG-compatible lighting (NVIS green) is not modeled in the standard DCS UH-1H — the cockpit lighting is the original white/red configuration. Real UH-1H aircraft in later service were modified for NVG compatibility with green-filtered instruments and NVG-compatible exterior lights.*

---

### 2.11 Cargo Hook and Sling Load Controls

| Control | Location | Function | Notes |
|---|---|---|---|
| **Cargo Hook Release (Pilot)** | Cyclic grip — guarded button | Electrically releases external sling load | BQT familiarization only |
| **Cargo Hook Release (Copilot)** | Copilot cyclic or instrument panel | Backup release | |
| **Cargo Hook Armed/Safe** | Instrument panel or subpanel | Arms electrical release circuit | Must be ARMED for electrical release to function |
| **Manual/Emergency Release** | Cabin crew position | Mechanical backup release | Operated by crew chief/door gunner |

**Scope:** Sling load operations require specialized training beyond BQT. The student is introduced to the cargo hook system for identification purposes only — no sling load training is conducted in this course.

---

### 2.12 Armament Panel (Familiarization Only)

If the UH-1H is configured with weapons (door-mounted M60 machine guns, rocket pods), the armament panel is located on the pilot's subpanel or instrument panel. BQT-level familiarization includes:

| Control | Function | Notes |
|---|---|---|
| **Master Arm** | ARM / SAFE — enables weapon circuits | SAFE for all BQT operations |
| **Weapon Select** | Selects weapon station/type | Identification only |
| **Weapons Release** | Fires selected weapon | On cyclic grip; not used in BQT |

> *⚠ Realism Divergence: The DCS UH-1H comes with door gunner positions (M60D machine guns) and can be equipped with rocket pods (M134 minigun, FFAR rockets). In multiplayer, human players can operate the door guns. The armament system is functional in DCS and well-modeled, but is outside BQT scope.*

---

### Instructor Notes — Module 2

| Common Student Error | Correction |
|---|---|
| **Cannot locate engine instruments quickly** | Blindfold cockpit exercise: instructor calls out an instrument, student must point to its location. Repeat until immediate |
| **Neglects dual tachometer significance** | Emphasize the "married needles" concept; have student deliberately split needles (governor OFF exercise) to recognize the visual cue |
| **Forgets to set inverter before expecting gyro instruments** | Include inverter in startup flow; explain that AI and DG will tumble/not function without AC power |
| **Cannot tune radios efficiently** | Practice: instructor calls a frequency, student must tune the correct radio to that frequency within 15 seconds. Repeat for all three radios |
| **Ignores caution panel during flight** | Establish a "caution panel scan" as part of the instrument scan cycle — brief glance at the caution panel every 30-60 seconds |
| **Does not understand force trim** | Dedicated ground exercise: with engine running, have student set and release force trim at different cyclic positions. Feel the difference between trimmed and out-of-trim flight |
| **Confusion between pilot and copilot instruments** | Clearly identify which panel is the pilot's reference. Establish that the pilot (right seat) uses the right-side instrument panel as primary |

---

## Module 3: Communications

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Tune each of the three communication radios (VHF-AM, UHF-AM, FM) to a specified frequency within 15 seconds.
2. Select the appropriate radio for transmit using the audio control panel.
3. Monitor multiple frequencies simultaneously and adjust individual radio volumes.
4. Use proper radio phraseology for all BQT operations (startup, taxi, takeoff, pattern, approach, landing, shutdown).
5. Operate the intercom system for crew coordination.
6. Configure radios for DCS single-player ATC communication and understand Easy Communication mode vs. realistic radio operation.
7. Explain guard frequency monitoring procedures and when to use guard.

---

### 3.1 Radio Communication Fundamentals

The UH-1H is equipped with **three independent communication radios** and an **intercom system (ICS)**. Unlike modern aircraft with digital frequency presets and radio management systems, the UH-1H pilot must manually tune each radio by rotating physical frequency selector knobs. This requires:

- **Pre-flight frequency planning:** Before engine start, know which frequencies you will need and write them on a kneecard or mark them on your mission briefing. You cannot look up frequencies in a database while flying.
- **Manual tuning proficiency:** Changing frequencies while flying the helicopter requires dividing attention. Practice until frequency changes become muscle memory.
- **Audio management:** With three radios and ICS active, the cockpit can become noisy. The pilot must manage volumes to prioritize the most important radio while maintaining awareness of secondary frequencies.

#### Radio Assignment by Mission Phase (BQT Standard)

| Mission Phase | Primary Radio | Frequency Type | Notes |
|---|---|---|---|
| **Startup / Ground Ops** | VHF-AM (ARC-134) | Ground / Clearance Delivery | Request startup, taxi clearance |
| **Taxi** | VHF-AM | Ground frequency | Ground control for taxi instructions |
| **Takeoff / Pattern** | VHF-AM | Tower frequency | Takeoff clearance, pattern calls |
| **Departure / Enroute** | VHF-AM or UHF-AM | Departure / Approach / Area freq | Transition from tower to area control |
| **Tactical / Inter-flight** | FM (ARC-131) | Mission-assigned FM frequency | Communication with wingman, ground units |
| **Emergency** | UHF-AM | GUARD 243.0 MHz / VHF GUARD 121.5 MHz | Emergency declarations, distress calls |
| **Approach / Landing** | VHF-AM | Approach / Tower | Pattern entry, approach clearance, landing |

---

### 3.2 VHF-AM Radio — AN/ARC-134

| Parameter | Detail |
|---|---|
| **Band** | VHF Amplitude Modulation |
| **Frequency Range** | 116.000-149.975 MHz |
| **Channel Spacing** | 25 kHz |
| **Tuning** | Four rotary knobs: 100 MHz, 10 MHz, 1 MHz, 0.1/0.025 MHz |
| **Controls** | Volume / OFF knob, frequency selector knobs |
| **Location** | Center pedestal — top of radio stack |
| **Primary Use** | ATC communication (ground, tower, approach, center, CTAF) |
| **DCS Transmit Key** | `V` (default) |

**Tuning Procedure (Example: Tune to 124.000 MHz):**
1. Set the **100 MHz** knob to `1`
2. Set the **10 MHz** knob to `2`
3. Set the **1 MHz** knob to `4`
4. Set the **0.1 MHz** knob to `0.0`
5. Verify the frequency display reads `124.000`

In DCS: left-click on each knob to increase, right-click to decrease. Mouse scroll wheel also works for fine adjustment.

---

### 3.3 UHF-AM Radio — AN/ARC-51BX

| Parameter | Detail |
|---|---|
| **Band** | UHF Amplitude Modulation |
| **Frequency Range** | 225.000-399.975 MHz |
| **Channel Spacing** | 25 kHz |
| **Tuning (Manual)** | Frequency selector knobs (100, 10, 1, 0.1, 0.025 MHz) |
| **Tuning (Preset)** | 20 preset channel selector knob — channels pre-programmed in DCS mission editor |
| **Mode Switch** | OFF / MANUAL / PRESET / GUARD |
| **Controls** | Volume knob, mode switch, frequency/channel selectors, squelch |
| **Location** | Center pedestal — middle of radio stack |
| **Primary Use** | Military ATC, inter-aircraft (military), GUARD (243.0 MHz) |
| **DCS Transmit Key** | `Y` (default) |

**Mode Switch Positions:**

| Mode | Function |
|---|---|
| **OFF** | Radio is off |
| **MANUAL** | Frequency set by manual tuning knobs |
| **PRESET** | Frequency determined by preset channel knob (1-20); channels programmed before mission |
| **GUARD** | Monitors 243.0 MHz (military emergency frequency) continuously; transmit on guard |

**GUARD Frequency (243.0 MHz):** The international military distress frequency. In emergency situations, the pilot transmits "MAYDAY, MAYDAY, MAYDAY" on guard. In DCS, guard is monitored by AWACS and some AI ATC facilities. When not actively using UHF for communication, good practice is to leave the UHF in GUARD mode.

---

### 3.4 FM Radio — AN/ARC-131

| Parameter | Detail |
|---|---|
| **Band** | VHF Frequency Modulation |
| **Frequency Range** | 30.000-75.975 MHz |
| **Channel Spacing** | 25 kHz |
| **Tuning** | Frequency selector knobs |
| **Controls** | Volume / OFF knob, squelch, frequency selectors |
| **Location** | Center pedestal — bottom of radio stack |
| **Primary Use** | Tactical communication (ground units, inter-flight, FAC), DCS SRS multiplayer |
| **DCS Transmit Key** | `C` (default) |

**FM radio characteristics:**
- FM provides clearer audio in the VHF-low band than AM, and is resistant to certain types of interference.
- Primary tactical radio for Army aviation — used for communication with ground forces (JTACs, ground commanders), wingman/flight, and tactical nets.
- In DCS single-player, the FM radio is less frequently used. In multiplayer with SRS (SimpleRadio Standalone), FM becomes critical for tactical communication.

---

### 3.5 Intercom System (ICS)

| Parameter | Detail |
|---|---|
| **Function** | Crew communication between pilot, copilot, and crew chief/door gunner positions |
| **Hot Mic** | When enabled, all ICS-connected crew hear each other continuously without keying |
| **Cold Mic (PTT)** | Requires pressing the radio trigger to first detent to key ICS |
| **Volume** | Individual ICS volume on each crew station's audio panel |
| **ICS Positions** | PILOT, COPILOT, CREW (cabin positions) |

**ICS Keying:**
- **First detent** on the collective radio trigger: Keys ICS only (crew hears you, radio does not transmit)
- **Second detent** (full squeeze): Keys the selected radio (transmits on the radio selected by the transmit selector switch)

This two-stage trigger is critical for crew coordination. The pilot can talk to the crew without transmitting on the radio, or can talk on the radio (which the crew also hears through the ICS).

---

### 3.6 Standard Radio Calls — BQT Operations

The following are standard radio phraseology examples for BQT training operations. All calls use the aircraft callsign followed by position/intentions.

#### Startup

> **Pilot:** "*[Airfield] Ground, [Callsign], parking spot [number], request startup, [ATIS information].*"
> **ATC:** "*[Callsign], [Airfield] Ground, startup approved, altimeter [setting], wind [direction/speed].*"

#### Taxi (Hover Taxi)

> **Pilot:** "*[Airfield] Ground, [Callsign], parking spot [number], request hover taxi to runway [number].*"
> **ATC:** "*[Callsign], hover taxi to runway [number] via [taxiway], winds [direction/speed].*"
> **Pilot:** "*Hover taxi to runway [number] via [taxiway], [Callsign].*"

#### Takeoff

> **Pilot:** "*[Airfield] Tower, [Callsign], holding short runway [number], ready for takeoff.*"
> **ATC:** "*[Callsign], runway [number], winds [direction/speed], cleared for takeoff.*"
> **Pilot:** "*Cleared for takeoff, runway [number], [Callsign].*"

#### Pattern Calls

> **Pilot (Downwind):** "*[Airfield] Tower, [Callsign], downwind runway [number], full stop.*"  
> **Pilot (Base):** "*[Callsign], turning base.*"  
> **Pilot (Final):** "*[Callsign], final, full stop.*"

#### Landing

> **ATC:** "*[Callsign], cleared to land runway [number], winds [direction/speed].*"
> **Pilot:** "*Cleared to land, [Callsign].*"

#### Go-Around

> **Pilot:** "*[Callsign], going around.*"
> **ATC:** "*[Callsign], roger, make left/right traffic, report downwind.*"

#### Shutdown

> **Pilot:** "*[Airfield] Ground, [Callsign], [location], shutting down.*"
> **ATC:** "*[Callsign], roger.*"

---

### 3.7 DCS-Specific Radio Operations

#### Easy Communication Mode

DCS offers an "Easy Communication" mode that bypasses the need for physically tuned radios. When enabled:
- A menu appears on screen with available ATC options
- The player selects from numbered menu items
- No actual radio tuning or frequency management is required
- Useful for early training when the student is overwhelmed by other tasks

**BQT Training Progression:**
1. **Phase 1:** Use Easy Communication to reduce workload during initial hover and flight training
2. **Phase 2:** Transition to tuning the VHF-AM radio for ATC while using Easy Communication for backup
3. **Phase 3:** Full realistic radio operation — all three radios manually tuned, Easy Communication disabled

#### SRS (SimpleRadio Standalone) Integration

In multiplayer DCS, SRS replaces Easy Communication with realistic radio simulation:
- Each radio in the cockpit maps to a real voice channel
- The pilot must have the correct frequency tuned to hear and transmit
- Radio selection, volume, and transmit keying all function realistically
- SRS adds radio effects (static, distance-based signal degradation, line-of-sight limitations)

SRS is not required for BQT (which is primarily single-player), but students who progress to multiplayer should understand that SRS requires the full radio management skills taught in this module.

#### DCS ATC Frequencies

In DCS missions, airfield frequencies are typically:
- Published in the mission briefing
- Available via the F10 map (radio frequency information)
- Standard DCS airfield frequencies often use VHF-AM for tower/ground

The student should always check the mission briefing for frequencies and write them on a kneecard before starting the engine.

> *⚠ Realism Divergence: DCS ATC is significantly simplified compared to real-world ATC. There is no clearance delivery, no ATIS (usually), no radar vectors for VFR traffic, and no handoff between ATC facilities in most single-player missions. Radio calls are handled through a menu system even in "realistic" radio mode — the student selects from a list of available calls rather than free-speaking. In multiplayer with human ATC (via SRS and LotATC or similar), communication is more realistic. The student should learn proper phraseology even though DCS does not require it, as it prepares them for multiplayer and builds good habits.*

---

### Instructor Notes — Module 3

| Common Student Error | Correction |
|---|---|
| **Transmitting on wrong radio** | Before every transmission, verify the transmit selector switch position. Develop the habit: "Check selector, key radio." |
| **Forgetting to tune tower after ground** | Write frequency changes on the kneecard in sequence (ground → tower → departure). Brief the frequency plan before starting |
| **Talking on radio when intending ICS** | Practice the two-detent trigger: first detent = ICS, full squeeze = radio. Have the student practice distinguishing the two detents |
| **Not monitoring guard** | Establish UHF in GUARD mode as a standard configuration when UHF is not being used for active communication |
| **Transmitting without listening first** | "Listen before you talk" — monitor the frequency for at least 5 seconds before transmitting to avoid stepping on other traffic |
| **Volume management problems** | Teach a standard volume setup: primary radio loudest, secondary radios at half volume, ICS at comfortable level |
| **Frequency confusion between radios** | Color-code the kneecard: VHF frequencies in one color, UHF in another, FM in a third |

---

## Module 4: Ground Operations

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Perform a complete cold-and-dark startup of the UH-1H from battery ON through engine running, governor engaged, and all avionics powered — switch by switch, without reference to a checklist.
2. Recognize and correctly respond to hot start, hung start, and no-light-off abort conditions.
3. Demonstrate understanding of the throttle correlator and governor interaction through ground exercises.
4. Perform a complete before-takeoff check, verifying all engine and flight systems are within limits.
5. Engage the rotor from ground idle to flight RPM correctly and safely.
6. Perform hover taxi at 3-5 ft skid height maintaining heading, altitude, and track.
7. Perform a hover power check and determine if sufficient power is available for the intended operation (IGE and OGE).

---

### 4.1 Cold-and-Dark Startup — Full Procedure

The following is the complete switch-by-switch startup procedure from a cold-and-dark state (all switches off, engine not running, rotor stationary).

**Prerequisites:** Aircraft on firm, level ground. All doors secured or positioned as desired. No ground personnel within rotor arc. Wind conditions noted.

#### Phase 1: Electrical Power

| Step | Action | Cockpit Location | Expected Indication | DCS Click |
|---|---|---|---|---|
| 1 | **Battery** — ON | Overhead console — Electrical panel | Caution panel illuminates (multiple lights); voltmeter shows ~24V battery | Left-click toggle |
| 2 | **Caution Panel Check** — verify lights illuminated | Instrument panel — Caution panel | Multiple caution lights ON (RPM, GEN, etc.) — this is normal on battery before engine start | Visual check |
| 3 | **Caution Light Test** — press and hold | Overhead console — Test panel | ALL caution lights should illuminate; verify no burned bulbs | Left-click and hold |
| 4 | **Inverter** — ON | Overhead console — Electrical panel | AC power available; attitude indicator begins erecting (may take 2-3 minutes to stabilize) | Left-click toggle |

#### Phase 2: Fuel System

| Step | Action | Cockpit Location | Expected Indication | DCS Click |
|---|---|---|---|---|
| 5 | **Fuel Valve** — ON | Overhead console — Fuel panel (guarded) | Fuel valve open; no immediate cockpit indication except valve position | Lift guard, left-click toggle |
| 6 | **Fuel Boost Pump** — ON | Overhead console — Fuel panel | FUEL BOOST caution light extinguishes (was on due to no fuel pressure); fuel pressure established | Left-click toggle |
| 7 | **Fuel Quantity** — check | Instrument panel — Fuel quantity gauge | Verify adequate fuel for planned mission (note in pounds) | Visual check |

#### Phase 3: Pre-Start Checks

| Step | Action | Expected Indication |
|---|---|---|
| 8 | **Throttle** — verify CLOSED (full counterclockwise on twist-grip) | Throttle at fuel cutoff position; no fuel to engine |
| 9 | **Collective** — full DOWN and locked (friction set) | Collective at bottom of travel; minimum blade pitch |
| 10 | **Pedals** — centered or slightly left (anticipate torque during start) | Neutral position |
| 11 | **Cyclic** — centered | Neutral position |
| 12 | **Area clear** — visually verify no personnel or obstacles in rotor arc | Look out both sides and behind |
| 13 | **Governor (GOV) switch** — OFF (for start) | Governor disengaged; will be engaged after engine stabilizes |

> *⚠ Realism Divergence: In the real UH-1H, the pre-start procedure includes checking the fire extinguisher, verifying the rotor brake is released, checking tie-downs are removed, and conducting a thorough walk-around inspection. DCS does not model these items. The student should understand they exist in the real-world procedure.*

#### Phase 4: Engine Start

| Step | Action | Cockpit Location | Expected Indication | Critical Monitoring |
|---|---|---|---|---|
| 14 | **Starter Button** — press and HOLD | Overhead console — Engine panel | Starter engages; N1 begins to increase from 0% | Monitor N1 and EGT |
| 15 | Monitor **N1 increasing** | Instrument panel — N1 gauge | N1 rises steadily: 5%, 10%, 15%... | Smooth acceleration; no stagnation |
| 16 | At **~15% N1** — advance throttle to **IDLE** | Collective grip — twist throttle clockwise to IDLE detent | Fuel introduced to combustion chamber | Watch for EGT rise (light-off) |
| 17 | Monitor **EGT** for light-off | Instrument panel — EGT gauge | EGT begins to rise — confirms ignition | **If no EGT rise by ~25% N1 → ABORT** |
| 18 | Monitor **EGT during acceleration** | EGT gauge | EGT rises, peaks, then settles | **Must not exceed 720°C (starting limit)** — if exceeding → ABORT (hot start) |
| 19 | Monitor **N1 acceleration** to idle | N1 gauge | N1 accelerates through to ~58-62% and stabilizes | **If N1 stagnates below idle → ABORT** (hung start) |
| 20 | **Release starter button** | Overhead console | Starter disengages; N1 at idle, EGT settling | Starter has duty cycle limits |
| 21 | **Stabilize at ground idle** (~30-60 seconds) | All engine instruments | N1: ~58-62%, EGT: settling below 610°C, oil pressure: rising into range (35-70 PSI), Nr: beginning to increase | Allow engine to thermally stabilize before advancing power |

**Start Abort Decision Matrix:**

| Condition | Recognition | Action | Wait Before Reattempt |
|---|---|---|---|
| **No light-off** | No EGT rise by 25% N1 | Throttle to CLOSED; release starter; motor for 30 sec to purge | Check fuel valve, boost pump; wait 30 sec |
| **Hot start** | EGT exceeding 720°C | Throttle to CLOSED immediately; motor to purge | Wait 2 min for turbine cooling |
| **Hung start** | N1 stagnates below ~55% with rising EGT | Throttle to CLOSED; motor to clear | Check battery voltage; may need external power |
| **Over-temp during acceleration** | EGT above limits but N1 continues to idle | Throttle to CLOSED; engine may be damaged | Real aircraft: inspect before restart. DCS: restart permitted |

> *⚠ Realism Divergence: The real UH-1H requires strict starter duty cycle management: maximum 60 seconds of cranking, then a mandatory 2-minute cool-down before the next start attempt. Three start attempts maximum before a 30-minute cooling period. DCS does not enforce these limitations — the student can crank the starter continuously without damage. However, the student should practice respecting the duty cycle limits as part of procedural discipline. Real-world hot starts can cause turbine blade damage, creep, or failure; DCS models the temperature exceedance but not cumulative thermal damage.*

#### Phase 5: Post-Start — Generator, Governor, Systems

| Step | Action | Cockpit Location | Expected Indication |
|---|---|---|---|
| 22 | **Generator (GEN)** — ON | Overhead console — Electrical panel | GEN caution light extinguishes; voltmeter shows 28V; generator powering bus |
| 23 | **Governor (GOV)** — ON | Overhead console — Engine panel | Governor engages; Nr begins to be governed (small Nr adjustment may be noted) |
| 24 | **RPM Warning Audio** — ON | Overhead console — Engine panel | Low-RPM warning audio system armed |
| 25 | **Engine Oil Pressure** — check | Instrument panel — Engine oil pressure gauge | 35-70 PSI (within ~30 seconds of start) |
| 26 | **Engine Oil Temperature** — check | Instrument panel — Engine oil temp gauge | Rising toward operating range; may take several minutes |
| 27 | **Transmission Oil Pressure** — check | Instrument panel — Trans oil pressure gauge | 30-70 PSI |
| 28 | **Transmission Oil Temperature** — check | Instrument panel — Trans oil temp gauge | Rising toward operating range |
| 29 | **EGT** — verify below continuous limit | Instrument panel — EGT gauge | < 610°C and stable |
| 30 | **Caution Panel** — verify clear | Instrument panel — Caution panel | All caution lights extinguished except any expected for current state |

#### Phase 6: Avionics Power-On

| Step | Action | Cockpit Location | Notes |
|---|---|---|---|
| 31 | **VHF-AM (AN/ARC-134)** — ON and tune | Center pedestal — top radio | Tune to ground/ATIS frequency; set volume |
| 32 | **UHF-AM (AN/ARC-51BX)** — ON, set to GUARD or manual freq | Center pedestal — middle radio | GUARD mode or tune to assigned UHF frequency |
| 33 | **FM (AN/ARC-131)** — ON and tune if required | Center pedestal — bottom radio | Tune to assigned FM frequency |
| 34 | **Audio Control Panel** — configure | Center pedestal — audio panels | Set volumes for all radios; select VHF for transmit (typical BQT start) |
| 35 | **ADF (AN/ARN-83)** — ON if required | Navigation equipment panel | Tune to NDB frequency if planned |
| 36 | **VOR/ILS (AN/ARN-82)** — ON if required | Navigation equipment panel | Tune to VOR frequency if planned |
| 37 | **Transponder** — STANDBY (then ON/ALT before takeoff) | Center pedestal | Set squawk code per clearance; leave in STANDBY until ready for taxi |
| 38 | **Radar Altimeter** — ON, set low-altitude warning bug | Instrument panel | Set bug to desired warning altitude |
| 39 | **Barometric Altimeter** — set current altimeter setting | Instrument panel — altimeter | Set Kollsman window to current QNH (in. Hg) per ATIS or weather briefing |
| 40 | **Heading Indicator / DG** — set to magnetic compass | Instrument panel — DG | Uncage, align to magnetic compass reading (requires aircraft stationary on known heading) |

> *⚠ Realism Divergence: In the real UH-1H, the attitude indicator and directional gyro require 2-5 minutes to erect and stabilize after AC power is applied (inverter ON). DCS models a shorter gyro erection time. The student should develop the habit of turning on the inverter early in the startup sequence and verifying gyro stabilization before flight.*

---

### 4.2 Throttle Correlation and Governor Exercise

**Purpose:** To give the student a visceral understanding of how the correlator and governor manage RPM, and what happens when the governor fails.

**Exercise 1 — Normal Operation (Governor ON):**
1. Engine at ground idle, governor ON.
2. Slowly raise the collective 1-2 inches. Observe:
   - Nr remains stable (governor corrects)
   - EGT increases (more fuel flow for more power)
   - Torque increases (more load on transmission)
3. Lower collective back to bottom. Observe:
   - Nr remains stable (governor corrects back)
   - EGT and torque decrease
4. **Lesson:** The correlator and governor together maintain Nr regardless of collective position.

**Exercise 2 — Governor OFF (Manual Throttle):**
1. Engine at ground idle, turn governor **OFF**.
2. Slowly raise the collective 1-2 inches. Observe:
   - Nr begins to **drop** (the correlator adds fuel, but not enough)
   - The pilot must twist the throttle to add fuel and recover Nr
3. Lower collective. Observe:
   - Nr begins to **rise** (correlator reduces fuel, but not enough)
   - The pilot must twist throttle back to prevent overspeed
4. **Lesson:** Without the governor, the pilot must continuously manage throttle to maintain Nr. The correlator only provides approximate compensation.

**Exercise 3 — Sensitivity Check:**
1. Governor ON. Make a rapid collective input (raise and lower quickly).
2. Observe the momentary Nr excursion before the governor catches up.
3. **Lesson:** Even with the governor, rapid collective movements cause transient Nr changes. Smooth, deliberate collective inputs give the governor time to compensate.

> *⚠ Realism Divergence: In DCS, governor behavior is well-modeled and the throttle correlation is representative. However, the physical sensation of the twist-grip throttle on the collective is difficult to replicate with a desktop HOTAS. Real UH-1H throttle management requires fine wrist rotation while the hand is gripping the collective — a dexterity skill that takes significant practice. Students using keyboard or axis-mapped throttle controls should understand that real throttle management is more nuanced.*

---

### 4.3 Rotor Engagement — Idle to Flight RPM

After the engine is stabilized at ground idle and all post-start checks are complete:

| Step | Action | Expected Indication | Critical Monitoring |
|---|---|---|---|
| 1 | **Collective** — verify full DOWN | Minimum pitch; minimum power demand | |
| 2 | **Throttle** — advance past idle stop to **FLY** detent | Press idle stop release on collective while twisting throttle clockwise | Requires pressing the idle stop release button |
| 3 | Monitor **Nr increasing** | Nr rises from ground idle (~59-62%) toward governed RPM (324 RPM / 100%) | Nr should increase smoothly; governor engages and stabilizes |
| 4 | Monitor **EGT** during power increase | EGT rises as engine produces more power | Must remain below continuous limit (610°C) |
| 5 | **Nr stabilized** at 324 ±3 RPM | Dual tach shows Nr and N2 needles "married" | Governor maintaining RPM |
| 6 | **Low RPM warning audio test** — verify audio warning is functional | Briefly reduce throttle to trigger low-RPM warning, then return to FLY | Audio tone should sound below ~294 RPM Nr; confirms warning system is active |
| 7 | **Wait for rotor to stabilize** (~30 seconds) | Rotor track smooths out; vibrations settle to normal level | Initial rotor engagement may produce some vibration as blades track |

**Rotor Engagement Safety Notes:**
- Keep collective **full down** during throttle advance to FLY — this minimizes rotor thrust and prevents the helicopter from becoming light on the skids.
- Ensure all personnel are clear of the rotor arc. The UH-1H's 48-ft rotor diameter means the blade tips extend 24 ft from the mast in all directions and dip significantly at low RPM.
- Rotor at low RPM (during spin-up) droops significantly and can strike the tail boom if the cyclic is displaced. Keep cyclic centered during rotor engagement.

> *⚠ Realism Divergence: In the real UH-1H, the throttle idle stop release is a physical button that requires deliberate finger pressure while simultaneously twisting the grip. This coordination takes practice in the real aircraft. DCS maps this to a click or keypress, which is simpler. The student should understand that the real procedure requires physical dexterity.*

---

### 4.4 Before-Takeoff Checks

After rotor engagement and stabilization, the pilot performs the before-takeoff check before hover or departure:

| Check Item | Action | Verify |
|---|---|---|
| **Engine instruments** | Scan all engine gauges | N1 governed, Nr 324 ±3, EGT < 610°C, torque at idle value, oil P&T in range |
| **Transmission instruments** | Check trans oil P&T | Within limits |
| **Hydraulics** | Check hydraulic pressure gauge | 1,000-1,500 PSI normal |
| **Flight controls** | Full cyclic deflection (left/right/fore/aft), collective full up/down, pedals full left/right | Smooth, light response with hydraulics; no binding or restriction |
| **Force trim** | Set force trim — verify it holds cyclic position; release — verify controls move freely | Magnetic brake engaging and releasing properly |
| **Governor** | Verify GOV switch ON | Governor maintaining Nr |
| **RPM Warning** | Verify audio warning ON | |
| **Caution panel** | Verify CLEAR (all lights extinguished) | No unresolved cautions |
| **Altimeter** | Set to current QNH / field elevation crosscheck | Reads within 75 ft of known field elevation |
| **Transponder** | ON or ALT (altitude reporting) — squawk code set | Appropriate code set per clearance |
| **Radios** | Tuned and volume set; transmit selector on correct radio | Comm check if possible |
| **Doors/Cargo** | Secured as briefed | |
| **Crew brief** | Intentions, abort criteria, emergency plan | Brief crew on planned departure, pattern, and emergency actions |

---

### 4.5 Hover Taxi

The UH-1H taxis by **hover taxi** — there are no wheels. The pilot lifts the helicopter to 3-5 ft skid height and translates forward at walking speed or slightly faster (typically under 20 knots ground speed).

#### Hover Taxi Technique

| Phase | Action | Key Points |
|---|---|---|
| **Pick-up to hover** | Smoothly raise collective while coordinating pedals (left pedal as collective increases) and cyclic (slight right cyclic to counter translating tendency) | Establish a stable 3-5 ft hover before beginning taxi |
| **Begin taxi** | Apply slight forward cyclic to begin forward movement | Nose dips slightly; maintain altitude with collective |
| **Maintain track** | Use cyclic to steer; use pedals to maintain heading aligned with taxi route | Look well ahead — not at the ground directly below |
| **Speed control** | Forward cyclic angle determines speed; aft cyclic to slow/stop | Keep speed at walking pace (~5-10 knots) in congested areas |
| **Stop** | Apply aft cyclic to arrest forward motion; maintain hover altitude with collective | Anticipate the pitch-up and left yaw as you decelerate |
| **Set down** | Slowly lower collective; maintain heading and position as skids approach ground | Feel for ground contact; gentle collective reduction |

#### Crosswind Hover Taxi

- In a crosswind, the helicopter will drift with the wind unless corrected.
- Apply cyclic into the wind to maintain track.
- Strong crosswinds (>15 knots) increase the risk of dynamic rollover during liftoff and set-down.
- If the wind is from the left, the tail rotor is working harder (wind opposing tail rotor thrust) — monitor pedal authority.
- If the wind is from the right, the tail rotor workload decreases — monitor for LTE if the wind shifts aft.

---

### 4.6 Hover Power Check

Before departing the hover area, the pilot should verify that sufficient power is available for the intended operation.

**IGE Hover Power Check:**
1. Establish a stable hover at 3-5 ft (IGE).
2. Read the torque gauge — this is the power required to hover IGE at current weight, altitude, and temperature.
3. Note the maximum continuous torque limit (~40 PSI).
4. The difference between current hover torque and the max continuous limit is the **power margin**.

**OGE Hover Power Check:**
1. If the mission requires OGE hover (>24 ft AGL), the pilot must verify OGE power is available.
2. OGE hover requires approximately 10-15% more torque than IGE.
3. If IGE hover torque is close to the maximum limit, OGE hover may not be possible at current conditions.
4. The pilot should calculate expected power requirements using available performance data (OAT, pressure altitude, gross weight) or verify empirically by slowly climbing above ground effect.

**Decision: GO or NO-GO:**
- If sufficient power margin exists → proceed with departure
- If power margin is marginal → consider a rolling/running takeoff (less power than hover), or reduce weight (offload fuel, passengers, cargo), or wait for cooler temperatures
- If power margin is insufficient → do not attempt departure; reduce weight or wait for better conditions

---

### Instructor Notes — Module 4

| Common Student Error | Correction |
|---|---|
| **Hot start — throttle advanced too early or too fast** | Emphasize: wait for 15% N1 before introducing fuel. Practice the timing: watch N1, count "fifteen percent, throttle to idle." |
| **Burning out the starter (real-world habit)** | Teach the 60-second/2-minute duty cycle even though DCS doesn't enforce it. Build good habits |
| **Forgetting fuel valve or boost pump** | Use the mnemonic: "Fuel first" — fuel valve and boost pump before any start attempt |
| **Skipping the governor exercise** | This exercise is the foundation of RPM management understanding. Do not skip it. The student who does not understand governor operation will struggle with emergencies later |
| **Advancing throttle to FLY with collective up** | Emphasize: collective FULL DOWN before advancing to FLY. A student who advances to flight RPM with collective up will produce unexpected thrust and may lift off uncontrolled |
| **Jerky hover taxi** | Start with zero wind, open area. Emphasize: look far ahead, tiny inputs, patience. The stabilizer bar helps, but only if the student gives it time to work |
| **Not performing a hover power check** | Make the power check a mandatory callout: "Torque [X] PSI, power margin is [Y] PSI, go/no-go for [operation]." |
| **Forgetting to set the altimeter** | Include in the before-takeoff flow; crosscheck with field elevation. An altimeter error sets up all subsequent altitude calls to be wrong |

---

## Module 5: Hover & Takeoff

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Pick up to a stable 3-5 ft hover from the ground and maintain position, heading, and altitude within ±3 ft, ±10°, and ±2 ft respectively.
2. Perform hover turns (pedal turns) through 360° while maintaining position and altitude.
3. Perform forward, sideward, and rearward hover taxi at controlled speeds.
4. Perform a hover power check and state the power margin available.
5. Execute a normal takeoff from a hover through ETL to climbing flight at Vy.
6. Execute a no-hover takeoff, running takeoff, and maximum performance takeoff.
7. Describe the control inputs required during transition through ETL.
8. State the climb speeds for best rate (Vy) and cruise climb, and demonstrate level-off technique.

---

### 5.1 Hover Technique

#### Picking Up to a Hover

This is one of the most demanding skills for a new helicopter pilot. The UH-1H must be brought smoothly from ground contact to a stable 3-5 ft hover without lateral drift, yaw, or altitude excursions.

**Procedure:**

| Phase | Action | Control Inputs | Common Errors |
|---|---|---|---|
| **Pre-liftoff** | Set cyclic centered, pedals slightly left of center (anticipate torque reaction), collective at bottom | All controls positioned; eyes outside on a reference point 50-100 ft ahead | Staring at the gauges instead of outside references |
| **Initial collective raise** | Smoothly and slowly raise collective | Feel the aircraft become light on the skids; apply left pedal progressively as torque increases; small cyclic corrections to maintain position | Raising collective too fast — helicopter jerks off the ground |
| **Light on skids** | Aircraft weight transfers from skids to rotor; the helicopter rocks gently | Continue smooth collective increase; maintain heading with pedals; maintain position with cyclic | Over-correcting lateral drift; chasing the aircraft with cyclic |
| **Skids clear ground** | At ~1-2 ft, the aircraft is fully airborne in ground effect | Continue raising collective to reach 3-5 ft; stabilize | Height control oscillations — going up/down/up/down |
| **Stable hover** | Maintain 3-5 ft, heading, and position | Constant small corrections on all three controls; scan pattern: reference point → horizon → instruments → reference point | Fixating on one axis; ignoring drift while correcting heading |

**Key Principles:**
- **Eyes outside.** The primary hover reference is a fixed point on the ground 50-100 ft ahead. Peripheral vision detects drift, altitude changes, and heading changes.
- **Small inputs.** The stabilizer bar helps dampen pilot inputs, but only if the inputs are small. Large corrections cause oscillations that the stabilizer bar amplifies through its gyroscopic lag.
- **Patience.** After each correction, wait for the aircraft to respond before making another. The UH-1H's stabilizer bar introduces a ~0.5-1 second lag between cyclic input and rotor disc response.
- **Pedals are continuous.** Unlike cyclic (set and wait), pedals require constant adjustment because torque changes with every collective input and every gust of wind.

#### Hover Scan Pattern

```
Reference Point (50-100 ft ahead)
         ↕
    Peripheral Vision (drift, altitude)
         ↕
   Brief Instrument Check (Nr, torque, EGT)
         ↕
    Back to Reference Point
```

The hover scan is approximately 80% outside and 20% instruments. The student should never stare at any single reference for more than 2-3 seconds.

---

### 5.2 Hover Power Check

The hover power check is a mandatory assessment performed before committing to departure.

**Procedure:**
1. Establish a stable hover at 3-5 ft (IGE).
2. Read the torque gauge. This is **power required to hover IGE**.
3. Note the **maximum continuous torque** limit (~40 PSI).
4. Calculate the **power margin**: Max continuous torque minus hover torque.

**Example:**
- Hover torque: 32 PSI
- Max continuous: 40 PSI
- Power margin: 8 PSI — sufficient for normal operations

**Power margin assessment:**

| Power Margin | Assessment | Action |
|---|---|---|
| **> 5 PSI** | Good power margin | Normal takeoff, OGE operations likely available |
| **3-5 PSI** | Marginal | Normal takeoff possible; OGE operations may not be available. Consider running takeoff |
| **< 3 PSI** | Insufficient for normal operations | Running takeoff required; reduce weight or wait for cooler temperatures. OGE hover not available |
| **At or above max continuous in hover** | Performance limited | Cannot sustain hover; running takeoff mandatory; consider mission abort if obstacles require climbing flight |

**OGE Power Check (if required):**
- From a stable hover, slowly climb vertically while monitoring torque.
- At approximately 24 ft AGL (one half rotor diameter), ground effect diminishes.
- If torque approaches max continuous before reaching OGE, the aircraft cannot hover OGE at current conditions.

---

### 5.3 Hover Turns (Pedal Turns)

Pedal turns are 360° turns performed in a stationary hover, used for area observation and directional changes before hover taxi.

**Technique:**

| Direction | Control Input | Coordination Required |
|---|---|---|
| **Left pedal turn** (nose left) | Apply left pedal smoothly | As the nose turns left, the tail moves right — apply slight right cyclic to maintain position over the spot. Collective may need slight adjustment as power demand changes with changing tail rotor loading |
| **Right pedal turn** (nose right) | Apply right pedal smoothly | As the nose turns right, the tail moves left — apply slight left cyclic. Right pedal turns require less tail rotor thrust (reducing anti-torque), so collective may need slight increase to maintain altitude |

**LTE Awareness During Pedal Turns:**
- During a right pedal turn in a hover, the tail rotor is producing less thrust (less anti-torque needed as the turn reduces yaw demand).
- If the wind is from the rear during the turn, the tail rotor may enter an LTE condition.
- **Critical:** Slow, deliberate pedal turns. If uncommanded yaw rate increases — immediately apply forward cyclic to gain airspeed and escape the LTE condition.
- Avoid hovering pedal turns in wind speeds above ~15 knots until proficient.

---

### 5.4 Hover Taxi (Forward, Sideward, Rearward)

#### Forward Hover Taxi

| Phase | Action | Speed | Notes |
|---|---|---|---|
| From stable hover | Apply slight forward cyclic | 0-5 knots | Nose dips slightly; maintain altitude with collective |
| Accelerate | Increase forward cyclic angle slightly | 5-15 knots | Speed controlled by cyclic angle; altitude by collective |
| Maintain track | Cyclic for direction; pedals for heading alignment | Walking pace in congested areas | Look ahead, not down |
| Decelerate | Aft cyclic to reduce speed; anticipate nose-up pitch and altitude gain | Returning to 0 knots | Maintain heading with pedals |

#### Sideward Hover Taxi

- Used for positioning and obstacle avoidance.
- Apply lateral cyclic in the desired direction.
- Speed limit: ~20 knots (structural limit for sideward flight near the ground).
- **Hazard:** Dynamic rollover risk if a skid catches during sideward movement near the ground.
- Crew coordination essential — the pilot cannot see in all directions. Crew chief/door gunner should clear the direction of movement.

#### Rearward Hover Taxi

- Used for repositioning when forward taxi is not possible.
- Apply aft cyclic gently.
- Speed limit: ~20 knots (structural).
- **Hazard:** Tail rotor strike risk — the tail rotor extends well behind the fuselage and below the main rotor plane. Obstacles behind the aircraft can contact the tail rotor during rearward taxi.
- Crew coordination is **mandatory** — the pilot has very limited rearward visibility.
- Use minimal speed and distance; reposition by pedal turn to face the desired direction when possible.

---

### 5.5 Normal Takeoff

The normal takeoff departs from a stable hover, accelerates through ETL, and transitions to climbing flight.

**Procedure:**

| Step | Action | Expected Aircraft Response | Control Inputs |
|---|---|---|---|
| 1 | Establish stable hover at 3-5 ft; complete hover power check | Aircraft stable, power margin confirmed | Steady inputs on all controls |
| 2 | Smoothly apply forward cyclic to begin acceleration | Nose dips, aircraft begins forward movement | Forward cyclic; maintain altitude with collective |
| 3 | **Passing through ETL (~16-24 knots)** | Aircraft "gets light," vibrations decrease, nose pitches up, left yaw tendency | Forward cyclic to counteract nose-up pitch; right pedal to counteract left yaw; slight collective reduction (more efficient lift = less power needed) |
| 4 | Continue acceleration to Vy (60 KIAS) | Aircraft climbing; translational lift fully developed | Adjust cyclic for desired pitch attitude; adjust collective for desired climb rate; trim |
| 5 | Positive rate of climb confirmed (VSI shows climb, altimeter increasing) | Climbing through departure altitude | Maintain Vy (60 KIAS) for best rate of climb |
| 6 | Clear of obstacles, established in climb | Stable climb at 60 KIAS | Set force trim; monitor engine instruments (EGT, torque, Nr) |

**ETL Transition — Detailed Control Sequence:**

The transition through ETL is the most dynamic phase of the takeoff and requires coordinated control inputs:

1. **Below ETL (0-16 knots):** High power, high tail rotor demand, helicopter in full hover mode. Cyclic, collective, and pedal inputs are all active.
2. **Entering ETL (16-18 knots):** Vibrations from transverse flow effect. The rotor begins to encounter clean air. Aircraft becomes more efficient.
3. **Through ETL (18-24 knots):** Rapid lift increase. The nose pitches up due to increased lift on the aft portion of the disc. Left yaw tendency increases (translating tendency changes). The pilot must:
   - Apply **forward cyclic** to prevent the nose from rising excessively
   - Apply **right pedal** to counteract left yaw
   - **Reduce collective slightly** — the rotor is producing more lift at the same power setting
4. **Above ETL (24+ knots):** Aircraft is in translational flight. Vibrations settle. Controls become more responsive due to increased airflow over all surfaces. The vertical stabilizer begins contributing to directional stability, reducing pedal workload.

---

### 5.6 No-Hover Takeoff

Used when power is insufficient for a sustained OGE hover but sufficient for IGE hover and acceleration.

**Technique:**
1. Position aircraft facing into the wind on a clear departure path.
2. Raise collective to begin a light hover (skids barely clear of ground — 1-2 ft).
3. Immediately apply forward cyclic to begin acceleration while remaining in ground effect.
4. As the aircraft accelerates through ETL, it will gain translational lift and begin to climb.
5. Once past ETL and climbing, transition to normal climb profile.

**Key principle:** Stay in ground effect (below ~24 ft AGL) during the acceleration phase. Ground effect reduces power required, allowing the aircraft to accelerate to translational lift speed even when OGE hover power is not available.

---

### 5.7 Running Takeoff

Used when hover capability is severely limited (high gross weight, high density altitude, heavy load).

**Technique:**
1. Aircraft on the ground, throttle at FLY, collective at minimum.
2. Smoothly increase collective to make the aircraft light on the skids.
3. Apply forward cyclic to begin forward movement **while the skids are still touching**.
4. The aircraft slides forward on the skids (or becomes very light and skids skim the surface).
5. As speed increases, the aircraft lifts off in ground effect and transitions through ETL.
6. Continue acceleration to Vy and establish a normal climb.

**Risks:**
- Skid damage if surface is rough or uneven.
- Dynamic rollover risk if a skid catches during the slide.
- Requires a long, clear departure area with no obstacles.

---

### 5.8 Maximum Performance Takeoff

Used when obstacles require a steep departure climb. This technique demands maximum power and is used when the departure area is confined.

**Technique:**
1. Establish a hover at 3-5 ft. Verify maximum power available.
2. Apply maximum allowable power (max torque for conditions).
3. At the same time, apply forward cyclic to accelerate — the aircraft climbs steeply while accelerating.
4. The aim is to clear the obstacle at the minimum safe speed, then continue acceleration to Vy.
5. As obstacles are cleared, transition to a normal climb.

**Risks:**
- Operating at maximum power limits — EGT and torque must be closely monitored.
- If engine failure occurs during this phase, autorotation options are limited due to low airspeed and low altitude.
- This is the highest-risk takeoff profile and should only be used when obstacles require it.

---

### 5.9 Climb Profiles

| Profile | Airspeed | Power | Usage |
|---|---|---|---|
| **Best Rate of Climb (Vy)** | ~60 KIAS | Max continuous or as required | Maximum altitude gain per unit time; used for departures and obstacle clearance |
| **Cruise Climb** | ~80 KIAS | Moderate climb power | Gaining altitude while making better forward progress; used enroute |
| **Enroute Climb** | 80-90 KIAS | Reduced climb power | Gradual altitude gain during cruise; fuel efficient |

#### Level-Off Technique

1. **Lead the level-off** by 10% of the climb rate (e.g., at 500 fpm climb, begin level-off 50 ft below target altitude).
2. Smoothly lower the nose (forward cyclic) to accelerate to cruise speed.
3. As airspeed increases, reduce collective (power) to maintain altitude.
4. Retrim for cruise (force trim release → set → release).
5. Final check: altitude, airspeed, heading, engine instruments within limits.

---

### 5.10 Departure Procedures

**Standard VFR Departure:**
1. After takeoff, climb straight ahead (or per departure instructions) at Vy (60 KIAS).
2. At pattern altitude or as directed, turn to departure heading.
3. Contact departure frequency (switch from tower to departure/area freq) when clear of the traffic pattern.
4. Continue climb to desired enroute altitude.
5. Transition to cruise speed (90-100 KIAS) and cruise power.

**Communication:**
> "*[Callsign], departing [runway], climbing to [altitude], request frequency change.*"
> Tower: "*[Callsign], frequency change approved, contact [Departure] on [frequency].*"
> "*Switching to [frequency], [Callsign].*"

---

### 5.11 Ground Resonance — Awareness

Ground resonance is a potentially catastrophic oscillation that occurs when the rotor system's lead-lag motion couples with the fuselage/landing gear dynamics. While ground resonance is primarily associated with **fully articulated rotor systems** (3+ blades with lead-lag hinges), the student must understand the concept:

**For the UH-1H teetering rotor:**
- The two-blade teetering rotor has **no lead-lag hinges**, which makes it significantly less susceptible to classical ground resonance than fully articulated systems.
- However, the UH-1H can experience **sympathetic vibrations** if the rotor system is imbalanced (blade damage, hub damage) while on the ground.
- If violent oscillation develops on the ground: **immediately lift off** if Nr is sufficient (full up collective), or **immediately shut down** if Nr is low (throttle to CLOSED, rotor brake if available). Do not remain on the ground with the oscillation present.

> *⚠ Realism Divergence: DCS does not model ground resonance for the UH-1H. This is an academic awareness item. The student should understand the concept and the immediate action, even though they will not encounter it in the simulation.*

---

### Instructor Notes — Module 5

| Common Student Error | Correction |
|---|---|
| **Over-controlling during hover pickup** | "Squeeze the collective — don't yank it." Emphasize slow, smooth collective application. One inch of collective per second as a starting guideline |
| **Failing to coordinate pedals with collective** | Before every hover exercise, remind: "Collective up = left pedal. Collective down = right pedal." Make it a verbal callout until it becomes instinctive |
| **Staring at the ground under the aircraft** | "Eyes out — look at a reference point 50-100 ft ahead." Physically point at the reference. Peripheral vision handles hover height |
| **Nose-up pitch surprise at ETL** | Brief the ETL sequence before every takeoff: "At 16-24 knots, the nose will pitch up. Be ready with forward cyclic." |
| **Not reducing collective through ETL** | Explain: "The rotor just got 10-15% more efficient — you need less power. If you don't reduce collective, you'll balloon up." |
| **Oscillating in hover (pilot-induced oscillation)** | "Hands off — let the helicopter stabilize." Demonstrate: make a deliberate disturbance, then take hands off cyclic. The stabilizer bar helps the aircraft settle. Then show the student that chasing the oscillation makes it worse |
| **LTE during pedal turns** | Start with left pedal turns only (safer — higher tail rotor thrust). Right pedal turns only after left pedal turns are proficient. Always brief LTE recovery before hover work |
| **Not performing hover power check** | Make it a crew callout requirement: "Hover torque [X], max continuous [Y], margin [Z], go/no-go." No departure without this call |

---

## Module 6: Basic Flight Maneuvers

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Maintain straight and level flight at cruise speed (90-100 KIAS) within ±100 ft altitude, ±10 KIAS, and ±10° heading.
2. Execute coordinated level turns at 15°, 30°, and 45° bank angles while maintaining altitude within ±100 ft.
3. Perform climbs and descents at specified rates while maintaining airspeed within ±10 KIAS.
4. Demonstrate slow flight characteristics below ETL and describe the increased power requirements.
5. Perform speed changes (acceleration and deceleration) while maintaining altitude.
6. Execute practice autorotation entries and power recoveries at altitude.
7. Demonstrate correct force trim usage during all maneuvers.
8. Fly straight and level at 40, 60, 80, and 100 KIAS and describe the handling differences at each speed.

---

### 6.1 Level Flight — Cruise

**Cruise Speed:** 90-100 KIAS (most efficient for range; comfortable control feel).

**Establishing Cruise:**
1. Level off from climb at target altitude.
2. Allow airspeed to build to 90-100 KIAS.
3. Reduce power (collective) to cruise setting (~25-32 PSI torque, varying with weight and altitude).
4. Set force trim (press and release force trim button on cyclic).
5. Fine-tune: adjust cyclic for pitch attitude that holds 90-100 KIAS, adjust collective for altitude, adjust pedals to center the ball.
6. Re-trim after each adjustment.

**Cruise Power Settings (Approximate — Sea Level, ~7,500 lbs GW):**

| Airspeed | Torque (Approx) | EGT (Approx) | Fuel Flow (Approx) | Notes |
|---|---|---|---|---|
| 60 KIAS | ~28-32 PSI | ~520-560°C | ~260-280 lbs/hr | Slower; higher nose attitude; approaching best endurance |
| 80 KIAS | ~26-30 PSI | ~500-540°C | ~240-260 lbs/hr | Economical cruise |
| 100 KIAS | ~28-32 PSI | ~520-560°C | ~250-270 lbs/hr | Best range speed; moderate nose-down attitude |
| 120 KIAS | ~34-38 PSI | ~560-590°C | ~280-310 lbs/hr | High speed cruise; approaching Vne at altitude; increased vibration |

> *⚠ Realism Divergence: Real-world power settings vary significantly with density altitude, gross weight, and aircraft condition. The values above are approximate for DCS at sea level with a mid-weight aircraft. DCS power requirements may differ slightly from real-world charts. The student should develop their own feel for power settings at various airspeeds and conditions.*

---

### 6.2 Turns

Turns in the UH-1H require coordination of all three controls:

**Entering a Turn:**
1. Look in the direction of the turn (clear the area).
2. Apply lateral cyclic in the direction of the turn.
3. Apply slight aft cyclic to maintain pitch attitude (prevent nose drop in a turn).
4. Increase collective slightly to compensate for the increased load factor (more lift needed to maintain altitude in a banked turn).
5. Apply pedal to maintain coordinated flight (ball centered in the turn indicator).

**In the Turn:**
- Maintain bank angle with cyclic.
- Maintain altitude with collective.
- Maintain coordinated flight with pedals (ball centered).
- Monitor airspeed — tends to decay in turns due to increased drag.

**Rolling Out:**
1. Anticipate the rollout by ~10° before the desired heading (lead the heading).
2. Apply opposite lateral cyclic to level the wings.
3. Reduce collective slightly (back to level flight power).
4. Center pedals as bank angle decreases.
5. Re-trim.

#### Turn Parameters

| Bank Angle | G-Load | Altitude Loss Tendency | Collective Adjustment | Recommended Usage |
|---|---|---|---|---|
| **15°** | ~1.04 G | Minimal | Negligible | Gentle heading corrections; enroute turns |
| **30°** | ~1.15 G | Moderate | Slight increase needed | Standard turns; pattern turns |
| **45°** | ~1.41 G | Significant | Noticeable increase needed | Steep turns; maximum for normal operations |
| **60°** | ~2.00 G | Extreme | Major increase — approaching torque limits | Structural limit; emergency only; NOT standard BQT maneuver |

**Key Caution — Load Factor and Retreating Blade Stall:**
At higher bank angles, the effective load factor increases, which reduces the airspeed at which retreating blade stall occurs. A 45° banked turn at 100 KIAS produces the same blade loading as straight-and-level flight at approximately 119 KIAS. The student must reduce airspeed before entering steep turns.

---

### 6.3 Climbs and Descents

#### Climbs

| Technique | Airspeed | Power | Usage |
|---|---|---|---|
| **Best Rate (Vy)** | 60 KIAS | Max continuous (~40 PSI) or less | Maximum altitude gain per time; obstacle clearance, departure |
| **Cruise Climb** | 80 KIAS | Moderate climb power (~34-38 PSI) | Gaining altitude while enroute; better visibility over nose |
| **Max Angle Climb** | 50-55 KIAS | Max continuous | Maximum altitude gain per distance; clearing close obstacles |

**Climb Technique:**
1. Increase collective to desired climb power.
2. Apply aft cyclic to reduce airspeed to climb speed.
3. Coordinate pedals (left pedal as collective increases).
4. Trim for climb attitude.
5. Monitor Nr (governor should hold; verify), EGT (must stay within limits at higher power), and torque.

#### Descents

| Technique | Airspeed | Power | Rate of Descent | Usage |
|---|---|---|---|---|
| **Cruise Descent** | 90-100 KIAS | Reduced power (~20-25 PSI) | 500-1,000 fpm | Normal enroute descent |
| **Approach Descent** | 60-80 KIAS | Progressively reducing | 300-500 fpm | Approach to landing pattern |
| **Autorotation Descent** | 65 KIAS | Idle (flat pitch / no power) | ~1,500-2,000 fpm | Engine failure; practice autorotation |

**Descent Considerations:**
- **Nr tends to increase** during descents (reduced collective = reduced load on rotor = RPM rises). The governor compensates by reducing fuel flow, but monitor Nr on the dual tach.
- **Avoid rapid collective reductions** — can cause Nr overshoot beyond governor correction range, resulting in transient overspeed.
- **Settling with power risk** — if descending at low airspeed with moderate power applied, watch for VRS conditions (see Module 1, Section 1.8).

---

### 6.4 Slow Flight

Slow flight below ETL (~16-24 knots) transitions the helicopter from efficient translational flight back into the hover regime. Characteristics:

| Parameter | Above ETL | Below ETL (Slow Flight) |
|---|---|---|
| **Power required** | Moderate (translational lift assisting) | High (no translational lift; rotor working harder) |
| **Vibration** | Low, smooth | Increasing; transverse flow effect vibrations return |
| **Control response** | Crisp; airflow over all surfaces | Sluggish; less airflow over vertical fin, less tail rotor effectiveness from relative wind |
| **Pedal workload** | Low (vertical fin helps stabilize yaw) | High (tail rotor must provide all anti-torque; pedal authority may be reduced) |
| **Directional stability** | Good (vertical fin effective) | Poor (vertical fin ineffective; LTE risk increases) |

**Slow Flight Exercise:**
1. From cruise, progressively decelerate (aft cyclic, increase collective to maintain altitude).
2. Note the increasing vibration as the aircraft passes back through ETL.
3. Note the increasing power (collective) required to maintain altitude.
4. Note the increasing pedal inputs required to maintain heading.
5. Establish a slow-flight speed of ~30-40 KIAS and maintain altitude and heading.
6. Accelerate back to cruise (forward cyclic, reduce collective as ETL efficiency returns).

**Training value:** The student learns the power curve — that below a certain speed (sometimes called the "backside of the power curve"), more power is required for slower speed. This is counterintuitive for fixed-wing pilots and is a fundamental concept in helicopter aerodynamics.

---

### 6.5 Speed Changes

#### Acceleration (Slower to Faster)

1. Apply forward cyclic (nose drops, speed builds).
2. The rotor becomes more efficient as translational lift increases — collective may need to be **reduced** to maintain altitude.
3. Trim for new airspeed.

#### Deceleration (Faster to Slower)

1. Apply aft cyclic (nose rises, speed decreases).
2. As airspeed decreases, the rotor becomes less efficient — collective must be **increased** to maintain altitude.
3. As the aircraft decelerates below ETL, power required increases significantly.
4. Coordinate pedals with collective changes.
5. Trim for new airspeed.

**Key Relationship:** During speed changes at constant altitude:
- **Accelerating:** Forward cyclic + reduce collective (more efficient rotor) + right pedal (less torque)
- **Decelerating:** Aft cyclic + increase collective (less efficient rotor) + left pedal (more torque)

---

### 6.6 Straight and Level at Various Airspeeds

The student should fly straight and level at 40, 60, 80, and 100 KIAS to experience the handling differences:

| Airspeed | Nose Attitude | Power Required | Vibration Level | Control Feel | Notes |
|---|---|---|---|---|---|
| **40 KIAS** | Nose high (~5-8° pitch up) | High (~32-36 PSI) | Moderate (near ETL) | Sluggish; high pedal workload | On the backside of the power curve; power increases with slower speed |
| **60 KIAS** | Slightly nose up (~2-4°) | Moderate (~28-32 PSI) | Low | Good; balanced controls | Vy — best rate of climb speed; good reference for approach |
| **80 KIAS** | Near level (~0-2°) | Moderate-low (~26-30 PSI) | Low | Responsive; comfortable | Economical cruise; good general-purpose speed |
| **100 KIAS** | Slight nose down (~0 to -2°) | Moderate (~28-32 PSI) | Low, 2-per-rev noticeable | Responsive; cyclic more sensitive | Best range speed; approaching higher-vibration regime |
| **120 KIAS** | Nose down (~-2 to -4°) | Higher (~34-38 PSI) | Increasing; 2-per-rev more pronounced | Very responsive; approaching Vne sensitivity | Near Vne at altitude; blade stall awareness |

**2-Per-Rev Vibration:** The UH-1H's two-blade rotor produces a characteristic vibration at twice the rotor RPM frequency (2 × 324 RPM = 648 cycles/min ≈ 10.8 Hz). This vibration is always present but becomes more noticeable at higher airspeeds as the retreating blade operates at higher angles of attack. It is a normal characteristic, not an indication of malfunction.

---

### 6.7 Autorotation Entry (Practice — Power Recovery)

Practice autorotation entries are performed at altitude with a **power recovery** at the bottom — the student does not fly a full autorotation to the ground at this stage (that is covered in Module 8: Emergency Procedures).

**Purpose:** Build the reflexive response to engine failure: collective down, maintain Nr, establish autorotation airspeed.

#### Entry Procedure

| Step | Action | Expected Response | Critical Monitoring |
|---|---|---|---|
| 1 | Instructor simulates engine failure (throttle chop or call "engine failure") | Audio RPM warning, Nr begins to decay, left yaw (torque removed) | Nr — react before Nr drops below 294 RPM |
| 2 | **Lower collective immediately** — full down or to bottom | Nr stabilizes or increases (rotor disc now in autorotation — air flowing up through disc drives the rotor) | Nr must stay above 294 RPM; if below, the rotor does not have enough energy to arrest descent |
| 3 | **Maintain Nr** in autorotation range (294-324 RPM) | Nr governed by collective position and airspeed | If Nr too high → raise collective slightly; if Nr too low → lower collective further or adjust airspeed |
| 4 | **Establish autorotation airspeed: ~65 KIAS** | Aircraft descending at ~1,500-2,000 fpm; forward cyclic to establish 65 KIAS | 65 KIAS = best glide for autorotation (max range for distance to landing area) |
| 5 | **Right pedal** to maintain heading (no torque = no need for left pedal; the aircraft will yaw right without torque, requiring right pedal correction) | Heading stabilized; ball centered | Coordinated flight in autorotation |
| 6 | **Trim for 65 KIAS descent** | Stable autorotation glide established | Monitor Nr, airspeed, rate of descent |
| 7 | **Power recovery** (practice only) — smoothly increase collective and throttle to regain powered flight | Nr may fluctuate as power is reapplied; left pedal needed as torque returns | Smooth, coordinated recovery; avoid over-torquing |

#### Autorotation Key Speeds

| Speed | Value | Purpose |
|---|---|---|
| **Best glide (max range)** | ~65 KIAS | Covers the maximum distance from a given altitude — use when you need to reach a specific landing area |
| **Min rate of descent** | ~55 KIAS | Minimizes descent rate — use when you have a landing area directly below and need maximum time |
| **Never exceed in autorotation** | ~100 KIAS | Structural and Nr overspeed risk at high speed |

#### Two-Blade Rotor Autorotation Characteristics

The UH-1H's two-blade teetering rotor stores **less kinetic energy** than multi-blade systems of similar diameter. This has critical implications:

- **Reaction time is shorter.** Nr decays faster after power loss because the two-blade rotor has less moment of inertia. The pilot must lower collective **within 1-2 seconds** of engine failure to maintain Nr above 294 RPM.
- **Flare energy is less.** During the final flare in a full autorotation, the two-blade rotor has less stored energy to arrest the rate of descent and cushion the landing. Timing of the flare and collective pull must be more precise.
- **Practice makes the difference.** The autorotation entry must become a reflex — hear the RPM warning, collective goes down. No hesitation.

> *⚠ Realism Divergence: DCS models autorotation realistically for the UH-1H, including Nr decay rate, autorotation airspeeds, and collective/airspeed interaction. The rotor energy and flare/cushion behavior is well-represented. One notable DCS behavior: the autorotation RPM stability can be slightly more forgiving than the real aircraft — real-world Nr can decay below recoverable range faster than some students expect in DCS. Always practice as if the margin is razor-thin.*

---

### 6.8 Force Trim Technique — In-Flight Practice

The UH-1H force trim (magnetic brake) is used **constantly** in flight. Unlike an electric trim system that moves a tab, the magnetic brake simply locks the controls in position. The pilot must actively manage trim throughout all maneuvers.

**Trim Workflow:**
1. **Establish desired flight condition** (airspeed, altitude, heading, power).
2. **Hold the controls** in the position that maintains this condition.
3. **Press force trim release button** on the cyclic (thumb button).
4. **Release the button** — the magnetic brakes lock the controls in the current position.
5. The controls are now "trimmed" — they hold the current flight condition without pilot force.

**When to Re-Trim:**
- Every airspeed change
- Every power (collective) change
- Every altitude change
- Every turn entry and rollout
- Any configuration change (doors, cargo, etc.)
- Anytime you feel stick forces fighting you

**Out-of-Trim Indications:**
- The pilot feels a force on the cyclic (pushing forward, pulling back, pushing left/right) that must be countered with constant pressure.
- If the pilot releases the cyclic, the controls snap back to the trimmed position, which is no longer the correct position for the current flight condition.
- Out-of-trim forces increase pilot fatigue and reduce control precision.

**Common Trim Errors:**
- Forgetting to trim after a speed change → constant stick force, fatigue
- Trimming at the wrong airspeed → as airspeed changes, forces build again
- Not releasing force trim during maneuvers → fighting the brakes during control movements

---

### Instructor Notes — Module 6

| Common Student Error | Correction |
|---|---|
| **Not trimming after every speed/power change** | "If you're pushing or pulling, you need to trim." Call out "trim!" during flight whenever you see the student fighting the controls |
| **Altitude loss in turns** | "More bank = more collective. Add collective as you add bank." Have the student call out torque values in turns |
| **Uncoordinated turns (ball off center)** | "Step on the ball." Remind the student to glance at the turn-and-slip indicator during every turn. An off-center ball means inefficient flight and excess drag |
| **Delayed autorotation entry** | Practice the reflex: instructor calls "engine failure," student must have collective down within 2 seconds. Use a timer. The student who hesitates will lose Nr below recoverable range |
| **Forgetting right pedal in autorotation** | "No torque = no left pedal. Right pedal to hold heading." Drill this as part of the autorotation entry sequence |
| **Chasing Nr in autorotation** | Teach "set it and leave it" — establish 65 KIAS, set collective for Nr in the 294-324 range, and resist the urge to constantly adjust. Small collective adjustments for Nr trends, not Nr twitches |
| **Over-speeding in descent** | Remind: "Collective down = speed builds if you don't raise the nose." Maintain autorotation airspeed with cyclic, not collective |
| **Fear of autorotation practice** | Start at high altitude (3,000+ ft AGL) with plenty of recovery margin. Demonstrate first. Build confidence with repeated entries before adding complexity |

---

## Module 7: Navigation

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Tune and use the AN/ARN-83 ADF to home to an NDB station and identify station passage.
2. Tune and use the AN/ARN-82 VOR receiver to track inbound and outbound on a VOR radial using the CDI.
3. Describe basic ILS approach concepts (localizer and glideslope) and demonstrate CDI interpretation for an ILS approach.
4. Set and read the magnetic compass and directional gyro, and realign the DG to the compass periodically.
5. Perform basic dead reckoning navigation using time-speed-distance calculations and pilotage (visual map reference).
6. Set the radar altimeter low-altitude warning bug and use the radar altimeter for terrain clearance reference.
7. Set the transponder to a specified squawk code and mode.

---

### 7.1 Navigation in the UH-1H — Overview

The UH-1H has **no GPS, no FMS, no moving map display, and no digital navigation system**. All navigation is performed using:

1. **Radio navigation aids** — ADF (NDB) and VOR/ILS
2. **Compass and gyro** — magnetic compass and directional gyro
3. **Pilotage** — visual identification of terrain features and landmarks
4. **Dead reckoning** — time, speed, and distance calculations

This is fundamentally different from navigation in modern glass-cockpit aircraft and demands skills that many DCS students have never developed. The student must learn to **plan the navigation before flight** (plot courses, calculate headings, identify checkpoints) because there is no in-flight database to query.

| Navigation Method | Equipment | Accuracy | Range | DCS Availability |
|---|---|---|---|---|
| **ADF/NDB** | AN/ARN-83 | ±5-10° bearing | 50-200 NM (depends on NDB power) | Modeled — NDBs on DCS maps |
| **VOR** | AN/ARN-82 | ±1-2° radial | Line of sight (~100-200 NM depending on altitude) | Modeled — VORs on DCS maps |
| **ILS** | AN/ARN-82 | Precision approach capable | ~18 NM (localizer), ~10 NM (glideslope) | Modeled — ILS at equipped airfields |
| **Compass/DG** | Magnetic compass + gyro | ±2-5° heading | Unlimited (self-contained) | Modeled |
| **Pilotage** | Pilot's eyes + map | Depends on terrain and visibility | Visual range | DCS terrain matches map |
| **Dead Reckoning** | Clock + airspeed + heading | Degrades over distance | Unlimited (with increasing error) | Fully applicable |
| **Radar Altimeter** | Radar altimeter | ±5 ft AGL | 0-5,000 ft AGL | Modeled |

---

### 7.2 ADF (Automatic Direction Finder) — AN/ARN-83

The ADF is a radio receiver that tunes to NDB (Non-Directional Beacon) stations and displays a **bearing pointer** showing the direction to the station relative to the aircraft's heading.

#### ADF Controls and Indications

| Control / Indicator | Location | Function |
|---|---|---|
| **ADF Control Head** | Center pedestal or lower instrument panel | Frequency tuning knobs, mode switch (OFF/ADF/ANT/LOOP), volume |
| **Frequency Selector** | ADF control head | Tunes to NDB frequency (190-1,799.5 kHz) |
| **Mode Switch** | ADF control head | OFF: radio off / ADF: bearing pointer active / ANT: audio only (no bearing) / LOOP: manual direction finding |
| **ADF Bearing Pointer** | Compass card (instrument panel) | Thin needle that points toward the NDB station, superimposed on the compass card |

#### Using the ADF

**Homing to an NDB:**
1. Tune the ADF frequency selector to the NDB frequency.
2. Set mode to ADF.
3. Identify the station — listen for the Morse code identifier (NAV audio on the audio panel).
4. Read the bearing pointer on the compass card — the pointer indicates the direction **to** the station.
5. **Homing technique:** Turn the aircraft until the ADF bearing pointer is at the 12 o'clock position (pointing straight ahead). Fly toward the station.
6. Wind will cause the aircraft to drift; the bearing pointer will shift. The pilot must continuously correct heading to keep the pointer near 12 o'clock. This is "homing" — simple but not efficient in a crosswind (produces a curved track).

**Tracking to an NDB (Wind Correction):**
1. Home toward the station initially.
2. Note the wind correction angle (WCA) required to maintain a straight track — observe how far the bearing pointer drifts off the nose.
3. Apply a heading correction into the wind. The goal: the bearing pointer should read a constant relative bearing that corresponds to the desired track.
4. Adjust WCA as needed. This produces a straight-line track to the station, more efficient than homing.

**Station Passage:**
- As the aircraft approaches the NDB, the bearing pointer becomes increasingly sensitive (small position changes cause large bearing swings).
- Station passage is confirmed when the bearing pointer swings from ahead (12 o'clock) to behind (6 o'clock) — a rapid, positive swing.
- After station passage, the pilot navigates outbound from the station on the desired heading.

> *⚠ Realism Divergence: DCS models NDB stations and the ADF bearing pointer accurately. However, real-world ADF is subject to errors: thunderstorm attraction (the needle points toward lightning instead of the station), coastal refraction, night effect (sky wave interference), and terrain shielding. DCS does not model these error sources — the ADF bearing in DCS is accurate and reliable in all conditions. The student should understand that real-world ADF navigation requires awareness of these error sources.*

---

### 7.3 VOR/ILS — AN/ARN-82

The VOR (VHF Omnidirectional Range) receiver and ILS (Instrument Landing System) receiver are integrated in the AN/ARN-82 unit. VOR provides radial (bearing) information from a VOR station; ILS provides precision approach guidance (localizer and glideslope).

#### VOR Controls and Indications

| Control / Indicator | Location | Function |
|---|---|---|
| **VOR Control Head** | Center pedestal or lower instrument panel | Frequency tuning knobs, volume, mode |
| **Frequency Selector** | VOR control head | Tunes to VOR/ILS frequency (108.0-117.95 MHz) |
| **Course Deviation Indicator (CDI)** | Instrument panel (pilot's side) | Vertical needle: centered = on course; left = course is to the left; right = course is to the right |
| **OBS (Omni-Bearing Selector)** | Knob on CDI | Rotates to select the desired radial/course |
| **TO/FROM Flag** | CDI display | TO = flying toward the station on the selected course; FROM = flying away from the station |
| **Glideslope Needle** | CDI display (horizontal needle) | For ILS approaches only — above center = above glideslope; below = below glideslope |
| **OFF/Warning Flag** | CDI display | Indicates signal not received or unreliable |

#### Using VOR — Tracking a Radial

**Determine Position (Where am I?):**
1. Tune VOR frequency and identify the station (Morse code ident).
2. Rotate the OBS knob until the CDI centers with a FROM flag.
3. Read the radial indicated by the OBS — this is the radial you are on (the magnetic bearing **from** the station).
4. Cross-reference with a second VOR for a position fix (intersection of two radials).

**Tracking Inbound to a VOR:**
1. Tune and identify the VOR station.
2. Set the OBS to the desired inbound course. A TO flag should appear.
3. Fly a heading that maintains the CDI centered.
4. If the CDI moves left, the course is to your left — correct left.
5. If the CDI moves right, the course is to your right — correct right.
6. Adjust heading by 5-10° increments and observe CDI response.
7. Apply wind correction angle to maintain a centered CDI.

**Tracking Outbound from a VOR:**
1. After station passage (CDI flag switches from TO to FROM).
2. Set OBS to desired outbound radial.
3. Fly to center the CDI with FROM flag displayed.
4. Maintain CDI centered with heading corrections.

#### CDI Sensitivity

| Phase | CDI Full Deflection Equals |
|---|---|
| **VOR enroute** | ~10° off the selected radial (~200 ft per dot at close range, ~1 NM per dot at 60 NM) |
| **ILS localizer** | ~2.5° off the localizer course (~750 ft at the outer marker) |
| **ILS glideslope** | ~0.7° off the glideslope |

**Key point:** The CDI is more sensitive closer to the station. At long range, the CDI may appear centered even when the aircraft is offset by a significant distance. At short range, small deviations cause large CDI deflections.

---

### 7.4 ILS Approach — Basic Concepts

The ILS provides precision approach guidance using two radio beams:

| Component | Guidance | CDI Indication |
|---|---|---|
| **Localizer** | Lateral (left/right of centerline) | Vertical needle on CDI — same as VOR but more sensitive |
| **Glideslope** | Vertical (above/below desired descent path) | Horizontal needle on CDI — above center = fly down, below center = fly up |

**Basic ILS Approach Technique (Overview):**
1. Tune ILS frequency (108.10-111.95 MHz, odd tenths).
2. Set inbound course on OBS (some ILS/CDI combinations auto-set; others require manual OBS setting matching published ILS course).
3. Intercept the localizer — fly toward the inbound course and center the CDI.
4. Intercept the glideslope — as the glideslope needle descends from above center to center, begin descent to maintain it centered.
5. Fly the approach: maintain CDI centered (localizer) and glideslope needle centered, adjusting heading and rate of descent.
6. At decision altitude (DA), the pilot must have the runway in sight to continue; otherwise, execute a missed approach.

**BQT Scope:** ILS approaches require instrument flight skills that are beyond BQT scope. The student is introduced to ILS concepts and can practice tracking the localizer and glideslope in VMC to build foundational skills. Full ILS proficiency is an instrument qualification requirement.

#### Marker Beacons

| Marker | Distance from Threshold (Typical) | Light | Audio |
|---|---|---|---|
| **Outer Marker (OM)** | ~4-7 NM | Blue | Low-pitched tone (dashes) |
| **Middle Marker (MM)** | ~0.5-1 NM | Amber | Medium-pitched tone (alternating dots/dashes) |
| **Inner Marker (IM)** | ~0.1 NM (at threshold) | White | High-pitched tone (dots) |

---

### 7.5 Compass and Directional Gyro

#### Magnetic Compass

The magnetic compass is mounted above the instrument panel (visible to the pilot) and provides the **primary magnetic heading reference**. However, it has significant limitations:

| Error | Cause | Compensation |
|---|---|---|
| **Deviation** | Aircraft magnetic fields interfere | Deviation card posted on compass; different error at each heading |
| **Variation** | Magnetic north ≠ true north | Apply local variation to convert between true and magnetic |
| **Dip errors (acceleration/deceleration)** | The compass needle dips due to the Earth's magnetic field; acceleration/deceleration in a turn causes erroneous heading indications | Avoid reading the compass during turns; read only in straight, level, unaccelerated flight |
| **Northerly turning error** | Compass lags during turns through north, leads during turns through south | OSUN: Overshoot South, Undershoot North — roll out early on northerly headings, late on southerly |
| **Oscillation** | Turbulence, vibration | Let the compass settle before reading |

**Key rule:** The magnetic compass is accurate only in straight, level, unaccelerated flight. For all other conditions, use the directional gyro.

#### Directional Gyro (Heading Indicator)

The DG is a gyroscopic instrument that provides a **stable heading reference** without the dip and turning errors of the magnetic compass. However, it has its own limitation:

- **Precession:** The gyro drifts over time (~3° per 15 minutes, varying by hemisphere and aircraft vibration).
- **Solution:** The pilot must periodically (every 10-15 minutes) compare the DG to the magnetic compass (in straight, level flight) and reset the DG to match.

**DG Alignment Procedure:**
1. In straight and level, unaccelerated flight.
2. Read the magnetic compass (wait for it to settle).
3. Adjust the DG heading knob to match the compass reading.
4. Set the DG.
5. Repeat every 10-15 minutes.

---

### 7.6 Dead Reckoning and Pilotage

#### Dead Reckoning (DR)

DR navigation uses **heading, airspeed, and time** to calculate position. The basic formula:

**Distance = Speed × Time**

Example: Flying at 90 KIAS for 20 minutes = 90 × (20/60) = 30 NM.

**DR Procedure:**
1. Before flight: plot the course on a map. Measure the true course and distance.
2. Apply magnetic variation to get magnetic course.
3. Apply wind correction angle (WCA) to get magnetic heading to fly.
4. Calculate time enroute: distance ÷ groundspeed.
5. At departure, note the time. Fly the calculated heading.
6. At the calculated time, you should be at or near the destination.

**DR Accuracy:** Degrades with distance. Heading errors, wind estimation errors, and airspeed indicator inaccuracies all compound. DR is reliable for short legs (20-40 NM) but becomes increasingly approximate over longer distances. Supplement with pilotage and radio nav fixes.

#### Pilotage

Pilotage is visual navigation by identifying ground features and comparing them to a map:

| Feature Type | Reliability | Notes |
|---|---|---|
| **Rivers, lakes, coastlines** | Excellent | Large, distinctive, easy to see from altitude |
| **Roads, highways** | Good | Major roads are distinctive; minor roads can be confusing |
| **Mountains, ridgelines** | Good | Distinctive terrain features visible at distance |
| **Towns, cities** | Good | Size and layout help identification |
| **Railroads, power lines** | Moderate | Can be hard to see at altitude; good at low altitude |
| **Individual buildings** | Poor | Difficult to distinguish from altitude unless distinctive |

**DCS-Specific Pilotage Notes:**
- DCS terrain maps (Caucasus, Nevada, Syria, etc.) are reasonably accurate for major features.
- The F10 map can be used as a "chart" for planning, but the student should practice navigating without the F10 map open to build real navigation skills.
- DCS terrain rendering quality affects visual landmark identification — higher graphics settings help.

---

### 7.7 Radar Altimeter

| Parameter | Detail |
|---|---|
| **Function** | Measures absolute altitude above ground level (AGL) using radar pulse |
| **Range** | 0 to ~5,000 ft AGL |
| **Low-Altitude Warning Bug** | Pilot-adjustable; triggers audio and visual warning when descending below set altitude |
| **Accuracy** | ±5 ft (within effective range) |
| **Location** | Instrument panel |

**Usage:**
- Set the low-altitude warning bug to minimum safe altitude for the current operation (e.g., 200 ft AGL for general flying, 50 ft for low-level operations, decision height for approaches).
- The radar altimeter reads **terrain directly below the aircraft** — it does not predict terrain ahead. On sloping terrain, the reading changes rapidly.
- For approaches: provides positive altitude reference in AGL — useful for establishing hover altitude at unfamiliar landing zones.

---

### 7.8 Transponder

| Parameter | Detail |
|---|---|
| **Designation** | AN/APX-72 (or similar) |
| **Modes** | OFF / STANDBY / ON (Mode A) / ALT (Mode A + C altitude reporting) |
| **Code Entry** | Four octal digit wheels (0000-7777) |
| **IDENT** | Press to highlight aircraft on ATC radar display |
| **Standard Codes** | 1200 (VFR), 7700 (Emergency), 7600 (Radio failure), 7500 (Hijack) |

**Transponder Procedures:**
- Set to STANDBY during startup (warms up but does not transmit).
- Set to ON or ALT before taxi (as instructed by ATC or per local procedures).
- Set squawk code per ATC clearance or use 1200 for VFR flight without ATC services.
- Press IDENT when requested by ATC ("Squawk ident").
- Set 7700 in an emergency.

> *⚠ Realism Divergence: DCS ATC uses transponder codes in a simplified manner. Mode C (altitude reporting) is modeled but the DCS ATC system does not always interrogate or verify altitude. The student should learn proper transponder operation and standard codes as they will be critical in multiplayer environments with human ATC.*

---

### 7.9 Navigation Planning (Pre-Flight)

Because the UH-1H has no in-flight navigation database, the pilot must plan navigation **before starting the engine**:

**Pre-Flight Navigation Checklist:**

| Item | Action | Notes |
|---|---|---|
| **Route** | Plot on map/chart | Identify waypoints, checkpoints, and course legs |
| **Courses** | Measure true course for each leg; convert to magnetic heading | Apply magnetic variation |
| **Distances** | Measure distance for each leg in NM | Use map scale |
| **Time** | Calculate time for each leg based on planned airspeed and distance | Note cumulative time for fuel planning |
| **Frequencies** | List all nav aid frequencies (NDB, VOR, ILS) along the route | Write on kneecard |
| **Comm frequencies** | List ATC frequencies (ground, tower, approach, center, CTAF) | Write on kneecard |
| **Checkpoints** | Identify visual landmarks at ~10 NM intervals along each leg | Rivers, roads, towns, terrain features |
| **Alternates** | Identify alternate landing areas and their frequencies | In case of weather, emergency, or diversion |
| **Fuel** | Calculate fuel required for route + reserve | Verify fuel quantity is sufficient before departure |

**Kneecard:** The pilot creates a kneecard (small card strapped to the thigh) with all navigation data organized by leg. This is the primary in-flight reference for an analog-cockpit aircraft.

---

### Instructor Notes — Module 7

| Common Student Error | Correction |
|---|---|
| **Relying on the F10 map instead of navigation instruments** | Restrict F10 map access progressively — Phase 1: F10 allowed for awareness; Phase 2: F10 only for emergencies; Phase 3: no F10 |
| **Cannot interpret ADF bearing pointer** | Use a ground exercise with a diagram: draw the compass card, place the bearing pointer, and ask "Which direction is the station?" Repeat until instant |
| **VOR CDI confusion (fly toward or away from needle?)** | Rule: "Fly toward the needle" — if the CDI is deflected left, fly left to center it. This works for both TO and FROM indications |
| **Not resetting DG to compass** | Set a timer: every 10-15 minutes, the instructor asks "When did you last check the DG?" Build the habit |
| **No pre-flight navigation planning** | Require a completed kneecard before every navigation training event. No kneecard = no flight |
| **Ignoring wind correction** | Fly a DR leg without wind correction, then observe the error at the checkpoint. Repeat with wind correction and show the improvement. The contrast is instructive |
| **Not identifying VOR/NDB stations** | "If you can't hear the ident, you can't trust the needle." Enforce station identification by Morse code before using any nav aid |

---

## Module 8: Emergency Procedures

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Recite all boldface/immediate-action emergency procedures from memory.
2. Perform a complete autorotation from entry through touchdown (straight-in, 90°, and 180° profiles).
3. Recognize and recover from Loss of Tail Rotor Effectiveness (LTE).
4. Recognize and recover from settling with power (vortex ring state).
5. Describe governor failure indications and fly with manual throttle.
6. Describe hydraulic failure indications and execute a run-on landing without hydraulics.
7. Describe electrical failure management and bus load shedding.
8. Describe compressor stall recognition and recovery.
9. Explain mast bumping prevention, recognition, and why recovery is not possible once mast contact occurs.
10. Describe dynamic rollover conditions, prevention, and emergency procedures.
11. Identify which emergency procedures DCS models vs. which are academic-only.

---

### 8.1 Boldface / Immediate Action Items

**Boldface items** are emergency procedures that must be **memorized verbatim** and executed from memory without reference to a checklist. These are time-critical situations where seconds determine survival. Per TM 55-1520-210-10:

---

#### ENGINE FAILURE IN FLIGHT (Autorotation Entry)

```
1. COLLECTIVE .............. LOWER (immediately — maintain Nr)
2. THROTTLE ................ CLOSE (full counterclockwise to OFF)
3. AIRSPEED ................ ESTABLISH 65 KIAS (autorotation glide)
4. PEDALS .................. MAINTAIN HEADING (right pedal — no torque)
5. Nr ...................... MAINTAIN 294-324 RPM (with collective)
6. SELECT LANDING AREA ..... Plan approach
7. EXECUTE AUTOROTATION .... Flare → Collective pull → Touchdown
```

---

#### ENGINE FAILURE AT HOVER / LOW ALTITUDE

```
1. COLLECTIVE .............. ADJUST to cushion landing
                            (If altitude available: lower collective to maintain Nr,
                             then pull collective to cushion at touchdown)
2. CYCLIC .................. MAINTAIN LEVEL ATTITUDE
3. PEDALS .................. MAINTAIN HEADING
4. THROTTLE ................ CLOSE (after touchdown)
```

**Critical note:** At hover altitude (<50 ft), there is **no time** for a full autorotation. The pilot uses remaining rotor inertia to cushion the landing. The two-blade rotor has limited stored energy — reaction must be immediate.

---

#### ENGINE FIRE IN FLIGHT

```
1. THROTTLE ................ CLOSE (enter autorotation)
2. EMERGENCY FUEL SHUTOFF .. OFF (cut fuel to engine)
3. CABIN HEAT .............. OFF (prevent smoke/fumes in cockpit)
4. LAND IMMEDIATELY ........ Autorotate to nearest suitable area
5. After landing: BATTERY .. OFF, egress aircraft immediately
```

---

#### FUEL CONTROL / GOVERNOR FAILURE

```
1. GOVERNOR (GOV) SWITCH ... OFF
2. THROTTLE ................ MANUAL — adjust to maintain Nr 324 RPM
3. COLLECTIVE .............. COORDINATE with throttle
4. LAND AS SOON AS PRACTICABLE
```

---

#### EMERGENCY ENGINE SHUTDOWN (Ground)

```
1. THROTTLE ................ CLOSE (fuel cutoff)
2. FUEL VALVE .............. OFF
3. BATTERY ................. OFF
4. EVACUATE if fire suspected
```

---

#### HYDRAULIC SYSTEM FAILURE

```
1. AIRSPEED ................ ADJUST to 60-80 KIAS (manageable control forces)
2. AVOID HOVER ............. Run-on landing recommended
3. HYD CONTROL SWITCH ...... OFF (if controls are surging or uncommanded)
4. LAND AS SOON AS PRACTICABLE
```

---

#### TAIL ROTOR FAILURE / LOSS OF TAIL ROTOR THRUST

```
IF IN FORWARD FLIGHT (above ETL):
1. AUTOROTATE .............. Enter autorotation (reduces torque to near zero)
2. AIRSPEED ................ MAINTAIN above ETL — vertical fin provides directional stability
3. THROTTLE ................ CLOSE for landing
4. EXECUTE RUN-ON LANDING .. Do not attempt to hover

IF AT HOVER / LOW SPEED:
1. AUTOROTATE .............. Lower collective immediately
2. CYCLIC .................. FORWARD to gain airspeed if altitude permits
3. EXECUTE EMERGENCY LANDING
```

**Critical note:** Loss of tail rotor drive eliminates anti-torque. In powered flight, torque from the engine will spin the fuselage. The only remedy is to remove the torque (autorotate / close throttle) and use the vertical fin for directional stability at speed. **Never attempt to hover with no tail rotor.**

---

#### MAST BUMPING — LOW-G RECOVERY

```
1. AFT CYCLIC .............. GENTLY apply (reload the rotor disc)
2. DO NOT PUSH FORWARD ..... NEVER apply forward cyclic under low-G
3. COLLECTIVE .............. AS REQUIRED to reload disc
4. IF IMPACT HAS OCCURRED .. Mast separation is catastrophic — no recovery
```

---

### 8.2 Autorotation — Complete Procedure

Autorotation is the most critical emergency procedure in a single-engine helicopter. When the engine fails, the rotor must be **driven by the upward flow of air** through the disc rather than by the engine. The pilot trades altitude for rotor energy (Nr), then uses that stored energy in the flare and collective pull to cushion the landing.

#### Autorotation Phases

| Phase | Altitude | Action | Nr Management | Airspeed |
|---|---|---|---|---|
| **1. Entry** | Initial altitude | Collective down immediately; throttle close; right pedal | Nr recovering/stabilizing to 294-324 | Transitioning to ~65 KIAS |
| **2. Glide** | Descending at ~1,500-2,000 fpm | Maintain 65 KIAS with cyclic; select landing area; plan approach | Maintain 294-324 RPM with collective | 65 KIAS (best glide) or 55 KIAS (min sink) |
| **3. Flare** | ~75-100 ft AGL | Aft cyclic to raise the nose ~20-30°; rate of descent decreases; Nr increases (energy stored in flare) | Nr builds during flare — do NOT pull collective yet | Decelerating from 65 toward 0 |
| **4. Level & Pull** | ~10-15 ft AGL | Level the aircraft (cyclic forward to level attitude); pull collective firmly to trade rotor energy for lift | Nr decreasing rapidly as energy is consumed — one chance | Near 0 KIAS; descending slowly |
| **5. Touchdown** | Ground contact | Slight nose-up attitude; skids level; slide to a stop if any forward speed remains | Nr continuing to decay — landing is complete | 0 or near 0 |

#### Autorotation Profiles

| Profile | Description | When Used | Notes |
|---|---|---|---|
| **Straight-in** | From altitude, descend straight to the landing area without turns | Landing area is directly ahead; simplest profile | Preferred when alignment allows |
| **90° autorotation** | Enter autorotation, make a 90° turn to align with landing area, then straight-in | Landing area is off to one side | Single turn; moderate complexity |
| **180° autorotation** | Enter autorotation, make a 180° turn (overhead approach), then straight-in | Landing area is behind or requires significant repositioning | Most complex; highest risk of mismanaging energy |

#### Critical Timing — Two-Blade Rotor

The UH-1H two-blade teetering rotor has **less moment of inertia** than multi-blade systems:

| Factor | UH-1H (2-blade) | Multi-blade (e.g., UH-60, 4-blade) |
|---|---|---|
| **Nr decay rate after power loss** | Fast — Nr drops below 294 within ~2-3 seconds without collective reduction | Slower — more blades = more mass = more stored energy |
| **Time to lower collective** | Must be within **1-2 seconds** | Slightly more margin (~3-4 seconds) |
| **Flare energy available** | Less — must time flare precisely | More energy available; slightly more forgiving |
| **Collective pull cushion** | One pull, one chance — if you pull too early or too late, you cannot recover | More margin for timing errors |

**Training emphasis:** The autorotation entry must be a **reflex**. The pilot who hesitates for 3 seconds after power loss in a UH-1H will likely have Nr below recovery range. Drill this until the response is automatic: audio warning / power loss indication → collective DOWN.

#### Autorotation Speed Reference

| Condition | Best Speed | Rate of Descent | Notes |
|---|---|---|---|
| **Max range (best glide)** | ~65 KIAS | ~1,700 fpm | Maximum distance from altitude; use when landing area is distant |
| **Min rate of descent** | ~55 KIAS | ~1,500 fpm | Minimum time to reach ground; use when over a landing area |
| **Heavy (max GW)** | ~70 KIAS | ~2,000+ fpm | Higher weight = higher disc loading = faster descent |
| **Light (low GW)** | ~55 KIAS | ~1,400 fpm | Lower weight = better performance |

> *⚠ Realism Divergence: DCS models autorotation for the UH-1H with good fidelity. The rotor energy, Nr decay, glide performance, and flare/collective pull dynamics are well-represented. Some DCS-specific notes: (1) The DCS ground interaction during autorotation touchdown can be quirky — the skids may bounce or the aircraft may roll unexpectedly on uneven terrain. Practice on flat surfaces first. (2) The DCS autorotation is slightly more forgiving than the real aircraft in terms of Nr decay rate — the student should not rely on this margin. (3) Wind in DCS significantly affects autorotation landing point — always consider wind when selecting a landing area.*

---

### 8.3 Loss of Tail Rotor Effectiveness (LTE) — Detailed

LTE is the condition where the tail rotor's anti-torque capability is degraded by aerodynamic interference, resulting in uncommanded yaw (usually right yaw in U.S. helicopters).

#### LTE Causes (By Wind Azimuth)

| Wind Direction (Relative to Nose) | Azimuth Range | Mechanism | Risk Level |
|---|---|---|---|
| **Left rear quarter** | 285°-315° | Main rotor downwash vortex blown into tail rotor disc; turbulent air reduces tail rotor efficiency | High |
| **Rear (tail)** | 120°-240° | Weathercock effect — wind pushes the tail, yawing the nose into the wind; exceeds pedal authority | High — most common LTE trigger |
| **Left rear arc** | 210°-330° | Tail rotor vortex ring state — tailwind pushes disturbed air back through the tail rotor, collapsing its thrust | Very High — sudden onset with little warning |

#### LTE Recognition

- Uncommanded right yaw (nose swings right without pedal input).
- Inability to maintain heading with full left pedal.
- Increasing yaw rate that does not respond to pedal input.
- May be accompanied by unusual vibration or buffeting near the tail.

#### LTE Recovery

| Step | Action | Rationale |
|---|---|---|
| 1 | **Forward cyclic** — immediately | Gain airspeed; even 15-20 knots of forward speed dramatically improves directional stability (vertical fin becomes effective) |
| 2 | **Lower collective** — if altitude permits | Reduces torque; less anti-torque needed; reduces tail rotor demand |
| 3 | **Pedals** — do NOT add excessive left pedal if tail rotor is in vortex ring state | Adding pedal can worsen vortex ring state of the tail rotor; let airspeed cure the condition |
| 4 | **If spin develops and altitude is insufficient** | Autorotate — lower collective removes torque entirely; the yaw will stop (no torque = no anti-torque requirement) |

**Prevention:**
- Avoid prolonged hover with winds from the 210°-330° relative azimuth.
- Keep hover pedal turns slow and deliberate.
- Maintain awareness of wind direction at all times during hover and low-speed operations.
- If the wind shifts to a dangerous azimuth, accelerate into forward flight or land.

> *⚠ Realism Divergence: DCS models LTE for the UH-1H. The tail rotor vortex ring state and weathercock effects are modeled and will cause uncommanded yaw under the conditions described. DCS does a good job of representing this hazard. However, the exact onset azimuth and severity may vary slightly from the real aircraft. The student should experience LTE in DCS intentionally (under controlled conditions at altitude) to recognize the onset and practice recovery.*

---

### 8.4 Settling with Power (Vortex Ring State) — Detailed

| Entry Conditions | Threshold |
|---|---|
| **Airspeed** | Below ~30 KIAS |
| **Rate of descent** | Exceeding ~300 fpm |
| **Power** | Moderate to high (collective up, engine producing torque) |

**All three conditions must be present simultaneously.**

#### Recognition

- High rate of descent (1,000-3,000+ fpm) despite significant power application.
- Aircraft shuddering/vibrating — irregular turbulence in the rotor disc.
- Random pitch and roll excursions as the vortex disturbs the rotor symmetrically and asymmetrically.
- Increasing collective does NOT arrest the descent — it may worsen it.

#### Recovery

| Step | Action | Rationale |
|---|---|---|
| 1 | **Forward cyclic** — aggressively push cyclic forward | Gain airspeed to fly OUT of the vortex ring; the rotor must move into clean air |
| 2 | **Lower collective** — reduce power momentarily | Reduce the downwash that feeds the vortex; helps break the recirculation pattern |
| 3 | **Gain airspeed above 30 KIAS** | Once above 30 KIAS, the rotor disc is in clean air; normal flight resumes |
| 4 | **Apply power normally** | Once out of the vortex ring, climb away |

**Altitude required for recovery:** Typically 200-500 ft of altitude loss during recovery. If altitude is insufficient (below 500 ft AGL in VRS), the aircraft will impact the ground. **Prevention is the only reliable solution at low altitude.**

**Prevention:**
- Avoid steep approaches (>300 fpm descent) at low airspeed (<30 KIAS).
- During approaches, maintain at least 30-40 KIAS until very close to the hover point.
- If a steep, slow descent is required, keep the aircraft moving laterally or forward (even 10-15 knots breaks the VRS pattern).

> *⚠ Realism Divergence: DCS models settling with power/VRS for the UH-1H. The symptoms and recovery are representative. The student should practice deliberately entering VRS at altitude (2,000+ ft AGL) to recognize the onset and practice recovery. DCS recovery mechanics are similar to real-world, though the exact descent rate and recovery altitude may vary.*

---

### 8.5 Governor Failure

**Recognition:**
- Nr begins to fluctuate beyond normal governor range (wider than ±3 RPM).
- GOV EMER caution light may illuminate.
- Nr may trend high or low as collective changes without governor correction.

**Immediate Action:**
1. **GOV switch OFF** — disengage the malfunctioning governor.
2. **Throttle** — manually maintain Nr at 324 RPM using twist-grip.
3. The correlator still functions — collective changes still approximate fuel flow adjustment.
4. **Fly conservatively** — smooth, deliberate collective inputs to give yourself time to correct Nr with throttle.
5. **Land as soon as practicable** — governor failure is manageable but significantly increases pilot workload.

**Manual Throttle Technique:**
- **Collective up** → twist throttle in (clockwise) to add fuel → Nr wants to drop, must add fuel.
- **Collective down** → twist throttle out (counterclockwise) to reduce fuel → Nr wants to rise, must reduce fuel.
- **Turns/gusts** → Nr will vary — constant small throttle adjustments needed.
- **Priority:** Nr management. If you must sacrifice something, sacrifice precise heading or altitude to maintain Nr within limits.

> *⚠ Realism Divergence: DCS models governor failure as a clean switchover to manual throttle. The real UH-1H can experience partial governor malfunctions (hunting, delayed response, intermittent engagement) that are more challenging to diagnose and manage than the binary DCS failure. The student should practice the manual throttle exercise (Module 4) extensively to prepare for governor failure.*

---

### 8.6 Hydraulic Failure

**Recognition:**
- Flight controls become **extremely heavy** — sudden increase in control forces.
- HYDRAULIC PRESS caution light may illuminate.
- Hydraulic pressure gauge drops to zero or abnormally low.
- Possible master caution light.

**Flight Characteristics Without Hydraulics:**
- Cyclic forces: 40-60+ lbs depending on airspeed and maneuver.
- Collective forces: Heavy but manageable.
- Pedal forces: Very heavy.
- The aircraft is flyable but fatiguing. Precise control is difficult.
- Best speed for manageable forces: **60-80 KIAS**.

**Procedure:**
1. Maintain control — adjust airspeed to 60-80 KIAS (most comfortable).
2. Plan a **run-on landing** at the nearest suitable field.
3. Avoid hover — hovering without hydraulics is extremely difficult and dangerous due to the constant corrections required.
4. Use a shallow approach angle with forward speed maintained to touchdown.
5. Touch down at 20-30 knots forward speed; slide to a stop on the skids.
6. After stop: normal shutdown.

> *⚠ Realism Divergence: DCS models hydraulic failure with increased control forces. The simulation provides a good representation of the difficulty. However, the actual physical effort required in the real aircraft is difficult to replicate with a desktop joystick. Students using force-feedback sticks or high-resistance spring sticks will get a better approximation. The real aircraft requires genuine arm strength to fly without hydraulics — DCS can only approximate this.*

---

### 8.7 Electrical Failure

**Generator Failure:**

| Step | Action | Notes |
|---|---|---|
| 1 | GEN caution light illuminates; voltmeter drops | Battery now sole power source |
| 2 | **GEN switch** — RESET, then ON | May restore generator |
| 3 | If generator does not reset: **Shed non-essential loads** | Turn off radios not needed for emergency, non-essential lights, non-critical equipment |
| 4 | **Battery endurance: ~30 minutes** | Varies with electrical load; prioritize essential instruments and one comm radio |
| 5 | **Land as soon as practicable** | Battery will eventually die; plan approach before it does |

**Essential loads to keep powered:**
- Flight instruments (attitude indicator, heading indicator — AC powered through inverter)
- One communication radio (VHF-AM for ATC or FM for tactical)
- Caution panel
- Engine instruments (most are direct-reading mechanical and do not require electrical power)

**Total Electrical Failure (Battery also dead):**
- Loss of all electrically powered instruments (AI, DG, radios, caution panel).
- Engine continues to run — the engine's mechanical fuel control does not require electrical power.
- Navigate by magnetic compass (mechanical) and outside reference.
- No radio communication available.
- Fly to nearest suitable airfield and execute a visual approach.
- Transponder on 7600 (radio failure) if set before battery died.

---

### 8.8 Compressor Stall

**Recognition:**
- Loud bang or series of bangs from the engine.
- EGT spike (may exceed limits).
- Possible power loss or power surge.
- Engine vibration.

**Recovery:**
1. Reduce throttle (lower collective) to decrease engine demand.
2. Allow the compressor to restabilize.
3. Slowly re-advance power.
4. If stall recurs: land as soon as practicable — possible engine damage.

> *⚠ Realism Divergence: DCS does not model dynamic compressor stall in the UH-1H. This is an academic knowledge item. The student should understand the concept as it is a real hazard for the T53 engine, particularly in sandy/dusty environments (FOD) or when operating at high altitude with deteriorated engine health.*

---

### 8.9 Fuel System Malfunctions

#### Fuel Boost Pump Failure

- FUEL BOOST caution light illuminates.
- Engine may continue to run on gravity feed in level flight.
- In unusual attitudes (steep bank, nose-up/down), gravity feed may be interrupted.
- **Action:** Land as soon as practicable; maintain level flight to maximize gravity feed reliability.

#### Fuel Filter Bypass

- FUEL FILTER caution light illuminates.
- Fuel is bypassing the filter due to contamination.
- Engine continues to operate but unfiltered fuel is reaching the engine — risk of fuel control contamination.
- **Action:** Land as soon as practicable.

#### Fuel Starvation vs. Fuel Exhaustion

| Condition | Cause | Indication | Action |
|---|---|---|---|
| **Fuel starvation** | Fuel in tanks but not reaching engine (valve closed, line blocked, boost pump failed) | EGT drops, N1 decreases, Nr decreases, fuel quantity shows remaining fuel | Autorotate; check fuel valve, boost pump, fuel selector |
| **Fuel exhaustion** | No fuel remaining | Same as starvation but fuel quantity reads zero or near-zero | Autorotate immediately; no recovery possible |

---

### 8.10 Transmission Failure Indications

The main transmission is a critical component. Failure indications:

| Indication | Severity | Action |
|---|---|---|
| **CHIP DET light** | Possible metallic contamination; early warning | Land as soon as possible; metal particles may indicate internal wear or pending failure |
| **XMSN OIL PRESS low** | Loss of lubrication | Land immediately — transmission may seize without oil pressure |
| **XMSN OIL TEMP high (>120°C)** | Overheating | Reduce power; land immediately — overheating may cause gear failure |
| **Unusual noise/vibration from transmission area** | Possible gear or bearing failure | Reduce power; land immediately at nearest suitable area |

**"Land as soon as possible" vs. "Land as soon as practicable":**
- **As soon as possible** = land NOW at the nearest point where a safe landing can be made, even if it is not an airfield (field, road, clearing). The situation is critical.
- **As soon as practicable** = land at the nearest suitable airfield or safe landing area without unnecessarily extending flight. The situation is serious but not immediately critical.

---

### 8.11 Mast Bumping — Prevention and Emergency Response

*Repeated from Module 1 with additional emergency emphasis.*

**The UH-1H's teetering rotor makes mast bumping the most feared and least recoverable emergency.**

**Prevention (the ONLY effective response):**
1. Never push forward cyclic aggressively — ever.
2. Maintain positive G at all times.
3. In turbulence: slow down, fly at moderate power, accept ride quality rather than trying to smooth it with cyclic.
4. After engine failure: establish autorotation with smooth control inputs. Do NOT push the nose over.
5. During formation flying or maneuvering: avoid abrupt cyclic movements.
6. Light gross weight increases susceptibility — be more cautious at lighter weights.

**If mast bumping occurs:**
- If the mast separates, the main rotor departs the aircraft. There is no recovery. The aircraft is uncontrollable and will impact the ground.
- If a mild bump occurs (contact without separation — extremely unlikely to recognize in time): gently apply aft cyclic to reload the disc, reduce collective to reduce power, and land immediately for inspection.
- **Realistically:** If you feel mast bumping, it is already too late. Prevention is the only viable strategy.

---

### 8.12 Dynamic Rollover

**Conditions:**
- One skid on the ground (slope operations, uneven terrain).
- Lateral drift at touchdown or liftoff.
- Crosswind pushing the aircraft laterally.
- External force (sling load, tiedown not removed).

**Critical roll rate:** If roll rate exceeds ~10°/second around the ground contact point, cyclic authority is insufficient to stop the roll.

**Emergency Procedure:**
- **If roll rate is low (<10°/sec) and still early:** LOWER COLLECTIVE — reduce lift, place the aircraft back on the ground, re-establish both skids on the surface.
- **If roll rate is high (>10°/sec):** It may be too late for collective reduction to stop the roll. Full opposite cyclic and collective reduction are attempted, but recovery is uncertain once the critical rate is exceeded.

**Prevention:**
- During slope operations: limit lateral roll rate, keep the upslope skid in contact as long as possible.
- During liftoff in crosswind: lift off smoothly and transition to forward flight quickly.
- Always verify tiedowns and external connections are removed before liftoff.

---

### 8.13 DCS Emergency Modeling Summary

| Emergency | DCS Models It? | Fidelity | Notes |
|---|---|---|---|
| **Engine failure** | Yes | High | Realistic Nr decay, autorotation dynamics |
| **Engine fire** | Yes | Moderate | Fire warning; shutdown procedure works |
| **Governor failure** | Yes | High | Manual throttle required; good practice |
| **Hydraulic failure** | Yes | High | Heavy controls; run-on landing required |
| **Tail rotor failure** | Yes | High | Loss of anti-torque; autorotation required |
| **LTE** | Yes | High | Tail rotor effectiveness modeled by wind azimuth |
| **Settling with power / VRS** | Yes | High | Symptoms and recovery representative |
| **Mast bumping** | Yes | High | Can destroy the aircraft; good training |
| **Dynamic rollover** | Yes | Moderate | Modeled during slope operations |
| **Compressor stall** | No | N/A | Academic knowledge only |
| **Generator failure** | Yes | Moderate | Electrical system failure chain modeled |
| **Fuel starvation/exhaustion** | Yes | Moderate | Engine quits when fuel runs out |
| **Transmission failure** | Partial | Low | Chip detector light; limited failure progression |

**Triggering Emergencies in DCS:**
- Failures can be set in the **Mission Editor** (pre-set or random).
- The **DCS failure system** can trigger specific failures at a given time, probability, or condition.
- For BQT training: set engine failure at a specific time to practice autorotation entries. Vary the altitude and flight condition.

---

### Instructor Notes — Module 8

| Common Student Error | Correction |
|---|---|
| **Delayed collective reduction on engine failure** | Drill until reflexive — instructor calls "engine failure," student must lower collective within 2 seconds. No exceptions. The two-blade rotor does not forgive hesitation |
| **Forgetting right pedal in autorotation** | Build it into the drill: "Collective down, right pedal, 65 KIAS." Three things, in order, every time |
| **Flare too early or too late** | Practice straight-in autorotations repeatedly. Start at altitude with power recovery, then progress to full touchdown. Flare at ~75-100 ft AGL; the flare is by feel as much as altitude reference |
| **Pulling collective too early in autorotation** | "Wait for the flare to do its job." The flare kills forward speed and rate of descent AND builds Nr. Pull collective only when the aircraft is level and close to the ground (~10-15 ft) |
| **Panic during LTE** | Practice LTE intentionally at altitude. The first encounter is terrifying; subsequent encounters build confidence. Emphasize: "Forward cyclic. That's the cure. Forward cyclic." |
| **Adding power during VRS** | "Collective DOES NOT help in VRS — it makes it worse. Push forward first." Counter-intuitive but critical |
| **Pushing forward cyclic during mast bumping awareness** | "Aft cyclic is always safe. Forward cyclic under low-G is lethal." Repeat this mantra every flight until it is internalized |
| **Over-torquing during autorotation power recovery** | Smooth power application — watch the torque gauge. The governor helps, but during the transition from idle to powered flight, torque can spike. Coordinate collective and throttle smoothly |
| **Not knowing boldface from memory** | Quiz at the beginning of every flight brief. Student must recite engine failure, engine fire, and hydraulic failure boldface from memory before the aircraft is started. No perfect recitation = no flight |

---

## Module 9: Approach & Landing

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Execute a standard VFR traffic pattern and approach in the UH-1H.
2. Perform a normal approach to a hover and a normal landing.
3. Perform a steep approach to a confined area or restricted zone.
4. Perform a shallow/running landing.
5. Execute a go-around (wave-off) from any point in the approach.
6. Perform crosswind approach and landing.
7. Perform slope landings (left/right/nose-up/nose-down slopes).
8. Describe confined area operations (recon, approach, landing, departure).
9. Describe pinnacle and ridgeline operations.
10. Use the radar altimeter and visual references for approach altitude management.

---

### 9.1 VFR Traffic Pattern

The standard helicopter VFR traffic pattern is typically smaller and lower than fixed-wing patterns. For the UH-1H at an uncontrolled field:

| Pattern Leg | Altitude (AGL) | Airspeed | Notes |
|---|---|---|---|
| **Upwind** (after takeoff) | Climbing through 200-500 ft | 60 KIAS accelerating | Normal takeoff; begin turn to crosswind at 200-300 ft AGL |
| **Crosswind** | 500 ft AGL | 70-80 KIAS | 90° turn from runway heading; level off at pattern altitude |
| **Downwind** | 500 ft AGL | 80-90 KIAS | Parallel to landing direction; offset ~500-800 ft laterally |
| **Base** | Begin descent from 500 ft | 60-70 KIAS decelerating | 90° turn toward landing area; begin descent |
| **Final** | Descending to hover | 50-60 KIAS decelerating | Aligned with landing point; approach angle ~6-10° |

**Pattern entry/exit:**
- Enter the pattern at a 45° angle to the downwind leg.
- When departing, fly the upwind leg and depart straight out or at a 45° angle.
- Communicate intentions on the appropriate frequency (CTAF or tower).

**DCS-specific notes:**
- Many DCS maps have helipads rather than full airfields. Traffic patterns may be adapted to the terrain and helipad location.
- The student should practice traffic patterns at established DCS airfields before moving to tactical helipads.

---

### 9.2 Normal Approach to a Hover

The standard approach profile for a UH-1H landing at a prepared surface:

| Phase | Altitude | Airspeed | Power (Collective) | Description |
|---|---|---|---|---|
| **Initial approach** | Pattern altitude (~500 ft AGL) | 80-90 KIAS | Cruise power | Downwind leg; configure for approach |
| **Base turn** | Begin descent from 500 ft | 60-70 KIAS | Reduce slightly | Turn to base; start gradual descent |
| **Final approach** | 300 ft → descending | 50-60 KIAS, decelerating | Reducing progressively | Stabilize descent angle (~6-10°); aim at landing point |
| **Short final** | 100-50 ft AGL | 30-40 KIAS, decelerating | Increasing (decelerating requires power to maintain glidepath) | The aircraft is decelerating through ETL (16-24 KIAS); expect increased power required as translational lift diminishes |
| **Hover** | 3-5 ft skid height | 0 KIAS | Hover power (~38-42 PSI torque depending on GW/DA) | Stabilize in a hover over the landing point |
| **Touchdown** | 0 ft | 0 KIAS | Reduce collective to lower aircraft to ground | Smoothly lower collective; both skids contact simultaneously |

#### Approach Angle Reference

| Approach Type | Angle | Airspeed Profile | When Used |
|---|---|---|---|
| **Normal** | ~6-10° | Gradual deceleration from 60 KIAS to hover | Standard approach to prepared pads |
| **Steep** | ~12-15° | Faster deceleration; more collective management | Confined areas; obstacles on approach path |
| **Shallow / Running** | ~3-6° | Maintain higher airspeed to near-touchdown | When power is limited; high DA/heavy GW; no-hover landings |

#### Transitioning Through ETL

The most critical phase of the approach is the deceleration through Effective Translational Lift (ETL, ~16-24 KIAS):

- As airspeed decreases below ETL, the induced power requirement **increases sharply**.
- The pilot must **raise collective** progressively to maintain the glidepath as translational lift diminishes.
- If insufficient power is available (high DA, heavy GW), the aircraft will sink rapidly below the glidepath.
- The nose will tend to pitch up as the aircraft decelerates — manage with forward cyclic.
- Left pedal is required as power increases (torque effect).

---

### 9.3 Steep Approach

Used when obstacles exist on the approach path or when landing in a confined area with limited overshoot space.

| Parameter | Value | Notes |
|---|---|---|
| **Approach angle** | 12-15° (steeper than normal) | Requires more power management |
| **Entry airspeed** | 50-60 KIAS | Begin from a higher altitude relative to distance |
| **Rate of descent** | 700-1,000+ fpm initially | Higher than normal approach |
| **Power management** | Critical — as airspeed decreases, collective must increase to arrest descent rate | Risk of exceeding power available at high DA/heavy GW |
| **Flare / deceleration** | More aggressive deceleration at the bottom of the approach | The pilot trades forward speed for lift in the flare |
| **Go-around** | More difficult — obstacles behind, limited overshoot area | Commit point must be identified before starting the approach |

**Procedure:**
1. Identify the landing area and approach path from the downwind leg.
2. Plan the approach to clear all obstacles with safe margin.
3. Establish the steep approach angle, reducing airspeed and increasing descent rate.
4. As the aircraft nears the landing area, progressively decelerate and raise collective.
5. Transition to a hover over the landing point.
6. Land normally.

**Hazards:**
- Steep approaches put the aircraft close to settling with power (VRS) conditions — high descent rate + low airspeed + high power.
- If the approach becomes too steep and airspeed drops below 30 KIAS with a high rate of descent, VRS is possible.
- Always maintain forward airspeed above 30 KIAS until the final deceleration to hover.

---

### 9.4 Shallow / Running Landing

Used when power available is insufficient for a hover landing (high density altitude, heavy gross weight, or power margin is limited).

| Phase | Airspeed | Altitude | Notes |
|---|---|---|---|
| **Approach** | 50-60 KIAS | Gradual descent at ~3-6° | Shallower than normal approach |
| **Short final** | 20-30 KIAS | 5-10 ft AGL | Maintain translational lift as long as possible |
| **Touchdown** | 10-20 KIAS ground speed | Skids touch ground with forward speed | Slide forward on skids until decelerated |
| **Ground roll** | Decelerating to 0 | On the ground | Lower collective fully; do not attempt to hover |

**Technique:**
- The key is to **never lose translational lift until the skids are on the ground**.
- The aircraft touches down with forward speed, maintaining translational lift until ground contact.
- After touchdown, smoothly lower collective to full down; the aircraft slides forward on the skids and decelerates.
- This requires a smooth, firm surface. Running landings on soft, muddy, or rocky terrain may cause the skids to dig in and the aircraft to pitch forward.

**When required:**
- High density altitude (DA > 6,000 ft) where hover power exceeds available power.
- Heavy gross weight (near or at max GW) where hover power exceeds available.
- One engine inoperative in multi-engine helicopters (not applicable to UH-1H's single engine, but the technique applies to any low-power situation).
- Hydraulic failure — a run-on landing avoids the difficulty of hovering without hydraulics.

---

### 9.5 Go-Around (Wave-Off)

A go-around can be executed from any point in the approach where the pilot determines the approach is unstable, unsafe, or will not result in a safe landing.

**Procedure:**
1. **Power** — smoothly increase collective to climb power (watch torque — do not exceed limits).
2. **Cyclic** — lower the nose slightly to accelerate; establish a positive climb rate.
3. **Pedals** — adjust for torque (left pedal as power increases).
4. **Airspeed** — accelerate to Vy (60 KIAS) for best rate of climb.
5. **Announce** — "Going around" on the appropriate frequency.
6. **Re-enter the pattern** — climb to pattern altitude and re-enter the traffic pattern for another approach.

**Decision criteria for go-around:**
- Approach is unstable (too fast, too slow, too high, too low).
- Obstacle or traffic conflict.
- Crosswind exceeds comfort level or aircraft capability.
- Power required exceeds power available (aircraft not responding to collective input on approach).
- Any doubt about the safety of the landing.

**"Go around early, go around often."** There is no penalty for a go-around. There is a severe penalty for forcing a bad approach to a landing.

---

### 9.6 Crosswind Approach and Landing

| Wind Condition | Technique | Notes |
|---|---|---|
| **Light crosswind (5-10 kt)** | Crab angle on approach; transition to sideslip near touchdown | Manageable with normal technique |
| **Moderate crosswind (10-20 kt)** | Crab or sideslip on approach; maintain heading alignment with pedals | Requires more coordination; ensure upwind skid touches first |
| **Strong crosswind (>20 kt)** | Consider alternate landing direction; if no alternative, use significant crab and coordinate aggressively near the ground | High pilot workload; near the limits of the aircraft in some conditions |

**Crosswind hover technique:**
- In a hover, the wind pushes the aircraft laterally. Counter with cyclic into the wind.
- The tail may weathervane (wind pushes the tail downwind) — correct with pedals.
- Maintain ground position with a combination of cyclic (lateral) and pedals (heading).

**Crosswind landing technique:**
1. On approach, crab into the wind to maintain ground track alignment with the landing point.
2. Near the ground (below 50 ft), transition from crab to sideslip — lower the upwind wing (cyclic into wind) and maintain heading with opposite pedal.
3. Touch down on the upwind skid first, then lower the downwind skid.
4. After both skids are on the ground, lower collective fully to plant the aircraft firmly.

---

### 9.7 Slope Landing

Helicopters frequently land on sloping terrain. The UH-1H can safely land on slopes up to approximately **5-7°** depending on conditions.

#### Technique by Slope Direction

| Slope Direction | Technique | Hazard |
|---|---|---|
| **Left slope** (left skid uphill) | Approach from uphill side; lower aircraft until uphill (left) skid contacts ground; slowly lower collective while maintaining level fuselage with cyclic; downhill (right) skid contacts as collective decreases | **Dynamic rollover** — if the aircraft rolls toward the downhill side, it may exceed the critical rollover angle around the uphill skid contact point |
| **Right slope** (right skid uphill) | Mirror of left slope procedure; same dynamic rollover risk toward the downhill (left) side | Same risk; additionally, the tail rotor is on the left side — ensure sufficient clearance from the slope |
| **Nose-uphill slope** | Approach to the slope; uphill skids (front) touch first; lower collective while maintaining position with cyclic | Less dynamic rollover risk; more stable; preferred when slope direction can be chosen |
| **Nose-downhill slope** | Least preferred; downhill skids touch first; risk of the aircraft sliding or nose pitching over | **Avoid if possible** — the aircraft may slide forward on the slope, and the mast angle relative to the slope may reduce rotor clearance |

**Dynamic Rollover Prevention during Slope Operations:**
1. Keep movements slow — never snatch the collective up.
2. If you feel the aircraft begin to roll toward the downhill side, **immediately lower collective** to plant both skids.
3. Maintain the upslope skid in contact with the ground during the entire collective-lowering process.
4. If the roll rate exceeds your ability to correct with cyclic, lowering collective is the last resort.

---

### 9.8 Confined Area Operations

A confined area is a landing zone surrounded by obstacles (trees, buildings, wires) that restrict the approach and departure paths.

#### Confined Area Procedure

| Phase | Action | Notes |
|---|---|---|
| **1. Reconnaissance** | Overfly the area at altitude (500-1,000 ft AGL); identify obstacles, wind direction, approach/departure paths, surface conditions | Never land in an area you haven't surveyed. Plan the escape route (go-around path) before committing |
| **2. High Recon** | Orbit or fly past at 500+ ft; note: wind indicators (smoke, dust, vegetation), obstacle heights, wires, surface slope, surface type | In DCS, use F2 external view or map to assist recon; in realistic training, use cockpit view only |
| **3. Low Recon** | Fly the intended approach path at a safe altitude (above obstacles); confirm obstacle clearance, wind effect, and that the area is suitable | This is the final check before commitment. If anything is unsatisfactory, abort and select a different area |
| **4. Approach** | Execute the approach (usually steep approach) along the planned path; clear obstacles with safe margin | Maintain power margin awareness — if power required approaches power available, go around before committing |
| **5. Landing** | Terminate to a hover, then land; or execute a running landing if power is limited | After landing, note the departure path and any changes in conditions |
| **6. Departure** | Depart along the planned departure path; obstacles are behind and below | Use max performance takeoff if obstacles are close |

**Key confined area considerations:**
- **Wind:** Always plan approach into the wind if possible. Headwind reduces power required and shortens the approach.
- **Wires:** The most dangerous obstacle. Wires are nearly invisible, especially in DCS. Assume wires are present near any road, building, or utility pole.
- **Power margin:** Calculate power required vs. power available before committing. If the margin is thin, do not attempt the confined area landing.
- **Escape route:** Always have a go-around plan. If the approach goes wrong, where will you fly to?

---

### 9.9 Pinnacle and Ridgeline Operations

A pinnacle is an elevated point of terrain (hilltop, ridge) that falls away on all sides.

#### Pinnacle Approach Considerations

| Factor | Consideration |
|---|---|
| **Wind** | Wind at a pinnacle is often stronger and more turbulent than at lower elevations; expect updrafts on the windward side and downdrafts/turbulence on the leeward side |
| **Approach direction** | Always approach into the wind along the windward side; never fly through the downdraft area on the leeward side at low altitude |
| **Power** | Higher elevation = higher density altitude = less power available; the aircraft may be power-limited at the pinnacle |
| **Ground effect** | Ground effect is reduced or absent on a pinnacle (the terrain falls away from the rotor disc); expect OGE power required |
| **Turbulence** | Expect mechanical turbulence from the terrain, especially in moderate to strong winds; maintain a higher-than-normal approach speed for controllability |

**Technique:**
1. Approach from the windward side, slightly above the pinnacle elevation.
2. Terminate to a hover at the pinnacle; expect OGE hover power requirement (no ground effect).
3. Land smoothly; the surface may be uneven (slope landing technique may be needed).
4. Depart off the windward side (into the wind); avoid the leeward downdraft.

---

### 9.10 Night Approach and Landing Considerations

| Factor | Day | Night |
|---|---|---|
| **Visual references** | Abundant — ground texture, obstacles clearly visible | Limited — reduced depth perception, reliance on lighting and instruments |
| **Approach technique** | Normal visual approach | Use radar altimeter for altitude; cross-reference with baro altimeter; maintain instrument scan through the approach |
| **Landing zone identification** | Visual — easy | Requires lighting (landing light, NVG, or illuminated pad). DCS UH-1H has a searchlight/landing light |
| **Spatial disorientation risk** | Low | High — especially over water or featureless terrain at night |
| **Go-around threshold** | Standard | Lower — go around earlier if anything is uncertain |

**DCS Night Operations:**
- The UH-1H has a **searchlight** (Landing Light switch) that can illuminate the landing area.
- Use the **radar altimeter** (`RadAlt`) for precise AGL altitude on approach.
- NVG mode is available in DCS — adjust cockpit lighting to NVG-compatible (green/low intensity) if using NVG.
- Practice night approaches in DCS using the instrument approach technique: radar altimeter for altitude, airspeed indicator for speed, visual references only for the final 50 ft to hover.

> *⚠ Realism Divergence: DCS night operations are visually darker than real-world NVG operations but also lack many real-world ambient light sources. The DCS searchlight provides good illumination of the landing area. Real-world UH-1H night operations were often conducted with NVG (AN/AVS-6 or similar) which provide a broader field of illuminated view than the DCS searchlight. DCS NVG mode is a reasonable approximation but does not replicate the depth perception challenges of real NVG operations.*

---

### Instructor Notes — Module 9

| Common Student Error | Correction |
|---|---|
| **Coming in too fast on final** | Decelerate early. If still at 60 KIAS inside 300 ft AGL, the approach is too fast. Start slowing on base turn |
| **Not managing power through ETL transition** | "As the airspeed bleeds through 20 knots, you need to be pulling collective. If you don't, you'll fall through." Practice the ETL transition at altitude until the power-for-airspeed trade is intuitive |
| **Failing to go around on a bad approach** | Positive reinforcement for go-arounds. "Good decision" every time. Students who feel pressured to land will force bad approaches. Eliminate that pressure |
| **Running out of pedal in a crosswind** | If near full pedal and still drifting/yawing, the wind exceeds the aircraft's capability for that hover direction. Turn the nose into the wind or go around |
| **Rushing slope landings** | "Slow is smooth, smooth is fast." Slope landings require patience. Lower the collective slowly, watching for any roll tendency. If it starts to roll, collective DOWN immediately |
| **Not performing recon before confined area landing** | Refuse to allow students to land in an unrecognized area. "What's the surface? Where are the wires? Where's the wind from? What's your go-around path?" All must be answered before the approach begins |
| **Approaching pinnacle from leeward side** | "Always approach from the windward side. The leeward side has turbulence and downdrafts that can put you into the terrain." Demonstrate the wind effects at altitude first |
| **Fixating on the landing point and losing instrument scan** | "Eyes up, scan the instruments, then back to the landing point." Especially important at night or in reduced visibility. Maintain a scan pattern even on visual approach |

---

## Module 10: Shutdown & Post-Flight

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Execute a complete normal engine shutdown from idle to fully secured aircraft.
2. Perform a post-shutdown walk-around inspection.
3. Describe the proper sequence for de-energizing electrical systems.
4. Explain the engine cooldown requirement and its purpose.
5. Identify DCS-specific shutdown behaviors and any divergence from the real aircraft.

---

### 10.1 Pre-Shutdown Checks (Before Engine Shutdown)

After landing and coming to a stable hover or ground contact, perform these checks before initiating engine shutdown:

| Step | Action | Notes |
|---|---|---|
| 1 | **Parking area** — Position the aircraft in the designated parking spot, aligned with the desired heading | On helipads: center the aircraft; on ramps: follow ground crew marshalling |
| 2 | **Collective** — Full down; aircraft firmly on the ground | Verify both skids are firmly planted; no rocking or instability |
| 3 | **Throttle** — Reduce to idle (full counterclockwise to the idle detent — NOT to cutoff) | Allow the engine to stabilize at idle (~60% N1); rotor RPM will decrease to idle range |
| 4 | **Engine idle cooldown** — Run at idle for **2 minutes minimum** | This allows the turbine to cool gradually. Shutting down immediately after high-power operation can cause thermal stress, turbine blade warping, and hot section damage |
| 5 | **Radios** — Set frequencies as required; make shutdown/parking call if appropriate | "Tower, [callsign], shutting down at [location]" or as directed |
| 6 | **Transponder** — OFF or STANDBY | No longer transmitting |
| 7 | **Navigation equipment** — OFF (ADF, VOR) | De-energize nav receivers |

---

### 10.2 Engine Shutdown Procedure

**After the 2-minute cooldown at idle, execute the following sequence in order:**

| Step | Control / Switch | Position | Panel Location | Notes |
|---|---|---|---|---|
| 1 | **Throttle** | Rotate full counterclockwise past idle detent to **CUTOFF** | Collective grip | This cuts fuel to the engine. N1 and EGT will begin to decrease |
| 2 | **Monitor EGT** | Observe EGT decreasing | Engine instrument panel | EGT should decrease smoothly. If EGT stalls or rises, there may be a residual fuel issue (unlikely but monitor) |
| 3 | **Monitor Nr / N1** | Observe rotor RPM and N1 decreasing | Engine instrument panel | Nr will coast down as the rotor decelerates; N1 will drop to zero. The rotor takes approximately 1-2 minutes to stop fully |
| 4 | **Wait for rotor stop** | Observe the main rotor blades coming to a complete stop | Visual reference (look up through chin bubble or side windows) | **NEVER exit the aircraft or allow personnel to approach until the rotor has completely stopped** |
| 5 | **Fuel valve** | **OFF** (closed) | Lower console / overhead (per aircraft configuration) | Shuts off fuel supply at the tank; prevents fuel from reaching the engine even if throttle is inadvertently opened |
| 6 | **Generator switch** | **OFF** | Overhead console | Disconnects the generator from the bus; no longer charging the battery |
| 7 | **Battery switch** | **OFF** | Overhead console | De-energizes the entire electrical system; all lights, instruments, and avionics power down |
| 8 | **All remaining switches** | **OFF** | All panels | Verify: all toggle switches OFF, all circuit breakers in (or as placarded), all knobs in the OFF/detent position |

---

### 10.3 Rotor Brake (If Applicable)

The real UH-1H has a **rotor brake** that can be applied after the engine is shut down to slow the rotor to a stop more quickly. The rotor brake should only be applied when Nr has decreased below approximately **50% of normal RPM** — applying it at higher RPM can damage the brake or the rotor system.

| Rotor Brake Step | Action | Notes |
|---|---|---|
| 1 | Wait for Nr to decrease to <50% (~160 RPM) | Visual reference — blades are rotating slowly enough to count individual blades |
| 2 | Apply rotor brake gradually | Do NOT slam the brake on; apply progressively |
| 3 | Hold until rotor stops | Release the brake once the rotor is fully stopped |

> *⚠ Realism Divergence: The DCS UH-1H does not model a rotor brake. After engine shutdown, the rotor will coast to a stop on its own over approximately 1-2 minutes of simulation time. The student should wait for the rotor to stop before considering the aircraft "secured" — same as the real aircraft procedure, minus the rotor brake application.*

---

### 10.4 Post-Shutdown Walk-Around

After the rotor has stopped and the aircraft is fully de-energized:

| Inspection Item | What to Check | Notes |
|---|---|---|
| **Main rotor blades** | Damage, erosion, cracks, security of blade bolts | Visual inspection from the ground; note any leading-edge erosion or nicks |
| **Tail rotor** | Blade condition, security, tail rotor gearbox area for leaks | Approach from the side — never walk under the tail boom toward the tail rotor |
| **Engine exhaust** | Foreign object debris, unusual deposits, discoloration | Black soot is normal; unusual coloring may indicate engine issues |
| **Transmission / mast area** | Oil leaks, fluid seepage, any visible damage | Check the area around the transmission cowling |
| **Hydraulic system** | Fluid leaks on actuators, lines, or reservoir | Check servo actuators beneath the aircraft |
| **Landing skids** | Damage from hard landings, deformation, crosstube condition | After slope landings, check for bending; after running landings, check for wear |
| **Fuel system** | Leaks, fuel cap security, drain valve condition | Ensure fuel cap is secure; check for fuel stains or drips |
| **External skin / structure** | Dents, cracks, loose panels, missing fasteners | General walk-around looking for anything unusual |
| **Tiedowns** | Secure the aircraft if it will be parked for an extended period | Main rotor blade tiedowns, skid tiedowns to pad anchors |

---

### 10.5 Post-Flight Documentation

In real-world operations, the pilot completes post-flight documentation:

| Document | Purpose | Notes |
|---|---|---|
| **DA Form 2408-12** (Army Aircraft Maintenance and Inspection Record) | Record flight hours, discrepancies, maintenance required | The pilot notes any malfunctions, unusual behavior, or damage observed |
| **Logbook entry** | Record flight time, mission, crew | Standard military aviation record-keeping |
| **Discrepancy report** | Any malfunction or abnormality must be documented for maintenance action | "Write it up" — every fault, no matter how small, must be recorded |

**DCS relevance:** While DCS does not require paperwork, the habit of mentally reviewing the flight for any abnormalities is valuable. Did anything unusual happen? Did an instrument read abnormally? Did the aircraft handle differently? This debrief discipline translates to better situational awareness on subsequent flights.

---

### 10.6 Emergency Shutdown (Engine Fire on Ground)

If an engine fire is suspected or observed during ground operations:

| Step | Action | Priority |
|---|---|---|
| 1 | **Throttle** — CUTOFF immediately | Eliminate fuel flow to the engine |
| 2 | **Fuel valve** — OFF | Isolate the fuel supply entirely |
| 3 | **Battery** — OFF | De-energize to prevent electrical arcing or ignition |
| 4 | **Evacuate** — All crew and passengers exit immediately | Move upwind and at least 100 ft from the aircraft |
| 5 | **Fire extinguisher** — If available and fire is small, attempt to extinguish | Only if safe to do so; if fire is large or spreading, evacuate and wait for fire crew |

---

### 10.7 Hot Refueling (Engine Running)

Hot refueling (refueling with the engine running and rotors turning) is an operational procedure used when rapid turnaround is required.

| Step | Action | Notes |
|---|---|---|
| 1 | **Collective** — Full down, aircraft on ground | Skids firmly planted |
| 2 | **Throttle** — Idle | Engine at ground idle; Nr in idle range |
| 3 | **All electrical equipment near fuel** — Consideration for spark sources | Radio transmissions may be restricted during fueling (depends on SOP) |
| 4 | **Passengers/cargo** — Deplane if SOP requires | Ground crew manages fueling |
| 5 | **Pilot** — Remain at the controls throughout | Ready for emergency shutdown if fuel spill or fire occurs |
| 6 | **After fueling** — Verify fuel quantity; resume operations | Check fuel gauge after fueling; verify cap secured |

> *⚠ Realism Divergence: DCS models hot refueling at FARP (Forward Arming and Refueling Point) locations. The UH-1H can be refueled and rearmed at a FARP with the engine running. The DCS process is simplified — taxi to the FARP pad, and the rearm/refuel menu appears. The real-world hot refueling procedure is more complex and involves ground crew coordination, grounding straps, and safety protocols that are not modeled in DCS.*

---

### 10.8 Securing the Aircraft for Extended Parking

| Item | Action | Notes |
|---|---|---|
| **Main rotor blades** | Secure with blade tiedown straps | Prevent wind from moving the blades and causing mast damage |
| **Pitot tube cover** | Install if available | Prevents insects/debris from blocking the pitot system |
| **Engine intake covers** | Install if available | Prevents FOD from entering the engine intake during storage |
| **Exhaust cover** | Install if available | Prevents birds/debris from nesting in the exhaust |
| **Skid tiedowns** | Secure to pad or ground anchors | Prevents the aircraft from being moved by wind |
| **Cockpit** | All switches OFF; canopy/doors closed or secured | Prevent rain/moisture intrusion |

---

### 10.9 Complete Shutdown Sequence — Quick Reference

The following is a condensed, step-by-step quick reference for normal shutdown:

```
NORMAL SHUTDOWN — UH-1H

After landing:
1. COLLECTIVE .............. Full down (aircraft on ground)
2. THROTTLE ................ Idle (2-minute cooldown)
3. TRANSPONDER ............. OFF
4. RADIOS .................. OFF (after shutdown call)
5. NAV EQUIPMENT ........... OFF (ADF, VOR)

After 2-minute cooldown:
6. THROTTLE ................ CUTOFF (past idle detent)
7. EGT ..................... MONITOR decreasing
8. Nr / N1 ................. MONITOR decreasing
9. WAIT FOR ROTOR STOP ..... Do not exit until rotor stops

After rotor stop:
10. FUEL VALVE .............. OFF
11. GENERATOR ............... OFF
12. BATTERY ................. OFF
13. ALL SWITCHES ............ OFF (verify all panels)

Post-shutdown:
14. Walk-around inspection
15. Document discrepancies
16. Secure aircraft (tiedowns, covers) if required
```

---

### Instructor Notes — Module 10

| Common Student Error | Correction |
|---|---|
| **Skipping the cooldown period** | "Two minutes at idle — minimum. The turbine needs to cool gradually. Shutting down hot will cost an engine overhaul." Enforce this every shutdown |
| **Turning off the battery before the engine has fully spooled down** | "Wait for the rotor to stop and N1 to reach zero before de-energizing. There is no rush." |
| **Exiting the aircraft before the rotor stops** | "The rotor is invisible when spinning slowly. People have been killed walking into a still-spinning rotor. Wait for full stop." Enforce a strict 'remain seated until rotor stops' policy |
| **Forgetting to close the fuel valve** | "Fuel valve OFF is part of the shutdown. A leaking fuel line with an open fuel valve can create a fire hazard on a parked aircraft." |
| **Not performing a post-shutdown walk-around** | "Every flight ends with a walk-around. You may find damage that occurred during the flight that you didn't notice from the cockpit." |
| **Leaving switches on after shutdown** | "Everything OFF. If a maintainer comes to work on the aircraft and the battery switch is on, or a magneto or generator switch is on, it creates a safety hazard." |

---

## Appendix: DCS UH-1H Key Binds — Quick Reference

The following table provides the most commonly used key binds for the DCS UH-1H module. These are the **default** key assignments and may vary if the user has customized their controls.

| Function | Default Key Bind | Category |
|---|---|---|
| **Engine start** | `LShift + Home` | Engine |
| **Engine stop** | `LShift + End` | Engine |
| **Throttle increase** | `PgUp` | Engine |
| **Throttle decrease** | `PgDn` | Engine |
| **Governor ON/OFF** | `LCtrl + Home` | Engine |
| **Idle stop release** | `LShift + PgDn` | Engine |
| **Battery** | `LShift + B` | Electrical |
| **Generator** | `LShift + G` | Electrical |
| **Inverter** | `LShift + I` | Electrical |
| **Fuel valve** | `LShift + F` | Fuel |
| **Fuel boost pump** | `LCtrl + B` | Fuel |
| **Landing light** | `LCtrl + L` | Lighting |
| **Nav lights** | `LShift + L` | Lighting |
| **Pitot heat** | `LShift + P` | Anti-ice |
| **Force trim** | `LCtrl + T` | Flight controls |
| **Force trim release** | `T` | Flight controls |

**Note:** For full key bind reference, consult the DCS UH-1H module options in the game settings. Many functions require mouse clickable cockpit interaction rather than keyboard shortcuts.

---

*This research dossier is based on TM 55-1520-210-10, TM 55-1520-210-CL, TC 3-04.4, FM 1-240, AR 95-1, and the Eagle Dynamics DCS: UH-1H Huey module documentation. For simulation training use only.*
