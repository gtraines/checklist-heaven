# UH-1H Huey — DCS Checklist

> **Aircraft:** Bell UH-1H Iroquois "Huey" | **Role:** Utility / Light Attack Helicopter
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [Cockpit Orientation](#cockpit-orientation)
2. [Operating Limitations](#1-operating-limitations)
3. [Performance & V-Speeds](#2-performance--v-speeds)
4. [Emergency Procedures (Quick Ref)](#3-emergency-procedures-quick-ref)
5. [Weapons & Stores (Quick Ref)](#4-weapons--stores-quick-ref)
6. [Startup Checklist](#startup-checklist)
7. [Hover & Takeoff](#hover--takeoff)
8. [Navigation](#navigation)
9. [Weapons Employment](#weapons-employment)
   - [M134 Minigun](#m134-minigun)
   - [M60 Door Guns](#m60-door-guns)
   - [2.75-inch Rockets (M157/M159)](#275-inch-rockets)
10. [Defensive Procedures](#defensive-procedures)
11. [Landing Checklist](#landing-checklist)
12. [Shutdown Checklist](#shutdown-checklist)
13. [Emergency Procedures (Detailed)](#emergency-procedures)
14. [Keyboard & Joystick Reference](#keyboard--joystick-reference)

---

## Cockpit Orientation

```
┌──────────────────────────────────────────┐
│  AI Attitude Indicator    VSI            │
│  Altimeter    Airspeed    Heading (DI)   │
│  Engine Gauges: N1, TOT, Torque          │
│  Throttle (collective twist)             │
│  Collective (left)  Cyclic (right)       │
└──────────────────────────────────────────┘
```

| Control | Description |
|---|---|
| Collective | Left hand — controls altitude/thrust |
| Cyclic | Right hand (stick) — controls direction/bank |
| Anti-Torque Pedals | Feet — controls yaw heading |
| Throttle | Twist on collective — controls engine power |

| Panel | Location | Function |
|---|---|---|
| Engine gauges | Center panel | N1%, Torque, TOT (Turbine Outlet Temp) |
| Attitude indicator | Top center | Artificial horizon |
| Radio panel | Center console | FM/UHF radios |
| Armament panel | Center | Weapon system controls |
| Governor switch | Collective | RPM governor on/off |

---

## 1. Operating Limitations

| Parameter | Limit | Notes |
|---|---|---|
| **Max Takeoff Weight (MTOW)** | **9,500 lbs** | Standard max gross weight |
| **Max Landing Weight** | **9,500 lbs** | Same as MTOW |
| **VNE (Never Exceed)** | **124 KIAS** | At Sea Level; decreases with altitude and weight |
| **G-Limits** | **+2.5 G / +3.0 G** | Low G (Pushovers) is **PROHIBITED** due to Mast Bumping risk* |
| **Crosswind Limit** | **30-35 knots** | LTE risk increases with wind from 4 to 8 o'clock* |

## 2. Performance & V-Speeds

| Regime | Speed (KIAS) | Configuration / Notes |
|---|---|---|
| **Takeoff / Best Climb ($V_Y$)** | **60** | Standard climb speed |
| **Cruise** | **80 - 90** | Typical cruise speed range |
| **Landing Approach** | **60** | Normal approach, decelerate to hover |
| **Autorotation** | **60** | Adjust cyclic to maintain 60 KIAS |
| **Max Speed ($V_{NE}$)** | **124** | Do not exceed |

## 3. Emergency Procedures (Quick Ref)

| Emergency | Immediate Action Steps |
|---|---|
| **Engine Failure** (Hover/Low Altitude) | 1. **COLLECTIVE** — ADJUST to maintain Rotor RPM<br>2. **PEDALS** — CONTROL YAW<br>3. **CUSHION LANDING** — With Collective |
| **Engine Failure** (Cruise/In-Flight) | 1. **AUTOROTATE** — ENTER<br>2. **CYCLIC** — ADJUST for 60 KIAS<br>3. **EMERGENCY FUEL SHUTOFF** — OFF (if fire suspected) |
| **Engine Fire** (In Flight) | 1. **POWER** — OFF (Enter Autorotation)<br>2. **EMERGENCY FUEL SHUTOFF** — OFF<br>3. **CABIN HEAT** — OFF<br>4. **LAND IMMEDIATELY** |
| **Hydraulic Failure** | 1. **AIRSPEED** — ADJUST to 60-80 KIAS (manageable forces)<br>2. **HYD CONT SWITCH** — OFF (if surging)<br>3. **LAND AS SOON AS PRACTICABLE** (Run-on landing) |
| **Electrical Failure** (Main Gen) | 1. **GEN SWITCH** — RESET, then ON<br>2. **NON-ESSENTIAL EQUIP** — OFF (if power not restored)<br>3. **LAND AS SOON AS PRACTICABLE** |
| **Loss of Tail Rotor Effectiveness (LTE)** | 1. **COLLECTIVE** — LOWER (Reduce Torque)<br>2. **CYCLIC** — FORWARD (Gain Airspeed)<br>3. **PEDALS** — AS REQUIRED |

## 4. Weapons & Stores (Quick Ref)

| Weapon / System | Type | Effective Range | Best Suited For | Simulation Notes |
|---|---|---|---|---|
| **M60D** | 7.62mm Door Gun | ~800m | Infantry, Soft Vehicles, Self-Defense | Operated by AI or player; limited side/rear arc |
| **M134 Minigun** | 7.62mm Rotary MG | 1000 - 1500m | Heavy suppression, Light structures | High rate of fire (2400/4000 rpm); consumes ammo rapidly |
| **Hydra 70 (M151)** | HE Rocket (10lb) | 1.5 - 3km | General purpose, Light vehicles | Standard HE rocket; requires manual compensation |
| **Hydra 70 (M229)** | HE Rocket (17lb) | 1.5 - 3km | Structures, Dug-in infantry | Heavier warhead; slightly different trajectory than M151 |
| **Hydra 70 (M156)** | White Phosphorus | 1.5 - 3km | Target marking, Incendiary | Creates significant smoke; good for marking for CAS |
| **Hydra 70 (M257/M278)** | Illumination Flare | Varies | Night Ops, Battlefield Illum. | M257 (Visible), M278 (IR); aim high to deploy over target |
| **Hydra 70 (M259)** | Smoke Screen | 1.5 - 3km | Obscuring friendly movement | Screening smoke |

---

## Startup Checklist

### Pre-Start
- [ ] **Parking Brake** — SET (if on ground)
- [ ] **All switches** — OFF/NORMAL
- [ ] **Collective** — FULL DOWN (lowest position)
- [ ] **Throttle** — IDLE detent (twist grip)
- [ ] **Battery Switch** — ON

### Engine Start (Lycoming T53-L-13B turboshaft)
- [ ] **Throttle** — IDLE position
- [ ] **Fuel** — ON, check quantity
- [ ] **Starter** — ENGAGE (`RAlt + Home` or right-click starter panel)
  - N1 RPM rising
  - TOT rising — monitor (max 870°C during start)
  - N1 reaches 58–60% — release starter
- [ ] **Throttle** — advance to FLIGHT detent (not over-torque)
- [ ] **Rotor RPM** — rising toward 100%
  - Target: **324 RPM** (100%)
- [ ] **Governor** — ON
- [ ] **TOT** — stabilize < 615°C at flight idle
- [ ] **Engine warm-up** — 2 minutes at IDLE
- [ ] **Hydraulics** — check (green light)
- [ ] **Avionics** — all ON

### Radio Setup
- [ ] **FM Radio (ARC-131)** — ON, set frequency
- [ ] **UHF Radio (ARC-134)** — ON, set frequency
- [ ] Check comms with ATC/flight lead

---

## Hover & Takeoff

### Before Takeoff
- [ ] **Systems check** — all green
- [ ] **Rotor RPM** — 100% (324 RPM)
- [ ] **Altimeter** — set current QNH
- [ ] **Fuel** — check remaining, minimum 30 min reserve

### Hover Takeoff
1. [ ] Slowly raise collective to light on skids
2. [ ] Pedal as needed to maintain heading (left pedal on power increase)
3. [ ] Bring to hover at 3–5 ft AGL
4. [ ] **Stabilize** — adjust pedal, cyclic, collective
5. [ ] Confirm systems nominal before departing

### Transition to Forward Flight
1. [ ] From hover, push cyclic forward slightly
2. [ ] Collective as needed to maintain altitude
3. [ ] Nose-low attitude builds airspeed
4. [ ] At **40 kts** — ETL (Effective Translational Lift) gained — flight more efficient
5. [ ] Climb at 70–80 kts for best rate of climb

### Normal Takeoff
- [ ] Accelerate through ETL (~40 kts)
- [ ] Climb: 70–80 kts
- [ ] Best endurance speed: **70 kts**
- [ ] Best range speed: **90 kts**
- [ ] Max cruise: **120 kts**

---

## Navigation

### VFR Navigation
- The UH-1H has no TACAN or GPS
- Primary navigation is by **visual reference** (map reading)
- Use F10 map (`F10`) for reference

### Radio Navigation
- [ ] **ADF** — if available in mission, tune to beacon
- [ ] **TACAN** — not available on base UH-1H

### Navigation Tips
- Fly low and slow — use terrain features
- Note roads, rivers, power lines as reference
- Maintain at least 300 ft AGL for safety
- Skid roads if needed in urban areas

---

## Weapons Employment

### Weapons Available
| Weapon | Mount | Type |
|---|---|---|
| M134 Minigun (×2) | Wing stub | 7.62mm, 4,000 rpm |
| 2.75-inch FFAR rockets | Wing pods | Area suppression |
| M60 Door Gun (×2) | Crew positions | 7.62mm manual |

### Master Arm
- [ ] **Armament Master Switch** — ON (`O` key)
- [ ] **Weapon select** — desired station

---

### M134 Minigun

#### Employment
- Range: up to 1,000 m effective
- Rate of fire: 4,000 rpm (high setting)
- Very effective against personnel, light vehicles, aircraft

#### Attack Run
1. [ ] **Master Arm** — ON
2. [ ] Select miniguns on armament panel
3. [ ] Dive or orbit approach
4. [ ] Aim with HUD pipper
5. [ ] Fire: `Space` or trigger
6. [ ] Short bursts: 2–3 seconds (overheating risk)

---

### M60 Door Guns

- Operated by crew (right-seat crew chief / door gunners)
- In multiplayer: crewmembers control door guns
- In single-player: AI controls door guns automatically

---

### 2.75-inch Rockets

#### M157 (7-round) / M159 (19-round) Pods

1. [ ] **Master Arm** — ON
2. [ ] Select rocket pods on armament panel
3. [ ] Set salvo quantity (1, 2, 4, or all)
4. [ ] Dive: 10°–20° toward target
5. [ ] Aim pipper on target
6. [ ] Fire at 600–1,200 m range: `Space`
7. [ ] Pull off at 400 m minimum

> **Note:** Rockets are most effective in diving runs. Hover rocket employment possible but exposes aircraft to ground fire.

## Realism Notes
* **Mast Bumping**: The DCS UH-1H module accurately models "Mast Bumping". Avoid low-G pushover maneuvers (cyclic forward) to prevent catastrophic rotor separation.
* **LTE (Loss of Tail Rotor Effectiveness)**: High power settings combined with slow speeds and tailwinds (especially from the 4-8 o'clock position) can cause unrecoverable spins.
* **Weapon Aiming**: There is no CCIP/CCRP. Rocket and fixed-minigun accuracy depends entirely on pilot skill with the reflex sight and manual estimation of windage/drop.
* **Weight**: Fully loaded gunships (XM200 pods + Miniguns) have significantly reduced hover performance, especially in hot/high conditions.

---

## Defensive Procedures

### The UH-1H Has NO COUNTERMEASURES
- No RWR, no chaff, no flares
- Survivability = **tactics and situational awareness**

### Threat Avoidance
- [ ] Fly **NOE** (Nap-of-the-Earth) — tree-top level in threat areas
- [ ] Use **terrain masking** — hills, ridges, trees between you and threat
- [ ] **Never hover in the open** near threat SAMs or AAA
- [ ] Avoid known AAA/SAM positions by minimum 3–5 km

### SAM/AAA Evasion
1. Immediate: **descend to trees/terrain**
2. Turn perpendicular to threat radar bearing
3. Use terrain features to mask
4. Abort mission if threat too close

### Small Arms Fire
- Assume all ground fire is a threat
- **Jink** left-right while transiting
- Keep low and fast over open ground
- Do not orbit predictably over threat areas

---

## Landing Checklist

### Normal Approach
1. [ ] Reduce airspeed to 60 kts on final
2. [ ] Begin deceleration to slow flight
3. [ ] **Approach angle:** 10°–15° standard
4. [ ] At 40 kts — ETL loss, need more collective
5. [ ] **Arrive at hover** — 3–5 ft AGL
6. [ ] **Set down** — lower collective smoothly
7. [ ] **Settle onto skids**

### Running Landing (if preferred)
1. [ ] Maintain 30–40 kts to touchdown
2. [ ] Skids touch at low forward speed
3. [ ] Lower collective — settle

### Autorotation Landing
*(See Emergency Procedures below)*

---

## Shutdown Checklist

- [ ] **Hover/taxi** to parking
- [ ] **Set down** — collective full down
- [ ] **Rotor brake** — apply if equipped
- [ ] **Throttle** — IDLE position
- [ ] Allow engine to cool: 1–2 minutes at IDLE
- [ ] **Throttle** — CUT-OFF
- [ ] **Rotor** — spinning down, clear rotor arc
- [ ] **All switches** — OFF
- [ ] **Battery** — OFF

---

## Emergency Procedures

### Engine Failure / Autorotation

**Immediate Action:**
1. [ ] **COLLECTIVE** — lower immediately (within 2 seconds)
   - Maintain rotor RPM 280–324
2. [ ] **PEDALS** — adjust to maintain heading
3. [ ] **MAYDAY** — transmit if time permits
4. [ ] **Airspeed** — 65–70 kts (best glide / best autorotation)
5. [ ] Select landing area

**Autorotation Flare:**
1. At 100 ft AGL — begin flare (pull cyclic back)
2. Slow to near-zero groundspeed
3. At 10–15 ft AGL — reduce flare
4. **Level flare** — trade inertia for reduced descent rate
5. **Collective pull** — cushion touchdown
6. Set down — collective full down

### Low Rotor RPM
1. Collective — decrease
2. Throttle — increase if engine running
3. Recover RPM above 280 before full collective application

### Tail Rotor Failure
1. **Small tail rotor loss** — reduce power, autorotate
2. **Yaw** — use collective/pedal to control
3. Running landing preferred

---

## Keyboard & Joystick Reference

### Collective & Throttle
| Function | Key | Axis |
|---|---|---|
| Collective Up | `PgUp` | Collective axis |
| Collective Down | `PgDn` | Collective axis |
| Throttle (twist) | via cockpit | Throttle axis |
| Rotor Brake | cockpit lever | — |

### Cyclic (Stick)
| Function | Key | Axis |
|---|---|---|
| Pitch Forward/Back | `Numpad 8/2` | Stick Y |
| Roll Left/Right | `Numpad 4/6` | Stick X |
| Trim Release | cockpit | Trim button |

### Pedals (Anti-Torque)
| Function | Key | Axis |
|---|---|---|
| Left Pedal | `Z` | Rudder axis |
| Right Pedal | `X` | Rudder axis |

### Weapons
| Function | Key |
|---|---|
| Master Arm | `O` |
| Fire / Rockets | `Space` or trigger |
| Jettison | `LAlt + J` |

### Navigation & Comms
| Function | Key |
|---|---|
| Radio Menu | `\` |
| F10 Map | `F10` |
| Pause | `P` |

---

## Cross-References
- [Mi-24 Hind Checklist →](mi-24-hind.md)
- [OH-58D Kiowa Checklist →](oh-58d-kiowa.md)
- [9-Line CAS Procedures →](../procedures/9-line-cas.md)
- [Radio Communications →](../procedures/radio-communications.md)
- [Airfield & ATC →](../procedures/airfield-atc-communications.md)

---

*Based on Eagle Dynamics DCS UH-1H documentation. For simulation use only.*

<!-- Co-authored-by: Copilot <223556219+Copilot@users.noreply.github.com> -->
