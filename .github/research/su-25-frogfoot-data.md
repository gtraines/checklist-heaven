# Research Dossier: Su-25 "Frogfoot" (DCS Flaming Cliffs 3 vs Real World)

**Aircraft:** Su-25 "Frogfoot" (Grach)
**Module:** DCS: Flaming Cliffs 3 (Standard Su-25, non-T/SM)
**Primary Focus:** Comparison of Real World Manuals vs DCS Implementation

## 1. Operating Limitations

| Parameter | Real World (approx.) | DCS World (FC3) | Notes / Discrepancies |
| :--- | :--- | :--- | :--- |
| **Max Takeoff Weight (MTOW)** | Normal: 14,600 kg<br>Max: 17,600 kg<br>Overload: ~19,300 kg | ~17,600 kg is practically the limit for standard runways. Can take off heavier but performance is degraded significantly. | DCS allows overloading beyond safety limits; tire blowouts are a risk at high weights/speeds. |
| **Max Landing Weight** | 13,300 kg | Not strictly enforced by physics engine damage, but gear damage likely > 5-7 m/s sink rate if heavy. | Real manual restricts landing weight strictly to preserve airframe life. DCS is more forgiving unless hard landing. |
| **G-Limits** | +6.5 G (Clean)<br>+5.0 G (Loaded)<br>-2.0 G | Structural damage modeled. Wings can snap if G-limit exceeded significantly, especially with asymmetric load. | "Loaded" G-limit varies dynamically in DCS based on store weight. Watch the G-meter. |
| **AoA Limits** | Critical AoA: ~20°<br>Stall Warning: ~18° | Stall buffet starts ~16-18°. Departure/Spin entry at ~20-22° depending on load. | DCS PFM (Professional Flight Model) simulates stall buffet accurately. |
| **Crosswind Limit** | 12 m/s (Takeoff/Landing) | Manageable up to ~15 m/s with proper technique. | Real world limit is conservative. DCS allows pushing limits. |
| **Max Mach** | M 0.82 | M 0.82 | Airframe vibration/buffet modeled near Mach limit. |

## 2. Performance & V-Speeds

| Parameter | Real World (Standard) | DCS World (Observed) | Notes |
| :--- | :--- | :--- | :--- |
| **Rotation Speed (Vr)** | Clean: 240 km/h<br>Loaded: 280-300+ km/h | Clean: ~250 km/h<br>Max Weight: ~320 km/h | Depends heavily on weight. In DCS, rotate gently to avoid tail strike. |
| **Takeoff Speed (Unstick)** | Clean: 260 km/h<br>Loaded: 300+ km/h | Clean: ~270 km/h<br>Max Weight: ~340 km/h | |
| **Approach Speed** | 260-270 km/h (plus corrections) | 260-280 km/h | Keep AoA around 10-12 degrees on approach. |
| **Corner Speed** | ~450-550 km/h | ~450-500 km/h | Best instantaneous turn rate. |
| **Best Climb Speed (Vy)** | ~550-600 km/h | ~600 km/h | Maintain for best energy rate. |
| **Stall Speed (Vs)** | ~190-200 km/h (Landing Config) | ~180-200 km/h | Buffet precedes stall. |
| **Max Speed (Vne)** | 1000 km/h (Sea Level) | ~950-1000 km/h | Risk of structural failure or control reversal/lockup at Vne. |
| **Gear Limit (Vlo)** | 400 km/h | 400 km/h | Gear damage likely if extended above limit. |
| **Flaps Limit (Vfe)** | Maneuver (10°): 500 km/h<br>Landing (25°): 400 km/h | Maneuver: 500 km/h<br>Landing: 400 km/h | Flaps may jam or suffer structural failure if limits exceeded. |
| **Chute Limit** | 300 km/h (Deployment) | 300 km/h | Chute can rip off if deployed too fast. |

## 3. Emergency Procedures (Boldface/Immediate Action)

*Note: DCS Flaming Cliffs 3 does not support clickable cockpits for all switches. Procedures are "simulated" via keybinds or simplified logic.*

### Engine Failure on Takeoff
1. **Below V1 (Decision Speed):** ABORT. Throttle IDLE. Deploy Chute. Brake MAX.
2. **Above V1/Airborne:**
   - Maintain Directional Control (Rudder).
   - Jettison External Stores (Emergency Jettison - `Ctrl + W`).
   - Climbing turn towards *operating* engine (gentle).
   - Maintain Airspeed > 300 km/h.

### Engine Fire in Flight
1. **Throttle (Affected Engine):** IDLE.
2. **Engine Stopcock (Affected):** OFF (`RAlt + End` or `RCtrl + End`).
3. **Fire Extinguisher:** DISCHARGE (Automatic in FC3 or specialized keybind if modeled, usually assumed automatic upon shutdown/fire detect in simplified modes, but verify binding). *Note: FC3 Su-25 often requires just shutting down the engine to "simulate" handling the fire, extinguishing isn't always a separate manual step.*

### Engine Failure in Flight (Restart)
1. **Altitude:** Below 6,000m (Preferred < 4,000m).
2. **Airspeed:** 400 - 600 km/h.
3. **Throttle:** IDLE.
4. **Engine Start:** INITIATE (`RAlt + Home` or `RCtrl + Home`).
   - *Note: In Real World, this involves APU start, ignition switches, etc. In DCS FC3, it is a single macro command.*

### Hydraulic Failure
1. **Indication:** Stiff controls, loss of flaps/gear actuation, "Hydraulic" warning light.
2. **Action:**
   - Reduce Airspeed.
   - Avoid sharp maneuvers.
   - Use Emergency Gear Extension if main system failed (`Alt + G` or similar if modeled, otherwise rely on backup system automatic engagement).
   - Expect longer landing roll (no wheel brakes if main system fail? - Check pneumatic backup in DCS).

### Electrical Failure
1. **Generators:** OFF (Simulated).
2. **Non-essential systems:** OFF.
3. **Land ASAP:** Battery life is limited (~20 mins).
   - *DCS Note: Electrical failures often result in loss of SAS (Stability Augmentation), making the aircraft unstable.*

### Spin Recovery
1. **Throttle:** IDLE.
2. **Controls:** NEUTRAL.
3. **Rudder:** FULL OPPOSITE to spin direction.
4. **Stick:** Ease FORWARD to break stall.
5. **Recover:** Smoothly pull out of dive after rotation stops.

### Ejection Sequence
1. **Pull Handle:** `Ctrl + E` (3 times).

## 4. Sources & Notes
- **DCS Manual:** *DCS Flaming Cliffs 3 Flight Manual (2020)*
- **Real World Reference:** *Su-25 Flight Manual (Aeroflot/Military Archive)*
- **Discrepancy Note:** The DCS Su-25 (standard) has a Professional Flight Model (PFM) which is very accurate regarding physics, but the Systems modeling (SSM) is simplified (non-clickable).
- **Navigation:** Real Su-25 uses RSBN/PRMG navigation. In DCS FC3, this is simplified compared to the Su-25T, but still requires understanding of the HSI and mode selection (Route/Return/Landing).
- **Weapons:** Real world employment requires strict parameter adherence. DCS allows slightly more loose parameters, but the laser rangefinder (`Shift + O`) usage is critical for accuracy.
