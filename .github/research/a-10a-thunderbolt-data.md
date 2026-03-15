# Research Dossier: A-10A Thunderbolt II (DCS World)

**Source Notes:**
- Primary data based on DCS World A-10A Flight Manual (Eagle Dynamics/Flaming Cliffs 3).
- Real-world USAF A-10A Dash-1 (T.O. 1A-10A-1) used for comparison.
- **Discrepancy Note:** The DCS A-10A is a "Flaming Cliffs 3" level module, meaning it uses a Simplified Systems Model (SSM) compared to the A-10C. It lacks a clickable cockpit and some advanced avionics functions. However, it uses the Advanced Flight Model (AFM), so aerodynamic limits are realistic.

## 1. Operating Limitations

| Parameter | Limit | DCS vs Real World Notes |
|---|---|---|
| **Max Takeoff Weight (MTOW)** | 51,000 lbs (approx) | Standard combat MTOW is often cited around 47-50k depending on runway. Absolute max structural is ~50k. |
| **Max Landing Weight** | 46,000 lbs (Structural) | Recommended < 40,000 lbs for normal operations. |
| **G-Limits** | +7.33 G / -3.0 G (Symmetric)<br>+5.86 G (Asymmetric/Rolling) | Limits reduce with external stores. Heavily loaded A-10s are often limited to +4.0 - +5.0 G. |
| **AoA Limits** | 20-22 Units (Indicated) | Stall warning (chopper) starts ~20 units. Stall ~23 units. |
| **Crosswind Component** | 20 knots | Dry runway. 15 knots wet. |
| **Max Mach** | M 0.75 | Do not exceed. Airframe drag usually prevents reaching this in level flight. |

## 2. Performance & V-Speeds

| Regime | Speed (KIAS / Knots) | Configuration / Notes |
|---|---|---|
| **Rotation Speed (Vr)** | 135 - 150 KIAS | Dependent on weight. 140 is a good average for combat load. |
| **Takeoff Speed** | 150 - 160 KIAS | Lift-off. |
| **Landing Approach** | 130 - 140 KIAS | Final approach speed (on AoA indexer). |
| **Corner Speed** | 280 - 320 KIAS | Best maneuvering/turn rate. |
| **Best Climb (Vy)** | 200 - 220 KIAS | Clean / Light stores. |
| **Stall Speed (Vs)** | ~110 KIAS | Dirty (Gear/Flaps Down), dependent on weight. |
| **Max Speed (Vne)** | 450 KIAS | Structural limit (approximate). Low altitude. |
| **Gear Extension (Vlo)** | 200 KIAS | Do not extend above this. |
| **Flaps Limit (Vfe)** | 200 KIAS | Maneuver (MVR) & Down (DN). |
| **Canopy Open** | 50 KIAS | Taxi only. |

## 3. Emergency Procedures (Boldface/Immediate Action)

*Note: DCS A-10A uses keybinds, not clickable switches.*

### Engine Failure on Takeoff (Abort)
1. **Throttles** — IDLE
2. **Wheel Brakes** — MAX
3. **Speed Brakes** — OPEN (`LShift + B`)
4. **Jettison Stores** — (`LCtrl + W`) if unable to stop

### Engine Fire in Flight
1. **Throttles** — IDLE (Affected Engine)
2. **Fire Handle** — PULL (Keybind required, usually not default mapped - verify `Fire Extinguisher` key)
3. **Agent** — DISCHARGE
4. **Land ASAP**

### Engine Failure in Flight (Restart)
1. **Throttles** — IDLE
2. **Crossfeed** — OPEN (If fuel imbalance suspects)
3. **Ignition** — ON (Auto in A-10A usually)
4. **APU** — START (if below 15,000 ft) - `LShift + L` (Power), `LAlt + E` (Start) - *Verification needed if APU aids restart in A-10A FC3*
5. **Engine Start** — `RAlt + Home` (Left) / `RCtrl + Home` (Right)

### Hydraulic Failure
1. **Monitor** — Left/Right System Pressures.
2. **Flight Controls** — Enable Manual Reversion (`LCtrl + L` or similar if modeled) if both fail.
3. **Gear** — Emergency Extend (`LShift + LCtrl + G` - verify bind).
4. **Brakes** — Emergency Brakes (Accumulator only).

### Electrical Failure
1. **Reduce Load** — Turn off unnecessary avionics.
2. **Battery** — 20 mins approx.
3. **Get Visual** — Navigation will fail (CDU/HUD).

### Spin Recovery
1. **Throttles** — IDLE
2. **Stick** — NEUTRAL / AFT slightly
3. **Rudder** — FULL OPPOSITE to spin
4. **Recover** — Dive recovery once rotation stops.

### Ejection Sequence
1. **Eject** — `LCtrl + E` (x3)
