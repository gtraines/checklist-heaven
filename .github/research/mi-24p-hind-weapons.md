# Research Dossier: Mi-24P Hind — Weapons Qualification Course (WQC)

**Source Material Priority:**
1. **Primary (Simulation Truth):** Official DCS Mi-24P Eagle Dynamics module documentation and actual in-game behavior
2. **Secondary (Realism Context):** Real-world Soviet/Russian military documentation — Mi-24P RLE, Technical Description, 9M114/9M120 System Manuals, Soviet VVS weapons employment circulars
3. **Conflict Resolution:** DCS procedure documented as primary instruction; real-world divergences noted as *⚠ Realism Divergence*

**Aircraft Summary:** DCS Mi-24P is a full-fidelity, dual-seat, clickable-cockpit attack helicopter module. Crew division: Pilot (rear cockpit) flies aircraft and fires fixed-forward weapons; WSO (front cockpit) operates PKV-1 sight, manages ATGM SACLOS guidance, selects weapons. No FLIR targeting pod — visual/optical engagement only. All systems metric (Soviet convention): km/h, meters, °C, kg.

---

## Module 1: Weapons Systems Overview & Cockpit Switchology

### Learning Objectives
- Identify all weapons available in DCS Mi-24P module and their employment parameters
- Locate and operate master arm and weapon selector controls in both cockpits
- Execute proper weapons arming/safe sequence for each weapon type
- Demonstrate salvo/ripple fire controls for rockets and multiple ATGM employment
- Perform emergency stores jettison procedure
- Apply correct crew coordination procedures for weapons employment
- Configure DCS keyboard bindings for efficient weapons employment
- Describe the pylon station numbering convention and weapon-to-station compatibility rules

### DCS Mi-24P Weapons Inventory

| Weapon System | NATO Designation | Type | Caliber | Max Range | Warhead | Delivery | Max Carried |
|---|---|---|---|---|---|---|---|
| **GSh-30K** | — | Twin-barrel cannon | 30 mm | 1,500 m effective | APHE / HE-Frag (mixed belt) | Pilot-fired, fixed forward | 250 rounds |
| **9M114 Shturm** | AT-6 Spiral | Radio-command ATGM | 130 mm | 5,000 m | HEAT (600+ mm RHA) | WSO SACLOS guidance | 4 missiles |
| **9M120 Ataka** | AT-9 Spiral-2 | Radio-command ATGM | 130 mm | 6,000 m | HEAT (800+ mm) / Thermobaric | WSO SACLOS guidance | 4 missiles |
| **S-5** | — | Unguided rocket | 57 mm | 1,800 m effective | HE-Frag / HEAT | Pods: UB-16 (16-rnd) or UB-32 (32-rnd) | 128 rockets (4×UB-32) |
| **S-8** | — | Unguided rocket | 80 mm | 4,000 m | HE-Frag / HEAT / Thermobaric | Pods: B-8V20A (20-rnd) | 80 rockets (4 pods) |
| **S-13** | — | Unguided rocket | 122 mm | 4,500 m | HE-Frag / Penetrator | Pods: B-13L (5-rnd) | 20 rockets (4 pods) |
| **S-24** | — | Heavy unguided rocket | 240 mm | 6,000 m | HE blast-fragmentation (123 kg) | APU-68UM single rail | 4 rockets |
| **R-60** | AA-8 Aphid | IR air-to-air missile | — | 8,000 m (5,000 m effective) | 3 kg HE-Frag | Fire-and-forget IR | 4 missiles |
| **R-73** | AA-11 Archer | IR air-to-air missile | — | 30,000 m (15,000 m effective) | 7.4 kg HE-Frag | Fire-and-forget IR | 4 missiles |
| **FAB-100** | — | General purpose bomb | — | Altitude-dependent | 45 kg HE blast | Gravity release | Variable (pylon-dependent) |
| **FAB-250** | — | General purpose bomb | — | Altitude-dependent | 97 kg HE blast | Gravity release | Variable |
| **FAB-500** | — | General purpose bomb | — | Altitude-dependent | 200 kg HE blast | Gravity release | Variable |
| **KMGU-2** | — | Submunitions dispenser | — | Altitude-dependent | AO-2.5RT frag / PTAB-2.5M HEAT | Cluster dispense | 4 dispensers |
| **RBK-250** | — | Cluster bomb | — | Altitude-dependent | Submunitions (anti-personnel/anti-armor) | Gravity release | Variable |
| **RBK-500** | — | Cluster bomb | — | Altitude-dependent | Submunitions (area denial) | Gravity release | Variable |

*⚠ Realism Divergence: DCS Mi-24P weapon options in the mission editor may vary by game version and module updates. Verify available stores in the DCS Mission Editor loadout screen for the specific version you are running. Not all listed munitions may be selectable.*

### Pylon Station Configuration

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
| **1** | Left | Outer | 500 kg | ATGM rails, AAM rails, rocket pods, bombs, S-24 rails, KMGU | Primary ATGM / AAM station |
| **2** | Left | Inner | 500 kg | Rocket pods, bombs, KMGU, PTB-450 external fuel tank | Rockets / bombs / fuel |
| **3** | Right | Inner | 500 kg | Rocket pods, bombs, KMGU, PTB-450 external fuel tank | Rockets / bombs / fuel |
| **4** | Right | Outer | 500 kg | ATGM rails, AAM rails, rocket pods, bombs, S-24 rails, KMGU | Primary ATGM / AAM station |

**Station-Specific Restrictions:**
- **ATGMs (Shturm/Ataka):** Outer stations (1 and 4) only — APU-68UM launch rail required
- **AAMs (R-60/R-73):** Outer stations (1 and 4) only — APU-62-1M launch rail required
- **S-24 Heavy Rockets:** Outer stations (1 and 4) only — APU-68UM rail required
- **Rocket Pods (B-8V20A, B-13L, UB-16/32):** All stations (1–4)
- **Bombs (FAB, RBK):** All stations (1–4)
- **KMGU Dispensers:** All stations (1–4)
- **External Fuel (PTB-450):** Inner stations (2 and 3) only

*⚠ Realism Divergence: Real Mi-24P outer pylons use dedicated APU-68UM rails with specific wiring for ATGM guidance; DCS allows greater mixing flexibility in the loadout screen than real-world ground crew could configure in the field. Inner stations on the real aircraft have no ATGM wiring harness.*

### WSO Front Cockpit — Weapons Panel

The WSO (front seat — press `1` to switch in single-player) controls the primary weapons management panel located on the left console and forward instrument panel.

| Control | Panel Location | Physical Type | Positions / Range | Function |
|---|---|---|---|---|
| **Master Arm Switch** | Left console, weapons section, upper row | Two-position toggle with guard | SAFE / ARMED | Enables/disables all weapons firing circuits |
| **Weapon Type Selector** | Center weapons panel, rotary switch | 5-position rotary | OFF / CANNON / ROCKETS / ATGM / AAM | Routes fire command to selected weapon group |
| **Pylon Selector** | Center weapons panel, below type selector | Multi-position rotary | 1 / 2 / 3 / 4 / ALL | Selects individual pylon or all for firing |
| **ATGM Mode Switch** | ATGM sub-panel, left console | Two-position toggle | SHTURM / ATAKA | Selects guidance algorithm for missile type |
| **Rocket Salvo Selector** | Rocket sub-panel, left console | 4-position rotary | 1 / 2 / 4 / FULL POD | Number of rockets per trigger pull |
| **Rocket Ripple Interval** | Rocket sub-panel, left console | Variable knob | 0.05–0.5 sec | Time delay between successive rockets in salvo |
| **Fire Button** | WSO cyclic grip, index finger | Momentary trigger | PRESS | Primary weapon release for WSO-controlled weapons |
| **Emergency Jettison** | Emergency panel, upper left | Guarded button | LIFT GUARD + PRESS + HOLD (3 sec) | Jettisons all external stores simultaneously |
| **Selective Jettison** | Emergency panel, next to pylon selector | Momentary button | SELECT PYLON → PRESS | Jettisons stores on selected pylon only |

### Pilot Rear Cockpit — Weapons Controls

The Pilot (rear seat — press `2` to switch in single-player) has limited weapons controls focused on fixed-forward weapons (cannon, rockets) and safety overrides.

| Control | Panel Location | Physical Type | Positions | Function |
|---|---|---|---|---|
| **Cannon Trigger** | Pilot cyclic grip, index finger | Momentary trigger | SQUEEZE | Fires GSh-30K cannon |
| **Rocket Fire Button** | Pilot cyclic grip, thumb button | Momentary button | PRESS | Fires rockets in pilot CCIP mode |
| **Weapon Safety Override** | Pilot collective, forward-facing toggle | Two-position toggle | SAFE / FIRE | Pilot-accessible safety override; must be FIRE for any weapon release |
| **Master Arm Indicator** | Instrument panel, weapons status cluster | Warning light | OFF (safe) / ON (armed) | Mirrors WSO Master Arm state; pilot cannot arm/disarm |
| **Weapon Status Lights** | Instrument panel, right side | Cluster of indicator lights | Per-pylon status | Indicates loaded/empty status for each station |
| **Emergency Jettison Handle** | Left console, guarded | Guarded T-handle | PULL | Pilot emergency jettison backup (if WSO incapacitated) |

*⚠ Realism Divergence: On the real Mi-24P, the pilot has a dedicated emergency jettison T-handle as a dual-action backup requiring both crew members to act simultaneously. DCS models single-crew jettison from either cockpit for gameplay practicality.*

### Master Arm Sequence — Step-by-Step DCS Procedures

#### 1. Pre-Flight Weapons Verification

1. **WSO Seat** (`1`):
   - Master Arm → verify SAFE (guard closed)
   - Weapon Type Selector → rotate through all positions, verify no warning lights
   - Pylon Selector → rotate through stations 1–4, note loaded indicators
   - ATGM Mode → verify matches loaded missile type (Shturm or Ataka)
   - Rocket Salvo → set to 1 (default safe setting)
2. **Pilot Seat** (`2`):
   - Weapon Safety → verify SAFE
   - Master Arm Indicator → verify OFF (dark)
   - Check weapon status lights correspond to briefed loadout
3. **External View** (`F2`):
   - Visual check that pylons display correct stores
   - Confirm loadout matches DCS Mission Editor selection

#### 2. Combat Arming Sequence (Approaching Target Area)

1. **WSO:** Master Arm switch guard → OPEN → switch to ARMED
   - Master Arm warning light illuminates (both cockpits)
2. **WSO:** Weapon Type Selector → set to planned first weapon (e.g., ATGM)
3. **WSO:** Pylon Selector → select appropriate station(s)
4. **WSO:** Configure sub-system:
   - *If ATGM:* ATGM Mode → SHTURM or ATAKA as loaded
   - *If Rockets:* Salvo Selector → set quantity; Ripple Interval → set timing
   - *If Cannon:* No additional WSO setup (pilot-fired)
   - *If AAM:* Seeker power activates automatically with weapon selection
5. **Pilot:** Weapon Safety → FIRE
6. **Both:** Intercom call: **"Weapons hot"**

#### 3. Post-Engagement Safe Sequence

1. **WSO:** Master Arm → SAFE, close guard
2. **WSO:** Weapon Type Selector → OFF
3. **Pilot:** Weapon Safety → SAFE
4. **Both:** Intercom call: **"Weapons safe"**
5. **WSO:** Verify all warning lights extinguished

### Emergency Stores Jettison Procedures

#### Emergency Jettison — All Stores

**Conditions:** Aircraft emergency requiring immediate weight reduction; combat damage; engine failure; fire.

1. **WSO (Primary):**
   - Master Arm → SAFE (prevent weapon detonation on jettison)
   - Emergency Jettison guard → OPEN
   - Emergency Jettison button → PRESS and HOLD (minimum 3 seconds)
   - All four pylons release stores simultaneously
2. **Pilot (Backup):**
   - Emergency Jettison T-handle → PULL (if WSO unable)
3. **Both:**
   - Pilot: Announce **"Jettisoning stores"** on radio
   - Verify stores separation via external view or wingman confirmation
   - WSO: Confirm all station status lights show EMPTY
   - Pilot: Retrim aircraft for changed CG and reduced weight

#### Selective Jettison — Single Station

**Conditions:** Hung store, asymmetric load, combat damage to specific pylon.

1. **WSO:** Pylon Selector → select target station number (1, 2, 3, or 4)
2. **WSO:** Selective Jettison button → PRESS (brief press, <1 second)
3. **WSO:** Verify selected station status light → EMPTY
4. **WSO:** Verify adjacent stations → still loaded (no unintended jettison)
5. **Pilot:** Retrim as necessary for asymmetric load change

*⚠ Realism Divergence: Real Mi-24P emergency jettison is a dual-action safety system requiring coordinated action from both pilot and WSO simultaneously (two switches activated within 0.5 seconds). DCS simplifies this to single-crew operation from either seat for gameplay reasons.*

### DCS Keyboard / HOTAS Reference (Default Bindings)

| Function | Default Key | Category | Notes |
|---|---|---|---|
| **Master Arm Toggle** | `O` | Weapons | Toggles between SAFE and ARMED |
| **Fire Weapon (Primary)** | `Space` | Weapons | Fires currently selected weapon |
| **Fire Weapon (Alt)** | `LCtrl + Space` | Weapons | Alternative fire key |
| **Weapon Select Next** | `D` | Weapons | Cycles to next weapon type |
| **Weapon Select Previous** | `LShift + D` | Weapons | Cycles to previous weapon type |
| **Cannon Fire** | `Space` (Pilot seat) | Weapons | Fires GSh-30K from pilot position |
| **Rocket Salvo Mode** | Via cockpit click | Weapons | Click salvo selector knob in WSO cockpit |
| **Single Chaff** | `Delete` | Countermeasures | Dispenses one chaff cartridge |
| **Single Flare** | `Insert` | Countermeasures | Dispenses one flare cartridge |
| **Countermeasures Dispense** | `Q` | Countermeasures | Runs active CM program |
| **Emergency Jettison** | `LAlt + J` | Emergency | Jettisons all external stores |
| **Seat Switch → WSO** | `1` | Navigation | Switches to front (WSO) cockpit |
| **Seat Switch → Pilot** | `2` | Navigation | Switches to rear (Pilot) cockpit |
| **External View** | `F2` | View | External camera for loadout verification |
| **PKV-1 Slew (Axes)** | Assignable | Sight | Bind to HOTAS hat or ministick |
| **PKV-1 Zoom** | `+` / `-` (numpad) | Sight | Increase / decrease magnification |

**Recommended HOTAS Configuration:**
- **Trigger:** Cannon fire / weapon release
- **Thumb Button:** Weapon select next
- **Coolie Hat:** PKV-1 sight slew (up/down/left/right)
- **Paddle Switch:** Master arm toggle
- **TMS Up/Down:** Zoom in / zoom out
- **DMS Right/Left:** Pylon select next / previous
- **CMS Dispense:** Countermeasures program

### Typical Combat Loadout Configurations

| Mission Type | Station 1 (L Outer) | Station 2 (L Inner) | Station 3 (R Inner) | Station 4 (R Outer) | Cannon | Total Stores Weight |
|---|---|---|---|---|---|---|
| **Anti-Armor** | 2×Ataka (84 kg) | B-8V20A (252 kg) | B-8V20A (252 kg) | 2×Ataka (84 kg) | 250 rds | 672 kg |
| **Close Support** | B-8V20A (252 kg) | B-8V20A (252 kg) | B-8V20A (252 kg) | B-8V20A (252 kg) | 250 rds | 1,008 kg |
| **Heavy Strike** | S-24 (235 kg) | B-13L (435 kg) | B-13L (435 kg) | S-24 (235 kg) | 250 rds | 1,340 kg |
| **Self-Defense Mix** | 2×Ataka (84 kg) | B-8V20A (252 kg) | B-8V20A (252 kg) | 2×R-60 (87 kg) | 250 rds | 675 kg |
| **Light Recon** | — | B-8V20A (252 kg) | B-8V20A (252 kg) | — | 250 rds | 504 kg |
| **Bomb Delivery** | FAB-250 (250 kg) | FAB-250 (250 kg) | FAB-250 (250 kg) | FAB-250 (250 kg) | 250 rds | 1,000 kg |
| **Cluster Strike** | RBK-250 | KMGU-2 | KMGU-2 | RBK-250 | 250 rds | ~1,200 kg |
| **Maximum ATGM Standoff** | 2×Ataka (84 kg) | — | — | 2×Ataka (84 kg) | 250 rds | 168 kg |

**Loadout Selection Criteria:**
- **Threat Environment:** High AAA → maximize standoff (ATGM loadout); low threat → rockets/bombs for volume
- **Target Type:** Armor → ATGM + HEAT rockets; soft → HE-Frag rockets + cannon; structures → S-13/S-24/FAB
- **Mission Duration:** Long-range → consider PTB-450 fuel tanks on inner stations; reduce ordnance
- **Air Threat:** Add R-60 or R-73 on one outer station if enemy helicopter/air activity expected
- **Weight vs. Performance:** Heavy loadouts reduce hover ceiling, VNE, and agility — see Module 11

### Common Student Errors in Weapons Switchology

| Error | Consequence | Correction |
|---|---|---|
| Forgetting Master Arm | Weapons will not fire despite proper sight picture | Verify Master Arm ARMED before every engagement; check warning light |
| Wrong weapon type selected | Trigger pull fires wrong weapon or nothing fires | Cross-check weapon selector position AND pylon selector before each shot |
| Incorrect salvo setting | Fires too many/few rockets; wastes ammunition | Set salvo BEFORE entering attack profile; verify via cockpit click |
| Seat switching during engagement | Loses sight picture, weapon control, and guidance link | Complete entire engagement cycle from one seat; switch only between targets |
| Premature weapons safe | Cannot re-engage quickly if threat re-emerges | Keep Master Arm ARMED until all targets neutralized or egressing |
| Emergency jettison confusion | Jettisons all stores when selective jettison intended | Practice selective vs. emergency jettison; know control locations |
| Not verifying loadout | Discovers wrong stores in combat | Always verify loadout in external view and via station status lights |
| Pilot fires with Safety on SAFE | Trigger input ignored; missed engagement opportunity | Pilot verify Weapon Safety → FIRE during arming sequence |
| Forgetting ATGM mode switch | Guidance algorithm mismatch with loaded missile type | Cross-check ATGM mode (Shturm/Ataka) matches physical pylon load |

### Crew Coordination Standards

#### Single-Player Seat Switching Workflow

The single-player workflow requires disciplined seat management. **Never switch seats during active SACLOS guidance** — the missile will go ballistic.

| Phase | Seat | Actions | Key |
|---|---|---|---|
| **Pre-flight setup** | WSO (`1`) | Arm weapons, select type, configure salvo/mode | Preparation |
| **Taxi / takeoff / transit** | Pilot (`2`) | Fly aircraft, navigate to AO | Navigation |
| **Target area approach** | WSO (`1`) | PKV-1 power on, scan for targets, acquire | Acquisition |
| **ATGM engagement** | WSO (`1`) | Launch missile, guide to impact via SACLOS | **Do not switch** |
| **Cannon / rocket attack** | Pilot (`2`) | Maneuver aircraft, aim, fire fixed weapons | Direct fire |
| **Post-attack BDA** | WSO (`1`) | Assess damage through PKV-1, select next weapon | Assessment |
| **Egress** | Pilot (`2`) | Break maneuver, evasion, navigate home | Escape |

**Critical Rule:** Engage autopilot (heading + altitude hold) before switching seats during combat. The aircraft will hold approximately steady while you transition.

#### Multi-Player Crew Procedures

| Situation | Pilot Call | WSO Call | Coordination |
|---|---|---|---|
| **Arming** | "Weapons safe, standing by" | "Arming up — weapons hot" | Pilot confirms safety before WSO arms |
| **Target ID** | "Tally target" or "No joy" | "Target identified, [type] at [bearing], [range]" | WSO acquires first via PKV-1 |
| **Ready to fire** | "Steady, cleared to engage" | "Ready to fire [weapon type]" | Pilot stabilizes platform |
| **Weapon release** | (Maintain steady flight) | "Firing" / "Missile away" | Pilot holds course through guidance |
| **Impact** | "Breaking [direction]" | "Splash" / "Miss — re-engaging" | Pilot breaks only after guidance complete |
| **Threat warning** | "Maneuvering, [direction]" | "Threat, [type], [bearing]" | WSO manages countermeasures |
| **Abort** | "Aborting, egressing [direction]" | "Weapons safe" | WSO safes all weapons |

---

## Module 2: PKV-1 Sight — Operations & Target Acquisition

### Learning Objectives
- Power up and align PKV-1 gyrostabilized sight system in correct sequence
- Operate PKV-1 controls for target acquisition and weapon aiming
- Execute systematic search patterns for target acquisition
- Demonstrate visual range estimation techniques using mil-dot ranging methods
- Operate the laser rangefinder (if equipped/modeled in DCS) for accurate range data
- Identify PKV-1 sight picture for each weapon mode (cannon, rockets, ATGM)
- Apply target acquisition techniques in various lighting and weather conditions
- Conduct battle damage assessment (BDA) through PKV-1 after engagement

### PKV-1 System Architecture

| Specification | Value | Notes |
|---|---|---|
| **Type** | Collimating, gyrostabilized optical sight | Daytime optical only — no thermal/FLIR |
| **Location** | WSO front cockpit, forward of instrument panel | Periscope-style viewing head; WSO looks through eyepiece |
| **Stabilization** | Pitch and yaw gyrostabilization (dual-axis) | Compensates for aircraft movement in flight |
| **Field of View** | ~6° (narrow) / ~18° (wide) | DCS implementation may vary; narrow FOV at max zoom |
| **Magnification** | 1× to 8× (variable, continuous) | Controlled via zoom lever on sight head |
| **Reticle** | Weapon-specific graticules (illuminated) | Different patterns for cannon, rockets, ATGM, AAM |
| **Slew Limits** | ±45° azimuth, +20° / -60° elevation | Gimbal-constrained; hard stops at limits |
| **Slew Rate** | ~15°/second (manual joystick) | Faster slew possible with practice |
| **Power Source** | AC 115V, 400 Hz from main inverter | Must be powered before use; gyro spin-up required |
| **Weight** | ~35 kg (sight head assembly) | Mounted on shock-isolated pedestal |

### PKV-1 Power-On & Alignment Sequence (DCS Cockpit Procedures)

1. **Pre-Power Checks:**
   - WSO: Verify PKV-1 protective covers removed (external view)
   - WSO: Check AC inverter operating (instrument panel indicator)
   - WSO: PKV-1 power switch location — left side panel near sight head

2. **Power-On Sequence:**
   - WSO: PKV-1 Power Switch → ON
   - Wait: 2-3 minutes for gyro stabilization (gyro spin-up time)
   - WSO: Observe gyro ready light (when available)
   - WSO: Test sight elevation and azimuth movement — smooth operation

3. **Boresight Verification:**
   - Pilot: Point aircraft at known reference point 1-2 km distant
   - WSO: Center PKV-1 on same reference point
   - WSO: Verify sight and aircraft heading alignment within 2°
   - WSO: If misaligned, use boresight adjustment screws (maintenance function)

*⚠ Realism Divergence: Real PKV-1 requires 5-minute gyro warm-up and has more complex boresight procedures; DCS simplifies this to immediate availability after power-on.*

### PKV-1 Controls (WSO Front Cockpit)

| Control | Location | Function | Operation |
|---|---|---|---|
| **Power Switch** | Left side panel, upper row | ON/OFF power to sight system | Toggle up (ON) / down (OFF) |
| **Slew Joystick** | Right side of sight head | Move sight in azimuth/elevation | 4-axis analog stick; proportional rate |
| **Zoom Lever** | Left side of sight head | Variable magnification 1× to 8× | Rotary lever; clockwise = zoom in |
| **Weapon Mode Selector** | Below sight head, front face | Select reticle for weapon type | 4-position rotary (CANNON/ROCKETS/ATGM/AAM) |
| **Brightness Control** | Left side panel, below power switch | Adjust reticle illumination intensity | Rotary knob; clockwise = brighter |
| **Cage/Uncage** | Top of sight head | Lock/unlock sight to aircraft axis | Spring-loaded button; press = cage, release = uncage |
| **LRF Fire** | Sight head, left thumb | Fire laser rangefinder (if modeled) | Momentary button press |

