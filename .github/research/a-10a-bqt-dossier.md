# Research Dossier: A-10A Basic Qualification Training (BQT)

> **Aircraft:** Fairchild Republic A-10A Thunderbolt II
> **Course Level:** Basic Qualification (Level 100)
> **Reference:** T.O. 1A-10A-1 Flight Manual / DCS Flaming Cliffs 3 Module
>
> **DCS Module Note:** The A-10A is a **Flaming Cliffs 3 (FC3)** simplified-systems module. It has NO clickable cockpit — all systems are controlled via keyboard bindings. However, it uses the **Advanced Flight Model (AFM)**, so aerodynamic behavior (stalls, spins, G-limits, flight envelope) is realistic.

## Overview

This dossier provides the technical research foundation for a Basic Qualification Training course in the DCS A-10A Thunderbolt II. The course covers all phases of flight from cold-and-dark startup through safe recovery. **Combat employment (weapons delivery, CAS tactics) is out of scope** — those topics are covered in a separate Weapons Employment course.

The A-10A was designed from the outset as a close air support platform built around the GAU-8/A 30mm cannon. Its twin TF34-GE-100 high-bypass turbofan engines provide excellent loiter time and fuel efficiency at low altitude. The airframe is legendarily survivable, with redundant flight controls, self-sealing fuel tanks, and a titanium "bathtub" protecting the cockpit. These design features directly affect how the aircraft handles and how pilots must manage emergencies.

**Primary Real-World Sources:**
- T.O. 1A-10A-1 (A-10A Flight Manual / Dash-1)
- T.O. 1A-10A-34-1-1 (Non-Nuclear Weapons Delivery Manual — systems context only)
- AFMAN 11-2A-10 Vol. 3 (A-10 Operations Procedures)
- AFMAN 11-217 (Instrument Flying Procedures)

---

## Module 1: Aircraft Systems & Aerodynamics

### 1.1 Learning Objectives

*   Student can describe the TF34-GE-100 engine characteristics including spool-up time, thrust output, and operating limitations.
*   Student can explain the A-10A fuel system layout, feed sequence, and low-fuel indications.
*   Student can describe the dual-redundant hydraulic flight control system and explain manual reversion procedures.
*   Student can identify the A-10A survivability features and explain their operational implications.
*   Student can recognize stall onset using the AOA indexer and describe departure/spin characteristics.

### 1.2 Key Data

#### 1.2.1 TF34-GE-100 Turbofan Engines

| Parameter | Value | Notes |
|---|---|---|
| **Engine Type** | General Electric TF34-GE-100 High-Bypass Turbofan | 6.2:1 bypass ratio — very quiet, efficient at low altitude |
| **Thrust (per engine)** | 9,065 lbf (40.32 kN) | Sea level static; total 18,130 lbf installed thrust |
| **Spool-Up Time** | ~4–6 seconds (idle to MIL) | Significantly faster than turbojets; high-bypass design spools quickly |
| **Idle RPM** | ~55–60% N2 | Ground idle; flight idle slightly higher |
| **Max RPM** | 100% N2 | No afterburner — MIL power is maximum |
| **EGT Limit (Start)** | 649°C (1,200°F) | Abort start if exceeded; "hot start" |
| **EGT Limit (Continuous)** | 607°C (1,125°F) | Normal operating max |
| **Oil Pressure (Min)** | 15 PSI | Below this = caution; 0 PSI = shutdown engine |
| **Fuel Flow (Cruise)** | ~1,800–2,200 lbs/hr total | Both engines, mid-altitude cruise |
| **Fuel Flow (Low Alt Combat)** | ~3,000–3,500 lbs/hr total | Full power, low altitude |

> *⚠ Realism Divergence: In the real A-10A, the pilot monitors individual N1/N2 gauges, EGT, fuel flow, and oil pressure on analog cockpit instruments. In DCS FC3, engine parameters are displayed on a simplified HUD/panel overlay. The pilot cannot interact with individual engine instruments but can monitor basic RPM and temperature via the on-screen gauges.*

#### 1.2.2 Fuel System

| Parameter | Value | Notes |
|---|---|---|
| **Internal Fuel** | 10,700 lbs (approx. 1,600 US gal) | Two main wing tanks + fuselage feeder cells |
| **External Tanks** | 2 × 600 US gal (optional) | Stations 3 and 9 |
| **Fuel Type** | JP-8 (JP-4 alternate) | Standard USAF |
| **Low Fuel Warning** | ~1,500 lbs remaining | Caution light on annunciator panel |
| **Bingo Fuel** | Mission dependent | Typically 2,500–3,000 lbs for RTB |
| **Feed Sequence** | Wing tanks → Fuselage cells (automatic) | Crossfeed valve for balancing |

*   **Self-Sealing Tanks:** The A-10A's internal fuel tanks are filled with reticulated polyurethane foam and are self-sealing, designed to survive 23mm HEI hits. In DCS, fuel leaks from combat damage are modeled.
*   **Fuel Dump:** Not available on the A-10A. If overweight for landing, the pilot must burn off fuel or jettison stores.

> *⚠ Realism Divergence: Real A-10A pilots manage fuel balance via a cockpit crossfeed switch and monitor individual tank quantities. In DCS FC3, fuel management is simplified — the system auto-feeds and the pilot sees only total fuel remaining on the HUD.*

