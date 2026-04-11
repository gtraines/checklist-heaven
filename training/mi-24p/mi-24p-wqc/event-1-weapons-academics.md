# Event 1 — Weapons Systems Academics

> **Course:** Mi-24P Hind Weapons Qualification Course | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Weapons Inventory](#weapons-inventory)
3. [Pylon Station Configuration](#pylon-station-configuration)
4. [WSO Front Cockpit — Weapons Panel](#wso-front-cockpit--weapons-panel)
5. [Pilot Rear Cockpit — Weapons Controls](#pilot-rear-cockpit--weapons-controls)
6. [Arming & Safe Procedures](#arming--safe-procedures)
7. [Emergency Stores Jettison](#emergency-stores-jettison)
8. [DCS Key Bindings & HOTAS Configuration](#dcs-key-bindings--hotas-configuration)
9. [Standard Loadout Configurations](#standard-loadout-configurations)
10. [Crew Coordination Standards](#crew-coordination-standards)
11. [Common Errors](#common-errors)
12. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Identify all weapons available in DCS Mi-24P module, their warhead types, and employment ranges
- [ ] Locate and operate Master Arm and Weapon Selector controls in both cockpits
- [ ] Execute the correct weapons arming sequence and post-engagement safe sequence
- [ ] Execute total and selective emergency stores jettison procedures
- [ ] Describe pylon station numbering, loading restrictions, and store compatibility rules
- [ ] Configure DCS key bindings for efficient weapons employment
- [ ] Select correct loadout configuration for a given mission type
- [ ] Apply single-player seat-switching workflow without losing aircraft control
- [ ] Demonstrate multi-crew coordination calls for weapons employment

---

## Weapons Inventory

The Mi-24P carries a broad mix of fixed-forward cannon, guided missiles, unguided rockets, and air-to-air missiles. The DCS Mi-24P module includes the following weapons:

| Weapon System | NATO Designation | Type | Max Range | Warhead | Delivery | Max Carried |
|---|---|---|---|---|---|---|
| **GSh-30K** | — | Twin-barrel 30 mm cannon | 1,500 m effective | APHE / HE-Frag (mixed belt) | Pilot-fired, fixed forward | 250 rounds |
| **9M114 Shturm** | AT-6 Spiral | Radio-command ATGM | 5,000 m | HEAT (600+ mm RHAe) | WSO SACLOS guidance | 4 missiles |
| **9M120 Ataka** | AT-9 Spiral-2 | Radio-command ATGM | 6,000 m | HEAT (800+ mm) / Thermobaric | WSO SACLOS guidance | 4 missiles |
| **S-5** | — | 57 mm unguided rocket | 1,800 m effective | HE-Frag / HEAT / Flechette | Pods: UB-16 (16-rnd), UB-32 (32-rnd) | 128 rockets (4×UB-32) |
| **S-8** | — | 80 mm unguided rocket | 2,000 m effective | HE-Frag / HEAT / Thermobaric | Pods: B-8V20A (20-rnd) | 80 rockets (4 pods) |
| **S-13** | — | 122 mm unguided rocket | 2,500 m effective | HE-Frag / Penetrator | Pods: B-13L (5-rnd) | 20 rockets (4 pods) |
| **S-24** | — | 240 mm heavy rocket | 4,000 m effective | HE blast-fragmentation (123 kg warhead) | APU-68UM single rail | 4 rockets |
| **FAB-100/250/500** | — | General purpose bombs | Altitude-dependent | 45 / 97 / 200 kg HE blast | Gravity release | Variable (pylon-dependent) |
| **KMGU-2** | — | Submunitions dispenser | Altitude-dependent | AO-2.5RT frag / PTAB-2.5M HEAT | Cluster dispense | 4 dispensers |
| **RBK-250/500** | — | Cluster bombs | Altitude-dependent | Submunitions (anti-personnel / anti-armor) | Gravity release | Variable |
| **R-60** | AA-8 Aphid | IR air-to-air missile | 5,000 m effective | 3 kg HE-Frag | Fire-and-forget IR | 4 missiles |
| **R-73** | AA-11 Archer | IR air-to-air missile | 15,000 m effective | 7.4 kg HE-Frag | Fire-and-forget IR | 4 missiles |

> **Version Note:** Weapon availability in the DCS Mission Editor may vary by module version. Verify available stores in the loadout screen for your specific installation. FAB bombs, KMGU-2, and cluster munitions may require specific module versions or theater packs.

### Weapon Character Summary

Understanding each weapon's core character prevents target mismatches:

| Weapon | Character | Strength | Limitation |
|---|---|---|---|
| **GSh-30K** | Short-range, high rate of fire, pilot-aimed | Volume of fire, always available | Minimum range 400 m; fixed mount — pilot aims the aircraft |
| **Shturm** | Long-range, precision, SACLOS-guided | Penetrates all armor at 5 km standoff | 15-sec flight time; must hold steady throughout |
| **Ataka** | Extended-range, dual-warhead, SACLOS | Thermobaric variant for bunkers/infantry | More expensive, same guidance limitations as Shturm |
| **S-5** | Area saturation, mass fire | Cheapest area effect, high volume | Short range; poor accuracy at individual targets |
| **S-8** | Versatile, moderate range, CCIP | Accurate in dive; suitable for mixed targets | Ballistic — no guidance after launch |
| **S-13** | Heavy penetrator | Defeats hardened shelters, bridges | Only 5 per pod; heavy recoil; requires firm dive |
| **S-24** | Maximum blast effect | Largest warhead in rotary inventory | Single rocket; heavy; manual aim only |
| **R-60** | Rear-aspect IR missile | Self-defense vs. helicopters | Short range; limited off-boresight |
| **R-73** | Advanced IR, off-boresight | All-aspect; highly capable | Helicopter-vs-fighter engagement rarely favorable |

---

## Pylon Station Configuration

The Mi-24P has four stub-wing pylon stations — two per side (inner and outer). Each pylon uses a BD3-57KrV universal pylon adaptor that accepts Soviet-standard store interfaces.

**Station Numbering Convention (Pilot's Perspective):**

```
        LEFT SIDE               RIGHT SIDE
   ┌─────┬─────┐           ┌─────┬─────┐
   │ Stn │ Stn │  FUSELAGE │ Stn │ Stn │
   │  1  │  2  │ ═══════════│  3  │  4  │
   │outer│inner│           │inner│outer│
   └─────┴─────┘           └─────┴─────┘
```

| Station | Wing | Position | Max Weight | Compatible Stores | Primary Role |
|---|---|---|---|---|---|
| **1** | Left | Outer | 500 kg | ATGM rails, AAM rails, rocket pods, bombs, S-24 rails, KMGU | Primary ATGM / AAM |
| **2** | Left | Inner | 500 kg | Rocket pods, bombs, KMGU, PTB-450 external fuel tank | Rockets / bombs / fuel |
| **3** | Right | Inner | 500 kg | Rocket pods, bombs, KMGU, PTB-450 external fuel tank | Rockets / bombs / fuel |
| **4** | Right | Outer | 500 kg | ATGM rails, AAM rails, rocket pods, bombs, S-24 rails, KMGU | Primary ATGM / AAM |

**Station Restrictions:**
- **ATGMs and S-24:** Outer stations (1 and 4) only — APU-68UM launch rail required
- **AAMs (R-60/R-73):** Outer stations (1 and 4) only — APU-62-1M launch rail required
- **Rocket Pods (B-8V20A, B-13L, UB-16, UB-32):** All stations (1–4)
- **Bombs and KMGU:** All stations (1–4)
- **External Fuel (PTB-450):** Inner stations (2 and 3) only

> **Key Principle:** Always load symmetrically. Asymmetric loading (e.g., one outer pylon missing) causes a roll tendency requiring trim compensation. Lateral imbalance is acceptable within ±100 kg between sides.

---

## WSO Front Cockpit — Weapons Panel

The WSO (front seat — press `1` to switch) controls all weapons management from the left console and forward instrument panel.

| Control | Panel Location | Type | Positions | Function |
|---|---|---|---|---|
| **Master Arm Switch** | Left console, weapons section, upper row | Two-position toggle with guard | SAFE / ARMED | Enables all weapons firing circuits |
| **Weapon Type Selector** | Center weapons panel | 5-position rotary | OFF / CANNON / ROCKETS / ATGM / AAM | Routes fire command to selected weapon |
| **Pylon Selector** | Center weapons panel, below type selector | Multi-position rotary | 1 / 2 / 3 / 4 / ALL | Selects pylon(s) for firing |
| **ATGM Mode Switch** | ATGM sub-panel, left console | Two-position toggle | SHTURM / ATAKA | Selects SACLOS guidance algorithm |
| **Rocket Salvo Selector** | Rocket sub-panel, left console | 4-position rotary | 1 / 2 / 4 / FULL POD | Rockets per trigger pull |
| **Rocket Ripple Interval** | Rocket sub-panel | Variable knob | 0.05–0.5 sec | Delay between successive rockets in salvo |
| **Fire Button** | WSO cyclic grip, index finger | Momentary trigger | PRESS | Primary weapon release (WSO-controlled weapons) |
| **Emergency Jettison** | Emergency panel, upper left | Guarded button | LIFT GUARD + PRESS + HOLD (3 sec) | Jettisons all external stores simultaneously |
| **Selective Jettison** | Emergency panel | Momentary button | SELECT PYLON → PRESS | Jettisons stores on selected pylon only |

---

## Pilot Rear Cockpit — Weapons Controls

The Pilot (rear seat — press `2`) has limited weapons controls focused on fixed-forward firing and safety overrides.

| Control | Panel Location | Type | Positions | Function |
|---|---|---|---|---|
| **Cannon Trigger** | Pilot cyclic grip, index finger | Momentary trigger | SQUEEZE | Fires GSh-30K cannon |
| **Rocket Fire Button** | Pilot cyclic grip, thumb | Momentary button | PRESS | Fires rockets (pilot CCIP mode) |
| **Weapon Safety Override** | Pilot collective, forward-facing toggle | Two-position toggle | SAFE / FIRE | Must be FIRE for any weapon release |
| **Master Arm Indicator** | Instrument panel, weapons status cluster | Warning light | OFF / ON (armed) | Mirrors WSO Master Arm state |
| **Weapon Status Lights** | Instrument panel, right side | Indicator cluster | Per-pylon status | Loaded/empty status per station |
| **Emergency Jettison T-Handle** | Left console, guarded | Guarded T-handle | PULL | Pilot backup jettison (if WSO incapacitated) |

> **Critical:** The Pilot cannot arm or disarm the aircraft from the rear cockpit — only the WSO controls Master Arm. However, the Pilot's Weapon Safety must be in the FIRE position for *any* weapon to fire.

---

## Arming & Safe Procedures

### Pre-Flight Weapons Verification

1. **WSO Seat** (`1`):
   - Master Arm → verify **SAFE** (guard closed)
   - Weapon Type Selector → rotate all positions; no unexpected warning lights
   - Pylon Selector → positions 1–4; note which status lights are lit (loaded)
   - ATGM Mode Switch → verify matches loaded missile type (Shturm or Ataka)
   - Rocket Salvo → set to **1** (default safe setting)

2. **Pilot Seat** (`2`):
   - Weapon Safety → verify **SAFE**
   - Master Arm Indicator → verify **OFF** (dark)
   - Station status lights → confirm match to briefed loadout

3. **External View** (`F2`): Visually confirm pylons show correct stores.

### Combat Arming Sequence (Approaching Target Area)

| Step | Crew | Action |
|---|---|---|
| 1 | WSO | Master Arm guard → **OPEN** → switch to **ARMED** (both cockpits show warning light) |
| 2 | WSO | Weapon Type Selector → set to planned first weapon |
| 3 | WSO | Pylon Selector → select appropriate station(s) |
| 4 | WSO | Configure sub-system (see below) |
| 5 | Pilot | Weapon Safety → **FIRE** |
| 6 | Both | Intercom: **"Weapons hot"** |

**Sub-System Configuration (Step 4 Detail):**
- *If ATGM:* ATGM Mode → SHTURM or ATAKA as loaded; verify PKV-1 in ATGM mode
- *If Rockets:* Salvo Selector → set quantity; Ripple Interval → set timing
- *If Cannon:* No additional WSO setup; pilot ready to fire
- *If AAM:* Seeker activates automatically; WSO listen for acquisition tone

### Post-Engagement Safe Sequence

| Step | Crew | Action |
|---|---|---|
| 1 | WSO | Master Arm → **SAFE**, close guard |
| 2 | WSO | Weapon Type Selector → **OFF** |
| 3 | Pilot | Weapon Safety → **SAFE** |
| 4 | Both | Intercom: **"Weapons safe"** |
| 5 | WSO | Verify all warning lights extinguished |

---

## Emergency Stores Jettison

### Total Jettison — All Stores

**Use when:** Weight emergency, fire, engine failure, combat damage requiring immediate unloading.

1. **WSO (Primary):**
   - Master Arm → **SAFE** (prevents detonation during jettison)
   - Emergency Jettison guard → OPEN
   - Emergency Jettison button → **PRESS AND HOLD (3+ seconds)**
2. **Pilot (Backup if WSO incapacitated):**
   - Emergency Jettison T-handle → **PULL**
3. **Both:**
   - Announce **"Jettisoning stores"** on radio
   - Confirm stores clear via external view or wingman
   - WSO: Confirm all station status lights → **EMPTY**
   - Pilot: Retrim for new weight and CG

### Selective Jettison — Single Station

**Use when:** Hung store, asymmetric load, single pylon damaged.

1. WSO: Pylon Selector → target station number (1, 2, 3, or 4)
2. WSO: Selective Jettison button → **PRESS** (brief press)
3. WSO: Verify selected station light → **EMPTY**
4. WSO: Verify adjacent stations still lit (no unintended jettison)
5. Pilot: Retrim as needed

### Jettison Priority (Emergency Performance)

| Priority | Jettison First | Reason |
|---|---|---|
| 1st | S-24 rockets (235 kg each) | Heaviest individual items |
| 2nd | B-13L pods (435 kg each) | Heavy rocket pods |
| 3rd | FAB-500 bombs | Largest ordnance |
| 4th | B-8V20A pods (252 kg each) | Standard rocket pods |
| Last | ATGM / AAM rails | Retain self-defense capability if possible |

---

## DCS Key Bindings & HOTAS Configuration

### Default Key Bindings

| Function | Default Key | Notes |
|---|---|---|
| **Master Arm Toggle** | `O` | Toggles SAFE / ARMED |
| **Fire Weapon (Primary)** | `Space` | Fires selected weapon |
| **Weapon Select Next** | `D` | Cycles weapon type |
| **Weapon Select Previous** | `LShift + D` | Reverse cycle |
| **Emergency Jettison** | `LAlt + J` | Jettisons all stores |
| **Single Chaff** | `Delete` | One chaff cartridge |
| **Single Flare** | `Insert` | One flare cartridge |
| **Countermeasures Program** | `Q` | Runs active CM program |
| **Seat → WSO (Front)** | `1` | Switches to front cockpit |
| **Seat → Pilot (Rear)** | `2` | Switches to rear cockpit |
| **External View** | `F2` | Loadout verification |
| **PKV-1 Zoom In** | `Numpad +` | Increase magnification |
| **PKV-1 Zoom Out** | `Numpad -` | Decrease magnification |

### Recommended HOTAS Bindings

| HOTAS Control | Binding | Reason |
|---|---|---|
| **Trigger** | Cannon fire / weapon release | Primary fire — always accessible |
| **Thumb Button** | Weapon select next | Rapid weapon cycling |
| **Coolie Hat** | PKV-1 sight slew (4-way) | Target tracking without hands off stick |
| **Paddle Switch** | Master Arm toggle | Quick arm/safe |
| **TMS Up / Down** | PKV-1 zoom in / zoom out | Magnification control |
| **DMS Right / Left** | Pylon select next / previous | Station cycling |
| **CMS Dispense** | Countermeasures program | Immediate CM employment |

---

## Standard Loadout Configurations

| Mission Type | Stn 1 (L Outer) | Stn 2 (L Inner) | Stn 3 (R Inner) | Stn 4 (R Outer) | Stores Weight |
|---|---|---|---|---|---|
| **Anti-Armor** | 2×Ataka (84 kg) | B-8V20A (252 kg) | B-8V20A (252 kg) | 2×Ataka (84 kg) | 672 kg |
| **Close Support** | B-8V20A (252 kg) | B-8V20A (252 kg) | B-8V20A (252 kg) | B-8V20A (252 kg) | 1,008 kg |
| **Heavy Strike** | S-24 (235 kg) | B-13L (435 kg) | B-13L (435 kg) | S-24 (235 kg) | 1,340 kg |
| **Self-Defense Mix** | 2×Ataka (84 kg) | B-8V20A (252 kg) | B-8V20A (252 kg) | 2×R-60 (87 kg) | 675 kg |
| **Standoff ATGM** | 2×Ataka (84 kg) | — | — | 2×Ataka (84 kg) | 168 kg |
| **Light Recon** | — | B-8V20A (252 kg) | B-8V20A (252 kg) | — | 504 kg |

**Loadout Selection Factors:**
- **Threat Environment:** High AAA/SAM density → maximize standoff with ATGM; low threat → rockets for volume
- **Target Type:** Armor → ATGM + HEAT rockets; soft targets → HE-Frag rockets + cannon; structures → S-13 / S-24 / FAB
- **Air Threat:** Add R-60 or R-73 on one outer station if enemy helicopter/fixed-wing activity expected
- **Gross Weight:** Heavy loadouts reduce hover ceiling and VNE — see Event 8 for weight/performance planning

---

## Crew Coordination Standards

### Single-Player Seat-Switching Workflow

The student must internalize this workflow before any live-fire events. **Never switch seats during active SACLOS guidance** — the missile will fly ballistic.

| Phase | Seat | Key Actions |
|---|---|---|
| **Pre-flight / Arming** | WSO (`1`) | Arm weapons, verify loadout, configure type/salvo/mode |
| **Takeoff / Transit** | Pilot (`2`) | Fly aircraft, navigate to area of operations |
| **Target area approach** | WSO (`1`) | Power up PKV-1, scan for targets, acquire |
| **ATGM engagement** | WSO (`1`) | Launch, guide missile to impact — **do not switch seats** |
| **Cannon / rocket attack** | Pilot (`2`) | Maneuver aircraft, CCIP delivery, fire fixed weapons |
| **Post-attack BDA** | WSO (`1`) | Assess damage, select next weapon |
| **Threat detected** | WSO (`1`) | Dispense CM, call threat direction, advise evasion |
| **Egress** | Pilot (`2`) | Break maneuver, evasion, navigate home |

**Rule:** Engage autopilot (heading + altitude hold) before switching seats. The aircraft will hold approximately steady during the transition.

### Multi-Crew Coordination Calls

| Situation | Pilot Call | WSO Call |
|---|---|---|
| **Arming** | "Weapons safe, standing by" | "Arming up — weapons hot" |
| **Target ID** | "Tally" or "No joy" | "Target, [type], [bearing], [range]" |
| **Ready to fire** | "Steady, cleared to engage" | "Ready to fire [weapon]" |
| **Firing** | (Hold steady) | "Firing" / "Missile away, guiding" |
| **Impact** | "Breaking [direction]" | "Splash" / "Miss, [direction]" |
| **Threat** | "Maneuvering [direction]" | "Threat, [type], [bearing]" |
| **Abort** | "Aborting, egressing [direction]" | "Weapons safe" |

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| **Forgetting Master Arm** | Weapons will not fire | Verify armed and warning light ON before every attack |
| **Wrong weapon type selected** | Fires wrong weapon or nothing fires | Cross-check selector AND pylon before each shot |
| **Incorrect salvo setting** | Wastes ammunition | Set salvo BEFORE entering attack profile |
| **Switching seats during ATGM guidance** | Missile goes ballistic | Stay in WSO seat for entire guidance phase |
| **Premature weapons safe** | Cannot re-engage quickly | Keep armed until all targets neutralized or egressing |
| **Pilot Safety on SAFE** | Trigger input ignored | Pilot: verify Weapon Safety → FIRE during arming sequence |
| **Wrong ATGM mode** | Guidance mismatch with loaded missile | Cross-check ATGM mode (Shturm/Ataka) matches physical load |
| **Not verifying loadout** | Wrong stores in combat | Always verify via external view AND status lights |

---

## Completion Standards

The student must demonstrate the following without reference to notes before proceeding to Event 2:

- [ ] Locate and identify all weapons panel controls in both WSO and Pilot cockpits without prompting
- [ ] Recite all weapons in the Mi-24P inventory with correct warhead type and effective range
- [ ] Execute the combat arming sequence in correct order from memory
- [ ] Execute the post-engagement safe sequence in correct order from memory
- [ ] Describe total jettison and selective jettison procedures including correct T-handle usage
- [ ] State correct pylon assignment rules (which stores go on which stations)
- [ ] Describe the single-player seat-switching workflow and state the rule for ATGM guidance
- [ ] Make correct crew coordination calls for a simulated target engagement

---

*Based on DCS World Mi-24P Hind module by Eagle Dynamics and Mi-24P RLE (Rukovodstvo po Letnoy Ekspluatatsii). For simulation use only.*
