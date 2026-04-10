Act as an expert military aviation instructor, USAF A-10C "Thunderbolt II" Weapons System Officer / instructor pilot, and DCS World subject-matter expert. I need you to compile a detailed research dossier for an **A-10C Basic Qualification Training (BQT) Course**.

**Objective:**
Create a structured syllabus and technical research document covering all aspects of safe A-10C operation from cold-and-dark startup through safe recovery. This is a **full-fidelity clickable cockpit module** — all procedures involve physical cockpit switches, panels, and HOTAS commands. Combat employment (weapons delivery, TGP targeting, JTAC coordination) is **out of scope** for this course. However, the student must be introduced to the core avionics (MFCDs, CDU, EGI) at a basic navigation level.

**Source Material Priority:**
1.  **Real-World (Primary Truth):** Use real USAF documentation wherever possible:
    *   *T.O. 1A-10C-1 Flight Manual* — the authoritative primary source for systems, limitations, and procedures.
    *   *AFMAN 11-2A-10C Vol 3* — operating procedures, pattern standards, crosswind limits, boldface emergency procedures.
    *   *T.O. 1A-10C-34-1-1 Non-Nuclear Weapons Delivery Manual* — systems context only (weapons employment is out of scope).
    *   USAF Contact Flying and Instrument Flying manuals for pattern geometry and approach standards.
    *   Any publicly available ACC/AFMC A-10C guidance or supplements.
2.  **DCS Simulation (Secondary / Override):** Where the DCS A-10C module diverges from real-world procedures (e.g., simplified APU behavior, EGI alignment time compression, absent INS drift, missing circuit breaker modeling), **the DCS procedure is what the student will actually execute**. Document the DCS procedure as the primary instruction.
3.  **Divergence Footnotes:** Any time the real-world procedure differs from DCS, include a clearly marked footnote formatted as:
    > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

**Key Distinction from the A-10A (FC3) BQT:**
The A-10C is a **full-fidelity, clickable cockpit module**. Unlike the A-10A (Flaming Cliffs 3), every switch, dial, and panel is interactive. This course must teach the student to interact with the physical cockpit — not just memorize keybinds. Procedures should reference cockpit switch positions, panel locations, and HOTAS commands. Where keyboard shortcuts exist as alternatives, note them, but the primary instruction should be "hands in the cockpit."

**Required Research Modules:**

**Module 1: Aircraft Systems & Aerodynamics**
*   TF34-GE-100A turbofan engines: start cycle, spool-up lag, ITT/N1/N2 limits, idle vs. flight idle behavior.
*   Fuel system: internal tanks, feed sequence, crossfeed, low-fuel warnings, fuel totalizer and flow indicators.
*   Hydraulic system: A and B systems, what each powers, manual reversion capability and flying qualities.
*   Electrical system: battery, generators, APU, essential/non-essential bus, emergency bus behavior.
*   Flight control system: SAS (Stability Augmentation System), EAC (Enhanced Attitude Control), trim authority, manual reversion. Explain SAS vs. EAC differences and when each is operative.
*   Environmental Control System (ECS): anti-ice, pressurization (simplified in DCS), windshield defog.
*   Survivability features: titanium bathtub, self-sealing fuel cells, redundant flight controls, dual engines.
*   Stall characteristics: AoA indexer (green donut, chevrons, red stall marker), departure behavior, buffet onset, spin susceptibility.