#### 1.2.3 Flight Control System

| System | Description |
|---|---|
| **Primary** | Dual-redundant hydraulic (Left + Right systems, 3,000 PSI each) |
| **Backup** | Manual reversion — direct mechanical linkage to all surfaces |
| **Control Surfaces** | Ailerons, elevators, rudders, split speed brakes |
| **Trim** | Electric pitch, roll, and rudder trim |
| **Flaps** | Three positions: UP, MVR (Maneuver / 7°), DN (Down / 20°) |
| **Speed Brakes** | Split surfaces on aft fuselage; extend symmetrically |

*   **Manual Reversion:** The A-10A is one of the few modern jets that can be flown with BOTH hydraulic systems failed. In manual reversion, stick forces increase dramatically (60–80 lbs estimated), but the aircraft remains controllable. Pitch trim still functions electrically.
*   **Dual Hydraulic Independence:** Each system powers one side of the flight controls. Loss of one system still provides full-authority hydraulic control on the other side, with degraded control on the failed side.

> *⚠ Realism Divergence: In the real A-10A, manual reversion requires significant physical effort — pilots report needing both hands on the stick. DCS models the increased control sluggishness but obviously cannot simulate the physical force required. The flight model does increase control response lag and reduce control authority when hydraulics fail.*

#### 1.2.4 Survivability Features

| Feature | Description | Operational Impact |
|---|---|---|
| **Titanium Bathtub** | 1,200 lb titanium alloy enclosure around cockpit | Protects pilot from ground fire up to 23mm; affects CG |
| **Redundant Flight Controls** | Dual hydraulic + manual reversion | Fly-home capability with catastrophic damage |
| **Redundant Engines** | Wide-spaced nacelles, separated by fuselage | One engine loss = controllable asymmetric flight |
| **Self-Sealing Fuel** | Foam-filled, self-sealing tanks | Reduces fire/explosion risk from combat hits |
| **ACES II Ejection Seat** | Zero-zero capable | Safe ejection from 0 altitude / 0 airspeed |
| **Triple-Redundant Structures** | Overlapping spars/skins in wing and tail | Can lose significant structure and continue flight |

#### 1.2.5 Stall Characteristics

| Parameter | Value | Notes |
|---|---|---|
| **Stall Warning Onset** | ~20 AoA units | Buffet and tone; indexer shows full "donut" + chevron |
| **Full Stall** | ~23 AoA units | Nose drops; may roll/yaw if uncoordinated |
| **Stall Speed (Clean)** | ~130 KIAS | Light weight; increases significantly with stores |
| **Stall Speed (Dirty)** | ~110 KIAS | Gear/flaps down, light weight |
| **Departure Susceptibility** | Low to Moderate | Straight-wing design is very stall-resistant; departure usually from aggressive aft stick + yaw |
| **Spin Characteristics** | Recoverable | Standard spin recovery: idle / neutral stick / opposite rudder; typically recovers in 1–2 turns |

*   **AOA Indexer:** Three-light system on the left canopy bow:
    - **Green donut (○):** On-speed (correct AoA for approach)
    - **Amber chevron up (∧):** Slow / high AoA — add power / lower nose
    - **Amber chevron down (∨):** Fast / low AoA — reduce power / raise nose
    - **Combination lights** indicate transitional states

> *⚠ Realism Divergence: The real A-10A has a physical AOA indexer mounted on the canopy frame plus an AOA gauge on the instrument panel. In DCS FC3, the AOA indexer information is presented on the HUD overlay. The behavior and thresholds are the same — only the presentation differs.*

### 1.3 DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Throttle Up** | `Num +` (or HOTAS throttle axis) | Both engines simultaneously |
| **Throttle Down** | `Num -` | Both engines simultaneously |
| **Left Engine Start** | `RAlt + Home` | |
| **Right Engine Start** | `RCtrl + Home` | |
| **Left Engine Stop** | `RAlt + End` | |
| **Right Engine Stop** | `RCtrl + End` | |
| **Flaps Up** | `LShift + F` | Cycles: DN → MVR → UP |
| **Flaps Down** | `LCtrl + F` | Cycles: UP → MVR → DN |
| **Speed Brakes Open** | `LShift + B` | |
| **Speed Brakes Close** | `LCtrl + B` | |
| **Trim: Nose Up** | `RCtrl + ;` | |
| **Trim: Nose Down** | `RCtrl + .` | |
| **Trim: Left** | `RCtrl + ,` | Roll trim |
| **Trim: Right** | `RCtrl + /` | Roll trim |
| **Rudder Trim Left** | `RCtrl + Z` | |
| **Rudder Trim Right** | `RCtrl + X` | |

### 1.4 Instructor Notes

