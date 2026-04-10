# Event 2 — Startup & Ground Operations

> **Course:** A-10C Basic Qualification Training | **Event Type:** Flight (Ground Operations Focus)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Cold-and-Dark to Engines Running](#part-1--cold-and-dark-to-engines-running)
5. [Part 2 — Avionics Power-On](#part-2--avionics-power-on)
6. [Part 3 — EGI Alignment](#part-3--egi-alignment)
7. [Part 4 — Pre-Taxi Checks](#part-4--pre-taxi-checks)
8. [Part 5 — Taxi](#part-5--taxi)
9. [Part 6 — Pre-Takeoff Checks](#part-6--pre-takeoff-checks)
10. [Part 7 — Shutdown](#part-7--shutdown)
11. [Completion Standards](#completion-standards)
12. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Complete a full cold-and-dark startup without exceeding ITT limits or missing a start abort criterion
- [ ] Power on all avionics systems in the correct sequence
- [ ] Complete a full EGI alignment and verify NAV solution quality on the CDU
- [ ] Perform all pre-taxi and pre-takeoff checks without reference to notes
- [ ] Taxi the aircraft using NWS HI and NWS LO, differential braking, and correct speed control
- [ ] Perform a complete controlled shutdown from engines running to cold-and-dark

> **This event does not include takeoff or flight.** The student taxis to the runway, completes pre-takeoff checks, then taxis back and shuts down. If time permits, the sortie may include a single traffic pattern at the instructor's discretion.

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase 1 | Cold-and-dark startup (all switches) |
| Phase 2 | Avionics power-on sequence |
| Phase 3 | EGI alignment — wait for NAV READY |
| Phase 4 | Pre-taxi checks |
| Phase 5 | Taxi to runway and back to parking |
| Phase 6 | Pre-takeoff checks at hold short |
| Phase 7 | Shutdown — cold-and-dark |

### Key Numbers for This Event

| Item | Value |
|---|---|
| ITT Start Abort Limit | **860°C** |
| N2 for Fuel Introduction | ~12–15% |
| Engine Idle (N1) | 62–65% |
| Engine Idle (ITT) | 400–500°C |
| EGI Alignment Time | 3–5 min (full GC) |
| Max Taxi Speed (ramp) | 10 kts |
| Max Taxi Speed (straight taxiway) | 25 kts |
| Max Taxi Speed (turns) | 10 kts |

---

## Pre-Mission Setup

- [ ] Load DCS World; select **A-10C** or **A-10C II** on a prepared airfield
  - Caucasus: Batumi or Kobuleti recommended (well-marked taxiways)
  - NTTR: Nellis or Creech
- [ ] Set to **cold and dark** spawn (not ramp start / hot start)
- [ ] Set weather: **good VMC, calm winds or < 10 kts, day**
- [ ] Confirm mouse clickable cockpit controls are functional (hover over battery switch — verify tooltip appears)
- [ ] Confirm HOTAS mapped: throttle axis, pitch/roll, rudder

---

## Part 1 — Cold-and-Dark to Engines Running

Work methodically through each switch. Announce each action aloud during training: *"Battery — ON."*

### Phase 1A: Electrical & Warning Lights

| Step | Switch | Location | Click Action | Indication |
|---|---|---|---|---|
| 1 | **Battery Switch** | Left console — Electrical Panel | Left-click → ON | Cockpit begins powering; some caution lights illuminate |
| 2 | **Inverter Switch** | Left console — Electrical Panel | Left-click → STBY | AC instruments begin receiving power |
| 3 | **Warning Light Test** | Left glareshield / UFC area | Left-click and hold | All caution/warning lights illuminate; verify none burned out |
| 4 | Release warning light test | — | Release | Only actual faults remain |

> **Instructor Note:** A completely dark cockpit is normal before battery ON. If lights flicker or instruments don't power after battery ON, check the Battery switch is in the ON position (click again if needed).

### Phase 1B: APU Start

| Step | Switch | Location | Click Action | Indication |
|---|---|---|---|---|
| 5 | **APU Switch** | Left console — Electrical Panel | Left-click → START | APU begins spooling; listen for turbine whine |
| 6 | Wait for APU stabilization | — | — | APU RPM stable; APU GEN available |
| 7 | **APU Generator Switch** | Left console — Electrical Panel | Left-click → PWR | Buses fully powered; most caution lights clear |

### Phase 1C: Left Engine Start

| Step | Switch / Action | Location | Indication |
|---|---|---|---|
| 8 | **Left Throttle** — confirm at IDLE (full aft, before CUTOFF) | Throttle quadrant | Throttle in IDLE detent |
| 9 | **Left Engine Operate Switch** — IGN | Left console — Engine Panel | Starter engages; N2 begins rising |
| 10 | Monitor **Left N2** on engine gauge | Right instrument panel (lower) | N2 % rising from 0 |
| 11 | At **~12–15% N2** — advance **Left Throttle** from CUTOFF to IDLE | Throttle quadrant | Throttle moves past CUTOFF detent; fuel introduced |
| 12 | Monitor **Left ITT** | Right instrument panel (lower) | ITT rises sharply → peaks → stabilizes; **must NOT exceed 860°C** |
| 13 | Monitor **Left N1** accelerating through 30%, 50%, 60%... | Right instrument panel (lower) | N1 rising steadily |
| 14 | Engine stabilizes at idle | — | N1: 62–65%; ITT: 400–500°C; Oil: 25–65 PSI; Fuel Flow: 600–800 lbs/hr |
| 15 | **Left Engine Operate Switch** — NORM | Left console — Engine Panel | Returns to normal operating mode |

> **Hot Start:** If ITT reaches 860°C and continues rising — **immediately** pull left throttle to CUTOFF. Switch Engine Operate to MOTOR. Allow 30-second dry crank to cool. Retry.

### Phase 1D: Right Engine Start

Repeat the left engine start procedure for the right engine:

| Step | Action | Same As Left? |
|---|---|---|
| 16 | Confirm Right Throttle at IDLE | Yes |
| 17 | Right Engine Operate Switch — IGN | Mirror of left |
| 18 | Monitor N2; introduce fuel at ~12–15% N2 | Yes — same criteria |
| 19 | Monitor ITT; engine stabilizes at idle | Yes — same parameters |
| 20 | Right Engine Operate Switch — NORM | Yes |

### Phase 1E: Generators & APU Shutdown

| Step | Switch | Location | Click Action | Indication |
|---|---|---|---|---|
| 21 | **Left Generator Switch** | Left console — Electrical Panel | Left-click → PWR | Left generator online |
| 22 | **Right Generator Switch** | Left console — Electrical Panel | Left-click → PWR | Right generator online |
| 23 | Verify both generators stable | — | — | No GEN caution lights |
| 24 | **APU Generator Switch** | Left console — Electrical Panel | Left-click → OFF | APU generator off bus |
| 25 | **APU Switch** | Left console — Electrical Panel | Left-click → OFF | APU spools down |

### Phase 1F: Post-Start Checks

| Check | Requirement |
|---|---|
| Hydraulic A pressure | 3,000 PSI ±200 (right instrument panel) |
| Hydraulic B pressure | 3,000 PSI ±200 (right instrument panel) |
| Flight control check | Full stick and rudder deflection — controls move freely |
| Speed brake check | Open then close — verify extension/retraction |
| Flap check | Cycle MVR → UP — verify movement |
| Caution/warning panel | All faults cleared (or only expected items) |
| Anti-Skid | ON (left console) |
| Oxygen Supply | ON, 100%, NORMAL (right console — cosmetic in DCS) |

---

## Part 2 — Avionics Power-On

Power avionics in this sequence. Starting CDU and EGI early maximizes alignment time.

| Step | System | Switch / Action | Location | Warm-Up |
|---|---|---|---|---|
| 1 | **CDU** | CDU Power knob — ON (rotate clockwise) | Right console, forward | ~30 sec self-test |
| 2 | **EGI / NAV** | Via CDU — press `NAV` page; EGI powers on with CDU in DCS | CDU display | 3–5 min alignment begins |
| 3 | **UFC** | Powers on with avionics bus (battery/APU earlier) | Glareshield center | Verify display active |
| 4 | **Left MFCD** | Brightness knob — rotate clockwise past OFF detent | Left MFCD bezel (lower-left) | ~5 sec self-test |
| 5 | **Right MFCD** | Brightness knob — rotate clockwise past OFF detent | Right MFCD bezel (lower-left) | ~5 sec self-test |
| 6 | **TGP** | AHCP TGP switch — STBY | Left glareshield — AHCP | 3–5 min IR cooling (power early) |
| 7 | **HMCS** | AHCP HMCS switch — ON (if A-10C II) | Left glareshield — AHCP | Immediate; boresight later |
| 8 | **IFFCC** | AHCP IFFCC switch — TEST, then ON | Left glareshield — AHCP | ~10 sec self-test |
| 9 | **CMSP** | CMSP switch — STBY, then MAN | Left console — CMSP Panel | Immediate |
| 10 | **IFF** | Via UFC: enter Mode 3/C codes | UFC keypad | Per mission brief |
| 11 | **Radios** | Via UFC: COM1 (UHF) and COM2 (VHF) frequencies | UFC keypad | Per mission brief |
| 12 | **Pitot Heat** | Pitot Heat switch — ON | Left console — ECS Panel | Always ON before flight |
| 13 | **Anti-Ice** | Engine Anti-Ice — ON if temp < 10°C / IMC | Left console — ECS Panel | As conditions require |

> **Master Arm:** Verify SAFE on AHCP. **Master Arm is ALWAYS SAFE during BQT** — there is no weapons employment in this course. Leaving Master Arm in ARM is a training violation.

---

## Part 3 — EGI Alignment

EGI alignment is **mandatory** before taxi. Moving the aircraft during alignment degrades accuracy.

### Full GC (Gyrocompass) Alignment

| Step | Action | Indication |
|---|---|---|
| 1 | CDU powered ON; NAV page active | CDU displays alignment status |
| 2 | Aircraft **stationary** — do not move during alignment | Movement degrades INS quality |
| 3 | CDU shows alignment quality progressing | Alignment quality number decreasing (lower = better) |
| 4 | CDU shows **"NAV"** or alignment complete indication | EGI aligned — GPS augmented position valid |
| 5 | Verify GPS status: GPS OK, satellites tracked | CDU NAV page shows GPS source valid |

**Alignment takes 3–5 minutes in DCS.** Use this time to complete the avionics setup checklist and brief the mission.

> *⚠ Realism Divergence: Real-world full GC alignment takes 4–8 minutes and is sensitive to vibration. DCS compresses alignment time and does not model INS drift — once aligned, position accuracy is maintained indefinitely. In reality, periodic TACAN cross-checks or GPS updates are required to correct INS drift over time.*

### Verifying Alignment Quality

- CDU NAV page alignment quality number: **≤ 1.0 is adequate** for navigation.
- GPS OK indication: GPS is augmenting the INS — position is reliable.
- Do not taxi until **NAV READY** (or equivalent DCS indication that alignment is complete).

---

## Part 4 — Pre-Taxi Checks

Perform at parking position before releasing brakes.

| Check | Required State | How to Verify |
|---|---|---|
| **SAS Channels** | All three ON (Pitch, Yaw, Roll) | SAS panel — all switches UP/ON; no SAS caution lights |
| **EAC** | ARM | SAS panel — EAC switch to ARM position |
| **Trim** | Neutral (0° pitch, 0° roll, 0° yaw) | Trim indicator on instrument panel |
| **Flaps** | UP for taxi | Flap switch on left console |
| **Speed Brakes** | CLOSED | No SPEED BRAKE caution |
| **EGI** | NAV READY / aligned | CDU NAV page |
| **Altimeter** | Set to field QNH | Kollsman window — match ATIS or tower |
| **Canopy** | CLOSED AND LOCKED | Canopy handle fully forward; CANOPY light out |
| **NWS** | Ready to engage HI | Will press NWS button after brake release |
| **Master Arm** | SAFE | AHCP — always SAFE in BQT |

---

## Part 5 — Taxi

### NWS Modes

| Mode | Engagement | Authority | Use |
|---|---|---|---|
| **NWS HI** | Press NWS button on stick (or `A` key) | ±60° nosewheel deflection | Ramp maneuvering, parking, tight turns |
| **NWS LO** | Press NWS button again to toggle | ±15° nosewheel deflection | Taxiway, runway alignment, takeoff roll |
| **NWS OFF** | Paddle switch or auto at weight-off-wheels | Rudder only | Flight operations |

### Taxi Procedure

| Step | Action | Notes |
|---|---|---|
| 1 | **Parking Brake** — RELEASE (`W`) | Left console or keyboard |
| 2 | **NWS HI** — ENGAGE (NWS button on stick) | HI for ramp; switch to LO on taxiway |
| 3 | Advance throttles slightly above idle | A-10C is heavy — needs brief power to start rolling |
| 4 | **Brake check** within first 50 ft of rolling | Verify both sides decelerate; anti-skid functioning |
| 5 | **NWS LO** — switch when on taxiway | More stable at taxi speed |
| 6 | Maintain **10–15 kts** on straight taxiway; **< 10 kts** in turns | Standard USAF taxi limits |
| 7 | Use **differential braking** for tight turns if needed | `Q` left brake / `E` right brake (or toe brakes) |
| 8 | Monitor for other aircraft, ground vehicles | DCS multiplayer: check for traffic |

### Taxi Speed Reference

| Area | Max Speed |
|---|---|
| Ramp / Parking | 10 kts |
| Taxiway (straight) | 25 kts |
| Taxiway (turns) | 10 kts |
| Congested / blind corner | 5 kts |

> **NWS Tip:** NWS LO is the correct mode for taxiway use. NWS HI is sensitive and easy to over-control at taxi speeds — it will cause oscillating S-turns. Switch to HI only for tight ramp maneuvering and parking.

---

## Part 6 — Pre-Takeoff Checks

Performed at the runway hold-short. Student reads challenge; confirms each item.

| Challenge | Required State |
|---|---|
| **SAS** | All channels — ON (Pitch, Yaw, Roll confirmed) |
| **EAC** | ARM |
| **TRIM** | SET — pitch/roll/yaw at takeoff position (neutral) |
| **FLAPS** | MVR (7°) — confirm on flap indicator |
| **SPEED BRAKES** | CLOSED |
| **EGI / NAV** | ALIGNED — NAV READY on CDU |
| **ALTIMETER** | SET — QNH in Kollsman window |
| **CANOPY** | CLOSED AND LOCKED — CANOPY light OUT |
| **SEAT** | ARMED — SEAT NOT ARMED light OUT |
| **PITOT HEAT** | ON |
| **FUEL** | Checked — sufficient for sortie |
| **CAUTION PANEL** | CLEAR — no unresolved cautions |
| **NWS** | LO — for takeoff roll |
| **MASTER ARM** | SAFE |
| **LIGHTS** | Landing light ON; anti-collision ON |
| **IFF/TRANSPONDER** | SET per ATC |

---

## Part 7 — Shutdown

After returning to parking, perform the complete shutdown.

### Avionics Power-Down (Reverse of Power-On)

| Step | System | Action |
|---|---|---|
| 1 | **CMSP** | OFF |
| 2 | **HMCS** | OFF |
| 3 | **TGP** | OFF (AHCP TGP — OFF) |
| 4 | **IFFCC** | OFF |
| 5 | **Master Arm** | Verify SAFE |
| 6 | **IFF** | STBY or OFF |
| 7 | **Right MFCD** | Brightness knob fully counterclockwise to OFF |
| 8 | **Left MFCD** | Brightness knob fully counterclockwise to OFF |
| 9 | **CDU** | Power OFF |
| 10 | **Exterior Lights** | All OFF |
| 11 | **Cockpit Lights** | All OFF |
| 12 | **Pitot Heat** | OFF |

### Engine Shutdown

| Step | Action | Notes |
|---|---|---|
| 13 | **Parking Brake** — SET | Before any shutdown |
| 14 | Left throttle — IDLE (hold ~30 sec for cool-down) | Allow ITT to stabilize |
| 15 | Left throttle — **CUTOFF** (pull through IDLE detent) | Fuel cut; N1 and ITT begin decaying |
| 16 | Monitor Left N1 spool-down | Allow to reach < 20% before completing shutdown |
| 17 | Right throttle — IDLE (hold ~30 sec) | Same cool-down procedure |
| 18 | Right throttle — **CUTOFF** | Fuel cut |
| 19 | Monitor Right N1 spool-down | Both engines winding down |

### Electrical Shutdown

| Step | Switch | Action |
|---|---|---|
| 20 | Left Generator | OFF |
| 21 | Right Generator | OFF |
| 22 | Inverter | OFF |
| 23 | Oxygen | OFF (right console) |
| 24 | **Battery** | **OFF** — cockpit goes dark; cold-and-dark complete |

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Engine start | No ITT overtemp; all engines reach stable idle |
| Start sequence | Correct fuel introduction timing (12–15% N2) |
| Post-start checks | Hydraulic pressure, flight controls, warnings — all verified |
| Avionics sequence | All systems powered on in correct order |
| EGI alignment | NAV READY before taxi |
| Taxi technique | Remains on taxiway; correct NWS mode for each phase |
| Taxi speed | ≤ 25 kts straight; ≤ 10 kts in turns |
| Pre-takeoff | All items verified without omission |
| Shutdown | Complete cold-and-dark; no electrical or fire risk items left active |

---

## Common Errors

| Error | Correction |
|---|---|
| Introducing fuel before 12% N2 | Wait for N2 — premature fuel causes hot starts. Watch the gauge, not the clock. |
| Not switching Engine Operate back to NORM after start | Leaving in IGN is incorrect procedure. Include NORM switch in the start flow. |
| Forgetting to power MFCDs (brightness knob) | MFCDs are OFF by default. Brightness knob must physically be rotated. Include in avionics flow. |
| Taxiing before EGI alignment completes | Movement degrades alignment. Plan start timing to allow 3–5 min before taxi. |
| NWS HI on taxiway — oscillating S-turns | Switch to NWS LO on the taxiway. HI is for ramp only. |
| Skipping brake check after rolling | Mandatory within first 50 ft. Teaches the habit; catches brake failures before they matter. |
| Forgetting pitot heat | Always ON before flight. Build it into the avionics flow — never leave without it. |
| Not setting altimeter QNH | Wrong altimeter = wrong altitude. Drill: altimeter is checked every pre-takeoff, every time. |

---

[← Event 1: Academics](event-1-academics.md) | [→ Event 3: Familiarization Flight 1](event-3-fam-1.md)

---

*Based on T.O. 1A-10C-1, AFMAN 11-2A-10C Vol 3, and Eagle Dynamics DCS A-10C documentation. For simulation use only.*
