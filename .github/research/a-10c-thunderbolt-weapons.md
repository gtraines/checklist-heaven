# Research Dossier: A-10C / A-10C II Thunderbolt II Weapons & Systems

**Source Notes:**
- Primary data based on DCS World A-10C II Tank Killer Flight Manual (Eagle Dynamics).
- Real-world USAF A-10C Dash-1 (T.O. 1A-10C-34-1-1).
- **Discrepancy Note:** The DCS A-10C and A-10C II are high-fidelity modules.
  - **A-10C:** Standard Mavericks, JDAMs, LGBs.
  - **A-10C II:** Adds **APKWS** (Laser Guided Rockets), **HMCS** (Helmet Mounted Cueing System), and **GBU-54** (LJDAM).
- **DSMS:** Weapons are managed via the Digital Stores Management System (DSMS) and Multifunction Color Displays (MFCD).

## Weapon/System Categories

### Gun/Cannon
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **GAU-8/A Avenger** | 30mm Gatling Gun | < 2 NM | **Primary Anti-Armor Weapon.** Tanks, IFVs, Bunkers. | Massive recoil slows aircraft. 1,150 rounds. PAC (Precision Attitude Control) stabilizes aiming. |

### Air-to-Ground Missiles
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **AGM-65D/G** | IR Guided (Heat) | 6-8 NM | Moving Armor, Night Ops, Ships (G). | Force Correlate (G) for large targets. Require lock via MFD. |
| **AGM-65H/K** | TV Guided (CCD) | 4-6 NM | Daylight only. High contrast targets. | K = Heavy Warhead; H = Light Warhead. Force Correlate available. |
| **AGM-65L** | Laser Maverick | 6-8 NM | Buddy Lasing, Designated targets. | Requires laser code match. (A-10C II can self-lase easily). |

### Rockets (Guided & Unguided)
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **APKWS (M151/M282)** | Laser Guided Rocket | 2-5 NM | **Precision Strike (Light Armor/Trucks).** | **A-10C II Only.** Requires laser code. Very accurate, low collateral. |
| **Hydra 70 (M151)** | 2.75" HE Rocket | 1-2 NM | Soft targets, suppression. | Area effect. CCIP aiming. |
| **Hydra 70 (M257)** | Illumination Flare | Overhead | Battlefield Illumination. | Parachute flare. |
| **Hydra 70 (M274)** | Smoke (White Phosphorus) | 1-2 NM | Marking targets for FAC. | "Willie Pete". |

### Guided Bombs (JDAM / LGB)
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **GBU-38 (JDAM)** | GPS/INS Guided (500 lb) | 5-10 NM | All weather, coordinate strikes. | Requires alignment. Drop on coordinate (SPI). |
| **GBU-31 (JDAM)** | GPS/INS Guided (2000 lb) | 5-10 NM | Heavy structures, bridges. | Massive blast. |
| **GBU-54 (LJDAM)** | Laser/GPS Hybrid (500 lb) | 5-10 NM | **Moving Targets.** | **A-10C II Only.** Can update guidance mid-flight via laser. |
| **GBU-12** | Laser Guided Bomb (500 lb) | Varies | Precision point targets. | Requires TGP lasing or Buddy Lase. |
| **GBU-10** | Laser Guided Bomb (2000 lb) | Varies | Heavy bunkers. | Requires TGP lasing. |

### Unguided Bombs
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **Mk-82** | 500 lb GP (Low Drag) | CCIP / CCRP | General Purpose. | Standard slick bomb. |
| **Mk-82AIR** | 500 lb High Drag | Low Level | Low-altitude, high-speed passes. | Ballute slows bomb. |
| **CBU-87 (CEM)** | Cluster Bomb | Area | Soft targets, Trucks. | Height of Burst (HOB) configurable in DSMS. |
| **CBU-97 (SFW)** | Sensor Fuzed | Area | **Heavy Armor Columns.** | Deploys skeets. Devastating against tank columns. |
| **CBU-103/105 (WCMD)** | GPS Guided Cluster | 5-8 NM | Stand-off cluster delivery. | **Wind Corrected Munitions Dispenser.** Accurate cluster delivery from altitude. |

### Pods & Systems
| System | Type | Capability | Notes |
|---|---|---|---|
| **Litening II TGP** | Targeting Pod | FLIR / CCD / Laser | Essential for self-lasing (LGBs) and long-range ID. | Use TMS/DMS HOTAS commands to operate. |
| **HMCS** | Helmet Mounted Cueing | HMD / Cueing | **A-10C II Only.** See targets through airframe. Slew sensors to look. | "Look-and-shoot" capability with APKWS/Aim-9. |
| **ALQ-131 / ALQ-184** | ECM Pod | Electronic Countermeasures | Jamming. | Reduces enemy radar lock range. |
| **AIM-9M** | IR AA Missile | < 5 NM | Self Defense. | Short range. |
