# Event 10 — Mission Planning & Loadout Optimization

> **Course:** OH-58D Kiowa Warrior Weapons Employment Course | **Event Type:** Academic / Ground
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — Threat Analysis & IPB](#part-1--threat-analysis--ipb)
4. [Part 2 — Loadout Selection](#part-2--loadout-selection)
5. [Part 3 — Engagement Planning](#part-3--engagement-planning)
6. [Part 4 — Communication & Laser Code Planning](#part-4--communication--laser-code-planning)
7. [Part 5 — DCS Mission Editor Integration](#part-5--dcs-mission-editor-integration)
8. [Part 6 — Weather & Environmental Considerations](#part-6--weather--environmental-considerations)
9. [Completion Standards](#completion-standards)
10. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Conduct a threat analysis using available mission briefing information and produce a threat ring overlay for route planning
- [ ] Select an optimal weapons loadout based on the target set, threat environment, mission type, and aircraft performance constraints
- [ ] Compute a power check for the planned loadout at mission conditions (pressure altitude + temperature) and determine HOGE capability
- [ ] Develop a pre-mission engagement plan including EA boundaries, Battle Positions (primary/alternate/supplementary), TRPs, trigger lines, and engagement priorities
- [ ] Establish a communication frequency plan and laser PRF code deconfliction matrix for multi-ship/multi-designator operations
- [ ] Use the DCS Mission Editor to configure loadouts, set waypoints along terrain-masked corridors, and mark target/BP reference points
- [ ] Brief the impact of weather and environmental conditions on sensor effectiveness and weapons employment

---

## Ground Brief

### Mission Profile

This event is conducted entirely as a **ground/academic event** — no flight required. The student produces a complete mission plan for a hypothetical scenario assigned by the instructor.

| Phase | Activity |
|---|---|
| Phase 1 | Threat analysis — map overlay with threat rings and route options |
| Phase 2 | Loadout selection — complete rationale; power check computation |
| Phase 3 | Engagement planning — EA, BPs, TRPs, trigger lines, priorities, ammunition management |
| Phase 4 | Communication plan — frequencies, PRF codes, brevity codes |
| Phase 5 | DCS Mission Editor configuration — loadout, waypoints, reference points |
| Phase 6 | Weather brief — sensor and weapons impact for scenario conditions |
| Phase 7 | Mission brief presentation — student briefs to instructor |

---

## Part 1 — Threat Analysis & IPB

### Intelligence Preparation of the Battlefield (IPB)

Before planning any weapons mission, the pilot conducts a threat analysis of the assigned operational area:

| Intelligence Element | What to Look For | Planning Impact |
|---------------------|-----------------|-----------------|
| **Enemy Air Defense** | SAM sites (SA-6, SA-8, SA-11, SA-15); MANPADS units; radar AAA (ZSU-23-4) | Defines no-fly zones; dictates ingress/egress corridors; determines CM requirements |
| **Enemy Armor** | MBTs, IFVs, APCs — location, quantity, direction | Determines Hellfire-K loadout requirement; identifies primary EA |
| **Enemy Soft Targets** | Trucks, C2 vehicles, logistics, troop positions | Determines rocket/gun/APKWS balance |
| **Enemy Air Threat** | Fighters, attack helicopters — presence and activity | Determines whether Stinger loadout is needed; influences route altitude |
| **Terrain** | Ridgelines, valleys, treelines, urban areas | Identifies BP locations, covered routes, masking opportunities |
| **Friendly Positions** | Ground unit locations, FEBA | Defines fire coordination lines; prevents fratricide; identifies FARP and rally locations |

### Threat Ring Mapping

For each identified threat system, plot an engagement ring on the mission map:

| Threat System | Engagement Range | Mapping Action |
|---------------|-----------------|----------------|
| **MANPADS** (SA-7/14/16/18 Igla) | ~5 km | 5 km rings around known/suspected infantry positions |
| **SA-8 Gecko** | ~12 km | 12 km ring; note SA-8 is mobile — may relocate between missions |
| **SA-11 Buk** | ~35 km | 35 km ring; major no-fly zone for helicopter operations |
| **SA-15 Tor** | ~12 km | 12 km ring; extremely fast reaction; extremely dangerous |
| **ZSU-23-4 Shilka** | ~2.5 km (effective) | 2.5 km ring; typically co-located with armor formations |
| **Small Arms** | ~1 km (effective vs. helicopters) | Assume present along FEBA and near all enemy positions |

### Route Planning Rule

Plot ingress and egress routes through **gaps between threat rings**, using terrain-masked corridors. If no gap exists:
- Plan SEAD coordination before entry, OR
- Accept the risk with maximum CM and strict terrain masking, OR
- Request mission modification from the ground commander

---

## Part 2 — Loadout Selection

The OH-58D's **two-pylon limitation** makes loadout selection one of the most consequential mission planning decisions. Every loadout is a tradeoff.

### Standard Loadout Configurations

| Loadout | Left Pylon | Right Pylon | Mission Profile | Best For |
|---------|-----------|-------------|-----------------|----------|
| **Full Hellfire** | 2× AGM-114 | 2× AGM-114 | Maximum anti-armor | Known armor-heavy EA; tank formations; when gun/rockets not needed |
| **Scout/Attack** | M3P .50 cal | 2× AGM-114 | Balanced recon + precision | Scout mission with engagement authority; most versatile for unknown threat mix |
| **General Purpose** | M260 Hydra 70 (7×) | 2× AGM-114 | Mixed precision + area | Mixed target set (armor + soft); most common combat loadout |
| **APKWS Mix** | M260 APKWS (7×) | 2× AGM-114 | Precision-heavy | All targets require guided weapons; low collateral damage missions |
| **Light Scout** | M3P .50 cal | M260 Hydra 70 (7×) | Light engagement + recon | Low-threat reconnaissance; extended endurance; no precision requirement |
| **Full Rockets** | M260 rockets | M260 rockets | Maximum area fires | Area suppression; no armor threat expected; maximum ammunition depth |
| **Air Defense** | AIM-92 Stinger (×2) | 2× AGM-114 | Anti-air + anti-armor | Credible enemy air threat; accept loss of gun/rocket capability |

### Loadout Decision Factors

| Factor | Consideration |
|--------|--------------|
| **Target Set** | Armor → Hellfire K; soft targets → rockets/gun; mixed → General Purpose |
| **Threat Environment** | High AD threat → Hellfire standoff preferred over close-in rockets/gun work |
| **Mission Type** | Scout → Scout/Attack (.50 cal + Hellfire); deliberate attack → Full Hellfire or GP |
| **Air Threat** | Significant air threat → consider Stinger on one pylon; accept reduced ground ordnance |
| **Performance** | Hot/high conditions → lighter loadout for HOGE capability; heavy loadout may prevent hover |
| **Endurance** | Lighter loadout = less drag = better fuel economy = more time on station |

### Weight & Performance Planning

| Loadout | Approx. Added Weight | Performance Impact |
|---------|---------------------|-------------------|
| 4× AGM-114 Hellfire | ~400 lbs | Significant — may prevent HOGE in hot/high conditions |
| 2× AGM-114 + M260 rockets | ~300 lbs | Moderate — good performance in most conditions |
| 2× AGM-114 + M3P .50 cal | ~350 lbs | Moderate — .50 cal pod with ammunition is heavy |
| 2× M260 rocket pods | ~200 lbs | Light — best performance with ordnance |
| M3P .50 cal + M260 rockets | ~250 lbs | Light-Moderate — good endurance configuration |

### Power Check Requirements

Before every weapons mission, compute:

| Step | Computation |
|------|-------------|
| 1 | **Gross weight at takeoff:** empty weight + fuel weight + weapons weight + crew + equipment |
| 2 | **Power available at mission conditions:** use pressure altitude + OAT to enter power chart |
| 3 | **Power required for HOGE** at computed gross weight |
| 4 | **Margin assessment:** if power available < power required for HOGE, hull-down hover-fire is not possible |

**If HOGE capability is insufficient:**
- Reduce fuel load (accept shorter endurance)
- Reduce weapons (lighter loadout)
- Plan running takeoff instead of vertical
- Accept that hull-down hover engagement is not available; plan running fire only

> **Instructor Note:** In temperate DCS conditions (sea level, 15°C), the OH-58D handles most loadouts. In hot/high DCS missions (Middle East maps, summer, 3,000 ft+ elevation), full Hellfire loadouts may exceed HOGE capability. Power check is mandatory — not optional.

---

## Part 3 — Engagement Planning

### Pre-Mission Engagement Plan Elements

| Element | Content |
|---------|---------|
| **Engagement Area (EA)** | Geographic bounds; marked on map and kneeboard |
| **Battle Positions (BP)** | Primary, Alternate, Supplementary — each with approach and egress routes |
| **Target Reference Points (TRP)** | Pre-designated points within EA for rapid target handoff |
| **Trigger Lines** | Lines that initiate specific engagements ("engage when enemy crosses Phase Line RED") |
| **Priority of Engagement** | 1: AD; 2: Armor; 3: C2; 4: Soft targets — or as assigned by mission brief |
| **Weapons Allocation** | Hellfire for Priorities 1–2; APKWS/rockets for Priorities 3–4; gun for targets of opportunity |
| **Ammunition Management** | Define "Bingo Ammo" states: Hellfire ≤1; rockets ≤3; gun ≤100 rounds → report to lead; consider RTB |
| **Abort Criteria** | Winchester; Bingo fuel; combat damage; weather below minimums; loss of comms |

### Engagement Sequence — Armor Defense Example

| Phase | Action | Timeframe |
|-------|--------|-----------|
| **Pre-Position** | Occupy primary BP via covered route; establish hull-down | T−5 min (before enemy arrival) |
| **Observation** | MMS scan EA; report enemy composition, location, movement | T=0 (enemy enters EA) |
| **Engagement** | Engage per priority: AD → armor → C2 → soft | T+0:30 to T+5:00 |
| **Displacement** | Move to alternate BP after 1–2 engagements from each position | After each engagement pair |
| **Re-engagement** | Continue from alternate/supplementary BPs | Until targets destroyed or Winchester |
| **Withdrawal** | Covered egress to FARP or rally point | Winchester, Bingo fuel, or mission complete |

---

## Part 4 — Communication & Laser Code Planning

### Frequency Plan

| Net | Purpose | Participants |
|-----|---------|-------------|
| **Team Internal** | Kiowa-to-Kiowa / Kiowa-to-Apache; target handoff, tactical calls | Aviation team members |
| **Ground Maneuver** | Coordination with ground commander; CCA requests; BDA reports | Ground element + aviation team lead |
| **Brigade/Battalion Fires** | Artillery coordination; fire support deconfliction | FSO/FSE + aviation |
| **Air Traffic / FARP** | FARP coordination; airspace deconfliction | ATC / FARP personnel |
| **Guard** | Emergency frequency | All |

### Laser PRF Code Deconfliction

When multiple designators operate simultaneously, **each must use a unique PRF code** to prevent weapons from homing on the wrong laser spot.

| Designator | PRF Code (Example) | Notes |
|-----------|-------------------|-------|
| Kiowa 1 | 1688 | Primary designator; EA left sector |
| Kiowa 2 | 1687 | Secondary designator; EA right sector |
| JTAC (if present) | 1686 | Ground-based designator for priority targets |
| Apache (if designating) | 1685 | Coordinated pre-mission |

**Rule:** Brief PRF codes during mission planning. Write them on the kneeboard. Verify on MFD before every engagement. Never assume the code is correct from a previous mission.

### Standard Brevity Codes

| Code | Meaning |
|------|---------|
| **"Rifle"** | Hellfire launch |
| **"Rockets"** | Rocket fire (unguided or APKWS) |
| **"Guns"** | .50 cal engagement |
| **"Fox Two"** | Stinger (IR air-to-air missile) launch |
| **"Spot"** | Laser designator active on target |
| **"Splash"** | Weapon impact on target |
| **"Cease laser"** | Stop laser designation |
| **"Winchester"** | All weapons expended |
| **"Bingo"** | Minimum fuel for return to FARP |
| **"Bingo Ammo"** | Minimum ammunition reserve remaining |
| **"Tally"** | Visual contact with target on MMS |
| **"No Joy"** | No visual contact with target |
| **"Engaged"** | Currently engaging target; do not reassign |
| **"Cleared Hot"** | Authorization to fire on specified target |
| **"Abort"** | Do not fire / cease engagement immediately |
| **"Break"** | Immediate defensive maneuver required |
| **"Remask"** | Return to hull-down / terrain cover |

---

## Part 5 — DCS Mission Editor Integration

### Configuring Loadouts

| Step | Action |
|------|--------|
| 1 | Open Mission Editor; select OH-58D unit |
| 2 | Open the payload/loadout tab |
| 3 | Select left pylon weapon (Hellfire, rockets, .50 cal, Stinger) |
| 4 | Select right pylon weapon (Hellfire, rockets, Stinger) |
| 5 | Select specific variant where applicable (Hellfire K/M/N; rocket warhead type) |
| 6 | Verify total weight and check against performance charts |

### Waypoint and Reference Point Planning

| Element | Mission Editor Action |
|---------|---------------------|
| **Waypoints** | Set ingress route along terrain-masked corridors; altitude waypoints for NOE flight segments |
| **Target Points** | Mark known/suspected target locations; visible as reference in cockpit |
| **FARP** | Mark FARP location; plan return route with sufficient fuel |
| **Battle Positions** | Mark as waypoints or reference points for cockpit navigation |
| **EA Boundaries** | Mark as reference points on map |
| **TRPs** | Mark as numbered reference points; brief on kneeboard with descriptions |

---

## Part 6 — Weather & Environmental Considerations

| Condition | Impact on Sensors | Impact on Weapons |
|-----------|------------------|------------------|
| **Clear day** | TV sensor optimal; TIS backup; visual PID possible | All weapons nominal |
| **Overcast / low ceiling** | TV degraded if ceiling below clouds is hazy; TIS unaffected | Pop-up attacks limited if ceiling is below apex altitude (300–800 ft); diving fire limited by cloud base |
| **Night (clear)** | TIS primary; TV unusable for NVG; NVG required for terrain avoidance | All weapons nominal; laser fully effective |
| **Night (overcast)** | TIS only; reduced terrain contrast even with NVG | All weapons nominal; increased CFIT risk reduces aggressiveness |
| **Fog / heavy rain** | TIS degraded; MMS effectiveness significantly reduced | Close-range only; consider mission abort |
| **Strong crosswind** | No sensor impact | Unguided rockets significantly affected (lateral drift); guided weapons (Hellfire, APKWS) unaffected |
| **Hot temperature** | No sensor impact | Power-limited; lighter loadout may be required; reduced HOGE capability |
| **High altitude** | No sensor impact | Reduced engine performance; longer distances to accelerate; lighter loadout required |

> **Instructor Note:** Students consistently underplan for weather. A hot, high-altitude mission in fog requires a fundamentally different loadout and engagement plan than a standard sea-level mission. Weather impact on sensors and weapons must be briefed during every mission planning session.

---

## Completion Standards

The student passes this event when they can produce a complete mission plan and brief it to the instructor. The plan must include, without instructor prompting:

- [ ] A threat ring map overlay with all known threat systems plotted at correct engagement ranges
- [ ] A route plan that routes ingress/egress through gaps between threat rings using terrain-masked corridors
- [ ] A loadout selection with written rationale citing at minimum: target set, threat environment, mission type, and power check result
- [ ] A power check computation using assigned scenario conditions (pressure altitude, temperature, gross weight)
- [ ] An engagement plan with EA boundaries, at least 3 TRPs, a minimum of one primary and two alternate BPs, trigger lines, engagement priorities, and ammunition management ("Bingo" states)
- [ ] A communication plan with frequency assignments and a PRF code matrix (minimum 2 designators deconflicted)
- [ ] A weather impact analysis for the assigned scenario conditions, covering both sensor effectiveness and weapons performance
- [ ] A Mission Editor configuration screenshot or walkthrough demonstrating correct loadout, waypoints, and reference points

---

## Common Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Loading max weapons without power check | Aircraft cannot HOGE; hull-down engagement not possible; forced to running fire only | Compute power check before finalizing loadout; reduce weapons or fuel if needed |
| Not planning alternate BPs | Stuck in one position; enemy locates and suppresses | Plan at minimum Primary, Alternate, and Supplementary; brief approach/egress for each |
| Not deconflicting PRF codes | Multiple lasers on same code; weapons home on wrong laser | Brief unique PRF codes; write on kneeboard; verify on MFD before every engagement |
| Routing through threat rings | Aircraft enters SAM engagement zone; shot down on ingress | Map all threat rings; route around them; accept longer flight time |
| Not planning ammunition management | All Hellfires expended on first target group; nothing for follow-on | Brief allocation: "No more than 2 Hellfire per target group" or equivalent ROE |
| Ignoring fuel planning | Bingo fuel during engagement; forced to disengage mid-fight | Plan: transit time + station time + reserve + return; monitor fuel continuously |
| Not briefing brevity codes | Confusion during engagement; ambiguous communications | Brief brevity codes pre-mission; standardize across the team; write on kneeboard |
| Wrong loadout for mission | All rockets vs. armor (ineffective); all Hellfire vs. soft targets (overkill) | Match loadout to target set; when uncertain, use General Purpose loadout |
| Ignoring weather impact | TIS unusable in heavy rain; rockets inaccurate in crosswind — not planned for | Brief weather impact on each sensor and weapon; adjust plan or loadout accordingly |

---

*Based on TM 1-1520-248-10, FM 3-04.126, FM 3-04.140, ATP 3-04.1, TC 1-211, Polychop Simulations DCS OH-58D documentation. For simulation use only.*
