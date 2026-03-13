# 9-Line CAS Procedures — DCS Checklist

> **Procedure:** Close Air Support (CAS) Request and Execution
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [Overview](#overview)
2. [Roles in CAS](#roles-in-cas)
3. [9-Line Format](#9-line-format)
4. [Requesting CAS (JTAC/FAC Procedures)](#requesting-cas)
5. [Responding to CAS (Pilot/Aircrew Procedures)](#responding-to-cas)
6. [Type I, II, and III CAS](#type-i-ii-and-iii-cas)
7. [Marking Methods](#marking-methods)
8. [Talk-On Procedures](#talk-on-procedures)
9. [Laser Designation Coordination](#laser-designation)
10. [Battle Damage Assessment (BDA)](#battle-damage-assessment)
11. [Abort Criteria](#abort-criteria)
12. [CAS Radio Brevity Codes](#cas-radio-brevity-codes)
13. [9-Line Quick Reference Card](#9-line-quick-reference-card)

---

## Overview

Close Air Support (CAS) is air action against hostile targets that are in close proximity to friendly forces. It requires detailed integration of each air mission with the fire and movement of those forces.

**CAS involves three key players:**
- **JTAC/FAC** — Joint Terminal Attack Controller / Forward Air Controller on the ground
- **Pilot/Aircrew** — Attack aircraft providing fires
- **ASOC/FSCOORD** — Air Support Operations Center / Fire Support Coordinator (oversight)

---

## Roles in CAS

### JTAC / FAC (Forward Air Controller)
- Controls all aircraft providing CAS support
- Issues the 9-line brief to attacking aircraft
- Clears aircraft "hot" for weapons release
- Provides BDA after attack
- Ensures deconfliction from friendly fires

### Pilot / Aircrew
- Checks in with JTAC on assigned frequency
- Reads back 9-line brief
- Confirms visual on target or marks
- Requests and receives "cleared hot"
- Executes attack, reports weapons away
- Reports BDA to JTAC

---

## 9-Line Format

The 9-Line CAS Brief provides the attacking aircraft all information needed for the attack.

```
LINE 1: IP/BP/RP
LINE 2: HEADING TO TARGET (from IP/BP)
LINE 3: DISTANCE (IP/BP to target)
LINE 4: TARGET ELEVATION (MSL in feet)
LINE 5: TARGET DESCRIPTION
LINE 6: TARGET LOCATION (coordinates)
LINE 7: TYPE OF MARK (laser/IR/smoke/grid)
LINE 8: FRIENDLIES (location and distance from target)
LINE 9: EGRESS (direction)

ADDITIONAL:
- REMARKS (restrictions, threat, TOT)
- AUTHENTICATION (if required)
```

---

### Line-by-Line Explanation

#### Line 1 — IP/BP/RP
**Initial Point, Battle Position, or Reference Point**

- Named geographic feature, known waypoint, or coordinate
- Starting point for the attack run
- Example: `"Whiskey, Hotel 3 Alpha"` or `"IP is Checkpoint BRAVO"`

#### Line 2 — Heading
**Magnetic heading from IP to target**

- 3-digit magnetic heading
- Example: `"Two-Seven-Zero degrees"` (270°)
- Pilot flies this heading from IP toward target

#### Line 3 — Distance
**Distance from IP to target in nautical miles or kilometers**

- Example: `"Five-point-five nautical miles"`
- Helps pilot anticipate target acquisition distance

#### Line 4 — Target Elevation
**Target elevation above mean sea level (MSL) in feet**

- Example: `"Elevation one-two-five-zero feet"`
- Used for weapon fuze settings and deconfliction

#### Line 5 — Target Description
**What the target looks like**

- Be specific: vehicle type, color, orientation
- Example: `"Two T-72 tanks, hull down, in tree line, pointing north"`
- Include quantity

#### Line 6 — Target Location
**Grid coordinates of the target**

- MGRS 8 or 10-digit grid, or Lat/Long, or GEOREF
- Example: `"Grid: Three-Seven-Tango-Kilo-five-five-niner-zero-eight-four-seven-zero"`
- Pilot enters in navigation system or notes

#### Line 7 — Mark Type
**How the target will be marked for pilot identification**

| Mark Type | Description |
|---|---|
| Laser | Laser designation — provide laser code |
| IR Pointer | Infrared pointer (needs NVG or FLIR) |
| Smoke | Colored smoke (state color) |
| White Phosphorus (WP) | Smoke/incendiary round |
| Illumination | Illumination round at night |
| Grid Only | No mark — precision grid delivery |
| Self | Pilot marks own target (rare) |

- Example: `"Laser, code one-six-eight-eight"`
- Or: `"Smoke, advise when you have the smoke"`

#### Line 8 — Friendlies
**Location of friendly forces relative to target**

- Direction and distance
- Example: `"Friendlies three-hundred meters south of target"`
- Critical — pilot must deconflict from this position

#### Line 9 — Egress
**Recommended egress direction after attack**

- Cardinal direction or heading
- Example: `"Egress west"` or `"Recommend egress two-seven-zero"`
- Pilot may acknowledge or modify as needed

---

## Requesting CAS

*(JTAC / FAC Perspective)*

### Check-In Sequence

When attack aircraft arrive on frequency:

```
JTAC: "[Callsign], [JTAC callsign], check in, over"
PILOT: "[JTAC callsign], [callsign], two-ship A-10C, 
        mission [number], base plus [ordnance codes], 
        time on station two-zero mikes, over"
JTAC: "Copy, stand by for 9-line"
```

### 9-Line Transmission

Deliver the 9-line clearly, one line at a time, with pauses:

```
JTAC: "[Callsign], 9-line follows:
       Line 1: IP is Checkpoint WHISKEY
       Line 2: Heading zero-four-five
       Line 3: Three-point-zero nautical miles
       Line 4: Elevation five-hundred feet
       Line 5: One BMP-2 infantry fighting vehicle, stationary
       Line 6: Grid three-seven-Tango-Kilo-four-five-six-zero-one-two-three-zero
       Line 7: Laser, code one-six-eight-eight
       Line 8: Friendlies two-hundred meters north, marked by VS-17 panel
       Line 9: Egress west
       Remarks: Single pass, threats SA-13 to the east, 
                 advise when 2 minutes out, over"
```

### Pilot Readback

Pilot reads back and JTAC confirms:

```
PILOT: "Copy 9-line: IP Checkpoint WHISKEY, 
        heading zero-four-five, three-point-zero miles,
        elevation five hundred, BMP-2 stationary,
        grid 37TK45601230, laser one-six-eight-eight,
        friendlies two-hundred north VS-17,
        egress west, remarks single pass SA-13 east, over"
        
JTAC: "[Callsign], readback correct, call inbound"
```

### Clearing Hot

When pilot calls inbound and has visual:

```
PILOT: "[JTAC callsign], [callsign] is in from the east, 
        have laser, over"
        
JTAC: "[Callsign], cleared hot"
OR
JTAC: "[Callsign], ABORT ABORT ABORT — [reason]"
```

---

## Responding to CAS

*(Pilot / Aircrew Perspective)*

### Check-In with JTAC

```
PILOT: "[JTAC callsign], [callsign], check-in, over"
```

Provide:
- Callsign
- Aircraft type and number
- Ordnance (type and quantity)
- Time on station (TOS)
- Remarks (altitude, restrictions)

Example:
```
PILOT: "Axeman, NAIL Two-One, flight of two A-10C, 
        base plus two GBU-12, two Maverick, full gun,
        time on station three-zero minutes,
        currently at eight thousand feet, over"
```

### Receiving the 9-Line

1. [ ] **Get out kneeboard** / note page
2. [ ] Write down each line as transmitted
3. [ ] Confirm unclear items: `"Say again line [number]"`
4. [ ] **Readback entire 9-line** when complete
5. [ ] Confirm readback with JTAC

### 9-Line Copy Format (Kneeboard)

```
┌─────────────────────────────────────┐
│ 9-LINE CAS BRIEF                    │
├─────────────────────────────────────┤
│ 1. IP:                              │
│ 2. HDG:          °                  │
│ 3. DIST:         NM/KM              │
│ 4. ELEV:         ft MSL             │
│ 5. TGT:                             │
│ 6. COORD:                           │
│ 7. MARK:         Code:              │
│ 8. FRENDLY:      / direction        │
│ 9. EGRESS:                          │
│ REMARKS:                            │
└─────────────────────────────────────┘
```

### Attack Execution

1. [ ] From IP, fly heading to target (Line 2)
2. [ ] At distance (Line 3) — begin target search
3. [ ] Acquire target or wait for mark (Line 7)
4. [ ] Confirm visual: `"In sight"` or `"Tally"`
5. [ ] Call inbound: `"[JTAC], [callsign] inbound from [direction]"`
6. [ ] Receive **"Cleared Hot"** before releasing
7. [ ] Release weapons
8. [ ] Call: `"Weapons away"` or `"Rifle/Pickle"`
9. [ ] Egress on Line 9 heading
10. [ ] Report BDA: `"BDA: [target] destroyed/damaged/no effect"`

### If NOT Cleared Hot by Release Point
- **Abort attack**
- Call: `"[callsign] aborting"`
- Egress safely
- Return for another pass or await new brief

---

## Type I, II, and III CAS

### Type I CAS
- **JTAC has visual on aircraft AND target**
- JTAC issues clearance specific to each attack
- Most common and safest

### Type II CAS
- **JTAC has visual on either aircraft OR target, not both**
- Or attack occurs beyond JTAC's visual range (e.g., night, obscured)
- JTAC must positively identify target by mark or description
- Higher risk — use only when required

### Type III CAS
- **JTAC has no visual on aircraft or target**
- Attack authority delegated to aircrew
- Aircrew self-separates from friendlies
- Requires detailed situational awareness

---

## Marking Methods

### Laser Designation
- Most precise
- JTAC uses MBITR/AN/PEQ laser
- OH-58D, A/OA-10, or other aircraft can lase
- **Codes must match** — designator = seeker code
- Default code: **1688** unless otherwise assigned

### Smoke
- Visual mark only — good weather required
- JTAC fires colored smoke round at or near target
- **Do not assume smoke IS the target** — confirm offset
- `"Identify smoke, target is [direction and distance] from smoke"`

### IR Pointer (FLIR/NVG Required)
- JTAC uses AN/PEQ-2 or similar IR pointer
- Only visible with NVG or thermal imager
- Very precise — good for night ops

### WP (White Phosphorus)
- Produces white smoke marker
- Impacts target area
- Burns visually and thermally

### Talk-On / Grid Only
- No physical mark
- Pilot locates target by description and coordinates
- Most demanding on aircrew

---

## Talk-On Procedures

When no mark available, JTAC "talks the pilot's eyes" onto target.

### Talk-On Method
1. JTAC establishes reference point pilot can see
2. Provides offset from reference: `"From the river bend, 500 meters northeast"`
3. Describes target: `"Two vehicles, in the open, stationary"`
4. Pilot confirms: `"Tally two vehicles, in the open"`
5. JTAC confirms: `"That's the target, cleared hot"`

### Reference Points
- Roads, rivers, bridges
- Buildings, towers
- Smoke, fire, dust
- Previous strike impacts

---

## Laser Designation

### Coordinate Laser Codes Before Mission
- Standard code: **1688**
- Mission-specific codes assigned by FAC/JTAC
- All attack aircraft must know designator's code

### Designation Timing
- **Continuous lase:** JTAC lases entire missile/bomb flight
- **Timed lase:** JTAC lases only last 10–15 seconds (preserves battery, reduces detection)
- Pilot calls: `"Lase on my call"` or `"Continuous lase"`

### Verbal Coordination
```
PILOT: "Axeman, NAIL Two-One, thirty seconds"
JTAC:  "NAIL Two-One, thirty seconds, lasing"
PILOT: "NAIL Two-One, in hot"
JTAC:  "NAIL Two-One, cleared hot"
PILOT: "NAIL Two-One, weapons away"
       [10 seconds later]
PILOT: "NAIL Two-One, off, egressing west"
JTAC:  "NAIL Two-One, splash. BDA?"
PILOT: "BDA: one BMP destroyed, secondary explosion observed"
```

---

## Battle Damage Assessment

BDA provided after each attack pass.

### BDA Format
```
"BDA: [target type], [quantity], [result]"
```

| Result | Description |
|---|---|
| Destroyed | Target non-functional, on fire, or exploded |
| Damaged | Target damaged, mission kill possible |
| No Effect | Ordnance did not affect target |
| Unknown | BDA obscured by smoke/dust |

Example:
```
"BDA: two T-72s, both destroyed with secondary explosions, 
      one ZSU-23-4 damaged, no visible secondaries"
```

---

## Abort Criteria

Attack MUST be aborted if:
- [ ] "ABORT" transmitted by JTAC at any time
- [ ] Cannot positively ID target
- [ ] Unsure of friendly position
- [ ] Aircraft not on correct heading from IP
- [ ] Weapon system malfunction
- [ ] Not cleared hot by release point
- [ ] Any doubt about target identification

### Abort Call
```
PILOT: "[callsign], aborting, [reason]"
JTAC:  "Copy abort"
```

---

## CAS Radio Brevity Codes

| Word | Meaning |
|---|---|
| CLEARED HOT | Authorized to release weapons |
| ABORT | Do not release — stop attack immediately |
| RIFLE | AGM-65 Maverick away |
| PICKLE | Bombs/rockets released |
| GUNS | Strafing run |
| SPLASH | Weapons impact on target |
| TALLY | Have visual on target |
| NO JOY | Cannot see target |
| IN | Beginning attack run |
| OFF | Exiting attack run |
| WINCHESTER | Out of ammunition |
| BINGO | Minimum fuel for return |
| FEET DRY | Over land |
| FEET WET | Over water |
| ANGEL | Altitude in thousands of feet |
| BOGEY | Unknown aircraft |
| BANDIT | Confirmed hostile aircraft |
| BUDDY SPIKE | Friendly aircraft locked on by another friendly |

---

## 9-Line Quick Reference Card

> **Print or screenshot this card for tablet/kneeboard use**

```
╔════════════════════════════════════════╗
║       9-LINE CAS QUICK REFERENCE       ║
╠════════════════════════════════════════╣
║ 1. IP/BP/RP: _________________________║
║ 2. HDG (from IP to TGT): _________ ° ║
║ 3. DIST (IP to TGT): __________ NM  ║
║ 4. ELEV (MSL): ______________ ft    ║
║ 5. TGT DESCRIPTION: _______________ ║
║    _________________________________ ║
║ 6. TGT LOCATION: _________________  ║
║ 7. MARK: __________ CODE: _________ ║
║ 8. FRIENDLIES: ___________________ ║
║    DIR from TGT: _________________ ║
║ 9. EGRESS: _______________________ ║
║ REMARKS: _________________________ ║
╠════════════════════════════════════════╣
║ ATTACK SEQUENCE:                      ║
║ □ Copy 9-line  □ Readback              ║
║ □ Fly IP→TGT  □ Acquire               ║
║ □ Call inbound □ Cleared hot           ║
║ □ Weapons away □ Egress               ║
║ □ BDA report                          ║
╚════════════════════════════════════════╝
```

---

## Cross-References
- [Radio Communications →](radio-communications.md)
- [Airfield & ATC →](airfield-atc-communications.md)
- [A-10C Weapons →](../aircraft/a-10c.md#weapons-employment)
- [A-10C II Weapons →](../aircraft/a-10c-ii.md#weapons-employment)
- [Su-25T Weapons →](../aircraft/su-25t.md#weapons-employment)
- [OH-58D Laser Designation →](../aircraft/oh-58d-kiowa.md#laser-designation)

---

*Based on Joint Publication 3-09.3 Close Air Support procedures and Eagle Dynamics DCS documentation. For simulation use only.*
