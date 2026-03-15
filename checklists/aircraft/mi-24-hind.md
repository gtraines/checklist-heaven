# Mi-24P Hind — DCS Checklist

> **Aircraft:** Mil Mi-24P Hind-F | **Role:** Attack / Gunship Helicopter
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [Cockpit Orientation](#cockpit-orientation)
2. [Crew Positions](#crew-positions)
3. [Operating Limitations](#1-operating-limitations)
4. [Performance & V-Speeds](#2-performance--v-speeds)
5. [Emergency Procedures](#3-emergency-procedures-immediate-action)
6. [Weapons & Stores](#4-weapons--stores)
7. [Startup Checklist](#startup-checklist)
8. [Hover & Takeoff](#hover--takeoff)
9. [Navigation](#navigation)
10. [Avionics & Systems](#avionics--systems)
11. [Weapons Employment](#weapons-employment)
   - [GSh-30-2 30mm Cannon](#gsh-30-2-30mm-cannon)
   - [Unguided Rockets (S-8/S-24)](#unguided-rockets)
   - [9M114 Shturm ATGM](#9m114-shturm-atgm)
   - [9M120 Ataka ATGM](#9m120-ataka-atgm)
   - [R-60 / R-73 AAM](#r-60--r-73-aam)
12. [Defensive Systems](#defensive-systems)
13. [Landing Checklist](#landing-checklist)
14. [Shutdown Checklist](#shutdown-checklist)
15. [Keyboard & Joystick Reference](#keyboard--joystick-reference)

---

## Cockpit Orientation

The Mi-24P has two crew positions:
- **Front cockpit** — Weapons Systems Officer (WSO/Gunner)
- **Rear cockpit** — Pilot

```
Front Cockpit (WSO):
┌──────────────────────────────────────────┐
│  PKV Sight         SHORAN panel          │
│  Weapon controls   Weapon selector       │
│  Ataka/Shturm sight panel                │
└──────────────────────────────────────────┘

Rear Cockpit (Pilot):
┌──────────────────────────────────────────┐
│  Flight instruments   Engine gauges      │
│  Autopilot panel      Navigation         │
│  Collective/Cyclic                       │
└──────────────────────────────────────────┘
```

---

## Crew Positions

| Position | Seat | Primary Function | Key |
|---|---|---|---|
| Pilot | Rear | Fly the aircraft | Default spawn |
| Weapons Systems Officer | Front | Operate weapons and sights | Switch: `2` |

In single-player: switch between positions by pressing `2` (rear) or `1` (front).

## 1. Operating Limitations

| Parameter | Limit | Notes |
|---|---|---|
| **Max Takeoff Weight (MTOW)** | **11,500 kg** (25,353 lbs) | Normal max. Overload TO possible. |
| **Max Landing Weight** | **11,500 kg** | Same as MTOW for normal ops. |
| **G-Limits** | **+3.5 G / -0.5 G** | Hard banking increases load factor rapidly. |
| **VNE (Never Exceed)** | **300 km/h** (162 kts) | Retreating blade stall risk beyond this. |
| **Max Autorotation Entry** | **220 km/h** | Initiate below this speed. |
| **Max Sideward Flight** | **50 km/h** | Lateral limit to avoid tail rotor issues. |
| **Max Backward Flight** | **40 km/h** | Rearward speed limit. |
| **Rotor RPM (Normal)** | **92-98%** | Nominal operating range. |
| **Crosswind Component** | **12 m/s** (~23 kts) | Landing/Takeoff limit. |

## 2. Performance & V-Speeds

| Regime | Speed (km/h) | Configuration / Notes |
|---|---|---|
| **VNE (Never Exceed)** | **300** | Structural/aeroelastic limit. |
| **Cruise Speed** | **260** | Normal cruise (loaded). |
| **Best Range** | **220** | Fuel-optimal cruise. |
| **Best Endurance** | **120** | Max loiter time. |
| **Autorotation** | **170** | Optimal glide speed. |
| **Max Climb Rate** | **~12 m/s** | Clean, sea level. |
| **Sideward Flight** | **< 50** | Lateral maneuver limit. |
| **Backward Flight** | **< 40** | Rearward maneuver limit. |

## 3. Emergency Procedures (Immediate Action)

| Emergency | Immediate Action Steps |
|---|---|
| **Engine Failure (Single)** | 1. **Collective** — ADJUST for level flight<br>2. **Fuel Feed** — CROSS-FEED OPEN<br>3. **Failed Engine** — IDLE, then OFF<br>4. **Airspeed** — 160-180 km/h<br>5. **Land** — ASAP |
| **Engine Failure (Dual)** | 1. **Collective** — LOWER IMMEDIATELY<br>2. **Airspeed** — 170 km/h<br>3. **Rotor RPM** — Maintain 92-98%<br>4. **Flare** — At ~30-50m AGL<br>5. **Collective** — PULL at 5-10m<br>6. **Touchdown** — Level skids |
| **Tail Rotor Failure** | 1. **Airspeed** — INCREASE > 120 km/h<br>2. **Collective** — Control yaw with power<br>3. **Land** — ASAP (Running landing)<br>4. **Do NOT Hover** |
| **Engine Fire** | 1. **Throttle** — IDLE then OFF<br>2. **Fire Extinguisher** — DISCHARGE<br>3. **Land** — ASAP |
| **Hydraulic Failure** | 1. **Force Trim** — Use to assist<br>2. **Airspeed** — Reduce < 150 km/h<br>3. **Land** — ASAP |
| **Crew Egress** | 1. **Autorotate** — To suitable area<br>2. **Doors/Windows** — KICK OUT<br>3. **Exit** — Rapidly |

## 4. Weapons & Stores

| Weapon / System | Type | Effective Range | Best Suited For | Simulation Notes |
|---|---|---|---|---|
| **GSh-30K** | 30mm Twin Cannon | < 1.5 km | Light Armor, APCs, Trucks | Fixed starboard mount. Pilot aims aircraft. |
| **9M114 Shturm** | ATGM (Radio) | 400m - 5 km | **Primary Anti-Tank**, MBTs | Operator keeps crosshair on target. Steady flight required. |
| **9M120 Ataka** | ATGM (Radio) | 400m - 6 km | MBTs, IFVs, Bunkers | Faster, longer range than Shturm. |
| **S-8 Rockets** | 80mm Unguided | 1-2 km | Soft targets, Light armor | 20-round B-8V20A pods. CCIP/Manual. |
| **S-13 Rockets** | 122mm Unguided | 1-2.5 km | Bunkers, Light Vehicles | 5-round O-25 pods. Heavy punch. |
| **S-24 Rockets** | 240mm Heavy | 2-3 km | Hardened targets | Single rail. Powerful, inaccurate without ranging. |
| **9M39 Igla** | IR Air-to-Air | 0.5 - 5 km | Helicopters, Low Aircraft | All-aspect IR. External rail. |
| **FAB-100/250** | GP Bomb | Overflight | Soft area targets | Low altitude delivery. |
| **RBK-250** | Cluster Dispenser | Area | Soft target concentrations | Area denial. Low altitude pass. |

## Realism Notes
*   **Cannon Variant:** The Mi-24P ('P' for Pushka - cannon) is distinct from the Mi-24V in that it uses a fixed, side-mounted twin-barrel 30mm GSh-30K cannon rather than the flexible 12.7mm Yak-B turret. This requires the pilot to aim the entire helicopter at the target.
*   **ATGM Guidance:** The Shturm and Ataka missiles are radio-command guided. In the simulation (and reality), the Weapons Operator must maintain the sight crosshair on the target until impact. The pilot must fly a steady profile to avoid masking the guidance antenna or exceeding the seeker's field of view.
*   **Crew Roles:** The DCS module accurately simulates the division of labor: Pilot flies and fires fixed forward weapons (rockets, cannon), while the Weapons Operator (front seat) manages the guided missiles (ATGMs) and detection systems.

---

## Startup Checklist

### Pre-Start (Rear Cockpit — Pilot)
- [ ] **Parking Brake** — SET (`W`)
- [ ] **All switches** — OFF/SAFE
- [ ] **Collective** — full DOWN
- [ ] **Throttle** — IDLE detent

### Engine Start (Isotov TV3-117V × 2)
- [ ] **APU** — START (if available)
  - APU provides electrical/hydraulic power for start
- [ ] **Battery / Generator** — ON
- [ ] **Left Engine Start** — `RAlt + Home`
  - NG% rising
  - TIT (Turbine Inlet Temp) — monitor (max 830°C during start)
  - NG > 60% — engine running stable
- [ ] **Right Engine Start** — `RCtrl + Home`
  - Same procedure
- [ ] Both engines at IDLE — confirm RPM ~70%
- [ ] **Rotor RPM** — rising toward 95% (95% = flight RPM)
- [ ] **Governor** — ON (maintains 95% rotor RPM)
- [ ] **APU** — OFF after generators stable
- [ ] **Hydraulics** — check normal
- [ ] **Avionics warm-up** — 3–5 minutes

### Avionics Power-On
- [ ] **Navigation system** — ON
- [ ] **PKV Sight system** — ON (front cockpit)
- [ ] **Ataka/Shturm guidance** — ON
- [ ] **SPO-15 RWR** — ON
- [ ] **UV-26 chaff/flare** — ON, program selected
- [ ] **Radios** — ON, frequencies set
  - R-863 UHF
  - R-828 VHF/FM

---

## Hover & Takeoff

### Before Takeoff
- [ ] **Rotor RPM** — 95%
- [ ] **Engine temps** — normal
- [ ] **Hydraulics** — normal
- [ ] **Weapon safeties** — SAFE until operational

### Hover
1. Smoothly raise collective to achieve light on wheels
2. Left pedal input with power application (counter torque)
3. Hover at 5–10 m AGL — Mi-24 needs more forward speed than UH-1
4. **Minimum ETL** in hover is poor — Mi-24 is heavy; hover endurance is short

### Takeoff
1. Push cyclic forward for translational flight
2. Climb at **120 kph** for best rate
3. ETL at ~50 kph
4. Max speed: **330 kph** (Mi-24P is fast for a helicopter)
5. Normal cruise: **220–250 kph**

> **Note:** The Mi-24P can be flown like a fixed-wing aircraft at high speed — it has wings that provide lift.

---

## Navigation

### Navigation System (PNK-800 / ARK-15)
- [ ] **ARK-15 ADF** — power ON, tune to NDB
- [ ] **RSBN** — tune to beacon if available
- [ ] **PNK-800** — set waypoints if equipped

### Navigation Tips
- Mi-24 operates at medium altitudes (500–2,000 m) more comfortably than NOE
- Use speed for survivability — 250+ kph
- Plan attack corridors with escape routes

---

## Avionics & Systems

### PKV-8 Sight (Front Cockpit)
- Primary targeting system for WSO
- Used for cannon, rockets, and ATGM guidance
- [ ] **PKV Power** — ON
- [ ] Reticle indicates weapon aim point
- [ ] Gyro stabilized — effective from moving aircraft

### SPO-15 Beryoza RWR
*(Same as Su-25T — see [Su-25T SPO-15](su-25t.md#spo-15-beryoza-rwr))*

### Autopilot
- [ ] **Autopilot** — engages multiple channels:
  - Roll stabilization
  - Pitch stabilization
  - Heading hold
  - Altitude hold
- [ ] Enables hands-off weapon employment

---

## Weapons Employment

### Weapon Stations

| Station | Weapon Options |
|---|---|
| Outboard pylons (4) | S-8/S-24 rockets, Ataka ATGM, Shturm ATGM |
| Fixed nose cannon | GSh-30-2 30mm (Mi-24P) |

### Master Arm
- [ ] **Weapon Master** — ARMED (`O` key)
- [ ] **Weapon select** — choose on front cockpit panel

---

### GSh-30-2 30mm Cannon

The Mi-24P carries a fixed twin-barrel 30mm cannon (replacing the Yak-B).

#### Employment
1. [ ] **Gun select** — cannon mode
2. [ ] Align aircraft nose on target (cannon is fixed)
3. [ ] Dive angle: 10°–20°
4. [ ] Open fire: 1,000–1,500 m
5. [ ] Short bursts: 1–2 seconds
6. [ ] Pull off at 400 m minimum

> **Note:** The fixed cannon means the pilot must point the whole aircraft. Coordinate with WSO for rocket/ATGM.

---

### Unguided Rockets

#### S-8 (80mm) / S-24 (240mm)

1. [ ] **Select rockets** on weapon panel (front cockpit)
2. [ ] Set salvo: 1, 2, or 4 rockets
3. [ ] Dive approach: 15°–25°
4. [ ] WSO aims via PKV sight; pilot flies
5. [ ] Fire at 1,200–2,000 m: `Space`
6. [ ] Pull off at 600 m minimum

---

### 9M114 Shturm ATGM

Radio-command guided (SACLOS) anti-tank missile.

| Spec | Value |
|---|---|
| Range | 400 m – 5,000 m |
| Guidance | SACLOS (Joystick manual guidance) |
| Warhead | HEAT (anti-armor) |
| Penetration | 600 mm RHA |

#### Shturm Employment
1. [ ] **Select Shturm** on weapon panel
2. [ ] **Sight** — PKV aimed at target
3. [ ] Approach: level flight or shallow dive, 2–4 km range
4. [ ] **Fire:** `Space`
5. [ ] **Manual guidance** — use joystick hat/keyboard to fly missile onto target
6. [ ] Keep PKV sight on target throughout flight (~10 sec to max range)

> **Note:** Shturm requires constant manual correction — practice required!

---

### 9M120 Ataka ATGM

Improved SACLOS missile with greater range.

| Spec | Value |
|---|---|
| Range | 400 m – 6,000 m |
| Guidance | SACLOS (radio-command) |
| Warhead | HEAT or Thermobaric |
| Penetration | 800 mm RHA |

#### Ataka Employment
1. [ ] **Select Ataka** on weapon panel
2. [ ] Same SACLOS guidance as Shturm
3. [ ] Greater range allows engagement from outside most MANPADS
4. [ ] Fire at 4–5 km for maximum standoff

---

### R-60 / R-73 AAM

Self-defense air-to-air missiles for fixed-wing threats.

#### R-60 (Short Range IR)
1. [ ] Select R-60
2. [ ] Tone on lock
3. [ ] Fire: `Space`

#### R-73 (Agile IR with helmet cueing)
1. [ ] Select R-73
2. [ ] Look at target (helmet sight if equipped)
3. [ ] Tone — fire

---

## Defensive Systems

### SPO-15 Beryoza
*(Same as Su-25T — see [Su-25T Defensive](su-25t.md#defensive-systems))*

### UV-26 Chaff/Flare System
- [ ] **UV-26** — ON, program selected
- [ ] **Chaff** — `[`
- [ ] **Flares** — `]`
- [ ] Automatic program: engages on IR/radar lock
- Standard break: hard jink + flares

### Tactical Defensive Procedures
1. Never hover in SAM/AAA threat area
2. Use terrain masking
3. High-speed attack runs at 250+ kph reduce exposure time
4. After weapons employment, immediately break off

---

## Landing Checklist

### Approach
1. Reduce speed: 120 → 80 → 60 kph on final
2. Begin deceleration at 500 m from intended landing point
3. Arrive at hover, 5–10 m AGL
4. **Pedal** to align with landing direction
5. Lower collective — set down

### Running Landing
1. Maintain 40–50 kph to touchdown
2. Lower collective on contact
3. Wheel brakes if available

---

## Shutdown Checklist

- [ ] **Set down** at parking
- [ ] **Parking Brake** — SET (`W`)
- [ ] **Weapon systems** — SAFE
- [ ] **Throttle** — IDLE
- [ ] Cool engines: 2 minutes at IDLE
- [ ] **Throttle** — CUT-OFF
- [ ] **Avionics** — all OFF
- [ ] **Battery** — OFF

---

## Emergency Procedures

### Engine Failure (Single)
1. Maintain altitude with remaining engine
2. Reduce load — jettison stores if required (`LAlt + J`)
3. Land at nearest suitable area

### Engine Failure (Dual) — Autorotation
1. **COLLECTIVE** — lower immediately
2. Maintain rotor RPM in green band
3. Airspeed: 130–150 kph for best auto
4. Flare at 50 m AGL
5. Cushion landing with collective

### Tail Rotor Failure
1. Reduce collective/power
2. Running landing: maintain directional control with cyclic
3. Do not hover — tail rotor required for hover

---

## Keyboard & Joystick Reference

### Cockpit Switching
| Function | Key |
|---|---|
| Switch to Pilot (Rear) | `2` |
| Switch to WSO (Front) | `1` |

### Flight Controls
| Function | Key | Axis |
|---|---|---|
| Collective Up/Down | `PgUp / PgDn` | Collective axis |
| Pitch | `Numpad 8/2` | Stick Y |
| Roll | `Numpad 4/6` | Stick X |
| Yaw/Pedals | `Z / X` | Rudder axis |

### Weapons
| Function | Key |
|---|---|
| Master Arm | `O` |
| Fire | `Space` or trigger |
| Missile guide (SACLOS) | Joystick hat / Numpad |
| Chaff | `[` |
| Flares | `]` |
| Jettison | `LAlt + J` |

### Navigation
| Function | Key |
|---|---|
| F10 Map | `F10` |
| Radio Menu | `\` |

---

## Cross-References
- [UH-1H Huey →](uh-1h-huey.md)
- [OH-58D Kiowa →](oh-58d-kiowa.md)
- [9-Line CAS Procedures →](../procedures/9-line-cas.md)
- [Radio Communications →](../procedures/radio-communications.md)
- [Airfield & ATC →](../procedures/airfield-atc-communications.md)

---

*Based on Eagle Dynamics DCS Mi-24P documentation. For simulation use only.*

<!-- Co-authored-by: Copilot <223556219+Copilot@users.noreply.github.com> -->