**DCS Keyboard Bindings for PKV-1:**
| Function | Default Key | Notes |
|---|---|---|
| PKV-1 Slew Up | Numpad 8 | Bind to HOTAS hat for smoother control |
| PKV-1 Slew Down | Numpad 2 | Bind to HOTAS hat |
| PKV-1 Slew Left | Numpad 4 | Bind to HOTAS hat |
| PKV-1 Slew Right | Numpad 6 | Bind to HOTAS hat |
| PKV-1 Zoom In | Numpad + | Analog axis binding recommended |
| PKV-1 Zoom Out | Numpad - | Analog axis binding recommended |
| Weapon Mode Next | D | Cycles through PKV-1 reticle modes |

### PKV-1 Weapon Mode Reticles

| Weapon Mode | Reticle Pattern | Range Marks | Usage | Magnification Recommendation |
|---|---|---|---|---|
| **Cannon** | Cross with horizontal range bars | 500m, 1000m, 1500m marks | Pilot reference for dive attacks; WSO spot assistance | 2-4× (wide area) |
| **Rockets** | Circular mil-dot ring pattern with center pipper | Range rings at 500m intervals to 3,000m | CCIP integration when available; manual aim backup | 2-4× (target area) |
| **ATGM** | Fine crosshair with tracking box outline | No range marks (range not relevant to SACLOS) | SACLOS guidance — keep crosshair on target | 4-8× (precision tracking) |
| **AAM** | Large acquisition circle with center dot | Seeker FOV indication ring | Air-to-air target cueing — slew seeker to target | 1-2× (wide search) |

**Reticle Illumination Notes:**
- **Daytime:** Medium brightness; too bright washes out target background
- **Overcast:** Increase brightness for contrast against grey sky
- **Dusk:** Reduce brightness to preserve dark adaptation
- **Night:** PKV-1 is unusable at night (no night vision capability)

### Laser Rangefinder (LRF) System

**System Status in DCS Mi-24P:**

The real Mi-24P can be equipped with a laser rangefinder integrated into the PKV-1 sight system for accurate slant range measurement. DCS implementation may vary by module version.

| Specification | Value | Notes |
|---|---|---|
| **Type** | Pulsed laser rangefinder | Eye-safe in DCS |
| **Range** | 400m to 10,000m | Effective against cooperative targets |
| **Accuracy** | ±5m typical | Better than visual estimation |
| **Display** | Numeric range readout on PKV-1 sight / cockpit display | Shows last measured range |
| **Integration** | Feeds range to ballistic computer for CCIP | Improves rocket/cannon CCIP accuracy |
| **Pulse Rate** | Single-shot or continuous update | Single-shot conserves laser energy |

**LRF Operating Procedure (if modeled in DCS):**
1. PKV-1: Center crosshair on target
2. LRF: Press laser fire button (thumb button on sight head)
3. Range: Read displayed range value
4. Integration: CCIP pipper updates automatically with measured range
5. Employment: Fire weapon using improved CCIP solution

**LRF Employment Tips:**
- Use LRF before every engagement when time permits — measured range is always more accurate than visual estimation
- LRF works against solid objects (vehicles, structures, terrain); may fail against thin targets (antennas, wires)
- Atmospheric conditions (dust, rain, fog) reduce LRF effective range
- LRF pulse is detectable by advanced laser warning receivers — use judiciously in high-threat environments

*⚠ Realism Divergence: The real Mi-24P's rangefinder integration depends on the specific sub-variant and modification level. Some Mi-24Ps lack LRF entirely; others have the Raduga-Sh rangefinder. DCS may model this system differently from any specific real-world configuration. If LRF is not available in your DCS version, all ranging must be performed visually using the mil-dot estimation method described below.*

### Range Estimation Without Laser Rangefinder

### Target Acquisition Techniques (Visual/Optical Methods)

**Naked-Eye Acquisition First:**
- Never search through PKV-1 sight initially — too narrow field of view
- Use naked eye or binoculars to identify general target area
- Reference terrain features, buildings, roads for initial orientation
- Estimate target bearing from aircraft nose before PKV acquisition

**Visual Target Identification Cues:**
| Target Type | Visual Cues | Distance Recognition |
|---|---|---|
| **Main Battle Tanks** | Low profile, angular, track marks | 2-3 km (good visibility) |
| **APCs/IFVs** | Higher profile, wheels/tracks visible | 1.5-2.5 km |
| **Soft Vehicles** | Movement, dust clouds, reflections | 1-4 km (varies by size) |
| **Infantry** | Movement, muzzle flashes, positions | 0.5-1.5 km |
| **Structures** | Geometric shapes vs. natural terrain | 3-5 km |
| **Active AAA** | Muzzle flashes, tracer fire | 2-4 km (when firing) |

**Systematic Search Patterns:**

1. **Sector Scan (preferred for area search):**
   - Divide suspected area into 30° sectors
   - Scan each sector left-to-right, top-to-bottom
   - Spend 15-20 seconds per sector maximum
   - Use wide magnification (1-2×) initially

2. **Rapid Area Scan (time-critical):**
   - Quick left-right sweeps across suspected area
   - Look for movement, geometric shapes, color contrast
   - Switch to narrow magnification only after spotting candidate

3. **Reference Point Method:**
   - Use prominent terrain feature as reference
   - Search systematically around reference in expanding circles
   - Maintain bearing reference to aircraft heading

### Range Estimation Without Laser Rangefinder

**Mil-Dot Ranging Formula:**

*Range (meters) = Known Target Dimension (meters) × 1,000 ÷ Apparent Size (mils)*

| Vehicle Type | Length (m) | Width (m) | Height (m) | 1km Apparent Size (mils) | 2km Apparent Size (mils) |
|---|---|---|---|---|---|
| **T-72/T-80 MBT** | 9.5 | 3.6 | 2.2 | ~9.5 length / ~2.2 height | ~4.8 length / ~1.1 height |
| **BMP-2 IFV** | 7.3 | 3.2 | 2.5 | ~7.3 length / ~2.5 height | ~3.7 length / ~1.3 height |
| **BTR-80 APC** | 7.7 | 2.9 | 2.4 | ~7.7 length / ~2.4 height | ~3.9 length / ~1.2 height |
| **Truck (Ural-4320)** | 8.0 | 2.5 | 3.0 | ~8.0 length / ~3.0 height | ~4.0 length / ~1.5 height |
| **ZSU-23-4 Shilka** | 6.5 | 3.1 | 2.6 (turret) | ~6.5 length / ~2.6 height | ~3.3 length / ~1.3 height |

**Ranging Procedure (without LRF):**
1. Identify target type (determines known dimensions)
2. Set PKV-1 to 4× or higher magnification for precision
3. Compare target apparent size against reticle mil marks
4. Calculate range using formula above
5. Round to nearest 500m for weapon employment
6. Call estimated range to pilot

**Range Estimation Accuracy:**
| Method | Accuracy | Best Used For |
|---|---|---|
| **Mil-dot visual ranging** | ±200-500m at 2-4km | All weapon types when LRF unavailable |
| **LRF (if equipped)** | ±5m | Precision engagements, CCIP solutions |
| **Terrain association** | ±500-1000m | Quick estimates using known landmarks |
| **Mark-on-target** | Varies | Using map coordinates for pre-planned targets |

### PKV-1 Environmental Limitations

**Lighting Conditions:**
- **Optimal:** Bright daylight, high contrast lighting
- **Degraded:** Overcast, haze, dust, smoke in target area
- **Unusable:** Night operations (no night vision capability)
- **Sun Angle:** Avoid looking toward sun; causes sight washout

**Weather Limitations:**
- **Rain:** Degrades optics; water droplets on sight window
- **Snow:** Contrast reduction; target blending with background
- **Heat Shimmer:** Distorts sight picture at long range (>3km)
- **Dust:** Common in desert operations; blocks visibility

**Tactical Concealment vs. PKV-1:**
- **Camouflage:** Effective against optical sight; look for geometric patterns
- **Thermal Masking:** Not applicable (PKV-1 is optical, not thermal)
- **Movement:** Primary detection method; stationary targets harder to acquire
- **Defilade:** Targets in terrain shadows more difficult to identify

### Target Acquisition Sequence (Standard DCS Procedure)

1. **Initial Search:**
   - Pilot: Approach target area at 2-4 km standoff
   - WSO: PKV-1 power verified ON, weapon mode selected
   - WSO: Begin naked-eye search for target indicators

2. **PKV Acquisition:**
   - WSO: Slew PKV-1 to suspected target bearing
   - WSO: Use wide field of view initially (1-2× magnification)
   - WSO: Identify target using visual cues and range estimation
   - WSO: Call "Target acquired" to pilot with bearing and type

3. **Target Verification:**
   - WSO: Increase magnification to 4-6× for positive identification
   - WSO: Confirm target type matches briefed threat
   - WSO: Estimate range and call to pilot
   - WSO: Call "Target confirmed, ready to engage"

4. **Engagement Preparation:**
   - WSO: Select appropriate weapon for target type and range
   - WSO: Adjust magnification for engagement (varies by weapon)
   - WSO: Center target in reticle and maintain track
   - WSO: Call "Ready to fire" when stable sight picture achieved

### Battle Damage Assessment (BDA) Procedures

**Immediate Post-Shot BDA (through PKV-1):**
- WSO: Keep sight on target area after weapon impact
- WSO: Look for secondary explosions, fire, smoke
- WSO: Assess target mobility — stopped, moving, destroyed
- WSO: Call BDA to pilot: "Target destroyed/damaged/missed"

**BDA Reporting Standards:**
| BDA Call | Meaning | Indicators |
|---|---|---|
| **"Target destroyed"** | Target neutralized | Fire, explosion, no movement for 30+ seconds |
| **"Target damaged"** | Target hit but operational | Smoke, movement reduced, partial effect |
| **"Target missed"** | No hit observed | No visible effect on target |
| **"Unable to assess"** | BDA obscured | Dust, smoke, terrain masking BDA view |

### Common Student Errors with PKV-1

| Error | Consequence | Correction |
|---|---|---|
| Searching through narrow magnification | Misses targets; tunnel vision; disorientation | Always start with wide FOV (1-2×), narrow only after acquisition |
| Slewing too fast past target | Overshoots target; loses reference; wastes time | Smooth, deliberate movements; slow near suspected target area |
| Wrong weapon mode selected on PKV-1 | Incorrect reticle for engagement; wrong ballistic solution | Verify weapon mode matches selected weapon BEFORE engagement |
| Not using naked eye first | Inefficient search; wastes time searching through narrow FOV | Always acquire with naked eye/binoculars before PKV |
| Inadequate range estimation | Wrong weapon/profile selection; missed engagement | Practice mil-dot ranging; use LRF when available |
| Sun glare in sight | Cannot see target or reticle; temporary blindness | Reposition aircraft or wait for sun angle change |
| Forgetting BDA | Cannot assess engagement success; may waste ordnance | Always maintain sight picture through impact + 10 seconds |
| Not caging sight before maneuvering | Sight hits gimbal stops; loses orientation reference | Cage before aggressive maneuvering, uncage when stable |
| Ignoring sight limitations in bad weather | Fruitless searching; wasted time on station | Assess visibility conditions before committing to visual search |
| Zoom level too high during tracking | Loses target during aircraft movement; oscillation | Use 4-6× for tracking; only 8× for precision BDA |

### DCS-Specific PKV-1 Tips

**View Controls:**
- Use `RCtrl + Numpad Enter` to toggle into PKV-1 sight view (DCS default)
- Use mouse scroll to zoom when in sight view
- TrackIR/VR users: Head position must be near eyepiece to see through sight

**Known DCS Behaviors:**
- PKV-1 gyro stabilization may not be as precise as real system — expect some drift
- Sight slew rate may feel slower than expected; bind to analog axis for best control
- Weapon mode selector animation may lag behind actual mode change
- PKV-1 view in DCS renders at reduced resolution compared to external view — normal behavior
- Night missions: PKV-1 is entirely black at night; this is accurate (no night vision)

**Recommended HOTAS Bindings for PKV-1:**
| Function | Recommended Binding | Reason |
|---|---|---|
| PKV-1 Slew (4-axis) | Coolie hat or ministick | Proportional control essential for smooth tracking |
| Zoom In/Out | Analog rotary or slider | Continuous zoom better than stepped |
| Weapon Mode Cycle | Pinky or boat switch | Quick access without removing hands |
| LRF Fire | Thumb button (DMS) | One-press ranging before engagement |
| Cage/Uncage | Same hat button (long press) | Paired with slew control for efficiency |

---

## Module 3: GSh-30K 30mm Cannon Employment

### Learning Objectives
- Identify GSh-30K cannon specifications and mount limitations in DCS Mi-24P
- Execute diving strafe attack profiles with proper entry parameters
- Apply CCIP (if available) for cannon delivery accuracy
- Demonstrate burst discipline and recoil management techniques
- Select appropriate target engagement ranges for different target types
- Coordinate pilot-WSO procedures for cannon employment
- Assess cannon effectiveness against various target types

### GSh-30K System Data

| Specification | Value | Notes |
|---|---|---|
| **Full Designation** | GSh-30K (Gryazev-Shipunov 30mm twin-barrel) | Soviet designation 9A623K |
| **Mount Type** | Fixed forward, starboard fuselage pod | Non-traversing; aligned with aircraft longitudinal axis |
| **Barrel Configuration** | Twin-barrel, side-by-side | Parallel bore axes; minimal convergence |
| **Caliber** | 30×165mm | Same family as GSh-30-1 (Su-25), GSh-30-2 (BMP-2) |
| **Rate of Fire** | 2,600-3,000 RPM (combined) | ~43-50 rounds/second; high burst rate |
| **Ammunition Capacity** | 250 rounds (DCS standard load) | ~5-6 seconds continuous fire |
| **Muzzle Velocity** | 890 m/s (APHE), 900 m/s (HE-Frag) | High velocity; flat trajectory to 1,000m |
| **Effective Range** | 800m (armor penetration), 1,500m (soft targets) | Accuracy degrades beyond 1,500m |
| **Max Ballistic Range** | 4,000m | Area suppression only; no accuracy guarantee |
| **Dispersion** | ~2-3 mils (stationary), 4-6 mils (flight conditions) | DCS may model reduced dispersion |
| **Weight (loaded)** | ~390 kg total system (gun + ammo + mount) | Offset to starboard side |
| **Recoil Force** | ~5,000 N average per barrel | Produces noticeable yaw moment |

### DCS Mi-24P Ammunition Types

| Ammunition | NATO Code | Warhead | Penetration | Best Targets | DCS Notes |
|---|---|---|---|---|---|
| **3UOF8 APHE** | — | Armor-piercing HE (steel core + HE filler) | 65mm RHA at 500m, 40mm at 1,000m | Light armor, APCs, IFVs, SPAAGs | Primary anti-armor round; effective against BMP/BTR series |
| **3UOR8 HE-Frag** | — | High explosive fragmentation (pre-fragmented sleeve) | Area effect (~5m lethal radius) | Soft targets, troops, trucks, light structures | Area suppression; higher fragment count |

**Ammunition Mix and Loading:**
- DCS standard loadout: Mixed belt (~60% APHE, ~40% HE-Frag)
- Belt loading pattern: Typically alternating groups (e.g., 3 APHE, 2 HE-Frag)
- Tracer rounds: Every 5th round is a tracer for burst observation
- Player cannot select ammunition type mid-flight; mix is pre-loaded

**Penetration vs. Range:**
| Range | APHE Penetration (RHA) | Notes |
|---|---|---|
| 200m | ~80mm | Point-blank; maximum penetration |
| 500m | ~65mm | Optimal engagement range for armor |
| 1,000m | ~40mm | Marginal against IFV frontal armor |
| 1,500m | ~25mm | Effective only against thin-skinned vehicles |
| 2,000m | ~15mm | Soft targets only |

### Fixed Mount Employment Implications

**Aircraft-as-Weapon Concept:**
- Pilot aims entire helicopter — nose must point at target during engagement
- No off-boresight capability; no lateral traverse
- WSO has no control over cannon aiming (unlike rockets/ATGM)
- Requires aggressive aircraft maneuvering to achieve proper firing solution

**Firing Solution Requirements:**
- Target must be within ±2° of aircraft longitudinal axis
- Pilot must hold steady flight during burst (1-3 seconds)
- Any aircraft movement during burst spreads rounds over wider area
- Yaw control critical — pedal inputs affect accuracy significantly

### CCIP System Integration (DCS Implementation)

**CCIP Computation Factors:**
- Aircraft airspeed (groundspeed with wind correction)
- Altitude above target (radar altimeter primary)
- Dive angle (flight path vs. horizon)
- G-loading (if aircraft is maneuvering)
- Ammunition ballistics (muzzle velocity, drag)

**CCIP Display (where implemented):**
- HUD pipper shows computed impact point
- Pipper moves in real-time as aircraft parameters change
- Range-to-target displayed numerically (if modeled)
- Lead angle computed automatically for moving targets

*⚠ Realism Divergence: Real Mi-24P has limited CCIP capability compared to modern Western attack aircraft; DCS may provide more accurate CCIP than real aircraft.*

### Cannon Employment Profiles

#### 1. Diving Strafe Attack (Primary Profile)

| Parameter | Value | Rationale |
|---|---|---|
| **Entry Altitude** | 800-1,200m AGL | Clear terrain obstacles; adequate dive angle |
| **Entry Airspeed** | 220-260 km/h | Balance between stability and survivability |
| **Dive Angle** | 15-25° | Optimum accuracy vs. target exposure time |
| **Firing Range** | 800-1,200m | Maximum accuracy envelope |
| **Break-off Range** | 400-600m | AAA avoidance; terrain clearance |
| **Minimum Recovery Alt** | 100m AGL | Terrain clearance plus safety margin |
| **Burst Duration** | 1-2 seconds | Ammunition conservation; thermal limits |

**Diving Strafe Execution:**
1. **Approach:** Level flight at entry altitude, target bearing 2-4 km
2. **Roll-In:** 30-45° bank to align with target; reduce power
3. **Dive Establish:** Nose down to achieve 15-25° dive angle
4. **Target Acquisition:** Pilot acquires target through HUD/sight
5. **Firing Pass:** Steady dive, trigger squeeze at 800-1,200m
6. **Break-Off:** Pull up at 400-600m range, level off at 100m+ AGL

#### 2. Shallow Strafe Pass (Secondary Profile)

| Parameter | Value | Application |
|---|---|---|
| **Entry Altitude** | 200-400m AGL | Low-level approach; terrain masking |
| **Dive Angle** | 5-10° | Reduced target exposure |
| **Firing Range** | 1,000-1,500m | Extended range for soft targets |
| **Target Types** | Soft vehicles, troops, structures | Not effective against armor |
| **Burst Duration** | 2-3 seconds | Longer burst acceptable for area targets |

#### 3. Level Run (Emergency/Suppression Only)

| Parameter | Value | Limitations |
|---|---|---|
| **Altitude** | 50-200m AGL | Very low level; high risk |
| **Firing Range** | 1,500-2,000m | Reduced accuracy; suppression only |
| **Target Types** | Area suppression only | Not for precision engagement |
| **Burst Duration** | 3-4 seconds | Longer burst compensates for reduced accuracy |

### Cannon Effects on Aircraft Performance

**Recoil Forces (DCS Modeling):**
- **Yaw Moment:** Gun is offset to starboard — firing produces left yaw tendency
  - Counter with right pedal input during firing
  - Effect is proportional to burst length
  - DCS may under-model this compared to real aircraft
- **Pitch Effect:** Slight nose-up tendency due to mount position below CG
  - Counter with slight forward cyclic during firing
- **Deceleration:** Recoil produces ~1-2 km/h speed loss per second of firing
  - Insignificant in dive attacks; notable in level flight
- **Vibration:** Airframe vibration during firing may affect:
  - Pilot's ability to maintain precise aim (accept it; don't fight it)
  - Instrument needle fluctuation (ignore during engagement)
  - PKV-1 sight image (WSO should avoid zoomed view during pilot firing)

**Recoil Compensation Technique (Pilot):**
1. Anticipate left yaw — pre-load right pedal slightly before trigger squeeze
2. Maintain constant pedal pressure throughout burst
3. Release pedal smoothly as firing stops
4. Accept minor dispersion — do not chase aim during burst

**Thermal Limitations:**
- Barrel overheating after sustained firing (>8-10 seconds cumulative without cooling)
- Rate of fire reduction after thermal limit reached (DCS may model this)
- Minimum 10-second cooling period between extended bursts recommended
- Real-world: barrel life ~3,000 rounds; DCS does not model barrel wear

**Ammunition Conservation Strategy:**
| Situation | Budget | Burst Length | Rationale |
|---|---|---|---|
| **Single high-value target** | 40-60 rounds (1-1.5 sec) | Short, precise | One pass, conserve for re-attack |
| **Multiple soft targets** | 30-40 rounds per target (1 sec) | Short | One burst per target, move on |
| **Area suppression** | 80-100 rounds (2-3 sec) | Medium | Wider area requires longer burst |
| **Emergency self-defense** | Reserve 50-60 rounds minimum | Short | Always maintain self-defense reserve |
| **Total sortie budget** | 250 rounds = 4-6 engagements | — | Plan attacks before committing |

**Ammunition Status Awareness:**
- Track rounds fired mentally: each 1-second burst ≈ 40-50 rounds
- After 3 engagements, assume ~50% ammunition remaining
- After 5 engagements, consider RTB for rearm
- DCS ammunition counter (if modeled): check between passes

### Target Type vs. Employment Matrix

| Target Type | Recommended Profile | Range | Burst Length | Expected Effect |
|---|---|---|---|---|
| **MBT (frontal aspect)** | Steep dive, APHE rounds | 600-800m | 1-2 sec | Damage optics/tracks; unlikely kill |
| **MBT (flank/rear)** | Diving strafe | 800-1,000m | 2-3 sec | Engine/fuel fire possible |
| **Light Armor (BMP)** | Diving strafe | 800-1,200m | 1-2 sec | High kill probability |
| **APCs** | Diving/shallow | 1,000-1,500m | 1-2 sec | High kill probability |
| **Trucks/Soft Vehicles** | Shallow/level | 1,000-2,000m | 2-3 sec | Destruction likely |
| **AAA Sites** | Diving strafe | 600-1,000m | 2-3 sec | Crew suppression/equipment damage |
| **Troops in Open** | Shallow pass | 1,500-2,000m | 3-4 sec | Area suppression |
| **Bunkers/Structures** | Diving strafe | 800-1,000m | 2-4 sec | Damage; unlikely destruction |

### Cannon vs. ATGM Decision Matrix

**Use Cannon When:**
- Range < 1,500m and target is soft/light armor
- Multiple small targets in close proximity
- Time-critical engagement (no time for ATGM setup)
- Need to suppress area targets or troops
- ATGM inventory depleted
- Target too close for ATGM minimum range (<400m)

**Use ATGM When:**
- Range > 1,500m or target in defilade
- Heavy armor (MBT) requiring guaranteed kill
- Standoff required due to heavy AAA threat
- Precision engagement required (minimize collateral damage)
- Target is stationary and SACLOS guidance time available

### Crew Coordination for Cannon Employment

**Single-Player Seat Switching:**
1. WSO Seat: Select cannon mode, verify master arm, identify target
2. Switch to Pilot Seat: Maneuver to attack heading, acquire target
3. Remain in Pilot Seat: Execute attack profile, fire cannon, break off
4. WSO Seat (post-attack): Conduct BDA, select next weapon if required

**Multi-Player Crew Procedures:**
- WSO: "Target identified, [type] at [range], ready for cannon"
- Pilot: "Tally target, rolling in"
- WSO: "Cleared to fire" (or "Hold fire" if abort required)
- Pilot: "Firing" (during trigger squeeze)
- WSO: Calls BDA — "Target destroyed/damaged/missed"
- Pilot: "Breaking [direction]"

### DCS-Specific Cannon Modeling Notes

