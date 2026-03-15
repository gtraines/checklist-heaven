# Su-25T Frogfoot — DCS Checklist

> **Aircraft:** Sukhoi Su-25T Frogfoot-B | **Role:** Close Air Support / Ground Attack
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [Cockpit Orientation](#cockpit-orientation)
2. [Operating Limitations](#operating-limitations)
3. [Performance & V-Speeds](#performance--v-speeds)
4. [Emergency Procedures (Quick Ref)](#emergency-procedures-reference)
5. [Weapons & Stores (Quick Ref)](#weapons--stores-reference)
6. [Startup Checklist](#startup-checklist)
7. [Taxi & Takeoff](#taxi--takeoff)
8. [Navigation](#navigation)
9. [Avionics & Systems](#avionics--systems)
10. [Weapons Employment](#weapons-employment)
   - [Air-to-Ground Rockets & Guns](#air-to-ground-rockets--guns)
   - [Unguided Bombs](#unguided-bombs)
   - [Guided Weapons (Kh-25ML, Kh-29L/T, Kh-58)](#guided-weapons)
   - [TV/Laser Guided Bombs (KAB-500)](#tvlaser-guided-bombs)
   - [Anti-Radiation (Kh-58)](#anti-radiation-kh-58)
   - [SEAD Procedures](#sead-procedures)
11. [Defensive Systems](#defensive-systems)
12. [Landing Checklist](#landing-checklist)
13. [Shutdown Checklist](#shutdown-checklist)
14. [Emergency Procedures (Detailed)](#emergency-procedures)
15. [Keyboard & Joystick Reference](#keyboard--joystick-reference)

---

## Cockpit Orientation

```
┌─────────────────────────────────────────┐
│  HUD        ILS/NAV panel   MASTER ARM  │
│  MFD (Shkval)  Weapon Selector          │
│  Throttle   Gear/Flap       SPO-15 RWR │
└─────────────────────────────────────────┘
```

| Panel | Location | Function |
|---|---|---|
| Shkval MFD | Center instrument | TV targeting system |
| SPO-15 Beryoza | Right console | Radar Warning Receiver |
| EKRAN | Left instrument cluster | System warning display |
| Weapon selector | Right console | Selects weapon system |
| Autopilot panel | Left console | Route/altitude hold |

---

## Operating Limitations

| Parameter | Limit | Notes |
|---|---|---|
| **Max Takeoff Weight (MTOW)** | 19,500 kg (42,990 lbs) | Absolute max combat load |
| **Max Landing Weight** | 13,300 kg (29,321 lbs) | Risk of gear collapse above this limit* |
| **G-Limits** | +6.5 / -2.0 (Clean)<br>+5.0 (Loaded) | EKRAN provides audible "OVER-G" warning |
| **AoA Limits** | 20° (Clean)<br>16-18° (Loaded) | Critical AoA ~22°; Stall onset 18-20° |
| **Crosswind Component** | 15 m/s (~30 kts) | Ground handling degrades significantly >12 m/s* |
| **Max Mach** | M 0.82 | Airframe drag limit |

## Performance & V-Speeds

| Regime | Speed (km/h) | Configuration / Notes |
|---|---|---|
| **Rotation (Vr)** | 230 - 240 | Loaded (Clean: ~210) |
| **Takeoff Speed** | 260 - 270 | Lift-off speed |
| **Landing Approach** | 280 - 300 | Loaded / Heavy |
| **Landing Approach** | 250 - 260 | Clean / Light (Pattern speed) |
| **Corner Speed** | 450 - 550 | Best maneuvering range |
| **Best Climb (Vy)** | 550 - 600 | Clean |
| **Stall Speed (Vs)** | ~180 | Landing configuration (varies by weight) |
| **Max Speed (Vne)** | 950 | Sea Level (Structural limit >1000) |
| **Gear Extension (Vlo)** | 400 | Do not exceed or doors may jam |
| **Flaps Limit (Vfe)** | 500 (Maneuver)<br>400 (Landing) | Maneuver ~10°, Landing Full |
| **Drag Chute** | < 280 | Deploy on touchdown |

## Emergency Procedures (Quick Ref)

| Emergency | Immediate Action Steps |
|---|---|
| **Engine Failure on Takeoff** | 1. **Throttle** — IDLE<br>2. **Brakes** — MAX<br>3. **Drag Chute** — DEPLOY (`P`)<br>4. **Jettison Stores** — (`LCtrl + W`) |
| **Engine Fire in Flight** | 1. **Throttle** — IDLE (Affected Engine)<br>2. **Fire Extinguisher** — DISCHARGE (Auto/Manual)<br>3. **Engine** — SHUTDOWN (`RAlt + End` / `RCtrl + End`)<br>4. **Land ASAP** |
| **Engine Restart** | 1. **Throttle** — IDLE<br>2. **Airspeed** — 300-400 km/h<br>3. **Engine Start** — INITIATE (`RAlt + Home` / `RCtrl + Home`)<br>4. **Throttle** — ADVANCE slowly (>30% RPM) |
| **Hydraulic Failure** | 1. **Monitor** — Hydro 1/2 Pressures<br>2. **Gear** — EMERGENCY EXTEND (`LCtrl + G`)<br>3. **Flaps** — Plan for No-Flap Landing<br>4. **Brakes** — Expect failure (Use Chute) |
| **Electrical Failure** | 1. **Reduce Load** — Radar/EO/Lights OFF<br>2. **Battery** — Monitor (approx 20 min life)<br>3. **Land ASAP** |
| **Spin Recovery** | 1. **Throttle** — IDLE<br>2. **Stick** — NEUTRAL<br>3. **Rudder** — FULL OPPOSITE<br>4. **Recover** — Gentle pull-out |
| **Ejection** | 1. **Canopy** — JETTISON<br>2. **Eject** — INITIATE (`LCtrl + E` x3) |

## Weapons & Stores (Quick Ref)

| Weapon / System | Type | Effective Range | Best Suited For | Simulation Notes |
|---|---|---|---|---|
| **9A4172 Vikhr** | Beam Riding Missile | 8-10 km | **Anti-Tank (Primary)**, Helicopters | Requires continuous laser lock; fly straight during guidance |
| **Kh-29L** | Laser Missile | 8-10 km | Hardened Bunkers, Bridges | Heavy missile; requires Shkval laser lock |
| **Kh-29T** | TV Missile | 8-12 km | Pop-up attacks (High Threat) | **Fire & Forget**; Daylight only (Contrast lock) |
| **Kh-25MPU** | Anti-Radiation | 20-40 km | SEAD (Short/Med Range) | Requires **Phantasmagoria** pod |
| **Kh-58** | Anti-Radiation | 40-100+ km | SEAD (Long Range/High Value) | Requires **Phantasmagoria** pod |
| **FAB-500** | GP Bomb | CCIP | Soft targets, light vehicles | Accurate with CCIP; no guidance |
| **RBK-500** | Cluster Bomb | Area | Convoys, soft armor | Area denial; weak against MBTs in DCS |
| **S-8 / S-13** | Rockets | 1-2.5 km | Infantry, Trucks, BMPs | Fired in salvos; CCIP aimed |
| **GSh-30-2** | 30mm Cannon | < 1.5 km | Light Armor, Strafing | High recoil vibrates HUD; limited ammo |
| **Mercury Pod** | LLTV System | N/A | Night Operations | Allows night use of Shkval/Vikhr |

## Realism Notes
- **Max Landing Weight:** In DCS, landing significantly above 13,300 kg often results in tire blowouts or gear collapse, which is modeled more strictly than in some other modules.
- **Crosswind:** DCS Su-25T ground handling logic can be unstable (tipping) in crosswinds >12 m/s, which may differ slightly from real-world tolerances.
- **Cockpit:** The DCS Su-25T does not have a clickable cockpit; all procedures assume keybinds or HOTAS mappings.

---

## Startup Checklist

### Pre-Start
- [ ] **Parking Brake** — SET (`W` key)
- [ ] **Throttle** — IDLE (`PgDn` to minimum)
- [ ] **Master Power** — ON (`RShift + L`)
- [ ] **Battery** — ON
- [ ] **EKRAN** — check (no red warnings)

### Engine Start
- [ ] **Left Engine Start** — `RAlt + Home` (or use right-click start lever in cockpit)
  - Wait for N2 > 50%
  - EGT rising — normal
- [ ] **Right Engine Start** — `RCtrl + Home`
  - Wait for N2 > 50%
  - Both engines at IDLE — confirm RPM ~65%
- [ ] **Generators** — ON (both)
- [ ] **Hydraulics** — check pressure (green)
- [ ] **Fuel** — check quantity and transfer pumps ON
- [ ] **Oxygen** — ON and check flow
- [ ] **SPO-15 RWR** — ON
- [ ] **EKRAN** — all green / no warnings

### Avionics Power-On
- [ ] **PNK Navigation Computer** — ON
- [ ] **ILS** — set frequency if applicable
- [ ] **R-862 Radio** — ON, set frequency
- [ ] **Shkval TV System** — ON (takes ~1 min warm-up)
- [ ] **Laser Rangefinder** — SAFE (arm only when weapons employment)
- [ ] **ATGM Guidance** — check selected weapon type

---

## Taxi & Takeoff

### Taxi
- [ ] **Parking Brake** — RELEASE (`W`)
- [ ] **Nose Wheel Steering** — ON (engaged with brake key)
- [ ] **Throttle** — advance slowly to taxi speed
- [ ] Taxi to runway, keep speed < 20 kph in turns

### Takeoff
- [ ] **Flaps** — TAKEOFF position (`F` key)
- [ ] **Trim** — check neutral
- [ ] **ILS/NAV** — confirm active waypoint
- [ ] **Throttle** — FULL (`PgUp`)
- [ ] Rotate at ~220 kph
- [ ] **Gear** — UP at positive rate of climb (`G` key)
- [ ] **Flaps** — RETRACT above 300 kph (`F` key)
- [ ] Climb to assigned altitude

---

## Navigation

### Waypoint Navigation (PNK System)
- [ ] **PNK Power** — ON
- [ ] **Waypoints** — pre-planned in mission editor or set via cockpit
- [ ] **Waypoint select** — `1` / `2` to cycle waypoints
- [ ] **Autopilot Route Mode** — `LAlt + 1` (route following)
- [ ] **Autopilot Altitude Hold** — `LAlt + 2`

### Navigation Modes
| Mode | Key | Description |
|---|---|---|
| Route Mode | `LAlt + 1` | Follow pre-planned waypoints |
| Altitude Hold | `LAlt + 2` | Maintain current altitude |
| Heading Hold | `LAlt + 3` | Maintain current heading |
| Return to Base | `LAlt + 0` | Navigate to home base waypoint |

### ILS Approach
- [ ] **ILS Frequency** — set on radio/nav panel
- [ ] **ILS Mode** — select on PNK
- [ ] Intercept localizer at ~10 NM from field
- [ ] Descend on glide slope (3°)
- [ ] Break off if not stabilized by 500 ft AGL

---

## Avionics & Systems

### Shkval TV/Laser Targeting System
- [ ] **Shkval Power** — ON (warm-up ~60 sec)
- [ ] **Shkval FOV** — WIDE (default) or NARROW (`*` numpad)
- [ ] **Shkval Slew** — numpad 8/2/4/6 (up/down/left/right)
- [ ] **Target Lock** — `Enter` (numpad)
- [ ] **Laser Arm** — `O` key
- [ ] **Laser Fire** — `O` key (hold for ranging/designation)

### SPO-15 Beryoza RWR
- [ ] **Power** — ON
- [ ] Indicators: **F** = fighter radar, **C** = SAM/AAA radar
- [ ] **Volume** — adjust as needed
- [ ] Alert tones indicate threat type and direction

### EKRAN System Warnings
| Warning | Meaning | Action |
|---|---|---|
| ENGINE | Engine fault | Check RPM/EGT, reduce power |
| HYD | Hydraulics failure | Emergency gear extension |
| FIRE | Engine fire | Shutdown affected engine, pull fire handle |
| OIL | Low oil pressure | Land immediately |

---

## Weapons Employment

### Air-to-Ground Rockets & Guns

#### S-8 / S-24 Rockets
- [ ] **Master Arm** — ARM (`O` key to arm systems)
- [ ] **Weapon Mode** — select ROCKETS on weapon panel
- [ ] **Salvo size** — set as desired
- [ ] Dive attack: 30°–45° dive, release at 1,200–1,800 m range
- [ ] Pull off with at least 500 m buffer
- [ ] **Key:** `Space` or joystick trigger to fire

#### GSh-30-2 30mm Gun
- [ ] **Master Arm** — ARM
- [ ] **Gun mode** — select
- [ ] Strafe run: 15°–20° dive
- [ ] Open fire at 1,200 m, cease at 600 m
- [ ] **Key:** `Space` or joystick trigger

---

### Unguided Bombs

#### OFAB-250 / FAB-500 Free-Fall Bombs
- [ ] **Master Arm** — ARM
- [ ] **Bomb mode** — select on weapon panel
- [ ] **CCIP** (Continuously Computed Impact Point) — crosshair on MFD
- [ ] Dive angle: 20°–45°
- [ ] Align CCIP crosshair on target
- [ ] Release: `Space` or joystick trigger
- [ ] Minimum release altitude: 500 m AGL (high drag) / 1,500 m AGL (low drag)

---

### Guided Weapons

#### Kh-25ML (Laser-Guided)
- [ ] **Master Arm** — ARM
- [ ] **Weapon select** — Kh-25ML on pylons 3/7 or 4/6
- [ ] **Shkval** — slew to target, lock (`Enter`)
- [ ] **Laser** — ARM (`O`), will fire automatically when in envelope
- [ ] Attack profile: level or shallow dive, 3–5 km range
- [ ] **Launch envelope:** 3–10 km, altitude 500–5000 m
- [ ] Fire: `Space` (missile flies to laser spot)
- [ ] **Hold laser on target until impact**

#### Kh-29L (Laser-Guided, Heavy)
- [ ] Same procedure as Kh-25ML
- [ ] **Launch envelope:** 2–8 km
- [ ] Heavier warhead — use against hardened targets

#### Kh-29T (TV-Guided)
- [ ] **Master Arm** — ARM
- [ ] **Shkval** — slave to missile seeker via MFD
- [ ] **Missile FOV** — slew to target
- [ ] **Lock:** `Enter` (missile seeker locks)
- [ ] **Fire:** `Space`
- [ ] **Fire-and-forget** — no need to track after launch

#### KAB-500Kr (TV-Guided Bomb)
- [ ] **Master Arm** — ARM
- [ ] **Shkval** — center on target
- [ ] **KAB mode** — selected
- [ ] **Lock:** seeker slaves to Shkval aim point
- [ ] **Confirm lock** on MFD
- [ ] **Release:** `Space`
- [ ] **Minimum altitude:** 1,000 m AGL; optimal 2,000–5,000 m

---

### TV/Laser Guided Bombs

#### KAB-500L (Laser-Guided Bomb)
- [ ] **Master Arm** — ARM
- [ ] **Shkval** — slew to target and lock
- [ ] **Laser** — ARM
- [ ] **Release:** `Space`
- [ ] Maintain laser on target through impact
- [ ] **Minimum altitude:** 1,000 m AGL

---

### Anti-Radiation Kh-58

#### Kh-58 (ARM — Anti-Radiation Missile)
- [ ] **Master Arm** — ARM
- [ ] **SPO-15** — identify threat emitter (SAM/AAA radar)
- [ ] **Kh-58 seeker** — tune to emitter frequency
- [ ] **Launch zone:** 10–160 km depending on altitude
- [ ] **Fire:** `Space`
- [ ] **Fire-and-forget** — seeker homes on radar emissions

---

### SEAD Procedures

#### Standard SEAD Attack Sequence
1. [ ] Identify SAM radar via SPO-15 or briefing
2. [ ] Plan ingress to avoid known threat envelopes
3. [ ] Arm Kh-58 and select on weapon panel
4. [ ] Approach at medium-high altitude (3,000–5,000 m)
5. [ ] Acquire target on Shkval if needed
6. [ ] Enter launch envelope; fire Kh-58
7. [ ] Immediately turn cold (away from threat) after launch
8. [ ] Confirm radar shutdown via SPO-15

---

## Defensive Systems

### SPO-15 Beryoza (RWR)
- Continuous audio/visual warning of radar threats
- **SPO-15 modes:** Active (full) / Passive (quiet)

### Chaff & Flares
- [ ] **Chaff/Flare program** — select
- [ ] **Chaff** — `[` key (left bracket) — counters radar-guided missiles
- [ ] **Flares** — `]` key (right bracket) — counters IR-guided missiles
- [ ] **Auto mode** — engage for automatic dispensing upon threat
- [ ] **Jink maneuver** — break turn + flares on missile warning

### Typical Defensive Sequence (Missile Launch Warning)
1. **Break** hard into the threat bearing (from SPO-15)
2. **Deploy Flares** — `]` (2–3 bursts)
3. **Chaff** — `[` if radar-guided threat
4. **Nose low** — gain airspeed
5. **Terrain mask** — use terrain if available

---

## Landing Checklist

- [ ] **ATIS / Weather** — get field info
- [ ] **Fuel** — check remaining (> 500 kg for safe landing)
- [ ] **Gear** — DOWN (`G`) — confirm 3 green lights
- [ ] **Flaps** — LANDING (`F`)
- [ ] **Speed** — 270–290 kph on approach
- [ ] **ILS** — intercept if available
- [ ] Touchdown speed: ~230 kph
- [ ] **Brakes** — `W` (wheel brakes)
- [ ] **Drag chute** — `C` key (if installed)
- [ ] **Spoilers** — auto on touchdown

---

## Shutdown Checklist

- [ ] **Taxi** to parking spot, align nose
- [ ] **Parking Brake** — SET (`W`)
- [ ] **Throttle** — IDLE, then CUT-OFF
- [ ] Wait for engines to spool down (RPM < 20%)
- [ ] **Avionics** — all OFF
- [ ] **Battery** — OFF
- [ ] **Master Power** — OFF

---

## Emergency Procedures

### Engine Fire
1. **Throttle** affected engine — IDLE
2. **Fire handle** — PULL (right-click in cockpit)
3. If fire persists — shutdown engine
4. Single-engine approach — reduce speed carefully

### Hydraulic Failure
1. **Landing Gear** — emergency extend (`LCtrl + G`)
2. **Flaps** — may not function — prepare for flapless landing
3. **Speed** — add 20–30 kph to approach speed

### Ejection
- **Eject:** `LCtrl + E` (hold 1 second)
- Minimum safe altitude: ~100 m AGL for seat to function

---


---

## Keyboard & Joystick Reference

### Flight Controls
| Function | Keyboard | Joystick Axis |
|---|---|---|
| Pitch | `NumPad 8/2` | Joystick Y-axis |
| Roll | `NumPad 4/6` | Joystick X-axis |
| Yaw / Rudder | `Z / X` | Twist/Pedals |
| Throttle Inc/Dec | `PgUp / PgDn` | Throttle axis |
| Trim Pitch | `NumPad + / -` | Hat switch |

### Gear & Flaps
| Function | Key |
|---|---|
| Landing Gear | `G` |
| Flaps | `F` / `LShift+F` |
| Wheel Brakes | `W` |
| Drag Chute | `C` |

### Weapons
| Function | Key |
|---|---|
| Master Arm | `O` |
| Weapon Release / Fire | `Space` or trigger |
| Chaff | `[` |
| Flares | `]` |
| Jettison Stores | `LAlt + J` |
| Shkval: Slew Up/Down | `Numpad 8/2` |
| Shkval: Slew Left/Right | `Numpad 4/6` |
| Shkval: Lock | `Numpad Enter` |
| Shkval: Wide/Narrow | `Numpad *` |
| Laser Arm/Fire | `O` |

### Autopilot
| Function | Key |
|---|---|
| Route Mode | `LAlt + 1` |
| Altitude Hold | `LAlt + 2` |
| Heading Hold | `LAlt + 3` |
| Autopilot Disengage | `LAlt + Z` |

---

## Cross-References
- [9-Line CAS Procedures →](../procedures/9-line-cas.md)
- [Radio Communications →](../procedures/radio-communications.md)
- [Airfield & ATC →](../procedures/airfield-atc-communications.md)
- [Su-25 (Standard) →](su-25.md)
- [NS430 Navigation Module →](ns430.md)

---

*Based on Eagle Dynamics DCS Su-25T documentation. For simulation use only.*
