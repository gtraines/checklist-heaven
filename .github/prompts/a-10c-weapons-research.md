Act as an expert USAF A-10C "Thunderbolt II" weapons officer and DCS World mission planner, cross-referencing real-world USAF technical manuals with DCS simulation documentation. I need you to compile a detailed research dossier for an **A-10C Weapons Employment Course**.

**Objective:**
Create a comprehensive technical reference document covering the employment of all air-to-ground and self-defense weapons available on the DCS A-10C and A-10C II modules. This research will be used to build a multi-event training course with structured exercises and grading criteria. The student has already completed the A-10C BQT course and is proficient in basic flight operations, startup/shutdown, navigation, traffic patterns, and emergency procedures.

**DCS Module Context:**
The DCS A-10C and A-10C II are **full-fidelity, clickable-cockpit modules**:
- **Fully interactive cockpit** — all systems operated via mouse-clickable switches, the UFC (Up-Front Controller), MFCDs, CDU, and HOTAS controls.
- Weapons are managed through the **DSMS (Digital Stores Management System)** — a dedicated MFD page for inventory management, profile selection, fuze settings, release quantities, and delivery mode configuration. There is NO simple "cycle weapons" key.
- The **IFFCC (Integrated Flight & Fire Control Computer)** provides CCIP, CCRP, and manual delivery modes with computed HUD symbology.
- **Targeting Pod (TGP):** The A-10C carries the **AN/AAQ-28 Litening AT**; the A-10C II carries the **Sniper XR (AN/AAQ-33)**. Both provide self-designation capability for LGBs, laser-guided rockets, and target identification for all weapons.
- **A-10C II additions:** HMCS (Helmet-Mounted Cueing System), APKWS (Advanced Precision Kill Weapon System — laser-guided Hydra 70), GBU-39 SDB (Small Diameter Bomb), GBU-54 LJDAM (Laser JDAM). The A-10C II is a superset of the A-10C — all A-10C procedures apply unless noted.
- **Advanced Flight Model (AFM)** — aerodynamics, weapon ballistics, GAU-8/A recoil, and stores drag are realistically modeled.

**Source Material Prioritization:**
1. **Primary (Simulation Truth):** Official DCS A-10C / A-10C II documentation and actual in-game behavior. When the sim contradicts real-world procedures, **the sim wins** — document the DCS procedure as primary instruction.
2. **Secondary (Realism Context):** Real-world USAF documentation:
   - *T.O. 1A-10C-34-1-1* (A-10C Nonnuclear Weapons Delivery Manual)
   - *T.O. 1A-10C-1* (A-10C Flight Manual)
   - *AFMAN 11-2A-10C Vol. 3* (A-10C Operations Procedures)
   - *MCM 3-1* (USAF Tactical Employment — Multi-Command Manual)
   - *AFTTP 3-3.A-10* (Tactical Employment — A-10)
   - A-10C weapons supplements and IFFCC technical orders
3. **Conflict Resolution:** When a real-world procedure conflicts with DCS, document the **DCS procedure** as the primary instruction and add a clearly marked footnote:
   > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

**Required Research Modules:**

---

**Module 1: DSMS, IFFCC & HUD Weapons Symbology**
- **DSMS (Digital Stores Management System):**
  - Accessing the DSMS page on the left or right MFCD.
  - Inventory page: reading loaded stations, quantities, weapon types.
  - Profile pages: selecting delivery profiles (CCIP, CCRP, Manual, DTOS).
  - Setting fuze options (nose/tail, instantaneous/delay/proximity), release quantity (single/pair/ripple), and ripple interval.
  - Arming delay (AD) settings for low-altitude deliveries.
  - Station jettison and emergency jettison procedures.
- **IFFCC Modes:**
  - CCIP (Continuously Computed Impact Point) — pipper tracks ground impact point in real time.
  - CCRP (Continuously Computed Release Point) — steering cue to overfly computed release point; auto-release or manual consent.
  - Manual — pilot-estimated delivery using fixed reference marks.
  - DTOS (Dive Toss) — loft/toss delivery using TGP or SPI designation.
