Act as an expert US Army OH-58D Kiowa Warrior weapons officer, aerial scout, and DCS World mission planner, cross-referencing real-world Army technical manuals with DCS simulation documentation. I need you to compile a detailed research dossier for an **OH-58D Kiowa Warrior Weapons Employment Course**.

**Objective:**
Create a comprehensive technical reference document covering the employment of all weapons and sensor systems available on the DCS OH-58D Kiowa Warrior module. This research will be used to build a multi-event training course with structured exercises and grading criteria. The student has already completed the OH-58D BQT course and is proficient in basic flight operations, startup/shutdown, hover, navigation, traffic patterns, autorotation, and emergency procedures.

**DCS Module Context:**
The DCS OH-58D Kiowa Warrior is a **full-fidelity, clickable-cockpit module** by Polychop Simulations:
- **Fully interactive cockpit** — all systems operated via mouse-clickable switches, MFD pages, and HOTAS controls.
- **Mast Mounted Sight (MMS)** — the primary sensor and targeting system, housing TV (day camera), Thermal Imaging Sensor (TIS/FLIR), Laser Rangefinder/Designator (LRF/D), and boresight capability. The MMS is mounted above the rotor disc, allowing the aircraft to remain hull-down behind terrain while the sight observes and designates targets.
- **Weapons managed through MFD weapons pages** — weapon selection, quantity, laser code (PRF), and delivery mode are configured via the multifunction displays. There is no centralized stores management system like the A-10C's DSMS.
- **Universal Weapons Pylons (UWP)** — two pylons (left and right) that can carry AGM-114 Hellfire missiles (2 per pylon), M260 7-tube rocket launchers, or the M3P .50 caliber machine gun pod. Loadout is mixed based on mission requirements.
- **FADEC-controlled T703-AD-700A engine** (~650 SHP) — the OH-58D is a power-limited, single-engine platform. Weapons loadout directly impacts hover ceiling, rate of climb, and maneuvering performance. Weight management is a critical tactical consideration.
- **Advanced Flight Model (AFM)** — rotor aerodynamics, retreating blade stall, LTE, settling with power, translational lift, weapon recoil effects, and stores drag are realistically modeled.