**DCS Keyboard/HOTAS Bindings for Cannon:**
| Function | Default Key | Notes |
|---|---|---|
| Weapon Fire | Space | Primary trigger — fires currently selected weapon |
| Select Cannon | C (cycle) | Cycles weapon stations to cannon |
| Master Arm Toggle | See Module 1 | Must be armed before cannon fires |
| CCIP Mode Toggle | O (if available) | Enable CCIP pipper overlay |

**Recommended HOTAS Setup:**
- Bind weapon fire to primary trigger (1st detent or full press)
- Bind weapon cycle to HOTAS hat or switch
- Practice smooth trigger squeeze — avoid stabbing the button

**Accuracy Modeling:**
- DCS models ballistic dispersion based on range, flight conditions, and G-loading
- Dispersion increases with altitude, speed, and bank angle
- Vibration effects during firing may be simplified vs. real aircraft
- CCIP accuracy may be optimistic compared to real Mi-24P system

**Visual and Audio Cues:**
- Muzzle flash visible from cockpit (may affect night vision adaptation)
- Tracers (every 5th round) help with burst adjustment and range estimation
- Impact effects vary by target type and ammunition (sparks on armor, dust on ground)
- Rate of fire audio helps with burst discipline — practice counting "one-one-thousand" = ~40 rounds
- Empty ammunition warning: cessation of fire audio/visual

*⚠ Realism Divergence: The real GSh-30K produces significantly more airframe vibration and yaw moment than modeled in DCS. Real pilots report difficulty maintaining aim during extended bursts, with the aircraft requiring substantial pedal and cyclic input to hold on target. DCS provides a more benign firing experience, which may give unrealistic expectations of accuracy.*

### Common Student Errors in Cannon Employment

| Error | Consequence | Correction |
|---|---|---|
| **Too steep dive angle** | Excessive altitude loss; terrain impact risk | Limit to 25° maximum; practice altitude awareness |
| **Firing too early** | Rounds fall short; target escapes | Wait until 800-1,000m range; use CCIP reference |
| **Excessive burst length** | Ammunition wastage; barrel overheating | Practice 1-2 second burst discipline |
| **Poor pedal coordination** | Rounds scatter left/right of target | Coordinate pedal inputs to keep nose steady |
| **Late break-off** | AAA vulnerability; terrain impact | Break at 400-600m range regardless of BDA |
| **Wrong target prioritization** | Inefficient use of limited ammunition | Engage soft targets with cannon; save ATGM for armor |
| **Inadequate BDA** | Cannot assess need for re-engagement | Maintain visual on target area through break maneuver |

---

## Module 4: 9M114 Shturm ATGM Employment

### Learning Objectives
- Explain SACLOS guidance principles and crew responsibilities for Shturm
- Execute proper WSO guidance technique throughout missile time-of-flight
- Demonstrate pilot flight profile requirements for SACLOS guidance
- Apply Shturm engagement envelopes for various target types and ranges
- Coordinate single-player seat switching during ATGM engagements
- Troubleshoot SACLOS guidance failures and execute abort procedures
- Select appropriate employment profiles for tactical situations

### 9M114 Shturm System Data

| Specification | Value | Notes |
|---|---|---|
| **Full Designation** | 9M114 Shturm (Storm) | NATO: AT-6 Spiral |
| **System Designation** | 9K113 Shturm complex | Complete weapon system |
| **Launcher** | APU-68UM rail | 2 missiles per outer pylon max |
| **Guidance Type** | Radio-command SACLOS | Semi-Automatic Command to Line-Of-Sight |
| **Warhead** | HEAT shaped charge | 600+ mm RHA penetration |
| **Warhead Weight** | 5.4 kg | High explosive content |
| **Missile Weight** | 31 kg | Complete round |
| **Length** | 1.8m | Transportation/storage length |
| **Diameter** | 130mm | Body diameter |
| **Propulsion** | Solid rocket + sustainer | Two-stage motor |

### Shturm Performance Envelope

| Parameter | Value | Constraints |
|---|---|---|
| **Minimum Range** | 400m | Guidance stabilization distance |
| **Maximum Range** | 5,000m | Radio command effective range |
| **Typical Engagement** | 1,500-4,000m | Optimal accuracy envelope |
| **Missile Velocity** | 350 m/s average | Variable throughout flight |
| **Time of Flight** | 15 seconds (max range) | WSO guidance duration |
| **Altitude Limits** | 50m-4,000m AGL | Platform altitude limits |
| **Temperature Limits** | -40°C to +50°C | Operational constraints |

### SACLOS Guidance Principles

**Semi-Automatic Command to Line-Of-Sight (SACLOS) Explained:**
1. **WSO Role:** Keeps PKV-1 sight crosshair on target throughout missile flight
2. **System Role:** Tracks missile via IR beacon, measures deviation from sight line
3. **Radio Commands:** System transmits corrections to missile automatically
4. **Missile Role:** Receives commands via radio link, adjusts flight path
5. **No Pilot Input:** Pilot maintains steady flight; no direct missile control

**SACLOS vs. Other Guidance Types:**
| Guidance Type | Operator Workload | Platform Requirements | Advantages | Disadvantages |
|---|---|---|---|---|
| **SACLOS (Shturm)** | High (continuous track) | Steady flight required | Simple, reliable | Requires stable platform |
| **Laser SAL (Hellfire)** | Medium (maintain spot) | Laser illumination | Fire-and-forget capable | Laser can be defeated |
| **TV/IR (Maverick)** | Low (lock-and-shoot) | Minimal after launch | True fire-and-forget | Weather/smoke limitation |

**Platform Stability Requirements:**
- Maximum turn rate during guidance: ~5°/second
- No abrupt altitude changes >50m during missile flight
- Minimize vibration/turbulence effects on sight stability
- Autopilot engagement recommended during guidance phase

### WSO SACLOS Guidance Technique

**Pre-Launch Sequence:**
1. **Target Acquisition:** PKV-1 on target, magnification 4-6×
2. **Range Estimation:** Confirm target within Shturm envelope
3. **Weapon Selection:** Select Shturm mode, verify pylon armed
4. **Sight Stabilization:** Ensure smooth sight movement on target
5. **Launch Authorization:** "Ready to fire" call to pilot

**Launch and Guidance:**
1. **Launch:** Press fire button — missile leaves rail after 0.5-1 second delay
2. **Initial Tracking:** Keep crosshair on target — do NOT follow missile
3. **Guidance Phase:** Missile appears in peripheral vision; continue target track
4. **Steady Tracking:** Smooth joystick inputs; avoid overcontrolling
5. **Terminal Phase:** Maintain track until impact (or 3-5 seconds after)

**Post-Impact:**
1. **BDA:** Assess target destruction/damage through PKV-1
2. **Re-engagement:** If required, select next missile and repeat
3. **Break:** Maneuver only after guidance complete or missile impact

**Critical WSO Technique Points:**
- Track the TARGET, not the missile
- Smooth, steady sight movements — avoid jerky corrections
- If you lose sight of target, continue tracking last known position
- Do not chase the missile's flightpath with the sight
- Maintain crosshair on target center-mass throughout flight

### Pilot Flight Profile During SACLOS

**Ideal Flight Profile:**
- Straight and level flight at constant airspeed
- Minimize turn rate to <5°/second maximum
- Avoid altitude changes >20m during missile flight
- Maintain power setting to avoid airspeed fluctuation
- Use autopilot if available and reliable

**Acceptable Maneuvers During Guidance:**
- Very gentle turns (<3°/second)
- Minor altitude corrections for terrain clearance
- Small power adjustments to maintain airspeed
- Defensive maneuvers only if under immediate fire

**Prohibited Maneuvers:**
- Hard turns >10°/second
- Aggressive climbs/dives
- Autorotation or emergency procedures (unless critical)
- Evasive jinking or random maneuvers

### Shturm Employment Profiles

#### 1. Profile Attack (Primary Technique)

| Phase | Altitude | Airspeed | Actions |
|---|---|---|---|
| **Approach** | 50-100m AGL | 200-250 km/h | Low-level, terrain masking |
| **Pop-Up** | 200-400m AGL | Reduce to 180 km/h | Gain altitude for LOS |
| **Acquire** | Hold altitude | 160-180 km/h | WSO finds target |
| **Fire** | Hold steady | Hold airspeed | Launch missile |
| **Guide** | ±20m altitude | ±20 km/h speed | 10-15 seconds steady |
| **Break** | Dive to 50m | Increase speed | After impact/miss |

#### 2. Running Fire (High Threat Areas)

| Parameter | Value | Notes |
|---|---|---|
| **Altitude** | 100-300m AGL | Above small arms, below SAMs |
| **Airspeed** | 220-260 km/h | Compromise speed/stability |
| **Course** | Straight line 3-5 km | Parallel to threat axis |
| **Engagement** | Single shot per pass | No time for re-engagement |
| **Escape** | Immediate after impact | No BDA assessment |

#### 3. Hull-Down/Stationary (Deliberate Attack)

| Parameter | Value | Application |
|---|---|---|
| **Position** | Terrain-masked hover/taxi | Behind ridgeline or trees |
| **Exposure** | Minimal — sight line only | Just enough for LOS |
| **Time** | Extended — up to 30 seconds | Multiple engagements |
| **Advantage** | Maximum accuracy | Stable platform |
| **Risk** | Vulnerable if detected | Requires escape plan |

### Engagement Envelope Parameters

**Range vs. Target Type:**
| Target | Minimum Range | Optimum Range | Maximum Range | Notes |
|---|---|---|---|---|
| **MBT (frontal)** | 800m | 2,000-3,000m | 5,000m | Standoff from return fire |
| **MBT (flank/rear)** | 400m | 1,500-2,500m | 5,000m | Higher kill probability |
| **IFV/APC** | 400m | 1,000-2,000m | 4,000m | Adequate warhead effect |
| **Bunkers** | 600m | 1,500-2,500m | 4,000m | Structural targets |
| **Mobile AAA** | 800m | 2,500-4,000m | 5,000m | Avoid return fire envelope |

**Aspect Angle Considerations:**
- **Frontal (0-30°):** Requires precision aim; maximum armor
- **Oblique (30-60°):** Good compromise; adequate penetration
- **Flank (60-90°):** Optimum kill probability; thinner armor
- **Rear (>90°):** Maximum effect; engine compartment vulnerable

### DCS Cockpit Procedures (Step-by-Step)

**DCS Key Bindings for Shturm ATGM:**
| Function | Default Key | Notes |
|---|---|---|
| Select ATGM | D (weapon cycle) | Cycle to ATGM mode |
| Fire Missile | Space | Fire currently selected ATGM |
| PKV-1 Slew | Numpad 2/4/6/8 | Track target through sight |
| PKV-1 Zoom In/Out | Numpad +/- | Magnification control |
| Seat Switch (WSO) | 1 | Access weapon controls |
| Seat Switch (Pilot) | 2 | Access flight controls |
| Autopilot Engage | A (default) | Heading/altitude hold for stable guidance |

**Single-Player ATGM Engagement:**

1. **Setup (WSO Seat):**
   - Seat switch: Press "1" for WSO seat
   - Master Arm: Verify ARMED
   - Weapon Selector: Set to ATGM
   - Missile Type: Select SHTURM
   - Pylon Select: Choose appropriate pylon (1 or 4 for outer stations)

2. **Target Acquisition (WSO Seat):**
   - PKV-1: Power ON, weapon mode ATGM
   - Magnification: 4-6× for target identification
   - Acquire: Center crosshair on target aimpoint
   - Range: Estimate and confirm within Shturm envelope

3. **Pre-Launch (Switch to Pilot Seat):**
   - Seat switch: Press "2" for pilot seat
   - Position: Maneuver for engagement geometry
   - Autopilot: Engage if available (heading/altitude hold)
   - Airspeed: Stabilize at 160-180 km/h

4. **Launch (WSO Seat):**
   - Quick seat switch: Press "1"
   - Final check: Crosshair on target
   - Fire: Press Space or assigned fire button
   - Track: Maintain crosshair on target (do NOT follow missile)

5. **Guidance Phase (WSO Seat):**
   - Duration: 8-15 seconds depending on range
   - Track: Keep crosshair steady on target center-mass
   - Corrections: Smooth joystick inputs only
   - Ignore: Missile flightpath — track target only

6. **Post-Impact:**
   - BDA: Assess through PKV-1 sight
   - Next Target: If multiple engagements planned
   - Break: Switch to pilot seat and maneuver away

**Multi-Player Procedures:**
- WSO handles all targeting, weapon selection, and guidance
- Pilot maintains steady flight per WSO guidance calls
- Standard crew calls: "Ready to fire," "Firing," "Guiding," "Impact," "Break"

### Shturm vs. Western ATGM Comparison

| Aspect | 9M114 Shturm | AGM-114 Hellfire | Notes |
|---|---|---|---|
| **Guidance** | Radio-command SACLOS | Semi-active laser SAL | Different tracking methods |
| **Operator Workload** | High (continuous track) | Medium (maintain laser) | Shturm requires more focus |
| **Platform Constraints** | Must maintain steady flight | Can maneuver after launch | Shturm more restrictive |
| **Range** | 5 km | 8+ km | Hellfire has longer reach |
| **Warhead** | 5.4 kg HEAT | 9 kg tandem HEAT | Hellfire more powerful |
| **Accuracy** | ±1 meter CEP | ±0.5 meter CEP | Hellfire more precise |
| **Jam Resistance** | Moderate (radio frequency) | High (laser frequency) | Different vulnerabilities |

### Common SACLOS Guidance Errors

| Error | Symptom | Cause | Correction |
|---|---|---|---|
| **Missile flies right of target** | Impact right of aimpoint | WSO overcorrecting left | Reduce joystick input magnitude |
| **Missile flies high** | Impact above target | Aircraft climbing during guidance | Pilot: maintain level flight |
| **Guidance link lost** | Missile flies ballistic | Radio interference or range | Re-engage with new missile |
| **Late impact (wide miss)** | Missile doesn't guide to target | WSO lost target track | Practice target tracking discipline |
| **Premature impact** | Missile hits ground early | Aircraft descending or sight aimed low | Pilot: level flight; WSO: aim center mass |
| **Spiral flight path** | Erratic missile behavior | Excessive WSO corrections | Smooth, minimal joystick inputs |

### Tactical Employment Considerations

**Multiple Target Engagements:**
- Plan engagement sequence by priority and geometry
- Maximum 2 consecutive shots per position (counter-battery avoidance)
- Reserve 1-2 missiles for self-defense or opportunity targets
- Consider ammunition remaining vs. threat density

**Threat Environment Integration:**
- Coordinate with SPO-15 RWR — abort if SAM threat develops
- Plan escape routes before engagement
- Use terrain masking between shots
- Monitor AAA threat range vs. ATGM standoff distance

**Weather and Visibility:**
- SACLOS requires visual contact throughout missile flight
- Haze, dust, or smoke degrades guidance accuracy
- Minimum visibility: 3-4 km for effective employment
- Sun angle: avoid firing directly into sun (sight washout)

### Advanced SACLOS Techniques

**Moving Target Engagement:**
- Lead target by estimated movement during missile flight
- Track projected intercept point, not current target position
- Account for target speed: slow vehicles need minimal lead
- Fast vehicles (>30 km/h): may require 1-2 vehicle lengths lead

**Multiple Missile Ripple Fire:**
- Launch second missile 3-5 seconds after first
- Maintain guidance on first missile until impact
- Switch to second missile guidance after first impact
- Requires experienced WSO — high workload technique

**Defensive ATGM Employment:**
- Launch from maximum range to minimize exposure
- Single shot per firing position
- Immediate displacement after missile impact
- No BDA assessment — assume hit and evade

### DCS-Specific Shturm Modeling Notes

**Guidance Fidelity:**
- DCS SACLOS implementation tracks WSO sight line accurately
- Missile responds to PKV-1 crosshair position with slight delay (~0.1-0.2 sec)
- Guidance link reliability is 100% within range envelope in DCS (no random failures)
- Real-world radio command link is subject to ECM, terrain multipath, and weather; DCS does not model these

**Platform Stability in DCS:**
- DCS autopilot provides adequate stability for SACLOS guidance
- In single-player, autopilot is essential — cannot guide and fly simultaneously
- Multi-player: pilot must maintain discipline; jerky inputs will degrade accuracy
- DCS wind model may cause slight sight drift during guidance — compensate with joystick

**Missile Flight Behavior:**
- DCS Shturm flight profile is generally accurate (boost + sustain phases)
- Missile visible as bright spot in sight peripheral vision — ignore it
- Impact flash is reliable for BDA in clear weather
- DCS may model slightly better hit probability than real system at extreme ranges

*⚠ Realism Divergence: The real 9M114 Shturm has a documented probability of hit (Pk) of approximately 0.85-0.90 against stationary targets under ideal conditions, degrading to 0.50-0.70 against moving targets or in adverse weather. DCS does not model random guidance failures, so experienced WSOs can achieve near-perfect hit rates. Additionally, the real Shturm radio command link is susceptible to electronic countermeasures (ECM) which DCS does not simulate. Real SACLOS also requires that the launch platform antenna maintain clear line-of-sight to the missile's rear beacon — terrain shadowing can break guidance.*

*⚠ Realism Divergence: Real Mi-24 ATGM employment doctrine emphasizes formation tactics — one helicopter designates while another maneuvers. Single-ship ATGM attacks are considered emergency-only in Soviet doctrine due to the platform vulnerability during the 10-15 second guidance phase. DCS single-player missions often require solo ATGM employment, which is doctrinally unrealistic.*

---

## Module 5: 9M120 Ataka ATGM Employment

### Learning Objectives
- Compare and contrast Ataka vs. Shturm capabilities and employment
- Select appropriate Ataka warhead variant (HEAT vs. thermobaric) for target type
- Execute extended-range engagements using Ataka's 6km capability
- Apply faster missile speed implications for guidance and tactics
- Demonstrate mixed Shturm/Ataka loadout employment techniques
- Coordinate sequential ATGM engagements with different missile types
- Assess Ataka effectiveness against various target types

### 9M120 Ataka System Data

| Specification | Value | Notes |
|---|---|---|
| **Full Designation** | 9M120 Ataka (Attack) | NATO: AT-9 Spiral-2 |
| **System Designation** | 9K121 Ataka complex | Improved Shturm evolution |
| **Launcher** | APU-68UM rail (same as Shturm) | Compatible rail system |
| **Guidance Type** | Radio-command SACLOS (improved) | Enhanced guidance algorithm |
| **Warhead Weight** | 5.4-6.0 kg | Varies by variant |
| **Missile Weight** | 42 kg | Heavier than Shturm |
| **Length** | 1.87m | Slightly longer than Shturm |
| **Diameter** | 130mm | Same as Shturm |
| **Propulsion** | Solid rocket + sustainer | More powerful motor |

### Ataka Performance Envelope (Improved vs. Shturm)

| Parameter | Ataka Value | Shturm Comparison | Improvement |
|---|---|---|---|
| **Minimum Range** | 400m | 400m | Same |
| **Maximum Range** | 6,000m | 5,000m | +1,000m (20%) |
| **Typical Engagement** | 2,000-5,000m | 1,500-4,000m | Extended envelope |
| **Missile Velocity** | 400-550 m/s | 350 m/s | 40-57% faster |
| **Time of Flight** | 12 seconds (max range) | 15 seconds | 20% faster |
| **Accuracy (CEP)** | ±0.5m | ±1.0m | 50% more accurate |

### Ataka Warhead Variants (DCS Implementation)

| Variant | NATO Code | Warhead Type | Penetration/Effect | Best Targets | DCS Availability |
|---|---|---|---|---|---|
| **9M120F** | AT-9A | HEAT tandem charge | 800+ mm RHA | MBTs, heavy armor | Standard |
| **9M120F-1** | AT-9B | Thermobaric | Blast/overpressure | Bunkers, buildings, troops | If modeled |
| **9M120M** | AT-9C | HEAT enhanced | 950+ mm RHA | Modern MBTs | Advanced variant |

*⚠ Realism Divergence: DCS may not model all warhead variants; check mission editor for available types.*

### Key Differences from Shturm

**Performance Advantages:**
- **Extended Range:** 6km vs. 5km maximum engagement
- **Higher Speed:** Reduced time-of-flight and exposure time
- **Improved Accuracy:** Better guidance algorithm and aerodynamics
- **Enhanced Warhead:** Tandem charge penetrates reactive armor
- **Weather Tolerance:** Improved performance in adverse conditions

**Tactical Implications:**
- **Standoff Capability:** Engage beyond most AAA effective range
- **Reduced Guidance Time:** Less pilot workload for platform stability
- **Multiple Target Capability:** Faster re-engagement cycle
- **Survivability:** Greater standoff reduces counter-fire risk

**Employment Considerations:**
- **Cost vs. Benefit:** Save Ataka for high-value/long-range targets
- **Warhead Selection:** Choose appropriate variant for target type
- **Mixed Loadouts:** Combine with Shturm for versatility

### Thermobaric Warhead Employment

**Thermobaric (Fuel-Air Explosive) Physics:**
- **Phase 1 — Dispersal:** Warhead ruptures, dispersing fuel aerosol cloud (~8-10m diameter)
- **Phase 2 — Ignition:** Detonation wave ignites aerosol cloud after ~100ms delay
- **Phase 3 — Blast:** Overpressure wave propagates through area (peak pressure ~30 bar in enclosed spaces)
- **Phase 4 — Vacuum:** Negative pressure phase — oxygen depletion and vacuum effect
- **Total effect duration:** ~200-500ms
- **Lethal radius (open air):** ~10-15m from detonation point
- **Lethal radius (enclosed):** Fills entire enclosed space (bunker, room, trench)

**Key Thermobaric Properties:**
- Overpressure propagates around corners and into openings (unlike shaped charges)
- Concrete structures amplify the blast effect (pressure reflection)
- Open-air effectiveness is reduced compared to enclosed space employment
- Ineffective against heavy armor (no penetration capability)
- Highly effective against personnel regardless of body armor
- Secondary fires common from ignited materials

**Thermobaric vs. HEAT Target Selection:**
| Target Type | HEAT Ataka | Thermobaric Ataka | Reasoning |
|---|---|---|---|
| **MBT** | Primary choice | Not effective | Requires penetration |
| **APC/IFV** | Effective | Effective | Either warhead works |
| **Bunkers** | Limited effect | Primary choice | Overpressure vs. structure |
| **Buildings** | Penetrates but limited | Devastating | Area effect preferred |
| **Troops in Open** | Overkill | Excellent | Area effect advantage |
| **Artillery Sites** | Effective | Excellent | Personnel + equipment |

### Ataka Employment Profiles

#### 1. Extended Standoff Engagement (Unique to Ataka)

| Parameter | Value | Rationale |
|---|---|---|
| **Range** | 4,000-6,000m | Beyond most AAA effective range |
| **Altitude** | 300-600m AGL | Line-of-sight over terrain |
| **Profile** | Level flight or gentle climb | Maximize range performance |
| **Target Priority** | High-value, stationary | Justify long-range shot |
| **Guidance Time** | 10-15 seconds | Extended platform stability requirement |

**Extended Range Execution:**
1. **Approach:** High altitude approach for maximum LOS
2. **Acquisition:** Early target identification at extended range
3. **Setup:** Stable platform, minimal maneuvering
4. **Launch:** From maximum effective range
5. **Guidance:** Extended guidance time — maintain discipline
6. **Escape:** Immediate break after impact/miss

#### 2. Sequential Mixed ATGM Employment

**Shturm First, Ataka Follow-up:**
- Use Shturm for initial target (shorter range, lower cost)
- Reserve Ataka for long-range or high-priority targets
- Switch missile types based on target distance and importance

**Ataka First, Shturm Clean-up:**
- Use Ataka for primary threat at long range
- Follow with Shturm for closer secondary targets
- Exploit Ataka's extended range for opening engagement

### DCS Cockpit Procedures (Ataka-Specific)

**DCS Key Bindings for Ataka ATGM:**
| Function | Default Key | Notes |
|---|---|---|
| Select ATGM | D (weapon cycle) | Cycle until ATGM mode active |
| Fire Missile | Space | Fires currently selected ATGM |
| Pylon Select | W / E (cycle) | Choose loaded pylon station |
| PKV-1 Slew | Numpad 2/4/6/8 | Guide missile via sight tracking |
| PKV-1 Zoom | Numpad +/- | Adjust magnification for range |
| Seat Switch (WSO) | 1 | Access ATGM controls and sight |
| Seat Switch (Pilot) | 2 | Fly aircraft during guidance |
| Autopilot Engage | A | Essential for single-player SACLOS |

