# Basic and Intermediate Surface Attack Course
> **Course:** Fixed-Wing Surface Attack | **Aircraft:** A-10A, A-10C, A-10C II, Su-25, Su-25T
> [← Back to Index](index.md)

---

## Table of Contents

1. [Course Overview](#course-overview)
2. [Quick Reference: Essential Brevity Codes](#quick-reference-essential-brevity-codes)
3. [Phase 1: Basic Surface Attack (Fundamentals)](#phase-1-basic-surface-attack-fundamentals)
4. [Phase 2: Intermediate Surface Attack (Precision & Systems)](#phase-2-intermediate-surface-attack-precision--systems)
5. [Phase 3: Close Air Support (CAS) & JTAC Coordination](#phase-3-close-air-support-cas--jtac-coordination)
6. [Phase 4: Airborne Forward Air Controller (FAC-A)](#phase-4-airborne-forward-air-controller-fac-a)
7. [References](#references)

---

## Course Overview

This course provides a structured progression from basic unguided surface attack through advanced airborne forward air control operations. Students will develop proficiency across the four primary DCS World fixed-wing surface attack platforms, gaining competency in both high-fidelity and simplified avionics systems before proceeding to joint terminal attack controller (JTAC) coordination and FAC-A duties.

**Prerequisites:**
- Completion of aircraft-specific type qualification (see [aircraft checklists](#references))
- Basic navigation and radio communications proficiency (see [Radio Communications](../checklists/procedures/radio-communications.md))
- Familiarity with air-to-ground weapons loading and arming procedures

**Course Structure:**

| Phase | Title | Focus | Hours (Approx.) |
| :---: | :--- | :--- | :---: |
| 1 | Basic Surface Attack | Attack Patterns & Geometry, Unguided Weapons, Visual Delivery, Safe Escape | 5 |
| 2 | Intermediate Surface Attack | TGP/Shkval, Precision Guided Munitions | 4 |
| 3 | CAS & JTAC Coordination | 9-Line, Check-In, Keyhole CAS | 4 |
| 4 | Airborne FAC-A | Stack Management, Marking, Talk-On | 4 |

**Applicable References:**
- MCWP 3-23.1 (Close Air Support)
- JP 3-09.3 (Joint Procedures for Air Operations)
- DTIC ADA429336 (FAC-A Doctrine)

---

## Quick Reference: Essential Brevity Codes

| Code | Meaning |
| :--- | :--- |
| **TALLY** | Pilot has the target in sight |
| **VISUAL** | Pilot has the friendly element in sight |
| **CONTACT** | Pilot has the reference landmark / mark in sight |
| **BLIND** | Pilot does NOT have friendly element in sight |
| **NO JOY** | Pilot does NOT have the target in sight |
| **IN** | Commencing attack run; entering weapons employment zone |
| **OFF** | Attack complete; egressing the target area |
| **PICKLE** | Bomb/stores released |
| **RIFLE** | Air-to-ground guided missile fired |
| **GUNS GUNS GUNS** | Strafing run in progress |
| **BINGO** | Fuel state at pre-briefed minimum; must RTB or tank |
| **WINCHESTER** | Out of all ordnance |
| **ABORT** | Cease attack; do not employ weapons |
| **CLEARED HOT** | JTAC/FAC-A authorises weapons release |
| **CONTINUE DRY** | Continue the attack pass; do NOT release weapons |
| **KNOCK IT OFF** | Cease all offensive manoeuvring immediately |

---

## Phase 1: Basic Surface Attack (Fundamentals)

### Learning Objectives

Upon completion of Phase 1, the student will be able to:

1. Describe the Standard Basic Surface Attack Pattern and execute correct range brevity calls.
2. Describe the Tactical Surface Attack Pattern and explain how it differs from the basic training pattern.
3. Execute a safe, accurate high-angle dive attack with unguided general-purpose bombs.
4. Execute a low-angle dive / strafe attack with rockets and the gun system.
5. Identify and apply correct frag avoidance and minimum recovery altitudes for all unguided ordnance types.
6. Configure stores management systems (DSMS or simplified equivalents) correctly prior to weapons employment.

---

### 1.1 Attack Patterns & Geometry

Before mastering individual weapon deliveries, pilots must understand how to position the aircraft relative to the target. Two fundamental geometries govern this course: the **Standard Basic Surface Attack Pattern** (range and training operations) and the **Tactical Surface Attack Pattern** (combat employment).

---

#### 1.1.1 Standard Basic Surface Attack Pattern

The basic pattern is the foundation of all range operations. Predictability and repeatability are intentional — the circuit gives pilots a structured, repeatable geometry in which to practise dive angles, airspeed, and release parameters without the added workload of threat management.

**Pattern Legs:**

| Leg | Description |
| :--- | :--- |
| **Crosswind** | Initial turn after recovery to re-enter the downwind. |
| **Downwind** | Parallel to the run-in heading, opposite direction. All pre-attack checks complete here. |
| **Base** | 90° turn from downwind to intercept the run-in heading. Manages spacing to target. |
| **Final (Run-In)** | The attack leg. Acquire target, establish dive parameters, and release. |
| **Recovery** | Immediate 4–5 g pull after weapon release. Egress off-axis; return to pattern altitude. |

**Pattern Diagram (Right-Hand Circuit):**

```
             ↑  DOWNWIND  (pre-attack checks)
             │
             └──►  BASE  (2–3 NM abeam; 90° turn to final)
                   │
                   ↓  FINAL / RUN-IN  ("In" call)
                   │
                  [T]  TARGET  — weapon release
                   │
                   ↑  RECOVERY  ("Off" call; 4–5 g pull)
                   │
              ─────┘  (crosswind — rejoin pattern)
```

**Typical Parameters:**

| Parameter | Value |
| :--- | :--- |
| **Pattern Altitude** | 3,000 – 5,000 ft AGL |
| **Base Distance (abeam target)** | 2 – 3 NM |
| **Run-In Airspeed** | 300 – 350 KIAS |
| **Multi-Ship Spacing** | 30 – 60 seconds |

**Standard Range Calls:**
- **"In"** — Transmitted when commencing roll-in or turning base-to-final.
  *Example:* `"Colt 1-1, In, Heading 270."`
- **"Off [Safe/Armed] [Direction]"** — Transmitted when initiating the recovery pull.
  *Example:* `"Colt 1-1, Off Safe, Right."`

---

#### 1.1.2 Tactical Surface Attack Pattern

Combat employment abandons the rigid circuit in favour of geometries that minimise exposure time, maximise surprise, and enable mutual support. The core principle is unpredictability — varying attack axes, altitudes, and timing to defeat enemy tracking solutions.

**Key Tactical Concepts:**

| Concept | Description |
| :--- | :--- |
| **IP (Initial Point)** | A distinct geographic feature 5–15 NM from the target. Aircraft hold here and depart on sequence. |
| **Wheel / Orbit** | Racetrack or circular hold at the IP; provides continuous observation at standoff. |
| **Pop-Up Attack** | Low-level terrain-masked ingress; rapid climb at the action point to acquire target and dive. |
| **Shooter-Cover** | One aircraft attacks; wingman maintains overwatch and threat suppression. |

**Tactical Considerations:**
- **"One Pass, Haul Ass"** — Avoid re-attacking on the same heading. Predictable runs are the primary cause of loss to radar-directed AAA.
- **Egress Jinking** — Execute aggressive heading and altitude changes immediately after release to deny enemy tracking solutions.
- **Attack Axis Selection** — Brief the attack heading to avoid known threat sectors, maximise safe egress, and prevent fratricide.
- **Terrain Masking** — Use terrain between the IP and target area to reduce radar and visual detection prior to the pop-up or run-in.

---

#### 1.1.3 Pattern Comparison

| Feature | Basic Pattern (Range) | Tactical Pattern (Combat) |
| :--- | :--- | :--- |
| **Primary Goal** | Training, Safety, Repetition | Survivability, Effect on Target |
| **Shape** | Rectangular / Box Circuit | IP Hold, Wheel, Pop-Up, Straight-In |
| **Predictability** | High — intentional | Low — intentional |
| **Entry Point** | Downwind leg | IP or action point |
| **Communications** | Standard range calls (`"In"`, `"Off"`) | Brevity codes, authentication |
| **Threat Environment** | None (simulated) | Active — AAA, SAMs, MANPADS |

---

### 1.2 Weapons Delivery: High-Angle Dive (30–45°)

High-angle dive attacks provide accurate ballistic solutions and maximise frag clearance. They are the primary delivery method for slick (low-drag) general-purpose bombs.

**Applicable Ordnance:** Mk-82, Mk-84, CBU-87/97

| Parameter | Value |
| :--- | :--- |
| Dive Angle | 30° – 45° |
| Release Altitude | 4,000 – 6,000 ft AGL |
| Release Airspeed | 300 – 350 KIAS |
| Minimum Recovery Altitude | 2,000 ft AGL (frag avoidance floor) |

> ⚠️ **SAFETY:** Never release slick stores below 2,000 ft AGL. Frag envelope will reach recovery altitude at lower release points. If the pipper/CCIP solution is not established by the roll-in point, ABORT and re-attack.

**General Attack Geometry:**
1. Establish offset holding altitude (typically 8,000–10,000 ft AGL) on the run-in heading.
2. Roll in at the target, establishing 30–45° nose-low attitude.
3. Confirm dive angle, airspeed, and CCIP/pipper on target.
4. Release at computed altitude (CCIP auto-release or manual pickle).
5. Immediate pull recovery; 4–5 g minimum to clear frag.
6. Egress off-axis from the attack heading.

---

### 1.3 Weapons Delivery: Low-Angle Dive / Strafing (10–20°)

Low-angle delivery is used for area suppression with rockets and for gun employment. Requires high-drag ordnance (Mk-82AIR/Snakeye) if bombs are employed.

| Parameter | Value |
| :--- | :--- |
| Dive Angle | 10° – 20° |
| Release Altitude | 500 – 1,500 ft AGL |
| Release Airspeed | 350 – 450 KIAS |
| Minimum Recovery Altitude | 300 ft AGL (high-drag ordnance only) |

**Gun Employment Ranges:**

| Platform | Open Fire (Max Effective) | Break-off (Minimum) |
| :--- | :--- | :--- |
| A-10C/II (GAU-8/A) — High Angle | 1.5 – 2.0 NM slant range | Pull off target |
| A-10C/II (GAU-8/A) — Low Angle | 0.8 – 1.2 NM slant range | Pull off by 0.5 NM |
| A-10A (GAU-8/A) | 1.5 NM slant range | Break by 0.5 NM |

> ⚠️ **SAFETY:** Do not commence strafing above 20° dive angle without switching to high-drag ordnance. Below 300 ft AGL, cease all weapons employment and execute immediate pull-up.

---

### 1.4 Aircraft-Specific Procedures — Phase 1

#### A-10C / A-10C II (High Fidelity)

> See also: [A-10C Checklist](../checklists/aircraft/a-10c.md) | [A-10C II Checklist](../checklists/aircraft/a-10c-ii.md)

**Pre-Attack DSMS Configuration:**
1. `DSMS` → Select weapon station(s).
2. Set **Ripple Quantity** and **Spacing** for multiple-bomb runs.
3. Confirm **Fuze** settings (Nose/Tail, Delay).
4. Ensure **Master Arm** → ARM.

**HUD Mode Selection:**
- `Master Mode Button (M)` — Cycle to **A-G** mode.
- **CCIP** → Visual dive delivery; pipper shows instantaneous impact point.
- **CCRP** → Designated point release; used for level and loft deliveries.

**CCIP Dive Attack Sequence:**
1. Designate target in CCIP (slew HUD if available).
2. Roll in; align CCIP pipper with target.
3. Depress and hold `WEAPON RELEASE (RAlt+Space)` — bomb releases when CCIP solution is valid.
4. Pull 4–5 g recovery.

**Strafing:**
1. Select **GUN** via HOTAS (`TDC Depress` or DSMS GUN select).
2. Confirm `EEGS` funnel displayed in HUD.
3. Fire: `Gun Trigger (Space)`.
4. Break off at 0.8 NM / 300 ft AGL minimum.

---

#### A-10A (FC3 — Simplified Avionics)

> See also: [A-10A Checklist](../checklists/aircraft/a-10a.md)

The A-10A uses a simplified avionics suite. No DSMS or TGP are available. All weapons delivery is visual/HUD only.

**Key Differences from A-10C:**
- No DSMS: Stores cycled with `D` key.
- Air-to-Ground mode: `7` key.
- Ripple: `LCtrl + Space`.
- No laser targeting capability (Mavericks use optical lock only).

**Dive Attack Sequence:**
1. Press `7` to enter A-G mode.
2. Press `D` to cycle to the desired weapon type.
3. Roll in to 30° dive. Align gunsight reticle with target.
4. Press `WEAPON RELEASE (RAlt+Space)` at release cue altitude.
5. Pull recovery.

**Strafing:**
1. Select GUN via `D` cycling.
2. Align pipper. Open fire at 1.5 NM. Break by 0.5 NM.

---

#### Su-25T (High Fidelity)

> See also: [Su-25T Checklist](../checklists/aircraft/su-25t.md)

**Pre-Attack Configuration:**
1. `LShift+Space` → **Master Arm ON**.
2. `7` → A-G Mode.
3. `RShift+O` → **Laser Rangefinder/Designator ON** (CRITICAL — weapons will not guide without this).
4. `D` → Cycle hardpoints to desired weapon station.

**Shkval TV System (Unguided/Rockets Phase 1):**
- For unguided rockets and gun employment, Shkval provides ranging and aiming cues.
- `O` → Uncage/activate Shkval.
- `+` / `-` → Zoom in/out.

**Dive Attack (Rockets/Bombs):**
1. Shallow dive, 10–20°.
2. Airspeed 400–500 km/h maintained throughout.
3. Align Shkval on target. Confirm ranging.
4. Release: `RAlt+Space`.

**Strafing (GSh-30-2):**
1. Select gun via `D`.
2. Align HUD reticle.
3. Fire: `Space`.

---

#### Su-25 (Standard — Visual Only)

> See also: [Su-25 Checklist](../checklists/aircraft/su-25.md)

The standard Su-25 uses the ASP-17 optical gunsight. No TV or laser systems are available for unguided delivery.

- All delivery is visual using the HUD/gunsight reticle.
- Recommended dive: 20–30°.
- `RShift+O` → Laser rangefinder (ranging only, not designation).
- Gun and rockets: align HUD reticle; release/fire at computed range.

---

### 1.5 Phase 1 — Practice Mission Profile

**Mission Name:** IRON ANVIL 01

| Parameter | Detail |
| :--- | :--- |
| **Time of Day** | Daytime (1000–1400 local) |
| **Weather** | CAVOK, visibility unrestricted, winds calm |
| **Threat Environment** | Low — MANPADS possible, no radar-guided SAMs |
| **Airfield** | Kutaisi (UGKO) or equivalent |
| **Target Area** | Pre-surveyed ground target range, soft-skinned vehicles |

**Student Objectives:**
1. Conduct pre-flight stores check and DSMS/simplified configuration.
2. Complete one (1) high-angle dive attack with Mk-82 (CCIP or visual).
3. Complete one (1) gun strafing pass on a designated target.
4. Complete one (1) rocket attack (low-angle, 10–15°).
5. Return to base with fuel above Bingo state.

**Success Criteria:**
- At least 1 of 2 Mk-82s impacts within 25 m of target.
- Strafing rounds observed on target or within 10 m.
- No safety violations (minimum altitude, frag clearance).
- Correct pre/post-attack brevity calls transmitted.

---

## Phase 2: Intermediate Surface Attack (Precision & Systems)

### Learning Objectives

Upon completion of Phase 2, the student will be able to:

1. Employ the A-10C Targeting Pod (TGP) to designate targets and employ laser-guided bombs.
2. Configure and fire the AGM-65 Maverick (all variants) using DSMS and TGP cuing.
3. Operate the Su-25T Shkval system to lock, track, and engage targets with the Vikhr laser beam rider missile.
4. Employ TV-guided weapons (Kh-29T / KAB-500Kr) from level flight.
5. Apply proper sensor management and multi-sensor coordination discipline.

---

### 2.1 A-10C / A-10C II — TGP & Laser-Guided Weapons

> See also: [A-10C Checklist](../checklists/aircraft/a-10c.md)

#### TGP Employment

The AN/AAQ-28 LITENING TGP provides targeting, laser designation, and IR/CCD imagery for all precision engagement.

**TGP Setup:**
1. `DSMS` → `INV` → Select laser weapon station → `LASER` → Set code to **1688** (or briefed code).
2. Slew TGP using TDC (Throttle Designator Control).
3. `TMS Up Short` → **Point Track** (locks onto a specific aim point).
4. `TMS Up Long` → **Area Track** (area/centroid tracking for moving targets).
5. `TMS Right Long` → **Set as SPI** (Sensor Point of Interest — slaves all sensors).

**CCRP Level Release (LGB):**
1. Select LGB station in DSMS. Confirm laser code match.
2. TGP in Point Track on target.
3. `Master Mode → CCRP`. Confirm SPI set.
4. Fly release cue on HUD. System releases automatically at computed point.
5. Laser fires automatically at computed lase time (or manual `Designate` as required).
6. LGB guides to spot. Do NOT manoeuvre excessively during terminal guidance.

**CCRP Parameters (LGB/JDAM):**

| Parameter | Value |
| :--- | :--- |
| Employment Altitude | 10,000 – 20,000 ft AGL |
| Airspeed | 250 – 300 KIAS |
| Laser Fire | 10–15 sec prior to impact |
| Lase Code | 1688 (default) or briefed |

---

#### AGM-65 Maverick Employment

**Setup:**
1. Load Mavericks in DSMS. Confirm seeker type (E = EO, D/G = IIR).
2. Select Maverick station. `Master Mode → MAVERICK`.
3. `China Hat Forward Long` → Slave all sensors to SPI (aligns Maverick seeker to TGP designate).

**Engagement Sequence:**
1. TGP designates target (Point Track, SPI set).
2. China Hat Forward Long → seeker slaved to SPI.
3. Confirm seeker gate on target in MFD.
4. `TMS Up Short` → Seeker lock.
5. Confirm lock tone. Check range within envelope.
6. Hold `WEAPON RELEASE (RAlt+Space)` to fire.
7. Transmit: *"Rifle"*. Monitor missile track in MFD.

---

### 2.2 A-10A — Maverick (Simplified)

> See also: [A-10A Checklist](../checklists/aircraft/a-10a.md)

The A-10A employs Mavericks using an optical boresight (no TGP slaving).

1. `D` → Cycle to Maverick station.
2. Maverick seeker bracket appears in HUD.
3. Slew bracket over target using hat switch.
4. `Enter` → Lock. Confirm lock tone.
5. `RAlt+Space` → Fire.
6. Transmit: *"Rifle"*.

> ⚠️ **Limitation:** No TGP slaving; all designation is manual boresight. Ensure target is clearly visible before lock attempt.

---

### 2.3 Su-25T — Shkval & Vikhr

> See also: [Su-25T Checklist](../checklists/aircraft/su-25t.md)

#### Shkval TV System Operation

The Shkval is a forward-looking TV/laser system that provides designation for the Vikhr anti-tank missile and Kh-29T/KAB-500Kr guided weapons.

**Activation:**
1. `LShift+Space` → Master Arm ON.
2. `7` → A-G Mode.
3. `RShift+O` → **Laser Designator ON** ← This step is critical and is commonly missed.
4. `O` → **Uncage Shkval**.

**Target Acquisition:**
1. `+` / `-` → Zoom to locate target.
2. Slew crosshair using hat switch.
3. `Enter` → Lock. The Shkval gate will follow the target.

#### Vikhr (AT-16) Laser Beam Rider

The 9A-4172 Vikhr is a supersonic laser beam rider. The missile flies along the laser beam — the aircraft must hold steady and maintain the lock until impact.

**Engagement Sequence:**
1. Shkval locked on target (gate tracking).
2. Confirm laser designator ON (`RShift+O`).
3. Select Vikhr via `D` cycle.
4. Dive angle: 10–20°. Airspeed: 400–500 km/h.
5. Confirm range (within envelope, typically < 8 km).
6. **Press and hold** `RAlt+Space` for approximately 1 second → Vikhr fires.
7. **Maintain steady flight and lock** throughout missile flight. Any break in beam will cause miss.
8. Transmit: *"Rifle"*.

> ⚠️ **CRITICAL:** Do NOT manoeuvre aggressively after Vikhr launch. The laser beam is fixed to the aircraft boresight — breaking the beam kills the missile guidance. Maintain wings-level or gentle bank only.

#### TV-Guided Weapons (Kh-29T / KAB-500Kr) — Level Delivery

1. Activate Shkval. Lock target.
2. Select Kh-29T or KAB-500Kr via `D`.
3. Fly level at 400–500 km/h.
4. Confirm Shkval locked. Release: `RAlt+Space`.
5. Transmit: *"Rifle"* (Kh-29T) or *"Pickle"* (KAB-500Kr).
6. Weapon guides autonomously post-release — may manoeuvre after release.

---

### 2.4 Su-25 — Semi-Active Laser Guided Missiles (Kh-25ML / Kh-29L)

> See also: [Su-25 Checklist](../checklists/aircraft/su-25.md)

1. `RShift+O` → Laser rangefinder/designator ON.
2. `D` → Cycle to Kh-25ML or Kh-29L.
3. In HUD, slew the designation reticle over target.
4. `Enter` → Lock.
5. **Maintain dive** throughout engagement — semi-active laser requires continuous illumination.
6. Release: `RAlt+Space`. Transmit: *"Rifle"*.
7. Hold dive angle and laser on until impact or seeker self-guidance confirmed.

---

### 2.5 Phase 2 — Practice Mission Profile

**Mission Name:** PRECISION STRIKE 02

| Parameter | Detail |
| :--- | :--- |
| **Time of Day** | Dawn or Dusk (transition lighting) |
| **Weather** | Scattered cloud at 8,000 ft, 15 km visibility |
| **Threat Environment** | Medium — radar-guided AAA possible, IR MANPADS likely |
| **Airfield** | Tbilisi (UGTB) or equivalent |
| **Target Area** | Armoured vehicle concentration, mixed hardened/soft targets |

**Student Objectives:**
1. Employ one (1) LGB or JDAM against a designated hardened target (A-10C/II only).
2. Employ one (1) Maverick against an armoured vehicle target.
3. Employ one (1) Vikhr against an armoured vehicle target (Su-25T only).
4. Maintain altitude deconfliction above threat envelope (above Angels 12 for ingress).

**Success Criteria:**
- LGB/JDAM: Direct hit or within 5 m CEP.
- Maverick/Vikhr: Target killed or mission-kill achieved.
- No break in Vikhr laser beam during flight.
- Correct brevity codes used for all weapons releases.
- Egress completed above minimum recovery altitude.

---

## Phase 3: Close Air Support (CAS) & JTAC Coordination

### Learning Objectives

Upon completion of Phase 3, the student will be able to:

1. Conduct a proper CAS check-in using the MNPOPCA format.
2. Receive, read back, and execute a 9-Line CAS brief.
3. Operate within a Keyhole CAS geometry, holding at assigned anchors.
4. Integrate with a JTAC for a full cleared-hot attack, including abort procedures.

---

### 3.1 CAS Check-In Format (MNPOPCA)

Upon entering the CAS area, the flight lead transmits check-in to the JTAC on the assigned TAD (Tactical Air Direction) frequency.

| # | Element | Example |
| :---: | :--- | :--- |
| 1 | **M**ission Number | "Mission Alpha Tango 41" |
| 2 | **N**umber & Type of Aircraft | "Two A-10C" |
| 3 | **P**osition & Altitude | "10 NM north, Angels 15" |
| 4 | **O**rdnance | "Four Mk-82, two Mavericks, full gun" |
| 5 | **P**laytime | "Forty-five minutes" |
| 6 | **C**apabilities | "Day, laser, TGP" |
| 7 | **A**bort Code | "Abort code: EAGLE" |

---

### 3.2 The 9-Line CAS Brief

The 9-Line is the standard format for passing target information from a JTAC to attacking aircraft. It must be read back in full for lines 4, 6, and any restrictions.

| Line | Element | Example |
| :---: | :--- | :--- |
| 1 | **IP/BP** (Initial Point / Battle Position) | "IP: BRIDGE" |
| 2 | **Heading** (from IP to target) | "Heading 230" |
| 3 | **Distance** (IP to target) | "4.5 NM" |
| 4 | **Target Elevation** (MSL) ← *Read back* | "Elevation 1,240 ft" |
| 5 | **Target Description** | "T-72 in the open" |
| 6 | **Target Coordinates** ← *Read back* | "41S MR 123 456" |
| 7 | **Mark Type** | "Smoke, colour red" |
| 8 | **Friendlies** (location relative to target) | "Friendlies 400 m north, marked IR strobe" |
| 9 | **Egress Direction** | "Egress west" |
| +  | **Restrictions / Remarks** ← *Read back if given* | "No ordnance north of Phase Line GREEN" |

> ✅ **READ BACK REQUIREMENT:** Lines **4**, **6**, and all **restrictions/remarks** must be read back verbatim. JTAC confirms: *"Read back correct."* Do not attack until confirmation received.

---

### 3.3 Keyhole CAS Geometry

The Keyhole is the preferred CAS stack geometry in high-threat environments. Aircraft hold at static anchor points and enter the attack corridor only when **Cleared Hot** by the JTAC/FAC-A.

```
                          N
                          |
                    [ALPHA / 360°]
                    Hold North
                   /            \
                  /              \
        [DELTA]---                ---[BRAVO]
        W / 270°    [TARGET/IP]    E / 090°
                  \              /
                   \            /
                    [CHARLIE / 180°]
                    Hold South
                          |
                          S

        [ECHO] = Overhead Hold (above target; FAC-A or stack top)
```

**Hold Commands:**
- `"Hold Alpha 10"` — Hold at North anchor, 10 NM from target, racetrack pattern.
- `"Hold Bravo 8"` — Hold at East anchor, 8 NM from target.

**Attack Commands:**
- `"Push from Alpha"` — Cleared to ingress from North anchor.
- `"Ingress Alpha, Egress Bravo"` — Attack from North, exit to East.

**Altitude Deconfliction:**

| Layer | Altitude | Occupant |
| :--- | :--- | :--- |
| CAS Stack | Angels 18 – 20 | Holding aircraft (transit/top) |
| FAC-A Working | Angels 14 – 15 | FAC-A platform |
| Attack / GTL Avoidance | Below Angels 12 | Attacking aircraft only — cleared hot |

> ⚠️ **Aircraft do NOT descend below Angels 12 until CLEARED HOT by JTAC/FAC-A.** Descend from hold altitude only on explicit attack clearance.

---

### 3.4 Full CAS Sequence (Student Execution)

1. **Arrive** at assigned anchor. Establish racetrack hold.
2. **Check in** with JTAC using MNPOPCA format.
3. **Receive 9-Line.** Copy all nine lines and restrictions.
4. **Read back** Lines 4, 6, and restrictions. Await confirmation.
5. **Confirm ordnance** configured, Master Arm armed.
6. Await **"Push from [Anchor]"** clearance.
7. Transmit: *"[Callsign] In from [Anchor]"* — JTAC acknowledges.
8. Acquire mark / target. Transmit: *"Tally"* (target) and/or *"Contact"* (mark).
9. Await **"Cleared Hot"**. If not received by minimum release point → **Abort**.
10. Employ weapons. Transmit: *"Pickle"* / *"Rifle"* / *"Guns Guns Guns"*.
11. Complete pass. Transmit: *"[Callsign] Off [Direction], BDA [assessment]"*.
12. Egress to directed anchor or exit point. Transmit: *"[Callsign] Egress [Direction]"*.

---

### 3.5 Abort Criteria

Abort the attack pass immediately if ANY of the following occur:

- **Cleared Hot** not received prior to minimum weapons release point.
- JTAC transmits **"Abort"** at any point.
- Target NOT positively identified before release point.
- Friendly positions NOT confirmed clear of attack corridor.
- Aircraft systems degraded (weapon malfunction, HUD failure, DSMS fault).

On abort: execute immediate wings-level pull-up, egress to directed anchor, transmit: *"[Callsign] Abort, [reason if known]"*.

---

### 3.6 Phase 3 — Practice Mission Profile

**Mission Name:** CLOSE FIGHT 03

| Parameter | Detail |
| :--- | :--- |
| **Time of Day** | Midday |
| **Weather** | Scattered cloud, 5,000 ft ceiling, 10 km visibility |
| **Threat Environment** | Medium-High — MANPADS, ZSU-23, possible radar SAM |
| **JTAC** | Ground JTAC (human or scripted AI) at contact position |
| **Target Area** | Enemy armoured element within 400 m of friendly positions |

**Student Objectives:**
1. Complete full CAS check-in (MNPOPCA format, all 7 elements).
2. Receive and accurately read back a full 9-Line brief.
3. Execute one (1) Cleared Hot attack from a Keyhole anchor.
4. Execute one (1) deliberate Abort when JTAC triggers the abort scenario.
5. Transmit accurate BDA after attack completion.

**Success Criteria:**
- MNPOPCA check-in complete, all elements present.
- 9-Line read-back: Lines 4, 6, and restrictions correct.
- Cleared Hot attack: Weapon employment within designated attack corridor.
- Abort executed correctly — no weapons released after abort call.
- BDA transmitted within 30 seconds of egress.

---

## Phase 4: Airborne Forward Air Controller (FAC-A)

### Learning Objectives

Upon completion of Phase 4, the student will be able to:

1. Establish and manage a Keyhole CAS stack with multiple attacking aircraft.
2. Conduct target marking using WP (Willy Pete) rockets and IR sparkle (night).
3. Execute a standard talk-on sequence to guide attacking aircraft onto target.
4. Apply Wedding Cake altitude deconfliction within a multi-ship CAS environment.
5. Issue 9-Line briefs and clearing authorities as the controlling FAC-A.

---

### 4.1 FAC-A Platform Notes

> See also: [UH-1H Huey Checklist](../checklists/aircraft/uh-1h-huey.md) (rotary-wing FAC-A)

The FAC-A role can be performed from:

| Platform | Notes |
| :--- | :--- |
| **A-10C / A-10C II** | TGP provides superior target designation; can self-lase while controlling |
| **A-10A** | Limited to visual marking and control; no TGP |
| **Su-25T** | Shkval provides FLIR/TV designation capability |
| **UH-1H Huey** | Low-altitude FAC-A; provides excellent slow-speed target identification; high vulnerability |

The FAC-A operates in the **working layer (Angels 14–15)** and does NOT attack targets while exercising FAC-A responsibilities unless in extremis.

---

### 4.2 Wedding Cake Altitude Deconfliction

The "Wedding Cake" separates transit, holding, and working aircraft by altitude band, preventing deconfliction conflicts in a dense CAS environment.

```
  ┌─────────────────────────────────────────────┐
  │  TOP LAYER:   Angels 20+                    │  Transit / Top Stack / Fuel
  ├─────────────────────────────────────────────┤
  │  MIDDLE LAYER: Angels 15–19                 │  CAS Stack Hold
  ├─────────────────────────────────────────────┤
  │  LOW LAYER:   Angels 5–14                   │  FAC-A Working / Attack
  └─────────────────────────────────────────────┘
                       ↑
              Below Angels 12: Cleared Hot attack zone
              Below Angels 5:  AAA / MANPADS envelope (avoid)
```

**Key Principle:** FAC-A operates at Angels 14–15. Attacking aircraft descend from their hold altitude through Angels 12 ONLY when Cleared Hot by FAC-A.

---

### 4.3 Stack Management Sequence

1. **Establish** working orbit at Angels 14–15 over or near the target area.
2. **Check-in** all aircraft: receive MNPOPCA from each flight. Assign anchor points and hold altitudes per the Keyhole diagram.
3. **Brief** the next attacking flight via 9-Line at their anchor. Await read-back confirmation.
4. **Sequence** attacks: one flight in the attack corridor at a time.
5. **Push** command: *"[Callsign], Push from [Anchor]."*
6. **Monitor** attack: confirm Tally/Contact calls, issue Cleared Hot only when positive ID established.
7. **Post-attack:** receive BDA, sequence next flight.
8. **Expedite** or hold traffic as battle rhythm dictates.

---

### 4.4 Marking Procedures

#### WP (White Phosphorus / Willy Pete) Marking

WP rockets are fired near the target to provide a visible smoke reference. The attacking pilot uses the smoke to orient onto the target.

**Procedure:**
1. FAC-A rolls in on the mark point (not the target — offset as appropriate).
2. Fire WP rocket.
3. Transmit: *"Mark is on deck."*
4. Attacker acknowledges: *"Contact the mark."*
5. FAC-A: *"Target is [X] metres [direction] from the mark."* (e.g., *"Target is 200 metres east of the mark."*)
6. Attacker: *"Tally"* when target acquired.
7. FAC-A: *"Cleared Hot."*

#### Sparkle (IR Laser Pointer — Night Operations)

Used with NVG-equipped attacking aircraft. The FAC-A illuminates the target with an IR laser pointer.

1. FAC-A: *"Sparkle ON."* Illuminates target with IR designator.
2. Attacker (on NVGs): *"Contact Sparkle."*
3. FAC-A may wiggle beam: *"Snake"* — confirms positive identification.
4. FAC-A: *"Cleared Hot."*

> ⚠️ **SAFETY — Sparkle:** Ensure attacking aircraft are confirmed on NVGs and have confirmed Contact Sparkle before issuing Cleared Hot. A missed Sparkle contact in a dense threat environment is grounds for abort.

---

### 4.5 Talk-On Procedure

Talk-On is used when marks are not available or practical. The FAC-A verbally guides the attacker from a large reference to the specific target using a four-step funnel.

```
ANCHOR  →  FUNNEL  →  REFERENCE  →  TARGET
 (Large)    (Medium)    (Local)      (Specific)
```

**Example Talk-On Sequence:**
1. **Anchor (Large Landmark):**
   *"Reference the main highway running east-west."*
2. **Funnel (Narrow to Area):**
   *"Follow the highway east to the T-junction."*
3. **Reference (Local Feature):**
   *"From the T-junction, 200 metres south, there is a large red barn."*
4. **Target (Specific Object):**
   *"Target is two T-72s in the treeline 50 metres west of the barn."*
5. Attacker: *"Tally"* (or: *"No Joy"* → FAC-A continues talk-on).
6. FAC-A: *"Confirm Tally?"* — Attacker: *"Tally, two tanks, treeline west of barn."*
7. FAC-A: *"That's correct. Cleared Hot."*

> ✅ **Best Practice:** Always confirm the attacker has the correct target by asking them to describe what they see before issuing Cleared Hot. Misidentification is the primary cause of fratricide.

---

### 4.6 Issuing the 9-Line as FAC-A

When acting as FAC-A, the student must brief the 9-Line **to** attacking aircraft, not receive it. All elements must be pre-planned before pushing aircraft from their anchor.

**Pre-Brief Checklist (FAC-A):**
- [ ] IP/BP confirmed and attacker is aware of its location.
- [ ] Heading from IP calculated.
- [ ] Distance from IP to target measured.
- [ ] Target elevation (MSL) confirmed from map/charts.
- [ ] Target description unambiguous.
- [ ] Target coordinates confirmed correct (MGRS or Lat/Long).
- [ ] Mark method available and ready.
- [ ] Friendly positions confirmed and communicated (grid or visual indicator).
- [ ] Egress direction deconflicted from friendly positions.
- [ ] Restrictions/ROE stated explicitly.

---

### 4.7 Phase 4 — Practice Mission Profile

**Mission Name:** IRON CONTROL 04

| Parameter | Detail |
| :--- | :--- |
| **Time of Day** | Night (NVG training environment) |
| **Weather** | Clear, unlimited visibility (night), winds calm |
| **Threat Environment** | Medium — MANPADS and radar AAA; SAM system suppressed but not destroyed |
| **FAC-A Platform** | A-10C (student) or UH-1H (alternative) |
| **Attack Aircraft** | Two-ship A-10C or Su-25T (AI or additional student) |

**Student Objectives (FAC-A):**
1. Check-in two attacking aircraft; assign Keyhole anchors.
2. Brief a complete 9-Line to each flight at their hold point.
3. Execute one (1) WP mark and control an attack to Cleared Hot.
4. Execute one (1) Sparkle mark (night) and control an attack to Cleared Hot.
5. Execute one (1) Talk-On sequence without marks.
6. Manage altitude deconfliction throughout; no altitude conflicts.
7. Receive and record BDA from each attacking flight.

**Success Criteria:**
- All check-ins received; anchors correctly assigned.
- 9-Lines complete and read-back confirmed for both flights.
- WP mark placed within 100 m of target. Attack Cleared Hot with correct attacker orientation.
- Sparkle mark confirmed Contact by attacker before Cleared Hot.
- Talk-On: attacker achieves Tally within 3 description steps.
- Zero altitude conflicts in stack.
- BDA received from all attacking flights.

---

## References

### Aircraft Checklists

| Platform | Checklist |
| :--- | :--- |
| A-10A (FC3) | [../aircraft/a-10a.md](../checklists/aircraft/a-10a.md) |
| A-10C Thunderbolt II | [../aircraft/a-10c.md](../checklists/aircraft/a-10c.md) |
| A-10C II Thunderbolt II | [../aircraft/a-10c-ii.md](../checklists/aircraft/a-10c-ii.md) |
| Su-25 Grach | [../aircraft/su-25.md](../checklists/aircraft/su-25.md) |
| Su-25T Frogfoot | [../aircraft/su-25t.md](../checklists/aircraft/su-25t.md) |
| UH-1H Huey (FAC-A) | [../aircraft/uh-1h-huey.md](../checklists/aircraft/uh-1h-huey.md) |

### Related Procedures

| Document | Link |
| :--- | :--- |
| 9-Line CAS Quick Reference | [./9-line-cas.md](../checklists/procedures/9-line-cas.md) |
| Radio Communications | [./radio-communications.md](../checklists/procedures/radio-communications.md) |
| Airfield ATC Communications | [./airfield-atc-communications.md](../checklists/procedures/airfield-atc-communications.md) |

### Doctrinal References

| Reference | Title |
| :--- | :--- |
| MCWP 3-23.1 | Close Air Support |
| JP 3-09.3 | Joint Procedures for Air Operations in Support of Land Forces |
| DTIC ADA429336 | FAC-A Doctrine and Procedures |

---

*End of Document — Basic and Intermediate Surface Attack Course*
