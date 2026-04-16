Act as an expert military aviation instructor, U.S. Army UH-1H "Huey" instructor pilot, and DCS World subject-matter expert. I need you to compile a detailed research dossier for a **UH-1H Basic Qualification Training (BQT) Course**.

**Objective:**
Create a structured syllabus and technical research document covering all aspects of safe UH-1H operation from cold-and-dark startup through safe recovery. This is a **full-fidelity clickable cockpit module** (Belsimtek / Eagle Dynamics) — all procedures involve physical cockpit switches, panels, collective/cyclic controls, and HOTAS commands. The UH-1H is a **utility transport helicopter** — while it can be armed with door guns and rocket pods, weapons employment is **out of scope** for this course. However, the student must be introduced to the weapons panel and armament switches at a basic familiarization level. The student must learn to manage the engine, radios, and navigation systems to a proficient level.

**Source Material Priority:**
1.  **Real-World (Primary Truth):** Use real U.S. Army documentation wherever possible:
    *   *TM 55-1520-210-10 (Operator's Manual, UH-1H/V)* — the authoritative primary source for systems, limitations, and procedures.
    *   *TM 55-1520-210-CL (Operator's and Crewmember's Checklist)* — condensed checklists and boldface/immediate-action emergency procedures.
    *   *AR 95-1 (Flight Regulations)* — Army flight rules, weather minimums, and general operating procedures.
    *   *TC 3-04.4 (Fundamentals of Flight)* — Army helicopter aerodynamics, aeronautical decision-making, and crew coordination.
    *   *FM 1-240 (Utility and Cargo Helicopter Operations)* — doctrine for UH-1 series tactical employment and standard flight procedures.
    *   Any publicly available USAACE (U.S. Army Aviation Center of Excellence) training circulars, ATMs (Aircrew Training Manuals), or supplements for the UH-1H.
2.  **DCS Simulation (Secondary / Override):** Where the DCS UH-1H module (Belsimtek / Eagle Dynamics) diverges from real-world procedures (e.g., simplified governor behavior, altered rotor dynamics, absence of certain circuit breakers, compressed warm-up times, simplified hydraulic modeling, or flight model idiosyncrasies), **the DCS procedure is what the student will actually execute**. Document the DCS procedure as the primary instruction.
3.  **Divergence Footnotes:** Any time the real-world procedure differs from DCS, include a clearly marked footnote formatted as:
    > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

**Key Distinction — Rotary-Wing Fundamentals:**
The UH-1H is a **single-engine, medium utility helicopter** with a **two-blade, semi-rigid (teetering) main rotor system**. This is one of the most distinctive and important characteristics of the aircraft. Unlike fully articulated rotor systems, the teetering rotor has unique flight characteristics the student must internalize:
*   **Rotor RPM (Nr) management** is life-critical. The UH-1H uses a **throttle correlator** linked to the collective (raising collective increases fuel flow) combined with a **governor** that fine-tunes RPM. The pilot must understand how the correlator and governor interact, and must be prepared to manage RPM manually with the twist-grip throttle if the governor fails.
*   **Collective/cyclic/pedal coordination** replaces the throttle/stick/rudder mental model. All three controls are interdependent — changing collective changes yaw, changing cyclic changes required collective, etc.
*   **Hover is a learned skill** with no fixed-wing equivalent. Significant course time will be devoted to hover work (stationary, taxi, turns, sideward, rearward).
*   **Two-blade teetering rotor** produces a characteristic "Huey thump" (low-frequency blade slap) and has specific handling qualities:
    *   Susceptible to **mast bumping** under low-G or negative-G conditions. Low-G pushovers are immediately dangerous.
    *   Produces a distinctive **2-per-rev vibration** (two beats per revolution) that increases with airspeed and is normal within limits.
    *   **Retreating blade stall** occurs at a lower airspeed than fully articulated systems due to the rotor design.
*   **Loss of Tail Rotor Effectiveness (LTE)** and **settling with power (vortex ring state)** are rotary-wing-specific emergencies that the student must understand deeply.
*   **Single-engine helicopter emergency = autorotation.** There is no "single-engine cruise" option. Engine failure requires immediate autorotation entry. The UH-1H's two-blade rotor stores less energy than multi-blade systems, making prompt collective reduction critical.

**Key Distinction — DCS Module (Belsimtek / Eagle Dynamics):**
The DCS UH-1H is a **full-fidelity, clickable cockpit module** and was one of the first high-fidelity helicopter modules in DCS World. Every switch, dial, circuit breaker, and panel is interactive. The cockpit models both the **pilot (right seat)** and **copilot (left seat)** stations, though the player primarily operates from the pilot seat. This course must teach the student to interact with the physical cockpit — not just memorize keybinds. Procedures should reference cockpit switch positions, panel locations, and collective/cyclic/pedal inputs. Where keyboard shortcuts exist as alternatives, note them, but the primary instruction should be "hands in the cockpit."

**Key Distinction — Analog Cockpit:**
The UH-1H has a **fully analog cockpit** with **no digital displays, MFDs, or glass cockpit systems**. All navigation, engine monitoring, and flight reference is via **steam gauges** and analog radios. This is a fundamentally different experience from modern glass-cockpit helicopters. The student must learn to:
*   **Scan analog instruments** efficiently (radial scan pattern centered on the attitude indicator).
*   **Tune radios manually** using frequency knobs (no preset digital channels).
*   **Navigate using ADF, VOR/ILS, and dead reckoning** — there is no GPS, no moving map, no digital waypoints.
*   **Monitor engine health** via individual analog gauges (no EICAS, no caution advisory computer).

**Required Research Modules:**

**Module 1: Aircraft Systems & Aerodynamics**
*   T53-L-13B Lycoming turboshaft engine: start cycle (N1 spool, exhaust gas temperature/EGT monitoring, fuel introduction), spool-up characteristics, idle behavior, power output (1,400 SHP), engine limitations (continuous, transient, starting EGT limits), throttle correlator and governor operation, manual throttle control, engine oil system, compressor stall.
*   Rotor system: main rotor (2-blade, semi-rigid/teetering, 48-ft diameter), tail rotor (2-blade, left side, pusher configuration), rotor RPM (Nr) governing (correlator + governor), normal operating RPM (324 RPM / 6600 RPM engine), autorotation RPM range, stabilizer bar ("Bell bar") function and effect on handling, droop compensator.
*   Transmission system: main transmission (42° gearbox), tail rotor driveshaft and gearbox, freewheeling unit (for autorotation), transmission oil system (temperature and pressure limits), torque measurement.
*   Fuel system: fuel cell locations and capacity (~210 US gallons / 1,390 lbs), fuel boost pump, fuel filter bypass, fuel quantity indication, low-fuel warning, fuel consumption at various power settings, cross-feed (if applicable).
*   Hydraulic system: single hydraulic system (irreversible servo-actuated flight controls), hydraulic pump (engine-driven), hydraulic pressure and temperature indications, hydraulic failure handling (controls become extremely heavy but flyable), hydraulic accumulator.
*   Electrical system: DC starter-generator (28V), AC inverter, main battery, external power receptacle, essential/non-essential bus, generator failure behavior, battery endurance, circuit breaker panels (pilot and copilot sides).
*   SAS/SCAS (Stability Augmentation System): if modeled in DCS — what it does, engagement, failure indications, flight without SAS.
*   Force trim system: magnetic brake system on cyclic and pedals, how to set, release, and re-trim.
*   Rotary-wing aerodynamics specific to the UH-1H:
    *   Translating tendency (left drift in hover due to tail rotor thrust).
    *   Translational lift (ETL): speed at which it occurs (~16-24 knots), indications (vibration decrease, nose pitch up, left yaw tendency), required control inputs.
    *   Transverse flow effect and its impact in transition.
    *   Retreating blade stall: what causes it, symptoms, recovery, VNE relationship.
    *   Dissymmetry of lift and flapping (teetering rotor specific — the teetering hinge is the flapping solution).
    *   Ground effect vs. out-of-ground-effect (IGE vs. OGE) hover performance.
    *   Settling with power (vortex ring state): conditions, recognition, recovery.
    *   Loss of Tail Rotor Effectiveness (LTE): critical wind azimuths (main rotor vortex interference, weathercock instability, tail rotor vortex ring state), recognition, recovery.
    *   Mast bumping: **especially critical for the two-blade teetering rotor** — what causes it (low G, negative G, abrupt cyclic in low-G), prevention, why it is immediately catastrophic (mast separation). Emphasis: never push forward cyclic aggressively.
    *   Pendular action and dynamic rollover: causes, recognition, prevention during slope operations and confined area takeoffs.
    *   Blade stall and power settling at high density altitude and gross weight.

**Module 2: Cockpit Familiarization**
*   Cockpit layout: overhead console (engine controls, governor, fuel), center pedestal (radios), instrument panel (flight instruments, engine instruments, caution panel), left/right subpanels, circuit breaker panels — describe each major panel and its primary function.
*   **Overhead console:** Throttle quadrant (twist-grip on collective, but overhead has emergency fuel shutoff and governor switch area), fuel valve, battery/generator/inverter switches, pitot heat, engine anti-ice, RPM warning audio, caution light test.
*   **Instrument panel:**
    *   **Pilot's flight instruments:** Attitude indicator, airspeed indicator (knots), barometric altimeter, vertical speed indicator, gyro compass / directional gyro, turn-and-slip indicator (slip ball critical for coordinated flight and tail rotor failure detection).
    *   **Engine instruments:** Torque pressure gauge, exhaust gas temperature (EGT), gas producer (N1), rotor RPM (Nr) and engine RPM (N2) dual tachometer, fuel flow, engine oil pressure and temperature, transmission oil pressure and temperature.
    *   **Caution/advisory panel:** Master caution light, individual caution indicators (RPM, ENGINE OIL PRESS, XMSN OIL PRESS, FUEL BOOST, etc.), fire warning light (T-handle).
*   **Center pedestal — Radios:**
    *   AN/ARC-134 (VHF-AM): frequency range, tuning, usage (ATC, common traffic).
    *   AN/ARC-51BX (UHF-AM): frequency range, preset channels, manual tune, guard frequency.
    *   AN/ARC-131 (FM): frequency range, usage (tactical/inter-flight communication).
    *   Intercom (ICS): hot mic vs. cyclic trigger keying, crew positions, ICS volume.
*   **Navigation radios:**
    *   AN/ARN-83 ADF (Automatic Direction Finder): tuning, ADF needle on compass card, NDB approach basics.
    *   AN/ARN-82 VOR/ILS receiver: tuning, CDI (Course Deviation Indicator), ILS approach capability.
    *   Marker beacon receiver.
*   **Pilot controls — Collective and cyclic:**
    *   Collective grip: twist-grip throttle (correlator), idle stop release, landing light switch, searchlight control, radio trigger positions.
    *   Cyclic grip: force trim release button (important!), weapons release (if armed), cargo release.
    *   Pedals: anti-torque pedals, adjustment mechanism.
*   Lighting: cockpit lighting controls (instrument lights, console lights, dome light), exterior lights (position/nav lights, anti-collision beacon, landing light, searchlight), NVG compatibility (if modeled).
*   **Cargo hook and sling load** controls: location, release mechanism (pilot and copilot stations). Familiarization only — sling load operations are a separate skill.

**Module 3: Communications**
*   Radio operation fundamentals: the UH-1H has **three independent radios** (VHF-AM, UHF-AM, FM) and an intercom (ICS). The student must learn to:
    *   Tune each radio manually using frequency selector knobs.
    *   Select which radio to transmit on using the audio control panel.
    *   Monitor multiple frequencies simultaneously.
    *   Use proper radio phraseology (FAA/ICAO for ATC, military brevity for tactical comms).
*   Audio control panel: radio select switches, volume controls, ICS/radio priority.
*   Intercom system: hot mic configuration, ICS positions (pilot, copilot, crew), keying technique.
*   Common radio calls for the BQT environment: startup clearance, taxi, takeoff, pattern calls, approach/landing, shutdown advisory.
*   Guard frequency monitoring (UHF 243.0 MHz / VHF 121.5 MHz).
*   DCS-specific: how radio keybinds map to cockpit switches, Easy Communication mode vs. realistic radio operation, SRS (SimpleRadio Standalone) integration notes if applicable.

**Module 4: Ground Operations**
*   Cold-and-dark startup: **full switch-by-switch procedure** from battery ON through engine running and avionics alive.
    *   Battery ON → caution panel check → inverter ON → warning light test.
    *   Fuel valve ON → fuel boost pump ON → fuel pressure indication.
    *   Throttle to CLOSED (full idle stop), collective full down.
    *   Engine start sequence: starter button press, N1 rotation indication, EGT rise monitoring, throttle to IDLE at proper N1 (allow fuel introduction), N1/N2/Nr stabilization, abort criteria (hot start [EGT exceeding limits], hung start [N1 stagnates], no light-off [no EGT rise]).
    *   Post-start: engine stabilization at ground idle, Nr building to operating range, EGT settling within limits.
    *   Generator ON → load on bus, voltage check.
    *   Governor check: governor ON, verify RPM stabilization.
    *   Avionics power-on: radios, navigation equipment, transponder.
    *   Hydraulics check: hydraulic pressure indication, flight control check (full cyclic/collective/pedal deflection with hydraulics — smooth and light).
*   Throttle correlation and governor operation: **dedicated practice** — the student must understand and feel how the correlator changes fuel flow with collective, and how the governor fine-tunes. Practice: raise collective slowly, observe Nr, observe governor correction, observe EGT and torque changes.
*   Pre-takeoff checks (before takeoff checklist): engine instruments in limits, torque available check (power check — can we hover at this weight/altitude/temperature?), caution panel clear, flight controls free and correct, force trim operational, radios set and checked, altimeter set, transponder set, doors and cargo secure.
*   Rotor engagement: throttle from IDLE past the idle stop to FLY detent, Nr increasing to operating RPM (324 ± 3 RPM), rotor smoothing, low RPM warning audio check.
*   Ground taxi: the UH-1H taxis by **hover taxi** (no wheels) — technique for hovering forward at 3-5 ft skid height, crosswind hover taxi, taxiway awareness, obstacle clearance.
*   Engine run-up and systems check: mag check (N/A for turbine — but governor RPM check), systems verification, pre-takeoff brief.

**Module 5: Hover & Takeoff**
*   Hover technique:
    *   Picking up to a hover: smooth collective application, coordinating pedals (left pedal as collective increases for U.S. counterclockwise rotor), cyclic corrections to maintain position, achieving a stable 3-5 ft hover.
    *   Stationary hover: maintaining position/heading/altitude using outside references, scan pattern (reference point, horizon, instruments, repeat).
    *   Hover power check: verifying power required vs. power available at current weight/altitude/temperature using torque gauge. Can we take off?
    *   Hover turns (pedal turns): 360° turns maintaining position and altitude, coordination of cyclic to compensate for translating tendency changes.
    *   Hover taxi: forward, sideward, and rearward flight at hover taxi speeds (<20 knots ground speed), obstacle awareness, crew coordination calls.
*   Takeoff profiles:
    *   Normal takeoff: from a stable 3-5 ft hover, accelerate through ETL (expect vibration, nose pitch up, left yaw — apply right pedal and forward cyclic), positive rate of climb, continue to climb speed.
    *   No-hover takeoff (performance limited): technique for departing without establishing a full hover — used when power margin is insufficient for OGE hover.
    *   Maximum performance takeoff: when and why to use it, technique (vertical climb to clear obstacles, then accelerate).
    *   Running takeoff: technique for departing with minimal hover time, using ground effect during acceleration.
*   Climb profile: Vy (best rate of climb speed — ~60 KIAS), cruise climb (~80 KIAS), single-engine best rate of climb (N/A — single engine aircraft, but note best autorotation glide speed), level-off technique (lower nose before target altitude, allow acceleration, reduce power to cruise).
*   Departure: standard VFR departure, communication procedures (departure call on tower frequency, switch to departure/area freq).
*   **Ground resonance:** What it is, conditions that cause it (damaged lead-lag dampers — less likely on the teetering Huey rotor than fully articulated systems, but the student should understand the concept). The two-blade teetering rotor is generally less susceptible, but the concept must be understood.

**Module 6: Basic Flight Maneuvers**
*   Level flight: cruise speed (~90-100 KIAS), power settings for various altitudes, trim technique (force trim set — release button, hold desired position, press button to lock).
*   Turns: coordinated turns using cyclic and pedals (step on the ball), load factor awareness, collective adjustment to maintain altitude in turns (more collective in turns to compensate for increased load), bank angle vs. G-load, recommended max bank for normal operations (30°), max bank structural limit (60°).
*   Climbs and descents: recommended profiles, power management, Nr awareness during descents (Nr may increase — governor compensates, but monitor), avoid low-side RPM excursions during rapid collective changes.
*   Slow flight: characteristics below ETL, transition back to hover regime, increasing power requirements, pedal requirements as speed decreases.
*   Speed changes: acceleration/deceleration, nose attitude and collective relationship, maintaining altitude during transitions.
*   Straight and level flight at various airspeeds: differences in control feel and power required at 40, 60, 80, 100 KIAS, vibration profile at each speed.
*   Autorotation entry (practice): recognition of engine failure cues (Nr decay, audio warning, yaw, EGT drop), immediate actions (**lower collective immediately**, maintain Nr in autorotation range, establish autorotation airspeed ~65 KIAS), power recovery at altitude (not full-down autorotation at this stage). Emphasis on the **criticality of reaction time** with the two-blade rotor — less inertia means Nr decays faster.
*   **Trim technique:** The UH-1H force trim (magnetic brake) system — how to set (press and release button while holding desired control position), release (press and hold), and re-trim. Why constant trimming is necessary as airspeed and power change. Out-of-trim indications and forces.

**Module 7: Navigation**
*   The UH-1H uses **analog radio navigation** — there is no GPS, no FMS, no digital moving map. Navigation is a fundamental pilot skill in this aircraft.
*   **ADF (Automatic Direction Finder) / AN/ARN-83:**
    *   Tuning to NDB frequencies.
    *   Reading the ADF bearing pointer on the compass card.
    *   Homing to an NDB: tracking inbound, wind correction.
    *   Station passage recognition.
*   **VOR/ILS / AN/ARN-82:**
    *   Tuning VOR frequencies.
    *   CDI interpretation: TO/FROM, course selection, tracking inbound and outbound on a radial.
    *   ILS approach: localizer and glideslope needles, basic ILS approach technique.
    *   DME (if modeled): distance readout, groundspeed computation.
*   **Compass navigation:**
    *   Magnetic compass and directional gyro: setting, precession, periodic realignment.
    *   Dead reckoning: time-speed-distance calculations, wind correction angle.
    *   Pilotage: map reading, terrain association, checkpoint identification.
*   **Radar altimeter:** Setting low-altitude warning bug, reading absolute altitude AGL, usage during low-level flight and approaches.
*   **Transponder:** Squawk code entry, modes (standby, normal, altitude reporting), ident function.
*   **Scope limitation:** This module covers basic "point A to point B" navigation and radio aid usage. Mission planning, tactical route planning, and NOE (nap of the earth) flight are out of scope.

**Module 8: Emergency Procedures (Academic)**
*   **Boldface (Memory/Immediate Action) Items:** Per TM 55-1520-210-10 — these must be memorized verbatim:
    *   Engine failure in flight (autorotation entry)
    *   Engine failure at hover / near the ground
    *   Engine fire in flight
    *   Fuel control failure
    *   Emergency engine shutdown
    *   Hydraulic system failure (boost-off landing)
    *   Tail rotor failure / loss of tail rotor thrust
    *   Mast bumping (low-G condition) — **immediate action: apply aft cyclic gently, do NOT push forward**
*   **Autorotation — full procedure:**
    *   Entry: immediate collective down, Nr into autorotation range (294-324 RPM), establish glide (~65 KIAS).
    *   Glide: autorotation airspeed for max range vs. min rate of descent, Nr management (collective adjustments), turn to selected landing area.
    *   Flare: at ~75-100 ft AGL, apply aft cyclic to reduce speed and arrest rate of descent, Nr increases during flare.
    *   Collective pull / cushion: at ~10-15 ft, level the aircraft, apply collective to cushion touchdown using stored rotor energy.
    *   Touchdown: slight nose-up attitude, level skids, slide to a stop.
    *   Straight-in, 90°, and 180° autorotation profiles.
*   Loss of Tail Rotor Effectiveness (LTE): wind conditions that cause it (main rotor vortex interference 285°-315° relative wind, weathercock instability 120°-240°, tail rotor vortex ring state 210°-330°), recognition (uncommanded right yaw, inability to maintain heading), recovery procedure (forward cyclic to gain airspeed, if altitude permits; do not add excessive pedal input).
*   Settling with power (vortex ring state): flight conditions that cause it (low airspeed <30 kts, high rate of descent >300 fpm, high power applied), recognition (high rate of descent despite power application, aircraft shudder), recovery (forward cyclic, reduce collective, gain airspeed to fly out).
*   Governor failure: recognition (Nr fluctuations or divergence), immediate action (GOV switch OFF, manual throttle control), technique for flying with manual throttle — correlator still functions but pilot must actively manage RPM.
*   Hydraulic failure: identification (controls become very heavy, master caution), flight characteristics without hydraulics (flyable but requires significant force), recommended approach (shallow approach, run-on landing to avoid hover work without hydraulics).
*   Electrical failure: generator loss, bus load shedding, battery-only endurance (~30 min), reduced avionics prioritization.
*   Compressor stall: causes (FOD, rapid throttle movement, high-altitude engine operation), recognition (loud bang, EGT spike, power loss), recovery (reduce throttle, clear the stall, slowly re-advance).
*   Fuel system malfunctions: fuel boost pump failure, fuel filter bypass, fuel starvation vs. fuel exhaustion.
*   Transmission failure indications: chip detector light, oil pressure/temperature exceedances, noise/vibration — land as soon as possible vs. land as soon as practicable.
*   Mast bumping: **critical emphasis for the teetering rotor** — conditions to avoid (low G, pushovers, abrupt forward cyclic, turbulence at light gross weight), why recovery is not possible once mast contact occurs (catastrophic structural failure), training emphasis on smooth control inputs and never unloading the rotor disk.
*   Dynamic rollover: conditions that cause it (slope operations, crosswind, skid caught on obstacle, sling load lateral pull), recognition (helicopter rolling despite opposite cyclic), prevention (limit roll rate to 10°/sec during slope operations), recovery (reduce collective if caught early).
*   **DCS-specific emergency notes:** Which failures DCS actually models vs. which are simplified or absent. How to trigger practice emergencies in DCS (mission editor failure triggers). Note any differences in flight model behavior during emergencies compared to real-world expectations.

**Module 9: Approach & Landing**
*   VFR traffic pattern: pattern altitude (typically 800-1,000 ft AGL), downwind leg (parallel to landing direction, ~500-800m lateral distance), base turn, final approach.
*   Normal approach: from pattern altitude, decelerating approach from ~60-80 KIAS, progressive collective reduction, constant angle approach (aim point stays fixed in windscreen), transition to hover at intended landing point, vertical descent to touchdown.
*   Steep approach: when to use (obstacles, confined areas), technique (~10-15° glide path), power management, abort criteria.
*   Shallow approach / running landing: when to use (high gross weight, high density altitude, limited power margin), technique — touchdown with 20-30 knots forward speed and slide to a stop on skids.
*   Hover to landing: transitioning from a stable hover to ground contact, slow collective reduction, feeling for the ground, prevent lateral drift at touchdown.
*   Go-around / wave-off: recognition of unstable approach (too fast, too high, too low, not aligned), power application, climb-out and re-enter pattern.
*   Crosswind approach and landing: wind effect on approach, LTE awareness on final (especially right quartering tailwinds), pedal requirements, drift correction techniques.
*   Slope landing: technique (uphill skid contacts first), limitations (lateral slope ~15°, fore/aft ~10°), dynamic rollover awareness, collective management on slopes.
*   Confined area operations: high/low recon, power check, approach angle selection, escape route identification, ground crew coordination, power management in ground effect.
*   Pinnacle and ridgeline operations: wind effects, approach techniques, power management OGE, escape routes.
*   **DCS-specific:** Ground handling and skid interaction in DCS, autostart behavior (for reference only — the student must learn manual procedures, but should understand what autostart does differently), DCS wind and weather effects on approach.

**Module 10: Shutdown & Post-Flight**
*   Post-landing: hover to parking spot, set down, verify stable on ground (skids firmly planted, no lateral drift).
*   Shutdown procedure:
    *   Throttle to IDLE (twist-grip full open / counterclockwise to idle stop) — engine at ground idle, Nr decreasing.
    *   Wait for stabilization: EGT settling, Nr at idle.
    *   Avionics OFF: radios off, navigation equipment off, transponder off (or standby).
    *   Throttle to OFF (fuel shutoff): engine spools down, EGT drops, Nr decays.
    *   Monitor engine spool-down: N1 decreasing to zero, EGT cooling, rotor slowing and stopping.
    *   Generator OFF, inverter OFF.
    *   Fuel boost pump OFF, fuel valve OFF.
    *   Battery OFF.
*   Post-shutdown checks: rotor stopped, all switches verified OFF, tie-down rotor blades (if applicable), security of cargo/cabin, close doors.
*   Full switch-by-switch shutdown from engine running to cold-and-dark.

**For each module, provide:**
1.  **Learning Objectives:** Measurable outcomes the student must demonstrate.
2.  **Key Data Table:** Rotor RPM limits (power-on, autorotation, transient), torque limits (continuous, transient), EGT limits (continuous, transient, starting), V-speeds (Vy, Vne, autorotation), fuel flow figures, oil pressure/temperature limits — with normal ranges and caution/warning thresholds.
3.  **Cockpit Switch Reference:** Specific switch names, panel locations, and the DCS mouse-click or keybind action to operate them. Include keyboard shortcuts as secondary reference where they exist.
4.  **Instructor Notes:** Common student failure points and how to address them. Focus on the most frequent errors seen in DCS (e.g., over-torquing on takeoff, failing to manage Nr in autorotation practice, LTE encounters during hover pedal turns, aggressive forward cyclic causing mast bumping, hot starts during startup, failing to manage throttle correlation during collective changes, burning out the starter by cranking too long, cross-controlling in turns).
5.  **Realism Divergence Footnotes:** Where DCS simplifies or omits real-world procedures. Format as:
    > *⚠ Realism Divergence: [explanation]*

**Output Format:**
A single, structured Markdown document suitable for saving as `.github/research/uh-1h-bqt-dossier.md`. Use heading levels ##, ###, and #### consistently. Tables for all data. Cockpit switch locations described by panel name (e.g., "Overhead console — Fuel/Engine panel", "Center pedestal — Radio stack", "Instrument panel — Pilot's flight instruments"). All performance data in U.S. customary units (knots, feet, pounds, Fahrenheit) with metric conversions in parentheses where helpful.
