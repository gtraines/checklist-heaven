# Event 5 — APKWS Laser-Guided Rocket Employment

> **Course:** OH-58D Kiowa Warrior Weapons Employment Course | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — System Overview](#part-1--system-overview)
4. [Part 2 — Decision Matrix: APKWS vs. Hellfire vs. Unguided](#part-2--decision-matrix-apkws-vs-hellfire-vs-unguided)
5. [Part 3 — Seeker Basket Concept](#part-3--seeker-basket-concept)
6. [Part 4 — Weapons Page Setup & PRF Configuration](#part-4--weapons-page-setup--prf-configuration)
7. [Part 5 — Employment Sequence](#part-5--employment-sequence)
8. [Part 6 — Employment Profiles](#part-6--employment-profiles)
9. [Part 7 — Buddy Lasing for APKWS](#part-7--buddy-lasing-for-apkws)
10. [Completion Standards](#completion-standards)
11. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Describe how APKWS (AGR-20A) guidance works, including the DASALS seeker and semi-active laser homing principle
- [ ] Explain the seeker acquisition basket concept and its implications for aircraft aiming
- [ ] Correctly differentiate when APKWS is the appropriate weapon vs. Hellfire or unguided Hydra 70 based on target type, range, and collateral damage constraints
- [ ] Configure the APKWS weapons page including PRF code verification
- [ ] Execute the full APKWS employment sequence: target acquisition → CCIP alignment → laser designation → fire → maintain laser → BDA
- [ ] Execute APKWS engagements from diving, running, and hover fire profiles
- [ ] Coordinate a buddy-lased APKWS engagement with an external designator
- [ ] Apply appropriate laser discipline (laser active before fire; maintained through impact)

---

## Ground Brief

### Mission Profile

| Phase | Activity |
|---|---|
| Phase 1 | Academic review — APKWS guidance, seeker basket, decision matrix |
| Phase 2 | Startup; weapons page setup; PRF code verification |
| Phase 3 | Diving fire APKWS engagements — ≥ 4 rounds against point targets at 1,500–3,000 m |
| Phase 4 | Running/level fire APKWS — 2 engagements |
| Phase 5 | Hover fire APKWS — 2 engagements |
| Phase 6 | Buddy-lasing scenario — 1 engagement coordinated with external designator (simulated or actual JTAC) |
| Phase 7 | Shutdown; debrief |

### Key Parameters for This Event

| Item | Value |
|---|---|
| Effective range | 1,500–5,000 m |
| Accuracy (CEP) | ~1–2 m |
| Warhead | M151 HE (10 lb) |
| Rounds per pod (M260) | 7 tubes |
| Maximum correction (seeker) | ~2–5° from boresight |
| Seeker FOV (half-angle) | ~10° |
| Diving fire range | 1,500–3,000 m |
| Hover fire range | 1,000–2,000 m |
| Break-off range | 1,000 m / 300 ft AGL |

---

## Part 1 — System Overview

The **APKWS** (Advanced Precision Kill Weapon System), designated **AGR-20A**, is a **semi-active laser (SAL) guided 2.75-inch rocket**. It uses the standard Mk 66 rocket motor and an M151 HE warhead with a **WGU-59/B DASALS** (Distributed Aperture Semi-Active Laser Seeker) guidance section inserted between the motor and warhead.

| Parameter | Value |
|-----------|-------|
| **Designation** | AGR-20A |
| **Guidance** | Semi-Active Laser (SAL) homing via WGU-59/B DASALS |
| **Motor** | Mk 66 Mod 4 (identical to unguided Hydra 70) |
| **Warhead** | M151 HE (10 lb High Explosive) |
| **Launcher** | M260 (7-tube) — same launcher as unguided Hydra 70 |
| **Effective Range** | 1,500–5,000 m |
| **Accuracy** | ~1–2 m CEP |
| **Guidance Requirement** | Laser designation at matching PRF code |

### How APKWS Guidance Works

1. The rocket is launched from the M260 launcher using **CCIP aiming** — identical to an unguided rocket.
2. After motor ignition and fin deployment, the **DASALS seeker** activates and searches for reflected laser energy at the programmed PRF code.
3. The seeker has a **limited field of regard (the "basket")** — the rocket must be aimed close enough to the target that the seeker can acquire the laser reflection after launch.
4. Once acquired, the seeker sends steering commands to guidance fins, correcting the rocket's trajectory to home on the laser spot.
5. The rocket impacts at or within ~1–2 m of the laser spot.

> **Key Concept:** APKWS is NOT a missile. It has **limited maneuvering capability** — it can correct its trajectory by a few degrees but cannot perform large course corrections. The pilot must aim the aircraft to place the rocket on a trajectory that enters the seeker basket. Think of it as a **"smart bullet"** — guided, but requiring the shooter to still aim it correctly.

---

## Part 2 — Decision Matrix: APKWS vs. Hellfire vs. Unguided

| Factor | Unguided Hydra 70 | APKWS (AGR-20A) | AGM-114 Hellfire |
|--------|-------------------|-----------------|-----------------|
| **Guidance** | None | Semi-Active Laser | Semi-Active Laser |
| **Accuracy** | ~10–50 m CEP | ~1–2 m CEP | ~1–3 m CEP |
| **Range** | 1,500–4,000 m | 1,500–5,000 m | 500–8,000 m |
| **Warhead** | Multiple (10–17 lb) | M151 HE (10 lb) | HEAT/Blast-Frag/Thermobaric (20+ lb) |
| **Maneuvering** | Fixed ballistic | Limited (~2–5°) | Full proportional navigation |
| **Fire-and-Forget** | N/A | No — laser through impact | No (SAL variants — laser through impact) |
| **Rounds per pylon** | 7 | 7 | 2 |
| **Max loadout** | 14 | 14 | 4 |
| **Target class** | Area; suppression | Point; soft to light armor | Armor; hardened; high-value |

### When to Choose APKWS

| Choose APKWS When... | Instead of... | Reason |
|---------------------|--------------|--------|
| Target is a single vehicle, fighting position, or structure | Unguided rockets | Precision required; unguided accuracy insufficient |
| Target is soft or light-armored (truck, technical, BRDM, dismounts in cover) | Hellfire | Hellfire warhead is overkill; conserve Hellfires for MBTs and hardened targets |
| Collateral damage is a constraint | Either | Small 10 lb warhead + ~1 m CEP = minimum collateral |
| Hellfire inventory is depleted | Hellfire | APKWS provides precision capability from rocket pods |
| Multiple dispersed soft targets require engagement | Hellfire | 7 APKWS per pod vs. 2–4 Hellfires per aircraft; more rounds for multiple targets |
| Target is beyond unguided effective range (> 3,000 m) | Unguided rockets | APKWS maintains precision at extended ranges where unguided accuracy collapses |

---

## Part 3 — Seeker Basket Concept

The APKWS seeker can only acquire the laser spot if it is within a cone centered on the rocket's forward axis after launch.

| Parameter | Approximate Value |
|-----------|-----------------|
| **Seeker FOV (half-angle)** | ~10° |
| **Maximum correction** | ~2–5° from boresight |
| **Implication** | Rocket must be aimed within ~5–10° of the target at launch |

### Practical Implication

If the CCIP pipper is on or very near the target at the moment of fire, the rocket is within the basket and the seeker will acquire. If the pipper is far off (pointing at terrain 100+ meters from the target), the seeker likely will not acquire — the rocket will continue on its ballistic trajectory and miss.

**APKWS is not a "fire-and-steer" weapon.** Unlike Hellfire, it cannot acquire a target that is 90° off its flight path. Aim the aircraft; then fire; then lase.

### Basket Alignment by Attack Profile

| Profile | Basket Alignment | Miss Basket Risk |
|---------|----------------|-----------------|
| **Diving fire (15°)** | Rocket trajectory passes through target area naturally | Low — dive geometry naturally aligns with ground target |
| **Running fire (level)** | Rocket arcs downward; basket sweeps across target | Moderate — must aim accurately; less margin for error |
| **Hover fire** | Rocket fired near-level at target | Moderate — shorter range helps; platform instability can shift basket |

---

## Part 4 — Weapons Page Setup & PRF Configuration

| Step | Action | Notes |
|------|--------|-------|
| 1 | Select **APKWS** on MFD weapons page | APKWS sub-page displays |
| 2 | Verify warhead type | M151 HE (standard APKWS loadout) |
| 3 | Verify APKWS count | Track rounds per pod; 7 per M260 |
| 4 | **Verify PRF code** | APKWS PRF must match MMS LRD PRF code |
| 5 | Verify MMS is tracking target in **Point Track** | Stable designation required |
| 6 | **Master Arm → ARM** when entering attack profile | ARM before reaching firing range |
| 7 | Arm laser | LASER ARMED |

> **PRF Code Discipline:** An APKWS seeker tuned to a different PRF code than the MMS laser will not acquire. This is an automatic REPEAT standard. Verify PRF match as a formal checklist step before every engagement — not as an afterthought.

---

## Part 5 — Employment Sequence

### Standard Self-Designation APKWS Engagement

| Step | Action | Notes |
|------|--------|-------|
| 1 | **Acquire target** with MMS | WFOV → NFOV; identify and confirm target type |
| 2 | **Point Track** target | MMS locked on target; crosshair stabilized |
| 3 | **Select APKWS** on weapons page | Verify count and PRF code |
| 4 | **Master Arm → ARM** | MASTER ARM annunciated |
| 5 | **Arm laser** | LASER ARMED |
| 6 | **Establish attack profile** | Diving or running fire; align aircraft on inbound heading |
| 7 | **Begin lasing target** | LASER FIRING; energy on target; reflected spot available to seeker |
| 8 | **Place CCIP pipper on or near target** | Seeker basket must include the target; CCIP accuracy matters |
| 9 | **Wait for pipper stabilization** (1–2 seconds) | Steady-state; trim; unaccelerated |
| 10 | **Fire** | Trigger press; rocket launches |
| 11 | **Maintain laser** | Continue lasing — rocket guides to spot |
| 12 | **Impact** | Observe on MMS |
| 13 | **Cease lase → BDA** | Release laser after confirmed impact |
| 14 | **Re-engage or safe** | Next target or Master Arm → SAFE |

> **Order Matters:** Laser → Aim → Fire → Maintain. The seeker activates after launch and searches for the reflected laser spot. If the laser is off when the seeker activates, it will not acquire. Laser must be active at and after the moment of launch.

---

## Part 6 — Employment Profiles

### Diving Fire (Recommended for APKWS)

| Parameter | Value |
|-----------|-------|
| **Dive Angle** | 10–15° |
| **Airspeed** | 80–100 KIAS |
| **Firing Range** | 1,500–3,000 m slant range |
| **Entry Altitude** | 800–1,200 ft AGL |
| **Break-Off** | 1,000 m / 300 ft AGL |
| **Laser** | Active before fire; maintained through impact |

Diving fire is the preferred APKWS profile. The dive naturally aligns the rocket's trajectory with the ground target, maximizing seeker basket acquisition probability. Establish the dive, trim for steady-state, lase the target, place the CCIP pipper on or near the target, then fire.

### Running Fire (Level)

| Parameter | Value |
|-----------|-------|
| **Altitude** | 200–500 ft AGL |
| **Airspeed** | 60–100 KIAS |
| **Firing Range** | 1,500–2,500 m |
| **Laser** | Active before fire; maintained through impact |

Running fire is the fallback when terrain or weather prevents a dive. Aim more carefully — the basket margin is smaller than in diving fire. Fire in single shots for each target.

### Hover Fire

| Parameter | Value |
|-----------|-------|
| **Airspeed** | 0–20 KIAS |
| **Firing Range** | 1,000–2,000 m |
| **Laser** | Active before fire; maintained through impact |
| **Notes** | Stable hover critical for basket alignment; escape route planned before firing |

---

## Part 7 — Buddy Lasing for APKWS

APKWS can home on an **external laser designation** (JTAC, FAC, wingman) when PRF codes are matched.

### Coordination Flow

| Step | External Designator (JTAC/FAC) | OH-58D Action |
|------|-------------------------------|--------------|
| 1 | Passes target description and PRF code | Acknowledge PRF; configure APKWS weapons page to matching code |
| 2 | "Laser on" / "Lasing" | Aim aircraft toward designated target area; place CCIP pipper in target area |
| 3 | Maintains laser | Verify CCIP is aligned; prepare to fire |
| 4 | Maintains laser | **"Rockets, code [PRF], firing"** — fire APKWS |
| 5 | Maintains laser through impact | Confirm laser active from external source; do not lase over them |
| 6 | "Spot out" after impact | **"Splash"** — observe BDA; report |

> **Instructor Note:** Buddy-lased APKWS requires the OH-58D pilot to still aim the aircraft toward the target area — the rocket must enter the seeker basket regardless of who is lasing. Confirm the external designator's PRF code before flight when possible. Once airborne, confirm via radio. PRF mismatch during a buddy-lase engagement is an automatic repeat.

---

## Completion Standards

The student passes this event when they can, without instructor prompting:

- [ ] Correctly choose APKWS vs. Hellfire vs. unguided rockets for a target called by the instructor, and state the rationale
- [ ] Configure the APKWS weapons page with correct PRF code and verify weapon count
- [ ] Explain the seeker basket concept and demonstrate aircraft aiming (CCIP pipper near target) as a prerequisite step before firing
- [ ] Execute the laser sequence correctly: laser active before fire, maintained through impact — **laser discipline is an automatic REPEAT if laser is released before impact**
- [ ] Execute at least 4 APKWS engagements in diving fire profile — at least 3 of 4 must result in direct hits (≤ 5 m from aimpoint)
- [ ] Execute at least 2 APKWS engagements in running or hover fire
- [ ] Demonstrate a buddy-lased engagement coordinated with instructor (simulating JTAC) using correct communication flow
- [ ] Master Arm → SAFE after each engagement sequence
- [ ] Conduct BDA after each hit; report target status

---

## Common Errors

| Error | Consequence | Correction |
|-------|-------------|------------|
| Firing without laser active | Rocket launches unguided; ballistic trajectory; miss | Verify LASER FIRING status before trigger press; laser first, then fire |
| CCIP pipper far from target at launch | Rocket outside seeker basket; fails to acquire; miss | Place CCIP pipper on or near target — APKWS requires aircraft aiming just like an unguided round |
| PRF code mismatch between MMS and APKWS | Seeker cannot acquire laser spot; round misses | PRF verification is a formal mandatory step; check before arming |
| Treating APKWS like Hellfire (fire without aiming) | APKWS cannot correct large angular errors; miss | APKWS requires aircraft pointing; it is a "smart bullet" not a "smart missile" |
| Releasing laser before impact | Rocket loses guidance in terminal phase; misses | Maintain laser through impact — identical discipline to Hellfire |
| Using APKWS against MBT or heavy armor | M151 HE insufficient; no armor penetration | Use Hellfire-K or -M for armored targets; APKWS is for soft to lightly armored targets |
| Hover fire beyond 2,000 m | Limited correction energy at extended range; degraded accuracy | Reduce range for hover fire; use diving fire for extended range precision |
| Buddy-lase without PRF coordination | Seeker tuned to wrong code; fails to acquire external spot | Confirm external PRF before firing; do not assume; verify and confirm |

---

*Based on TM 1-1520-248-10, FM 3-04.140, BAE Systems AGR-20A documentation, Polychop Simulations DCS OH-58D documentation. For simulation use only.*
