# Event 5 — Door Gun Employment & Crew Coordination

> **Course:** UH-1H Huey Weapons Employment Course | **Event Type:** Simulator (Flight, Multi-Crew)
>
> [← Back to Course Overview](overview.md)

---

## Table of Contents

1. [Learning Objectives](#learning-objectives)
2. [Ground Brief](#ground-brief)
3. [Part 1 — M60D System Knowledge & Crew Stations](#part-1--m60d-system-knowledge--crew-stations)
4. [Part 2 — Crew Coordination Standards](#part-2--crew-coordination-standards)
5. [Part 3 — Pilot Technique for Door Gun Support](#part-3--pilot-technique-for-door-gun-support)
6. [Part 4 — Door Gun Live Fire (Gunner Station)](#part-4--door-gun-live-fire-gunner-station)
7. [Part 5 — Door Gun Integration with Pilot Weapons](#part-5--door-gun-integration-with-pilot-weapons)
8. [Part 6 — Sector Discipline & Ceasefire Procedures](#part-6--sector-discipline--ceasefire-procedures)
9. [Completion Standards](#completion-standards)
10. [Common Errors](#common-errors)

---

## Learning Objectives

Upon completion of this event the student will be able to:

- [ ] State the M60D system characteristics and the two door gun crew stations in DCS
- [ ] Operate the port and starboard door gun stations; acquire and engage a target
- [ ] Apply crew coordination call standards: "engaging," "cease fire," "target" calls
- [ ] Fly a pilot orbit pattern that places the target within the door gunner's effective sector
- [ ] Integrate door gun suppression with a pilot rocket pass using correct timing and communication
- [ ] Apply sector discipline: do not fire forward of the nose or aft of the tail reference datum
- [ ] Execute a cease-fire command and verify safe on both door gun stations

---

## Ground Brief

### Mission Profile

1. M60D knowledge review (3 questions — pre-departure)
2. Multi-crew startup: IP/student as pilot; second crew as door gunners (AI or second student if available)
3. Transit to range at 1,000 ft AGL
4. Part 3: Pilot technique demonstration — orbit placing target in gunner sector
5. Part 4: Student to door gun station; live fire 2 passes (port, then starboard)
6. Part 5: Combined pass — pilot rockets + door gun suppression; timing drill
7. Part 6: Sector discipline and cease-fire drill
8. Return and debrief

### Key Numbers Table

| Parameter | Value | Notes |
|---|---|---|
| **M60D caliber** | 7.62×51mm NATO | Same round as M134 minigun; different weapon |
| **M60D rate of fire** | ~550 rpm | Much slower than M134; single barrel |
| **Effective range** | 800–1,000 m | Same as M134 for planning |
| **Max range** | 1,100 m | Accuracy degrades rapidly beyond this |
| **Danger close** | 200 m | Same as M134 |
| **Ammunition per gun** | 300 rounds (DCS typical) | |
| **Door gun arc — forward limit** | Aircraft nose (0°) | Do not fire forward of nose |
| **Door gun arc — aft limit** | Aircraft tail datum | Do not fire aft of tail |
| **Effective firing sector** | 30°–150° from nose (per side) | Practical engagement window |
| **Pilot orbit for door gun support** | Right-hand orbit; 60–80 KIAS; 300–500 ft AGL | Places gunner on the inside of the turn, facing the target |
| **DCS port door gun station** | `F5` (crew station key) | Verify in Controls → Crew Stations |
| **DCS starboard door gun station** | `F6` (crew station key) | Verify in Controls → Crew Stations |

### Multi-Crew Note

This event is optimized for two students (one pilot, one gunner) or IP-plus-student. If flying single-crew (no second seat player), the student cycles between the pilot seat and door gun stations to understand both perspectives. The pilot-gunner integration drill (Part 5) requires active multi-crew — if single crew, IP will demonstrate the integration and the student will observe.

---

## Part 1 — M60D System Knowledge & Crew Stations

### Pre-Departure Quiz (3 Questions)

1. **"What is the effective range of the M60D?"**
   - Answer: 800–1,000 m. Beyond 1,100 m, accuracy is unreliable.

2. **"What is the door gun forward firing limit?"**
   - Answer: The aircraft nose — do not fire forward of the nose arc. Doing so creates a hazard to the main rotor and risks rounds impacting the aircraft's own forward flight path.

3. **"What is the crew call to stop firing immediately?"**
   - Answer: *"CEASE FIRE"* — this is a mandatory stop; the gunner releases the trigger and announces *"Weapons safe, port/starboard gun."*

### M60D System Notes

The M60D is a pintle-mounted, swing-arm variant of the M60 GPMG designed for helicopter use. Key characteristics:

- Belt-fed; operator loads and clears own weapon
- Swing arm allows approximately 120° of arc per side
- Operator fires using the rear spade grip triggers (both thumbs depress simultaneously)
- No depression adjustment knob — the gunner aims and fires by direct sight
- Tracers are 1:5 ratio (same as M134); use tracer walk to correct fire

### DCS Door Gun Stations

In DCS, the UH-1H has two crew-operable door gun stations:

| Station | Key | Notes |
|---|---|---|
| Port (left) door gun | `F5` | Switches view to left gunner position |
| Starboard (right) door gun | `F6` | Switches view to right gunner position |
| Return to pilot seat | `F1` | Returns to front-left pilot seat |

To engage targets from the door gun station:
1. Press `F5` or `F6` to move to the station.
2. Use mouse to aim the weapon (click-and-drag; mouse controls the gun arc).
3. Left-click (or configured fire button) to fire.
4. The gunner has no armament panel — the pilot handles Master Arm for door guns (they are always live when Master Arm is ARM and GUNS is selected, or as a separate system — verify in DCS options).

> **DCS Configuration Note:** In some DCS configurations, door guns fire independently of the Master Arm panel. Verify before the event whether door guns require pilot Master Arm ARM or fire independently. If fire independently, include a crew call to the pilot before the gunner opens fire regardless.

---

## Part 2 — Crew Coordination Standards

### Required Calls — Gunner

All calls are on the ICS (intercom); voice calls are modeled in DCS multiplayer ICS.

| Situation | Call |
|---|---|
| Gunner ready at station | *"Port/starboard gun — manned and ready."* |
| Gunner has acquired a target | *"Target! Port gun — [description and bearing]."* |
| Gunner opening fire | *"Engaging — port gun."* |
| Gunner ceasing fire (rounds expended) | *"Port gun — ammo low / dry. Weapon clear."* |
| Gunner ceasing fire (target destroyed) | *"Target destroyed — port gun — weapons safe."* |
| Gunner reports a malfunction | *"Port gun — stoppage — working it."* |

### Required Calls — Pilot

| Situation | Call |
|---|---|
| Pilot begins attack pass | *"Pilot attacking — door guns hold fire until my pass is complete."* |
| Pilot clear of the target | *"Pilot clear — door guns free."* |
| Pilot ordering cease fire | *"CEASE FIRE — CEASE FIRE — all stations."* |
| Pilot acknowledging gunner target call | *"Roger, target — [direction] — I'm maneuvering."* |

### Cease Fire Authority

The *"CEASE FIRE"* command may be given by the pilot at any time. It is not a request — it is a command. All gunners immediately release triggers and call *"Weapons safe."* Common reasons:

- Friendly forces enter the fire zone
- Aircraft maneuver will place rotor arc over the target
- Target identification unclear
- Abort directed by higher authority

---

## Part 3 — Pilot Technique for Door Gun Support

### The Orbit Pattern

Door guns are most effective when the target is positioned at the 3–9 o'clock position (90° from the nose) relative to the firing side of the aircraft. To achieve this consistently, the pilot flies a right-hand orbit centered on the target:

**Right-hand orbit — port (left) gun:**
- The port gunner faces left (outboard); in a right-hand orbit, the target at the center is always at the port side.
- Orbit altitude: 300–500 ft AGL.
- Orbit airspeed: 60–80 KIAS.
- Orbit radius: 300–600 m from target (within effective range).

**Left-hand orbit — starboard (right) gun:**
- The starboard gunner faces right (outboard); in a left-hand orbit, the target is always at the starboard side.

### Bank Angle Effect

In a 30° bank orbit, the effective gun depression increases (the aircraft tilts, pointing the gun more downward). Students should note that:
- Shallow bank (15–20°): gun is approximately level; effective at medium altitude.
- Steep bank (30–45°): gun points more steeply downward; better for close-in, low-altitude orbits.
- Too steep (>45°): difficult for the gunner to track; aircraft enters unusual attitude territory.

**Standard orbit bank angle: 20–30°.**

### Setting Up the Orbit

1. Approach target area at 1,000 ft AGL.
2. Identify target; call *"Target at [bearing], beginning orbit."*
3. Begin right-hand orbit (for port gun); establish 300–500 ft AGL, 60–70 KIAS, 20–30° bank.
4. Gunner calls: *"Target acquired."*
5. Pilot: *"You are cleared to engage."*
6. Maintain orbit; adjust radius to keep target in the 70°–120° arc off the nose (optimal sector).

---

## Part 4 — Door Gun Live Fire (Gunner Station)

### Gunner Familiarization (IP Demo First)

Before the student enters the gunner station:

1. IP takes pilot seat; establishes right-hand orbit at 400 ft AGL, 70 KIAS.
2. IP selects `F5` (port gun station) while describing what the student will see.
3. IP demonstrates target acquisition; fires a 3-second burst; demonstrates tracer walk.
4. IP returns to pilot seat (`F1`).
5. IP debrief: *"Notice the limited arc — forward limit is the nose; aft limit is the tail. The swing arm stops before you can fire into the rotor arc. Within that arc, aim and walk the tracers."*

### Student Gunner Passes

**Pass 1 — Port Gun**

1. Student moves to port gun station (`F5`).
2. IP establishes right-hand orbit at 400 ft AGL, 70 KIAS.
3. Student: *"Port gun — manned and ready."*
4. Student acquires target visually; calls *"Target — 9 o'clock."*
5. IP: *"Cleared to engage."*
6. Student fires 3-second burst; applies tracer walk; calls *"Engaging — port gun."*
7. After burst: *"Rounds expended — target [assessment]."*
8. IP: *"Cease fire — port gun."*
9. Student: *"Port gun — weapons safe."*

**Pass 2 — Starboard Gun**

1. Student moves to starboard gun station (`F6`).
2. IP establishes left-hand orbit at 400 ft AGL, 70 KIAS.
3. Repeat same call sequence for starboard gun.

### Gunner Scoring Criteria

- Target acquired within 10 seconds of entering the sector.
- Firing call made before first round.
- At least one 3-second burst; tracers walked onto target (or within 25 m).
- Cease-fire command responded to within 1 trigger-release.

---

## Part 5 — Door Gun Integration with Pilot Weapons

### The Combined Pass

The combined pass is the primary tactical employment of the armed UH-1H: the pilot uses rockets or minigun while the door gunners suppress flanking threats or the same target simultaneously.

**Sequence:**

1. **Pre-coordination:** before beginning, pilot and gunner brief the pass:
   - Pilot: *"I'll be making a diving rocket pass from the north. I'll call 'clear' when I'm off the target. Until then, door guns hold fire."*
   - Gunner: *"Understood — holding fire until 'clear' call."*

2. **Pilot attack:** pilot conducts normal diving pass; door guns are cold.
3. **Pilot pull-off:** *"Pilot clear — door guns free."*
4. **Gunner engagement:** gunner opens fire on the same target or designated secondary target.
5. **Sequence complete:** both stations call safe after engagement.

> **IP Note:** The timing of the "clear" call is critical. The pilot should not call clear while still in the pull-off climb over the target — wait until the aircraft has broken and is climbing away. Door gun rounds fired at the target while the pilot is still descending toward it could pass through the pilot's flight path if the gunner fires forward toward the nose arc.

### Timing Drill

IP will call the sequence at specific moments to stress the student's timing:

1. Pilot begins dive — IP calls *"Door gun engaging"* (simulating an undisciplined gunner) — student (as pilot) must call *"CEASE FIRE — CEASE FIRE"* and abort the pass.
2. Pilot completes pass and calls *"clear"* — door gunner engages correctly.
3. Debrief: what was the safety hazard in scenario 1?

---

## Part 6 — Sector Discipline & Ceasefire Procedures

### Sector Discipline Rules

**Forward limit:** The gunner must not fire forward of the aircraft nose. In DCS, the M60D swing arm has a physical stop preventing forward fire. The gunner must not attempt to push the weapon past this stop or angle the arm to fire at targets forward of the nose — this indicates the pilot needs to reposition the aircraft to bring the target into sector.

**Aft limit:** The gunner must not fire aft of the aircraft tail. Rounds fired aft of the tail datum have no tactical effect (the aircraft has already passed the target) and may endanger following aircraft.

**Rotor disk:**  The swing arm is designed to prevent the gun from pointing upward into the rotor disk. Never force the weapon upward.

### Common Sector Violation Scenarios

| Scenario | Correct Action |
|---|---|
| Target drifts forward of nose arc during orbit | Gunner calls *"Target forward — pilot reposition"*; pilot adjusts orbit radius or heading |
| Target moves aft of tail arc | Gunner calls *"Target aft — lost — pilot reposition"*; pilot repositions orbit |
| Target on opposite side from gunner station | Gunner calls *"No target — port side"*; pilot switches to left-hand orbit or switches active gunner |

### Cease Fire Drill

IP will conduct two unexpected cease-fire drills during the event:

1. During a live burst: IP calls *"CEASE FIRE"* — student (as gunner) must release trigger and call *"Weapons safe"* within 2 seconds.
2. Pilot calls *"Abort"* during approach — student (as pilot) must call *"CEASE FIRE — CEASE FIRE"* and break off immediately.

Both drills are graded: failure to respond within 2 seconds of a cease-fire call is an Incomplete Item.

---

## Completion Standards

| Standard | Criterion |
|---|---|
| Pre-departure quiz | All 3 questions correct |
| Gunner ready call | Made within 10 seconds of entering station |
| Target call | Made before opening fire, with bearing/description |
| Engaging call | Made before first round on every pass |
| Orbit pattern — altitude | 300–500 ft AGL maintained during orbit |
| Orbit pattern — target sector | Target maintained in 70°–120° arc during engagement |
| Tracer walk | Rounds within 25 m of target on at least 1 burst |
| Combined pass timing | Door guns held until *"pilot clear"* call |
| Cease fire response | Trigger released within 2 seconds of CEASE FIRE command — **zero tolerance** |
| Sector discipline | No forward-of-nose fire; no aft-of-tail fire |
| Post-engagement safe call | *"Weapons safe"* called after each engagement |

---

## Common Errors

| Error | Correction |
|---|---|
| Gunner opens fire without *"engaging"* call | Mandatory call before every burst; IP calls cease fire and requires re-brief |
| Pilot does not call *"clear"* before door guns engage | Pilot must verbalize clear; without clear call, door guns remain cold |
| Orbit too wide (target out of range) | Brief the effective range (1,000 m); if target not visible in tracers, reduce orbit radius |
| Orbit too tight (target under aircraft) | Brief minimum safe orbit radius based on altitude; at 400 ft AGL, 300 m is the minimum practical radius |
| Gunner fires past forward limit | Sector violation; IP calls cease fire; re-brief the arc discipline |
| Cease fire command not responded to within 2 seconds | Reinforce: CEASE FIRE is a command, not a request; immediate trigger release |
| Switching stations without notifying pilot | Brief: always call before leaving a station: *"Port gun — unmanning; weapon safe."* |

---

*Based on TM 43-0001-27 (Guided Missiles and Rockets), FM 3-04.140, and Eagle Dynamics / Belsimtek DCS UH-1H module documentation. For simulation use only.*
