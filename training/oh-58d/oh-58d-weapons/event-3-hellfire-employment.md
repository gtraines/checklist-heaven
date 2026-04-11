# Event 3 — AGM-114 Hellfire Employment

> **Course:** OH-58D Kiowa Warrior Weapons Employment Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — Missile Variants & Target Selection](#part-1--missile-variants--target-selection)
4. [Part 2 — Guidance Modes](#part-2--guidance-modes)
5. [Part 3 — LOBL Employment Sequence](#part-3--lobl-employment-sequence)
6. [Part 4 — LOAL Employment Sequence](#part-4--loal-employment-sequence)
7. [Part 5 — Launch Envelopes](#part-5--launch-envelopes)
8. [Part 6 — Tactical Employment Techniques](#part-6--tactical-employment-techniques)
9. [Part 7 — Buddy Lase Operations](#part-7--buddy-lase-operations)
10. [Part 8 — Weight & Performance Considerations](#part-8--weight--performance-considerations)
11. [Completion Standards](#completion-standards)
12. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Select the correct AGM-114 variant (K, M, or N) based on the designated target type
- [ ] Describe all four guidance modes and select the appropriate mode for a given tactical situation
- [ ] Execute a complete LOBL engagement from hull-down, including all steps from target acquisition through BDA
- [ ] Execute a LOAL engagement with correct lasing timeline for the selected LOAL sub-mode
- [ ] Demonstrate laser maintenance through missile impact — no early cessation of designation
- [ ] Verify all in-envelope constraints before firing and recognize NOT RDY indications
- [ ] Apply buddy-lase procedures: designating for another shooter and receiving external designation
- [ ] Execute a hull-down engagement in under 45 seconds from unmask to remask
- [ ] Compute basic weight impact of Hellfire loadout and identify when HOGE may be constrained

> **Prerequisite Check:** Before this event, the student must demonstrate proficiency in MMS Point Track and laser operations (Event 1 standards) and correct arming/de-arming sequence (Event 2 standards). If these are deficient, remediate Events 1 and 2 before proceeding.

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase 1 | Academic review — Hellfire variants, guidance modes, envelope |
| Phase 2 | Cold-and-dark startup; MMS boresight; pre-engagement checks |
| Phase 3 | Hull-down LOBL engagements — single targets; 3+ successful LOBL shots required |
| Phase 4 | LOAL engagements — LOAL-DIR and LOAL-HI practice |
| Phase 5 | Buddy-lase demonstration (instructor acts as external shooter; student designates) |
| Phase 6 | Shutdown; debrief |

### Key Numbers for This Event

| Item | Value |
|---|---|
| Hellfire minimum range (LOBL) | ~500 m |
| Hellfire optimum range (LOBL) | 1,500–5,000 m |
| Hellfire maximum range | ~8,000 m |
| LOAL-DIR lasing start (at 4 km) | ~8–10 sec before estimated impact |
| LOAL-HI lasing start (at 4 km) | ~10–15 sec before estimated impact |
| Maximum hull-down time | 60 seconds per unmask cycle |
| Maximum recommended time per BP | 2 engagements, then displace |
| M3P + 4× Hellfire loadout weight impact | ~400 lbs added to aircraft GW |

---

## Part 1 — Missile Variants & Target Selection

All OH-58D Hellfires use **Semi-Active Laser (SAL)** guidance. They home on reflected laser energy from the MMS laser designator. The three variants differ only in warhead type and terminal effect.

### Variants

| Variant | Designation | Warhead | Primary Target Set |
|---------|-------------|---------|-------------------|
| **AGM-114K** | Hellfire II | Tandem HEAT (shaped charge + precursor defeats Explosive Reactive Armor) | MBTs, IFVs, heavy armor, hardened bunkers |
| **AGM-114M** | Hellfire II | Blast-Fragmentation | Soft vehicles, trucks, boats, structures, troops in the open |
| **AGM-114N** | Hellfire II (MAC) | Metal Augmented Charge (Thermobaric) | Bunkers, caves, enclosed fighting positions, troops in cover |

### Variant Selection Matrix

| Target Type | Recommended Variant | Rationale |
|-------------|-------------------|-----------|
| Main Battle Tank (T-72, T-80, T-90) | **AGM-114K** | Tandem HEAT defeats ERA and heavy composite armor |
| IFV / APC (BMP, BTR, M2 Bradley) | **AGM-114K** | HEAT penetrates light-to-medium armor reliably |
| Light vehicles, trucks, technicals | **AGM-114M** | Blast-frag provides wider damage radius; HEAT overpenetrates with insufficient secondary effect |
| Boats / patrol craft | **AGM-114M** | Blast-frag causes structural damage and crew casualties |
| Buildings / structures (general) | **AGM-114M** | General demolition; good structural damage |
| Buildings with personnel inside | **AGM-114N** | Thermobaric overpressure devastates interior spaces and occupants |
| Bunkers / cave entrances | **AGM-114N** | MAC creates lethal overpressure wave in enclosed spaces |
| Troops in prepared positions (defilade) | **AGM-114N** | Thermobaric defeats cover that stops fragmentation |
| Troops in the open | **AGM-114M** | Blast-frag delivers better fragmentation pattern against exposed personnel |

### AGM-114L (Longbow Hellfire) — Do Not Use on OH-58D

The AGM-114L uses **radar guidance (RF)** and requires the Apache Longbow Fire Control Radar (FCR) for targeting. The OH-58D has **no FCR** and cannot employ the AGM-114L. If this variant appears in the DCS loadout screen, do not load it — use SAL variants (K/M/N) exclusively.

---

## Part 2 — Guidance Modes

All SAL variants support four guidance modes. Mode selection determines the missile's flight profile and the lasing timeline.

### Mode Overview

| Mode | Abbreviation | Missile Flight Path | Lasing Requirement | Best Situation |
|------|-------------|--------------------|--------------------|---------------|
| **Lock-On Before Launch** | LOBL | Direct proportional navigation to laser spot | Lase **before** launch; wait for LOCK indication | Clear LOS to target; highest confidence shot; primary mode |
| **Lock-On After Launch — Direct** | LOAL-DIR | Direct (near-line-of-sight) trajectory toward target area | Launch without laser; begin lasing before TOF expires | Clear LOS exists but lock uncertain pre-launch; medium range |
| **Lock-On After Launch — Low** | LOAL-LO | Low loft arc; missile clears low terrain obstacles | Launch without laser; lase during terminal phase | Short range with intervening low terrain |
| **Lock-On After Launch — High** | LOAL-HI | High loft arc; missile climbs then dives onto target | Launch without laser; lase during terminal descent | Long range; significant terrain between shooter and target; maximum standoff |

### Mode Selection Guidelines

| Tactical Situation | Recommended Mode | Reason |
|-------------------|-----------------|--------|
| Clear LOS, range < 5 km | **LOBL** | Highest Pk; confirmed lock pre-launch |
| Clear LOS, 5–8 km, lock uncertain | **LOAL-DIR** | Missile reaches target before lock timeout if laser starts mid-flight |
| Partial terrain masking between shooter and target | **LOAL-LO** or **LOAL-HI** | Missile arcs over intervening terrain |
| Maximum standoff; target behind ridgeline | **LOAL-HI** | Highest trajectory; greatest range and terrain clearance |
| Buddy lase — Kiowa receives external designation | **LOAL-DIR** or **LOBL** | Depends on whether Kiowa can observe the laser spot pre-launch |
| Multiple rapid engagements | **LOBL** | Fastest shot-to-shot cycle; immediate feedback on lock quality |

---

## Part 3 — LOBL Employment Sequence

LOBL is the **primary Hellfire mode** for the OH-58D. The missile confirms guidance before launch, providing the highest probability of kill.

### Step-by-Step LOBL Procedure

| Step | Action | MFD / Cockpit Indication |
|------|--------|--------------------------|
| 1 | **Occupy battle position** — hull-down; MMS unmasked above terrain | MMS video shows target area |
| 2 | **Acquire target in WFOV** — systematic search of assigned sector | Target area visible |
| 3 | **Switch to NFOV** — close in on contact | Target visible; NFOV magnification |
| 4 | **Identify and classify** — PID per ROE | Positive identification of hostile target |
| 5 | **Engage Point Track** on target | PT indication; crosshair tracking target |
| 6 | **LRF pulse** — verify target is within envelope | Range readout on MFD (confirm 500 m – 8,000 m) |
| 7 | **Select Hellfire** on weapons page | HF displayed; verify variant (K / M / N) matches target type |
| 8 | **Select LOBL** mode | LOBL annunciated on MFD |
| 9 | **Verify PRF code** — MMS code matches missile seeker code | PRF code confirmed on both MMS and weapons sub-page |
| 10 | **Master Arm → ARM** | MASTER ARM annunciation on MFD |
| 11 | **Arm laser** | LASER ARMED indication |
| 12 | **Begin lasing** — press and hold laser designate | LASER FIRING indication; energy on target |
| 13 | **Wait for LOCK** — missile seeker acquires reflected laser energy | **LOCK** indication on MFD |
| 14 | **Verify in-envelope** — RDY indication | RDY on weapons page; launch acceptability region valid |
| 15 | **Pickle (fire)** | MSL AWAY annunciation; missile leaves rail |
| 16 | **Maintain Point Track** — hold laser on target | Crosshair on target; laser firing |
| 17 | **Maintain lasing** until impact | Do not release under any circumstances until impact flash |
| 18 | **Impact observed** | Impact flash on MMS |
| 19 | **Cease laser** — release designate button | LASER OFF |
| 20 | **BDA** — observe target for 10 seconds | Secondary explosions, target movement, crew activity; report results |
| 21 | **Remask / Re-engage or safe** | Descend below terrain; move to alternate BP; or Master Arm → SAFE |

> **CRITICAL — Never release laser before impact.** The AGM-114 SAL seeker homes on reflected laser energy. The moment lasing stops, the seeker loses its guidance reference. The missile will fly ballistic to its last computed trajectory and miss. This is the single most common cause of Hellfire misses, and it is entirely pilot error. Maintain designation until you see the flash. Count the time of flight if necessary — but **do not stop lasing**.

---

## Part 4 — LOAL Employment Sequence

LOAL modes are used when pre-launch lock cannot be achieved (excessive range, terrain masking, or geometry prevents the seeker from seeing the laser spot before launch) or when the pilot wants to minimize hull-down exposure time.

### LOAL General Procedure

| Step | Action | Notes |
|------|--------|-------|
| 1 | **Acquire target** with MMS; establish Point Track | Identical to LOBL steps 1–6 |
| 2 | **Select Hellfire → LOAL mode** (DIR / LO / HI) | Select based on range and terrain — see mode guidelines above |
| 3 | **Verify PRF code** | Missile will search for this PRF code during terminal phase |
| 4 | **Master Arm → ARM** | — |
| 5 | **Arm laser** | Ready to lase when needed — do NOT lase before launch in LOAL |
| 6 | **Pickle (fire)** — missile launches on programmed trajectory | MSL AWAY; missile follows selected flight profile |
| 7 | **Note estimated TOF** | MFD may display estimated TOF; begin mental countdown |
| 8 | **Begin lasing** at the correct time | See lasing timeline below; precision crosshair on target |
| 9 | **Maintain lasing** until impact | Missile acquires laser; guides to impact |
| 10 | **Impact → Cease laser → BDA** | Same as LOBL steps 18–21 |

### LOAL Lasing Timeline

| Mode | Approx. TOF (at 4 km) | When to Start Lasing | Notes |
|------|----------------------|----------------------|-------|
| **LOAL-DIR** | ~12–15 sec | 8–10 sec before estimated impact | Direct trajectory; needs laser acquisition relatively early |
| **LOAL-LO** | ~15–20 sec | 8–10 sec before estimated impact | Low arc; laser needed as missile approaches target area |
| **LOAL-HI** | ~20–30 sec | 10–15 sec before estimated impact | High arc; laser needed during terminal dive |

**Rule of thumb:** Start lasing at approximately **60–70% of estimated TOF**. It is always better to start lasing early — the missile has more time to acquire and correct — than to lase late and have the missile fly past the acquisition window.

> *⚠ Realism Divergence: Real-world employment uses precise time-of-flight tables based on exact range, altitude, and temperature. DCS provides a simplified TOF estimate. The principle (lase before terminal phase) is identical. In DCS, erring on the side of earlier lasing is recommended — there is minimal penalty for lasing too early in LOAL mode.*

---

## Part 5 — Launch Envelopes

### Range Constraints

| Mode | Minimum Range | Maximum Range | Optimum Range |
|------|--------------|---------------|---------------|
| **LOBL** | ~500 m | ~8,000 m | 1,500–5,000 m |
| **LOAL-DIR** | ~750 m | ~8,000 m | 2,000–6,000 m |
| **LOAL-LO** | ~500 m | ~6,000 m | 1,000–4,000 m |
| **LOAL-HI** | ~1,500 m | ~8,000 m | 3,000–8,000 m |

> *⚠ Realism Divergence: Real-world Hellfire maximum range depends on variant, altitude, temperature, and atmospheric conditions. The 8 km figure is a nominal maximum under good conditions. DCS models range primarily as a function of motor burn and drag.*

### Altitude & Airspeed Constraints

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Minimum Launch Altitude** | ~50 ft AGL (hover fire) | Hull-down hover is the primary employment posture |
| **Maximum Launch Altitude** | ~15,000 ft MSL | Limited by motor performance at altitude |
| **Minimum Airspeed** | 0 KIAS (hover) | Hover fire is normal — no airspeed required |
| **Maximum Airspeed** | ~120 KIAS (near Vne) | High-speed launch is possible; limits maneuvering margin |
| **Recommended Speed** | 0–60 KIAS | Hover to slow flight; best MMS tracking stability |

### Out-of-Envelope Indicators

If the MFD shows **NOT RDY** or the launch acceptability region is invalid, the missile should not be fired. Common causes:
- Range below minimum (too close — missile cannot arm and track)
- Range beyond maximum (motor will not reach)
- Excessive airspeed or altitude (rare at typical OH-58D operating parameters)
- Laser not armed or not firing (LOBL only)
- Seeker not locked (LOBL only)

---

## Part 6 — Tactical Employment Techniques

### Hull-Down Engagement (Primary Technique)

The defining OH-58D employment posture. Minimizes exposure while delivering precision fires.

| Phase | Action | Target Duration |
|-------|--------|----------------|
| **Approach** | NOE flight (25–50 ft AGL); fully terrain-masked; approach from covered route | As needed |
| **Unmask to hull-down** | Rise until MMS clears terrain; fuselage remains below cover | 20–60 seconds (acquire, engage, BDA) |
| **Remask** | Descend below terrain immediately after BDA | Immediate |

**Hull-Down Engagement Sequence (Condensed):**
1. Approach BP at NOE; arrive from covered route.
2. Hover into hull-down — rise until MMS clears terrain, no more.
3. Acquire target (WFOV → NFOV → Point Track).
4. Execute LOBL sequence; fire when LOCK confirmed.
5. Maintain laser until impact.
6. BDA: 10 seconds on target area; report results.
7. Remask immediately — descend below terrain.
8. Move to alternate BP after 1–2 engagements.

**Hull-Down Time Standards:**
| Guideline | Duration |
|-----------|----------|
| Maximum recommended per unmask | 45–60 seconds |
| Optimal (pre-planned engagement) | 20–30 seconds |
| Minimum (rapid shot) | 10–15 seconds |

### Running Fire

Engagement during lateral or forward movement:
- Used when the BP is compromised, during displacement to alternate BP, or when targets require rapid servicing during movement.
- Maintain 30–60 KIAS; MMS tracks target via Point Track; execute LOBL during movement.
- **Advantage:** Harder to detect and target; continuous movement complicates enemy return fire.
- **Disadvantage:** MMS tracking is less stable during maneuvering; slightly increased miss risk.

### Rapid Engagement (Unmask-Shoot-Remask)

Minimizing exposure time to the absolute minimum:
1. Pre-plan the engagement: know the target bearing and approximate range from map study or previous observation.
2. Rise to hull-down with MMS already pointing in the correct azimuth sector.
3. Acquire target as rapidly as possible — MMS should be in NFOV near the expected contact area.
4. LOBL lock → fire immediately upon LOCK indication.
5. Maintain laser designation (the mast allows lasing while beginning to remask — the fuselage can descend while the MMS still has LOS).
6. Remask after impact.

**Target time in hull-down:** < 30 seconds — acquire, lock, fire, guide, BDA, remask.

### Ripple Fire (Multiple Targets)

Engaging multiple targets in sequence:
1. Fire first missile → maintain laser → impact → BDA (5 seconds).
2. Immediately slew MMS to next target → Point Track → LOBL lock → fire.
3. Repeat until Winchester or all targets destroyed.
4. Remask and displace to alternate BP.

**Typical cadence:** 15–30 seconds between shots (target acquisition and lock time for each subsequent target).

---

## Part 7 — Buddy Lase Operations

### OH-58D Designates for Another Shooter

| Step | OH-58D Action | Shooter Action |
|------|--------------|----------------|
| 1 | Acquire and Point Track target with MMS | Monitor frequency; prepare weapon |
| 2 | Report: *"Lasing, code 1688, target [type] at [grid / TRP]"* | Set weapon PRF to match; confirm |
| 3 | Begin lasing; report: *"Spot"* | *"Copied, code 1688"* |
| 4 | Maintain lasing | *"Cleared hot" → "Rifle"* (launch) |
| 5 | Maintain lasing until *"Splash"* | Report *"Splash"* on impact |
| 6 | Conduct BDA; report target status | Copy BDA |

### OH-58D Receives External Designation

| Step | External Designator | OH-58D Action |
|------|-------------------|--------------|
| 1 | Acquires target; reports PRF code | Set Hellfire weapon PRF to match external laser code |
| 2 | Reports *"Lasing, code [PRF]"* / *"Spot"* | Confirm MMS can see target area; select Hellfire LOBL or LOAL |
| 3 | Maintains laser designation | Fire when ready: *"Rifle"* |
| 4 | Maintains laser until impact | Monitor MMS for impact |
| 5 | Reports BDA | Copy BDA |

> **PRF Code Coordination:** In buddy-lase operations, the wrong PRF code means the weapon cannot see the laser. Brief codes before every mission. Write them on your kneeboard. Verify on MFD before every engagement where coordination is required.

---

## Part 8 — Weight & Performance Considerations

The OH-58D is a **power-limited, single-engine platform**. Every weapons loadout reduces hover ceiling and rate of climb.

| Loadout | Approximate Added Weight | Performance Impact |
|---------|------------------------|-------------------|
| 4× AGM-114 (full Hellfire) | ~400 lbs | Significant — may prevent HOGE in hot/high conditions; reduced maneuvering margin |
| 2× AGM-114 + M260 rockets | ~300 lbs | Moderate — good performance in most conditions |
| 2× AGM-114 + M3P .50 cal | ~350 lbs | Moderate — gun pod with ammo is heavy |

**Critical Hot/High Planning Factor:** In conditions above 30°C and/or above 3,000 ft elevation, a fully loaded OH-58D (4× Hellfire, full fuel) may not be able to hover out of ground effect (HOGE). The pilot may need to perform a running takeoff and will be unable to use hull-down hover engagement until weight decreases through fuel burn. Always compute power available vs. required before accepting a weapons loadout.

> In most standard DCS temperate conditions (sea level, 15°C), full Hellfire loadouts are manageable. In Persian Gulf or Syria summer missions at inland elevations, compute first.

---

## Completion Standards

The student passes this event when they can, without instructor prompting:

- [ ] Correctly select the appropriate Hellfire variant (K, M, or N) for a target type called by the instructor, and state the rationale
- [ ] Select LOBL guidance mode and navigate to the Hellfire MFD sub-page within 10 seconds of weapon selection command
- [ ] Execute a complete LOBL engagement sequence from hull-down, including Point Track, LRF range verification, PRF check, Master Arm, laser arm, lock confirmation, and pickle — 3 successful hits required
- [ ] Maintain continuous laser designation from lock through impact on each LOBL engagement — no early cessation (automatic REPEAT if laser is released before impact flash)
- [ ] Execute a complete LOAL engagement (LOAL-DIR or LOAL-HI) with correct lasing timeline — 1 successful hit required
- [ ] Achieve hull-down exposure time ≤ 60 seconds per unmask cycle on each engagement
- [ ] Displace to an alternate BP after the first two engagements from the initial BP
- [ ] Conduct BDA within 10 seconds of each impact; report results verbally
- [ ] Demonstrate buddy-lase designation procedure for an external shooter (instructor acts as shooter)
- [ ] Demonstrate de-arming sequence (Laser SAFE, Master Arm SAFE) within 5 seconds of each engagement completion

---

## Common Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Firing LOBL without confirmed LOCK indication | Missile launches unguided; flies ballistic; misses | Wait for the LOCK annunciation — do not rush the shot; no LOCK = no fire |
| Breaking laser before impact | Missile loses guidance in terminal phase; misses or strikes offset | Maintain laser until the impact flash; count TOF if needed; resist the urge to remask early |
| PRF code mismatch between MMS and weapon | Seeker cannot acquire laser; missile flies ballistic | PRF verification is a mandatory arming step — check every time, without exception |
| LOAL lasing too late | Missile flies past the acquisition window; misses | Start lasing at 60–70% of TOF; err early rather than late |
| Over-unmasking (fuselage above terrain) | Aircraft vulnerable to visual detection, small arms, MANPADS | Rise only until MMS clears; use radar altimeter cross-check; practice hull-down hover precision |
| Remaining in WFOV for designation | Target too small to aim accurately; laser wanders off target | Switch to NFOV before final ID and Point Track; WFOV is for search only |
| Not selecting correct variant | HEAT on soft target (over-penetration, low effect) or blast-frag on heavy armor (insufficient penetration) | Brief target types pre-mission; verify variant on sub-page before engagement |
| Hovering in the same BP after engagement | Enemy identifies position; counter-fires on known location | Move to alternate BP after every 1–2 engagements; never fire more than 2 missiles from the same position |
| Forgetting to arm laser before LOBL | Laser does not fire; seeker sees nothing; LOCK never achieved | LASER ARMED is a mandatory arming step; verify indication; include in verbal checklist |
| Excessive time in hull-down (target fixation) | Extended exposure increases detection and engagement probability | Set a personal time limit (45 seconds); if no lock within 30 seconds, remask and reapproach |

---

*Based on TM 1-1520-248-10, TM 9-1425-484-12 series (AGM-114 Hellfire), FM 3-04.140, Polychop Simulations DCS OH-58D documentation. For simulation use only.*