**Warhead Variant Selection (if available):**
1. **Weapon Panel:** Select ATGM mode
2. **Missile Type:** Choose ATAKA from selector
3. **Warhead Select:** HEAT or Thermobaric (if modeled)
4. **Pylon Select:** Choose loaded pylon (typically outer stations)

**Mixed Loadout Management:**
- **Example:** Station 1: 2×Shturm, Station 4: 2×Ataka
- **Target Assignment:** Close targets → Shturm; distant/critical → Ataka
- **Ammunition Count:** Track remaining missiles by type
- **Engagement Priority:** Use appropriate missile for each target

### Extended Range Engagement Techniques

**Long Range Target Acquisition:**
- **Initial Detection:** Use naked eye or binoculars at 4-6km
- **PKV Magnification:** Maximum zoom (6-8×) for identification
- **Range Estimation:** Critical for 4,000m+ shots
- **Environmental Factors:** Heat shimmer, atmospheric clarity affect accuracy

**Platform Stability at Extended Range:**
- **Autopilot Use:** Essential for 10-15 second guidance
- **Altitude Selection:** Higher altitude reduces terrain masking
- **Wind Compensation:** Crosswinds more significant at long range
- **Vibration Control:** Smooth flight critical for accuracy

### Ataka vs. Shturm Tactical Decision Matrix

| Situation | Recommended Missile | Reasoning |
|---|---|---|
| **Target at 1,500m** | Shturm | Save Ataka for long-range shots |
| **Target at 4,500m** | Ataka | Beyond effective Shturm range |
| **MBT in open** | Either (HEAT variant) | Both effective against armor |
| **Bunker complex** | Ataka (thermobaric) | Optimal warhead for target |
| **High-threat AAA area** | Ataka | Extended standoff capability |
| **Multiple close targets** | Shturm | Conserve expensive Ataka |
| **Time-critical shot** | Ataka | Faster time-of-flight |
| **Moving target** | Ataka | Better accuracy, less lead required |

### Advanced Ataka Employment Techniques

**Rapid Sequential Engagements:**
1. **First Shot:** Ataka at longest-range target
2. **Guidance:** Maintain track while preparing next shot
3. **Impact/Assessment:** Quick BDA
4. **Second Shot:** Immediate follow-up (Shturm or second Ataka)
5. **Escape:** Break contact after second impact

**Mixed Warhead Tactics:**
- **HEAT for Armor:** Primary anti-tank mission
- **Thermobaric for Structures:** Urban/fortified positions
- **Sequential Employment:** HEAT to breach, thermobaric to clear
- **Target-Specific Selection:** Match warhead to target type

### Ataka Effectiveness vs. Target Types

| Target | HEAT Ataka | Thermobaric Ataka | Expected Result |
|---|---|---|---|
| **T-80/T-72 MBT** | High kill probability | Minimal effect | HEAT penetrates armor |
| **BMP-2/3 IFV** | Guaranteed kill | Guaranteed kill | Either warhead effective |
| **Concrete Bunker** | Structural damage | Complete destruction | Thermobaric optimal |
| **Soft Bunker/Trench** | Limited effect | Devastating | Overpressure effect |
| **Command Post (building)** | Penetration only | Complete destruction | Area effect preferred |
| **SAM Site (mixed)** | Equipment damage | Personnel + equipment | Thermobaric affects both |
| **Artillery Battery** | Single vehicle | Multiple vehicles/crew | Area effect advantage |

### Common Ataka Employment Errors

| Error | Consequence | Correction |
|---|---|---|
| **Using Ataka for close targets** | Waste expensive missile | Reserve for long-range/high-value |
| **Wrong warhead selection** | Suboptimal target effect | Match warhead to target type |
| **Inadequate platform stability** | Reduced accuracy at long range | Use autopilot, minimize maneuvering |
| **Poor range estimation** | Miss at extended range | Practice ranging techniques |
| **Rushing long-range shots** | Wasted engagement opportunity | Take time for proper setup |
| **Not exploiting range advantage** | Unnecessary exposure to threats | Use 4-6km standoff when possible |
| **Ignoring environmental factors** | Degraded accuracy | Account for visibility, wind, shimmer |

### Ataka vs. Western Long-Range ATGM

| Aspect | 9M120 Ataka | AGM-114L Hellfire | AH-64 Apache Comparison |
|---|---|---|---|
| **Maximum Range** | 6 km | 8+ km | Hellfire slight advantage |
| **Guidance** | Radio SACLOS | Semi-active laser | Different methods |
| **Platform Constraint** | Must maintain steady flight | Can maneuver after launch | Ataka more restrictive |
| **Warhead Options** | HEAT/thermobaric | HEAT/blast-frag | Similar variety |
| **All-Weather** | Limited (optical sight) | Good (laser/radar) | Western systems superior |
| **Accuracy** | ±0.5m CEP | ±0.3m CEP | Slight Western advantage |

### Realism Divergences (DCS Ataka Implementation)

*⚠ Realism Divergence: DCS may not model all three 9M120 warhead variants. The thermobaric variant (9M120F-1) may be unavailable or simplified. Check the DCS Mission Editor for which variants are selectable on the Mi-24P. Real-world variant selection is performed during pre-flight loading — the crew cannot change warhead type in flight.*

*⚠ Realism Divergence: Real 9M120 Ataka guidance reliability is approximately 0.88-0.93 Pk against stationary targets, degrading at extreme range and in adverse weather. DCS typically provides near-perfect guidance fidelity, making hits appear easier than real-world employment. Additionally, the real Ataka's radio command link operates on a different frequency band than Shturm, requiring separate radio channels — DCS does not model this frequency management.*

*⚠ Realism Divergence: Thermobaric warhead effects in DCS may be significantly simplified. Real thermobaric weapons produce devastating overpressure effects in enclosed spaces that are difficult to model in game engines. DCS may represent the effect as a standard explosion with increased radius rather than modeling true fuel-air explosive physics. Target damage in enclosed spaces may be under-represented.*

**Simplified Aspects in DCS:**
- Warhead selection may be pre-configured vs. field-selectable
- Guidance accuracy may be optimistic compared to real system
- Environmental effects (weather, visibility) simplified
- Radio jamming/interference not typically modeled
- Thermobaric effects may be under-modeled for enclosed targets
- Mixed Shturm/Ataka management may be streamlined

**Training Value Despite Simplifications:**
- Core SACLOS principles remain accurate and transferable
- Crew coordination requirements are realistic
- Tactical employment decision-making (warhead selection, range management) is valid
- Range/performance data is representative of real capabilities
- The doctrine of matching warhead type to target type is faithfully represented

---

## Module 6: Unguided Rocket Employment (S-5, S-8, S-13, S-24)

### Learning Objectives
- Identify Soviet unguided rocket families (S-5, S-8, S-13, S-24) and their warhead variants
- Execute CCIP-guided rocket attacks using PKV-1 sight integration
- Apply appropriate rocket selection for different target types and missions
- Demonstrate diving and shallow rocket attack profiles
- Coordinate salvo fire control for area and point targets
- Operate UB-16, UB-32, B-8V20A, and B-13L launcher pods
- Assess rocket effectiveness and plan re-engagement sequences
- Apply rocket employment in suppression and close support roles

### Soviet Unguided Rocket System Overview

**Naming Convention:**
- **S** = Snaryad (Projectile/Shell)
- **Number** = Caliber in millimeters (approximately)
- **Letter Suffix** = Warhead type (M = standard, K = cumulative/HEAT, O = fragmentation, OF = HE-Frag)

**Launcher Pod Designations:**
- **UB** = Universalny Blok (Universal Block) — S-5 launchers
- **B** = Blok (Block) — S-8 and S-13 launchers
- **APU** = Aviatsionnoye Puskovoye Ustroistvo (Aircraft Launch Device) — S-24 rail

**Complete Launcher Integration:**
| Rocket Type | Caliber | Standard Launcher | Capacity per Pod | Compatible Stations | Weight per Pod (loaded) |
|---|---|---|---|---|---|
| **S-5** | 57mm | UB-16-57 pod | 16 rockets | Inner/Outer (1,2,3,4) | ~160 kg |
| **S-5** | 57mm | UB-32A-24 pod | 32 rockets | Inner/Outer (1,2,3,4) | ~290 kg |
| **S-8** | 80mm | B-8V20A pod | 20 rockets | Inner/Outer (2,3,4) | ~252 kg |
| **S-13** | 122mm | B-13L pod | 5 rockets | Inner/Outer (all) | ~435 kg |
| **S-24** | 240mm | APU-68UM rail | 1 rocket | Outer only (1,4) | ~235 kg |

### S-5 (57mm) Rocket System

**S-5 Performance Data:**
| Specification | Value | Notes |
|---|---|---|
| **Caliber** | 57mm | Lightest Soviet helicopter rocket |
| **Length** | ~0.88m (varies by variant) | Compact; high pod density |
| **Weight** | 3.7-5.0 kg (by variant) | Lightest rocket in inventory |
| **Motor Burn Time** | 0.7-1.0 seconds | Short burn; coast to target |
| **Maximum Range** | 2,500-3,000m | Shorter than S-8 |
| **Effective Range** | 300-1,500m | Close-range area weapon |
| **Muzzle Velocity** | 450 m/s | Moderate initial velocity |
| **Dispersion** | Higher than S-8 (~5-8 mils) | Area saturation weapon |

**S-5 Warhead Variants (DCS Availability):**
| Designation | Warhead Type | Weight | Effect | Best Targets | DCS Model |
|---|---|---|---|---|---|
| **S-5M** | HE-Fragmentation | 3.86 kg | Fragments + blast (lethal radius ~5m) | Troops, soft vehicles | Standard |
| **S-5K** | HEAT cumulative | 3.7 kg | ~130mm RHA penetration | Light armor, trucks | If available |
| **S-5KO** | HEAT + fragmentation | 4.0 kg | Dual-purpose: penetration + fragments | Mixed targets | If available |
| **S-5S** | Flechette (APERS) | 5.0 kg | 1,000 flechettes per rocket | Troops, unprotected targets | If available |

**UB-16-57 Pod Configuration:**
- **Tube Arrangement:** 4×4 matrix (16 tubes)
- **Firing Sequence:** Configurable — single, pairs, or full salvo
- **Electrical Interface:** 28V DC firing circuit
- **Pod Weight (empty):** ~57 kg
- **Primary Role:** Area saturation with high volume of fire

**UB-32A-24 Pod Configuration:**
- **Tube Arrangement:** Concentric rings (32 tubes)
- **Firing Sequence:** Sequential or salvo
- **Pod Weight (empty):** ~83 kg
- **Primary Role:** Maximum firepower per pylon; 32 rockets per pod
- **Note:** UB-32 is the preferred pod for maximum volume of fire

**S-5 Employment Notes:**
- S-5 rockets are the lightest and cheapest option — use for area suppression
- High volume of fire compensates for lower individual accuracy
- UB-32 pod carries 32 rockets — sustained suppression capability
- Not effective against armor heavier than BTR-class APCs
- Ideal for "danger close" support due to smaller warhead blast radius
- Short effective range (~1,500m) requires closer approach than S-8

*⚠ Realism Divergence: S-5 availability on the DCS Mi-24P depends on the module version. Some DCS versions may not include S-5 rockets or UB-16/UB-32 pods. Check the DCS Mission Editor loadout options. If unavailable, S-8 rockets in B-8V20A pods serve a similar tactical role.*

### S-8 (80mm) Rocket System

**S-8 Performance Data:**
| Specification | Value | Notes |
|---|---|---|
| **Caliber** | 80mm | Standard Soviet medium rocket |
| **Length** | 1.68m | Including warhead and motor |
| **Weight** | 11.3 kg | Complete rocket |
| **Motor Burn Time** | 1.1 seconds | Sustainer burns throughout flight |
| **Maximum Range** | 4,000m | Ballistic maximum |
| **Effective Range** | 500-2,000m | Accuracy-limited envelope |
| **Muzzle Velocity** | 510 m/s | Initial velocity at rail departure |

**S-8 Warhead Variants (DCS Availability):**
| Designation | Warhead Type | Weight | Effect | Best Targets | DCS Model |
|---|---|---|---|---|---|
| **S-8KOM** | HEAT cumulative | 9.2 kg | 420mm RHA penetration | Light armor, APCs | Standard |
| **S-8TsM** | Thermobaric | 9.5 kg | Blast/overpressure | Bunkers, structures | If available |
| **S-8OFP2** | HE-Fragmentation | 9.4 kg | Area fragmentation | Soft targets, personnel | Standard |
| **S-8BM** | Bunker-penetrating | 9.8 kg | Delayed fuze penetrator | Hardened structures | If available |

**B-8V20A Pod Configuration:**
- **Tube Arrangement:** 4 rows × 5 columns
- **Firing Sequence:** Configurable (sequential/paired/salvo)
- **Electrical Interface:** 28V DC firing circuit
- **Safety Features:** Arming delay, misfire indication
- **Reload Time:** Ground servicing only (no air-to-air reload)

### S-13 (122mm) Rocket System

**S-13 Performance Data:**
| Specification | Value | Notes |
|---|---|---|
| **Caliber** | 122mm | Heavy unguided rocket |
| **Length** | 1.68m | Same length as S-8 |
| **Weight** | 58.5 kg | Much heavier than S-8 |
| **Motor Burn Time** | 2.2 seconds | Longer burn for heavier payload |
| **Maximum Range** | 4,500m | Extended range vs. S-8 |
| **Effective Range** | 800-2,500m | Accuracy envelope |
| **Muzzle Velocity** | 475 m/s | Slightly slower than S-8 |

**S-13 Warhead Variants:**
| Designation | Warhead Type | Weight | Effect | Best Targets |
|---|---|---|---|---|
| **S-13OF** | HE-Fragmentation | 32 kg | Large blast radius | Soft area targets |
| **S-13B** | Bunker penetrator | 33 kg | Concrete penetration + HE | Hardened structures |
| **S-13DF** | Dual-purpose | 31 kg | Penetration + fragmentation | Mixed targets |

**B-13L Pod Configuration:**
- **Tube Arrangement:** Single row, 5 rockets
- **Firing Modes:** Single, paired, or full salvo
- **Recoil Effect:** Significant due to heavy rockets
- **Accuracy:** Lower than S-8 due to weight and size

### S-24 (240mm) Heavy Rocket System

**S-24 Performance Data:**
| Specification | Value | Notes |
|---|---|---|
| **Caliber** | 240mm | Heaviest Soviet helicopter rocket |
| **Length** | 2.3m | Longer than S-8/S-13 |
| **Weight** | 235 kg | Complete rocket on rail |
| **Motor Burn Time** | 3.0 seconds | Extended burn time |
| **Maximum Range** | 6,000m | Long-range capability |
| **Effective Range** | 1,500-4,000m | Practical accuracy limit |
| **Muzzle Velocity** | 420 m/s | Slower due to massive weight |

**S-24 Warhead:**
| Designation | Warhead Type | Weight | Effect | Application |
|---|---|---|---|---|
| **S-24B** | High explosive | 123 kg | Massive blast effect | Bunkers, bridges, concentrations |

**APU-68UM Rail Configuration:**
- **Single Rocket:** One S-24 per rail
- **Maximum Load:** 4 rockets (outer pylons only)
- **Firing Effect:** Severe recoil; affects aircraft handling
- **Accuracy:** Manual aim only; no CCIP integration

### CCIP Integration for Rocket Employment

**Mi-24P CCIP System (DCS Implementation):**
- **Computation:** Real-time impact point calculation
- **Display:** Pipper overlay on PKV-1 sight or HUD
- **Inputs:** Airspeed, altitude, dive angle, rocket ballistics
- **Accuracy:** Dependent on stable flight and correct parameters

**CCIP Pipper Interpretation:**
| Rocket Type | CCIP Accuracy | Range Limitation | Notes |
|---|---|---|---|
| **S-5** | Medium (±15m at 1km) | Effective to 1.5km | Area weapon; accuracy less critical |
| **S-8** | High (±10m at 1km) | Effective to 2km | Most accurate CCIP rocket delivery |
| **S-13** | Medium (±20m at 1km) | Effective to 2.5km | Reduced precision but heavier warhead |
| **S-24** | Low/None | Manual aim only | No CCIP integration; fixed pipper only |

*⚠ Realism Divergence: Real Mi-24P CCIP for rockets is significantly less sophisticated than DCS implementation. The real system provides a basic computed sight depression rather than a dynamic pipper. DCS may provide enhanced accuracy aids that do not exist on the real aircraft, making rocket employment appear easier than real-world operations.*

### Rocket Employment Profiles

#### 1. Diving Rocket Attack (Primary Profile)

**S-8 Diving Parameters:**
| Parameter | Value | Rationale |
|---|---|---|
| **Entry Altitude** | 800-1,500m AGL | CCIP computation range |
| **Dive Angle** | 20-30° | Optimal accuracy vs. survivability |
| **Entry Airspeed** | 200-240 km/h | Stable platform speed |
| **Release Range** | 800-1,500m | Maximum accuracy envelope |
| **Salvo Size** | 2-4 rockets | Balance effect vs. ammunition conservation |
| **Break-off Range** | 500-700m | AAA avoidance |
| **Recovery Altitude** | 100m+ AGL | Terrain clearance |

**S-13 Diving Parameters:**
| Parameter | Value | Differences from S-8 |
|---|---|---|
| **Entry Altitude** | 1,000-1,800m AGL | Higher due to heavier rockets |
| **Dive Angle** | 25-35° | Steeper for better accuracy |
| **Release Range** | 1,200-2,000m | Extended range capability |
| **Salvo Size** | 1-2 rockets | Limited pod capacity |

**Diving Attack Execution:**
1. **Approach:** Level flight at entry altitude, identify target area
2. **Roll-in:** Bank to align with target, reduce power
3. **Dive Establish:** Achieve target dive angle, stabilize airspeed
4. **CCIP Acquisition:** PKV-1 on target, CCIP pipper visible
5. **Release:** Fire when pipper on target, maintain dive briefly
6. **Break-off:** Pull up at minimum range, level off at safe altitude

#### 2. Shallow Pass Profile

**Application:** Low-altitude approach, reduced exposure time
| Parameter | S-8 Value | S-13 Value | Notes |
|---|---|---|---|
| **Approach Altitude** | 50-200m AGL | 100-300m AGL | Terrain masking |
| **Dive Angle** | 5-15° | 10-20° | Gentle dive |
| **Release Range** | 1,500-2,500m | 2,000-3,000m | Extended standoff |
| **Target Types** | Area targets | Structures, concentrations | Less precision required |

#### 3. Level/Running Attack

**Emergency Profile Only:**
- **Altitude:** Very low (30-100m AGL)
- **Accuracy:** Significantly degraded
- **Application:** Suppression fire, area denial
- **Risk:** High exposure to ground fire

### Salvo Fire Control and Tactics

**Single Rocket Fire:**
- **Application:** Point targets, ammunition conservation
- **Technique:** Single trigger pull, immediate BDA
- **Re-engagement:** Adjust aim based on first round impact

**Paired Fire (2-4 Rockets):**
- **Application:** Small area targets, improved hit probability
- **Technique:** Brief trigger hold (0.5-1 second)
- **Pattern:** Small dispersion pattern on target
- **Effect:** Increased damage/suppression

**Salvo Fire (Full Pod):**
- **S-8:** 20 rockets in rapid sequence
- **S-13:** 5 rockets (full pod capacity)
- **Application:** Large area targets, saturation attack
- **Effect:** Area denial, massive suppression
- **Ammunition:** Significant expenditure; use judiciously

**Ripple Fire Timing:**
- **Interval:** 0.1-0.5 seconds between rockets
- **Pattern:** Adjustable dispersion
- **Control:** WSO manages salvo settings before attack

### Target Type vs. Rocket Selection Matrix

| Target Type | S-5 HE | S-5 HEAT | S-8 HEAT | S-8 HE-Frag | S-13 HE | S-24 HE | Primary Choice |
|---|---|---|---|---|---|---|---|
| **Light Armor (BMP)** | Ineffective | Marginal | Excellent | Good | Overkill | Overkill | S-8 HEAT |
| **APCs (BTR)** | Marginal | Good | Excellent | Good | Overkill | Overkill | S-8 HEAT or S-5K |
| **Trucks/Soft Vehicles** | Excellent | Overkill | Good | Excellent | Good | Overkill | S-5M or S-8 HE-Frag |
| **Troops in Open** | Excellent | Marginal | Limited | Excellent | Excellent | Excellent | S-5M / S-5S / S-8 HE-Frag |
| **Bunkers (soft)** | Ineffective | Ineffective | Limited | Good | Excellent | Excellent | S-13 HE |
| **Bunkers (hardened)** | Ineffective | Ineffective | Minimal | Minimal | Good | Excellent | S-24 HE |
| **Buildings** | Good | Good | Good | Good | Excellent | Excellent | S-13 HE |
| **AAA Sites** | Good | Good | Good | Excellent | Excellent | Excellent | S-8 HE-Frag / S-5 salvo |
| **Supply Dumps** | Good | Good | Good | Excellent | Excellent | Excellent | Mixed loadout |
| **Bridge/Infrastructure** | Ineffective | Ineffective | Minimal | Minimal | Good | Excellent | S-24 HE |
| **Troop Concentrations** | Excellent | Limited | Limited | Excellent | Excellent | Excellent | S-5 salvo / S-13 |

### Mixed Rocket Loadout Strategies

**Versatile Loadout Example:**
- **Station 1:** B-8V20A (S-8 HEAT) — anti-armor
- **Station 2:** B-8V20A (S-8 HE-Frag) — soft targets
- **Station 3:** B-13L (S-13 HE) — structures
- **Station 4:** S-24 — hardened targets

**Engagement Sequence:**
1. **Threat Assessment:** Identify primary target types in AO
2. **Weapon Selection:** Choose appropriate rocket for each target
3. **Attack Planning:** Sequence attacks by target priority and geometry
4. **Ammunition Management:** Track rounds remaining per type

### Crew Coordination for Rocket Employment

**DCS Key Bindings for Rocket Employment:**
| Function | Default Key | Notes |
|---|---|---|
| Select Rockets | D (weapon cycle) | Cycle to rocket mode |
| Fire Rockets | Space | Fire currently selected rocket type |
| Pylon Select | W / E (cycle) | Choose specific pod/pylon |
| Salvo Mode (if avail) | — | Check DCS Mi-24P key bindings |
| Ripple Interval (if avail) | — | May be set pre-flight only |
| CCIP Toggle | O (if available) | Enable CCIP pipper overlay |
| Master Arm | See Module 1 | Must be armed before rockets fire |

**Single-Player Procedures:**
1. **Setup (WSO Seat):** Select rocket type, set salvo mode, arm weapons
2. **Target Acquisition (WSO Seat):** PKV-1 on target, verify CCIP
3. **Attack (Pilot Seat):** Maneuver to attack heading, acquire CCIP pipper
4. **Fire (Pilot Seat):** Trigger pull when pipper on target
5. **BDA (WSO Seat):** Assess effect, select next weapon if required

**Multi-Player Crew Calls:**
- WSO: "Target identified, [type] at [bearing/range], recommend [rocket type]"
- Pilot: "Roger, maneuvering for rocket attack"
- WSO: "CCIP active, cleared to fire"
- Pilot: "Firing [salvo size]"
- WSO: "Impact, [BDA call]"
- Pilot: "Breaking [direction]"

### Advanced Rocket Employment Techniques

**Sequential Target Engagement:**
1. **Primary Target:** Highest threat (use appropriate rocket type)
2. **Secondary Target:** Opportunity target (use remaining rockets)
3. **Ammunition Management:** Reserve some rockets for egress/self-defense
4. **Re-engagement:** If required, reposition and attack again

**Suppression Fire:**
- **Technique:** Continuous rocket fire to suppress enemy activity
- **Application:** Covering friendly forces, neutralizing AAA
- **Rocket Choice:** S-8 HE-Frag for sustained fire
- **Pattern:** Area coverage rather than point accuracy

