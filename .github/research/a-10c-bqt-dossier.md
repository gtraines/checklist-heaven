# Research Dossier: A-10C Basic Qualification Training (BQT)

> **Aircraft:** Fairchild Republic A-10C Thunderbolt II "Warthog"
> **Course Level:** Basic Qualification (Level 100)
> **Reference:** T.O. 1A-10C-1 Flight Manual / DCS A-10C II Tank Killer Module
>
> **DCS Module Note:** The A-10C is a **full-fidelity, clickable cockpit** module. Every switch, dial, circuit breaker panel, and indicator is interactive. Unlike the FC3 A-10A, all procedures involve physical cockpit interaction via mouse clicks and HOTAS commands. Keyboard shortcuts exist as alternatives but are secondary — the primary instruction is "hands in the cockpit." The A-10C II variant adds HMCS (Helmet Mounted Cueing System), APKWS (Laser Guided Rockets), and GBU-54 (LJDAM). Flight performance is identical between C and C II.

## Overview

This dossier provides the technical research foundation for a Basic Qualification Training course in the DCS A-10C Thunderbolt II. The course covers all phases of flight from cold-and-dark startup through safe recovery. **Combat employment (weapons delivery, TGP targeting, JTAC coordination) is out of scope** — those topics are covered in a separate Weapons Employment course. However, the student is introduced to core avionics (MFCDs, CDU, EGI) at a basic navigation level.

The A-10C is the precision engagement upgrade of the original A-10A, adding digital avionics, GPS-guided munitions capability, HOTAS controls, two multifunction color displays (MFCDs), a Control Display Unit (CDU), and the LASTE (Low Altitude Safety and Targeting Enhancement) system incorporating SAS and EAC. The airframe retains the A-10A's legendary survivability: twin TF34-GE-100A turbofans, titanium cockpit "bathtub," redundant hydraulic flight controls with manual reversion, and self-sealing fuel cells.

**Primary Real-World Sources:**
- T.O. 1A-10C-1 (A-10C Flight Manual / Dash-1)
- T.O. 1A-10C-34-1-1 (Non-Nuclear Weapons Delivery Manual — systems context only)
- AFMAN 11-2A-10C Vol. 3 (A-10C Operations Procedures)
- AFMAN 11-217 (Instrument Flying Procedures)
- USAF Contact Flying Manual

---

## Module 1: Aircraft Systems & Aerodynamics

### 1.1 Learning Objectives

- Student can describe the TF34-GE-100A engine characteristics including start cycle, spool-up lag, and ITT/N1/N2 operating limits.
- Student can explain the A-10C fuel system layout, feed sequence, crossfeed operation, and low-fuel indications.
- Student can describe the dual-redundant hydraulic system (A and B), identify what each powers, and explain manual reversion capability.
- Student can explain the electrical system architecture: battery, generators, APU, essential/non-essential bus, and emergency bus behavior.
- Student can describe the SAS and EAC flight control augmentation systems and explain when each is operative.
- Student can identify the ECS functions modeled in DCS (anti-ice, defog) and those simplified or absent.
- Student can list the A-10C survivability features and explain their operational implications.
- Student can recognize stall onset using the AoA indexer and describe departure/spin characteristics.

### 1.2 Key Data

#### 1.2.1 TF34-GE-100A Turbofan Engines

| Parameter | Value | Notes |
|---|---|---|
| **Engine Type** | General Electric TF34-GE-100A High-Bypass Turbofan | 6.2:1 bypass ratio; quiet, efficient at low altitude |
| **Thrust (per engine)** | 9,065 lbf (40.32 kN) | Sea level static; total 18,130 lbf installed |
| **Number of Engines** | 2 | Mounted high on rear fuselage pylons for FOD/IR protection |
| **Spool-Up Time** | ~4–6 seconds (idle to MIL) | High-bypass design spools relatively quickly |
| **Ground Idle RPM** | ~62–65% N1 | Approximately 60% N2 |
| **Flight Idle RPM** | ~70% N1 | Higher than ground idle; engages automatically airborne |
| **Max RPM (N1)** | 98% | Primary thrust indicator |
| **Max RPM (N2)** | 99% | Core speed limit |
| **ITT Limit (Start)** | 860°C | Abort start if exceeded — hot start |
| **ITT Limit (Max Continuous)** | 810°C | Normal operations ceiling |
| **ITT Limit (Transient/Takeoff)** | 900°C | 5-minute time limit |
| **Oil Pressure (Normal)** | 25–65 PSI | Per engine |
| **Oil Pressure (Min)** | 15 PSI | Below = caution; 0 PSI = shutdown engine |
| **Fuel Flow (Cruise)** | ~1,800–2,200 lbs/hr total | Both engines, mid-altitude cruise |
| **Fuel Flow (Max Power, Low Alt)** | ~3,000–3,500 lbs/hr total | Both engines, full military power |

**Start Cycle Sequence:**
The TF34-GE-100A uses a pneumatic start via the APU or crossbleed air. The start sequence is:
1. APU provides bleed air to spin the engine starter.
2. N2 begins to rise. At approximately 12–15% N2, fuel is introduced (throttle advanced from CUTOFF to IDLE).
3. Ignition occurs; ITT rises sharply then stabilizes.
4. Engine accelerates through light-off to idle (~62% N1). Total start time: ~30–45 seconds per engine.
5. **Abort criteria:** ITT exceeding 860°C (hot start), N2 stagnation below 55% (hung start), or no light-off within 30 seconds.

**Spool-Up Lag:**
The TF34's high-bypass design means throttle response from idle to full power takes 4–6 seconds. This is operationally significant during go-arounds and low-altitude maneuvering — the pilot must anticipate power requirements. Unlike low-bypass engines, the TF34 does not suffer from compressor stall issues during rapid throttle advancement.

> *⚠ Realism Divergence: In the real A-10C, individual engine instruments (ITT, N1, N2, fuel flow, oil pressure) are analog gauges on the right instrument panel. DCS models all of these gauges accurately and they are fully readable/clickable. The DCS start cycle closely matches real-world procedures. However, DCS does not model all hot-start failure modes — a real hot start can cause turbine blade damage requiring maintenance action; in DCS, a hot start simply prevents the engine from reaching idle and requires a motor cycle to clear.*

#### 1.2.2 Fuel System

| Parameter | Value | Notes |
|---|---|---|
| **Internal Fuel Capacity** | ~10,700 lbs (~1,644 US gal) | Two main wing tanks + fuselage feeder cells |
| **External Tanks** | 2 × 600 US gal (Stations 3 and 9) | ~4,000 lbs additional per pair |
| **Fuel Type** | JP-8 (JP-4 alternate) | Standard USAF |
| **Low Fuel Warning** | ~1,500 lbs total remaining | Master Caution + FUEL LOW caution light |
| **Bingo Fuel** | Mission dependent | Typically 2,500–3,000 lbs for RTB |
| **Feed Sequence** | Wing tanks → Fuselage feeder cells (automatic) | Gravity and boost pump assisted |
| **Fuel Totalizer** | Center instrument panel | Displays total remaining fuel |
| **Fuel Flow Indicators** | Right instrument panel | Individual per-engine flow rate |

**Fuel System Architecture:**
- **Main Wing Tanks:** Left and right wing tanks are the primary fuel storage. Feed is automatic via boost pumps.
- **Fuselage Cells:** Internal fuselage cells act as feeders/collectors, receiving fuel from wing tanks.
- **Crossfeed:** A crossfeed valve allows either engine to draw fuel from both sides, essential for single-engine operations or fuel balancing. The crossfeed switch is on the **fuel panel, left console**.
- **Self-Sealing Tanks:** All internal tanks use reticulated polyurethane foam and are self-sealing, designed to survive 23mm HEI impacts.
- **Fuel Dump:** Not available on the A-10C. If overweight for landing, the pilot must burn off fuel or jettison stores.
- **Boost Pumps:** Left and right wing boost pumps, plus a fuselage transfer pump. Loss of boost pumps may result in fuel starvation at high altitude.

**Cockpit Switch Reference:**
| Switch / Indicator | Location | Action |
|---|---|---|
| Fuel Totalizer | Center instrument panel | Displays total fuel (lbs) — rotate knob to set |
| L/R Fuel Flow Gauges | Right instrument panel | Read-only — lbs/hr per engine |
| L/R Wing Boost Pump switches | Left console — Fuel Panel | ON/OFF — normally ON |
| Crossfeed Switch | Left console — Fuel Panel | OPEN/CLOSED — normally CLOSED |
| Signal Fuel Low Caution | Caution/Advisory panel | Illuminates at ~1,500 lbs |

> *⚠ Realism Divergence: The real A-10C fuel system includes additional complexity in the form of a vent/pressurization system and suction feed backup. DCS models the boost pumps and crossfeed accurately but simplifies the vent system. Fuel imbalance warnings are modeled. Fuel leaks from combat damage are modeled and will show decreasing fuel quantity on the affected side.*

#### 1.2.3 Hydraulic System

| System | Operating Pressure | Powers |
|---|---|---|
| **Hydraulic System A** | 3,000 PSI | Left elevator, left aileron, left rudder, nosewheel steering (NWS), normal brakes |
| **Hydraulic System B** | 3,000 PSI | Right elevator, right aileron, right rudder, speed brakes, utility functions |
| **Combined** | Both at 3,000 PSI | Landing gear extension/retraction, flaps |

- **Dual Independence:** Each hydraulic system is powered by an engine-driven pump (System A = left engine, System B = right engine). Loss of one system still provides full-authority hydraulic control on one side, with degraded response on the failed side.
- **Manual Reversion:** With BOTH hydraulic systems failed, the pilot engages manual reversion via pitch and roll disconnect switches on the **left console**. In manual reversion: stick forces increase dramatically (~60–80 lbs), no flaps, no speed brakes, emergency gear extension only, and differential braking for directional control.
- **Hydraulic Pressure Gauges:** Two gauges on the **right instrument panel** — one for System A, one for System B. Normal indication: 3,000 PSI ±200.

**Cockpit Switch Reference:**
| Switch / Indicator | Location | Action |
|---|---|---|
| HYD A Pressure Gauge | Right instrument panel | Read-only — normal 3,000 PSI |
| HYD B Pressure Gauge | Right instrument panel | Read-only — normal 3,000 PSI |
| Manual Pitch Reversion | Left console — Flight Control Panel | NORM / MAN REVERT |
| Manual Roll Reversion | Left console — Flight Control Panel | NORM / MAN REVERT |

> *⚠ Realism Divergence: DCS fully models dual hydraulic failure and manual reversion. The significantly increased stick forces are simulated — the pilot will notice sluggish, heavy response. In the real aircraft, the physical effort is extreme and fatiguing; in DCS, this translates to reduced control deflection rates. Emergency gear extension (gravity drop) is also fully modeled.*

#### 1.2.4 Electrical System

| Component | Function | Notes |
|---|---|---|
| **Battery** | 24V DC — initial power source | Powers essential bus for ~30 min |
| **APU Generator** | 115V AC / 28V DC | Provides ground power; can be used as emergency backup in flight below 15,000 ft |
| **Left Generator** | 115V AC / 28V DC | Primary — powered by left engine |
| **Right Generator** | 115V AC / 28V DC | Primary — powered by right engine |
| **Inverter** | Converts DC to AC | Powers AC instruments from battery |
| **Essential Bus** | Critical flight instruments | Stays powered as long as ANY source is available |
| **Non-Essential Bus** | Avionics, lighting, non-critical | Shed first during electrical emergency |
| **Emergency Bus** | Standby instruments, fire warning | Battery-backed; always available if battery has charge |

**Electrical Architecture:**
- **Normal Operation:** Both engine-driven generators supply the main AC and DC buses. The battery is maintained on float charge.
- **Single Generator Loss:** The remaining generator powers all buses — no degradation unless load exceeds capacity.
- **Double Generator Loss:** The battery and APU (if started below 15,000 ft) become the only power sources. The non-essential bus is shed automatically. Essential instruments (standby ADI, magnetic compass, engine instruments, fire warning) remain on the emergency bus.
- **Battery-Only Endurance:** Approximately 30 minutes with non-essential bus shed. Sufficient for an emergency approach and landing.

**Cockpit Switch Reference:**
| Switch / Indicator | Location | Action |
|---|---|---|
| Battery Switch | Left console — Electrical Panel | ON / OFF |
| APU Switch | Left console — Electrical Panel | START / ON / OFF |
| Left Generator Switch | Left console — Electrical Panel | PWR / OFF / TEST |
| Right Generator Switch | Left console — Electrical Panel | PWR / OFF / TEST |
| Inverter Switch | Left console — Electrical Panel | STBY / OFF / TEST |
| Essential Bus Indicator | Caution panel | ESSENTIAL BUS FAIL warning |

> *⚠ Realism Divergence: DCS models the electrical system with good fidelity, including bus shedding during double generator failure and battery endurance. However, individual circuit breaker modeling is simplified — in the real A-10C, the pilot can pull/reset individual CBs for troubleshooting. In DCS, most circuit breakers are non-functional cosmetic items. The APU start sequence is accurately modeled including the altitude limitation.*

#### 1.2.5 Flight Control System — SAS & EAC

| System | Function | Controls |
|---|---|---|
| **SAS (Stability Augmentation System)** | Provides rate damping in pitch, yaw, and roll | 3 channels: Pitch, Yaw, Roll — each independently switchable |
| **EAC (Enhanced Attitude Control)** | Provides attitude hold and turn coordination | Works through SAS — requires SAS channels engaged |
| **Trim** | Electric trim in pitch, roll, and rudder | Trim button on stick (4-way hat); rudder trim on left console |

**SAS Details:**
- SAS provides **rate damping** — it resists uncommanded aircraft motions (turbulence, asymmetric thrust, etc.) but does not hold attitude.
- Three independent channels: **Pitch SAS**, **Yaw SAS** (left and right independently), and **Roll SAS** (DCS simplifies to a combined yaw channel).
- SAS switches are on the **SAS panel, left console**. Each channel has an ON/OFF toggle.
- If a SAS channel trips off (due to transient or malfunction), the pilot must manually reset it.
- **SAS OFF handling:** Without SAS, the A-10C is still fully controllable but requires more pilot input — particularly in yaw. The aircraft tends to develop dutch roll oscillations without yaw SAS.

**EAC Details:**
- EAC provides **attitude hold** — when the pilot releases the stick, EAC holds the current bank angle and pitch attitude.
- EAC also provides **turn coordination** — reducing the need for rudder input in turns.
- EAC operates THROUGH the SAS servos — if SAS channels are disengaged, EAC cannot function on those axes.
- EAC is armed via a switch on the **SAS panel, left console** and engaged via the **autopilot/paddle switch on the HOTAS stick**.
- **EAC vs. Autopilot:** EAC is NOT a full autopilot. It holds attitude but does not hold heading, altitude, or navigate. Think of it as a "hands-off for a moment" system.

**Cockpit Switch Reference:**
| Switch / Indicator | Location | Action |
|---|---|---|
| Pitch SAS Switch | Left console — SAS Panel | ON / OFF |
| Yaw SAS Switch | Left console — SAS Panel | ON / OFF |
| Roll SAS Switch | Left console — SAS Panel | ON / OFF (DCS: combined L/R yaw) |
| EAC Switch | Left console — SAS Panel | ARM / OFF |
| SAS Paddle Switch | HOTAS Stick | Press to disengage/re-engage SAS (momentary) |
| Trim Hat | HOTAS Stick | 4-way: Pitch up/down, Roll left/right |
| Rudder Trim | Left console | Rotary knob |

