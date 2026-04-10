# Event 1 — Weapons Systems Academics

> **Course:** A-10A Weapons Employment | **Event Type:** Ground (Academic)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Weapons Safety Rules](#weapons-safety-rules)
3. [Module 1 — FC3 Weapons Interface](#module-1--fc3-weapons-interface)
4. [Module 2 — Unguided Weapons Overview](#module-2--unguided-weapons-overview)
5. [Module 3 — Cluster Munitions Overview](#module-3--cluster-munitions-overview)
6. [Module 4 — AGM-65 Maverick Overview](#module-4--agm-65-maverick-overview)
7. [Module 5 — Pave Penny & Defensive Systems](#module-5--pave-penny--defensive-systems)
8. [Weapons Modes Cheat Sheet](#weapons-modes-cheat-sheet)
9. [Completion Standards](#completion-standards)

---

## Learning Objectives

Upon completion of this event the student will be able to:
- [ ] Describe the FC3 weapons cycling interface and explain why it differs from the A-10C
- [ ] State the correct employment mode (CCIP/CCRP/Guided) for each weapon type
- [ ] Recite the three safety rules for weapons employment
- [ ] Explain the difference between IR (AGM-65D/G) and TV (AGM-65H/K) Maverick seekers
- [ ] Describe the Pave Penny's capability and explain why the A-10A cannot self-designate for LGBs

---

## Weapons Safety Rules

These three rules apply to every weapons release in this course. Violation of any rule results in a **DOWN** grade.

> **Rule 1 — Positive Target ID (VID):** Do not release weapons until the target is positively identified as hostile. For Mavericks, confirm the seeker is tracking the intended target — not a decoy, friendly vehicle, or terrain feature. If you cannot identify it — do not shoot.
>
> **Rule 2 — Safe Escape:** Ensure sufficient altitude and airspeed to escape the weapon's fragmentation envelope before release. Do not fly through your own frag pattern. The GAU-8/A's massive recoil will decelerate you — plan your escape energy accordingly.
>
> **Rule 3 — Master Arm Discipline:** Master Arm (`O`) is ON only during the attack run. Return to SAFE immediately after weapon release or abort.

---

## Module 1 — FC3 Weapons Interface

### The Non-Clickable Cockpit

The DCS A-10A is a Flaming Cliffs 3 module. Unlike the A-10C (full fidelity), you do **not** interact with cockpit panels. All weapon selection and employment is performed via keybinds.

| Function | Key | Notes |
|---|---|---|
| Master Arm (Toggle) | `O` | ARM before attack, SAFE after |
| Cycle Weapon Station | `D` | Cycles through loaded stores left-to-right |
| Fire / Release | `Space` | Guns, rockets, bombs, and missiles |
| Maverick Slew | `Numpad 8/2/4/6` | Up/Down/Left/Right |
| Maverick Lock | `Numpad Enter` | Locks seeker on contrast target |
| Jettison All | `LAlt + J` | Emergency stores dump |
| Chaff | `[` | Radar countermeasure |
| Flares | `]` | IR countermeasure |

### Weapon Cycling (`D`)

The `D` key cycles through each loaded station sequentially. The HUD updates to show the currently selected weapon type and delivery mode (CCIP pipper, CCRP steering, or Maverick seeker display).

**Critical difference from the A-10C:** There is no DSMS page, no profile selection, no ripple settings accessible through a cockpit interface. What you cycle to is what you get. Plan your loadout carefully in the mission editor — you cannot reconfigure in flight.

**Instructor Note:** Students who transition from the A-10C often look for MFD pages that do not exist. Brief clearly: "This is an analog jet with a keyboard. The `D` key is your weapons panel."

---

## Module 2 — Unguided Weapons Overview

### GAU-8/A Avenger (30mm Gatling Gun)

The GAU-8/A is the A-10's defining weapon — a seven-barrel rotary cannon designed specifically to destroy Soviet main battle tanks.

| Parameter | Value |
|---|---|
| Caliber | 30mm |
| Rounds | 1,174 (standard combat load) |
| Rate of fire | 3,900 rpm |
| Effective range | < 1.5–2 NM (2,800–3,700 m) |
| Ammunition | Combat mix: API (Armor Piercing Incendiary) / HEI (High Explosive Incendiary) |
| Employment | CCIP — Gun Cross on HUD |

**Recoil effect:** The GAU-8/A produces approximately 10,000 lbs of recoil force. When firing, the aircraft decelerates noticeably. In a shallow dive, this can cause the pipper to drift. Use short bursts (1–2 seconds) and re-aim between bursts.

> **Realism Note:** The real A-10 has selectable fire rates (2,100 and 4,200 rpm). DCS FC3 models a single rate (~3,900 rpm). Real pilots typically use the low rate for precision strafing and high rate for area suppression.

### Hydra 70 Rockets

| Variant | Type | Best Use |
|---|---|---|
| M151 | High Explosive | Soft targets, trucks, suppression |
| M274 | White Phosphorus (Smoke) | Target marking for FAC/CAS |
| M257 | Illumination Flare | Battlefield illumination (night) |

- All variants fire from LAU-68 or LAU-131 seven-tube pods
- CCIP delivery only — pipper moves with range
- Dive angle ≥ 15° for acceptable dispersion

### Mk-82 / Mk-82AIR / Mk-84 Gravity Bombs

| Bomb | Weight | Type | Notes |
|---|---|---|---|
| Mk-82 | 500 lb | Low Drag (slick) | General purpose — trucks, infantry, light armor |
| Mk-82AIR | 500 lb | High Drag (ballute) | Low-altitude delivery; retarding device slows bomb |
| Mk-84 | 2,000 lb | Low Drag (slick) | Massive blast radius — bridges, bunkers, structures |

- **CCIP:** Visual dive delivery — HUD pipper tracks computed impact point
- **CCRP:** Level flight delivery — HUD provides steering and auto-release cue

> **Key difference — Mk-82 vs. Mk-82AIR:** The standard Mk-82 requires a dive delivery with high pull-off altitude (frag envelope). The Mk-82AIR deploys a ballute (balloon-parachute) that retards the bomb, allowing safe delivery from low altitude at high speed. Use Mk-82AIR when terrain or threats demand low-level ingress.

---

## Module 3 — Cluster Munitions Overview

### CBU-87 Combined Effects Munition (CEM)

| Parameter | Value |
|---|---|
| Weight | ~950 lb |
| Submunitions | 202 BLU-97/B bomblets |
| Effects | Anti-armor (shaped charge) + anti-personnel (frag) + incendiary |
| Pattern | ~200 m × 400 m (depending on release altitude/speed) |
| Best targets | Soft target concentrations — truck parks, infantry positions, mixed columns |

The CBU-87 is a general-purpose area weapon. Each BLU-97/B bomblet has a shaped charge capable of penetrating light armor, plus a fragmentation casing and zirconium incendiary ring.

### CBU-97 Sensor Fuzed Weapon (SFW)

| Parameter | Value |
|---|---|
| Weight | ~927 lb |
| Submunitions | 10 BLU-108/B canisters → 40 Skeet warheads |
| Guidance | Passive IR (each Skeet seeks heat sources) |
| Pattern | Searches area beneath canister descent path |
| Best targets | **Heavy armor columns** — MBTs, IFVs in formation |

The CBU-97 is the A-10A's "tank plinking" weapon. After release, each BLU-108 canister descends by parachute, spins, and ejects four Skeet warheads. Each Skeet uses a passive IR sensor to detect armored vehicle heat signatures and fires an explosively formed penetrator (EFP) downward.

> **Realism Note:** The CBU-97 is extremely effective in DCS against massed armor. In reality, its effectiveness degrades in rain, fog, and against camouflaged/cold targets. DCS does not fully model these degradation factors.

### Release Parameters (Both CBU Types)

| Parameter | Value |
|---|---|
| Delivery | Level or shallow dive (10–20°) |
| Release altitude | 300–600 m AGL (optimal submunition scatter) |
| Airspeed | 300–450 kts |
| Min safe altitude | 300 m AGL (below this, submunitions may not arm) |

---

## Module 4 — AGM-65 Maverick Overview

The AGM-65 Maverick is the A-10A's primary precision standoff weapon. It is fire-and-forget — after launch, the missile guides itself to the target independently.

### Seeker Types

| Variant | Seeker | Warhead | Range | Conditions |
|---|---|---|---|---|
| **AGM-65D** | Imaging IR (IIR) | 125 lb shaped charge | 6–8 NM | Day/Night, most weather |
| **AGM-65G** | Imaging IR (IIR) | 300 lb blast/frag | 6–8 NM | Day/Night — ships, bunkers |
| **AGM-65H** | CCD TV (Electro-Optical) | 125 lb shaped charge | 4–6 NM | Daylight only |
| **AGM-65K** | CCD TV (Electro-Optical) | 300 lb blast/frag | 6–10 NM | Daylight only — bridges, bunkers |

### IR vs. TV — When to Use Which

| Condition | Use IR (D/G) | Use TV (H/K) |
|---|---|---|
| Night operations | ✓ | ✗ |
| Dawn/dusk | ✓ | Limited |
| High contrast daytime | ✓ | ✓ |
| Cold/camouflaged targets | Limited | ✓ (if visible) |
| Ships / large structures | AGM-65G | AGM-65K |
| Tanks / vehicles | AGM-65D | AGM-65H |

### Maverick Employment Basics

1. Select Maverick station (`D`)
2. Seeker powers on — allow 3–5 minutes for IIR cooldown (IR variants)
3. Slew seeker to target area (`Numpad 8/2/4/6`)
4. Identify target — confirm VID
5. Lock (`Numpad Enter`) — seeker squares on target
6. Confirm lock is on intended target (not decoy or terrain)
7. Fire (`Space`) — **fire and forget**
8. Break off — the missile guides itself

### IR Seeker Polarity

IR Mavericks (D/G) can display in **White Hot** or **Black Hot** polarity. Switching polarity can help acquire targets that blend into the background in one mode.

> **Realism Note:** Real AGM-65D seekers require a 3–5 minute cooldown cycle after power-on. DCS models this — if you fire immediately after selecting the Maverick, the seeker image will be degraded. Power on Mavericks early in the mission.

---

## Module 5 — Pave Penny & Defensive Systems

### Pave Penny (AN/AAS-35V) Laser Spot Tracker

| Parameter | Value |
|---|---|
| Type | Passive Laser Spot Tracker (TISL) |
| Capability | Detects laser energy from external designators |
| Limitation | **Cannot self-designate** — detection only |
| HUD cue | Diamond symbol at laser spot location |

The Pave Penny detects laser energy reflected from a target that is being designated by a JTAC, FAC, or another aircraft ("buddy lase"). It places a diamond cue on the HUD showing where the laser spot is.

**What it cannot do:** The Pave Penny is not a targeting pod. It cannot generate its own laser designation. The A-10A **cannot self-guide LGBs** (GBU-10/12). If carrying LGBs, an external designator is required.

> This course does not cover buddy-lasing or LGB employment, as they require coordination with external assets.

### AIM-9M Sidewinder (Self-Defense)

| Parameter | Value |
|---|---|
| Type | IR Homing Air-to-Air Missile |
| Range | < 5 NM |
| Best targets | Helicopters, slow movers |
| Requirement | Seeker tone (growl) before launch |

The AIM-9M is a self-defense weapon only. It is not covered in the flight events of this course, but the student must understand its availability and employment envelope.

### ALE-40 Chaff/Flare System

| Function | Key |
|---|---|
| Chaff (radar countermeasure) | `[` |
| Flares (IR countermeasure) | `]` |

### ALQ-131 / ALQ-184 ECM Pod

Active electronic jamming pod. Reduces radar lock-on range for enemy SAMs. Power ON before entering threat area.

---

## Weapons Modes Cheat Sheet

| Weapon | Master Arm | Select | HUD Mode | Lock Required | Fire-and-Forget |
|---|---|---|---|---|---|
| GAU-8/A | ON (`O`) | `D` (cycle to Gun) | CCIP — Gun Cross | No | N/A |
| Hydra 70 | ON (`O`) | `D` (cycle to rockets) | CCIP — Pipper | No | N/A |
| Mk-82/84 (CCIP) | ON (`O`) | `D` (cycle to bomb) | CCIP — Pipper | No | N/A |
| Mk-82/84 (CCRP) | ON (`O`) | `D` (cycle to bomb) | CCRP — Steering/Release cue | No | N/A |
| CBU-87/97 | ON (`O`) | `D` (cycle to CBU) | CCIP or Level release | No | N/A |
| AGM-65 (all) | ON (`O`) | `D` (cycle to Maverick) | Seeker display | **Yes** (`Numpad Enter`) | **Yes** |
| AIM-9M | ON (`O`) | `D` (cycle to AIM-9) | A-A — Seeker tone | Tone lock | Yes |

---

## Completion Standards

Pass by correctly answering all five questions before proceeding to Event 2:

- [ ] **Q1:** You are carrying AGM-65D Mavericks for a night strike. Should you power them on immediately after engine start? *(Answer: Yes — IIR seekers need 3–5 minutes to cool down; power on early)*
- [ ] **Q2:** You are diving at 20° on a target and fire the GAU-8/A for 4 seconds. Your airspeed drops and the pipper drifts off target. What happened? *(Answer: GAU-8/A recoil decelerated the aircraft; use 1–2 second bursts)*
- [ ] **Q3:** You are carrying Pave Penny and GBU-12s but have no JTAC or buddy lase available. Can you self-designate? *(Answer: No — Pave Penny is a tracker, not a designator; the A-10A cannot self-lase)*
- [ ] **Q4:** What is the primary difference between CBU-87 and CBU-97? *(Answer: CBU-87 uses pre-fragmented bomblets (area suppression); CBU-97 uses IR-seeking Skeet warheads that actively target armored vehicles)*
- [ ] **Q5:** You lock an AGM-65H on a target in fading twilight but the seeker image is dark and grainy. Should you fire? *(Answer: No — the H variant is TV/CCD, daylight only; switch to AGM-65D (IR) for low-light conditions)*

---

[→ Proceed to Event 2: GAU-8/A Gun & Rockets](event-2-guns-rockets.md)

---

*Based on T.O. 1A-10A-34-1-1 and Eagle Dynamics DCS World documentation. For simulation use only.*
