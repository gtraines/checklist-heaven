Act as an expert military aviation instructor, Russian/Soviet Mi-24 "Hind" instructor pilot, and DCS World subject-matter expert. I need you to compile a detailed research dossier for a **Mi-24P Basic Qualification Training (BQT) Course**.

**Objective:**
Create a structured syllabus and technical research document covering all aspects of safe Mi-24P operation from cold-and-dark startup through safe recovery. This is a **full-fidelity, dual-seat clickable cockpit module** (Eagle Dynamics) — all procedures involve physical cockpit switches, panels, collective/cyclic controls, and HOTAS commands across **two crew stations** (Pilot in the rear cockpit, Weapons Systems Officer in the front cockpit). Weapons employment (ATGM engagement, rocket attacks, cannon strafing, air-to-air missiles) is **out of scope** for this course. However, the student must be introduced to the weapons panel, PKV sight system, and SPO-15 RWR at a basic familiarization level, and to the navigation system (DISS-15, ARK-15, RSBN) at a basic navigation level.

**Source Material Priority:**
1.  **Real-World (Primary Truth):** Use real Soviet/Russian military documentation wherever possible:
    *   *Technical Description and Operating Instructions for the Mi-24P (Tekhnicheskoye Opisaniye i Instruktsiya po Ekspluatatsii Mi-24P)* — the authoritative primary source for systems, limitations, and procedures. Available in translated form.
    *   *Mi-24 Flight Manual (Rukovodstvo po Letnoy Ekspluatatsii - RLE)* — the Russian equivalent of a NATOPS/Dash-1 flight manual covering normal procedures, limitations, and emergency procedures.
    *   *Soviet/Russian helicopter aerodynamics training manuals* — rotary-wing theory as applied to the Mi-24 family, including the effects of stub wings on rotor offloading.
    *   Any publicly available translated Soviet Air Force or Army Aviation (AA VVS) training circulars, accident investigation summaries, or technical bulletins for the Mi-24 family.
    *   Western intelligence assessments and translated technical evaluations of the Mi-24 (e.g., NATO reporting, DIA technical assessments) where original Soviet documentation is unavailable.
2.  **DCS Simulation (Secondary / Override):** Where the DCS Mi-24P module (Eagle Dynamics) diverges from real-world procedures (e.g., simplified APU behavior, compressed alignment times, altered flight model specifics, absent circuit breakers, simplified hydraulic modeling, single-player crew-switching mechanics), **the DCS procedure is what the student will actually execute**. Document the DCS procedure as the primary instruction.
3.  **Divergence Footnotes:** Any time the real-world procedure differs from DCS, include a clearly marked footnote formatted as:
    > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

**Key Distinction — Heavy Attack Helicopter:**
The Mi-24P is a **twin-engine, heavy attack helicopter** with stub wings. Unlike light observation helicopters (OH-58D, UH-1H), the Hind is designed for speed, not hover precision. The student must internalize:
*   **The Mi-24P is NOT a good hover platform.** At ~11,000 kg MTOW, it demands enormous power to hover, especially OGE or in hot/high conditions. Hover time should be minimized. The aircraft wants to fly fast.
*   **Stub wings offload the rotor in forward flight.** At cruise speeds (220-260 km/h), the wings generate meaningful lift (~25% of total at high speed), improving performance and range. However, the wings also create additional drag at low speeds and can produce adverse effects during autorotation (increased descent rate compared to a wingless helicopter of similar weight).
*   **Twin engines provide survivability.** Unlike a single-engine helicopter, the Mi-24P can sustain flight on one engine (with limitations). Single-engine procedures are critical knowledge, not just "autorotate immediately."
*   **Fixed cannon means the pilot is the gunner.** The GSh-30K is fixed to the starboard fuselage — the pilot aims the aircraft. This affects maneuvering doctrine even at the BQT level (the student must understand why the aircraft flies the way it does).
*   **Two-crew coordination is fundamental.** Even in basic qualification, the student must understand the pilot/WSO division of labor. In DCS single-player, the student will switch between seats using `1` (front/WSO) and `2` (rear/Pilot) — this mechanic must be taught.
*   **Retractable tricycle landing gear** replaces skids — ground handling, taxiing, and nosewheel steering are fundamentally different from skid-equipped helicopters. The Mi-24P taxis on its wheels like a fixed-wing aircraft.
*   **Soviet metric system** is primary: speeds in km/h, altitudes in meters, temperatures in °C, weights in kg. Provide conversions in parentheses where helpful, but train in metric.

