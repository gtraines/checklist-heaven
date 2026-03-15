# Close Combat Attack (CCA) Data for DCS World

**Reference:** Based on FM 3-04.126 *Attack Reconnaissance Helicopter Operations* and DCS World technical constraints.

## 1. Helicopter Employment Modes

### Running Fire
**Description:** Engaging targets while in level or shallow dive forward flight (typically >40 knots).
*   **DCS Advantages:**
    *   **Energy:** Increases rocket kinetic energy and range.
    *   **Survivability:** Makes the helicopter a harder target for small arms and RPGs compared to a static hover.
    *   **Stability:** Forward flight (ETL) often provides a more stable platform for unguided rockets.

### Diving Fire
**Description:** Initiating an attack from altitude with a steep nose-low attitude (15-20 degrees).
*   **Applicable Airframes:** Mi-24P, UH-1H, AH-64D (rockets).
*   **Technique:** Climb to 1500-2000ft AGL, roll in, dive, fire between 1.5km - 2.5km, and break off before entering the WEZ (Weapon Engagement Zone) of SHORAD.
*   **Advantage:** Improved slant range visibility and rocket ballistics; potential top-attack angles against armor.

### Hover Fire
**Description:** Engagement from a stationary OGE/IGE hover, utilizing terrain masking.
*   **Masking/Unmasking:**
    *   Establish a hover behind cover (tree line/ridge).
    *   **Unmask:** Increase collective to expose sensors/weapons.
    *   **Fire:** Engage target (Hellfire/Vikhr/Tube-launched missiles).
    *   **Mask:** Immediately reduce collective to break Line of Sight (LOS).
    *   **Duration:** Exposure time should be <10 seconds to avoid ATGM return fire.

### Attack Patterns
*   **Racetrack:** Oval pattern. Inbound leg for attack, outbound leg for cooling/reloading. Good for continuous suppression.
*   **Figure-8:** Continuous turns to keep the target on one side (or alternate) while maintaining energy.
*   **L-Attack:** Ingress from one direction, attack, and break 90 degrees to egress. Confuses enemy predicting the flight path.
*   **Cloverleaf:** Multiple attack runs from different headings (e.g., North, then West, then South) to avoid predictability.

---

## 2. Weapons Systems & Switchology

### UH-1H Huey (Gunship Configuration)
| System | Role | DCS Procedure |
| :--- | :--- | :--- |
| **Flex Sights** | Targeting | **Pilot (Right):** Uses XM60 Reflex Sight for fixed-forward fire.<br>**Co-Pilot (Left):** Uses Flexible Sight (pantograph) for off-axis minigun fire. |
| **Door Gunners** | Suppression | **AI:** Use "ROE" menu (`LWin + H`) to set *Return Fire* / *Free Fire*.<br>**Player:** Take manual control (TrackIR/Mouse) for precision work. |
| **Rockets** | 2.75" Hydra | **Sight Depression:** Pilot manually depresses XM60 sight.<br>• **1000m:** ~20-25 mils<br>• **1500m:** ~35-40 mils<br>• **2000m:** ~50-60 mils |

### OH-58D Kiowa Warrior
| System | Role | DCS Procedure |
| :--- | :--- | :--- |
| **MMS** | Sight / Laser | **Acquisition:** CPG slews MMS (TV/Thermal).<br>**Lasing:** 1st detent = Range, 2nd detent = Designate ("L" symbol). Match laser code. |
| **Hellfire** | Anti-Armor | **LOBL:** Lase -> Seeker acquires spot (Box) -> Fire. Requires LOS.<br>**LOAL:** Select LOAL-DIR/LO/HI -> Fire -> Missile acquires laser after launch. |
| **Weapons** | Guns / Rockets | **Fixed Pylons:** Pilot aligns aircraft with "I-Beam" on HUD.<br>**Constraint:** Fire when range cue is within I-Beam dynamic launch zone. |

