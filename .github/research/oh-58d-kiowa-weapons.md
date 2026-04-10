# Research Dossier: OH-58D Kiowa Warrior — Weapons Employment

**Target Aircraft:** OH-58D Kiowa Warrior (DCS World — Polychop Simulations)
**Course:** Weapons Employment Training
**Prerequisite:** OH-58D Basic Qualification Training (BQT) complete — student is proficient in startup, hover, basic flight, navigation, traffic patterns, autorotation, and emergency procedures.

---

## Source Material & Prioritization

| Priority | Source | Use |
|----------|--------|-----|
| **Primary** | DCS OH-58D module documentation (Polychop manual) and verified in-game behavior | All cockpit procedures, switchology, and system behavior as implemented |
| **Secondary** | *TM 1-1520-248-10* (OH-58D Operator's Manual) | Systems data, limitations, normal/emergency procedures |
| **Secondary** | *FM 3-04.126* (Attack Reconnaissance Helicopter Ops) | Tactics, battle positions, CCA doctrine |
| **Secondary** | *FM 3-04.140* (Helicopter Gunnery) | Gunnery techniques, qualification standards, range procedures |
| **Secondary** | *TC 1-211* / *TC 1-237* (Aircrew Training Manuals) | Task standards, crew coordination, grading criteria |
| **Secondary** | *ATP 3-04.1* (Aviation Tactical Employment) | Team tactics, engagement area operations |
| **Secondary** | AGM-114 Hellfire TMs (*TM 9-1425-484-12* series) | Missile performance, guidance modes, launch envelopes |
| **Tertiary** | Community guides, Polychop forums, DCS user documentation | Gap-filling where official sources are silent |

> When real-world and DCS procedures conflict, the **DCS procedure is primary**. Divergences are footnoted with:
> *⚠ Realism Divergence: [explanation]*

---

## Aircraft & Module Overview

| Parameter | Value |
|-----------|-------|
| **Engine** | T703-AD-700A (~650 SHP), FADEC auto/manual |
| **Main Rotor** | 4-blade, soft-in-plane, 35 ft diameter |
| **Tail Rotor** | 2-blade |
| **MTOW** | 5,500 lbs |
| **Weapons Pylons** | 2× Universal Weapons Pylons (UWP) — left and right |
| **Primary Sensor** | Mast Mounted Sight (MMS) — TV, TIS/FLIR, LRF/D |
| **Weapons** | AGM-114 Hellfire (K/M/N), Hydra 70 rockets, APKWS (AGR-20A), M3P .50 cal, AIM-92 Stinger |
| **DCS Developer** | Polychop Simulations |
| **Cockpit Fidelity** | Full-fidelity clickable cockpit, AFM |

### Pylon Configuration

Each UWP accepts **one** of the following:

| Station | Options |
|---------|---------|
| Left UWP | 2× AGM-114 Hellfire **OR** 1× M260 rocket pod (7 tubes) **OR** 1× M3P .50 cal gun pod |
| Right UWP | 2× AGM-114 Hellfire **OR** 1× M260 rocket pod (7 tubes) |

> **Critical:** The OH-58D is a **power-limited, single-engine platform**. Every loadout decision trades weapons capability against hover ceiling, rate of climb, and maneuvering margin. Weight management is not optional — it is a survival consideration.

---

## Table of Contents

1. [Module 1 — MMS Operations & Targeting](#module-1--mms-operations--targeting)
2. [Module 2 — Weapons Management System & HUD Symbology](#module-2--weapons-management-system--hud-symbology)
3. [Module 3 — AGM-114 Hellfire Employment](#module-3--agm-114-hellfire-employment)
4. [Module 4 — Hydra 70 Unguided Rocket Employment](#module-4--hydra-70-unguided-rocket-employment)
5. [Module 5 — APKWS Laser-Guided Rocket Employment](#module-5--apkws-laser-guided-rocket-employment)
6. [Module 6 — M3P .50 Caliber Machine Gun Employment](#module-6--m3p-50-caliber-machine-gun-employment)
7. [Module 7 — AIM-92 Stinger Air-to-Air Employment](#module-7--aim-92-stinger-air-to-air-employment)
8. [Module 8 — Countermeasures & Defensive Systems](#module-8--countermeasures--defensive-systems)
9. [Module 9 — Close Combat Attack Tactics & Engagement Area Operations](#module-9--close-combat-attack-tactics--engagement-area-operations)
10. [Module 10 — Mission Planning & Loadout Optimization](#module-10--mission-planning--loadout-optimization)

---

## Module 1 — MMS Operations & Targeting

### Learning Objectives

- Describe the MMS sensor suite (TV, TIS/FLIR, LRF/D) and its mast-mounted advantage.
- Power on, align, and boresight the MMS in DCS.
- Operate each sensor mode (TV, FLIR) including FOV, polarity, gain/level adjustments.
- Employ the Laser Rangefinder for single-pulse ranging and the Laser Designator for continuous designation.
- Set and verify PRF (laser) codes on the MFD.
- Execute systematic target acquisition, identification, and Battle Damage Assessment (BDA) using the MMS.

---

### 1.1 MMS Architecture

The Mast Mounted Sight is the OH-58D's defining tactical sensor. Mounted on a mast above the main rotor hub, it allows the aircraft to remain **hull-down** — fuselage concealed behind terrain, trees, or structures — while the MMS observes and designates targets.

#### Sensor Suite

| Sensor | Function | Primary Use |
|--------|----------|-------------|
| **TV (Day Camera)** | Electro-optical daylight imagery | Daytime target ID; high-resolution imagery in good visibility |
| **TIS / FLIR (Thermal Imaging Sensor)** | Infrared thermal imagery | Night/low-visibility ops; detects heat signatures through haze, light fog, darkness |
| **LRF (Laser Rangefinder)** | Single-pulse laser ranging | Precise range to target for weapons solutions and coordinate extraction |
| **LRD (Laser Designator)** | Continuous coded laser energy | Terminal guidance for Hellfire (SAL) and APKWS; buddy lasing for other shooters |

#### Mast-Mounted Advantage

- The MMS is positioned **above the rotor disc**, approximately 12 feet above the fuselage.
- This allows the pilot to **unmask only the sight** above a ridgeline, treeline, or building while the entire helicopter remains masked.
- The fuselage, engine, tail rotor, and crew are below terrain cover — dramatically reducing the aircraft's visual, radar, and IR signature to the threat.
- This is the fundamental tactical employment posture of the OH-58D: **observe and designate from hull-down, minimizing exposure**.

#### Field of Regard

| Axis | Range | Notes |
|------|-------|-------|
| **Azimuth** | 360° continuous | Full rotation; can observe in any direction regardless of aircraft heading |
| **Elevation** | Approximately +30° to −80° | Depression range allows observation of targets well below the aircraft; elevation permits sky-search for air threats |

> *⚠ Realism Divergence: The real OH-58D MMS has an azimuth limit at certain depression angles due to mechanical gimbal constraints and mast/rotor interference. In DCS, the MMS generally provides full 360° rotation at all depression angles without restriction. Real-world operators would encounter gimbal stops at extreme combinations.*

#### Slew Rates

- **Coarse Slew:** Rapid repositioning of the MMS to a new sector; used during initial search and gross target area acquisition.
- **Fine Slew:** Slow, precise movement for refining crosshair placement on a specific target; used during final target identification and laser designation.
- Slew is controlled via the **cyclic-mounted MMS controller** (HOTAS mapping in DCS) or by clicking/dragging on the MFD MMS page.

---

### 1.2 MMS Power-On & Alignment

#### Startup Sequence

| Step | Action | Notes |
|------|--------|-------|
| 1 | Confirm aircraft power on (battery/generator) | MMS requires 28V DC power |
| 2 | MMS Power switch → **ON** | Located on the MMS control panel; begins sensor warm-up |
| 3 | Wait for MMS initialization | TIS/FLIR requires thermal stabilization (~60–90 seconds); TV available almost immediately |
| 4 | Select initial sensor mode (TV or TIS) on MFD | OSB press on MMS MFD page |
| 5 | Verify MMS video on MFD | Confirm imagery; check for degraded image or FOV anomalies |
| 6 | Perform boresight (if required) | See boresight procedure below |

#### Boresight Procedures

Boresighting ensures the MMS sensors, crosshair, and laser are aligned to the same point. Misalignment causes the laser to hit a different point than the crosshair indicates — **critical for precision weapons delivery**.

**Ground Boresight:**
1. Position the aircraft on a level surface with a known reference point (e.g., a distant, clearly identifiable target or marker) at ≥1,000 m.
2. Access the MMS boresight page on the MFD.
3. Slew the TV crosshair precisely onto the reference point and confirm.
4. Switch to TIS — adjust crosshair to same reference point and confirm.
5. Fire a single LRF pulse — verify range matches expected range to the reference point.
6. Accept boresight and return to operational mode.

**Air Boresight:**
- Performed in flight by slewing sensors to a known, identifiable point and verifying alignment.
- Less precise than ground boresight but useful for mid-mission corrections.

> *⚠ Realism Divergence: Real-world OH-58D boresight involves a detailed, multi-step procedure using a boresight target panel and specialized collimation. DCS simplifies this to an MFD-based align/accept process. The fundamental concept (ensure crosshair = laser = sensors) is identical, but the DCS procedure is faster and less involved.*

---

### 1.3 MFD MMS Page Layout

The MMS page is the primary MFD display during weapons employment. It shows:

| Element | Description |
|---------|-------------|
| **Video Window** | Live TV or TIS imagery filling most of the MFD |
| **Crosshair / Reticle** | Center aiming reference; the laser fires to this point |
| **Sensor Mode Indicator** | Shows current sensor: TV or TIS |
| **FOV Indicator** | Shows current field of view: WIDE or NARROW (NFOV/WFOV) |
| **Polarity Indicator** (TIS only) | WHT (white-hot) or BLK (black-hot) |
| **Laser Code (PRF)** | Current 4-digit pulse repetition frequency code |
| **Laser Status** | SAFE / ARMED / FIRING indicators |
| **Range Readout** | Last LRF range in meters; updates on each pulse |
| **Target Coordinates** | Extracted LAT/LONG of the point under the crosshair (when LRF range is valid) |
| **Azimuth / Elevation** | MMS pointing direction relative to aircraft heading |
| **Weapon Status** | Selected weapon and readiness (when in weapons employment mode) |
| **OSB Functions** | Option Select Buttons around the MFD bezel for sensor controls, weapon actions, and mode selection |

---

### 1.4 Sensor Modes

#### TV (Day Camera)

- **Optimal Conditions:** Daylight, good visibility, VMC.
- **FOV Options:**
  - **Wide FOV (WFOV):** Broader view for sector search and situational awareness.
  - **Narrow FOV (NFOV):** Magnified view for target identification and precision aiming.
- **Zoom:** Step-zoom or continuous zoom (per DCS implementation); additional magnification beyond NFOV for long-range ID.
- **Advantages:** High resolution; natural-appearance imagery; best for PID (Positive Identification) of friendly vs. enemy.
- **Limitations:** Useless at night or in degraded visibility (fog, rain, smoke).

#### TIS / FLIR (Thermal Imaging Sensor)

- **Optimal Conditions:** Night, low visibility, dawn/dusk, obscured conditions.
- **FOV Options:** Same WFOV / NFOV toggle as TV.
- **Polarity:**
  - **White-Hot (WHT):** Hot objects appear white on a dark background — standard for vehicle and personnel detection.
  - **Black-Hot (BLK):** Hot objects appear dark on a light background — can improve contrast in certain environments (desert, snow).
- **Gain / Level:**
  - **Gain:** Adjusts sensor sensitivity (amplification of temperature differences). Higher gain = more contrast but more noise.
  - **Level:** Adjusts the brightness midpoint. Shifting level can reveal details in overly bright or dark scenes.
- **Advantages:** Operates in total darkness; detects heat signatures through light obscurants; reveals camouflaged vehicles by thermal signature.
- **Limitations:** Thermal crossover (dawn/dusk periods when ambient and target temperatures equalize, reducing contrast); heavy rain and thick fog severely degrade performance; cannot read text or markings (no color/detail like TV).

#### Sensor Selection Guidelines

| Condition | Recommended Sensor | Reason |
|-----------|--------------------|--------|
| Bright daylight | TV | Best resolution and PID capability |
| Dusk / dawn | TIS (adjust gain/level) | Thermal crossover period — TIS may struggle; try both |
| Night (clear) | TIS | Only viable sensor |
| Night (haze/light fog) | TIS | Thermal penetrates light obscurants |
| Heavy fog/rain | TIS (degraded) | Limited effectiveness; consider aborting engagement |
| Smoke/dust | TIS | Thermal penetrates many battlefield obscurants |
| PID required (ROE) | TV (if light permits) | Only TV provides visual identification detail |

---

### 1.5 MMS Controls & Tracking Modes

#### Control Mapping (DCS HOTAS)

| Function | Default Control | Notes |
|----------|----------------|-------|
| **MMS Slew** | Cyclic-mounted hat/ministick (configurable) | Analog slew for coarse and fine movement |
| **FOV Toggle** | HOTAS button (configurable) | Cycle WFOV ↔ NFOV |
| **Sensor Toggle** | HOTAS button (configurable) | Toggle TV ↔ TIS |
| **Polarity Toggle** | HOTAS button or MFD OSB | WHT ↔ BLK (TIS only) |
| **LRF Pulse** | HOTAS button (configurable) | Single-press for range |
| **Laser Designate** | HOTAS button (configurable) | Press and hold for continuous laser designation |
| **Track Mode** | MFD OSB or HOTAS | Cycle through track modes |

> **Instructor Note:** Students should configure HOTAS bindings before the first weapons flight. Efficient MMS operation depends on muscle memory with slew, FOV, sensor toggle, and laser controls. Do not rely on mouse-clicking the MFD during tactical engagements.

#### Tracking Modes

| Mode | Behavior | Use Case |
|------|----------|----------|
| **Manual (No Track)** | MMS stays where the pilot slews it; no automatic tracking | Initial search; looking around the battlefield |
| **Point Track** | MMS automatically tracks a high-contrast point (vehicle, structure edge) | Locked onto a specific target; maintains crosshair on target during aircraft movement |
| **Area Track** | MMS tracks a ground area/region; maintains pointing at a geographic location | Observing a road junction or engagement area; MMS compensates for aircraft drift but doesn't track a moving target |
| **Inertial** | MMS maintains pointing at a fixed direction (stabilized against aircraft movement) | Observing a specific azimuth/bearing while maneuvering |

**Track Mode Selection:**
- Use **Manual** during initial sector search and wide-area scanning.
- Use **Area Track** when monitoring a specific engagement area or suspected target location.
- Use **Point Track** when locked onto a confirmed target for engagement — this is the mode used during Hellfire and APKWS designation.
- Use **Inertial** when you need the MMS to hold a direction while repositioning the aircraft.

**Track Stability:**
- Point Track requires sufficient contrast between target and background. It can lose lock on low-contrast targets, targets entering shadows, or targets obscured by smoke.
- If track is lost during laser designation, the missile loses guidance — **critical failure mode during Hellfire engagement**.

---

### 1.6 Laser Operations

#### Laser Rangefinder (LRF)

- **Function:** Fires a single laser pulse to measure range to the point under the crosshair.
- **Output:** Range in meters displayed on MFD.
- **Use Cases:**
  - Pre-engagement range checks (verify target is within weapon envelope).
  - Coordinate extraction (range + MMS azimuth/elevation + aircraft GPS → target LAT/LONG).
  - Updated range for CCIP calculations (rocket/gun pipper accuracy).

#### Laser Designator (LRD)

- **Function:** Fires continuous coded laser energy at the PRF code set on the MFD. The reflected laser energy provides guidance for SAL-homing weapons (Hellfire K/M/N, APKWS).
- **Activation:** Press and hold the laser designate control. The laser fires continuously while held.
- **PRF Code:**
  - 4-digit Pulse Repetition Frequency code that identifies this specific laser.
  - Set on the MFD weapons/MMS page.
  - The weapon seeker must be set to the **same PRF code** to home on this laser's energy.
  - Default code is typically **1688** — can be changed for multi-ship operations and buddy lasing.
- **Laser Safety / Arming:**
  - The laser has an **ARM/SAFE** state controlled via the cockpit.
  - Laser must be **ARMED** before the designator will fire. The rangefinder may operate regardless of arm state.
  - ARM the laser only when entering the engagement sequence — keep SAFE during transit and non-tactical flight.

#### Lasing Timeline

| Phase | Hellfire (LOBL) | Hellfire (LOAL) | APKWS |
|-------|----------------|-----------------|-------|
| **Pre-Launch** | Lase continuously; missile confirms lock before launch | Do NOT lase — missile launches blind on trajectory | Do NOT lase — aim with CCIP reticle |
| **Mid-Flight** | Continue lasing — missile is guiding on reflected energy | Begin lasing ~5–10 sec before estimated impact (depends on mode and range) | Begin lasing before rocket enters terminal guidance phase |
| **Terminal** | Maintain laser on target until impact | Maintain laser on target until impact | Maintain laser on target until impact |
| **Post-Impact** | Cease lase; conduct BDA | Cease lase; conduct BDA | Cease lase; conduct BDA |

> **Instructor Note:** The most critical student failure with laser-guided weapons is **breaking laser designation before impact**. Emphasize: the laser is the weapon's eyes. If you stop lasing, the weapon goes stupid. Maintain designation until you see the flash of impact.

#### Self-Designation vs. Buddy Lasing

| Method | Description | PRF Coordination |
|--------|-------------|------------------|
| **Self-Designation** | OH-58D MMS lases the target; own Hellfire/APKWS homes on own laser | Weapon PRF = MMS PRF (same aircraft — automatic) |
| **Buddy Lase (Designate for Others)** | OH-58D MMS lases; Apache/A-10/Harrier fires weapon that homes on Kiowa's laser | Coordinate PRF code via radio; shooter sets weapon to Kiowa's code |
| **Receive Buddy Lase** | JTAC/FAC/wingman lases; OH-58D fires Hellfire/APKWS that homes on external laser | Set MMS/weapon PRF to match external designator's code |

**Buddy Lase Communication Flow:**
1. "Lasing, code [PRF], [bearing/range from reference point]."
2. "Copy, code [PRF], tally target."
3. "Cleared hot" / "Rifle" (Hellfire) or "Rockets" (APKWS).
4. "Spot" — confirms laser is on.
5. "Splash" — weapon impact.

---

### 1.7 Target Acquisition Workflow

#### Search → Detect → Identify → Classify → Engage → BDA

| Step | Action | MMS Activity |
|------|--------|-------------|
| **Search** | Systematic scan of assigned sector | WFOV; TIS or TV per conditions; Manual or Area Track mode |
| **Detect** | Spot a potential target | NFOV; slew to suspect contact; begin closing for identification |
| **Identify** | Determine what the contact is | NFOV/Zoom; TV for visual ID if light permits; TIS for thermal signature analysis |
| **Classify** | Determine friend/foe/neutral and target priority | PID per ROE; check against known friendly positions; communicate with ground element |
| **Engage** | Commit to weapons employment | Point Track on target; select weapon; arm laser; execute firing sequence |
| **BDA** | Assess results post-strike | Maintain MMS on impact point; observe for secondary explosions, target movement, surviving threats; report results |

#### Systematic Search Patterns

- **Sector Scan:** Divide assigned sector into left/center/right sub-sectors; scan near-to-far in each sub-sector; overlap sub-sectors for complete coverage.
- **Road/Trail Scan:** Follow linear features (roads, trails, power lines) that canalize enemy movement.
- **Key Terrain Scan:** Prioritize likely enemy positions: treelines, ridgelines, intersections, defiles, built-up areas.
- **Threat-First Scan:** Scan for highest-threat systems first (air defense, armor) before methodically clearing the sector.

#### Grid Coordinate Extraction

The MMS can generate target coordinates by combining:
- Aircraft GPS position.
- MMS azimuth and elevation pointing angles.
- LRF slant range to target.

The computed target LAT/LONG is displayed on the MFD and can be:
- Reported to ground forces ("Target at grid [coordinates], [description]").
- Used for indirect fire (artillery/mortar) call-for-fire.
- Entered as a target point for JDAM-equipped platforms.

> *⚠ Realism Divergence: Real-world OH-58D coordinate extraction accuracy depends on aircraft GPS quality, LRF range accuracy, and MMS pointing calibration — typical error ~50–100 m CEP at longer ranges. DCS may provide more precise coordinates than a real-world system would. Instructors should note that in reality, grid coordinates from a mast sight at 5+ km are approximate and require confirmation.*

---

### 1.8 Common Student Errors — MMS

| Error | Consequence | Correction |
|-------|-------------|------------|
| Forgetting to arm the laser before engagement | Laser does not fire; weapon has no guidance energy | Always confirm LASER ARMED indication on MFD before starting engagement sequence |
| Using TV at night or in low visibility | Blank/unusable image; missed targets | Switch to TIS for night/degraded conditions; verify sensor selection as part of pre-engagement check |
| Leaving MMS in WFOV for engagement | Target too small to identify or precisely designate | Switch to NFOV before final target ID and engagement; WFOV is for search only |
| Breaking Point Track during aircraft maneuver | MMS loses lock; laser drifts off target; weapon loses guidance | Minimize aggressive maneuvering during laser designation; if track breaks, re-acquire immediately or abort shot |
| Not verifying PRF code match before buddy lase | Weapon cannot see laser; guides on noise or wrong laser | Always confirm PRF code coordination on radio; verify code displayed on MFD matches briefed code |
| Failing to boresight before first engagement | Crosshair does not match laser point; weapons miss by offset distance | Perform ground boresight at FARP before mission; verify boresight with LRF range check against known distance |
| Slewing MMS too aggressively during fine tracking | Overshoot target; slow re-acquisition | Use fine slew for final aiming; reduce slew input near target |
| Not conducting BDA after strike | Unknown engagement result; possible re-attack needed but not initiated | Immediately post-impact, maintain MMS on target area; observe for 5–10 seconds; report results |

---

## Module 2 — Weapons Management System & HUD Symbology

### Learning Objectives

- Navigate the MFD weapons pages and identify all weapon status indications.
- Execute the Master Arm sequence and describe each arming state.
- Interpret HUD/MFD weapons symbology for Hellfire, rockets, gun, and APKWS.
- Perform emergency and selective jettison procedures.
- Conduct a weapon system BIT and interpret ready/not-ready indications.

---

### 2.1 Weapons MFD Pages

The OH-58D does not have a centralized stores management system like the A-10C's DSMS. Instead, weapons are managed through dedicated **MFD pages** accessed via the Option Select Buttons (OSBs).

#### Weapons Page — Overview

| Display Element | Description |
|----------------|-------------|
| **Selected Weapon** | Currently active weapon type (HF = Hellfire, RKT = Rockets, GUN = .50 cal, APKWS) |
| **Weapon Inventory** | Per-station count of remaining weapons (e.g., "L: 2 HF / R: 7 RKT") |
| **Weapon Readiness** | RDY (ready to fire), NOT RDY (system constraint — not armed, out of envelope, etc.) |
| **Guidance Mode** (Hellfire) | LOBL, LOAL-DIR, LOAL-LO, LOAL-HI |
| **PRF Code** | Current laser code assigned to the weapon |
| **Fuze Status** | Arming wire status, fuze selection if applicable |
| **Master Arm State** | SAFE / ARM indication on weapons page |

#### Weapon Selection Cycle

| Action | Result |
|--------|--------|
| Press WPN SELECT OSB or HOTAS weapon cycle | Cycles through loaded weapons: HF → RKT → GUN → APKWS → (repeat) |
| Press specific weapon OSB on MFD | Jumps directly to that weapon type |

> **Instructor Note:** Students must be able to rapidly select the correct weapon type without cycling through all options. During a multi-target engagement, time spent fumbling with weapon selection is time spent exposed. Recommend assigning direct-select HOTAS bindings for primary weapons.

#### Hellfire Sub-Page

| Element | Description |
|---------|-------------|
| **Missile Count** | Remaining missiles per pylon |
| **Variant** | K / M / N — displayed per loaded missile |
| **Guidance Mode** | LOBL / LOAL-DIR / LOAL-LO / LOAL-HI — selectable via OSB |
| **PRF Code** | 4-digit code; editable via OSB/MFD |
| **Seeker Status** | TRACKING / NO TRACK / LOCK — SAL seeker status (LOBL mode) |
| **Constraints** | In-range / out-of-range indication; launch acceptability region |
| **Priority / Channel** | Missile priority selection (PRI / ALT) if applicable |

#### Rocket Sub-Page

| Element | Description |
|---------|-------------|
| **Rocket Count** | Remaining rockets per pod |
| **Warhead Type** | Displayed per loaded warhead (M151 HE, M229 HE, M282 MPP, M156 WP, etc.) |
| **Quantity per Salvo** | Selectable: 1, 2, 4, 7 (full pod) |
| **CCIP Data** | Range, impact point status |
| **APKWS Mode** (if loaded) | Laser-guided mode; PRF code display |

#### Gun Sub-Page

| Element | Description |
|---------|-------------|
| **Round Count** | Remaining .50 cal ammunition |
| **Rate** | Fixed (~1,100 RPM) — not pilot-selectable |
| **CCIP Data** | Pipper position, range to impact |

---

### 2.2 Master Arm & Arming Sequence

#### Master Arm Switch

| Position | State | Effect |
|----------|-------|--------|
| **SAFE** | Weapons safed | No weapon can fire regardless of other switch positions; default state for all non-tactical flight |
| **ARM** | Weapons armed | Selected weapon is hot; trigger/pickle will fire if weapon-specific constraints are met |

**Location:** Master Arm switch is on the armament panel, typically left console or instrument panel (per DCS cockpit layout).

#### Full Arming Sequence

| Step | Action | Verification |
|------|--------|--------------|
| 1 | **Master Arm → ARM** | MASTER ARM indication on MFD; caution panel shows armed state |
| 2 | **Select weapon type** on MFD or HOTAS | Weapon type displayed; inventory confirmed |
| 3 | **Select guidance mode** (Hellfire) or **quantity** (rockets) | Mode/quantity displayed on weapons sub-page |
| 4 | **Verify PRF code** (laser weapons) | PRF code matches briefed code; matches MMS laser code |
| 5 | **Arm laser** (laser-guided weapons) | LASER ARMED indication on MFD |
| 6 | **Confirm weapon ready** | RDY indication on MFD weapons page |
| 7 | **Confirm in-envelope** | Range, altitude, airspeed within weapon parameters |
| 8 | **Fire / Pickle** | Weapon fires/launches |

#### De-Arming Sequence

| Step | Action | Notes |
|------|--------|-------|
| 1 | Cease fire; release trigger/pickle | — |
| 2 | Laser → SAFE (if armed) | Prevents inadvertent lasing |
| 3 | Master Arm → SAFE | Weapons safed; prevents inadvertent firing |
| 4 | Verify SAFE indications on MFD | Confirm all weapon pages show SAFE |

> **Instructor Note:** Master Arm should remain SAFE during all transit, hover-hold, and non-engagement phases. ARM only when commencing an engagement run and SAFE immediately after. This prevents sympathetic weapon release during turbulence, HOTAS fumbles, or unintended button presses.

---

### 2.3 Emergency & Selective Jettison

#### Emergency Jettison

| Item | Detail |
|------|--------|
| **Purpose** | Immediately shed all external stores for weight reduction in emergency (engine failure, combat damage, escape maneuver) |
| **Control** | Emergency jettison button — guarded, red, on armament panel |
| **Action** | Press — releases all stores from both pylons simultaneously |
| **When to Use** | Single-engine emergency requiring immediate weight reduction; combat egress requiring max performance; uncontrollable aircraft where stores drag prevents recovery |

#### Selective Jettison

| Item | Detail |
|------|--------|
| **Purpose** | Drop specific stores from one pylon for weight management or hung ordnance |
| **Control** | Selective jettison via MFD weapons page (select station → jettison) |
| **When to Use** | Hung missile; asymmetric load balancing; partial weight reduction |

> *⚠ Realism Divergence: Real-world OH-58D jettison procedures involve specific circuit-breaker and arming-wire safety considerations. DCS simplifies jettison to a button press with immediate stores separation. The emergency jettison button functions identically in concept but lacks the real-world safety interlocks and confirmation steps.*

---

### 2.4 HUD / MFD Weapons Symbology

The OH-58D displays weapons symbology primarily on the **MFD** (overlaid on the MMS video or on a dedicated weapons page) rather than a traditional fighter-style HUD. Some symbology may also appear on the pilot's flight display.

#### Hellfire Symbology

| Symbol | Meaning |
|--------|---------|
| **Crosshair (MMS)** | Laser aim point; center of MMS FOV |
| **Lock Diamond / Box** | Appears around target when SAL seeker detects reflected laser energy (LOBL) |
| **LOCK / TRK indication** | Seeker is tracking laser reflection; missile ready to guide |
| **NO TRK** | Seeker cannot see laser; check lasing, PRF code, range, LOS |
| **Mode annunciation** | LOBL / LOAL-DIR / LOAL-LO / LOAL-HI displayed |
| **Range bar / TOF** | Estimated time of flight; counts down after launch |
| **Launch acceptability region** | Indicates whether current range/geometry is within launch envelope |
| **MSL away annunciation** | Confirms missile has left the rail |

#### Rocket / APKWS Symbology

| Symbol | Meaning |
|--------|---------|
| **CCIP Reticle ("I-Beam")** | Continuously computed impact point; shows where rockets will impact based on current aircraft state |
| **Impact Point Marker** | Moves across the MFD as aircraft attitude/airspeed/altitude change |
| **Range readout** | Slant range from aircraft to computed impact point |
| **Quantity indicator** | Number of rockets in next salvo |
| **APKWS laser guidance overlay** | Additional symbology showing laser designation requirement (PRF code, laser status) |

#### Gun (.50 Cal) Symbology

| Symbol | Meaning |
|--------|---------|
| **CCIP Pipper** | Computed bullet impact point accounting for range, airspeed, bullet drop, and drift |
| **Bullet stream line** | Predicted bullet trajectory path |
| **Range readout** | Estimated range to ground impact |
| **Round count** | Remaining ammunition |

#### Common Symbology Elements

| Symbol | Meaning |
|--------|---------|
| **MASTER ARM** | Visible when Master Arm is in ARM position |
| **WEAPON TYPE** | Active weapon type annunciator (HF / RKT / GUN / APKWS) |
| **RDY / NOT RDY** | Weapon readiness for selected type |
| **ROUNDS / QTY** | Ammunition or weapon count remaining |

---

### 2.5 Weapon System BIT & Status

#### Pre-Flight Weapon BIT

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Access weapon BIT page on MFD | BIT options displayed per weapon type |
| 2 | Initiate Hellfire BIT | Missile status: GO / NO-GO per rail; seeker reports status |
| 3 | Initiate Rocket system BIT | Launcher circuitry check; continuity verified |
| 4 | Initiate Gun BIT | Feed system and trigger circuit verified |
| 5 | Review BIT summary | All weapons GO → proceed; any NO-GO → troubleshoot or fly with reduced capability |

#### Hangfire / Misfire Procedures

| Condition | Indication | Procedure |
|-----------|-----------|-----------|
| **Misfire** | Trigger pressed / pickle pressed; weapon does not fire; no launch indication | Wait minimum safe interval; re-attempt once; if second attempt fails → safe weapon → troubleshoot or select alternate weapon |
| **Hangfire** | Partial launch indication; weapon may be in delayed ignition | Do NOT re-fire; maintain aircraft heading clear of friendlies; wait safe interval; report condition; proceed to safe area for EOD assessment if applicable |
| **Hung Ordnance** | Weapon remains on rail/launcher after fire command | Safe Master Arm; select alternate weapon; attempt selective jettison if tactically appropriate; land with hung ordnance per procedures |

> *⚠ Realism Divergence: DCS generally does not simulate hangfire conditions or partial weapon malfunctions. Misfires may occur (weapon simply doesn't fire), but the complex real-world decision tree for hangfire/cook-off risk assessment is not modeled. Instructors should brief these procedures for doctrinal awareness even though DCS won't produce the failure mode.*

---

### 2.6 Common Student Errors — Weapons Management

| Error | Consequence | Correction |
|-------|-------------|------------|
| Forgetting Master Arm before engagement | Pickle/trigger press has no effect; wasted engagement opportunity; target escapes | Include "MASTER ARM — ARM" as a verbal callout in the engagement checklist; verify ARM annunciation before committing |
| Selecting wrong weapon type | Fires rocket when Hellfire intended (or vice versa); wrong warhead on target | Verify weapon type on MFD before pressing fire; use direct-select bindings |
| Not verifying PRF code before firing laser-guided weapon | Weapon seeker set to different code than laser; missile doesn't guide | PRF code verification is a mandatory step in arming sequence — check every time |
| Leaving Master Arm in ARM during non-engagement flight | Risk of sympathetic fire from turbulence or accidental trigger press | SAFE immediately after engagement; make it habit to verify SAFE after every engagement pass |
| Ignoring NOT RDY indication and attempting to fire | Weapon doesn't fire; wasted time troubleshooting in engagement zone | Respect the NOT RDY indication — check for out-of-envelope condition, safety state, or weapon malfunction before re-attempting |
| Not checking weapon inventory before committing to engagement | "Winchester" (out of ammo) discovery at worst possible moment | Brief loadout and check inventory during pre-engagement phase; track expenditures mentally throughout mission |

---

## Module 3 — AGM-114 Hellfire Employment

### Learning Objectives

- Identify the AGM-114 variants available on the OH-58D (K, M, N) and select the correct variant for a given target type.
- Describe the four guidance modes (LOBL, LOAL-DIR, LOAL-LO, LOAL-HI) and when to use each.
- Execute a complete Hellfire engagement from hull-down in LOBL mode.
- Execute a LOAL engagement with proper lasing timeline.
- Apply buddy-lase procedures for cooperative engagements.
- Manage launch envelopes (range, altitude, airspeed, aspect) and recognize out-of-envelope conditions.

---

### 3.1 Missile Variants

| Variant | Designation | Guidance | Warhead | Primary Target Set |
|---------|-------------|----------|---------|-------------------|
| **AGM-114K** | Hellfire II | Semi-Active Laser (SAL) | Tandem HEAT (shaped charge + precursor for ERA defeat) | MBTs, IFVs, heavy armor, hardened bunkers |
| **AGM-114M** | Hellfire II | Semi-Active Laser (SAL) | Blast-Fragmentation | Soft targets, light vehicles, boats, structures, troop concentrations |
| **AGM-114N** | Hellfire II (MAC) | Semi-Active Laser (SAL) | Metal Augmented Charge (Thermobaric) | Bunkers, caves, buildings, enclosed fighting positions, personnel in cover |

#### Variant Selection Decision Matrix

| Target Type | Recommended Variant | Rationale |
|-------------|-------------------|-----------|
| Main Battle Tank (T-72, T-80, T-90) | **AGM-114K** | Tandem HEAT defeats ERA and heavy composite armor |
| IFV / APC (BMP, BTR, M2) | **AGM-114K** | HEAT penetrates light-to-medium armor reliably |
| Light Vehicles / Trucks / Technicals | **AGM-114M** | Blast-frag provides wider damage radius; HEAT overpenetrates without sufficient behind-armor effect |
| Boats / Patrol Craft | **AGM-114M** | Blast-frag causes structural damage and crew casualties |
| Buildings / Structures | **AGM-114M** or **AGM-114N** | M for general destruction; N for thermobaric interior effect |
| Bunkers / Cave Entrances | **AGM-114N** | Thermobaric overpressure effect devastates enclosed spaces |
| Troop Positions in Cover | **AGM-114N** | MAC creates lethal overpressure wave in defilade positions |
| Troop Positions in Open | **AGM-114M** | Blast-frag provides best fragmentation pattern against exposed personnel |

#### AGM-114L (Longbow Hellfire) — Note

The AGM-114L is a **radar-guided (RF) fire-and-forget** missile associated with the AH-64D Apache Longbow's Fire Control Radar (FCR). The OH-58D **does not carry an FCR** and therefore:

- **Cannot self-designate** for the AGM-114L.
- The AGM-114L is **not a standard OH-58D weapon** in DCS or real-world operations.
- If available in the DCS loadout screen, it is **not recommended** for OH-58D employment. Use SAL variants (K/M/N) exclusively.

---

### 3.2 Guidance Modes

All SAL Hellfire variants use the same four guidance modes. The mode determines the **missile flight profile** and the **lasing timeline**.

#### Mode Overview

| Mode | Abbreviation | Missile Flight Path | Lasing Requirement | Best Use |
|------|-------------|--------------------|--------------------|----------|
| **Lock-On Before Launch** | LOBL | Direct proportional navigation to laser spot | Lase **before** launch; missile confirms lock pre-launch | Short-to-medium range; clear LOS; highest confidence shot |
| **Lock-On After Launch — Direct** | LOAL-DIR | Direct (line-of-sight) trajectory toward target area | Launch without laser; begin lasing before TOF expires | Medium range; LOS exists but lock unconfirmed pre-launch |
| **Lock-On After Launch — Low** | LOAL-LO | Low-trajectory loft; missile flies below ridgeline if possible | Launch without laser; lase during terminal phase | Short range; terrain between shooter and target |
| **Lock-On After Launch — High** | LOAL-HI | High loft trajectory; missile climbs then dives onto target | Launch without laser; lase during terminal descent | Long range; terrain obstacles; maximum standoff |

#### Mode Selection Guidelines

| Situation | Recommended Mode | Rationale |
|-----------|-----------------|-----------|
| Clear LOS to target, < 5 km | **LOBL** | Highest Pk; confirmed lock before committing missile |
| Clear LOS, 5–8 km, uncertain lock | **LOAL-DIR** | Missile can reach target before lock timeout if laser starts mid-flight |
| Partial terrain masking between shooter and target | **LOAL-LO** or **LOAL-HI** | Missile arcs over or around intervening terrain |
| Maximum standoff desired; target behind ridgeline | **LOAL-HI** | Highest trajectory allows longest range and greatest terrain clearance |
| Buddy lase (JTAC/FAC lasing, Kiowa shooting) | **LOAL-DIR** or **LOBL** | Depends on whether Kiowa can see the laser spot pre-launch |
| Multiple rapid engagements | **LOBL** | Fastest shot-to-shot cycle; immediate feedback on lock quality |

---

### 3.3 Employment Sequence — LOBL (Primary)

LOBL is the **primary Hellfire employment mode** for the OH-58D. It provides the highest probability of kill because the missile confirms guidance before launch.

#### Step-by-Step Procedure

| Step | Action | MFD/Cockpit Indication |
|------|--------|----------------------|
| 1 | **Occupy battle position** — hull-down; MMS unmasked above terrain | MMS video shows target area |
| 2 | **Acquire target** with MMS — search in WFOV; identify in NFOV | Target visible in MMS; range > minimum |
| 3 | **Point Track** target — engage MMS Point Track mode on target | PT indication on MFD; crosshair tracks target |
| 4 | **LRF range** — pulse LRF to verify target range | Range readout on MFD (confirm within 500 m – 8,000 m) |
| 5 | **Select Hellfire** on weapons page | HF displayed; variant confirmed (K/M/N) |
| 6 | **Select LOBL** mode | LOBL annunciated on MFD |
| 7 | **Verify PRF code** — MMS code matches missile seeker code | PRF code displayed on both MMS and weapons page |
| 8 | **Master Arm → ARM** | MASTER ARM annunciation on MFD |
| 9 | **Arm laser** | LASER ARMED indication |
| 10 | **Begin lasing** — press and hold laser designate | LASER FIRING indication; laser energy on target |
| 11 | **Wait for lock** — missile seeker acquires reflected laser | LOCK indication on MFD; audio tone (if implemented) |
| 12 | **Verify in-envelope** — range and constraints met | RDY indication; launch acceptability region shows valid |
| 13 | **Pickle (fire)** | MSL AWAY annunciation; missile departs rail |
| 14 | **Maintain lasing** — hold laser on target until impact | Crosshair on target; Point Track active; laser firing |
| 15 | **Impact** | Observe flash on MMS |
| 16 | **Cease lase** — release laser designate button | LASER OFF |
| 17 | **BDA** — observe target for secondary explosions, movement, destruction | MMS on target; report results |
| 18 | **Re-engage or safe** — select next target or Master Arm → SAFE | Weapon status updated |

> **Critical:** Do **NOT** release the laser before impact. The missile is guided by reflected laser energy — if the laser stops, the missile loses guidance and will miss. Maintain steady Point Track and laser until you see the impact flash.

---

### 3.4 Employment Sequence — LOAL

LOAL modes are used when LOBL lock cannot be obtained before launch (range, geometry, or terrain masking prevents the missile from seeing the laser pre-launch) or when the pilot wants to minimize exposure time.

#### LOAL General Procedure

| Step | Action | Notes |
|------|--------|-------|
| 1 | **Acquire target** with MMS; establish Point Track | Same as LOBL steps 1–4 |
| 2 | **Select Hellfire → LOAL mode** (DIR / LO / HI) | Mode selection based on range and terrain — see guidelines above |
| 3 | **Verify PRF code** | Must match — missile will search for this code after launch |
| 4 | **Master Arm → ARM** | — |
| 5 | **Arm laser** | Ready to lase when needed (do NOT lase yet in LOAL) |
| 6 | **Pickle (fire)** — missile launches on programmed trajectory | MSL AWAY annunciation; missile follows selected flight profile |
| 7 | **Note TOF** — estimated time of flight displayed | Start mental countdown |
| 8 | **Begin lasing** at appropriate time (see table below) | LASER FIRING; crosshair precisely on target |
| 9 | **Maintain lasing** until impact | Missile acquires laser, adjusts course, guides to impact |
| 10 | **Impact → cease lase → BDA** | Same as LOBL steps 16–18 |

#### LOAL Lasing Timeline

| Mode | Approximate TOF (at 4 km) | When to Start Lasing | Notes |
|------|--------------------------|----------------------|-------|
| **LOAL-DIR** | ~12–15 sec | 8–10 sec before estimated impact | Missile is flying direct; needs laser acquisition relatively early |
| **LOAL-LO** | ~15–20 sec | 8–10 sec before estimated impact | Missile on low arc; laser needed as it approaches target area |
| **LOAL-HI** | ~20–30 sec | 10–15 sec before estimated impact | Missile at high altitude; laser needed during terminal dive |

> **Instructor Note:** The exact lasing start time varies with range. As a rule of thumb: **start lasing at ~60–70% of estimated TOF** and hold until impact. It is always better to start lasing early (missile has more time to acquire and correct) than late (missile may fly past the laser acquisition window).

> *⚠ Realism Divergence: Real-world Hellfire employment uses detailed time-of-flight tables based on exact range, altitude, and temperature. DCS provides a simplified TOF estimate. The general principle (lase before terminal phase) is identical, but precise timing may differ. In DCS, erring on the side of earlier lasing is recommended — there is little penalty for lasing too early in LOAL.*

---

### 3.5 Launch Envelopes

#### Range Constraints

| Parameter | LOBL | LOAL-DIR | LOAL-LO | LOAL-HI |
|-----------|------|----------|---------|---------|
| **Minimum Range** | ~500 m | ~750 m | ~500 m | ~1,500 m |
| **Maximum Range** | ~8,000 m | ~8,000 m | ~6,000 m | ~8,000 m |
| **Optimum Range** | 1,500–5,000 m | 2,000–6,000 m | 1,000–4,000 m | 3,000–8,000 m |

> *⚠ Realism Divergence: Real-world Hellfire maximum range depends on variant, altitude, temperature, and atmospheric conditions. The 8 km figure is a nominal maximum. DCS models range primarily as a function of motor burn time and drag; atmospheric effects may be simplified.*

#### Altitude & Airspeed Constraints

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Minimum Launch Altitude** | ~50 ft AGL (hover fire) | Hull-down fire is standard; lower altitudes possible |
| **Maximum Launch Altitude** | ~15,000 ft MSL | Limited by missile motor performance at altitude |
| **Minimum Airspeed** | 0 KIAS (hover) | Hover fire is a primary OH-58D employment method |
| **Maximum Airspeed** | ~120 KIAS | Near Vne; missile launch at high speed is acceptable but limits maneuvering margin |
| **Recommended Engagement Speed** | 0–60 KIAS | Hover to slow forward flight; minimizes platform movement for steady MMS tracking |

#### Angle-Off Constraints

| Parameter | Limit | Notes |
|-----------|-------|-------|
| **Maximum look angle** | Varies by mode; generally ≤ 60° off missile flight path | Missile must be able to maneuver to reach laser spot after acquiring it |
| **LOBL** | Missile can tolerate up to ~30° off-axis at launch (seeker tracking pre-launch) | Self-corrects quickly |
| **LOAL** | Missile fired toward target area; laser spot must be within seeker FOV during acquisition | Greater offset = higher miss risk |

---

### 3.6 Tactical Employment Techniques

#### Hull-Down Engagement (Primary Technique)

The fundamental OH-58D Hellfire employment posture:

1. **Approach BP** at NOE altitude (25–50 ft AGL), terrain masked.
2. **Hover into hull-down position** — rise until MMS clears terrain; fuselage remains below cover.
3. **Acquire and identify** target using MMS (WFOV → NFOV → Point Track).
4. **Execute LOBL engagement sequence** (see 3.3 above).
5. **Maintain hull-down** throughout engagement — do not over-unmask.
6. **After impact, remask** — descend below terrain; move to alternate BP.

| Phase | Exposure | Duration |
|-------|----------|----------|
| Approach | None (fully masked) | As needed |
| Unmask to hull-down | MMS only | 20–60 sec (acquire, engage, BDA) |
| Remask | None | Immediate after BDA |

> **Instructor Note:** Hull-down discipline is the Kiowa's primary survivability tool. The smaller the exposure, the harder the aircraft is to detect. Students should practice minimizing time in hull-down — acquire quickly, shoot accurately, BDA fast, remask immediately.

#### Running Fire

Engagement during lateral or forward movement:

- Used when the battle position is compromised, during movement to alternate BP, or when multiple targets require rapid servicing.
- **Procedure:** Maintain 30–60 KIAS lateral or forward flight; MMS tracks target via Point Track; execute LOBL engagement during movement.
- **Advantage:** Harder to target; continuous movement complicates enemy return fire.
- **Disadvantage:** MMS tracking is less stable; higher miss risk; pilot workload increases.

#### Rapid Engagement (Unmask-Shoot-Remask)

Minimizing exposure to absolute minimum:

1. Pre-plan the engagement: know the target bearing and approximate range from map study or previous observation.
2. Rise to hull-down; MMS is already pointed in the correct azimuth.
3. Acquire target as rapidly as possible (MMS should be in NFOV, near the expected target area).
4. LOBL lock → fire immediately upon lock.
5. Maintain laser designation (can begin remasking while maintaining laser LOS — the mast allows this).
6. Remask after impact.

**Target time in hull-down: < 30 seconds** — acquire, lock, fire, guide, BDA, remask.

#### Ripple Fire

Engaging multiple targets sequentially:

1. Fire first missile → maintain laser → impact → BDA.
2. Immediately slew MMS to next target → Point Track → new LOBL lock → fire.
3. Repeat until Winchester (out of Hellfires) or targets destroyed.
4. Remask and move to alternate BP.

**Typical cadence:** 15–30 seconds between shots (target acquisition and lock time for each subsequent target).

#### Buddy Lase Operations

**OH-58D designates for another shooter:**

| Step | OH-58D Action | Shooter Action |
|------|--------------|----------------|
| 1 | Acquire and track target with MMS | Monitor frequency; prepare weapon |
| 2 | Report: "Lasing, code [PRF], target [description] at [grid]" | Set weapon PRF to match; report "Copied, code [PRF]" |
| 3 | Begin lasing | Report "Spot" (laser confirmed on) |
| 4 | Maintain lasing | "Cleared hot" from controlling authority → "Rifle" (launch) |
| 5 | Maintain lasing until "Splash" (impact) | Monitor weapon in flight |
| 6 | BDA: report target status | Copy BDA |

**OH-58D receives external designation:**

| Step | External Designator | OH-58D Action |
|------|-------------------|--------------|
| 1 | Acquires target; reports PRF code | Set weapon PRF to match external laser code |
| 2 | Reports "Lasing" / "Spot" | Confirm MMS can see target area; select Hellfire; LOBL or LOAL |
| 3 | Maintains laser | Fire when ready: "Rifle" |
| 4 | Maintains laser until "Splash" | Monitor MMS for impact |
| 5 | Reports BDA | Copy BDA |

---

### 3.7 Weight & Performance Impact

| Loadout | Weight (Approx.) | Impact on Performance |
|---------|------------------|----------------------|
| 4× AGM-114 (full Hellfire) | ~400 lbs | Significant reduction in hover ceiling and rate of climb; reduced maneuvering margin; approach power-limited MTOW in hot/high conditions |
| 2× AGM-114 + M260 rockets | ~300 lbs | Moderate performance impact; balanced loadout |
| 2× AGM-114 + .50 cal | ~350 lbs | Moderate impact; gun pod is heavier than a 2-missile rack |

> **Critical Planning Factor:** In hot/high conditions (temperature > 30°C, elevation > 3,000 ft), a fully loaded OH-58D (4× Hellfire, full fuel) may not be able to hover out of ground effect (HOGE). The pilot may need to perform a running takeoff and cannot use hull-down hover engagement until fuel is burned and weight decreases. **Always compute power available vs. power required before mission.**

---

### 3.8 Common Student Errors — Hellfire

| Error | Consequence | Correction |
|-------|-------------|------------|
| Firing LOBL without confirmed LOCK indication | Missile launches unguided; flies to last computed trajectory; misses | Wait for LOCK annunciation and audio tone before pickle; do not rush the shot |
| Breaking laser before impact | Missile loses guidance in terminal phase; misses or hits offset | Maintain laser until impact flash; count the TOF; resist urge to remask early |
| Wrong PRF code between MMS and weapon | Missile seeker cannot acquire laser; flies ballistic | Verify PRF match as mandatory step in arming sequence |
| LOAL lasing too late | Missile flies past target before acquiring laser; miss | Start lasing earlier than you think necessary; 60–70% of TOF as guideline |
| Over-unmasking (exposing fuselage above terrain) | Aircraft vulnerable to visual detection, small arms, MANPADS | Rise only until MMS clears; practice hull-down hover precision; instrument cross-check on radar altimeter |
| Not selecting correct variant for target | HEAT on soft target (overpenetration, low secondary damage) or blast-frag on heavy armor (insufficient penetration) | Brief target types pre-mission; select variant on weapons page before engagement |
| Hovering in same BP after engagement | Enemy identifies position; return fire on known location | Move to alternate BP after every engagement; never fire more than 2 missiles from same position |
| Forgetting to arm laser before going LOBL | Laser doesn't fire; seeker sees nothing; no lock achieved | LASER ARMED is a mandatory step; verify indication before initiating lasing |
| Excessive time in hull-down (target fixation) | Extended exposure increases vulnerability | Set personal time limit (e.g., 45 sec max); if no lock in 30 sec, remask and re-approach |

---

## Module 4 — Hydra 70 Unguided Rocket Employment

### Learning Objectives

- Identify available Hydra 70 warhead types and select the appropriate warhead for a given target.
- Configure the rocket weapons page (warhead, quantity per salvo, inventory).
- Interpret CCIP reticle ("I-beam") symbology for rocket delivery.
- Execute diving fire, running fire, and hover fire rocket profiles.
- Apply correct parameters (dive angle, airspeed, range) for accurate rocket delivery.
- Manage rocket dispersion and accuracy factors.

---

### 4.1 System Overview

#### M260 Launcher

| Parameter | Value |
|-----------|-------|
| **Designation** | M260 Lightweight Launcher |
| **Capacity** | 7 tubes (7 rockets per pod) |
| **Mounting** | Left and/or right UWP |
| **Maximum Loadout** | 14 rockets (2× M260 pods) — but this uses both pylons, precluding Hellfire or .50 cal |
| **Rocket Motor** | Mk 66 Mod 4 (common to all 2.75-inch / 70mm rockets) |
| **Rocket Diameter** | 2.75 inches (70 mm) |
| **Spin Stabilization** | Folding fins deploy after launch; rocket spins for stability |

#### Available Warheads (DCS OH-58D)

| Warhead | Type | Weight | Effect | Primary Target Set |
|---------|------|--------|--------|-------------------|
| **M151 HE** | High Explosive | 10 lbs | Blast + fragmentation; 10 m lethal radius | Troops in open, light vehicles, soft targets |
| **M229 HE** | High Explosive (Heavy) | 17 lbs | Larger blast radius; greater fragmentation | Structures, material targets, vehicle concentrations |
| **M282 MPP** | Multi-Purpose Penetrator | ~9 lbs | Shaped charge + frag; penetrates light armor | Light APCs, bunkers, hardened fighting positions |
| **M156 WP** | White Phosphorus | ~9 lbs | Incendiary + dense white smoke | Target marking ("Mark on my smoke"), incendiary, screening |
| **M257 Illum** | Illumination (Overt) | ~7 lbs | Visible light parachute flare; ~1 million candlepower | Night battlefield illumination; area denial awareness |
| **M278 IR Illum** | Illumination (Covert IR) | ~7 lbs | IR-only parachute flare; visible through NVGs | Covert night illumination for NVG-equipped friendlies |

#### Warhead Selection Guide

| Target / Situation | Recommended Warhead | Notes |
|-------------------|--------------------|----- |
| Troops in the open | **M151 HE** | Best frag pattern for personnel |
| Trucks, technicals, soft-skin vehicles | **M151 HE** or **M229 HE** | M229 for clustered targets; M151 for single vehicles |
| Structures / buildings | **M229 HE** | Heavier warhead for structural damage |
| Light armored vehicles (BTR, BRDM) | **M282 MPP** | Shaped charge defeats thin armor; uncertain against heavy armor |
| Bunkers / fighting positions | **M282 MPP** | Penetrating warhead |
| Target marking for CCA coordination | **M156 WP** | "Mark on my smoke" — visible to ground troops and other aircraft |
| Night illumination (overt) | **M257** | Use when concealment not required |
| Night illumination (covert/NVG) | **M278** | IR-only; invisible to naked eye |

---

### 4.2 CCIP Delivery System

The OH-58D provides a **Continuously Computed Impact Point (CCIP)** for rocket delivery, displayed as an "I-beam" reticle on the MFD.

#### CCIP Reticle Behavior

| Element | Description |
|---------|-------------|
| **I-Beam Pipper** | The computed ground impact point of the next rocket(s) based on current aircraft attitude, airspeed, altitude, and ballistic data |
| **Movement** | The pipper moves dynamically — changes in pitch, bank, airspeed, or altitude all shift the predicted impact point |
| **Range Arc / Bar** | Indicates slant range to the computed impact point; may include range rings or numeric readout |
| **Stabilization** | Pipper accounts for aircraft velocity vector; more stable in steady-state flight than in maneuvering |

#### CCIP Accuracy Factors

| Factor | Effect on Accuracy | Mitigation |
|--------|-------------------|------------|
| **Aircraft stability** | Unsteady platform → wandering pipper → dispersed impacts | Trim aircraft; fly steady state for 2–3 seconds before firing |
| **Dive angle** | Steeper dive = tighter dispersion; shallower = wider spread | Use 10–20° dive for best accuracy |
| **Airspeed** | Higher speed = less time of flight = less wind drift = tighter impact | Maintain 80–100 KIAS for best results |
| **Range** | Greater range = more dispersion from wind, motor variation, spin dynamics | Engage at 1,500–3,000 m for best accuracy |
| **Wind** | Crosswind displaces unguided rockets laterally | No good mitigation other than reduced range and multiple rounds |
| **Rotor wash** | At very close range / hover fire, rotor downwash can deflect rocket trajectory | Maintain > 800 m minimum range in hover fire |
| **G-loading** | Firing during a pull or turn changes rocket release geometry | Fire in wings-level, steady-state conditions |

> *⚠ Realism Divergence: DCS models rocket ballistics including gravity, drag, and wind drift. The CCIP calculation in DCS is generally accurate when the aircraft is in steady flight. Real-world Hydra 70 dispersion is somewhat larger than DCS typically shows due to motor variation, fin deployment inconsistency, and atmospheric turbulence not fully modeled in the sim.*

---

### 4.3 Employment Profiles

#### Diving Fire (Primary Method)

The most accurate unguided rocket delivery method. The pilot establishes a dive toward the target, places the CCIP pipper on the target, and fires.

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Dive Angle** | 10–20° | Steeper = tighter dispersion; 15° is a good standard |
| **Entry Altitude** | 800–1,500 ft AGL | Above small-arms effective range ceiling |
| **Airspeed** | 80–100 KIAS | Higher speed improves accuracy and reduces exposure |
| **Firing Range** | 1,500–3,000 m slant range | Sweet spot for accuracy vs. vulnerability |
| **Minimum Recovery Altitude** | 300 ft AGL | Do NOT descend below this during recovery; break off earlier if necessary |
| **Break-Off Range** | ~1,000 m | Cease fire and pull off; do not press below this range |

**Procedure:**
1. Establish inbound at entry altitude and airspeed.
2. Identify target on MFD/MMS.
3. Establish dive angle (push over smoothly to 10–20°).
4. Place CCIP pipper on target; let pipper stabilize for 1–2 seconds.
5. Fire (single or pairs depending on target size and confidence).
6. Observe impacts; adjust aim if re-firing.
7. Initiate pull-off at break-off range / minimum recovery altitude.
8. Break turn (typically 30–60° bank away from target area).

#### Running Fire (Level Delivery)

Used for area suppression or when dive attack is impractical (low ceiling, time pressure).

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Altitude** | 200–500 ft AGL | Low-level; increases vulnerability to ground fire |
| **Airspeed** | 60–100 KIAS | — |
| **Dive Angle** | 0–5° (level to slight nose-down) | Shallow angle = wider dispersion |
| **Range** | 1,000–2,500 m | Shorter range compensates for reduced accuracy |

**Disadvantage:** Wider dispersion pattern; higher risk of ground fire at low altitude; less time to observe and correct.

#### Hover Fire

Engagement from a stationary or near-stationary hover. Close-range, high-risk.

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Airspeed** | 0–20 KIAS | Hover or slow creep |
| **Range** | 800–2,000 m | Close range required for accuracy from hover |
| **Altitude** | Hover altitude — typically 30–100 ft AGL | Higher hover improves rocket trajectory (less drop) but increases exposure |

**Procedure:**
1. Establish stable hover at engagement altitude.
2. Aim aircraft (nose pointed at target — rockets are forward-fixed).
3. Place CCIP pipper on target.
4. Fire (short salvo — 1–2 rockets to observe fall of shot).
5. Adjust and re-fire.
6. Transition to forward flight or lateral movement immediately after engagement.

> **Instructor Note:** Hover fire with unguided rockets is inherently less accurate than diving fire and puts the aircraft in a vulnerable, stationary position. Use only when terrain prevents a dive attack or when engaging close-range opportunity targets. Always plan an escape route before initiating hover fire.

---

### 4.4 Weapons Page Setup

| Step | Action | Notes |
|------|--------|-------|
| 1 | Select **RKT** (Rockets) on MFD weapons page | Rocket sub-page displays |
| 2 | Verify warhead type displayed matches loaded warhead | Warhead type auto-detected from loadout |
| 3 | Select **quantity per salvo** (1, 2, 4, or 7) | 1 = precision; 2 = standard; 4 or 7 = area suppression |
| 4 | Verify rocket count (remaining per pod) | Track expenditure; 7 per pod total |
| 5 | Master Arm → ARM when ready to engage | — |
| 6 | CCIP pipper active on MFD | Pipper tracks ground impact point |

#### Quantity Per Salvo Selection

| Quantity | Use Case |
|----------|----------|
| **1** | Precision marking (WP); ranging shot; ammunition conservation |
| **2** | Standard engagement; small point target; balance of accuracy and effect |
| **4** | Area target; vehicle group; increased probability of hit |
| **7** (full pod) | Massed fires; large target area; danger-close suppression |

---

### 4.5 Dispersion & Accuracy

#### Expected Dispersion at Various Ranges

| Range | Dive Angle | Approximate Dispersion (CEP) | Notes |
|-------|-----------|------------------------------|-------|
| 1,500 m | 15° dive | ~10–15 m | Best case; stable platform, steady dive |
| 2,000 m | 15° dive | ~15–25 m | Standard engagement range |
| 3,000 m | 15° dive | ~30–50 m | Extended range; useful for area targets only |
| 2,000 m | Level (0°) | ~30–50 m | Running fire; wider spread |
| 1,500 m | Hover | ~20–30 m | Rotor wash and platform instability degrade accuracy |

> These are approximate values. Actual DCS dispersion depends on implementation details and may vary. Use ranging shots (single rocket) to calibrate before committing a full salvo.

#### Techniques for Improving Accuracy

1. **Trim the aircraft** — an in-trim aircraft provides a stable platform; out-of-trim causes the pipper to wander.
2. **Steady-state flight** — fly at constant airspeed, altitude, and dive angle for 2–3 seconds before firing.
3. **Use ranging shots** — fire 1 rocket; observe impact; adjust aim; fire for effect with remaining rounds.
4. **Minimize G-loading** — fire during wings-level, unaccelerated flight.
5. **Use CCIP pipper settling time** — the pipper moves rapidly during attitude changes; wait for it to stabilize.

---

### 4.6 Common Student Errors — Rockets

| Error | Consequence | Correction |
|-------|-------------|------------|
| Firing during a bank or pull | Rockets disperse widely; miss target | Wings-level, steady state before trigger; release back-pressure before firing |
| Pressing too close (below break-off range) | Risk of frag self-damage; insufficient recovery altitude; target fixation | Respect the 1,000 m break-off / 300 ft AGL minimum; call "PULL OFF" to self if needed |
| Using full-pod salvos at long range | All 7 rockets wasted on a miss; no ammo for follow-up | Use 1–2 rockets for initial observation; increase quantity only when confirmed on target |
| Not trimming aircraft before rocket run | Pipper wanders; aiming is fighting the aircraft; poor accuracy | Trim for airspeed and dive angle before entering firing range |
| Selecting wrong warhead for target | WP on armor (ineffective); HE when marking was needed | Brief warhead plan during pre-mission; verify warhead displayed on MFD matches intent |
| Hover fire at excessive range (> 2 km) | Rocket dispersion too wide to reliably hit point target | Reduce range or transition to diving fire for longer-range engagements |
| Forgetting Master Arm before rocket run | Trigger press yields nothing; wasted run exposes aircraft | "ARM — HOT — CLEARED" verbal cadence before committing to attack run |
| Not observing fall of shot | Unknown result; wastes ammunition on repeated blind salvos | Watch MMS or direct view for impact; adjust aim; report results |

---

## Module 5 — APKWS Laser-Guided Rocket Employment

### Learning Objectives

- Describe the APKWS (AGR-20A) guidance mechanism and how it differs from both unguided rockets and Hellfire missiles.
- Configure the APKWS weapons page including PRF code assignment.
- Execute an APKWS engagement with proper laser designation timing.
- Apply correct firing geometry to ensure the rocket enters the seeker acquisition basket.
- Select APKWS vs. Hellfire vs. unguided rockets based on target requirements.

---

### 5.1 System Overview

The APKWS (Advanced Precision Kill Weapon System), designated **AGR-20A**, is a **semi-active laser (SAL) guided 2.75-inch rocket**. It uses the standard Mk 66 rocket motor and a standard warhead (typically M151 HE) with an added **WGU-59/B DASALS** (Distributed Aperture Semi-Active Laser Seeker) guidance section inserted between the motor and warhead.

| Parameter | Value |
|-----------|-------|
| **Designation** | AGR-20A |
| **Guidance** | Semi-Active Laser (SAL) homing via WGU-59/B DASALS |
| **Motor** | Mk 66 Mod 4 (same as unguided Hydra 70) |
| **Warhead** | M151 HE (10 lb High Explosive) — primary; other warheads possible per configuration |
| **Launcher** | M260 (7-tube) — same launcher as unguided Hydra 70 |
| **Effective Range** | 1,500 m – 5,000 m |
| **Accuracy** | ~1–2 m CEP (vs. ~10–50 m CEP for unguided at same range) |
| **Guidance Requirement** | Laser designation from MMS or external source; PRF code match required |

#### How APKWS Guidance Works

1. The rocket is launched from the M260 launcher using CCIP aiming — same as an unguided rocket.
2. After motor burnout and fin deployment, the **DASALS seeker** activates and searches for reflected laser energy at the programmed PRF code.
3. The seeker has a **limited field of regard** (the "basket") — the rocket must be aimed close enough to the target that the seeker can see the laser reflection after launch.
4. Once the seeker acquires the laser spot, it sends steering commands to the guidance fins, adjusting the rocket's trajectory to home on the spot.
5. The rocket impacts at or very near the laser spot — transforming an area weapon into a point weapon.

> **Key Concept:** APKWS is NOT a missile — it has **limited maneuvering capability** compared to Hellfire. It can correct its trajectory by a few degrees but cannot perform large turns. The pilot must aim the aircraft reasonably close to the target before firing. Think of it as a "smart bullet" rather than a guided missile.

---

### 5.2 APKWS vs. Hellfire vs. Unguided — Decision Matrix

| Factor | Unguided Hydra 70 | APKWS (AGR-20A) | AGM-114 Hellfire |
|--------|-------------------|-----------------|-----------------|
| **Guidance** | None | SAL laser | SAL laser |
| **Accuracy** | ~10–50 m CEP | ~1–2 m CEP | ~1–3 m CEP |
| **Range** | 1,500–4,000 m | 1,500–5,000 m | 500–8,000 m |
| **Warhead** | Multiple options (10–17 lb) | M151 HE (10 lb) | HEAT/Blast-Frag/Thermobaric (20+ lb) |
| **Target** | Area targets, suppression | Point targets, low collateral | Armor, hardened, high-value |
| **Maneuvering** | Fixed ballistic | Limited correction (~2–5°) | Full proportional navigation |
| **Fire-and-forget?** | N/A (unguided) | No — requires laser through impact | No — requires laser through impact (SAL) |
| **Ammo Depth** | 7 per pod (14 max) | 7 per pod (14 max) | 2 per pylon (4 max) |
| **Cost per Round** | Low | Moderate | High |

#### When to Use APKWS

| Use APKWS When... | Instead of... | Reason |
|-------------------|--------------|--------|
| Target is a single vehicle, fighting position, or small structure | Unguided rockets | Precision needed; unguided likely to miss or require multiple salvos |
| Target is soft/light (truck, technical, dismounts in cover) | Hellfire | Hellfire warhead is overkill; APKWS conserves Hellfires for armor |
| Collateral damage must be minimized | Either | Small 10 lb warhead + precision = minimal collateral |
| Hellfire inventory is depleted | Hellfire | APKWS provides guided capability from rocket pod |
| Multiple dispersed soft targets | Hellfire | APKWS offers more rounds (7+ vs. 2–4 Hellfires) for multiple engagements |

---

### 5.3 Employment Sequence

#### Step-by-Step APKWS Engagement

| Step | Action | Notes |
|------|--------|-------|
| 1 | **Acquire target** with MMS | WFOV → NFOV → identify and confirm target |
| 2 | **Point Track** target with MMS | Crosshair locked on target; MMS stabilized |
| 3 | **Select APKWS** on weapons page | APKWS displayed; verify warhead, count |
| 4 | **Verify PRF code** | MMS PRF = APKWS PRF (must match for guidance) |
| 5 | **Master Arm → ARM** | MASTER ARM annunciated |
| 6 | **Arm laser** | LASER ARMED |
| 7 | **Establish attack profile** | Diving or running fire; aim aircraft so CCIP pipper approaches target |
| 8 | **Begin lasing target** | LASER FIRING; laser energy on target; reflected spot visible to seeker |
| 9 | **Place CCIP pipper near/on target** | APKWS needs to be launched within the seeker basket — aim accurately |
| 10 | **Fire** | Trigger press; rocket launches |
| 11 | **Maintain laser designation** | Continue lasing until impact — rocket guides to spot |
| 12 | **Impact** | Observe on MMS |
| 13 | **Cease lase → BDA** | Release laser; observe target; report results |
| 14 | **Re-engage or safe** | Select next target or Master Arm → SAFE |

> **Critical Difference from Hellfire:** With APKWS, you must **aim the aircraft** (using CCIP) AND **lase the target** simultaneously. The rocket needs to be launched within the seeker's acquisition basket, which means the CCIP pipper should be pointing close to the target area at the time of launch. With Hellfire LOBL, the aircraft pointing is less critical because the missile has full proportional navigation.

---

### 5.4 Seeker Acquisition Basket

The APKWS seeker can only acquire the laser spot if it is within a cone centered on the rocket's flight path.

| Parameter | Approximate Value |
|-----------|------------------|
| **Seeker FOV** | ~20° cone (half-angle ~10°) |
| **Maximum correction** | ~2–5° from boresight, depending on range and energy |
| **Implication** | Rocket must be aimed within ~5–10° of the target at launch |

**Practical Guideline:** If the CCIP pipper is on or very near the target at the moment of fire, the rocket is within the basket. If the pipper is far off (e.g., pointing at terrain 200 m from the target), the seeker likely will not acquire.

#### Basket Geometry by Attack Profile

| Profile | Basket Alignment | Risk of Missing Basket |
|---------|-----------------|----------------------|
| **Diving fire (15° dive)** | Rocket trajectory passes through target area; excellent basket alignment | Low — dive naturally points rocket toward ground target |
| **Running fire (level)** | Rocket arcs downward; basket sweeps across target area | Moderate — must be aimed accurately; less margin for error |
| **Hover fire** | Rocket fired near-level or slightly depressed; basket depends on target range | Moderate-High — shorter range helps but platform instability can shift basket |

---

### 5.5 Employment Profiles

APKWS uses the same general profiles as unguided rockets (Module 4) but with the addition of laser designation.

#### Diving Fire (Recommended)

| Parameter | Value |
|-----------|-------|
| **Dive Angle** | 10–15° |
| **Airspeed** | 80–100 KIAS |
| **Firing Range** | 1,500–3,000 m |
| **Entry Altitude** | 800–1,200 ft AGL |
| **Break-Off** | 1,000 m / 300 ft AGL |
| **Laser** | Lasing before fire; maintain through impact |

#### Running / Level Fire

| Parameter | Value |
|-----------|-------|
| **Altitude** | 200–500 ft AGL |
| **Airspeed** | 60–100 KIAS |
| **Range** | 1,500–2,500 m |
| **Laser** | Lasing before fire; maintain through impact |
| **Accuracy** | Reduced vs. diving fire; basin alignment more critical |

#### Hover Fire

| Parameter | Value |
|-----------|-------|
| **Airspeed** | 0–20 KIAS |
| **Range** | 1,000–2,000 m |
| **Laser** | Lasing before fire; maintain through impact |
| **Accuracy** | Good at shorter ranges; platform stability essential |

---

### 5.6 Buddy Lasing for APKWS

APKWS can home on an **external laser designation** (JTAC, FAC, wingman) if the PRF codes match.

| Step | External Designator | OH-58D Action |
|------|-------------------|--------------|
| 1 | Reports target and PRF code | Set APKWS weapon PRF to match external code |
| 2 | Reports "Lasing" / "Spot" | Aim aircraft using CCIP toward designated target area |
| 3 | Maintains laser | Fire APKWS when CCIP is in alignment with target area |
| 4 | Maintains laser until impact | "Rockets, code [PRF]" — report launch |
| 5 | — | "Splash" — report impact; BDA |

> **Instructor Note:** Buddy-lased APKWS requires good coordination — the OH-58D pilot must aim the aircraft toward the target area even though someone else is lasing. This is because the rocket still needs to be launched within the seeker basket. It is not a "fire anywhere" weapon.

---

### 5.7 Common Student Errors — APKWS

| Error | Consequence | Correction |
|-------|-------------|------------|
| Firing APKWS without laser active | Rocket launches unguided; reverts to ballistic trajectory; misses | Always confirm LASER FIRING before trigger pull; laser first, then fire |
| Poor CCIP alignment at launch (pipper far from target) | Rocket outside seeker basket; cannot acquire laser; misses | Place CCIP pipper on or near target before firing; think of it as "aimed guided" |
| PRF code mismatch between MMS and APKWS | Seeker cannot see laser; guides on noise or fails to acquire | Verify PRF match as mandatory step; same discipline as Hellfire |
| Treating APKWS like a Hellfire (firing without aiming) | Rocket doesn't have Hellfire's proportional nav; extreme off-axis shots fail | APKWS requires aircraft pointing; CCIP pipper must be near target |
| Breaking laser before impact | Rocket loses guidance in terminal phase; reverts to ballistic | Maintain laser until impact — identical discipline to Hellfire |
| Using APKWS against heavy armor | M151 HE warhead insufficient against MBT or IFV armor | Use Hellfire (K variant) for armored targets; APKWS is for soft/light targets |
| Firing at maximum range from hover | Limited rocket energy at extended range reduces maneuverability; miss | Reduce range to 1,500–2,000 m from hover; or use diving fire for longer-range shots |

---

## Module 6 — M3P .50 Caliber Machine Gun Employment

### Learning Objectives

- Describe the M3P .50 cal system characteristics, including fixed-mount limitation and ammunition capacity.
- Interpret CCIP pipper symbology for gun employment.
- Execute diving fire, running fire, and hover fire gun profiles.
- Manage recoil effects on aircraft handling.
- Apply ammunition conservation discipline.
- Identify appropriate target sets for .50 cal vs. other weapons.

---

### 6.1 System Data

| Parameter | Value |
|-----------|-------|
| **Designation** | M3P .50 Caliber Heavy Machine Gun |
| **Caliber** | 12.7 × 99 mm (.50 BMG) |
| **Type** | Pod-mounted, electrically driven |
| **Mount** | **Fixed forward-firing** on the **left UWP only** |
| **Traverse / Articulation** | **None** — the gun is fixed to the pylon; the pilot aims by pointing the aircraft |
| **Rate of Fire** | ~1,100 RPM |
| **Ammunition Capacity** | ~500 rounds |
| **Sustained Fire Duration** | ~27 seconds of continuous fire (500 rounds ÷ ~1,100 RPM) |
| **Effective Range (Point Target)** | 1,000–1,500 m |
| **Effective Range (Area Suppression)** | Up to 2,000 m |
| **Maximum Range** | ~6,800 m (ballistic maximum; not tactically useful) |
| **Muzzle Velocity** | ~890 m/s |
| **Ammunition Type** | Ball, AP, API, tracer (standard mix includes tracer for visual feedback) |

#### Mount Characteristics

The M3P is **fixed-firing, bore-sighted along the aircraft longitudinal axis**. Unlike the Apache's M230 chain gun which traverses and elevates independently, the OH-58D pilot must **aim the entire helicopter** at the target to aim the gun.

**Implications:**
- The pilot must fly the aircraft to place the CCIP pipper on the target — requires coordinated flight inputs.
- Cannot fire at targets to the side without banking/yawing the aircraft toward the target.
- Helicopter nose position = gun aim direction.
- In hover, the pilot uses pedal turns and cyclic pitch/roll to aim.

#### Pylon Limitation

The .50 cal occupies the **left UWP exclusively**, preventing the left pylon from carrying Hellfire or rockets. Typical loadouts when carrying the .50 cal:

| Left Pylon | Right Pylon | Mission Profile |
|-----------|-------------|-----------------|
| M3P .50 cal | 2× AGM-114 Hellfire | Scout/Attack — precision + self-defense |
| M3P .50 cal | M260 rockets (7× Hydra 70) | Light attack — area + point suppression |
| M3P .50 cal | M260 APKWS (7× AGR-20A) | Precision light attack |

---

### 6.2 CCIP Gun Symbology

| Symbol | Description |
|--------|-------------|
| **Gun CCIP Pipper** | Computed bullet impact point on the ground, accounting for range, airspeed, bullet drop, and drift |
| **Bullet Stream Line** | Predicted trajectory of the bullet stream from aircraft to impact |
| **Range Readout** | Estimated slant range from aircraft to the computed ground impact point |
| **Round Count** | Remaining .50 cal ammunition displayed on weapons page |
| **MASTER ARM** | Armed state indication |
| **GUN Selected** | Weapon type annunciator confirming .50 cal is active weapon |

#### CCIP Pipper Behavior

- The pipper moves **rapidly** with aircraft attitude changes — small pitch and yaw inputs cause large pipper displacement.
- The pipper accounts for **bullet drop** — at longer ranges, the pipper depresses below the aircraft nose to compensate for gravity.
- **Tracer observation** is the secondary aiming method: watch the tracer stream and "walk" rounds onto the target by adjusting aircraft attitude.

---

### 6.3 Employment Profiles

#### Diving / Running Fire (Primary Method)

The most effective .50 cal delivery method. The pilot establishes a shallow dive or level run toward the target, places the pipper on the target, and fires in controlled bursts.

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Dive Angle** | 5–15° | Shallower than rocket dive; steeper angles require faster recovery |
| **Airspeed** | 60–100 KIAS | Higher speed reduces exposure time and improves pipper stability |
| **Firing Range** | 800–1,500 m | Within effective range for point targets |
| **Entry Altitude** | 500–1,000 ft AGL | Lower entry than rockets/Hellfire; gun is a close-range weapon |
| **Break-Off Range** | 500 m | Close range break-off; initiate pull immediately after last burst |
| **Minimum Recovery Altitude** | 200 ft AGL | Lower because engagement is closer/shallower |

**Procedure:**
1. Inbound at entry altitude and airspeed, target identified.
2. Establish shallow dive (5–15°).
3. Place CCIP pipper on target; stabilize for 1 second.
4. Fire in **controlled bursts** (2–3 seconds per burst).
5. Observe tracer impacts; adjust aim between bursts.
6. Cease fire at break-off range; initiate pull-off maneuver.
7. Break turn away from target area.

#### Hover Fire

Close-range engagement from a stationary or near-stationary hover. High risk; used for self-defense or point-blank opportunity targets.

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Airspeed** | 0–20 KIAS | Hover or slow lateral creep |
| **Range** | 400–1,000 m | Close range; pipper accurate at short distance |
| **Altitude** | 30–100 ft AGL | Standard hover height |

**Procedure:**
1. Stabilize hover; identify target.
2. Aim aircraft nose at target using cyclic and pedals.
3. Place CCIP pipper on target.
4. Fire in short bursts (2–3 seconds).
5. Observe tracer impacts; adjust by pedal (azimuth) and cyclic (elevation).
6. Transition to forward flight immediately after engagement.

> **Instructor Note:** Hover fire with the .50 cal is an extreme close-quarters engagement. The aircraft is stationary, vulnerable, and the gun's recoil will disturb hover stability. Use only when absolutely necessary (self-defense, danger-close suppression). Transition away from hover as soon as the engagement is complete.

#### Lateral Break Fire

Suppressive fire while breaking off from a target or during evasive maneuvering:

1. During a break turn (30–60° bank), momentarily yaw the nose through the target bearing.
2. Fire a burst as the pipper sweeps across the target area.
3. Continue the break turn.

**Purpose:** Suppression, not precision. Forces the enemy to take cover during the aircraft's most vulnerable moment (break/egress). Accuracy is low — this is area fire.

---

### 6.4 Recoil Effects

| Effect | Description | Compensation |
|--------|-------------|-------------|
| **Yaw** | Gun recoil induces a yaw moment (nose tends to move in response to firing) | Anticipatory pedal input opposite to yaw tendency; short bursts minimize effect |
| **Pitch** | Minor pitch disturbance from sustained fire | Steady cyclic; trim for engagement speed before firing |
| **Hover Disturbance** | In hover, recoil-induced yaw is more pronounced (no forward airspeed for directional stability) | Use short bursts; re-stabilize between bursts; expect pedal workload to increase |
| **Airspeed Bleed** | Minimal — .50 cal recoil is far less than the A-10C's GAU-8 (~40 lbf vs. 19,000 lbf) | Not a significant factor; ignore for practical purposes |

> *⚠ Realism Divergence: DCS models .50 cal recoil effects to some degree, but the magnitude may be less than the real aircraft. Real-world OH-58D pilots report noticeable yaw disturbance in hover fire. DCS may understate this effect. Instructors should brief the real-world handling qualities even if the sim is more forgiving.*

---

### 6.5 Ammunition Management

With only ~500 rounds and a rate of fire of ~1,100 RPM, **ammunition management is critical**.

| Burst Duration | Rounds Expended | Percentage of Total |
|---------------|----------------|-------------------|
| 1 second | ~18 rounds | 3.6% |
| 2 seconds | ~37 rounds | 7.3% |
| 3 seconds | ~55 rounds | 11% |
| 5 seconds | ~92 rounds | 18.4% |
| 10 seconds | ~183 rounds | 36.7% |
| Continuous (27 sec) | ~500 rounds | 100% — Winchester |

**Discipline Guidelines:**
- **Standard burst:** 2–3 seconds (37–55 rounds). Sufficient to walk rounds onto a point target.
- **Suppressive burst:** 3–5 seconds. Used for area suppression of troop positions.
- **Never exceed 5 seconds continuous** except in extremis self-defense.
- **Monitor round count** on MFD after each engagement.
- **Report "Bingo guns"** when ammunition drops below 100 rounds (reserve for self-defense).

---

### 6.6 Target Selection

| Target | Effectiveness | Notes |
|--------|--------------|-------|
| Troops in the open | **Excellent** | .50 cal is lethal against exposed personnel |
| Unarmored vehicles (trucks, technicals) | **Excellent** | AP/API rounds penetrate engine blocks and crew compartments |
| Light boats / watercraft | **Excellent** | Hull penetration; disabling fire |
| Light structures (wooden buildings, sandbag positions) | **Good** | .50 cal penetrates wood, sandbags, light walls |
| IFV / APC (BMP-1, BTR-60) | **Marginal** | May penetrate thin armor at close range with AP; unreliable |
| APC (M113, BTR-80) | **Poor** | Insufficient penetration except at extreme close range, ideal angle |
| MBT (T-72, T-80) | **Ineffective** | .50 cal cannot penetrate main battle tank armor; do not engage |
| Radar / SAM sites (exposed components) | **Good** | Can damage antennas, radar dishes, exposed electronics, tires |

> **Rule of Thumb:** If it has visible armor plating, use Hellfire or rockets instead. The .50 cal is for soft targets, self-defense, and suppression.

---

### 6.7 Common Student Errors — .50 Cal

| Error | Consequence | Correction |
|-------|-------------|------------|
| Continuous fire (> 5 seconds) | Ammunition depleted in 2–3 passes; Winchester early in mission | Enforce burst discipline: 2–3 sec max per trigger pull; count "one-one-thousand, two-one-thousand, release" |
| Engaging armored vehicles with .50 cal | Rounds bounce off; no effect; wasted ammo and exposure time | PID target type before engaging; select Hellfire or rockets for armor |
| Not tracking tracer impacts for correction | Rounds miss; continued firing at same offset | Watch tracers; adjust aim between bursts; "walk" rounds onto target |
| Forgetting the gun is fixed-mount (aiming with MMS instead of aircraft) | MMS crosshair on target but gun is not aligned; rounds miss | The aircraft nose = gun aim. Fly the aircraft to put the CCIP pipper on target, not the MMS crosshair |
| Hover fire at long range (> 1,500 m) | Bullet drop and dispersion at long range makes hits unlikely from unstable hover platform | Close range (< 1,000 m) for hover fire; use diving fire for longer ranges |
| Not managing recoil in hover | Yaw excursion causes pipper to wander off target; rounds spray | Short bursts; re-stabilize between bursts; anticipate yaw with opposite pedal |
| Not reserving ammunition for self-defense | Gun Winchester with enemy troops nearby; no suppressive capability for egress | Reserve ~100 rounds minimum; report "Bingo guns" to flight lead |

---

## Module 7 — AIM-92 Stinger Air-to-Air Employment

### Learning Objectives

- Describe the AIM-92 Stinger ATAS system and its role as a self-defense weapon.
- Identify the engagement envelope (range, aspect, altitude) for the Stinger.
- Execute the Stinger employment sequence (if modeled in DCS).
- Apply self-defense doctrine: when to engage vs. when to evade.
- Recognize threat aircraft and their relative vulnerability to Stinger.

---

### 7.1 System Overview

| Parameter | Value |
|-----------|-------|
| **Designation** | AIM-92 Stinger (Air-to-Air Stinger — ATAS) |
| **Origin** | Adapted from FIM-92 Stinger MANPADS for helicopter air-to-air self-defense |
| **Guidance** | Infrared (IR) homing — passive all-aspect seeker |
| **Launcher** | ATAS launcher pod; typically 2 missiles per launcher |
| **Mounting** | Universal Weapons Pylon (UWP) — occupies one pylon |
| **Warhead** | ~3 lb HE blast-fragmentation with proximity and impact fuze |
| **Effective Range** | ~500 m – 4,500 m |
| **Maximum Speed** | Mach 2+ (supersonic) |
| **Seeker** | Dual-band IR (UV + IR) for IRCCM capability; all-aspect acquisition |
| **Fuzing** | Proximity and contact; dual mode |
| **IFF** | Not modeled in DCS; real-world systems include IFF interrogation |

#### DCS Implementation Status

> **Important:** The AIM-92 Stinger may or may not be available on the DCS OH-58D depending on the module version and Polychop's implementation status. If the Stinger is **not available in the DCS loadout**, this module serves as **doctrinal reference only**. Check the current DCS module documentation and loadout screen for availability.
>
> If unavailable in DCS: skip the cockpit procedures section and treat this module as a real-world doctrine briefing for situational awareness. The self-defense concepts and threat recognition principles remain valid regardless of whether the weapon is modeled.

---

### 7.2 Missile Performance

#### Engagement Envelope

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Minimum Range** | ~500 m | Missile arming distance; closer shots may not fuze |
| **Maximum Range** | ~4,500 m | Varies with target aspect, speed, altitude |
| **Optimum Range** | 1,000–3,000 m | Best Pk (probability of kill) zone |
| **Aspect** | All-aspect (front, side, rear) | Rear-aspect (tail-on) preferred for highest Pk due to strongest IR signature |
| **Target Speed (Max)** | Effective against subsonic and low-supersonic targets | Limited against fast jets in afterburner at long range (seeker may track but missile may not reach) |
| **Launch Altitude** | Surface to ~15,000 ft MSL | Effective at typical helicopter operating altitudes |
| **Launch Speed** | 0–120 KIAS (OH-58D speed range) | Helicopter forward speed has minimal effect on missile performance |

#### Seeker Characteristics

| Feature | Description |
|---------|-------------|
| **Acquisition Tone** | Low growl — seeker is scanning; detecting IR source but not locked |
| **Lock Tone** | High-pitched steady tone — seeker locked on target; ready to fire |
| **All-Aspect** | Can engage from front, side, or rear hemisphere |
| **IRCCM** | IR Counter-Countermeasure capability; resists basic flare decoys |
| **Cool-Down** | Seeker requires coolant gas; limited operating time once activated (~45 seconds typical for MANPADS; may be modeled differently in ATAS configuration) |

---

### 7.3 Employment Sequence (if modeled in DCS)

| Step | Action | Indication |
|------|--------|-----------|
| 1 | **Detect threat aircraft** | Visual or RWR; wingman callout; situational awareness |
| 2 | **Select Stinger** on weapons page | STG or ATAS displayed on MFD |
| 3 | **Master Arm → ARM** | MASTER ARM annunciated |
| 4 | **Activate seeker** (uncage) | Seeker growl tone audible — seeker scanning |
| 5 | **Point aircraft nose at threat** | Seeker requires aircraft pointing (within seeker gimbal limits) |
| 6 | **Acquire lock** | Tone changes from growl to high-pitched steady lock tone |
| 7 | **Confirm within engagement envelope** | Range 500–4,500 m; aspect acceptable |
| 8 | **Fire** (pickle) | Missile launches; trails smoke toward target |
| 9 | **Immediately break/evade** | Do NOT wait to observe results; begin defensive maneuvering |
| 10 | **Observe result** (if safe to do so) | Target destroyed / hit / missed; report |
| 11 | **Re-engage or disengage** | Fire second missile if available; or egress and call for fighter support |

> **Critical Doctrine:** After firing, your priority is **survival, not BDA**. The OH-58D is not a fighter. Fire the Stinger and immediately break into terrain — use terrain masking as your primary defense. Do not circle to watch.

---

### 7.4 Self-Defense Doctrine

#### Rules of Engagement

The OH-58D carries Stinger for **self-defense only** — it is NOT conducting an air superiority mission.

| Decision Point | Action |
|---------------|--------|
| Enemy helicopter detected; not currently engaged by it | **Do NOT engage** unless it is attacking you or friendly forces. Report position to higher; request fighter support |
| Enemy helicopter attacking you / your formation | **Engage** with Stinger if within envelope; break and evade simultaneously |
| Enemy fixed-wing (slow mover: Su-25, L-39) | **Engage** with Stinger if in envelope and attacking you; otherwise evade via terrain masking |
| Enemy fast jet (MiG-29, Su-27, F-4) | **Do NOT engage** with Stinger (outside practical envelope; extremely low Pk); immediately terrain mask, jettison stores if necessary, call for fighter support |
| Friendly aircraft nearby (potential fratricide) | **Confirm target hostile** before firing; IFF procedures; communicate with flight lead |

#### Defensive Priority Sequence

1. **Terrain mask** — get behind terrain immediately; nap-of-the-earth.
2. **Jettison stores** (if needed for speed/maneuverability) — emergency jettison for maximum performance.
3. **Dispense countermeasures** — flares against IR threats; chaff against radar threats.
4. **Fire Stinger** — if threat is within envelope and engaging you.
5. **Call for help** — "Mayday" or "Engaged defensive" on appropriate frequency; request fighter CAP.
6. **Egress** — run for friendly territory, FARP, or protected area.

> **Instructor Note:** Students instinctively want to fight. Drill into them that the Kiowa is a scout, not a fighter. The Stinger is a last-resort "get off me" weapon. The primary defense is ALWAYS terrain masking and evasion. Fighting an enemy fighter or attack helicopter in a prolonged engagement is suicidal in an OH-58D.

---

### 7.5 Air-to-Air Threat Environment in DCS

| Threat | Type | Stinger Effectiveness | Recommended Response |
|--------|------|----------------------|---------------------|
| **Mi-24 Hind** | Attack helicopter | **Good** — large, hot (2× engines), relatively slow | Stinger if engaging you; terrain mask and evade if possible |
| **Ka-50 Black Shark** | Attack helicopter | **Good** — single engine but exposed IR signature | Stinger + terrain mask; be aware of Ka-50's 30mm cannon range |
| **Mi-8 Hip** | Transport/armed helo | **Good** — large IR signature; slow; vulnerable | Stinger effective; but confirm ROE (may be transport with civilians) |
| **Su-25 Frogfoot** | Ground attack jet | **Moderate** — subsonic; 2× engines with moderate IR; can engage if in envelope | Stinger when in rear/side aspect; terrain mask immediately |
| **L-39 Albatros** | Light attack/trainer | **Good** — slow; small but hot engine; vulnerable to Stinger | Stinger effective in most aspects |
| **MiG-29 / Su-27** | Fighter | **Poor** — fast; difficult to achieve lock at speed; often outside envelope before you can fire | Do NOT engage; terrain mask immediately; jettison stores; call for fighters |
| **F/A-18, F-16** | Friendly (fratricide risk!) | **N/A — DO NOT ENGAGE** | PID before any engagement; confirm hostile on radio |

---

### 7.6 Common Student Errors — Stinger / Air-to-Air

| Error | Consequence | Correction |
|-------|-------------|------------|
| Attempting to dogfight enemy aircraft | OH-58D destroyed; not designed for air-to-air maneuvering | Fire Stinger and break; do not pursue; terrain mask is priority |
| Firing without confirmed hostile identification | Fratricide; shooting down friendly aircraft | Always PID; if in doubt, do not fire; radio confirmation |
| Waiting for BDA after Stinger launch | Stationary helicopter is easy target for enemy's return shot or wingman | Fire and break immediately; check results only when in safe position |
| Ignoring Stinger availability during mission planning | No air-to-air self-defense when enemy air threat exists | If air threat is briefed, consider loading Stinger on one pylon; accept reduced ground ordnance |
| Engaging fast jets at long range | Missile cannot reach target; wasted Stinger | Only engage targets within 3,000 m and within practical speed envelope |
| Not jettisoning stores when under air attack | Reduced speed and maneuverability; cannot outrun or out-turn threat | Jettison stores for max performance when survival is at stake |

---

## Module 8 — Countermeasures & Defensive Systems

### Learning Objectives

- Describe the OH-58D countermeasures suite (chaff, flares, RWR).
- Configure and operate the countermeasures dispenser (manual and programmed modes).
- Interpret RWR threat display symbology and audio cues.
- Execute threat-specific defensive reactions (IR MANPADS, radar SAMs, AAA, enemy aircraft).
- Apply rotary-wing defensive maneuvering techniques (terrain masking, NOE, break maneuvers, jinking).

---

### 8.1 Countermeasures Dispenser System

#### System Overview

| Parameter | Value |
|-----------|-------|
| **Dispenser Type** | AN/ALE-47 (or equivalent per DCS implementation) |
| **Countermeasure Types** | Chaff (radar decoy) and Flares (IR decoy) |
| **Chaff Capacity** | ~30 bundles (approximate; varies by loadout configuration) |
| **Flare Capacity** | ~30 cartridges (approximate; varies by configuration) |
| **Dispense Modes** | Manual, Semi-Automatic, Programmed (per DCS implementation) |
| **Location** | Dispenser pods mounted on fuselage or tailboom |

#### Countermeasure Types

| Type | Purpose | Effective Against | Ineffective Against |
|------|---------|-------------------|-------------------|
| **Chaff** | Radar decoy — creates false radar returns to break missile lock or confuse tracking radar | Radar-guided SAMs (SA-6, SA-8, SA-11, SA-15), radar-directed AAA (ZSU-23-4 Shilka) | IR-guided missiles, optically-aimed weapons, small arms |
| **Flares** | IR decoy — creates a heat source brighter than the aircraft to seduce IR seekers | IR-guided MANPADS (SA-7, SA-14, Igla, Stinger), IR SAMs (SA-9, SA-13), IR AAMs | Radar-guided missiles, AAA, small arms |

#### Dispense Controls

| Mode | Operation | Best Use |
|------|-----------|----------|
| **Manual** | Pilot presses chaff or flare button; single expenditure per press | Precise countermeasure deployment; maximum conservation |
| **Semi-Automatic** | Pressing dispense button triggers a pre-programmed burst sequence (e.g., 2 flares + 1 chaff) | Standard defensive response; balanced between conservation and effectiveness |
| **Programmed / Auto** | System dispenses countermeasures automatically based on pre-set programs or RWR cueing | High-threat areas; when pilot workload prevents manual dispensing |

> *⚠ Realism Divergence: DCS countermeasures dispensing may be simplified compared to the real AN/ALE-47, which supports complex programming with multiple programs, timing sequences, and RWR-cued automatic dispensing. DCS may implement manual and/or semi-automatic modes only. The real system's full programmability may not be modeled. Check DCS module-specific documentation for exact implementation.*

#### Countermeasures Control Panel

| Control | Function |
|---------|----------|
| **CM Mode Switch** | OFF / MAN / SEMI / AUTO |
| **Chaff Button** | Manual chaff dispense (may be HOTAS-mappable) |
| **Flare Button** | Manual flare dispense (may be HOTAS-mappable) |
| **Program Select** | Selects pre-set CM program (1–6, if implemented) |
| **Jettison** | Emergency jettison of all remaining CM stores |

> **Instructor Note:** Map chaff and flare dispense to HOTAS buttons for immediate access. In a threat reaction, there is no time to reach for cockpit panel switches. HOTAS-mapped CM dispense is critical for survival.

---

### 8.2 Radar Warning Receiver (RWR)

#### System Overview

The RWR detects and displays radar emissions from threat systems, providing the pilot with situational awareness of radar-based threats.

| Parameter | Description |
|-----------|-------------|
| **Display** | Azimuth display showing relative bearing of radar emitters around the aircraft |
| **Symbology** | Threat-type symbols or numeric codes identifying the emitter type |
| **Audio** | Tone cues for new threats, lock-on, and launch detection |
| **Priority** | Prioritizes most dangerous threats (launch > lock > search) |

#### RWR Threat Display

| Element | Meaning |
|---------|---------|
| **Symbol at bearing** | A radar emitter is detected at that bearing relative to the aircraft nose |
| **Symbol type / number** | Identifies the threat system (e.g., "8" = SA-8, "11" = SA-11, "15" = SA-15, "S" = Search radar, "A" = AAA radar) |
| **Diamond / highlighted symbol** | Highest-priority threat (tracking/lock-on) |
| **Flashing symbol** | Launch detection — missile is in the air |

#### RWR Audio Cues

| Tone | Meaning | Required Response |
|------|---------|-------------------|
| **New contact tone** (single beep) | New radar emitter detected | Note bearing and type; assess threat level |
| **Steady warble / high-priority tone** | Radar has transitioned from search to track — you are being locked | Initiate defensive maneuver; dispense chaff; prepare for launch |
| **Launch warning** (rapid, urgent tone) | Missile launch detected | Immediate defensive action: break + countermeasures + terrain mask |

#### Common DCS Threat Systems

| RWR Symbol | Threat System | Type | Countermeasure |
|-----------|---------------|------|---------------|
| **2** | SA-2 Guideline | Radar SAM (long range) | Chaff + terrain mask + NOE (avoid overflying) |
| **3** | SA-3 Goa | Radar SAM (medium range) | Chaff + terrain mask |
| **6** | SA-6 Gainful | Radar SAM (mobile, medium range) | Chaff + terrain mask + NOE |
| **8** | SA-8 Gecko | Radar SAM (short range, mobile) | Chaff + terrain mask; operates with OH-58D's engagement zone |
| **11** | SA-11 Gadfly (Buk) | Radar SAM (medium range, mobile) | Chaff + terrain mask; extremely dangerous; avoid engagement zone |
| **15** | SA-15 Gauntlet (Tor) | Radar SAM (short range, very fast reaction) | Chaff + terrain mask; very difficult to defend against once locked |
| **S** / **23** | ZSU-23-4 Shilka | Radar-directed AAA | Chaff if radar-directed; terrain mask; stay outside 2,500 m range |
| **R** | EWR (Early Warning Radar) | Search only — no engagement | Note: means the enemy knows you're in the area; expect SAM/fighter activity |

---

### 8.3 Defensive Maneuvering — Rotary-Wing Specific

Rotary-wing defensive maneuvering differs fundamentally from fixed-wing tactics. The OH-58D's primary defense is **terrain masking**, not speed or high-G maneuvering.

#### Terrain Masking (Primary Defense)

| Technique | Description |
|-----------|-------------|
| **Terrain Flight** | Fly at extremely low altitude (NOE: 25–50 ft AGL; contour: 50–100 ft AGL) using terrain features to block line-of-sight from threat |
| **Ridgeline Masking** | Place a ridge, hill, or elevated terrain between aircraft and threat |
| **Treeline / Forest Masking** | Fly behind or within treeline cover; dense forest blocks visual and many radar LOS |
| **Urban Masking** | Use buildings and structures as LOS blockers in urban environment |
| **Defilade** | Aircraft below the crest of terrain; only MMS (mast) above cover (hull-down = tactical; full defilade = survival) |

**Terrain masking is the most effective defense available to a helicopter.** An SA-11 cannot hit what it cannot see. No amount of chaff or flares replaces being behind a hill.

#### Nap-of-the-Earth (NOE) Flight

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Altitude** | 25–50 ft AGL | Below treeline; using terrain contours |
| **Airspeed** | 40–80 KIAS | Speed limited by obstacle avoidance reaction time |
| **Visibility Requirement** | Must see terrain features ahead; degraded in night/IMC | NVGs essential for night NOE |
| **Risk** | Wire strike, CFIT, controlled flight into terrain | Highest risk flight regime — requires constant terrain awareness |

> **Instructor Note:** NOE flight is extraordinarily demanding. Students should have mastered basic low-level flight before attempting NOE in a threat environment. In DCS, the wire/obstacle hazard is somewhat reduced but terrain CFIT is fully modeled.

#### Break Maneuvers

| Maneuver | Technique | Use Case |
|----------|-----------|----------|
| **Break Turn** | 45–60° bank; pull to accelerate turn; descend toward terrain | Generic defensive response; puts energy into turn rate; closes with terrain |
| **Diving Break** | Push nose down while banking; trade altitude for speed; terrain mask | When above terrain and need to rapidly descend behind cover |
| **Pedal Turn** (hover) | Rapid 90–180° pedal turn to present smallest profile and initiate escape heading | From hover; break LOS; transition to forward flight immediately |
| **Terrain Reversal** | Reverse direction behind terrain feature; threat loses LOS | When flying along a ridgeline; reverse behind the ridge to break tracking |

#### Jinking

Random, unpredictable flight path changes to defeat tracking solutions:

- Change heading ±30° every 3–5 seconds.
- Change altitude ±50 ft.
- Vary airspeed ±20 KIAS.
- **Do NOT establish a predictable pattern** — the purpose is randomness.
- Most effective against optically-aimed weapons (AAA, MANPADS gunners); less effective against radar tracking.

#### Flare Dispensing During Defensive Maneuver

| Situation | Dispense Pattern | Notes |
|-----------|-----------------|-------|
| IR MANPADS launch detected | Multiple flares (3–5) in rapid succession + break turn | Flares must be hotter than aircraft; break turn puts aircraft heat source at different bearing than flares |
| Sustained IR threat | Continuous flare dispensing (1 per 2–3 seconds) while terrain masking | Conservation is secondary to survival; dispense until masked |
| Radar SAM launch | Chaff burst (2–3 bundles) + break turn + terrain mask | Chaff creates radar clutter; break changes tracking geometry |
| Mixed threat | Chaff + flares simultaneously | If unsure of threat type, dispense both |

---

### 8.4 Threat-Specific Defensive Reactions

#### IR MANPADS (SA-7 Grail, SA-14 Gremlin, SA-16/18 Igla, Stinger)

| Phase | Action |
|-------|--------|
| **Detection** | Often no RWR warning (passive IR — no radar emission); first indication may be launch trail or wingman call |
| **Immediate Response** | FLARES (multiple) + break turn into terrain + descend |
| **Sustained** | Continue dispensing flares; terrain mask; NOE flight away from threat |
| **Key Point** | MANPADS are launch-and-leave weapons; once you break LOS and defeat the first missile, the threat is from a different shooter, not the same one re-engaging |

#### Radar SAMs (SA-8, SA-11, SA-15)

| Phase | Action |
|-------|--------|
| **RWR Search Detection** | Note bearing; assess range; begin planning escape route toward terrain cover |
| **RWR Lock / Track** | CHAFF + break turn; descend to NOE; put terrain between aircraft and threat bearing |
| **RWR Launch** | CHAFF (multiple bursts) + aggressive break + terrain mask; dispense continuously until masked |
| **Key Point** | Against modern SAMs (SA-11, SA-15), chaff alone is often insufficient. **Terrain masking is essential.** Plan routes to avoid radar SAM engagement zones entirely |

#### Radar-Directed AAA (ZSU-23-4 Shilka)

| Phase | Action |
|-------|--------|
| **Detection** | RWR shows AAA tracking radar; tracer fire visible |
| **Immediate Response** | Jink + terrain mask; CHAFF if radar-directed; break away |
| **Key Point** | ZSU-23-4 effective range is ~2,500 m; maintain standoff > 3,000 m if possible. If inside engagement zone, jink aggressively and egress at maximum speed |

#### Optically-Aimed AAA & Small Arms

| Phase | Action |
|-------|--------|
| **Detection** | Tracer fire, muzzle flashes; no RWR warning (no radar) |
| **Immediate Response** | Jink; increase speed; break away from fire; terrain mask |
| **Key Point** | No countermeasures effective against optically aimed guns. Speed, jinking, and terrain are the only defenses. Keep moving; do not hover in threat areas |

---

### 8.5 SEAD/Threat Avoidance in Mission Planning

| Principle | Application |
|-----------|-------------|
| **Route planning** | Plot ingress/egress routes through terrain-masked corridors; avoid known SAM engagement zones |
| **Standoff engagement** | Use Hellfire max range (8 km) to engage from outside MANPADS (5 km) and AAA (2.5 km) envelopes |
| **Time-on-target discipline** | Minimize time in any area within threat engagement zones; rapid engagement cycles |
| **Altitude management** | NOE until weapons release; pop up only to engage; remask immediately |
| **Mutual support** | Wingman provides overwatch during engagement; can suppress or report threats |
| **SEAD coordination** | If friendly SEAD assets are available, coordinate suppression of enemy air defenses before entering threat areas |

---

### 8.6 Common Student Errors — Defensive Systems

| Error | Consequence | Correction |
|-------|-------------|------------|
| Not mapping CM to HOTAS | Cannot dispense chaff/flares quickly enough during threat reaction | Map chaff and flare to HOTAS before every mission; verify bindings |
| Dispensing flares against radar threats (or chaff against IR threats) | Wrong countermeasure; ineffective defense | Know the threat type from RWR (radar) or visual (IR launch trail); match countermeasure to threat |
| Flying above terrain when threats are present | Visible to radar and visual observation; easy target | Maintain NOE / terrain-masked flight in threat areas; only unmask to engage |
| Predictable jinking pattern | Enemy tracks pattern and anticipates; fires where you'll be | Randomize heading, altitude, and speed changes; no pattern |
| Ignoring RWR new-contact warnings | Surprised by lock-on or launch; no time to react | Acknowledge every RWR contact; assess threat bearing and type; plan escape route preemptively |
| Hovering in known threat area without terrain cover | Stationary target; easy kill for MANPADS, AAA, or SAM | Never hover in the open in a threat area; always have terrain cover behind you |
| Not pre-planning escape routes | When threatened, pilot doesn't know where to go; wastes time deciding | Brief escape routes (terrain corridors) before entering engagement area; know where the nearest cover is at all times |
| Waiting too long to dispense countermeasures | Missile is too close for countermeasures to be effective | Dispense immediately upon threat detection; better to waste CM than take a hit |

---

## Module 9 — Close Combat Attack Tactics & Engagement Area Operations

### Learning Objectives

- Distinguish CCA (Close Combat Attack) from CAS (Close Air Support) and explain why the OH-58D conducts CCA.
- Plan and execute a battle position (BP) engagement using hull-down technique.
- Develop and operate within an engagement area (EA) using target reference points, trigger lines, and sectors of fire.
- Execute scout/attack and hunter/killer team tactics.
- Apply rotary-wing attack profiles (hover fire, running fire, diving fire, pop-up).
- Conduct target handoff procedures with ground forces and other aircraft.

---

### 9.1 CCA vs. CAS — Doctrinal Distinction

| Concept | CAS (Close Air Support) | CCA (Close Combat Attack) |
|---------|------------------------|--------------------------|
| **Definition** | Air action against hostile targets in close proximity to friendly forces, requiring detailed integration with the fire and movement of those forces (Joint doctrine) | An attack by Army aviation assets providing direct fire support to ground maneuver forces, integrated through Army tactical command and control (Army doctrine) |
| **Who Conducts** | Fixed-wing aircraft (A-10, F/A-18, F-16, etc.); joint tasking | Army rotary-wing assets (AH-64, OH-58D) as organic maneuver elements |
| **Control** | Requires a JTAC (Joint Terminal Attack Controller); formal 9-line brief | Controlled by the ground maneuver commander via the aviation unit's command net; less formal control procedures |
| **Integration** | Joint operation; fires coordinated through ASOC/DASC | Organic Army fires; coordinated directly between aviation and ground maneuver units |
| **OH-58D Role** | OH-58D typically does not conduct formal CAS (lacks JTAC integration) | OH-58D conducts CCA as an organic Army Aviation scout/attack asset |

> **Key Takeaway for Training:** When an OH-58D Kiowa attacks enemy forces in support of ground troops, it is conducting **CCA, not CAS**. The coordination procedures are Army-centric (ground commander → aviation team leader → flight lead → wingman), not joint (JTAC → pilot). The distinction matters because it changes the control procedures, communication flows, and coordination authority.

> *⚠ Realism Divergence: In DCS multiplayer, the OH-58D often operates in a mixed environment where JTACs (human or AI) may use 9-line CAS procedures. While doctrinally incorrect for CCA, students should be familiar with both CCA and CAS communication formats since DCS missions may use either. The tactical principles (fire and maneuver, deconfliction, positive identification) remain identical regardless of the doctrinal label.*

---

### 9.2 Battle Position Operations

A **Battle Position (BP)** is a defensive or offensive position from which the OH-58D observes and engages targets in an assigned engagement area.

#### Selecting a Battle Position

| Criterion | Description |
|-----------|-------------|
| **Fields of Fire** | BP must provide clear LOS to the engagement area; MMS must be able to observe and designate targets at engagement ranges (1–8 km) |
| **Cover & Concealment** | BP must offer terrain cover for hull-down operations; the fuselage must be maskable behind terrain |
| **Mask** | A terrain feature (ridgeline, treeline, building) that permits hull-down exposure of MMS only |
| **Routes In/Out** | Covered routes to approach and depart the BP without exposing the aircraft; avoid skylining |
| **Alternate & Supplementary BPs** | Pre-plan at least 2 alternate positions; never plan to fight from one position only |
| **Distance from EA** | Within Hellfire range (1–8 km) of the engagement area; optimum 2–5 km for best accuracy and survivability balance |

#### Hull-Down Engagement Cycle

| Step | Action | Notes |
|------|--------|-------|
| 1 | **Approach BP** | NOE flight; terrain masked; arrive at BP from covered route |
| 2 | **Hover into hull-down** | Rise until MMS clears mask; fuselage below cover |
| 3 | **Scan EA** | MMS in WFOV; systematic search of assigned sector |
| 4 | **Detect & identify target** | MMS to NFOV; PID; classify as threat |
| 5 | **Engage** | LOBL Hellfire (primary); rockets or APKWS for lighter targets |
| 6 | **BDA** | Observe impact; report results |
| 7 | **Remask** | Descend below terrain; do not linger in hull-down |
| 8 | **Move to alternate BP** | After 1–2 engagements from same position, displace to prevent enemy counter-fire on known position |

#### Time in Hull-Down

| Guideline | Duration |
|-----------|----------|
| **Maximum recommended** | 45–60 seconds per unmask (search + engage + BDA) |
| **Optimal** | 20–30 seconds (pre-planned engagement: know where to look, shoot quickly, remask) |
| **Minimum** | 10–15 seconds (rapid shot: pre-sighted target, LOBL lock, fire, guide, remask) |

> **Instructor Note:** Students consistently spend too long in hull-down. They search slowly, fiddle with weapon settings, and forget to remask. Drill the cycle: unmask → scan → engage → BDA → remask. Treat hull-down time like breath-hold underwater — the clock is ticking.

---

### 9.3 Engagement Area Operations

An **Engagement Area (EA)** is a pre-planned area where the commander intends to destroy an enemy force using massed fires.

#### EA Development

| Element | Description |
|---------|-------------|
| **EA Boundary** | Defined geographic limits of the area where targets are expected and fires are authorized |
| **Target Reference Points (TRPs)** | Pre-designated points within the EA used for rapid target handoff ("From TRP 1, south 300 m, 2 vehicles") |
| **Trigger Lines** | Lines within the EA that trigger engagement; when enemy crosses a trigger line, specific weapons fire |
| **Engagement Priorities** | Pre-assigned priority: e.g., "Priority 1: air defense; Priority 2: armor; Priority 3: soft targets" |
| **Weapons Allocation** | Which weapons to use against which target types within the EA |

#### Sector of Fire Assignment

In multi-ship operations, each aircraft is assigned a **sector of fire** within the EA to prevent mutual interference and ensure complete coverage.

| Aircraft | Sector | Battle Position |
|----------|--------|----------------|
| **Lead (Kiowa 1)** | Left half of EA (270°–360° from friendly line) | BP Alpha (left flank) |
| **Wing (Kiowa 2)** | Right half of EA (360°–090° from friendly line) | BP Bravo (right flank) |

**Sector overlap zone:** ~10° overlap in the center to prevent a gap; coordination required for targets in the overlap.

#### Priority of Engagement

| Priority | Target Type | Weapon | Rationale |
|----------|------------|--------|-----------|
| 1 | **Air Defense** (SA-8, ZSU-23-4, MANPADS) | Hellfire K or M | Destroying enemy AD protects both aircraft and ground forces |
| 2 | **Armor** (MBTs, IFVs) | Hellfire K | Armor is the primary ground threat to friendly maneuver |
| 3 | **C2 Vehicles** (command posts, comm vehicles) | Hellfire M or APKWS | Disrupting enemy command degrades the entire formation |
| 4 | **Soft Targets** (trucks, troops, logistics) | Rockets, .50 cal, APKWS | Lower priority; lower-cost weapons appropriate |

---

### 9.4 Team Tactics

#### Scout/Attack Team (OH-58D + AH-64 Apache)

The classic Army Aviation team pairing:

| Role | Aircraft | Function |
|------|----------|----------|
| **Scout** | OH-58D Kiowa | Finds, identifies, and designates targets; provides laser designation for Apache Hellfire shots |
| **Attack** | AH-64 Apache | Fires Hellfire missiles guided by Kiowa's laser; provides heavy fires |

**Procedure:**
1. Kiowa advances to BP; hull-down observation of EA.
2. Kiowa detects and identifies target.
3. Kiowa reports: "Tally [target type] at [grid/TRP], preparing to lase, code [PRF]."
4. Apache confirms: "Copy, code [PRF], standing by."
5. Kiowa begins lasing: "Spot."
6. Apache fires: "Rifle."
7. Kiowa maintains laser until: "Splash."
8. Kiowa conducts BDA; reports results.
9. Cycle repeats for next target.

**Advantage:** The Kiowa takes the risk of forward observation; the Apache remains masked farther back with greater firepower. The Kiowa's small size and MMS mast make it harder to detect than the Apache.

#### Hunter/Killer (OH-58D + OH-58D)

Two Kiowas working as a team:

| Role | Aircraft | Function |
|------|----------|----------|
| **Hunter** | Kiowa 1 | Finds and designates targets; provides laser; may also engage |
| **Killer** | Kiowa 2 | Engages designated targets; receives buddy-lase or self-engages on separate targets |

**Employment:**
- Both aircraft occupy separate BPs with overlapping sectors of fire.
- The hunter finds targets; designates for the killer.
- After the killer shoots, roles can swap (the killer becomes the hunter at the next BP).
- This allows continuous observation and engagement with one aircraft always in a covering position.

#### Multi-Ship Coordination

| Element | Standard |
|---------|----------|
| **Spacing** | BPs separated by 500–2,000 m (visual contact or radio coordination) |
| **Communication** | Internal team frequency; rapid target handoff using TRPs and clock calls |
| **Deconfliction** | Vertical (one high, one low) or lateral (separate BPs); never cross each other's engagement arcs |
| **Weapons Hold / Tight / Free** | Hold = don't fire unless self-defense; Tight = fire only at targets positively identified as hostile; Free = fire at any target not confirmed friendly |

#### Clock Call Format

Rapid target handoff between team members:

> "Contact, [target type], [clock position from lead], [range], [altitude/description]."
> Example: "Contact, BTR, 2 o'clock, 3 klicks, moving south on road."

---

### 9.5 Attack Profiles — Rotary-Wing

| Profile | Description | Best For | Exposure |
|---------|-------------|----------|----------|
| **Hover Fire (Hull-Down)** | Stationary engagement from masked BP; MMS only exposed | Hellfire LOBL; precision observation; maximum stealth | Lowest (MMS only) |
| **Running Fire** | Engagement during lateral/forward flight at 30–80 KIAS | Rockets, .50 cal, Hellfire during displacement | Moderate (aircraft exposed during run) |
| **Diving Fire** | 10–20° dive toward target; rockets and gun primary | Hydra 70 rockets; .50 cal strafing | High (aircraft unmasked and descending toward threat) |
| **Pop-Up Attack** | NOE approach → rapid climb to weapons release → engage → descend behind terrain | Any weapon; used to surprise enemy; limited exposure time | Moderate-High (brief exposure at apex) |

#### Pop-Up Attack Procedure

| Step | Action | Notes |
|------|--------|-------|
| 1 | NOE approach toward target area | Terrain masked; navigating by map/GPS to planned pop-up point |
| 2 | At planned IP (Initial Point), climb rapidly | Full collective; climb at 40–60 KIAS |
| 3 | At apex (300–800 ft AGL), acquire target with MMS or visual | Quick scan; target should be near the expected location from map study |
| 4 | Engage | Rockets, gun, or snap LOBL Hellfire shot |
| 5 | Immediately push over and descend behind terrain | Break turn + descent; NOE egress |
| 6 | Egress along covered route to alternate BP or rally point | Do not return along the same route |

**Pop-up apex time:** Target < 15 seconds from climb to descent. Anything longer and the aircraft is a sitting target.

---

### 9.6 Target Handoff Procedures

#### Grid-Based Handoff

> "Target at grid [6-digit or 8-digit grid], [target description], [activity]."
> Example: "Target at grid NV 3847 5621, two T-72 tanks, stationary in treeline."

**Requires:** MMS coordinate extraction from LRF + GPS; transmitted to receiving element via radio.

#### TRP-Based Handoff

> "From TRP [number], [direction], [distance], [description]."
> Example: "From TRP 3, east 500 meters, BMP in defilade."

**Advantage:** Fastest method when TRPs are pre-briefed; no grid reference needed; both parties have TRPs on their maps.

#### Laser-Based Handoff

> "Lasing, code [PRF], target at [bearing/range from reference]."

**Used for:** Direct handoff to a Hellfire shooter (Apache, wingman) or buddy-lased APKWS.

#### Talk-On Procedure (Ground to Air)

When ground forces direct the aircraft onto a target they can see:

| Step | Ground Element | Aircraft |
|------|---------------|---------|
| 1 | "From my position, look [direction]" | Slew MMS to indicated bearing from ground element's position |
| 2 | "Range [distance], [terrain feature]" | Narrow search to indicated area |
| 3 | "Target is [description] at [specific feature]" | Identify target on MMS |
| 4 | — | "Tally target" (confirms visual on MMS) |
| 5 | "Cleared hot" or "You are cleared to engage" | Engage with appropriate weapon |

---

### 9.7 Common Student Errors — CCA Tactics

| Error | Consequence | Correction |
|-------|-------------|------------|
| Failing to plan alternate BPs | Stuck in one position; enemy identifies and suppresses the position | Always plan Primary, Alternate, Supplementary positions; displace after 1–2 engagements |
| Engaging without PID (Positive Identification) | Fratricide; engaging friendly vehicles or civilians | Always PID per ROE before firing; use MMS NFOV and TV sensor for identification |
| Not coordinating sectors of fire in multi-ship | Both aircraft engage same target; other targets escape; mutual interference | Brief sectors before mission; use TRP-based sectors; maintain communication |
| Skylining (silhouetting aircraft against sky) | Aircraft visible to enemy from below; easy target | Approach BPs from behind terrain; ensure background behind aircraft is terrain, not sky |
| Engaging targets beyond weapon effective range | Missile or rocket at extreme range has low Pk; wasted ordnance | Know effective ranges: Hellfire 2–6 km optimal; rockets 1.5–3 km; gun < 1.5 km |
| Not conducting BDA and immediately re-engaging destroyed targets | Wasting ordnance on already-destroyed targets | BDA each strike; confirm destroyed before moving to next target |
| Flying a predictable engagement pattern | Enemy anticipates next approach; lays ambush at expected BP | Vary approach routes, BPs, and timing; never be predictable |
| Target fixation (staring through MMS, ignoring aircraft state) | Aircraft drifts out of hull-down; altitude/airspeed decay; vulnerability increases | Cross-check instruments during MMS operations; maintain positional awareness |
| Not pre-planning the pop-up attack (winging it) | Long exposure at apex; can't find target; wastes time above terrain | Brief the target location, pop-up IP, expected target bearing from apex, and egress route before execution |

---

## Module 10 — Mission Planning & Loadout Optimization

### Learning Objectives

- Conduct threat analysis and map threat engagement zones for route planning.
- Select an optimal weapons loadout based on mission requirements, threat environment, and performance constraints.
- Plan engagement areas, battle positions, and coordination measures.
- Establish communication and laser code deconfliction plans.
- Configure loadouts and waypoints in the DCS Mission Editor.
- Apply weather and environmental considerations to weapons planning.

---

### 10.1 Threat Analysis

#### Intelligence Preparation of the Battlefield (IPB)

Before planning a weapons mission, the pilot must understand the threat environment. In DCS, this means studying the mission briefing and map for:

| Intelligence Element | What to Look For | Impact on Planning |
|---------------------|-----------------|-------------------|
| **Enemy Air Defense** | SAM sites (SA-6, SA-8, SA-11, SA-15); MANPADS units; AAA (ZSU-23-4, ZU-23) | Defines no-fly zones; dictates ingress/egress corridors; determines CM requirements |
| **Enemy Armor** | MBTs, IFVs, APCs — location, quantity, direction of movement | Determines Hellfire (K) loadout requirements; identifies primary EA |
| **Enemy Soft Targets** | Trucks, C2 vehicles, logistics, troop positions | Determines rocket/gun/.50 cal loadout balance |
| **Enemy Air Threat** | Fighters, attack helicopters — presence and activity | Determines Stinger loadout requirement; influences route altitude |
| **Terrain** | Ridgelines, valleys, treelines, urban areas | Identifies BP locations, covered routes, terrain masking opportunities |
| **Friendly Positions** | Ground unit locations, forward edge of battle area (FEBA) | Defines fire coordination lines; prevents fratricide; establishes rally/FARP locations |

#### Threat Ring Mapping

| Threat System | Engagement Range | Mapping Action |
|---------------|-----------------|----------------|
| **MANPADS** (SA-7/14/16/18) | ~5 km | Draw 5 km rings around known/suspected infantry positions |
| **SA-8 Gecko** | ~12 km | Draw 12 km ring; note: SA-8 is mobile — may relocate |
| **SA-11 Buk** | ~35 km | Draw 35 km ring; major no-fly zone for helicopter operations |
| **SA-15 Tor** | ~12 km | Draw 12 km ring; extremely fast reaction; very dangerous |
| **ZSU-23-4 Shilka** | ~2.5 km (effective) | Draw 2.5 km ring; typically co-located with armor formations |
| **Small Arms** | ~1 km (effective against helicopters) | Assume present along FEBA and near all enemy positions |

**Route Planning Rule:** Plot ingress and egress routes through gaps between threat rings, using terrain-masked corridors. If no gap exists, plan SEAD before entry or accept the risk with maximum CM and terrain masking.

---

### 10.2 Loadout Selection

The OH-58D's **two-pylon limitation** makes loadout selection one of the most consequential mission planning decisions. Every loadout is a tradeoff.

#### Standard Loadout Configurations

| Loadout | Left Pylon | Right Pylon | Mission Profile | Best For |
|---------|-----------|-------------|-----------------|----------|
| **Full Hellfire** | 2× AGM-114 | 2× AGM-114 | Maximum anti-armor | Armor-heavy EA; known tank formations; when gun/rockets not needed |
| **Scout/Attack** | M3P .50 cal | 2× AGM-114 | Balanced recon + precision | Scout mission with engagement authority; most versatile for unknown threat mix |
| **General Purpose** | M260 rockets (7× Hydra 70) | 2× AGM-114 | Mixed precision + area | Mixed target set (armor + soft); most common combat loadout |
| **APKWS Mix** | M260 APKWS (7× AGR-20A) | 2× AGM-114 | Precision-heavy | When all targets require guided weapons; low collateral damage missions |
| **Light Scout** | M3P .50 cal | M260 rockets (7× Hydra 70) | Light engagement + self-defense | Low-threat reconnaissance; extended endurance; no precision requirement |
| **Full Rockets** | M260 rockets | M260 rockets | Maximum area fires | Area suppression; FASCAM/smoke delivery; no armor threat expected |
| **Air Defense** | AIM-92 Stinger (×2) | 2× AGM-114 | Anti-air + anti-armor | Known enemy air threat; requires giving up gun/rocket capability |

#### Loadout Decision Factors

| Factor | Consideration |
|--------|--------------|
| **Target Set** | Armor → Hellfire K; soft targets → rockets/gun; mixed → General Purpose loadout |
| **Threat Environment** | High AD threat → minimize exposure → favor Hellfire standoff over rockets/gun close-in work |
| **Mission Type** | Scout → Scout/Attack (.50 cal + Hellfire); deliberate attack → Full Hellfire or GP loadout |
| **Air Threat** | Significant air threat → consider Stinger on one pylon (accept reduced ground ordnance) |
| **Performance** | Hot/high conditions → lighter loadout for adequate hover performance; heavy loadout may prevent HOGE |
| **Endurance** | Lighter loadout = less drag = better fuel economy = more time on station |

#### Weight & Performance Planning

| Loadout | Approximate Added Weight | Performance Impact |
|---------|------------------------|-------------------|
| 4× AGM-114 Hellfire | ~400 lbs | Significant — may prevent HOGE in hot/high conditions |
| 2× AGM-114 + M260 rockets | ~300 lbs | Moderate — good performance in most conditions |
| 2× AGM-114 + M3P .50 cal | ~350 lbs | Moderate — .50 cal pod with ammo is heavy |
| 2× M260 rocket pods | ~200 lbs | Light — best performance with ordnance |
| M3P .50 cal + M260 rockets | ~250 lbs | Light-Moderate — good endurance configuration |

**Power Check Requirements:**

Before every weapons mission, compute:
1. **Gross weight** at takeoff (empty weight + fuel + weapons + crew + equipment).
2. **Power available** at mission conditions (pressure altitude + temperature → OAT chart).
3. **Power required** for HOGE at mission weight.
4. **Margin:** If PA < PR for HOGE, you cannot hover-fire from hull-down. Options: reduce fuel, reduce weapons, perform running takeoff, or accept that hull-down engagement is not possible until weight decreases.

> **Instructor Note:** In temperate DCS conditions (sea level, 15°C), the OH-58D can handle most loadouts. In hot/high DCS missions (Middle East maps, summer, 3,000 ft+ elevation), a full Hellfire loadout may exceed HOGE capability. Students MUST check power before committing to a loadout.

---

### 10.3 Engagement Planning

#### Pre-Mission Engagement Plan

| Element | Content |
|---------|---------|
| **Engagement Area (EA)** | Geographic bounds; marked on map/kneeboard |
| **Battle Positions (BP)** | Primary, Alternate, Supplementary — marked with approach/egress routes |
| **Target Reference Points (TRP)** | Pre-designated points within EA for rapid target handoff |
| **Trigger Lines** | Lines within EA that trigger engagement (e.g., "engage when enemy crosses Phase Line RED") |
| **Priority of Engagement** | 1: AD, 2: Armor, 3: C2, 4: Soft targets (or per mission briefing) |
| **Weapons Allocation** | Hellfire for Priority 1–2; rockets/APKWS for Priority 3–4; gun for targets of opportunity |
| **Ammunition Management** | "Bingo" state: Hellfire ≤1 remaining; rockets ≤3 remaining; gun ≤100 rounds → report to lead; consider RTB |
| **Abort Criteria** | When to disengage: Winchester; Bingo fuel; combat damage; weather below minimums; loss of communications |

#### Engagement Sequence Planning

For a typical armor-defense engagement:

| Phase | Action | Timeframe |
|-------|--------|-----------|
| **Pre-Position** | Occupy primary BP via covered route; establish hull-down | T-5 min (before expected enemy arrival) |
| **Observation** | MMS scan of EA; report enemy composition, location, movement | T-0 (enemy enters EA) |
| **Engagement** | Engage per priority: AD first, then armor from front to rear | T+0:30 to T+5:00 |
| **Displacement** | Move to alternate BP after 1–2 engagements from primary | After each engagement pair |
| **Re-engagement** | Continue engagement from alternate/supplementary BPs | Until targets destroyed or Winchester |
| **Withdrawal** | Disengage; covered egress to FARP or rally point | When Winchester, Bingo fuel, or mission complete |

---

### 10.4 Communication Planning

#### Frequency Plan

| Net | Purpose | Who |
|-----|---------|-----|
| **Team Internal** | Kiowa-to-Kiowa / Kiowa-to-Apache coordination; target handoff, tactical calls | Aviation team only |
| **Ground Maneuver** | Coordination with ground commander; CCA requests; fire coordination; BDA reports | Ground element + aviation team lead |
| **Brigade/Battalion Fires** | Artillery coordination; fire support coordination; deconfliction | FSO/FSE + aviation |
| **Air Traffic / FARP** | FARP coordination; airspace deconfliction | ATC / FARP personnel |
| **Guard** | Emergency frequency | All |

#### Laser Code Deconfliction

When multiple designators are active (e.g., two Kiowas + a JTAC), each must use a **unique PRF code** to prevent weapons from homing on the wrong laser.

| Designator | PRF Code | Notes |
|-----------|----------|-------|
| Kiowa 1 | 1688 (default) | Primary designator for EA left sector |
| Kiowa 2 | 1687 | Secondary designator for EA right sector |
| JTAC | 1686 | Ground-based designator for priority targets |
| Apache (if buddy-lasing) | 1685 | Coordinated pre-mission |

**Rule:** Brief PRF codes during mission planning. Verify codes on MFD before every engagement. Never assume the code is set correctly.

#### Brevity Codes

| Code | Meaning |
|------|---------|
| **"Rifle"** | Hellfire launch |
| **"Rockets"** | Rocket fire (unguided or APKWS) |
| **"Guns"** | .50 cal engagement |
| **"Fox Two"** | Stinger (IR A/A missile) launch |
| **"Spot"** | Laser designator is active on target |
| **"Splash"** | Weapon impact on target |
| **"Cease laser"** | Stop laser designation |
| **"Winchester"** | All weapons expended |
| **"Bingo"** | Minimum fuel for return to FARP |
| **"Bingo Ammo"** | Minimum ammunition remaining (reserve only) |
| **"Tally"** | Visual contact with target |
| **"No Joy"** | No visual contact with target |
| **"Contact"** | Target detected (radar/sensor — less common for OH-58D; use "Tally" for MMS visual) |
| **"Engaged"** | Currently engaging a target; do not reassign |
| **"Cleared Hot"** | Authorization to fire on specified target |
| **"Abort"** | Do not fire / cease engagement immediately |
| **"Break"** | Immediate defensive maneuver required; threat |
| **"Remask"** | Return to hull-down / terrain cover |

---

### 10.5 DCS Mission Editor Integration

#### Setting Up Loadouts

| Step | Action |
|------|--------|
| 1 | Open Mission Editor; select OH-58D unit |
| 2 | Click on the loadout/payload tab |
| 3 | Select left pylon weapon (Hellfire, rockets, .50 cal) |
| 4 | Select right pylon weapon (Hellfire, rockets) |
| 5 | Select specific warhead/variant if applicable (Hellfire K/M/N; rocket warhead type) |
| 6 | Verify total weight and check against performance charts |

#### Waypoint and Target Planning

| Element | Mission Editor Action |
|---------|---------------------|
| **Waypoints** | Set ingress route following terrain-masked corridors; add altitude waypoints for NOE flight |
| **Target Points** | Mark known/suspected target locations; use as reference in cockpit |
| **FARP** | Mark the Forward Arming and Refueling Point; plan return route |
| **Battle Positions** | Can be marked as waypoints or reference points for the pilot to navigate to |
| **Engagement Area** | Mark EA boundaries as reference points on the map |

#### Weather Considerations

| Condition | Impact on Weapons Employment |
|-----------|----------------------------|
| **Clear day** | TV sensor optimal; all weapons nominal; visual PID possible |
| **Overcast / low ceiling** | May prevent pop-up attacks (ceiling below apex altitude); diving fire limited by cloud base |
| **Night (clear)** | TIS primary sensor; TV unusable; NVG required for terrain avoidance; all weapons nominal |
| **Night (overcast)** | TIS only; reduced terrain visibility even with NVG; increased CFIT risk |
| **Fog / heavy rain** | TIS degraded; MMS effectiveness significantly reduced; close-range only; consider mission abort |
| **Strong crosswind** | Unguided rockets significantly affected (lateral drift); guided weapons (Hellfire, APKWS) unaffected |
| **Hot temperature** | Power-limited performance; may need lighter loadout; reduced HOGE capability |
| **High altitude** | Reduced engine performance; lighter loadout required; longer landing/takeoff distances |

> **Instructor Note:** Students often ignore weather effects on weapons employment. A hot, high-altitude mission with fog requires a fundamentally different loadout and engagement plan than a clear, sea-level mission. Brief weather impact during mission planning.

---

### 10.6 Common Student Errors — Mission Planning

| Error | Consequence | Correction |
|-------|-------------|------------|
| Loading max weapons without checking performance | Aircraft cannot HOGE; stuck performing running takeoff; cannot use hull-down engagement | Always compute power check before finalizing loadout; reduce weapons if needed for HOGE |
| Not planning alternate BPs | Stuck in one position; enemy locates and suppresses | Always plan at least 2 alternates per primary BP; brief approach/egress routes for each |
| Not deconflicting PRF codes | Multiple lasers on same code; weapons guide to wrong target | Brief unique PRF codes; write them on kneeboard; verify on MFD before engagement |
| Planning routes through threat rings | Aircraft enters SAM engagement zone; shot down on ingress | Map all known threat rings; route around them; accept longer flight time for survivability |
| Not planning ammunition management | Fires all Hellfires at first target group; nothing left for follow-on targets | Brief ammunition allocation: "No more than 2 Hellfire per target group" or similar ROE |
| Ignoring fuel planning | Bingo fuel during engagement; forced to disengage mid-fight | Plan fuel: transit time + station time + reserve + return to FARP; monitor fuel state continuously |
| Not briefing brevity codes | Confusion during engagement; "I'm firing" instead of "Rifle"; ambiguous communication | Brief brevity codes during pre-mission; standardize across the team |
| Selecting wrong loadout for mission | All rockets against armor (ineffective); all Hellfire against soft targets (overkill, ammo waste) | Match loadout to expected target set; when uncertain, use General Purpose loadout for flexibility |
| Not considering weather impact on sensors/weapons | TIS FLIR useless in heavy rain; rockets inaccurate in strong crosswind | Brief weather and its impact on each weapon system; adjust plan or loadout accordingly |

---

## Appendices

### Appendix A — Master Weapons Quick-Reference

| Weapon | Type | Guidance | Range | Warhead | Target Set | Qty (Max) |
|--------|------|----------|-------|---------|------------|----------|
| AGM-114K | Missile | SAL (LOBL/LOAL) | 500–8,000 m | Tandem HEAT | Heavy armor, bunkers | 4 |
| AGM-114M | Missile | SAL (LOBL/LOAL) | 500–8,000 m | Blast-Frag | Soft targets, structures, boats | 4 |
| AGM-114N | Missile | SAL (LOBL/LOAL) | 500–8,000 m | Thermobaric (MAC) | Bunkers, caves, enclosed spaces | 4 |
| APKWS (AGR-20A) | Guided Rocket | SAL (laser) | 1,500–5,000 m | M151 HE (10 lb) | Light vehicles, point targets | 14 |
| Hydra 70 (M151) | Unguided Rocket | None (ballistic) | 1,500–4,000 m | HE (10 lb) | Troops, soft targets | 14 |
| Hydra 70 (M229) | Unguided Rocket | None (ballistic) | 1,500–3,500 m | HE (17 lb) | Structures, material targets | 14 |
| Hydra 70 (M282) | Unguided Rocket | None (ballistic) | 1,500–4,000 m | MPP (shaped charge) | Light armor, bunkers | 14 |
| Hydra 70 (M156) | Unguided Rocket | None (ballistic) | 1,500–3,000 m | WP (marking/incendiary) | Target marking | 14 |
| M3P .50 cal | Gun | None (ballistic) | 800–2,000 m | 12.7mm ball/AP/API/tracer | Troops, trucks, light targets | 500 rds |
| AIM-92 Stinger | Missile | IR homing | 500–4,500 m | HE-frag (3 lb) | Self-defense A/A | 2–4 |

### Appendix B — Standard Attack Profiles Quick-Reference

| Profile | Altitude | Airspeed | Dive | Range | Primary Weapon |
|---------|----------|----------|------|-------|---------------|
| Hull-Down (Hover) | ~50 ft AGL (MMS exposed) | 0 KIAS | N/A | 1,500–8,000 m | Hellfire, APKWS |
| Running Fire | 100–300 ft AGL | 30–80 KIAS | 0° | 1,000–6,000 m | Hellfire, rockets, .50 cal |
| Diving Fire | 800–1,500 ft AGL (entry) | 80–100 KIAS | 10–20° | 1,500–3,000 m | Rockets, APKWS, .50 cal |
| Pop-Up Attack | NOE → 300–800 ft apex | 40–60 KIAS (climb) | Varies | 1,000–3,000 m | Any |
| Hover Fire (Gun/Rocket) | 30–100 ft AGL | 0–20 KIAS | 0° | 400–2,000 m | .50 cal, rockets |

### Appendix C — Threat Engagement Zones Quick-Reference

| Threat | Type | Effective Range | Guidance | Primary CM | Primary Defense |
|--------|------|----------------|----------|-----------|-----------------|
| SA-7 Grail | IR MANPADS | ~4,200 m | IR | Flares | Terrain mask + flares |
| SA-14 Gremlin | IR MANPADS | ~4,500 m | IR (improved) | Flares | Terrain mask + flares |
| SA-16/18 Igla | IR MANPADS | ~5,200 m | IR (IRCCM) | Flares (less effective) | Terrain mask (primary) + flares |
| SA-8 Gecko | Radar SAM | ~12 km | Radar | Chaff | Terrain mask + standoff + chaff |
| SA-11 Buk | Radar SAM | ~35 km | Radar | Chaff | Avoid engagement zone entirely |
| SA-15 Tor | Radar SAM | ~12 km | Radar | Chaff | Terrain mask + avoid; extremely dangerous |
| ZSU-23-4 Shilka | Radar AAA | ~2,500 m | Radar-directed optical | Chaff + jink | Standoff > 3 km + terrain mask |
| ZU-23 | Optical AAA | ~2,000 m | Optical | None (optical aim) | Jink + terrain mask + speed |
| Small Arms | Rifle/MG | ~1,000 m | Optical | None | Speed + altitude + jink |

---

*Research compiled for OH-58D Kiowa Warrior Weapons Employment Training Course development. Primary source: DCS World Polychop OH-58D module documentation and verified in-game behavior. Secondary sources: TM 1-1520-248-10, FM 3-04.126, FM 3-04.140, TC 1-211, ATP 3-04.1, AGM-114 Hellfire technical manuals. For simulation training use only.*
