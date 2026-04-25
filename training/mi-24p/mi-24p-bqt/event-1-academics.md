# Event 1 — Aircraft Systems & Academics

> **Course:** Mi-24P Hind Basic Qualification Training | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [The Mi-24P Hind — Aircraft Overview](#the-mi-24p-hind--aircraft-overview)
3. [Powerplant — TV3-117V Turboshaft Engines](#powerplant--tv3-117v-turboshaft-engines)
4. [Rotor System & Transmission](#rotor-system--transmission)
5. [Fuel System](#fuel-system)
6. [Hydraulic System](#hydraulic-system)
7. [Electrical System & APU](#electrical-system--apu)
8. [Flight Controls & Autopilot](#flight-controls--autopilot)
9. [Stub Wing Aerodynamics](#stub-wing-aerodynamics)
10. [Rotary-Wing Aerodynamics](#rotary-wing-aerodynamics)
11. [Cockpit Orientation](#cockpit-orientation)
12. [Operating Limitations](#operating-limitations)
13. [Boldface Emergency Procedures](#boldface-emergency-procedures)
14. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Describe the TV3-117V turboshaft engine start cycle, governing modes, and all engine limitations (EGT, torque, Nr)
- [ ] Explain the 5-blade articulated main rotor system, VR-24 transmission, and Nr governing range
- [ ] Describe the dual hydraulic system, what each system powers, and flight characteristics on main vs. backup failure
- [ ] Explain the electrical system (dual generators, APU, batteries) and single/dual generator failure implications
- [ ] Describe the AI-9V APU — purpose, operating limits, and when it shuts down automatically
- [ ] Explain stub wing aerodynamic contribution at different airspeeds and its effect on autorotation
- [ ] Define and explain: ETL, LTE (loss of tail rotor effectiveness), ground resonance, settling with power, autorotation in a high-disk-loading aircraft
- [ ] Locate and identify all major cockpit panels and instruments in both the Pilot (rear) and WSO (front) cockpits
- [ ] Recite all critical operating limitations from memory (EGT, torque, Nr, VNE, G-limits, weight)
- [ ] Recite all boldface emergency procedures verbatim, in sequence, without reference to notes

---

## The Mi-24P Hind — Aircraft Overview

| Characteristic | Value |
|---|---|
| **Type** | Heavy attack / gunship helicopter with troop transport capability |
| **Manufacturer** | Mil Moscow Helicopter Plant |
| **Designation** | Mi-24P (NATO: Hind-F) |
| **Engines** | 2 × Klimov TV3-117V turboshaft (~2,200 SHP each) |
| **Main Rotor** | 5-blade, fully articulated; 17.3 m (56.75 ft) diameter |
| **Tail Rotor** | 3-blade, right-side **pusher** configuration |
| **Landing Gear** | Retractable tricycle — nosewheel steering, toe brakes |
| **Stub Wings** | Fixed wings, 4.5 m² area, ~12° negative incidence |
| **MTOW** | 11,500 kg (25,353 lbs) |
| **Crew** | 2 — Pilot (rear cockpit) + WSO (front cockpit) |
| **Fixed Armament** | GSh-30K twin-barrel 30 mm cannon (starboard fuselage, fixed) |
| **DCS Module** | Eagle Dynamics — native, full-fidelity |
| **Cockpit** | Dual-seat, all switches clickable in both cockpits |
| **Units** | Soviet metric — km/h, meters, °C, kg |

### The Six Key Character Traits

Understanding these traits early prevents the most common student errors:

| # | Trait | Implication |
|---|---|---|
| 1 | **Not a hover platform** | At 10,000+ kg, OGE hover may be impossible. Minimize hover time — the Hind wants to fly fast |
| 2 | **Stub wings change everything** | Wings contribute ~25% of total lift at cruise. At low speed, they add drag. Autorotation descent rate is much higher than light helicopters |
| 3 | **Twin engines = survivability** | Single-engine flight is possible. Engine failure ≠ autorotate immediately. Identify → secure → single-engine procedures |
| 4 | **Wheeled gear = ground resonance risk** | Articulated rotor + tricycle gear = dangerous resonance on the ground. The fastest ground emergency in aviation |
| 5 | **Two-crew aircraft** | Even in DCS single-player, the student must understand both cockpit roles |
| 6 | **Fixed cannon = pilot aims the aircraft** | The GSh-30K is bolted to the starboard fuselage. The pilot is the gun platform |

---

## Powerplant — TV3-117V Turboshaft Engines

The Mi-24P is powered by two Klimov **TV3-117V** turboshaft engines. The design is a **free-turbine** arrangement: the gas generator section (compressor + combustor + gas producer turbine) is mechanically independent of the power turbine, which drives the transmission through the VR-24 gearbox.

Both engines share a common combining gearbox that drives the single main rotor shaft. If one engine fails, the other continues to power both the rotor and the tail rotor.

### Engine Operating Limits

| Parameter | Normal | Continuous Max | Transient Max | Start Limit |
|---|---|---|---|---|
| **EGT (Exhaust Gas Temp)** | 700–750°C | 800°C | 900°C (limited duration) | 900°C |
| **Torque (% per engine)** | 70–80% | 85% | 95% (5 sec, emergency) | — |
| **Nr (Rotor RPM)** | 95% | 92–98% | — | — |
| **Oil Pressure** | Normal range per indicator | — | — | < min = abort |
| **Oil Temperature** | Per indicator | — | — | > max = reduce power |

### Start Abort Criteria

| Condition | Indication | Action |
|---|---|---|
| **Hot Start** | EGT exceeds 900°C and continues rising | Fuel cutoff lever OFF immediately |
| **Hung Start** | EGT rising, RPM not increasing | Fuel cutoff lever OFF; investigate |
| **No Light-Off** | No EGT rise within 30 sec of fuel introduction | Fuel cutoff lever OFF |
| **Oil Pressure** | No oil pressure within 30 sec of engine start | Fuel cutoff lever OFF; maintenance |

### Engine Governing

The TV3-117V uses a **hydromechanical fuel control** with constant-speed governing to maintain Nr at 95%. When power demand increases (collective up), the fuel control increases fuel flow to maintain rotor speed. Each engine is governed independently; the transmission handles power sharing automatically.

> *⚠ Realism Divergence: DCS simplifies engine governor modeling. Real TV3-117V transients (Nr droop during rapid collective pulls, fuel control lag) are approximated. The student should practice smooth, gradual collective inputs rather than rapid pulls.*

---

## Rotor System & Transmission

### Main Rotor

| Parameter | Value |
|---|---|
| **Blade count** | 5 |
| **Rotor type** | Fully articulated (lead-lag, flap, feather hinges on each blade) |
| **Diameter** | 17.3 m (56.75 ft) |
| **Rotation** | Counter-clockwise when viewed from above |
| **Normal Nr** | 95% |
| **Operating range** | 92–98% |
| **Autorotation range** | 89–105% |

The fully articulated system allows each blade to move independently — this provides excellent load distribution across the disc but also creates the **ground resonance** risk when the articulation coupling frequency matches the aircraft's ground resonance frequency.

### VR-24 Combining Gearbox

The VR-24 gearbox receives power from both engines and drives the main rotor shaft and the tail rotor driveshaft. It contains the rotor brake mechanism.

- **Rotor brake:** Applied after engine shutdown when Nr < 50% to stop the rotor
- **Gearbox oil temp/pressure** must be monitored — gearbox failure = immediate emergency

### Tail Rotor

| Parameter | Value |
|---|---|
| **Blade count** | 3 |
| **Configuration** | Right-side **pusher** — pushes tail LEFT, nose RIGHT |
| **Anti-torque** | Left pedal applies pitch to increase thrust (counteract torque) |
| **Torque compensation** | During power-on, left pedal is required to maintain heading |

**Critical Note:** The Mi-24P tail rotor is on the **right side** and is a **pusher** type. This is opposite to most American helicopters (left-side, puller). Right pedal is "less anti-torque." At high power settings, significant left pedal is required.

---

## Fuel System

| Parameter | Value |
|---|---|
| **Internal capacity** | ~1,500 kg (~2,000 L) |
| **Tank arrangement** | Multiple internal tanks (fuselage) |
| **External tanks** | Optional — up to 4 × ~500 L PTB-450 tanks on wing pylons |
| **Feed system** | Fuel boost pumps in each tank; gravity transfer between tanks |
| **Fuel type** | TS-1 or RT jet fuel (NATO equivalent: Jet-A / JP-8) |
| **Fuel indicators** | Fuel gauges in both cockpits; low-fuel warning lights |

**Minimum fuel (bingo):** ~300 kg — land immediately at the nearest suitable airfield.

---

## Hydraulic System

The Mi-24P has **two independent hydraulic systems**: main and backup.

| System | Powers | Failure Consequence |
|---|---|---|
| **Main hydraulic** | Flight controls (primary), landing gear, rotor brake | Heavy control forces; manageable |
| **Backup hydraulic** | Flight controls (backup path) | Very heavy forces; still flyable |
| **Dual failure** | — | Extremely heavy forces; emergency landing required immediately |

### Hydraulic Failure Flight Characteristics

- **Main hydraulic failure:** Controls become noticeably heavier. Autopilot OFF (requires hydraulics). Fly deliberately; avoid large inputs.
- **Backup hydraulic failure:** Controls very heavy. Two-hand inputs may be required. Land ASAP.
- **Dual failure:** Controls extremely heavy or immovable depending on speed/altitude. Controlled crash landing.

> *⚠ Realism Divergence: DCS models hydraulic failure with increased control forces. Full dual-hydraulic-failure control immovability may be simplified in the DCS implementation.*

---

## Electrical System & APU

### Generators

| Component | Output | Purpose |
|---|---|---|
| **Left engine generator** | DC, 28V | Primary electrical bus |
| **Right engine generator** | DC, 28V | Primary electrical bus (parallel) |
| **Battery 1 & 2** | DC, 28V, ~20–30 min endurance | Emergency backup if both generators offline |
| **AI-9V APU** | Powers start sequence | Used for engine starting and ground power |

### AI-9V Auxiliary Power Unit (APU)

The AI-9V APU is a small turbine that provides power and bleed air for starting the main engines. It is **not** used in flight (it shuts down automatically after engine starts are complete and generators are online).

| APU Operating Limit | Value |
|---|---|
| **Max continuous run time** | ~10 minutes |
| **Automatic shutdown** | When main generators come online |
| **APU EGT limit** | Monitor during start |

> **DCS:** APU is started via the APU panel in the pilot's cockpit. It must be running before engine start can begin.

### Generator Failure

| Scenario | Result | Action |
|---|---|---|
| **Single generator failure** | Remaining generator supplies full aircraft | Reduce non-essential loads; monitor |
| **Dual generator failure** | Batteries supply power — ~20–30 min | Land immediately; battery bus only |
| **APU restart in flight** | Possible if batteries have charge | Emergency procedure only |

---

## Flight Controls & Autopilot

### Control System

The Mi-24P uses **irreversible hydraulic flight controls** — unlike mechanical-link helicopters, pilot inputs are transmitted hydraulically. The controls do not provide aerodynamic feedback (no "feel" from the airstream). The **force trim** (STU) system provides artificial centering force.

| Control | Function |
|---|---|
| **Collective** | Changes main rotor blade pitch to control altitude/power |
| **Cyclic** | Tilts rotor disc to control pitch and roll |
| **Pedals** | Changes tail rotor pitch for yaw (heading) control |
| **Force Trim (STU)** | Magnetic brake system that holds controls in position when released |

### Autopilot — SAU-V4 / VUAP-1

The Mi-24P autopilot has **4 channels** that can be engaged independently:

| Channel | Function | Disengage Condition |
|---|---|---|
| **Pitch** | Maintains pitch attitude | Pilot cyclic input (force trim break) |
| **Roll** | Maintains roll attitude | Pilot cyclic input (force trim break) |
| **Heading (Yaw)** | Maintains selected heading | Pedal input |
| **Altitude** | Maintains barometric altitude | Collective input |

**Autopilot limitations:**
- AP must be OFF for takeoff and landing
- Do not engage AP below 50 m AGL
- AP does not prevent exceedance of limits — pilot is still responsible
- Switching cockpit seats: engage AP before switching — aircraft needs to hold attitude

---

## Stub Wing Aerodynamics

The Mi-24P's stub wings are not "optional" — they are a fundamental part of the aircraft's aerodynamic design.

| Speed Range | Wing Contribution | Net Effect |
|---|---|---|
| **Hover — 50 km/h** | Minimal lift, significant drag | Wings hurt performance at low speed |
| **50–100 km/h** | Growing lift contribution | Transition zone — rotor and wings share load |
| **100–200 km/h** | Significant lift | Wings relieve rotor — cruise efficiency improves |
| **200–260 km/h** | ~25% of total lift | Hind is now part helicopter, part airplane |

**Autorotation implication:** The wings continue to generate lift at high speed, but in autorotation, the rotor is ungoverned. The higher disc loading and wing drag mean a **much steeper autorotation descent rate (15–20 m/s)** compared to 5–8 m/s for a light helicopter.

---

## Rotary-Wing Aerodynamics

### Effective Translational Lift (ETL)

As the helicopter accelerates through approximately **50 km/h**, the rotor begins operating in clean, undisturbed air rather than recirculated hover wash. Rotor efficiency increases dramatically — the aircraft "leaps into flight" with less power.

- **Indication:** Aircraft wants to climb and pitch up through ETL
- **Technique:** Apply slight forward cyclic and accept the power reduction naturally

### Loss of Tail Rotor Effectiveness (LTE)

The Mi-24P is most susceptible to LTE when:
- Wind is from the **right-front quadrant (270°–360° relative)**
- Speed is **below 80 km/h**
- Power is **high** (large left pedal input required)

**Recovery:** Apply right pedal (reduce anti-torque), lower nose, gain airspeed immediately.

### Ground Resonance

Ground resonance is the **most dangerous ground emergency** for the Mi-24P.

| What It Is | An unstable vibration coupling between the articulated rotor lead-lag motion and the aircraft's natural frequency on the landing gear |
|---|---|
| **When It Occurs** | Ground contact with rotor turning — takeoff, landing, hover taxi, engine runup |
| **Identification** | Increasing vibration, shaking of the aircraft that grows louder/stronger |
| **Time to Destruction** | 3–5 seconds if not corrected immediately |

**Emergency Decision:**
- **Nr ≥ 90% (can fly):** Fly away immediately — collective up, get airborne
- **Nr < 90% (cannot fly):** Shut down immediately — fuel cutoff, full collective down, evacuate

### Settling with Power (Vortex Ring State)

| Entry Conditions | Descent rate > 300 ft/min (1.5 m/s) + Low speed (< 80 km/h) + High power |
|---|---|
| **Indications** | Loss of collective effectiveness; aircraft continues to sink despite collective UP |
| **Recovery** | Lower collective momentarily + Forward cyclic to gain airspeed + Climb out |

**Note:** The Mi-24P's high gross weight and high disc loading make it **more susceptible** to settling with power than a light helicopter. Always maintain airspeed during descents.

---

## Cockpit Orientation

### Seat Convention (DCS)

| Key | Cockpit | Crew Role |
|---|---|---|
| `1` | **Front** | WSO (Weapons Systems Officer) — weapons, targeting, ATGM guidance |
| `2` | **Rear** | **Pilot** — flies the aircraft; default spawn position |

### Pilot Cockpit (Rear) — Major Areas

```
┌─────────────────────────────────────────────────────────┐
│                  OVERHEAD PANEL                         │
│    [Lights] [Electrical] [Fuel] [Hydraulics] [Misc]     │
├─────────────────────────────────────────────────────────┤
│ LEFT CONSOLE │      MAIN INSTRUMENT PANEL      │ RIGHT  │
│              │                                 │CONSOLE │
│ [Throttles]  │  [Airspeed] [Altimeter] [VSI]   │        │
│ [Fuel pumps] │  [Horizon]  [Turn/Slip] [RMI]   │[Radios]│
│ [Hydraulics] │  [HSI]      [Clock]    [EGT]    │[IFF]   │
│ [Intercom]   │  [Torque]   [Nr]       [OAT]    │[Nav]   │
│              │  [Radar Alt][Fuel gauges]        │        │
│              │  [Caution panel — left side]     │        │
├─────────────────────────────────────────────────────────┤
│ COLLECTIVE                                    CYCLIC     │
│ [Throttle] [Trim]                             [Trigger] │
└─────────────────────────────────────────────────────────┘
```

### Key Instruments — Pilot Cockpit

| Instrument | Units | Location |
|---|---|---|
| **ASI (Airspeed Indicator)** | km/h | Main panel, upper left |
| **Altimeter** | Meters | Main panel, upper right |
| **Radar Altimeter (A-037)** | Meters | Main panel |
| **VSI (Vertical Speed)** | m/s | Main panel |
| **Artificial Horizon** | Degrees | Main panel, center |
| **HSI (Horizontal Situation)** | Degrees | Main panel, lower center |
| **Nr (Rotor RPM)** | % | Main panel |
| **EGT (per engine)** | °C | Main panel, engine instruments |
| **Torque (per engine)** | % | Main panel, engine instruments |
| **Fuel gauges** | kg | Main panel, lower |

### WSO Cockpit (Front) — Major Areas

The front cockpit is the WSO's domain. The pilot should be familiar with the location of:
- **PKV-1 collimating sight** — targeting sight for weapons delivery
- **Weapons control panel** — weapons selection, arming, release
- **SPO-15 (Beryoza) RWR** — radar warning receiver display and controls
- **UV-26 countermeasures panel** — chaff/flare programming and dispensing
- **Navigation panel** — backup nav controls

---

## Operating Limitations

### Airspeed

| Limit | Speed | Condition |
|---|---|---|
| **VNE** | 300 km/h | Never exceed |
| **Max — gear down** | 250 km/h | Retract gear above this speed if airborne |
| **Autorotation** | 170 km/h | Best glide speed |

### Rotor / Engine

| Parameter | Limit |
|---|---|
| **Nr (normal)** | 92–98% (target: 95%) |
| **Nr (min transient)** | 89% |
| **EGT (continuous)** | 800°C |
| **EGT (start limit)** | 900°C |
| **Torque (continuous)** | 85% per engine |
| **Torque (transient, 5 sec)** | 95% per engine |

### Weight & Balance

| Limit | Value |
|---|---|
| **MTOW** | 11,500 kg |
| **Training weight** | ~10,000–10,500 kg |
| **Min fuel (bingo)** | ~300 kg |

### Crosswind / Environmental

| Limit | Value |
|---|---|
| **Max crosswind — takeoff/landing** | 12 m/s |
| **Max tailwind — takeoff/landing** | 5 m/s |
| **Max bank angle (training)** | 45° |
| **Max positive G** | +2.5 G |
| **Min G (avoid)** | −0.5 G |

---

## Boldface Emergency Procedures

These must be **memorized verbatim** and recited on demand without reference to notes. All are immediate-action memory items.

### Engine Failure In Flight (Single)

1. **COLLECTIVE** — MAINTAIN Nr (95%)
2. **OPERATIVE ENGINE** — INCREASE POWER (torque ≤ 95%)
3. **AIRSPEED** — 120–140 km/h (minimum single-engine speed)
4. **FAILED ENGINE** — IDENTIFY (EGT, torque, Nr indication)
5. **FAILED ENGINE FUEL CUTOFF LEVER** — OFF
6. **LAND AS SOON AS PRACTICABLE**

### Dual Engine Failure / Autorotation

1. **COLLECTIVE** — FULL DOWN (immediately)
2. **AIRSPEED** — 170 km/h
3. **Nr** — MONITOR (89–105% range)
4. **JETTISON STORES** — if time permits
5. **At 50–30 m AGL** — BEGIN FLARE (raise nose)
6. **At 5–8 m AGL** — LEVEL, COLLECTIVE PULL (cushion)
7. **GROUND CONTACT** — COLLECTIVE DOWN, cyclic neutral

### Engine Fire — Left or Right

1. **AFFECTED ENGINE FUEL CUTOFF LEVER** — OFF
2. **FIRE SUPPRESSION** — PRESS (affected engine button)
3. **If fire persists** — OTHER EXTINGUISHER BOTTLE to affected engine
4. **LAND IMMEDIATELY**

### Ground Resonance

**IF Nr ≥ 90% (aircraft can fly):**
1. **COLLECTIVE** — UP — FLY AWAY IMMEDIATELY

**IF Nr < 90% (aircraft cannot fly):**
1. **BOTH FUEL CUTOFFS** — OFF
2. **COLLECTIVE** — FULL DOWN
3. **EVACUATE**

### Tail Rotor Failure (In Flight)

1. **AIRSPEED** — 130–160 km/h (directional control via vertical stabilizer)
2. **HOVER AND LOW SPEED** — AVOID
3. **RUNNING LANDING ONLY** — do not attempt to hover
4. **AT TOUCHDOWN** — be prepared for yaw during rollout

---

## Completion Standards

The student **PASSES** Event 1 when they can:

| Standard | Requirement |
|---|---|
| **Oral exam** | Answer all knowledge questions correctly, or self-correct within one re-ask |
| **Boldface recitation** | Recite all 5 boldface items verbatim, without prompting, in sequence |
| **Cockpit identification** | Point out any named instrument/control in either cockpit within 10 seconds |
| **Limitations** | State all critical limits (VNE, Nr range, EGT limits, torque limits, crosswind limit) from memory |
| **Aerodynamics** | Explain ETL, LTE, ground resonance, and settling with power in own words |

A student who cannot recite boldface procedures verbatim does **not** advance to Event 2, regardless of other performance.

---

*Based on Mi-24P RLE, Mi-24P Technical Description, and Eagle Dynamics DCS World Mi-24P Hind module documentation. For simulation use only.*
