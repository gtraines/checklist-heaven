Act as an expert U.S. Army UH-1H "Huey" gunship pilot, attack helicopter tactics instructor, and DCS World subject-matter expert, cross-referencing real-world U.S. Army technical manuals with DCS simulation documentation. I need you to compile a detailed research dossier for a **UH-1H Huey Weapons Employment Course**.

**Objective:**
Create a comprehensive technical reference document covering the employment of all weapons and systems available on the DCS UH-1H Huey module (Belsimtek / Eagle Dynamics). This research will be used to build a multi-event training course with structured exercises and grading criteria. The student has already completed the UH-1H BQT course and is fully proficient in basic flight operations, startup/shutdown, hover, navigation, traffic patterns, autorotation, and emergency procedures.

This is a **pure unguided-weapons platform** — no laser designators, no targeting pods, no precision-guided munitions (no Hellfire, no APKWS). All weapons delivery is visual/optical. The student must master ballistic fundamentals, aiming techniques using the AN/M2A1 optical sight, attack profiles, and crew coordination with door gunners. This is fundamentally different from a glass-cockpit attack helicopter course and should be treated as such.

---

**DCS Module Context:**
The DCS UH-1H Huey (Belsimtek / Eagle Dynamics) is a **full-fidelity, clickable-cockpit module**:
- **Fully interactive analog cockpit** — every switch, circuit breaker, and dial is clickable. No MFDs, no digital weapons management display, no CCIP pipper on a screen. Weapons are selected and managed through the physical armament panel.
- **Weapons stations:** Two forward stub-wing pylons (left and right) for rockets or minigun pods, plus two aft crew door gun stations (port and starboard). Not all stations are always occupied — loadout varies by mission.
- **Sight system:** The AN/M2A1 optical sight (or equivalent deflection sight) provides aiming reference for rockets and forward-firing weapons. This is a basic graduated optical sight — NOT a radar or laser-coupled CCIP system. Accurate delivery requires the pilot to understand ballistics, set the correct depression angle, and fly precise airspeed and dive parameters.
- **No onboard targeting sensor.** Target identification and acquisition are entirely visual. There is no FLIR, no TV camera, no laser rangefinder. The pilot must positively identify targets using the naked eye or binoculars before engaging.
- **Crew coordination is critical.** In single-player DCS, the player can switch to the door gunner positions. In multiplayer, dedicated crew members operate the door guns. The pilot and gunners must coordinate calls, sectors of fire, and engagement sequences.
- **DCS weapons keybinds:** Many armament functions use the cockpit panel; some have keyboard shortcuts. Document both the physical cockpit switch location and the keyboard shortcut (if it exists).

---

