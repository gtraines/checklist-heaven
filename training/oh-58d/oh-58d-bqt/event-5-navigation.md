# Event 5 — Basic Navigation

> **Course:** OH-58D Kiowa Warrior Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Startup & AHRS/GPS Review](#part-1--startup--ahrsgps-review)
5. [Part 2 — Waypoint Navigation Setup](#part-2--waypoint-navigation-setup)
6. [Part 3 — Navigation Flight](#part-3--navigation-flight)
7. [Part 4 — MFD Moving Map Operations](#part-4--mfd-moving-map-operations)
8. [Part 5 — Radar Altimeter Use](#part-5--radar-altimeter-use)
9. [Part 6 — Return and Landing](#part-6--return-and-landing)
10. [Part 7 — Shutdown](#part-7--shutdown)
11. [Completion Standards](#completion-standards)
12. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Enter, modify, and delete waypoints in the AHRS/GPS system
- [ ] Navigate between waypoints using the MFD moving map and HSI heading reference
- [ ] Interpret the MFD navigation page: current waypoint, distance-to-go, bearing, groundspeed
- [ ] Use the radar altimeter to maintain a set AGL altitude with low-level alert set
- [ ] Fly a simple cross-country navigation profile from the departure airfield to two waypoints and return
- [ ] Apply the concept of pilotage (map-to-ground visual reference) as a backup to GPS navigation

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase 1 | Startup, AHRS/GPS alignment, waypoint entry |
| Phase 2 | Departure to Waypoint 1 (WP1) — direct navigation |
| Phase 3 | WP1 to Waypoint 2 (WP2) — with heading change |
| Phase 4 | WP2 to return waypoint / home airfield |
| Phase 5 | Normal approach and landing |
| Phase 6 | Shutdown |

### Key Numbers for This Event

| Item | Value |
|---|---|
| Navigation Airspeed | 80–100 KIAS cruise |
| Navigation Altitude | 1,000–1,500 ft AGL (500 ft AGL min for safety) |
| Radar Altimeter Alert | Set to 300 ft AGL (minimum for this event) |
| AHRS Alignment Required | Full alignment before departure |
| Waypoint Distance (each leg) | 15–25 nm (instructor assigns based on map) |
| Heading Tolerance | ±5° of assigned track |
| Altitude Tolerance | ±100 ft |

---

## Pre-Mission Setup

- [ ] Load DCS OH-58D on a departure airfield
- [ ] Instructor pre-briefs the navigation route: departure airfield → WP1 → WP2 → return
- [ ] Student draws route on paper or notes waypoint coordinates/names
- [ ] Recommended maps:
  - **Caucasus:** PGUA (Tbilisi) → URSS (Sochi) area; or Batumi to Kutaisi
  - **NTTR:** Nellis → Indian Springs → North Las Vegas → Nellis
  - **Persian Gulf:** Al Minhad → Khasab → Dubai
- [ ] Confirm weather: VMC throughout route
- [ ] Confirm HOTAS and mouse functionality

---

## Part 1 — Startup & AHRS/GPS Review

Perform the complete startup. During the AHRS/GPS alignment wait time, review the navigation system:

### AHRS/GPS System Overview

The OH-58D uses a combined **AHRS (Attitude and Heading Reference System) / GPS** unit. The AHRS provides attitude (pitch and roll) and heading derived from solid-state gyroscopes and accelerometers, augmented by GPS for position accuracy.

| Component | Function |
|---|---|
| **AHRS** | Attitude (pitch/roll), magnetic heading, derived vertical speed |
| **GPS** | Position fix (lat/lon), groundspeed, track, time-to-waypoint |
| **MFD** | Primary display for navigation data — moving map, waypoint data, HSI page |

**Navigation Pages on MFD:**
- **Moving Map** — aircraft symbol on a terrain/chart map; waypoints displayed
- **HSI Page** — compass rose with bearing pointer to selected waypoint; cross-track error
- **Waypoint Data** — current waypoint name, distance, bearing, ETE

### MFD Navigation Controls

| Control | Action |
|---|---|
| **WPT button** | Cycles through waypoints |
| **MAP/NAV mode** | Toggles moving map vs. navigation data display |
| **Range +/−** | Zoom level on moving map |
| **Direct-To** | Navigate directly to selected waypoint |

---

## Part 2 — Waypoint Navigation Setup

Before departure, program the route into the AHRS/GPS.

### Entering Waypoints

The exact procedure varies by DCS OH-58D module implementation. General steps:

| Step | Action | Notes |
|---|---|---|
| 1 | Access the **AHRS/GPS controller** (right console) | Power must be on; alignment complete |
| 2 | Select **Waypoint Entry mode** | Per Polychop DCS controls |
| 3 | Enter **WP1 coordinates** (latitude/longitude) or select from preset database | Confirm position appears on MFD |
| 4 | Enter **WP2 coordinates** | Confirm position appears on MFD |
| 5 | Enter **Return/Home waypoint** | Airfield coordinates or pre-programmed |
| 6 | Verify **waypoints displayed on MFD** moving map | Waypoints should appear at correct map locations |
| 7 | Select **WP1** as active waypoint | Bearing pointer on HSI should orient to WP1 |

**Pre-Departure Navigation Check:**
- [ ] All waypoints entered and verified on MFD
- [ ] Active waypoint = WP1
- [ ] HSI bearing pointer oriented toward WP1
- [ ] Distance-to-WP1 displayed and plausible (match against paper plan)
- [ ] AHRS heading agrees with compass rose (± 5°)

---

## Part 3 — Navigation Flight

### Departure to WP1

| Step | Action |
|---|---|
| 1 | Normal takeoff; climb to navigation altitude (1,000–1,500 ft AGL) |
| 2 | Roll out on the initial heading toward WP1 (use HSI bearing pointer) |
| 3 | Establish cruise at 80–100 KIAS |
| 4 | Cross-check: **HSI bearing pointer** (primary direction cue) |
| 5 | Cross-check: **MFD moving map** (confirm track over ground) |
| 6 | Monitor **distance-to-WP** decreasing on MFD data page |
| 7 | Monitor **cross-track error** — am I left or right of the desired track? |
| 8 | Correct cross-track error with heading adjustment (**double the cross-track angle** if < 5 nm from track) |

### Navigation Technique

**Primary Cross-Check (every 30–60 seconds):**
```
HSI bearing pointer → MFD moving map → Distance/ETE → Altitude → Back to horizon
```

**Pilotage Backup (every major waypoint):**
- What should I be able to see on the ground right now?
- Look outside — does the terrain match the map?
- Identify a recognizable feature (river, lake, airfield, town, road)

### WP1 to WP2 — Heading Change

| Step | Action |
|---|---|
| 1 | As WP1 distance decreases to ~2 nm, **pre-calculate turn heading to WP2** | |
| 2 | Select **WP2** as active waypoint | HSI bearing pointer swings to WP2 |
| 3 | Turn to new heading | Roll out on HSI bearing pointer |
| 4 | Cross-check MFD — confirm aircraft tracking toward WP2 | |
| 5 | Continue navigation to WP2 | |

### WP2 to Return

| Step | Action |
|---|---|
| 1 | At WP2, select **Return waypoint** as active | |
| 2 | Turn toward home | |
| 3 | Begin descent planning: 1,500 ft AGL → 1,000 ft AGL → pattern altitude | |
| 4 | Identify the departure airfield visually as you approach | |

---

## Part 4 — MFD Moving Map Operations

### Map Range Changes

Practice zoom in/out to understand what features are visible at each range:

| Range | What is Visible |
|---|---|
| **50 nm** | Regional picture; waypoints, major terrain |
| **25 nm** | Airfields, towns, large terrain features |
| **10 nm** | Local airfields, roads, rivers visible |
| **5 nm** | Fine detail; approach area, specific LZs |

**Standard Navigation Zoom:** 10–25 nm. Zoom in only when examining a specific area.

### Cross-Track Error

The MFD or HSI will indicate if you are left or right of the desired track (cross-track error). A helicopter can often tolerate greater cross-track error than a fighter, but sloppy navigation becomes a significant problem in confined terrain.

**Rule:** If cross-track error is > 0.5 nm, correct heading by **twice the number of degrees of your track error** until back on course, then resume direct bearing.

---

## Part 5 — Radar Altimeter Use

The radar altimeter provides **AGL (Above Ground Level)** altitude — critical for low-level operations. Unlike the barometric altimeter (which reads pressure altitude above sea level), the radar alt reads directly to the terrain below.

### Setting the Radar Altimeter

| Step | Action |
|---|---|
| 1 | Set the **Low Altitude Warning** to **300 ft AGL** for this event (instructor may adjust) |
| 2 | Verify the warning audio/light activates if altitude descends below set threshold |
| 3 | During navigation, monitor radar alt alongside barometric alt |

### When to Use Radar Altimeter vs. Barometric

| Situation | Primary Reference |
|---|---|
| **Low-level navigation (< 500 ft AGL)** | Radar altimeter — terrain clearance is the priority |
| **Approaches and landings** | Radar altimeter — AGL is what matters for obstacle clearance |
| **En route at altitude (> 1,000 ft AGL)** | Barometric — altitude coordination with ATC |
| **Practice autorotation** | Radar altimeter — decision altitude (200–300 ft AGL) |

### Radar Altimeter Exercise

From 1,000 ft AGL cruise, the instructor will ask the student to descend to **500 ft AGL** using the radar altimeter as the primary reference (without looking at the barometric alt). The student must:
- Smoothly descend to 500 ft AGL per radar alt
- Level off exactly at 500 ft AGL
- Hold ±50 ft for 30 seconds
- Return to 1,000 ft AGL

---

## Part 6 — Return and Landing

### Airfield Identification

Before descending for the approach:
- [ ] Identify the airfield on the MFD moving map
- [ ] Visual contact with the airfield
- [ ] Plan the approach: which runway/pad, pattern direction, wind correction

### Normal Approach and Landing

Use the normal decelerating approach from Event 4:
- Enter the pattern at 500–800 ft AGL
- Cruise: 70–80 KIAS downwind
- Decelerate on base and final
- Terminate to hover at landing point
- Set down

---

## Part 7 — Shutdown

Complete shutdown per Event 2 standard.

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Waypoints entered | All waypoints correct and verified before departure |
| Navigation accuracy — track | Within ±1 nm of planned track throughout |
| Navigation accuracy — heading | Within ±5° of required heading to waypoint |
| Navigation accuracy — altitude | ±100 ft of assigned altitude |
| MFD usage | Student actively uses moving map throughout; not just GPS pointer |
| Radar altimeter | Warning altitude set; AGL descent exercise within ±50 ft |
| Waypoint transitions | Active waypoint changed at correct point; no missed turns |
| Return and approach | Field identified visually before GPS lead; normal approach completed |

---

## Common Errors

| Error | Correction |
|---|---|
| **Trusting GPS without looking outside** | "The GPS can be wrong. The map can be wrong. Look outside. What do you see? Does it match?" |
| **Not pre-planning waypoint turns** | "You can't turn on a waypoint you didn't see coming. Start the turn setup 2 nm out." |
| **Flying the bearing pointer without cross-track awareness** | "Following the pointer to the waypoint doesn't mean you're on the planned track. Check the moving map — are you on the line?" |
| **Ignoring radar altimeter at low altitude** | "Below 500 ft, the radar alt is your primary. Set the warning, cross-check continuously." |
| **Not identifying airfield visually before GPS lead** | "You should be able to see your destination before the GPS says you're there. Find it on the map, find it outside." |
| **Skipping pilotage** | "What's under you right now? What's ahead? GPS bugging out — can you navigate without it? Pilotage is not optional." |

---

[→ Proceed to Event 6: Traffic Pattern & Landings](event-6-traffic-pattern.md)

---

*Based on TM 1-1520-248-10, TC 3-04.4, TC 3-04.62, and Eagle Dynamics / Polychop Simulations DCS OH-58D documentation. For simulation use only.*
