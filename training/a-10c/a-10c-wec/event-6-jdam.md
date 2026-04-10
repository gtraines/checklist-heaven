# Event 6 — JDAM & GPS-Guided Weapons (GBU-38 / GBU-31)

> **Course:** A-10C Weapons Employment Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Target of Opportunity (TOO) Mode](#part-1--target-of-opportunity-too-mode)
5. [Part 2 — Pre-Planned (PP) Mode](#part-2--pre-planned-pp-mode)
6. [Part 3 — JDAM Loft Delivery](#part-3--jdam-loft-delivery)
7. [Part 4 — Multi-JDAM Employment](#part-4--multi-jdam-employment)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Explain the GPS/INS dual-guidance architecture of the JDAM and how it differs from laser guidance
- [ ] Distinguish between TOO and PP JDAM employment modes and select the appropriate mode
- [ ] Configure the DSMS for GBU-38 and GBU-31 including correct fuze, quantity, and release interval
- [ ] Execute a TOO JDAM delivery using TGP-designated coordinates
- [ ] Execute a PP delivery using a pre-loaded CDU steerpoint as the target
- [ ] Program target elevation accurately and explain the consequence of elevation errors
- [ ] Perform a JDAM loft delivery for stand-off range
- [ ] Employ multiple JDAMs against separate targets or in a ripple pass

---

## Ground Brief

### JDAM Guidance System

| Component | Function |
|---|---|
| **GPS receiver** | Primary guidance — navigates directly to surveyed coordinates |
| **INS (ring-laser gyro)** | Secondary guidance — corrects GPS drop-outs; provides continuity of guidance |
| **Dual guidance** | If GPS is denied/jammed: INS alone may degrade CEP to 20–30 m |
| **No seeker** | JDAM cannot follow a laser spot or TV image — it homes on coordinates only |

> **Key Insight:** An LGB guides to *laser energy on a target*. A JDAM guides to *coordinates in space*. A moving target will survive a JDAM; a fixed hardened structure is a JDAM's ideal target.

### JDAM vs LGB — When to Use Which

| Factor | JDAM | LGB |
|---|---|---|
| Weather (cloud, smoke) | **All-weather** — GPS unaffected | Limited by laser LOS |
| Moving targets | Ineffective | **Can be effective** (with POINT track + lase) |
| Hard fixed targets | **Preferred** | Good — if laser LOS is clear |
| Stand-off range | **Excellent** — loft profile | Limited by TGP range |
| Target elevation accuracy needed | **Critical (±30 ft)** | Not critical |

### GBU-38 and GBU-31 Quick Reference

| Weapon | Body | Total Weight | CEP | Typical Use |
|---|---|---|---|---|
| **GBU-38** | Mk-82 (500 lb) | ~570 lb | < 5 m (GPS) | Soft fixed targets; flexible loading |
| **GBU-31** | Mk-84 (2,000 lb) | ~2,115 lb | < 5 m (GPS) | Hard targets; hardened bunkers |

### JDAM Employment Modes

| Mode | Description | When to Use |
|---|---|---|
| **TOO (Target of Opportunity)** | Coordinates are designated NOW via TGP or SPI | Target not known before flight; identified in-flight |
| **PP (Pre-Planned)** | Coordinates loaded in CDU before takeoff or in-flight via data-link | Fixed, known target with accurate survey coordinates |

### Target Elevation — Critical Parameter

- JDAM uses target elevation (Z-axis) in its fire-control solution.
- **Error of ±100 ft in elevation = impact error of several meters** at terminal angle.
- Accurate elevation sources (in priority order):
  1. **DTED (Digital Terrain Elevation Data)** — loaded via data cartridge; automatic
  2. **TGP laser range** — TGP laser ranges to the target surface and reads ELEV
  3. **Survey data** — pre-briefed elevation from target intelligence
  4. **CDU steerpoint ELEV** — manually entered

> **CRITICAL:** Before any JDAM release, verify **target elevation is correct** on the DSMS JDAM sub-page.

---

## Pre-Mission Setup

### Recommended Loadout

| Station | Weapon |
|---|---|
| 3, 4 | GBU-38 (500 lb JDAM) |
| 8, 9 | GBU-38 (500 lb JDAM) |
| 5 | GBU-31 (2,000 lb JDAM, optional) |
| 10 | TGP |

### DSMS Configuration — GBU-38 TOO

| Step | Action |
|---|---|
| 1 | DSMS STATUS → select GBU-38 station |
| 2 | PROF → **CCRP** mode |
| 3 | DSMS JDAM sub-page → **TOO** mode |
| 4 | Fuze: **NOSE / INST** (training) |
| 5 | Qty: **SGL** |
| 6 | Verify ELEV field — leave blank for TGP-derived elevation |

### Pre-Attack Checks

| Step | Action |
|---|---|
| 1 | CDU → GPS status page → verify **GPS READY** and satellite count ≥ 4 |
| 2 | TGP → **OPER** on AHCP |
| 3 | DSMS: GBU-38 selected; CCRP; TOO mode |
| 4 | CDU steerpoints loaded for PP targets if applicable |
| 5 | MASTER ARM → **SAFE** until IP |

---

## Part 1 — Target of Opportunity (TOO) Mode

TOO mode is used when a target is identified and designated in-flight. The pilot uses the TGP to designate the target, the IFFCC reads the TGP's GPS coordinates (laser-ranged), and those coordinates are programmed into the JDAM's guidance unit at release.

### TOO Delivery Workflow

```
[TGP acquires target → POINT track → SPI set]
         ↓
[DSMS: GBU-38, CCRP, TOO selected]
         ↓
[CCRP steering cue appears → fly azimuth line]
         ↓
[Hold pickle → auto-release → JDAM navigates to TGP coordinates]
         ↓
[No laser required after release → egress immediately]
```

### TOO Delivery Procedure

| Step | Action |
|---|---|
| 1 | TGP: find and ID target; switch to **NARROW FOV** for precise aiming |
| 2 | **POINT track:** TMS UP short → hold lock on target |
| 3 | **SPI:** TMS UP short → coordinates set from TGP |
| 4 | TGP: enable laser ranging → verify **ELEV** reading on HUD/CDU |
| 5 | DSMS: verify GBU-38, CCRP, **TOO** mode |
| 6 | **MASTER ARM → ARM** |
| 7 | Fly CCRP azimuth steering line → center FPM on cue |
| 8 | **Hold pickle** — range bar descends |
| 9 | **Auto-release** — weapon away |
| 10 | **Immediate egress** — no laser required; maneuver freely |
| 11 | TGP optional — assess impact |

### TOO Mode: What Happens at Release

- At the moment of release, the IFFCC **freezes the current TGP GPS coordinates** and sends them to the JDAM.
- The JDAM guidance kit programs itself with those coordinates, then navigates independently.
- **Post-release target movement:** If the TGP moves off target after release, the JDAM is unaffected — it is already flying to the coordinates that were captured at release.
- **If TGP LOS is lost before release:** JDAM uses last SPI coordinates — still functional if SPI was correctly set.

---

## Part 2 — Pre-Planned (PP) Mode

PP mode is used for pre-surveyed, fixed, high-confidence targets. Coordinates and elevation are entered into a CDU steerpoint before the engagement.

### CDU Steerpoint Loading

| Step | Action |
|---|---|
| 1 | CDU → **STPT** page |
| 2 | Select steerpoint number (e.g., 11–20 for PP targets) |
| 3 | Enter **LAT/LON** from target intelligence |
| 4 | Enter **ELEV** — elevation in feet MSL from survey data |
| 5 | Verify coordinates on MFCD TGP (slew TGP to steerpoint to confirm it points at the target) |

### PP Delivery Procedure

| Step | Action |
|---|---|
| 1 | DSMS: GBU-38 selected; CCRP; **PP** mode |
| 2 | DSMS JDAM sub-page → select the CDU steerpoint number as the target |
| 3 | Verify LAT/LON and ELEV are correct |
| 4 | TGP (optional): slew to steerpoint to visually confirm it is on the correct target |
| 5 | MASTER ARM → ARM |
| 6 | Fly CCRP steering cue |
| 7 | Hold pickle → auto-release |
| 8 | Egress |

> **Advantage of PP:** The solution is computed from precise survey data, not real-time TGP designation. In degraded visibility (night, weather) where the TGP cannot see the target, PP mode allows accurate employment against known coordinates.

---

## Part 3 — JDAM Loft Delivery

A loft delivery extends the release range significantly, allowing the A-10C to remain further from defended targets while still delivering the JDAM accurately.

### Loft Profile Geometry

```
                    /-- JDAM ballistic arc --\
               /  /                           \  \
          /   /                                \   \ impact
     / (pull)                                        [target]
[IP]------------ level flight -------------------------
```

| Parameter | Value |
|---|---|
| Entry Altitude | 10,000–14,000 ft AGL |
| Entry Airspeed | 350–400 KIAS |
| Entry Range to Target | ~10 nm |
| Pull Angle | 10–15° nose-up |
| Release Altitude | 12,000–16,000 ft AGL |
| Typical Standoff Range | 15–25 nm (GBU-31) |

### Loft Delivery Procedure

| Step | Action |
|---|---|
| 1 | Verify GPS READY; JDAM PP/TOO mode selected |
| 2 | Set SPI to target (TOO) or verify PP steerpoint |
| 3 | Fly at entry altitude toward IP at 350 KIAS |
| 4 | At computed IP: initiate **10–15° nose-up pitch** |
| 5 | Hold pickle — IFFCC computes loft release point |
| 6 | **Auto-release** during the climb — JDAM flies ballistic arc to target |
| 7 | Immediately roll off and egress — TGP not required after release |

> **Training Note:** Loft delivery timing is computed by the IFFCC automatically when CCRP is selected with JDAM in TOO or PP mode. The pilot's only job is to fly the CCRP steering cue and hold pickle. The system handles the rest.

---

## Part 4 — Multi-JDAM Employment

### Employment Against Multiple Separate Targets

| Method | Description |
|---|---|
| **Sequential TOO** | Designate target 1 → release → re-designate target 2 → release |
| **PP Multi-target** | Pre-load targets in steerpoints 11, 12, etc. → sequence through in DSMS |
| **Ripple** | DSMS ripple setting — multiple bombs on same target in one pass |

### Sequential TOO Procedure (Two Separate Targets)

| Step | Action |
|---|---|
| 1 | TGP: designate **target 1** → POINT track → SPI |
| 2 | DSMS: GBU-38, station 3, TOO |
| 3 | Hold pickle → auto-release station 3 |
| 4 | Immediately: TGP slew to **target 2** → POINT track → SPI |
| 5 | DSMS: GBU-38, station 4, TOO |
| 6 | Hold pickle → auto-release station 4 |
| 7 | Confirm both impacts via TGP or egress |

> **Time constraint:** JDAM coordinates are frozen at release. Both JDAMs must be released before the pilot egresses. The second release can occur within seconds of the first.

### Event Sequence

- [ ] **Pass 1:** Instructor demonstrates TOO delivery; student observes
- [ ] **Pass 2:** Student executes GBU-38 TOO delivery independently
- [ ] **Pass 3:** Student executes GBU-38 PP delivery against pre-loaded steerpoint
- [ ] **Pass 4:** Student executes loft delivery (GBU-31 or GBU-38)
- [ ] **Pass 5 (Advanced):** Student executes two-target sequential TOO employment

---

## Completion Standards

| Item | Standard |
|---|---|
| **GPS status verified** | GPS READY confirmed; ≥ 4 satellites before any JDAM employment |
| **DSMS mode selection** | TOO vs PP selected correctly; CCRP mode; correct fuze |
| **TGP POINT track** | Lock stable on target before SPI set |
| **Target elevation** | ELEV verified correct (laser-ranged or survey); not left blank unless DTED is loaded |
| **GBU-38 accuracy** | Impact within **30 m** of designated target |
| **GBU-31 accuracy** | Impact within **30 m** of designated target |
| **PP employment** | Steerpoint coordinates correct; TGP confirms before release |
| **Loft delivery** | Weapon releases during climb; impact within 30 m |
| **Multi-JDAM** | Both JDAMs hit separate targets within 30 m; correct station sequence |
| **Egress** | Immediate post-release egress; no lingering in threat envelope |
| **Master Arm discipline** | ARM at IP; SAFE after last pass |

---

## Common Errors

| Error | Correction |
|---|---|
| **GPS not checked** | "JDAM is GPS-guided. No GPS lock = large miss. Check the CDU GPS page before every JDAM pass." |
| **Elevation field blank (no DTED)** | "If DTED is not loaded, ELEV defaults to zero. A target at 1,000 ft MSL will take a 1,000-ft elevation miss. Range the target with the TGP laser or enter survey elevation." |
| **TOO when PP data is better** | "If you have a survey coordinate, use PP. TGP laser coordinates are excellent, but pre-surveyed targets deserve PP mode for maximum accuracy." |
| **Holding pickle after release (waiting)** | "Once the bomb is off, it's flying. No need to hold pickle. Your next job is to designate the next target or egress. Release and move on." |
| **Maneuvering between sequential TOO passes** | "For sequential targets: designate, release, re-designate, release — fast. Don't fly away between passes. TOO is a rapid two-target workflow." |
| **Ripple interval too short** | "If bombs hit simultaneously, fragmentation effects overlap and may void both. Consult DSMS ripple interval guidance; use ≥ 0.5 sec for GBU-38." |
| **JDAM against a moving target** | "JDAM homes to coordinates. If the target drives 50 meters left after you release — the bomb hits where the target was. Use Maverick or cannon for movers." |

---

[← Event 5: Laser-Guided Bombs](event-5-lgb.md) | [→ Event 7: Advanced Systems & Self-Defense](event-7-advanced-selfdefense.md)

---

*Based on T.O. 1A-10C-34-1-1 and Eagle Dynamics DCS A-10C/II documentation. For simulation use only.*
