Act as an expert Soviet/Russian Mi-24P Hind weapons officer, attack helicopter tactics instructor, and DCS World mission planner, cross-referencing real-world Soviet and Russian military technical documentation with DCS simulation documentation. I need you to compile a detailed research dossier for a **Mi-24P Hind Weapons Qualification Course (WQC)**.

**Objective:**
Create a comprehensive technical reference document covering the employment of all weapons and sensor systems available on the DCS Mi-24P Hind module. This research will be used to build a multi-event training course with structured exercises and grading criteria. The student has already completed the Mi-24P BQT course and is proficient in basic flight operations, startup/shutdown, hover, running takeoff/landing, navigation, traffic patterns, autorotation, and emergency procedures.

**DCS Module Context:**
The DCS Mi-24P (Eagle Dynamics — native module) is a **full-fidelity, dual-seat, clickable-cockpit module**:
- **Dual cockpit, fully interactive** — all systems in both the Pilot (rear) and WSO (front) cockpits are operated via mouse-clickable switches.
- **Seat switching (single-player):** `1` = WSO (front cockpit); `2` = Pilot (rear cockpit). In multiplayer, a dedicated WSO handles the front cockpit.
- **Division of labor:** The Pilot flies the aircraft and fires fixed-forward weapons (GSh-30K cannon, rockets when using CCIP in pilot mode). The WSO operates the PKV-1 collimating sight, manages ATGM guidance (Shturm/Ataka SACLOS), and selects weapons from the front cockpit weapons panel. This crew coordination is central to effective Mi-24P employment.
- **No targeting pod.** The Mi-24P uses optical/mechanical sighting systems — the PKV-1 gyrostabilized collimating sight (WSO front cockpit) and the PNK-800 navigation attack system. There is no FLIR targeting pod. Target identification and engagement are visual / optical.
- **SACLOS missile guidance:** The 9M114 Shturm and 9M120 Ataka ATGMs use **radio-command SACLOS (Semi-Automatic Command to Line-Of-Sight)** guidance. The WSO manually tracks the target with the PKV-1 sight joystick; the guidance system transmits corrections to the missile automatically. The pilot must maintain steady flight throughout missile time-of-flight.
- **Fixed cannon:** The GSh-30K twin-barrel 30mm cannon is bolted to the starboard fuselage in a fixed forward mount. The pilot points the entire aircraft at the target. There is no turret.
- **Units convention:** Soviet metric throughout — km/h, meters, °C, kg. All data tables must include metric values; imperial/KIAS conversions are optional but welcome.
- **Stub wing pylons:** 4 pylons total (inner and outer, left and right stub wings). Loadout combinations affect weight, performance (hover ceiling, rate of climb, VNE margin), and survivability.

**Source Material Prioritization:**
1. **Primary (Simulation Truth):** Official DCS Mi-24P Eagle Dynamics module documentation and actual in-game behavior. When the sim contradicts real-world procedures, **the sim wins** — document the DCS procedure as primary instruction.
2. **Secondary (Realism Context):** Real-world Soviet/Russian military documentation:
   - *Mi-24P RLE (Rukovodstvo po Letnoy Ekspluatatsii)* — Mi-24P Flight Manual (weapons employment sections)
   - *Mi-24P Technical Description & Operating Instructions (Tekhnicheskoye Opisaniye)* — weapons systems architecture
   - *9M114 Shturm System Technical Manual* (Boyevaya Mashina 9P149 and related docs)
   - *9M120 Ataka System Technical Manual*
   - Soviet VVS (Air Force) and AA (Army Aviation) weapons employment circulars and attack tactics manuals
   - *GRAU documentation* on S-5, S-8, S-13, S-24 unguided rocket families
   - Western intelligence assessments (DIA, NATC, NATO publications) where Soviet originals are unavailable — label clearly as secondary/intelligence-derived
   - Translated excerpts from Soviet helicopter gunnery training manuals (TC equivalent)
3. **Conflict Resolution:** When a real-world procedure conflicts with DCS, document the **DCS procedure** as the primary instruction and add a clearly marked footnote:
   > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

**Required Research Modules:**

---

