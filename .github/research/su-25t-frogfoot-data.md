# Research Dossier: Sukhoi Su-25T Frogfoot (DCS World)

**Source Notes:**
- Primary data based on DCS World Su-25T Flight Manual (Eagle Dynamics).
- Real-world Su-25 "Grach" combat manuals (translated) used for comparison.
- **Discrepancy Note:** The DCS Su-25T is a simplified flight model (SSM/AFM hybrid depending on version history, now generally AFM) compared to full fidelity modules, but accurately models structural limits. Real-world manuals often refer to the base Su-25; the 'T' variant is heavier and has different drag characteristics due to the dorsal hump.

## 1. Operating Limitations

| Parameter | Limit | DCS vs Real World Notes |
|---|---|---|
| **Max Takeoff Weight (MTOW)** | 19,500 kg (42,990 lbs) | Max combat load. Absolute max allowable. |
| **Max Landing Weight** | 13,300 kg (29,321 lbs) | Landing above this risks gear collapse or tire failure in DCS. |
| **G-Limits** | +6.5 G / -2.0 G (Clean)<br>+5.0 G (with stores) | Reduced to +5.0G with significant ordinance. EKRAN will warn "OVER-G" audibly. |
| **AoA Limits** | 20° (Normal)<br>16-18° (Loaded) | Critical AoA is ~22°. Stall warning onset approx 18-20° depending on load. |
| **Crosswind Component** | 15 m/s (approx 30 kts) | 90-degree crosswind limit. DCS ground handling can be twitchy above 12 m/s. |
| **Max Mach** | M 0.82 | Airframe drag limit. |

## 2. Performance & V-Speeds

| Regime | Speed (KIAS / km/h) | Configuration / Notes |
|---|---|---|
| **Rotation Speed (Vr)** | 230-240 km/h | Loaded. 210 km/h if clean (rare). |
| **Takeoff Speed** | 260-270 km/h | Lift-off speed. |
| **Landing Approach** | 280-300 km/h | Loaded/Heavy. |
| **Landing Approach** | 250-260 km/h | Clean/Light (Pattern speed). |
| **Corner Speed** | 450-550 km/h | Best maneuvering range. |
| **Best Climb (Vy)** | 550-600 km/h | Clean. |
| **Stall Speed (Vs)** | ~180 km/h | Landing config, standard weight. Varies significantly with weight. |
| **Vne (Max Speed)** | 950 km/h (Sea Level) | Instrument redline. Structural damage above 1000 km/h. |
| **Vlo (Gear Extend)** | 400 km/h | Gear doors may jam or rip off above this in DCS. |
| **Vfe (Flaps)** | 500 km/h (Maneuver)<br>400 km/h (Takeoff/Landing) | "Maneuver" flaps are roughly 10°. "Takeoff/Landing" are full extension. |
| **Chute Deploy** | < 280 km/h | Max speed for drag chute deployment. |

## 3. Emergency Procedures (Boldface/Immediate Action)

*Note: The Su-25T in DCS does not have clickable switches for all these procedures, but keybinds exist.*

### Engine Failure on Takeoff (Abort)
1. **Throttle** — IDLE
2. **Brakes** — MAX
3. **Drag Chute** — DEPLOY (`P` / `LAlt+P`)
4. **Jettison External Stores** — (`LCtrl + W` or `LAlt + R` emergency jettison)

### Engine Fire in Flight
1. **Throttle (Affected Engine)** — IDLE
2. **Fire Extinguisher** — DISCHARGE (Automatic in Su-25T, or manual override if mapped)
3. **Affected Engine** — SHUTDOWN (`RAlt+End` / `RCtrl+End`)
4. **Land ASAP**

### Engine Failure in Flight (Restart)
1. **Throttle (Affected Engine)** — IDLE
2. **Airspeed** — 300 - 400 km/h (Optimum windmill range)
3. **Engine Start** — INITIATE (`RAlt+Home` / `RCtrl+Home`)
4. **Throttle** — ADVANCE slowly after RPM stabilizes > 30%

### Hydraulic Failure
1. **Monitor Pressures** — Check Hydro 1 / Hydro 2 gauges.
2. **Landing Gear** — EMERGENCY EXTEND (`LCtrl+G`) if main system fails.
3. **Flaps** — May be inoperative. Plan for high-speed, no-flap landing.
4. **Braking** — Be prepared for loss of wheel brakes (use Chute early).

### Electrical Failure (Generator Failure)
1. **Reduce Load** — Turn off non-essential avionics (Radar, EO, Lights).
2. **Battery Power** — Limited time (approx 20 mins).
3. **Land ASAP**.

### Spin Recovery
1. **Throttle** — IDLE
2. **Stick** — NEUTRAL
3. **Rudder** — FULL OPPOSITE to spin direction
4. **Recover** — Pull out gently once rotation stops.

### Ejection Sequence
1. **Canopy** — JETTISON (Automatic usually)
2. **Eject** — INITIATE (`LCtrl + E` x3)