> *⚠ Realism Divergence: DCS models SAS and EAC with high fidelity. The primary simplification is that the real A-10C has separate left and right yaw SAS channels, while DCS combines them into a single yaw SAS switch. The SAS trip/reset behavior is accurately modeled — transients (such as weapon release or heavy turbulence) can trip individual channels. EAC attitude hold and turn coordination are accurately modeled.*

#### 1.2.6 Environmental Control System (ECS)

| System | DCS Status | Notes |
|---|---|---|
| **Anti-Ice (Engine)** | Modeled | Engine anti-ice switch on left console |
| **Anti-Ice (Pitot)** | Modeled | Pitot heat switch — critical for accurate airspeed |
| **Windshield Defog/De-Ice** | Partially modeled | Bleed air defog; rain removal not modeled |
| **Pressurization** | Not modeled | Real aircraft pressurized to 8,000 ft cabin altitude |
| **Oxygen System** | Cosmetic | Switches exist but no physiological effects |

**Cockpit Switch Reference:**
| Switch / Indicator | Location | Action |
|---|---|---|
| Engine Anti-Ice | Left console — ECS Panel | ON / OFF |
| Pitot Heat | Left console — ECS Panel | ON / OFF — **always ON for flight** |
| Windshield Defog | Left console — ECS Panel | ON / OFF |

> *⚠ Realism Divergence: The real A-10C has a full ECS providing pressurization, temperature control, and oxygen regulation. DCS simplifies this significantly — pressurization is not modeled, oxygen has no physiological effect, and temperature control is cosmetic. However, pitot heat IS operationally important in DCS — forgetting it can cause erratic airspeed indications in icing conditions. Engine anti-ice should be used when operating in visible moisture below 10°C.*

#### 1.2.7 Survivability Features

| Feature | Description |
|---|---|
| **Titanium "Bathtub"** | 1,200 lbs of titanium armor surrounding the cockpit — resists 23mm HEI rounds |
| **Self-Sealing Fuel Tanks** | Reticulated polyurethane foam; designed to survive 23mm impacts |
| **Redundant Flight Controls** | Dual hydraulic systems + manual reversion; can fly with both systems failed |
| **Dual Engines** | Widely separated on fuselage; single-engine flight is routine |
| **Foam-Filled Fuselage** | Fire-retardant foam in fuselage voids |
| **Triple-Redundant Spar** | Wing main spar has three load paths |
| **Combat Damage Tolerance** | Designed to sustain significant battle damage and remain flyable |

These features directly affect training:
- Students must practice single-engine procedures as a **routine** skill, not an emergency afterthought.
- Manual reversion handling should be demonstrated at altitude before solo flight.
- The aircraft's damage tolerance means battle-damaged A-10Cs may return with significant controllability issues — students need exposure to degraded-mode flight.

#### 1.2.8 Stall Characteristics

| Indicator | AoA (Units) | Meaning |
|---|---|---|
| **Green Donut** (AoA Indexer) | ~11 units | On-speed — optimal approach AoA |
| **Upper Chevron** (▲) | < 11 units | Fast — below on-speed AoA |
| **Lower Chevron** (▼) | > 11 units | Slow — above on-speed AoA |
| **Buffet Onset** | ~18 units | Light airframe buffet — approaching stall |
| **Stall Warning (Chopper)** | ~20 units | Stick shaker / audio warning |
| **Full Stall** | ~22–24 units | Wing stall — loss of lift; nose drops |

**Departure & Spin Characteristics:**
- The A-10C is generally resistant to departures. The straight wing and large tail surfaces provide natural stall warning through buffet and progressive lift loss.
- Stall is characterized by a nose-drop — the aircraft tends to recover naturally with neutral stick and forward throttle.
- Spins are possible but require sustained pro-spin inputs. Recovery: idle throttle, neutral stick, full opposite rudder, then dive recovery once rotation stops.
- With asymmetric stores, stall behavior may include a wing drop toward the heavier side. Students should be aware of this during slow flight practice.

**AoA Indexer Location:** Left canopy rail — three lights visible in peripheral vision during approach.

> *⚠ Realism Divergence: DCS models the A-10C's stall characteristics with good accuracy using the Advanced Flight Model (AFM). Buffet onset, progressive stall, and spin behavior match real-world descriptions closely. The AoA indexer is accurately modeled and is the primary approach speed reference. One simplification: the real A-10C has a stick shaker (physical vibration) at stall onset; DCS provides only audio warning and visual indexer indication — no force feedback stick shaker unless the pilot uses a force-feedback joystick.*

### 1.3 Instructor Notes

| Common Student Error | Correction |
|---|---|
| Ignoring spool-up lag during go-around | Emphasize: 4–6 seconds from idle to full power. Anticipate power needs — don't wait until on the runway to go full throttle. |
| Not monitoring ITT during start | ITT is the primary engine health indicator during start. Drill: eyes on ITT from fuel introduction to idle stabilization. |
| Forgetting to reset tripped SAS channels | SAS channels trip silently. Student must develop a scan that includes SAS panel. Teach "SAS check" as part of every post-maneuver scan. |
| Confusing SAS and EAC functions | SAS = rate damping (always on). EAC = attitude hold (optional). EAC needs SAS. Demonstrate: fly with SAS only, then add EAC — feel the difference. |
| Neglecting fuel balance during single-engine ops | If one engine is shut down, the corresponding wing tank stops feeding. Crossfeed must be opened or the remaining engine will flame out. |
| Not understanding manual reversion implications | Demonstrate at altitude: engage manual reversion, feel the heavy stick forces, practice a wide pattern approach. Student must know this before solo. |

---

## Module 2: Cockpit Familiarization

### 2.1 Learning Objectives

- Student can identify and locate all major cockpit panels: left console, right console, instrument panel, glareshield, and center pedestal.
- Student can describe the function of the AHCP (Armament HUD Control Panel) switches and identify Master Arm, Gun/PAC Arm, Laser Arm, and TGP positions.
- Student can explain the LASTE system and its SAS/EAC sub-modes.
- Student can operate the UFC (Upfront Controller) for radio tuning, IFF, and basic steerpoint selection.
- Student can power on and navigate the left and right MFCDs using OSB buttons.
- Student can access the CDU and perform basic steerpoint page navigation.
- Student can identify the CMSC/CMSP displays and select a chaff/flare program.
- Student can read all engine instruments and state their normal operating ranges.
- Student can identify warning/caution/advisory panel indications and acknowledge master caution.
- Student can operate cockpit and exterior lighting for day and night operations.

### 2.2 Cockpit Layout Overview

```
┌─────────────────────────────────────────────────────────────────────┐
│                         CANOPY FRAME                                │
│                                                                     │
│  AoA Indexer                                        Standby ADI     │
│  (L canopy rail)              HUD                   (R glare)       │
│                        ┌─────────────┐                              │
│    Master Caution ──── │             │ ──── Fire Warning T-Handles  │
│                        └─────────────┘                              │
│                                                                     │
│  ┌──────────┐    ┌──────────────────┐    ┌──────────┐              │
│  │ LEFT     │    │  INSTRUMENT      │    │ RIGHT    │              │
│  │ MFCD     │    │  PANEL           │    │ MFCD     │              │
│  │          │    │  (ADI, HSI,      │    │          │              │
│  │ OSB 1-20 │    │   Altimeter,     │    │ OSB 1-20 │              │
│  │          │    │   Airspeed,      │    │          │              │
│  └──────────┘    │   VSI, AoA)      │    └──────────┘              │
│                  └──────────────────┘                                │
│                                                                     │
│  ┌─────────────────┐              ┌──────────────────┐             │
│  │  LEFT CONSOLE   │              │  RIGHT CONSOLE   │             │
│  │  - Electrical   │    Stick     │  - CDU            │             │
│  │  - Fuel Panel   │     & Seat   │  - Lighting       │             │
│  │  - ECS Panel    │              │  - TACAN           │             │
│  │  - SAS Panel    │   Throttle   │  - IFF Panel       │             │
│  │  - Flight Ctrl  │   Quadrant   │  - Oxygen           │             │
│  └─────────────────┘              └──────────────────┘             │
│                                                                     │
│  GLARESHIELD: UFC (center), AHCP (left), CMSC (right)              │
│  LOWER INSTRUMENT: Engine gauges, Hyd gauges, Fuel totalizer       │
└─────────────────────────────────────────────────────────────────────┘
```

### 2.3 Panel-by-Panel Reference

#### 2.3.1 Left Console

| Panel | Location | Key Switches / Functions |
|---|---|---|
| **Electrical Panel** | Left console, forward | Battery, APU, L/R Generator, Inverter |
| **Fuel Panel** | Left console, mid-forward | L/R Wing Boost Pumps, Crossfeed, Tank Gate |
| **ECS Panel** | Left console, mid | Pitot Heat, Engine Anti-Ice, Defog, Bleed Air |
| **SAS Panel** | Left console, mid-aft | Pitch/Yaw/Roll SAS, EAC Arm, Autopilot |
| **Flight Control Panel** | Left console, aft | Manual Pitch/Roll Reversion, Flap Switch, Speed Brake |
| **Throttle Quadrant** | Left console, aft-lower | Dual throttles, friction lock, Engine Operate (IGN/MOTOR/NORM), Engine Fire T-Handles |

#### 2.3.2 Right Console

| Panel | Location | Key Switches / Functions |
|---|---|---|
| **CDU (Control Display Unit)** | Right console, forward | Primary navigation computer — alphanumeric keyboard, function keys, display |
| **Lighting Panel** | Right console, mid | Cockpit flood/instrument/console lighting, formation lights |
| **TACAN Panel** | Right console, mid | TACAN channel selector, mode (T/R, A/A, OFF) |
| **IFF Panel** | Right console, mid-aft | IFF Mode 1/2/3/4, IDENT |
| **Oxygen Panel** | Right console, aft | Supply lever, diluter, emergency |

#### 2.3.3 Instrument Panel (Center)

| Instrument | Location | Function |
|---|---|---|
| **ADI (Attitude Director Indicator)** | Center, upper | Primary pitch/roll reference, ILS needles |
| **HSI (Horizontal Situation Indicator)** | Center, lower | Heading, course, bearing to steerpoint, CDI |
| **Altimeter** | Center-right | Barometric altitude — Kollsman window for QNH |
| **Airspeed Indicator** | Center-left | Calibrated airspeed (KIAS), Mach window |
| **VSI (Vertical Speed Indicator)** | Right of altimeter | Rate of climb/descent (ft/min) |
| **AoA Gauge** | Left of ADI | AoA in units — backup to HUD/indexer |
| **Accelerometer (G Meter)** | Below AoA gauge | Current G, max G, min G — resettable |
| **Clock** | Lower right | Elapsed time / mission time |
| **Standby ADI** | Right glareshield | Backup attitude reference — uncage for use |
| **Standby Compass** | Windshield frame | Magnetic compass — primary backup if all electrics fail |

#### 2.3.4 Glareshield

| Panel | Location | Key Functions |
|---|---|---|
| **UFC (Upfront Controller)** | Glareshield, center | Radio frequency entry, IFF, steerpoint select, master caution acknowledge, option display |
| **AHCP (Armament HUD Control Panel)** | Glareshield, left | Master Arm (SAFE/ARM/TRAIN), Gun/PAC Arm, Laser Arm (SAFE/ARM), TGP (OFF/STBY/OPER), IFFCC, HMCS |
| **CMSC (Countermeasures Signal Converter)** | Right of right MFCD | RWR threat display, missile launch warning, priority/search indicators |

#### 2.3.5 Lower Instrument Panel (Engine Gauges)

| Gauge | Location | Normal Range |
|---|---|---|
| **Left ITT** | Lower left | 400–600°C cruise, <810°C continuous, <860°C start |
| **Right ITT** | Lower right | Same as left |
| **Left N1 (Fan Speed)** | Below left ITT | 62–65% idle, <98% max |
| **Right N1** | Below right ITT | Same |
| **Left N2 (Core Speed)** | Below left N1 | ~60% idle, <99% max |
| **Right N2** | Below right N2 | Same |
| **Left Fuel Flow** | Lower cluster | 600–1,200 lbs/hr per engine cruise |
| **Right Fuel Flow** | Lower cluster | Same |
| **Left Oil Pressure** | Lower cluster | 25–65 PSI normal |
| **Right Oil Pressure** | Lower cluster | Same |
| **Hydraulic A Pressure** | Lower right cluster | 3,000 PSI ±200 |
| **Hydraulic B Pressure** | Lower right cluster | 3,000 PSI ±200 |
| **Fuel Totalizer** | Center lower | Rotary set — shows total lbs remaining |

### 2.4 Key Systems Detail

#### 2.4.1 AHCP (Armament HUD Control Panel)

The AHCP is the master armament control panel on the **left glareshield**. For BQT, the student must identify each switch position but will not employ weapons.

| Switch | Positions | BQT Setting | Notes |
|---|---|---|---|
| **Master Arm** | SAFE / ARM / TRAIN | **SAFE** | TRAIN enables HUD symbology without live release |
| **Gun/PAC Arm** | SAFE / ARM / 1 / 2 | **SAFE** | PAC = Precision Attitude Control (gun stabilization) |
| **Laser Arm** | SAFE / ARM | **SAFE** | Arms TGP laser designator |
| **TGP** | OFF / STBY / OPER | **STBY → OPER** | Power on early — IR detector needs 3–5 min cooling |
| **IFFCC** | OFF / TEST / ON | **ON** | Initializes weapon computer for HUD symbology |
| **HMCS** | OFF / ON | **ON** (if equipped) | Helmet Mounted Cueing System |
| **Altimeter** | RADAR / BARO / DIS | **RADAR** | Selects radar altimeter source for HUD |

#### 2.4.2 LASTE (Low Altitude Safety and Targeting Enhancement)

LASTE is the integrated system that provides:
- **SAS** — Rate damping (described in Module 1)
- **EAC** — Attitude hold and turn coordination (described in Module 1)
- **Ground Collision Avoidance System (GCAS)** — Warns of impending terrain impact (PULL UP cue)
- **IFFCC (Integrated Flight and Fire Control Computer)** — Computes weapon delivery solutions for HUD display

For BQT, the student interacts primarily with SAS/EAC. GCAS is always active (no switch to enable). IFFCC is powered on for HUD symbology but weapons delivery is out of scope.

#### 2.4.3 UFC (Upfront Controller)

The UFC is the primary pilot interface for communications and IFF, located at **glareshield center**.

| Function | Action | Notes |
|---|---|---|
| **Radio Frequency Entry** | Press radio select (COM1/COM2), enter frequency on scratchpad, press ENTER | COM1 = UHF (ARC-164), COM2 = VHF (ARC-186) |
| **Master Caution Acknowledge** | Press the **master caution** button (left of UFC) | Extinguishes master caution light; caution panel retains active faults |
| **Steerpoint Select** | Rotate the steerpoint knob (left rotary on UFC) | Cycles through mission steerpoints; HUD cue updates |
| **IFF** | Select IFF on UFC, enter Mode 3/C code | Required for ATC identification |
| **Option Display** | 5 option windows (1–5) with adjacent buttons | Context-dependent — shows radio presets, IFF modes, etc. |

**Key UFC Keyboard:**
- Numeric keypad (0–9) for frequency and code entry
- ENTER to confirm
- CLR to clear scratchpad
- Left/Right rotary knobs for steerpoint and radio channel selection

