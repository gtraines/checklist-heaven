# CCA vs. CAS Doctrine — DCS Helicopter Operations

> **Procedure:** Close Combat Attack (CCA) vs. Close Air Support (CAS)
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [CCA vs. CAS Distinction](#cca-vs-cas-distinction)
2. [The CCA 5-Line Format](#the-cca-5-line-format)
3. [The CAS 9-Line Format (Rotary Wing Applicability)](#the-cas-9-line-format-rotary-wing-applicability)
4. [Keyhole CAS for Helicopters](#keyhole-cas-for-helicopters)
5. [Helicopter Employment Modes](#helicopter-employment-modes)

---

## CCA vs. CAS Distinction

In DCS World helicopter operations, understanding the difference between Close Combat Attack (CCA) and Close Air Support (CAS) is critical for effective communication and employment. While often used interchangeably in casual play, they represent distinct doctrinal concepts (ref: FM 3-04.126).

### 1. Close Combat Attack (CCA)
**Definition:** A hasty or deliberate attack by Army aircraft providing air-to-ground fires for friendly units engaged in close combat.
*   **Key Characteristic:** The **pilot** is in control of the engagement, not a JTAC. The ground unit functions as an *observer*, providing target data, but the aviator makes the final decision on engagement based on their perspective.
*   **Communication:** Direct, informal, and dynamic.
*   **Format:** Typically uses the **5-Line** format ("CCA 5-Line").
*   **Usage in DCS:** Most common when working with fellow players in Combined Arms who are in tanks/vehicles but are not trained JTACs, or when self-generating targets in a dynamic environment.

### 2. Close Air Support (CAS)
**Definition:** Air action by fixed-wing or rotary-wing aircraft against hostile targets that are in close proximity to friendly forces, requiring **detailed integration** of each air mission with the fire and movement of those forces.
*   **Key Characteristic:** A qualified **JTAC/FAC(A)** controls the airstrike. The JTAC clears the aircraft "Hot".
*   **Communication:** Formal, structured, and procedural.
*   **Format:** Uses the **9-Line** format.
*   **Usage in DCS:** Used when working with a human JTAC, in structured milsim events, or when detailed deconfliction with artillery/other air assets is simulated.

### Check-In Process
*   **CCA Check-In:** Abbreviated. The pilot simply states presence and capability.
    *   *Pilot:* "Enfield 1-1, Uzi 9-1, 5km South, ready for tasking."
    *   *Observer:* "Uzi 9-1, fire mission..." (Proceeds to 5-line).
*   **CAS Check-In:** Detailed. Follows the standard **CAS Check-In Brief** (MNPOPCA).
    *   **M**ission Number
    *   **N**umber and Type of Aircraft
    *   **P**osition and Altitude
    *   **O**rdnance
    *   **P**laytime (Time on Station)
    *   **C**apabilities (Sensors/Laser code)
    *   **A**bort Code

### Summary of Differences

| Feature | CCA | CAS |
| :--- | :--- | :--- |
| **Control** | **Pilot** determines engagement | **JTAC** grants clearance |
| **Clearance** | "At my command" (Pilot) | "Cleared Hot" (JTAC) |
| **Format** | 5-Line (Hasty) | 9-Line (Standard) |
| **Focus** | Dynamic fire and maneuver | Integrated fires |
| **DCS Use** | Hasty support, CA players | Structured support, Scripted JTACs |

---

## The CCA 5-Line Format

The CCA 5-Line is a condensed "friendly-centric" format designed for speed. It orients the pilot from the **observer's** position or a known friendly position.

### Format Breakdown

| Line | Item | Description |
| :--- | :--- | :--- |
| **1** | **Observer / Warning Order** | Who is calling and what kind of mission (e.g., "Fire Mission"). |
| **2** | **Friendly Location / Mark** | Where the friendlies are. Can be a grid, a landmark, or "My Position" (if visual). |
| **3** | **Target Location** | Relative to the friendly position (Direction & Distance) or a Grid. |
| **4** | **Target Description / Mark** | What the target is and how it's marked (Smoke, Laser, IR, Tracer). |
| **5** | **Remarks / Restrictions** | Ammo selection, "At my command", Danger Close, Egress direction. |

### DCS Example Transmission

**Scenario:** A ground player (Humvee) requests support from an AH-64D against a BMP-2.

**Ground (Observer):** "Enfield 1-1, this is Uzi 9-1, Fire Mission, over."
**Air (Pilot):** "Uzi 9-1, Enfield 1-1, send Fire Mission."

**Ground (Observer):**
*   **Line 1:** "Uzi 9-1."
*   **Line 2:** "My position, marked by IR strobe."
*   **Line 3:** "Direction 3-3-0, Distance 800 meters."
*   **Line 4:** "BMP-2 in the open, marked by tracers."
*   **Line 5:** "Use cannon, danger close, at my command."

**Air (Pilot):** "Tally tracers, tally BMP. In from the south, cannon."

---

## The CAS 9-Line Format (Rotary Wing Applicability)

While primarily associated with fixed-wing, helicopters use the 9-Line when integrated into a larger CAS stack or working with a formal JTAC.

### Rotary Wing Specifics
*   **IP vs. BP:** Fixed-wing aircraft use an **IP (Initial Point)** (Line 1) to start their run. Helicopters often use a **BP (Battle Position)** or **HA (Holding Area)**.
*   **Run-in:** Helicopters may not "run in" from miles away. Line 1-3 might be static if firing from a hover in a BP.
*   **Egress (Line 9):** Often "Egress to BP" or "Re-mask" rather than a compass heading.

*For full 9-Line procedures, see the [9-Line CAS Checklist](9-line-cas.md).*

---

## Keyhole CAS for Helicopters

The "Keyhole" template is an efficient way to manage airspace around a target, keeping aircraft organized without rigid IPs.

### The Template
Imagine the **Target** is the center of a clock.
*   **A (Alpha):** North
*   **B (Bravo):** East
*   **C (Charlie):** South
*   **D (Delta):** West
*   **E (Echo):** Overhead (Target location)

### DCS Application
A JTAC might assign a helicopter to a specific sector to deconflict from fixed-wing aircraft or artillery.
*   **Instruction:** "Enfield 1-1, proceed to **Keyhole Delta 5**."
*   **Meaning:** Hold West (Delta) of the target, at 5km distance.

### HAs and BPs in Keyhole
*   **Holding Area (HA):** A safe waiting position. In Keyhole, an HA is often defined by distance (e.g., "Hold Delta 10" = West, 10km).
*   **Battle Position (BP):** The attack position. Helicopters move from the HA to a BP closer to the target (e.g., "Attack from BP Bravo 3" = East, 3km) to fire, then return to the HA.

---

## Helicopter Employment Modes

DCS helicopters can engage targets using three primary flight profiles.

### 1. Running Fire
**Description:** Firing while in forward flight (typically >40 knots).
*   **DCS Advantages:**
    *   **Energy:** Increases rocket kinetic energy and range.
    *   **Safety:** Makes the helicopter a harder target for small arms and unguided RPGs compared to hovering.
    *   **Stability:** Forward flight often provides a more stable platform for unguided rockets (SAS/autopilot stability).
*   **Use Case:** Rocket runs (Hydra/S-8/S-13) or gun runs against area targets.

### 2. Diving Fire
**Description:** Initiating an attack from altitude with a nose-low attitude.
*   **DCS Advantages:**
    *   **Accuracy:** Improved slant range visibility and rocket ballistics.
    *   **Top Attack:** Better angles against tank roof armor (less effective in DCS than real life, but still valid).
*   **Applicable Airframes:** Mi-24P, UH-1H, AH-64D (rockets).
*   **Technique:** Climb to 1500-2000ft AGL, roll in, dive at 10-20 degrees, fire, and break off before entering the WEZ (Weapon Engagement Zone) of SHORAD.

### 3. Hover Fire (The "Sniper" Mode)
**Description:** Firing from a stationary hover, usually masked by terrain or trees.
*   **Low Hover (Masked):**
    *   **Technique:** Establish a hover behind cover (tree line/ridge).
    *   **Unmasking:** "Pop up" vertically just enough to clear sensors/weapons, fire, and immediately "mask" (drop down).
    *   **Duration:** Exposure time should be <10 seconds to avoid ATGM return fire.
*   **High Hover (OGE - Out of Ground Effect):**
    *   **Risk:** High vulnerability. In DCS, only use if outside threat range (>4km for Hellfire/Vikhr) or if no threats exist.
    *   **Considerations:** requires significant power; watch EGT/TGT limits in hot/high conditions.

### 4. Attack Patterns
*   **Racetrack:** Oval pattern. Inbound leg for attack, outbound leg for cooling/reloading. Good for continuous pressure with wingman (Wheel pattern).
*   **Figure-8:** Similar to racetrack but the turn is reversed to keep the target on the same side of the aircraft (or alternate sides).
*   **L-Attack:** Ingress from one direction, attack, and break 90 degrees to egress. Confuses enemy predicting the flight path.
*   **Cloverleaf:** Multiple attack runs from different headings (e.g., North, then West, then South) to avoid predictability.

---

*Based on FM 3-04.126 and DCS World tactics.*
