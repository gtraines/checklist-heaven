# Event 4 — TGP Operations & AGM-65 Maverick

> **Course:** A-10C Weapons Employment Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — TGP Operations](#part-1--tgp-operations)
5. [Part 2 — AGM-65 Maverick Employment](#part-2--agm-65-maverick-employment)
6. [Completion Standards](#completion-standards)
7. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Power up the TGP during ground operations and verify operational status before takeoff
- [ ] Navigate the TGP MFCD page: FOV, polarity, sensor mode (FLIR/CCD), and OSB functions
- [ ] Employ HOTAS controls (China Hat, TMS, DMS) to slew the TGP, establish POINT and AREA track, and set SPI
- [ ] Laser-designate a target using the TGP (LASER ARM set, correct code, TMS UP long)
- [ ] Explain the SPI system: what it is, how to set it from TGP, and how it integrates with weapons
- [ ] Select an appropriate Maverick variant (IR vs. EO-TV) for day/night conditions
- [ ] Employ the SPI-handoff-to-Maverick workflow against at least 2 independent targets
- [ ] Demonstrate IR Maverick cooldown discipline — select during ingress, verify "RDY" before targeting
- [ ] Conduct a multi-target Maverick ripple sequence (≥ 2 missiles, separate targets)

---

## Ground Brief

### TGP Pod Variants

| Pod | Aircraft | Key Capabilities |
|---|---|---|
| **Litening AT** (AN/AAQ-28) | A-10C | FLIR 640×480, CCD-TV, laser designator/rangefinder, laser spot tracker (LST) |
| **Sniper XR** (AN/AAQ-33) | A-10C II | Enhanced FLIR 1024×1024, longer detection range, HMCS slew integration |

Both pods are mounted on station 10 (right inboard pylon). For training purposes, operational procedures are identical — the Sniper XR has better image quality.

### TGP Power-On Sequence

| Step | Action | Timing |
|---|---|---|
| 1 | AHCP: **TGP → STBY** | During engine start or EGI alignment |
| 2 | Wait ~90 seconds | Pod performs gyro spin-up and thermal calibration |
| 3 | AHCP: **TGP → OPER** | Pod enters operational mode |
| 4 | Verify MFCD TGP page shows live video | Cross-hairs centered; OSBs labeled |

**Rule:** Power up TGP during ground operations. By the time the aircraft is airborne and approaching the target area, the pod will be ready.

### TGP Track Modes

| Mode | Behavior | Best Use |
|---|---|---|
| **Snowplow** | Cross-hairs fixed forward and below; moves with aircraft | Initial route search along a heading |
| **INR** (Inertial) | Cross-hairs stabilized on a ground point via INS | Short-term ground point hold; approximate |
| **AREA** | Scene correlation tracking — locks to terrain features | Fixed structures, intersections, static targets |
| **POINT** | Contrast tracking — follows a specific object | Moving targets, vehicles; **required for laser designation** |

**Key Rule:** Always use **POINT track** for laser designation and weapon delivery. AREA track can drift off a moving target.

### TGP HOTAS Controls

| Control | Function |
|---|---|
| **China Hat FWD** | Slave TGP to current SPI (points pod at SPI) |
| **China Hat AFT** | Toggle SOI (Sensor of Interest) to TGP |
| **DMS Hat** | Slew TGP cross-hairs (when TGP is SOI) |
| **TMS UP (short)** | Set SPI from current TGP cross-hair position |
| **TMS UP (long)** | Fire laser continuously (designation) |
| **TMS LEFT** | Abort/break track — return to INR |

> **SOI (Sensor of Interest):** The TGP only responds to slew commands when it is the active SOI. Verify green border on TGP MFCD page. Press China Hat AFT to make TGP the SOI.

### Laser Operations

| Requirement | Action |
|---|---|
| LASER ARM switch | AHCP → **LASER ARM → ARM** |
| Laser code set | CDU → LSR page → enter **1688** (default) |
| TGP in POINT track | Tracking target object (not terrain) |
| Lasing | **TMS UP long** → laser fires; MFCD shows "LSR FIRE" |

**Laser Timing Rule for LGBs:**
- Pre-release: Laser OFF (range-only if needed)
- Terminal phase (~10–15 seconds before impact): Laser **MUST be ON**
- Post-impact: Laser OFF

### AGM-65 Maverick Variant Summary

| Variant | Seeker | Warhead | Day/Night |
|---|---|---|---|
| **AGM-65D** | Imaging IR | 125 lb shaped charge | Day and Night |
| **AGM-65G** | Imaging IR | 300 lb penetrating blast-frag | Day and Night |
| **AGM-65H** | EO-TV (CCD) | 125 lb shaped charge | **Day Only** |
| **AGM-65K** | EO-TV (CCD) | 300 lb penetrating blast-frag | **Day Only** |
| **AGM-65L** | Laser (SAL) | 300 lb penetrating blast-frag | Day and Night |

#### Variant Selection Logic

| Condition | Use |
|---|---|
| Night or low visibility | **D (light) or G (heavy)** — IR works in darkness |
| Daytime, best visual ID | **H (light) or K (heavy)** — CCD provides excellent contrast |
| External laser available (JTAC) | **L** — seeker acquires laser energy; no slewing required |
| Large/hard target (bunker, bridge) | **G, K, or L** (300 lb warhead) |
| Individual armored vehicle | **D or H** (125 lb shaped charge) |

#### IR Cooldown (D/G)

- IR seekers require **3–5 minutes** of cooldown before they are operational.
- **Select IR Mavericks on DSMS during ingress** — not over the target area.
- Wait for **"RDY"** on the MFCD before attempting to lock.
- EO-TV (H/K) are **instant-ready** — no cooldown.

---

## Pre-Mission Setup

### Recommended Loadout

| Station | Weapon |
|---|---|
| 2, 10 | AGM-65D (IR Maverick — 2 per outboard) |
| 3, 9 | AGM-65G (IR Maverick — heavy, 2 per inboard) |
| 4, 8 | AGM-65H or AGM-65K (EO-TV — for Part 2 day training) |
| 10 | TGP (Litening or Sniper — right inboard pylon) |

*(Adjust per available DCS mission loadout)*

### DSMS Pre-Mission Checks

| Step | Action |
|---|---|
| 1 | DSMS STATUS → verify TGP on station 10 |
| 2 | DSMS STATUS → verify Maverick stations and quantities |
| 3 | Select **IR Maverick** stations; wait for cooldown (select early!) |
| 4 | CDU → LSR → verify laser code **1688** |
| 5 | AHCP: TGP OPER; verify MFCD shows TGP video |
| 6 | AHCP: **LASER ARM → SAFE** (will ARM before designation pass) |

---

## Part 1 — TGP Operations

### TGP Familiarization Sequence

The instructor directs a series of TGP exercises before any weapon employment:

#### Exercise 1: Search and Identification

| Step | Instruction |
|---|---|
| 1 | TGP SOI (China Hat AFT); WIDE FOV |
| 2 | Slew DMS hat to search an area 3–5 nm ahead |
| 3 | Identify a vehicle or structure in FLIR (WHOT) |
| 4 | Switch to NARROW FOV; confirm target type |
| 5 | Toggle polarity (WHOT/BHOT) to compare contrast |
| 6 | Switch to CCD/TV mode; compare image quality (day only) |

#### Exercise 2: POINT Track and SPI

| Step | Instruction |
|---|---|
| 1 | Slew TGP cross-hairs onto a vehicle |
| 2 | Enter POINT track: TMS UP (short) when cross-hairs are on target |
| 3 | Observe: gate appears and follows target |
| 4 | Set SPI: TMS UP short → SPI set (see SPI symbol on HUD and TAD) |
| 5 | Check TAD page — SPI diamond should appear at target location |
| 6 | Slave TGP back to SPI: China Hat FWD (verify pod points at SPI) |

#### Exercise 3: Laser Designation

| Step | Instruction |
|---|---|
| 1 | TGP in POINT track on vehicle target |
| 2 | AHCP: **LASER ARM → ARM** |
| 3 | Verify laser code on CDU (1688) |
| 4 | **TMS UP long** → laser fires → "LSR FIRE" on MFCD |
| 5 | Hold for 3 seconds; release → laser stops |
| 6 | Observe coordinates update (laser-range provides precise ELEV) |
| 7 | **LASER ARM → SAFE** after exercise |

#### Exercise 4: SPI Handoff to Another Sensor

| Step | Instruction |
|---|---|
| 1 | TGP tracking target; SPI set |
| 2 | Navigate to TAD MFCD page |
| 3 | Observe SPI diamond on TAD — matches TGP target position |
| 4 | Slave Maverick (when selected) to SPI: China Hat FWD |
| 5 | Verify Maverick seeker slews to TGP-designated point |

**After completing all 4 exercises:** Instructor evaluates student proficiency with TGP before proceeding to Maverick employment.

---

## Part 2 — AGM-65 Maverick Employment

### Standard Employment Sequence (SPI Handoff Method)

This is the **preferred** method — use TGP to find and designate, then handoff to Maverick for the shot. Minimizes time looking at the Maverick seeker.

```
[TGP finds target → POINT track → SPI set]
         ↓
[Maverick selected; seeker slaved to SPI via China Hat FWD]
         ↓
[Maverick SOI; narrow FOV; confirm target; TMS UP → LOCK]
         ↓
[Within envelope; PICKLE → missile fires; fire-and-forget]
         ↓
[TGP resumes tracking next target; cycle next Maverick]
```

| Step | Action |
|---|---|
| 1 | **TGP:** acquire and POINT track target |
| 2 | **TMS UP (short):** Set SPI from TGP |
| 3 | **DSMS:** Verify IR or EO-TV Maverick is selected; "RDY" confirmed |
| 4 | **China Hat FWD:** Slave Maverick seeker to SPI |
| 5 | **China Hat AFT:** Switch SOI to Maverick MFCD page |
| 6 | **DMS:** Fine-slew to center cross-hairs on target |
| 7 | Switch to **NARROW FOV** — confirm target in center of seeker |
| 8 | **TMS UP (short):** Lock — tracking gate appears on target |
| 9 | Verify stable lock — gate holds on target, not drifting |
| 10 | **AHCP: MASTER ARM → ARM** (if not already armed) |
| 11 | Verify within launch envelope (4–10 nm, above 3,000 ft AGL) |
| 12 | **PICKLE** — missile launches; fire-and-forget |
| 13 | Observe flight; BDA on TGP |
| 14 | DSMS auto-advances to next Maverick; repeat for next target |

### Profile A: Medium-Altitude Standoff

| Parameter | Value |
|---|---|
| Entry Altitude | 12,000–18,000 ft AGL |
| Airspeed | 300–350 KIAS |
| Dive Angle | 0–15° |
| Launch Range | 6–10 nm (IR) / 4–6 nm (EO-TV) |
| Min Launch Altitude | 3,000 ft AGL |

### Profile B: Pop-Up (Threat Environment)

| Parameter | Value |
|---|---|
| Ingress Altitude | 200–500 ft AGL (terrain masked) |
| Pop-Up Distance | 3–5 nm from target |
| Pull-Up | 15–20° nose-up; climb to 5,000–8,000 ft AGL |
| Lock and Launch | During apex or descent; 3–5 nm slant |
| Egress | Return to low altitude immediately after launch |

**Pop-Up Technique:**

| Step | Action |
|---|---|
| 1 | Ingress low at 400+ KIAS; Maverick cooled and ready during ingress |
| 2 | At 3–5 nm from target: **pull up** to 15–20° nose-high |
| 3 | Climb to 5,000–8,000 ft AGL |
| 4 | **SPI from TGP** (if TGP still has target) — **or** slew Maverick directly |
| 5 | China Hat FWD → slave to SPI; switch SOI to Maverick |
| 6 | Narrow FOV; lock (TMS UP); pickle |
| 7 | **Push back down immediately** after launch — terrain mask |
| 8 | Missile guides autonomously — no further pilot input |

### Multi-Target Ripple Sequence

After the first Maverick is fired:
1. DSMS auto-advances to next Maverick station — new seeker video on MFCD.
2. **TGP slews to next target** (or new SPI is set by instructor).
3. **China Hat FWD** — slave new Maverick to new SPI.
4. Lock; pickle.
5. Cycle time: experienced pilots achieve **30–45 sec per missile**.

### Event Sequence — Maverick Passes

- [ ] **Pass 1:** Standard medium-altitude — single target; SPI handoff method; instructor observing
- [ ] **Pass 2:** Independent — student selects target on TGP and executes full sequence
- [ ] **Pass 3:** Pop-up profile — low ingress; instructor evaluates lock acquisition speed
- [ ] **Pass 4 & 5:** Ripple — 2 missiles, 2 separate targets in one pass; student executes independently
- [ ] **Verbal Q:** Instructor queries: "Target is a T-72 in low visibility at night — which Maverick variant?" *(AGM-65D or G — IR; EO-TV not functional at night)*

---

## Completion Standards

| Item | Standard |
|---|---|
| **TGP power-on** | TGP powered in STBY during ground ops; OPER before takeoff |
| **POINT track** | Student independently achieves stable POINT track on a moving vehicle |
| **SPI from TGP** | SPI set correctly; TAD shows SPI diamond at target location |
| **Laser designation** | Laser fires (LASER ARM set, code correct, TMS UP long); MFCD confirms "LSR FIRE" |
| **IR cooldown discipline** | Maverick selected during ingress; "RDY" confirmed before targeting run |
| **SPI handoff to Maverick** | Maverick seeker slaved to TGP-designated target before lock |
| **Lock-on confirmation** | Stable tracking gate confirmed in NARROW FOV before firing |
| **Maverick accuracy** | ≥ 3 of 5 missiles impact designated target |
| **Ripple employment** | ≥ 2 missiles, 2 separate targets, with correct re-acquisition sequence |
| **Variant selection** | Correct variant selected for scenario conditions (day/night, target type) |
| **Master Arm discipline** | ARM before each engagement; SAFE after last missile |

---

## Common Errors

| Error | Correction |
|---|---|
| **Not powering TGP during ground ops** | "TGP takes 90 seconds. Power it up during engine start. Never overhead the target before the pod is ready." |
| **Wrong SOI for slew** | "Check the green border. If TGP MFCD doesn't have the green border, slew commands go nowhere." |
| **AREA track on moving targets** | "AREA locks to terrain. Target drives away. Moving target = POINT track." |
| **IR Maverick not cooled** | "You selected it over the target. Cooldown takes 3–5 minutes. Select during ingress." |
| **Not using SPI handoff** | "Manual Maverick slew is slow. TGP → SPI → China Hat FWD is the standard. Always." |
| **Firing outside launch envelope** | "The HUD shows in-zone / out-of-zone. Check range. Don't fire out of zone." |
| **EO-TV Maverick at night** | "H and K are daylight only. At night: D, G, or L only. Check your variant." |
| **No PID before firing** | "If you can't see what it is on the seeker, you don't shoot. PID required." |
| **Laser code mismatch** | "CDU LSR page shows the code. Weapon code must match. 1688 is default. Verify." |

---

[← Event 3: Unguided & Cluster Munitions](event-3-bombs.md) | [→ Event 5: Laser-Guided Bombs](event-5-lgb.md)

---

*Based on T.O. 1A-10C-34-1-1 and Eagle Dynamics DCS A-10C/II documentation. For simulation use only.*
