Act as an expert military aviation instructor, U.S. Army OH-58D "Kiowa Warrior" instructor pilot, and DCS World subject-matter expert. I need you to compile a detailed research dossier for an **OH-58D Basic Qualification Training (BQT) Course**.

**Objective:**
Create a structured syllabus and technical research document covering all aspects of safe OH-58D operation from cold-and-dark startup through safe recovery. This is a **full-fidelity clickable cockpit module** (Polychop Simulations) — all procedures involve physical cockpit switches, panels, collective/cyclic controls, and HOTAS commands. Combat employment (weapons delivery, Hellfire engagement, close combat attack tactics) is **out of scope** for this course. However, the student must be introduced to the MMS (Mast-Mounted Sight) at a basic familiarization level, and to the navigation system (AHRS/GPS) at a basic navigation level.

**Source Material Priority:**
1.  **Real-World (Primary Truth):** Use real U.S. Army documentation wherever possible:
    *   *TM 1-1520-248-10 (Operator's Manual, OH-58D Kiowa Warrior)* — the authoritative primary source for systems, limitations, and procedures.
    *   *TM 1-1520-248-CL (Operator's and Crewmember's Checklist)* — condensed checklists and boldface/immediate-action emergency procedures.
    *   *AR 95-1 (Flight Regulations)* — Army flight rules, weather minimums, and general operating procedures.
    *   *TC 3-04.4 (Fundamentals of Flight)* — Army helicopter aerodynamics, aeronautical decision-making, and crew coordination.
    *   *TC 3-04.62 (Tactical Flight Procedures)* — tactical flight profiles and terrain flight techniques (for context only; tactical employment is out of scope).
    *   Any publicly available USAACE (U.S. Army Aviation Center of Excellence) training circulars or supplements for the OH-58D.
2.  **DCS Simulation (Secondary / Override):** Where the DCS OH-58D module (Polychop Simulations) diverges from real-world procedures (e.g., simplified FADEC behavior, altered rotor dynamics, absence of certain circuit breakers, compressed alignment times, simplified hydraulic modeling), **the DCS procedure is what the student will actually execute**. Document the DCS procedure as the primary instruction.
3.  **Divergence Footnotes:** Any time the real-world procedure differs from DCS, include a clearly marked footnote formatted as:
    > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

**Key Distinction — Rotary-Wing Fundamentals:**
The OH-58D is a **single-engine, light observation/scout helicopter** with a **four-blade, soft-in-plane (bearingless) main rotor system**. Unlike the two-blade teetering rotor of the UH-1H, the four-blade system stores more rotational energy and is less susceptible to mast bumping, but brings its own characteristics the student must internalize:
*   **Rotor RPM (Nr) management** is life-critical. The T703-AD-700A engine with **FADEC (Full Authority Digital Engine Control)** manages Nr automatically in normal mode, but the pilot must recognize and respond to FADEC failures requiring manual throttle operation.
*   **Collective/cyclic/pedal coordination** replaces the throttle/stick/rudder mental model. All three controls are interdependent — changing collective changes yaw, changing cyclic changes required collective, etc.
*   **Hover is a learned skill** with no fixed-wing equivalent. Significant course time will be devoted to hover work (stationary, taxi, turns, sideward, rearward).
*   **The OH-58D is a light, power-limited helicopter.** At high density altitude or with weapons loaded, power margin can be very thin. Power management awareness is critical throughout all phases of flight.
*   **Loss of Tail Rotor Effectiveness (LTE)** and **settling with power (vortex ring state)** are rotary-wing-specific emergencies that the student must understand deeply.
*   **Single-engine helicopter emergency = autorotation.** There is no "single-engine cruise" option. Engine failure requires immediate autorotation entry.
*   **Ground resonance** is a concern specific to helicopters with lead-lag articulation (soft-in-plane systems). The student must recognize it and execute the correct immediate action (fly away if Nr is sufficient, or immediate shutdown if on the ground with low Nr).

**Key Distinction — DCS Module (Polychop Simulations):**
The DCS OH-58D is a **full-fidelity, clickable cockpit module**. Every switch, dial, and panel is interactive. The cockpit features a **mix of analog instruments and digital systems** — conventional steam gauges for flight and engine instruments alongside the **MFD (Multi-Function Display)** for navigation, sensor management, and weapons employment. This course must teach the student to interact with the physical cockpit — not just memorize keybinds. Procedures should reference cockpit switch positions, panel locations, and collective/cyclic/pedal inputs. Where keyboard shortcuts exist as alternatives, note them, but the primary instruction should be "hands in the cockpit."

**Key Distinction — Hybrid Analog/Digital Cockpit:**
The OH-58D combines **analog steam gauges** (flight instruments, engine instruments) with **digital avionics** (MFD, AHRS/GPS, MMS controller). This is a transitional-era cockpit — more capable than the fully analog UH-1H but not a full glass cockpit. The student must learn to:
*   **Scan analog instruments** efficiently (radial scan pattern centered on the attitude indicator) for flight and engine data.
*   **Operate the MFD** for navigation waypoints, moving map, sensor control, and systems pages.
*   **Use AHRS/GPS navigation** — the OH-58D has digital waypoint navigation, unlike the ADF/VOR-only UH-1H.
*   **Tune radios** using the radio control heads on the center pedestal.
*   **Monitor engine health** via individual analog gauges (Torque, TOT, N1, Nr) — no EICAS or digital engine display.

**Required Research Modules:**

**Module 1: Aircraft Systems & Aerodynamics**
*   T703-AD-700A Rolls-Royce (Allison) turboshaft engine: FADEC operation (auto mode vs. manual/backup mode), start cycle (N1/Ng ramp, TOT monitoring, fuel introduction via FADEC), spool-up characteristics, power available vs. power required, idle behavior (ground idle vs. flight idle), engine limitations (continuous, transient, starting TOT limits), power output (~650 SHP), engine oil system, compressor stall.
*   FADEC (Full Authority Digital Engine Control): detailed explanation of what it manages (fuel metering, Nr governing, torque limiting, TOT limiting, start sequencing), auto mode vs. manual/backup mode, failure indicators (FADEC caution light), FADEC-OFF handling qualities (pilot must manually manage throttle — correlator provides baseline, but fine RPM control is manual), training emphasis on manual throttle proficiency.
*   Rotor system: main rotor (4-blade, soft-in-plane/bearingless, composite construction), tail rotor (2-blade), rotor RPM (Nr) governing via FADEC, normal operating RPM range, autorotation RPM range, blade stall characteristics at high gross weight/altitude/G, rotor inertia and energy storage compared to 2-blade systems.
*   Transmission system: main transmission, tail rotor gearbox, freewheeling unit (for autorotation), power limits (torque continuous vs. transient in percent or ft-lbs), oil temperature and pressure limits, chip detector indications.
*   Fuel system: internal fuel capacity (~110 US gallons / ~730 lbs JP-8), fuel boost pump, fuel filter bypass, fuel quantity indication (pounds), low-fuel warnings, fuel consumption at various power settings, crossfeed (if applicable), crashworthy fuel cells.
*   Hydraulic system: single hydraulic system (irreversible servo-actuated flight controls), hydraulic pump (engine-driven), hydraulic pressure and temperature indications, hydraulic failure handling (controls become extremely heavy but flyable), hydraulic accumulator.
*   Electrical system: DC starter-generator (28V), battery, essential/non-essential bus, generator failure behavior, battery endurance, external power receptacle, circuit breaker panels.
*   Flight control system: mechanical mixing (collective-to-yaw, collective-to-cyclic coupling), force trim (magnetic brake system on cyclic and pedals), SAS/SCAS (if modeled in DCS — what it does, engagement, failure indications), hydraulic boost.
*   Survivability features: crashworthy fuel cells, energy-absorbing seats, armored crew seats, IR suppressor (Black Hole exhaust), wire strike protection system (WSPS) — note which are modeled in DCS.
*   Rotary-wing aerodynamics specific to the OH-58D:
    *   Translating tendency (left drift in hover for U.S. helicopters with counterclockwise main rotor).
    *   Translational lift (ETL): speed at which it occurs (~16–24 knots), indications (vibration decrease, nose pitch up, left yaw tendency), required control inputs.
    *   Transverse flow effect and its impact in transition.
    *   Retreating blade stall: what causes it, symptoms, recovery, relationship to Vne.
    *   Dissymmetry of lift and flapping.
    *   Ground effect vs. out-of-ground-effect (IGE vs. OGE) hover performance.
    *   Settling with power (vortex ring state): conditions (<30 kts airspeed, >300 fpm descent, high power), recognition, recovery (forward cyclic, reduce collective, gain airspeed).
    *   Loss of Tail Rotor Effectiveness (LTE): critical wind azimuths (main rotor vortex interference, weathercock instability, tail rotor vortex ring state), recognition (uncommanded right yaw), recovery (forward cyclic first to gain airspeed).
    *   Mast bumping: what causes it (low G, negative G, abrupt cyclic), prevention, why it is catastrophic. Note: 4-blade soft-in-plane rotor is less susceptible than 2-blade teetering systems, but low-G pushovers remain prohibited.
    *   Pendular action and dynamic rollover: causes, recognition, prevention during slope operations and confined area takeoffs.
    *   Ground resonance: **especially relevant for the soft-in-plane rotor system** — conditions that cause it (hard surface, one skid contact, unbalanced condition, lead-lag damper degradation), recognition (violent oscillation building rapidly), immediate action (full up collective to fly away if Nr sufficient; or immediate shutdown if on ground with low Nr).

**Module 2: Cockpit Familiarization**
*   Cockpit layout: left console, right console, instrument panel (pilot and copilot sides), center pedestal, overhead console — describe each major panel and its primary function.
*   **Overhead console:** Engine start controls, fuel valve, battery/generator switches, pitot heat, engine anti-ice, FADEC mode select, RPM warning audio, caution light test.
*   **Instrument panel:**
    *   **Pilot's flight instruments:** Attitude indicator, airspeed indicator (knots), barometric altimeter, vertical speed indicator, heading indicator / HSI, turn-and-slip indicator (slip ball critical for coordinated flight and tail rotor failure detection).
    *   **Engine instruments:** Torque gauge (Q — percent or ft-lbs), TOT (Turbine Outlet Temperature), gas producer (N1/Ng), rotor RPM (Nr) and engine RPM dual tachometer, fuel flow, engine oil pressure and temperature, transmission oil pressure and temperature.
    *   **Caution/advisory panel:** Master caution light, individual caution indicators (ENGINE OIL, XMSN OIL, FUEL BOOST, FADEC, CHIP DET, etc.), fire warning (T-handle).
*   **MFD (Multi-Function Display):** Power-on sequence, default pages, bezel button nomenclature (OSB — Option Select Buttons), basic page navigation (NAV, ENG, WPN, SYS pages), brightness control.
*   **MMS (Mast-Mounted Sight) controller:** Physical location (copilot side, but pilot can access), basic operation overview (TV daylight, thermal/FLIR, laser range finder/designator). Familiarization only — tactical sensor employment is out of scope.
*   **Weapon panel:** Location, ARM/SAFE switch positions, weapon select knob/switch. Identification only — employment is out of scope.
*   **Center pedestal — Radios:**
    *   ARC-201 (VHF/FM): frequency range, tuning method, usage (tactical/inter-flight communication).
    *   ARC-164 (UHF-AM): frequency range, preset channels, manual tune, guard frequency (243.0 MHz).
    *   Additional radios if modeled (VHF-AM for ATC).
    *   Audio panel / ICS: radio select switches, volume controls, ICS/radio priority, hot mic configuration.
*   **AHRS/GPS navigation system:** Location (MFD interface), basic waypoint display, bearing/distance readout, moving map.
*   **Radar altimeter:** Setting, reading, low-altitude warning bug.
*   **Pilot controls — Collective and cyclic:**
    *   Collective grip: throttle (FADEC manages — twist-grip may be detent or full-range depending on module fidelity), idle stop release, landing light switch, searchlight control, radio trigger positions.
    *   Cyclic grip: force trim release button, MMS slew (if pilot-accessible), weapons release (if configured), cargo release.
    *   Pedals: anti-torque pedals, adjustment mechanism.
*   Lighting: cockpit lighting controls (instrument lights, console lights, dome light), exterior lights (position/nav lights, anti-collision beacon, landing light, searchlight, IR formation lights), ANVIS NVG compatibility.

**Module 3: Communications**
*   Radio systems overview: the OH-58D has **UHF-AM (ARC-164)** and **VHF/FM (ARC-201)** radios, plus an **intercom (ICS)** system. The student must learn to:
    *   Tune each radio using the control head on the center pedestal (frequency selectors, preset channels where available).
    *   Select which radio to transmit on using the audio control panel.
    *   Monitor multiple frequencies simultaneously (UHF for ATC/common, FM for tactical/inter-flight).
    *   Use proper radio phraseology (FAA/ICAO for ATC communications, military brevity for tactical comms).
*   Audio control panel / ICS: radio select switches, volume controls, ICS positions (pilot, copilot), hot mic vs. keyed transmit, ICS priority.
*   Intercom system: hot mic configuration, crew communication during critical phases (startup, hover, landing), keying technique (collective trigger positions — typically 1st detent ICS, 2nd detent radio transmit).
*   Common radio calls for the BQT environment: startup clearance, taxi, takeoff clearance, pattern calls (crosswind, downwind, base, final), approach/landing clearance, go-around advisory, shutdown advisory.
*   Guard frequency monitoring (UHF 243.0 MHz / VHF 121.5 MHz).
*   DCS-specific: how radio keybinds map to cockpit switches, Easy Communication mode vs. realistic radio operation, SRS (SimpleRadio Standalone) integration notes if applicable.

**Module 4: Ground Operations**
*   Cold-and-dark startup: **full switch-by-switch procedure** from battery ON through engine running and avionics alive.
    *   Battery ON → caution panel check → warning light test.
    *   Fuel boost pump ON → fuel pressure indication.
    *   Engine start sequence: FADEC-initiated start (throttle to IDLE detent or START), N1/Ng monitoring, TOT monitoring, abort criteria (hot start [TOT exceeding limits], hung start [N1 stagnates], no light-off [no TOT rise]).
    *   Post-start stabilization: engine at ground idle, FADEC governing Nr, TOT settling within limits.
    *   Generator ON → electrical bus powered.
    *   Avionics power-on: MFD boot sequence, AHRS/GPS initialization, radios, transponder.
    *   Hydraulic system check: pressure indication, flight control check (full cyclic/collective/pedal deflection — smooth and light with hydraulics).
*   **AHRS/GPS alignment:**
    *   Alignment procedure: how to initiate, duration, status indications on MFD, when alignment quality is sufficient for navigation.
    *   DCS-specific alignment time vs. real-world (real-world may require several minutes; DCS may compress this).
*   Flight control rigging / before-takeoff check: force trim check (set, verify hold, release, verify free), SAS engagement (if modeled), caution panel clear.
*   Rotor engagement: throttle to FLY (flight idle), Nr rising to governed RPM, rotor smoothing, FADEC managing power.
*   Ground taxi (hover taxi): techniques for hovering forward at low altitude (<3 ft skid height), crosswind hover taxi, NVG taxi considerations.
*   Pre-takeoff checks: engine instruments in limits, torque available check (power check — compare hover torque against continuous limit), caution panel clear, flight controls free and correct, force trim operational, radios set and checked, altimeter set, transponder set, AHRS/GPS aligned and verified.
*   Engine run-up and systems check: FADEC status verification, all caution lights extinguished, crew brief (intentions, abort criteria, emergency plan).

**Module 5: Hover & Takeoff**
*   Hover technique:
    *   Picking up to a hover: smooth collective application, coordinating pedals (left pedal as collective increases), cyclic corrections to maintain position, achieving a stable 3–5 ft hover.
    *   Stationary hover: maintaining position/heading/altitude using outside references, scan pattern (reference point, horizon, instruments, repeat).
    *   Hover power check: verifying power required vs. power available at current weight/altitude/temperature using torque gauge. Can we take off? Determine if OGE operations are available.
    *   Hover turns (pedal turns): 360° turns maintaining position and altitude, coordination of cyclic to compensate for translating tendency changes during the turn.
    *   Hover taxi: forward, sideward, and rearward flight at hover taxi speeds (<20 knots ground speed), obstacle awareness, crew coordination calls.
*   Takeoff profiles:
    *   Normal takeoff: from a stable 3–5 ft hover, accelerate through ETL (expect vibration, nose pitch up, left yaw — apply right pedal and forward cyclic), positive rate of climb, continue to climb speed.
    *   No-hover takeoff (performance limited): technique for departing without establishing a full hover — remain in ground effect, accelerate through ETL, transition to climb.
    *   Maximum performance takeoff: when and why to use it, technique (climb vertically to clear obstacles, then accelerate).
    *   Running takeoff: technique for departing with minimal hover time when severely power-limited — skid slide, ground effect acceleration, ETL transition.
*   Climb profile: Vy (best rate of climb speed — ~55–60 KIAS per TM), cruise climb (~80 KIAS), level-off technique (lower nose before target altitude, allow acceleration, reduce power to cruise).
*   Departure: standard VFR departure, communication procedures (departure call on tower frequency, switch to departure/area frequency).
*   **Ground resonance:** Detailed coverage — this is a real risk for the 4-blade soft-in-plane rotor system. Conditions, recognition (violent oscillation building rapidly), immediate action (full up collective to fly away if RPM sufficient; immediate engine shutdown if on ground with low RPM). Why hesitation or wrong action can be catastrophic.

**Module 6: Basic Flight Maneuvers**
*   Level flight: cruise speed (~80–100 KIAS), power settings for various altitudes, trim technique (force trim set — press and release trim button while holding desired control position).
*   Turns: coordinated turns using cyclic and pedals (step on the ball), load factor awareness, collective adjustment to maintain altitude in turns (more collective to compensate for increased load), bank angle vs. G-load, recommended max bank for normal operations (~30°).
*   Climbs and descents: recommended profiles, power management, Nr awareness during descents (FADEC compensates, but monitor for excursions), avoid rapid collective changes that could exceed FADEC response rate.
*   Slow flight: characteristics below ETL, transition back to hover regime, increasing power requirements, pedal requirements as speed decreases.
*   Speed changes: acceleration/deceleration, nose attitude and collective relationship, maintaining altitude during transitions.
*   Straight and level flight at various airspeeds: differences in control feel and power required at 40, 60, 80, 100 KIAS, vibration profile at each speed.
*   Autorotation entry (practice): recognition of engine failure cues (Nr decay, audio warning, yaw change, TOT drop), immediate actions (**lower collective immediately**, maintain Nr in autorotation range, establish autorotation airspeed ~60–80 KIAS per TM), power recovery at altitude (not full-down autorotation at this stage). Emphasis: even with the 4-blade rotor's greater inertia, prompt collective reduction is critical.
*   **Trim technique:** The OH-58D force trim (magnetic brake) system — how to set (press and release button while holding desired control position), release (press and hold), and re-trim. Why constant trimming is necessary as airspeed and power change.

**Module 7: Navigation (AHRS/GPS & Conventional)**
*   **AHRS/GPS navigation (primary):**
    *   Waypoint navigation: selecting waypoints on MFD, bearing/distance/ETA readout, direct-to navigation.
    *   Creating/modifying waypoints in the MFD/navigation system (if available in DCS).
    *   MFD navigation page: moving map display, map orientation (north-up vs. track-up), range/scale adjustment.
    *   HSI / heading indicator: setting heading bug, course to waypoint, CDI for tracking.
*   **Conventional navigation aids (backup / supplement):**
    *   TACAN (if modeled): tuning, reading bearing and DME.
    *   ADF (if modeled): tuning NDB frequencies, bearing interpretation.
*   **Radar altimeter:** Setting low-altitude warning bug, reading absolute altitude AGL, usage during low-level flight and approaches.
*   **Transponder:** Squawk code entry, modes (standby, normal, altitude reporting), ident function.
*   **Scope limitation:** This module covers basic "point A to point B" navigation. Mission planning, tactical route planning, and NOE (nap of the earth) flight are out of scope.

**Module 8: Emergency Procedures (Academic)**
*   **Boldface (Memory/Immediate Action) Items:** Per TM 1-1520-248-10 — these must be memorized verbatim:
    *   Engine failure in flight (autorotation entry)
    *   Engine failure at hover / near the ground
    *   Engine fire in flight
    *   Emergency engine shutdown
    *   FADEC failure (auto-to-manual transfer)
    *   Hydraulic system failure
    *   Tail rotor failure / loss of tail rotor thrust
    *   Mast bumping (low-G condition)
*   **Autorotation — full procedure:**
    *   Entry: immediate collective down, Nr into autorotation range, establish glide (~60–80 KIAS per TM for best glide).
    *   Glide: autorotation airspeed for max range vs. min rate of descent, Nr management (collective adjustments), turn to selected landing area.
    *   Flare: at ~75–100 ft AGL, apply aft cyclic to reduce speed and arrest rate of descent, Nr increases during flare.
    *   Collective pull / cushion: at ~10–15 ft, level the aircraft, apply collective to cushion touchdown using stored rotor energy.
    *   Touchdown: slight nose-up attitude, level skids, slide to a stop.
    *   Straight-in, 90°, and 180° autorotation profiles.
*   Loss of Tail Rotor Effectiveness (LTE): wind conditions that cause it (main rotor vortex interference, weathercock instability, tail rotor vortex ring state — specific azimuths), recognition (uncommanded right yaw, inability to maintain heading), recovery procedure (forward cyclic to gain airspeed first; if altitude permits, reduce collective; if spin develops, enter autorotation).
*   Settling with power (vortex ring state): flight conditions that cause it (low airspeed <30 kts, high rate of descent >300 fpm, high power applied), recognition (high rate of descent despite power application, aircraft shudder), recovery (forward cyclic, reduce collective, gain airspeed to fly out).
*   FADEC failure: recognition (FADEC caution light, Nr excursions, power fluctuations), immediate action (FADEC mode switch to MANUAL/BACKUP), manual throttle control technique (correlator provides baseline, pilot fine-tunes with twist-grip), handling qualities in manual mode, land as soon as practicable.
*   Hydraulic failure: identification (controls become very heavy, master caution), flight characteristics without hydraulics (flyable but requires significant force), recommended approach (shallow approach, run-on landing to avoid hover work without hydraulics).
*   Electrical failure: generator loss, bus load shedding, battery-only endurance, reduced avionics prioritization (MFD, AHRS/GPS, radios — what to keep vs. shed).
*   Transmission failure indications: chip detector light, oil pressure/temperature exceedances, noise/vibration — land as soon as possible vs. land as soon as practicable.
*   Mast bumping: conditions to avoid (low G, pushovers, abrupt cyclic, turbulence at light gross weight), why recovery is not possible once mast contact occurs, training emphasis on smooth control inputs. Note the 4-blade soft-in-plane rotor is less susceptible than a teetering system, but the prohibition on low-G flight remains.
*   Dynamic rollover: conditions that cause it (slope operations, crosswind, skid caught on obstacle), recognition (helicopter rolling despite opposite cyclic), prevention (limit roll rate during slope operations), recovery (reduce collective if caught early).
*   Ground resonance: reiterate emergency procedure — fly away or shut down. Critical to distinguish based on Nr.
*   **DCS-specific emergency notes:** Which failures DCS actually models vs. which are simplified or absent. How to trigger practice emergencies in DCS (mission editor failure triggers). Note any differences in flight model behavior during emergencies compared to real-world expectations.

**Module 9: Approach & Landing**
*   VFR traffic pattern: pattern altitude (typically 800–1,000 ft AGL), downwind leg (parallel to landing direction, ~500–800m lateral distance), base turn, final approach. Airspeeds at each leg.
*   Normal approach: from pattern altitude, decelerating approach from ~60–80 KIAS, progressive collective reduction, constant angle approach (aim point stays fixed in windscreen), transition to hover at intended landing point, vertical descent to touchdown.
*   Steep approach: when to use (obstacles, confined areas), technique (~10–15° glide path), power management, abort criteria.
*   Shallow approach / running landing: when to use (high gross weight, high density altitude, limited power margin), technique — touchdown with 20–30 knots forward speed and slide to a stop on skids.
*   Hover to landing: transitioning from a stable hover to ground contact, slow collective reduction, feeling for the ground, prevent lateral drift at touchdown.
*   Go-around / wave-off: recognition of unstable approach (too fast, too high, too low, not aligned), power application, climb-out and re-enter pattern.
*   Crosswind approach and landing: wind effect on approach, LTE awareness on final (especially right quartering tailwinds), pedal requirements, drift correction techniques.
*   Slope landing: technique (uphill skid contacts first), limitations (lateral slope limits, fore/aft limits), dynamic rollover awareness, collective management on slopes.
*   Confined area operations: high/low recon, power check, approach angle selection, escape route identification, ground crew coordination, power management in ground effect.
*   Pinnacle and ridgeline operations: wind effects, approach techniques, power management OGE, escape routes.
*   **DCS-specific:** Ground handling and skid interaction in DCS, autostart behavior (for reference only — the student must learn manual procedures), DCS wind and weather effects on approach.

**Module 10: Shutdown & Post-Flight**
*   Post-landing: hover to parking spot, set down, verify stable on ground (skids firmly planted, no lateral drift).
*   Shutdown procedure:
    *   Throttle to IDLE (engine at ground idle, Nr decreasing to idle governed RPM).
    *   Wait for stabilization: TOT settling, Nr at idle.
    *   Avionics OFF: MFD off, AHRS/GPS off, radios off, transponder off (or standby).
    *   Throttle to OFF (fuel shutoff): engine spools down, TOT drops, Nr decays.
    *   Monitor engine spool-down: N1 decreasing to zero, TOT cooling, rotor slowing and stopping.
    *   Generator OFF.
    *   Fuel boost pump OFF, fuel valve OFF.
    *   Battery OFF.
*   Post-shutdown checks: rotor stopped, all switches verified OFF, tie-down rotor blades (if applicable), MMS stowed, security of cargo/cabin, close doors.
*   Full switch-by-switch shutdown from engine running to cold-and-dark.
*   Rotor brake (if modeled in DCS): when to apply, technique — note whether DCS models this or if rotor coasts to stop.

**For each module, provide:**
1.  **Learning Objectives:** Measurable outcomes the student must demonstrate.
2.  **Key Data Table:** Rotor RPM limits (power-on, autorotation, transient), torque limits (continuous, transient), TOT limits (continuous, transient, starting), V-speeds (Vy, Vne, autorotation best glide, autorotation min sink), fuel flow figures, oil pressure/temperature limits — with normal ranges and caution/warning thresholds.
3.  **Cockpit Switch Reference:** Specific switch names, panel locations, and the DCS mouse-click or collective/cyclic HOTAS action to operate them. Include keyboard shortcuts as secondary reference where they exist.
4.  **Instructor Notes:** Common student failure points and how to address them. Focus on the most frequent errors seen in DCS (e.g., over-torquing on takeoff, failing to manage Nr in autorotation practice, LTE encounters during hover pedal turns, ham-fisting the collective during hover work, ground resonance panic, FADEC failure surprise, forgetting AHRS alignment before departure).
5.  **Realism Divergence Footnotes:** Where DCS simplifies or omits real-world procedures. Format as:
    > *⚠ Realism Divergence: [explanation]*

**Output Format:**
A single, structured Markdown document suitable for saving as `.github/research/oh-58d-bqt-dossier.md`. Use heading levels ##, ###, and #### consistently. Tables for all data. Cockpit switch locations described by panel name (e.g., "Left console — Fuel Panel", "Overhead console — Engine Start panel", "Instrument panel — Engine gauges"). All performance data in U.S. customary units (knots, feet, pounds, Fahrenheit) with metric conversions in parentheses where helpful.
