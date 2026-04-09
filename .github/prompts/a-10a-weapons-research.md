Act as an expert USAF A-10A "Thunderbolt II" weapons officer and DCS World mission planner, cross-referencing real-world USAF technical manuals with DCS simulation documentation. I need you to compile a detailed research dossier for an **A-10A Weapons Employment Course**.

**Objective:**
Create a comprehensive technical reference document covering the employment of all air-to-ground weapons available on the DCS A-10A (Flaming Cliffs 3 module). This research will be used to build a multi-event training course with structured exercises and grading criteria. The student has already completed the A-10A BQT course and is proficient in basic flight operations.

**DCS Module Context:**
The DCS A-10A is an **FC3 (Flaming Cliffs 3) simplified-systems module**:
- **No clickable cockpit** — all systems are keyboard/HOTAS keybind operated.
- Weapons are cycled via the `D` key, not through a DSMS/MFD workflow (unlike the A-10C).
- **No Targeting Pod (TGP)** — the A-10A cannot self-designate for LGBs. It carries the **Pave Penny (AN/AAS-35)** laser spot tracker, which detects laser energy from a JTAC or buddy lazer, but does NOT designate.
- **Advanced Flight Model (AFM)** — aerodynamics, weapon ballistics, and recoil effects are realistic.
- **GAU-8/A recoil** is modeled — sustained fire will decelerate the aircraft noticeably.

**Source Material Prioritization:**
1. **Primary (Simulation Truth):** Official DCS A-10A FC3 documentation and actual in-game behavior. When the sim contradicts real-world procedures, **the sim wins** — document the DCS procedure as primary instruction.
2. **Secondary (Realism Context):** Real-world USAF documentation:
   - *T.O. 1A-10A-34-1-1* (A-10A Non-Nuclear Weapons Delivery Manual)
   - *AFMAN 11-2A-10 Vol. 3* (A-10 Operations Procedures)
   - *MCM 3-1* (USAF Tactical Employment Manual — Multi-Command Manual)
   - A-10A Dash-1 weapons employment supplements
3. **Conflict Resolution:** When a real-world procedure conflicts with DCS, document the **DCS procedure** as the primary instruction and add a clearly marked footnote:
   > *⚠ Realism Divergence: [explanation of the real-world procedure and how/why DCS differs.]*

**Required Research Modules:**

---

**Module 1: Weapons Systems Overview & HUD Symbology**
- **HUD Weapons Symbology:**
  - Gun cross / pipper behavior in CCIP mode.
  - Bomb fall line and CCIP pipper for iron bombs.
  - CCRP steering cue and solution cue for level delivery.
  - Maverick bore-sight cross and seeker slew indicators.
- **Weapons Cycling & Selection:**
  - How the `D` key / weapon select key cycles through loaded stations.
  - Station priority / cycling order for typical loadouts.
  - Master Arm engagement and safe/arm/weapon-hot logic.
- **Delivery Modes Available in FC3:**
  - CCIP (Continuously Computed Impact Point) — diving/strafing.
  - CCRP (Continuously Computed Release Point) — level delivery.
  - Maverick autonomous seeker modes (IR / EO-TV).

---

**Module 2: GAU-8/A Avenger Cannon**
- **System Data:**
  - 30mm 7-barrel Gatling; 3,900 RPM.
  - Ammunition: 1,174 rounds capacity; standard combat mix (PGU-14/B API + PGU-13/B HEI).
  - Effective range vs. armored targets: 4,000–6,000 ft slant range.
  - Effective range vs. soft targets: up to 8,000–12,000 ft slant range.
- **Employment Profiles:**
  - 20–30° dive angle strafing pass (anti-armor).
  - Shallow / low-angle strafing (soft targets, troops-in-contact).
  - Trigger discipline: 1–2 second bursts; barrel erosion and ammunition conservation.
- **Recoil Effects:**
  - DCS models the ~19,000 lbf recoil force — noticeable airspeed bleed during firing.
  - Nose wander / pitch oscillation during long bursts.
  - Compensation techniques: trim and anticipation.
- **Common student errors with the GAU-8.**

---

**Module 3: Unguided Bombs (Iron Bombs & Cluster Munitions)**
- **Available Ordnance:**
  - Mk-82 (500 lb GP, low-drag).
  - Mk-82 AIR (BSU-49 — high-drag / retarded, for low-altitude delivery).
  - Mk-84 (2,000 lb GP).
  - CBU-87 (Combined Effects Munition — anti-armor/personnel/incendiary).
  - CBU-97 (Sensor Fuzed Weapon — autonomous anti-armor skeet munition).
- **Delivery Modes:**
  - CCIP dive bombing: recommended dive angles (20–45°), entry altitudes, release altitudes, and minimum recovery altitudes.
  - CCRP level bombing: altitude, airspeed, and solution timing.
  - Low-altitude delivery with Mk-82 AIR (pop-up profiles).
- **Fuzing:**
  - Nose/tail fuze options (if selectable in FC3).
  - Instantaneous vs. delay fuze selection for different targets.
  - CBU-97 SFW employment altitude requirements (minimum burst altitude for skeet acquisition).
- **Bomb damage assessment considerations by target type.**

---

