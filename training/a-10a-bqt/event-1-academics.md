# Event 1 — Aircraft Systems & Academics

> **Course:** A-10A Basic Qualification Training | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Aircraft Overview](#aircraft-overview)
3. [Propulsion — TF34-GE-100 Engines](#propulsion--tf34-ge-100-engines)
4. [Flight Control System](#flight-control-system)
5. [Fuel System](#fuel-system)
6. [Survivability Features](#survivability-features)
7. [AOA Indexer & Stall Characteristics](#aoa-indexer--stall-characteristics)
8. [Operating Limitations](#operating-limitations)
9. [Emergency Procedures (Academic)](#emergency-procedures-academic)
10. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] State the key characteristics of the TF34-GE-100 engine including thrust, spool-up time, and EGT limits
- [ ] Describe the dual-redundant hydraulic flight control system and explain manual reversion
- [ ] Explain the A-10A fuel system feed sequence and low-fuel indications
- [ ] Identify the major survivability features of the A-10A and their operational implications
- [ ] Describe AOA indexer indications and stall onset characteristics
- [ ] Recite the three critical operating limitations (max weight, G-limit, AoA limit) from memory
- [ ] State the correct immediate action response to engine fire, single-engine failure, and hydraulic failure

---

## Aircraft Overview

The A-10A "Thunderbolt II" — universally known as the "Warthog" — is a dedicated close air support aircraft designed from the ground up around the 30mm GAU-8/A Avenger cannon. It is slow, heavily armed, and extraordinarily survivable.

### Key Characteristics vs. Other DCS Aircraft

| Characteristic | A-10A | Su-25T | Operational Implication |
|---|---|---|---|
| **Engine Type** | High-bypass turbofan | Turbojet | A-10A spools faster; much quieter |
| **Max Speed** | ~380 KTAS (low alt) | ~500 KTAS | A-10A is significantly slower |
| **Stall Speed (dirty)** | ~110 KIAS | ~145 km/h | Similar dirty stall speeds |
| **Cockpit (DCS)** | Simplified FC3 | Full-fidelity | No clickable cockpit in A-10A |
| **Flight Model** | Advanced (AFM) | Advanced (AFM) | Both have realistic aerodynamics |
| **Redundancy** | Exceptional | Moderate | A-10A can fly with severe battle damage |

**Instructor Note:** The A-10A is not a fast jet. Students with prior fast-jet experience will feel it is painfully slow. Frame the aircraft's strengths correctly: unmatched survivability, precision loiter capability, and the most powerful cannon ever mounted on an aircraft.

---

## Propulsion — TF34-GE-100 Engines

### Engine Specifications

| Parameter | Value |
|---|---|
| Engine Model | General Electric TF34-GE-100 |
| Type | High-bypass turbofan (6.2:1 bypass ratio) |
| Thrust (per engine) | 9,065 lbf (40.32 kN) |
| Total Installed Thrust | ~18,130 lbf (both engines) |
| Idle RPM (N2) | ~55–60% |
| Max RPM (N2) | 100% (no afterburner) |
| EGT Limit — Start | 649°C / 1,200°F |
| EGT Limit — Continuous | 607°C / 1,125°F |
| Min Oil Pressure | 15 PSI |
| Fuel Flow (cruise, both) | ~1,800–2,200 lbs/hr |
| Fuel Flow (max power) | ~3,000–3,500 lbs/hr |

### Spool-Up Characteristics

The TF34's high-bypass design provides a **significant advantage over turbojets**: spool-up from idle to military (max) power takes approximately **4–6 seconds**. This is meaningfully faster than the Su-25T's R-195 (9–12 seconds), but pilots must still anticipate power requirements — do not wait until the aircraft is slow and sinking before adding power.

**On final approach:** The correct technique is to set power on base leg and make **small, anticipatory adjustments** throughout the approach. Reacting to low airspeed on short final with a power addition will produce 4–6 seconds of lag before useful thrust arrives.

> *⚠ Realism Divergence: Real A-10A pilots monitor individual N1/N2 RPM gauges, EGT, oil pressure, and fuel flow on analog cockpit instruments. In DCS FC3, these parameters are shown in a simplified digital overlay. The behavior of hot starts and hung starts is modeled, but the pilot cannot interact with engine controls beyond throttle position.*

---

## Flight Control System

The A-10A uses a **dual-redundant hydraulic flight control system** with a unique manual reversion backup that no other modern combat jet offers.

| System | Description |
|---|---|
| **Primary Hydraulic** | Left + Right systems, 3,000 PSI each |
| **Manual Reversion** | Direct mechanical linkage; all surfaces controllable without hydraulics |
| **Control Surfaces** | Ailerons, elevators, rudders, split speed brakes |
| **Trim** | Electric pitch, roll, and rudder trim |
| **Flap Positions** | UP / MVR (7°) / DN (20°) |
| **Speed Brakes** | Split surfaces on aft fuselage |

### Manual Reversion

The A-10A is one of very few modern combat jets that remains fully controllable with **both hydraulic systems failed**. In manual reversion:
- Stick forces increase dramatically (60–80 lbs estimated in the real aircraft)
- Aircraft remains flyable but sluggish
- Precision maneuvering is very difficult
- DCS models the increased control lag and reduced authority

> *⚠ Realism Divergence: DCS cannot model physical stick forces. The flight model does correctly increase control response lag and reduce control authority in manual reversion.*

### Trim System

**Every significant speed or configuration change requires trim adjustment.** The A-10A has no fly-by-wire stability augmentation.

| Trim Action | DCS Keybind |
|---|---|
| Pitch Trim Up (nose up) | `RCtrl + ;` |
| Pitch Trim Down (nose down) | `RCtrl + .` |
| Roll Trim Left | `RCtrl + ,` |
| Roll Trim Right | `RCtrl + /` |
| Rudder Trim Left | `RCtrl + Z` |
| Rudder Trim Right | `RCtrl + X` |

**Instructor Note:** Students who "fight the stick" without trimming will fly imprecise profiles and fatigue quickly. The mantra for this aircraft is the same as the Su-25T: **Trim for speed. Trim early. Trim often.**

---

## Fuel System

| Parameter | Value |
|---|---|
| Internal Fuel Capacity | ~10,700 lbs (~1,600 US gal) |
| External Tanks (optional) | 2 × 600 US gal (stations 3 and 9) |
| Feed Sequence | Wing tanks → Fuselage feeder cells (automatic) |
| Low Fuel Warning | ~1,500 lbs remaining |
| Bingo Fuel (RTB planning) | ~2,500–3,000 lbs (mission dependent) |

- **Self-Sealing Tanks:** Internal tanks are foam-filled and self-sealing; designed to survive 23mm HEI cannon hits.
- **No Fuel Dump:** The A-10A cannot dump fuel. If overweight for landing, burn off fuel or jettison stores.

> *⚠ Realism Divergence: Real pilots manage fuel balance manually via a cockpit crossfeed switch. DCS FC3 auto-manages fuel and shows only total fuel remaining.*

---

## Survivability Features

| Feature | Description | Operational Impact |
|---|---|---|
| **Titanium Bathtub** | ~1,200 lb titanium enclosure around cockpit | Protects pilot from 23mm fire |
| **Redundant Hydraulics** | Two independent systems | One system loss = full control retained |
| **Manual Reversion** | Mechanical backup | Fly-home after total hydraulic failure |
| **Wide Engine Spacing** | Nacelles far apart on aft fuselage | One engine loss = manageable asymmetric flight |
| **Self-Sealing Fuel** | Foam-filled tanks | Resist fuel fire after battle damage |
| **ACES II Seat** | Zero-zero capable ejection | Safe ejection at any altitude and speed |
| **Structural Redundancy** | Overlapping spars, multi-path load structures | Can lose significant wing/tail area and continue |

---

## AOA Indexer & Stall Characteristics

### AOA Indexer

The AOA (Angle of Attack) indexer is a three-light system on the left canopy bow. It is the **primary reference for approach and landing** — use it instead of airspeed for final approach.

| Light | Symbol | State | Action |
|---|---|---|---|
| **Green** | ○ (Donut) | On-speed — correct AoA | Maintain |
| **Amber (upper)** | △ (Chevron Up) | Slow / High AoA | Add power; lower nose slightly |
| **Amber (lower)** | ▽ (Chevron Down) | Fast / Low AoA | Reduce power; allow slight nose up |

Combination indications (e.g., donut + upper chevron) indicate transitional states.

### Stall Characteristics

| Parameter | Value |
|---|---|
| Stall Warning Onset | ~20 AoA units |
| Full Stall | ~23 AoA units |
| Stall Speed (clean, light) | ~130 KIAS |
| Stall Speed (dirty — gear/flaps) | ~110 KIAS |
| Departure Susceptibility | Low — straight wing is very forgiving |
| Spin Recovery | Standard: idle / neutral stick / opposite rudder |

**Stall Recovery Priority:** Nose down → Wings level → Power. In that order. Reducing AoA is the first priority — not adding power.

> *⚠ Realism Divergence: The real A-10A has a physical AOA indexer on the canopy frame plus a dedicated AoA gauge. In DCS FC3, AOA indexer information is displayed on the HUD overlay. Thresholds and behavior are the same.*

---

## Operating Limitations

Memorize these limitations before your first flight:

| Limitation | Value | Consequence of Violation |
|---|---|---|
| **Max Takeoff Weight** | ~50,000 lbs (structural) | Tire failure; structural overload |
| **Max Landing Weight** | 46,000 lbs structural; recommend < 40,000 lbs | Hard landing structural damage |
| **G-Limit (clean)** | +7.33 G / −3.0 G | Structural failure |
| **G-Limit (stores)** | Typically +4.0–5.0 G | Reduce with heavy/asymmetric loadout |
| **Max AoA** | 20–22 units (stall warning) | Stall/departure; spin below 10,000 ft |

### Airspeed Limitations

| Limit | Speed (KIAS) |
|---|---|
| Vne (Never Exceed) | 450 |
| Max Mach | M 0.75 |
| Gear Extension (Vlo) | 200 |
| Flaps Limit (Vfe) | 200 |
| Crosswind Limit — Dry | 20 knots |
| Crosswind Limit — Wet | 15 knots |
| Canopy Open (taxi only) | 50 |

---

## Emergency Procedures (Academic)

These procedures are academic review. Memorize the immediate action items; they will be practiced in Event 5.

### Engine Fire / Engine Failure In Flight

1. **Throttle (affected engine)** — IDLE
2. **Identify** — yaw direction, RPM drop, EGT change
3. **Throttle (affected)** — OFF (`RAlt + End` / `RCtrl + End`)
4. **Fire handle** — PULL (if fire warning)
5. **Agent** — DISCHARGE (if fire persists)
6. **Land ASAP**

*"Dead foot, dead engine" — the foot requiring NO rudder pressure points to the failed engine. Push the opposite.*

### Engine Failure on Takeoff (Below Vr)

1. **Throttles** — IDLE
2. **Wheel Brakes** — MAX (`W`)
3. **Speed Brakes** — OPEN (`LShift + B`)
4. **Jettison stores** — if unable to stop (`LCtrl + W`)

### Hydraulic Failure

1. **Identify** — HYD PRESS caution (one or both systems)
2. **Single system:** Retain full control via remaining system; land when practical
3. **Dual system:** Accept heavy controls (manual reversion); fly straight-in approach; avoid aggressive maneuvering
4. **Emergency gear:** `LShift + LCtrl + G` if normal gear extend fails

### Ejection Criteria (ACES II)

- **Zero-zero capable** — safe ejection from ground level at zero airspeed
- **Decision altitude:** 2,000 ft AGL is the practical minimum for uncontrolled aircraft
- **Below 2,000 ft AGL** with uncontrolled departure or unrecoverable situation: **EJECT immediately**
- **DCS Eject:** `LCtrl + E` × 3

---

## Completion Standards

This is an academic event. The student passes by correctly answering the following questions before proceeding to Event 2:

- [ ] **Q1:** What is the TF34 spool-up time from idle to military power? *(Answer: 4–6 seconds)*
- [ ] **Q2:** What does a green donut on the AOA indexer indicate? *(Answer: On-speed — correct AoA for approach)*
- [ ] **Q3:** You have a suspected engine fire. What are your first two actions? *(Answer: Throttle to idle on the affected engine; identify which engine)*
- [ ] **Q4:** The A-10A can be landed with both hydraulic systems failed. True or false, and why? *(Answer: True — the aircraft has direct mechanical manual reversion on all flight controls)*
- [ ] **Q5:** What is the maximum G-limit on a clean A-10A? *(Answer: +7.33 G / −3.0 G — but reduces with stores)*
- [ ] **Q6:** At what altitude should an uncontrolled A-10A pilot eject? *(Answer: 2,000 ft AGL minimum for uncontrolled aircraft; seat is zero-zero capable)*

---

[→ Proceed to Event 2: Familiarization Flight 1](event-2-fam-1.md)

---

*Based on T.O. 1A-10A-1 and Eagle Dynamics DCS World documentation. For simulation use only.*
