# Su-25T Weapons Employment Dossier

**Subject:** Su-25T "Frogfoot-B" Weapons Systems & Employment Procedures  
**Target Simulator:** DCS World  
**Status:** Research Draft for Training Mission Development

---

## Module 1: Targeting Systems

The Su-25T relies on electro-optical systems for precision targeting. Unlike Western pods (TGP), these are integrated into the airframe or specialized dedicated pods.

### 1.1 I-251 "Shkval" EO System
The primary daytime targeting system located in the nose.

*   **Capabilities (DCS):**
    *   **Daytime Only:** The camera has no thermal imaging capability. It relies on visible light contrast.
    *   **Zoom Levels:** Two discrete steps — 23x (wide) and 8x (narrow).
    *   **Slew Rates:** Variable. Fast slew for gross acquisition, fine slew for precision aiming.
    *   **Stabilization:** Ground-stabilized once slewed.

*   **Constraints:**
    *   **Gimbal Limits:** Azimuth ±35°, Elevation +15° to -85°.
    *   **Contrast Lock:** Requires sufficient contrast between target and background. Smoke, shadows, or low light will break lock or prevent it.
    *   **Laser Rangefinder:** Integrated. Must be active for ranging (unguided) and designation (guided).

*   **Realism Notes:**
    *   **Slew Rate:** In DCS, the slew rate is relatively fast and smooth. Real-world pilots report the system is clunkier and harder to fine-tune under G-load.
    *   **Contrast Lock:** DCS allows locking onto "nothing" (ground texture) more easily than the real system, which struggled with low-contrast terrain (e.g., green tank on green grass).

### 1.2 "Mercury" (Merkury) LLTV Pod
Low-Light Television system for night operations.

*   **Capabilities (DCS):**
    *   **Night Vision:** Amplifies available light. Green-scale image on the HUD/IT-23M TV monitor.
    *   **Integration:** Overlays directly with the Shkval logic. You select the pod, but the symbology remains similar.
    *   **Range:** Shorter effective range than Shkval due to lower resolution (~3-5 km identification range).

*   **Constraints:**
    *   **Mounting:** Centerline station only (Station 6).
    *   **Conflict:** Cannot carry the "Phantasmagoria" SEAD pod or MPS-410 Jammer if Mercury is mounted.
    *   **Daytime:** Useless in daylight (image washes out).

*   **Realism Notes:**
    *   **Usage:** Rarely fielded in large numbers. In DCS, it transforms the Su-25T into a viable night-attacker, whereas in reality, night Su-25 operations were extremely hazardous and rare.

---

## Module 2: Unguided Munitions (CCIP/CCRP)

### 2.1 Guns (GSh-30-2)
Twin-barrel 30mm autocannon fixed in the nose.

*   **Ammo:** 250 rounds.
*   **Modes:**
    *   **Fix:** Fixed depression (reticle static).
    *   **Prog:** Computed impact point (reticle moves).
*   **DCS Employment Sequence:**
    1.  Master Arm: ON
    2.  Mode: A-G (`7`)
    3.  Weapon Select: Gun (`C`)
    4.  Laser: ON (`RShift + O`) - Improves accuracy.
    5.  Dive: 15-20°.
    6.  Fire: Spacebar.
*   **Key Constraints:**
    *   Effective Range: < 1.5 km.
    *   Vibration: Sustained fire vibrates the airframe heavily, degrading HUD readability.
*   **Realism Notes:** The real GSh-30-2 has a selectable rate of fire (3000 vs 300 rpm). DCS models the high rate by default.

### 2.2 Rockets (S-8, S-13, S-25)
*   **S-8 (80mm):** Pods of 20. Area saturation.
*   **S-13 (122mm):** Pods of 5. Light armor/bunkers.
*   **S-25 (340mm):** Single massive rocket. Heavy blast/fragmentation.
*   **DCS Employment Sequence (CCIP):**
    1.  Master Arm: ON
    2.  Mode: A-G (`7`)
    3.  Select Pylons.
    4.  Laser: ON (`RShift + O`) - Critical for accurate ranging.
    5.  Maneuver: Dive 15-30°.
    6.  Pipper: Place dot on target.
    7.  Fire: Spacebar.
*   **Common Errors:**
    *   Firing without Laser Ranging: The reticle will be fixed at a default depression, leading to massive misses.
    *   Shallow Dive: Rockets disperse more in shallow dives. Steeper = more accurate.

### 2.3 Bombs (FAB-100/250/500, RBK)
*   **Modes:**
    *   **CCIP (Dive):** Visual dive. Pipper on target.
    *   **CCRP (Level):** Designated target point. Fly level. Auto-release.
*   **DCS Employment Sequence (CCRP/Level):**
    1.  Master Arm: ON
    2.  Mode: A-G (`7`)
    3.  Select Bombs.
    4.  Slew Shkval (`;`, `,`, `.`, `/`) to target area.
    5.  Lock: (`Enter`) to stabilize ground point.
    6.  Align: Fly to keep the vertical steering line centered.
    7.  Pickle: Hold Weapon Release (`Space`) continuously when the "Release Range" cue appears.
    8.  Release: Bombs drop automatically when parameters are met.