*   **"The Hog Doesn't Hurry":** Emphasize from Day 1 that the A-10A is a slow, deliberate aircraft. Max speed is ~380 KTAS at sea level. Students coming from fighters will struggle with the pace. Frame this as an advantage: more time to think, observe, and plan.
*   **Engine Response:** Unlike the Su-25T's turbojets, the TF34 turbofan spools relatively quickly (~4–6 sec idle-to-MIL vs. 9–12 sec for the R-195). This is a significant safety advantage on approach, but students should still be taught to anticipate power needs rather than react to them.
*   **Trim Discipline:** The A-10A has no fly-by-wire augmentation. Every speed change, every configuration change, every power change requires a trim adjustment. Students who "fight the stick" will fly imprecise profiles and fatigue quickly.
*   **AOA Indexer Reliance:** Teach students to fly approaches by AOA indexer, not by airspeed alone. Airspeed varies with weight; AOA indexer always gives the correct energy state.

### 1.5 Realism Divergence Notes

*   **Cockpit Interaction:** The most significant divergence is the FC3 simplified cockpit. Real A-10A pilots interact with hundreds of switches, circuit breakers, and panels. DCS FC3 reduces this to keyboard shortcuts. All procedural steps that reference "switch to ON" should be understood as "press the assigned keybind."
*   **INS/NAV System:** The real A-10A uses an AN/ASN-141 INS that requires 4–8 minutes of ground alignment. DCS FC3 provides instant navigation alignment on power-up.
*   **Caution/Warning Panel:** The real aircraft has a Master Caution panel with dozens of individual advisory lights. DCS FC3 provides simplified warning messages.

---

## Module 2: Ground Operations

### 2.1 Learning Objectives

*   Perform cold-and-dark power-up sequence using correct keybind order.
*   Execute dual engine start without exceeding EGT limits.
*   Verify post-start systems indications (hydraulics, electrical, avionics).
*   Taxi safely using nose wheel steering and differential braking.
*   Perform pre-takeoff run-up and checklist items.

### 2.2 Key Data

#### 2.2.1 Startup Sequence

| Step | Action | Keybind | Indication |
|---|---|---|---|
| 1 | **Electrical Power ON** | `RShift + L` | HUD and gauges energize |
| 2 | **Left Engine Start** | `RAlt + Home` | RPM rises, EGT rises then stabilizes; idle ~55–60% N2 |
| 3 | **Wait for Left to Stabilize** | — | Oil pressure > 15 PSI, EGT < 607°C |
| 4 | **Right Engine Start** | `RCtrl + Home` | Same indications as left engine |
| 5 | **Wait for Right to Stabilize** | — | Both engines at stable idle |
| 6 | **Avionics/Systems Check** | Various | HUD displays, warning lights extinguish |
| 7 | **Canopy Close** | `LCtrl + C` | Visual canopy closes |
| 8 | **Nose Wheel Steering ON** | `Q` (toggle) | NWS engaged for taxi |

#### 2.2.2 Engine Start Limitations

| Parameter | Limit | Action if Exceeded |
|---|---|---|
| **EGT (during start)** | 649°C (1,200°F) | Abort start — motor to cool, attempt restart |
| **Hung Start** | RPM stagnates below idle | Abort — fuel off, motor, reattempt |
| **Hot Start** | EGT rising above limit | Fuel off immediately; motor dry for 30 sec |
| **Start Interval** | 30 sec minimum between attempts | Allow engine to soak/cool |
| **Max Start Attempts** | 3 before extended cool-down | Prevent starter damage |

> *⚠ Realism Divergence: In the real A-10A, the engine start involves a detailed sequence: battery ON, APU start (or GPU connection), throttle from OFF to IDLE at specified RPM, monitoring a dedicated EGT gauge, and listening for abnormal sounds. In DCS FC3, the start is a single keybind per engine. The simulation does model hot starts and hung starts via the flight model, but the pilot cannot intervene with the same granularity as the real cockpit.*

#### 2.2.3 Taxi Procedures

| Parameter | Value | Notes |
|---|---|---|
| **NWS Authority** | ~±60° (full range) | Very responsive; use gentle inputs |
| **Taxi Speed (Straight)** | 15–20 knots | Moderate power sufficient |
| **Taxi Speed (Turns)** | < 10 knots | Prevent tire side-loading |
| **Brake Application** | Toe brakes / `W` key | Smooth, progressive — avoid locking wheels |
| **Canopy Limit (Open)** | 50 KIAS | Close before runway |

### 2.3 DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Power ON** | `RShift + L` | Master electrical |
| **Left Engine Start** | `RAlt + Home` | |
| **Right Engine Start** | `RCtrl + Home` | |
| **Left Engine Stop** | `RAlt + End` | |
| **Right Engine Stop** | `RCtrl + End` | |
| **Canopy Open/Close** | `LCtrl + C` | Toggle |
| **NWS Toggle** | `Q` | Engage before taxi |
| **Wheel Brakes** | `W` | Hold to apply |
| **Parking Brake** | `LCtrl + W` | Toggle |
| **Navigation Lights** | `RCtrl + L` | |
| **Landing Light** | `LAlt + L` | For night taxi |
| **Anti-Collision Light** | `RShift + RCtrl + L` | Beacon; indicates engines running |

### 2.4 Instructor Notes