**Module 1: Weapons Systems Overview & Cockpit Switchology**
- **Weapons available in DCS Mi-24P (full inventory table):**
  - GSh-30K 30mm cannon (fixed, pilot-fired)
  - 9M114 Shturm ATGM (SACLOS, WSO-guided)
  - 9M120 Ataka ATGM (SACLOS, WSO-guided)
  - S-5 (57mm) unguided rockets
  - S-8 (80mm) unguided rockets — B-8V20A 20-round pods
  - S-13 (122mm) unguided rockets — B-13L 5-round pods
  - S-24 (240mm) heavy unguided rockets — single-round APU-68UM rail
  - R-60 (AA-8 Aphid) air-to-air missile — self-defense
  - R-73 (AA-11 Archer) air-to-air missile — self-defense
  - FAB-100 / FAB-250 general-purpose bombs (if available in DCS)
  - RBK-250 cluster munitions (if available in DCS)
- **Pylon stations:**
  - Station numbering convention (inner/outer, left/right)
  - Maximum load per pylon (weight limit)
  - Compatible weapons per station
  - Typical combat loadout configurations (anti-armor, close support, mixed)
- **WSO Front Cockpit — Weapons Panel:**
  - Weapons master arm switch: location, positions (SAFE / ARMED)
  - Weapon selector switch/panel: how to select between cannon, rockets, ATGMs, AAMs
  - Salvo/ripple controls (for rockets): single, pairs, full pod
  - ATGM guidance panel: arming, mode selection (Shturm vs. Ataka), launch enable
  - Emergency stores jettison: panel location and procedure
- **Pilot Rear Cockpit — Weapons Controls:**
  - Trigger on cyclic: cannon fire (primary for fixed weapons)
  - Rocket fire button on collective or cyclic (pilot-fired rockets)
  - Weapon safe switch accessible to pilot
  - Observation of WSO-controlled weapons from pilot seat (no direct pilot engagement for ATGMs)
- **Master Arm sequence (both cockpits):**
  - Pre-engagement arming checklist
  - Weapons safe sequence post-engagement or on abort
- **DCS keyboard/HOTAS reference for weapons** (defaults and recommended bindings)
- **Common student errors in weapons switchology**

---

**Module 2: PKV-1 Sight — Operations & Target Acquisition**
- **PKV-1 System Architecture:**
  - Type: collimating, gyrostabilized optical sight (daytime optical — no thermal/FLIR)
  - Location: WSO front cockpit
  - Purpose: aiming rockets, designating targets for ATGM SACLOS guidance, cannon aiming reference
  - Stabilization axes: pitch and yaw gyrostabilization; response to aircraft maneuver
  - Field of view and zoom (if applicable in DCS)
- **PKV-1 Power-On & Alignment:**
  - Power switch location and sequence
  - Gyro warm-up requirements
  - Boresight verification procedure (with pilot position crosscheck)
- **PKV-1 Controls (WSO):**
  - Slew: joystick axis for ATGM guidance and sight movement
  - Reticle: sight picture description for each weapon mode
  - Zoom / magnification (if modeled)
  - Switching between weapon modes
- **Target Acquisition Techniques (daytime optical):**
  - Naked-eye acquisition before PKV designation
  - Visual cues: dust, muzzle flash, vehicle movement, heat shimmer
  - Range estimation: visual reference vs. sight ranging
  - Systematic search patterns: sector scan, area scan
  - Target identification and classification prior to engagement
  - Limitations: no night capability; no thermal; degraded in dust/smoke/haze
- **Laser Rangefinder (if equipped in DCS):**
  - System designation and operation
  - Range display on PKV or cockpit instrument
  - Integration with weapons ballistic solution
- **Battle Damage Assessment (BDA):**
  - Post-strike visual assessment through PKV
  - Standard BDA reporting format
- **Common student errors with PKV-1**

---

**Module 3: GSh-30K 30mm Cannon Employment**
- **System Data:**
  - Designation: GSh-30K (Gryazev-Shipunov 30mm twin-barrel)
  - Mount: fixed to starboard fuselage, fixed-forward (non-traversing)
  - Rate of fire: ~2,600–3,000 rounds per minute (single sustained burst or cyclic)
  - Ammunition capacity: ~250 rounds standard load in DCS (confirm actual DCS figure)
  - Standard ammunition types: APHE, HE-Frag (specify DCS loadout)
  - Muzzle velocity: ~900 m/s
  - Effective range: anti-armor ~600–800 m; soft targets ~1,000–1,500 m
