# Event 1 — Aircraft Systems & Academics

> **Course:** OH-58D Kiowa Warrior Basic Qualification Training | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [The OH-58D — Aircraft Overview](#the-oh-58d--aircraft-overview)
3. [Powerplant — T703-AD-700A Engine](#powerplant--t703-ad-700a-engine)
4. [Rotor System & Transmission](#rotor-system--transmission)
5. [Fuel, Hydraulic & Electrical Systems](#fuel-hydraulic--electrical-systems)
6. [FADEC — Full Authority Digital Engine Control](#fadec--full-authority-digital-engine-control)
7. [Rotary-Wing Aerodynamics](#rotary-wing-aerodynamics)
8. [Cockpit Orientation](#cockpit-orientation)
9. [Operating Limitations](#operating-limitations)
10. [Boldface Emergency Procedures](#boldface-emergency-procedures)
11. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Describe the T703-AD-700A turboshaft engine operating cycle, FADEC auto vs. manual mode, and all engine limitations (continuous, transient, starting)
- [ ] Explain the 4-blade soft-in-plane main rotor system, Nr governing range, and autorotation RPM range
- [ ] Describe the single hydraulic system, what it powers, and the flight characteristics when hydraulics are lost
- [ ] Explain the electrical system (DC generator, battery) and state battery endurance with generator offline
- [ ] Define and explain the following aerodynamic phenomena: translating tendency, ETL, transverse flow effect, dissymmetry of lift, retreating blade stall, ground effect (IGE vs. OGE), settling with power (SWP), LTE, mast bumping, and dynamic rollover
- [ ] Locate and identify all major cockpit panels and instruments by name and position
- [ ] Recite all critical operating limitations from memory (torque, TOT, Nr, Vne, G-limits, weight)
- [ ] Recite all boldface emergency procedures verbatim, in sequence, without reference to notes

---

## The OH-58D — Aircraft Overview

| Characteristic | Value |
|---|---|
| **Type** | Single-engine light observation/attack helicopter |
| **Manufacturer** | Bell Helicopter Textron |
| **Engine** | Rolls-Royce (Allison) 250-C30R/3 — T703-AD-700A |
| **Main Rotor** | 4-blade, soft-in-plane, semi-rigid; 35 ft diameter |
| **Tail Rotor** | 2-blade, semi-rigid; counterclockwise when viewed from left |
| **Max Gross Weight** | 5,500 lbs |
| **Vne (Doors On)** | 120 KIAS |
| **Vne (Doors Off)** | 110 KIAS |
| **Crew** | Pilot (right seat) + Co-Pilot/Observer (left seat) |
| **Primary Mission** | Armed reconnaissance, scout, light attack |
| **DCS Module** | Polychop Simulations — full-fidelity AFM |

The OH-58D is a **single-engine helicopter**. There is no second engine to pick up the load in case of failure. This means engine failure procedures must be **automatic and immediate**. The time from engine failure to unrecoverable Nr decay can be as little as 2–3 seconds at low altitude. Boldface drills are not optional.

---

## Powerplant — T703-AD-700A Engine

The OH-58D is powered by a single Rolls-Royce 250-C30R/3 turboshaft engine, designated **T703-AD-700A** under military nomenclature. It is a **free-turbine** design: the gas producer (N1/Ng) is mechanically independent of the power turbine (N2/Np), which drives the transmission and rotors.

### Engine Operating Limits

| Parameter | Continuous Limit | Transient Limit | Starting Limit |
|---|---|---|---|
| **TOT (Turbine Outlet Temperature)** | 737°C | 810°C (5 min) | **843°C** |
| **N1 (Gas Producer)** | 100% | 104% (5 sec) | — |
| **Torque (Q)** | 100% | 110% (10 sec) | — |
| **Engine Oil Pressure** | 90–130 PSI | — | < 60 PSI = shutdown |
| **Engine Oil Temperature** | 70–107°C | — | > 107°C = reduce power |

### Start Abort Criteria

| Condition | Indication | Action |
|---|---|---|
| **Hot Start** | TOT exceeds **843°C** and continues rising | Throttle to OFF immediately |
| **Hung Start** | N1 stagnates; TOT rising without N1 progress | Throttle to OFF; report to maintenance |
| **No Light-Off** | No TOT rise within 30 sec of fuel introduction | Throttle to OFF; investigate |
| **Chip Light** | CHIP caution illuminates during start | Abort; maintenance inspection required |

> *A hot start is the most common student error during Event 2. TOT rises quickly. The student must monitor the TOT gauge continuously and be prepared to pull the throttle to OFF without hesitation if 843°C is approached. Do not wait to see if it stabilizes.*

---

## Rotor System & Transmission

### Main Rotor

| Parameter | Value |
|---|---|
| **Blades** | 4-blade, soft-in-plane, semi-rigid hub |
| **Diameter** | 35 ft |
| **Rotation** | Counterclockwise when viewed from above (U.S. convention) |
| **Nr (Power On — Normal)** | 98–100% |
| **Nr (Power Off — Autorotation)** | 90–107% |
| **Nr Caution (Low)** | < 95% (caution light) |
| **Nr Warning (Low)** | < 90% (audio + light) |
| **Nr Overspeed** | > 107% |

### Tail Rotor

| Parameter | Value |
|---|---|
| **Blades** | 2-blade, semi-rigid |
| **Function** | Anti-torque; also provides directional control (yaw) |
| **Rotation** | Counterclockwise when viewed from left side |
| **Failure** | LTE precursor; loss = uncontrolled yaw toward retreating side |

### Transmission Limits

| Parameter | Caution | Limit |
|---|---|---|
| **Trans Oil Pressure** | < 30 PSI | XMSN OIL PRESS caution → reduce power/land |
| **Trans Oil Temperature** | 110–120°C | > 120°C = reduce power immediately |

---

## Fuel, Hydraulic & Electrical Systems

### Fuel System

| Parameter | Value |
|---|---|
| **Usable Fuel** | ~265 lbs (approx. 39 US gallons) |
| **Low Fuel Warning** | LOW FUEL caution at ≤ 83 lbs |
| **Fuel Boost Pump** | Electric; required for engine start and normal operations |
| **Endurance** | ~2 hours cruise depending on power setting |

### Hydraulic System

| Parameter | Value |
|---|---|
| **Type** | Single system — NO redundancy |
| **Pressure** | ~1,000 PSI |
| **Powers** | All flight control servos (cyclic, collective, tail rotor) |
| **Failure Effect** | All boost lost; control forces increase dramatically; run-on landing recommended |

> *⚠ The OH-58D has ONE hydraulic system. There is no backup. Any hydraulic failure means flying with raw, unboosted controls under extreme physical effort. Avoid hover after hydraulic failure if at all possible.*

### Electrical System

| Component | Function |
|---|---|
| **DC Starter-Generator** | Engine-driven; primary power source (28V DC) |
| **Battery** | 24V NiCd; ~30 min endurance on essential bus only |
| **Inverter** | DC-to-AC conversion; required for attitude indicator and some avionics |
| **Essential Bus** | Engine instruments, caution panel, radios — always powered |
| **Non-Essential Bus** | MFD, MMS, weapons panels — shed on battery-only ops |

---

## FADEC — Full Authority Digital Engine Control

The FADEC is the most important system-knowledge item for the OH-58D student. In **Auto Mode** (normal), the FADEC governs Nr automatically — the pilot sets the throttle to FLY and the FADEC handles fuel scheduling to maintain 100% Nr as collective changes. In **Manual Mode** (degraded/emergency), the pilot must coordinate throttle with collective manually.

| Situation | FADEC Mode | Pilot Action |
|---|---|---|
| Normal flight | AUTO | Throttle to FLY detent; collective freely as needed |
| FADEC failure | MANUAL | Correlate throttle with collective; monitor Nr and TOT continuously |
| Engine start | AUTO (start scheduling) | Follow startup sequence; FADEC manages fuel during light-off |

**FADEC Failure Indications:**
- FADEC caution light illuminates
- Nr may fluctuate or diverge from 100%
- TOT may spike or oscillate

**FADEC Failure Action:**
1. Throttle — adjust manually to maintain Nr at 100%
2. Monitor TOT — do not exceed 737°C continuous
3. Land as soon as practicable

---

## Rotary-Wing Aerodynamics

This section covers the aerodynamic phenomena that make helicopter flight fundamentally different from fixed-wing operations. All of these phenomena are modeled to varying degrees in the DCS OH-58D AFM.

### Translating Tendency (Hover Drift)

The tail rotor produces lateral thrust to counteract main rotor torque. On U.S. helicopters with counterclockwise main rotor rotation (viewed from above), this thrust pushes the aircraft **right**. The pilot compensates with **left cyclic** in hover.

- **Student Error:** Failure to pre-position cyclic slightly left before lifting to a hover. Result: immediate right drift.
- **DCS Behavior:** Modeled. Expect right drift in a no-wind hover with no left cyclic input.

### Effective Translational Lift (ETL)

As airspeed increases through **16–24 knots**, the rotor transitions from operating in its own disturbed downwash into cleaner air, producing a noticeable increase in lift efficiency.

| ETL Indication | What Happens | Pilot Response |
|---|---|---|
| Airspeed ~16–24 kts | Aircraft pitches nose-up, wants to climb, vibration changes | Forward cyclic, slight collective reduction, left pedal |
| Fully through ETL (> 24 kts) | Power requirement drops significantly | Reduce collective to maintain altitude if not climbing |

- **Student Error:** Allowing the nose to pitch up through ETL without forward cyclic, resulting in an uncontrolled climb.

### Transverse Flow Effect

During ETL transition, air entering the aft rotor disc has greater induced velocity than the forward disc, causing a **right roll tendency and vibration** at 10–20 knots. Left cyclic is required to counteract this.

### Dissymmetry of Lift & Blade Flapping

In forward flight, the advancing blade (into the relative wind) generates more lift than the retreating blade. The rotor compensates through **blade flapping** — advancing blade flaps up, retreating blade flaps down — equalizing lift. This is automatic in the rotor design.

### Retreating Blade Stall

At high airspeeds, the retreating blade can reach its stall angle of attack. Onset indications:

| Indication | Meaning |
|---|---|
| Abnormal vibration in pitch and roll | Retreating blade stall onset |
| Nose pitch-up (uncommanded) | Blade stall advancing to critical stage |
| Left roll tendency | Aft disc losing lift |

**Recovery:** Immediately reduce collective → reduce airspeed → level wings. Do NOT pull aft cyclic.

- **OH-58D Vne:** 120 KIAS (doors on) / 110 KIAS (doors off). Exceeding Vne risks retreating blade stall.

### Ground Effect (IGE vs. OGE)

In Ground Effect (IGE) — within approximately one rotor diameter (~35 ft) of the surface — the rotor operates more efficiently because ground interrupts the rotor downwash. This means **less power is required to hover IGE** than OGE.

| Condition | Hover Altitude | Power Required |
|---|---|---|
| **IGE** | < 35 ft AGL | Lower (10–15% less torque typical) |
| **OGE** | > 35 ft AGL | Higher |

- **Practical Implication:** If you cannot maintain a hover OGE (power-limited), you cannot accomplish a pinnacle or confined area operation that requires OGE hover.
- **DCS Behavior:** Ground effect modeled. The aircraft will require more collective as it rises above one rotor diameter.

### Settling with Power (Vortex Ring State)

Settling with Power (SWP) occurs when the helicopter descends into its own rotor downwash while under power. Conditions:

| Condition | Value |
|---|---|
| **Power** | 20–100% torque applied |
| **Rate of Descent** | > 300 FPM |
| **Airspeed** | < 30 KIAS (usually < 15 KIAS) |
| **Tailwind** | Increases susceptibility |

**Onset:** Increased vibration → uncommanded descent → loss of rotor authority → rapid sink rate.

**Recovery (Boldface):**
1. **CYCLIC** — **FORWARD** (aggressively — gain forward airspeed, break out of downwash)
2. **COLLECTIVE** — **Reduce momentarily** (if altitude permits, to break the vortex state)
3. Recover from resulting dive

> *SWP is the most dangerous approach-phase hazard. It can develop within 2–3 seconds and become unrecoverable below 200–300 ft AGL. The student must recognize onset and react immediately.*

### Loss of Tail Rotor Effectiveness (LTE)

LTE is a condition where the tail rotor cannot produce sufficient thrust to maintain directional control. Contributing conditions:

| Condition | LTE Risk |
|---|---|
| **Low airspeed (< 30 KIAS)** | High — no weathervaning effect to assist yaw control |
| **High power (high torque)** | High — more anti-torque thrust required |
| **Tailwind** | High — tailwind reduces tail rotor effectiveness |
| **Left crosswind (210–330° relative)** | High — vortex ring state of the tail rotor possible |
| **Right crosswind (030–160° relative)** | Moderate — main rotor disk vortex interference |

**LTE Onset:** Uncommanded right yaw that cannot be arrested with full left pedal.

**Recovery (Boldface):**
1. **PEDAL** — **FULL LEFT** (maximum anti-torque)
2. **COLLECTIVE** — **REDUCE** (reduce torque reaction; maintain Nr)
3. **CYCLIC** — **FORWARD** (gain airspeed; increase tail rotor effectiveness)
4. If unrecoverable: **EXECUTE AUTOROTATION**

### Mast Bumping

Mast bumping occurs when the rotor hub contacts the mast in **low-G flight conditions**. The soft-in-plane rotor of the OH-58D is particularly susceptible.

**Conditions:** Pushovers, negative-G flight, abrupt lateral cyclic at low airspeed.

**Effect:** Catastrophic structural failure — the rotor severs the mast. No recovery.

**Prevention:**
- Never push the nose over abruptly below 30 KIAS
- Never apply aggressive lateral cyclic at low airspeed
- Never enter negative-G flight
- If a low-G condition is inadvertently entered: **aft cyclic smoothly** to reload the rotor; do NOT add lateral cyclic

> *⚠ Mast bumping in the OH-58D is survivability-ending. One event is enough to sever the mast. This is not a warning or caution — it is a fatal outcome.*

### Dynamic Rollover

Dynamic rollover occurs during takeoff or landing when one skid is on the ground and a rolling moment exceeds the cyclic's ability to stop it.

| Factor | Effect |
|---|---|
| **Slope** | Side slope increases rollover tendency to the downslope side |
| **Crosswind** | Wind can assist the rollover moment |
| **Lateral cyclic near stop** | Nearing cyclic limits reduces arrest capability |
| **High collective** | More lift to the rotor = more roll moment |

**Critical Roll Rate:** Once dynamic rollover begins, if the roll rate exceeds ~10°/sec with the cyclic at its stop, recovery is no longer possible.

**Prevention:**
- Reduce collective smoothly during touchdown; do not hold collective high with a skid on the ground
- On slopes: upslope skid touches first
- If rollover begins with a skid on the ground: **COLLECTIVE DOWN immediately**

---

## Cockpit Orientation

The student must be able to locate each panel **by name** before Event 2. Use the DCS clickable cockpit and the OH-58D checklist for visual reference.

```
                        OVERHEAD CONSOLE
  [Fuel/Boost] [Generator] [Inverter] [Battery] [Lights] [FADEC]

  LEFT INSTRUMENT PANEL        CENTER          RIGHT INSTRUMENT PANEL
  [Torque gauge]          [MFD Display]        [TOT gauge]
  [Nr (Rotor RPM)]        [Caution Panel]      [N1 gauge]
  [Airspeed indicator]                         [Engine Oil Press/Temp]
  [Altimeter]                                  [Trans Oil Press/Temp]
  [VSI]

  LEFT CONSOLE             BETWEEN SEATS         RIGHT CONSOLE
  [Cyclic base]            [Collective]          [Radio panels]
  [Pedals (L)]             [Throttle grip]       [AHRS/GPS controller]
  [Force trim]                                   [Radar altimeter]
```

| Panel / Control | Location | Key Functions |
|---|---|---|
| **Battery Switch** | Overhead console | Master electrical power ON/OFF |
| **Fuel Boost Pump** | Overhead console — fuel panel | Required ON before engine start |
| **Generator Switch** | Overhead console — electrical panel | Generator ON after engine start |
| **Inverter Switch** | Overhead console — electrical panel | AC power for attitude indicator |
| **FADEC Switch** | Overhead console | Auto/Manual mode selection |
| **Throttle (Twist Grip)** | Collective grip | Engine power control; FLY detent for normal ops |
| **Force Trim Release** | Cyclic grip | Press-hold to move controls; release to set trim |
| **MFD (Multi-Function Display)** | Center instrument panel | Navigation pages, moving map, system data |
| **Caution/Warning Panel** | Center instrument panel | Engine, systems, and rotor caution lights |
| **Torque Gauge (Q%)** | Left instrument panel | Primary power indication |
| **TOT Gauge** | Right instrument panel | Engine temperature — primary limitation |
| **Nr Gauge (Rotor RPM)** | Left instrument panel | Rotor speed — critical in autorotation |
| **N1 Gauge** | Right instrument panel | Gas producer speed |
| **Airspeed Indicator** | Left instrument panel | Airspeed in KIAS |
| **Altimeter** | Left instrument panel | Pressure altitude |
| **Radar Altimeter** | Right console | AGL altitude — critical for low-level ops |
| **AHRS/GPS Controller** | Right console | Navigation system controller |
| **Radio Panels** | Right console | VHF/FM, UHF communications |
| **MMS Control Panel** | Left console / overhead area | Mast-Mounted Sight control (familiarization only) |

---

## Operating Limitations

Memorize these before Event 2. They will be tested verbally at the start of Event 7 and the Check Ride.

### Rotor Limits

| Parameter | Normal | Caution | Warning / Limit |
|---|---|---|---|
| **Nr (Power On)** | 98–100% | < 98% or > 100% | < 90% (critical low) / > 107% (overspeed) |
| **Nr (Autorotation)** | 90–107% | — | < 90% / > 107% |

### Engine Limits

| Parameter | Continuous | Transient | Start Limit |
|---|---|---|---|
| **TOT** | ≤ 737°C | 810°C (5 min) | **843°C** |
| **Torque** | ≤ 100% | 110% (10 sec) | — |
| **N1** | ≤ 100% | 104% (5 sec) | — |
| **Oil Pressure** | 90–130 PSI | — | < 60 PSI = shutdown |
| **Oil Temperature** | 70–107°C | — | > 107°C = reduce power |

### Airspeed Limits

| Limit | Speed |
|---|---|
| **Vne (Doors On)** | 120 KIAS |
| **Vne (Doors Off)** | 110 KIAS |
| **Max Sideward / Rearward Flight** | 35 kts |
| **Max Hover Taxi Speed** | 20 kts |
| **Best Autorotation (Min Rate of Descent)** | 60 KIAS |
| **Best Autorotation (Max Glide Distance)** | 80 KIAS |
| **ETL (Effective Translational Lift)** | 16–24 KIAS |

### Weight Limits

| Limit | Value |
|---|---|
| **Maximum Gross Weight** | 5,500 lbs |

### G-Limits

| Limit | Value |
|---|---|
| **Maximum Positive G** | +2.5 G |
| **Maximum Negative G** | −0.5 G |

### Crosswind & Wind Limits

| Condition | Limit |
|---|---|
| **Max Crosswind (Hover/Landing)** | 35 kts |
| **LTE Awareness Zone** | > 20 kts, low airspeed |

### Slope Limits

| Condition | Limit |
|---|---|
| **Side slope** | ≤ 10° |
| **Nose-up slope** | ≤ 10° |
| **Nose-down slope** | ≤ 5° |

---

## Boldface Emergency Procedures

These procedures must be **committed to memory** and recited verbatim before Event 2. They will be tested at the start of Event 7 and the Check Ride. Incorrect or incomplete boldface = no flight.

### 1. ENGINE FAILURE — POWER OFF (Autorotation Entry)

| Step | Action |
|---|---|
| 1 | **COLLECTIVE** — **LOWER** (immediately; maintain Nr 90–107%) |
| 2 | **AIRSPEED** — **60–80 KIAS** (best autorotation speed) |
| 3 | **THROTTLE** — **OFF** (if not already; engine has failed) |
| 4 | **MAYDAY** — **TRANSMIT** (if time permits) |
| 5 | **EXECUTE** — **AUTOROTATION TO LANDING** |

> *The first action — COLLECTIVE DOWN — must be instantaneous. Every second of delay causes Nr to decay below the safe autorotation range. Below 90% Nr, the recovery margin narrows rapidly.*

### 2. ENGINE FIRE IN FLIGHT

| Step | Action |
|---|---|
| 1 | **THROTTLE** — **OFF** |
| 2 | **AUTOROTATE** — **EXECUTE** |
| 3 | **LAND ASAP** |
| 4 | **FUEL BOOST PUMP** — **OFF** |
| 5 | **BATTERY** — **OFF** (after landing, before exiting) |

### 3. SETTLING WITH POWER (SWP) RECOVERY

| Step | Action |
|---|---|
| 1 | **CYCLIC** — **FORWARD AGGRESSIVELY** (gain forward airspeed) |
| 2 | **COLLECTIVE** — **REDUCE MOMENTARILY** (break vortex state; if altitude permits) |
| 3 | **RECOVER** from resulting nose-low attitude |

> *Do NOT pull aft cyclic. Do NOT increase collective. Both worsen SWP by deepening the aircraft further into its own downwash.*

### 4. LOSS OF TAIL ROTOR EFFECTIVENESS (LTE) RECOVERY

| Step | Action |
|---|---|
| 1 | **PEDAL** — **FULL LEFT** |
| 2 | **COLLECTIVE** — **REDUCE** (reduce torque) |
| 3 | **CYCLIC** — **FORWARD** (gain airspeed; improve tail rotor authority) |
| 4 | If unrecoverable: **AUTOROTATE** |

### 5. HYDRAULIC FAILURE IN FLIGHT

| Step | Action |
|---|---|
| 1 | **Expect** — HIGH CONTROL FORCES |
| 2 | **AIRSPEED** — **40–60 KIAS** (run-on landing speed) |
| 3 | **AVOID HOVER** — plan a run-on landing to a suitable area |
| 4 | **LAND ASAP** |

---

## Completion Standards

This is an academic event. The student passes by correctly answering the following questions without reference to notes.

- [ ] **Q1:** What is the TOT abort limit during engine start? *(843°C)*
- [ ] **Q2:** What is the normal power-on Nr range? *(98–100%)*. Autorotation range? *(90–107%)*
- [ ] **Q3:** The OH-58D has one hydraulic system. It fails in flight. What happens to the flight controls? *(All hydraulic boost is lost; control forces increase dramatically; avoid hover; plan run-on landing at 40–60 KIAS)*
- [ ] **Q4:** Define ETL. At what airspeed does it develop? What does the aircraft do? *(Effective Translational Lift — 16–24 kts; aircraft pitches nose-up, lift efficiency increases; requires forward cyclic and collective adjustment)*
- [ ] **Q5:** What three conditions lead to Settling with Power? *(Power applied 20–100%; Rate of descent > 300 FPM; Airspeed < 30 KIAS)*
- [ ] **Q6:** What is the FADEC in Auto Mode doing for you? *(Maintaining Nr at 100% by automatically adjusting fuel flow as collective changes)*
- [ ] **Q7:** Recite ENGINE FAILURE boldface verbatim. *(Collective LOWER / Airspeed 60–80 KIAS / Throttle OFF / Mayday transmit / Execute autorotation)*
- [ ] **Q8:** Recite SETTLING WITH POWER recovery boldface verbatim. *(Cyclic FORWARD aggressively / Collective REDUCE momentarily / Recover)*
- [ ] **Q9:** What is mast bumping and what causes it? *(Rotor hub contacts the mast — caused by low-G/pushovers/aggressive lateral cyclic at low airspeed; potentially fatal)*
- [ ] **Q10:** What is the maximum gross weight? Vne doors on? *(5,500 lbs; 120 KIAS)*

---

[→ Proceed to Event 2: Startup & Ground Operations](event-2-startup-ground-ops.md)

---

*Based on TM 1-1520-248-10, TC 3-04.4, and Eagle Dynamics / Polychop Simulations DCS OH-58D documentation. For simulation use only.*
