# OH-58D Kiowa Warrior — DCS Checklist

> **Aircraft:** Bell OH-58D Kiowa Warrior | **Role:** Scout / Light Attack Helicopter
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [Cockpit Orientation](#cockpit-orientation)
2. [Operating Limitations](#operating-limitations)
3. [Performance & V-Speeds](#performance--v-speeds)
4. [Communications Setup](#communications-setup)
5. [Cold-Dark Startup](#cold-dark-startup)
6. [Post-Start Checks](#post-start-checks)
7. [AHRS/GPS Alignment](#ahrsgps-alignment)
8. [Before-Taxi Checklist](#before-taxi-checklist)
9. [Hover Taxi](#hover-taxi)
10. [Pre-Takeoff Checklist](#pre-takeoff-checklist)
11. [Hover & Takeoff](#hover--takeoff)
12. [Basic Flight Maneuvers](#basic-flight-maneuvers)
13. [Navigation (AHRS/GPS)](#navigation-ahrsgps)
14. [Traffic Pattern](#traffic-pattern)
15. [Approach & Landing](#approach--landing)
16. [Emergency Procedures](#emergency-procedures)
17. [MMS (Mast-Mounted Sight)](#mms-mast-mounted-sight)
18. [Weapons Employment](#weapons-employment)
19. [Scout Procedures](#scout-procedures)
20. [Laser Designation](#laser-designation)
21. [Defensive Procedures](#defensive-procedures)
22. [Shutdown Checklist](#shutdown-checklist)
23. [Keyboard & Joystick Reference](#keyboard--joystick-reference)
24. [Cross-References](#cross-references)
25. [Realism Notes](#realism-notes)

---

## Cockpit Orientation

```
┌─────────────────────────────────────────────────────┐
│              OVERHEAD CONSOLE                        │
│  Battery  Generator  Fuel Valve  Boost Pump  FADEC   │
│  Rotor Brake  Anti-Collision  Position Lights        │
├─────────────────────────────────────────────────────┤
│              INSTRUMENT PANEL                        │
│  Attitude Indicator  Airspeed Indicator  Altimeter   │
│  VSI  Radar Altimeter  Heading Indicator/HSI         │
│  Torque (% Q)  TOT  N1  Nr  Oil Press/Temp           │
│  MFD (Multi-Function Display) — Center               │
│  Caution/Warning Panel                               │
├─────────────────────────────────────────────────────┤
│              CENTER PEDESTAL                         │
│  ARC-164 (UHF) Control Head                         │
│  ARC-201 (FM) Control Head                          │
│  Audio Panel (ICS / Radio Select)                   │
│  Transponder (IFF)                                  │
├─────────────────────────────────────────────────────┤
│  LEFT CONSOLE          │      RIGHT CONSOLE          │
│  MMS Controller        │  Weapon Panel               │
│  Collective (twist grip│  Master Arm                 │
│  throttle)             │  Weapon Select              │
└─────────────────────────────────────────────────────┘
```

| Panel | Location | Key Instruments |
|---|---|---|
| **Overhead console** | Above pilot | Battery, generator, FADEC, fuel valve, boost pump, rotor brake, lights |
| **Instrument panel** | Forward | ADI, ASI, altimeter, VSI, radar altimeter, HSI, engine gauges, MFD |
| **Center pedestal** | Between seats | ARC-164 UHF, ARC-201 FM, audio panel, transponder |
| **Collective** | Left side | Twist-grip throttle (IDLE → FLY detent), radio trigger |
| **Left console** | Left | MMS controller |
| **Right console** | Right | Weapon panel, master arm |

---

## Operating Limitations

| Parameter | Normal | Caution | Limit |
|---|---|---|---|
| **Max gross weight** | — | — | 5,500 lbs (2,495 kg) |
| **TOT (continuous)** | < 738°C | 738–810°C | > 810°C |
| **TOT (takeoff, 5 min)** | ≤ 810°C | — | > 810°C (time limit) |
| **TOT (starting)** | < 810°C | — | > 810°C for > 10 sec → abort |
| **N1/Ng (gas producer)** | 62–104% | — | > 104% (overspeed) |
| **Nr (rotor, power on)** | 97–101% | 90–97% or 101–107% | < 90% / > 107% |
| **Nr (autorotation)** | 90–107% | — | < 90% / > 107% |
| **Torque (continuous)** | ≤ 85% Q | 85–100% Q | > 100% Q |
| **Torque (takeoff, 5 min)** | ≤ 100% Q | — | Exceeded: reduce immediately |
| **Engine oil pressure** | 40–130 PSI | < 40 or > 130 | < 25 PSI (critical) |
| **Engine oil temperature** | < 107°C | 107–150°C | > 150°C |
| **Side slope** | — | — | 10° max (dynamic rollover risk) |
| **Low-G / Pushovers** | **PROHIBITED** | — | Risk of mast bumping |

> *⚠ See [Realism Notes](#realism-notes) for differences between these real-world limits and what the DCS module enforces.*

---

## Performance & V-Speeds

| Speed | Value | Notes |
|---|---|---|
| **Vne (never exceed)** | 110–120 KIAS | Configuration-dependent; decreases with altitude and stores |
| **Vy (best rate of climb)** | ~55–60 KIAS | Standard departure climb speed |
| **Cruise (best range)** | ~90 KIAS | Normal cruise band 80–100 KIAS |
| **Cruise climb** | ~80 KIAS | Enroute altitude gain |
| **ETL (translational lift)** | 16–24 KIAS | Power demand drops significantly above ~24 KIAS |
| **Autorotation (best glide)** | ~72 KIAS | Maximum glide distance from altitude |
| **Autorotation (min sink)** | ~55 KIAS | Minimum rate of descent |
| **Autorotation descent rate** | ~1,500–2,000 fpm | In the glide (collective down) |
| **Hydraulic-off landing speed** | 50–60 KIAS | Run-on landing; avoid hover |

---

## Communications Setup

### Radio Systems

| System | Designation | Band | Primary Use |
|---|---|---|---|
| **UHF-AM** | ARC-164 | 225–399.975 MHz | ATC (tower, ground, approach), guard (243.0 MHz) |
| **VHF/FM** | ARC-201 | 30–87.975 MHz | Inter-flight coordination, ground forces |
| **ICS** | Intercom | — | Crew coordination (hot mic or trigger detent 1) |

### ARC-164 (UHF) Setup
- [ ] **Mode** — BOTH (monitors main frequency + guard 243.0 MHz simultaneously)
- [ ] **Frequency** — Tune to tower/ground per mission briefing
- [ ] **Volume** — Set to comfortable level

### ARC-201 (FM) Setup
- [ ] **Mode** — SC (single channel)
- [ ] **Frequency** — Tune to inter-flight frequency per mission briefing
- [ ] **Volume** — Set to comfortable level

### Audio Panel
- [ ] **Transmit select** — UHF (for ATC calls)
- [ ] **UHF and FM volumes** — Up
- [ ] **ICS mode** — Hot mic (continuous crew comms)

### Radio Trigger (Collective)
- **First detent** — Transmits on ICS (crew intercom)
- **Second detent** — Transmits on selected external radio (UHF or FM)

### Standard Guard
- Monitor **243.0 MHz** (UHF guard) at all times via BOTH mode on ARC-164

---

## Cold-Dark Startup

### Pre-Start
- [ ] **Exterior walkaround** — Rotor blades clear, pitot uncovered, tail rotor intact, skids clear

### Engine Start Sequence

- [ ] **Battery** — ON *(multiple caution lights will illuminate — normal for cold-dark)*
- [ ] **Caution/warning panel** — Check for pre-existing faults
- [ ] **Fuel shutoff valve** — OPEN (verify)
- [ ] **Fuel boost pump** — ON
- [ ] **FADEC mode** — Verify AUTO
- [ ] **Rotor brake** — OFF (released)
- [ ] **Throttle** — IDLE detent
- [ ] **Starter** — PRESS *(N1 begins to rise)*

**Monitor during start:**
- [ ] **N1** — Rising smoothly (FADEC introduces fuel at ~15–20% N1)
- [ ] **TOT** — Monitor throughout; must remain **< 810°C**; if exceeded for > 10 sec → abort
- [ ] **Starter** — Release when N1 reaches ~58–62% (self-sustaining speed)
- [ ] **Engine stabilizes** — N1 at ground idle (~62–65%), TOT decreases, Nr rises to 100%
- [ ] **Generator** — ON *(caution lights for generator should extinguish)*
- [ ] **Electrical panel** — Verify buses powered, ~28V DC

### Start Abnormalities

| Abnormality | Indication | Action |
|---|---|---|
| **Hot start** | TOT > 810°C and climbing | Throttle OFF immediately; motor to cool if available |
| **Hung start** | N1 stops rising below idle (~62%) | Throttle OFF; wait 30 sec minimum before retry |
| **No light-off** | N1 rising but no TOT by ~25% N1 | Throttle OFF; check fuel shutoff open |
| **Compressor stall** | Loud bangs, fluctuating TOT/N1 | Throttle OFF immediately; investigate before retry |

---

## Post-Start Checks

- [ ] **N1** — Ground idle (~62–65%), stable
- [ ] **TOT** — Stable, well below limits
- [ ] **Nr** — 100% governed, stable
- [ ] **Torque** — Low at idle (~10–20% Q)
- [ ] **Oil pressure** — 40–130 PSI
- [ ] **Oil temperature** — < 107°C
- [ ] **Hydraulic pressure** — ~1,000 PSI
- [ ] **Generator** — ON, ~28V DC bus voltage
- [ ] **Fuel quantity** — Verify mission fuel load
- [ ] **Caution panel test** — Press test button (all lights illuminate, then extinguish)
- [ ] **Caution panel** — No unexpected cautions
- [ ] **Flight controls** — Cyclic, collective, pedals: full and free, no binding
- [ ] **Anti-collision light** — ON

---

## AHRS/GPS Alignment

- [ ] **AHRS** — ON (should be powered with battery)
- [ ] **Aircraft** — Remain stationary during alignment
- [ ] **Wait for alignment** — ~30–90 seconds in DCS (full align: 2–5 min real-world)
- [ ] **MFD NAV page** — Verify AHRS aligned; heading and attitude indications valid
- [ ] **GPS** — Acquiring satellites; verify position on moving map matches known ramp location
- [ ] **Heading check** — Compare AHRS heading to known ramp/runway orientation

> *⚠ Do not move the aircraft until AHRS alignment is confirmed complete. Any movement during alignment corrupts the gyro data.*

---

## Before-Taxi Checklist

- [ ] **Engine instruments** — N1, TOT, Q, oil pressure/temp all in green
- [ ] **Nr** — 100% governed
- [ ] **Hydraulic pressure** — ~1,000 PSI, normal
- [ ] **Generator** — ON, bus voltage normal
- [ ] **AHRS/GPS** — Aligned, position valid
- [ ] **MFD** — NAV page, moving map active, waypoints verified
- [ ] **Radios** — Frequencies tuned, transmit check complete
- [ ] **Altimeter** — QNH/QFE set per ATIS or briefing
- [ ] **Radar altimeter** — ON
- [ ] **Flight instruments** — Heading indicator aligned, attitude indicator erect
- [ ] **Caution panel** — No unexpected cautions
- [ ] **Fuel** — Sufficient for mission, quantity noted
- [ ] **Anti-collision & position lights** — ON
- [ ] **Doors** — Closed and secure

**Request taxi:**
> *"[Ground], [Callsign], [position], request hover taxi to [destination]"*

---

## Hover Taxi

| Parameter | Value |
|---|---|
| **Hover height** | 3–5 feet skid height AGL |
| **Taxi speed** | Walking pace — ~5–10 knots ground speed |
| **Directional control** | Pedals for heading; cyclic for lateral/fore-aft position |

**Technique:**
1. Smoothly raise collective to establish a 3–5 ft hover
2. Allow aircraft to stabilize before beginning movement
3. Apply gentle forward cyclic to begin movement at walking pace
4. Use pedals to maintain heading along taxiway centerline
5. Stop at hold-short points by neutralizing cyclic and maintaining hover

**Hover taxi hazards:**

| Hazard | Mitigation |
|---|---|
| **Ground resonance** | Any rapid vibration build-up: Nr good → fly away; Nr low → shutdown immediately |
| **Weathervaning** | Active pedal inputs; slow down in crosswinds |
| **Obstacle clearance** | Rotor diameter ~35 ft — maintain 17+ ft clearance from structures |
| **FOD** | Approach ramp areas at minimum speed; visualize debris on walkaround |

---

## Pre-Takeoff Checklist

- [ ] **Engine instruments** — All green (scan N1, TOT, Q, oil pressure/temp)
- [ ] **Nr** — 100% governed
- [ ] **Fuel** — Sufficient for mission and go-around
- [ ] **Flight instruments** — Altimeter set, heading indicator aligned, attitude indicator erect
- [ ] **Radar altimeter** — ON, decision height set
- [ ] **Radios** — Tower frequency on UHF, FM inter-flight frequency set
- [ ] **MFD** — NAV page, waypoints verified
- [ ] **Caution panel** — Clear of unexpected warnings
- [ ] **Anti-collision & position lights** — ON
- [ ] **Doors & harness** — Secure
- [ ] **Departure plan** — Direction, altitude, initial heading reviewed
- [ ] **Emergency plan** — Abort criteria, forced landing area, immediate action briefed

**Request takeoff:**
> *"[Tower], [Callsign], holding short runway [number], ready for departure [direction/VFR]"*

---

## Hover & Takeoff

### Hovering

**Controls in hover:**
- **Collective** → altitude (up = climb, down = descend)
- **Cyclic** → horizontal position (forward/back/left/right)
- **Pedals** → heading (yaw)
- **Throttle** → FADEC governs in AUTO mode (no pilot input needed)

**Hover technique:**
1. Smoothly increase collective — ~1–2 sec from ground to hover height
2. Apply left pedal as needed to counteract torque
3. Stabilize at **3–5 ft skid height** — small, smooth corrections

**Translating tendency:** The OH-58D drifts **right** in a hover (tail rotor thrust). Compensate with slight **left cyclic** — this is a constant trim requirement.

### Power Check

Before takeoff, establish a stable 3-ft hover and note torque required:

| Hover Torque (IGE) | Assessment |
|---|---|
| ≤ 75% Q | Normal — full maneuver capability including OGE hover |
| 75–85% Q | Marginal — normal takeoff OK; OGE hover may not be possible |
| 85–95% Q | Critical — running takeoff preferred; no OGE capability |
| > 95% Q | Cannot hover effectively — reduce weight or wait for better conditions |

### Translational Lift (ETL)

ETL occurs at **16–24 KIAS** — rotor efficiency increases significantly as it moves through undisturbed air.

**Pilot actions through ETL:**
1. As speed approaches 16 KIAS, expect a climb tendency and slight nose pitch-up
2. Apply slight forward cyclic to maintain desired acceleration and climb angle
3. Collective may be reduced slightly as power margin increases through ETL

### Normal Takeoff (from Hover)

1. [ ] Establish stable hover at 3–5 ft, into the wind
2. [ ] **Power check** — note hover torque, verify margins adequate
3. [ ] Apply gentle forward cyclic — begin acceleration while maintaining altitude
4. [ ] As speed approaches **16–24 KIAS (ETL)**, rotor efficiency increases — anticipate climb tendency
5. [ ] Climb through ETL at **~55–60 KIAS (Vy)** for best rate of climb
6. [ ] Maintain heading with pedals; coordinate through power changes

### Maximum Performance Takeoff

Used for obstacle clearance or confined area departures:
1. [ ] Establish hover at 3–5 ft IGE
2. [ ] Pull max power (up to 100% Q, 5-min limit) for vertical or near-vertical climb
3. [ ] Once obstacle is cleared, lower nose and accelerate to Vy
4. [ ] Monitor TOT — must remain ≤ 810°C

### Running Takeoff

Used when hover OGE is not possible (marginal power conditions):
1. [ ] From a low hover or ground roll, apply forward cyclic to begin acceleration
2. [ ] Allow aircraft to accelerate while skids remain close to or on the ground
3. [ ] At ETL (~16–24 KIAS), aircraft becomes airborne — continue climb

### Ground Resonance — Immediate Action

A rapid, violent vibration building during ground contact:

**Nr in normal range (97–101%):** COLLECTIVE — INCREASE. **Fly away immediately.**
**Nr low or decaying:** COLLECTIVE — FULL DOWN. THROTTLE — OFF. Rotor brake when < 40% Nr.

> **Do NOT wait or hesitate. Ground resonance can destroy the aircraft in seconds.**

---

## Basic Flight Maneuvers

### Straight and Level Flight

| Parameter | Value |
|---|---|
| Cruise speed | 80–100 KIAS |
| Cruise torque | ~50–70% Q (varies with weight/DA) |
| Trim | Use trim system to relieve sustained control pressures |

### Turns

- **Normal:** ≤ 30° bank angle; use coordinated pedal to remain in balance
- **Medium:** 30–45° bank; anticipate additional collective for altitude maintenance
- **Steep:** > 45° bank; avoid in normal operations (structural limit ~60°)

### Climbs

| Type | Speed | Configuration |
|---|---|---|
| Best rate | ~55–60 KIAS (Vy) | Normal departure |
| Cruise climb | ~80 KIAS | Enroute altitude gain |
| Max performance | Minimum airspeed with max power | Obstacle clearance |

### Descents

- **Cruise descent:** Reduce collective, maintain airspeed, descent ~500–1,000 fpm
- **Avoid:** Descending at low airspeed (< 24 KIAS) with power applied — VRS risk

### Slow Flight

- Reduce airspeed to 20–40 KIAS while maintaining altitude
- Power increases as speed decreases below ETL — monitor torque
- Avoid going below ~16 KIAS with power unless intentionally hovering

### Autorotation Practice (Power-Off Descent)

Used to practice engine-failure glide. Entry:
1. [ ] **COLLECTIVE — FULL DOWN** (immediately — most critical step)
2. [ ] **Airspeed — 72 KIAS** (best glide) or **55 KIAS** (min sink)
3. [ ] **Nr — Monitor 90–107%** (Nr should stabilize)
4. [ ] **Pedals** — Right pedal (no engine torque to counteract)
5. [ ] **Power recovery** — At ~300 ft AGL: increase collective, resume normal flight

---

## Navigation (AHRS/GPS)

### MFD Navigation Setup

- [ ] **MFD** — ON, select **NAV page**
- [ ] **Moving map** — Verify current position displayed correctly
- [ ] **Waypoints** — Load and verify per mission briefing
- [ ] **ENG page** — Briefly check all engine instruments via MFD

### Waypoint Navigation

| Step | Action |
|---|---|
| 1 | On MFD NAV page, select desired waypoint |
| 2 | HSI will display bearing and distance to waypoint |
| 3 | Fly the indicated heading; adjust for wind drift |
| 4 | On approach to waypoint, MFD will sequence to next waypoint |

### Radar Altimeter

- **ON** before takeoff; set decision height bug as appropriate
- Provides **AGL altitude** — critical for low-level flight and approaches
- Normal reading at hover: **3–5 ft**

### Transponder (IFF)

| Mode | Setting |
|---|---|
| **STBY** | Powered but not transmitting — use on ground |
| **NORM / ON** | Standard transponder — transmitting squawk code |
| **ALT** | Mode C — includes altitude encoding |
| **EMER** | Squawk 7700 (emergency) |

- Before takeoff: Set assigned squawk code; select **ALT** mode
- After landing: Set **STBY**

### TACAN (if equipped)

- Tune channel per mission briefing
- Provides bearing and DME (distance) to a TACAN station
- Cross-check with GPS position for navigation accuracy

---

## Traffic Pattern

### Standard VFR Pattern

```
         Crosswind
    ┌─────────────┐
    │             │
    │  Departure  │  Base
    │  (Upwind)   │
    │             │
────┘  Downwind   └──────────
◄── Runway ──────────────►  Final
```

| Leg | Altitude (AGL) | Airspeed | Notes |
|---|---|---|---|
| **Departure (upwind)** | Climbing | 55–60 KIAS (Vy) | Straight climb over runway |
| **Crosswind** | 300–500 ft → pattern alt | 70–80 KIAS | Turn at 300–500 ft AGL |
| **Downwind** | 500–700 ft | 80–90 KIAS | Abeam the numbers: begin checks |
| **Base** | Descending | 60–70 KIAS | ~300–500 fpm descent |
| **Final** | Descending to landing | 50–60 KIAS, decelerating | Align, decelerate to hover |

### Radio Calls

| Position | Call |
|---|---|
| **Entering downwind** | "[Tower], [Callsign], entering [left/right] downwind runway [number]" |
| **Turning base** | "[Tower], [Callsign], turning base runway [number]" |
| **Final** | "[Tower], [Callsign], final runway [number], [full stop/touch and go]" |
| **Go-around** | "[Tower], [Callsign], going around" |
| **Clear of runway** | "[Ground], [Callsign], clear of runway [number]" |

### Downwind Abeam — Pre-Landing Checks

- [ ] **Fuel** — Sufficient for go-around and re-pattern
- [ ] **Engine instruments** — Green
- [ ] **Landing light** — As required
- [ ] **Radar altimeter** — Decision height set
- [ ] **Harness** — Locked

---

## Approach & Landing

### Normal Approach

| Parameter | Value |
|---|---|
| **Approach angle** | 6–10° |
| **Entry airspeed (final)** | 60–70 KIAS, decelerating |
| **Termination** | Hover at 3–5 ft over landing point |

**Sequence (final to touchdown):**
1. Roll wings level, aligned with landing zone
2. Airspeed 50–60 KIAS, decelerating continuously
3. At ~200 ft AGL: ~40–50 KIAS, descent rate decreasing
4. At ~100 ft AGL: ~30–40 KIAS, approaching hover speed
5. At ~50 ft AGL: Near-hover airspeed, hover power
6. Arrive at 3–5 ft hover over landing point, zero forward speed
7. Verify stable hover and position; clear of obstacles
8. Slowly lower collective — settle onto skids; collective full down on ground

### Steep Approach

*Use for confined areas or obstacle clearance on short final.*

| Parameter | Value |
|---|---|
| **Approach angle** | 12–15° |
| **Entry airspeed** | 50–60 KIAS |

- Maintain angle with reduced power initially
- **Do NOT let descent rate exceed 500 fpm below 40 KIAS** — VRS risk
- As speed decreases below 40 KIAS, increase collective to arrest descent
- Transition smoothly to hover over landing point

### Shallow Approach

*Use for minimal-obstacle environments or power-limited conditions.*

| Parameter | Value |
|---|---|
| **Approach angle** | 3–5° |
| **Entry airspeed** | 60–70 KIAS, decelerating gradually |

- Lower angle requires longer deceleration — begin earlier
- More power required throughout compared to normal approach

### Crosswind Approach

- Crab into the wind to track centerline on final
- As airspeed decreases through ETL, increase pedal and lateral cyclic to maintain heading
- In hover: apply pedals for heading; cyclic to hold position against wind drift

### Go-Around

From any point in the approach:
1. **COLLECTIVE — INCREASE** (to climb power)
2. **AIRSPEED — Accelerate** through ETL to Vy
3. Climb to pattern altitude
4. Communicate: "[Tower], [Callsign], going around"

### Slope Landing

- [ ] Approach into the wind if possible
- [ ] Hover over slope at 3–5 ft; assess surface
- [ ] Slowly lower the **uphill skid first** — apply **downhill cyclic** throughout
- [ ] As weight comes on the uphill skid, continue lowering collective gradually
- [ ] Lower the downhill skid; collective full down when stable

> **Dynamic rollover risk:** If the aircraft begins to roll uncontrollably, immediately **COLLECTIVE UP** to fly away. Never allow the rotor to contact the terrain.

### Confined Area Landing

- [ ] Reconnaissance pass — fly over the area first; confirm landing surface, obstacles, departure path
- [ ] Determine wind direction
- [ ] Approach at steeper angle to clear obstacles
- [ ] Monitor torque — recirculation in confined areas increases power required
- [ ] Maintain rotor clearance: OH-58D rotor diameter ~35 ft; need 17+ ft clearance each side

### Pinnacle Landing

- [ ] Reconnaissance: Assess wind, surface, obstacles, escape routes from multiple angles
- [ ] Approach from the **upwind side** (not from the lee/downwind side — severe downdrafts)
- [ ] Fly normal or steep approach while maintaining ability to go around
- [ ] Hover assessment: verify landing surface and rotor clearance from all obstacles
- [ ] Land slowly — prepared for wind gusts and updraft/downdraft changes at pinnacle edge

### Final Touchdown Sequence (all approaches)

1. Stable hover at 3–5 ft
2. Verify position — clear, over intended point
3. Slowly lower collective — descend ~1–2 ft/sec
4. Maintain heading with pedals; position with cyclic
5. Feel skids contact ground; continue to collective full down
6. On ground: cyclic centered, pedals neutral, collective full down

---

## Emergency Procedures

> **Boldface procedures are memory items — execute immediately without reference.**

### ENGINE FAILURE — IN FLIGHT

> **1. COLLECTIVE — FULL DOWN (immediately)**
> **2. AIRSPEED — 72 KIAS (best glide) or 55 KIAS (minimum sink)**
> **3. Nr — MONITOR (maintain 90–107%)**
> **4. THROTTLE — IDLE (if not already)**
> **5. MAYDAY — Transmit (frequency + guard)**
> **6. SELECT LANDING AREA — Turn toward best available site**
> **7. EXECUTE AUTOROTATION TO TOUCHDOWN**

*Nr should stabilize in the 90–107% range with collective down at glide speed. Pedals: right pedal typically needed (no engine torque to counteract).*

### ENGINE FAILURE — AT HOVER / LOW ALTITUDE

> **1. COLLECTIVE — MAINTAIN (cushion the landing)**
> **2. CYCLIC — Level the aircraft**
> **3. PEDALS — Maintain heading if possible**
> **4. ACCEPT THE LANDING — Do NOT attempt to fly away**

*At hover or very low altitude there is insufficient height to establish an autorotation glide. Use the rotor's stored inertia to cushion the descent. Do not dump the collective — every inch of rotor energy is needed to slow the sink rate.*

### GROUND RESONANCE

*Rapid, escalating vibration during ground contact:*

> **Nr NORMAL (97–101%):**
> **1. COLLECTIVE — INCREASE. FLY AWAY IMMEDIATELY.**
>
> **Nr LOW or DECAYING:**
> **1. COLLECTIVE — FULL DOWN**
> **2. THROTTLE — OFF**
> **3. ROTOR BRAKE — APPLY when Nr < 40%**

**Do NOT wait or hesitate. Ground resonance can destroy the aircraft in seconds.**

### LOSS OF TAIL ROTOR EFFECTIVENESS (LTE)

*Uncommanded right yaw (spin) that pedals cannot stop:*

> **1. PEDALS — FULL LEFT (attempt to stop the yaw)**
> **2. COLLECTIVE — REDUCE (decrease torque to reduce tail rotor demand)**
> **3. CYCLIC — FORWARD (gain airspeed to restore tail rotor effectiveness)**
> **4. IF UNABLE TO RECOVER — Enter autorotation (collective full down eliminates torque)**

*Recovery actions are near-simultaneous — execute together, not as a slow serial sequence.*

**LTE risk conditions:** Low airspeed, high power, wind from left-rear arc (210°–330° relative). Avoid prolonged hover with wind in that sector.

### VORTEX RING STATE (VRS / SETTLING WITH POWER)

*Three conditions: low airspeed (< 24 KIAS) + high rate of descent (> 300–500 fpm) + power applied.*

> **1. CYCLIC — FORWARD (lower the nose aggressively)**
> **2. GAIN AIRSPEED — Accelerate through ETL**
> **3. COLLECTIVE — Adjust as speed increases (may need to reduce initially)**
> **4. SACRIFICE ALTITUDE for airspeed**

**Prevention:** Avoid descending vertically at low airspeed with power on. On steep approaches, do not let descent rate exceed 500 fpm below 40 KIAS.

### FADEC FAILURE / MANUAL REVERSION

> **1. THROTTLE — ASSUME MANUAL CONTROL**
> **2. Nr — MAINTAIN 97–101% with throttle**
> **3. AVOID RAPID COLLECTIVE INPUTS (throttle response slower in manual)**
> **4. LAND AS SOON AS PRACTICABLE**

*The throttle correlator provides a baseline, but the pilot must fine-tune Nr manually. Monitor TOT and torque — FADEC no longer protects against exceedances.*

### HYDRAULIC FAILURE

> **1. CONTROLS — EXPECT VERY HEAVY FORCES**
> **2. AVOID ABRUPT INPUTS**
> **3. AIRSPEED — MAINTAIN 60–80 KIAS (most manageable forces)**
> **4. DO NOT ATTEMPT TO HOVER**
> **5. PLAN A RUN-ON LANDING (50–60 KIAS, skid touchdown)**

### TAIL ROTOR FAILURE (Loss of Directional Control)

> **1. ENTER AUTOROTATION — Reduce collective to eliminate torque**
> **2. AIRSPEED — 72 KIAS (best glide)**
> **3. EXECUTE AUTOROTATION TO TOUCHDOWN**

### ENGINE FIRE — IN FLIGHT

> **1. THROTTLE — IDLE**
> **2. FUEL SHUTOFF — CLOSED**
> **3. ENTER AUTOROTATION**
> **4. LAND IMMEDIATELY**
> **5. EVACUATE after touchdown**

### ELECTRICAL FIRE

> **1. BATTERY — OFF**
> **2. GENERATOR — OFF**
> **3. VENTILATE cockpit**
> **4. LAND AS SOON AS POSSIBLE**

### Full Autorotation — Touchdown Phases

**Phase 1 — Entry (0–3 sec):** Collective FULL DOWN → Establish 72 KIAS → Monitor Nr 90–107% → MAYDAY call

**Phase 2 — Glide:** Maintain 72 KIAS. Select landing area. Aim 1/3 from near edge of LZ. Rate of descent ~1,500–2,000 fpm.

**Phase 3 — Flare (~75–100 ft AGL):** Aft cyclic to raise the nose. Airspeed decreases through ~20–30 KIAS. Nr increases (stores energy for collective pull). 20–30° nose-up attitude.

**Phase 4 — Cushion (~10–15 ft AGL):** Forward cyclic to level aircraft. **COLLECTIVE PULL** — use stored rotor energy to cushion. Touchdown. Collective full down after ground contact; throttle off.

---

## MMS (Mast-Mounted Sight)

The MMS is the OH-58D's defining capability — a sensor ball mounted above the rotor head, allowing observation while in hull-defilade (body concealed behind terrain or structures).

### MMS Components

| Component | Function |
|---|---|
| **TV Camera** | Daytime observation |
| **FLIR** | Thermal/night observation |
| **Laser Rangefinder** | Range to target |
| **Laser Designator** | Designates targets for laser-guided weapons |

### MMS Operation

1. [ ] **MMS power** — ON (from avionics panel)
2. [ ] **FLIR warm-up** — 3–5 minutes
3. [ ] Select **TV** (day) or **FLIR** (night) on MFD WPN page
4. [ ] **Slew MMS** using hat switch or keyboard
5. [ ] **Laser range** — activate to get range to target
6. [ ] **Laser designate** — activate for Hellfire or LGB guidance

### MMS Key Controls

| Function | Key / Control |
|---|---|
| MMS slew up | `Numpad 8` |
| MMS slew down | `Numpad 2` |
| MMS slew left | `Numpad 4` |
| MMS slew right | `Numpad 6` |
| MMS zoom in | `Numpad +` |
| MMS zoom out | `Numpad -` |
| Laser range/designate | `O` |
| Video switch (TV/FLIR) | MFD OSB |

---

## Weapons Employment

> *⚠ The following sections cover combat employment beyond the BQT scope. Procedures are preserved from prior documentation. Validate against the Polychop OH-58D module release notes before relying on keybinds.*

### Weapon Stations

| Station | Weapon Options |
|---|---|
| Left stub | 2.75-in rocket pod or .50 cal gun |
| Right stub | AGM-114 Hellfire × 4, or AIM-92 × 2 |

### Arming

- [ ] **Master Arm** — ARM (`O`)
- [ ] Select weapon via MFD WPN page

---

### M296 .50 cal Machine Gun

- Fixed forward firing
- Effective range: up to 1,000 m against personnel and light vehicles

#### Employment
1. [ ] Select .50 cal on WPN page
2. [ ] Point aircraft at target
3. [ ] Fire: `Space` or trigger (2nd detent)
4. [ ] Burst: 2–3 seconds

---

### 2.75-inch Rockets (Hydra 70)

| Variant | Warhead | Use |
|---|---|---|
| M151 HE-FRAG | 10 lb HE | Personnel, soft targets |
| M261 MPSM | Multi-point | Area targets |
| M264 WP | White phosphorus | Marking, incendiary |
| M229 HEAT | Shaped charge | Light armor |

#### Employment
1. [ ] Select rocket pod on WPN page
2. [ ] Set salvo: 1, 2, or ripple
3. [ ] Dive: 10°–20° toward target
4. [ ] Aim MFD/HUD pipper on target
5. [ ] Fire at 600–1,200 m: `Space`
6. [ ] Pull off at 300 m minimum

---

### AGM-114 Hellfire

| Variant | Guidance | Range | Target |
|---|---|---|---|
| AGM-114A/C | SALH (Semi-Active Laser Homing) | 500m–8km | Armor |
| AGM-114K | Laser + IIR | 500m–8km | Armor, moving |

#### Hellfire Laser Procedure (SALH)
1. [ ] **Master Arm** — ARM
2. [ ] Select AGM-114 on WPN page
3. [ ] **MMS** — Slew to target
4. [ ] **Laser code** — Set (match seeker to designator code)
5. [ ] **Laser designate** — Activate (`O`)
6. [ ] **Missile ready** — Confirm (MFD indication)
7. [ ] **Fire:** `Space`
8. [ ] **Hold laser on target** until impact

#### Hellfire from Defilade
1. Position behind cover
2. **Pop up** just above ridgeline
3. **MMS** — Immediately acquire target, lase
4. **Fire** from behind cover if pop-up attack
5. Or **fire from cover** — MMS can guide up to ~45° off-axis

> **The Kiowa's key tactical advantage is firing from defilade. Master hull-defilade technique for survivability.**

---

### AIM-92 Stinger

Self-defense air-to-air weapon.

1. [ ] Select AIM-92 on WPN page
2. [ ] Acquire airborne target
3. [ ] Seeker tone when locked
4. [ ] Fire: `Space`

---

## Scout Procedures

> *⚠ Beyond BQT scope — tactical reconnaissance and mission employment. Preserved for reference.*

### RSTA (Reconnaissance, Surveillance, Target Acquisition)

#### Scout Mission Sequence
1. [ ] Plan approach — avoid open ground
2. [ ] **Move by bounds** — low level, terrain masking
3. [ ] **Occupy OP** (Observation Post) — behind cover
4. [ ] **MMS** — Scan sector
5. [ ] **ID targets** — Report to FAC/attack aircraft
6. [ ] **Lase** for attack aircraft as needed
7. [ ] After engagement — **Confirm BDA** (Battle Damage Assessment)

#### Target Report Format (SALUTE)
```
Size:      (number of vehicles/personnel)
Activity:  (stationary, moving, etc.)
Location:  (8/10-digit grid)
Unit:      (type — T-72, BMP, truck)
Time:      (time of observation)
Equipment: (additional info)
```

---

## Laser Designation

> *⚠ Beyond BQT scope. Preserved for reference.*

### Laser Codes
- Default code: **1688** (check with FAC/flight lead)
- Must match: designator code = seeker code

### Self-Designation Procedure
1. [ ] MMS on target
2. [ ] Laser STANDBY — check code
3. [ ] Fire weapon (`Space`) — missile launches
4. [ ] Immediately lase (`O`) — hold until impact
5. [ ] Do not break hard — laser must stay on target

### Remote Designation (for Other Aircraft)
1. [ ] Coordinate laser codes with requesting aircraft
2. [ ] Get target info (grid, description)
3. [ ] MMS to target area — acquire target
4. [ ] Notify aircraft: "Ready to lase"
5. [ ] On fire: lase immediately — hold until "Splash"

---

## Defensive Procedures

> *⚠ Beyond BQT scope. Preserved for reference.*

### No Chaff/Flare (Standard Kiowa)
- Limited/no self-protection systems
- **Survivability = tactics**

### Threat Response
1. **Break** immediately on threat warning
2. **Dive** to terrain masking
3. **Extend** — distance is survivability for an unprotected aircraft
4. Never hover in the open if SAM/AAA are present

### Threat Identification
- Use MMS to ID threats from defilade
- Report threat positions to higher/attack aircraft
- Do not engage beyond weapons capability

---

## Shutdown Checklist

### Post-Landing (Before Shutdown)

- [ ] Confirm stable on ground — collective full down, no sliding
- [ ] Confirm authorized parking area
- [ ] **Transponder** — STBY
- [ ] **Landing/search light** — OFF

### Engine Cooldown

- [ ] Remain at **ground idle for 2–3 minutes minimum** before shutdown
- [ ] Monitor TOT — must be stable and well below limits before proceeding
- [ ] *Extended cooldown if TOT is still elevated from high-power operations*

### Shutdown Sequence

- [ ] **Avionics / MFD** — OFF
- [ ] **Radios** — OFF (ARC-164 and ARC-201)
- [ ] **Position lights** — OFF
- [ ] **Anti-collision light** — OFF
- [ ] **Throttle** — IDLE (roll to idle detent)
- [ ] **Throttle** — OFF / Cutoff *(engine spools down, Nr begins to decrease)*
- [ ] **Monitor Nr decay** — Do NOT apply rotor brake yet
- [ ] **Fuel shutoff** — CLOSED
- [ ] **Generator** — OFF
- [ ] **Rotor brake** — APPLY when Nr drops below ~40%
- [ ] **Wait for rotors to stop completely**
- [ ] **Battery** — OFF *(all power removed — cockpit goes dark)*

### Cold-Dark State Verification

| System | Status |
|---|---|
| Battery | OFF |
| Generator | OFF |
| Engine | Shut down, Nr = 0 |
| Fuel shutoff | CLOSED |
| Throttle | OFF / Cutoff |
| All avionics | OFF |
| Radios | OFF |
| MFD | OFF |
| All lights | OFF |
| Transponder | OFF |
| Radar altimeter | OFF |
| Rotor brake | Applied (per SOP) |
| Collective | Full down |

**Radio call after shutdown:**
> *"[Ground], [Callsign], [location], shutting down"*

---

## Keyboard & Joystick Reference

### Flight Controls

| Function | Key | Axis |
|---|---|---|
| Collective Up | `PgUp` | Collective axis |
| Collective Down | `PgDn` | Collective axis |
| Pitch Forward/Back | `Numpad 8 / 2` | Stick Y |
| Roll Left/Right | `Numpad 4 / 6` | Stick X |
| Yaw Left/Right | `Z / X` | Rudder pedals |
| Trim | `T` + stick | — |

### Engine / Systems

| Function | Key |
|---|---|
| Starter | (clickable cockpit) |
| Throttle IDLE → FLY | Collective twist-grip or axis |
| FADEC AUTO/MANUAL | (clickable cockpit) |
| Rotor brake | (clickable cockpit) |

### Radios

| Function | Key |
|---|---|
| ICS transmit | Radio trigger — 1st detent |
| Radio transmit | Radio trigger — 2nd detent |
| Radio menu (easy comms) | `\` |
| F10 Map | `F10` |

### MMS Controls

| Function | Key |
|---|---|
| MMS slew up | `Numpad 8` |
| MMS slew down | `Numpad 2` |
| MMS slew left | `Numpad 4` |
| MMS slew right | `Numpad 6` |
| MMS zoom in | `Numpad +` |
| MMS zoom out | `Numpad -` |
| Laser range/designate | `O` |
| TV/FLIR toggle | MFD OSB |

### Weapons

| Function | Key |
|---|---|
| Master Arm | `O` |
| Fire / Release | `Space` or trigger (2nd detent) |
| Weapon jettison | `LAlt + J` |

---

## Cross-References

- [UH-1H Huey →](uh-1h-huey.md)
- [Mi-24 Hind →](mi-24-hind.md)
- [9-Line CAS Procedures →](../procedures/9-line-cas.md)
- [Radio Communications →](../procedures/radio-communications.md)
- [Airfield & ATC →](../procedures/airfield-atc-communications.md)

---

## Realism Notes

### Operating Limits

The values in the [Operating Limitations](#operating-limitations) table are based on **TM 1-1520-248-10** (real-world). The DCS Polychop module may use slightly different caution/warning trigger points. Observe the actual gauge markings and caution panel thresholds in DCS as the operative limits in simulation.

Key corrections from prior documentation:
- **Torque continuous limit is 85% Q** (not 100%). The 100% Q limit is a 5-minute takeoff power limit, not a continuous operating limit.
- **TOT start limit is < 810°C** (not 843°C). A start that exceeds 810°C for more than 10 seconds should be aborted as a hot start.
- **Nr power-on normal range is 97–101%** (not 98–100%).
- **Vne is 110–120 KIAS** (not 140 kts). The OH-58D is a light scout helicopter — the 140-kt figure applies to other aircraft.
- **Autorotation best glide is ~72 KIAS** (not 65 kts). Min sink rate is ~55 KIAS.

### Translating Tendency

The OH-58D drifts to the **right** in a hover. This is caused by tail rotor thrust pushing the aircraft right to counteract left pedal (applied to oppose main rotor torque). The pilot compensates with slight **left cyclic** as a continuous trim input. This is the operationally correct behavior for a U.S. helicopter with a counterclockwise main rotor.

### ETL Speed

**Effective Translational Lift (ETL)** occurs at **16–24 KIAS** — not ~40 kts as previously stated. The 16–24 KIAS range is consistent with real-world rotary-wing aerodynamics and the TM 1-1520-248-10. The DCS module may vary slightly from this figure.

### Autorotation

DCS autorotation behavior may differ from real-world. The flare timing, Nr response, and touchdown dynamics in DCS should be validated empirically through practice in-sim. The real OH-58D has a steep descent rate (~1,500–2,000 fpm) and limited glide ratio (~4:1). Autorotation to touchdown in a Kiowa requires significant practice in either environment.

### Weapons & Combat Sections

The Weapons Employment, Scout Procedures, Laser Designation, and Defensive Procedures sections are preserved from prior documentation. These cover combat employment **beyond the BQT scope** established by the research dossier. They have not been independently validated against the Polychop module implementation. Cross-check keybinds and MFD procedures against the module's manual before operational use.

---

*Based on TM 1-1520-248-10 (Operator's Manual) and Eagle Dynamics/Polychop Simulations DCS OH-58D module documentation. For simulation use only.*

<!-- Co-authored-by: Copilot <223556219+Copilot@users.noreply.github.com> -->