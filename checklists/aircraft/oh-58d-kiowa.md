# OH-58D Kiowa Warrior — DCS Checklist

> **Aircraft:** Bell OH-58D Kiowa Warrior | **Role:** Scout / Light Attack Helicopter
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [Cockpit Orientation](#cockpit-orientation)
2. [MMS (Mast-Mounted Sight)](#mms-mast-mounted-sight)
3. [Operating Limitations](#1-operating-limitations)
4. [Performance & V-Speeds](#2-performance--v-speeds)
5. [Emergency Procedures](#3-emergency-procedures-immediate-action)
6. [Weapons & Stores](#4-weapons--stores)
7. [Startup Checklist](#startup-checklist)
8. [Hover & Takeoff](#hover--takeoff)
9. [Navigation (AHRS/GPS)](#navigation-ahrsgps)
10. [Avionics & Systems](#avionics--systems)
11. [Weapons Employment](#weapons-employment)
   - [M296 .50 cal Machine Gun](#m296-50-cal-machine-gun)
   - [2.75-inch Rockets (Hydra 70)](#275-inch-rockets-hydra-70)
   - [AGM-114 Hellfire](#agm-114-hellfire)
   - [AIM-92 Stinger (Air Defense)](#aim-92-stinger)
12. [Scout Procedures (RSTA)](#scout-procedures)
13. [Laser Designation Procedures](#laser-designation)
14. [Defensive Procedures](#defensive-procedures)
15. [Landing Checklist](#landing-checklist)
16. [Shutdown Checklist](#shutdown-checklist)
17. [Keyboard & Joystick Reference](#keyboard--joystick-reference)

---

## Cockpit Orientation

The OH-58D Kiowa Warrior is a scout helicopter with a ball-mounted sight above the rotor mast.

```
┌──────────────────────────────────────────────┐
│  MFD (Multi-Function Display) — Center       │
│  MMS control  Weapon selector                │
│  ANVIS NVG mount  Radar altimeter            │
│  GPS/AHRS display                            │
│  Collective   Cyclic                         │
└──────────────────────────────────────────────┘
```

| Panel | Location | Function |
|---|---|---|
| MFD | Center | Multi-function display (navigation, weapons) |
| MMS Controller | Left | Mast-Mounted Sight control |
| Weapon Panel | Right | Weapon arm and select |
| GPS/Nav | Center | Navigation computer |
| ANVIS | Helmet | Night Vision Goggle mount |

---

## MMS (Mast-Mounted Sight)

The MMS is the OH-58D's unique capability — a sensor ball mounted above the rotor head, allowing observation while hull-defilade (hiding body behind terrain).

### MMS Components
| Component | Function |
|---|---|
| TV Camera | Daytime observation |
| FLIR | Thermal/night observation |
| Laser Rangefinder | Range to target |
| Laser Designator | Designates targets for laser-guided weapons |

### MMS Operation
1. [ ] **MMS power** — ON (from avionics panel)
2. [ ] Warm-up: 3–5 minutes (FLIR)
3. [ ] Select **TV** (day) or **FLIR** (night)
4. [ ] **Slew MMS** using hat switch or keyboard
5. [ ] **Laser Range** — activate to get range to target
6. [ ] **Laser Designate** — activates for Hellfire or LGB guidance

### MMS Key Controls
| Function | Key / Control |
|---|---|
| MMS slew up | `Numpad 8` |
| MMS slew down | `Numpad 2` |
| MMS slew left | `Numpad 4` |
| MMS slew right | `Numpad 6` |
| MMS zoom in | `Numpad +` |
| MMS zoom out | `Numpad -` |
| Laser range/designate | `O` key |
| Video switch (TV/FLIR) | MFD OSB |

## 1. Operating Limitations

| Parameter | Limit | Notes |
|---|---|---|
| **Max Takeoff Weight (MTOW)** | **5,500 lbs (2,495 kg)** | Standard max gross for KW; earlier models 5,200 lbs |
| **Max Landing Weight** | **5,500 lbs** | Same as MTOW |
| **G-Limits** | **+2.5 G to -0.5 G** | At Max Gross Weight; avoid negative G (mast bumping) |
| **Rotor RPM Limits ($N_R$)** | **Power On: 98% - 100%**<br>**Power Off: 90% - 107%** | Transient limits exist |
| **Torque Limits (Q)** | **Continuous: 100%**<br>**Transient (10 sec): 110%** | Exceeding 100% requires inspection |
| **TOT Limits** | **Continuous: 737°C**<br>**Start (10 sec): 843°C** | Strict start limits |
| **Slope Landing Limits** | **10° (Side/Nose Up)**<br>**5° (Nose Down)** | Terrain interaction varies in sim |
| **Crosswind Component** | **35 knots** | Sideward/Rearward; High LTE risk |

## 2. Performance & V-Speeds

| Regime | Speed (KIAS) | Configuration / Notes |
|---|---|---|
| **Hover Taxi** | **< 20** | Standard ground taxi |
| **Takeoff Profile** | **45 - 60** | Climb out speed |
| **Max Rate of Climb ($V_Y$)** | **55 - 60** | Variable with weight |
| **Max Range Speed** | **90 - 100** | Depends on drag (MMS/Stores) |
| **Max Speed ($V_{NE}$)** | **110 - 120** | 110 KIAS with doors off |
| **Autorotation** | **60 (Min Rate)**<br>**80 (Max Glide)** | Range 60-80 KIAS |
| **Sideward/Rearward** | **35** | Max control limit |
| **Landing Approach** | **60** | Initial approach speed |

---

## 3. Emergency Procedures (Immediate Action)

| Emergency | Immediate Action Steps |
|---|---|
| **Engine Failure - In Flight** | 1. **COLLECTIVE** — ADJUST (Maintain $N_R$)<br>2. **PEDALS** — ADJUST (Trim)<br>3. **CYCLIC** — ADJUST (60-80 KIAS)<br>4. **LANDING** — ACCOMPLISH |
| **Engine Fire - In Flight** | 1. **LAND IMMEDIATELY**<br>2. **EMERGENCY SHUTDOWN** — ACCOMPLISH (Once on ground) |
| **Engine Fire - On Ground** | 1. **EMERGENCY SHUTDOWN** — ACCOMPLISH |
| **Emergency Shutdown** | 1. **THROTTLE** — OFF<br>2. **FUEL BOOST** — OFF<br>3. **BATTERY** — OFF<br>4. **ROTOR BRAKE** — APPLY |
| **FADEC Failure / Overspeed** | 1. **COLLECTIVE** — ADJUST ($N_R$)<br>2. **THROTTLE** — ADJUST (Match $N_G$/TGT)<br>3. **FADEC MODE SWITCH** — CHECK<br>4. **LAND AS SOON AS PRACTICABLE** |
| **Hydraulic Failure** | 1. **AIRSPEED** — ADJUST (60-80 KIAS)<br>2. **HYDRAULIC SWITCH** — OFF (If hardover)<br>3. **LAND AS SOON AS POSSIBLE** (Run-on landing) |
| **Tail Rotor Failure / Spin** | 1. **AUTOROTATION** — ENTER<br>2. **THROTTLE** — IDLE<br>3. **LANDING** — ACCOMPLISH |
| **LTE (Uncommanded Yaw)** | 1. **COLLECTIVE** — REDUCE<br>2. **CYCLIC** — FORWARD (Gain airspeed)<br>3. **PEDALS** — FULL LEFT<br>4. **AIRSPEED** — INCREASE |
| **Electrical Failure (DC Gen)** | 1. **GEN RESET** — PRESS<br>2. **GEN SWITCH** — ON<br>3. **If Fails:** NON-ESSENTIAL BUS — OFF<br>4. **LAND AS SOON AS PRACTICABLE** |
| **Engine Restart - In Flight** | 1. **AIRSPEED** — 60 KIAS<br>2. **COLLECTIVE** — ADJUST ($N_R$)<br>3. **THROTTLE** — IDLE (If $N_1$ < 50%) / FLY (If $N_1$ > 50%)<br>4. **START SWITCH** — PRESS (If $N_1$ < 50%) |

## 4. Weapons & Stores

| Weapon / System | Type | Effective Range | Best Suited For | Simulation Notes |
|---|---|---|---|---|
| **AGM-114K Hellfire II** | SAL Missile (Anti-Tank) | 500m - 8km | Heavy armor (MBTs) | Requires constant laser (MMS or Buddy) |
| **AGM-114M Hellfire II** | SAL Missile (Blast-Frag) | ~8km | Soft targets, boats, structures | Blast-frag warhead; delay fuse possible |
| **AGM-114N Hellfire II** | SAL Missile (Thermobaric) | ~8km | Bunkers, caves, enclosed spaces | MAC warhead for pressure/heat effect |
| **Hydra 70 (M151/M229)** | Unguided Rocket (HE) | 1.5km - 4km | Area suppression, soft targets | Aim using CCIP "I-beam" in HUD |
| **APKWS (AGR-20A)** | Laser-Guided Rocket | 1.5km - 5km+ | Precision strikes, light armor | Needs laser designation; fly into basket |
| **M3P .50 Cal** | Heavy Machine Gun | 1km - 1.5km | Infantry, technicals, defense | Fixed mount; aim with aircraft nose |

## Realism Notes
*   **MMS Dynamics:** The Mast Mounted Sight adds significant top weight and drag. Be aware of handling differences and $V_{NE}$ limits compared to clean helicopters.
*   **Hellfire Types:** The OH-58D does not typically carry the radar-guided AGM-114L (Longbow) in this configuration; stick to SAL variants (K/M/N) for realism.
*   **Power Management:** The Kiowa is power-limited. A full load of 4 Hellfires heavily impacts climb rate and maneuverability. A mixed "Scout" loadout (2x Hellfire + .50 Cal or Rockets) is often preferred.
*   **FADEC:** The FADEC system is critical and modeled in detail. Startup sequence is sensitive to throttle position (must be at Idle detent).
*   **LTE:** The aircraft is susceptible to Loss of Tail Rotor Effectiveness in high power/low speed conditions, especially with tailwinds.

---

## Startup Checklist

### Pre-Start
- [ ] **Parking Brake** — SET (`W`)
- [ ] **All switches** — OFF
- [ ] **Collective** — full DOWN
- [ ] **Throttle** — IDLE detent

### Engine Start (Allison 250-C30R turboshaft)
- [ ] **Battery** — ON
- [ ] **Fuel** — ON, check quantity
- [ ] **Starter** — ENGAGE (`RAlt + Home`)
  - N1 rising
  - TOT rising — monitor (max 810°C start limit)
  - N1 reaches 65% — engine running
- [ ] **Throttle** — advance to FLIGHT
- [ ] **Rotor RPM** — rising to 100% (395 RPM)
- [ ] **Engine warm-up** — 2 minutes at IDLE
- [ ] **All systems** — check no caution lights

### Avionics Startup
- [ ] **MFD** — ON
- [ ] **GPS/AHRS** — ON (allow alignment ~3 min)
- [ ] **MMS** — ON (warm-up 3–5 min)
- [ ] **Weapon system** — ON
- [ ] **Radios** — ON
  - VHF/FM: ARC-201
  - UHF: ARC-164
- [ ] **ANVIS (NVG)** — arm if night operations

---

## Hover & Takeoff

### Hover
1. Smoothly raise collective
2. Left pedal with power
3. Achieve stable hover 3–5 ft AGL
4. **Kiowa is lighter and more agile than Huey** — responsive controls

### Takeoff to Forward Flight
1. Push cyclic forward
2. Accelerate through ETL (~40 kts)
3. Climb at 70–80 kts
4. Cruise: **90–100 kts** (best endurance)
5. Max speed: **140 kts**

### Hull-Defilade Technique (Scout Hover)
1. Position helicopter behind ridge/trees
2. **Only MMS ball visible above cover**
3. **DO NOT** hover in open when enemy contact possible
4. Observe through MMS while hull hidden

---

## Navigation (AHRS/GPS)

### GPS Navigation
- [ ] **GPS/AHRS** — ON and aligned
- [ ] **Waypoints** — pre-plan or set via MFD
- [ ] **MFD nav page** — shows bearing, distance, ETE
- [ ] **Heading/HSI** — shown on MFD

### Waypoint Entry
1. Press NAV on MFD
2. Select waypoint number
3. Enter coordinates (UTM/MGRS or Lat/Long)
4. Activate for steering

### Navigation Tips
- GPS provides 10-digit grid square accuracy
- Use MFD map overlay for situational awareness
- Assign friendly unit positions as waypoints for deconfliction

---

## Avionics & Systems

### MFD Pages
| Page | Content |
|---|---|
| NAV | Navigation, waypoints, bearing |
| WPN | Weapon status and selection |
| ENG | Engine parameters |
| MMS | MMS video feed |
| PLT | Pilot formats |

### ANVIS NVG Operations
- [ ] Ambient light check
- [ ] ANVIS aligned and adjusted
- [ ] Interior lighting — NVG compatible (reduced white light)
- [ ] Reduce cockpit light to minimum for NVG

---

## Weapons Employment

### Weapon Stations
| Station | Weapon Options |
|---|---|
| Left stub | 2.75-in rocket pod or .50 cal gun |
| Right stub | AGM-114 Hellfire × 4, or AIM-92 × 2 |

### Master Arm
- [ ] **Weapon Master** — ARM (`O`)
- [ ] Select weapon via MFD WPN page

---

### M296 .50 cal Machine Gun

- Fixed forward firing
- Effective against personnel, light vehicles, aircraft
- Range: up to 1,000 m effective

#### Employment
1. [ ] Select .50 cal on WPN page
2. Point aircraft at target
3. Fire: `Space` or trigger
4. Burst: 2–3 seconds

---

### 2.75-inch Rockets (Hydra 70)

| Variant | Warhead | Use |
|---|---|---|
| M151 HE-FRAG | 10 lb HE | Personnel, soft targets |
| M261 MPSM | Multi-point | Area targets |
| M264 WP | White phosphorus | Marking, incendiary |
| M229 HEAT | Shaped charge | Light armor |

#### Employment
1. [ ] Select rocket pod on WPN page
2. Set salvo: 1, 2, or ripple
3. Dive: 10°–20° toward target
4. Aim MFD/HUD pipper on target
5. Fire at 600–1,200 m: `Space`
6. Pull off at 300 m minimum

---

### AGM-114 Hellfire

The Hellfire is the primary anti-armor weapon of the OH-58D.

| Variant | Guidance | Range | Target |
|---|---|---|---|
| AGM-114A/C | SALH (Semi-Active Laser Homing) | 500m–8km | Armor |
| AGM-114K | Laser + IIR | 500m–8km | Armor, moving |
| AGM-114L Longbow | MMW Radar (not on Kiowa) | — | — |

#### Hellfire Laser Procedures (SALH)
1. [ ] **Master Arm** — ARM
2. [ ] Select AGM-114 on WPN page
3. [ ] **MMS** — slew to target
4. [ ] **Laser code** — set (match seeker to designator code)
5. [ ] **Laser designate** — activate (`O`)
   - MMS lases target
6. [ ] **Missile ready** — confirm (MFD indication)
7. [ ] **Fire:** `Space`
8. [ ] **Hold laser on target** until impact

#### Hellfire Buddy Lase
- OH-58D can designate for other aircraft's Hellfires
- Or can lase while another aircraft fires
- Coordinate laser codes before mission

#### Hellfire from Defilade
1. Position behind cover
2. **Pop up** just above ridgeline
3. **MMS** — immediate acquire target, lase
4. **Fire** from behind cover if pop-up attack
5. Or **fire from cover** — MMS can guide up to 45° off-axis

> **Tip:** The Kiowa's key advantage is firing from defilade. Master hull-defilade technique for survivability.

---

### AIM-92 Stinger

Self-defense air-to-air weapon.

1. [ ] Select AIM-92 on WPN page
2. Acquire airborne target
3. Seeker tone when locked
4. Fire: `Space`

---

## Scout Procedures

### RSTA (Reconnaissance, Surveillance, Target Acquisition)

#### Scout Mission Sequence
1. [ ] Plan approach — avoid open ground
2. [ ] **Move by bounds** — low level, terrain masking
3. [ ] **Occupy OP** (Observation Post) — behind cover
4. [ ] **MMS** — scan sector
5. [ ] **ID targets** — report to FAC/attack aircraft
6. [ ] **Lase** for attack aircraft as needed
7. [ ] After engagement — **confirm BDA** (Battle Damage Assessment)

#### Target Report Format (SALUTE)
```
Size:      (number of vehicles/personnel)
Activity:  (stationary, moving, etc.)
Location:  (8/10-digit grid)
Unit:      (type — T-72, BMP, truck)
Time:      (time of observation)
Equipment: (additional info)
```

---

## Laser Designation

### Laser Codes
- Default code: **1688** (check with FAC/flight lead)
- Must match: designator code = seeker code

### Self-Designation Procedure
1. [ ] MMS on target
2. [ ] Laser STANDBY — check code
3. [ ] Fire weapon (`Space`) — missile launches
4. [ ] Immediately lase: `O` (hold until impact)
5. [ ] Do not break hard — laser must stay on target

### Remote Designation (for Other Aircraft)
1. [ ] Coordinate laser codes with requesting aircraft
2. [ ] Get target info (grid, description)
3. [ ] MMS to target area — acquire target
4. [ ] Notify aircraft: "Ready to lase"
5. [ ] On fire: lase immediately — hold until "Splash"

---

## Defensive Procedures

### No Chaff/Flare (Standard Kiowa)
- Limited/no self-protection
- **Survivability = tactics**

### Threat Response
1. **Break** immediately on threat warning
2. **Dive** to terrain masking
3. **Extend** — distance is life for unprotected aircraft
4. Never hover in open if SAM/AAA present

### Threat Identification
- Use MMS to ID threats from defilade
- Report threat positions to higher/attack aircraft
- Do not engage beyond weapons capability

---

## Landing Checklist

### Normal Approach
1. Reduce airspeed to 60 kts on final
2. Decelerate smoothly — collective/cyclic coordination
3. Arrive at hover: 3–5 ft AGL
4. **Set down** — collective full down

### Running Landing
- Can land at 20–30 kts if area allows
- Reduces power required and exposure time

---

## Shutdown Checklist

- [ ] **Set down** at parking
- [ ] **Parking Brake** — SET (`W`)
- [ ] **Weapons** — SAFE
- [ ] **MMS** — STOW/OFF
- [ ] **Throttle** — IDLE
- [ ] Cool: 1–2 minutes
- [ ] **Throttle** — CUT-OFF
- [ ] **All avionics** — OFF
- [ ] **Battery** — OFF

---

## Emergency Procedures

### Engine Failure
1. **COLLECTIVE** — lower immediately
2. Enter autorotation (same procedure as UH-1H)
3. Airspeed: 65 kts for best autorotation
4. Flare at 50 ft
5. Cushion landing

### Single Engine (N/A — Single Engine Aircraft)
- Kiowa is single-engine — any engine failure = autorotation

---

## Keyboard & Joystick Reference

### Flight Controls
| Function | Key | Axis |
|---|---|---|
| Collective Up/Down | `PgUp / PgDn` | Collective |
| Pitch | `Numpad 8/2` | Stick Y |
| Roll | `Numpad 4/6` | Stick X |
| Yaw | `Z / X` | Pedals |

### MMS Controls
| Function | Key |
|---|---|
| MMS slew up | `Numpad 8` |
| MMS slew down | `Numpad 2` |
| MMS slew left | `Numpad 4` |
| MMS slew right | `Numpad 6` |
| Laser on/off | `O` |
| TV/FLIR toggle | MFD OSB |

### Weapons
| Function | Key |
|---|---|
| Master Arm | `O` |
| Fire / Release | `Space` or trigger |
| Jettison | `LAlt + J` |

### Navigation
| Function | Key |
|---|---|
| F10 Map | `F10` |
| Radio Menu | `\` |

---

## Cross-References
- [UH-1H Huey →](uh-1h-huey.md)
- [Mi-24 Hind →](mi-24-hind.md)
- [9-Line CAS Procedures →](../procedures/9-line-cas.md)
- [Radio Communications →](../procedures/radio-communications.md)
- [Airfield & ATC →](../procedures/airfield-atc-communications.md)

---

*Based on Eagle Dynamics DCS OH-58D documentation. For simulation use only.*

<!-- Co-authored-by: Copilot <223556219+Copilot@users.noreply.github.com> -->