#### 2.4.4 MFCDs (Multifunction Color Displays)

The A-10C has two identical 5" × 5" color MFCDs flanking the instrument panel.

| Feature | Detail |
|---|---|
| **Power** | Brightness knob on each MFCD bezel — rotate clockwise from OFF to power on |
| **OSBs (Option Select Buttons)** | 20 per MFCD — 5 per side (top, bottom, left, right) |
| **Designation** | Left MFCD = "LMFD", Right MFCD = "RMFD" |
| **Default Pages** | Configurable — typically LMFD shows TAD or TGP, RMFD shows HSD or WPN |

**Common MFCD Pages:**
| Page | OSB Access | Function |
|---|---|---|
| **HQ (Home)** | OSB at top-left | Master page directory |
| **TAD (Tactical Awareness Display)** | Via HQ menu | Moving map with own-ship, steerpoints, threats |
| **HSD (Horizontal Situation Display)** | Via HQ menu | Navigation display — heading, course, waypoints |
| **WPN (Weapon)** | Via HQ menu | Weapon selection and status (BQT: view only) |
| **STAT (Status)** | Via HQ menu | System status page — fuel, stores, faults |
| **CDU (Mirror)** | Via HQ menu | Mirrors CDU display on MFCD |
| **TGP** | Via HQ menu | Targeting pod video feed |
| **DSMS (Digital Stores Management)** | Via WPN | Stores inventory and management |

**MFCD Power-On Sequence:**
1. Rotate brightness knob clockwise past detent — display illuminates.
2. MFCD runs a brief self-test (~5 seconds).
3. Default pages load based on DTC (Data Transfer Cartridge) programming or last-used configuration.
4. Press any OSB to begin navigation.

#### 2.4.5 CDU (Control Display Unit)

The CDU is the primary navigation computer interface, located on the **right console, forward**.

| Feature | Detail |
|---|---|
| **Display** | Small monochrome LCD with multiple lines of text |
| **Keyboard** | Full alphanumeric keyboard + function keys |
| **Key Pages** | WPT (waypoints), FPLN (flight plan), NAV (navigation status), PERF (performance) |
| **Power** | CDU power switch on right console — ON initiates self-test (~30 sec) |

**Basic CDU Operations for BQT:**
| Task | Procedure |
|---|---|
| Access steerpoints | Press `WPT` → use page up/down to cycle steerpoints |
| Enter coordinates | Select steerpoint → type LAT/LONG or MGRS → press `ENTER` |
| Check nav status | Press `NAV` → verify GPS status, position quality |
| Select active steerpoint | Press `STEER` → enter steerpoint number → `ENTER` |

#### 2.4.6 CMSC / CMSP (Countermeasures)

| System | Location | Function |
|---|---|---|
| **CMSC (Countermeasures Signal Converter)** | Right of right MFCD | Displays RWR threats (azimuth), missile launch warnings, priority/search |
| **CMSP (Countermeasures Signal Processor)** | Left console or HOTAS | Chaff/flare program selection, manual/auto/semi-auto dispensing |
| **MWS (Missile Warning System)** | Integrated | Audio/visual warning of inbound missiles |

**CMSP Operation:**
| Switch/Button | Location | Function |
|---|---|---|
| CMSP Power | Left console — CMSP Panel | OFF / STBY / MAN / SEMI / AUTO |
| Chaff Dispense | HOTAS CMS Switch (aft) or `[` key | Dispenses chaff bundle |
| Flare Dispense | HOTAS CMS Switch (forward) or `]` key | Dispenses flare |
| Program Select | CMSP panel — rotary or OSB | Selects pre-programmed countermeasure pattern |
| Jettison | CMSP panel | Emergency dispense all remaining |

**BQT Requirement:** Student must be able to power on CMSP, select MAN mode, and manually dispense chaff/flares. Auto/semi-auto program configuration is covered in weapons employment courses.

#### 2.4.7 Warning / Caution / Advisory Panel

| Category | Color | Location | Response |
|---|---|---|---|
| **Warning** | Red | Fire T-handles (glareshield), MASTER WARNING | Immediate action required — boldface procedures |
| **Caution** | Yellow/Amber | Caution panel (right of instrument panel) | Timely action required — consult checklist |
| **Advisory** | Green | Advisory panel (below caution panel) | Informational — no immediate action |
| **Master Caution** | Amber | Left of UFC, glareshield | Press to acknowledge — clears light but not fault |
| **Fire Warning T-Handles** | Red | Glareshield, two handles (L/R engine) | Pull to shut off fuel/hydraulic, arm extinguisher |
| **Gear Warning Horn** | Audio | N/A | Sounds when throttle below threshold with gear up |

#### 2.4.8 Lighting Controls

| System | Location | Controls |
|---|---|---|
| **Cockpit Flood Lights** | Right console — Lighting Panel | Rotary dimmer — red/white selectable |
| **Instrument Lights** | Right console — Lighting Panel | Rotary dimmer |
| **Console Lights** | Right console — Lighting Panel | Rotary dimmer (L/R console) |
| **Formation Lights** | Right console — Lighting Panel | Rotary dimmer — wing tip formation strips |
| **Position Lights (Nav)** | Right console — Lighting Panel | OFF / FLASH / STEADY, DIM / BRT |
| **Anti-Collision Light** | Right console — Lighting Panel | ON / OFF — red rotating beacon |
| **Landing Light** | Left main gear door | ON / OFF — extends with gear; switch on left console |
| **Taxi Light** | Nose gear | ON / OFF — switch on left console |

**Day/Night Procedures:**
- **Day:** Instrument/console lights OFF or low. Position lights FLASH (for traffic visibility). Landing light ON for takeoff/landing.
- **Night:** Cockpit flood to comfortable level (red preferred for night vision preservation). All exterior lights per local procedures. Formation lights for formation flying.

### 2.5 Instructor Notes

| Common Student Error | Correction |
|---|---|
| Overwhelmed by cockpit complexity — doesn't know where to look | Use a structured cockpit scan: start at left console top, sweep right across glareshield, down instrument panel, right console. Practice "blindfold cockpit" — student points to switch by name. |
| Leaving Master Arm in ARM after startup | Drill: Master Arm is ALWAYS SAFE unless actively attacking. BQT students should never have Master Arm in ARM. Build the habit early. |
| Not powering TGP early enough | TGP IR detector needs 3–5 minutes to cool. Set to STBY during avionics power-up. Transition to OPER after taxi. |
| Forgetting MFCD power-on (brightness knob) | MFCDs are OFF by default in cold-and-dark. Student must physically rotate brightness knob. Include in startup flow. |
| Confusing UFC steerpoint knob with radio knob | Left rotary = steerpoint, right rotary = radio channel. Label mentally during cockpit familiarization. |
| Not acknowledging Master Caution | Master Caution illuminates and stays on until pressed. Student must acknowledge AND check caution panel for the specific fault. Teach: "Acknowledge, Identify, Action." |

---

## Module 3: Ground Operations

### 3.1 Learning Objectives

- Student can perform a complete cold-and-dark to engines-running startup using cockpit switches (no autostart).
- Student can monitor ITT, N1, and N2 during engine start and identify abort criteria (hot start, hung start, no light-off).
- Student can complete the avionics power-on sequence including MFCDs, CDU, UFC, HMCS, TGP, and IFFCC.
- Student can perform an EGI alignment and verify navigation solution quality.
- Student can taxi the aircraft using NWS (HI and LO modes), differential braking, and appropriate taxi speeds.
- Student can complete pre-takeoff checks including SAS engagement, EAC arming, trim set, flaps, and warning panel clear.

### 3.2 Cold-and-Dark Startup Procedure

The following is the complete switch-by-switch startup sequence from a cold-and-dark cockpit. This is the **primary procedure** the student must master.

#### Phase 1: Battery & Electrical

| Step | Switch / Action | Location | Expected Indication |
|---|---|---|---|
| 1 | **Battery Switch** — ON | Left console — Electrical Panel | Battery bus powered; some caution lights illuminate |
| 2 | **Inverter Switch** — STBY | Left console — Electrical Panel | AC instruments begin receiving power |
| 3 | **Warning Light Test** — PRESS & HOLD | Glareshield — left of UFC | All caution/warning lights illuminate; verify none burned out |
| 4 | Release Warning Light Test | — | Only actual faults remain illuminated |

#### Phase 2: APU Start

| Step | Switch / Action | Location | Expected Indication |
|---|---|---|---|
| 5 | **APU Switch** — START (hold momentarily) | Left console — Electrical Panel | APU begins spooling; listen for turbine whine |
| 6 | Wait for APU RPM to stabilize | — | APU RPM gauge shows stable (~100%); APU GEN light available |
| 7 | **APU Generator** — PWR | Left console — Electrical Panel | APU generator online; electrical buses fully powered |

> *⚠ Realism Divergence: The real A-10C APU (GTCP36-150) requires approximately 30 seconds to reach operating speed and may require multiple start attempts in cold weather. DCS models a reliable APU start with appropriate spool time but does not simulate cold-weather starting difficulties or APU fuel consumption from the main tanks.*

#### Phase 3: Left Engine Start

| Step | Switch / Action | Location | Expected Indication |
|---|---|---|---|
| 8 | **Left Throttle** — ensure at IDLE (full aft) | Throttle quadrant | Throttle in IDLE detent |
| 9 | **Left Engine Operate Switch** — IGN (or MOTOR for dry motor) | Left console — Engine Panel | IGN engages igniter and starter |
| 10 | Monitor **Left N2** rising | Right instrument panel | N2 begins increasing from 0% |
| 11 | At **~12–15% N2** — advance **Left Throttle** past CUTOFF detent to IDLE | Throttle quadrant | Fuel introduced; ITT begins rising |
| 12 | Monitor **Left ITT** | Right instrument panel | ITT rises sharply, peaks, then settles — **must not exceed 860°C** |
| 13 | Monitor **Left N1** accelerating | Right instrument panel | N1 increases through 20%, 30%, 40%... |
| 14 | Engine stabilizes at IDLE | — | N1 ~62–65%, N2 ~60%, ITT 400–500°C, fuel flow ~600–800 lbs/hr, oil pressure 25–65 PSI |
| 15 | **Left Engine Operate Switch** — NORM | Left console — Engine Panel | Normal engine operation mode |

**Abort Criteria During Start:**
| Condition | Indication | Action |
|---|---|---|
| **Hot Start** | ITT exceeds 860°C and continues rising | Throttle to CUTOFF, Engine Operate to MOTOR (dry crank 30 sec to cool), retry |
| **Hung Start** | N2 stalls below 55%, ITT rising | Throttle to CUTOFF, Engine Operate to MOTOR, retry |
| **No Light-Off** | No ITT rise within 30 seconds of fuel introduction | Throttle to CUTOFF, Engine Operate to OFF, check fuel/ignition |
| **Low Oil Pressure** | Oil pressure below 15 PSI after idle stabilization | Shutdown engine, investigate |

#### Phase 4: Right Engine Start

| Step | Switch / Action | Location | Expected Indication |
|---|---|---|---|
| 16 | **Right Throttle** — ensure at IDLE | Throttle quadrant | In IDLE detent |
| 17 | **Right Engine Operate Switch** — IGN | Left console — Engine Panel | Same sequence as left engine |
| 18 | Monitor N2, introduce fuel at ~12–15% N2 | — | Same procedure as steps 10–14 |
| 19 | Right engine stabilizes at IDLE | — | Same parameters as left engine |
| 20 | **Right Engine Operate Switch** — NORM | Left console — Engine Panel | Normal operation |

#### Phase 5: Generators & APU Shutdown

| Step | Switch / Action | Location | Expected Indication |
|---|---|---|---|
| 21 | **Left Generator Switch** — PWR | Left console — Electrical Panel | Left generator online; supplies L bus |
| 22 | **Right Generator Switch** — PWR | Left console — Electrical Panel | Right generator online; supplies R bus |
| 23 | Verify both generators stable | — | No GEN caution lights |
| 24 | **APU Generator** — OFF | Left console — Electrical Panel | APU generator disconnected from bus |
| 25 | **APU Switch** — OFF | Left console — Electrical Panel | APU spools down and shuts off |

#### Phase 6: Post-Start Checks

| Step | Check / Action | Expected Indication |
|---|---|---|
| 26 | **Hydraulic Pressure A** — CHECK | 3,000 PSI ±200 |
| 27 | **Hydraulic Pressure B** — CHECK | 3,000 PSI ±200 |
| 28 | **Flight Control Check** — full deflection stick and rudder | Controls move freely; no binding |
| 29 | **Speed Brakes** — OPEN then CLOSE | Verify extension and retraction |
| 30 | **Flaps** — cycle MVR then UP | Verify movement; set for taxi |
| 31 | **Caution/Warning Panel** — CHECK | All faults cleared (or only expected items) |
| 32 | **Oxygen** — ON, 100%, NORMAL | Switches set (cosmetic in DCS) |
| 33 | **Anti-Skid** — ON | Left console — critical for braking |

> *⚠ Realism Divergence: In the real A-10C, the flight control check is performed with a crew chief observing surface deflections externally and confirming via intercom. In DCS, the pilot performs the check alone using external view (F2) or simply verifying stick/rudder forces feel correct. Additionally, the real A-10C has a detailed crew-chief / pilot challenge-response flow for the entire startup — DCS students perform all steps solo.*

### 3.3 Avionics Power-On Sequence

Avionics should be powered on in a specific order to allow systems to initialize properly.

| Step | System | Switch / Action | Location | Warm-Up Time |
|---|---|---|---|---|
| 1 | **CDU** | CDU Power — ON | Right console | ~30 sec self-test |
| 2 | **EGI** | EGI Switch — ON (via CDU or dedicated switch) | CDU NAV page | 3–8 min alignment |
| 3 | **UFC** | UFC Power — ON (powers with avionics master) | Glareshield | Immediate |
| 4 | **Left MFCD** | Brightness knob — rotate clockwise past detent | Left MFCD bezel | ~5 sec self-test |
| 5 | **Right MFCD** | Brightness knob — rotate clockwise past detent | Right MFCD bezel | ~5 sec self-test |
| 6 | **TGP** | AHCP TGP Switch — STBY | Left glareshield — AHCP | 3–5 min IR cooling |
| 7 | **HMCS** | AHCP HMCS Switch — ON | Left glareshield — AHCP | Immediate; boresight on ground |
| 8 | **IFFCC** | AHCP IFFCC Switch — TEST then ON | Left glareshield — AHCP | Self-test ~10 sec |
| 9 | **CMSP** | CMSP Switch — STBY then MAN | Left console — CMSP Panel | Immediate |
| 10 | **IFF** | Set Mode 3/C codes via UFC | UFC keypad | Per mission brief |
| 11 | **Radios** | Set frequencies via UFC | UFC keypad | COM1 (UHF), COM2 (VHF) |

### 3.4 EGI (Embedded GPS/INS) Alignment

The EGI must align before the navigation system provides accurate position data. This is one of the most critical ground procedures.

#### Alignment Types

| Type | Procedure | Time (DCS) | Time (Real) | Accuracy |
|---|---|---|---|---|
| **Full GC (Gyrocompass) Alignment** | Power on EGI, remain stationary, wait for alignment complete | ~3–5 min | 4–8 min | Best — full INS calibration |
| **Stored Heading Alignment** | EGI uses last-known heading + GPS | ~90 sec | 2–4 min | Good — faster, slightly less INS accuracy |
| **GPS Only (In-Flight)** | EGI uses GPS position without full INS alignment | Immediate | N/A | GPS-dependent — no inertial backup |

