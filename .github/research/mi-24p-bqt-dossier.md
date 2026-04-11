# Research Dossier: Mi-24P Hind — Basic Qualification Training (BQT)

> **Module:** DCS Mi-24P Hind (Eagle Dynamics — Full Fidelity, Dual-Seat Clickable Cockpit)
> **Course Type:** Basic Qualification Training — Cold-Dark to Safe Recovery
> **Scope Exclusion:** Weapons employment (ATGM, rockets, cannon, AAM) is out of scope. Basic familiarization with weapons panel, PKV sight, and SPO-15 RWR is included.

---

## Source Material & Prioritization

| Priority | Source | Usage |
|----------|--------|-------|
| **Primary** | *Mi-24P RLE (Rukovodstvo po Letnoy Ekspluatatsii)* — Flight Manual | Systems, limitations, normal/emergency procedures |
| **Primary** | *Mi-24P Technical Description & Operating Instructions (Tekhnicheskoye Opisaniye)* | Detailed system architecture, servicing limits |
| **Primary** | Soviet/Russian helicopter aerodynamics manuals | Rotary-wing theory, Mi-24 family flight characteristics |
| **Primary** | Translated Soviet Air Force / AA VVS training circulars | Training standards, crew coordination doctrine |
| **Secondary** | Western intelligence assessments (NATO, DIA) | Gap-fill where original Soviet docs unavailable |
| **Override** | DCS Mi-24P module (Eagle Dynamics) | Where DCS behavior diverges from real-world, DCS is what the student flies |

> **Rule:** Real-world Soviet/Russian documentation is the primary truth for systems knowledge and procedural depth. Where DCS diverges (simplified APU, compressed alignment, absent circuit breakers, single-player crew-switching mechanics), the DCS procedure is taught as the primary instruction. All divergences are footnoted with `⚠ Realism Divergence`.

---

## Aircraft & Module Overview

| Attribute | Value |
|-----------|-------|
| **Designation** | Mil Mi-24P (NATO: Hind-F) |
| **Role** | Heavy attack / gunship helicopter with troop transport capability |
| **Crew** | 2 — Pilot (rear cockpit), Weapons Systems Officer (front cockpit) |
| **Engines** | 2 × Klimov TV3-117V turboshaft (~2,200 SHP each) |
| **Main Rotor** | 5-blade, fully articulated, 17.3 m (56.75 ft) diameter |
| **Tail Rotor** | 3-blade, right-side pusher configuration |
| **Stub Wings** | Fixed wings with 4.5 m² area, ~12° negative incidence; offload rotor by ~25% at cruise |
| **Landing Gear** | Retractable tricycle (nosewheel steering, toe brakes) |
| **MTOW** | 11,500 kg (25,353 lbs) |
| **VNE** | 300 km/h (162 kts) |
| **Cruise Speed** | 220–260 km/h (119–140 kts) |
| **Best Range Speed** | 220 km/h (119 kts) |
| **Autorotation Speed** | 170 km/h (92 kts) |
| **Rotor RPM (Normal)** | 95% (operating range 92–98%) |
| **Internal Fuel** | ~1,500 kg (~2,000 L) |
| **Fixed Armament** | GSh-30K twin-barrel 30 mm cannon (starboard fuselage mount, fixed forward) |
| **DCS Developer** | Eagle Dynamics (native module) |
| **Cockpit** | Full-fidelity, dual-seat, all switches clickable in both cockpits |
| **Units Convention** | Soviet metric — km/h, meters, °C, kg (conversions provided) |

### Key Character Traits for the Student

1. **The Mi-24P is not a hover platform.** At 11,000+ kg, it demands enormous power to hover. OGE hover may be impossible at high gross weight. Minimize hover time — the Hind wants to fly fast.
2. **Stub wings change the aerodynamics.** Wings generate ~25% of total lift at cruise, improving performance and range. But they increase drag at low speed and increase autorotation descent rate.
3. **Twin engines = survivability.** Single-engine flight is possible (with limitations). This is not "autorotate immediately" — it's "identify, secure, single-engine procedures."
4. **Wheeled landing gear = ground resonance risk.** The articulated rotor + tricycle gear combination makes ground resonance a critical emergency to understand.
5. **Two-crew aircraft.** Even in DCS single-player (seat switch: `1` WSO front / `2` Pilot rear), the student must understand the division of labor.
6. **Fixed cannon = pilot aims the aircraft.** The GSh-30K is fixed to the starboard fuselage. The pilot is the gunner for fixed weapons.

---

## Table of Contents

