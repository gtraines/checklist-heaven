# Su-25T Surface Attack Course

> **Course:** Su-25T Surface Attack | **Aircraft:** Su-25T Frogfoot | **Target:** DCS World
>
> [← Back to Index](../index.md)

---

## Table of Contents

1. [Course Overview](#course-overview)
2. [Platform Employment Notes](#platform-employment-notes)
3. [Phase 1: Basic Surface Attack](#phase-1-basic-surface-attack)
4. [Phase 2: Intermediate Surface Attack](#phase-2-intermediate-surface-attack)
5. [Phase 3: CAS & JTAC Coordination](#phase-3-cas--jtac-coordination)
6. [Phase 4: Airborne FAC-A](#phase-4-airborne-fac-a)
7. [Mission Editor Setup](#mission-editor-setup)
8. [References & Realism Notes](#references--realism-notes)

---

## Course Overview

Single-type syllabus that mirrors the four phases of the general Surface Attack Course, tailored exclusively to Su-25T systems, envelopes, and survivability limits.

**Prerequisites**
- Su-25T basic qualification (startup/taxi/takeoff/landing).
- Radio communications and brevity familiarity (see [Radio Communications](./radio-communications.md)).
- Loadout configuration and countermeasure programming (flares only; no chaff).

**Course Flow**

| Phase | Focus | Weapons & Sensors |
| :---: | :--- | :--- |
| 1 | Fundamentals | Gun, S-8/S-13/S-25, FAB/RBK (unguided), safe escape | 
| 2 | Precision & Systems | Shkval/laser, Vikhr, Kh-25ML, Kh-29L/T, KAB-500Kr |
| 3 | CAS & JTAC | 9-Line, talk-on with Shkval cues, keyhole CAS | 
| 4 | FAC-A | Marks with rockets/smoke, single-type control, stack management |

---

## Platform Employment Notes

- **Airframe/handling:** Straight-wing attack jet with sluggish throttle response; plan power changes early. Respect ~6.5–7.0G limits; avoid max-G with airbrake extended near the ground.
- **Stability aids:** Keep SAS dampers ON for deliveries; disengage route/altitude hold before roll-in.
- **HUD & modes:** CCIP/CCRP-like cues; pipper depression shifts with load and pressure altitude—re-verify after rearm. Gun cross/funnel for GSh-30-2.
- **Navigation:** ARK-22 ADF and limited RSBN (map dependent); no INS/datalink. Use mission editor waypoints/beacons for range work.
- **Survivability:** SPO-15 sector RWR only; no MAWS. Flares available, no chaff—beam/terrain mask instead of chaffing. "One pass, haul ass" mindset.
- **Shkval & laser:** Limited slew rate; contrast lock sensitive to sun/weather. Laser duty ~30–35s continuous; cool 30–40s before re-lase. Reliable ranging ~7–8 km on armored targets.
- **Pods:** Mercury LLTV for low-light (keep <4–5G). Fantasmagoria for SEAD cueing to Kh-25MPU/Kh-58 (mission-dependent).

---

## Phase 1: Basic Surface Attack

### Learning Objectives
- [ ] Fly box/tactical patterns with correct IN/OFF brevity.
- [ ] Employ gun and rockets within safe slant range and dive parameters.
- [ ] Deliver unguided bombs with proper frag avoidance and recovery altitudes.
- [ ] Execute safe escape with limited self-protection (flares only).

### Profiles & Parameters
- **High-angle bombs (FAB-250/500):** 20–25° dive from 11–13k ft MSL; release ≥4.5–5.0k ft AGL; 4–5G escape, egress off-axis.
- **Low-angle rockets/gun:** 10–15° dive from 3.0–4.5k ft AGL; cease fire ≥1.5–2.0k ft AGL; slant 1.2–2.5 km (S-8), 1.5–3.0 km (S-13), 1.2–1.8 km (gun).
- **S-25 heavy rocket:** 10–25°; 2.0–4.0 km slant; stabilize before release to manage recoil.

### Setup & Execution
- Stores: 2×B-8 (S-8) or mixed S-8/S-13, 2×FAB-250, full gun; optional SPS-141 jammer if enabled.
- Checks: Dampers ON, Master Arm SAFE until roll-in, pipper depression confirmed after rearm, flare program set.
- Pattern: Standard box for range work; tactical wheel/butterfly for field conditions. Call "IN", release, immediate 4–5G recovery, "OFF" with heading/altitude.

---

## Phase 2: Intermediate Surface Attack

### Learning Objectives
- [ ] Use Shkval to find, lock, and range targets; manage laser cooling.
- [ ] Employ CCRP/CCIP with laser ranging for accuracy.
- [ ] Employ guided ordnance within envelopes without breaking lock.

### Profiles & Parameters
- **Vikhr / Kh-25ML:** 1,500–3,000 m AGL; level or 5–15° shallow dive; keep target within ±20°; lase through TOF.
- **Kh-29L (laser):** 3–10 km; continuous lase; expect heavy post-release handling.
- **Kh-29T / KAB-500Kr (TV):** 3–12 km (Kh-29T), 3–10 km (KAB-500Kr); establish solid TV lock pre-release; maintain stable wings.

### Setup & Execution
- Loadouts: 2–4×Vikhr on twin racks; 2×Kh-25ML or 2×Kh-29T; optional Mercury for night; gun retained.
- Sensor flow: Boresight Shkval, wide FOV to acquire, narrow to refine; cage/uncage practice; re-lase if timer exceeds duty cycle.
- Abort criteria: Laser overtemp, loss of lock, or RWR spike without clearance—call "CONTINUE DRY" and reset.

---

## Phase 3: CAS & JTAC Coordination

### Learning Objectives
- [ ] Execute 9-Line and check-in for a single-type Su-25T flight.
- [ ] Conduct talk-on using Shkval references and visual marks.
- [ ] Apply keyhole CAS geometry and deconfliction with limited self-protection.

### Profiles & Parameters
- Holds 8–12k ft MSL, 10–15 NM IP-to-target. Use rockets/bombs for area targets; Vikhr/Kh-25ML for points.
- Maintain laser discipline while awaiting clearance; keep SPO-15 scan; terrain mask during holds if threats present.

### Setup & Execution
- Loadouts: Mixed S-8 + Vikhr + Kh-25ML; smoke rockets optional for marks; prioritize flare quantity over weight.
- Comms: Standard CAS brevity (TALLY/VISUAL/CONTACT/IN/OFF/CONTINUE DRY/CLEARED HOT).
- Talk-on: Use Shkval narrow FOV landmarks; pass bearing/range/feature; confirm with "CONTACT"/"TALLY" before clearance.

---

## Phase 4: Airborne FAC-A

### Learning Objectives
- [ ] Manage a stack with only SPO-15 sector cues and flares.
- [ ] Mark with rockets/smoke and pass concise target data to single-type shooters.
- [ ] Enforce "one pass" survivability mindset for low self-protection aircraft.

### Profiles & Parameters
- Holds 10–15k ft MSL, offset 3–5 NM. Pop to mark, then immediate egress; re-attack only when threat picture permits.

### Setup & Execution
- Loadouts: Smoke rockets or S-8 for marking, limited Vikhr/Kh-25 for self-escort, gun. Keep fuel light for handling.
- Control: Use bearing/range/landmark references from Shkval view; no datalink available. Issue "CLEARED HOT" / "CONTINUE DRY" explicitly.
- Threat reactions: Pre-brief jink directions; beam and terrain mask (no chaff). Do not loiter inside MANPADS/SHORAD WEZ.

---

## Mission Editor Setup

- **Start conditions:** Provide cold start at base and hot start near range/FOB. Enable ground power for quick power-up (no INS alignment needed).
- **Patterns:** Mark box lanes (~5×3 NM) and tactical anchor points (IP, egress, hold) with altitude blocks for altitude deconfliction.
- **Targets by phase:**
  - Phase 1: Truck convoys, soft targets, strafe pits, open bomb circles.
  - Phase 2: Tanks/IFVs for Vikhr, hardened bunkers for Kh-25/29, bridges/ships for heavy aimpoints, radar emitters for SEAD drills.
  - Phase 3: Urban blocks/clutter for talk-ons; JTAC with laser off by default to force pilot marks.
  - Phase 4: FAC-A stack with AI shooters; smoke triggers for marks.
- **Threat templates:** Build from light MANPADS/AAA to SHORAD (Strela/OSA) to medium SAM (Kub/Buk) for SEAD progression. Draw threat rings on map.
- **Maps:** Keep map-agnostic; add RSBN/ADF beacons where available (Caucasus/NTTR examples acceptable).

---

## References & Realism Notes

- DCS Su-25T Flight Manual (Eagle Dynamics).
- MCWP 3-23.1 / JP 3-09.3 CAS doctrine (applied to Su-25T comms/geometry).
- Simulation-specific: Vikhr/SEAD fit more generous than many real-world loadouts; SPO-15 and laser cooling modeled approximately. No chaff—plan beam/terrain masking instead.

*Based on Eagle Dynamics DCS World documentation. For simulation use only.*