**Area Denial:**
- **Technique:** Blanket rocket fire across wide area
- **Application:** Deny enemy movement, create obstacles
- **Rocket Choice:** Mixed S-8/S-13 for varied effects
- **Timing:** Coordinate with ground forces for maximum effect

### Rocket vs. Other Weapons Decision Matrix

**Use Rockets When:**
- Multiple targets in same general area
- Area suppression required
- Targets beyond effective cannon range but closer than ATGM minimum
- Fast attack profile needed (no SACLOS guidance time)
- Mixed target types (armor and soft) in same engagement

**Use Other Weapons When:**
- **Cannon:** Single point target <1,500m, high accuracy required
- **ATGM:** Heavy armor >2,000m, precision kill required
- **Bombs:** Very large area targets, structures requiring maximum effect

### Environmental Factors Affecting Rocket Accuracy

**Wind Effects:**
- **Crosswind:** Deflects rockets left/right of intended path
- **Headwind:** Reduces range, steepens trajectory
- **Tailwind:** Extends range, flattens trajectory
- **Compensation:** CCIP accounts for known wind; adjust aim for unknown wind

**Visibility/Weather:**
- **Dust/Smoke:** Obscures target and impact assessment
- **Rain:** Affects rocket performance and sight visibility
- **Sun Angle:** Can wash out CCIP display or PKV-1 sight

**Altitude/Temperature Effects:**
- **High Altitude:** Reduced air density affects rocket performance
- **Temperature:** Hot weather reduces motor performance
- **Humidity:** Minimal effect on unguided rockets

### Common Rocket Employment Errors

| Error | Consequence | Correction |
|---|---|---|
| **Wrong salvo setting** | Too few/many rockets fired | Verify salvo selector before attack |
| **Poor CCIP discipline** | Rounds miss target area | Wait for stable pipper on target |
| **Inadequate dive angle** | Reduced accuracy, early break-off | Maintain 20-30° dive for best results |
| **Late target acquisition** | Rushed shot, poor accuracy | Acquire target early in dive |
| **Excessive salvo size** | Ammunition waste | Use minimum effective salvo |
| **Wrong rocket type** | Suboptimal target effect | Match warhead to target type |
| **Ignoring wind effects** | Consistent left/right miss | Compensate for observed wind |
| **Poor ammunition management** | Run out of appropriate rocket type | Plan engagement sequence |

### Realism Divergences (DCS Rocket Implementation)

*⚠ Realism Divergence: DCS rocket dispersion patterns are typically more consistent and predictable than real-world unguided rockets. Real S-8 rockets have a dispersion of approximately 3-7 mils depending on flight conditions, with individual rockets varying significantly due to manufacturing tolerances, propellant temperature, and in-flight stability. DCS may model tighter dispersion, making rockets appear more accurate than they are in reality.*

*⚠ Realism Divergence: S-5 rockets (if available in DCS) may have simplified ballistics. Real S-5 dispersion is considerably worse than S-8 due to the shorter motor burn and lighter weight, making them primarily area suppression weapons. DCS may model S-5 as more accurate than real-world performance.*

*⚠ Realism Divergence: Real S-24 employment from a helicopter is extremely rare and difficult. The S-24's massive recoil and weight severely affect helicopter handling. Most real Mi-24 units reserve S-24 for fixed-wing aircraft employment. DCS models the S-24 option but may not fully represent the handling challenges associated with firing a 235 kg rocket from a rotary-wing platform.*

**Simplified Aspects in DCS:**
- CCIP accuracy is optimistic vs. real Mi-24P system
- Wind and temperature effects on rocket performance may be reduced
- Rocket motor variability (real-world consistency issues) not modeled
- Warhead fragmentation patterns simplified
- Salvo fire control may be more user-friendly than real panel

**Training Value Maintained:**
- Core employment profiles (diving, shallow, level) are accurate
- Target type vs. weapon selection decision-making is realistic
- Crew coordination requirements reflect real-world procedures
- Range/altitude parameters are representative of actual doctrine

---

## Module 7: Air-to-Air Missiles — R-60 and R-73 (Self-Defense)

### Learning Objectives
- Understand Mi-24P air-to-air doctrine limitations and appropriate employment
- Execute R-60/R-73 engagement procedures against helicopter and slow aircraft threats
- Demonstrate proper target acquisition and missile seeker employment
- Coordinate air-to-air engagement with defensive maneuvering and countermeasures
- Apply engagement envelope constraints for rotary-wing platforms
- Assess air-to-air missile effectiveness vs. different threat types
- Integrate AAM employment with SPO-15 threat detection

### Mi-24P Air-to-Air Role and Doctrine Limitations

**Primary Role:** Close Air Support and Anti-Tank
- Mi-24P is NOT a dedicated air-to-air fighter
- AAMs are defensive weapons for self-protection only
- Primary threats: Enemy helicopters, slow fixed-wing aircraft
- Avoid engagement with fast jets when possible

**Soviet Doctrine:**
- **Primary Defense:** Terrain masking, low altitude, speed
- **Secondary Defense:** Countermeasures (chaff/flares) + evasive maneuvers  
- **Last Resort:** Air-to-air missile engagement
- **Escape Priority:** Disengage and evade rather than sustain air combat

**Threat Prioritization:**
| Threat Type | Engagement Priority | Recommended Response |
|---|---|---|
| **Fast Jets (F-16, A-10)** | AVOID | Terrain masking + countermeasures + escape |
| **Attack Helicopters** | HIGH | AAM engagement if favorable geometry |
| **Transport Helicopters** | MEDIUM | AAM if mission-critical to engage |
| **Slow Fixed-Wing** | MEDIUM | AAM if they pose immediate threat |
| **MANPADS Teams** | LOW | Cannon/rockets more appropriate |

### R-60 (AA-8 Aphid) System Data

| Specification | Value | Notes |
|---|---|---|
| **NATO Designation** | AA-8 Aphid | Western intelligence designation |
| **Seeker Type** | Infrared homing (IR) | Heat-seeking guidance |
| **Seeker Sensitivity** | All-aspect capability | Can engage from any angle |
| **Warhead** | 3 kg HE fragmentation | Proximity fuze |
| **Warhead Effect** | 7.5m lethal radius | Effective against aircraft |
| **Motor Type** | Single-stage solid rocket | 2.2 second burn time |
| **Weight** | 43.5 kg | Complete missile |
| **Length** | 2.08m | Rail-mounted configuration |
| **Range (Max)** | 8,000m | Ballistic maximum |
| **Range (Effective)** | 500-5,000m | Practical engagement envelope |
| **Speed** | Mach 2.5 | Maximum velocity |
| **G-Limit** | 7G | Maneuver capability |

### R-73 (AA-11 Archer) System Data

| Specification | Value | Notes |
|---|---|---|
| **NATO Designation** | AA-11 Archer | Advanced short-range AAM |
| **Seeker Type** | Infrared imaging | Advanced IR seeker |
| **Seeker Capability** | All-aspect + off-boresight | Can lock targets at angle |
| **Warhead** | 7.4 kg HE fragmentation | Larger than R-60 |
| **Warhead Effect** | 12m lethal radius | Enhanced lethality |
| **Motor Type** | Single-stage solid rocket | 3.5 second burn time |
| **Weight** | 105 kg | Significantly heavier than R-60 |
| **Length** | 2.93m | Longer missile |
| **Range (Max)** | 30,000m | Extended maximum range |
| **Range (Effective)** | 300-15,000m | Much longer than R-60 |
| **Speed** | Mach 2.5+ | High-speed intercept |
| **G-Limit** | 12G | High maneuverability |

### R-60 vs. R-73 Comparison and Selection

| Aspect | R-60 (AA-8) | R-73 (AA-11) | Recommendation |
|---|---|---|---|
| **Best Against** | Helicopters, slow aircraft | All air targets including maneuvering | R-73 for versatility |
| **Range Advantage** | Basic (5km effective) | Extended (15km effective) | R-73 for standoff |
| **Maneuverability** | Good (7G tracking) | Excellent (12G tracking) | R-73 for crossing targets |
| **Seeker Capability** | Standard spinning-reticle IR | Advanced imaging IR (IRCCM) | R-73 for clutter/CM resistance |
| **Off-Boresight** | Minimal (±5°) | Wide (±45° with HMS) | R-73 for snap shots |
| **Weight Impact** | Lower (43.5 kg) | Higher (105 kg) | R-60 for performance retention |
| **Cost/Availability** | More common, cheaper | Less common, expensive | R-60 for training/practice |
| **Flare Resistance** | Low (easily decoyed) | Moderate (IRCCM equipped) | R-73 vs. CM-equipped threats |

**Tactical Selection:**
- **R-60:** Use against helicopters and slow threats; preserve R-73 for serious threats
- **R-73:** Use against fast movers, crossing targets, or when maximum capability needed
- **Mixed Load:** Carry both types for different threat scenarios

### AAM Engagement Envelopes

**R-60 Engagement Parameters:**
| Parameter | Head-On | Beam | Tail Chase | Notes |
|---|---|---|---|---|
| **Minimum Range** | 500m | 800m | 300m | Seeker lock-on distance |
| **Maximum Range** | 5,000m | 3,500m | 8,000m | Practical kill range |
| **Optimum Range** | 1,500-3,000m | 1,000-2,500m | 2,000-5,000m | Highest kill probability |
| **Altitude Floor** | 50m AGL | 100m AGL | 50m AGL | Ground clutter avoidance |
| **Closure Rate** | <600 km/h | Any | <400 km/h | Seeker tracking limits |

**R-73 Engagement Parameters:**
| Parameter | Head-On | Beam | Tail Chase | Notes |
|---|---|---|---|---|
| **Minimum Range** | 300m | 500m | 200m | Advanced seeker capability |
| **Maximum Range** | 12,000m | 8,000m | 15,000m | Extended envelope |
| **Optimum Range** | 2,000-6,000m | 1,500-5,000m | 3,000-10,000m | High kill probability |
| **Off-Boresight** | ±45° | ±60° | ±30° | Lock-on after launch capability |

### DCS Cockpit Procedures (Air-to-Air Employment)

**DCS Key Bindings for AAM Employment:**
| Function | Default Key | Notes |
|---|---|---|
| Select AAM | D (weapon cycle) | Cycle to air-to-air mode |
| Fire Missile | Space | Launch currently selected AAM |
| Seeker Lock / Uncage | — | Check DCS Mi-24P key bindings |
| Pylon Select | W / E (cycle) | Choose missile station |
| Master Arm | See Module 1 | Must be armed |
| Seat Switch (WSO) | 1 | Weapon selection and seeker control |
| Seat Switch (Pilot) | 2 | Maneuvering for engagement |

**R-60/R-73 Engagement Sequence:**

1. **Threat Detection:**
   - SPO-15 RWR: Audio/visual threat indication
   - Visual: Naked eye or binocular acquisition of threat
   - PKV-1: Sight acquisition and identification

2. **Weapon Selection (WSO Seat):**
   - Seat Switch: Press "1" for WSO seat
   - Master Arm: Verify ARMED
   - Weapon Selector: Set to AAM (air-to-air missile)
   - Missile Type: Select R-60 or R-73
   - Pylon Select: Choose loaded pylon

3. **Target Acquisition:**
   - PKV-1: Slew sight onto target aircraft
   - Magnification: 2-4× for target identification
   - Range Estimation: Confirm within missile envelope
   - Aspect Assessment: Determine target heading and speed

4. **Seeker Activation:**
   - Seeker Power: ON (automatic with weapon selection)
   - Seeker Slew: Direct seeker to target bearing
   - Lock Indication: Audio tone + visual symbol
   - Launch Authorization: Verify clear to fire

5. **Launch:**
   - Fire Button: Press when solid lock achieved
   - Missile Departure: 0.5-1.0 second delay
   - Guidance: Missile guides autonomously (fire-and-forget)
   - Maneuver: Aircraft free to maneuver after launch

6. **Post-Launch:**
   - BDA: Assess missile impact/miss
   - Threat Assessment: Continue monitoring for additional threats
   - Escape: Maneuver to avoid counter-fire

### Helicopter vs. Helicopter Air Combat

**Engagement Geometry:**
- **Preferred:** Beam or head-on aspects for R-60/R-73 effectiveness
- **Avoid:** Stern chase unless significant speed advantage
- **Altitude:** Maintain altitude advantage when possible
- **Terrain:** Use terrain masking for approach and escape

**Common Helicopter Threat Scenarios:**
| Threat Aircraft | Typical Tactics | Recommended Response |
|---|---|---|
| **Mi-24/Mi-28 (Enemy)** | Low-level attack runs | R-73 head-on or beam shot |
| **AH-64 Apache** | Standoff ATGM attacks | Close distance, R-73 engagement |
| **AH-1 Cobra** | Pop-up attacks | R-60 beam shot during pop-up |
| **UH-60 Transport** | Low-level insertion | R-60 from any aspect |
| **Ka-50/52 Hokum** | Hovering attacks | R-73 for maneuverability |

**Crew Coordination (Multi-Player):**
- WSO: "Air contact, helicopter, 2 o'clock, 3 kilometers"
- Pilot: "Tally target, maneuvering for shot"
- WSO: "Seeker active, attempting lock"
- WSO: "Seeker lock, firing R-73"
- WSO: "Missile away, breaking right"
- Pilot: "Roger, evading"

### Air-to-Air Integration with Defensive Systems

**SPO-15 RWR Integration:**
- **Threat Detection:** RWR provides bearing to radar-equipped threats
- **Threat Classification:** Identify fighter vs. attack aircraft radar signatures
- **Reaction Time:** SPO-15 warning to AAM launch should be <10 seconds
- **Limitations:** No RWR warning for visual/IR threats

**Countermeasures Coordination:**
- **Pre-Launch:** Dispense flares if IR threat detected
- **During Engagement:** Avoid countermeasures (may decoy own missile)
- **Post-Launch:** Resume countermeasures for defensive purposes
- **Escape Maneuver:** Combine AAM shot with immediate evasive action

### Fast Jet Threat Engagement (Limitations)

**When NOT to Engage Fast Jets:**
- **High Speed Differential:** Closure rate >800 km/h
- **High Altitude:** Fast jet above 3,000m AGL
- **Head-On Attack:** Fast jet in attack dive toward Mi-24P
- **Multiple Threats:** More than one fast jet in area
- **Low Fuel/Ammunition:** Insufficient resources for sustained engagement

**Defensive Priorities vs. Fast Jets:**
1. **Terrain Masking:** Drop to very low altitude (<50m AGL)
2. **Countermeasures:** Continuous flare/chaff dispensing
3. **Evasive Maneuver:** Hard turns, altitude changes
4. **Speed:** Maximum available airspeed for escape
5. **AAM (Last Resort):** Only if no escape option available

### AAM Effectiveness Assessment

**Kill Probability Factors:**
| Factor | R-60 | R-73 | Notes |
|---|---|---|---|
| **Range (Optimum)** | 85% | 90% | Within ideal engagement zone |
| **Range (Maximum)** | 40% | 60% | At extended ranges |
| **Head-On** | 75% | 85% | Good seeker acquisition |
| **Beam** | 65% | 80% | Moderate crossing angle |
| **Tail Chase** | 80% | 85% | Hot target signature |
| **vs. Maneuvering** | 50% | 70% | Target evasive maneuvers |
| **vs. Countermeasures** | 30% | 50% | Flares/chaff employment |

**Target Type vs. Effectiveness:**
| Target | R-60 Effectiveness | R-73 Effectiveness | Notes |
|---|---|---|---|
| **Large Helicopter** | High | High | Strong IR signature |
| **Small Helicopter** | Medium | High | R-73 better seeker |
| **Turboprop Aircraft** | High | High | Hot engine signature |
| **Jet Fighter** | Low | Medium | High speed, countermeasures |
| **Transport Aircraft** | High | High | Large, hot signature |

### Advanced AAM Techniques

**Multiple Target Engagement:**
1. **Priority Target:** Engage most immediate threat first
2. **Quick Re-engagement:** Switch to second missile rapidly
3. **Ammunition Management:** Reserve missiles for highest threats
4. **Escape Planning:** Plan exit after final shot

**Defensive Counter-Air:**
- **Patrol Pattern:** Establish defensive perimeter around friendly assets
- **Early Warning:** Coordinate with ground controllers for threat data
- **Ambush Tactics:** Use terrain masking to achieve surprise
- **Mutual Support:** Work with other helicopters for overlapping coverage

**Off-Boresight Shots (R-73 Only):**
- **Seeker Acquisition:** Lock target outside aircraft nose pointing
- **Launch Envelope:** R-73 can guide to targets ±45° off centerline
- **Technique:** Slew seeker to target, wait for lock, fire immediately
- **Advantage:** No need to maneuver aircraft for firing solution

### Common AAM Employment Errors

| Error | Consequence | Correction |
|---|---|---|
| **Engaging fast jets unnecessarily** | Exposure to superior threats | Evade instead of engage |
| **Firing outside envelope** | Missile miss; waste ammunition | Verify range/aspect before launch |
| **No threat prioritization** | Engage wrong target first | Always engage most immediate threat |
| **Poor escape planning** | Trapped after engagement | Plan exit route before engagement |
| **Inadequate BDA** | Cannot assess engagement success | Track missile to impact |
| **Wrong missile selection** | Suboptimal performance | Match missile to threat type |
| **Firing into ground clutter** | Seeker confusion; missile miss | Maintain altitude separation from ground |
| **Inadequate lock indication** | Premature shot; likely miss | Wait for solid seeker lock |

### Air-to-Air Missile Limitations

**Environmental Factors:**
- **Sun Angle:** Can cause seeker false lock or tracking errors
- **Cloud Cover:** May break seeker lock during missile flight
- **Dust/Haze:** Reduces seeker acquisition range
- **Ground Clutter:** Low-altitude targets may be lost in terrain return

**Platform Limitations:**
- **Mi-24P Speed:** Cannot sustain high-speed air combat
- **Maneuverability:** Limited compared to dedicated fighters
- **Radar:** No airborne radar for beyond-visual-range shots
- **Ammunition:** Limited missile capacity (typically 2-4 total)

**Tactical Limitations:**
- **Primary Mission:** AAM employment may compromise ground attack mission
- **Fuel Consumption:** Air combat burns fuel rapidly
- **Exposure:** Air-to-air engagement increases vulnerability
- **Training:** Mi-24P crews typically have limited air combat training

### Realism Divergences (DCS AAM Implementation)

*⚠ Realism Divergence: R-60 availability on the Mi-24P in DCS may not reflect all real-world sub-variants. Some Mi-24P configurations carried only R-60M (improved) or R-60MK (export). The specific seeker performance and countermeasure resistance depends on the variant modeled. DCS may model a generic R-60 that does not match any specific real-world variant exactly.*

*⚠ Realism Divergence: R-73 off-boresight capability in DCS depends on whether a helmet-mounted sight (HMS) is modeled. Real Mi-24P crews using R-73 typically had the Shchel-3UM HMS for wide-angle target designation. Without HMS, R-73 off-boresight capability is limited to the seeker's own gimbal range. DCS may simplify this by providing off-boresight capability without requiring HMS operation.*

*⚠ Realism Divergence: Real Mi-24P air-to-air engagements are extremely rare in historical combat. The helicopter's AAM capability was primarily a deterrent and emergency self-defense measure. DCS scenarios may feature more frequent air-to-air combat than would occur in real operations. Hit probabilities in DCS may be higher than real-world data suggests, particularly against maneuvering targets employing countermeasures.*

**Simplified Aspects in DCS:**
- IR seeker acquisition is more reliable than real systems (no false locks from sun, terrain)
- Environmental factors (sun angle, cloud cover) may have reduced impact on seeker performance
- Countermeasures effectiveness against R-60 may be under-modeled (real R-60 is very susceptible to flares)
- R-73 IRCCM may be simplified vs. real system's complex flare rejection logic

**Training Value Despite Simplifications:**
- Core engagement principles (envelope, aspect, priority) remain valid
- Threat prioritization and self-defense doctrine are accurately represented
- Crew coordination requirements are realistic
- Decision-making framework (evade vs. engage) is the most important learning outcome

---

## Module 8: SPO-15 Beryoza RWR — Threat Detection & Analysis

### Learning Objectives
- Operate SPO-15 "Beryoza" radar warning receiver system controls
- Interpret RWR display symbols and audio warnings for threat classification
- Apply threat prioritization and response procedures based on RWR indications
- Coordinate RWR threat calls between pilot and WSO crew positions
- Understand RWR limitations and gaps in threat coverage
- Integrate RWR warnings with countermeasures and evasive maneuvers
- Execute threat reaction procedures for different emitter types

### SPO-15 "Beryoza" System Overview

**System Designation and Purpose:**
- **Full Name:** SPO-15 "Beryoza" (Birch Tree)
- **Type:** Radar Warning Receiver (RWR)
- **Function:** Detects and classifies radar emissions from threat systems
- **Coverage:** 360° azimuth, limited elevation coverage
- **Integration:** Interfaces with UV-26 countermeasures system

**Technical Specifications:**
| Parameter | Value | Notes |
|---|---|---|
| **Frequency Range** | 2-18 GHz | Covers most fire-control radars |
| **Azimuth Coverage** | 360° | Full circle coverage |
| **Elevation Coverage** | ±45° typical | Limited above/below aircraft |
| **Range Sensitivity** | 25-150 km | Depends on emitter power |
| **Threat Library** | 50+ emitter types | Soviet/Warsaw Pact primary |
| **Response Time** | <1 second | From detection to display |
| **Power Requirements** | 115V AC, 400Hz | From aircraft electrical system |

### SPO-15 Display and Controls (WSO Front Cockpit)

**DCS Key Bindings for SPO-15 RWR:**
| Function | Default Key | Notes |
|---|---|---|
| SPO-15 Power | — | Check DCS Mi-24P key bindings; typically left panel switch |
| SPO-15 Mode | — | Toggle STANDBY/OPERATE |
| SPO-15 Brightness | — | Rotary control on display bezel |
| Audio Volume | — | Separate from intercom volume |
| Priority Reset | — | Clears current priority threat marker |
| BIT / Test | — | Built-in test; verifies system operation |

*Note: SPO-15 controls in DCS may be mouse-clickable only. Check the specific key binding page for the Mi-24P module for bindable functions.*

**Primary Display:**
- **Type:** Circular CRT display with bearing scale
- **Center:** Aircraft position (nose = top of display)
- **Bearing Scale:** 0° (north) to 360° in 30° increments
- **Threat Symbols:** Alphanumeric codes for different emitter types
- **Threat Rings:** Distance estimation (inner/outer rings)
- **Priority Indicator:** Highest threat highlighted

**WSO Control Panel:**
| Control | Location | Function | Positions |
|---|---|---|---|
| **Master Power** | Left side panel | System power on/off | OFF / ON |
| **Mode Selector** | Below display | Operating mode selection | STANDBY / OPERATE / TEST |
| **Brightness** | Display bezel | CRT brightness control | Variable knob |
| **Audio Volume** | Left panel | Warning tone volume | Variable knob |
| **Priority Reset** | Center panel | Clear priority threat | Momentary button |
| **BIT Switch** | Test panel | Built-in test function | TEST / NORMAL |

**Pilot (Rear Cockpit) Indications:**
- **Audio Only:** Threat warning tones via intercom
- **Caution Light:** General RWR warning light on caution panel
- **No Visual Display:** Pilot relies on WSO for bearing/threat type
- **Crew Coordination:** Essential for threat response

### SPO-15 Threat Library and Symbol Recognition

**Soviet/Russian SAM Systems:**
| Symbol | NATO Name | System | Frequency | Threat Level | Range |
|---|---|---|---|---|---|
| **6** | SA-6 Gainful | Kub (2K12) | I/J-Band | HIGH | 25 km |
| **8** | SA-8 Gecko | Osa (9K33) | H/I-Band | HIGH | 15 km |
| **10** | SA-10 Grumble | S-300P | C-Band | EXTREME | 100+ km |
| **11** | SA-11 Gadfly | Buk (9K37) | H-Band | HIGH | 35 km |
| **13** | SA-13 Gopher | Strela-10 | None | NONE* | 5 km |
| **15** | SA-15 Gauntlet | Tor (9K330) | H/I-Band | HIGH | 12 km |
| **19** | SA-19 Grison | Tunguska | H/I-Band | HIGH | 8 km |

