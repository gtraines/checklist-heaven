# Research Dossier: A-10C / A-10C II Thunderbolt II — Weapons Employment

> **Purpose:** Comprehensive technical reference for building the A-10C Weapons Employment Course.
> Student prerequisite: A-10C BQT (basic flight operations, startup/shutdown, navigation, pattern work, EPs).

**Source Notes:**
- **Primary (Simulation Truth):** DCS World A-10C / A-10C II module documentation and verified in-game behavior.
- **Secondary (Realism Context):** T.O. 1A-10C-34-1-1 (Nonnuclear Weapons Delivery), T.O. 1A-10C-1 (Flight Manual), AFMAN 11-2A-10C Vol. 3, MCM 3-1, AFTTP 3-3.A-10.
- **Conflict Resolution:** DCS procedure is primary instruction. Real-world divergences noted with: ⚠ Realism Divergence.
- **Module Variants:** A-10C II is a superset of A-10C. All procedures apply to both unless marked **(A-10C II Only)**.

---

## Quick-Reference: Complete Weapons Inventory

### Gun / Cannon
| Weapon | Type | Effective Range | Best Suited For | Key Notes |
|---|---|---|---|---|
| **GAU-8/A Avenger** | 30mm 7-barrel Gatling | 4,000–12,000 ft slant | Armor, IFVs, bunkers, soft targets | 1,174 rds; ~19,000 lbf recoil; PAC modes via IFFCC |

### Air-to-Ground Missiles
| Weapon | Guidance | Range | Best Suited For | Key Notes |
|---|---|---|---|---|
| **AGM-65D** | Imaging IR | 4–8 nm | Armor (day/night) | 125 lb shaped-charge; cooldown required |
| **AGM-65G** | Imaging IR | 4–10 nm | Bunkers, bridges, ships | 300 lb penetrating blast-frag |
| **AGM-65H** | CCD / EO-TV | 4–6 nm | High-contrast targets (day) | 125 lb shaped-charge; daylight only |
| **AGM-65K** | CCD / EO-TV | 4–6 nm | Heavy structures (day) | 300 lb penetrating blast-frag |
| **AGM-65L** | Laser | 6–8 nm | Designated targets | Requires laser code match; buddy or self-lase |

### Rockets
| Weapon | Type | Range | Best Suited For | Key Notes |
|---|---|---|---|---|
| **APKWS (M151/M282)** | Laser-guided 2.75" | 1.5–5.0 km | Precision CAS, light armor | **(A-10C II Only)** Semi-active laser homing |
| **Hydra 70 M151** | 2.75" HE | 1–2 nm | Soft targets, suppression | Unguided; area effect |
| **Hydra 70 M156** | 2.75" WP | 1–2 nm | Marking, incendiary | White phosphorus |
| **Hydra 70 M274** | 2.75" Smoke | 1–2 nm | Target marking for FAC | Practice/marking round |
| **Hydra 70 M257** | 2.75" Illumination | Overhead | Night battlefield illum | Parachute flare |

### Guided Bombs
| Weapon | Guidance | Weight | Best Suited For | Key Notes |
|---|---|---|---|---|
| **GBU-12** | Laser (Paveway II) | 500 lb | Precision point targets | Self-lase via TGP or buddy lase |
| **GBU-10** | Laser (Paveway II) | 2,000 lb | Bunkers, heavy structures | Self-lase via TGP |
| **GBU-38** | GPS/INS (JDAM) | 500 lb | All-weather coordinate strikes | ~10 m CEP (GPS) |
| **GBU-31** | GPS/INS (JDAM) | 2,000 lb | Heavy structures, bridges | ~10 m CEP (GPS) |
| **GBU-54** | Laser + GPS (LJDAM) | 500 lb | Moving targets | **(A-10C II Only)** Hybrid guidance |
| **GBU-39** | GPS/INS (SDB) | 250 lb | Standoff, low collateral | **(A-10C II Only)** ~40 nm glide range |

### Cluster Munitions
| Weapon | Type | Best Suited For | Key Notes |
|---|---|---|---|
| **CBU-87** | CEM (BLU-97 bomblets) | Armor, troops, convoys | Unguided; HOF programmable |
| **CBU-97** | SFW (BLU-108 skeets) | Armor formations | IR-seeking autonomous skeets |
| **CBU-103** | WCMD + CEM | Stand-off cluster delivery | Wind-corrected; GPS-aided |
| **CBU-105** | WCMD + SFW | Stand-off anti-armor | Wind-corrected SFW |

### Unguided Bombs
| Weapon | Weight | Variant | Best Suited For | Key Notes |
|---|---|---|---|---|
| **Mk-82** | 500 lb | Low-drag GP | General purpose | Standard slick bomb |
| **Mk-82 AIR** | 500 lb | High-drag (BSU-49/B) | Low-altitude delivery | Ballute retarder |
| **Mk-82 Snakeye** | 500 lb | High-drag (BSU-33/B) | Low-altitude delivery | Retarder fin assembly |
| **Mk-84** | 2,000 lb | Low-drag GP | Heavy targets | Large blast radius |

### Pods, Sensors & Defensive Systems
| System | Type | Capability | Key Notes |
|---|---|---|---|
| **AN/AAQ-28 Litening AT** | Targeting Pod | FLIR / CCD / Laser designator / LST | A-10C standard TGP |
| **AN/AAQ-33 Sniper XR** | Targeting Pod | Extended range FLIR / Laser / HMCS integration | A-10C II TGP |
| **HMCS** | Helmet-Mounted Cueing | Look-and-designate; sensor slew | **(A-10C II Only)** |
| **ALR-69** | RWR | Threat azimuth, type, launch warning | Both variants |
| **ALE-47** | CM Dispenser | Chaff + flare programs | CMSP managed |
| **ALQ-131 / ALQ-184** | ECM Pod | Active radar jamming | Station 6 (centerline) |
| **AIM-9M Sidewinder** | IR AAM | Self-defense air-to-air | 0.5–5 nm; IRCCM |

---

## Module 1: DSMS, IFFCC & HUD Weapons Symbology

### 1.1 Digital Stores Management System (DSMS)

The DSMS is the central weapons management interface on the A-10C. Unlike the FC3 A-10A (where weapons cycle with a single key), the A-10C requires the pilot to interact with a dedicated MFD page to select, configure, and monitor all ordnance.

#### Accessing the DSMS

1. On either MFCD (left or right): press the **DSMS** OSB (Option Select Button) — typically bottom row.
2. The DSMS STATUS page appears showing all loaded stations (1–11), weapon type per station, and quantity remaining.

#### DSMS Page Hierarchy

| Page | Function | Access |
|---|---|---|
| **STATUS** | Overview of all stations — weapon type, quantity, readiness | Default DSMS page |
| **INV** (Inventory) | Detailed per-station inventory — fuze status, arming wire | OSB from STATUS |
| **PROF** (Profile) | Delivery profile selection and parameters per weapon type | OSB from STATUS |
| **UTIL** (Utility) | Jettison options, special functions | OSB from STATUS |

#### Profile Configuration (PROF Page)

Each weapon type has a configurable delivery profile:

| Parameter | Options | Notes |
|---|---|---|
| **Delivery Mode** | CCIP / CCRP / MAN / DTOS | Weapon-dependent availability |
| **Fuze** | NOSE / TAIL / N+T | Selects which fuze activates |
| **Fuze Function** | INST / DLY1 / DLY2 / PRX | Instantaneous, delay (short/long), proximity |
| **Release Qty** | SGL / PRS / RPL | Single, pairs, ripple |
| **Ripple Count** | 2–20 | Number of weapons per ripple (when RPL selected) |
| **Ripple Interval** | 25–500 ft (or ms) | Spacing between release events |
| **Arming Delay (AD)** | 0–99.9 sec | Time delay before fuze arms after release; critical for low-alt |
| **Escape Maneuver** | NONE / CLM / TRN / LTRN | Post-release escape cue on HUD |

**Profile Save:** Profiles can be saved and recalled. Set up profiles on the ground during pre-flight to avoid heads-down time in combat.

#### Station Priority and Selection

- DSMS selects stations based on a **priority queue** — typically outboard-to-inboard, left-right alternating.
- Pilot can manually override by selecting specific stations on the INV page.
- When a weapon type is depleted from one station, DSMS automatically advances to the next station carrying that type.

#### Jettison

| Method | Action | Use |
|---|---|---|
| **Selective Jettison** | DSMS UTIL → select station → JETT | Drop specific stores for drag reduction or emergency |
| **Emergency Jettison** | EMERG JETT button (right of Master Arm panel) | Instantly releases all pylons — combat emergency only |

### 1.2 IFFCC Delivery Modes

The IFFCC (Integrated Flight & Fire Control Computer) computes weapon delivery solutions and drives HUD symbology.

#### CCIP (Continuously Computed Impact Point)

- The IFFCC continuously calculates where the weapon would impact if released **now**.
- A **pipper** (circle with dot) is displayed on the HUD representing the ground impact point.
- Pilot flies to place the pipper on the target, then pickles.
- Best for: visual target acquisition, diving deliveries, gun/rocket strafing.
- The pipper moves dynamically with aircraft attitude, altitude, and airspeed.

| Weapon Type | CCIP Pipper Behavior |
|---|---|
| Bombs | Pipper on bomb fall line; moves with dive angle and speed |
| Gun | Fixed gun cross or PAC-stabilized reticle |
| Rockets | Pipper similar to bombs but faster movement due to rocket ballistics |

#### CCRP (Continuously Computed Release Point)

- The IFFCC computes the point in space where the weapon must be released to hit a designated target (SPI).
- HUD displays: **azimuth steering line** (fly left/right to center it), **range bar** (closing to target), **pull-up cue**, and **release cue**.
- At the computed release point, the system can **auto-release** (if consent is given by holding pickle) or the pilot can manually release.
- Best for: pre-planned targets, level delivery, medium-altitude, GPS/laser weapons.

| CCRP HUD Element | Meaning |
|---|---|
| Azimuth Steering Line | Vertical line — center it to fly correct ground track to SPI |
| Range Bar | Horizontal bar descending — when it reaches the FPM, weapon releases |
| Pull-up Cue | "X" symbol — if it appears, pull up to achieve release parameters |
| Solution Circle | Circle around FPM — indicates valid release solution exists |
| Time-to-Release | Digital countdown (seconds) |

#### Manual Delivery

- No computer assistance — pilot uses fixed HUD references (mil-depression marks) and experience.
- Rarely used in A-10C; primarily a backup if IFFCC fails.

#### DTOS (Dive Toss)

- Loft/toss delivery mode: pilot designates target via TGP or SPI, pulls into a climb, and the IFFCC computes a release point during the climb arc.
- Used for standoff delivery of iron bombs or to increase release altitude against defended targets.
- HUD shows steering cues similar to CCRP but accounting for loft trajectory.

### 1.3 HUD Weapons Symbology

#### Gun HUD Symbology

| Element | Description |
|---|---|
| **Gun Cross** | Fixed cross — represents boresight of GAU-8/A |
| **PAC Reticle** | Stabilized aiming reference in PAC-1 mode — compensates for aircraft motion |
| **Gun Funnel** | Converging lines in PAC-3 (A-A mode) — target fills funnel at correct range |
| **Rounds Remaining** | Digital readout — bottom of HUD |

#### Bomb HUD Symbology (CCIP)

| Element | Description |
|---|---|
| **Bomb Fall Line (BFL)** | Vertical line from FPM downward — weapon trajectory |
| **CCIP Pipper** | Circle on BFL — where bomb impacts now |
| **MIN RNG Caret** | Caret on BFL — minimum safe release altitude; do NOT release below this |
| **Release Cue** | Flashing pipper or tone — valid release solution |

#### Bomb HUD Symbology (CCRP)

| Element | Description |
|---|---|
| **Azimuth Steering Line** | Vertical line — steer to center on FPM |
| **Range Bar** | Descending horizontal bar — represents time/distance to release |
| **Solution Circle** | Circle around FPM — valid solution indication |
| **Auto-Release Point** | Range bar meets FPM — weapon releases (if pickle held) |

#### Maverick HUD Symbology

| Element | Description |
|---|---|
| **Bore-sight Cross** | Where the Maverick seeker is pointing |
| **Seeker Footprint** | Box showing seeker FOV on ground |
| **Lock Diamond** | Diamond indicates seeker is tracking a target |
| **RDY Indication** | MFCD shows "RDY" when missile is ready to fire |

#### JDAM HUD Symbology

| Element | Description |
|---|---|
| **Steering Cue** | Azimuth steering line to fly over release point |
| **Time-to-Release** | Countdown in seconds |
| **Solution Cue** | Indicates weapon has valid GPS solution |
| **In-Zone / Out-of-Zone** | Release zone boundary indication |

### 1.4 Master Arm Panel

Located on the left armament panel (AHCP — Armament HUD Control Panel):

| Switch | Positions | Function |
|---|---|---|
| **MASTER ARM** | SAFE / ARM / TRAIN | SAFE: no release; ARM: weapons hot; TRAIN: symbology active, no release |
| **GUN/PAC** | SAFE / ARM / GUNARM | Arms GAU-8/A; GUNARM = PAC + gun together |
| **LASER ARM** | SAFE / ARM | Arms TGP laser designator; required for LGB guidance & APKWS |
| **EMERG JETT** | Button (guarded) | Emergency jettison of all stores |

#### Pre-Attack Arming Sequence (Standard)

1. **MASTER ARM** → ARM
2. **GUN/PAC** → ARM (if employing gun)
3. **LASER ARM** → ARM (if employing laser-guided weapons)
4. Select weapon on DSMS
5. Confirm delivery mode (CCIP/CCRP)
6. Verify HUD symbology active

> ⚠ **Realism Divergence:** In real life, pilots follow a strict Master Arm discipline — ARM only when entering the target area, SAFE immediately after. DCS does not enforce this but the course will require students to practice the discipline.

---

## Module 2: GAU-8/A Avenger Cannon

### 2.1 System Data

| Parameter | Value |
|---|---|
| Designation | GAU-8/A Avenger |
| Caliber | 30 × 173 mm |
| Type | 7-barrel externally powered Gatling gun |
| Rate of Fire | 3,900 rounds/min (HIGH); LOW not modeled in DCS |
| Ammunition Capacity | 1,174 rounds |
| Combat Mix | PGU-14/B API (armor-piercing incendiary) + PGU-13/B HEI (high-explosive incendiary), 5:1 ratio |
| Muzzle Velocity | ~1,070 m/s (3,510 ft/s) — API round |
| Recoil Force | ~19,000 lbf (modeled in DCS) |
| Gun Depression | -2° below fuselage reference line (boresighted to fly 1 mil low at ~4,000 ft range) |
| Weight (loaded) | ~4,029 lbs (gun + ammo drum + linkless feed) |

#### Effective Engagement Ranges

| Target Type | Effective Range (Slant) | Notes |
|---|---|---|
| Main Battle Tanks (MBT) | 4,000–6,000 ft | Rear/top aspect preferred; DU core defeats light armor |
| IFVs / APCs | 4,000–8,000 ft | Any aspect; lighter armor easier to penetrate |
| Soft Targets (trucks, AA guns, troops) | 6,000–12,000 ft | HEI rounds effective at longer range |
| Buildings / Bunkers | 4,000–6,000 ft | Multiple passes may be required |

#### Ammunition Conservation