*   **Start Simplicity is Deceptive:** Because FC3 starts are single-keybind, students may rush. Enforce the discipline of watching RPM and EGT stabilize before starting the second engine. This builds habits that transfer to the A-10C module.
*   **NWS Sensitivity:** The A-10A NWS is much more responsive than students expect. Brief, small rudder inputs during taxi prevent the nose from hunting left-right. Full deflection at speed will depart the taxiway.
*   **Brake Discipline:** Teach "speed brakes for speed, wheel brakes for stop." On long taxi, students tend to ride the brakes, which causes overheating. Use power reduction first, brakes only for final deceleration and turns.
*   **Warm-Up Period:** Though DCS allows immediate taxi, teach the discipline of 1–2 minutes of idle warm-up after start. This allows hydraulic pressures to stabilize and simulates proper real-world procedure.

### 2.5 Realism Divergence Notes

*   **GPU/APU Procedures:** Real A-10A starts typically use external GPU power. The APU (JFS — Jet Fuel Starter on some variants) is used for autonomous starts. DCS FC3 does not model GPU connection or APU operation — engines start directly.
*   **Circuit Breaker Scan:** Real pre-start includes verifying all circuit breakers are in. DCS FC3 has no circuit breakers.
*   **Intercom/Comm Check:** Real-world includes checking UHF/VHF radios and intercom with ground crew. DCS FC3 auto-tunes radios.
*   **Flight Control Check:** Real-world includes full-throw control check with visual confirmation by ground crew. In DCS, the student should still cycle all controls visually checking surface movement using external view (`F2`).

---

## Module 3: Takeoff & Departure

### 3.1 Learning Objectives

*   Configure aircraft for takeoff (flaps, trim, controls check).
*   Execute normal takeoff maintaining runway centerline.
*   Rotate at correct Vr for current weight.
*   Perform "clean-up" (gear/flap retraction) on correct schedule.
*   Recognize and execute Rejected Takeoff (RTO) decision.

### 3.2 Key Data

#### 3.2.1 Takeoff Configuration

| Item | Setting | Notes |
|---|---|---|
| **Flaps** | MVR (Maneuver / 7°) | Standard takeoff setting |
| **Trim** | Slightly nose-up | 1–2 units; aircraft should be slightly tail-heavy |
| **Speed Brakes** | Closed | Verify before roll |
| **NWS** | Engaged | For directional control during roll |
| **Canopy** | Closed and locked | |
| **Parking Brake** | Set until ready | Release to begin roll |

#### 3.2.2 V-Speeds by Weight Class

| Weight Class | Gross Weight (lbs) | Vr (KIAS) | Vlof (KIAS) | V2 / Initial Climb (KIAS) |
|---|---|---|---|---|
| **Light (Training)** | 30,000–35,000 | 120–130 | 135–140 | 150–160 |
| **Normal (Partial Stores)** | 35,000–42,000 | 130–140 | 145–155 | 160–170 |
| **Heavy (Max Fuel + Stores)** | 42,000–50,000 | 140–150 | 155–165 | 170–180 |

#### 3.2.3 Climb Speeds

| Profile | Speed (KIAS) | Usage |
|---|---|---|
| **Vx (Best Angle)** | 160–170 | Obstacle clearance; max altitude per ground distance |
| **Vy (Best Rate)** | 200–220 | Standard departure; max altitude per time |
| **En Route Climb** | 250–280 | Cruise climb; faster transit |

#### 3.2.4 Gear & Flap Schedule

| Action | Condition | Keybind |
|---|---|---|
| **Gear Retract** | Positive rate of climb confirmed | `G` |
| **Flaps MVR → UP** | Above 150 KIAS and 200 ft AGL | `LShift + F` |
| **Gear Limit Speed** | < 200 KIAS | Do not extend/retract above this |
| **Flap Limit Speed** | < 200 KIAS | DN and MVR positions |

### 3.3 DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Flaps Maneuver** | `LShift + F` / `LCtrl + F` | Cycle to desired position |
| **Gear Up** | `G` | Single press toggles |
| **Gear Down** | `G` | Single press toggles |
| **NWS Toggle** | `Q` | Disengage after liftoff |
| **Parking Brake** | `LCtrl + W` | Release to begin roll |
| **Speed Brakes Close** | `LCtrl + B` | Verify closed before takeoff |
| **Wheel Brakes** | `W` | For RTO |
| **Emergency Jettison** | `LCtrl + W` | Stores jettison for RTO if unable to stop |

### 3.4 Instructor Notes

*   **Rotation Technique:** The A-10A rotates gently. Pulling too aggressively causes a pitch rate that can lead to tail strike — the main gear is far aft and the empennage is low. Teach a smooth 2–3°/sec pitch rate to 8–10° nose-up.
*   **Directional Control:** The A-10A has excellent directional stability on the ground due to the wide-track main gear. However, crosswinds require active rudder. Teach students to position the rudder INTO the crosswind during the roll and reduce correction as speed builds.
*   **RTO Decision Speed:** A useful rule of thumb is 100 KIAS — below this, an abort is almost always preferable. Above 100 KIAS with more than half the runway remaining, continue unless there is a fire, engine failure, or flight control malfunction.
*   **Asymmetric Thrust on Takeoff:** If an engine fails during the takeoff roll, the yaw is immediate and significant. The wide engine spacing creates a large yaw moment. Rudder and differential braking must be instantaneous.
*   **Climb-Out Error:** Students often retract flaps too early. Wait until 150 KIAS and 200 ft AGL minimum. Premature flap retraction at low speed causes sink.

