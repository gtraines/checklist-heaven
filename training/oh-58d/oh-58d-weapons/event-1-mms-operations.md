# Event 1 — MMS Operations & Targeting

> **Course:** OH-58D Kiowa Warrior Weapons Employment Course | **Event Type:** Academics / Simulator
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — MMS Architecture & Mast-Mounted Advantage](#part-1--mms-architecture--mast-mounted-advantage)
4. [Part 2 — Power-On & Boresight](#part-2--power-on--boresight)
5. [Part 3 — MFD MMS Page Layout](#part-3--mfd-mms-page-layout)
6. [Part 4 — Sensor Modes: TV and TIS/FLIR](#part-4--sensor-modes-tv-and-tisflir)
7. [Part 5 — MMS Controls & Tracking Modes](#part-5--mms-controls--tracking-modes)
8. [Part 6 — Laser Operations](#part-6--laser-operations)
9. [Part 7 — Target Acquisition Workflow](#part-7--target-acquisition-workflow)
10. [Completion Standards](#completion-standards)
11. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Describe the MMS sensor suite (TV, TIS/FLIR, LRF/D) and explain the tactical advantage of mast-mounted positioning
- [ ] Power on, initialize, and boresight the MMS in DCS
- [ ] Operate each sensor mode (TV, FLIR) including FOV, polarity, and gain/level adjustments
- [ ] Employ the Laser Rangefinder (LRF) for single-pulse ranging and interpret the range readout
- [ ] Employ the Laser Designator (LRD) for continuous designation and verify laser armed/firing indications
- [ ] Set and verify PRF (laser) codes on the MFD
- [ ] Select the correct tracking mode (Manual, Area Track, Point Track, Inertial) for each phase of target engagement
- [ ] Execute a complete target acquisition sequence: Search → Detect → Identify → Classify → Engage → BDA

> **Event Structure:** This is a two-part academic and simulator event. Part A covers system knowledge (ground brief). Part B is conducted in a DCS ramp-start scenario — the student powers up the MMS from cold, boresights it, and runs through all sensor modes and tracking modes against a designated target set. No weapons are fired in this event.

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase A | Academic briefing — MMS architecture, sensor modes, laser operations |
| Phase B | DCS simulator — power-on, boresight, sensor familiarization |
| Phase C | DCS simulator — target acquisition drills using all sensor modes and tracking modes |
| Phase D | DCS simulator — laser ranging and designation practice against stationary targets |

### Key Reference Data

| Item | Value |
|---|---|
| MMS Power Requirement | 28V DC aircraft power |
| TIS/FLIR Warm-Up Time | ~60–90 seconds after power-on |
| TV Availability | Nearly immediate after power-on |
| MMS Field of Regard — Azimuth | 360° continuous |
| MMS Field of Regard — Elevation | Approximately +30° to −80° |
| Default PRF Code | 1688 |
| LRF Single-Pulse Range Accuracy | ~5–10 m at tactical ranges |
| Minimum Boresight Distance | 1,000 m to reference point |

---

## Part 1 — MMS Architecture & Mast-Mounted Advantage

### Sensor Suite

The Mast Mounted Sight (MMS) is the OH-58D's primary sensor system and tactical signature. It houses three distinct sensors in a single stabilized turret positioned above the main rotor hub:

| Sensor | Function | Primary Use |
|--------|----------|-------------|
| **TV (Day Camera)** | Electro-optical daylight imagery | Daytime target ID; high-resolution positive identification (PID) |
| **TIS / FLIR (Thermal Imaging Sensor)** | Infrared thermal imagery | Night/low-visibility operations; heat signature detection through haze, darkness, light obscurants |
| **LRF (Laser Rangefinder)** | Single-pulse laser ranging | Precise range to target for weapons solutions and coordinate extraction |
| **LRD (Laser Designator)** | Continuous coded laser energy | Terminal guidance for Hellfire (SAL) and APKWS; buddy lasing for other shooters |

### The Hull-Down Advantage

The MMS is positioned approximately **12 feet above the fuselage** on the main rotor mast — above the rotor disc. This geometry is the tactical foundation of all OH-58D operations:

- The pilot can **unmask only the MMS** above a ridgeline, treeline, or building rooftop.
- The **entire fuselage, engine exhaust, crew, and tail rotor remain below terrain cover**.
- This dramatically reduces the aircraft's visual, IR, and radar signature to enemy forces.
- A hull-down Kiowa presents only a small spherical sensor pod above the skyline — extremely difficult to detect and nearly impossible to engage with anything but a perfectly aimed shot.

> **Instructor Note:** Students must internalize that hull-down is not a convenience — it is the survival doctrine for this aircraft. A Kiowa that rises above terrain cover is trading its primary survivability advantage for a few extra degrees of sensor coverage. The MMS was designed so this trade is almost never necessary.

### Field of Regard

| Axis | Range | Notes |
|------|-------|-------|
| **Azimuth** | 360° continuous | Full rotation; can observe in any direction independent of aircraft heading |
| **Elevation** | Approximately +30° to −80° | Depression allows observation of targets well below the aircraft; useful for observing valley floors from a ridgeline BP |

> *⚠ Realism Divergence: The real OH-58D MMS has azimuth gimbal stops at certain extreme elevation angles due to mechanical constraints and mast/rotor proximity. DCS provides full 360° rotation at all depression angles without restriction. Real-world operators encounter these gimbal stops during steep depression work.*

### Slew Rates

| Mode | Use |
|------|-----|
| **Coarse Slew** | Rapid MMS repositioning to a new sector; initial search and gross target area acquisition |
| **Fine Slew** | Slow, precise movement for crosshair refinement; used during final target identification and laser designation |

Slew is controlled via the **cyclic-mounted MMS ministick or hat** (HOTAS mapping in DCS). Students should configure analog slew axes — digital hat switches cause jerky, imprecise MMS movement that makes precise designation difficult.

---

## Part 2 — Power-On & Boresight

### MMS Startup Sequence

| Step | Action | Notes |
|------|--------|-------|
| 1 | Confirm aircraft power — battery/generator online | MMS requires 28V DC |
| 2 | MMS Power switch → **ON** | Begins sensor warm-up sequence |
| 3 | Wait for TIS/FLIR initialization | TV available almost immediately; TIS/FLIR requires ~60–90 seconds to thermally stabilize |
| 4 | Select initial sensor mode on MFD — TV or TIS | OSB press on MMS MFD page |
| 5 | Verify MMS video on MFD | Confirm imagery appears; check for degraded image or blank screen |
| 6 | Perform boresight | See procedure below |

### Ground Boresight Procedure

Boresighting ensures the MMS sensors, crosshair, and laser all point to the same physical location. A mis-boresighted system causes the laser to strike a different point than the crosshair indicates — causing precision weapons to miss even when the MFD shows the crosshair on target.

**Standard Ground Boresight:**
1. Position the aircraft on a level surface. Identify a reference point at ≥ 1,000 m — a building corner, fence post, or prominent terrain feature.
2. Access the **MMS boresight page** on the MFD.
3. Slew the **TV crosshair** precisely onto the reference point and confirm.
4. Switch to **TIS** — adjust crosshair to the same reference point and confirm.
5. Fire a single **LRF pulse** — verify range readout matches the known or estimated distance to the reference point.
6. Accept boresight and return to operational sensor mode.

**Air Boresight:**
- Performed in flight using an identifiable landmark at known range.
- Less precise than ground boresight; useful for mid-mission verification.
- Fire the LRF; compare readout to a GPS-computed range to the known point.

> *⚠ Realism Divergence: Real-world boresight uses a specialized collimation panel and multi-step procedure with written log entries. DCS simplifies this to an MFD align/accept process. The fundamental requirement (crosshair = laser = target) is identical.*

> **Instructor Note:** Boresight must be completed before the first engagement of every flight. A student who fires a laser-guided weapon without boresighting and misses as a result earns a mandatory re-fly of this event.

---

## Part 3 — MFD MMS Page Layout

The MMS page is the primary MFD display during all sensor operations and weapons employment. Students must be able to read and interpret every element at a glance.

| Element | Description |
|---------|-------------|
| **Video Window** | Live TV or TIS imagery filling the MFD display area |
| **Crosshair / Reticle** | Center aiming reference; the laser fires to this point |
| **Sensor Mode Indicator** | Active sensor: TV or TIS |
| **FOV Indicator** | Current field of view: WIDE (WFOV) or NARROW (NFOV) |
| **Polarity Indicator** *(TIS only)* | WHT (white-hot) or BLK (black-hot) |
| **Laser Code (PRF)** | Current 4-digit pulse repetition frequency code |
| **Laser Status** | SAFE / ARMED / FIRING indications |
| **Range Readout** | Last LRF range in meters; updates on each pulse |
| **Target Coordinates** | Computed LAT/LONG of the point under the crosshair (requires valid LRF range) |
| **Azimuth / Elevation** | MMS pointing direction relative to aircraft heading |
| **Weapon Status** | Selected weapon type and readiness state |
| **OSB Functions** | Option Select Buttons around the MFD bezel — sensor controls, weapon actions, mode selection |

---

## Part 4 — Sensor Modes: TV and TIS/FLIR

### TV (Day Camera)

| Parameter | Description |
|-----------|-------------|
| **Optimal Conditions** | Daylight, good visibility, VMC |
| **WFOV** | Broad view for sector search and situational awareness |
| **NFOV** | Magnified view for target identification and precise laser placement |
| **Advantages** | High resolution; natural-appearance imagery; only sensor capable of text/marking recognition; best for PID |
| **Limitations** | Completely ineffective at night or in degraded visibility — do not attempt TV engagement at night |

### TIS / FLIR (Thermal Imaging Sensor)

| Parameter | Description |
|-----------|-------------|
| **Optimal Conditions** | Night, low visibility, dawn/dusk, haze, smoke, dust |
| **WFOV / NFOV** | Same toggle as TV |
| **Polarity — White-Hot (WHT)** | Hot objects appear white on dark background; standard for vehicle/personnel detection |
| **Polarity — Black-Hot (BLK)** | Hot objects appear dark on light background; may improve contrast in desert or snow environments |
| **Gain** | Adjusts sensor sensitivity — higher gain increases contrast but amplifies noise |
| **Level** | Adjusts brightness midpoint — shifting level reveals detail in overly bright or dark scenes |
| **Advantages** | Operates in total darkness; detects heat signatures through light obscurants; reveals engine-warm vehicles camouflaged to visual sensors |
| **Limitations** | Thermal crossover (dawn/dusk — ambient and target temperatures equalize, reducing contrast); degraded in heavy rain and thick fog; cannot read text, markings, or colors |

### Sensor Selection Guide

| Condition | Recommended Sensor | Reason |
|-----------|--------------------|--------|
| Bright daylight, good visibility | TV | Best resolution; PID capable |
| Dusk / dawn | TIS (adjust gain/level) | Thermal crossover — try both; TIS may be marginal |
| Night (clear) | TIS | Only viable sensor |
| Night (haze or light fog) | TIS | Thermal penetrates light obscurants |
| Heavy fog or rain | TIS (degraded) | Significantly reduced effectiveness; consider abort |
| Smoke / dust | TIS | Thermal penetrates many battlefield obscurants |
| PID required by ROE | TV (if light permits) | Only TV provides visual marking and identification detail |

---

## Part 5 — MMS Controls & Tracking Modes

### HOTAS Mapping (DCS)

| Function | Recommended Binding | Notes |
|----------|---------------------|-------|
| **MMS Slew X/Y** | Analog ministick or hat | Analog axes strongly preferred; digital hat causes jerky, imprecise slew |
| **FOV Toggle** | HOTAS button | WFOV ↔ NFOV |
| **Sensor Toggle** | HOTAS button | TV ↔ TIS |
| **Polarity Toggle** | HOTAS button or MFD OSB | WHT ↔ BLK (TIS only) |
| **LRF Pulse** | HOTAS button | Single press for range measurement |
| **Laser Designate** | HOTAS button (hold) | Press and hold for continuous laser designation |
| **Track Mode Select** | MFD OSB or HOTAS | Cycle tracking modes |

> **Instructor Note:** Verify HOTAS bindings before commencing Part B of this event. Every item on the table above must have a functional HOTAS binding. Anything missing must be corrected before proceeding.

### Tracking Modes

| Mode | Behavior | Use Case |
|------|----------|----------|
| **Manual (No Track)** | MMS stays where the pilot slews it; no automatic stabilization beyond gyro | Initial search; wide-area scan; transitioning between targets |
| **Area Track** | MMS maintains pointing at a fixed geographic location; compensates for aircraft movement | Monitoring a road junction, suspected target area, or engagement area while the aircraft drifts |
| **Point Track** | MMS automatically tracks a high-contrast point (vehicle, structure edge, heat source) against the background | Locked onto a confirmed target; use for all laser designation — this is the mode used during Hellfire and APKWS engagement |
| **Inertial** | MMS maintains a stabilized direction (heading/elevation) regardless of aircraft movement | Holding a bearing while repositioning the aircraft; useful when you want the MMS to stay pointed at a sector |

**Tracking Mode Discipline:**
- Use **Manual** during initial sector search and while scanning for new contacts.
- Use **Area Track** when monitoring a specific location (suspected target, trigger line, intersection).
- Use **Point Track** when locked onto a confirmed target for engagement — engage Point Track mode **before** arming the laser for any precision weapon shot.
- If **Point Track is lost** during laser designation, the laser drifts off the target. A Hellfire or APKWS in flight will lose guidance. Re-acquire immediately or abort the shot.

---

## Part 6 — Laser Operations

### Laser Rangefinder (LRF)

| Item | Description |
|------|-------------|
| **Function** | Fires a single laser pulse and measures round-trip time to compute slant range |
| **Output** | Range in meters on the MFD |
| **Trigger** | Single press of the LRF button on HOTAS |
| **Uses** | Pre-engagement range check (is target in envelope?); coordinate extraction; CCIP range input for rocket accuracy |

**When to LRF:**
- Before every engagement — confirm the target is within the weapon's effective range.
- After slewing to a new contact — confirm distance before committing to an engagement.
- When extracting target coordinates for reporting or indirect fire coordination.

### Laser Designator (LRD)

| Item | Description |
|------|-------------|
| **Function** | Fires continuous coded laser energy at the set PRF code |
| **Activation** | Press and **hold** the laser designate button |
| **PRF Code** | 4-digit Pulse Repetition Frequency code; set on the MFD weapons/MMS page; default: **1688** |
| **Required Match** | The seeker of the homing weapon must be programmed to the same PRF code |
| **ARM/SAFE** | Laser must be **ARMED** before the designator will fire; arm only when entering the engagement sequence |

### Lasing Timeline by Weapon

| Weapon / Mode | When to Start Lasing | Maintain Until |
|--------------|---------------------|----------------|
| **Hellfire LOBL** | Before launch — lase continuously; wait for LOCK indication | Impact confirmed |
| **Hellfire LOAL-DIR** | ~8–10 seconds before estimated impact | Impact confirmed |
| **Hellfire LOAL-LO** | ~8–10 seconds before estimated impact | Impact confirmed |
| **Hellfire LOAL-HI** | ~10–15 seconds before estimated impact | Impact confirmed |
| **APKWS** | Before launch — lase during attack run; maintain through impact | Impact confirmed |

> **The single most important lesson in this event:** The laser is the weapon's eyes. If the laser stops, the weapon goes blind and will miss. This is true for every laser-guided weapon in the OH-58D's inventory. **Maintain designation until you see the impact flash — not until you think impact is imminent, not until the aircraft starts to drift. Until you see the flash.**

### Self-Designation vs. Buddy Lasing

| Method | Description | PRF Coordination |
|--------|-------------|------------------|
| **Self-Designation** | OH-58D lases its own target; own weapon homes on own laser | Automatic — same PRF set on both MMS and weapon |
| **Buddy Lase (Designate for Others)** | OH-58D lases; other aircraft fires weapon homing on Kiowa's laser | Brief PRF code to shooter on radio before engagement |
| **Receive Buddy Lase** | External source (JTAC, wingman) lases; OH-58D fires weapon homing on external laser | Set MMS/weapon PRF to match external designator's briefed code |

**Buddy Lase Radio Flow:**
1. Designator: *"Lasing, code 1688, target BTR at TRP 2."*
2. Shooter: *"Copy, code 1688."*
3. Designator: *"Spot"* (laser is active)
4. Controlling authority: *"Cleared hot"*
5. Shooter: *"Rifle"* (Hellfire launch)
6. Designator: *"Splash"* (impact observed)

---

## Part 7 — Target Acquisition Workflow

### Search → Detect → Identify → Classify → Engage → BDA

| Step | Action | MMS Activity |
|------|--------|-------------|
| **Search** | Systematic scan of assigned sector | WFOV; TIS or TV per conditions; Manual or Area Track mode |
| **Detect** | Potential contact spotted | NFOV; slew toward contact; transition to finer observation |
| **Identify** | Determine what the contact is | NFOV or Zoom; TV for visual ID when light permits; TIS for thermal signature |
| **Classify** | Determine friend/foe/neutral and priority | PID per ROE; cross-check against known friendly positions; communicate with ground element |
| **Engage** | Commit to weapons employment | Point Track on target; select weapon; arm laser; execute firing sequence |
| **BDA** | Assess results post-strike | MMS on impact point; observe for secondary explosions, movement, personnel leaving vehicle; report |

### Systematic Search Patterns

| Pattern | Technique |
|---------|-----------|
| **Sector Scan** | Divide sector into left/center/right sub-sectors; scan near-to-far in each; overlap sub-sectors for complete coverage |
| **Road/Trail Scan** | Follow linear features (roads, trails, power lines) that canalize enemy movement |
| **Key Terrain Scan** | Prioritize likely enemy positions: treelines, ridgelines, intersections, defiles, built-up areas |
| **Threat-First Scan** | Scan for highest-threat systems first (air defense, armor) before methodically clearing the sector |

### Grid Coordinate Extraction

When the LRF provides a valid range, the MMS computes a target LAT/LONG from:
- Aircraft GPS position
- MMS azimuth and elevation pointing angles
- LRF slant range

The computed coordinates are displayed on the MFD and can be reported to ground forces, used for artillery call-for-fire, or forwarded to other aviation elements.

> *⚠ Realism Divergence: Real-world coordinate extraction accuracy is approximately 50–100 m CEP at extended ranges, depending on GPS quality, LRF accuracy, and boresight calibration. DCS may provide more precise results. Instructors should note that in actual operations, grid coordinates extracted from an airborne MMS at 5+ km are confirmatory only — not authoritative.*

---

## Completion Standards

The student passes this event when they can, without instructor prompting:

- [ ] Correctly power on the MMS and wait for TIS initialization without attempting to use TIS before warm-up completes
- [ ] Perform a satisfactory ground boresight using a reference point at ≥ 1,000 m; verify with LRF pulse
- [ ] Identify every element on the MFD MMS page by name and function
- [ ] Switch between TV and TIS sensor modes and explain when each is appropriate
- [ ] Toggle FOV between WFOV and NFOV, and explain the tactical use of each
- [ ] Adjust TIS polarity and explain the difference between WHT and BLK
- [ ] Select each of the four tracking modes (Manual, Area Track, Point Track, Inertial) and describe the use case for each
- [ ] Engage Point Track on a designated target and maintain track while the aircraft hovers and drifts
- [ ] Fire the LRF and interpret the range readout; correlate range to weapon employment decision (in or out of envelope)
- [ ] Arm the laser, verify LASER ARMED indication, and maintain continuous designation on a stationary target for ≥ 30 seconds without breaking designation
- [ ] Describe the complete lasing timeline for Hellfire LOBL, Hellfire LOAL, and APKWS
- [ ] Verbally brief the buddy lase communication flow for a self-designate and a receive-buddy-lase scenario
- [ ] Execute a complete Search → Detect → Identify → Classify workflow against a designated target using the correct sensor mode for the environmental conditions

---

## Common Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Forgetting to arm the laser | Laser does not fire; weapon has no guidance energy | Always confirm LASER ARMED indication on MFD before starting engagement sequence; include as a verbal checklist item |
| Using TV at night or in low visibility | Blank or unusable image; targets missed | Switch to TIS for all night/degraded conditions; verify sensor selection in pre-engagement check |
| Remaining in WFOV for final designation | Target too small to precisely designate; laser point wanders | Switch to NFOV before final ID and laser designation; WFOV is a search tool only |
| Breaking Point Track during aircraft movement | MMS loses lock; laser drifts off target; weapon loses guidance | Minimize maneuvering during designation; if track breaks, immediately re-acquire or abort shot |
| PRF code mismatch before buddy lasing | Weapon homes on wrong laser or noise; misses | Confirm PRF on radio; verify code displayed on MFD matches briefed code before every laser-guided engagement |
| Skipping boresight | Crosshair does not match laser point; weapons miss by a fixed offset | Perform boresight before every mission's first engagement; verify with LRF range check |
| Over-slewing with coarse input during fine tracking | Overshoot target; extended re-acquisition time | Use fine slew for final aiming; reduce slew rate near the target |
| Not conducting BDA after strike | Unknown engagement result; may be re-attacking a destroyed target | Immediately post-impact: maintain MMS on target area; observe for 10 seconds minimum; report results verbally |
| Attempting to TIS during crossover without gain/level adjustment | Poorly contrasted image; targets missed during marginal conditions | Adjust gain and level in dawn/dusk/thermal crossover conditions; try both polarity settings |

---

*Based on TM 1-1520-248-10 (OH-58D Operator's Manual), Polychop Simulations DCS OH-58D documentation. For simulation use only.*
