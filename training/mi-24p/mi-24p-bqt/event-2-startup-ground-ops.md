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
CB HANDLES RAISED → BATTERY 1 & 2 ON → POWER FROM BATTERY ON → INVERTER #1 ON
→ FUEL VALVES/PUMPS → THROTTLE FULL LEFT → ROTOR BRAKE OFF
    │
    ▼
APU START (AI-9V) → Monitor EGT < 720°C, Air Pressure, RPM → WAIT 1 MIN MINIMUM
    │
    ▼
LEFT ENGINE START → N1 rises → push FUEL SHUTOFF LEVER FORWARD → governed 70-75% → LEFT GEN ON
    │
    ▼
RIGHT ENGINE START → same sequence → RIGHT GEN ON
    │
    ▼
POST-START ELECTRICAL: POWER FROM BATTERY OFF → INVERTER OFF → TRANSFORMERS MAIN → RECTIFIERS ON → APU OFF
    │
    ▼
AVIONICS ON (both cockpits — switch seats as needed)
    │
    ▼
THROTTLE TO MAX (PgUp) → Governor engages → Nr climbs to 95%
    │
    ▼
PRE-TAKEOFF CHECK
    │
    ▼
READY TO TAXI / HOVER TAXI
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

### Step 2 — Pre-Electrical Setup (Before Battery ON)

Per the DCS Mi-24P Guide, these switches must be set **before** Battery ON:

| Step | Action | Switch Location |
|---|---|---|
| 1 | Raise **Right Circuit Breaker Panel Handle** | Rear cockpit, right panel — sets all CBs to ON |
| 2 | Raise **Left Circuit Breaker Panel Handle** | Rear cockpit, left panel — sets all CBs to ON |
| 3 | **Battery 1** — ON | Overhead panel, electrical section |
| 4 | **Battery 2** — ON | Overhead panel, electrical section |
| 5 | **DC selector knob** — BATT | Overhead electrical panel |
| 6 | Verify DC voltmeter reads ≥ 24V | Overhead panel |
| 7 | **POWER FROM BATTERY switch** (flip safety cover) — ON | Overhead panel |
| 8 | **Inverter #1 (PO-750)** (flip safety cover) — ON | Overhead panel |
| 9 | **AC selector knob** — 115 (Inverter) | Overhead panel |
| 10 | Mute **RI-65 aural warnings** (Nadia) | Press RI-65 OFF button |
| 11 | **Fire Extinguisher System Power** — ON | Overhead panel |
| 12 | **Engine Fuel Feed Valves** (Service Tank 1 & 2) — OPEN | Overhead fuel panel |
| 13 | **Engine Fuel Shutoff Valves** (L & R) — OPEN | Overhead fuel panel |
| 14 | **Fuel Pump switches** (cells 1, 2, 4, 5) — ON | Overhead fuel panel |
| 15 | **ECL (Engine Control Levers)** — confirm MIDDLE detent | Left console |
| 16 | **Throttle Twist Grip** — FULL LEFT (minimum) | Collective grip (`PgDn` binding) |
| 17 | **Rotor Brake** — OFF (fully disengaged) | Left console |
| 18 | **Parking Brake** — SET (`LShift + W`) | — |

### Step 3 — APU Start (AI-9V)

| Step | Action | Notes |
|---|---|---|
| 19 | **APU Mode Switch** — START (down) | APU panel |
| 20 | **APU START button** — PRESS and hold ~4 sec | AUTO ON annunciator should illuminate |
| 21 | Monitor APU EGT, Air Pressure, Oil Pressure rising | Check within 9 seconds |
| 22 | Wait for: APU EGT < **720°C**, Air Pressure 1.2–2.0 kg/cm², APU NORMAL RPM annunciator | ~20–60 sec |
| 23 | **Minimum 1 minute APU run** before starting main engines | Required for APU protection |
| 24 | Verify APU ON (RUNNING) annunciator illuminated | — |

### Step 4 — Left Engine Start

| Step | Action | Notes |
|---|---|---|
| 25 | Confirm rotor brake **OFF** | — |
| 26 | Select **START mode** on starter panel | — |
| 27 | Select **Left Engine** | — |
| 28 | **START button** — PRESS 2–3 sec (`RAlt + Home`) | AUTO ON and STARTER ON annunciators illuminate; oil pressure rising |
| 29 | Once N1 begins rising → push **Left Engine Red Fuel Shutoff lever (Engine Stop) FORWARD** | CRITICAL: this introduces fuel; without it engine cranks but won't light off |
| 30 | Monitor left EGT — must stay below **830°C** | Abort if exceeded |
| 31 | STARTER ON extinguishes at **60–65% N1** | — |
| 32 | Wait for N1 to reach **70–75%** (ground idle) | Not 63–65%; engine continues spinning up after starter cuts |
| 33 | Verify oil pressure ≥ 1 kg/cm² at 45% N1; then 3–4.5 kgf/cm² at idle | — |
| 34 | **Left Generator** — ON | Overhead electrical panel |

