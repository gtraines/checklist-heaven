# Research Dossier: A-10A Basic Qualification Training (BQT)

> **Aircraft:** Fairchild Republic A-10A Thunderbolt II
> **Course Level:** Basic Qualification (Level 100)
> **Reference:** T.O. 1A-10A-1 Flight Manual / DCS Flaming Cliffs 3 Module
>
> **DCS Module Note:** The A-10A is a **Flaming Cliffs 3 (FC3)** simplified-systems module. It has NO clickable cockpit — all systems are controlled via keyboard bindings. However, it uses the **Advanced Flight Model (AFM)**, so aerodynamic behavior (stalls, spins, G-limits, flight envelope) is realistic.
>
> **Correction Note:** This dossier replaces a prior version that contained inaccuracies. All numerical data has been cross-checked against T.O. 1A-10A-1 (publicly available excerpts), General Electric TF34 engine specifications, and verified DCS FC3 module behavior. Where the prior dossier contained errors, they have been corrected and noted.

## Overview

This dossier provides the technical research foundation for a Basic Qualification Training course in the DCS A-10A Thunderbolt II. The course covers all phases of flight from cold-and-dark startup through safe recovery. **Combat employment (weapons delivery, CAS tactics) is out of scope** — those topics are covered in a separate Weapons Employment course.

The A-10A was designed from the outset as a close air support platform built around the GAU-8/A 30mm cannon. Its twin TF34-GE-100 high-bypass turbofan engines provide excellent loiter time and fuel efficiency at low altitude. The airframe is legendarily survivable, with redundant flight controls, self-sealing fuel tanks, and a titanium "bathtub" protecting the cockpit. These design features directly affect how the aircraft handles and how pilots must manage emergencies.

**Primary Real-World Sources:**
- T.O. 1A-10A-1 (A-10A Flight Manual / Dash-1)
- T.O. 1A-10A-34-1-1 (Non-Nuclear Weapons Delivery Manual — systems context only)
- AFMAN 11-2A-10 Vol. 3 (A-10 Operations Procedures)
- AFMAN 11-217 (Instrument Flying Procedures)
- General Electric TF34-GE-100/100A engine specifications

---
## Module 1 — Aircraft Systems & Aerodynamics

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Describe the TF34-GE-100 turbofan engine characteristics including spool-up time, thrust output, and operating limitations.
2. Explain the A-10A fuel system layout, feed sequence, and low-fuel indications.
3. Describe the dual-redundant hydraulic flight control system and explain manual reversion procedures.
4. Identify the A-10A survivability features and explain their operational implications.
5. Recognize stall onset using the AOA indexer and describe departure/spin characteristics.

---

### 1.1 Powerplant — TF34-GE-100 Turbofan (×2)

The A-10A is powered by two General Electric TF34-GE-100 high-bypass turbofan engines mounted in nacelles on the upper rear fuselage, widely separated by the airframe. This placement protects the engines from ground fire ingestion and foreign object damage, while the wide spacing increases survivability (a single hit is unlikely to damage both engines).

#### Engine Parameters & Limitations

| Parameter | Value | Notes |
|---|---|---|
| **Engine Type** | GE TF34-GE-100 High-Bypass Turbofan | 6.2:1 bypass ratio; very quiet, efficient at low altitude |
| **Thrust (per engine)** | 9,065 lbf (40.32 kN) | Sea level static; total installed thrust: 18,130 lbf |
| **No Afterburner** | MIL power is maximum available | Students from fighter backgrounds must adjust expectations |
| **Spool-Up Time** | ~4–6 seconds (idle to MIL) | Relatively fast for a turbofan; plan power changes ahead regardless |
| **Ground Idle RPM** | ~55–60% N2 | Slightly higher in flight idle |
| **Max N2** | 100% | MIL power; no afterburner stage |
| **EGT Limit (Starting)** | ≤ 725°C (1,337°F) | Abort start if exceeded ("hot start") |
| **EGT Limit (Continuous)** | ≤ 650°C (1,202°F) | Normal sustained operating max |
| **EGT Limit (Transient)** | ≤ 690°C (1,274°F) | Allowed during acceleration for ≤ 10 seconds |
| **Oil Pressure (Normal)** | 25–65 PSI | Varies with RPM and temperature |
| **Oil Pressure (Min)** | 15 PSI | Below 15 PSI = caution; 0 PSI = shutdown engine |
| **Fuel Flow (Cruise, both engines)** | ~1,800–2,200 lbs/hr | Mid-altitude, economical cruise |
| **Fuel Flow (Low-Alt, MIL power)** | ~3,000–3,500 lbs/hr | Full power, low altitude operations |

> *⚠ Prior Dossier Correction: The previous dossier listed EGT start limit as 649°C (1,200°F) and continuous limit as 607°C (1,125°F). These were understated. Per TF34 engine specifications and T.O. excerpts, the start limit is 725°C and continuous limit is approximately 650°C. DCS FC3 does model hot starts — a rising EGT that exceeds the start limit will abort/damage the engine.*

#### Engine Start Cycle

1. **Normal start (DCS FC3):** Electrical power ON → press engine start key → RPM begins rising → EGT rises (peaks, then settles) → RPM stabilizes at ground idle (~55–60% N2). In DCS FC3, this is a single-keybind operation per engine.
2. **Real-world start sequence (for reference):** Battery/GPU → APU/JFS start → throttle from OFF to IDLE at specified RPM gate → monitor EGT on dedicated gauge → oil pressure rising → stable idle. DCS simplifies this to a single key press.
3. **Spool-up characteristics:** The TF34 responds relatively quickly (~4–6 seconds idle to MIL), but students must still anticipate power needs, especially on approach and during go-arounds.
4. **Engine shutdown:** In DCS FC3, use the engine stop keybind. The throttle must be at idle before shutdown.

> *⚠ Realism Divergence: In the real A-10A, engine start requires APU/JFS operation, specific throttle positions at RPM gates, and monitoring of individual instruments. DCS FC3 abstracts this to a single keybind per engine. The simulation does model hot starts and hung starts, but the pilot cannot intervene with cockpit switches — only by using the engine stop keybind.*

---

### 1.2 Fuel System

| Parameter | Value | Notes |
|---|---|---|
| **Internal Fuel** | ~10,700 lbs (~1,600 US gal) | Two main wing tanks + fuselage feeder cells |
| **External Tanks** | 2 × 600 US gal (optional) | Wing stations 3 and 9 |
| **Fuel Type** | JP-8 (JP-4 alternate) | Standard USAF |
| **Low Fuel Warning** | ~1,500 lbs remaining | Caution light on annunciator panel |
| **Bingo Fuel** | Mission dependent | Typical training bingo: 2,500–3,000 lbs for RTB |
| **Feed Sequence** | Wing tanks → fuselage cells (automatic) | Crossfeed valve available for balancing |
| **Fuel Dump** | **Not available** | No fuel dump capability; burn off or jettison stores |

**Self-Sealing Tanks:** Internal fuel tanks are filled with reticulated polyurethane foam and are self-sealing, designed to survive 23mm HEI hits. DCS models fuel leaks from combat damage.

> *⚠ Realism Divergence: Real A-10A pilots manage fuel balance via a cockpit crossfeed switch and monitor individual tank quantities. In DCS FC3, fuel management is simplified — the system auto-feeds and the pilot sees only total fuel remaining on the HUD.*

---

### 1.3 Flight Control System

| System | Description |
|---|---|
| **Primary** | Dual-redundant hydraulic (Left + Right systems, 3,000 PSI each) |
| **Backup** | Manual reversion — direct mechanical linkage to all flight control surfaces |
| **Control Surfaces** | Ailerons, elevators, twin rudders, split speed brakes |
| **Trim** | Electric pitch, roll, and rudder trim (functions even in manual reversion) |
| **Flaps** | Three positions: UP / MVR (Maneuver, 7°) / DN (Down, 20°) |
| **Speed Brakes** | Split surfaces on aft fuselage; extend symmetrically; very effective with minimal pitch change |

**Manual Reversion:** The A-10A is one of the few modern combat aircraft that can be flown with BOTH hydraulic systems completely failed. In manual reversion, direct mechanical linkages connect the stick and pedals to the flight control surfaces. Stick forces increase dramatically (estimated 60–80 lbs or more), but the aircraft remains controllable. Pitch trim still functions electrically, providing critical assistance.

**Dual Hydraulic Independence:** Each hydraulic system powers one side of the flight controls independently. Loss of one system still provides full-authority hydraulic control on the intact side, with degraded (mechanically linked) control on the failed side. This is a key survivability feature.

> *⚠ Realism Divergence: DCS models increased control sluggishness and reduced authority when hydraulics fail but cannot simulate the physical force required. Students with force-feedback sticks may notice some change; others will notice only response lag.*

---

### 1.4 Survivability Features

| Feature | Description | Operational Impact |
|---|---|---|
| **Titanium Bathtub** | ~1,200 lb titanium alloy enclosure around cockpit | Protects pilot from ground fire up to 23mm; significant CG contribution |
| **Redundant Flight Controls** | Dual hydraulic + manual reversion | Fly-home capability with catastrophic battle damage |
| **Redundant Engines** | Wide-spaced nacelles, separated by fuselage | Single engine loss = controllable asymmetric flight; wide spacing means a single hit rarely kills both |
| **Self-Sealing Fuel** | Foam-filled, self-sealing tanks | Reduces fire/explosion risk |
| **ACES II Ejection Seat** | Zero-zero capable | Safe ejection from 0 altitude / 0 airspeed |
| **Triple-Redundant Structures** | Overlapping spars and skins in wing and tail | Aircraft can sustain major structural damage and remain flyable |

---

### 1.5 Stall Characteristics

| Parameter | Value | Notes |
|---|---|---|
| **Stall Warning (Buffet Onset)** | ~18–20 AoA units | Light buffet; indexer shows amber UP chevron |
| **Full Stall** | ~23–25 AoA units | Nose drops; possible wing rock or yaw if uncoordinated |
| **Stall Speed (Clean, light)** | ~130 KIAS | Increases significantly with stores and higher weight |
| **Stall Speed (Dirty, light)** | ~110 KIAS | Gear and flaps down, light weight |
| **Departure Susceptibility** | Low | Straight-wing design is inherently stall-resistant |
| **Spin Characteristics** | Recoverable | Standard recovery: idle / neutral stick / opposite rudder; typically 1–2 turns |

**AOA Indexer:** Three-light system mounted on the left canopy bow:

| Display | Meaning | Action |
|---|---|---|
| **○ (Green donut)** | On-speed (correct approach AoA) | Maintain — this is the target |
| **△ (Amber chevron UP)** | Slow / high AoA | Add power; lower nose slightly |
| **▽ (Amber chevron DOWN)** | Fast / low AoA | Reduce power; allow slight pitch up |
| **△ + ○** | Slightly slow | Small power addition |
| **▽ + ○** | Slightly fast | Small power reduction |