***SA-13 = IR-guided; no radar warning**

**Western/NATO SAM Systems (DCS Scenarios):**
| Symbol | NATO Name | System | Frequency | Threat Level | Range |
|---|---|---|---|---|---|
| **H** | HAWK | MIM-23 HAWK | C/X-Band | HIGH | 40 km |
| **P** | Patriot | MIM-104 Patriot | C-Band | EXTREME | 100+ km |
| **N** | NASAMS | NASAMS | X-Band | HIGH | 25 km |
| **R** | Roland | Roland | Ku-Band | HIGH | 8 km |
| **GP** | Gepard | Gepard SPAAG | Ku-Band | MEDIUM | 5 km |

*Note: SPO-15 threat library in DCS may use different symbols for Western systems than shown above. Learn the DCS-specific symbology through the BIT/test function.*

**Anti-Aircraft Artillery (AAA):**
| Symbol | NATO Name | System | Radar Type | Threat Level | Range |
|---|---|---|---|---|---|
| **S** | Gun Dish | ZSU-23-4 Shilka | Fire control | MEDIUM | 3 km |
| **G** | Flap Wheel | ZSU-57-2 | Search only | LOW | 4 km |
| **A** | Generic AAA | Various | Multiple | MEDIUM | Variable |

*Note: Optically-aimed AAA (ZU-23-2, small arms) provides NO RWR warning*

**Airborne Threats:**
| Symbol | NATO Name | Aircraft Type | Radar | Threat Level | Notes |
|---|---|---|---|---|---|
| **F** | Fighter | Generic | Fire control | HIGH | MiG-21/23/25/29 |
| **I** | Interceptor | Long-range | Search/track | HIGH | MiG-31, Su-27 |
| **A** | Attack | Ground attack | Multi-mode | MEDIUM | Su-25, various |
| **W** | AWACS | Airborne control | Surveillance | LOW | A-50, E-3 |

### Audio Warning System

**Tone Types and Meanings:**
| Tone Pattern | Threat Type | Urgency | Response |
|---|---|---|---|
| **Continuous Low** | Search radar | LOW | Monitor, no immediate action |
| **Intermittent Medium** | Tracking radar | MEDIUM | Prepare countermeasures |
| **Rapid High Beeps** | Fire control radar | HIGH | Immediate evasive action |
| **Warbling Siren** | Missile guidance | EXTREME | Emergency evasion + countermeasures |
| **Single Chirp** | New threat acquisition | INFO | Check display for new symbol |

**Audio Priority System:**
- **Highest Priority:** Missile guidance radars override all other tones
- **Second Priority:** Fire control radars
- **Third Priority:** Tracking radars
- **Lowest Priority:** Search radars
- **Pilot Audio:** Simplified - only high/extreme priority threats

### Threat Prioritization and Response Matrix

**Priority Level 1 (EXTREME - Immediate Action Required):**
| Threat | Symbol | Response | Time Available |
|---|---|---|---|
| **SA-10 (S-300)** | 10 | Terrain masking + countermeasures | 15-30 seconds |
| **Active Missile Guidance** | Various | Emergency evasive maneuver | 5-15 seconds |
| **Fighter Fire Control** | F | Hard break + countermeasures | 10-20 seconds |

**Priority Level 2 (HIGH - Urgent Response):**
| Threat | Symbol | Response | Time Available |
|---|---|---|---|
| **SA-6/8/11/15** | 6/8/11/15 | Evasive maneuver + countermeasures | 30-60 seconds |
| **ZSU-23-4** | S | Low altitude + terrain masking | 15-30 seconds |
| **Fighter Search** | F | Monitor closely, prepare to evade | 60+ seconds |

**Priority Level 3 (MEDIUM - Monitor):**
| Threat | Symbol | Response | Time Available |
|---|---|---|---|
| **Long Range SAM** | Various | Note bearing, continue mission | 2-5 minutes |
| **Search Radars** | Various | Situational awareness only | Continuous |

### Standard Threat Response Procedures

**WSO Threat Call Format:**
"RWR contact, [threat type], [bearing], [priority level]"

**Examples:**
- "RWR contact, SA-6, bearing 030, high priority"
- "RWR contact, ZSU-23, bearing 270, medium priority" 
- "MISSILE GUIDANCE, bearing 045, EXTREME priority"

**Pilot Response Sequence:**
1. **Acknowledge:** "Roger, SA-6, bearing 030"
2. **Assess:** Check terrain masking options
3. **Decide:** Continue mission or evade based on threat level
4. **Execute:** Maneuver/countermeasures as appropriate
5. **Report:** "Maneuvering low, dispensing chaff"

### SPO-15 System Limitations and Blind Spots

**Critical Limitations:**
- **IR-Guided Systems:** No warning for MANPADS (SA-7/9/13/16/18)
- **Optical Systems:** No warning for optically-aimed guns (ZU-23-2)
- **Elevation Limits:** Limited detection above/below aircraft
- **Low Power Emitters:** May not detect some portable systems
- **Frequency Gaps:** Some modern radars outside detection range
- **Electronic Warfare:** Susceptible to jamming and deception

**MANPADS Threat Gap (Critical Awareness):**
| MANPADS Type | Guidance | SPO-15 Warning | Effective Range |
|---|---|---|---|
| **SA-7 (Strela-2)** | IR | NONE | 3.5 km |
| **SA-9 (Strela-1)** | IR | NONE | 5 km |
| **SA-13 (Strela-10)** | IR | NONE | 5 km |
| **SA-16 (Igla-1)** | IR | NONE | 5.2 km |
| **SA-18 (Igla)** | IR | NONE | 5.2 km |

**Tactical Implication:** Most immediate helicopter threats provide NO RWR warning!

### Terrain Masking and Evasive Techniques

**Terrain Masking Principles:**
- **Objective:** Break line-of-sight between threat radar and aircraft
- **Technique:** Fly below ridgelines, behind hills, in valleys
- **Altitude:** As low as safely possible (15-50m AGL)
- **Speed:** Maintain maximum safe speed during masking

**Evasive Maneuver Types:**
| Maneuver | Application | Technique | Effectiveness |
|---|---|---|---|
| **Terrain Masking** | Long-range SAMs | Fly below radar horizon | Excellent |
| **Notching** | Doppler radars | 90° turn to radar beam | Good |
| **Chaff Corridor** | Radar-guided missiles | Straight line + chaff | Good |
| **Hard Break** | Incoming missile | >4G turn + dive | Variable |
| **Altitude Change** | Tracking radars | Rapid climb/dive | Moderate |

### Integration with UV-26 Countermeasures

**Automatic Dispense (If Available):**
- **Trigger:** High priority RWR warning
- **Pattern:** Pre-programmed chaff/flare sequence
- **Override:** Manual control available
- **Coordination:** WSO manages both systems

**Manual Countermeasures:**
- **Chaff:** Effective against radar-guided threats
- **Flares:** Limited effectiveness (RWR threats typically radar)
- **Timing:** Dispense on RWR warning, not after missile launch
- **Quantity:** Preserve countermeasures for highest threats

### RWR Tactical Employment

**Pre-Mission Planning:**
- **Threat Assessment:** Study known SAM/AAA positions
- **Route Planning:** Avoid known high-threat areas
- **Ingress/Egress:** Plan routes using terrain masking
- **Countermeasures:** Load appropriate chaff/flare mix

**In-Flight Procedures:**
- **Continuous Monitoring:** WSO monitors RWR throughout mission
- **Threat Updates:** Report new/changed threats to pilot
- **Mission Modification:** Alter plan based on actual threat picture
- **Coordination:** Share threat data with other aircraft

**Mission Abort Criteria:**
- **SA-10/S-300:** Immediate abort unless terrain masking available
- **Multiple High Threats:** 3+ high priority simultaneous contacts
- **Fire Control Lock:** Sustained tracking by fire control radar
- **Missile Launch:** Any missile guidance indication

### Advanced RWR Techniques

**Threat Classification:**
- **Emitter Identification:** Match symbol to actual threat system
- **Range Estimation:** Use signal strength and ring position
- **Multiple Emitters:** Prioritize most immediate threats
- **False Alarms:** Distinguish real threats from spurious signals

**Electronic Warfare Awareness:**
- **Jamming Indications:** Unusual display behavior or loss of threats
- **Deception:** False threat symbols or bearing errors
- **Countermeasures:** Electronic attack against RWR system
- **Backup Procedures:** Visual confirmation when RWR unreliable

### Common RWR Interpretation Errors

| Error | Consequence | Correction |
|---|---|---|
| **Ignoring low-priority threats** | Threat escalation goes unnoticed | Monitor all contacts continuously |
| **Over-reacting to distant threats** | Mission disruption, fuel waste | Assess actual threat vs. mission risk |
| **Confusing symbols** | Wrong response to threat type | Memorize symbol meanings thoroughly |
| **Poor crew coordination** | Pilot unaware of threat changes | Standard threat call procedures |
| **Forgetting RWR limitations** | Surprise by IR/optical threats | Maintain visual scanning always |
| **Inadequate response time** | Delayed reaction to high threats | Pre-brief response procedures |
| **Misreading bearing** | Wrong direction for evasive maneuver | Double-check bearing before maneuvering |

### RWR Training and Proficiency

**Simulator Training:**
- **Threat Library:** Learn all symbol meanings
- **Response Drills:** Practice immediate action procedures
- **Crew Coordination:** Standardize threat call procedures
- **Scenario Training:** Multiple threat, complex environments

**Flight Training:**
- **Benign Environment:** Basic RWR operation and controls
- **Simulated Threats:** Training with ground-based emitters
- **Live Threats:** Actual SAM/AAA sites (with safety deconfliction)
- **Electronic Warfare:** Training in jamming/deception environment

### Realism Divergences (DCS SPO-15 Implementation)

*⚠ Realism Divergence: The real SPO-15 Beryoza CRT display is significantly harder to read than the DCS representation. Real CRT displays suffer from washout in bright lighting, phosphor persistence creating ghost images, and analog noise. DCS provides a cleaner, more readable display that makes threat identification easier than real-world operations.*

*⚠ Realism Divergence: The real SPO-15 threat library is limited to approximately 50 emitter types, primarily Soviet/Warsaw Pact and common NATO systems of the 1970s-1980s era. Modern SAM systems (SA-15 Tor, Patriot PAC-3, NASAMS) may not be in the real SPO-15 library but are often represented in DCS for gameplay purposes. The real system would display unknown emitters as generic symbols.*

*⚠ Realism Divergence: SPO-15 range estimation in DCS may be more accurate than the real system. Real RWRs provide only rough range estimation based on signal strength, which varies with emitter power settings, atmospheric conditions, and antenna orientation. DCS may provide consistent, reliable range rings that give students unrealistic confidence in threat distance assessment.*

*⚠ Realism Divergence: Real SPO-15 suffers from false alarms caused by friendly radar emissions, civilian signals, and multipath reflections. DCS typically does not model these nuisance signals, which in real operations can cause alert fatigue and delayed response to genuine threats.*

**Training Value Despite Simplifications:**
- Core threat detection and classification principles are accurate
- Symbol recognition training transfers to real-world operations
- Crew coordination procedures are the most critical learning outcome
- Tactical response concepts (masking, notching, evasion) are fully valid
- System limitation awareness (IR/optical gaps) is critical and well-represented

---

## Module 9: UV-26 Countermeasures — Chaff & Flares

### Learning Objectives
- Operate UV-26 countermeasures dispenser system controls and programming
- Select appropriate countermeasures (chaff vs. flares) for different threat types
- Execute manual and automatic dispense procedures coordinated with threat warnings
- Apply countermeasures employment techniques with evasive maneuvering
- Assess countermeasures effectiveness and adjust employment tactics
- Coordinate countermeasures between pilot and WSO crew positions
- Integrate UV-26 employment with SPO-15 threat detection and mission planning

### UV-26 Countermeasures System Overview

**System Designation:**
- **Full Name:** UV-26 Countermeasures Dispenser System
- **Type:** Chaff and flare dispenser for self-defense
- **Purpose:** Defeat radar and infrared guided missiles/weapons
- **Integration:** Interfaces with SPO-15 RWR for automatic operation
- **Capacity:** Variable cartridge load (mission-configurable)

**Physical Configuration:**
| Component | Location | Function | Notes |
|---|---|---|---|
| **Dispenser Units** | Fuselage sides/tail boom | Houses cartridge tubes | Multiple units (2-4 dispensers) |
| **Control Panel** | WSO front cockpit, left side | Programming and manual control | Primary interface |
| **Pilot Controls** | Rear cockpit, left panel | Emergency manual dispense | Limited: single press only |
| **Cartridge Types** | Loaded pre-flight | Chaff (RR-129), flares (PPI-26), or mixed | Ground crew configurable per mission |

### UV-26 Technical Specifications

| Parameter | Value | Notes |
|---|---|---|
| **Total Capacity** | 60+ cartridges typical | Varies by configuration |
| **Chaff Cartridges** | RR-129 type | Radar frequency coverage |
| **Flare Cartridges** | PPI-26 type | IR spectrum coverage |
| **Dispense Rate** | 1-8 cartridges/second | Programmable |
| **Sequencing** | Multiple patterns available | Pre-programmed or manual |
| **Response Time** | <0.5 seconds | From command to dispense |
| **Cartridge Weight** | ~0.5 kg each | Affects aircraft performance |

### Chaff vs. Flares — Threat Application

**Chaff (RR-129) Employment:**
| Threat Type | Effectiveness | Application | Notes |
|---|---|---|---|
| **Radar SAMs** | High | SA-6, SA-8, SA-11, SA-15 | Primary radar countermeasure |
| **Radar AAA** | High | ZSU-23-4 Shilka, SA-19 Tunguska | Fire control radar disruption |
| **Fighter Radars** | Medium | Air-to-air radar missiles | Must combine with maneuver |
| **Search Radars** | Low | Early warning / surveillance | Limited tactical value |
| **IR Threats** | None | MANPADS, IR AAM | Chaff completely ineffective |

**Flares (PPI-26) Employment:**
| Threat Type | Effectiveness | Application | Notes |
|---|---|---|---|
| **MANPADS** | High | SA-7, SA-9, SA-13, SA-16, SA-18 | Primary IR countermeasure |
| **IR Air-to-Air** | High | R-60, R-73, AIM-9 | Essential for survival |
| **Advanced IR Seekers** | Medium | Modern MANPADS with IRCCM | Multiple flares required |
| **Radar Threats** | None | SA-6, SA-8, SA-11, etc. | Flares completely ineffective |
| **Optical/Visual** | None | Optically-aimed guns | No decoy effect |

**Critical Understanding:** Wrong countermeasures type = zero effectiveness!

### UV-26 Control Panel (WSO Front Cockpit)

**DCS Key Bindings for UV-26 Countermeasures:**
| Function | Default Key | Notes |
|---|---|---|
| Dispense Chaff | — | Check DCS Mi-24P key bindings |
| Dispense Flare | Q (common default) | Often bound to HOTAS for fast access |
| Countermeasures Release (both) | — | May fire current program |
| CM Program Select | — | Cycle through programs 1-5 |
| CM Mode (Auto/Semi/Manual) | — | Panel switch in WSO cockpit |
| Emergency Jettison (all) | — | Hold for 3+ seconds |

*Note: Binding chaff and flare dispense to separate HOTAS buttons is strongly recommended for rapid threat-appropriate response.*

**Primary Controls:**
| Control | Function | Settings | Operation |
|---|---|---|---|
| **Master Power** | System on/off | OFF/ON | Toggle switch |
| **Mode Selector** | Operating mode | AUTO/SEMI/MANUAL | 3-position switch |
| **Program Selector** | Dispense pattern | 1/2/3/4/5 | Pre-configured programs |
| **Quantity Select** | Cartridges per burst | 1/2/4/8 | Burst size |
| **Interval Select** | Time between bursts | 0.5/1.0/2.0/4.0 sec | Spacing control |
| **Chaff Button** | Manual chaff dispense | Momentary | Single or burst |
| **Flare Button** | Manual flare dispense | Momentary | Single or burst |
| **Emergency Dispense** | Dump all stores | Hold 3+ seconds | Emergency only |

**Mode Descriptions:**
- **AUTO:** System responds automatically to SPO-15 high-priority threats
- **SEMI-AUTO:** Manual initiation, automatic sequencing per program
- **MANUAL:** Complete manual control of all dispense functions

### Pilot (Rear Cockpit) Countermeasures Controls

**Available Controls:**
| Control | Function | Capability | Limitations |
|---|---|---|---|
| **Chaff Button** | Single chaff dispense | Immediate response | Single cartridge only |
| **Flare Button** | Single flare dispense | Immediate response | Single cartridge only |
| **Mode Override** | Emergency manual mode | Bypasses WSO control | Emergency use only |

**Crew Coordination:**
- **Normal Operations:** WSO manages all countermeasures
- **Emergency:** Pilot can override for immediate response
- **Communication:** Clear calls for countermeasures employment
- **Backup:** Pilot ready to take over if WSO incapacitated

### Pre-Programmed Dispense Patterns

**Program 1 — Radar SAM Response:**
- **Pattern:** 4 chaff, 0.5 sec interval, single burst
- **Application:** SA-6/SA-8 missile launch
- **Duration:** 2 seconds total
- **Follow-up:** Manual assessment and additional bursts

**Program 2 — IR Missile Response:**
- **Pattern:** 6 flares, 0.5 sec interval, continuous
- **Application:** MANPADS launch detection
- **Duration:** 3 seconds initial, repeats every 2 seconds
- **Follow-up:** Continues until manual stop

**Program 3 — Mixed Threat:**
- **Pattern:** 2 chaff + 2 flares, 1.0 sec interval
- **Application:** Unknown or mixed threat environment
- **Duration:** 4 seconds per cycle
- **Follow-up:** Assess threat type and switch to appropriate program

**Program 4 — Area Defense:**
- **Pattern:** Continuous mixed dispense
- **Application:** Transit through high-threat area
- **Duration:** Continuous until stopped or ammunition exhausted
- **Follow-up:** Monitor ammunition remaining

**Program 5 — Combat Emergency:**
- **Pattern:** Maximum rate mixed dispense
- **Application:** Multiple simultaneous threats
- **Duration:** Rapid ammunition expenditure
- **Follow-up:** Emergency egress procedures

### Countermeasures Employment Techniques

#### 1. Preventive Dispensing

**Application:** High-threat area transit
- **Technique:** Continuous low-rate dispense
- **Pattern:** 1 chaff + 1 flare every 10-15 seconds
- **Advantage:** Creates protective "cloud" around aircraft
- **Disadvantage:** Rapid ammunition consumption
- **Decision Factors:** Threat density, mission duration, ammunition available

#### 2. Reactive Dispensing

**Application:** Specific threat response
- **Trigger:** SPO-15 warning or visual missile sighting
- **Technique:** Immediate appropriate countermeasures + evasive maneuver
- **Pattern:** Threat-specific program selection
- **Timing:** <2 seconds from threat detection to countermeasures

#### 3. Defensive Maneuvering Integration

**Chaff Employment with Evasive Action:**
1. **Initial Dispense:** 4-6 chaff cartridges immediately
2. **Turn Into Chaff:** Hard turn toward chaff cloud
3. **Additional Chaff:** Continue dispensing during turn
4. **Altitude Change:** Climb or dive to separate from chaff cloud
5. **Assessment:** Monitor SPO-15 for radar lock break

**Flare Employment with Evasive Action:**
1. **Flare Dispense:** 6-8 flares immediately
2. **Turn Away:** Turn away from heat source (sun, ground)
3. **Altitude Change:** Dive toward cooler background
4. **Additional Flares:** Continue dispensing throughout maneuver
5. **Cool Aircraft:** Reduce power if tactically feasible

### Threat-Specific Employment Procedures

**SA-6/SA-8 (Radar SAM) Response:**
1. **SPO-15 Warning:** High-priority radar threat
2. **Immediate:** Program 1 (4 chaff, 0.5 sec interval)
3. **Maneuver:** Hard turn + dive toward terrain
4. **Additional:** Continue chaff every 3-4 seconds
5. **Assessment:** Monitor RWR for guidance radar break

**MANPADS (IR) Response:**
1. **Visual Detection:** Missile launch flash or smoke trail
2. **Immediate:** Program 2 (6 flares, continuous)
3. **Maneuver:** Hard turn + dive away from heat source
4. **Additional:** Continue flares until missile impact/miss
5. **Assessment:** Visual confirmation of missile fate

**Fighter Engagement:**
1. **RWR/Visual:** Fighter fire control radar or visual contact
2. **Mixed Response:** Program 3 (chaff + flares)
3. **Evasive Action:** Terrain masking + maximum performance maneuver
4. **Sustain:** Continue countermeasures throughout engagement
5. **Escape:** Disengage at first opportunity

### Ammunition Management and Conservation

**Typical Loadout:**
- **Total Cartridges:** 60 (example configuration)
- **Chaff:** 36 cartridges (60%)
- **Flares:** 24 cartridges (40%)
- **Mixed Programs:** Adjust ratio based on threat assessment

**Conservation Techniques:**
| Phase | Technique | Rationale |
|---|---|---|
| **Ingress** | Minimal preventive | Save ammunition for target area |
| **Target Area** | Responsive only | Use when actually threatened |
| **Egress** | Preventive acceptable | Priority is getting home safely |
| **Emergency** | Use all available | Survival over conservation |

**Ammunition Tracking:**
- **WSO Responsibility:** Monitor remaining cartridge count
- **Display:** Remaining count on UV-26 panel
- **Crew Coordination:** Call remaining count to pilot
- **Decision Point:** Reserve minimum 10 cartridges for egress

### Advanced Countermeasures Techniques

**Corridor Tactics:**
- **Technique:** Create chaff/flare corridor along flight path
- **Application:** Penetrating heavy SAM environment
- **Execution:** Continuous dispensing + straight-line flight
- **Effectiveness:** High vs. multiple radar threats
- **Cost:** Rapid ammunition expenditure

**Notching with Chaff:**
- **Technique:** 90° turn into chaff cloud
- **Application:** Doppler radar defeat (SA-11, fighter radars)
- **Timing:** Turn must occur while chaff is effective
- **Effectiveness:** Very high vs. pulse-Doppler systems
- **Follow-up:** Maintain perpendicular heading briefly

**Heat Source Masking:**
- **Technique:** Flare dispensing while maneuvering toward cool background
- **Application:** IR missile defeat
- **Background:** Terrain, shadows, cool sky
- **Timing:** Coordinate flares with aircraft cooling (reduced power)
- **Effectiveness:** High vs. older IR seekers

### Environmental Factors Affecting Countermeasures

**Weather Effects:**
| Condition | Chaff Effect | Flare Effect | Countermeasures |
|---|---|---|---|
| **High Winds** | Rapid dispersion | Rapid dispersion | Increase dispense rate |
| **Rain** | Reduced effectiveness | Reduced effectiveness | Increase quantity |
| **Low Clouds** | Neutral | Background masking | Use terrain + flares |
| **Clear Skies** | Good effectiveness | Hot aircraft vs. cold sky | Maneuver toward terrain |
| **Dust/Haze** | Enhanced persistence | Reduced visibility | Mixed technique |

**Time of Day:**
- **Daylight:** Flares less effective vs. modern IR seekers
- **Dusk/Dawn:** Thermal gradient advantages
- **Night:** Flares more effective; aircraft cooler vs. ground
- **Hot Day:** IR threats more effective; more flares required

### Common Countermeasures Employment Errors

| Error | Consequence | Correction |
|---|---|---|
| **Wrong countermeasures type** | Zero effectiveness vs. threat | Match countermeasures to threat guidance |
| **Too late employment** | Missile inside minimum deflection range | Dispense immediately on threat detection |
| **Inadequate quantity** | Insufficient decoy density | Use programmed bursts, not single cartridges |
| **Poor maneuver coordination** | Aircraft flies away from countermeasures | Coordinate maneuver to use countermeasures effectively |
| **Excessive conservation** | Inadequate response to real threats | Better to waste than to be shot down |
| **No ammunition tracking** | Run out when most needed | Monitor count continuously |
| **Panic dispensing** | Waste all ammunition quickly | Disciplined employment per threat type |
| **Ignoring environmental factors** | Reduced effectiveness | Adjust technique for conditions |

