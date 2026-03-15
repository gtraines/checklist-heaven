# Role
You are a military aviation researcher gathering technical data for a simulated flight training course.

# Task
Conduct detailed research on Basic and Intermediate Surface Attack, Close Air Support (CAS), and Forward Air Controller (Airborne) (FAC-A) procedures for the following aircraft in DCS World:
- **US:** A-10C / A-10C II, A-10A
- **Russian:** Su-25, Su-25T

**Do NOT generate the training course itself.** Your output must be a compiled research document saved to `@.github/research/surface-attack-data.md`.

# Research Requirements

## 1. Weapons Delivery Parameters
Gather data for both US (CCIP/CCRP) and Russian (Visual/Continuously Computed) delivery modes.
- **Dive Angles:** Standard high-angle (30-45°) and low-angle (10-20°) parameters.
- **Altitudes:** Release altitudes and "min recovery altitudes" for safe escape from fragmentation.
- **Speed:** Recommended release airspeeds for unguided bombs (Mk-82, FAB-100/250/500), rockets, and guns.
- **Switchology:**
    - A-10C/II: HUD modes, DSMS profiles, Laser code settings.
    - Su-25/T: Weapon selector panel usage, Laser rangefinder/designator modes.

## 2. Sensor & Precision Systems
- **Targeting Pods (TGP):** Key workflows for A-10C (Point/Area track, Laser designation).
- **Shkval/Mercury:** Key workflows for Su-25T (Slew, Lock, Laser usage).
- **Maverick/Vikhr:** Employment envelopes (min/max range) and constraints.

## 3. Close Air Support (CAS) Standards
Research current simulated doctrine (based on JP 3-09.3 / JFIRE where applicable to DCS).
- **CAS Check-In:** Format and required information.
- **The 9-Line:** Structure of the standard Fixed-Wing CAS 9-Line.
- **Keyhole CAS:** Diagram/explain the "Keyhole" template (Alpha-Echo holding points).
- **Brevity Codes:** List essential CAS brevity (e.g., "In," "Off," "Rifle," "Pickle," "Tally," "Visual," "Contact").

## 4. Forward Air Controller (Airborne)
- **Marking:** Procedures for marking targets with WP rockets (Willie Pete) or Laser (Sparkle).
- **Talk-On:** Techniques for guiding other pilots' eyes to the target.
- **Deconfliction:** Standard altitude blocks or lateral separation methods.

# Output Format
Compile all findings into a structured markdown file at `@.github/research/surface-attack-data.md`.
- Use clear headers for each aircraft/topic.
- Include tables for quick-reference numbers (e.g., "Weapon Release Parameters").
- Note any specific DCS quirks or limitations (e.g., A-10A lacking advanced TGP features).