> *⚠ Realism Divergence: The real A-10A has a physical AOA indexer mounted on the canopy frame plus an AOA gauge on the instrument panel, plus an aural tone that increases in pitch with AoA. DCS FC3 presents AOA indexer information on the HUD overlay. The thresholds and behavior are the same — only the presentation differs.*

---

### 1.6 Aircraft Dimensions & Weight Summary

| Parameter | Value |
|---|---|
| **Wingspan** | 57 ft 6 in (17.53 m) |
| **Length** | 53 ft 4 in (16.26 m) |
| **Height** | 14 ft 8 in (4.47 m) |
| **Empty Weight** | ~24,960 lbs (11,321 kg) |
| **Max Takeoff Weight (MTOW)** | ~50,000 lbs (22,680 kg) |
| **Max Landing Weight** | ~42,000 lbs (19,050 kg) recommended; 46,000 lbs structural |
| **Max External Stores** | ~16,000 lbs on 11 pylons |
| **Wing Area** | 506 ft² (47.0 m²) |
| **Wing Loading (MTOW)** | ~99 lbs/ft² | 

---

### Module 1 — DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Throttle Up** | `Num +` (or HOTAS axis) | Both engines simultaneously |
| **Throttle Down** | `Num -` (or HOTAS axis) | Both engines simultaneously |
| **Left Engine Start** | `RAlt + Home` | |
| **Right Engine Start** | `RCtrl + Home` | |
| **Left Engine Stop** | `RAlt + End` | |
| **Right Engine Stop** | `RCtrl + End` | |
| **Flaps Up** | `LShift + F` | Cycles: DN → MVR → UP |
| **Flaps Down** | `LCtrl + F` | Cycles: UP → MVR → DN |
| **Speed Brakes Open** | `LShift + B` | |
| **Speed Brakes Close** | `LCtrl + B` | |
| **Speed Brakes Toggle** | `B` | Toggles between open/closed |
| **Pitch Trim Up** | `RCtrl + ;` | |
| **Pitch Trim Down** | `RCtrl + .` | |
| **Roll Trim Left** | `RCtrl + ,` | |
| **Roll Trim Right** | `RCtrl + /` | |
| **Rudder Trim Left** | `RCtrl + Z` | |
| **Rudder Trim Right** | `RCtrl + X` | |

---

### Module 1 — Instructor Notes

| Topic | Guidance |
|---|---|
| **"The Hog Doesn't Hurry"** | Emphasize from Day 1 that the A-10A is a slow, deliberate aircraft. Max speed is ~380 KTAS at sea level. Students from fighter backgrounds will struggle with the pace. Frame this as an advantage: more time to think, observe, and plan. |
| **Engine Response** | Unlike turbojets, the TF34 high-bypass turbofan spools relatively quickly (~4–6 sec idle-to-MIL). This is a significant safety advantage on approach, but students should still anticipate power needs rather than react to them. |
| **Trim Discipline** | The A-10A has NO fly-by-wire augmentation, no SAS, no CAS. Every speed, configuration, and power change requires re-trimming. Students who "fight the stick" fly imprecise profiles and fatigue quickly. "If you are holding steady pressure for more than 5 seconds — trim it out." |
| **AOA Indexer Reliance** | Teach approaches by AOA indexer, not by airspeed alone. Airspeed varies with weight; the AOA indexer always shows the correct energy state. |
| **FC3 Cockpit Abstraction** | The most significant divergence is the simplified cockpit. Real A-10A pilots interact with hundreds of switches, circuit breakers, and panels. DCS FC3 reduces this to keyboard shortcuts. All procedural steps that reference "switch to ON" = "press the assigned keybind." |
| **INS/NAV System** | The real A-10A uses an AN/ASN-141 INS requiring 4–8 minutes of ground alignment. DCS FC3 provides instant navigation on power-up. |

---

## Module 2 — Ground Operations & Startup

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Execute a cold-and-dark to engines-running startup using DCS FC3 keybinds.
2. Identify all startup-sequence caution indications and respond appropriately.
3. Perform proper taxi procedures including nosewheel steering and brake management.
4. Execute run-up checks before takeoff.

---

### 2.1 Cold-and-Dark Startup Sequence

The A-10A FC3 startup is heavily simplified compared to the real aircraft. In reality, the A-10A requires APU start, specific throttle sequencing at RPM gates, INS alignment (4–8 minutes), avionics sequencing, and extensive panel checks. In DCS FC3, this is condensed to a series of keybind presses.

#### Phase 1 — Electrical Power

| Step | Action | Key | Expected Result |
|---|---|---|---|
| 1 | Electrical Power ON | `RShift + L` | Master caution clears; avionics begin powering up; HUD comes alive |

> *Note: In DCS FC3, `RShift + L` activates the "Electrics" system, which simulates turning on battery/generator power. This powers all avionics, HUD, and radios simultaneously.*

#### Phase 2 — Engine Start (Left Engine First)

| Step | Action | Key | Expected Result |
|---|---|---|---|
| 2 | Start Left Engine | `RAlt + Home` | N2 RPM begins rising; EGT rises to a peak then settles |
| 3 | **Monitor EGT** | Observe HUD/instruments | EGT must stay below 725°C during start; if exceeded → HOT START |
| 4 | Wait for stable idle | — | N2 settles ~55–60%; EGT settles below 650°C; oil pressure shows 25–65 PSI |

#### Phase 3 — Engine Start (Right Engine)

| Step | Action | Key | Expected Result |
|---|---|---|---|
| 5 | Start Right Engine | `RCtrl + Home` | Same as left engine; monitor EGT |
| 6 | **Monitor EGT** | Observe | Same limits: peak below 725°C; stabilize below 650°C |
| 7 | Wait for stable idle | — | Both engines at ground idle; all cautions clear |

#### Phase 4 — Post-Start Checks

| Step | Action | Key | Expected Result |
|---|---|---|---|
| 8 | Verify both engines running | Check HUD engine display | Both N2 ~55–60%; EGT < 650°C |
| 9 | Navigation system ready | — | DCS FC3: NAV available immediately (no INS alignment needed) |
| 10 | Set altimeter (QNH/QFE) | `RAlt + Num+` / `RAlt + Num-` | Match field elevation on HUD altimeter |
| 11 | Set radar altimeter | Automatic in FC3 | Functions below 5,000 ft AGL |
| 12 | SAS / Autopilot modes available | Various | AP will not engage below a minimum speed |

> *⚠ Prior Dossier Correction: The previous dossier did not clearly distinguish between real-world and DCS FC3 startup. Real A-10A startup takes 5–10 minutes including INS alignment and sequential panel checks. DCS FC3 startup takes approximately 60–90 seconds total.*

> *⚠ Realism Divergence: The real A-10A startup sequence includes: External power/battery → APU start → APU stable → Throttle(s) OFF to IDLE at ~15% N2 → monitor EGT/oil/N2 → repeat for second engine → APU shutdown → INS alignment (4+ minutes) → avionics panel sequencing → BIT checks → radio setup. DCS FC3 eliminates all of this complexity.*

---

### 2.2 Hot Start Recognition & Response

A "hot start" occurs when EGT exceeds the start limit (725°C) during the engine start sequence, indicating the engine is over-temperature.

| Situation | Action |
|---|---|
| **EGT exceeding 725°C during start** | Immediately press engine stop keybind (`RAlt + End` for left / `RCtrl + End` for right) |
| **After abort:** | Wait 30–60 seconds for engine to cool before re-attempting start |
| **Repeated hot starts** | Possible fuel control issue; in DCS, try restarting once more; if it fails again, return to mission planning |

> *⚠ Realism Divergence: In the real A-10A, hot starts can be caused by APU bleed duct failures, fuel control scheduling problems, or high ambient temperatures. The pilot has physical fuel shutoff, ignition cutoff, and fire extinguisher options. DCS FC3 abstracts this — the pilot can only stop and restart the engine.*

---

### 2.3 Taxi Procedures

#### Nosewheel Steering (NWS)

| Parameter | Value | Notes |
|---|---|---|
| **NWS Authority** | ±45° (primary mode) | Sufficient for all taxiway turns |
| **NWS Control** | Rudder pedals (or rudder axis) | Automatic in FC3 when on the ground |
| **Differential Braking** | Available | Use for tight turns when NWS authority is insufficient |
| **Taxi Speed** | 10–15 knots recommended | Do not exceed 20 knots; no ATC ground speed displays |

> *⚠ Prior Dossier Correction: The previous dossier listed NWS authority as ±60°. The real A-10A has approximately ±45° of NWS authority in the primary steering mode. ±60° is achievable only through differential braking or castered free-wheeling (NWS off).*

#### Taxi Technique

1. **Advance throttle slightly** — just enough to begin rolling. The A-10A is relatively light on the nosewheel; do not apply excessive power.
2. **Use symmetric braking** to modulate speed. Riding brakes while applying power wastes fuel and heats brakes.
3. **Check brakes** — immediately after beginning to taxi, test both brakes to confirm function.
4. **Steer with rudder pedals** — smooth inputs; avoid rapid reversals at speed.
5. **Plan ahead for turns** — at 10–15 knots, the aircraft responds reasonably to NWS; wider turns are more comfortable.
6. **Monitor wingtips** — the A-10A wingspan is 57.5 ft; be aware of obstacles, other aircraft, and taxiway edges.

---

### 2.4 Before-Takeoff Checks

Perform these checks after reaching the runway hold-short line and before entering the active runway:

| # | Item | Action | Notes |
|---|---|---|---|
| 1 | **Brakes** | SET (hold) | |
| 2 | **Flight Controls** | Full deflection all axes — confirm movement | Visual check: use external view (`F2`) to verify surfaces |
| 3 | **Trim** | Set for takeoff (neutral or slightly nose-up) | |
| 4 | **Flaps** | Set as required (typically UP for normal takeoff; MVR for short-field) | `LCtrl + F` to extend |
| 5 | **Speed Brakes** | Verify CLOSED | `LCtrl + B` to ensure closed |
| 6 | **Altimeter** | Set and confirmed | Match field elevation |
| 7 | **Fuel** | Check quantity; confirm sufficient for mission | |
| 8 | **Canopy** | Closed and locked | `LCtrl + C` |
| 9 | **Engine Instruments** | Both engines: N2 ~55–60%, EGT < 650°C, oil pressure normal | |
| 10 | **Ejection Seat** | Armed | In real aircraft — DCS does not model this as a separate step |

---

### 2.5 Brake System

| Parameter | Value | Notes |
|---|---|---|
| **Normal Brakes** | Hydraulic, toe pedals | `W` key in DCS FC3 (applies both) |
| **Parking Brake** | Set/release | `LCtrl + W` in DCS FC3 |
| **Anti-Skid** | Modeled in DCS | Prevents flat-spotting during heavy braking |
| **Emergency Brakes** | Separate accumulator system | Not separately modeled in FC3; brakes always function |

> *⚠ Prior Dossier Correction: The previous dossier listed `LCtrl + W` as BOTH parking brake AND emergency jettison. `LCtrl + W` is the parking brake. Emergency jettison is a separate keybind (see Module 6 — Emergencies).*

---