**Key Distinction — DCS Module (Eagle Dynamics):**
The DCS Mi-24P is a **native Eagle Dynamics full-fidelity module** with two fully interactive cockpits. Every switch, dial, gauge, and panel in both the pilot (rear) and WSO (front) cockpit is clickable. This course must teach the student to interact with the physical cockpit — not just memorize keybinds. Procedures should reference cockpit switch positions, panel locations, and collective/cyclic/pedal inputs with the specific cockpit (Pilot or WSO) clearly identified. Where keyboard shortcuts exist as alternatives, note them, but the primary instruction should be "hands in the cockpit."

**Required Research Modules:**

**Module 1: Aircraft Systems & Aerodynamics**
*   TV3-117V turboshaft engines (×2): start cycle (APU-assisted and cross-bleed), spool-up characteristics, turbine temperature monitoring (TIT), gas generator RPM (Ng), power turbine RPM (Nf), engine limitations (continuous, transient, starting TIT limits), idle behavior, emergency shutdown.
*   Rotor system: main rotor (5-blade, fully articulated), tail rotor (3-blade, right side, pusher configuration), rotor RPM (Nr) governing, autorotation RPM range, lead-lag dampers, blade fold (ground operations).
*   Transmission system: main gearbox (VR-24), intermediate gearbox, tail rotor gearbox, combining gearbox — power limits (torque continuous vs. transient), oil temperature and pressure limits, chip detectors.
*   Stub wings: aerodynamic function (lift generation in forward flight, weapon pylons), effect on rotor offloading at speed, effect on autorotation (increased descent rate), wing area and incidence angle, why the Mi-24P "wants to fly fast."
*   Fuel system: internal fuel tanks (location, capacity ~1,500 kg), fuel sequence, fuel boost pumps, fuel quantity indication, cross-feed system, low-fuel warnings, fuel consumption at various power settings, external ferry tanks (if modeled).
*   Hydraulic system: main and backup hydraulic systems, what each powers (flight controls, landing gear, brakes), hydraulic-off flight characteristics, emergency hydraulic pump.
*   Electrical system: two DC generators (one per engine), batteries, AC inverters, essential/non-essential bus, APU generator, generator failure behavior, battery endurance, bus tie.
*   APU (AI-9V auxiliary power unit): function (electrical power and bleed air for engine start), start procedure, limitations, auto-shutdown conditions.
*   Flight control system: hydraulic boost (irreversible controls), force trim, autopilot integration, mechanical mixing (collective-to-yaw, collective-to-cyclic), control travel limits.
*   Autopilot system: channels available (roll, pitch, heading, altitude, flight director), engagement/disengagement, autopilot-off handling, trim interaction, barometric altitude hold vs. radar altitude hold.
*   Survivability features: armored crew compartments, armored windscreens, self-sealing fuel cells, IR suppressor exhaust mixer, redundant systems, crash-resistant landing gear.
*   Rotary-wing aerodynamics specific to the Mi-24P:
    *   Translating tendency (drift in hover due to tail rotor thrust).
    *   Translational lift (ETL): speed at which it occurs (~50 km/h for the Hind), indications, required control inputs — note the Hind's ETL is experienced differently due to the wings and high weight.
    *   Transverse flow effect and its impact in transition.
    *   Retreating blade stall: what causes it, why the Mi-24P's VNE (300 km/h) exists, symptoms, recovery.
    *   Dissymmetry of lift and flapping.
    *   Ground effect vs. out-of-ground-effect (IGE vs. OGE) hover performance — critical for the Mi-24P because OGE hover may not be possible at high gross weight.
    *   Settling with power (vortex ring state): conditions, recognition, recovery — the Mi-24P's high disc loading makes this a particular concern.
    *   Loss of Tail Rotor Effectiveness (LTE): critical wind azimuths (note: right-side pusher tail rotor affects the specific azimuths), recognition, recovery.
    *   Mast bumping: relevance to the Mi-24P's fully articulated rotor system (less susceptible than semi-rigid, but still a factor at low/negative G).
    *   Dynamic rollover: causes, recognition, prevention during ground operations — applicable to the wheeled landing gear configuration.
    *   Ground resonance: what it is, conditions that cause it (wheeled landing gear on hard surface, unbalanced condition, improper tire pressure), recognition (violent oscillation), immediate action — this is a **critical emergency** for the wheeled Mi-24P.

