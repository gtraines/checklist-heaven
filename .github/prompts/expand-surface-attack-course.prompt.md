You are an expert aviation instructor specializing in surface attack tactics. Your task is to expand the existing `checklists/procedures/surface-attack-course.md` document with new sections on attack patterns, using the research provided in `.github/research/surface-attack-patterns.md`.

## Goal
Add detailed instructional content for:
1.  **Standard Basic Surface Attack Pattern** (Range operations).
2.  **Tactical Surface Attack Pattern** (Combat employment).

## Instructions

1.  **Read the Source Material:**
    *   Review `.github/research/surface-attack-patterns.md` to understand the key concepts, geometries, and differences between the two patterns.

2.  **Update `checklists/procedures/surface-attack-course.md`:**
    *   **Insert a New Section:** Create a new top-level section (e.g., `## Phase 1.5: Attack Patterns & Geometry` or integrate into Phase 1 and Phase 2 appropriately) to house this information. It likely fits best before or at the start of "Phase 1: Basic Surface Attack".
    *   **Standard Basic Surface Attack Pattern:**
        *   Describe the rectangular/box pattern (Crosswind, Downwind, Base, Final, Recovery).
        *   Explain key parameters (typical altitudes, speeds, spacing).
        *   Include a text-based diagram (ASCII art or code block) illustrating the pattern if possible.
    *   **Tactical Surface Attack Pattern:**
        *   Describe the "Wheel" or "Butterfly" patterns and the concept of IP-to-Target runs.
        *   Highlight the focus on unpredictability and survivability (e.g., "One pass, haul ass", jinking).
        *   Contrast this with the basic pattern.

3.  **Formatting & Style:**
    *   Maintain the existing file's tone: Professional, instructional, military aviation style.
    *   Use **bold** for key terms and actions.
    *   Use `inline code` for specific values or brevity codes.
    *   Ensure the new sections are properly linked in the Table of Contents (if the TOC is manual; if auto-generated, ensure headers are correct).
    *   Update the "Learning Objectives" in relevant phases to reflect the new material.

4.  **Verification:**
    *   Check that the new content flows logically with the existing "High-Angle Dive" and "Low-Angle Dive" sections.
    *   Ensure no existing content is overwritten or lost.

## Example Output Structure
```markdown
## Phase 1: Basic Surface Attack (Fundamentals)
...
### 1.1 Standard Basic Surface Attack Pattern
[Content from research...]
...
### 1.2 Weapons Delivery: High-Angle Dive
...
```