#### Full Alignment Procedure

| Step | Action | Indication |
|---|---|---|
| 1 | CDU powered ON, EGI switch ON | CDU displays NAV page — alignment status shows "ALIGN" |
| 2 | **Aircraft must be stationary** — do not taxi during alignment | Any movement degrades alignment quality |
| 3 | CDU shows alignment quality progressing | Alignment quality number decreases (lower = better) |
| 4 | CDU shows **"NAV"** or **"NAV READY"** | EGI alignment complete — position data valid |
| 5 | Verify GPS status on CDU NAV page | GPS satellites tracked, position accuracy displayed |

**Alignment Quality Check:**
- CDU NAV page shows alignment quality as a numeric value.
- Lower numbers = better alignment.
- A value of ≤ 1.0 is generally considered adequate for navigation.
- GPS augmentation significantly improves position accuracy even with a marginal INS alignment.

> *⚠ Realism Divergence: The real A-10C EGI (Honeywell H-764G) requires 4–8 minutes for a full gyrocompass alignment and is sensitive to vibration and movement during the process. DCS compresses alignment time to approximately 3–5 minutes. Additionally, the real EGI exhibits INS drift over time (requiring periodic GPS updates or TACAN cross-checks); DCS does not model INS drift — GPS position remains accurate indefinitely once aligned. Real-world stored heading alignment requires the pilot to manually enter the aircraft's parking heading; DCS automates this.*

### 3.5 Taxi Procedures

#### Nosewheel Steering (NWS)

| Mode | Engagement | Authority | Use |
|---|---|---|---|
| **NWS HI** | Press NWS button on stick (or `A` key) — default mode | ±60° | Tight turns, ramp maneuvering, parking |
| **NWS LO** | Press NWS button again to toggle | ±15° | Runway taxi, high-speed taxi, takeoff roll |
| **NWS OFF** | Release NWS; or paddle switch disengage | Rudder only | Flight operations; NWS auto-disengages at weight-off-wheels |

**NWS Button:** Located on the HOTAS stick grip — the same button used for air refueling disconnect (A/R). Short press toggles NWS HI/LO. The paddle switch (back of stick grip) disengages NWS entirely.

#### Taxi Procedure

| Step | Action | Notes |
|---|---|---|
| 1 | **Parking Brake** — RELEASE | `W` key or cockpit handle |
| 2 | **NWS** — engage HI for ramp maneuvering | Press NWS button on stick |
| 3 | Advance throttles slightly above idle | A-10C is heavy — may need moderate power to start rolling |
| 4 | **Brake Check** — within first 50 ft of rolling | Tap brakes to verify — both sides should decelerate evenly |
| 5 | Switch to **NWS LO** for taxiway | More stable at taxi speed |
| 6 | Maintain **10–15 kts** taxi speed | Standard USAF taxi speed; max 25 kts on straight taxiway |
| 7 | Use **differential braking** for tight turns if needed | Left brake = `Q`, Right brake = `E` (or toe brakes) |
| 8 | Monitor **anti-skid ON** | Prevents wheel lockup during braking |

**Taxi Speed Limits:**
| Condition | Max Speed |
|---|---|
| Ramp / Parking area | 10 kts |
| Taxiway (straight) | 25 kts |
| Taxiway (turns) | 10 kts |
| Congested area | 5 kts |

> *⚠ Realism Divergence: The real A-10C has a mechanical NWS linkage with HI/LO detent positions on the NWS button. DCS models the HI/LO toggle accurately. However, the real aircraft's nosewheel shimmy damper and differential braking feel are simplified in DCS — the sim tends to be more forgiving of aggressive nosewheel inputs than the real aircraft. Real A-10C pilots report that NWS HI is quite sensitive and easy to over-control; in DCS, this sensitivity depends on joystick curve settings.*

### 3.6 Pre-Takeoff Checks

Performed at the runway hold-short line or in the arming area.

| Check | Required State | How to Verify |
|---|---|---|
| **SAS Channels** | All engaged (Pitch, Yaw, Roll) | SAS panel — all switches ON, no SAS caution lights |
| **EAC** | Armed | SAS panel — EAC switch to ARM |
| **Trim** | Set for takeoff (0° pitch, 0° roll, 0° rudder) | Trim indicator on instrument panel; HUD trim caret centered |
| **Flaps** | 7° (MVR position) for standard takeoff | Flap switch to MVR; verify flap indicator |
| **Speedbrakes** | CLOSED | Speedbrake switch to CLOSE; no "SPEED BRAKE" caution |
| **Fuel** | Sufficient for mission | Fuel totalizer checked; crossfeed CLOSED |
| **EGI** | Aligned — NAV mode | CDU NAV page shows NAV READY; GPS OK |
| **Altimeter** | Set to field QNH | Kollsman window matches ATIS/tower altimeter setting |
| **Canopy** | Closed and locked | Canopy handle full forward; CANOPY warning light OUT |
| **Ejection Seat** | Armed | Seat safety pin removed; SEAT NOT ARMED light OUT |
| **Pitot Heat** | ON | Left console — ECS panel |
| **Exterior Lights** | Landing light ON, anti-collision ON | Left console and lighting panel |
| **Transponder/IFF** | Set per ATC | UFC — Mode 3/C set |
| **Caution/Warning Panel** | CLEAR | No amber or red indications |
| **NWS** | LO (for takeoff roll) | Toggle to LO before lineup |

### 3.7 Instructor Notes

| Common Student Error | Correction |
|---|---|
| Moving throttle to IDLE before N2 reaches 12–15% | Premature fuel introduction causes hot start. Drill: "Watch N2, wait for 12–15% before moving throttle." Have student call out N2 percentage verbally. |
| Forgetting to switch Engine Operate from IGN to NORM | Leaving in IGN wastes igniter life (irrelevant in DCS but builds bad habits). Include in the flow. |
| Taxiing in NWS HI on taxiways | NWS HI is too sensitive for straight-line taxi — causes S-turning. Switch to NWS LO after clearing the ramp. |
| Starting taxi before EGI alignment completes | EGI alignment degrades if aircraft moves. Emphasize: complete alignment before brake release. Plan startup timing to allow 3–5 min alignment. |
| Skipping the brake check after starting to roll | The brake check verifies anti-skid function and brake effectiveness. Make it mandatory in the first 50 feet. |
| Forgetting to set altimeter QNH before takeoff | Wrong altimeter setting = wrong altitude readout = potential CFIT. Drill: altimeter check is part of every pre-takeoff flow. |
| Not confirming SAS engagement before takeoff | Flying without SAS is survivable but degraded. SAS check must be a gate item — do not take the runway without all channels confirmed. |

---

## Module 4: Takeoff & Departure

### 4.1 Learning Objectives

- Student can perform a normal takeoff including lineup, throttle advance, directional control, rotation, gear retraction, and flap schedule.
- Student can execute a crosswind takeoff using appropriate technique within published limits.
- Student can perform a rejected takeoff (abort) using the correct boldface procedure.
- Student can fly the standard climb profile at appropriate speeds and power settings.
- Student can execute a standard VFR departure and overhead break entry.

### 4.2 Key Data

| Parameter | Value | Notes |
|---|---|---|
| **Rotation Speed (Vr)** | 135–150 KIAS | Weight dependent; average ~140 KIAS |
| **Liftoff Speed** | 150–160 KIAS | Weight dependent |
| **Gear Retraction** | After positive rate of climb confirmed | VSI positive, altimeter increasing |
| **Flap Retraction** | 200 KIAS | Retract from MVR (7°) to UP above 200 KIAS |
| **Climb Speed (Vy)** | 200–220 KIAS | Best rate of climb; clean configuration |
| **Climb Power** | Military (full throttle) | No afterburner — MIL is maximum |
| **Max Crosswind (Dry)** | 30 kts | Per AFMAN 11-2A-10C Vol 3 |
| **Max Crosswind (Wet)** | 20 kts | Wet or contaminated runway |
| **Max Tailwind** | 10 kts | Component |
| **Decision Speed (Abort)** | ~100 KIAS (rule of thumb) | No formal V1 — pilot judgment based on remaining runway |
| **Takeoff Flap Setting** | 7° (MVR) | Standard; 20° (DN) for short field |

### 4.3 Normal Takeoff Procedure

| Step | Action | Notes |
|---|---|---|
| 1 | **Lineup** — taxi onto runway centerline | Align nosewheel on centerline; verify runway heading matches HSI |
| 2 | **NWS** — LO or OFF | LO for directional control during roll; transitions to rudder |
| 3 | **Brakes** — HOLD (feet on pedals) | Hold brakes during power check if desired |
| 4 | **Throttles** — smoothly advance to FULL | `PgUp` or throttle axis; allow 2–3 seconds for spool-up |
| 5 | Verify **both engines responding** | Matched N1 rise; no split; no abnormal ITT |
| 6 | **Brakes** — RELEASE | Begin takeoff roll |
| 7 | **Directional control** — NWS and rudder | Rudder authority increases with speed; NWS less effective above 60 kts |
| 8 | **80 KIAS** — crosscheck instruments alive | Airspeed rising, engine instruments normal — last chance for low-speed abort |
| 9 | **Vr (135–150 KIAS)** — ROTATE | Smooth aft stick; pitch to ~10° nose up |
| 10 | **Liftoff** — weight off wheels | Positive rate confirmed on VSI and altimeter |
| 11 | **Gear** — UP | `G` key or gear handle in cockpit — verify 3 green lights extinguish |
| 12 | **Climb** — accelerate to 200 KIAS | Maintain runway heading or departure instructions |
| 13 | **200 KIAS** — **Flaps UP** | Retract from MVR to UP; verify flap indicator |
| 14 | Continue climb at **200–220 KIAS** | Best rate of climb speed (Vy) |

**Power Management:**
- The TF34 has no afterburner — Military (100%) is maximum power.
- Takeoff uses full military power. There is no throttle "gate" to push through.
- After gear and flaps are up and climbing at Vy, power can be reduced to ~90% N1 for noise/endurance if desired, but military power is acceptable for the entire climb.

### 4.4 Crosswind Takeoff Technique

| Phase | Technique |
|---|---|
| **Lineup** | Align on centerline; note wind direction (windsock, ATIS) |
| **Roll** | Apply into-wind aileron (wing down into wind); rudder to maintain centerline |
| **Rotation** | At Vr, rotate normally; aircraft may drift downwind — accept momentary drift |
| **Climb** | Establish wind correction angle (crab into wind) immediately after liftoff |
| **Limit** | Do not attempt takeoff with crosswind component exceeding 30 kts (dry) / 20 kts (wet) |

### 4.5 Rejected Takeoff (Abort)

This is a **BOLDFACE** procedure — the student must memorize it.

| Step | Immediate Action | Notes |
|---|---|---|
| 1 | **THROTTLES** — **IDLE** | Both throttles full aft |
| 2 | **WHEEL BRAKES** — **MAX** | Maximum pedal pressure; anti-skid provides modulation |
| 3 | **SPEED BRAKES** — **OPEN** | Increases drag; `B` key or cockpit switch |
| 4 | **JETTISON** — IF REQUIRED | Master Arm → ARM, Jettison Button — for overweight/fire scenarios |
| 5 | If fire: **FIRE HANDLE** — PULL (affected side) | Shuts off fuel and hydraulic to affected engine |

**Decision Criteria:**
- Any **engine failure, fire, or abnormality** before rotation speed → ABORT.
- After Vr / liftoff: abort only if unable to fly. Once airborne, commit to flying — the runway behind you is useless.
- **No formal V1:** Unlike airline operations, the A-10C does not publish a V1 speed. The pilot uses judgment based on remaining runway, speed, and the nature of the malfunction.

> *⚠ Realism Divergence: DCS models the abort sequence accurately including brake effectiveness and speed brake drag. However, DCS does not model tire blowouts from heavy braking, brake fade from heat, or the need for barrier engagement. The real A-10C can engage a tailhook-cable system on prepared runways — this is not modeled in DCS. Additionally, jettisoning stores in DCS is instantaneous; in reality, jettison racks have a brief sequencing delay.*

### 4.6 Climb Profile

| Phase | Speed | Power | Configuration | Pitch |
|---|---|---|---|---|
| **Initial Climb** (0–1,000 ft AGL) | Accelerating to 200 KIAS | Military | Gear UP, Flaps retracting | 10–15° |
| **Normal Climb** (above 1,000 ft AGL) | 200–220 KIAS | Military or reduced | Clean | 8–12° (as needed for speed) |
| **Level-Off** | Cruise speed (250–300 KIAS typical) | Reduce to cruise power | Clean | Smoothly lower nose; allow speed to build |

**Level-Off Technique:**
- Begin level-off approximately 10% of climb rate before target altitude (e.g., climbing at 2,000 fpm → begin level-off 200 ft before target altitude).
- Reduce pitch gradually, then reduce power as speed increases to cruise.
- Trim nose-down as speed builds — the A-10C requires constant trimming as speed changes.

### 4.7 Departure Procedures

| Type | Description |
|---|---|
| **Standard VFR Departure** | Climb on runway heading to 1,000 ft AGL, then turn on course per departure instructions or as directed by ATC |
| **Overhead Break Entry** | If returning to or arriving at a military airfield: approach at 350 KIAS, 1,500 ft AGL, overhead the runway — break with 60° bank turn to downwind. This is typically a recovery procedure (Module 8) but the student should understand it as a departure reference. |
| **Instrument Departure** | If departing IFR: follow published SID or radar vectors. Maintain climb speed and comply with altitude restrictions. |

### 4.8 Instructor Notes

| Common Student Error | Correction |
|---|---|
| Not advancing throttles smoothly — jerking to full | Smooth throttle advancement prevents N1 overshoot and gives time to check for engine anomalies. Teach: 2–3 second push from idle to MIL. |
| Rotating too early (before Vr) | Premature rotation increases drag and delays acceleration. The A-10C is heavy — it needs Vr to fly. Wait for the airspeed. |
| Forgetting to retract gear after positive rate | Gear creates massive drag — slows acceleration and climb. Drill: "Positive rate — gear up" as a verbal callout. |
| Not retracting flaps at 200 KIAS | Flaps above 200 KIAS = structural risk. Set a "flaps gate" at 200 KIAS in the student's scan. |
| Poor directional control during crosswind takeoff | Student over-corrects with rudder. Teach smooth, progressive inputs. NWS LO helps at low speed; transition to rudder by 60–80 kts. |
| Hesitating during abort decision | Abort decisions must be instantaneous below Vr. Any hesitation costs runway. Drill: practice aborts from various speeds on the first training sortie. |
| Climbing too steep (pitch > 15°) | Excessive pitch = low speed = approaching stall. The A-10C is underpowered relative to fighters — respect the climb schedule. 200 KIAS is the target, not a maximum pitch angle. |

---

## Module 5: Basic Flight Maneuvers

### 5.1 Learning Objectives

- Student can maintain level flight at various altitudes and airspeeds using appropriate power settings.
- Student can execute coordinated turns at 30°, 45°, and 60° bank while managing load factor and AoA.
- Student can perform climbs and descents at recommended profiles with AoA awareness.
- Student can fly slow flight with proper flap management and identify minimum controllable airspeed (VMCA).
- Student can recognize approach-to-stall indications using the AoA indexer and execute a prompt recovery.
- Student can demonstrate proper trim technique as speed and configuration change.
- Student can operate the speed brake and anticipate its pitch effects.

