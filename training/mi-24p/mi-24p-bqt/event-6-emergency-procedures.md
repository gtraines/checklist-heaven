# Event 6 — Emergency Procedures

> **Course:** Mi-24P Hind Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [In-Sim Procedures](#in-sim-procedures)
4. [Completion Standards](#completion-standards)
5. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Recite and execute all boldface emergency procedures from memory without hesitation
- [ ] Simulate a single-engine failure: identify the failed engine, perform boldface, transition to single-engine flight
- [ ] Execute a practice power-off autorotation to a safe recovery (no actual engine shutdown required in DCS)
- [ ] Demonstrate the correct response to simulated tail rotor failure at cruise speed
- [ ] Describe (and where DCS permits, simulate) hydraulic and electrical failure procedures
- [ ] Correctly identify ground resonance onset and execute the immediate action decision
- [ ] Demonstrate LTE recovery technique

---

## Ground Brief

### Emergency Philosophy — The Mi-24P Advantage and Responsibility

The Mi-24P's twin engines provide a significant survival advantage over single-engine helicopters. However, this advantage comes with a responsibility:

- **Single-engine failure** is NOT an automatic autorotation — identify, secure, fly single-engine
- **Dual-engine failure** IS an autorotation — but the Mi-24P descends very fast (15–20 m/s vs. 5–8 m/s for light helicopters)
- **Time available** is still limited. Boldface is still mandatory. Hesitation costs lives.

### The "5 Ts" — Emergency Decision Framework

Teach students this framework for any emergency:

| T | Action |
|---|---|
| **Terrain** | Where are we? What landing options exist? |
| **Time** | How much time do we have? Immediate → boldface. Time available → checklist. |
| **Troops** | Who/what is on board? Any implications? |
| **Tell** | Declare emergency (Mayday). Coordinate with ATC/wingmen. |
| **Terminate** | If required — controlled termination (emergency landing, egress) |

### Practice Autorotation vs. Real Autorotation

In DCS, practice autorotations are conducted by:
1. Reducing collective to minimum
2. Simulating engine failure by managing collective only (engines still running but collective at floor)
3. Flying the autorotation profile
4. At 20–30 m AGL — applying power (collective) to simulate the recovery cushion
5. **NOT** actually shutting down the engines during training

> *This is a key difference from real-world Mi-24P training, where actual engine flameouts were practiced at altitude. In DCS single-player, the engine failure simulation using idle power + collective floor is the safe alternative. The autorotation flight model is still valid.*

### Mi-24P Autorotation Warning

The Mi-24P autorotation descent rate (**15–20 m/s**, ~3,000–4,000 ft/min) is significantly higher than light helicopters. This is caused by:
- High aircraft gross weight
- Stub wings adding drag (not converting to useful lift in autorotation)
- High disk loading (small rotor area relative to weight)

The flare and cushion timing is **more critical** and the margin for error is **smaller** than in light helicopters. Practice at altitude before evaluating at lower altitudes.

---

## In-Sim Procedures

### Exercise 1 — Boldface Oral Recitation (Pre-Flight / In-Sim)

Before any flying, the student will recite all 5 boldface items from memory. The instructor will prompt with the emergency title only.

| Emergency | Student Must Recite |
|---|---|
| Engine failure in flight (single) | Steps 1–6 in order, verbatim |
| Dual engine failure / autorotation | Steps 1–7 in order, verbatim |
| Engine fire | Steps 1–4 in order, verbatim |
| Ground resonance | Both sub-cases: Nr ≥ 90% and Nr < 90% |
| Tail rotor failure | Steps 1–4 in order, verbatim |

**Pass criterion:** All 5 boldface items recited correctly without hesitation or prompting. Any item failed → student re-studies and re-tests before flight.

### Exercise 2 — Single-Engine Failure Simulation

**Setup:** Fly at 300 m, 180 km/h. Instructor announces "simulated left engine failure — execute boldface."

| Step | Student Action | Standard |
|---|---|---|
| 1 | **COLLECTIVE** — maintain Nr 95% | Nr stays 92–98% |
| 2 | **RIGHT ENGINE** — increase power to torque ≤ 95% | Does not exceed 95% transient limit |
| 3 | **Airspeed** — adjust to 120–140 km/h | Minimum single-engine speed |
| 4 | **Identify failed engine** — left EGT, torque, Nr contribution all low | Verbalize: "Left engine" |
| 5 | **Left fuel cutoff lever** — verbalize "Left fuel cutoff OFF" (do not actually pull in DCS sim) | Instructor confirms verbal procedure |
| 6 | **Declare emergency** — "Mayday, Mayday, [callsign], single engine, intentions..." | |
| 7 | **Fly single-engine profile** — 120–140 km/h, torque ≤ 85% on operative engine | |
| 8 | **Plan immediate landing** — nearest suitable surface | |

**Instructor re-starts:** After the simulation, instructor confirms both engines healthy before continuing.

**Key teaching point:** Single-engine torque limit is **85% continuous, 95% transient for 5 seconds**. Do not exceed this — the operative engine can be overloaded if the student pulls too much power.

### Exercise 3 — Practice Autorotation

**Setup:** Fly at 600 m, 170 km/h, over a clear area with an identified touchdown point.

| Step | Student Action | Standard |
|---|---|---|
| 1 | Instructor announces "Practice autorotation — execute" | |
| 2 | **COLLECTIVE** — FULL DOWN (immediately) | Nr rises into 95–100% range |
| 3 | **Airspeed** — 170 km/h | Best autorotation speed |
| 4 | **Nr** — monitor 89–105% range | No Nr exceedance |
| 5 | **Verify descent rate** — 15–20 m/s (3,000–4,000 ft/min) | Expected for Mi-24P |
| 6 | **At 50–30 m AGL** — BEGIN FLARE | Raise nose to arrest descent rate |
| 7 | **Flare effect:** descent rate reduces, Nr increases | Use Nr energy to arrest descent |
| 8 | **At 5–8 m AGL** — LEVEL aircraft | Forward cyclic to arrest flare |
| 9 | **COLLECTIVE PULL** — cushion the landing | Pull smoothly to arrest remaining descent |
| 10 | **POWER RECOVERY** (DCS training): Add power at 10 m and fly away | Practice recovery, not actual touchdown |

**Altitude split for training:**
- First 2 practice autorotations: power recovery at 50 m (just entering the flare)
- Next 2: power recovery at 20 m (completing the flare)
- Final: power recovery at 10 m (completing through cushion phase)

> *Do not attempt a full no-power touchdown in DCS without instructor briefing — the Mi-24P's high descent rate makes the flare timing critical and a hard landing will damage the aircraft.*

### Exercise 4 — LTE Recognition and Recovery

**Setup:** Establish a hover or very slow flight (< 30 km/h) at 10 m. Instructor applies wind from the right-front sector using DCS weather or mission editor.

| Step | Action | Notes |
|---|---|---|
| 1 | Student hovering; simulated LTE onset | Yaw begins to develop unexpectedly |
| 2 | **Recognize:** Uncommanded right yaw | "LTE onset — uncommanded right yaw" |
| 3 | **Apply right pedal** | Reduce anti-torque to allow engine to stop yaw |
| 4 | **Forward cyclic** — gain airspeed | Airspeed = authority over yaw |
| 5 | **At 50+ km/h** — yaw recoverable with left pedal again | Directional stability restored |
| 6 | Climb to safe altitude, recover | |

**Key teaching point:** Do NOT apply left pedal to fight the yaw — this applies more anti-torque, which feeds the LTE. The counterintuitive recovery (right pedal + airspeed) must be drilled.

### Exercise 5 — Ground Resonance Recognition (Ground Exercise)

**Setup:** On the ground, rotor running, pre-takeoff check complete.

The instructor will brief this as a recognition and decision exercise — not an actual induced resonance (which would destroy the aircraft).

| Scenario A | Nr ≥ 90% — decision: FLY |
|---|---|
| **Student response:** | "Increasing vibration — ground resonance onset — Nr [read value] ≥ 90% — FLY AWAY" |
| **Action:** | Collective UP — become airborne immediately |

| Scenario B | Nr < 90% — decision: SHUT DOWN |
|---|---|
| **Student response:** | "Increasing vibration — ground resonance onset — Nr [read value] < 90% — SHUT DOWN" |
| **Action:** | Fuel cutoffs OFF, collective full DOWN, evacuate |

Instructor drills this as a **verbal decision exercise** from ground position. Student states Nr, states decision, states actions.

### Exercise 6 — Hydraulic Failure Simulation

**Setup:** At 300 m, 180 km/h, trimmed level. Instructor announces "Simulated main hydraulic failure."

| Step | Student Action | Notes |
|---|---|---|
| 1 | Note increased control forces | Main hydraulic failure — controls heavier |
| 2 | **Autopilot** — OFF | AP requires hydraulic pressure |
| 3 | Fly deliberately — larger, slower inputs | No aggressive maneuvers |
| 4 | **Plan landing** — nearest suitable airfield | Do not delay |
| 5 | Brief: if backup also fails — controls extremely heavy; immediate landing required | |

> *⚠ DCS Note: DCS models hydraulic failure with increased control force. The student should practice flying with deliberate, slow inputs even without an actual hydraulic failure, to develop muscle memory.*

### Exercise 7 — Electrical Failure Simulation

**Setup:** At 300 m, 180 km/h. Instructor announces "Simulated right generator failure."

| Step | Student Action | Notes |
|---|---|---|
| 1 | Note caution light — generator failure | One generator offline |
| 2 | Reduce non-essential electrical loads | APU-powered systems, non-essential lights |
| 3 | Monitor remaining generator load | |
| 4 | Land as soon as practical | Do not delay with single generator |

**If dual generator failure briefed:**
| Step | Student Action |
|---|---|
| 1 | Battery bus only — ~20 min endurance |
| 2 | All non-essential loads OFF immediately |
| 3 | Attempt APU restart in flight (if time permits) |
| 4 | Land IMMEDIATELY |

---

## Completion Standards

| Standard | Requirement |
|---|---|
| **Boldface recitation** | All 5 items recited verbatim without prompting before flight |
| **Single-engine failure** | All 6 steps executed correctly; failed engine identified; airspeed within 120–140 km/h |
| **Autorotation — Nr** | Nr maintained 89–105%; no Nr exceedance throughout |
| **Autorotation — airspeed** | 170 km/h ±15 km/h during steady autorotation |
| **Autorotation — flare** | Initiated between 30–50 m AGL; descent rate visibly arrested |
| **LTE recovery** | Correct recovery initiated within 3 seconds of onset; airspeed gained |
| **Ground resonance decision** | Correct decision (fly vs. shut down) stated within 2 seconds; correct actions stated |
| **Hydraulic failure** | AP off; deliberate control technique; landing planned |

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| Autorotating immediately on single-engine failure | Unnecessary autorotation; abandons flyable aircraft | "Single engine = fly. You have a second engine. Use it. Autorotate only on DUAL failure" |
| Nr exceedance during autorotation | Rotor overspeed damage | "Collective is your Nr control. Too low collective = Nr too high. Raise collective slightly to regulate" |
| Late flare in autorotation | High descent rate at touchdown; hard landing | "The Mi-24P descends FAST. Flare at 30–50 m, not 10 m. You are heavier than anything you've flown" |
| Applying left pedal on LTE onset | Feeds the yaw; loss of control | "LTE recovery is counterintuitive. RIGHT pedal + forward cyclic. Drill this until it's automatic" |
| Hesitating on ground resonance decision | 3–5 seconds to destruction | "In resonance you have no time. Pre-brief the decision. Know your Nr. Act before thinking" |
| Not declaring emergency | No priority handling; no search and rescue activated | "Every emergency is a Mayday. Say it. ATC can always stand you down if you recover" |

---

*Based on Mi-24P RLE and Eagle Dynamics DCS World Mi-24P Hind module documentation. For simulation use only.*