| Burst Duration | Rounds Expended (approx.) | Passes Available (1,174 rds) |
|---|---|---|
| 1 second | ~65 rounds | ~18 passes |
| 2 seconds | ~130 rounds | ~9 passes |
| 3 seconds | ~195 rounds | ~6 passes |
| 5 seconds (max recommended) | ~325 rounds | ~3 passes |

**Instructor Note:** Students should plan for 1–2 second bursts. The GAU-8/A is devastating — short, accurate bursts are more effective than sustained fire. Reserve ammunition for multiple targets/passes.

### 2.2 IFFCC Gun Modes (PAC)

The IFFCC provides three gun aiming modes via the PAC (Precision Attitude Control) system:

#### PAC-1: Strafe Mode (Primary)

- **Function:** Stabilized gun cross. The IFFCC compensates for aircraft pitch, roll, and yaw to hold the gun cross steady on a ground point.
- **HUD Symbology:** Fixed gun cross (+) with a small computed pipper that drifts toward the predicted impact point.
- **Activation:** GUN/PAC switch → ARM; weapon select → GUN; IFFCC mode → PAC-1.
- **Use:** Anti-armor strafe, point target engagement. **Highest accuracy mode.**
- **Technique:** Place the stabilized pipper on target. The stabilization fights against small aircraft movements — the pilot holds steady and fires.

#### PAC-2: CCRP for Gun

- **Function:** Computes a continuously updated impact point along the HUD azimuth line, accounting for wind, aircraft state, and ballistics.
- **Use:** Level or shallow-dive gun employment where the pilot cannot visually acquire the pipper on a distant target.
- **Less commonly used than PAC-1 in DCS.**

#### PAC-3: Air-to-Air Gun (Funnel)

- **Function:** Lead-computing funnel (similar to EEGS). Two converging lines form a funnel — when the target fills the funnel at the correct wingspan, the pilot is at the correct lead.
- **Use:** Self-defense air-to-air gun employment. **Not a primary mission** — documented for completeness.
- **Activation:** A-A master mode → gun selected.

### 2.3 DCS Employment Sequence (Gun)

| Step | Action | Notes |
|---|---|---|
| 1 | **MASTER ARM** → ARM | Left AHCP panel |
| 2 | **GUN/PAC** → ARM (or GUNARM) | Same panel; GUNARM enables PAC + gun simultaneously |
| 3 | **DSMS** → verify gun selected | Check "GUN" displayed on HUD or MFCD status |
| 4 | Set **IFFCC mode** to desired PAC mode | PAC-1 for strafe (default and recommended) |
| 5 | Establish attack geometry: dive angle, airspeed, altitude | See profiles below |
| 6 | Place **PAC pipper on target** | Track smoothly — no jerky corrections |
| 7 | **Trigger — SQUEEZE** (1–2 sec burst) | HOTAS trigger or assigned key |
| 8 | Observe impacts; correct aim for next burst if required | |
| 9 | **Pull off** at minimum recovery altitude | Do NOT press below frag altitude |
| 10 | **Egress** — jink away from target area | Defensive maneuver if in threat environment |

### 2.4 Employment Profiles

#### Profile A: Medium-Angle Strafe (Anti-Armor)

| Parameter | Value |
|---|---|
| Entry Altitude | 8,000–10,000 ft AGL |
| Entry Airspeed | 350 KIAS |
| Dive Angle | 20–30° |
| Open Fire Range | ~6,000 ft slant |
| Cease Fire / Recover | 4,000 ft slant / 3,000 ft AGL minimum |
| Burst Duration | 1–2 seconds |
| Passes | Multiple (2–3 typical) |

**Technique:**
1. Roll in from the perch (high-key position offset from target).
2. Establish 20–30° dive; airspeed will build — manage with throttle idle if needed.
3. Place PAC pipper on target; track smoothly for 1–2 seconds before firing.
4. Fire 1–2 second burst.
5. **Recover at 3,000 ft AGL minimum** — initiate 3–4 G pull.
6. Jink left or right during pull-off to avoid predictable flight path.

#### Profile B: Shallow Strafe (Soft Targets / Troops-in-Contact)

| Parameter | Value |
|---|---|
| Entry Altitude | 3,000–5,000 ft AGL |
| Entry Airspeed | 300–350 KIAS |
| Dive Angle | 5–15° |
| Open Fire Range | ~8,000 ft slant |
| Cease Fire / Recover | 3,000 ft slant / 1,500 ft AGL minimum |
| Burst Duration | 1–2 seconds |

**Technique:**
1. Set up for a shallow approach — nearly level or slightly nose-low.
2. Higher closure rate with target — less time on target, longer firing range.
3. Best against area targets: troop concentrations, vehicle convoys, soft-skin targets.
4. Recovery altitude is lower — requires disciplined pull-off.

### 2.5 Recoil Effects in DCS

The DCS flight model accurately simulates GAU-8/A recoil:

| Effect | Magnitude | Mitigation |
|---|---|---|
| Airspeed bleed | ~10–15 KIAS loss per 2-sec burst at 350 KIAS | Anticipate speed loss; do not fire when slow |
| Nose pitch-up tendency | Slight pitch perturbation | Apply forward stick during firing; trim nose-down slightly before run |
| Yaw wander | Minor lateral oscillation during long bursts | Keep bursts short (< 2 sec); rudder correction |
| Altitude loss awareness | Speed loss in dive = reduced pull-out energy | Plan recovery with speed margin; begin recovery EARLY |

> ⚠ **Realism Divergence:** In real life, the GAU-8/A produces visible gun gas that can cause engine compressor stalls in certain conditions (low altitude, straight flight path through the gas cloud). DCS does not model compressor stalls from gun gas ingestion.

### 2.6 Common Student Errors

| Error | Correction |
|---|---|
| Firing too long (> 3 sec bursts) | 1–2 second bursts. More passes, shorter bursts = more effective. |
| Pressing below minimum recovery altitude | Set a **hard floor**: 3,000 ft AGL for medium-angle, 1,500 ft AGL for shallow. Pull off even if not on target. |
| Not tracking before firing | Pipper must be on target and **stable** for at least 1 second before trigger press. Snap shots are inaccurate. |
| Forgetting speed loss from recoil | Brief the speed: "I need 350 at the top; I'll lose 15 per burst; I need 300 minimum at the bottom." |
| Predictable attack geometry | Vary roll-in heading by ±30° between passes. Never fly the same run-in line twice. |
| GUN/PAC switch in SAFE | Gun will not fire. Check "GUN" on HUD. Students miss this under stress. |

---

## Module 3: Unguided Bombs (Iron Bombs)

### 3.1 Available Ordnance

| Weapon | Body | Weight | Drag Config | Primary Use |
|---|---|---|---|---|
| **Mk-82** | General Purpose | 500 lb | Low-drag (slick) | Standard medium-altitude dive bombing |
| **Mk-82 AIR** | GP + BSU-49/B ballute | 500 lb | High-drag (retarded) | Low-altitude / high-speed delivery |
| **Mk-82 Snakeye** | GP + BSU-33/B fins | 500 lb | High-drag (retarded) | Low-altitude delivery; alternate retarder |
| **Mk-84** | General Purpose | 2,000 lb | Low-drag (slick) | Heavy targets: bridges, bunkers, buildings |

#### Fuze Options

| Fuze Setting | Effect | Best Against |
|---|---|---|
| **INST** (Instantaneous) | Detonates on contact | Soft targets, personnel, light vehicles, exposed equipment |
| **DLY1** (Short Delay) | ~10–25 ms delay | Targets requiring penetration before detonation: light structures, revetments |
| **DLY2** (Long Delay) | ~60–200 ms delay | Hardened targets: bunkers, bridge piers, buried C2 |
| **N+T** (Nose + Tail) | Both fuzes active | Maximum detonation reliability; standard for combat |

#### Fuze Position

| Setting | Function |
|---|---|
| **NOSE** | Nose fuze activates; tail fuze safe |
| **TAIL** | Tail fuze activates; nose fuze safe |
| **N+T** | Both fuzes active — if nose fails, tail detonates (and vice versa) |

### 3.2 DSMS Profile Setup for Iron Bombs

| Step | Action | Notes |
|---|---|---|
| 1 | DSMS page → select bomb type (e.g., MK-82) | Confirm station and quantity |
| 2 | **PROF** page → set delivery mode: **CCIP** or **CCRP** | CCIP for visual; CCRP for pre-planned/SPI |
| 3 | Set **Fuze**: NOSE / TAIL / N+T | Standard: N+T |
| 4 | Set **Fuze Function**: INST / DLY1 / DLY2 | Per target type (see table above) |
| 5 | Set **Release Qty**: SGL / PRS / RPL | SGL = 1 bomb; PRS = 2 (one per side); RPL = ripple |
| 6 | If RPL: set **Ripple Count** (2–20) and **Ripple Interval** (ft or ms) | Wider interval = longer bomb stick pattern across target |
| 7 | Set **AD** (Arming Delay) if low-altitude | Ensures bomb arms after safe separation; prevents frag to own aircraft |
| 8 | Verify profile on DSMS — confirm all settings before roll-in | |

#### Arming Delay (AD) Guidance

| Delivery Altitude | Recommended AD | Rationale |
|---|---|---|
| > 5,000 ft AGL | 0 sec (none needed) | Sufficient frag clearance from altitude |
| 2,000–5,000 ft AGL | 2–4 sec | Moderate frag risk |
| < 2,000 ft AGL | 4–8 sec | Critical — frag will reach release altitude without delay |
| Mk-82 AIR / Snakeye | 0 sec (retarder provides separation) | High-drag device creates frag clearance |

### 3.3 Delivery Modes

#### CCIP Dive Bombing (Primary for Visual Targets)

| Parameter | Mk-82 | Mk-82 AIR / Snakeye | Mk-84 |
|---|---|---|---|
| Recommended Dive Angle | 30–45° | 10–20° (low-alt) | 30–45° |
| Entry Altitude | 10,000–15,000 ft AGL | 2,000–5,000 ft AGL | 12,000–15,000 ft AGL |
| Entry Airspeed | 350–400 KIAS | 350–450 KIAS | 350–400 KIAS |
| Release Altitude (min) | 4,000 ft AGL | 500–1,000 ft AGL (w/ retarder) | 5,000 ft AGL |
| Recovery Altitude (min) | 3,000 ft AGL | 500 ft AGL (high-drag) | 4,000 ft AGL |
| Frag Clearance | Safe above min release alt | Retarder provides separation | Safe above min release alt |

**CCIP Dive Bombing Technique:**

1. **Set up the perch:** 10,000–15,000 ft AGL, offset 2–3 nm from target, 350 KIAS.
2. **Roll in:** Roll to ~135° bank toward target, pull nose through horizon, roll wings-level in the dive.
3. **Establish dive angle:** 30–45° nose-low. Airspeed will build — throttle idle.
4. **Track the pipper:** CCIP pipper drifts toward target as dive continues. Place pipper on target.
5. **"Track, track, PICKLE"**: Hold steady tracking for 1–2 seconds, then release.
6. **Pull off:** Immediate 4–5 G pull; minimum 3,000 ft AGL recovery.
7. **Jink:** Vary pull-off direction.

> **MIN RNG Caret:** The HUD displays a caret on the bomb fall line representing minimum safe release altitude. **Do NOT release the weapon below this caret.** If the CCIP pipper has not reached the target when the MIN RNG caret is near the pipper, wave off.

#### CCRP Level / Shallow-Dive Delivery

| Parameter | All Iron Bombs |
|---|---|
| Altitude | 10,000–20,000 ft AGL |
| Airspeed | 300–400 KIAS |
| Dive Angle | 0–20° |
| SPI Required | Yes — set from TGP, TAD, or steerpoint |
| Release | Auto-release (hold pickle through countdown) or manual |

**CCRP Technique:**

1. Set SPI on target (TGP point track, steerpoint, or TAD cursor).
2. DSMS confirms weapon + CCRP mode.
3. Fly the **azimuth steering line** — center it on the FPM.
4. **Range bar** descends as aircraft approaches release point.
5. **Hold pickle** (consent) — weapon auto-releases when range bar meets FPM.
6. Alternatively: release manually when range bar and solution circle align.

#### Low-Altitude Delivery with Mk-82 AIR / Snakeye

| Parameter | Value |
|---|---|
| Altitude | 200–1,000 ft AGL |
| Airspeed | 400–450 KIAS |
| Dive Angle | Level to 10° |
| Arming Delay | 0 sec (retarder provides safe separation) |
| Release | CCIP — pipper placed on target in near-level flight |

**Pop-Up Attack Profile (Low-Altitude to CCIP):**

1. Ingress low: 200–500 ft AGL, 400+ KIAS, terrain masking.
2. At ~3 nm from target: **pop-up** — pull to 20–30° nose-up.
3. At 3,000–5,000 ft AGL: roll inverted, pull nose through to target, roll wings-level in a 30° dive.
4. Acquire target; CCIP pipper on target; pickle.
5. Recover at minimum altitude; egress low.

### 3.4 Fragmentation Patterns & Safe Separation

| Weapon | Lethal Radius (approx.) | Safe Separation (own aircraft) |
|---|---|---|
| Mk-82 (INST) | ~150 ft | > 3,000 ft AGL release altitude |
| Mk-82 (DLY) | ~150 ft | > 2,000 ft (delay allows separation) |
| Mk-84 (INST) | ~400 ft | > 5,000 ft AGL release altitude |
| Mk-84 (DLY) | ~400 ft | > 3,500 ft AGL |

> ⚠ **Realism Divergence:** DCS models bomb blast and fragmentation damage to the player aircraft, but the frag model may be less punishing than real-world tables. Students should still treat minimum release altitudes as absolute — frag damage in DCS can still destroy or critically damage the aircraft.

### 3.5 Common Student Errors

| Error | Correction |
|---|---|
| Releasing below MIN RNG caret | "If the pipper hasn't reached the target and the caret is near, WAVE OFF. There is always another pass." |
| Forgetting fuze settings | Always verify DSMS fuze before roll-in. Wrong fuze = dud or wrong effect. |
| Pressing below recovery altitude | Set a hard floor. Brief it. Honor it. "I will not fly below 3,000 ft." |
| CCIP pipper chasing — jerky tracking | "Track, track, pickle." Smooth, steady corrections only. If the pipper won't settle, wave off. |
| Not setting arming delay for low-alt Mk-82 slick | Frag from own bomb at < 2,000 ft AGL = self-kill. Use AD or switch to Mk-82 AIR. |
| Ripple interval too short | Bombs land too close together — wasted ordnance. 75–125 ft interval for vehicle columns. |
| Forgetting to set CCRP SPI | CCRP without an SPI = no steering cue, no auto-release. Weapon does nothing. |

---

## Module 4: Cluster Munitions

### 4.1 Available Ordnance

#### Unguided Cluster Munitions

| Weapon | Dispenser | Submunition | Quantity | Effect |
|---|---|---|---|---|
| **CBU-87 CEM** | SUU-65/B TMD | BLU-97/B (Combined Effects) | 202 bomblets | Anti-armor (shaped charge), anti-personnel (frag), incendiary |
| **CBU-97 SFW** | SUU-66/B TMD | BLU-108/B (Sensor Fuzed) | 10 submunitions × 4 skeets = 40 IR-seeking skeets | Autonomous anti-armor — skeets scan, detect, fire EFP |

#### Wind-Corrected (WCMD) Cluster Munitions