### 3.5 Realism Divergence Notes

*   **Takeoff Checklist:** Real A-10A pilots run a formal pre-takeoff checklist including INS alignment verification, armament safety, and flight control check with visual ground crew confirmation. DCS FC3 does not require INS alignment and has no ground crew interaction.
*   **Anti-Skid System:** The real A-10A has an anti-skid braking system that prevents tire lockup during RTO. DCS FC3 models anti-skid behavior but the pilot has no toggle for it — it is always active.
*   **Afterburner:** The TF34-GE-100 has NO afterburner. MIL power is maximum. Students accustomed to afterburner-equipped aircraft must adjust their expectations of acceleration and climb performance.

---

## Module 4: Basic Flight Maneuvers

### 4.1 Learning Objectives

*   Maintain straight-and-level flight at assigned altitude and heading within ±100 ft and ±5°.
*   Execute coordinated 30°, 45°, and 60° banked turns maintaining altitude within ±100 ft.
*   Perform climbs and descents at assigned airspeeds within ±10 KIAS.
*   Demonstrate slow flight with flaps extended, maintaining controlled flight to buffet onset.
*   Recognize approach-to-stall indications and execute prompt recovery.
*   Demonstrate proper trim technique during speed and configuration changes.

### 4.2 Key Data

#### 4.2.1 Cruise Performance

| Altitude | Power Setting | Speed (KIAS) | Fuel Flow (Total, lbs/hr) |
|---|---|---|---|
| **Low (1,000–5,000 ft)** | 70–80% N2 | 250–300 | 2,200–2,800 |
| **Medium (10,000–15,000 ft)** | 75–85% N2 | 280–320 | 1,800–2,400 |
| **Loiter** | 60–65% N2 | 200–220 | 1,400–1,800 |
| **Max Endurance** | ~62% N2 | ~180 | ~1,200 |

#### 4.2.2 Load Factor / Turn Performance

| Bank Angle | G-Load | Stall Speed Multiplier | Notes |
|---|---|---|---|
| **30°** | 1.15 G | 1.07× | Gentle maneuvering |
| **45°** | 1.41 G | 1.19× | Standard tactical turn |
| **60°** | 2.0 G | 1.41× | Aggressive; monitor AoA |
| **Max Structural** | 7.33 G (clean) | — | Reduce with stores; typically limit to 4–5 G loaded |

#### 4.2.3 AoA Reference

| Condition | AoA (Units) | Indication |
|---|---|---|
| **Optimum Cruise** | 6–8 | Quiet flight |
| **Approach (On-Speed)** | 14–16 | Green donut on indexer |
| **Buffet Onset** | 18–20 | Light airframe buffet; indexer amber UP |
| **Stall Warning** | 20–22 | Strong buffet, aural tone, stick shaker |
| **Full Stall** | 23+ | Nose drops; possible wing rock |

#### 4.2.4 Slow Flight Configuration

| Configuration | Min Controllable Speed (KIAS) | Flap Position | Notes |
|---|---|---|---|
| **Clean** | ~140–150 | UP | Light weight |
| **MVR Flaps** | ~125–135 | MVR (7°) | Transition to approach |
| **Full Flaps + Gear** | ~110–120 | DN (20°) | Landing configuration |

### 4.3 DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Pitch Trim Up** | `RCtrl + ;` | Small increments |
| **Pitch Trim Down** | `RCtrl + .` | Small increments |
| **Roll Trim Left** | `RCtrl + ,` | |
| **Roll Trim Right** | `RCtrl + /` | |
| **Rudder Trim Left** | `RCtrl + Z` | |
| **Rudder Trim Right** | `RCtrl + X` | |
| **Flaps Cycle** | `LShift + F` / `LCtrl + F` | |
| **Autopilot Engage** | `A` | Altitude/heading hold |
| **Autopilot Disengage** | `LAlt + A` | Or any control input |
| **Speed Brakes** | `B` (toggle) or `LShift/LCtrl + B` | For descent management |

### 4.4 Instructor Notes

*   **"Fly the AOA":** Reinforce that AoA is the primary energy management tool, not airspeed. Airspeed varies with weight and altitude; AoA is consistent. In DCS FC3, the HUD AoA readout is the student's primary reference.
*   **Trim, Trim, Trim:** The A-10A has no SAS (Stability Augmentation System) or CAS (Control Augmentation System). It is a purely manual aircraft with hydraulic boost. Every power change, configuration change, or speed change requires re-trimming. Students who fight the stick will tire and fly sloppy profiles.
*   **Coordinated Flight:** The A-10A requires active rudder coordination in turns. The twin engines and large vertical tails create adverse yaw. Students must use rudder to keep the ball centered, especially in steep turns.
*   **Energy Awareness:** At low altitude and heavy weight, the A-10A has very limited excess thrust. Energy management becomes critical. Students must learn to trade altitude for airspeed and vice versa, especially in the traffic pattern.
*   **Stall Recovery Priority:** Nose down → Wings level → Power. In that order. Students instinctively pull power first, which doesn't reduce AoA. The critical first action is reducing AoA by lowering the nose.
*   **Speed Brake as Descent Tool:** Teach students to use speed brakes aggressively for descents rather than nosing over and building excessive speed. The A-10's split speed brakes are very effective and introduce minimal pitch change.

