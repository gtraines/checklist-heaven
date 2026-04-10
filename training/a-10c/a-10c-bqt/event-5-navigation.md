# Event 5 — Navigation

> **Course:** A-10C Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Avionics Familiarization (Ground)](#part-1--avionics-familiarization-ground)
5. [Part 2 — CDU Navigation](#part-2--cdu-navigation)
6. [Part 3 — TACAN Navigation](#part-3--tacan-navigation)
7. [Part 4 — TAD & HSD Orientation](#part-4--tad--hsd-orientation)
8. [Part 5 — ILS Approach Setup & Execution](#part-5--ils-approach-setup--execution)
9. [Part 6 — Full-Stop Landing](#part-6--full-stop-landing)
10. [Completion Standards](#completion-standards)
11. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Enter and select CDU steerpoints during flight
- [ ] Navigate using STEER-PT mode with HSI/CDI tracking
- [ ] Set up a TACAN channel and navigate to a TACAN station or offset
- [ ] Orient themselves on the TAD (Tactical Awareness Display) and understand HSD symbology
- [ ] Program and fly a VOR/ILS approach using the CDU and HSI
- [ ] Fly an ILS approach to minimums and execute a landing

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Pre-flight | Avionics familiarization on ground (static) |
| Phase 1 | Startup, taxi, takeoff — standard |
| Phase 2 | CDU steerpoint navigation — fly a 3-point route |
| Phase 3 | TACAN bearing/distance navigation |
| Phase 4 | TAD/HSD situational awareness exercises |
| Phase 5 | ILS approach setup and execution |
| Phase 6 | Full-stop landing |

### Key Navigation Concepts

| Concept | Summary |
|---|---|
| **STEER-PT** | CDU command mode that activates current steerpoint as nav destination |
| **Steerpoint** | Georeferenced waypoint stored in CDU; displayed as numbered STP icon on TAD |
| **CDI** | Course Deviation Indicator on HSI — needle left/right shows off-course |
| **TACAN** | UHF ranging/bearing nav system; gives bearing and DME (nautical miles) |
| **TAD** | Tactical Awareness Display (MFD page) — top-down god's-eye view of aircraft + steerpoints |
| **HSD** | Horizontal Situation Display (MFD page) — compass-oriented HSI-like tactical display |
| **ILS** | Instrument Landing System; localizer (lateral) + glideslope (vertical) needles on HSI |
| **EGI** | Embedded GPS/INS — primary navigation source; fully degraded if GPS signal lost |

---

## Pre-Mission Setup

- [ ] Cold and dark start (student performs with no checklist prompts)
- [ ] In CDU ground setup: load a 3-steerpoint route prior to taxi (see Part 1)
- [ ] Weather: **light overcast or broken — MVFR (ceiling 2,000 ft)** to make ILS meaningful
- [ ] Wind: light crosswind (5–10 kts) to add minor challenge to landing
- [ ] Fuel: 100% — this event is longer than previous events

---

## Part 1 — Avionics Familiarization (Ground)

Complete this phase during engine start and EGI alignment (idle time).

### CDU Overview

The CDU (Control and Display Unit) is the primary avionics management computer for the A-10C. It controls:
- Navigation (steerpoints, flight plans)
- Sensor management
- Weapons delivery data

| CDU Page | Access | Function |
|---|---|---|
| STEER | `STE` LSK | Activate/select steerpoints |
| NAV | Main menu → NAV | Navigation mode; set as STEER-PT for waypoint nav |
| WAYPT | Main menu → WAYPT | View and edit steerpoints |
| COMM | Main menu → COMM | Radio frequencies (presets and manual) |

### Entering a Steerpoint

1. CDU power ON → `WAYPT` (left-side LSK)
2. Select steerpoint number (use number keys 1–99)
3. LSK next to latitude field → enter coordinates (or accept pre-loaded mission data)
4. LSK next to longitude field → enter coordinates
5. LSK `ELEV` → enter elevation (ft MSL)
6. Press `ENTR` → steerpoint saved
7. Repeat for additional steerpoints

> **DCS Note:** In most DCS missions, steerpoints are pre-loaded from the mission file. The pilot selects them; they do not normally need to enter raw coordinates. Confirm in the pre-mission briefing screen.

### Selecting a Steerpoint

| Method | Action |
|---|---|
| CDU | `STE` → steerpoint number → ENTR |
| UFC slew | `↑` / `↓` buttons under STEER readout |
| HOTAS | TMS button (preset to cycle steerpoints) |

### Activating Steerpoint Navigation

1. CDU main menu → `NAV`
2. NAV mode display → select **STEER-PT**
3. HSI CDI needle deflects toward steerpoint
4. TAD displays aircraft position relative to steerpoint symbol

---

## Part 2 — CDU Navigation

### Pre-Flight Steerpoint Setup (Complete Before Taxi)

Load 3 steerpoints forming a triangular route departing from and returning to the airfield.

| STP | Description | Notes |
|---|---|---|
| 1 | Airfield (homebase) | Loaded by default in most missions |
| 2 | Checkpoint A — identifiable landmark | Mountain peak, lake, coastal feature |
| 3 | Checkpoint B — 40–60 nm from A | Another identifiable feature |
| 4 | Return to airfield (same as STP 1 or separate approach fix) | |

### Inflight Exercise

1. After takeoff and established at 10,000 ft:
   - [ ] Select **STP 2** on CDU; confirm HSI CDI needle deflects toward STP 2
   - [ ] Fly to intercept the CDI centerline; maintain track
   - [ ] Cross-check TAD — confirm ownship moving toward STP symbol
2. At STP 2:
   - [ ] Fly-over confirmed (STP 2 symbol passes aft on TAD)
   - [ ] Select **STP 3** — CDI swings to new course
   - [ ] Fly to STP 3
3. At STP 3:
   - [ ] Select **STP 4** (return) — fly home
4. During all legs, maintain:
   - Altitude: **10,000 ft ±150 ft**
   - Airspeed: **250 KIAS ±15 KIAS**
   - CDI centered ±half-deflection

> **Note on CDI tracking:** Do not "chase" the CDI needle with abrupt turns. Intercept the course at a 30–45° cut, then gently roll toward the course as the needle centers. Once centered, fly the course heading.

---

## Part 3 — TACAN Navigation

### TACAN Setup

1. **TACAN control panel** (left console, avionics bay):
   - Channel: enter 3-digit channel number (e.g., channel 26X for Batumi in DCS)
   - Mode: **T/R** (Transmit/Receive)
   - Volume: set audible for Morse code ID
2. UFC: TACAN channel can be entered via UFC → `TCN` button:
   - Press `TCN` → enter channel → `ENTR`
   - Select mode via OSB adjacent to mode field
3. HSI: select **TACAN** mode — CDI needle now points to/from the TACAN station

### TACAN HSI Interpretation

| HSI Element | Meaning |
|---|---|
| CDI needle | Deflects left/right of course line — track correction required |
| Bearing pointer | Points toward TACAN station from ownship |
| DME readout | Distance (nm) from TACAN station |
| TO/FROM flag | **TO** = flying toward the station; **FROM** = past it |

### Exercise: Fly to TACAN Station

1. With TACAN tuned and receiving (bearing pointer active):
   - [ ] Turn to align heading with bearing pointer — fly direct to station
   - [ ] Cross-check decreasing DME — confirm closing
   - [ ] At station passage: bearing pointer swings; DME decreases to near-zero then increases
   - [ ] Note TO → FROM flip on HSI
2. Fly **away from station** to 10 nm; turn back inbound
3. Set course (OBS/CRS knob on HSI) to station bearing; center CDI; fly inbound track

---

## Part 4 — TAD & HSD Orientation

### TAD Page Setup

1. Left or right MFD → `TAD` (OSB or menu)
2. TAD scale: adjust with `SCL+` / `SCL-` OSBs — start at **40 nm** scale
3. TAD orientation: **NORTH-UP** (first) then switch to **TRACK-UP** for comparison

| TAD Symbol | Meaning |
|---|---|
| Aircraft symbol (center) | Ownship — pointing in direction of travel |
| Numbered circles | CDU steerpoints |
| Dotted line | Course to current steerpoint |
| FLIR footprint (if TGP active) | Sensor coverage cone |
| Ownship velocity vector | Short line from nose — shows where aircraft will be in ~60 seconds |

### TAD Exercises

- [ ] At TAD scale 40 nm: identify all 3 steerpoints by number
- [ ] Reduce scale to 10 nm: confirm ownship centered; steerpoints may be off-screen
- [ ] Switch to TRACK-UP: aircraft remains at center; map rotates with heading
- [ ] Switch to NORTH-UP: traditional map orientation; easier to correlate with paper charts
- [ ] Cross-check steerpoint on TAD vs. CDU readout vs. HSI bearing

### HSD Page

1. MFD → `HSD` (Horizontal Situation Display)
2. HSD is a compass-oriented HSI-style display with tactical overlay

| HSD Element | Meaning |
|---|---|
| Compass rose | Heading reference; aircraft heading at top |
| Current steerpoint bearing line | Line from ownship to steerpoint |
| CDI bar | Same as HSI needle — course deviation |
| DME ring | Circle at steerpoint DME distance |

> **HSD vs. TAD:** Use TAD for situational awareness (where am I relative to the world?). Use HSD for navigation management (am I on course?). Most pilots display TAD on one MFD and HSD on the other.

---

## Part 5 — ILS Approach Setup & Execution

### Pre-Approach Briefing

Before beginning descent:
- [ ] Identify ILS frequency for destination runway (from kneeboard, mission briefing, or airport plate)
- [ ] Identify inbound course (localizer course in degrees)
- [ ] Identify glideslope angle (typically 3.0°)
- [ ] Identify Decision Altitude (DA) or Minimum Descent Altitude (MDA)
- [ ] Identify missed approach procedure: heading, altitude, fix

### ILS Setup on UFC

1. **UFC** → `ILS` button
2. Enter ILS frequency (e.g., 108.90 MHz)
3. Enter inbound course (e.g., 130°)
4. Press `ENTR` → UFC activates ILS

> **DCS Note:** ILS frequencies in DCS missions are listed in the kneeboard (F10 map → airport info in some missions). Common DCS ILS examples: Batumi ILS RWY 13 = 110.30 MHz, course 126°.

### HSI ILS Mode

1. HSI mode selector → `ILS`
2. Set course (CRS) to localizer inbound course
3. HSI now displays:
   - **CDI needle**: localizer — left/right of course
   - **Glideslope bar**: above/below glideslope (vertical needle)
   - **Fly-to indication**: turn toward CDI deflection to correct

### ILS Approach — Procedure

| Phase | Action |
|---|---|
| **Setup (30 nm out)** | Tune ILS; set course; confirm HSI mode ILS; set altimeter |
| **Initial descent** | Descend to approach altitude (per airport plate or 2,500 ft AGL if unknown) |
| **Localizer intercept** | Fly toward final approach course; intercept at 30–45° cut |
| **Established on loc** | CDI centered ±half-deflection; maintain inbound course |
| **Glideslope intercept** | At final approach fix, watch glideslope bar descend to center; begin descent when centered |
| **Final** | Both CDI and GS bar centered; 3° descent; 130–135 KIAS; gear + flaps DN |
| **Decision Altitude** | Runway in sight → land; not in sight → **missed approach immediately** |

### Common ILS Corrections

| Indication | Correction |
|---|---|
| CDI deflects right | Fly right (turn toward the needle) |
| CDI deflects left | Fly left (turn toward the needle) |
| GS bar above | You are **below** glideslope — add power; raise nose slightly |
| GS bar below | You are **above** glideslope — reduce power; lower nose slightly |

> **Technique for stable ILS:** Once established, make **small, smooth corrections** using gentle bank changes (< 15°) for localizer and minor power adjustments for glideslope. Do not chase needles with large inputs.

### Minimums Callout

At 500 ft AGL callout: *"Five hundred."*
At minimums (typically 200 ft AGL on ILS Cat I): *"Minimums."*
- Runway in sight → *"Runway, landing"* → land
- Runway NOT in sight → *"Missed approach"* → apply power; climb; follow missed approach

---

## Part 6 — Full-Stop Landing

- Student executes approach from ILS final (or VFR pattern if weather permits)
- Focus: stabilized, on-speed, on-glidepath touchdown
- Post-touchdown: speed brakes, aerodynamic braking, smooth transition to wheel brakes
- Clear runway promptly; standard taxi and shutdown

---

## Completion Standards

| Standard | Requirement |
|---|---|
| CDU steerpoint selection | Correct STP selected with no instructor prompting |
| Course tracking | CDI within half-deflection for ≥ 80% of each leg |
| TACAN setup | Station identified (Morse ID), bearing pointer active |
| TACAN station passage | Identifies TO → FROM flip and confirms inbound track |
| TAD orientation | Can identify ownship, steerpoints, and velocity vector on 40 nm scale |
| ILS setup | Correct frequency and course entered before approach |
| ILS localizer | CDI within half-deflection from FAF to threshold |
| ILS glideslope | Glideslope bar within full deflection; corrections initiated within 5 seconds |
| Minimums call | Verbal callout at 500 ft and minimums |
| Landing | Stabilized by 300 ft AGL; touchdown within 1,500 ft of threshold |

---

## Common Errors

| Error | Correction |
|---|---|
| Chasing CDI with large bank angles | Use gentle turns (< 20°) for CDI corrections. Overshoot and undershoot cycles = too aggressive. |
| Forgetting to set OBS/CRS for ILS | The CDI needle is meaningless unless the course is set. Always set CRS = localizer course. |
| Glideslope descent starts too early | Glideslope descent begins only when the GS bar is centered (descending from above), not at FAF. |
| Looking down at CDU during approach | Avionics must be set BEFORE the final approach gate. Eyes outside and on instruments on final. |
| Not identifying TACAN by Morse code | Brief the ID before calling the station active. Mistuned TACAN is a common navigation error. |
| Missed approach indecision | "If you're not seeing the runway at minimums, go around. Do not look for it below minimums." |

---

[← Event 4: Familiarization Flight 2](event-4-fam-2.md) | [→ Event 6: Traffic Pattern](event-6-traffic-pattern.md)

---

*Based on T.O. 1A-10C-1, AFMAN 11-2A-10C Vol 3, and Eagle Dynamics DCS A-10C documentation. For simulation use only.*