**Module 2: Cockpit Familiarization**
*   **Rear Cockpit (Pilot):** This is the primary flying cockpit and the default spawn position.
    *   Instrument panel: flight instruments (ADI, HSI, altimeter — barometric in meters, airspeed in km/h, vertical speed indicator, slip ball), engine instruments (TIT, Ng, Nf/Nr, torque, fuel flow, oil pressure/temperature).
    *   Left console: electrical panel, fuel panel, engine start panel, lighting controls.
    *   Right console: radio panels (R-863, R-828), IFF, navigation equipment.
    *   Center pedestal: throttle quadrant (two throttles), collective friction, trim controls.
    *   Overhead panel: circuit breakers, anti-ice, pitot heat, rotating beacon.
    *   Caution/advisory panel: master caution, individual warning lights (fire, hydraulic, generator, fuel, rotor brake, autopilot disconnect), fire suppression panel.
    *   Collective controls: collective lever with throttle twist grips (×2), landing light switch, radio trigger, collective-mounted switches.
    *   Cyclic controls: cyclic grip with weapon release, trim release, radio trigger, cyclic-mounted switches.
    *   Pedals: anti-torque pedals with toe brakes (nosewheel steering linked to pedals).
*   **Front Cockpit (WSO):** The weapons operator station.
    *   PKV-1 sight: location, basic function (weapons aiming for pilot-fired weapons), power-on — familiarization only.
    *   Weapons panel: weapon select switches, master arm, salvo/single selection — identification only, employment out of scope.
    *   ATGM guidance panel: Shturm/Ataka guidance system controls — identification only.
    *   SPO-15 "Beryoza" RWR: display location, basic threat indication, audio warnings — familiarization level.
    *   UV-26 countermeasures panel: chaff/flare dispensers, program selection — familiarization level.
    *   Duplicate flight instruments: basic flight instruments available to WSO, their differences from pilot's instruments.
*   **Seat switching in DCS:** How to switch between Pilot (`2` key) and WSO (`1` key) in single-player, what resets or changes when switching, limitations.
*   Lighting: cockpit lighting controls (day/night) for both cockpits, exterior lights (position, anti-collision, landing/search light, formation lights), NVG compatibility.

**Module 3: Ground Operations**
*   Cold-and-dark startup: **full switch-by-switch procedure** from battery ON through both engines running and avionics alive. Document for **both cockpits** where actions are split between Pilot and WSO stations.
    *   Battery ON → master caution check → warning light test.
    *   APU start sequence: APU switch, APU RPM indication, APU generator engagement. DCS-specific APU behavior.
    *   Left engine start: throttle to IDLE detent, engine start button, Ng monitoring, TIT monitoring, abort criteria (hot start, hung start, no light-off, TIT exceedance).
    *   Right engine start: same procedure, opposite engine. Cross-bleed start (if APU unavailable).
    *   Post-start stabilization: both engines at ground idle, Nr governing (governor ON), TIT settling within limits.
    *   Generator switches: verify both engine generators online, APU generator OFF, APU shutdown.
    *   Hydraulic system check: pressure indications for main and backup systems, flight control check (full cyclic/collective/pedal deflection).
    *   Avionics power-on: navigation system, radios (R-863 UHF, R-828 VHF/FM), IFF, SPO-15 RWR, PKV sight system standby.