### Module 2 — DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Electrical Power** | `RShift + L` | Toggles all electrics |
| **Left Engine Start** | `RAlt + Home` | |
| **Right Engine Start** | `RCtrl + Home` | |
| **Left Engine Stop** | `RAlt + End` | |
| **Right Engine Stop** | `RCtrl + End` | |
| **Wheel Brakes** | `W` | Hold to brake |
| **Parking Brake** | `LCtrl + W` | Toggle |
| **Canopy Open/Close** | `LCtrl + C` | Toggle |
| **Landing/Taxi Light** | `L` or `RCtrl + L` | Varies by specific binding; check assignments |
| **Altimeter Set (+)** | `RAlt + Num+` | Increase QNH |
| **Altimeter Set (-)** | `RAlt + Num-` | Decrease QNH |
| **Nosewheel Steering** | Rudder axis / pedals | Automatic on ground; no separate NWS toggle in FC3 |

---

### Module 2 — Instructor Notes

| Topic | Guidance |
|---|---|
| **"Real Start vs. FC3 Start"** | Acknowledge the simplification honestly. The FC3 start is not wrong — it is abstracted. The real procedure exists for fidelity context, not for execution in DCS. Students should learn the FC3 keybinds without apology. |
| **EGT Monitoring** | Even in FC3, hot starts are possible if ambient temperature is very high or the mission editor sets abnormal conditions. Teach students to WATCH EGT during start, not just mash keys. |
| **Taxi Discipline** | The A-10A is easy to over-speed on taxi because the engines produce substantial thrust at idle. Teach students to use brake taps, not throttle reduction, to control taxi speed — cutting throttle below idle spools the engines down, then requires power re-application and a spool-up delay. |
| **Before-Takeoff Flow** | Encourage a "flow" pattern: Left-to-right, top-to-bottom across the keybind checklist. This builds consistency and reduces missed items. |

---

## Module 3 — Communications

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Understand radio communications in the DCS FC3 simplified model.
2. Configure and use DCS Easy Communications for ATC and wingman commands.
3. Execute standard radio calls for all phases of flight using proper USAF phraseology.
4. Understand guard frequency monitoring and emergency communications.
5. Configure SRS (SimpleRadio Standalone) for multiplayer operations if applicable.

---

### 3.1 Radio Systems Overview

#### Real-World A-10A Radios

The real A-10A is equipped with:

| Radio | Type | Frequency Range | Primary Use |
|---|---|---|---|
| **AN/ARC-164** | UHF AM | 225.000–399.975 MHz | Primary ATC, tactical, inter-flight |
| **AN/ARC-186** | VHF AM/FM | 30.000–87.975 MHz (FM) / 108.000–173.975 MHz (AM) | Ground control, JTAC/FAC, Army coordination |
| **KY-58** | HAVE QUICK secure voice | UHF band | Encrypted tactical comms (not modeled in DCS FC3) |

#### DCS FC3 Radio Model

In DCS FC3, radios are **not individually tunable**. Instead, communications are handled through:

1. **Easy Communications Menu** — a structured menu system accessed via keybind that provides pre-built radio calls for ATC, wingman, AWACS, and tanker.
2. **Direct frequency tuning** — not available in FC3 (available only in full-fidelity modules like the A-10C II).
3. **SRS (SimpleRadio Standalone)** — a third-party mod for multiplayer that adds realistic radio simulation on top of FC3. If the server supports SRS, it overrides Easy Comm for player-to-player communication.

---

### 3.2 DCS Easy Communications System

#### Accessing the Comm Menu

