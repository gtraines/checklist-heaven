# Event 7 — Air-to-Air Self-Defense (R-60 & R-73)

> **Course:** Mi-24P Hind Weapons Qualification Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [R-60 System Data](#r-60-system-data)
4. [R-73 System Data](#r-73-system-data)
5. [Missile Comparison](#missile-comparison)
6. [Engagement Envelopes](#engagement-envelopes)
7. [Threat Prioritization](#threat-prioritization)
8. [Engagement Sequence](#engagement-sequence)
9. [When NOT to Engage](#when-not-to-engage)
10. [Integration with Defensive Systems](#integration-with-defensive-systems)
11. [In-Sim Procedures](#in-sim-procedures)
12. [Common Errors](#common-errors)
13. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] State Mi-24P air-to-air doctrine: self-defense role, not offensive air combat
- [ ] Explain R-60 and R-73 seeker types, effective envelopes, and flare resistance
- [ ] Select R-60 vs. R-73 based on target type and engagement aspect
- [ ] Execute R-60/R-73 seeker acquisition and launch sequence in DCS
- [ ] Identify which threats require engagement vs. terrain masking and escape
- [ ] Coordinate air-to-air engagement with defensive maneuvering and countermeasures
- [ ] State 5 situations where fast-jet engagement should be avoided

---

## Ground Brief

### The Mi-24P Is Not a Fighter

This is the most critical ground truth of this event. Soviet doctrine assigns the Mi-24P to the Close Air Support and anti-tank role. The R-60 and R-73 were added as **emergency self-defense weapons**, not to create a helicopter fighter. If a crew thinks of AAMs as offensive tools, they will take engagements they should avoid, burn fuel, and likely die.

**Doctrine priority order (from most to least preferred):**
1. **Don't be seen** — terrain masking, low altitude, route planning
2. **Don't be hit** — countermeasures + evasive maneuvering
3. **Shoot back** — AAM as absolute last resort against helicopters
4. **Escape** — disengage from fast jets immediately

### Threat Priority vs. Response

| Threat | Priority | Recommended Response |
|---|---|---|
| **Fast jets (F-16, A-10, MiG-29)** | AVOID | Terrain masking + CM + escape |
| **Enemy attack helicopters (Mi-24, Ka-50, AH-64)** | HIGH | AAM if geometry favorable |
| **Transport helicopters (Mi-8, UH-60)** | MEDIUM | AAM if mission-critical |
| **Slow fixed-wing (An-2, L-39)** | MEDIUM | AAM if immediate threat |
| **MANPADS teams** | LOW | Cannon / rockets more appropriate |

---

## R-60 System Data

| Specification | Value |
|---|---|
| **NATO Designation** | AA-8 Aphid |
| **Seeker Type** | Infrared homing (all-aspect) |
| **Warhead** | 3 kg HE fragmentation |
| **Lethal Radius** | 7.5 m (proximity fuze) |
| **Missile Weight** | 43.5 kg |
| **Effective Range** | 500–5,000 m |
| **Max Speed** | Mach 2.5 |
| **G-Limit (missile)** | 7G |
| **Flare Resistance** | Low (easily decoyed) |
| **Best Against** | Helicopters, slow aircraft |

---

## R-73 System Data

| Specification | Value |
|---|---|
| **NATO Designation** | AA-11 Archer |
| **Seeker Type** | Infrared imaging (advanced IRCCM) |
| **Seeker Capability** | All-aspect + off-boresight |
| **Warhead** | 7.4 kg HE fragmentation |
| **Lethal Radius** | 12 m (proximity fuze) |
| **Missile Weight** | 105 kg |
| **Effective Range** | 300–15,000 m |
| **Max Speed** | Mach 2.5+ |
| **G-Limit (missile)** | 12G |
| **Flare Resistance** | Moderate (IRCCM equipped) |
| **Off-Boresight** | ±45° (with HMS if modeled) |
| **Best Against** | All air targets including maneuvering threats |

---

## Missile Comparison

| Aspect | R-60 (AA-8) | R-73 (AA-11) |
|---|---|---|
| **Max Effective Range** | 5,000 m | 15,000 m |
| **Maneuverability** | 7G | 12G |
| **Seeker** | Spinning-reticle IR | Imaging IR (IRCCM) |
| **Off-Boresight** | ±5° | ±45° (with HMS) |
| **Flare Resistance** | Low | Moderate |
| **Weight** | 43.5 kg (lighter) | 105 kg (heavier) |
| **Use For** | Helicopters, slow aircraft | All threats; snap shots |
| **Conserve For** | Routine engagements | High-value / maneuvering threats |

> *⚠ Realism Divergence: R-73 off-boresight capability in DCS depends on whether the Shchel-3UM HMS is modeled. DCS may provide off-boresight capability without requiring HMS operation. Real-world R-60 is more susceptible to decoy flares than DCS typically models.*

---

## Engagement Envelopes

### R-60

| Aspect | Min Range | Max Range | Optimum |
|---|---|---|---|
| **Head-On** | 500 m | 5,000 m | 1,500–3,000 m |
| **Beam** | 800 m | 3,500 m | 1,000–2,500 m |
| **Tail Chase** | 300 m | 8,000 m | 2,000–5,000 m |

**Altitude floor:** ≥50 m AGL (head-on/tail), ≥100 m AGL (beam) — ground clutter below these altitudes degrades seeker.

### R-73

| Aspect | Min Range | Max Range | Optimum |
|---|---|---|---|
| **Head-On** | 300 m | 12,000 m | 2,000–6,000 m |
| **Beam** | 500 m | 8,000 m | 1,500–5,000 m |
| **Tail Chase** | 200 m | 15,000 m | 3,000–10,000 m |

---

## Threat Prioritization

### Helicopter vs. Helicopter Engagements

| Enemy Aircraft | Tactics | Recommended Approach |
|---|---|---|
| **Mi-24 / Mi-28** | Low-level attack runs | R-73 head-on or beam shot |
| **Ka-50 / Ka-52** | Hovering ATGM attacks | R-73 (high maneuverability needed) |
| **AH-64 Apache** | Standoff ATGM at 4–6 km | Close distance; R-73 engagement |
| **AH-1 Cobra** | Pop-up attacks | R-60 beam shot during pop-up |
| **UH-60 Transport** | Low-level insertion | R-60 (any aspect; large, slow target) |

### Engagement Geometry

- **Preferred:** Beam or head-on aspect (highest kill probability)
- **Avoid:** Stern chase unless significant speed advantage
- **Altitude:** Maintain altitude advantage when possible
- **Terrain:** Use terrain masking during approach and escape

### Kill Probability Table

| Factor | R-60 | R-73 |
|---|---|---|
| Optimum range | 85% | 90% |
| Maximum range | 40% | 60% |
| Head-on aspect | 75% | 85% |
| Beam aspect | 65% | 80% |
| vs. maneuvering target | 50% | 70% |
| vs. countermeasures | 30% | 50% |

---

## Engagement Sequence

### Standard AAM Engagement (DCS)

**Step 1 — Threat Detection:**
- SPO-15: Audio/visual warning (radar-equipped threats)
- Visual: Naked eye acquisition; binoculars or PKV-1 for identification
- Crew call: WSO to pilot — "Air contact, [type], [bearing], [range]"

**Step 2 — Weapon Selection (WSO Seat — `1`):**
1. Master Arm → **ARMED**
2. Weapon Selector → **AAM**
3. Missile Type → R-60 or R-73
4. Pylon Selector → loaded station

**Step 3 — Target Acquisition:**
1. PKV-1 slew onto target aircraft
2. Magnification 2–4× for identification
3. Range check — within missile envelope
4. Aspect assessment — target heading and speed

**Step 4 — Seeker Activation and Lock:**
1. Seeker power on (automatic with weapon selection)
2. Direct seeker to target bearing
3. Wait for **solid lock** — distinct audio tone + visual symbol
4. Call: "Seeker lock, [missile type], ready to fire"

**Step 5 — Launch:**
1. Fire button → press when solid lock confirmed
2. 0.5–1.0 second delay before missile leaves rail
3. Missile is fire-and-forget after launch — aircraft free to maneuver

**Step 6 — Post-Launch:**
1. BDA: track missile to impact or miss
2. Threat assessment: continued monitoring
3. Escape: immediate maneuvering to avoid counter-fire

---

## When NOT to Engage

Fast jet threats are fundamentally different from helicopter threats. The Mi-24P cannot win a sustained air combat engagement against a jet fighter.

**Do NOT engage when:**
- Closure rate >800 km/h (seeker tracking limits)
- Fast jet at altitude >3,000 m AGL
- Fast jet in attack dive directly toward aircraft
- Multiple fast jets in area
- Low fuel or ammunition (cannot sustain engagement)

**Defensive priorities vs. fast jets:**
1. Terrain masking — drop to <50 m AGL immediately
2. Maximum speed — every knot counts for escape
3. Continuous countermeasures — flares (R-60/AIM-9) or chaff (radar AAM)
4. Hard evasive turns
5. AAM — only if no escape option

---

## Integration with Defensive Systems

### SPO-15 RWR Integration

- RWR provides bearing to radar-equipped threats (fighters, some helicopter radars)
- Classify signature: fighter vs. helicopter based on RWR symbol
- Reaction time target: SPO-15 warning to AAM launch ≤10 seconds
- Limitation: No RWR warning for visual/IR threats

### Countermeasures During AAM Engagement

| Phase | Countermeasures Action |
|---|---|
| **Pre-launch** | Dispense flares if IR threat incoming |
| **During own engagement** | Avoid dispensing flares (may decoy own missile) |
| **Post-launch** | Resume countermeasures for own defense |
| **Escape** | Combine with immediate evasive maneuver |

---

## In-Sim Procedures

### DCS Key Bindings

| Function | Default Key |
|---|---|
| **Select AAM** | `D` (weapon cycle to air-to-air) |
| **Fire Missile** | `Space` |
| **Pylon Select** | `W` / `E` (cycle) |
| **PKV-1 Slew** | Numpad 2/4/6/8 |
| **Seat — WSO** | `1` |
| **Seat — Pilot** | `2` |
| **Autopilot** | `A` |

### Mission Practice Sequence

**Exercise 1 — R-60 vs. stationary helicopter at 2,500 m:**
- Profile: Approach from beam aspect
- Seeker lock required before firing
- Standard: Valid lock achieved; missile fired within envelope

**Exercise 2 — R-73 vs. slow aircraft at 4,000 m:**
- Profile: Head-on aspect engagement
- Standard: Solid lock; missile away; hit or near-miss

**Exercise 3 — Threat response drill (no shoot):**
- Fast jet contact detected by SPO-15
- Standard: Immediate terrain masking + countermeasures; no engagement attempt

**Exercise 4 — Combined defensive engagement:**
- MANPADS launch (visual); immediate flares + evasion
- Followed by enemy helicopter at 3,000 m; R-60 engagement
- Standard: Correct CM for MANPADS; correct AAM employment; both handled in sequence

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| **Engaging fast jets** | Exposure to superior threats | Evade; do not engage |
| **Firing without solid lock** | Likely miss; ammunition waste | Wait for distinct audio tone + symbol |
| **No escape plan before engagement** | Trapped after shot | Plan exit route before firing |
| **Firing outside effective envelope** | Miss; waste | Verify range and aspect before launch |
| **No threat prioritization** | Engage wrong target first | Most immediate threat first |
| **Dispensing own flares during guidance** | May decoy own missile | Hold CM during own missile flight |
| **Firing into ground clutter** | Seeker false lock | Maintain altitude separation from terrain |
| **Wrong missile selection** | Suboptimal performance | R-73 for jets/maneuvering; R-60 for slow/easy |
| **AAM as primary weapon** | Mission scope creep | Ground attack mission takes priority |

---

## Completion Standards

The student must demonstrate the following to the instructor's satisfaction:

- [ ] Correctly state Mi-24P air-to-air doctrine (self-defense only) in pre-flight oral
- [ ] List 3 scenarios where fast-jet engagement should be avoided
- [ ] Execute R-60 engagement: seeker lock confirmed before launch; target within envelope
- [ ] Execute R-73 engagement: correct lock procedure; missile away
- [ ] Demonstrate correct fast-jet response: terrain masking + CM; no engagement
- [ ] Execute combined scenario (MANPADS + enemy helicopter) with correct response to each
- [ ] No engagement attempt outside effective missile envelope
- [ ] Correct CM selection (flares) coordinated with post-launch maneuver

---

*Based on DCS World Mi-24P Hind module by Eagle Dynamics; R-60 and R-73 missile system documentation; Soviet Air Forces air-to-air doctrine for attack helicopters. For simulation use only.*
