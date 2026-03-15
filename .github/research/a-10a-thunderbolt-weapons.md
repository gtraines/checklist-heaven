# Research Dossier: A-10A Thunderbolt II Weapons & Systems

**Source Notes:**
- Primary data based on DCS World A-10A Flight Manual (Eagle Dynamics/Flaming Cliffs 3).
- Real-world USAF A-10A Dash-1 (T.O. 1A-10A-34-1-1) used for capability comparison.
- **Discrepancy Note:** The A-10A in DCS is a "FC3" module with non-clickable cockpit. Weapons are selected by cycling through stores (`D`), not via DSMS/MFD like the A-10C. Targeting Pod (TGP) is NOT available on the A-10A; Mavericks use their own seeker heads for targeting.

## Weapon/System Categories

### Gun/Cannon
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **GAU-8/A Avenger** | 30mm Gatling Gun | < 1.5 - 2 NM | **Primary Anti-Armor Weapon.** Tanks, IFVs, Bunkers. | Massive recoil slows aircraft. 1,150 rounds standard (Combat Mix: API/HEI). CCIP aiming in HUD (Gun Cross). |

### Air-to-Ground Missiles
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **AGM-65D Maverick** | IR Guided (Heat) | 6-8 NM | **Moving Armor**, Night Ops. Tanks, SAMs (Short Range). | Use built-in IR seeker (`Enter` to lock). Polarity (White/Black Hot) switchable. |
| **AGM-65H/K** | TV Guided (CCD) | 4-6 NM (H)<br>6-10 NM (K - Heavy) | Daylight only. High contrast targets. | 'K' model has heavy warhead (300 lb) for bridges/bunkers. 'H' is light warhead (125 lb). |
| **AGM-65G** | IR Guided (Heavy) | 6-8 NM | Large targets (Ships, Bunkers). | Heavy warhead + IR seeker. Good for night strikes on structures. |

### Air-to-Air Missiles
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **AIM-9M Sidewinder** | IR Homing | < 5 NM | Self-defense vs Helicopters / Slow Movers. | Seeker tone required. |

### Unguided Bombs
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **Mk-82** | 500 lb GP (Low Drag) | CCIP / CCRP | General Purpose. Trucks, Infantry, Light Armor. | Standard "slick" bomb. Dive toss or level release. |
| **Mk-82AIR (BSU-49)** | 500 lb High Drag | Low Level | Low-altitude, high-speed passes. | Ballute slows bomb to allow safe separation. |
| **Mk-84** | 2,000 lb GP | CCIP / CCRP | Large structures, bridges. | Massive blast radius. |
| **CBU-87 (CEM)** | Cluster Bomb | Area | Armor columns, soft target concentrations. | Combined Effects Munition (Armor/Personell/Incendiary). |
| **CBU-97 (SFW)** | Sensor Fuzed Weapon | Area | **Heavy Armor Columns.** | Deploys skeets that seek heat sources. "Tank Plinking" weapon. |

### Rockets
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **Hydra 70 (M151)** | 2.75" HE Rocket | 1-2 NM | Soft targets, trucks, suppression. | Fired from LAU-68 (7-tube) or LAU-131 (7-tube). CCIP aimed. |
| **Hydra 70 (M257)** | Illumination Flare | Overhead | Battlefield Illumination at night. | Parachute flare. |
| **Hydra 70 (M274)** | Smoke (White Phosphorus) | 1-2 NM | Marking targets for FAC/CAS. | "Willie Pete". |

### Pods & Systems
| System | Type | Capability | Notes |
|---|---|---|---|
| **ALQ-131 / ALQ-184** | ECM Pod | Electronic Countermeasures | Jamming enemy radar. | Active jamming reduces lock range. |
| **Pave Penny (TISL)** | Laser Spot Tracker | Laser Detection Only | **Not a designator.** Detects laser energy from JTAC/Other aircraft and puts a diamond in HUD. | Cannot self-designate for LGBs (GBU-10/12). A-10A can drop LGBs only if someone else lases (Buddy Lasing). |
