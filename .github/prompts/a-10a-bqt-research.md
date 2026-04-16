Act as an expert military aviation instructor and USAF A-10A "Thunderbolt II" pilot, cross-referencing real-world technical manuals with DCS World simulation documentation. I need you to compile a detailed research dossier for an **A-10A Basic Qualification Training (BQT) Course**.

**Objective:**
Create a structured syllabus and technical research document covering all aspects of safe A-10A operation from cold-and-dark startup to safe recovery. Combat employment is **out of scope** for this course.

**Correction Directive:**
A previous version of this research dossier (`.github/research/a-10a-bqt-dossier.md`) was generated and found to contain inaccuracies. This prompt is being re-executed to produce a corrected, authoritative replacement. When generating each module, cross-check all numerical data (V-speeds, RPM limits, EGT limits, fuel capacities, weights, distances) against the T.O. 1A-10A-1 or best available real-world sources. Where DCS behavior overrides the real-world value, clearly mark it. Do not carry forward unverified data from the prior dossier — treat each module as a fresh research effort.

**Source Material Priority:**
1.  **Real-World (Primary Truth):** Use real USAF documentation wherever possible:
    *   *A1-A10A-1 Flight Manual* (T.O. 1A-10A-1) — the authoritative primary source.
    *   *A1-A10A-34-1-1 Non-Nuclear Weapons Delivery Manual* (for systems overview context only).
    *   USAF Instrument Flying and Contact Flying manuals for pattern/approach standards.
    *   Any publicly available ACC/AFMC A-10 NATOPS-equivalent guidance.
2.  **DCS Simulation (Secondary / Override):** Where the DCS A-10A "Flaming Cliffs" module diverges from real-world procedures (e.g., missing clickable systems, simplified avionics, absent INS alignment, keybind-only controls), **the DCS procedure is what the student will actually execute**. Document the DCS procedure as the primary instruction.
3.  **Divergence Footnotes:** Any time the real-world procedure differs from DCS, include a clearly marked footnote formatted as:
    > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

**Required Research Modules:**

**Module 1: Aircraft Systems & Aerodynamics**
*   TF34-GE-100 turbofan engines: key characteristics, spool-up behavior, thrust response.
*   Fuel system overview: internal tanks, feed sequence, low-fuel indications.
*   Flight control system: manual reversion capability, trim authority.
*   Survivability features relevant to flight operations (titanium tub, redundant systems).
*   Stall characteristics: AOA indexer, departure behavior, and spin susceptibility.

**Module 2: Ground Operations**
*   Pre-start checklist: electrical power, circuit breaker scan, warning light check.
*   Engine start sequence: GPU vs. battery start, crossbleed, start limitations (EGT / RPM gates).
*   Post-start systems check: hydraulics, flight controls, avionics warm-up.
*   Taxi procedures: nose wheel steering (NWS) engagement/disengagement, differential braking technique.
*   Run-up and arming checks (in DCS context: Master Arm discipline).

**Module 3: Communications**
*   Radio operation fundamentals: the A-10A has **UHF and VHF radios** accessible via DCS keybinds (Flaming Cliffs simplified radio model). The student must learn to:
    *   Select and tune frequencies using the DCS communications menu.
    *   Transmit on the correct radio for the situation (UHF for ATC/tower, VHF-FM for tactical).
    *   Monitor multiple frequencies where the sim permits.
    *   Use proper radio phraseology (FAA/ICAO for ATC, military brevity for tactical comms).
*   DCS Easy Communication mode: how the radio menu (`\` key) maps to real-world radio operations; what is abstracted away.
*   Common radio calls for the BQT environment: startup/taxi clearance, takeoff, pattern calls (crosswind, downwind, base, final), go-around, approach/landing clearance, shutdown advisory.
*   Guard frequency monitoring (UHF 243.0 MHz / VHF 121.5 MHz) — real-world significance and DCS implementation (if any).
*   SRS (SimpleRadio Standalone) integration notes: how SRS restores realistic radio behavior to the Flaming Cliffs A-10A; frequency management, radio selection, and PTT keying.
*   IFF/transponder: real-world Mode 1/2/3C/4 usage and DCS implementation status.

**Module 4: Takeoff & Departure**
*   Normal takeoff: flap setting, trim, rotation speed (Vr) by weight.
*   Maximum effort / short-field takeoff considerations.
*   Rejected takeoff (RTO) procedure and decision speed.
*   Obstacle clearance climb speeds (Vx, Vy) for typical training loads.
*   Gear and flap retraction schedule.

**Module 5: Basic Flight Maneuvers**
*   Level flight, straight-and-level cruise speeds, power settings.
*   Turns: coordinated technique, load factor awareness, AoA management.
*   Climbs and descents: recommended profiles and airspeed schedules.
*   Slow flight: flap extension schedule, minimum control speeds.
*   Approach-to-stall recognition and recovery (buffet onset, AOA warning tones).
*   Emergency Level Flight recovery (trim runaway awareness).

**Module 6: Emergency Procedures (Academic)**
*   Single engine failure (identification, isolation, single-engine approach).
*   Hydraulic system failure (manual reversion flying qualities).
*   Fire warning response.
*   Controlled ejection decision criteria (minimum altitude thresholds for the ACES II seat).

**Module 7: Approach & Landing**
*   VFR traffic pattern: altitudes, speeds, configurations by leg.
*   Visual Approach profile: AOA indexer targets, glidepath references.
*   Flare technique: the A-10 "flat attitude" landing technique.
*   Rollout: directional control, braking technique, avoiding brake fade.
*   Go-around procedure from any point in the pattern.

**For each module, provide:**
1.  **Learning Objectives:** Measurable outcomes the student must demonstrate.
2.  **Key Data Table:** V-speeds, RPM percentages, EGT limits, AOA units, fuel flow figures.
3.  **DCS Keybind Reference:** The specific DCS keyboard commands for each critical action.
4.  **Instructor Notes:** Common student failure points and how to address them.
5.  **Realism Divergence Footnotes:** Where DCS simplifies or omits real procedures.

**Output Format:**
A single, structured Markdown document suitable for saving as `.github/research/a-10a-bqt-dossier.md`. Use heading levels ##, ###, and #### consistently.