### UV-26 System Malfunctions and Backup Procedures

**Common Malfunctions:**
| Malfunction | Symptoms | Backup Procedure |
|---|---|---|
| **Program failure** | No automatic dispense | Switch to MANUAL mode |
| **Dispenser jam** | Some cartridges not dispensing | Use functioning dispensers only |
| **Control panel failure** | No panel response | Use pilot emergency controls |
| **Cartridge misfire** | Reduced dispense count | Increase burst size |
| **Power failure** | No system operation | Check electrical system, use manual backup |

**Emergency Procedures:**
1. **Total System Failure:** Rely entirely on evasive maneuvering and terrain masking
2. **Partial Failure:** Use functioning components with increased effectiveness requirements
3. **Low Ammunition:** Prioritize highest threats, conserve for egress
4. **Jamming/Degradation:** Increase dispense rate to compensate

### Integration with Mission Planning

**Pre-Flight Considerations:**
- **Threat Assessment:** Radar vs. IR threat predominance
- **Loadout Selection:** Adjust chaff/flare ratio accordingly
- **Route Planning:** High-threat areas require more countermeasures
- **Weather:** Account for environmental effects on effectiveness
- **Backup Plans:** Alternative routes if countermeasures fail

**In-Flight Adaptation:**
- **Threat Changes:** Modify employment based on actual vs. planned threats
- **Ammunition Status:** Adjust tactics based on remaining countermeasures
- **System Degradation:** Account for malfunctions in tactical decisions
- **Crew Coordination:** Ensure both crew members aware of countermeasures status

### Countermeasures vs. Stealth Philosophy

**Soviet/Russian Approach:**
- **Philosophy:** Penetrate defenses with speed, countermeasures, and tactics
- **Assumptions:** Enemy will detect aircraft; survival depends on defeating weapons
- **Tactics:** Active countermeasures + aggressive maneuvering
- **Training:** Emphasis on countermeasures employment and evasive action

**Western Comparison:**
- **Stealth First:** Avoid detection through signature reduction
- **Countermeasures Secondary:** Backup for when stealth fails
- **Different Training:** Emphasis on signature management and routing

**Mi-24P Application:**
- **No Stealth Capability:** Large, hot, radar-reflective helicopter
- **Countermeasures Critical:** Primary defense against guided weapons
- **Tactics Essential:** Must use terrain, speed, and countermeasures for survival

### Realism Divergences (DCS UV-26 Implementation)

*⚠ Realism Divergence: DCS countermeasures effectiveness is typically more predictable than real-world employment. Real chaff and flare effectiveness varies dramatically based on atmospheric conditions, threat seeker sophistication, dispensing geometry relative to the threat, and timing. DCS uses simplified models that generally make countermeasures more reliable than they are in reality.*

*⚠ Realism Divergence: Real PPI-26 flares have specific burn time, temperature, and spectral characteristics that may or may not match the threat missile's seeker discrimination algorithms. Modern MANPADS (SA-18, Stinger) have improved flare rejection capabilities that DCS may not fully model. Students should not assume flares will always defeat IR threats.*

*⚠ Realism Divergence: The UV-26 programming interface in DCS is simplified. The real system requires pre-flight programming of dispense patterns using a somewhat cumbersome Soviet control panel. DCS may allow easier in-flight program changes than the real system permits. Additionally, real UV-26 cartridge reliability is approximately 95%, meaning occasional misfires — DCS does not model individual cartridge failures.*

**Training Value Despite Simplifications:**
- Correct countermeasures type for threat type is the most critical lesson — fully valid in DCS
- Crew coordination requirements are realistic
- Ammunition management discipline is important and well-represented
- Integration with evasive maneuvering is essential and accurately modeled
- The principle of reactive vs. preventive dispensing is valid

---

## Module 10: Close Combat Attack (CCA) Tactics — Mi-24P Employment

### Learning Objectives
- Apply Soviet attack helicopter doctrine principles in DCS Mi-24P employment
- Execute coordinated approach, attack, and egress profiles for different mission types
- Demonstrate target prioritization and engagement sequencing in complex scenarios
- Coordinate formation tactics and mutual support techniques with other aircraft
- Integrate threat reaction procedures into attack profiles and mission planning
- Assess mission effectiveness and apply lessons learned to subsequent operations
- Apply crew resource management principles during high-workload combat operations

### Soviet Attack Helicopter Doctrine Overview

**Mi-24P Role in Soviet Military:**
- **Primary Mission:** Close Air Support (CAS) for ground forces
- **Secondary Mission:** Anti-tank operations in main battle area
- **Employment Philosophy:** Mass employment in coordinated attacks
- **Tactical Unit:** Pair (2 aircraft) or flight (4 aircraft) formations
- **Survival Concept:** Speed and firepower over stealth and precision

**Soviet vs. Western Helicopter Tactics:**
| Aspect | Soviet (Mi-24P) | Western (AH-64) | Implications |
|---|---|---|---|
| **Approach** | High speed, low altitude | Standoff precision | Mi-24 accepts higher risk |
| **Attack Profile** | Fast diving/running attacks | Hover and shoot | Mi-24 minimizes exposure time |
| **Weapons** | Volume fire (rockets/cannon) | Precision (ATGM primary) | Different ammunition management |
| **Survivability** | Speed + countermeasures | Stealth + precision | Different threat responses |
| **Formation** | Close coordination | Independent operations | Higher crew coordination demands |

**Soviet Threat Environment Assumptions:**
- **Air Defenses:** Dense, overlapping SAM and AAA coverage
- **Maneuver:** Rapidly changing ground situation
- **Support:** Limited close air support; helicopter must be self-sufficient
- **Navigation:** GPS not available; visual/inertial navigation primary

### Attack Mission Planning and Preparation

**Mission Analysis Process:**
1. **Threat Assessment:** Identify known/suspected air defense positions
2. **Target Analysis:** Primary, secondary, and opportunity target identification
3. **Route Planning:** Ingress/egress routes using terrain masking
4. **Weapons Selection:** Loadout optimization for target types and threat environment
5. **Fuel Planning:** Combat radius with reserves for extended combat
6. **Contingency Planning:** Alternate targets, abort criteria, emergency procedures

**Intelligence Requirements:**
| Intelligence Type | Critical Information | Source | Reliability |
|---|---|---|---|
| **SEAD** | SAM/AAA positions and status | Electronic intel, reconnaissance | Medium-High |
| **Target** | Location, description, priority | Ground forces, aviation | High |
| **Weather** | Visibility, winds, ceiling | Meteorology | High |
| **Friendly Forces** | Position, planned movements | Ground coordination | High |
| **Enemy Activity** | Movement, reinforcements | Multiple sources | Variable |

**Loadout Selection by Mission Type:**
| Mission Type | Primary Weapons | Secondary Weapons | Rationale |
|---|---|---|---|
| **Anti-Armor** | 4×Ataka, 2×B-8V20A | 250 rds cannon | Maximum ATGM capability |
| **Close Support** | 4×B-8V20A, 250 rds cannon | — | Volume fire against mixed targets |
| **SEAD** | 4×B-8V20A, 250 rds cannon | — | Suppress AAA sites |
| **Reconnaissance** | 2×B-8V20A, 250 rds cannon | 2×R-60 | Self-defense priority |
| **Mixed/Flexible** | 2×Ataka, 2×B-8V20A, 2×R-60 | 250 rds cannon | Versatile loadout |

### Tactical Approach Profiles

#### 1. Low-Level Ingress (Primary Method)

**Profile Parameters:**
- **Altitude:** 15-50m AGL (Nap-Of-Earth)
- **Airspeed:** 220-260 km/h
- **Terrain Usage:** Valleys, behind ridgelines, urban areas
- **Formation:** Line abreast or trail, 500-1000m separation

**Execution:**
1. **Route Selection:** Use terrain features to mask approach
2. **Navigation:** Visual pilotage with map/GPS backup
3. **Threat Monitoring:** Continuous RWR monitoring
4. **Communication:** Minimal radio use; pre-briefed checkpoints
5. **Formation:** Maintain visual contact with wingman
6. **Target Area:** Arrive at planned initial point (IP) on time/altitude

#### 2. High-Low Profile

**Application:** Long-range approach over benign territory
- **High Phase:** 500-1500m AGL at cruise speed
- **Transition:** Descend to low level 10-15 km from target
- **Low Phase:** As above for final approach

#### 3. Pop-Up Attack Profile

**Application:** Targets beyond terrain masking
- **Approach:** Low level to firing position
- **Pop-Up:** Climb to 200-600m for line-of-sight
- **Attack:** Weapon employment at altitude
- **Dive:** Immediate return to low level

### Target Area Tactics

**Target Prioritization (Standard Sequence):**
1. **Air Defense Assets:** SAMs, AAA that threaten own aircraft
2. **Command and Control:** Command posts, communications
3. **Anti-Tank Systems:** AT missiles, AT guns threatening friendly armor
4. **Direct Fire Systems:** Tanks, IFVs engaging friendly forces
5. **Indirect Fire:** Artillery, mortars supporting enemy
6. **Logistics:** Supply vehicles, fuel, ammunition
7. **Personnel:** Infantry, support troops

**Search and Acquisition:**
- **Initial Search:** Naked eye from 2-4 km standoff
- **PKV-1 Confirmation:** Positive target identification before engagement
- **Range Estimation:** Confirm within weapon envelope
- **Threat Assessment:** Verify no immediate air defense threat to engagement
- **Attack Authorization:** Clear with ground controller if applicable

### Attack Execution Profiles

#### 1. Diving Attack (Primary for Precision)

**Profile Geometry:**
- **Entry Altitude:** 800-1500m AGL
- **Dive Angle:** 20-30° typical
- **Entry Speed:** 220-260 km/h
- **Weapon Release:** 800-2000m range (weapon dependent)
- **Break-off:** 400-600m range
- **Recovery:** 100m+ AGL minimum

**Execution Steps:**
1. **Setup:** Approach target area at entry altitude
2. **Identify:** Locate and identify target through PKV-1
3. **Roll-in:** Bank toward target, reduce power
4. **Dive:** Establish dive angle and stabilize airspeed
5. **Track:** PKV-1 or CCIP on target
6. **Fire:** Weapon release at appropriate range
7. **Break:** Pull up and maneuver for next target or egress

#### 2. Running Attack (High Threat Areas)

**Profile Parameters:**
- **Altitude:** 50-200m AGL
- **Speed:** Maximum safe (260+ km/h)
- **Track:** Straight line across target area
- **Exposure:** Minimum time over target

**Advantages:**
- Minimum exposure time to ground threats
- High survivability in dense air defense environment
- Suitable for area targets requiring volume fire

**Disadvantages:**
- Reduced accuracy vs. diving attack
- Limited opportunity for precise target identification
- Single pass only (no re-engagement)

#### 3. Multiple Attack Runs

**Application:** Multiple targets or re-engagement required
- **First Pass:** Highest priority target
- **Egress/Re-position:** Brief departure from target area
- **Re-engagement:** Different axis of attack for second run
- **Ammunition Management:** Reserve weapons for subsequent passes

### Formation Tactics and Coordination

**Two-Ship (Pair) Formation:**
- **Lead Responsibilities:** Navigation, target identification, first attack
- **Wingman Responsibilities:** Formation, threat warning, follow-up attack
- **Attack Sequence:** Lead attacks while wingman covers; roles may reverse
- **Mutual Support:** Overwatching, threat calls, damage assessment

**Standard Formation Calls:**
| Situation | Lead Call | Wingman Response | Action |
|---|---|---|---|
| **Target Identified** | "Lead has target, tank, 2 o'clock" | "Two has target" | Wingman confirms |
| **Commencing Attack** | "Lead in hot" | "Two covering" | Lead attacks, wingman overwatches |
| **Weapon Away** | "Lead off target, left" | "Two in hot" | Wingman begins attack |
| **Threat Warning** | "Flak, 10 o'clock" | "Two breaking left" | Both aircraft evade |
| **Abort/RTB** | "Lead aborting, fuel" | "Two following" | Formation egress |

**Four-Ship (Flight) Tactics:**
- **Element Structure:** Two 2-ship elements
- **Lead Element:** Primary attack responsibility
- **Trail Element:** Overwatch, follow-up, threat suppression
- **Coordination:** More complex; requires experienced flight lead

### Threat Reaction During Attack

**SAM/AAA Response:**
1. **SPO-15 Warning:** Immediate threat assessment
2. **Evasive Action:** Hard turn toward terrain masking
3. **Countermeasures:** Appropriate chaff/flare employment
4. **Altitude:** Dive to minimum safe altitude
5. **Abort Decision:** Based on threat level and mission criticality

**Air Threat Response:**
1. **Visual/RWR Contact:** Identify threat type and bearing
2. **Threat Call:** Inform wingman of air threat
3. **Defensive Maneuver:** Hard turn, dive, terrain masking
4. **Countermeasures:** Chaff/flares as appropriate
5. **Engagement:** AAM employment only if unavoidable

**Ground Fire Response:**
1. **Muzzle Flashes:** Visual identification of small arms/AAA
2. **Evasive Action:** Jinking flight, altitude/heading changes
3. **Suppression:** Return fire with cannon/rockets if possible
4. **Displacement:** Move to different attack axis

### Crew Resource Management (CRM) in Combat

**Single-Player Seat Management:**
- **Planning Phase:** Setup all weapons systems from WSO seat
- **Approach:** Pilot seat for navigation and formation flying
- **Target Acquisition:** WSO seat for PKV-1 operation and target ID
- **ATGM Employment:** WSO seat for SACLOS guidance
- **Cannon/Rockets:** Pilot seat for attack maneuvering
- **Post-Attack:** WSO seat for BDA and next weapon selection

**Multi-Player Crew Coordination:**
- **WSO Primary:** Target acquisition, identification, weapons management
- **Pilot Primary:** Aircraft control, navigation, formation flying, threat avoidance
- **Shared:** Threat detection, mission planning, damage assessment
- **Communication:** Continuous coordination throughout mission

**High-Workload Management:**
| Situation | Priority Actions | Secondary Actions | Crew Division |
|---|---|---|---|
| **Multiple Targets** | Engage highest threat first | Plan engagement sequence | WSO: targeting; Pilot: maneuvering |
| **Under Fire** | Evasive maneuver + countermeasures | Return suppressive fire | Pilot: evasion; WSO: countermeasures |
| **System Failure** | Continue mission with degraded capability | Troubleshoot if time permits | Both: adapt procedures |
| **Fuel Emergency** | Direct route to recovery base | Jettison stores if required | Pilot: navigation; WSO: fuel management |

### Post-Attack Procedures and Egress

**Battle Damage Assessment (BDA):**
- **Immediate:** Visual assessment through PKV-1 during break maneuver
- **Extended:** Overfly target area from safe distance/altitude
- **Reporting:** Standard BDA report to controlling agency
- **Re-engagement:** Decision based on target status and ammunition remaining

**Egress Planning:**
- **Route Selection:** Different from ingress route when possible
- **Altitude:** Low level until clear of threat area
- **Speed:** Maximum safe speed initially, cruise for fuel conservation
- **Formation:** Maintain mutual support throughout egress
- **Navigation:** Direct routing with threat avoidance

**Emergency Egress:**
- **Immediate Threat:** Maximum performance escape regardless of fuel
- **System Failure:** Adjust egress profile for degraded capability
- **Combat Damage:** Formation support for damaged aircraft
- **Fuel Emergency:** Direct routing to nearest suitable airfield

### Mission Types and Specific Tactics

#### Close Air Support (CAS)

**Coordination Requirements:**
- **Ground Controller:** Forward Air Controller (FAC) or Joint Terminal Attack Controller (JTAC)
- **Target Marking:** Smoke, laser designation, or detailed verbal description
- **Friendly Forces:** Confirm positions to avoid fratricide
- **Clearance:** Positive clearance required before each attack

**CAS Attack Sequence:**
1. **Check-In:** Report to ground controller with capabilities
2. **Target Brief:** Receive target description, location, restrictions
3. **Target Acquisition:** "Tally target" call when visually acquired
4. **Attack Clearance:** "Cleared hot" from controller
5. **Attack Execution:** Weapon employment per briefed parameters
6. **BDA Report:** Report results to controller

#### Anti-Tank Mission

**Target Priorities:**
1. **Main Battle Tanks:** Primary threat to friendly armor
2. **IFVs/APCs:** Secondary armored threats
3. **AT Missile Systems:** Long-range anti-tank threats
4. **Command Vehicles:** Coordination and control elements

**ATGM Employment Considerations:**
- **Standoff Range:** Use maximum Ataka/Shturm range for survivability
- **Multiple Targets:** Plan engagement sequence by priority and geometry
- **Platform Stability:** Coordinate with pilot for steady SACLOS guidance
- **Re-engagement:** Time for multiple shots vs. threat response time

#### SEAD (Suppression of Enemy Air Defenses)

**Target Classification:**
- **Immediate:** Air defense systems actively engaging friendly aircraft
- **Planned:** Known air defense positions requiring neutralization
- **Opportunity:** Air defense systems discovered during mission

**SEAD Weapons Employment:**
- **Cannon:** Most effective against AAA crews and optical equipment
- **Rockets:** Area suppression of SAM sites and gun positions
- **ATGM:** Precision engagement of high-value radar/missile systems

### Advanced CCA Techniques

**Multiple Axis Attack:**
- **Technique:** Attack same target from different directions
- **Advantage:** Prevents enemy from concentrating defensive fire
- **Coordination:** Requires precise timing and communication
- **Application:** High-value, heavily defended targets

**Decoy and Suppress:**
- **Technique:** One aircraft draws fire while another attacks
- **Roles:** Decoy aircraft uses countermeasures and evasion; attack aircraft engages
- **Application:** Dense air defense environments
- **Risk:** High risk to decoy aircraft

**Sequential Target Engagement:**
- **Technique:** Systematic engagement of multiple targets
- **Planning:** Pre-briefed target sequence and weapon allocation
- **Flexibility:** Adapt to changing tactical situation
- **Ammunition Management:** Reserve capability for highest priority targets

### Lessons Learned and Tactical Development

**Common Tactical Errors:**
| Error | Consequence | Correction |
|---|---|---|
| **Predictable attack patterns** | Enemy adaptation, increased losses | Vary approach/attack profiles |
| **Inadequate threat assessment** | Surprise by air defenses | Thorough intelligence preparation |
| **Poor crew coordination** | Reduced effectiveness, safety issues | Standardize procedures, practice |
| **Target fixation** | Miss other threats or targets | Maintain situational awareness |
| **Ammunition waste** | Unable to complete mission | Disciplined weapons employment |
| **Poor egress planning** | Trapped in threat area | Plan egress before attack |

**Training Progression:**
1. **Individual Proficiency:** Single aircraft, basic attack profiles
2. **Formation Basics:** Two-ship coordination and communication
3. **Threat Integration:** Training with simulated air defenses
4. **Mission Integration:** Combined arms training with ground forces
5. **Advanced Tactics:** Complex scenarios with multiple threats/targets

### Realism Considerations

*⚠ Realism Divergence: DCS AI ground units behave differently from real-world opponents. AI air defenses have predictable engagement patterns, consistent reaction times, and limited tactical adaptation. Real air defense crews adapt to observed attack patterns, vary engagement profiles, and employ passive defense measures (camouflage, decoys, emission control) that DCS AI does not replicate.*

*⚠ Realism Divergence: DCS provides significantly better situational awareness than real helicopter combat. The external view, perfect weather forecasts, and ability to pause/replay missions do not exist in reality. Real helicopter CCA operations are conducted in the "fog of war" with incomplete intelligence, communication disruption, and extreme stress — factors that DCS cannot replicate.*

*⚠ Realism Divergence: Soviet attack helicopter doctrine emphasized mass employment (squadron-level attacks with 8-24 aircraft) and centralized command and control through dedicated helicopter coordination centers. DCS scenarios typically involve 1-4 aircraft operating semi-independently, which is not representative of real Soviet employment doctrine. Students should be aware that the tactics practiced in DCS are simplified versions of actual combined-arms operations.*

**Training Value Despite DCS Limitations:**
- Tactical principles (approach profiles, target prioritization, threat reaction) are fully valid
- Crew coordination procedures and communication standards are transferable
- Mission planning process and considerations are realistic
- The decision-making framework (engage vs. evade, target priority, ammunition management) is the most valuable learning outcome

### DCS Mission Editor — Building CCA Training Scenarios

**Purpose:** Use the DCS Mission Editor to build progressive CCA training scenarios that develop skills from basic to advanced employment. This section provides templates for instructor-created training missions.

**Mission Editor Setup Basics:**
1. **Map Selection:** Choose terrain appropriate for helicopter operations (valleys, ridgelines, open areas for targets)
2. **Weather:** Start with clear weather for basic training; add adverse conditions for advanced scenarios
3. **Time of Day:** Begin with daylight; progress to dusk/dawn for advanced scenarios
4. **Difficulty Settings:** Adjust AI skill levels to match student proficiency

**Progressive Training Mission Templates:**

**Scenario 1 — Basic Weapons Delivery (Introductory):**
| Element | Configuration | Purpose |
|---|---|---|
| **Targets** | 4-6 soft vehicles (trucks, fuel trucks) stationary in open | Practice basic attack profiles |
| **Threats** | None | Focus on weapons delivery technique |
| **Loadout** | B-8V20A rockets + cannon | Volume fire practice |
| **Objectives** | Destroy all targets with >50% accuracy | Establish baseline proficiency |
| **Mission Editor Notes** | Place targets in visible locations; mark with smoke triggers | Easy target acquisition |

**Scenario 2 — Weapons Selection (Intermediate):**
| Element | Configuration | Purpose |
|---|---|---|
| **Targets** | Mixed: 2 tanks, 4 APCs, 4 trucks, 1 bunker | Weapon-to-target matching |
| **Threats** | 1-2 ZU-23-2 (optical AAA) | Introduce suppression fire requirement |
| **Loadout** | ATGM + B-8V20A + cannon | Full weapons suite |
| **Objectives** | Match correct weapon to each target type | Decision-making under time pressure |
| **Mission Editor Notes** | Spread targets across 2-3 km area; AAA protecting high-value targets | Force prioritization |

**Scenario 3 — Threat Environment (Advanced):**
| Element | Configuration | Purpose |
|---|---|---|
| **Targets** | 3-4 armored vehicles + artillery battery | High-value target engagement |
| **Threats** | SA-8 Osa + ZSU-23-4 Shilka + MANPADS teams | Full air defense threat |
| **Loadout** | 4×Ataka + B-8V20A + cannon + full countermeasures | Full combat loadout |
| **Objectives** | Destroy priority targets, survive all threats | Integrated weapons + defensive employment |
| **Mission Editor Notes** | Vary AI skill; place threats to force route planning; add trigger zones for threat activation | Test planning and reaction |

**Scenario 4 — Combined Arms CCA (Expert):**
| Element | Configuration | Purpose |
|---|---|---|
| **Targets** | Armored column (tanks, IFVs, command vehicles) moving on road | Moving target engagement |
| **Threats** | SA-11 Buk (long-range) + Tunguska (SHORAD) + MANPADS screen | Layered air defense |
| **Friendly Forces** | Friendly armor requiring CAS | Fratricide avoidance |
| **Loadout** | Mission-dependent (student selects) | Loadout planning test |
| **Objectives** | Support friendly advance, suppress air defense, destroy armor | Full mission planning and execution |
| **Mission Editor Notes** | Use waypoints for moving columns; trigger-based SEAD activation; require student to communicate with ground FAC | Complex scenario management |

**Mission Editor Tips for Instructors:**
- **Triggers:** Use trigger zones to activate threats when students enter engagement area (prevents AI from engaging too early)
- **Scoring:** Use condition triggers to track target destruction and student survival
- **Waypoints:** Set AI unit waypoints for moving targets; vary speeds for difficulty
- **FARP Placement:** Include forward arming and refueling points for multi-sortie training
- **Wingman AI:** Set AI wingman skill to "Excellent" for formation practice; "Average" for independent operations
- **Radio Frequencies:** Configure ground FAC radio for CAS coordination practice
- **Debriefing:** Use the DCS track recorder for post-mission analysis and after-action review