- **HUD Weapons Symbology (per mode):**
  - Gun cross, gun funnel, and PAC (Precision Attitude Control) modes for the GAU-8/A.
  - Bomb fall line and CCIP pipper for iron bombs.
  - CCRP azimuth steering line, range bar, pull-up cue, and consent-to-release symbology.
  - Maverick symbology: bore-sight cross, seeker footprint, lock indication.
  - JDAM symbology: time-to-release, steering cue, solution circle.
  - Rocket CCIP pipper and impact line.
- **Master Arm Panel:**
  - MASTER ARM switch (SAFE / ARM / TRAIN).
  - GUN/PAC ARM switch.
  - Laser ARM switch (required before TGP lasing or APKWS guidance).
  - Emergency jettison button.

---

**Module 2: GAU-8/A Avenger Cannon**
- **System Data:**
  - 30mm 7-barrel Gatling; selectable rate (HIGH: 3,900 RPM / LOW: not modeled in DCS — always HIGH).
  - Ammunition: 1,174 rounds capacity; standard combat mix (PGU-14/B API + PGU-13/B HEI, 5:1 ratio).
  - Effective range vs. armored targets: 4,000–6,000 ft slant range.
  - Effective range vs. soft targets: up to 8,000–12,000 ft slant range.
- **IFFCC Gun Modes:**
  - PAC-1 (Precision Attitude Control — Strafe): stabilized gun cross; highest accuracy mode.
  - PAC-2 (CCRP equivalent for guns): computed impact point along HUD azimuth line.
  - PAC-3 (Gun funnel / EEGS-like): lead-computing funnel for air-to-air (not primary mission but documented).
  - Gun cross behavior: fixed vs. computed pipper placement.
- **Employment Profiles:**
  - 20–30° dive strafing (anti-armor): entry 8,000–10,000 ft AGL, 350 KIAS, minimum recovery altitude.
  - Shallow / low-angle strafing (soft targets, troops-in-contact): 5–15° dive.
  - Trigger discipline: 1–2 second bursts (50–130 rounds); sustained fire effects on barrel wear and accuracy.
- **Recoil Effects:**
  - DCS models ~19,000 lbf recoil — noticeable airspeed bleed during sustained fire.
  - Nose wander and yaw during long bursts.
  - Compensation techniques: trim anticipation, shorter bursts, speed management.
- **DSMS setup for gun:** rate selection, round count display, arming.
- **Common student errors with the GAU-8/A.**

---

**Module 3: Unguided Bombs (Iron Bombs)**
- **Available Ordnance:**
  - Mk-82 (500 lb GP, low-drag).
  - Mk-82 AIR (BSU-49/B high-drag — retarded delivery for low-altitude).
  - Mk-82 Snakeye (BSU-33/B retarder fins — alternate high-drag option).
  - Mk-84 (2,000 lb GP).
- **DSMS Profile Setup:**
  - Selecting bomb type, fuze (NOSE / TAIL / N+T), fuze function (INST / DLY1 / DLY2), arming delay (AD).
  - Release quantity (SGL / PRS / RPL), ripple count, ripple interval (feet or milliseconds).
  - Profile save and recall.
- **Delivery Modes:**
  - CCIP dive bombing: recommended dive angles (20–45°), entry altitudes, release altitudes, minimum recovery altitudes per bomb type.
  - CCIP pipper tracking and release technique: "track, track, pickle."
  - CCRP level/shallow-dive delivery: steering cue, range bar, auto-release or manual consent.
  - CCRP altitude and airspeed requirements for computed solution accuracy.
  - Low-altitude delivery with Mk-82 AIR/Snakeye: pop-up attack profiles, minimum release altitude for safe separation with retarded fins.
- **Fuze Selection Guide:**
  - Instantaneous: soft targets, personnel, light vehicles.
  - Delay: bunkers, hardened targets, bridge piers, buried infrastructure.
  - Nose + Tail: maximum detonation reliability.
- **Fragmentation patterns and safe separation distances.**
- **Common student errors with iron bombs.**

---

**Module 4: Cluster Munitions**
- **Available Ordnance:**
  - CBU-87 CEM (Combined Effects Munition) — anti-armor/personnel/incendiary BLU-97 bomblets.
  - CBU-97 SFW (Sensor Fuzed Weapon) — BLU-108 submunitions with autonomous IR-seeker skeets; anti-armor.
  - CBU-103 (WCMD + CBU-87) — Wind-Corrected Munitions Dispenser with CEM payload.
  - CBU-104 (WCMD + CBU-97 SFW payload — if available in DCS).
  - CBU-105 (WCMD + SFW) — Wind-corrected SFW.
