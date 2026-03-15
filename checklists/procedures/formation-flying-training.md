# Formation Flying Training Course

> **Scope:** UH-1H, Mi-24P, OH-58D, Su-25/T, A-10A/C/II | **Target:** DCS World
>
> [← Back to Index](../index.md)

---

## 1. Executive Summary

Formation flying is the cornerstone of military aviation, enabling mutual support, massed firepower, and efficient airspace management. In DCS World, it presents unique challenges due to network latency ("netcode"), AI behavior quirks, and the lack of physical sensory feedback (seat-of-the-pants feel).

This course synthesizes real-world doctrine (US Air Force, US Army, and Russian Aviation) adapted for the simulation environment. It breaks down the discipline into universal concepts applicable to all airframes, followed by deep dives into rotary-wing and fixed-wing specifics. The goal is to move pilots from "not crashing" to "tactical proficiency."

---

## 2. Universal Standards (Fixed & Rotary)

### 2.1 Terminology & Organization

*   **Flight Lead (Lead):** The commander of the formation. Responsible for navigation, communication, and the safety of the flight. Lead *navigates* and *clears*.
*   **Wingman:** Pilots flying off Lead's wing. Responsible for station keeping and mutual support. Wingmen *aviate* (don't hit Lead), *navigate* (know where you are), and *communicate* (backup Lead).
*   **Element (Section):** A 2-ship formation (Lead + Dash-2). The fundamental fighting unit.
*   **Flight (Division):** A 4-ship formation, composed of two elements (Lead element: #1 & #2; Second element: #3 & #4).
*   **Dash-X:** Refers to the position in the flight (e.g., "Dash-2" is the first wingman).

### 2.2 Core Concepts: The Contract

The formation "Contract" is the unspoken (or spoken) agreement that keeps everyone alive.

*   **Lead's Responsibilities:**
    *   Be stable and predictable. No sudden moves.
    *   Signal all turns, speed changes, and configuration changes (radio or visual).
    *   Navigate the mission profile.
    *   Consider the wingman's energy state (don't drag them through the floor).
*   **Wingman's Responsibilities:**
    *   **NEVER** hit Lead.
    *   Keep Lead in sight (Visual).
    *   Maintain position (Station Keeping).
    *   Be ready to engage/support on command.

### 2.3 Communications (Brevity)

*   **"Visual"**: Wingman sees Lead/Friendly.
*   **"Blind"**: Wingman has lost sight of Lead/Friendly (DANGEROUS).
*   **"Tally"**: Sighting of an enemy target.
*   **"No Joy"**: No sighting of enemy target.
*   **"Fence In/Out"**: Command to set cockpit switches for combat/admin phases (Master Arm, Lights, RWR).
*   **"Check [Left/Right]"**: Turn specified degrees (usually 30°) to verify formation integrity or spacing.
*   **"Reform"**: Return to close/parade formation.
*   **"Padlocked"**: Focused exclusively on a target/threat (cannot maintain situational awareness).

---

## 3. Rotary-Wing Deep Dive

### 3.1 Unique Challenges
*   **Rotor Wash:** Flying too close or below Lead can result in loss of lift or severe turbulence. Stack *step-up* is preferred for safety.
*   **Torque/Yaw:** Power changes result in yaw; Lead must be smooth to prevent the formation from "accordioning" (compressing/stretching).
*   **Hover:** Hover formation requires referencing ground objects *and* Lead. Vertigo is a high risk in dust/brownout.