**Source Material Prioritization:**
1. **Primary (Simulation Truth):** Official DCS OH-58D documentation (Polychop module manual) and actual in-game behavior. When the sim contradicts real-world procedures, **the sim wins** — document the DCS procedure as primary instruction.
2. **Secondary (Realism Context):** Real-world US Army documentation:
   - *TM 1-1520-248-10* (OH-58D Operator's Manual)
   - *TM 1-1520-248-CL* (OH-58D Operator's Checklist)
   - *TC 1-211* (Aircrew Training Manual — Attack Helicopter)
   - *TC 1-237* (Aircrew Training Manual — Utility & Observation Helicopter)
   - *FM 3-04.126* (Attack Reconnaissance Helicopter Operations)
   - *FM 3-04.140* (Helicopter Gunnery)
   - *ATP 3-04.1* (Aviation Tactical Employment)
   - *ATTP 3-06.1* (Aviation Urban Operations)
   - *STP 1-15OH24-SM-TG* (OH-58D Soldier's Manual / Trainer's Guide)
   - AGM-114 Hellfire technical manuals (TM 9-1425-484-12 series)
   - Hydra 70 rocket system technical manuals
3. **Conflict Resolution:** When a real-world procedure conflicts with DCS, document the **DCS procedure** as the primary instruction and add a clearly marked footnote:
   > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

**Required Research Modules:**

---

**Module 1: MMS (Mast Mounted Sight) Operations & Targeting**
- **MMS Architecture:**
  - Sensor suite: TV (day camera), TIS/FLIR (thermal), LRF/D (laser rangefinder/designator).
  - Mast-mounted position: enables hull-down observation and designation while fuselage remains masked by terrain.
  - MMS field of regard: azimuth and elevation limits; gimbal stops.
  - MMS slew rates and tracking modes.
- **MMS Power-On & Alignment:**
  - MMS switch positions and warm-up sequence.
  - Boresight procedures: ground and air boresight, verification.
  - MFD MMS page layout: video imagery, symbology overlays, OSB functions.
- **Sensor Modes:**
  - TV (Day Camera): daytime target identification; FOV (narrow/wide); zoom levels.
  - TIS/FLIR (Thermal): polarity (white-hot/black-hot); gain/level adjustment; FOV (narrow/wide).
  - Automatic/manual sensor switching; when to use each sensor.
  - Unified vs. independent sensor pointing.
- **MMS Controls:**
  - Slew: HOTAS slew control mapping; slew rate (fine/coarse).
  - FOV: toggle narrow/wide; zoom levels per sensor.
  - Polarity: switching FLIR polarity.
  - Track modes: point track, area track, inertial; when and how to use each.
  - Stow/unstow procedures and auto-stow behavior.
- **Laser Operations:**
  - LRF (Laser Rangefinder): single-pulse ranging; range readout on MFD.
  - LRD (Laser Designator): continuous lasing for Hellfire/APKWS terminal guidance.
  - Laser code (PRF code): setting the 4-digit pulse repetition frequency code on MFD (default code, code coordination with other assets).
  - Laser safety: arm/safe sequencing; laser status indications.
  - Self-designation vs. buddy lasing: procedures for designating for own weapons vs. designating for wingman/Apache/fixed-wing.
  - Lasing timeline: when to initiate lase relative to missile/rocket time of flight.
- **Target Acquisition Workflow:**
  - Systematic search patterns: sector scan, area scan, point-to-point.
  - Target detection → identification → classification → engagement decision.
  - Range estimation: laser range vs. map range vs. MFD cursor range.
  - Grid coordinate extraction from MMS for reporting and CAS coordination.
  - Battle Damage Assessment (BDA) using MMS post-strike.
- **Common student errors with MMS.**

---

**Module 2: Weapons Management System & HUD Symbology**
- **Weapons MFD Pages:**
  - Accessing the weapons page on MFD.
  - Weapons inventory display: loaded stations, quantities, weapon types.
  - Weapon selection: cycling between Hellfire, rockets, gun.
  - Weapon-specific sub-pages: Hellfire setup, rocket setup, gun setup.
  - Laser code (PRF) assignment per weapon.
- **Master Arm & Arming Sequence:**
  - Master Arm switch location and positions (SAFE / ARM).
  - Arming sequence: Master Arm → weapon select → mode select → constraints check → fire.
  - Emergency jettison: stores jettison procedure and panel location.
  - Weapon safe procedures post-engagement.
- **HUD / MFD Weapons Symbology:**
  - Hellfire symbology: seeker status, lock-on indications (LOBL/LOAL), launch constraints, time of flight.
  - Rocket symbology: CCIP reticle ("I-beam"), impact point calculation, range.
  - Gun symbology: CCIP pipper for .50 cal, bullet drop compensation.
  - Laser status indicators: armed, firing, code match.
  - Range bar / range readout behavior per weapon type.
- **Weapon Status Indications:**
  - Ready/not-ready indications per weapon.
  - Weapon BIT (Built-In Test) and status checks.
  - Hangfire / misfire indications and procedures.
- **Common student errors with weapons management.**

---

**Module 3: AGM-114 Hellfire Employment**
- **Missile Variants (DCS OH-58D):**
  - AGM-114K Hellfire II: Semi-Active Laser (SAL), tandem HEAT warhead — primary anti-armor.
  - AGM-114M Hellfire II: SAL, blast-fragmentation warhead — soft targets, structures, boats.
  - AGM-114N Hellfire II (MAC): SAL, thermobaric/metal augmented charge — bunkers, enclosed spaces.
  - AGM-114L Longbow Hellfire: note OH-58D limitations (no FCR — cannot self-designate for RF missile; availability and employment constraints in DCS).
- **Hellfire Guidance Modes:**
  - LOBL (Lock-On Before Launch): MMS acquires and laser-designates target; missile sees laser energy before launch; confirms lock; fire. Safest mode — missile confirms guidance before departing rail.
  - LOAL-DIR (Lock-On After Launch — Direct): missile launches on a direct trajectory toward the target area; acquires laser designation in flight. Used when LOS to target exists but lock cannot be confirmed pre-launch.
  - LOAL-LO (Lock-On After Launch — Low): missile launches on a low trajectory; acquires laser in flight. Used for shorter ranges or when terrain permits low flight path.
  - LOAL-HI (Lock-On After Launch — High): missile launches on a high loft trajectory; acquires laser at apogee or during descent. Used for long range or when terrain/obstacles require a high arc. Maximum standoff.
  - Mode selection on MFD: switching between LOBL/LOAL modes; when to use each.
- **Employment Sequence (Step-by-Step Cockpit Switchology):**
  - Pre-engagement: Master Arm ON → Hellfire selected → variant selected → PRF code verified → MMS on target → guidance mode selected.
  - LOBL: MMS lasing → lock-on confirmation (audio/visual) → constraints met → fire → maintain designation until impact.
  - LOAL: MMS aimed at target area → guidance mode selected (DIR/LO/HI) → fire → begin lasing at appropriate time based on time-of-flight → maintain designation until impact.
  - Post-shot: BDA via MMS → weapon status check → re-engage or safe.
- **Launch Envelopes:**
  - Minimum/maximum range per guidance mode (LOBL vs. LOAL-DIR/LO/HI).
  - Altitude constraints: minimum launch altitude AGL; maximum altitude.
  - Airspeed constraints: hover fire vs. running fire; maximum airspeed for launch.
  - Angle-off constraints: maximum angle between missile flight path and laser line-of-sight.
  - Terrain masking considerations: ensuring missile flight path clears obstacles.
- **Tactical Employment Techniques:**
  - Hull-down engagement: expose only MMS; designate and fire from behind terrain.
  - Running fire: engagement during lateral or forward movement.
  - Rapid engagement: minimizing exposure time — unmask, shoot, remask.
  - Ripple fire: engaging multiple targets sequentially; re-designation between shots.
  - Buddy designation: receiving laser from JTAC, FAC, wingman, or Apache; setting PRF code to match external designator. Communication flow: "Spot" / "Laser On" / "Rifle" / "Splash."
  - Remote designation for other shooters: OH-58D designates while Apache or fixed-wing fires.
- **Variant Selection Guide:**
  - K (HEAT): heavy armor (MBTs, IFVs), hardened bunkers.
  - M (Blast-Frag): soft targets, light vehicles, boats, troop concentrations, structures.
  - N (Thermobaric): bunkers, caves, buildings, enclosed fighting positions.
- **Weight & Performance Impact:**
  - 4x Hellfire load vs. 2x Hellfire + rockets: effect on MTOW, hover ceiling, power margin.
  - Mission planning: selecting loadout based on target set and performance requirements.
- **Common student errors with Hellfire.**

---

**Module 4: Hydra 70 Unguided Rocket Employment**
- **System Overview:**
  - M260 7-tube lightweight launcher.
  - Pylon mounting: left and/or right UWP.
  - Rocket motor: Mk 66 Mod 4 (common motor for all warheads).
- **Available Warheads (DCS):**
  - M151 HE (High Explosive): 10 lb warhead — anti-personnel, light vehicles, soft targets.
  - M229 HE (High Explosive): 17 lb warhead — heavier targets, structures.
  - M282 MPP (Multi-Purpose Penetrator): light armor, bunkers, material targets.
  - M156 WP (White Phosphorus): target marking, incendiary, screening smoke.
  - M257/M278 Illumination: battlefield illumination (overt/covert IR).
  - Flechette/APERS variants (if available in DCS).
- **CCIP Delivery System:**
  - The OH-58D provides a CCIP (Continuously Computed Impact Point) reticle ("I-beam") on the MFD/HUD for rocket delivery.
  - CCIP pipper behavior: how the impact point moves with aircraft attitude, airspeed, altitude, and wind.
  - Accuracy factors: range, dive angle, airspeed, wind, rotor wash effects.
- **Employment Profiles:**
  - **Diving Fire:** 10–20° dive angle; 1.5–3.0 km slant range; 80–100 KIAS. Primary accurate delivery method.
  - **Running Fire (Level):** shallow/level flight; reduced accuracy; used for area suppression.
  - **Hover Fire:** engagement from a stationary or near-stationary hover; close-range; high exposure risk.
  - Recommended entry parameters: altitude, airspeed, dive angle per profile.
  - Recovery/break-off: minimum altitude and range; pull-off maneuver.
- **Weapons Page Setup:**
  - Rocket type/warhead selection.
  - Quantity per salvo: single, pairs, or full pod.
  - Inventory tracking on MFD.
  - Fuzing considerations per warhead type.
- **Warhead Selection Guide:**
  - M151 HE: troops in the open, trucks, soft targets.
  - M229 HE: structures, heavier material targets.
  - M282 MPP: light armor, bunkers, hardened targets.
  - M156 WP: marking for CCA coordination ("Mark on my smoke"), incendiary.
  - Illumination: night operations support.
- **Dispersion & Accuracy:**
  - Expected dispersion pattern at various ranges.
  - Factors affecting accuracy: range, altitude, airspeed, wind, G-loading, rotor vibration.
  - Techniques for improving accuracy: stable platform, consistent parameters, proper trim.
- **Common student errors with rockets.**

---

**Module 5: APKWS (Advanced Precision Kill Weapon System / AGR-20A)**
- **System Overview:**
  - Laser-guided Hydra 70 rocket with WGU-59/B guidance section (DASALS — Distributed Aperture Semi-Active Laser Seeker).
  - Semi-active laser homing: requires laser designation from MMS or external source.
  - Compatible warheads: M151 HE (primary), others if available in DCS.
  - Fired from standard M260 launcher — same physical rocket, different guidance section.
- **Guidance Principles:**
  - Rocket must be fired into a "basket" (field of regard) where the seeker can acquire the reflected laser energy.
  - Limited maneuvering capability compared to Hellfire — must be aimed relatively close to the target initially.
  - Laser code (PRF) must match between rocket seeker and designating laser.
  - Terminal guidance: seeker acquires laser spot in flight and corrects trajectory.
- **Employment Sequence (Step-by-Step):**
  - Pre-engagement: Master Arm → APKWS selected → PRF code set → MMS on target → laser armed.
  - Fire: aim aircraft using CCIP reticle to place rocket within seeker acquisition basket → fire → MMS lases target → rocket acquires laser and guides.
  - Lasing timing: must be lasing before rocket enters terminal guidance phase.
  - Post-shot: BDA via MMS → re-engage or safe.
- **Employment Profiles:**
  - Diving fire: 10–15° dive; 1.5–3.0 km range; provides best accuracy and seeker geometry.
  - Running fire: level or shallow dive; requires good basket alignment.
  - Hover fire: close range; precision engagement of specific targets.
  - Maximum and minimum effective ranges.
  - Altitude and airspeed constraints.
- **APKWS vs. Hellfire Decision Matrix:**
  - APKWS: lighter targets, lower collateral damage, cheaper, shorter range, less warhead effect.
  - Hellfire: armor, hardened targets, longer range, larger warhead, can engage from hull-down.
  - When to choose APKWS over unguided rockets: precision required but Hellfire unnecessary.
- **APKWS vs. Unguided Rocket Comparison:**
  - Same launcher, same motor — difference is guidance section.
  - Accuracy improvement: from area-effect (unguided) to point-target (APKWS).
  - Cost-per-round vs. probability of kill tradeoff.
- **Buddy Lasing for APKWS:**
  - External designation from JTAC or wingman; PRF code coordination.
- **Common student errors with APKWS.**

---

**Module 6: M3P .50 Caliber Machine Gun Employment**
- **System Data:**
  - M3P .50 caliber (12.7×99mm) heavy machine gun.
  - Podded mount on the left universal weapons pylon.
  - Fixed forward-firing — does NOT traverse; the pilot aims by pointing the aircraft.
  - Rate of fire: ~1,100 RPM.
  - Ammunition capacity: ~500 rounds.
  - Effective range: 1,000–1,500 m (point targets); up to 2,000 m (area suppression).
- **CCIP Gun Symbology:**
  - CCIP pipper for .50 cal: bullet drop compensation based on range, airspeed, altitude.
  - Pipper behavior: how it moves with aircraft attitude changes.
  - Range estimation using MMS laser range or symbology.
- **Employment Profiles:**
  - **Diving/Running Fire:** 5–15° dive; 60–100 KIAS; 800–1,500 m range. Primary employment method.
  - **Hover Fire:** close range (< 1,000 m); high exposure; used for self-defense or point-blank engagement.
  - **Lateral Break Fire:** engaging while breaking off from a target; suppressive fire.
  - Trigger discipline: burst lengths (3–5 second bursts) to manage ammunition and accuracy.
  - Aiming technique: walk tracers onto target; adjust for drift.
- **Recoil Effects:**
  - .50 cal recoil effect on aircraft attitude (yaw tendency, pitch disturbance).
  - Compensation techniques: pedal input, anticipatory trim.
  - Effect more pronounced in hover than in forward flight.
- **Target Selection:**
  - Troops in the open, unarmored vehicles, trucks, boats, light structures.
  - NOT effective against armored vehicles (IFVs, APCs with armor) — use Hellfire/rockets.
  - Self-defense application: engaging threats during evasion or when other weapons unavailable.
- **Loadout Considerations:**
  - .50 cal occupies the LEFT pylon — cannot be combined with left-side Hellfire or rockets.
  - Typical mixed loadout: .50 cal (left) + Hellfire or rockets (right).
  - Weight penalty: pod weight + ammunition.
- **Ammunition Management:**
  - Round count display on MFD.
  - Ammunition conservation: the 500-round load depletes quickly at 1,100 RPM (~27 seconds of continuous fire).
  - Burst discipline essential.
- **Common student errors with .50 cal.**

---

**Module 7: AIM-92 Stinger Air-to-Air Employment**
- **System Overview:**
  - AIM-92 Stinger: IR-homing air-to-air missile adapted from FIM-92 MANPADS.
  - Mounted on the Air-to-Air Stinger (ATAS) launcher — 2 missiles per launcher, mounted on UWP.
  - Purpose: self-defense against enemy rotary-wing and slow-moving fixed-wing aircraft.
  - Note: document DCS availability — if the AIM-92 is NOT modeled or available in the DCS OH-58D module, clearly state this and provide the real-world doctrinal employment for reference only.
- **Missile Performance:**
  - IR (infrared) all-aspect seeker; IFF interrogation capability (real-world).
  - Effective range: ~500 m to 4,500 m.
  - Engagement envelope: altitude, aspect angle, closure rate constraints.
  - Seeker tone: acquisition growl → lock tone.
- **Employment Sequence (if modeled in DCS):**
  - Master Arm → Stinger selected → seeker uncaged → acquire target (audio tone) → lock confirmation → fire → break/evade.
  - HUD/MFD symbology for air-to-air mode.
  - Minimum range considerations: arming distance.
- **Self-Defense Doctrine:**
  - The OH-58D is NOT an air superiority platform — Stinger is strictly self-defense.
  - Engagement criteria: when to engage (defensive situation, imminent threat) vs. when to evade (terrain mask, call for fighter support, disengage).
  - Evasive maneuvering combined with Stinger employment.
  - ROE considerations: IFF procedures, positive identification before firing.
- **Air-to-Air Threat Environment:**
  - Common DCS threats: enemy helicopters (Mi-24, Ka-50, Mi-8), slow movers (Su-25, L-39).
  - Against fast jets: Stinger has very limited capability; primary defense is terrain masking and evasion.
- **Common student errors with Stinger (or air-to-air engagements).**

---

**Module 8: Countermeasures & Defensive Systems**
- **Countermeasures Dispenser:**
  - Chaff and flare dispensers: location, capacity, loading.
  - Dispense controls: manual, semi-automatic, or programmed modes (per DCS implementation).
  - Chaff: RF decoy against radar-guided threats (radar SAMs, radar-directed AAA).
  - Flares: IR decoy against IR-guided threats (MANPADS: SA-7/14/16/18/24, IR SAMs, IR AAMs).
  - Dispense programs: burst count, interval, sequence configuration.
- **RWR (Radar Warning Receiver):**
  - Threat display: azimuth, threat type, engagement status.
  - Audio cues: new threat, lock-on, launch warning.
  - Threat identification: symbol/number correlation to threat types.
  - RWR integration with countermeasures: cued dispensing.
- **Defensive Maneuvering (Rotary-Wing Specific):**
  - Terrain masking: primary defense — using terrain, trees, buildings to break LOS with threat.
  - Nap-of-the-earth (NOE) flight: 25–50 ft AGL; using terrain contours to avoid detection.
  - Pop-up attack profiles: unmask → engage → remask behind terrain.
  - Break maneuvers: direction, G-loading, altitude loss management.
  - Jinking: irregular flight path to defeat tracking solutions.
  - Flare dispensing during break: timing and pattern.
- **Threat-Specific Defensive Reactions:**
  - IR MANPADS (SA-7, Igla, Stinger): flares + terrain masking + break turn.
  - Radar SAMs (SA-8, SA-11, SA-15): chaff + terrain masking + NOE; avoid overflying engagement zones.
  - AAA (ZSU-23-4, ZU-23): jinking + terrain masking + standoff; do not overfly.
  - Enemy aircraft: terrain masking + Stinger (if available) + call for fighter support.
- **SEAD/Threat Avoidance:**
  - Route planning around known threats.
  - Standoff engagement: using Hellfire max range to remain outside threat envelopes.
  - Time-on-station management: minimizing exposure in threat areas.
- **Common student errors with defensive systems.**

---

**Module 9: Close Combat Attack (CCA) Tactics & Engagement Area Operations**
- **CCA Fundamentals (Rotary-Wing):**
  - CCA vs. CAS: the OH-58D conducts Close Combat Attack (CCA), not CAS — it is an Army Aviation organic asset, not a joint fire support asset. Explain the doctrinal distinction.
  - CCA request and coordination: ground commander integration; frequency management; target handoff.
  - Fire coordination measures: engagement areas, battle positions, forward edge, restricted fire areas.
- **Battle Position Operations:**
  - Selecting and occupying a battle position (BP): terrain analysis, fields of fire, routes in/out.
  - Hull-down technique: MMS exposed, fuselage masked — primary OH-58D engagement posture.
  - Alternate and supplementary positions: pre-planned movement between BPs.
  - Unmask → observe → engage → remask cycle; minimizing exposure time.
  - Lateral movement between BPs to avoid counter-battery/return fire.
- **Engagement Area (EA) Operations:**
  - Engagement area development: identifying kill zones, trigger lines, target reference points.
  - Sector sketch: assigning sectors of fire for multiple aircraft.
  - Priority of fire: engaging highest-threat targets first (advancing armor vs. support vehicles).
  - Coordinated engagement: timing fires with wingman or ground maneuver.
- **Team Tactics:**
  - Scout/Attack Team: OH-58D scouts and designates; AH-64 Apache engages with Hellfire (buddy lase).
  - Hunter/Killer operations: two OH-58D aircraft — one observes/designates, one engages.
  - Wingman coordination: spacing, communication, deconfliction.
  - Multi-ship battle drill: clock calls, engagement sequencing, weapons hold/tight/free.
- **Attack Profiles (Rotary-Wing Specific):**
  - **Hover fire:** Stationary engagement from hull-down BP. Maximum accuracy; highest vulnerability if detected.
  - **Running fire:** Engagement during lateral or forward movement. Reduced accuracy; reduced exposure time.
  - **Diving fire:** Engagement during a diving attack run. Used for rockets/gun primarily.
  - **Pop-up attack:** NOE approach → rapid climb to weapons release altitude → engage → descend behind terrain.
  - Engagement geometry: offset angles, aspect considerations, avoid overflying the target.
  - Egress: break direction, terrain masking route, rally point.
- **Target Handoff Procedures:**
  - Using MMS grid coordinates: "Target at [grid] [description]."
  - Using terrain reference: "From [TRP], [direction], [distance], [description]."
  - Using laser designation: "Laser code [PRF], spot [bearing/range]."
  - Inter-cockpit coordination with ground forces: talk-on techniques.
- **Common student errors with CCA tactics.**

---

**Module 10: Mission Planning & Loadout Optimization**
- **Threat Analysis:**
  - Intelligence preparation: identifying enemy air defenses, armor, infantry positions.
  - Mapping threat rings: MANPADS range, SAM envelopes, AAA effective range.
  - Route planning: terrain-masked ingress/egress routes avoiding threat engagement zones.
- **Loadout Selection:**
  - Mission-based loadout decisions (the OH-58D's 2-pylon limitation makes loadout selection critical):
    - **Anti-Armor:** 4x AGM-114K Hellfire (2 per pylon) — maximum anti-armor capability; no rockets or gun.
    - **Scout/Attack:** 2x Hellfire (right) + M3P .50 cal (left) — balanced reconnaissance and light engagement.
    - **General Purpose:** 2x Hellfire (right) + M260 rockets (left) — mixed precision and area weapons.
    - **Light Scout:** 1x M260 rockets (right) + M3P .50 cal (left) — maximum endurance, light engagement.
    - **Full Rockets:** 2x M260 rocket pods — maximum area suppression; no precision capability.
  - Weight and performance tradeoffs: compute power margin for each loadout at mission conditions (temperature, altitude, fuel).
  - Fuel planning: endurance vs. weapons weight; loiter time on station.
- **Engagement Planning:**
  - Selecting battle positions: fields of fire, cover, concealment, routes.
  - Primary, alternate, and supplementary positions.
  - Engagement area priorities: target types, weapons allocation per target.
  - Ammunition management: Hellfire for armor, rockets for soft targets, gun for troops/self-defense.
- **Communication Planning:**
  - Frequencies: internal team, ground maneuver element, artillery/fires, air traffic.
  - Laser code deconfliction: ensuring unique PRF codes when multiple designators are active.
  - Brevity codes: "Rifle" (Hellfire launch), "Rockets" (rocket fire), "Guns" (gun engagement), "Spot" (laser on), "Splash" (impact), "Winchester" (out of weapons), "Bingo" (fuel state).
- **DCS Mission Editor Integration:**
  - Setting up weapons loadouts in the DCS mission editor.
  - Configuring waypoints, target points, and engagement zones.
  - Weather considerations: thermal conditions affecting FLIR, wind affecting rockets.
- **Common student errors with mission planning.**

---

**For each weapon system / module, provide:**
1. **DCS Employment Sequence:** Step-by-step cockpit switchology (weapon setup → Master Arm → sensor → designate → fire) with specific switch names, panel locations, MFD pages, and HOTAS functions.
2. **Key Constraints:** Min/max range, altitude, airspeed, dive angle, and weapon-specific limits.
3. **Recommended Attack Profiles:** Entry altitude, speed, dive angle, engagement range, egress maneuver — with rotary-wing-specific profiles (hover fire, running fire, diving fire, pop-up).
4. **Common Student Errors:** What students usually do wrong and how to fix it.
5. **Realism Divergence Notes:** Where DCS simplifies, omits, or diverges from real-world procedures/limitations.

**Output Format:**
A single, structured Markdown document suitable for saving as `.github/research/oh-58d-weapons-dossier.md`. Use heading levels `##`, `###`, and `####` consistently. Include data tables for all numerical parameters. Target length: comprehensive — this document should be the single authoritative reference for building the entire weapons employment training course.