- **Employment Considerations:**
  - CBU-87/97 (unguided): Must be delivered from computed altitude and dive angle for proper footprint. Minimum burst altitude for CBU-97 skeet acquisition (~1,500–3,000 ft AGL).
  - WCMD variants (CBU-103/105): GPS-aided wind correction — set coordinates or use SPI. DSMS programming for WCMD wind data input.
  - Footprint orientation: CCIP delivery aligns footprint along aircraft track; CCRP may orient differently.
- **DSMS Profile Setup:**
  - Burst altitude settings, fuze options (differ from iron bombs).
  - HOF (Height of Function) programming for cluster munitions.
- **Delivery Modes:**
  - CCIP for CBU-87/97 — dive angles, release altitudes, dispenser function altitude.
  - CCRP for WCMD — coordinate-based delivery, auto-release.
- **Target Sets:**
  - CBU-87: armor columns, troop concentrations, soft-skin convoys, airfield denial.
  - CBU-97/105: armor formations, vehicle parks (IR-seeking skeets prioritize hot engines).
- **Common student errors with cluster munitions.**

---

**Module 5: Unguided Rockets (Hydra 70 Family)**
- **Available Variants:**
  - M151 (HE warhead) — anti-personnel, light vehicles, soft targets.
  - M156 (WP / white phosphorus) — marking, incendiary.
  - M274 (smoke practice) — target marking for CAS coordination.
  - M257 (illumination) — battlefield illumination for night operations.
- **Launcher Types:** LAU-68 (7-tube), LAU-131 (7-tube), LAU-61 (19-tube) — availability per DCS loadout.
- **DSMS Profile Setup:**
  - Rocket type selection, quantity per salvo (1, 2, 4, 7, 14, etc.), inventory tracking.
- **Employment Profiles:**
  - 10–20° dive angle; 1.0–2.0 nm slant range; 250–350 KIAS.
  - CCIP pipper usage for rockets — pipper behavior differs from bomb CCIP (faster movement).
  - Ripple vs. single fire modes.
  - WP marking technique for FAC/CAS scenarios: "Mark on my smoke."
- **Dispersion and accuracy characteristics.**
- **Common student errors with rockets.**

---

**Module 6: TGP (Targeting Pod) Operations**
- **Pod Variants:**
  - AN/AAQ-28 Litening AT (A-10C) — FLIR, CCD-TV, laser designator/rangefinder, laser spot tracker.
  - AN/AAQ-33 Sniper XR (A-10C II) — upgraded FLIR resolution, extended range, HMCS slew integration.
- **TGP Power-On & Alignment:**
  - TGP switch: OFF → STBY → OPER.
  - Warm-up time and alignment requirements.
  - MFD TGP page layout: FLIR imagery, symbology overlays, OSB functions.
- **TGP Modes:**
  - A-G (Air-to-Ground): primary mode for target designation and weapons delivery.
  - A-A (Air-to-Air): not primary; mention for completeness.
  - Snowplow / Inertial / Point Track modes: behavior and use cases.
- **Sensor Controls:**
  - FOV: Narrow / Wide field of view toggle.
  - Polarity: White-Hot / Black-Hot (FLIR); Day TV (CCD).
  - Slew: HOTAS slew (China Hat, TMS) vs. cursor slew.
  - Area Track, Point Track, and Inertial modes: when and how to use each.
- **Laser Operations:**
  - Laser ARM switch on armament panel.
  - Laser fire: TMS UP (short press to range; long press to designate).
  - Laser code setting: CDU → LSR page → 4-digit PRF code (default 1688).
  - Lasing for LGBs: timing — lase at release, or lase continuously? DCS-specific behavior.
  - Lasing for APKWS: terminal guidance laser-on timing.
  - Buddy lasing: setting laser code to match JTAC or wingman; receiving external designation via LST (Laser Spot Tracker).
- **SPI (Sensor Point of Interest):**
  - SPI is the master designation reference shared across systems (TAD, HUD, TGP, CDU steerpoint).
  - Setting SPI: from TGP, from TAD cursor, from HUD CCIP point, from CDU steerpoint.
  - SPI handoff between systems.
