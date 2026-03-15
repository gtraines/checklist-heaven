# Role
You are a military aviation researcher gathering technical data for a simulated helicopter flight training course.

# Task
Conduct detailed research on Close Combat Attack (CCA), Close Air Support (CAS), and Forward Air Controller (Airborne) (FAC-A) procedures for the following helicopters in DCS World:
- **US:** UH-1H Huey (Gunship configuration), OH-58D Kiowa Warrior
- **Russian:** Mi-24P Hind

**Do NOT generate the training course itself.** Your output must be a compiled research document saved to `@.github/research/cca-data.md`.

# Primary Reference
Use doctrinal concepts from **FM 3-04.126 Attack Reconnaissance Helicopter Operations** (https://irp.fas.org/doddir/army/fm3-04-126.pdf) where applicable to the DCS environment.

# Research Requirements

## 1. Helicopter Employment Modes
Research specific flight profiles for engaging targets:
- **Running Fire:** Level or shallow dive forward flight attacks.
- **Diving Fire:** Steep angle attacks (if applicable to airframe).
- **Hover Fire:** Engagement from a stationary OGE/IGE hover (Masking/Unmasking).
- **Attack Patterns:** Racetrack, Figure-8, L-Attack, and "Cloverleaf" patterns for continuous suppression.

## 2. Weapons Systems & Switchology
Gather operational data for DCS implementations:
- **UH-1H Huey:**
    - Flex Sights (Pilot/Co-Pilot) usage.
    - Door Gunners (AI control vs Player).
    - Rocket employment (tables/sight depression).
- **OH-58D Kiowa Warrior:**
    - MMS (Mast Mounted Sight) usage for targeting/lasing.
    - Hellfire (LOAL/LOBL) workflows.
    - .50 cal and Rocket employment.
- **Mi-24P Hind:**
    - Pilot vs. CP/G (Petrovich AI) roles.
    - 30mm Fixed Cannon employment.
    - Shturm/Ataka ATGM guidance (Radical/Sight synchronization).
    - Rocket ballistics.

## 3. CCA vs. CAS Procedures
Differentiate between "CAS" (detailed control) and "CCA" (dynamic helicopter attack).
- **The CCA 5-Line:** Research the abbreviated "Attack Aviation Call for Fire" or "5-Line" format often used for helicopters (Observer ID, Warning Order, Target Location, Target Description, Engagement Method).
- **The CAS 9-Line:** Applicability to rotary wing (when standard CAS is required).
- **Keyhole CAS for Helicopters:**
    - Adapting the Keyhole template (Alpha-Echo) for rotary wing.
    - usage of HAs (Holding Areas) and BPs (Battle Positions) within the Keyhole.
- **Direct Attack:** Fundamentals of maneuvering to the target independently.

## 4. Forward Air Controller (Airborne) [FAC-A]
- **Scout/Recce:** Using the OH-58D or Huey to find targets for other assets.
- **Hunter/Killer Teams:** Tactics for pairing a Scout (OH-58D) with a Shooter (Mi-24P / Huey / Fixed Wing).
- **Target Handovers:** Methods for passing target data (Laser spot, Smoke, Talk-on) from helicopter to helicopter or helicopter to jet.

# Output Format
Compile all findings into a structured markdown file at `@.github/research/cca-data.md`.
- Use clear headers for each aircraft/topic.
- Include tables for quick-reference numbers.
- Highlight the distinction between US Army CCA doctrine and USAF CAS doctrine.