> **DCS Key:** `RAlt + Home` — triggers left engine start sequence

### Step 5 — Right Engine Start

| Step | Action | Notes |
|---|---|---|
| 35 | Select **Right Engine** | — |
| 36 | **START button** — PRESS 2–3 sec (`RCtrl + Home`) | — |
| 37 | Push **Right Engine Red Fuel Shutoff lever FORWARD** | Same as left engine — required for fuel flow |
| 38 | Monitor right EGT — stay below **830°C** | — |
| 39 | Wait for N1 **70–75%** (ground idle) | — |
| 40 | **Right Generator** — ON | — |
| 41 | Both engines at idle — **main rotor speed 45–70% Nr** (governor not yet engaged) | — |

> **DCS Key:** `RCtrl + Home` — triggers right engine start sequence

### Step 6 — Post-Start Electrical

| Step | Action | Notes |
|---|---|---|
| 42 | Verify generators online: LH/RH GEN OUT annunciators extinguish; GEN PARAL'D illuminates | — |
| 43 | **POWER FROM BATTERY switch** — OFF | — |
| 44 | **Inverter #1 (PO-750)** — OFF | — |
| 45 | **36V & 115V Transformer switches** — MAIN | — |
| 46 | **Rectifiers (L & R)** — ON | LH/RH RECT OFF annunciators extinguish |
| 47 | **APU** — OFF (press APU OFF button) | — |
| 48 | **Air Conditioner** — CONDITION | — |

### Step 7 — Rotor Engagement (Engine Run-Up)

| Step | Action | Notes |
|---|---|---|
| 49 | **Engine Dust Protector System Power** — ON | Wait for oil temps: engine > +30°C, main gearbox > -15°C |
| 50 | **Collective** — FULL DOWN | Minimum pitch |
| 51 | **Throttle Twist Grip** — advance to **MAX** (`PgUp`) | Governor engages; Nr rises to **95%** |
| 52 | Verify Nr stable at **95%** | Governor holding; ±2% acceptable |
| 53 | Engine instruments — verify normal | EGT, torque, oil pressure all in green |

### Step 8 — WSO Cockpit (Front) Setup

Switch to front cockpit: press `1`.

| Step | Action | Notes |
|---|---|---|
| 54 | **Armament Circuit Breakers** — ON | Front cockpit |
| 55 | **Weapons master arm** — SAFE | ACP, center console |
| 56 | **All weapon switches** — SAFE/OFF | Verify rockets, ATGM, cannon all safe |
| 57 | **Countermeasure Dispenser Selectors** — ON | — |
| 58 | **Magnetic Variation** — set per theater | Caucasus +6.4°, Syria +5.0°, Nevada +14.2° |
| 59 | **SPO-10 (or Beryoza) RWR** — (set by Pilot) | — |

Switch back to rear cockpit: press `2`.

### Step 9 — Avionics (Pilot Rear Cockpit)

| Step | Action | Notes |
|---|---|---|
| 60 | **ICS switches (NET 1 & 2)** — ON | — |
| 61 | **R-863 UHF radio** — ON, set frequency | — |
| 62 | **R-828 VHF/FM radio** — ON, set frequency | — |
| 63 | **Radar altimeter** — ON | Set decision height bug |
| 64 | **DISS-15 Doppler** — ON | Ground speed/drift; 2–3 min warm-up |
| 65 | **Vertical Gyros 1 & 2** — ON; cage each (2-sec press) | Confirm VERT GYRO FAIL extinguishes |
| 66 | **GREBEN-1 Course Control** — ON | Wait 3 min; then SYNC → MAG mode |
| 67 | **SPO-10 RWR** — ON, sound ON | — |
| 68 | **IFF** — STANDBY | — |
| 69 | **ARK-U2/ARK-15 ADF** — ON; mode → COMPASS | — |
| 70 | **SPUU-52 Tail Rotor Pitch Limit** — ON | — |
| 71 | **Autopilot Roll and Pitch channels** — ENGAGE | DO NOT engage Yaw channel |
| 72 | Lights: Navigation, Formation, Blade Tip, Anti-Collision — ON | — |
| 73 | Allow nav systems to warm up | DISS-15: 2–3 min; gyros: 1–2 min |

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
