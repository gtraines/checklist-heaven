I need you to perform a **Research Phase** to gather reference data for the [INSERT AIRCRAFT NAME] in DCS World. This data will be used by another AI model to generate the final checklist.

Please consult real-world technical manuals (NATOPS, Dash-1, -10) as your primary source for data, but verify against DCS World module documentation where possible.

**Output Requirement:**
Do NOT generate the final checklist yet. Instead, compile a detailed "Research Dossier" containing the following data points. Include notes on sources and any discrepancies between real-world manuals and the DCS simulation.

Save your output to a new file: `.github/research/[aircraft_name]-data.md`

### 1. Operating Limitations
Gather data for:
- Max Takeoff Weight (MTOW)
- Max Landing Weight
- G-Limits (Symmetric & Asymmetric)
- Angle of Attack (AoA) Limits
- Crosswind Component Limit

### 2. Performance & V-Speeds
Gather data for:
- Rotation Speed (Vr) - Clean vs Loaded
- Takeoff Speed
- Landing Approach Speed - Clean vs Loaded
- Corner Speed (Manuevering Speed)
- Best Climb Speed (Vy)
- Stall Speed (Vs) - Landing Configuration
- Max Speed (Vne) - Sea Level & Altitude
- Gear Extension Limit (Vlo)
- Flap Extension Limits (Vfe)

### 3. Emergency Procedures (Boldface/Immediate Action)
Gather the exact "Boldface" or "Immediate Action" steps for:
- Engine Failure on Takeoff
- Engine Fire in Flight
- Engine Failure in Flight (Restart)
- Hydraulic Failure
- Electrical Failure
- Spin Recovery
- Ejection Sequence

Format the output as a structured Markdown file in `.github/research/`. Include a "Notes" column or section for any ambiguities the checklist writer should be aware of.
