# Event 8 — Countermeasures & Defensive Systems

> **Course:** OH-58D Kiowa Warrior Weapons Employment Course | **Event Type:** Academic / Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — Countermeasures Dispenser System](#part-1--countermeasures-dispenser-system)
4. [Part 2 — Radar Warning Receiver](#part-2--radar-warning-receiver)
5. [Part 3 — Terrain Masking & Defensive Maneuvering](#part-3--terrain-masking--defensive-maneuvering)
6. [Part 4 — Threat-Specific Defensive Reactions](#part-4--threat-specific-defensive-reactions)
7. [Part 5 — Threat Avoidance in Mission Planning](#part-5--threat-avoidance-in-mission-planning)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Describe the AN/ALE-47 countermeasures dispenser system, including chaff and flare capacity, dispense modes, and HOTAS control requirements
- [ ] Correctly select chaff vs. flares based on the identified threat type (radar vs. IR)
- [ ] Interpret RWR symbology and audio cues: search, track/lock, and launch indications
- [ ] Identify common DCS threat systems by RWR symbol and state the appropriate countermeasure
- [ ] Execute terrain masking as the primary defensive technique, using ridgelines, treelines, and defilade
- [ ] Execute NOE flight (25–50 ft AGL) for threat avoidance
- [ ] Execute break turns and jinking in response to threat indications
- [ ] Apply threat-specific defensive reactions for IR MANPADS, radar SAMs, radar-directed AAA, and optically-aimed weapons
- [ ] Incorporate countermeasures and terrain avoidance into mission route planning

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase 1 | Academic — CM dispenser system, RWR, threat types, CM selection |
| Phase 2 | Simulator — RWR recognition scenarios; threat-specific reaction drills |
| Phase 3 | Flight — NOE flight practice; terrain masking in local training area |
| Phase 4 | Flight — simulated threat environment; practice defensive reactions with CM employment |
| Phase 5 | Shutdown; debrief |

### Key Parameters for This Event

| Item | Value |
|---|---|
| Chaff capacity | ~30 bundles |
| Flare capacity | ~30 cartridges |
| NOE altitude | 25–50 ft AGL |
| Contour flight altitude | 50–100 ft AGL |
| ZSU-23-4 effective range | ~2,500 m (stay > 3,000 m) |
| MANPADS maximum range (typical) | ~5,000 m |
| Jinking pattern interval | Direction/altitude change every 3–5 seconds |
| Break turn bank angle | 45–60° |

---

## Part 1 — Countermeasures Dispenser System

### System Overview

| Parameter | Value |
|-----------|-------|
| **Dispenser Type** | AN/ALE-47 (or equivalent per DCS implementation) |
| **Countermeasure Types** | Chaff (radar decoy) and Flares (IR decoy) |
| **Chaff Capacity** | ~30 bundles (approximate; varies by configuration) |
| **Flare Capacity** | ~30 cartridges (approximate; varies by configuration) |
| **Dispense Modes** | Manual, Semi-Automatic, Programmed |
| **Location** | Dispenser pods on fuselage or tailboom |

### Countermeasure Types

| Type | Purpose | Effective Against | NOT Effective Against |
|------|---------|-------------------|----------------------|
| **Chaff** | Radar decoy — creates false radar returns to break missile lock or confuse tracking | Radar SAMs (SA-6, SA-8, SA-11, SA-15), radar-directed AAA (ZSU-23-4) | IR-guided missiles, optically-aimed weapons, small arms |
| **Flares** | IR decoy — creates a heat source brighter than the aircraft to seduce IR seekers | IR MANPADS (SA-7, SA-14, Igla, Stinger), IR SAMs (SA-9, SA-13), IR AAMs | Radar-guided missiles, AAA, small arms |

### Dispense Modes

| Mode | Operation | Best Use |
|------|-----------|----------|
| **Manual** | Single countermeasure per button press | Precise deployment; maximum conservation |
| **Semi-Automatic** | Pre-programmed burst sequence per button press (e.g., 2 flares + 1 chaff) | Standard defensive response; balance of conservation and effectiveness |
| **Programmed / Auto** | Automatic dispensing on pre-set program or RWR cueing | High-threat areas; when pilot workload prevents manual dispensing |

> **HOTAS Mapping Requirement:** Map chaff and flare dispense buttons to HOTAS before every mission. In a threat reaction there is no time to reach for panel switches. Unbound countermeasures are effectively unavailable in combat. Verify HOTAS bindings during pre-flight.

> *⚠ Realism Divergence: The real AN/ALE-47 supports complex programming with multiple programs, timing sequences, and RWR-cued automatic dispensing. DCS may implement manual and semi-automatic modes only. Full programmability may not be modeled — check current DCS module documentation.*

### Control Panel

| Control | Function |
|---------|----------|
| **CM Mode Switch** | OFF / MAN / SEMI / AUTO |
| **Chaff Button** | Manual chaff dispense (HOTAS-mappable) |
| **Flare Button** | Manual flare dispense (HOTAS-mappable) |
| **Program Select** | Selects pre-set CM program (if implemented) |
| **Jettison** | Emergency jettison of all remaining CM stores |

---

## Part 2 — Radar Warning Receiver

### System Overview

| Parameter | Description |
|-----------|-------------|
| **Display** | Azimuth display showing relative bearing of radar emitters around the aircraft |
| **Symbology** | Threat-type symbols or numeric codes identifying the emitter |
| **Audio** | Tone cues for new contacts, lock-on, and missile launch |
| **Priority** | Prioritizes most dangerous threats (launch > lock > search) |

### RWR Display Elements

| Element | Meaning |
|---------|---------|
| **Symbol at bearing** | A radar emitter detected at that bearing relative to the aircraft nose |
| **Symbol type / number** | Identifies the threat system (see threat table below) |
| **Diamond / highlighted symbol** | Highest-priority threat — currently tracking you |
| **Flashing symbol** | Launch detection — missile is airborne and guiding |

### RWR Audio Cues

| Tone | Meaning | Required Response |
|------|---------|-------------------|
| **New contact tone** (single beep) | New radar emitter detected | Note bearing and type; assess threat level; begin planning |
| **Steady warble / high-priority tone** | Radar transitioning from search to track — you are being locked | Initiate defensive maneuver; dispense chaff; descend to terrain |
| **Launch warning** (rapid, urgent repeating tone) | Missile launch detected | **IMMEDIATE** break + countermeasures + terrain mask |

### Common DCS Threat Systems

| RWR Symbol | System | Type | Countermeasure |
|-----------|--------|------|---------------|
| **2** | SA-2 Guideline | Radar SAM — long range | Chaff + terrain mask + NOE; avoid overflying |
| **3** | SA-3 Goa | Radar SAM — medium range | Chaff + terrain mask |
| **6** | SA-6 Gainful | Radar SAM — mobile, medium range | Chaff + terrain mask + NOE |
| **8** | SA-8 Gecko | Radar SAM — short range, mobile | Chaff + terrain mask; operates within OH-58D engagement zone |
| **11** | SA-11 Gadfly (Buk) | Radar SAM — mobile, medium range | Chaff + terrain mask; extremely dangerous; avoid engagement zone entirely |
| **15** | SA-15 Gauntlet (Tor) | Radar SAM — short range, fast reaction | Chaff + terrain mask; very difficult to defeat once locked |
| **S / 23** | ZSU-23-4 Shilka | Radar-directed AAA | Chaff if radar-directed; terrain mask; standoff > 3,000 m |
| **R** | Early Warning Radar | Search only — no weapon | Indicates enemy knows your general area; expect SAMs and fighters |

---

## Part 3 — Terrain Masking & Defensive Maneuvering

**The OH-58D's primary defense is terrain masking, not countermeasures.** An SA-11 cannot hit what it cannot see. No quantity of chaff or flares replaces being behind a hill.

### Terrain Masking Techniques

| Technique | Description |
|-----------|-------------|
| **Terrain Flight** | Fly at extremely low altitude (NOE: 25–50 ft AGL; contour: 50–100 ft AGL) using terrain features to block line-of-sight from threat |
| **Ridgeline Masking** | Place a ridge or hill between the aircraft and the threat bearing |
| **Treeline / Forest Masking** | Fly behind or within dense treeline; forest blocks visual and many radar LOS |
| **Urban Masking** | Use buildings and structures as LOS blockers in urban environments |
| **Defilade / Hull-Down** | Aircraft body below terrain crest; only MMS visible (hull-down = tactical use; full defilade = survival) |

### NOE Flight

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Altitude** | 25–50 ft AGL | Below treeline; following terrain contours |
| **Airspeed** | 40–80 KIAS | Limited by obstacle avoidance reaction time |
| **Visibility** | Must see terrain features ahead | NVGs essential for night NOE; IMC = do not attempt |
| **Primary Risk** | Wire strike, CFIT | Requires constant terrain awareness; highest-risk flight regime |

> **Instructor Note:** NOE flight is extraordinarily demanding. Students must have mastered basic low-level flight before attempting NOE in a threat environment. In DCS, wire/obstacle hazards are partially modeled but terrain CFIT is fully simulated.

### Break Maneuvers

| Maneuver | Technique | Use Case |
|----------|-----------|----------|
| **Break Turn** | 45–60° bank; pull to accelerate turn rate; descend toward terrain | Generic defensive response; closes with terrain |
| **Diving Break** | Push nose down while banking; trade altitude for speed and rapid descent | When above terrain and need to rapidly descend behind cover |
| **Pedal Turn** (from hover) | Rapid 90–180° pedal turn; present smallest profile; transition to forward flight | From hover; break LOS; initiate escape immediately |
| **Terrain Reversal** | Reverse direction behind a terrain feature; break tracking LOS | When flying along a ridgeline; reverse behind crest |

### Jinking

Random, unpredictable flight path changes to defeat tracking solutions:

- Change heading ±30° every 3–5 seconds
- Change altitude ±50 ft
- Vary airspeed ±20 KIAS
- **Never establish a predictable pattern** — the purpose is randomness
- Most effective against optically-aimed weapons (AAA, MANPADS gunners)
- Less effective against radar tracking systems

### Flare Dispensing During Defensive Maneuver

| Situation | Dispense Pattern | Notes |
|-----------|-----------------|-------|
| IR MANPADS launch detected | 3–5 flares in rapid succession + break turn | Break turn changes the bearing relationship between aircraft and flares |
| Sustained IR threat environment | 1 flare per 2–3 seconds while terrain masking | Conservation secondary to survival; dispense until masked |
| Radar SAM launch detected | 2–3 chaff bundles + break turn + terrain mask | Chaff creates clutter; break changes tracking geometry |
| Threat type unknown | Chaff + flares simultaneously | When uncertain of threat type, dispense both |

---

## Part 4 — Threat-Specific Defensive Reactions

### IR MANPADS (SA-7, SA-14, SA-16/18 Igla, FIM-92 Stinger)

| Phase | Action |
|-------|--------|
| **Detection** | Often no RWR warning — IR MANPADS are passive (no radar). First indication may be launch smoke trail, wingman callout, or impact |
| **Immediate Response** | **FLARES** (3–5 in rapid succession) + break turn into terrain + descend |
| **Sustained** | Continue dispensing flares; terrain mask immediately; NOE flight away from threat |
| **Key Point** | MANPADS are launch-and-leave; once you break LOS and defeat the missile, the same shooter cannot immediately re-engage. But a second shooter may |

### Radar SAMs (SA-8 Gecko, SA-11 Gadfly/Buk, SA-15 Gauntlet/Tor)

| Phase | Action |
|-------|--------|
| **RWR — Search** | Note bearing; assess range; plan escape route toward nearest terrain cover |
| **RWR — Track / Lock** | **CHAFF** + break turn; descend to NOE; put terrain between aircraft and threat bearing immediately |
| **RWR — Launch** | **CHAFF** (multiple bursts) + aggressive break turn + terrain mask; dispense continuously until masked |
| **Key Point** | Against modern SAMs (SA-11, SA-15), chaff alone is often insufficient. Terrain masking is essential. Plan routes to avoid radar SAM engagement zones entirely |

### Radar-Directed AAA (ZSU-23-4 Shilka)

| Phase | Action |
|-------|--------|
| **Detection** | RWR shows AAA tracking radar ("S" or "23"); tracer fire may be visible |
| **Immediate Response** | **Jink** + terrain mask; chaff if radar-directed; break away |
| **Key Point** | ZSU-23-4 effective range ~2,500 m. Maintain standoff > 3,000 m when possible. Inside that range: jink aggressively and egress at maximum airspeed |

### Optically-Aimed AAA & Small Arms

| Phase | Action |
|-------|--------|
| **Detection** | Tracer fire, muzzle flashes; NO RWR warning (no radar emission from these threats) |
| **Immediate Response** | **Jink**; increase speed; break away from fire direction; terrain mask |
| **Key Point** | Countermeasures are ineffective against optically-aimed weapons. Speed, jinking, and terrain are the only defenses. Keep moving — never hover in the open near a known threat |

---

## Part 5 — Threat Avoidance in Mission Planning

| Principle | Application |
|-----------|-------------|
| **Route planning** | Plot ingress/egress through terrain-masked corridors; avoid known SAM engagement zones; use rivers, valleys, and ridgelines |
| **Standoff engagement** | Hellfire maximum range (8 km) allows engagement from outside most MANPADS (5 km) and AAA (2.5 km) envelopes |
| **Time-on-target discipline** | Minimize time in any area within threat engagement zones; rapid engagement cycles; hull-down when possible |
| **Altitude management** | NOE until weapons release; pop up only to engage target; remask immediately after |
| **Mutual support** | Wingman/section provides overwatch during engagement; can suppress or report threats |
| **SEAD coordination** | If SEAD assets are available, coordinate suppression of radar SAMs before entering threat area |
| **Threat ring mapping** | Plot all known threat positions and engagement rings in DCS Mission Editor before flight; mark "no-go" zones on your mental map |

---

## Completion Standards

The student passes this event when they can, without instructor prompting:

- [ ] State the purpose, effective targets, and limitations of chaff vs. flares; correctly identify which to deploy against radar vs. IR threats
- [ ] Demonstrate HOTAS-mapped countermeasure deployment — chaff and flare must be bound and verified before the flight phase begins
- [ ] Correctly interpret 5 RWR symbology and audio scenarios called by the instructor (identify threat type, bearing, and required response)
- [ ] Execute terrain masking within 5 seconds of a simulated threat indication — aircraft must be behind terrain cover or below visible crest line before 5 seconds elapsed
- [ ] Execute NOE flight (25–50 ft AGL) for a minimum of 3 minutes with no altitude busts below 15 ft or above 80 ft AGL
- [ ] Execute correct threat-specific reactions for all four threat types (IR MANPADS, radar SAM, radar AAA, optical AAA) in the simulator or debrief environment
- [ ] Identify and brief a terrain-masked ingress/egress route through a sample threat environment provided by the instructor

---

## Common Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| CM not mapped to HOTAS | Cannot dispense quickly enough during threat reaction; aircraft destroyed | Map chaff and flare to HOTAS before every mission; verify during pre-flight |
| Flares against radar threats (or chaff against IR) | Wrong countermeasure; missile continues to guide | Identify threat type from RWR (radar) or visual signature (IR launch trail); match countermeasure to threat |
| Flying above terrain in known threat areas | Visible to radar and visual observation; easy target | Maintain NOE/terrain-masked flight in threat areas; only unmask to engage |
| Predictable jinking pattern | Enemy tracks the pattern and anticipates future position | Randomize every parameter (heading, altitude, speed); no rhythm |
| Ignoring RWR new-contact tones | Surprised by lock-on or launch with no time to react | Acknowledge every RWR contact; assess type and bearing; plan escape route immediately |
| Hovering in the open near known threats | Stationary, fully exposed target; easy kill | Never hover in the open in a threat area; always have terrain cover within 5 seconds of flight |
| No pre-planned escape routes | When threatened, no immediate decision; wasted reaction time | Brief escape routes before entering engagement area; know the nearest cover at all times |
| Waiting too long to dispense | Missile is inside minimum decoying distance when CM finally deployed | Dispense immediately upon launch indication; wasted CM is preferable to a hit |

---

*Based on TM 1-1520-248-10, FM 3-04.140, ATP 3-04.1, Polychop Simulations DCS OH-58D documentation. For simulation use only.*