- **Fixed Mount Implications:**
  - The pilot aims the entire aircraft — nose of helicopter must point at target
  - No off-boresight capability; no lateral slew
  - Engagement requires maneuvering the aircraft into a dive or level run directly at the target
  - WSO has no cannon control
- **CCIP (Continuously Computed Impact Point) for Cannon:**
  - How CCIP is displayed in DCS (HUD or PKV sight)
  - CCIP computation factors: airspeed, altitude, dive angle, wind (if modeled)
  - CCIP pipper behavior during maneuver
- **Employment Profiles:**
  - **Diving strafe (primary):** 10–20° dive, 220–260 km/h, engagement range 800–1,200 m, break-off altitude
  - **Shallow pass (soft targets):** 5–10° dive or level, 180–220 km/h, engagement range 1,000–1,500 m
  - **Running fire (level):** target tracking in level flight at cruise speed; reduced accuracy; area suppression only
  - Entry altitude and pattern for each profile
  - Minimum recovery altitude and pull-off technique
  - Burst discipline: burst length recommendations (1–2 sec); effects of long bursts on accuracy
- **Cannon Effects on Aircraft:**
  - Recoil forces (if modeled in DCS): nose wander, airspeed bleed
  - Compensations: trim, power, shorter bursts
- **Target Type vs. Employment Profile matrix:**
  - Heavy armor (MBTs): ranges and angles; expected penetration
  - Light armor / APCs / IFVs: optimum parameters
  - Soft targets, troops, trucks: parameters
  - Hardened positions: parameters
- **Cannon vs. ATGM Employment Decision:**
  - When to use cannon vs. Shturm/Ataka
  - Threat considerations (AAA, MANPADS) driving standoff vs. close engagement
- **DCS-specific cannon modeling notes (realism divergences)**
- **Common student errors with cannon employment**

---

**Module 4: 9M114 Shturm ATGM Employment**
- **System Data:**
  - Designation: 9M114 Shturm (NATO: AT-6 Spiral); carrier system 9K113
  - Guidance: Radio-command SACLOS — WSO tracks target via PKV-1; ground station transmits corrections to missile via radio beam
  - Propulsion: Solid rocket with sustainer
  - Warhead: HEAT (shaped charge); 600+ mm RHA penetration; specify DCS warhead variant
  - Range: minimum ~400 m; maximum ~5,000 m; typical engagement: 1,500–4,000 m
  - Speed: ~350 m/s average; time-of-flight to max range ~15 seconds
  - Pylon capacity: 2 missiles per outboard pylon (APU-68 launch rail); 4 total max standard
- **SACLOS Guidance Principles:**
  - How SACLOS works: WSO keeps sight on target; system compares missile position (measured by IR tracker) vs. sight line and transmits corrections via radio
  - Unlike laser guidance (AGM-114 SAL), there is no laser spot on target — the tracking is of the missile, not the target
  - Flight platform stability requirement: pilot must hold steady, level flight throughout missile time-of-flight (turn, climb, or dive breaks guidance geometry)
  - Maximum aircraft turn rate during Shturm guidance (specify limit if known from RLE)
  - Wind effects on guidance: crosswind correction applied automatically by system; limits if known
- **WSO Guidance Technique:**
  - Sight acquisition: PKV-1 on target before launch
  - Launch: command from weapon panel; missile leaves rail; WSO continues tracking target
  - Manual correction (if required): joystick input to keep reticle on target
  - Concentration: WSO cannot engage other tasks during Shturm guidance — 10–15 seconds of single-task focus
- **Employment Sequence (Step-by-Step DCS Cockpit Switchology):**
  - Pre-engagement: master arm → Shturm selected → missile type/pylon verified → PKV on target
  - Launch: fire → maintain PKV on target throughout flight
  - Post-shot: weapon count update → BDA → re-engage or safe
- **Engagement Envelopes:**
  - Minimum range: 400 m (guidance stabilization time — missile must travel far enough to enter guidance beam)
  - Maximum range: 5,000 m
  - Minimum altitude AGL: guidance geometry requirements
  - Maximum airspeed during engagement: steady flight constraint
  - Angle constraints: aspect angle on target for effective guidance geometry
  - Terrain masking: flight path must have clear LOS throughout missile flight
