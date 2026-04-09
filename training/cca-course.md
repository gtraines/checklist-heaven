# Close Combat Attack (CCA) Aviation Course
> **Course:** Helicopter Close Combat Attack | **Aircraft:** UH-1H Huey, OH-58D Kiowa Warrior, Mi-24P Hind
> [← Back to Index](index.md)

---

## Table of Contents

1. [Course Overview](#course-overview)
2. [Quick Reference: Essential Brevity Codes](#quick-reference-essential-brevity-codes)
3. [Phase 1: Direct Attack Fundamentals](#phase-1-direct-attack-fundamentals)
4. [Phase 2: Weapons Systems & Employment](#phase-2-weapons-systems--employment)
5. [Phase 3: Close Combat Attack (CCA) & JTAC Coordination](#phase-3-close-combat-attack-cca--jtac-coordination)
6. [Phase 4: Scout/Recce & Hunter-Killer Operations (FAC-A)](#phase-4-scoutrecce--hunter-killer-operations-fac-a)
7. [References](#references)

---

## Course Overview

This course provides a structured progression in helicopter close combat attack operations for DCS World. Students will develop proficiency in direct attack techniques, platform-specific weapons employment, CCA coordination with ground forces, and Hunter-Killer team operations with the OH-58D as the primary scout asset.

> **CCA vs. CAS — A Critical Distinction:**
> - **CCA (Close Combat Attack):** A hasty, pilot-initiated attack. The ground unit acts as an *observer*, not a controller. The pilot has authority to engage. Governed by **FM 3-04.126**.
> - **CAS (Close Air Support):** Requires a qualified JTAC or FAC(A) to formally clear aircraft "Hot." Governed by **JP 3-09.3 / MCWP 3-23.1**.
>
> Helicopter crews may execute either, depending on the tactical situation and proximity to friendly forces.

**Prerequisites:**
- Aircraft type qualification (see [UH-1H Checklist](../checklists/aircraft/uh-1h-huey.md), [OH-58D Checklist](../checklists/aircraft/oh-58d-kiowa.md), [Mi-24P Checklist](../checklists/aircraft/mi-24-hind.md))
- Basic navigation and radio communications (see [Radio Communications](../checklists/procedures/radio-communications.md))
- Familiarity with NOE (Nap-of-the-Earth) and contour flight techniques

**Course Structure:**

| Phase | Title | Focus | Hours (Approx.) |
| :---: | :--- | :--- | :---: |
| 1 | Direct Attack Fundamentals | Flight profiles, Terrain masking, Attack patterns | 4 |
| 2 | Weapons Systems & Employment | Platform-specific switchology, Rockets, ATGMs, Guns | 4 |
| 3 | CCA & JTAC Coordination | 5-Line, 9-Line, Keyhole, Cleared Hot | 4 |
| 4 | Scout/Recce & Hunter-Killer | FAC-A, Buddy Lase, Target Handover | 4 |

**Applicable References:**
- FM 3-04.126 (Attack Reconnaissance Helicopter Operations)
- JP 3-09.3 (Joint Procedures for Air Operations in CAS)
- MCWP 3-23.1 (Close Air Support)

---

## Quick Reference: Essential Brevity Codes

| Code | Meaning |
| :--- | :--- |
| **TALLY** | Pilot has the target in sight |
| **VISUAL** | Pilot has the friendly element in sight |
| **CONTACT** | Pilot has the reference landmark or mark in sight |
| **BLIND** | Pilot does NOT have friendly element in sight |
| **NO JOY** | Pilot does NOT have the target in sight |
| **IN** | Commencing attack run |
| **OFF** | Attack complete; egressing target area |
| **RIFLE** | Air-to-ground guided missile fired (Hellfire/Vikhr/Shturm) |
| **GUNS GUNS GUNS** | Cannon/minigun run in progress |
| **SPLASH** | Rounds on target |
| **CLEARED HOT** | JTAC authorizes weapon employment |
| **ABORT** | Cease attack; do not employ weapons |
| **BINGO** | Fuel state requiring RTB |
| **WINCHESTER** | Out of all ordnance |
| **MASKED** | Aircraft has gone behind terrain cover |
| **UNMASKED** | Aircraft has exposed itself from behind cover |
| **SPARKLE** | IR pointer is on target |
| **SNAKE** | Wiggling IR pointer to identify/confirm |

---

## Phase 1: Direct Attack Fundamentals

### Learning Objectives
- Execute Running Fire, Diving Fire, and Hover Fire attack profiles for each airframe.
- Demonstrate terrain masking, unmask-fire-remask sequences.
- Execute Racetrack, Figure-8, L-Attack, and Cloverleaf attack patterns.
- Identify and avoid Weapon Engagement Zones (WEZ) based on threat type.

---

### 1.1 Helicopter Flight Profiles

#### Running Fire
Engaging targets while in level or shallow-dive forward flight (>40 KIAS).

| Airframe | Recommended Speed | Dive Angle | Engagement Range |
| :--- | :--- | :--- | :--- |
| UH-1H | 60–90 KIAS | 0–10° | 600–1,500 m |
| OH-58D | 50–70 KIAS | 0–5° | 600–2,000 m (Hellfire) |
| Mi-24P | 180–250 km/h | 0–15° | 1,000–3,000 m |

**Technique:**
1. Approach target at low altitude (below terrain masking line if possible).
2. Acquire target using aircraft optics or visual.
3. Fire rockets/cannon while passing through engagement parameters.
4. Continue forward and break left or right off target.

> **Survivability Note:** Running fire keeps the helicopter as a moving target, reducing accuracy of AAA/small arms. Do not fly straight-and-level for more than 3–5 seconds over a defended target.

---

#### Diving Fire
Initiating an attack from altitude with a 15–20° nose-low attitude.

| Airframe | Setup Altitude | Break-off Altitude | Range at Release |
| :--- | :--- | :--- | :--- |
| UH-1H | 1,500–2,000 ft AGL | 300–500 ft AGL | 600–1,200 m |
| Mi-24P | 1,500–2,000 ft AGL | 400–600 ft AGL | 1,000–2,500 m |
| OH-58D | Not recommended (limited rockets) | — | — |

**Technique:**
1. Climb to setup altitude above the terrain masking line.
2. Acquire target and roll in to 15–20° dive.
3. Fire between 1,500–2,500 m slant range.
4. Pull to 4G to recover; clear of fragmentation before 300 ft AGL.

---

#### Hover Fire (Masking/Unmasking)
Engaging from a stationary hover, using terrain to limit exposure time.

```
        [TREE LINE / RIDGE]
         _______________
        |               |
        |   MASKED      |  ← Establish hover here
        |   (Covered)   |
         _______________
              ↑ Unmask (collective up, expose rotor/sight)
              ↓ Re-mask (collective down, break LOS)
```

**Technique:**
1. Establish hover behind cover, at OGE if required.
2. **Unmask:** Increase collective briefly to expose sensors or weapons above the masking line.
3. Acquire and fire (Hellfire, Vikhr, or Shturm).
4. **Re-mask immediately:** Reduce collective, return behind cover.
5. **Exposure time:** Target < 10 seconds to reduce vulnerability to return ATGM fire.

> **OH-58D Advantage:** The Mast Mounted Sight (MMS) allows the scout to remain in **hull defilade**, exposing only the mast to lase or designate. The helicopter body remains below the terrain mask.

---

### 1.2 Attack Patterns

#### Racetrack
```
  ←←←←←←←←←←←←←←←←←
  ↑   (Outbound leg)  ↓
  ↑                   ↓ Rearm/reorient
  ↑                   ↓
  →→→→→→→[TGT]→→→→→→→
          (Inbound / Attack Leg)
```
- **Use:** Sustained suppression, repeated attack passes.
- **Airframes:** All. Best for Mi-24P with multiple attack passes.

#### Figure-8
- Continuous S-turn keeping the target consistently on one side.
- **Use:** Observation or continuous fire while retaining maneuver energy.
- **Airframes:** OH-58D (recce), UH-1H.

#### L-Attack
- Approach from one direction, fire, and break 90° on egress.
- **Use:** Denies enemy the ability to lead the aircraft's flight path for AAA/MANPADS.
- **Airframes:** All. Recommended for any MANPADS threat.

#### Cloverleaf
- Multiple attack runs from different headings (e.g., North → West → South → East).
- **Use:** Suppression of a fortified position with 360° coverage.
- **Airframes:** Mi-24P (best suited for aggressive multi-direction attack).

---

### Practice Mission Profile — Phase 1

| Element | Detail |
| :--- | :--- |
| **Mission** | "First Blood" — Basic Direct Attack |
| **Weather** | VMC, Day, Visibility > 10 NM |
| **Threat** | Light infantry, ZU-23 in open (avoid MANPADS for Phase 1) |
| **Objectives** | Execute one Running Fire pass, one Diving Fire pass, and one Hover-Fire-Remask cycle against designated targets. |
| **Success Criteria** | Weapons on target for 2 of 3 passes; No exposure > 15 seconds on Hover Fire; Correct pattern execution identified by instructor. |

---

## Phase 2: Weapons Systems & Employment

### Learning Objectives
- Configure and employ rockets, cannon, and ATGMs for each airframe.
- Execute Hellfire LOBL and LOAL engagements (OH-58D).
- Execute Vikhr/Shturm guidance discipline for the Mi-24P.
- Control door gunners and flex sights in the UH-1H.

---

### 2.1 UH-1H Huey — Weapons & Switchology

**Primary Weapons:** M134 Minigun (flex), M60D Door Guns, 2.75" Hydra-70 Rockets (M157/M159 pods).

#### Flex Sights & Minigun
| Seat | Control | Notes |
| :--- | :--- | :--- |
| **Pilot (Right)** | XM60 Reflex Sight — Fixed-forward fire | Aim aircraft to aim gun |
| **Co-Pilot (Left)** | Flexible Sight — Off-axis minigun | Pantograph slew; fires independently of nose |

**Rocket Employment:**
The Huey lacks a ballistic computer for rockets. Pilots use manual sight depression based on range.

| Range | Sight Depression (Approx.) |
| :---: | :---: |
| 1,000 m | 20–25 mils |
| 1,500 m | 35–40 mils |
| 2,000 m | 50–60 mils |

1. Establish a running fire approach at 60–90 KIAS.
2. Depress XM60 sight to the appropriate graduation.
3. Place the pipper on target.
4. Fire a burst of 7–14 rockets; break off after firing.

#### Door Gunners
| Mode | Technique |
| :--- | :--- |
| **AI Free Fire** | Set ROE to "Free" via `LWin + H` menu. Gunners engage on their own. |
| **AI Return Fire Only** | Set ROE to "Return" — passive until engaged. |
| **Player Control** | Take gunner seat; aim manually with TrackIR / Mouse Look. |

> **DCS Tip:** For CCA support, set door gunners to "Free" on initial approach; switch to "Hold Fire" if friendlies are in the arc to prevent fratricide.

---

### 2.2 OH-58D Kiowa Warrior — Weapons & Switchology

**Primary Weapons:** MMS Laser Designator/Sight, AGM-114 Hellfire, 2.75" Rockets, M3P .50 cal.

#### Mast Mounted Sight (MMS) — Targeting & Lasing

| Action | Procedure |
| :--- | :--- |
| **Activate MMS** | Select TV or Thermal on MFD |
| **Slew** | Thumbwheel / Slew Axis |
| **Range Only** | First detent laser — "R" appears |
| **Designate** | Second detent laser — "L" appears, begins ranging/designating |
| **Laser Code** | Must match receiver code (default 1688) |

#### Hellfire Employment — LOBL vs. LOAL

**LOBL (Lock-On Before Launch):**
1. Unmask and slew MMS to target.
2. Acquire laser lock on target ("Box" appears on seeker).
3. Confirm seeker is tracking.
4. Fire — missile guides directly to laser spot.
5. Re-mask if required; maintain lase until impact.

**LOAL (Lock-On After Launch):**
1. Select LOAL mode: `DIR` (Direct), `LO` (Low), or `HI` (High trajectory).
2. Fire without visual on target (shooter can be masked).
3. Missile climbs to programmed trajectory, then acquires the laser spot downrange.
4. Scout/Observer unmasks and lases target as missile is in flight.

> **LOAL Advantage:** The firing aircraft never needs LOS to the target. The OH-58D can remain masked while another aircraft (or the scout itself, once repositioned) provides the laser spot.

---

### 2.3 Mi-24P Hind — Weapons & Switchology

**Primary Weapons:** GSh-30K 30mm Fixed Cannon, 9M114 Shturm / 9M120 Ataka ATGM, S-5 / S-8 / S-24 Rockets.

#### Crew Role Distribution
| Crew Position | Primary Function |
| :--- | :--- |
| **Pilot (Rear)** | Aircraft handling, Fixed cannon, Rockets, Rocket system mode |
| **CP/G (Front / Petrovich AI)** | Raduga-Sh optics, Target acquisition, ATGM guidance |

#### 30mm Fixed Cannon (GSh-30K)
1. Set ASP-17BTs gunsight to **Auto** mode for computed lead.
2. Fly a 10–15° dive at target.
3. Open fire at 1,500–2,000 m slant range.
4. Burst length: 20–30 rounds (Low rate for precision; High rate for saturation).
5. Break off by 600–800 m slant range.

> **DCS Note:** In Auto mode the ASP-17 pipper compensates for ballistic drop and aircraft velocity. Manual mode is used only if Auto is unavailable.

#### Shturm / Ataka ATGM Employment (SACLOS)
The Shturm and Ataka are SACLOS-guided (Semi-Automatic Command to Line-Of-Sight). The CP/G's optic crosshair must remain on the target from launch to impact.

1. **Before Launch:**
   - CP/G (or player in CP/G seat): Uncage Raduga-Sh sight (`O`).
   - Slew to target; acquire track.
   - *Cage* the sight if not ready to prevent gimbal lock during maneuvering.
2. **Launch:**
   - Pilot stabilizes aircraft on approach (minimal bank, <20°).
   - CP/G places crosshair on target and fires.
3. **Guidance:**
   - CP/G maintains crosshair on target for the full flight time (~12–15 sec for 3 km).
   - **CRITICAL:** Pilot must NOT bank excessively or pull >2G during missile flight — excessive maneuver causes the missile to lose guidance.
4. **Petrovich AI (Single Player):**
   - Designate target to Petrovich via the target designation system.
   - Petrovich will autonomously guide the missile; pilot focuses on maintaining the required flight parameters.

---

### Practice Mission Profile — Phase 2

| Element | Detail |
| :--- | :--- |
| **Mission** | "Iron Fist" — Weapons Qualification |
| **Weather** | VMC, Day |
| **Threat** | Mixed armor/APC (T-72, BMP), ZSU-23-4 Shilka (moderate AAA) |
| **Objectives** | Destroy 2x armor targets per airframe using each available weapons system (rockets, cannon/minigun, ATGM/Hellfire) within a 10-minute window. |
| **Success Criteria** | 4 of 6 targets destroyed; correct LOBL/LOAL procedures used (OH-58D); ATGM guidance maintained to impact (Mi-24P); No fratricide. |

---

## Phase 3: Close Combat Attack (CCA) & JTAC Coordination

### Learning Objectives
- Demonstrate the CCA 5-Line format for hasty attacks.
- Execute a formal CAS 9-Line with a JTAC (or AI JTAC).
- Utilize the Keyhole CAS template adapted for rotary wing assets.
- Transition from "Observer-directed CCA" to "JTAC-Cleared-Hot CAS."

---

### 3.1 The CCA 5-Line — Hasty Attack Coordination

The 5-Line is the primary call format when a ground unit requests immediate helicopter fire support. The ground unit acts as an **observer**, not a controller — the helicopter pilot retains final engagement authority.

| Line | Item | Example |
| :--- | :--- | :--- |
| **1** | Observer ID / Warning Order | "Uzi 9-1, fire mission, helicopter" |
| **2** | Friendly Location / Mark | "My pos marked by IR strobe, grid NB 123 456" |
| **3** | Target Location | "From my pos, direction 030, distance 800m" |
| **4** | Target Description / Mark | "BMP-2 in open, moving north, marked by tracer" |
| **5** | Remarks / Method | "Danger Close (600m), At My Command, expend all" |

**Readback:** The pilot reads back Lines 3, 4, and any Danger Close declarations.

**Danger Close Thresholds (Rotary Wing):**
| Weapon | Danger Close Distance |
| :--- | :--- |
| 2.75" Rockets | 300 m from friendlies |
| 20mm/30mm Cannon | 200 m from friendlies |
| ATGMs (Hellfire/Vikhr) | 200 m from friendlies |

---

### 3.2 The CAS 9-Line (Rotary Wing Adaptation)

When operating under a qualified JTAC, helicopter crews use the standard 9-Line with rotary-wing adaptations.

| Line | Item | Rotary Wing Note |
| :--- | :--- | :--- |
| **1** | IP / Battle Position (BP) | Use BP instead of IP for helicopters; may be a hover point |
| **2** | Heading | Often omitted if attacking from hover; include for running fire |
| **3** | Distance | BP to target (meters preferred for rotary) |
| **4** | Target Elevation | As normal — **Readback required** |
| **5** | Target Description | As normal |
| **6** | Target Coordinates | MGRS preferred — **Readback required** |
| **7** | Mark | Laser code, WP, Smoke, or IR |
| **8** | Friendlies | Location of nearest friendly; Danger Close is critical |
| **9** | Egress | "Re-mask to Battle Position Delta" or "Egress West" |

**Remarks:** "Final attack heading 030 through 060. Danger Close. Expend all rockets."

---

### 3.3 Keyhole CAS — Rotary Wing Adaptation

The Keyhole Template is adapted for rotary wing by replacing "Holding" racetrack patterns with **Holding Areas (HA)** and **Battle Positions (BP)**.

#### Keyhole Geometry

```
                  ALPHA (NORTH)
                      |
                    [HA-A]
                      |
   DELTA (WEST) ----[TGT/ECHO]---- BRAVO (EAST)
   [HA-D]                            [HA-B]
                      |
                    [HA-C]
                      |
                  CHARLIE (SOUTH)
```

| Point | Designation | Position | Typical Use |
| :--- | :--- | :--- | :--- |
| **Alpha** | HA-A | North of target | Staging / Initial hold |
| **Bravo** | HA-B | East of target | Alternate hold / Egress |
| **Charlie** | HA-C | South of target | Stack overflow |
| **Delta** | HA-D | West of target | Attack hold |
| **Echo** | Overhead | Above target | FAC-A orbit or direct overhead |

#### Holding Area (HA) vs. Battle Position (BP)
- **HA (Holding Area):** A terrain-masked area at distance (3–8 km from target) where aircraft loiter, fuel permitting. Aircraft remain masked and monitor radio.
- **BP (Battle Position):** A specific firing point on the edge of the engagement area (1–2 km from target) from which the aircraft will unmask and engage.

**Execution:**
1. JTAC/FAC-A: "Uzi 1-1, hold at Alpha, 5 kilometers."
2. Aircraft: Moves to HA-A, establishes masked hover or low orbit.
3. JTAC/FAC-A: Passes 9-Line or 5-Line while aircraft is at HA.
4. JTAC/FAC-A: "Uzi 1-1, proceed Battle Position Delta." (Moves aircraft to BP-D, west of target.)
5. Aircraft: "Uzi 1-1, in from Battle Position Delta."
6. JTAC: "Uzi 1-1, Cleared Hot."
7. Aircraft: Unmasks from BP, fires, re-masks. "Uzi 1-1, off, Splash."

---

### 3.4 Direct Attack (Uncontrolled CCA)

When no JTAC or ground observer is available, helicopter crews execute Direct Attack based on mission briefing data and crew coordination.

1. **Pre-Mission:** Target grid, description, and friendlies' position confirmed in mission briefing.
2. **Target Area:** Ingress via terrain masking at NOE.
3. **Target Acquisition:** Pilot or CP/G acquires target visually or via sensors.
4. **Engagement:** Crew confirms no friendlies in the weapons arc.
5. **Execution:** Engage using Running Fire or Hover Fire.
6. **Battle Damage Assessment (BDA):** Remain in the area only long enough to observe first-round impact; report "Splash" and effect.

---

### Practice Mission Profile — Phase 3

| Element | Detail |
| :--- | :--- |
| **Mission** | "Haymaker" — CCA/CAS Integration |
| **Weather** | VMC, Day |
| **Threat** | Infantry, light armor (ZSU-23-4), MANPADS possible |
| **Objectives** | (1) Execute a full CCA 5-Line tasking from an AI ground unit. (2) Check in with a JTAC, receive a 9-Line, hold at Alpha 5, move to BP Delta, and execute Cleared Hot engagement using Keyhole template. |
| **Success Criteria** | Correct 5-Line readback; Correct 9-Line readback (lines 4, 6, restrictions); Aircraft holds at correct Keyhole point; Weapon delivered after Cleared Hot call; No engagement before Cleared Hot. |

---

## Phase 4: Scout/Recce & Hunter-Killer Operations (FAC-A)

### Learning Objectives
- Employ the OH-58D in hull defilade for target acquisition and laser designation.
- Coordinate a Hunter-Killer team (OH-58D + Mi-24P or UH-1H).
- Pass targets via Laser Spot, IR Sparkle, and Talk-On.
- Manage a two-ship stack using Keyhole holding.

---

### 4.1 Scout / Recce Role

#### OH-58D — Primary Scout Platform

The OH-58D's Mast Mounted Sight (MMS) provides a decisive advantage: the helicopter body can remain below terrain while only the MMS is exposed.

**Hull Defilade Procedure:**
1. Position the OH-58D behind a ridgeline, treeline, or building.
2. Hover at the lowest altitude possible while keeping the MMS line-of-sight to the target area.
3. Slew MMS to target area (TV or Thermal).
4. Designate target with laser.
5. Call "Sparkle" (IR mode) or "Laser On" to the shooter.
6. Re-mask immediately after designation.

#### UH-1H — Visual Recce Only
The Huey has no long-range optics. Scout duties are limited to:
- **Mark 1 Eyeball:** Low/slow over-flight to confirm targets visually.
- **Recce by Fire:** Firing a single WP rocket near suspected enemy positions to observe reaction.
- **Lead the Shooter:** Fly ahead of the Mi-24P at low altitude and call targets by direction and distance.

---

### 4.2 Hunter-Killer Team Operations

#### Team Composition

| Team Name | Scout | Shooter | Notes |
| :--- | :--- | :--- | :--- |
| **Light (Pink) Team** | OH-58D | UH-1H | Best for lightly defended targets; Huey suppresses, Scout designates |
| **Heavy Team** | OH-58D | Mi-24P | Preferred for armor; LOAL Hellfire or Vikhr engagement |
| **Heavy Hind Team** | Mi-24P (High) | Mi-24P (Low) | High ship spots/suppresses from 1,500 ft; Low ship attacks NOE |

---

#### Light Team — OH-58D + UH-1H

```
[OH-58D at HA-A, hull defilade, MMS on target]
          ↓ Calls target to UH-1H
[UH-1H at HA-D, masked, waiting]
          ↓ "Cleared Hot" from Scout or JTAC
[UH-1H Unmasks → Running Fire Attack → Re-masks to HA-B]
          ↓ OH-58D: "Splash observed, assess 1x BMP destroyed."
```

**Communication Flow:**
1. OH-58D: "Uzi 1-1 has tally on BMP-2, grid NB 123 456, heading 010."
2. UH-1H: "Uzi 2-1, contact, ready at Delta."
3. OH-58D: "Uzi 2-1, Cleared Hot from Delta, egress Bravo."
4. UH-1H: "In from Delta." *[Unmasks, fires rockets.]* "Off, Splash."
5. OH-58D: "Uzi 2-1, direct hit, BMP destroyed. Re-mask to Alpha."

---

#### Heavy Team — OH-58D + Mi-24P (LOAL Hellfire)

The most tactically capable rotary wing configuration. The OH-58D fires the laser from hull defilade; the Mi-24P fires a Hellfire in LOAL mode and never exposes itself.

```
[Mi-24P at BP-Delta, masked behind ridgeline]
          ↓ Fires Hellfire LOAL-HI
[Missile climbs above terrain, seeks laser spot]
          ↓ Scout designates from hull defilade at HA-Alpha
[Hellfire guides onto laser spot]
[Mi-24P remains masked throughout — never exposes to threat]
```

**Laser Synchronization:**
- Both aircraft set to the same laser PRF code (e.g., 1688).
- OH-58D: Confirm "Laser On" before missile arrives in terminal phase (~5 sec before impact).
- Mi-24P: Confirm "Rifle" at launch; "Steady" to indicate aircraft is stable.

---

#### Heavy Hind Team — Hi-Lo Tactics

1. **High Ship (1,500–2,000 ft AGL):** Draws AAA/MANPADS attention; provides overwatch. Fires ATGMs from range.
2. **Low Ship (NOE, <100 ft AGL):** Approaches unseen using terrain masking. Fires rockets or cannon at close range.
3. **Deconfliction:** High ship calls "In" before firing; Low ship holds until High ship is "Off" and clear of fragmentation.

---

### 4.3 Target Handover Methods

#### 1. Laser Spot (Primary)
- **Requirement:** Both aircraft must have Laser Spot Search (LSS) or coded receiver.
- **Geometry ("The Basket"):** Shooter must be within ±60° of the laser line-of-sight to acquire the spot.
- **Procedure:**
    1. Scout: "Laser On, code 1688."
    2. Shooter: Searches for laser spot on seeker or MFD.
    3. Shooter: "Contact Laser / Spot." Fires.

#### 2. IR Sparkle (Night Operations)
- **Requirement:** Crew Night Vision Devices (NVGs).
- **Procedure:**
    1. Scout: "Sparkle On." (Activates IR pointer toward target.)
    2. Shooter: "Contact Sparkle."
    3. Scout: "Snake." (Wiggles pointer to confirm identification.)
    4. Shooter: Acquires on NVGs and attacks.

#### 3. Talk-On (Day / No NVGs)
Guide the shooter from a large feature down to the specific target.
1. **Anchor:** "See the north-south road at grid NB 12?"
2. **Funnel:** "Follow the road south to the bridge."
3. **Reference:** "Just east of the bridge, the tree line."
4. **Target:** "At the east end of the tree line — BMP-2 facing south."
5. Scout: "Call Tally."

> **DCS Resolution Tip:** Avoid subtle references ("the slight hill"). Use high-contrast, identifiable objects — roads, rivers, buildings, smoke, or fire.

---

### 4.4 Stack Management (FAC-A Role)

When the OH-58D or a designated aircraft is acting as FAC-A, it manages all rotary and fixed-wing assets in the battlespace.

**Wedding Cake (Altitude Blocks):**
| Layer | Altitude Block | Occupant |
| :--- | :--- | :--- |
| **High (Transit)** | Angels 12–15 | Fixed-wing checking in; awaiting tasking |
| **Middle (Stack)** | Angels 8–11 | Rotary wing holding at Keyhole points |
| **Low (Working)** | Below Angels 8 | FAC-A or attacking aircraft |

**Deconfliction Call:**
> "All stations Hammer, FAC-A is Uzi 9-1 at Echo, Angels 8. Rotary wing hold at Alpha or Delta below Angels 6. Fixed wing Angels 12 and above. Report ready."

---

### Practice Mission Profile — Phase 4

| Element | Detail |
| :--- | :--- |
| **Mission** | "Long Arm" — Hunter-Killer Coordination |
| **Weather** | VMC, Day. Night variant recommended for Sparkle qualification. |
| **Threat** | Armor platoon (3x T-72, 1x ZSU-23-4), MANPADS probable |
| **Objectives** | (1) OH-58D identifies and designates all targets from hull defilade. (2) Mi-24P executes LOAL Hellfire/Vikhr engagement from masked position. (3) UH-1H provides rocket/minigun suppression of Shilka on Scout's call. (4) Conduct a Keyhole stack with both aircraft holding at separate anchors simultaneously. |
| **Success Criteria** | All engagements executed without shooter exposing before "Cleared Hot" or Scout "Laser On"; ZSU neutralized before Mi-24P exposes; Correct Keyhole anchor assignments; Proper target handover sequence (Laser → Contact → Rifle → Splash). |

---

## References

| Reference | Description |
| :--- | :--- |
| **FM 3-04.126** | Attack Reconnaissance Helicopter Operations (US Army) |
| **JP 3-09.3** | Joint Procedures for Air Operations in CAS |
| **MCWP 3-23.1** | Close Air Support (USMC) |
| [UH-1H Huey Checklist](../checklists/aircraft/uh-1h-huey.md) | DCS UH-1H systems and procedures |
| [OH-58D Kiowa Checklist](../checklists/aircraft/oh-58d-kiowa.md) | DCS OH-58D systems and procedures |
| [Mi-24P Hind Checklist](../checklists/aircraft/mi-24-hind.md) | DCS Mi-24P systems and procedures |
| [Surface Attack Course](./surface-attack-course.md) | Fixed-wing equivalent course (A-10, Su-25) |
| [Radio Communications](../checklists/procedures/radio-communications.md) | Frequencies, formats, and radio discipline |

---

*Based on FM 3-04.126 Attack Reconnaissance Helicopter Operations, JP 3-09.3, and Eagle Dynamics DCS World documentation. For simulation use only.*