### 4.5 Realism Divergence Notes

*   **Autopilot:** The real A-10A has a basic attitude-hold autopilot that maintains pitch and bank angles. DCS FC3 provides a simplified autopilot that holds altitude and heading. The behavior is similar but not identical.
*   **Stick Forces:** In the real aircraft, stick forces are moderate in normal flight but increase significantly at high speed or in manual reversion. DCS cannot simulate physical stick forces, but students using force-feedback sticks may notice some variation.
*   **Aural Warnings:** The real A-10A has an aural AoA tone system that increases in pitch as AoA increases. DCS models this sound, but the fidelity varies.

---

## Module 5: Emergency Procedures (Academic)

### 5.1 Learning Objectives

*   Identify single-engine failure symptoms and execute the correct immediate action items.
*   Describe the procedure for securing a failed engine and setting up for single-engine approach.
*   Describe hydraulic system failure indications and the transition to manual reversion.
*   Describe the fire warning system and correct emergency response.
*   State the minimum altitude / conditions for controlled ejection using the ACES II seat.

### 5.2 Key Data

#### 5.2.1 Single Engine Operations

| Parameter | Value | Notes |
|---|---|---|
| **Vmca (Min Control — Air)** | ~120 KIAS | Below this, directional control may be insufficient |
| **Single-Engine Climb Rate** | ~500–1,500 fpm | Depends on weight and altitude; may be negative at heavy weight/high altitude |
| **Single-Engine Approach Speed** | +10 KIAS over normal | Add speed for reduced go-around capability |
| **Max Asymmetric Thrust** | ~9,000 lbf yaw moment | Wide engine spacing = large yaw moment; immediate rudder required |

#### 5.2.2 Boldface / Immediate Action Items

**ENGINE FAILURE / FIRE IN FLIGHT:**
1. **Throttle (affected)** — IDLE
2. **Identify** — confirm which engine (yaw direction, RPM, EGT)
3. **Throttle (affected)** — OFF (`RAlt + End` or `RCtrl + End`)
4. **Fire Handle** — PULL (if fire warning)
5. **Agent** — DISCHARGE (if fire persists)
6. **Maintain** — wings level, ball centered with rudder
7. **Land ASAP**

**ENGINE FAILURE ON TAKEOFF (below Vr):**
1. **Throttles** — IDLE
2. **Wheel Brakes** — MAX (`W`)
3. **Speed Brakes** — OPEN (`LShift + B`)
4. **Emergency Jettison** — if unable to stop (`LCtrl + W`)

**ENGINE FAILURE ON TAKEOFF (above Vr, airborne):**
1. **Maintain Directional Control** — rudder into good engine
2. **Climb** — if positive rate, continue; clean up gear/flaps
3. **If No Climb** — jettison stores (`LCtrl + W`), consider landing ahead
4. **Do NOT attempt to return** — to the airfield until above 500 ft AGL and > 150 KIAS

#### 5.2.3 Hydraulic Failure

| Scenario | Indication | Action |
|---|---|---|
| **Single System Failure** | HYD PRESS caution (one side) | Other system provides full control; land when practical |
| **Dual System Failure** | Both HYD PRESS cautions | Manual reversion — heavy stick forces; declare emergency; fly gentle maneuvers; wide pattern |
| **Emergency Gear Extension** | Gear won't extend normally | `LShift + LCtrl + G` — gravity/pneumatic drop |
| **Emergency Brakes** | Normal brakes failed | Accumulator provides approximately 6 brake applications |

#### 5.2.4 ACES II Ejection Seat

| Parameter | Value | Notes |
|---|---|---|
| **Ejection System** | ACES II (Advanced Concept Ejection Seat) | Zero-zero capable |
| **Mode 1 (Low Speed)** | 0–250 KEAS, any altitude | Parachute deployment by drogue, then main canopy |
| **Mode 2 (High Speed)** | 250–600 KEAS | Delayed opening; windblast protection |
| **Minimum Altitude (Controlled)** | 0 ft (zero-zero) | Seat is designed for ground-level ejection |
| **Recommended Decision Altitude** | 2,000 ft AGL | Below this, recovery from unusual attitudes may be impossible |
| **DCS Ejection** | `LCtrl + E` (×3) | Triple-press required as safety interlock |

### 5.3 DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Left Engine Stop** | `RAlt + End` | Secure failed engine |
| **Right Engine Stop** | `RCtrl + End` | Secure failed engine |
| **Left Engine Restart** | `RAlt + Home` | Attempt air restart |
| **Right Engine Restart** | `RCtrl + Home` | Attempt air restart |
| **Speed Brakes Open** | `LShift + B` | |
| **Speed Brakes Close** | `LCtrl + B` | |
| **Emergency Gear Extend** | `LShift + LCtrl + G` | |
| **Stores Jettison** | `LCtrl + W` | Emergency jettison |
| **Ejection** | `LCtrl + E` (×3) | Triple-press to eject |
| **Fire Extinguisher** | Check keybind mapping | May need to be manually mapped |

### 5.4 Instructor Notes