- **Target Identification & Coordination:**
  - Using TGP to find, identify, and track targets before weapons release.
  - 9-line CAS integration: TGP confirms target prior to "Cleared Hot."
  - Recording coordinates from TGP for JDAM/LJDAM employment.
- **Common student errors with TGP.**

---

**Module 7: AGM-65 Maverick Family (Precision Guided)**
- **Variants Available on DCS A-10C:**
  - AGM-65D (IR seeker — imaging infrared, 125 lb shaped-charge warhead).
  - AGM-65G (IR seeker — 300 lb penetrating blast-frag warhead).
  - AGM-65H (CCD/EO-TV seeker — daytime only, 125 lb shaped-charge warhead).
  - AGM-65K (CCD/EO-TV seeker — 300 lb penetrating blast-frag warhead).
- **DSMS Maverick Setup:**
  - Selecting Maverick stations and type.
  - Maverick page on MFCD: seeker video, polarity, FOV, status.
  - Pre-launch cooldown for IR variants (D/G) — takes time; plan ahead.
- **Seeker Operations (Full-Fidelity):**
  - IR (D/G): polarity (WHOT/BHOT); FOV narrow/wide; contrast adjustment.
  - EO-TV (H/K): daylight-only; contrast-dependent; FOV narrow/wide.
  - Slewing the seeker: HOTAS slew controls; China Hat for sensor select; TMS for lock.
  - SPI handoff: slewing Maverick seeker to SPI (TGP target) for rapid lock.
  - Lock-on: TMS UP to lock; confirm stable tracking gate on target; verify "RDY" on MFCD.
  - "Maverick handoff" — automatic seeker cue to SPI or TGP designation.
- **Employment Profiles:**
  - Stand-off range: 4–10 nm depending on variant, altitude, and atmospheric conditions.
  - Launch envelope: altitude (min/max), dive angle, airspeed constraints.
  - Single-shot targeting cycle: designate → lock → verify → pickle → assess → re-attack.
  - Ripple Maverick employment: sequential lock-shoot-lock cycle.
- **Variant Selection Guide:**
  - IR (D/G) vs. EO-TV (H/K): day/night, weather, target thermal signature.
  - Heavy warhead (G/K) for bunkers, bridges, large structures.
  - Light warhead (D/H) for individual vehicles, armor.
- **Common student errors with Mavericks.**

---

**Module 8: Laser-Guided Bombs (Paveway II / III)**
- **Available Ordnance:**
  - GBU-12 (Paveway II — 500 lb Mk-82 body + laser guidance kit).
  - GBU-10 (Paveway II — 2,000 lb Mk-84 body + laser guidance kit).
- **Self-Lasing with TGP:**
  - The A-10C can self-designate — a major capability difference from the A-10A (Pave Penny only).
  - Workflow: TGP acquires target → lock (Point Track) → set laser code → arm laser → DSMS selects LGB → delivery mode (CCRP preferred) → release → TGP lases → bomb guides.
  - Laser timing: when to start lasing relative to release (DCS-specific behavior).
  - Terminal guidance: laser must be on target for final ~10–15 seconds of flight.
- **Buddy Lasing (External Designation):**
  - Laser code coordination: match codes with JTAC, FAC-A, or wingman.
  - LST (Laser Spot Tracker) mode on TGP: detecting external laser energy.
  - Communication flow: "Spot" / "Laser On" / "Rifle" / "Splash."
  - Timing: external laser activation before or at release? DCS-specific behavior.
- **DSMS Profile Setup:**
  - LGB selection, laser code verification, fuze (typically NOSE/INST or NOSE/DLY for hardened targets).
  - Release mode: CCRP with auto-release preferred for LGBs.
- **Delivery Profiles:**
  - Medium-altitude CCRP: 12,000–18,000 ft AGL; 350 KIAS; wings-level release.
  - Dive delivery CCIP: steeper profile for reduced time-of-flight; self-lasing throughout.
  - Loft/DTOS delivery: if applicable in DCS.
- **Environmental Limitations:**
  - Weather: cloud undercast breaks laser path — LGB requires clear line-of-sight from laser to target.
  - Smoke, dust, obscurants degrade laser effectiveness.
- **Common student errors with LGBs.**

---