- **Tactical Employment Techniques:**
  - **Profile attack:** low-altitude approach → pop-up → stabilize → fire → guidance → break
  - **Running fire:** stabilized level flight at cruise; fire from cruising altitude; requires 10–15 sec straight-and-level
  - **Hull-down from terrain mask:** taxi to firing position → hover or slow flight → expose and fire → remask after shot
  - Multiple engagements: re-engagement timing after first shot
  - Ripple fire (if possible): sequential shots at multiple targets
  - Hand-off: pilot task during guidance (hands off weapons; maintain steady flight; monitor instruments)
- **Comparing Shturm to Western ATGMs:**
  - Shturm SACLOS vs. AGM-114 SAL (Hellfire): guidance concept differences; crew workload differences; accuracy comparison
  - Advantage: large warhead, long range, reliable radio guidance not dependent on laser spot quality
  - Disadvantage: requires steady flight; no fire-and-forget; radio jamming susceptibility
- **Shturm vs. Ataka (comparison preview):** key differences between the two Soviet ATGMs
- **Realism divergences (DCS vs. real 9M114)**
- **Common student errors with Shturm employment**

---

**Module 5: 9M120 Ataka ATGM Employment**
- **System Data:**
  - Designation: 9M120 Ataka (NATO: AT-9 Spiral-2); improved evolution of Shturm
  - Guidance: Radio-command SACLOS (same concept as Shturm but improved system)
  - Warhead variants available in DCS: HEAT (anti-armor); Thermobaric (blast/bunker); specify which are in DCS
  - HEAT warhead: 800+ mm RHA penetration (tandem charge on some variants)
  - Range: minimum ~400 m; maximum ~6,000 m; typical engagement: 2,000–5,000 m
  - Speed: ~400–550 m/s; faster than Shturm; shorter time-of-flight
- **Differences from Shturm:**
  - Greater range (6 km vs. 5 km)
  - Higher warhead penetration (tandem charge vs. single)
  - Thermobaric variant (specific targets)
  - Faster missile: shorter guidance time window
  - Same SACLOS guidance concept — same crew technique
- **Thermobaric Variant Employment:**
  - Target types suited to thermobaric warhead: bunkers, enclosed spaces, buildings, infantry in defilade
  - Employment parameters: how thermobaric warhead differs from HEAT in effects
  - When to select thermobaric vs. HEAT
- **Employment Sequence (DCS cockpit switchology):**
  - Variant selection (HEAT vs. thermobaric)
  - Pylon selection vs. Shturm pylon separation
  - Pre-launch, launch, guidance, post-shot — as Module 4 but noting Ataka-specific differences
- **Ataka Engagement Envelopes:**
  - Extended max range exploitation: 4,000–6,000 m engagement profile
  - Minimum range and guidance stabilization
  - Altitude and airspeed constraints (same steady-flight requirement)
- **Tactical Employment:**
  - Standoff engagement: using 5–6 km range to stay outside MANPADS envelope (~5 km for SA-16/SA-18)
  - Sequential Shturm / Ataka mixed loadout tactics
  - Re-engagement timing with faster missile
- **Realism divergences (DCS vs. real 9M120)**
- **Common student errors with Ataka (including warhead selection mistakes)**

---

**Module 6: Unguided Rocket Employment (S-5, S-8, S-13, S-24)**
- **Soviet Unguided Rocket System Overview:**
  - Naming convention: S = Snaryad (projectile); number = caliber in mm
  - Common launcher types: B-8V20A (S-8, 20-round), B-13L (S-13, 5-round), APU-68 (S-24, single)
  - Pylon integration: which pylons carry which launchers
  - Salvo settings: single, 2-round, 4-round, full pod (per system)
- **S-5 (57mm) Rockets:**
  - Warhead variants: S-5M (HE-Frag), S-5K (HEAT), S-5KO (HEAT-Frag), S-5MO (HE-Frag submunitions) — confirm which DCS models
  - Launcher: UB-16 (16-round pod) or UB-32 (32-round pod)
  - Range and accuracy: effective 400–1,200 m; close-range area fire
  - Employment: area suppression, anti-personnel, light vehicles