*   **Navigation system alignment/warm-up:**
    *   DISS-15 Doppler navigation system: power-on, warm-up time, functionality.
    *   ARK-15 ADF: power-on, tuning.
    *   RSBN: power-on, beacon selection.
    *   DCS-specific alignment times vs. real-world.
*   Autopilot pre-flight check: channel engagement, trim synchronization.
*   **Landing gear and ground handling:**
    *   Nosewheel steering: engagement, authority (linked to pedals), high-speed vs. low-speed steering.
    *   Wheel brakes: toe brakes on pedals, parking brake engagement/release.
    *   Taxi procedures: taxi speeds, power required for taxi, turns, brake check.
    *   Rotor engagement: throttles to flight position, Nr stabilization at 95%, rotor smoothing.
*   Pre-takeoff checks: both engines instruments in limits, torque available check (power check), caution panel clear, flight controls free and correct, radios set, altimeter set (QFE/QNH — Soviet convention), autopilot channels set.

**Module 4: Hover & Takeoff**
*   Hover technique (note: the Mi-24P hovers poorly compared to lighter helicopters):
    *   Picking up to a hover: collective application, pedal coordination, cyclic corrections — the Mi-24P requires significant power and aggressive pedal input.
    *   Hover power check: verifying power required vs. power available at current weight/altitude/temperature. **OGE hover may not be possible at high gross weight.**
    *   Hover turns (pedal turns): technique, power management — the Mi-24P's high inertia makes precise hover work demanding.
    *   Hover taxi: forward taxi at hover altitude, nosewheel steering not available (gear may be up), speed control.
*   Takeoff profiles:
    *   Normal takeoff: from a brief hover or running takeoff, accelerate through ETL (~50 km/h), climb at 120-140 km/h. The Mi-24P accelerates quickly through ETL due to high power.
    *   Running takeoff (preferred for the Mi-24P): from the ground roll, apply power progressively, nose down attitude, accelerate to translational lift, rotation and climb — this is the **standard Mi-24P departure** because it minimizes time in the vulnerable hover regime.
    *   Maximum performance takeoff: when and why (obstacle clearance), technique, power management, the role of the wings in climb.
*   Climb profile: best rate of climb speed (~120-140 km/h), cruise climb (~200 km/h), level-off technique, power management.
*   Departure: standard VFR departure from a tactical airfield.
*   **Ground resonance:** What it is, conditions that cause it (wheeled landing gear, one gear extended, improper tire inflation, rotor imbalance), recognition (violent oscillation building rapidly), immediate action:
    *   If Nr is sufficient: **full collective to get airborne immediately** — break ground contact.
    *   If Nr is insufficient or on the ground with low RPM: **immediate shutdown** — throttles to OFF, rotor brake.
    *   Why this is a **catastrophic emergency** unique to helicopters with wheeled undercarriage and articulated rotors — the Mi-24P is particularly susceptible.

**Module 5: Basic Flight Maneuvers**
*   Level flight: cruise speed (220-260 km/h), power settings for various altitudes, trim technique, the Mi-24P's stability characteristics at speed (note: wings improve longitudinal stability).
*   Turns: coordinated turns using cyclic and pedals, load factor awareness (limit +3.5 G), collective adjustment to maintain altitude in turns, bank angle vs. G, the effect of speed on turn performance.
*   Climbs and descents: recommended profiles, power management, Nr awareness during descents, the role of autorotation in descent planning.
*   Slow flight: characteristics below ETL, transition back to hover regime, power requirements — the Mi-24P's high disc loading means power required increases rapidly as speed decreases.
*   Autorotation entry (practice): recognition of dual engine failure cues, immediate actions (lower collective, maintain Nr 92-98%, establish autorotation airspeed ~170 km/h), the effect of stub wings on autorotation descent rate (higher than a wingless helicopter), power recovery at altitude (not full-down autorotation at this stage).
*   **Trim technique:** The Mi-24P force trim system — how to set, release, and re-trim. Why constant trimming is necessary. Autopilot interaction with trim.
*   Speed changes: acceleration/deceleration, nose attitude and collective relationship, the effect of the wings generating more lift as speed increases.
*   **Autopilot usage in flight:** Engaging/disengaging channels, limitations, what the autopilot holds (attitude, altitude, heading), when to use it, how to override it, trim state after disconnect.
*   Straight and level flight at various airspeeds: differences in control feel and power required at 100, 150, 200, 260 km/h — note the "sweet spot" where the wings begin contributing meaningful lift.