**Module 4: Unguided Rockets (Hydra 70 Family)**
- **Available Variants:**
  - M151 (HE warhead) — anti-personnel, soft targets.
  - M274 (WP / smoke marking) — target designation for CAS.
  - M257 (illumination) — battlefield illumination for night operations.
- **Launcher Types:** LAU-68 / LAU-131 (7-tube pods).
- **Employment Profiles:**
  - 10–20° dive angle; 1.0–2.0 nm firing range.
  - Ripple vs. single fire modes.
  - CCIP pipper usage for rockets.
- **Marking technique for FAC/CAS scenarios.**
- **Dispersion and accuracy characteristics.**

---

**Module 5: AGM-65 Maverick Family (Precision Guided)**
- **Variants Available on DCS A-10A:**
  - AGM-65D (IR seeker — imaging infrared).
  - AGM-65G (IR seeker — heavy warhead, 300 lb blast-frag).
  - AGM-65H (CCD/EO-TV seeker — daytime only, 125 lb shaped charge).
  - AGM-65K (CCD/EO-TV seeker — heavy warhead, 300 lb).
- **Seeker Operations:**
  - IR (D/G): polarity switching (White-Hot / Black-Hot); pre-launch cool-down considerations.
  - EO-TV (H/K): daylight-only, contrast-dependent; FOV and slew techniques.
  - Lock-on procedure: slew to target → lock (`Enter` or designated key) → confirm tracking → pickle.
  - "Maverick handoff" — seeker automatically uncages and acquires.
- **Employment Profiles:**
  - Stand-off range: 4–10 nm depending on variant and conditions.
  - Launch envelope: altitude, dive angle, airspeed constraints.
  - Single-shot vs. ripple fire considerations.
- **Variant Selection Guide:**
  - When to use IR (D/G) vs. EO-TV (H/K).
  - Night operations: IR only.
  - Target type guidance (heavy warhead G/K for bunkers/bridges; light warhead D/H for armor/vehicles).
- **Common student errors with Mavericks.**

---

**Module 6: Pave Penny & Buddy Lasing (LGB Delivery)**
- **AN/AAS-35 Pave Penny:**
  - Laser spot tracker only — NOT a designator.
  - Detects laser energy from an external source (JTAC, buddy aircraft, ground FAC).
  - Displays a diamond marker in HUD when laser is detected.
  - Operational limitations: field of view, range, weather/obscurants.
- **Laser-Guided Bombs (if available in FC3 loadout):**
  - GBU-10 (2,000 lb LGB), GBU-12 (500 lb LGB) — availability on FC3 A-10A.
  - Employment requires external laser designation (buddy lasing or JTAC).
  - Release profile: CCRP to computed release point while Pave Penny tracks external laser.
  - Coordination requirements: laser code matching, designation timing, "laser on" call.
- **Buddy Lasing Workflow:**
  - A-10A + laser-equipped wingman/JTAC coordination.
  - Communication flow: "Spot, Spot" / "Laser On" / "Rifle" / "Splash."
  - Timing: laser on before or at release? DCS specifics.
- **Limitations and workarounds for FC3 module.**

---

**Module 7: AIM-9M Sidewinder (Self-Defense A/A)**
- **Missile Data:**
  - AIM-9M all-aspect IR homing; rear-aspect preferred.
  - Effective range: 0.5–5 nm (conditions dependent).
  - IRCCM (IR Counter-Countermeasure) capability.
- **Employment:**
  - Seeker tone interpretation (growl = tracking; steady tone = lock).
  - Launch envelope (aspect, range, altitude).
  - Self-defense doctrine: when to engage vs. when to evade.
- **DCS FC3 A/A mode activation and keybinds.**
- **This is a self-defense weapon only — the A-10A is NOT a fighter.**

---

**Module 8: ECM & Defensive Systems**
- **ALQ-131 / ALQ-184 ECM Pod:**
  - Jamming modes and effectiveness by threat type.
  - Pod station assignment (affect on weapons loadout).
  - When to use active jamming vs. passive (RWR-only) posture.
- **Countermeasures:**
  - Chaff and flare programs.
  - DCS keybinds for dispensing.
  - Doctrine: when to dispense (RWR launch warning, visual SAM launch, etc.).
- **RWR Interpretation:**
  - Threat prioritization on RWR display.
  - SAM engagement zones and "notching" technique.
  - Terrain masking as primary defense.
- **Survivability integration:** Using ECM + countermeasures + terrain masking + speed as a layered defense.

---

**For each weapon system / module, provide:**
1. **DCS Employment Sequence:** Step-by-step keybind switchology (Master Arm → Mode → Select → Lock → Pickle / Fire).
2. **Key Constraints:** Min/Max range, altitude, airspeed, dive angle, and recovery altitude.
3. **Recommended Attack Profiles:** Entry altitude, speed, dive angle, release/fire parameters, egress.
4. **Common Student Errors:** What students usually do wrong and how to fix it.
5. **Realism Divergence Notes:** Where DCS simplifies or omits real-world procedures/limitations.

**Output Format:**
A single, structured Markdown document suitable for saving as `.github/research/a-10a-weapons-dossier.md`. Use heading levels `##`, `###`, and `####` consistently. Include data tables for all numerical parameters.