- **S-8 (80mm) Rockets:**
  - Warhead variants available in DCS: S-8KOM (HEAT, anti-armor), S-8TsM (incendiary/thermobaric), S-8BM (bunker penetrating), S-8OFP2 (HE-Frag) — confirm DCS availability
  - Launcher: B-8V20A (20-round pod)
  - Range: 1,000–4,000 m (effective accuracy varies by variant)
  - Employment: versatile — anti-armor (HEAT), structures, soft targets, area suppression
  - CCIP delivery system on Mi-24P for S-8
- **S-13 (122mm) Rockets:**
  - Warhead variants: S-13B (bunker/runway penetrating), S-13DF (HE-Frag), S-13T (tandem warhead) — confirm DCS availability
  - Launcher: B-13L (5-round pod)
  - Range: 1,500–3,000 m effective
  - Employment: hardened targets — bunkers, airfield infrastructure, light armor
  - Heavy punch at cost of limited quantity per pod
- **S-24 (240mm) Heavy Rocket:**
  - Single-round launcher: APU-68UM rail mount
  - Warhead: S-24B (HE, large blast-frag effect)
  - Range: 2,000–4,000 m typical; can be fired to ~6,000 m
  - Employment: blast/anti-materiel against hardened structures, bridges, large vehicles, concentrations
  - Very high recoil: airframe reaction; accuracy challenges; best at dive angles
- **CCIP Delivery System (Mi-24P):**
  - How the CCIP pipper is generated and displayed (DCS model)
  - Computation inputs: airspeed, altitude, dive angle, aircraft motion
  - PKV-1 sight role in rocket CCIP (WSO sight vs. pilot HUD indication)
  - Accuracy limitations of Mi-24P CCIP vs. Western systems
- **Rocket Employment Profiles (for each rocket family):**
  - **Diving attack (primary):** 15–25° dive; 180–240 km/h; range at release; break-off altitude and range; minimum pull-off altitude
  - **Shallow pass:** 5–10° dive; area suppression; range 1,000–2,000 m
  - **Running/Level fire:** reduced accuracy; suppression only; no recommended for precision effect
  - Entry altitude, approach geometry, and escape maneuver for each profile
- **Warhead Selection Guide (all rocket types):**
  - Target type → recommended rocket/warhead combination
  - When S-5 is preferred; when S-8 is better; when S-13/S-24 for heavy targets
- **Dispersion and Accuracy:**
  - Expected dispersion at various ranges by type
  - Factors: airspeed, altitude, dive angle, rotor vibration, aircraft stability
  - Techniques for accuracy improvement: stable platform, correct speed/angle, proper trim
- **Realism divergences (DCS vs. real Soviet rocket systems)**
- **Common student errors with rocket employment**

---

**Module 7: Air-to-Air Missiles — R-60 and R-73 (Self-Defense)**
- **Role and Doctrine:**
  - The Mi-24P is not a dogfighter — AAMs are for self-defense against helicopter threats and slow fixed-wing
  - Primary threat: enemy attack helicopters, slow fixed-wing (Bronco, Tucano, COIN), helicopters
  - Secondary threat: fast jets — limited engagement envelope; if a fast jet has a guns/missile solution on you, the best defense is low altitude + terrain masking + UV-26
  - AAM employment is a last resort after all evasive options are exhausted
- **R-60 (AA-8 Aphid):**
  - Type: short-range IR air-to-air missile; all-aspect seeker (DCS)
  - Range: minimum ~300 m; maximum ~5,000 m (effective ~3,000 m against maneuvering target)
  - G-limit: high-G seeker, suitable for crossing targets
  - Seeker acquisition: audio and visual tone/indication in cockpit
  - Variant in DCS: R-60 or R-60M (identify which is modeled)
- **R-73 (AA-11 Archer):**
  - Type: agile short-range IR air-to-air missile; all-aspect seeker; helmet cuing capability
  - Range: minimum ~300 m; maximum ~30 km (effective ~8–12 km against air targets)
  - Highly maneuverable: can track and engage crossing or off-boresight targets
  - Helmet Mounted Sight (HMD/HMS): if modeled in DCS, how it interacts with R-73 seeker cueing
  - Variant in DCS: confirm which R-73 variant is available
