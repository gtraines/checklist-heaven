# UH-1H Huey Weapons Employment Course — Research Dossier

> **Aircraft:** Bell UH-1H Iroquois ("Huey") | **Module:** Belsimtek / Eagle Dynamics DCS World
>
> **Course Level:** Post-BQT weapons qualification | **Platform Type:** Unguided weapons only — no precision guidance, no targeting sensors
>
> **Sources:** TM 55-1520-210-10, TM 55-1520-210-CL, TM 9-1055-476-13&P, FM 3-04.140, FM 1-240, ATP 3-04.1, TC 1-237; DCS UH-1H module documentation and in-game behavior.

---

> **Scope:** This dossier supports a multi-event UH-1H Weapons Employment Course (WEC) for students who have completed the UH-1H BQT. All weapons described are unguided and visually aimed. Accuracy depends entirely on the pilot's mastery of ballistics, sight picture, and aircraft energy management. Simulation-specific behavior is documented as primary instruction; real-world references provide context and depth.

---

## Module 1: Weapons Systems Overview & Cockpit Armament Switchology

### 1.1 Weapons Available in the DCS UH-1H — Full Inventory

The DCS UH-1H module (Belsimtek / Eagle Dynamics) models the aircraft in a flexible gunship configuration. The following weapons are available for selection in the Mission Editor and loadout screen:

| Weapon | Type | Station | DCS Modeled | Notes |
|---|---|---|---|---|
| XM-158 7-tube launcher | 2.75-inch FFAR rocket pod | Left or right pylon | Yes — full | Compact; 7 tubes; standard suppression loadout |
| XM-159 19-tube launcher | 2.75-inch FFAR rocket pod | Left or right pylon | Yes — full | High-capacity area suppression pod |
| M134 Minigun pod | 7.62×51mm, 6-barrel rotary | Left or right pylon | Yes — forward fire | Electrically driven; pilot-aimed |
| M60D Door Gun (port) | 7.62×51mm, single-barrel | Port (left) door station | Yes — crew station | Flexible; crew-aimed; player-switchable seat |
| M60D Door Gun (starboard) | 7.62×51mm, single-barrel | Starboard (right) door station | Yes — crew station | Flexible; crew-aimed; player-switchable seat |

**Available Rocket Warhead Variants (DCS vs. real-world):**

| Warhead | Designation | DCS Modeled | Notes |
|---|---|---|---|
| High Explosive (10 lb) | M151 HE | Yes | Primary anti-personnel / light armor warhead |
| High Explosive (17 lb) | M229 HE | Yes | Heavier blast; better against light vehicles and structures |
| White Phosphorus | M156 WP | Yes | Smoke/incendiary marking; visible burn; real-world incendiary use |
| Illumination (parachute flare) | M257 Illum | Yes | Parachute-deployed flare; night operations |
| Flechette/APERS | M255/M257 variant | No (real-world only) | Anti-personnel dart warhead; not modeled in DCS |
| High Explosive, shaped charge | M247 HEAT | No (real-world only) | Anti-armor round; not modeled in DCS UH-1H |

> *⚠ Realism Divergence: Real UH-1H gunship loadouts in Vietnam-era operations commonly included flechette (APERS) warheads for anti-personnel area coverage. DCS does not model flechette or the M247 HEAT round — the DCS loadout screen offers M151, M229, M156, and M257. Training focuses on available DCS warheads.*

---

### 1.2 Pylon/Station Configuration

**Station identification:**
- **Left pylon** (port stub wing): Forward-firing weapons; rockets or minigun pod.
- **Right pylon** (starboard stub wing): Forward-firing weapons; rockets or minigun pod.
- **Port door station** (left aft): M60D door gun on swivel/pintle mount.
- **Starboard door station** (right aft): M60D door gun on swivel/pintle mount.

**Maximum load per pylon (approximate, TM 55-1520-210-10 and DCS behavior):**
- XM-159 (19-tube pod): ~68 kg (150 lb) unloaded; ~95 kg (210 lb) loaded with 19 × 2.75-inch rockets.
- XM-158 (7-tube pod): ~27 kg (60 lb) unloaded; ~40 kg (88 lb) loaded.
- M134 pod: ~30 kg (66 lb) unloaded; up to ~115 kg (253 lb) loaded with 1,500 rounds of 7.62mm belt.
- Maximum gross weight limit for weapons-loaded configurations is governed by Vne and hover power margin. See Module 8.

**Compatible weapons per station:**

| Station | Compatible Weapons |
|---|---|
| Left pylon | XM-158, XM-159, M134 pod (one weapon per pylon) |
| Right pylon | XM-158, XM-159, M134 pod (one weapon per pylon) |
| Port door | M60D door gun (fixed to door mount) |
| Starboard door | M60D door gun (fixed to door mount) |

> *Note: DCS does not allow two different forward-firing weapon types on the same pylon simultaneously. You may mix types between pylons (e.g., M134 left + XM-159 right), but not stack within a single pylon.*

**Typical combat loadout configurations:**

| Configuration | Left Pylon | Right Pylon | Door Guns | Notes |
|---|---|---|---|---|
| Clean | None | None | M60D × 2 | Maximum performance; door guns only |
| Light rockets | XM-158 | XM-158 | M60D × 2 | 14 rockets total; minimal weight penalty |
| Heavy rockets | XM-159 | XM-159 | M60D × 2 | 38 rockets total; significant weight; LZ prep |
| Minigun only | M134 | M134 | M60D × 2 | Maximum gun firepower; no rockets |
| Mixed (standard gunship) | M134 | XM-159 | M60D × 2 | Versatile; rockets for range, minigun for suppression |
| Full gunship (heavy) | XM-159 | XM-159 | M60D × 2 | Maximum firepower; greatest weight/performance penalty |

**Effect of asymmetric loadout on handling:**
An asymmetric configuration (e.g., one pylon loaded, the other empty) creates a rolling moment toward the heavier side and requires sustained cyclic input or trim bias to maintain wings-level flight. During attack runs, asymmetry complicates aiming — the pilot must pre-compensate. It is preferable to maintain symmetric loads; if one pylon is jettisoned or expended, adjust trim immediately and consider jettisoning the opposite pylon if handling is compromised.

---

### 1.3 Cockpit Armament Panel — Complete Description

**Panel location:** The armament panel is located on the **right console/subpanel area**, below and to the right of the instrument cluster, forward of the right sidewall circuit breaker panels. It is within easy reach of the pilot's right hand. In DCS, the panel is fully clickable — every switch can be actuated with the mouse cursor.

**Master Arm Switch:**
- **Location:** Upper left portion of the armament panel.
- **Positions:** SAFE (down/off) and ARM (up/on).
- **Safety guard:** The Master Arm switch has a spring-loaded guard that must be lifted before the switch can be moved to ARM. DCS models this guard — left-click lifts the guard, second click throws the switch.
- **Function:** Energizes the weapons firing circuit. No forward-firing weapons can fire without Master Arm in the ARM position. Door guns are independent of the Master Arm circuit.

> *⚠ Realism Divergence: Real aircraft used a safety wire on the Master Arm guard in peacetime. DCS does not require wire removal but does require two clicks (lift guard, then switch). If weapons will not fire, Master Arm in SAFE is the most common cause.*

**Weapon Select Switch:**
- **Location:** Center of the armament panel.
- **Positions (DCS-modeled):**
  - **SAFE** — no weapon selected; firing circuit open even with Master Arm in ARM.
  - **ROCKETS** — selects the rocket launchers (XM-158 or XM-159 on loaded pylons).
  - **GUNS** — selects the M134 minigun pod(s) if loaded.
  - **ROCKETS AND GUNS** — selects both weapons to fire simultaneously on trigger press.

**Firing Mode / Intervalometer:**
- **Location:** Lower section of armament panel.
- **Positions:**
  - **SINGLE** — one rocket fires per trigger pull.
  - **PAIRS** — one rocket from each loaded pylon fires per trigger pull (two rockets total).

> *⚠ Realism Divergence: The real system supports SINGLE, PAIRS, and ripple-fire rates. DCS models SINGLE and PAIRS. Holding the trigger with PAIRS selected continues firing in pairs at a fixed rate rather than as a true separate RIPPLE mode. Verify behavior in the current DCS version.*

**Jettison Panel:**
- **Location:** Separate from the main armament panel; on the center console area. In DCS, accessible via a dedicated cockpit switch.
- **Function:** Emergency jettison drops all stores from both pylons simultaneously.
- **Procedure:** Master Arm to SAFE → Jettison cover lifted → Jettison switch actuated → Verify pylons clear.

---

### 1.4 Pilot Weapons Controls on Cyclic

**Primary weapons fire trigger:**
- **Location:** Primary (first-stage) trigger on the cyclic grip, right index finger.
- **Function:** Fires the weapon selected on the armament panel.
- **DCS mapping:** `Space` (default keyboard); HOTAS trigger axis/button.

**Weapon safe from cyclic:** There is no quick-safe on the cyclic. The pilot must reach the armament panel to place Master Arm to SAFE. The fastest safe is to set the weapon selector to SAFE on the armament panel.

**Force trim and weapons fire interaction:** The DCS UH-1H force trim system (`T` — hold to release; `LCtrl + T` — set trim) does not inhibit weapons firing. Pilots should maintain trim during attack runs for attitude stability but do not need to release trim to fire.

---

### 1.5 DCS Keyboard / HOTAS Reference — Weapons Functions

| Function | Default Keybind | Cockpit Location | Notes |
|---|---|---|---|
| Master Arm ARM/SAFE | Mouse click only | Armament panel — upper left | Two-click: lift guard then switch |
| Weapon select: ROCKETS | Mouse click only | Armament panel — center | Rotate selector |
| Weapon select: GUNS | Mouse click only | Armament panel — center | Rotate selector |
| Weapon select: SAFE | Mouse click only | Armament panel — center | Rotate selector |
| Fire mode: SINGLE | Mouse click only | Armament panel — lower | Intervalometer |
| Fire mode: PAIRS | Mouse click only | Armament panel — lower | Intervalometer |
| Weapons fire (rockets/guns) | `Space` | Cyclic primary trigger | HOTAS: assign to trigger |
| Emergency jettison | Mouse click on jettison switch | Center console jettison panel | Lift cover, then switch |
| Switch to port door gun station | `F5` (or crew keybind) | View/seat menu | Verify in DCS input settings |
| Switch to starboard door gun station | `F6` (or crew keybind) | View/seat menu | Verify in DCS input settings |
| Door gun fire (crew station) | `Space` (while in crew station) | Crew station trigger | Standard fire trigger |

> *Note: DCS default crew station keybinds vary by input profile version. `F1`–`F6` typically map to crew positions in multi-crew aircraft. Consolidated keybind table is in the Appendix.*

---

### 1.6 Pre-Engagement Arming Checklist (Weapons Hot)

Execute upon entering the engagement area or when cleared hot.

1. **Weapon selector** — set per mission (ROCKETS / GUNS / ROCKETS AND GUNS)
2. **Fire mode selector** — set per mission (SINGLE or PAIRS)
3. **Master Arm guard** — LIFT (left-click to raise guard)
4. **Master Arm switch** — ARM
5. **Armament panel** — scan; verify all settings correct
6. **Crew** — "Weapons hot, engaging [target description]"
7. **Sight** — position head on sight; verify reticle visible

---

### 1.7 Weapons Safe Sequence (Post-Engagement / Mission Abort)

1. **Trigger** — release
2. **Master Arm** — SAFE
3. **Master Arm guard** — lower
4. **Weapon selector** — SAFE
5. **Crew** — "Weapons safe"
6. **Jettison panel** — verify cover closed

---

### 1.8 Common Student Errors — Weapons Switchology

| Error | Correction |
|---|---|
| Master Arm left in ARM during transit | Safe weapons immediately after engagement; Master Arm SAFE is part of post-engagement checklist |
| Wrong weapon type selected | Verbalize weapon selector position during arming checklist before every run |
| Forgetting to lift Master Arm guard | Guard requires a separate click; will not move without guard raised |
| Wrong fire mode selected | Brief fire mode during arming checklist; verbalize the setting |
| Attempting to fire with Master Arm in SAFE | Reinforce: no firing circuit without Master Arm ARM |
| Emergency jettison without safing first | Correct sequence: Master Arm SAFE → jettison, to prevent inadvertent arming during event |
| Not briefing crew before weapons hot | Crew call "Weapons hot, engaging…" is mandatory before every attack |

---

## Module 2: Sight Systems & Target Acquisition

### 2.1 The AN/M2A1 Optical Sight — DCS UH-1H

**Sight type:** The DCS UH-1H models a fixed-depression **optical deflection/collimating sight** positioned in the upper center of the instrument panel, projecting a reticle onto or through a glass plate visible through the front windscreen. This is NOT a ballistic computing sight — it does not receive airspeed, altitude, or G-force inputs. The pilot manually selects the appropriate depression setting (if adjustable) and flies precise airspeed and altitude parameters to match the sight calibration.

> *⚠ Realism Divergence: The real UH-1H gunship used several sight configurations depending on the variant and modification period. The M73 sight (used on earlier gunships) and the M74/AN/M2A1-type deflection sight (later variants) differ in adjustment range and reticle design. DCS models a sight consistent with the AN/M2A1-type. The following description applies to the DCS implementation; differences from specific real-world TM values are noted.*

**Reticle design (DCS):**
- Central **aiming dot or cross** — the primary aim reference for forward-firing weapons.
- **Mil graduation marks** — radial or linear tick marks allowing the pilot to estimate target angular size, range, and lead angle.
- **Depression scale** — if present, indicates the current depression angle below the aircraft's longitudinal axis.
- The reticle is visible from the pilot's normal seated position when the head is positioned at the correct eye relief distance (roughly 25–30 cm from the sight glass). At incorrect eye relief, the reticle will appear blurred, cut off, or double.

**Sight mounting location:**
- The sight is mounted on a **pedestal above the instrument panel center**, angled toward the pilot's face. In the DCS cockpit, it is the optical device directly in front of the pilot on the upper instrument panel. It does not obstruct normal instrument scan when the pilot looks below the sight glass.

