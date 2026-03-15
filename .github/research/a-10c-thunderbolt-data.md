# Research Dossier: A-10C / A-10C II Thunderbolt II (DCS World)

**Source Notes:**
- Primary data based on DCS World A-10C II Tank Killer Flight Manual (Eagle Dynamics).
- Real-world USAF A-10C Dash-1 used for comparison.
- **Discrepancy Note:** The DCS A-10C and A-10C II are high-fidelity modules with nearly full systems modeling (clickable cockpit). The "II" (Tank Killer) variant adds the HMCS (Helmet Mounted Cueing System), APKWS (Laser Guided Rockets), and GBU-54 (LJDAM). Flight performance is identical between C and C II.

## 1. Operating Limitations

| Parameter | Limit | DCS vs Real World Notes |
|---|---|---|
| **Max Takeoff Weight (MTOW)** | 51,000 lbs (approx) | Standard combat MTOW ~47,000-48,000 lbs. |
| **Max Landing Weight** | 46,000 lbs (Structural) | Recommended < 40,000 lbs for normal ops. |
| **G-Limits** | +7.33 G / -3.0 G (Clean)<br>+5.0 G (Rolling / Loaded) | EGI/CADC limits warnings based on stores configuration. |
| **AoA Limits** | 20-22 Units (Indicated) | Stall warning (chopper) starts ~20 units. Stall ~23 units. |
| **Crosswind Component** | 20 knots | Dry runway. 15 knots wet. |
| **Max Mach** | M 0.75 | Airframe drag usually prevents reaching this. |
| **APU Operation** | < 15,000 ft | For starting or emergency power. |

## 2. Performance & V-Speeds

| Regime | Speed (KIAS / Knots) | Configuration / Notes |
|---|---|---|
| **Rotation Speed (Vr)** | 135 - 150 KIAS | Weight dependent. |
| **Takeoff Speed** | 150 - 160 KIAS | Lift-off. |
| **Landing Approach** | 130 - 140 KIAS | On AoA Indexer (Green Circle). |
| **Corner Speed** | 280 - 320 KIAS | Best maneuvering/turn rate. |
| **Best Climb (Vy)** | 200 - 220 KIAS | Clean / Light stores. |
| **Stall Speed (Vs)** | ~110 KIAS | Dirty (Gear/Flaps Down), dependent on weight. |
| **Max Speed (Vne)** | 450 KIAS | Low altitude structural limit. |
| **Gear Extension (Vlo)** | 200 KIAS | Do not extend above this. |
| **Flaps Limit (Vfe)** | 200 KIAS | Maneuver (MVR) & Down (DN). |
| **Refueling Speed** | 200 - 220 KIAS | Typical tanker speed. |

## 3. Emergency Procedures (Boldface/Immediate Action)

### Engine Failure on Takeoff (Abort)
1. **Throttles** — IDLE
2. **Wheel Brakes** — MAX
3. **Speed Brakes** — OPEN
4. **Jettison** — IF REQUIRED (Master Arm ARM, Jettison Button)

### Engine Fire in Flight
1. **Throttles** — IDLE (Affected Engine)
2. **Fire Handle** — PULL (T-Handle on glare shield)
3. **Agent** — DISCHARGE (Toggle switch L/R)
4. **Land ASAP**

### Engine Failure in Flight (Restart)
1. **Throttles** — IDLE
2. **Crossfeed** — OPEN (if needed)
3. **APU** — START (if < 15,000 ft)
4. **Engine Operate** — MOTOR (if using APU assist) or IGN (if windmill > 30%)
5. **Throttle** — IDLE (to introduce fuel)

### Hydraulic Failure (Dual)
1. **Manual Reversion** — ENGAGE (Pitch/Roll switches on left console)
2. **Control Stick** — Fly carefully (limited authority)
3. **Land ASAP** — No flaps, emergency gear extension required.

### Electrical Failure (Double Gen)
1. **Emergency Flood** — AS REQUIRED
2. **Standby Attitude** — UNCAGE
3. **Get Visual** — EGI/HUD/CDU will fail.

### Spin Recovery
1. **Throttles** — IDLE
2. **Stick** — NEUTRAL / AFT Slightly
3. **Rudder** — FULL OPPOSITE to spin
4. **Recover** — Dive recovery once rotation stops.

### Ejection Sequence
1. **Eject** — PULL HANDLE (3 times or hold)
