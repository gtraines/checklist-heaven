# Military Airfield & ATC Communications — DCS Checklist

> **Procedure:** Military Airfield and Air Traffic Control Communications
>
> [← Back to Index](../index.md)

---

## Table of Contents
1. [Overview](#overview)
2. [Airfield Services & Frequencies](#airfield-services--frequencies)
3. [Departure Procedures](#departure)
4. [Arrival & Approach Procedures](#arrival--approach)
5. [Landing & Taxi In](#landing--taxi-in)
6. [Instrument Approaches](#instrument-approaches)
7. [ATIS / Field Information](#atis--field-information)
8. [Ground Movement](#ground-movement)
9. [Pattern Procedures](#pattern-procedures)
10. [Hot Pit / FARP Operations](#hot-pit--farp-operations)
11. [IFR Procedures](#ifr-procedures)
12. [Communication Failure](#communication-failure)
13. [DCS ATC Operations](#dcs-atc-operations)
14. [Airfield Quick Reference Cards](#airfield-quick-reference-cards)

---

## Overview

Military airfield communications follow a structured sequence from initial contact to engine shutdown. In DCS, AI ATC services are available at most airfields and respond to standard calls via the radio menu (`\`).

**Key principle:** Each frequency serves a specific phase of flight. Transition between them at the appropriate time.

---

## Airfield Services & Frequencies

### Standard ATC Frequency Sequence

| Service | Phase | Typical Freq (civil) | Military |
|---|---|---|---|
| **ATIS** | Before calling | 118–136 MHz | 118–400 MHz |
| **Clearance Delivery** | Before taxi | 118–136 MHz | Less common |
| **Ground Control** | Taxi | 121.600–121.925 | Varies |
| **Tower** | Takeoff/Landing | 118–136 MHz | 118–400 MHz |
| **Approach Control** | Arrival | 119–136 MHz | 118–400 MHz |
| **Departure Control** | Departure | 119–136 MHz | 118–400 MHz |
| **En Route / AWACS** | Transit | — | 225–400 MHz UHF |
| **Guard** | Emergency | 121.500 VHF / 243.000 UHF | Always |

### DCS Default Frequencies by Map

#### Caucasus Map — Key Fields
| Field | Tower | Approach/Departure | Ground |
|---|---|---|---|
| Batumi | 131.000 | 133.000 | 130.000 |
| Kobuleti | 133.000 | 133.000 | — |
| Senaki | 132.000 | 133.000 | — |
| Kutaisi | 134.000 | 133.000 | — |
| Tbilisi Lochini | 139.000 | 133.000 | — |
| Gudauta | 130.000 | 133.000 | — |
| Beslan | 141.000 | 133.000 | — |
| Mozdok | 135.000 | 133.000 | — |

#### Syria Map — Key Fields
| Field | Tower | Approach |
|---|---|---|
| Incirlik | 360.800 | 123.300 |
| Akrotiri | 123.300 | 123.600 |
| Ramat David | 118.200 | 119.700 |
| Hatzerim | 118.700 | 123.600 |

#### Persian Gulf Map — Key Fields
| Field | Tower | Approach |
|---|---|---|
| Al Dhafra | 118.650 | 121.100 |
| Al Minhad | 118.500 | 121.600 |
| Al Ain | 118.400 | 121.100 |
| Fujairah | 118.900 | 121.700 |

---

## Departure

### Pre-Departure Flow

#### Step 1 — ATIS / Field Information
- [ ] Tune ATIS frequency
- [ ] Copy: **winds, active runway, QNH/altimeter, NOTAMs**
- [ ] Note ATIS identifier letter (e.g., "Information CHARLIE")

#### Step 2 — Ground Taxi Clearance
```
FORMAT:
"[Ground], [callsign], at [location], request taxi"

EXAMPLE:
PILOT: "Batumi Ground, NAIL Two-One, 
        flight of two at the ramp, 
        ready to taxi, have Information Charlie"
GROUND: "NAIL Two-One, Batumi Ground, 
         taxi Runway Two-Seven via Taxiway Alpha, 
         QNH 1013"
PILOT: "Runway Two-Seven, Taxiway Alpha, 
        QNH 1013, NAIL Two-One"
```

#### Step 3 — Takeoff Clearance
```
FORMAT:
"[Tower], [callsign], [position], ready for departure"

EXAMPLE:
PILOT: "Batumi Tower, NAIL Two-One, 
        holding short Runway Two-Seven, 
        ready for departure"
TOWER: "NAIL Two-One, Batumi Tower, 
        cleared for takeoff Runway Two-Seven, 
        winds two-eight-zero at twelve"
PILOT: "Cleared takeoff Two-Seven, NAIL Two-One"
```

#### After Takeoff
```
TOWER: "NAIL Two-One, contact Departure on 133.000"
PILOT: "133.000, NAIL Two-One"
```

#### Step 4 — Departure Control
```
PILOT: "Batumi Departure, NAIL Two-One, 
        passing through two thousand, 
        heading north"
DEPARTURE: "NAIL Two-One, radar contact, 
            climb and maintain flight level one-five-zero, 
            proceed on course"
```

---

## Arrival & Approach

### Step 1 — En Route Descent / ATIS

Approximately 50–100 NM from field:
- [ ] Copy ATIS (tune ATIS frequency)
- [ ] Note: runway in use, winds, altimeter, conditions

### Step 2 — Approach Control Contact
```
FORMAT:
"[Approach], [callsign], [position], [altitude], [intentions]"

EXAMPLE:
PILOT: "Batumi Approach, NAIL Two-One, 
        forty miles northwest at ten thousand, 
        inbound for landing, have Information Alpha"
APPROACH: "NAIL Two-One, Batumi Approach, 
           radar contact, expect ILS Runway Two-Seven, 
           descend and maintain five thousand, 
           altimeter 1013"
PILOT: "Descend five thousand, altimeter 1013, 
        ILS Runway Two-Seven, NAIL Two-One"
```

### Step 3 — Vectors to Final

ATC provides radar vectors to intercept the ILS/approach:
```
APPROACH: "NAIL Two-One, fly heading two-five-zero, 
           intercept localizer Runway Two-Seven"
APPROACH: "NAIL Two-One, descend and maintain 
           two thousand, cleared ILS approach 
           Runway Two-Seven"
PILOT: "Descend two thousand, cleared ILS Two-Seven, 
        NAIL Two-One"
```

### Step 4 — Tower Contact
When cleared for approach or on short final:
```
APPROACH: "NAIL Two-One, contact Tower on 131.000"
PILOT: "131.000, NAIL Two-One"

PILOT: "Batumi Tower, NAIL Two-One, 
        final ILS Runway Two-Seven"
TOWER: "NAIL Two-One, cleared to land 
        Runway Two-Seven, winds two-eight-zero 
        at ten"
```

---

## Landing & Taxi In

### Touch-and-Go
```
TOWER: "NAIL Two-One, cleared touch-and-go, 
        Runway Two-Seven"
PILOT: "Touch-and-go Two-Seven, NAIL Two-One"
```

### After Landing
```
TOWER: "NAIL Two-One, contact Ground on 130.000"
PILOT: "130.000, NAIL Two-One, good day"

PILOT: "Batumi Ground, NAIL Two-One, 
        off Two-Seven, request taxi to ramp"
GROUND: "NAIL Two-One, taxi to ramp via Taxiway Alpha"
```

### Parking Confirmation
When at parking:
- [ ] Aircraft shutdown per checklist
- [ ] Log off frequency (in real life — just monitor in DCS)

---

## Instrument Approaches

### ILS (Instrument Landing System)

**Components:**
- **Localizer** — lateral guidance (L/R of centerline)
- **Glide Slope** — vertical guidance (3° descent path)
- **Outer Marker** — typically 4–7 NM from runway

#### ILS Approach Checklist
- [ ] **ILS frequency** — set on NAV radio
- [ ] **Approach course** — set on HSI/CDI
- [ ] **Altimeter** — set QNH
- [ ] **Gear** — DOWN by 10 NM from runway
- [ ] **Flaps** — landing setting by glide slope intercept
- [ ] Intercept localizer: CDI centers L/R
- [ ] Intercept glide slope: G/S indicator centers V
- [ ] Descend at **~500 fpm** on 3° slope
- [ ] **DH (Decision Height)** — typically 200 ft AGL
- [ ] At DH: runway visible → land / not visible → **missed approach**

#### Typical ILS Speeds
| Phase | Speed |
|---|---|
| Initial approach | 200 kts |
| Intercept glide slope | 150–160 kts |
| Final approach | 130–150 kts |
| Touchdown | 120–130 kts |

### VOR Approach
- Provides only lateral guidance
- CDI tracks VOR radial
- Descent per step-down fixes
- MDA (Minimum Descent Altitude) not descended below until runway in sight

### NDB (ADF) Approach
- Aircraft ADF points toward NDB station
- Track inbound heading to runway
- Older, less precise

### GPS / RNAV Approach
- GPS provides lateral and vertical guidance (LPV/LNAV+V)
- Use CDI in GPS mode
- A-10C uses RNAV; NS430 provides RNAV

---

## ATIS / Field Information

### ATIS Content Format

```
[Field name] INFORMATION [LETTER] [TIME ZULU]
RUNWAY [number] IN USE
WIND [direction] AT [speed], GUSTS [if applicable]
VISIBILITY [statute miles or km]
CEILING [height] [broken/overcast/few]
TEMPERATURE [°C], DEWPOINT [°C]
ALTIMETER/QNH [setting]
REMARKS: [NOTAMs, special conditions]
ADVISE [callsign] YOU HAVE INFORMATION [LETTER]
```

### Reading Back ATIS
Always tell ATC which ATIS you have:
`"Have Information [LETTER]"`

---

## Ground Movement

### Taxi Instructions
- **Runway:** always read back runway number
- **Taxiways:** note taxiway letters/names
- **Hold Short:** stop before the runway hold short line
- **Cross Runway:** explicit clearance required

### Taxiway Lights (at night)
| Color | Meaning |
|---|---|
| Blue | Taxiway centerline |
| Green | Runway centerline |
| White | Runway edge |
| Red | Runway hold point |
| Yellow | Taxiway centerline |

### Hot Spots
Areas of increased collision risk — usually announced by Ground:
`"Taxi via Taxiway Alpha, caution Hot Spot One"`

---

## Pattern Procedures

### Standard Traffic Pattern (VFR)

```
[Upwind]  →  [Crosswind]  →  [Downwind]  →  [Base]  →  [Final]
 Takeoff      Turn 90°       Parallel        Turn        Final
              at 500 ft AGL  to runway     to runway    approach
```

**Standard altitude:** 1,000 ft AGL  
**Standard distance:** 1–1.5 NM from runway on downwind

### Pattern Radio Calls
| Phase | Call |
|---|---|
| Taking off | "NAIL Two-One, departing Runway Two-Seven" |
| Crosswind | (usually no call required) |
| Downwind | "NAIL Two-One, Runway Two-Seven, downwind" |
| Base | "NAIL Two-One, base" |
| Final | "NAIL Two-One, final Runway Two-Seven" |

### Overhead Break (Military Pattern)

Military aircraft typically enter via **overhead break**:

1. Fly over field at **1,000 ft AGL** at **350+ kts**
2. At mid-field — **pitchout:** hard turn (3–5G) to downwind
3. Configure: gear, flaps on downwind
4. Roll out on final: **1.5 NM** from threshold
5. Speed on final: **150–160 kts**

```
PILOT: "Batumi Tower, NAIL Two-One, 
        two-ship for the break"
TOWER: "NAIL Two-One, Batumi Tower, 
        runway Two-Seven, winds, 
        cleared for the break"
PILOT: "Cleared break Two-Seven, NAIL Two-One"
```

---

## Hot Pit / FARP Operations

### FARP (Forward Arming and Refueling Point)

Used for rapid turnaround in combat operations:

#### FARP Arrival
1. Contact FARP on assigned frequency
2. Request: `"FARP, NAIL Two-One, inbound for fuel and rearm"`
3. Follow FARP handler instructions
4. **Hot refuel** — engine may remain running
5. Confirm new fuel load and ordnance before departure

#### Hot Refuel Checklist
- [ ] **Master Arm** — SAFE
- [ ] **All weapons** — safed
- [ ] **Radio** — announce "HOT" on FARP frequency
- [ ] Engines — **IDLE** or **OFF** per FARP SOP
- [ ] Ground crew connect fuel
- [ ] **Do not transmit on HF** during fueling (spark risk)

#### After Rearming
- [ ] Confirm new loadout with ground crew
- [ ] **Walk-around** (if time permits)
- [ ] **Resume startup** per aircraft checklist

---

## IFR Procedures

### IFR Flight Plan
For IFR operations, file:
- Departure — Destination
- Route (airways or direct)
- Altitude
- Speed
- Time en route

### IFR Separation
- Vertical: 1,000 ft below FL290 / 2,000 ft above
- Lateral: radar separation as provided by ATC

### Lost Communications (IFR)
See [Communication Failure](#communication-failure) section.

---

## Communication Failure

### Radio Failure in Flight (IFR)

#### Squawk 7600
Set transponder code 7600 to alert ATC.

#### NORDO Procedures (No Radio)
1. Continue flight plan as filed
2. Maintain filed altitude
3. At destination: arrive at filed ETA
4. Fly approach at filed time
5. Land on active runway
6. Taxiway: follow light signals from tower

### Tower Light Signals

| Signal | Ground | Airborne |
|---|---|---|
| Steady GREEN | Cleared to taxi | Cleared to land |
| Flashing GREEN | Cleared to taxi | Cleared to return and land |
| Steady RED | Stop | Give way, continue circling |
| Flashing RED | Taxi clear of runway | Unsafe, do not land |
| Flashing WHITE | Return to start | — |
| Alternating R/G | General warning | General warning |

---

## DCS ATC Operations

### DCS ATC Radio Menu Usage

Press `\` to open communications menu:

```
\ → [1] ATC → [1] Tbilisi → [1] Request Start
                             [2] Request Taxi  
                             [3] Request Takeoff
                             [4] Request Landing
                             [5] Report Final
```

### DCS ATC Limitations
- AI ATC responds to preset menu options
- Does not understand free-text
- Frequencies may not match perfectly with radio settings
- Always set radio to correct freq even if using menu

### Getting Landing Clearance
```
\  [Radio menu]
→ ATC
→ [Field name]
→ Request Landing
```

### Getting Takeoff Clearance
```
\  [Radio menu]
→ ATC
→ [Field name]
→ Request Takeoff
```

---

## Airfield Quick Reference Cards

### Departure Quick Reference
```
╔═══════════════════════════════════╗
║   DEPARTURE SEQUENCE              ║
╠═══════════════════════════════════╣
║ 1. ATIS — copy info letter        ║
║ 2. Ground — request taxi          ║
║ 3. Taxi to runway hold short      ║
║ 4. Tower — ready for departure    ║
║ 5. Tower clears for takeoff       ║
║ 6. Takeoff                        ║
║ 7. Departure — check in           ║
║ 8. En route                       ║
╚═══════════════════════════════════╝
```

### Arrival Quick Reference
```
╔═══════════════════════════════════╗
║   ARRIVAL SEQUENCE                ║
╠═══════════════════════════════════╣
║ 1. ATIS — copy info letter        ║
║ 2. Approach — check in (50 NM)    ║
║ 3. Descend per ATC                ║
║ 4. ILS/approach clearance         ║
║ 5. Tower — report final/contact   ║
║ 6. Cleared to land                ║
║ 7. Land                           ║
║ 8. Ground — taxi to ramp          ║
╚═══════════════════════════════════╝
```

### Overhead Break Quick Reference
```
╔═══════════════════════════════════╗
║   OVERHEAD BREAK PATTERN          ║
╠═══════════════════════════════════╣
║ 1. 1,000 ft AGL, 350 kts          ║
║ 2. Call "two-ship for the break"  ║
║ 3. Tower clears break             ║
║ 4. Pitchout at mid-field          ║
║ 5. Downwind: gear, flaps          ║
║ 6. Base turn: stabilize           ║
║ 7. Final: 150 kts, confirm gear   ║
║ 8. Land                           ║
╚═══════════════════════════════════╝
```

### ILS Approach Quick Reference
```
╔═══════════════════════════════════╗
║   ILS APPROACH CHECKLIST          ║
╠═══════════════════════════════════╣
║ □ ILS freq set + ident confirmed  ║
║ □ Approach course set             ║
║ □ Altimeter set (QNH)             ║
║ □ Gear DOWN by 10 NM              ║
║ □ Flaps landing                   ║
║ □ Intercept localizer             ║
║ □ Intercept glide slope (3°)      ║
║ □ Descend 500 fpm                 ║
║ □ At DH: runway in sight → land   ║
║ □ At DH: no runway → go around    ║
╚═══════════════════════════════════╝
```

---

## Cross-References
- [9-Line CAS Procedures →](9-line-cas.md)
- [Radio Communications →](radio-communications.md)
- [NS430 Approach Procedures →](../aircraft/ns430.md#approach--ils)
- [A-10C Navigation →](../aircraft/a-10c.md#navigation-cdupegi)
- [Back to Index →](../index.md)

---

*Based on ICAO, FAA, and NATO ATC procedures. For simulation use only.*
