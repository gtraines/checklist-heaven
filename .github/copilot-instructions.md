# Copilot Instructions — checklist-heaven

This repository is a collection of **Markdown-based aviation checklists** for DCS World simulation. There is no build system, test suite, or linter — all content is static Markdown.

## Repository Structure

```
checklists/
  index.md               # Master index — links to all aircraft and procedures
  aircraft/              # One .md file per aircraft
  procedures/            # Standalone procedure docs (CAS, radio comms, ATC)
```

## Checklist File Conventions

Every checklist file follows the same structure:

1. **Header block** with aircraft name, role, and a back-link to `../index.md`:
   ```markdown
   # Aircraft Name — DCS Checklist

   > **Aircraft:** Full name | **Role:** Role description
   >
   > [← Back to Index](../index.md)
   ```

2. **Table of Contents** with numbered entries linking to `##` sections via GitHub-style anchors (spaces → `-`, special chars stripped, `&` → omitted).

3. **Section separator** (`---`) between every major section.

4. **Checklist items** use `- [ ]` task list syntax with the control/key in bold and the action after an em dash:
   ```markdown
   - [ ] **Master Arm** — ARM (`O` key)
   ```

5. **Keyboard references** are always inline code: `` `G` ``, `` `LAlt + J` ``.

6. **Tables** use the pattern `| Column | Column |` with a separator row `|---|---|`.

7. **Cockpit diagrams** use fenced code blocks with ASCII art.

8. **Cross-references** section at the bottom of each aircraft file links to related procedures and related aircraft.

9. **Footer** is an italicized disclaimer: `*Based on Eagle Dynamics DCS ... documentation. For simulation use only.*`

## Source Prioritization

- **Target Simulation:** Eagle Dynamics' DCS World (Digital Combat Simulator) is the default target unless otherwise specified.
- **Primary Source:** Real-world US Military Technical Manuals (e.g., NATOPS, Dash-1, -10 operator manuals). Use these for structure, phraseology, and procedural depth.
- **Secondary Source:** Flight simulator module documentation (DCS, BMS, etc.) for simulation-specific quirks or keybinds.
- **Tone:** Maintain a professional, military aviation tone. Use standard brevity codes and terminology where applicable.
- **Conflict Resolution:** When official military documentation contradicts the flight simulator behavior/documentation:
  1. **Follow the Simulator:** The checklist step must work in the sim.
  2. **Note the Disagreement:** Add a brief note or symbol (e.g., `*`) at the step.
  3. **Detailed Footnote:** Add a section at the end of the file (e.g., `## Realism Notes`) discussing the discrepancy in detail.

## Research Workflow

The directory `.github/research/` is available for saving intermediate research outputs. Use this when:
- Synthesizing large technical manuals (NATOPS, Dash-1) into raw data.
- Passing context between different AI models (e.g., using a high-context model for research and a reasoning model for checklist generation).
- Storing reference tables, raw procedure dumps, or extracted performance data before formatting it into the final checklist structure.

## Index Maintenance

When adding a new aircraft or procedure file:
- Add a row to the table in `checklists/index.md`
- Add a row to the table in `README.md`
- Link back to `../index.md` from the new file's header block

## Naming Conventions

- Aircraft files: `{manufacturer-model}.md` in lowercase kebab-case (e.g., `mi-24-hind.md`, `a-10c-ii.md`)
- Procedure files: descriptive kebab-case (e.g., `radio-communications.md`)
- Section anchors follow GitHub Markdown rules: lowercase, spaces to hyphens, punctuation stripped (except hyphens), `&` dropped and surrounding spaces collapsed to one hyphen
