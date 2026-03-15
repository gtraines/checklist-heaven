# Research Dossier: Surface Attack, CAS, and FAC-A Procedures (DCS World)

**Scope:** A-10C/II, A-10A, Su-25, Su-25T
**Context:** Digital Combat Simulator (DCS) World
**References:** MCWP 3-23.1, DTIC ADA429336, JP 3-09.3

---

## 1. A-10C / A-10C II Thunderbolt II

### Weapons Delivery Parameters (CCIP/CCRP)
| Parameter | High Angle Dive (30-45°) | Low Angle Dive (10-20°) | Level / Loft |
| :--- | :--- | :--- | :--- |
| **Typical Ordnance** | Mk-82, Mk-84, CBU-87/97 | Mk-82AIR, Rockets, Gun | JDAM, LGB, Maverick |
| **Release Altitude** | 4,000 - 6,000 ft AGL | 500 - 1,500 ft AGL | 10,000 - 20,000 ft (JDAM/LGB) |
| **Release Airspeed** | 300 - 350 KIAS | 350 - 450 KIAS | 250 - 300 KIAS |
| **Min Recovery Alt** | 2,000 ft AGL (Frag Avoidance) | 300 ft AGL (requires high drag) | N/A |
| **Gun (GAU-8) Range** | Open Fire: 1.5 - 2.0 NM | Open Fire: 0.8 - 1.2 NM | N/A |

**Switchology & Setup:**
*   **HUD Modes:** Cycle via Master Mode Button (M). Select **CCIP** for visual dive, **CCRP** for level release or lofting designated points.
*   **DSMS (Digital Stores Management):**
    *   **Profile:** Select weapon profile (e.g., MK-82).
    *   **Settings:** Set RP (Ripple Quantity), SGL/PRS (Single/Pairs), and IMP (Impact spacing).
    *   **Laser Code:** For GBU-12/LGBs, set code in DSMS -> INV -> Select Station -> LASER -> 1688.
*   **TGP Laser:** To self-lase, ensure TGP is SOI.
    *   **LATCH:** Toggle LATCH ON in TGP Control page for "One click ON, One click OFF" lasing.
    *   **Fire:** Press Trigger First Detent (if configured) or NWS Button (classic mapping) to fire laser. "L" flashes in HUD/TGP.

### Sensor & Precision Systems
*   **Litening Targeting Pod (TGP):**
    *   **Activation:** Power ON via switch panel. Select TGP on MFD.
    *   **Slew:** Use Slew Control (cursor) to move crosshairs.
    *   **Track Modes:**
        *   TMS Up Short: **Point Track** (Stabilizes on a specific contrast edge/vehicle).
        *   TMS Up Long: **Area Track** (Stabilizes on the ground coordinate).
    *   **Designation:** TMS Right Long sets SPI (Sensor Point of Interest) to TGP center.
*   **Maverick (AGM-65):**
    *   **Slave to TGP:** Set TGP as SOI, find target. China Hat Forward Long slaves all sensors (Maverick) to SPI.
    *   **Lock:** Switch SOI to Maverick (Coolie Hat Right/Left). Slew slightly to refine. TMS Up Short to lock.
    *   **Rifle:** Hold Weapon Release button.

---

## 2. A-10A Thunderbolt II (FC3)

### Weapons Delivery Parameters
*   **Simplified Avionics:** No DSMS or TGP. Visual delivery primary.
*   **Dive Angles:** Standard 30° dive for "Slick" bombs (Mk-82). Put the CCIP pipper on target, release, pull up 4G.
*   **Gun Runs:** "Gun Cross" CCIP mode.
    *   **PAC:** A-10A simulates PAC (Precision Attitude Control) automatically when gun is fired—nose stays stable.
    *   **Range:** Fire at 1.5 NM slant range. Break off by 0.5 NM to avoid fragmentation.

**Switchology:**
*   **Weapon Select:** D to cycle stores (AGM, Bombs, Rockets, Gun).
*   **Mode Select:** 7 (A-G Mode).
*   **Ripple:** LCtrl + Space to change ripple quantity (quantity displayed in HUD).
*   **Maverick:**
    *   Select Maverick.
    *   Slew seeker (Bracket Keys or Axis).
    *   Lock: Enter.
    *   Fire: RAlt + Space (Weapon Release).

---

## 3. Su-25T "Frogfoot"

### Weapons Delivery Parameters
| Parameter | Dive / Run | Level |
| :--- | :--- | :--- |
| **Typical Ordnance** | Vikhr, Rockets, Gun, Bombs | Kh-29T, KAB-500Kr |
| **Airspeed** | 400 - 500 km/h | 400 - 500 km/h |
| **Dive Angle** | 10 - 20° (Shallow) | Level (TV Guided) |

