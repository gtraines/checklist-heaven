# OH-58D Kiowa Warrior — Basic Qualification Training Research Dossier

> **Aircraft:** Bell OH-58D Kiowa Warrior | **Role:** Scout / Light Attack Helicopter
> **Course Level:** Basic Qualification (Level 100)
> **Primary Reference:** TM 1-1520-248-10 (Operator's Manual), TM 1-1520-248-CL (Checklists)
> **Supplementary References:** AR 95-1 (Flight Regulations), TC 3-04.4 (Fundamentals of Flight), TC 3-04.62 (Tactical Flight Procedures)
> **DCS Module:** Polychop Simulations OH-58D Kiowa Warrior — Full-fidelity, clickable cockpit module. Every switch, dial, circuit breaker, and instrument is interactive. The module uses an advanced flight model (AFM) providing realistic rotor dynamics, autorotation, and retreating blade stall behavior.

---

## Overview

### Purpose

This document is the technical research foundation for an OH-58D Kiowa Warrior Basic Qualification Training (BQT) course in DCS World. It compiles systems knowledge, aerodynamic data, cockpit procedures, and emergency procedures into a single reference that will be converted into structured training events.

### Scope

**Covered:** Cold-and-dark startup through safe aircraft recovery in day VMC conditions — including hover work, basic flight maneuvers, navigation, traffic pattern operations, emergency procedures (academic and practice autorotations), and shutdown.

**Not Covered:** Combat employment (weapons delivery, Hellfire engagement, close combat attack, RSTA mission tactics, team scout/attack procedures). The Mast-Mounted Sight (MMS) is introduced at a familiarization level only. Weapons panels are identified but not employed.

### Aircraft Background

The Bell OH-58D Kiowa Warrior is a single-engine, four-blade light observation and attack helicopter developed for the U.S. Army. Derived from the Bell 206 JetRanger, the OH-58D was extensively modified under the Army Helicopter Improvement Program (AHIP) with a Mast-Mounted Sight (MMS) housing TV, thermal imaging, and laser range finder/designator sensors. The "Warrior" upgrade added weapons pylons capable of carrying AGM-114 Hellfire missiles, 2.75-inch Hydra 70 rockets, AIM-92 Stinger air-to-air missiles, and the M296 .50 caliber machine gun. Powered by a single Rolls-Royce (Allison) 250-C30R/3 turboshaft engine (redesignated T703-AD-700A under military nomenclature) producing approximately 650 shaft horsepower, the OH-58D operates at a maximum gross weight of 5,500 lbs with a Vne of 110–120 KIAS depending on configuration.

The OH-58D served as the U.S. Army's primary armed reconnaissance helicopter from the late 1980s through its retirement in 2017, operating extensively in Operations Desert Storm, Iraqi Freedom, and Enduring Freedom. Its role has since been absorbed by the AH-64 Apache and unmanned systems.

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
| TM 1-1520-248-23P | Maintenance allocation, parts — for systems context |
| USAACE Training Circulars | Fort Rucker/Novosel training standards and maneuver descriptions |

### Source Priority Rule

Real-world documentation is the **primary truth** for systems knowledge, limitations, aerodynamic behavior, and procedural structure. Where the DCS Polychop module diverges from real-world procedures or behavior, **the DCS procedure is what the student will actually execute** and is documented as the primary instruction. All divergences are footnoted:

> *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

---

## Module 1: Aircraft Systems & Aerodynamics

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Describe the T703-AD-700A turboshaft engine's operating cycle, FADEC modes, and all engine limitations (continuous, transient, starting).
2. Explain the main rotor system (4-blade, soft-in-plane) and tail rotor system (2-blade), including Nr governing, autorotation RPM range, and blade stall conditions.
3. Identify the transmission system components (main gearbox, tail rotor gearbox, intermediate gearbox) and state torque, oil temperature, and oil pressure limits.
4. Describe the fuel system architecture, capacity, boost pump function, and low-fuel warnings.
5. Explain the single hydraulic system, what it powers, and the flight characteristics when hydraulics are lost.
6. Describe the electrical system (DC generator, battery, bus architecture) and state battery endurance with generator offline.
7. Explain FADEC auto vs. manual mode, recognize FADEC failure indications, and describe the handling qualities impact of FADEC-OFF operations.
8. Describe the mechanical flight control system including mixing linkages, force trim, and hydraulic boost.
9. Define and explain the following rotary-wing aerodynamic phenomena: translating tendency, translational lift (ETL), transverse flow effect, dissymmetry of lift, retreating blade stall, ground effect (IGE vs. OGE), settling with power, LTE, mast bumping, and dynamic rollover.

---

### 1.1 Powerplant — T703-AD-700A Turboshaft Engine

The OH-58D is powered by a single Rolls-Royce (Allison) 250-C30R/3 turboshaft engine, designated **T703-AD-700A** under military nomenclature. It is a free-turbine design: the gas producer section (N1/Ng) is mechanically independent of the power turbine (N2/Np), which drives the main transmission and rotor system through a reduction gearbox.

#### Engine Operating Parameters

| Parameter | Value | Notes |
|---|---|---|
| **Engine Type** | Rolls-Royce 250-C30R/3 (T703-AD-700A) | Free-turbine turboshaft; gas producer + power turbine |
| **Max Continuous Power** | ~650 SHP | Sea level, standard day; derated from 650+ SHP rating |
| **Takeoff Power (5-min)** | ~650 SHP | Higher torque limit permitted for 5 minutes |
| **Gas Producer (N1/Ng)** | Idle: ~62–64% / Max: 104% (do not exceed) | FADEC governs N1 in auto mode |
| **Power Turbine (N2/Np)** | 100% = 6,016 RPM output shaft | Drives main rotor via transmission reduction |
| **Turbine Outlet Temperature (TOT)** | Continuous: 737°C / Transient (10 sec): 810°C / Start (10 sec): 843°C | TOT is the primary engine health indicator |
| **Idle RPM (Ground)** | N1 ~62%, Nr ~62–65% | Throttle at IDLE detent; rotor turns but below governed flight range |
| **Flight Idle RPM** | N1 ~72%, Nr governing to 100% | Throttle at FLY detent; FADEC governs Nr |
| **Spool-Up Time** | ~4–6 seconds (flight idle to max power) | Free turbine spools faster than fixed-shaft designs; still requires anticipation on collective inputs |
| **Oil Pressure** | Normal: 90–130 PSI / Min: 60 PSI | Below 60 PSI = caution |
| **Oil Temperature** | Normal: 70–107°C / Max: 107°C | Above 107°C = land as soon as practicable |
| **Fuel Flow** | Cruise (~80 KIAS): ~250 lbs/hr / Hover (IGE): ~300 lbs/hr | Varies significantly with weight, altitude, temperature |

#### FADEC Operation

The FADEC (Full Authority Digital Engine Control) manages all engine parameters in **auto mode**, including:
- Nr governing to 100% (adjusts fuel flow to maintain rotor RPM regardless of collective input)
- TOT limiting (prevents exceedances during high-demand situations)
- N1 overspeed protection
- Engine start sequencing (automated light-off and acceleration schedule)

In **manual mode** (FADEC failure or deliberate selection), the pilot must:
- Manually control the throttle to maintain Nr within 98–100% (power on)
- Monitor and respect TOT limits without automatic protection
- Anticipate collective inputs with throttle adjustments (collective up = more throttle required)

| FADEC Mode | Pilot Action | Nr Management | TOT Protection |
|---|---|---|---|
| **Auto** | Collective only; FADEC adjusts engine | Automatic (100%) | Automatic limiting |
| **Manual** | Throttle + collective coordinated | Pilot responsibility | Pilot responsibility |

> *⚠ Realism Divergence: In the real OH-58D, FADEC failure modes include partial authority degradation, intermittent N1 hunting, and nuanced manual reversion scenarios documented in TM 1-1520-248-10 Chapter 9. DCS models a simplified FADEC failure — typically a clean switchover to manual mode with a caution light. The real aircraft may exhibit transient Nr oscillations during transfer that DCS does not replicate.*

#### Engine Start Cycle

1. Throttle at **IDLE** detent (cutoff position).
2. Press **START** button — starter motor cranks N1/Ng.
3. At approximately **15% N1**, fuel is introduced (light-off).
4. TOT rises — monitor for hot start (TOT exceeding 843°C during start).
5. N1 accelerates through **58–62%** to stabilize at ground idle (~62–64%).
6. If TOT exceeds start limits or N1 hangs below idle → **abort start** (throttle OFF, motor to cool, attempt restart).

**Abort Criteria:**
- **Hot start:** TOT exceeds 843°C during start cycle → throttle OFF immediately, motor to purge.
- **Hung start:** N1 fails to accelerate to idle within ~60 seconds → throttle OFF, motor.
- **No light-off:** No TOT rise by ~25% N1 → throttle OFF, check fuel boost, reattempt.

> *⚠ Realism Divergence: The real OH-58D requires precise throttle placement at the IDLE detent for the start sequence. DCS models this requirement but may have slightly different N1/TOT acceleration profiles. Real hot starts can cause turbine damage requiring maintenance; DCS models the temperature exceedance but does not track cumulative thermal damage.*

---

### 1.2 Rotor System

#### Main Rotor

| Parameter | Value | Notes |
|---|---|---|
| **Configuration** | 4-blade, soft-in-plane, bearingless composite hub | Upgraded from original 2-blade teetering OH-58A/C rotor |
| **Diameter** | 35 ft (10.67 m) | |
| **Nr (Power On)** | 98–100% continuous | FADEC governs to 100% in auto mode |
| **Nr (Power Off / Autorotation)** | 90–107% | 90% minimum for safe autorotation; above 107% = overspeed |
| **Nr Transient Low Limit** | 90% (momentary) | Below 90% = rotor stall risk, reduced autorotation capability |
| **Nr Transient High Limit** | 107% (momentary, power off) | Above 107% = structural risk to rotor head/mast |
| **Rotor Direction** | Counterclockwise (viewed from above) | Standard U.S. configuration; determines translating tendency and yaw response |

The 4-blade soft-in-plane rotor provides smoother ride characteristics and lower vibration than the original 2-blade teetering rotor of the OH-58A/C. The bearingless composite hub uses flexbeam elements for flapping and lead-lag articulation, reducing maintenance burden.

**Blade Stall:** At high gross weight, high altitude, high G, or high airspeed, the retreating blade may exceed its critical angle of attack. The 4-blade system is more resistant to blade stall onset than a 2-blade system, but pilots must respect Vne and G limits. Symptoms include vibration, uncommanded pitch-up or roll, and increased control forces.

#### Tail Rotor

| Parameter | Value | Notes |
|---|---|---|
| **Configuration** | 2-blade, semi-rigid | Mounted on left side of vertical fin |
| **Diameter** | 5.42 ft (1.65 m) | |
| **Function** | Anti-torque, yaw control | Pedal input directly changes tail rotor blade pitch |
| **Drive** | Driveshaft from main transmission through tail rotor gearbox | Loss of drive = loss of anti-torque |

> *⚠ Realism Divergence: The real OH-58D tail rotor can experience bearing wear and gearbox failures producing vibration and noise before catastrophic failure. DCS models tail rotor failure as a binary event (functional or failed) without progressive degradation.*

---

### 1.3 Transmission System

| Component | Function | Key Limits |
|---|---|---|
| **Main Transmission** | Reduces engine output RPM to main rotor RPM | Torque: 100% continuous / 110% transient (10 sec) |
| **Tail Rotor Gearbox** | Drives tail rotor from main transmission output | Oil temp/pressure monitored; chip detector equipped |
| **Intermediate Gearbox** | 90° turn in driveshaft routing to tail boom | Oil temp/pressure monitored; chip detector equipped |
| **Freewheeling Unit (Sprag Clutch)** | Allows rotor to spin freely when engine output drops below rotor RPM | Enables autorotation; must disengage cleanly or autorotation entry is degraded |

#### Transmission Limits

| Parameter | Normal | Caution | Warning |
|---|---|---|---|
| **Torque (Q)** | ≤ 100% | 100–110% (10 sec max) | > 110% |
| **Trans Oil Pressure** | 30–60 PSI | < 30 PSI | XMSN OIL PRESS caution |
| **Trans Oil Temperature** | < 110°C | 110–120°C | > 120°C |
| **Chip Detector** | Clear | — | CHIP light = metallic particles detected; land ASAP |

> *⚠ Realism Divergence: In the real OH-58D, chip detectors can distinguish between fuzz (minor) and hard metal particles (major) through maintenance crew burn-check procedures. In DCS, a chip light is a binary caution requiring the student to treat it as a "land as soon as possible" event.*

---

### 1.4 Fuel System

| Parameter | Value | Notes |
|---|---|---|
| **Internal Fuel Capacity** | ~112 US gallons (~750 lbs JP-8) | Single crashworthy fuel cell |
| **Fuel Type** | JP-8 (primary), JP-5, Jet-A acceptable | |
| **Fuel Boost Pump** | Electric, pilot-controlled | Must be ON before start and during flight; gravity feed is emergency backup only |
| **Fuel Quantity Indicator** | Instrument panel — calibrated in pounds | |
| **Low Fuel Warning** | Caution light at approximately 83 lbs (~12 gal) remaining | Approximately 20 minutes of flight at cruise |
| **Fuel Consumption (Hover IGE)** | ~300 lbs/hr | At sea level, mid gross weight |
| **Fuel Consumption (Cruise ~80 KIAS)** | ~250 lbs/hr | At sea level, mid gross weight |
| **Endurance (No Reserve)** | ~2.5–3.0 hours cruise | Varies significantly with weight, altitude, mission profile |

The fuel system is a single-cell, crashworthy, self-sealing design. The electric boost pump provides positive fuel pressure to the engine; loss of the boost pump triggers a caution light and requires the pilot to monitor for engine fuel starvation. Gravity feed is available as a backup but is not reliable in all flight attitudes.

> *⚠ Realism Divergence: The real OH-58D has a more complex fuel system with a sump, filter/separator, and specific gravity feed limitations by flight attitude. DCS simplifies fuel feed — the boost pump caution triggers but gravity feed generally continues to supply fuel in normal flight attitudes without the attitude restrictions of the real aircraft.*

---

### 1.5 Hydraulic System

| Parameter | Value | Notes |
|---|---|---|
| **System Type** | Single hydraulic system | No redundancy — single-point failure |
| **Pressure** | ~1,000 PSI (system dependent) | |
| **Powers** | Flight control servo actuators (cyclic, collective, tail rotor) | All flight controls are hydraulically boosted |
| **Reservoir** | Single, with sight gauge | |
| **Hydraulic-Off Flight** | Controllable but extremely high control forces | Run-on landing recommended; avoid hover |

The OH-58D uses a **single hydraulic system** with no backup. This means any hydraulic failure (pump, line, or fluid loss) results in loss of all hydraulic boost to the flight controls. The aircraft is controllable without hydraulics but requires significant pilot strength — control forces increase dramatically, especially in the cyclic. A run-on landing at 40–60 KIAS is recommended to reduce the control forces required for a hover landing.

> *⚠ Realism Divergence: In the real OH-58D, hydraulic-off flight requires extreme physical effort — two-handed cyclic inputs and bracing against the collective. DCS models increased control forces but may not fully replicate the physical difficulty. Students should understand that real hydraulic failure is a much more demanding emergency than DCS depicts.*

---

### 1.6 Electrical System

| Component | Function | Notes |
|---|---|---|
| **DC Starter-Generator** | Primary electrical power source (28V DC) | Engine-driven; comes online after engine start, generator switch ON |
| **Battery** | 24V nickel-cadmium | Provides power for start and emergency bus; ~30 min endurance without generator |
| **Essential Bus** | Powers critical instruments, caution panel, radios | Remains powered on battery alone |
| **Non-Essential Bus** | Powers MFD, MMS, weapons systems, lighting | Shed in generator-off/battery-only operations |
| **Inverter** | Converts DC to AC for AC-powered instruments | Required for attitude indicator, some avionics |

**Generator Failure Sequence:**
1. GEN caution light illuminates.
2. Attempt generator reset (GEN RESET button).
3. If reset fails → shed non-essential bus (non-essential loads OFF).
4. Monitor battery voltage — approximately 30 minutes endurance on essential bus.
5. Land as soon as practicable.

> *⚠ Realism Divergence: The real OH-58D electrical system includes specific load-shedding priorities and bus-tie logic that may not be fully modeled in DCS. The DCS module provides generator failure and battery-only operations, but the nuanced bus transfer behavior may be simplified.*

---

### 1.7 FADEC — Full Authority Digital Engine Control

The FADEC system deserves its own subsection due to its critical importance in single-engine helicopter operations.

| Feature | Auto Mode | Manual Mode |
|---|---|---|
| **Nr Governing** | Automatic — maintains 100% | Pilot must correlate throttle with collective |
| **TOT Limiting** | Automatic — prevents exceedance | Pilot must monitor and respect limits |
| **N1 Overspeed Protection** | Active | Inactive — pilot manages throttle |
| **Start Sequencing** | Automatic fuel scheduling | Manual throttle advancement |
| **Collective Compensation** | Automatic fuel flow adjustment | Pilot must lead/lag throttle with collective changes |

**Auto Mode (Normal Operations):**
The pilot uses the collective freely. The FADEC adjusts fuel flow to maintain Nr at 100%. The only engine instrument that requires routine monitoring is torque (to avoid exceeding limits) and TOT (to verify FADEC is maintaining limits).

**Manual Mode (Degraded Operations):**
The pilot must coordinate throttle with collective. Increasing collective without adding throttle will cause Nr to decay; decreasing collective without reducing throttle will cause Nr to overspeed. This requires continuous scan of Nr and TOT while simultaneously flying the aircraft.

**FADEC Failure Recognition:**
- **FADEC caution light** illuminates
- Nr may fluctuate or diverge from 100%
- TOT may spike or oscillate
- In DCS, the aircraft may yaw as Nr changes (torque effect on anti-torque requirements)

---

### 1.8 Flight Control System

The OH-58D uses a conventional mechanical flight control system with hydraulic boost.

| Control | Function | Mechanism |
|---|---|---|
| **Cyclic** | Controls main rotor tip-path plane tilt (pitch and roll) | Mechanical linkage → swashplate → hydraulic servo |
| **Collective** | Controls main rotor blade pitch angle (power/lift) | Mechanical linkage → swashplate → hydraulic servo |
| **Anti-Torque Pedals** | Controls tail rotor blade pitch (yaw) | Mechanical linkage → tail rotor pitch change mechanism |
| **Throttle** | Mounted on collective grip; twist-grip design | Controls engine power in manual FADEC mode; in auto, set to FLY and leave |

#### Mechanical Mixing

The OH-58D incorporates mechanical mixing linkages:
- **Collective-to-yaw mixing:** Increasing collective automatically increases tail rotor pitch to compensate for the increased main rotor torque reaction. This reduces but does not eliminate the yaw input required from the pilot.
- **Collective-to-cyclic mixing:** Compensates for the pitch/roll tendency that accompanies collective changes.

These mixing systems reduce pilot workload but do not fully eliminate the need for coordinated inputs.

#### Force Trim

The force trim system uses a magnetic brake to hold the cyclic and pedals at a set position. The pilot presses the **force trim release** button (typically on the cyclic grip) to move the controls, then releases to set the new trim position. This replaces the traditional fixed-wing trim tab concept.

- **Force trim release:** Press-and-hold → move controls → release to set new reference
- **Trim must be reset** any time airspeed, power, or CG changes significantly
- Failure to re-trim results in the pilot fighting constant control forces

> *⚠ Realism Divergence: The real OH-58D has distinct force trim feel characteristics (breakout force, gradient) that vary by airspeed due to aerodynamic feedback. DCS models force trim functionally but the control force gradient may not perfectly replicate the real aircraft's feel, particularly at low airspeed where real control forces are very light.*

---

### 1.9 Survivability Features

| Feature | Description | DCS Modeled? |
|---|---|---|
| **Crashworthy Fuel Cell** | Self-sealing, crash-resistant fuel bladder; resists puncture and reduces post-crash fire risk | Partially — crash damage modeled but self-sealing behavior simplified |
| **Energy-Absorbing Crew Seats** | Stroking seats designed to attenuate vertical crash loads | Not directly — DCS models crew injury through damage model |
| **Armored Crew Seats** | Ballistic protection against small-arms fire | Yes — damage model includes ballistic protection |
| **IR Suppressor** | Engine exhaust mixing with ambient air to reduce IR signature | Visual model present; functional IR reduction modeled for AI targeting |
| **Wire Strike Protection System (WSPS)** | Deflector blades and cutters above and below cockpit | Not modeled — no wire strike hazard in DCS |
| **Redundant Flight Controls** | Dual push-pull tubes in critical linkage areas | Not individually modeled — battle damage may sever controls as a single event |

---

### 1.10 Rotary-Wing Aerodynamics

This section covers the aerodynamic phenomena critical to safe helicopter operations. Unlike fixed-wing aerodynamics (where the wing is fixed and airspeed generates lift), the rotary wing is a dynamic system where each blade experiences continuously changing relative wind, angle of attack, and velocity throughout every revolution.

#### Translating Tendency (Hover Drift)

In a hover, the tail rotor produces lateral thrust (to the right on U.S. helicopters with counterclockwise main rotor) to counteract main rotor torque. This lateral thrust causes the entire aircraft to drift **left**. The pilot compensates with a slight **right cyclic** input in hover.

- **Effect in DCS:** Present. In a no-wind hover, the aircraft will drift left if the pilot does not apply right cyclic.
- **Student Error:** Failure to apply right cyclic compensation in hover, leading to slow left drift.

#### Translational Lift (ETL)

As forward airspeed increases through approximately **16–24 knots**, the rotor disc transitions from operating in its own disturbed downwash (hover) to operating in cleaner, undisturbed air. This produces a noticeable increase in lift efficiency called **Effective Translational Lift (ETL)**.

| Indication | Description |
|---|---|
| **Airspeed** | 16–24 knots (develops progressively) |
| **Aircraft Response** | Nose pitches up, aircraft tends to climb, vibration decreases |
| **Required Correction** | Forward cyclic to maintain attitude, slight collective reduction, left pedal as power requirement decreases |

- **Effect in DCS:** Modeled. The student will feel the aircraft "break free" of the hover power requirement and should anticipate the nose-up pitch.

#### Transverse Flow Effect

During transition through ETL, air passing through the aft portion of the rotor disc has a higher induced flow angle than air entering the forward portion. This causes the aft blades to operate at a lower angle of attack than the forward blades, creating a rolling moment (typically a **right roll** tendency and vibration at 10–20 knots).

- **Effect in DCS:** Modeled as increased vibration and roll tendency during transition.
- **Student Error:** Failure to anticipate the roll input required during acceleration through 10–20 knots.

#### Dissymmetry of Lift and Blade Flapping

In forward flight, the advancing blade (moving into the relative wind) experiences higher airspeed and produces more lift than the retreating blade (moving away from the relative wind). To equalize lift across the disc, the blades **flap** — the advancing blade flaps up (reducing angle of attack) and the retreating blade flaps down (increasing angle of attack).

This flapping is inherent in the rotor design and occurs automatically. However, at high forward airspeeds, the retreating blade may reach its stall angle of attack, causing **retreating blade stall**.

#### Retreating Blade Stall

| Factor | Effect |
|---|---|
| **High Forward Airspeed** | Increases velocity differential between advancing and retreating blades |
| **High Gross Weight** | Requires higher blade angles of attack to produce required lift |
| **High Altitude (DA)** | Thinner air requires higher blade angles |
| **High G Loading** | Increases required lift, increasing blade angles |
| **Turbulence** | Random angle of attack excursions |

**Symptoms:** Vibration (usually low-frequency), uncommanded pitch-up or roll, increasing control forces. In severe cases, loss of control.

**Recovery:** Reduce airspeed (aft cyclic), reduce collective (lower blade angles), reduce G (level the aircraft), descend to lower altitude if possible.

**OH-58D Vne** is set to protect against retreating blade stall onset:

| Configuration | Vne (KIAS) | Notes |
|---|---|---|
| **Doors On, Clean** | 120 KIAS | Standard configuration |
| **Doors Off** | 110 KIAS | Increased drag shifts retreating blade stall onset |
| **With External Stores** | 110–120 KIAS | Depends on specific stores and weight |

#### Ground Effect (IGE vs. OGE)

| Condition | Definition | Performance Impact |
|---|---|---|
| **In Ground Effect (IGE)** | Hover altitude ≤ ~½ rotor diameter (≤ ~17 ft skid height) | Reduced power required; ground surface reflects downwash, reducing induced drag |
| **Out of Ground Effect (OGE)** | Hover altitude > ~½ rotor diameter | Full induced power required; approximately 15–20% more power than IGE hover |

**Significance:** A helicopter may be able to hover IGE but **not** OGE at the same weight/altitude/temperature. The pilot must verify OGE hover capability before departing a confined area where the hover-out will be above ground effect height.

**OH-58D Power Check:** Before takeoff, the student should verify that torque required to hover at 3–5 ft skid height is below the available torque limit, with adequate margin for OGE operations and maneuvering.

#### Settling with Power (Vortex Ring State)

| Condition | Threshold |
|---|---|
| **Airspeed** | Below ETL (< ~16 knots) |
| **Rate of Descent** | > 300 FPM |
| **Power Applied** | Moderate to high (above 40–50% of available) |

When these three conditions combine, the rotor can enter its own downwash vortex. Applying more collective (more power) worsens the condition because the increased downwash feeds the vortex.

**Recognition:** High rate of descent that does not arrest with collective application; erratic control response; vibration.

**Recovery:**
1. Cyclic forward — **get airspeed** (break out of the vortex laterally)
2. Reduce collective slightly (counterintuitive but reduces downwash feeding the vortex)
3. As airspeed increases through ETL, the vortex breaks and normal powered flight resumes

> *⚠ Realism Divergence: DCS models vortex ring state aerodynamics. However, the onset may be slightly more or less abrupt than the real aircraft depending on the flight model iteration. The recovery technique (cyclic forward, reduce collective, gain airspeed) is identical in DCS and is fully effective.*

#### Loss of Tail Rotor Effectiveness (LTE)

LTE is not a mechanical failure — it is an **aerodynamic condition** where the tail rotor cannot produce sufficient anti-torque thrust due to wind interaction with the main rotor downwash and fuselage wake.

**Critical Wind Azimuths (relative to aircraft nose):**

| Wind Direction | Azimuth | Mechanism |
|---|---|---|
| **Main Rotor Disc Vortex Interference** | 285°–315° (left rear quartering) | Main rotor tip vortices are pushed into the tail rotor disc, reducing its effectiveness |
| **Weathercock Instability** | 120°–240° (tail wind sector) | Fuselage weathercocks into the wind, which means the tail wants to swap with the nose |
| **Tail Rotor Vortex Ring State** | 210°–330° (left crosswind to tail) | Tail rotor operates in its own recirculating vortex |

**Recognition:** Uncommanded right yaw that increases despite left pedal application.

**Recovery (Boldface):**
1. **COLLECTIVE — REDUCE** (reduce main rotor torque, reduce anti-torque demand)
2. **CYCLIC — FORWARD** (gain airspeed to break the aerodynamic interference)
3. **PEDALS — FULL LEFT** (as required)
4. **AIRSPEED — INCREASE** (above ETL; translational lift and clean airflow restore tail rotor effectiveness)

> *⚠ Realism Divergence: DCS models LTE and the pilot will experience uncommanded yaw in the critical wind azimuths. However, the onset and severity may differ slightly from the real aircraft. The recovery technique is identical and fully effective in DCS.*

#### Mast Bumping

Mast bumping occurs when the rotor hub contacts the mast in a **semi-rigid or teetering rotor system** during **low-G or negative-G** flight conditions. The OH-58D's 4-blade soft-in-plane system is **more resistant** to mast bumping than a 2-blade teetering design, but it is **not immune**.

**Conditions that can cause mast bumping:**
- Low-G or negative-G maneuvers (pushovers, turbulence-induced unloading)
- Abrupt cyclic inputs at low rotor loading
- Excessive flapping angles

**Why it is catastrophic:** Contact between the rotor hub and mast can sever the mast, causing immediate loss of the rotor system. There is no recovery.

**Prevention:**
- Avoid abrupt pushovers or negative-G flight
- Maintain positive G at all times
- Avoid abrupt cyclic inputs, particularly at low airspeed
- G-limits: +2.5 G to −0.5 G at max gross weight

> *⚠ Realism Divergence: DCS may not model mast bumping with full fidelity. In the real aircraft, even momentary contact can cause catastrophic mast severance. Students should internalize the G limits and avoid negative-G flight regardless of whether DCS produces the full consequence.*

#### Pendular Action and Dynamic Rollover

**Pendular Action:** The helicopter fuselage is suspended below the rotor system like a pendulum. During slope operations, crosswind hover, or abrupt cyclic inputs, the fuselage can oscillate laterally or longitudinally beneath the rotor disc.

**Dynamic Rollover:** Occurs when one skid is fixed (caught on ground obstruction, slope edge, or tiedown) and the pilot applies collective. The helicopter pivots around the fixed skid. Beyond a **critical rollover angle** (~5–15° depending on rate), the roll becomes self-sustaining and the helicopter rolls over regardless of control input.

**Prevention:**
- Apply collective slowly during slope takeoffs
- Ensure both skids are clear before increasing collective
- If roll begins, **immediately reduce collective** (this is counterintuitive — the pilot wants to "fly out" but must first unload the pivot point)
- Maintain awareness of skid contact during crosswind hover and slope operations

**Slope Landing Limits:**

| Condition | Maximum Slope |
|---|---|
| **Side Slope / Nose-Up Slope** | 10° |
| **Nose-Down Slope** | 5° |

#### Instructor Notes — Module 1

| Common Student Error | Correction |
|---|---|
| Confusing Nr (rotor RPM) with N1 (gas producer RPM) | Emphasize: Nr is your **life** gauge. N1 is the engine speed. In auto FADEC, Nr should always be 100%. |
| Not understanding collective-yaw coupling | Demonstrate in hover: raise collective → aircraft yaws right (main rotor torque increases). Mixing compensates partially, but pedal correction is always needed. |
| Failing to anticipate ETL during acceleration | Brief the student that at 16–24 knots, the nose will pitch up and the aircraft will want to climb. Forward cyclic and collective reduction are required. |
| Over-relying on FADEC | Explain that FADEC failure converts the aircraft into a "manual-everything" machine. The student must understand the engine, not just trust the computer. |
| Dismissing LTE as rare | LTE is the #1 killer in light helicopters. Emphasis: never hover with wind from the left-rear (285°–315°), and always have an escape plan. |
| Ignoring mast bumping risk because "it's not modeled perfectly in DCS" | Brief the G limits and negative-G prohibition. Build correct habits regardless of sim fidelity. |

---

## Module 2: Cockpit Familiarization

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Identify all major cockpit panels by name and location (left console, right console, instrument panel, center pedestal, overhead console).
2. Locate and describe the function of every engine instrument (Torque, TOT, N1, Nr, fuel flow, oil pressure/temperature).
3. Power on and navigate the MFD through its default pages using OSB (Option Select Button) inputs.
4. Describe the MMS sensor suite (TV, FLIR, laser rangefinder/designator) and locate the MMS controller — familiarization only.
5. Identify the weapon panel switches (ARM/SAFE, weapon select) and state their function — identification only.
6. Locate and interpret every caution/advisory indicator on the caution panel.
7. Set and read the radar altimeter, including the low-altitude warning bug.
8. Identify all flight instruments and state their power source (DC, AC/inverter, pitot-static).
9. Locate and operate all cockpit and exterior lighting controls.
10. Identify the HOTAS functions on the collective grip and cyclic grip.

---

### 2.1 Cockpit Layout Overview

The OH-58D cockpit is a tandem-width (side-by-side) configuration seating pilot (right seat) and copilot/observer (left seat). The instrument panel is shared, with the MFD centrally mounted.

```
┌─────────────────────────────────────────────────────────────┐
│                     OVERHEAD CONSOLE                         │
│   Engine start panel  Generator  Fuel boost  Lighting       │
├──────────┬──────────────────────────────────┬───────────────┤
│  LEFT    │       INSTRUMENT PANEL            │   RIGHT      │
│ CONSOLE  │                                   │  CONSOLE     │
│          │  ┌─────┐  ┌─────────┐  ┌─────┐   │              │
│ MMS      │  │Eng  │  │   MFD   │  │Eng  │   │ Weapon      │
│ Control  │  │Instr│  │(Center) │  │Instr│   │ Panel       │
│          │  │(L)  │  │         │  │(R)  │   │              │
│ Circuit  │  └─────┘  └─────────┘  └─────┘   │ AHRS/GPS    │
│ Breakers │                                   │ Control     │
│          │  Attitude  Airspeed   Altimeter    │              │
│ Comms    │  Indicator  Indicator  (Baro)     │ Radio       │
│ Panel    │  VSI  Heading  Turn Coord  RadAlt │ Panels      │
├──────────┴──────────────────────────────────┴───────────────┤
│                     CENTER PEDESTAL                          │
│   Throttle quadrant   Collective friction   Pedal adjust    │
└─────────────────────────────────────────────────────────────┘
```

| Panel Area | Location | Primary Contents |
|---|---|---|
| **Overhead Console** | Above pilots' heads | Engine start switch, generator switch, fuel boost pump, battery, inverter, lighting master controls |
| **Instrument Panel — Left** | Left of MFD | Pilot engine instruments (Torque, TOT, N1, Nr), fuel quantity, oil pressure/temperature |
| **Instrument Panel — Center** | Center | MFD (Multi-Function Display), master caution, caution/advisory panel |
| **Instrument Panel — Right** | Right of MFD | Flight instruments (attitude indicator, airspeed, altimeter, VSI, heading indicator, turn coordinator) |
| **Left Console** | Pilot's left | MMS controller, circuit breaker panels, communications panel, collective quadrant |
| **Right Console** | Pilot's right | Weapon panel, AHRS/GPS controller, radio panels, transponder |
| **Center Pedestal** | Between seats, below instrument panel | Throttle quadrant, collective friction adjustment, pedal adjustment |
| **Radar Altimeter** | Lower instrument panel | Analog radar altitude indicator with bug setting |

---

### 2.2 MFD (Multi-Function Display)

The MFD is the primary digital display, centrally mounted on the instrument panel. It provides navigation, weapons, engine, and sensor (MMS) information on selectable pages.

| Feature | Description |
|---|---|
| **Display Type** | Color LCD, sunlight readable |
| **OSB (Option Select Buttons)** | Bezel-mounted buttons around the display edge (typically 20 OSBs) |
| **Power** | Non-essential bus (requires generator; lost on battery-only operations) |
| **Default Pages** | Navigation (NAV), Engine (ENG), Tactical (TAC), MMS video feed |

#### MFD Page Navigation

| Page | Access | Primary Use |
|---|---|---|
| **NAV** | OSB press (labeled NAV) | Moving map, waypoints, bearing/distance/ETA, own-ship position |
| **ENG** | OSB press (labeled ENG) | Digital engine parameters (mirrors analog gauges with trend data) |
| **TAC** | OSB press (labeled TAC) | Tactical display (weapons employment — familiarization only) |
| **MMS Video** | OSB press (labeled MMS/VIDEO) | Live video feed from the Mast-Mounted Sight (TV or FLIR) |

#### Cockpit Switch Reference — MFD

| Switch / Control | Location | Action | DCS Keybind |
|---|---|---|---|
| MFD Power | Overhead console — Avionics section | Toggle ON/OFF (mouse click) | — |
| MFD Brightness | MFD bezel — rotary knob | Rotate to adjust (mouse scroll) | — |
| OSB Buttons | MFD bezel — surrounding display | Left-click to select page/option | — |
| MFD Mode Select | MFD bezel — top row OSBs | Left-click to cycle NAV/ENG/TAC/MMS | — |

> *⚠ Realism Divergence: The real OH-58D MFD (typically the IDM/CDU combined display unit) has additional pages for data modem messaging, digital map overlays, and mission data loading that are not fully replicated in DCS. The DCS MFD provides NAV, ENG, and MMS video pages that are sufficient for BQT-level operations.*

---

### 2.3 MMS (Mast-Mounted Sight) — Familiarization

The MMS is the OH-58D's signature system — a sensor ball mounted above the main rotor hub on a mast extension, allowing the aircraft to observe targets from hull-defilade (only the MMS ball exposed above terrain/obstacles).

**This module provides familiarization only.** Tactical employment (target acquisition, laser designation for Hellfire, RSTA procedures) is covered in follow-on weapons employment courses.

| MMS Component | Function |
|---|---|
| **TV Camera** | Daytime visual observation; variable zoom |
| **FLIR (Thermal)** | Night/obscured conditions observation; requires ~3–5 min warmup |
| **Laser Rangefinder (LRF)** | Provides slant range to target; range data feeds navigation and weapons |
| **Laser Designator (LD)** | Designates targets for semi-active laser (SAL) guided munitions (Hellfire) |

#### MMS Controller

| Control | Location | Function |
|---|---|---|
| **MMS Slew** | Left console — hand controller (or cyclic hat switch in DCS) | Slew the MMS sensor ball in azimuth and elevation |
| **Zoom In/Out** | MMS controller or keyboard | Adjust sensor field of view |
| **Sensor Select (TV/FLIR)** | MFD OSB or MMS controller | Switch between TV and FLIR video |
| **Laser Arm/Fire** | Weapon panel and/or cyclic trigger | Arm and activate laser (familiarization only) |

#### DCS Keybind Reference — MMS

| Action | Default DCS Keybind | Notes |
|---|---|---|
| MMS Slew Up | `Numpad 8` | Continuous slew while held |
| MMS Slew Down | `Numpad 2` | Continuous slew while held |
| MMS Slew Left | `Numpad 4` | Continuous slew while held |
| MMS Slew Right | `Numpad 6` | Continuous slew while held |
| MMS Zoom In | `Numpad +` | Narrower FOV, higher magnification |
| MMS Zoom Out | `Numpad -` | Wider FOV, lower magnification |
| Laser Range/Designate | `O` | Activates laser (when armed) |
| Video Switch (TV/FLIR) | MFD OSB (mouse click) | Select sensor on MFD page |

> *⚠ Realism Divergence: The real MMS has additional operational modes (auto-track, scene lock, target handoff to other platforms via IDM) that are either simplified or not fully implemented in the DCS module. For BQT purposes, the student only needs to power on the MMS, select a sensor, and slew the sight to a general area.*

---

### 2.4 Weapon Panel — Identification Only

| Switch / Indicator | Location | Function | BQT Scope |
|---|---|---|---|
| **Master Arm** | Right console — Weapon Panel | ARM / SAFE — enables/disables all weapons | Identify location; leave in SAFE |
| **Weapon Select** | Right console — Weapon Panel | Selects active weapon station/type | Identify location only |
| **Weapon Release / Trigger** | Cyclic grip | Fires selected weapon when Master Arm is ARM | Identify location only |
| **Rocket Pair/Ripple** | Weapon Panel | Selects rocket firing mode | Identify location only |

**BQT Limitation:** The student must be able to **identify** these controls and state their function but will not employ weapons during the BQT course. The Master Arm switch will remain in SAFE throughout all BQT events.

---

### 2.5 AHRS/GPS Navigation System

| Component | Location | Function |
|---|---|---|
| **AHRS (Attitude Heading Reference System)** | Internal avionics bay | Provides heading, attitude, and position reference |
| **GPS Receiver** | Internal avionics bay | Provides position and ground speed data |
| **AHRS/GPS Controller** | Right console | Pilot interface for entering waypoints, selecting navigation mode |
| **MFD NAV Page** | Center instrument panel — MFD | Displays moving map, waypoints, bearing/distance/ETA |

#### Navigation Data Display

| Data | Where Displayed | Notes |
|---|---|---|
| **Current Position** | MFD NAV page (own-ship symbol) | Lat/Long or MGRS depending on configuration |
| **Bearing to Waypoint** | MFD NAV page, HSI | Magnetic bearing from current position |
| **Distance to Waypoint** | MFD NAV page | Nautical miles |
| **Ground Speed** | MFD NAV page | Knots |
| **Heading** | Heading indicator (analog) + MFD | Magnetic heading |
| **ETA** | MFD NAV page | Estimated time of arrival at selected waypoint |

> *⚠ Realism Divergence: The real OH-58D uses an Embedded GPS/INS (EGI) with a more complex alignment and initialization process including crypto key loading for military GPS. DCS simplifies alignment to a shorter time period and does not require crypto loading. The basic navigation functionality (waypoint selection, bearing/distance) is functionally identical.*

---

### 2.6 Engine Instruments

All engine instruments are located on the **left side of the instrument panel** (pilot's primary scan area) with digital readouts also available on the MFD ENG page.

| Instrument | Location | Normal Range | Caution / Warning |
|---|---|---|---|
| **Torque (Q) Gauge** | Instrument panel — left | 0–100% | > 100% continuous = caution; > 110% = warning |
| **TOT Gauge** | Instrument panel — left | < 737°C continuous | > 737°C = caution; > 810°C transient; > 843°C start |
| **N1 (Gas Producer) Gauge** | Instrument panel — left | Ground idle: ~62% / Flight: ~72–100% | > 104% = overspeed |
| **Nr (Rotor RPM) Gauge** | Instrument panel — left | Power on: 98–100% / Power off: 90–107% | < 90% = low rotor RPM (critical) |
| **Fuel Flow Indicator** | Instrument panel — left | ~200–350 lbs/hr (varies) | Cross-reference with fuel quantity for endurance |
| **Oil Pressure Gauge** | Instrument panel — left | 90–130 PSI | < 60 PSI = caution |
| **Oil Temperature Gauge** | Instrument panel — left | 70–107°C | > 107°C = caution |
| **Fuel Quantity Indicator** | Instrument panel — left | Calibrated in lbs | < 83 lbs = LOW FUEL caution |

**Primary Scan Pattern (Engine Instruments):**
The student should develop a clockwise scan: Torque → TOT → N1 → Nr → Fuel Flow → Oil Pressure → Oil Temperature → Fuel Quantity, then transition to flight instruments.

---

### 2.7 Caution/Advisory Panel

| Indicator | Color | Meaning |
|---|---|---|
| **MASTER CAUTION** | Amber (illuminated) | One or more caution conditions exist — check individual lights |
| **ENGINE OUT** | Red | Engine has failed or N1 below threshold |
| **FADEC** | Amber | FADEC degraded or in manual mode |
| **GEN** | Amber | Generator offline |
| **FUEL BOOST** | Amber | Fuel boost pump pressure low or off |
| **LOW FUEL** | Amber | Fuel quantity below ~83 lbs |
| **XMSN OIL PRESS** | Amber | Transmission oil pressure below limits |
| **XMSN OIL TEMP** | Amber | Transmission oil temperature above limits |
| **CHIP** (Main Trans / Tail Rotor / Engine) | Amber | Metal particles detected in respective oil system |
| **HYD** | Amber | Hydraulic pressure low or system failure |
| **FIRE** | Red | Engine/APU fire detected (if fire detection system modeled) |

#### Master Caution Reset

| Action | Control | Location |
|---|---|---|
| Reset master caution light | MASTER CAUTION reset button | Instrument panel — near master caution light |

The master caution light illuminates whenever a new caution condition triggers. Pressing the reset button extinguishes the master caution light but leaves the individual caution indicator illuminated until the condition is resolved.

> *⚠ Realism Divergence: The real OH-58D caution panel includes additional indicators (EMER BUS, INV, MAIN XMSN OIL HOT, T/R CHIP, ENG CHIP, etc.) and some are configurable. DCS may not model every individual caution indicator. The student should know the major caution lights and understand that any amber or red light requires immediate attention and cross-reference with the emergency procedures.*

---

### 2.8 Radar Altimeter

| Feature | Description |
|---|---|
| **Type** | Analog radar altimeter (APN-209 or similar) |
| **Location** | Lower instrument panel |
| **Range** | 0–1,500 ft AGL (typical) |
| **Low-Altitude Warning Bug** | Rotary knob sets the bug; audio and visual warning when descending through set altitude |
| **Display** | Analog needle on circular gauge |

**Usage:** The radar altimeter provides **actual height above ground level (AGL)**, which is critical for:
- Hover altitude verification (3–5 ft skid height for normal hover)
- Low-level flight (terrain following/terrain avoidance reference)
- Approach and landing (verifying altitude during deceleration to hover)

**Setting the Low-Altitude Bug:**
1. Rotate the bug-set knob to the desired warning altitude (e.g., 50 ft for approach, 200 ft for cruise).
2. When the aircraft descends through the set altitude, the low-altitude warning activates (typically an audio tone and a visual flag).

---

### 2.9 Flight Instruments

| Instrument | Location | Power Source | Function |
|---|---|---|---|
| **Attitude Indicator (AI)** | Instrument panel — right of center | AC (inverter required) | Pitch and roll reference |
| **Airspeed Indicator (ASI)** | Instrument panel — left of AI | Pitot-static (no electrical) | Indicated airspeed (KIAS) |
| **Barometric Altimeter** | Instrument panel — right of AI | Pitot-static (no electrical) | Pressure altitude; set local altimeter (Kollsman window) |
| **Vertical Speed Indicator (VSI)** | Instrument panel — below altimeter | Pitot-static (no electrical) | Rate of climb/descent (ft/min) |
| **Heading Indicator** | Instrument panel — below AI | AC (inverter required) or magnetic | Magnetic heading; requires periodic alignment with compass |
| **Turn Coordinator / Slip Ball** | Instrument panel — lower center | DC or AC | Yaw coordination; critical for hover and pedal turn reference |
| **Magnetic Compass** | Windshield frame (standby) | None (magnetic) | Backup heading reference; subject to errors in turns and accelerations |

**Power Failure Impact:**
- If the **inverter** fails: Attitude indicator and heading indicator (if electrically driven) become inoperative. The pilot must use the airspeed indicator, barometric altimeter, VSI, magnetic compass, and external visual references.
- If **pitot-static** is blocked: Airspeed indicator, altimeter, and VSI become unreliable. The pilot must use power settings and known performance data to estimate airspeed.

---

### 2.10 Lighting

#### Cockpit Lighting

| Control | Location | Function |
|---|---|---|
| **Instrument Panel Lights** | Overhead console — Lighting section | Illuminate instrument panel; rotary dimmer for brightness |
| **Console Lights** | Overhead console — Lighting section | Illuminate left and right consoles |
| **Standby Compass Light** | Overhead console | Illuminate magnetic compass |
| **NVG Compatibility Mode** | Overhead console or individual filters | Reduces lighting to NVG-compatible wavelengths (blue-green filtered) |
| **Caution Panel Brightness** | Near caution panel | Dim/bright for caution/advisory indicators |

#### Exterior Lighting

| Light | Location | Control | Purpose |
|---|---|---|---|
| **Position Lights (Nav Lights)** | Fuselage (red/green/white) | Overhead console — EXT LT section | Standard navigation lights; required for night flight |
| **Anti-Collision Light** | Tail boom / top of fuselage | Overhead console — ANTI-COL | Flashing red/white beacon; alerting other aircraft |
| **Landing Light** | Nose or skid-mounted | Collective grip switch or overhead console | High-intensity light for approach/landing |
| **Search Light** | Nose-mounted (if equipped) | Collective grip switch | Directional illumination; can be slewed in some configurations |
| **IR Formation Lights** | Various fuselage positions | Overhead console — IR | Visible only through NVGs; for NVG formation flight |

> *⚠ Realism Divergence: The real OH-58D has specific ANVIS NVG lighting configurations and covert IR lighting that are critical for night combat operations. DCS models basic NVG effects and IR lighting, but the full range of lighting configurations and NVG compatibility modes may be simplified.*

---

### 2.11 Collective and Cyclic Controls — HOTAS Functions

#### Collective Grip

| Control | Location on Grip | Function |
|---|---|---|
| **Throttle** | Twist grip (left hand) | Engine power in manual FADEC mode; set to FLY in auto mode |
| **Idle/Cutoff Detent** | Throttle rotation stops | IDLE = ground idle; OFF/CUTOFF = engine shutdown |
| **FLY Detent** | Throttle full open position | Flight idle; FADEC governing active |
| **Landing Light Switch** | Collective grip — forward | Toggle landing light ON/OFF |
| **Search Light Switch** | Collective grip — forward (if equipped) | Toggle/slew search light |
| **Radio Trigger (ICS/Radio)** | Collective grip — front | Press for intercom (ICS) or radio transmit |
| **Starter Button** | Collective grip or overhead console | Engage engine starter motor |

#### Cyclic Grip

| Control | Location on Grip | Function |
|---|---|---|
| **Force Trim Release** | Cyclic grip — thumb button | Press-and-hold to release force trim, reposition, release to set |
| **Weapon Release / Trigger** | Cyclic grip — index finger trigger | Fires selected weapon (Master Arm must be ARM) — BQT: identification only |
| **MMS Slew (Hat Switch)** | Cyclic grip — thumb hat (if configured) | Slew MMS sensor in azimuth/elevation |
| **Radio Trigger (alternate)** | Cyclic grip (depending on configuration) | Radio transmit alternate position |

#### Anti-Torque Pedals

| Control | Function |
|---|---|
| **Left Pedal** | Increases tail rotor thrust → yaw left (nose left) |
| **Right Pedal** | Decreases tail rotor thrust → yaw right (nose right) |
| **Pedal Adjust** | Center pedestal — pedal position adjustment for pilot leg length |

> *⚠ Realism Divergence: The real OH-58D HOTAS grip layout varies by block modification and unit configuration. The DCS module implements a standardized HOTAS layout. Some functions available on the real aircraft's collective or cyclic grips may be mapped to keyboard shortcuts in DCS rather than clickable grip buttons.*

---

### Instructor Notes — Module 2

| Common Student Error | Correction |
|---|---|
| Not knowing where engine instruments are in a scan | Force the student to verbalize the clockwise scan: Torque → TOT → N1 → Nr → Fuel → Oil. Repeat until automatic. |
| Ignoring the caution panel | Brief that MASTER CAUTION = "something is wrong, find out what." The student must immediately scan individual lights. |
| Failing to set radar altimeter bug | Include bug-setting in the before-takeoff check. Set bug to 50 ft for pattern work, adjustable for mission. |
| Confusion between MFD pages | Walk through each page during cockpit familiarization. NAV = where am I, ENG = how is the engine, MMS = what do I see. |
| Over-focusing on MMS during BQT | Redirect: "MMS is for familiarization. Your primary job in BQT is to fly the aircraft. MMS training comes later." |
| Not understanding force trim | Demonstrate: without releasing trim, the cyclic fights back. With trim released, controls are free. Student must develop the habit of trimming constantly. |

---

## Module 3: Ground Operations

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Perform a complete cold-and-dark startup from battery ON through engine running, avionics powered, and rotor system engaged — using cockpit switches, not autostart.
2. State the engine start abort criteria (hot start, hung start, no light-off) and demonstrate the correct abort procedure.
3. Perform the AHRS/GPS alignment procedure and confirm navigation system readiness.
4. Conduct a complete flight control check (cyclic, collective, pedals) and verify hydraulic pressure.
5. Transition the throttle from IDLE to FLY and verify Nr governing at 100%.
6. Conduct hover taxi at less than 20 knots and less than 3 ft skid height.
7. Complete all pre-takeoff checks from memory using the proper checklist flow.

---

### 3.1 Cold-and-Dark Startup — Full Switch-by-Switch Procedure

The following procedure takes the aircraft from a completely dead cockpit (all switches OFF, battery disconnected, engine cold) to fully operational with the rotor system turning and all avionics online.

#### Phase 1: Electrical Power-Up

| Step | Switch / Action | Location | Expected Result |
|---|---|---|---|
| 1 | **BATTERY** — ON | Overhead console — Electrical panel | Battery bus energized; some caution lights illuminate for self-test |
| 2 | **Caution Panel** — CHECK | Instrument panel — center | Verify caution lights illuminate for test, then extinguish (normal startup indications may persist until engine starts) |
| 3 | **Warning Light Test** — PRESS and hold | Instrument panel or overhead console | All caution/advisory lights illuminate; verify no burned-out bulbs |
| 4 | **INVERTER** — ON | Overhead console — Electrical panel | AC bus powered; attitude indicator and heading indicator begin to spool up |

> *⚠ Realism Divergence: The real OH-58D has a specific bus-tie and battery contactors sequence with voltage checks. DCS simplifies this to battery ON → immediate bus power. The student should still follow the correct switch sequence for procedural discipline.*

#### Phase 2: Fuel System

| Step | Switch / Action | Location | Expected Result |
|---|---|---|---|
| 5 | **FUEL BOOST PUMP** — ON | Overhead console — Fuel panel | FUEL BOOST caution light extinguishes; fuel pressure indication on gauge |
| 6 | **Fuel Quantity** — CHECK | Instrument panel — left | Verify adequate fuel for intended flight (minimum for BQT: ≥ 500 lbs recommended) |

#### Phase 3: Engine Start

| Step | Switch / Action | Location | Expected Result |
|---|---|---|---|
| 7 | **Throttle** — verify at **IDLE** (cutoff) detent | Collective grip — twist throttle | Throttle must be at idle detent for the start sequence to proceed |
| 8 | **ENGINE START** — PRESS | Overhead console — Engine panel (or collective grip) | Starter motor engages; N1 begins to increase |
| 9 | Monitor **N1** rising | Instrument panel — N1 gauge | N1 should accelerate smoothly |
| 10 | At **~15% N1** — fuel introduces (light-off) | Automatic (FADEC controlled) | TOT begins to rise; confirm light-off |
| 11 | Monitor **TOT** during start | Instrument panel — TOT gauge | **Must not exceed 843°C** (10-second start limit) |
| 12 | N1 accelerates to **~62–64%** (ground idle) | Instrument panel — N1 gauge | Engine stabilizes at ground idle; TOT settles below 737°C |
| 13 | **Oil Pressure** — CHECK | Instrument panel — Oil Press gauge | Within 90–130 PSI normal range; minimum 60 PSI |
| 14 | **Oil Temperature** — MONITOR | Instrument panel — Oil Temp gauge | Rising toward normal range (70–107°C); will take several minutes to stabilize |

**Engine Start Timeline (DCS):**

| Time (approx.) | Event | N1 (%) | TOT |
|---|---|---|---|
| 0 sec | START button pressed | 0 → rising | Ambient |
| ~5 sec | Starter cranking | ~10–12% | Ambient |
| ~8 sec | Light-off (fuel ignition) | ~15% | Rising rapidly |
| ~15 sec | Acceleration through | ~30–40% | Peak (monitor for hot start) |
| ~25 sec | Approaching idle | ~55–60% | Decreasing from peak |
| ~30–35 sec | Ground idle stabilized | ~62–64% | < 737°C continuous |

#### Start Abort Criteria

| Condition | Indication | Immediate Action |
|---|---|---|
| **Hot Start** | TOT exceeds 843°C during start | **THROTTLE — OFF** immediately; motor to purge residual fuel; wait 2 min before reattempt |
| **Hung Start** | N1 fails to accelerate past ~40% within 60 sec | **THROTTLE — OFF**; motor for 30 sec to clear; reattempt |
| **No Light-Off** | No TOT rise by ~25% N1 | **THROTTLE — OFF**; check FUEL BOOST is ON; motor to purge; reattempt |
| **Oil Pressure Failure** | Oil pressure does not rise within 30 sec of idle | **THROTTLE — OFF**; do not attempt further starts; maintenance required |

> *⚠ Realism Divergence: In the real OH-58D, a hot start can cause turbine blade thermal damage requiring borescope inspection and possible engine change. DCS models the temperature exceedance and prevents start completion but does not track cumulative thermal damage. The real aircraft also requires a specific motoring procedure (starter engaged, throttle OFF) to purge fuel and cool the turbine — DCS models this but the cooling may be compressed in time.*

#### Phase 4: Post-Start / Generator and Avionics

| Step | Switch / Action | Location | Expected Result |
|---|---|---|---|
| 15 | **GENERATOR** — ON | Overhead console — Electrical panel | GEN caution light extinguishes; generator powering DC bus |
| 16 | **Voltmeter** — CHECK | Instrument panel or overhead console | ~28V DC (generator output) |
| 17 | Engine warm-up — **2 minutes at IDLE** | — | Allow oil to circulate and engine temperatures to stabilize |
| 18 | **MFD** — ON | Overhead console — Avionics section or MFD power switch | MFD powers on; displays initial page |
| 19 | **AHRS/GPS** — ON | Right console — AHRS/GPS controller | System begins alignment (see Section 3.2) |
| 20 | **Radios** — ON | Right console — Radio panels | VHF/FM (ARC-201), UHF (ARC-164) power on; set frequencies |
| 21 | **Transponder** — ON and set | Right console — Transponder panel | Set to assigned squawk code |
| 22 | **MMS** — ON (optional for BQT) | Left console or overhead — MMS power | MMS powers on; FLIR requires ~3–5 min warmup |

> *⚠ Realism Divergence: The real OH-58D avionics power-on sequence includes additional steps for IDM (Improved Data Modem) initialization, HAVE QUICK radio setup, and IFF/AIMS crypto loading. DCS simplifies avionics initialization — radios power on immediately with frequency selection only.*

#### Phase 5: Hydraulic and Flight Control Check

| Step | Switch / Action | Location | Expected Result |
|---|---|---|---|
| 23 | **Hydraulic Pressure** — CHECK | Instrument panel — HYD gauge | ~1,000 PSI (system nominal); HYD caution light OFF |
| 24 | **Flight Control Check** — full deflection: cyclic (forward, aft, left, right), collective (full up, full down), pedals (full left, full right) | All controls — physical movement | Controls move smoothly through full range with hydraulic assist; no binding or unusual resistance |
| 25 | **Force Trim** — CHECK | Cyclic grip — force trim release button | Press-and-release: controls should hold position; release and feel for detent/lock |

---

### 3.2 AHRS/GPS Alignment

| Phase | Duration (DCS) | Duration (Real) | Indication |
|---|---|---|---|
| **Coarse Alignment** | ~30 sec | ~2 min | AHRS/GPS controller shows ALIGN status |
| **Fine Alignment** | ~2–3 min | ~5–8 min | Status transitions from ALIGN to NAV |
| **Navigation Ready** | Total ~3 min | Total ~8–10 min | NAV mode active; position and heading valid |

**Procedure:**
1. AHRS/GPS controller — power ON (already completed in Phase 4, Step 19).
2. Verify aircraft is **stationary** during alignment (movement degrades alignment quality).
3. Monitor alignment status on AHRS/GPS controller or MFD NAV page.
4. When status shows **NAV** — alignment is complete; position and heading data are valid.
5. Verify displayed position against known parking location (gross error check).

> *⚠ Realism Divergence: The real OH-58D EGI alignment takes 8–10 minutes for full accuracy and can be degraded by aircraft movement, vibration, or nearby magnetic interference. DCS compresses alignment time to approximately 3 minutes. The real system also has a stored heading alignment mode (~90 sec) with degraded accuracy that DCS may not differentiate.*

---

### 3.3 Rotor Engagement

| Step | Action | Expected Result | Caution |
|---|---|---|---|
| 1 | Verify engine stabilized at ground idle (~62% N1, TOT < 737°C) | Engine instruments in normal range | Do not advance throttle until engine is stable and warmed up |
| 2 | **Throttle** — rotate smoothly from **IDLE** to **FLY** (flight idle detent) | N1 increases to ~72%+; FADEC governs Nr toward 100% | Advance throttle smoothly — abrupt advancement can cause TOT spike |
| 3 | Monitor **Nr** increasing | Nr climbs from ground idle (~62–65%) toward 100% | Takes ~15–30 sec for Nr to stabilize at 100% |
| 4 | Nr stabilizes at **100%** | Nr gauge reads 100% ± 1% | If Nr does not reach 100%, check FADEC mode — ensure AUTO |
| 5 | Verify **Torque (Q)** reading | Should be ~20–35% at flat pitch (collective full down) on the ground | Higher torque at flat pitch may indicate dragging brakes or mis-rigged controls |

**Rotor Engagement Cautions:**
- **Never advance throttle abruptly** — this can cause TOT overshoot and N1 overspeed.
- **Ensure area is clear** — rotor blade tip path describes a 35 ft diameter circle.
- **Collective must be full down** (flat pitch) during throttle advancement — blade pitch at flat minimizes load on the engine during rotor spin-up.
- **Crew and ground personnel** must be briefed on rotor engagement; remain clear of the rotor disc arc.

---

### 3.4 Ground Taxi (Hover Taxi)

The OH-58D has **fixed skids** — there is no wheeled ground taxi capability. All ground movement is accomplished by **hover taxi** at less than 20 knots and less than 3 ft skid height.

| Parameter | Value | Notes |
|---|---|---|
| **Max Hover Taxi Speed** | < 20 knots ground speed | Higher speeds in hover regime risk uncontrolled translation |
| **Hover Taxi Height** | < 3 ft skid height | Minimizes ground effect turbulence on other aircraft/personnel |
| **Surface Awareness** | Continuously scan for obstacles, personnel, loose debris | Rotor downwash can lift FOD and endanger nearby personnel |

**Technique:**
1. From a stable hover at 3–5 ft skid height, apply slight forward cyclic to begin forward movement.
2. Use pedals to maintain heading.
3. Collective adjustments to maintain constant altitude (terrain changes require collective response).
4. Speed control: more forward cyclic = more speed; aft cyclic (flare) to decelerate.
5. To stop: aft cyclic to arrest forward movement, then stabilize in a hover.

**Hover Taxi Hazards:**
- **Brownout/whiteout:** Over dusty or snowy surfaces, rotor downwash can create zero-visibility conditions. Maintain constant scan of visual references at the periphery.
- **FOD:** Loose debris becomes projectiles in rotor downwash.
- **Confined areas:** Be aware of rotor clearance (35 ft diameter) when taxiing near buildings, other aircraft, or obstacles.

---

### 3.5 Pre-Takeoff Checks

Conduct at the hover spot or holding area before departing into the traffic pattern or departing the airfield.

| Check | Action | Verify |
|---|---|---|
| **Engine Instruments** | Scan Torque, TOT, N1, Nr, Oil Press, Oil Temp | All in normal operating range |
| **Torque Available (Power Check)** | Note torque required to hover at 3–5 ft IGE; compare to torque limit (100% continuous) | Adequate margin for OGE operations and maneuvering (typically need ~15–20% margin above hover torque) |
| **Nr** | Verify FADEC governing | 100% ± 1% |
| **Caution Panel** | Scan all indicators | No caution lights illuminated |
| **Flight Controls** | Verify free and correct response | Cyclic, collective, pedals respond normally |
| **Force Trim** | Check set and functional | Cyclic holds position when released |
| **Radios** | Check comm on assigned frequencies | Two-way comm established with tower/flight |
| **Altimeter** | Set to local altimeter setting (QNH) | Barometric altimeter shows field elevation ± 75 ft |
| **Radar Altimeter** | Set low-altitude bug as appropriate | Bug set (e.g., 50 ft for pattern work) |
| **Transponder** | Verify squawking assigned code | Transponder in ALT mode |
| **Doors/Harness** | Doors secured; harness tight and locked | — |

#### Cockpit Switch Reference — Pre-Takeoff

| Item | Switch / Action | Location |
|---|---|---|
| Engine instruments scan | Visual check of all gauges | Instrument panel — left |
| Caution panel check | Visual scan | Instrument panel — center |
| Altimeter set | Rotate Kollsman knob | Instrument panel — right (altimeter) |
| Radar alt bug set | Rotate bug-set knob | Lower instrument panel — radar altimeter |
| Transponder set | Select mode and code | Right console — transponder panel |
| Radio check | Key radio trigger on collective grip | Collective grip — radio trigger |

---

### Instructor Notes — Module 3

| Common Student Error | Correction |
|---|---|
| Starting engine with throttle not at IDLE detent | Critical: DCS requires throttle at IDLE for start. If not in detent, starter will engage but no light-off occurs. Brief the student to verify throttle position before every start attempt. |
| Not monitoring TOT during start | Emphasize: TOT is the instrument to watch during start. N1 can be checked with peripheral vision, but TOT exceedances cause damage. |
| Advancing throttle too quickly from IDLE to FLY | Demo the smooth, continuous twist. A jerky advancement causes TOT spike and possible Nr overshoot. "Like turning a volume knob, not flipping a switch." |
| Skipping the flight control check | Reinforce: the flight control check confirms hydraulics are working and controls are not jammed. In a real aircraft, this check catches rigging errors and hydraulic failures before they matter. |
| Moving the aircraft during AHRS alignment | The aircraft must be stationary. Any movement (including wind rocking) degrades alignment. Wait for NAV indication before hover taxi. |
| Attempting to hover taxi too fast | Hover taxi is slow and deliberate. Students from fixed-wing backgrounds want to "taxi to the runway" — brief that hover taxi is measured, with constant altitude and heading corrections. |
| Not conducting a power check before departure | The power check confirms the aircraft can hover OGE and has maneuvering margin. Without it, the student may lift off and discover insufficient power to clear obstacles. |

---

## Module 4: Hover & Takeoff

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Pick the aircraft up to a stable 3–5 ft hover from the ground using smooth, coordinated collective, cyclic, and pedal inputs.
2. Perform a hover power check and determine if adequate power is available for OGE operations.
3. Execute 360° hover pedal turns (left and right) while maintaining position and altitude within ±5 ft and ±3 ft respectively.
4. Conduct hover taxi (forward, sideward, rearward) at speeds below 20 knots while maintaining altitude and heading.
5. Perform a normal takeoff: accelerate from hover through ETL, manage aircraft attitude changes, and establish a climb at Vy (55–60 KIAS).
6. Describe and execute a no-hover takeoff and a maximum performance takeoff profile.
7. Recognize and respond to ground resonance indications.

---

### 4.1 Hover Technique

#### Picking Up to a Hover

This is the foundational rotary-wing skill. The student transitions the aircraft from resting on the skids to a stable hover at 3–5 ft AGL.

**Procedure:**
1. Verify collective is at the **full-down** (flat pitch) position.
2. Verify pedals are approximately centered (slight left pedal anticipated for torque compensation).
3. Pick an outside visual reference point (a spot on the ground 20–30 ft ahead at approximately 1 o'clock position).
4. **Slowly and smoothly increase collective** — as the aircraft becomes light on the skids:
   - Add **left pedal** to compensate for increasing torque (main rotor torque reaction causes right yaw).
   - Apply **slight right cyclic** to compensate for translating tendency (left drift).
   - Adjust **fore/aft cyclic** to prevent drift.
5. Continue increasing collective until the aircraft lifts to 3–5 ft skid height on the radar altimeter.
6. **Stop collective input** and make fine adjustments to stabilize.

| Control Input | Purpose | Common Error |
|---|---|---|
| Collective (up) | Increases rotor blade pitch angle → more lift | Over-pulling: launches to 10+ ft; under-pulling: never leaves the ground |
| Left pedal | Counteracts main rotor torque reaction (right yaw) | Late pedal input: aircraft yaws right significantly before correction |
| Right cyclic (slight) | Counteracts translating tendency (left drift) | None applied: aircraft drifts left; over-applied: aircraft drifts right |
| Fore/aft cyclic | Maintains position over the spot | Over-controlling: pilot-induced oscillation (PIO) |

**Key Torque Reference for Hover:**

| Condition | Approximate Hover Torque | Notes |
|---|---|---|
| Light (4,000 lbs, sea level, ISA) | ~55–65% | Significant power margin available |
| Mid (4,800 lbs, sea level, ISA) | ~70–80% | Normal BQT training weight |
| Heavy (5,500 lbs, sea level, ISA) | ~85–95% | Near max; minimal OGE margin |
| High/Hot (5,000 lbs, 5,000 ft DA) | ~80–95% | Density altitude significantly reduces power available |

> *⚠ Realism Divergence: In the real OH-58D, hover technique requires constant micro-corrections with all four controls simultaneously. DCS models this accurately, but control force feedback (if using a non-force-feedback stick) may feel different. The student should develop the habit of making small, smooth inputs — the OH-58D responds quickly due to its light weight.*

---

#### Hover Power Check

Before departing the hover spot, the student must verify that adequate power is available for the planned operation.

**Procedure:**
1. Establish a stable hover at 3–5 ft IGE.
2. Note torque required to hover (e.g., 72%).
3. Compare to maximum continuous torque (100%).
4. Calculate margin: 100% − 72% = **28% margin**.
5. Determine if margin is sufficient:
   - **OGE hover:** Typically requires 15–20% more torque than IGE hover.
   - **Maneuvering margin:** Need at least 5–10% above OGE hover torque for safe maneuvering.
   - If IGE hover torque is **above 80%**, OGE operations and obstacle clearance may be marginal.

| Decision | Criteria | Action |
|---|---|---|
| **GO** | IGE hover torque ≤ 80% (sea level) | OGE capable with adequate margin |
| **MARGINAL** | IGE hover torque 80–90% | OGE possible but limited margin; consider running takeoff |
| **NO-GO (for normal takeoff)** | IGE hover torque > 90% | Cannot sustain OGE hover; must use no-hover or running takeoff or reduce weight |

---

#### Hover Pedal Turns (360° Turns)

**Purpose:** Develop yaw control skill and demonstrate the relationship between power, torque, and pedal authority.

**Procedure:**
1. Establish stable hover at 3–5 ft.
2. Apply **left pedal** to begin a left (counterclockwise) turn.
3. Maintain altitude with collective — pedal turns change yaw, which changes the tail rotor thrust vector, which changes power demand slightly.
4. Maintain position over the ground reference — the aircraft will tend to translate in the direction of the turn due to tail rotor thrust.
5. Complete a smooth 360° turn and stabilize on the original heading.
6. Repeat to the **right** (right pedal turn) — note that right pedal turns require **less** left pedal authority and may be faster/easier.

**Standards:**
- Maintain position within ±5 ft of the reference point.
- Maintain altitude within ±3 ft.
- Complete 360° turn smoothly without abrupt stops or jerks.
- Constant rate of turn throughout.

**Hazard — LTE during Pedal Turns:**
During a right pedal turn (nose moving clockwise), the tail may pass through the critical LTE azimuths relative to the wind. If the wind is from the front-right quadrant, the tail will momentarily face the wind during the turn, and as it passes through the 285°–315° sector, LTE can develop.

**Mitigation:** Perform hover pedal turns into the wind (wind on the nose) when possible. Be prepared to apply forward cyclic and reduce collective if uncommanded right yaw develops.

---

#### Hover Taxi (Forward, Sideward, Rearward)

| Direction | Technique | Max Speed | Hazard |
|---|---|---|---|
| **Forward** | Slight forward cyclic from hover; pedals maintain heading; collective maintains altitude | < 20 kts | Overtaxiing — too much speed in hover regime leads to uncontrolled acceleration |
| **Sideward (Right)** | Right cyclic from hover; pedals maintain heading; collective maintains altitude | 35 kts (structural) / < 20 kts (practical) | LTE if wind aligns with critical azimuths; tail strike on obstacles |
| **Sideward (Left)** | Left cyclic from hover; pedals maintain heading; collective maintains altitude | 35 kts (structural) / < 20 kts (practical) | Tail rotor clearance on obstacles to the right (tail rotor is on left side, but fuselage translates left) |
| **Rearward** | Aft cyclic from hover; pedals maintain heading; collective maintains altitude | 35 kts (structural) / < 20 kts (practical) | Cannot see behind; requires crew coordination or ground guide; tail strike risk |

> *⚠ Realism Divergence: Sideward and rearward hover taxi limits in DCS may not enforce the 35-knot structural limit with the same fidelity as the real aircraft. The student should self-impose the 20-knot practical limit for safety.*

---

### 4.2 Takeoff Profiles

#### Normal Takeoff (From Hover)

The standard departure: from a stable hover, accelerate into forward flight and climb.

**Procedure:**
1. From a stable hover at 3–5 ft IGE, facing into the wind (or as assigned).
2. Apply **forward cyclic** to begin forward acceleration.
3. As the aircraft accelerates through **10–15 knots**, expect:
   - Increased vibration (transverse flow effect).
   - Slight right roll tendency.
   - Correct with left cyclic.
4. As the aircraft accelerates through **16–24 knots (ETL)**:
   - Nose pitches up (translational lift kicks in — rotor becomes more efficient).
   - Aircraft tends to climb — **reduce collective slightly** to maintain desired climb rate.
   - Aircraft yaws left (reduced torque requirement = reduced anti-torque demand = nose yaws left) — **right pedal** correction.
   - Apply **forward cyclic** to maintain accelerating attitude.
5. Continue accelerating to **Vy (55–60 KIAS)** and establish climb.
6. At 500 ft AGL or clear of obstacles, continue to cruise climb or level off as briefed.

| Phase | Airspeed | Expected Aircraft Behavior | Pilot Correction |
|---|---|---|---|
| Hover → acceleration | 0–10 kts | Forward translation begins | Forward cyclic; pedals maintain heading |
| Transverse flow | 10–20 kts | Vibration, right roll | Left cyclic; maintain heading |
| ETL | 16–24 kts | Nose up, yaw left, climb tendency | Forward cyclic, right pedal, reduce collective slightly |
| Climb established | 55–60 kts (Vy) | Stable climb; smoother ride | Trim for Vy; adjust collective for desired climb rate |

---

#### No-Hover Takeoff (Performance Limited)

Used when the aircraft **cannot sustain a hover** at the current weight/altitude/temperature, but can fly in forward flight (where translational lift provides the additional efficiency needed).

**Procedure:**
1. Aircraft on the ground, rotor at 100%, collective at flat pitch.
2. Smoothly and continuously increase collective while simultaneously applying **forward cyclic**.
3. The aircraft will become light on the skids and begin to slide forward before achieving a full hover.
4. As forward speed builds and translational lift develops, the aircraft will become airborne.
5. Continue accelerating to Vy and climb.

**Caution:** This technique requires a clear, unobstructed departure path. The aircraft may not clear obstacles in the initial climb segment.

---

#### Maximum Performance Takeoff

Used when obstacles (trees, buildings, wires) immediately surround the takeoff area and the pilot needs to gain maximum altitude in minimum distance.

**Procedure:**
1. From a stable hover at maximum available altitude (5–10 ft IGE, or as high as power permits).
2. Verify maximum torque available (do not exceed 110% transient).
3. Apply **maximum collective** (up to transient torque limit) while simultaneously applying **forward cyclic** to begin acceleration.
4. Maintain a steep nose-up attitude (~10–15° nose up) to trade airspeed for altitude during the initial climb.
5. As the aircraft clears the obstacles, transition to Vy attitude and reduce torque to continuous limits.

**Standards:**
- Maximum altitude gain in minimum distance.
- Torque may exceed 100% (transient limit: 110% for 10 seconds).
- This is a high-workload, high-risk maneuver — brief it thoroughly before execution.

> *⚠ Realism Divergence: The real OH-58D max performance takeoff is limited by actual engine/transmission torque available on the day (weight, altitude, temperature). DCS models torque limitations, but the pilot should practice this maneuver at different weight/altitude combinations to understand the actual margins.*

---

### 4.3 Climb Profiles

| Profile | Airspeed (KIAS) | Purpose | Notes |
|---|---|---|---|
| **Vy (Best Rate of Climb)** | 55–60 | Maximum altitude gain per unit time | Standard departure climb |
| **Cruise Climb** | 70–80 | Balance between climb rate and forward progress | Used when distance is a factor |
| **Vx (Best Angle of Climb)** | 45–50 | Maximum altitude gain per unit distance | Obstacle clearance after max performance takeoff |

**Climb Power Setting:**
- Vy climb: torque as required to maintain 55–60 KIAS at desired climb rate, not to exceed 100% continuous.
- Expected climb rate (sea level, mid weight): ~800–1,200 ft/min.
- Higher altitude and weight reduce climb rate significantly.

---

### 4.4 Departure Procedures

**Standard VFR Departure:**
1. After takeoff, climb on runway/takeoff heading to 500 ft AGL.
2. At 500 ft AGL, begin turn to departure heading as briefed (or as directed by ATC/tower).
3. Continue climb to pattern altitude or cruise altitude.
4. Depart the traffic area as briefed.

**Communication:**
- Before takeoff: "Tower/Traffic, [callsign], [location], departing [direction]."
- After clearing the traffic area: switch to en-route frequency.

---

### 4.5 Ground Resonance

**What It Is:** Ground resonance is a self-exciting, rapidly divergent oscillation that occurs when the helicopter is in contact with the ground and the lead-lag motion of the main rotor blades becomes coupled with the natural frequency of the fuselage on its landing gear. In the OH-58D, this can occur on hard surfaces when one skid has more contact than the other (partial contact), or when a landing shock excites the rotor system.

**Conditions:**
- Hard or paved surface (soft ground absorbs energy and prevents the resonance from building)
- One skid contact (partial ground contact during takeoff or landing)
- Rotor RPM in a critical range (usually near normal operating RPM)
- Unbalanced rotor condition (blade damage, ice accumulation)

**Recognition:** Violent lateral or longitudinal oscillation that **increases rapidly** in amplitude. The oscillation develops in seconds and can destroy the aircraft within 5–10 seconds if not corrected.

**Immediate Action (Boldface):**

| Condition | Action | Rationale |
|---|---|---|
| **Nr is in the normal flight range (≥ 90%)** | **COLLECTIVE — FULL UP** (fly away from the ground) | Breaking ground contact eliminates the ground resonance coupling. Once airborne, the oscillation ceases immediately. |
| **Nr is below safe flight range (< 90%)** or engine is not running | **THROTTLE — OFF / MIXTURE — CUTOFF** and **COLLECTIVE — FULL DOWN** | Cannot fly; must stop the rotor as quickly as possible to prevent structural failure |

> *⚠ Realism Divergence: Ground resonance is more common in helicopters with articulated rotors and especially on hard surfaces. The OH-58D's soft-in-plane rotor system is designed to be resistant to ground resonance, but it is not immune. DCS may or may not model ground resonance with full fidelity — the student should know the procedure regardless, because the correct response (fly or shut down) is the same across all helicopter types.*

---

### Instructor Notes — Module 4

| Common Student Error | Correction |
|---|---|
| Over-pulling collective on initial hover pickup | "Slowly" is the key word. Demonstrate a smooth, 3–5 second collective pull from flat pitch to hover. The aircraft should rise gently, not leap. |
| Failing to add left pedal during collective increase | Brief the coupling: "Collective up = right yaw. You must lead with left pedal as you pull collective, or the aircraft will yaw right before you can correct." |
| Pilot-Induced Oscillation (PIO) in hover | The OH-58D is responsive. Students over-correct, then over-correct the correction, creating oscillation. Teach: "Small inputs. Wait for the aircraft to respond before adding more. Relax your grip." |
| Not conducting hover power check | Make it a mandatory checklist item. "What's your hover torque? What's your torque available? Can you fly OGE?" If the student can't answer, they don't depart. |
| Panic during ETL transition | Brief extensively: "At 16–24 knots, the aircraft will pitch up and you'll feel a bump. It's translational lift — it's good. Forward cyclic, slight right pedal, reduce collective slightly." |
| Attempting maximum performance takeoff without proper briefing | This is a high-risk maneuver. Do not introduce it until the student has demonstrated consistent normal takeoffs. Brief the power limits and abort criteria before every max performance attempt. |
| Ignoring ground resonance briefing | Even if DCS doesn't fully model it, the student must know: "If the aircraft shakes violently on the ground — fly or die." The response must be instinctive. |

---

## Module 5: Basic Flight Maneuvers

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Maintain straight-and-level flight at various airspeeds (40, 60, 80, 100 KIAS) and altitudes using proper trim technique.
2. Execute coordinated turns at 15°, 30°, and 45° of bank while maintaining altitude within ±100 ft.
3. Perform climbs and descents at specified airspeeds and rates, managing power and Nr throughout.
4. Demonstrate slow flight characteristics near and below ETL, recognizing the increased power requirement and control sensitivity.
5. Execute a practice autorotation entry at altitude: lower collective, maintain Nr, establish autorotation airspeed (60–80 KIAS), and perform a power recovery.
6. Demonstrate proper force trim technique — trimming for each airspeed, power setting, and configuration change.
7. Execute smooth acceleration and deceleration between different cruise speeds while maintaining altitude.

---

### 5.1 Straight-and-Level Flight

#### Power and Speed Relationships

Unlike fixed-wing aircraft where power primarily controls altitude and pitch controls speed, in a helicopter **collective (power) and cyclic (attitude) are interdependent for both altitude and speed**. The relationship is:
- **More forward cyclic** → nose down → airspeed increases → altitude tends to decrease → add collective to maintain altitude.
- **More collective** → more lift → altitude increases → aircraft decelerates unless cyclic is adjusted.

In practice, the student should think: "Cyclic controls where I'm going, collective controls whether I stay at this altitude."

#### Cruise Speed Reference

| Airspeed (KIAS) | Approximate Torque (mid-weight, SL) | Flight Regime | Notes |
|---|---|---|---|
| 40 | 55–65% | Slow cruise / approaching ETL boundary | High power, nose-up attitude, sensitive controls |
| 60 | 45–55% | Normal cruise (low) | Good visibility, moderate power |
| 80 | 40–50% | Normal cruise (efficient) | Typical cross-country speed |
| 100 | 45–55% | High-speed cruise | Near max range speed; approaching Vne at high weight |
| 110–120 | 50–60%+ | Vne region | Do not exceed; configuration dependent |

**Note:** The power-required curve for helicopters is "bucket-shaped" — power required is high at very low airspeeds (hover), decreases to a minimum in the 60–80 KIAS range, then increases again at high airspeeds due to parasite drag. The student should understand this concept to manage fuel endurance.

#### Trim Technique

The OH-58D force trim system requires active management:

1. As airspeed changes, the aerodynamic forces on the rotor system change, altering the cyclic forces the pilot feels.
2. **After any airspeed or power change**, the pilot should:
   - Press and hold the **force trim release** button (cyclic grip).
   - Reposition the cyclic to the desired neutral position.
   - Release the force trim button — the cyclic is now "set" at the new position.
3. If the pilot does not re-trim, they will be fighting constant cyclic forces, increasing fatigue and degrading precision.

**Trim Scenarios:**

| Situation | Required Trim Action |
|---|---|
| Accelerate from 60 to 80 KIAS | Trim forward — nose wants to pitch up as you accelerate (cyclic moves forward, trim the new position) |
| Decelerate from 80 to 60 KIAS | Trim aft — nose wants to pitch down as you decelerate |
| Increase collective for climb | Trim cyclic slightly (aircraft tendency changes); trim pedals (more torque = more left pedal) |
| Decrease collective for descent | Trim cyclic and pedals for the new power setting |

---

### 5.2 Coordinated Turns

**Technique:**
1. Pick a visual reference on the horizon in the direction of the turn.
2. Apply **cyclic in the direction of the turn** (left stick for left turn, right stick for right turn).
3. As the bank establishes, apply **slight aft cyclic** to maintain the nose on the horizon (prevents nose from dropping in the turn).
4. Add **collective** as bank increases to maintain altitude — a banked turn increases the load factor, requiring more total lift.
5. Add **pedal as needed** to keep the slip ball centered (coordinated flight).
6. To roll out: apply **opposite cyclic** to level the wings, reduce collective to level-flight setting, adjust pedals.

#### Bank Angle and G-Loading

| Bank Angle | Load Factor (G) | Collective Increase Required | Notes |
|---|---|---|---|
| 15° | 1.04 G | Negligible | Gentle turn — training standard |
| 30° | 1.15 G | ~5% torque increase | Moderate turn — standard maneuvering |
| 45° | 1.41 G | ~15% torque increase | Aggressive turn — significant power required |
| 60° | 2.0 G | ~40% torque increase | **Near structural limit** (max 2.5 G); avoid at high gross weight |

**G-Limit Awareness:** The OH-58D is limited to +2.5 G at max gross weight. At 60° of bank, the load factor is 2.0 G — leaving only 0.5 G of margin. Students must be aware that high-bank-angle turns at heavy weights rapidly approach structural limits.

> *⚠ Realism Divergence: DCS models G-loading effects on the aircraft structure and rotor system. However, the pilot may not receive as much physical feedback (seat-of-the-pants G feel) as in the real aircraft. The student should monitor the G-meter (if available on MFD) and limit bank to 45° during BQT maneuvers.*

---

### 5.3 Climbs and Descents

#### Climbs

| Type | Airspeed (KIAS) | Technique | Power Setting |
|---|---|---|---|
| **Normal Climb (Vy)** | 55–60 | Forward cyclic to maintain Vy, increase collective for desired climb rate | As required, ≤ 100% torque continuous |
| **Cruise Climb** | 70–80 | Slight collective increase from cruise, maintain airspeed with cyclic | ~5–10% above cruise torque |
| **Max Angle Climb (Vx)** | 45–50 | Steep nose-up attitude; maximum altitude per distance | Maximum continuous power |

**Nr Awareness in Climbs:**
During a climb, the engine works harder. In FADEC auto mode, Nr should remain at 100%. If the pilot demands more power than available (pulling collective above the torque limit), FADEC will attempt to maintain Nr but TOT will approach limits. The student must monitor torque and TOT.

#### Descents

| Type | Airspeed (KIAS) | Technique | Power Setting |
|---|---|---|---|
| **Normal Descent** | 80 | Reduce collective to reduce power, forward cyclic to maintain airspeed, descend at 500–1,000 FPM | Reduced from cruise |
| **Cruise Descent** | 80–100 | Slight collective reduction; gradual descent | ~5–10% below cruise torque |
| **Emergency Descent** | 80 | Aggressive collective reduction; may use autorotation profile | Near flat pitch; Nr management critical |

**Nr Awareness in Descents:**
Reducing collective rapidly can cause **Nr to increase above 100%** (the rotor blades are unloaded and windmilling). The FADEC will attempt to govern, but rapid collective reductions in combination with descent can cause Nr overshoot. The student must reduce collective smoothly and monitor Nr, especially in autorotation-entry practice.

> *⚠ Realism Divergence: In the real OH-58D, Nr overspeed above 107% (power off) is a structural concern for the rotor head and mast. DCS models Nr governing and overspeed to varying degrees of fidelity. The student should develop the habit of smooth, progressive collective changes rather than abrupt inputs.*

---

### 5.4 Slow Flight

Slow flight occurs at airspeeds **below ETL** (approximately < 24 knots), where the helicopter transitions from translational flight back toward the hover regime.

**Characteristics of Slow Flight:**
- **Power required increases** as translational lift diminishes.
- **Control sensitivity increases** — cyclic inputs produce larger attitude changes.
- **Pedal authority changes** — more left pedal required as torque increases to maintain altitude.
- **Aircraft instability increases** — the helicopter is less stable in all axes below ETL.
- **Settling with power risk** increases if the aircraft is descending while slow.

**Training Purpose:** The student must understand the transition between forward flight and hover, and recognize the visual/tactile cues (increased vibration, nose-up pitch tendency, increased power demand) that indicate ETL is decaying.

| Speed Range | Characteristics | Required Inputs |
|---|---|---|
| 30–24 KIAS | Beginning transition; slight power increase needed | Small collective increase; forward cyclic to maintain speed |
| 24–16 KIAS | ETL decaying; noticeable power increase; vibration increases (transverse flow) | Significant collective increase; pedal adjustment; cyclic becomes more sensitive |
| < 16 KIAS | Hover regime; maximum power required for altitude maintenance | Full hover control technique; coordinated inputs on all controls |

---

### 5.5 Autorotation Entry (Practice)

**Purpose:** The autorotation is the single most critical emergency maneuver in single-engine helicopter operations. In the BQT course, the student practices **autorotation entry and power recovery at altitude** — not a full autorotation to the ground. Full autorotations are introduced in later training.

#### What Is Autorotation?

When the engine fails (or the freewheeling unit disengages the engine from the rotor), the main rotor is no longer powered. However, the rotor can continue to spin if the pilot **immediately lowers the collective** (reduces blade pitch). Air flowing upward through the rotor disc (as the aircraft descends) drives the rotor — the rotor becomes a windmill, using the aircraft's gravitational potential energy to maintain rotor RPM.

#### Entry Procedure (Engine Failure in Forward Flight)

| Step | Action | Reason |
|---|---|---|
| 1 | **COLLECTIVE — FULL DOWN** (immediately) | Reduces blade pitch to allow air to drive the rotor; prevents Nr decay |
| 2 | **PEDALS — ADJUST** (right pedal in autorotation) | With no engine torque, less anti-torque is needed; the aircraft will yaw right if pedals are not adjusted |
| 3 | **CYCLIC — ADJUST** for autorotation airspeed (60–80 KIAS) | 60 KIAS = minimum rate of descent; 80 KIAS = maximum glide distance |
| 4 | **Nr — MONITOR** (must remain 90–107%) | Nr below 90% = rotor stall risk; above 107% = structural risk |

#### Autorotation Key Data

| Parameter | Value | Notes |
|---|---|---|
| **Autorotation Airspeed (Min RoD)** | 60 KIAS | Minimum rate of descent — best for hovering autorotation or when landing site is close |
| **Autorotation Airspeed (Max Glide)** | 80 KIAS | Maximum distance — best when landing site is farther away |
| **Nr Range (Autorotation)** | 90–107% | Must remain in this range throughout; FADEC is not governing (engine is failed) |
| **Rate of Descent (Autorotation)** | ~1,500–2,000 FPM | Varies with weight and airspeed; the OH-58D descends rapidly in autorotation |
| **Glide Ratio** | ~4:1 | For every 1,000 ft of altitude, the aircraft glides approximately 4,000 ft forward at max glide speed |
| **Available Reaction Time** | ~1–2 seconds | Time from engine failure recognition to collective-down before Nr decays below safe limits |

**Practice Autorotation at Altitude (Power Recovery):**
1. Instructor announces "simulated engine failure" (or reduces throttle to idle in DCS).
2. Student **immediately lowers collective to full down**.
3. Student adjusts pedals and cyclic for autorotation airspeed (60–80 KIAS).
4. Student monitors Nr (should stabilize in 90–107% range).
5. After demonstrating stable autorotation glide for ~500–1,000 ft altitude loss:
   - **COLLECTIVE — INCREASE** (smooth, not abrupt)
   - **THROTTLE — FLY** (if manually reduced)
   - FADEC re-governs Nr to 100%.
   - Student resumes powered flight.

> *⚠ Realism Divergence: In the real OH-58D, autorotation entry must occur within approximately 1 second of engine failure to prevent Nr from decaying below 90%. DCS models Nr decay rate accurately enough for training purposes, but the sensation of urgency may be less intense without physical motion cues. The instructor should emphasize that autorotation entry is a reflex, not a decision — "The collective goes down before you finish thinking about it."*

---

### 5.6 Speed Changes (Acceleration / Deceleration)

#### Acceleration (e.g., 60 → 100 KIAS)

1. Apply forward cyclic (nose down) → airspeed increases.
2. As the aircraft accelerates, nose will want to pitch back up — maintain forward pressure.
3. Collective may need to increase slightly to maintain altitude (drag increases at higher speed).
4. **Trim** for the new airspeed.
5. Pedal adjustment for the new power setting.

#### Deceleration (e.g., 100 → 60 KIAS)

1. Apply aft cyclic (nose up) → airspeed decreases.
2. As the aircraft decelerates, power required changes (follows the bucket curve — initially decreases, then increases as you approach hover).
3. Collective must increase as airspeed decreases below ~80 KIAS to maintain altitude.
4. **Trim** for the new airspeed.
5. Pedal adjustment for the new power setting.
6. **If decelerating below ETL:** Significant collective increase required; full hover control technique applies.

---

### 5.7 Straight-and-Level Flight at Various Airspeeds

The student must be able to maintain straight-and-level flight at 40, 60, 80, and 100 KIAS, demonstrating understanding of how control feel and power requirements change across the airspeed range.

| Airspeed | Attitude (Nose) | Power (Torque) | Control Feel | Stability |
|---|---|---|---|---|
| **40 KIAS** | Nose up ~5–8° | High (~55–65%) | Sensitive; sluggish yaw response | Low — near ETL boundary; requires active control |
| **60 KIAS** | Nose level to slight up | Moderate (~45–55%) | Responsive; balanced | Moderate — in translational lift; reasonable stability |
| **80 KIAS** | Slight nose down | Low-moderate (~40–50%) | Firm; good feedback | Good — efficient regime; most stable |
| **100 KIAS** | Nose down ~3–5° | Moderate (~45–55%) | Firm; higher control forces | Good — approaching Vne; parasite drag increasing |

---

### Instructor Notes — Module 5

| Common Student Error | Correction |
|---|---|
| Not trimming after speed changes | Every speed change = re-trim. The student should develop the habit of releasing and resetting force trim as a reflexive action after any power or speed adjustment. |
| Losing altitude in turns | Brief: "Turns require more lift. As you bank, add collective to maintain altitude. The steeper the bank, the more collective." |
| Abrupt collective reduction in descent | The collective controls Nr when you reduce power. Abrupt reduction = Nr overshoot. "Move the collective like you're adjusting a volume knob." |
| Delayed autorotation entry | The single most dangerous error. Drill: "Engine fails → collective DOWN. No thinking. No diagnosis first. Collective DOWN, then figure out what happened." |
| Fear of autorotation practice | Normalize it: "We're going to practice this at altitude with plenty of room. I'll recover if needed. Your job is to get the collective down fast and find 60 knots." |
| Over-controlling at low airspeed | Below ETL, the aircraft is more responsive and less stable. Students from cruise-speed practice over-control when slow. "Smaller inputs. Let the aircraft settle." |
| Not monitoring Nr during autorotation | Nr is the student's life in autorotation. If it decays below 90%, the rotor will not produce enough lift for a safe flare and landing. Drill the Nr scan into the autorotation procedure. |

---

## Module 6: Navigation (Basic AHRS/GPS)

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Select and navigate to a pre-programmed waypoint using the MFD NAV page.
2. Read and interpret bearing, distance, ground speed, and ETA to the active waypoint.
3. Create or modify a waypoint using the AHRS/GPS controller or MFD interface (enter coordinates in Lat/Long or MGRS format).
4. Orient the MFD moving map (north-up vs. track-up) and maintain situational awareness of own-ship position.
5. Set and use the heading bug on the heading indicator / HSI for course tracking.
6. Set the radar altimeter low-altitude warning bug and explain its use during low-level navigation.
7. Use TACAN (if modeled in DCS) for bearing and distance to a ground station.

---

### 6.1 AHRS/GPS Navigation System Overview

The OH-58D uses an AHRS (Attitude Heading Reference System) integrated with a GPS receiver to provide the primary navigation solution. This system feeds data to the MFD, which displays the navigation information to the pilot.

| Component | Function | Location |
|---|---|---|
| **AHRS** | Provides attitude (pitch, roll) and magnetic heading reference | Internal avionics bay (no pilot interaction except alignment) |
| **GPS Receiver** | Provides latitude/longitude position, ground speed, ground track | Internal avionics bay |
| **AHRS/GPS Controller** | Pilot input device: waypoint entry, mode selection, alignment commands | Right console |
| **MFD NAV Page** | Primary navigation display: map, waypoints, route, bearing/distance | Center instrument panel |
| **Heading Indicator / HSI** | Analog heading display with heading bug and course pointer | Instrument panel — right |
| **Magnetic Compass** | Standby heading reference | Windshield frame |

---

### 6.2 Waypoint Navigation

#### Selecting a Waypoint

1. On the MFD, navigate to the **NAV page** (press the NAV OSB).
2. The NAV page displays:
   - Own-ship position symbol (centered or offset on the moving map).
   - Waypoints (numbered triangles or symbols on the map).
   - Active waypoint (highlighted or connected by a course line).
3. To **select a different waypoint as active**: use the OSB buttons to cycle through waypoints, or use the AHRS/GPS controller to enter the desired waypoint number.

#### Navigation Data Display

| Data | Display Location | How to Read |
|---|---|---|
| **Bearing to Waypoint (BRG)** | MFD NAV page — data block | Magnetic bearing in degrees (e.g., 270°) |
| **Distance to Waypoint (DIST)** | MFD NAV page — data block | Nautical miles (e.g., 12.4 NM) |
| **Ground Speed (GS)** | MFD NAV page — data block | Knots (e.g., 85 kts) |
| **Estimated Time of Arrival (ETA)** | MFD NAV page — data block | Time or minutes to waypoint |
| **Ground Track** | MFD NAV page — own-ship symbol direction | Direction of travel over the ground |
| **Current Position** | MFD NAV page — data block or cursor | Lat/Long or MGRS coordinates |

#### Course Tracking Technique

1. Note the bearing to the active waypoint (e.g., 270°).
2. Set the heading bug on the heading indicator to the bearing (270°).
3. Turn to the heading and maintain it.
4. Periodically check the MFD NAV page — if the bearing changes (e.g., now 275°), adjust heading to re-intercept the course.
5. Wind correction: if the aircraft drifts off course, apply a wind correction angle (crab into the wind) to maintain a straight ground track to the waypoint.

> *⚠ Realism Divergence: The real OH-58D EGI system provides HSI course deviation indication (CDI) similar to a VOR needle. The DCS module may or may not implement a full CDI display. The student should use the MFD NAV page bearing/distance readout and heading indicator as the primary course-tracking method.*

---

### 6.3 Waypoint Entry / Modification

**Creating a New Waypoint:**

| Step | Action | Notes |
|---|---|---|
| 1 | Access the waypoint entry page on the AHRS/GPS controller or MFD | Typically through OSB on MFD NAV page → WPT EDIT |
| 2 | Select an empty waypoint number (e.g., WPT 10) | Overwriting a pre-programmed waypoint is possible |
| 3 | Enter coordinates in **Lat/Long** (e.g., N 42°15'30" E 043°30'00") or **MGRS** (e.g., 38T LP 1234 5678) | DCS may support one or both formats depending on module |
| 4 | Confirm entry (press ENTER / ENT OSB) | Waypoint is saved and appears on the moving map |
| 5 | Select the new waypoint as active (if desired) | Route sequence updates |

**Mark Point (Capture Current Position):**

| Step | Action | Notes |
|---|---|---|
| 1 | While in flight (or hover), press the **MARK** function on the MFD or AHRS/GPS controller | Captures current GPS position |
| 2 | The mark point is stored as a waypoint (next available number) | Useful for marking POIs, landing zones, or reference points |
| 3 | Note the waypoint number assigned | Can be navigated to later or shared with flight |

> *⚠ Realism Divergence: The real OH-58D uses the Control Display Unit (CDU) integrated with the IDM for detailed waypoint management, including importing waypoints from a mission data transfer device (MDTD) and sharing waypoints over the digital data link. DCS simplifies waypoint entry to manual keyboard input through the MFD/AHRS controller interface.*

---

### 6.4 MFD Moving Map

The MFD NAV page can display a moving map showing terrain, cultural features, and overlaid navigation data.

| Feature | Description |
|---|---|
| **Orientation** | North-up (map always oriented north) or Track-up (map rotates so direction of flight is always up) |
| **Range Scale** | Adjustable zoom level (e.g., 5 NM, 10 NM, 25 NM rings) |
| **Own-Ship Symbol** | Aircraft position and heading on the map |
| **Waypoints** | Displayed as numbered symbols on the map |
| **Route Line** | Connecting line between sequential waypoints (if a route is programmed) |
| **Range Rings** | Concentric circles at selected distances for situational awareness |

**Map Orientation Selection:**
- **North-Up:** Best for correlating with paper maps and maintaining geographic awareness. The own-ship symbol rotates as the aircraft turns.
- **Track-Up:** Best for intuitive situational awareness during flight. The map rotates so the direction of flight is always "up." This is the recommended setting for BQT-level navigation.

---

### 6.5 Heading Indicator / HSI

| Feature | Function |
|---|---|
| **Compass Card** | Rotating card showing magnetic heading; lubber line at top reads current heading |
| **Heading Bug** | Pilot-settable reference marker; set to desired heading or course to waypoint |
| **Course Pointer** | May display bearing to active waypoint (if HSI mode connected to AHRS/GPS) |
| **Heading Bug Set** | Rotary knob on the heading indicator bezel |

**DCS Usage:**
- The heading bug is set by rotating the knob on the heading indicator (mouse scroll in DCS).
- Use the heading bug as a visual aid for maintaining course to the next waypoint.
- Cross-check heading indicator with magnetic compass periodically (heading indicator may precess and require reset).

---

### 6.6 Radar Altimeter Usage for Navigation

While the radar altimeter's primary purpose is altitude awareness, it is also a critical tool during low-level navigation.

| Scenario | Bug Setting | Purpose |
|---|---|---|
| **Pattern Work** | 50 ft | Alerts pilot if descending below pattern altitude unintentionally |
| **Low-Level Navigation** | 100–200 ft | Terrain clearance warning during low-level flight |
| **Approach** | Decision height (e.g., 50 ft) | Alerts pilot at minimum altitude for go-around decision |
| **NOE / Terrain Flight** | 25–50 ft | Advanced — not BQT scope, but student should understand the concept |

---

### 6.7 Radio Navigation Aids

#### TACAN (If Modeled)

| Feature | Description |
|---|---|
| **TACAN** | Tactical Air Navigation — provides bearing (BRG) and distance (DME) to a ground TACAN station |
| **Channel Selection** | Set via avionics panel; channels 1–126, X or Y band |
| **Mode** | T/R (Transmit/Receive) for ground station; A/A for air-to-air TACAN (if modeled) |
| **Display** | Bearing on HSI course pointer; DME on MFD or dedicated DME display |

**Usage:**
- TACAN is useful for navigating to airfields or reference points when GPS is unavailable or as a cross-check.
- In DCS, TACAN stations are pre-placed on the map. The pilot selects the correct channel for the desired station.

#### ADF (If Modeled)

| Feature | Description |
|---|---|
| **ADF (Automatic Direction Finder)** | Provides relative bearing to an NDB (Non-Directional Beacon) |
| **Frequency Selection** | Set via avionics panel; frequency in kHz |
| **Display** | ADF needle on the heading indicator or RMI |

> *⚠ Realism Divergence: The real OH-58D is equipped with TACAN (AN/ARN-149) and ADF capabilities. The DCS module may implement TACAN at a basic level but may not fully model ADF. If TACAN is not modeled, the student relies entirely on AHRS/GPS for navigation. The core BQT navigation skills (waypoint selection, bearing/distance, map orientation) remain GPS-based and are not affected by the absence of TACAN/ADF.*

---

### 6.8 Scope Limitation

This module covers **basic "point A to point B" navigation**:
- Selecting and navigating to pre-programmed waypoints.
- Creating mark points and entering new waypoints.
- Reading navigation instruments (bearing, distance, ETA).
- Using the heading indicator and radar altimeter to support navigation.

**The following are OUT OF SCOPE for BQT:**
- Mission planning and route development.
- Tactical route planning (terrain masking, threat avoidance).
- Nap-of-the-earth (NOE) and contour navigation.
- Digital communication / IDM waypoint sharing.
- Multi-ship navigation and coordination.

---

### Instructor Notes — Module 6

| Common Student Error | Correction |
|---|---|
| Fixating on the MFD during navigation | "The MFD is a tool, not a window. Look outside 80% of the time, glance at the MFD 20%. Your job is to not hit anything while flying to the waypoint." |
| Not setting the heading bug | The heading bug is a quick, reliable cross-reference. Make it a standard procedure: new waypoint selected → check bearing → set heading bug → turn to heading. |
| Confusing bearing with heading | Bearing = direction TO the waypoint FROM you. Heading = direction your nose is pointing. They should be similar if you're on course, but wind may separate them. |
| Not cross-checking position | After long flights, cross-check MFD position against known landmarks (rivers, airfields, roads). GPS is reliable but not infallible. |
| Ignoring radar altimeter in cruise | The radar altimeter is always relevant. Even at pattern altitude, the bug should be set as a safety backup. |
| Not understanding map orientation | Demonstrate both north-up and track-up. North-up correlates with paper maps; track-up is more intuitive for flight. Let the student choose, but recommend track-up for BQT. |

---

## Module 7: Emergency Procedures (Academic)

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Recite from memory all boldface/immediate-action emergency procedures for the OH-58D.
2. Describe the engine failure procedure for both forward flight and hover/low-altitude conditions.
3. Explain the complete autorotation procedure from entry through touchdown.
4. Describe the recovery procedure for Loss of Tail Rotor Effectiveness (LTE).
5. Describe the conditions, recognition, and recovery for settling with power (vortex ring state).
6. Explain FADEC failure modes and the transition from auto to manual engine control.
7. Describe hydraulic system failure indications and the recommended approach/landing technique.
8. Describe electrical failure response and battery-only endurance limitations.
9. Identify transmission failure indications (chip lights, oil pressure/temperature) and state the appropriate pilot response.
10. Explain mast bumping and dynamic rollover prevention, recognition, and (where possible) recovery.
11. Identify which emergency scenarios DCS models vs. simplifies or omits.

---

### 7.1 Boldface / Immediate-Action Emergency Procedures

Boldface procedures are memorized verbatim and executed **immediately** without reference to a checklist. These procedures address time-critical emergencies where delay can be fatal.

#### ENGINE FAILURE — IN FLIGHT

| Step | Action | Notes |
|---|---|---|
| 1 | **COLLECTIVE — LOWER** (immediately) | Maintain Nr within 90–107% (autorotation range) |
| 2 | **PEDALS — ADJUST** | Compensate for loss of engine torque (right pedal as torque is now zero) |
| 3 | **CYCLIC — ADJUST** | Establish autorotation airspeed: 60 KIAS (min descent) or 80 KIAS (max glide) |
| 4 | **LANDING — ACCOMPLISH** | Select landing site, maneuver to it, flare, collective pull, touchdown |

**Time-Critical:** The collective must be lowered within **approximately 1–2 seconds** of engine failure to prevent Nr from decaying below 90%. Below 90% Nr, the rotor will not produce sufficient lift for a safe autorotation flare and landing.

---

#### ENGINE FAILURE — HOVER / LOW ALTITUDE (Below 500 ft AGL)

| Step | Action | Notes |
|---|---|---|
| 1 | **COLLECTIVE — MAINTAIN / INCREASE** (as needed) | At low altitude, the priority is to cushion the landing, not establish a glide |
| 2 | **PEDALS — ADJUST** | Maintain heading alignment with available landing area |
| 3 | **CYCLIC — LEVEL ATTITUDE** | Prevent excessive nose-down or bank angle close to the ground |
| 4 | **CUSHION LANDING** with remaining Nr | Pull collective just before touchdown to arrest descent rate |

**Low-Altitude Engine Failure:** Below ~500 ft AGL (altitude depends on speed), the pilot may not have enough altitude to establish a full autorotation glide. The response changes from "establish glide" to "cushion the impact with available rotor energy." At very low altitude (below 100 ft), the pilot trades Nr for lift — the rotor will slow, but the touchdown will be survivable.

---

#### ENGINE FIRE — IN FLIGHT

| Step | Action | Notes |
|---|---|---|
| 1 | **LAND IMMEDIATELY** | This is a "land now" emergency — any suitable area |
| 2 | **EMERGENCY SHUTDOWN — ACCOMPLISH** (once on ground) | Throttle OFF → Fuel Boost OFF → Battery OFF |

---

#### EMERGENCY SHUTDOWN

| Step | Action | Notes |
|---|---|---|
| 1 | **THROTTLE — OFF** | Engine fuel supply cut |
| 2 | **FUEL BOOST — OFF** | Prevent fuel pressure from feeding a fire |
| 3 | **BATTERY — OFF** | Remove all electrical power |
| 4 | **ROTOR BRAKE — APPLY** (as required) | Stop the rotor if conditions warrant (fire on the ground) |

---

#### FADEC FAILURE

| Step | Action | Notes |
|---|---|---|
| 1 | **FADEC caution light** — NOTE | Confirm FADEC failure indication |
| 2 | **COLLECTIVE — ADJUST** | If Nr overspeed: increase collective (load the rotor); if Nr underspeed: decrease collective (unload the rotor) |
| 3 | **THROTTLE — ADJUST** | Manually correlate throttle to maintain Nr at 100% ± 2% |
| 4 | **FADEC MODE SWITCH — CHECK** | Verify if in MANUAL mode; if switchable to AUTO and fault clears, attempt reselection |
| 5 | **LAND AS SOON AS PRACTICABLE** | Manual throttle operation is high workload; minimize flight time |

---

#### HYDRAULIC SYSTEM FAILURE

| Step | Action | Notes |
|---|---|---|
| 1 | **AIRSPEED — ADJUST** to 60–80 KIAS | Moderate airspeed reduces control forces |
| 2 | **HYDRAULIC SWITCH — OFF** (if uncommanded inputs or hardover) | Isolates the hydraulic system from the flight controls |
| 3 | **LAND AS SOON AS POSSIBLE** | Run-on landing at 40–60 KIAS recommended; avoid hover (extreme control forces) |

---

#### TAIL ROTOR FAILURE (Complete Loss of Thrust)

| Step | Action | Notes |
|---|---|---|
| 1 | **AUTOROTATION — ENTER** | The only way to control yaw without a tail rotor is to eliminate engine torque |
| 2 | **THROTTLE — IDLE** (or OFF prior to touchdown) | Zero torque = zero yaw tendency from the engine |
| 3 | **LANDING — ACCOMPLISH** | Run-on landing if possible (maintains directional control with airspeed); full autorotation to a clear area |

**Note:** Without the tail rotor, the aircraft will spin uncontrollably in powered flight. Autorotation eliminates the torque that causes the spin. The landing will be a full autorotation with potential for some yaw at touchdown.

---

### 7.2 Loss of Tail Rotor Effectiveness (LTE) — Expanded

LTE was introduced in Module 1. This section provides the expanded emergency response.

**Conditions (Review):**
- Low airspeed (hover or slow flight below ETL)
- Wind from critical azimuths (285°–315° left rear quartering; 120°–240° tail wind; 210°–330° tail rotor VRS)
- High power setting (high torque = high anti-torque demand)

**Recognition:**
- Uncommanded right yaw that does not respond to normal left pedal correction
- Yaw rate may increase despite full left pedal application
- Often occurs during hover turns, confined area hover, or crosswind hover

**Recovery Procedure (Boldface):**

| Step | Action | Rationale |
|---|---|---|
| 1 | **COLLECTIVE — REDUCE** | Reduces main rotor torque → reduces anti-torque demand → slows or stops the yaw |
| 2 | **CYCLIC — FORWARD** | Initiates forward acceleration to gain airspeed |
| 3 | **PEDALS — FULL LEFT** (as required) | Maximum available anti-torque input |
| 4 | **AIRSPEED — INCREASE** above ETL | Translational lift restores clean airflow to the tail rotor; effectiveness returns |

**Critical Teaching Point:** LTE is **not a mechanical failure** — the tail rotor is working, but the air it's operating in is disrupted. The fix is to change the aerodynamic environment by gaining airspeed or reducing the anti-torque demand (reducing power).

**Prevention:**
- Always hover into the wind when possible.
- Avoid hover or slow flight with wind from the left rear quarter (285°–315°).
- During hover pedal turns, be aware of the wind direction relative to your tail.
- Maintain situational awareness of wind direction and speed at all times.
- If landing in a confined area, plan the approach so that the wind is on the nose during the final deceleration to hover.

---

### 7.3 Settling with Power (Vortex Ring State) — Expanded

**Conditions (Review):**
- Airspeed below ETL (< ~16 knots)
- Rate of descent exceeding ~300 FPM
- Power applied (moderate to high — above 40–50% of available)

**Recognition:**
- High rate of descent that does not arrest with collective application
- Aircraft may feel "mushy" — controls respond but altitude continues to decrease
- Vibration and erratic attitude changes
- VSI shows increasing descent rate despite collective increase

**Recovery Procedure:**

| Step | Action | Rationale |
|---|---|---|
| 1 | **CYCLIC — FORWARD** (aggressively) | Break out of the vortex laterally by gaining airspeed |
| 2 | **COLLECTIVE — REDUCE** (slightly, if altitude permits) | Reduces downwash feeding the vortex |
| 3 | **AIRSPEED — INCREASE** through ETL | Translational lift breaks the vortex ring; normal powered flight resumes |

**Counterintuitive Aspect:** The natural instinct when descending is to pull more collective (more power). In vortex ring state, this **worsens** the condition because the increased downwash feeds the recirculating vortex. The correct response is to get **airspeed** first, which requires trading altitude for speed — hence the forward cyclic.

**Altitude Required for Recovery:** Approximately 200–500 ft of altitude may be lost during recovery. If at low altitude when vortex ring state develops, recovery may not be possible before ground contact.

**Prevention:**
- Never descend vertically at rates exceeding 300 FPM without significant forward airspeed.
- During approaches, maintain airspeed above ETL until the final deceleration to hover.
- If conducting a steep approach, monitor rate of descent and maintain airspeed.

---

### 7.4 Autorotation — Full Procedure

#### Phase 1: Entry (0–3 seconds)

| Action | Purpose |
|---|---|
| **COLLECTIVE — FULL DOWN** (immediately) | Reduce blade pitch; allow rotor to autorotate; preserve Nr |
| **PEDALS — ADJUST** (right pedal) | Compensate for loss of engine torque; maintain heading |
| **CYCLIC — ADJUST** for autorotation airspeed | 60 KIAS (min descent rate) or 80 KIAS (max glide distance) |

#### Phase 2: Glide (Majority of autorotation)

| Parameter | Value |
|---|---|
| **Airspeed** | 60–80 KIAS (student choice based on distance to landing area) |
| **Nr** | 90–107% (monitor continuously) |
| **Rate of Descent** | ~1,500–2,000 FPM |
| **Collective** | Near full down (may adjust slightly to manage Nr within limits) |
| **Heading** | Toward the selected landing area |
| **Turns** | Gentle banks only (< 30°); excessive bank increases descent rate and risks Nr decay |

**Landing Area Selection:**
- Pick the largest, flattest, most obstacle-free area within glide range.
- Glide ratio ~4:1 at 80 KIAS (e.g., from 1,000 ft AGL, can glide approximately 4,000 ft / ~0.66 NM).
- Into the wind is preferred (reduces ground speed at touchdown).

#### Phase 3: Flare (50–100 ft AGL)

| Action | Purpose |
|---|---|
| **CYCLIC — AFT** (nose up ~15–20°) | Decelerates the aircraft; trades airspeed for rotor energy (Nr increases) |
| **Nr will INCREASE** during flare | This is desired — you are "storing" energy in the rotor for the final collective pull |
| **Airspeed decreases** through the flare | From 60–80 to near 0 at touchdown |

#### Phase 4: Collective Pull / Cushion (Near the ground, ~10–15 ft AGL)

| Action | Purpose |
|---|---|
| **CYCLIC — LEVEL** (level the aircraft) | Prevent tail strike or excessive nose-up attitude at touchdown |
| **COLLECTIVE — PULL** (smooth, firm upward) | Uses the stored rotor energy to arrest the descent rate just before touchdown |
| **Nr will DECAY** rapidly during collective pull | This is expected — you are spending the stored energy; touchdown must occur before Nr decays completely |

#### Phase 5: Touchdown

| Action | Notes |
|---|---|
| Aircraft contacts ground at minimal forward speed and descent rate | Skids absorb the landing; aircraft should be level or slightly nose-up |
| **COLLECTIVE — FULL DOWN** after contact | Prevent dynamic rollover or tip-over from residual rotor thrust |
| **THROTTLE — OFF** | Secure the engine (if not already failed) |

#### Autorotation Decision Tree

| Altitude at Engine Failure | Recommended Profile |
|---|---|
| **Above 500 ft AGL, in forward flight** | Full autorotation — establish glide, select landing area, flare, cushion, land |
| **200–500 ft AGL, in forward flight** | Abbreviated autorotation — less time for site selection; focus on maintaining Nr and cushioning |
| **Below 200 ft AGL, in forward flight** | Minimal time — lower collective, maintain attitude, cushion with available Nr |
| **In a hover (3–5 ft)** | Cushion with collective — maintain level attitude, absorb the drop (skid-height hover has minimal energy to manage) |
| **In a hover (above 50 ft)** | Lower collective, establish autorotation, limited flare, cushion — very challenging; altitude-speed diagram "deadman's curve" applies |

> *⚠ Realism Divergence: DCS models autorotation aerodynamics, including Nr behavior during entry, glide, flare, and cushion. However, the physical sensation of sink rate, G-loading during flare, and the timing judgment for the collective pull are significantly harder to replicate without motion cues. Students should practice autorotation entries and power recoveries extensively before attempting full autorotations to the ground. The "feel" in DCS is adequate for procedural training but does not fully replicate the real experience.*

---

### 7.5 FADEC Failure — Expanded

**Failure Modes:**

| Mode | Indication | Nr Behavior | Pilot Action |
|---|---|---|---|
| **Auto → Manual Transfer** | FADEC caution light; possible Nr fluctuation during transfer | Nr may briefly overspeed or underspeed before pilot assumes throttle control | Immediately correlate throttle with collective; stabilize Nr at 100% |
| **Complete FADEC Loss** | FADEC caution light; no automatic fuel control | Nr is entirely pilot-controlled via throttle | Manual correlation: collective up = throttle up; collective down = throttle down |
| **Intermittent FADEC** | FADEC caution light flickers; Nr hunting (oscillating) | Nr surges and sags unpredictably | Attempt to reselect AUTO; if unstable, switch to MANUAL and land |

**Manual Throttle Correlation:**
In manual mode, the pilot must anticipate every collective change with a corresponding throttle change:
- **Collective UP** (more blade pitch, more drag on rotor) → **Throttle UP** (more fuel, more engine power) → Nr maintained
- **Collective DOWN** (less blade pitch, less drag) → **Throttle DOWN** (less fuel, less power) → Nr maintained
- If the pilot raises collective without adding throttle, Nr decays. If collective is lowered without reducing throttle, Nr overspeeds.

**This is the highest-workload emergency in the OH-58D.** The pilot is simultaneously flying, navigating to a landing site, managing engine power manually, and communicating. Minimize flight time — land as soon as practicable.

> *⚠ Realism Divergence: The real OH-58D FADEC can experience partial authority failures where some functions remain operative (e.g., TOT limiting works but Nr governing does not). DCS typically models a cleaner auto-to-manual transfer without the partial failure modes. The manual throttle correlation technique is identical in both.*

---

### 7.6 Hydraulic System Failure — Expanded

**Identification:**
- HYD caution light illuminates.
- Flight controls become **extremely heavy** — the pilot must physically force the cyclic, collective, and pedals.
- Possible uncommanded control inputs (hardover) if a servo fails to a fixed position.

**Flight Characteristics Without Hydraulics:**
- **Cyclic:** Requires two-handed input; very high forces, especially at low airspeed.
- **Collective:** Heavy but manageable with deliberate inputs.
- **Pedals:** Heavy; may require full leg pressure for yaw corrections.
- The aircraft is controllable but **not maneuverable** in the way the student expects. Precision hover is essentially impossible.

**Recommended Approach:**
1. Maintain airspeed at **60–80 KIAS** (control forces are most manageable in this range).
2. Plan a **run-on landing** (approach at 40–60 KIAS with forward speed at touchdown).
3. Do not attempt to hover — the control forces required for hover without hydraulics are extreme.
4. Use a **shallow approach angle** to minimize the power and control changes required.
5. Accept a running landing on a suitable surface (runway, taxiway, flat field).

> *⚠ Realism Divergence: DCS models increased control forces in hydraulic failure but may not fully replicate the physical difficulty. In the real OH-58D, hydraulic failure requires the pilot to brace against the seat and use both hands on the cyclic. The student should understand that real hydraulic failure is far more physically demanding than DCS depicts, and a hover landing is effectively impossible without hydraulic assist.*

---

### 7.7 Electrical Failure — Expanded

#### Generator Failure

| Step | Action | Notes |
|---|---|---|
| 1 | **GEN caution light** — NOTE | Confirm generator offline |
| 2 | **GEN RESET** — PRESS | Attempt to reset the generator |
| 3 | **GEN SWITCH** — verify ON | If generator resets, GEN light extinguishes; resume normal operations |
| 4 | If generator **does not reset**: **NON-ESSENTIAL BUS — OFF** | Shed non-essential loads to conserve battery |
| 5 | **LAND AS SOON AS PRACTICABLE** | Battery endurance ~30 minutes on essential bus |

#### Battery-Only Operations

| System | Status | Notes |
|---|---|---|
| **Essential Bus** | Powered | Critical instruments, caution panel, radios (limited) |
| **Non-Essential Bus** | OFF (shed) | MFD, MMS, weapons systems — all lost |
| **Inverter** | May be lost (depends on bus) | Attitude indicator and heading indicator may fail |
| **Navigation** | Degraded — GPS may be lost with non-essential bus | Rely on magnetic compass and visual navigation |
| **Endurance** | ~30 minutes | Depends on battery state of charge and electrical load |

**Priority:** Fly the aircraft, navigate to the nearest suitable landing area using visual references and the magnetic compass, and land before battery is exhausted.

---

### 7.8 Transmission Failure Indications

| Indication | Severity | Response |
|---|---|---|
| **CHIP light** (main transmission, tail rotor gearbox, or engine) | Serious — metallic particles in oil | **LAND AS SOON AS POSSIBLE**; minimize maneuvering; monitor torque and temperature |
| **XMSN OIL PRESS low** | Critical — potential gearbox seizure | **LAND AS SOON AS POSSIBLE**; reduce torque if feasible |
| **XMSN OIL TEMP high** | Serious — gearbox overheating | **LAND AS SOON AS POSSIBLE**; reduce torque; monitor for noise/vibration |
| **Noise / Vibration from transmission** | Critical — imminent failure possible | **LAND IMMEDIATELY**; prepare for potential autorotation if transmission seizes |

**Transmission Seizure:** If the main transmission seizes, the rotor stops. There is no recovery. The aircraft will not autorotate because the rotor is mechanically locked. This is immediately catastrophic. The chip lights and oil indications are early warnings designed to get the aircraft on the ground **before** seizure occurs.

---

### 7.9 Mast Bumping — Awareness

Covered in detail in Module 1 (Section 1.10). Key reminders:

- The OH-58D 4-blade soft-in-plane rotor is more resistant than a 2-blade teetering rotor, but not immune.
- Avoid low-G and negative-G flight (**G limits: +2.5 to −0.5**).
- Avoid abrupt cyclic inputs at low rotor loading.
- If mast contact occurs, the result is immediate and catastrophic — there is no recovery procedure.
- **Prevention is the only strategy.**

---

### 7.10 Dynamic Rollover — Awareness

Covered in detail in Module 1 (Section 1.10). Key reminders:

- Occurs when one skid is fixed and collective is applied, causing the helicopter to pivot over the fixed point.
- Critical rollover angle is approximately **5–15°** depending on rate.
- Beyond the critical angle, the rollover is self-sustaining regardless of control input.
- **Immediate action if rollover begins:** REDUCE COLLECTIVE (unload the pivot point).
- Prevention: apply collective smoothly; ensure both skids are clear; be aware during slope operations, crosswind hover, and after a hard landing where one skid may have penetrated soft ground.

---

### 7.11 DCS-Specific Emergency Notes

| Emergency | DCS Modeling Fidelity | Notes |
|---|---|---|
| **Engine Failure** | **Modeled** — engine can fail (triggered by damage or instructor-induced) | Autorotation dynamics are functional; Nr decay and recovery respond correctly |
| **FADEC Failure** | **Modeled** — FADEC can fail, requiring manual throttle | Transfer to manual mode is functional; Nr must be managed by pilot |
| **Hydraulic Failure** | **Partially Modeled** — increased control forces | May not fully replicate the extreme physical difficulty of the real aircraft |
| **Tail Rotor Failure** | **Modeled** — tail rotor can be damaged/destroyed | Aircraft enters uncontrolled yaw; autorotation is the correct response |
| **LTE** | **Modeled** — uncommanded yaw in critical wind azimuths | Recovery technique (reduce collective, forward cyclic, gain airspeed) works in DCS |
| **Settling with Power** | **Modeled** — vortex ring state aerodynamics present | Recovery technique (forward cyclic, reduce collective, gain airspeed) works in DCS |
| **Electrical Failure (Generator)** | **Modeled** — generator can fail | Battery-only operations functional; avionics shed |
| **Transmission Chip Light** | **Partially Modeled** — may appear with battle damage | Full progressive gearbox wear not modeled |
| **Mast Bumping** | **Limited Modeling** — may or may not cause rotor separation in DCS | Student should respect G limits regardless |
| **Ground Resonance** | **Limited Modeling** — may not be present in DCS | Student should know the procedure; it's a universal helicopter emergency |
| **Dynamic Rollover** | **Partially Modeled** — aircraft can roll over on slopes | Severity and onset angle may differ from real aircraft |
| **Engine Fire** | **Modeled** — fire can occur from battle damage | Fire detection and response may be simplified |

---

### Instructor Notes — Module 7

| Common Student Error | Correction |
|---|---|
| Hesitating on autorotation entry | "The collective goes down FIRST. Before you think. Before you diagnose. Down. You have 1–2 seconds before Nr decays below recovery." Drill this as a reflex. |
| Pulling collective in settling with power | "I know it feels wrong, but pulling collective in a vortex is like pouring gas on a fire. Push the cyclic forward. Get airspeed. Then climb out." |
| Applying right pedal during LTE (uncommanded right yaw) | "Left pedal — FULL if needed. And reduce collective. You're fighting torque, not the tail rotor. Reduce power, and the yaw stops." |
| Not memorizing boldface items | "These are not guidelines. They are the exact words you say and the exact actions you take, in order, from memory. There is no time to look them up." Test verbally at the start of every flight. |
| Over-relying on FADEC — not prepared for manual | "FADEC makes your life easy. FADEC failure makes your life very hard. Practice manual correlation: collective up, throttle up. Collective down, throttle down. It must be natural." |
| Attempting to hover with hydraulic failure | "You will not hover without hydraulics. Plan a run-on landing from the start. 60 knots, shallow approach, accept the run." |
| Not understanding "land as soon as possible" vs. "land as soon as practicable" | "ASAP = land at the nearest suitable spot; don't fly past a good field looking for a runway. Practicable = get to an airfield if one is close, but don't extend the flight unnecessarily." |

---

## Module 8: Approach & Landing

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Fly a standard VFR helicopter traffic pattern (downwind, base, final) at the appropriate altitude and airspeeds.
2. Execute a normal decelerating approach from 60–80 KIAS to a hover over the intended landing point.
3. Execute a steep approach appropriate for obstacle-rich or confined environments.
4. Execute a shallow approach / running landing when power margins are limited.
5. Transition from a stable hover to ground contact with controlled collective reduction.
6. Execute a go-around / wave-off from any point during the approach.
7. Apply crosswind correction techniques during approach and landing, with awareness of LTE risk.
8. Describe slope landing technique and limitations (10° side slope, 5° nose-down).
9. Describe confined area approach considerations (power check, approach angle, escape route).

---

### 8.1 VFR Helicopter Traffic Pattern

Helicopter traffic patterns differ from fixed-wing patterns. Helicopters typically fly a tighter, lower pattern and the approach terminates in a hover rather than a runway touchdown.

#### Pattern Geometry

| Leg | Altitude (AGL) | Airspeed (KIAS) | Notes |
|---|---|---|---|
| **Upwind / Departure** | Climbing from hover to pattern altitude | 55–60 (Vy) → accelerate | After takeoff, climb on runway heading |
| **Crosswind Turn** | ~300–500 ft AGL | 60–80 | Turn 90° from departure heading |
| **Downwind** | 500 ft AGL (standard) | 80 | Parallel to landing direction, offset ~500–800 ft |
| **Base Turn** | Begin descent on base | 70 → decelerating | Turn 90° toward landing area; begin descent |
| **Final Approach** | Descending from ~300 ft to hover | 60 → decelerating to hover | Align with landing point; progressive deceleration |

**Pattern Entry:**
- From the traffic area: enter the downwind at pattern altitude (500 ft AGL) and pattern airspeed (80 KIAS).
- From a departure: climb to pattern altitude, crosswind turn, then downwind.
- Adjust pattern for wind: keep turns into the wind when possible.

**Communications:**
- Downwind: "[Callsign], downwind, [runway/landing area], [type approach]."
- Base: "[Callsign], base."
- Final: "[Callsign], final."

> *⚠ Realism Divergence: Helicopter traffic patterns at Army airfields follow AR 95-1 and local ATSOP (Air Traffic Standing Operating Procedures), which may specify different altitudes and geometries than civilian or USAF patterns. DCS airfields may not have specific helicopter traffic patterns defined — the student should use 500 ft AGL and the standard geometry as a default, adjusting for the specific training scenario.*

---

### 8.2 Normal Approach (Decelerating Approach to Hover)

The normal approach is the standard technique for transitioning from forward flight to a hover over the intended landing point. It is a **constant angle, decelerating** approach.

#### Procedure

| Phase | Altitude (AGL) | Airspeed (KIAS) | Power (Torque) | Actions |
|---|---|---|---|---|
| **Initial Approach** | 300–500 ft | 60–80 | Cruise power | Align with landing point; set approach angle (~8–10°) |
| **Mid Approach** | 200–300 ft | 50–60 | Reducing | Progressive aft cyclic to decelerate; lower collective as airspeed decreases; maintain approach angle |
| **Short Final** | 100–200 ft | 30–50 | Increasing (ETL fading) | Power increases as translational lift diminishes; pedal adjustments for torque changes |
| **Transition to Hover** | 50–100 ft | 10–30 | Hover power approaching | Through ETL — expect transverse flow vibration, yaw left, pitch up |
| **Hover** | 3–5 ft | 0 | Hover power | Stabilize over the intended landing point; verify position and altitude |

#### Approach Angle Reference

A normal approach uses approximately an **8–10° glide path** — shallower than a steep approach but steeper than a running landing. The pilot can visualize this by placing the landing point approximately **1/3 up from the bottom of the windshield** and maintaining that visual angle throughout the approach.

#### Key Technique Points

1. **Collective and airspeed are coupled during the approach:** As you decelerate (aft cyclic), the aircraft wants to climb. Reduce collective to maintain the approach angle. As airspeed decreases below ETL, the power required increases — add collective to prevent sinking.
2. **The ETL transition is the critical moment:** As the aircraft decelerates through 24–16 knots, translational lift diminishes. Power required jumps. The nose will pitch up. Vibration increases. The pilot must smoothly add collective and adjust cyclic/pedals.
3. **Visual references are primary:** The pilot should aim for the landing point using the windshield and peripheral references, cross-checking instruments (airspeed, radar altimeter, torque) periodically.

> *⚠ Realism Divergence: The visual cues and approach angle perception in DCS depend on monitor setup, FOV settings, and VR headset (if used). The approach technique is identical, but students may struggle with depth perception and altitude judgment in DCS. Encourage use of the radar altimeter as a cross-check during approach.*

---

### 8.3 Steep Approach

Used when obstacles (trees, buildings, wires) surround the landing area and a shallower approach angle would not clear them.

#### Procedure

| Phase | Description | Notes |
|---|---|---|
| **Entry** | Align with landing point at 60 KIAS, approximately 300–500 ft AGL | Steeper than normal — approach angle ~15–20° |
| **Deceleration** | Aft cyclic and collective reduction — faster deceleration rate than normal | The aircraft descends more steeply; rate of descent is higher |
| **Power Management** | Power increases significantly during deceleration (translational lift fading faster due to steeper angle) | Watch for torque limits; settling with power risk increases |
| **Transition to Hover** | Arrive at hover altitude over the landing point | May need high power to arrest descent; careful collective management |

**Hazards:**
- **Settling with power:** The steep approach combines low airspeed and high rate of descent — exactly the conditions for vortex ring state. Maintain airspeed above ETL as long as possible and avoid descent rates exceeding 300 FPM at airspeeds below ETL.
- **Over-torque:** The power demand during a steep approach can exceed normal limits. Monitor torque.
- **Visual illusion:** The steep approach angle can create the illusion of a faster-than-normal closure rate with the ground.

---

### 8.4 Shallow Approach / Running Landing

Used when **power margins are limited** (high gross weight, high density altitude, hot day) and the aircraft cannot sustain a hover at the current conditions. The aircraft lands with forward speed and slides to a stop on the skids.

#### Procedure

| Phase | Description | Notes |
|---|---|---|
| **Entry** | Align with landing area at 60 KIAS, ~300 ft AGL | Approach angle ~3–5° (very shallow) |
| **Deceleration** | Gentle deceleration — maintain airspeed higher than normal approach | Keep ETL until near the ground |
| **Touchdown** | Contact the ground with **forward speed** (~20–30 KIAS) and a slight nose-up attitude | The aircraft will slide forward on the skids |
| **Slide** | Skids slide on the surface; aircraft decelerates due to friction | Reduce collective progressively; do not slam collective down (may cause nose-down pitch) |
| **Stop** | Aircraft comes to rest; verify stable | Ensure both skids are evenly on the ground before fully lowering collective |

**Surface Requirements:**
- Flat, smooth, hard surface (runway, taxiway, or firm flat ground).
- Debris-free — the skids will slide and kick up anything on the surface.
- Adequate length to decelerate (~100–200 ft of clear area beyond touchdown point).

> *⚠ Realism Divergence: Running landings in DCS depend on the ground handling model and skid friction. The DCS module may handle running landings differently than the real aircraft — the student should practice on a known flat surface (runway) before attempting on unprepared terrain.*

---

### 8.5 Hover to Landing (Touchdown from Hover)

Once stabilized in a hover over the landing point, the final step is to place the aircraft on the ground.

**Procedure:**
1. From a stable hover at 3–5 ft skid height.
2. Verify position is correct over the intended landing point.
3. **Smoothly and progressively lower the collective** — the aircraft will descend.
4. As the skids approach the ground, continue reducing collective.
5. **Touchdown:** Feel the skids contact the ground.
6. **After contact:** Verify the aircraft is stable (not on a slope, not rocking). Continue reducing collective to flat pitch.
7. If the aircraft rocks or one skid is not firmly on the ground — **increase collective** to return to hover and reposition.

**Hazard — Dynamic Rollover on Landing:**
If one skid contacts the ground before the other (slope, uneven surface, crosswind), the aircraft can pivot around that skid. Reduce collective smoothly and ensure both skids make contact simultaneously when possible.

---

### 8.6 Go-Around / Wave-Off

A go-around is initiated at any point during the approach when the pilot determines the approach is unstable, the landing area is unsuitable, or safety of flight is compromised.

**Decision Criteria:**
- Approach is too fast, too slow, too steep, or too shallow to correct safely.
- Landing area obstruction discovered (vehicle, personnel, debris).
- Crosswind or tailwind exceeds comfort level.
- Rate of descent is excessive and not arresting with normal correction.
- Power demand approaching limits with insufficient margin.
- Any uncertainty about the safety of the landing.

**Procedure:**

| Step | Action | Notes |
|---|---|---|
| 1 | **COLLECTIVE — INCREASE** (smoothly but assertively) | Apply power to arrest descent and begin climbing |
| 2 | **CYCLIC — FORWARD** | Lower the nose to accelerate; gain airspeed to Vy (55–60 KIAS) |
| 3 | **PEDALS — ADJUST** | Left pedal to compensate for increased torque |
| 4 | **CLIMB** to pattern altitude | Re-enter the pattern for another approach |

**Key Point:** The go-around decision must be made **early**. Attempting to salvage an unstable approach at low altitude and low airspeed consumes power, altitude, and options. The earlier the go-around is initiated, the more margin is available.

> *⚠ Realism Divergence: Go-arounds in DCS are procedurally identical to the real aircraft. The timing and judgment are the same. The student should develop the habit of executing a go-around proactively rather than waiting until the situation deteriorates.*

---

### 8.7 Crosswind Approach and Landing

**Effects of Crosswind on Approach:**
- The aircraft drifts in the direction of the wind; the pilot must crab (point the nose into the wind) or apply a sideslip (wing-low) correction to maintain ground track to the landing point.
- On short final, as the aircraft decelerates through ETL, the crosswind effect becomes more pronounced because the tail rotor is working harder (more power = more torque = more anti-torque demand).
- **LTE awareness:** If the crosswind comes from the left rear quadrant (relative to the aircraft on final), LTE risk increases during the hover phase.

**Technique:**
1. During the approach, crab into the wind to maintain ground track.
2. On short final (~100 ft and below), transition from crab to a **sideslip** (use pedals to align the nose with the landing direction, use cyclic to correct for drift).
3. In the hover, position the aircraft directly over the landing point and use pedal to maintain heading aligned with the wind or as desired.
4. Touch down with the upwind skid slightly first if on a slope, or simultaneously on flat ground.

**Crosswind Limits:**

| Condition | Maximum Crosswind |
|---|---|
| **General Hover / Sideward Flight** | 35 knots |
| **Practical Comfort for BQT Students** | 15–20 knots | Students should build crosswind experience progressively |

---

### 8.8 Slope Landing

**Technique:**
1. Approach the slope from the downhill side when possible (allows escape route if power is insufficient).
2. Hover over the intended landing point.
3. Slowly lower the collective to descend toward the slope.
4. **Uphill skid contacts first** (for a side slope) — maintain collective pressure to keep the aircraft light on the uphill skid.
5. Slowly continue lowering collective to place the downhill skid on the ground.
6. Once both skids are on the ground and the aircraft is stable, lower collective to flat pitch.

**Hazards:**
- **Dynamic rollover:** If the uphill skid is fixed and the pilot continues to apply collective, the aircraft will roll over the uphill skid toward the downhill side. **If rollover begins, immediately reduce collective.**
- **Slope exceeds limits:** If the cyclic reaches the stop (full deflection) before the downhill skid contacts the ground, the slope exceeds the aircraft's capability. Lift off and select a new landing site.

**Slope Limits:**

| Slope Direction | Maximum Angle |
|---|---|
| **Side Slope / Nose-Up** | 10° |
| **Nose-Down** | 5° |

**Slope Departure:**
1. Increase collective to become light on the skids.
2. Lift the downhill skid first (cyclic toward the uphill side).
3. Once both skids are clear, establish a level hover.
4. Depart normally.

---

### 8.9 Confined Area Operations

**Definition:** A confined area is a landing zone surrounded by obstacles (trees, buildings, terrain) that restrict the approach and departure path. Confined area operations require careful planning and execution.

**Planning Considerations:**

| Factor | Consideration |
|---|---|
| **Wind** | Determine wind direction and speed; plan approach into the wind |
| **Obstacles** | Identify highest obstacles on the approach and departure paths; ensure obstacle clearance |
| **Power Required** | Will the aircraft need to hover OGE to clear obstacles? Verify power margin |
| **Escape Route** | Identify an escape route (direction to fly if a go-around is needed) before beginning the approach |
| **Surface** | Assess landing surface (slope, softness, debris, water) |
| **Sun/Shadows** | Determine if the approach will be into the sun (visibility concerns) |

**Procedure:**
1. **Reconnaissance orbit:** Fly over or around the confined area at a safe altitude to assess wind, obstacles, surface, and plan the approach path.
2. **Power check:** Before descending into the confined area, verify that the aircraft has adequate power for an OGE hover and go-around.
3. **Approach:** Fly the planned approach path, clearing all obstacles by a safe margin.
4. **Landing:** Terminate in a hover over the landing point, verify position, and descend to the ground.
5. **Departure plan:** Before shutting down (if applicable), mentally rehearse the departure path and escape route.

> *⚠ Realism Divergence: Confined area operations in DCS are limited by the map's terrain and object modeling. Some obstacles may not be physically modeled (trees may be penetrable, wires may not exist). The student should treat all visible obstacles as real and practice proper confined area procedures regardless of whether DCS enforces them.*

---

### 8.10 DCS-Specific Landing Notes

| Topic | DCS Behavior | Real Aircraft |
|---|---|---|
| **Autostart** | DCS provides an autostart function that completes the startup sequence automatically. For reference only — the student must learn manual start. Autostart may not properly configure all systems for flight. | N/A |
| **Skid-Ground Interaction** | DCS models skid contact and ground friction. The aircraft will slide on some surfaces and grip on others. Ground handling may feel different than the real aircraft, especially on slopes. | Real skids have specific friction coefficients and can dig into soft ground |
| **Ground Effect** | DCS models ground effect, but the boundary and intensity may differ from the real aircraft. The student should use the power check as the primary reference for performance capability. | Real ground effect is well-defined and consistent |
| **Approach Angle Judgment** | Depth perception in DCS (especially on 2D monitors) can make approach angle judgment difficult. Recommend using radar altimeter and VSI as cross-checks. | Real visual references (depth perception, peripheral vision) are available |

---

### Instructor Notes — Module 8

| Common Student Error | Correction |
|---|---|
| Approach too fast — overshooting the landing point | "Start decelerating earlier. Watch the landing point in the windshield — if it's moving down, you're going too fast. If it's moving up, you're going too slow." |
| Not adding power during ETL transition on approach | "As you slow through ETL, the aircraft sinks. If you don't add collective, you'll hit the ground before you're ready. Anticipate the power increase." |
| Go-around decision too late | "If in doubt — go around. Every approach you fly is a decision loop: 'Can I land from here?' If the answer is 'maybe,' the answer is 'go around.'" |
| Slamming collective down on touchdown | "Lower the collective smoothly. The aircraft is still a helicopter on the ground — abrupt inputs cause the fuselage to rock and the rotor disc to tilt. Smooth, all the way to flat pitch." |
| Ignoring crosswind effects on approach | "Wind doesn't stop because you're landing. As you slow down, the crosswind has more effect. Plan for it: where is the wind? How will it push you? When will LTE become a factor?" |
| Approaching a slope too aggressively | "Slope landings are slow and deliberate. Place the uphill skid first, then slowly lower to the downhill. If the cyclic hits the stop, the slope is too steep — go around." |
| Not doing a recon orbit for confined areas | "You never fly into a confined area blind. Orbit first: wind, obstacles, surface, escape route. Then approach." |

---

## Module 9: Shutdown

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Hover taxi the aircraft to a designated parking spot and set down safely.
2. Execute a complete shutdown from engine running to cold-and-dark using the proper switch-by-switch procedure.
3. State the correct throttle sequencing (FLY → IDLE → OFF) and the monitoring required during engine spool-down.
4. Identify the correct avionics and electrical power-down sequence.
5. Describe rotor brake usage (if applicable) during shutdown.

---

### 9.1 Post-Landing / Hover to Parking

After completing the last approach and landing, the aircraft must be repositioned to a designated parking spot.

| Step | Action | Notes |
|---|---|---|
| 1 | From the landing point, lift to a 3-ft hover | Standard hover pickup |
| 2 | Hover taxi to the designated parking spot | < 20 knots, < 3 ft skid height |
| 3 | Position the aircraft over the parking spot | Align with parking markings or ground crew signals |
| 4 | Slowly lower collective to set down | Ensure both skids contact the ground simultaneously |
| 5 | Once firmly on the ground, lower collective to **flat pitch** | Aircraft stable on skids; no tendency to rock or slide |
| 6 | Verify stable | Aircraft is not on a slope, skids are firmly planted |

---

### 9.2 Shutdown Procedure — Full Switch-by-Switch

#### Phase 1: Engine Cooldown and Throttle Sequencing

| Step | Switch / Action | Location | Expected Result |
|---|---|---|---|
| 1 | **Throttle — IDLE** (rotate from FLY to IDLE detent) | Collective grip — twist throttle | Nr decreases from 100% to ground idle (~62–65%); engine at ground idle; TOT decreases |
| 2 | Wait **2 minutes** at IDLE for engine cooldown | — | Allow TOT to stabilize and turbine to cool; prevents thermal shock to hot-section components |
| 3 | Monitor **TOT** during cooldown | Instrument panel — TOT gauge | TOT should decrease steadily; if TOT remains elevated, continue cooling |
| 4 | **Throttle — OFF** (rotate to cutoff) | Collective grip — twist throttle past IDLE to OFF | Fuel supply cut; engine begins to spool down |
| 5 | Monitor **N1** decreasing | Instrument panel — N1 gauge | N1 should decrease smoothly to 0% |
| 6 | Monitor **Nr** decreasing | Instrument panel — Nr gauge | Rotor RPM decreases as engine spools down; rotor coasts to a stop |
| 7 | Monitor **TOT** decreasing | Instrument panel — TOT gauge | TOT should decrease to ambient; any TOT rise during spool-down could indicate a fuel leak |

**Engine Cooldown Time:**

| Condition | Recommended Cooldown | Rationale |
|---|---|---|
| **Normal (post-cruise)** | 2 minutes at IDLE | Standard thermal management |
| **Post-high-power (post-hover, post-climb)** | 3–5 minutes at IDLE | Hot-section temperatures are higher; more cooling needed |
| **Emergency shutdown** | No cooldown — throttle OFF immediately | Engine damage is accepted to address the emergency |

> *⚠ Realism Divergence: In the real OH-58D, the 2-minute cooldown at idle is a mandatory maintenance requirement to prevent thermal shock to the turbine blades and hot-section components. Skipping cooldown can cause thermal stress cracking. DCS does not model turbine thermal damage from shutdown without cooldown, but the student should develop the habit of performing the cooldown for procedural discipline.*

#### Phase 2: Avionics and Electrical Power-Down

| Step | Switch / Action | Location | Expected Result |
|---|---|---|---|
| 8 | **MMS — OFF** | Left console or overhead — MMS power | MMS sensor ball powers down |
| 9 | **Radios — OFF** | Right console — Radio panels | VHF/FM, UHF, transponder powered down |
| 10 | **AHRS/GPS — OFF** | Right console — AHRS/GPS controller | Navigation system powered down |
| 11 | **MFD — OFF** | Overhead console — Avionics section or MFD power switch | MFD display blanks |
| 12 | **Transponder — OFF** (if not already with radios) | Right console — Transponder panel | Transponder stops transmitting |

#### Phase 3: Electrical System Shutdown

| Step | Switch / Action | Location | Expected Result |
|---|---|---|---|
| 13 | **GENERATOR — OFF** | Overhead console — Electrical panel | Generator disconnected from bus; aircraft on battery power only |
| 14 | **INVERTER — OFF** | Overhead console — Electrical panel | AC bus de-energized; attitude indicator and heading indicator spin down |
| 15 | **FUEL BOOST PUMP — OFF** | Overhead console — Fuel panel | Fuel boost pump stops; FUEL BOOST caution light illuminates (expected) |
| 16 | **BATTERY — OFF** | Overhead console — Electrical panel | All electrical power removed; cockpit goes dark; caution lights extinguish |

#### Phase 4: Rotor Stop and Securing

| Step | Action | Notes |
|---|---|---|
| 17 | Monitor rotor coasting to a stop | Rotor will coast from 100% to 0% over 1–3 minutes depending on wind and blade condition |
| 18 | **ROTOR BRAKE — APPLY** (if equipped and desired) | Rotor brake slows rotor to stop more quickly; apply only below ~40% Nr to avoid damage |
| 19 | When rotor is fully stopped, verify all switches OFF | Final cockpit scan — all switches in the OFF position |
| 20 | Aircraft is **cold and dark** | Shutdown complete |

**Rotor Brake Usage:**

| Condition | Rotor Brake Action |
|---|---|
| **Normal Shutdown** | Optional — may apply below 40% Nr to expedite rotor stop |
| **High-Wind Shutdown** | Recommended — rotor can windmill in strong wind, maintaining rotation indefinitely |
| **Emergency** | Per emergency procedure (e.g., ground resonance: apply rotor brake with shutdown if Nr is too low to fly) |

> *⚠ Realism Divergence: The real OH-58D rotor brake must not be applied above approximately 40% Nr to avoid overheating the brake and damaging the brake disc. DCS may not enforce this restriction. The student should apply the rotor brake only after Nr has decayed significantly (below 40%).*

---

### 9.3 Complete Shutdown Summary (Quick Reference)

| # | Action | Location |
|---|---|---|
| 1 | Throttle → IDLE | Collective grip |
| 2 | Wait 2 min (cooldown) | — |
| 3 | Throttle → OFF | Collective grip |
| 4 | MMS → OFF | Left console / overhead |
| 5 | Radios → OFF | Right console |
| 6 | AHRS/GPS → OFF | Right console |
| 7 | MFD → OFF | Overhead / MFD switch |
| 8 | Generator → OFF | Overhead console |
| 9 | Inverter → OFF | Overhead console |
| 10 | Fuel Boost Pump → OFF | Overhead console |
| 11 | Battery → OFF | Overhead console |
| 12 | Rotor Brake → APPLY (below 40% Nr) | As equipped |
| 13 | Verify all switches OFF | Full cockpit scan |

---

### Instructor Notes — Module 9

| Common Student Error | Correction |
|---|---|
| Skipping the engine cooldown | "Two minutes at idle. Every time. The turbine is at 700°C+ after hover work. Slamming it to OFF is like dumping ice water on a hot pan — thermal shock cracks metal. Build the habit now." |
| Shutting off battery before generator | "Generator off before battery. If you shut battery off first with the generator still running, you can spike voltage on the bus and damage avionics. Generator → Inverter → Fuel Boost → Battery." |
| Not monitoring engine spool-down | "Watch N1 and TOT as the engine spools down. N1 should decrease smoothly. TOT should decrease. If TOT rises during spool-down, something is wrong (possible fuel leak into hot section). Call it out." |
| Applying rotor brake too early (high Nr) | "Rotor brake below 40% Nr only. Above that, you'll overheat the brake disc. Just let it coast." |
| Leaving avionics on during spool-down | "Avionics off before generator off. If you kill the generator with avionics still powered, they switch to battery and drain it unnecessarily. Clean sequence: avionics → generator → inverter → fuel boost → battery." |
| Not doing a final cockpit scan | "Before you walk away from the aircraft, every switch should be OFF. One missed switch (fuel boost left on, for example) can drain the battery overnight or create a hazard." |

---

## Appendix: Master Limitations Summary

| Parameter | Normal | Caution | Warning / Limit |
|---|---|---|---|
| **Nr (Power On)** | 98–100% | < 98% or > 100% | < 90% (critical low) / > 107% (overspeed) |
| **Nr (Power Off)** | 90–107% | — | < 90% / > 107% |
| **Torque (Q)** | ≤ 100% | 100–110% (10 sec transient) | > 110% |
| **TOT (Continuous)** | < 737°C | 737–810°C | > 810°C (transient) / > 843°C (start) |
| **N1 (Gas Producer)** | ≤ 100% | — | > 104% (overspeed) |
| **Oil Pressure** | 90–130 PSI | 60–90 PSI | < 60 PSI |
| **Oil Temperature** | 70–107°C | — | > 107°C |
| **Trans Oil Pressure** | 30–60 PSI | < 30 PSI | XMSN OIL PRESS caution |
| **Trans Oil Temperature** | < 110°C | 110–120°C | > 120°C |
| **Fuel Quantity** | > 83 lbs | — | ≤ 83 lbs (LOW FUEL caution) |
| **G-Limits** | +1.0 to +2.0 G | > +2.0 G | +2.5 G max / −0.5 G min |
| **Vne (Doors On)** | ≤ 120 KIAS | — | > 120 KIAS |
| **Vne (Doors Off)** | ≤ 110 KIAS | — | > 110 KIAS |
| **Max Gross Weight** | ≤ 5,500 lbs | — | > 5,500 lbs |
| **Slope (Side/Nose-Up)** | ≤ 10° | — | > 10° |
| **Slope (Nose-Down)** | ≤ 5° | — | > 5° |
| **Crosswind (Hover)** | ≤ 35 kts | > 20 kts (LTE awareness) | > 35 kts |

---

## Appendix: V-Speed Reference

| V-Speed | Value (KIAS) | Purpose |
|---|---|---|
| **Vy (Best Rate of Climb)** | 55–60 | Maximum altitude gain per unit time |
| **Vx (Best Angle of Climb)** | 45–50 | Maximum altitude gain per unit distance |
| **Cruise** | 80–100 | Normal cross-country speed; best range ~90–100 |
| **Vne (Doors On)** | 120 | Maximum airspeed — structural/retreating blade stall |
| **Vne (Doors Off)** | 110 | Reduced for increased drag |
| **Autorotation (Min RoD)** | 60 | Minimum rate of descent; best for close landing sites |
| **Autorotation (Max Glide)** | 80 | Maximum distance; best for distant landing sites |
| **ETL** | 16–24 | Effective Translational Lift — efficiency increases through this range |
| **Hover Taxi Max** | 20 | Maximum hover taxi speed |
| **Sideward / Rearward Max** | 35 | Structural limit for lateral and rearward flight |

---

*This research dossier is based on TM 1-1520-248-10 (Operator's Manual), TC 3-04.4 (Fundamentals of Flight), and DCS World Polychop Simulations OH-58D module documentation. For simulation training use only.*

