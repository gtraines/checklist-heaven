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
The OH-58D is a **single-engine, light observation helicopter**. Unlike fixed-wing BQT courses (A-10C, A-10A), this course centers on rotary-wing aerodynamics, hover technique, power management, and autorotation. The student must internalize:
*   **Rotor RPM (Nr) management** is life-critical. Unlike a fixed-wing aircraft that can glide indefinitely, a helicopter with decayed Nr will not autorotate. The governor/FADEC manages Nr in normal flight, but the pilot must recognize and respond to Nr excursions.
*   **Collective/cyclic/pedal coordination** replaces the throttle/stick/rudder mental model. All three controls are interdependent — changing collective changes yaw, changing cyclic changes required collective, etc.
*   **Hover is a learned skill** with no fixed-wing equivalent. Significant course time will be devoted to hover work (stationary, taxi, turns, sideward, rearward).
*   **Loss of Tail Rotor Effectiveness (LTE)** and **settling with power (vortex ring state)** are rotary-wing-specific emergencies that the student must understand deeply.
*   **Single-engine helicopter emergency = autorotation.** There is no "single-engine cruise" option. Engine failure requires immediate autorotation entry.

**Key Distinction — DCS Module (Polychop Simulations):**
The DCS OH-58D is a full-fidelity, clickable cockpit module. Every switch, dial, and panel is interactive. This course must teach the student to interact with the physical cockpit — not just memorize keybinds. Procedures should reference cockpit switch positions, panel locations, and collective/cyclic/pedal inputs. Where keyboard shortcuts exist as alternatives, note them, but the primary instruction should be "hands in the cockpit."

**Required Research Modules:**

**Module 1: Aircraft Systems & Aerodynamics**
*   T703-AD-700A turboshaft engine: FADEC operation (auto vs. manual modes), start cycle (N1/Ng ramp, TOT monitoring), spool-up characteristics, power available vs. power required, idle behavior, engine limitations (continuous, transient, starting).
*   Rotor system: main rotor (4-blade, soft-in-plane), tail rotor (2-blade), rotor RPM (Nr) governing, autorotation RPM range, blade stall at high gross weight/altitude/G.
*   Transmission system: main transmission, tail rotor gearbox, power limits (torque continuous vs. transient), oil temperature and pressure limits.
*   Fuel system: internal fuel capacity, fuel boost pump, fuel quantity indication, low-fuel warnings, fuel consumption at various power settings.
*   Hydraulic system: single hydraulic system, what it powers (flight controls), hydraulic-off flight characteristics, irreversible controls.
*   Electrical system: DC generator, battery, essential/non-essential bus, generator failure behavior, battery endurance.
*   FADEC (Full Authority Digital Engine Control): what it manages, auto mode vs. manual mode, failure indicators, FADEC-OFF handling qualities.
*   Flight control system: mechanical mixing (collective-to-yaw, collective-to-cyclic), force trim, SAS (if modeled), hydraulic boost.
*   Survivability features: crashworthy fuel cells, energy-absorbing seats, armored crew seats, IR suppressor (if modeled).
*   Rotary-wing aerodynamics specific to the OH-58D:
    *   Translating tendency (left drift in hover for U.S. helicopters with counterclockwise main rotor).
    *   Translational lift (ETL): speed at which it occurs (~16-24 knots), indications, required control inputs.
    *   Transverse flow effect and its impact in transition.
    *   Retreating blade stall: what causes it, symptoms, recovery.
    *   Dissymmetry of lift and flapping.
    *   Ground effect vs. out-of-ground-effect (IGE vs. OGE) hover performance.
    *   Settling with power (vortex ring state): conditions, recognition, recovery.
    *   Loss of Tail Rotor Effectiveness (LTE): critical wind azimuths, recognition, recovery.
    *   Mast bumping: what causes it (low G, negative G), prevention, why it is immediately catastrophic.
    *   Pendular action and dynamic rollover: causes, recognition, prevention during slope operations and confined area takeoffs.

**Module 2: Cockpit Familiarization**
*   Cockpit layout: left console, right console, instrument panel, center pedestal, overhead console — describe each major panel and its primary function.
*   **MFD (Multi-Function Display):** Power-on, default pages, button nomenclature, basic page navigation.
*   **MMS (Mast-Mounted Sight) controller:** Physical location, basic operation (TV, thermal, laser range finder). Familiarization only — tactical employment is out of scope.
*   **Weapon panel:** Location, ARM/SAFE switch positions, weapon select. Identification only — employment is out of scope.
*   **AHRS/GPS navigation system:** Where it is, how to access waypoints, basic data display for navigation.
*   **Engine instruments:** Torque (Q), TOT, N1 (gas producer), Nr (rotor RPM), fuel flow, oil pressure/temperature — location and normal operating ranges.
*   **Caution/Advisory panel:** Master caution light, individual caution indicators, fire warning.
*   **Radar altimeter:** Setting, reading, low-altitude warning bug.
*   **Flight instruments:** Attitude indicator, airspeed indicator, barometric altimeter, vertical speed indicator, heading indicator, slip ball (turn coordinator).
*   Lighting: cockpit lighting controls (day/night), exterior lights (position, anti-collision, landing/search light), ANVIS NVG compatibility.
*   **Collective and cyclic controls:** HOTAS functions on collective grip (radio triggers, searchlight, landing light, trim release) and cyclic grip (weapon release, MMS slew, force trim).