**Module 6: Navigation (Basic DISS-15 / ARK-15 / RSBN)**
*   **DISS-15 Doppler Navigation System:** Function (ground speed and drift measurement), display, integration with flight planning, limitations over water.
*   **ARK-15 ADF (Automatic Direction Finder):** Tuning to NDB stations, needle presentation on HSI, bearing-to-station, homing procedure, ARK-15 vs. ARK-UD (if modeled).
*   **RSBN (Short-Range Radio Navigation):** Soviet equivalent to TACAN — tuning to ground beacons, range and bearing display, approach aid usage.
*   Waypoint navigation: selecting/entering waypoints (if supported in DCS navigation system), bearing/distance readout.
*   HSI (Horizontal Situation Indicator): heading, course, bearing-to-beacon, CDI needle interpretation.
*   Radar altimeter: setting decision height/low-altitude warning, terrain awareness, Soviet A-037 radar altimeter usage.
*   Radio communication: R-863 UHF radio (pilot/WSO), R-828 VHF/FM radio, frequency setting, preset channels, intercom system between cockpits.
*   **Scope limitation:** This module covers basic "point A to point B" navigation. Mission planning, tactical route planning, and threat avoidance are out of scope.

**Module 7: Emergency Procedures (Academic)**
*   **Boldface (Memory/Immediate Action) Items:** Per the Mi-24P RLE — these must be memorized verbatim:
    *   Single engine failure in flight (identify, secure, single-engine flight)
    *   Dual engine failure in flight (autorotation entry)
    *   Engine failure at hover / low altitude
    *   Engine fire in flight (left engine, right engine — separate procedures due to asymmetric fire suppression)
    *   Emergency shutdown
    *   Hydraulic system failure (main system, backup system, both)
    *   Tail rotor failure / loss of tail rotor drive
    *   Tail rotor pitch control failure (runaway)
    *   Main gearbox failure indications
