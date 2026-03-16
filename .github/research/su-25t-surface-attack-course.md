# Research: Su-25T Surface Attack Course

## Executive Summary
- Purpose: Provide Su-25T-only research to rewrite `checklists/procedures/surface-attack-course.md` (Phases 1–4) with aircraft-specific tactics, envelopes, and mission setup.
- Focus: Map the existing course flow to Su-25T capabilities (Shkval/laser, Vikhr/Kh-series/KAB, unguided rockets/bombs, SEAD with Fantasmagoria).
- Outcome: A syllabus with sortie profiles, loadouts, and mission editor setup tailored to the Su-25T’s avionics, handling, and defensive limitations.

## Aircraft Overview (Su-25T)
- Airframe/handling: Straight-wing attack jet; sluggish throttle response (non-afterburning turbofans). Plan power changes early; avoid abrupt throttle chops near the ground.
- Flight control aids: Four SAS channels (pitch, roll, yaw, altitude); use dampers on for weapons delivery. Autopilot route/altitude hold useful for transits but disengage for attack.
- AoA/over-G: Respect 6.5–7.0G limit; high AoA increases drag quickly. Airbrake effective; avoid simultaneous airbrake + max G in low-altitude jinks.
- HUD/delivery cues: CCIP/CCRP-like director for bombs/rockets; pipper depression varies with stores and barometric altitude—reconfirm after rearm. Gun cross and funnel for GSh-30-2.
- Navigation: ARK-22 ADF; no INS/DL; RSBN limited to maps that support it. Use waypoints via mission editor or simple beacon navigation. No onboard TACAN/ILS equivalent.
- Survivability: SPO-15 RWR with sector cues only; no MAWS. Limited to flares (no chaff). Plan beam/terrain masking; “one pass, haul ass” mindset.

## Sensors & Avionics
- Shkval: TV sensor, narrow/wide FOV, limited slew rate; contrast lock sensitive to sun angle/weather. Laser range/designate with duty cycle limits (~30–35s continuous; cool 30–40s). Max reliable range ~7–8 km for tanks, shorter in haze.
- Mercury LLTV pod: Optional night/low-light aid; g-limit ~4–5G practical; reduced resolution. Best for level or shallow-turn observation.
- Fantasmagoria pod: SEAD cueing for radar emitters; power-up/self-test before taxi. Provides bearing/ID; handoff to Kh-25MPU/Kh-58U (if enabled in mission). Keep emitter within azimuth gates; plan pop-up/loft if terrain masking.
- Rangefinding: Laser is primary for CCRP/CCIP accuracy with guided weapons; manage duty cycle to avoid burnout mid-sortie.

## Weapons Employment (Unguided/Guided/SEAD)
- Gun (GSh-30-2): Effective 1,200–1,800 m slant range; 10–15° dive; min recovery ~1,500–2,000 ft AGL; short bursts to avoid dispersion and overheat.
- Rockets:
  - S-8: 1.2–2.5 km slant range; 10–20° dive; salvo for area targets.
  - S-13: Heavier punch; 1.5–3.0 km; 10–20° dive; limit to stable wings-level shots.
  - S-25 (OF/OFM): Single heavy rocket; 2.0–4.0 km; 10–25°; significant recoil—stabilize before release.
- Bombs:
  - FAB-100/250/500: High-angle 20–30° from 10–14k ft MSL; release no lower than 4.5–5.0k ft AGL for frag; low-angle 10–15° from 3.5–5.0k ft AGL with longer escape.
  - RBK (PTAB/AB): Use above 1,500–2,000 ft AGL for pattern effectiveness; avoid strong crosswinds.
- Guided/ATGM:
  - 9K121 Vikhr: 6–8 km envelope; keep within ±20° off boresight; pair laser with Shkval lock; ripple in pairs for high-value threats.
  - Kh-25ML: 3–10 km; laser-guided; stabilize platform; maintain lase through TOF.
  - Kh-29L (laser): 3–10 km; heavy; expect sluggish handling post-release; continuous lase required.
  - Kh-29T (TV): 3–12 km; establish solid TV lock; maintain stable attitude to prevent break-lock.
  - KAB-500Kr: TV-guided; 3–10 km; CCRP-like release followed by steering the TV lock.
- SEAD:
  - Kh-25MPU (with Fantasmagoria): 10–40 km envelope depending on altitude; loft/pop-up to maintain emitter lock.
  - Threat reactions: Pre-brief jink directions; rely on beam maneuvers and terrain masking (no chaff carried). Time on laser carefully; minimize hot runs.