1. [Module 1 — Aircraft Systems & Aerodynamics](#module-1--aircraft-systems--aerodynamics)
2. [Module 2 — Cockpit Familiarization](#module-2--cockpit-familiarization)
3. [Module 3 — Ground Operations](#module-3--ground-operations)
4. [Module 4 — Hover & Takeoff](#module-4--hover--takeoff)
5. [Module 5 — Basic Flight Maneuvers](#module-5--basic-flight-maneuvers)
6. [Module 6 — Navigation (DISS-15 / ARK-15 / RSBN)](#module-6--navigation-diss-15--ark-15--rsbn)
7. [Module 7 — Emergency Procedures](#module-7--emergency-procedures)
8. [Module 8 — Approach & Landing](#module-8--approach--landing)
9. [Module 9 — Shutdown](#module-9--shutdown)
10. [Appendices](#appendices)

---

## Module 1 — Aircraft Systems & Aerodynamics

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Describe the TV3-117V turboshaft engine start cycle, normal operating parameters, and limitations.
2. Explain the function and operating limits of the main rotor, tail rotor, and transmission system.
3. Describe the role of the stub wings in forward flight and their effect on hover, autorotation, and cruise performance.
4. Identify the fuel system components, capacity, cross-feed operation, and low-fuel warnings.
5. Describe the main and backup hydraulic systems, what each powers, and the consequences of failure.
6. Explain the electrical system architecture including generators, batteries, APU generator, and bus configuration.
7. Describe the AI-9V APU function, start procedure, and limitations.
8. Explain the flight control system including hydraulic boost, force trim, and mechanical mixing.
9. Describe the autopilot channels (roll, pitch, heading, altitude) and their engagement/disengagement.
10. Identify key rotary-wing aerodynamic phenomena specific to the Mi-24P (ETL, LTE, settling with power, ground resonance, retreating blade stall, ground effect).

---

### 1.1 Powerplant — TV3-117V Turboshaft (×2)

The Mi-24P is powered by two Klimov TV3-117V turboshaft engines, each producing approximately 2,200 SHP (1,640 kW) at takeoff power. The engines are mounted side-by-side above the cabin, feeding power through a combining gearbox (VR-24) to the main transmission.

#### Engine Parameters & Limitations

| Parameter | Normal | Transient (max 30 sec) | Starting Limit | Emergency |
|-----------|--------|----------------------|----------------|-----------|
| **TIT (Turbine Inlet Temp)** | ≤ 800°C | ≤ 870°C (30 sec) | ≤ 830°C (start cycle) | ≤ 900°C (15 sec, single-engine) |
| **Ng (Gas Generator RPM)** | 88–97% | ≤ 100% (30 sec) | — | ≤ 101% (15 sec) |
| **Nf (Free Turbine / Power Turbine RPM)** | 95 ± 2% | 100% | — | — |
| **Oil Pressure** | 3.0–4.5 kgf/cm² | — | — | Min 2.0 kgf/cm² |
| **Oil Temperature** | 70–130°C | ≤ 150°C (10 min) | — | — |
| **Fuel Flow (per engine, cruise)** | ~400–500 kg/h | — | — | — |

#### Engine Start Cycle

1. **APU-assisted start (normal):** The AI-9V APU provides bleed air to spin the gas generator and electrical power for the starter. Throttle at IDLE detent → press Engine Start button → monitor Ng rise → TIT rise (abort if TIT exceeds 830°C) → Ng stabilizes at ~63–65% at ground idle.
2. **Cross-bleed start:** If APU is unavailable, the running engine provides bleed air to start the second engine. Requires the first engine at or above ground idle.
3. **Spool-up characteristics:** The TV3-117V has moderate spool-up lag (~4–5 seconds from idle to takeoff power). Students must anticipate power demand — particularly critical during go-arounds and single-engine emergencies.
4. **Idle behavior:** Ground idle Ng ~63–65%. Flight idle is engaged by advancing throttles to the FLY detent; Nr governing activates to maintain 95%.
5. **Emergency shutdown:** Throttle to STOP (past IDLE detent) cuts fuel. Fire handles/extinguisher bottles are separate.

> *⚠ Realism Divergence: The DCS Mi-24P engine model closely follows real-world parameters, but the AI-9V APU start is somewhat simplified — real-world APU start requires a specific battery voltage threshold and multiple cockpit checks not all modeled in DCS. The cross-bleed start procedure is functional in DCS.*

---

### 1.2 Rotor System

#### Main Rotor

| Parameter | Value |
|-----------|-------|
| **Type** | 5-blade, fully articulated |
| **Diameter** | 17.3 m (56.75 ft) |
| **Rotation** | Counter-clockwise (viewed from above) |
| **Normal Nr** | 95% (operating range 92–98%) |
| **Min Nr (Caution)** | < 92% |
| **Max Nr (Caution)** | > 98% |
| **Autorotation Nr Range** | 92–110% (target 95–98% for best control) |
| **Lead-Lag Dampers** | Hydraulic, each blade — critical for ground resonance prevention |

The 5-blade articulated head has flap, lead-lag, and feathering hinges on each blade. Lead-lag dampers are hydraulic and prevent ground resonance — if a damper fails, ground resonance risk increases dramatically.

#### Tail Rotor

| Parameter | Value |
|-----------|-------|
| **Type** | 3-blade, pusher configuration |
| **Location** | Right side of vertical stabilizer |
| **Rotation** | Provides thrust to the right (counteracts main rotor torque) |
| **Drive** | Via intermediate and tail rotor gearboxes |

The pusher tail rotor on the right side means that torque compensation dynamics differ from U.S. helicopters with left-side tail rotors. The critical LTE wind azimuths are rotated accordingly (see Section 1.11).

> *⚠ Realism Divergence: DCS models the tail rotor authority and LTE dynamics, but the specific onset characteristics may differ slightly from real-world documentation. The tail rotor is fully functional and failure modes are modeled.*

---

### 1.3 Transmission System

| Component | Function | Limits |
|-----------|----------|--------|
| **VR-24 Main Gearbox** | Combines power from both engines, drives main rotor | Oil temp ≤ 100°C (normal), ≤ 110°C (max); Oil pressure 3.5–5.5 kgf/cm² |
| **Intermediate Gearbox** | Redirects drive shaft from engines to tail rotor | Oil temp ≤ 100°C; chip detector monitored |
| **Tail Rotor Gearbox** | Final drive to tail rotor | Oil temp ≤ 100°C |
| **Combining Gearbox** | Merges output of both engines before main gearbox | Integral to engine installation |

**Torque Limits:**

| Regime | Torque (%) | Duration |
|--------|-----------|----------|
| Continuous (both engines) | ≤ 85% | Unlimited |
| Transient (both engines) | ≤ 96% | ≤ 30 seconds |
| Single-engine max continuous | ≤ 93% (on operating engine) | Unlimited |
| Single-engine transient | ≤ 106% | ≤ 30 seconds |

Chip detectors are installed on the main, intermediate, and tail rotor gearboxes. A chip light indicates metal contamination — this is a **land as soon as practicable** condition.

---

### 1.4 Stub Wings

The Mi-24P features fixed stub wings with an area of approximately 4.5 m² and a negative incidence angle of ~12°.

| Aspect | Effect |
|--------|--------|
| **Lift generation** | At cruise (220–260 km/h), wings produce ~20–25% of total aircraft lift, offloading the main rotor |
| **Rotor offloading** | Reduces required rotor thrust at speed → lower torque demand → improved fuel efficiency and range |
| **Low-speed drag** | At hover and low speeds, wings produce only drag — no useful lift. This increases power required to hover |
| **Autorotation effect** | Wings increase descent rate in autorotation (more drag, fixed pitch = less efficient than a wingless helicopter) |
| **Weapon pylons** | 4 hardpoints (2 per wing) for rockets, ATGMs, bombs, AAMs |
| **Stability** | Wings improve longitudinal stability at speed, making the Hind more "airplane-like" at cruise |

**Key Insight:** The stub wings are the reason the Mi-24P "wants to fly fast." At cruise speeds, the wings improve efficiency. At hover, they are parasitic weight and drag. This fundamentally shapes operational technique — running takeoffs and running landings are preferred.

---

### 1.5 Fuel System

| Parameter | Value |
|-----------|-------|
| **Internal capacity** | ~1,500 kg (~2,000 L / ~528 US gal) |
| **Tank configuration** | Multiple internal tanks (fuselage and cabin area), self-sealing |
| **Fuel type** | TS-1 kerosene (Jet-A equivalent) |
| **Boost pumps** | Electric, one per engine feed line |
| **Cross-feed** | Valve allows either engine to draw from any tank |
| **Low fuel warning** | Amber caution at ~300 kg remaining |
| **Fuel flow (cruise, both engines)** | ~800–1,000 kg/h total |
| **Fuel flow (hover, both engines)** | ~1,200–1,400 kg/h total |
| **Endurance (cruise, internal fuel)** | ~1.5–2 hours depending on load/altitude |
| **External tanks** | Optional; mounted on wing pylons (displaces weapons) |

**Fuel Management Notes:**
- Cross-feed is critical for single-engine operations — ensure the operating engine can access all fuel.
- Fuel consumption in hover is ~30–40% higher than cruise due to the enormous power demand.
- Low fuel warning at 300 kg gives approximately 15–20 minutes at cruise, significantly less in hover.

> *⚠ Realism Divergence: DCS models the fuel system with functional boost pumps, cross-feed valve, and fuel quantity indication. External ferry tanks may not be fully modeled depending on DCS version. Self-sealing tank behavior under combat damage is simplified.*

---

### 1.6 Hydraulic System

| System | Powers | Pressure |
|--------|--------|----------|
| **Main hydraulic** | Flight controls (cyclic, collective, pedals), landing gear actuation, wheel brakes, nosewheel steering | 65 ± 5 kgf/cm² |
| **Backup hydraulic** | Flight controls only (emergency backup) | 65 ± 5 kgf/cm² |
| **Emergency pump** | Electric, provides backup pressure if both engine-driven pumps fail | Activates automatically or manually |

**Hydraulic Failure Consequences:**
- **Main system failure:** Backup system maintains flight control authority. Landing gear may require emergency extension (gravity/pneumatic).
- **Backup system failure:** Main system continues normal operation. Reduced redundancy — land as soon as practicable.
- **Dual failure:** Controls become extremely heavy (irreversible system without hydraulic boost). Flight is possible but demands enormous physical effort. Reduce speed below 150 km/h. **Land immediately.**

---

### 1.7 Electrical System

| Component | Function |
|-----------|----------|
| **DC Generators (×2)** | One per engine, 28.5V DC, primary power source |
| **Batteries (×2)** | 24V, backup power, engine start assist |
| **AC Inverters** | Convert DC to AC for instruments and avionics |
| **APU Generator** | Provides ground power during startup before engines running |
| **Essential Bus** | Fed by battery — instruments, fire detection, emergency comms |
| **Non-Essential Bus** | Shed-able loads — most avionics, lighting, comfort systems |

**Battery Endurance:** Approximately 20–30 minutes on batteries alone (essential bus only). Sufficient for emergency approach and landing.

**Generator Failure:**
- Single generator loss: remaining generator powers both buses via bus tie. Monitor load — shed non-essential equipment if needed.
- Dual generator loss: battery power only. Essential bus keeps critical instruments and one radio. **Land immediately.**

---

### 1.8 APU — AI-9V Auxiliary Power Unit

| Parameter | Value |
|-----------|-------|
| **Type** | AI-9V gas turbine APU |
| **Function** | Bleed air for engine start, electrical power via APU generator |
| **Start source** | Battery power |
| **RPM indication** | APU RPM gauge (Pilot — Left console) |
| **Auto-shutdown** | Over-temperature, over-speed, oil pressure loss |
| **Ground use only** | APU typically shut down after engines are running; in-flight restart may be possible in emergency |

**Start Procedure:**
1. Battery ON → verify battery voltage sufficient.
2. APU switch to START → monitor RPM gauge → stabilize at operating RPM.
3. APU generator switch ON → verify power on bus.
4. Proceed with engine start.
5. After both engines running and generators online → APU generator OFF → APU switch OFF.

> *⚠ Realism Divergence: DCS simplifies the APU start — real-world APU requires battery voltage above a minimum threshold and has a more complex start monitoring sequence. In DCS, the APU starts reliably with battery switch ON.*

---

### 1.9 Flight Control System

The Mi-24P uses a **fully hydraulic, irreversible** flight control system. The pilot inputs commands through mechanical linkages that position hydraulic servo actuators — there is no direct mechanical connection to the rotor.

| Feature | Description |
|---------|-------------|
| **Control type** | Irreversible hydraulic boost (pilot moves valves, hydraulics move controls) |
| **Force trim** | Electromagnetic clutch — holds control position, pilot can override by pressing trim release |
| **Mechanical mixing** | Collective-to-yaw (reduces pedal workload) and collective-to-cyclic (reduces pitch change with power) |
| **Control limits** | Collective: 0–100% travel; Cyclic: full deflection F/A and L/R; Pedals: full travel |
| **SAS** | No separate SAS — the autopilot provides stability augmentation |
| **Trim release** | Button on cyclic grip — releases force trim, allows re-centering |

**Key Point:** Because controls are irreversible, a hydraulic failure results in **extremely heavy or impossible** control forces. The backup hydraulic system exists precisely for this reason.

---

### 1.10 Autopilot System

The Mi-24P autopilot provides multi-channel stabilization:

| Channel | Function | Engagement |
|---------|----------|------------|
| **Roll** | Maintains bank angle, wings-level in coordinated flight | Individual switch on autopilot panel |
| **Pitch** | Maintains pitch attitude | Individual switch |
| **Heading** | Maintains magnetic heading | Individual switch |
| **Altitude** | Maintains barometric altitude (coarse) or radar altitude (fine) | Individual switch; requires radar altimeter for radar alt hold |
| **Flight Director** | Provides steering commands for navigation/approach | Coupled with navigation system |

**Engagement/Disengagement:**
- Engage channels individually on the autopilot panel (Pilot — Right console or instrument panel).
- **Trim must be centered/synchronized before engagement** — engaging autopilot with large trim offsets causes a jolt.
- Disengage by pressing the autopilot disconnect button on the cyclic or switching channels off on the panel.
- After disconnect, the aircraft will hold the last trim state — re-trim immediately.

**Autopilot Limitations:**
- Autopilot authority is limited — it cannot recover from extreme attitudes.
- Overriding autopilot (pushing through it) is possible by applying force past the autopilot servo limit.
- Autopilot should be OFF for hover, takeoff, and landing (it is designed for stabilized forward flight).

> *⚠ Realism Divergence: DCS implements all four autopilot channels. The radar altitude hold mode may have slightly different hold accuracy than real-world. Flight director coupling to navigation depends on navigation system setup.*

---

### 1.11 Survivability Features

| Feature | Description |
|---------|-------------|
| **Armored cockpits** | Both crew compartments have armor plating (steel and titanium), withstanding 12.7mm rounds from most angles |
| **Armored windscreens** | Flat-panel bulletproof glass in both cockpits |
| **Self-sealing fuel cells** | Internal tanks seal automatically after small-arms penetration |
| **IR suppressor** | Exhaust mixer reduces thermal signature (fitted on most variants) |
| **Redundant hydraulics** | Main + backup systems; dual generators; twin engines |
| **Crash-resistant gear** | Tricycle landing gear designed to absorb vertical loads in hard/emergency landings |
| **Cargo compartment** | Can carry 8 troops or cargo; rear clamshell doors |

---

### 1.12 Rotary-Wing Aerodynamics — Mi-24P Specifics

#### Translating Tendency
In hover, the tail rotor (right-side pusher) produces a lateral thrust to the right to counteract main rotor torque. This causes the aircraft to drift right. The pilot compensates with a slight left cyclic input. The Mi-24P's high weight makes this effect pronounced.

#### Translational Lift (ETL)
As the helicopter accelerates through approximately **50 km/h (27 kts)**, the rotor moves into undisturbed air, dramatically increasing lift efficiency. Indications include:
- Nose pitch-up tendency (rotor flaps back).
- Reduced power required for the same altitude.
- Vibration reduction as the rotor enters clean air.

The Mi-24P's ETL transition is influenced by the stub wings beginning to generate lift simultaneously. The combined effect makes the transition particularly noticeable — the aircraft "comes alive" at ETL.

#### Transverse Flow Effect
During the transition through 25–50 km/h, the rear portion of the rotor disc receives a more vertical airflow than the front. This creates a lateral vibration and a tendency to roll. Corrected with cyclic input. Transient effect — it passes once through ETL.

#### Retreating Blade Stall
The VNE of 300 km/h (162 kts) exists primarily because of retreating blade stall. As forward speed increases, the retreating blade sees progressively lower relative wind, requiring higher angles of attack to maintain lift. At VNE, the retreating blade stalls, causing:
- Vibration (typically 2/rev at stall onset, progressing to 5/rev).
- Pitch-up tendency.
- Roll toward the retreating side.

**Recovery:** Reduce airspeed, lower collective, reduce bank angle/G loading.

#### Dissymmetry of Lift & Flapping
The advancing blade generates more lift than the retreating blade at any forward speed. The articulated rotor head allows blades to flap up (advancing side) and down (retreating side) to equalize lift. This is an inherent design feature — no pilot action required. However, it produces a nose-up pitching moment ("blowback") with increasing airspeed.

#### Ground Effect vs. Out-of-Ground-Effect (IGE vs. OGE)

| Condition | Performance Impact |
|-----------|-------------------|
| **IGE hover** (< ½ rotor diameter AGL, ~8.5 m) | Reduced power required (~10–15% less torque than OGE); induced velocity is partially blocked by ground |
| **OGE hover** (> 1 rotor diameter AGL) | Full induced power penalty; may **not be achievable** at MTOW in hot/high conditions |

**Critical Point:** At high gross weight (>10,500 kg), particularly on hot days or at altitude, the Mi-24P may not have sufficient power for OGE hover. **The pilot must verify power available vs. power required before attempting to hover.** This is a go/no-go decision.

#### Settling with Power (Vortex Ring State)

| Factor | Threshold |
|--------|-----------|
| **Conditions** | Airspeed < 50 km/h, descent rate > 5 m/s, high power applied |
| **Recognition** | High rate of descent despite power increase; vibration; loss of collective effectiveness; uncommanded roll/yaw |
| **Recovery** | Cyclic forward → gain airspeed above 50 km/h → collective adjust. Altitude loss will occur |

The Mi-24P's high disc loading (~50 kg/m²) makes it more susceptible to vortex ring state than lighter helicopters. The rate of descent threshold is lower, and recovery requires more altitude.

#### Loss of Tail Rotor Effectiveness (LTE)

The Mi-24P's **right-side pusher** tail rotor creates specific vulnerable wind azimuths:

| Wind Azimuth (relative to nose) | Effect | Risk |
|----------------------------------|--------|------|
| **Left quartering tailwind (210–330°)** | Main rotor vortex interference with tail rotor | Moderate — reduced tail rotor efficiency |
| **Direct tailwind (150–210°)** | Tail rotor operates in disturbed air from fuselage/rotor wake | High — sudden yaw authority loss |
| **Right quartering headwind (280–330°)** | Weathercock effect opposes tail rotor authority | Moderate — yaw divergence |

**Recognition:** Uncommanded yaw (typically nose-right for the Mi-24P), increasing pedal input required without effect.
**Recovery:** Apply full opposite pedal → cyclic forward to gain airspeed → as airspeed increases, vertical stabilizer provides directional stability and tail rotor regains effectiveness.

> *⚠ Realism Divergence: DCS models LTE dynamics for the Mi-24P. The specific onset speed and wind azimuths may vary slightly from published RLE figures. Students should practice LTE recognition in controlled DCS scenarios.*

#### Mast Bumping
The fully articulated rotor head on the Mi-24P is less susceptible to mast bumping than semi-rigid (teetering) rotor systems. However, at very low or negative G (pushover maneuvers, turbulence), the rotor hub can still contact the mast. This is a **catastrophic, non-recoverable** event.

**Prevention:** Avoid low-G and negative-G maneuvers. Limit pushovers. In turbulence, maintain positive G. The +3.5 G / −0.5 G limits exist partly for this reason.

#### Dynamic Rollover
Applicable during ground operations when one wheel is "anchored" (stuck in soft ground, on a curb, or during slope operations). If the helicopter begins to roll around the contact point, the rolling moment may exceed the pilot's ability to correct.

**Prevention:** Smooth collective inputs during takeoff and landing. Avoid lateral drift on the ground. On slopes, land uphill and depart downhill. If rollover begins — lower collective immediately.

#### Ground Resonance

**This is the most critical ground emergency for the Mi-24P.**

Ground resonance occurs when the oscillation frequency of the lead-lag motion of the articulated rotor blades couples with the natural frequency of the airframe on its landing gear. It can destroy the aircraft in seconds.

| Factor | Detail |
|--------|--------|
| **Conditions** | Wheeled landing gear on hard surface + articulated rotor + imbalance trigger (blade damper failure, unequal tire pressure, hard landing, one gear not fully extended) |
| **Recognition** | Rapid, violent oscillation building in intensity — the aircraft shakes aggressively, progressing to airframe-destructive levels within 3–5 seconds |
| **Immediate Action (Nr sufficient)** | **Full collective UP — get airborne immediately.** Breaking ground contact stops the coupling. |
| **Immediate Action (Nr insufficient)** | **Throttles to OFF — rotor brake ON — emergency shutdown.** Cannot fly, must stop the rotor. |
| **Time available** | 3–5 seconds from onset to structural failure. **This is the fastest-developing helicopter emergency.** |

> *⚠ Realism Divergence: DCS models ground resonance to a degree. The onset conditions and severity may be less dramatic than real-world, but the emergency is achievable in DCS and students should practice recognition and immediate action.*

---

### Module 1 — Key Data Summary Table

| Parameter | Normal Range | Caution | Warning/Limit |
|-----------|-------------|---------|---------------|
| **Nr (Rotor RPM)** | 95% | < 92% or > 98% | < 88% (autorotation min) / > 104% |
| **TIT (per engine)** | ≤ 800°C | 800–830°C (start only) | > 870°C transient / > 900°C emergency |
| **Ng (Gas Generator)** | 88–97% | > 97% sustained | > 100% transient / > 101% emergency |
| **Torque (both engines)** | ≤ 85% | 85–96% (transient) | > 96% |
| **Torque (single engine)** | ≤ 93% | 93–106% (transient) | > 106% |
| **Main GB Oil Temp** | ≤ 100°C | 100–110°C | > 110°C |
| **Main GB Oil Pressure** | 3.5–5.5 kgf/cm² | < 3.5 | < 2.5 |
| **Engine Oil Pressure** | 3.0–4.5 kgf/cm² | < 3.0 | < 2.0 |
| **Engine Oil Temp** | 70–130°C | 130–150°C | > 150°C |
| **Hydraulic Pressure** | 65 ± 5 kgf/cm² | < 55 | < 45 |
| **VNE** | — | — | 300 km/h (162 kts) |
| **G Limits** | +1.0 to +2.5 | +2.5 to +3.5 | > +3.5 or < −0.5 |
| **Max Sideward** | — | — | 50 km/h |
| **Max Rearward** | — | — | 40 km/h |
| **Crosswind (T/O & Landing)** | — | — | 12 m/s (23 kts) |

---

### Module 1 — Instructor Notes / Common Student Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Attempting OGE hover at high gross weight on a hot day | Torque exceeds limits or insufficient power → settling | Perform power check IGE before attempting OGE. If torque ≥ 90% IGE, do not attempt OGE hover |
| Ignoring TIT during engine start | Hot start → engine damage | Eyes on TIT gauge from moment of start initiation. Abort at 830°C |
| Failing to understand wing effect at low speed | Expects helicopter to hover like a UH-1 → frustrated by power demand | Brief the student: "This aircraft wants to fly at 200+ km/h. Hover is a transient state, not the operating regime" |
| Not recognizing ground resonance onset | Destruction of aircraft within seconds | Brief extensively. Practice recognition. Drill: "Vibration on ground → immediate collective UP or immediate shutdown" |
| Exceeding VNE in a dive | Retreating blade stall → loss of control | Brief VNE as an absolute limit. Set the lesson: bank and speed together increase stall risk on the retreating blade |
| Misunderstanding single-engine capability | Assumes dual engine failure procedures when only one fails | Emphasize: twin-engine helicopter can fly on one engine. Identify → secure → fly. Not "autorotate immediately" |

---

## Module 2 — Cockpit Familiarization

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Locate and identify all primary panels and instruments in the **Pilot (rear) cockpit**.
2. Locate and identify key panels and instruments in the **WSO (front) cockpit**.
3. Describe the function of each flight instrument and engine gauge, including normal indications.
4. Identify the caution/advisory panel indicators and their meanings.
5. Demonstrate DCS seat-switching between Pilot and WSO positions.
6. Locate and describe (at familiarization level) the weapons panel, PKV sight, SPO-15 RWR, and UV-26 countermeasures panel.
7. Operate cockpit lighting controls for day and night operations.
8. Identify collective, cyclic, and pedal controls and their associated HOTAS functions.

---

### 2.1 Rear Cockpit — Pilot Station

The Pilot occupies the **rear (upper) cockpit** and is the default spawn position in DCS single-player. This is the primary flying station — all flight controls, engine management, and aircraft systems are controlled from here.

#### Instrument Panel (Main Panel — Pilot)

```
┌─────────────────────────────────────────────────────────────────┐
│                         PILOT INSTRUMENT PANEL                    │
│                                                                   │
│  ┌─────┐  ┌─────┐  ┌─────┐  ┌─────┐  ┌─────┐  ┌─────┐         │
│  │ ADI │  │ HSI │  │ ASI │  │ ALT │  │ VSI │  │ SLIP│         │
│  │     │  │     │  │km/h │  │  m  │  │ m/s │  │BALL │         │
│  └─────┘  └─────┘  └─────┘  └─────┘  └─────┘  └─────┘         │
│                                                                   │
│  ┌─────┐  ┌─────┐  ┌─────┐  ┌─────┐  ┌─────┐  ┌─────┐         │
│  │TIT L│  │TIT R│  │Ng L │  │Ng R │  │Nf/Nr│  │ TRQ │         │
│  │ °C  │  │ °C  │  │  %  │  │  %  │  │  %  │  │  %  │         │
│  └─────┘  └─────┘  └─────┘  └─────┘  └─────┘  └─────┘         │
│                                                                   │
│  ┌─────┐  ┌─────┐  ┌──────────────┐  ┌─────────────────┐       │
│  │FUEL │  │FUEL │  │  RADAR ALT   │  │  CAUTION/WARN   │       │
│  │QTY  │  │FLOW │  │   (A-037)    │  │     PANEL       │       │
│  └─────┘  └─────┘  └──────────────┘  └─────────────────┘       │
└─────────────────────────────────────────────────────────────────┘
```

| Instrument | Location | Unit | Normal Reading | Notes |
|------------|----------|------|----------------|-------|
| **ADI (Attitude Director Indicator)** | Center-left | Degrees pitch/roll | Wings level, horizon centered | Primary attitude reference; flight director bars when coupled |
| **HSI (Horizontal Situation Indicator)** | Below ADI | Degrees magnetic | Current heading, course pointer | Bearing to waypoint/NDB, CDI needle |
| **Airspeed Indicator (ASI)** | Left of ADI | **km/h** | 0 (ground) / 220–260 (cruise) | Soviet dial reads km/h, not knots |
| **Barometric Altimeter** | Right of ADI | **meters** | Field elevation | Set QFE (field pressure) or QNH (sea-level pressure) |
| **Vertical Speed Indicator (VSI)** | Right side | **m/s** | 0 (level) | Reads in meters per second, not feet per minute |
| **Slip Ball** | Below ADI / integrated | Centered = coordinated | Ball centered | Coordinated flight reference |
| **TIT Gauges (L/R)** | Engine cluster | °C | ≤ 800°C | Separate gauge per engine; primary overheat indicator |
| **Ng Gauges (L/R)** | Engine cluster | % | 88–97% | Gas generator RPM per engine |
| **Nf/Nr Gauge** | Engine cluster | % | 95% | Free turbine / rotor RPM (linked through transmission) |
| **Torque Gauge** | Engine cluster | % | ≤ 85% continuous | Combined or per-engine; primary power indicator |
| **Fuel Quantity** | Lower panel | **kg** | 1,500 (full) → 0 | Total fuel remaining |
| **Fuel Flow** | Lower panel | **kg/h** | 800–1,000 (cruise) | Total flow or per-engine |
| **Radar Altimeter (A-037)** | Lower center | **meters** | AGL reading | Setting ring for low-altitude warning; bug and audio alert |
| **Caution/Advisory Panel** | Right side | — | All dark (normal) | Master caution + individual caution/warning lights |

#### Left Console — Pilot

| Panel | Function | Key Switches |
|-------|----------|-------------|
| **Electrical Panel** | Battery, generators, APU generator, bus ties | Battery switch, Gen 1/Gen 2 switches, APU Gen switch |
| **Fuel Panel** | Boost pumps, cross-feed, fuel shutoff | Boost pump L/R, cross-feed valve, fuel shutoff L/R |
| **Engine Start Panel** | Engine start buttons, APU start, throttle idle stops | Start button L/R, APU switch, emergency fuel valve |
| **Lighting Panel** | Cockpit lights, instrument flood, NVG filter | Dimmer knobs (instruments, console, flood), NVG switch |

#### Right Console — Pilot

| Panel | Function | Key Switches |
|-------|----------|-------------|
| **Radio Panel — R-863** | UHF radio | Frequency selector, volume, preset/manual, transmit mode |
| **Radio Panel — R-828** | VHF/FM radio | Frequency selector, volume, preset/manual |
| **IFF Panel** | Transponder / SRO-2 IFF | Mode selector, code entry, master switch |
| **Navigation Panel** | RSBN, ARK-15, DISS-15 controls | Channel/frequency selectors, mode switches |
| **Autopilot Panel** | AP channel engagement | Roll, Pitch, Heading, Altitude channel switches; disconnect |

#### Overhead Panel — Pilot

| Panel | Function | Key Switches |
|-------|----------|-------------|
| **Circuit Breakers** | System protection | Individual CBs per system (many not functional in DCS) |
| **Anti-Ice** | Engine intake anti-ice, pitot heat | Engine anti-ice L/R, pitot heat switch |
| **Exterior Lights** | Navigation, anti-collision, landing light | Nav lights, beacon, landing/search light switches |
| **Rotor Brake** | Stops rotor during shutdown | Rotor brake lever (engage after Nr drops below ~40%) |
| **Ventilation** | Cockpit air | Fan/vent switches |

#### Caution/Advisory Panel — Pilot

| Light | Meaning | Response |
|-------|---------|----------|
| **MASTER CAUTION** (amber) | One or more caution conditions active | Identify specific caution light(s), take action |
| **FIRE L / FIRE R** (red) | Engine fire detected | Execute engine fire emergency procedure |
| **HYD MAIN** (amber) | Main hydraulic pressure low | Check backup; land as soon as practicable |
| **HYD BACKUP** (amber) | Backup hydraulic pressure low | Monitor main system; land as soon as practicable |
| **GEN 1 / GEN 2** (amber) | Generator offline | Check generator switch; bus tie; shed loads if needed |
| **FUEL LOW** (amber) | Fuel quantity below ~300 kg | Plan immediate landing |
| **CHIP DET** (amber) | Metal particles in gearbox oil | Land as soon as practicable; monitor temps/pressures |
| **GOV** (amber) | Governor malfunction | Monitor Nr manually; prepare for manual throttle |
| **AP DISC** (amber) | Autopilot disconnected | Verify intentional; re-engage or hand-fly |
| **ROTOR BRAKE** (amber) | Rotor brake engaged | Verify brake off before flight |
| **GEAR** (red/amber) | Landing gear not down and locked | Verify gear position; emergency extension if needed |

#### Fire Suppression Panel — Pilot

| Control | Function |
|---------|----------|
| **Fire Test** | Tests fire detection circuits for both engines |
| **Agent Select (1 / 2)** | Selects which fire extinguisher bottle to discharge |
| **Discharge Button** | Discharges selected agent into the selected engine compartment |
| **Engine Select (L / R)** | Selects which engine compartment receives the agent |

---

### 2.2 Center Pedestal / Throttle Quadrant — Pilot

| Control | Location | Function |
|---------|----------|----------|
| **Throttle Levers (×2)** | Center pedestal, side-by-side | Left throttle = Left engine, Right = Right engine. STOP → IDLE → FLY detent range |
| **Collective Friction** | Collective lever | Adjustable friction to hold collective position |
| **Trim Panel** | Near throttle quadrant | Force trim master, trim mode selector |
| **Parking Brake** | Lower pedestal | Engages/releases main wheel brakes |

---

### 2.3 Pilot Controls — Collective, Cyclic, Pedals

#### Collective Lever (Left Hand)

| Feature | Function |
|---------|----------|
| **Lever** | Controls main rotor blade pitch (up = more pitch = more lift = more power required) |
| **Throttle Twist Grips (×2)** | Integrated with collective; twist forward = increase RPM. In governor mode, typically left at FLY detent |
| **Radio Trigger** | PTT (Push-to-Talk) for selected radio |
| **Landing Light Switch** | Toggle landing/search light |
| **Collective-mounted switches** | May include additional functions (trim, HOTAS assignments) |

#### Cyclic Stick (Right Hand)

| Feature | Function |
|---------|----------|
| **Stick** | Controls main rotor disc tilt (forward/back = pitch, left/right = roll) |
| **Trim Release Button** | Releases force trim electromagnetic clutch; hold, reposition, release to set new trim |
| **Weapon Release / Trigger** | Fires selected weapon (cannon, rockets — pilot-fired weapons) |
| **Radio Trigger** | Secondary PTT |
| **HOTAS Assignments** | Additional buttons may be mapped to countermeasures, target designate, etc. |

#### Anti-Torque Pedals

| Feature | Function |
|---------|----------|
| **Pedals** | Control tail rotor blade pitch → yaw authority |
| **Toe Brakes** | Top of each pedal — differential or simultaneous wheel braking |
| **Nosewheel Steering** | Linked to pedals when on ground with weight on wheels — pedal input steers the nosewheel |

---

### 2.4 Front Cockpit — WSO Station

The Weapons Systems Officer (WSO) occupies the **front (lower) cockpit**. In DCS, switch to the WSO seat by pressing `1`.

#### Key Systems (Familiarization Level)

| System | Location | BQT Scope |
|--------|----------|-----------|
| **PKV-1 Sight** | Center instrument panel, WSO | **Familiarization only** — location, power-on switch, basic sight picture. Not used for weapons employment in BQT |
| **Weapons Panel** | Left console, WSO | **Identification only** — weapon select switches, master arm switch (ARM/SAFE), salvo/single selector. Student must know ARM/SAFE and verify SAFE during BQT |
| **ATGM Guidance Panel** | Right area, WSO | **Identification only** — Shturm/Ataka guidance controls, sight slew. Out of scope |
| **SPO-15 "Beryoza" RWR** | Upper instrument panel, WSO | **Familiarization** — display location, threat sector indication, audio tone meaning, basic threat awareness |
| **UV-26 Countermeasures** | Left/right console, WSO | **Familiarization** — chaff/flare dispenser controls, program selection, expendable count. Student should know how to set a program but not tactical employment |
| **Duplicate Flight Instruments** | Center panel, WSO | Backup ADI, altimeter, airspeed — WSO has basic flight reference. Less comprehensive than pilot panel |
| **Radio Controls** | Right console, WSO | WSO has independent access to R-863 and R-828 frequencies |

#### SPO-15 "Beryoza" RWR — Basic Orientation

The SPO-15 provides a **hemispherical threat display** showing the relative bearing sector of radar emitters. It does not provide range.

| Indication | Meaning |
|------------|---------|
| **Illuminated sector** | Radar emitter detected in that sector relative to aircraft nose |
| **Continuous tone** | Search radar tracking (CW or pulse) |
| **Rapid pulsing tone** | Missile guidance radar / lock-on |
| **Launch warning** | Distinct rapid tone indicating missile launch (if missile warning system active) |

The student should be able to identify that they are being tracked and from which general direction. Tactical response (maneuvering, countermeasures employment) is out of BQT scope.

---

### 2.5 Seat Switching in DCS

In DCS single-player, the Mi-24P allows switching between crew positions:

| Key | Position | Notes |
|-----|----------|-------|
| `1` | **Front cockpit (WSO)** | Weapons operator station; guided weapons, sensors |
| `2` | **Rear cockpit (Pilot)** | Flight controls, engines, navigation — **default spawn** |

**Important notes for seat switching:**
- Switching seats does **not** pause the simulation — the aircraft continues flying on its current course/autopilot state.
- **Engage autopilot before switching forward** — the aircraft will maintain attitude/altitude while you configure WSO systems.
- The AI crewmember in the unoccupied seat provides basic assistance (e.g., AI pilot will maintain flight if you are in WSO seat), but AI behavior is limited.
- Certain switches are only accessible from one seat — students must learn which actions require which cockpit.
- In multiplayer, each seat can be occupied by a human player — multi-crew procedures are the intended design.

> *⚠ Realism Divergence: Real-world Mi-24P operations always involve a two-person crew. The single-player seat-switching mechanic with AI crew is a DCS gameplay accommodation. AI crew behavior does not replicate a trained human crewmember.*

---

### 2.6 Lighting Controls

#### Cockpit Lighting — Pilot (Rear)

| Control | Location | Function |
|---------|----------|----------|
| **Instrument Lights** | Pilot — Left console — Lighting panel | Dimmer knob for instrument panel backlighting |
| **Console Lights** | Pilot — Left console — Lighting panel | Dimmer for left/right console illumination |
| **Flood Light** | Pilot — Left console — Lighting panel | Red or white flood light for overall cockpit illumination |
| **NVG Filter** | Pilot — Lighting panel | Switches cockpit lighting to NVG-compatible mode |

#### Cockpit Lighting — WSO (Front)

| Control | Location | Function |
|---------|----------|----------|
| **Instrument Lights** | WSO — Lighting panel | Independent dimmer for WSO instruments |
| **Sight Illumination** | WSO — PKV panel | PKV reticle brightness |

#### Exterior Lighting

| Light | Control Location | Function |
|-------|-----------------|----------|
| **Navigation Lights** | Pilot — Overhead panel | Position lights (red/green/white) for formation and identification |
| **Anti-Collision Beacon** | Pilot — Overhead panel | Rotating red beacon — indicates aircraft is operating |
| **Landing / Search Light** | Pilot — Collective or overhead panel | Retractable landing light for approach and hover |
| **Formation Lights** | Pilot — Overhead panel | Dim lights for close formation flying at night |

---

### Module 2 — Instructor Notes / Common Student Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Spawning and not knowing which cockpit they are in | Confusion, attempting to fly from WSO seat | Brief the student: default spawn is Pilot (rear, `2`). If you see the PKV sight, you are in the WSO seat — press `2` |
| Not engaging autopilot before switching to WSO seat | Aircraft enters uncontrolled flight | Drill: "Autopilot ON before switching seats — always" |
| Unable to locate engine instruments | Cannot monitor start or flight parameters | Walk through instrument panel layout in a cold-dark cockpit. Use cockpit labels |
| Confusing km/h and knots | Applying wrong speeds for procedures | Emphasize: "This is a Soviet aircraft. Your ASI reads km/h. VNE is 300 km/h, not 300 knots" |
| Confusing meters and feet for altitude | Dangerous altitude errors | Emphasize: "Your altimeter reads meters. 1,000 m ≈ 3,280 ft. Pattern altitude will be in meters" |
| Not knowing where caution lights are | Fails to respond to system warnings | Brief caution panel location and practice light test during startup |
| Leaving master arm in ARM during BQT | Inadvertent weapon release | Verify ARM/SAFE switch is in SAFE at start of every BQT sortie |

---

## Module 3 — Ground Operations

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Perform a complete cold-and-dark startup of the Mi-24P from battery ON through both engines running and avionics alive.
2. Execute the APU start sequence and describe APU function and limitations.
3. Start both engines (APU-assisted), monitoring TIT and Ng, and identify abort criteria.
4. Complete post-start checks including hydraulic, electrical, and generator verification.
5. Power on and configure the navigation system (DISS-15, ARK-15, RSBN) and radios (R-863, R-828).
6. Perform ground taxi using nosewheel steering and wheel brakes.
7. Complete the pre-takeoff checklist and verify power available.

---

### 3.1 Cold-and-Dark Startup — Full Procedure

The startup procedure is performed primarily from the **Pilot (rear) cockpit**. Some avionics initialization requires switching to the **WSO (front) cockpit**. Steps are listed with cockpit identified.

#### Phase 1: Electrical Power (Pilot — Left Console)

| Step | Action | Panel / Location | Indication |
|------|--------|-----------------|------------|
| 1 | **Parking Brake** — SET | Pilot — Lower pedestal | Brake lever locked |
| 2 | **Collective** — Full DOWN | Pilot — Left hand | Collective at bottom stop |
| 3 | **Throttles (both)** — IDLE detent | Pilot — Center pedestal | Both throttle levers at IDLE stop |
| 4 | **Battery 1** — ON | Pilot — Left console — Electrical panel | Battery voltage on voltmeter (~24V) |
| 5 | **Battery 2** — ON | Pilot — Left console — Electrical panel | Voltage confirmed |
| 6 | **Caution Panel** — CHECK | Pilot — Instrument panel | Multiple caution lights illuminate (expected with engines off) |
| 7 | **Warning Light Test** — PRESS and HOLD | Pilot — Instrument panel | All caution/warning lights illuminate; release — only power-related lights remain |

> **DCS Keyboard Alternative:** `RShift + L` toggles battery in some control configurations.

#### Phase 2: APU Start (Pilot — Left Console)

| Step | Action | Panel / Location | Indication |
|------|--------|-----------------|------------|
| 8 | **Fuel Boost Pumps** — ON (both) | Pilot — Left console — Fuel panel | Fuel pressure indication on gauge |
| 9 | **APU Start Button** — PRESS | Pilot — Left console — Engine start panel | APU RPM gauge begins rising |
| 10 | Wait for APU RPM to stabilize | — | APU RPM at operating range |
| 11 | **APU Generator** — ON | Pilot — Left console — Electrical panel | Electrical buses powered; additional caution lights may extinguish |

> *⚠ Realism Divergence: Real-world APU start requires battery voltage above a minimum threshold, has a time-limited start cycle, and includes exhaust monitoring. DCS simplifies the sequence — the APU starts reliably with batteries on.*

#### Phase 3: Left Engine Start (Pilot)

| Step | Action | Panel / Location | Indication |
|------|--------|-----------------|------------|
| 12 | **Left Throttle** — Confirm at IDLE detent | Pilot — Center pedestal | Throttle at IDLE stop |
| 13 | **Left Engine Start Button** — PRESS and HOLD until light-off | Pilot — Left console — Engine start panel | Ng begins rising; TIT begins rising |
| 14 | Monitor **Ng** rise | Pilot — Instrument panel — Ng L gauge | Ng increases steadily toward 63–65% |
| 15 | Monitor **TIT** — abort if > 830°C | Pilot — Instrument panel — TIT L gauge | TIT rises, peaks, then settles below 800°C |
| 16 | Wait for **Ng** to stabilize at ground idle (~63–65%) | — | Ng steady; TIT settling |
| 17 | Confirm **oil pressure** in range | Pilot — Instrument panel | 3.0–4.5 kgf/cm² |

**Start Abort Criteria:**

| Condition | Indication | Action |
|-----------|-----------|--------|
| **Hot start** | TIT exceeds 830°C and continues rising | Throttle to STOP immediately; allow engine to cool before re-attempt |
| **Hung start** | Ng stalls below 55% and does not increase | Throttle to STOP; cycle starter after 30-sec cool-down |
| **No light-off** | No TIT rise within 10 seconds of start | Release start button; throttle to STOP; verify fuel boost pumps ON |
| **Oil pressure fail** | No oil pressure within 30 seconds of idle | Throttle to STOP; do not continue |

> **DCS Keyboard Alternative:** `RAlt + Home` starts Left Engine in default keybinds.

#### Phase 4: Right Engine Start (Pilot)

| Step | Action | Indication |
|------|--------|------------|
| 18 | **Right Engine Start Button** — PRESS and HOLD | Ng R begins rising |
| 19 | Monitor Ng and TIT (same limits as left engine) | TIT ≤ 830°C; Ng → 63–65% |
| 20 | Wait for stabilization | Both engines at ground idle |
| 21 | Confirm both engines' oil pressures normal | 3.0–4.5 kgf/cm² each |

> **DCS Keyboard Alternative:** `RCtrl + Home` starts Right Engine in default keybinds.

#### Phase 5: Post-Start Checks (Pilot)

| Step | Action | Indication |
|------|--------|------------|
| 22 | **Left Generator** — ON | Pilot — Left console — Electrical panel | GEN 1 caution light extinguishes |
| 23 | **Right Generator** — ON | Pilot — Left console — Electrical panel | GEN 2 caution light extinguishes |
| 24 | **APU Generator** — OFF | Pilot — Left console — Electrical panel | APU no longer supplying power |
| 25 | **APU** — OFF | Pilot — Left console — Engine start panel | APU RPM drops to zero |
| 26 | **Hydraulic Pressure** — CHECK both systems | Pilot — Instrument panel | Main: 65 ± 5 kgf/cm²; Backup: 65 ± 5 kgf/cm² |
| 27 | **Flight Control Check** — Full cyclic, collective, pedal deflection | Pilot — Controls | Smooth, full travel, no binding |
| 28 | **Caution Panel** — CHECK | Pilot — Instrument panel | Only expected lights (gear-related if on ground) |

#### Phase 6: Avionics Power-On (Pilot + WSO)

| Step | Action | Cockpit | Notes |
|------|--------|---------|-------|
| 29 | **R-863 UHF Radio** — ON, set frequency | Pilot — Right console | Primary ATC/flight communications |
| 30 | **R-828 VHF/FM Radio** — ON, set frequency | Pilot — Right console | Backup / ground communications |
| 31 | **IFF/SRO-2** — STANDBY | Pilot — Right console | Transponder on but not interrogating |
| 32 | **ARK-15 ADF** — ON | Pilot — Right console — Nav panel | Tune to NDB if available |
| 33 | **RSBN** — ON, select channel | Pilot — Right console — Nav panel | Tune to ground beacon |
| 34 | **DISS-15 Doppler** — ON | Pilot — Right console — Nav panel | Warm-up required (~3–5 min) |
| 35 | **Radar Altimeter (A-037)** — ON, set warning altitude | Pilot — Instrument panel | Set bug to desired low-altitude warning |
| 36 | **Autopilot** — STANDBY (do not engage channels yet) | Pilot — Right console — AP panel | AP ready for engagement after takeoff |
| 37 | Switch to WSO cockpit (`1` key) | — | Configure WSO-specific systems |
| 38 | **SPO-15 RWR** — ON | WSO — Upper panel | RWR display illuminates, self-test |
| 39 | **UV-26 Countermeasures** — ON, program selected | WSO — CM panel | Expendable count displayed; program set |
| 40 | **PKV-1 Sight** — STANDBY (if familiarization desired) | WSO — Instrument panel | Sight warms up; not needed for BQT |
| 41 | **Weapon Master** — SAFE | WSO — Left console — Weapons panel | Verify SAFE for all BQT operations |
| 42 | Switch back to Pilot cockpit (`2` key) | — | Resume pilot duties |

> *⚠ Realism Divergence: Real-world avionics power-on includes warm-up times for gyroscopic instruments (ADI, HSI) of 3–5 minutes and inertial system alignment. DCS compresses these warm-up times. The DISS-15 Doppler warm-up is modeled but may be shorter than real-world.*

---

### 3.2 Navigation System Alignment / Warm-Up

| System | Warm-Up Time (DCS) | Warm-Up Time (Real-World) | Notes |
|--------|-------------------|--------------------------|-------|
| **DISS-15 Doppler** | ~2–3 minutes | ~5–10 minutes | Provides ground speed and drift. No output until warmed up |
| **ARK-15 ADF** | ~30 seconds | ~1–2 minutes | Ready when needle responds to NDB signal |
| **RSBN** | ~1 minute | ~3–5 minutes | Channel must be tuned to a functioning ground beacon |
| **Gyro Instruments** | ~1 minute | ~3–5 minutes | ADI and HSI need gyro spin-up for accurate attitude and heading |

> *⚠ Realism Divergence: DCS compresses all warm-up and alignment times significantly. Real-world Mi-24P ground time from cold-start to takeoff-ready is 10–15 minutes; in DCS, it is approximately 3–5 minutes.*

---

### 3.3 Autopilot Pre-Flight Check

| Step | Action | Indication |
|------|--------|------------|
| 1 | Verify all AP channel switches OFF | AP panel — all switches in OFF position |
| 2 | Press force trim release on cyclic, center stick | Trim is neutral |
| 3 | Engage Roll channel — verify no transient | Aircraft does not jolt or roll |
| 4 | Engage Pitch channel — verify no transient | Aircraft does not pitch |
| 5 | Disengage both channels | AP channels OFF |
| 6 | AP is confirmed functional — do not engage for takeoff | Ready for in-flight engagement |

---

### 3.4 Landing Gear & Ground Handling

#### Nosewheel Steering

| Aspect | Detail |
|--------|--------|
| **Engagement** | Automatic when weight is on wheels; pedals steer the nosewheel |
| **Authority** | ±45° (approximately) — sufficient for taxi turns |
| **Speed limit** | Taxi at ≤ 20 km/h on straight taxiway; ≤ 10 km/h in turns |
| **Linkage** | Directly linked to anti-torque pedals — pedal input = nosewheel steering on ground, yaw control in flight |

#### Wheel Brakes

| Control | Function |
|---------|----------|
| **Toe brakes** | Top of each pedal — left pedal = left brake, right = right. Can apply differentially for tight turns |
| **Parking brake** | Lever on lower pedestal — SET for parking, RELEASE before taxi |
| **Brake check** | During initial taxi — apply brakes briefly, confirm both sides respond evenly |

#### Taxi Procedure

| Step | Action | Notes |
|------|--------|-------|
| 1 | Release parking brake | Verify aircraft begins to roll (may need slight collective increase) |
| 2 | Advance collective slightly | Just enough power to start moving; heavy aircraft needs noticeable collective |
| 3 | Steer with pedals | Nosewheel responds to pedal input |
| 4 | Maintain ≤ 20 km/h | Read ASI or estimate — walking speed is too fast |
| 5 | Brake check | Apply toe brakes briefly to confirm stopping ability |
| 6 | Taxi to runway/takeoff point | Maintain directional control, avoid sharp turns at speed |

> *⚠ Realism Divergence: DCS ground handling is generally well-modeled, but tire friction, nosewheel shimmy, and differential braking feel may differ from real-world. The general technique is accurate.*

---

### 3.5 Rotor Engagement

| Step | Action | Indication |
|------|--------|------------|
| 1 | Verify both engines at ground idle (Ng ~63–65%) | Engine gauges stable |
| 2 | **Throttles** — Advance both to **FLY** detent | Throttles past IDLE into FLY range |
| 3 | **Nr** — Monitor rising | Nr gauge increasing toward 95% |
| 4 | **Governor** — Verify ON | Governor maintains Nr at 95% automatically |
| 5 | Wait for Nr to stabilize at 95% | Nr steady at 95 ± 2% |
| 6 | **Rotor smoothing** — Note vibration level | Normal light vibration; excessive vibration = maintenance issue |
| 7 | **Rotor brake** — Verify OFF | Rotor brake disengaged (should be off already) |

---

### 3.6 Pre-Takeoff Checklist

| Item | Check | Standard |
|------|-------|----------|
| **Engines** | Both at FLY, Ng/TIT/Oil in limits | Per Module 1 limits table |
| **Nr** | 95% | 92–98% acceptable |
| **Torque** | Available torque noted | Pilot reads torque at ground idle and calculates available margin |
| **Hydraulics** | Main and backup pressure normal | 65 ± 5 kgf/cm² each |
| **Caution Panel** | Clear (no amber/red except expected) | All cautions resolved |
| **Flight Controls** | Free and correct (full deflection check complete) | Smooth, full travel |
| **Trim** | Neutral / set for takeoff | Force trim set |
| **Radios** | R-863 and R-828 set, checked | Communications verified with ATC |
| **Altimeter** | Set to QFE (field elevation = 0) or QNH (sea-level pressure) | Reads correctly for known field elevation |
| **Radar Altimeter** | ON, warning altitude set | Bug at desired decision height |
| **Navigation** | ARK-15 / RSBN tuned (if applicable) | Bearing/distance verified |
| **Fuel** | Quantity sufficient, boost pumps ON, cross-feed OFF | Fuel qty noted, endurance calculated |
| **Autopilot** | Channels OFF (will engage after takeoff if desired) | All AP switches OFF |
| **Landing Gear** | DOWN and locked (three green lights) | Green light for each gear |
| **Weapons** | SAFE (verify from WSO cockpit if not already confirmed) | Master arm SAFE |
| **Crew Coordination** | Brief WSO on departure plan | Communication confirmed |
| **Exterior Lights** | As required (beacon ON, nav lights per conditions) | Anti-collision beacon ON minimum |

---

### Module 3 — Key Data Summary Table

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Ground Idle Ng** | 63–65% | Both engines |
| **TIT Start Limit** | ≤ 830°C | Abort above |
| **APU Start** | Battery ON → APU button | ~30 sec to operating RPM |
| **Nav Warm-Up (DCS)** | 2–3 min | DISS-15 Doppler longest |
| **Taxi Speed** | ≤ 20 km/h straight, ≤ 10 km/h turns | Use ASI or estimate |
| **Nr at FLY** | 95% | Governor maintains |
| **Altimeter Setting** | QFE or QNH | Soviet convention: QFE preferred (field = 0) |

---

### Module 3 — Instructor Notes / Common Student Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Starting engine with throttle not at IDLE | Possible over-speed or uncommanded power | Verify IDLE detent before pressing start button |
| Not monitoring TIT during start | Hot start → engine damage | "Eyes on TIT from the moment you press START" |
| Forgetting APU shutdown after generators online | APU runs unnecessarily, wastes fuel, adds heat | Checklist discipline: "Gens online → APU gen OFF → APU OFF" |
| Releasing parking brake without sufficient power set | Aircraft rolls unexpectedly on slopes | Set slight collective before brake release; be ready to brake |
| Taxiing too fast | Inability to stop or turn safely | "20 km/h is faster than you think. Err on the slow side" |
| Skipping flight control check | Undetected binding or hydraulic issue | Require full-deflection check every startup. Make it non-negotiable |
| Not setting altimeter correctly (QFE vs. QNH confusion) | Altitude errors in pattern | Brief QFE vs. QNH before each sortie: "QFE = field reads zero. QNH = field reads field elevation" |
| Forgetting to configure WSO-side systems | RWR/CM not ready; weapons not verified SAFE | Include WSO cockpit check in startup flow. "Switch to `1`, set RWR/CM, verify SAFE, switch back to `2`" |

---

## Module 4 — Hover & Takeoff

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Perform a hover power check and determine if IGE/OGE hover is achievable at current weight and conditions.
2. Execute a controlled pick-up to a hover and maintain a stable hover using outside references.
3. Perform hover turns (pedal turns) maintaining position and altitude.
4. Execute a running takeoff (preferred Mi-24P departure).
5. Execute a normal hover takeoff when conditions permit.
6. Describe the maximum performance takeoff technique and when to use it.
7. Establish the recommended climb profile (120–140 km/h Vy).
8. Recognize and respond to ground resonance during ground operations.

---

### 4.1 Hover Technique

**Critical Context:** The Mi-24P is a poor hover platform. At 11,000+ kg, it requires enormous power to hover. The stub wings produce only drag at hover speeds. Hover time should be minimized — the Mi-24P is designed for running takeoffs and running landings.

#### Pick-Up to a Hover

| Step | Action | Notes |
|------|--------|-------|
| 1 | Verify pre-takeoff checks complete | Engines, instruments, caution panel |
| 2 | Set force trim | Cyclic approximately centered |
| 3 | Smoothly increase collective | **Slowly** — power demand is large; expect 60–80% torque for IGE hover |
| 4 | Apply **left pedal** as collective increases | Counteract torque effect — aggressive pedal input needed due to high power |
| 5 | Maintain position with cyclic corrections | Outside reference: pick a ground point and hold over it |
| 6 | Establish hover at 2–3 m (6–10 ft) AGL | Gear may be down or up; if up, hover at ~5 m |
| 7 | Stabilize — hold heading, position, altitude | Constant small corrections on all three controls |

**Power Requirements for Hover:**

| Condition | Approx. Torque Required | Feasibility |
|-----------|------------------------|-------------|
| IGE hover, light weight (9,000 kg), sea level, standard day | 60–70% | Comfortable |
| IGE hover, MTOW (11,500 kg), sea level, standard day | 80–90% | Marginal — minimal reserve |
| OGE hover, MTOW, sea level, standard day | 90–100%+ | **May not be possible** |
| IGE hover, MTOW, 1,000 m elevation, hot day (35°C) | 90–100%+ | **May not be possible** |
| Light weight, sea level, OGE | 70–80% | Achievable with margin |

#### Hover Power Check

Before committing to any hover operation, verify:

1. Note current torque in IGE hover.
2. Compare to maximum continuous torque (85% both engines).
3. If hover torque ≥ 80%, OGE hover is marginal or impossible.
4. If hover torque ≥ 85%, **do not attempt** OGE hover — use running takeoff.
5. If hover torque ≥ 90%, even IGE hover is marginal — **recommend running takeoff**.

**Decision Rule:** If IGE hover torque exceeds 80% of max continuous, plan a running takeoff.

#### Hover Turns (Pedal Turns)

| Aspect | Technique |
|--------|-----------|
| **Input** | Pedals only — apply steady pedal in desired turn direction |
| **Collective** | Slight increase may be needed as torque demand shifts |
| **Cyclic** | Anticipate drift — the aircraft will translate slightly during yaw changes |
| **Speed** | Slow, controlled rotation — the Mi-24P has high yaw inertia |
| **Common error** | Over-pedal → rapid rotation → student chases heading → overcorrection spiral |
| **Correction** | "Small, smooth pedal inputs. Let the aircraft rotate. Anticipate the stop" |

#### Hover Taxi

| Aspect | Technique |
|--------|-----------|
| **Speed** | < 20 km/h forward |
| **Altitude** | 2–3 m AGL (landing gear down) or 5 m (gear up) |
| **Control** | Cyclic forward for movement, collective for altitude, pedals for heading |
| **Nosewheel steering** | Not available in flight — pedals control tail rotor only |
| **Risk** | LTE in crosswind during slow hover taxi — maintain awareness of wind direction |

---

### 4.2 Takeoff Profiles

#### Running Takeoff (Preferred — Standard Mi-24P Departure)

The running takeoff is the **standard departure method** for the Mi-24P. It minimizes time in the power-intensive hover regime and uses the aircraft's natural tendency to accelerate.

| Step | Action | Parameter |
|------|--------|-----------|
| 1 | Align with takeoff direction on runway/taxiway | Into wind preferred |
| 2 | Smoothly increase collective to 70–80% torque | Aircraft begins rolling forward |
| 3 | Maintain directional control with pedals (nosewheel steering) | Keep straight |
| 4 | As speed builds (~30–40 km/h), apply slight forward cyclic | Nose attitude lowers, acceleration increases |
| 5 | At ~50 km/h — **ETL** | Feel: vibration decrease, lift increase, nose pitch-up tendency |
| 6 | Counter ETL pitch-up with forward cyclic | Maintain acceleration |
| 7 | At 70–80 km/h — aircraft becomes light on gear | Reduce forward cyclic slightly |
| 8 | Aircraft lifts off; establish positive climb | Gear clears ground |
| 9 | **Landing gear** — UP | Pilot — gear lever UP; verify three gear lights extinguish |
| 10 | Accelerate to **120–140 km/h** (Vy) | Best rate of climb speed |
| 11 | Climb at Vy to desired altitude | Maintain torque within limits |

> **DCS Keyboard:** Landing gear toggle: `G` (default).

**Why Running Takeoff is Preferred:**
- Requires ~15–20% less torque than hover takeoff.
- Wings begin generating lift during the ground roll.
- Less exposure to LTE and vortex ring state.
- Faster transition to safe flight regime.
- The aircraft's design intent — Mi-24P was designed for runway operations.

#### Normal Hover Takeoff

Used when runway is unavailable or precision departure is required (confined area with clear departure path).

| Step | Action | Notes |
|------|--------|-------|
| 1 | Establish IGE hover (per 4.1) | Verify adequate power margin |
| 2 | Confirm hover power check | Torque < 80% desired |
| 3 | Smoothly apply forward cyclic | Aircraft begins accelerating |
| 4 | As speed builds, expect nose pitch-up at ETL (~50 km/h) | Counter with cyclic |
| 5 | Maintain altitude or begin gentle climb | Collective adjustment as translational lift increases efficiency |
| 6 | At 80+ km/h, accelerate to Vy (120–140 km/h) | Positive rate established |
| 7 | **Gear UP** | After positive rate and climb confirmed |
| 8 | Continue climb at Vy | Wings now contributing lift |

#### Maximum Performance Takeoff

Used when obstacles require maximum climb gradient (trees, buildings, wires). Higher risk — should only be attempted when necessary.

| Step | Action | Notes |
|------|--------|-------|
| 1 | Establish hover (or from ground with collective pull) | Maximum power application |
| 2 | Apply maximum allowable torque | ≤ 96% transient (both engines) for ≤ 30 seconds |
| 3 | Simultaneously apply forward cyclic for acceleration AND collective for climb | Aggressive but controlled |
| 4 | Pitch attitude: 10–15° nose up initially | Trading speed for altitude |
| 5 | Accelerate through ETL as rapidly as possible | Wings begin helping |
| 6 | Transition to Vy (120–140 km/h) once clear of obstacles | Reduce to continuous torque limits |
| 7 | **Gear UP** after obstacle clearance | Reduce drag |

**Warning:** Maximum performance takeoff at high gross weight in hot/high conditions may exceed engine limits. Verify power available before committing.

---

### 4.3 Climb Profile

| Profile | Airspeed | Torque | Use |
|---------|----------|--------|-----|
| **Best Rate of Climb (Vy)** | 120–140 km/h (65–76 kts) | 85–90% | Maximum altitude gain per time |
| **Cruise Climb** | 180–200 km/h (97–108 kts) | 80–85% | Comfortable climb, better forward speed |
| **En Route Climb** | 220 km/h (119 kts) | 75–80% | Fuel-efficient climb to cruise altitude |

**Level-Off Technique:**
1. As approaching desired altitude (~50 m before), reduce collective gradually.
2. Allow airspeed to increase toward cruise (220–260 km/h).
3. Adjust power for level flight — torque typically 60–75% at cruise.
4. Trim for hands-off flight. Engage autopilot if desired.

---

### 4.4 Ground Resonance — Emergency Procedure

Ground resonance is the **single most time-critical emergency** for the Mi-24P. It can destroy the aircraft in 3–5 seconds.

#### Conditions That Trigger Ground Resonance

| Factor | Detail |
|--------|--------|
| Hard surface (concrete, asphalt) | Resonance couples more effectively on rigid surfaces |
| Wheels on ground with rotor turning | Required coupling path: landing gear ↔ airframe ↔ rotor |
| Triggering event | Lead-lag damper malfunction, unequal tire pressure, hard landing, single-gear ground contact, blade imbalance |
| Rotor RPM in resonance band | Specific Nr ranges where rotor lead-lag frequency matches airframe natural frequency |

#### Recognition

| Symptom | Timing |
|---------|--------|
| Sudden onset of airframe oscillation | 0 seconds — onset |
| Oscillation amplitude increasing rapidly | 1–2 seconds — building |
| Violent shaking, potential structural failure | 3–5 seconds — critical |

The oscillation is unmistakable — it is far more violent than any normal vibration. The aircraft will feel like it is tearing itself apart.

#### Immediate Action — Decision Tree

```
Ground Resonance Detected!
│
├── Nr ≥ 90% (rotor has energy to fly)?
│   ├── YES → FULL COLLECTIVE UP → GET AIRBORNE
│   │         Breaking ground contact eliminates the resonance.
│   │         Once airborne, fly to a different landing spot.
│   │         Inspect aircraft before further flight.
│   │
│   └── NO → THROTTLES TO STOP → ROTOR BRAKE ON → EMERGENCY SHUTDOWN
│            Cannot fly. Stop the rotor as fast as possible.
│            Evacuate aircraft after rotor stops.
│            Aircraft is grounded for maintenance.
```

> *⚠ Realism Divergence: DCS models ground resonance, but the onset severity and time-to-destruction may be less dramatic than real-world. The phenomenon is achievable in DCS and the emergency response (fly or shut down) should be practiced.*

---

### Module 4 — Key Data Summary Table

| Parameter | Value | Notes |
|-----------|-------|-------|
| **ETL speed** | ~50 km/h (27 kts) | Vibration decrease, lift increase, nose pitch-up |
| **Running takeoff liftoff** | ~70–80 km/h (38–43 kts) | Varies with weight and wind |
| **Vy (Best Rate of Climb)** | 120–140 km/h (65–76 kts) | Weight dependent |
| **Cruise Climb** | 180–200 km/h (97–108 kts) | Comfortable en route climb |
| **Hover torque (IGE, moderate weight)** | 60–80% | Condition dependent |
| **Running T/O torque** | 70–80% | Less than hover |
| **Max Performance torque** | ≤ 96% (transient, 30 sec) | Obstacle clearance only |
| **Ground resonance decision threshold** | Nr ≥ 90% → fly; Nr < 90% → shut down | 3–5 seconds to act |

---

### Module 4 — Instructor Notes / Common Student Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Attempting hover at MTOW on a hot day | Exceeds torque limits or settles into ground | Pre-brief power margins. "If you can't hover, you can always do a running takeoff" |
| Raising collective too fast during pick-up | Over-torque, over-yaw (insufficient pedal compensation) | "Collective comes up slowly. Pedal leads collective — add left pedal before you feel the yaw" |
| Failing to counter ETL pitch-up | Aircraft pitches nose up sharply at 50 km/h | "Anticipate ETL. As you pass 40 km/h, prepare for forward cyclic input" |
| Not retracting gear after takeoff | Increased drag, reduced performance, speed limitation | "Positive rate, gear UP. Make it a callout" |
| Ignoring ground resonance briefing | Frozen response when vibration starts | "Ground resonance kills in seconds. The answer is always: fly or shut down. There is no third option" |
| Over-controlling in hover | Pilot-induced oscillation, aircraft wobbles | "The Mi-24 is heavy. Inputs take time to respond. Be patient. Small corrections" |
| Using hover takeoff when running takeoff is available | Unnecessary power exposure, higher risk | "If you have a runway, use it. Running takeoffs save power and reduce risk" |
| Not performing hover power check | Commits to OGE hover without knowing power margin | "Hover power check is mandatory before every OGE operation. No exceptions" |

---

## Module 5 — Basic Flight Maneuvers

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Maintain level flight at cruise speed (220–260 km/h), trimmed and in coordinated flight.
2. Execute coordinated turns at 15°, 30°, and 45° bank, maintaining altitude and airspeed.
3. Perform climbs and descents at recommended profiles.
4. Demonstrate slow flight and the transition from cruise to below ETL.
5. Execute a practice autorotation entry with power recovery at altitude.
6. Use the force trim system effectively during speed changes and maneuvers.
7. Operate the autopilot channels (roll, pitch, heading, altitude) in flight.
8. Demonstrate straight and level flight at 100, 150, 200, and 260 km/h, noting control feel and power changes.

---

### 5.1 Level Flight

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Cruise speed** | 220–260 km/h (119–140 kts) | Wings generating significant lift (~20–25% of total) |
| **Cruise torque** | 60–75% | Varies with altitude, weight, temperature |
| **Cruise altitude (training)** | 300–1,000 m (1,000–3,300 ft) AGL | Typical BQT training altitude |
| **Trim** | Set for hands-off flight | Re-trim after every speed/power change |

**Stability Characteristics at Cruise:**
The Mi-24P is notably stable at cruise speeds due to the stub wings providing longitudinal stability. The aircraft "wants" to fly at 220+ km/h and resists disturbances at this speed. This is unlike lighter helicopters that are inherently less stable. Students transitioning from UH-1 or OH-58 will notice the Hind feels more like a fixed-wing aircraft at speed.

**Power Settings by Altitude (Approximate, MTOW):**

| Altitude | Cruise Speed | Torque Required | Notes |
|----------|-------------|-----------------|-------|
| Sea level | 240 km/h | 60–65% | Comfortable margin |
| 500 m | 240 km/h | 65–70% | Moderate |
| 1,000 m | 240 km/h | 70–75% | Higher power demand |
| 2,000 m | 240 km/h | 78–85% | Approaching limits at MTOW |

---

### 5.2 Turns

#### Coordinated Turn Technique

| Input | Action |
|-------|--------|
| **Cyclic** | Roll into desired bank angle |
| **Pedals** | Coordinate — keep slip ball centered |
| **Collective** | **Increase** slightly as bank increases to maintain altitude (more lift vector tilted = less vertical lift) |

#### Bank Angle vs. G-Loading

| Bank Angle | G-Load | Torque Increase Required | Notes |
|------------|--------|--------------------------|-------|
| 15° | 1.04 G | Minimal | Gentle turn; standard course corrections |
| 30° | 1.15 G | ~5% | Standard maneuvering turn |
| 45° | 1.41 G | ~15–20% | Significant; monitor torque |
| 60° | 2.0 G | ~30–40% | **Caution** — approaching structural awareness |
| 75° | — | — | **Not recommended** — approaching G limit at any speed |

**Structural Limit:** +3.5 G. At 60° bank, any additional pull or turbulence gust approaches this limit. Students should be briefed that 45° bank is the normal training limit, with 60° introduced only with instructor supervision.

**Turn at Speed:**
At cruise (240 km/h), the Mi-24P turns with a relatively large radius due to its weight and speed. The wings contribute to turn performance by maintaining lift efficiency. Below 150 km/h, turn radius decreases but power required increases as wing lift diminishes.

---

### 5.3 Climbs & Descents

#### Climbs

| Profile | Airspeed | Torque | Use |
|---------|----------|--------|-----|
| **Vy (Best Rate)** | 120–140 km/h | 85–90% | Maximum altitude gain per time |
| **Cruise Climb** | 200 km/h | 80–85% | En route with reasonable forward speed |
| **High-Speed Climb** | 240 km/h | 85–90% | Terrain clearance while maintaining speed |

**Climb Technique:**
1. Increase collective to desired climb power.
2. Adjust cyclic to maintain target airspeed (nose up for slower, nose down for faster).
3. Trim for the climb attitude.
4. Monitor Nr — should remain at 95%. Governor handles automatically.
5. Monitor TIT — sustained climb may approach continuous limits at altitude.

#### Descents

| Profile | Airspeed | Power | Descent Rate | Use |
|---------|----------|-------|-------------|-----|
| **Cruise Descent** | 220–260 km/h | 50–60% | 3–5 m/s | Standard en route descent |
| **Rapid Descent** | 200 km/h | 30–40% | 8–10 m/s | Tactical or expedited altitude loss |
| **Autorotation Descent** | 170 km/h | 0% (idle) | 15–20+ m/s | Emergency — engine failure |

**Descent Cautions:**
- **Nr management:** In low-power descents, Nr may increase as the rotor enters autorotation regime. The governor reduces fuel flow automatically, but monitor Nf/Nr.
- **Settling with power risk:** If descending at slow speed (< 50 km/h) with power applied, risk of vortex ring state. Maintain airspeed above 50 km/h during powered descents.
- **Wing effects:** The stub wings generate more drag during descent, which increases the descent rate compared to a wingless helicopter. This is a factor in autorotation planning.

---

### 5.4 Slow Flight

Slow flight (below 100 km/h) fundamentally changes the Mi-24P's handling:

| Speed Range | Character | Notes |
|-------------|-----------|-------|
| 220–260 km/h | Stable, airplane-like; wings generating lift | Normal operating regime |
| 100–150 km/h | Transitional; wings losing effectiveness; more power required | Increasing collective needed |
| 50–100 km/h | Wings producing minimal lift, maximum drag; high power required | Near ETL; control feel changes |
| < 50 km/h | Below ETL; rotor doing all the work; hover-like power demand | Full collective may be needed; control authority changes |
| 0 km/h (hover) | Maximum power required; wings = dead weight/drag | Only feasible at moderate gross weight |

**Transition from Cruise to Slow Flight:**
1. Reduce collective progressively — airspeed decreases.
2. As speed drops below ~150 km/h, note increasing collective requirement to maintain altitude.
3. At ~100 km/h, retrim — trim forces change significantly.
4. Below 50 km/h (ETL), expect:
   - Vibration increase (transverse flow effect).
   - Significant power increase required.
   - Yaw changes (collective-to-yaw coupling becomes dominant).
   - Control feel changes from airplane-like to helicopter-like.

**Warning:** If collective is already at 85%+ during slow flight, the aircraft cannot maintain altitude below ETL. The student must recognize this and either accelerate or accept a descent.

---

### 5.5 Autorotation Entry (Practice)

Practice autorotation in the Mi-24P is performed at altitude with a power recovery — **not** a full-down autorotation.

#### Autorotation Entry Procedure

| Step | Action | Parameter |
|------|--------|-----------|
| 1 | Establish entry altitude ≥ 500 m AGL | Safety margin |
| 2 | Entry airspeed: 180–200 km/h | Above optimal auto speed |
| 3 | Instructor simulates dual engine failure (throttles to IDLE) | Or student practices throttle chop |
| 4 | **Immediately lower collective** to maintain Nr | Nr target: 95% (92–98% acceptable) |
| 5 | Establish autorotation airspeed: **170 km/h (92 kts)** | Best glide speed |
| 6 | Trim for 170 km/h | Stable descent |
| 7 | Monitor Nr — adjust collective to maintain 92–98% | Nr increases with collective down; may need to raise collective slightly |
| 8 | Note descent rate: **15–20 m/s (3,000–4,000 fpm)** | High due to weight + wing drag |
| 9 | At recovery altitude (~200 m AGL): **throttles to FLY** | Engines spool up |
| 10 | **Collective UP** to arrest descent | As engines provide power |
| 11 | Resume normal flight | Climb or level off |

#### Autorotation Key Data

| Parameter | Value |
|-----------|-------|
| **Best glide speed** | 170 km/h (92 kts) |
| **Nr target** | 95% (range 92–98%) |
| **Descent rate** | 15–20 m/s (~3,000–4,000 fpm) — **HIGH** |
| **Glide ratio** | ~4:1 (approximately) — poor compared to lighter helicopters |
| **Time from 500 m to ground** | ~25–35 seconds |
| **Wing effect** | Wings increase descent rate (drag) but also provide some energy to manage in flare |

**Key Difference from Single-Engine Helicopters:** In a light single-engine helicopter, autorotation descent rates are 8–12 m/s. The Mi-24P descends at 15–20+ m/s due to its high weight and wing drag. This means less time to react, less glide distance, and a more aggressive flare required. However, the Mi-24P has twin engines — a total power loss is much less likely than in a single-engine helicopter.

> *⚠ Realism Divergence: DCS autorotation descent rates and glide characteristics are modeled but may differ slightly from published RLE figures. The overall technique is accurate. The high descent rate is evident in DCS and should be briefed extensively.*

---

### 5.6 Trim Technique

The Mi-24P force trim system uses electromagnetic clutches to hold the cyclic and pedals in position.

| Action | Method |
|--------|--------|
| **Set trim** | Release trim button on cyclic → controls hold current position |
| **Release trim** | Press and hold trim release button → move controls to new position → release button |
| **Re-trim after speed change** | Every speed change requires re-trimming — control forces change significantly |
| **Autopilot interaction** | Autopilot uses the trim system — when AP disconnects, trim position determines where controls "sit" |

**When to Trim:**
- After every speed change (accelerate/decelerate).
- After every power change (climb/descent/level off).
- After every configuration change (gear up/down).
- After autopilot disconnect.
- If you are holding steady pressure on any control for more than 5 seconds — trim it out.

**Common DCS Mistake:** Students forget to trim and fight the controls for extended periods. This leads to fatigue and imprecise flying. Instruction should emphasize: "Trim is your friend. If you are holding pressure, you are doing it wrong."

---

### 5.7 Autopilot Usage in Flight

#### Engaging the Autopilot

| Step | Action | Notes |
|------|--------|-------|
| 1 | Establish stable, trimmed flight | Airspeed 150+ km/h, wings level, descent rate zero |
| 2 | Verify trim is centered / neutral pressure | AP will hold current trim state |
| 3 | Engage **Pitch** channel first | Holds current pitch attitude |
| 4 | Engage **Roll** channel | Holds current bank angle (should be wings level) |
| 5 | Engage **Heading** (optional) | Holds current magnetic heading |
| 6 | Engage **Altitude** (optional) | Holds current barometric altitude |

#### Autopilot Modes Summary

| Channel | Holds | Override Method | Notes |
|---------|-------|----------------|-------|
| **Pitch** | Pitch attitude | Push through with cyclic | Re-engages when released to trim position |
| **Roll** | Bank angle / wings level | Push through with cyclic | Returns to wings level when released |
| **Heading** | Magnetic heading | Override with pedal or bank; AP re-captures when released | Holds heading, not track |
| **Altitude** | Barometric altitude | Collective change; AP re-captures | Coarse hold; ±30 m accuracy |
| **Radar Alt Hold** | Radar altitude | Requires radar altimeter active | Terrain-following (coarse); use with caution |

#### Disengaging the Autopilot

| Method | Effect |
|--------|--------|
| **AP Disconnect button** (cyclic) | Disconnects all channels simultaneously |
| **Individual channel switches** | Turns off specific channels |
| **Override by force** | Pushing through AP authority — AP remains engaged but is overridden |

**After Disconnect:** The aircraft will fly at whatever trim state existed when AP disconnected. **Re-trim immediately** or engage manual control with awareness of the current trim position.

**When NOT to Use Autopilot:**
- Hover (AP not designed for hover).
- Takeoff and landing (AP not designed for these regimes).
- Below 100 km/h (AP authority may be insufficient or inappropriate).
- During emergency procedures (unless specifically beneficial).

> *⚠ Realism Divergence: DCS implements all four autopilot channels. The altitude hold accuracy and flight director coupling may differ from real-world specs. The general behavior and engagement/disengagement procedures are accurate.*

---

### 5.8 Speed Changes — Control Feel at Various Airspeeds

| Airspeed | Control Feel | Power Required | Wing Contribution | Notes |
|----------|-------------|----------------|-------------------|-------|
| **100 km/h** | Heavy, helicopter-like; large inputs needed | High (75–85%) | Minimal (~5%) | Just above ETL; uncomfortable regime |
| **150 km/h** | Transitional; moderate inputs | Moderate (65–75%) | Growing (~10%) | Wings beginning to contribute |
| **200 km/h** | Lighter, more responsive; airplane-like | Moderate (60–70%) | Significant (~15%) | Comfortable; good maneuvering speed |
| **260 km/h** | Light, responsive; very stable | Moderate (65–75%) | High (~25%) | Fast cruise; rotor offloaded |
| **300 km/h (VNE)** | Very light; potential vibration onset | High (75–85%) | Maximum (~25%) | **LIMIT — retreating blade stall risk** |

**Key Insight for Students:** The Mi-24P feels like two different aircraft depending on speed:
- **Below 100 km/h:** It's a heavy, power-hungry helicopter that requires aggressive inputs and constant attention.
- **Above 200 km/h:** It's a stable, predictable, almost airplane-like platform that is pleasant to fly.

The training goal is to get the student comfortable in both regimes and especially in the transition between them.

---

### Module 5 — Instructor Notes / Common Student Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Not trimming after speed changes | Fighting controls, imprecise flight, fatigue | "If you are holding pressure for more than 5 seconds, TRIM" |
| Exceeding bank angle limits in turns | G-limit exceedance, structural concern | Brief bank angle limits before each maneuvering sortie. 45° training max |
| Nr excursion during autorotation practice | Over-speed or under-speed rotor | "Collective controls Nr in autorotation. Up = slower, Down = faster" |
| Panic during autorotation descent rate | Premature power recovery or excessive collective input | Brief the high descent rate (15–20 m/s) before practice. "It will be fast. That is normal for this aircraft" |
| Trying to hover at high speed | Reducing speed too fast, entering settling with power | "Decelerate gradually. Monitor power required. If torque exceeds 85%, stop slowing down" |
| Not engaging autopilot before switching seats | Uncontrolled flight during seat switch | "AP ON. Trimmed. Stable. Then switch" |
| Misunderstanding autopilot altitude hold | Expects precise altitude hold; gets ±30 m oscillation | Brief: "AP altitude hold is coarse. It prevents altitude excursions, not precision hover" |
| Flying at VNE in level flight | Retreating blade stall, structural risk | "VNE is 300 km/h. Your cruise should be 240–260 km/h. Leave margin" |

---

## Module 6 — Navigation (DISS-15 / ARK-15 / RSBN)

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Describe the function of the DISS-15 Doppler navigation system and interpret its displays.
2. Tune the ARK-15 ADF to an NDB station and navigate using the bearing pointer.
3. Tune the RSBN to a ground beacon and use range/bearing data for navigation.
4. Interpret the HSI (Horizontal Situation Indicator) for heading, course, and bearing information.
5. Set the radar altimeter (A-037) warning altitude and interpret the display.
6. Operate the R-863 UHF and R-828 VHF/FM radios, including frequency setting and preset channels.
7. Navigate between two points using available navigation aids.

---

### 6.1 DISS-15 Doppler Navigation System

The DISS-15 is a **Doppler radar-based** system that measures ground speed and drift angle by detecting the Doppler shift of radar signals reflected from the ground.

| Parameter | Detail |
|-----------|--------|
| **Function** | Measures ground speed (km/h) and drift angle (degrees) |
| **Display** | Pilot — Instrument panel — dedicated DISS indicators |
| **Output** | Ground speed readout; drift angle needle; data fed to navigation computer |
| **Warm-up** | ~2–3 minutes in DCS; 5–10 minutes real-world |
| **Limitations** | Inaccurate over smooth water (no Doppler return); accuracy degrades at very low altitude |
| **Integration** | Feeds into PNK (flight-navigation complex) for computed position if equipped |

**Pilot Use:**
- Ground speed indication is useful for wind calculation (compare ground speed to indicated airspeed).
- Drift angle helps maintain track over ground.
- In DCS, the DISS-15 provides data but the Mi-24P does not have a sophisticated moving map — navigation remains primarily by ARK-15, RSBN, and visual reference.

> *⚠ Realism Divergence: The DISS-15 is modeled in DCS with basic functionality. Real-world systems feed into a more complex PNK-800 flight-navigation complex that may not be fully replicated. The ground speed and drift indications are functional.*

---

### 6.2 ARK-15 ADF (Automatic Direction Finder)

The ARK-15 is a **radio compass** that points toward NDB (Non-Directional Beacon) ground stations.

| Parameter | Detail |
|-----------|--------|
| **Function** | Receives NDB signal, drives bearing pointer on HSI toward station |
| **Frequency range** | 150–1,299.5 kHz |
| **Tuning** | Pilot — Right console — ARK-15 panel — frequency knobs or preset channel selector |
| **Display** | Bearing pointer (thin needle) on HSI — points toward the NDB |
| **Modes** | COMPASS (bearing pointer active), ANT (antenna only, no pointer), OFF |
| **Accuracy** | ±3° typical; degrades near station and at low signal strength |

#### ADF Navigation Procedure

| Step | Action | Notes |
|------|--------|-------|
| 1 | Identify the NDB frequency from mission briefing or charts | e.g., 350 kHz |
| 2 | Tune ARK-15 to the NDB frequency | Rotate frequency knobs on ARK-15 panel |
| 3 | Select COMPASS mode | Bearing pointer activates on HSI |
| 4 | **Bearing pointer** shows direction TO the station | Thin needle on HSI |
| 5 | To fly direct to station: turn until bearing pointer is at 12 o'clock | Heading = station bearing |
| 6 | Maintain bearing pointer at 12 o'clock (correct for wind) | If pointer drifts right, turn right slightly |
| 7 | Station passage: pointer swings 180° (from ahead to behind) | Note time/position for navigation log |

**Homing vs. Tracking:**
- **Homing** (simple): Keep the needle at 12 o'clock. In wind, this produces a curved path.
- **Tracking** (advanced): Bracket the wind correction angle to fly a straight ground track to the station.

---

### 6.3 RSBN (Short-Range Radio Navigation)

RSBN (Радиотехническая Система Ближней Навигации) is the Soviet equivalent to TACAN. It provides **range and bearing** to a ground-based beacon.

| Parameter | Detail |
|-----------|--------|
| **Function** | Distance (range) and azimuth (bearing) from a ground beacon |
| **Range** | Up to ~150–200 km (line-of-sight dependent) |
| **Tuning** | Pilot — Right console — RSBN panel — channel selector |
| **Display** | Range: dedicated range indicator (km); Bearing: CDI needle and bearing pointer on HSI |
| **Channels** | Preset channels corresponding to specific ground beacons |
| **Approach aid** | Can provide glide path guidance for instrument approaches (PRMG mode, similar to ILS) |

#### RSBN Navigation Procedure

| Step | Action | Notes |
|------|--------|-------|
| 1 | Select RSBN channel for desired beacon | From mission briefing or charts |
| 2 | Verify signal lock | Range indicator shows distance; bearing indicator active |
| 3 | Read **range** (km) on range indicator | Distance to beacon |
| 4 | Read **bearing** from HSI CDI and bearing pointer | Magnetic bearing TO the beacon |
| 5 | Navigate using range and bearing | Combines heading toward beacon with distance check |
| 6 | For approach: select PRMG mode (if available) | CDI and glideslope indications for instrument approach |

> *⚠ Realism Divergence: DCS models RSBN with basic range and bearing functionality. Not all DCS maps have RSBN beacons available. The approach guidance (PRMG) mode may be limited depending on the DCS map and mission setup. Verify beacon availability in the mission editor.*

---

### 6.4 HSI (Horizontal Situation Indicator)

The HSI is located on the **Pilot — Instrument panel** and integrates heading, course, and bearing information.

| Element | Function |
|---------|----------|
| **Compass card** | Rotating ring showing magnetic heading (current heading under lubber line at top) |
| **Heading marker / lubber line** | Fixed at top — current heading |
| **Course pointer** | Rotatable arrow — set desired course |
| **CDI (Course Deviation Indicator)** | Bar that deflects left/right of course pointer — shows deviation from selected course |
| **ARK-15 bearing pointer** | Thin needle — points toward tuned NDB station |
| **RSBN bearing pointer** | Second needle or combined indication — points toward RSBN beacon |
| **Heading bug** | Rotatable marker — set desired heading for reference |

**Reading the HSI:**
1. Current heading: read the compass card under the lubber line.
2. Bearing to NDB: read where the ARK-15 needle points on the compass card.
3. Course deviation: CDI bar centered = on course; deflected left = you are right of course.
4. Range to RSBN: read on the separate range indicator (not on HSI).

---

### 6.5 Radar Altimeter — A-037

| Parameter | Detail |
|-----------|--------|
| **Function** | Measures absolute altitude above ground level (AGL) using radar |
| **Range** | 0–750 m (0–2,460 ft) |
| **Display** | Pilot — Instrument panel — dedicated radar altimeter dial |
| **Warning bug** | Rotatable marker — set desired low-altitude warning height |
| **Audio alert** | Sounds when descending through set warning altitude |
| **Accuracy** | ±2 m below 50 m; ±5% above 50 m |
| **Use** | Terrain awareness, approach height reference, altitude hold coupling |

**Setting the Radar Altimeter:**

| Step | Action |
|------|--------|
| 1 | Rotate the warning altitude knob to desired height (e.g., 50 m for approach) |
| 2 | Verify the bug position on the dial |
| 3 | When the aircraft descends through the set altitude, an audio warning sounds |
| 4 | Also used for autopilot radar altitude hold mode |

---

### 6.6 Radio Communication

#### R-863 UHF Radio

| Parameter | Detail |
|-----------|--------|
| **Band** | UHF (220–400 MHz) |
| **Location** | Pilot — Right console; WSO — Right console (independent access) |
| **Modes** | Preset channel or manual frequency |
| **Presets** | Up to 20 preset channels (configured in DCS mission editor) |
| **Use** | Primary ATC communications, air-to-air |
| **PTT** | Radio trigger on collective or cyclic |

#### R-828 VHF/FM Radio

| Parameter | Detail |
|-----------|--------|
| **Band** | VHF/FM (20–60 MHz) |
| **Location** | Pilot — Right console; WSO may have access |
| **Modes** | Preset channel or manual frequency |
| **Presets** | Up to 10 preset channels |
| **Use** | Ground communications, backup air-to-air |

#### Intercom System (SPU-8)

| Feature | Detail |
|---------|--------|
| **Function** | Allows Pilot and WSO to communicate |
| **Selector** | SPU-8 panel — selects which radio or intercom is active |
| **Hot mic** | Intercom may be always-on or PTT depending on setting |
| **DCS single-player** | Intercom not critical (only one human); in multi-crew, essential |

**Radio Procedure:**
1. Tune desired frequency or select preset channel.
2. Select the radio on the SPU-8 intercom selector.
3. Press PTT (radio trigger on collective/cyclic) and speak.
4. Release PTT to listen.

> *⚠ Realism Divergence: DCS radio modeling is functional but simplified. Real-world radio procedures include encryption, frequency hopping, and specific call-sign protocols. DCS uses simple frequency tuning with SRS (SimpleRadio Standalone) for multi-player communications.*

---

### Module 6 — Key Data Summary Table

| System | Tuning Location | Display | Key Use |
|--------|----------------|---------|---------|
| **DISS-15** | Pilot — Right console — Nav panel | Ground speed (km/h), drift (°) | Wind compensation, ground track |
| **ARK-15** | Pilot — Right console — ARK panel | HSI bearing pointer | NDB homing, bearing to station |
| **RSBN** | Pilot — Right console — RSBN panel | HSI CDI + range indicator | Range/bearing to beacon, approach |
| **Radar Alt** | Pilot — Instrument panel | Altitude AGL (m) | Terrain awareness, approach reference |
| **R-863** | Pilot/WSO — Right console | Audio | Primary UHF communications |
| **R-828** | Pilot — Right console | Audio | VHF/FM backup communications |
| **SPU-8** | Pilot/WSO — Intercom panel | Audio | Pilot-WSO intercom, radio select |

---

### Module 6 — Instructor Notes / Common Student Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Not waiting for DISS-15 warm-up | No ground speed data available | "If DISS reads zero, it's still warming up. Wait 2–3 minutes after power-on" |
| Confusing ADF homing with tracking | Curved flight path in crosswind, arrives late/off-target | Brief homing vs. tracking. "Homing is easy but wasteful. Tracking is precise but requires wind correction" |
| Tuning wrong RSBN channel | No signal or wrong beacon | "Verify channel from the mission briefing before takeoff. Cross-check range — does it make sense?" |
| Not setting radar altimeter warning | No audio alert for terrain proximity | "Set the bug before every flight. For pattern work, 50 m. For en route, 100 m" |
| Misreading HSI bearing pointer | Flying away from station instead of toward it | "The needle points TO the station. If the needle points behind you, the station is behind you" |
| Confusing km/h with m/s on instruments | Speed/altitude confusion | "ASI = km/h. VSI = m/s. Radar alt = m. Know your units" |
| Not tuning radios before takeoff | Unable to communicate with ATC | "Radios should be tuned and checked during the startup flow — Step 29–30 in Module 3" |

---

## Module 7 — Emergency Procedures

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Recite all boldface/immediate-action emergency procedures from memory.
2. Identify the failed engine in a single-engine failure and execute the securing procedure.
3. Describe single-engine flight characteristics and recommended speeds.
4. Execute autorotation entry from dual engine failure, including the full procedure through touchdown.
5. Describe the response to engine fire, including fire extinguisher operation.
6. Describe hydraulic failure responses for main, backup, and dual failure.
7. Describe electrical failure responses and battery-only endurance.
8. Describe tail rotor failure types and appropriate responses.
9. Execute ground resonance immediate action.
10. Identify which emergencies DCS models and which are simplified or absent.

---

### 7.1 Boldface / Immediate Action Items

These procedures must be **memorized verbatim** and executed without reference to a checklist. They address the most time-critical emergencies.

#### Single Engine Failure in Flight

```
1. COLLECTIVE — ADJUST (maintain Nr 92–98%)
2. IDENTIFY failed engine (TIT dropping, Ng dropping on one side)
3. FAILED ENGINE throttle — IDLE, then STOP
4. OPERATING ENGINE — VERIFY in limits (TIT ≤ 900°C emergency, torque ≤ 106% transient)
5. CROSS-FEED — OPEN (ensure operating engine has fuel access)
6. AIRSPEED — 160–180 km/h (best single-engine performance)
7. LAND — As soon as practicable
```

#### Dual Engine Failure in Flight (Autorotation)

```
1. COLLECTIVE — LOWER IMMEDIATELY (maintain Nr 92–98%)
2. AIRSPEED — 170 km/h (best autorotation glide)
3. Nr — MONITOR (adjust collective to maintain 92–98%)
4. LANDING AREA — SELECT (best available)
5. GEAR — DOWN (if not already)
6. At ~30–50 m AGL — FLARE (raise nose to reduce forward speed and descent rate)
7. At ~5–10 m AGL — COLLECTIVE UP (cushion touchdown)
8. TOUCHDOWN — Level attitude, accept ground contact
```

#### Engine Failure at Hover / Low Altitude

```
1. COLLECTIVE — MAINTAIN (cushion immediate descent)
2. If altitude and Nr permit — ATTEMPT TO LAND STRAIGHT AHEAD
3. If insufficient altitude — ACCEPT HARD LANDING (crash-resistant gear will absorb)
4. After landing — EMERGENCY SHUTDOWN
```

#### Engine Fire — Left Engine

```
1. LEFT THROTTLE — IDLE, then STOP
2. LEFT FUEL SHUTOFF — CLOSED
3. FIRE AGENT SELECT — BOTTLE 1
4. ENGINE SELECT — LEFT
5. DISCHARGE — PRESS
6. If fire continues after 5 seconds — BOTTLE 2, DISCHARGE
7. LAND IMMEDIATELY
```

#### Engine Fire — Right Engine

```
1. RIGHT THROTTLE — IDLE, then STOP
2. RIGHT FUEL SHUTOFF — CLOSED
3. FIRE AGENT SELECT — BOTTLE 1
4. ENGINE SELECT — RIGHT
5. DISCHARGE — PRESS
6. If fire continues after 5 seconds — BOTTLE 2, DISCHARGE
7. LAND IMMEDIATELY
```

#### Emergency Shutdown (Ground or Air)

```
1. BOTH THROTTLES — STOP
2. FUEL SHUTOFF — BOTH CLOSED
3. BATTERY — OFF (if fire/electrical emergency)
4. ROTOR BRAKE — ON (when Nr drops below 40%)
5. EVACUATE — After rotor stops
```

#### Hydraulic System Failure — Main

```
1. VERIFY backup hydraulic pressure normal (65 kgf/cm²)
2. If backup normal — CONTINUE FLIGHT on backup system
3. LANDING GEAR — Verify DOWN (may need emergency extension)
4. LAND — As soon as practicable
```

#### Hydraulic System Failure — Backup

```
1. VERIFY main hydraulic pressure normal
2. If main normal — CONTINUE FLIGHT on main system (reduced redundancy)
3. LAND — As soon as practicable
```

#### Hydraulic System Failure — Both Systems

```
1. EMERGENCY HYDRAULIC PUMP — ON (if available)
2. AIRSPEED — REDUCE below 150 km/h (lighter control forces)
3. CONTROLS — EXTREMELY HEAVY (requires maximum physical effort)
4. LAND IMMEDIATELY — Straight-in approach; running landing preferred
```

#### Tail Rotor Failure / Loss of Tail Rotor Drive

```
1. AIRSPEED — INCREASE above 120 km/h (vertical stabilizer provides directional stability)
2. DO NOT HOVER — No yaw control at low speed
3. YAW CONTROL — Use collective changes for coarse yaw control (power changes = yaw changes)
4. LANDING — Running landing ONLY; maintain 80+ km/h until touchdown
5. DIRECTION CONTROL ON GROUND — Differential braking after touchdown
```

#### Tail Rotor Pitch Control Failure (Runaway)

```
1. If nose yaws uncommanded — IDENTIFY direction of yaw
2. PEDAL — FULL OPPOSITE to counter yaw (may have limited effect)
3. POWER — ADJUST collective to counteract yaw (reducing power may reduce yaw tendency)
4. AIRSPEED — Maintain 120+ km/h for vertical stabilizer authority
5. LAND IMMEDIATELY — Running landing
```

---

### 7.2 Single Engine Operations — Expanded

The Mi-24P's twin-engine configuration means that single-engine flight is **not an autorotation scenario**. The aircraft can fly, maneuver, and land on one engine — with significant limitations.

#### Identifying the Failed Engine

| Indicator | Failed Engine | Operating Engine |
|-----------|--------------|-----------------|
| **TIT** | Dropping toward ambient | Normal or increasing |
| **Ng** | Dropping toward zero | Normal or increasing |
| **Torque** | Dropping | Increasing (compensating) |
| **Yaw** | Aircraft yaws toward failed engine side (asymmetric torque) | — |

#### Single-Engine Flight Characteristics

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Max continuous torque** | 93% (on operating engine) | Versus 85% with both engines |
| **Max transient torque** | 106% (30 seconds) | Emergency only |
| **TIT limit** | 900°C (15 seconds) | Emergency power |
| **Recommended airspeed** | 160–180 km/h (86–97 kts) | Best single-engine performance |
| **Hover capability** | **NOT possible** at most weights | Insufficient power from one engine |
| **Climb capability** | Limited — may not be able to maintain altitude at high weight | Depends on weight, altitude, temperature |
| **Service ceiling** | Dramatically reduced | May be unable to maintain current altitude |

#### Single-Engine Approach & Landing

1. Declare emergency. Plan straight-in approach to nearest suitable field.
2. Maintain 160–180 km/h en route; do not slow below 140 km/h until short final.
3. Gear DOWN early (gravity extension if hydraulic main failed).
4. **Running landing preferred** — do not attempt to hover.
5. Decelerate gradually on final; touch down at 60–80 km/h ground speed.
6. Nosewheel steering and brakes for directional control after landing.

---

### 7.3 Loss of Tail Rotor Effectiveness (LTE) — Expanded

See Module 1 Section 1.12 for aerodynamic details. This section covers the emergency response.

**Recognition:**
- Uncommanded yaw (typically nose-right for the Mi-24P due to right-side pusher tail rotor).
- Increasing pedal input with no yaw arrest.
- May occur during hover pedal turns, slow flight in crosswind, or approach to landing.

**Recovery Procedure:**

| Step | Action | Timing |
|------|--------|--------|
| 1 | Apply full opposite pedal | Immediate |
| 2 | Push cyclic forward — accelerate | As speed increases, vertical stabilizer helps, tail rotor regains authority |
| 3 | Above 80–100 km/h — yaw stabilizes | Recovery achieved |
| 4 | If at low altitude — accept the yaw and focus on controlled landing | Do not fixate on stopping the yaw at the cost of a crash |

**Prevention:**
- Avoid prolonged hover in tailwind conditions.
- During hover pedal turns, monitor wind direction — if turning into the critical azimuth, stop the turn.
- Maintain situational awareness of wind relative to aircraft heading at all times during low-speed flight.

---

### 7.4 Settling with Power (Vortex Ring State) — Expanded

**Conditions:**
- Airspeed < 50 km/h.
- Descent rate > 5 m/s.
- Power applied (collective up).

**Recognition:**
- High descent rate that does **not** improve with additional collective.
- Vibration and buffeting.
- Uncommanded roll or yaw oscillations.
- Altitude loss accelerating.

**Recovery:**

| Step | Action | Notes |
|------|--------|-------|
| 1 | **Cyclic forward** — gain airspeed | Priority is to escape the vortex |
| 2 | **Reduce collective** momentarily | Breaks the vortex ring |
| 3 | Accelerate above 50 km/h | Out of the vortex ring envelope |
| 4 | Resume normal flight | Altitude loss: 50–150+ m during recovery |

**Mi-24P Specific Risk:** The high disc loading (~50 kg/m²) means the Mi-24P enters vortex ring state at **lower** descent rates than lighter helicopters. The altitude loss during recovery is also greater due to the aircraft's weight. At low altitude, vortex ring state may be unrecoverable.

---

### 7.5 Autorotation — Full Procedure (Expanded)

Autorotation in the Mi-24P is the **last resort** — it requires a dual engine failure or other catastrophic loss of power. The procedure is demanding due to the high descent rate and weight.

#### Full Autorotation Procedure

| Phase | Action | Parameters |
|-------|--------|-----------|
| **Entry** | Lower collective immediately; maintain Nr 92–98% | Within 2 seconds of power loss |
| **Glide** | Establish 170 km/h; adjust collective for Nr | Descent rate: 15–20 m/s |
| **Gear** | Gear DOWN (if not already) | Critical — need gear for landing |
| **Site selection** | Choose landing area (field, road, clear area) | Into wind preferred |
| **Flare** | At ~30–50 m AGL, raise nose to ~15–20° nose up | Converts forward speed to rotor energy; reduces descent rate |
| **Level** | At ~10–15 m AGL, level the aircraft | Prevent tail strike |
| **Collective pull** | At ~5–10 m AGL, pull collective firmly | Uses stored rotor energy to cushion landing |
| **Touchdown** | Level attitude, accept ground contact | Gear absorbs impact; expect firm landing |
| **After landing** | Emergency shutdown; evacuate if necessary | Rotor will be near-stopped; brake if needed |

#### Autorotation Key Parameters

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Best glide speed** | 170 km/h (92 kts) | Maximum glide distance per altitude |
| **Nr range** | 92–98% | Below 92% = rotor stall risk; above 110% = overspeed risk |
| **Descent rate** | 15–20 m/s (3,000–4,000 fpm) | **Very high** — less time and distance than light helicopters |
| **Glide ratio** | ~4:1 | From 500 m AGL: ~2 km glide distance |
| **Flare initiation** | 30–50 m AGL | Higher than light helicopters due to inertia and speed |
| **Collective pull height** | 5–10 m AGL | Timing is critical — too early = run out of rotor energy; too late = hard impact |

**Wing Effect on Autorotation:**
The stub wings increase drag during autorotation, resulting in a **higher descent rate** than a wingless helicopter of comparable weight. However, the wings also carry kinetic energy at speed that can be converted in the flare. The net effect is that the Mi-24P auto is faster, more aggressive, and requires more altitude than a UH-1 or OH-58D autorotation.

> *⚠ Realism Divergence: DCS models autorotation dynamics for the Mi-24P. The descent rate and glide characteristics are generally accurate but may differ slightly from published RLE figures. Full autorotation landings are challenging in DCS and require extensive practice.*

---

### 7.6 Hydraulic Failure — Expanded

#### Main Hydraulic System Failure

| Aspect | Detail |
|--------|--------|
| **Indication** | HYD MAIN caution light; pressure gauge shows < 55 kgf/cm² |
| **Effect** | Backup system takes over flight control authority automatically |
| **Flight characteristics** | Normal (backup provides full control authority) |
| **Landing gear** | May require emergency extension (main system normally powers gear) |
| **Action** | Land as soon as practicable; do not delay |

#### Backup Hydraulic System Failure

| Aspect | Detail |
|--------|--------|
| **Indication** | HYD BACKUP caution light; pressure gauge shows < 55 kgf/cm² |
| **Effect** | Main system continues to power all controls |
| **Flight characteristics** | Normal — but reduced redundancy |
| **Action** | Land as soon as practicable |

#### Dual Hydraulic Failure

| Aspect | Detail |
|--------|--------|
| **Indication** | Both HYD caution lights; both pressure gauges low |
| **Effect** | **Controls become extremely heavy or impossible** — irreversible system has no manual reversion |
| **Emergency pump** | Activate emergency electric hydraulic pump (if available) — may restore partial authority |
| **Action** | Reduce speed below 150 km/h; fly straight-in approach; running landing; **LAND IMMEDIATELY** |
| **Physical effort** | Maximum pilot strength required to move controls |

---

### 7.7 Electrical Failure — Expanded

#### Single Generator Failure

| Aspect | Detail |
|--------|--------|
| **Indication** | GEN 1 or GEN 2 caution light |
| **Effect** | Remaining generator powers both buses via bus tie |
| **Action** | Monitor electrical load; shed non-essential equipment if needed |
| **Flight** | Continue normal operations; land as soon as convenient |

#### Dual Generator Failure

| Aspect | Detail |
|--------|--------|
| **Indication** | Both GEN caution lights |
| **Effect** | Battery power only — essential bus remains powered |
| **Battery endurance** | ~20–30 minutes |
| **Available systems** | Basic flight instruments, one radio (R-863), fire detection |
| **Lost systems** | Most avionics, navigation, non-essential instruments |
| **Action** | Declare emergency; **LAND IMMEDIATELY** before battery depletion |

#### APU Restart in Flight

If both generators fail but engines are running, attempt APU restart for emergency electrical power:

1. APU switch — START (requires sufficient battery voltage).
2. If APU starts — APU Generator ON.
3. Essential and non-essential buses restored.
4. Proceed to nearest landing field.

> *⚠ Realism Divergence: In-flight APU restart capability may not be fully modeled in DCS. Real-world Mi-24P can attempt APU restart in flight for emergency power. In DCS, this may or may not be functional depending on module version.*

---

### 7.8 Fire — Expanded

#### Fire Detection System

The Mi-24P has dedicated fire detection loops for both engine compartments. A fire illuminates the respective **FIRE L** or **FIRE R** warning light (red) and triggers an audio alarm.

#### Fire Suppression System

| Component | Detail |
|-----------|--------|
| **Fire bottles** | 2 × fire extinguisher bottles |
| **Agent select** | Pilot — Fire panel — Bottle 1 or Bottle 2 selector |
| **Engine select** | Pilot — Fire panel — LEFT or RIGHT engine selector |
| **Discharge** | Pilot — Fire panel — DISCHARGE button |
| **Sequence** | Discharge Bottle 1 first; if fire persists 5 seconds, discharge Bottle 2 |

#### Engine Fire Procedure (Either Engine)

1. Throttle (affected engine) — IDLE then STOP.
2. Fuel shutoff (affected engine) — CLOSED.
3. Select BOTTLE 1 → Select affected ENGINE → DISCHARGE.
4. If fire light remains after 5 seconds → Select BOTTLE 2 → DISCHARGE.
5. If fire extinguished — continue single-engine to nearest field.
6. If fire NOT extinguished — **LAND IMMEDIATELY** by any means available.

#### Electrical Fire

1. Identify smoke source (panel/console area).
2. If identifiable CB — pull the circuit breaker.
3. If not identifiable — shed electrical loads progressively (generator off, non-essential bus off).
4. Ventilate cockpit if possible (open vent, but be aware of draft potentially feeding fire).
5. Land immediately.

---

### 7.9 Main Gearbox Failure Indications

| Indication | Severity | Action |
|------------|----------|--------|
| **Chip light** (CHIP DET caution) | Warning — metal in oil | Land as soon as practicable; monitor oil temp/pressure |
| **Oil pressure dropping** | Caution → Warning | If below 2.5 kgf/cm² — **Land immediately** |
| **Oil temperature rising** | Caution → Warning | If above 110°C — **Land as soon as possible**; above 130°C — **Land immediately** |
| **Unusual noise / vibration** | Warning | Reduce power; **Land immediately** |
| **Seizure** (sudden rotor deceleration) | **Critical** | Enter autorotation; **Land immediately** |

---

### 7.10 Additional Emergency Awareness Items

#### Mast Bumping

- **Fully articulated rotor = lower risk** than semi-rigid/teetering systems.
- Still possible at very low/negative G (pushovers, turbulence).
- **Non-recoverable** once mast contact occurs.
- Prevention: avoid pushovers, maintain positive G, respect −0.5 G limit.

#### Dynamic Rollover

- Occurs when one gear anchored and aircraft rolls around the contact point.
- Prevention: smooth collective, avoid lateral drift on ground, avoid slope operations beyond limits.
- If rollover begins and is recognized early: **lower collective immediately**.
- If rollover progresses beyond ~10° — may be unrecoverable.

#### Ground Resonance

Covered extensively in Module 4, Section 4.4. Emergency response:
- Nr ≥ 90% → **Full collective UP — fly**.
- Nr < 90% → **Throttles STOP — rotor brake ON — shutdown**.

---

### 7.11 DCS-Specific Emergency Modeling

| Emergency | DCS Implementation |
|-----------|-------------------|
| **Single engine failure** | Fully modeled; AI or manual trigger |
| **Dual engine failure** | Fully modeled; autorotation functional |
| **Engine fire** | Modeled; fire detection and suppression functional |
| **Hydraulic failure (main)** | Modeled; backup system activates |
| **Hydraulic failure (dual)** | Partially modeled; controls heavy |
| **Tail rotor failure** | Modeled; various failure modes |
| **Generator failure** | Modeled; bus shedding functional |
| **Gearbox failure** | Partially modeled; chip lights functional |
| **Ground resonance** | Modeled to a degree; less severe than real-world |
| **Settling with power** | Fully modeled; vortex ring dynamics functional |
| **LTE** | Modeled; specific onset may differ from real-world |

**How to Practice Emergencies in DCS:**
- **Mission Editor:** Use triggers to simulate engine failures, hydraulic failures, etc. at specific times or conditions.
- **Failure menu:** `LCtrl + F` (default) opens the failure panel for manual failure injection.
- **Training missions:** Some DCS training missions include scripted emergencies.

> *⚠ Realism Divergence: DCS emergency modeling is generally good but not perfect. Some failure modes may be simplified (e.g., gearbox seizure progression) or absent (e.g., specific electrical fire modeling). The core flight-critical emergencies (engine failure, autorotation, hydraulic failure, tail rotor failure) are well-modeled and suitable for training.*

---

### Module 7 — Instructor Notes / Common Student Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Failing to lower collective immediately on dual engine failure | Nr decays rapidly → rotor stall → unrecoverable | "The first action is ALWAYS lower collective. It must be reflexive" |
| Attempting to hover on one engine | Insufficient power → settling → crash | "Single engine = no hover. Running approach and running landing ONLY" |
| Not identifying which engine failed | Securing the wrong engine → dual engine failure | "TIT/Ng are your identification tools. The gauge going DOWN is the dead engine" |
| Panic during autorotation — pulling collective too early | Bleeds rotor energy at altitude → insufficient cushion at ground | "Trust the altitude. Collective pull is at 5–10 m, NOT at 100 m" |
| Not putting gear down for autorotation | Belly landing → aircraft damage, reduced cushion | "Gear DOWN is a critical autorotation step. Do it early" |
| Freezing during ground resonance | Destruction of aircraft | "3 seconds to act. There is no time to think. Drill the decision: fly or shut down" |
| Discharging both fire bottles simultaneously | No reserve if fire reignites | "Bottle 1 first. Wait 5 seconds. Bottle 2 only if fire persists" |
| Not declaring emergency on single engine | Delays coordination for priority landing | "Any engine failure is an emergency. Declare it. Get priority handling" |

---

## Module 8 — Approach & Landing

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Fly a standard VFR traffic pattern at the correct altitude and airspeeds.
2. Execute a running landing (the standard Mi-24P landing technique).
3. Execute a hover landing when conditions require precision placement.
4. Perform a steep approach for obstacle-rich environments.
5. Execute a go-around / wave-off from an unstable approach.
6. Manage landing gear (normal extension/retraction, emergency extension).
7. Apply crosswind corrections during approach and landing.
8. Use wheel brakes and nosewheel steering for rollout after a running landing.

---

### 8.1 VFR Traffic Pattern

The Mi-24P traffic pattern follows a standard rectangular pattern adapted for helicopter performance. Soviet convention may use **QFE** (altimeter reads zero at field elevation) for pattern altitude.

#### Pattern Parameters

| Leg | Altitude | Airspeed | Configuration | Notes |
|-----|----------|----------|--------------|-------|
| **Upwind / Departure** | Climbing through 200 m | 140–180 km/h | Gear UP | After takeoff, climbing |
| **Crosswind Turn** | 200 m (650 ft) AGL | 180 km/h | Gear UP | 90° turn to crosswind |
| **Downwind** | 200 m (650 ft) AGL | 200–220 km/h | Gear UP initially | Level, parallel to runway |
| **Abeam landing point** | 200 m | 200 km/h | **Gear DOWN** | Begin deceleration |
| **Base Turn** | Descending through 150 m | 160–180 km/h | Gear DOWN | 90° turn to base |
| **Final Approach** | Descending to field | 120–140 km/h | Gear DOWN, configured | Decelerating approach |
| **Short Final** | 50–20 m | 80–100 km/h (running) or 0–30 km/h (hover) | Gear DOWN | Landing type determines speed |

> *Note: Soviet traffic pattern convention may differ from Western (ICAO) patterns. Some Soviet airfields use left traffic; others right traffic. Pattern altitude of 200 m (660 ft) is typical for helicopters. Adapt to the specific DCS airfield.*

#### Downwind Checklist (Before turning base)

| Item | Action |
|------|--------|
| **Landing Gear** | DOWN — 3 green lights confirmed |
| **Airspeed** | Decelerating below 200 km/h |
| **Altimeter** | Set QFE (or verify QNH) |
| **Radar Altimeter** | Bug set to decision height (e.g., 50 m) |
| **Radios** | Tower frequency set, landing clearance requested |
| **Autopilot** | OFF (hand-fly the approach) |
| **Fuel** | Sufficient for approach + missed approach |
| **Weapons** | SAFE (verify) |

---

### 8.2 Running Landing (Preferred — Standard Mi-24P Arrival)

The running landing is the **standard landing technique** for the Mi-24P. It requires significantly less power than a hover landing and matches the aircraft's design intent.

#### Running Landing Procedure

| Step | Action | Parameter |
|------|--------|-----------|
| 1 | Stabilize on final approach | 120–140 km/h, 3–5° glide path, descending |
| 2 | Decelerate progressively on short final | Reduce speed to 80–100 km/h |
| 3 | Maintain descent rate at 2–3 m/s | Shallow, controlled descent |
| 4 | At ~3–5 m AGL — begin cushioning with collective | Reduce descent rate to < 1 m/s |
| 5 | **Main gear touches first** | Slight nose-up attitude; main wheels contact |
| 6 | **Lower nose** — nosewheel contacts | Smooth forward cyclic as main gear rolls |
| 7 | **Collective DOWN** — ground the aircraft | Reduce lift, weight on wheels |
| 8 | **Pedal steering** — nosewheel steering engaged | Maintain directional control |
| 9 | **Toe brakes** — apply smoothly | Progressive braking; do not lock wheels |
| 10 | Decelerate to taxi speed or stop | Taxi to parking or hold position |

**Running Landing Speeds:**

| Phase | Speed | Notes |
|-------|-------|-------|
| **Short final** | 80–100 km/h | Decelerating |
| **Touchdown** | 50–70 km/h | Ground speed at main gear contact |
| **Rollout** | 50 → 0 km/h | Braking to stop or taxi speed |

**Why Running Landing is Preferred:**
- Requires 20–30% less power than hover landing.
- Smoother touchdown — less demanding on pilot technique.
- Less exposure to LTE and settling with power.
- Natural use of the retractable landing gear.
- The aircraft's wing lift assists during the approach, reducing collective demand.

---

### 8.3 Hover Landing

Used when precision placement is required (confined area, specific parking spot, tactical LZ) and power margin permits.

#### Hover Landing Procedure

| Step | Action | Notes |
|------|--------|-------|
| 1 | Decelerate to hover on final approach | Progressive speed reduction: 120 → 80 → 50 → 0 km/h |
| 2 | As speed drops below ETL (~50 km/h), increase collective | Power demand rises rapidly |
| 3 | Establish stable hover over intended landing point | 2–3 m AGL |
| 4 | Verify power margin — torque should be < 85% | If torque > 85%, consider running landing instead |
| 5 | Slowly lower collective | Descend at < 0.5 m/s |
| 6 | Maintain position with cyclic, heading with pedals | Small corrections |
| 7 | Ground contact — lower collective to full down | Weight fully on gear |
| 8 | Cyclic neutral, pedals neutral | Aircraft settled |

**Power Requirement Warning:** At high gross weight or hot/high conditions, the Mi-24P may not have sufficient power for a hover landing. If torque exceeds 85% during the deceleration to hover, **abort and execute a running landing instead.**

---

### 8.4 Steep Approach

Used for obstacle-rich environments (trees, buildings, wires near the landing zone).

| Parameter | Value |
|-----------|-------|
| **Approach angle** | 8–12° (steeper than normal 3–5°) |
| **Entry speed** | 100–120 km/h |
| **Deceleration** | Progressive — airspeed decreases as descent steepens |
| **Power management** | Higher collective on short final to arrest descent rate |
| **Transition** | To running landing (80+ km/h) or hover (if power permits) |

**Steep Approach Technique:**

| Step | Action |
|------|--------|
| 1 | Identify obstacles and plan approach angle to clear them |
| 2 | Establish steeper descent angle (8–12°) by reducing collective more than normal |
| 3 | Maintain airspeed at 100–120 km/h — do not let speed decay below 80 km/h |
| 4 | As clearing obstacles, smoothly increase collective to arrest descent |
| 5 | Transition to running landing or hover (depending on power available) |
| 6 | Complete landing per appropriate technique |

**Caution:** A steep approach at low speed in the Mi-24P requires significant power to arrest the descent. If the descent rate exceeds 5 m/s at an airspeed below 50 km/h, the aircraft is in the settling-with-power envelope. Maintain airspeed.

---

### 8.5 Go-Around / Wave-Off

| Condition | Action |
|-----------|--------|
| **Unstable approach** (airspeed, altitude, descent rate not converging) | Go around |
| **Obstacle on runway** | Go around |
| **Power approaching limits** (torque > 90% and increasing) | Go around |
| **Loss of visual references** | Go around |
| **Windshear / turbulence on final** | Go around |

#### Go-Around Procedure

| Step | Action | Notes |
|------|--------|-------|
| 1 | **Collective UP** — apply climb power (torque 80–90%) | Arrest descent |
| 2 | **Cyclic forward** — accelerate | Gain airspeed for safe flight |
| 3 | Maintain or gain altitude | Positive climb rate established |
| 4 | At 120+ km/h — established in climb | Safe flight regime |
| 5 | **Gear** — verify DOWN or retract as appropriate | If going around for re-pattern, may keep down |
| 6 | Re-enter traffic pattern | Climb to pattern altitude, re-establish downwind |

**Decision Point:** The go-around decision should be made **no lower than 50 m AGL**. Below 50 m AGL, committing to the landing is usually safer than a go-around (risk of settling with power during low-altitude power application).

---

### 8.6 Landing Gear Management

#### Normal Extension / Retraction

| Action | Method | Indication |
|--------|--------|------------|
| **Gear DOWN** | Pilot — Gear lever DOWN | 3 green lights (nose, left main, right main) |
| **Gear UP** | Pilot — Gear lever UP | 3 green lights extinguish; gear in transit indicators |
| **Gear in transit** | — | Amber/red lights during travel |
| **Gear locked** | — | Green lights = down and locked; no light = up and locked |

> **DCS Keyboard:** `G` (default) toggles gear.

**Airspeed Limitations:**

| Action | Max Airspeed |
|--------|-------------|
| **Gear extension** | 250 km/h |
| **Gear retraction** | 250 km/h |
| **Flight with gear down** | 250 km/h (increased drag) |

#### Emergency Gear Extension

If the normal hydraulic gear system fails:

| Step | Action | Notes |
|------|--------|-------|
| 1 | Attempt normal extension first | Gear lever DOWN |
| 2 | If no green lights — **Emergency extension** | Pilot — Emergency gear handle / lever |
| 3 | Pull emergency gear release | Gear drops under gravity and air loads |
| 4 | Verify 3 green lights | Gear down and locked |
| 5 | If gear uncertain — plan for gear-up landing or running landing on main gear | Inform ATC |

> *⚠ Realism Divergence: DCS models the landing gear system including emergency extension. The specific emergency extension method (gravity drop vs. pneumatic) may be simplified in DCS. The procedure is functional.*

---

### 8.7 Crosswind Approach & Landing

| Factor | Detail |
|--------|--------|
| **Crosswind limit** | 12 m/s (23 kts) — takeoff and landing |
| **Technique** | Crab on approach → wing-low (slip) on short final → align with centerline at touchdown |
| **Pedal requirement** | Increasing pedal into wind as speed decreases |
| **LTE risk** | Crosswind from critical azimuth increases LTE risk on short final |
| **Running landing in crosswind** | Touch down main gear first; lower nose; apply into-wind brake slightly more |
| **Hover landing in crosswind** | Maintain heading with pedals; drift correction with cyclic; higher workload |

---

### 8.8 Wheel Brakes & Rollout

| Action | Technique |
|--------|-----------|
| **After main gear contact** | Hold collective to avoid full weight transfer; lower nose smoothly |
| **After nosewheel contact** | Begin braking — toe brakes progressively |
| **Differential braking** | Use individual toe brakes for directional control if needed |
| **Anti-skid** | May be modeled; if not, modulate braking to prevent wheel lock-up |
| **Parking brake** | Apply after coming to full stop at parking position |

---

### 8.9 DCS-Specific Notes

| Topic | Notes |
|-------|-------|
| **Autostart** | `LWin + Home` (default) executes automatic startup. Student must learn manual start but should understand autostart skips detailed checks and warm-up |
| **Ground friction** | DCS ground model may feel different from real-world; braking effectiveness and nosewheel authority may vary |
| **Gear interaction** | DCS models gear damage from hard landings; excessive descent rate at touchdown can collapse gear |
| **Terrain interaction** | DCS models slope and uneven terrain; be aware of dynamic rollover risk on uneven surfaces |

---

### Module 8 — Key Data Summary Table

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Pattern altitude** | 200 m (660 ft) AGL | Soviet convention; QFE preferred |
| **Downwind speed** | 200–220 km/h | Decelerating |
| **Final approach speed** | 120–140 km/h | Normal approach |
| **Running landing touchdown** | 50–70 km/h | Ground speed at contact |
| **Hover landing transition** | Below 50 km/h → hover | Power dependent |
| **Go-around decision** | ≥ 50 m AGL | Below 50 m, commit to landing |
| **Gear extension limit** | 250 km/h | Max speed for gear operation |
| **Crosswind limit** | 12 m/s (23 kts) | Hard limit |

---

### Module 8 — Instructor Notes / Common Student Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Attempting hover landing at high gross weight | Torque exceeds limits; settles into ground | "Power check: if torque > 85% at hover altitude, go running landing" |
| Not lowering gear before landing | Belly landing → aircraft damage | "Gear DOWN at the downwind abeam point. Verify 3 green lights" |
| Approaching too fast on final | Overshoots landing point; excessive float | "120–140 on final, decelerating. Not 200 km/h" |
| Approaching too slow on final | Settling with power risk; excessive torque | "Maintain at least 80 km/h until short final. Speed is safety" |
| Hard braking after running landing | Wheel lockup, loss of directional control, tire damage | "Progressive braking. Squeeze, don't stomp" |
| Not going around when approach is unstable | Dangerous landing attempt | "Below 50 m is the commit point. Above 50 m, there is ALWAYS time to go around" |
| Forgetting to disconnect autopilot for landing | AP fights pilot inputs during flare | "AP OFF before entering the pattern. Hand-fly the approach" |
| Ignoring crosswind on final | Drift into obstacles; LTE at low speed | "Wind awareness is continuous. If crosswind exceeds 12 m/s, do not attempt landing" |

---

## Module 9 — Shutdown & Securing

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Taxi the Mi-24P from the runway to a parking area using nosewheel steering and wheel brakes.
2. Perform a complete engine shutdown procedure in the correct sequence.
3. Execute a full cold-dark cockpit shutdown, securing all systems.
4. Apply the rotor brake at the correct Nr.
5. Describe post-flight checks and aircraft securing.

---

### 9.1 Taxi to Parking

After the landing rollout is complete or the aircraft has come to hover at a taxiway:

| Step | Action | Notes |
|------|--------|-------|
| 1 | Exit the runway / active | Follow ATC / taxi instructions |
| 2 | Taxi speed: 15–20 km/h (walking pace) | Mi-24P is large; be cautious near structures |
| 3 | Nosewheel steering via pedals | Keep directional control |
| 4 | Avoid sharp turns at speed | Risk of tipping with high CG |
| 5 | Use toe brakes as needed for speed control | Smooth, progressive |
| 6 | Navigate to assigned parking spot | |
| 7 | Align aircraft with parking markers / chocks | Nose into wind if possible |
| 8 | Come to a full stop | Apply wheel brakes |
| 9 | Set parking brake | Hold position |

---

### 9.2 Engine Shutdown Procedure

The Mi-24P shutdown follows a specific sequence to protect the engines and turbine components. A 2-minute cool-down period at idle is required before engine cutoff.

#### Pre-Shutdown Checks

| Step | Action | Notes |
|------|--------|-------|
| 1 | **Parking brake** — SET | Aircraft stationary |
| 2 | **Weapons** — SAFE, master arm OFF | WSO confirms all weapons safe |
| 3 | **Radar altimeter** — OFF | |
| 4 | **RSBN** — OFF | |
| 5 | **Doppler (DISS-15)** — OFF | |
| 6 | **ARK-15** — OFF | |
| 7 | **Autopilot** — OFF | All channels disengaged |
| 8 | **Exterior lights** — OFF | Anti-collision, nav, landing lights |
| 9 | **Collective** — FULL DOWN | Minimum pitch |
| 10 | **Engine RPM** — verify both at IDLE | Stabilize for cool-down |

#### Engine Cool-Down

| Step | Action | Notes |
|------|--------|-------|
| 11 | Run both engines at idle for **2 minutes** | Allows turbine temperature to stabilize |
| 12 | Monitor EGT — should decrease to < 400°C | If EGT remains high, extend idle time |

#### Engine Cutoff Sequence

**Shut down the RIGHT engine first, then the LEFT engine.**

| Step | Action | Notes |
|------|--------|-------|
| 13 | **Right engine fuel cutoff lever** — OFF (idle stop to cutoff) | Right engine spools down |
| 14 | Monitor right engine: EGT decreasing, Nr contribution dropping | Right engine winding down |
| 15 | Wait for right engine to fully stop | EGT → 0, RPM → 0 |
| 16 | **Left engine fuel cutoff lever** — OFF | Left engine spools down |
| 17 | Monitor left engine: EGT decreasing, Nr decreasing | Left engine winding down |
| 18 | Wait for left engine to fully stop | EGT → 0, RPM → 0 |

> *Note: Shutting down one engine at a time allows monitoring of each engine's spool-down independently. If an abnormality occurs (hung EGT, unusual sounds), it can be identified and addressed.*

> **DCS Shortcut:** `RShift + End` (left engine stop), `RCtrl + End` (right engine stop) — keyboard alternatives if using non-clickable controls.

---

### 9.3 Rotor Brake Application

| Step | Action | Notes |
|------|--------|-------|
| 19 | After BOTH engines are at 0% — monitor Nr | Nr decays naturally after engine shutdown |
| 20 | When Nr drops below **50%** — apply **rotor brake** | Gently — progressive application |
| 21 | Rotor brake — increase pressure progressively | Do not slam the rotor brake at high Nr |
| 22 | Rotor comes to a full stop | Nr = 0% |

**WARNING:** Do NOT apply the rotor brake above 50% Nr. Excessive braking force on a spinning rotor at high RPM can damage the rotor brake mechanism, the transmission, and the rotor hub.

> *⚠ Realism Divergence: DCS models the rotor brake but may not fully simulate rotor brake damage from premature application. Real-world Mi-24 rotor brake application requires Nr below a specific threshold (typically ~40–50%). In DCS, the rotor brake can generally be applied once Nr is decaying, but good habit is to wait for < 50%.*

---

### 9.4 Electrical & Systems Shutdown (Cold-Dark)

After engines and rotor are stopped:

#### Pilot Cockpit (Rear) — Shutdown Sequence

| Step | Action | Notes |
|------|--------|-------|
| 23 | **Cockpit lighting** — OFF | All interior lights |
| 24 | **Instrument lighting** — OFF | |
| 25 | **Pitot heat** — OFF | |
| 26 | **Fuel pumps** — OFF (all) | Fuel boost pump switches |
| 27 | **Hydraulic systems** — OFF (if switchable) | |
| 28 | **IFF/Transponder** — OFF | |
| 29 | **SPO-15 (Beryoza) RWR** — OFF | WSO may also have switch |
| 30 | **UV-26 countermeasures** — OFF and SAFE | |
| 31 | **Inverters** — OFF | AC power conversion |
| 32 | **Right generator** — OFF | |
| 33 | **Left generator** — OFF | |
| 34 | **APU generator** — OFF (if running) | |
| 35 | **APU** — OFF (if still running) | Normally APU is off after engine start |
| 36 | **Battery 2** — OFF | |
| 37 | **Battery 1** — OFF | **Last electrical item** — cockpit goes dark |

#### WSO Cockpit (Front) — Shutdown Items

| Step | Action | Notes |
|------|--------|-------|
| 38 | **Weapon systems** — all OFF and SAFE | ATGM, rockets, cannon — all switches safe |
| 39 | **PKV sight** — OFF | |
| 40 | **SPO-15 (front)** — OFF | If separate switch exists |
| 41 | **UV-26 (front)** — SAFE | |
| 42 | **Cockpit lighting** — OFF | |

> *Note: In DCS, seat switching (`1` for WSO, `2` for Pilot) may be needed to access both cockpits during shutdown. A real-world crew of two handles this simultaneously.*

---

### 9.5 Post-Flight / Securing

| Item | Action |
|------|--------|
| **Rotor** | Fully stopped, blades at rest |
| **Gear** | Down and locked (confirmed by visual or green lights before battery off) |
| **Parking brake** | SET |
| **Wheel chocks** | Placed (ground crew) |
| **Tie-downs** | Secured to rotor blade tips and fuselage (if windy conditions) |
| **Covers** | Pitot covers, intake plugs, exhaust covers (ground crew) |
| **Forms / Logbook** | Record flight time, discrepancies, maintenance items |

---

### 9.6 DCS Quick Shutdown (Autostart Off)

For training efficiency, DCS provides a quick shutdown:

| Method | Key | Effect |
|--------|-----|--------|
| **Auto shutdown** | `LShift + End` (default) | Reverses autostart; shuts down all systems |

> *This is acceptable for repositioning between training flights. Full manual shutdown must be demonstrated during evaluation.*

---

### Module 9 — Key Data Summary Table

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Cool-down idle time** | 2 minutes minimum | Protect turbine blades |
| **Shutdown order** | Right engine → Left engine | One at a time for monitoring |
| **Rotor brake application** | Nr < 50% | Do not brake above 50% |
| **Last electrical off** | Battery 1 | Final switch to dark cockpit |
| **DCS auto shutdown** | `LShift + End` | Quick method for repositioning |

---

### Module 9 — Instructor Notes / Common Student Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Skipping engine cool-down period | Thermal shock to turbine blades; shortened engine life | "2 minutes at idle. Watch the clock. Engines need to cool" |
| Applying rotor brake at high Nr | Rotor brake damage, transmission stress | "Wait for Nr below 50%. The rotor slows on its own — patience" |
| Shutting off battery before generators | Momentary electrical interruption; avionics spike | "Generators off FIRST, then batteries. Work from systems → power" |
| Leaving weapons armed during shutdown | Safety hazard; inadvertent release possible | "Weapons SAFE is the FIRST post-landing check. Always" |
| Forgetting to secure WSO cockpit | Switches left on drain residual power | "Switch to seat 1 and verify WSO cockpit cold and dark" |
| Rushing through shutdown | Missed steps; switches left on | "Shutdown is not a race. Methodical, top-to-bottom, left-to-right" |

---

## Appendix A — Master Limitations Summary

| Parameter | Limit | Units | Notes |
|-----------|-------|-------|-------|
| **VNE** | 300 | km/h | Never exceed |
| **Max speed — gear down** | 250 | km/h | |
| **Max airspeed — doors open** | 200 | km/h | If applicable |
| **Max crosswind — takeoff / landing** | 12 | m/s | |
| **Max tailwind — takeoff / landing** | 5 | m/s | |
| **Nr — normal operating range** | 92–98 | % | Target: 95% |
| **Nr — minimum (transient)** | 89 | % | Requires immediate correction |
| **Nr — autorotation range** | 89–105 | % | |
| **Max torque — continuous** | 85 | % | Per engine |
| **Max torque — transient (5 sec)** | 95 | % | Emergency only |
| **Max EGT — continuous** | 800 | °C | Per engine |
| **Max EGT — transient start** | 900 | °C | During starting only, limited time |
| **Max altitude** | 4,500 | m | Service ceiling (ISA) |
| **Max bank angle** | 60 | ° | Structural / flight manual limit |
| **Max G — positive** | +2.5 | G | Clean configuration |
| **Min G — negative** | –0.5 | G | Avoid prolonged negative G |
| **MTOW** | 11,500 | kg | Max takeoff weight |
| **Max landing weight** | 11,000 | kg | (approximate) |
| **Internal fuel capacity** | ~1,500 | kg | |
| **Min fuel for flight** | 300 | kg | Reserve / bingo |
| **Autorotation entry speed** | 170 | km/h | Optimal energy state |
| **Rotor brake application** | < 50 | % Nr | Do not brake above this Nr |
| **Engine cool-down** | 2 | minutes | At idle before shutdown |

---

## Appendix B — V-Speed Reference

| Symbol | Speed (km/h) | Speed (kts) | Description |
|--------|-------------|-------------|-------------|
| **VNE** | 300 | 162 | Never exceed speed |
| **Vmax (gear down)** | 250 | 135 | Maximum speed with gear extended |
| **Vcruise** | 220–260 | 119–140 | Normal cruise speed range |
| **Vy (best rate of climb)** | 120–140 | 65–76 | At normal gross weight |
| **Vx (best angle of climb)** | 100–110 | 54–59 | Obstacle clearance |
| **ETL (effective translational lift)** | ~50 | ~27 | Speed where translational lift develops |
| **Vautorotation** | 170 | 92 | Best glide speed in autorotation |
| **Vapproach (normal)** | 120–140 | 65–76 | Final approach speed |
| **Vrunning landing** | 50–70 | 27–38 | Ground speed at touchdown |
| **Vtaxi** | 15–20 | 8–11 | Normal taxi speed |
| **Vpattern (downwind)** | 200–220 | 108–119 | Traffic pattern downwind leg |

---

## Appendix C — Emergency Boldface Quick Reference

The following are **BOLDFACE** (memory-item, immediate action) procedures for the Mi-24P. These must be memorized verbatim.

### Single Engine Failure (In Flight)

1. **Collective — MAINTAIN Nr (95%)**
2. **Operative engine — INCREASE POWER (torque ≤ 95%)**
3. **Airspeed — 120–140 km/h (min single-engine speed)**
4. **Failed engine — IDENTIFY (EGT, torque, RPM)**
5. **Failed engine — fuel cutoff lever OFF**
6. **LAND AS SOON AS PRACTICABLE**

### Dual Engine Failure / Autorotation

1. **Collective — FULL DOWN (immediately)**
2. **Airspeed — 170 km/h**
3. **Nr — monitor (89–105% range)**
4. **Jettison stores if time permits**
5. **At 50–30 m — begin flare (raise nose)**
6. **At 5–8 m — level, COLLECTIVE PULL (cushion)**
7. **Ground contact — COLLECTIVE DOWN, cyclic neutral**

### Engine Fire (Left or Right)

1. **Affected engine — fuel cutoff lever OFF**
2. **Fire suppression — PRESS (affected engine)**
3. **If fire persists — other extinguisher bottle to affected engine**
4. **LAND IMMEDIATELY**

### Tail Rotor Failure

1. **Airspeed — 130–160 km/h** (directional control via vertical stabilizer)
2. **Avoid hover / low speed**
3. **Running landing ONLY — do not attempt to hover**
4. **Touchdown: be prepared for yaw at rollout**

---

## Appendix D — DCS Keyboard Reference (Common)

| Function | Default Key | Notes |
|----------|-------------|-------|
| **Seat — WSO (Front)** | `1` | Front cockpit |
| **Seat — Pilot (Rear)** | `2` | Rear cockpit (default spawn) |
| **Left Engine Start** | `RAlt + Home` | |
| **Right Engine Start** | `RCtrl + Home` | |
| **Left Engine Stop** | `RShift + End` | |
| **Right Engine Stop** | `RCtrl + End` | |
| **Landing Gear Toggle** | `G` | |
| **Autopilot Engage** | (binding varies) | Check DCS controls |
| **Wheel Brakes** | `W` | Hold to brake |
| **Parking Brake** | (binding varies) | |
| **Autostart** | `LWin + Home` | Automated startup sequence |
| **Auto Shutdown** | `LShift + End` | Automated shutdown sequence |
| **UV-26 Dispense** | `Insert` (default) | Countermeasures |
| **Collective Up** | `Num +` or HOTAS | |
| **Collective Down** | `Num -` or HOTAS | |

> *Note: Key bindings are DCS defaults and may vary by user configuration. Always verify in DCS Controls settings.*

---

## Appendix E — Weight & Balance Quick Reference

| Configuration | Approx Weight (kg) | Notes |
|---------------|-------------------|-------|
| **Empty weight** | ~8,500 | No fuel, no payload, no crew |
| **Operating empty** | ~8,900 | + crew, fluids, unusable fuel |
| **Internal fuel (full)** | ~1,500 | Standard internal tanks |
| **External fuel (per tank)** | ~500 | If external tanks equipped |
| **Crew (2)** | ~180 | Pilot + WSO |
| **8 × Passengers (troop transport)** | ~720 | If carrying troops |
| **Max takeoff weight (MTOW)** | 11,500 | Structural limit |
| **Typical training mission** | ~10,000–10,500 | Full fuel, no/light weapons |
| **Typical combat mission** | ~11,000–11,500 | Full fuel + weapons load |

**CG Considerations:**
- Weapons on stub wings affect lateral and longitudinal CG.
- Fuel burn shifts CG progressively as flight continues.
- Loading troops/cargo shifts CG — verify within limits.
- In DCS, weight and balance is handled by the mission editor and payload screen.

---

*Research compiled from Mi-24P RLE (Rukovodstvo po Letnoy Ekspluatatsii), technical descriptions, Mil Moscow Helicopter Plant documentation, Soviet-era flight training manuals, and Eagle Dynamics DCS World Mi-24P Hind module documentation. Where real-world sources conflict with DCS simulation behavior, DCS behavior takes precedence for checklist procedures and is noted with ⚠ Realism Divergence markers. For simulation use only.*