*   **"Dead Foot, Dead Engine":** Teach this mnemonic. When an engine fails, the aircraft yaws toward the dead engine. The foot that requires NO rudder pressure is on the dead engine side. The pilot must push the OPPOSITE rudder (the active foot).
*   **The 2,000-Foot Rule:** If the aircraft is below 2,000 ft AGL and uncontrollable (spin, unrecoverable dive, total control failure), the decision is EJECT. Do not waste altitude trying heroic recoveries below this floor.
*   **Single-Engine Landing:** The A-10A lands very well on one engine. The approach speed increase is modest (+10 KIAS). The critical risk is a go-around on one engine — climb performance may be marginal. Commit to the approach.
*   **Manual Reversion Landing:** Practice this in training! The aircraft is controllable but sluggish. Fly a wide pattern, use gentle inputs, and plan a long straight-in approach. Precision maneuvers are nearly impossible.
*   **DCS Engine Restart:** In DCS FC3, an in-flight engine restart is attempted by pressing the engine start key. It may or may not succeed depending on the failure type. Wind-milling restart above 200 KIAS has the best chance.

### 5.5 Realism Divergence Notes

*   **Fire Detection / Suppression:** The real A-10A has a fire detection system with engine bay fire loops and a two-shot extinguishing system per engine. DCS FC3 simplifies this — fire warnings appear, but the detailed fire suppression panel is not interactive.
*   **Emergency Oxygen:** Real emergency procedures include verifying emergency oxygen. DCS does not model pilot oxygen systems.
*   **Dual Engine Failure:** In the real aircraft, dual engine failure at altitude allows glide to an airfield or suitable landing site (A-10A glide ratio is approximately 17:1 clean). DCS models this glide behavior accurately.
*   **Hydraulic Accumulator:** The real A-10A has hydraulic accumulators that provide limited control authority (approximately 6 full gear cycles or equivalent brake applications) after total hydraulic failure. DCS models this degraded capability.

---

## Module 6: Approach & Landing

### 6.1 Learning Objectives

*   Fly a standard VFR rectangular traffic pattern at correct altitudes and airspeeds.
*   Configure the aircraft for each pattern leg (downwind, base, final).
*   Fly final approach using AOA indexer as primary reference.
*   Execute a stabilized approach to touchdown with correct flare technique.
*   Perform rollout with directional control and appropriate braking.
*   Execute a go-around from any point in the pattern.

### 6.2 Key Data

#### 6.2.1 VFR Traffic Pattern

| Leg | Altitude (AGL) | Speed (KIAS) | Configuration | Notes |
|---|---|---|---|---|
| **Upwind** | Climbing | 150–170 | Gear UP, Flaps UP | Departure leg; climbing through pattern altitude |
| **Crosswind** | 1,000–1,500 ft | 180–200 | Clean | Turn when 30° off departure end |
| **Downwind** | 1,500 ft AGL | 180–200 | Clean initially | Parallel to runway; abeam threshold: begin checklist |
| **Abeam / Pre-Landing** | 1,500 ft | Decelerating to 160–170 | Gear DOWN, Flaps MVR → DN | Gear down abeam the threshold |
| **Base Turn** | Descending | 150–160 | Gear DOWN, Flaps DN | Begin descent; ~500 fpm |
| **Final** | Descending | 130–140 | Gear DOWN, Flaps DN | AOA indexer: green donut |
| **Short Final** | 200–100 ft | 130–135 | Full landing config | Stable; no corrections below 100 ft |

#### 6.2.2 AOA Indexer Targets (Final Approach)

| Indexer Display | AoA State | Action |
|---|---|---|
| **▽ (Chevron Down — Amber)** | Fast / Low AoA | Reduce power; allow slight pitch up |
| **○ (Donut — Green)** | On-Speed / Correct AoA | Maintain; this is the target |
| **△ (Chevron Up — Amber)** | Slow / High AoA | Add power; lower nose slightly |
| **△ + ○ (Chevron + Donut)** | Slightly Slow | Small power addition |
| **▽ + ○ (Chevron + Donut)** | Slightly Fast | Small power reduction |

#### 6.2.3 Landing Data

| Parameter | Value | Notes |
|---|---|---|
| **Touchdown Speed** | 120–130 KIAS | Weight dependent |
| **Touchdown Attitude** | 5–8° nose up | "Flat" compared to fighters; slight flare |
| **Approach AoA** | 14–16 units | Green donut |
| **Normal Landing Roll** | 2,000–3,000 ft | Dry runway, normal weight |
| **Max Landing Weight** | 46,000 lbs (structural) | Recommended < 40,000 lbs normal ops |
| **Crosswind Limit** | 20 knots (dry) / 15 knots (wet) | |

### 6.3 DCS Keybind Reference

| Action | Default Keybind | Notes |
|---|---|---|
| **Gear Toggle** | `G` | Verify three green (or visual gear indicators) |
| **Flaps Down (Landing)** | `LCtrl + F` | Cycle to DN (20°) |
| **Flaps Up** | `LShift + F` | For go-around |
| **Speed Brakes** | `B` (toggle) | Close before touchdown |
| **Wheel Brakes** | `W` | Apply after nosewheel contact |
| **Drag Chute Deploy** | `P` | Deploy on touchdown — *if available on the variant* |
| **NWS Engage** | `Q` | Engage after nosewheel contact for rollout |
| **Anti-Skid** | Always active | Cannot be toggled in FC3 |
| **Tailhook** | `H` | Emergency arresting — if arresting cable available |