**Module 9: GPS-Guided Weapons (JDAM)**
- **Available Ordnance:**
  - GBU-38 (JDAM — 500 lb Mk-82 body + GPS/INS tail kit).
  - GBU-31 (JDAM — 2,000 lb Mk-84 body + GPS/INS tail kit).
  - GBU-31(V)3/B (JDAM — BLU-109 penetrator body + GPS/INS tail kit, if available).
- **JDAM Fundamentals:**
  - GPS/INS guidance — no laser required; weather-independent (all-weather capability).
  - Coordinate-based: weapon flies to programmed LAT/LONG/ELEV.
  - Accuracy: ~10 m CEP (GPS); ~30 m CEP (INS-only, GPS denied).
- **DSMS JDAM Setup:**
  - Selecting JDAM stations; DSMS JDAM-specific sub-pages.
  - Coordinate entry: manual LAT/LONG/ELEV via CDU or UFC.
  - SPI transfer: TGP-derived coordinates → SPI → JDAM target.
  - TOO (Target of Opportunity) mode: coordinates updated in real-time from SPI/TGP.
  - PP (Pre-Planned) mode: pre-loaded coordinates from mission planning.
- **Delivery Modes:**
  - CCRP: primary delivery mode. Steering cue, time-to-release countdown, auto-release.
  - Release envelope: altitude (min/max), airspeed, dive angle. JDAM has wide envelope.
  - Loft delivery: high-angle release for standoff distance.
- **Coordinate Accuracy:**
  - Source accuracy matters: TGP-derived coordinates (good), TAD-cursor coordinates (less accurate), manually entered (variable).
  - Target elevation critical: incorrect elevation degrades accuracy significantly.
  - Technique: use TGP to refine coordinates before committing to release.
- **Multi-JDAM Employment:**
  - Ripple release of multiple JDAMs to different targets in one pass (if DSMS supports pre-planned sequence).
  - Sequential release to same target for redundancy.
- **Common student errors with JDAMs.**

---

**Module 10: A-10C II Advanced Munitions**

> **Note:** This module covers weapons unique to the A-10C II. If the student is flying the A-10C (non-II), this module may be deferred. All other modules apply to both variants.

- **APKWS (Advanced Precision Kill Weapon System):**
  - Laser-guided Hydra 70 rocket with WGU-59/B guidance section.
  - Semi-active laser homing: requires laser designation (self-lase via TGP or buddy lase).
  - Warhead: M151 HE (same as unguided Hydra 70) but precision-guided.
  - Employment: fire in CCIP; laser must be on target; rocket acquires laser in flight.
  - DSMS setup: select APKWS; arm laser; set laser code.
  - Range: 1.5–5.0 km (shorter than Maverick but much cheaper and lighter).
  - Use case: precision CAS against individual vehicles, personnel in structures, small targets — where Maverick is too expensive or collateral damage must be minimized.
- **GBU-39 SDB (Small Diameter Bomb):**
  - 250 lb GPS/INS guided glide bomb.
  - Diamond Back wing kit: extended glide range (~40 nm from high altitude).
  - Coordinate-based (like JDAM but lighter, longer range, smaller warhead).
  - DSMS setup: similar to JDAM — coordinate entry, SPI transfer, fuze options.
  - Employment: CCRP release at medium-to-high altitude for maximum glide range.
  - Carriage: 4 per BRU-61 rack — high magazine depth.
  - Use case: hardened point targets (bunkers, C2 nodes) at standoff range; reduced collateral damage.
- **GBU-54 LJDAM (Laser JDAM):**
  - GPS/INS + semi-active laser terminal guidance — hybrid weapon.
  - Launches like a JDAM (GPS coordinates) but acquires laser designation in terminal phase for moving target engagement.
  - DSMS setup: JDAM coordinate entry + laser code.
  - Employment: CCRP release; TGP lases target in terminal phase; weapon corrects from GPS to laser.
  - Use case: moving targets (vehicle convoys, relocating TELs) where pure GPS JDAM would miss.
- **HMCS (Helmet-Mounted Cueing System):**
  - Look-and-designate: pilot looks at target → TMS UP → SPI set to HMCS LOS.
  - Rapid Maverick cueing: HMCS slews Maverick seeker to pilot's look angle.
  - TGP slew: HMCS commands TGP to look where pilot looks.
  - Integration with all weapons via SPI: HMCS sets SPI → JDAM/LGB/APKWS receive coordinates.
  - Employment advantage: dramatically reduces sensor-to-shooter timeline.
