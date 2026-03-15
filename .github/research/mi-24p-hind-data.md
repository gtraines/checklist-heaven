# Research Dossier: Mi-24P Hind (DCS World)

**Source Notes:**
- Primary data based on DCS World Mi-24P Hind module (Eagle Dynamics — full fidelity).
- Real-world Soviet/Russian Mi-24P manuals and translated documentation used for comparison.
- **Discrepancy Note:** The DCS Mi-24P is a high-fidelity module with clickable cockpit (two crew positions: Pilot and Weapons Operator). Some real-world limitations are approximated. The 'P' variant uses a fixed twin-barrel GSh-30K cannon (starboard fuselage mount) vs the flexibly-mounted Yak-B of the Mi-24V/D.

## 1. Operating Limitations

| Parameter | Limit | DCS vs Real World Notes |
|---|---|---|
| **Max Takeoff Weight (MTOW)** | 11,500 kg (25,353 lbs) | Normal max. Overload TO possible at 11,500 kg. |
| **Max Landing Weight** | 11,500 kg | Same as MTOW for normal ops. |
| **G-Limits** | +3.5 G / -0.5 G | Helicopter limits. Hard banking increases load factor rapidly. |
| **VNE (Never Exceed Speed)** | 300 km/h (162 kts) | Absolute limit. Retreating blade stall risk beyond this. |
| **Max Autorotation Entry** | 220 km/h | Recommend initiating autorotation below this speed. |
| **Max Sideward Flight** | 50 km/h | Lateral limit to avoid tail rotor issues. |
| **Max Backward Flight** | 40 km/h | Rearward speed limit. |
| **Rotor RPM (Normal)** | 95% | Operating range 92-98%. |
| **Crosswind Component** | 12 m/s (~23 kts) | Landing/Takeoff crosswind limit. |

## 2. Performance & V-Speeds

| Regime | Speed (km/h / kts) | Configuration / Notes |
|---|---|---|
| **VNE (Never Exceed)** | 300 km/h (162 kts) | Hard limit. Structural/aeroelastic risk. |
| **Cruise Speed** | 260 km/h (140 kts) | Normal cruise (loaded). |
| **Best Range** | 220 km/h (119 kts) | Fuel-optimal cruise. |
| **Best Endurance** | 120 km/h (65 kts) | Max loiter time. |
| **Autorotation Speed** | 170 km/h (92 kts) | Optimal autorotation glide. |
| **Hover (IGE)** | 0 km/h | In-ground-effect hover: up to ~4m altitude. |
| **Hover (OGE)** | 0 km/h | Out-of-ground-effect hover: requires more power. |
| **Max Climb Rate** | ~12 m/s | Clean, sea level. |
| **Sideward Flight** | < 50 km/h | Lateral maneuver limit. |
| **Backward Flight** | < 40 km/h | Rearward maneuver limit. |

## 3. Emergency Procedures (Boldface/Immediate Action)

### Engine Failure (Single Engine)
1. **Collective** — MAINTAIN or adjust for level flight
2. **Fuel Feed** — CROSS-FEED OPEN (if one engine out)
3. **Failed Engine** — IDLE, then OFF
4. **Airspeed** — maintain 160-180 km/h for best single-engine performance
5. **Land ASAP** at nearest suitable area

### Engine Failure (Dual / Total Power Loss)
1. **Collective** — LOWER IMMEDIATELY (auto-rotation)
2. **Airspeed** — establish 170 km/h
3. **Autorotation** — maintain RPM in green (92-98%)
4. **Flare** — at ~30-50m AGL, raise nose to reduce speed
5. **Collective** — PULL at 5-10m AGL to cushion landing
6. **Touchdown** — level skids, collective full up

### Tail Rotor Failure
1. **Airspeed** — INCREASE to 120+ km/h (improves directional stability)
2. **Land ASAP** — running landing preferred
3. **Collective** — control yaw with power changes
4. **Do NOT hover** — loss of yaw control likely

### Fire (Engine Compartment)
1. **Throttle (affected engine)** — IDLE then OFF
2. **Fire Extinguisher** — DISCHARGE (First bottle, then second if needed)
3. **Land ASAP**

### Hydraulic Failure
1. **Force Trim** — may assist control
2. **Reduce airspeed** — below 150 km/h
3. **Land ASAP** — controls become heavy

### Ejection / Crew Egress
1. The Mi-24P does not have ejection seats.
2. **Autorotate** to suitable area.
3. **Emergency exits** — kick out doors/windows before egress.
