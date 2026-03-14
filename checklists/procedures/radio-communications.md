# Military Aviation Radio Communications — DCS Checklist

> **Procedure:** Military Aviation Radio Procedures, Frequencies, and Phraseology
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [Overview](#overview)
2. [Radio Types in DCS](#radio-types-in-dcs)
3. [Standard Frequency Cards](#frequency-cards)
4. [NATO Phonetic Alphabet](#nato-phonetic-alphabet)
5. [Standard Brevity Codes](#standard-brevity-codes)
6. [Check-In Procedures](#check-in-procedures)
7. [AWACS Procedures](#awacs-procedures)
8. [Tanker/Air Refueling Comms](#tankerair-refueling-comms)
9. [Formation Communications](#formation-communications)
10. [Mayday & Emergency Procedures](#mayday--emergency-procedures)
11. [Position Reports](#position-reports)
12. [Radio Discipline](#radio-discipline)
13. [DCS Radio System](#dcs-radio-system)
14. [Quick Reference](#quick-reference)

---

## Overview

Military aviation communication follows strict protocols for clarity, brevity, and safety. In DCS multiplayer, following these procedures improves coordination and immersion. The basics apply to all aircraft in this checklist collection.

**Radio discipline = mission success and safety.**

---

## Radio Types in DCS

### Common Radio Equipment by Aircraft

| Aircraft | VHF/FM | UHF | Additional |
|---|---|---|---|
| A-10C/C II | ARC-186 (VHF) | ARC-164 (UHF) | ARC-210 (A-10C II) |
| Su-25T | R-862 | R-862 (dual mode) | — |
| UH-1H Huey | ARC-131 (FM) | ARC-134 (UHF) | — |
| Mi-24P | R-863 (UHF) | R-828 (FM) | — |
| OH-58D | ARC-201 (VHF/FM) | ARC-164 (UHF) | — |

### Frequency Bands
| Band | Range | Military Use |
|---|---|---|
| VHF Low (30–88 MHz) | Short range | Ground forces, Army aviation |
| VHF High (118–137 MHz) | Civil ATC | Civil control (used in DCS ATC) |
| VHF Military (138–174 MHz) | Long range | Tactical |
| UHF (225–400 MHz) | Long range | Primary military aviation |

---

## Frequency Cards

### Guard Frequencies (Always Monitor)
| Type | Frequency |
|---|---|
| UHF Guard | **243.000 MHz** |
| VHF Guard | **121.500 MHz** |

### Common DCS Frequencies (Default Missions)

| Service | Frequency | Notes |
|---|---|---|
| ATC (tower) | Per airfield — check ATIS | Varies by map/mission |
| AWACS / GCI | 251.000 MHz UHF (common) | Check briefing |
| Tanker | 270.000 MHz UHF (common) | Check briefing |
| FAC/JTAC | Assigned per mission | Brief on ground |
| Flight Common | 265.000 MHz UHF | Intra-flight |

### CAUCASUS Map Common Frequencies

| Airfield | Tower | Approach | ATIS |
|---|---|---|---|
| Batumi | 131.000 | 133.000 | 128.000 |
| Kutaisi | 134.000 | 133.000 | 128.000 |
| Kobuleti | 133.000 | 133.000 | — |
| Senaki | 132.000 | 133.000 | — |
| Tbilisi Lochini | 139.000 | 133.000 | 128.000 |
| Maykop | 135.000 | 133.000 | — |

### PERSIAN GULF Map Common Frequencies

| Airfield | Tower | Approach |
|---|---|---|
| Al Dhafra | 118.650 | 121.100 |
| Al Minhad | 118.500 | 121.600 |
| Dubai International | 118.750 | 124.900 |
| Fujairah | 118.900 | 121.700 |

---

## NATO Phonetic Alphabet

| Letter | Phonetic | Letter | Phonetic |
|---|---|---|---|
| A | **Alpha** | N | **November** |
| B | **Bravo** | O | **Oscar** |
| C | **Charlie** | P | **Papa** |
| D | **Delta** | Q | **Quebec** |
| E | **Echo** | R | **Romeo** |
| F | **Foxtrot** | S | **Sierra** |
| G | **Golf** | T | **Tango** |
| H | **Hotel** | U | **Uniform** |
| I | **India** | V | **Victor** |
| J | **Juliet** | W | **Whiskey** |
| K | **Kilo** | X | **X-ray** |
| L | **Lima** | Y | **Yankee** |
| M | **Mike** | Z | **Zulu** |

### Numbers (Standard Pronunciation)
| Digit | Say As |
|---|---|
| 0 | "ZEE-ro" |
| 1 | "WUN" |
| 2 | "TOO" |
| 3 | "TREE" |
| 4 | "FOW-er" |
| 5 | "FIFE" |
| 6 | "SIX" |
| 7 | "SEV-en" |
| 8 | "AIT" |
| 9 | "NIN-er" |

---

## Standard Brevity Codes

### Common Air-to-Air Brevity

| Word | Meaning |
|---|---|
| BOGEY | Unknown aircraft |
| BANDIT | Confirmed hostile aircraft |
| HOSTILE | Positively ID'd enemy |
| FRIENDLY | Confirmed friendly |
| BULLSEYE | Designated reference point for position reports |
| ANGELS | Altitude in thousands of feet (Angels 10 = 10,000 ft) |
| BUSTER | Fly at max speed |
| PLAYTIME | Time remaining on station |
| BINGO | Minimum fuel for recovery |
| WINCHESTER | All weapons expended |
| SPLASH | Target destroyed |
| TALLY | Visual on target/bandit |
| VISUAL | Visual on friendly aircraft |
| NO JOY | Cannot see the target/bandit |
| BLIND | Cannot see friendly |
| CONTACT | Radar/visual contact |
| LOCK | Radar lock on target |
| NAKED | No radar warning receiver indication |
| SPIKE | RWR indication of nose-aspect radar |
| BUDDY SPIKE | RWR lock from friendly (IFF failure) |
| BANZAI | Immediate attack, all aircraft |
| BRAKE | Turn immediately in stated direction |
| ANCHOR | Establish orbit over a point |
| FENCE | Transition from/to combat area |
| FENCE IN | Arm weapons, ECM on — entering combat |
| FENCE OUT | Safe weapons, ECM off — leaving combat |

### Air-to-Ground Brevity

| Word | Meaning |
|---|---|
| CLEARED HOT | Authorized to release weapons |
| ABORT | Do not release — stop attack |
| IN | Beginning attack run |
| OFF | Exiting attack run |
| PICKLE | Bomb release initiated |
| RIFLE | AGM-65 Maverick fired |
| GUNS | Strafing run |
| SNAKE | Maverick/laser-guided missile in flight |
| TRACK | Missile/bomb tracking |
| SPLASH | Weapon impact |
| SHACK | Direct hit on target |
| CONTINUE | Continue attack |
| JOKER | Fuel at planned recovery level |
| TEXACO | Tanker callsign (also: request refueling) |
| FEET DRY | Over land |
| FEET WET | Over water |

---

## Check-In Procedures

### Checking in with AWACS / GCI

```
FORMAT: "[Station callsign], [your callsign], [info]"

EXAMPLE:
PILOT: "Magic, NAIL Two-One, check-in"
AWACS: "NAIL Two-One, Magic, go ahead"
PILOT: "Magic, NAIL Two-One, flight of two A-10C
        northwest of Batumi, looking for picture, over"
AWACS: "NAIL Two-One, picture clean, CAP is two Angels 
        south of Bullseye, advise when ready for tasking"
```

### Standard Check-In Information
- Callsign
- Aircraft type and number
- Current position (or area)
- Current altitude
- Ordnance / mission capability
- Fuel (time on station or BINGO time)
- Special equipment (FLIR, laser, etc.)

### FENCE IN Checklist
Before entering combat area:
- [ ] **Master Arm** — ARM
- [ ] **ECM** — ON
- [ ] **Chaff/Flare** — armed and program set
- [ ] **IFF** — verify codes correct
- [ ] **Radios** — set to tactical frequencies
- [ ] **Weapons** — selected and ready
- [ ] **Comms** — check with flight lead

---

## AWACS Procedures

### AWACS / GCI Services Available

| Service | Description |
|---|---|
| Picture | Status of air threat picture |
| Bogey Dope | Bearing, range, altitude of specific contact |
| Declare | Pilot asks AWACS to ID a contact |
| Vector | AWACS gives heading to intercept |
| Buddy | Position of specific friendly aircraft |

### AWACS Radio Calls

#### Requesting Picture
```
PILOT: "Magic, NAIL Two-One, request picture"
AWACS: "NAIL Two-One, picture: two groups, bullseye 
        zero-six-zero, forty, angels twelve. 
        Second group bullseye two-seven-zero, 
        thirty, angels eight"
```

#### Declaring a Contact
```
PILOT: "Magic, NAIL Two-One, declare, bearing 
        two-seven-zero, twenty miles, low"
AWACS: "NAIL Two-One, declare: hostile"
   OR: "NAIL Two-One, declare: friendly"
   OR: "NAIL Two-One, unable"
```

#### Requesting Bogey Dope
```
PILOT: "Magic, NAIL Two-One, bogey dope"
AWACS: "NAIL Two-One, single group, bearing 
        zero-nine-zero, thirty miles, angels ten, 
        hot" (approaching)
```

---

## Tanker/Air Refueling Comms

### Tanker Check-In

```
PILOT: "Texaco, NAIL Two-One, request AR"
TANKER: "NAIL Two-One, Texaco, state your position 
         and fuel state"
PILOT: "Texaco, northwest of Kobuleti, 3.5 internal, 
        request pre-contact"
TANKER: "NAIL Two-One, cleared pre-contact, 
         on my right wing, 
         290 degrees, 20,000 feet, 275 knots"
```

### Refueling Sequence
```
PILOT: "NAIL Two-One, pre-contact"     (approaching)
TANKER: "Cleared contact"              (clear to connect)
PILOT: "NAIL Two-One, contact"        (boom/drogue connected)
TANKER: "Receiving"                    (fuel flowing)
PILOT: "Full, disconnect"              (done)
TANKER: "Breakaway, breakaway"        (emergency)
```

### AR Brevity
| Word | Meaning |
|---|---|
| TEXACO | Tanker (or request AR) |
| PREBRIEFED | Follow prebriefed AR plan |
| PRE-CONTACT | Positioned, ready to connect |
| CONTACT | Connected to boom/drogue |
| OVERRUN | About to overrun tanker |
| BREAKAWAY | Emergency disconnect immediately |

---

## Formation Communications

### Basic Formation Radio Calls

#### Flight Internal (encrypted / discrete freq)

```
LEAD: "Two, check left/right"
WING: "Two" (acknowledge)

LEAD: "Two, go Combat Spread"
WING: "Two" (moving)

LEAD: "Two, push [frequency]"
WING: "Two" (switching)
```

#### Standard Formation Calls
| Call | Meaning |
|---|---|
| "Go tactical" | Switch to tactical frequency |
| "Go combat spread" | 1–2 NM abreast formation |
| "Tightened up" | Close formation |
| "Visual" | Flight member has visual on lead |
| "Blind" | Flight member lost visual on lead |
| "One, two's blind" | Wing is blind to lead |
| "Check fuel" | Lead calls fuel check |
| "State" | Report fuel and weapons remaining |

### State Report Format
```
"[callsign], [fuel: lbs or time], [weapons remaining]"
Example: "Two, 4.2 [thousand lbs], 2 Maverick, full gun"
```

---

## Mayday & Emergency Procedures

### MAYDAY Call
For life-threatening emergency:

```
FORMAT:
"MAYDAY MAYDAY MAYDAY
 [Station callsign] on Guard
 [Own callsign]
 [Nature of emergency]
 [Position]
 [Intentions]
 [Aircraft type]
 [Souls on board (if applicable)]"

EXAMPLE:
"MAYDAY MAYDAY MAYDAY
 Any station on Guard
 NAIL Two-One
 Engine fire, declared emergency
 15 miles northwest of Batumi at 8,000 feet
 Attempting single-engine return to Batumi
 A-10C, two souls on board"
```

### PAN-PAN Call
For urgent but not immediately life-threatening:

```
"PAN PAN PAN
 [Station]
 [Callsign]
 [Problem]"
```

### Squawk Emergency
- Set transponder to **7700** (emergency)
- **7600** — Radio failure
- **7500** — Hijack

### DCS Emergency
In DCS: press `\` to access comms menu, then contact ATC.
Squawk 7700: set on IFF panel.

---

## Position Reports

### Standard Position Report Format

```
"[Station], [callsign], [position], [altitude], [intentions]"

EXAMPLE:
"Batumi Approach, NAIL Two-One, 
 30 miles northwest, 10,000 feet, 
 inbound for landing, request approach information"
```

### Bullseye Position Report
Used to protect own position while reporting to AWACS:

```
"[Callsign], Bullseye [bearing]/[distance], [altitude]"
EXAMPLE:
"NAIL Two-One, Bullseye zero-four-five/forty, 
 angels ten, heading south"
```

Bullseye is a pre-briefed reference point known to all.

---

## Radio Discipline

### Golden Rules
1. **Think before you transmit** — know what you're going to say
2. **Brief, clear transmissions** — brevity saves lives
3. **Station — Callsign — Message** (who you're calling — who you are — what you want)
4. **Listen before transmitting** — don't step on others
5. **Don't use first names** — use callsigns
6. **Acknowledge all messages** — even if just your callsign
7. **Never say "repeat"** — say "say again" (repeat has artillery meaning)
8. **"Over"** — your transmission complete, expect reply
9. **"Out"** — conversation complete, no reply expected
10. **"Roger"** — message received and understood
11. **"Wilco"** — will comply with instruction

### Common Mistakes to Avoid
- ❌ "Uh..." — dead air
- ❌ "Yeah" — non-standard
- ❌ "Repeat" — (means fire again in artillery)
- ❌ Saying your callsign twice when calling someone else
- ❌ Transmitting over another transmission

---

## DCS Radio System

### Opening Radio Menu
- `\` (backslash) — opens comms menu
- Number keys select menu items
- Submenus for ATC, AWACS, Wingmen, etc.

### DCS AI Radio Interaction
The radio menu allows:
- ATC requests (taxi, takeoff, approach, landing)
- AWACS/GCI contact
- Tanker contact
- Wingman commands

### Comms Key Reference
| Function | Key |
|---|---|
| Radio menu | `\` (backslash) |
| Close menu | `Esc` |
| Select option | number keys |
| Request ATC | `\` → ATC |
| AWACS/GCI | `\` → AWACS |

---

## Quick Reference

### Radio Call Cheat Sheet

| Situation | Say |
|---|---|
| Checking in | "[Station], [callsign], check in" |
| Have visual on target | "Tally [target]" |
| No visual on target | "No Joy" |
| Have visual on friendly | "Visual" |
| Lost visual on friendly | "Blind" |
| Ready to attack | "[callsign] in [from direction]" |
| Weapon released | "Pickle / Rifle / Guns" |
| Off target | "[callsign] off [direction]" |
| Hit | "Shack" |
| Miss | "No effect" |
| Emergency | "Mayday Mayday Mayday" |
| Abort | "Abort" |
| Out of gas | "Bingo" |
| Out of weapons | "Winchester" |

---

## Cross-References
- [9-Line CAS Procedures →](9-line-cas.md)
- [Airfield & ATC Communications →](airfield-atc-communications.md)
- [A-10C Comms Setup →](../aircraft/a-10c.md#avionics--systems)
- [NS430 Radio Management →](../aircraft/ns430.md#radio-management)
- [Back to Index →](../index.md)

---

*Based on ICAO and NATO aviation communication standards. For simulation use only.*
