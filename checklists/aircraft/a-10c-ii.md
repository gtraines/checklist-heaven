# A-10C II Thunderbolt II — DCS Checklist

> **Aircraft:** Fairchild Republic A-10C II Thunderbolt II "Warthog" | **Role:** Close Air Support / Ground Attack
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [A-10C II vs A-10C Differences](#a-10c-ii-vs-a-10c-differences)
2. [Cockpit Orientation](#cockpit-orientation)
3. [Operating Limitations](#operating-limitations)
4. [Performance & V-Speeds](#performance--v-speeds)
5. [Emergency Procedures (Quick Ref)](#emergency-procedures-quick-ref)
6. [Weapons & Stores (Quick Ref)](#weapons--stores-quick-ref)
7. [Startup Checklist](#startup-checklist)
8. [Navigation (CDU/EGI/SADL)](#navigation-cduegisadl)
9. [Avionics & Systems](#avionics--systems)
   - [MFCD Operations](#mfcd-operations)
   - [TGP Sniper XR](#tgp-sniper-xr)
   - [HMCS/JHMCS](#hmcsjhmcs)
   - [Link-16 / SADL](#link-16--sadl)
10. [HOTAS Reference](#hotas-reference)
11. [Weapons Employment](#weapons-employment)
    - [GAU-8/A 30mm Cannon](#gau-8a-30mm-cannon)
    - [AGM-65 Maverick](#agm-65-maverick)
    - [JDAM (GBU-31/32/38)](#jdam-gbu-313238)
    - [Paveway LGB](#paveway-lgb)
    - [GBU-54 Laser JDAM](#gbu-54-laser-jdam)
    - [SDB GBU-39](#sdb-gbu-39)
    - [APKWS Rockets](#apkws-rockets)
12. [Defensive Systems](#defensive-systems)
13. [Landing Checklist](#landing-checklist)
14. [Shutdown Checklist](#shutdown-checklist)
15. [Emergency Procedures (Detailed)](#emergency-procedures)
16. [Keyboard & HOTAS Reference](#keyboard--hotas-reference)

---

## A-10C II vs A-10C Differences

The A-10C II is an upgraded version of the A-10C with the following additions:

| Feature | A-10C | A-10C II |
|---|---|---|
| Targeting Pod | Litening AT | Sniper XR (longer range) |
| Helmet System | HMCS | JHMCS (improved) |
| Datalink | None | Link-16 / SADL |
| ARC-210 Radio | No | Yes (replaces ARC-186) |
| Laser JDAM | No | GBU-54 (Laser + GPS) |
| APKWS | No | Advanced Precision Kill Weapon System |
| Cockpit Glass | Some analog | Additional digital integration |

**Same startup, same base procedures as A-10C.** Refer to [A-10C Checklist](a-10c.md) for shared procedures.

---

## Cockpit Orientation

Same layout as A-10C with additional:

| Addition | Location | Function |
|---|---|---|
| SADL/Link-16 indicator | Center MFCD | Network picture / contacts |
| ARC-210 radio panel | Right console | Multi-band radio |
| JHMCS calibration | Helmet | Enhanced cueing |

---

## Operating Limitations

| Parameter | Limit | Notes |
|---|---|---|
| **Max Takeoff Weight (MTOW)** | ~51,000 lbs | Structural Max (Standard Combat ~47k) |
| **Max Landing Weight** | 46,000 lbs | Structural Limit (Rec. < 40k) |
| **G-Limits** | +7.33 / -3.0 (Clean)<br>+5.0 (Loaded) | Limits reduce with store asymmetry |
| **AoA Limits** | 20–22 Units | Stall warning (chopper) ~20 units |
| **Max Crosswind (Dry)** | 30 kts | Ref: AFMAN 11-2A-10C Vol 3 |
| **Max Crosswind (Wet)** | 20 kts | Wet or contaminated runway |
| **Max Tailwind** | 10 kts | All conditions |
| **Max Headwind (Canopy Open)** | 45 kts | Ground taxi |
| **Max Mach** | M 0.75 | Airframe drag usually limits level flight |
| **APU Operation** | < 15,000 ft | For starting or emergency power |
| **Engine ITT (Start)** | 860°C max | Abort start if exceeded |
| **Engine ITT (Max Continuous)** | 810°C | Normal operations limit |
| **Engine ITT (Transient/TO)** | 900°C | Not to exceed limit |
| **Fan Speed N1** | 98% max | Primary thrust indicator |
| **Core Speed N2** | 99% max | — |

## Performance & V-Speeds

| Regime | Speed (KIAS) | Configuration / Notes |
|---|---|---|
| **Rotation (Vr)** | 135 - 150 | Weight dependent (Avg 140) |
| **Takeoff Speed** | 150 - 160 | Lift-off |
| **Landing Approach** | 130 - 140 | **AoA Indexer (Green Circle)** |
| **Corner Speed** | 280 - 320 | Best Turn Rate |
| **Best Climb (Vy)** | 200 - 220 | Clean / Light Stores |
| **Stall Speed (Vs)** | ~110 | Gear/Flaps Down (Weight dependent) |
| **Max Speed (Vne)** | 450 | Low Altitude Structural Limit |
| **Gear Extension (Vlo)** | 200 | Do not extend above |
| **Flaps Limit (Vfe)** | 200 | Maneuver (MVR) & Down (DN) |
| **Refueling** | 200 - 220 | Typical tanker speed |

## Emergency Procedures (Quick Ref)

> **BOLDFACE** items are critical memory actions per AFMAN 11-2A-10C Vol 3. Perform without reference to checklist.

| Emergency | Immediate Action Steps (Boldface) |
|---|---|
| **ABORT (Engine Failure/Fire on Takeoff)** | 1. **THROTTLES** — IDLE<br>2. **WHEEL BRAKES** — MAX<br>3. **SPEEDBRAKES** — OPEN<br>*(If fire exists:)*<br>4. **FIRE HANDLE** — PULL<br>5. **EXTINGUISHER SWITCH** — FWD/AFT as required |
| **ENGINE FIRE (In Flight)** | 1. **THROTTLE (Affected)** — IDLE<br>2. **FIRE HANDLE (Affected)** — PULL<br>3. **EXTINGUISHER SWITCH** — FWD/AFT as required |
| **DOUBLE ENGINE FAILURE** | 1. **THROTTLES** — IDLE<br>2. **APU SWITCH** — START<br>3. **ENGINE OPERATE SWITCHES** — IGN<br>*(Proceed to crossbleed/APU restart logic)* |
| **MANUAL REVERSION (Hydraulic Failure)** | 1. **FLIGHT CONTROLS** — MAN REVERSION<br>2. **Fly conservatively** — limited control authority<br>3. **Land ASAP** — no flaps, emergency gear |
| **ENGINE RESTART (Air Start)** | 1. **Throttle (dead)** — IDLE<br>2. **Crossfeed** — OPEN if needed<br>3. **APU** — START (below 15,000 ft)<br>4. **ENGINE OPERATE** — IGN |
| **EJECTION** | 1. **EJECTION HANDLE** — PULL |

## Weapons & Stores (Quick Ref)

| Weapon / System | Type | Effective Range | Best Suited For | Simulation Notes |
|---|---|---|---|---|
| **GAU-8/A Avenger** | 30mm Cannon | < 2 NM | **Anti-Armor** (Tanks/IFVs) | PAC stabilizes aiming; massive recoil |
| **AGM-65D/G** | IR Missile | 6-8 NM | Moving Armor, Night Ops | Force Correlate (G) for large targets |
| **AGM-65H/K** | TV Missile | 4-6 NM | High Contrast (Day) | K = Heavy Warhead; H = Light |
| **AGM-65L** | Laser Missile | 6-8 NM | Buddy Lasing | Requires laser code match |
| **GBU-38** | JDAM (500lb) | 5-10 NM | All Weather / Coordinate | GPS Guided; Requires alignment |
| **GBU-54 LJDAM** | Laser+GPS (500lb) | 5-10 NM | **Moving Targets** | **A-10C II Only** — terminal laser guidance |
| **GBU-12** | LGB (500lb) | Varies | Precision Point | Requires TGP lasing |
| **GBU-39 SDB** | GPS Bomb (250lb) | 5-10 NM | Lightly Armored / Soft | 4 per BRU-61 rack; 4 targets per pass |
| **APKWS** | Guided Rocket | 1.5-5 NM | Light Armor / Precision | **A-10C II Only** — SAL guidance |
| **CBU-97 (SFW)** | Sensor Fuzed | Area | **Heavy Armor Columns** | Deploys seeking skeets; "Tank Plinker" |
| **CBU-105 (WCMD)** | GPS Cluster | 5-8 NM | Heavy Armor (Stand-off) | Wind Corrected; accurate from altitude |
| **Hydra 70 (M151)** | 2.75" Rocket | 1-2 NM | Soft Targets, Suppression | CCIP aiming |
| **Sniper XR TGP** | Targeting Pod | N/A | ID / Self-Lasing | Longer range than Litening AT |
| **JHMCS** | Helmet Sight | N/A | Cueing / SA | **A-10C II Only** — "Look-and-shoot" |

## Realism Notes
- **A-10C II vs A-10C:** The "Tank Killer" (II) variant adds the JHMCS, APKWS, GBU-54 LJDAM, SADL/Link-16, and the Sniper XR TGP. Flight performance is identical.
- **Manual Reversion:** In dual hydraulic failure, flight controls must be switched to "Manual Reversion" (Pitch/Roll switches on left console). Control authority is significantly reduced.
- **APKWS Range:** Real-world APKWS range extends to ~5 km; DCS models this accurately. The rocket is semi-active laser homing — do not break laser until impact.

---

## Startup Checklist

### Pre-Start
- [ ] **Parking Brake** — SET (`W`)
- [ ] **Battery** — ON
- [ ] **Emergency Flight Controls** — NORMAL

### Engine Start
*(Same as A-10C — see [A-10C Startup](a-10c.md#startup-checklist))*
- [ ] **Left Engine** — `RAlt + Home`
- [ ] **Right Engine** — `RCtrl + Home`
- [ ] Both at IDLE — stable

### A-10C II Additional Avionics
- [ ] **CDU** — ON
- [ ] **EGI (GPS/INS)** — ON — allow GPS alignment
- [ ] **Sniper XR TGP** — ON (earlier warmup due to better IR detector — ~3 min)
- [ ] **JHMCS** — ON and boresight (see procedure below)
- [ ] **Link-16 / SADL** — ON, set network codes
- [ ] **ARC-210** — ON, set frequencies
- [ ] **IFF** — set Mode 1/2/3/4 codes

### JHMCS (Scorpion HMD) Alignment
1. [ ] **HMCS Power Switch** (Bat/AC panel) — **ON**
2. [ ] **MFCD** — select **HMCS** page
3. [ ] Select **ALIGN**
4. [ ] **Coarse Align:** Look at the HUD boresight cross. Press and hold the designated align button (TMS Up or profile-specific) until "ALIGN OK" appears.
5. [ ] **Fine Align:** Use cursor slews to adjust Az/El/Roll crosshair overlay to match HUD center precisely.
6. [ ] Verify HMCS symbology is visible and conformal with HUD before taxi.

---

## Navigation (CDU/EGI/SADL)

### Standard Navigation
*(Same as A-10C — see [A-10C Navigation](a-10c.md#navigation-cdupegi))*

### SADL Network Navigation
- [ ] **SADL power** — ON (from cockpit panel)
- [ ] **Network ID** — set (mission-specific)
- [ ] **HSD** — shows SADL contacts as symbology
- Blue tracks = friendly aircraft
- Red/yellow tracks = potential threats (if received)
- [ ] **Waypoint** — can receive from SADL network

---

## Avionics & Systems

### MFCD Operations
*(Same as A-10C — see [A-10C MFCD](a-10c.md#mfcd-operations))*

Additional A-10C II MFCD pages:
- `SADL` — datalink network display
- Enhanced `HSD` with network contacts

---

### TGP Sniper XR

The Sniper XR has greater range and resolution than the Litening AT.

- [ ] **Power** — STBY, then OPER
- [ ] Warmup ~3 minutes
- Longer slant range capability vs Litening (~12+ NM effective)
- Improved IMC (In-Cloud) track capability

#### Sniper XR Operation
1. Same procedure as A-10C TGP
2. Greater zoom capability (EFOV)
3. Better long-range target identification
4. **SPI** designation same as Litening

---

### HMCS/JHMCS

#### JHMCS (Joint Helmet Mounted Cueing System)
- [ ] **Power** — ON
- [ ] **Boresight** — look at alignment target, confirm
- [ ] Provides weapons cueing in HMD
- [ ] **HMCS display:** heading, altitude, weapon mode
- [ ] Look at target and press TMS to slave weapon seeker to HMD line-of-sight
- Particularly effective for AGM-65 off-axis slaving

---

### Link-16 / SADL

#### SADL (Situation Awareness Data Link)
- [ ] **SADL** — ON (from power/avionics panel)
- [ ] Set **network address** (mission assigned)
- [ ] **HSD** — select SADL overlay
- [ ] Receive: friendly aircraft positions updated automatically
- [ ] Transmit: own position transmitted to all SADL-equipped friendlies

#### Link-16 Tactical Picture
| Symbol | Meaning |
|---|---|
| Blue diamond | Friendly aircraft |
| Blue circle | Friendly surface |
| Yellow circle | Unknown contact |
| Red square | Hostile (if received) |

---

## HOTAS Reference

*(Same base HOTAS as A-10C — see [A-10C HOTAS](a-10c.md#hotas-reference))*

### A-10C II HOTAS Additions
| Function | Control |
|---|---|
| JHMCS slave weapon | TMS Forward |
| SADL receive/update | DMS Forward (MFCD page) |

---

## Weapons Employment

### Pre-Attack Checks
*(Same as A-10C)*
- [ ] **Master Arm** — ARM
- [ ] **Laser Arm** — ARM
- [ ] **TGP** — OPER, tracking target

---

### GAU-8/A 30mm Cannon
*(Same as A-10C — see [A-10C Cannon](a-10c.md#gau-8a-30mm-cannon))*

---

### AGM-65 Maverick
*(Same as A-10C — see [A-10C Maverick](a-10c.md#agm-65-maverick))*

#### A-10C II Enhancement: JHMCS Cueing
- Look at target with JHMCS
- **TMS Forward** — slaves AGM-65 to LOS
- Confirm lock — fire

---

### JDAM (GBU-31/32/38)
*(Same as A-10C — see [A-10C JDAM](a-10c.md#jdam-gbu-313238))*

---

### Paveway LGB
*(Same as A-10C — see [A-10C LGB](a-10c.md#paveway-lgb-gbu-1012))*

---

### GBU-54 Laser JDAM

The GBU-54 combines GPS guidance with a laser seeker — the best of both:
- **GPS guidance** for initial flight phase
- **Laser terminal guidance** for precision against moving targets

| Advantage | Description |
|---|---|
| Moving target | Can hit vehicles in motion via laser |
| All-weather | GPS guides when laser obscured |
| Reduced CEP | Laser improves accuracy to <1 m |

#### GBU-54 Procedure
1. [ ] **Master Arm** — ARM
2. [ ] **Laser Arm** — ARM
3. [ ] Select GBU-54 on WPN page
4. [ ] **TGP** — designate target, SPI set
5. [ ] **CCRP delivery** — fly release cue
6. [ ] Release at computed point
7. [ ] **Lase immediately** and maintain laser on target
8. [ ] Bomb homes on laser spot in terminal phase
9. [ ] **Effective against moving targets** if laser held

---

### SDB GBU-39
*(Same as A-10C — see [A-10C SDB](a-10c.md#sdb-gbu-39))*

---

### APKWS Rockets

**Advanced Precision Kill Weapon System** — laser-guided 2.75-inch rocket

| Feature | Value |
|---|---|
| Warhead | M151 (10 lb shaped charge) |
| Range | 1.5 – 5 km |
| Guidance | Semi-Active Laser (SAL) |
| Targets | Soft vehicles, light armor, personnel |

> **DSMS Laser Code Setup:** In DSMS → INV → select the APKWS station → **LASER** → set code (default **1688**). Must match the TGP laser code if self-lasing. Set via **LATCH** or **PULSE** mode on the AHCP laser arm switch.

#### APKWS Procedure
1. [ ] **Master Arm** — ARM
2. [ ] **Laser Arm** — ARM
3. [ ] Select APKWS pod on WPN page
4. [ ] **Delivery mode** — CCIP or CCRP (CCRP recommended for loft delivery)
5. [ ] **TGP** — lock target (POINT track mode)
6. [ ] **Lase** — hold laser on target (`O`)
7. [ ] **Fire** at 1.5–5 km range: `Space` or trigger
8. [ ] **Hold laser on target** until impact (~5–8 sec)
9. [ ] Can fire multiple rockets while holding laser

> **Tip:** Very effective against vehicles and light armor. Much cheaper than a Maverick for soft targets. Unlike dumb rockets, do NOT break laser until impact confirmed.

---

## Defensive Systems

*(Same as A-10C — see [A-10C Defensive Systems](a-10c.md#defensive-systems))*

### A-10C II Additional: SADL Threat Warning
- Receive threat information via SADL from other aircraft/AWACS
- HSD shows threat areas (if populated by network)

---

## Landing Checklist

*(Same as A-10C — see [A-10C Landing](a-10c.md#landing-checklist))*

---

## Shutdown Checklist

*(Same as A-10C — see [A-10C Shutdown](a-10c.md#shutdown-checklist))*

Additional:
- [ ] **SADL** — OFF
- [ ] **Link-16** — OFF
- [ ] **JHMCS** — OFF

---

## Emergency Procedures

*(Same as A-10C — see [A-10C Emergencies](a-10c.md#emergency-procedures))*

---


---

## Keyboard & HOTAS Reference

*(Same as A-10C — see [A-10C Reference](a-10c.md#keyboard--hotas-reference))*

### A-10C II Additions
| Function | Key/Action |
|---|---|
| JHMCS slave to LOS | TMS Forward (while in A/G mode) |
| SADL display | MFCD OSB select |

---

## Cross-References
- [A-10C Checklist →](a-10c.md)
- [A-10A Checklist →](a-10a.md)
- [9-Line CAS Procedures →](../procedures/9-line-cas.md)
- [Radio Communications →](../procedures/radio-communications.md)
- [Airfield & ATC →](../procedures/airfield-atc-communications.md)

---

*Based on Eagle Dynamics DCS A-10C II documentation. For simulation use only.*
