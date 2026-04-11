# Event 5 — Basic Navigation

> **Course:** Mi-24P Hind Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [In-Sim Procedures](#in-sim-procedures)
4. [Completion Standards](#completion-standards)
5. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Use the DISS-15 Doppler navigator to determine ground speed and drift angle
- [ ] Tune the ARK-15 ADF to an NDB station and track inbound and outbound
- [ ] Use the RSBN system to navigate to a beacon
- [ ] Interpret the HSI (Horizontal Situation Indicator) for course deviation and bearing
- [ ] Use the A-037 radar altimeter as a terrain reference during low-altitude operations
- [ ] Navigate a simple cross-country route using at least two nav systems
- [ ] Conduct a basic radio call on the R-863 UHF and R-828 VHF/FM radios

---

## Ground Brief

### The Mi-24P Nav Suite

The Mi-24P uses **Soviet-era navigation systems** that are different from Western GPS/INS platforms. None of them provide a moving map in the Western sense. Navigation is procedural and systems-based.

| System | Type | What It Provides |
|---|---|---|
| **DISS-15** | Doppler radar | Ground speed + drift angle; input for the navigation computer |
| **ARK-15** | ADF (Automatic Direction Finder) | Bearing to NDB stations; needle points toward the station |
| **RSBN** | Radio navigation (Soviet TACAN) | Distance and bearing to RSBN ground beacons |
| **HSI** | Cockpit display | Combines magnetic heading, course deviation, bearing indicator |
| **A-037** | Radar altimeter | Height above terrain (AGL) up to 750 m |
| **R-863 UHF** | Radio | Air-to-ground, ATC communications |
| **R-828 VHF/FM** | Radio | Team communications; FM |

> *Note: The Mi-24P does not have GPS. All navigation is done by these Soviet systems. DCS provides the F10 map as a planning tool — this is acceptable for mission planning but should not substitute for cockpit navigation during exercises.*

### ARK-15 ADF — How It Works

The ARK-15 is a compass that points toward a radio beacon (NDB — Non-Directional Beacon). It operates in the low/medium frequency band.

- **RMI needle (or ADF indicator)** points toward the station
- **Track inbound:** Keep needle on the nose (0° bearing relative) — heading toward station
- **Track outbound:** Keep needle on the tail (180° bearing relative) — heading away from station
- **Cross-wind correction:** The needle will deflect; correct heading until needle returns to nose/tail

### RSBN — Soviet Navigation Beacon System

RSBN beacons operate similarly to Western TACAN or VOR/DME:
- Provides **bearing** to the beacon
- Provides **distance** (DME equivalent) to the beacon
- HSI can display the RSBN course deviation

### DISS-15 Doppler

The DISS-15 measures ground speed and drift angle using Doppler radar returns from the ground. It feeds data to the navigation computer. In DCS:
- Requires warm-up (3–5 min after power on)
- Provides ground speed readout
- Works best when airborne and level; may be unreliable at hover or very slow speed

### Radar Altimeter (A-037)

The A-037 is different from the barometric altimeter:

| Barometric Altimeter | Radar Altimeter |
|---|---|
| Reads altitude above sea level or field elevation (MSL or QFE) | Reads height directly above terrain (AGL) |
| Affected by QNH/QFE setting | Independent of pressure setting |
| Accurate anywhere | Accurate only when terrain is flat below the aircraft |
| No terrain awareness | Direct terrain clearance indication |

The A-037 has a **decision height bug** — set it to the minimum safe altitude and an audio/visual alert triggers if you descend below it.

---

## In-Sim Procedures

### Exercise 1 — System Check and Warm-Up (Pre-Flight)

From startup (assume Event 2 startup procedure complete):

| Step | Action | Notes |
|---|---|---|
| 1 | **DISS-15** — ON | Allow 3–5 min warm-up |
| 2 | **ARK-15** — ON | Allow 2–3 min warm-up; tune to an NDB frequency |
| 3 | **RSBN** — ON | Allow 5–7 min warm-up; tune to nearest RSBN beacon |
| 4 | **A-037** — ON | Set decision height bug to 50 m |
| 5 | **R-863** — check frequency | Confirm on ATC frequency |
| 6 | Verify DISS-15 reading ground speed (should read ~0 on ground) | |
| 7 | Verify ARK-15 needle is pointing (has a valid reading if NDB in range) | |

### Exercise 2 — ADF Tracking (ARK-15)

Plan: Take off and fly to an NDB station using the ARK-15.

| Step | Action | Notes |
|---|---|---|
| 1 | Take off — running takeoff; climb to 300 m | Cruise at 180 km/h |
| 2 | Tune ARK-15 to the briefed NDB frequency | |
| 3 | Note ARK-15 / RMI needle position | Needle points toward station |
| 4 | **Turn toward the needle** | Heading toward station |
| 5 | Track inbound: needle at 0° bearing (station on the nose) | |
| 6 | **Wind correction:** If needle drifts, add correction to bring it back | Technique: "bracket and bisect" |
| 7 | Fly over the station — needle swings to 180° | Station passage confirmed |
| 8 | **Track outbound:** Maintain needle at 180° (station on tail) | Hold heading or correct for wind |
| 9 | Continue outbound for 3 minutes | |
| 10 | Turn back inbound — re-intercept and track to station | Repeat the process |

### Exercise 3 — RSBN Navigation

| Step | Action | Notes |
|---|---|---|
| 1 | Tune RSBN to the briefed beacon | Enter beacon identifier/channel |
| 2 | Read range on DME indicator | Distance to beacon in km |
| 3 | Read bearing on HSI (RSBN course pointer) | Bearing to beacon |
| 4 | Turn to track toward beacon | Heading = bearing to beacon |
| 5 | Track inbound monitoring range | Range decreases as you approach |
| 6 | Pass overhead beacon — range at minimum | |
| 7 | Outbound: Turn to a new heading; note bearing from station | |

### Exercise 4 — Radar Altimeter Operations

| Step | Action | Notes |
|---|---|---|
| 1 | Descend to 100 m AGL (use terrain for reference) | |
| 2 | Compare radar altimeter reading to barometric altimeter | Radar reads AGL; baro reads AMSL |
| 3 | Set decision height bug to 50 m | |
| 4 | Descend to 60 m — note how close to the alert level | |
| 5 | Do not descend below 50 m during exercise | |
| 6 | Climb back to 300 m | The A-037 is for terrain reference — use it |

### Exercise 5 — Cross-Country Navigation Profile

A complete navigation sortie linking all systems. Instructor briefs the route.

**Sample route (3 legs):**

| Leg | From | To | Method | Altitude | Airspeed |
|---|---|---|---|---|---|
| 1 | Home airfield | NDB Alpha | ARK-15 inbound | 300 m | 180 km/h |
| 2 | NDB Alpha | RSBN Beacon | RSBN | 400 m | 200 km/h |
| 3 | RSBN Beacon | Home airfield | ARK-15 inbound / visual | 200 m | 180 km/h |

**For each leg:**
1. Before departure: brief heading, expected time en route, fuel required
2. In flight: use primary nav system; cross-check with secondary
3. Note any cross-wind corrections required
4. Report position at each waypoint
5. Arrival: set up for traffic pattern

### Exercise 6 — Radio Calls

Practice standard radio calls during the navigation sortie:

| Call | When | Format |
|---|---|---|
| **Departure call** | Before takeoff | "Tower, [callsign], Runway [X], requesting takeoff" |
| **Position report** | At each waypoint | "[Callsign], position [waypoint], altitude [X] meters, estimating [next waypoint] in [X] minutes" |
| **Inbound call** | 5 km from airfield | "[Callsign] inbound with [ATIS or conditions], request landing" |
| **Go-around call** | If go-around required | "[Callsign] going around" |

> *DCS Note: Radio calls in DCS multiplayer use actual voice comms (SRS is recommended). In single-player, use the \[ \] communications menu for ATC interaction.*

---

## Completion Standards

| Standard | Requirement |
|---|---|
| **ARK-15 tracking** | Successfully tracks inbound to station; needle within ±10° during tracking |
| **Station passage** | Correctly identifies needle swing as station passage |
| **RSBN** | Reads range and bearing correctly; tracks toward beacon |
| **Radar altimeter** | Correctly reads AGL height; correctly interprets difference from barometric alt |
| **Cross-country** | Completes all 3 legs; arrives at home airfield within ±2 km of direct route |
| **Radio calls** | Makes all required calls in correct format |
| **Wind correction** | Demonstrates at least one wind correction technique during tracking |

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| Chasing the ADF needle | Constant heading oscillations; never tracks a stable course | "Don't steer to the needle — steer to the station. If the needle is left, turn left — then stop and hold" |
| Confusing barometric and radar altimeter | Terrain clearance errors | "Baro = above sea level. Radar = above the ground right now. Below 200 m, the radar altimeter is truth" |
| Not warming up DISS-15 before flight | Unreliable ground speed data | "Avionics on, wait 5 minutes. DISS-15 is not instant-on" |
| Forgetting RSBN warm-up | System shows invalid data | "Same principle — give nav systems time. Rushed alignment = useless data" |
| Not monitoring altitude while navigating | Altitude deviations while "heads-in" | "Heads-in is heads-in-the-cockpit, not heads-in-the-nav-panel. Scan: altitude → nav → altitude" |

---

*Based on Mi-24P RLE, Soviet navigation system documentation, and Eagle Dynamics DCS World Mi-24P Hind module documentation. For simulation use only.*
