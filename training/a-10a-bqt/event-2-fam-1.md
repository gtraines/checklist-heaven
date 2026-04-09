# Event 2 — Familiarization Flight 1 (Fam-1)

> **Course:** A-10A Basic Qualification Training | **Event Type:** Flight
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Pre-Mission Setup](#pre-mission-setup)
4. [Part 1 — Cold Start & Cockpit Checks](#part-1--cold-start--cockpit-checks)
5. [Part 2 — Taxi](#part-2--taxi)
6. [Part 3 — Takeoff & Departure](#part-3--takeoff--departure)
7. [Part 4 — Basic Airwork](#part-4--basic-airwork)
8. [Part 5 — Return & Landing](#part-5--return--landing)
9. [Completion Standards](#completion-standards)
10. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Complete a cold-start engine start without exceeding EGT limits
- [ ] Taxi to the runway using nose wheel steering without departing the taxiway
- [ ] Execute a normal takeoff and achieve a clean aircraft configuration by 500 ft AGL
- [ ] Perform basic airwork: 30° and 45° banked turns, 500 ft/min climbs and descents
- [ ] Fly a rectangular traffic pattern and execute one full-stop landing

---

## Ground Brief

### Mission Profile
This is a two-phase flight:
1. **Phase 1 (Ground):** Cold start and taxi
2. **Phase 2 (Air):** Takeoff, basic airwork at medium altitude, one traffic pattern, full-stop landing

### Key Numbers for This Flight

| Item | Value |
|---|---|
| Fuel Load | 50% internal (~5,300 lbs) |
| Stores | Clean (no weapons) |
| Gross Weight (approx.) | ~33,000 lbs |
| Vr (Rotation) | ~125–130 KIAS |
| Vlof (Liftoff) | ~140 KIAS |
| Vy (Best Climb) | 200–210 KIAS |
| Cruise Speed | 250–280 KIAS |
| Pattern Altitude | 1,500 ft AGL |
| Pattern Speed (Downwind) | 180–200 KIAS |
| Final Approach Speed | ~135 KIAS (AOA indexer: green donut) |
| Touchdown Speed | ~120–125 KIAS |

### Spool-Up Reminder
Before you taxi, demonstrate the spool-up lag: advance both throttles from idle to maximum and count seconds until RPM stabilizes. You should feel thrust build noticeably within **4–6 seconds**. This is meaningfully faster than a turbojet — but you must still be ahead of the aircraft on final approach.

---

## Pre-Mission Setup

- [ ] Load DCS World and select **A-10A** on a prepared airfield (Caucasus: Batumi or Kobuleti recommended; NTTR: Nellis or Creech)
- [ ] Set mission to **good weather, day VMC** — no clouds, winds calm or < 10 knots
- [ ] Set aircraft to **cold and dark** (not "ramp start")
- [ ] Confirm A-10A FC3 keybinds are mapped (throttle axis, pitch/roll axis, rudder axis or twist)

---

## Part 1 — Cold Start & Cockpit Checks

### Step 1: Electrical Power
- [ ] **Master Electrical** — ON (`RShift + L`)
- [ ] Confirm HUD illuminates and warning lights energize
- [ ] Allow warning lights to clear as systems initialize

### Step 2: Canopy
- [ ] **Canopy** — CLOSE AND LOCK (`LCtrl + C`)
- [ ] Verify closed visually (external view `F2` if needed)

### Step 3: Left Engine Start
- [ ] **Left Engine Start** — INITIATE (`RAlt + Home`)
- [ ] Monitor RPM rising through 20–25% N2
- [ ] Watch EGT — must NOT exceed **649°C**
- [ ] Left engine settles at idle: **~55–60% N2**
- [ ] Verify oil pressure > 15 PSI

### Step 4: Right Engine Start
- [ ] **Right Engine Start** — INITIATE (`RCtrl + Home`)
- [ ] Monitor same parameters as left engine
- [ ] Both engines at stable idle before proceeding

### Step 5: Post-Start Checks
- [ ] **Warning lights** — verify clear (no hydraulic, fuel, electrical cautions)
- [ ] **Flaps** — set to MVR (`LCtrl + F` or `LShift + F` to cycle to MVR)
- [ ] **Speed Brakes** — confirm closed (`LCtrl + B` if deployed)
- [ ] **Trim** — center all three axes (pitch, roll, rudder)
- [ ] **Canopy** — confirm closed and locked

> *⚠ FC3 Note: In the real A-10A, post-start involves a full switch and circuit breaker scan, INS alignment (4–8 min), and radio checks. DCS FC3 requires only that the engines reach stable idle and the few available caution lights are clear.*

---

## Part 2 — Taxi

### NWS Engagement & Taxi
- [ ] **Nose Wheel Steering (NWS)** — ENGAGE (`Q`)
- [ ] Confirm NWS engaged — the aircraft will steer via rudder input
- [ ] **Parking Brake** — RELEASE (`LCtrl + W`)
- [ ] Apply small throttle input to begin rolling
- [ ] Maintain **15–20 knots** on straight taxiways
- [ ] Reduce to **< 10 knots** before turns

### NWS Technique
The A-10A NWS is responsive but not as twitchy as the Su-25T. Use smooth rudder inputs for gentle turns. On keyboard, a held input will produce a continuous turn — release and center to stop the turn.

> **Technique:** Smooth, progressive rudder inputs. Give the aircraft time to respond before adding more correction. Chasing the nose left-right at high taxi speed will cause oscillations.

- [ ] **Brake Check** — apply brakes at slow speed, verify deceleration
- [ ] Taxi to runway hold-short line

### Hold-Short / Run-Up
- [ ] **Throttles** — advance briefly to ~70% N2; verify RPM responsive and symmetric
- [ ] Return throttles to idle
- [ ] **Trim** — confirm pitch slightly nose-up (1–2 units)
- [ ] **Flaps** — confirm MVR position
- [ ] **Speed Brakes** — confirm CLOSED
- [ ] Confirm runway clear; obtain clearance if multiplayer

---

## Part 3 — Takeoff & Departure

### Takeoff Roll
- [ ] **Line up** on runway centerline
- [ ] **Throttles** — ADVANCE TO MAXIMUM (full forward or `PgUp`)
- [ ] Maintain centerline with rudder; NWS assists at low speed, becomes less effective above ~30 KIAS
- [ ] Call airspeed mentally: "70…100…120…"

### Rotation
- [ ] At **125–130 KIAS** — smooth back pressure, rotate to **8–10° nose-up attitude**
- [ ] Do NOT jerk the nose up — smooth 2–3°/sec pitch rate
- [ ] Aircraft lifts off at ~140 KIAS

> **Warning:** Rotating aggressively increases risk of tail strike — the A-10A sits tail-low on its main gear. Keep rotation rate smooth and deliberate.

### Clean-Up
- [ ] **Positive rate of climb** — confirm on VSI
- [ ] **Gear UP** (`G`) — at positive rate, below 200 KIAS
- [ ] **Flaps UP** (`LShift + F`) — above 150 KIAS and 200 ft AGL
- [ ] **Trim** — adjust nose-down as flaps retract (flap retraction causes nose pitch-up)
- [ ] **NWS** — will auto-disengage in air; re-engage on landing rollout

### Departure Climb
- [ ] Climb at **200–210 KIAS** (Vy) to assigned altitude (10,000 ft MSL recommended for airwork)
- [ ] Trim continuously as speed builds
- [ ] Confirm clean configuration before leveling off

---

## Part 4 — Basic Airwork

Conduct all maneuvers at **10,000 ft MSL** with adequate recovery altitude below.

### Exercise A: Straight & Level
- [ ] Establish level flight at assigned altitude (±100 ft)
- [ ] Trim aircraft to hands-off: zero stick pressure required
- [ ] Set cruise power: ~75% N2; note airspeed (~260–280 KIAS)

### Exercise B: Level Turns

| Maneuver | Standard |
|---|---|
| 30° bank turn | Altitude ±100 ft; ball centered |
| 45° bank turn | Altitude ±150 ft; ball centered; increase back pressure |
| 60° bank turn (demo) | Observe G-load increase; watch AoA |

**Technique:** Unlike the Su-25T, the A-10A's twin-tail design requires less active rudder coordination, but you should still keep the slip/skid ball centered. Add progressive back pressure as bank angle increases to maintain altitude.

### Exercise C: Climbs and Descents
- [ ] **500 ft/min climb** — note required pitch and power change; trim to sustain
- [ ] **1,000 ft/min descent** — reduce power; open speed brakes if needed; maintain 250–260 KIAS
- [ ] **Level-off** — anticipate target altitude by 100 ft; add power; re-trim

### Exercise D: Trim Demonstration
- [ ] **Accelerate** from 250 to 350 KIAS — observe pitch tendency; trim to maintain altitude
- [ ] **Decelerate** from 350 to 200 KIAS — observe pitch tendency; trim to maintain altitude
- [ ] Demonstrate: properly trimmed aircraft holds altitude hands-off

**Instructor Note:** A student using constant stick pressure is not trimming. Brief them: hands off the stick, check deviation, trim to correct. Repeat until the aircraft flies itself.

---

## Part 5 — Return & Landing

### Descent & Approach Setup
- [ ] Descend to **1,500 ft AGL** within 10–15 nm of the field
- [ ] Reduce to **180–200 KIAS** by downwind entry
- [ ] Set up rectangular pattern parallel to the runway

### Downwind Configuration
- [ ] Fly downwind at **1,500 ft AGL** and **180–200 KIAS**
- [ ] Abeam runway threshold:
  - [ ] Reduce throttle to ~60–65% N2
  - [ ] **Gear DOWN** (`G`) — below 200 KIAS — confirm 3 green indicators
  - [ ] **Flaps DN** (`LCtrl + F` cycle to DN) — below 200 KIAS
  - [ ] Trim nose slightly up for approach attitude
- [ ] Speed should settle to **160–170 KIAS** on downwind with gear/flaps down

### Base Leg
- [ ] Turn base when runway is ~45° behind the wingtip
- [ ] Reduce to **150–160 KIAS**
- [ ] Begin descent (~500 ft/min)
- [ ] Cross-check AOA indexer

### Final Approach
- [ ] Turn final — wings level — align with runway centerline
- [ ] **Target: green donut on AOA indexer** (approximately 130–140 KIAS)
- [ ] Stabilize: constant glidepath (~3°), constant descent rate
- [ ] Speed brakes — CLOSED (verify)
- [ ] **Do NOT allow airspeed to decay below 120 KIAS on final** — go-around may be required

### Landing Flare & Touchdown
- [ ] At 50–100 ft AGL — slight back pressure to arrest descent rate (2–3° pitch increase)
- [ ] Do NOT over-flare — the A-10A lands "flat" compared to fighters
- [ ] **Touchdown at approximately 120–125 KIAS** — main gear first
- [ ] Maintain directional control with rudder; engage NWS (`Q`) after nosewheel contact

### Rollout & Braking
- [ ] **Speed Brakes** — OPEN (`LShift + B`) after touchdown
- [ ] Allow speed to decrease to **~80 KIAS** before applying significant wheel brakes
- [ ] **Progressive braking** — smooth, increasing pressure (`W` key or brake axis)
- [ ] Do NOT lock wheels — anti-skid is active, but aggressive braking still causes flat-spotting
- [ ] Maintain runway centerline to full stop

> **Note:** The A-10A has NO drag chute. Rollout relies entirely on aerodynamic drag, speed brakes, and wheel brakes. Plan for **2,000–3,000 ft** of rollout on a clean runway.

---

## Completion Standards

| Standard | Requirement |
|---|---|
| Engine start | No EGT overtemp; all warnings clear before taxi |
| Taxi | Remain on taxiway; taxi speed ≤ 20 KTAS |
| Rotation | Within ±15 KIAS of Vr; no runway excursion |
| Clean-up | Gear and flaps retracted by 500 ft AGL |
| Airwork turns | Altitude ±150 ft in 30° and 45° turns |
| Approach | Stabilized on final ≥ 0.5 nm from threshold |
| AOA on final | AOA indexer green donut ±1 indicator unit |
| Touchdown | Within first 1,000 ft of runway; on centerline ±10 ft |
| Braking | No wheel lockup; stopped within runway length |

---

## Common Errors

| Error | Correction |
|---|---|
| NWS over-correction during taxi | Smooth, progressive inputs; reduce taxi speed before turns |
| Aggressive rotation causing porpoise | Slow, deliberate pitch rate: 2–3°/sec to 8–10° |
| Gear/flaps not retracted on schedule | Build the habit: "positive rate, gear up; 150 KIAS + 200 ft, flaps up" |
| Chasing the AOA indexer on final | Set power on base; make tiny corrections; don't over-react to half-indicator deviations |
| Over-flaring and float | Slight check of descent — do not pull aggressively; aircraft lands flat |
| Heavy braking immediately after touchdown | Speed brakes first; let speed decay before braking; smooth pressure only |
| NWS not re-engaged for rollout | `Q` after nosewheel contact for directional control |

---

[← Event 1: Academics](event-1-academics.md) | [→ Event 3: Fam-2](event-3-fam-2.md)

---

*Based on T.O. 1A-10A-1 and Eagle Dynamics DCS World documentation. For simulation use only.*