**Recommended Training Progression:**
| Stage | Scenarios | Focus Area | Mastery Criteria |
|---|---|---|---|
| **Stage 1** | Scenario 1 × 3 missions | Basic weapons delivery | >60% accuracy, safe recovery |
| **Stage 2** | Scenario 2 × 3 missions | Weapon-target matching | Correct weapon for each target type |
| **Stage 3** | Scenario 3 × 5 missions | Threat integration | Survive all threats, destroy priority targets |
| **Stage 4** | Scenario 4 × 5 missions | Combined arms | Mission success with no fratricide |

---

## Module 11: Weapons Loading, Weight & Performance Considerations

### Learning Objectives
- Calculate aircraft performance limitations based on weapons loadout and fuel state
- Select optimal loadout configurations for different mission types and conditions
- Execute emergency jettison procedures for various scenarios and loadout configurations
- Assess center of gravity effects and handling characteristics with different loadouts
- Apply weight and balance principles to mission planning and fuel management
- Coordinate ground crew for proper weapons loading and aircraft configuration
- Integrate performance limitations into tactical planning and execution

### Mi-24P Weight and Balance Fundamentals

**Basic Weight Categories:**
| Component | Weight (kg) | Notes |
|---|---|---|
| **Empty Weight** | 8,500 kg | Standard aircraft without fuel/stores |
| **Crew** | 180 kg | 2 crew members + equipment |
| **Fuel (Maximum)** | 1,851 kg | Internal fuel tanks full |
| **Weapons (Maximum)** | 2,400 kg | Maximum external stores load |
| **Maximum Takeoff Weight** | 12,000 kg | Normal operations limit |
| **Emergency Overload** | 12,500 kg | Emergency operations only |

**Center of Gravity Envelope:**
- **Forward Limit:** 23% Mean Aerodynamic Chord (MAC)
- **Aft Limit:** 31% MAC
- **Lateral Limits:** ±3% of fuselage width
- **CG Shift:** Fuel consumption and stores jettison affect balance

### Performance Impact of External Stores

**Hover Performance (Out of Ground Effect):**
| Gross Weight | Hover Ceiling (Standard Day) | Notes |
|---|---|---|
| **9,000 kg** | 2,400 m | Light configuration |
| **10,000 kg** | 1,800 m | Typical combat weight |
| **11,000 kg** | 1,200 m | Heavy combat load |
| **12,000 kg** | 600 m | Maximum weight |

**Forward Flight Performance:**
| Configuration | VNE (km/h) | Service Ceiling (m) | Range (km) |
|---|---|---|---|
| **Clean** | 335 | 4,500 | 450 |
| **Light Combat** | 310 | 4,200 | 420 |
| **Heavy Combat** | 280 | 3,800 | 380 |
| **Maximum Load** | 250 | 3,200 | 320 |

*Performance data assumes standard atmospheric conditions*

### Standard Loadout Configurations

#### Configuration 1: Anti-Armor (Maximum ATGM)

**Loadout:**
- Station 1: 2×Ataka (84 kg)
- Station 2: B-8V20A + 20×S-8 (252 kg)
- Station 3: B-8V20A + 20×S-8 (252 kg)
- Station 4: 2×Ataka (84 kg)
- **Total Stores:** 672 kg
- **Fuel Recommended:** 1,200 kg (combat radius consideration)

**Performance Impact:**
- **Hover OGE:** 1,400m (standard day)
- **VNE:** 295 km/h
- **Range:** 380 km combat radius
- **Handling:** Slight nose-heavy tendency

#### Configuration 2: Close Support (Maximum Rockets)

**Loadout:**
- Station 1: B-8V20A + 20×S-8 (252 kg)
- Station 2: B-8V20A + 20×S-8 (252 kg)
- Station 3: B-8V20A + 20×S-8 (252 kg)
- Station 4: B-8V20A + 20×S-8 (252 kg)
- **Total Stores:** 1,008 kg
- **Fuel Recommended:** 1,000 kg

**Performance Impact:**
- **Hover OGE:** 1,100m
- **VNE:** 285 km/h
- **Range:** 350 km combat radius
- **Handling:** Balanced, predictable

#### Configuration 3: Heavy Support (Maximum Effect)

**Loadout:**
- Station 1: S-24 (235 kg)
- Station 2: B-13L + 5×S-13 (435 kg)
- Station 3: B-13L + 5×S-13 (435 kg)
- Station 4: S-24 (235 kg)
- **Total Stores:** 1,340 kg
- **Fuel Recommended:** 900 kg

**Performance Impact:**
- **Hover OGE:** 900m
- **VNE:** 270 km/h
- **Range:** 300 km combat radius
- **Handling:** Heavy, reduced agility

#### Configuration 4: Self-Defense (Air Threat Environment)

**Loadout:**
- Station 1: 2×Ataka (84 kg)
- Station 2: 2×R-60 + B-8V20A (295 kg)
- Station 3: 2×R-60 + B-8V20A (295 kg)
- Station 4: 2×Ataka (84 kg)
- **Total Stores:** 758 kg
- **Fuel Recommended:** 1,300 kg

**Performance Impact:**
- **Hover OGE:** 1,350m
- **VNE:** 290 km/h
- **Range:** 400 km combat radius
- **Handling:** Good performance retention for air combat

### Weight Distribution and Handling Effects

**Longitudinal Balance:**
| Loading Pattern | CG Effect | Handling Characteristics |
|---|---|---|
| **Forward Heavy** | Nose down tendency | Stable but heavy on cyclic |
| **Aft Heavy** | Tail down tendency | Unstable, requires attention |
| **Balanced** | Neutral | Normal handling qualities |

**Lateral Balance:**
- **Asymmetric Loading:** Causes roll tendency requiring trim compensation
- **Single-Side Failures:** Jettison may create significant imbalance
- **Formation Flying:** Lateral imbalance affects formation position keeping

### Emergency Jettison Procedures

**Total Emergency Jettison:**
1. **Master Arm:** SAFE (prevent accidental weapon firing)
2. **Emergency Jettison Cover:** Lift cover on WSO panel
3. **Jettison Button:** Press and hold for 3+ seconds
4. **Verification:** Visual confirmation all stores separated
5. **CG Adjustment:** Trim aircraft for new balance point
6. **Performance:** Recalculate performance with new weight

**Selective Jettison by Priority:**

**Jettison Priority 1 (Emergency Performance):**
- S-24 rockets (235 kg each) — heaviest individual items
- Fuel tanks (if external tanks installed)
- B-13L pods (435 kg each) — heavy rocket pods

**Jettison Priority 2 (Combat Damage):**
- Damaged/malfunctioning systems
- Stores creating asymmetric loading
- Stores preventing normal flight control

**Jettison Priority 3 (Mission Abort):**
- Unused ordnance per Rules of Engagement
- Retain minimum self-defense capability (cannon ammunition, some AAMs)

### Common Weight and Balance Errors

| Error | Consequence | Prevention |
|---|---|---|
| **Exceeding weight limits** | Reduced performance, safety risk | Careful mission planning with weight worksheet |
| **Poor CG management** | Handling difficulties, aft CG instability | Systematic loading procedures; balance heavy stores |
| **Inadequate fuel planning** | Mission abort, emergency landing | Conservative fuel calculations; 15-minute reserve minimum |
| **Improper jettison sequencing** | CG problems, asymmetric loading | Practice emergency procedures; jettison heavy stores first |
| **Ignoring environmental factors** | Performance shortfall at altitude/temperature | Apply DA/PA corrections to all performance data |
| **Asymmetric loading** | Roll tendency, increased pilot workload | Always load symmetrically; if asymmetric, limit to ±100 kg difference |
| **Not accounting for cannon ammo weight** | CG shift as ammunition depletes | 250 rounds ≈ 75 kg; forward CG shift during firing |

### Arming and De-Arming Procedures (Real-World Context for Realism Awareness)

**Purpose:** This section describes real-world weapons arming/de-arming procedures that are not fully modeled in DCS but are important for understanding the complete weapons employment cycle. Awareness of these procedures enhances realism appreciation and informs proper DCS mission setup.

**Real-World Pre-Flight Arming (Ground Crew):**

| Step | Action | Responsible | Safety Requirement |
|---|---|---|---|
| 1 | Aircraft power OFF, all switches safe | Pilot confirmation | Master Arm SAFE, weapons switches OFF |
| 2 | Ground crew approaches aircraft | Weapons technician (armorer) | Fire extinguisher positioned nearby |
| 3 | Install safety pins/flags on all stores | Armorer | Red "REMOVE BEFORE FLIGHT" streamers visible |
| 4 | Physically mount stores on stations | Armorer + loader | Verify mechanical locks engaged |
| 5 | Connect electrical umbilicals | Armorer | Continuity check per store |
| 6 | Verify fuze settings (bombs, rockets) | Armorer | Match weapon fuze to ordered settings |
| 7 | Remove safety pins/flags last | Armorer | Count pins; verify against manifest |
| 8 | Final inspection — walk-around | Armorer + pilot | Visual check all stations |
| 9 | Aircraft power ON for system test | Pilot/WSO | Verify all stores displayed correctly |

**Real-World Post-Mission De-Arming (Ground Crew):**

| Step | Action | Responsible | Safety Requirement |
|---|---|---|---|
| 1 | Aircraft in designated de-arming area | Pilot | Clear of other aircraft/personnel |
| 2 | Master Arm → SAFE | Pilot | Verify both cockpits safe |
| 3 | All weapons switches → OFF | WSO | Verify no active circuits |
| 4 | Aircraft power → OFF | Pilot | Complete electrical isolation |
| 5 | Ground crew approaches | Armorer | 5-minute wait after shutdown for hot stores |
| 6 | Install safety pins on ALL remaining stores | Armorer | Even partially expended pods |
| 7 | Inspect for hung ordnance / misfires | Armorer | Extreme caution — treat as live |
| 8 | Report ammunition expenditure | WSO/armorer | Rounds/missiles expended count |
| 9 | Download remaining stores if required | Armorer | Reverse of loading procedure |

**Hung Ordnance / Misfire Procedures:**
- **Hung ordnance** = weapon that failed to release when commanded
- **Misfire** = weapon that failed to fire when trigger/fire button pressed
- **DO NOT** attempt to cycle or re-fire a hung/misfired weapon in the arming area
- Wait minimum 5 minutes before ground crew approach
- Armorer approaches from side, installs safety pin first
- Hung ordnance may require explosive ordnance disposal (EOD) team

**Safety Zones (Real-World):**
| Zone | Radius | Personnel Allowed | Purpose |
|---|---|---|---|
| **Arming Area** | 100m clear zone | Arming crew only | Weapons hot operations |
| **De-Arming Area** | 100m clear zone | De-arming crew only | Weapons safe-ing |
| **Parking Area** | 50m between aircraft | Ground crew | Normal operations with safed weapons |
| **Ammunition Storage** | 500m+ from aircraft | Authorized personnel | Munitions handling |

*⚠ Realism Divergence: DCS does not model real-world arming/de-arming procedures, safety zones, or ground crew operations. Weapons are immediately available when loaded in the Mission Editor. Students should understand that real-world weapons handling involves extensive safety procedures, multiple qualified personnel, and significant time overhead that DCS omits entirely. A real Mi-24P weapons turnaround (land, de-arm, rearm, arm) takes 20-45 minutes with a trained ground crew — not the 30-second DCS FARP rearm cycle.*

### DCS-Specific Module 11 Notes

**DCS Weapons Loading:**
- Weapons are configured in the Mission Editor during mission setup
- In-mission rearming occurs at FARPs or airbases via the ground crew menu
- DCS FARP rearm: land at designated FARP, wait for rearm timer
- All weight/balance calculations are handled automatically by DCS flight model
- DCS does model performance degradation with increased weapon load

**DCS Performance Considerations:**
- Verify actual DCS Mi-24P performance numbers by testing in-game (may differ from published specs)
- DCS flight model may be more or less forgiving than real aircraft at maximum weight
- Hot-and-high performance penalties may be simplified in DCS
- Engine limitations (torque, temperature) are modeled but may be less restrictive than real aircraft

### Realism Divergences (DCS Weight & Performance)

*⚠ Realism Divergence: DCS does not model real-world density altitude effects as precisely as actual flight. Real Mi-24P performance degrades dramatically at high altitude and hot temperatures — operations above 1,500m density altitude require significant weight reduction that may not be apparent in DCS. Students should always plan for worst-case performance when creating realistic scenarios.*

*⚠ Realism Divergence: The DCS FARP rearming system is vastly simplified compared to real forward arming and refueling operations. Real FARP operations require ground crew, ammunition transport, physical loading, arming, and safety checks — a process that takes 20-45 minutes minimum. DCS represents this as a timer-based automatic process.*

---

## Appendix A: Weapons Quick Reference Card

### Master Weapons Table

| Weapon | Range | Warhead | Best Targets | Employment Notes |
|---|---|---|---|---|
| **GSh-30K Cannon** | 400-1,500m | 30mm APHE/HE-Frag | Light armor, soft targets, AAA | Fixed mount; pilot-aimed; 250 rds |
| **9M114 Shturm** | 400-5,000m | HEAT (600+ mm RHAe) | MBTs, IFVs, bunkers | SACLOS; 15 sec flight to max range |
| **9M120 Ataka** | 400-6,000m | HEAT (800+ mm) / Thermobaric | Heavy armor, bunkers, infantry | SACLOS; 12 sec flight to max range |
| **S-5 Rockets** | 300-1,800m | HE-Frag/HEAT/Flechette | Soft targets, infantry, light vehicles | 16 or 32-round pods; area fire |
| **S-8 Rockets** | 500-2,000m | HE-Frag/HEAT/Tandem | Mixed targets, light armor | 20-round pods; CCIP |
| **S-13 Rockets** | 800-2,500m | HE penetrator (1m concrete) | Bunkers, hardened shelters, bridges | 5-round pods; heavy recoil |
| **S-24 Rockets** | 1,500-4,000m | HE blast (123 kg warhead) | Hardened targets, structures | Single rocket; manual aim |
| **FAB-100/250/500** | Release altitude dependent | HE blast (46/100/213 kg fill) | Structures, area targets | If available in DCS; CCIP/manual |
| **RBK-250/500** | Release altitude dependent | Cluster (submunitions) | Area targets, dispersed vehicles | If available in DCS |
| **KMGU-2** | Release altitude dependent | Submunition dispenser | Runways, area denial, soft targets | If available in DCS |
| **R-60 AAM** | 500-5,000m | HE-Frag (3.5 kg) | Helicopters, slow aircraft | IR seeker; rear-aspect preferred |
| **R-73 AAM** | 300-15,000m | HE-Frag (7.4 kg) | All air targets | Advanced IR; ±45° off-boresight |

### Employment Envelopes Summary

| Weapon | Min Range | Optimal Range | Max Range | Speed (km/h) | Dive Angle | Platform Requirements |
|---|---|---|---|---|---|---|
| **GSh-30K** | 400m | 800-1,200m | 1,500m | 200-280 | 10-20° | Diving attack preferred |
| **Shturm** | 400m | 1,500-4,000m | 5,000m | 100-180 | Level | Steady flight 10-15 sec |
| **Ataka** | 400m | 2,000-5,000m | 6,000m | 100-200 | Level | Steady flight 8-12 sec |
| **S-5** | 300m | 800-1,200m | 1,800m | 200-280 | 5-15° | Shallow dive, area fire |
| **S-8** | 500m | 1,000-1,500m | 2,000m | 220-300 | 10-20° | CCIP diving attack |
| **S-13** | 800m | 1,500-2,000m | 2,500m | 250-320 | 15-30° | Firm diving attack |
| **S-24** | 1,500m | 2,000-3,000m | 4,000m | 250-320 | 10-20° | Stable platform, manual aim |
| **R-60** | 500m | 1,500-3,000m | 5,000m | Any | Any | Tone + uncage before launch |
| **R-73** | 300m | 2,000-8,000m | 15,000m | Any | Any | Advanced seeker auto-track |

### Weapon-to-Target Matching Quick Reference

| Target Type | Primary Weapon | Secondary Weapon | Notes |
|---|---|---|---|
| **MBT (T-72, M1, Leo2)** | Ataka HEAT | Shturm HEAT | Top attack if possible |
| **IFV/APC (BMP, BTR, M2)** | Shturm | S-8 HEAT / Cannon | Multiple hits with S-8 |
| **Truck / Soft Vehicle** | Cannon / S-5 | S-8 HE-Frag | Conserve ATGMs |
| **Infantry in Open** | S-5 Flechette / Cannon | S-8 HE-Frag | Area saturation |
| **Infantry in Buildings** | S-13 / Ataka Thermobaric | S-24 | Penetration + blast |
| **Bunker / Hardened Target** | S-13 | S-24 / Ataka | Penetrator warheads |
| **Artillery Battery** | S-8 (salvo) | S-5 (mass fire) | Suppress then destroy |
| **SAM Site** | Ataka (standoff) | S-24 (if range allows) | Prioritize radar vehicle |
| **AAA (ZSU, ZU-23)** | Cannon (suppression) | S-8 / Ataka | Suppress before team attacks |
| **Helicopter** | R-60 / R-73 | Cannon | Guns if missile unavailable |
| **Fixed-Wing Aircraft** | R-73 | R-60 | Defensive engagement only |

---

## Appendix B: Crew Coordination Quick Reference

### Standard Crew Calls

**Target Acquisition:**
- WSO: "Target identified, [type] at [bearing], [range]"
- Pilot: "Tally target" or "No joy"
- WSO: "Marking target" (designating in PKV-1)

**Weapons Employment:**
- WSO: "Ready to fire [weapon]"
- Pilot: "Cleared to engage" or "Hold fire"
- WSO: "Firing [weapon]"
- WSO: "Missile away, guiding" (ATGM specific)
- WSO: "Impact, [BDA]" or "Miss [direction]"

**Threat Warnings:**
- WSO: "RWR contact, [type], bearing [###]"
- WSO: "MISSILE LAUNCH, [bearing]" → immediate evasion
- Either: "FLAK/AAA, [bearing]"
- Either: "MANPADS, [bearing], [direction]"
- Either: "BREAK [left/right]" — immediate maximum performance turn

**Countermeasures:**
- WSO: "Dispensing chaff" / "Dispensing flares"
- WSO: "Countermeasures program [#], executing"
- WSO: "Countermeasures LOW" — 25% remaining
- WSO: "Countermeasures OUT" — empty

**Navigation/Situation:**
- Pilot: "Feet dry" / "Feet wet" (crossing land/water boundary)
- Pilot: "FARP in sight, requesting rearm"
- Pilot: "Bingo fuel" — minimum fuel for RTB
- WSO: "Ammunition state: [cannon rounds], [ATGMs], [rockets]"

### Single-Player Seat Switching Guide (DCS)

**Default Seat-Switch Key:** `1` (Pilot) / `2` (WSO) — *verify in DCS key bindings*

**Mission Phase → Recommended Seat:**
| Phase | Seat | Reason |
|---|---|---|
| Pre-flight / Startup | Pilot | Systems startup |
| Weapons arming / config | WSO | Weapons panel access |
| Takeoff / Transit | Pilot | Aircraft control |
| Ingress / Threat assessment | WSO | RWR monitoring, PKV-1 scan |
| ATGM engagement | WSO | SACLOS guidance required |
| Rocket / Cannon attack | Pilot | Maneuvering + fixed-gun aiming |
| Air-to-air engagement | WSO | Seeker management, launch authority |
| Defensive (missile evasion) | WSO | Countermeasures dispensing |
| Post-attack / BDA | WSO | BDA assessment, next target |
| RTB / Landing | Pilot | Aircraft control |

**Seat-Switching Tips:**
- Avoid switching during active ATGM guidance — missile will go ballistic
- Set autopilot before switching seats to prevent loss of control
- Confirm weapon state immediately after switching to WSO seat
- In emergencies, stay in pilot seat — survival takes priority over weapons

---

## Appendix C: Threat / Countermeasures Matrix

### Threat Response Guide

| Threat Type | Threat Level | Primary Response | Countermeasures | Maneuver | Time Available |
|---|---|---|---|---|---|
| **SA-6 Gainful** | HIGH | Terrain masking | Chaff + hard turn | Dive to low level | 30-60 sec |
| **SA-8 Gecko** | HIGH | Terrain masking | Chaff + jinking | NOE escape | 15-30 sec |
| **SA-11 Buk** | EXTREME | Immediate terrain masking | Chaff + max performance | NOE + terrain break | 15-40 sec |
| **SA-15 Tor** | EXTREME | Terrain masking | Chaff + hard maneuver | Immediate NOE | 10-25 sec |
| **Tunguska** | HIGH | Standoff / terrain | Chaff + flares | Break + low level | 10-20 sec |
| **ZSU-23-4 Shilka** | MEDIUM | Terrain masking | Chaff | NOE + jink | 15-30 sec |
| **MANPADS (Igla/Stinger)** | HIGH | Evasive + flares | Continuous flare program | Hard turn + dive | 5-15 sec |
| **HAWK** | HIGH | Terrain masking | Chaff + hard maneuver | Break + NOE | 20-40 sec |
| **Roland** | MEDIUM-HIGH | Terrain masking | Chaff + jinking | NOE escape | 15-25 sec |
| **Gepard / Vulcan** | MEDIUM | Standoff range | None effective | Jink + terrain | 10-20 sec |
| **Fighter aircraft** | HIGH | Terrain + speed | Chaff + flares | Max performance turn | 20-45 sec |
| **Attack helicopter** | MEDIUM | Terrain masking | Flares (if IR missile) | Terrain interposition | 15-30 sec |
| **Small arms / HMG** | LOW | Altitude + speed | None effective | Climb + accelerate | 5-10 sec |

### RWR Symbol Quick Reference (SPO-15 Beryoza)

| Symbol | System | Type | Threat Level | Immediate Response |
|---|---|---|---|---|
| **2** | SA-2 Guideline | SAM (radar) | HIGH | Terrain masking, chaff |
| **3** | SA-3 Goa | SAM (radar) | HIGH | Terrain masking, chaff |
| **6** | SA-6 Gainful | SAM (radar) | HIGH | Immediate evasion, chaff |
| **8** | SA-8 Gecko | SAM (radar) | HIGH | Terrain masking, chaff |
| **11** | SA-11 Buk | SAM (radar) | EXTREME | Emergency evasion, chaff |
| **15** | SA-15 Tor | SAM (radar) | EXTREME | Emergency evasion, chaff |
| **S** | ZSU-23-4 Shilka | AAA (radar) | MEDIUM | Low altitude, chaff |
| **H** | HAWK | SAM (radar) | HIGH | Terrain masking, chaff |
| **R** | Roland | SAM (radar) | MEDIUM-HIGH | Terrain masking, chaff |
| **F** | Fighter radar | Air-to-air | HIGH | Defensive maneuver, chaff + flares |
| **10** | SA-10 Grumble | SAM (radar) | EXTREME | Emergency evasion (unlikely to survive) |

*Note: SPO-15 cannot detect IR-only threats (MANPADS, R-60/R-73). Visual lookout is the only defense against IR threats.*

### Countermeasures Program Reference (UV-26)

| Program | Chaff | Flares | Interval | Use Against |
|---|---|---|---|---|
| **1 (Default)** | 1 | 1 | 1.0 sec | Unknown / mixed threat |
| **2 (Radar SAM)** | 2 | 0 | 0.5 sec | SA-6, SA-8, SA-11 |
| **3 (IR Missile)** | 0 | 2 | 0.5 sec | MANPADS, IR AAM |
| **4 (Dense Threat)** | 2 | 2 | 0.3 sec | Multiple simultaneous threats |
| **Manual** | 1 | 0 or 0/1 | On demand | Selective response, conservation |

*Programs may vary by DCS version — verify in countermeasures setup panel.*

---

**Footer Disclaimer:**
*This research dossier is based on DCS World Mi-24P Hind module by Eagle Dynamics and real-world Soviet/Russian military documentation. Information is compiled for training purposes in the DCS simulation environment. Real-world procedures may differ significantly. For simulation use only.*