*   **Realism Notes:** CCRP in the Su-25T is less precise than Western equivalents (JDAM/Paveway) due to INS drift and older computing logic. Wind correction is manual/rudimentary.

---

## Module 3: Guided Missiles (Vikhr & Kh-25/29)

### 3.1 9A4172 "Vikhr" (AT-16 Scallion)
The signature weapon of the Su-25T. Supersonic, laser-beam riding anti-tank missile.

*   **Mechanics:** Beam-rider. The missile looks backwards at the launch aircraft to stay centered in a laser grid pattern.
*   **DCS Employment Sequence:**
    1.  Master Arm: ON
    2.  Mode: A-G (`7`)
    3.  Select Vikhr pods.
    4.  Shkval: ON (`O`). Slew to target.
    5.  Target Size: Adjust gate size (`Rcrtl + [` / `]`) to match target (approx 10m).
    6.  Lock: (`Enter`).
    7.  Laser: ON (`RShift + O`). **Mandatory**.
    8.  Maneuver: Align the large outer circle (launch zone) with the small inner circle (seeker/laser limit).
    9.  Launch: Press and hold release (`Space`).
*   **Key Constraints:**
    *   **Range:** Max ~8-10km (high alt), ~6km (low alt). Min ~800m.
    *   **Launch Window:** You must fly relatively straight toward the target. Banking > 30° usually breaks the beam.
*   **Common Errors:**
    *   **Not turning on the Laser:** The missile will launch but go stupid immediately.
    *   **Banking after launch:** The missile loses the laser beam and spirals into the ground.
*   **Realism Notes:**
    *   **Launch Auth Override (`LAlt + W`):** In DCS, you often need this for head-on shots against helos or max-range shots where the computer is too conservative. Real pilots use this strictly for emergency close-range shots.

### 3.2 Kh-25ML (AS-10 Karen) & Kh-29L (AS-14 Kedge)
Heavy laser-guided missiles.

*   **Kh-25ML:** "Light" tactical missile. Good for APCs, light bunkers, SA-9/13.
*   **Kh-29L:** Heavy hitter (320kg HE warhead). Kills anything (bridges, ships, concrete bunkers).
*   **DCS Employment Sequence:**
    1.  Same setup as Vikhr (Laser ON is critical).
    2.  Lock target with Shkval.
    3.  Wait for "LA" (Launch Authorized).
    4.  Launch.
*   **Difference from Vikhr:** These are semi-active laser homers. You can maneuver more freely after launch, as long as the Shkval gimbal limits aren't exceeded. You don't need to point the nose *directly* at the target, just keep the target within the Shkval's view.

---

## Module 4: SEAD (Suppression of Enemy Air Defenses)

### 4.1 L-081 "Fantasmagoria" Pod
ELINT pod required to detect and target radar emitters.

*   **Function:** Detects radar emissions, classifies them, and provides triangulation for SEAD missiles.
*   **DCS Usage:**
    *   Appears on the HUD as diamonds (emitters).
    *   Selectable cursor allows you to "lock" a specific emitter.
*   **Constraint:** Must be mounted on the centerline. Mutually exclusive with Mercury LLTV and MPS-410 Jammer.

### 4.2 Kh-58 (AS-11 Kilter)
Long-range anti-radiation missile.

*   **Target:** Long-range search radars (Patriot, S-300, Hawk).
*   **Capabilities:**
    *   **Range:** up to 120km (high altitude launch).
    *   **Speed:** Mach 3+.
    *   **Memory:** If the radar shuts down, the Kh-58 attempts to fly to the last known location (INS).
*   **DCS Employment Sequence:**
    1.  Mode: A-G (`7`).
    2.  Sensor: Phantasmagoria ON (`I` - usually on by default in SEAD mode).
    3.  Select Kh-58.
    4.  Slew cursor to HUD diamond.
    5.  Lock (`Enter`).
    6.  Wait for LA.
    7.  Launch.
*   **Realism Notes:**
    *   **Launch & Leave:** True fire-and-forget. You can turn away immediately after launch.

### 4.3 Kh-25MPU (AS-12 Kegler)
Short/Medium-range anti-radiation missile.

*   **Target:** SHORAD radars (Roland, Gepard, Osa, Tunguska).
*   **Capabilities:**
    *   **Range:** ~20-40km.
    *   **Seeker:** Less sophisticated than Kh-58.
*   **Constraint:** The seeker head must have a clear line of sight to the emitter before launch.
*   **Common Errors:**
    *   Firing at long-range search radars. The Kh-25MPU warhead is too small to reliably kill a large radar van unless it's a direct hit.
    *   Thinking it has INS memory like the Kh-58. It effectively goes ballistic if the radar turns off (though DCS logic sometimes is generous here).