**Switchology:**
*   **Master Arm:** LShift + Space.
*   **A-G Mode:** 7.
*   **Laser:** RShift + O to turn on Laser Rangefinder/Designator. **CRITICAL:** Must be ON for Vikhr, Kh-25ML, Kh-29L, and accurate Gun/Rocket CCIP.
*   **Weapon Select:** D cycles hardpoints.

### Sensor & Precision Systems (Shkval / Vikhr)
*   **Shkval (TV System):**
    *   **Uncage:** O.
    *   **Slew:** Slew keys usually ,. /; or Axis.
    *   **Lock:** Enter. Target box shrinks to size of target (Contrast lock).
    *   **Zoom:** + / - (23x / 8x).
*   **Mercury (LLTV) Pod:**
    *   Must be carried on centerline.
    *   Activates automatically at night when Shkval is uncaged (O), providing green-scale night vision.
*   **9A4172 Vikhr Employment:**
    *   **Type:** Laser Beam Rider.
    *   **Constraint:** You must fly the "Launch Zone" circle onto the target reticle in the HUD.
    *   **Constraint:** Do NOT bank excessively or pull hard Gs while missile is in flight, or it will lose the laser beam.
    *   **Launch:** Press and hold release (Space or RAlt+Space) until missile departs (approx 1 sec delay). Keep nose steady until impact.

---

## 4. Su-25 "Grach" (Standard)

### Weapons Delivery Parameters
*   **Visual Only:** No TV screen. Pilot aims through the HUD (ASP-17 gunsight).
*   **Laser:** RShift + O activates Klen-PS laser rangefinder in the nose.
*   **Bombing:**
    *   Dive at 20-30°.
    *   Pip is "Computed" (CCIP) based on laser range. If laser is OFF, it uses barometric altitude (less accurate).