### 5.2 Key Data

| Parameter | Value | Notes |
|---|---|---|
| **Cruise Speed (Low Altitude)** | 250–300 KIAS | Typical tactical cruise below 10,000 ft |
| **Cruise Speed (Medium Altitude)** | 220–260 KIAS | 10,000–20,000 ft; power limited |
| **Cruise Power Setting** | 80–88% N1 | Altitude and weight dependent |
| **Max Level Speed** | ~380 KIAS (sea level) | Drag limited; rarely achieved in practice |
| **Flap Extension Speed (Vfe)** | 200 KIAS | Both MVR and DN positions |
| **MVR Flap Speed Range** | 150–200 KIAS | Used for maneuvering and pattern work |
| **DN Flap Speed Range** | Below 170 KIAS | Landing configuration |
| **Corner Speed** | 280–320 KIAS | Best instantaneous turn rate |
| **Max G (Clean)** | +7.33 / -3.0 G | Symmetric loading |
| **Max G (Loaded/Asym)** | +5.0 G | With external stores |
| **Stall Speed (Clean)** | ~130 KIAS | Weight dependent; ISA sea level |
| **Stall Speed (Dirty)** | ~110 KIAS | Gear/flaps down; weight dependent |

### 5.3 Level Flight

**Maintaining Altitude and Airspeed:**
- The A-10C is a subsonic, straight-wing aircraft. It is happiest at 250–300 KIAS at low to medium altitude.
- Power required increases significantly below 200 KIAS (back side of the power curve) and above 350 KIAS (drag rise).
- The pilot must continuously trim as fuel burns off and the CG shifts. The A-10C does NOT self-trim — SAS provides rate damping, not trim.

**Power Settings (Approximate):**

| Altitude | Speed | N1 (Approx) | Notes |
|---|---|---|---|
| Sea level | 250 KIAS | 82–85% | Light stores |
| Sea level | 300 KIAS | 88–92% | Near max level |
| 10,000 ft | 220 KIAS | 80–84% | Typical cruise |
| 10,000 ft | 280 KIAS | 88–92% | Fast cruise |
| 20,000 ft | 220 KIAS | 86–90% | Engines working harder in thin air |
| 20,000 ft | 250 KIAS | 92–96% | Near max level at altitude |

### 5.4 Turns

**Bank Angle vs. G-Load:**

| Bank Angle | G-Load | Stall Speed Increase | Notes |
|---|---|---|---|
| 30° | 1.15 G | +7% | Gentle maneuvering turn |
| 45° | 1.41 G | +19% | Standard tactical turn |
| 60° | 2.0 G | +41% | Aggressive; requires significant back pressure |
| 75° | 3.86 G | +97% | Very aggressive; nearing structural limits with stores |

**Coordinated Turn Technique:**
1. Roll to desired bank angle using ailerons.
2. Apply back pressure to maintain altitude — the steeper the bank, the more back pressure required.
3. Apply rudder coordination — ball centered on the slip/skid indicator.
4. With **SAS and EAC engaged**, turn coordination is largely automatic. Without EAC, the pilot must manually coordinate with rudder.
5. Monitor **AoA** — in steep turns, AoA increases. If AoA approaches buffet onset (~18 units), reduce bank angle or accept altitude loss.
6. Monitor **G-meter** — do not exceed +5.0 G with external stores, +7.33 G clean.

**Trim in Turns:**
- The A-10C requires nose-up trim in sustained turns to prevent altitude loss without excessive back pressure.
- In brief turns (< 30 seconds), manual back pressure is sufficient.
- In sustained orbits, add nose-up trim; remove it when rolling wings level.

### 5.5 Climbs & Descents

**Climb Profiles:**

| Type | Speed | Power | Use |
|---|---|---|---|
| **Best Rate (Vy)** | 200–220 KIAS | Military | Maximum altitude gain per minute |
| **Cruise Climb** | 250 KIAS | 90–95% N1 | En route climb; trades climb rate for forward speed |
| **Emergency Climb** | 200 KIAS | Military | After single-engine or emergency — max altitude for options |

**Descent Profiles:**

| Type | Speed | Power | Rate | Use |
|---|---|---|---|---|
| **Cruise Descent** | 250–300 KIAS | 80% N1 | ~1,500 fpm | Normal en route descent |
| **Penetration Descent** | 250 KIAS | Idle | ~3,000–4,000 fpm | Rapid altitude loss; speed brakes as needed |
| **Emergency Descent** | 300+ KIAS | Idle + speed brakes | Max rate | Depressurization / fire / smoke — get below 10,000 ft |

**AoA Awareness in Descents:**
- During idle-power descents, airspeed tends to increase. Monitor airspeed to avoid exceeding Vne (450 KIAS).
- During deceleration at altitude, AoA increases — monitor for unintended slow flight.
- Speed brakes cause a slight nose-down pitch change; trim as needed.

### 5.6 Slow Flight

**Purpose:** The student must understand the A-10C's handling characteristics at low airspeed, including flap management, minimum controllable airspeed, and SAS behavior.

**Flap Extension Schedule:**

| Speed | Flap Position | Notes |
|---|---|---|
| Above 200 KIAS | UP | No flaps; clean configuration |
| 200 KIAS | MVR (7°) available | Maneuver flaps; extend for pattern work, slow flight practice |
| Below 170 KIAS | DN (20°) available | Full flap; landing configuration |

**Slow Flight Procedure:**
1. **Altitude:** Minimum 5,000 ft AGL for practice.
2. **Configuration:** Gear UP, Flaps MVR (or DN for full slow flight).
3. Gradually reduce power and allow airspeed to decay.
4. At **~150 KIAS (MVR flaps)** — aircraft is in slow flight regime; back side of power curve.
5. Student maintains altitude by adding power — pitch attitude is relatively constant; speed is controlled by power.
6. **VMCA (Minimum Controllable Airspeed):** Approximately 120–125 KIAS in landing configuration. The aircraft remains controllable but sluggish; any further deceleration enters approach-to-stall.

**SAS Behavior at Low Speed:**
- SAS authority decreases as airspeed decreases (reduced control surface effectiveness).
- Yaw SAS may become less effective below 130 KIAS — pilot may notice increased yaw wander.
- EAC attitude hold becomes less precise at low speed.
- The aircraft remains controllable without SAS at slow speed, but workload increases significantly.

### 5.7 Approach-to-Stall

**AoA Indexer Progression:**

| Indexer Light | Symbol | AoA (Units) | Meaning | Pilot Action |
|---|---|---|---|---|
| Upper chevron (green) | ▲ | < 11 | Fast — below on-speed | Reduce power or raise nose |
| Green donut | ● | ~11 | On-speed — optimal approach | Maintain — this is the target |
| Lower chevron (amber) | ▼ | > 11, < 18 | Slow — above on-speed | Add power or lower nose |
| Stall warning (red) | ▼▼ | ~18–20 | Approaching stall — buffet onset | Immediate recovery action |
| Full stall | — | > 22 | Wing stall — nose drops | Full recovery procedure |

**Approach-to-Stall Practice:**

| Step | Action | Notes |
|---|---|---|
| 1 | Altitude: minimum 5,000 ft AGL | Recovery altitude margin |
| 2 | Clean configuration (or as assigned: flaps, gear) | Stall speed varies significantly with config |
| 3 | Reduce power to idle | Allow airspeed to decay |
| 4 | Maintain altitude with increasing pitch | AoA increases |
| 5 | **AoA Indexer:** observe green donut → lower chevron → buffet | Call out each indication verbally |
| 6 | At **buffet onset / stall warning** (~20 units) — **RECOVER** | Do NOT allow full stall unless demonstrating |

**Stall Recovery:**

| Step | Action |
|---|---|
| 1 | **Nose** — lower smoothly (reduce AoA) |
| 2 | **Throttles** — MILITARY (full power) |
| 3 | **Wings** — level (if in bank) |
| 4 | **Recover** — positive G, climbing, accelerating |
| 5 | **Altitude loss:** expect 200–500 ft depending on entry conditions |

> *⚠ Realism Divergence: DCS models A-10C stall characteristics accurately via the AFM. Buffet onset, progressive AoA increase, and nose-drop stall are well represented. However, the real aircraft has a stick shaker that physically vibrates the control column at stall onset — DCS relies on audio warning and visual AoA indexer only. Additionally, the real A-10C can exhibit asymmetric wing drop at stall with asymmetric stores; DCS models this but the effect may be less pronounced than in reality.*

### 5.8 Trim Technique

**The A-10C requires constant trimming.** This is one of the most important handling skills for the student to develop.

| Situation | Trim Requirement |
|---|---|
| Speed increase | Nose-down trim (aircraft pitches up as speed increases) |
| Speed decrease | Nose-up trim (aircraft pitches down as speed decreases) |
| Flap extension | Nose-up trim (flaps create pitch-down moment) |
| Flap retraction | Nose-down trim |
| Gear extension | Nose-up trim (slight) |
| Fuel burn-off | Trim changes as CG shifts — usually nose-down over time |
| Power change | Nose-up trim with power increase (engines are above CG) |
| Configuration change | Retrim after any configuration change |

**Electric Trim:**
- **Stick trim hat:** 4-way — pitch (fore/aft), roll (left/right)
- **Rudder trim:** Rotary knob on left console
- **Trim indicator:** On instrument panel — shows pitch and roll trim position

**Trim Philosophy:**
- The student should trim so that the aircraft flies the desired speed/attitude with **hands-off stick**.
- If the student is holding constant back or forward pressure, the aircraft is out of trim.
- SAS provides rate damping but does NOT trim the aircraft. EAC holds attitude but fights the pilot if the aircraft is poorly trimmed.

> *⚠ Realism Divergence: Electric trim in DCS functions identically to the real aircraft. One difference: the real A-10C has a manual trim tab on each elevator that provides a last-resort trim capability if electric trim fails. DCS models electric trim failure (requiring manual reversion) but the manual trim tabs are not independently adjustable — in DCS, manual reversion uses fixed trim settings. Real A-10C pilots set the manual trim tabs before flight via a ground adjustment.*

### 5.9 Speed Brake Operation

| Parameter | Detail |
|---|---|
| **Switch Location** | Left console — Flight Control Panel; also HOTAS speed brake switch |
| **Positions** | OPEN / CLOSE (switch); or proportional via HOTAS |
| **Effect** | Significant drag increase; moderate nose-down pitch tendency |
| **Speed Limit** | No specific limit — speed brakes are rated for all airspeeds up to Vne |
| **Keyboard** | `B` — toggle open/close |

**Pitch Effect:**
- Speed brake deployment causes a nose-down pitch change. The student must anticipate this and apply back stick / nose-up trim.
- Speed brake retraction causes a nose-up pitch change.
- In formation or close to the ground, these pitch transients can be hazardous — deploy/retract smoothly.

### 5.10 Instructor Notes

| Common Student Error | Correction |
|---|---|
| Not trimming — fighting the stick through every maneuver | Emphasize: if you're holding pressure, you're out of trim. Demonstrate: properly trimmed aircraft flies itself. Make trim a habit, not an afterthought. |
| Over-G with external stores | Clean limit is +7.33 G but loaded limit is +5.0 G. Student must know their configuration before maneuvering. Check loadout before every flight. |
| Pulling too hard in steep turns — entering buffet | Teach: bank angle determines G required. If buffeting, reduce bank or accept altitude loss. Do NOT pull through the buffet. |
| Failing to add power in turns to maintain altitude | In banked flight, more lift (and therefore more thrust) is needed. Teach: add power proportionally to bank angle. 60° bank needs roughly double the lift. |
| Not using AoA indexer during slow flight | The AoA indexer is the primary speed reference in the pattern and slow flight. Wean the student off the airspeed indicator for these regimes — "fly the indexer." |
| Surprise at speed brake pitch effect | Brief the student before first speed brake use. Demonstrate: deploy speed brakes in level flight, observe nose-down pitch; retract, observe nose-up pitch. Then practice smooth transitions. |
| Attempting to fight through a stall instead of recovering | Stall recovery must be instinctive: nose down, power up, wings level. Any hesitation costs altitude. Practice until it's reflexive. |

---

## Module 6: Navigation (Basic CDU/EGI)

### 6.1 Learning Objectives

- Student can select and navigate to steerpoints using the CDU and HUD steerpoint cue.
- Student can create a new steerpoint in the CDU by entering LAT/LONG or MGRS coordinates.
- Student can create a mark point capturing the aircraft's current position.
- Student can interpret the HSI (heading, course, bearing-to-steerpoint).
- Student can orient on the MFCD TAD display (own-ship, steerpoints, range scale).
- Student can set up TACAN (mode, channel) and interpret CDI and DME readouts.
- Student can configure an ILS approach via UFC frequency entry and monitor CDI/glideslope on the ADI.

### 6.2 Key Instruments & Displays

#### 6.2.1 HUD Navigation Symbology

| Symbol | Description | Notes |
|---|---|---|
| **Steerpoint Cue ("Tadpole")** | Small circle with tail indicating direction to active steerpoint | Fly toward the tadpole to navigate to steerpoint |
| **Distance Readout** | Nautical miles to active steerpoint | Digital readout on HUD |
| **Time/ETA Readout** | Estimated time to steerpoint | Based on current ground speed |
| **Heading Tape** | Current magnetic heading | Top of HUD |
| **Flight Path Marker (FPM)** | Shows where the aircraft is actually going | Accounts for wind drift |
| **Altitude** | Current barometric altitude | Right side of HUD |
| **Airspeed** | Current calibrated airspeed (KIAS) | Left side of HUD |

#### 6.2.2 HSI (Horizontal Situation Indicator)

| Element | Description |
|---|---|
| **Compass Rose** | Current magnetic heading under the lubber line |
| **Course Arrow** | Set course (manually or from CDU) |
| **CDI (Course Deviation Indicator)** | Shows lateral deviation from selected course — centered = on course |
| **Bearing Pointer** | Points toward active steerpoint (or TACAN station) |
| **DME Window** | Distance to TACAN station (when TACAN is active) |
| **To/From Flag** | Indicates whether flying toward or away from the selected course origin |

### 6.3 Steerpoint Navigation

#### 6.3.1 Selecting Steerpoints

| Method | Procedure |
|---|---|
| **UFC Steerpoint Knob** | Rotate the left rotary knob on the UFC to cycle through steerpoints. HUD cue updates immediately. |
| **CDU WPT Page** | Press `WPT` on CDU → use increment/decrement keys to select steerpoint → press `STEER` to activate. |
| **HOTAS DMS** | DMS Up/Down (if mapped) cycles active steerpoint. |

**HUD Steerpoint Cue Interpretation:**
- The tadpole symbol points from the steerpoint position toward the aircraft's current heading correction needed.
- When the tadpole is centered in the HUD and the tail points down, the aircraft is flying directly toward the steerpoint.
- Distance and ETA are shown digitally — the student should cross-reference these with the mission plan.

#### 6.3.2 Creating a Steerpoint in the CDU

| Step | Action | Notes |
|---|---|---|
| 1 | Press **`WPT`** on CDU | Enters waypoint management page |
| 2 | Navigate to an empty steerpoint number | Use page up/down or type steerpoint number |
| 3 | Select **coordinate format** | LAT/LONG (DD MM SS.S) or MGRS |
| 4 | Type coordinates using CDU keyboard | Enter latitude, press `ENTER`; enter longitude, press `ENTER` |
| 5 | Verify coordinates on CDU display | Cross-check against mission planning materials |
| 6 | Press **`STEER`** to navigate to the new steerpoint | HUD cue and HSI update |

