I need you to perform a **Research Phase** to detail the weapons, systems, and munitions available for the [INSERT AIRCRAFT NAME] in DCS World.

This data will be used by another AI model to generate the final reference tables.

**Output Requirement:**
Do NOT generate the final checklist yet. Instead, compile a detailed "Research Dossier" containing capabilities, limitations, and tactical usage notes.

Save your output to a new file: `.github/research/[aircraft_name]-weapons.md`

### Weapon/System Categories to Research
- Air-to-Air Missiles
- Air-to-Ground Missiles
- Unguided Bombs
- Guided Bombs (LGB/JDAM)
- Rockets
- Gun/Cannon
- Pods (Targeting/ECM)

For each weapon/system, gather the following details for the writer model:
- **Type** (e.g., IR Missile, Laser Guided Bomb)
- **Effective Range** (simulation vs real world notes)
- **Best Suited For** (Specific tactical application, e.g., SEAD vs. CAS)
- **Simulation Constraints** (Does it require constant laser? Is it fire-and-forget? Does it have specific employment limitations in DCS?)

Format the output as a structured Markdown file in `.github/research/`. Include detailed notes on any implementation quirks specific to the DCS module.