**Depression/elevation adjustment (DCS behavior):**
- In DCS, the sight depression setting is **adjusted via mouse wheel** on the depression knob of the sight pedestal, or via a clickable adjustment knob.
- Depression is measured in **mils** (thousandths of a radian). 1 mil = 0.057°.
- Standard depression settings for common attack airspeeds and ranges are derived from ballistic tables (see Module 3).
- **If the sight is not adjusted for the actual attack airspeed and range, rockets will impact short or long of the aim point.** This is the most common accuracy error.

**Lead angle computation:**
- The AN/M2A1-type sight does **NOT** automatically compute lead angle for aircraft motion. The pilot must manually offset the aim point for:
  - Aircraft groundspeed vector (the helicopter is moving forward while the rocket travels to the target).
  - Crosswind drift (the rocket drifts downwind after launch).
  - Target motion (for moving targets, the pilot must add forward lead).
- In practice, ballistic tables provide depression settings that account for the **forward throw** of the rocket relative to launch point for a specific airspeed and range. The tables assume still air and level terrain. Deviations require manual correction.

**Relationship between sight depression, airspeed, and range:**
- The rocket follows a curved ballistic path after launch. At a given airspeed and range, there is one correct depression angle that puts the bullet on the target.
- If the pilot is 10 KIAS faster than the table value, rockets will impact **long** (forward throw increases).
- If the pilot is 10 KIAS slow, rockets will impact **short**.
- Depression settings are provided in Module 3, Table 3.2.

**Instructor note:** Students initially underestimate the sensitivity of the sight to airspeed variation. A 15-knot speed error produces a lateral or range error of 30–60 meters at 1,000 m slant range. Airspeed discipline is not optional — it is a direct accuracy input.

---

### 2.2 Visual Target Acquisition Without Sensors

The UH-1H has no targeting sensors. Target acquisition is entirely by eye — pilot and crew scanning from the aircraft. The following techniques are drawn from TC 1-237 and FM 3-04.140.

**Horizon scanning technique:**
- At cruise altitude (500–1,500 ft AGL), scan left to right in 10° sectors along the forward hemisphere.
- Pause briefly in each sector — moving eyes do not resolve detail.
- Assign specific scan sectors by crew position: pilot scans the front 180°; port door gunner scans the left 90°–270°; starboard gunner scans the right 90°–270°.
- Look for movement first (vehicles, troops), then contrasting shapes (vehicle silhouettes against terrain, dust trails), then muzzle flash or smoke.

**Distance estimation — angular size method:**
Known target angular size at 1,000 m:
| Target | Approximate Width | Angular Size at 1,000 m |
|---|---|---|
| T-72 / T-80 main battle tank | 3.7 m | 3.7 mils |
| BMP-2 IFV | 3.0 m | 3.0 mils |
| Military truck (ZIL-131) | 2.3 m | 2.3 mils |
| Standing soldier | 0.5 m | 0.5 mils |

If a known target appears to subtend X mils in the sight, range = (known width in meters × 1,000) ÷ X mils.

**Target identification criteria (positive ID):**
Before any weapon employment, the crew must positively identify the target as hostile. Positive identification requires:
1. Visual confirmation of hostile indicator (weapons in use, hostile markings, direct observation of hostile act).
2. Confirmation that no friendly forces are within the engagement area (clearance from ground controller or flight lead).
3. Agreement between pilot and any available crew member that the target is hostile.
In DCS single-player, the F10 map can be used for target identification before engagement.

**Threat recognition in DCS — common target types:**

| Target | Visual Signature | Notes |
|---|---|---|
| Main battle tank (T-72) | Large tracked vehicle, long barrel, dusty track | High-value; M229 HE or multiple M151 runs |
| BMP / BTR IFV | Smaller tracked/wheeled, turret visible | Mobile; engage from standoff |
| Military truck | Boxy, 2-axle or 3-axle, often in convoy | Soft-skinned; single M151 or minigun pass |
| AAA (ZSU-23-4 Shilka) | Boxy turret, 4 barrels, radar dish | Extreme threat; engage before it fires |
| SAM (SA-9 Gaskin) | Launch vehicle with twin launch rails | Engage from max range; immediate threat |
| Troops in the open | Small shapes, clustered or moving in single file | M151 or minigun; area suppression |

**Acquisition from altitude vs. low level:**
- **High altitude (500–1,500 ft AGL):** Greater acquisition range; longer target identification time; increased AAA/small arms threat exposure if within range; better overall situational awareness.
- **Low altitude (< 200 ft AGL, nap-of-earth):** Reduced radar/visual detection by ground threat; shorter acquisition window for pilot; terrain masking limits sight lines. Use low altitude for approach to the target area; pop up to acquisition altitude for attack.

**Scanning while flying:** The pilot cannot maintain a sustained head-down sight scan while also monitoring aircraft instruments. Use the following cycle: 3–5 seconds instrument scan → 10–15 seconds external scan → 3–5 seconds instrument cross-check → external scan. Never maintain external scan for more than 20 seconds without an instrument check at low altitude.

---

### 2.3 Coordination with Door Gunners for Target Designation

**Door gunner target call format:**
> *"[Pilot callsign], [position] — [o'clock direction], [distance], [target description], [additional remarks]."*

Example: *"Pilot, right door — 3 o'clock, 800 meters, truck convoy, north side of road, moving east."*

**Full call components:**
1. Who is calling (crew position).
2. Target bearing: o'clock direction relative to the aircraft nose (12 o'clock = directly ahead).
3. Distance: in meters or nautical miles.
4. Target description: vehicle type, number, activity.
5. Additional remarks: direction of movement, terrain reference, threat indicators.

**Pilot acknowledgment:** *"Roger, 3 o'clock, copy truck convoy."* If pilot cannot acquire: *"No joy, talk me on."* Gunner then provides additional steering cues: *"Right 2 degrees, target behind the tree line."*

**Pilot target pickup:** Once the pilot acquires the target visually, call: *"Tally."* If the target is lost during maneuvering: *"Lost visual."* The gunner resumes talking-on.

---

### 2.4 WP Marking Rockets for Target Identification

**M156 WP employment as a target marker:**
- The M156 fires a standard 2.75-inch rocket motor; on impact, white phosphorus burns and produces dense white smoke, typically 1–3 meters above the ground impact point.
- WP burn time: approximately 60 seconds; visible in both day and night conditions.
- WP smoke drift: white phosphorus smoke drifts with surface wind. Account for wind direction when assessing mark-to-target offset.

**Call format for WP marking in CCA:**
- Before firing: *"Smoke out."*
- After impact: *"Mark is burning."*
- If controller cannot see mark: *"Smoke, [color — always white for WP], [direction from target]."*
- Correction: *"Smoke is [X] meters [direction] of target."* Adjust aim point accordingly.

**Spotting WP impact and adjusting:**
- Estimate distance from mark to desired impact point in meters.
- Adjust aim point by the appropriate angular offset using mils (at 1,000 m, 1 mil = 1 m of offset).
- Re-attack with adjusted depression/aim point.

**Instructor note:** WP rockets are a "marking and adjusting" tool, not a precision first-round-on-target weapon. Brief students to plan a WP marking pass before the main attack when targets are obscured or uncertain. Two rockets are standard for a marking pass: one to find the target area, the second to confirm or bracket.

---

### 2.5 Danger Close Ranges

**Definition:** Danger close is the distance within which friendly forces may be affected by weapons effects — fragmentation, blast, burning particles (WP), or ricochet. Below danger close distance, the ground commander must positively accept risk and explicitly authorize engagement.

**Danger close distances by weapon (from FM 3-04.140 and ATP 3-04.1):**

| Weapon | Danger Close Distance | Notes |
|---|---|---|
| 2.75-inch FFAR M151 HE | 230 meters | From friendly forces to intended point of impact |
| 2.75-inch FFAR M229 HE | 230 meters | Same as M151; larger warhead, same declared danger close |
| M156 WP | 300 meters | WP fragments and burning particles can travel further than blast |
| M134 Minigun (7.62mm) | 200 meters | Ricochet and fragmentation; line of fire discipline required |
| M60D Door Gun (7.62mm) | 200 meters | Same as M134 |

> *⚠ Realism Divergence: DCS does not model fragmentation splash zones or ricochet effects on allied AI units. Danger close in DCS is an academic and ROE-compliance discipline, not a simulated physical effect. Instructors must enforce danger close as a procedural standard regardless of DCS AI behavior.*

**Procedure when within danger close:**
1. Ground commander explicitly states: *"Cleared hot, danger close."*
2. Pilot reads back the danger close clearance before firing.
3. Attack direction is briefed so ground forces know to take cover.
4. After engagement: assess BDA and check for friendly casualty report from ground element.

---

### 2.6 Common Student Errors — Sight Systems & Target Acquisition

| Error | Correction |
|---|---|
| Head position incorrect — reticle not visible or blurred | Set correct eye relief at the sight; adjust seat position before entering target area |
| Sight depression not adjusted for attack airspeed | Set depression based on ballistic table before each attack profile; verify airspeed at roll-in |
| Scanning too fast — not dwelling in sectors | Enforce 1–2 second dwell per sector; movement detection requires brief stationary focus |
| Positive ID not confirmed before firing | Stop-fire drill: if crew cannot confirm target ID, abort the run |
| Door gunner call not acknowledged before engagement | Pilot must call "Tally" or "No joy" after every gunner target call |
| WP mark fired without announcing "Smoke out" | Enforce radio discipline; all crew must know when marking rounds are outbound |
| Engagement inside danger close without explicit clearance | Drill danger close procedure; require verbal readback before firing |

---


## Module 3: 2.75-Inch FFAR Rocket Employment

### 3.1 Rocket System Description

The **2.75-inch Folding Fin Aerial Rocket (FFAR)**, known in U.S. Army service as the **Mk 40** motor series (with variants), is an unguided aerial rocket optimized for helicopter delivery. The 2.75-inch diameter references the motor tube diameter. After ejection from the launcher tube, four **folding fins** spring open from the motor base, stabilizing the rocket in flight.

**Motor performance (2.75-inch Mk 40 / Mk 66 series, from TM 9-1340-222-10):**
- Motor ignition: electrical signal from cyclic trigger through armament panel firing circuit.
- Burnout time: approximately **1.1 seconds** after launch (Mk 40 motor); 0.8 seconds for Mk 66 (later motor).
- Velocity at burnout: ~600–700 m/s (Mk 40 series).
- Time of flight to 500 m: ~0.8 seconds.
- Time of flight to 1,000 m: ~1.5 seconds.
- Time of flight to 2,000 m: ~3.5 seconds.
- Maximum range: ~8,000 m (motor burnout + coast to impact).
- **Maximum effective range for point targets (with M151/M229 HE):** 1,500–2,000 m from a diving attack profile.
- **Practical employment range (routine training):** 500–1,500 m slant range.

> *⚠ Realism Divergence: DCS models rocket flight physics including ballistic arc and approximate time of flight. Specific motor burnout timing and terminal ballistics (fragmentation radius) are approximated. For training purposes, use DCS observation of impact point as ground truth and correlate to ballistic table values below.*

**XM-158 (7-tube) launcher:**
- Seven tubes arranged in a circular pattern (one center, six surrounding).
- Mounting: left or right pylon hardpoint.
- Ripple fire sequence: tubes fire in a pre-set sequence (typically from outer tubes inward) to minimize blast interference.
- Weight: ~40 kg loaded with 7 × M151 HE rockets.
- Use: close-in fire support, single-pass with limited capacity; preferred when ammunition conservation is required or weight is a factor.

**XM-159 (19-tube) launcher:**
- Nineteen tubes in a hexagonal close-packed arrangement.
- Mounting: left or right pylon hardpoint.
- Ripple fire sequence: pre-set sequential firing.
- Weight: ~95 kg loaded with 19 × M151 HE rockets.
- Use: area suppression; LZ preparation; sustained fire support missions. Higher weight cost — plan for density altitude impact.

---

### 3.2 Available Warheads — Full Data Table

| Warhead | Designation | HE Fill | Burst Radius (lethal) | Burst Radius (casualty) | DCS Modeled | Best Targets |
|---|---|---|---|---|---|---|
| HE (10 lb) | M151 | Comp B, ~6.2 lb | ~10 m | ~25 m | Yes | Personnel, light vehicles, open equipment |
| HE (17 lb) | M229 | Comp B, ~10 lb | ~15 m | ~35 m | Yes | Light vehicles, structures, hardened positions |
| White Phosphorus | M156 | WP, ~6 lb | N/A (burn radius ~3 m) | — | Yes | Target marking, obscurant, incendiary effect on soft targets |
| Illumination | M257 | 1× M671 flare unit | N/A | — | Yes | Night illumination; parachute-deployed; burns ~100 sec |
| Flechette (APERS) | M255 series | ~2,200 darts | 40 m wide × 250 m long | — | No (academic) | Anti-personnel area; not in DCS |

> *Sources: TM 9-1340-222-10; FM 3-04.140, Appendix B. DCS modeled burst effects are approximate; the M151 and M229 produce visible explosions with fragment effects on DCS ground units. The M257 illumination deploys a parachute flare visible at night.*

**M257 Illumination employment altitude:** For optimum ground illumination coverage, the M257 should be fired at a range and altitude that produces flare ignition at **800–1,200 ft AGL** above the target. The flare burns approximately **100 seconds** and descends slowly under the parachute. Fire the round so it arcs and ignites near the top of the ballistic arc — this requires a near-vertical or steep-angle shot, or firing from level flight at reduced airspeed with a high-elevation aim point. (See Module 9.)

---

### 3.3 Ballistics Data Table

The following table provides depression angle settings for the AN/M2A1 sight at standard attack airspeeds and dive angles. Values are derived from TM 55-1520-210-10, Appendix F, cross-referenced with FM 3-04.140, Table B-3 (2.75-inch FFAR, M151 HE, Mk 40 motor, standard atmosphere, sea level, no wind).

**Depression is measured in mils below the aircraft longitudinal axis (horizontal). Set the sight depression knob to the listed value before commencing the attack run.**

#### Table 3.3-A: Depression Settings — Level / Running Fire (0° dive)