**Coordinate Formats:**
| Format | Example | Notes |
|---|---|---|
| **LAT/LONG (DD MM SS.S)** | N 42° 21' 30.0" / E 043° 10' 15.0" | Standard geographic coordinates |
| **MGRS** | 38T LN 12345 67890 | Military Grid Reference System — common in tactical briefs |

#### 6.3.3 Mark Point Creation

| Step | Action | Notes |
|---|---|---|
| 1 | Fly over or near the point of interest | Aircraft GPS position will be captured |
| 2 | Press **MARK** function on CDU (or HOTAS if mapped) | Captures current aircraft position as a steerpoint |
| 3 | CDU assigns next available steerpoint number | Student can rename or verify coordinates |
| 4 | Use `STEER` to navigate back to the mark point | Useful for returning to a reference point |

### 6.4 MFCD TAD (Tactical Awareness Display)

The TAD is the primary moving-map navigation display.

| Element | Description |
|---|---|
| **Own-Ship Symbol** | Aircraft icon at center of display — shows current heading |
| **Steerpoints** | Numbered diamonds on the map — active steerpoint highlighted |
| **Course Line** | Line from current position to active steerpoint |
| **Range Scale** | Adjustable via OSB — typically 10, 20, 40, 80, 160 NM |
| **North Arrow** | Indicates map orientation (track-up or north-up) |
| **Heading/Track** | Digital readout of current heading and ground track |

**TAD Operation:**
| Action | Method |
|---|---|
| Select TAD page | MFCD HQ menu → TAD |
| Zoom in/out | OSBs on bottom edge — range scale buttons |
| Switch orientation | OSB for MAP orientation — track-up / north-up |
| Cursor (TDC) | Slew TDC to designate point of interest on map |
| Center on own-ship | Press own-ship OSB |

**BQT Scope:** The student should be able to orient on the TAD, identify own-ship position relative to steerpoints, and adjust the range scale. Threat rings, bullseye, and tactical overlays are out of scope for BQT.

### 6.5 TACAN

TACAN (Tactical Air Navigation) provides bearing and distance to a ground-based or air-based TACAN station.

| Parameter | Detail |
|---|---|
| **Panel Location** | Right console — TACAN Panel |
| **Modes** | T/R (Transmit/Receive — ground station), A/A (Air-to-Air — tanker or buddy), OFF |
| **Channel** | 3-digit channel number (1–126) + X or Y band |
| **CDI** | Course deviation on HSI — set desired course, CDI shows deviation |
| **DME** | Distance to station in nautical miles — displayed on HSI DME window |
| **Bearing** | Bearing pointer on HSI points toward station |

**TACAN Setup:**

| Step | Action | Notes |
|---|---|---|
| 1 | **TACAN mode** — set to T/R (ground station) or A/A (air) | Rotary switch on TACAN panel |
| 2 | **Channel** — dial desired channel | Tens and units knobs on TACAN panel |
| 3 | **Band** — X or Y | Toggle on TACAN panel |
| 4 | Verify **bearing pointer** on HSI points toward station | If no lock, check channel and range |
| 5 | Verify **DME** readout | Nautical miles to station; dashes if no lock |
| 6 | Set **course** on HSI to desired inbound course | CDI centers when on course |

**TACAN Use Cases in BQT:**
- Navigation to/from an airfield with a TACAN station.
- DME checks for position verification.
- Holding pattern reference (bearing and DME from a fix).
- Air-to-air TACAN for formation rejoin (A/A mode to flight lead).

> *⚠ Realism Divergence: DCS models TACAN with good fidelity — bearing, DME, and mode selection all work correctly. The primary simplification is that DCS TACAN stations have no terrain masking — the signal is always receivable if within range, regardless of intervening terrain. In reality, TACAN is line-of-sight and can be blocked by mountains. Additionally, DCS does not model TACAN station overload or interference.*

### 6.6 ILS Approach Setup

The A-10C can fly ILS (Instrument Landing System) approaches using the ADI localizer and glideslope needles.

| Step | Action | Notes |
|---|---|---|
| 1 | **Obtain ILS frequency** for destination runway | From approach plate, ATIS, or mission briefing |
| 2 | **UFC** — select NAV radio (ILS uses VHF NAV) | Press appropriate UFC option; some DCS airfields use specific ILS setups |
| 3 | **Enter ILS frequency** on UFC scratchpad | Type frequency → ENTER |
| 4 | **Set inbound course** on HSI | Rotate course knob to match published ILS course |
| 5 | **ADI** — verify localizer and glideslope bars appear | Horizontal bar = glideslope; vertical bar = localizer |
| 6 | **Fly the needles** — centered = on course and glideslope | Fly toward the needle deflection |

**ILS Approach Profile:**
| Phase | Altitude / Speed | Action |
|---|---|---|
| Intercept | 3,000 ft AGL, 8–10 NM | Established on localizer course, decelerating |
| Glideslope Capture | ~2,500 ft AGL | Glideslope bar begins moving down — follow it |
| Final Approach | Descending on 3° glidepath | 140 KIAS, gear down, flaps as needed |
| Decision Altitude | 200 ft AGL (typical) | Runway in sight → land; not in sight → go around |

> *⚠ Realism Divergence: DCS models ILS approaches at equipped airfields. The A-10C's ILS receiver and ADI needles function correctly. However, not all DCS airfields have ILS — check the mission editor or airfield data. The real A-10C can also fly TACAN approaches (non-precision) and GPS approaches via the CDU — DCS supports TACAN approaches but does not model GPS approach procedures (RNAV/LPV).*

### 6.7 Scope Limitation

This module covers **"how to get from A to B"** — basic steerpoint navigation, TACAN, and ILS approach procedures.

**Out of scope for BQT:**
- Mission planning (route construction, DMPI creation)
- Data Transfer Cartridge (DTC) loading
- Threat rings and tactical overlays on TAD/HSD
- Tactical navigation (terrain masking, pop-up points, IP-to-target runs)
- Offset aimpoint procedures
- RNAV / GPS approach procedures

These topics are covered in weapons employment and mission planning courses.

### 6.8 Instructor Notes

| Common Student Error | Correction |
|---|---|
| Chasing the steerpoint cue instead of flying a heading | Teach: note the bearing to the steerpoint, set that heading, and fly it. Small corrections, not constant chasing. The tadpole should be a reference, not a flight director. |
| Not verifying steerpoint coordinates after entry | Typos in coordinates lead to navigation errors. Drill: always re-read the CDU display after entering coordinates — verify against the source. |
| Confusing TACAN bearing with heading | TACAN bearing pointer shows the direction TO the station FROM the aircraft. It does NOT show the heading to fly — wind correction is required. Teach the difference between bearing and heading. |
| Forgetting to set ILS course on HSI | Without the correct course set, the CDI will show reverse sensing. Drill: frequency AND course — both must be set. |
| Over-reliance on GPS — no TACAN skills | GPS makes navigation easy, but TACAN is the backup. Practice TACAN-only navigation on at least one sortie. In combat, GPS can be jammed — TACAN provides an independent source. |
| Not adjusting TAD range scale appropriately | Students often leave TAD at 80 NM scale when they need 20 NM detail. Teach: adjust range scale for the current phase of flight. En route = 80 NM; terminal area = 20 NM; pattern = 10 NM. |

---

## Module 7: Emergency Procedures (Academic)

### 7.1 Learning Objectives

- Student can recite all **boldface (memory) items** verbatim: Abort, Engine Fire, Double Engine Failure, Manual Reversion, and Ejection.
- Student can identify and respond to a single engine failure including isolation, restart attempt, and single-engine approach.
- Student can identify and respond to hydraulic system failures (A, B, and dual) including manual reversion.
- Student can identify and respond to electrical failures including generator loss and battery-only operations.
- Student can describe fire detection and response for engine, APU, and electrical fires.
- Student can perform emergency landing gear extension.
- Student can state the ejection decision criteria and ACES II seat limitations.
- Student can distinguish which emergencies DCS models faithfully vs. those that are simplified or absent.

### 7.2 Boldface (Memory) Items

Per AFMAN 11-2A-10C Vol 3, these procedures must be committed to memory and executed without reference to a checklist. In training, the student must recite them verbatim on demand.

#### ABORT (Engine Failure/Fire on Takeoff)

| Step | Action |
|---|---|
| 1 | **THROTTLES** — **IDLE** |
| 2 | **WHEEL BRAKES** — **MAX** |
| 3 | **SPEED BRAKES** — **OPEN** |
| *(If fire exists:)* | |
| 4 | **FIRE HANDLE (Affected)** — **PULL** |
| 5 | **EXTINGUISHER SWITCH** — **FWD/AFT as required** |

#### ENGINE FIRE IN FLIGHT

| Step | Action |
|---|---|
| 1 | **THROTTLE (Affected Engine)** — **IDLE** |
| 2 | **FIRE HANDLE (Affected Engine)** — **PULL** |
| 3 | **EXTINGUISHER SWITCH** — **FWD/AFT as required** |
| 4 | **LAND ASAP** |

#### DOUBLE ENGINE FAILURE

| Step | Action |
|---|---|
| 1 | **THROTTLES** — **IDLE** |
| 2 | **APU SWITCH** — **START** (if below 15,000 ft) |
| 3 | **ENGINE OPERATE SWITCHES** — **IGN** |
| *(Proceed to crossbleed/APU restart logic)* | |

#### MANUAL REVERSION (Dual Hydraulic Failure)

| Step | Action |
|---|---|
| 1 | **FLIGHT CONTROLS** — **MAN REVERSION** (Pitch and Roll switches) |
| 2 | **Fly conservatively** — limited control authority |
| 3 | **LAND ASAP** — no flaps, emergency gear extension |

#### EJECTION

| Step | Action |
|---|---|
| 1 | **EJECTION HANDLE** — **PULL** |

### 7.3 Emergency Procedures Detail

#### 7.3.1 Single Engine Failure

**Identification:**
| Indication | Detail |
|---|---|
| Asymmetric thrust (yaw) | Aircraft yaws toward the dead engine |
| N1/N2 decaying on one engine | Affected engine instruments winding down |
| ITT anomaly | May spike (fire) or drop to zero (flameout) |
| Fire warning (if applicable) | T-handle light illuminates, audio warning |

**Response Procedure:**

| Step | Action | Notes |
|---|---|---|
| 1 | **Identify** — confirm which engine has failed | Cross-check N1, N2, ITT, fuel flow; yaw direction |
| 2 | **Maintain control** — rudder into the live engine | Prevent yaw departure |
| 3 | If fire: execute **Engine Fire** boldface | Pull fire handle, extinguisher |
| 4 | If no fire: **attempt restart** | |
| 4a | Throttle (dead engine) — IDLE | Ensure fuel is flowing |
| 4b | Crossfeed — OPEN | Allow dead engine to draw fuel from opposite wing |
| 4c | APU — START (if below 15,000 ft) | Provides bleed air for starter assist |
| 4d | Engine Operate (dead engine) — IGN | Engages igniter and starter |
| 4e | Monitor N2 and ITT | Same criteria as normal start |
| 5 | If restart fails: **secure the dead engine** | Throttle to CUTOFF |
| 6 | **Jettison stores** if needed for performance | Reduce weight and drag |
| 7 | **Navigate to nearest suitable field** | Fly single-engine approach (Module 8) |

**Single-Engine Flying Qualities:**
| Parameter | Detail |
|---|---|
| Controllability | Fully controllable; requires rudder trim into live engine |
| Max level speed | Reduced ~30%; approximately 250 KIAS at low altitude |
| Climb capability | Significantly reduced; may be unable to maintain altitude above 15,000 ft depending on weight |
| Approach speed | Add 15 KIAS to normal approach speed |
| Minimum Control Speed (Vmca) | ~120 KIAS — below this, directional control cannot be maintained |

#### 7.3.2 Hydraulic Failure

**System A Failure:**

| Symptom | Lost Capability | Retained Capability |
|---|---|---|
| HYD A pressure drops to 0 | Left elevator, left aileron, left rudder, NWS, normal brakes | Right-side hydraulic controls (System B); flight controls functional but degraded feel |

**System B Failure:**

| Symptom | Lost Capability | Retained Capability |
|---|---|---|
| HYD B pressure drops to 0 | Right elevator, right aileron, right rudder, speed brakes, utility functions | Left-side hydraulic controls (System A); flight controls functional but degraded feel |

**Dual Hydraulic Failure:**

| Step | Action | Notes |
|---|---|---|
| 1 | **MANUAL REVERSION** — engage (Pitch and Roll switches to MAN REVERT) | Left console — Flight Control Panel |
| 2 | Stick forces increase to **60–80 lbs** | Reduced control deflection rate |
| 3 | **No flaps** available | Landing in clean configuration |
| 4 | **No speed brakes** available | Higher approach speed; longer rollout |
| 5 | **No NWS** | Differential braking for directional control (emergency brakes only) |
| 6 | **Emergency gear extension** — required | Gravity drop system |
| 7 | Fly **wide, gentle pattern** | Avoid aggressive maneuvering — control authority is limited |
| 8 | Approach speed: **150–160 KIAS** (higher than normal due to no flaps) | Touchdown firmly; accept a firm landing |
| 9 | **Emergency brakes** — use carefully | Without anti-skid, braking is aggressive; tire blowout risk |

> *⚠ Realism Divergence: DCS fully models manual reversion including the increased stick forces (manifested as reduced control deflection rates). Emergency gear extension via gravity drop is modeled. However, DCS does not model the extreme physical fatigue that real pilots report during extended manual reversion flight — the 60–80 lbs of stick force is physically exhausting over more than a few minutes. Also, DCS does not model tire blowouts from emergency braking without anti-skid.*

#### 7.3.3 Electrical Failure

**Single Generator Loss:**

| Step | Action |
|---|---|
| 1 | GEN caution light illuminates (L or R) |
| 2 | Remaining generator picks up full load — no degradation normally |
| 3 | Monitor remaining generator — if it also fails, proceed to double gen failure |

**Double Generator Failure:**

| Step | Action | Notes |
|---|---|---|
| 1 | Both GEN caution lights illuminate | Non-essential bus sheds automatically |
| 2 | **APU** — START (if below 15,000 ft) | APU generator can power essential bus |
| 3 | If APU unavailable: **battery only** | ~30 minutes endurance |
| 4 | **Essential instruments only:** standby ADI, magnetic compass, engine instruments, fire warning | HUD, MFCDs, CDU, UFC — all lost |
| 5 | **Standby ADI** — UNCAGE | Pull knob to uncage — provides pitch and roll reference |
| 6 | **Navigate visually** to nearest field | No GPS, no TACAN, no ILS (unless APU restores power) |
| 7 | **Land ASAP** | Battery endurance is limited |

**Battery-Only Flight:**

| System | Available | Not Available |
|---|---|---|
| Standby ADI | ✓ | HUD |
| Magnetic compass | ✓ | HSI, CDU, UFC |
| Engine instruments | ✓ (most on essential bus) | MFCDs |
| Fire warning | ✓ | CMSP, IFF, radios (most) |
| Emergency bus items | ✓ | All non-essential bus items |
| UHF radio (emergency) | ✓ (if wired to essential bus) | Normal radio stack |

#### 7.3.4 Fire

