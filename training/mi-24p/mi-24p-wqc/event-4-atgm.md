# Event 4 — ATGM Employment (Shturm & Ataka)

> **Course:** Mi-24P Hind Weapons Qualification Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Shturm System Data](#shturm-system-data)
4. [Ataka System Data](#ataka-system-data)
5. [SACLOS Guidance Principles](#saclos-guidance-principles)
6. [WSO Guidance Technique](#wso-guidance-technique)
7. [Pilot Flight Profile During Guidance](#pilot-flight-profile-during-guidance)
8. [Employment Profiles](#employment-profiles)
9. [Warhead Selection](#warhead-selection)
10. [Shturm vs. Ataka Decision](#shturm-vs-ataka-decision)
11. [In-Sim Procedures](#in-sim-procedures)
12. [Common Errors](#common-errors)
13. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Explain SACLOS guidance principles and the WSO's role throughout missile time-of-flight
- [ ] Execute WSO tracking technique — track target, not missile, throughout guidance
- [ ] Demonstrate pilot flight profile requirements during SACLOS guidance phase
- [ ] Execute Shturm and Ataka engagement sequences using DCS cockpit controls
- [ ] Select Shturm vs. Ataka based on target range, type, and threat environment
- [ ] Select appropriate Ataka warhead variant (HEAT vs. thermobaric) for target type
- [ ] Execute single-player seat-switching during ATGM engagement without guidance loss
- [ ] Coordinate crew calls for ATGM employment: ready, firing, guiding, splash/miss

---

## Ground Brief

### The Fundamental ATGM Problem

Both ATGMs in the Mi-24P's inventory — Shturm and Ataka — share the same guidance method: **SACLOS (Semi-Automatic Command to Line-Of-Sight)**. This method is powerful (range up to 6 km, precision to within 1 meter CEP) but unforgiving. During the missile's entire flight:

- **The WSO must keep the PKV-1 crosshair on the target** — any deviation becomes an error command to the missile
- **The Pilot must hold steady flight** — aircraft maneuvering displaces the sight line, sending false commands
- **Neither crewmember can break their task** — the missile will miss if either breaks discipline

This mutual commitment during the guidance phase — up to 15 seconds for a Shturm at max range — is the defining challenge of Mi-24P weapons employment.

### ATGM Priority Hierarchy

| Scenario | ATGM Use | Alternative |
|---|---|---|
| MBT at 2,000+ m | **Required** — only weapon with reliable kill | None (cannon ineffective frontally) |
| MBT at <400 m | **Not possible** — below minimum range | Cannon (flank/rear) or break off |
| AAA in threat environment | **Preferred** — maintains standoff | Rockets (if threat environment permits) |
| Multiple soft targets | **Avoid** — expensive; conserve | Rockets or cannon |

---

## Shturm System Data

| Specification | Value | Notes |
|---|---|---|
| **Designation** | 9M114 Shturm (Storm) | NATO: AT-6 Spiral |
| **Guidance** | Radio-command SACLOS | Semi-automatic command to line-of-sight |
| **Warhead** | HEAT shaped charge | 600+ mm RHAe penetration |
| **Warhead Weight** | 5.4 kg | |
| **Missile Weight** | 31 kg | |
| **Min Range** | 400 m | Guidance stabilization distance |
| **Max Range** | 5,000 m | Radio command effective range |
| **Optimal Range** | 1,500–4,000 m | Best accuracy window |
| **Missile Velocity** | 350 m/s average | Variable through flight |
| **Time of Flight (max range)** | ~15 seconds | Maximum WSO guidance duration |
| **Launcher** | APU-68UM rail | 2 missiles per outer pylon |
| **Max Carried** | 4 missiles (2 per outer station) | |

---

## Ataka System Data

| Specification | Value | Improvement vs. Shturm |
|---|---|---|
| **Designation** | 9M120 Ataka (Attack) | NATO: AT-9 Spiral-2 |
| **Guidance** | Radio-command SACLOS (improved algorithm) | Better guidance fidelity |
| **Min Range** | 400 m | Same |
| **Max Range** | 6,000 m | +1,000 m (20% further) |
| **Optimal Range** | 2,000–5,000 m | Extended envelope |
| **Missile Velocity** | 400–550 m/s | 40–57% faster than Shturm |
| **Time of Flight (max range)** | ~12 seconds | 3 seconds less exposure |
| **Accuracy (CEP)** | ±0.5 m | 50% more accurate than Shturm |
| **Warhead Options** | HEAT (800+ mm) / Thermobaric | Dual-role capability |
| **Missile Weight** | 42 kg | Heavier than Shturm |

### Ataka Warhead Variants

| Variant | Type | Penetration/Effect | Best Targets |
|---|---|---|---|
| **9M120F (HEAT)** | Tandem shaped charge | 800+ mm RHAe | MBTs, heavy armor |
| **9M120F-1 (Thermobaric)** | Fuel-air explosive | Blast/overpressure | Bunkers, buildings, troops |
| **9M120M (Enhanced HEAT)** | Enhanced tandem | 950+ mm RHAe | Modern MBTs with ERA |

> **DCS Note:** Not all warhead variants may be available in your DCS module version. Verify in Mission Editor.

### Thermobaric Warhead — How It Works

| Phase | What Happens | Time |
|---|---|---|
| 1 — Dispersal | Warhead ruptures; fuel aerosol cloud forms (~8–10 m diameter) | 0 ms |
| 2 — Ignition | Detonation wave ignites aerosol cloud | ~100 ms |
| 3 — Blast | Overpressure wave propagates through area (30+ bar in enclosed spaces) | 100–400 ms |
| 4 — Vacuum | Negative pressure phase; oxygen depletion | 400–500 ms |

**Key Properties:** Overpressure propagates around corners and through openings — ideal for bunkers and buildings. Highly effective against personnel regardless of body armor. Not effective against heavy armor.

### Thermobaric vs. HEAT Target Matching

| Target Type | Use HEAT | Use Thermobaric |
|---|---|---|
| **MBT** | ✓ Required | ✗ Ineffective |
| **APC / IFV** | ✓ Effective | ✓ Effective (either works) |
| **Bunker (concrete)** | Structural damage only | ✓ **Primary choice** |
| **Buildings / command posts** | Penetrates only | ✓ **Devastating** |
| **Troops in open** | Overkill | ✓ Area effect advantage |
| **Artillery battery** | Equipment damage | ✓ Personnel + equipment |

---

## SACLOS Guidance Principles

### How SACLOS Works

1. **WSO:** Keeps PKV-1 crosshair on target throughout missile flight
2. **System:** Tracks missile via IR beacon; measures deviation from sight line
3. **Radio Commands:** Transmits corrections to missile automatically
4. **Missile:** Receives commands; adjusts flight path
5. **No Pilot Steering:** Pilot holds steady — no direct missile control

### Platform Stability Requirements

| Parameter | Limit | Consequence of Exceeding |
|---|---|---|
| **Turn rate during guidance** | ≤5°/second | Sight line displacement → guidance error |
| **Altitude change** | ≤20 m per second | Vertical sight displacement → miss |
| **Airspeed change** | ≤20 km/h per second | Attitude change affects sight | 
| **Autopilot** | Engage if available | Without autopilot: single-player guidance is nearly impossible |

---

## WSO Guidance Technique

### The Golden Rule: Track the Target — Not the Missile

The most common student error is looking at the missile and trying to steer it to the target. This is backwards. The SACLOS system steers the missile to wherever the crosshair points — the WSO's only job is to keep the crosshair on the target.

### Pre-Launch Sequence

1. Target Acquisition: PKV-1 on target, magnification 4–6×
2. Range Confirmation: Target within ATGM envelope (>400 m)
3. Weapon Selection: ATGM mode selected; correct missile type (Shturm/Ataka)
4. Sight Stabilization: Smooth tracking established
5. Launch Authorization: Call **"Ready to fire"** to pilot

### Launch and Guidance

| Step | Action | Critical Note |
|---|---|---|
| **Launch** | Press fire button | 0.5–1 sec delay before missile leaves rail |
| **Initial tracking** | Keep crosshair on target | Do NOT look at missile |
| **Guidance phase** | Smooth joystick corrections | Minimal inputs; avoid overcontrol |
| **Missile visible?** | Bright spot in peripheral vision | Ignore it — keep tracking target |
| **Terminal phase** | Maintain track until impact | Hold 3–5 seconds after impact for BDA |

### Guidance Quality Indicators

| Sight Behavior | Likely Outcome | WSO Action |
|---|---|---|
| Crosshair steady on target | Accurate guidance; hit expected | Maintain; no correction needed |
| Crosshair oscillating slightly | Acceptable; minor error | Damp oscillation with small inputs |
| Crosshair drifting off target | Miss likely unless corrected | Smooth correction back to center |
| Target lost (dust/smoke) | Track last known position | Hold steady; avoid random input |

---

## Pilot Flight Profile During Guidance

### Ideal Profile

- Straight and level flight at constant airspeed (160–200 km/h)
- Turn rate <5°/second maximum
- No altitude changes >20 m during missile flight
- Steady power setting; avoid collective changes
- Autopilot engaged (heading + altitude hold) — **essential for single-player**

### Acceptable During Guidance

- Very gentle turns (<3°/second)
- Minor altitude corrections for terrain clearance
- Small power adjustments to maintain airspeed

### Prohibited During Guidance

- Hard turns >10°/second
- Aggressive climbs or dives
- Evasive jinking or random maneuvers
- Autopilot disengagement (unless emergency)

> *⚠ Exception:* If under immediate threat of destruction (missile launch at aircraft), the pilot breaks off regardless — a missed ATGM is better than a lost aircraft.

---

## Employment Profiles

### Profile 1 — Pop-Up Attack (Primary)

Best accuracy; good threat avoidance on approach.

| Phase | Altitude | Airspeed | Actions |
|---|---|---|---|
| **Low-level approach** | 50–100 m AGL | 200–250 km/h | Terrain masking |
| **Pop-up** | Rise to 200–400 m AGL | Reduce to 180 km/h | Gain LOS over terrain |
| **Acquire** | Hold altitude | 160–180 km/h | WSO acquires target |
| **Fire** | Hold steady | Hold airspeed | Launch missile |
| **Guide** | ±20 m altitude hold | ±20 km/h | 8–15 seconds |
| **Break** | Dive to 50 m | Increase speed | After impact or miss |

### Profile 2 — Running Fire (High-Threat Areas)

Less precise but minimizes exposure time.

| Parameter | Value |
|---|---|
| **Altitude** | 100–300 m AGL |
| **Airspeed** | 220–260 km/h |
| **Course** | Straight line 3–5 km |
| **Shots per pass** | 1 (no time for re-engagement) |
| **Post-impact** | Immediate break — no BDA |

### Profile 3 — Hull-Down / Stationary (Deliberate Attack)

Maximum accuracy; requires good terrain concealment.

| Parameter | Value |
|---|---|
| **Position** | Terrain-masked hover or slow taxi |
| **Exposure** | Minimal — just enough for LOS |
| **Time on target** | Extended (up to 30 seconds) |
| **Risk** | High if position revealed |
| **Advantage** | Stable platform = maximum SACLOS accuracy |

---

## Shturm vs. Ataka Decision

| Situation | Recommended | Reason |
|---|---|---|
| Target at <3,000 m | **Shturm** | Save Ataka for extended range |
| Target at 4,000–6,000 m | **Ataka** | Only Ataka can reach |
| MBT in open | Either (HEAT) | Both effective against armor |
| Bunker or building | **Ataka Thermobaric** | Optimal warhead for target |
| Heavy AAA area | **Ataka** | Extended standoff (6 km) |
| Multiple close targets (budget) | **Shturm** | Less costly per shot |
| Time-critical shot | **Ataka** | Faster time-of-flight |
| Moving target | **Ataka** | Better accuracy; less lead required |

---

## In-Sim Procedures

### DCS Key Bindings

| Function | Default Key |
|---|---|
| **Select ATGM** | `D` (weapon cycle to ATGM) |
| **Fire Missile** | `Space` |
| **ATGM Type (Shturm/Ataka)** | Cockpit click — ATGM mode switch |
| **PKV-1 Slew** | Numpad 2/4/6/8 |
| **PKV-1 Zoom In/Out** | Numpad + / − |
| **Autopilot** | `A` (verify DCS key bindings) |
| **Seat → WSO** | `1` |
| **Seat → Pilot** | `2` |

### Single-Player ATGM Engagement — Step by Step

**Step 1 — WSO Seat Setup:**
1. `1` → WSO seat
2. Master Arm → **ARMED**
3. Weapon Selector → **ATGM**
4. ATGM Mode → **SHTURM** or **ATAKA** (matches loaded missiles)
5. Pylon Selector → outer station (1 or 4) with missiles loaded

**Step 2 — Target Acquisition (WSO Seat):**
1. PKV-1 power ON; weapon mode set to **ATGM**
2. Magnification 4–6×
3. Center crosshair on target; estimate range
4. Call (verbalize): **"Target confirmed, [type], [range], ready to fire"**

**Step 3 — Position (Pilot Seat):**
1. `2` → Pilot seat
2. Maneuver to engagement geometry (target bearing ahead)
3. Autopilot → **ON** (heading + altitude hold)
4. Stabilize at 160–180 km/h

**Step 4 — Launch (WSO Seat):**
1. `1` → WSO seat quickly
2. Final crosshair check — centered on target
3. Fire button → **PRESS**
4. **Track target** — do not look at missile

**Step 5 — Guidance (WSO Seat — do not switch):**
1. Maintain crosshair on target center-mass (8–15 seconds)
2. Smooth joystick corrections only
3. Hold position until impact or timeout

**Step 6 — Post-Impact:**
1. BDA through PKV-1 — call result
2. If re-engagement required: repeat from Step 4
3. `2` → Pilot seat → break maneuver

### Mission Practice Sequence

**Exercise 1 — Shturm vs. stationary IFV at 1,500 m:**
- Profile: Pop-up attack; entry 150 m AGL; pop to 300 m
- Success: Impact within 3 m of target

**Exercise 2 — Shturm vs. stationary MBT at 3,000 m:**
- Profile: Level flight approach; autopilot; 15-second guidance
- Success: Direct hit or impact within 3 m

**Exercise 3 — Ataka vs. stationary MBT at 4,500 m:**
- Profile: Pop-up at 400 m AGL; 12-second guidance
- Success: Direct hit

**Exercise 4 — Sequential engagement (2 targets):**
- Profile: Shturm on target 1 (1,500 m); Ataka on target 2 (3,500 m)
- Success: Both hits; no guidance break between engagements

**Exercise 5 — Ataka thermobaric vs. bunker:**
- Warhead: Select thermobaric variant
- Success: Bunker structure damage confirmed via BDA

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| **Tracking the missile, not the target** | Spiral miss pattern | Watch target only; ignore missile in periphery |
| **Switching seats during guidance** | Missile flies ballistic (miss) | Stay in WSO seat for entire guidance phase |
| **Pilot turns during guidance** | Sight line displaced → miss | Pilot: engage autopilot; hold heading |
| **Overcorrecting sight** | Spiral oscillation | Smaller, smoother joystick inputs |
| **Target lost in dust/smoke** | Random guidance → miss | Hold last known position; do not overcorrect |
| **Firing within minimum range** | Guidance fails | Verify range >400 m before launch |
| **Using Ataka at <2,000 m** | Waste of expensive missile | Use Shturm for closer targets |
| **Wrong ATGM mode selected** | Wrong guidance algorithm | Verify SHTURM/ATAKA matches loaded missiles |
| **No autopilot (single-player)** | Cannot guide and fly simultaneously | Always autopilot before switching to WSO seat |

---

## Completion Standards

The student must demonstrate the following to the instructor's satisfaction:

- [ ] Correctly explain SACLOS guidance in plain language (pre-flight oral)
- [ ] Execute Shturm engagement on stationary target at 2,000 m — impact within 5 m
- [ ] Execute Ataka engagement on stationary target at 4,000 m — impact within 5 m
- [ ] Complete all guidance phases without seat-switching during missile flight
- [ ] Select correct warhead for 3 target types when prompted (armor vs. bunker vs. building)
- [ ] Make correct crew calls in sequence for entire engagement cycle
- [ ] Demonstrate 3 consecutive ATGM engagements with no guidance breaks
- [ ] No unauthorized maneuvers during pilot flight profile phase

---

*Based on DCS World Mi-24P Hind module by Eagle Dynamics; 9M114 Shturm and 9M120 Ataka system manuals; Soviet VVS weapons employment doctrine. For simulation use only.*
