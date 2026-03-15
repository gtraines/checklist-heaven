# Research Dossier: OH-58D Kiowa Warrior Weapons

**Target Aircraft:** OH-58D Kiowa Warrior (DCS World Module)
**Focus:** AGM-114 Hellfire, Hydra 70/APKWS, .50 Cal Machine Gun

---

## 1. Air-to-Ground Missiles (AGM-114 Hellfire)

The OH-58D carries Hellfire missiles on the universal weapons pylons (usually 2 per side if fully loaded, or mixed loadouts). The MMS (Mast Mounted Sight) provides laser designation for SAL variants.

### AGM-114K Hellfire II
- **Type:** Semi-Active Laser (SAL) Guided Anti-Tank Missile.
- **Effective Range:** 500m to 8,000m (8km). Optimum shots often 2-6km.
- **Best Suited For:** Heavy armor (MBTs), hardened targets. High penetration capability with tandem warhead (defeats ERA).
- **Simulation Constraints:** 
  - Requires constant laser designation (LOAL or LOBL). 
  - The OH-58D pilot/co-pilot must keep the MMS laser on target until impact (unless remotely designated by a buddy or JTAC).
  - Can be launched in LOAL (Lock-On After Launch) modes (DIR, LO, HI) to mask the helicopter during flight.

### AGM-114M Hellfire II
- **Type:** Semi-Active Laser (SAL) Guided Blast-Fragmentation Missile.
- **Effective Range:** Similar to K model (approx 8km max).
- **Best Suited For:** Soft targets, light armored vehicles, boats/ships, caves, and structures. The blast-frag warhead is less effective against heavy tank armor but superior for area effect or breaching.
- **Simulation Constraints:** 
  - Same laser requirements as the K model.
  - Delay fuse options may be simulated for penetrating structures before detonating.

### AGM-114N Hellfire II (MAC)
- **Type:** Semi-Active Laser (SAL) Guided Metal Augmented Charge (Thermobaric).
- **Effective Range:** Similar to K/M models (approx 8km max).
- **Best Suited For:** Enclosed spaces, bunkers, caves, buildings, and personnel in cover. The thermobaric effect creates a sustained high-pressure wave and heat, ideal for destroying targets from the inside.
- **Simulation Constraints:** 
  - Same laser requirements as K/M.
  - Visual damage in DCS may be similar to M, but damage model calculations differ for enclosed targets.

### AGM-114L Longbow Hellfire
- **Type:** Radar Guided (RF) Fire-and-Forget Anti-Tank Missile.
- **Note on OH-58D:** The OH-58D **lacks a Fire Control Radar (FCR)**. It generally **cannot** self-designate or employ the AGM-114L autonomously in the same manner as an AH-64D.
- **Simulation Constraints:** 
  - In DCS, the OH-58D is primarily a SAL Hellfire platform. If the AGM-114L is available in the loadout, it would require external radar data or specific mission constraints (or might not be employable). *Correction:* The OH-58D typically does not carry the L model in standard configuration; it carries SAL missiles (K/M/N). The L is widely associated with the Longbow Apache. Users should stick to SAL variants for the Kiowa.

---

## 2. Rockets (Hydra 70 & APKWS)

Carried in 7-tube launchers (M260).

### Hydra 70 (Unguided)
- **Type:** 2.75-inch (70mm) Unguided Folding-Fin Aerial Rocket.
- **Warheads:**
  - **M151 HE:** 10lb High Explosive (anti-personnel/material).
  - **M229 HE:** 17lb High Explosive (larger warhead, less range/more drop).
  - **M282 MPP:** Multi-Purpose Penetrator (light armor/bunkers).
  - **M156 WP:** White Phosphorus (marking/smoke/incendiary).
  - **M257/M278:** Illumination flares (Overt/IR).
- **Effective Range:** 1,500m to 4,000m (can go further, but accuracy degrades significantly).
- **Best Suited For:** Area suppression, soft targets, trucks, infantry, marking targets (WP).
- **Simulation Constraints:** 
  - Unguided. Requires accurate aircraft ballistics calculation.
  - The OH-58D provides a CCIP (Continuously Computed Impact Point) reticle ("I-beam") for rockets in the HUD/display, making them fairly accurate compared to older helos.
  - Vulnerable to wind drift.

### APKWS (AGR-20A)
- **Type:** Advanced Precision Kill Weapon System (Laser-Guided Hydra 70).
- **Effective Range:** 1,500m to 5,000m+ (Requires enough energy to maneuver).
- **Best Suited For:** Precision strikes on light vehicles, technicals, snipers, or specific windows/doors. Low collateral damage compared to Hellfire.
- **Simulation Constraints:** 
  - **Requires Laser Designation.**
  - The rocket must be fired into a "basket" where it can see the laser spot.
  - It is essentially a mini-missile.
  - In DCS, select the appropriate laser code (PRF) to match the designator (MMS or external).
  - Limited maneuverability compared to Hellfire; needs to be aimed relatively close to the target initially.

---

## 3. Gun System

### M3P .50 Caliber Machine Gun
- **Type:** 12.7mm (.50 BMG) Heavy Machine Gun (Podded).
- **Mount:** Fixed on the left weapons pylon.
- **Ammo Capacity:** 500 rounds.
- **Effective Range:** ~1,000m to 1,500m for point targets; up to 2,000m for area suppression.
- **Best Suited For:** Infantry, unarmored trucks, light boats, self-defense.
- **Simulation Constraints:** 
  - **Fixed Mount:** It does not traverse or articulate like the Apache's 30mm chain gun. The pilot must aim the entire helicopter to aim the gun.
  - Uses the same CCIP symbology in the display.
  - High rate of fire (~1,000+ rpm), can deplete ammo quickly.
  - Recoil can slightly affect flight profile in a hover.
  - Cannot be used simultaneously with a left-side missile/rocket loadout (it takes the pylon slot).

---

## 4. Implementation Notes for DCS World
- **MMS (Mast Mounted Sight):** The key to employing guided weapons (Hellfire/APKWS). It houses TV and Thermal (FLIR) sensors and the Laser Designator/Rangefinder. It allows the Kiowa to unmask *only* the sight while the fuselage remains behind cover (hull-down).
- **Remote Hellfire Ops:** The OH-58D is an excellent scout/designator for other shooters (Apache/Harrier/A-10).
- **Weight Management:** The Kiowa is power-limited. Carrying 4 Hellfires significantly affects performance. A common "Scout" loadout is 2x Hellfire (or 1 pod Rockets) + .50 Cal, or 2x Hellfire + 1x Rocket pod.