**Engine Fire:**
- Detected by fire warning T-handle illumination (red light on glareshield) and audio tone.
- Response: Engine Fire boldface (throttle idle, fire handle pull, extinguisher).
- The fire handle shuts off fuel and hydraulic fluid to the affected engine and arms the extinguisher.
- The extinguisher switch (FWD/AFT) directs agent to the forward or aft section of the engine bay.

**APU Fire:**
| Step | Action |
|---|---|
| 1 | APU FIRE warning light illuminates |
| 2 | **APU Switch** — OFF |
| 3 | If fire persists: **APU fire extinguisher** — DISCHARGE |

**Electrical Fire:**
| Step | Action |
|---|---|
| 1 | Smoke or burning smell in cockpit |
| 2 | **Identify source** — check for sparking, melting panels |
| 3 | **Affected system** — OFF (if identifiable) |
| 4 | **Vent cockpit** — open canopy slightly or use bleed air (speed dependent) |
| 5 | If unable to isolate: **LAND IMMEDIATELY** |

> *⚠ Realism Divergence: DCS models engine fire detection and the fire handle / extinguisher system accurately. APU fire is modeled. Electrical fires are partially modeled — smoke in the cockpit can occur, but the detailed circuit-breaker isolation procedure is simplified since individual CBs are mostly non-functional in DCS. In reality, the pilot would systematically pull circuit breakers to isolate the source; in DCS, turning off the suspected system is the best available action.*

#### 7.3.5 Landing Gear Emergency

**Normal Gear Extension:**
- Gear handle DOWN; hydraulic pressure extends gear; 3 green lights indicate down-and-locked.

**Emergency Gear Extension (Gravity Drop):**

| Step | Action | Notes |
|---|---|---|
| 1 | **Gear handle** — DOWN | Attempt normal extension first |
| 2 | If no 3 green lights: **Emergency gear extension handle** — PULL | Located on left console or lower instrument panel |
| 3 | Gear drops under gravity | May take 10–15 seconds to fully extend and lock |
| 4 | Verify **3 green lights** | If any gear unsafe: fly-by tower for visual confirmation |
| 5 | If gear does not lock: prepare for **gear-up landing** | Foam runway if available; minimize touchdown speed |

**Gear-Unsafe Indications:**
| Indication | Meaning |
|---|---|
| Red "unsafe" light | Gear in transit — not fully up or down |
| Missing green light(s) | Affected gear leg not locked down |
| Gear warning horn | Sounds when throttle is below threshold with gear up — indicates configuration warning |

#### 7.3.6 Controlled Ejection

**ACES II Ejection Seat:**

| Parameter | Value | Notes |
|---|---|---|
| **Seat Type** | ACES II (Advanced Concept Ejection Seat) | Zero-zero capable (0 speed, 0 altitude) |
| **Min Altitude (Level Flight)** | 0 ft | Zero-zero capability |
| **Min Altitude (Dive)** | 2,000 ft AGL | Below 2,000 ft in a dive = insufficient time for parachute |
| **Min Altitude (Inverted)** | 6,000 ft AGL | Seat must right itself — needs altitude |
| **Max Speed** | 450 KIAS | At or below Vne |
| **Activation** | Pull ejection handle between legs | DCS: `LCtrl + E` (hold 1 second) or 3× press |

**Ejection Decision Criteria:**
- **Eject if:** Aircraft is uncontrollable, on fire with fire spreading, structural failure imminent, or unable to maintain safe altitude.
- **Do NOT delay** ejection below minimum altitude. The decision to eject should be made early — altitude is life.
- **Before ejection (if time permits):** transmit MAYDAY with position, jettison canopy (auto in ACES II sequence), tighten harness, assume position (head back, elbows in).

> *⚠ Realism Divergence: DCS models the ACES II seat with zero-zero capability. Ejection is survivable at all modeled speeds and altitudes consistent with real-world data. The automatic sequencing (canopy jettison → seat fire → drogue → main chute) is modeled as a single event. DCS does not model ejection injuries (spinal compression, windblast, tumble injuries) that are common in real-world ejections, nor does it model the post-ejection survival aspects (parachute landing, survival radio, rescue).*

### 7.4 DCS Emergency Modeling Summary

| Emergency | DCS Fidelity | Notes |
|---|---|---|
| Engine failure (single) | ✅ High | Accurate — asymmetric thrust, restart procedure works |
| Engine fire | ✅ High | Fire detection, T-handle, extinguisher all modeled |
| Double engine failure | ✅ High | APU restart, windmill restart both work |
| Hydraulic failure (single) | ✅ High | Degraded controls accurately modeled |
| Dual hydraulic / manual reversion | ✅ High | Heavy stick forces (reduced rate) modeled |
| Generator failure (single) | ✅ Moderate | Bus behavior correct; no load shedding detail |
| Double generator failure | ✅ Moderate | Battery-only flight works; standby instruments available |
| Engine fire extinguisher | ✅ High | FWD/AFT agent selection modeled |
| Electrical fire | ⚠ Low | Smoke modeled; CB isolation not possible |
| Emergency gear extension | ✅ High | Gravity drop works correctly |
| Gear-up landing | ✅ Moderate | Aircraft slides; damage modeled; no foam runway |
| ACES II ejection | ✅ High | Zero-zero; survivable per real-world envelope |
| Tire blowout | ❌ Not modeled | DCS does not simulate tire failures |
| Bird strike | ⚠ Low | Engine damage from birds not specifically modeled |
| Compressor stall | ❌ Not modeled | TF34 rarely stalls in reality; not simulated |
| Fuel leak (combat) | ✅ High | Fuel quantity decreases from damaged tanks |
| Structural failure | ⚠ Low | Wings can separate from extreme damage/G; limited modeling |

### 7.5 Instructor Notes

| Common Student Error | Correction |
|---|---|
| Cannot recite boldface from memory | Boldface is non-negotiable. Student must recite perfectly before flying. Quiz at the start of every brief until it's second nature. Incorrect boldface = no fly. |
| Hesitating during single-engine identification | The aircraft yaws toward the dead engine — that's the instant cue. Teach: "dead foot, dead engine." Rudder pressure tells you which side failed. |
| Forgetting to open crossfeed during single-engine ops | Without crossfeed, the dead engine's wing tank fuel is inaccessible to the running engine. Eventually, the running engine starves. Drill: "Engine failure — crossfeed OPEN" as part of the immediate response. |
| Panicking during manual reversion | Manual reversion is flyable but requires calm, deliberate inputs. Demonstrate at altitude first. Practice until the student can fly a pattern and land in manual reversion. |
| Delaying ejection decision | "Eject, eject, eject" is a command, not a suggestion. If the student is wrestling with an uncontrollable aircraft below 2,000 ft, they've already waited too long. Teach the decision altitude concept: below X altitude, if the situation isn't improving, eject. |
| Over-fixating on emergency procedures and neglecting to fly the aircraft | Priority: Aviate → Navigate → Communicate → Troubleshoot. The aircraft must be under control before running any checklist. Drill: "First fly the airplane." |

---

## Module 8: Traffic Pattern & Landing

### 8.1 Learning Objectives

- Student can fly a VFR overhead break pattern (350 KIAS initial, 60° break, downwind, base, final).
- Student can fly a straight-in approach with proper speed schedule and configuration timing.
- Student can use the AoA indexer as the primary approach speed reference (green donut = on-speed).
- Student can maintain a 3° glidepath using visual aim point and PAPI/VASI references.
- Student can execute the A-10C "flat attitude" landing technique with proper flare and touchdown.
- Student can perform rollout procedures: aerodynamic braking, wheel braking, and speed brake deployment.
- Student can execute a go-around / missed approach from any point in the pattern.
- Student can perform a crosswind landing using wing-low or crab technique.

### 8.2 Key Data

| Parameter | Value | Notes |
|---|---|---|
| **Overhead Break Entry** | 350 KIAS, 1,500 ft AGL | Parallel to runway, same direction as landing |
| **Break Turn** | 60° bank, idle power | Decelerates rapidly in the turn |
| **Downwind Speed** | 200 KIAS | Gear and flaps in this leg |
| **Downwind Altitude** | 1,500 ft AGL | Standard USAF pattern altitude |
| **Gear Extension Speed** | ≤ 200 KIAS | 3 green lights; gear warning horn silences |
| **Flap Extension** | MVR (7°) at 200 KIAS; DN (20°) below 170 KIAS | As needed; DN for full stop landing |
| **Base Turn** | 30° bank | Begin when runway threshold is 45° behind the wing |
| **Final Approach Speed** | 130–140 KIAS | **AoA Indexer: green donut = on-speed** |
| **On-Speed AoA** | ~11 units | Green donut; this is the primary reference |
| **Touchdown Speed** | ~120 KIAS | Firm touchdown acceptable |
| **Go-Around** | Full power, positive rate, gear up | Flaps to MVR, accelerate, re-enter pattern |
| **Max Crosswind (Landing)** | 30 kts (dry), 20 kts (wet) | Same as takeoff limits |

### 8.3 VFR Overhead Break Pattern

```
                    ═══════════════════════════════════════
                    RUNWAY (Landing Direction →)
                    ═══════════════════════════════════════
                    
                    ┌─── Initial (350 KIAS, 1,500 ft AGL) ───→
                    │
                    │  BREAK POINT (abeam approach end)
                    │    ↓ 60° bank, idle power
                    │
        Base ←──────┤  Downwind (200 KIAS, gear down, flaps)
        (30° bank)  │    ← ← ← ← ← ← ← ← ← ← ← ← ←
                    │
                    │
               Final Approach (130-140 KIAS, green donut)
                    │
                    ↓
                 TOUCHDOWN (~120 KIAS)
```

#### Pattern Procedure

| Phase | Action | Speed / Config | Altitude |
|---|---|---|---|
| **Initial** | Approach parallel to runway, same direction as landing | 350 KIAS, clean | 1,500 ft AGL |
| **Break** | Abeam approach end: 60° bank turn (direction per traffic pattern), idle power | Decelerating | Maintain 1,500 ft |
| **Downwind** | Roll out on downwind heading, parallel to runway, opposite direction | 200 KIAS | 1,500 ft AGL |
| **Gear** | **Gear DOWN** | ≤ 200 KIAS | 1,500 ft AGL |
| **Flaps** | **MVR** (7°) initially; **DN** (20°) when below 170 KIAS and established | Decelerating to 150 | 1,500 ft AGL |
| **Downwind Checks** | Gear: 3 green. Flaps: set. Fuel: checked. Speed brake: closed. | 150 KIAS | 1,500 ft AGL |
| **Base Turn** | When runway threshold is 45° behind the wing: 30° bank turn | 140–150 KIAS | Begin descent |
| **Final** | Roll out aligned with runway centerline | 130–140 KIAS | Descending on ~3° glide path |
| **Short Final** | AoA indexer = green donut; aim point = 1,000 ft markers | 130–135 KIAS | ~200–300 ft AGL |
| **Flare** | Minimal flare — reduce rate of descent | ~125 KIAS | 10–20 ft |
| **Touchdown** | Main gear first, firm touchdown acceptable | ~120 KIAS | 0 ft |

### 8.4 Straight-In Approach

Used for instrument approaches, low traffic, or fuel-critical situations.

| Phase | Action | Speed / Config |
|---|---|---|
| **10 NM** | Established on final approach course | 200 KIAS, clean |
| **8 NM** | Begin deceleration | Reducing power |
| **6 NM** | **Gear DOWN**, **Flaps MVR** | 200 KIAS |
| **5 NM** | **Flaps DN** if full-stop landing | 170 KIAS, descending |
| **3 NM** | On glidepath, on-speed | 130–140 KIAS; green donut |
| **1 NM** | Short final — stabilized | 130 KIAS; constant descent rate |
| **Threshold** | Minimal flare, touchdown | ~120 KIAS |

### 8.5 Final Approach — AoA Indexer Reference

**The AoA indexer is the PRIMARY approach speed reference for the A-10C.** The pilot should fly the indexer, not the airspeed indicator, during the final approach phase.

| Indexer Indication | AoA | Meaning | Correction |
|---|---|---|---|
| **Upper Chevron (▲)** only | < 8 units | FAST | Reduce power; accept slight deceleration |
| **Upper Chevron + Donut** (▲●) | 8–10 units | Slightly fast | Minor power reduction |
| **Green Donut (●)** only | ~11 units | **ON-SPEED** | Maintain — this is the target |
| **Donut + Lower Chevron** (●▼) | 12–14 units | Slightly slow | Add power smoothly |
| **Lower Chevron (▼)** only | 15–18 units | SLOW | Add significant power; do NOT raise nose further |
| **Lower Chevron flashing** | > 18 units | DANGEROUSLY SLOW | Go around if on final; full stall recovery if not |

**Approach Speed vs. Weight:**
- The green donut corresponds to approximately 11 units AoA regardless of weight.
- The KIAS at which green donut illuminates varies with weight:
  - Light (35,000 lbs): ~125 KIAS
  - Medium (40,000 lbs): ~130 KIAS
  - Heavy (45,000 lbs): ~140 KIAS
- This is why the AoA indexer is superior to a fixed target speed — it automatically adjusts for weight.

### 8.6 Glidepath Management

| Reference | Description |
|---|---|
| **Visual Aim Point** | 1,000 ft markers (large white rectangles on runway) — maintain a constant visual depression angle to these |
| **3° Glidepath** | Standard — approximately 300 ft/NM descent rate |
| **PAPI (Precision Approach Path Indicator)** | 4 lights beside runway: 2 red / 2 white = on path; 3+ red = low; 3+ white = high |
| **VASI** | Similar to PAPI; "red over white = you're all right" |
| **HUD Flight Path Marker (FPM)** | Place the FPM on the aim point — this gives a direct glidepath indication |
| **Descent Rate** | At 130 KIAS approach speed: approximately 600–700 ft/min descent rate for 3° path |

### 8.7 Flare & Touchdown

**The A-10C uses a "flat attitude" landing technique:**

| Phase | Technique | Notes |
|---|---|---|
| **50 ft** | Maintain approach attitude and speed | Do NOT pull back yet |
| **20 ft** | Begin minimal flare — slight back stick | Just enough to arrest descent rate |
| **10 ft** | Continue slight flare; power to idle | Smoothly retard throttles |
| **Touchdown** | Main gear contacts first | A firm touchdown is normal and acceptable |
| **Nose gear** | Lower nose gently after main gear contact | Do NOT slam the nose down; controlled lower |

**Key Points:**
- The A-10C is NOT a "grease it on" airplane. Its rugged landing gear is designed for firm touchdowns on austere surfaces.
- Do NOT attempt to hold the aircraft off the runway — this leads to floating, ballooning, and potential porpoising.
- Touch down **on the centerline, at the aim point**, with the correct speed. Precision matters more than smoothness.

### 8.8 Rollout Procedures

| Step | Action | Notes |
|---|---|---|
| 1 | **Nose up** — hold back stick for aerodynamic braking | Increases drag at higher rollout speeds |
| 2 | **Speed brakes** — OPEN | `B` key or cockpit switch; adds significant drag |
| 3 | At **100 KIAS** — nose lower gently | Transition from aero braking to wheel braking |
| 4 | **Wheel brakes** — progressively apply | `W` key or toe brakes; anti-skid provides modulation |
| 5 | Maintain **centerline** with rudder/NWS | NWS re-engages when NWS button pressed after landing |
| 6 | Decelerate to **taxi speed** (~15 kts) | Clear the runway at the first available taxiway |