| Action | Default Keybind | Notes |
|---|---|---|
| **Open Comm Menu** | `\` (backslash) | Opens the main communications menu |
| **Navigate Menu** | `F1` – `F12` | Select numbered options |
| **Close Menu** | `Esc` or `\` | Exits without sending a call |

#### Menu Structure

```
Main Menu (\)
├── F1: Wingman #2
│   ├── F1: Engage My Target
│   ├── F2: Cover Me
│   ├── F3: Return to Base
│   ├── F4: Rejoin Formation
│   └── ...
├── F2: Wingman #3 (if applicable)
├── F3: Wingman #4 (if applicable)
├── F5: ATC / Tower
│   ├── F1: Inbound (request approach/landing)
│   ├── F2: Taxi to Runway
│   ├── F3: Request Takeoff
│   └── ...
├── F6: AWACS / GCI
│   ├── F1: Declare (request BRA to nearest hostile)
│   ├── F2: Request Vector to Nearest Airfield
│   ├── F3: Request Tanker
│   └── ...
├── F8: Ground Crew
│   ├── F1: Rearm / Refuel
│   ├── F2: Request Ground Power
│   └── ...
└── F10: Other (custom messages in multiplayer)
```

> *⚠ Realism Divergence: The real A-10A pilot manually tunes radio frequencies, monitors guard (243.0 MHz UHF / 121.5 MHz VHF), and uses proper USAF brevity. DCS Easy Comm automates all of this into a menu system. Proper radio discipline (correct phraseology, brevity, listening before transmitting) cannot be practiced in Easy Comm mode.*

---

### 3.3 Standard Radio Calls (USAF Phraseology)

Even though DCS Easy Comm handles the mechanics, students should learn the proper structure of radio calls for multiplayer and SRS environments.

#### Call Structure

**Format:** `[Station called], [Your callsign], [Your message]`

#### Ground Operations

| Phase | Example Call |
|---|---|
| **Taxi Request** | *"Ground, Hawg 11, parking spot Alpha-3, request taxi runway 27 with information Bravo."* |
| **Taxi Readback** | *"Hawg 11, taxi runway 27 via Alpha, Bravo."* |
| **Holding Short** | *"Tower, Hawg 11, holding short runway 27, ready for departure."* |

#### Takeoff & Departure

| Phase | Example Call |
|---|---|
| **Takeoff Clearance** | *"Hawg 11, runway 27, cleared for takeoff."* (readback) |
| **Airborne** | *"Departure, Hawg 11, airborne runway 27, passing 1,500 climbing 10,000."* |

#### Pattern & Landing

| Phase | Example Call |
|---|---|
| **Inbound** | *"Tower, Hawg 11, 10 miles south, inbound for full stop, information Charlie."* |
| **Downwind** | *"Tower, Hawg 11, downwind runway 27, full stop."* |
| **Base Turn** | *"Hawg 11, base, gear down, full stop."* |
| **Final** | *"Hawg 11, final, runway 27."* |
| **Go-Around** | *"Hawg 11, going around."* |

#### Emergency

| Phase | Example Call |
|---|---|
| **Mayday** | *"MAYDAY, MAYDAY, MAYDAY, Hawg 11, [nature of emergency], [position], [altitude], [fuel state], [intentions], [souls on board]."* |
| **Pan** | *"PAN PAN PAN, Hawg 11, [situation], request [assistance]."* |

---

### 3.4 Guard Frequencies

| Frequency | Band | Purpose |
|---|---|---|
| **243.0 MHz** | UHF (Military) | International military distress frequency |
| **121.5 MHz** | VHF (Civil/Military) | International civil distress frequency |

> *In DCS FC3: Guard is not separately monitorable. Emergency calls in multiplayer rely on SRS or the F10 "Other" menu.*

---

### 3.5 IFF / Transponder

| Mode | Purpose | DCS FC3 Notes |
|---|---|---|
| **Mode 1** | Mission-specific identification | Not individually set in FC3 |
| **Mode 2** | Unit identification | Not individually set in FC3 |
| **Mode 3/A** | ATC identification (squawk code) | Not available in FC3 |
| **Mode 4** | Encrypted IFF (crypto required) | Modeled as automatic in DCS; IFF interrogation via `I` or `RAlt + I` |
| **Emergency Squawk (7700)** | Mayday declaration via transponder | Not available in FC3 |

#### DCS IFF Keybinds

| Action | Default Keybind | Notes |
|---|---|---|
| **IFF Interrogate** | `I` | Points at target; returns hostile/friendly in DCS |
| **Identify Friend/Foe** | `RAlt + I` | Alternative IFF mode |

> *⚠ Realism Divergence: Real IFF requires mode selection, crypto loading, and proper code entry. DCS FC3 reduces this to a simple "point and interrogate" keybind that returns a binary friend/foe result.*

---

### 3.6 SRS (SimpleRadio Standalone) Integration

For multiplayer servers using SRS:

| Feature | Details |
|---|---|
| **What is SRS?** | A third-party mod that adds realistic radio comms to DCS multiplayer |
| **Radio Simulation** | Provides UHF/VHF/AM/FM radio panels that overlay the DCS screen |
| **Frequency Tuning** | Player manually tunes frequencies on the SRS radio panel |
| **PTT (Push-to-Talk)** | Separate PTT keybinds for each radio (configurable in SRS settings) |
| **Encryption** | SRS supports HAVE QUICK and encrypted channels |
| **FC3 Compatibility** | FC3 modules work with SRS; the SRS overlay replaces Easy Comm for human-to-human comms |
| **AI Comms** | DCS Easy Comm still works for AI ATC/wingman even when SRS is active |

---

### Module 3 — Instructor Notes

| Topic | Guidance |
|---|---|
| **Easy Comm Sufficiency** | For single-player BQT training, Easy Comm is perfectly adequate. Students should focus on WHEN to make calls, not how to tune radios — timing and situational awareness are the real skills. |
| **Phraseology Practice** | Even in single-player, encourage students to verbalize the proper radio call before pressing the Easy Comm key. This builds muscle memory for multiplayer / SRS environments. |
| **SRS Introduction** | Do not require SRS for BQT. Introduce it as an optional enhancement for multiplayer. Students who wish to join online communities (e.g., Hoggit, Open Conflict) will need SRS proficiency. |
| **Brevity** | Teach brevity from Day 1: say what's necessary, nothing more. *"Hawg 11, base, gear down, full stop"* — not a life story. |

---

## Module 4 — Takeoff & Departure

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Execute a normal takeoff from a paved runway.
2. Execute a short-field takeoff using MVR flaps.
3. Identify and respond to engine failure during the takeoff roll and after rotation.
4. Describe V-speeds for different weight classes and configurations.
5. Execute standard departure procedures from the traffic pattern.

---

### 4.1 V-Speeds & Takeoff Planning

#### V-Speed Definitions

| V-Speed | Definition |
|---|---|
| **Vr** (Rotation) | Speed at which the pilot initiates rotation (pitch-up) for liftoff |
| **Vlof** (Lift-Off) | Speed at which the aircraft becomes airborne |
| **V2** (Takeoff Safety) | Minimum safe climb speed with one engine inoperative (OEI) |
| **Vmca** (Min Control Air)** | Minimum speed at which directional control can be maintained with one engine failed and the other at MIL power |
| **Vref** (Reference) | Approach/landing reference speed; target speed for final approach |

#### V-Speeds by Weight Class

| Weight Class | Gross Weight | Vr | V2 (OEI) | Vmca | Notes |
|---|---|---|---|---|---|
| **Light (Training)** | 30,000–35,000 lbs | ~105 KIAS | ~120 KIAS | ~110 KIAS | Typical BQT configuration: internal fuel only, no/light stores |
| **Medium (Typical CAS)** | 35,000–42,000 lbs | ~115 KIAS | ~130 KIAS | ~115 KIAS | Internal fuel + moderate stores |
| **Heavy (Max Stores)** | 42,000–50,000 lbs | ~130 KIAS | ~145 KIAS | ~120 KIAS | Near MTOW; avoid soft-field operations at this weight |

> *⚠ Important: These are approximate values for planning. Actual speeds vary with temperature, pressure altitude, and specific store configurations. The A-10A has NO takeoff performance computer — pilots use T.O. charts (not available in FC3) or these planning figures.*

> *⚠ Prior Dossier Correction: The previous dossier presented V-speeds without clear weight-class correlation and some values appeared approximate. The figures above are derived from publicly available T.O. 1A-10A-1 excerpt data and verified against DCS AFM behavior. Vmca of ~110 KIAS for light weight is a commonly cited planning figure.*

---

### 4.2 Normal Takeoff (Flaps UP)

This is the standard takeoff procedure for a light to medium-weight A-10A on a runway of adequate length (≥ 6,000 ft).

| Phase | Action | Notes |
|---|---|---|
| **1. Lineup** | Taxi onto runway centerline; align nosewheel | Ensure no traffic on final |
| **2. Hold Brakes** | Apply and hold wheel brakes (`W`) | Prevents rolling during power application |
| **3. Power Up** | Smoothly advance throttle to approximately 85–90% N2 | Allow engines to stabilize for 2–3 seconds; confirm both N2 gauges match |
| **4. Check Engines** | Verify both engines at matched RPM, EGT normal | If mismatch > 5% N2 or any caution → ABORT |
| **5. Release Brakes** | Release `W` | Aircraft begins rolling |
| **6. Full Power** | Advance to 100% (MIL power) | As aircraft begins rolling; smooth throttle movement |
| **7. Track Centerline** | Use nosewheel steering / rudder pedals | Correct for crosswind with into-wind rudder; keep wings level with aileron into wind |
| **8. Rotate at Vr** | At ~105–130 KIAS (weight dependent), gently pull back on stick | Smooth 2–3° per second pitch rate; target 8–10° nose-up initial attitude |
| **9. Liftoff** | Aircraft becomes airborne 5–10 knots above Vr | Do NOT jerk the stick; the A-10A will fly when ready |
| **10. Gear Up** | Once positive rate of climb confirmed + no runway remaining | `G` key; confirm gear transit indication on HUD |
| **11. Accelerate** | Maintain 8–10° pitch; allow speed to build | Target 150–160 KIAS initial climb speed |
| **12. Climb** | At departure altitude / safe speed, set climb power (~90% N2) | |

#### Crosswind Corrections During Takeoff

| Crosswind Component | Technique |
|---|---|
| **0–10 knots** | Normal rudder/aileron inputs; no special technique needed |
| **10–20 knots** | Wing slightly into wind on initial roll; aggressive rudder may be needed at rotation |
| **20–25 knots** | Maximum demonstrated crosswind; delay rotation slightly (+5 KIAS) to ensure adequate control authority |
| **> 25 knots** | Consider alternate runway or delay takeoff |

---

### 4.3 Short-Field Takeoff (MVR Flaps)

Use when runway length is limited (< 5,000 ft) or when operating at higher gross weights.

| Phase | Action | Notes |
|---|---|---|
| **1. Set Flaps MVR** | `LCtrl + F` (one press from UP) | 7° flap deflection — reduces ground roll ~10–15% |
| **2. Lineup & Hold** | Same as normal takeoff | |
| **3. Power to MIL** | Full throttle while holding brakes | Allow both engines to stabilize at 100% N2 |
| **4. Release Brakes** | Release `W` | Rolling start at maximum thrust |
| **5. Rotate** | At Vr (same as normal, but aircraft will lift off sooner) | Flaps reduce liftoff speed by ~5–8 KIAS |
| **6. Gear Up** | Positive rate, no runway remaining | `G` key |
| **7. Accelerate & Retract Flaps** | Accelerate to ≥ 150 KIAS, then retract flaps | `LShift + F` to return flaps UP |

> *⚠ CAUTION: Do NOT exceed 200 KIAS with flaps extended. The flap limit speed is 200 KIAS — exceeding this can cause structural damage to the flap mechanism.*

#### Speed Limits with Flaps

| Configuration | Max Speed |
|---|---|
| **Flaps UP** | Vne (450 KIAS / 0.75 Mach, whichever is lower) |
| **Flaps MVR (7°)** | 200 KIAS |
| **Flaps DN (20°)** | 200 KIAS |

---

### 4.4 Takeoff Abort (Rejected Takeoff)

| Decision Point | Action |
|---|---|
| **Below Vr** | Throttle to IDLE → Apply maximum brakes (`W`) → Deploy speed brakes (`LShift + B`) → Maintain centerline with rudder |
| **Above Vr but NOT airborne** | Same as below Vr — do NOT attempt to fly an aircraft that won't rotate |
| **Airborne, engine failure below V2** | If sufficient runway remaining: land straight ahead. If insufficient: continue to V2, climb, and execute single-engine procedures |
| **Airborne, engine failure above V2** | Continue takeoff; climb at V2; execute single-engine procedures |

#### Abort Criteria

- Engine failure (RPM rollback, EGT spike, fire indication)
- Directional control loss
- Tire failure / unusual vibration
- Caution/warning light that indicates an unsafe-to-fly condition
- Any doubt about the aircraft's ability to fly safely

> *Instructor emphasis: "If in doubt — ABORT. Runway behind you is useless; speed above you is expensive; runway ahead of you can save your life."*

---

### 4.5 Engine Failure During Takeoff (Airborne)

If an engine fails after liftoff:

| Phase | Action | Notes |
|---|---|---|
| **1. FLY THE AIRCRAFT** | Maintain wings level; prevent yaw with rudder | Priority one — ALWAYS |
| **2. Identify failed engine** | RPM rollback / EGT drop on one side | In FC3: check engine indicators on HUD |
| **3. Maintain Vmca** | ≥ 110–120 KIAS (weight dependent) | If speed decays below Vmca, you WILL lose directional control |
| **4. Maintain / climb** | At V2 speed, the A-10A will maintain altitude or climb slowly on one engine | At heavy weights, climb rate may be minimal (200–500 fpm) |
| **5. Clean up** | Gear up (`G`); flaps up (`LShift + F`) | Reduce drag; improve climb performance |
| **6. If engine is ON FIRE** | Shut down the affected engine (`RAlt + End` or `RCtrl + End`) | In FC3, this is the primary action for engine fire |
| **7. Plan** | Return for immediate landing if able; or continue to suitable airfield | Single-engine landing speed: add ~10 KIAS to normal Vref |

> *⚠ Realism Divergence: Real A-10A engine failure procedures include fire handle pull, fire extinguisher discharge, fuel crossfeed management, bleed air configuration, and generator bus switching. DCS FC3 reduces this to identifying the failed engine and (if necessary) shutting it down. The flight characteristics (yaw, reduced climb, asymmetric thrust) are accurately modeled by the AFM.*

---

### 4.6 Departure Procedures

After takeoff, standard departure options:

| Departure Type | Description |
|---|---|
| **Straight-Out** | Continue runway heading to pattern altitude (1,500 ft AGL) or assigned altitude; then turn on course |
| **Crosswind Departure** | Climb to pattern altitude, then turn crosswind (90° from runway heading) |
| **Downwind Departure** | Climb to pattern altitude, turn crosswind, then continue to downwind heading (180° from takeoff). Used when departing opposite the takeoff direction. |
| **Overhead Departure** | Climb above pattern altitude, overfly the field, then depart on course. Less common in tactical operations. |

---

### Module 4 — DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Throttle to MIL** | `Num +` (full forward) or HOTAS | |
| **Throttle to IDLE** | `Num -` (full back) or HOTAS | |
| **Gear Toggle** | `G` | Up/Down toggle |
| **Flaps Down (one step)** | `LCtrl + F` | UP→MVR→DN |
| **Flaps Up (one step)** | `LShift + F` | DN→MVR→UP |
| **Speed Brakes Open** | `LShift + B` | |
| **Speed Brakes Close** | `LCtrl + B` | |
| **Wheel Brakes** | `W` | Hold to brake |
| **Parking Brake** | `LCtrl + W` | Toggle |

---

### Module 4 — Instructor Notes

| Topic | Guidance |
|---|---|
| **Weight Awareness** | Begin every takeoff briefing with "What do we weigh?" Students must develop the habit of considering weight before computing V-speeds, choosing flap setting, and planning abort distance. In DCS, check fuel quantity before taxi. |
| **Rotation Feel** | The A-10A rotates smoothly and predictably. Teach students to pull gently and steadily — not yank. Over-rotation wastes energy and can lead to tail strike at heavy weights. |
| **Single-Engine Emphasis** | Engine failure at low altitude is the most dangerous takeoff emergency. Drill the response: FLY → IDENTIFY → MAINTAIN SPEED → CLEAN UP → DECIDE. Speed is life; let the aircraft accelerate to V2 before worrying about anything else. |
| **Abort Decision** | Teach the "abort zone" concept: below Vr, always abort for any engine problem. Above Vr, the decision depends on altitude, speed, and remaining runway. Emphasize that continuing a bad takeoff is worse than aborting with room to stop. |

---

## Module 5 — Flight Maneuvers & Airwork

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Execute level flight at assigned altitudes with proper trim technique.
2. Perform coordinated turns at varying bank angles including steep turns.
3. Demonstrate stall recognition and recovery in clean and dirty configurations.
4. Execute slow flight and approach-to-stall maneuvers with confidence.
5. Perform single-engine flight and demonstrate directional control techniques.
6. Describe the A-10A's traffic pattern and execute standard overhead and straight-in patterns.

---

### 5.1 Level Flight & Trim

#### Cruise Configurations

| Weight Class | Cruise Speed | Cruise Altitude | Approx. Power Setting | Fuel Flow (both engines) |
|---|---|---|---|---|
| **Light (< 35,000 lbs)** | 250–280 KIAS | 10,000–15,000 ft | 80–85% N2 | ~1,800–2,200 lbs/hr |
| **Medium (35,000–42,000)** | 240–270 KIAS | 8,000–12,000 ft | 85–90% N2 | ~2,200–2,600 lbs/hr |
| **Heavy (> 42,000 lbs)** | 220–250 KIAS | 5,000–10,000 ft | 88–92% N2 | ~2,500–3,000 lbs/hr |

> *The A-10A's optimum cruise altitude is relatively low — typically below FL200. Above FL250, the aircraft struggles to maintain useful maneuvering speed. Most tactical operations occur between 5,000 and 15,000 ft AGL.*

#### Trim Discipline

The A-10A has **no stability augmentation system (SAS)** and **no fly-by-wire**. All flight control inputs are direct hydraulic (or mechanical in manual reversion). This means:

- **Every configuration change requires re-trimming:** speed change, power change, gear/flap extension, stores release.
- **Trim in all three axes:** pitch trim (`RCtrl + ;` / `RCtrl + .`), roll trim (`RCtrl + ,` / `RCtrl + /`), rudder trim (`RCtrl + Z` / `RCtrl + X`).
- **The test:** If you are holding any constant stick or rudder pressure for more than 5 seconds, you need to trim.
- **Combat loads create asymmetry:** After releasing ordnance from one wing, the aircraft will roll toward the heavy wing. Immediate roll and potentially rudder trim is required.

---

### 5.2 Turns

#### Standard Rate Turns

| Bank Angle | Application | Notes |
|---|---|---|
| **15–20°** | Gentle maneuvering; heading corrections | Minimal altitude change; easy to maintain |
| **30°** | Standard turn; pattern turns | Standard bank for overhead pattern turns |
| **45°** | Steep turn (training maneuver) | Requires back-pressure and/or power addition to maintain altitude |
| **60°** | Very steep; G-loading ~2.0G | Significant back-pressure; substantial altitude loss if power not added |
| **> 60°** | Not standard for BQT | G-loading increases rapidly; reserve for combat maneuvering course |

#### Steep Turn Procedure (45° Bank)

1. Clear the area (visual scan + check for traffic).
2. Establish entry altitude and airspeed (recommend 250 KIAS at a convenient altitude).
3. Smoothly roll to 45° bank while simultaneously adding slight back-pressure.
4. Add ~5% N2 power to compensate for increased load factor.
5. Maintain altitude ±100 ft and airspeed ±10 KIAS through the turn.
6. At ~30° before desired rollout heading, begin rolling wings level.
7. Reduce power to original setting; re-trim.
8. **Standards:** ±100 ft altitude, ±10 KIAS speed, ±5° heading at rollout.

---

### 5.3 Stall Series

#### Clean Configuration Stall (Power Off)

| Phase | Action |
|---|---|
| **Setup** | 10,000 ft AGL minimum; clear the area; configure clean (gear up, flaps up, speed brakes closed) |
| **Entry** | Reduce power to idle (`Num -`); maintain altitude — allow speed to decay |
| **Approach to stall** | At ~18–20 AoA, buffet onset begins; AOA indexer shows amber UP chevron |
| **Stall** | At ~23–25 AoA, nose drops; possible wing rock; airspeed ~130 KIAS clean/light |
| **Recovery** | Simultaneously: power to MIL → lower nose below horizon → wings level with rudder → recover to level flight at safe speed |
| **Exit** | Resume normal flight above 180 KIAS; re-trim |

#### Dirty Configuration Stall (Approach Configuration)

| Phase | Action |
|---|---|
| **Setup** | 10,000 ft AGL; clear area; gear down (`G`); flaps DN (`LCtrl + F` × 2); speed brakes closed |
| **Entry** | Power at approach setting (~75–80% N2); maintain altitude; allow speed to decay |
| **Approach to stall** | Buffet onset earlier due to increased drag; ~110 KIAS for light weight |
| **Stall** | Nose drops; more pronounced than clean stall due to drag |
| **Recovery** | Power to MIL → lower nose → wings level → positive rate → gear up → flaps up (incrementally) → accelerate |
| **Exit** | Resume normal flight; re-trim |

> *⚠ Stall Note: The A-10A's straight wing provides very benign stall characteristics. There is ample buffet warning before stall break. The aircraft does not "snap" or depart suddenly unless the entry is deeply uncoordinated (crossed controls). Spin entry requires deliberate effort. This is by design — the aircraft was built for low-speed, high-AoA maneuvering in the CAS environment.*

---

### 5.4 Slow Flight

| Phase | Action | Notes |
|---|---|---|
| **Setup** | Altitude ≥ 5,000 ft AGL; clear area | |
| **Configuration** | Gear down; flaps MVR (7°) | Simulate approach configuration |
| **Decelerate** | Reduce power gradually; maintain altitude; allow speed to decrease to ~120–130 KIAS | |
| **Stabilize** | Fly at ~10 KIAS above stall speed (dirty) | Requires ~80–85% N2 power to maintain level flight |
| **Maneuver** | Execute gentle turns (≤ 15° bank) while maintaining altitude and speed | Demonstrates the back side of the power curve; pitch controls speed, power controls altitude |
| **Recovery** | Add power to MIL → accelerate to safe speed → retract flaps → gear up → re-trim | |

> *Instructor Note: Slow flight teaches the relationship between AoA, power, and aircraft state. In the A-10A, slow flight is comfortable and stable — the aircraft WANTS to fly at these speeds. Use this to build student confidence in the low-speed regime they will operate in during CAS.*

---

### 5.5 Single-Engine Flight

#### Configuration

- One engine failed (simulated by shutting down one engine: `RAlt + End` for left, `RCtrl + End` for right)
- Other engine at MIL power

#### Characteristics

| Parameter | Value/Behavior |
|---|---|
| **Vmca** | ~110–120 KIAS (weight dependent) — NEVER go below this speed |
| **Climb Rate (Light Weight)** | ~500–1,000 fpm at V2 speed | 
| **Climb Rate (Heavy Weight)** | ~0–500 fpm at V2 speed (may not climb at very heavy weights) |
| **Yaw** | Strong yaw toward dead engine; requires significant rudder input (5–10° pedal displacement) |
| **Roll** | Tendency to roll toward dead engine; correct with aileron |
| **Rudder Trim** | ESSENTIAL — trim out the rudder force as soon as stable | 
| **Recommended Speed** | V2 + 10 KIAS minimum; 150–160 KIAS for comfortable maneuvering |

#### Procedure

1. **FLY THE AIRCRAFT** — maintain wings level, prevent yaw.
2. **Identify** the failed engine (which N2 is dropping? which EGT is anomalous?).
3. **Confirm** the identification: "Dead foot = dead engine."
4. **Secure** the failed engine if necessary (fire, oil failure): use engine stop keybind.
5. **Trim** — significant rudder trim toward the good engine; roll trim as needed.
6. **Reduce drag** — gear up, flaps up, speed brakes closed.
7. **Plan** — proceed to nearest suitable airfield for single-engine landing.

> *⚠ Realism Divergence: In the real A-10A, the pilot would also manage fuel crossfeed, generator bus switching, bleed air reconfiguration, and fire suppression. DCS FC3 does not model these subsystems. The yaw/roll/performance effects are accurately modeled via the AFM.*

---

### 5.6 Traffic Pattern

The A-10A uses standard USAF overhead and rectangular traffic patterns.

#### Overhead Pattern (Break Pattern)

```
                    ← Initial Approach (250-300 KIAS, pattern alt)
                    ┌─────────────────────────────────────────┐
                    │              OVERHEAD BREAK              │
                    │  (Break at approach end of runway)       │
                    │                                          │
         Downwind   │  (150-170 KIAS, gear/flaps)             │
         ◄──────────┤                                          │
                    │                                          │
                    │         ┌── Base Turn ──┐                │
                    │         │  (130-140 KIAS)│                │
                    │         │               │                │
                    └─────────┘               │                │
                              Final           │                │
                              (Vref: 120-140) │                │
                              ▼               │                │
                    ════════[RUNWAY]═══════════                │
                              ▲                                │
                              │                                │
                              └── Departure ───────────────────┘
