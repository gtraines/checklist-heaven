# Research Dossier: Su-25T Basic Qualification Training (BQT)

> **Aircraft:** Sukhoi Su-25T "Frogfoot-B"
> **Course Level:** Basic Qualification (Level 100)
> **Reference:** NATOPS / Dash-1 Standardized Format

## Overview
This dossier outlines the syllabus for the Basic Qualification Training (BQT) course for the Su-25T. It is designed to take a student from zero experience to a safe, competent operator capable of day VFR flight, recovery, and basic emergencies.

---

## Module 1: Aircraft Systems & Aerodynamics

### 1.1 Learning Objectives
*   Student can explain the aerodynamic differences between the Su-25A and Su-25T (specifically weight and drag).
*   Student understands the R-195 engine operation limitations, specifically spool-up lag.
*   Student can demonstrate the use of the ACS (Automatic Control System) modes.

### 1.2 Key Data
*   **Empty Weight:** ~10,740 kg (significantly heavier than Su-25A).
*   **Engine:** 2x R-195 Turbojets (4,500 kgf thrust each).
*   **Spool-up Time:** Idle to Max Power takes **9-12 seconds**. This is a critical flight safety factor.
*   **ACS Modes:**
    *   **Route Following:** Navigation via waypoints.
    *   **Combat Steering:** Stabilizes aim for gun/rocket runs.
    *   **Landing:** Koppled approach (ILS/PRMG).
    *   **Emergency Level:** (`LAlt + 3`) Returns aircraft to straight and level.

### 1.3 Instructor Notes
*   **The "Hump" Penalty:** Emphasize that the dorsal avionics hump and Shkval nose sensor add parasitic drag. The Su-25T bleeds energy much faster in turns than the base Su-25. It is **not** a dogfighter.
*   **Engine Lag:** Demonstrate this on the ramp. Slam throttle to max and count out loud until RPM stabilizes. Students often crash on approach because they are behind the power curve.

### 1.4 Realism Notes
*   **Hydraulics:** The DCS model accurately simulates hydraulic failure. Loss of the primary booster system makes the stick extremely heavy, requiring both hands (in reality) or significant trim input (in sim).
*   **Diff-Braking:** The Su-25T has no differential braking in the air, but relies on rudders. On the ground, differential braking is essential as the rudder is ineffective at taxi speeds without NWS.

---

## Module 2: Ground Operations

### 2.1 Learning Objectives
*   Perform Pre-Start cockpit scan (Electrical, EKRAN check).
*   Execute Engine Start sequence without exceeding EGT limits.
*   Perform safe taxi to the active runway using NWS.

### 2.2 Key Data
*   **Electrical Power:** `RShift + L` (AC/DC Generators are automatic after start).
*   **Start Sequence:** Left Engine (`RAlt + Home`), then Right Engine (`RCtrl + Home`).
*   **Idle RPM:** ~36-40% N1 / ~60-65% N2.
*   **Taxi Speed:** Max 20-30 km/h on straights, < 10 km/h in turns.

### 2.3 Instructor Notes
*   **EKRAN is Life:** Train students to look at the EKRAN (warning panel) immediately upon power up. It talks to you.
*   **NWS Madness:** The Su-25T nose wheel steering is notoriously sensitive. Instruct students to tap the rudder keys/pedals rather than hold them, or use low curves.
*   **Warm-up:** In DCS, immediate takeoff is possible, but teach the discipline of waiting for oil temps/hydraulics (watch the warning lights extinguish).

### 2.4 Realism Notes
*   **Inertial Navigation:** In the real jet, the I-251 "Shkval" system requires alignment time (3-15 mins). DCS simplifies this, but the "Wait for Shkval" (TV warm up) is a remnant of this requirement.
*   **Canopy:** The canopy is pneumatically sealed. Ensure it is closed and locked (`LCtrl + C`) before engine start to prevent fumes in the cockpit (roleplay).

---

## Module 3: Takeoff & Departure

### 3.1 Learning Objectives
*   Calculate and execute rotation at correct Vr.
*   Maintain runway centerline during takeoff roll.
*   Perform "Clean Up" (Gear/Flaps) on schedule.