**Module 2: Cockpit Familiarization**
*   Cockpit layout: left console, right console, instrument panel, glareshield, center pedestal — describe each major panel.
*   **AHCP (Armament HUD Control Panel):** Master Arm, Gun/PAC Arm, Laser Arm, TGP switch positions. (Identify only — employment out of scope.)
*   **LASTE (Low Altitude Safety and Targeting Enhancement):** What it does, SAS and EAC sub-modes.
*   **UFC (Upfront Controller):** Radio tuning, IFF, master caution acknowledge, steerpoint selection basics.
*   **Left and Right MFCDs:** Power-on sequence, default pages, button nomenclature (OSB 1–20), basic page navigation.
*   **CDU (Control Display Unit):** Where it is, how to access steerpoint pages, basic data entry for navigation.
*   **CMSC (Countermeasures Signal Converter) / CMSP (Countermeasures Signal Processor):** RWR threat display, chaff/flare program selection, MWS (Missile Warning System).
*   **Engine instruments:** ITT, N1, N2, fuel flow, oil pressure gauges — location and normal operating ranges.
*   **Warning/Caution/Advisory panel:** Master caution light, fire warning T-handles, gear warning horn.
*   Lighting: cockpit lighting controls (day/night), exterior lights (position, anti-collision, landing/taxi lights).

**Module 3: Ground Operations**
*   Cold-and-dark startup: **full switch-by-switch procedure** from battery ON through engines running and avionics alive.
    *   Battery switch ON → inverter → warning light test.
    *   APU start sequence: APU switch → RPM indication → generator tie.
    *   Left engine start: throttle detent, engine operate switch (NORM/IGN), ITT/N1/N2 monitoring, abort criteria (hot start, hung start).
    *   Right engine start: same procedure, opposite side.
    *   Generator switches: verify both generators online, APU generator off.
    *   Post-start: hydraulic pressure check (A and B), flight control check (full deflection), warning panel clear.
*   Avionics power-on sequence: MFCDs, CDU, UFC, HMCS, TGP standby (power on but do not configure), IFFCC.
*   **EGI (Embedded GPS/INS) Alignment:**
    *   Full alignment procedure: how long, what indications, when alignment quality is sufficient.
    *   Stored heading alignment (faster) vs. full GC alignment.
    *   DCS-specific alignment time vs. real-world alignment time.
*   INS/GPS status: how to confirm nav solution quality on CDU/MFCD.
*   Taxi procedures: nose wheel steering (NWS) — engage/disengage (paddle switch on stick), HI and LO NWS, differential braking, taxi speed limits, brake check.
*   Pre-takeoff checks: SAS channels engaged, EAC ON, trim set, flaps, fuel, canopy, warning panel clear.

**Module 4: Takeoff & Departure**
*   Normal takeoff: lineup, throttle advance, directional control (NWS → rudder transition), rotation speed (Vr) by weight, positive rate — gear up, flap retraction schedule.
*   Crosswind takeoff technique: max demonstrated crosswind (30 kts dry, 20 kts wet per AFMAN 11-2A-10C Vol 3).
*   Rejected takeoff (abort): decision speed, procedure (throttle idle, max braking, speedbrakes open, emergency — jettison/fire handle if needed).
*   Climb profile: Vy (200–220 KIAS), climb power setting, level-off technique.
*   Departure: standard VFR departure, overhead break entry if applicable.

**Module 5: Basic Flight Maneuvers**
*   Level flight: cruise speed, power settings for various altitudes.
*   Turns: coordinated technique, load factor awareness (G meter reading), AoA management in turns, bank angle vs. G.
*   Climbs and descents: recommended profiles, AoA awareness during descents.
*   Slow flight: flap extension schedule (MVR at 200 KIAS, DN below 200 KIAS), minimum controllable airspeed (VMCA), SAS behavior at low speed.
*   Approach-to-stall: AoA indexer progression (green donut → upper chevron → lower chevron → stall buffet), recognition and recovery.
*   **Trim technique:** The A-10C requires constant trimming. Electric trim vs. manual trim tab. SAS trimming behavior.
*   Speed brake operation: deployment, retraction, speed brake effects on pitch.

