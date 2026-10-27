# A-10A Reference Manual Research — DCS FC3 A-10A Flight Manual

**Source:** `reference/A-10A Flight Manual EN.pdf` — Eagle Dynamics DCS World [A-10A: DCS Flaming Cliffs], 104 pages, ©2013 The Fighter Collection / Eagle Dynamics

## Critical Note
This reference is the **DCS Flaming Cliffs 3 game manual**, not the real USAF Technical Order (T.O. 1A-10A-1 / AFMAN 11-2A-10 Vol 3). It contains:
- Cockpit instrument descriptions
- Game-mode (simplified "Game" avionics vs. realistic mode) description
- Weapon employment procedures specific to DCS FC3
- Radio communications (DCS menu-based)
- Combat maneuver theory

It does **NOT** contain:
- MTOW / Max landing weight
- G-limits (clean or loaded)
- V-speeds (Vr, V2, Vmca, Vref)
- EGT / ITT limits for start, continuous, transient
- N1/N2 limits
- Crosswind / tailwind limits
- Traffic pattern speeds/altitudes

**Implication:** All performance/limitation data in `a-10a.md` (Operating Limitations and Performance & V-Speeds sections) cannot be verified or falsified against this reference. Those values appear sourced from the real T.O. 1A-10A-1.

---

## Extracted Facts — What the Manual Does State

### Flap Extension Speed (p. 28)
> "Flaps will not extend or auto-retract if the airspeed exceeds **185 to 219 KIAS** depending on altitude."

- Flap positions mentioned: MVR (for takeoff)
- The range 185–219 KIAS is altitude-dependent (lower limit at low altitude, higher limit at altitude)

### AoA Indicator (p. 39)
> "For landing, the range of AoA is marked between **15 and 21 units**."

### AoA Indexer (p. 39)
- Upper indicator lit = AoA too large / airspeed too low (slow)
- Lower indicator lit = AoA too small / airspeed too fast (fast)
- Central indicator = correct landing AoA
- Combined central + upper/lower = slightly off

### Oil Pressure Warning (p. 42)
> "If the oil pressure drops lower than **27.5 units**, the warning lamp on the caution panel will light."
- Units unclear (may not be PSI)

### AGM-65D Range (p. 58)
> "launch range against vehicle targets approaching **6 nm**"
- The AGM-65B (TV) has shorter range than D (IIR)
- The manual covers AGM-65K and AGM-65D only (not G variant)
- Manual does not list AGM-65G

### AGM-65 Seeker Gimbal Limits (p. 54)
> "The seeker's gimbal limits are in width **±60 degrees**. For launch however, it is necessary that the target be within **±30 degrees**."

### GAU-8/A Cannon (p. 95 employment checklist)
> "A small gun cross is located at the top of the HUD. At a distance of **more than 2.5 miles** this cross-hair is crossed out by an 'X' symbol. At a distance less than 2.5 miles, the range to ground is displayed under the cross-hair."

Effective range statement (p. 93, air-to-air gun section, by implication for A2G):
> "Effective fire is generally **below 800 meters**." (stated in air-to-air context; A2G is similar)

### AIM-9 Lock Range (p. 93)
> "Lock range depends on target IR-signature and can vary from **.1 to 10 miles**."

---

## Values NOT Found in This Manual
The following checklist values have no corresponding data in this reference:
- MTOW (~50,000 lbs)
- Max Landing Weight (~42,000 lbs rec / 46,000 lbs structural)
- G-limits (+7.33/−3.0 clean; +5.86 loaded)
- V-speeds (Vr, V2, Vmca, Vref by weight)
- EGT limits (725°C start, 650°C continuous, 690°C transient)
- N2 max (100%)
- Crosswind limits (25 kts demonstrated, 15 kts wet)
- Best glide (200 KIAS / 8–10:1)
- Glide range estimates (13–17 NM from 10,000 ft)
- Pattern altitudes (1,500 ft AGL)
- Traffic pattern speeds