- **AAM Cockpit Procedures (DCS):**
  - Weapon selection: WSO selects AAM from weapons panel
  - Seeker activation: steps to slave seeker to target
  - Lock-on indication: audio tone (growl/ready tone); visual indication on HUD or sight
  - Launch constraints: check prior to firing
  - Fire: trigger or weapon release
  - Post-shot: maintain aspect if necessary; break away
- **Engagement Geometry:**
  - Helicopter vs. helicopter: closure, angles-off, maneuvering
  - R-60 vs. R-73 launch parameter comparison
  - Minimum altitude for safe employment (ensure missile clears terrain)
  - Deconfliction: avoid shooting into the ground or at friendly aircraft
- **Tactical Procedures:**
  - Threat detection via SPO-15 → react → maneuver → assess → engage if safe
  - Threat from below: difficult — helicopter's thermal signature vs. cold sky vs. terrain clutter
  - Threat from above: better acquisition opportunity
  - Break with countermeasures + AAM engagement sequence
- **Realism divergences (DCS vs. real R-60/R-73)**
- **Common student errors with AAM employment**

---

**Module 8: SPO-15 Beryoza RWR — Threat Detection & Analysis**
- **System Overview:**
  - Designation: SPO-15 "Beryoza" (Birch tree) — Radar Warning Receiver
  - Purpose: detects radar emissions from fire-control radars, SAM guidance radars, airborne intercept radars
  - Coverage: 360° azimuth; indicates bearing and emitter type
  - Display: circular azimuth display with threat icons; threat priority indicator
  - Audio: tonal and character alerts per threat type
- **Front Cockpit Controls (WSO Primary):**
  - Power switch: ON / OFF
  - Mode selection (if applicable in DCS)
  - Threat priority display interpretation
  - Muting audio alert without disabling the system
- **Pilot Cockpit (Rear) — SPO-15 Indication:**
  - What the pilot can see from rear cockpit (repeater or audio only)
  - Crew coordination: WSO calls threats to pilot using clock position and threat type
- **Threat Library (Soviet threat emitters):**
  - SA-6 (Kub/Gainful) — fire-control radar: ZP acquisition radar
  - SA-8 (Osa/Gecko) — combined acquisition/guidance
  - SA-9 (Strela-1) — optical/IR guided, no radar warning
  - SA-13 (Strela-10) — optical/IR, no radar warning
  - SA-15 (Tor/Gauntlet) — fire-control radar
  - SA-19 (Tunguska/Grison) — fire-control radar; also has guns
  - ZSU-23-4 (Shilka) — Gun Dish fire-control radar
  - ZU-23-2 — optically aimed, no radar; no RWR warning
  - Airborne threats: MiG-21/23/25 fire-control radars; AWACS
  - MANPADS (Igla, Strela-2): IR only; NO SPO-15 warning (critical awareness point)
- **SPO-15 Limitations:**
  - No warning for IR-guided threats (MANPADS, R-73, Python, AIM-9)
  - No warning for guns (ZU-23, Shilka in optical mode, small arms)
  - Coverage elevation limits (below certain depression angles may not detect)
  - Sensitivity: weak emitters at long range may not trigger
  - Confusion: multiple simultaneous emitters — priority logic
- **Threat Response Matrix:**
  - Detect → classify → assess → react
  - Priority: immediate SAM threat → terrain masking → countermeasures → evade → engage if possible
  - Response by threat type (SAM vs. AI radar vs. airborne)
- **Realism divergences (DCS SPO-15 implementation)**
- **Common student errors in RWR interpretation**

---

**Module 9: UV-26 Countermeasures — Chaff & Flares**
- **System Overview:**
  - Designation: UV-26 countermeasures dispenser
  - Payload: chaff cartridges and/or flare cartridges (mixed or separate — confirm DCS loadout configuration)
  - Launcher location: fuselage sides / tail area
  - Capacity: cartridge count per DCS implementation
- **Front Cockpit (WSO) Controls:**
  - Power switch
  - Program selector: AUTO, SEMI-AUTO, MANUAL modes (confirm DCS implementation)
  - Burst quantity and interval programming (if DCS models programming)
  - Dispense button (WSO-activated)
