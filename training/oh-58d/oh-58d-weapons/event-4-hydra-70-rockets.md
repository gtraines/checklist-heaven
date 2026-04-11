# Event 4 — Hydra 70 Unguided Rocket Employment

> **Course:** OH-58D Kiowa Warrior Weapons Employment Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — System Overview & Warhead Selection](#part-1--system-overview--warhead-selection)
4. [Part 2 — CCIP Delivery System](#part-2--ccip-delivery-system)
5. [Part 3 — Weapons Page Setup](#part-3--weapons-page-setup)
6. [Part 4 — Employment Profile: Diving Fire](#part-4--employment-profile-diving-fire)
7. [Part 5 — Employment Profile: Running Fire](#part-5--employment-profile-running-fire)
8. [Part 6 — Employment Profile: Hover Fire](#part-6--employment-profile-hover-fire)
9. [Part 7 — Dispersion, Accuracy & Techniques](#part-7--dispersion-accuracy--techniques)
10. [Completion Standards](#completion-standards)
11. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Identify available Hydra 70 warhead types and select the appropriate warhead for a given target type and mission requirement
- [ ] Configure the rocket weapons page including warhead type, quantity per salvo, and inventory confirmation
- [ ] Interpret CCIP reticle ("I-beam") symbology and explain how aircraft state inputs affect pipper position
- [ ] Execute a diving fire rocket profile at standard parameters (10–20° dive, 80–100 KIAS, 1,500–3,000 m)
- [ ] Execute a running fire rocket profile for area suppression
- [ ] Execute a hover fire rocket profile from a stabilized hover
- [ ] Apply techniques to improve accuracy: trimming, steady-state flight, ranging shots, CCIP stabilization time
- [ ] Manage rocket expenditure across multiple targets using appropriate salvo sizes

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase 1 | Academic review — warhead types, CCIP principles, employment profiles |
| Phase 2 | Cold-and-dark startup; weapons page setup; pre-attack checks |
| Phase 3 | Diving fire profile — ≥ 5 passes at designated target range with various salvo sizes |
| Phase 4 | Running fire profile — 2 passes for area suppression |
| Phase 5 | Hover fire profile — 2 engagements from stable hover |
| Phase 6 | Shutdown; debrief |

### Key Parameters for This Event

| Item | Value |
|---|---|
| Diving fire — dive angle | 10–20° (15° standard) |
| Diving fire — entry altitude | 800–1,500 ft AGL |
| Diving fire — airspeed | 80–100 KIAS |
| Diving fire — firing range | 1,500–3,000 m slant range |
| Break-off range | ~1,000 m (cease fire; pull off) |
| Minimum recovery altitude | 300 ft AGL |
| Hover fire — range | 800–2,000 m |
| Hover fire — minimum range | 800 m (rotor wash degrades accuracy below this) |
| Rockets per pod (M260) | 7 tubes |

---

## Part 1 — System Overview & Warhead Selection

### M260 Launcher

| Parameter | Value |
|-----------|-------|
| **Designation** | M260 Lightweight Launcher |
| **Capacity** | 7 tubes (7 rockets per pod) |
| **Mounting** | Left and/or right UWP |
| **Maximum Loadout** | 14 rockets (2× M260 pods — both pylons) |
| **Rocket Motor** | Mk 66 Mod 4 (2.75-inch / 70 mm) |
| **Spin Stabilization** | Folding fins deploy after launch; rocket spins for trajectory stability |

### Available Warheads (DCS OH-58D)

| Warhead | Type | Weight | Effect | Primary Use |
|---------|------|--------|--------|------------|
| **M151 HE** | High Explosive | 10 lbs | Blast + fragmentation; ~10 m lethal radius | Troops in the open, light vehicles, soft targets |
| **M229 HE** | High Explosive (Heavy) | 17 lbs | Larger blast radius; greater fragmentation | Structures, material targets, vehicle concentrations |
| **M282 MPP** | Multi-Purpose Penetrator | ~9 lbs | Shaped charge + frag; penetrates light armor | Light APCs, bunkers, hardened fighting positions |
| **M156 WP** | White Phosphorus | ~9 lbs | Incendiary + dense white smoke | Target marking ("Mark on my smoke"), incendiary effects, screening |
| **M257 Illum** | Illumination (Overt) | ~7 lbs | Visible parachute flare; ~1 million candlepower | Night battlefield illumination |
| **M278 IR Illum** | Illumination (Covert IR) | ~7 lbs | IR-only parachute flare | Covert night illumination for NVG-equipped forces |

### Warhead Selection Guide

| Target / Situation | Recommended Warhead | Notes |
|-------------------|--------------------|-------|
| Troops in the open | **M151 HE** | Best frag pattern for personnel |
| Trucks, technicals, soft-skin vehicles | **M151 HE** or **M229 HE** | M229 for clustered or larger vehicles |
| Structures / buildings | **M229 HE** | Heavier warhead for structural damage |
| Light armored vehicles (BTR, BRDM) | **M282 MPP** | Shaped charge defeats thin armor |
| Bunkers / reinforced fighting positions | **M282 MPP** | Penetrating warhead defeats overhead cover |
| Target marking for CCA coordination | **M156 WP** | Produces visible smoke; "Mark on my smoke" call for ground forces |
| Night illumination — overt | **M257** | When concealment is not a constraint |
| Night illumination — NVG / covert | **M278** | IR-only flare; invisible to the naked eye |

> **Note:** The Hydra 70 is fundamentally an **area weapon**. Even with CCIP, circular error probable (CEP) at typical engagement ranges is 10–50 meters. Do not attempt to engage point targets where a miss of 20+ meters is tactically unacceptable — use APKWS (Event 5) or Hellfire (Event 3) for those situations.

---

## Part 2 — CCIP Delivery System

The OH-58D provides a **Continuously Computed Impact Point (CCIP)** for rocket delivery, displayed as an "I-beam" reticle on the MFD.

### CCIP Reticle Behavior

| Element | Description |
|---------|-------------|
| **I-Beam Pipper** | Computed ground impact point of the next rocket(s) given current aircraft state |
| **Dynamic Movement** | Pipper shifts continuously with attitude, airspeed, and altitude changes |
| **Range Arc / Readout** | Indicates slant range from the aircraft to the computed impact point |
| **Stabilization** | Pipper is most stable in steady-state, unaccelerated flight; maneuvering causes pipper to wander |

### CCIP Accuracy Factors

| Factor | Effect on Accuracy | Mitigation |
|--------|-------------------|------------|
| **Aircraft stability** | Unsteady platform → wandering pipper → dispersed impacts | Trim aircraft; fly steady-state for 2–3 seconds before firing |
| **Dive angle** | Steeper dive = tighter dispersion; shallower = wider spread | Use 10–20° dive for best accuracy |
| **Airspeed** | Higher speed = less time of flight = less wind drift | Maintain 80–100 KIAS for best results |
| **Range** | Greater range = more dispersion from wind, motor variation, fin deployment | Engage at 1,500–3,000 m for best accuracy |
| **Wind** | Crosswind displaces unguided rockets laterally | Reduce range; account for wind in aim offset; or use APKWS |
| **Rotor wash** | At very close range in hover fire, rotor downwash can deflect trajectory | Maintain ≥ 800 m minimum range in hover fire |
| **G-loading** | Firing during a pull or turn changes rocket release geometry | Fire in wings-level, unaccelerated condition only |

> *⚠ Realism Divergence: DCS models rocket ballistics including gravity, drag, and wind drift. Real-world Hydra 70 dispersion is somewhat larger than DCS typically shows due to motor variation, fin deployment inconsistency, and atmospheric turbulence. The CCIP is generally accurate in DCS when the aircraft is in steady flight.*

---

## Part 3 — Weapons Page Setup

Before each rocket attack run, configure the weapons page:

| Step | Action | Notes |
|------|--------|-------|
| 1 | Select **RKT** on MFD weapons page | Rocket sub-page displays |
| 2 | Verify warhead type matches the loaded warhead | Auto-detected from loadout; confirm |
| 3 | Select **quantity per salvo** | See salvo selection table below |
| 4 | Verify rocket count (remaining per pod) | Track expenditure; 7 per pod |
| 5 | **Master Arm → ARM** when entering the attack run | ARM before reaching firing range |
| 6 | Verify CCIP pipper is active on MFD | Pipper should be moving dynamically with aircraft state |

### Quantity Per Salvo Selection

| Quantity | Best Use |
|----------|----------|
| **1** | Ranging shot; WP marking; ammunition conservation; single precision target |
| **2** | Standard engagement; small point target; balance of accuracy and effect |
| **4** | Area target; vehicle group; increased probability of hit when aim is uncertain |
| **7** (full pod) | Massed suppression; large area target; danger-close suppression of enemy assault |

**Practice Discipline:** Always fire 1 rocket first as a ranging shot when engaging a new target type or at an unfamiliar range. Observe the fall of shot. Adjust aim. Then commit a larger salvo. This conserves ammunition and improves hit probability.

---

## Part 4 — Employment Profile: Diving Fire

Diving fire is the **most accurate** unguided rocket delivery method and is the primary technique for the OH-58D.

### Profile Parameters

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Dive Angle** | 10–20° | 15° is the standard; steeper gives tighter dispersion but requires faster recovery |
| **Entry Altitude** | 800–1,500 ft AGL | Above small-arms effective range during the initial dive |
| **Airspeed** | 80–100 KIAS | Higher speed improves accuracy and reduces exposure time |
| **Firing Range** | 1,500–3,000 m slant range | Optimum accuracy vs. vulnerability tradeoff |
| **Break-Off Range** | ~1,000 m | Cease fire; initiate pull-off |
| **Minimum Recovery Altitude** | 300 ft AGL | Never descend below this; break off earlier if necessary |

### Diving Fire Procedure

| Step | Action |
|------|--------|
| 1 | Establish inbound at entry altitude and airspeed; target identified on MFD |
| 2 | Verify weapons page: correct warhead, quantity per salvo, Master Arm → ARM |
| 3 | Establish dive angle (push over smoothly to 10–20°); maintain constant airspeed |
| 4 | Place CCIP pipper on target; **wait 1–2 seconds for pipper to stabilize** |
| 5 | Fire (1-rocket ranging shot first; then fire-for-effect based on observed impact) |
| 6 | Observe impacts on MFD/visual; note offset from target |
| 7 | Adjust aim on next salvo (if additional rockets) |
| 8 | **Initiate pull-off at break-off range (1,000 m) or 300 ft AGL — whichever comes first** |
| 9 | Break turn (30–60° bank) away from the target area |
| 10 | Master Arm → SAFE after egressing the target area |

> **Safety:** The break-off range and minimum recovery altitude are hard limits. Target fixation during a dive is the primary cause of controlled flight into terrain. Call "PULL OFF" to yourself if you reach either limit, regardless of whether you have fired all planned rounds.

---

## Part 5 — Employment Profile: Running Fire

Running fire delivers rockets from level or slightly nose-low flight. It is less accurate than diving fire but is used for area suppression or when terrain or weather prevents a dive attack.

### Profile Parameters

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Altitude** | 200–500 ft AGL | Low-level; increased vulnerability to ground fire |
| **Airspeed** | 60–100 KIAS | — |
| **Dive Angle** | 0–5° (level to slight nose-down) | Shallow angle = wider dispersion pattern |
| **Firing Range** | 1,000–2,500 m | Shorter range partially compensates for reduced accuracy |

### Running Fire Procedure

| Step | Action |
|------|--------|
| 1 | Establish level inbound run at 200–500 ft AGL; target identified |
| 2 | Verify weapons page; Master Arm → ARM |
| 3 | Adjust heading to place CCIP pipper near target area |
| 4 | Fire when pipper sweeps onto target; multiple rockets for area coverage |
| 5 | Break off when through the target area or at break-off range |

**Tradeoffs vs. Diving Fire:**
- Wider dispersion — suitable for area targets only
- Higher vulnerability from ground fire (low altitude, sustained exposure)
- Less time to observe and correct aim between runs

---

## Part 6 — Employment Profile: Hover Fire

Hover fire engages targets from a stationary or near-stationary hover. It is a close-range, high-risk technique used when terrain prevents a dive attack or for very close opportunity targets.

### Profile Parameters

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Airspeed** | 0–20 KIAS | Hover or slow creep |
| **Range** | 800–2,000 m | Close range required for acceptable accuracy |
| **Altitude** | 30–100 ft AGL | Standard hover height; higher hover improves trajectory angle |
| **Minimum Range** | 800 m | Below this, rotor wash deflects rocket trajectory |

### Hover Fire Procedure

| Step | Action |
|------|--------|
| 1 | Establish stable hover at engagement altitude; target identified |
| 2 | Verify weapons page; Master Arm → ARM |
| 3 | **Aim the aircraft nose at the target** — rockets are fixed-forward; aircraft heading = aim direction |
| 4 | Place CCIP pipper on target (adjust with cyclic pitch/roll and pedals) |
| 5 | Fire in short salvos (1–2 rockets); observe fall of shot |
| 6 | Adjust aim between salvos |
| 7 | **Transition to forward flight immediately** after the last salvo |

> **Instructor Note:** Hover fire with unguided rockets puts the aircraft in its most vulnerable state: stationary, fully exposed, and at low altitude. Use only when diving fire is not possible. Always plan an escape route before initiating hover fire. The aircraft should be moving within 5 seconds of the last rocket release.

---

## Part 7 — Dispersion, Accuracy & Techniques

### Expected Dispersion at Standard Ranges

| Range | Profile | Approx. CEP | Notes |
|-------|---------|-------------|-------|
| 1,500 m | 15° dive | ~10–15 m | Best case; stable platform, steady dive |
| 2,000 m | 15° dive | ~15–25 m | Standard engagement range |
| 3,000 m | 15° dive | ~30–50 m | Extended range; area targets only |
| 2,000 m | Level running fire | ~30–50 m | Reduced accuracy in level delivery |
| 1,500 m | Hover | ~20–30 m | Rotor wash and platform instability degrade accuracy |

> These are approximate values. Actual DCS dispersion varies by implementation. Use ranging shots before committing full salvos.

### Techniques for Improving Accuracy

1. **Trim the aircraft** before the attack run. An untrimmed aircraft causes the CCIP pipper to wander — you fight the aircraft instead of aiming.
2. **Fly steady-state** at constant airspeed, attitude, and dive angle for 2–3 seconds before firing. The pipper needs time to stabilize after the aircraft settles.
3. **Use ranging shots.** Fire 1 rocket; observe the impact; note the offset; adjust aim; then fire for effect with the remaining salvo.
4. **Minimize G-loading.** Fire during wings-level, unaccelerated flight. Pulling or banking during the firing pass changes rocket release geometry.
5. **Wait for pipper stabilization.** The pipper moves rapidly during attitude changes. After establishing your dive, wait for the pipper to settle before pressing the trigger.

---

## Completion Standards

The student passes this event when they can, without instructor prompting:

- [ ] Correctly select the appropriate warhead type for a target called by the instructor and state the rationale
- [ ] Configure the weapons page with correct warhead, salvo quantity, and verify inventory; complete the Master Arm sequence before each pass
- [ ] Execute the diving fire profile at standard parameters (15° dive, 80–100 KIAS, 1,500–3,000 m firing range) with trim and steady-state established before firing — **3 passes minimum; at least 1 direct hit per 3 rockets in each pass**
- [ ] Demonstrate the ranging shot technique (1 rocket first; observe; adjust; fire-for-effect) on at least 2 passes
- [ ] Execute the break-off at or before 1,000 m slant range on every pass; minimum recovery altitude ≥ 300 ft AGL
- [ ] Execute at least 1 running fire pass demonstrating area suppression technique
- [ ] Execute at least 2 hover fire engagements from a stabilized hover at 800–2,000 m
- [ ] Master Arm → SAFE immediately after each attack profile
- [ ] Conduct BDA after each pass; report results to instructor

---

## Common Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Firing during a bank or pull | Rockets disperse widely across a broad area; miss point target entirely | Establish wings-level, steady-state before trigger press; release back-pressure before firing |
| Pressing below break-off range | Risk of fragmentation self-damage; insufficient recovery altitude; controlled flight toward terrain | Hard limit at 1,000 m / 300 ft AGL; break off when either limit is reached, regardless of result |
| Firing full-pod salvos on the first pass | All 7 rockets wasted on an uncorrected miss; no ammunition left for follow-up | Use 1-rocket ranging shot on first engagement; scale up salvo size only after confirming aim is correct |
| Not trimming before the attack run | Pipper wanders as pilot fights the aircraft; erratic dispersion | Trim for attack airspeed and dive angle before entering firing range; feel the aircraft in trim |
| Wrong warhead for target | WP on armor (no effect); M151 HE on structures (insufficient damage) | Brief warhead plan pre-mission; verify warhead displayed on MFD before arming |
| Hover fire at > 2,000 m | Rocket dispersion too wide for a point target at extended range | Reduce range to < 2,000 m for hover fire; use diving fire for longer-range engagements |
| Forgetting Master Arm before the attack run | Trigger press yields nothing; full exposure for a wasted run | Verbal cadence: "ARM — HOT — CLEARED" before crossing the outer firing boundary |
| Not observing fall of shot | Unknown impact location; continued firing without aim adjustment wastes ammunition | Watch MMS or direct visual for rocket impact; adjust aim between salvos |

---

*Based on TM 1-1520-248-10, FM 3-04.140, Polychop Simulations DCS OH-58D documentation. For simulation use only.*