**Module 3: Ground Operations**
*   Cold-and-dark startup: **full switch-by-switch procedure** from battery ON through engine running and avionics alive.
    *   Battery ON → caution panel check → warning light test.
    *   Fuel boost pump ON → fuel pressure indication.
    *   Engine start sequence: throttle to IDLE detent, starter engaged, N1/Ng monitoring, TOT monitoring, abort criteria (hot start, hung start, no light-off).
    *   Post-start stabilization: engine at ground idle, Nr governing, TOT settling within limits.
    *   Generator ON → electrical bus powered, inverter check.
    *   Avionics power-on: MFD, AHRS/GPS, radios, transponder.
    *   Hydraulic system check: pressure indication, flight control check (full cyclic/collective/pedal deflection).
*   **AHRS/GPS alignment:**
    *   Alignment procedure: how long, what indications, when alignment quality is sufficient.
    *   DCS-specific alignment time vs. real-world.
*   Flight control rigging / before-takeoff check: force trim check, SAS engagement (if modeled), caution panel clear.
*   Rotor engagement: throttle to FLY (flight idle), Nr stabilization at 100%, rotor smoothing.
*   Ground taxi (hover taxi): techniques for hovering forward at low altitude (<3 ft skid height), NVG taxi considerations.
*   Pre-takeoff checks: engine instruments in limits, torque available check (power check), caution panel clear, flight controls free, radios set, altimeter set.

**Module 4: Hover & Takeoff**
*   Hover technique:
    *   Stationary hover: picking up to a hover, maintaining position/heading/altitude using outside references, scan pattern.
    *   Hover power check: verifying power required vs. power available at current weight/altitude/temperature.
    *   Hover turns (pedal turns): 360° turns maintaining position and altitude.
    *   Hover taxi: forward, sideward, and rearward flight at hover taxi speeds (<20 knots).
*   Takeoff profiles:
    *   Normal takeoff: from hover, accelerate through ETL (nose will pitch up, aircraft will yaw left — corrections required), positive rate, continue climb.
    *   No-hover takeoff (when performance limited): technique for departing without establishing a full hover.
    *   Maximum performance takeoff: when and why to use it, technique.
*   Climb profile: Vy (best rate of climb speed, ~55-60 KIAS), cruise climb, level-off technique.
*   Departure: standard VFR departure, communication procedures.
*   **Ground resonance:** What it is, conditions that cause it (hard surface, one skid, unbalanced condition), recognition (violent oscillation), immediate action (full up collective if RPM is sufficient, or immediate shutdown if on the ground and RPM is low). Why this is an emergency unique to helicopters.

**Module 5: Basic Flight Maneuvers**
*   Level flight: cruise speed (~80-100 KIAS), power settings for various altitudes, trim technique.
*   Turns: coordinated turns using cyclic and pedals, load factor awareness, collective adjustment to maintain altitude in turns, bank angle vs. G.
*   Climbs and descents: recommended profiles, power management, Nr awareness during descents.
*   Slow flight: characteristics below ETL, transition back to hover regime, power requirements.
*   Autorotation entry (practice): recognition of engine failure cues, immediate actions (lower collective, maintain Nr, establish autorotation airspeed 60-80 KIAS), power recovery at altitude (not full-down autorotation at this stage).
*   **Trim technique:** The OH-58D force trim system — how to set, release, and re-trim. Why constant trimming is necessary as airspeed and power change.
*   Speed changes: acceleration/deceleration, nose attitude and collective relationship, maintaining altitude during transitions.
*   Straight and level flight at various airspeeds: differences in control feel and power required at 40, 60, 80, 100 KIAS.

**Module 6: Navigation (Basic AHRS/GPS)**
*   Waypoint navigation: selecting waypoints, MFD navigation page, bearing/distance/ETA readout.
*   Creating/modifying waypoints in the MFD/navigation system.
*   Map orientation: MFD moving map (if available), north-up vs. track-up.
*   HSI / heading indicator: setting heading bug, course to waypoint.
*   Radar altimeter usage: setting decision height/low-altitude warning, terrain awareness during low-level flight.
*   Radio navigation aids: TACAN usage (if modeled), ADF (if modeled).
*   **Scope limitation:** This module covers basic "point A to point B" navigation. Mission planning, tactical route planning, and threat avoidance are out of scope.