### Mi-24P Hind
| System | Role | DCS Procedure |
| :--- | :--- | :--- |
| **Crew Roles** | Coordination | **Pilot (Rear):** Flies + Fixed Weapons (Cannon/Rockets).<br>**CP/G (Front/Petrovich):** Operates Raduga-Sh optics, detects targets, guides ATGMs. |
| **30mm Cannon** | Fixed Gun | **ASP-17 Sight:** Set to **Auto** for computed lead/drop.<br>**Rates:** Low (300 rpm) for precision; High (2000+ rpm) for saturation. |
| **Shturm/Ataka** | ATGM | **Guidance:** SACLOS. Pilot aligns aircraft roughly (+/- 60°). CP/G keeps crosshair on target.<br>**Sync:** "Cage" or "Reset" sight before search to prevent gimbal lock. |

---

## 3. CCA vs. CAS Procedures

**Distinction:**
*   **CCA (Close Combat Attack):** Hasty, pilot-controlled attack. The ground unit is an *observer*, not a controller. Pilot makes the engagement decision.
*   **CAS (Close Air Support):** Detailed integration, requires a qualified JTAC/FAC(A) to clear the aircraft "Hot".

### The CCA 5-Line (Attack Aviation Call for Fire)
A friendly-centric, abbreviated format for rapid execution.

| Line | Item | Description |
| :--- | :--- | :--- |
| **1** | **Observer ID / WARNO** | "Uzi 9-1, Fire Mission." |
| **2** | **Friendly Loc / Mark** | "My pos, marked by IR strobe." |
| **3** | **Target Location** | "Direction 330, Distance 800m" (from friendlies). |
| **4** | **Target Desc / Mark** | "BMP in open, marked by tracer." |
| **5** | **Remarks** | "Danger Close, At my Command." |

### The CAS 9-Line (Rotary Wing)
Used when integrating with fixed-wing or formal JTACs.
*   **IP vs. BP:** Helicopters use **Battle Positions (BPs)** instead of Initial Points (IPs).
*   **Run-in:** Lines 1-3 may be static if firing from a hover.
*   **Egress:** Often "Re-mask" or "Return to HA".

### Keyhole CAS
**Template:** Target is the center (Echo). A=North, B=East, C=South, D=West.
*   **Usage:** "Hold Keyhole Delta 5" -> Hold West, 5km from target.
*   **HA vs BP:** Move from **HA** (Holding Area) at distance to **BP** (Battle Position) to fire, then return.

---

## 4. Forward Air Controller (Airborne) [FAC-A]

### Scout/Recce Role
*   **OH-58D Kiowa:** The premier FAC-A platform.
    *   **MMS Advantage:** Can operate in **hull defilade**, exposing only the sight to lase/designate.
    *   **Buddy Lase:** Designates for other aircraft (Hellfires/LGBs) while remaining hidden.
*   **UH-1H Huey:** Limited to visual recce ("Mark 1 Eyeball") or "Recce by Fire". Lacks long-range optics for safe standoff.

### Hunter/Killer Teams
**Concept:** Pairing a "Finder" (Scout) with a "Shooter" (Gunship).

**Common Teams:**
*   **Pink Team (Modern):** **OH-58D** (Finder/Lase) + **AH-64D / Mi-24P** (Shooter).
    *   *Tactic:* OH-58D unmasks and lases. AH-64D fires Hellfire **LOAL** from behind cover.
*   **Heavy Team:** **2x Mi-24P**.
    *   *Tactic:* High/Low. One draws fire/spots (1500ft), one attacks low (NOE).

### Target Handovers
**Methods for passing the target to the shooter:**

1.  **Laser Spot (LSS):**
    *   **Code:** Both aircraft must set the same PRF code (e.g., 1688).
    *   **Geometry:** Shooter must be within +/- 60° of the laser line to see the spot ("The Basket").
2.  **Match Sparkle (IR Pointer):**
    *   Scout: "Sparkle" (Turn on IR pointer).
    *   Shooter: "Contact Sparkle."
    *   *Note:* Requires NVGs.
3.  **Talk-On:**
    *   Using large, distinct terrain features (Roads, Rivers, TRPs).
    *   *DCS Constraint:* Avoid subtle references ("that bush") due to VR/Resolution limits. Use high-contrast objects.
