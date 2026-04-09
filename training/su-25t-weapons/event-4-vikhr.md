# Event 4 — Vikhr Anti-Tank Missile

> **Course:** Su-25T Weapons Employment | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Shkval Acquisition & Target Lock](#part-1--shkval-acquisition--target-lock)
5. [Part 2 — Single Vikhr Employment](#part-2--single-vikhr-employment)
6. [Part 3 — Multiple Engagements](#part-3--multiple-engagements)
7. [Part 4 — Launch Authorization Override](#part-4--launch-authorization-override)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Acquire and lock a vehicle target using the Shkval with correct gate sizing
- [ ] Execute a single Vikhr engagement from a valid launch window
- [ ] Maintain beam discipline (straight and level) from launch through impact
- [ ] Engage two targets in succession without losing situational awareness
- [ ] Explain when and why the Launch Authorization Override is used

---

## Ground Brief

### How the Vikhr Works

The Vikhr is a **laser beam-riding** missile. Understanding this guidance principle is critical to avoiding the most common student failure.

```
  AIRCRAFT ──[laser beam]──► TARGET
      │
      └──► Vikhr launched → looks BACKWARDS at aircraft
                           → steers to stay in center of beam
```

After launch, the missile **looks backward** at the launching aircraft to stay centered in the laser beam projected from the aircraft's nose. If the beam moves off the target — because the aircraft banks, jinks, or the Shkval gimbal is exceeded — the missile has no reference and goes ballistic.

**Beam discipline: fly straight, fly level, keep the target in the Shkval.**

### Launch Window

The Vikhr has both a minimum and maximum range, and a valid azimuth envelope.

```
                    Valid launch cone
                   /                \
                  /   Max ~8–10 km   \
                 /                    \
   [AIRCRAFT] ──────────────────────────[TARGET]
                 \                    /
                  \   Min ~800 m     /
                   \                /
```

The fire control computer displays two circles on the HUD:
- **Large outer circle:** Launch zone authorized (you are in range)
- **Small inner circle:** Laser / Shkval axis

When both circles are concentric (aligned) and you have a target lock — you have a valid shot.

---

## Pre-Mission Setup

- [ ] 4–6 static armor targets (T-72, BMP) at 2 km, 4 km, 6 km, and 8 km from initial point
- [ ] Weather: Day VMC
- [ ] **Loadout:** 2× UPK-23/250 (or no pod), 2× Vikhr rails (APU-6 × 2 = 12 total Vikhr missiles)
- [ ] No centerline pod required for this event
- [ ] Fuel: 70%

---

## Part 1 — Shkval Acquisition & Target Lock

Before flying attacks, practice Shkval acquisition on the ground at the airfield parking area.

### Shkval Procedure (Practice)

1. - [ ] **Shkval** — ON (`O`)
2. - [ ] Confirm image on IT-23M TV display (HUD inset or monitor)
3. - [ ] **Slew** toward a parked vehicle or building: `;` left, `'` right, `p` up, `/` down
4. - [ ] **Zoom in** (`numpad *`) to see target clearly
5. - [ ] **Adjust gate size** (`RCtrl + [` / `RCtrl + ]`) to fit tightly around target
   - Gate should encompass the target vehicle, not the surrounding terrain
6. - [ ] **Lock** (`Enter`) — Shkval initiates contrast tracking
7. - [ ] Observe: the gate should track the target as the aircraft moves
8. - [ ] **Break lock** (`Enter` again or `Backspace`)
9. - [ ] Practice: 5 acquisitions and locks on different targets before airborne work

**Instructor Note:** Students who skip gate sizing will lock onto background terrain. A gate set to the default (large) size will see the vehicle as a small blob inside the gate and lock on the ground texture around it. Teach: "Gate fits the vehicle — tires to turret."

---

## Part 2 — Single Vikhr Employment

### Full Attack Switchology

1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Mode** — A-G (`7`)
3. - [ ] **Select** — Vikhr pylon (`D` or pylon select page)
4. - [ ] **Shkval** — ON (`O`) if not already active
5. - [ ] **Slew** to target area, zoom in, adjust gate, **Lock** (`Enter`)
6. - [ ] **Laser** — ON (`RShift + O`) — **MANDATORY**
7. - [ ] **Confirm launch authorization:** outer circle aligns with inner circle on HUD
8. - [ ] **Fly straight and level** — establish targeting pass
9. - [ ] **Launch** (`Space`) — hold until missile leaves rail
10. - [ ] **Hold course:** wings level, ≤ 10° bank, Shkval on target until impact (~8–12 sec at 6 km)
11. - [ ] Observe impact in Shkval
12. - [ ] **Break lock, Master Arm SAFE** after confirmed impact

### Attack Profile

```
   Entry: 2,000–3,000 m MSL, 450–500 km/h
         |
   Slew Shkval to target → Zoom → Gate → Lock
         |
   Laser ON → verify LA circles aligned
         |
   Fire Vikhr → fly straight and level
         |
   Hold beam for 8–12 seconds
         |
   Impact → safe → debrief
```

### Vikhr Range vs. Altitude

| Altitude AGL | Max effective range |
|---|---|
| 500 m | ~4–5 km |
| 1,000 m | ~6 km |
| 2,000 m | ~8 km |
| 3,000 m+ | ~8–10 km |

Higher altitude extends range because the beam geometry is better. Low-altitude employment increases survivability from threats but reduces max range.

**Instructor Note:** Students often launch from maximum range at low altitude where the beam geometry barely works. Brief: "At 6 km with 800 m altitude, you are at the edge. At 4 km with 1,000 m altitude, you have a solid shot."

---

## Part 3 — Multiple Engagements

After mastering the single shot, practice engaging two targets per pass.

### Two-Shot Pass Procedure

The Vikhr fires in pairs from the two rails. After the first missile impacts:
1. - [ ] Maintain lock on original target or immediately re-slew to second target
2. - [ ] Wait for **new LA cue** (system resets after each shot)
3. - [ ] Fire second missile
4. - [ ] Hold beam until second missile impacts
5. - [ ] Break lock, egress

**Timing:** At 4 km range, impact time is ~6 seconds. You can typically fire second missile 2–3 seconds after the first.

### Target Re-Acquisition (Miss Recovery)

If a missile misses:
1. - [ ] Note where it missed (short, long, left, right)
2. - [ ] **Do not immediately re-lock** — re-establish situational awareness first
3. - [ ] Identify if target survived
4. - [ ] If target is still active: re-slew, re-lock, re-engage
5. - [ ] Do not sacrifice beam discipline trying to rush a second shot

---

## Part 4 — Launch Authorization Override

### When to Use It

The DCS Su-25T fire control is conservative about granting Launch Authorization. In some situations — especially max-range shots or head-on shots against helicopters — the system will deny LA even though the geometry is valid.

**`LAlt + W` — Launch Authorization Override**

### Appropriate Use Cases
- Target is within valid range (verify manually) but LA not granted
- Helicopter target approaching head-on at 6+ km
- Target at max range (8–9 km) from high altitude

### What It Does
Bypasses the fire control interlock. The missile **will** launch. If your geometry is wrong, the missile will miss and you have burned a round.

> **Realism Note:** In the real aircraft, the override exists for emergency close-range shots when the fire control malfunctions or the geometry is extreme. DCS players frequently use it as routine — this is not correct technique. Teach the student to **confirm range and geometry manually** before using override.

### Practice Exercise
1. - [ ] Position for a shot at 8.5 km (intentionally beyond normal LA)
2. - [ ] Observe: LA circles will not align; system denies authorization
3. - [ ] Visually confirm slant range on HUD is within Vikhr envelope (< 10 km)
4. - [ ] **Apply override** (`LAlt + W`)
5. - [ ] Fire — beam discipline as normal
6. - [ ] Note result — did range geometry support a hit?

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Shkval acquisition | Gate properly sized on 3 of 3 locks before airborne work |
| Vikhr hit (standard pass) | Hit or within 20 m on ≥ 3 of 5 single-shot passes |
| Laser discipline | Laser ON before every launch — no "cold laser" launches |
| Beam discipline | Wings level within 10° from launch to impact on every pass |
| Two-shot pass | Second missile fired correctly on ≥ 1 two-shot pass |
| Override usage | Student correctly explains criteria for override before using it |

---

## Common Errors

| Error | Correction |
|---|---|
| Laser not ON | Verify: laser step in switchology, every time |
| Gate too large — locks on ground | Adjust gate: "gate fits the vehicle" |
| Banking after launch | Brief: from launch to impact, wings level |
| Firing outside min range (< 800 m) | Missile cannot arm — abort pass if inside 1 km |
| Breaking lock to observe impact | Lock must be maintained through impact — watch in the Shkval, don't break |
| Misusing override as shortcut | Teach: verify range manually; override is a last resort, not a habit |

---

[← Event 3: Gravity Bombs](event-3-bombs.md) | [→ Event 5: Laser-Guided Missiles](event-5-laser-guided.md)

---

*Based on Eagle Dynamics DCS World documentation. For simulation use only.*
