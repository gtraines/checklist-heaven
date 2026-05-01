# Event 7 — Night Weapons Employment

> **Course:** UH-1H Huey Weapons Employment Course | **Event Type:** Simulator (Flight — Night)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents

1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — Night Systems & NVG Operations Review](#part-1--night-systems--nvg-operations-review)
4. [Part 2 — Night Departure & Range Transit](#part-2--night-departure--range-transit)
5. [Part 3 — M257 Illumination Rocket Employment](#part-3--m257-illumination-rocket-employment)
6. [Part 4 — WP at Night](#part-4--wp-at-night)
7. [Part 5 — Night Rocket Attack (NVG)](#part-5--night-rocket-attack-nvg)
8. [Part 6 — Night Minigun Pass](#part-6--night-minigun-pass)
9. [Part 7 — Night Door Gun (Crew Coordination)](#part-7--night-door-gun-crew-coordination)
10. [Completion Standards](#completion-standards)
11. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:

- [ ] Configure the DCS UH-1H for night operations including NVG activation and cockpit lighting adjustment
- [ ] Set up and employ the M257 illumination rocket for battlefield illumination
- [ ] Fire a WP marking rocket at night and call the mark using NVG visual reference
- [ ] Conduct a night rocket attack using NVG; identify the additional altitude and airspeed margins required
- [ ] Conduct a night minigun pass; explain how NVG tracer visibility differs from daytime
- [ ] Apply night crew coordination standards; state the additional callouts required for night door gun operations

---

## Ground Brief

### Mission Profile

1. Night systems review (verbal quiz, 3 questions)
2. DCS night configuration: set mission time to 0200 local; no moon or partial moon to increase training value
3. Cold-dark startup; cockpit lights adjusted; NVG activated
4. Night departure; transit at 1,000 ft AGL
5. Illumination rocket: M257 employment; 1 pass; illuminate a designated area
6. WP mark at night: 1 rocket; mark call with NVG reference
7. Night rocket attack: 3 passes (10° dive); NVG; apply night parameters
8. Night minigun: 2 passes; tracer walk under NVG
9. Night door gun: 1 orbit engagement; crew coordination with NVG callouts
10. Return; night landing; debrief

### Key Numbers Table

| Parameter | Value | Notes |
|---|---|---|
| **NVG activation (DCS)** | Backtick `` ` `` key | Toggles NVG on/off; requires NVG-equipped loadout in mission |
| **Cockpit lighting** | Reduce to minimum | Avoid cockpit light wash on NVG image |
| **Night orbit altitude (10° dive)** | +200 ft vs. day | 1,200–1,400 ft AGL vs. 1,000–1,200 ft day |
| **Night airspeed margin** | +10 KIAS vs. day | 90 KIAS night vs. 80 KIAS day (optional IP direction) |
| **Night pull-off altitude** | +100 ft vs. day | 400 ft AGL floor (10° dive) vs. 300 ft day |
| **M257 burst altitude** | 600–800 ft AGL | Too low = insufficient illumination arc; too high = rapid burnout |
| **M257 illumination duration** | ~120 seconds | Plan second rocket before first expires for continuous illum |
| **WP at night — hazard** | Burning phosphorus visible 10+ km | PID is harder at night; confirm target before firing |
| **Danger close — WP** | 300 m | Unchanged from day; more critical at night (limited visibility) |
| **NVG visibility — tracers** | Tracers very bright under NVG | Tracer wash can temporarily degrade NVG image |

### Night vs. Day Comparison

| Factor | Day | Night (NVG) |
|---|---|---|
| Target identification | Visual; 2–5 km | NVG; 1–2 km effective; dependent on illumination and ambient light |
| Depression setting | Standard tables | Same tables — ballistics unchanged |
| Orbit altitude | 1,000–1,200 ft AGL | 1,200–1,400 ft AGL (+200 ft margin) |
| Pull-off altitude floor | 300 ft AGL (10°) | 400 ft AGL (10°) |
| Tracer visibility | Moderate; daylight conditions | High; NVG amplifies tracer luminance — can cause washout |
| WP marking | Visible white smoke | Visible burning phosphorus (bright); effective night marker |
| Illumination rockets | Not typically used | M257 essential for target area illumination |

---

## Part 1 — Night Systems & NVG Operations Review

### Pre-Departure Quiz (3 Questions)

1. **"How do you activate NVG in the DCS UH-1H?"**
   - Answer: Backtick key (`` ` ``). NVG must be equipped in the mission editor for the crew to have them.

2. **"What altitude adjustment do you apply to the diving attack pull-off floor at night?"**
   - Answer: +100 ft. 10° dive: 400 ft AGL at night vs. 300 ft day. 20° dive: 600 ft AGL at night vs. 500 ft day.

3. **"Why are tracers especially significant under NVG?"**
   - Answer: NVG amplifies luminance — tracer rounds appear very bright and can temporarily wash out the image. The gunner or pilot must be prepared for this and not mistake the NVG washout for a malfunction.

### Cockpit Configuration for Night Operations

Before departure, set:

1. Instrument panel lighting — set to low (do not use full bright; NVG washout risk).
2. Exterior lights — set to appropriate mode for the mission (blacked-out for combat; standard for ferry).
3. NVG — activated via backtick key; confirm image is active before departure.
4. Announce to crew: *"NVG active — maintain cockpit light discipline."*

> **DCS NVG Note:** The DCS UH-1H models NVG as a simple image overlay activated by the `` ` `` key. There is no NVG adjustment mechanism (gain, focus) in the DCS model. The NVG image is represented as a green-tinted wide-angle view. Effective use requires the student to commit to the NVG for target acquisition; toggling rapidly between NVG and unaided view is distracting and should be avoided.

---

## Part 2 — Night Departure & Range Transit

### Night Departure Procedure

1. Complete standard startup; NVG confirmed active before lifting.
2. Hover check: identical to day procedure — state torque; GO/NO-GO verbal.
3. Departure call: *"Departing — NVG active — range transit."*
4. Climb to 1,200 ft AGL on instruments (AI, altimeter, VSI); do not rely on visual horizon at low altitude at night.
5. Transition to NVG scan for traffic once at altitude.
6. Transit at 80–90 KIAS; maintain heading on directional gyro.

### Range Arrival

1. Arrive at range boundary at 1,200 ft AGL.
2. Positively identify the range before descending.
3. Identify the target point using NVG before arming.
4. Call IP: *"Target identified — at [bearing], approximately [distance]. Request clearance to arm."*
5. IP clears: arm per standard arming checklist.

---

## Part 3 — M257 Illumination Rocket Employment

### M257 Overview

The M257 illumination rocket ejects a parachute-suspended flare at the burst point. It provides sustained battlefield illumination over a relatively large area.

**Employment:**
- Fired to arrive over the target area.
- Burst altitude: 600–800 ft AGL over the target area for optimal illumination arc.
- Flare burns for approximately 120 seconds; plan a follow-on rocket before the first expires to maintain continuous illumination.

### DCS Loadout Note

M257 illumination rockets are available in the mission editor under the XM-158 or XM-159 pod with the ILLUM (illumination) warhead type selected. The flare effect is modeled in DCS with a visible burning flare suspended under a parachute.

### Firing Procedure

1. Set fire mode: SINGLE.
2. Set weapon selector: ROCKETS.
3. Set depression: 32 mils (10° dive, 80 KIAS, 1,000 m) — standard.
4. Arm: full checklist, verbal.
5. Attack: 10° dive; fire at 1,000 m slant range.
6. Pull off; observe burst point.
7. If burst point is over the target area at 600–800 ft: *"Illumination good — mark the area."*
8. If burst is too high or too low: correct for next rocket.

### Illumination Call

After the flare ignites:

> *"[Ground element callsign], Warlord 6 — illumination is up over the target area. Mark is [direction and distance from flare to target]. Flare burn time approximately 2 minutes. I will relay as needed. Over."*

### Student Execution

- 1 illumination rocket pass.
- Student makes illumination call using standard format.
- IP assesses: was burst altitude approximately 600–800 ft AGL over the target? Was the call complete?

---

## Part 4 — WP at Night

### Night WP Employment

White phosphorus is more tactically significant at night because the burning phosphorus is visible for a very long distance and creates a distinctive, easily-identified mark.

**Advantages at night:**
- Visible to all NVG-equipped aircraft and ground forces within 10+ km.
- Burns for 60–90 seconds; does not require sustained observation.
- Oriented fire is easier because the burning phosphorus indicates direction of spread.

**Hazards at night:**
- Target PID is more difficult; confirming target identity before firing is more critical.
- Danger close distance is unchanged (300 m) but is harder to manage in darkness.
- Burning debris scatter is difficult to observe with NVG.

### Night WP Mark Call

Same format as day; add NVG reference:

> *"Warlord 6 — mark is [bearing/distance] from [reference point]. Burning white phosphorus visible, NVG. Target is [description], [direction and distance from smoke]."*

### Student Execution

1. IP designates a target; student fires 1 WP rocket (10° dive; 32 mils; 80 KIAS; 1,000 m).
2. Student observes burning WP under NVG.
3. Student makes mark call with NVG reference.
4. IP assesses: did the student confirm target PID before firing? Was the mark call complete?

---

## Part 5 — Night Rocket Attack (NVG)

### Night Attack Parameters

Night attacks use the same depression table as day. The changes are:
- Increased orbit altitude (+200 ft): 1,200–1,400 ft AGL.
- Increased pull-off floor (+100 ft): 400 ft AGL (10° dive).
- Reduced maximum attack airspeed: 90 KIAS (not 100+) — night spatial disorientation risk at high speed.

### Night PID Before Firing

At night, positive target identification (PID) must be confirmed before the roll-in — not during the dive. The target must be:
1. **Clearly visible on NVG** before arming.
2. **Confirmed as a valid target** (not friendly; not civilian infrastructure unless cleared).
3. **Re-acquired visually** after roll-in begins.

If the target is lost during the dive: **abort — pull off — do not fire**.

### Night Attack Procedure (10° Dive)

1. Orbit at 1,200–1,400 ft AGL; 70 KIAS; establish target PID on NVG.
2. Set depression: 32 mils (standard training value).
3. Arm: full checklist verbal.
4. Roll-in: establish 10° dive; accelerate to 90 KIAS.
5. Confirm target on NVG before the fire point.
6. Fire at 1,000 m slant range; single rocket.
7. Pull off: above 400 ft AGL; break; climb.
8. Observe impact on NVG.
9. Safe sequence.
10. Verbalize impact and correction.

### Night Impact Observation

NVG detonation observation:
- HE (M151/M229): bright flash visible on NVG; impact point clearly observable.
- The flash will cause momentary NVG washout — this is normal and brief (< 1 second).
- After washout clears: assess impact location.

### Student Passes (Night Rockets)

- 3 diving passes; 10°; 90 KIAS; 1,000 m; 32 mils.
- Night pull-off floor: 400 ft AGL.
- Impact verbalized after each pass.
- At least 1 pass within 75 m of aim point (night tolerance is wider than day by 25 m).

---

## Part 6 — Night Minigun Pass

### Night Minigun Technique

The minigun tracer walk is the same technique as day, but NVG tracer brightness requires adjustment:

1. **Expect NVG washout at burst start.** The initial burst will briefly wash out the NVG image. Do not panic and do not stop firing — the washout is momentary.
2. **After washout clears**: resume tracer walk; walk rounds onto target.
3. **Short bursts are especially important at night**: 2–3 seconds maximum per burst. Long bursts increase NVG washout duration.

### Night Minigun Procedure

1. Orbit at 1,200 ft AGL; 70 KIAS; right-hand orbit.
2. NVG target PID confirmed before arming.
3. Depression: 32 mils (10° dive, 80 KIAS, 1,000 m).
4. Arm: full checklist verbal.
5. Roll-in: 10° dive; 80–90 KIAS.
6. Begin burst: 2–3 seconds; walk tracers onto target under NVG.
7. Pull off: above 400 ft AGL.
8. Safe sequence.

### Student Passes

- 2 passes; standard 10° dive; apply night pull-off floor (400 ft AGL).
- After each pass: student verbalizes tracer impact and any NVG washout experienced.

---

## Part 7 — Night Door Gun (Crew Coordination)

### Night Door Gun Considerations

Night door gun operations require additional crew coordination because:
- The gunner's NVG is aimed through the door gun sight, not the pilot's perspective.
- The target may be visible to the gunner but not to the pilot (or vice versa).
- Cease-fire commands must be transmitted without visual confirmation of the gunner's actions.

### Night Crew Calls — Additional Requirements

| Situation | Call |
|---|---|
| Gunner has target on NVG | *"NVG tally — [description and bearing] — engaging."* |
| Gunner reports NVG washout | *"NVG wash — recovering — stand by."* |
| Pilot confirms target on NVG | *"Pilot NVG tally — [bearing]."* |
| Pilot cannot see the gunner's target | *"No joy from pilot seat — confirm target description."* |

### Night Door Gun Procedure

1. Pilot establishes right-hand orbit at 400 ft AGL; 70 KIAS.
2. Gunner: *"Port gun — NVG active — manned and ready."*
3. Gunner acquires target on NVG; calls: *"NVG tally — target at 9 o'clock."*
4. Pilot: *"Roger tally — cleared to engage."*
5. Gunner fires 2-second burst; applies tracer walk under NVG.
6. After burst: *"Rounds on target — port gun — weapons safe."*
7. Safe sequence.

### Student Execution

- 1 orbit engagement from port gun station; NVG active.
- Student uses night-specific call format.
- IP assesses: were all night-specific calls made? Was the burst short (≤3 seconds)?

---

## Completion Standards

| Standard | Criterion |
|---|---|
| Night quiz | All 3 questions correct before departure |
| NVG activation | Confirmed active before departure; cockpit lights adjusted |
| Night departure | Instruments used for climb; NVG for scan at altitude |
| M257 illumination | Burst approximately 600–800 ft AGL over target area; mark call complete |
| WP night mark | Target PID confirmed before firing; mark call with NVG reference |
| Night rocket — altitude floor | Pull-off at or above 400 ft AGL on all passes — **zero tolerance** |
| Night rocket — accuracy | At least 1 of 3 passes within 75 m of aim point |
| Night minigun — burst length | No burst exceeds 3 seconds |
| Night minigun — NVG washout | Student verbalizes washout and recovery; does not stop the burst |
| Night door gun — calls | All night-specific calls made; *"NVG tally"* format used |
| All night passes — safe sequence | Master Arm SAFE first; complete after every engagement |

---

## Common Errors

| Error | Correction |
|---|---|
| NVG not activated before departure | Enforce: NVG check is part of pre-departure litany; *"NVG — active"* before lifting |
| Using day pull-off floor (300 ft) at night | Brief: night floor is 400 ft (10° dive); +100 ft margin is mandatory |
| Not confirming target PID on NVG before roll-in | Brief: at night, PID must be confirmed in the orbit, not during the dive; if target is not identified before roll-in, do not roll in |
| Stopping burst due to NVG washout | Brief: washout is momentary; continue burst; recover tracking after washout clears |
| Long bursts (>3 seconds) under NVG | Night burst discipline: 2–3 s max; NVG washout compounds with burst length |
| Night door gun calls: using day format | *"NVG tally"* is required at night; using *"tally"* alone is an II |
| Cockpit lights not reduced before NVG | Cockpit light wash degrades NVG quality; reduce to minimum before activating NVG |

---

*Based on FM 3-04.113 (Night Operations), TM 55-1520-210-10, and Eagle Dynamics / Belsimtek DCS UH-1H module documentation. For simulation use only.*
