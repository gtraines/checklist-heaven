You are an expert DCS World mission designer and aviation instructor.

Your task is to conduct research to identify the best locations on the **DCS: Nevada Test and Training Range (NTTR)** map to conduct the practical exercises outlined in `checklists/procedures/surface-attack-course.md`.

## Goal
Generate a research document (`.github/research/nttr-training-ranges.md`) that maps specific NTTR locations to the four phases of the surface attack course.

## Research Requirements

### 1. Map Analysis (NTTR)
Identify suitable operating areas for each course phase. Focus on standard DCS map locations, landmarks, and existing range infrastructure.

*   **Phase 1 (Basic Surface Attack):** Needs a formal weapons range with a clear run-in line, scoring towers (visual references), and open desert for safe aborts. The "Box Pattern" requires roughly 5NM x 3NM of clear airspace.
    *   *Candidate areas to investigate:* Range 61, Range 62, Range 63B (The Container Village).
*   **Phase 2 (Intermediate/Precision):** Needs distinct targets for sensor acquisition (TGP/Shkval). Hardened targets (bunkers) and vehicle shapes.
    *   *Candidate areas:* Dreamland (Range 64), Tolicha Peak.
*   **Phase 3 (CAS & JTAC):** Needs complex terrain or urban clutter for realistic "Talk-On" and target ID difficulties.
    *   *Candidate areas:* Goldfield, Tonopah Test Range (TTR) airfield environs, or urban mockups in the ranges.
*   **Phase 4 (FAC-A):** Needs an area suitable for holding stacks (Angels 15-20) with clear sightlines for the FAC-A.

### 2. Location Details
For each identified location, provide:
*   **Name/Designator:** (e.g., "Range 62")
*   **Coordinates:** MGRS and Lat/Long (approximate is fine).
*   **Elevation:** Ground elevation in feet.
*   **Nearest Airfield:** (e.g., Creech AFB, Nellis AFB).
*   **Navigation Instructions:**
    *   Heading/Distance from nearest TACAN (e.g., "BTY 240 for 15 NM").
    *   Visual landmarks for VFR approach.

### 3. Scenario Setup Notes
For each location, describe what *Mission Editor* objects would need to be placed to make the scenario work.
*   *Example:* "Place a group of red smoke markers at the run-in line start."
*   *Example:* "Place static T-72 tanks in the open at Range 63 for Maverick practice."

## Output Format
Structure the research as a Markdown document with sections for each Phase.

```markdown
# Research: NTTR Locations for Surface Attack Training

## Phase 1 Location: [Name]
*   **Coordinates:** ...
*   **Access:** Depart Creech AFB, fly Hdg 310 for 10 NM...
*   **Suitability:** Excellent for box patterns due to...
*   **Required Scenery:** Standard range targets are present.

...
```
