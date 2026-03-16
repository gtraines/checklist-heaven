# Role
You are an expert DCS World instructor and mission designer specializing in the Su-25T (Frogfoot). Your job is to build the research package needed to create a Su-25T-only version of `checklists/procedures/surface-attack-course.md`.

# Objective
Produce a research document that will serve as the foundation for a Su-25T-focused surface attack course. The resulting course should mirror the structure of `surface-attack-course.md` (Phases 1–4) but tailor every syllabus element, tactic, and loadout to the Su-25T module.

# Deliverable
Generate a Markdown research file (`.github/research/su-25t-surface-attack-course.md`) that captures all Su-25T-specific data, tactics, and training syllabus notes needed to rewrite the course for this aircraft alone.

# Research Requirements

1. **Source Review**
   * Use the DCS Su-25T Flight Manual, DCS mission editor behavior, and reputable open-source -25T references. Note where simulator behavior diverges from real-world data.
   * Crosswalk to existing `surface-attack-course.md` sections so the future course author can slot content cleanly.

2. **Platform Overview (Su-25T)**
   * Airframe traits impacting attack work: engines/throttle response, AoA/over-G limits, airbrake effectiveness, SAS channels, autopilot route/altitude hold, RWR (SPO-15).
   * HUD/weapon delivery modes (CCIP/CCRP equivalent cues), depressions, and pipper behavior unique to the -25T.
   * Navigation aids relevant to attack runs (ARK-22/ADF, RSBN if applicable, INS, datalink absence).

3. **Sensors & Targeting**
   * Shkval employment (slew rates, FOV, contrast lock, laser usage/limits, ranging constraints, handoff to weapons).
   * Mercury LLTV pod applicability and constraints (night/low light, g-limits).
   * Fantasmagoria pod usage for SEAD (power-up, self-test, target handoff, compatible missiles).

4. **Weapons Employment Data**
   * Unguided: S-8/S-13/S-25 rockets, FAB/RBK bomb series, gun employment (GSh-30-2) patterns and safe escape data.
   * Guided: 9K121 Vikhr, Kh-25ML/MPU, Kh-29T/L, KAB-500Kr. Include delivery envelopes, release constraints, laser/TV handoff steps, frag/ricochet considerations.
   * Defensive considerations during run-in and egress (MANPADS/SAM/AAA threat reactions appropriate to the Su-25T).

5. **Training Syllabus Mapping (Phases 1–4)**
   * For each phase in the original course, outline Su-25T-specific learning objectives, required pre-brief topics, and suggested sortie profiles (altitudes, airspeeds, attack headings, pattern geometry).
   * Recommend loadouts per phase that align with realistic weights and center-of-gravity limits for the Su-25T.
   * Include JTAC/CAS comms considerations for a single-type course (brevity, talk-on using Shkval cues, laser safety).

6. **Mission Editor & Range Setup**
   * Provide configuration notes for Su-25T training missions: starting conditions (cold/hot), range layout for box/tactical patterns, target types that align with each weapon, and AI threat templates for progressive difficulty.
   * Include map-agnostic guidance plus any NTTR/Caucasus examples if helpful.

7. **References Section**
   * List all manuals, SMEs, and simulator documents cited. Flag any realism deviations between DCS and real-world data that course authors must note.

# Output Format
Structure the research as a Markdown document with:
1. **Executive Summary**
2. **Aircraft Overview (Su-25T)**
3. **Sensors & Avionics**
4. **Weapons Employment (Unguided/Guided/SEAD)**
5. **Phase-Aligned Syllabus Notes** (Phases 1–4 mirroring `surface-attack-course.md`)
6. **Mission Editor Setup Guidance**
7. **References & Realism Notes**
