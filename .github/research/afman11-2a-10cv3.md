# A-10C / A-10C II Procedure Research
**Source:** AFMAN 11-2A-10C Vol 3 & T.O. 1A-10C-1 (Combined Research)

## 1. Normal Procedures

### Interior Inspection (Critical Missing Items in DCS)
While DCS allows for a rapid start, the full AFMAN procedure includes checks often overlooked:
*   **Oxygen System Check:** 
    *   Supply Lever: **ON**
    *   Diluter Lever: **100%**
    *   Emergency Toggle: **NORMAL**
    *   *Note: Crucial for high-altitude operations; DCS default is often just 'On'.*
*   **Stability Augmentation System (SAS):**
    *   Check all 4 channels (Pitch/Yaw L/R) engage correctly.
    *   Test the **SAS DISENGAGE** button on the stick (ensure they pop off).
    *   Re-engage all channels.
*   **Anti-Skid System:** 
    *   Switch: **ON** (Often forgotten in sim; critical for maximum performance braking).
*   **Emergency Flight Control System (MRFCS):**
    *   Emergency Flight Control Switch: **MAN REVERSION** (Check controls)
    *   Switch: **NORMAL** (Check controls)
*   **Signal Lights Lamp Test:**
    *   Test checking AOA, Refuel, and Caution panel lights.

### Challenge/Response Checks
**Before Taxi:**
*   **Crew Chief:** "Chocks removed, marshaler in sight."
*   **Pilot:** "Brakes checked, steering engaged."
*   **Instruments:** "Checked" (Altimeter, HSI, ADI).

**Before Takeoff:**
*   **Canopy:** "CLOSED and LOCKED, Light OUT"
*   **Seat:** "ARMED" (Ground safety pin removed)
*   **Flaps:** "SET" (7° for Takeoff)
*   **Speedbrakes:** "CLOSED"
*   **Trim:** "SET" (Takeoff position: ~0 Pitch, 0 Roll, 0 Yaw)
*   **IFF/TACAN:** "SET" (As required for mission)

### Lineup Check (Runway Items)
Performed when taking the active runway.
*   **Runway Heading:** VERIFY (Compare HSI to Runway heading)
*   **Pitot Heat:** ON
*   **Exterior Lights:** ON (Landing Lights / Anti-Collision as required)
*   **Transponder:** ALT (Mode 3/C active)
*   **Ignition:** ON (If conditions require, otherwise AUTO)

---

## 2. A-10C II Specifics

### HMD (Scorpion HMCS) Alignment
1.  **Power Up:**
    *   HMCS Power Switch (Bat/AC panel): **ON**
2.  **Alignment Procedure:**
    *   MFCD: Select **HMCS** Page.
    *   Select **ALIGN**.
    *   **Coarse Align:** Look at the HUD boresight cross. Press and hold designated HOTAS button (usually TMS Up or specific align button depending on HOTAS profile) until "ALIGN OK".
    *   **Fine Align (Az/El/Roll):** Adjust crosshair overlay to perfectly match HUD center using cursor slews.
3.  **Operation:**
    *   Ensure HMCS symbology is visible and conformal with HUD.

### APKWS (Laser Guided Rockets)
*   **Loading:** Must be loaded in DSMS inventory as **APKWS** (e.g., M151/M282 heads with WGU-59/B guidance).
*   **Laser Code:**
    *   Default is **1688**.
    *   Must match the TGP laser code (LSR) if self-lasing.
    *   Set via **INV** (Inventory) page in DSMS -> Select Station -> **LASER** -> Edit Code.
*   **Employment Differences:**
    *   **Profile:** Set to **CCRP** or **CCIP**.
    *   **Laser:** Must actuate laser (**LATCH** or **PULSE**) before impact. 
    *   **Trajectory:** Ideally lofted slightly or fired within kinetic envelope (range < 5nm typically).
    *   **Q-Beam:** Unlike dumb rockets, verify **LASER** logic is set (Combat Mix recommended).

---

## 3. Emergency Procedures (Boldface)

*Ref: T.O. 1A-10C-1 Critical Action Procedures*

### ABORT (Engine Failure/Fire on Takeoff)
**1. THROTTLES - IDLE**
**2. WHEEL BRAKES - MAX**
**3. SPEEDBRAKES - OPEN**
*(If Fire Exists:)*
**4. FIRE HANDLE - PULL**
**5. EXTINGUISHER SWITCH - FWD / AFT (As Required)**

### ENGINE FIRE (DURING FLIGHT)
**1. THROTTLE (Affected Engine) - IDLE**
**2. FIRE HANDLE (Affected Engine) - PULL**
**3. EXTINGUISHER SWITCH - FWD / AFT (As Required)**

### DOUBLE ENGINE FAILURE (POST-STALL / STAGNATION)
**1. THROTTLES - IDLE**
**2. APU SWITCH - START**
**3. ENGINE OPERATE SWITCHES - IGN**
*(Then proceed to Crossbleed or APU restart logic)*

### MANUAL REVERSION (Loss of Hydraulics)
*Not Boldface, but Critical Memory Item:*
**1. FLIGHT CONTROLS - MAN REVERSION**
**2. LANDING GEAR HANDLE - UP** (If takeoff) or **AS REQUIRED**

### EJECTION
**1. EJECTION HANDLE - PULL**

---

## 4. Operating Limitations

### Wind Limits
*   **Max Crosswind (Dry):** 30 Knots
*   **Max Crosswind (Wet):** 20 Knots
*   **Max Tailwind:** 10 Knots
*   **Max Headwind (Canopy Open):** 45 Knots

### Airspeed Limits (Vne / Vlimit)
*   **Landing Gear Operation/Extended:** 200 KIAS
*   **Flaps (MVR / 7°):** 200 KIAS
*   **Flaps (DN / 20°):** 200 KIAS
*   **Speedbrakes:** No Limit (Operational up to Vne)
*   **Canopy Opening (Ground):** 45 Knots Taxi

### Engine Limits (TF34-GE-100A)
*   **Max ITT (Start):** 860°C
*   **Max ITT (Normal / TO):** 900°C (Transient) / 810°C (Max Continuous)
*   **Core RPM (N2):** Max 99% (Fan Speed N1 is primary thrust indicator)
*   **Fan Speed (N1):** Max 98%
*   **Oil Pressure:** 55-95 PSI (Normal Range)
