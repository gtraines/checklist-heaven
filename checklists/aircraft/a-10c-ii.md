# A-10C II Thunderbolt II — DCS Checklist

> **Aircraft:** Fairchild Republic A-10C II Thunderbolt II "Warthog" | **Role:** Close Air Support / Ground Attack
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [A-10C II vs A-10C Differences](#a-10c-ii-vs-a-10c-differences)
2. [Cockpit Orientation](#cockpit-orientation)
3. [Startup Checklist](#startup-checklist)
4. [Navigation (CDU/EGI/SADL)](#navigation-cduegisadl)
5. [Avionics & Systems](#avionics--systems)
   - [MFCD Operations](#mfcd-operations)
   - [TGP Sniper XR](#tgp-sniper-xr)
   - [HMCS/JHMCS](#hmcsjhmcs)
   - [Link-16 / SADL](#link-16--sadl)
6. [HOTAS Reference](#hotas-reference)
7. [Weapons Employment](#weapons-employment)
   - [GAU-8/A 30mm Cannon](#gau-8a-30mm-cannon)
   - [AGM-65 Maverick](#agm-65-maverick)
   - [JDAM (GBU-31/32/38)](#jdam-gbu-313238)
   - [Paveway LGB](#paveway-lgb)
   - [GBU-54 Laser JDAM](#gbu-54-laser-jdam)
   - [SDB GBU-39](#sdb-gbu-39)
   - [APKWS Rockets](#apkws-rockets)
8. [Defensive Systems](#defensive-systems)
9. [Landing Checklist](#landing-checklist)
10. [Shutdown Checklist](#shutdown-checklist)
11. [Emergency Procedures](#emergency-procedures)
12. [Keyboard & HOTAS Reference](#keyboard--hotas-reference)

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
- [ ] **JHMCS** — ON and boresight
- [ ] **Link-16 / SADL** — ON, set network codes
- [ ] **ARC-210** — ON, set frequencies
- [ ] **IFF** — set Mode 1/2/3/4 codes

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

#### APKWS Procedure
1. [ ] **Master Arm** — ARM
2. [ ] **Laser Arm** — ARM
3. [ ] Select APKWS pod on WPN page
4. [ ] **TGP** — lock target (POINT track mode)
5. [ ] **Lase** — hold laser on target (`O`)
6. [ ] **Fire** at 1.5–5 km range: `Space` or trigger
7. [ ] **Hold laser on target** until impact (~5–8 sec)
8. [ ] Can fire multiple rockets while holding laser

> **Tip:** Very effective against vehicles and light armor. Much cheaper than a Maverick for soft targets.

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
