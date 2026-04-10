# Event 3 — Unguided & Cluster Munitions

> **Course:** A-10C Weapons Employment Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Unguided Bombs (Mk-82 / Mk-84)](#part-1--unguided-bombs-mk-82--mk-84)
5. [Part 2 — Low-Altitude Delivery (Mk-82AIR / Snakeye)](#part-2--low-altitude-delivery-mk-82air--snakeye)
6. [Part 3 — Cluster Munitions (CBU-87 / CBU-97)](#part-3--cluster-munitions-cbu-87--cbu-97)
7. [Part 4 — WCMD Stand-Off (CBU-103 / CBU-105)](#part-4--wcmd-stand-off-cbu-103--cbu-105)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Configure DSMS for iron bombs: delivery mode, fuze type, fuze function, ripple quantity, and arming delay
- [ ] Deliver Mk-82 slick in CCIP (30–45° dive) with impact within 75 m of target
- [ ] Deliver Mk-82 in CCRP (level / shallow dive) from a pre-planned SPI
- [ ] Employ Mk-82AIR or Snakeye in a low-altitude level or pop-up profile
- [ ] Explain fragmentation clearance and minimum release altitudes for all iron bomb variants
- [ ] Set correct HOF for CBU-87 CEM and CBU-97 SFW; explain why each requires different HOF
- [ ] Deliver CBU-87 or CBU-97 in CCIP, correctly aligning the ground track with the target orientation
- [ ] Employ WCMD (CBU-103 or CBU-105) in CCRP with correct SPI designation

---

## Ground Brief

### Iron Bombs — Fuze Configuration

| Fuze Function | Effect | Best Against |
|---|---|---|
| **INST** (Instantaneous) | Detonates on contact | Soft targets, personnel, light vehicles |
| **DLY1** (Short Delay, ~10–25 ms) | Penetrates light structures before detonation | Revetments, light buildings |
| **DLY2** (Long Delay, ~60–200 ms) | Deep penetration before detonation | Hardened bunkers, bridge piers |
| **N+T** (Nose + Tail) | Both fuzes active — redundancy | Standard combat setting for all deliveries |

### Arming Delay (AD) — When It Matters

| Delivery Altitude | AD Required | Reason |
|---|---|---|
| > 5,000 ft AGL | None (0 sec) | Frag clearance from altitude |
| 2,000–5,000 ft AGL | 2–4 sec | Moderate frag risk |
| < 2,000 ft AGL (slick bomb) | 4–8 sec | Critical — frag reaches release altitude |
| Mk-82AIR / Snakeye | 0 sec | High-drag retarder provides physical separation |

**Rule:** When in doubt, set AD. A delayed bomb that hits the target is better than an early detonation that damages your aircraft.

### Cluster Munitions Fundamentals

#### CBU-87 CEM — Combined Effects Munition

- 202 BLU-97/B submunitions scattered in an elliptical pattern along the ground track.
- Each bomblet: shaped-charge (anti-armor), fragmentation ring (anti-personnel), incendiary disk.
- Opens at programmed **HOF (Height of Function)**: **1,000–2,000 ft AGL** (default: 1,500 ft).
- **Track alignment critical:** footprint is elliptical along the aircraft's ground track. For linear targets (convoys), fly parallel to the column.

#### CBU-97 SFW — Sensor Fuzed Weapon

- 10 BLU-108/B submunitions × 4 IR-seeking skeets each = **40 autonomous anti-armor warheads**.
- Each skeet scans for hot IR signature (running vehicle engines) and fires an EFP (Explosively Formed Penetrator) downward.
- HOF: **1,500–3,000 ft AGL** (default: 2,000 ft). Skeets need altitude to scan and arm.
- **Critical:** SFW is useless against **cold targets** (parked, concealed). Use CBU-87 against cold vehicles.

#### HOF Quick Reference

| Munition | Minimum HOF | Maximum HOF | Recommended |
|---|---|---|---|
| CBU-87 CEM | 500 ft AGL | 3,000 ft AGL | 1,500 ft AGL |
| CBU-97 SFW | 1,500 ft AGL | 3,000 ft AGL | 2,000 ft AGL |

### WCMD (CBU-103 / CBU-105)

- Adds GPS/INS tail kit to standard CBU cannister — enables stand-off, high-altitude delivery.
- Wind is corrected by the guidance kit — enables delivery from 15,000–25,000 ft AGL without crosswind error.
- **Delivery mode: CCRP** (requires SPI; same as JDAM/LGB workflow).
- Ideal when target is defended and low-altitude/medium-altitude approach is not survivable.

### Minimum Pull-Off Altitudes

| Weapon | Minimum Recovery Altitude |
|---|---|
| Mk-82 (CCIP, 30–45°) | **3,000 ft AGL** |
| Mk-84 (CCIP, 30–45°) | **4,000 ft AGL** |
| Mk-82AIR / Snakeye (low-alt) | **500 ft AGL** |
| CBU-87 CCIP | **3,000 ft AGL** |
| CBU-97 CCIP | **4,000 ft AGL** |

---

## Pre-Mission Setup

### Recommended Loadout

| Station | Weapon |
|---|---|
| 4, 8 | Mk-82 (2 per station) |
| 3, 9 | Mk-84 (1 per station) |
| 2, 10 | Mk-82AIR (2 per station) |
| 5, 7 | CBU-87 (1 per station) |
| 3, 9 (alt) | CBU-97 (if loadout varies) |

*(Adjust per available DCS mission loadout — instructor loads mission appropriately)*

### DSMS Setup — Iron Bombs (Mk-82 Slick)

| Step | Action |
|---|---|
| 1 | DSMS STATUS → select Mk-82 station |
| 2 | PROF → Delivery Mode: **CCIP** (for dive) or **CCRP** (for level) |
| 3 | Fuze: **N+T** |
| 4 | Fuze Function: **INST** (soft targets) or **DLY1** (structures) |
| 5 | Release Qty: **SGL** for accuracy training |
| 6 | AD: **0 sec** (CCIP medium-altitude) or **2–4 sec** (if < 5,000 ft) |
| 7 | Escape Maneuver: **CLM** (climbing escape) |
| 8 | Verify on DSMS; confirm "MK82" and mode on HUD |

---

## Part 1 — Unguided Bombs (Mk-82 / Mk-84)

### CCIP Dive Delivery — Standard Profile

```
         Perch: 10,000–15,000 ft AGL, 350 KIAS
              ↓ Roll in toward target
         Dive: 30–45°, throttle idle
              ↓ [CCIP pipper drifts to target]
         Track 1–2 seconds → PICKLE
              ↓
         Recover: 3,000 ft AGL (Mk-82) / 4,000 ft (Mk-84)
         4–5 G pull
              ↓ Jink egress
```

| Parameter | Mk-82 | Mk-84 |
|---|---|---|
| Dive Angle | 30–45° | 30–45° |
| Entry Altitude | 10,000–15,000 ft AGL | 12,000–15,000 ft AGL |
| Entry Airspeed | 350–400 KIAS | 350–400 KIAS |
| Min Release Altitude | 4,000 ft AGL | 5,000 ft AGL |
| Min Recovery Altitude | **3,000 ft AGL** | **4,000 ft AGL** |
| Fuze (standard) | N+T / INST | N+T / DLY1 or DLY2 |

**Step-by-Step:**

| Step | Action |
|---|---|
| 1 | Fly to perch: 10,000–15,000 ft AGL, 2–3 nm offset, 350 KIAS |
| 2 | AHCP: **MASTER ARM → ARM** |
| 3 | Verify CCIP pipper visible on HUD; bomb type annunciated |
| 4 | Roll in — roll ~135°, pull nose through horizon, roll wings-level in dive |
| 5 | Establish **30–45° dive angle**; throttle idle |
| 6 | CCIP pipper moves toward target — **do not chase it**; let it drift onto target |
| 7 | When pipper is on target and **stable**: "Track, track, PICKLE" |
| 8 | **Begin pull-off immediately** — 4–5 G |
| 9 | Recover to 3,000 ft AGL (Mk-82) or 4,000 ft (Mk-84) minimum |
| 10 | Jink during pull-off; egress off threat axis |
| 11 | After all passes: **MASTER ARM → SAFE** |

> **Pipper Rule:** Never release below the MIN RNG caret. If the pipper hasn't settled on target when the caret approaches, **wave off**. There is always another pass. A wave-off is never graded against the student.

### CCRP Level Delivery

| Parameter | Value |
|---|---|
| Altitude | 10,000–20,000 ft AGL |
| Airspeed | 300–400 KIAS |
| Dive Angle | 0–20° |
| SPI Required | Yes — set from TGP (preferred) or steerpoint |

**Step-by-Step:**

| Step | Action |
|---|---|
| 1 | Set SPI on target: TGP → POINT track target → TMS UP (SPI from TGP) |
| 2 | DSMS: select Mk-82; PROF → **CCRP** mode |
| 3 | AHCP: **MASTER ARM → ARM** |
| 4 | HUD shows azimuth steering line — center it on FPM |
| 5 | Range bar descends; solution circle appears around FPM |
| 6 | **Hold pickle** — weapon auto-releases when range bar meets FPM |
| 7 | Continue straight and level through release; begin turn/climb after release |
| 8 | **MASTER ARM → SAFE** after pass |

> **SPI Required:** CCRP will not generate steering cues without a valid SPI. If the azimuth steering line is absent, verify TGP is in POINT track and TMS UP was pressed.

### Event Sequence — Bomb Passes

- [ ] **Mk-82 CCIP Pass 1:** Instructor observation — assess dive angle and recovery
- [ ] **Mk-82 CCIP Pass 2:** Independent — student selects target; instructor assesses accuracy
- [ ] **Mk-84 CCIP Pass 1:** Independent — student configures DSMS; instructor assesses fuze selection
- [ ] **Mk-82 CCRP Pass 1:** Student designates SPI with TGP; level delivery; instructor assesses technique

---

## Part 2 — Low-Altitude Delivery (Mk-82AIR / Snakeye)

The high-drag variants allow delivery at **200–1,000 ft AGL** — terrain-masking ingress with a pop-up attack, or a level/shallow-dive pass at low altitude. The ballute (Mk-82AIR) or retarder fins (Snakeye) slow the bomb, allowing the aircraft to clear the frag pattern.

### Pop-Up Attack Profile

```
         Ingress: 200–500 ft AGL, 400–450 KIAS (terrain masked)
              ↓ At 3 nm from target — PULL UP
         Pull to 20–30° nose-up; climb to 3,000–5,000 ft AGL
              ↓ Roll inverted; pull nose to target; roll wings-level in 20–30° dive
         CCIP pipper on target → PICKLE
              ↓
         Recover: 500 ft AGL minimum
         Low-altitude egress
```

| Parameter | Value |
|---|---|
| Ingress Altitude | 200–500 ft AGL |
| Ingress Airspeed | 400–450 KIAS |
| Pop-Up Altitude | 3,000–5,000 ft AGL |
| Dive Angle (delivery) | 20–30° |
| Min Recovery Altitude | **500 ft AGL** |
| AD Setting | **0 sec** (retarder provides separation) |

**DSMS Differences from Slick Mk-82:**
- Select **Mk-82AIR** or **MK82SE** (Snakeye) on DSMS.
- AD = **0 sec** (retarder handles separation).
- All other settings same as standard iron bomb.

### Level Low-Altitude Pass (Alternate Profile)

For training environments where the pop-up is not required:

| Step | Action |
|---|---|
| 1 | Ingress at 200–500 ft AGL, 400 KIAS |
| 2 | CCIP pipper drifts toward target as aircraft approaches |
| 3 | When pipper is on target: **PICKLE** |
| 4 | Continue straight; retarder deploys behind the aircraft |
| 5 | Pull up immediately to 1,000 ft AGL or higher after release |

### Event Sequence — Low-Altitude Passes

- [ ] **Mk-82AIR Pop-Up Pass 1:** Student performs full pop-up profile
- [ ] **Mk-82AIR Level Pass 1:** Student performs low-level pass at 300–500 ft AGL

---

## Part 3 — Cluster Munitions (CBU-87 / CBU-97)

### DSMS Setup — CBU-87

| Step | Action |
|---|---|
| 1 | DSMS STATUS → select CBU-87 station |
| 2 | PROF → Delivery Mode: **CCIP** |
| 3 | Set **HOF**: **1,500 ft AGL** (default) |
| 4 | Release Qty: **SGL** |
| 5 | Verify on HUD: "CBU87" with CCIP pipper |

### DSMS Setup — CBU-97

| Step | Action |
|---|---|
| 1 | DSMS STATUS → select CBU-97 station |
| 2 | PROF → Delivery Mode: **CCIP** |
| 3 | Set **HOF**: **2,000 ft AGL** |
| 4 | Release Qty: **SGL** |
| 5 | Verify on HUD |

### CBU-87 CEM Delivery Profile

| Parameter | Value |
|---|---|
| Entry Altitude | 8,000–15,000 ft AGL |
| Dive Angle | 20–40° |
| Entry Airspeed | 350–400 KIAS |
| Min Release Altitude | HOF + 2,000 ft (= 3,500 ft AGL with HOF 1,500) |
| Min Recovery Altitude | **3,000 ft AGL** |

**Track Alignment:** For vehicle columns, fly **parallel** to the column axis. The footprint aligns along the aircraft's ground track — a perpendicular approach drops bomblets across only a narrow strip of the column.

### CBU-97 SFW Delivery Profile

| Parameter | Value |
|---|---|
| Entry Altitude | 10,000–18,000 ft AGL |
| Dive Angle | 20–45° |
| Entry Airspeed | 350–400 KIAS |
| Min Release Altitude | HOF + 3,000 ft (= 5,000 ft AGL with HOF 2,000) |
| Min Recovery Altitude | **4,000 ft AGL** |

**Target state:** SFW requires **running (hot) vehicle engines**. Confirm target is active before employment.

### Event Sequence — Cluster Passes

- [ ] **CBU-87 Pass 1:** Student sets HOF 1,500; delivers against vehicle column; track alignment assessed
- [ ] **CBU-97 Pass 1:** Student sets HOF 2,000; delivers against active armor formation
- [ ] **Verbal Q:** Instructor asks "target is cold/concealed — which weapon?" *(CBU-87, not SFW)*

---

## Part 4 — WCMD Stand-Off (CBU-103 / CBU-105)

WCMD enables high-altitude, stand-off cluster delivery — the GPS/INS tail kit corrects for wind drift that would otherwise scatter the footprint unpredictably.

### DSMS Setup — WCMD

| Step | Action |
|---|---|
| 1 | DSMS STATUS → select CBU-103 or CBU-105 station |
| 2 | PROF → Delivery Mode: **CCRP** |
| 3 | Set **HOF** (same as base munition: 1,500 for CEM, 2,000 for SFW) |
| 4 | Set SPI — TGP point track on target area center → TMS UP |
| 5 | Verify GPS status (same as JDAM) |
| 6 | Release Qty: **SGL** |

### WCMD Delivery Profile

| Parameter | Value |
|---|---|
| Altitude | 15,000–25,000 ft AGL |
| Airspeed | 300–400 KIAS |
| Dive Angle | 0–20° |
| Standoff | 5–8 nm at medium altitude |
| Release Mode | CCRP auto-release (hold pickle) |

**Step-by-Step:**

| Step | Action |
|---|---|
| 1 | TGP: acquire target area → POINT track → TMS UP (SPI set) |
| 2 | DSMS: CBU-103/105 selected; CCRP; HOF set; GPS confirmed |
| 3 | AHCP: MASTER ARM → ARM |
| 4 | Fly azimuth steering line — center on FPM |
| 5 | **Hold pickle** through auto-release |
| 6 | Break off — weapon guides independently; no further action needed |
| 7 | MASTER ARM → SAFE |

### Event Sequence — WCMD Pass

- [ ] **WCMD Pass 1:** Student designates target with TGP; configures DSMS for CBU-103 CCRP; level delivery

---

## Completion Standards

| Item | Standard |
|---|---|
| **Mk-82 CCIP accuracy** | ≥ 2 of 3 passes within **75 m** of target; no release below MIN RNG caret |
| **Mk-82 CCRP accuracy** | Impact within **50 m** of SPI; azimuth steering line centered before release |
| **Mk-84 CCIP** | Correct fuze setting; impact within **100 m**; min 4,000 ft AGL recovery |
| **Mk-82AIR low-altitude** | Correct AD (0 sec); min 500 ft AGL recovery |
| **CBU-87 HOF** | HOF set to 1,500 ft AGL ±200 ft; track aligned with target |
| **CBU-97 HOF** | HOF set to 2,000 ft AGL ±200 ft; target confirmed as active (hot) |
| **WCMD CCRP** | SPI correctly set via TGP; CCRP auto-release executed correctly |
| **DSMS setup** | All configurations performed independently — no instructor prompting |
| **Master Arm discipline** | ARM before each event; SAFE after last pass — no exceptions |

---

## Common Errors

| Error | Correction |
|---|---|
| **Releasing below MIN RNG caret** | "Wave off — always another pass. Minimum altitudes are hard floors." |
| **Wrong fuze for target** | Brief it: "Mk-82 against soft target = INST. Against bunker = DLY2." |
| **No arming delay at low altitude with slick Mk-82** | "500 ft AGL release without AD = frag hits the aircraft. Set AD 4–8 sec." |
| **CBU-87 track perpendicular to column** | "Footprint aligns with your ground track. Fly parallel to the convoy." |
| **CBU-97 against cold targets** | "SFW finds heat. Cold target = no target. Brief the target state every time." |
| **HOF not set (left at default/zero)** | "Bomblets never scatter. Verify HOF before every cluster pass." |
| **WCMD without SPI** | "CCRP needs a target. No SPI = no steering cue = no release. Check TGP designation." |
| **CCRP pipper released before hold** | "CCRP is consent-based. Hold pickle through the auto-release point. Release too early = no weapon release." |

---

[← Event 2: Gun & Rockets](event-2-guns-rockets.md) | [→ Event 4: TGP & Maverick](event-4-tgp-maverick.md)

---

*Based on T.O. 1A-10C-34-1-1 and Eagle Dynamics DCS A-10C/II documentation. For simulation use only.*
