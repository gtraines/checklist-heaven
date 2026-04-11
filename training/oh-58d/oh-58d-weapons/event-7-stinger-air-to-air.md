# Event 7 — AIM-92 Stinger Air-to-Air Self-Defense

> **Course:** OH-58D Kiowa Warrior Weapons Employment Course | **Event Type:** Academic / Simulator
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — System Overview](#part-1--system-overview)
4. [Part 2 — Engagement Envelope & Seeker Characteristics](#part-2--engagement-envelope--seeker-characteristics)
5. [Part 3 — Employment Sequence](#part-3--employment-sequence)
6. [Part 4 — Self-Defense Doctrine](#part-4--self-defense-doctrine)
7. [Part 5 — Air Threat Environment in DCS](#part-5--air-threat-environment-in-dcs)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Describe the AIM-92 Stinger ATAS system and its role as an OH-58D self-defense weapon
- [ ] Identify the Stinger engagement envelope (range, aspect, altitude, target speed) and state the optimum firing parameters
- [ ] Execute the Stinger employment sequence (if modeled in DCS) from threat detection through launch
- [ ] Apply the correct defensive priority sequence: terrain mask → countermeasures → Stinger → egress
- [ ] State the ROE for air-to-air self-defense: when to engage vs. when to evade
- [ ] Assess the Stinger's practical effectiveness against DCS air threats by category (helicopters, slow movers, fast jets)
- [ ] Explain why the OH-58D must not attempt to pursue or dogfight air threats

---

## Ground Brief

### Mission Profile

> **DCS Availability Note:** The AIM-92 Stinger may or may not be modeled on the DCS OH-58D depending on the current Polychop module version. Check the loadout screen before flight.
>
> - **If Stinger is available in DCS:** Complete all phases including flight.
> - **If Stinger is not available in DCS:** This event is conducted as an **academic and simulator session only**. The doctrine, threat recognition, and self-defense procedures remain valid and must be learned regardless of weapon availability.

| Phase | Activity |
|---|---|
| Phase 1 | Academic — system data, engagement envelope, seeker operation, ROE |
| Phase 2 | Doctrine brief — defensive priority sequence; threat-by-threat assessment |
| Phase 3 | Simulator/scenario — threat intercept scenarios; practice terrain masking and decision-making |
| Phase 4 | Flight (if Stinger available) — seeker tone familiarization; employment sequence from hover and slow flight |
| Phase 5 | Shutdown; debrief |

### Key Parameters for This Event

| Item | Value |
|---|---|
| Guidance type | Infrared (IR) homing — passive all-aspect |
| Effective range | 500–4,500 m |
| Optimum range | 1,000–3,000 m |
| Minimum range (arming) | ~500 m |
| Seeker acquisition tone | Low growl |
| Seeker lock tone | High-pitched steady tone |
| Warhead | ~3 lb HE blast-fragmentation |
| Missiles per ATAS launcher | 2 |

---

## Part 1 — System Overview

The **AIM-92 Stinger** (Air-to-Air Stinger — ATAS) is an adaptation of the **FIM-92 Stinger MANPADS** for helicopter air-to-air self-defense employment. It is not an offensive weapon — it is a **last-resort self-defense system** carried to provide the OH-58D with a capability against enemy aircraft that prosecute attacks on the helicopter or its formation.

| Parameter | Value |
|-----------|-------|
| **Designation** | AIM-92 Stinger (ATAS) |
| **Guidance** | Infrared (IR) homing — passive all-aspect seeker |
| **Launcher** | ATAS launcher pod — typically 2 missiles per launcher |
| **Mounting** | Universal Weapons Pylon (UWP) — occupies one pylon |
| **Warhead** | ~3 lb HE blast-fragmentation; proximity and contact fuze |
| **Effective Range** | 500 m – 4,500 m |
| **Maximum Speed** | Mach 2+ (supersonic missile) |
| **Seeker** | Dual-band IR (UV + IR) with IRCCM capability; all-aspect |
| **IFF** | Not modeled in DCS; real-world ATAS includes IFF interrogation |

### Pylon Considerations

Loading the ATAS launcher on one UWP removes that pylon from ground ordnance. A pilot who loads Stinger accepts reduced ground attack capability in exchange for air-to-air self-defense. This is a mission planning decision based on the briefed air threat level.

| Left Pylon | Right Pylon | Mission Context |
|-----------|-------------|-----------------|
| M3P .50 cal | ATAS (2× Stinger) | Scout with self-defense; reduced precision ground capability |
| M260 Rockets | ATAS (2× Stinger) | Area suppression with air threat coverage |
| ATAS (2× Stinger) | ATAS (2× Stinger) | Pure air-defense escort; no ground ordnance |

---

## Part 2 — Engagement Envelope & Seeker Characteristics

### Engagement Envelope

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Minimum Range** | ~500 m | Missile arming distance; shots inside this range may not fuze |
| **Maximum Range** | ~4,500 m | Varies with target aspect, speed, and altitude |
| **Optimum Range** | 1,000–3,000 m | Highest Pk (probability of kill) zone |
| **Preferred Aspect** | Rear-aspect (tail-on) | Strongest IR signature; highest Pk; but all-aspect capable |
| **All-Aspect Capable** | Yes (UV + IR dual-band) | Can engage from front, side, or rear hemisphere |
| **Target Speed** | Subsonic and low-supersonic | Effective against helicopters and slow movers; limited against high-speed fighters |
| **Launch Altitude** | Surface to ~15,000 ft MSL | Effective throughout OH-58D operating altitudes |
| **Launch Speed** | 0–120 KIAS | Helicopter forward speed has minimal effect on missile performance |

### Seeker Characteristics

| Feature | Description |
|---------|-------------|
| **Acquisition Growl** | Low growl tone — seeker scanning; detecting IR source but not locked |
| **Lock Tone** | High-pitched steady tone — seeker locked on target; ready to fire |
| **IRCCM** | Dual-band IR resists basic flare decoys better than older single-band seekers |
| **Coolant** | Seeker requires coolant gas; operating time after activation is limited |
| **All-Aspect** | Dual-band allows reliable lock from front, side, and rear hemispheres |

---

## Part 3 — Employment Sequence

> **DCS Availability:** If Stinger is not modeled in the current DCS module version, study this sequence doctrinally. The steps reflect real-world ATAS procedures.

| Step | Action | Indication |
|------|--------|-----------|
| 1 | **Detect threat aircraft** | Visual contact / RWR indication / wingman callout |
| 2 | **Assess threat** | Type, direction, range, aspect — is it engaging you or friendly forces? |
| 3 | **Select Stinger** on weapons page | STG or ATAS displayed on MFD |
| 4 | **Master Arm → ARM** | MASTER ARM annunciated |
| 5 | **Activate seeker (uncage)** | Seeker growl tone begins |
| 6 | **Point aircraft nose at threat** | Seeker requires forward pointing (within gimbal limits) |
| 7 | **Acquire lock** | Tone changes from growl to high-pitched steady lock tone |
| 8 | **Confirm within engagement envelope** | Range 500–4,500 m; aspect and speed acceptable; hostile confirmed |
| 9 | **Fire (pickle)** | Missile launches; smoke trail toward target |
| 10 | **IMMEDIATELY BREAK AND EVADE** | Do NOT wait for BDA; begin defensive maneuvering into terrain immediately |
| 11 | **Dispense countermeasures** | Flares/chaff during break turn |
| 12 | **Terrain mask** | Behind terrain as quickly as possible |
| 13 | **Observe result** (only if safe position achieved) | Report "Splash" or "No joy" |
| 14 | **Re-engage or egress** | Second missile if available and target still threat; or egress |

> **Critical Doctrine:** After firing, **survival is the priority — not BDA.** The OH-58D is a scout, not a fighter. Fire the Stinger and break immediately into terrain. An OH-58D hovering or circling after a Stinger launch is easy prey for the threat aircraft's wingman or any surviving return shot.

---

## Part 4 — Self-Defense Doctrine

### Rules of Engagement

The OH-58D carries Stinger for **self-defense only**. It does not conduct independent air superiority or offensive counter-air missions.

| Situation | Action |
|-----------|--------|
| Enemy helicopter detected; not currently engaging you or friendly forces | **Do NOT engage.** Report position and type to higher command; request fighter CAP |
| Enemy helicopter or aircraft actively attacking you or your formation | **Engage with Stinger** if within envelope; break and evade simultaneously |
| Enemy fixed-wing slow mover (Su-25, L-39) attacking | **Engage** with Stinger if in envelope and you are the target; terrain mask immediately after |
| Enemy fast jet (MiG-29, Su-27, F-4, F-16) | **Do NOT engage** — Stinger is outside practical Pk envelope against fast movers; terrain mask immediately; jettison stores for max performance; call for fighter support |
| Positive identification of target is uncertain | **Do NOT fire** — confirm hostile via radio, visual PID, IFF; fratricide risk |

### Defensive Priority Sequence

When under air attack, execute in this order:

1. **Terrain Mask** — get behind terrain immediately; nap-of-the-earth flight; this is always the first action.
2. **Jettison Stores** — if needed for speed and maneuverability; emergency jettison for maximum performance escape.
3. **Dispense Countermeasures** — flares against IR threats; chaff against radar threats.
4. **Fire Stinger** — if threat is within envelope, confirmed hostile, and actively engaging you.
5. **Call for Help** — "Engaged defensive" on appropriate frequency; request fighter CAP; report type and position of threat.
6. **Egress** — run for friendly territory, FARP, or protected airspace.

> **Instructor Note:** Students instinctively want to fight. Drill into them that the Kiowa is a scout, not a fighter. The Stinger is a last-resort "get off me" weapon. The primary defense is ALWAYS terrain masking and evasion. A prolonged air-to-air engagement in an OH-58D against any enemy aircraft with a gun is nearly always fatal for the Kiowa.

---

## Part 5 — Air Threat Environment in DCS

| Threat | Type | Stinger Effectiveness | Recommended Response |
|--------|------|----------------------|---------------------|
| **Mi-24 Hind** | Attack helicopter | **Good** — large IR signature; two hot engines; relatively slow | Stinger if engaging you; terrain mask simultaneously; be aware of 12.7mm gun range |
| **Ka-50 Black Shark** | Attack helicopter | **Good** — single engine with exposed IR signature | Stinger + terrain mask; be aware of Ka-50's 30mm cannon effective range |
| **Mi-8 Hip** | Transport/armed helicopter | **Good** — large IR signature; slow; vulnerable | Stinger effective; confirm ROE before engaging (may be unarmed transport) |
| **Su-25 Frogfoot** | Ground attack jet | **Moderate** — subsonic; 2× engines; moderate IR; engaging from rear aspect preferred | Stinger when in rear/side aspect and within 3,000 m; terrain mask immediately |
| **L-39 Albatros** | Light attack/trainer jet | **Good** — slow; single engine; vulnerable to Stinger | Stinger effective in most aspects within 3,000 m |
| **MiG-29 / Su-27** | Air superiority fighter | **Poor** — fast; rapidly out of envelope; high closing speed | **Do NOT engage;** terrain mask immediately; jettison stores; call for fighters |
| **F/A-18, F-16 (Friendly)** | Coalition aircraft | **DO NOT ENGAGE** — fratricide | PID before any engagement; confirm hostile on radio before weapon employment |

---

## Completion Standards

The student passes this event when they can, without instructor prompting:

- [ ] State the AIM-92 Stinger engagement envelope (minimum range, maximum range, optimum range, and all-aspect capability)
- [ ] Describe the seeker acquisition tone vs. lock tone and explain the significance of each
- [ ] Execute the employment sequence in correct order from threat detection through fire-and-break (in DCS if available, or on whiteboard/simulator if not)
- [ ] State the defensive priority sequence in correct order: terrain mask → stores jettison → countermeasures → Stinger → call for help → egress
- [ ] Correctly decide whether to engage or evade for each of the following threats called by the instructor: Mi-24, Ka-50, Su-25, MiG-29, unknown fixed-wing
- [ ] Explain why the OH-58D must not pursue or dogfight any air threat after a Stinger launch
- [ ] State the ROE for Stinger employment: self-defense only; hostile confirmation required; fratricide PID requirement

---

## Common Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Attempting to dogfight the enemy aircraft | OH-58D destroyed; not designed for air-to-air maneuvering | Fire Stinger and break immediately; do not pursue; terrain is your wingman |
| Firing without confirmed hostile identification | Fratricide — shooting down friendly aircraft | Always PID; if uncertain, do not fire; radio confirmation required before employment |
| Waiting to observe BDA after launch | Stationary helicopter is easy target for threat's return shot or wingman | Fire and break immediately; BDA is a secondary concern |
| Ignoring Stinger during mission planning when air threat is briefed | No air-to-air self-defense capability when it is needed | If air threat is assessed as credible, load Stinger on one pylon; brief the loadout tradeoff |
| Engaging fast jets at long range | Missile cannot reach target or lacks Pk; wasted Stinger | Only engage within 3,000 m optimum envelope; assess target speed before firing |
| Not jettisoning stores when under air attack from fast jet | Reduced speed and maneuverability; cannot evade threat effectively | Emergency jettison when survival requires maximum aircraft performance |
| Firing Stinger without achieving lock tone | Missile guides on noise; likely miss | Wait for the high-pitched steady lock tone before pressing the trigger |

---

*Based on TM 1-1520-248-10, FM 3-04.140, AIM-92 ATAS system documentation, Polychop Simulations DCS OH-58D documentation. For simulation use only.*