| Attack Airspeed (KIAS) | Slant Range (m) | Depression Setting (mils) | TOF (sec) | Notes |
|---|---|---|---|---|
| 60 KIAS | 500 | 32 | 0.8 | Short range; accuracy adequate for area targets |
| 60 KIAS | 800 | 38 | 1.3 | — |
| 60 KIAS | 1,000 | 44 | 1.6 | — |
| 80 KIAS | 500 | 28 | 0.8 | — |
| 80 KIAS | 800 | 35 | 1.3 | Standard running fire parameter |
| 80 KIAS | 1,000 | 41 | 1.6 | — |
| 100 KIAS | 800 | 32 | 1.3 | — |
| 100 KIAS | 1,200 | 40 | 2.0 | — |

#### Table 3.3-B: Depression Settings — Diving Attack (10° dive angle)

| Attack Airspeed (KIAS) | Slant Range (m) | Depression Setting (mils) | TOF (sec) | Min Release Alt (ft AGL) |
|---|---|---|---|---|
| 80 KIAS | 600 | 20 | 1.0 | 200 |
| 80 KIAS | 800 | 26 | 1.3 | 250 |
| 80 KIAS | 1,000 | 32 | 1.6 | 300 |
| 100 KIAS | 800 | 22 | 1.3 | 250 |
| 100 KIAS | 1,000 | 28 | 1.6 | 300 |
| 100 KIAS | 1,200 | 34 | 2.0 | 400 |

#### Table 3.3-C: Depression Settings — Diving Attack (20° dive angle)

| Attack Airspeed (KIAS) | Slant Range (m) | Depression Setting (mils) | TOF (sec) | Min Release Alt (ft AGL) |
|---|---|---|---|---|
| 80 KIAS | 600 | 12 | 1.0 | 300 |
| 80 KIAS | 800 | 18 | 1.3 | 400 |
| 80 KIAS | 1,000 | 24 | 1.6 | 500 |
| 100 KIAS | 800 | 14 | 1.3 | 400 |
| 100 KIAS | 1,000 | 20 | 1.6 | 500 |
| 100 KIAS | 1,200 | 26 | 2.0 | 600 |

> *Note: These values are derived from published TM data. DCS may vary slightly from real-world ballistics. During initial training, conduct a ranging pass (observe impact point, note error, adjust depression) before committing to precision engagement. Wind and density altitude corrections follow.*

**Wind correction:**
- Headwind: rockets travel faster than in still air; impact will be slightly long. Increase depression by 1–2 mils per 10-knot headwind component.
- Tailwind: opposite; decrease depression by 1–2 mils per 10-knot tailwind component.
- Crosswind: aim point shifts downwind; offset aim point upwind by approximately 1 mil per 5 knots of crosswind at 1,000 m range.
- In DCS, wind effects on rockets are modeled; verify in mission briefing wind layer before setting depression.

**Density altitude correction:**
- At high DA (> 3,000 ft DA), rocket motors produce slightly less thrust; impact will be marginally short. In practice, the correction is small (< 5 mils) for altitudes below 8,000 ft DA and is generally not applied in DCS training. Monitor and adjust empirically.

---

### 3.4 Employment Profiles

#### 3.4.1 Diving Attack (Primary Accurate Profile)

The diving attack is the most accurate rocket delivery profile. The aircraft descends toward the target at a controlled dive angle, fires at a specified slant range, and executes a pull-off recovery.

**Parameters:**
- Dive angle: 10–20° (10° is standard; 20° is used for increased accuracy and steeper terrain)
- Attack airspeed: 80–100 KIAS at release
- Release slant range: 600–1,200 m (see ballistic table)
- Minimum release altitude: 300 ft AGL (10° dive, 80 KIAS); 500 ft AGL (20° dive, 100 KIAS)
- Minimum recovery altitude: 200 ft AGL after pull-off

**Step-by-step procedure:**
1. Enter orbit at 800–1,500 ft AGL; identify target.
2. Set sight depression per ballistic table for planned airspeed and range.
3. Master Arm ARM; weapon selector ROCKETS; fire mode per plan.
4. Roll in to attack heading; establish 10–20° nose-low dive.
5. Accelerate to 80–100 KIAS; maintain dive angle.
6. Align sight reticle on target; wait for slant range to reach fire point.
7. Fire trigger; fire number of rounds per plan (SINGLE or PAIRS).
8. Immediately after last round: break off (left or right, 2–3 G pull); climb to recovery altitude.
9. Evaluate impact; re-attack or disengage.

**Pull-off procedure:**
- Apply 2–3 G cyclic pull; simultaneously apply right pedal (to counteract torque during climb-out).
- Turn to a predetermined safe direction (not over own troops; not into rising terrain).
- Climb to orbit altitude before commencing re-attack.
- Minimum altitude before executing the break: 300 ft AGL (10° dive). Do NOT delay the break.

#### 3.4.2 Running / Level Fire

Level or very shallow (<5°) attack. Lower accuracy; used for area suppression when dive angle is not feasible (low ceiling, terrain).

**Parameters:**
- Altitude: 50–300 ft AGL
- Airspeed: 60–100 KIAS
- Range: 400–1,000 m
- Depression: per Table 3.3-A

**Step-by-step procedure:**
1. Approach target in low-level flight; maintain 60–100 KIAS.
2. Set sight depression for level fire at planned airspeed.
3. Master Arm ARM; weapon selector ROCKETS.
4. At planned range, align sight on target and fire.
5. Continue forward flight; pull off after passing target's bearing (do not overfly target directly at low altitude).
6. Turn to re-attack heading; climb if ceiling allows.

> *Instructor note: Running fire is a suppression tool, not a precision weapon. Brief students that accuracy from level flight at 100 ft AGL is significantly worse than a 10° dive from 800 ft AGL. Use running fire for area targets (road intersection, tree line) and diving attack for point targets (vehicle, bunker).*

#### 3.4.3 Circling / Wagon Wheel (Orbiting Fire)

The **wagon wheel** (or orbiting attack) is the primary sustained-fire attack pattern for the UH-1H. The aircraft orbits the target at a constant range and altitude; during each inbound arc, the pilot fires rockets or guns; the aircraft completes the orbit and re-attacks.

**Parameters:**
- Orbit radius: 400–800 m from target
- Orbit altitude: 500–1,200 ft AGL
- Orbit airspeed: 60–80 KIAS
- Dive angle during attack arc: 10–15° toward target as pilot turns inbound
- Roll-in: at a bearing ~90–120° before the planned attack heading (begin turning inbound)

**Step-by-step procedure:**
1. Establish a left- or right-hand orbit at planned radius and altitude.
2. Identify the target; assign it a clock position reference (e.g., "target at 12 o'clock in the orbit").
3. At 90–120° prior to the attack heading, begin roll-in: lower the nose 10–15°, accelerate to 80 KIAS.
4. Track sight reticle to target; fire at planned range.
5. After firing: pull off; continue orbit; climb back to orbit altitude.
6. Next pass: repeat. Multiple passes provide sustained fire.

**Door gunner coordination during wagon wheel:**
- Right-hand orbit: during the inbound arc the target is on the pilot's right; the starboard door gunner has the target.
- Pilot call: *"Target right, engaging."*
- Starboard gunner fires simultaneously or in sequence per crew coordination plan.
- Left-hand orbit: opposite — port gunner has the target.

Full wagon wheel doctrine is covered in Module 6.

#### 3.4.4 Hover Fire

Firing rockets from a stationary hover. Highest accuracy; highest crew exposure risk.

**Parameters:**
- Altitude: 10–50 ft AGL (low hover for stability)
- Airspeed: 0 KIAS (stationary); minor wind drift correction applied
- Range: typically 200–600 m
- Depression: low depression (< 20 mils) at short ranges; aim point essentially direct

**Step-by-step procedure:**
1. Establish a stable hover; confirm pedal and cyclic control before firing.
2. Set sight depression for hover fire (very low depression at close range).
3. Master Arm ARM.
4. Align nose toward target; stabilize attitude.
5. Fire; assess impact; fire corrective rounds.
6. After engagement: break left or right; gain airspeed immediately to reduce exposure.

> *Instructor note: Hover fire is used when terrain prevents a diving approach and there is no alternative. The aircraft is stationary — it is the easiest target on the battlefield. Limit hover fire to 5–10 seconds of total exposure. Pre-brief an escape route before entering hover.*

---

### 3.5 Attack Run Parameters — Master Table

| Profile | Entry Alt (ft AGL) | Entry Airspeed (KIAS) | Dive Angle | Release Range (m) | Release Alt (ft AGL) | Pull-off Alt (ft AGL) | Recovery Airspeed (KIAS) |
|---|---|---|---|---|---|---|---|
| Level / Running | 50–300 | 60–100 | 0–5° | 400–1,000 | Same as entry | N/A — continue forward | 60–100 |
| Diving (10°) | 800–1,500 | 80–100 | 10° | 600–1,200 | 300+ | 200 min | 60–80 |
| Diving (20°) | 1,000–1,500 | 80–100 | 20° | 600–1,000 | 500+ | 300 min | 60–80 |
| Wagon Wheel | 500–1,200 | 60–80 (orbit); 80 (attack arc) | 10–15° (attack arc) | 600–1,000 | 300+ | Return to orbit | 60–80 |
| Hover | 10–50 | 0 | 0° | 200–600 | Same (hover) | Immediate breakout | 60+ |

---

### 3.6 Salvo vs. Single-Round Employment

| Mode | Rounds per Trigger Pull | Use |
|---|---|---|
| SINGLE | 1 | Precision engagement; specific point target; ammunition conservation |
| PAIRS | 2 (one per pylon) | Increased probability of hit on area/point target; moderate expenditure |
| Full pod (sustained PAIRS hold) | All remaining | Maximum area suppression; LZ prep; high ammo expenditure |

**Ammunition allocation guidance (per target type):**

| Target Type | Recommended Allocation |
|---|---|
| Light vehicle (truck, UAZ) | 2–4 × M151 HE; or 1–2 × M229 HE |
| Armored vehicle (BMP, BTR) | 6–8 × M229 HE; or multiple passes |
| Personnel in the open | 4–6 × M151 HE area burst |
| Bunker / emplacement | 4–6 × M229 HE; direct or near-direct hit required |
| LZ suppression (50×50 m area) | 8–12 rockets; walking fire across area |
| Main battle tank (T-72) | Not recommended with M151/M229 without massed fire; 12+ M229 for mobility kill |

---

### 3.7 Ripple Fire / Walking Fire Technique

"Walking fire" is the technique of firing multiple rockets in quick succession, adjusting aim slightly between rounds to walk the impact point across a target complex (e.g., a vehicle convoy along a road).

**Procedure:**
1. Set fire mode to PAIRS.
2. On first trigger pull: observe impact of first pair; note error (long/short/left/right).
3. Apply correction: raise or lower sight depression; adjust left/right aim by banking slightly.
4. Fire next pair; continue until target complex is covered.
5. Burst timing: 0.5–1.5 seconds between trigger actuations allows first pair to impact before next is fired, enabling adjustment.

**Instructor note:** Walking fire requires trigger discipline. Students tend to hold the trigger and fire continuously without adjustment. Enforce the "observe — adjust — fire" cycle from the first training pass.

---

### 3.8 Common Student Errors — Rocket Employment

| Error | Correction |
|---|---|
| Incorrect depression setting (most common) | Verbalize depression setting during arming checklist; verify against ballistic table before roll-in |
| Airspeed not stabilized at release | At roll-in, announce airspeed and hold it; 10 KIAS variation = 30–60 m range error at 1,000 m |
| Late trigger press (too close) | Brief minimum release range; use a cockpit timer or landmark to mark the fire point |
| No pull-off after firing | Reinforce: break-off is mandatory; do not continue into low altitude without pulling off |
| Firing past minimum release altitude | Add a hard altitude floor callout: "Breaking off at 400 ft" — call it on every pass |
| Not correcting for wind | Brief wind before every attack; adjust aim point at roll-in; walk first round before committing |
| Over-expending on first target | Assign per-target ammunition budget; enforce conservation during training |
| Firing at hovering MBT from single pass | Brief correct target allocation; MBTs require massed or sustained fire, not single-pass shots |

---

## Module 4: M134 Minigun Pod Employment

### 4.1 System Overview

The **M134 Minigun** is a 7.62×51mm NATO, six-barrel, electrically driven rotary machine gun. In the DCS UH-1H, it is available as a **pylon-mounted forward-firing pod** on the left and/or right pylon. The M134 is not crew-aimed — it is fixed to the pylon, parallel to the aircraft's longitudinal axis, and aimed entirely by the pilot using the same optical sight used for rockets.

**Specifications (TM 9-1005-224-10):**
- Caliber: 7.62×51mm NATO
- Barrel configuration: 6 barrels, rotating electrically via a drive motor
- Rate of fire: **2,000 RPM** (low) or **4,000 RPM** (high) — rate is selectable in DCS via an armament panel switch if modeled; default in many DCS configurations is a fixed 2,000 RPM per trigger hold
- Ammunition: M80 ball, M62 tracer, or mixed belts (standard military mix: 4 ball : 1 tracer)
- **Ammunition capacity per pod (DCS loadout):** ~1,500 rounds per pod (varies by DCS loadout configuration; some loadouts offer up to 3,000 rounds per pod)
- Weight loaded (1,500 rounds): approximately 115 kg (253 lb) per pod

> *⚠ Realism Divergence: The real M134 is usually rate-selectable at 2,000 or 4,000 RPM via a selector on the installation. DCS UH-1H models the M134 firing behavior, but the rate selector may not be fully interactive in all DCS versions. Check current module version. For training purposes, assume 2,000 RPM as the standard rate.*

**Pod mounting:** Left pylon, right pylon, or both. The pod is fixed — it cannot slew. The barrel cluster points forward, parallel to the rotor mast. All aiming is done by pointing the aircraft.

**Tracer-to-ball ratio:** Standard U.S. military 7.62mm linked belts load one M62 tracer for every four M80 ball rounds (4:1 ball-to-tracer). In DCS, tracers are visible and are the primary aiming feedback tool.

---

### 4.2 Sight Use for the M134

The M134's trajectory is much flatter and shorter-range than 2.75-inch rockets. At the engagement ranges used for minigun employment (200–800 m), the bullet drop is minimal.

**Depression settings for M134 (approximate, 2,000 RPM, 7.62mm M80 ball):**