```

#### Overhead Pattern Procedures

| Leg | Altitude | Speed | Configuration | Actions |
|---|---|---|---|---|
| **Initial** | 1,500 ft AGL | 250–300 KIAS | Clean | Radio: request overhead pattern entry |
| **Break** | 1,500 ft AGL | 250+ KIAS → decelerating | Clean → transitioning | Aggressive turn (60–70° bank) to downwind heading; pull power to idle; begin decelerating |
| **Downwind** | 1,500 ft AGL | 150–170 KIAS | Gear DOWN (`G`); Flaps MVR or DN | Gear at 200 KIAS or below; check 3 green (gear down and locked indication) |
| **Abeam Threshold** | 1,500 ft AGL | 150–160 KIAS | Dirty | Begin timing or spacing for base turn; descend to ~1,000 ft AGL |
| **Base** | ~1,000 ft AGL | 130–140 KIAS | Dirty | Turn base; continue descent; align for final |
| **Final** | Descending | Vref (120–140 KIAS) | Dirty | AOA indexer on-speed ("donut"); stabilized by 300 ft AGL |

#### Rectangular Pattern (Straight-In Capable)

For situations where an overhead approach is not appropriate (low visibility, multiple aircraft, controller direction):

| Leg | Altitude | Speed | Notes |
|---|---|---|---|
| **Upwind / Departure** | Climbing to 1,500 ft AGL | 150+ KIAS | After takeoff; climbing |
| **Crosswind** | 1,500 ft AGL | 170–180 KIAS | Level off; begin configuring for downwind |
| **Downwind** | 1,500 ft AGL | 150–170 KIAS | Gear down; flaps as required |
| **Base** | Descending | 130–140 KIAS | Descend; align for final |
| **Final** | Descending | Vref | Stabilized approach; AOA on-speed |

> *⚠ Prior Dossier Correction: The previous dossier listed pattern altitude as 1,500 ft AGL without qualification. This is the standard USAF overhead pattern altitude per AFMAN 11-2A-10 Vol. 3. This value is correct and has been retained.*

---

### 5.7 Speed Limits Summary

| Configuration | Maximum Speed | Notes |
|---|---|---|
| **Clean** | 450 KIAS / Mach 0.75 | Whichever is lower (Mach limit applies above ~FL200) |
| **Gear Down** | 200 KIAS | Below 200 KIAS before extending; retract before accelerating above 200 |
| **Flaps (any position)** | 200 KIAS | MVR or DN — same limit |
| **Speed Brakes** | No restriction | Can be deployed at any speed within the normal flight envelope |

---

### Module 5 — DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Gear Toggle** | `G` | |
| **Flaps Down** | `LCtrl + F` | |
| **Flaps Up** | `LShift + F` | |
| **Speed Brakes Toggle** | `B` | |
| **Speed Brakes Open** | `LShift + B` | |
| **Speed Brakes Close** | `LCtrl + B` | |
| **Pitch Trim Nose Up** | `RCtrl + ;` | |
| **Pitch Trim Nose Down** | `RCtrl + .` | |
| **Roll Trim Left** | `RCtrl + ,` | |
| **Roll Trim Right** | `RCtrl + /` | |
| **Rudder Trim Left** | `RCtrl + Z` | |
| **Rudder Trim Right** | `RCtrl + X` | |
| **Autopilot** | `A` (engage/disengage) | Level-flight hold; not a full autopilot — maintains current attitude |
| **Left Engine Stop** | `RAlt + End` | For single-engine practice |
| **Right Engine Stop** | `RCtrl + End` | For single-engine practice |
| **Left Engine Start** | `RAlt + Home` | To restart |
| **Right Engine Start** | `RCtrl + Home` | To restart |

---

### Module 5 — Instructor Notes

| Topic | Guidance |
|---|---|
| **Trim, Trim, Trim** | This module is where trim discipline is drilled. Every maneuver entry and exit requires re-trimming. Debrief trim technique on every flight. |
| **Stall Confidence** | The A-10A stall is benign. Let students experience it repeatedly until they are comfortable. Fear of the stall leads to poor low-speed handling, which is deadly in the CAS environment. |
| **Single-Engine Respect** | While the A-10A flies well on one engine, students must NEVER become complacent. Below Vmca, the aircraft becomes uncontrollable. Drill the Vmca number into every student: "What's your Vmca today?" should be a pre-flight question. |
| **Pattern Standards** | Hold tight standards on the pattern: ±100 ft altitude on downwind, ±10 KIAS on final, AOA indexer on-speed by 300 ft AGL. Sloppy patterns lead to sloppy landings. |
| **Overhead Break** | The overhead break is a high-energy maneuver unique to military aviation. Teach the sequence: initial → break → decelerate → configure → downwind. The break itself is aggressive (60–70° bank) but controlled. Students love it — channel that enthusiasm into precision. |
| **Glide Ratio Reality** | The A-10A clean glide ratio is approximately 8–10:1, NOT 17:1 as listed in the previous dossier. This means from 10,000 ft AGL with both engines failed, the aircraft can glide approximately 13–17 NM. Plan accordingly — this is NOT a glider. |

---

## Module 6 — Emergency Procedures

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Execute immediate-action (boldface) procedures for engine fire, dual engine failure, and flight control failure from memory.
2. Describe the dual-hydraulic system failure and manual reversion characteristics.
3. Execute a forced landing / glide approach following dual engine failure.
4. Identify ejection criteria and execute emergency ground egress.
5. Respond to common system failures: electrical, fuel, and instrument malfunctions.

---

### 6.1 Emergency Philosophy

The A-10A was designed for survivability. Its redundant systems mean that many "emergencies" in other aircraft are merely "degraded operations" in the Hog. The pilot's priorities remain constant:

1. **Maintain aircraft control** — Fly the aircraft FIRST
2. **Analyze the situation** — What failed? What still works?
3. **Take appropriate action** — Execute the applicable procedure
4. **Land as soon as conditions permit** — Do not press the mission with a degraded aircraft

> *DCS FC3 Note: Emergency procedures in FC3 are simplified because the systems are simplified. You cannot pull fire handles, discharge extinguishers, isolate electrical busses, or manage individual hydraulic systems. However, the AFM accurately models the EFFECTS of failures: yaw, reduced performance, control degradation, and fire damage progression. The pilot's procedural response is simplified but the recognition and decision-making skills are realistic.*

---

### 6.2 Boldface (Immediate-Action) Procedures

These procedures must be executed from **memory** — they address time-critical emergencies where delay can be fatal.

#### ENGINE FIRE (Single Engine)

```
ENGINE FIRE (IN FLIGHT)
━━━━━━━━━━━━━━━━━━━━━━
1. THROTTLE (affected engine) ............ IDLE
2. ENGINE (affected engine) .............. SHUT DOWN
   • Left:  RAlt + End
   • Right: RCtrl + End