*   **Single engine operations:** Identification of failed engine, securing procedure, single-engine flight characteristics (yaw, power limitations), recommended speeds for single-engine flight, single-engine approach and landing.
*   Loss of Tail Rotor Effectiveness (LTE): wind conditions, recognition (uncommanded yaw — direction depends on Mi-24P's right-side pusher tail rotor), recovery procedure.
*   Settling with power (vortex ring state): flight conditions that cause it, recognition, recovery (cyclic forward, reduce collective, gain airspeed) — the Mi-24P's high disc loading increases susceptibility.
*   Autorotation: full procedure from dual engine failure through touchdown — entry, glide (~170 km/h), flare, collective pull, touchdown technique. Effect of stub wings (higher descent rate but also more energy to manage in flare). Landing gear considerations (gear down for autorotation landing).
*   Hydraulic failure: main system vs. backup system, flight characteristics without hydraulics, emergency hydraulic pump, recommended approach.
*   Electrical failure: generator loss (single, dual), bus shedding, battery-only endurance, reduced avionics, APU restart in flight (if modeled).
*   Fire: engine fire (each engine separately), fire detection system, fire extinguisher bottles (two, selectable), APU fire, electrical fire, cargo compartment fire.
*   Main gearbox failure indications: chip lights, oil pressure/temperature exceedances, noise/vibration — land as soon as possible vs. land immediately.
*   Ground resonance: conditions, recognition, immediate action (fly or shut down — decision tree based on Nr).
*   Mast bumping awareness: conditions to avoid (low G, pushovers, turbulence), why recovery is difficult once mast contact occurs.
*   Dynamic rollover: conditions during ground operations, recognition, prevention.
*   **DCS-specific emergency notes:** Which failures DCS actually models, which are simplified, which are absent. How to trigger practice emergencies in DCS mission editor.

**Module 8: Approach & Landing**
*   VFR traffic pattern: pattern altitude and geometry (note: Soviet traffic pattern conventions may differ from Western), downwind leg, base turn, final approach.
*   Normal approach: from pattern altitude, decelerating approach, progressive collective reduction, transition to hover or running landing.
*   **Running landing (preferred for Mi-24P):** Technique — maintain forward speed, touchdown on main gear first, lower nose, nosewheel steering and brakes. This is the **standard Mi-24P landing** because it requires less power than a hover landing.
*   Hover landing: when to use (confined areas, precision placement), power requirements, transition from forward flight to hover to touchdown.
*   Steep approach: when to use (obstacles, confined areas), technique, power management — note the Mi-24P's high power requirement at low speed.
*   Go-around / wave-off: recognition of unstable approach, power application, climb-out and re-enter pattern.
*   Crosswind considerations: wind effect on approach, LTE awareness on final, pedal requirements, crosswind limits (12 m/s).
*   Landing gear management: normal extension/retraction, emergency extension (if gear system fails), gear indicator lights, gear-unsafe indications.
*   Wheel brakes and rollout: braking technique after running landing, anti-skid (if modeled), parking brake engagement.
*   **DCS-specific:** Autostart behavior (for reference only — the student must learn manual start, but should understand what autostart does differently). Ground handling and gear interaction in DCS.

**Module 9: Shutdown**
*   Post-landing: taxi to parking spot, parking brake set, verify stable on ground.
*   Shutdown procedure: throttles to IDLE → stabilization period → throttles to OFF, engine spool-down monitoring (TIT, Ng).
*   Rotor brake engagement: when the rotor RPM reaches the appropriate range, engage rotor brake.
*   Post-shutdown: avionics off sequence (both cockpits), generators off, APU off (if running), fuel boost pumps off, battery off.
*   Full switch-by-switch shutdown from engines running to cold-and-dark — document for **both cockpits** where actions are split.

**For each module, provide:**
1.  **Learning Objectives:** Measurable outcomes the student must demonstrate.
2.  **Key Data Table:** Rotor RPM limits, engine parameters (TIT, Ng, Nf), torque limits, V-speeds (in km/h with knot conversions), fuel flow figures, oil pressure/temperature limits, hydraulic pressures — with normal ranges and caution/warning thresholds.
3.  **Cockpit Switch Reference:** Specific switch names, panel locations, **which cockpit (Pilot/WSO)**, and the DCS mouse-click or collective/cyclic HOTAS action to operate them. Include keyboard shortcuts as secondary reference where they exist.
4.  **Instructor Notes:** Common student failure points and how to address them. Focus on the most frequent errors seen in DCS (e.g., over-torquing on takeoff, failing to manage Nr in autorotation practice, LTE encounters during hover pedal turns, ground resonance from improper ground handling, forgetting to switch between crew positions, running out of power trying to hover at high gross weight, failing to use running takeoffs/landings).
5.  **Realism Divergence Footnotes:** Where DCS simplifies or omits real-world procedures. Format as:
    > *⚠ Realism Divergence: [explanation]*

**Output Format:**
A single, structured Markdown document suitable for saving as `.github/research/mi-24p-bqt-dossier.md`. Use heading levels ##, ###, and #### consistently. Tables for all data. Cockpit switch locations described by cockpit and panel name (e.g., "Pilot — Left console — Electrical Panel", "WSO — Instrument panel — Weapons selector", "Pilot — Overhead panel — Anti-ice"). Soviet/metric units are primary with Western conversions in parentheses where helpful.