- **Common student errors with A-10C II advanced munitions.**

---

**Module 11: AIM-9M Sidewinder (Self-Defense A/A)**
- **Missile Data:**
  - AIM-9M all-aspect IR homing; rear-aspect preferred for highest Pk.
  - Effective range: 0.5–5 nm (conditions dependent).
  - IRCCM (IR Counter-Countermeasure) capability.
- **Employment (Full-Fidelity Cockpit):**
  - Master mode: A-A (air-to-air mode) via HOTAS or cockpit switch.
  - Seeker tone: growl = tracking, steady high-pitch = lock.
  - Uncage: TMS UP to uncage seeker; allow seeker to track target.
  - Launch: pickle button when within parameters.
  - HUD A-A symbology: AIM-9 seeker circle, target designator box, range cue.
- **Self-Defense Doctrine:**
  - This is a **self-defense weapon only** — the A-10C is NOT a fighter.
  - When to engage (defensive situation, bandit in weapons envelope, no other option) vs. when to evade/jettison stores and run.
  - Jettison stores for speed: if engaged by fighters, jettison weapons → max power → terrain mask → call for help.
- **Common student errors with AIM-9.**

---

**Module 12: ECM, Countermeasures & Defensive Systems**
- **CMSP (Countermeasures Signal Processor):**
  - CMSP panel on front dash — MAN / SEMI / AUTO modes.
  - Program selection: 1–6 pre-programmed CM programs (chaff/flare combinations).
  - Manual dispense: chaff button / flare button on HOTAS or cockpit.
  - Semi-automatic: RWR-cued dispensing upon threat detection.
  - Auto: fully automated response to detected threats.
  - Programming custom CM programs: dispense count, interval, sequence.
- **ALE-47 Countermeasures Dispenser:**
  - Chaff (RF decoy) and flare (IR decoy) inventory management.
  - Chaff effectiveness: against radar-guided threats (SAMs, AAA radar).
  - Flare effectiveness: against IR-guided threats (MANPADS, IR SAMs, IR AAMs).
- **ALR-69 Radar Warning Receiver (RWR):**
  - Threat display: azimuth display of emitters; threat type symbols.
  - Priority threats: launch warning, lock-on warning, search radar.
  - Audio cues: new threat, launch warning tones.
  - Threat identification by symbol type.
- **ALQ-131 / ALQ-184 ECM Pod:**
  - Jamming modes and activation.
  - Pod station assignment — impact on weapons loadout (typically station 6 centerline).
  - When to use active jamming vs. passive (RWR-only) posture.
  - ECM vs. EMCON considerations.
- **Defensive Maneuvering Integration:**
  - Layered defense: ECM + countermeasures + terrain masking + speed + maneuver.
  - "Notching" radar-guided threats: placing the threat on the beam (3/9 o'clock) to exploit Doppler notch.
  - Terrain masking as primary SEAD avoidance technique.
  - Jink / maneuver patterns for AAA and IR threat avoidance.
  - Threat-specific defensive reactions: SA-8, SA-11, SA-15, ZSU-23-4, MANPADS.
- **Common student errors with defensive systems.**

---

**For each weapon system / module, provide:**
1. **DCS Employment Sequence:** Step-by-step cockpit switchology (DSMS setup → Master Arm → Mode → TGP/sensor → Designate → Pickle / Fire) with specific switch names, panel locations, and HOTAS functions.
2. **Key Constraints:** Min/max range, altitude, airspeed, dive angle, recovery altitude, and weapon-specific limits.
3. **Recommended Attack Profiles:** Entry altitude, speed, dive angle, release/fire parameters, egress maneuver.
4. **Common Student Errors:** What students usually do wrong and how to fix it.
5. **Realism Divergence Notes:** Where DCS simplifies, omits, or diverges from real-world procedures/limitations.

**Output Format:**
A single, structured Markdown document suitable for saving as `.github/research/a-10c-weapons-dossier.md`. Use heading levels `##`, `###`, and `####` consistently. Include data tables for all numerical parameters. Target length: comprehensive — this document should be the single authoritative reference for building the entire training course.
