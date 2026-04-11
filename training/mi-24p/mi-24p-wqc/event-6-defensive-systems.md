# Event 6 — Defensive Systems: SPO-15 RWR & UV-26 Countermeasures

> **Course:** Mi-24P Hind Weapons Qualification Course | **Event Type:** Ground/Sim
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [SPO-15 RWR System](#spo-15-rwr-system)
4. [Threat Library](#threat-library)
5. [RWR Limitations](#rwr-limitations)
6. [UV-26 Countermeasures System](#uv-26-countermeasures-system)
7. [Chaff vs. Flares](#chaff-vs-flares)
8. [Employment Techniques](#employment-techniques)
9. [Threat-Specific Procedures](#threat-specific-procedures)
10. [In-Sim Procedures](#in-sim-procedures)
11. [Common Errors](#common-errors)
12. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Power on, test, and operate the SPO-15 RWR from the WSO seat
- [ ] Identify ≥8 threat system symbols and their corresponding audio warnings
- [ ] Describe the MANPADS blind spot and its tactical implications
- [ ] State the correct countermeasures type (chaff or flare) for 6 different threat types
- [ ] Execute the correct UV-26 program for a radar SAM threat
- [ ] Execute the correct UV-26 program for a MANPADS/IR threat
- [ ] Coordinate standard threat call format from WSO to pilot
- [ ] Integrate countermeasures employment with evasive maneuvering
- [ ] Manage countermeasures ammunition throughout a simulated mission

---

## Ground Brief

### The Threat Environment

The Mi-24P is large, loud, and hot — it cannot hide. Survival depends on three layers of defense:

| Layer | Method | Purpose |
|---|---|---|
| **1 — Avoidance** | Route planning, terrain masking, low altitude | Don't be detected |
| **2 — Warning** | SPO-15 RWR | Know when detected/tracked |
| **3 — Defeat** | UV-26 + evasive maneuver | Defeat weapons already in flight |

These systems are only as good as the crew using them. A crew that ignores the RWR or reaches for flares when chaff is needed provides zero protection.

### The Most Important Lesson

**Wrong countermeasures = zero effectiveness.** Chaff does nothing against an IR missile. Flares do nothing against a radar-guided SAM. Before firing any countermeasures, the WSO must identify the threat type.

---

## SPO-15 RWR System

### System Overview

| Parameter | Value |
|---|---|
| **Full Name** | SPO-15 "Beryoza" (Birch Tree) |
| **Type** | Radar Warning Receiver (RWR) |
| **Coverage** | 360° azimuth, ±45° elevation |
| **Frequency Range** | 2–18 GHz (most fire control radars) |
| **Threat Library** | 50+ emitter types |
| **Detection Range** | 25–150 km (depends on emitter power) |
| **Response Time** | <1 second from detection to display |

### Controls (WSO Front Cockpit)

| Control | Function | Positions |
|---|---|---|
| **Master Power** | System on/off | OFF / ON |
| **Mode Selector** | Operating mode | STANDBY / OPERATE / TEST |
| **Brightness** | CRT display brightness | Variable knob |
| **Audio Volume** | Warning tone volume | Variable knob |
| **Priority Reset** | Clears priority threat marker | Momentary button |
| **BIT Switch** | Built-in test | TEST / NORMAL |

> *Note: Some SPO-15 controls in DCS may be mouse-clickable only. Check Mi-24P key bindings for bindable functions.*

### Display Interpretation

| Element | Meaning |
|---|---|
| **Center** | Aircraft position (nose = top of display) |
| **Bearing Scale** | 0–360° in 30° increments |
| **Threat Symbol** | Alphanumeric code for emitter type |
| **Inner Ring** | Closer / stronger signal |
| **Outer Ring** | More distant / weaker signal |
| **Priority Marker** | Highlights highest-priority threat |

### Pilot (Rear Cockpit) Indications

The pilot has **audio warnings only** (via intercom) and a general caution light. He has no display. The WSO is responsible for all threat identification, bearing calls, and recommended responses.

### Audio Warning Tones

| Tone Pattern | Threat Type | Urgency |
|---|---|---|
| **Continuous Low** | Search radar | LOW — monitor |
| **Intermittent Medium** | Tracking radar | MEDIUM — prepare CM |
| **Rapid High Beeps** | Fire control radar | HIGH — immediate action |
| **Warbling Siren** | Missile guidance | EXTREME — emergency evasion |
| **Single Chirp** | New threat acquired | INFO — check display |

---

## Threat Library

### Soviet/Russian SAM Systems

| Symbol | System | NATO Name | Threat Level | Range |
|---|---|---|---|---|
| **10** | S-300P | SA-10 Grumble | EXTREME | 100+ km |
| **11** | 9K37 Buk | SA-11 Gadfly | HIGH | 35 km |
| **6** | 2K12 Kub | SA-6 Gainful | HIGH | 25 km |
| **8** | 9K33 Osa | SA-8 Gecko | HIGH | 15 km |
| **15** | 9K330 Tor | SA-15 Gauntlet | HIGH | 12 km |
| **19** | Tunguska | SA-19 Grison | HIGH | 8 km |
| **13** | Strela-10 | SA-13 Gopher | NONE* | 5 km |

> ***SA-13 is IR-guided — no RWR warning possible.**

### Anti-Aircraft Artillery

| Symbol | System | NATO Name | Threat Level |
|---|---|---|---|
| **S** | ZSU-23-4 | Shilka / Gun Dish | MEDIUM |
| **G** | ZSU-57-2 | Flap Wheel | LOW |

> *Note: Optically-aimed AAA (ZU-23-2, small arms) provides NO RWR warning.*

### Airborne Threats

| Symbol | Type | Threat Level |
|---|---|---|
| **F** | Fighter (MiG-21/23/25/29) | HIGH |
| **I** | Interceptor (MiG-31, Su-27) | HIGH |
| **A** | Attack aircraft | MEDIUM |

### Threat Response Matrix

| Priority | Threats | Response | Time Available |
|---|---|---|---|
| **EXTREME** | SA-10, active missile guidance, fighter FC radar | Terrain masking + CM — immediately | 5–30 seconds |
| **HIGH** | SA-6/8/11/15, ZSU-23-4 | Evasive maneuver + CM | 15–60 seconds |
| **MEDIUM** | Search radars, distant threats | Monitor; plan response | 2–5+ minutes |

---

## RWR Limitations

The SPO-15 is a radar warning receiver — it only detects radar emissions. Understanding what it **cannot** detect is as important as what it can.

### The MANPADS Blind Spot

Most helicopter combat losses occur from IR-guided threats that the RWR cannot detect:

| Threat | Guidance | SPO-15 Warning |
|---|---|---|
| **SA-7 Strela-2** | Infrared | **NONE** |
| **SA-9 Strela-1** | Infrared | **NONE** |
| **SA-13 Strela-10** | Infrared | **NONE** |
| **SA-16 Igla-1** | Infrared | **NONE** |
| **SA-18 Igla** | Infrared | **NONE** |
| **Stinger (FIM-92)** | Infrared | **NONE** |

**Tactical Implication:** Visual scanning for smoke trails and muzzle flashes is mandatory at all times. Low-altitude flight increases MANPADS exposure. The crew cannot rely on the RWR for IR threat warning.

### Other Blind Spots

- **Optically-aimed guns** (ZU-23-2, small arms) — no radar; no warning
- **Limited elevation coverage** — threats directly above or below may not be detected
- **Low-power emitters** — some portable systems below detection threshold
- **Passive IR systems** — no radar emissions; no detectable signal

---

## UV-26 Countermeasures System

### System Overview

| Parameter | Value |
|---|---|
| **Type** | Chaff and flare dispenser |
| **Typical Capacity** | 60+ cartridges |
| **Chaff Type** | RR-129 (radar frequency coverage) |
| **Flare Type** | PPI-26 (IR spectrum) |
| **Dispense Rate** | 1–8 cartridges/second (programmable) |
| **Response Time** | <0.5 seconds |

### Operating Modes

| Mode | Operation | Use When |
|---|---|---|
| **AUTO** | Responds automatically to SPO-15 high-priority threats | Well-defined threat environment |
| **SEMI-AUTO** | Manual initiation; automatic program sequencing | Mixed threat environment |
| **MANUAL** | Complete manual control | Specific technique required; AUTO failed |

### WSO Control Panel

| Control | Function | Settings |
|---|---|---|
| **Program Selector** | Dispense pattern selection | 1/2/3/4/5 |
| **Quantity Select** | Cartridges per burst | 1/2/4/8 |
| **Interval Select** | Time between bursts | 0.5/1.0/2.0/4.0 sec |
| **Chaff Button** | Manual chaff dispense | Momentary |
| **Flare Button** | Manual flare dispense | Momentary |
| **Emergency Dispense** | Dump all stores | Hold 3+ seconds |

### Pre-Programmed Patterns

| Program | Pattern | Application |
|---|---|---|
| **1** | 4 chaff, 0.5 sec intervals | Radar SAM (SA-6/SA-8) launch |
| **2** | 6 flares, continuous | MANPADS/IR launch detection |
| **3** | 2 chaff + 2 flares, 1.0 sec | Unknown or mixed threat |
| **4** | Continuous mixed | Transit through high-threat area |
| **5** | Maximum rate, mixed | Multiple simultaneous threats (emergency) |

---

## Chaff vs. Flares

| Threat | Use Chaff | Use Flares |
|---|---|---|
| **Radar SAM (SA-6/8/11)** | ✓ | ✗ (ineffective) |
| **Radar AAA (ZSU-23-4)** | ✓ | ✗ (ineffective) |
| **Fighter radar missile** | ✓ (+ maneuver) | ✗ (ineffective) |
| **MANPADS (SA-7/16/18)** | ✗ (ineffective) | ✓ |
| **IR air-to-air (R-60/AIM-9)** | ✗ (ineffective) | ✓ |
| **Advanced IR (IRCCM)** | ✗ | ✓ (multiple required) |
| **Optically-aimed AAA** | ✗ | ✗ (maneuver only) |

---

## Employment Techniques

### Technique 1 — Reactive Dispensing

**Application:** Specific threat response
- Trigger: SPO-15 warning or visual missile sighting
- Response: Immediate appropriate CM + evasive maneuver
- Timing: <2 seconds from threat detection to countermeasures

### Technique 2 — Preventive Dispensing

**Application:** High-threat area transit
- Pattern: 1 chaff + 1 flare every 10–15 seconds
- Advantage: Creates protective cloud around aircraft
- Disadvantage: Rapid ammunition consumption
- Use only when threat density justifies expenditure

### Technique 3 — Notching with Chaff

**Application:** Defeating Doppler radar-guided missiles (SA-11, fighter radar AAM)
1. Dispense 4–6 chaff cartridges
2. Hard 90° turn into the chaff cloud (perpendicular to threat bearing)
3. Maintain heading briefly while chaff settles
4. Resume evasive maneuvering

### Technique 4 — Flare Employment with Maneuver

1. Dispense 6–8 flares immediately on IR threat indication
2. Hard turn **away** from heat source (sun, ground)
3. Dive toward cooler background (terrain, shadows)
4. Continue dispensing throughout maneuver
5. Reduce power briefly if tactically feasible (reduces IR signature)

---

## Threat-Specific Procedures

### SA-6/SA-8 Response (Radar SAM)

1. SPO-15 high-priority warning received
2. WSO calls: **"RWR contact, SA-[6/8], bearing [XXX], high priority"**
3. Select Program 1 (4 chaff); dispense immediately
4. Pilot: hard turn + dive toward terrain
5. WSO: continue chaff every 3–4 seconds
6. Monitor SPO-15 for radar lock break
7. Continue terrain masking until threat clears

### MANPADS Response (IR Missile)

1. Visual: missile launch flash or smoke trail
2. WSO calls: **"MISSILE launch, bearing [XXX], dispensing flares"**
3. Select Program 2 (6 flares, continuous)
4. Pilot: hard turn + dive away from threat; maximize terrain use
5. WSO: continue flares until missile impacts/misses
6. Visual confirmation of missile fate

### Extreme Threat (Missile Guidance Detected)

1. Warbling siren from SPO-15
2. WSO calls: **"MISSILE GUIDANCE, bearing [XXX], EXTREME"**
3. Program 5: maximum rate, mixed
4. Pilot: immediate hard break + dive to terrain
5. All other tasks suspended until threat resolved

---

## In-Sim Procedures

### DCS Key Bindings

| Function | Key/Control |
|---|---|
| **SPO-15 Power** | Cockpit click (WSO left panel) |
| **UV-26 Dispense Flare** | `Q` (verify in DCS key bindings) |
| **UV-26 Dispense Chaff** | Assigned or cockpit click |
| **CM Program Select** | Cockpit click — panel switch |
| **CM Mode** | Cockpit click — AUTO/SEMI/MANUAL |

> *Strongly recommend binding chaff and flare to separate HOTAS buttons for rapid threat-appropriate response.*

### Startup / Pre-Mission

1. WSO Seat (`1`)
2. SPO-15 power → **ON**
3. Mode → **OPERATE**
4. BIT test → confirm display active; tones functional
5. UV-26 power → **ON**
6. Mode → **SEMI-AUTO**
7. Program 3 selected (mixed — default transit setting)
8. Call to pilot: "SPO-15 and UV-26 — online, ready"

### Threat Call Standard Format

**WSO to Pilot:** `"RWR contact, [threat type], bearing [XXX], [priority level]"`

Examples:
- "RWR contact, SA-8, bearing 045, high priority"
- "ZSU-23, bearing 270, medium priority"
- "MISSILE GUIDANCE, bearing 090, EXTREME"

### Countermeasures Management

| Phase | Technique |
|---|---|
| **Ingress** | Minimal preventive; save ammunition for target area |
| **Target area** | Reactive only — dispense on actual threat detection |
| **Egress** | Preventive acceptable — survival priority |
| **Emergency** | Use everything available |

Minimum reserve: hold back 10 cartridges for final egress.

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| **Wrong countermeasures type** | Zero effectiveness | Identify threat first; match CM to threat guidance |
| **Too late employment** | Missile inside minimum deflection range | Dispense immediately on detection — no hesitation |
| **Single cartridge instead of burst** | Insufficient decoy density | Use programmed bursts (4–6 minimum) |
| **No maneuver coordination** | Aircraft flies away from CM cloud | Coordinate turn to use CM cloud |
| **Excessive conservation** | Inadequate response to real threats | Better to waste CM than to be hit |
| **No ammunition tracking** | Run out when needed most | WSO monitors count continuously |
| **Panic dispensing** | All CM gone in first engagement | Disciplined, threat-specific employment |
| **Forgetting MANPADS gap** | Surprise IR hit with no warning | Maintain visual scan always; assume MANPADS present |
| **Pilot relying on RWR for IR warning** | No warning before impact | Crew brief: RWR only covers radar threats |

---

## Completion Standards

The student must demonstrate the following to the instructor's satisfaction:

- [ ] Power on and test SPO-15 and UV-26 correctly
- [ ] Identify ≥8 threat symbols by type and priority level (oral)
- [ ] Correctly state MANPADS blind spot and 3 threats that produce no RWR warning
- [ ] Select correct countermeasures type (chaff or flare) for 6 different threats without error
- [ ] Execute standard threat call format correctly in 3 simulated scenarios
- [ ] Execute correct CM program for radar SAM threat with simultaneous maneuver
- [ ] Execute correct CM program for IR missile threat with simultaneous maneuver
- [ ] Complete simulated mission (transit + target + egress) with correct CM employment throughout
- [ ] No CM type errors in any simulated threat scenario

---

*Based on DCS World Mi-24P Hind module by Eagle Dynamics; SPO-15 Beryoza RWR and UV-26 system documentation; Soviet Air Forces defensive systems doctrine. For simulation use only.*
