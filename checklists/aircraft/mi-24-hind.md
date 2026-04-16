# Mi-24P Hind — DCS Checklist

> **Aircraft:** Mil Mi-24P Hind-F | **Role:** Attack / Gunship Helicopter
>
> [← Back to Index](../index.md)

---

## Table of Contents

1. [Cockpit Orientation](#cockpit-orientation)
2. [Operating Limitations](#operating-limitations)
3. [Performance & V-Speeds](#performance--v-speeds)
4. [Communications Setup](#communications-setup)
5. [Cold-Dark Startup](#cold-dark-startup)
6. [Post-Start & Rotor Engagement](#post-start--rotor-engagement)
7. [Navigation System Warm-Up](#navigation-system-warm-up)
8. [Before-Taxi Checklist](#before-taxi-checklist)
9. [Ground Taxi](#ground-taxi)
10. [Pre-Takeoff Checklist](#pre-takeoff-checklist)
11. [Hover Operations](#hover-operations)
12. [Takeoff Profiles](#takeoff-profiles)
13. [Climb Profile](#climb-profile)
14. [Basic Flight Maneuvers](#basic-flight-maneuvers)
15. [Traffic Pattern](#traffic-pattern)
16. [Approach & Landing](#approach--landing)
17. [Emergency Procedures](#emergency-procedures)
18. [Weapons & Systems](#weapons--systems)
19. [Defensive Systems](#defensive-systems)
20. [Shutdown Checklist](#shutdown-checklist)
21. [Keyboard & Joystick Reference](#keyboard--joystick-reference)
22. [Cross-References](#cross-references)
23. [Realism Notes](#realism-notes)

---

## Cockpit Orientation

The Mi-24P has two crew positions:

- **Front cockpit** — Weapons Systems Officer (WSO/Gunner)
- **Rear cockpit** — Pilot (primary flying station)

```
Front Cockpit (WSO — seat `1`):
┌──────────────────────────────────────────┐
│  PKV Sight         SPO-15 RWR display    │
│  Weapon controls   Weapon selector       │
│  Ataka/Shturm guidance panel             │
│  UV-26 countermeasures control           │
└──────────────────────────────────────────┘

Rear Cockpit (Pilot — seat `2`, default spawn):
┌──────────────────────────────────────────┐
│  Flight instruments   Engine gauges      │
│  Autopilot panel      Navigation panel   │
│  R-863 / R-828 radio consoles            │
│  Collective / Cyclic / Throttles         │
└──────────────────────────────────────────┘
```

| Position | Seat | Primary Function | DCS Key |
|---|---|---|---|
| Pilot | Rear | Fly the aircraft | `2` (default spawn) |
| Weapons Systems Officer | Front | Operate weapons and sights | `1` |

> **Single-player:** You spawn in the Pilot (rear) cockpit by default. Switch to WSO with `1`; return to Pilot with `2`.

---

## Operating Limitations

### Engine Limits (TV3-117V × 2)

| Parameter | Normal | Transient (30 sec) | Start Limit | Emergency (single-eng) |
|---|---|---|---|---|
| **TIT (Turbine Inlet Temp)** | ≤ 800°C | ≤ 870°C | ≤ 830°C | ≤ 900°C (15 sec) |
| **Ng (Gas Generator RPM)** | 88–97% | ≤ 100% | — | ≤ 101% (15 sec) |
| **Oil Pressure** | 3.0–4.5 kgf/cm² | — | — | Min 2.0 kgf/cm² |
| **Oil Temperature** | 70–130°C | ≤ 150°C | — | — |

### Rotor & Transmission Limits

| Parameter | Limit | Notes |
|---|---|---|
| **Nr (Normal)** | 92–98% | Target 95% |
| **Nr (Min, Caution)** | < 92% | Requires immediate correction |
| **Nr (Max, Caution)** | > 98% | Reduce collective |
| **Nr (Autorotation range)** | 89–105% | Monitor closely |
| **Torque — Continuous (both eng)** | ≤ 85% | Unlimited duration |
| **Torque — Transient (both eng)** | ≤ 96% | ≤ 30 seconds |
| **Torque — Single-eng continuous** | ≤ 93% | On operating engine |
| **Torque — Single-eng transient** | ≤ 106% | ≤ 30 seconds |

### Flight Envelope Limits

| Parameter | Limit | Notes |
|---|---|---|
| **VNE** | 300 km/h (162 kts) | Never exceed |
| **Max speed — gear down** | 250 km/h (135 kts) | |
| **Crosswind — T/O & landing** | 12 m/s (23 kts) | Hard limit |
| **Tailwind — T/O & landing** | 5 m/s (10 kts) | Hard limit |
| **Max bank angle** | 60° | Normal training limit: 45° |
| **G-Limits** | +2.5 G / –0.5 G | Clean configuration |
| **Max sideward flight** | 50 km/h (27 kts) | |
| **Max backward flight** | 40 km/h (22 kts) | |
| **MTOW** | 11,500 kg | |
| **Min fuel for flight** | 300 kg | Reserve / bingo |

### Start Abort Criteria

| Condition | Indication | Action |
|---|---|---|
| **Hot start** | TIT exceeds 830°C and continues rising | Throttle to STOP immediately |
| **Hung start** | Ng stalls below 55%, does not increase | Throttle to STOP; cool 30 sec before retry |
| **No light-off** | No TIT rise within 10 seconds of start | Release button; throttle to STOP |
| **Oil pressure fail** | No oil pressure within 30 sec of idle | Throttle to STOP; do not continue |

---

## Performance & V-Speeds

> **Soviet convention:** speeds in km/h, altitudes in meters, temps in °C. Knot equivalents provided for reference.

| Symbol | Speed (km/h) | Speed (kts) | Description |
|---|---|---|---|
| **VNE** | 300 | 162 | Never exceed |
| **Vmax (gear down)** | 250 | 135 | Max speed with gear extended |
| **Vcruise** | 220–260 | 119–140 | Normal cruise range |
| **Vy (Best Rate of Climb)** | 120–140 | 65–76 | Maximum altitude gain per minute |
| **Vx (Best Angle of Climb)** | 100–110 | 54–59 | Obstacle clearance |
| **Vautorotation** | 170 | 92 | Best glide speed (dual engine failure) |
| **ETL (Translational Lift)** | ~50 | ~27 | Vibration decrease, nose pitch-up tendency |
| **Vapproach (normal final)** | 120–140 | 65–76 | Final approach speed |
| **Vrunning landing** | 50–70 | 27–38 | Ground speed at main gear contact |
| **Vpattern (downwind)** | 200–220 | 108–119 | Traffic pattern downwind speed |
| **Vtaxi** | 15–20 | 8–11 | Max taxi speed (10 km/h in turns) |
| **Single-engine best speed** | 160–180 | 86–97 | Best performance on one engine |

**Autorotation Note:** Descent rate is 15–20 m/s (3,000–4,000 fpm) — significantly higher than light helicopters due to aircraft weight and stub wing drag. Time from 500 m AGL to ground: approximately 25–35 seconds.

---

## Communications Setup

### R-863 UHF Radio (Primary — ATC & Flight Ops)

| Step | Action |
|---|---|
| 1 | **R-863 power switch** — ON (Pilot right console) |
| 2 | Set frequency for departure airfield ATC |
| 3 | Verify squelch / volume appropriate |
| 4 | Confirm frequency with ATC: "TAXI / ATIS check" |

### R-828 VHF/FM Radio (Backup / Ground / Flight Lead)

| Step | Action |
|---|---|
| 1 | **R-828 power switch** — ON (Pilot right console) |
| 2 | Set frequency per mission plan |
| 3 | Use for ground communications or inter-flight coordination |

### ICS (Intercockpit Communication System)

- ICS active when both cockpits are manned (multiplayer).
- In single-player, `1` / `2` key switches between seats; ICS not applicable.

---

## Cold-Dark Startup

> All steps performed from **Pilot (rear) cockpit** unless marked WSO.

### Phase 1 — Electrical Power (Left Console)

- [ ] **Parking Brake** — SET
- [ ] **Collective** — Full DOWN
- [ ] **Both Throttles** — IDLE detent (confirm at stop)
- [ ] **Battery 1** — ON (voltmeter shows ~24V)
- [ ] **Battery 2** — ON (voltage confirmed)
- [ ] **Caution Panel** — CHECK (multiple lights expected with engines off)
- [ ] **Warning Light Test** — PRESS and HOLD; verify all lights illuminate; release

### Phase 2 — APU Start (Left Console)

- [ ] **Fuel Boost Pumps (both)** — ON → fuel pressure indication confirmed
- [ ] **APU Start Button** — PRESS → APU RPM rising
- [ ] Wait for APU RPM to stabilize at operating range
- [ ] **APU Generator** — ON → additional buses powered; caution lights begin extinguishing

> *DCS keyboard alternative: autostart available via `LWin + Home`. Manual procedure preferred for training.*

### Phase 3 — Left Engine Start

- [ ] **Left Throttle** — Confirm at IDLE detent
- [ ] **Left Engine Start Button** — PRESS (`RAlt + Home`)
- [ ] **Ng (L)** — Monitor rising toward 63–65%
- [ ] **TIT (L)** — Monitor; **ABORT if exceeds 830°C**
- [ ] Wait for Ng to stabilize at ground idle (~63–65%)
- [ ] **Oil Pressure (L)** — Confirm 3.0–4.5 kgf/cm² within 30 sec

### Phase 4 — Right Engine Start

- [ ] **Right Throttle** — Confirm at IDLE detent
- [ ] **Right Engine Start Button** — PRESS (`RCtrl + Home`)
- [ ] **Ng (R)** — Monitor rising toward 63–65%
- [ ] **TIT (R)** — Monitor; **ABORT if exceeds 830°C**
- [ ] Wait for Ng to stabilize (~63–65%)
- [ ] **Oil Pressure (R)** — Confirm 3.0–4.5 kgf/cm²

### Phase 5 — Post-Start Electrical

- [ ] **Left Generator** — ON → GEN 1 caution extinguishes
- [ ] **Right Generator** — ON → GEN 2 caution extinguishes
- [ ] **APU Generator** — OFF
- [ ] **APU** — OFF → APU RPM decays to zero

### Phase 6 — Avionics Power-On (Pilot)

- [ ] **R-863 UHF Radio** — ON; set departure frequency
- [ ] **R-828 VHF/FM Radio** — ON; set frequency per plan
- [ ] **IFF/SRO-2** — STANDBY
- [ ] **ARK-15 ADF** — ON; tune to NDB if available
- [ ] **RSBN** — ON; select beacon channel
- [ ] **DISS-15 Doppler** — ON (warm-up: 2–3 min)
- [ ] **Radar Altimeter (A-037)** — ON; set warning altitude bug
- [ ] **Autopilot** — STANDBY (do not engage channels yet)

### Phase 7 — WSO Cockpit (Switch to seat `1`)

- [ ] **SPO-15 RWR** — ON → display illuminates, self-test completes
- [ ] **UV-26 Countermeasures** — ON; program selected; expendable count confirmed
- [ ] **PKV-1 Sight** — STANDBY (if familiarization desired)
- [ ] **Weapon Master** — **SAFE** (verify all weapon stations safe)
- [ ] **Switch back to Pilot cockpit** (`2` key)

---

## Post-Start & Rotor Engagement

### Post-Start Checks (Pilot)

- [ ] **Hydraulic Pressure (Main)** — 65 ± 5 kgf/cm²
- [ ] **Hydraulic Pressure (Backup)** — 65 ± 5 kgf/cm²
- [ ] **Flight Control Check** — Full cyclic, collective, and pedal deflection; smooth, full travel, no binding
- [ ] **Caution Panel** — Clear (only expected gear-related lights)

### Rotor Engagement

- [ ] **Both engines** — Confirmed at ground idle (Ng ~63–65%)
- [ ] **Both Throttles** — Advance to **FLY** detent
- [ ] **Nr** — Monitor rising toward 95%
- [ ] **Governor** — Verify ON (Nr stabilizes at 95% automatically)
- [ ] **Nr** — Stable at 95 ± 2% (92–98% acceptable)
- [ ] **Rotor Brake** — Verify OFF

> The governor maintains 95% Nr automatically once throttles are in the FLY detent. Monitor for ~30–60 seconds until stable.

---

## Navigation System Warm-Up

| System | DCS Warm-Up | Real-World | Notes |
|---|---|---|---|
| **DISS-15 Doppler** | ~2–3 min | ~5–10 min | No ground speed output until warm |
| **ARK-15 ADF** | ~30 sec | ~1–2 min | Ready when needle responds to NDB |
| **RSBN** | ~1 min | ~3–5 min | Tune to active beacon channel |
| **Gyro Instruments (ADI/HSI)** | ~1 min | ~3–5 min | ADI and HSI need gyro spin-up |

- [ ] **DISS-15** — Verify warm-up complete; ground speed displayed
- [ ] **ARK-15** — Bearing pointer responds to tuned NDB
- [ ] **RSBN** — Channel confirmed; bearing/distance displayed
- [ ] **ADI / HSI** — Attitude and heading stable and correct

> *⚠ DCS compresses warm-up times. Real-world ground time from cold start to takeoff-ready is 10–15 minutes; DCS allows ~3–5 minutes.*

---

## Before-Taxi Checklist

- [ ] **Engines** — Both at FLY, Ng/TIT/Oil in limits
- [ ] **Nr** — 95% stable
- [ ] **Hydraulics** — Both systems 65 ± 5 kgf/cm²
- [ ] **Flight Controls** — Free and correct (check complete)
- [ ] **Caution Panel** — Clear of unresolved warnings
- [ ] **Navigation** — DISS-15 warmed up; ARK-15 / RSBN tuned
- [ ] **Radios** — R-863 and R-828 set and checked
- [ ] **Altimeter** — Set QFE (field = 0) or QNH (sea-level pressure)
- [ ] **Landing Gear** — DOWN and locked (3 green lights)
- [ ] **Weapons** — SAFE (confirmed)
- [ ] **Parking Brake** — SET (until ready to taxi)

---

## Ground Taxi

### Nosewheel Steering

| Aspect | Detail |
|---|---|
| **Engagement** | Automatic when weight on wheels; pedals steer nosewheel |
| **Authority** | ±45° — sufficient for taxi turns |
| **Speed limit** | ≤ 20 km/h straight; ≤ 10 km/h in turns |
| **In flight** | Pedals control tail rotor only (no nosewheel) |

### Wheel Brakes

| Control | Function |
|---|---|
| **Toe brakes** | Left pedal top = left brake; right pedal top = right brake |
| **Differential** | Apply asymmetrically for tight turns |
| **Parking Brake** | Lever on lower pedestal — SET for parking |

### Taxi Procedure

- [ ] **ATC clearance** — Obtained before brake release
- [ ] **Parking Brake** — RELEASE
- [ ] **Collective** — Increase slightly to initiate roll (heavy aircraft needs noticeable input)
- [ ] **Speed** — Maintain ≤ 20 km/h; ≤ 10 km/h in turns
- [ ] **Brake Check** — Brief application of toe brakes; confirm both sides respond evenly
- [ ] **Steering** — Pedals for directional control; avoid sharp turns at speed

---

## Pre-Takeoff Checklist

- [ ] **Engines** — Both at FLY; Ng, TIT, oil in limits
- [ ] **Nr** — 95% stable
- [ ] **Torque** — Note available margin (record current torque at ground idle)
- [ ] **Hydraulics** — Main and backup 65 ± 5 kgf/cm²
- [ ] **Caution Panel** — Clear
- [ ] **Flight Controls** — Free and correct
- [ ] **Trim** — Neutral / set for takeoff
- [ ] **Radios** — R-863 set; ATC clearance obtained
- [ ] **Altimeter** — QFE or QNH set; reading correct
- [ ] **Radar Altimeter** — ON; warning altitude bug set
- [ ] **Navigation** — ARK-15 / RSBN tuned if applicable
- [ ] **Fuel** — Sufficient; boost pumps ON; cross-feed OFF
- [ ] **Autopilot** — All channels OFF
- [ ] **Landing Gear** — DOWN and locked (3 green)
- [ ] **Weapons** — SAFE (verify from WSO cockpit)
- [ ] **Exterior Lights** — Anti-collision beacon ON minimum
- [ ] **Departure plan** — Brief WSO on profile

---

## Hover Operations

> **Critical Context:** The Mi-24P is a poor hover platform. At 11,000+ kg, the stub wings produce only drag at hover speeds. Minimize hover time — running takeoffs and landings are preferred.

### Hover Power Check

Before any hover operation, verify power margin:

| IGE Hover Torque | Assessment | Recommendation |
|---|---|---|
| < 80% | Comfortable | Hover and OGE hover feasible |
| 80–85% | Marginal | OGE hover not recommended |
| ≥ 85% | Insufficient | **Use running takeoff** |
| ≥ 90% | Critical | Even IGE hover marginal |

### Pick-Up to a Hover

- [ ] Pre-takeoff checks complete
- [ ] Set force trim (cyclic approximately centered)
- [ ] Collective — increase **slowly** (expect 60–80% torque for IGE hover)
- [ ] **Left pedal** — apply progressively as collective rises (counteract torque)
- [ ] Maintain position with cyclic; use outside reference point
- [ ] Establish hover at 2–3 m (6–10 ft) AGL
- [ ] Stabilize heading, position, altitude with small constant corrections

### Hover Turns (Pedal Turns)

- Apply steady pedal in desired turn direction; use small, smooth inputs
- Apply slight collective increase as torque demand shifts
- Anticipate drift — cyclic corrections needed during yaw changes
- The Mi-24P has high yaw inertia — let it rotate; anticipate the stop

### Hover Taxi

| Aspect | Technique |
|---|---|
| **Speed** | < 20 km/h forward |
| **Altitude** | 2–3 m AGL (gear down) or 5 m (gear up) |
| **Control** | Cyclic for movement; collective for altitude; pedals for heading |
| **LTE risk** | Crosswind awareness critical during slow hover taxi |

---

## Takeoff Profiles

### Running Takeoff (Preferred — Standard Mi-24P Departure)

> The running takeoff is the standard departure method. It requires ~15–20% less torque than a hover takeoff and uses the aircraft's acceleration advantage.

- [ ] Align with takeoff direction (into wind preferred)
- [ ] Collective — smoothly increase to 70–80% torque; aircraft begins rolling forward
- [ ] Pedals — maintain directional control via nosewheel steering
- [ ] As speed builds (~30–40 km/h) — apply slight forward cyclic
- [ ] At ~50 km/h (ETL) — expect vibration decrease and nose pitch-up tendency
- [ ] Forward cyclic — counter ETL pitch-up; maintain acceleration
- [ ] At 70–80 km/h — aircraft becomes light on gear
- [ ] Aircraft lifts off; establish positive climb
- [ ] **Landing Gear** — UP (`G`); verify 3 green lights extinguish
- [ ] Accelerate to 120–140 km/h (Vy)
- [ ] Climb at Vy to desired altitude

### Normal Hover Takeoff

Used when runway unavailable or precision departure required.

- [ ] Establish IGE hover and confirm power margin (torque < 80%)
- [ ] Smooth forward cyclic — aircraft begins accelerating
- [ ] At ETL (~50 km/h) — counter pitch-up with forward cyclic
- [ ] Maintain altitude or begin gentle climb; adjust collective as translational lift increases
- [ ] At 80+ km/h — accelerate to Vy (120–140 km/h)
- [ ] **Gear** — UP (`G`) after positive rate and climb confirmed

### Maximum Performance Takeoff

Used only to clear obstacles — higher risk; extra monitoring required.

- [ ] Apply maximum allowable torque (≤ 96% transient, ≤ 30 sec)
- [ ] Forward cyclic + collective simultaneously for climb and acceleration
- [ ] Pitch attitude: 10–15° nose up initially; trade speed for altitude
- [ ] Accelerate through ETL as rapidly as possible
- [ ] Transition to Vy once clear of obstacles
- [ ] **Gear** — UP after obstacle clearance

---

## Climb Profile

| Profile | Airspeed | Torque | Use |
|---|---|---|---|
| **Vy (Best Rate)** | 120–140 km/h (65–76 kts) | 85–90% | Maximum altitude gain |
| **Cruise Climb** | 180–200 km/h (97–108 kts) | 80–85% | En route with speed |
| **High-Speed Climb** | 240 km/h (130 kts) | 85–90% | Terrain clearance at speed |

**Level-Off Technique:**
1. Approaching desired altitude (~50 m before) — reduce collective gradually
2. Allow airspeed to increase toward cruise (220–260 km/h)
3. Adjust power for level flight — torque typically 60–75%
4. Trim for hands-off flight; engage autopilot if desired

---

## Basic Flight Maneuvers

### Level Flight

| Parameter | Value |
|---|---|
| **Cruise speed** | 220–260 km/h (119–140 kts) |
| **Cruise torque** | 60–75% (varies with altitude/weight) |
| **Wing lift contribution at cruise** | ~20–25% of total aircraft lift |

The Mi-24P is notably stable at cruise speeds. The stub wings provide longitudinal stability — the aircraft behaves more like a fixed-wing aircraft above 200 km/h.

### Coordinated Turns

| Bank Angle | G-Load | Action |
|---|---|---|
| 15° | 1.04 G | Small collective increase; standard course correction |
| 30° | 1.15 G | Moderate collective increase; standard maneuvering turn |
| 45° | 1.41 G | Significant collective increase; monitor torque |
| 60° | 2.0 G | **Caution** — approaching structural limits; instructor supervision |

Training limit: **45° bank**. Coordinate with pedals to keep slip ball centered.

### Trim Technique

- Force trim uses electromagnetic clutches on cyclic and pedals
- **Set trim:** Release trim button → controls hold current position
- **Change trim:** Press and hold trim release → move controls to new position → release button
- **Re-trim after every:** Speed change, power change, configuration change, autopilot disconnect
- *Rule: If holding steady control pressure for more than 5 seconds — trim it out*

### Autopilot Engagement

| Step | Action |
|---|---|
| 1 | Establish stable, trimmed flight (150+ km/h, wings level) |
| 2 | Verify neutral control pressure |
| 3 | Engage **Pitch** channel first |
| 4 | Engage **Roll** channel (wings level) |
| 5 | Engage **Heading** (optional) — holds current magnetic heading |
| 6 | Engage **Altitude** (optional) — holds barometric altitude ±30 m |

**Do NOT use autopilot during:** hover, takeoff, landing, or below 100 km/h.

**After AP disconnect:** Aircraft holds last trim state. Re-trim immediately or fly with awareness of current trim position.

### Slow Flight (Below ETL)

| Speed | Character | Notes |
|---|---|---|
| 220–260 km/h | Stable, airplane-like; wings generating 20–25% lift | Normal cruise |
| 100–150 km/h | Transitional; wings losing effectiveness; more power needed | Increasing collective required |
| 50–100 km/h | Near ETL; high drag; control feel changing | Anticipate significant collective increase |
| < 50 km/h | Below ETL; rotor doing all work; hover-like power demand | 80–90%+ torque may be required |

---

## Traffic Pattern

> Soviet convention: **QFE** altimeter setting preferred (field elevation reads 0). Pattern altitude: **200 m (660 ft) AGL**.

| Leg | Altitude | Airspeed | Configuration | Notes |
|---|---|---|---|---|
| **Upwind** | Climbing through 200 m | 140–180 km/h | Gear UP | After takeoff |
| **Crosswind Turn** | 200 m AGL | 180 km/h | Gear UP | 90° turn |
| **Downwind** | 200 m AGL | 200–220 km/h | Gear UP → DOWN | Level, parallel to runway |
| **Abeam landing point** | 200 m | 200 km/h | **Gear DOWN** | Begin deceleration; check 3 greens |
| **Base Turn** | Descending through 150 m | 160–180 km/h | Gear DOWN | 90° turn to base |
| **Final Approach** | Descending to field | 120–140 km/h | Gear DOWN | Decelerating |
| **Short Final** | 50–20 m | 80–100 km/h (running) or 0–30 km/h (hover) | Gear DOWN | Landing type determines speed |

### Downwind Checklist (Before Turning Base)

- [ ] **Landing Gear** — DOWN; 3 green lights confirmed (`G`)
- [ ] **Airspeed** — Decelerating below 200 km/h
- [ ] **Altimeter** — Set QFE (or verify QNH)
- [ ] **Radar Altimeter** — Bug set to decision height (e.g., 50 m)
- [ ] **Radios** — Tower frequency set; landing clearance requested
- [ ] **Autopilot** — OFF (hand-fly the approach)
- [ ] **Fuel** — Sufficient for approach + missed approach
- [ ] **Weapons** — SAFE (verify)

---

## Approach & Landing

### Running Landing (Preferred — Standard Mi-24P Arrival)

> The running landing requires 20–30% less power than a hover landing and matches the aircraft's design intent. Preferred at all normal weights.

- [ ] Stabilize on final: 120–140 km/h, 3–5° glide path, descending
- [ ] Decelerate progressively on short final to 80–100 km/h
- [ ] Maintain descent rate at 2–3 m/s
- [ ] At 3–5 m AGL — begin cushioning with collective; reduce descent rate to < 1 m/s
- [ ] **Main gear touches first** (slight nose-up attitude)
- [ ] **Lower nose** — nosewheel contacts; smooth forward cyclic
- [ ] **Collective** — DOWN; ground aircraft and transfer weight to wheels
- [ ] **Pedals** — nosewheel steering engaged; maintain directional control
- [ ] **Toe brakes** — apply progressively (do not lock wheels)
- [ ] Decelerate to taxi speed or stop

**Running Landing Speed Targets:**

| Phase | Speed |
|---|---|
| Short final | 80–100 km/h |
| Main gear contact | 50–70 km/h |
| Rollout | 50 → 0 km/h |

### Hover Landing

Used for precision placement; only when power margin allows (torque < 85% at hover).

- [ ] Decelerate to hover on final: 120 → 80 → 50 → 0 km/h
- [ ] As speed drops below ETL (~50 km/h) — increase collective to maintain altitude
- [ ] If torque exceeds 85% — **abort and execute running landing**
- [ ] Establish stable hover over intended landing point at 2–3 m AGL
- [ ] Slowly lower collective — descend at < 0.5 m/s
- [ ] Maintain position (cyclic) and heading (pedals) with small corrections
- [ ] Ground contact — collective to full DOWN; weight fully on gear
- [ ] Cyclic and pedals — neutral; aircraft settled

### Steep Approach (Obstacle Environment)

| Parameter | Value |
|---|---|
| Approach angle | 8–12° |
| Entry speed | 100–120 km/h |

- [ ] Identify obstacles; plan approach angle to clear them
- [ ] Establish steeper descent by reducing collective more than normal
- [ ] Maintain 100+ km/h — do not let speed decay below 80 km/h
- [ ] As clearing obstacles — smoothly increase collective to arrest descent
- [ ] Transition to running landing or hover per power available
- [ ] **Caution:** If descent rate exceeds 5 m/s at < 50 km/h → settling with power risk. Maintain airspeed.

### Go-Around / Wave-Off

**Go-around decision height: ≥ 50 m AGL.** Below 50 m AGL, committing to the landing is usually safer.

| Condition | Action |
|---|---|
| Unstable approach (speed/altitude not converging) | Go around |
| Torque > 90% and increasing | Go around |
| Obstacle on runway or loss of visual | Go around |

Go-around procedure:
- [ ] **Collective** — UP to 80–90% torque; arrest descent
- [ ] **Cyclic** — forward; accelerate
- [ ] At 120+ km/h — positive climb established
- [ ] **Gear** — evaluate; maintain down for immediate re-approach or retract for re-pattern
- [ ] Re-enter pattern at 200 m AGL on downwind

### Emergency Gear Extension

If normal hydraulic extension fails:
- [ ] Attempt normal extension first (gear lever DOWN)
- [ ] If no green lights — Emergency gear handle — PULL (gear drops under gravity)
- [ ] Verify 3 green lights; plan running landing on main gear if uncertain

---

## Emergency Procedures

> **BOLDFACE items are memorized immediate-action procedures.** Execute without reference to checklist.

### Single Engine Failure — In Flight (BOLDFACE)

```
1. COLLECTIVE — MAINTAIN Nr (92–98%)
2. OPERATIVE ENGINE — INCREASE POWER (torque ≤ 95%)
3. AIRSPEED — 160–180 km/h (best single-engine performance)
4. FAILED ENGINE — IDENTIFY (TIT dropping, Ng dropping on one side; aircraft yaws toward failed side)
5. FAILED ENGINE throttle — IDLE, then STOP
6. CROSS-FEED — OPEN (ensure operating engine has fuel access)
7. LAND — AS SOON AS PRACTICABLE (running landing preferred; do NOT attempt to hover)
```

**Identifying the Failed Engine:**

| Indicator | Failed Engine | Operating Engine |
|---|---|---|
| TIT | Dropping | Normal or increasing |
| Ng | Dropping toward zero | Normal or increasing |
| Torque | Dropping | Increasing |
| Yaw | Aircraft yaws toward failed side | — |

**Single-engine limits:**

| Parameter | Limit |
|---|---|
| Max continuous torque | 93% (operating engine) |
| Max transient torque | 106% (≤ 30 sec) |
| TIT emergency limit | 900°C (15 sec) |
| Hover capability | **NOT possible** at most weights |

### Dual Engine Failure — Autorotation (BOLDFACE)

```
1. COLLECTIVE — FULL DOWN IMMEDIATELY (within 2 seconds)
2. AIRSPEED — 170 km/h (92 kts) [best glide]
3. Nr — MONITOR, maintain 89–105%
4. LANDING AREA — SELECT (best available; into wind)
5. GEAR — DOWN (`G`)
6. At ~30–50 m AGL — FLARE (raise nose 15–20°; reduces forward speed and descent rate)
7. At 5–10 m AGL — LEVEL aircraft; COLLECTIVE PULL (cushion touchdown)
8. TOUCHDOWN — Level attitude; accept ground contact
```

> **Warning:** Descent rate is 15–20 m/s (3,000–4,000 fpm). Time from 500 m AGL to ground is approximately 25–35 seconds. Act immediately. There is no margin for hesitation.

### Engine Failure at Hover / Low Altitude (BOLDFACE)

```
1. COLLECTIVE — MAINTAIN (cushion immediate descent; do NOT slam down)
2. If altitude and Nr permit — LAND STRAIGHT AHEAD
3. If insufficient altitude — ACCEPT HARD LANDING (crash-resistant gear absorbs impact)
4. After landing — EMERGENCY SHUTDOWN
```

### Engine Fire — Left Engine (BOLDFACE)

```
1. LEFT THROTTLE — IDLE, then STOP
2. LEFT FUEL SHUTOFF — CLOSED
3. FIRE AGENT SELECT — BOTTLE 1, ENGINE — LEFT
4. DISCHARGE — PRESS
5. If fire persists after 5 sec — BOTTLE 2, DISCHARGE
6. LAND IMMEDIATELY
```

### Engine Fire — Right Engine (BOLDFACE)

```
1. RIGHT THROTTLE — IDLE, then STOP
2. RIGHT FUEL SHUTOFF — CLOSED
3. FIRE AGENT SELECT — BOTTLE 1, ENGINE — RIGHT
4. DISCHARGE — PRESS
5. If fire persists after 5 sec — BOTTLE 2, DISCHARGE
6. LAND IMMEDIATELY
```

### Emergency Shutdown

```
1. BOTH THROTTLES — STOP
2. FUEL SHUTOFF — BOTH CLOSED
3. BATTERY — OFF (if fire or electrical emergency)
4. ROTOR BRAKE — ON when Nr drops below 50%
5. EVACUATE — After rotor stops
```

### Ground Resonance (BOLDFACE)

> **Time-critical: The aircraft can be destroyed in 3–5 seconds. Act immediately.**

```
GROUND RESONANCE DETECTED (sudden, rapidly increasing airframe oscillation)
│
├── Nr ≥ 90%?
│   ├── YES → COLLECTIVE FULL UP — GET AIRBORNE IMMEDIATELY
│   │         Breaking ground contact eliminates the resonance.
│   │         Land at a different spot; inspect before further flight.
│   │
│   └── NO → THROTTLES TO STOP — ROTOR BRAKE ON — EMERGENCY SHUTDOWN
│            Cannot fly. Stop the rotor as fast as possible.
│            Evacuate after rotor stops.
```

**Conditions that trigger ground resonance:** Hard surface (concrete/asphalt), wheels on ground with rotor turning, damper malfunction, hard landing, single-gear ground contact, blade imbalance.

### Loss of Tail Rotor Effectiveness (LTE)

**Recognition:** Uncommanded yaw (nose-right for Mi-24P), increasing pedal with no yaw arrest. Occurs during hover, slow flight in crosswind, or approach.

```
1. FULL OPPOSITE PEDAL — immediately
2. CYCLIC FORWARD — accelerate
3. Above 80–100 km/h — yaw stabilizes (vertical stabilizer regains authority)
4. If at low altitude — accept the yaw; focus on controlled landing
```

**Prevention:** Avoid prolonged hover in tailwind. Monitor wind direction during pedal turns. Avoid the critical azimuth (tail into wind).

### Vortex Ring State (Settling with Power)

**Conditions:** Airspeed < 50 km/h + descent rate > 5 m/s + power applied.

**Recognition:** High descent rate not improving with added collective; vibration and buffeting; uncommanded roll or yaw.

```
1. CYCLIC FORWARD — gain airspeed (priority)
2. COLLECTIVE — reduce momentarily (breaks vortex)
3. Accelerate above 50 km/h — out of VRS envelope
4. Resume normal flight (expect 50–150+ m altitude loss during recovery)
```

> At low altitude, VRS may be unrecoverable. Maintain 50+ km/h during all powered descents.

### Hydraulic Failure — Main System

```
1. VERIFY backup hydraulic pressure normal (65 kgf/cm²)
2. If backup normal — CONTINUE FLIGHT on backup
3. GEAR — DOWN (emergency extension if needed)
4. LAND — As soon as practicable
```

### Hydraulic Failure — Both Systems

```
1. EMERGENCY HYDRAULIC PUMP — ON (if available)
2. AIRSPEED — REDUCE below 150 km/h (lighter control forces)
3. CONTROLS — EXTREMELY HEAVY (maximum physical effort required)
4. LAND IMMEDIATELY — Straight-in; running landing preferred
```

### Tail Rotor Failure / Loss of Drive (BOLDFACE)

```
1. AIRSPEED — INCREASE above 130–160 km/h (vertical stabilizer provides yaw authority)
2. DO NOT HOVER — no yaw control at low speed
3. YAW CONTROL — use collective changes for coarse directional control
4. LANDING — RUNNING LANDING ONLY; maintain 80+ km/h until touchdown
5. After touchdown — differential braking for directional control
```

---

## Weapons & Systems

> ⚠ **Scope Note:** Weapons employment is **beyond BQT scope**. The procedures below are provided as a familiarization reference. Tactical employment requires dedicated weapons training. All weapon systems should remain **SAFE** during all BQT sorties.

### Weapon Stations

| Station | Weapon Options |
|---|---|
| Outboard pylons × 4 (2 per stub wing) | S-8 / S-13 / S-24 rockets; Ataka / Shturm ATGM; FAB bombs; RBK dispensers; R-60 / R-73 AAM |
| Fixed right-side fuselage mount | GSh-30-2 twin-barrel 30mm cannon (pilot-aimed) |

### Weapons & Stores Summary

| Weapon / System | Type | Effective Range | Notes |
|---|---|---|---|
| **GSh-30-2 30mm Cannon** | Fixed twin cannon | < 1.5 km | Fixed starboard mount; pilot aims aircraft |
| **9M114 Shturm** | ATGM (SACLOS radio) | 400 m – 5 km | WSO guides; steady flight required |
| **9M120 Ataka** | ATGM (SACLOS radio) | 400 m – 6 km | Improved range vs. Shturm |
| **S-8 Rockets (80mm)** | Unguided | 1–2 km | 20-round B-8V20A pods |
| **S-13 Rockets (122mm)** | Unguided | 1–2.5 km | 5-round pods; heavy punch |
| **S-24 Rockets (240mm)** | Unguided heavy | 2–3 km | Single rail; powerful |
| **R-60 / R-73 AAM** | IR air-to-air | 0.5–5 km | Self-defense |
| **FAB-100/250 / RBK-250** | Bombs / Dispensers | Overflight | Low-altitude delivery |

### Master Arm (WSO Cockpit — seat `1`)

- [ ] **Weapon Master** — ARM (enable only when cleared for weapons employment)
- [ ] **Weapon select** — choose on front cockpit panel
- [ ] After employment — **Master Arm → SAFE immediately**

---

## Defensive Systems

> ⚠ **Scope Note:** Tactical employment of defensive systems is beyond BQT scope. Familiarization provided below.

### SPO-15 Beryoza RWR

- [ ] **SPO-15** — ON (WSO cockpit; pilot may also have indicator)
- Displays threat radar lock and launch warnings
- Audio tones indicate threat type and intensity
- *(See also: [Su-25T SPO-15](su-25t.md#spo-15-beryoza-rwr) for operating notes)*

### UV-26 Chaff / Flare System

| Function | Key (Default) |
|---|---|
| **Chaff** | `[` |
| **Flares** | `]` |
| **Auto-program** | Engages on IR/radar lock detection |

- [ ] **UV-26** — ON; program selected; count confirmed
- Standard defensive break: hard jink + flares simultaneous
- Never hover in SAM/AAA threat area
- High-speed attack runs (250+ km/h) minimize exposure time

---

## Shutdown Checklist

### Taxi to Parking

- [ ] Exit runway; taxi to parking at ≤ 20 km/h
- [ ] Navigate to assigned parking spot; align with markers (nose into wind if possible)
- [ ] Come to full stop; apply wheel brakes
- [ ] **Parking Brake** — SET

### Pre-Shutdown Checks

- [ ] **Weapons** — SAFE; Master Arm OFF (WSO confirms)
- [ ] **Radar Altimeter** — OFF
- [ ] **RSBN** — OFF
- [ ] **DISS-15 Doppler** — OFF
- [ ] **ARK-15** — OFF
- [ ] **Autopilot** — OFF (all channels disengaged)
- [ ] **Exterior Lights** — OFF
- [ ] **Collective** — FULL DOWN

### Engine Cool-Down

- [ ] **Both engines** — Verify at IDLE
- [ ] **Cool-down** — Run at IDLE for **2 minutes minimum**
- [ ] Monitor EGT — should decrease to < 400°C before cutoff

### Engine Shutdown (Right first, then Left)

- [ ] **Right engine fuel cutoff lever** — OFF (`RCtrl + End`)
- [ ] Monitor right engine: EGT decreasing, Ng dropping
- [ ] Wait for right engine to fully stop (EGT → 0, RPM → 0)
- [ ] **Left engine fuel cutoff lever** — OFF (`RShift + End`)
- [ ] Monitor left engine: EGT decreasing, Nr decreasing
- [ ] Wait for left engine to fully stop

### Rotor Brake

- [ ] After both engines at 0% — monitor Nr decay naturally
- [ ] When **Nr drops below 50%** — apply rotor brake gently
- [ ] Increase pressure progressively until rotor stops (Nr = 0%)

> **WARNING:** Do NOT apply rotor brake above 50% Nr. Premature braking can damage the rotor brake mechanism and transmission.

### Electrical & Systems Shutdown (Pilot Cockpit)

- [ ] **Cockpit and instrument lighting** — OFF
- [ ] **Pitot heat** — OFF
- [ ] **Fuel pumps** — OFF (all)
- [ ] **IFF / Transponder** — OFF
- [ ] **Inverters** — OFF
- [ ] **Right Generator** — OFF
- [ ] **Left Generator** — OFF
- [ ] **Battery 2** — OFF
- [ ] **Battery 1** — OFF *(cockpit goes dark)*

### WSO Cockpit Shutdown (Switch to seat `1`)

- [ ] **All weapon systems** — OFF and SAFE
- [ ] **PKV Sight** — OFF
- [ ] **SPO-15 (front)** — OFF
- [ ] **UV-26 (front)** — SAFE
- [ ] **Cockpit lighting** — OFF
- [ ] **Switch back to Pilot** (`2`) or exit aircraft

### DCS Quick Shutdown

| Method | Key | Effect |
|---|---|---|
| **Auto Shutdown** | `LShift + End` | Reverses autostart; shuts all systems |

> Acceptable for repositioning. Full manual shutdown required for evaluation sorties.

---

## Keyboard & Joystick Reference

### Cockpit Switching

| Function | Key |
|---|---|
| Switch to WSO (Front) | `1` |
| Switch to Pilot (Rear) | `2` (default spawn) |

### Engine Controls

| Function | Key |
|---|---|
| Left Engine Start | `RAlt + Home` |
| Right Engine Start | `RCtrl + Home` |
| Left Engine Stop | `RShift + End` |
| Right Engine Stop | `RCtrl + End` |
| Autostart | `LWin + Home` |
| Auto Shutdown | `LShift + End` |

### Flight Controls

| Function | Key | Axis |
|---|---|---|
| Collective Up / Down | `Num +` / `Num –` or HOTAS axis | Collective |
| Pitch | Numpad 8 / 2 | Stick Y |
| Roll | Numpad 4 / 6 | Stick X |
| Yaw / Pedals | `Z` / `X` | Rudder axis |
| Wheel Brakes | `W` (hold) | — |
| Landing Gear Toggle | `G` | — |
| Force Trim Release | Cyclic button / joystick button | — |

### Navigation & Systems

| Function | Key |
|---|---|
| F10 Map | `F10` |
| Radio Menu | `\` |

### Weapons & Defensive

| Function | Key |
|---|---|
| Master Arm | `O` |
| Fire / Release | `Space` or trigger |
| SACLOS Missile Guide | Joystick hat / Numpad |
| Chaff | `[` |
| Flares | `]` |
| Jettison Stores | `LAlt + J` |
| UV-26 Dispense | `Insert` (default) |

---

## Cross-References

- [UH-1H Huey →](uh-1h-huey.md)
- [OH-58D Kiowa →](oh-58d-kiowa.md)
- [9-Line CAS Procedures →](../procedures/9-line-cas.md)
- [Radio Communications →](../procedures/radio-communications.md)
- [Airfield & ATC →](../procedures/airfield-atc-communications.md)

---

## Realism Notes

### Cannon Variant
The Mi-24P ('P' for *Pushka* — cannon) uses a fixed twin-barrel 30mm GSh-30-2 cannon on the starboard fuselage rather than the flexible 12.7mm Yak-B turret of the Mi-24V. The pilot must aim the entire aircraft at the target. This fundamentally changes attack geometry compared to the V variant.

### ATGM Guidance
The Shturm (9M114) and Ataka (9M120) missiles are SACLOS (radio-command) guided. The WSO must maintain the sight crosshair on the target from launch to impact. The pilot must fly a steady, level profile to avoid masking the guidance antenna or exceeding the seeker field of view. In DCS, manual guidance input via joystick hat is required; autopilot engagement before missile employment helps maintain a stable platform.

### Stub Wing Aerodynamics
The fixed stub wings produce approximately 20–25% of total lift at cruise speeds (220+ km/h), significantly offloading the main rotor and improving fuel efficiency. However, at hover and low speeds, the wings produce only drag and increase power required. This is why running takeoffs and landings are operationally preferred and why the Mi-24P has poor hover endurance compared to pure utility helicopters.

### Crew Key Mapping
**Pilot spawns in the REAR cockpit** (seat `2`). The WSO is in the FRONT cockpit (seat `1`). This is the reverse of the intuitive assumption. All primary flight instruments, throttles, and collective are in the rear cockpit. All primary weapons and targeting systems are in the front cockpit.

### Autorotation Limitations
The Mi-24P autorotation descent rate of 15–20 m/s is approximately twice that of a light single-engine helicopter. The stub wings increase drag in autorotation, worsening glide performance. The aircraft has a glide ratio of approximately 4:1. From 500 m AGL, expect only ~2 km of glide distance and approximately 25–35 seconds to the ground. Twin-engine reliability makes this scenario rare, but the procedure must be briefed and practiced.

### Ground Resonance
The Mi-24P uses a 5-blade fully articulated rotor with hydraulic lead-lag dampers. The wheeled undercarriage (vs. skids) provides a coupling path for ground resonance. A damper failure or triggering event (hard landing, uneven tire pressure, blade imbalance) during ground operations with the rotor turning can result in ground resonance. The phenomenon is modeled in DCS. The decision tree (fly if Nr ≥ 90%; emergency shutdown if Nr < 90%) must be reflexive — the aircraft can be destroyed within seconds.

### Metric Units
The Mi-24P uses Soviet metric conventions: speeds in km/h (not knots), altitudes in meters (not feet), temperatures in °C, weights in kg. The altimeter QFE convention means the altimeter is typically set to read zero at field elevation. Students transitioning from Western aircraft must adjust to metric instruments throughout.

### Divergences from Real-World Procedures
1. **APU start:** Real-world requires battery voltage check, startup time monitoring, and exhaust temperature observation not fully modeled in DCS.
2. **Navigation warm-up:** DCS compresses warm-up times significantly. Real cold-start to takeoff-ready is 10–15 minutes; DCS allows ~3–5 minutes.
3. **Autorotation descent rate:** DCS may differ slightly from published RLE figures, but the high descent rate characteristic is evident.
4. **Ground resonance onset:** DCS models the phenomenon but onset severity and time-to-destruction may be less dramatic than real-world.

---

*Based on Mil Mi-24P RLE (Rukovodstvo po Letnoy Ekspluatatsii), Soviet-era flight training manuals, and Eagle Dynamics DCS World Mi-24P Hind module documentation. Where real-world sources conflict with DCS simulation behavior, DCS behavior takes precedence. For simulation use only.*

<!-- Co-authored-by: Copilot <223556219+Copilot@users.noreply.github.com> -->