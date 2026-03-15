I need you to take the research data available in `.github/research/[aircraft_name]-data.md` and `.github/research/[aircraft_name]-weapons.md` and format it into the final Markdown tables for the [INSERT AIRCRAFT NAME] checklist.

**Inputs:**
- Research Dossier: `.github/research/[aircraft_name]-data.md` (Operating Limits, V-Speeds, Emergency Procedures)
- Research Dossier: `.github/research/[aircraft_name]-weapons.md` (Weapons, Systems, Munitions)

**Goal:**
Create clean, formatted Markdown tables that match the repository's style guide. Do not include raw research notes—synthesize them into concise table cells.

### Table 1: Operating Limitations
| Parameter | Limit | Notes |
|---|---|---|
| *e.g., Max Takeoff Weight* | *e.g., 47,600 lbs* | *Runway condition dependent* |

### Table 2: Performance & V-Speeds
| Regime | Speed (KIAS) | Configuration / Notes |
|---|---|---|
| *e.g., Rotation (Vr)* | *135* | *Clean, 50% fuel* |

### Table 3: Emergency Procedures (Immediate Action)
| Emergency | Immediate Action Steps |
|---|---|
| *e.g., Engine Fire* | 1. **Throttle** — IDLE<br>2. **Fire Handle** — PULL<br>3. **Agent** — DISCHARGE |

### Table 4: Weapons & Stores
| Weapon / System | Type | Effective Range | Best Suited For | Simulation Notes |
|---|---|---|---|---|
| *e.g., GBU-12* | *LGB* | *~5 NM* | *Pinpoint strike* | *Requires laser code 1688 set in kneeboard* |

**Formatting Rules:**
- Use `<br>` for multi-line steps within a single table cell.
- Bold key controls/switches (e.g., **Master Arm**).
- If the research notes a discrepancy between Real World and DCS, stick to the DCS-functional value but add a footnote symbol (e.g., `*`).
- Footnotes for discrepancies should be generated as a "Realism Notes" list below the tables.

**Output:**
Provide the tables and the Realism Notes section ready to copy-paste into the final checklist file.