### 3.2 Key Data
*   **Flaps:** Takeoff Position (`LShift + F`).
*   **Trim:** Pitch trim **Neutral to Slight Nose Up** (green lights in center).
*   **Vr (Rotation):** 
    *   Clean/Light: 210 km/h
    *   Combat Load (Vikhrs/Fuel): **240-250 km/h**
*   **Vlof (Liftoff):** ~260-270 km/h.
*   **Gear Retraction:** Positive Rate, < 400 km/h.
*   **Flap Retraction:** > 300 km/h and > 150m AGL.

### 3.3 Instructor Notes
*   **The "Frog" Leap:** The Su-25T tends to "leap" off the runway if trimmed too far back. Instruct smooth rotation to 10-12 degrees pitch.
*   **Tire Failures:** Taking off over-weight (>19,500kg) or rotating too late (>350 km/h on ground) will blow tires.

### 3.4 Realism Notes
*   **Asymmetric Load:** The Su-25T is very sensitive to asymmetric stores. If taking off with a mismatch (e.g., after rearming only one side), the roll tendency at liftoff can be lethal. DCS models this correctly.

---

## Module 4: Basic Flight Maneuvers (BFM)

### 4.1 Learning Objectives
*   Demonstrate coordinated turns (bank angle 30/45/60).
*   Recognize and recover from approach-to-stall buffet.
*   Demonstrate proper trim technique during speed changes.

### 4.2 Key Data
*   **Cruise Speed:** 500-600 km/h.
*   **Corner Velocity:** 450-550 km/h.
*   **Stall Speed:** ~180-200 km/h (depending on weight).
*   **AoA Limit:** ~20 units (Critical).

### 4.3 Instructor Notes
*   **Trim, Trim, Trim:** The Su-25T Flight Control System is purely hydro-mechanical (no Fly-By-Wire). Every speed change requires a trim change. Students who "fight the stick" will fatigue and fly imprecise profiles.
*   **The Buffet:** The airframe shudders significantly before the stall. This is the primary tactile warning.
*   **Rudder Usage:** Unlike the A-10, the Su-25T requires coordinated rudder in turns to keep the ball centered.

### 4.4 Realism Notes
*   **Spin Characteristics:** The Su-25T has a nasty flat spin mode if forced into a high-AoA yaw state. Recovery is often impossible below 2,000m. DCS models the specific CG shift that causes this.

---

## Module 5: Approach & Landing

### 5.1 Learning Objectives
*   Fly a standard visual traffic pattern (rectangular).
*   Stabilize final approach speed and AoA.
*   Execute safe touchdown and aerobraking/chute deployment.

### 5.2 Key Data
*   **Pattern Speed (Downwind):** 400 km/h.
*   **Gear/Flaps Extension:** < 400 km/h (Flaps Landing).
*   **Final Approach Speed:**
    *   Heavy: 290-300 km/h
    *   Normal: 270-280 km/h
    *   Light: 260 km/h
*   **Touchdown:** ~240 km/h.
*   **Max Landing Weight:** 13,300 kg (Verify fuel dumping/store jettison if emergency).
*   **Chute:** Deploy immediately on touchdown (`P` key).

### 5.3 Instructor Notes
*   **Power Management:** Due to engine lag, power corrections on final must be anticipatory. If you get low and slow, you are already crashing. Add power *before* the speed bleeds off.
*   **The Flare:** Do not over-flare. The Su-25T sits low. A slight check of the descent rate is all that is needed. Flaring too high causes a hard slam (stall) onto the gear.
*   **Braking:** Do **not** slam wheel brakes immediately. Deploy chute, let speed drop below 200 km/h, then apply brakes. Blowing tires closes the runway.

### 5.4 Realism Notes
*   **Drag Chute Logic:** In the real aircraft, the chute is often deployed *before* nosewheel touchdown (aerobraking phase) to stabilize the aircraft. In DCS, this works well.
*   **Gear Strength:** The DCS Su-25T gear is surprisingly fragile regarding side-loads. Crabbed landings (landing while drifting sideways) will collapse the gear instantly. De-crab is mandatory.