*   **Laser Guided Missiles (Kh-25ML, Kh-29L):**
    *   Dive required.
    *   Slew the laser designator reticle in the HUD.
    *   Lock (Enter) stabilizes the laser spot on the ground.
    *   Launch and maintain dive until impact (Laser has limited gimbal limits—don't pull up too early or laser mask occurs).

---

## 5. Close Air Support (CAS) Standards

### CAS Check-In (Radio Call)
Standard format when arriving on station to contact JTAC/FAC-A.
> "Playboy 1-1, Hog 1-1." (Establish Comms)
> "Hog 1-1, this is Playboy 1-1. Proceed to IP Ford. Advise when ready for check-in."
> "Hog 1-1 ready."

**Format (MNPOPCA):**
1.  **M**ission Number (Optional in DCS)
2.  **N**umber and Type of Aircraft ("2 times A-10C")
3.  **P**osition and Altitude ("IP Ford, angels 15")
4.  **O**rdnance ("2 times GBU-12, 1 time GBU-38, 1150 rounds gun")
5.  **P**laytime (Time on Station) ("30 mikes")
6.  **C**apabilities ("TGP, Laser, IR Pointer")
7.  **A**bort Code (if applicable)

### The 9-Line Briefing
The standard format for passing target data. **Read back lines 4, 6, and restrictions.**

1.  **IP / BP:** (Initial Point / Battle Position) - "IP Ford"
2.  **Heading:** (IP to Target) - "Magnetic 1-8-0"
3.  **Distance:** (IP to Target) - "12 Nautical Miles"
4.  **Elevation:** (Target Elevation) - "1,250 feet MSL"
5.  **Target Description:** - "Two T-72 tanks in open"
6.  **Target Coordinates:** - "NB 123 456" (MGRS preferred) or Lat/Long
7.  **Mark:** (Type of Mark) - "Laser 1688" or "WP"
8.  **Friendlies:** (Location of nearest friendlies) - "South 500 meters"
9.  **Egress:** (Exit direction) - "Turn East, pull to angels 20"

**Remarks:** "Final attack heading 170 through 190. Danger Close."

### Keyhole CAS Template (Doctrinal Deep Dive)
The Keyhole Template provides an efficient method for airspace control without the rigidity of formal Airspace Coordination Areas (ACAs). It is anchor-based geometry centered on the **Target**.

**1. Geometry & Anchors:**
The template is built around the Target (Center) and five anchor points:
*   **Alpha (A):** North (360° Magnetic)
*   **Bravo (B):** East (090° Magnetic)
*   **Charlie (C):** South (180° Magnetic)
*   **Delta (D):** West (270° Magnetic)
*   **Echo (E):** Overhead the Target

**2. Holding Procedures:**
Holds are directed by giving the Anchor Point and the Distance (in Nautical Miles) from the target.
*   **Command:** "Hold [Anchor Point] [Distance]"
*   **Example:** "Hog 1-1, Hold **Alpha 10**."
    *   *Meaning:* Hold North of the target at 10 NM.
    *   *Action:* Aircraft establishes a race-track pattern centered on the Alpha radial at 10 NM.
*   **Example:** "Hold **Delta 5**."
    *   *Meaning:* Hold West of the target at 5 NM.

**3. Ingress & Egress:**
The Keyhole allows the FAC-A/JTAC to dictate attack direction to avoid artillery Gun Target Lines (GTLs) or other threats.
*   **Command:** "Ingress [Anchor Point], Egress [Anchor Point]"
*   **Example:** "Ingress Alpha, Egress Bravo."
    *   *Meaning:* Attack from the North (heading South to target), then turn East after the attack.

**4. Altitude Deconfliction:**
Multiple flights can hold at the same Anchor Point if separated by altitude.
*   **CAS Stack:** Aircraft waiting for their turn. (e.g., Angels 18-20).
*   **FAC-A:** Operating altitude (e.g., Angels 14-15).
*   **Gun Target Line (GTL):** Artillery apex must be avoided (e.g., Stay above Angels 12).
*   **Example Call:** "Hog 1-1, Hold Alpha 8, Angels 15. Viper 2-1, Hold Alpha 8, Angels 20."

### Essential Brevity Codes
*   **Tally:** Pilot sees the *Target*.
*   **Visual:** Pilot sees *Friendly* aircraft/troops.
*   **Contact:** Pilot sees a specified reference point (landmark).
*   **Blind:** Pilot does NOT see the friendly aircraft/troops.
*   **No Joy:** Pilot does NOT see the target.
*   **Rifle:** Air-to-Ground missile launch (Maverick).
*   **Pickle:** Bomb release.
*   **Guns Guns Guns:** Gun firing.
*   **In:** Entering the terminal attack run.
*   **Off:** Attack complete, turning away.
*   **Winchester:** Out of ordnance.
*   **Bingo:** Fuel state requiring return to base.

---

## 6. Forward Air Controller (Airborne) [FAC-A]

### Stack Management & The Keyhole
The FAC-A is responsible for deconflicting multiple assets (The Stack). The Keyhole Template is the primary tool for this.

**1. Wheel vs. Keyhole:**
*   **The Wheel:** Aircraft orbit the target at a constant radius (visual observation). *Drawback:* Hard to deconflict with artillery/surface fire; predictable flight path.
*   **The Keyhole:** Aircraft hold at static points (Alpha-Delta) and only enter the center when cleared. *Advantage:* Keeps aircraft out of the threat/artillery zone until "Cleared Hot."

**2. Managing the Stack:**
The FAC-A builds a "wedding cake" of airspace layers above the battlefield.
*   **Top Layer (Transit/Hold):** Assets checking in or awaiting tasking (e.g., Angels 20+).
*   **Middle Layer (The Stack):** Assets holding at Keyhole points, briefed and ready (e.g., Angels 15-19).
*   **Low Layer (FAC-A / Working):** The FAC-A (if visual) or the asset currently attacking (e.g., Angels 5-14).

**3. Execution Sequence:**
1.  **Check-In:** Aircraft arrives at IP.
2.  **Stacking:** FAC-A directs: "Proceed Alpha 10, Block Angels 20 to 22."
3.  **Briefing:** FAC-A passes 9-line while aircraft holds at Alpha.
4.  **Ingress:** FAC-A calls: "Push from Alpha, Ingress Alpha, Egress Delta."
5.  **Attack:** Aircraft leaves Alpha 10, drops altitude to attack parameters, strikes target.
6.  **Egress:** Aircraft turns West (Delta), climbs back to stack altitude, returns to Hold Delta or Alpha as directed.

### Marking Procedures
*   **Willie Pete (WP):** White Phosphorus rockets (M156/M274).
    *   FAC-A dives and fires rocket near target.
    *   Call: "Mark is on deck."
    *   Attacker: "Contact the mark."
    *   FAC-A: "From the mark, West 50 meters, T-72."
*   **Sparkle (IR Pointer):**
    *   Night only. Uses TGP IR Pointer.
    *   FAC-A: "Sparkle ON."
    *   Attacker (NVGs ON): "Contact Sparkle."
    *   FAC-A: "Snake" (Wiggle the beam to distinguish from clutter).

### Talk-On Techniques
Guiding the attacker's eyes to the target using large-to-small references.
1.  **Anchor Point:** Large, obvious landmark ("See the large lake?").
2.  **Funnel:** Narrow down ("Go to the north tip of the lake").
3.  **Reference:** Local feature ("Follow the road east to the T-intersection").
4.  **Target:** Specific object ("At the intersection, the bunker on the NE corner").