**Module 6: Navigation (Basic CDU/EGI)**
*   Steerpoint navigation: selecting steerpoints on CDU, HUD steerpoint cue (tadpole), distance/bearing/ETA readout.
*   Creating a steerpoint in the CDU: entering LAT/LONG, MGRS coordinates.
*   Mark point creation: capturing current position as a steerpoint.
*   HSI (Horizontal Situation Indicator): heading, course, bearing-to-steerpoint.
*   MFCD TAD (Tactical Awareness Display): basic orientation — own-ship symbol, steerpoints, range scale.
*   TACAN: mode selection (T/R, A/A), channel set, CDI needle, DME.
*   ILS approach setup: frequency set on UFC, CDI/glideslope indication on ADI.
*   **Scope limitation:** This module covers "how to get from A to B." Mission planning, data cartridge loading, threat rings, and tactical navigation are out of scope.

**Module 7: Emergency Procedures (Academic)**
*   **Boldface (Memory) Items:** Per AFMAN 11-2A-10C Vol 3 — these must be memorized verbatim:
    *   Abort (engine failure/fire on takeoff)
    *   Engine fire in flight
    *   Double engine failure
    *   Manual reversion
    *   Ejection
*   Single engine failure: identification (asymmetric thrust, yaw), isolation, restart attempt, single-engine flying qualities, single-engine approach.
*   Hydraulic failure: A system failure, B system failure, dual hydraulic failure — manual reversion procedure and handling qualities.
*   Electrical failure: generator loss, bus shedding, essential bus behavior, battery-only flight time.
*   Fire: engine fire, APU fire, electrical fire — detection, isolation, response.
*   Landing gear emergency: normal vs. emergency extension, gear-unsafe indications, arrested landing considerations.
*   Controlled ejection: decision criteria, ACES II seat capability, minimum altitudes by flight condition.
*   **DCS-specific emergency notes:** Which failures DCS actually models vs. which are simplified or absent.

**Module 8: Traffic Pattern & Landing**
*   VFR traffic pattern: overhead break entry (350 kts, 1,500 ft AGL), break turn (60° bank), downwind leg (200 kts, gear and flaps), base turn, final approach.
*   Straight-in approach: when to use, speed schedule, configuration timing.
*   Final approach: **AoA indexer is the primary reference** (green donut = on-speed), typical approach speed 130–140 KIAS.
*   Glidepath: visual aim point (1,000 ft markers), 3° glidepath, PAPI/VASI references if available.
*   Flare and touchdown: the A-10 "flat attitude" landing technique — minimal flare, firm touchdown is acceptable.
*   Rollout: aerodynamic braking (hold nose up), wheel braking technique, speed brake deployment on rollout, avoiding brake fade.
*   Go-around / missed approach: full power, positive rate, gear up, flaps to MVR, clean up and re-enter pattern.
*   Crosswind landing: wing-low / crab technique, max demonstrated values.
*   **DCS-specific:** Autostart behavior (for reference only — the student must learn manual start, but should understand what autostart does differently).

**Module 9: Shutdown**
*   Post-landing taxi: canopy, lights, taxi to parking.
*   Shutdown procedure: throttles idle → cut-off, APU (if needed), avionics power-down sequence, battery off.
*   Full switch-by-switch shutdown from engines running to cold-and-dark.

**For each module, provide:**
1.  **Learning Objectives:** Measurable outcomes the student must demonstrate.
2.  **Key Data Table:** V-speeds, RPM percentages, ITT limits, AoA units, fuel flow figures, hydraulic pressures — with normal ranges and caution/warning thresholds.
3.  **Cockpit Switch Reference:** Specific switch names, panel locations, and the DCS mouse-click or HOTAS action to operate them. Include keyboard shortcuts as secondary reference where they exist.
4.  **Instructor Notes:** Common student failure points and how to address them. Focus on the most frequent errors seen in DCS (e.g., forgetting SAS engagement, skipping EGI alignment, not setting NWS to HI for taxi).
5.  **Realism Divergence Footnotes:** Where DCS simplifies or omits real-world procedures. Format as:
    > *⚠ Realism Divergence: [explanation]*

**Output Format:**
A single, structured Markdown document suitable for saving as `.github/research/a-10c-bqt-dossier.md`. Use heading levels ##, ###, and #### consistently. Tables for all data. Cockpit switch locations described by panel name (e.g., "AHCP — left glareshield", "Right console — CDU").