**Brake Management:**
- Anti-skid is critical — ensures maximum braking without wheel lockup.
- Do NOT pump the brakes — apply steady, progressive pressure and let anti-skid modulate.
- Speed brakes are the most effective decelerator above 100 KIAS; wheel brakes are most effective below 80 KIAS.
- Brake fade is possible with heavy sustained braking (not modeled in DCS but a real-world concern).

### 8.9 Go-Around / Missed Approach

**Execute a go-around from any point in the approach where a safe landing is not assured.**

| Step | Action | Notes |
|---|---|---|
| 1 | **THROTTLES** — **FULL (Military)** | Smooth but immediate; accept 4–6 sec spool-up |
| 2 | **Pitch** — arrest descent, establish positive rate | Do NOT pitch up aggressively — accelerate first |
| 3 | **Positive rate confirmed** — **GEAR UP** | `G` key; reduce drag |
| 4 | **Flaps** — MVR | Retract from DN to MVR; improves acceleration |
| 5 | **Accelerate** to 200 KIAS | Clean up |
| 6 | **Flaps** — UP (above 200 KIAS) | Fully clean |
| 7 | **Re-enter pattern** or fly missed approach procedure | Climb to pattern altitude; re-enter on downwind |

**Go-Around Decision Criteria:**
- Not stabilized by 200 ft AGL (speed, glidepath, or lineup not corrected)
- AoA indexer showing lower chevron flashing (dangerously slow)
- Runway incursion (vehicle, aircraft, animal on runway)
- Windshear (sudden airspeed loss or altitude deviation)
- Pilot uncertainty — **if in doubt, go around.** There is always another approach.

> *⚠ Realism Divergence: DCS models go-around performance accurately — the 4–6 second spool-up lag is present, and the pilot must anticipate the power application. One difference: in the real world, go-arounds in the A-10C pattern are common and expected; tower controllers anticipate them. In DCS single-player, there is no penalty for going around, but the student should practice communicating the go-around call ("Tower, [callsign], going around") to build habits for multiplayer.*

### 8.10 Crosswind Landing

| Technique | Description | When to Use |
|---|---|---|
| **Crab** | Fly the approach crabbed into the wind (offset heading); kick out the crab with rudder just before touchdown | Works well in moderate crosswinds; less physical effort |
| **Wing-Low (Sideslip)** | Lower the upwind wing to prevent drift; use opposite rudder to maintain runway alignment | Continuous correction; more precise; preferred for strong crosswinds |
| **Combination** | Crab on approach, transition to wing-low in the flare | Most common technique; balances workload |

**Crosswind Landing Procedure:**

| Phase | Action |
|---|---|
| **Final Approach** | Establish crab angle into the wind; maintain centerline track |
| **Short Final (100 ft)** | Transition to wing-low: lower upwind wing, opposite rudder for alignment |
| **Flare** | Maintain wing-low; touch down on upwind main gear first |
| **Touchdown** | Upwind main gear → both mains → nose gear; firm touchdown acceptable |
| **Rollout** | Aileron into wind, rudder/NWS for centerline; be prepared for weathervaning |

**Crosswind Limits:**

| Surface Condition | Max Crosswind Component |
|---|---|
| Dry runway | 30 kts |
| Wet runway | 20 kts |
| Icy / Contaminated | 15 kts (use extreme caution) |

### 8.11 DCS Autostart Reference

> **Note:** BQT students must learn the manual startup and landing procedures. However, the student should understand what DCS autostart does, because they may encounter it in multiplayer or training scenarios.
>
> **DCS Autostart (`LAlt + Home`):** Automatically executes the full startup sequence. The student should recognize that autostart:
> - Skips EGI alignment wait (alignment runs in background)
> - May not set radios or IFF to mission-specific frequencies
> - Does not teach cockpit interaction skills
> - Is acceptable for quick mission entry but NOT for BQT evaluation

### 8.12 Instructor Notes

| Common Student Error | Correction |
|---|---|
| Entering the break too slow or too fast | 350 KIAS is the target. Too slow = not enough energy for the break turn. Too fast = overshoots downwind. Brief the student on the energy management concept. |
| Not configuring in time on downwind | Gear and flaps must be down before the base turn. If not configured, extend downwind — do not rush. Teach: "configure on downwind or go around." |
| Chasing the airspeed indicator on final instead of using AoA indexer | The AoA indexer IS the approach speed reference. Wean the student off the airspeed indicator for final approach. Tape over the airspeed indicator during training if needed. |
| Aggressive flare — ballooning | The A-10C needs minimal flare. Aggressive pull leads to ballooning, float, and potential hard landing on the second contact. Teach: "fly it onto the runway." |
| Not using speed brakes on rollout | Speed brakes are the primary decelerator above 100 KIAS. Deploy immediately after touchdown. Make it part of the landing flow: "mains on — speed brakes open." |
| Landing long (past the aim point) | If the aim point is moving up in the windscreen, the pilot is high. Correct early or go around. Do NOT try to "save" a high approach by diving at the runway. |
| Hesitating on go-around decision | Go-arounds must be immediate and decisive. Any delay costs altitude and options. Teach: "The decision to go around is ALWAYS correct. The decision to force a bad landing is SOMETIMES fatal." |
| Excessive bank on base turn — stall/spin risk | Base turn is 30° bank maximum. Higher bank + low speed + low altitude = classic base-to-final stall accident. This is the most dangerous point in the pattern. Hammer this home. |

---

## Module 9: Shutdown

### 9.1 Learning Objectives

- Student can perform post-landing taxi procedures including canopy operations, light configuration, and taxi to parking.
- Student can execute the full shutdown procedure from engines running to cold-and-dark.
- Student can perform the avionics power-down in the correct sequence.

### 9.2 Post-Landing Taxi

| Step | Action | Notes |
|---|---|---|
| 1 | **Clear the runway** at first available taxiway | Maintain taxi speed; do not stop on the runway |
| 2 | **Speed Brakes** — CLOSE | Retract after cleared of runway |
| 3 | **Flaps** — UP | Retract after clearing runway |
| 4 | **NWS** — engage HI | For ramp maneuvering |
| 5 | **Landing Light** — OFF | After clearing runway |
| 6 | **Taxi Light** — ON (if needed) | For ramp visibility |
| 7 | **Transponder / IFF** — STBY | No longer needed after landing |
| 8 | Taxi to assigned parking spot | Maintain 10 kts in ramp area |
| 9 | Align on parking marks / follow marshaller | Chocks and ground crew available |

### 9.3 Shutdown Procedure

The following is the complete switch-by-switch shutdown from engines running to cold-and-dark.

#### Phase 1: Parking & Securing

| Step | Switch / Action | Location | Notes |
|---|---|---|---|
| 1 | **Parking Brake** — SET | Cockpit handle or `W` key | Aircraft stationary; chocks in place if available |
| 2 | **Canopy** — OPEN (if desired) | Canopy handle aft | Ground operations in warm weather |
| 3 | **Ejection Seat** — SAFE | Insert ground safety pin | Prevents inadvertent ejection during ground ops |

#### Phase 2: Avionics Power-Down

Power down avionics in reverse order of power-on.

| Step | System | Switch / Action | Location |
|---|---|---|---|
| 4 | **CMSP** | CMSP Switch — OFF | Left console — CMSP Panel |
| 5 | **HMCS** | AHCP HMCS Switch — OFF | Left glareshield — AHCP |
| 6 | **TGP** | AHCP TGP Switch — OFF | Left glareshield — AHCP |
| 7 | **IFFCC** | AHCP IFFCC Switch — OFF | Left glareshield — AHCP |
| 8 | **Master Arm** | Verify SAFE | Left glareshield — AHCP |
| 9 | **IFF** | IFF — OFF / STBY | Right console — IFF Panel |
| 10 | **Right MFCD** | Brightness knob — OFF (rotate fully counterclockwise) | Right MFCD bezel |
| 11 | **Left MFCD** | Brightness knob — OFF (rotate fully counterclockwise) | Left MFCD bezel |
| 12 | **CDU** | CDU Power — OFF | Right console |
| 13 | **UFC** | Will lose power with avionics bus | Glareshield |
| 14 | **Exterior Lights** | All OFF (position, anti-collision, taxi, formation) | Right console — Lighting Panel + left console |
| 15 | **Cockpit Lights** | All OFF | Right console — Lighting Panel |
| 16 | **Pitot Heat** | OFF | Left console — ECS Panel |

#### Phase 3: Engine Shutdown

| Step | Switch / Action | Location | Expected Indication |
|---|---|---|---|
| 17 | **Left Throttle** — IDLE (hold 30 sec for cool-down) | Throttle quadrant | N1 at idle ~62%; ITT stabilizes |
| 18 | **Left Throttle** — CUTOFF (pull past IDLE detent to CUTOFF) | Throttle quadrant | Fuel cut; N1 and ITT begin decaying |
| 19 | Monitor **Left N1** spooling down | Right instrument panel | N1 decreasing; allow full spool-down |
| 20 | **Right Throttle** — IDLE (hold 30 sec for cool-down) | Throttle quadrant | Same as left |
| 21 | **Right Throttle** — CUTOFF | Throttle quadrant | Fuel cut; N1 and ITT decaying |
| 22 | Monitor **Right N1** spooling down | Right instrument panel | N1 decreasing to 0 |
| 23 | Wait for **both engines** N1 < 20% | — | Engines are effectively stopped |

> *⚠ Realism Divergence: In the real A-10C, the engines should be allowed to idle for approximately 2 minutes before shutdown to allow turbine cooling, particularly after high-power operations. In DCS, the cooling period is not necessary — the engine can be shut down immediately without damage. However, a brief cool-down (30 seconds) is included in this procedure to build proper habits.*

#### Phase 4: Electrical Shutdown

| Step | Switch / Action | Location | Expected Indication |
|---|---|---|---|
| 24 | **Left Generator** — OFF | Left console — Electrical Panel | Left bus de-energized |
| 25 | **Right Generator** — OFF | Left console — Electrical Panel | Right bus de-energized |
| 26 | **Inverter** — OFF | Left console — Electrical Panel | AC instruments lose power |
| 27 | **Oxygen** — OFF | Right console — Oxygen Panel | Supply lever OFF |
| 28 | **Battery** — OFF | Left console — Electrical Panel | All power removed; cockpit goes dark |

**Aircraft is now cold-and-dark.**

### 9.4 Quick-Reference Shutdown Flow

For experienced students, the shutdown can be summarized as:

```
PARKING BRAKE — SET
AVIONICS — ALL OFF (CMSP, HMCS, TGP, IFFCC, IFF, MFCDs, CDU)
LIGHTS — ALL OFF
PITOT HEAT — OFF
THROTTLES — IDLE (cool-down) → CUTOFF
GENERATORS — OFF
INVERTER — OFF
BATTERY — OFF
```

### 9.5 Instructor Notes

| Common Student Error | Correction |
|---|---|
| Shutting down engines before powering down avionics | Avionics should be powered down before engine shutdown. Cutting engines first causes an abrupt power loss to avionics, which in reality can cause uncommanded stores release or system faults. In DCS it's harmless, but the habit is wrong. |
| Forgetting to set parking brake before shutdown | The aircraft will roll if on a slope. Always set parking brake first. Make it the first item in the shutdown flow. |
| Leaving Master Arm in ARM during shutdown | Master Arm must be SAFE before any ground operations. Verify SAFE as part of the avionics power-down sequence. This is a safety-critical habit. |
| Rushing the shutdown — skipping the cool-down | While DCS doesn't penalize a hot shutdown, the real procedure includes a turbine cool-down period. Teach the proper sequence even though DCS is forgiving. |
| Not safing the ejection seat | In real operations, the ground safety pin must be inserted before any maintenance or ground crew approach. In DCS, this is cosmetic, but mentioning it reinforces the mindset. |

---

## Appendix: Master V-Speed & Limits Reference

| Parameter | Value | Source |
|---|---|---|
| Vr (Rotation) | 135–150 KIAS | T.O. 1A-10C-1, weight dependent |
| Vy (Best Climb) | 200–220 KIAS | T.O. 1A-10C-1 |
| Vfe (Flap Limit) | 200 KIAS | T.O. 1A-10C-1 |
| Vlo (Gear Limit) | 200 KIAS | T.O. 1A-10C-1 |
| Vne (Never Exceed) | 450 KIAS | T.O. 1A-10C-1 |
| Vs (Stall, Clean) | ~130 KIAS | Weight dependent |
| Vs (Stall, Dirty) | ~110 KIAS | Gear/flaps down, weight dependent |
| Vmca (Min Control, Single Engine) | ~120 KIAS | Approximate |
| Approach (On-Speed) | 130–140 KIAS | AoA Indexer green donut (~11 units) |
| Corner Speed | 280–320 KIAS | Best instantaneous turn rate |
| Max G (Clean) | +7.33 / -3.0 | T.O. 1A-10C-1 |
| Max G (Loaded) | +5.0 | With external stores |
| Max Crosswind (Dry) | 30 kts | AFMAN 11-2A-10C Vol 3 |
| Max Crosswind (Wet) | 20 kts | AFMAN 11-2A-10C Vol 3 |
| Max Tailwind | 10 kts | AFMAN 11-2A-10C Vol 3 |
| Max Mach | M 0.75 | Drag limited |
| ITT Start Limit | 860°C | Abort if exceeded |
| ITT Max Continuous | 810°C | Normal ops |
| ITT Transient | 900°C | 5-minute limit |
| N1 Max | 98% | Fan speed |
| N2 Max | 99% | Core speed |
| APU Max Altitude | 15,000 ft | Start or emergency power |
| Battery-Only Endurance | ~30 min | Non-essential bus shed |

---

## Appendix: Cockpit Panel Quick Locator

| Panel / System | Location |
|---|---|
| Battery, APU, Generators, Inverter | Left console — Electrical Panel |
| Fuel Pumps, Crossfeed | Left console — Fuel Panel |
| Pitot Heat, Anti-Ice, Defog | Left console — ECS Panel |
| SAS, EAC, Autopilot | Left console — SAS Panel |
| Manual Reversion, Flaps, Speed Brake | Left console — Flight Control Panel |
| Engine Operate (IGN/MOTOR/NORM) | Left console — Engine Panel |
| CMSP | Left console — CMSP Panel |
| Throttle Quadrant | Left console, aft-lower |
| CDU | Right console — forward |
| Lighting Controls | Right console — Lighting Panel |
| TACAN | Right console — TACAN Panel |
| IFF | Right console — IFF Panel |
| Oxygen | Right console — Oxygen Panel |
| UFC | Glareshield — center |
| AHCP (Master Arm, TGP, IFFCC, etc.) | Glareshield — left |
| CMSC (RWR Display) | Right of right MFCD |
| Fire T-Handles | Glareshield — above instrument panel |
| Master Caution | Left of UFC |
| Left MFCD | Instrument panel — left |
| Right MFCD | Instrument panel — right |
| ADI, HSI, Altimeter, Airspeed | Center instrument panel |
| Engine Gauges (ITT, N1, N2, FF, Oil) | Lower instrument panel |
| Hydraulic Gauges | Lower right instrument panel |
| Fuel Totalizer | Center lower instrument panel |
| AoA Indexer | Left canopy rail |
| Standby ADI | Right glareshield |
| Magnetic Compass | Windshield frame |

---

*Research compiled from T.O. 1A-10C-1, AFMAN 11-2A-10C Vol 3, Eagle Dynamics DCS A-10C II Flight Manual, and publicly available USAF training materials. For DCS World simulation use only.*