### 3.2 Standard Formations
*   **Trail:** Simplest. 3-5 rotor disks separation. Good for transiting restricted terrain. Vulnerable to ambush from rear.
*   **Staggered Trail (Left/Right):** Wingman is 30-45 degrees off Lead's tail. Allows Wingman to cover Lead's blind spot. Standard for transit.
*   **Heavy Left/Right (Echelon):** All aircraft on one side. Used for gun runs or landing breaks.
*   **Combat Cruise:** Fluid. Wingman maintains a "cone" behind Lead (e.g., 5-7 o'clock), maneuvering freely to scan terrain. Maximizes mutual support.

### 3.3 Aircraft Specifics

#### **UH-1H Huey**
*   **Visual References:**
    *   *Staggered:* Align the simulated pilot's door frame with Lead's skid or engine exhaust.
    *   *Distance:* Read the tail number clearly but not the inspection stencils.
*   **Handling:** Very sensitive to collective changes. Lead must announce "Coming up on power" or "Dropping collective."

#### **Mi-24P Hind**
*   **Visual References:**
    *   Large size makes it easy to see, but high inertia makes it hard to stop.
    *   *Station:* Align the weapon pylons or the large exhaust suppressors.
*   **Doctrine:** Russian doctrine often emphasizes tighter, more rigid formations ("Parade") compared to Western "Fluid" tactics.
*   **Handling:** The Hind is fast but heavy. Wingmen must anticipate turns early. Overshooting is common; use the airbrake or sideslip (pedal turn) carefully to bleed speed.

#### **OH-58D Kiowa Warrior**
*   **Role:** Scout/Recon. Formation is often extremely loose ("Scout Team").
*   **MMS Usage:** Lead may mask (hide) while Wingman unmasks to scan with the Mast Mounted Sight (MMS), or vice versa.
*   **Tactics:** "Bounding Overwatch." One moves while the other covers. Not a traditional "parade" formation aircraft.

---

## 4. Fixed-Wing Deep Dive (CAS Jets)

### 4.1 Standard Formations
*   **Fingertip (Parade):** Tight. Wingman's wingtip aligned with Lead's fuselage reference. Used for weather penetration, airfield arrival/departure, and show. *Not tactical.*
*   **Route:** Looser fingertip (2-4 ship widths). Allows Wingman to check instruments/charts.
*   **Combat Spread (Line Abreast):** 1-2 miles apart, abreast. Maximizes visual coverage (Lead checks Wingman's 6, Wingman checks Lead's 6). Hardest to fly but most lethal.
*   **Trail (Radar/Visual):** Used for bad weather or night. Wingman follows Lead using radar or strictly visual cues.

### 4.2 Aircraft Specifics

#### **A-10A / A-10C / A-10C II**
*   **Reference (AFI 11-2A-10):**
    *   *Fingertip:* Place the front of Lead's wingtip on the star (insignia) of the fuselage. Align Lead's trailing edge of the wing with the engine exhaust.
*   **Speed:**
    *   Cruise/Join: 220-250 kts.
    *   Refueling: AAR door markings (yellow/white bands) on the nose are critical cues for the tanker (KC-135/KC-10).
*   **Tactics:** "Wagon Wheel" or "Shooter-Cover" during CAS. While Lead attacks, Wingman orbits high/dry to spot threats.

#### **Su-25 / Su-25T**
*   **Visual References:**
    *   *Close:* Align the wing fence (metal ridge on the wing) with the Lead's outer pylon.
    *   *Route:* Keep Lead's canopy fully visible above the wing line.
*   **Handling:** The Su-25T is heavy (especially with Vikhr missiles). Roll rate is sluggish. Lead must roll *slowly* into turns.
*   **Airbrakes:** The wingtip airbrakes are very effective. Use "boards out" momentarily to fix overshoots rather than cutting throttle to idle (spool-up time is slow).

---

## 5. DCS World Training Drills

### Phase 1: Basic (The "String")
*   **Goal:** Safety and stability.
*   **Setup:** 2-ship (Player + AI or Player + Player). 5000ft AGL, Clear weather.
*   **Drill:**
    1.  Join up in **Route** formation (Left/Right).
    2.  Lead flies straight and level at constant speed.
    3.  Lead initiates gentle turns (15-20° bank). Wingman maintains the "plane" of the turn (stacking level with Lead).
    4.  **Cross-under:** Wingman moves from Right wing to Left wing smoothly, passing *below* Lead's wake.

### Phase 2: Intermediate (The "Bellows")
*   **Goal:** Energy management.
*   **Setup:** 2-ship.
*   **Drill:**
    1.  **Accordions:** Lead accelerates/decelerates by 50 knots. Wingman must match without overshooting/lagging.
    2.  **Turning Rendezvous:** Lead orbits at 30° bank. Wingman cuts inside the circle ("lead pursuit") to join, then slides into position.
    3.  **Climbing/Descending Turns:** Lead performs a helix climb/descent. Wingman must manage power heavily to stay in position.

### Phase 3: Advanced (Tactical)
*   **Goal:** Combat effectiveness.
*   **Setup:** Low level (NOE - Nap of Earth) or Combat Spread.
*   **Drill:**
    1.  **Tactical Turns:** 90° turns in Combat Spread.
        *   *Check Turn:* Both turn 90° simultaneously (requires Wingman to cross over).
        *   *Tac Turn:* Wingman turns *first* (if turning into Wingman) or Lead turns first (if turning away), maintaining the line-abreast geometry.
    2.  **Break & Rejoin:** Overhead break procedure for landing. 3-5 second interval break. Rejoin on downwind.
    3.  **Low-Level Route:** Navigate a valley in Trail or Combat Cruise. Lead focuses on navigation; Wingman focuses on terrain clearance and covering Lead.

---

## 6. DCS Implementation Notes

### AI Wingmen
*   **Collision:** DCS AI flies "on rails" in formation. They will not evade you. **YOU** must evade *them*.
*   **Tasks:** Use the radio menu (`\` key) `Flight -> Go To -> Formation` to reset them if they get stuck.
*   **Behavior:** AI struggles with "Combat Spread" in tight terrain; they often revert to "Trail."

### Multiplayer / Netcode
*   **Lag Buffer:** In high-latency servers, fly slightly looser.
*   **"Warping":** If Lead warps/teleports, trust their *average* vector, not their instantaneous position.
*   **Prediction:** Do not react to small jitters. Fly the trend.

---

## 7. References
*   **AFI 11-2A-10C Vol 3:** A-10C Operations Procedures.
*   **CNATRA P-800 series:** US Navy Flight Training Instructions (Formation).
*   **TC 3-04.4:** Fundamentals of Flight (Army Rotary Wing).
*   **DCS World Manuals:** Su-25T Flight Manual, A-10C II Tank Killer Manual.

---

*Based on Eagle Dynamics DCS World documentation. For use as a simulation aid only.*
