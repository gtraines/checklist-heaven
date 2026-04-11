# Event 2 — Weapons Management System & HUD Symbology

> **Course:** OH-58D Kiowa Warrior Weapons Employment Course | **Event Type:** Academics / Simulator
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — MFD Weapons Pages](#part-1--mfd-weapons-pages)
4. [Part 2 — Master Arm & Arming Sequence](#part-2--master-arm--arming-sequence)
5. [Part 3 — Emergency & Selective Jettison](#part-3--emergency--selective-jettison)
6. [Part 4 — HUD / MFD Weapons Symbology](#part-4--hud--mfd-weapons-symbology)
7. [Part 5 — Weapon System BIT & Status](#part-5--weapon-system-bit--status)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Navigate between MFD weapons pages and identify all display elements by name and function
- [ ] Select any weapon type directly using MFD OSBs and HOTAS weapon-cycle inputs
- [ ] Execute the complete Master Arm arming sequence from SAFE to a verified weapon-ready state
- [ ] Perform the de-arming sequence immediately after an engagement
- [ ] Describe the emergency jettison and selective jettison procedures and state when each is appropriate
- [ ] Interpret all HUD/MFD weapons symbology for Hellfire, rockets, APKWS, and gun
- [ ] Conduct a pre-flight weapon BIT and correctly interpret GO / NO-GO results
- [ ] State the correct procedure for a misfire, hangfire, and hung ordnance condition

> **Event Structure:** Academic and simulator. Part A is the ground brief covering all weapons page content and symbology. Part B places the student in a DCS hot-start with weapons loaded. The student navigates all weapons pages, practices the full arming/de-arming cycle with each weapon type selected, and demonstrates jettison knowledge. No weapons are fired in this event — that begins in Event 3.

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase A | Academic — MFD weapons page layout; weapon selection; arming sequence |
| Phase B | Academic — HUD/MFD symbology for each weapon type |
| Phase C | Simulator — navigate all weapons pages; select each weapon type; complete arm/de-arm cycle |
| Phase D | Simulator — weapon BIT; jettison procedure demonstration (instructor calls simulated emergency) |

### Key Concepts

| Concept | Value |
|---------|-------|
| Master Arm states | SAFE (default) and ARM (tactical) |
| Laser arm states | SAFE and ARMED (separate from Master Arm) |
| Weapon ready indication | **RDY** (ready to fire) / **NOT RDY** (constraint present) |
| Default PRF code | 1688 |
| Emergency jettison | All stores — both pylons — simultaneous |
| Selective jettison | Individual station or pylon via MFD weapons page |

---

## Part 1 — MFD Weapons Pages

The OH-58D does not use a centralized stores management system. Weapons are managed through dedicated **MFD pages** accessed via the Option Select Buttons (OSBs) on the MFD bezel.

### Weapons Page — Top-Level Overview

| Display Element | Description |
|----------------|-------------|
| **Selected Weapon** | Currently active weapon type: HF (Hellfire), RKT (Rockets), GUN (.50 cal), APKWS |
| **Weapon Inventory** | Per-station count of remaining weapons (e.g., "L: 2 HF / R: 7 RKT") |
| **Weapon Readiness** | RDY — ready to fire; NOT RDY — system constraint present |
| **Guidance Mode** *(Hellfire)* | LOBL / LOAL-DIR / LOAL-LO / LOAL-HI |
| **PRF Code** | Current laser code assigned to the weapon seeker |
| **Master Arm State** | SAFE / ARM indication |

### Weapon Selection

| Method | Action |
|--------|--------|
| **HOTAS weapon cycle** | Cycles through loaded weapons: HF → RKT → GUN → APKWS → repeat |
| **Direct OSB press** | Pressing the specific weapon OSB on the MFD jumps directly to that weapon |

> **Instructor Note:** Students must be able to select any weapon type directly without cycling through the full list. During a multi-target engagement, wasted time on weapon selection is time spent exposed in a hostile engagement area. Assign direct-select HOTAS bindings for all primary weapons before Event 3.

### Hellfire Sub-Page

| Element | Description |
|---------|-------------|
| **Missile Count** | Remaining missiles per pylon (left / right) |
| **Variant** | K / M / N — variant displayed per loaded missile |
| **Guidance Mode** | LOBL / LOAL-DIR / LOAL-LO / LOAL-HI — selectable via OSB |
| **PRF Code** | 4-digit code; editable via MFD OSB; must match MMS laser code |
| **Seeker Status** | TRACKING / NO TRACK / LOCK — SAL seeker acquisition state (LOBL mode) |
| **Constraints** | In-range / out-of-range indication; launch acceptability region active |

### Rocket Sub-Page

| Element | Description |
|---------|-------------|
| **Rocket Count** | Remaining rockets per pod |
| **Warhead Type** | Auto-detected from loadout: M151 HE, M229 HE, M282 MPP, M156 WP, M257/M278 Illum |
| **Quantity per Salvo** | Selectable: 1, 2, 4, 7 (full pod) |
| **CCIP Data** | Current impact point range; CCIP status |
| **APKWS Mode** *(if APKWS loaded)* | Laser-guided mode active; PRF code displayed |

### Gun Sub-Page

| Element | Description |
|---------|-------------|
| **Round Count** | Remaining .50 caliber ammunition |
| **Rate** | Fixed ~1,100 RPM — not pilot-selectable |
| **CCIP Data** | Pipper position; slant range to computed ground impact |

---

## Part 2 — Master Arm & Arming Sequence

### Master Arm Switch

| Position | State | Effect |
|----------|-------|--------|
| **SAFE** | Weapons safed | No weapon can fire regardless of any other switch position; default for all non-tactical flight |
| **ARM** | Weapons armed | Selected weapon is hot; trigger/pickle will fire if weapon-specific constraints are met |

**Location in DCS:** Master Arm switch is located on the armament panel — consult the Polychop OH-58D manual for precise cockpit location. Verify the switch position is displayed on the MFD weapons page.

### Complete Arming Sequence

Execute this sequence before every engagement:

| Step | Action | Verification |
|------|--------|--------------|
| 1 | **Master Arm → ARM** | MASTER ARM indication on MFD; caution panel armed state |
| 2 | **Select weapon type** on MFD or HOTAS | Weapon type displayed; inventory confirmed |
| 3 | **Select guidance mode** (Hellfire) **or quantity** (rockets) | Mode/quantity shown on sub-page |
| 4 | **Verify PRF code** *(laser weapons)* | PRF code matches briefed code; matches MMS laser code |
| 5 | **Arm laser** *(laser-guided weapons)* | LASER ARMED indication on MFD |
| 6 | **Confirm RDY** | RDY indication on MFD weapons page |
| 7 | **Confirm in-envelope** | Range, altitude, and airspeed within weapon parameters |
| 8 | **Fire / Pickle** | Weapon fires/launches |

> **Verbal Cadence:** Develop a consistent pre-engagement verbal checklist. A common format:
> *"Master Arm — ARM. Weapon — [type]. Mode — [LOBL/RKT/GUN]. Code — [PRF]. Laser — ARM. Ready. Cleared hot."*
> Consistency prevents missed steps under stress.

### De-Arming Sequence

Execute immediately after every engagement:

| Step | Action | Notes |
|------|--------|-------|
| 1 | Cease fire; release trigger/pickle | — |
| 2 | **Laser → SAFE** *(if armed)* | Prevents inadvertent lasing during egress or repositioning |
| 3 | **Master Arm → SAFE** | Weapons safed; prevents sympathetic fire |
| 4 | Verify SAFE indications on MFD | Confirm all weapon pages show SAFE state |

> **Instructor Note:** Master Arm must return to SAFE during all transit, repositioning, hover-hold, and non-engagement phases. ARM only when commencing an attack. This discipline is non-negotiable — an armed aircraft during an unintended HOTAS press or turbulence encounter can fire unintentionally.

---

## Part 3 — Emergency & Selective Jettison

### Emergency Jettison

| Item | Detail |
|------|--------|
| **Purpose** | Immediately shed all external stores for maximum weight reduction |
| **Control** | Emergency jettison button — guarded, typically red, on armament panel |
| **Action** | Lift guard → press; releases all stores from both pylons simultaneously |
| **Effect** | Both pylons cleared; aircraft at minimum weight for maximum climb/maneuver performance |

**When to use emergency jettison:**
- Single-engine emergency requiring immediate weight reduction to maintain flight
- Combat egress requiring maximum performance (enemy pursuit, MANPADS track)
- Aircraft in uncontrolled state where weapons drag is preventing recovery

### Selective Jettison

| Item | Detail |
|------|--------|
| **Purpose** | Drop specific stores from one pylon for weight management or hung ordnance |
| **Control** | Select station on MFD weapons page → jettison OSB |
| **When to use** | Hung missile (will not fire, cannot be safed); asymmetric load balance after partial expenditure; controlled weight reduction |

> *⚠ Realism Divergence: Real-world jettison involves specific arming-wire safety considerations and circuit breaker checks before selective jettison of unexpended ordnance. DCS simplifies jettison to a button press with immediate store separation. The emergency jettison button concept is identical, but the real-world safety interlocks and confirmation procedures are not fully modeled.*

> **Briefing Note:** Emergency jettison is a simulated procedure in DCS — the instructor will call the scenario ("Engine failure — you're losing power"). The student must demonstrate the correct response (emergency jettison if power is critically low) without coaching.

---

## Part 4 — HUD / MFD Weapons Symbology

The OH-58D displays weapons symbology primarily on the **MFD** (overlaid on MMS video or on a dedicated weapons page) rather than a traditional fighter HUD. Students must be able to interpret this symbology without hesitation during tactical operations.

### Hellfire Symbology

| Symbol | Meaning |
|--------|---------|
| **Crosshair (MMS)** | Laser aim point; center of MMS field of view |
| **Lock Diamond / Box** | Appears around target when SAL seeker detects reflected laser energy (LOBL mode) |
| **LOCK / TRK indication** | Seeker is tracking laser reflection; missile is ready to guide |
| **NO TRK** | Seeker cannot see the laser; check: laser armed and firing, PRF code match, range within envelope, unobstructed LOS |
| **Mode annunciation** | LOBL / LOAL-DIR / LOAL-LO / LOAL-HI displayed on weapons page |
| **Launch Acceptability Region** | Indicates whether current range and geometry support a valid launch |
| **MSL AWAY** | Confirms missile has left the rail |

### Rocket / APKWS Symbology

| Symbol | Meaning |
|--------|---------|
| **CCIP Reticle ("I-Beam")** | Continuously computed impact point; shows where rockets/APKWS will impact given current aircraft state |
| **Pipper Movement** | Pipper shifts dynamically with attitude, airspeed, and altitude changes |
| **Range Readout** | Slant range from aircraft to computed impact point |
| **Quantity Indicator** | Number of rockets in the next salvo |
| **APKWS Laser Overlay** | Additional symbology showing PRF code and laser status when APKWS is selected |

### Gun (.50 Cal) Symbology

| Symbol | Meaning |
|--------|---------|
| **CCIP Pipper** | Computed bullet impact point accounting for range, airspeed, bullet drop, and wind |
| **Bullet Stream Line** | Predicted trajectory of the bullet stream from aircraft to ground |
| **Range Readout** | Slant range to ground impact |
| **Round Count** | Remaining ammunition |

### Common Symbology Elements

| Symbol | Meaning |
|--------|---------|
| **MASTER ARM** | ARM indication visible when Master Arm is in the armed position |
| **WEAPON TYPE** | Active weapon annunciator: HF / RKT / GUN / APKWS |
| **RDY / NOT RDY** | Weapon readiness for selected type |
| **ROUNDS / QTY** | Ammunition or weapon count remaining |

### Interpreting "NOT RDY"

When the weapons page shows NOT RDY, do not attempt to fire. Diagnose the cause:

| Possible Cause | Check |
|---------------|-------|
| Master Arm in SAFE | Verify Master Arm switch position; look for ARM indication on MFD |
| Laser not armed *(laser weapons)* | Verify LASER ARMED indication |
| PRF code mismatch | Verify PRF code on weapons page matches MMS page |
| Out of envelope (range/altitude/speed) | Check range via LRF; confirm aircraft position |
| Weapon malfunction or feed issue | BIT; attempt alternate weapon station; report to maintenance |

---

## Part 5 — Weapon System BIT & Status

### Pre-Flight Weapon BIT

Conduct before committing to an engagement. Identifies system faults before the tactical requirement arises.

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Access BIT page on MFD | BIT options displayed per weapon type |
| 2 | Initiate **Hellfire BIT** | Missile status: GO / NO-GO per rail; seeker self-test |
| 3 | Initiate **Rocket system BIT** | Launcher circuitry check; continuity verification |
| 4 | Initiate **Gun BIT** | Feed system and trigger circuit check |
| 5 | Review BIT summary | All weapons GO → proceed to mission. Any NO-GO → troubleshoot or accept reduced capability and brief the limitation. |

### Misfire, Hangfire & Hung Ordnance Procedures

> *⚠ Realism Divergence: DCS does not model hangfire conditions (delayed ignition with ordnance on the rail). The real-world hangfire is a significant safety hazard requiring strict time-delay procedures and special handling. In DCS, students should understand these procedures for doctrinal awareness, but the simulator will not generate this specific failure.*

| Condition | Indication | Procedure |
|-----------|-----------|-----------|
| **Misfire** | Trigger/pickle pressed; no launch indication; weapon did not fire | Wait a minimum safe interval (~5 seconds); re-attempt once. If second attempt fails: safe the weapon; select alternate weapon or station; report condition to lead |
| **Hangfire** | Partial launch indication or delayed ignition suspected | Do NOT re-fire; maintain current aircraft heading clear of friendlies; wait minimum safe interval; report; proceed to a safe area; treat as live ordnance on the rail |
| **Hung Ordnance** | Weapon remains on the rail/launcher after fire command; launch indication absent | Safe Master Arm; select alternate weapon or station; report hung ordnance; attempt selective jettison only if tactically appropriate (jettising unexpended ordnance into friendly areas is not authorized); land with hung ordnance and follow EOD procedures |

---

## Completion Standards

The student passes this event when they can, without instructor prompting:

- [ ] Navigate to each weapon sub-page (Hellfire, Rockets, Gun, APKWS) via MFD OSB within 5 seconds per selection
- [ ] Select any specific weapon type directly (not by cycling) from HOTAS or MFD; state the weapon type, variant, and inventory count visible on the sub-page
- [ ] Execute the complete arming sequence from SAFE to RDY for each weapon type, reciting each step verbally as a checklist
- [ ] De-arm the system (Laser → SAFE, Master Arm → SAFE) and verify SAFE indications on MFD within 5 seconds of ceasing fire
- [ ] Set a new PRF code on the MFD weapons page when directed by the instructor
- [ ] Identify and correctly interpret all symbology elements listed in Part 4 when the instructor calls out a symbol by its visual description
- [ ] Explain the meaning of NOT RDY and diagnose at least three possible causes
- [ ] Complete a weapon BIT and correctly interpret the GO / NO-GO result
- [ ] Demonstrate knowledge of emergency jettison location and procedure; state the conditions under which it is appropriate
- [ ] Verbally brief the correct procedure for a misfire and a hung ordnance condition

---

## Common Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Forgetting Master Arm before engagement | Trigger/pickle press has no effect; wasted engagement opportunity; target escapes or returns fire | Make "MASTER ARM — ARM" a verbal callout before every engagement; verify ARM annunciation before committing |
| Selecting wrong weapon type | Fires rockets when Hellfire intended (or vice versa); wrong effect on target | Confirm weapon type on MFD sub-page before pressing fire; use direct-select bindings |
| Not verifying PRF code before firing laser-guided weapon | Weapon seeker on different code than laser; missile/rocket does not guide | PRF code verification is mandatory in arming sequence — check every engagement, every time |
| Leaving Master Arm in ARM during repositioning | Risk of sympathetic fire during turbulence or inadvertent trigger press | SAFE immediately after each engagement; verify SAFE annunciation; never transit between BPs with ARM active |
| Ignoring NOT RDY and pressing fire anyway | No weapon fires; student confused and wasting time in the engagement zone | Respect NOT RDY — it means a constraint exists. Diagnose and resolve before re-attempting |
| Not checking weapon inventory before committing to an engagement | Discovers Winchester (out of ammo) at worst possible moment | Brief loadout during pre-mission; check sub-page inventory before each engagement; track expenditures mentally |
| Cycling through weapons (rather than direct-select) during engagement | 3–5 seconds of fumbling; exposure time wasted; target may have moved or fired | Configure direct-select HOTAS bindings; practice weapon selection until it is muscle memory |

---

*Based on TM 1-1520-248-10, Polychop Simulations DCS OH-58D documentation. For simulation use only.*
