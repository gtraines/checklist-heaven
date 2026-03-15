# Research Dossier: Sukhoi Su-25 Frogfoot (Standard) Weapons & Systems

**Source Notes:**
- Primary data based on DCS World Su-25 Module (Flaming Cliffs 3 / MAC).
- This is the standard "Grach" variant, **NOT** the Su-25T.
- **Key Difference:** Lacks the Shkval TV system and Vikhr missiles. Targeting relies on visual acquisition and the internal "Klen-PS" laser rangefinder/designator.
- **Cockpit:** Non-clickable in DCS.

## Weapon/System Categories

### Air-to-Air Missiles
| Weapon | Type | Effective Range (DCS) | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **R-60M (AA-8 'Aphid')** | IR Homing (Short Range) | < 3 km (Rear aspect)<br>< 1-1.5 km (All aspect) | Self-defense against helicopters or unaware subsonic aircraft. | Very short range. Highly susceptible to flares. Small warhead (requires direct hit or very close proximity). |

### Air-to-Ground Missiles (Laser Guided)
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **Kh-25ML (AS-10 'Karen')** | Semi-Active Laser Homing | 8-10 km | Precision strike on light armor, bunkers, SAM radars. | Requires continuous laser designation from Klen-PS. Pilot must keep nose pointed at target (laser has limited gimbal limits). |
| **Kh-29L (AS-14 'Kedge')** | Semi-Active Laser Homing | 8-10 km | Hardened targets, bridges, heavy industrial structures. | Massive 320kg HE warhead. Heavy drag/weight affects aircraft handling. Requires continuous laser. |
| **S-25L** | Laser Guided Rocket | 3-7 km | Pinpoint strike on specific bunkers or windows. | A variant of the S-25 heavy rocket with a laser seeker. Requires laser lock. |

### Unguided Bombs
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **FAB-100 / 250 / 500** | General Purpose (HE) | Overflight / Dive | Soft targets, infantry, light vehicles, buildings. | Aimed via CCIP (Continuously Computed Impact Point). Very accurate in stable dive. |
| **RBK-250 / 500** | Cluster Bomb Dispenser | Area Effect | Concentrations of soft targets/light armor. | Deploys bomblets (PTAB/AO) over an area. Ineffective against heavy armor (MBTs) in DCS. |
| **BetAB-500** | Concrete Piercing | Precision (Dive) | Runways, hardened shelters. | Rocket booster fires after release to penetrate concrete. |
| **KMGU-2** | Submunition Dispenser | Overflight | Soft area targets (convoys). | Dispenses small mines/bomblets in a linear pattern. |
| **SAB-100** | Illumination Bomb | High Altitude | Night operations flare support. | Drops on parachute to illuminate target area. |

### Rockets
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **S-5** | 57mm Unguided | < 1-1.5 km | Infantry, soft trucks. | Low damage, high spread. Fired in large salvos. Obsolete against armor. |
| **S-8** | 80mm Unguided | 1.5-2.5 km | Light armor (BMP/APC), Trucks. | Standard reliable rocket. Good balance of quantity and punch. |
| **S-13** | 122mm Unguided | 1.5-3 km | Light bunkers, light armor. | Heavier punch, fewer rockets (5 per pod). |
| **S-24** | 240mm Heavy Rocket | 2-3 km | Hardened points, buildings. | Single rocket per pylon. Massive HE effect. Accurate with laser ranging. |
| **S-25** | 340mm Heavy Rocket | 2-3 km | Very hard targets. | Extremely heavy warhead. Significant drag. |

### Gun/Cannon
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **GSh-30-2** | Twin-barrel 30mm | < 1-1.5 km | Light armor (BMP/APC), Trucks. | Fixed internal cannon. High rate of fire (3000 rpm). Limited ammo (250 rnds). Recoil affects flight path. |
| **SPPU-22-1** | Gun Pod (GSh-23) | < 1 km | Strafing columns. | Can be depressed downwards for strafing while level. Can mount backwards to fire rearward (suppression). |

### Pods & Systems
| System | Type | Capability | Notes |
|---|---|---|---|
| **Klen-PS** | Laser Rangefinder/Designator | Laser Designation | Internal nose system. **Key Constraint:** Limited gimbal field of view. Pilot must dive at target to maintain laser lock. Not a pod. |
| **SPS-141 Gvozdika** | ECM Pod | Electronic Countermeasures | Jamming. Reduces enemy radar lock range. | Active jamming. Replaces a weapon station. |
| **SPO-15 Beryozha** | RWR | Radar Warning Receiver | Detects radar threats. | Internal system. Shows direction and type of threat. |