### 6.4 Instructor Notes

*   **The "Flat" Landing:** The A-10A does not flare dramatically like a fighter. The approach is flown at a relatively shallow glideslope (~3°), and the flare is a gentle pitch increase of 2–3° to arrest the descent rate. The main gear touches first with the nosewheel following almost immediately. Over-flaring causes a float that wastes runway.
*   **Power Management on Final:** This is the number one area where students struggle. The A-10A's TF34 engines respond relatively quickly, but students must still be AHEAD of the aircraft. If you're correcting on short final, you're already late. Teach: "Set the power on base turn and make tiny corrections."
*   **The "Donut Chase":** Students fixate on keeping the AOA indexer exactly on the green donut and make constant power/pitch changes. This creates a PIO (Pilot-Induced Oscillation) on approach. Teach: "Accept a half-chevron deviation. Small, smooth corrections. Don't chase perfection."
*   **Go-Around Execution:** Full power → Establish positive climb → Gear UP → Flaps MVR. Do NOT raise gear until a positive rate of climb is confirmed. Students panic and retract gear while still descending, which guarantees a gear-up landing.
*   **Crosswind Technique:** The A-10A uses a wing-low (sideslip) method for crosswind landings. Crab on final, transition to wing-low on short final (300–200 ft), and touch down on the upwind main gear first. Do NOT land in a crab — side-loads on the wide-track gear can collapse it.
*   **Braking Technique:** After touchdown: nosewheel on the runway → NWS ON → smooth progressive braking. Do NOT slam the brakes immediately — at 120+ KIAS, aggressive braking causes tire hydroplaning (wet) or flat-spotting (dry). Let speed decay to ~80 KIAS, then increase braking progressively.

### 6.5 Realism Divergence Notes

*   **Drag Chute:** The real A-10A does NOT have a drag chute. The DCS `P` key deploys a drag chute on some aircraft but this function is not applicable to the A-10A. Landing rollout relies entirely on wheel brakes and aerodynamic drag from speed brakes.
*   **Precision Approach Path Indicator (PAPI):** Real-world airfields have PAPI/VASI visual glideslope indicators. DCS models these on many airfields. Teach students to use them: two red / two white = on glidepath.
*   **ILS/Instrument Approach:** The real A-10A is fully ILS-capable with an HSI and CDI. DCS FC3 provides a simplified ILS overlay. Instrument approaches are out of scope for BQT but students should know the capability exists.
*   **Touch-and-Go:** In the real A-10A, touch-and-go practice involves: touchdown → throttles to MIL → flaps MVR → accelerate → rotate. DCS models this correctly. Ensure students retrim for takeoff during the roll.

---

## Appendix A: Quick Reference Card

### Critical V-Speeds (Normal Training Weight ~35,000 lbs)

| Parameter | Speed (KIAS) |
|---|---|
| **Vs (Stall, Dirty)** | ~110 |
| **Vs (Stall, Clean)** | ~130 |
| **Vr (Rotation)** | 130 |
| **V2 (Initial Climb)** | 160 |
| **Vx (Best Angle)** | 165 |
| **Vy (Best Rate)** | 210 |
| **Cruise** | 250–300 |
| **Vfe (Flaps)** | 200 |
| **Vlo (Gear)** | 200 |
| **Corner Speed** | 300 |
| **Vne** | 450 |
| **Final Approach** | 135 |
| **Touchdown** | 125 |

### Emergency Keybinds

| Action | Keybind |
|---|---|
| **Eject** | `LCtrl + E` (×3) |
| **Emergency Gear** | `LShift + LCtrl + G` |
| **Stores Jettison** | `LCtrl + W` |
| **Speed Brakes Open** | `LShift + B` |
| **Left Engine Stop** | `RAlt + End` |
| **Right Engine Stop** | `RCtrl + End` |

---

## Appendix B: Recommended Syllabus Flow

| Event | Title | Focus |
|---|---|---|
| **Event 1** | Academics (Ground School) | Modules 1, 5 — Systems, aero, emergency procedures |
| **Event 2** | FAM-1 (Familiarization 1) | Modules 2, 3 — Ground ops, startup, taxi, takeoff |
| **Event 3** | FAM-2 (Familiarization 2) | Module 4 — Area work: turns, climbs, descents, slow flight, stalls |
| **Event 4** | Traffic Pattern / Landing Practice | Module 6 — Pattern work: multiple approaches, full stop, touch-and-go |
| **Event 5** | Emergency Procedures (Practice) | Module 5 — Simulated single-engine, hydraulic failure, ejection criteria |
| **Event 6** | BQT Check Ride | All Modules — Comprehensive evaluation: cold start through landing |

---

*Sources: T.O. 1A-10A-1 Flight Manual (publicly available excerpts), AFMAN 11-2A-10 Vol. 3, DCS World A-10A Flaming Cliffs 3 Module Documentation (Eagle Dynamics). For simulation use only.*