| Weapon | Base Munition | Guidance | Effect |
|---|---|---|---|
| **CBU-103** | CBU-87 CEM payload | GPS/INS wind correction (WCMD tail kit) | Wind-corrected CEM delivery — improved accuracy from altitude |
| **CBU-105** | CBU-97 SFW payload | GPS/INS wind correction (WCMD tail kit) | Wind-corrected SFW — stand-off anti-armor |

### 4.2 Employment Concepts

#### CBU-87 CEM — How It Works

1. Dispenser released from aircraft.
2. At programmed **HOF (Height of Function)** altitude, dispenser opens.
3. 202 BLU-97/B bomblets scatter in an elliptical **footprint** along the aircraft track.
4. Each bomblet contains: shaped-charge jet (penetrates ~7" steel), fragmentation ring, zirconium incendiary disk.
5. Footprint size depends on: release altitude, airspeed, dive angle, and HOF setting.

| Footprint Parameter | Approximate Value |
|---|---|
| Length | 600–1,200 ft (along track) |
| Width | 300–600 ft (perpendicular to track) |
| Bomblet density | ~1 bomblet per 100–200 sq ft |

#### CBU-97 SFW — How It Works

1. Dispenser released from aircraft.
2. At programmed HOF, dispenser opens and releases 10 BLU-108/B submunitions.
3. Each BLU-108/B deploys a parachute, spins, and releases **4 IR-seeking skeet warheads**.
4. Each skeet scans the ground with an IR sensor. Upon detecting a hot target (vehicle engine), it fires an **Explosively Formed Penetrator (EFP)** downward.
5. 10 submunitions × 4 skeets = **40 independently targeting anti-armor warheads**.

| SFW Parameter | Value |
|---|---|
| Minimum effective HOF | ~1,500 ft AGL (skeets need altitude to scan) |
| Maximum effective HOF | ~3,000 ft AGL |
| Footprint | ~500 × 500 ft (roughly circular) |
| Target type | Hot engines — running vehicles, recently operated equipment |
| Ineffective against | Cold (parked and cooled) vehicles, personnel, structures |

**Instructor Note:** SFW is devastating against active vehicle formations but useless against cold/concealed targets. Brief the target requirement clearly.

### 4.3 WCMD Variants (CBU-103 / CBU-105)

The WCMD (Wind-Corrected Munitions Dispenser) adds a GPS/INS tail kit to the standard CBU canister:

| Feature | Unguided CBU-87/97 | WCMD CBU-103/105 |
|---|---|---|
| Wind correction | None — affected by crosswind | GPS/INS corrects for measured winds |
| Delivery mode | CCIP (best) | CCRP (coordinate-based, like JDAM) |
| Release altitude | Low-medium (for footprint accuracy) | Medium-high (wind correction enables altitude) |
| Stand-off | Minimal | 5–8 nm from medium altitude |
| DSMS setup | Standard bomb profile | Coordinate-based: SPI or steerpoint required |

#### DSMS Setup for WCMD

1. Select CBU-103 or CBU-105 on DSMS.
2. Set delivery mode: **CCRP**.
3. Set target coordinates (SPI from TGP, steerpoint, or manual entry).
4. Set **HOF altitude** — critical for cluster effectiveness.
5. Verify wind data is current (EGI provides wind estimates to WCMD).
6. Fly CCRP steering cue; auto-release.

### 4.4 DSMS Profile Setup (Unguided CBU)

| Step | Action | Notes |
|---|---|---|
| 1 | DSMS → select CBU-87 or CBU-97 | Verify station and quantity |
| 2 | PROF → delivery mode: **CCIP** | For unguided CBUs |
| 3 | Set **HOF** (Height of Function) | CBU-87: 1,000–2,000 ft AGL; CBU-97: 1,500–3,000 ft AGL |
| 4 | Fuze: typically fixed (dispenser opens at HOF) | DSMS may show limited fuze options for CBUs |
| 5 | Release Qty: SGL recommended | One dispenser per pass for footprint management |
| 6 | Verify profile; confirm on HUD | |

### 4.5 Delivery Profiles

#### CBU-87 CEM — CCIP Delivery

| Parameter | Value |
|---|---|
| Entry Altitude | 8,000–15,000 ft AGL |
| Dive Angle | 20–40° |
| Airspeed | 350–400 KIAS |
| Release Altitude | > HOF + 2,000 ft (to ensure dispenser opens at HOF) |
| HOF Setting | 1,000–2,000 ft AGL |
| Recovery Altitude | > 3,000 ft AGL |

**Technique:** Standard CCIP dive delivery — pipper on center of target area. Footprint aligns along aircraft ground track. For linear targets (convoys), fly parallel to the column.

#### CBU-97 SFW — CCIP Delivery

| Parameter | Value |
|---|---|
| Entry Altitude | 10,000–18,000 ft AGL |
| Dive Angle | 20–45° |
| Airspeed | 350–400 KIAS |
| Release Altitude | > HOF + 3,000 ft (minimum: ~5,000 ft AGL if HOF = 2,000) |
| HOF Setting | 1,500–3,000 ft AGL (student should use 2,000 ft default) |
| Recovery Altitude | > 4,000 ft AGL |

**Technique:** Same as CBU-87 but higher release altitude required. Pipper on center of vehicle formation. SFW is area-effect — do not try to "precision aim" at individual vehicles.

#### WCMD (CBU-103/105) — CCRP Delivery

| Parameter | Value |
|---|---|
| Altitude | 15,000–25,000 ft AGL |
| Airspeed | 300–400 KIAS |
| Dive Angle | 0–20° (level preferred) |
| SPI | Required — coordinates of target area center |
| HOF Setting | Same as base munition (1,000–2,000 for CEM; 1,500–3,000 for SFW) |
| Release | Auto-release via CCRP (hold pickle through countdown) |

### 4.6 Target Set Selection Guide

| Target Type | Best Munition | Rationale |
|---|---|---|
| Armor column (moving) | CBU-97 SFW or CBU-105 | IR-seeking skeets acquire running engines |
| Armor column (cold/parked) | CBU-87 CEM | SFW won't detect cold targets; CEM effective regardless |
| Troop concentration | CBU-87 CEM | Fragmentation + incendiary |
| Soft-skin convoy | CBU-87 CEM | Shaped charge + frag overkill but effective |
| Vehicle park (mixed) | CBU-97 SFW | Skeets discriminate vehicles from terrain |
| Airfield denial | CBU-87 CEM | Runway cratering + area denial |
| Stand-off (defended target) | CBU-103 or CBU-105 | WCMD enables high-altitude release outside SAM MEZ |

### 4.7 Common Student Errors

| Error | Correction |
|---|---|
| HOF set too low for SFW | If HOF < 1,500 ft, skeets don't have time to scan. Use 2,000 ft default. |
| Using SFW against cold/concealed targets | SFW requires hot IR signatures. Brief the target state. Use CEM instead. |
| Releasing CBU from too low altitude | Dispenser must open at HOF. If release alt < HOF + separation distance, bomblets never scatter properly. |
| Not aligning track with linear target | Footprint is elliptical along track. Fly **parallel** to convoys, not perpendicular. |
| Confusing WCMD (CCRP) with unguided CBU (CCIP) | WCMD needs SPI and coordinates. Unguided CBU uses visual CCIP pipper. Different DSMS setup entirely. |

---

## Module 5: Unguided Rockets (Hydra 70 Family)

### 5.1 Available Variants

| Rocket | Warhead | Weight (each) | Primary Use |
|---|---|---|---|
| **M151** | HE (High Explosive) | ~13.6 lb | Anti-personnel, light vehicles, soft targets, suppression |
| **M156** | WP (White Phosphorus) | ~14.1 lb | Incendiary, marking (produces thick white smoke) |
| **M274** | Smoke (Practice) | ~13.0 lb | Target marking for FAC/CAS coordination |
| **M257** | Illumination | ~14.5 lb | Battlefield illumination (parachute flare, ~1 million candlepower) |

### 5.2 Launcher Types

| Launcher | Tubes | Stations | Notes |
|---|---|---|---|
| **LAU-68** | 7 | Wing pylons (2, 3, 9, 10) | Standard 7-tube pod; lightweight |
| **LAU-131** | 7 | Wing pylons | Alternate 7-tube pod |
| **LAU-61** | 19 | Wing pylons | High-capacity 19-tube pod; heavier |

**Typical Loadout:** 4 × LAU-68 (28 rockets total) or 4 × LAU-61 (76 rockets total). Mixed loads possible — WP on one station, HE on another.

### 5.3 DSMS Profile Setup

| Step | Action | Notes |
|---|---|---|
| 1 | DSMS → select rocket type (e.g., M151 HE) | System groups by warhead type |
| 2 | PROF → delivery mode: **CCIP** | Rockets are almost always CCIP |
| 3 | Set **Qty per salvo**: 1, 2, 4, 7, 14, etc. | 1 = single rocket; 7 = full pod; 14 = two pods simultaneously |
| 4 | Set **Ripple**: if desired, ripple fires from multiple pods | Not common; single salvo preferred for accuracy |
| 5 | Verify profile; note total inventory remaining | |

#### Salvo Selection Guide

| Salvo Size | Rockets per Press | Best For |
|---|---|---|
| **1** | Single rocket | Marking (WP), precision against point target |
| **2** | Pair | Light suppression, ranging |
| **4** | Small salvo | Moderate area coverage |
| **7** | Full pod | Area suppression, heavy engagement |
| **14+** | Multi-pod | Saturating a large area (rare — conservation issue) |

### 5.4 Employment Profiles

#### Profile A: Standard Rocket Run (Anti-Personnel / Soft Target)

| Parameter | Value |
|---|---|
| Entry Altitude | 5,000–8,000 ft AGL |
| Dive Angle | 10–20° |
| Entry Airspeed | 300–350 KIAS |
| Fire Range | 6,000–10,000 ft slant |
| Cease Fire / Recover | 4,000 ft slant / 2,000 ft AGL minimum |
| Salvo Size | 2–4 per press |

**Technique:**
1. Set up similarly to a shallow strafe run.
2. Place CCIP pipper on target area.
3. Pipper movement is **faster than bombs** — rockets are faster and lighter, so the pipper moves rapidly.
4. Fire when pipper settles on target; **short burst** (1–2 trigger presses).
5. Observe impacts; correct aim if needed.
6. Pull off at minimum altitude.

#### Profile B: WP Marking Run (FAC/CAS)

| Parameter | Value |
|---|---|
| Entry Altitude | 5,000–8,000 ft AGL |
| Dive Angle | 10–20° |
| Airspeed | 300–350 KIAS |
| Salvo Size | **1** (single WP rocket) |
| Purpose | Mark target for follow-on aircraft or JTAC confirmation |

**Communication Flow:**
1. FAC/JTAC: *"Hawg 1-1, mark my target with Willy Pete."*
2. Pilot: *"Hawg 1-1, in hot from the south."*
3. Fire single WP rocket at target area.
4. FAC/JTAC: *"Good mark. Target is 50 meters north of your smoke."*
5. Pilot adjusts aim for next pass with HE or other ordnance.

#### Profile C: Illumination (M257)

| Parameter | Value |
|---|---|
| Delivery | Fire at high angle over target area; flare deploys at apex |
| Altitude | 3,000–5,000 ft AGL |
| Technique | Lob delivery — aim above target; flare parachutes down |
| Duration | ~2 minutes per flare |
| Use | Night CAS — illuminate target area for visual identification |

### 5.5 Rocket Dispersion & Accuracy

| Factor | Effect on Accuracy |
|---|---|
| Range | Dispersion increases linearly with range — closer = tighter grouping |
| Dive angle | Steeper dive = shorter time-of-flight = less dispersion |
| Crosswind | Rockets drift in crosswind (no guidance correction) |
| Aircraft stability | Any yaw/roll at launch degrades accuracy — stabilized flight essential |
| Salvo size | Larger salvo increases probability of hit but wastes rockets on area targets |

| Range (Slant) | Approximate Dispersion (M151 HE) |
|---|---|
| 3,000 ft | ±10–15 ft (very tight) |
| 6,000 ft | ±25–40 ft |
| 10,000 ft | ±50–80 ft |
| 12,000 ft | ±80–120 ft (max practical range) |

### 5.6 DCS Employment Sequence

| Step | Action | Notes |
|---|---|---|
| 1 | **MASTER ARM** → ARM | |
| 2 | DSMS → select rocket type | Confirm correct warhead (HE vs. WP) |
| 3 | Set salvo size on DSMS PROF page | 1 for marking, 2–4 for engagement |
| 4 | Establish attack geometry: 10–20° dive, 300–350 KIAS | |
| 5 | Place **CCIP pipper on target** | Track smoothly — pipper moves fast |
| 6 | **Pickle / fire** (weapon release button) | Short press for each salvo |
| 7 | Observe impacts; adjust | |
| 8 | **Pull off** at minimum altitude | |

### 5.7 Common Student Errors

| Error | Correction |
|---|---|
| Firing too far away (> 10,000 ft) | Rockets lose accuracy rapidly with range. Close to 6,000–8,000 ft for effective engagement. |
| Holding fire too long — emptying pods | Rockets are expendable but finite. 2–4 per pass. Conserve for multiple targets. |
| CCIP pipper chasing | Pipper moves fast with rockets. Anticipate — lead the pipper to the target, don't chase it. |
| Using HE when marking is needed | WP (M156/M274) for marking; HE (M151) for destruction. Wrong warhead = wrong effect. |
| Not switching salvo size for marking | Single rocket for marking. If salvo is set to 7, you'll fire an entire pod for one mark. |
| Ignoring wind correction | Crosswind pushes unguided rockets. Aim upwind slightly on windy days. |

---

## Module 6: TGP (Targeting Pod) Operations

### 6.1 Pod Variants

| Pod | Designation | Aircraft | Key Capabilities |
|---|---|---|---|
| **Litening AT** | AN/AAQ-28 | A-10C | FLIR (640×480), CCD-TV, laser designator/rangefinder, laser spot tracker (LST) |
| **Sniper XR** | AN/AAQ-33 | A-10C II | Enhanced FLIR (1024×1024), extended detection range, HMCS slew integration, improved tracking |

Both pods mount on station 10 (right inboard pylon) in DCS. Functionality is operationally identical for training purposes — the Sniper XR has better image quality and longer detection range.

### 6.2 TGP Power-On & Alignment

| Step | Action | Expected Result |
|---|---|---|
| 1 | **TGP switch** (AHCP panel) → **STBY** | Pod powers up; begins gyro spin-up and thermal calibration |
| 2 | Wait **~90 seconds** | Pod completes alignment; MFCD shows "STBY" then transitions to "OPER READY" |
| 3 | **TGP switch** → **OPER** | Pod enters operational mode; FLIR imagery appears on selected MFCD |
| 4 | Verify MFCD TGP page | Live video feed; OSB functions labeled; cross-hairs centered |

> **Instructor Note:** Power up the TGP during engine start / EGI alignment. By the time taxi is complete, the pod will be aligned and operational. Do not wait until airborne.

### 6.3 MFCD TGP Page Layout

The TGP page displays live sensor video with overlaid symbology:

| Element | Location | Function |
|---|---|---|
| **Cross-hairs** | Center | Where the sensor is looking / where the laser will fire |
| **FOV indicator** | Top-left | WIDE or NARR (field of view) |
| **Sensor mode** | Top-left | FLIR / CCD (TV) / LST |
| **Polarity** | Top-right | WHOT / BHOT (FLIR) or TV (CCD) |
| **Laser status** | Bottom-left | ARM / FIRE / CODE |
| **Coordinates** | Bottom | LAT/LONG/ELEV of cross-hair point on ground |
| **Track mode** | Bottom-center | INR (Inertial) / AREA / POINT |
| **Slant range** | Right side | Distance to cross-hair point |

#### OSB Functions (Key Buttons)

| OSB | Function | Notes |
|---|---|---|
| **FOV** | Toggle Wide / Narrow | Use Wide for search; Narrow for ID and designation |
| **FLIR / TV** | Toggle sensor | FLIR for thermal; TV for daylight visual |
| **WHOT / BHOT** | Toggle FLIR polarity | White-hot vs. black-hot; switch to find contrast |
| **TRK** | Cycle track mode | INR → AREA → POINT |
| **A-G / A-A** | Sensor master mode | A-G for ground targets (primary) |
| **MARK** | Create a markpoint at current cross-hair position | Saves LAT/LONG/ELEV as a CDU steerpoint |
| **SLAVE** | Slave TGP to SPI | Points TGP at current SPI location |

### 6.4 TGP Modes

#### Snowplow Mode

- TGP points straight ahead and below at a fixed depression angle.
- As aircraft flies forward, the sensor view "plows" forward across the ground.
- Use: initial search along a route or heading.
- The cross-hairs are not stabilized on any ground point — they move with the aircraft.

#### Inertial (INR) Mode

- Cross-hairs are stabilized on a ground point using INS position.
- As the aircraft moves, the sensor tracks the INS-computed ground point.
- Drift accumulates — INR is approximate. Use for initial cueing, not precision.
- Activate: slew to a point; release slew; pod enters INR on that position.

#### Area Track (AREA)

- TGP uses scene correlation to track a ground area — a region of terrain texture or features.
- More stable than INR; no drift.
- Use: tracking a fixed point on the ground (building, intersection, parked vehicle).
- **Not effective against moving targets** — the tracker locks to terrain, not the object.

#### Point Track (POINT)

- TGP uses contrast tracking to follow a **specific object** (vehicle, person, hot source).
- Most precise mode; follows moving targets.
- Requires adequate contrast between target and background.
- **This is the mode used for laser designation** — the laser fires at the cross-hair point, which is on the tracked object.
- If contrast is lost (target enters shadow, obscured by dust), tracker may break lock. Re-acquire manually.

### 6.5 Sensor Controls (HOTAS)

The TGP is primarily controlled via HOTAS. The key bindings use the **China Hat**, **TMS (Target Management Switch)**, and **DMS (Display Management Switch)** on the throttle and stick:

| HOTAS Control | Short Press | Long Press | Function |
|---|---|---|---|
| **China Hat FWD** | Slave TGP to SPI | — | Points pod at current SPI |
| **China Hat AFT** | Toggle TGP SOI (Sensor of Interest) | — | Makes TGP the active sensor for slewing |
| **TMS UP** | Set SPI from TGP / laser fire (range) | **Laser designate** (continuous lase) | Short = range/SPI; Long = laser ON |
| **TMS DOWN** | — | — | Context-dependent |
| **TMS LEFT** | Abort track / return to previous mode | — | Cancels current track |
| **TMS RIGHT** | — | — | Context-dependent |
| **DMS UP/DOWN/LEFT/RIGHT** | Slew TGP cross-hairs | — | Fine control of sensor aim point |
| **Slew (throttle)** | Slew TGP when SOI | — | Coarse slew; release snaps to INR on that point |

> **SOI (Sensor of Interest):** Only the sensor currently designated as SOI responds to slew commands. Press China Hat AFT to toggle SOI between TGP and other sensors (Maverick, TAD, etc.). A green border on the MFCD indicates the SOI page.

### 6.6 Laser Operations

#### Pre-Requisites for Lasing

| Requirement | How to Set |
|---|---|
| **LASER ARM** switch → ARM | AHCP panel; required before any laser operation |
| **Laser code set** | CDU → LSR page → enter 4-digit PRF code (default: **1688**) |
| **TGP in POINT track** | Target must be tracked — laser fires at tracked point |
| **Master Arm → ARM** | Required if lasing for weapon guidance (LGB, APKWS) |

#### Lasing Procedure

| Step | Action | Result |
|---|---|---|
| 1 | Acquire target on TGP (slew + search) | Cross-hairs on target |
| 2 | Enter **POINT track** (TMS UP short when on target) | Pod tracks the object — cross-hairs follow it |
| 3 | Verify POINT track stable — cross-hairs on target, not drifting | |
| 4 | **TMS UP long press** | Laser fires continuously; "LASE" or "LSR FIRE" appears on MFCD |
| 5 | Laser designation active — other systems (LGB, APKWS) can guide to this point | |
| 6 | Release TMS UP to stop lasing | Laser stops; pod remains in POINT track |

#### Laser Code

- 4-digit code (1111–1788 range, specific valid codes based on PRF table).
- Default: **1688** — standard NATO training code.
- Must match the seeker code on the weapon (LGB kit, APKWS guidance section).
- For buddy lasing: match the code set by the JTAC or FAC-A.
- Set via CDU → LSR page → enter code → ENTER.

#### Laser Timing for LGBs

| Phase | Laser Status | Notes |
|---|---|---|
| Pre-release | OFF (ranging only if needed) | Conserve laser life; don't alert target |
| At release | May be ON or OFF (weapon-dependent) | CCRP auto-release does not require laser at release |
| Terminal phase (~10–15 sec before impact) | **MUST be ON** | LGB seeker needs laser energy on target for final guidance |
| Post-impact | OFF | Turn off laser; assess damage |

> ⚠ **Realism Divergence:** In real life, there are laser safety considerations (eye hazards, COMSEC of laser codes). DCS does not model laser safety — the laser fires instantly with no warm-up or safety protocol. Students should still practice proper laser discipline (laser ON only when needed).

#### Laser Timing for APKWS

- APKWS acquires laser energy **in flight** — the rocket is launched ballistically and then homes on the laser spot.
- Laser must be ON **before the rocket arrives** in the laser acquisition basket.
- Practical timing: start lasing ~2–3 seconds after firing the rocket.
- If laser is late, the rocket may fly ballistically past the target.

### 6.7 SPI (Sensor Point of Interest)

The SPI is the **master designation reference** — a single ground point shared across all systems:

#### SPI Sources (in priority order)

| Source | How to Set | Accuracy |
|---|---|---|
| **TGP** (POINT track) | TMS UP short while TGP is tracking | Highest — laser-ranging provides precise coordinates |
| **HUD** (CCIP) | TMS UP short in CCIP mode | Good — computed from aircraft state and terrain |
| **TAD cursor** | Move cursor to target on TAD; TMS UP | Moderate — limited by map accuracy and altitude |
| **CDU steerpoint** | Select steerpoint on CDU; TMS UP | Variable — depends on coordinate source quality |
| **HMCS** (A-10C II) | Look at target; TMS UP | Good for cueing; less precise than TGP for delivery |

#### SPI Handoff Between Systems

The beauty of SPI is that setting it from any source **updates all other systems**:

- Set SPI from TGP → JDAM receives coordinates; TAD shows SPI diamond; HUD shows SPI mark.
- Set SPI from TAD → TGP slaves to that point (China Hat FWD).
- Set SPI from steerpoint → all systems align to that waypoint.

**Workflow for TGP → JDAM delivery:**
1. TGP acquires target → POINT track.
2. TMS UP short → SPI set to TGP coordinates.
3. DSMS has JDAM selected in CCRP mode.
4. JDAM automatically receives SPI coordinates as target.
5. Fly CCRP steering cue → auto-release.

**Workflow for TGP → LGB delivery:**
1. TGP acquires target → POINT track.
2. TMS UP short → SPI set.
3. DSMS has GBU-12 selected in CCRP mode.
4. Fly CCRP steering cue → auto-release.
5. After release: TMS UP long → laser ON → guide bomb to impact.

### 6.8 Target Identification & CAS Coordination

#### Target Search Pattern

1. Start in **WIDE FOV** — scan the area of interest.
2. Identify potential targets by thermal signature (FLIR) or visual contrast (CCD).
3. Switch to **NARROW FOV** for identification — zoom in on suspicious objects.
4. Confirm target: vehicle type, orientation, movement, friendly/enemy.
5. Enter **POINT track** on confirmed target.
6. Set SPI and proceed to weapons delivery.

#### 9-Line CAS Integration

| 9-Line Element | TGP Role |
|---|---|
| Line 4 — Target Elevation | TGP provides accurate laser-ranged elevation |
| Line 6 — Target Description | TGP provides positive identification (PID) |
| Line 8 — Final Attack Heading | Pilot plans attack to keep TGP LOS clear |
| "Cleared Hot" | Pilot verifies TGP is tracking the correct target before releasing |

**Golden Rule:** Never release a weapon without positive identification (PID) of the target on the TGP. "If I can't see it, I don't drop on it."

### 6.9 Common Student Errors

| Error | Correction |
|---|---|
| Not warming up TGP during ground ops | Power up in STBY during engine start. 90 seconds to warm up. |
| Using AREA track on moving targets | AREA locks to terrain. Target drives away. Use POINT track for movers. |
| Forgetting to arm laser | LASER ARM switch (AHCP panel) must be ARM before lasing. No laser = LGB is a dumb bomb. |
| Laser code mismatch | Verify CDU LSR page code matches weapon code. Mismatch = no guidance. |
| Slewing wrong sensor (SOI not on TGP) | Check for green border on TGP MFCD page. China Hat AFT toggles SOI. |
| Lasing too early — laser discipline | Laser ON only when needed (terminal phase for LGBs, ~2 sec after launch for APKWS). |
| Not setting SPI before CCRP delivery | No SPI = no CCRP steering cue. Set SPI first, then select weapon. |
| TGP masked by aircraft structure in turn | Bank angle can mask the TGP (mounted under right wing). Maintain LOS. |

---

## Module 7: AGM-65 Maverick Family (Precision Guided Missiles)

### 7.1 Variant Data

| Variant | Seeker | Warhead | Weight | Range | Day/Night |
|---|---|---|---|---|---|
| **AGM-65D** | Imaging IR (IIR) | 125 lb shaped charge | 485 lb | 4–8 nm | Day and Night |
| **AGM-65G** | Imaging IR (IIR) | 300 lb penetrating blast-frag | 672 lb | 4–10 nm | Day and Night |
| **AGM-65H** | CCD / EO-TV | 125 lb shaped charge | 462 lb | 4–6 nm | Day Only |
| **AGM-65K** | CCD / EO-TV | 300 lb penetrating blast-frag | 648 lb | 4–6 nm | Day Only |
| **AGM-65L** | Laser (SAL) | 300 lb penetrating blast-frag | ~672 lb | 6–8 nm | Day and Night |

#### Warhead Selection Guide

| Warhead | Best Against | Notes |
|---|---|---|
| **125 lb shaped charge** (D, H) | Individual armored vehicles (MBTs, IFVs) | Penetrates armor; limited blast radius |
| **300 lb penetrating blast-frag** (G, K, L) | Bunkers, bridges, C2 facilities, ships | Penetrates concrete/earth then detonates; large blast |

#### Seeker Selection Guide

| Condition | Best Variant | Rationale |
|---|---|---|
| Night / low-visibility | D or G (IR) | IR imaging works in darkness; sees thermal contrast |
| Day / clear weather | H or K (EO-TV) | High-resolution CCD provides excellent visual ID |
| External designation available | L (Laser) | Lock-on to laser energy; no seeker slewing required |
| Mixed conditions / flexible | D (IR light) or G (IR heavy) | IR works in all lighting; most versatile |

### 7.2 DSMS Maverick Setup

| Step | Action | Notes |
|---|---|---|
| 1 | **DSMS** → select AGM-65 variant | Confirm station(s) loaded |
| 2 | DSMS shows Maverick status per station | Stations cycle outboard-to-inboard |
| 3 | **MFCD** automatically displays Maverick video page | Shows seeker FOV as live video |
| 4 | **Pre-launch cooldown** (IR variants D/G only) | Takes ~3–5 minutes; plan ahead — power on during transit |
| 5 | Confirm **"RDY"** status on MFCD | Missile is powered, cooled (if IR), and ready to fire |

#### IR Cooldown (D/G Variants)

- IR seekers contain a cryogenic cooling element that must reach operating temperature.
- In DCS: select the missile on DSMS → cooldown begins automatically.
- Timer: approximately **3–5 minutes** after selection.
- **Plan ahead:** Select Mavericks during ingress, not when approaching the target.
- EO-TV variants (H/K) have **no cooldown requirement** — ready instantly.

### 7.3 Seeker Operations

#### IR Seeker (D/G)

| Control | Function |
|---|---|
| **Polarity** (OSB on Maverick MFCD page) | Toggle WHOT / BHOT — white-hot vs. black-hot |
| **FOV** (OSB) | Toggle WIDE / NARROW — wide for search, narrow for lock |
| **Gain / Contrast** | Adjust via MFCD OSBs for best image |
| **Slew** | DMS (when Maverick is SOI) — moves seeker cross-hairs |

**IR Target Identification:**
- Hot targets (running engines, recently fired weapons) appear as bright spots in WHOT.
- Switch polarity if target is hard to distinguish — sometimes BHOT provides better contrast.
- Narrow FOV zooms in for positive ID before lock.

#### EO-TV Seeker (H/K)

| Control | Function |
|---|---|
| **FOV** (OSB) | Toggle WIDE / NARROW |
| **Gain / Contrast** | Adjust for best video image |
| **Slew** | DMS (when Maverick is SOI) |

**EO-TV Limitations:**
- Daylight only — completely non-functional at night.
- Requires visual contrast between target and background.
- Shadows, smoke, and haze degrade performance.
- Best against: dark vehicles on light terrain, structures, vehicles on roads.

#### Laser Seeker (L)

| Control | Function |
|---|---|
| **Laser code** | Must match designating laser (TGP, JTAC, FAC-A) |
| **Lock-on** | Seeker acquires laser energy; pilot confirms "RDY" on MFCD |
| **No slewing** | Laser Maverick homes to laser spot — no manual slew required |

### 7.4 Maverick Lock-On Procedure

#### Standard Lock-On (IR/EO-TV: D, G, H, K)

| Step | Action | Notes |
|---|---|---|
| 1 | Maverick powered; "RDY" on MFCD | Cooldown complete (IR) |
| 2 | **China Hat AFT** → make Maverick MFCD the **SOI** | Green border on Maverick page |
| 3 | Slew cross-hairs onto target using **DMS** | Coarse slew; switch to NARROW FOV for precision |
| 4 | **TMS UP** (short press) → **LOCK** | Seeker tracking gate appears around target; seeker follows |
| 5 | Verify stable track — gate remains on target | If gate drifts, break lock (TMS LEFT) and re-acquire |
| 6 | MFCD shows "TRK" or lock indication | Missile is tracking; ready to fire |
| 7 | **Pickle** (weapon release button) → missile launches | |
| 8 | Observe missile flight; begin re-acquisition for next missile | |

#### SPI Handoff to Maverick (Fast Method)

This is the preferred technique when the TGP has already identified and designated a target:

| Step | Action |
|---|---|
| 1 | TGP is tracking target (POINT track); SPI is set from TGP |
| 2 | Select Maverick on DSMS; Maverick MFCD page appears |
| 3 | **China Hat FWD** → slave Maverick seeker to SPI |
| 4 | Maverick seeker slews to SPI location — target should appear in seeker FOV |
| 5 | Switch to NARROW FOV; confirm target in center |
| 6 | **TMS UP** → lock |
| 7 | **Pickle** → fire |

> **This technique dramatically speeds up the targeting cycle.** Without SPI handoff, the pilot must manually slew the Maverick seeker across the ground to find the target — slow and error-prone.

#### Force Correlate (G/K Variants)

- The AGM-65G and AGM-65K support **Force Correlate** — a mode where the seeker locks onto the strongest contrast source within its FOV.
- Useful for large, high-contrast targets (ships, large buildings, fuel storage).
- Not reliable for small targets in cluttered environments.
- Activate: OSB on Maverick MFCD page; or it may auto-engage based on DSMS mode setting.

### 7.5 Employment Profiles

#### Profile A: Medium-Altitude Standoff (Standard)

| Parameter | Value |
|---|---|
| Entry Altitude | 12,000–18,000 ft AGL |
| Airspeed | 300–350 KIAS |
| Dive Angle | 0–15° (nearly level preferred) |
| Launch Range | 6–10 nm (IR); 4–6 nm (EO-TV) |
| Minimum Launch Altitude | 3,000 ft AGL |
| Post-Launch | Jink / break to defeat ground threats |

**Technique:**
1. Transit at 15,000 ft AGL; TGP tracking target; SPI set.
2. Select Maverick; slave to SPI (China Hat FWD).
3. Lock target (TMS UP); verify track.
4. At 6–8 nm: pickle. Missile fires and guides autonomously.
5. Break off; re-acquire next target on TGP; cycle next Maverick; repeat.

#### Profile B: Low-Altitude Pop-Up (Threat Environment)

| Parameter | Value |
|---|---|
| Ingress Altitude | 200–500 ft AGL (terrain masked) |
| Pop-Up | 3–5 nm from target; pull to 15–20° nose-up |
| Apex | ~5,000–8,000 ft AGL |
| Lock & Launch | During apex/descent; 3–5 nm slant range |
| Egress | Dive back to low altitude; terrain mask |

**Technique:**
1. Ingress low; Maverick ready and cooled (selected during ingress).
2. Pop up; acquire target quickly (SPI handoff preferred).
3. Lock; pickle immediately.
4. Push back down to low altitude.
5. Missile guides independently — no pilot input needed after launch.

### 7.6 Ripple Maverick Employment

For multi-target engagements:

1. Fire missile #1 at target A.
2. DSMS automatically advances to next Maverick on the next station.
3. New seeker video appears on MFCD.
4. Slew to target B (or use SPI handoff to new target).
5. Lock; pickle.
6. Repeat until out of missiles or out of targets.

**Time per cycle:** Experienced pilots can achieve **30–45 seconds per missile** in a continuous engagement.

### 7.7 Common Student Errors

| Error | Correction |
|---|---|
| Maverick not cooled (IR variant) | Select Maverick during ingress, not over the target. 3–5 min cooldown. |
| Locking on terrain instead of target | Use NARROW FOV; ensure cross-hairs are ON the vehicle, not beside it. |
| Not using SPI handoff | "Always use the TGP first. Find target with TGP → set SPI → slave Maverick." Manual slew is slower and less reliable. |
| Firing outside launch envelope | Max range depends on altitude and speed. At low altitude, range is reduced. Check "IN ZONE" on HUD. |
| Forgetting Master Arm | Pickle with Master Arm SAFE = nothing happens. Verify ARM before every run. |
| Using EO-TV variant at night | AGM-65H/K are daylight only. At night, only IR (D/G) or Laser (L) work. |
| Maverick launched at wingman / friendly | Positive identification (PID) is mandatory. "If I can't ID it on TGP and Maverick seeker, I don't shoot." |

> ⚠ **Realism Divergence:** In real life, Maverick coolant is consumable — each missile has a finite cooldown time before the cryogenic element is depleted. In DCS, the cooldown model is simplified and the missile remains cooled indefinitely once powered. Students should still practice timely selection to build good habits.

---

## Module 8: Laser-Guided Bombs (Paveway II)

### 8.1 Available Ordnance

| Weapon | Body | Guidance Kit | Total Weight | CEP (with laser) | Warhead |
|---|---|---|---|---|---|
| **GBU-12** | Mk-82 (500 lb) | Paveway II laser kit | ~610 lb | ~3 ft (< 1 m) | 192 lb Comp B GP |
| **GBU-10** | Mk-84 (2,000 lb) | Paveway II laser kit | ~2,084 lb | ~3 ft (< 1 m) | 945 lb Tritonal GP |

#### How LGBs Work

1. Bomb is released from aircraft (ballistically — it falls like a dumb bomb initially).
2. After release, the **laser seeker** in the bomb's nose detects reflected laser energy bouncing off the target.
3. Guidance fins steer the bomb toward the laser "spot" (highest laser energy concentration on the ground).
4. Bomb follows the reflected laser energy to impact.
5. **No laser = no guidance** — the bomb becomes a dumb bomb and impacts wherever gravity takes it.

#### Critical Concept: The "Laser Basket"

- The LGB seeker has a limited field of view (~±15° from its centerline).
- The bomb must be released close enough to the correct trajectory that the seeker can "see" the laser spot.
- If the bomb is released too far off-angle (e.g., massive crosswind, wrong heading), the seeker may never acquire the laser.
- **CCRP delivery ensures the bomb is in the basket** — the IFFCC computes the release point to put the bomb on the correct trajectory.

### 8.2 Self-Lasing with TGP (Primary Method)

The A-10C's TGP (Litening AT or Sniper XR) gives the aircraft **self-designation capability** — a major improvement over the A-10A, which could only receive external laser energy via the Pave Penny.

#### Self-Lase Workflow (Step-by-Step)

| Step | Action | System | Notes |
|---|---|---|---|
| 1 | **TGP** → acquire target | TGP MFCD | Search in WIDE FOV; zoom NARROW for ID |
| 2 | **POINT track** target | TGP | TMS UP short; cross-hairs lock to target |
| 3 | **TMS UP short** → set SPI from TGP | SPI system | All systems receive target coordinates |
| 4 | Verify **laser code** matches weapon | CDU → LSR page | Default 1688; must match GBU seeker code |
| 5 | **LASER ARM** → ARM | AHCP panel | Required before lasing |
| 6 | **DSMS** → select GBU-12 or GBU-10 | DSMS MFCD | Confirm correct weapon and station |
| 7 | Set delivery mode: **CCRP** | DSMS PROF page | CCRP is primary for LGBs |
| 8 | Set fuze: typically **NOSE / INST** | DSMS PROF | NOSE/DLY for hardened targets |
| 9 | **Fly CCRP steering cue** | HUD | Center azimuth steering line; watch range bar |
| 10 | **Hold pickle** (consent for auto-release) | Stick | IFFCC releases bomb at computed point |
| 11 | After release: **TMS UP long** → laser ON | TGP | Must lase for final 10–15 seconds of bomb flight |
| 12 | Maintain TGP LOS on target (no aggressive maneuvering) | Aircraft | Pod must see the target to lase it |
| 13 | **IMPACT** — observe on TGP | TGP | Release TMS UP; laser OFF |
| 14 | Assess damage; re-attack if necessary | | |

#### Laser Timing — When to Start Lasing

| Release Altitude | Bomb Time-of-Flight (approx.) | Laser ON Time |
|---|---|---|
| 12,000 ft AGL | ~20 seconds | Last 10–15 sec before impact |
| 18,000 ft AGL | ~30 seconds | Last 10–15 sec before impact |
| 8,000 ft AGL | ~12 seconds | Lase from release (short TOF) |

**Rule of Thumb:** If TOF is > 15 seconds, you can delay the laser. If TOF is < 15 seconds, lase from release.

> **Instructor Note:** Students should always lase from release on their first several deliveries. The "delayed lasing" technique is an advanced optimization for the check ride.

### 8.3 Buddy Lasing (External Designation)

When a JTAC (ground-based), FAC-A (airborne forward air controller), or wingman provides laser designation:

#### Buddy Lase Workflow

| Step | Action | Notes |
|---|---|---|
| 1 | Coordinate laser code with designator | Radio: "Hawg 1-1, confirm laser code 1688" |
| 2 | Set matching code on CDU → LSR page | Must match exactly |
| 3 | Select GBU on DSMS; CCRP mode | Standard setup |
| 4 | Set SPI to target coordinates (provided by JTAC or TGP) | If no TGP coordinates, use JTAC coordinates in CDU steerpoint |
| 5 | Fly CCRP steering cue | Standard |
| 6 | At appropriate time: radio **"Hawg 1-1, request laser"** | 15–20 sec before computed release |
| 7 | JTAC/FAC-A responds: **"Laser on, code 1688"** | Laser is illuminating the target |
| 8 | **Hold pickle** → weapon releases at CCRP point | |
| 9 | Bomb guides to reflected laser energy | |
| 10 | **"Splash"** — impact confirmed | |
| 11 | JTAC/FAC-A: **"Laser off. Good hit."** | |

#### LST (Laser Spot Tracker) Mode

- The TGP can detect external laser energy in **LST mode**.
- When active, the TGP scans for laser PRF codes and displays a diamond on the MFCD where external laser energy is detected.
- This allows the A-10C pilot to **see** where the JTAC is pointing before releasing.
- LST mode: TGP MFCD OSB → LST; enter expected laser code; scan area.

#### Communication Flow (Standard)

| Speaker | Call | Meaning |
|---|---|---|
| Pilot | *"JTAC, Hawg 1-1, IP inbound, 30 seconds, request laser"* | About to release; needs laser |
| JTAC | *"Hawg 1-1, laser on, code 1688"* | Laser is active on target |
| Pilot | *"Hawg 1-1, laser captured" / "Spot"* | TGP LST detects the laser |
| Pilot | *"Hawg 1-1, rifle"* | Bomb/missile released |
| JTAC | *"Hawg 1-1, splash"* or Pilot observes impact | Impact confirmed |
| JTAC | *"Laser off. Good hit / re-attack"* | BDA |

### 8.4 Delivery Profiles

#### Profile A: Medium-Altitude CCRP (Primary — Self-Lase)

| Parameter | GBU-12 | GBU-10 |
|---|---|---|
| Entry Altitude | 12,000–18,000 ft AGL | 15,000–20,000 ft AGL |
| Airspeed | 300–350 KIAS | 300–350 KIAS |
| Dive Angle | 0–10° (level preferred) | 0–10° (level preferred) |
| Release Mode | CCRP auto-release | CCRP auto-release |
| Fuze | NOSE / INST (soft) or NOSE / DLY (hardened) | NOSE / INST or DLY |
| Recovery | Maintain straight flight for TGP LOS until impact | Same; longer TOF |

**Why level CCRP?** Level delivery maximizes standoff from ground threats, provides stable TGP tracking, and gives the pilot time to manage laser timing. Diving delivery exposes the aircraft to AAA/SAMs for longer and reduces time to manage sensors.

#### Profile B: Dive CCIP (Alternate — Self-Lase)

| Parameter | GBU-12 |
|---|---|
| Entry Altitude | 12,000–15,000 ft AGL |
| Dive Angle | 20–30° |
| Airspeed | 350–400 KIAS |
| Release Altitude | > 8,000 ft AGL |
| Laser | ON from release (short TOF in dive) |
| Recovery | 4 G pull; minimum 5,000 ft AGL |

**Trade-off:** Dive CCIP is more intuitive (pipper on target, pickle) but requires lasing throughout the dive — TGP must track through the pull-off. More skill-intensive.

### 8.5 Environmental Limitations

| Factor | Effect | Mitigation |
|---|---|---|
| **Cloud** | Laser blocked by any cloud between pod and target | Must have clear LOS from aircraft to target; plan around cloud layers |
| **Smoke / dust** | Attenuates laser; scattered return confuses seeker | Avoid lasing through smoke. Wait for smoke to clear or adjust aimpoint |
| **Humidity / fog** | Reduces laser range; may degrade tracking | Lower altitude delivery to reduce atmospheric path |
| **Target reflectivity** | Very dark or very shiny surfaces reflect laser differently | Adjust aimpoint to nearby contrasting surface if available |

### 8.6 Common Student Errors

| Error | Correction |
|---|---|
| Forgetting to arm laser | "Laser ARM → ARM. No laser, no guidance. It's a 500 lb dumb bomb." |
| Laser code mismatch | Verify CDU LSR page before every delivery. Brief the code. |
| Maneuvering aggressively after release | TGP must maintain LOS. No aggressive bank or turn until impact. |
| Laser ON too late (bomb misses) | Bomb needs laser for final ~10–15 sec. If in doubt, lase from release. |
| Using CCIP for LGB (not recommended for beginners) | CCRP auto-release places bomb in the laser basket. CCIP requires precise dive angle and pilot must manage laser while diving. Start with CCRP. |
| Not using TGP POINT track before lasing | Laser without POINT track hits whatever is under the cross-hairs — which may drift. POINT track locks to the target. |
| Releasing below cloud layer with laser above clouds | Laser can't penetrate clouds. Bomb goes dumb. Check LOS. |

> ⚠ **Realism Divergence:** In real life, Paveway II bombs have a "time-out" — if the seeker doesn't detect laser energy within a certain time after release, it enters a ballistic trajectory and cannot re-acquire. DCS models this approximately but may be more forgiving. Students should always plan laser timing conservatively.

---

## Module 9: GPS-Guided Weapons (JDAM)

### 9.1 Available Ordnance

| Weapon | Body | Guidance | Total Weight | CEP (GPS) | CEP (INS Only) |
|---|---|---|---|---|---|
| **GBU-38** | Mk-82 (500 lb) | GPS/INS tail kit | ~560 lb | ~10 m (~33 ft) | ~30 m (~100 ft) |
| **GBU-31** | Mk-84 (2,000 lb) | GPS/INS tail kit | ~2,036 lb | ~10 m (~33 ft) | ~30 m (~100 ft) |
| **GBU-31(V)3/B** | BLU-109 penetrator | GPS/INS tail kit | ~2,170 lb | ~10 m (~33 ft) | ~30 m (~100 ft) |

#### How JDAM Works

1. Before release, the weapon receives **target coordinates** (LAT/LONG/ELEV) from the aircraft's avionics.
2. At release, the JDAM's onboard GPS receiver and INS begin tracking its own position.
3. The weapon flies a computed trajectory, continuously correcting to reach the programmed coordinates.
4. **No pilot input after release** — fire-and-forget.
5. **No laser required** — all-weather, day/night capable.
6. **No line-of-sight required** — weapon guides through clouds, smoke, dust.

#### JDAM vs. LGB — When to Use Each

| Factor | JDAM (GBU-38/31) | LGB (GBU-12/10) |
|---|---|---|
| Weather | All-weather (GPS — no LOS needed) | Clear weather only (laser blocked by clouds) |
| Accuracy | ~10 m CEP | ~1–3 m CEP (much more accurate) |
| Moving targets | Not effective (flies to fixed coordinates) | Can track moving target if laser follows it |
| Pilot workload | Low (set coordinates, auto-release, forget) | Higher (manage TGP, lasing, LOS) |
| Multi-target | Easy — program multiple coordinates | One target per laser designator at a time |
| Cost/weight | Heavier (tail kit + GPS receiver) | Lighter guidance kit |

**Decision rule:** Use JDAM when weather is bad, target doesn't move, or pilot workload is high. Use LGB when precision is critical, target may move, or conditions permit.

### 9.2 JDAM Targeting Modes

#### TOO (Target of Opportunity)

- Coordinates updated **in real time** from the current SPI.
- As the TGP moves (or the pilot re-designates), the JDAM's target coordinates update.
- Weapon receives final coordinates at the moment of release.
- **Best for:** Dynamic targeting — pilot finds target during mission, designates, and drops.

| TOO Workflow |
|---|
| 1. TGP acquires target → POINT track |
| 2. TMS UP → SPI set from TGP (coordinates flow to JDAM) |
| 3. JDAM target coordinates update in real time on DSMS page |
| 4. Fly CCRP steering cue → hold pickle → auto-release |
| 5. JDAM guides to last received coordinates |

#### PP (Pre-Planned)

- Target coordinates are entered **before takeoff** or during transit.
- Entered via CDU steerpoint or manual LAT/LONG/ELEV entry on DSMS JDAM sub-page.
- Weapon target is fixed — does not update from SPI.
- **Best for:** Known-position targets (buildings, bridges, bunkers, airfield infrastructure).

| PP Workflow |
|---|
| 1. Before flight: enter target coordinates via CDU steerpoint or DSMS manual entry |
| 2. DSMS → select JDAM → set target to PP steerpoint |
| 3. Fly CCRP steering cue → hold pickle → auto-release |
| 4. JDAM guides to pre-programmed coordinates |

### 9.3 DSMS JDAM Setup

| Step | Action | Notes |
|---|---|---|
| 1 | **DSMS** → select GBU-38 or GBU-31 | Confirm station and quantity |
| 2 | DSMS shows JDAM-specific sub-page | Displays target coordinates, mode, and status |
| 3 | Set **mode**: TOO or PP | TOO = SPI-driven; PP = pre-programmed coordinates |
| 4 | If PP: enter **LAT / LONG / ELEV** | Via CDU steerpoint selection or manual entry on DSMS sub-page |
| 5 | If TOO: verify SPI is on correct target | Set SPI from TGP (preferred) or other source |
| 6 | Set delivery mode: **CCRP** | Only mode for JDAM |
| 7 | Set fuze: **N+T / INST** (standard) or **N+T / DLY** (penetration) | |
| 8 | Verify **GPS status**: "GPS" indicator on DSMS | If no GPS, weapon falls back to INS — 30 m CEP instead of 10 m |

#### Target Elevation — Critical

| Factor | Impact |
|---|---|
| Correct target elevation | 10 m CEP — weapon hits within 33 ft of target |
| Target elevation wrong by 100 ft | Weapon misses by ~50–100 m (miss depends on release geometry) |
| Target elevation wrong by 500 ft | Weapon misses by several hundred meters — total miss |

**Rule:** Target elevation accuracy is the single most important factor in JDAM accuracy. Always use TGP laser-ranging for elevation when possible.

**Sources of elevation (in order of accuracy):**
1. **TGP laser range** — most accurate (~±1 m)
2. **DTED (Digital Terrain Elevation Data)** — good for terrain, bad for rooftops/elevated structures
3. **Mission planning tools** — depends on source map accuracy
4. **Pilot estimate** — unreliable; last resort

### 9.4 Delivery Profiles

#### Profile A: Medium-Altitude Level CCRP (Standard)

| Parameter | GBU-38 | GBU-31 |
|---|---|---|
| Altitude | 15,000–25,000 ft AGL | 15,000–25,000 ft AGL |
| Airspeed | 300–400 KIAS | 300–400 KIAS |
| Dive Angle | 0–10° | 0–10° |
| Release Mode | CCRP auto-release | CCRP auto-release |
| Standoff Range | 5–8 nm (depends on altitude and speed) | 5–10 nm |

**Technique:**
1. SPI set on target (TGP preferred for coordinate accuracy).
2. DSMS has JDAM selected in CCRP.
3. Fly the azimuth steering line — center it.
4. Watch range bar descend.
5. Hold pickle — weapon releases at computed point.
6. **Immediately break off** — no need to maintain LOS. JDAM is fire-and-forget.

#### Profile B: Loft Delivery (Maximum Standoff)

| Parameter | Value |
|---|---|
| Altitude | 5,000–15,000 ft AGL (entry) |
| Airspeed | 400+ KIAS |
| Technique | Pull to 20–30° nose-up; IFFCC releases weapon during climb arc |
| Standoff | Potentially 10–15+ nm |
| Use | Outside SAM engagement zone; terrain-masked approach |

**Technique:**
1. Ingress low/fast.
2. At computed point, pull up aggressively (20–30° nose-up).
3. CCRP computes release during climb — weapon releases at optimal point.
4. Weapon lofts on a high arc; GPS guides it to target.
5. Pilot pushes back down to low altitude after release.

### 9.5 Multi-JDAM Employment

| Technique | Method | Notes |
|---|---|---|
| **Same target, ripple** | Set ripple quantity > 1 on DSMS | Multiple JDAMs to same coordinate; redundancy |
| **Different targets, sequential** | Set SPI → release → set new SPI → release | Must re-designate between releases |
| **Different targets, pre-planned** | Pre-program multiple steerpoints; assign each JDAM to a steerpoint | Fastest multi-target method |

### 9.6 GPS Denial / INS Fallback

| GPS Status | JDAM Behavior | Accuracy |
|---|---|---|
| GPS available | Full GPS/INS guidance | ~10 m CEP |
| GPS denied (jamming) | INS-only guidance | ~30 m CEP (degrades with time since last GPS fix) |
| GPS denied for extended period | INS drift accumulates | > 50 m CEP possible |

> ⚠ **Realism Divergence:** DCS simulates GPS and INS behavior, but GPS jamming/denial is scenario-dependent and may not be present in all training missions. Students should understand the concept for operational realism — the weapon works without GPS but with reduced accuracy.

### 9.7 Common Student Errors

| Error | Correction |
|---|---|
| Wrong target coordinates (manual entry error) | Always cross-check coordinates against map. Use TGP-derived SPI whenever possible. |
| Target elevation not set or incorrect | Elevation is critical. Laser-range with TGP. Never leave elevation at 0 ft. |
| Releasing in TOO mode without setting SPI | JDAM has no target coordinates if SPI was never set. No guidance = miss. |
| Expecting JDAM to hit a moving target | JDAM flies to fixed coordinates. If the target moves after release, the bomb misses. Use LGB or LJDAM for movers. |
| Not verifying GPS status | "GPS" must be displayed on DSMS. If no GPS, brief the reduced accuracy. |
| Forgetting to hold pickle in CCRP | Release is consent-based: hold pickle through the auto-release point. If released early, weapon may not have valid solution. |
| Trying to use CCIP with JDAM | JDAM is CCRP only. CCIP mode does not apply. |

---

## Module 10: A-10C II Advanced Munitions

> **Note:** This module covers weapons and systems unique to the **A-10C II** upgrade. If the student is flying the base A-10C (non-II), this module may be deferred. All other modules in this dossier apply to both variants.

### 10.1 APKWS (Advanced Precision Kill Weapon System)

#### System Data

| Parameter | Value |
|---|---|
| Designation | APKWS II (WGU-59/B guidance section + Hydra 70 rocket) |
| Guidance | Semi-Active Laser Homing (SALH) |
| Warhead | M151 HE (10 lb) — same as unguided Hydra 70 |
| Motor | Mk 66 Mod 4 (same as standard Hydra 70) |
| Effective Range | 1.5–5.0 km |
| CEP | < 2 m (with stable laser designation) |
| Launcher | LAU-68 (7-tube) or LAU-131 (7-tube) |
| Laser Code | Must match designator (TGP or external) — default 1688 |

#### How APKWS Works

1. Pilot fires the rocket from a compatible launcher (same motor and trajectory as unguided Hydra 70).
2. After launch, the WGU-59/B guidance section deploys small steering fins and activates a **laser seeker** in the nose.
3. The rocket detects the **reflected laser energy** from a designated target.
4. The guidance section steers the rocket toward the laser spot — same principle as Paveway LGBs but on a rocket body.
5. **Laser must be ON the target before or at the moment of rocket motor ignition** — the seeker needs to acquire the laser energy during its short time of flight.

#### APKWS vs. Unguided Rockets vs. Maverick

| Factor | Unguided Hydra 70 | APKWS | AGM-65 Maverick |
|---|---|---|---|
| Guidance | None (ballistic) | Semi-active laser homing | EO-TV or IR lock-on |
| Accuracy | Area effect (~50 m CEP at 2 km) | ~2 m CEP | ~1 m CEP |
| Range | 1–3 km | 1.5–5 km | 4–10 nm (8–18 km) |
| Warhead | 10 lb HE | 10 lb HE (same) | 57 lb (D) or 300 lb (G) shaped charge |
| Cost per round | Very low | Low-moderate | Very expensive |
| Collateral damage | High (area weapon) | Very low | Moderate (large warhead) |
| Best use | Soft targets, marking | Precision CAS, danger-close, individual vehicles | Armor, bunkers, large targets |

**Decision rule:** Use APKWS when you need precision rocket fire with minimal collateral damage — soft vehicles, personnel in structures, danger-close situations where a 500 lb bomb is too much. Use Maverick for hard/armored targets at longer range.

#### DSMS APKWS Setup

| Step | Action | Notes |
|---|---|---|
| 1 | **DSMS** → select APKWS station | Confirm launcher and quantity |
| 2 | Set delivery mode: **CCIP** | CCIP is the primary mode for APKWS |
| 3 | Set **laser code** on DSMS APKWS sub-page | Must match TGP laser code (or buddy laser code) |
| 4 | **TGP** → acquire target → POINT track | Laser will fire from TGP |
| 5 | Arm **Master Arm** → ARM | |
| 6 | Arm **laser** → TGP laser arm | Laser must be active before firing |

#### DCS Employment Sequence

| Step | Action |
|---|---|
| 1 | TGP acquires target → POINT track → confirm stable track |
| 2 | DSMS: APKWS selected, CCIP mode, laser code set |
| 3 | Master Arm → ARM |
| 4 | TGP laser arm → ON (ensure laser is firing — confirm "L" on TGP MFCD) |
| 5 | Fly CCIP — place the CCIP pipper on or near the target |
| 6 | **Pickle** — rockets fire in selected salvo quantity |
| 7 | Rockets acquire laser in flight → guide to laser spot |
| 8 | Assess BDA on TGP; re-attack if needed |

> **Key timing note:** The TGP laser must be **actively designating** the target when the rocket is in flight. Unlike LGBs (which have a longer time of flight and can have the laser turned on later), APKWS rockets have a very short flight time (2–5 seconds), so **the laser should be on the target BEFORE firing**.

#### Delivery Profile

| Parameter | Value |
|---|---|
| Altitude | 5,000–12,000 ft AGL |
| Airspeed | 250–350 KIAS |
| Dive Angle | 5–20° |
| Range | 1.5–5.0 km (0.8–2.7 nm) slant range |
| Salvo Size | 1–4 rockets per trigger press |
| Mode | CCIP |

#### Common Student Errors

| Error | Correction |
|---|---|
| Laser not firing when rockets launch | Arm TGP laser BEFORE firing. Verify "L" indicator on TGP MFCD. |
| Laser code mismatch | DSMS APKWS code must match TGP laser code. Check both. |
| Firing at too long a range | APKWS effective max is ~5 km. Beyond that, rocket energy dissipates and guidance degrades. |
| Firing at too steep a dive angle | Rocket seeker has limited field of view — steep dives can cause seeker to lose the laser spot. Keep dive < 20°. |
| Using APKWS against heavy armor | M151 warhead is 10 lb HE — insufficient against MBTs. Use Maverick or LGB for heavy armor. |

> ⚠ **Realism Divergence:** APKWS is a relatively recent addition to DCS. Real-world APKWS employment procedures evolved significantly over its fielding. DCS models the basic SALH guidance and CCIP employment but may simplify some aspects of laser timing and seeker acquisition logic. Students should expect minor behavior differences compared to real-world TTP documentation.

---

### 10.2 GBU-39 SDB (Small Diameter Bomb)

#### System Data

| Parameter | Value |
|---|---|
| Designation | GBU-39/B Small Diameter Bomb (SDB I) |
| Guidance | GPS/INS (same principle as JDAM) |
| Warhead | 36 lb blast-fragmentation + penetrator case |
| Total Weight | ~250 lb |
| Wing Kit | Diamond Back deployable wings — extends glide range |
| Glide Range | Up to ~40 nm from 25,000 ft AGL (altitude dependent) |
| CEP | ~5–8 m (GPS); ~30 m (INS-only) |
| Carriage | 4 per BRU-61/A rack (high magazine depth) |
| Fuze | Electronic — programmable (impact or delay) |

#### How SDB Works

1. SDB receives target coordinates (LAT/LONG/ELEV) before release — same as JDAM.
2. At release, the Diamond Back wing kit deploys, giving the bomb a high lift-to-drag ratio.
3. The bomb **glides** toward the target coordinates, using GPS/INS guidance.
4. Standoff range depends on release altitude: higher = more glide range.
5. **Coordinate-based, fire-and-forget** — same concept as JDAM but lighter, longer range, smaller warhead.

#### SDB vs. JDAM — When to Use Each

| Factor | GBU-39 SDB | GBU-38 JDAM (500 lb) |
|---|---|---|
| Weight | 250 lb | 560 lb |
| Warhead | 36 lb (small) | ~200 lb (large) |
| Glide range | ~40 nm from 25,000 ft | ~8 nm from 25,000 ft |
| Accuracy | ~5–8 m CEP | ~10 m CEP |
| Per-station quantity | 4 per BRU-61 rack | 1 per station |
| Best use | Hardened point targets, standoff range, low collateral damage | General-purpose area destruction |

**Decision rule:** Use SDB when standoff range is needed, target is small/hardened, or collateral damage must be minimized. Use JDAM for larger targets where the bigger warhead is needed.

#### DSMS SDB Setup

| Step | Action | Notes |
|---|---|---|
| 1 | **DSMS** → select GBU-39 station (BRU-61 rack) | Shows 4 bombs per rack |
| 2 | Set **mode**: TOO or PP | Same as JDAM — TOO = SPI-driven, PP = pre-programmed |
| 3 | If PP: enter **LAT / LONG / ELEV** | Via CDU steerpoint or DSMS manual entry |
| 4 | If TOO: verify SPI is on correct target | TGP-derived SPI preferred |
| 5 | Set delivery mode: **CCRP** | CCRP only (same as JDAM) |
| 6 | Set fuze: as required | Impact or delay |
| 7 | Verify GPS status | GPS indicator on DSMS |

#### Delivery Profile

| Parameter | Value |
|---|---|
| Altitude | 15,000–25,000 ft AGL (higher = more range) |
| Airspeed | 300–400 KIAS |
| Dive Angle | 0–10° (level preferred for maximum glide) |
| Release Mode | CCRP auto-release |
| Standoff Range | 10–40 nm (altitude dependent) |

**Technique:** Same as JDAM — fly CCRP steering cue, hold pickle, auto-release, break off. No post-release guidance required.

#### Multi-SDB Employment

| Technique | Method |
|---|---|
| Same target, ripple | Multiple SDBs to same coordinates (redundancy or area saturation) |
| Different targets, sequential | BRU-61 rack can assign each of 4 SDBs to different pre-planned coordinates |
| Maximum magazine depth | 2× BRU-61 racks = 8 SDBs. High sortie productivity for multi-target missions. |

#### Common Student Errors

| Error | Correction |
|---|---|
| Releasing at low altitude | SDB glide range drops dramatically below 10,000 ft. Release high for standoff. |
| Expecting SDB to destroy large targets | 36 lb warhead. Effective against point targets (vehicles, bunkers) but not against large structures. Use JDAM/LGB for bigger targets. |
| Target elevation error | Same critical issue as JDAM — elevation accuracy is key. Use TGP laser-range. |
| Not assigning individual coordinates to each SDB | If all 4 go to same target, you waste 3 bombs. Use DSMS to assign different steerpoints. |

> ⚠ **Realism Divergence:** SDB in DCS may not fully model the Diamond Back wing deployment animation or the full range of the real weapon from maximum altitude. Glide range may be somewhat reduced compared to published real-world figures. Students should experiment with release altitudes to calibrate expectations.

---

### 10.3 GBU-54 LJDAM (Laser JDAM)

#### System Data

| Parameter | Value |
|---|---|
| Designation | GBU-54/B Laser JDAM |
| Body | Mk-82 (500 lb) |
| Guidance | GPS/INS + Semi-Active Laser Homing (terminal phase) |
| Total Weight | ~570 lb |
| CEP (GPS only) | ~10 m |
| CEP (GPS + laser terminal) | ~3 m (moving target capable) |
| Laser Code | Must match designator — default 1688 |

#### How LJDAM Works

1. LJDAM launches exactly like a standard JDAM — GPS/INS guidance to programmed coordinates.
2. During the **terminal phase** (final 10–15 seconds of flight), the DSU-38/B laser sensor in the nose activates.
3. If the sensor detects reflected laser energy matching its code, the weapon **corrects from GPS to laser**.
4. This allows the weapon to engage **moving targets** — the laser follows the target, and the bomb follows the laser.
5. If no laser is detected, the weapon continues on GPS/INS guidance (degrades to standard JDAM accuracy).
6. **Dual-mode failsafe:** Even if the laser drops out, the weapon still hits the GPS coordinates — it doesn't go ballistic.

#### LJDAM vs. JDAM vs. LGB

| Factor | GBU-54 LJDAM | GBU-38 JDAM | GBU-12 LGB |
|---|---|---|---|
| Guidance | GPS/INS + laser (terminal) | GPS/INS only | Laser only |
| Moving targets | Yes (laser tracks them) | No | Yes (if laser tracks them) |
| All-weather | Yes (GPS; laser improves terminal) | Yes | No (laser needs LOS) |
| Accuracy | ~3 m (with laser) / ~10 m (GPS only) | ~10 m | ~1–3 m |
| Failsafe | Hits GPS coords if laser lost | N/A (GPS always) | Goes ballistic if laser lost |

**Decision rule:** LJDAM is the best weapon for **moving targets in any weather**. Use it when the target might move but conditions might be marginal. Use standard JDAM for stationary targets. Use LGB when weather is clear and maximum accuracy is needed.

#### DSMS LJDAM Setup

| Step | Action | Notes |
|---|---|---|
| 1 | **DSMS** → select GBU-54 | Station and quantity |
| 2 | Set **mode**: TOO or PP | Same as JDAM |
| 3 | Enter coordinates (PP) or verify SPI (TOO) | Same as JDAM |
| 4 | Set **laser code** on DSMS sub-page | Must match TGP laser code |
| 5 | Set delivery mode: **CCRP** | CCRP only |
| 6 | Set fuze as required | |
| 7 | Verify GPS status | |
| 8 | Arm TGP laser — will need to lase in terminal phase | |

#### DCS Employment Sequence — Moving Target

| Step | Action |
|---|---|
| 1 | TGP acquires moving target → AREA track (let TGP track the target) |
| 2 | Set SPI from TGP (TMS UP) — coordinates flow to LJDAM |
| 3 | DSMS: GBU-54 selected, CCRP, laser code set |
| 4 | Master Arm → ARM |
| 5 | Fly CCRP steering cue → hold pickle → auto-release |
| 6 | After release: TGP continues tracking the moving target |
| 7 | In terminal phase (~10–15 sec before impact): arm TGP laser → lase target |
| 8 | LJDAM detects laser → corrects from GPS to laser → follows moving target |
| 9 | Impact and BDA |

> **Critical:** Laser must be ON the target during the terminal phase. Too early wastes laser time and risks losing track. Too late means the weapon doesn't have time to correct. DCS models this timing window.

#### Delivery Profile

| Parameter | Value |
|---|---|
| Altitude | 15,000–25,000 ft AGL |
| Airspeed | 300–400 KIAS |
| Dive Angle | 0–10° |
| Release Mode | CCRP auto-release |
| Laser | ON in terminal phase (~last 10–15 seconds) |

#### Common Student Errors

| Error | Correction |
|---|---|
| Not lasing during terminal phase | LJDAM needs laser in final seconds. Without laser, it hits GPS coords — misses moving target. |
| Laser code mismatch | DSMS code must match TGP. Check both before release. |
| Releasing on a moving target without using LJDAM | Standard JDAM hits fixed coordinates. If target moves, it misses. Use LJDAM or LGB for movers. |
| Lasing too early (wasting laser energy) | Wait until terminal phase. TGP laser has limited continuous-use time in some models. |

> ⚠ **Realism Divergence:** GBU-54 LJDAM is a relatively recent DCS addition. The real DSU-38/B laser sensor has specific acquisition timing and field-of-view constraints that DCS simplifies. Students may find the weapon slightly more forgiving in DCS than real-world performance data would suggest.

---

### 10.4 HMCS (Helmet-Mounted Cueing System)

#### System Overview

| Parameter | Value |
|---|---|
| System | Scorpion HMCS (A-10C II) |
| Function | Head-tracked targeting; projects targeting symbology on visor |
| Integration | SPI system, TGP, Maverick, all weapons via SPI |
| Modes | A/G (air-to-ground) and A/A (air-to-air) |

#### How HMCS Changes the Targeting Workflow

**Without HMCS (standard A-10C):**
1. Find target visually or via SA page.
2. Slew TGP to target area (China Hat, HOTAS slew).
3. TGP acquires and tracks target.
4. Set SPI from TGP.
5. Weapon receives SPI coordinates.
6. Employ weapon.

**With HMCS (A-10C II):**
1. Pilot **looks at the target** through the HMCS visor.
2. TMS UP → **SPI set to HMCS line-of-sight** (instantly).
3. TGP automatically slews to HMCS designation point.
4. TGP refines and tracks target.
5. Weapon receives SPI coordinates.
6. Employ weapon.

**Advantage:** Steps 2–3 from the non-HMCS workflow are compressed into a single head movement + button press. This dramatically reduces the **sensor-to-shooter timeline** — critical in time-sensitive CAS.

#### HMCS Employment Modes

| Mode | Function | Best For |
|---|---|---|
| **SPI designation** | Look at target → TMS UP → SPI set to HMCS LOS | Rapid JDAM/LGB/SDB targeting |
| **TGP slew** | HMCS commands TGP to look at pilot's head position | Finding targets quickly with TGP |
| **Maverick cueing** | HMCS slews Maverick seeker to pilot's look angle | Rapid Maverick lock-on |
| **AIM-9 cueing** | HMCS designates A/A target for Sidewinder | Off-boresight missile cueing |

#### DCS HMCS Setup

| Step | Action | Notes |
|---|---|---|
| 1 | HMCS power → ON | Helmet-mounted display activates |
| 2 | Verify alignment | HMCS aligns automatically; verify symbology overlay is accurate |
| 3 | Select SOI (Sensor of Interest) as needed | China Hat controls which sensor HMCS commands |
| 4 | Look at target → TMS UP | SPI set to HMCS LOS; TGP slews to that point |

#### HMCS + Weapon Integration Examples

**HMCS → JDAM (rapid TOO targeting):**
1. Pilot sees target → looks at it with HMCS.
2. TMS UP → SPI set → coordinates flow to JDAM in TOO mode.
3. TGP slews to that point → pilot confirms target on TGP MFCD.
4. Fly CCRP → release.

**HMCS → Maverick:**
1. Maverick powered and selected on DSMS.
2. Pilot looks at target with HMCS.
3. HMCS slews Maverick seeker to pilot's look angle.
4. Maverick seeker acquires target → pilot confirms → TMS UP to lock.
5. Pickle.

**HMCS → AIM-9:**
1. A/A mode selected.
2. Pilot looks at bandit with HMCS.
3. AIM-9 seeker cued to pilot's look angle.
4. Seeker acquires → tone → uncage → fire.

#### Common Student Errors

| Error | Correction |
|---|---|
| Not using HMCS for initial target cueing | HMCS dramatically speeds up the targeting cycle. Always use it for first-look acquisition. |
| Trusting HMCS SPI as final coordinates | HMCS gives approximate coordinates from head position. Always refine with TGP before releasing weapons. |
| Head movement after TMS UP | Once TMS UP is pressed, the SPI is set. Moving your head afterward doesn't change it. Re-designate if needed. |
| Not verifying TGP refined the target | After HMCS designation, check TGP MFCD to confirm the sensor is tracking the correct target before releasing. |

> ⚠ **Realism Divergence:** The Scorpion HMCS in DCS requires TrackIR, VR, or another head-tracking solution to function. Without head tracking, HMCS is not usable. Real-world HMCS alignment and accuracy may differ from the DCS implementation. Students should calibrate their head-tracking system carefully for best results.

---

## Module 11: AIM-9M Sidewinder (Self-Defense Air-to-Air)

### 11.1 Missile Data

| Parameter | Value |
|---|---|
| Designation | AIM-9M Sidewinder |
| Guidance | Infrared homing (all-aspect, rear-aspect preferred) |
| Seeker | Cooled indium antimonide (InSb) IR detector |
| IRCCM | Yes — reduced susceptibility to flares (closed-loop tracking) |
| Warhead | WDU-17/B annular blast-fragmentation (~20.8 lb) |
| Fuze | Active laser proximity + contact |
| Weight | ~188 lb |
| Effective Range | ~0.5–5 nm (conditions dependent) |
| Max G | ~35 G (missile capability) |
| Motor | Mk 36 Mod 11 solid-fuel rocket |
| Envelope | All-aspect engagement; highest Pk from rear hemisphere |

### 11.2 A/A Mode & HUD Symbology

#### Entering A/A Mode

| Step | Action | Notes |
|---|---|---|
| 1 | Master Mode → **A/A** | Via HOTAS or cockpit panel switch |
| 2 | DSMS shows AIM-9 selected | If more than one A/A weapon, ensure Sidewinder is active |
| 3 | HUD transitions to **A/A symbology** | Different from A/G HUD |

#### A/A HUD Symbology

| Symbol | Description |
|---|---|
| **Seeker Circle** | Shows where the AIM-9 seeker is looking (small circle, moves with seeker) |
| **Target Designator Box** | TD box appears around a tracked/locked target |
| **Missile Diamond** | AIM-9 ready indicator — shows lock status |
| **Range Cue** | Dynamic launch zone: Rmax (max range) and Rmin (min range) displayed |
| **Aspect Cue** | Indicates target aspect angle (head-on, beam, tail) |
| **Shoot Cue** | Appears when within valid launch envelope |

### 11.3 Seeker Operations

| Seeker State | Audio | HUD | Action |
|---|---|---|---|
| **Uncooled / OFF** | None | No seeker circle | Power on missile; wait for cool-down |
| **Caged (boresight)** | Low growl | Seeker circle centered on boresight | Seeker is slaved to aircraft boresight or radar/HMCS cue |
| **Tracking (search)** | Increasing growl | Seeker circle moves toward heat source | Seeker is detecting IR energy — not yet locked |
| **Locked** | Steady high-pitch tone | Seeker circle locked on target; diamond/shoot cue appears | Seeker is locked on — valid launch if within envelope |

#### Seeker Employment Steps

| Step | Action |
|---|---|
| 1 | A/A mode → AIM-9 selected |
| 2 | Point nose toward target (within seeker gimbal limits — ~±40° off boresight) |
| 3 | Listen for **growl** — seeker is detecting IR energy |
| 4 | **TMS UP** → uncage seeker (allows seeker to track freely) |
| 5 | Seeker slews to target — growl increases → becomes **steady high tone** = locked |
| 6 | Verify within launch envelope (range cue and shoot cue on HUD) |
| 7 | **Pickle** → missile launches |
| 8 | Observe missile track → break for defense |

### 11.4 HMCS Integration (A-10C II Only)

| Step | Action |
|---|---|
| 1 | A/A mode → AIM-9 selected |
| 2 | HMCS powered and aligned |
| 3 | **Look at target** with HMCS — AIM-9 seeker cued to pilot's head direction |
| 4 | Seeker acquires target at high off-boresight angle (up to ~±60° with HMCS cue) |
| 5 | Growl → steady tone = locked |
| 6 | Pickle → missile launches |

**HMCS advantage:** Allows engaging targets at high off-boresight angles without needing to point the aircraft nose at the target. Critical for self-defense when bandit is not directly ahead.

### 11.5 Self-Defense Doctrine

> **The A-10C is NOT a fighter.** AIM-9 Sidewinder on the A-10 is a **self-defense weapon only**. The A-10's speed, maneuverability, and lack of radar make it a poor dogfighter. The goal is **survival**, not air-to-air kills.

#### Decision Matrix: Engage or Evade?

| Situation | Action |
|---|---|
| Bandit in weapons envelope, closing, no escape option | ENGAGE — fire AIM-9 in self-defense |
| Bandit at range, not yet committed | EVADE — terrain mask, call for fighter CAP |
| Multiple bandits | EVADE — jettison stores, max power, terrain mask, call for help |
| Bandit in beam/behind, high aspect rate | ENGAGE if opportunity shot presents; otherwise EVADE |
| Friendly fighters en route | EVADE and survive until help arrives |

#### Self-Defense Priorities (in order)

1. **Jettison stores** — drop bombs/rockets to reduce weight and drag. Use emergency jettison if needed.
2. **Max power / terrain mask** — A-10 is slow; use terrain to break LOS with bandit.
3. **Call for help** — "MAYDAY" or "DEFENSIVE" on appropriate frequency. Request fighter escort.
4. **Fire AIM-9 if no other option** — only if bandit is within envelope and you have no escape route.
5. **Maneuver aggressively** — use the A-10's tight turn radius at low speed; force an overshoot.

#### Jettison Procedures

| Method | Action | Notes |
|---|---|---|
| **Selective jettison** | DSMS → select stations → jettison | Drops specific stores; keeps Sidewinders |
| **Emergency jettison** | Emergency jettison button | Drops ALL stores (including Sidewinders!) — last resort |

> **Key principle:** If you're engaged by fighters, your primary survival tool is **terrain masking** and **friendly fighter support** — not the AIM-9. Fire it only if you have a clean shot and no other option.

### 11.6 Common Student Errors

| Error | Correction |
|---|---|
| Trying to dogfight in an A-10 | The A-10 is NOT a fighter. Do not attempt extended BFM. Defend, fire if opportunity, evade. |
| Not jettisoning stores when engaged | Stores add weight and drag. Jettison bombs/rockets immediately to gain speed and maneuverability. |
| Firing at max range | AIM-9M Pk drops significantly at long range. Wait for a clean tone and closer range. Rear-aspect preferred. |
| Forgetting to uncage seeker | TMS UP to uncage. If the seeker stays caged, it won't track. |
| Firing without tone | No steady tone = no lock. Missile will guide on whatever IR source it finds (or nothing). Wait for tone. |
| Neglecting to call for help | Always call DEFENSIVE on frequency. Friendly fighters are your best defense. |
| Engaging when they should evade | If escape is possible, escape. AIM-9 engagement should be last resort. |

> ⚠ **Realism Divergence:** In real life, AIM-9M IRCCM is quite effective against flares, but DCS models this variably depending on scenario design. Also, real-world A-10 pilots receive extensive air combat maneuvering training beyond what's covered here — DCS students should practice basic defensive BFM (break turns, scissors, rate fight) against AI opponents in training missions.

---

## Module 12: ECM, Countermeasures & Defensive Systems

### 12.1 Defensive Systems Overview

The A-10C integrates four primary defensive systems:

| System | Function | Type |
|---|---|---|
| **ALR-69 RWR** | Radar Warning Receiver — detects and identifies radar emitters | Passive (receive only) |
| **CMSP** | Countermeasures Signal Processor — manages CM dispensing programs | Controller |
| **ALE-47 CMDS** | Countermeasures Dispensing Set — dispenses chaff and flares | Active (dispense) |
| **ALQ-131 / ALQ-184 ECM Pod** | Electronic Countermeasures — jams enemy radar | Active (transmit) |

These systems work together as a **layered defense**: detect the threat (RWR), counter it electronically (ECM pod) and kinetically (chaff/flares), and maneuver to defeat it (pilot action).

### 12.2 ALR-69 Radar Warning Receiver (RWR)

#### RWR Display

| Feature | Description |
|---|---|
| Display location | Left front panel (CRT display) |
| Display type | Azimuth (bearing) display — top of display = aircraft nose |
| Threat symbols | Alphanumeric codes positioned at relative bearing |
| Range indication | Closer to center = higher signal strength (approximately closer range) |
| Priority | Most dangerous threat highlighted (typically closest or in launch mode) |

#### Threat Symbols (DCS Common)

| Symbol | Threat Type | Example |
|---|---|---|
| **2** | SA-2 Guideline | Long-range, high-altitude SAM |
| **3** | SA-3 Goa | Medium-range SAM |
| **6** | SA-6 Gainful | Mobile medium-range SAM |
| **8** | SA-8 Gecko | Short-range mobile SAM |
| **11** | SA-11 Gadfly (Buk) | Medium-range mobile SAM |
| **15** | SA-15 Gauntlet (Tor) | Short-range mobile SAM (highly dangerous) |
| **19** | SA-19 Grison (Tunguska) | Combo gun/missile SPAAG |
| **A** | AAA radar (ZSU-23-4, etc.) | Radar-guided anti-aircraft artillery |
| **S** | Search radar | Early warning; not yet tracking |
| **M** | MiG / airborne fighter radar | Air-to-air threat |

#### RWR Audio Cues

| Audio | Meaning | Urgency |
|---|---|---|
| **New contact tone** (single beep) | New emitter detected | Low — awareness |
| **Steady warble** | Radar is tracking you (STT or TWS) | Medium — prepare to defend |
| **Rapid high-pitch tone** | **MISSILE LAUNCH** — missile is in the air | **CRITICAL — immediate action** |
| **PRF change** (tone shifts) | Emitter changed mode (search → track → launch) | Escalating — respond to each change |

#### RWR Procedures

| Step | Action |
|---|---|
| 1 | **Scan RWR display** continuously during ingress/egress |
| 2 | Identify threat type by symbol |
| 3 | Note bearing — plan maneuver to avoid or mask |
| 4 | If tracking: prepare CM program, consider terrain masking |
| 5 | If **launch**: execute immediate defensive response (see 12.6) |

### 12.3 CMSP (Countermeasures Signal Processor)

#### CMSP Panel

| Control | Function |
|---|---|
| **MWS** (Missile Warning System) | Not functional in DCS A-10C (placeholder) |
| **JMR** (Jammer) | ECM pod on/off (if loaded) |
| **RWR** | RWR audio on/off and display mode |
| **DISP** (Dispense) | Countermeasures mode selector |
| **Mode Selector** | OFF / STBY / MAN / SEMI / AUTO |

#### CMSP Modes

| Mode | Behavior | Use Case |
|---|---|---|
| **OFF** | No CM dispensing | Pre-flight / on ground |
| **STBY** (Standby) | System powered but no dispensing | Taxiing, holding |
| **MAN** (Manual) | Pilot manually presses chaff or flare button; dispenses per selected program | Full pilot control |
| **SEMI** (Semi-Auto) | RWR-triggered: when RWR detects specific threat, CMSP recommends program; pilot confirms with button press | Reduced workload; pilot still in the loop |
| **AUTO** | Fully automatic: CMSP dispenses CM automatically in response to RWR-detected threats | High-threat environment; maximum automation; uses expendables faster |

**Recommendation:** Use **MAN** for training and low-threat environments. Use **SEMI** or **AUTO** in high-threat environments where pilot workload is already high.

#### CM Programs

The CMSP has **6 programmable CM programs** (1–6), each defining:

| Parameter | Options |
|---|---|
| **Chaff quantity** | Number of chaff bundles per dispense event |
| **Chaff interval** | Time between chaff bundles (seconds) |
| **Flare quantity** | Number of flares per dispense event |
| **Flare interval** | Time between flares (seconds) |
| **Repeat count** | Number of times the program repeats |
| **Sequence** | Chaff-only, flare-only, or interleaved |

#### Default Program Examples (Typical)

| Program | Chaff | Flare | Use |
|---|---|---|---|
| **PGM 1** | 2 chaff, 0.5s interval | 2 flares, 0.5s interval | General-purpose |
| **PGM 2** | 4 chaff, 0.25s interval | 0 flares | Radar threat only |
| **PGM 3** | 0 chaff | 4 flares, 0.5s interval | IR threat only |
| **PGM 4** | 6 chaff, 0.25s interval | 6 flares, 0.25s interval | Heavy threat — rapid dispense |

> **Note:** Programs are configurable in the DCS Mission Editor (per-aircraft loadout) or via in-cockpit CMSP programming. Students should learn to verify and set programs during pre-flight.

#### CMSP Programming Steps (In-Cockpit)

| Step | Action |
|---|---|
| 1 | CMSP → MAN mode |
| 2 | Press CMSP **PROG** button to enter programming mode |
| 3 | Select program number (1–6) using increment buttons |
| 4 | Set chaff burst count, interval |
| 5 | Set flare burst count, interval |
| 6 | Set repeat count and sequence |
| 7 | Exit programming mode |

### 12.4 ALE-47 Countermeasures Dispensing Set

#### Inventory

| Expendable | Typical Load | Function |
|---|---|---|
| **Chaff** (RR-170/AL) | 120 bundles (variable) | RF decoy — creates false radar returns |
| **Flare** (MJU-7/B) | 60 flares (variable) | IR decoy — creates hot signature to seduce IR missiles |

#### Dispense Controls (HOTAS)

| Control | Action |
|---|---|
| **Chaff button** (Throttle) | Dispenses chaff per active CM program |
| **Flare button** (Throttle) | Dispenses flares per active CM program |
| **Panic / ECM Dispense** (if mapped) | Rapid all-type dispense |

#### Chaff vs. Flare — When to Use

| Threat Type | Counter | Expendable |
|---|---|---|
| **Radar-guided SAM** (SA-2, SA-6, SA-8, SA-11) | **Chaff** + maneuvering + ECM | Chaff bundles |
| **IR-guided SAM** (SA-9, SA-13, Igla, Strela) | **Flares** + maneuvering | Flares |
| **IR-guided AAM** (R-60, R-73, AIM-9 equivalent) | **Flares** + break turn | Flares |
| **Radar-guided AAM** (R-27R, AIM-7 equivalent) | **Chaff** + notch maneuver | Chaff |
| **AAA** (ZSU-23-4) | **Chaff** (if radar-guided) + jink | Chaff (if radar tracking); maneuver is primary |
| **MANPADS** (Igla, Stinger) | **Flares** + aggressive break | Flares (high priority) |

### 12.5 ALQ-131 / ALQ-184 ECM Pod

#### System Data

| Parameter | ALQ-131 | ALQ-184 |
|---|---|---|
| Type | Self-protection jammer | Self-protection jammer |
| Function | Transmits electronic countermeasures against radar threats | Same |
| Station | Station 6 (centerline pylon) — displaces one weapon station | Same |
| Modes | Standby, Transmit | Standby, Transmit |
| Effectiveness | Band-specific; works against older radar systems | Improved band coverage |

#### ECM Employment

| Step | Action |
|---|---|
| 1 | ECM pod loaded on Station 6 (mission planning) |
| 2 | CMSP → JMR (Jammer) → ON |
| 3 | ECM pod enters standby; transmit mode activates automatically when RWR detects threat (in some configurations) |
| 4 | Manual activation: CMSP JMR transmit |

#### ECM Considerations

| Factor | Guidance |
|---|---|
| **When to transmit** | When entering threat envelope; turn off when no radar threats (reduces RF signature) |
| **EMCON (Emission Control)** | Active jamming reveals your position by bearing. If stealth/surprise is needed, keep ECM off. |
| **ECM vs. terrain masking** | Terrain masking is preferred over active ECM when possible — silent is better than loud |
| **ECM + chaff** | Use both together against radar threats — chaff creates false returns while ECM jams tracking |
| **Modern threats** | Some modern SAMs (SA-11, SA-15) have ECCM (electronic counter-countermeasures) — ECM alone may not be sufficient |
| **Weight penalty** | ECM pod on Station 6 = one fewer weapon station. Plan loadout accordingly. |

### 12.6 Defensive Maneuvering Integration

#### Layered Defense Model

| Layer | System | Action |
|---|---|---|
| **1. Avoid** | Mission planning | Route around known threats; use terrain masking |
| **2. Detect** | ALR-69 RWR | Identify threat type, bearing, mode (search/track/launch) |
| **3. Counter (electronic)** | ALQ-131/184 ECM | Jam threat radar; degrade tracking solution |
| **4. Counter (expendable)** | ALE-47 chaff/flare | Decoy missile seeker away from aircraft |
| **5. Maneuver** | Pilot | Break turn, notch, terrain mask, jink |
| **6. Engage (last resort)** | Weapons | SEAD (if equipped), AIM-9 (if air threat) |

#### Threat-Specific Defensive Reactions

##### Radar-Guided SAM (SA-2, SA-6, SA-8, SA-11, SA-15)

| Phase | Action |
|---|---|
| RWR shows tracking | ECM ON; note bearing; plan escape route; prepare chaff |
| RWR shows **LAUNCH** | Immediately: **hard break turn** perpendicular to threat bearing (beam / 3-9 line) |
| During break | Dispense **chaff** (4–6 bundles, rapid interval); maintain break |
| **Notch maneuver** | Place the SAM on your 3 or 9 o'clock — Doppler radar loses you in the ground clutter |
| After notch | Terrain mask — descend to put terrain between you and the SAM |
| Re-assess | Check RWR — if threat persists, continue maneuvering; if cleared, resume mission |

##### IR-Guided SAM / MANPADS (SA-9, SA-13, Igla, Strela)

| Phase | Action |
|---|---|
| RWR warning (may not detect IR threats!) | Visual scan for launch smoke/flash |
| Visual launch detection | Immediately: **hard break toward the missile** + **flares** (4+ flares, rapid interval) |
| During break | Maximum G turn into the missile to increase crossing rate; continue flares |
| After break | Reduce IR signature: throttle back (briefly), jink, terrain mask |
| Note | IR threats have short range (1–4 nm) — if you can extend to 5+ nm, you're likely safe |

##### Radar-Guided AAA (ZSU-23-4, Gepard)

| Phase | Action |
|---|---|
| RWR shows AAA tracking | Immediate **jink** — unpredictable heading/altitude changes |
| While in envelope | Random jink pattern: ±30° heading changes every 2–3 seconds; vary altitude ±500 ft |
| Chaff | Dispense chaff to break radar lock (limited effectiveness against continuous tracking) |
| Primary defense | **Speed + jink + terrain mask** — AAA is most effective against predictable flight paths |
| Exit | Egress out of AAA envelope (~2–4 nm range) as quickly as possible |

##### Air-to-Air Threat (Fighter)

| Phase | Action |
|---|---|
| RWR shows fighter radar | Assess situation: bearing, range, aspect |
| Fighter inside 10 nm, closing | **Defensive call** on frequency; jettison stores; max power |
| Fighter has radar lock | Dispense chaff + notch (beam the threat) |
| Fighter firing IR missile | Break toward missile + flares |
| Fighter in visual range | If AIM-9 opportunity: fire → break → extend. If not: terrain mask |
| Primary survival | **Terrain masking + speed + friendly fighter support** — do NOT attempt extended BFM |

### 12.7 Expendable Management

| Principle | Guidance |
|---|---|
| **Conservation** | Expendables are limited. Don't dump all chaff/flares on first threat. |
| **Budget** | Mentally divide expendables by expected threat exposures on the mission |
| **Priority** | Save flares for IR threats (MANPADS in CAS environment are the #1 killer) |
| **Awareness** | Monitor expendable remaining count on CMSP display |
| **Bingo** | If expendables reach bingo (≤20% remaining), consider aborting to replenish |

### 12.8 Common Student Errors

| Error | Correction |
|---|---|
| CMSP left in STBY during mission | Set CMSP to MAN or SEMI before entering threat environment. STBY = no CM dispense. |
| Not checking CM programs pre-flight | Verify chaff/flare programs match expected threats. Flare-heavy for CAS; chaff-heavy for SEAD suppression. |
| Dumping all expendables on first threat | Conserve. Use minimum effective quantity per threat engagement. Budget for the full mission. |
| Not notching radar SAMs | Break turn alone is insufficient. You must put the threat on your beam to exploit Doppler notch. |
| Flying predictable path through AAA | Jink. Constant heading/altitude = death against radar-guided AAA. |
| ECM on when not needed | Active jamming radiates RF energy. It tells everyone where you are. Use only when in threat envelope. |
| Ignoring RWR audio | Audio cues are faster than visual. Learn the tones: new contact → tracking → LAUNCH. React immediately to launch tone. |
| Not terrain masking | Terrain is your best friend. Hills and ridgelines block both radar and IR threats. Use them aggressively. |
| Trying to outrun missiles | The A-10 is slow (~300–400 KIAS max). You CANNOT outrun a SAM or AAM. Maneuver + CM is the answer. |
| Forgetting to jettison stores when engaged by fighters | Every pound of ordnance slows you down. Jettison everything (except AIM-9) when fighters are on you. |

> ⚠ **Realism Divergence:** DCS models countermeasure effectiveness and threat behavior with varying fidelity depending on the threat module. Some SAMs may be more or less susceptible to chaff/ECM than real-world counterparts. The ALR-69 RWR in DCS provides accurate bearing but signal-strength-based range estimation is approximate. CMSP AUTO mode may behave differently from real-world threat-library-driven automatic dispense logic. Students should experiment with defensive reactions against each specific DCS SAM type to calibrate expectations.

---

*This concludes the A-10C / A-10C II Weapons Employment Research Dossier. All 12 modules are complete and ready for conversion into a structured training course.*

*Based on DCS World module documentation, Eagle Dynamics forums, real-world USAF T.O. 1A-10C-34-1 (Nonnuclear Weapons Delivery Manual), and community-sourced employment data. For simulation use only.*
