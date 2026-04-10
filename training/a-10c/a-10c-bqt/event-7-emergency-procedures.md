# Event 7 — Emergency Procedures

> **Course:** A-10C Basic Qualification Training | **Event Type:** Flight (Simulated Emergencies)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Boldface Review](#boldface-review)
4. [Part 1 — Single-Engine Failure](#part-1--single-engine-failure)
5. [Part 2 — Engine Fire](#part-2--engine-fire)
6. [Part 3 — Hydraulic Failures](#part-3--hydraulic-failures)
7. [Part 4 — Electrical Failures](#part-4--electrical-failures)
8. [Part 5 — Ejection Criteria](#part-5--ejection-criteria)
9. [Part 6 — Emergency Landing](#part-6--emergency-landing)
10. [Completion Standards](#completion-standards)
11. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Recite all 5 boldface emergency procedures verbatim from memory
- [ ] Identify and correctly diagnose a simulated single-engine failure
- [ ] Execute the single-engine operating procedure and fly to a safe landing
- [ ] Identify the signs of an engine fire and execute the Engine Fire procedure
- [ ] Understand the effect of Hydraulic A, B, and dual failure on aircraft control
- [ ] Configure the aircraft for manual reversion flight and execute a landing
- [ ] Identify the criteria for immediate ejection without hesitation

---

## Ground Brief

### Emergency Philosophy

> **Boldface items are to be executed FROM MEMORY, immediately, without reference to any checklist. Non-boldface items may be accomplished using the appropriate checklist.**
>
> The boldface procedures exist because any delay in executing them means the emergency has already exceeded the safe window for recovery.

### Overview of Emergencies Covered

| Emergency | Boldface | Sim Method |
|---|---|---|
| Abort | Yes | Ground only (conceptual review) |
| Single-engine failure | No | Instructor cuts throttle mid-flight |
| Engine fire | Yes | Instructor activates fire light simulation |
| HYD A failure | No | Instructor failure via DCS mission editor |
| HYD B failure | No | Instructor failure via DCS mission editor |
| HYD A + B (Dual) | Yes (Manual Reversion) | Instructor failure |
| Double generator failure | No | Instructor failure |
| Ejection criteria | Yes | Q&A ground only |

---

## Boldface Review

Before every flight event, the student must recite all 5 boldface procedures from memory. This event emphasizes them in context.

### 1. Abort (Ground)

> **Throttles — IDLE**
> **Brakes — APPLY (maximum)**
> **Drag Chute — DEPLOY** (if equipped / if runway insufficient)
> **If fire** — Throttles OFF; emergency shutdown

### 2. Engine Fire (Inflight)

> **Affected throttle — OFF**
> **Fire Handle — PULL**
> **Halon Discharge — PRESS** (first shot)
> **If fire persists 30 sec — Second Discharge**
> **Emergency Procedures — ACCOMPLISH**

### 3. Double Engine Failure (Inflight)

> **Throttles — IDLE** (both)
> **APU — START** (if available; powers avionics)
> **Best glide speed — ESTABLISH** (approx. 170–190 KIAS clean)
> **Airstart — ATTEMPT** (one engine per the Airstart checklist)
> **If no airstart by safe altitude — EJECT**

### 4. Manual Reversion (HYD A + B Dual Failure)

> **EFC switch — MAN REVERSION** (Emergency Flight Computer switch, left console)
> **Flight controls — CHECK** (verify control response in manual reversion)
> **Speed — REDUCE** to recommended speed (reduce to < 200 KIAS; control forces increase)
> **Land as soon as possible**

### 5. Ejection

> **If directed or criteria met:**
> **Throttles — IDLE**
> **Canopy** — JETTISON (optional; auto with ejection)
> **Ejection Handle — PULL** (between legs or above head)

---

## Part 1 — Single-Engine Failure

### Recognition Signs

| Indication | Explanation |
|---|---|
| N1 decrease on one engine | Compressor slowing; engine losing thrust |
| Torque mismatch | Yaw toward failed engine; rudder input required |
| ITT decrease on failed engine | Engine cooling without combustion |
| Generator offline (one side) | Loss of associated electrical bus |
| Warning light: ENG L (or R) | Engine warning light on caution panel |

### Single-Engine Operating Procedure (Non-Boldface)

| Step | Action |
|---|---|
| 1 | Identify failed engine: *"Left/Right engine failed"* — confirm on instruments |
| 2 | Throttle (failed engine) — IDLE (do not shut down unless fire) |
| 3 | Rudder — apply toward **good engine** side; maintain heading |
| 4 | Power (good engine) — advance as required; do not exceed ITT/N1 limits |
| 5 | Check fuel: cross-feed may be required if fuel imbalance develops |
| 6 | Declare emergency; land as soon as practical |
| 7 | If airstart possible (engine not on fire): attempt airstart on failed engine per checklist |

### Single-Engine Performance Data

| Condition | Performance |
|---|---|
| Single engine (one engine idle) | Maintains level flight at reduced power |
| Single engine (one engine OFF) | Can maintain flight; reduced service ceiling |
| Service ceiling (single engine) | ~25,000–30,000 ft (one engine) |
| Takeoff (single engine) | **Not recommended** — identify on roll; abort |
| Landing (single engine) | Higher than normal glidepath preferred; avoid overshoot |

### Single-Engine Approach Notes

- Fly a **wider pattern** than normal — the aircraft cannot accelerate quickly if approach is too slow
- Maintain **final speed at minimum 135 KIAS** — do not allow speed to decay
- **Go-around on single engine:** possible but energy-limited; make the decision early
- Single-engine go-around from < 100 ft AGL: questionable — land if safely on runway

### Airstart Procedure (Summary)

| Step | Action |
|---|---|
| 1 | Affected throttle — OFF |
| 2 | Airspeed — **230–270 KIAS** (windmill start range) |
| 3 | Affected throttle — advance to **IDLE** |
| 4 | Observe IGN light; N2 rising; ITT rising |
| 5 | If ITT rises normally — throttle to desired power |
| 6 | If no start in 30 seconds — ABORT airstart; throttle OFF |

> **DCS Note:** TF34 engines in DCS windmill start reliably between 230–270 KIAS at altitudes below 25,000 ft. Above that altitude, assisted start (APU or cross-bleed) may be required and is not modeled in all mission contexts.

---

## Part 2 — Engine Fire

### Engine Fire Indications

| Indication | Source |
|---|---|
| **FIRE warning light** (red) — L or R engine | Fire detector loop — heat sensor in engine bay |
| Overheat warning | ENG OVERHEAT caution |
| Abnormal ITT rise | Fuel-fed fire |
| Visible smoke/flame (external) | Observed from wingman or ground |

### Engine Fire Procedure (Boldface — execute from memory)

| Step | Action | Notes |
|---|---|---|
| 1 | **Affected throttle — OFF** | Remove fuel source |
| 2 | **Fire Handle — PULL** | Arms the Halon system; confirms fire |
| 3 | **HALON DISCHARGE — PRESS** (first shot) | Discharges Halon into engine bay |
| 4 | Wait **30 seconds** | Halon must extinguish fire |
| 5 | If FIRE light **extinguishes** | Fire out; single-engine landing; declare emergency |
| 6 | If FIRE light **remains** | Second shot: press HALON DISCHARGE again |
| 7 | If FIRE light **still remains** | **Eject** |

> **DCS Note:** DCS models fire detection and Halon discharge. The fire light will extinguish on first shot in most scenarios. Second shot failure → the aircraft is not recoverable — eject criteria apply.

---

## Part 3 — Hydraulic Failures

### Hydraulic System Architecture

The A-10C has **two independent hydraulic systems**: HYD A and HYD B. Both must fail before manual reversion becomes necessary.

| System | Powers |
|---|---|
| **HYD A** | Primary flight controls (elevator, rudder, ailerons — primary); gear; brakes |
| **HYD B** | Secondary flight controls (elevator, rudder, ailerons — secondary); flaps; speedbrakes |
| **Both (dual)** | Manual reversion (degraded control forces) |

### HYD A Failure (Non-Boldface)

| Indication | HYD A PRESS caution light |
|---|---|
| Effect | Reduced control authority; controls feel heavier |
| Procedure | Maintain altitude; do not maneuver aggressively; land as soon as practical |
| Landing | Normal pattern; avoid heavy braking (HYD B brakes still available) |

### HYD B Failure (Non-Boldface)

| Indication | HYD B PRESS caution light |
|---|---|
| Effect | Flaps inoperative; speed brakes inoperative |
| Procedure | No flap extension; approach at higher speed (~150 KIAS minimum); land long |
| Landing | Higher approach speed; longer rollout; plan for no speed brakes |

### HYD A + B Dual Failure — Manual Reversion (Boldface)

| Indication | Both HYD PRESS lights; control forces increase dramatically |
|---|---|
| Effect | No powered flight controls; pilot must move control surfaces against aerodynamic loads manually |

**Manual Reversion Procedure:**

| Step | Action |
|---|---|
| 1 | **EFC Switch — MAN REVERSION** (left console) |
| 2 | Verify flight controls respond (expect heavy forces) |
| 3 | **Reduce speed to < 200 KIAS** — control forces manageable below 200 KIAS |
| 4 | Avoid steep banks or aggressive maneuvers |
| 5 | Declare emergency; land as soon as possible |
| 6 | Landing: **no flaps; no speed brakes** — extended rollout required |
| 7 | Approach speed: **175–180 KIAS** (no flap approach) |
| 8 | **Long runway** preferred — rollout may exceed 8,000 ft |

> **Handling note:** In DCS, manual reversion is modeled with increased control forces. The aircraft is flyable but sluggish. Students should practice at altitude before attempting an approach.

---

## Part 4 — Electrical Failures

### Electrical System Overview

| Bus | Source | Powers |
|---|---|---|
| Essential DC | Battery + both generators | Minimum required systems (instruments, EGI backup) |
| Left main AC | Left generator | Left MFD, left hydraulic controls |
| Right main AC | Right generator | Right MFD, CDU, IFFCC |

### Double Generator Failure (Non-Boldface)

| Indication | Both GEN caution lights; MFDs fail |
|---|---|
| Effect | Aircraft reverts to battery/inverter power; limited instruments |
| Procedure | **APU GEN ON** immediately; restores essential AC power |
| If APU fails | Standby instruments only (standby attitude, airspeed, altimeter) |

### Procedure for Double Generator Failure

| Step | Action |
|---|---|
| 1 | Identify: both GEN caution lights |
| 2 | **APU — START** |
| 3 | **APU GEN — ON** |
| 4 | Verify essential AC restored |
| 5 | Attempt to reset failed generators (RESET switch) |
| 6 | If no restore: fly on standby instruments; declare emergency; land |

### Flying on Standby Instruments

| Instrument | Provides |
|---|---|
| Standby attitude indicator | Pitch and roll |
| Standby airspeed | Indicated airspeed |
| Standby altimeter | Altitude (barometric) |
| Magnetic compass | Heading (uncorrected) |

> **IFR on standby instruments is extremely demanding.** Land VFR if at all possible. If IMC, the standby instruments are sufficient for a precision ILS only if the student is trained in partial-panel flying.

---

## Part 5 — Ejection Criteria

### Ejection Decision — Immediate Ejection Criteria

The following conditions require **immediate ejection without hesitation**:

| Condition | Rationale |
|---|---|
| Uncontrolled flight / departure from controlled flight below 10,000 ft AGL | Recovery time insufficient |
| Both engines failed; airstart failed; below safe ejection altitude | No other option |
| Engine fire; both Halon shots failed; fire light still on | Aircraft will be destroyed |
| Structural failure / loss of flight controls | Unrecoverable |
| Controlled flight into terrain (CFIT) imminent | Insufficient altitude to maneuver |

### Ejection Altitude Minimums

| Maneuver | Minimum Altitude AGL |
|---|---|
| Straight-and-level ejection | **500 ft AGL** |
| Turning ejection | **1,000 ft AGL** |
| Inverted ejection | **2,000 ft AGL** (seat fires downward; very high risk) |
| Zero-altitude / zero-speed (ground) | Capable — ACES II seat is rated zero-zero |

### Ejection Procedure (Boldface)

| Step | Action |
|---|---|
| 1 | Throttles — IDLE |
| 2 | Aircraft — wings level if possible |
| 3 | Canopy jettison (optional — auto with ejection initiation) |
| 4 | **Pull ejection handle** — between legs or overhead handle |

### The Human Factor

> *"A decision to eject is never wrong if the aircraft cannot be safely recovered. A pilot who ejects from a recoverable aircraft survives to fly again. A pilot who delays ejection from an unrecoverable aircraft often does not."*
>
> Drill the ejection criteria. Know the numbers. The decision must be made before the aircraft reaches the minimum altitude — not at it.

### Q&A Review (Verbally Confirm Before End of Event)

| Question | Answer |
|---|---|
| Minimum altitude for straight ejection? | 500 ft AGL |
| Both Halon shots failed — what do you do? | **Eject** |
| Double engine failure with no successful airstart — criteria met at what altitude? | Student-declared when recovery not possible; must eject before running out of recovery altitude |
| What does the EFC switch MAN REVERSION position do? | Removes hydraulic power from flight controls; pilot moves surfaces manually |
| Single-engine go-around from 50 ft AGL — recommended? | Land if safely on runway; go-around has high risk at that height on single engine |

---

## Part 6 — Emergency Landing

After simulated emergencies, the student lands with at least one complication in effect:

### Option A: Single-Engine Full-Stop Landing

- Wider pattern; higher approach speed (135 KIAS minimum)
- No touch-and-go
- Apply power early on final to avoid low-energy trap
- Full-stop rollout; do not taxi for extended distance (potential runway foaming required in real world)

### Option B: Manual Reversion No-Flap Landing

- Approach at **175–180 KIAS**
- No speed brakes
- Long runway; extended rollout
- Braking: maximum braking available; anticipate brake heating
- NWS may be degraded — use differential braking for directional control

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Boldface recitation | All 5 procedures verbatim, < 30 seconds each, no prompting |
| Single-engine ID | Correct engine identified within 10 seconds; appropriate rudder applied |
| Engine fire procedure | Steps 1–3 in correct order; verbalized; no hesitation |
| Manual reversion | EFC switch selected; speed reduced; landing accomplished |
| Electrical failure | APU GEN ON within 20 seconds of double-generator light |
| Ejection criteria Q&A | All 5 criteria questions answered correctly |
| Emergency landing | Stabilized approach; touchdown within first 2,000 ft (no-flap); no runway excursion |

---

## Common Errors

| Error | Correction |
|---|---|
| Cutting wrong engine on single-engine ID | "Confirm — dead foot, dead engine." Rudder pressure tells you which side has lost thrust. |
| Forgetting to pull fire handle | Fire handle must be pulled to arm Halon. Announce it: "Fire handle — pulled." |
| Not reducing speed in manual reversion | Above 200 KIAS, control forces are extreme. Slow down FIRST. |
| Hesitating on ejection Q&A | There should be zero hesitation on ejection criteria. Drill until it is automatic. |
| Approaching too fast on single-engine | Faster approach = more runway required. Use AoA indexer even on single-engine approach. |
| Double generator → not starting APU immediately | APU is the primary backup power source. It should be the first thought on double-generator failure. |

---

[← Event 6: Traffic Pattern](event-6-traffic-pattern.md) | [→ Event 8: Check Ride](event-8-check-ride.md)

---

*Based on T.O. 1A-10C-1, AFMAN 11-2A-10C Vol 3, and Eagle Dynamics DCS A-10C documentation. For simulation use only.*