| Attack Airspeed (KIAS) | Engagement Range (m) | Depression Setting (mils) | Notes |
|---|---|---|---|
| 60 KIAS | 200 | 5 | Very close range; hover fire or running fire |
| 60 KIAS | 400 | 8 | — |
| 60 KIAS | 600 | 12 | Standard running fire range |
| 80 KIAS | 400 | 7 | — |
| 80 KIAS | 600 | 10 | Standard diving fire range |
| 80 KIAS | 800 | 14 | Near-maximum effective range |
| 100 KIAS | 600 | 8 | — |
| 100 KIAS | 800 | 12 | — |

> *Note: Minigun depression settings are significantly lower than rocket settings at equivalent range because the bullet velocity (~850 m/s at muzzle) is much greater than the rocket, minimizing drop. In practice, at ranges under 600 m, many pilots use direct aim (minimal depression) and walk tracers onto target.*

**Lead angle for forward motion:**
At 80 KIAS (41 m/s) and 600 m range, TOF is ~0.7 sec; the aircraft moves ~29 m forward during TOF. This creates a forward bias in impact — the rounds impact approximately 29 m ahead of the aim point at time of fire (at 600 m range, 80 KIAS). In practice, the pilot aims at the target and the forward motion of the aircraft mostly compensates for bullet TOF. For close-range (< 400 m), aim at the leading edge of the target.

---

### 4.3 Aiming Technique — Walking Tracers

The **tracer walk** technique is the primary minigun aiming method when the impact point is not immediately on target.

**Procedure:**
1. Before firing, align the sight approximately on or just short of the target.
2. Fire a short burst (0.5–1.0 second).
3. Observe tracer stream — identify where it impacts (short, left, right, long).
4. Adjust aim:
   - Short: raise nose slightly or increase depression.
   - Long: lower nose slightly.
   - Left: bank slightly left (moves tracer stream right relative to ground).
   - Right: bank slightly right.
5. Continue firing while adjusting — the tracer stream "walks" to the target.
6. Once on target, maintain aim and continue firing for target effect (3–5 second burst).

**Self-commentary during training (callouts):**
- *"Short, short"* — rounds impacting short; raising nose.
- *"On target"* — rounds on target; maintaining.
- *"Right — correcting"* — rounds right of target; banking left.

These callouts discipline the student to observe before adjusting and prevent the instinct to spray without feedback.

---

### 4.4 Employment Profiles

#### Diving Fire
- Dive angle: 5–15°
- Airspeed: 60–100 KIAS
- Engagement range: 300–800 m
- Procedure: same as rocket diving attack (Module 3.4.1) but lower depression settings; shorter engagement range.

#### Running / Level Fire
- Level flight at 50–300 ft AGL; 60–100 KIAS
- Engagement range: 200–600 m
- Technique: approach low-level; align nose on target; fire burst; continue forward; break off.
- Use: strafing along a tree line, road, or trench.

#### Circling Fire (Wagon Wheel)
- As part of the wagon wheel orbit (Module 6)
- During the inbound arc, the pilot aligns the nose toward the target and fires
- The narrower engagement window of minigun vs. rockets means shorter burst duration per pass — discipline trigger to fire only while aim is valid

#### Hover Fire
- Stationary hover; 10–50 ft AGL
- Engagement range: 100–300 m
- Highest accuracy; highest exposure
- Limit exposure to < 10 seconds; pre-plan escape heading

---

### 4.5 Recoil Effects and Compensation

**Recoil force:** The M134 firing 2,000 RPM generates a significant forward-directed reactive force on the pylon (recoil is directed aft of the pod, pushing the aircraft forward). The net effect is a slight nose-down and forward pitching tendency during sustained fire.

**Asymmetric fire (one pod only):**
- Firing the left M134 only creates a rightward yaw tendency (torque from recoil and slipstream).
- Firing the right M134 only creates a leftward yaw tendency.
- Correction: apply opposite pedal to maintain heading during single-pod fire.
- In DCS, asymmetric recoil effects are modeled — students will feel the aircraft weathervane if they do not apply pedal correction.

**Compensation during fire:**
- Apply slight aft cyclic to prevent nose drop during a sustained burst.
- Apply pedal as needed for yaw control (especially on single-pod fire).
- After fire stops, re-trim — the trim reference will have shifted during firing.

---

### 4.6 Ammunition Management

| Rounds Remaining | Minutes at 2,000 RPM | Bursts Remaining (3-sec burst) |
|---|---|---|
| 1,500 (full pod) | 0.75 min (45 sec total) | ~15 bursts |
| 1,000 | 0.50 min (30 sec) | ~10 bursts |
| 500 | 0.25 min (15 sec) | ~5 bursts |

> *Note: There is no round-counter visible in the DCS UH-1H cockpit. Pilots must mentally track elapsed trigger time to estimate rounds remaining. Pre-brief the maximum fire time per engagement (e.g., "3-second bursts; limit 10 passes per pod").*

**Conservation discipline:**
- Use 3-second bursts on point targets; walk tracers before committing.
- Reserve 15–20% of ammunition for self-defense or unexpected targets.
- Do not fire suppressive bursts against targets not yet positively identified.

---

### 4.7 M134 vs. Door Gun Tradeoffs

| Factor | M134 Minigun Pod | M60D Door Gun |
|---|---|---|
| Rate of fire | 2,000–4,000 RPM | ~550 RPM |
| Pilot-aimed | Yes | No (crew-aimed) |
| Coverage arc | Forward only (fixed to pylon) | ~120° horizontal arc per side |
| Range (effective) | Up to 800 m | 200–500 m practical |
| Ammunition | 1,500+ rounds (stored in pod) | 200–400 rounds per gun |
| Pylon weight | Heavy (~115 kg loaded) | Door mount (minimal weight) |
| Best use | Sustained forward-firing suppression; column attack | Flank/rear coverage; close-in protection; escorting troops |
| Limitation | No side or rear coverage; no flexibility | Low rate of fire; requires crew discipline |

**Mission selection guidance:**
- If primary mission is forward fire support (attack runs, LZ prep): carry M134 + rockets (mixed loadout) or dual M134.
- If primary mission is troop escort (convoy, LZ security): carry rockets or light rockets + M60D door guns only; M60Ds provide critical flank protection.
- If expecting SAM/AAA threat: prioritize performance; minimize pylon weight; use light loadout.

---

### 4.8 Common Student Errors — M134 Minigun

| Error | Correction |
|---|---|
| Firing without observing tracer impact first | Enforce 0.5-sec "probe burst" on first trigger pull; observe; then adjust |
| Sustained trigger hold without adjustment | Drill burst discipline: 3 seconds maximum per burst; observe between bursts |
| Not correcting for asymmetric recoil | Brief pedal correction; grade on heading control during single-pod fire |
| Attempting M134 at ranges > 800 m | Brief maximum effective range; M134 is a short-range weapon; rockets for > 800 m |
| Failing to set sight depression for minigun (using rocket setting) | Separate arming checklists for rocket and minigun profiles; verify selector and depression before each profile |
| Depleting ammunition without tracking | Pre-brief fire time budget; require verbal "ammo count" call every other pass |

---

## Module 5: M60D Door Gun Employment (Crew Stations)

### 5.1 System Overview

The **M60D** is the aircraft-modified variant of the M60 general-purpose machine gun, adapted for helicopter door mounting. It uses a **pintle/swivel mount** installed in the port (left) and starboard (right) cabin doorways of the UH-1H, allowing the gunner to traverse the weapon through a broad arc without repositioning.

**Specifications (TM 9-1005-298-14&P):**
- Caliber: 7.62×51mm NATO
- Operating principle: gas-operated, air-cooled, belt-fed
- Rate of fire: ~550 RPM cyclic; practical rate of fire: 200 RPM sustained (barrel heating limits)
- Barrel length: 560 mm (22 in) — aircraft version
- Feed: disintegrating metal link belt
- Standard ammunition load per gun (DCS): 200–400 rounds per gun (belt box mounted to the gun or pintle mount)
- Weight (weapon only): ~8.5 kg (18.8 lb)
- Effective range: 200–500 m practical; 1,100 m maximum range of projectile

**Modifications for aircraft use (M60D vs. ground M60):**
- Spade grip handles (A-shape pistol grips) replace the stock — the gunner fires with both thumbs on the spade triggers.
- Charging handle relocated for accessibility in the door position.
- No bipod or tripod — the pintle mount replaces the ground mount.

---

### 5.2 Door Mount — Traverse and Elevation Limits

| Parameter | Port Gun (left door) | Starboard Gun (right door) |
|---|---|---|
| Azimuth traverse | ~90° forward to ~180° aft (relative to aircraft nose) | ~90° forward to ~180° aft (mirror image) |
| Elevation up | ~+30° above horizontal | ~+30° above horizontal |
| Depression down | ~–50° below horizontal | ~–50° below horizontal |
| Hard stops | Forward stop prevents gun from sweeping through cockpit; aft stop prevents strike on tail rotor arc | Same |

> *⚠ Realism Divergence: DCS models the door gun traverse arc but the azimuth limits may not exactly replicate the real aircraft's mechanical stops. Do not attempt to fire the door gun forward of the cockpit — in the real aircraft, the forward hard stop prevents this. In DCS, respect the real-world limitation as a procedural rule regardless of simulation behavior.*

**Critical safety note — tail rotor arc:** The aft traverse stop on both door guns must prevent the barrel from swinging into the tail rotor arc. In the real aircraft, this is a physical mechanical stop. In DCS single-player, the student operating the door gun must be briefed never to point the gun aft past the cabin bulkhead. **Firing into the tail rotor arc will destroy the aircraft.**

---

### 5.3 DCS Crew Station Operation

**Switching to door gun positions:**
DCS UH-1H supports multiple crew positions accessible to the player. In single-player, the player can switch from the pilot seat to either door gun position to demonstrate door gun operation. In multiplayer, each crew position is occupied by a separate player.

- **Pilot seat:** Default crew position; F1 or 1 (depending on DCS version).
- **Port (left) door gun:** Access via F5 or by selecting crew position 5. Verify in current DCS UH-1H input settings.
- **Starboard (right) door gun:** Access via F6 or by selecting crew position 6. Verify in current DCS UH-1H input settings.

> *Note: Crew position keybinds have changed between DCS versions. Before the first training event, verify the correct keybinds by accessing Options → Controls → UH-1H in DCS. The Appendix contains the current default table.*

**View from door gun positions:**
- The player's view is placed at the gunner's position in the doorway; the gun is visible in the lower portion of the view.
- The gun traverses with mouse movement (or joystick slew) — the cursor moves the weapon.
- Elevation and azimuth are controlled by mouse look; the gun follows the view direction within the traverse limits.
- Trigger: Space or HOTAS trigger button while in the crew station.

**DCS limitations vs. real-world:**
- DCS does not model barrel overheating or mandatory barrel changes for the M60D.
- DCS does not model reloading — when ammunition is expended, the gun is inoperative.
- DCS does not model stoppages in standard training mode; mission editor failures can simulate stoppages for advanced training.
- The DCS gunner view does not include a formal sight — aiming is by line-of-sight through the gun barrel with tracers for feedback.

---

### 5.4 Gunner Technique

**Leading a moving target:**
- A ground vehicle moving perpendicular to the line of fire at 40 km/h (25 mph) requires approximately **2–4 vehicle-lengths of forward lead** at 400 m engagement range.
- Formula: Lead = (Target speed [m/s]) × (Time of flight [sec]).
  - At 400 m, 7.62mm TOF ≈ 0.5 sec; vehicle at 40 km/h = 11 m/s; lead = 11 × 0.5 = 5.5 m ≈ 1 vehicle length.
- For shorter ranges (< 200 m), lead reduction is minor; aim at the cab of the vehicle.

**Walking tracers onto a moving target:**
1. Aim behind the target (or at its current position).
2. Fire a short burst; observe tracer stream.
3. If short or trailing: walk forward (toward direction of target movement).
4. If ahead: walk back slightly; let the target drive into the stream.
5. Once on target: maintain aim; continue firing in 5–7 round bursts.

**Burst discipline:**
- Point target (vehicle, position): 5–7 round bursts; observe; correct; fire again.
- Area suppression (tree line, open area): up to 20-round burst; observe effects; continue.
- Avoid sustained trigger hold > 3–5 seconds without an observation pause. Prevents ammunition waste and allows target effect assessment.

