# Event 2 — Startup & Ground Operations

> **Course:** Mi-24P Hind Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [In-Sim Procedures](#in-sim-procedures)
4. [Completion Standards](#completion-standards)
5. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Set up the cold-and-dark cockpit in both the Pilot (rear) and WSO (front) positions
- [ ] Start the AI-9V APU and verify its readiness for engine start
- [ ] Start both TV3-117V engines in the correct sequence, monitoring EGT throughout
- [ ] Connect generators and verify electrical power on the main bus
- [ ] Bring all required avionics online (nav systems, RWR, communications)
- [ ] Engage the main rotor and verify Nr stabilizes at 95%
- [ ] Complete a pre-takeoff check
- [ ] Perform basic hover taxi from parking to a designated position
- [ ] Execute a complete shutdown sequence — both engines, rotor brake, cold-dark

---

## Ground Brief

### Why Startup Sequence Matters

The Mi-24P startup follows a specific order for system protection:
- **APU first** — provides DC power and bleed air for engine start
- **Left engine first** — then right (by convention; both via APU bleed)
- **Generator connection** — after each engine reaches governed speed
- **Avionics after generators** — avionics require stable power; starting them on battery stresses the system
- **Nav system warm-up** — Soviet inertial and Doppler systems need time to align/stabilize (DISS-15, ARK-15, RSBN)
- **Weapons SAFE** — the WSO verifies weapons safe early; never depart with uncertain weapons state

### DCS Seat Switching

In single-player DCS, you control both cockpits:

| Key | Seat | Role |
|---|---|---|
| `1` | **Front** | WSO — weapons, targeting, RWR |
| `2` | **Rear** | **Pilot** — flies the aircraft (default spawn) |

Before switching seats, **engage the autopilot** so the aircraft holds its attitude while you are "not at the controls."

### Understanding the Startup Flow

```
COLD DARK
    │
    ▼
BATTERY 1 & 2 ON (Pilot rear cockpit)
    │
    ▼
APU START (AI-9V) → APU running → green light
    │
    ▼
LEFT ENGINE START → N1 rises → EGT rises → governed speed → LEFT GEN ON
    │
    ▼
RIGHT ENGINE START → governed speed → RIGHT GEN ON
    │
    ▼
APU SHUTDOWN (auto, or manual)
    │
    ▼
AVIONICS ON (both cockpits — switch seats)
    │
    ▼
ROTOR ENGAGE (Nr climbs to 95%)
    │
    ▼
PRE-TAKEOFF CHECK
    │
    ▼
READY TO TAXI / HOVER TAXI
```

---

## In-Sim Procedures

### Step 1 — Cold-Dark Verify (Pilot Rear Cockpit)

Spawn into the Mi-24P. Default seat is Pilot (rear). Verify the cockpit is cold and dark:
- All gauges reading zero
- All lights dark
- Engines off

### Step 2 — Battery Power ON

| Step | Action | Switch Location |
|---|---|---|
| 1 | **Battery 1** — ON | Overhead panel, electrical section |
| 2 | **Battery 2** — ON | Overhead panel, electrical section |
| 3 | Verify cockpit instruments come alive | Gauges deflect to initial positions |

### Step 3 — APU Start (AI-9V)

| Step | Action | Notes |
|---|---|---|
| 4 | **APU fuel valve** — OPEN | APU fuel section |
| 5 | **APU START button** — PRESS | APU panel |
| 6 | Monitor APU EGT | Should rise, then stabilize |
| 7 | Wait for APU **READY** light | ~30–60 seconds |
| 8 | Verify APU running — ready for engine start | Green APU ready light ON |

### Step 4 — Left Engine Start

| Step | Action | Notes |
|---|---|---|
| 9 | **Left engine fuel cutoff lever** — IDLE position | Lever to idle/run position |
| 10 | **Left engine start button** — PRESS | Starter engages; N1 begins to rise |
| 11 | Monitor left EGT — do not exceed **900°C** | Watch throughout start sequence |
| 12 | Monitor N1 / Nr — left engine N1 rising | |
| 13 | Wait for left engine to reach governed speed | Nr contribution from left engine |
| 14 | **Left generator** — ON | Overhead electrical panel |
| 15 | Verify left generator on bus — indicator light | Electrical bus powered by left engine |

> **DCS Key:** `RAlt + Home` — left engine start (if using keyboard shortcut)

### Step 5 — Right Engine Start

| Step | Action | Notes |
|---|---|---|
| 16 | **Right engine fuel cutoff lever** — IDLE | |
| 17 | **Right engine START button** — PRESS | |
| 18 | Monitor right EGT — do not exceed **900°C** | |
| 19 | Wait for right engine to reach governed speed | |
| 20 | **Right generator** — ON | |
| 21 | Verify right generator on bus | Both engines and generators now online |

> **DCS Key:** `RCtrl + Home` — right engine start (if using keyboard shortcut)

### Step 6 — APU Shutdown

| Step | Action | Notes |
|---|---|---|
| 22 | **APU** — OFF (if not auto-shutdown) | APU normally shuts off automatically when generators come online |
| 23 | Verify APU READY light extinguishes | |

### Step 7 — WSO Cockpit (Front) Setup

Switch to front cockpit: press `1`.

| Step | Action | Notes |
|---|---|---|
| 24 | **Weapons master arm** — SAFE | Master arm switch SAFE |
| 25 | **All weapon switches** — SAFE/OFF | Verify rockets, ATGM, cannon all safe |
| 26 | **SPO-15 (Beryoza) RWR** — ON | RWR panel; allows threat detection |
| 27 | **UV-26 countermeasures** — ON | CM system panel; set to AUTO or MANUAL |
| 28 | **PKV sight** — OFF (not needed for BQT) | BQT does not include weapons employment |
| 29 | **Cockpit lighting** — adjust as needed | |

Switch back to rear cockpit: press `2`.

### Step 8 — Avionics (Pilot Rear Cockpit)

| Step | Action | Notes |
|---|---|---|
| 30 | **DISS-15 Doppler** — ON | Navigation — ground speed and drift data |
| 31 | **ARK-15 ADF** — ON | ADF for NDB navigation |
| 32 | **RSBN** — ON | RSBN nav system (Soviet TACAN equivalent) |
| 33 | **Radar altimeter (A-037)** — ON | Set decision height bug as needed |
| 34 | **R-863 UHF radio** — ON, set frequency | Set tower / departure frequency |
| 35 | **R-828 VHF/FM radio** — ON, set frequency | Team internal freq if applicable |
| 36 | **SPU-8 intercom** — ON | Crew intercom |
| 37 | Allow nav systems to warm up | DISS-15 requires 3–5 min; ARK-15 requires 2–3 min; RSBN requires 5–7 min |

> *⚠ Realism Divergence: DCS may abbreviate or skip alignment/warm-up delays for some systems. Real Soviet nav systems (DISS-15, RSBN) had significant warm-up requirements. DCS warm-up times may be shortened.*

### Step 9 — Autopilot Pre-Flight

| Step | Action | Notes |
|---|---|---|
| 38 | **Autopilot channels** — check each engages and disengages | Pitch, Roll, Heading, Altitude |
| 39 | **Force trim** — check function | Press and release; controls should hold in place |
| 40 | **Autopilot** — OFF for startup and taxi | Do not depart with AP engaged |

### Step 10 — Rotor Engagement

| Step | Action | Notes |
|---|---|---|
| 41 | **Collective** — FULL DOWN | Minimum pitch before engaging rotor |
| 42 | **Rotor engagement control** — ENGAGE | Rotor brake releases; rotor starts to turn |
| 43 | Monitor Nr — climbs from 0% | Should increase steadily |
| 44 | At ~80–85% Nr — verify no unusual vibrations | Watch for ground resonance onset |
| 45 | Nr stabilizes at **95%** | Governed by engine fuel controls |
| 46 | Engine instruments — verify normal | EGT, torque, oil pressure all in green |

> **Ground Resonance Watch:** During rotor engagement, if increasing vibration is felt — particularly a rhythmic "gallop" — this is ground resonance onset. At Nr < 90%: shut down immediately (collective down, fuel cutoffs). At Nr ≥ 90%: fly away immediately.

### Step 11 — Pre-Takeoff Check

Complete before any movement:

| Item | Check | Standard |
|---|---|---|
| **Nr** | 95% | Stable, within 92–98% |
| **EGT both engines** | In limits | < 800°C continuous |
| **Torque both engines** | In limits | Normal cruise settings |
| **Hydraulics** | Pressure normal | Main and backup indicators |
| **Flight controls** | FULL travel, no binding | Cyclic, collective, pedals |
| **Autopilot** | OFF | Not engaged for takeoff |
| **Gear** | DOWN — 3 green lights | Verified before taxi |
| **Weapons** | SAFE | Confirmed from both cockpits |
| **Fuel** | Quantity noted | > 300 kg minimum |
| **Instruments** | All alive and reading correctly | No flags, no off-scale |

### Step 12 — Hover Taxi to Position

For Event 2, the student will hover taxi from the parking spot to a designated point.

| Step | Action | Notes |
|---|---|---|
| 47 | **Collective** — increase smoothly to lift from the ground | Expect ~70–80% torque at training weight |
| 48 | At 3–5 m wheel height — stabilize in hover | This is a hover POWER CHECK point |
| 49 | **Torque check** — if torque > 85% to maintain hover, hover landing is marginal today | Note for approach planning |
| 50 | Hover taxi to designated point | Slow pace: 5–10 km/h |
| 51 | Maintain altitude and heading throughout | Small cyclic corrections; pedals for heading |
| 52 | Arrive at designated point — hold hover | Stabilize for 30 seconds |
| 53 | Set down smoothly | Lower collective; avoid bouncing |

### Step 13 — Shutdown Procedure

After the hover taxi exercise, shut down the aircraft:

| Step | Action | Notes |
|---|---|---|
| 54 | **Parking brake** — SET | |
| 55 | **Weapons** — verify SAFE | WSO confirms (or switch to seat 1) |
| 56 | **Avionics** — OFF (nav systems, radios, altimeter) | In order: RSBN, DISS-15, ARK-15, radios |
| 57 | **Autopilot** — verify OFF | |
| 58 | **Collective** — FULL DOWN | Minimum pitch |
| 59 | Allow engines to run at idle for **2 minutes** | Cool-down period — critical for turbine life |
| 60 | **Right engine fuel cutoff** — OFF | Right engine spools down |
| 61 | Wait for right engine to fully stop | |
| 62 | **Left engine fuel cutoff** — OFF | Left engine spools down |
| 63 | Wait for left engine to fully stop | |
| 64 | Monitor Nr — wait for Nr to drop below **50%** | |
| 65 | **Rotor brake** — apply gradually | Do NOT apply above 50% Nr |
| 66 | Rotor comes to full stop | |
| 67 | Switch to WSO cockpit (`1`) — cold-dark WSO | All WSO switches OFF/SAFE |
| 68 | Switch to Pilot cockpit (`2`) | |
| 69 | **Right generator** — OFF | |
| 70 | **Left generator** — OFF | |
| 71 | **Battery 2** — OFF | |
| 72 | **Battery 1** — OFF | Cockpit goes dark — COMPLETE |

---

## Completion Standards

| Standard | Requirement |
|---|---|
| **APU start** | APU started within 2 attempts; EGT monitored throughout |
| **Engine starts** | Both engines started without hot start (EGT < 900°C throughout) |
| **Engine order** | Left engine started before right |
| **Generator connection** | Both generators connected before avionics powered |
| **WSO cockpit** | Weapons verified SAFE; SPO-15 and UV-26 configured |
| **Rotor engagement** | Nr reaches 95% without ground resonance onset |
| **Pre-takeoff check** | Completed in order; no items omitted |
| **Hover taxi** | Altitude ±1 m during transit; no sudden power applications |
| **Shutdown order** | Correct sequence: avionics → cool-down → right engine → left engine → rotor brake → electrical |
| **Rotor brake timing** | Applied only after Nr < 50% |

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| Starting engines before APU is ready | Engine may not light; incomplete start | Wait for APU READY light before attempting engine start |
| Not monitoring EGT during start | Hot start goes undetected; engine damage | Eyes on EGT from the moment fuel is introduced until governed speed |
| Connecting generator before governed speed | Generator voltage spike; possible bus damage | Wait for full governed speed before connecting generator |
| Powering avionics on battery alone | Battery drain; alignment failures | Generators on the bus FIRST, then avionics |
| Applying rotor brake at high Nr | Rotor brake mechanism damage | Nr below 50% before any rotor brake application |
| Skipping engine cool-down | Thermal shock to turbine blades | Two full minutes at idle — watch the clock |
| Jerky hover taxi inputs | Altitude and position control lost | Slow, smooth cyclic inputs; anticipate the aircraft's response |

---

*Based on Mi-24P RLE and Eagle Dynamics DCS World Mi-24P Hind module documentation. For simulation use only.*