3. MONITOR fire indication ............... OBSERVE
   • If fire persists → PREPARE TO EJECT
   • If fire extinguishes → proceed to nearest airfield
4. SINGLE-ENGINE procedures .............. EXECUTE
```

> *Real-world expansion: In the real A-10A, the pilot would also pull the fire handle (which shuts off fuel, hydraulics, bleed air, and electrics to that engine), discharge the fire extinguisher, and configure fuel crossfeed. DCS FC3 combines all of this into the engine stop keybind.*

#### DUAL ENGINE FAILURE / FLAMEOUT

```
DUAL ENGINE FAILURE
━━━━━━━━━━━━━━━━━━━━━━
1. AIRSPEED ............................ MAINTAIN 200 KIAS
   (best glide speed; adjust for weight)
2. ALTITUDE ............................ TRADE FOR DISTANCE
   • Glide ratio: ~8–10:1 clean
   • From 10,000 ft ≈ 13–17 NM glide range
3. RESTART ATTEMPT ..................... EXECUTE
   • Left Engine:  RAlt + Home
   • Right Engine: RCtrl + Home
4. IF restart fails .................... PREPARE FOR FORCED LANDING
   • Aim for longest available runway or flat terrain
   • Gear DOWN below 200 KIAS
5. IF no landing site available ........ EJECT
   • Minimum ejection altitude: as high as possible
   • ACES II is zero-zero capable, but altitude = time = options
```

> *⚠ Prior Dossier Correction: The previous dossier listed glide ratio as 17:1 clean. This is incorrect. The A-10A clean glide ratio is approximately 8–10:1. At 17:1 the aircraft would have sailplane-like performance, which contradicts its aerodynamic design (large fuselage cross-section, wing pylons, engine nacelles). Best glide speed is approximately 200 KIAS clean, varying with weight.*

#### FLIGHT CONTROL FAILURE (DUAL HYDRAULIC LOSS)

```
DUAL HYDRAULIC FAILURE — MANUAL REVERSION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. AIRSPEED ............................ REDUCE TO 200 KIAS OR LESS
   (control forces increase dramatically at higher speeds)
2. PITCH TRIM .......................... USE EXTENSIVELY
   (electric trim still functions — this is your primary pitch control aid)
3. CONTROL INPUTS ...................... SMOOTH, DELIBERATE, MODERATE
   (stick forces: 60–80+ lbs; small inputs; anticipate response lag)
4. CONFIGURE EARLY ..................... GEAR AND FLAPS WELL BEFORE FINAL
   (each configuration change requires significant re-trimming)
5. APPROACH ............................. LONG, FLAT, STABILIZED
   (plan a 10+ mile straight-in approach if possible)
6. LANDING .............................. EXPECT FIRM ARRIVAL
   (precise flare is very difficult with manual reversion; plan accordingly)
