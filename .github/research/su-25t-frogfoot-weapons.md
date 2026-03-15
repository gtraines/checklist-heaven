# Research Dossier: Sukhoi Su-25T Frogfoot Weapons & Systems

**Source Notes:**
- Primary data based on DCS World Su-25T Module documentation (Eagle Dynamics).
- Comparisons made to real-world Su-25 "Grach" capability where relevant, though the 'T' model is specifically the "Tank Buster" variant with advanced avionics (Shkval, Vikhr).
- **Discrepancy Note:** The Su-25T in DCS is a "free" module but models complex systems like the Shkval and Vikhr missile very accurately. However, it lacks a clickable cockpit, so weapon selection is via keyboard/HOTAS commands, not cockpit switches.

## Weapon/System Categories

### Air-to-Air Missiles
| Weapon | Type | Effective Range (DCS) | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **R-60M (AA-8 'Aphid')** | IR Homing (Short Range) | < 3-5 km (Rear aspect)<br>< 1-2 km (All aspect limited) | Self-defense against helicopters or slow movers. Very short legs against fighters. | Requires IR seeker lock tone. Limited off-boresight capability compared to modern missiles (AIM-9X/R-73). |
| **R-73 (AA-11 'Archer')** | IR Homing (Short/Med) | < 10-15 km | High off-boresight dogfighting. | Helmet Mounted Sight (HMS) not available in Su-25T (unlike Su-27/33). Seeker must lock target. |

### Air-to-Ground Missiles
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **9A4172 Vikhr** | Laser Beam Riding (Supersonic) | 8-10 km (Day)<br>6-8 km (Night w/ LLTV) | **Primary Anti-Tank Weapon.** MBTs, IFVs, slow helicopters. | Requires continuous laser designation (Shkval). Must fly relatively straight at target during guidance (beam rider). Carried in 8-tube launchers (APU-8). |
| **Kh-29L (AS-14 'Kedge')** | Semi-Active Laser Homing | 8-10 km | Hardened bunkers, bridges, ships. Massive warhead (320kg HE). | Requires Shkval laser lock. "Heavy" missile flight characteristics. |
| **Kh-29T (AS-14 'Kedge')** | TV Guided | 8-12 km | Same as 'L' but Fire-and-Forget. Good for high-threat environments (pop-up attack). | Contrast lock required. Cannot be used at night (TV seeker). |
| **Kh-25ML (AS-10 'Karen')** | Semi-Active Laser Homing | 8-10 km | General purpose precision strike (Light bunkers, armor). | Lighter than Kh-29. Requires continuous laser. |
| **Kh-25MPU (AS-12 'Kegler')** | Anti-Radiation (Passive Radar) | 20-40 km | SEAD (Suppression of Enemy Air Defenses). Targets radar emitters. | Requires Phantasmagoria pod to detect emitters. Lock and fire. |
| **Kh-58 (AS-11 'Kilter')** | Anti-Radiation (Passive Radar) | 40-100+ km | Long-range SEAD. High-value SAM sites (Patriot, S-300 radars). | Requires Phantasmagoria pod. Fire and forget once locked. |

### Unguided Bombs
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **FAB-100 / 250 / 500** | General Purpose (HE) | Overflight / CCIP | Soft targets, infantry, light vehicles. | CCIP (Continuously Computed Impact Point) is very accurate in Su-25T. |
| **RBK-250 / 500** | Cluster Bomb Dispenser | Area Effect | Concentrations of soft/light armor. | Area denial. Ineffective against heavy armor (MBTs) in DCS usually. |
| **BetAB-500** | Concrete Piercing | Precision (CCIP) | Runways, hardened shelters. | Rocket-assisted penetration. |
| **KMGU-2** | Submunition Dispenser | Overflight | Soft area targets (convoys). | Dispenses small mines/bomblets. |

### Guided Bombs (TV/Laser)
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **KAB-500Kr** | TV Guided Bomb | < 10 km (Glide) | Stationary hardened targets. | Fire and forget (Contrast lock). Daylight only. |

### Rockets
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **S-8 (Komar)** | 80mm Unguided | 1-2 km | Soft targets, trucks, infantry. | Fired in salvos. CCIP aiming. |
| **S-13** | 122mm Unguided | 1-2.5 km | Light bunkers, light armor. | Heavy punch, fewer rockets per pod. |
| **S-24** | 240mm Heavy Rocket | 2-3 km | Hardened points. Massive HE effect. | Single rocket per pylon. Very accurate with laser rangefinding. |
| **S-25L** | Laser Guided Rocket | 3-7 km | Precision strike on specific window/bunker vent. | "Poor man's Maverick." Requires laser lock. |

### Gun/Cannon
| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **GSh-30-2** | Twin-barrel 30mm | < 1-1.5 km | Light armor (BMP/APC), Trucks. | High rate of fire, limited ammo (250 rnds). Vibration shakes HUD. |
| **SPPU-22-1** | Gun Pod (GSh-23) | < 1 km | Strafing columns. | Can be depressed downwards for strafing while level. |

### Pods & Systems
| System | Type | Capability | Notes |
|---|---|---|---|
| **I-251 Shkval** | TV Targeting System | 23x Zoom, Auto-tracking | Nose-mounted (built-in). Day only. Laser designator included. |
| **Mercury (Merkury) LLTV** | Low Light TV Pod | Night Vision for Shkval | Mounts on centerline. Allows night usage of Shkval and Vikhr/Kh-25ML (limited range). |
| **Phantasmagoria** | ELINT / SEAD Pod | Radar Emitter Detection | Required for Kh-58/Kh-25MPU usage. Detects and hands off targets to ARMs. |
| **MPS-410** | ECM Pod | Electronic Countermeasures | Jamming. Reduces enemy radar lock range. | Active jamming. |
