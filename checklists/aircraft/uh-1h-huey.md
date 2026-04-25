# UH-1H Huey — DCS Checklist

> **Aircraft:** Bell UH-1H Iroquois "Huey" | **Role:** Utility / Light Attack Helicopter
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [Cockpit Orientation](#cockpit-orientation)
2. [Operating Limitations](#1-operating-limitations)
3. [Performance & V-Speeds](#2-performance--v-speeds)
4. [Emergency Procedures (Quick Ref)](#3-emergency-procedures-quick-ref)
5. [Weapons & Stores (Quick Ref)](#4-weapons--stores-quick-ref)
6. [Startup Checklist](#startup-checklist)
7. [Before Takeoff](#before-takeoff)
8. [Hover & Takeoff](#hover--takeoff)
9. [Navigation](#navigation)
10. [Weapons Employment](#weapons-employment)
    - [M134 Minigun](#m134-minigun)
    - [M60 Door Guns](#m60-door-guns)
    - [2.75-inch Rockets (M157/M159)](#275-inch-rockets)
11. [Defensive Procedures](#defensive-procedures)
12. [Landing Checklist](#landing-checklist)
13. [Shutdown Checklist](#shutdown-checklist)
14. [Emergency Procedures (Detailed)](#emergency-procedures-detailed)
15. [Keyboard & Joystick Reference](#keyboard--joystick-reference)

---

## Cockpit Orientation

```
┌─────────────────────────────────────────────────────────────┐
│                    OVERHEAD CONSOLE                          │
│  [FUEL VLV] [BOOST PMP] [GOV] [BATT] [GEN] [INV] [DEICE]  │
│  [PITOT HT] [RPM WARN] [START BTN] [CAUTION TEST]          │
├──────────────────────┬──────────────────────────────────────┤
│   COPILOT PANEL (L)  │         PILOT PANEL (R)              │
│  ┌───┐ ┌───┐ ┌───┐  │  ┌───┐ ┌───┐ ┌───┐                  │
│  │ATT│ │ASI│ │ALT│  │  │ATT│ │ASI│ │ALT│                  │
│  └───┘ └───┘ └───┘  │  └───┘ └───┘ └───┘                  │
│  ┌───┐ ┌───┐ ┌───┐  │  ┌───┐ ┌───┐ ┌───┐                  │
│  │VSI│ │HDG│ │T&S│  │  │VSI│ │HDG│ │T&S│                  │
│  └───┘ └───┘ └───┘  │  └───┘ └───┘ └───┘                  │
│  ┌─────────────────────────────────────┐                    │
│  │  ENGINE INSTRUMENTS (CENTER)         │                    │
│  │  [TRQ PSI] [EGT °C] [N1%] [Nr/N2]  │                    │
│  │  [ENG OIL P/T] [XMSN OIL P/T]      │                    │
│  └─────────────────────────────────────┘                    │
│  ┌───────────────┐  ┌─────────────────┐                    │
│  │ CAUTION PANEL │  │ FUEL QTY / MISC │                    │
│  └───────────────┘  └─────────────────┘                    │
├──────────────────────────────────────────────────────────────┤
│                    CENTER PEDESTAL                            │
│  [AN/ARC-134 VHF-AM] [AN/ARC-51BX UHF-AM] [AN/ARC-131 FM] │
│  [AUDIO PANEL (L)]               [AUDIO PANEL (R)]          │
└──────────────────────────────────────────────────────────────┘
```

| Control | Description |
|---|---|
| **Collective** | Left hand — raises/lowers all blade pitch simultaneously; controls altitude and total rotor thrust |
| **Cyclic** | Right hand — tilts the rotor disc; controls direction and bank |
| **Anti-Torque Pedals** | Feet — controls tail rotor pitch; controls yaw and heading |
| **Throttle (twist-grip)** | Twist on collective grip — controls engine fuel flow; works with correlator/governor |

| Panel | Location | Key Items |
|---|---|---|
| **Overhead console** | Above both crew members | Battery, Generator, Inverter, Fuel Valve, Boost Pump, Governor (GOV), Starter, RPM Warning, De-ice |
| **Engine instruments** | Center instrument panel | Torque (PSI), EGT (°C), N1 (%), Dual tachometer (Nr/N2), Engine & Trans oil P/T |
| **Flight instruments** | Pilot's right panel (primary) | Attitude indicator, ASI, Altimeter, VSI, Heading indicator, Turn-and-slip |
| **Caution panel** | Instrument panel | Master Caution, RPM, GEN, GOV EMER, FUEL BOOST, CHIP DET, XMSN OIL, ENG OIL, FIRE |
| **Center pedestal** | Between seats | AN/ARC-134 (VHF-AM), AN/ARC-51BX (UHF-AM), AN/ARC-131 (FM), Transponder, Audio panels |

---

## 1. Operating Limitations

### Engine Limits

| Parameter | Normal | Caution | Limit |
|---|---|---|---|
| **EGT** | < 610°C | 610–625°C (5 sec max) | 720°C starting (10 sec max) |
| **N1 (Gas Producer)** | 58–100% | — | > 101% (overspeed) |
| **Nr (Rotor RPM)** | 321–327 RPM | 294–321 or 327–339 | < 294 RPM (RPM warning) / > 339 RPM (overspeed) |
| **Torque** | < 40 PSI | 40–48 PSI (time-limited) | > 50 PSI (structural limit) |
| **Engine Oil Pressure** | 35–70 PSI | < 35 PSI | < 25 PSI |
| **Engine Oil Temperature** | < 107°C | 107–120°C | > 120°C |
| **Trans Oil Pressure** | 30–70 PSI | < 30 PSI | XMSN OIL PRESS caution |
| **Trans Oil Temperature** | < 110°C | 110–120°C | > 120°C |

### Aircraft Limits

| Parameter | Limit | Notes |
|---|---|---|
| **Max Takeoff Weight** | 9,500 lbs | Standard max gross weight |
| **Vne (Never Exceed)** | 124 KIAS | At sea level; decreases with altitude and weight |
| **Low-G / Pushovers** | **PROHIBITED** | Teetering rotor — risk of catastrophic mast bumping |
| **LTE Risk Azimuth** | Wind from 210°–330° relative | Avoid prolonged hover with wind from left-rear arc |

## 2. Performance & V-Speeds

| Regime | Speed (KIAS) | Notes |
|---|---|---|
| **Vy — Best Rate of Climb** | **60** | Standard climb after takeoff |
| **Cruise** | **90–100** | Best range ~100 KIAS |
| **Cruise Climb** | 80 | Enroute altitude gain |
| **Autorotation (Best Glide)** | **65** | Best distance from altitude |
| **Autorotation (Min Sink)** | 55 | Minimum rate of descent |
| **ETL (Translational Lift)** | 16–24 | Power demand drops significantly above ~24 KIAS |
| **Vne (Never Exceed)** | **124** | Do not exceed |

## 3. Emergency Procedures (Quick Ref)

> Memorize boldface items. These must be executed from memory without checklist reference.

| Emergency | Immediate Action (Boldface) |
|---|---|
| **Engine Failure — In Flight** | 1. **COLLECTIVE** — LOWER immediately (maintain Nr 294–324 RPM)<br>2. **THROTTLE** — CLOSE (full counterclockwise to OFF)<br>3. **AIRSPEED** — 65 KIAS (autorotation glide)<br>4. **PEDALS** — MAINTAIN HEADING (right pedal — no torque)<br>5. SELECT LANDING AREA |
| **Engine Failure — Hover** | 1. **COLLECTIVE** — ADJUST to cushion landing (remaining rotor energy)<br>2. **CYCLIC** — MAINTAIN LEVEL ATTITUDE<br>3. **PEDALS** — MAINTAIN HEADING<br>4. **THROTTLE** — CLOSE (after touchdown) |
| **Engine Fire — In Flight** | 1. **THROTTLE** — CLOSE (enter autorotation)<br>2. **EMERGENCY FUEL SHUTOFF** — OFF<br>3. **CABIN HEAT** — OFF<br>4. **LAND IMMEDIATELY** (autorotate to nearest area) |
| **Hydraulic Failure** | 1. **AIRSPEED** — 60–80 KIAS (manageable control forces)<br>2. **AVOID HOVER** — plan run-on landing<br>3. **LAND AS SOON AS PRACTICABLE** |
| **Generator Failure** | 1. **GEN SWITCH** — RESET, then ON<br>2. **NON-ESSENTIAL EQUIP** — OFF (if not restored)<br>3. **LAND AS SOON AS PRACTICABLE** (~30 min battery) |
| **Loss of Tail Rotor Effectiveness (LTE)** | 1. **CYCLIC** — FORWARD (gain airspeed — cures LTE)<br>2. **COLLECTIVE** — LOWER (reduce torque demand)<br>3. **If spin develops** — AUTOROTATE (removes torque) |
| **Governor Failure** | 1. **GOV SWITCH** — OFF<br>2. **THROTTLE** — MANUAL (maintain Nr 324 RPM)<br>3. **LAND AS SOON AS PRACTICABLE** |
| **Mast Bumping / Low-G** | 1. **AFT CYCLIC** — GENTLY (reload the disc)<br>2. **NEVER push forward cyclic** under low-G |

## 4. Weapons & Stores (Quick Ref)

| Weapon / System | Type | Effective Range | Best Suited For | Simulation Notes |
|---|---|---|---|---|
| **M60D** | 7.62mm Door Gun | ~800m | Infantry, Soft Vehicles, Self-Defense | Operated by AI or player; limited side/rear arc |
| **M134 Minigun** | 7.62mm Rotary MG | 1000 - 1500m | Heavy suppression, Light structures | High rate of fire (2400/4000 rpm); consumes ammo rapidly |
| **Hydra 70 (M151)** | HE Rocket (10lb) | 1.5 - 3km | General purpose, Light vehicles | Standard HE rocket; requires manual compensation |
| **Hydra 70 (M229)** | HE Rocket (17lb) | 1.5 - 3km | Structures, Dug-in infantry | Heavier warhead; slightly different trajectory than M151 |
| **Hydra 70 (M156)** | White Phosphorus | 1.5 - 3km | Target marking, Incendiary | Creates significant smoke; good for marking for CAS |
| **Hydra 70 (M257/M278)** | Illumination Flare | Varies | Night Ops, Battlefield Illum. | M257 (Visible), M278 (IR); aim high to deploy over target |
| **Hydra 70 (M259)** | Smoke Screen | 1.5 - 3km | Obscuring friendly movement | Screening smoke |

---

## Startup Checklist

### Phase 1 — Electrical Power

- [ ] **Battery** — ON *(overhead console — electrical panel; caution panel illuminates normally)*
- [ ] **Caution Panel** — CHECK *(multiple lights on at battery-only — normal before engine start)*
- [ ] **Caution Light Test** — PRESS AND HOLD *(verify all bulbs illuminate; release)*
- [ ] **Inverter** — ON *(overhead — allows attitude indicator and heading indicator to erect; allow 2–3 min to stabilize)*

### Phase 2 — Fuel System

- [ ] **Fuel Valve** — ON *(overhead — guarded; lift guard and toggle)*
- [ ] **Fuel Boost Pump** — ON *(overhead — FUEL BOOST caution light extinguishes when pressure established)*
- [ ] **Fuel Quantity** — CHECK *(sufficient for mission; note quantity in pounds)*

### Phase 3 — Pre-Start Checks

- [ ] **Throttle** — CLOSED *(full counterclockwise on twist-grip to fuel cutoff)*
- [ ] **Collective** — FULL DOWN and friction set
- [ ] **Cyclic** — CENTERED
- [ ] **Pedals** — CENTERED
- [ ] **Governor (GOV)** — OFF *(overhead — must be off for start; engage after stabilizing at idle)*
- [ ] **Area** — CLEAR *(no personnel within 24 ft rotor arc; look both sides and behind)*

### Phase 4 — Engine Start

> **EGT limit during start: 720°C (10-second maximum).** Monitor continuously. If exceeded: throttle to CLOSED immediately.

- [ ] **Starter Button** — PRESS AND HOLD *(overhead — N1 begins increasing)*
- [ ] At **~15% N1** — **Throttle** — advance to **IDLE detent** *(introduces fuel to combustion chamber)*
- [ ] **EGT** — MONITOR for light-off *(rise confirms ignition; expect 200–400°C at light-off)*
  - If no EGT rise by 25% N1 → **ABORT** — throttle CLOSED, motor 30 sec to purge
  - If EGT exceeds **720°C** → **HOT START** — throttle CLOSED immediately; wait 2 min
  - If N1 stagnates below ~55% with rising EGT → **HUNG START** — throttle CLOSED; motor to clear
- [ ] **N1** — accelerating to **58–62%** (ground idle)
- [ ] **Starter Button** — RELEASE *(at idle; do not exceed 60 sec cranking)*
- [ ] **Stabilize at ground idle** — wait 30–60 seconds *(EGT settling, oil pressure rising)*

### Phase 5 — Post-Start

- [ ] **Engine Oil Pressure** — CHECK 35–70 PSI *(within ~30 sec of start)*
- [ ] **EGT** — CHECK below 610°C and stable
- [ ] **Generator (GEN)** — ON *(overhead — GEN caution light extinguishes; voltmeter shows ~28V)*
- [ ] **Governor (GOV)** — ON *(overhead — Nr will adjust to 324 RPM as governor engages)*
- [ ] **RPM Warning Audio** — ON *(overhead — arms low-RPM audio warning)*
- [ ] **Trans Oil Pressure** — CHECK 30–70 PSI
- [ ] **Caution Panel** — VERIFY CLEAR *(all lights out except any normal for current state)*

### Phase 6 — Rotor Engagement (Idle → Flight RPM)

> Keep collective **full down** throughout. Clear the rotor arc.

- [ ] **Idle Stop Release** — PRESS *(button on collective grip while twisting throttle)*
- [ ] **Throttle** — advance to **FLY detent** *(Nr begins rising toward 324 RPM)*
- [ ] **Nr** — MONITOR rising to **324 ±3 RPM** *(needles "marry" when governor holds)*
- [ ] **EGT** — VERIFY below 610°C during power increase
- [ ] **Wait** ~30 seconds for rotor to stabilize

### Phase 7 — Avionics & Navigation Setup

- [ ] **VHF-AM (AN/ARC-134)** — ON; tune ground/tower frequency; set volume
- [ ] **UHF-AM (AN/ARC-51BX)** — ON; GUARD mode or assigned frequency
- [ ] **FM (AN/ARC-131)** — ON; tune assigned frequency if required
- [ ] **Audio Panel** — configure volumes; select VHF for transmit
- [ ] **ADF (AN/ARN-83)** — ON; tune if NDB navigation planned
- [ ] **VOR/ILS (AN/ARN-82)** — ON; tune if VOR navigation planned
- [ ] **Transponder** — STANDBY; squawk code set per clearance
- [ ] **Radar Altimeter** — ON; set low-altitude warning bug
- [ ] **Altimeter** — set current QNH *(Kollsman window; crosscheck with known field elevation)*
- [ ] **Heading Indicator (DG)** — align to magnetic compass *(aircraft stationary)*

---

## Before Takeoff

### Before-Takeoff Checks

- [ ] **Engine instruments** — all within limits *(Nr 324 ±3, EGT < 610°C, torque at idle PSI, oil P&T in range)*
- [ ] **Trans instruments** — within limits
- [ ] **Flight controls** — CYCLE FULL TRAVEL *(cyclic fore/aft/left/right, collective up/down, pedals full left/right — smooth, no binding)*
- [ ] **Force trim** — CHECK *(set trim, verify it holds; release, verify controls move freely)*
- [ ] **Governor (GOV)** — ON
- [ ] **RPM Warning** — ON
- [ ] **Caution panel** — CLEAR
- [ ] **Altimeter** — SET *(reads within 75 ft of known field elevation)*
- [ ] **Transponder** — ON or ALT *(altitude reporting)*
- [ ] **Radios** — tuned; transmit selector set; comm check complete
- [ ] **Crew brief** — complete *(intentions, abort criteria, emergency plan)*

### Hover Power Check

> Mandatory before departure. Determines whether OGE operations are available.

1. Lift to a **stable hover at 3–5 ft** (in ground effect).
2. Read **Torque gauge (PSI)** — this is hover-IGE power required.
3. Compare against max continuous limit (**40 PSI**).

| Power Margin (40 PSI minus hover torque) | Assessment |
|---|---|
| **> 5 PSI** | Good — normal takeoff; OGE operations likely available |
| **3–5 PSI** | Marginal — normal takeoff possible; OGE hover may not be available |
| **< 3 PSI** | Insufficient — running takeoff required; OGE hover not available |
| **At or above 40 PSI in hover** | Performance-limited — running takeoff mandatory; consider mission abort |

---

## Hover & Takeoff

### Hover Technique

1. Set cyclic centered, pedals slightly left (anticipate torque), collective at bottom.
2. Smoothly and slowly raise collective — apply **left pedal** progressively; small cyclic corrections to stay over the spot.
3. As aircraft goes light on skids, continue smooth collective increase.
4. Establish stable hover at **3–5 ft AGL**.
5. Eyes **outside** on a fixed point 50–100 ft ahead. Small, patient inputs only.

> **Pedals are continuous** — heading requires constant adjustment with every collective change or wind gust.

### Normal Takeoff

1. - [ ] Hover power check complete; departure path clear
2. - [ ] Smoothly apply **forward cyclic** to begin acceleration
3. - [ ] Maintain altitude with collective during acceleration
4. - [ ] Passing through **ETL (~16–24 KIAS)**:
   - Expect: vibrations, nose pitching up, slight left yaw
   - Apply **forward cyclic** to hold attitude
   - Apply **right pedal** to counter left yaw
   - **Reduce collective slightly** (rotor more efficient — less power needed for same lift)
5. - [ ] Continue acceleration to **Vy 60 KIAS**
6. - [ ] Positive climb confirmed — set force trim; monitor EGT and torque

### No-Hover Takeoff *(limited power margin)*

1. Position into the wind on a clear departure path.
2. Raise collective until skids barely clear ground (1–2 ft) — remain in ground effect.
3. Immediately apply **forward cyclic** to accelerate while in ground effect.
4. Aircraft will gain translational lift through ETL and begin climbing.
5. Transition to normal climb at Vy (60 KIAS).

### Running Takeoff *(severely power-limited)*

1. Aircraft on the ground, throttle at FLY, collective at minimum.
2. Smoothly increase collective until aircraft is light on skids.
3. Apply **forward cyclic** — aircraft slides forward on skids.
4. As speed increases, aircraft lifts off in ground effect and transitions through ETL.
5. Continue to Vy (60 KIAS) and establish normal climb.

### Climb Profiles

| Profile | Airspeed | Usage |
|---|---|---|
| **Best Rate (Vy)** | 60 KIAS | Maximum altitude gain; obstacle clearance departures |
| **Cruise Climb** | 80 KIAS | Enroute altitude gain while making forward progress |
| **Enroute Cruise** | 90–100 KIAS | Normal transit; best range ~100 KIAS |

---

## Navigation

### Available Equipment

| System | Capability | Notes |
|---|---|---|
| **ADF (AN/ARN-83)** | NDB bearing pointer | 190–1,799.5 kHz; identify station by Morse code before use |
| **VOR/ILS (AN/ARN-82)** | CDI deviation / glideslope | 108.0–117.95 MHz; OBS selects desired radial |
| **Heading Indicator (DG)** | Magnetic heading | Gyroscopic — precess ~2°/min; reset to magnetic compass every 15 min |
| **Magnetic Compass** | Backup heading | Direct reading; use for DG alignment |
| **Radar Altimeter** | AGL altitude | Set low-altitude warning bug for terrain clearance |
| **Transponder** | ATC identification | Mode A+C for altitude reporting |

> **No GPS. No TACAN. No moving map.** Primary navigation is by ADF, VOR, dead reckoning, and visual pilotage.

### VFR Navigation Tips

- Note mission frequencies before startup — write on kneecard.
- Identify all ADF/VOR stations by Morse code ident before trusting the needle.
- Reset DG to magnetic compass heading every ~15 minutes.
- Use F10 map (`F10`) for reference; rely on cockpit instruments for realistic navigation.
- Fly low and slow — use terrain features (roads, rivers, ridgelines) for pilotage.
- Maintain at least 300 ft AGL for safety margin; use radar altimeter for low-level work.

---

## Weapons Employment

### Weapons Available
| Weapon | Mount | Type |
|---|---|---|
| M134 Minigun (×2) | Wing stub | 7.62mm, 4,000 rpm |
| 2.75-inch FFAR rockets | Wing pods | Area suppression |
| M60 Door Gun (×2) | Crew positions | 7.62mm manual |

### Master Arm
- [ ] **Armament Master Switch** — ON (`O` key)
- [ ] **Weapon select** — desired station

---

### M134 Minigun

#### Employment
- Range: up to 1,000 m effective
- Rate of fire: 4,000 rpm (high setting)
- Very effective against personnel, light vehicles, aircraft

#### Attack Run
1. [ ] **Master Arm** — ON
2. [ ] Select miniguns on armament panel
3. [ ] Dive or orbit approach
4. [ ] Aim with HUD pipper
5. [ ] Fire: `Space` or trigger
6. [ ] Short bursts: 2–3 seconds (overheating risk)

---

### M60 Door Guns

- Operated by crew (right-seat crew chief / door gunners)
- In multiplayer: crewmembers control door guns
- In single-player: AI controls door guns automatically

---

### 2.75-inch Rockets

#### M157 (7-round) / M159 (19-round) Pods

1. [ ] **Master Arm** — ON
2. [ ] Select rocket pods on armament panel
3. [ ] Set salvo quantity (1, 2, 4, or all)
4. [ ] Dive: 10°–20° toward target
5. [ ] Aim pipper on target
6. [ ] Fire at 600–1,200 m range: `Space`
7. [ ] Pull off at 400 m minimum

> **Note:** Rockets are most effective in diving runs. Hover rocket employment possible but exposes aircraft to ground fire.

## Realism Notes
- **Mast Bumping:** The DCS UH-1H accurately models mast bumping. Avoid all forward cyclic pushes under low-G. A two-blade teetering rotor has zero recovery margin once the mast is struck — rotor separation is instant and fatal.
- **LTE (Loss of Tail Rotor Effectiveness):** Wind from the left-rear arc (210°–330° relative) can cause uncommanded right yaw at hover/low speed. Forward cyclic (gain airspeed) is the cure. LTE is fully modeled in DCS.
- **Settling with Power (VRS):** Steep, slow approaches (< 30 KIAS with high power) risk vortex ring state. DCS models VRS — if the aircraft is sinking and collective isn't helping, push forward cyclic immediately.
- **Teetering Rotor — Nr management:** The two-blade rotor loses RPM faster than multi-blade systems. In autorotation, the collective must come down within 1–2 seconds of power loss. There is no margin for hesitation.
- **No FADEC:** The correlator + governor system is not automatic like FADEC. Governor failure requires the pilot to manually manage throttle to maintain Nr. Practice the manual throttle exercise regularly.
- **Torque in PSI, not %:** DCS displays torque pressure in PSI. Continuous limit is ~40 PSI; military (time-limited) is 40–48 PSI; structural limit is > 50 PSI.
- **Weapon Aiming:** There is no CCIP/CCRP. Rocket and fixed-minigun accuracy depends entirely on pilot skill with the reflex sight and manual estimation of ballistic drop and windage.
- **Countermeasures (Sim Divergence):** The standard UH-1H did not carry an IR flare dispenser as original equipment; Vietnam-era Hueys relied entirely on tactics and terrain for survivability. The DCS module includes a flare dispenser for gameplay reasons. In tactical employment: treat flares as a last-resort supplement to NOE flying — not a reliable substitute for terrain masking.

---

## Defensive Procedures

### Countermeasures — IR Flares

The DCS UH-1H is equipped with an IR flare dispenser. **No RWR. No chaff.**

#### Flare Employment
- [ ] Confirm flares loaded *(re-arm screen or mission load-out)*
- [ ] On threat detection — **dispense flares** (`]`) + **immediate break turn**
- [ ] **Descend to terrain** simultaneously — flares alone are not sufficient

> **No RWR fitted.** Threat cuing relies on visual detection (missile launch flash, smoke trail) or crew call-outs. Dispense early; do not wait for impact.

### Threat Avoidance
- [ ] Fly **NOE** (Nap-of-the-Earth) — tree-top level in threat areas
- [ ] Use **terrain masking** — hills, ridges, trees between you and threat
- [ ] **Never hover in the open** near threat SAMs or AAA
- [ ] Avoid known AAA/SAM positions by minimum 3–5 km

### SAM/AAA Evasion
1. Immediate: **descend to trees/terrain**
2. Turn perpendicular to threat radar bearing
3. Use terrain features to mask
4. Abort mission if threat too close

### Small Arms Fire
- Assume all ground fire is a threat
- **Jink** left-right while transiting
- Keep low and fast over open ground
- Do not orbit predictably over threat areas

---

## Landing Checklist

### Traffic Pattern

| Leg | Altitude (AGL) | Airspeed | Notes |
|---|---|---|---|
| **Upwind** | Climbing 200–500 ft | 60 KIAS | Turn to crosswind at 200–300 ft AGL |
| **Crosswind** | 500 ft | 70–80 KIAS | Level off at pattern altitude |
| **Downwind** | 500 ft | 80–90 KIAS | Parallel to landing direction; 500–800 ft offset |
| **Base** | Begin descent from 500 ft | 60–70 KIAS | Decelerating; turn toward landing area |
| **Final** | Descending to hover | 50–60 KIAS decelerating | Align with landing point; approach angle below |

### Normal Approach *(6–10°)*

1. - [ ] Reduce to 60 KIAS on final
2. - [ ] Establish **6–10° descent angle** — gradual deceleration
3. - [ ] Passing through **ETL (~16–24 KIAS)** — **raise collective** to maintain glidepath as translational lift diminishes; left pedal as power increases
4. - [ ] Terminate to a stable **hover at 3–5 ft AGL**
5. - [ ] **Set down** — smoothly lower collective; both skids contact simultaneously

### Steep Approach *(12–15°)*

*Use when obstacles restrict the approach path or confined landing area.*

1. - [ ] Plan approach from pattern to clear all obstacles
2. - [ ] Establish **12–15° descent angle** at 50–60 KIAS
3. - [ ] Decelerate more aggressively; maintain airspeed **above 30 KIAS** until final deceleration to hover
4. - [ ] Terminate to hover at the landing point; land normally

> **Caution:** Steep approaches with high descent rates below 30 KIAS risk Settling with Power (VRS). If rate of descent appears excessive and collective is not arresting it — push forward cyclic immediately to gain airspeed.

### Running Landing *(limited power)*

1. - [ ] Maintain **20–30 KIAS translational lift** until skid contact
2. - [ ] Touch down with forward speed; **do not attempt to hover**
3. - [ ] Skids slide forward — lower collective fully
4. - [ ] Aircraft decelerates to stop

### Go-Around

At any point in the approach:
1. **Collective** — increase smoothly to climb power (monitor torque — do not exceed limits)
2. **Cyclic** — lower nose slightly to accelerate
3. **Pedals** — left pedal for torque increase
4. **Airspeed** — accelerate to 60 KIAS (Vy)
5. Announce: *"Going around"* — re-enter pattern

> **Go around early, go around often.** No penalty for a go-around. Forcing a bad approach is the hazard.

---

## Shutdown Checklist

### Pre-Shutdown

- [ ] **Landing area** — position and align aircraft
- [ ] **Collective** — FULL DOWN; both skids firmly on ground
- [ ] **Transponder** — OFF or STANDBY
- [ ] **Radios** — make shutdown/parking call; leave on as needed
- [ ] **Throttle** — IDLE detent *(reduce to ground idle; rotor RPM decreases to idle range)*

### Engine Cooldown — **2 minutes minimum at idle**

> Allows the turbine to cool gradually. Do not skip.

### Shutdown Sequence

- [ ] **Throttle** — rotate full counterclockwise past idle detent to **CUTOFF** *(fuel flow stops)*
- [ ] **EGT** — MONITOR decreasing *(should drop smoothly)*
- [ ] **Nr / N1** — MONITOR decreasing *(rotor coasts down ~1–2 minutes)*
- [ ] **WAIT FOR ROTOR STOP** — do not exit or allow personnel to approach until rotor has fully stopped

> *Note: DCS does not model a rotor brake. The rotor coasts to a stop on its own.*

### De-energize

- [ ] **Fuel Valve** — OFF *(overhead — isolates fuel supply)*
- [ ] **Generator (GEN)** — OFF *(overhead)*
- [ ] **Battery** — OFF *(overhead — de-energizes all electrical systems)*
- [ ] **All switches** — VERIFY OFF *(scan all panels)*

### Post-Shutdown

- [ ] Walk-around inspection *(rotor blades, tail rotor, engine exhaust, skids, fluid leaks)*
- [ ] Document any discrepancies observed during flight

---

## Emergency Procedures (Detailed)

### Engine Failure / Autorotation

**Immediate action (from memory):**
1. - [ ] **Collective** — LOWER immediately *(within 1–2 seconds — Nr decays fast on the 2-blade rotor)*
2. - [ ] **Throttle** — CLOSE *(full counterclockwise to OFF)*
3. - [ ] **Airspeed** — 65 KIAS *(best glide; 55 KIAS for minimum sink)*
4. - [ ] **Pedals** — right pedal *(no torque — nose wants to yaw left; correct right)*
5. - [ ] Select landing area

**Autorotation glide:**
- Maintain **Nr 294–324 RPM** with collective — collective is the Nr management tool
- 65 KIAS gives best glide distance; 55 KIAS gives minimum rate of descent (~1,500 fpm)
- Typical descent: **1,500–2,000 fpm** at normal gross weight

**Flare and touchdown:**
1. At **~75–100 ft AGL** — apply **aft cyclic** (flare); nose rises ~20–30°; rate of descent arrests; Nr builds
2. At **~10–15 ft AGL** — **level the attitude** (forward cyclic); pull **collective firmly** to trade rotor energy for lift
3. **Touchdown** — slight nose-up; skids level; slide to stop if any forward speed remains

> **Critical:** The two-blade teetering rotor stores less energy than multi-blade systems. The collective must come down within **1–2 seconds** of power loss or Nr will decay below recovery range. The collective pull at the end is a one-time event — pull too early or too late and there is no recovery.

### Engine Fire — In Flight

1. - [ ] **Throttle** — CLOSE *(enter autorotation)*
2. - [ ] **Emergency Fuel Shutoff** — OFF *(overhead — cuts all fuel to engine)*
3. - [ ] **Cabin Heat** — OFF *(prevents smoke/fumes in cockpit)*
4. - [ ] **Autorotate** to nearest suitable area
5. After landing: **Battery** — OFF; evacuate immediately

### Hydraulic Failure

**Recognition:** Controls suddenly become extremely heavy (40–60+ lbs cyclic force).

1. - [ ] **Airspeed** — 60–80 KIAS *(most manageable control forces)*
2. - [ ] **Plan run-on landing** — avoid hover; hovering without hydraulics is dangerous
3. - [ ] Execute **running landing** at nearest suitable field (touch down at 20–30 KIAS; slide to stop)
4. After stop: normal shutdown

### Tail Rotor Failure / LTE

**In forward flight (above ETL ~24 KIAS):**
1. - [ ] **Autorotate** *(removes torque; yaw stops without anti-torque demand)*
2. - [ ] Maintain airspeed **above ETL** — vertical fin provides directional stability
3. - [ ] Execute **run-on landing** *(do not attempt to hover)*

**At hover / low speed:**
1. - [ ] **Lower collective** *(removes torque — yaw stops)*
2. - [ ] **Forward cyclic** *(gain airspeed if altitude permits — vertical fin becomes effective above ETL)*
3. - [ ] Execute emergency landing

**LTE recovery (uncommanded yaw, tail rotor still attached):**
1. - [ ] **Forward cyclic** — immediately *(gain airspeed; 15–20 knots breaks most LTE conditions)*
2. - [ ] **Lower collective** *(reduce torque demand)*
3. - [ ] **If spin develops and altitude is insufficient** — autorotate

### Low Rotor RPM / Governor Failure

**Low Nr (needle split — Nr dropping below N2):**
1. - [ ] **Collective** — LOWER *(reduce rotor load; Nr recovers)*
2. - [ ] **Throttle** — increase if engine is running *(add fuel to bring Nr up)*
3. - [ ] Recover Nr above **294 RPM** before applying collective

**Governor failure:**
1. - [ ] **GOV Switch** — OFF
2. - [ ] **Throttle** — MANUAL *(maintain Nr at 324 RPM by twisting grip)*
   - Collective up → throttle in (CW) to add fuel
   - Collective down → throttle out (CCW) to reduce fuel
3. - [ ] Smooth, deliberate collective inputs; avoid rapid changes
4. - [ ] **LAND AS SOON AS PRACTICABLE**

### Settling with Power (Vortex Ring State)

**Entry conditions:** Airspeed below ~30 KIAS + descent rate > 300 fpm + moderate-to-high power applied simultaneously.

**Recognition:** High rate of descent (1,000–3,000+ fpm) that does **not** respond to collective increase; shuddering; random pitch/roll excursions.

**Recovery:**
1. - [ ] **Forward cyclic** — aggressively *(fly out of the vortex into clean air)*
2. - [ ] **Lower collective** momentarily *(reduce downwash feeding the vortex)*
3. - [ ] Gain airspeed **above 30 KIAS** *(rotor back in clean air — normal flight resumes)*
4. - [ ] Apply power normally and climb away

> **Prevention:** Never allow a steep, slow descent (< 30 KIAS) with high power. During approaches, maintain at least 30–40 KIAS until the final deceleration to hover.

### Mast Bumping Prevention

> **No recovery is possible once the mast is struck.** Prevention is the only effective response.

- **NEVER** push forward cyclic aggressively — especially after a control input or in turbulence.
- Maintain **positive G** at all times.
- In turbulence: slow down; accept the ride.
- After power loss: lower collective smoothly — **do not push the nose over**.
- Lighter gross weight **increases** susceptibility — be more cautious at light weights.

**If low-G is encountered:**
1. - [ ] **Aft cyclic** — GENTLY *(reload the rotor disc)*
2. - [ ] **Do not** push forward cyclic
3. - [ ] Reduce collective slightly to reduce unloading

---

## Keyboard & Joystick Reference

### Engine & Systems
| Function | Key | Notes |
|---|---|---|
| Starter button | `LShift + Home` | Hold while N1 rises; release at idle |
| Engine stop (throttle cutoff) | `LShift + End` | |
| Throttle increase | `PgUp` | |
| Throttle decrease | `PgDn` | |
| Idle stop release | `LShift + PgDn` | Press to advance throttle past idle to FLY |
| Governor ON/OFF | `LCtrl + Home` | |
| Battery | `LShift + B` | |
| Generator | `LShift + G` | |
| Inverter | `LShift + I` | |
| Fuel valve | `LShift + F` | |
| Fuel boost pump | `LCtrl + B` | |

### Collective & Throttle
| Function | Key | Axis |
|---|---|---|
| Collective Up | `PgUp` | Collective axis |
| Collective Down | `PgDn` | Collective axis |
| Throttle (twist-grip) | cockpit click | Throttle axis |

### Cyclic (Stick)
| Function | Key | Axis |
|---|---|---|
| Pitch Forward/Back | `Numpad 8/2` | Stick Y |
| Roll Left/Right | `Numpad 4/6` | Stick X |
| Force Trim Release | `T` | Map to joystick button |
| Set Force Trim | `LCtrl + T` | |

### Pedals (Anti-Torque)
| Function | Key | Axis |
|---|---|---|
| Left Pedal | `Z` | Rudder axis |
| Right Pedal | `X` | Rudder axis |

### Lighting
| Function | Key |
|---|---|
| Landing light | `LCtrl + L` |
| Nav lights | `LShift + L` |
| Pitot heat | `LShift + P` |

### Weapons
| Function | Key |
|---|---|
| Master Arm | `O` |
| Fire / Rockets | `Space` or trigger |
| Dispense Flares | `]` |
| Jettison | `LAlt + J` |

### Navigation & Comms
| Function | Key |
|---|---|
| Radio Menu | `\` |
| F10 Map | `F10` |
| Transmit VHF-AM | `V` |
| Transmit UHF-AM | `Y` |
| Transmit FM | `C` |
| Pause | `P` |

---

## Cross-References
- [Mi-24 Hind Checklist →](mi-24-hind.md)
- [OH-58D Kiowa Checklist →](oh-58d-kiowa.md)
- [9-Line CAS Procedures →](../procedures/9-line-cas.md)
- [Radio Communications →](../procedures/radio-communications.md)
- [Airfield & ATC →](../procedures/airfield-atc-communications.md)

---

*Based on TM 55-1520-210-10, TM 55-1520-210-CL, and Eagle Dynamics DCS UH-1H module documentation. For simulation use only.*

<!-- Co-authored-by: Copilot <223556219+Copilot@users.noreply.github.com> -->