```

> *⚠ Realism Divergence: DCS models the increased sluggishness and reduced authority of manual reversion, but cannot simulate the physical stick forces. Students with force-feedback sticks will feel some change; others will notice response delay and reduced control authority. The experience is significantly less dramatic in DCS than in reality, where the pilot is exerting 60–80+ pounds of force on the stick.*

---

### 6.3 Single Engine Operations

(Cross-reference Module 5.5 for flight characteristics)

#### Engine Failure Decision Matrix

| Situation | Action |
|---|---|
| **Engine failure in cruise** | Identify → secure → trim → proceed to nearest airfield |
| **Engine failure in pattern** | If on downwind/base: continue pattern and land. If on initial: go around on one engine (if above Vmca). If below Vmca: lower nose immediately. |
| **Engine fire** | Shut down immediately; if fire persists > 30 seconds, prepare to eject |
| **Engine seizure (no fire)** | Shut down; prop windmilling creates drag — expect more yaw than a flameout |

#### Single-Engine Landing Considerations

| Parameter | Value/Guidance |
|---|---|
| **Approach speed** | Vref + 10 KIAS (additional margin for go-around capability) |
| **Pattern** | Fly a wider, flatter pattern — do NOT fly a tight overhead break on one engine |
| **Go-around** | Possible but marginal at heavy weights; plan to land from the first approach |
| **Flap setting** | MVR (7°) preferred — reduces stall speed without excessive drag increase |
| **Touchdown** | On-speed; do not flare excessively; accept a firm landing |

---

### 6.4 Electrical Failure

| Failure | Indication | Action (DCS FC3) |
|---|---|---|
| **Generator failure (one)** | Possible caution light; instruments may flicker | Not separately manageable in FC3; aircraft continues to fly on remaining generator |
| **Total electrical failure** | HUD blanks; all instruments lost | Fly by external references (horizon); attempt to reset power (`RShift + L` toggle); prepare for VFR landing |
| **Battery only** | Reduced instrument functionality | Limited time on battery (~30 minutes); land ASAP |

> *⚠ Realism Divergence: The real A-10A has a complex electrical system with dual generators, battery bus, essential bus, and manual bus-tie switches. The pilot can isolate failed systems and shed non-essential loads. DCS FC3 does not model bus management — the system either works or it doesn't.*

---

### 6.5 Fuel System Emergencies

| Emergency | Indication | Action |
|---|---|---|
| **Low Fuel** | Fuel quantity below ~1,500 lbs | Proceed immediately to nearest airfield; declare emergency if fuel state is critical |
| **Fuel Leak (Combat Damage)** | Rapid fuel quantity decrease | Climb to maximize glide range; head for nearest field; consider shutting down one engine to reduce consumption |
| **Fuel Imbalance** | One wing heavy; roll tendency | In FC3: not separately manageable (no crossfeed switch); trim and continue |
| **Engine Flameout (Fuel Starvation)** | RPM drops to zero; EGT drops | Confirm fuel remaining; attempt restart; if fuel exhausted → DUAL ENGINE FAILURE procedure |

---

### 6.6 Landing Gear Emergencies

| Emergency | Action |
|---|---|
| **Gear fails to extend** | Recycle: gear up, wait, gear down again (`G` twice). In DCS FC3, this usually works. |
| **Gear unsafe indication** | If fewer than 3 green (3 gear down and locked): recycle; attempt alternate extension |
| **Alternate Gear Extension** | Not separately modeled in FC3; recycling the keybind is the only option |
| **Gear-Up Landing (Belly Landing)** | Reduce to minimum safe speed; plan a long, flat approach; expect aircraft damage; DCS models gear-up landing damage |

> *Real-world note: The real A-10A has an emergency gear extension system (nitrogen blow-down). In DCS FC3, recycling the gear keybind simulates this. If gear still won't extend, a belly landing is the only option.*

---

### 6.7 Ejection

| Decision Criteria | Action |
|---|---|
| **Uncontrolled aircraft** | If aircraft is uncontrollable and below 10,000 ft AGL → EJECT IMMEDIATELY |
| **Dual engine failure, no restart, no landing site** | EJECT at maximum available altitude |
| **Fire that cannot be extinguished** | EJECT when fire threatens structural integrity |
| **Ejection decision altitude** | Do not delay below 2,000 ft AGL — at low altitude, every second matters |

#### Ejection Procedure (DCS)

| Step | Action | Key |
|---|---|---|
| 1 | **Eject** | `LCtrl + E` — press 3 times rapidly |

> *The triple-press requirement prevents accidental ejection. In DCS, ejection works from any attitude and airspeed (ACES II zero-zero seat). In reality, ejection at very high speed (> 450 KIAS) or extreme attitudes carries significant injury risk.*

---

### 6.8 Emergency Jettison

| Action | Default Keybind | Notes |
|---|---|---|
| **Emergency Jettison (All Stores)** | `LAlt + R` | Releases ALL external stores — pylons, bombs, tanks, missiles |

> *⚠ Prior Dossier Correction: The previous dossier listed emergency jettison as `LCtrl + W`. This is INCORRECT — `LCtrl + W` is the parking brake. The correct DCS default keybind for emergency jettison is `LAlt + R`. This confusion could be dangerous in an emergency — students must know the correct keybind.*

> *Note: Emergency jettison should only be used when the aircraft cannot safely land with its current stores configuration, or when maximum performance is needed (e.g., dual engine failure requiring maximum glide range, or single-engine go-around at heavy weight).*

---

### Module 6 — Emergency Quick Reference

| Emergency | Key Action | Keybind |
|---|---|---|
| **Engine Fire** | Shut down affected engine | `RAlt + End` (L) / `RCtrl + End` (R) |
| **Dual Engine Failure** | Maintain 200 KIAS; attempt restart | `RAlt + Home` (L) / `RCtrl + Home` (R) |
| **Emergency Jettison** | Dump all stores | `LAlt + R` |
| **Ejection** | Triple-press eject | `LCtrl + E` × 3 |
| **Gear Malfunction** | Recycle gear | `G` (toggle up/down) |

---

### Module 6 — Instructor Notes

| Topic | Guidance |
|---|---|
| **"Aviate, Navigate, Communicate"** | Drill this order relentlessly. The number one killer in emergencies is loss of aircraft control while the pilot is distracted by the emergency itself. FLY THE AIRCRAFT FIRST. |
| **Boldface Memorization** | Engine Fire and Dual Engine Failure procedures should be rote-memorized. Quiz students before every flight. "What do you do if you lose an engine on takeoff?" should get an instant, correct answer. |
| **Ejection Decision** | Students are reluctant to eject in DCS because "it's just a sim." Use this to train the decision-making process: "At what altitude and fuel state would you eject?" Make it a pre-flight discussion point. |
| **Emergency Jettison Keybind** | Explicitly correct the misinformation from the previous dossier. Make students DEMONSTRATE the correct keybind (`LAlt + R`) during ground brief. Muscle memory for the wrong key in an emergency = disaster. |
| **Glide Performance** | 8–10:1 glide ratio means the A-10A loses approximately 1,000 ft per 1.3–1.7 NM. From typical pattern altitude (1,500 ft), glide range is only ~2–3 NM. Students must internalize this — delay costs distance, and distance costs options. |

---

## Module 7 — Approach & Landing

### Learning Objectives

Upon completion of this module, the student will be able to:

1. Execute a stabilized visual approach using the AOA indexer.
2. Perform normal, short-field, and crosswind landings.
3. Execute a go-around from any point in the approach.
4. Perform a single-engine approach and landing.
5. Describe proper speed, configuration, and glidepath management.

---

### 7.1 Approach Planning

#### Key Speeds (Approach & Landing)

| Parameter | Light (< 35,000 lbs) | Medium (35,000–42,000 lbs) | Heavy (> 42,000 lbs) |
|---|---|---|---|
| **Vref (Final Approach)** | ~120 KIAS | ~130 KIAS | ~140 KIAS |
| **Threshold Speed** | Vref – 5 KIAS | Vref – 5 KIAS | Vref – 5 KIAS |
| **Go-Around Speed** | ≥ 120 KIAS | ≥ 130 KIAS | ≥ 140 KIAS |
| **Single-Engine Vref** | Vref + 10 KIAS | Vref + 10 KIAS | Vref + 10 KIAS |

> *The AOA indexer provides the definitive approach speed indication, regardless of weight. Fly the green donut — that IS on-speed for any weight. Use the table above as a cross-check, not the primary reference.*

#### Stabilized Approach Criteria

The approach must be stabilized by **300 ft AGL** (500 ft AGL in instrument conditions). Stabilized means:

- [ ] On speed (AOA indexer showing green donut, or within ±5 KIAS of Vref)
- [ ] On glidepath (3° visual approach slope)
- [ ] On centerline (aligned with runway)
- [ ] Landing configuration set (gear down, flaps as required)
- [ ] Power stable (not requiring large throttle corrections)

**If NOT stabilized by 300 ft AGL → MANDATORY GO-AROUND.** No exceptions.

---

### 7.2 Normal Landing (Full Flaps)

| Phase | Action | Notes |
|---|---|---|
| **1. Downwind** | 1,500 ft AGL; 150–170 KIAS; gear down (`G`); flaps DN (`LCtrl + F` × 2 from UP) | Check 3 green; verify gear down |
| **2. Base Turn** | Begin descent; 130–140 KIAS; bank ~30° | Start turn ~45° past abeam threshold |
| **3. Final Turn** | Roll wings level on runway centerline; ~1 mile from threshold | If not aligned → go around |
| **4. Final Approach** | Vref speed; AOA indexer "green donut"; ~3° glidepath | Small power adjustments to control glidepath; pitch controls speed |
| **5. Short Final (100 ft AGL)** | Cross-check: on speed, on glidepath, on centerline | Last chance for go-around decision |
| **6. Threshold Crossing** | ~50 ft AGL over threshold; begin reducing power | Smooth, gradual power reduction |
| **7. Flare** | Gentle pitch increase (~2–3°); reduce rate of descent | The A-10A does not need an aggressive flare; smooth transition to touchdown attitude |
| **8. Touchdown** | Main gear first; hold nose off briefly | ~Vref – 10 KIAS touchdown speed |
| **9. Nose Lower** | Allow nosewheel to lower gently | Do NOT slam it down; control with back-stick |
| **10. Decelerate** | IDLE power; brakes as required (`W`); speed brakes open (`LShift + B`) | Speed brakes significantly reduce rollout distance |
| **11. Turn Off** | Exit runway at a taxiway; report clear | |

---

### 7.3 Short-Field Landing

When runway length is limited or contaminated:

| Modification | Detail |
|---|---|
| **Approach speed** | Vref (no addition — fly the minimum safe speed) |
| **Flaps** | DN (full, 20°) |
| **Aim point** | ~500 ft from threshold (closer than normal) |
| **Touchdown** | Firm; on the aim point — do NOT float or try to grease it |
| **Braking** | Maximum braking immediately after touchdown; speed brakes open |
| **Rollout** | Expect 2,500–3,500 ft ground roll (clean, light weight, max effort braking) |

---

### 7.4 Crosswind Landing

| Crosswind | Technique |
|---|---|
| **0–10 kts** | Normal approach; slight wing-low into wind on short final; opposite rudder to maintain centerline (sideslip method) |
| **10–20 kts** | Pronounced wing-low; significant rudder required; de-crab at threshold; expect weathervaning on rollout |
| **20–25 kts** | Maximum demonstrated crosswind component; consider alternate runway; requires aggressive rudder/aileron coordination |
| **> 25 kts** | **Do not attempt.** Divert to an airfield with a more favorable runway alignment. |

#### Crosswind Landing Procedure

1. **On final:** Establish a crab into the wind to maintain centerline.
2. **At ~200 ft AGL:** Transition to sideslip — lower the upwind wing, apply opposite (downwind) rudder to align the nose with the runway.
3. **At touchdown:** Upwind main gear touches first; lower the downwind gear and nose; apply immediate rudder to maintain centerline.
4. **On rollout:** The aircraft will weathervane into the wind. Use aggressive rudder and differential braking to maintain centerline. Nosewheel steering authority decreases as speed increases — be prepared.

---

### 7.5 Go-Around (Missed Approach)

| Phase | Action | Notes |
|---|---|---|
| **1. Decision** | "GOING AROUND" — commit fully; no half-measures | |
| **2. Power** | FULL POWER (MIL) — `Num +` | Immediately; do not hesitate |
| **3. Pitch** | Establish 8–10° nose up | Positive rate of climb |
| **4. Gear** | UP — `G` | Once positive rate confirmed |
| **5. Flaps** | Retract incrementally — `LShift + F` | MVR first, then UP once above 150 KIAS |
| **6. Speed Brakes** | CLOSE — `LCtrl + B` | If they were open |
| **7. Climb** | Accelerate to 150–160 KIAS; re-enter pattern or climb to pattern altitude | |
| **8. Communicate** | "Hawg 11, going around" via Easy Comm (`\` → F5 → appropriate option) | |

**Go-Around is MANDATORY if:**
- Not stabilized by 300 ft AGL
- Runway not clear
- Excessive sink rate on short final
- Significant speed deviation (± 10+ KIAS from Vref)
- Pilot not confident the landing can be made safely
- Tower directs a go-around

> *Instructor Note: "A go-around is a NORMAL maneuver, not a failure. The failure is trying to salvage an unstable approach."*

---

### 7.6 Single-Engine Approach & Landing

| Consideration | Guidance |
|---|---|
| **Approach speed** | Vref + 10 KIAS (additional margin for asymmetric go-around) |
| **Pattern** | Fly a wider pattern; avoid steep turns toward the dead engine |
| **Flap setting** | MVR (7°) recommended — reduces stall speed without excessive drag |
| **Go-around capability** | Marginal at heavy weights; PLAN TO LAND FROM FIRST APPROACH |
| **Touchdown** | Accept a firm landing; do not attempt to float or grease it |
| **Directional control** | Maintain rudder input through touchdown and rollout; use differential braking as needed |

#### Single-Engine Go-Around Decision

- **If above Vmca + 10 KIAS and above 300 ft AGL:** Go-around is possible but demanding. Apply MIL power on the good engine, maintain directional control, clean up, and re-enter a wide pattern.
- **If below Vmca + 10 KIAS or below 200 ft AGL:** **DO NOT GO AROUND.** Commit to landing. A single-engine go-around below Vmca will result in loss of directional control.

---

### 7.7 No-Flap Landing

If flaps fail to extend:

| Modification | Detail |
|---|---|
| **Approach speed** | Vref + 15 KIAS (higher stall speed without flaps) |
| **Glidepath** | Flatter (reduced drag = shallower approach) |
| **Landing distance** | Significantly increased; ensure adequate runway length |
| **Touchdown** | Higher ground speed; expect longer rollout; use max braking and speed brakes |

---

### 7.8 After-Landing Procedures

| Step | Action | Key |
|---|---|---|
| 1 | Speed brakes CLOSED | `LCtrl + B` |
| 2 | Flaps UP | `LShift + F` (cycle to UP) |
| 3 | Exit runway at nearest taxiway | NWS/rudder |
| 4 | Report clear of active runway | Easy Comm |
| 5 | Taxi to parking at ≤ 15 knots | |
| 6 | At parking spot: apply parking brake | `LCtrl + W` |

---

### 7.9 Shutdown Procedure

| Step | Action | Key | Notes |
|---|---|---|---|
| 1 | Parking brake SET | `LCtrl + W` | |
| 2 | Throttle to IDLE | `Num -` | Both engines at idle for 2 minutes (cool-down) |
| 3 | Shutdown Left Engine | `RAlt + End` | |
| 4 | Shutdown Right Engine | `RCtrl + End` | |
| 5 | Electrical Power OFF | `RShift + L` | |
| 6 | Canopy Open | `LCtrl + C` | For ground crew access |

> *Real-world note: The real A-10A shutdown includes avionics sequencing, INS memory store, generator/battery switch sequencing, and oxygen system securing. DCS FC3 abstracts this to engine stop + power off.*

---

### Module 7 — DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Gear Toggle** | `G` | |
| **Flaps Down** | `LCtrl + F` | |
| **Flaps Up** | `LShift + F` | |
| **Speed Brakes Open** | `LShift + B` | |
| **Speed Brakes Close** | `LCtrl + B` | |
| **Speed Brakes Toggle** | `B` | |
| **Wheel Brakes** | `W` | |
| **Parking Brake** | `LCtrl + W` | |
| **Throttle Up** | `Num +` | |
| **Throttle Down** | `Num -` | |
| **Canopy** | `LCtrl + C` | |
| **Eject** | `LCtrl + E` × 3 | |
| **Left Engine Stop** | `RAlt + End` | |
| **Right Engine Stop** | `RCtrl + End` | |
| **Electrical Power** | `RShift + L` | |

---

### Module 7 — Instructor Notes

| Topic | Guidance |
|---|---|
| **AOA Indexer Primacy** | This module is where the AOA indexer becomes gospel. "Fly the donut" should be the approach mantra. Students who fixate on airspeed will miss power/glidepath corrections; students who fly the indexer will naturally arrive at the correct speed for any weight. |
| **Stabilized Approach Discipline** | The 300 ft gate is non-negotiable. Debrief every approach that is unstable at 300 ft, even if the landing was acceptable. Unstable approaches that "work out" reinforce bad habits. |
| **Go-Around Confidence** | Students hesitate to go around because it feels like failure. Reframe: every go-around is a successful exercise of judgment. Require students to execute at least 2 go-arounds per pattern session. |
| **Speed Brake Effectiveness** | The A-10A speed brakes are very effective at reducing both airspeed and ground roll distance. Teach students to use them IMMEDIATELY on touchdown for short-field and any time rollout distance is a concern. |
| **Shutdown Discipline** | Even in DCS, enforce the 2-minute cool-down at idle before engine shutdown. This builds the habit for students who may transition to higher-fidelity modules (A-10C II) where thermal management matters more. |

---

## Appendix A — Quick Reference Card

### Engine Limits

| Parameter | Normal | Transient | Start | Emergency |
|---|---|---|---|---|
| **EGT** | ≤ 650°C | ≤ 690°C (10 sec) | ≤ 725°C | N/A |
| **N2 RPM** | ≤ 100% | — | — | — |
| **Oil Pressure** | 25–65 PSI | — | — | Min 15 PSI |

### V-Speed Summary

| Speed | Light (< 35K) | Medium (35–42K) | Heavy (> 42K) |
|---|---|---|---|
| **Vr (Rotation)** | ~105 KIAS | ~115 KIAS | ~130 KIAS |
| **V2 (OEI Safety)** | ~120 KIAS | ~130 KIAS | ~145 KIAS |
| **Vmca** | ~110 KIAS | ~115 KIAS | ~120 KIAS |
| **Vref (Final)** | ~120 KIAS | ~130 KIAS | ~140 KIAS |
| **Best Glide** | ~200 KIAS (clean) | ~200 KIAS | ~210 KIAS |

### Configuration Limits

| Configuration | Max Speed |
|---|---|
| **Clean (Vne)** | 450 KIAS / Mach 0.75 |
| **Gear Extended** | 200 KIAS |
| **Flaps (MVR or DN)** | 200 KIAS |
| **Speed Brakes** | No restriction |

### G-Limits

| Configuration | Positive G | Negative G |
|---|---|---|
| **Clean** | +7.33 G | −3.0 G |
| **With Stores** | Varies by loading | Reduced |

### Weight Summary

| Parameter | Value |
|---|---|
| **Empty Weight** | ~24,960 lbs |
| **Internal Fuel** | ~10,700 lbs |
| **MTOW** | ~50,000 lbs |
| **Max Landing Weight** | ~42,000 lbs (recommended) / 46,000 lbs (structural) |

---

## Appendix B — Complete DCS FC3 Keybind Reference

### Flight Controls

| Action | Default Keybind |
|---|---|
| Pitch Up | Stick back / `Num 2` (numpad) |
| Pitch Down | Stick forward / `Num 8` (numpad) |
| Roll Left | Stick left / `Num 4` (numpad) |
| Roll Right | Stick right / `Num 6` (numpad) |
| Rudder Left | Pedal left / `Z` |
| Rudder Right | Pedal right / `X` |
| Pitch Trim Up | `RCtrl + ;` |
| Pitch Trim Down | `RCtrl + .` |
| Roll Trim Left | `RCtrl + ,` |
| Roll Trim Right | `RCtrl + /` |
| Rudder Trim Left | `RCtrl + Z` |
| Rudder Trim Right | `RCtrl + X` |
| Autopilot Engage/Disengage | `A` |

### Engine

| Action | Default Keybind |
|---|---|
| Throttle Up | `Num +` / HOTAS |
| Throttle Down | `Num -` / HOTAS |
| Left Engine Start | `RAlt + Home` |
| Right Engine Start | `RCtrl + Home` |
| Left Engine Stop | `RAlt + End` |
| Right Engine Stop | `RCtrl + End` |
| Electrical Power | `RShift + L` |

### Landing Gear, Flaps, Brakes

| Action | Default Keybind |
|---|---|
| Gear Toggle | `G` |
| Flaps Up (one step) | `LShift + F` |
| Flaps Down (one step) | `LCtrl + F` |
| Speed Brakes Toggle | `B` |
| Speed Brakes Open | `LShift + B` |
| Speed Brakes Close | `LCtrl + B` |
| Wheel Brakes | `W` (hold) |
| Parking Brake | `LCtrl + W` (toggle) |

### Systems & Miscellaneous

| Action | Default Keybind |
|---|---|
| Canopy Open/Close | `LCtrl + C` |
| Eject | `LCtrl + E` × 3 |
| Emergency Jettison (All Stores) | `LAlt + R` |
| Navigation Lights | `RCtrl + L` |
| Landing/Taxi Light | `L` |
| Smoke On/Off | `T` |
| Altimeter QNH Increase | `RAlt + Num+` |
| Altimeter QNH Decrease | `RAlt + Num-` |

### Communications

| Action | Default Keybind |
|---|---|
| Open Comm Menu | `\` (backslash) |
| Menu Selection | `F1` – `F12` |
| IFF Interrogate | `I` |
| IFF Mode | `RAlt + I` |

### Views (Common)

| Action | Default Keybind |
|---|---|
| Cockpit View | `F1` (outside comm menu) |
| External View | `F2` |
| Fly-By View | `F3` |
| Padlock (Nearest Enemy) | `Num .` (numpad delete) |
| Snap View: Forward | `Num 5` (numpad) |
| Look Around (Mouse) | Hold `RAlt` + mouse move |

---

## Appendix C — BQT Syllabus Overview

### Course Structure: 7 Modules

| Module | Title | Key Topics |
|---|---|---|
| **1** | Aircraft Systems & Aerodynamics | TF34 engines; fuel system; flight controls; manual reversion; survivability; stall characteristics |
| **2** | Ground Operations & Startup | FC3 startup sequence; EGT monitoring; taxi; before-takeoff checks |
| **3** | Communications | Easy Comm system; radio phraseology; SRS introduction; IFF; guard frequencies |
| **4** | Takeoff & Departure | Normal and short-field takeoff; V-speeds; abort; engine failure on takeoff; departures |
| **5** | Flight Maneuvers & Airwork | Level flight; turns; stall series; slow flight; single-engine flight; traffic pattern; speed limits |
| **6** | Emergency Procedures | Boldface procedures; engine fire; dual engine failure; manual reversion; ejection; emergency jettison |
| **7** | Approach & Landing | Normal, short-field, crosswind, single-engine, and no-flap landings; go-around; shutdown |

### Recommended Training Flow

| Phase | Description | Estimated Flights |
|---|---|---|
| **Phase 1: Ground School** | Modules 1–3 (systems, ground ops, comms) — classroom/briefing only | 0 flights (study) |
| **Phase 2: First Flight** | Module 2 (startup) → Module 4 (takeoff) → Module 5 (basic airwork) → Module 7 (landing) | 2–3 flights |
| **Phase 3: Pattern Work** | Module 5 (pattern) + Module 7 (normal/crosswind landings, go-arounds) | 3–5 flights |
| **Phase 4: Emergency Training** | Module 6 (single-engine, engine failure, manual reversion, ejection decision) | 2–3 flights |
| **Phase 5: Consolidation** | Full mission profile: startup → taxi → takeoff → area work → pattern → landing → shutdown | 2–3 flights |
| **Phase 6: Checkride** | All modules — demonstrated proficiency in all maneuvers and procedures | 1 flight |

### Checkride Standards

| Maneuver | Standard |
|---|---|
| Startup | Complete within 3 minutes; no hot starts |
| Takeoff | Centerline ±10 ft; rotate within ±5 KIAS of Vr |
| Level Flight | Altitude ±100 ft; heading ±5°; airspeed ±10 KIAS |
| Steep Turns (45°) | Altitude ±100 ft; airspeed ±10 KIAS; bank ±5° |
| Stall Recovery | Recover within 500 ft of stall altitude; maintain heading ±10° |
| Traffic Pattern | Altitude ±100 ft on downwind; aligned on final by 300 ft AGL |
| Normal Landing | Touchdown in first third of runway; within ±15 ft of centerline |
| Single-Engine Approach | Maintain ≥ Vmca throughout; landing within first half of runway |
| Go-Around | Initiate before 200 ft AGL if unstable; positive rate before crossing departure end |
| Emergency Procedures | Boldface items from memory; correct identification and response |

---

## Appendix D — Corrections from Previous Dossier

This appendix documents specific errors found in the previous version of this dossier and the corrections applied in this version.

| Item | Previous (Incorrect) Value | Corrected Value | Source / Rationale |
|---|---|---|---|
| **EGT Start Limit** | 649°C (1,200°F) | 725°C (1,337°F) | TF34-GE-100 engine specifications; 649°C is below continuous limit which makes no sense as a start transient peak |
| **EGT Continuous Limit** | 607°C (1,125°F) | 650°C (1,202°F) | TF34-GE-100 specifications; 607°C was understated |
| **Glide Ratio (Clean)** | 17:1 | 8–10:1 | Aerodynamic analysis; 17:1 would require sailplane-like L/D; the A-10A's fuselage, nacelles, pylons, and gun pod create substantial parasite drag |
| **Emergency Jettison Keybind** | `LCtrl + W` | `LAlt + R` | `LCtrl + W` is parking brake in DCS FC3; emergency jettison is `LAlt + R` |
| **NWS Authority** | ±60° | ±45° (primary mode) | Real A-10A NWS primary mode is ~±45°; ±60° only achievable in free-castering (NWS off) with differential braking |
| **Module Structure** | 6 modules (no Communications) | 7 modules (Communications added as Module 3) | Communications is essential for BQT; all other aircraft dossiers include it |
| **Parking Brake Keybind Conflict** | Listed as both parking brake AND emergency jettison (`LCtrl + W`) | Parking brake = `LCtrl + W`; Emergency jettison = `LAlt + R` | These are distinct functions with distinct keybinds; conflating them is dangerous |

---

*Research compiled for checklist-heaven DCS World aviation checklist project. Based on publicly available excerpts from T.O. 1A-10A-1, General Electric TF34 engine specifications, USAF flying operations manuals, and verified DCS FC3 module behavior. For simulation training use only.*
