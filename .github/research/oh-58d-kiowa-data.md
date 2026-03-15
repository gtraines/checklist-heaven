# OH-58D Kiowa Warrior Research Dossier

**Source:** TM 55-1520-248-10 (Operator's Manual), DCS World (Polychop Simulations)
**Aircraft:** OH-58D Kiowa Warrior

## 1. Operating Limitations

| Limit | Value | Notes |
| :--- | :--- | :--- |
| **Max Takeoff Weight (MTOW)** | 5,500 lbs (2,495 kg) | With STC or specific configurations; standard max gross often cited as 5,200 lbs for earlier models, but 5,500 lbs for KW. |
| **Max Landing Weight** | 5,500 lbs | Same as MTOW. |
| **G-Limits** | +2.5 G to -0.5 G | At Max Gross Weight. Avoid negative G maneuvers (mast bumping risk). |
| **Rotor RPM Limits (Nr)** | Power On: 98% - 100%<br>Power Off: 90% - 107% | Transient limits exist. Continuous operation range. |
| **Torque Limits (Q)** | Continuous: 100%<br>Transient (10 sec): 110% | Exceeding 100% requires inspection/maintenance logging in real life. |
| **TOT Limits (Turbine Outlet Temp)** | Continuous: 737°C<br>Start (10 sec): 843°C | Pay attention to start limits in DCS. |
| **Slope Landing Limits** | 10° (Side/Nose Up)<br>5° (Nose Down) | DCS terrain interaction may vary slightly. |
| **Crosswind Component** | 35 knots (Sideward/Rearward) | Loss of Tail Rotor Effectiveness (LTE) risk increases significantly with high crosswinds/tailwinds. |

## 2. Performance & V-Speeds

| V-Speed | Value (KIAS) | Notes |
| :--- | :--- | :--- |
| **Hover Taxi Speed** | < 20 knots | Standard ground taxi (hover) speed. |
| **Takeoff Profile** | 45-60 knots | Climb out speed. |
| **Max Rate of Climb (Vy)** | 55-60 knots | Variable with weight/altitude. |
| **Max Range Speed** | ~90-100 knots | Depends on drag (MMS, weapons). |
| **Max Speed (Vne)** | 110-120 knots | Reduced by gross weight, altitude, and external stores (doors off: 110 KIAS). |
| **Autorotation Speed** | 60 knots (Min Rate of Descent)<br>80 knots (Max Glide Distance) | Recommended range 60-80 KIAS. |
| **Sideward/Rearward Flight** | 35 knots | Max control limit. |
| **Landing Approach** | 60 knots (Initial) | Decelerating to hover. |
| **Gear/Flap Limits** | N/A | Fixed skids. |

## 3. Emergency Procedures (Boldface/Immediate Action)

### Engine Failure - In Flight
1. **COLLECTIVE** - ADJUST (Maintain Rotor RPM within limits).
2. **PEDALS** - ADJUST (Trim aircraft).
3. **CYCLIC** - ADJUST (Establish autorotational airspeed, approx 60-80 KIAS).
4. **LANDING** - ACCOMPLISH (Select spot, flare, cushion).

### Engine Fire - In Flight
1. **LAND IMMEDIATELY**.
2. **EMERGENCY SHUTDOWN** - ACCOMPLISH (Once on ground).

### Engine Fire - On Ground
1. **EMERGENCY SHUTDOWN** - ACCOMPLISH.

### Emergency Shutdown
1. **THROTTLE** - OFF.
2. **FUEL BOOST** - OFF.
3. **BATTERY** - OFF.
4. **ROTOR BRAKE** - APPLY (As required).

### FADEC Failure (Major) / Engine Overspeed/Underspeed
1. **COLLECTIVE** - ADJUST (If overspeed, increase; if underspeed, decrease).
2. **THROTTLE** - ADJUST (Match Ng/TGT to manual limits if FADEC switches to manual).
3. **FADEC MODE SWITCH** - CHECK (Verify Manual/Auto).
4. **LAND AS SOON AS PRACTICABLE**.

### Hydraulic System Failure
1. **AIRSPEED** - ADJUST (To comfortable control speed, typically 60-80 KIAS).
2. **HYDRAULIC SWITCH** - OFF (If uncommanded inputs/hardover felt).
3. **LAND AS SOON AS POSSIBLE** (Run-on landing recommended in shallow approach).

### Tail Rotor Failure (Complete Loss of Thrust) / Spin
1. **AUTOROTATION** - ENTER.
2. **THROTTLE** - IDLE (or OFF prior to touchdown).
3. **LANDING** - ACCOMPLISH (Run-on landing if possible, or full auto).

### Loss of Tail Rotor Effectiveness (LTE) - Uncommanded Right Yaw
1. **COLLECTIVE** - REDUCE (As required to stop yaw).
2. **CYCLIC** - FORWARD (To gain airspeed).
3. **PEDALS** - FULL LEFT (As required).
4. **AIRSPEED** - INCREASE (Above ETL).

### Electrical Failure (DC Generator)
1. **GEN RESET** - PRESS (Reset generator).
2. **GEN SWITCH** - ON.
3. **IF GENERATOR FAILS TO RESET**:
    *   **NON-ESSENTIAL BUS** - OFF.
    *   **LAND AS SOON AS PRACTICABLE**.

### Engine Restart - In Flight
1. **AIRSPEED** - 60 KIAS.
2. **COLLECTIVE** - ADJUST (Maintain Rotor RPM).
3. **THROTTLE** - IDLE (If N1 < 50%) or FLY (If N1 > 50%).
4. **START SWITCH** - PRESS (If N1 < 50%).
5. **LAND AS SOON AS POSSIBLE** (If restart fails).

### Ejection Sequence
*   **N/A** (Helicopter). Emergency Egress only.

### Transmission Oil Pressure Low / Temp High
1. **LAND AS SOON AS POSSIBLE**.
2. **EMERGENCY SHUTDOWN** - ACCOMPLISH (If noise/vibration occurs).

## Notes for Checklist Writer
*   **MMS (Mast Mounted Sight):** The specific mass and drag of the sight affects Vne and handling. Ensure pilots are aware of the top-heavy nature.
*   **Weapons:** The OH-58D carries Hellfires, Rockets, Stinger (ATAS), and .50 cal. Firing restrictions (sideslip) apply.
*   **DCS Specifics:** The Polychop module has specific FADEC behavior. The startup sequence is sensitive to throttle position (must be at Idle detent).
*   **Doors Off:** Vne is restricted to 110 KIAS usually.
*   **FADEC:** The FADEC in the OH-58D is a critical system. Failure modes are modeled in DCS and require manual throttle manipulation.
*   **LTE:** Loss of Tail Rotor Effectiveness is a significant threat in this airframe (high power, low speed, tailwind).
