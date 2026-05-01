# Event 1 — Weapons Systems & Academics

> **Course:** UH-1H Huey Weapons Employment Course | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents

1. [Learning Objectives](#learning-objectives)
2. [Part 1 — Weapons Inventory & Station Configuration](#part-1--weapons-inventory--station-configuration)
3. [Part 2 — Cockpit Armament Panel & Controls](#part-2--cockpit-armament-panel--controls)
4. [Part 3 — Arming & Safe Procedures](#part-3--arming--safe-procedures)
5. [Part 4 — Sight Systems & Ballistic Fundamentals](#part-4--sight-systems--ballistic-fundamentals)
6. [Part 5 — Weight, Performance & Loadout Planning](#part-5--weight-performance--loadout-planning)
7. [Part 6 — Weapons Malfunctions (Academic)](#part-6--weapons-malfunctions-academic)
8. [Completion Standards](#completion-standards)
9. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:

- [ ] Identify all weapons available on the DCS UH-1H by name, type, station, and primary target type
- [ ] Identify every switch on the cockpit armament panel by name and function; describe the two-click guard/switch sequence for Master Arm
- [ ] Recite the arming checklist and safe checklist from memory, in correct order, without prompting
- [ ] Explain what the AN/M2A1 sight depression setting controls, and why an airspeed error produces a range error at impact
- [ ] Given an attack airspeed and range from the ballistic table, state the correct depression setting
- [ ] State the danger close distances for each weapon system
- [ ] Describe the immediate action for: rocket misfire, M134 stoppage, M60D stoppage (SPORTS drill), and suspected hangfire
- [ ] State the performance impact of a full gunship loadout (2× XM-159 + door guns) versus a clean configuration at sea level

---

## Part 1 — Weapons Inventory & Station Configuration

### Weapons Available on the DCS UH-1H

The DCS UH-1H supports four weapon systems across four stations. All forward-firing weapons are **unguided** — there is no CCIP, no laser, no targeting sensor. The pilot aims using the AN/M2A1 optical sight and knowledge of ballistics.

| Weapon | Type | Station | Primary Target | Notes |
|---|---|---|---|---|
| XM-158 (7-tube launcher) | 2.75-inch FFAR rockets | Left or right pylon | Personnel, light vehicles | 7 tubes; lighter load |
| XM-159 (19-tube launcher) | 2.75-inch FFAR rockets | Left or right pylon | Area suppression, LZ prep | 19 tubes; heavier; higher ammo capacity |
| M134 Minigun pod | 7.62×51mm, 6-barrel rotary | Left or right pylon | Personnel, light vehicles, trench lines | Pilot-aimed; fixed forward |
| M60D Door Gun (port) | 7.62×51mm, single-barrel | Port (left) door | Flanking targets, personnel | Crew-aimed; flexible mount |
| M60D Door Gun (starboard) | 7.62×51mm, single-barrel | Starboard (right) door | Flanking targets, personnel | Crew-aimed; flexible mount |

**Key point:** The M60D door guns operate **independently** of the armament panel and Master Arm circuit. They require no pilot arming action — only crew station access and trigger press. The forward-firing weapons (rockets, M134) **all require** Master Arm ARM before they can fire.

### Rocket Warhead Options (DCS-Modeled)

| Designation | Type | Primary Use |
|---|---|---|
| M151 HE | High explosive, 10 lb | Anti-personnel, light vehicles; burst radius ~10 m lethal |
| M229 HE | High explosive, 17 lb | Light vehicles, structures; burst radius ~15 m lethal |
| M156 WP | White phosphorus | Target marking, obscurant; burns ~60 sec |
| M257 Illum | Parachute illumination flare | Night area illumination; burns ~100 sec |

> *Flechette (M255) and anti-armor HEAT (M247) rounds are not modeled in DCS. Train with the four listed warheads only.*

### Station Configuration Rules

- One weapon type per pylon — you cannot stack rockets and minigun on the same pylon.
- Pylons may be loaded with different types (e.g., M134 left + XM-159 right). This is the standard mixed gunship load.
- Door guns are always available if the crew station is occupied — they are not affected by pylon loadout choices.

### Typical Loadout Configurations

| Configuration | Left Pylon | Right Pylon | Use Case |
|---|---|---|---|
| Clean | Empty | Empty | Maximum performance; door guns only |
| Light rockets | XM-158 | XM-158 | Light attack; minimal performance penalty |
| Heavy rockets | XM-159 | XM-159 | LZ prep; area suppression; significant weight |
| Minigun only | M134 | M134 | Sustained gun suppression; no rockets |
| Mixed (standard gunship) | M134 | XM-159 | Versatile; rockets for range, gun for close-in |
| Full gunship | XM-159 | XM-159 | Maximum firepower; greatest performance cost |

---

## Part 2 — Cockpit Armament Panel & Controls

### Panel Location

The armament panel is on the **right subpanel**, below and right of the main instrument cluster, within easy right-hand reach of the pilot. In DCS, every switch on the panel is left-click interactive.

### Switch-by-Switch Description

**Master Arm Switch (upper left of panel)**
- Two positions: **SAFE** (down) and **ARM** (up).
- Protected by a spring-loaded guard that must be lifted before the switch can be moved to ARM.
- DCS: **two clicks required** — first click lifts the guard; second click throws the switch.
- Without Master Arm in ARM, the rocket and minigun firing circuit is open — weapons cannot fire.
- Door guns are **not** controlled by Master Arm.

**Weapon Select Switch (center of panel)**
- Positions: **SAFE** / **ROCKETS** / **GUNS** / **ROCKETS AND GUNS**
- SAFE: firing circuit open regardless of Master Arm position.
- ROCKETS: routes trigger to rocket launchers on loaded pylons.
- GUNS: routes trigger to M134 pod(s) if loaded.
- ROCKETS AND GUNS: simultaneous fire of both.

**Fire Mode / Intervalometer (lower panel)**
- **SINGLE**: one rocket fires per trigger pull.
- **PAIRS**: one rocket per loaded pylon per trigger pull (two rockets total if both pylons loaded).
- No distinct "RIPPLE" mode in DCS — holding trigger with PAIRS fires in pairs continuously.

**Jettison Panel (center console)**
- Separate from the main armament panel.
- Cover must be lifted before the jettison switch can be actuated.
- Actuating jettison drops all pylon stores simultaneously.
- Use only in emergency: aircraft distress, weapons hazard, or emergency landing.

### Pilot Weapons Controls on Cyclic

- **Primary trigger**: right index finger; fires the selected weapon when Master Arm is ARM.
- **DCS default**: `Space` key; should be remapped to HOTAS trigger for operational use.
- There is **no quick-safe on the cyclic** — the pilot must reach the armament panel to safe the system.
- Force trim (`T` hold / `LCtrl + T`) does **not** inhibit weapons fire.

### DCS Keybind Summary

| Function | Default Keybind | Location |
|---|---|---|
| Master Arm ARM/SAFE | Mouse click (two-click) | Armament panel upper left |
| Weapon select | Mouse click (rotate) | Armament panel center |
| Fire mode select | Mouse click | Armament panel lower |
| Weapons fire | `Space` | Cyclic trigger |
| Emergency jettison | Mouse click (two-click) | Center console jettison panel |
| Port door gun station | `F5` (verify in controls) | View/seat menu |
| Starboard door gun station | `F6` (verify in controls) | View/seat menu |
| NVG toggle | `` ` `` (backtick) | — |

> *All keybinds: verify against current DCS UH-1H input settings before flying. See dossier Appendix for the full table.*

---

## Part 3 — Arming & Safe Procedures

These checklists must be memorized. They are executed verbally before every attack run and after every engagement. No attack begins without completing the arming checklist.

### Weapons Hot (Arming Checklist)

Execute upon entering the engagement area or when cleared hot by IP/controller.

1. **Weapon selector** — SET (ROCKETS / GUNS / ROCKETS AND GUNS — per mission plan)
2. **Fire mode selector** — SET (SINGLE or PAIRS — per mission plan)
3. **Master Arm guard** — LIFT
4. **Master Arm switch** — ARM
5. **Armament panel** — SCAN (verify selector and mode match the plan)
6. **Crew** — *"Weapons hot, engaging [target description]"*
7. **Sight** — HEAD ON SIGHT (verify eye relief; reticle visible)

### Weapons Safe (Post-Engagement Checklist)

Execute immediately after the last round fires or on any abort.

1. **Trigger** — RELEASE
2. **Master Arm** — SAFE
3. **Master Arm guard** — LOWER
4. **Weapon selector** — SAFE
5. **Crew** — *"Weapons safe"*
6. **Jettison panel** — CONFIRM COVER CLOSED

> **Instructor note:** The safe checklist must be the student's immediate reflex after trigger release. Master Arm must go to SAFE before any other action — before BDA, before turning, before radio calls. Drill this sequence until it is automatic.

### Danger Close Distances (Memory Item)

| Weapon | Danger Close |
|---|---|
| 2.75-inch FFAR (M151/M229 HE) | **230 meters** from friendly forces |
| M156 WP | **300 meters** from friendly forces |
| M134 Minigun (7.62mm) | **200 meters** from friendly forces |
| M60D Door Gun (7.62mm) | **200 meters** from friendly forces |

Any engagement within these distances requires the ground commander's explicit acceptance of risk and a verbal readback by the pilot before firing.

---

## Part 4 — Sight Systems & Ballistic Fundamentals

### The AN/M2A1 Optical Sight

The DCS UH-1H uses a **fixed-mount optical deflection sight** on a pedestal above the instrument panel center. This sight:

- Is **NOT** a computing sight — it receives no airspeed, altitude, or sensor inputs.
- Projects a reticle with a center aiming point and mil graduation marks.
- Has an adjustable depression setting (mils below the aircraft's longitudinal axis) — adjusted via mouse wheel on the sight's depression knob.
- Is calibrated by the pilot to match the attack airspeed and slant range using the ballistic tables.

**What depression controls:** The depression angle tells the sight where to point relative to the aircraft's nose. At the correct depression for a given airspeed and range, the rocket's ballistic arc will carry it from the muzzle to the aim point at the intended impact. If the depression is too shallow (less mils), the sight points too high — the pilot fires too early and the rockets land short. If the depression is too steep (more mils), the pilot fires too late and rockets land long.

### Why Airspeed Discipline Matters

The ballistic tables assume a specific airspeed at rocket launch. At 80 KIAS and 1,000 m range, the forward throw of the rocket (distance the aircraft travels during rocket time of flight) is approximately 53 meters. If the pilot is 10 KIAS fast, the forward throw increases by ~7 m — rounds impact proportionally long. At 15 KIAS error, the range error at 1,000 m is approximately 30–60 meters.

**Rule:** Stabilize airspeed **before** roll-in. Do not adjust depression during the run to correct for an airspeed error — break off, correct airspeed, and re-attack.

### Ballistic Table — Key Depression Values (Memory Aids)

Students should memorize the primary training values. Full table is in the dossier (Module 3, Tables 3.3-A/B/C).

**Level fire (0° dive):**

| Airspeed (KIAS) | Range (m) | Depression (mils) |
|---|---|---|
| 60 | 800 | 38 |
| 80 | 800 | 35 |
| 80 | 1,000 | 41 |
| 100 | 1,000 | 38 |

**Diving attack (10° dive):**

| Airspeed (KIAS) | Range (m) | Depression (mils) |
|---|---|---|
| 80 | 800 | 26 |
| 80 | 1,000 | 32 |
| 100 | 1,000 | 28 |
| 100 | 1,200 | 34 |

### Target Acquisition — Visual Technique

Without sensors, target acquisition requires disciplined scanning:

1. Scan in 10° sectors left to right; pause 1–2 seconds per sector.
2. Look for movement first, then shape/contrast, then muzzle flash or dust.
3. Assign scan sectors to crew: pilot — forward 180°; port gunner — left 90–270°; starboard gunner — right 90–270°.
4. Never sustain external scan for > 20 seconds without an instrument cross-check at low altitude.

**Door gunner target call format:**
> *"Pilot, [position] — [o'clock], [distance], [description], [remarks]."*
> *"Pilot, right door — 3 o'clock, 800 meters, truck convoy, north side of road."*

Pilot response: *"Tally"* (target acquired) or *"No joy — talk me on"* (cannot find target).

---

## Part 5 — Weight, Performance & Loadout Planning

### Weapons Weight (Approximate)

| Item | Weight |
|---|---|
| XM-159 loaded (19 rockets) | ~95 kg (210 lb) |
| XM-158 loaded (7 rockets) | ~40 kg (88 lb) |
| M134 pod (1,500 rounds) | ~115 kg (253 lb) |
| M60D door gun + 400 rounds | ~15 kg (33 lb) per gun |

### Performance Impact by Loadout

| Loadout | Total Weapons Weight | IGE Hover Ceiling (Standard Day) | OGE Hover Ceiling |
|---|---|---|---|
| Clean | ~30 kg | ~12,000 ft DA | ~6,000 ft DA |
| 2× XM-158 | ~110 kg | ~11,000 ft DA | ~5,500 ft DA |
| 2× XM-159 | ~220 kg | ~9,500 ft DA | ~4,500 ft DA |
| Full gunship (2× XM-159) | ~250 kg | ~8,500 ft DA | ~3,500 ft DA |

### Pre-Departure Hover Check (With Weapons)

Before every armed departure:

1. Hover IGE at 3–5 ft AGL.
2. Read torque gauge.
3. If torque > 35–38 PSI to maintain hover: performance is marginal — reduce load or abort.
4. If torque > 40 PSI at IGE hover: abort; reduce load (fuel, ammunition, or stores).

### Density Altitude Planning

- High DA reduces engine power and lowers hover ceiling.
- For DA > 3,000 ft: use XM-158 instead of XM-159; consider clean loadout for single-aircraft ops.
- Always verify power margin with a hover check before committing to a loaded armed departure at elevated DA.

---

## Part 6 — Weapons Malfunctions (Academic)

These procedures are academic for this event. Practical application is integrated into subsequent flight events via Mission Editor-triggered failures.

### Misfire (No Ignition)

1. Release trigger.
2. Weapon selector — SAFE.
3. Wait 30 seconds (in case of delayed ignition — hangfire risk).
4. If no firing after 30 seconds: safe Master Arm; continue mission on remaining weapons.
5. Land at first opportunity; brief ground crew.

**Do not:** point the aircraft at friendly forces or another aircraft during the wait period.

### Hangfire (Delayed Ignition)

A rocket ignites after an unpredictable delay following the trigger press — seconds to minutes after the firing signal.

- **Do not** maneuver toward friendly forces during any misfire wait period.
- Treat every misfire as a potential hangfire for the full 30-second wait.
- DCS does not model true hangfire delay — this is academic knowledge for real-world safety awareness.

### M134 Minigun Stoppage

1. Release trigger.
2. Weapon selector — SAFE.
3. Check armament panel circuit breakers.
4. After 5–10 seconds, attempt to re-engage.
5. After two failed attempts: declare minigun inoperative; select alternative weapon.

### M60D Door Gun Stoppage — SPORTS

**S** — Slap the feed tray to ensure belt seating  
**P** — Pull the charging handle rearward  
**O** — Observe the chamber for clear/jam  
**R** — Release the charging handle  
**T** — Tap (confirm bolt in battery)  
**S** — Shoot — attempt to fire

### Suspected Unsafe Weapons (Master Arm Will Not Safe)

- Treat aircraft as loaded and armed.
- Do not point at friendly forces or aircraft.
- Land at the first available site; do not troubleshoot in flight.

---

## Completion Standards

This is a ground event — no flying. The student must pass all of the following before proceeding to Event 2:

| Standard | Criterion |
|---|---|
| Oral — weapons inventory | Name, type, station, and primary target for all five weapons without notes |
| Oral — armament panel | Describe every switch by name, position, and function; describe two-click Master Arm sequence |
| Recitation — arming checklist | 7-step arming checklist in correct order from memory; no prompts |
| Recitation — safe checklist | 6-step safe checklist in correct order from memory; first step must be "Master Arm SAFE" |
| Oral — ballistic fundamentals | Explain why airspeed error causes range error; give the correct depression for 80 KIAS, 1,000 m, 10° dive (answer: 32 mils) |
| Oral — danger close | State danger close distances for all four weapons without notes |
| Oral — malfunction procedures | State immediate action for misfire, M134 stoppage, and M60D SPORTS drill without notes |
| Oral — weight/performance | State the pre-departure hover check procedure; state what torque value triggers an abort |

> **IP note:** This event should run 60–90 minutes as a structured oral with the student referring to the ballistic table card. By the end, the student must close the card and demonstrate from memory. All eight standards must pass before Event 2 is authorized.

---

## Common Errors

| Error | Correction |
|---|---|
| Confusing Master Arm with weapon selector | Reinforce: Master Arm enables the circuit; weapon selector directs the circuit. Both must be set correctly |
| Arming checklist in wrong order (selector before guard lift) | Drill sequence until reflexive: selector → mode → guard lift → ARM → scan → crew call |
| Stating danger close for rockets as "300 meters" (WP value) | Review table; M151/M229 HE danger close is 230 m; WP is 300 m — different values |
| Stating SPORTS for rocket misfire | SPORTS is M60D door gun only; rocket misfire = safe + 30-second wait |
| Cannot explain depression/airspeed relationship | Use the analogy: the ballistic table is the "recipe" — change one ingredient (airspeed) and the result changes |

---

*Based on TM 55-1520-210-10, TM 55-1520-210-CL, FM 3-04.140, and Eagle Dynamics / Belsimtek DCS UH-1H module documentation. For simulation use only.*