- **Pilot Cockpit (Rear) Controls:**
  - Manual single-dispense button (if accessible from rear cockpit)
  - Integration with SPO-15 auto-dispense (if modeled)
- **Chaff vs. Flares — Role:**
  - Chaff: effective against radar-guided missiles and radar fire control; creates false return in radar frequency
  - Flares: effective against IR-guided missiles; creates false heat source
  - MANPADS (Igla/Strela) — primarily IR threat: **flares are the primary response**
  - SA-6 / SA-8 type — radar guided: **chaff + evasive maneuver**
  - SA-15 / SA-19 — modern threats: combined chaff + flares + aggressive maneuver
- **Standard Dispense Programs:**
  - Single flare (manual, immediate response)
  - Flare program (burst of 4–8 on SPO-15 alert or on contact)
  - Chaff program
  - Combined program (chaff + flares interleaved)
  - How to set up programs in DCS UV-26 panel
- **Tactical Use Procedures:**
  - Pre-planned dispense on entry to threat area
  - Reactive dispense on SPO-15 alert or visual missile sighting
  - Break maneuver + countermeasures: technique for maximum effectiveness
  - Reloading considerations (in DCS, fixed per sortie — no in-flight reload)
  - Conservation: how many to save for egress
- **DCS Keyboard Reference:** default keys for single chaff, single flare, and program fire
- **Realism divergences (DCS UV-26 vs. real system)**
- **Common student errors with countermeasures**

---

**Module 10: Close Combat Attack (CCA) Tactics — Mi-24P Employment**
- **Soviet Attack Helicopter Doctrine:**
  - Mi-24P role in Soviet VVS / AA: mass employment, close support, anti-armor in main battle area
  - Paired or flight (pair of pairs) employment: standard Soviet tactical unit
  - Speed and surprise over stealth: the Mi-24P uses high speed (220–260 km/h) and terrain masking rather than hover-and-shoot tactics
  - Threat environment: Soviet planners assumed near-peer air defense (SA-6/8/9/13, ZSU-23-4, ZU-23-2, small arms); high-threat penetration tactics
- **Approach and Attack Profiles:**
  - **Low-level approach:** NOE (Nap-Of-Earth, 15–30 m AGL) to firing position; max use of terrain masking; fast ingress
  - **Pop-up attack:** climb from low level to firing altitude → identify target → fire → dive back to low level; used for ATGM or rockets requiring line-of-sight
  - **Diving attack:** enter from medium altitude (500–800 m); dive to firing parameters; fire; break off; escape at low level
  - **Running attack pass:** high-speed level or shallow-dive pass; fire rockets or cannon in a single pass; immediate break
  - Entry procedures, release/fire points, break-off maneuvers and recovery for each profile
- **Target Prioritization:**
  - Air defense assets first (AAA, MANPADS, SAMs) if suppressable
  - Command vehicles, forward observers
  - Anti-tank weapons threatening own ground forces
  - Armor in order of threat (MBTs > IFVs > APCs)
  - Logistics and resupply
- **Threat Reactions In The Attack:**
  - AAA environment: jinking, irregular flight path on approach; speed on break-off
  - MANPADS threat: flares + hard break; stay below minimum engagement altitude of advanced MANPADS
  - SAM threat: terrain masking; avoid prolonged level flight; chaff + maneuver
  - Air threat (fighter, enemy helicopter): transition to defensive; notify wingman; consider AAM if necessary
- **Crew Coordination During Weapons Employment:**
  - Standard crew calls (Soviet convention and DCS equivalents):
    - "Target identified" — WSO calls target bearing and type
    - "Ready to fire" — WSO confirms ATGM ready
    - "Fire" — WSO fires; pilot maintains steady flight
    - "Splash" / "Miss" — WSO assesses
    - "Break [direction]" — threat call; pilot executes
  - Single-player adaptation: seat switching management during attack
  - Autopilot technique during ATGM engagement to stabilize aircraft while WSO guides
- **Formation Tactics:**
  - Wingman responsibilities
  - Lead / trail attack: lead fires; trail covers; then roles reverse
  - Mutual support against air threats
  - Communication and deconfliction
