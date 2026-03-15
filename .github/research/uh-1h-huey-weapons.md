# Research Dossier: UH-1H Huey Weapons & Systems

**Source Notes:**
- Based on DCS World UH-1H Huey module (Belsimtek / Eagle Dynamics).
- Focus on M60, M134, and Hydra 70 systems as requested.

## Weapon/System Categories

### Gun/Cannon Systems

| Weapon | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **M60D (Door Guns)** | 7.62mm Machine Gun (Pintle Mount) | ~800m (Suppression) / <500m (Point) | Infantry, Soft Vehicles, Self-Defense during LZ operations. | Operated by AI gunners or player (flexible aiming). Left/Right side mounting. AI can auto-engage or hold fire. Limited firing arc (side/rear). |
| **M134 Minigun (M21 Subsystem)** | 7.62mm 6-Barrel Rotary Machine Gun | 1000 - 1500m | Heavy suppression of infantry/soft targets. Cutting down light structures/foliage. | High rate of fire (selectable 2400/4000 rpm). Can be fixed-forward (Pilot fired) or flexible (Copilot/Gunner fired). Prone to rapid ammo depletion. |

### Rockets (Unguided) - Hydra 70 (2.75" FFAR)

**Launchers:**
- **XM158:** 7-tube launcher (Lightweight)
- **XM200:** 19-tube launcher (Heavy firepower)

| Warhead | Type | Effective Range | Best Suited For | Simulation Constraints |
|---|---|---|---|---|
| **M151 HE** | High Explosive (10lb) | 1.5 - 3km (Area) / <1.5km (Point) | General purpose, infantry in open, light vehicles, unarmored trucks. | Standard HE rocket. Requires manual ballistic compensation (reflex sight). |
| **M229 HE** | High Explosive (17lb) | 1.5 - 3km | Larger blast radius than M151. Better against structures or dug-in infantry. | Heavier warhead changes ballistic trajectory slightly compared to M151. |
| **M156 WP** | White Phosphorus | 1.5 - 3km | Target marking, smoke screening, incendiary effect against fuel/ammo dumps. | Creates significant smoke. Burning effect on soft targets. Good for marking for other aircraft. |
| **M257 / M278** | Illumination Flare | Varies (deploy altitude) | Night operations, battlefield illumination. | Parachute retards descent. M257 (Visible), M278 (IR) - check module specific availability. Aim high to deploy over target area. |
| **M259** | Smoke (Screening) | 1.5 - 3km | Creating smoke screens to obscure friendly movements. | - |

### Simulation & Tactical Notes
- **Aiming:** The pilot uses a simple reflex sight for fixed forward weapons (Miniguns in stowed position, Rockets). No CCIP/CCRP. Rocket accuracy depends entirely on pilot skill in estimating drop and windage.
- **Crew Coordination:** Effective use of the M21 flexible guns requires switching to the co-pilot seat or using AI orders to direct fire.
- **Weight Management:** Fully loaded XM200 pods + Miniguns significantly affect flight performance (hover capability), especially in hot/high conditions.
