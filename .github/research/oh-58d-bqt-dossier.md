# OH-58D Kiowa Warrior — Basic Qualification Training Research Dossier

> **Aircraft:** Bell OH-58D Kiowa Warrior | **Role:** Scout / Light Attack Helicopter
> **Course Level:** Basic Qualification (Level 100)
> **Primary Reference:** TM 1-1520-248-10 (Operator's Manual), TM 1-1520-248-CL (Checklists)
> **Supplementary References:** AR 95-1 (Flight Regulations), TC 3-04.4 (Fundamentals of Flight), TC 3-04.62 (Tactical Flight Procedures)
> **DCS Module:** Polychop Simulations OH-58D Kiowa Warrior — Full-fidelity, clickable cockpit module with advanced flight model (AFM).

---

## Overview

### Purpose

This document is the technical research foundation for an OH-58D Kiowa Warrior Basic Qualification Training (BQT) course in DCS World. It compiles systems knowledge, aerodynamic data, cockpit procedures, communications, and emergency procedures into a single reference that will be converted into structured, simulation-accurate checklists.

### Scope

**Covered:** Cold-and-dark startup through safe aircraft recovery in day VMC conditions — including communications setup, hover work, basic flight maneuvers, AHRS/GPS navigation, traffic pattern operations, emergency procedures (academic and practice autorotations), and shutdown.

**Not Covered:** Combat employment (weapons delivery, Hellfire engagement, close combat attack, RSTA mission tactics, team scout/attack procedures). The Mast-Mounted Sight (MMS) is introduced at a familiarization level only. Weapons panels are identified but not employed.

### Aircraft Background

The Bell OH-58D Kiowa Warrior is a single-engine, four-blade light observation and attack helicopter developed for the U.S. Army. Derived from the Bell 206 JetRanger, the OH-58D was extensively modified under the Army Helicopter Improvement Program (AHIP) with a Mast-Mounted Sight (MMS) housing TV, thermal imaging, and laser range finder/designator sensors. The "Warrior" upgrade added weapons pylons capable of carrying AGM-114 Hellfire missiles, 2.75-inch Hydra 70 rockets, AIM-92 Stinger air-to-air missiles, and the M296 .50 caliber machine gun.

Powered by a single Rolls-Royce (Allison) 250-C30R/3 turboshaft engine (military designation T703-AD-700A) producing approximately 650 shaft horsepower, the OH-58D operates at a maximum gross weight of 5,500 lbs with a Vne of 110–120 KIAS depending on configuration. The aircraft features a four-blade, soft-in-plane (bearingless) composite main rotor system and a two-blade tail rotor.

The OH-58D served as the U.S. Army's primary armed reconnaissance helicopter from the late 1980s through its retirement in 2017, operating extensively in Operations Desert Storm, Iraqi Freedom, and Enduring Freedom.

### Key Characteristics vs. Other DCS Helicopters

| Feature | OH-58D Kiowa | UH-1H Huey | Mi-24P Hind |
|---|---|---|---|
| **Rotor type** | 4-blade soft-in-plane (bearingless) | 2-blade teetering (semi-rigid) | 5-blade fully articulated |
| **Engine control** | FADEC (auto + manual backup) | Throttle correlator + governor | Manual throttle + governors |
| **Engine** | T703-AD-700A (~650 SHP) | T53-L-13B (~1,400 SHP) | 2× TV3-117V (~2,200 SHP each) |
| **Max gross weight** | 5,500 lbs | 9,500 lbs | 26,500 lbs |
| **Navigation** | AHRS/GPS + MFD moving map | ADF/VOR only (analog) | DISS + ARK-15 (analog) |
| **Cockpit** | Hybrid analog/digital (MFD) | Fully analog | Fully analog |
| **Unique risk** | Ground resonance (soft-in-plane) | Mast bumping (teetering) | Blade sailing (fully articulated) |
| **Power margin** | Very limited — light helicopter | Moderate | Generous |

### Avionics Introduction Level

The student is introduced to the MFD (Multi-Function Display), AHRS/GPS navigation system, and MMS at a **basic familiarization level** — sufficient to navigate between waypoints and understand the sensor suite's capability, but not to conduct tactical reconnaissance or weapons employment.

### Primary Real-World Sources

| Source | Description |
|---|---|
| TM 1-1520-248-10 | Operator's Manual — systems, limitations, normal/emergency procedures |
| TM 1-1520-248-CL | Operator's and Crewmember's Checklist — condensed procedures, boldface items |
| AR 95-1 | Army Flight Regulations — general operating rules |
| TC 3-04.4 | Fundamentals of Flight — rotary-wing aerodynamics, weather, ADM |
| TC 3-04.62 | Tactical Flight Procedures — terrain flight context (reference only) |
| USAACE Training Circulars | Fort Novosel training standards and maneuver descriptions |

### Source Priority Rule

Real-world documentation is the **primary truth** for systems knowledge, limitations, aerodynamic behavior, and procedural structure. Where the DCS Polychop module diverges from real-world procedures or behavior, **the DCS procedure is what the student will actually execute** and is documented as the primary instruction. All divergences are footnoted:

> *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

### Module Index

| Module | Title | Key Topics |
|---|---|---|
| 1 | Aircraft Systems & Aerodynamics | T703 engine, FADEC, rotor system, transmission, fuel, hydraulic, electrical, aero phenomena |
| 2 | Cockpit Familiarization | All panels, instruments, MFD, MMS, radios, controls, lighting |
| 3 | Communications | ARC-164 UHF, ARC-201 FM, ICS, audio panel, phraseology, DCS Easy Comm/SRS |
| 4 | Ground Operations | Cold-and-dark startup, AHRS alignment, rotor engagement, hover taxi, pre-takeoff |
| 5 | Hover & Takeoff | Hover technique, power check, takeoff profiles, climb, ground resonance |
| 6 | Basic Flight Maneuvers | Level flight, turns, climbs/descents, slow flight, autorotation practice, trim |
| 7 | Navigation (AHRS/GPS & Conventional) | MFD nav page, waypoints, moving map, TACAN, ADF, radar altimeter, transponder |
| 8 | Emergency Procedures (Academic) | Boldface items, full autorotation, LTE, VRS, FADEC failure, hydraulic, mast bumping |
| 9 | Approach & Landing | VFR pattern, normal/steep/shallow approach, go-around, slope, confined area, pinnacle |
| 10 | Shutdown & Post-Flight | Shutdown sequence, post-shutdown checks, cold-and-dark |

---

## Module 1: Aircraft Systems & Aerodynamics

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Describe the T703-AD-700A engine and its FADEC system, including auto vs. manual modes, start sequence, and engine limitations.
2. Explain the four-blade soft-in-plane (bearingless) main rotor system, its characteristics, and how it differs from teetering and fully articulated designs.
3. Identify normal operating ranges and caution/warning thresholds for all engine and transmission parameters.
4. Describe the fuel, hydraulic, and electrical systems, including emergency considerations for each.
5. Explain key rotary-wing aerodynamic phenomena: ETL, dissymmetry of lift, retreating blade stall, VRS, LTE, mast bumping, ground resonance, and dynamic rollover.
6. Identify the conditions that lead to ground resonance and state the correct immediate action.

---

### 1.1 Engine — T703-AD-700A (Rolls-Royce/Allison 250-C30R/3)

The OH-58D is powered by a single Rolls-Royce (Allison) 250-C30R/3 turboshaft engine, redesignated **T703-AD-700A** under military nomenclature. It is a free-turbine design: a gas producer section (compressor + combustor + gas producer turbine) drives a separate power turbine, which in turn drives the main transmission and rotor system through a freewheeling unit.

#### Engine Specifications

| Parameter | Value |
|---|---|
| **Type** | Free-turbine turboshaft |
| **Manufacturer** | Rolls-Royce (originally Allison) |
| **Military designation** | T703-AD-700A |
| **Commercial equivalent** | 250-C30R/3 |
| **Max rated power** | ~650 SHP (takeoff, 5 min) |
| **Max continuous power** | ~560 SHP |
| **Compressor** | 6 axial + 1 centrifugal stage |
| **Combustor** | Single reverse-flow annular |
| **Gas producer turbine** | 2-stage axial |
| **Power turbine** | 2-stage axial (free turbine) |
| **Fuel type** | JP-8 / JP-5 / Jet A-1 |
| **Engine oil** | MIL-PRF-23699 (synthetic) |
| **Dry weight** | ~160 lbs |

#### Engine Start Cycle

1. **Battery ON** — provides electrical power for FADEC and starter.
2. **FADEC self-test** — FADEC performs internal diagnostics (DCS: brief pause after battery; real-world: BIT test).
3. **Throttle to IDLE / START position** — initiates FADEC-controlled start sequence.
4. **Starter engagement** — starter-generator motors the gas producer (N1/Ng begins increasing).
5. **Fuel introduction** — FADEC introduces fuel at the appropriate N1 (~12–15% Ng). Pilot monitors TOT for light-off (visible as TOT rise on the gauge).
6. **TOT monitoring** — TOT rises through light-off, peaks, then settles. If TOT exceeds the starting limit → **HOT START** abort.
7. **N1 acceleration** — gas producer accelerates through the self-sustaining speed (~55–58% Ng). If N1 stagnates below self-sustaining with rising TOT → **HUNG START** abort.
8. **Idle stabilization** — N1 settles at ground idle (~62–65% Ng), TOT settles within continuous limits, oil pressure rising.
9. **Starter disengage** — automatic (FADEC disengages starter after self-sustaining speed reached) or manual release.

#### Start Abort Criteria

| Condition | Indication | Action |
|---|---|---|
| **Hot start** | TOT exceeds starting limit (see limits table) | Throttle to OFF immediately; motor for 30 sec to cool |
| **Hung start** | N1 stagnates below ~55% Ng with TOT rising | Throttle to OFF; motor 30 sec to purge |
| **No light-off** | No TOT rise by ~25% Ng | Throttle to OFF; motor 30 sec to clear fuel |
| **Starter duty cycle** | Exceeded continuous crank time | Throttle to OFF; wait per duty cycle limits before re-attempt |

#### Engine Operating Modes

| Mode | Description |
|---|---|
| **Ground idle** | ~62–65% Ng, Nr below flight RPM, FADEC governing at idle parameters |
| **Flight idle (FLY)** | Nr at governed flight RPM (~100% / 395 RPM), FADEC managing power to maintain Nr |
| **Continuous power** | Maximum power available without time restriction (torque ≤ continuous limit) |
| **Takeoff power (5 min)** | Maximum rated power; time-limited to 5 minutes continuous |
| **Transient (contingency)** | Above takeoff power; available momentarily — FADEC may allow brief exceedances |

#### FADEC — Full Authority Digital Engine Control

The T703-AD-700A uses a **FADEC** (Full Authority Digital Engine Control) that manages:

- **Fuel metering** — continuously adjusts fuel flow to maintain demanded power
- **Nr governing** — maintains rotor RPM at governed speed regardless of collective position
- **Torque limiting** — prevents overtorque by limiting fuel flow
- **TOT limiting** — prevents overtemperature by limiting fuel flow
- **Start sequencing** — automates fuel introduction timing and starter control during start
- **Overspeed protection** — prevents N1 and Nr from exceeding limits

**Auto mode (normal):** FADEC has full authority. Pilot moves collective; FADEC adjusts fuel to maintain Nr. Throttle twist-grip is at the FLY detent and essentially a set-and-forget control.

**Manual/Backup mode:** FADEC reverts to a degraded or backup control law. The pilot must **manually manage throttle** to maintain Nr. The collective-to-throttle correlator still provides a baseline fuel flow proportional to collective position, but the fine Nr governing is the pilot's responsibility. Handling qualities degrade — Nr will fluctuate with collective changes, and the pilot must anticipate and compensate.

**FADEC failure indications:**
- FADEC caution light on caution panel
- Nr excursions (over-speed or under-speed)
- Uncommanded power changes
- TOT excursions

> *⚠ Realism Divergence: The DCS Polychop module models FADEC auto and manual modes, but the fidelity of the backup mode may be simplified compared to the real T703 FADEC. Real-world FADEC has multiple redundancy levels and degraded modes; DCS likely models a single backup/manual mode. The start sequence in DCS is also somewhat accelerated compared to real-world turbine spool times.*

---

### 1.2 Rotor System

#### Main Rotor

| Parameter | Value |
|---|---|
| **Configuration** | 4-blade, soft-in-plane (bearingless), composite |
| **Diameter** | ~35 ft (10.7 m) |
| **Rotation direction** | Counterclockwise (viewed from above) — standard U.S. |
| **Governed RPM** | ~395 RPM (100% Nr) |
| **Normal operating range** | 97–101% Nr (383–399 RPM) |
| **Autorotation range** | ~90–107% Nr (~356–423 RPM) |
| **Blade material** | Composite (fiberglass/carbon fiber) |
| **Hub type** | Bearingless (flexures replace bearings for flap, lead-lag, and pitch change) |

The OH-58D's **bearingless (soft-in-plane)** rotor uses composite flexures instead of traditional hinges and bearings. This design:

- **Eliminates** conventional flap, lead-lag, and pitch-change bearings — reducing maintenance
- **Provides** lead-lag articulation through beam flexibility — this is what makes it "soft-in-plane"
- **Stores more rotational energy** than a 2-blade teetering system due to four blades and greater total blade mass
- **Is susceptible to ground resonance** due to the lead-lag degree of freedom (unlike a teetering rotor, which has no lead-lag articulation)

#### Tail Rotor

| Parameter | Value |
|---|---|
| **Configuration** | 2-blade, semi-rigid |
| **Location** | Left side of tail boom (pusher) |
| **Function** | Anti-torque; provides directional (yaw) control |
| **Drive** | Tail rotor driveshaft from main transmission through 90° gearbox |

#### Rotor RPM (Nr) Governing

In **FADEC auto mode**, Nr is governed automatically. The FADEC adjusts fuel flow to maintain Nr at the governed speed (~100% / 395 RPM) regardless of collective position. The pilot does not need to manage throttle.

In **FADEC manual/backup mode**, the correlator (mechanical linkage between collective and throttle) provides a proportional fuel flow, but the pilot must fine-tune with the twist-grip throttle to maintain Nr.

**Nr excursion awareness:**
- **Low Nr (below ~97%):** RPM warning audio sounds; increasing risk of blade stall and loss of rotor authority. If Nr continues to decay → autorotation entry may be required.
- **High Nr (above ~101%):** Overspeed — reduce power or increase collective to load the rotor. FADEC normally prevents this, but monitor during manual mode.
- **Autorotation Nr:** Nr will increase when collective is lowered (unloaded rotor in autorotation). Manage with collective — too much collective bleeds Nr; too little allows overspeed.

---

### 1.3 Transmission System

| Component | Description |
|---|---|
| **Main transmission** | Combines engine power turbine output to main rotor shaft; reduction gearing |
| **Tail rotor gearbox** | 90° gearbox at tail; drives tail rotor from driveshaft |
| **Freewheeling unit** | One-way clutch allowing rotor to freewheel during autorotation (disconnects from engine) |
| **Torque measurement** | Torque gauge reads main rotor drive torque (% or ft-lbs) |

#### Transmission Limits

| Parameter | Normal | Caution | Limit |
|---|---|---|---|
| **Torque (continuous)** | ≤ 85% Q | 85–100% Q | > 100% Q (structural) |
| **Torque (takeoff, 5 min)** | ≤ 100% Q | — | > 100% Q (time limit exceeded) |
| **Trans oil pressure** | 30–90 PSI | < 30 PSI | XMSN OIL PRESS caution |
| **Trans oil temperature** | < 110°C (230°F) | 110–120°C | > 120°C (248°F) |

> *Note: Torque limits may vary by block/configuration. The DCS module may use specific values — verify in-sim against the engine instrument markings and caution light trigger points.*

**Chip detector:** Metallic particles in transmission oil indicate internal wear. CHIP DET caution light → land as soon as practicable; assess severity.

---

### 1.4 Fuel System

| Parameter | Value |
|---|---|
| **Internal capacity** | ~110 US gallons (~730 lbs JP-8) |
| **Fuel cells** | Crashworthy, self-sealing bladder cells |
| **Fuel boost pump** | Electric; provides positive pressure to engine fuel system |
| **Fuel quantity indication** | Analog gauge, reading in pounds |
| **Low fuel warning** | Caution light at ~45 lbs (~6.8 gal) remaining |
| **Fuel filter bypass** | Automatic bypass if filter clogs; FUEL FILTER BYPASS caution light |
| **Typical cruise consumption** | ~200–250 lbs/hr (~30–38 gal/hr) at 80–90 KIAS |
| **Endurance (approx.)** | ~2.5–3 hours (varies with power setting, weight, altitude) |

**Fuel management notes:**
- **Always start with FUEL BOOST pump ON** — verifies fuel pressure before engine start.
- Low fuel warning triggers late — plan fuel stops conservatively.
- The OH-58D is a **short-endurance aircraft** compared to medium/heavy helicopters. Mission planning must account for limited fuel.

> *⚠ Realism Divergence: DCS fuel consumption rates may not precisely match real-world tables. Verify in-sim fuel flow at various power settings and plan missions with appropriate margin.*

---

### 1.5 Hydraulic System

| Parameter | Value |
|---|---|
| **Configuration** | Single hydraulic system |
| **Pump** | Engine-driven (runs whenever engine is turning) |
| **Pressure** | ~1,000 PSI nominal |
| **Function** | Powers irreversible flight control servo actuators (cyclic, collective, pedals) |
| **Accumulator** | Provides brief hydraulic pressure after pump failure for limited control inputs |

**Hydraulic failure:**
- Controls become **extremely heavy** — require significant pilot force to move
- Aircraft is **flyable** but demanding; avoid hover operations
- Recommended: **run-on landing** (shallow approach with forward speed at touchdown to avoid hover)
- Accumulator provides ~4–10 control inputs after pump failure — use them wisely

> *⚠ Realism Divergence: DCS may simplify hydraulic failure effects. Real-world hydraulic failure in the OH-58D requires approximately 40–50 lbs of force on the cyclic. DCS control forces may be modeled differently depending on controller hardware.*

---

### 1.6 Electrical System

| Component | Description |
|---|---|
| **Starter-generator** | 28V DC; provides starting torque and in-flight electrical generation |
| **Battery** | 24V nickel-cadmium; provides backup power and starting |
| **Essential bus** | Powers critical instruments, FADEC, caution panel, fire detection |
| **Non-essential bus** | Powers radios, MFD, lighting, non-critical avionics |
| **External power** | Receptacle for ground power unit (GPU) — used for maintenance |

**Generator failure:**
- GEN caution light illuminates
- Non-essential bus load may need to be shed
- Battery endurance: **~30 minutes** under reduced load (FADEC, essential instruments, one radio)
- Action: attempt generator reset; if unsuccessful, shed non-essential loads, land as soon as practicable

**Circuit breaker panels:** Located on both sides of the cockpit. Students should know the location of critical circuit breakers (FADEC, fuel boost, hydraulic, generator) but should **not** routinely manipulate CBs in flight except as directed by emergency procedures.

---

### 1.7 Flight Control System

| Component | Function |
|---|---|
| **Cyclic** | Tilts rotor disc — controls pitch and roll (direction of flight) |
| **Collective** | Changes all blade pitch simultaneously — controls total rotor thrust (altitude) |
| **Anti-torque pedals** | Changes tail rotor pitch — controls yaw (heading) |
| **Throttle (twist-grip)** | On collective grip — controls fuel flow; FADEC normally manages automatically |
| **Force trim** | Magnetic brake on cyclic and pedals; holds control position when set |
| **Mechanical mixing** | Collective-to-yaw coupling (left pedal with collective increase); collective-to-cyclic coupling |
| **Hydraulic boost** | Servo actuators reduce control forces to manageable levels |

**Force trim operation:**
- **Set:** Hold desired control position → press and release trim button on cyclic → controls hold position
- **Release:** Press and hold trim button → controls are free to move
- **Re-trim:** Required whenever airspeed, power, or CG changes significantly
- Force trim does **not** provide automatic stabilization — it simply holds the last-set position

**SAS/SCAS:** The real OH-58D has a limited stability augmentation system. In DCS, this may or may not be modeled. If present, it provides rate damping to reduce pilot workload in flight.

> *⚠ Realism Divergence: The DCS module may or may not fully model the OH-58D's SAS. Check in-sim whether a SAS switch exists and test its effect on handling. If not modeled, the aircraft will require more active pilot input than the real aircraft.*

---

### 1.8 Survivability Features

| Feature | Description | DCS Modeled? |
|---|---|---|
| **Crashworthy fuel cells** | Self-sealing, rupture-resistant bladder cells | Partially (fuel leak on damage) |
| **Energy-absorbing seats** | Crew seats designed to attenuate vertical crash loads | Visual only |
| **Armored crew seats** | Ballistic protection panels in seat backs | Yes (damage model) |
| **IR suppressor** | "Black Hole" exhaust system reduces IR signature | Yes (affects IR missile lock) |
| **Wire strike protection** | WSPS — cutter blades above and below cockpit | Visual only |

---

### 1.9 Rotary-Wing Aerodynamics

#### 1.9.1 Translating Tendency (Drift)

In hover, the tail rotor produces a lateral thrust (pushing the tail to the right for a counterclockwise-rotating main rotor), which causes the entire aircraft to drift **left**. The pilot compensates with a slight right cyclic input to maintain position. This is inherent to all single-rotor helicopters with counterclockwise main rotor rotation.

#### 1.9.2 Translational Lift (ETL)

As the helicopter accelerates from a hover to forward flight, it begins to fly into undisturbed air rather than re-circulating its own rotor downwash. This dramatically increases rotor efficiency.

| Phase | Airspeed | Indication |
|---|---|---|
| **ETL onset** | ~16 KIAS | Vibration increase, slight nose pitch-up tendency |
| **ETL fully developed** | ~24 KIAS | Vibration decreases, significant performance improvement, nose pitches up, left yaw tendency |

**Required control inputs through ETL:**
- **Forward cyclic** — counteract nose pitch-up
- **Right pedal** — counteract left yaw (increased torque effect)
- **Reduce collective slightly** — rotor is more efficient; less power needed for same lift

#### 1.9.3 Transverse Flow Effect

During transition through ETL, the air flowing over the rear of the rotor disc has a higher downwash angle than the front (the front encounters "fresh" air first). This creates a lateral vibration and a tendency to roll slightly right. Most pronounced at 10–20 KIAS.

#### 1.9.4 Retreating Blade Stall

At high forward airspeed, the retreating blade (moving opposite to the direction of flight) experiences reduced relative airspeed. To maintain lift equal to the advancing blade, it must increase angle of attack — eventually reaching the stall angle.

**Symptoms:** Low-frequency vibration, nose pitch-up, left roll tendency.
**Recovery:** Reduce airspeed (lower collective, aft cyclic), reduce bank angle, reduce gross weight if possible.
**Relationship to Vne:** The Vne is set partly to prevent retreating blade stall at max gross weight and G-loading.

#### 1.9.5 Dissymmetry of Lift and Flapping

The advancing blade has higher relative airspeed than the retreating blade. Without correction, this would cause a dramatic rolling moment. The rotor system compensates through **blade flapping** — the advancing blade flaps up (reducing angle of attack) and the retreating blade flaps down (increasing angle of attack). In the OH-58D's bearingless system, flapping occurs through flexure bending rather than physical hinges.

#### 1.9.6 Ground Effect (IGE vs. OGE)

| Condition | Description | Performance Impact |
|---|---|---|
| **In Ground Effect (IGE)** | Hover within ~½ rotor diameter of the ground (~17 ft for OH-58D) | Less power required; rotor downwash cushioned by ground |
| **Out of Ground Effect (OGE)** | Hover above ~1 rotor diameter from ground (~35 ft) | More power required; full rotor downwash without ground cushion |

**Practical impact:** The OH-58D is power-limited. At high density altitude or heavy gross weight, it may be possible to hover IGE but **not** OGE. The hover power check determines this.

#### 1.9.7 Settling with Power (Vortex Ring State — VRS)

Occurs when the helicopter descends into its own rotor downwash, creating a vortex ring around the rotor disc that dramatically reduces lift.

**Conditions (all three must be present):**
1. Low airspeed (< 30 KIAS)
2. High rate of descent (> 300 fpm)
3. Power applied (20–100% of available power)

**Recognition:** High rate of descent despite power application, aircraft shudder/vibration, uncontrollable sink.

**Recovery:**
1. **Forward cyclic** — gain airspeed to fly out of the vortex
2. **Reduce collective** — counterintuitive but breaks the vortex pattern
3. Requires ~100–200 ft of altitude to recover

**Prevention:** Avoid descending vertically at high rates with power applied. Maintain forward airspeed during descent whenever possible.

#### 1.9.8 Loss of Tail Rotor Effectiveness (LTE)

LTE is a reduction in tail rotor authority due to aerodynamic interference, not a mechanical failure. It results in an **uncommanded right yaw** that the pilot may not be able to counter with pedal input alone.

**Three contributing phenomena and their critical wind azimuths (relative to the nose):**

| Phenomenon | Wind Azimuth | Mechanism |
|---|---|---|
| **Main rotor vortex interference** | 285°–315° (left rear) | Main rotor tip vortices are blown into the tail rotor, disrupting its airflow |
| **Weathercock instability** | 120°–240° (rear arc) | Tailwind exceeds tail rotor authority; aircraft weathervanes |
| **Tail rotor vortex ring state** | 210°–330° (left rear arc) | Crosswind from the left causes the tail rotor to enter its own vortex ring |

**Most dangerous combined zone: ~210°–330° (left rear quadrant)**

**Recognition:** Uncommanded right yaw, inability to maintain heading despite full left pedal, increasing yaw rate.

**Recovery:**
1. **Forward cyclic** — gain airspeed (most effective cure; breaks the LTE condition)
2. **Reduce collective** — reduce torque demand on tail rotor
3. **If yaw rate becomes uncontrollable** — enter autorotation (removes all torque → removes need for tail rotor)

#### 1.9.9 Mast Bumping

Mast bumping occurs when the rotor head contacts the mast, potentially causing **catastrophic structural failure** (mast separation, loss of rotor). It is caused by excessive flapping angles under **low-G or negative-G conditions**.

**Conditions that cause low-G:**
- Abrupt forward cyclic (pushing over)
- Turbulence-induced unloading
- Aggressive cyclic inputs at low G
- Flying in the "dead man's curve" (high altitude, low airspeed)

**The OH-58D's 4-blade bearingless rotor is less susceptible** to mast bumping than the UH-1H's 2-blade teetering rotor because the bearingless flexures limit flapping more progressively. However, **low-G pushovers remain prohibited** — the risk of mast bumping still exists.

**Prevention:** Smooth control inputs. Never push forward cyclic aggressively. Avoid abrupt unloading maneuvers. Maintain positive G at all times.

**Recovery (if low-G is recognized before mast contact):** Apply **aft cyclic gently** to reload the rotor disc. **NEVER** push forward cyclic under low-G conditions.

#### 1.9.10 Dynamic Rollover

Dynamic rollover is an uncontrollable rolling motion that occurs when the helicopter pivots about a fixed skid (caught on an obstacle, slope lip, or tiedown). Once the roll rate exceeds the pilot's ability to correct with cyclic, the aircraft will roll over.

**Conditions:**
- Slope operations (upslope skid acts as pivot)
- Crosswind from the rollover direction
- Skid caught on obstacle or tiedown
- Sling load with lateral pull

**Critical roll rate:** ~10°/second — beyond this, recovery may be impossible.

**Prevention:** Slow, deliberate liftoffs on slopes. Verify skids are free before adding collective. Limit roll rate.

**Recovery (early stage only):** Reduce collective to remove the rolling moment. If roll rate is already high, reducing collective may not be sufficient.

#### 1.9.11 Ground Resonance

**Ground resonance is a critical risk for the OH-58D's soft-in-plane rotor system.** It is a self-excited oscillation that occurs when the lead-lag motion of the rotor blades couples with the natural frequency of the helicopter on its landing gear.

**Conditions:**
- Aircraft on the ground (typically hard surface)
- One skid in contact, one partially lifted (unequal weight distribution)
- Rotor system with lead-lag articulation (soft-in-plane = yes)
- Degraded lead-lag dampers

**Recognition:** Violent lateral oscillation that builds **extremely rapidly** (seconds). Distinct from normal vibration — the entire airframe shakes violently.

**Immediate action — CRITICAL DECISION:**
1. **If Nr is sufficient to fly:** FULL UP COLLECTIVE — fly away immediately. Once airborne, the landing gear is unloaded and the resonance condition breaks.
2. **If Nr is low (ground idle, spooling up, spooling down):** IMMEDIATE ENGINE SHUTDOWN — throttle to OFF. Reduce Nr as quickly as possible to decouple the rotor from the fuselage.

**Why hesitation is catastrophic:** Ground resonance can destroy the aircraft in seconds. The oscillation amplitude doubles with each cycle. There is no "wait and see" — the pilot must immediately execute one of the two actions above.

> *⚠ Realism Divergence: DCS may or may not model ground resonance for the OH-58D. If it is modeled, it may occur with different frequency or severity than real-world. Test in DCS by deliberately creating uneven ground contact conditions (slope, one skid) to determine if the phenomenon is implemented. If not modeled, the student should still understand the concept for real-world knowledge.*

---

### 1.10 Engine & Systems Limits Quick Reference

#### Engine Limits

| Parameter | Normal | Caution | Limit |
|---|---|---|---|
| **TOT (continuous)** | < 738°C (1,360°F) | 738–810°C | > 810°C |
| **TOT (takeoff, 5 min)** | ≤ 810°C (1,490°F) | — | > 810°C (time limit exceeded) |
| **TOT (starting)** | < 810°C | — | > 810°C for > 10 sec → abort |
| **N1/Ng (gas producer)** | 62–104% | — | > 104% (overspeed) |
| **Nr (rotor RPM)** | 97–101% (383–399 RPM) | 90–97% or 101–107% | < 90% / > 107% |
| **Torque (continuous)** | ≤ 85% Q | 85–100% Q | > 100% Q |
| **Torque (takeoff, 5 min)** | ≤ 100% Q | — | Exceeded: reduce immediately |
| **Engine oil pressure** | 40–130 PSI | < 40 or > 130 | < 25 PSI (critical) |
| **Engine oil temperature** | < 107°C (225°F) | 107–150°C | > 150°C (302°F) |

#### V-Speeds

| Speed | Value | Notes |
|---|---|---|
| **Vne (never exceed)** | 110–120 KIAS | Configuration-dependent (clean vs. stores); decreases with altitude |
| **Vy (best rate of climb)** | ~55–60 KIAS | Standard departure climb |
| **Cruise** | 80–100 KIAS | Best range ~90 KIAS |
| **Cruise climb** | ~80 KIAS | Enroute altitude gain |
| **Autorotation (best glide)** | ~72 KIAS | Maximum distance from altitude |
| **Autorotation (min sink)** | ~55 KIAS | Minimum rate of descent |
| **ETL (translational lift)** | 16–24 KIAS | Power demand drops significantly above ~24 KIAS |

> *Note: V-speed values are approximate and based on TM 1-1520-248-10 performance charts at standard conditions. Actual values vary with gross weight, altitude, and temperature. The DCS module may use slightly different values — verify in-sim.*

#### Aircraft Limits

| Parameter | Limit | Notes |
|---|---|---|
| **Max gross weight** | 5,500 lbs (2,495 kg) | Standard max; may be reduced at high DA |
| **Max useful load** | ~2,100–2,400 lbs | Varies with fuel and configuration |
| **Vne** | 110–120 KIAS | Configuration-dependent |
| **Low-G / Pushovers** | **PROHIBITED** | Risk of mast bumping (all rotor types) |
| **Max bank angle (normal)** | ~30° | Structural limit higher, but normal ops ≤ 30° |
| **Max bank angle (structural)** | ~60° | Emergency only |
| **Side slope limit** | ~10° | Dynamic rollover risk |
| **LTE risk azimuth** | 210°–330° relative | Avoid prolonged hover with wind from left-rear arc |

> *⚠ Realism Divergence: TOT and torque limits in the DCS OH-58D may be set to specific values that differ slightly from the -10 manual (e.g., the FADEC limiter thresholds may trip at different values). The student should observe the caution panel trigger points and gauge markings in DCS as the operative limits for simulation. The values in this table represent the real-world baseline.*

---

### 1.11 Cockpit Switch Reference — Module 1

| Switch/Control | Location | Function | DCS Action |
|---|---|---|---|
| **Battery** | Overhead console — Electrical panel | Master electrical power | Mouse click toggle |
| **Generator** | Overhead console — Electrical panel | Engages starter-generator for electrical generation | Mouse click toggle |
| **Fuel valve** | Overhead console — Fuel panel (guarded) | Opens fuel supply to engine | Lift guard, mouse click |
| **Fuel boost pump** | Overhead console — Fuel panel | Provides positive fuel pressure to engine | Mouse click toggle |
| **FADEC mode** | Overhead console — Engine panel | AUTO / MANUAL selection | Mouse click toggle |
| **Throttle** | Collective grip (twist-grip) | Controls fuel flow; IDLE → FLY detent | Axis or keyboard |
| **Idle stop release** | Collective grip (button) | Allows throttle past IDLE detent to FLY | Button press while twisting |

---

### 1.12 Instructor Notes — Module 1

**Common student errors:**

1. **Forgetting FADEC mode awareness:** Students treat the FADEC as "set and forget" and are unprepared when asked to fly manual throttle. Practice manual throttle drills early and often.
2. **Ground resonance confusion:** Students don't know the decision matrix (fly away vs. shut down based on Nr). Drill the two options repeatedly: "Nr good → fly. Nr bad → shutdown. No waiting."
3. **Overtorque on takeoff:** The OH-58D is power-limited. Students raise collective too aggressively and exceed torque limits. Emphasize smooth, gradual collective inputs.
4. **LTE surprise in hover:** Students hover with wind from the left rear and experience uncommanded right yaw. Teach wind awareness before every hover exercise.
5. **VRS entry during steep descent:** Students descend at low airspeed with power and enter VRS. Teach the three conditions (low speed, high descent, power) and how to avoid all three simultaneously.
6. **Nr management in autorotation practice:** Students fail to lower collective promptly. Emphasize: "Collective down is the first thing, every time, no exceptions."


---

## Module 2: Cockpit Familiarization

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Identify all major cockpit panels and their functions (overhead console, instrument panel, center pedestal, left/right consoles).
2. Locate and read all engine instruments (Torque, TOT, N1, Nr, fuel flow, oil P&T) and state their normal operating ranges.
3. Locate and read all flight instruments (attitude indicator, ASI, altimeter, VSI, heading indicator/HSI, turn-and-slip).
4. Identify all caution/advisory panel indicators and the master caution light.
5. Describe the MFD pages at a basic level (NAV, ENG, SYS) and operate the OSB buttons.
6. Identify the MMS controller and weapon panel at familiarization level.
7. Identify radio control heads (ARC-164 UHF, ARC-201 FM) and the audio panel/ICS.
8. Describe the HOTAS functions on the collective grip (throttle, idle stop, radio triggers, lights) and cyclic grip (force trim, weapons release).

---

### 2.1 Cockpit Layout Overview

The OH-58D cockpit is a tandem-style (side-by-side) arrangement with the **pilot in the right seat** and the **copilot/observer in the left seat**. The cockpit features a mix of analog instruments and digital avionics.

```
┌─────────────────────────────────────────────────────────────┐
│                    OVERHEAD CONSOLE                          │
│  [BATT] [GEN] [FUEL VLV] [BOOST PMP] [FADEC] [STARTER]    │
│  [PITOT HT] [ANTI-ICE] [RPM WARN] [CAUTION TEST]          │
│  [EXTERIOR LIGHTS] [COCKPIT LIGHTS]                         │
├──────────────────────┬──────────────────────────────────────┤
│   COPILOT PANEL (L)  │         PILOT PANEL (R)              │
│  ┌───┐ ┌───┐ ┌───┐  │  ┌───┐ ┌───┐ ┌───┐                  │
│  │ATT│ │ASI│ │ALT│  │  │ATT│ │ASI│ │ALT│                  │
│  └───┘ └───┘ └───┘  │  └───┘ └───┘ └───┘                  │
│  ┌───┐ ┌───┐ ┌───┐  │  ┌───┐ ┌───┐ ┌───┐                  │
│  │VSI│ │HSI│ │T&S│  │  │VSI│ │HSI│ │T&S│                  │
│  └───┘ └───┘ └───┘  │  └───┘ └───┘ └───┘                  │
│  ┌─────────────────────────────────────┐                    │
│  │  ENGINE INSTRUMENTS (CENTER)         │                    │
│  │  [TRQ %Q] [TOT °C] [N1 %] [Nr %]  │                    │
│  │  [FUEL FLOW] [ENG OIL P/T]         │                    │
│  │  [XMSN OIL P/T]                    │                    │
│  └─────────────────────────────────────┘                    │
│  ┌───────────────┐  ┌─────────────────┐                    │
│  │ CAUTION PANEL │  │   FUEL QTY      │                    │
│  └───────────────┘  └─────────────────┘                    │
├──────────────────────────────────────────────────────────────┤
│                    CENTER PEDESTAL                            │
│  [ARC-164 UHF-AM]  [ARC-201 VHF/FM]  [AUDIO PANEL / ICS]  │
│  [TRANSPONDER]                                               │
├──────────────────────────────────────────────────────────────┤
│                    MFD (Multi-Function Display)               │
│  ┌────────────────────────────────────┐                      │
│  │ [OSB 1] [OSB 2] [OSB 3] [OSB 4]  │                      │
│  │                                    │                      │
│  │      NAV / ENG / WPN / SYS        │                      │
│  │                                    │                      │
│  │ [OSB 5] [OSB 6] [OSB 7] [OSB 8]  │                      │
│  └────────────────────────────────────┘                      │
├──────────────────────────────────────────────────────────────┤
│         MMS CONTROLLER (Copilot side, pilot accessible)      │
│  [TV/FLIR select] [Zoom] [Slew] [Laser] [FOV]              │
└──────────────────────────────────────────────────────────────┘
```

---

### 2.2 Overhead Console

The overhead console is located above both crew members and contains the primary systems switches for engine starting, electrical power, fuel management, and lighting.

| Panel / Group | Switches | Function |
|---|---|---|
| **Electrical panel** | BATT, GEN, INVERTER | Master electrical power, generator, AC power |
| **Fuel panel** | FUEL VALVE (guarded), FUEL BOOST PUMP | Fuel supply to engine, fuel pressure |
| **Engine panel** | FADEC MODE (AUTO/MANUAL), STARTER, RPM WARN | Engine control mode, starting, RPM audio warning |
| **Environmental** | PITOT HEAT, ENGINE ANTI-ICE, DEFOG | Anti-ice and defogging systems |
| **Lighting** | COCKPIT LIGHTS (rheostat), INSTRUMENT LIGHTS, CONSOLE LIGHTS | Interior lighting for day/night/NVG |
| **Caution test** | CAUTION TEST button | Tests all caution panel bulbs |

---

### 2.3 Instrument Panel

#### Pilot's Flight Instruments (Right Side)

| Instrument | Location | Reading | Normal Range |
|---|---|---|---|
| **Attitude indicator** | Center of pilot's T-panel | Pitch and bank attitude | Wings level, nose on horizon = level flight |
| **Airspeed indicator (ASI)** | Left of attitude indicator | Indicated airspeed (KIAS) | 0–120+ KIAS; Vne marked |
| **Barometric altimeter** | Right of attitude indicator | Pressure altitude (ft MSL) | Kollsman window set to current QNH |
| **Vertical speed indicator (VSI)** | Below airspeed indicator | Rate of climb/descent (ft/min) | 0 in level flight; ± 500-1500 normal |
| **Heading indicator / HSI** | Below attitude indicator | Magnetic heading; course deviation | Aligned to magnetic compass; heading bug settable |
| **Turn-and-slip indicator** | Below altimeter | Rate of turn; slip ball coordination | Ball centered = coordinated flight |

**The slip ball is critical** — it indicates coordinated flight and is a primary indicator of tail rotor failure (ball will be displaced and unable to be centered).

#### Engine Instruments (Center Panel)

| Instrument | Parameter | Normal Range | Caution | Limit |
|---|---|---|---|---|
| **Torque gauge (Q)** | Rotor drive torque (% Q) | ≤ 85% | 85–100% | > 100% |
| **TOT gauge** | Turbine outlet temp (°C) | < 738°C | 738–810°C | > 810°C |
| **N1 / Ng gauge** | Gas producer speed (%) | 62–104% | — | > 104% |
| **Nr / N2 dual tach** | Rotor RPM and engine RPM (%) | 97–101% Nr | < 97% or > 101% | < 90% / > 107% |
| **Fuel flow** | Engine fuel consumption (lbs/hr) | 150–350 typical | — | — |
| **Engine oil P** | Engine oil pressure (PSI) | 40–130 | < 40 / > 130 | < 25 |
| **Engine oil T** | Engine oil temperature (°C) | < 107°C | 107–150°C | > 150°C |
| **Trans oil P** | Transmission oil pressure (PSI) | 30–90 | < 30 | XMSN caution |
| **Trans oil T** | Transmission oil temperature (°C) | < 110°C | 110–120°C | > 120°C |
| **Fuel quantity** | Fuel remaining (lbs) | Mission-dependent | ~100 lbs (plan RTB) | ~45 lbs (LOW FUEL caution) |

**Dual tachometer (Nr/N2):** Two needles on one instrument — the outer needle reads Nr (rotor RPM), the inner needle reads N2 (power turbine/engine output RPM). In normal governed flight, both needles should be "married" (overlapping). Splitting indicates governor/FADEC issue or autorotation condition.

---

### 2.4 Caution / Advisory Panel

The caution panel is a central annunciator with individual segment lights for each system. A **master caution light** illuminates whenever any caution indicator activates.

| Indicator | System | Meaning |
|---|---|---|
| **MASTER CAUTION** | All systems | Any caution active — check panel for specific indicator |
| **ENGINE OIL** | Engine | Oil pressure low or temperature high |
| **XMSN OIL** | Transmission | Trans oil pressure low or temperature high |
| **FUEL BOOST** | Fuel | Fuel boost pump pressure low |
| **FUEL FILTER** | Fuel | Fuel filter bypassed (clogged filter) |
| **LOW FUEL** | Fuel | Fuel quantity below ~45 lbs |
| **FADEC** | Engine | FADEC malfunction or degraded mode |
| **GEN** | Electrical | Generator offline or failure |
| **CHIP DET** | Transmission | Metallic particles in transmission oil |
| **HYD** | Hydraulic | Hydraulic pressure low |
| **FIRE** | Fire detection | Engine compartment fire detection |
| **RPM** | Rotor | Nr outside normal range (low or high) |
| **GOV** | Engine | Governor/FADEC governing anomaly |

**Master caution reset:** Press master caution light to acknowledge and reset. If the condition persists, the master caution will re-illuminate.

---

### 2.5 MFD (Multi-Function Display)

The MFD is a color display (or monochrome in some configurations) located on the instrument panel, operated by **OSB (Option Select Buttons)** around the bezel.

#### MFD Pages

| Page | Function | Key Information Displayed |
|---|---|---|
| **NAV** | Navigation | Moving map, waypoints, bearing/distance/ETA, aircraft position, heading |
| **ENG** | Engine monitoring | Digital readout of TRQ, TOT, N1, Nr, fuel flow, oil P/T — supplements analog gauges |
| **WPN** | Weapons | Weapon inventory, arming status, selected weapon — **familiarization only** |
| **SYS** | Systems status | Electrical, hydraulic, fuel system status summary |
| **FLT** | Flight data | Airspeed, altitude, heading in digital format |

#### MFD Operation

- **Power on:** Controlled by avionics master or dedicated MFD switch; MFD goes through a boot sequence after power is applied.
- **Page selection:** Press OSB buttons labeled for each page. Pages cycle or are directly selectable.
- **Brightness:** Adjustable via control — important for day/night/NVG operations.
- **OSB nomenclature:** Buttons are numbered around the bezel; specific labels change per page.

> *⚠ Realism Divergence: The DCS Polychop MFD implementation may not include all real-world pages or may have simplified page content. The navigation page and engine page are the most critical for BQT; verify their functionality in-sim.*

---

### 2.6 MMS (Mast-Mounted Sight) — Familiarization Only

The Mast-Mounted Sight is a sensor ball mounted **above the main rotor head** on a mast. This allows the OH-58D to observe targets while the aircraft body remains hidden behind terrain (hull-defilade).

| Sensor | Function |
|---|---|
| **TV (daylight)** | Daylight television camera; zoom capability |
| **FLIR (thermal)** | Forward-looking infrared; detects heat signatures; usable day/night |
| **Laser rangefinder** | Measures distance to target (slant range) |
| **Laser designator** | Designates targets for laser-guided munitions (Hellfire, etc.) |

**MMS controller:** Located primarily on the copilot side, but the pilot can access basic MMS controls through the cyclic grip or MFD interface. For BQT, the student only needs to:
- Know what the MMS is and where it is
- Understand its basic sensor modes (TV, FLIR, laser)
- Know that tactical sensor employment is a separate course

---

### 2.7 Weapon Panel — Identification Only

| Control | Location | Function |
|---|---|---|
| **Master ARM / SAFE** | Weapon panel (instrument panel or console) | Arms or safes all weapons systems |
| **Weapon select** | Weapon panel | Selects active weapon type (Hellfire, rockets, .50 cal, Stinger) |
| **Weapon quantity** | MFD WPN page or panel counters | Shows remaining ordnance |

**For BQT:** The student identifies the location of the weapon panel and knows that MASTER ARM must be in SAFE for all non-weapons training. No weapons employment procedures are taught.

---

### 2.8 Center Pedestal — Radios

| Radio | Designation | Type | Frequency Range | Primary Use |
|---|---|---|---|---|
| **UHF-AM** | ARC-164 | UHF amplitude modulation | 225.000–399.975 MHz | ATC communications, common frequencies, guard (243.0 MHz) |
| **VHF/FM** | ARC-201 | VHF frequency modulation | 30.000–87.975 MHz | Tactical/inter-flight communication, ground coordination |

**ARC-164 (UHF-AM):**
- Manual tune: frequency selector knobs
- Preset channels: selectable via channel knob (up to 20 presets, mission-dependent)
- Guard (243.0 MHz): selectable via GUARD position — monitors emergency frequency
- Mode: OFF / MAIN / BOTH / ADF

**ARC-201 (VHF/FM):**
- Frequency selection: knobs or preset channels
- Used primarily for tactical communications between flight members or with ground units
- Manual tune or preset modes available

**Audio panel / ICS:** Controls which radio(s) the pilot hears and transmits on. Volume controls for each radio and ICS. ICS (intercom) connects pilot and copilot for crew coordination.

> *⚠ Realism Divergence: The real OH-58D may have additional radio systems (e.g., SINCGARS, Have Quick II) not modeled in DCS. The DCS module provides the ARC-164 and ARC-201 as the primary radios. SRS (SimpleRadio Standalone) may be required for multiplayer radio fidelity.*

---

### 2.9 AHRS/GPS Navigation System

The OH-58D features an **Attitude Heading Reference System (AHRS)** coupled with a **GPS receiver**, providing:

| Capability | Description |
|---|---|
| **Position** | Accurate lat/long from GPS; displayed on MFD NAV page |
| **Heading** | AHRS-derived magnetic heading; more accurate than a magnetic compass alone |
| **Waypoint navigation** | Pre-programmed or pilot-entered waypoints; bearing, distance, and ETA displayed |
| **Moving map** | MFD NAV page displays aircraft position on a map with configurable scale and orientation |
| **Ground speed / track** | GPS-derived ground speed and track over ground |

**Alignment:** The AHRS requires an alignment period after power-on. The aircraft must be **stationary** during alignment. Alignment quality improves with time; a minimum quality is required before navigation data is reliable.

---

### 2.10 Radar Altimeter

| Feature | Description |
|---|---|
| **Function** | Measures absolute altitude above ground level (AGL) using radar |
| **Range** | Typically 0–1,500 ft AGL |
| **Low-altitude warning** | Adjustable bug; audio/visual warning when descending below set altitude |
| **Usage** | Critical during hover, low-level flight, and approach to landing |

**Setting:** Rotate the bug to the desired warning altitude. The warning light and/or audio will activate when the aircraft descends below that altitude.

---

### 2.11 Pilot Controls — Collective and Cyclic

#### Collective Grip

| Control | Location | Function |
|---|---|---|
| **Throttle (twist-grip)** | Outboard end of collective grip | Controls fuel flow; FADEC manages in auto mode; detents: OFF → IDLE → FLY |
| **Idle stop release** | Button on collective grip | Must press to advance throttle past IDLE to FLY |
| **Landing light switch** | Collective grip | Extends/retracts and on/off for landing/taxi light |
| **Searchlight control** | Collective grip | Extends/retracts and controls searchlight direction |
| **Radio trigger** | Collective grip (front) | 1st detent = ICS (intercom); 2nd detent = selected radio transmit |

#### Cyclic Grip

| Control | Location | Function |
|---|---|---|
| **Force trim release** | Button on cyclic grip | Press and release = set trim; press and hold = free controls |
| **Weapons release** | Cyclic grip (front) | Fires selected weapon (when armed) — **BQT: not used** |
| **MMS slew** | Cyclic grip or thumb controller | Slews MMS sensor — **BQT: familiarization only** |

#### Pedals

| Control | Function |
|---|---|
| **Anti-torque pedals** | Left pedal = increase tail rotor thrust (counter torque at high power); Right pedal = decrease tail rotor thrust |
| **Adjustment** | Fore/aft pedal position adjustable for pilot leg length |

---

### 2.12 Lighting

| Category | Controls | Notes |
|---|---|---|
| **Instrument lights** | Rheostat on overhead console | Adjusts panel/gauge illumination intensity |
| **Console lights** | Rheostat on overhead console | Illuminates switch panels |
| **Dome light** | Switch on overhead or side panel | White light for map reading; **off during NVG ops** |
| **Position/nav lights** | Switch on overhead console | Standard red/green/white navigation lights |
| **Anti-collision beacon** | Switch on overhead console | Red flashing beacon; on during flight |
| **Landing light** | Collective grip switch | Retractable; extends and illuminates for landing/taxi |
| **Searchlight** | Collective grip control | Retractable; steerable; for search/illumination |
| **IR formation lights** | Switch on overhead or lighting panel | Infrared lights visible under NVG; for formation flight |

**NVG compatibility:** The OH-58D cockpit is designed for ANVIS (Aviator Night Vision Imaging System) NVG operations. Instrument lighting can be dimmed to NVG-compatible levels. White lights (dome light, flashlights) must be **off** during NVG flight.

---

### 2.13 Cockpit Switch Reference — Module 2

| Switch/Control | Location | Function | DCS Action |
|---|---|---|---|
| **Attitude indicator** | Instrument panel — pilot's T | Pitch/bank reference | Read only; cage/uncage knob |
| **Altimeter Kollsman** | Instrument panel — altimeter | Set barometric pressure (QNH) | Mouse scroll on knob |
| **Heading bug** | HSI — heading indicator | Set desired heading | Mouse scroll on knob |
| **Radar altimeter bug** | Radar altimeter | Set low-altitude warning | Mouse scroll on knob |
| **MFD power** | Avionics panel or MFD bezel | Powers on MFD | Mouse click |
| **MFD OSB buttons** | MFD bezel (surrounding display) | Page/function selection | Mouse click on specific OSB |
| **MFD brightness** | MFD bezel (knob) | Adjust display brightness | Mouse scroll |
| **Caution test** | Overhead console | Tests all caution panel bulbs | Mouse click (hold) |
| **Master caution reset** | Caution panel (glare shield) | Acknowledges/resets master caution | Mouse click |
| **Radio trigger** | Collective grip | ICS (1st detent) / Radio TX (2nd detent) | Keyboard or joystick button |
| **Force trim** | Cyclic grip button | Set/release trim | Keyboard or joystick button |

---

### 2.14 Instructor Notes — Module 2

**Common student errors:**

1. **Ignoring the slip ball:** Students focus on the attitude indicator and heading indicator but neglect the turn-and-slip ball. Emphasize: "Ball centered = coordinated. Ball displaced = cross-controlled or tail rotor issue."
2. **MFD page confusion:** Students cycle through MFD pages randomly. Teach a systematic page-selection workflow: NAV for transit, ENG for monitoring, SYS for status checks.
3. **Dual tachometer misread:** Students confuse Nr (outer needle) with N2 (inner needle). Drill needle identification until it is automatic.
4. **Radio trigger detent confusion:** Students key the wrong detent (ICS when they mean radio, or vice versa). Practice the trigger feel — 1st detent is a "half-pull" for crew, 2nd detent is a full pull for radio.
5. **Forgetting Kollsman setting:** Students launch with a default altimeter setting and wonder why their altitude doesn't match the field elevation. Make altimeter setting part of the pre-takeoff checklist muscle memory.
6. **Not using the radar altimeter:** Students rely on barometric altitude for hover and low-level work. Teach radar altimeter as the primary altitude reference below 200 ft AGL.


---

## Module 3: Communications

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Identify and operate the OH-58D's radio systems: ARC-164 (UHF-AM) and ARC-201 (VHF/FM).
2. Tune frequencies manually on each radio using the control head knobs.
3. Configure the audio panel to select transmit and receive radios.
4. Operate the ICS (intercom) system for crew communication, including hot mic and trigger-keyed modes.
5. Use the collective radio trigger correctly (1st detent = ICS, 2nd detent = radio transmit).
6. Make standard radio calls for all phases of BQT flight: startup, taxi, takeoff, pattern, approach, landing, shutdown.
7. Monitor guard frequency (UHF 243.0 MHz).
8. Understand the difference between DCS Easy Communication and realistic radio operation.

---

### 3.1 Radio Systems Overview

The OH-58D is equipped with two primary radios and an intercom system:

| System | Designation | Type | Frequency Range | Primary Role |
|---|---|---|---|---|
| **UHF-AM** | AN/ARC-164 | UHF Amplitude Modulation | 225.000–399.975 MHz | ATC communications, common/tower frequencies, guard (243.0 MHz) |
| **VHF/FM** | AN/ARC-201 | VHF Frequency Modulation | 30.000–87.975 MHz | Tactical inter-flight communications, ground coordination |
| **ICS** | Intercom | Wired intercom | N/A | Pilot-to-copilot crew coordination |

**General radio doctrine:**
- **UHF-AM (ARC-164)** is the primary radio for communicating with ATC (tower, approach, departure, ground control) and for common tactical frequencies. UHF-AM is the standard military aviation band.
- **VHF/FM (ARC-201)** is used for tactical inter-flight communication (flight lead to wingman), coordination with ground forces, and SINCGARS-compatible networks (in real-world; DCS may simplify).
- **ICS** is used for all crew communication within the cockpit — callouts, confirmations, warnings, and coordination.

---

### 3.2 ARC-164 (UHF-AM) — Detailed Operation

| Feature | Description |
|---|---|
| **Frequency range** | 225.000–399.975 MHz (25 kHz spacing) |
| **Modes** | OFF / MAIN / BOTH / ADF |
| **Preset channels** | Up to 20 presets (mission-programmable) |
| **Guard frequency** | 243.0 MHz — international UHF emergency frequency |
| **GUARD/MAIN+GUARD** | BOTH mode monitors guard simultaneously with main frequency |
| **Squelch** | Adjustable; reduces background noise |

#### Tuning the ARC-164

**Manual tune:**
1. Ensure mode is set to MAIN (or BOTH for simultaneous guard monitoring).
2. Use the frequency selector knobs to set desired frequency (MHz on the left knob, kHz on the right knob).
3. Verify frequency displayed in the window matches desired frequency.

**Preset channels:**
1. Select PRESET mode on the control head.
2. Rotate channel selector to the desired preset number.
3. The radio automatically tunes to the pre-programmed frequency for that channel.

**Guard monitoring (recommended):**
- Set mode to BOTH — this monitors 243.0 MHz (guard) simultaneously with the selected main frequency.
- Guard is the emergency frequency — all aircraft should monitor it when possible.

#### Common UHF Frequencies (DCS)

| Frequency | Use |
|---|---|
| **243.0 MHz** | Guard (emergency) |
| **251.0 MHz** | Common UHF air-to-air |
| **253.0 MHz** | DCS common ground/tower (varies by mission) |
| **275.8 MHz** | AWACS / GCI (common in DCS MP) |
| **Mission-specific** | Per briefing — tower, approach, departure, JTAC |

> *Note: DCS frequencies are mission-dependent. The student should check the mission briefing for assigned frequencies before startup.*

---

### 3.3 ARC-201 (VHF/FM) — Detailed Operation

| Feature | Description |
|---|---|
| **Frequency range** | 30.000–87.975 MHz (25 kHz spacing) |
| **Modes** | OFF / SC (single channel) / FH (frequency hopping) |
| **Usage** | Tactical/inter-flight communication, ground forces coordination |
| **SINCGARS compatible** | Real-world: yes (frequency hopping). DCS: simplified — typically single-channel mode only |

#### Tuning the ARC-201

**Single channel (SC) mode:**
1. Set mode to SC.
2. Use frequency selector knobs to set desired frequency.
3. Verify frequency displayed matches desired frequency.

**Frequency hopping (FH):** Real-world SINCGARS uses a shared crypto key and hopping pattern. In DCS, this is typically not modeled — use single-channel mode.

#### Common FM Frequencies (DCS)

| Frequency | Use |
|---|---|
| **30.0 MHz** | Common FM default |
| **40.0 MHz** | Inter-flight coordination (common in DCS) |
| **Mission-specific** | Per briefing — JTAC, FAC, ground forces |

---

### 3.4 Audio Panel / ICS

The audio panel controls which radio(s) the pilot hears and transmits on.

| Control | Function |
|---|---|
| **UHF volume** | Adjusts ARC-164 receive volume in the pilot's headset |
| **FM volume** | Adjusts ARC-201 receive volume in the pilot's headset |
| **ICS volume** | Adjusts intercom volume |
| **Transmit select** | Selects which radio the radio trigger (2nd detent) transmits on: UHF or FM |
| **ICS mode** | Hot mic (always transmitting on ICS) or keyed (trigger 1st detent to transmit on ICS) |

#### Transmit/Receive Configuration

**Typical BQT setup:**
- **Transmit:** UHF (ARC-164) selected for ATC communications
- **Receive:** Both UHF and FM volumes up (monitor both)
- **ICS:** Hot mic for crew coordination (or keyed if preferred)

**Changing transmit radio:**
- Use the transmit select switch on the audio panel to toggle between UHF and FM
- When switching to talk on FM (e.g., to a wingman), select FM as transmit radio, make the call, then switch back to UHF for ATC

---

### 3.5 Intercom (ICS) System

The ICS connects pilot and copilot for crew communication without transmitting on any radio.

| Mode | Description |
|---|---|
| **Hot mic** | Both crew members hear each other at all times — no trigger press needed |
| **Keyed** | Must press radio trigger to 1st detent to speak on ICS |
| **Recommended for BQT** | Hot mic — reduces workload during training, especially in hover and emergency practice |

**Collective trigger positions:**
- **1st detent (partial squeeze):** ICS only — crew communication
- **2nd detent (full squeeze):** Selected radio transmit — broadcasts on UHF or FM (per transmit select)

**Keying technique:** The trigger is a graduated squeeze. The student must develop muscle memory to distinguish between:
- A light squeeze (1st detent) for talking to the copilot
- A full squeeze (2nd detent) for transmitting on the radio

**Common error:** Accidentally transmitting on the radio when intending to speak on ICS (squeezing too hard), or speaking on ICS when intending to transmit (not squeezing enough). This can result in unintended radio transmissions or missed calls.

---

### 3.6 Standard Radio Calls — BQT Environment

The following are standard radio calls the student must be able to make during BQT training flights.

#### ATC Communication (UHF-AM)

| Phase | Call | Example |
|---|---|---|
| **Startup clearance** | "[Ground/Tower], [Callsign], [Location], request startup" | "Batumi Ground, Army Kiowa 16, ramp parking, request startup and ATIS information" |
| **Taxi** | "[Ground], [Callsign], request hover taxi [destination]" | "Batumi Ground, Kiowa 16, request hover taxi to runway 13 via taxiway Alpha" |
| **Takeoff** | "[Tower], [Callsign], ready for departure [runway/direction]" | "Batumi Tower, Kiowa 16, holding short runway 13, ready for departure to the south" |
| **Departure** | "[Tower/Departure], [Callsign], departing [direction], climbing [altitude]" | "Batumi Tower, Kiowa 16, departing south, climbing to pattern altitude" |
| **Pattern entry** | "[Tower], [Callsign], entering [position] for runway [number]" | "Batumi Tower, Kiowa 16, entering left downwind runway 13" |
| **Base turn** | "[Tower], [Callsign], turning base" | "Batumi Tower, Kiowa 16, turning base runway 13" |
| **Final** | "[Tower], [Callsign], final runway [number], [type] landing" | "Batumi Tower, Kiowa 16, final runway 13, full stop" |
| **Go-around** | "[Tower], [Callsign], going around" | "Batumi Tower, Kiowa 16, going around" |
| **Landing clearance** | Listen for "[Callsign], cleared to land runway [number]" | Respond: "Cleared to land runway 13, Kiowa 16" |
| **Taxi after landing** | "[Ground], [Callsign], clear of runway [number], request taxi to parking" | "Batumi Ground, Kiowa 16, clear runway 13, request taxi to ramp" |
| **Shutdown** | "[Ground], [Callsign], parking, shutting down" | "Batumi Ground, Kiowa 16, ramp parking, shutting down" |

#### Inter-Flight Communication (FM)

| Situation | Call | Example |
|---|---|---|
| **Check-in** | "[Callsign], up [frequency]" | "Kiowa 16, up Button 3" |
| **Position report** | "[Callsign], [position], [altitude], [heading]" | "Kiowa 16, 5 miles south, 1000 feet, heading north" |
| **Tactical** | Military brevity as appropriate | Per unit SOP |

#### Phraseology Notes

- **Readback required:** Runway assignments, altimeter settings, hold short instructions, clearance limits
- **"Roger"** = received and understood (not agreement)
- **"Wilco"** = will comply
- **"Say again"** = repeat last transmission
- **"Unable"** = cannot comply with instruction
- **"Mayday"** (×3) = emergency distress call on guard or current frequency

---

### 3.7 Guard Frequency Monitoring

| Frequency | Band | Purpose |
|---|---|---|
| **243.0 MHz** | UHF | International military emergency frequency |
| **121.5 MHz** | VHF | International civil emergency frequency |

**Best practice:** Monitor guard (243.0 MHz) on UHF by setting ARC-164 to BOTH mode. This allows simultaneous monitoring of main frequency and guard.

If an emergency is heard on guard, relay to appropriate ATC if able. If declaring an emergency yourself, transmit on guard and current ATC frequency.

---

### 3.8 DCS-Specific Radio Operations

#### Easy Communication Mode

DCS offers an **Easy Communication** mode that simplifies radio operation:
- Radio menus appear via keyboard shortcut (default: `\` backslash)
- No need to tune frequencies or configure audio panels
- ATC responses are automatic
- **Not recommended for BQT** — students should learn realistic radio operation

#### Realistic Radio Mode

With Easy Communication **off**, the student must:
1. Tune the correct frequency on the appropriate radio
2. Select the correct radio for transmit on the audio panel
3. Key the radio trigger (2nd detent) to transmit
4. Listen for responses on the tuned frequency

#### SRS (SimpleRadio Standalone)

For multiplayer operations, **SRS** provides realistic radio simulation:
- Radios must be tuned to communicate with other players
- Transmissions are proximity- and frequency-dependent
- ICS works between crew members
- Separate software installation required; integrates with DCS cockpit radios

> *⚠ Realism Divergence: In single-player DCS with Easy Communication off, ATC interactions are still somewhat scripted/simplified compared to real-world radio procedures. SRS in multiplayer provides the most realistic radio experience but requires additional setup. The student should be proficient with cockpit radio operation regardless of communication mode.*

---

### 3.9 Cockpit Switch Reference — Module 3

| Switch/Control | Location | Function | DCS Action |
|---|---|---|---|
| **ARC-164 mode** | Center pedestal — UHF control head | OFF / MAIN / BOTH / ADF | Mouse click to cycle |
| **ARC-164 frequency** | Center pedestal — UHF control head | MHz and kHz selector knobs | Mouse scroll on each knob |
| **ARC-164 preset channel** | Center pedestal — UHF control head | Select preset channel number | Mouse scroll on channel knob |
| **ARC-164 volume** | Center pedestal — UHF control head or audio panel | UHF receive volume | Mouse scroll |
| **ARC-201 mode** | Center pedestal — FM control head | OFF / SC / FH | Mouse click to cycle |
| **ARC-201 frequency** | Center pedestal — FM control head | Frequency selector knobs | Mouse scroll on each knob |
| **ARC-201 volume** | Center pedestal — FM control head or audio panel | FM receive volume | Mouse scroll |
| **Audio panel — TX select** | Center pedestal — audio panel | Select UHF or FM for transmit | Mouse click toggle |
| **Audio panel — ICS mode** | Center pedestal — audio panel | Hot mic or keyed | Mouse click toggle |
| **Radio trigger** | Collective grip | 1st detent: ICS / 2nd detent: radio TX | Joystick button or keyboard |

**Keyboard defaults (DCS — verify in-sim):**

| Key | Function |
|---|---|
| `RAlt + \` | UHF transmit (Easy Comm menu) |
| `RCtrl + \` | VHF/FM transmit (Easy Comm menu) |
| `\` | Easy Comm menu (if enabled) |

> *Note: Actual key binds may differ by DCS version and user configuration. Always verify in Controls settings.*

---

### 3.10 Instructor Notes — Module 3

**Common student errors:**

1. **Wrong trigger detent:** Students transmit on radio when they meant ICS, or talk on ICS when they meant to transmit. Drill the trigger feel repeatedly. Use the callout "ICS check" and "Radio check" to practice.
2. **Forgetting to switch transmit radio:** Students call ATC on FM instead of UHF (or vice versa). Teach a workflow: before every transmission, glance at the transmit select indicator.
3. **Not monitoring guard:** Students leave UHF in MAIN mode instead of BOTH. Make BOTH mode part of the startup checklist.
4. **Poor readback discipline:** Students say "Roger" when they should read back a clearance. Drill: runway assignments, altimeter settings, and hold-short instructions always require readback.
5. **Talking too fast:** Students rush radio calls. Teach the cadence: key the mic, pause half a beat, speak clearly at conversational pace, unkey.
6. **Forgetting to tune before transmitting:** Students try to make a call without first verifying the correct frequency is set. Teach: "Tune — Verify — Key — Speak."
7. **Easy Communication crutch:** Students who learned with Easy Comm struggle with realistic radio operation. Start BQT with Easy Comm off from the first training event.


---

## Module 4: Ground Operations

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Perform a complete cold-dark start of the OH-58D Kiowa Warrior, switch by switch.
2. Understand the FADEC auto-start sequence and monitor parameters for a normal start.
3. Detect and respond to a hot start, hung start, or failed start during engine startup.
4. Align the AHRS/GPS system and verify navigation readiness.
5. Perform rotor engagement and track main rotor RPM (Nr) to governed speed.
6. Configure all cockpit systems for flight (radios, instruments, lighting, MFD).
7. Perform a complete before-taxi checklist.
8. Hover taxi safely, maintaining directional control and awareness of ground resonance.
9. Perform a pre-takeoff check at the holding point.

---

### 4.1 Cold-Dark Cockpit — Starting Condition

The training scenario begins with the OH-58D in a cold-dark state on the ramp. All switches are off, rotors are stationary, and no systems are powered.

**Pre-start walkaround (conceptual):** In real-world operations, the pilot performs an exterior inspection before entering the cockpit. In DCS, this is simulated by visual inspection from the external view:
- Rotor blades — no visible damage
- Pitot tube — uncovered
- Tail rotor — intact
- Landing skids — no obstructions
- Engine exhaust / IR suppressor — clear

---

### 4.2 Engine Start — Complete Procedure

The OH-58D features a FADEC-controlled engine start. In AUTO mode, the FADEC sequences the start automatically once the starter is engaged. The pilot's role is to monitor instruments and be prepared to abort if parameters exceed limits.

#### Step-by-Step Cold Start Sequence

| Step | Action | Expected Result |
|---|---|---|
| 1 | **Battery** — ON | Electrical bus powered; caution panel illuminates with multiple warnings (normal for cold start). Battery voltage should read ~24–28V DC. |
| 2 | **Verify caution/warning panel** — Check for pre-existing faults | Note any unexpected cautions. All cautions at this stage are normal (engine off, generators off, etc.). |
| 3 | **Fuel shutoff** — OPEN (verify) | Fuel valve open, allowing fuel to reach the engine. May already be in the open position. |
| 4 | **Throttle** — IDLE detent (or OFF then IDLE, per DCS model) | Throttle at idle detent position. FADEC auto mode will control fuel scheduling from here. |
| 5 | **FADEC mode** — Verify AUTO | FADEC auto mode selected. This is the default and normal mode for all operations. |
| 6 | **Rotor brake** — OFF (released) | Rotor brake released, allowing rotor rotation once engine drives the transmission. |
| 7 | **Starter button** — PRESS AND HOLD (or press momentarily per DCS) | Starter motor engages. N1 (gas generator) begins to spool up. |
| 8 | **Monitor N1 rise** — Observe N1 gauge increasing | N1 should begin rising smoothly. If N1 stalls below ~15%, suspect a hung start. |
| 9 | **FADEC introduces fuel** — Automatic (at ~15–20% N1) | TOT begins to rise as combustion occurs. A slight "light-off" indication on TOT. |
| 10 | **Monitor TOT during start** — Must remain below 810°C | TOT rises, peaks, then decreases as N1 continues to accelerate. Peak TOT during start should not exceed 810°C for more than ~10 seconds. |
| 11 | **Release starter** — When N1 reaches self-sustaining speed (~58–62% N1) | The engine is now self-sustaining. FADEC continues to manage acceleration to idle. |
| 12 | **Engine stabilizes at ground idle** | N1 stabilizes at ground idle (~62–65% N1). TOT stabilizes well below limits. Nr begins to increase as the transmission is engaged. |
| 13 | **Monitor Nr rise** — Track Nr on tachometer | Nr (main rotor RPM) increases as the freewheeling unit engages and the engine drives the rotor system through the transmission. |
| 14 | **Nr reaches governed speed** — ~100% (395 RPM) | FADEC governs Nr at 100%. All normal. Torque indication at ground idle is low (~10–20% Q). |
| 15 | **Generator(s)** — ON | Main generator comes online. Electrical load transfers from battery to generator. Caution lights for generator should extinguish. |
| 16 | **Verify electrical panel** — All buses powered | AC and DC buses show proper voltage. Inverter operating. |

> *⚠ Realism Divergence: The DCS OH-58D start sequence may be simplified compared to the real aircraft. The real aircraft has a more nuanced starter engagement sequence with specific N1 callouts. In DCS, pressing the starter button may automatically sequence the entire start with the FADEC doing all fuel scheduling. The key pilot actions — monitoring TOT and N1 — remain the same.*

#### Start Abnormalities

| Abnormality | Indication | Action |
|---|---|---|
| **Hot start** | TOT exceeds 810°C and continues rising | Immediately abort: throttle OFF, motor starter to assist cooling airflow if possible. Allow engine to cool completely before reattempt. |
| **Hung start** | N1 stabilizes below normal idle (~62%) and does not continue to accelerate | Abort: throttle OFF, wait 30 seconds minimum before reattempt. May indicate insufficient battery voltage or starter issue. |
| **No light-off** | N1 rises but TOT shows no indication of combustion by ~25% N1 | Abort: throttle OFF, check fuel shutoff valve is open. Purge residual fuel by dry-motoring (starter only, no fuel) if available. |
| **Compressor stall** | Loud bangs, fluctuating TOT and N1 | Abort: throttle OFF immediately. Do not reattempt until cause is investigated. |

---

### 4.3 Post-Start Checks

After the engine has stabilized at ground idle with Nr at 100%:

| System | Check | Expected |
|---|---|---|
| **Engine instruments** | N1, TOT, torque, oil pressure, oil temperature | All in green/normal ranges |
| **Nr** | Tachometer | 100% (±1%), governed by FADEC |
| **Caution/warning panel** | Scan for any illuminated cautions | Only expected cautions (e.g., parking brake if applicable). No master warning. |
| **Hydraulic pressure** | Gauge | ~1,000 PSI (within normal range) |
| **Generator** | On, voltage normal | ~28V DC bus voltage |
| **Fuel quantity** | Fuel gauge | Expected fuel load for the mission; note starting fuel. |
| **AHRS/GPS** | Begin alignment (see 4.4) | AHRS initializing. |
| **Flight controls** | Cyclic, collective, pedals — check freedom of movement | Full travel, no binding, control response on rotor head. |
| **Caution panel test** | Press test button | All caution lights should illuminate during test, then extinguish when released. |

---

### 4.4 AHRS/GPS Alignment

The OH-58D uses an Attitude Heading Reference System (AHRS) integrated with GPS for navigation and attitude reference.

| Step | Action | Notes |
|---|---|---|
| 1 | **AHRS** — ON (should be on with battery) | AHRS begins gyro alignment. |
| 2 | **Ensure aircraft is stationary** | AHRS alignment requires the aircraft to be still. Do not move the aircraft during alignment. |
| 3 | **Wait for alignment complete** | Alignment time varies: fast align (~30–90 seconds typical in DCS), full align (~2–5 minutes real world. DCS may accelerate this). |
| 4 | **Verify AHRS status on MFD** | NAV page or SYS page should show AHRS aligned. Heading and attitude indications become valid. |
| 5 | **GPS acquisition** | GPS acquires satellites and provides position. Verify position on MFD moving map matches known ramp location. |
| 6 | **Heading check** | Compare AHRS heading indication to known runway/ramp heading. Should agree within a few degrees. |

> *⚠ Realism Divergence: DCS AHRS alignment time may be significantly faster than real-world. The real OH-58D AHRS requires a precise alignment procedure with position input and can take several minutes. DCS may simplify this to an automatic alignment that completes quickly after power-on. The student should still practice the full alignment procedure conceptually.*

---

### 4.5 Systems Configuration for Flight

After engine start and AHRS alignment, configure remaining systems:

#### Avionics & MFD

| Step | Action |
|---|---|
| 1 | **MFD** — Power on (if not already on with battery). Verify MFD displays correctly. |
| 2 | **MFD page** — Select NAV page. Verify moving map shows current position. |
| 3 | **Waypoints** — If applicable, verify waypoint data is loaded and correct per mission brief. |
| 4 | **ENG page** — Briefly check engine page to verify all instruments reading normally via MFD. |

#### Radios (per Module 3)

| Step | Action |
|---|---|
| 1 | **ARC-164 (UHF)** — Set to BOTH mode (main + guard). Tune tower/ground frequency per mission brief. |
| 2 | **ARC-201 (FM)** — Set to SC mode. Tune inter-flight frequency per mission brief. |
| 3 | **Audio panel** — TX select to UHF. UHF and FM volumes up. ICS volume up. Hot mic on. |
| 4 | **Radio check** — Contact ground/tower: "[Callsign], radio check" and listen for response. |

#### Flight Instruments

| Step | Action |
|---|---|
| 1 | **Altimeter** — Set to current QNH/QFE per ATIS or mission brief. |
| 2 | **Radar altimeter** — ON. Set decision height bug if applicable. |
| 3 | **Heading indicator / HSI** — Verify heading agrees with AHRS and known orientation. |
| 4 | **Attitude indicator** — Verify level and erect. |

#### Lighting (as required)

| Step | Action |
|---|---|
| 1 | **Position lights** — As required (on for all flight operations). |
| 2 | **Anti-collision light** — ON before rotor engagement if not already on. Required whenever rotors are turning. |
| 3 | **Instrument lights** — Adjust for conditions (night operations: NVG-compatible green). |
| 4 | **Landing/search light** — Verify function, set to retract for taxi/takeoff. |

---

### 4.6 Before-Taxi Checklist

Complete this checklist before requesting taxi clearance:

- [ ] **Engine instruments** — All green, N1/TOT/Q normal
- [ ] **Nr** — 100% governed
- [ ] **Hydraulic pressure** — ~1,000 PSI, normal
- [ ] **Generators** — ON, bus voltage normal
- [ ] **AHRS/GPS** — Aligned, position valid
- [ ] **Radios** — Tuned, transmit check complete
- [ ] **Flight instruments** — Set (altimeter, DG, radar alt)
- [ ] **Caution panel** — No unexpected cautions
- [ ] **Fuel** — Sufficient for mission, quantity noted
- [ ] **Flight controls** — Full and free, response correct
- [ ] **Anti-collision light** — ON
- [ ] **Doors** — Closed and secure (DCS: verify via external view or cockpit check)
- [ ] **MFD** — NAV page, moving map active

---

### 4.7 Hover Taxi

#### Requesting Taxi

Contact ground control on UHF:
> "[Ground], [Callsign], [position], request hover taxi to [destination]"

Read back taxi instructions, including route and any hold-short instructions.

#### Hover Taxi Technique

| Parameter | Value |
|---|---|
| **Hover height** | 3–5 feet skid height (AGL) |
| **Taxi speed** | Walking pace — approximately 5–10 knots ground speed |
| **Directional control** | Pedals for heading; cyclic for lateral/fore-aft position |
| **Power management** | Collective adjusts height; anticipate power changes for wind gusts |

**Procedure:**
1. From the ground, slowly raise the collective to establish a 3–5 foot hover.
2. Allow the aircraft to stabilize in hover before beginning movement.
3. Apply gentle forward cyclic to begin forward movement at walking pace.
4. Use pedals to maintain heading along the taxiway centerline.
5. Maintain constant awareness of rotor clearance from obstacles (buildings, other aircraft, light poles).
6. Stop at designated holding points by neutralizing cyclic and maintaining hover.

**Critical cautions during hover taxi:**

| Hazard | Description | Mitigation |
|---|---|---|
| **Ground resonance** | Vibration building rapidly after lifting to a hover or during light ground contact | Immediate action: if Nr is in normal range, pull collective and fly away. If Nr is low, immediately reduce collective and shut down. Do NOT attempt to "ride it out." |
| **Weathervaning** | Crosswind causes the aircraft to yaw into the wind | Active pedal inputs; taxi at slower speed in strong crosswinds |
| **Recirculation** | In confined areas, rotor downwash recirculates and reduces lift | Expect higher power required; monitor torque |
| **Foreign object damage (FOD)** | Loose debris on the ramp area | Approach and taxi through ramp areas at minimum speed; check for debris on walkaround |
| **Obstacle clearance** | Rotor blade tip clearance from structures | Maintain at least half a rotor diameter (17+ feet) clearance from obstacles |

---

### 4.8 Pre-Takeoff Check

At the holding point (runway hold-short line or designated departure point), perform the pre-takeoff check:

- [ ] **Engine instruments** — All green (scan N1, TOT, Q, oil pressure/temp)
- [ ] **Nr** — 100% governed
- [ ] **Fuel** — Sufficient, balanced (if applicable)
- [ ] **Flight instruments** — Altimeter set, heading indicator aligned, attitude indicator erect
- [ ] **Radios** — Correct frequencies, transmit on UHF for tower
- [ ] **MFD** — NAV page, waypoints verified
- [ ] **Radar altimeter** — ON, decision height set
- [ ] **Caution panel** — Clear of unexpected warnings
- [ ] **Anti-collision & position lights** — ON
- [ ] **Doors & harness** — Secure
- [ ] **Departure plan** — Reviewed (direction, altitude, initial heading per clearance)
- [ ] **Emergency plan** — Briefed (abort criteria, forced landing area, emergency actions)

**Request takeoff clearance:**
> "[Tower], [Callsign], holding short runway [number], ready for departure [direction/VFR]"

---

### 4.9 Cockpit Switch Reference — Module 4

| Switch/Control | Location | Function | DCS Action |
|---|---|---|---|
| **Battery switch** | Overhead console / electrical panel | Master battery ON/OFF | Mouse click |
| **Fuel shutoff valve** | Overhead console / engine panel | Open/close fuel to engine | Mouse click |
| **Throttle** | Collective assembly (twist grip) | Idle / Fly / Off positions | Keyboard or axis |
| **FADEC mode** | Engine control panel | AUTO / MAN | Mouse click |
| **Starter button** | Overhead console / engine panel | Engages starter motor | Mouse click (hold or momentary per DCS) |
| **Rotor brake** | Overhead console | Engage/release rotor brake | Mouse click |
| **Generator switch** | Overhead console / electrical panel | Generator ON/OFF | Mouse click |
| **AHRS mode** | Avionics panel | OFF / ALIGN / NAV | Mouse click to cycle |
| **Altimeter knob** | Instrument panel — altimeter | Set QNH/QFE (Kollsman window) | Mouse scroll |
| **Radar altimeter** | Instrument panel | ON/OFF + decision height knob | Mouse click / scroll |
| **Anti-collision light** | Overhead console / lighting panel | ON/OFF | Mouse click |
| **Position lights** | Overhead console / lighting panel | OFF / DIM / BRT | Mouse click to cycle |
| **Instrument lights** | Overhead console / lighting panel | Brightness rheostat | Mouse scroll |
| **Caution panel test** | Caution panel | Press to test all lights | Mouse click |

---

### 4.10 Instructor Notes — Module 4

**Common student errors:**

1. **Not monitoring TOT during start:** Students press the starter and look away. Drill: "Eyes on TOT from the moment you hit the starter until the engine stabilizes." TOT exceedance during start is the most common start emergency.
2. **Moving during AHRS alignment:** Students get impatient and begin taxiing before AHRS is aligned. The AHRS needs the aircraft to be stationary. Verify alignment status on MFD before any movement.
3. **Skipping the before-taxi checklist:** Students are eager to fly and rush through or skip checks. Enforce the discipline: checklist complete before radio call for taxi.
4. **Abrupt collective inputs during hover taxi:** Students raise or lower the collective too quickly, causing altitude excursions or hard ground contact. Teach: "Small, smooth, steady" — and anticipate power changes rather than reacting.
5. **Failure to check six (360° clearance) before hover:** Students pull collective without verifying the area behind and above is clear. Teach: "Clear left, clear right, clear above, clear behind — pulling" as a verbal flow.
6. **Ground resonance ignorance:** Students feel a vibration and freeze instead of taking immediate action. This must be drilled: vibration = immediate decision (fly away or shut down). No hesitation. Ground resonance can destroy the aircraft in seconds.
7. **Not briefing the emergency plan before takeoff:** Students reach the runway without discussing abort criteria or forced landing areas. Make the emergency brief a required item in the pre-takeoff check.
8. **Forgetting anti-collision light:** Students start taxiing without the anti-collision light on. This is a safety hazard — other aircraft may not see rotor rotation. Include it as one of the first items after engine start.


---

## Module 5: Hover & Takeoff

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Perform a controlled hover at 3–5 feet skid height using coordinated collective, cyclic, and pedal inputs.
2. Execute a power check (hover power assessment) to determine aircraft capability for the conditions.
3. Perform a normal takeoff from a hover with a smooth transition through translational lift.
4. Perform a no-hover takeoff (surface-level wind, clear departure path).
5. Perform a maximum performance takeoff (obstacle clearance departure from confined area).
6. Perform a running takeoff (from forward taxi when hover OGE is not possible).
7. Identify and respond to ground resonance during hover or ground contact.
8. Transition from hover to forward flight, managing translational lift and climb.

---

### 5.1 Hovering — Fundamentals

The hover is the foundation of all helicopter operations. The OH-58D hovers at a standard 3–5 foot skid height for normal operations.

#### Hover Aerodynamics

| Concept | Description |
|---|---|
| **In Ground Effect (IGE)** | Hovering within approximately 1 rotor diameter of the surface (~35 ft for OH-58D). Ground effect provides a "cushion" — the rotor downwash is trapped and increases efficiency. Requires ~10–15% less power than OGE hover. |
| **Out of Ground Effect (OGE)** | Hovering above approximately 1 rotor diameter from the surface. No ground effect benefit. Requires maximum hover power. |
| **Translating tendency** | The OH-58D has a tendency to drift right in a hover due to tail rotor thrust. Compensate with slight left cyclic input. |
| **Tail rotor drift** | As left pedal is applied to counteract main rotor torque, the tail rotor produces a right-pushing thrust. The pilot must compensate with left cyclic. |
| **Pendular action** | The fuselage, suspended below the rotor head, tends to oscillate like a pendulum. Smooth, small inputs prevent pilot-induced oscillations (PIO). |

#### Hover Technique

**Controls coordination in hover:**
- **Collective** → controls altitude (up = climb, down = descend)
- **Cyclic** → controls horizontal position (forward/back/left/right drift)
- **Pedals** → controls heading (yaw left/right to maintain heading)
- **Throttle** → managed by FADEC in auto mode; pilot does not normally adjust

**Procedure — establishing a hover from the ground:**

| Step | Action | Notes |
|---|---|---|
| 1 | Ensure Nr is 100% governed | FADEC auto mode |
| 2 | Smoothly increase collective | Raise slowly — approximately 1–2 seconds from ground to hover height |
| 3 | As aircraft becomes light on skids, increase pedal input as needed | Left pedal to counteract torque as collective increases |
| 4 | Maintain heading with pedals, position with cyclic | Small, smooth corrections — avoid over-controlling |
| 5 | Stabilize at 3–5 ft skid height | Cross-check radar altimeter if available; primary reference is external visual |
| 6 | Perform hover checks | Verify instruments, announce "Stable in a hover" |

**Common hover errors and corrections:**

| Error | Cause | Correction |
|---|---|---|
| Overcontrolling / PIO | Excessive or rapid control inputs | Use smaller inputs; relax grip; focus on a distant reference point, not the ground directly below |
| Drifting right | Not compensating for translating tendency | Apply slight left cyclic; this is a constant trim requirement |
| Yaw oscillation | Over-correcting pedal inputs | Smaller pedal corrections; anticipate rather than react |
| Sinking after reaching hover height | Insufficient collective as aircraft settles | Slowly add collective to maintain altitude; check for overloaded condition |
| Bouncing off the ground | Raising collective too quickly, then reducing abruptly | Smooth, continuous collective raise; if bouncing starts, smoothly increase collective to fly out of it — do NOT slam collective down |

---

### 5.2 Power Check (Hover Power Assessment)

Before takeoff, the pilot performs a power check to verify the aircraft can hover, climb, and maintain safe flight margins.

**Purpose:** Determine the power available vs. power required. If the aircraft cannot hover in ground effect (IGE), it certainly cannot hover out of ground effect (OGE) or perform a normal takeoff.

#### Procedure

| Step | Action | Expected |
|---|---|---|
| 1 | Establish a stable 3-foot hover, into the wind | Note torque required to hover |
| 2 | Record hover torque (% Q) | This is "hover power required" |
| 3 | Compare to aircraft limits | Max continuous torque: 85% Q. Max takeoff torque: 100% Q. |
| 4 | Assess margins | If hovering at 75% Q, you have 25% margin to max takeoff. Adequate for normal operations. If hovering at 90% Q, you have only 10% margin — high DA or heavy aircraft. Consider reducing load. |

**Power assessment criteria:**

| Condition | Hover Torque | Assessment |
|---|---|---|
| **Normal** | ≤75% Q IGE | Adequate power for all maneuvers including OGE hover and max performance takeoff |
| **Marginal** | 75–85% Q IGE | Sufficient for normal takeoff. OGE hover may not be possible. Max performance limited. |
| **Critical** | 85–95% Q IGE | Normal takeoff possible with caution. Running takeoff may be preferred. No OGE capability. |
| **Insufficient** | >95% Q IGE (or cannot hover) | Cannot perform normal takeoff. Reduce weight or wait for conditions to improve. Running takeoff only option. |

> *Note: These are general guidelines. Actual limits depend on density altitude, wind, aircraft weight, and configuration. Always cross-reference the performance planning card / TM limits.*

---

### 5.3 Translational Lift

As the helicopter accelerates from a hover to forward flight, it encounters **translational lift** — a marked increase in rotor efficiency that occurs at approximately **16–24 knots** airspeed.

| Phase | Airspeed | Effect |
|---|---|---|
| **Hover** | 0 knots | Rotor is working through its own downwash; least efficient |
| **Approaching ETL** | 10–16 knots | Turbulent airflow — vibration increases |
| **Effective Translational Lift (ETL)** | ~16–24 knots | Rotor encounters clean, undisturbed air. Significant lift increase. Aircraft "jumps" upward. |
| **Beyond ETL** | >24 knots | Continued improvement in efficiency. Less power required for sustained flight. |

**Pilot actions through ETL:**
1. As speed increases toward ETL, the aircraft will tend to climb and the nose will pitch up.
2. Apply slight forward cyclic to maintain the desired rate of acceleration and climb angle.
3. Reduce collective slightly if necessary to maintain desired climb rate (power margin increases through ETL).
4. Maintain heading with pedals — torque effect changes as power changes.

---

### 5.4 Normal Takeoff (from a Hover)

The normal takeoff is the standard departure method when power margins are adequate and the departure path is clear.

#### Procedure

| Step | Action | Parameters |
|---|---|---|
| 1 | Establish a stable 3–5 ft hover, into the wind | Verify power check complete |
| 2 | Smoothly apply forward cyclic | Begin forward acceleration |
| 3 | As speed increases, apply slight collective increase to maintain altitude and begin climb | Maintain 3–5 ft until approaching ETL |
| 4 | Transition through ETL (~16–24 kts) | Expect the aircraft to want to climb and pitch up. Apply forward cyclic to maintain acceleration. |
| 5 | Establish a positive rate of climb | Climb at ~55–60 KIAS (Vy — best rate of climb speed) |
| 6 | Accelerate to Vy (55–60 KIAS) and climb | Maintain coordinated flight — ball centered |
| 7 | At 200 ft AGL, begin transition to cruise climb | Accelerate to 70–80 KIAS climb speed (or as desired) |
| 8 | At pattern altitude or assigned altitude, level off | Reduce power to cruise (~55–65% Q depending on conditions) |

**Key parameters:**

| Parameter | Value |
|---|---|
| **Best rate of climb (Vy)** | ~55–60 KIAS |
| **Best angle of climb (Vx)** | ~45–50 KIAS (for obstacle clearance) |
| **Normal climb torque** | 75–90% Q (depending on weight/DA) |
| **ETL** | ~16–24 knots |

---

### 5.5 No-Hover Takeoff

Used when a hover check has been performed and conditions allow a direct departure without establishing a sustained hover (e.g., adequate wind, clear departure path, minimizing time in the hover).

#### Procedure

| Step | Action |
|---|---|
| 1 | From the ground, smoothly raise collective while simultaneously applying slight forward cyclic. |
| 2 | Aircraft lifts and immediately begins forward acceleration — do not hover. |
| 3 | Continue acceleration through ETL with coordinated cyclic and collective. |
| 4 | At ETL, establish a positive climb at Vy (55–60 KIAS). |
| 5 | Continue as a normal departure. |

**Note:** The no-hover takeoff is quicker but requires a clear departure path and confidence in the power available (based on prior hover check or performance planning).

---

### 5.6 Maximum Performance Takeoff

Used for departure from confined areas where obstacles must be cleared immediately after takeoff. This maneuver uses maximum available power to achieve the steepest climb angle possible.

#### Procedure

| Step | Action | Notes |
|---|---|---|
| 1 | Establish a stable hover, facing into the wind and toward the departure path | Identify obstacles and clearance path |
| 2 | Note hover torque — verify adequate power available | Must have margin above hover to climb |
| 3 | Smoothly apply forward cyclic and increase collective simultaneously toward max takeoff power (up to 100% Q, 5 min limit) | Aggressive but smooth — do not exceed limits |
| 4 | Accelerate to Vx (~45–50 KIAS) — best angle of climb speed | Vx gives the steepest climb angle to clear obstacles |
| 5 | Clear the obstacle | Maintain Vx until obstacle is cleared |
| 6 | After clearing the obstacle, lower the nose and accelerate to Vy (55–60 KIAS) | Transition to best rate of climb for altitude gain |
| 7 | Reduce power to max continuous (85% Q) when able | Do not exceed 100% Q for more than 5 minutes |

**Critical notes:**
- Maximum performance takeoff is a planned, deliberate maneuver — not an emergency procedure.
- If the aircraft cannot hover at the departure point, it cannot perform a max performance takeoff (use running takeoff or reduce weight).
- Always have an abort plan if the aircraft fails to climb as expected.

---

### 5.7 Running Takeoff

Used when the aircraft is too heavy or density altitude is too high for a hover, but sufficient level ground is available for a surface-level acceleration through ETL.

#### Procedure

| Step | Action | Notes |
|---|---|---|
| 1 | Align the aircraft into the wind along the longest available clear surface | Departure path must be clear |
| 2 | From the ground, smoothly increase collective to become light on the skids | Aircraft should be "skimming" — skids lightly on the surface |
| 3 | Apply forward cyclic to begin forward acceleration while remaining near the ground | Maintain slight positive pressure on the skids or just barely airborne |
| 4 | Accelerate through ETL (~16–24 kts) | As translational lift builds, the aircraft will become airborne naturally |
| 5 | At ETL, establish a positive rate of climb | Do not attempt to climb before achieving ETL |
| 6 | Accelerate to Vy (55–60 KIAS) and climb normally | Standard departure from this point |

**Critical caution:** If the aircraft will not accelerate or become airborne before the end of the available surface, abort the takeoff: reduce collective, decelerate, and stop. Reassess weight and conditions.

---

### 5.8 Ground Resonance — Expanded Detail

Ground resonance is a critical risk during hover operations, particularly for the OH-58D with its 4-blade soft-in-plane bearingless rotor system.

| Aspect | Detail |
|---|---|
| **What is it** | A destructive oscillation caused by an imbalance in the lead-lag motion of the rotor blades coupling with the natural frequency of the aircraft on its landing gear (skids). |
| **Why the OH-58D is susceptible** | The soft-in-plane bearingless rotor design has rotor blade lead-lag frequencies that can couple with fuselage oscillation modes. Fully articulated and teetering rotors are less susceptible. |
| **When it occurs** | Typically during ground contact with power on — liftoff, touchdowns, hover taxi with skid-dragging. Most likely during partial contact (one skid touching, other light). |
| **How it feels** | Rapidly building lateral vibration/oscillation. The aircraft shakes violently with increasing amplitude. |
| **Time to failure** | Seconds — ground resonance can destroy an airframe in under 10 seconds if not corrected immediately. |

#### Immediate Action — BOLDFACE

**If Nr is in normal range (97–101%):**
> **COLLECTIVE — INCREASE (FLY AWAY IMMEDIATELY)**

Get the aircraft completely off the ground to break the ground contact that sustains the resonance. Hover or climb — any positive separation from the ground stops the feedback loop.

**If Nr is low or decaying:**
> **COLLECTIVE — FULL DOWN**
> **THROTTLE — IDLE / OFF**
> **ROTOR BRAKE — APPLY (when Nr is low enough)**

Shut down the rotor system as fast as possible. A low-Nr rotor does not have the centrifugal force to fly away safely and the resonance will worsen.

**Key principle:** React instantly. Do not hesitate, do not try to diagnose, do not try to "damp it out" with cyclic. The ONLY options are fly or shut down. Hesitation = aircraft destruction.

> *⚠ Realism Divergence: DCS may or may not fully model ground resonance for the OH-58D. If modeled, it will typically occur during improper ground contact at operating Nr. If not modeled, the student should still understand the procedure conceptually, as it is a critical real-world consideration for this rotor system. Test in DCS: attempt light skid contact during hover — if the aircraft develops lateral oscillation, ground resonance is modeled.*

---

### 5.9 Climb Profiles

| Profile | Speed | Torque | Use |
|---|---|---|---|
| **Best rate (Vy)** | 55–60 KIAS | 75–90% Q | Normal departure — maximum altitude gain per unit time |
| **Best angle (Vx)** | 45–50 KIAS | Max available (up to 100% Q) | Obstacle clearance — steepest flight path angle |
| **Cruise climb** | 70–80 KIAS | 65–80% Q | En route climb — compromise between climb rate and forward speed |
| **Max performance** | Vx initially, Vy after obstacle | Up to 100% Q (5 min limit) | Confined area departure with obstacle clearance |

---

### 5.10 Cockpit Switch Reference — Module 5

| Control | Location | Function | DCS Action |
|---|---|---|---|
| **Collective** | Left hand — collective lever | Controls blade pitch / power demand | Joystick axis (throttle axis or dedicated) |
| **Cyclic** | Right hand — cyclic stick | Controls rotor disc tilt / aircraft attitude | Joystick X/Y axis |
| **Pedals** | Feet — anti-torque pedals | Controls tail rotor pitch / yaw | Rudder pedals or keyboard (`Z` / `X` default) |
| **Throttle** | Collective — twist grip | FLY detent for powered flight; IDLE for ground/shutdown | Keyboard or axis |
| **Radar altimeter** | Instrument panel | Displays AGL height; useful for hover height reference | Visual reference only |
| **Torque gauge** | Instrument panel | Monitor power output during maneuvers | Visual reference |
| **Nr tachometer** | Instrument panel | Monitor rotor RPM — critical for ground resonance decisions | Visual reference |
| **Rotor brake** | Overhead console | Apply to stop rotor in emergency ground resonance (low Nr only) | Mouse click |

---

### 5.11 Instructor Notes — Module 5

**Common student errors:**

1. **Overcontrolling in the hover:** The #1 beginner problem. Students make large, rapid inputs trying to correct drift, which creates pilot-induced oscillations (PIO). Teach: "Make a correction half the size you think you need, then wait for the response." Focus vision on a distant reference, not the ground directly below.
2. **Failing to apply left pedal during collective increase:** As collective increases, torque increases, and the aircraft yaws right. Students forget to add left pedal. Teach: "Collective and pedal move together."
3. **Pulling too much collective during takeoff:** Students try to "jump" off the ground instead of a smooth transition. This over-torques and can exceed limits. Teach: "Smooth raise to hover height, pause, then transition to forward flight."
4. **Not managing ETL transition:** Students are surprised by the pitch-up and altitude gain at ETL. Teach: "Expect ETL at 16–24 knots — the aircraft will want to climb and pitch up. Lead it with forward cyclic."
5. **Attempting to hover at max gross weight on a hot day:** Students don't perform a proper power check and find they cannot hover. Teach performance planning awareness — weight, DA, wind all affect hover capability.
6. **Ignoring ground resonance vibration:** Students feel vibration and either freeze or try to diagnose it. Drill the immediate action relentlessly: "If you feel it, you have 2–3 seconds to decide: fly or shut down. No other option."
7. **Not setting up for maximum performance takeoff correctly:** Students don't face into the wind or don't identify the obstacle clearance path. Teach: "Plan the max perf takeoff before you pull collective — wind, obstacles, abort plan."
8. **Running takeoff — trying to climb before ETL:** Students pull collective before reaching translational lift speed and the aircraft settles. Teach: "Stay near the surface until ETL — the lift will come to you."


---

## Module 6: Basic Flight Maneuvers

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Maintain straight and level flight at a specified airspeed and altitude.
2. Perform coordinated level turns at 15°, 30°, and 45° angles of bank.
3. Execute controlled climbs and descents at specified rates.
4. Perform speed changes (acceleration and deceleration) while maintaining altitude.
5. Demonstrate slow flight near the lower end of the airspeed envelope.
6. Perform basic autorotation practice entries (power recovery).
7. Use trim effectively to reduce pilot workload in steady flight.
8. Understand and manage fuel consumption during flight.

---

### 6.1 Straight and Level Flight

Straight and level flight is the baseline maneuver — maintaining a constant heading, altitude, and airspeed.

#### Procedure

| Parameter | Target | Tolerance |
|---|---|---|
| **Altitude** | As assigned (e.g., 1,500 ft MSL) | ±100 ft |
| **Heading** | As assigned | ±10° |
| **Airspeed** | Cruise: 80–100 KIAS (typical) | ±5 kts |
| **Torque** | Whatever is required to maintain speed at level altitude | Monitor, don't fixate |
| **Ball** | Centered (coordinated flight) | Slight deflection acceptable in calm air |

**Technique:**
1. Establish the desired airspeed and altitude.
2. Adjust collective to set the power required to maintain level flight at that airspeed. For the OH-58D at typical gross weights, cruise at 80–90 KIAS requires approximately 55–65% Q.
3. Trim any cyclic forces — use the trim (force trim release) button to relieve cyclic pressure.
4. Scan: Altitude → Heading → Airspeed → Engine instruments → Outside → Repeat.
5. Make small corrections early rather than large corrections late.

**Trim usage:**
- The OH-58D uses a force trim system. Press the force trim release button (typically on the cyclic grip), move the cyclic to the desired position, then release the button to set the new trim point.
- Trim should be adjusted whenever the pilot is holding a sustained cyclic force. Well-trimmed flight reduces fatigue and allows smoother inputs.

> *⚠ Realism Divergence: DCS force trim behavior may differ from the real aircraft. In some DCS modules, the force trim sets a return-to-center position for the cyclic. In others, it acts as a friction-hold. The student should experiment in DCS to understand the specific force trim implementation for the OH-58D module.*

---

### 6.2 Level Turns

Turns are classified by bank angle. The OH-58D is a light, responsive helicopter — coordinated turns require simultaneous cyclic, collective, and pedal inputs.

#### Bank Angle Categories

| Category | Bank Angle | Load Factor | Use |
|---|---|---|---|
| **Shallow** | Up to 15° | ~1.0 G | Normal heading changes, pattern turns |
| **Medium** | 15°–30° | ~1.0–1.15 G | Standard maneuvering, course corrections |
| **Steep** | 30°–45° | ~1.15–1.41 G | Aggressive turns, avoidance, tactical maneuvering |
| **>45°** | >45° | >1.41 G | Not recommended for BQT — advanced tactical only |

#### Procedure — Medium Turn (30° bank)

| Step | Action | Notes |
|---|---|---|
| 1 | Select a reference point for roll-out (90°, 180°, 360° turn as desired) | Anticipate roll-out by ~10° of heading before reaching desired heading |
| 2 | Apply coordinated cyclic in the direction of turn | Smooth, gradual roll to 30° bank angle |
| 3 | Apply slight aft cyclic to maintain altitude | In a bank, the vertical component of lift decreases — the nose tends to drop |
| 4 | Add slight collective (power) to maintain altitude | Additional lift is needed to compensate for the bank angle |
| 5 | Apply pedal as needed to keep the ball centered | Inside pedal (direction of turn) is typically needed |
| 6 | Maintain bank angle, altitude, and airspeed throughout the turn | Scan: Bank → Altitude → Airspeed → Ball → Outside |
| 7 | Anticipate roll-out — begin leveling ~10° before desired heading | Roll wings level, release aft cyclic and power, neutralize pedals |
| 8 | Resume straight and level flight on new heading | Re-trim as needed |

**Key principle: "Lift the collective to turn."** In a helicopter, a turn requires more power than straight and level flight because the effective lift vector is tilted. The pilot must add collective to maintain altitude. This is unlike fixed-wing aircraft where the pilot primarily uses back pressure.

#### Altitude Loss in Turns

| Bank Angle | Additional Collective Required | Altitude Loss Tendency |
|---|---|---|
| 15° | Minimal | Slight — easily corrected |
| 30° | Noticeable | Moderate — must actively add collective |
| 45° | Significant | Substantial — requires deliberate power addition |

---

### 6.3 Climbs and Descents

#### Climbs

| Type | Speed | Power | Use |
|---|---|---|---|
| **Normal climb** | 55–60 KIAS (Vy) | 75–90% Q | Departure, altitude gain |
| **Cruise climb** | 70–80 KIAS | 65–80% Q | En route altitude change — trades climb rate for forward speed |
| **Max angle climb** | 45–50 KIAS (Vx) | Max available (100% Q, 5 min) | Obstacle clearance |

**Climb technique:**
1. Increase collective to desired climb power.
2. Adjust cyclic to maintain desired climb speed.
3. Maintain heading with pedals (torque change causes yaw).
4. Trim.
5. At desired altitude, lower collective to cruise power and accelerate/decelerate to cruise speed.

**Climb rate estimation:** At Vy (55–60 KIAS) with 85% Q, the OH-58D at moderate gross weight achieves approximately 500–1,000 fpm rate of climb (highly dependent on weight, DA, and temperature).

#### Descents

| Type | Speed | Power | Rate of Descent |
|---|---|---|---|
| **Normal descent** | 70–80 KIAS | Reduced (40–55% Q) | 300–500 fpm |
| **Cruise descent** | 80–100 KIAS | Slightly reduced | 200–300 fpm |
| **Rapid descent** | 80–90 KIAS | Low power (30–40% Q) | 800–1,500 fpm |

**Descent technique:**
1. Reduce collective to below cruise power.
2. Adjust cyclic to maintain desired descent speed.
3. Maintain heading with pedals.
4. Monitor rate of descent on VSI — do not exceed 1,500 fpm in normal operations.
5. At desired altitude, increase collective to cruise power and level off.

**Level-off technique:** Begin level-off approximately 50 ft before desired altitude for a 500 fpm descent, or 100 ft before for a 1,000 fpm descent. Add power smoothly to arrest the descent rate.

---

### 6.4 Speed Changes

The ability to change airspeed while maintaining altitude is a fundamental skill.

#### Acceleration (slow to fast)

| Step | Action |
|---|---|
| 1 | Lower the nose (forward cyclic) to accelerate |
| 2 | As speed increases, the aircraft will tend to climb — reduce collective to maintain altitude |
| 3 | As desired speed is reached, adjust nose attitude to maintain speed |
| 4 | Re-trim and adjust power for level flight at new speed |

#### Deceleration (fast to slow)

| Step | Action |
|---|---|
| 1 | Raise the nose (aft cyclic) to decelerate |
| 2 | As speed decreases, the aircraft will tend to descend — increase collective to maintain altitude |
| 3 | At desired speed, adjust nose attitude and power for level flight |
| 4 | Re-trim |

**Key principle:** In a helicopter, speed changes at constant altitude require power changes. Slowing down requires *more* power (closer to hover, which is the highest power state). Speeding up requires *less* power (more efficient in forward flight due to translational lift).

---

### 6.5 Slow Flight

Slow flight is flight at speeds near but above ETL (approximately 25–40 KIAS). This regime provides familiarity with the aircraft's handling at low speed and prepares the student for approach and hover.

#### Characteristics of Slow Flight

| Aspect | Detail |
|---|---|
| **Power required** | Higher than cruise — approaching hover power requirements |
| **Control response** | Reduced — cyclic and pedals have less aerodynamic effect at low speed |
| **Stability** | Decreased — more pilot attention required to maintain parameters |
| **Vibration** | Increased near ETL as rotor is at the edge of clean airflow |
| **Susceptibility to LTE** | Increased — low speed with high power and tail rotor demand |

**Procedure:**
1. From cruise, gradually decelerate by raising the nose and adding collective.
2. Stabilize at 30–40 KIAS, noting the increased power required and reduced control authority.
3. Practice maintaining altitude, heading, and speed in this regime.
4. Accelerate back to cruise: lower the nose, reduce collective slightly, and accelerate through ETL.

> *Note: Slow flight is where the aircraft transitions from airplane-like aerodynamic control authority to helicopter-like thrust-borne control. Students should be comfortable in this regime before practicing approaches and hovers.*

---

### 6.6 Autorotation Practice — Power Recovery

Autorotation is the most critical emergency maneuver in helicopter flight. This module covers the **practice entry and power recovery** — the full autorotation to touchdown is covered in Module 8 (Emergencies).

#### What is Autorotation?

When the engine fails or is deliberately disengaged from the rotor, the rotor system is driven by airflow from below (upward through the rotor disc) rather than by the engine. This is autorotation. The rotor continues to produce lift, but the helicopter descends.

**Key parameters for OH-58D autorotation:**

| Parameter | Value |
|---|---|
| **Best autorotation glide speed** | ~72 KIAS |
| **Minimum sink speed** | ~55 KIAS |
| **Rotor RPM range (autorotation)** | ~90–107% Nr |
| **Rate of descent** | ~1,500–2,000 fpm (varies with weight and speed) |
| **Autorotation entry** | Immediate — lower collective to full down, maintain Nr |

#### Practice Autorotation — Power Recovery Procedure

This is practiced at altitude with a recovery before touchdown. The purpose is to build muscle memory for the entry and manage Nr/airspeed.

| Step | Action | Notes |
|---|---|---|
| 1 | **Altitude:** Minimum 1,500 ft AGL for practice. Airspeed: 70–80 KIAS. | Verbal callout: "Practicing autorotation" |
| 2 | **Throttle — IDLE** (simulate engine failure) or instructor calls "Engine failure" | In DCS, roll the throttle to idle (or use a keybind to simulate engine failure) |
| 3 | **Collective — FULL DOWN immediately** | This is the critical initial action. Lowering collective maintains Nr by reducing blade pitch (reducing drag on the rotor). If collective is not lowered promptly, Nr decays rapidly. |
| 4 | **Maintain Nr in 90–107% range** | Monitor tachometer. Nr should stabilize or increase slightly with collective down at glide speed. |
| 5 | **Airspeed — 72 KIAS (best glide)** or **55 KIAS (minimum sink)** | Adjust nose attitude with cyclic to achieve target airspeed. |
| 6 | **Pedals — Maintain coordinated flight** | Without engine torque, pedal input changes significantly. Right pedal is typically needed (less left pedal since no torque to counteract). |
| 7 | **Observe descent rate** — ~1,500–2,000 fpm | The aircraft descends. This is normal. |
| 8 | **At recovery altitude (~500–800 ft AGL), RECOVER:** | Verbal callout: "Recovering" |
| 9 | **Throttle — FLY detent** | Re-engage engine power |
| 10 | **Collective — Increase smoothly to arrest descent** | Do not yank collective — smooth application |
| 11 | **Resume normal flight** | Climb, accelerate, and re-trim |

**Critical notes on autorotation entry:**
- The collective must go **full down** within approximately **1–2 seconds** of engine failure. Delay causes Nr to decay below the autorotation range, which can be unrecoverable.
- At altitude, the entry is the most critical part. If Nr is maintained, you have time to select a landing area and set up the approach (covered in Module 8).
- In DCS, the response to simulated engine failure may feel different from the real aircraft. Nr decay rate and autorotation characteristics are model-dependent.

> *⚠ Realism Divergence: DCS autorotation modeling varies in fidelity. The OH-58D module's autorotation may or may not accurately replicate real-world Nr decay rates, glide distances, and flare effectiveness. The student should practice extensively in DCS to learn the module's specific autorotation characteristics, which may differ from published real-world data. The fundamental procedure (lower collective, maintain Nr, establish glide speed) remains the same regardless of sim fidelity.*

---

### 6.7 Fuel Management

| Parameter | Value |
|---|---|
| **Total fuel capacity** | ~110 US gallons (~730 lbs JP-8) |
| **Fuel burn rate (cruise)** | ~40–50 gallons/hour (varies significantly with power setting and DA) |
| **Endurance (cruise)** | ~2–2.5 hours (with reserve) |
| **Low fuel warning** | ~45 lbs remaining |
| **Minimum landing fuel** | Plan to land with at least 20 minutes reserve |

**Fuel monitoring procedure:**
1. Note starting fuel quantity before takeoff.
2. Calculate expected fuel burn for the planned mission duration.
3. Monitor fuel gauge periodically (include in instrument scan).
4. Low fuel caution light — if it illuminates, land as soon as practical.
5. Track elapsed time as a cross-check against fuel gauge.

---

### 6.8 Cockpit Switch Reference — Module 6

| Control | Function | DCS Action |
|---|---|---|
| **Collective** | Controls power/lift for climbs, descents, turns, hover | Joystick throttle axis or dedicated axis |
| **Cyclic** | Controls pitch/roll attitude for speed, direction, and turns | Joystick X/Y |
| **Pedals** | Controls yaw for heading maintenance, coordinated flight | Rudder pedals or `Z`/`X` keys |
| **Force trim release** | Sets new cyclic trim point to relieve control pressure | Joystick button (configurable) |
| **Throttle** | Fly/Idle/Off — used for autorotation practice | Keyboard or axis |
| **VSI (Vertical Speed Indicator)** | Shows rate of climb/descent in fpm | Visual reference |
| **Airspeed indicator** | Shows indicated airspeed in knots | Visual reference |
| **Torque gauge** | Monitor power output | Visual reference |
| **Nr tachometer** | Critical for autorotation — monitor rotor RPM | Visual reference |
| **Fuel gauge** | Monitor remaining fuel | Visual reference |

---

### 6.9 Instructor Notes — Module 6

**Common student errors:**

1. **Fixating on one instrument:** Students stare at the altimeter during altitude-hold exercises and let heading and airspeed wander. Teach the scan pattern: "Altitude — Heading — Airspeed — Engine — Outside" in a continuous loop.
2. **Not trimming:** Students fight the cyclic for entire flights, building fatigue and degrading precision. Drill: "Any time you're holding a force for more than 5 seconds, trim it out."
3. **Losing altitude in turns:** Students forget to add collective when banking. Drill: "Bank and pull" — as you roll into the bank, add collective to maintain altitude.
4. **Uncoordinated turns:** Students focus on bank angle and forget the pedals. The ball drifts. Drill: "Step on the ball" — whichever side the ball is on, push that pedal.
5. **Autorotation — delayed collective drop:** The most critical error. Students hesitate to push the collective all the way down. Drill this until it's pure muscle memory: "Engine failure — COLLECTIVE DOWN." The entry must be instinctive.
6. **Autorotation — fixating on the descent:** Students watch the altimeter unwind and freeze, forgetting to establish glide speed. Drill: "Collective down → airspeed → Nr → look outside for landing area." It's a sequence, not a single action.
7. **Speed control during deceleration:** Students raise the nose too aggressively when slowing down, causing a balloon (altitude gain) followed by a sink. Teach: "Small attitude changes — the aircraft will decelerate; be patient."
8. **Not maintaining ball centered:** Students focus on pitch and roll and completely ignore the ball (slip/skid indicator). This leads to uncoordinated flight, which wastes power and is uncomfortable. Include the ball in every scan callout.


---

## Module 7: Navigation

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Program and navigate using waypoints on the MFD NAV page.
2. Interpret the MFD moving map display for situational awareness.
3. Use the AHRS/GPS system for position awareness and navigation.
4. Navigate using TACAN (if available in the DCS module).
5. Use the radar altimeter for terrain awareness and low-level flight.
6. Set and use the transponder for identification.
7. Perform basic dead-reckoning and pilotage navigation as a backup.
8. Plan and execute a cross-country navigation route using the MFD.

---

### 7.1 Navigation Systems Overview

The OH-58D Kiowa Warrior has a modern (for its era) digital navigation suite centered on the AHRS/GPS and displayed on the MFD. This is a significant capability advantage over analog-only helicopters like the UH-1H.

| System | Type | Function |
|---|---|---|
| **AHRS** | Attitude Heading Reference System | Provides attitude (pitch/roll) and magnetic heading. Gyro-stabilized. |
| **GPS** | Global Positioning System | Provides precise lat/long position, ground speed, ground track. |
| **MFD** | Multi-Function Display | Displays moving map, waypoints, navigation data, route lines. |
| **TACAN** | Tactical Air Navigation | UHF-based distance and bearing to a TACAN station (if equipped/modeled in DCS). |
| **Radar altimeter** | Radio altitude | Precise AGL altitude — critical for low-level flight and approach. |
| **Transponder** | IFF / Identification | Squawks Mode 1/2/3/4 for identification by ATC and friendly forces. |

---

### 7.2 MFD NAV Page — Detailed Operation

The MFD NAV page is the primary navigation display. It shows a moving map centered on the aircraft's current position with overlaid waypoints, route lines, and navigation data.

#### NAV Page Elements

| Element | Description |
|---|---|
| **Moving map** | Top-down map showing terrain, coastlines, roads, towns (detail depends on DCS map) |
| **Aircraft symbol** | Centered on the display — shows current position and heading |
| **Waypoints** | Displayed as symbols (typically numbered) on the map along the programmed route |
| **Active waypoint** | Highlighted waypoint the system is navigating to |
| **Route line** | Line connecting waypoints in sequence |
| **Bearing pointer** | Arrow/indicator showing direction to the active waypoint |
| **Distance to waypoint** | Nautical miles to the active waypoint (displayed digitally) |
| **Ground speed** | Current ground speed in knots |
| **Ground track** | Current track over the ground (degrees magnetic) |
| **ETE/ETA** | Estimated time en route / estimated time of arrival to active waypoint (if displayed) |
| **Scale/Zoom** | Map scale — adjustable via OSB buttons |

#### NAV Page Controls (OSB Buttons)

| OSB | Function |
|---|---|
| **Scale +/−** | Zoom in/out on the moving map (e.g., 5 NM, 10 NM, 20 NM, 50 NM ranges) |
| **WPT (waypoint)** | Select active waypoint / cycle through waypoints |
| **D-WPT (direct to waypoint)** | Navigate directly to a selected waypoint, skipping intermediate waypoints |
| **MAP mode** | Switch between track-up and north-up orientation |
| **Page select** | Cycle to other MFD pages (ENG, WPN, SYS, FLT) |

---

### 7.3 Waypoint Programming

Waypoints are typically pre-loaded for DCS missions, but the pilot should verify and be able to modify them.

#### Verifying Waypoints

| Step | Action |
|---|---|
| 1 | Select MFD NAV page |
| 2 | Cycle through waypoints using WPT OSB |
| 3 | For each waypoint, verify the position on the map matches the mission brief |
| 4 | Verify the sequence is correct (WPT 1 → WPT 2 → WPT 3, etc.) |

#### Navigating a Route

| Step | Action |
|---|---|
| 1 | Ensure NAV page is displayed on MFD |
| 2 | The active waypoint is displayed with bearing and distance |
| 3 | Turn to the bearing indicated and fly toward the waypoint |
| 4 | When the aircraft reaches the waypoint (or near it), the system automatically sequences to the next waypoint |
| 5 | If you want to skip to a specific waypoint, use D-WPT (direct to) to select it |

#### Direct-To Navigation

| Step | Action |
|---|---|
| 1 | Press D-WPT OSB on the NAV page |
| 2 | Select the desired waypoint number |
| 3 | The system provides a direct bearing and distance to that waypoint, ignoring intermediate waypoints |
| 4 | Fly the indicated bearing to navigate directly to the selected waypoint |

---

### 7.4 Map Orientation Modes

| Mode | Description | Use |
|---|---|---|
| **Track-up** | Map rotates so the aircraft's track is always pointing "up" on the display | Most intuitive for en route navigation — "up" is where you're going |
| **North-up** | Map is fixed with north at the top; the aircraft symbol rotates | Better for map reading, coordinate reference, and planning |

**Recommendation for BQT:** Use track-up for normal navigation. Switch to north-up when correlating the MFD position with a paper map or mission coordinates.

---

### 7.5 TACAN Navigation

TACAN (Tactical Air Navigation) provides bearing and distance to a ground-based TACAN station (or to another aircraft with TACAN A/A capability).

| Feature | Description |
|---|---|
| **Channels** | 1–126 (X and Y bands) |
| **Bearing** | Magnetic bearing TO the station |
| **Distance** | Slant range in nautical miles |
| **Modes** | T/R (transmit/receive — bearing and distance), REC (receive only — bearing only), A/A (air-to-air) |

#### TACAN Operation

| Step | Action |
|---|---|
| 1 | Set TACAN to desired channel and band (per mission brief or published TACAN chart) |
| 2 | Set mode to T/R for full bearing and distance |
| 3 | Verify bearing and distance readout — bearing pointer on HSI should point toward the station |
| 4 | Navigate by flying the bearing to the station or tracking a specific radial |

**Common TACAN stations in DCS Caucasus map:**

| Station | Channel | Location |
|---|---|---|
| Batumi | 16X | Batumi airfield |
| Senaki | 31X | Senaki-Kolkhi airfield |
| Kutaisi | 44X | Kutaisi-Kopitnari airfield |
| Tbilisi | 25X | Tbilisi-Lochini airfield |
| Sukhumi | 32X | Sukhumi-Babushara airfield |

> *Note: TACAN channels and availability vary by DCS map and mission setup. Always verify per mission brief.*

> *⚠ Realism Divergence: TACAN availability and implementation in the DCS OH-58D module may be simplified or may not be fully modeled. If the module does not include TACAN, the student should rely on AHRS/GPS and the MFD moving map for navigation. The GPS-based navigation system provides equivalent or superior accuracy for DCS purposes.*

---

### 7.6 Radar Altimeter

The radar altimeter provides precise height above ground level (AGL) by bouncing radio waves off the terrain directly below the aircraft.

| Feature | Description |
|---|---|
| **Function** | Displays AGL altitude — precise to within a few feet |
| **Range** | Typically 0–5,000 ft AGL (varies by system) |
| **Decision height bug** | Adjustable bug that provides a visual/audio alert at a set AGL altitude |
| **Primary use** | Low-level flight, approach to hover, terrain awareness |

#### Radar Altimeter Operation

| Step | Action |
|---|---|
| 1 | **Power** — ON (should be powered with avionics) |
| 2 | **Decision height** — Set as desired (e.g., 200 ft for approach, 50 ft for low-level) |
| 3 | **Interpretation** — AGL altitude displayed on gauge. This differs from barometric altitude (MSL). |
| 4 | **Low altitude warning** — When descending through the decision height, an alert (light or tone) activates |

**Important distinction:**
- **Barometric altimeter** = height above sea level (MSL) — set by QNH
- **Radar altimeter** = height above the ground directly below (AGL) — automatic, no setting
- Both are needed: barometric for ATC altitude assignments, radar alt for terrain clearance

**Terrain awareness:**
- In mountainous terrain, the radar altimeter provides critical terrain clearance information that the barometric altimeter cannot.
- Example: If flying at 3,000 ft MSL over a 2,500 ft ridge, the barometric altimeter shows 3,000 ft, but the radar altimeter correctly shows 500 ft AGL.
- Always cross-reference radar altimeter with barometric altimeter and outside visual references.

---

### 7.7 Transponder / IFF

The transponder provides identification and altitude encoding for ATC and friendly forces.

| Mode | Function |
|---|---|
| **Mode 1** | Military identification (2-digit code, unit/mission specific) |
| **Mode 2** | Military identification (4-digit code, individual aircraft specific) |
| **Mode 3/A** | Standard ATC transponder code (4-digit squawk code) |
| **Mode C** | Altitude encoding — automatically transmits barometric altitude to ATC |
| **Mode 4** | Encrypted IFF — crypto-based friend/foe identification |

#### Transponder Operation

| Step | Action |
|---|---|
| 1 | Set transponder to STBY (standby) during startup |
| 2 | Set Mode 3/A squawk code per ATC assignment or mission brief (e.g., 1200 for VFR, or assigned discrete code) |
| 3 | Before takeoff, set transponder to ON (or ALT for altitude encoding) |
| 4 | If directed by ATC: "Squawk [code]" — set the assigned code |
| 5 | If directed: "Ident" — press the IDENT button (sends a highlighted return to ATC radar) |
| 6 | After landing, set transponder back to STBY |

> *⚠ Realism Divergence: Transponder/IFF implementation in DCS varies by module. The OH-58D module may have a simplified transponder panel or may not model all modes. In many DCS missions, the transponder is not critical for gameplay. The student should set it per SOP for procedural discipline.*

---

### 7.8 Dead Reckoning and Pilotage

Even with GPS and the MFD, the pilot should be capable of basic visual navigation.

#### Pilotage (Visual Navigation)

| Technique | Description |
|---|---|
| **Map reading** | Correlate visible ground features (rivers, roads, coastlines, towns, mountains) with the map |
| **Checkpoint navigation** | Identify planned checkpoints (visual waypoints) and navigate between them |
| **Time-distance** | Use known ground speed and elapsed time to estimate position between checkpoints |

#### Dead Reckoning

| Step | Action |
|---|---|
| 1 | From a known position, fly a known heading at a known ground speed |
| 2 | After a measured time interval, estimate current position along the planned track |
| 3 | Correct for wind drift by comparing planned track to actual ground track |

**When to use dead reckoning:**
- GPS failure or degradation
- AHRS failure (heading unreliable) — use magnetic compass as backup
- Verification of GPS position against visual references (trust but verify)

---

### 7.9 Cross-Country Navigation Procedure

A basic cross-country flight using the MFD:

| Phase | Action |
|---|---|
| **Pre-flight** | Review mission brief for waypoints, altitudes, frequencies, NOTAMs. Verify waypoints loaded on MFD. Plan fuel for the route. |
| **Departure** | After takeoff and climb to en route altitude, verify NAV page shows active waypoint and bearing. Turn to intercept the course line. |
| **En route** | Follow bearing/distance to each waypoint. Monitor ground speed and ETE. Compare MFD position to outside visual references. Adjust heading for wind drift. |
| **At each waypoint** | Verify position agrees with expected visual references. System should auto-sequence to next waypoint. If not, manually select next waypoint. |
| **Arrival** | As destination appears on the map and visually, transition to approach navigation (pattern entry, ATC communications). |

---

### 7.10 Cockpit Switch Reference — Module 7

| Control | Location | Function | DCS Action |
|---|---|---|---|
| **MFD NAV page** | MFD bezel — OSB buttons | Select and operate NAV page | Mouse click on OSB |
| **MFD scale/zoom** | MFD bezel — OSB | Adjust map zoom level | Mouse click on +/− OSB |
| **MFD WPT select** | MFD bezel — OSB | Cycle active waypoint | Mouse click |
| **MFD D-WPT** | MFD bezel — OSB | Direct-to waypoint navigation | Mouse click |
| **MFD map mode** | MFD bezel — OSB | Toggle track-up / north-up | Mouse click |
| **TACAN channel** | TACAN control panel | Set channel and X/Y band | Mouse scroll / click |
| **TACAN mode** | TACAN control panel | OFF / REC / T/R / A/A | Mouse click to cycle |
| **Radar altimeter** | Instrument panel | ON/OFF, decision height knob | Mouse click / scroll |
| **Transponder mode** | Transponder panel | OFF / STBY / ON / ALT | Mouse click to cycle |
| **Transponder code** | Transponder panel | Set Mode 3/A squawk code (4 digits) | Mouse scroll on each digit |
| **IDENT button** | Transponder panel | Sends identification pulse to ATC | Mouse click |
| **Magnetic compass** | Instrument panel (standby) | Backup heading reference | Visual reference only |
| **Barometric altimeter** | Instrument panel | QNH/QFE setting via knob | Mouse scroll |

---

### 7.11 Instructor Notes — Module 7

**Common student errors:**

1. **GPS fixation / head-down:** Students stare at the MFD moving map and lose outside visual awareness. Drill: "The MFD is a tool, not a windshield. 80% outside, 20% instruments." For VFR flight, outside visual reference is primary.
2. **Wrong map scale:** Students leave the map zoomed in too tight and lose the big picture, or zoomed out too far and can't correlate local features. Teach: "Use tight zoom (5–10 NM) for local pattern work, medium (20 NM) for en route, wide (50 NM) for big-picture SA."
3. **Not verifying waypoints before departure:** Students assume the loaded waypoints are correct and discover errors en route. Drill: "Brief and verify every waypoint on the ground."
4. **Confusing barometric and radar altitude:** Students report AGL when ATC asks for altitude (MSL), or fly a barometric altitude in mountainous terrain without checking radar alt. Drill the distinction: "ATC speaks MSL. Terrain speaks AGL. Know which you need."
5. **Forgetting to set altimeter QNH:** Students fly with the previous flight's or a default altimeter setting, causing altitude errors. Include altimeter setting in every pre-flight checklist.
6. **Not correlating MFD with visual:** Students trust the MFD blindly and don't verify position against outside references. This is a problem if GPS degrades. Drill: "At every waypoint, look outside and confirm you see what you expect to see."
7. **Transponder left in standby:** Students forget to set the transponder to ON/ALT before takeoff, making them invisible to ATC radar. Include transponder in the pre-takeoff checklist.
8. **Poor track keeping:** Students wander off course between waypoints, making lazy S-turns instead of flying direct. Teach: "Point the aircraft at the waypoint, correct for wind, and hold the heading."


---

## Module 8: Emergency Procedures

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Execute all boldface (memory) emergency procedures without reference.
2. Perform a full autorotation to touchdown.
3. Recognize and recover from Vortex Ring State (VRS / Settling with Power).
4. Recognize and recover from Loss of Tail Rotor Effectiveness (LTE).
5. Respond to a FADEC failure (auto to manual transition).
6. Respond to a hydraulic failure (degraded flight controls).
7. Respond to electrical and generator failures.
8. Respond to transmission oil pressure/temperature cautions.
9. Recognize and respond to dynamic rollover.
10. Recognize and respond to ground resonance.
11. Perform emergency procedures for in-flight fire (engine, electrical, cabin).
12. Understand which emergencies are modeled in DCS and which are conceptual.

---

### 8.1 Boldface Emergency Procedures

**Boldface** items are memorized emergency procedures that must be executed immediately from memory. They are called "boldface" because they are printed in bold in the aircraft Technical Manual (-10). These are time-critical emergencies where delay could be catastrophic.

#### ENGINE FAILURE — IN FLIGHT

> **1. COLLECTIVE — FULL DOWN (immediately)**
> **2. AIRSPEED — 72 KIAS (best glide) or 55 KIAS (minimum sink)**
> **3. Nr — MONITOR (maintain 90–107%)**
> **4. THROTTLE — IDLE (if not already)**
> **5. MAYDAY call — "MAYDAY, MAYDAY, MAYDAY, [Callsign], engine failure, [position], [altitude], [souls on board]"**
> **6. SELECT LANDING AREA — Turn toward the best available landing site**
> **7. EXECUTE AUTOROTATION TO TOUCHDOWN (see 8.2)**

#### ENGINE FAILURE — AT HOVER (LOW ALTITUDE)

> **1. COLLECTIVE — MAINTAIN (cushion the landing)**
> **2. LEVEL the aircraft with cyclic**
> **3. PEDALS — Maintain heading if possible**
> **4. ACCEPT the landing — do NOT try to fly away**

*At very low altitude/hover, there is not enough height to enter autorotation. The stored energy in the rotor system is used to cushion the landing. The collective should NOT be dumped — use whatever rotor inertia is available to reduce the sink rate at touchdown.*

#### GROUND RESONANCE

> **If Nr is NORMAL (97–101%):**
> **1. COLLECTIVE — INCREASE (FLY AWAY IMMEDIATELY)**
>
> **If Nr is LOW or DECAYING:**
> **1. COLLECTIVE — FULL DOWN**
> **2. THROTTLE — OFF**
> **3. ROTOR BRAKE — APPLY (when safe)**

#### FADEC FAILURE / MANUAL REVERSION

> **1. THROTTLE — ASSUME MANUAL CONTROL**
> **2. Nr — MAINTAIN 97–101% with throttle**
> **3. AVOID RAPID COLLECTIVE INPUTS (throttle response is slower in manual)**
> **4. LAND AS SOON AS PRACTICABLE**

#### HYDRAULIC FAILURE

> **1. CONTROLS — EXPECT VERY HEAVY FORCES**
> **2. AVOID ABRUPT INPUTS**
> **3. AIRSPEED — MAINTAIN 60–80 KIAS (manageable control forces)**
> **4. LAND AS SOON AS POSSIBLE — RUN-ON LANDING RECOMMENDED**
> **5. Do NOT attempt to hover** (control forces in hover are extreme without hydraulics)

#### TAIL ROTOR FAILURE / LOSS OF TAIL ROTOR AUTHORITY

> **1. ENTER AUTOROTATION (reduce power to eliminate torque)**
> **2. AIRSPEED — 72 KIAS (best autorotation glide)**
> **3. EXECUTE AUTOROTATION TO TOUCHDOWN**
> **4. At touchdown, use directional control available (skid friction, collective reduction)**

#### ENGINE FIRE — IN FLIGHT

> **1. THROTTLE — IDLE**
> **2. FUEL SHUTOFF — CLOSED**
> **3. ENTER AUTOROTATION**
> **4. LAND IMMEDIATELY**
> **5. EVACUATE AIRCRAFT after touchdown**

#### ELECTRICAL FIRE

> **1. BATTERY — OFF**
> **2. GENERATOR — OFF**
> **3. IDENTIFY and isolate the source if possible**
> **4. VENTILATE cockpit (open vents/windows if possible)**
> **5. LAND AS SOON AS POSSIBLE**
> **6. If fire persists after electrical shutdown, LAND IMMEDIATELY and evacuate**

---

### 8.2 Full Autorotation — Touchdown Procedure

This expands on the practice autorotation entry (Module 6) to include the full sequence through touchdown.

#### Phase 1: Entry (0–3 seconds)

| Step | Action | Notes |
|---|---|---|
| 1 | **Collective — FULL DOWN** | Immediate — this is the most critical action. Preserves Nr. |
| 2 | **Airspeed — Establish 72 KIAS (best glide)** or **55 KIAS (min sink)** | 72 KIAS for maximum glide distance to a landing zone. 55 KIAS for minimum rate of descent (less distance covered). |
| 3 | **Nr — Monitor 90–107%** | Nr should stabilize in this range with collective down at glide speed. |
| 4 | **Pedals — Adjust for coordination** | Right pedal typically needed (no engine torque to counteract). |
| 5 | **MAYDAY call** | Transmit on current frequency and/or guard. |

#### Phase 2: Glide (majority of descent)

| Step | Action | Notes |
|---|---|---|
| 1 | **Select landing area** | Ideally flat, clear, into the wind. Accept the best available option. |
| 2 | **Turn toward landing area** | Gentle banked turns — avoid steep turns that increase sink rate. |
| 3 | **Maintain 72 KIAS and monitor Nr** | Cross-check airspeed and Nr throughout the glide. |
| 4 | **Plan the approach** | Aim for a point approximately 1/3 from the near edge of the landing area. |
| 5 | **Descent rate** | ~1,500–2,000 fpm — rapid descent. The OH-58D has limited glide distance. |

#### Phase 3: Flare (approximately 75–100 ft AGL)

| Step | Action | Notes |
|---|---|---|
| 1 | **Begin flare — aft cyclic** | At approximately 75–100 ft AGL, pull the cyclic aft to raise the nose. |
| 2 | **Purpose of flare** | Reduces forward airspeed and rate of descent. Trades airspeed for rotor RPM — Nr increases. |
| 3 | **Nr increase** | The flare causes the rotor to speed up (windmilling effect). This stores energy in the rotor for the collective pull in Phase 4. |
| 4 | **Airspeed decreasing** | From 72 KIAS, airspeed should decrease through the flare to approximately 20–30 KIAS. |
| 5 | **Attitude** | Nose high — approximately 20–30° nose up during the flare. |

#### Phase 4: Cushion and Touchdown (last 10–15 ft)

| Step | Action | Notes |
|---|---|---|
| 1 | **Level the aircraft** — forward cyclic to bring the nose toward level | The aircraft should be approximately level or slightly nose-up at touchdown |
| 2 | **Collective — PULL** — apply collective to use remaining rotor energy to cushion the landing | This is the "collective pull" — timing is critical. Too early and you run out of rotor energy high. Too late and you hit hard. |
| 3 | **Touchdown** — accept the landing | Expect a firm but survivable landing. Skids should contact the ground at near-zero forward speed if the flare was properly timed. |
| 4 | **After touchdown** — collective full down, throttle off, secure aircraft | Shut down all systems. Evacuate if fire or fuel leak is suspected. |

**Autorotation performance data (OH-58D approximate):**

| Parameter | Value |
|---|---|
| **Best glide speed** | 72 KIAS |
| **Minimum sink speed** | 55 KIAS |
| **Rate of descent (glide)** | ~1,500–2,000 fpm |
| **Glide ratio** | Approximately 4:1 (4 ft forward for every 1 ft of altitude lost) — *estimated* |
| **Nr range** | 90–107% (autorotation) |
| **Flare initiation** | ~75–100 ft AGL |
| **Minimum altitude for autorotation entry** | ~500+ ft AGL at speed; lower if already established in autorotation profile |

> *⚠ Realism Divergence: DCS autorotation behavior varies significantly from real-world. The flare effectiveness, cushion timing, and touchdown dynamics may be simplified or differ from the real aircraft. The student should practice extensively in DCS to learn the module's specific autorotation "feel." Common DCS-specific issues include: overly sensitive/insensitive flare, Nr decay rate differences, and touchdown impact tolerance. Real-world autorotation to touchdown in a Kiowa is a complex skill requiring extensive practice — in DCS, the physics model may be more forgiving or less forgiving depending on the implementation.*

---

### 8.3 Vortex Ring State (VRS) / Settling with Power

VRS occurs when the helicopter descends into its own rotor downwash, creating a turbulent vortex around the rotor disc that dramatically reduces lift.

#### Conditions for VRS

All three conditions must be present simultaneously:
1. **Low airspeed** — below effective translational lift (below ~16–24 KIAS)
2. **High rate of descent** — typically exceeding 300–500 fpm
3. **Power applied** — collective is not full down (not in autorotation)

#### Recognition

| Indication | Description |
|---|---|
| **Vibration increase** | Turbulent airflow causes noticeable vibration |
| **Uncommanded descent** | Rate of descent increases despite collective input |
| **Power ineffective** | Adding collective does not arrest the descent — it may worsen it |
| **Erratic instruments** | Airspeed indicator and VSI may fluctuate |
| **Mushing / wallowing** | Aircraft feels sluggish and unresponsive |

#### Recovery Procedure

> **1. CYCLIC — FORWARD (lower the nose aggressively)**
> **2. GAIN AIRSPEED — Accelerate through ETL**
> **3. COLLECTIVE — Adjust as speed increases (may need to reduce initially to help nose drop)**
> **4. ALTITUDE — Sacrifice altitude for airspeed**

**The key recovery action is to fly out of the vortex ring by gaining forward airspeed.** Once the rotor disc moves through clean air (above ETL speed), normal lift generation resumes.

**Prevention:**
- Avoid descending vertically or at very low airspeed with power on.
- In approaches, maintain at least 30+ KIAS until short final or descend at rates below 300 fpm.
- If conditions require a steep/vertical descent, lower the collective and enter autorotation (controlled descent through the vortex ring from below does not create VRS).

---

### 8.4 Loss of Tail Rotor Effectiveness (LTE)

LTE is a condition where the tail rotor becomes unable to counteract main rotor torque, resulting in an uncommanded yaw (spin) to the right (for American helicopters with counterclockwise-rotating main rotors).

#### Conditions Favoring LTE

| Condition | Description |
|---|---|
| **Low airspeed** | Below ETL, the tail rotor receives disturbed airflow |
| **High power setting** | High collective = high torque = high tail rotor demand |
| **Left crosswind** | Wind from the left can blank or interfere with tail rotor effectiveness |
| **Tail wind** | Tail wind can reduce the relative airflow over the tail rotor |
| **Right turns at low speed** | Entering a right turn at low speed can place the tail rotor in the main rotor's vortex wake |

#### Recognition

| Indication | Description |
|---|---|
| **Uncommanded right yaw** | Aircraft yaws right and pedal input cannot stop it |
| **Spin** | If uncorrected, the yaw accelerates into a spin |
| **Full left pedal — no effect** | The tail rotor is stalled or blanked; pedal authority is lost |

#### Recovery Procedure

> **1. PEDALS — FULL LEFT (attempt to stop the yaw)**
> **2. COLLECTIVE — REDUCE (decrease torque, which reduces tail rotor demand)**
> **3. CYCLIC — FORWARD (gain airspeed to restore tail rotor effectiveness)**
> **4. IF UNABLE TO RECOVER — Enter autorotation (collective full down eliminates torque completely)**

**Prevention:**
- Avoid hovering with a left crosswind or tailwind.
- Avoid high-power, low-airspeed flight conditions.
- Be cautious during right pedal turns at low speed.
- Maintain awareness of wind direction during all low-speed operations.

---

### 8.5 FADEC Failure — Manual Reversion

If the FADEC fails or must be manually overridden, the pilot assumes throttle control.

#### Indications of FADEC Failure

| Indication | Description |
|---|---|
| **FADEC caution light** | Illuminates on the caution panel |
| **Nr fluctuation** | Rotor RPM may vary if FADEC cannot govern |
| **TOT exceedance** | FADEC no longer limiting TOT — pilot must monitor |
| **Uncommanded power changes** | Engine power may surge or droop |

#### Procedure

| Step | Action | Notes |
|---|---|---|
| 1 | **Recognize FADEC failure** | Caution light, Nr fluctuation, uncommanded power change |
| 2 | **FADEC mode — MANUAL** (if not already) | Switch from AUTO to MAN on the FADEC panel |
| 3 | **Throttle — Assume manual control** | The pilot must now manage Nr by adjusting the throttle manually |
| 4 | **Nr — Maintain 97–101%** | The throttle correlator provides a baseline, but the pilot must fine-tune |
| 5 | **Avoid rapid collective inputs** | Without FADEC, Nr response to collective changes is slower; large collective inputs cause Nr droop or overspeed |
| 6 | **Monitor TOT and torque manually** | FADEC no longer protects against exceedances — the pilot must stay within limits |
| 7 | **Land as soon as practicable** | MANUAL mode is a degraded state — the aircraft is flyable but pilot workload is significantly increased |

> *⚠ Realism Divergence: DCS FADEC failure implementation may differ significantly from the real aircraft. The real T703 has multi-level FADEC redundancy before full manual reversion. DCS may provide a single AUTO/MAN toggle with simplified throttle dynamics. The student should practice manual throttle management in DCS to understand the module's specific behavior. Key differences to test: Nr response time to collective changes, TOT behavior during power changes, and hover stability without FADEC.*

---

### 8.6 Hydraulic Failure

The OH-58D has a single hydraulic system powering irreversible servo actuators for the flight controls.

#### Indications

| Indication | Description |
|---|---|
| **HYD PRESS caution light** | Hydraulic pressure has dropped below normal |
| **Heavy controls** | Cyclic, collective, and pedals become extremely difficult to move |
| **Hydraulic pressure gauge** | Reads low or zero (normal: ~1,000 PSI) |

#### Procedure

| Step | Action | Notes |
|---|---|---|
| 1 | **Confirm hydraulic failure** | HYD PRESS light, heavy controls, gauge reading |
| 2 | **Do NOT make abrupt control inputs** | Without hydraulic boost, forces are extreme. Sudden inputs can cause structural damage or loss of control. |
| 3 | **Maintain 60–80 KIAS** | This speed range provides the most manageable control forces |
| 4 | **Avoid hover** | Hovering without hydraulics requires ~40–50 lbs of cyclic force. It is nearly impossible to maintain precision hover without hydraulics. |
| 5 | **Plan a run-on landing** | Fly an approach that terminates in a forward-speed touchdown (run-on) rather than a hover. |
| 6 | **Approach at 50–60 KIAS** | Maintain speed through the approach. Accept a forward-speed touchdown on a runway or flat surface. |
| 7 | **Touchdown** | Allow the aircraft to slide on the skids at forward speed. Do not attempt to bring the aircraft to a hover before landing. |
| 8 | **After landing** — Shut down normally | Control forces return to normal once the rotor stops. |

> *⚠ Realism Divergence: DCS hydraulic failure may not accurately replicate the extreme control forces experienced in the real aircraft (estimated ~40–50 lbs cyclic force in hover, ~10–20 lbs at speed). The DCS implementation may feel "heavy" but manageable in ways that would be unrealistic. The student should still practice the correct procedure: avoid hover, fly a run-on landing, maintain 60–80 KIAS.*

---

### 8.7 Electrical Failures

#### Generator Failure

| Step | Action | Notes |
|---|---|---|
| 1 | **GEN caution light** illuminates | Generator has dropped offline |
| 2 | **Check generator switch** — Verify ON | May have tripped — try resetting |
| 3 | **If generator does not reset** — Aircraft is now on battery power only | Battery endurance: ~30 minutes under reduced load |
| 4 | **Reduce electrical load** | Turn off non-essential equipment (MMS, search light, any non-critical avionics) |
| 5 | **Land as soon as practicable** | Battery time is limited |

#### Complete Electrical Failure

| Step | Action | Notes |
|---|---|---|
| 1 | **Loss of all electrical power** | All instruments, lights, radios, and caution panel go dark |
| 2 | **Engine continues to run** | The T703 engine with FADEC may continue running on residual power, but the student should be prepared for engine complications |
| 3 | **Fly by standby instruments** | Magnetic compass (no power required), standby attitude indicator (if battery-backed), outside visual references |
| 4 | **Attempt to restore power** | Battery switch — cycle OFF then ON. Generator — cycle OFF then ON. |
| 5 | **If power cannot be restored** — Land as soon as possible | Without instruments, land at the nearest suitable location using visual references. |

---

### 8.8 Transmission Oil System Cautions

| Caution | Meaning | Action |
|---|---|---|
| **XMSN OIL PRESS** | Transmission oil pressure low | Land as soon as possible. Transmission failure can be catastrophic. Monitor for unusual vibration or noise. |
| **XMSN OIL TEMP** | Transmission oil temperature high | Reduce power if possible. Land as soon as practicable. High temperature degrades lubricant and can lead to transmission seizure. |

**Transmission failure (catastrophic):** If the transmission seizes, the main rotor may decouple from the engine. Immediate autorotation is required. This is one of the most serious emergencies — the student should recognize transmission cautions early and land before catastrophic failure occurs.

---

### 8.9 Dynamic Rollover

Dynamic rollover occurs when the helicopter begins to rotate about a fixed point on the ground (typically a skid) and the roll rate exceeds the pilot's ability to correct it.

#### Conditions

| Condition | Description |
|---|---|
| **One skid on the ground** | One skid is in contact while the other lifts — slope landing, crosswind, lateral drift |
| **Increasing collective** | Adding collective while one skid is anchored creates a rolling moment |
| **Lateral cyclic insufficient** | The cyclic cannot overcome the roll once a critical angle is passed (~5–8° depending on conditions) |

#### Recognition

| Indication | Description |
|---|---|
| **Lateral roll that does not respond to cyclic** | The aircraft continues rolling despite opposite cyclic input |
| **One skid lifting while the other is planted** | Visible through peripheral vision or attitude indicator |
| **Increasing roll rate** | Once past the critical angle, the roll accelerates |

#### Recovery (if roll has not exceeded critical angle)

> **1. COLLECTIVE — REDUCE (lower the lifting force)**
> **2. CYCLIC — INTO the roll (attempt to level the aircraft)**
> **3. Allow the aircraft to settle back onto both skids**

**If past the critical angle:** The roll is unrecoverable. The aircraft will roll over. Collective reduction is still the primary action — it may reduce the violence of the rollover.

**Prevention:**
- Lift off and land vertically — avoid lateral drift during takeoff and landing
- On slopes, use proper slope landing technique (uphill skid first on landing, downhill skid last on takeoff)
- Be cautious in crosswinds during ground operations
- Move the cyclic to the downslope side before raising the collective on a slope

---

### 8.10 Mast Bumping (Less Relevant to OH-58D)

The OH-58D's bearingless rotor system does not have the classic flap stop / mast bumping vulnerability of teetering (semi-rigid) rotor systems like the UH-1H. However, the student should understand:

- **Low-G / pushover risk:** Aggressive forward cyclic (pushing the nose down) in any helicopter can unload the rotor disc. In extreme cases, the blade can contact the mast or fuselage.
- **Prevention:** Avoid abrupt forward cyclic inputs, particularly at low airspeed or during turbulence. Maintain positive G loading at all times.

---

### 8.11 In-Flight Fire

#### Engine Fire

| Step | Action |
|---|---|
| 1 | **Throttle — IDLE** |
| 2 | **Fuel shutoff — CLOSED** |
| 3 | **Enter autorotation** |
| 4 | **Land immediately** |
| 5 | **Evacuate after touchdown** |

#### Electrical Fire

| Step | Action |
|---|---|
| 1 | **Battery — OFF** |
| 2 | **Generator — OFF** |
| 3 | **Identify source** — smell, smoke location, circuit breaker popped |
| 4 | **Ventilate** — open vents if available |
| 5 | **If fire extinguishes** — Land as soon as possible |
| 6 | **If fire persists** — Land immediately, evacuate |

#### Cabin Fire (non-electrical)

| Step | Action |
|---|---|
| 1 | **Attempt to extinguish** with onboard extinguisher if available |
| 2 | **Land immediately** |
| 3 | **Evacuate** |

---

### 8.12 DCS-Modeled vs. Conceptual Emergencies

Not all emergencies are modeled in DCS. The student should know which can be practiced in-sim and which are conceptual knowledge.

| Emergency | DCS Modeled? | Notes |
|---|---|---|
| **Engine failure** | ✅ Yes | Can simulate by rolling throttle to idle or using failure menu |
| **Autorotation** | ✅ Yes | Modeled — fidelity varies; practice extensively |
| **FADEC failure** | ⚠ Partially | May be triggered via failure menu; manual mode behavior may be simplified |
| **Hydraulic failure** | ⚠ Partially | May be triggered via failure menu; control force modeling varies |
| **VRS / Settling with power** | ✅ Yes | Usually well-modeled in DCS helicopter modules |
| **LTE** | ⚠ Partially | May be modeled; test by hovering with left crosswind at high power |
| **Ground resonance** | ⚠ Unknown | May or may not be modeled for the OH-58D; test empirically |
| **Dynamic rollover** | ⚠ Partially | Some DCS modules model this; test on slopes |
| **Mast bumping** | ❌ Unlikely | Not typically modeled for bearingless rotor systems |
| **Transmission failure** | ⚠ Partially | May be available via failure menu |
| **Generator failure** | ✅ Yes | Available via failure menu |
| **Complete electrical failure** | ✅ Yes | Available via failure menu |
| **Engine fire** | ⚠ Partially | Visual fire effects may be modeled; damage model varies |
| **Electrical fire** | ❌ Unlikely | Typically not modeled with visual effects |

> *To practice emergencies in DCS: use the in-game Mission Editor failure triggers, the in-flight failure menu, or the DCS "Random Failures" option. The student should practice each modeled emergency multiple times until the boldface procedures are automatic.*

---

### 8.13 Cockpit Switch Reference — Module 8

| Control | Function | DCS Action |
|---|---|---|
| **Collective** | Full down for autorotation entry; cushion for low-altitude engine failure | Joystick axis |
| **Throttle** | IDLE for autorotation practice; OFF for shutdown | Keyboard or axis |
| **Fuel shutoff** | CLOSED for engine fire or fuel emergency | Mouse click |
| **FADEC mode** | AUTO / MAN — switch during FADEC failure | Mouse click |
| **Battery switch** | OFF for electrical fire | Mouse click |
| **Generator switch** | OFF for electrical fire / generator failure | Mouse click |
| **Rotor brake** | Apply during ground resonance shutdown procedure | Mouse click |
| **Caution panel** | Monitor for all emergency indications | Visual reference |
| **Nr tachometer** | Critical during autorotation and ground resonance decisions | Visual reference |
| **TOT gauge** | Monitor during FADEC failure (manual mode) | Visual reference |
| **Hydraulic pressure gauge** | Confirm hydraulic failure | Visual reference |

---

### 8.14 Instructor Notes — Module 8

**Common student errors:**

1. **Delayed collective drop on engine failure:** This is the #1 killer in real-world autorotations and the #1 error in simulation. Students hesitate, try to diagnose, or instinctively pull collective (wrong direction). Drill: "Engine failure = collective DOWN. No thinking. No diagnosing. Down." Practice the entry 50+ times until it is purely reflexive.
2. **Flare timing — too early or too late:** Too early: the aircraft arrests forward speed but still has a high sink rate and no rotor energy left. Too late: the aircraft hits the ground at high speed. Drill: "Start the flare at 75–100 ft AGL. Watch the ground, not the altimeter."
3. **Not looking for a landing area during the glide:** Students fixate on instruments during autorotation and forget to look outside for a landing zone. Drill: "Instruments tell you how you're doing. Your eyes tell you where you're going. Look outside."
4. **VRS panic — pulling collective:** Students in VRS instinctively pull collective (more power), which worsens VRS by increasing the rate of descent. Drill: "VRS = nose down, get speed. Do NOT pull."
5. **LTE — not reducing power:** Students in LTE try to fight the yaw with pedal alone. If pedal is insufficient, they must reduce collective to reduce torque. Drill: "Can't stop the yaw with pedal? Lower the collective."
6. **Hydraulic failure — attempting to hover:** Students forget that hovering without hydraulics requires extreme force and attempt a normal approach to a hover. This almost always results in loss of control. Drill: "Hydraulic failure = run-on landing. Period. No hover."
7. **Not declaring MAYDAY:** Students forget to make emergency radio calls, especially under stress. Drill: after the boldface items are complete and the aircraft is under control, the next action is always MAYDAY.
8. **Ground resonance — hesitation:** Students feel the vibration and try to diagnose it instead of acting immediately. Ground resonance destroys aircraft in seconds. Drill: "Vibration on the ground = fly or shut down. NOW. No thinking."
9. **Dynamic rollover — not reducing collective:** Students try to stop a roll with cyclic alone. Once the roll starts, collective must come down to remove the lifting force. Drill: "Rolling on the ground? Collective DOWN first, then cyclic."
10. **FADEC manual mode — not monitoring TOT:** Students switch to manual and focus entirely on Nr, forgetting that FADEC is no longer protecting TOT. A TOT exceedance in manual mode can damage the engine. Drill: "In manual mode, you ARE the FADEC. Monitor Nr AND TOT AND torque."


---

## Module 9: Approach & Landing

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Fly a standard VFR traffic pattern (downwind, base, final) with correct altitudes, airspeeds, and radio calls.
2. Perform a normal approach to a hover and landing.
3. Perform a steep approach (for confined areas or obstacle clearance on short final).
4. Perform a shallow approach (for low-obstacle environments or reduced power situations).
5. Execute a go-around from any point in the approach.
6. Perform a crosswind approach and landing.
7. Perform a slope landing.
8. Perform a confined area approach and landing.
9. Perform a pinnacle approach and landing.
10. Manage the deceleration from cruise to hover through the approach phase.

---

### 9.1 VFR Traffic Pattern

The standard VFR helicopter traffic pattern is similar to fixed-wing but typically flown at lower altitudes and speeds.

#### Pattern Geometry

```
                   Crosswind                              
              ┌─────────────────┐                         
              │                 │                         
  Departure   │                 │   Base                  
  (Upwind)    │                 │                         
              │                 │                         
  ────────────┘   Downwind      └────────────────         
  ◄─── Runway ────────────────────────────►  Final        
       13                                  Approach       
```

#### Pattern Parameters

| Leg | Altitude (AGL) | Airspeed | Distance from Runway | Notes |
|---|---|---|---|---|
| **Departure (Upwind)** | Climbing through pattern alt | 55–60 KIAS (Vy) | Over the runway | Straight ahead climb after takeoff |
| **Crosswind** | At pattern altitude | 70–80 KIAS | Turning 90° from runway heading | Turn crosswind at ~300–500 ft AGL |
| **Downwind** | Pattern altitude (500–700 ft AGL typical) | 80–90 KIAS | ~½ to 1 mile parallel to runway | Abeam the numbers, begin approach checks |
| **Base** | Descending | 60–70 KIAS | Turning 90° toward runway | Begin descent, reduce speed |
| **Final** | Descending to landing | 50–60 KIAS, decelerating | Aligned with runway/landing zone | Final approach, decelerate to hover |

> *Note: Pattern altitude and distance may vary by airfield and local procedures. In DCS, typical helicopter pattern altitude is 500–700 ft AGL. Check mission brief or published procedures.*

#### Radio Calls in the Pattern

| Position | Call |
|---|---|
| **Entering downwind** | "[Tower], [Callsign], entering left/right downwind runway [number]" |
| **Turning base** | "[Tower], [Callsign], turning base runway [number]" |
| **Final** | "[Tower], [Callsign], final runway [number], [type] landing" |
| **Go-around** | "[Tower], [Callsign], going around" |
| **Clear of runway** | "[Ground], [Callsign], clear of runway [number]" |

---

### 9.2 Approach — Abeam-to-Touchdown Sequence

The approach begins abeam the intended landing point on the downwind leg and ends at touchdown.

#### Downwind Leg (Abeam the Numbers)

| Step | Action |
|---|---|
| 1 | **Abeam the landing zone** — note position, begin pre-landing checks |
| 2 | **Pre-landing checklist:** |
|   | • Fuel — sufficient for go-around and re-pattern |
|   | • Engine instruments — green |
|   | • Landing light — as required |
|   | • Radar altimeter — set decision height (e.g., 50 ft) |
|   | • Harness — locked |
| 3 | **Report:** "[Tower], [Callsign], abeam, downwind, runway [number]" (optional, per local procedure) |

#### Base Turn

| Step | Action |
|---|---|
| 1 | **Approximately 45° past the abeam point**, turn base |
| 2 | **Begin descent** — reduce collective, maintain 60–70 KIAS |
| 3 | **Announce:** "[Tower], [Callsign], turning base" |
| 4 | **Rate of descent** — approximately 300–500 fpm |
| 5 | **Configure for approach** — begin decelerating toward approach speed |

#### Final Approach

| Step | Action |
|---|---|
| 1 | **Roll wings level on final** — aligned with the landing zone |
| 2 | **Airspeed** — 50–60 KIAS, decelerating |
| 3 | **Glide path** — approximately 6–10° (normal approach angle) |
| 4 | **Announce:** "[Tower], [Callsign], final runway [number], full stop" |
| 5 | **Continue deceleration** — coordinated aft cyclic, collective as needed to manage descent rate |
| 6 | **At ~200 ft AGL / ½ mile** — airspeed ~40–50 KIAS, descent rate decreasing |
| 7 | **At ~100 ft AGL** — airspeed ~30–40 KIAS, clearly decelerating toward hover |
| 8 | **At ~50 ft AGL** — approaching hover speed, near-hover power applied |
| 9 | **Arrive at hover** over intended landing point at 3–5 ft skid height, zero forward speed |
| 10 | **Hover and verify position** — clear of obstacles, stable |
| 11 | **Land** — slowly lower collective, settle onto skids |

---

### 9.3 Normal Approach — Detailed

The normal approach is a constant-angle, constant-deceleration approach terminating in a hover over the intended landing point.

| Parameter | Value |
|---|---|
| **Approach angle** | ~6–10° (moderate) |
| **Entry airspeed** | 60–70 KIAS (turning final) |
| **Termination** | Hover at 3–5 ft over the landing point |
| **Power** | Gradually increasing from reduced (descent) to hover power |
| **Key skill** | Coordinating deceleration and descent so that the aircraft arrives at the landing point at hover speed and hover height simultaneously |

**The approach is essentially managing two variables to arrive at the same point at the same time:**
1. **Forward speed** → must reach zero (hover) at the landing point
2. **Altitude** → must reach hover height (~3–5 ft) at the landing point

If the student arrives at the landing point too fast, they overshoot (go-around). If too slow/high, they must hover forward or descend further. If too low, they risk dragging the skids before reaching the point.

---

### 9.4 Steep Approach

Used when obstacles on the approach path require a steeper-than-normal glide angle, or when landing in a confined area surrounded by tall obstacles.

| Parameter | Value |
|---|---|
| **Approach angle** | ~12–15° (steep) |
| **Entry airspeed** | 50–60 KIAS (slower than normal) |
| **Power** | Lower than normal approach initially (to descend steeply), increasing as speed decreases |
| **Risk** | Higher sink rate near the ground if power management is poor; VRS risk if descending too steeply at low airspeed |
| **Termination** | Hover or near-hover over the landing point |

#### Procedure

| Step | Action |
|---|---|
| 1 | On final, establish a steeper nose-down attitude with reduced power |
| 2 | Maintain 50–60 KIAS initially |
| 3 | Decelerate progressively — the approach angle requires a more aggressive deceleration profile |
| 4 | As speed decreases below 40 KIAS, increase collective to arrest the descent rate |
| 5 | Transition smoothly to a hover over the landing point |
| 6 | Do NOT let the descent rate exceed 500 fpm below 40 KIAS — VRS risk |

---

### 9.5 Shallow Approach

Used when obstacles are minimal and a shallow angle is preferred (e.g., power-limited conditions, long clear approach path).

| Parameter | Value |
|---|---|
| **Approach angle** | ~3–5° (shallow) |
| **Entry airspeed** | 70–80 KIAS |
| **Power** | Slightly reduced from cruise — gradual descent |
| **Advantage** | Lower power required throughout; more gradual deceleration |
| **Disadvantage** | Requires a long, clear approach path; longer time at low altitude |
| **Termination** | Hover or run-on landing |

#### Procedure

| Step | Action |
|---|---|
| 1 | On final, maintain a shallow descent angle with moderate power |
| 2 | Decelerate gradually — the shallow angle provides more distance to reduce speed |
| 3 | Continue a long, gradual deceleration to the landing point |
| 4 | Transition to a hover at the landing point, or continue to a run-on landing if power-limited |

---

### 9.6 Go-Around

A go-around can be initiated from any point in the approach when the approach becomes unstabilized, the landing area is obstructed, or conditions become unsafe.

#### Decision Criteria for Go-Around

| Condition | Action |
|---|---|
| **Approach unstabilized** | Speed too high, too low, too fast, off-centerline — go around |
| **Landing area obstructed** | Vehicle, aircraft, or personnel on the landing zone — go around |
| **Wind shift** | Significant tailwind or crosswind exceeds comfort — go around |
| **Instrument warning** | Engine or transmission caution during approach — go around and assess |
| **"Doesn't feel right"** | Trust your instincts — go around |

#### Procedure

| Step | Action |
|---|---|
| 1 | **Collective — INCREASE** to arrest descent and begin climbing |
| 2 | **Cyclic — FORWARD** to accelerate and transition away from the landing area |
| 3 | **Announce:** "[Tower], [Callsign], going around" |
| 4 | **Climb to pattern altitude** at Vy (55–60 KIAS) |
| 5 | **Re-enter the pattern** as directed by ATC or by own judgment |
| 6 | **Brief what went wrong** and correct on the next approach |

**Golden rule:** A go-around is always the safe choice. There is never a penalty for going around. There is always a penalty for pressing a bad approach.

---

### 9.7 Crosswind Approach and Landing

Crosswinds require the pilot to compensate for lateral drift throughout the approach and in the hover/landing.

#### Techniques

| Technique | Description | Use |
|---|---|---|
| **Crab method** | Point the nose into the wind (heading offset from course) during the approach, then align with the landing zone just before hover | Most common during the approach phase |
| **Sideslip method** | Maintain runway alignment with cyclic while using opposite pedal to keep heading aligned | More common at hover and during the landing |

#### Procedure

| Step | Action |
|---|---|
| 1 | On approach, crab into the wind to maintain ground track toward the landing zone |
| 2 | As speed decreases on short final, transition to a sideslip — use cyclic to counteract drift while maintaining heading with pedals |
| 3 | In the hover, maintain position with cyclic (into the wind) and heading with pedals |
| 4 | Land: slowly lower collective — be prepared for the aircraft to weathervane (yaw into the wind) as it settles |
| 5 | Once on the ground, lower collective fully and neutralize controls |

**Crosswind limitations:** The OH-58D can generally handle crosswinds up to ~15–20 knots. Beyond this, consider using a more into-wind landing direction if available.

---

### 9.8 Slope Landing

Landing on a slope requires a modified technique to prevent dynamic rollover.

#### Procedure — Landing Upslope

| Step | Action |
|---|---|
| 1 | Approach into the wind (if possible) toward the slope |
| 2 | Establish a hover over the intended landing point |
| 3 | Slowly lower collective to begin descending onto the slope |
| 4 | **Uphill skid contacts first** — the aircraft begins to tilt toward the slope |
| 5 | Apply cyclic toward the downhill side to keep the rotor disc level |
| 6 | Continue lowering collective as the downhill skid settles |
| 7 | Once both skids are on the ground, lower collective fully and hold cyclic to keep the aircraft from sliding |

**Critical caution:** If the aircraft begins to roll downhill and cyclic cannot arrest it, **immediately increase collective and fly away.** Do not fight a dynamic rollover on a slope — if the roll exceeds ~5–8°, it is unrecoverable.

**Maximum slope for OH-58D:** Approximately 6–8° lateral slope (refer to -10 manual for exact limit). Beyond this, the landing is considered unsafe.

---

### 9.9 Confined Area Landing

A confined area is any landing zone surrounded by obstacles that restrict approach and departure paths.

#### Procedure

| Step | Action |
|---|---|
| 1 | **Reconnaissance:** Overfly the area at altitude to assess size, obstacles, wind, surface condition, and approach/departure paths |
| 2 | **Plan the approach:** Select the approach path with the best obstacle clearance, into the wind if possible |
| 3 | **Steep approach:** Use a steep approach angle (12–15°) to clear obstacles on the approach path |
| 4 | **Touchdown:** Terminate in a hover over the landing point, verify clear of obstacles, then land |
| 5 | **Departure plan:** Before shutting down, note the departure path (may be different from the approach path) |

**Key considerations:**
- Recirculation: Rotor downwash in a confined area may recirculate, reducing lift. Expect higher power requirements.
- Obstacles: Maintain awareness of rotor clearance from trees, walls, or structures. OH-58D rotor diameter is ~35 ft — need 17+ ft clearance on each side.
- Wind turbulence: Obstacles can create turbulence and unpredictable wind patterns. Be prepared for unexpected gusts.

---

### 9.10 Pinnacle Landing

A pinnacle is an elevated point (hilltop, ridgeline, rooftop) with limited landing area and exposure to wind from multiple directions.

#### Procedure

| Step | Action |
|---|---|
| 1 | **Reconnaissance:** Fly around the pinnacle to assess wind, landing surface, obstacles, and escape routes |
| 2 | **Wind assessment:** Determine wind direction. Approach into the wind. On a pinnacle, wind may be unpredictable due to terrain effects. |
| 3 | **Approach:** Fly a normal or steep approach to the pinnacle, maintaining escape routes (ability to go around) |
| 4 | **High reconnaissance:** At hover height over the pinnacle, assess the landing surface and surrounding obstacles |
| 5 | **Land** — slowly lower collective to settle onto the pinnacle |
| 6 | **Caution:** Be prepared for rapid wind changes and updrafts/downdrafts near the pinnacle edge |

**Specific risks:**
- **Downdrafts on the lee side:** Wind flowing over a pinnacle creates downdrafts on the downwind side. Do not approach from the downwind side.
- **Turbulence:** The pinnacle disrupts airflow, creating unpredictable gusts at the landing zone.
- **Limited landing area:** Precision hover and landing skills are essential. Overshoot = fly off the pinnacle.
- **Escape route:** Always maintain an escape route (ability to fly away) until committed to the landing.

---

### 9.11 Landing — Final Touchdown

Regardless of the approach type, the final landing follows the same sequence:

| Step | Action |
|---|---|
| 1 | **Stable hover** at 3–5 ft over the landing point |
| 2 | **Verify position** — clear of obstacles, over the intended point |
| 3 | **Slowly lower collective** — descend at ~1–2 ft/sec |
| 4 | **Maintain heading with pedals** — the aircraft may yaw as collective changes |
| 5 | **Maintain position with cyclic** — prevent drift as the aircraft settles |
| 6 | **Ground contact** — feel the skids touch, then continue lowering collective to full down |
| 7 | **On the ground** — collective full down, cyclic centered, pedals neutral |
| 8 | **Confirm on the ground** — stable, no sliding, no tip-over tendency |

---

### 9.12 Cockpit Switch Reference — Module 9

| Control | Function | DCS Action |
|---|---|---|
| **Collective** | Power management throughout the approach; final descent to landing | Joystick axis |
| **Cyclic** | Attitude/speed management; position hold in hover | Joystick X/Y |
| **Pedals** | Heading management throughout approach and hover | Rudder pedals or keys |
| **Radar altimeter** | AGL height reference during approach | Visual reference |
| **Airspeed indicator** | Critical for approach speed management | Visual reference |
| **VSI** | Rate of descent monitoring | Visual reference |
| **Torque gauge** | Power monitoring — especially on steep approach and hover | Visual reference |
| **Landing light** | Illuminate landing area (night/dusk) | Mouse click — ON/OFF |

---

### 9.13 Instructor Notes — Module 9

**Common student errors:**

1. **Arriving at the landing point too fast:** Students don't decelerate enough during the approach and overshoot the intended landing point. Drill: "Start decelerating abeam the numbers on downwind. If you're still at 60 KIAS on short final, go around."
2. **Flaring too aggressively on final:** Students pull back hard on the cyclic on short final, causing the aircraft to balloon (gain altitude) and then sink rapidly. Drill: "Smooth, gradual deceleration — not an emergency stop."
3. **Not going around when needed:** Students press a bad approach because they don't want to "waste" the pattern work. Drill: "A go-around is the correct maneuver when the approach is unstable. It's never wrong."
4. **Losing altitude awareness on final:** Students focus on airspeed and position and let the aircraft descend below glide path. Use the radar altimeter as a cross-check. Drill: "If you're below 100 ft AGL and still above 50 KIAS, you're likely too low — go around."
5. **Crosswind landing — not compensating for drift:** Students let the crosswind blow them off the landing zone during the final deceleration to hover. Drill: "Into the wind with cyclic, heading with pedals. Don't let it push you."
6. **Slope landing — dynamic rollover:** Students don't apply enough downhill cyclic on a slope landing and the aircraft begins to roll. If this happens, immediate collective increase to fly away. Prevention: "Before you lower the collective on a slope, position the cyclic to the downhill side."
7. **Confined area — no reconnaissance:** Students fly directly into a confined area without overflying it first. This is a setup for disaster — obstacles, poor surface, no departure path. Drill: "Always overfly first. If you can't see the entire landing zone and the departure path, don't land."
8. **Pinnacle — approaching from the downwind side:** Students approach a pinnacle from the wrong direction and encounter severe downdrafts. Drill: "Wind goes OVER the pinnacle. You approach INTO the wind, from the UPWIND side."
9. **Hard landing from too high:** Students misjudge hover height and lower collective from 10+ ft instead of 3–5 ft. The landing is hard and risks skid damage or dynamic rollover. Drill: "Use the radar altimeter or hover at a height where you can see the ground clearly. 3–5 feet is 'standing on a chair' height."


---

## Module 10: Shutdown & Post-Flight

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Perform a complete engine shutdown sequence from a normal post-landing condition.
2. Cool the engine properly before shutdown to prevent thermal damage.
3. Secure all cockpit systems in the correct order.
4. Apply the rotor brake safely and understand rotor brake limitations.
5. Achieve a full cold-and-dark cockpit state.
6. Perform a post-flight inspection (conceptual / DCS external view).
7. Understand the correct sequencing of shutdown steps to prevent damage.

---

### 10.1 Post-Landing — Before Shutdown

After landing and confirming the aircraft is stable on the ground:

| Step | Action | Notes |
|---|---|---|
| 1 | **Confirm on the ground** — collective full down, stable on skids | No sliding, no rocking |
| 2 | **Parking position** — confirm you are in an authorized parking area | Clear of taxiways, other aircraft, and obstacles |
| 3 | **Radio call** | "[Ground], [Callsign], [location], shutting down" |
| 4 | **Transponder** — STBY | No longer needed; set to standby |
| 5 | **Landing/search light** — OFF | |
| 6 | **Radar altimeter** — OFF (or leave for shutdown sequence) | |

---

### 10.2 Engine Cooldown

Before shutting down the engine, the pilot must allow the turbine to cool to prevent thermal shock to the hot section components.

| Step | Action | Notes |
|---|---|---|
| 1 | **Maintain Nr at 100% (ground idle)** | Do not roll the throttle to idle prematurely |
| 2 | **Allow engine to idle for 2–3 minutes minimum** | TOT should decrease to a stabilized idle temperature |
| 3 | **Monitor TOT** — should be well below limits and stable | If TOT is still elevated (e.g., from a high-power approach), extend the cooldown |
| 4 | **Purpose:** Gradual cooling prevents thermal stress on turbine blades and hot section components | Shutting down a hot engine abruptly can cause warping and shorten engine life |

> *⚠ Realism Divergence: DCS does not model long-term engine wear from improper cooldown. However, the student should practice proper cooldown procedure for procedural discipline and habit formation. In DCS, a 1–2 minute idle period before shutdown is sufficient to demonstrate the procedure.*

---

### 10.3 Shutdown Sequence — Step by Step

After the engine cooldown period:

| Step | Action | Expected Result |
|---|---|---|
| 1 | **Avionics / MFD** — OFF | MFD screen goes dark. Navigation and display systems powered down. |
| 2 | **Radios** — OFF (ARC-164 and ARC-201) | Radio control heads powered down. |
| 3 | **Position lights** — OFF | External navigation lights off. |
| 4 | **Anti-collision light** — OFF | Strobe/beacon off. (Turn off AFTER rotors stop if following strict procedure, or at pilot discretion during shutdown.) |
| 5 | **Throttle** — IDLE (roll to idle detent) | Engine power reduces. Nr begins to decrease. |
| 6 | **Throttle** — OFF (full cutoff) | Fuel flow ceases. Engine spools down. Nr decreases. |
| 7 | **Monitor Nr decay** | Nr decreases as the rotor system decelerates. Do not apply rotor brake until Nr is below a safe threshold (see 10.4). |
| 8 | **Fuel shutoff** — CLOSED | Ensures no fuel reaches the engine. Safety measure. |
| 9 | **Generator** — OFF | Generator disconnected from electrical bus. Aircraft on battery only. |
| 10 | **Inverter** — OFF (if separate switch) | AC power removed. |
| 11 | **Rotor brake** — APPLY when Nr is below ~40% | See 10.4 for details. Rotor decelerates to a stop. |
| 12 | **Wait for rotors to stop completely** | Rotors coast to a stop with the rotor brake applied. |
| 13 | **Battery** — OFF | All electrical power removed. Cockpit goes dark. |
| 14 | **Aircraft is now cold and dark** | Shutdown complete. |

---

### 10.4 Rotor Brake

The rotor brake is used to decelerate and stop the rotor system after the engine is shut down.

| Parameter | Detail |
|---|---|
| **Purpose** | Stops the rotor from windmilling after engine shutdown |
| **When to apply** | Only after Nr has decayed below ~40% (consult -10 manual for exact figure) |
| **Never apply at high Nr** | Applying the rotor brake at high rotor RPM can overheat and damage the brake, or cause a sudden rotor deceleration that stresses the rotor system |
| **Release if necessary** | If the brake overheats (smell, smoke), release and allow the rotor to slow naturally |

#### Procedure

| Step | Action |
|---|---|
| 1 | After engine shutdown, monitor Nr on the tachometer |
| 2 | When Nr drops below ~40%, apply the rotor brake |
| 3 | Nr will decelerate to zero. The rotors stop. |
| 4 | After rotors stop, you may release the brake or leave it applied (aircraft-specific SOP) |

> *⚠ Realism Divergence: DCS rotor brake behavior may be simplified. In some modules, the rotor brake stops the rotor almost instantly regardless of Nr. The student should still practice correct procedure: wait for Nr to decay before applying the brake.*

---

### 10.5 Cold-and-Dark State Verification

After shutdown, verify the aircraft is fully secured:

| System | Status |
|---|---|
| **Battery** | OFF |
| **Generator** | OFF |
| **Engine** | Shut down, Nr = 0 |
| **Fuel shutoff** | CLOSED |
| **Throttle** | OFF / Cutoff |
| **All avionics** | OFF |
| **Radios** | OFF |
| **MFD** | OFF |
| **Lighting** | All OFF |
| **Transponder** | OFF |
| **Radar altimeter** | OFF |
| **Caution panel** | Dark (no power) |
| **Rotor brake** | Applied or released per SOP |
| **Collective** | Full down |
| **Cyclic** | Centered or secured |
| **Pedals** | Neutral |

---

### 10.6 Post-Flight Inspection (Conceptual)

In real-world operations, the pilot performs a post-flight walkaround after shutdown. In DCS, this is simulated by external view inspection:

| Area | Check |
|---|---|
| **Rotor blades** | No visible damage (DCS: visual check from external view) |
| **Tail rotor** | Intact, no damage |
| **Engine exhaust** | No visible fire or damage |
| **Skids** | No visible damage from hard landing or slope operations |
| **Airframe** | No combat damage, bird strikes, or other visible issues |
| **Fuel** | Note remaining fuel for next mission or maintenance |

---

### 10.7 Cockpit Switch Reference — Module 10

| Switch/Control | Location | Function | DCS Action |
|---|---|---|---|
| **MFD power** | MFD bezel / avionics panel | Power off the MFD | Mouse click |
| **ARC-164 mode** | UHF control head | OFF | Mouse click |
| **ARC-201 mode** | FM control head | OFF | Mouse click |
| **Position lights** | Lighting panel | OFF | Mouse click |
| **Anti-collision light** | Lighting panel | OFF | Mouse click |
| **Throttle** | Collective — twist grip | IDLE → OFF (cutoff) | Keyboard or axis |
| **Fuel shutoff** | Engine / overhead panel | CLOSED | Mouse click |
| **Generator** | Electrical panel | OFF | Mouse click |
| **Rotor brake** | Overhead console | APPLY / RELEASE | Mouse click |
| **Battery** | Electrical panel | OFF | Mouse click |
| **Transponder** | Transponder panel | OFF | Mouse click |
| **Radar altimeter** | Instrument panel | OFF | Mouse click |

---

### 10.8 Instructor Notes — Module 10

**Common student errors:**

1. **Skipping the engine cooldown:** Students shut down immediately after landing (rolling the throttle to off while TOT is still high). Drill: "Idle for 2 minutes after landing before shutdown. Let the turbine cool."
2. **Wrong shutdown order:** Students turn off the battery before shutting down the engine, or turn off the generator before the engine is shut down. Drill: "Engine first, then electrical. Think of it as the reverse of startup."
3. **Applying rotor brake at high Nr:** Students apply the rotor brake immediately after engine shutdown while Nr is still at 80%+. This damages the brake. Drill: "Wait for Nr below 40% before touching the rotor brake."
4. **Forgetting to close fuel shutoff:** Students shut down the engine but leave the fuel shutoff open. This is a safety hazard (fuel leaks). Drill: "Fuel shutoff CLOSED is part of every shutdown."
5. **Not making the shutdown radio call:** Students shut down without informing ATC. Drill: "You checked in with ground, you check out with ground."
6. **Leaving lights on after battery off:** Students wonder why the anti-collision light is still on after they turned the battery off (it's not — in DCS, external models may still show lights). Teach that the shutdown sequence turns off lights before battery for procedural completeness, even if DCS doesn't always reflect it.
7. **Not verifying cold-and-dark:** Students rush through shutdown and miss switches. Teach: "After shutdown, do a full panel scan — left to right, bottom to top. Every switch should be in the OFF position. If something is still illuminated, you missed a step."


---

## Appendix A: DCS Key Binds Reference

> *All key binds listed are DCS defaults for the OH-58D Kiowa Warrior module. Key binds may vary by DCS version, user configuration, or mod version. Always verify in the DCS Controls settings (Options → Controls → OH-58D).*

### A.1 Flight Controls

| Function | Default Key/Axis | Notes |
|---|---|---|
| **Cyclic pitch (fore/aft)** | Joystick Y-axis | Forward = nose down, Back = nose up |
| **Cyclic roll (left/right)** | Joystick X-axis | Left = roll left, Right = roll right |
| **Collective (up/down)** | Throttle axis or `PgUp`/`PgDn` | Up = more pitch/power, Down = less |
| **Pedals (anti-torque)** | Rudder axis or `Z`/`X` | `Z` = left pedal, `X` = right pedal |
| **Throttle (twist grip)** | Separate axis or `PgUp`/`PgDn` with modifier | Idle / Fly / Off detents |
| **Force trim release** | Joystick button (configurable) | Hold to move cyclic, release to set new trim |
| **Trim reset** | `LCtrl + T` | Resets trim to neutral (verify in module) |

### A.2 Engine & Systems

| Function | Default Key | Notes |
|---|---|---|
| **Engine start** | `Home` | Initiates FADEC auto-start sequence |
| **Engine stop** | `End` | Cuts throttle / shuts down engine |
| **Throttle — Idle** | `RShift + End` or axis | Rolls throttle to idle detent |
| **Throttle — Cutoff (Off)** | `RShift + End` (hold/full back) | Full cutoff — engine shutdown |
| **Rotor brake — Toggle** | `LCtrl + R` | Engages/disengages rotor brake (verify in module) |
| **FADEC mode — Toggle** | Module-specific | AUTO ↔ MAN toggle (check in controls) |
| **Battery — Toggle** | `LShift + L` | Battery ON/OFF (verify in module) |
| **Generator — Toggle** | Module-specific | Generator ON/OFF |
| **Fuel shutoff — Toggle** | Module-specific | Open/Close fuel to engine |

### A.3 Weapons & Combat (if applicable)

| Function | Default Key | Notes |
|---|---|---|
| **Master Arm — Toggle** | Module-specific | Arms/disarms weapons |
| **Weapon release / Fire** | `Space` or joystick trigger | Fires selected weapon |
| **Weapon select — Cycle** | `D` | Cycles through available weapons |

> *Note: The OH-58D in DCS may be equipped with the Mast Mounted Sight (MMS), .50 cal gun pod, Hellfire missiles, and/or rocket pods depending on the module version and mission loadout. Weapon-specific key binds are mission-dependent.*

### A.4 Radios & Communications

| Function | Default Key | Notes |
|---|---|---|
| **Easy Communication menu** | `\` (backslash) | Opens the simplified radio menu (if Easy Comm is enabled) |
| **UHF radio transmit** | `RAlt + \` | Transmit on ARC-164 (UHF) |
| **VHF/FM radio transmit** | `RCtrl + \` | Transmit on ARC-201 (FM) |
| **ICS transmit** | Joystick button (1st detent) | Crew intercom — configurable |
| **Radio transmit (selected)** | Joystick button (2nd detent) | Transmits on the currently selected radio |

### A.5 Navigation & Instruments

| Function | Default Key | Notes |
|---|---|---|
| **MFD — Page cycle** | Module-specific OSB | Cycle through NAV/ENG/WPN/SYS/FLT pages |
| **MFD — OSB buttons** | Mouse click on bezel | Context-dependent — select options on MFD |
| **Altimeter — Set QNH** | `LShift + RShift + PgUp/PgDn` or mouse scroll | Adjusts Kollsman window |
| **Radar altimeter — ON/OFF** | Module-specific | Toggle radar altimeter power |
| **TACAN channel** | Module-specific | Adjust TACAN channel (mouse scroll in cockpit) |
| **Transponder — Mode** | Module-specific | Cycle transponder modes |

### A.6 Lighting

| Function | Default Key | Notes |
|---|---|---|
| **Position lights — Cycle** | `RCtrl + L` | OFF / DIM / BRT |
| **Anti-collision light** | `LShift + RCtrl + L` | ON/OFF (verify in module) |
| **Landing/search light** | `LShift + L` | ON/OFF (verify in module) |
| **Instrument panel lights** | `LCtrl + L` | Brightness adjustment (or mouse in cockpit) |
| **Cockpit flood light** | Module-specific | Interior lighting for night operations |
| **NVG-compatible mode** | Module-specific | Green-filtered lighting for NVG operations |

### A.7 Views & Camera

| Function | Default Key | Notes |
|---|---|---|
| **Cockpit view** | `F1` | Internal cockpit view |
| **External view** | `F2` | Chase camera |
| **Fly-by view** | `F3` | External tracking view |
| **Padlock — Nearest enemy** | `F6` or `;` | Locks view to nearest threat |
| **Look around** | Mouse + `RAlt` or TrackIR/VR | Free look in cockpit |
| **Snap view — Front** | `Numpad 5` | Centered forward view |
| **Snap view — Left** | `Numpad 4` | Quick look left |
| **Snap view — Right** | `Numpad 6` | Quick look right |
| **Snap view — Up** | `Numpad 8` | Quick look up (for overhead panel) |
| **Snap view — Down** | `Numpad 2` | Quick look down (for center console) |
| **Zoom in** | `Numpad *` | Cockpit zoom in |
| **Zoom out** | `Numpad /` | Cockpit zoom out |

### A.8 General / Miscellaneous

| Function | Default Key | Notes |
|---|---|---|
| **Pause** | `Pause/Break` | Pause the simulation |
| **Time acceleration** | `LCtrl + Z` | Speed up time (mission editor / single player) |
| **Time deceleration** | `LShift + Z` | Slow down time |
| **Normal time** | `Z` | Reset to 1x time |
| **Active pause** | `LShift + Pause` | Pause but allow cockpit interaction |
| **Mission briefing** | `B` | Opens mission briefing in-flight |
| **Kneeboard** | `K` or `RShift + K` | Opens kneeboard (mission data, frequencies, etc.) |
| **Scoring / Labels** | `LShift + F10` | Map view (F10 map) for navigation reference |
| **Screenshot** | `PrtScn` | Captures screenshot |

### A.9 HOTAS Recommendations

For helicopter operations in DCS, the following HOTAS mappings are recommended:

| Function | Recommended Mapping | Priority |
|---|---|---|
| **Collective** | Dedicated throttle axis (linear, no detent preferred) | Critical |
| **Cyclic** | Joystick X/Y with moderate curves (15–25) | Critical |
| **Pedals** | Dedicated rudder pedals | Highly recommended |
| **Force trim release** | Joystick button (thumb or finger) | Critical |
| **Radio transmit** | Joystick or throttle button | Important |
| **Weapon release** | Joystick trigger (2nd stage if available) | Important |
| **Countermeasures** | Throttle button | Useful |
| **View control** | TrackIR or VR headset | Highly recommended |

**Axis curves:** Helicopter flight in DCS benefits from axis curves (typically 15–25 on cyclic, 0–10 on pedals, 0 on collective). This provides fine control near center without sacrificing full deflection at the extremes. Adjust to personal preference in DCS Options → Controls → Axis Tune.

---

*This appendix provides default key binds as a reference. The OH-58D module may have additional or different bindings. Always verify in DCS Options → Controls → OH-58D Kiowa Warrior. Key binds marked "Module-specific" require checking the module's actual control assignments, as they vary by developer and version.*

---

*Based on Eagle Dynamics DCS World, Polychop Simulations OH-58D Kiowa Warrior module documentation, TM 1-1520-248-10 (OH-58D Operator's Manual), and real-world US Army rotary-wing flight training doctrine (TC 3-04.4). For simulation use only.*