- **Mission Planning Considerations:**
  - Threat analysis: what air defenses are in the AO?
  - Loadout selection by mission: anti-armor, anti-soft, mixed, SEAD (gun/rockets only on AAA suppression)
  - Fuel planning: combat radius, loiter, reserve
  - Ingress/egress routing: terrain masking, threat avoidance
  - Weather and visibility: Mi-24P is day-VFR limited (no FLIR); minimum visibility and ceiling for effective employment
- **DCS Mission Editor Application:**
  - Building a training scenario for CCA tactics
  - Threat placement, spacing, and rules of engagement
  - Score/assessment: hits, misses, exposure time
- **Realism divergences (DCS CCA vs. real Soviet tactics)**
- **Common student errors in CCA employment**

---

**Module 11: Weapons Loading, Weight & Performance Considerations**
- **Standard Loadout Configurations (with DCS mission editor setup):**
  - Anti-armor (maximum ATGM): 4 × Ataka + 2 × S-8 pods
  - Close support (rockets + cannon): 4 × S-8 pods or mixed S-8/S-13
  - Heavy support: 4 × S-24 (if pylon-compatible); mass detonation effect
  - Self-defense loaded: 2 × R-60/R-73 + 2 × S-8 + 2 × Ataka
  - Light reconnaissance: minimal ordnance; fuel priority
- **Weight Limits and Performance Impact:**
  - Maximum all-up weight by loadout: confirm DCS modeled limits
  - OGE hover ceiling as a function of gross weight (table by weight)
  - Rate of climb vs. gross weight
  - VNE considerations with heavy external stores
  - Taxi and taxiway restrictions with full loadout
- **Jettison Procedures:**
  - Emergency jettison: all stores; location of emergency jettison control (WSO panel)
  - Selective jettison: single pylon or specific store
  - Jettison sequences and safety considerations (fusing on jettisoned ordnance)
  - Fuel remaining after jettison: performance recovery
- **Arming and De-Arming (Real-World Context for Realism Awareness):**
  - How real weapons are armed (fusing, arming wires) vs. DCS weapons panel arming
  - Ground crew role in real ops; DCS simplification
  - Hot-loading/hot-arming procedures (if relevant to DCS mission editor)

---

**Output Format Requirements:**

For each module, provide:

1. **Learning Objectives** — 5–8 bullet points the student must be able to do or describe upon completion
2. **Key Data Tables** — all numeric values in organized tables (ranges, speeds, altitudes, weights, rates of fire, etc.)
3. **Cockpit Switch Reference** — table of all relevant switches, panels, and controls with locations in both cockpits (pilot rear and WSO front), and DCS keyboard equivalents where applicable
4. **Step-by-Step Procedures** — numbered, switch-by-switch engagement/arming/delivery sequences for DCS
5. **Employment Parameters Table** — by profile (diving, level, pop-up, etc.) with entry altitude, airspeed, range at release, break-off altitude/range, minimum recovery altitude
6. **Instructor Notes / Common Student Errors** — table of most likely errors, consequences, and corrections
7. **Realism Divergence Footnotes** — all divergences between real-world sources and DCS behavior, marked with:
   > *⚠ Realism Divergence: [explanation]*

**Document Structure:**
- Header: "Research Dossier: Mi-24P Hind — Weapons Qualification Course (WQC)"
- Source material table with priority ranking
- Aircraft and module summary (reference — point to BQT dossier for full details)
- All 11 modules in sequence
- Appendix A: Weapons Quick Reference Card (all weapons, ranges, delivery parameters)
- Appendix B: Crew Coordination Quick Reference (standard crew calls, single-player seat switching guide)
- Appendix C: Threat / Countermeasures Matrix (threat type → recommended response)
- Footer disclaimer

**Writing Standards:**
- Use Soviet/Russian terminology for systems (with NATO equivalents in parentheses where relevant)
- Soviet metric units throughout: km/h, meters, °C, kg — include imperial equivalents in secondary column
- Maintain a professional, military aviation tone — not a guide or FAQ; a technical training document
- Procedures written in imperative (command) voice: "Select Ataka on weapons panel," not "You should select Ataka"
- Realism Divergences must be clearly separated from primary instruction — never mixed inline without a footnote
