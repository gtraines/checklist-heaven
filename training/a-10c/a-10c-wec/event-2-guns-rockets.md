# Event 2 — GAU-8/A Gun & Rockets

> **Course:** A-10C Weapons Employment Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — GAU-8/A Avenger Cannon](#part-1--gau-8a-avenger-cannon)
5. [Part 2 — Hydra 70 Rockets (M151 HE)](#part-2--hydra-70-rockets-m151-he)
6. [Part 3 — Target Marking (M274 WP)](#part-3--target-marking-m274-wp)
7. [Completion Standards](#completion-standards)
8. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Configure the DSMS for gun and rocket employment (mode, fuze, quantity)
- [ ] Employ the GAU-8/A in PAC-1 strafe against an armored target, achieving at least one confirmed hit per pass
- [ ] Demonstrate burst discipline (1–2 second bursts) and recover at minimum altitude on every pass
- [ ] Manage recoil-induced airspeed and altitude loss in the recovery
- [ ] Select and fire Hydra 70 M151 HE rockets in CCIP from a diving attack, impacting within 50 m of target
- [ ] Fire M274 WP rockets to accurately mark a target for a follow-on simulated attack

---

## Ground Brief

### The GAU-8/A Avenger — Key Facts

| Parameter | Value |
|---|---|
| Caliber | 30 × 173 mm |
| Type | 7-barrel externally powered Gatling gun |
| Rate of Fire | ~3,900 rds/min |
| Ammunition | 1,174 rounds (combat mix: 5:1 API/HEI) |
| Muzzle Velocity | ~1,070 m/s |
| Recoil Force | ~19,000 lbf |

#### Effective Engagement Ranges

| Target Type | Effective Range (Slant) |
|---|---|
| Main Battle Tanks (MBT) | 4,000–6,000 ft |
| IFVs / APCs | 4,000–8,000 ft |
| Soft Targets (trucks, guns, troops) | 6,000–12,000 ft |
| Buildings / Bunkers | 4,000–6,000 ft |

#### Ammunition Conservation

| Burst Duration | Rounds Expended | Passes Available |
|---|---|---|
| 1 second | ~65 rounds | ~18 passes |
| 2 seconds | ~130 rounds | ~9 passes |
| 3 seconds (max recommended) | ~195 rounds | ~6 passes |

**Rule:** 1–2 second bursts only. Short, accurate bursts — not sustained fire.

### PAC-1 — Precision Attitude Control

The IFFCC provides **PAC-1 (Strafe Mode)** for gun employment:
- The gun cross and a stabilized **PAC reticle** are displayed on the HUD.
- The IFFCC compensates for aircraft pitch, roll, and yaw, holding the reticle steady on the aiming point.
- The pilot places the stabilized reticle on the target and fires a short burst.
- The reticle is more accurate than a fixed sight because it corrects for aircraft motion during the firing solution.

### Recoil Effects

| Effect | Magnitude |
|---|---|
| Airspeed bleed | ~10–15 KIAS per 2-second burst at 350 KIAS |
| Nose pitch tendency | Slight pitch-up during firing |
| Yaw wander | Minor lateral oscillation during long bursts |

**Briefing technique:** "I will enter each pass at 350 KIAS. I will lose 10–15 kts per burst. I need 280+ KIAS at recovery to maintain 4 G pull-off. If I'm below 300 at the bottom, I pull off regardless."

### Minimum Pull-Off Altitudes (Hard Floors)

| Profile | Minimum Recovery Altitude |
|---|---|
| Medium-angle strafe (20–30°) | **3,000 ft AGL** |
| Shallow strafe (5–15°) | **1,500 ft AGL** |

**These are not suggestions.** Breaking below minimums on any pass is an automatic DOWN.

### Hydra 70 Rockets — Key Facts

| Parameter | Value |
|---|---|
| Rocket | 2.75" (70 mm) folding-fin aerial rocket |
| Motor | Mk 66 Mod 4 solid-fuel |
| Warheads (this event) | M151 HE (10 lb) and M274 WP (marking) |
| Launchers | LAU-68 (7-tube) or LAU-131 (7-tube) or LAU-61 (19-tube) |
| Effective Range | 1–3 km; CCIP accurate to ~2 km from stabilized dive |
| Delivery Mode | CCIP |
| Fuze | Point detonating (INST); proximity variants not covered here |

---

## Pre-Mission Setup

### Recommended Loadout

| Station | Weapon |
|---|---|
| 2, 10 (outboard pylons) | LAU-68 (Hydra 70 M151, 7-tube) |
| 3, 9 | LAU-68 (Hydra 70 M274 WP, 7-tube) |
| Gun | 1,174 rds (loaded by default) |

### DSMS Configuration — Gun

| Step | Action |
|---|---|
| 1 | DSMS STATUS page — note gun icon (cannon integral, not a pylon station) |
| 2 | DSMS PROF → **GUN** profile → verify mode: N/A (gun uses PAC, not CCIP/CCRP selector) |
| 3 | **AHCP:** GUN/PAC → **GUNARM** |
| 4 | **AHCP:** MASTER ARM → **ARM** (over target area only) |
| 5 | Verify **HUD shows "GUN"** and PAC reticle is displayed |

### DSMS Configuration — Rockets (M151 HE)

| Step | Action |
|---|---|
| 1 | DSMS STATUS → select rocket station (LAU-68) |
| 2 | DSMS PROF → Delivery Mode: **CCIP** |
| 3 | Fuze: **NOSE / INST** (standard HE) |
| 4 | Release Qty: **SGL** (1 rocket per press) or **RPL** with count 2–4 |
| 5 | **AHCP:** MASTER ARM → **ARM** (over target area) |
| 6 | Verify **HUD shows "RKT"** and CCIP pipper visible |

### DSMS Configuration — Rockets (M274 WP)

| Step | Action |
|---|---|
| 1 | DSMS STATUS → select WP rocket station |
| 2 | DSMS PROF → Delivery Mode: **CCIP** |
| 3 | Fuze: **NOSE / INST** |
| 4 | **AHCP:** MASTER ARM → **ARM** (over target area) |

---

## Part 1 — GAU-8/A Avenger Cannon

### Profile A: Medium-Angle Strafe (Anti-Armor)

```
         Perch: 8,000–10,000 ft AGL
              ↓ Roll in (nose toward target)
         Dive: 20–30°, 350 KIAS
              ↓ [PAC pipper stabilized on target]
         Open fire: ~6,000 ft slant range
         Burst: 1–2 seconds
              ↓
         Cease fire: 4,000 ft slant range
         Recover: 3,000 ft AGL — 3–4 G pull
              ↓
         Jink left or right during pull-off
              ↓
         Reset for next pass
```

**Step-by-Step:**

| Step | Action |
|---|---|
| 1 | Fly to **perch position**: 8,000–10,000 ft AGL, 2–3 nm offset from target, 350 KIAS |
| 2 | **AHCP:** MASTER ARM → ARM; GUN/PAC → GUNARM |
| 3 | Verify PAC reticle on HUD; "GUN" annunciation |
| 4 | **Roll in** toward target — roll ~135°, pull nose through horizon, roll wings-level in the dive |
| 5 | Establish **20–30° dive angle**; throttle to idle to prevent overspeed |
| 6 | Place PAC reticle **on target** — track steadily for 1–2 seconds before firing |
| 7 | **Squeeze trigger** — 1–2 second burst |
| 8 | **Begin pull-off** — do NOT wait for the recovery altitude to arrive; initiate recovery early |
| 9 | **4 G pull** — recover to 3,000 ft AGL minimum |
| 10 | **Jink** during pull-off (vary egress heading ±30°) |
| 11 | Climb back to perch; reset for next pass |
| 12 | After last pass: **MASTER ARM → SAFE; GUN/PAC → SAFE** |

### Profile B: Shallow Strafe (Soft Targets)

```
         Entry: 3,000–5,000 ft AGL, 300–350 KIAS
              ↓ Shallow dive 5–15°
         Open fire: ~8,000 ft slant
         Burst: 1–2 seconds
              ↓
         Recover: 1,500 ft AGL minimum
```

| Parameter | Value |
|---|---|
| Entry Altitude | 3,000–5,000 ft AGL |
| Entry Airspeed | 300–350 KIAS |
| Dive Angle | 5–15° |
| Open Fire Range | ~8,000 ft slant |
| Cease Fire / Recover | 1,500 ft AGL minimum |

**Best against:** Troop concentrations, vehicle convoys, soft-skin targets, AAA positions.

### Event Sequence — Gun Passes

Minimum **4 gun passes** required:
- [ ] **Pass 1:** Medium-angle strafe profile — instructor observing recovery altitude and burst discipline
- [ ] **Pass 2:** Medium-angle strafe — student selects target independently
- [ ] **Pass 3:** Shallow strafe profile — soft target
- [ ] **Pass 4:** Student choice of profile — demonstrate competency

---

## Part 2 — Hydra 70 Rockets (M151 HE)

### Standard Rocket Attack Profile

```
         Entry: 8,000–12,000 ft AGL, 300–350 KIAS
              ↓ Roll in — establish dive
         Dive: 15–30°, 300–350 KIAS
              ↓ [CCIP pipper on target]
         Fire: single or ripple burst
              ↓
         Recover: 2,000 ft AGL minimum
```

| Parameter | Value |
|---|---|
| Entry Altitude | 8,000–12,000 ft AGL |
| Entry Airspeed | 300–350 KIAS |
| Dive Angle | 15–30° (steeper = more accurate) |
| Maximum Accurate Range | ~2 km slant from stabilized dive |
| Minimum Pull-Off Altitude | **2,000 ft AGL** |
| Salvo Size | 1–4 rockets per trigger press |

**Technique:**

| Step | Action |
|---|---|
| 1 | DSMS: M151 rockets selected; CCIP mode; quantity set |
| 2 | Master Arm → ARM |
| 3 | Fly to perch: 8,000–12,000 ft AGL, 2–3 nm offset |
| 4 | Roll in; establish 15–30° dive |
| 5 | **CCIP pipper drifts toward target** — wait for it to stabilize |
| 6 | When pipper is on target and stable: **press and hold pickle** |
| 7 | Observe rocket impacts; note correction for next pass |
| 8 | Pull off at **2,000 ft AGL minimum** |
| 9 | Jink egress heading |
| 10 | After last pass: MASTER ARM → SAFE |

> **Pipper Lead:** The CCIP pipper automatically accounts for rocket ballistics. Place the pipper on the center of the target, not where you think the rockets will go. Trust the system.

### Event Sequence — Rocket Passes

Minimum **4 rocket passes** required:
- [ ] **Pass 1:** Instructor demonstration pass with commentary
- [ ] **Pass 2:** Student fires at stationary vehicle target — assessment
- [ ] **Pass 3:** Student fires at area target (vehicle group) — ripple salvo (4 rockets)
- [ ] **Pass 4:** Student choice of profile — demonstrate competency and accuracy

---

## Part 3 — Target Marking (M274 WP)

The Hydra 70 M274 WP (White Phosphorus) is used to mark targets for follow-on attackers or JTACs who need a visual reference. In CAS, "smoke the target" is a common JTAC request when no TGP or LASER is available.

### WP Marking Profile

| Parameter | Value |
|---|---|
| Delivery | Same CCIP dive profile as M151 HE |
| Dive Angle | 10–20° (shallower improves accuracy for area marking) |
| Desired Impact | **Upwind of target** — smoke drifts over the target |
| Communication | Call "SMOKE" or "MARKING" before firing; "SPLASH" when impacts |

**Technique:**
1. Coordinate with "JTAC" (instructor acting as ground controller) — confirm mark is requested.
2. Identify wind direction (check DCS weather or smoke from prior impacts).
3. **Aim for the upwind side** of the target — smoke drifts downwind onto the target.
4. Fire 2–4 WP rockets to create a visible smoke column.
5. Call **"SPLASH"** on radio when rockets impact.
6. "JTAC" confirms mark and clears follow-on attack.

### Event Sequence — Marking Pass

- [ ] **Pass 1:** Student fires WP mark; instructor assesses wind correction and communication

---

## Completion Standards

| Item | Standard |
|---|---|
| **Gun — hit rate** | At least **1 confirmed hit per pass** across ≥ 3 of 4 gun passes |
| **Gun — recovery altitude** | Never below 3,000 ft AGL (medium) or 1,500 ft AGL (shallow) on any pass |
| **Gun — burst discipline** | All bursts ≤ 2 seconds; no sustained fire |
| **Rockets — accuracy** | ≥ 2 of 4 passes impact within **50 m** of target |
| **Rockets — recovery altitude** | Never below 2,000 ft AGL on any pass |
| **WP mark** | Mark placed upwind; "SPLASH" called correctly; JTAC confirms |
| **Arming sequence** | Master Arm ARM before first pass; SAFE after last pass — no exceptions |
| **DSMS setup** | Student configures all weapons independently (no instructor prompting) |

---

## Common Errors

| Error | Correction |
|---|---|
| **Firing bursts > 2 seconds** | Brief "1-2 seconds max" pre-flight. If student exceeds, issue a correction immediately after the pass. |
| **Breaking below minimum altitude** | Hard floor — if broken, automatic DOWN. No exceptions, no explanations. |
| **Pipper on target but aircraft not stable** | "Track, track, pickle." Pipper must be on target AND stable for at least 1 second before firing. |
| **Speed loss from recoil not anticipated** | Brief the math: "You enter at 350. Two-second burst costs 15 kts. You need 300 at recovery to pull 4 G. Plan for it." |
| **GUN/PAC switch in SAFE** | No firing will occur. Students miss this under stress. Verify "GUN" on HUD before each pass. |
| **Rocket pipper not settled before firing** | Pipper swings wide if aircraft not in stable dive. Establish dive, allow pipper to settle, THEN fire. |
| **Not setting DSMS for rocket type** | Student switches from gun to rockets but leaves gun selected on DSMS — no rounds fire. Always verify DSMS selection. |
| **WP mark downwind of target** | Smoke drifts away from target. Brief wind check before every marking pass. |

---

[← Event 1: Academics](event-1-academics.md) | [→ Event 3: Unguided & Cluster Munitions](event-3-bombs.md)

---

*Based on T.O. 1A-10C-34-1-1 and Eagle Dynamics DCS A-10C/II documentation. For simulation use only.*
