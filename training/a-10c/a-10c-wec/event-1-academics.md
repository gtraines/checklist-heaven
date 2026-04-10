# Event 1 — Weapons Systems Academics

> **Course:** A-10C Weapons Employment Course | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [A-10C vs. A-10A — Weapons Architecture Differences](#a-10c-vs-a-10a--weapons-architecture-differences)
3. [AHCP — Armament HUD Control Panel](#ahcp--armament-hud-control-panel)
4. [DSMS — Digital Stores Management System](#dsms--digital-stores-management-system)
5. [IFFCC — Delivery Modes](#iffcc--delivery-modes)
6. [HUD Weapons Symbology](#hud-weapons-symbology)
7. [Weapons Systems Overview](#weapons-systems-overview)
8. [Weapons Safety Rules](#weapons-safety-rules)
9. [Pre-Flight Weapons Setup Sequence](#pre-flight-weapons-setup-sequence)
10. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Explain the key weapons-related differences between the A-10A (FC3) and A-10C (full-fidelity) modules
- [ ] Locate and identify all AHCP switches, state their positions, and explain the consequences of incorrect arming
- [ ] Navigate the DSMS STATUS, INV, PROF, and UTIL pages to configure any weapon type
- [ ] Explain the CCIP and CCRP delivery modes: what each computes, when each is used, and how the HUD differs
- [ ] Describe DTOS and MAN delivery modes and when they apply
- [ ] Identify all major HUD weapons symbology elements for gun, bombs, Maverick, and JDAM
- [ ] State the effective employment parameters (range, altitude, mode) for each weapon system in the course
- [ ] Recite the five Weapons Safety Rules from memory

---

## A-10C vs. A-10A — Weapons Architecture Differences

The A-10A (FC3) uses simplified systems — weapons cycle with the `D` key, delivery modes are limited to CCIP/CCRP, and there is no targeting pod. The A-10C replaces this with a **full avionics weapons suite**:

| System | A-10A (FC3) | A-10C (Full Fidelity) | Impact |
|---|---|---|---|
| **Weapons Selection** | `D` key cycles stores | DSMS MFD page — select station and weapon type | Requires heads-in cockpit time |
| **Delivery Mode** | CCIP or CCRP only | CCIP, CCRP, DTOS, MAN, + weapon-specific modes | More options; more setup required |
| **Fuze Control** | Not modeled | NOSE / TAIL / N+T × INST / DLY / PRX | Incorrect fuze = weapon malfunction |
| **Targeting Pod** | Pave Penny (LST only — cannot self-designate) | Litening AT or Sniper XR (full FLIR/CCD/laser) | A-10C can self-lase; creates whole new weapon categories |
| **Maverick Cueing** | Direct seeker control only | TGP SPI → Maverick cueing for hands-off designation | Much faster kill chain |
| **GPS Weapons** | Not available | GBU-38/31 JDAM, GBU-39 SDB (A-10C II) | New weapon categories; coordinate-based targeting |
| **Self-Defense** | No RWR integration | ALR-69 RWR + CMSP + ALE-47 + ECM pod | Full defensive suite |
| **HMCS** | Not available | Scorpion HMCS (A-10C II) | Look-and-designate — dramatic workflow change |

**Bottom line:** The A-10C is not just "more buttons" — it represents a fundamentally different targeting architecture. The TGP and DSMS enable weapon types and delivery techniques that simply do not exist on the A-10A.

---

## AHCP — Armament HUD Control Panel

The AHCP is located on the **glareshield, left side**. It is the master weapons control panel — nothing can be released without correct AHCP configuration.

| Switch | Positions | Function |
|---|---|---|
| **MASTER ARM** | SAFE / ARM / TRAIN | **SAFE:** no weapons can release. **ARM:** weapons hot — ready for delivery. **TRAIN:** HUD symbology active, no actual release. |
| **GUN/PAC** | SAFE / ARM / GUNARM | Arms the GAU-8/A cannon. **GUNARM** = PAC (Precision Attitude Control) aiming + gun simultaneously. |
| **LASER ARM** | SAFE / ARM | Arms the TGP laser designator. **Required** for all laser-guided weapons (LGBs, APKWS, AGM-65L, LJDAM). |
| **TGP** | OFF / ON | Powers the Targeting Pod (Litening/Sniper). TGP takes 1–3 minutes to initialize. Power on early in the mission. |
| **IFFCC** | OFF / ON / TEST | Powers the IFFCC delivery computer. **Must be ON** for CCIP/CCRP to function. |
| **EMERG JETT** | Button (guarded) | Emergency jettison — releases **all** stores instantly. Last resort only — cannot be undone. |

#### Standard Pre-Attack Arming Sequence

| Step | Action |
|---|---|
| 1 | Verify **safe environment** — target area clear of friendlies |
| 2 | **MASTER ARM** → ARM |
| 3 | **GUN/PAC** → ARM (if employing gun) |
| 4 | **LASER ARM** → ARM (if employing laser-guided weapons or TGP designation) |
| 5 | Confirm weapon selected on DSMS |
| 6 | Confirm delivery mode set on DSMS PROF page |
| 7 | Verify HUD symbology is active for selected weapon |

#### Post-Attack Safe Sequence (Required)

| Step | Action |
|---|---|
| 1 | After last pass or after egress from target area |
| 2 | **LASER ARM** → SAFE |
| 3 | **GUN/PAC** → SAFE |
| 4 | **MASTER ARM** → SAFE |

> **Master Arm Discipline:** ARM only over the target area. SAFE immediately on egress. This is a non-negotiable habit — it prevents negligent weapon release and is a graded item on the Check Ride.

---

## DSMS — Digital Stores Management System

The DSMS is the A-10C's weapons management computer, displayed on either MFCD.

### Accessing the DSMS

On either MFCD (left or right):
- Press the **DSMS** OSB (Option Select Button) — typically in the bottom row of OSBs.
- The DSMS STATUS page appears.

### DSMS Page Hierarchy

| Page | Function | Access |
|---|---|---|
| **STATUS** | All stations (1–11) — weapon type, quantity, readiness at a glance | Default DSMS entry |
| **INV** (Inventory) | Per-station detail — fuze status, arming wire, exact quantity | OSB from STATUS |
| **PROF** (Profile) | Delivery profile setup — mode, fuze, ripple, escape maneuver | OSB from STATUS |
| **UTIL** (Utility) | Jettison options, station inhibit, special functions | OSB from STATUS |

### Station Layout (A-10C)

```
Station:  1   2   3   4   5   6   7   8   9   10  11
          LAL LAO LI  LO  LF  CTR RF  RO  RI  RAO RAL
          (Left Aft-Left ... Centerline ... Right Aft-Left)
```
- Station 6 (centerline) typically carries the ECM pod (ALQ-131/184) if loaded.
- Stations 3 and 9 can carry 600-gallon external tanks.
- The cannon (GAU-8/A) is integral — not a pylon-mounted station.

### PROF Page — Delivery Profile Configuration

| Parameter | Options | Notes |
|---|---|---|
| **Delivery Mode** | CCIP / CCRP / MAN / DTOS | JDAM: CCRP only. LGB: CCRP preferred. Rockets/gun: CCIP. |
| **Fuze** | NOSE / TAIL / N+T | Selects which fuze activates |
| **Fuze Function** | INST / DLY1 / DLY2 / PRX | INST = instantaneous; DLY = delay (short/long); PRX = proximity |
| **Release Qty** | SGL / PRS / RPL | Single, pairs, ripple |
| **Ripple Count** | 2–20 | Weapons per ripple press |
| **Ripple Interval** | 25–500 ft | Spacing between releases |
| **Arming Delay (AD)** | 0–99.9 sec | Time before fuze arms after release — **critical for low-altitude delivery** |
| **Escape Maneuver** | NONE / CLM / TRN / LTRN | Post-release egress cue on HUD |

> **Fuze Rule:** Always verify fuze before beginning a delivery. An incorrectly set fuze (e.g., NOSE DLY on a building strafing pass instead of NOSE INST) can result in weapon failure or excessive blast risk.

### Station Priority and Selection

- DSMS automatically sequences stations in a configured priority (outboard-to-inboard, alternating left/right is typical).
- The pilot can manually override station selection on the INV page.
- When a station is depleted, DSMS advances to the next loaded station automatically.

### Jettison

| Method | Action | Use |
|---|---|---|
| **Selective Jettison** | DSMS UTIL → station → JETT | Drop specific stores for drag reduction or asymmetric load |
| **Emergency Jettison** | EMERG JETT button (AHCP) | ALL stores released instantly — combat emergency only |

---

## IFFCC — Delivery Modes

The IFFCC (Integrated Flight & Fire Control Computer) computes weapon delivery solutions and drives HUD symbology.

### CCIP — Continuously Computed Impact Point

- The IFFCC continuously calculates where the weapon would impact if released **right now**.
- A **pipper** (circle with dot) is displayed on the HUD, placed at the real-time ground impact point.
- The pilot flies to place the pipper on the target, then pickles.
- **Best for:** Diving attacks, visual acquisition, gun and rockets, low-drag bombs.

| Weapon Type | CCIP Pipper Behavior |
|---|---|
| Bombs | Pipper moves down BFL as dive increases; rises as aircraft climbs |
| Rockets | Similar to bombs; faster movement due to rocket ballistics |
| Gun (PAC-1) | Stabilized reticle — IFFCC compensates for aircraft motion |

**Minimum Release Altitude caret:** A small caret on the Bomb Fall Line marks the minimum safe release altitude. **Never release below this caret.** Below it, fragmentation or ricochet debris can damage the aircraft.

### CCRP — Continuously Computed Release Point

- The IFFCC computes the future release point in space where the weapon must leave the aircraft to hit a **pre-designated target (SPI)**.
- **Auto-release:** Hold the pickle button; the system releases the weapon automatically at the computed point.
- **Best for:** Level delivery, medium-altitude, GPS/laser-guided weapons, any target with a known position (SPI).

| CCRP HUD Element | Meaning |
|---|---|
| **Azimuth Steering Line** | Vertical line — center it on the FPM to fly the correct ground track |
| **Range Bar** | Horizontal bar descending toward FPM — represents time/distance remaining |
| **Solution Circle** | Circle around FPM — valid release solution exists |
| **Pull-Up Cue** (`X`) | If displayed, pull up immediately to achieve valid parameters |
| **Time-to-Release** | Digital countdown in seconds |
| **Auto-Release** | Range bar reaches FPM → weapon releases (pickle must be held) |

### DTOS — Dive Toss

- Pilot designates target via TGP or manual designation while diving, then **pulls into a climb**.
- IFFCC computes a release point **during the climb arc** — the weapon is "tossed" toward the target.
- Provides **increased standoff** compared to standard diving delivery.
- Used against heavily defended targets where a prolonged dive is dangerous.
- HUD shows CCRP-like steering cues accounting for the loft trajectory.

### MAN — Manual Delivery

- No computer assistance — pilot uses fixed HUD references and experience.
- Backup mode only — used if IFFCC fails.
- Rarely required in normal DCS operations.

---

## HUD Weapons Symbology

### Gun Symbology

| Element | Description |
|---|---|
| **Gun Cross** | Fixed cross — boresight of GAU-8/A barrel |
| **PAC Reticle (PAC-1)** | Stabilized aiming point — compensates for aircraft motion; place on target |
| **Rounds Remaining** | Digital counter at bottom of HUD |
| **Gun Funnel (PAC-3)** | Two converging lines for air-to-air lead computation |

### Bomb Symbology — CCIP

| Element | Description |
|---|---|
| **FPM** (Flight Path Marker) | Where the aircraft is going — reference for pipper relationship |
| **Bomb Fall Line (BFL)** | Vertical line from FPM downward — weapon trajectory track |
| **CCIP Pipper** | Circle on BFL — real-time ground impact point |
| **MIN RNG Caret** | Caret on BFL — minimum safe release altitude. Do NOT release below. |

### Bomb Symbology — CCRP

| Element | Description |
|---|---|
| **Azimuth Steering Line** | Vertical line to center on FPM |
| **Range Bar** | Horizontal line descending to FPM — time to release |
| **Solution Circle** | Circle around FPM when release solution is valid |
| **Auto-Release Point** | Moment range bar meets FPM — weapon releases if pickle held |
| **TT-Release** | Time-to-release countdown (digital, seconds) |

### Maverick Symbology

| Element | Description |
|---|---|
| **Boresight Cross** | Where the Maverick seeker is pointed |
| **Seeker Gate** | Box showing seeker's current tracking window |
| **Lock Diamond** | Diamond = seeker is tracking; no diamond = searching |
| **RDY** | MFCD "RDY" = missile ready to fire |
| **SHOOT** | Cue appears when within valid launch envelope |

### JDAM Symbology (CCRP)

| Element | Description |
|---|---|
| **Azimuth Steering Line** | Same as bomb CCRP — fly to center |
| **TT-Release** | Time-to-release countdown |
| **Solution Cue** | GPS solution valid |
| **In-Zone/Out-of-Zone** | Launch zone boundary indication |

---

## Weapons Systems Overview

*This is a survey — detailed employment is covered in Events 2–7.*

| Weapon | Event Covered | Key Concept |
|---|---|---|
| GAU-8/A Avenger | Event 2 | Short bursts; PAC-1 stabilized pipper; manage recoil |
| Hydra 70 Rockets | Event 2 | CCIP diving attack; 7 or 19 tube launchers |
| Mk-82 / Mk-84 Slick | Event 3 | CCIP (dive) and CCRP (level); fuze and AD critical |
| Mk-82AIR / Snakeye | Event 3 | High-drag; safe for low-altitude; arming delay |
| CBU-87 / CBU-97 | Event 3 | Cluster munitions; HOF programming; altitude-sensitive |
| WCMD CBU-103/105 | Event 3 | Wind-corrected delivery; GPS-aided standoff |
| TGP (Litening/Sniper) | Event 4 | POINT/AREA track; laser designation; SPI control |
| AGM-65 Maverick | Event 4 | TGP SPI cueing; IR vs. EO-TV; fire-and-forget |
| GBU-12 / GBU-10 LGB | Event 5 | Self-lase with TGP; buddy lase; laser timing |
| GBU-38 / GBU-31 JDAM | Event 6 | GPS/INS; coordinate-based; TOO vs. PP; fire-and-forget |
| APKWS *(A-10C II)* | Event 7 | Laser-guided rocket; CCIP + TGP laser; short range, high precision |
| GBU-39 SDB *(A-10C II)* | Event 7 | Glide bomb; up to 40 nm standoff; 4 per rack |
| GBU-54 LJDAM *(A-10C II)* | Event 7 | GPS + laser hybrid; moving target capable |
| HMCS *(A-10C II)* | Event 7 | Look-and-designate; sensor slew; SPI integration |
| AIM-9M Sidewinder | Event 7 | Self-defense only; seeker tone; HMCS cueing (A-10C II) |
| CMSP / ALE-47 / ECM | Event 7 | Layered defense; program selection; threat-specific reactions |

---

## Weapons Safety Rules

These five rules are **non-negotiable**. A violation of any one results in an automatic DOWN on any graded event.

| Rule | Statement |
|---|---|
| **Rule 1** | Master Arm stays **SAFE** until inside the target area and ready to deliver |
| **Rule 2** | **Identify your target** before releasing. No firing into uncleared areas. Positive ID required. |
| **Rule 3** | **Minimum altitudes are hard floors.** Never release below the MIN RNG caret or published minimum |
| **Rule 4** | **Safe the Master Arm immediately** on egress from the target area. Do not RTB with a hot jet. |
| **Rule 5** | **Emergency Jettison is last resort.** Call "JETTISON" on frequency. Used only when flight safety requires immediate store removal. |

---

## Pre-Flight Weapons Setup Sequence

This is the standard cockpit weapons setup sequence performed before every sortie. Memorize it before Event 2.

| Step | Action | Verify |
|---|---|---|
| 1 | **AHCP** → MASTER ARM SAFE | Confirm SAFE — no releases possible |
| 2 | **AHCP** → TGP ON | TGP powers up (1–3 min warmup) |
| 3 | **AHCP** → IFFCC ON | IFFCC initializes (~30 sec) |
| 4 | **DSMS** → STATUS page | Verify stations loaded match mission loadout |
| 5 | **DSMS** → INV | Check each station: weapon type, fuze installed |
| 6 | **DSMS** → PROF | Set delivery mode, fuze, ripple, AD for primary weapon |
| 7 | **TGP** → verify on MFCD | Confirm TGP image active; set laser code |
| 8 | **Arming Area** | Ground crew performs physical arming (remove safety pins) — DCS: taxi through arming area or use ATIS |
| 9 | **CMSP** → MAN or SEMI | Verify chaff/flare programs set; RWR on |
| 10 | Confirm Master Arm **SAFE** for takeoff | ARM only when ready to deliver |

---

## Completion Standards

This is an academic event. All items must be answered correctly without reference to notes.

- [ ] **Q1:** Name the three MASTER ARM positions and what each allows. *(SAFE: no release; ARM: weapons hot; TRAIN: symbology only, no release)*
- [ ] **Q2:** What does GUNARM on the GUN/PAC switch do that ARM alone does not? *(Enables PAC — Precision Attitude Control — simultaneously with arming the cannon)*
- [ ] **Q3:** What does LASER ARM arm, and which weapons require it? *(Arms TGP laser designator; required for LGBs, APKWS, AGM-65L, LJDAM)*
- [ ] **Q4:** On the DSMS PROF page, what is Arming Delay (AD), and when is it critical? *(Time before fuze arms after release; critical for low-altitude delivery to prevent premature detonation)*
- [ ] **Q5:** Explain CCIP in one sentence. *(Continuously Computed Impact Point — the HUD shows where the weapon hits right now; pilot places pipper on target and pickles)*
- [ ] **Q6:** Explain CCRP in one sentence. *(Continuously Computed Release Point — system computes future release point for a designated target SPI; auto-releases when parameters are met)*
- [ ] **Q7:** What does the MIN RNG caret on the bomb fall line indicate? *(Minimum safe release altitude — releasing below this risks aircraft damage from fragmentation or ricochet)*
- [ ] **Q8:** What must happen for CCRP auto-release to work? *(The pickle button must be held through the auto-release point; releasing pickle before that point aborts the release)*
- [ ] **Q9:** Describe the standard pre-attack arming sequence in order. *(Master Arm ARM → GUN/PAC ARM if gun → LASER ARM ARM if laser → confirm DSMS selection → confirm mode → verify HUD)*
- [ ] **Q10:** Recite the five Weapons Safety Rules. *(Safe until target area; identify before release; minimum altitudes are hard floors; safe immediately on egress; emergency jettison is last resort)*

---

[→ Proceed to Event 2: GAU-8/A Gun & Rockets](event-2-guns-rockets.md)

---

*Based on T.O. 1A-10C-34-1-1, T.O. 1A-10C-1, and Eagle Dynamics DCS A-10C/II documentation. For simulation use only.*
