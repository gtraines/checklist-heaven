# Event 2 — PKV-1 Sight Operations & Target Acquisition

> **Course:** Mi-24P Hind Weapons Qualification Course | **Event Type:** Ground/Simulation
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [PKV-1 System Overview](#pkv-1-system-overview)
4. [PKV-1 Controls](#pkv-1-controls)
5. [Weapon Mode Reticles](#weapon-mode-reticles)
6. [Laser Rangefinder](#laser-rangefinder)
7. [Target Acquisition Techniques](#target-acquisition-techniques)
8. [Range Estimation](#range-estimation)
9. [Target Acquisition Sequence](#target-acquisition-sequence)
10. [Battle Damage Assessment](#battle-damage-assessment)
11. [DCS-Specific Tips](#dcs-specific-tips)
12. [Common Errors](#common-errors)
13. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Power up and verify PKV-1 gyrostabilized sight in the correct sequence
- [ ] Operate PKV-1 slew, zoom, mode selection, and cage/uncage controls
- [ ] Identify the correct reticle for each weapon mode (cannon, rockets, ATGM, AAM)
- [ ] Execute a systematic naked-eye-to-PKV target acquisition sequence
- [ ] Use visual/mil-dot range estimation to estimate target range within ±500 m
- [ ] Operate the laser rangefinder (if modeled in DCS) for accurate range data
- [ ] Conduct battle damage assessment through the PKV-1 after weapon impact
- [ ] Apply correct PKV-1 procedures for different environmental conditions

---

## Ground Brief

### What the PKV-1 Is — and Is Not

The PKV-1 is the WSO's primary targeting tool, but understanding its limitations prevents overconfidence:

| Capability | Detail |
|---|---|
| **Optical/Daytime only** | No thermal, no FLIR — entirely dependent on visible light |
| **Fixed to cockpit** | Gyrostabilized but limited gimbal travel (±45° azimuth) |
| **No fire control computer** | No automatic target tracking, no ballistic computer integration for ATGM |
| **WSO-only** | The pilot has no equivalent sight — the WSO is the crew's only eyes-on-target |
| **No night capability** | At night the sight is black — no NVG, no IR, nothing |

The PKV-1 fundamentally defines the Mi-24P's employment: **daylight, visual range, pilot maneuvers the weapon platform, WSO guides the missile.** Every weapon employment in this course flows from PKV-1 target acquisition.

### Why This Event Comes First

No weapons event works without PKV-1 proficiency. Poor sight technique causes:
- Missed target acquisitions (long search times = less time on station)
- Wrong range estimates → wrong weapon selection → missed engagements
- ATGM guidance loss → expensive missile wasted
- Inadequate BDA → re-engagement of already-destroyed targets

---

## PKV-1 System Overview

| Specification | Value | Notes |
|---|---|---|
| **Type** | Collimating, gyrostabilized optical sight | Daytime optical only — no thermal/FLIR |
| **Location** | WSO front cockpit, forward of instrument panel | Periscope-style viewing head; WSO looks through eyepiece |
| **Stabilization** | Pitch and yaw gyrostabilization (dual-axis) | Compensates for aircraft movement during flight |
| **Field of View** | ~6° (narrow) / ~18° (wide) | Narrow FOV at maximum zoom |
| **Magnification** | 1× to 8× (variable, continuous) | Controlled via zoom lever on sight head |
| **Reticle** | Weapon-specific graticules (illuminated) | Different patterns for cannon, rockets, ATGM, AAM |
| **Slew Limits** | ±45° azimuth, +20° / −60° elevation | Hard stops at gimbal limits |
| **Slew Rate** | ~15°/second (manual joystick) | Bind to analog axis for best control |
| **Power Source** | AC 115V, 400 Hz from main inverter | Gyro spin-up required before use |

---

## PKV-1 Controls

### Power-On & Alignment Sequence

1. **Pre-Power Checks (WSO seat — `1`):**
   - Verify PKV-1 protective covers removed (external view `F2`)
   - Confirm AC inverter operating (instrument panel indicator)
   - Locate PKV-1 power switch — left side panel near sight head

2. **Power-On:**
   - PKV-1 Power Switch → **ON**
   - Wait 2–3 minutes for gyro stabilization in real ops (DCS: near-immediate)
   - Test elevation and azimuth movement — smooth, no binding

3. **Boresight Verification:**
   - Pilot: Point aircraft at known reference 1–2 km distant
   - WSO: Center PKV-1 on same reference point
   - Verify sight aligns with aircraft heading within 2°

> *⚠ Realism Divergence: Real PKV-1 requires a 5-minute gyro warm-up and more complex boresight procedures. DCS simplifies this to near-immediate availability after power-on.*

### PKV-1 Control Summary

| Control | Location | Function |
|---|---|---|
| **Power Switch** | Left side panel, upper row | ON/OFF power to sight system |
| **Slew Joystick** | Right side of sight head | Move sight in azimuth and elevation (analog, proportional) |
| **Zoom Lever** | Left side of sight head | Variable magnification 1× to 8× — clockwise = zoom in |
| **Weapon Mode Selector** | Below sight head | Select reticle: CANNON / ROCKETS / ATGM / AAM |
| **Brightness Control** | Left side panel | Adjust reticle illumination intensity |
| **Cage / Uncage** | Top of sight head | Lock sight to aircraft axis (cage) or free it for slew (uncage) |
| **LRF Fire** | Sight head, left thumb | Fire laser rangefinder (if modeled) |

### DCS Key Bindings

| Function | Default Key | Recommended Binding |
|---|---|---|
| PKV-1 Slew Up | Numpad 8 | HOTAS hat — up |
| PKV-1 Slew Down | Numpad 2 | HOTAS hat — down |
| PKV-1 Slew Left | Numpad 4 | HOTAS hat — left |
| PKV-1 Slew Right | Numpad 6 | HOTAS hat — right |
| PKV-1 Zoom In | Numpad + | Analog axis or rotary |
| PKV-1 Zoom Out | Numpad − | Analog axis or rotary |
| Weapon Mode Next | `D` | Pinky or boat switch |
| PKV-1 View | `RCtrl + Numpad Enter` | Cockpit click or key |

---

## Weapon Mode Reticles

Each weapon type has its own PKV-1 reticle. Using the **wrong reticle is a common source of missed engagements**.

| Weapon Mode | Reticle Pattern | Range Marks | Recommended Magnification | Use |
|---|---|---|---|---|
| **Cannon** | Cross with horizontal range bars | 500 m / 1,000 m / 1,500 m | 2–4× (wide area) | Pilot dive reference; WSO spot assist |
| **Rockets** | Circular mil-dot ring with center pipper | Range rings at 500 m intervals to 3,000 m | 2–4× (target area) | CCIP integration; manual aim backup |
| **ATGM** | Fine crosshair with tracking box | No range marks (not relevant to SACLOS) | 4–8× (precision tracking) | SACLOS guidance — keep crosshair on target |
| **AAM** | Large acquisition circle with center dot | Seeker FOV ring | 1–2× (wide search) | Air-to-air cueing — slew seeker to target |

**Reticle Brightness by Condition:**
- **Bright daylight:** Medium brightness (excess brightness washes out background)
- **Overcast:** Increase brightness for contrast against grey sky
- **Dusk:** Reduce brightness to preserve dark adaptation
- **Night:** PKV-1 is unusable — entirely dark

---

## Laser Rangefinder

### LRF System Data

| Specification | Value |
|---|---|
| **Type** | Pulsed laser rangefinder (Raduga-Sh) |
| **Effective Range** | 400 m to 10,000 m |
| **Accuracy** | ±5 m typical |
| **Display** | Numeric readout in PKV-1 sight / cockpit display |
| **Integration** | Feeds range to ballistic computer for improved CCIP solution |

> *⚠ Realism Divergence: Not all Mi-24P variants were equipped with LRF. DCS implementation varies by module version. If LRF is unavailable, use visual mil-dot ranging (described below).*

### LRF Operating Procedure

1. PKV-1: Center crosshair precisely on target
2. LRF: Press laser fire button (left thumb button on sight head)
3. Range: Read displayed range value
4. CCIP: Pipper updates automatically with measured range
5. Employment: Fire weapon using improved CCIP solution

**LRF Tips:**
- Use LRF before every engagement when time permits
- LRF works against solid objects (vehicles, structures, terrain); may fail against thin targets
- Atmospheric conditions (dust, rain, fog) reduce effective range
- LRF pulse is detectable by advanced laser warning receivers — use judiciously in high-threat environments

---

## Target Acquisition Techniques

### Naked-Eye First — Always

**Never begin target search through the PKV-1 sight.** The narrow field of view (~6° at max zoom) makes initial area searching extremely inefficient. Standard acquisition sequence:

1. Naked eye scan → identify general target area
2. Estimate target bearing from aircraft nose
3. PKV-1 slew to that bearing → acquire through wide FOV (1–2×)
4. Narrow magnification only after spotting the target

### Visual Target Identification Cues

| Target Type | Visual Cues | Typical Recognition Range |
|---|---|---|
| **Main Battle Tanks** | Low profile, angular hull, track marks, dustcloud | 2–3 km (good visibility) |
| **APCs / IFVs** | Higher profile, wheels or tracks visible, antenna | 1.5–2.5 km |
| **Soft Vehicles** | Movement, dust clouds, vehicle reflections | 1–4 km (varies by size) |
| **Infantry** | Movement, muzzle flashes, linear positions | 0.5–1.5 km |
| **Structures** | Geometric shapes against natural terrain | 3–5 km |
| **Active AAA** | Muzzle flashes, tracer fire, radar rotation | 2–4 km when firing |

### Systematic Search Patterns

**Sector Scan (preferred for area search):**
- Divide suspected area into 30° sectors
- Scan each sector left-to-right, top-to-bottom
- Spend 15–20 seconds per sector maximum
- Use 1–2× magnification initially

**Rapid Area Scan (time-critical):**
- Quick left-right sweeps across suspected area
- Look for movement, geometric shapes, color contrast
- Switch to narrow magnification only after spotting a candidate

**Reference Point Method:**
- Use a prominent terrain feature as reference
- Search systematically outward from reference in expanding arcs
- Maintain bearing reference to aircraft heading

### PKV-1 Environmental Limitations

| Condition | Effect on PKV-1 | Mitigation |
|---|---|---|
| **Bright daylight** | Optimal performance | Standard procedures |
| **Overcast / haze** | Reduced contrast | Increase brightness; search more slowly |
| **Rain** | Optics degraded; droplets on window | Reduce engagement range; accept reduced accuracy |
| **Heat shimmer** | Distorts long-range picture (>3 km) | Close to effective range for engagement |
| **Dust / smoke** | Blocks visibility | Use radar altimeter to stay above obscurant |
| **Sun directly ahead** | Sight washout | Reposition aircraft heading |
| **Night** | Unusable — entirely black | No PKV-1 operations at night |

---

## Range Estimation

### Mil-Dot Ranging Formula

When LRF is unavailable, use known target dimensions against the PKV-1 reticle:

> **Range (m) = Known Target Dimension (m) × 1,000 ÷ Apparent Size (mils)**

| Vehicle Type | Length (m) | Height (m) | Apparent Size @ 1 km | Apparent Size @ 2 km |
|---|---|---|---|---|
| **T-72 / T-80 MBT** | 9.5 | 2.2 | ~9.5 / ~2.2 mils | ~4.8 / ~1.1 mils |
| **BMP-2 IFV** | 7.3 | 2.5 | ~7.3 / ~2.5 mils | ~3.7 / ~1.3 mils |
| **BTR-80 APC** | 7.7 | 2.4 | ~7.7 / ~2.4 mils | ~3.9 / ~1.2 mils |
| **Ural-4320 Truck** | 8.0 | 3.0 | ~8.0 / ~3.0 mils | ~4.0 / ~1.5 mils |
| **ZSU-23-4 Shilka** | 6.5 | 2.6 | ~6.5 / ~2.6 mils | ~3.3 / ~1.3 mils |

**Procedure:**
1. Identify target type (determines known dimensions)
2. Set PKV-1 to 4× or higher for precision
3. Compare apparent size against reticle mil marks
4. Calculate range; round to nearest 500 m
5. Call estimated range to pilot

### Range Estimation Accuracy Comparison

| Method | Accuracy | When to Use |
|---|---|---|
| **LRF (if equipped)** | ±5 m | Always when available and time permits |
| **Mil-dot visual ranging** | ±200–500 m at 2–4 km | When LRF unavailable |
| **Terrain association** | ±500–1,000 m | Quick estimates using known landmarks |

---

## Target Acquisition Sequence

**Standard DCS Procedure — 4 Steps:**

### Step 1 — Initial Search (2–4 km standoff)
- Pilot: Approach target area at designated standoff distance
- WSO: PKV-1 power verified ON, weapon mode selected
- WSO: Begin **naked-eye** scan of suspected target area

### Step 2 — PKV Acquisition
- WSO: Slew PKV-1 to suspected target bearing (based on naked-eye identification)
- WSO: Use **1–2× magnification** initially
- WSO: Identify target using visual cues and size comparison
- WSO: Call **"Contact, [target type], [bearing], [estimated range]"**

### Step 3 — Target Verification
- WSO: Increase magnification to **4–6×** for positive identification
- WSO: Confirm target type matches briefed threat description
- WSO: Use mil-dot ranging or LRF to refine range estimate
- WSO: Call **"Target confirmed, [type], [range], ready to engage"**

### Step 4 — Engagement Preparation
- WSO: Select appropriate weapon for target type and range
- WSO: Adjust magnification for weapon delivery (see weapon mode reticle table)
- WSO: Center target in reticle and maintain track
- WSO: Call **"Ready to fire"** when stable sight picture achieved
- Pilot: **"Cleared to engage"** — hold steady flight

---

## Battle Damage Assessment

**Immediate Post-Shot BDA:**
- WSO: Keep sight on target area after weapon impact
- WSO: Look for secondary explosions, fire, smoke, mobility loss
- WSO: Hold sight picture for minimum 10 seconds after impact
- WSO: Call BDA to pilot

**BDA Reporting Standards:**

| Call | Meaning | Indicators |
|---|---|---|
| **"Target destroyed"** | Target neutralized | Fire, explosion, no movement for 30+ seconds |
| **"Target damaged"** | Hit but still operational | Smoke, reduced mobility, partial effect |
| **"Target missed"** | No hit observed | No visible effect on target |
| **"Unable to assess"** | BDA obscured | Dust, smoke, or terrain masking view |

---

## DCS-Specific Tips

**View Control:**
- Use `RCtrl + Numpad Enter` (or cockpit click) to enter PKV-1 sight view
- Mouse scroll wheel zooms when in sight view
- TrackIR/VR: Position head near eyepiece to see through sight

**Known DCS Behaviors:**
- PKV-1 gyro stabilization may drift slightly — small corrections are normal
- Sight slew rate may feel slower than expected — bind to analog axis for smoothest control
- Weapon mode selector animation may lag behind actual mode change — confirm by checking reticle pattern, not switch position
- PKV-1 renders at reduced resolution in DCS — this is normal; clarity is lower than external view

---

## Common Errors

| Error | Consequence | Correction |
|---|---|---|
| **Searching at narrow magnification** | Tunnel vision; misses targets; disorientation | Always start at 1–2× FOV; narrow only after acquisition |
| **Slewing past target too fast** | Overshoots; loses reference | Slow deliberate movements near suspected area |
| **Wrong weapon mode on PKV-1** | Incorrect reticle; wrong ballistic solution | Verify mode matches selected weapon BEFORE engagement |
| **Not using naked eye first** | Inefficient search; wasted time | Always naked-eye acquire before PKV |
| **Inadequate range estimation** | Wrong weapon/profile; missed engagement | Practice mil-dot ranging; use LRF every time |
| **Sun glare in sight** | Cannot see target; temporary blindness | Reposition aircraft heading or wait for sun angle |
| **No BDA after impact** | May re-engage destroyed targets; waste ordnance | Maintain sight through impact + 10 seconds |
| **Not caging before maneuver** | Sight hits gimbal stops; loses reference | Cage before aggressive maneuver; uncage when stable |
| **Zoom too high during tracking** | Loses target during aircraft movement | Stay at 4–6× while tracking; 8× only for static BDA |

---

## Completion Standards

The student must demonstrate the following to the instructor's satisfaction before proceeding to Event 3:

- [ ] Power up PKV-1 in correct sequence from WSO seat
- [ ] Demonstrate smooth sight slew and zoom using HOTAS bindings
- [ ] Select correct weapon mode reticle for three different weapon types when prompted
- [ ] Acquire a stationary ground target within 60 seconds from naked-eye search start
- [ ] Estimate target range to within ±500 m using visual/mil-dot method
- [ ] Operate LRF (if available) and read range output correctly
- [ ] Call correct BDA after simulated weapon impact
- [ ] State all major PKV-1 environmental limitations when prompted

---

*Based on DCS World Mi-24P Hind module by Eagle Dynamics and real-world PKV-1 optical sight system documentation. For simulation use only.*
