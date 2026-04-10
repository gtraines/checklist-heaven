# Event 5 — Laser-Guided Bombs (GBU-12 / GBU-10)

> **Course:** A-10C Weapons Employment Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Self-Lase Delivery (TGP)](#part-1--self-lase-delivery-tgp)
5. [Part 2 — Buddy-Lase Delivery (External Designation)](#part-2--buddy-lase-delivery-external-designation)
6. [Completion Standards](#completion-standards)
7. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Configure the DSMS for GBU-12 and GBU-10: mode (CCRP), fuze (NOSE/INST or DLY), laser code matching
- [ ] Explain how an LGB seeker acquires and follows reflected laser energy (the "laser basket" concept)
- [ ] Perform a complete self-lase CCRP delivery: TGP → POINT track → SPI → CCRP steering → release → lase terminal phase → assess BDA
- [ ] Correctly time the laser: delayed lasing from 10–15 seconds before impact (advanced) OR lase from release (standard)
- [ ] Explain the environmental limitations of laser guidance: clouds, smoke, humidity
- [ ] Coordinate a buddy-lase delivery using correct radio procedures and laser code matching
- [ ] Use TGP LST mode to detect and confirm external laser designation before releasing

---

## Ground Brief

### How LGBs Work

1. Weapon is released ballistically — falls like a dumb bomb initially.
2. The laser seeker in the weapon's nose detects **reflected laser energy** bouncing off the designated target.
3. Guidance fins steer the weapon toward the laser spot.
4. The seeker follows the laser energy all the way to impact.
5. **No laser = no guidance.** Without laser energy on the target, the weapon impacts wherever gravity takes it.

#### The Laser Basket

- The LGB seeker has a limited field of view — approximately **±15° from centerline**.
- The weapon must be on a trajectory where the seeker can "see" the laser spot.
- **CCRP delivery guarantees the bomb is in the basket** — the IFFCC computes the exact release point.
- Manual (CCIP) LGB delivery risks the seeker being out of the basket. CCRP is the standard.

### LGB Quick Reference

| Weapon | Body | Total Weight | CEP | Best Against |
|---|---|---|---|---|
| **GBU-12** | Mk-82 (500 lb) | ~610 lb | < 1 m | Vehicles, light structures, soft targets |
| **GBU-10** | Mk-84 (2,000 lb) | ~2,084 lb | < 1 m | Hardened bunkers, bridges, large structures |

### Fuze Selection

| Fuze Function | Use |
|---|---|
| **NOSE / INST** | Soft targets — vehicles, personnel, light structures |
| **NOSE / DLY1** | Light concrete structures; ensures penetration before detonation |
| **NOSE / DLY2** | Hardened bunkers, bridge piers |
| **N+T / INST** | Standard combat setting (dual fuze redundancy) |

### Laser Code

- 4-digit PRF code — must match the seeker code on the GBU guidance kit.
- **Default: 1688** (standard NATO training code).
- Set on: **CDU → LSR page → enter code → ENTER**.
- For buddy lase: coordinate with JTAC/FAC-A and match their code.

### Laser Timing

| Scenario | When to Lase |
|---|---|
| **Standard (training)** | Lase from release — simplest; never misses laser timing |
| **Advanced / tactical** | Lase only during terminal phase: ~10–15 sec before impact |
| **Short TOF (< 15 sec)** | Lase from release regardless |
| **Long TOF (> 20 sec)** | Delay lasing to terminal phase |

> **Instructor Note:** Students should lase from release for all training deliveries. The delayed-lasing technique is introduced as a concept for self-study and advanced employment.

### TGP LOS Maintenance After Release

After releasing the bomb, the TGP must continuously illuminate the target until impact. This means:
- **No aggressive maneuvering after release** — steep banks or pulls may mask the TGP (right inboard pylon) from the target.
- **Maintain roughly wings-level or a shallow orbit** through the bomb's time of flight.
- If TOS (time on station) permits, make a gentle orbit to maintain LOS.

### Environmental Limitations

| Factor | Effect | Mitigation |
|---|---|---|
| **Cloud undercast** | Laser blocked; bomb goes dumb | Must have clear LOS from aircraft to target through entire flight |
| **Smoke / dust** | Attenuates laser; degrades seeker acquisition | Avoid lasing through smoke; adjust aimpoint if needed |
| **Fog / humidity** | Reduces effective laser range | Deliver from lower altitude to reduce atmospheric path |

---

## Pre-Mission Setup

### Recommended Loadout

| Station | Weapon |
|---|---|
| 3, 9 | GBU-12 (Paveway II, 500 lb) |
| 4 or 8 | GBU-10 (Paveway II, 2,000 lb) |
| 10 | TGP (Litening or Sniper) |

### DSMS Configuration — GBU-12

| Step | Action |
|---|---|
| 1 | DSMS STATUS → select GBU-12 station |
| 2 | PROF → Delivery Mode: **CCRP** |
| 3 | Fuze: **NOSE / INST** (default for training) or **N+T / INST** |
| 4 | Release Qty: **SGL** |
| 5 | Verify "GBU12" and CCRP steering on HUD |

### Pre-Attack Checks

| Step | Action |
|---|---|
| 1 | CDU → LSR page → verify laser code **1688** |
| 2 | AHCP: **TGP → OPER**; verify MFCD video |
| 3 | AHCP: **LASER ARM → ARM** (over target area) |
| 4 | AHCP: **MASTER ARM → ARM** |
| 5 | DSMS: GBU-12 or GBU-10 selected; CCRP mode |

---

## Part 1 — Self-Lase Delivery (TGP)

### Standard Self-Lase CCRP Workflow

```
[TGP finds target → POINT track → SPI set]
         ↓
[DSMS: GBU selected; CCRP; fuze correct]
         ↓
[Fly CCRP azimuth steering line → hold pickle → auto-release]
         ↓
[Maintain TGP LOS → lase in terminal phase → impact → BDA]
```

| Step | Action |
|---|---|
| 1 | **TGP:** acquire target; WIDE FOV search → NARROW for ID |
| 2 | **POINT track:** TMS UP short → cross-hairs lock to target |
| 3 | **SPI:** TMS UP short → SPI set to TGP coordinates |
| 4 | Verify TGP coordinates; note target elevation (laser-ranged ELEV = accurate) |
| 5 | **DSMS:** GBU-12 or GBU-10 selected; CCRP mode; fuze set |
| 6 | **LASER ARM → ARM** (if not already armed) |
| 7 | **MASTER ARM → ARM** |
| 8 | **Fly CCRP steering cue:** center azimuth steering line on FPM |
| 9 | **Hold pickle** — watch range bar descend toward FPM |
| 10 | **Auto-release** — bomb releases when range bar meets FPM |
| 11 | Maintain **wings-level or shallow orbit** to preserve TGP LOS |
| 12 | **TMS UP long → laser ON** — lase continuously until impact |
| 13 | Observe bomb flight on TGP; confirm impact |
| 14 | **Release TMS UP → laser OFF** |
| 15 | BDA: assess damage; re-attack if required |
| 16 | **MASTER ARM → SAFE; LASER ARM → SAFE** after all passes |

### Profile A: Medium-Altitude CCRP (Primary)

| Parameter | GBU-12 | GBU-10 |
|---|---|---|
| Entry Altitude | 12,000–18,000 ft AGL | 15,000–20,000 ft AGL |
| Airspeed | 300–350 KIAS | 300–350 KIAS |
| Dive Angle | 0–10° (level preferred) | 0–10° |
| Bomb Time-of-Flight | ~20–30 sec | ~25–35 sec |
| Laser ON Time | Last 10–15 sec (or from release) | Last 10–15 sec (or from release) |

### Profile B: Dive CCIP (Alternate — Advanced)

| Parameter | GBU-12 |
|---|---|
| Entry Altitude | 12,000–15,000 ft AGL |
| Dive Angle | 20–30° |
| Airspeed | 350–400 KIAS |
| Min Release Altitude | 8,000 ft AGL |
| Laser | ON from release (short TOF in dive) |
| Recovery | 4 G pull; 5,000 ft AGL minimum |

> **Training note:** CCIP dive delivery with LGBs is not trained until the student demonstrates consistent CCRP proficiency. Dive CCIP is an advanced technique requiring simultaneous management of bomb fall line, pipper, and laser designation while maintaining TGP LOS through the dive and pull-off.

### Event Sequence — Self-Lase Passes

- [ ] **Pass 1:** Instructor demonstrates full CCRP self-lase sequence with commentary
- [ ] **Pass 2:** Student executes GBU-12 self-lase CCRP from medium altitude; instructor observes
- [ ] **Pass 3:** Student executes GBU-12 independently against a different target
- [ ] **Pass 4:** Student executes GBU-10 against a hardened structure; student selects appropriate fuze

---

## Part 2 — Buddy-Lase Delivery (External Designation)

In buddy-lase employment, the A-10C pilot **does not need to lase the target**. Instead, a JTAC, FAC-A, or wingman illuminates the target with their own laser. The A-10C releases the LGB and the bomb homes on the external laser energy.

### Why Buddy-Lase?

| Advantage | Explanation |
|---|---|
| Pilot workload reduction | Pilot focuses on CCRP delivery; no laser management required |
| Better geometry | JTAC on the ground has a more stable LOS than a maneuvering aircraft |
| All-aspect | Ground laser can designate targets the aircraft cannot see directly |
| Multi-ship coordination | Multiple aircraft can drop on a single JTAC designation |

### Buddy-Lase Workflow

| Step | Action |
|---|---|
| 1 | **Coordinate laser code:** Radio to JTAC/instructor — "Confirm laser code 1688" |
| 2 | **Set CDU LSR code** to match JTAC code |
| 3 | **TGP LST mode:** TGP OSB → LST; enter expected code — pod will scan for laser |
| 4 | **DSMS:** GBU-12 selected; CCRP mode; fuze set |
| 5 | **SPI:** Set from JTAC coordinates in CDU steerpoint, or use TGP to find the target area |
| 6 | **Fly CCRP steering cue** — same as self-lase; the delivery is identical |
| 7 | At ~20 sec before release: radio **"IP inbound, 20 seconds, request laser"** |
| 8 | JTAC/instructor responds: **"Laser on, code 1688"** |
| 9 | TGP LST shows diamond where laser is detected — **verify it's on the target** |
| 10 | Call: **"Laser captured"** (if LST confirms) |
| 11 | **Hold pickle → auto-release** |
| 12 | Call: **"Rifle"** (weapon released) |
| 13 | Bomb guides to JTAC laser spot |
| 14 | JTAC/instructor calls: **"Splash"** or student observes impact |
| 15 | JTAC: **"Laser off"** |
| 16 | Student: **"Good splash, RTB"** or request re-attack |

### Communication Script (Training)

| Call | Actor |
|---|---|
| *"JTAC, Hawg 1-1, IP inbound, 30 seconds, request laser, code 1688"* | Pilot |
| *"Hawg 1-1, JTAC, laser on, code 1688, confirm"* | JTAC (instructor) |
| *"JTAC, Hawg 1-1, spot confirmed, rifle"* | Pilot |
| *"Hawg 1-1, JTAC, splash. Direct hit. Laser off."* | JTAC (instructor) |

### LST Mode Procedure

| Step | Action |
|---|---|
| 1 | TGP MFCD → OSB: switch to **LST** mode |
| 2 | Enter expected laser code (1688) on TGP LST sub-page |
| 3 | TGP scans for laser energy at the specified PRF |
| 4 | When external laser detected: **diamond appears on MFCD** at laser source location |
| 5 | Confirm diamond is on the target, not a false spot |
| 6 | Proceed with release |

### Event Sequence — Buddy-Lase Pass

- [ ] **Pass 1:** Instructor acts as JTAC; student coordinates laser code, uses LST to confirm, releases GBU-12
- [ ] **Pass 2:** Student performs full radio communication sequence without prompting

---

## Completion Standards

| Item | Standard |
|---|---|
| **DSMS setup** | Correct weapon, CCRP mode, fuze selected independently |
| **Laser code** | CDU LSR code matches weapon code; verified before every pass |
| **LASER ARM** | ARM before each pass; SAFE after last pass |
| **TGP POINT track** | Stable tracking on target confirmed before designating |
| **CCRP delivery** | Azimuth steering line centered; pickle held through auto-release |
| **GBU-12 accuracy** | Impact within **10 m** of TGP-designated point |
| **GBU-10 accuracy** | Impact within **10 m** of TGP-designated point; correct fuze |
| **Laser timing** | Laser ON before bomb impact (confirmed by TGP video) |
| **TGP LOS maintained** | No aggressive maneuvering after release that breaks TGP LOS |
| **Buddy-lase coordination** | Correct radio procedure; laser code coordinated; LST confirms spot |
| **Master Arm discipline** | ARM only in target area; SAFE on egress |

---

## Common Errors

| Error | Correction |
|---|---|
| **Laser ARM not set** | "LASER ARM is on the AHCP — it's a separate switch from MASTER ARM. No LASER ARM = dumb bomb." |
| **Laser code mismatch** | "Brief the code. CDU LSR page shows it. Weapon code must match. 1688 default — verify every time." |
| **Aggressive maneuvering after release** | "TGP is on the right inboard pylon. Bank hard left = pod masked. Wings-level or slow orbit through impact." |
| **Laser ON too late** | "For training: lase from release. If the bomb impacts before the laser is on — dumb bomb hit. Lase earlier." |
| **TGP in AREA track — not POINT** | "AREA lock tracks terrain, not the vehicle. Vehicle moves — AREA misses. Use POINT track." |
| **Releasing above cloud layer** | "Laser can't penetrate clouds. If there's a cloud between you and the target, the bomb goes dumb." |
| **No SPI set before CCRP** | "CCRP needs a target. No SPI = no steering cue. TGP POINT track → TMS UP → SPI first." |
| **Buddy-lase without LST confirmation** | "Use LST to see the spot before you drop. Verify the diamond is on your target, not a false contact." |

---

[← Event 4: TGP & Maverick](event-4-tgp-maverick.md) | [→ Event 6: JDAM & GPS Weapons](event-6-jdam.md)

---

*Based on T.O. 1A-10C-34-1-1 and Eagle Dynamics DCS A-10C/II documentation. For simulation use only.*