## Phase-Aligned Syllabus Notes (mirrors surface-attack-course.md)
### Phase 1: Basic Surface Attack (Fundamentals)
- Objectives: Box pattern geometry; “IN/OFF” brevity; safe escape with unguided rockets/bombs/gun; frag/ricochet awareness.
- Profiles: 
  - High-angle bombs: 20–25° from 11–13k ft MSL; release ≥4.5k ft AGL; escape 4–5G.
  - Low-angle rockets/gun: 10–15° from 3.0–4.5k ft AGL; cease fire no lower than 1.5–2.0k ft AGL.
- Loadouts: 2×B-8 (S-8), 2×FAB-250, gun full; optional SPS-141 jammer if mission allows.
- Notes: Keep dampers ON; trim before roll-in; manage laser cooling even if unused early.

### Phase 2: Intermediate Surface Attack (Precision & Systems)
- Objectives: Shkval target work; CCRP/CCIP accuracy with laser ranging; guided weapon employment (Vikhr, Kh-25ML, Kh-29L/T, KAB-500Kr).
- Profiles:
  - Vikhr/Kh-25ML: 1,500–3,000 m AGL, 5–15° shallow dive or level; maintain line-of-sight and lase through TOF.
  - KAB-500Kr/Kh-29T: Level/shallower dives; TV lock prior to release; keep wings stable to avoid break-lock.
- Loadouts: 2–4×Vikhr on twin racks, 2×Kh-25ML or 2×Kh-29T, 1×Mercury (as needed), gun.
- Notes: Laser duty-cycle discipline; practice re-caging Shkval and boresight slews; rehearse “laser fail—continue dry” calls.

### Phase 3: CAS & JTAC Coordination
- Objectives: 9-Line execution; talk-on using Shkval cues; keyhole CAS geometry; deconfliction with a single-type flight.
- Profiles: Low/medium altitude holds (8–12k ft MSL); IP-to-target runs 10–15 NM; use rockets/bombs for area, Vikhr/Kh-25 for points.
- Loadouts: Mixed S-8 + Vikhr + Kh-25ML; smoke rockets optional for marks; flares priority over weight.
- Notes: Shkval narrow for PID; avoid long laser dwell waiting for clearance; use terrain masking to offset limited self-protection.

### Phase 4: Airborne FAC-A (Platform-Limited)
- Objectives: Manage stack with SPO-15 awareness; mark with rockets/smoke; coordinate single-type shooters; pass target data (bearing/range/landmark) using Shkval references.
- Profiles: Holds 10–15k ft MSL offset 3–5 NM; pop to mark then egress; “one-pass” mindset to reduce threat exposure.
- Loadouts: Smoke rockets or S-8 for marking, limited Vikhr/Kh-25 for self-escort, gun. Keep fuel light to preserve handling.
- Notes: No datalink—use clear, concise brevity; emphasize visual/landmark talk-ons and laser safety calls.

## Mission Editor Setup Guidance
- Starts: Provide cold start at main base and hot start at range/FOB for reps. Enable ground power for quick power-up (platform lacks INS alignment).
- Range layout: 
  - Box pattern lanes ~5×3 NM with initial/final headings marked by smoke or range towers.
  - Tactical pattern anchor points for wheel/butterfly (IP, egress, hold) with altitude blocks.
- Targets by phase:
  - Phase 1: Truck convoys, soft targets, strafe pits, open-area bomb circles.
  - Phase 2: Tanks/IFVs for Vikhr, hardened bunkers for Kh-25/29, static ships/bridges as heavy aimpoints, radar emitters for SEAD drills.
  - Phase 3: Urban blocks or cluttered areas for talk-ons; place JTAC with laser off by default to force pilot marking.
  - Phase 4: FAC-A stack with mixed AI shooters; use smoke-on-map triggers for marks.
- Threat templates: Start with MANPADS/AAA light; add short-range SAMs (Strela/OSA), then medium (Kub/Buk) for SEAD reps. Provide “threat rings” via mission marks.
- Maps: Keep guidance map-agnostic; optional NTTR/Caucasus examples—use RSBN/ADF beacons where available.

## References & Realism Notes
- DCS Su-25T Flight Manual (Eagle Dynamics).
- Su-25/Su-25T open-source operator data (public, unclassified).
- MCWP 3-23.1 / JP 3-09.3 for CAS brevity and geometry (applied to Su-25T where relevant).
- Realism notes: Su-25T in DCS includes Vikhr/SEAD options not fielded widely on baseline Su-25; note as simulation-specific. SPO-15 fidelity and laser cooling modeled approximately—verify in-mission. RSBN availability varies by map; use ADF when absent.