**Module 7: Emergency Procedures (Academic)**
*   **Boldface (Memory/Immediate Action) Items:** Per TM 1-1520-248-10 — these must be memorized verbatim:
    *   Engine failure in flight (autorotation entry)
    *   Engine failure at hover / low altitude
    *   Engine fire in flight
    *   Emergency shutdown
    *   FADEC failure
    *   Hydraulic system failure
    *   Tail rotor failure / loss of tail rotor thrust
*   Loss of Tail Rotor Effectiveness (LTE): wind conditions that cause it, recognition (uncommanded right yaw), recovery procedure.
*   Settling with power (vortex ring state): flight conditions that cause it (low airspeed, high rate of descent, high power), recognition (high rate of descent despite power application), recovery (cyclic forward, reduce collective, gain airspeed).
*   Autorotation: full procedure from engine failure through touchdown — entry, glide (60-80 KIAS), flare, collective pull, touchdown technique. Straight-in vs. 180° autorotation.
*   FADEC failure: auto-to-manual transfer, manual throttle control, handling qualities in manual mode.
*   Hydraulic failure: identification, flight characteristics without hydraulics, recommended approach (run-on landing).
*   Electrical failure: generator loss, bus shedding, battery-only endurance, reduced avionics.
*   Main transmission failure indications: chip lights, oil pressure/temperature exceedances, noise/vibration — land as soon as possible.
*   Mast bumping: awareness item — conditions to avoid (low G, pushovers, turbulence), why recovery is not possible once mast contact occurs.
*   Dynamic rollover: conditions that cause it (slope, crosswind, skid caught), recognition, prevention, recovery (if still in early phase — reduce collective).
*   **DCS-specific emergency notes:** Which failures DCS actually models vs. which are simplified or absent.

**Module 8: Approach & Landing**
*   VFR traffic pattern: pattern altitude, downwind leg, base turn, final approach.
*   Normal approach: from pattern altitude, decelerating approach from ~60-80 KIAS, progressive collective reduction, transition to hover at intended landing point.
*   Steep approach: when to use (obstacles, confined areas), technique, power management.
*   Shallow approach / running landing: when to use (high gross weight, high altitude, limited power margin), technique — touchdown with forward speed and slide to a stop.
*   Hover to landing: transitioning from a stable hover to ground contact, collective management during settling.
*   Go-around / wave-off: recognition of unstable approach, power application, climb-out and re-enter pattern.
*   Crosswind considerations: wind effect on approach, LTE awareness on final, pedal requirements.
*   Slope landing: technique, limitations (10° side slope, 5° nose-down), dynamic rollover awareness.
*   Confined area operations: power check, approach angle, escape route, ground crew coordination.
*   **DCS-specific:** Autostart behavior (for reference only — the student must learn manual start, but should understand what autostart does differently). Ground handling and skid interaction in DCS.

**Module 9: Shutdown**
*   Post-landing: hover to parking spot, set down, verify stable on ground.
*   Shutdown procedure: throttle to IDLE → wait for stabilization → throttle to OFF, engine spool-down monitoring (TOT, N1).
*   Post-shutdown: avionics off sequence, generator off, fuel boost off, battery off, rotor brake (if applicable).
*   Full switch-by-switch shutdown from engine running to cold-and-dark.

**For each module, provide:**
1.  **Learning Objectives:** Measurable outcomes the student must demonstrate.
2.  **Key Data Table:** Rotor RPM limits, torque limits, TOT limits, V-speeds, fuel flow figures, oil pressure/temperature limits — with normal ranges and caution/warning thresholds.
3.  **Cockpit Switch Reference:** Specific switch names, panel locations, and the DCS mouse-click or collective/cyclic HOTAS action to operate them. Include keyboard shortcuts as secondary reference where they exist.
4.  **Instructor Notes:** Common student failure points and how to address them. Focus on the most frequent errors seen in DCS (e.g., over-torquing on takeoff, failing to manage Nr in autorotation practice, LTE encounters during hover pedal turns, ham-fisting the collective during hover work, ground resonance panic).
5.  **Realism Divergence Footnotes:** Where DCS simplifies or omits real-world procedures. Format as:
    > *⚠ Realism Divergence: [explanation]*

**Output Format:**
A single, structured Markdown document suitable for saving as `.github/research/oh-58d-bqt-dossier.md`. Use heading levels ##, ###, and #### consistently. Tables for all data. Cockpit switch locations described by panel name (e.g., "Left console — Fuel Panel", "Overhead console — Engine Start panel", "Instrument panel — Engine gauges").
