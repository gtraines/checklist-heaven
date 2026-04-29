# Event 5 — Basic Navigation

> **Course:** UH-1H Huey Basic Qualification Training | **Event Type:** Simulator
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents

1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — Pre-Flight Navigation Planning](#part-1--pre-flight-navigation-planning)
4. [Part 2 — Radio Configuration and Frequency Management](#part-2--radio-configuration-and-frequency-management)
5. [Part 3 — Departure and Compass / DG Alignment](#part-3--departure-and-compass--dg-alignment)
6. [Part 4 — ADF Navigation (NDB Homing and Tracking)](#part-4--adf-navigation-ndb-homing-and-tracking)
7. [Part 5 — VOR Navigation (Radial Tracking)](#part-5--vor-navigation-radial-tracking)
8. [Part 6 — Dead Reckoning Navigation Leg](#part-6--dead-reckoning-navigation-leg)
9. [Part 7 — Return Navigation and Approach](#part-7--return-navigation-and-approach)
10. [Part 8 — Transponder and Radar Altimeter](#part-8--transponder-and-radar-altimeter)
11. [Completion Standards](#completion-standards)
12. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Complete a pre-flight navigation plan (route, magnetic courses, distances, times, frequencies, and checkpoints) before engine start, presented as a filled-out kneecard
- [ ] Tune each of the three communication radios (VHF-AM, UHF-AM, FM) to a specified frequency within 15 seconds while maintaining aircraft control in cruise flight
- [ ] Make all standard radio calls (startup, taxi, takeoff, downwind, base, final, landing, shutdown) with correct phraseology
- [ ] Correctly read and interpret the ADF bearing pointer; home to an NDB station; identify station passage; track outbound on a specified heading
- [ ] Tune a VOR, identify the station by Morse ident, determine current position radial, and track inbound to the station
- [ ] Demonstrate dead reckoning navigation on a 20–30 NM leg, arriving within 2 NM and 3 minutes of plan
- [ ] Reset the DG to the magnetic compass at least once during the flight, in straight and level unaccelerated flight
- [ ] Set the transponder squawk code and state the four emergency codes from memory (7700, 7600, 7500, 1200)
- [ ] Set the radar altimeter low-altitude warning bug; explain why the radar altimeter reads AGL rather than MSL

---

## Ground Brief

### Mission Profile

1. Pre-flight briefing: review kneecard (prepared before event)
2. Engine start — all standard radio calls from startup through departure
3. Departure climb to 2,500–3,000 ft AGL
4. ADF navigation leg — home to NDB station; identify station passage
5. VOR navigation leg — determine position; track inbound radial to VOR
6. Dead reckoning leg — specified course and distance using time/speed/distance
7. Compass/DG alignment check during cruise
8. Return to airfield — standard approach and landing
9. Shutdown

**This event is flown as a navigation cross-country**, not as a pattern/airwork event. The student manages navigation and communications while maintaining basic flight skills simultaneously.

### Key Numbers Table

| Parameter | Value | Notes |
|---|---|---|
| **Cruise airspeed** | 90–100 KIAS | Maintain throughout navigation legs |
| **Cruise altitude** | 2,500–3,000 ft AGL | As planned |
| **ADF frequency range** | 190–1,799.5 kHz | NDB station frequency; found in DCS mission briefing |
| **VOR frequency range** | 108.00–117.95 MHz | VOR station; also ILS if odd tenths |
| **DG reset interval** | Every 10–15 min | Compare to magnetic compass; reset in straight/level unaccelerated |
| **Transponder STANDBY → ON** | Before taxi | Set squawk code before STANDBY |
| **Standard VFR squawk** | 1200 | Used when no ATC squawk assigned |
| **Emergency squawk** | 7700 | Also: 7600 (radio failure), 7500 (hijack) |
| **Radar altimeter range** | 0–5,000 ft AGL | Set bug to MSA for the route |
| **DR formula** | D = S × T | Distance = Speed (KIAS) × Time (hrs) |

### Pre-Flight Kneecard Requirements

The student must present a completed kneecard before the IP will authorize engine start:

| Item | Required |
|---|---|
| Route legs with start/end points | ✓ |
| True course (°T) for each leg | ✓ |
| Magnetic course (°M) for each leg — variation applied | ✓ |
| Wind correction angle (if wind forecast available) | ✓ |
| Magnetic heading (°M) for each leg | ✓ |
| Distance (NM) for each leg | ✓ |
| Estimated time enroute (ETE) for each leg at 90 KIAS | ✓ |
| NDB frequency (for ADF leg) | ✓ |
| VOR frequency (for VOR leg) | ✓ |
| ATC frequencies (ground, tower, departure) | ✓ |
| Visual checkpoints (at ~10 NM intervals) | ✓ |
| Alternate airfield (name and frequency) | ✓ |

> **No kneecard = no flight.** This is a training discipline standard. The student must demonstrate they have planned the flight before the flight begins.

### Radio Assignment by Phase

| Phase | Radio | Frequency |
|---|---|---|
| Startup / Ground | VHF-AM (`V`) | Ground / ATIS frequency |
| Taxi | VHF-AM (`V`) | Ground frequency |
| Takeoff / Pattern | VHF-AM (`V`) | Tower frequency |
| Departure / Enroute | VHF-AM (`V`) | Departure / Area control |
| Emergency (passive monitor) | UHF-AM (`Y`) | GUARD (243.0 MHz) |
| Tactical (if applicable) | FM (`C`) | Assigned FM frequency |
| Approach / Landing | VHF-AM (`V`) | Approach / Tower |

---

## Part 1 — Pre-Flight Navigation Planning

> **Completed before engine start. IP reviews kneecard during ground brief.**

### Dead Reckoning Calculation (Example)

*Students use this formula for each planned DR leg:*

**ETE (min) = Distance (NM) ÷ Groundspeed (kts) × 60**

Example — 27 NM leg at 90 KIAS with a 10-knot headwind:
- Groundspeed ≈ 90 − 10 = 80 kts
- ETE = 27 ÷ 80 × 60 = 20.25 min ≈ 20 min 15 sec

**Magnetic Course Calculation:**

- True Course (map measurement) ± Magnetic Variation = Magnetic Course
- Magnetic Course ± Wind Correction Angle = Magnetic Heading to fly

**Visual Checkpoint Planning:**

| Checkpoint | Feature | Distance from Departure | Expected Time |
|---|---|---|---|
| CP-1 | (IP assigns per DCS map) | 10 NM | ETE − 7 min |
| CP-2 | (IP assigns per DCS map) | 20 NM | ETE − 3 min |
| NDB | ADF station | As planned | Bearing pointer swings |
| VOR | VOR station | As planned | CDI centers |

---

## Part 2 — Radio Configuration and Frequency Management

### Startup Radios

| Step | Action | Radio | Expected Result |
|---|---|---|---|
| 1 | Tune VHF-AM to ATIS or Ground frequency (from kneecard) | AN/ARC-134 (top pedestal) | Radio active; receive ATIS information |
| 2 | Set UHF-AM to GUARD mode | AN/ARC-51BX (middle pedestal) | Monitoring 243.0 MHz passively |
| 3 | Tune FM if required by mission | AN/ARC-131 (bottom pedestal) | Assigned FM frequency |
| 4 | Audio control panel — set volumes | Pedestal — audio panels | VHF loudest; UHF moderate; FM as required |
| 5 | Verify transmit selector on VHF-AM | Audio panel transmit switch | VHF selected for transmit |

### VHF-AM (AN/ARC-134) Tuning Procedure

Knobs are labeled 100 MHz, 10 MHz, 1 MHz, 0.1/0.025 MHz (from left to right):

**Example: Tune to 124.000 MHz**

| Knob | Set To |
|---|---|
| 100 MHz | 1 |
| 10 MHz | 2 |
| 1 MHz | 4 |
| 0.1 MHz | 0.0 |

In DCS: Left-click each knob to increase, right-click to decrease. Mouse scroll wheel = fine adjustment.

**Time limit:** Change any VHF frequency within 15 seconds while maintaining cruise flight. Practice this before the navigation event. If more than 15 seconds are required, altitude and heading deviations occur — this indicates the student is not yet proficient.

### Standard Radio Calls (Required for This Event)

All calls made in this event — student performs them, not IP:

| Phase | Call |
|---|---|
| **Request startup** | "*[Airfield] Ground, [Callsign], [parking spot], request startup, Information [letter]*" |
| **Request hover taxi** | "*[Airfield] Ground, [Callsign], ready to hover taxi, runway [X]*" |
| **Read-back taxi clearance** | Read back runway, taxiway, and any hold-short instructions verbatim |
| **Ready for departure** | "*[Airfield] Tower, [Callsign], holding short runway [X], ready for departure*" |
| **Read-back takeoff clearance** | Read back runway, wind, and clearance |
| **Frequency change (departing)** | "*[Airfield] Tower, request frequency change, [Callsign]*" |
| **Check-in with new frequency** | "*[Facility], [Callsign], passing [altitude], [intentions]*" |
| **Pattern calls (return)** | Downwind: position, runway, intent / Base: turning / Final: final, full stop |
| **After landing** | Contact ground; report clear of runway |
| **Shutdown** | "*[Airfield] Ground, [Callsign], [spot], shutting down*" |

> *⚠ DCS limitation: DCS single-player ATC responds to a menu system, not free speech. However, the student should verbally state the intended call before selecting the menu option. This builds phraseology habits for multiplayer.*

---

## Part 3 — Departure and Compass / DG Alignment

### Departure Sequence

| Step | Action | Notes |
|---|---|---|
| 1 | Standard startup; before-takeoff check | Reference Event 2 |
| 2 | Transponder — set squawk code, then STANDBY | Code from kneecard or ATC |
| 3 | Make all radio calls per Part 2 script | Student performs all calls |
| 4 | Transponder — ALT (altitude reporting) before departure | As ATC instructs or standard local procedure |
| 5 | Normal takeoff through ETL; climb to 2,500–3,000 ft AGL at Vy | Reference Event 3/4 |
| 6 | Level off; set cruise (90–100 KIAS) | Set force trim |
| 7 | Frequency change to departure/area control | Make call; check in on new frequency |

### DG Alignment (First Check, Departure Phase)

| Step | Conditions Required | Action |
|---|---|---|
| 1 | Straight and level, cruise airspeed, unaccelerated | Establish before reading |
| 2 | Read magnetic compass | Wait for compass to settle (~5 seconds after last turn) |
| 3 | Compare to DG heading | Note any difference |
| 4 | If difference >3°: adjust DG knob to match compass reading | Rotate the DG heading selector until DG matches compass |
| 5 | Record the time | Reset again in 10–15 minutes |

> **Reminder:** The magnetic compass is accurate only in straight, level, unaccelerated flight. Do not attempt to read the compass during a turn, acceleration, or deceleration.

**Student callout:** "DG aligned to magnetic, [heading]°. Next alignment in 15 minutes."

---

## Part 4 — ADF Navigation (NDB Homing and Tracking)

> **Prerequisites:** ADF (AN/ARN-83) powered on; NDB frequency tuned from kneecard; station identified by Morse code ident.**

### ADF Station Identification

| Step | Action | Expected Result |
|---|---|---|
| 1 | Tune ADF frequency on AN/ARN-83 control head | Bearing pointer activates |
| 2 | Set mode switch to ADF | Bearing pointer swings toward station |
| 3 | Enable NAV audio on audio control panel | Morse code ident audible in headset |
| 4 | **Identify station** — listen for Morse code (2–3 letters) and match to published ident | Confirmed — proceed; Unconfirmed — do not use bearing pointer |

> **Rule:** If you cannot hear and confirm the station ident, you cannot trust the bearing pointer. This applies in real-world AND in DCS.

### ADF Homing Procedure

| Step | Action | Notes |
|---|---|---|
| 1 | Read bearing pointer on compass card | Pointer shows direction to station relative to nose |
| 2 | Turn aircraft until bearing pointer points to **12 o'clock** (directly ahead) | Aircraft is now aimed at the station |
| 3 | Fly toward station | Monitor bearing pointer continuously |
| 4 | In crosswind: bearing pointer drifts off nose | Correct heading to keep pointer near 12 o'clock |
| 5 | As station approaches — pointer becomes very sensitive | Small position changes = large pointer movement |
| 6 | **Station passage** — pointer swings rapidly from 12 o'clock to 6 o'clock | Note time; turn to outbound heading immediately |

**Homing vs. Tracking (Brief to Student):**

| Method | Technique | Track Result |
|---|---|---|
| **Homing** | Always point nose at station (pointer at 12 o'clock) | Curved track in crosswind — less efficient |
| **Tracking (wind correction)** | Apply WCA so that relative bearing compensates for wind | Straight track to station — more efficient |

For BQT, homing is the minimum standard. Tracking with wind correction is the proficiency standard.

### ADF Outbound

After station passage, turn to the planned outbound heading. The bearing pointer will now point to approximately 6 o'clock (behind), confirming station passage.

---

## Part 5 — VOR Navigation (Radial Tracking)

> **Prerequisites:** VOR receiver (AN/ARN-82) powered on; VOR frequency tuned; station identified by Morse code ident.**

### VOR Station Identification

Same requirement as ADF — must hear and confirm Morse code ident before using the CDI.

### Determine Current Position (Position Fix)

| Step | Action | Expected Result |
|---|---|---|
| 1 | Tune VOR frequency; identify station | Verified |
| 2 | Rotate OBS knob until CDI **centers** with **FROM** flag | Centered CDI + FROM = current radial |
| 3 | Read the radial from the OBS window | This is the radial you are on — your magnetic bearing FROM the station |
| 4 | Student verbalizes: "I am on the [X]° radial from [station]" | Cross-reference with DG heading and ADF if available for position fix |

### Track Inbound to VOR

| Step | Action | Notes |
|---|---|---|
| 1 | Set OBS to desired **inbound course** (the reciprocal of the outbound radial) | Example: if flying from the east, set OBS to ~270° (inbound heading) |
| 2 | **TO flag** should appear | If FROM flag appears, you are on the wrong side of the station |
| 3 | Fly a heading to **center the CDI** | CDI deflected right → fly right; CDI deflected left → fly left |
| 4 | Apply **wind correction angle** to hold CDI centered | Small heading changes (5–10°); observe CDI response before correcting further |
| 5 | Maintain centered CDI to station | Sensitivity increases as station gets closer |
| 6 | **Station passage** — CDI becomes erratic; TO/FROM flag flips | Note time; transition to outbound if planned |

### CDI Rule: "Fly toward the needle"

- CDI deflected **right** → turn **right**
- CDI deflected **left** → turn **left**

This rule works for both TO and FROM indications. Use it as a memory aid until VOR tracking becomes instinctive.

---

## Part 6 — Dead Reckoning Navigation Leg

> **The IP assigns a heading, distance, and expected time. Student flies the DR leg from a defined departure point to an assigned destination, using heading and time only (no nav aid references during the leg).**

### DR Leg Execution

| Step | Action | Notes |
|---|---|---|
| 1 | At departure fix: note time; set DG to planned magnetic heading | Write off-blocks time on kneecard |
| 2 | Fly planned heading at 90 KIAS | Maintain ±5° heading; maintain ±100 ft altitude |
| 3 | Reset DG if 10–15 min interval has passed | In straight and level; use compass |
| 4 | At expected checkpoint times (CP-1, CP-2): look for planned visual landmarks | Identify landmark; note position vs. plan |
| 5 | Apply heading correction if landmark is off to one side | Estimate correction; update heading on kneecard |
| 6 | At calculated ETA — identify destination area | If within 2 NM and ±3 min = satisfactory |
| 7 | Student verbalizes: "Checkpoint identified [feature], on track / [X] NM [direction] of track" | IP evaluates identification and correction |

### DR Position Error Assessment

| Error | Diagnosis | Correction |
|---|---|---|
| Ahead of ETA with destination not reached | Groundspeed higher than planned (tailwind or faster airspeed) | Extend time; revise ETA |
| Behind ETA at destination | Groundspeed lower (headwind or slower airspeed) | Expected — adjust future leg times |
| Left of track | Wind from right, insufficient left WCA | Turn right to regain track |
| Right of track | Wind from left, insufficient right WCA | Turn left to regain track |

**Key lesson:** DR error accumulates. Cross-check with ADF/VOR at the first opportunity once the DR leg is complete.

---

## Part 7 — Return Navigation and Approach

### Return Navigation

| Step | Action | Notes |
|---|---|---|
| 1 | Turn to return heading (from kneecard) | DG set to return magnetic heading |
| 2 | Identify return nav aid (VOR or NDB) if available on return leg | Track inbound for final approach |
| 3 | Contact approach/tower frequency | VHF-AM; use standard radio calls |
| 4 | Transponder — ALT confirmed | For ATC identification |
| 5 | Descend to pattern altitude as directed | Cruise descent; 90 KIAS; 500–1,000 fpm |
| 6 | Enter traffic pattern | Per ATC instructions; standard left-hand unless directed otherwise |
| 7 | Standard radio calls: downwind, base, final | All student-performed |
| 8 | Approach and landing | Reference Event 3 technique; decelerate to hover; land |
| 9 | Clear runway; contact ground | "Clear runway [X], [Callsign]" |
| 10 | Hover taxi to parking | Reference Event 2/3 |
| 11 | Shutdown; "shutting down" call to ground | All steps per Event 2 |

---

## Part 8 — Transponder and Radar Altimeter

### Transponder

| Code | Meaning |
|---|---|
| **1200** | Standard VFR, no ATC squawk assigned |
| **7700** | Emergency — mayday condition |
| **7600** | Radio failure — cannot receive ATC |
| **7500** | Hijack / unlawful interference |
| **ATC-assigned** | Use exactly as assigned; read back to ATC |

**Setting the transponder:**
1. Rotate the four digit knobs to the desired code.
2. Mode switch to STANDBY during startup.
3. Mode switch to ON or ALT before taxi (per ATC or local procedures).
4. Press IDENT only when ATC requests "Squawk ident."

**Student quiz (before flight):** IP asks for each emergency code — student must answer without reference.

### Radar Altimeter

| Setting | Technique |
|---|---|
| **Bug setting** | Set to minimum safe altitude for the planned route (e.g., 200 ft for general flight; 50 ft for low-level) |
| **During approach** | Set to decision altitude or desired hover height |
| **AGL vs. MSL** | Radar altimeter reads **directly below the aircraft** — not terrain ahead; on sloping terrain, reading changes rapidly |
| **Cross-check** | Cross-check radar altimeter against barometric altimeter on approach — the difference is the terrain elevation MSL |

**Student verbalization:** After setting the bug: "Radar altimeter bug set to [X] ft AGL. Warning will trigger below this altitude."

---

## Completion Standards

| Standard | Requirement |
|---|---|
| **Kneecard** | Completed before engine start; all required items present (route, courses, distances, times, frequencies, checkpoints) |
| **Radio tuning** | Any radio tuned to a specified frequency within 15 seconds while maintaining cruise flight within tolerances |
| **Radio calls** | All standard calls made with correct phraseology; no significant errors (wrong callsign, wrong facility, inverted read-back) |
| **ADF navigation** | Station identified by ident; homed to NDB; station passage recognized (pointer swings to 6 o'clock); outbound heading established within ±10° |
| **VOR navigation** | Station identified; current radial determined; CDI tracked inbound with no more than ½ dot average deflection over a 5-NM leg |
| **Dead reckoning** | Destination identified within 2 NM lateral and ±3 minutes ETA on IP-assigned DR leg |
| **DG alignment** | Performed at least once in flight; at correct conditions (straight/level/unaccelerated); correct technique |
| **Transponder codes** | State all four emergency codes correctly from memory |
| **Cruise standards maintained** | ±100 ft altitude, ±10 KIAS, ±10° heading throughout navigation legs (additional deviation during radio tuning is acceptable — note and correct) |

> **Go/No-Go for Event 6:** Student must demonstrate ADF bearing pointer interpretation, inbound VOR tracking, and correct radio phraseology for all calls before progressing to Event 6.

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| No kneecard / incomplete kneecard | Not authorized to fly | Require it before every navigation event — no exceptions |
| Using F10 map instead of instruments | Navigation skill not built | Progressively restrict F10 access: Event 5 = reference allowed; later events = only for emergencies |
| Cannot read ADF bearing pointer | Navigates by guess; misidentifies station passage | Ground exercise: draw compass card, place pointer, ask "Which direction is the station?" 10 reps minimum |
| "Fly away from CDI needle" (VOR confusion) | Departs course; CDI deviates further | Repeat the rule: "Fly toward the needle." Demonstrate both cases on the ground |
| Not identifying nav aids by Morse code | Using unreliable indication; possibly tuned to wrong station | Enforce: "Can you hear the ident?" If no — re-tune and try again |
| Not resetting DG | DG precesses; heading errors accumulate; DR error grows | Set a 10-minute timer as a habit. IP calls "check your DG" if student forgets |
| Transmitting on wrong radio | Call heard on wrong frequency or not heard at all | Before transmitting: "Verify selector → key radio." Build as a habit |
| Forgetting frequency changes (missing calls) | ATC loses track of aircraft; student gets lost | Write frequency plan on kneecard in sequence; check off each frequency as changed |
| DR arriving far from destination | Incorrect heading, incorrect time, or ignored wind | Debrief each DR leg with a map — show student where they actually were vs. planned |

---

*Based on TM 55-1520-210-10, FM 3-04.203, FM 1-240, TC 3-04.4, and Eagle Dynamics / Belsimtek DCS UH-1H Huey module documentation. For simulation use only.*
