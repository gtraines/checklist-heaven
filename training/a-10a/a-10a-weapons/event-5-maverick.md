# Event 5 — AGM-65 Maverick

> **Course:** A-10A Weapons Employment | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — IR Maverick Employment (AGM-65D)](#part-1--ir-maverick-employment-agm-65d)
5. [Part 2 — TV Maverick Employment (AGM-65H)](#part-2--tv-maverick-employment-agm-65h)
6. [Part 3 — Heavy Maverick Employment (AGM-65K/G)](#part-3--heavy-maverick-employment-agm-65kg)
7. [Part 4 — Multiple Target Engagement](#part-4--multiple-target-engagement)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Power on, slew, and lock an AGM-65D (IR) Maverick against a vehicle target and achieve a hit
- [ ] Employ an AGM-65H (TV) Maverick against a high-contrast target in daylight
- [ ] Select the correct Maverick variant for target type and lighting conditions
- [ ] Engage two targets sequentially with Mavericks on a single pass
- [ ] Explain why IR Mavericks require cooldown time and how polarity affects acquisition

---

## Ground Brief

### The AGM-65 Maverick — Fire and Forget

The Maverick is the A-10A's primary precision standoff weapon. Unlike guided bombs, it carries its own seeker and guides itself to the target after launch. **You do not need to maintain a lock or illumination after firing** — break off immediately and re-attack or egress.

This makes the Maverick the safest precision weapon for the A-10A: fire from 4–8 NM, turn away, and the missile does the rest.

### Seeker Comparison

| Feature | IR (AGM-65D/G) | TV (AGM-65H/K) |
|---|---|---|
| Sensor | Imaging Infrared | CCD Television (Electro-Optical) |
| Night capable | **Yes** | No |
| Dawn/Dusk | Yes | Degraded |
| Overcast day | Yes | Yes |
| Cooldown required | **Yes (3–5 min)** | No |
| Polarity switch | Yes (White/Black Hot) | N/A |
| Lock mechanism | IR contrast | Visual contrast |
| Affected by | Cold targets, rain | Low light, shadows |

### Variant Selection Guide

| Target | Lighting | Recommended |
|---|---|---|
| MBT / IFV (moving, engines hot) | Day | AGM-65D or AGM-65H |
| MBT / IFV (moving, engines hot) | Night | **AGM-65D** (only option) |
| SAM launcher (active) | Any | AGM-65D (heat from radar/engine) |
| Bridge / building | Day | **AGM-65K** (TV, heavy warhead) |
| Bridge / building | Night | **AGM-65G** (IR, heavy warhead) |
| Ship / large structure | Day | AGM-65K or AGM-65G |
| Truck / soft vehicle | Day | AGM-65H (light warhead sufficient) |

### Launch Envelope

| Variant | Min Range | Max Range | Notes |
|---|---|---|---|
| AGM-65D (IR) | ~500 m | 6–8 NM | Best precision at 4–6 NM |
| AGM-65G (IR Heavy) | ~500 m | 6–8 NM | Same seeker as D, heavier warhead |
| AGM-65H (TV) | ~500 m | 4–6 NM | Daylight contrast dependent |
| AGM-65K (TV Heavy) | ~500 m | 6–10 NM | Extended range, daylight only |

---

## Pre-Mission Setup

- [ ] Place 4 armor targets (T-72/T-80) at varied ranges: 3, 5, 7 NM from initial point
- [ ] Place 1 hardened building (command post or bunker)
- [ ] Weather: Day VMC (Part 1–3); repeat Part 1 at dusk/night if possible
- [ ] **Loadout:**
  - 2× AGM-65D (IR) — inboard wing pylons
  - 2× AGM-65H (TV) — outboard wing pylons
  - 2× AGM-65K (TV Heavy) — additional pylons
  - Gun: 1,174 rounds (for BDA / follow-up)
- [ ] Fuel: 70%
- [ ] **Power on Mavericks immediately after engine start** — IIR variants need 3–5 min cooldown

---

## Part 1 — IR Maverick Employment (AGM-65D)

### Seeker Warm-Up

Before any AGM-65D employment:
1. - [ ] Cycle to AGM-65D station (`D`) immediately after startup
2. - [ ] Seeker begins cooldown — **wait 3–5 minutes**
3. - [ ] Seeker image will be noisy/grainy initially, then clear
4. - [ ] Once image is clear with distinct vehicle thermal signatures — seeker is ready

> **Critical:** If you launch an IR Maverick before the seeker has cooled, the lock will be unreliable and the missile may lose track. Always wait for a clear seeker image.

### Switchology

1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Weapon Select** — cycle to AGM-65D (`D`)
3. - [ ] Confirm seeker image is displayed (IR view of terrain ahead)
4. - [ ] **Slew** seeker to target area: `Numpad 8` (up), `Numpad 2` (down), `Numpad 4` (left), `Numpad 6` (right)
5. - [ ] **Identify target** — confirm VID (Rule 1: positive target identification)
6. - [ ] **Lock** on target: `Numpad Enter`
7. - [ ] Confirm: seeker gate squares on target and tracks it
8. - [ ] Verify lock is on the **intended target**, not a terrain feature or decoy
9. - [ ] **Fire** (`Space`)
10. - [ ] **Break off** immediately — fire-and-forget

### Attack Profile

```
  Entry: 8,000–12,000 ft MSL, 300–350 kts
         |
  Cycle to AGM-65D → seeker image active
         |
  Slew to target area → zoom/pan → identify target
         |
  Lock → confirm tracking → fire
         |
  Immediate break — turn off threat axis
         |
  Cycle to next Maverick for re-attack (if applicable)
```

### IR Polarity

The AGM-65D displays in one of two polarities:
- **White Hot:** Hot objects appear bright white against dark background
- **Black Hot:** Hot objects appear dark against bright background

Switch polarity if the target blends into the background in one mode. In DCS, the polarity switch varies by control binding — check your configuration.

**When to switch:**
- Target near water or wet terrain → try White Hot (water appears cold/dark)
- Target in desert or sun-heated terrain → try Black Hot (reduces background clutter)

### IR Seeker Limitations

| Condition | Effect |
|---|---|
| Target engine running (hot) | Strong signature — easy acquisition |
| Target engine cold (parked) | Weak signature — may be invisible to seeker |
| Rain / heavy moisture | IR attenuation — reduced range |
| Sun-heated terrain (midday) | Background clutter — harder to distinguish targets |

---

## Part 2 — TV Maverick Employment (AGM-65H)

The TV Maverick uses a CCD camera to lock onto visual contrast. It does not require cooldown and provides a clear visual image in daylight.

### Switchology

Same as AGM-65D, substituting the TV variant:
1. - [ ] **Master Arm** — ON (`O`)
2. - [ ] **Weapon Select** — cycle to AGM-65H (`D`)
3. - [ ] Confirm seeker image is displayed (video feed — terrain ahead)
4. - [ ] **Slew** to target: `Numpad 8/2/4/6`
5. - [ ] **Identify target** — TV image is clearer than IR for visual identification
6. - [ ] **Lock**: `Numpad Enter`
7. - [ ] Confirm tracking gate on target
8. - [ ] **Fire** (`Space`) — fire and forget
9. - [ ] Break off

### TV Seeker Advantages

- No cooldown required — ready immediately
- Clearer image in daylight — easier visual identification
- Works against cold targets (visual contrast, not heat)

### TV Seeker Limitations

- **Daylight only** — completely blind at night
- Degraded in shadows, haze, or low sun angle
- Requires visual contrast — a green vehicle on green grass may not lock
- Shorter range than IR variants (4–6 NM vs. 6–8 NM)

### Practice: IR vs. TV Comparison

1. - [ ] Acquire the same target with AGM-65D (IR), note the seeker image
2. - [ ] Cycle to AGM-65H (TV), acquire the same target, note the seeker image
3. - [ ] Compare: which seeker gives a clearer picture? Which locks faster?
4. - [ ] Answer: it depends on conditions — this is why you carry both

---

## Part 3 — Heavy Maverick Employment (AGM-65K/G)

The K (TV, heavy) and G (IR, heavy) variants carry a 300 lb blast/fragmentation warhead — more than double the standard 125 lb shaped charge. They are reserved for high-value targets.

### When to Use Heavy Variants

| Target | Standard (D/H) | Heavy (G/K) |
|---|---|---|
| Single tank | Sufficient | Overkill |
| APC / IFV | Sufficient | Overkill |
| Bridge span | Insufficient | **Required** |
| Bunker / C2 facility | Marginal | **Required** |
| Ship | Insufficient | **Required** |
| SAM radar vehicle | Sufficient | Acceptable |

### Employment: Hardened Target (Building)

1. - [ ] **Weapon Select** — cycle to AGM-65K (`D`)
2. - [ ] Slew seeker to building target
3. - [ ] **Aim for the structure center** — the 300 lb warhead needs a direct hit for maximum effect
4. - [ ] Lock and fire as per standard Maverick procedure
5. - [ ] **AGM-65G at night:** Same procedure, using IR seeker — the building's heat signature (even ambient) is sufficient for lock

### Heavy Warhead Notes

- The AGM-65K has the longest effective range (6–10 NM) of all A-10A Mavericks due to its larger motor
- Do not waste heavy variants on soft targets that a standard Maverick can kill
- Plan loadout: 2× standard for armor, 2× heavy for structures/ships

---

## Part 4 — Multiple Target Engagement

The Maverick's fire-and-forget capability enables rapid engagement of multiple targets on a single pass.

### Two-Target Pass Procedure

1. - [ ] Enter at 10,000 ft MSL, 350 kts, targets at 6–8 NM
2. - [ ] Cycle to first Maverick → slew → identify → lock → **fire**
3. - [ ] Immediately cycle to next Maverick (`D`)
4. - [ ] Slew to second target → identify → lock → **fire**
5. - [ ] Break off and egress

### Timing

At 6 NM closing at 350 kts, you have approximately 60 seconds before reaching minimum range. A skilled operator can lock and fire two Mavericks in 15–20 seconds, leaving ample time to egress.

### Rapid Engagement Tips

- **Pre-plan target assignments:** Know which Maverick goes to which target before entering the attack area
- **Slew to approximate target area first, then fine-tune** — don't start searching from the default seeker position
- **Lock only when certain** — a bad lock on the first shot wastes time and may send a missile into friendly territory
- **Don't rush the second shot** — if you can't identify the second target, egress with the missile still on the rail. A live Maverick on the jet is better than a fratricide

---

## Completion Standards

| Standard | Requirement |
|---|---|
| AGM-65D (IR) hit | Impact on or within 10 m of target on ≥ 2 of 3 shots |
| AGM-65H (TV) hit | Impact on target on ≥ 2 of 3 shots |
| Seeker cooldown | IR Mavericks powered on ≥ 3 minutes before first shot |
| Target identification | Positive VID confirmed on every shot — no blind launches |
| Variant selection | Correct variant selected for target type and conditions |
| Two-target pass | Both missiles hit on ≥ 1 of 2 two-target passes |
| Heavy Maverick selection | AGM-65K/G used only on hardened/heavy targets |
| Master Arm discipline | SAFE after every engagement |

---

## Common Errors

| Error | Correction |
|---|---|
| Firing IR Maverick before cooldown | Power on Mavericks at startup; wait for clear seeker image |
| Locking on terrain instead of target | Slew carefully; confirm VID before lock — look for vehicle shape |
| Using TV Maverick at night | AGM-65H/K are daylight only; switch to AGM-65D/G for low-light |
| Heavy Maverick on soft targets | Save K/G for bunkers, bridges, ships; use D/H for vehicles |
| Not breaking off after launch | Maverick is fire-and-forget — turn away immediately after launch |
| Rushing second shot on two-target pass | Take the time for positive VID; egress with a live missile if unsure |
| Firing inside minimum range (<500 m) | Seeker may not track; missile motor may not arm properly |

---

[← Event 4: Cluster Munitions](event-4-cluster-munitions.md) | [→ Event 6: Check Ride](event-6-check-ride.md)

---

*Based on T.O. 1A-10A-34-1-1 and Eagle Dynamics DCS World documentation. For simulation use only.*