**Sector discipline:**
Each gunner has a designated sector of fire. Do not cross into the other gunner's sector without coordination. Standard sector assignment:
- Port gunner: port (left) side, from 9 o'clock to 6 o'clock (looking aft-left).
- Starboard gunner: starboard (right) side, from 3 o'clock to 6 o'clock (looking aft-right).
- Overlap zone (6 o'clock): either gunner can engage after confirming the other has ceased fire.

---

### 5.5 Crew Coordination — Pilot and Gunners

**Mandatory pilot calls before maneuvering:**
These calls warn gunners of imminent attitude changes. Gunners must secure their position (hold on to the airframe) before aggressive maneuvers.
- *"Coming left"* — before a left turn.
- *"Coming right"* — before a right turn.
- *"Diving in"* — before a diving attack run; gunners brace.
- *"Breaking"* — before a hard pull-off; gunners brace; clear guns (remove fingers from triggers).
- *"Level"* — aircraft is back in level flight; gunners may resume firing.

**Gunner target call format (reviewed from Module 2.3):**
> *"Pilot, [position] — [o'clock], [distance], [description], [remarks]."*

**Engagement authorization:**
- Standard: pilot authorizes all engagements. Gunner calls target; pilot confirms engagement.
- Pilot call: *"Cleared to engage"* or *"Engage at will"* (when target area is cleared and pilot cannot engage from pilot seat).
- Gunner does not fire without authorization unless explicitly under immediate threat (self-defense call).

**Cease fire:**
- Call: *"Cease fire, cease fire"* — all crew stops firing immediately and acknowledges.
- Any crew member can call cease fire; pilot has final authority.
- After a cease fire call: all triggers released; report "Port gun safe" / "Starboard gun safe."

**Friendly forces awareness:**
- Before any gunner fire, the pilot confirms the target area is clear of friendly forces.
- If a gunner is uncertain: *"No joy on target — wait one"* — do not fire until confirmation.
- Identification of friendly troops in DCS: smoke panels, VS-17 panels (orange fluorescent), colored smoke.

---

### 5.6 Wagon Wheel / Orbiting Fire with Door Guns

The wagon wheel attack pattern (detailed in Module 6) incorporates door guns as a sustained fire supplement to the pilot's forward weapons. During each orbit, the door gunners have the opportunity to engage the target during the inbound and outbound arcs.

**Right-hand orbit:**
- Inbound arc: target is on the aircraft's right side → **starboard gunner** has the primary engagement window.
- Outbound arc: target transitions from right to left → **port gunner** may have a brief engagement window as target passes through left-door arc.
- Pilot call at roll-in: *"Target right, engaging"* → starboard gunner commences fire.

**Left-hand orbit:**
- Inbound arc: target is on the aircraft's left side → **port gunner** has the primary window.
- Pilot call: *"Target left, engaging."*

**Simultaneous pilot and gunner fire:**
- Pilot fires rockets or M134 during the inbound arc while door gunners also fire.
- Coordination: pilot calls weapon type: *"Rockets out, stand by."* Gunners continue fire unless blast/fragmentation hazard exists at the engagement range.
- At ranges > 300 m, door gun and rocket simultaneous fire is generally safe. At < 300 m with HE rockets, gunners should pause fire and take cover against potential fragmentation.

---

### 5.7 Door Gun Employment vs. Ground Troop Proximity

| Weapon | Danger Close Distance | Notes |
|---|---|---|
| M60D (7.62mm) | 200 meters from friendly forces | Ricochet; fragments; direct fire hazard |

**Positive identification requirement:** The M60D fires a small-caliber projectile with limited marking — there is no visible impact signature equivalent to rocket HE. Gunners must be certain of the target before firing. In the real aircraft, the commander's decision is final. In DCS, require students to verbalize positive identification before any door gun fire.

**Stop-fire authority:** Any crew member can halt fire by calling *"Cease fire."* The pilot has final authority over all weapons. The pilot can override a gunner's "fire" decision at any time.

---

### 5.8 Common Student Errors — M60D Door Gun

| Error | Correction |
|---|---|
| Not maintaining sector discipline | Brief sector assignments before flight; grade on sector violations |
| Firing without pilot authorization | Reinforce engagement authorization procedure on every training event |
| No lead on moving targets | Walk through lead calculation during academic training; then drill in DCS |
| Sustained trigger hold without observation pauses | Enforce 5–7 round burst discipline; use verbal callouts |
| Not calling target before engaging | Require target call format before every engagement; no call = no fire |
| Pointing gun aft of cabin bulkhead | Brief tail rotor arc safety hard stop; simulate mechanical stop as a procedural rule |
| Failing to acknowledge pilot maneuver calls | "Bracing" call required within 2 seconds of any pilot maneuver warning |

---

## Module 6: Attack Profiles & Gunnery Patterns

### 6.1 The Wagon Wheel / Rocket Run Orbit — Primary UH-1H Attack Pattern

The **wagon wheel** (also called the **orbiting attack** or **circle attack**) is the foundational attack pattern for the UH-1H gunship. It provides continuous fire against a target while preventing a single aircraft from flying a predictable straight-line approach. Each aircraft in a flight wheels around the target and fires on the inbound arc, then breaks off and re-enters the orbit.

**Complete wagon wheel pattern:**

| Element | Standard Value | Notes |
|---|---|---|
| Orbit altitude | 800–1,500 ft AGL | Higher = more safety margin; lower = better target acquisition |
| Orbit airspeed | 60–80 KIAS | Slow enough for continuous target track |
| Orbit radius | 400–800 m from target | Must match planned attack airspeed and slant range |
| Orbit direction | Left-hand (CCW) is standard | Right-hand when terrain or threat dictates |
| Roll-in point | 90–120° before attack heading | Begin turn inbound; lower nose to establish dive |
| Attack dive angle | 10–15° toward target | Steeper for more accuracy; shallower for area targets |
| Attack airspeed at release | 80–100 KIAS | Stabilize before firing |
| Release range | 600–1,000 m slant range | Per ballistic table |
| Pull-off | 2–3 G; turn away from target | Away from friendly forces; no overfly of target |
| Recovery altitude before re-attack | Return to orbit altitude | Minimum 300 ft AGL before next roll-in |

**Roll-in geometry:**
- The pilot is in the orbit at, say, the 9 o'clock position (target at 12 o'clock of the orbit).
- At 90° prior to the attack heading (passing through the 9 o'clock position), the pilot rolls into the inbound turn and begins to establish the dive.
- By the time the aircraft is pointing at the target (12 o'clock), it should be in a 10–15° dive at 80 KIAS and at the correct slant range to fire.

**Ammunition tracking during successive passes:**
- Assign a maximum round count per pass before entering the orbit (e.g., "2 rockets per pass, PAIRS").
- After each pass, call rounds expended: *"Two rockets expended, 16 remaining."*
- Brief the bingo count (minimum reserve to retain for self-defense or emergency): e.g., "Bingo is 4 rockets."
- When bingo is reached, disengage and exit the orbit.

**When to abort a pass:**
- Target obscured (smoke, dust, movement) — call *"Aborting, no joy"*; continue orbit; re-attack next pass.
- Aircraft parameters out of limits (too fast, too slow, wrong altitude at roll-in).
- Friendly forces in the impact zone — abort immediately; call ground element.
- Weapons malfunction — safe weapons; continue orbit without firing; assess malfunction.
- Too low at planned fire point — pull off; return to orbit altitude; do not press below minimum altitude.

---

### 6.2 Standard UH-1H Attack Profiles

#### 6.2.1 High Hover Attack

**Use:** LZ preparation; close-in suppression; final covering fire for troops at short range.

| Parameter | Value |
|---|---|
| Hover altitude | 50–200 ft AGL |
| Airspeed | 0 KIAS (stationary) |
| Weapons | Rockets (short range) or minigun |
| Engagement range | 200–600 m |
| Exposure risk | Extreme — stationary target |

**Procedure:**
1. Approach to an out-of-sight-line position; climb to hover altitude on approach.
2. Pop up to firing position; establish stable hover.
3. Align nose to target; set depression; Master Arm ARM.
4. Fire; assess; correct; fire again (up to 10–15 sec maximum hover exposure).
5. Break off — descend or accelerate to transition speed; escape laterally.

**Instructor note:** The high hover attack is used only when no other profile is feasible. A stationary helicopter at 100 ft AGL within 600 m of an armed enemy position is extremely vulnerable. Pre-brief an immediate escape direction and do not hesitate to break if taking fire.

---

#### 6.2.2 Running / Level Fire Attack

**Use:** Area suppression; tree line strafe; road column; when altitude restrictions prevent a dive.

| Parameter | Value |
|---|---|
| Entry altitude | 50–300 ft AGL |
| Entry airspeed | 80–100 KIAS |
| Dive angle | 0–5° |
| Engagement range | 400–1,000 m |
| Primary weapon | Rockets (area), minigun (line target) |

**Procedure:**
1. Approach target at low altitude; identify target bearing.
2. Set sight depression for level fire at planned airspeed.
3. Master Arm ARM; weapon selector set.
4. At planned range: align sight; fire burst or rockets.
5. Continue past target's bearing; do not pull up directly over target.
6. Break away; climb if ceiling allows; assess BDA.

---

#### 6.2.3 Diving Attack (Primary Profile)

**Use:** Point target destruction; most accurate forward-fire profile.

Full parameters and procedure are detailed in Module 3.4.1. Summary:

| Parameter | Value |
|---|---|
| Dive angle | 10–20° |
| Attack airspeed | 80–100 KIAS |
| Release range | 600–1,200 m |
| Minimum release altitude | 300–500 ft AGL |
| Pull-off | 2–3 G; 200 ft AGL minimum |

---

#### 6.2.4 Circling / Wagon Wheel

As described in 6.1 above. The primary sustained-fire pattern for the UH-1H flight.

---

### 6.3 Multi-Ship Attack Coordination

When two or more UH-1H aircraft operate as a fire team or flight, coordinated attack patterns ensure continuous fire and mutual support.

**Trail attack:**
- Two aircraft attack the same target in trail (one behind the other).
- Lead aircraft rolls in and fires; when lead calls *"Breaking off,"* trail begins roll-in.
- Result: target receives near-continuous engagement with minimal gap between aircraft.
- Communication format:
  - Lead: *"[Callsign], in from the north."* (entering attack)
  - Lead: *"Breaking right."* (leaving target area)
  - Trail: *"Trail, in."* (beginning attack)
  - Trail: *"Breaking left."* (leaving)
  - Both: *"[Callsign], off [direction], clear."* (safe, out of target area)

**Wagon wheel with two aircraft:**
- Aircraft orbit the target 180° apart — while one aircraft is inbound firing, the other is outbound climbing.
- This provides a continuous fire capability (every 30–45 seconds, one aircraft is firing).
- Entry to the orbit: lead enters first; trail enters 180° opposite on lead's call: *"Trail, take up position, 6 o'clock of the orbit."*

**In-out calls:**
- *"In"* — aircraft is beginning its attack run (inbound to target).
- *"Off"* — aircraft has completed firing and is pulling off (leaving target area).
- *"Splash"* — impact observed; used when WP or BDA can be confirmed.
- *"Abort"* — immediate cessation of attack for any reason.

**Separation and deconfliction:**
- Maintain a minimum of 500 ft vertical or 1,000 m horizontal separation between aircraft at all times during coordinated attacks.
- Do not roll in while another aircraft is in the target area (below the pull-off altitude).

---

### 6.4 LZ Preparation (LZ Prep)

The UH-1H gunship's most common historical mission was **LZ preparation** — suppressing enemy forces in and around a landing zone immediately before a flight of troop-carrying "slicks" (transport UH-1s) arrives to offload troops.

**Sequence of events:**
1. **Pre-mission:** Gunship flight lead coordinates with slick flight lead on LZ approach heading, arrival time, and abort criteria.
2. **Final prep pass timing:** The last fire pass must end at least **3 minutes** before slick touchdown (allows ordnance effects to settle; smoke to clear enough for slick pilots to see the LZ).
3. **Attack passes:** Gunship flight conducts 3–6 passes over the LZ perimeter, working from the far edge inward.
   - Begin with the tree lines and brush providing enemy cover.
   - Final passes target the LZ perimeter closest to the touchdown area.
   - Preferred weapons: rockets (M151 HE) for area suppression of the perimeter; minigun or door guns for close-in cover.
4. **Coordination call:** *"LZ cold, slicks cleared in"* — when gunships have completed final pass and assess LZ is suppressed.
5. **Overwatch during landing:** Gunships orbit the LZ during slick landing; stand by to engage if ground fire is observed.

**Communications with the slick flight:**
- *"[Gunship callsign] to [Slick callsign] — LZ prep complete, LZ cold, cleared in."*
- If the LZ is hot (taking fire): *"LZ hot — hold, orbit at [location and altitude]."*
- Gunships abort LZ hot call and conduct additional passes before re-clearing.

---

### 6.5 Immediate Action on Abort Criteria

Any of the following require immediate abort of the attack run:
1. **Friendly forces in the impact zone** — highest priority abort.
2. **Target obscured** — cannot confirm aim point.
3. **Aircraft below minimum release altitude** before fire point reached.
4. **Aircraft airspeed out of limits** at roll-in (> 15 KIAS deviation from planned).
5. **Weapons malfunction** — no firing effect despite trigger press with Master Arm ARM.
6. **Controller abort call** (*"Abort, abort"*) from ground or air controller.
7. **Traffic conflict** — another aircraft enters the attack corridor.

**Abort call and procedure:**
- Pilot calls: *"Aborting — [reason]."*
- Immediately cease trigger pressure.
- Break off: apply cyclic pull; turn away from target; climb.
- Report to flight lead and/or ground controller.
- Do not re-attack without briefing the reason for abort and correcting the condition.

---

### 6.6 Post-Attack Procedures

**Battle Damage Assessment (BDA):**
After each attack run (or after the full engagement sequence), the pilot conducts a visual BDA:
1. Overfly the target area at a safe altitude (500+ ft AGL) and offset — do not overfly directly.
2. Observe: vehicles destroyed/burning, troops no longer visible, positions suppressed.
3. Report to ground controller or flight lead.

**BDA format:**
> *"[Callsign] BDA: [number] rockets expended, [number] rounds minigun. Observed: [effects]. Target status: [destroyed/damaged/suppressed/unknown]."*

**Re-engagement decision:**
- If target is destroyed: disengage; report; move to next task.
- If target is damaged or suppressed: continue attack if ammunition allows; request additional assets if not.
- If no effect observed: reassess target type; consider ammunition mismatch (e.g., M151 HE against armored target); coordinate for more effective weapons.

---

### 6.7 Common Student Errors — Attack Profiles

| Error | Correction |
|---|---|
| Roll-in too late — arrives at fire point too high or too fast | Brief roll-in geometry; establish orbit first; practice roll-in timing before firing |
| Pressing below minimum release altitude | Hard altitude floor callout on every pass; IP grades on pull-off altitude |
| Re-attack without climbing to orbit altitude | Enforce orbit altitude recovery before every roll-in; one pattern required between passes |
| No "in" / "off" calls in multi-ship | Enforce radio discipline; no roll-in without "in" call; IP withholds clearance until call made |
| LZ prep too close to slick arrival | Brief timing; gunships must complete final pass with 3-min margin before slicks arrive |
| BDA not reported after engagement | Require BDA call after each attack sequence; grade on completeness of report |
| Holding trigger all the way to close range | Brief fire range discipline; trigger release at planned range even if pass continues |

---

## Module 7: Close Combat Attack (CCA) & Fire Support Integration

### 7.1 CCA Doctrine Overview

**Close Combat Attack (CCA)** is defined as the employment of organic Army aviation attack and armed reconnaissance assets against targets that are in close proximity to friendly ground forces (ATP 3-04.1). CCA is fundamentally different from Close Air Support (CAS) in jurisdiction, assets, and control authority:

| Factor | CCA | CAS (Joint) |
|---|---|---|
| Authority | Ground force commander (organic aviation) | JTAC / Joint FAC (FAC-A qualified) |
| Assets | Army attack/armed helicopters | Fixed-wing, USMC rotary, SOF |
| Control document | OPORD / FRAGO; verbal coordination | Air Tasking Order; 9-Line CAS request |
| Clearance | Ground commander; no JTAC required | JTAC "cleared hot" required |
| Proximity definition | CCA danger close: per weapon type | CAS danger close: generally 600 m for fixed-wing |
| Positive ID requirement | Mandatory | Mandatory |

**Key doctrinal distinction:** The UH-1H gunship flying CCA missions is organic to the ground unit it supports. The pilot takes guidance from the Ground Commander or designated ground element. A formal JTAC is not required, but positive identification and coordination are still legally and tactically mandatory.

> *⚠ Realism Divergence: DCS single-player AI ground units do not formally request CCA using ATP 3-04.1 format. In SP, the player simulates the coordination by consulting the briefing/map and self-directing. In multiplayer with human ground players, full coordination can be practiced. This module describes the real-world standard as academic knowledge; DCS implementation options are addressed in 7.6.*

---

### 7.2 Fire Request Formats

When a ground element requests helicopter fire support, the request should contain the following minimum information. In Army aviation, this is commonly transmitted on the unit's internal FM net:

**Minimum required elements:**
1. **Unit identification:** Who is requesting ("Alpha 3-6 requests fire support.")
2. **Target location:** Grid (MGRS or UTM) or talk-on from a known reference point.
3. **Target description:** What the target is, number of elements, activity.
4. **Friendly force location:** Minimum distance from target to nearest friendly element.
5. **Desired effects:** Suppress, destroy, mark, illuminate.
6. **Restrictions / Remarks:** Abort conditions, no-fire areas, civilians in vicinity.

**Standard ground fire request (example):**
> *"[Pilot callsign], this is [Ground callsign], fire mission. Target grid: Papa Alpha 4756 8823. Target description: enemy platoon, 20+ personnel, in the open, moving north. Friendly forces: 400 meters southwest of target. Desired effects: destroy. No restrictions."*

**Pilot readback:**
> *"[Ground callsign], [Pilot callsign] copies. Target: Papa Alpha 4756 8823. Enemy platoon, moving north. Friendlies 400 meters southwest. I will engage from the north, rockets, 2-pass. Advise ready."*

The pilot reads back key elements and announces the planned attack direction, weapons, and number of passes. The ground element confirms or corrects.

---

### 7.3 Target Location Methods

#### Grid Coordinate
- **MGRS (Military Grid Reference System):** Standard 8- or 10-digit grid identifying a point on the map.
- Pilot procedure: plot the grid on the DCS F10 map; fly to the grid area; acquire the target visually from the grid reference.
- DCS F10 map coordinates: DCS uses DCS-native coordinates (X/Y or lat/long depending on map settings). Convert to MGRS if required, or brief teams to use consistent coordinate format.
- Accuracy: a 10-digit MGRS is accurate to ±5 m; a 6-digit to ±100 m. Brief which precision level to use for the mission.

#### Talk-On Procedure
A **talk-on** is a verbal guidance sequence where the ground or air controller steers the pilot's eyes to the target using visual references.

**Standard talk-on sequence:**
1. **Initial reference point:** A large, obvious feature both parties can see (river bend, road junction, building).
   > *"See the river bend at your 11 o'clock?"*
2. **Direction and distance from reference:** Move from the reference to the target.
   > *"From the bend, come 200 meters northeast."*
3. **Target description:** What to look for at that point.
   > *"You should see a cluster of vehicles on the north bank — three trucks, stationary."*
4. **Confirmation:** Controller asks if pilot has tally; pilot responds.
   > *"Tally on three trucks, north bank."*
5. **Clearance:** Controller clears engagement or adjusts.

**Common talk-on errors:**
- Using references the pilot cannot see from altitude.
- Describing compass directions without noting the aircraft's current heading (confusion between aircraft-relative and ground-relative directions).
- Solution: use o'clock directions relative to the aircraft first, then switch to compass once both parties are oriented.

#### WP Smoke Marking
Ground unit fires a WP grenade or rocket at or near the target to mark it for the helicopter.
- Pilot acknowledges seeing smoke: *"Tally smoke, [color]."* (WP produces white smoke.)
- Controller confirms: *"Affirm, that is the mark — target is 30 meters north of smoke."*
- Pilot adjusts aim point 30 m north and engages.
- Note: Do not aim directly at the smoke mark — the mark may be on a friendly grenade or observation post. Always confirm offset.

#### Laser Pointer (DCS Context)
In DCS, AI ground units do not currently generate IR laser designators visible to the helicopter crew. In human multiplayer with proper mod support, IR lasers may be visible through NVG. In standard training, this method is academic.

---

### 7.4 Attack Coordination with Ground Forces

**Pre-attack safety brief (pilot to ground controller):**
Before each attack run, the pilot transmits:
> *"[Callsign], attack from the [direction], [weapon type], [number] passes. Standby for [weapon effects: smoke, HE, illumination]. Any restrictions?"*

This gives the ground element time to:
- Move personnel to covered positions.
- Remove vehicle antennas and equipment from the line of fire.
- Confirm no friendly forces are in the impact area.

**Run-in heading:**
- The pilot announces the heading of the attack pass.
- Ground forces to the side of or behind the attack direction are shielded; those in front of the attack must take cover.
- Fragmentation from M151/M229 is danger close at 230 m in the direction of fire.

**"Cleared hot":**
- The ground commander or ground controller transmits this phrase when they are ready for the attack to proceed.
- The pilot should NOT fire until cleared hot (except in immediate self-defense).
- *"[Pilot callsign], cleared hot."*

**"Abort, abort":**
- Any party (pilot, controller, ground commander) can call abort at any time.
- On hearing "Abort, abort": pilot immediately releases trigger, breaks off, climbs.
- Pilot acknowledges: *"Aborting."*
- After abort: assess and re-brief before any re-attack.

---

### 7.5 Rules of Engagement (ROE) and Positive Identification

**Positive identification (PID) requirement:** Before employment of any weapon, the pilot must be able to positively identify the target as a valid military objective. This means:
1. The target is clearly military in nature (armed forces, weapons systems, military equipment in hostile use).
2. The target is not in a protected site (hospital, cultural property, civilian concentration).
3. Collateral damage assessment (CDA) has been considered for the engagement.

**Procedure when target identity is uncertain:**
1. Cease attack approach; do not roll in.
2. Transmit: *"[Callsign], I cannot PID the target — request confirmation."*
3. Controller re-describes target or provides additional identification data.
4. If still uncertain: *"I cannot confirm hostile status — aborting this pass."*
5. Do not fire on uncertain targets. No military objective justifies firing on unconfirmed targets.

**Friendly force marking recognition (DCS):**

| Marking | Appearance in DCS | Real-world standard |
|---|---|---|
| VS-17 panel | Orange/pink rectangular panel on vehicle roof or ground | Standard U.S. ground forces marking |
| Colored smoke | Smoke grenade on the ground | Confirm color verbally — never assume |
| IR strobe | Flashing IR light (visible with NVG in DCS NVG mode) | Used at night; varies by unit SOP |
| Chem light | Not reliably rendered in DCS | Blue/IR chem lights; night operations |

**"Spike" (colored smoke) confirmation procedure:**
Ground pops smoke → Pilot sees smoke → Pilot calls color → Ground confirms or denies. Never: pilot asks ground to "pop smoke" on the target — this tells the enemy to also pop smoke to confuse identification.

---

### 7.6 DCS Mission Integration for CCA Training

**Single-player CCA simulation:**
- Use the **DCS Mission Editor** to create a mission with enemy ground forces near friendly AI units.
- Set mission briefing to include a target grid and description.
- Use the **F10 map** to identify target grids; brief self using written mission card format.
- Pre-brief attack direction, weapons, and number of passes before takeoff.
- After engagement: assess F10 map BDA (target destroyed/damaged shown by smoking wrecks).

**Simulating the fire request:**
- Write a formatted fire request card before takeoff; read it aloud as if receiving it on the radio.
- Execute the attack using the steps from 7.4.
- This disciplines the student to plan before they execute, rather than rolling directly to the target.

**Radio menu integration:**
- DCS AI ground units (when assigned correctly) can be tasked via the radio command menu to mark targets or hold position.
- Use this to simulate a ground element requesting fires.

**Multiplayer with human ground players:**
- Full ATP 3-04.1 coordination can be practiced with human players using DCS SRS (Simple Radio Standalone) or in-game communications.
- Human ground players use the F10 map for target grids; use MGRS coordinates.
- This is the highest-fidelity CCA training available in DCS.

---

### 7.7 Common Student Errors — CCA Execution

| Error | Correction |
|---|---|
| Attacking without a fire request readback | Enforce readback before every attack; no attack without confirmation |
| Not announcing attack direction before firing | Brief must-include elements for pre-attack call; grade on completeness |
| Engaging before "Cleared hot" | Reinforce: "Cleared hot" is a legal and tactical requirement, not optional |
| Aiming directly at the smoke mark | Brief offset procedure; smoke is proximity reference only, not aim point |
| Not calling "Aborting" when breaking off | All breaks must be called; silent breaks leave the ground element without situational awareness |
| Firing inside danger close without explicit clearance | Drill danger close procedures; require verbal readback of danger close acceptance |
| No BDA report after engagement | BDA report is mandatory after each sequence; grade on content and timeliness |

---

## Module 8: Weapons Loading, Weight & Performance

### 8.1 Loadout Configurations — Performance Impact

**UH-1H basic weight reference (empty/clean):**
- Empty weight: approximately 2,363 kg (5,210 lb) — varies by configuration
- Maximum gross weight: 4,309 kg (9,500 lb) — includes fuel, crew, and payload
- Fuel weight: Full internal fuel (~814 liters / 215 gal JP-4) = approximately 651 kg (1,435 lb)
- Standard crew weight: Pilot + crew chief + 2 gunners = approximately 320 kg (700 lb)

**Weapons weight per loadout item:**

| Item | Approximate Weight |
|---|---|
| XM-158 (7-tube loaded, M151 HE ×7) | ~40 kg (88 lb) |
| XM-159 (19-tube loaded, M151 HE ×19) | ~95 kg (210 lb) |
| M134 pod (1,500 rounds 7.62mm) | ~115 kg (253 lb) |
| M60D door gun (mounted, 400 rounds) | ~15 kg (33 lb) per gun |

**Standard loadout total weapons weight and performance:**

| Loadout | Total Weapons Weight | Available Payload Reduction | Notes |
|---|---|---|---|
| Clean (door guns only) | ~30 kg (66 lb) | Minimal | Maximum performance; reserve for escort duties |
| 2× XM-158 (14 rockets) | ~110 kg (242 lb) | Light | Standard light attack; minimal performance cost |
| 2× XM-159 (38 rockets) | ~220 kg (485 lb) | Moderate | Heavy LZ prep load; notable climb rate reduction |
| 2× M134 pods (3,000 rds total) | ~230 kg (507 lb) | Moderate | Similar weight to 2× XM-159; sustained gunfire |
| Mixed: M134 + XM-159 | ~210 kg (463 lb) | Moderate | Standard gunship load; versatile |
| Full: 2× XM-159 + 2× door guns | ~250 kg (551 lb) | Heavy | Maximum firepower; most restricted performance |

> *Note: DCS models weight effects on hover ceiling and climb rate. These values are approximate; DCS-specific behavior should be validated in-game at the mission's density altitude.*

---

### 8.2 Effect on Hover Ceiling, Vne, and Maneuverability

**Hover ceiling impact:**
The hover ceiling (both IGE and OGE) decreases as gross weight increases. With weapons loaded, the pilot must re-verify hover power margin before committing to a departure or confined area operation.

**Density altitude reference (approximate performance thresholds):**

| Loadout | IGE Hover Ceiling (Standard Day) | OGE Hover Ceiling (Standard Day) |
|---|---|---|
| Clean | ~12,000 ft DA | ~6,000 ft DA |
| 2× XM-158 | ~11,000 ft DA | ~5,500 ft DA |
| 2× XM-159 | ~9,500 ft DA | ~4,500 ft DA |
| Full gunship | ~8,500 ft DA | ~3,500 ft DA |

> *⚠ Realism Divergence: DCS approximates hover ceiling based on power loading. Real UH-1H performance data from TM 55-1520-210-10 is more precise and accounts for specific density altitude, aircraft weight, and power setting. Use these figures as planning guidance; always verify with a power check hover in DCS before committing to an operation in degraded-performance conditions.*

**Vne impact:**
The UH-1H Vne (never-exceed speed) is 124 KIAS in clean configuration. With external stores loaded, Vne may be reduced based on pylon drag and flutter margins. In DCS:
- External stores do not significantly reduce Vne in the DCS model for typical loadouts.
- However, asymmetric or heavy asymmetric loads may produce handling qualities that make high airspeeds uncomfortable before Vne is reached.
- Operationally, limit transit airspeed to 100 KIAS with heavy rocket loads to maintain control margin for maneuvering.

**Autorotation with weapons loaded:**
A heavier aircraft has a higher potential energy but requires more collective pitch at flare to arrest descent, consuming Nr more rapidly. At high density altitude with heavy stores, the autorotation margin is reduced:
- Higher rate of descent in the glide (~1,800–2,200 fpm at 65 KIAS for heavily loaded aircraft vs. ~1,500 fpm clean).
- Less collective travel available during flare (some collective already consumed against higher rotor drag).
- **Jettison option:** If engine failure occurs with a heavy stores load at high DA, jettisoning the pylons may be appropriate before autorotation entry if altitude and time permit.

**Maneuverability:**
- Roll rate and yaw response are modestly reduced with heavy pylon loads due to increased rotational inertia and pylon drag.
- The most significant maneuverability effect is in aggressive breaking turns (pulling off from a diving attack) — heavier aircraft requires more collective to maintain altitude in the break, which increases torque demand.
- Pre-flight brief: "Heavier aircraft, expect more collective during pull-off."

---

### 8.3 Density Altitude Planning

**Density altitude (DA) formula:**
DA ≈ Pressure Altitude + (120 × [OAT°C − ISA temp at altitude])

At sea level, ISA temp is 15°C. For every 1°C above ISA, add 120 ft to pressure altitude to get DA.

**Practical planning steps:**
1. Obtain field elevation and current QNH (altimeter setting).
2. Calculate pressure altitude: Field elevation + 27 ft per 0.01 inHg below 29.92.
3. Get OAT from DCS weather briefing.
4. Calculate DA.
5. Compare to hover ceiling table above.

**Weapons delivery at high DA:**
- Engine power is reduced at high DA — this limits both hover performance and the power margin for aggressive pull-offs after attack runs.
- Airspeed at a given IAS corresponds to a higher TAS at high DA — true rocket time of flight and drag are similar, but true groundspeed is higher, affecting weapons delivery accuracy.
- For training above 4,000 ft DA with heavy loads: reduce pylon payload; use XM-158 instead of XM-159; consider clean loadout for single-aircraft operations.

**Pre-departure hover check with weapons:**
1. Before takeoff, hover IGE at 3–5 ft AGL.
2. Note torque at hover: if torque > 35–38 PSI to maintain hover, performance is marginal for OGE hover or sustained climb with weapons.
3. If torque exceeds 40 PSI at IGE hover, abort; reduce load (fuel, ammunition, payload).
4. In DCS: same check — hover at 3 ft AGL; observe torque gauge; verify adequate margin before committing.

---

### 8.4 Emergency Jettison

**When to jettison:**
- Aircraft emergency requiring immediate weight reduction (engine failure, fire, fuel emergency).
- Weapons malfunction creating a safety hazard (hung store with suspected armed fuze).
- Aircraft gross weight exceeds autorotation safe landing weight at the given density altitude.

**Jettison panel location and sequence:**
- Jettison panel: center console area; labeled with station identifiers.
- In DCS, all-station jettison is the primary emergency jettison option — it drops both pylon stores simultaneously.

**Emergency jettison procedure:**
1. Master Arm — SAFE (prevents inadvertent weapon arming during jettison event).
2. Jettison panel cover — LIFT.
3. Jettison switch — ACTUATE.
4. Observe: pylons should clear; stores separate.
5. Verify: visually confirm pylons are clear; handling qualities improve (aircraft becomes lighter and more responsive).
6. Advise crew: *"Stores jettisoned — confirm clear."*

> *⚠ Realism Divergence: DCS models all-station jettison as a single event dropping all pylon stores. The real aircraft has both selective jettison (individual station) and all-station emergency jettison. In DCS, only the all-station emergency jettison is reliably modeled. If a single pylon malfunction requires selective jettison, use the all-station procedure and accept the asymmetric condition until landing.*

**Post-jettison checks:**
- Note new aircraft gross weight (lighter).
- Re-assess hover performance margin.
- Check handling qualities — aircraft should now fly symmetrically (both pylons empty).
- If one pylon failed to release: aircraft is asymmetric; see 8.5.

---

### 8.5 Asymmetric Stores

**Condition:** One pylon loaded (or heavier), one empty (or lighter). This occurs after:
- Selective jettison of one pylon (if modeled).
- One pylon expending all ammunition while the other retains rounds.
- Malfunction preventing one pylon's weapons from firing.
- Emergency jettison of one pylon.

**Handling technique:**
- The aircraft will roll toward the heavier side; apply opposite cyclic to maintain wings-level.
- Yaw tendency: heavier pylon creates more drag; apply opposite pedal.
- Apply trim to relieve sustained control inputs — set trim with asymmetric load established in level flight.
- Airspeed restriction: limit to 80 KIAS for asymmetric pylon load; aggressive maneuvering may be difficult to control.

**Landing with asymmetric stores:**
- Approach to a slow running landing or a careful hover; minimize lateral maneuver.
- At hover: torque effect and asymmetric weight will push the aircraft toward the heavy side — maintain awareness of drift tendency.
- Touchdown on a level surface; reduce collective smoothly.
- Post-landing: notify ground crew of asymmetric load before they approach the aircraft.

---

### 8.6 Common Student Errors — Weapons Loading & Performance

| Error | Correction |
|---|---|
| No pre-departure hover check with weapons | Enforce hover check as a mandatory pre-takeoff item whenever weapons are loaded |
| Loading full XM-159 × 2 at high DA without performance check | Brief DA planning; require weight/hover check before accepting heavy load at DA > 3,000 ft |
| Not adjusting trim for asymmetric loads | Drill: when asymmetric condition occurs, immediately set trim; verbalize the condition |
| Forgetting to jettison before emergency landing | Jettison decision must be briefed pre-mission; "if engine failure, jettison pylons before autorotation entry if altitude allows" |
| Exceeding 100 KIAS with heavy stores on aggressive maneuver | Brief airspeed restriction with heavy stores; grade on airspeed discipline during attack profiles |

---

## Module 9: Night and Reduced Visibility Weapons Employment

### 9.1 NVG (Night Vision Goggle) Operations — UH-1H Context

**Real-world NVG configuration:**
Vietnam-era UH-1H gunship operations were conducted without NVG — crews relied on ambient light (flares, fires, moonlight) and tracer feedback for weapons employment. Modern NVG-equipped UH-1H crews (post-Vietnam through current National Guard operations) use the **AN/AVS-6** Aviator's Night Vision Imaging System (ANVIS) or monocular **AN/PVS-14** — Generation III image-intensification devices.

**DCS NVG mode:**
- DCS UH-1H includes an NVG mode activatable via the **\` (tilde)** key or a designated NVG toggle keybind.
- DCS NVG simulates binocular image-intensified view with reduced field of view (approximately 40° vs. naked-eye 180°+).
- DCS NVG limitations vs. real: no depth perception loss modeled; no rain/moisture degradation; no bleed-through from bright light sources (real NVG whiteout in flare or explosion proximity is not fully modeled in all DCS versions).
- NVG view provides grayscale terrain and target imaging; tracers and flares are prominently visible.

**Cockpit lighting for NVG compatibility:**
- Before NVG operations, reduce all white-light cockpit lighting to minimum or turn off.
- Turn on NVG-compatible (red/green/IR) instrument lighting if available in DCS.
- In DCS UH-1H: reduce instrument panel lighting via the lighting rheostat (right sidewall panel) to its lowest setting; turn off cabin lighting.
- External lights: position/navigation lights (LShift + L) should be set to LOW or OFF for tactical operations; landing light (LCtrl + L) should be OFF.
- Warning: bright cockpit lights will bloom through NVG and reduce outside scene visibility.

**Weapons delivery on NVG:**
- The optical sight is still usable with NVG but requires head positioning to see through the sight glass; the NVG monocular may partially obscure the sight glass depending on helmet and NVG configuration.
- In DCS with NVG mode active, the sight remains visible; position the camera to align with the sight.
- **Tracer visibility on NVG:** M62 and M62-equivalent tracers appear brightly in the NVG image — they are the primary aiming feedback tool for night minigun and door gun employment.
- **WP marking visibility on NVG:** WP burns produce a bright, clearly visible white emission on NVG. WP marks at night are more easily seen on NVG than in daylight ambient light.

---

### 9.2 Illumination Rocket Employment (M257)

**System description:**
The **M257 Illumination Rocket** uses a standard 2.75-inch Mk 40 rocket motor to carry a single **M671 ground illumination flare** payload. The flare deploys via parachute at the peak of the ballistic arc and burns for approximately **100 seconds**, providing approximately **150,000 candela** of illumination over a ground footprint of roughly 200–400 meters diameter (dependent on altitude at deployment).

**Optimal deployment altitude:**
- Flare should deploy (parachute open, burn commences) at **800–1,200 ft AGL** over the target area.
- Too high: flare drifts far from target before reaching optimal illumination altitude; light is diffuse.
- Too low: flare burns out before reaching the ground observation zone; duration is insufficient.
- Target illumination altitude: **500–800 ft AGL** is the optimal burn altitude for ground observation.

**Employment procedure:**
1. **Pre-fire call:** *"Illumination round, [time to impact] seconds."* Crew notes time; all look for flare.
2. **Determine range and elevation:** Calculate the range at which the rocket's ballistic arc will peak at 800–1,200 ft AGL above target. At 80 KIAS level flight, the M257 at minimal elevation angle will peak at approximately 1,200 ft AGL at ~600–800 m range.
3. **Set sight elevation:** Reduce depression (aim higher than level) to achieve the required arc — typically 20–40 mils above the zero line.
4. **Fire:** Single illumination rocket.
5. **Observe deployment:** Parachute deploys; flare ignites at arc apex; illumination begins.
6. **Assess ground illumination:** Confirm target area is illuminated before calling door gunners to engage.

**Wind drift of M257:**
- The parachute-suspended flare drifts with the wind.
- At 10 knots surface wind, the flare drifts approximately 50–100 m per minute of burn.
- Fire upwind of the target so the flare drifts over the target area during its burn time.
- Pre-brief wind direction before firing illumination rounds.

**Crew coordination for illumination:**
- *"Illum rounds, out. Ignition in 10 seconds."* — Alert all crew.
- *"Light is on — mark."* — Flare burning; ready to engage ground target.
- *"Light out in [time]."* — Warning that flare will extinguish; prepare for darkness.
- If additional illumination is needed: fire next M257 before the first flare extinguishes to maintain continuous coverage.

---

### 9.3 WP Marking at Night

**M156 WP visibility at night:**
WP burns at approximately 2,760°C and emits a bright white-yellow flame with dense white smoke. At night, the WP flame is clearly visible to the naked eye at distances > 2,000 m in clear conditions and at > 800 m in light haze. On NVG, the WP burn is extremely bright and may bloom (overexpose) NVG image-intensifiers at close range.

**Technique for night WP marking:**
1. Fire M156 at planned aim point using normal depression table for nighttime airspeed.
2. Observe impact: the WP burst and subsequent burn will be clearly visible.
3. Report: *"Smoke is burning, [o'clock direction from target], [distance estimate] meters."*
4. Adjust next firing or call follow-on attack element.

**Combined WP and illumination for night attack:**
- Fire M257 illumination first to establish target area lighting.
- Under illumination, conduct visual target acquisition.
- Fire M156 WP on the specific target point within the illuminated area for precise marking.
- Follow-on attack: engage with M151/M229 HE or minigun against the burning WP mark.

---

### 9.4 Reduced Visibility Attack Considerations

**Effect of fog, smoke, and haze on target acquisition:**
- Visibility in real-world night fog can drop below 100 m; DCS models visibility reduction in weather settings.
- Minimum visibility for safe attack profile entry: **1,500 m** for diving attack (need to see the target at roll-in); **800 m** for running fire.
- Below 800 m visibility: abort attack profile; revert to WP marking or illumination to improve target acquisition range.

**Minimum visibility requirements by profile:**

| Profile | Minimum Visibility for Entry |
|---|---|
| Diving attack (10°) | 1,500 m (need to see target from 1,200 m slant range at roll-in) |
| Running / level fire | 800 m |
| Wagon wheel orbit | 2,000 m (need continuous target track throughout orbit) |
| Hover fire | 400 m (close range; can identify target even in poor visibility) |

**Flare employment in DCS:**
- DCS supports ground-based flares (scripted) and the M257 illumination rocket.
- Flare visibility on NVG: well-rendered in DCS; the primary illumination tool for night training.
- Artificial illumination from burning vehicles (destroyed by earlier engagement) also provides target area lighting — a secondary benefit of early strikes.

**Haze correction for sight:**
- In realistic haze, target contrast is reduced; angular size estimation becomes less accurate.
- Compensate by closing range before firing (reduce engagement range by 20–30% in haze conditions).
- Accept reduced accuracy at range; prefer closer engagement under degraded visibility.

---

### 9.5 Common Student Errors — Night / Reduced Visibility Employment

| Error | Correction |
|---|---|
| Attempting diving attack below visibility minimum | Brief visibility minimums; abort call required if visibility is below threshold at roll-in |
| Forgetting to dim cockpit lights before NVG | NVG pre-flight: cockpit lighting check is part of the checklist before NVG power-on |
| Firing illumination round at wrong elevation — flare too low | Brief M257 arc parameters; practice illumination pass before live engagement |
| Not accounting for wind drift on M257 | Brief wind direction before every illumination pass; fire upwind of target |
| Staring at WP burn on NVG — NVG bloom | Brief NVG technique: avoid direct prolonged stare at WP; look to the side; allow NVG to recover |
| No "light is on" call before directing crew to engage | Enforce illumination sequence calls; do not call crew to engage until illumination confirmed |
| Continuing attack past visibility minimum | Enforce hard abort below visibility floor; no exception |

---

## Module 10: Weapons Malfunctions & Procedures

### 10.1 Common Malfunction Types

#### Hangfire
**Definition:** A rocket that has received the electrical ignition signal but has a delayed ignition — the propellant lights after an unpredictable delay, potentially seconds after the trigger press.

**Real-world hazard:** A hangfire can result in a rocket launching unexpectedly after the pilot believes the system has misfired. This is extremely dangerous if the aircraft has already maneuvered away from the target and is now pointing at friendly forces or terrain.

**DCS behavior:** DCS does not currently model true hangfire delays — rockets either fire immediately or not at all. However, the hangfire procedures are taught as academic standards for real-world safety knowledge.

**Real-world hangfire procedure (TM 55-1520-210-CL):**
1. Weapon selector — SAFE.
2. Maintain current aircraft heading for 30 seconds (do not point at friendly forces).
3. If rocket has not fired after 30 seconds: assume hangfire has resolved (rocket self-contained); do not overfly people or structures.
4. Land at the first available site; do not jettison — jettisoning a hangfire creates an unpredictable hazard.
5. Ground ordnance disposal (EOD) clears the launcher.

---

#### Misfire
**Definition:** The ignition signal was sent but the rocket did not ignite. No delayed ignition expected.

**Real-world procedure:**
1. Weapon selector — SAFE.
2. Note the tube/launcher that misfired (if identifiable).
3. Wait 30 seconds (in case of delayed ignition).
4. If no firing: land; do not attempt to manually remove the round; EOD handles.

**DCS behavior:** DCS can model misfires via the Mission Editor → Failures section. In training mode, a misfire manifests as trigger press with no effect (no visual launch). The student should follow the misfire procedure even in DCS simulation.

---

#### Tube Jam (Rocket Stuck in Tube)
**Definition:** A round fails to exit the launcher tube — it is stuck partially engaged in the tube due to mechanical failure.

**Real-world hazard:** A tube jam with a loaded, armed rocket in the tube creates an explosive hazard at the launcher. The aircraft must land immediately.

**DCS behavior:** DCS does not model tube jams as a distinct failure mode. Academic knowledge only.

**Procedure (real-world):**
1. Weapon selector — SAFE.
2. Master Arm — SAFE.
3. Land immediately at the nearest suitable area.
4. Do not exit the aircraft in the direction of the stuck launcher tube.
5. Call EOD or ordnance personnel.

---

#### M134 Minigun Stoppage
**Definition:** The M134 rotary barrel mechanism stops rotating due to an ammunition jam, electrical failure, or mechanical failure.

**Indicators in DCS:** Trigger pressed; no tracer output; no gunfire sound.

**Immediate action (real-world and DCS):**
1. Release trigger.
2. Weapon selector — SAFE.
3. Check armament panel for power indication.
4. If electrical: check relevant circuit breakers.
5. Attempt to re-engage after 5–10 seconds (allows drive motor to reset).
6. If minigun does not fire after two attempts: declare minigun inoperative; do not continue attempting; select alternative weapon.

**Clearing the stoppage (real-world):**
The M134's drive motor can sometimes clear a jam by cycling. However, attempting to manually clear the M134 in flight is not authorized — if it does not self-clear, land and have ordnance personnel clear it.

---

#### M60D Door Gun Stoppage
**Definition:** The M60D experiences a feed jam, misfire, or mechanical failure interrupting fire.

**Immediate action — SPORTS drill (TM 9-1005-298-14&P):**
1. **S** — Slap the bottom of the magazine/feed tray cover to ensure proper seating.
2. **P** — Pull the charging handle rearward to extract the jammed round.
3. **O** — Observe: look into the chamber/feed area to confirm the jam cleared.
4. **R** — Release the charging handle to chamber a new round.
5. **T** — Tap the forward assist (if equipped) to ensure battery.
6. **S** — Shoot: attempt to fire.

**DCS behavior:** DCS does not model SPORTS drill execution. In DCS, door gun stoppages triggered via Mission Editor failures manifest as the gun ceasing to fire. The student should verbalize the SPORTS procedure as an academic exercise if the stoppage is simulated.

> *⚠ Realism Divergence: The M60D has no forward assist. The "Tap" step of SPORTS refers to confirming the bolt is fully in battery. In DCS, the only action is switching between crew positions and noting the malfunction. Procedures are taught for real-world knowledge.*

---

### 10.2 Hung Store (Rocket That Did Not Fire — Tube Occupied)

**Definition:** A rocket that did not fire on command remains in the launcher tube, armed and potentially dangerous.

**Real-world distinction from misfire:**
- A **misfire** means the ignition signal was sent with no result — possible hangfire, possible dud.
- A **hung store** means the rocket was in the tube before the mission but the tube counter indicates it should have fired and did not — the tube is confirmed occupied after the firing sequence.

**Real-world procedure (TM 55-1520-210-CL):**
1. Do not fire the affected launcher again.
2. Master Arm — SAFE.
3. Land at the first available site with sufficient space and EOD support.
4. Do not exit the aircraft by walking toward the launcher tubes.
5. Brief EOD: launcher tube number, type of round, number of attempts.

**DCS equivalent:**
- If a tube-count discrepancy is apparent (more tubes loaded than rounds fired), treat as a hung store.
- Safe the Master Arm; land; report as part of the post-mission debriefing.
- DCS ordnance removal does not require EOD — the student should acknowledge the procedure academically.

---

### 10.3 Electrical Failure and Weapons

**Effect of generator failure on weapons:**
- The M134 minigun is electrically driven; it requires electrical power to operate. Generator failure while the minigun is firing will stop the weapon immediately.
- The armament panel firing circuit (rockets) is also electrically powered. Generator failure renders the rocket firing circuit inoperative.
- **Battery-only operation:** On battery power alone, the armament panel may remain powered for a limited time (~15–30 minutes depending on battery state). However, M134 operation on battery is not recommended — the high current draw of the minigun will rapidly deplete the battery, leaving the aircraft with no electrical power for essential instruments.
- The M60D door guns are manually operated (no electrical requirement) and will continue to function after total electrical failure as long as ammunition is available.

**Procedure — weapons safe during electrical emergency:**
1. Generator failure or electrical emergency: Weapon selector — SAFE.
2. Master Arm — SAFE.
3. Declare weapons inoperative to crew.
4. Focus on aircraft emergency (refer to BQT emergency procedures for electrical failure).
5. Do not attempt to fire weapons on battery-only power in an emergency.

**Circuit breakers relevant to weapons:**
- Armament panel circuit breaker: located on the right sidewall circuit breaker panel. If the armament panel becomes inoperative, check this breaker first.
- M134 power breaker: separate circuit breaker for minigun pod power; check if minigun is inoperative.
- In DCS: click the circuit breaker panel to pop/reset individual breakers.

---

### 10.4 Unsafe Weapons Indications

**Master Arm light fails to indicate SAFE:**
- If Master Arm is placed in SAFE but the cockpit indication does not confirm SAFE (if any indication exists), treat the system as armed.
- Do not point the aircraft at friendly forces or aircraft.
- Land at the first available site; do not attempt to troubleshoot in flight.

**Armament panel switch failure:**
- If a weapons select switch is stuck, the circuit may remain energized.
- Procedure: do not attempt to force the switch; safe the Master Arm; land.

**General principle:** If there is any doubt about weapon status, assume the system is **ARMED and DANGEROUS**. Treat the aircraft as a loaded weapon and handle accordingly.

---

### 10.5 DCS Malfunction Modeling

| Malfunction | Modeled in DCS | How to Trigger (Mission Editor) | Academic or Simulated |
|---|---|---|---|
| Rocket misfire | Partial (via Mission Editor failure) | Failures → Armament failures | Simulated |
| Hangfire | Not modeled | — | Academic only |
| Tube jam | Not modeled | — | Academic only |
| M134 stoppage | Partial (via Mission Editor failure) | Failures → Armament failures | Simulated |
| M60D door gun stoppage | Partial (via Mission Editor failure) | Failures → Armament failures | Simulated |
| Hung store | Not modeled | — | Academic only |
| Armament panel electrical failure | Partial (via circuit breaker pull) | Click CB on right sidewall panel | Simulated |
| Generator failure affecting weapons | Yes (generator failure removes electrical power) | Failures → Engine / Electrical | Simulated |

**How to trigger malfunctions in DCS Mission Editor:**
1. Open Mission Editor; select aircraft; click "Failure" button.
2. In the failure list, find Armament-related failures.
3. Set time or condition trigger (e.g., "after 5 minutes of flight" or "on user request via F10 radio").
4. Save and run the mission; the malfunction will occur at the set trigger.

**Training recommendation:** IP should trigger at least one weapons malfunction per WEC event (e.g., M134 stoppage, rocket misfire) using Mission Editor failures to ensure students practice the immediate action procedures under realistic conditions.

---

### 10.6 Common Student Errors — Malfunction Procedures

| Error | Correction |
|---|---|
| Continuing to press trigger on a misfire without safing first | Enforce: any trigger press with no result = SAFE the weapon first; then troubleshoot |
| Attempting to re-fire a hangfire immediately | Brief 30-second wait requirement; reinforce with academic discussion of hangfire hazard |
| Declaring minigun inoperative after one attempt (before cycling) | Brief 2-attempt rule before declaring inoperative; allow 5–10 sec reset between attempts |
| SPORTS drill not verbalized on M60D stoppage | Require verbal SPORTS drill for every door gun stoppage in training |
| Not safing weapons before electrical emergency procedures | Brief sequence: weapons safe first, then address electrical emergency |
| Exiting aircraft toward launcher tubes after hung store | Academic brief: forbidden; reinforce on every post-malfunction debrief |
| Ignoring CB check when armament panel is inoperative | Circuit breaker check is first troubleshooting step; reinforce on every occurrence |

---

---

## Appendix: DCS UH-1H Weapons Keybind Reference

> *Note: Default keybinds are for the DCS UH-1H Belsimtek module as of DCS World 2.9 stable. Verify in Options → Controls → UH-1H before training. Many weapons functions are cockpit-click only — no default keyboard assignment. HOTAS users should assign critical functions (Master Arm, weapon select, fire) to physical buttons.*

| Function | Default Keybind | Cockpit Location | Notes |
|---|---|---|---|
| Master Arm ON (ARM) | Mouse click only | Armament panel — upper left | Two-click: lift guard, then switch to ARM |
| Master Arm OFF (SAFE) | Mouse click only | Armament panel — upper left | Click switch down to SAFE; lower guard |
| Weapon select: ROCKETS | Mouse click only | Armament panel — center selector | Rotate to ROCKETS position |
| Weapon select: GUNS (M134) | Mouse click only | Armament panel — center selector | Rotate to GUNS position |
| Weapon select: ROCKETS AND GUNS | Mouse click only | Armament panel — center selector | Rotate to combined position |
| Weapon select: SAFE | Mouse click only | Armament panel — center selector | Rotate to SAFE position |
| Fire mode: SINGLE | Mouse click only | Armament panel — intervalometer | One rocket per trigger pull |
| Fire mode: PAIRS | Mouse click only | Armament panel — intervalometer | One rocket per pylon per trigger pull |
| Weapons fire (rockets / minigun) | Space | Cyclic primary trigger | HOTAS: assign to joystick trigger button |
| Emergency stores jettison | Mouse click on jettison switch | Center console — jettison panel | Lift cover first; then press switch |
| NVG toggle (Night Vision Goggles) | `  ` (backtick / grave accent) | — | Toggles NVG image-intensifier view |
| Switch to pilot seat | F1 | — | Default pilot position |
| Switch to co-pilot seat | F2 | — | Right seat; limited weapons access |
| Switch to port (left) door gun station | F5 | — | M60D left door position; verify in controls |
| Switch to starboard (right) door gun station | F6 | — | M60D right door position; verify in controls |
| Door gun fire (while in crew station) | Space | Crew station trigger (spade grip) | Same key as weapons fire; contextual |
| Sight depression adjust (up) | Mouse wheel up on sight knob | AN/M2A1 sight pedestal | Rotate depression adjustment knob |
| Sight depression adjust (down) | Mouse wheel down on sight knob | AN/M2A1 sight pedestal | Rotate depression adjustment knob |
| Force trim release | T (hold) | Cyclic (trim release) | Hold to release; release key to re-engage trim |
| Force trim set | LCtrl + T | Cyclic | Stores current control position as trim reference |
| Battery ON/OFF | LShift + B | Electrical panel | Required before engine start |
| Generator ON/OFF | LShift + G | Electrical panel | Activate after engine start |
| Inverter ON/OFF | LShift + I | Electrical panel | Required for instruments and avionics |
| Landing light ON/OFF | LCtrl + L | Overhead / center console | Tactical: OFF for night gunship ops |
| Navigation lights ON/OFF | LShift + L | Overhead / center console | Tactical: reduce or OFF for NVG ops |

---

## Quick Reference Card

> *Summary for use as a crew-printed kneeboard reference. All values are standard-atmosphere, sea level. Adjust for DA and wind per Module 3 and Module 8.*

### QRC-1: Weapons Employment — Key Parameters

| Weapon | Warhead Options (DCS) | Max Effective Range | Primary Attack Profile | Primary Target Type |
|---|---|---|---|---|
| XM-158 (7-tube FFAR) | M151 HE, M229 HE, M156 WP, M257 Illum | 1,500 m (M151/M229) | Diving attack (10°), 80–100 KIAS | Personnel, light vehicles, LZ suppression |
| XM-159 (19-tube FFAR) | M151 HE, M229 HE, M156 WP, M257 Illum | 1,500 m (M151/M229) | Diving attack or wagon wheel | Area suppression, LZ preparation |
| M134 Minigun pod | 7.62mm ball/tracer | 800 m | Diving fire (5–15°), tracer walk | Personnel, light vehicles, trench lines |
| M60D Door Gun (port / starboard) | 7.62mm ball/tracer | 500 m practical | Wagon wheel orbit; close escort | Personnel, light vehicles, flanking targets |
| M156 WP | White phosphorus | 1,000 m (marking) | Level fire or diving fire | Target marking, obscurant |
| M257 Illumination | Parachute flare | Deploy at 600–800 m range | Level fire, slight elevation | Night area illumination |

---

### QRC-2: Danger Close Distances

| Weapon | Danger Close Distance |
|---|---|
| 2.75-inch FFAR M151/M229 HE | 230 meters from friendly forces |
| M156 WP | 300 meters from friendly forces |
| M134 Minigun (7.62mm) | 200 meters from friendly forces |
| M60D Door Gun (7.62mm) | 200 meters from friendly forces |

---

### QRC-3: Ballistic Depression Quick Reference (M151 HE, sea level, still air)

| Airspeed (KIAS) | Range (m) | Level Fire Depression (mils) | 10° Dive Depression (mils) |
|---|---|---|---|
| 60 | 500 | 32 | — |
| 60 | 800 | 38 | — |
| 80 | 600 | 28 | 20 |
| 80 | 800 | 35 | 26 |
| 80 | 1,000 | 41 | 32 |
| 100 | 800 | 32 | 22 |
| 100 | 1,000 | 38 | 28 |
| 100 | 1,200 | 40 | 34 |

---

### QRC-4: Attack Run Parameters

| Profile | Entry Alt (ft AGL) | Attack Airspeed (KIAS) | Dive Angle | Min Release Alt (ft AGL) |
|---|---|---|---|---|
| Level / Running | 50–300 | 60–100 | 0–5° | Same as entry |
| Diving (10°) | 800–1,500 | 80–100 | 10° | 300 |
| Diving (20°) | 1,000–1,500 | 80–100 | 20° | 500 |
| Wagon Wheel (orbit) | 500–1,200 | 60–80 (orbit) / 80 (attack arc) | 10–15° (attack arc) | 300 |
| Hover Fire | 10–50 | 0 | 0° | N/A — break off immediately after fire |

---

### QRC-5: Arming Checklist (Memory Aid)

**WEAPONS HOT:**
1. Selector — SET (ROCKETS / GUNS / BOTH)
2. Mode — SET (SINGLE / PAIRS)
3. Guard — LIFT
4. Master Arm — ARM
5. Panel — SCAN (verify)
6. Crew — "WEAPONS HOT"

**WEAPONS SAFE:**
1. Trigger — RELEASE
2. Master Arm — SAFE
3. Guard — LOWER
4. Selector — SAFE
5. Crew — "WEAPONS SAFE"

---

*Based on DCS UH-1H Belsimtek/Eagle Dynamics module documentation, TM 55-1520-210-10, FM 3-04.140, ATP 3-04.1, and TC 1-237. For simulation training use only. Not for use in actual aircraft operations.*