**Source Material Priority:**
1. **Primary (Simulation Truth):** Official DCS UH-1H Belsimtek module documentation and actual in-game behavior. When the simulation contradicts real-world procedures, **the sim wins** — document the DCS procedure as primary instruction.
2. **Secondary (Realism Context):** Real-world U.S. Army documentation:
   - *TM 55-1520-210-10 (Operator's Manual, UH-1H/V)* — primary aircraft and weapons system reference.
   - *TM 55-1520-210-CL (Operator's and Crewmember's Checklist)* — weapons arming and employment procedures.
   - *TM 9-1055-476-13&P* — M158/M159 2.75-inch rocket launcher technical manual.
   - *TM 9-1055-473-10* — XM-158 and XM-159 launcher operator's manual.
   - *TM 9-1340-222-10 series* — 2.75-inch Folding Fin Aerial Rocket (FFAR) technical manuals.
   - *TM 9-1005-224-10* — M134 Minigun operator's manual (if applicable to the module loadout).
   - *TM 9-1005-298-14&P* — M60D Machine Gun operator and maintenance manual.
   - *TC 1-237 (Aircrew Training Manual — Utility & Observation Helicopter)* — crew training standards.
   - *FM 3-04.140 (Helicopter Gunnery)* — helicopter weapons employment doctrine, attack profiles, target acquisition, ballistic data.
   - *FM 1-240 (Utility and Cargo Helicopter Operations)* — UH-1 tactical employment doctrine.
   - *ATP 3-04.1 (Aviation Tactical Employment)* — close combat attack (CCA) doctrine and procedures.
   - Vietnam-era USAARL (U.S. Army Aviation and Missile Research) technical reports on UH-1C/H gunship gunnery — publicly available via DTIC; highly relevant historical gunnery data.
3. **Conflict Resolution:** When a real-world procedure conflicts with DCS, document the **DCS procedure** as the primary instruction and add a clearly marked footnote:
   > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

---

**Required Research Modules:**

---

**Module 1: Weapons Systems Overview & Cockpit Armament Switchology**
- **Weapons available in the DCS UH-1H (full inventory table):**
  - XM-158 7-tube 2.75-inch FFAR launcher (forward-firing rockets)
  - XM-159 19-tube 2.75-inch FFAR launcher (forward-firing rockets)
  - M134 7.62mm Minigun pod (if modeled as a selectable loadout)
  - M60D 7.62mm Door Gun (port and starboard crew stations)
  - Available rocket warhead variants (M151 HE, M229 HE, M156 WP, M257 Illumination, flechette — document which are modeled in DCS vs. which are real-world-only knowledge)
- **Pylon/station configuration:**
  - Station identification: Left pylon, Right pylon, Port door station, Starboard door station.
  - Maximum load per pylon (weight limit; effect on performance — hover ceiling, Vne margin, climb rate).
  - Compatible weapons per station.
  - Typical combat loadout configurations: rockets-only, minigun + rockets (mixed), door guns only, full gunship.
  - Effect of asymmetric loadout on handling (torque, trim requirements).
- **Cockpit Armament Panel — complete description:**
  - Panel location in the cockpit (right subpanel area; describe exact location with reference to adjacent panels).
  - Master Arm switch: location, positions (SAFE / ARM), safety wire/guard if applicable.
  - Weapon select switches: rockets (ROCKETS position), miniguns (MINIGUNS / GUNS position), simultaneous select.
  - Firing mode: SINGLE / PAIRS / RIPPLE — describe what is modeled in DCS vs. what is the real aircraft.
  - Intervalometer / salvo setting (if modeled): number of rockets per trigger pull.
  - Jettison panel: location, emergency stores jettison procedure.
- **Pilot weapons controls on cyclic/collective:**
  - Weapons release / fire trigger: location on cyclic stick; which button fires rockets vs. guns.
  - Cyclic trigger: primary weapons fire.
  - Weapon safe: how pilot safes weapons from the cockpit without going to the armament panel.
  - Force trim and weapons fire interaction (is force trim release required before firing?).
- **DCS keyboard/HOTAS reference for all weapons functions** (document the default keybind for each function and the corresponding cockpit control).
- **Pre-engagement arming checklist** (complete switch-by-switch sequence from cold-panel to weapons hot).
- **Weapons safe sequence** (post-engagement or mission abort; de-arm sequence).
- **Common student errors in weapons switchology.**

---

**Module 2: Sight Systems & Target Acquisition**
- **AN/M2A1 Optical Sight (or equivalent — identify the exact sight modeled in DCS UH-1H):**
  - Sight type: describe whether it is a fixed-reticle ring-and-bead sight, a depression sight (with angular adjustment), or a computing sight.
  - Reticle design: mil marks, depression scale, range marks — describe what the student actually sees through the sight in DCS.
  - Sight mounting location in the cockpit: which panel/windscreen area; where the pilot positions their head to use it.
  - Depression/elevation adjustment: how to set the sight angle for different airspeed/range profiles (if adjustable). If fixed, describe the fixed angle and what it is calibrated for.
  - Lead angle computation: how the sight accounts (or does not account) for forward motion and target offset.
  - Relation to ballistic tables: the sight angle must match the airspeed and range to produce accurate rocket impact. Describe the relationship.
- **Visual target acquisition without sensors:**
  - Naked-eye scanning technique from the cockpit: horizon scanning, ground scanning, sector assignment.
  - Distance estimation methods: angular size of known objects (vehicles, structures), terrain features.
  - Target identification criteria: confirming target type before engagement (positive ID requirement).
  - Threat recognition in DCS: common target types (armor, trucks, AAA, troops) and their visual signatures.
  - Acquisition from altitude vs. low-level: tradeoffs (visibility range vs. threat exposure).
  - Scanning while flying: maintaining situational awareness and aircraft control while acquiring targets.
- **Coordination with door gunners for target designation:**
  - Door gunner call format: direction (o'clock), distance (meters/feet), description, marking (if used).
  - Pilot acknowledgment and target pickup.
  - Example: *"Pilot, right door — 3 o'clock, 800 meters, truck convoy, north side of road."*
- **WP marking rockets for target identification:**
  - Using M156 WP rounds as target markers.
  - Call format when using WP for CCA: *"Smoke is out"* / *"Mark is on the target"*.
  - Spotting WP impact and adjusting.
- **Danger Close ranges:**
  - Minimum safe employment ranges by weapon type (rockets, miniguns, door guns) for friendly troop proximity.
  - Real-world standard: document the danger close distances and whether DCS models fragmentation/splash.
- **Common student errors in target acquisition.**

---

**Module 3: 2.75-Inch FFAR Rocket Employment**
- **Rocket system description:**
  - 2.75-inch Folding Fin Aerial Rocket (FFAR): motor, fusing, folding-fin deployment sequence.
  - XM-158 (7-tube) launcher: tube arrangement, loading sequence, ripple fire capability.
  - XM-159 (19-tube) launcher: tube arrangement, preferred for area suppression missions.
  - Rocket motor performance: time to reach effective range, burnout time, max effective range, max range.
  - Fuzing options by warhead type: point detonating (PD), delay, proximity (if applicable in DCS).
- **Available warheads (DCS) — full data table for each:**
  - M151 HE (High Explosive, 10 lb): burst radius, lethal radius, best targets.
  - M229 HE (High Explosive, 17 lb): burst radius, lethal radius, best targets.
  - M156 WP (White Phosphorus): smoke duration, marking use, incendiary use.
  - M257 Illumination: burn time, altitude for employment, candlepower, night use.
  - Flechette/APERS dart warhead (if available in DCS): dart spread pattern, anti-personnel use.
  - For each: document which warheads are modeled in DCS with effects vs. which are real-world knowledge only.
- **Ballistics data table (real-world TM data; document any DCS differences):**
  - For each standard attack airspeed (60, 80, 100 KIAS) and dive angle (0°, 5°, 10°, 15°, 20°):
    - Slant range at release.
    - Depression angle setting.
    - Expected impact point relative to aim point.
    - Time of flight.
  - Density altitude correction factors (if applicable to DCS model).
  - Wind correction (crosswind, headwind/tailwind): procedure for adjusting aim point.
- **Employment profiles:**
  - **Diving attack (primary accurate profile):** recommended dive angle range (10–20°); airspeed (80–100 KIAS); release altitude (minimum/optimum); slant range at release; pull-off procedure and minimum recovery altitude. Step-by-step cockpit procedure.
  - **Running/level fire:** level or shallow (<5°) flight; primary for area suppression; accuracy degraded; when to use. Step-by-step cockpit procedure.
  - **Circling / Wagon Wheel (orbiting fire):** helicopter orbits the target at a set range and bearing; fires during the inbound portion of the orbit; provides sustained fire while maintaining standoff. Describe orbit radius, airspeed, dive angle, and coordination between pilot and door gunners during the wagon wheel. Step-by-step cockpit procedure.
  - **Hover fire:** close range; high accuracy from stable platform; extreme crew exposure risk; use only when no other profile is feasible. Step-by-step cockpit procedure.
- **Attack run parameters — master table:**
  - Entry altitude, entry airspeed, dive angle, release range, release altitude, pull-off altitude for each profile.
  - Recovery maneuver (break-off): direction, G-loading, minimum altitude before break.
  - Re-attack considerations: safe direction for re-entry; altitude for re-engagement.
- **Salvo vs. single-round employment:**
  - Single: precision engagement, specific target, ammunition conservation.
  - Pairs: increased hit probability for area/point target; moderate ammo expenditure.
  - Full pod: maximum area suppression; all remaining rounds in rapid sequence; high ammunition expenditure.
  - Mission planning: ammunition allocation per target type.
- **Ripple fire technique:**
  - Multiple engagements on a target complex: walk the impact point across the target area.
  - Time between trigger actuations for walking fire.
- **Common student errors with rockets.**

---

**Module 4: M134 Minigun Pod Employment (if available as loadout in DCS)**
- **System overview:**
  - M134 7.62×51mm NATO, 6-barrel rotating breech, electrically driven.
  - Rate of fire options in DCS (if selectable): 2,000 RPM or 4,000 RPM.
  - Pod mounting: left pylon, right pylon, or both — document what DCS allows.
  - Ammunition capacity per pod in DCS.
  - Tracer-to-ball ratio: identifies for the student how often a tracer appears in the stream.
- **Sight use for minigun:**
  - Depression and lead angle calculations for minigun (different from rockets — shorter range, flatter trajectory).
  - Tracer walk: the student walks tracers onto target; describe the technique.
  - Burst length: optimal burst duration; overheating or depletion risk.
- **Employment profiles:**
  - **Diving fire:** 5–15° dive; 60–100 KIAS; 300–800 m slant range; primary accuracy profile.
  - **Running/level fire:** level flight at low altitude; useful for strafing along a tree line or road.
  - **Circling fire:** as part of the wagon wheel orbit; minigun firing during inbound arc.
  - **Hover fire:** stationary; extreme close range (< 300 m); maximum accuracy; maximum exposure.
- **Aiming technique — walking tracers:**
  - How to walk the tracer stream from a known reference onto the target.
  - Adjustment calls: "short," "right," "on target" — self-commentary for training discipline.
- **Recoil effects:**
  - Minigun pod recoil affects aircraft heading and attitude — describe the effect and required compensation (pedal, cyclic, trim).
  - Asymmetric fire (one pod only): yaw tendency; correction.
- **Ammunition management:**
  - Round count display (if modeled in DCS).
  - Estimated rounds remaining by fire duration at 2,000 RPM and 4,000 RPM.
  - Conservation discipline: short bursts; high target value = more rounds; suppression = shorter bursts.
- **M134 vs. door gun tradeoffs:**
  - M134 (forward-firing, fixed): high rate of fire; pilot-aimed; no side/rear coverage.
  - M60D (door gun, flexible): crew-aimed; covers flanks and rear; lower rate of fire.
  - Mission selection: when to carry which combination.
- **Common student errors with minigun pod.**

---

**Module 5: M60D Door Gun Employment (Crew Stations)**
- **System overview:**
  - M60D 7.62×51mm NATO, single-barrel, gas-operated, air-cooled machine gun.
  - Door gun mount: pintle/swivel mount in the port (left) and starboard (right) door openings.
  - Traverse range: azimuth (fore/aft limit stops) and elevation limits — describe in degrees.
  - Rate of fire: ~550 RPM cyclic.
  - Feed from disintegrating belt (200–400 round standard load per gun in Vietnam-era use).
  - Tracer ratio in standard military 7.62mm ammunition.
- **DCS crew station operation:**
  - How to switch from the pilot seat to the port or starboard door gun position in DCS (keybind / station number).
  - View from each door gun station: describe the field of view and the control interface in DCS.
  - Door gun azimuth and elevation controls in DCS: how the player aims (mouse, joystick slew, etc.).
  - Trigger: fire button at the crew station.
  - DCS limitations vs. real-world: what is and is not modeled (reloading, barrel change, stoppages).
- **Gunner technique:**
  - Leading a moving target: forward lead estimate for ground vehicles (speed × angular lead).
  - Walking tracers onto target: start behind, walk forward.
  - Burst discipline: 5–7 round bursts for point targets; longer bursts for area suppression.
  - Sector discipline: each gunner has a sector of responsibility; do not cross into the other gunner's sector without coordination.
- **Crew coordination — pilot and gunners:**
  - Pilot calls before maneuvering: *"Coming left"* / *"Coming right"* / *"Diving in"* — warn gunners before attitude changes.
  - Gunner target call: direction, distance, description, recommended engagement decision.
  - Engagement authorization: pilot authorizes engagement or designates targets; gunner fires on pilot authorization (or when pilot calls "engage at will").
  - Cease fire: *"Cease fire, cease fire"* — immediate stop; all crew acknowledges.
  - Friendly forces awareness: gunner confirms target is NOT friendly before firing; "no joy" call if uncertain.
- **Wagon Wheel / Orbiting fire with door guns:**
  - Pilot establishes a right-hand orbit around the target at ~400–600 m radius.
  - During the inbound arc (target on the right side), the starboard door gunner has the target.
  - During the outbound arc (target on the left), the port door gunner may have opportunity.
  - Pilot calls: *"Engaging right"* / *"Target is on your side"* to alert the appropriate gunner.
  - Coordination between pilot firing rockets/miniguns and gunners firing simultaneously (or in sequence).
- **Door gun employment vs. ground troop proximity:**
  - M60D fragmentation danger close: minimum safe distance to friendly forces.
  - Positive identification requirement before fire.
  - Stop-fire authority: any crew member can call cease fire; pilot has final authority.
- **Common student errors with door gun employment.**

---

**Module 6: Attack Profiles & Gunnery Patterns**
- **The wagon wheel / rocket run orbit (the primary UH-1H attack formation):**
  - Describe the complete wagon wheel pattern: orbit altitude, airspeed, radius, entry and exit.
  - Roll-in point: where in the orbit the pilot rolls into the attack dive.
  - Attack parameters: dive angle, airspeed at release, range at release.
  - Pull-off: break direction, G-loading, recovery altitude.
  - Re-attack: climbing back to orbit altitude, re-entering the pattern.
  - Ammunition tracking during successive passes.
  - When to abort a pass: target obscured, too low, too fast, too slow, friendly forces in impact zone.
- **Standard UH-1H attack profiles (full parameter table for each):**
  - **High Hover Attack:** from stationary hover at altitude; weapons firing into targets below; primarily used for suppressive fire in LZ prep.
  - **Running Fire (level):** low-level approach to target; fire while in level flight; pull off over or past target; use for area suppression.
  - **Diving Attack (primary):** roll-in from altitude; 10–20° dive; fire rockets or guns; pull off; re-enter orbit. This is the most accurate and most dangerous profile — balance accuracy against exposure time.
  - **Circling / Wagon Wheel:** continuous orbit with successive passes by each helicopter in a flight; provides sustained fire while minimizing single aircraft exposure.
  - For each profile: entry altitude, entry airspeed, dive angle (if applicable), release/fire range, pull-off altitude, recovery airspeed, re-attack time.
- **Multi-ship attack coordination:**
  - Trail attack: two or more aircraft in trail; one aircraft attacks while the other covers; lead calls "breaking" and trail calls "in."
  - Echelon attack: aircraft offset to allow simultaneous roll-in on a linear target.
  - Firing order, separation, and mutual support doctrine.
  - Communication format for multi-ship attack (who calls "in," "off," "splash").
- **LZ preparation (LZ Prep):**
  - Describe the UH-1H's role in preparing a landing zone before troop-carrying slicks land.
  - Attack sequence: how many passes, which weapons, coverage area.
  - Coordination with the flight of slicks: timing the prep so troops arrive immediately after the last fire pass.
  - Communications with the flight lead and slick flight.
- **Immediate action on abort criteria:**
  - When to abort an attack run: obscured target, friendly proximity, aircraft parameters out of limits, weapons malfunction.
  - Abort call format and procedure.
- **Post-attack procedures:**
  - Battle Damage Assessment (BDA): visual assessment after the attack run; what to look for.
  - Reporting: BDA format — number of rounds expended, observed effects, target status.
  - Re-engagement decision: continue the attack or disengage.
- **Common student errors in attack profiles.**

---

**Module 7: Close Combat Attack (CCA) & Fire Support Integration**
- **CCA doctrine overview:**
  - Definition: CCA is attack helicopter fires delivered in close proximity to friendly forces.
  - Differs from CAS (Close Air Support) in that CCA is organic to the ground force's aviation assets — no JTAC/FAC required, but positive identification and coordination are still mandatory.
  - CCA vs. CAS: key doctrinal distinction that the student must understand (reference ATP 3-04.1 and FM 3-04.126 if applicable).
- **Fire request formats:**
  - Ground commander's request for helicopter fire support: how the request is formatted and transmitted to the helicopter flight lead.
  - Minimum information required: target location (grid or talk-on), target description, friendly force location (minimum distance to target), remarks/restrictions.
- **Target location methods:**
  - Grid coordinate: MGRS or lat/long; student must be able to mark a grid on a map and fly to the area.
  - Talk-on: ground or air controller verbally guides the helicopter to the target using visual references, headings, and distances.
  - Laser pointer (if applicable in DCS): ground unit illuminates target with IR laser pointer visible through NVG.
  - WP smoke marking: ground unit pops smoke on or near the target; helicopter crew identifies smoke; controller confirms color.
- **Attack coordination with ground forces:**
  - Safety brief: pilot briefs the ground controller on the attack direction, weapons to be used, and abort criteria.
  - Run-in heading: pilot announces the direction of the attack pass so ground forces can anticipate shell and fragmentation hazard direction.
  - "Cleared hot": ground commander or controller authorizes the attack.
  - "Abort, abort": immediate cease-fire; pilot or controller may call abort at any time.
- **ROE and positive identification:**
  - Positive identification requirement before any weapon employment.
  - Procedure when target identity is uncertain: challenge, abort, re-identify.
  - Friendly force marking: smoke, panels, IR strobes — what each looks like and how to confirm.
- **DCS mission integration:**
  - How to use the DCS radio menu and AI ground units to simulate CCA fire requests in single-player.
  - Using DCS F10 map for target grid extraction.
  - Multiplayer: communication with ground force players using SRS or in-game comms.
- **Common student errors in CCA execution.**

---

**Module 8: Weapons Loading, Weight & Performance**
- **Loadout configurations — performance impact table:**
  - For each standard loadout (clean, 2× XM-158, 2× XM-159, 2× minigun pods, mixed rocket + minigun, full gunship), document:
    - Loaded weight (approximate, based on TM data + DCS behavior).
    - Effect on hover ceiling (IGE and OGE) at sea level vs. 3,000 ft density altitude.
    - Effect on Vne margin (does the loaded aircraft reach Vne more easily?).
    - Effect on autorotation (heavier = faster descent rate = less margin on collective pull).
    - Effect on maneuverability (roll rate, yaw response).
  - Decision guidance: what loadout to choose based on mission type and density altitude.
- **Density altitude planning:**
  - How density altitude affects weapons delivery (same airspeed at high DA = more indicated airspeed required; engine power reduced = less margin for attack profiles).
  - Power check procedure with weapons loaded: hover check before departure to verify power margin.
- **Emergency jettison:**
  - When to jettison: system malfunction, emergency landing required, weight exceeds limits.
  - Jettison panel location; sequence (which stations first if selective jettison; all-stations for emergency).
  - Post-jettison checks: verify release, handling qualities without stores.
  - DCS modeling of jettison (does DCS UH-1H model individual station jettison vs. all-station? Document what is actually modeled).
- **Asymmetric stores:**
  - If one pylon jettisons or one launcher misfires, the aircraft flies asymmetrically loaded.
  - Handling technique: trim requirements, cyclic position, airspeed restrictions.
  - Landing with asymmetric stores: technique for landing with one pylon loaded and one empty.

---

**Module 9: Night and Reduced Visibility Weapons Employment**
- **NVG (Night Vision Goggle) operations — UH-1H context:**
  - Real-world NVG configuration for UH-1H gunship crews (AN/AVS-6 or AN/PVS-14 monoculars).
  - DCS NVG mode: how to activate, field of view, limitations vs. real NVG.
  - Cockpit lighting for NVG compatibility: what to turn off or reduce; NVG-compatible instrument lighting.
  - Weapons delivery on NVG: how sight picture changes; tracer visibility on NVG; WP marking visibility.
- **Illumination rocket employment:**
  - M257 illumination rocket: burn time, deployment altitude, candlepower, drift (wind effect).
  - Employment procedure: fire at correct altitude and range so the parachute flare deploys at the optimum illumination altitude.
  - Target illumination for door gunner / ground forces.
  - Coordination: announce illumination round time-of-flight before firing so crews know when to expect light.
- **WP marking at night:**
  - M156 WP visibility at night vs. day.
  - Using WP to identify target for follow-on attack.
- **Reduced visibility attack considerations:**
  - Fog, smoke, and haze effect on target acquisition range.
  - Minimum visibility requirements for attack profile entry (when to abort due to obscurement).
  - Flare employment in DCS and its limitations.

---

**Module 10: Weapons Malfunctions & Procedures**
- **Common malfunction types:**
  - Hangfire: rocket ignites but does not leave the tube (real-world hazard); DCS behavior.
  - Misfire: no ignition; procedure (safe weapons, wait period, inspect).
  - Tube jam (rocket stuck in tube): real-world; DCS behavior.
  - Minigun stoppage: ammunition jam or electrical malfunction; clearing procedure.
  - Door gun stoppage: M60D malfunction procedures (immediate action: SPORTS — Slap, Pull, Observe, Release, Tap, Shoot).
- **Hung store (rocket that did not fire but tube occupied):**
  - Real-world procedure: safe weapons; land; do not exit aircraft toward tubes without proper clearance.
  - DCS equivalent if modeled.
- **Electrical failure and weapons:**
  - Generator failure effect on weapons system.
  - Battery-only operation: which weapons systems remain powered on battery.
  - Procedure for safing weapons before/during electrical emergency.
- **Unsafe weapons indications:**
  - Master Arm light fails to indicate safe.
  - Armament panel switch failures.
  - Procedure: assume weapons are hot; don't point at friendly forces; land and inspect.
- **DCS malfunction modeling:**
  - Document which of the above malfunctions are modeled in DCS vs. which are academic-only knowledge.
  - How to trigger malfunctions in DCS (Mission Editor failures) for training use.
- **Common student errors in malfunction procedures.**

---

**Appendix: DCS UH-1H Weapons Keybind Reference**
Compile a complete table of all DCS UH-1H weapons-related key binds, using the following format:

| Function | Default Keybind | Cockpit Location | Notes |
|---|---|---|---|
| Master Arm ON/OFF | [bind] | Armament panel | |
| Rockets fire | [bind] | Cyclic trigger | |
| Select rockets | [bind] | Armament panel | |
| Select miniguns | [bind] | Armament panel | |
| Rocket salvo: single | [bind] | Armament panel | |
| Rocket salvo: pairs | [bind] | Armament panel | |
| Emergency jettison | [bind] | Jettison panel | |
| Switch to port door gun station | [bind] | View/seat change | |
| Switch to starboard door gun station | [bind] | View/seat change | |
| Door gun fire | [bind] | Crew station trigger | |
| Sight depression adjust (if applicable) | [bind] | Sight control | |

---

**Output Format Requirements:**

Structure the dossier as a Markdown document with the following formatting:

1. **Module headings** use `## Module N: Title`.
2. **Sub-section headings** use `### N.N Title`.
3. **Data tables** use the `| Column | Column |` pipe format with a separator row.
4. **Step-by-step procedures** use numbered lists.
5. **Realism divergence notes** use the blockquote format: `> *⚠ Realism Divergence: ...*`
6. **Key terms on first use** should be **bolded**.
7. **DCS keyboard shortcuts** must be formatted as inline code: `` `LShift + Home` ``.
8. **"Common student errors"** section at the end of every module — formatted as a table with two columns: *Error* and *Correction*.
9. **Instructor notes** interspersed where relevant — practical teaching guidance, not just raw data.

At the end of the document, include a one-page **Quick Reference Card** formatted as a table summarizing: weapon, warhead options, max effective range, primary attack profile, and primary target type.

The dossier should be written at the level of an actual Army aviation training circular — authoritative, specific, and directly usable as source material for generating training events. Avoid vague language ("approximately" should be replaced with actual values from the TMs wherever possible). If a value is uncertain or varies by edition of the TM, state the range and cite the source.
