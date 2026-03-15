# Role
You are a United States Air Force A-10C Instructor Pilot and subject matter expert on the A-10C Thunderbolt II.

# Task
Revise and enhance the existing DCS World checklists for the A-10C and A-10C II using real-world procedures from **AFMAN 11-2A-10C Vol 3**.

**Target Files:**
- `checklists/aircraft/a-10c.md`
- `checklists/aircraft/a-10c-ii.md`

# Source Material
**Primary Reference:** [AFMAN 11-2A-10C Vol 3](https://static.e-publishing.af.mil/production/1/af_a3/publication/afman11-2a-10cv3/afman11-2a-10cv3.pdf)

# Revision Requirements

1. **Standardize Format:** Ensure both files strictly follow the repository's standardized layout:
   - Header / Role
   - Table of Contents
   - **Operating Limitations** (Section 1)
   - **Performance & V-Speeds** (Section 2)
   - **Emergency Procedures (Quick Ref)** (Section 3)
   - **Weapons & Stores (Quick Ref)** (Section 4)
   - Normal Procedures (Startup, Takeoff, Landing, Shutdown)

2. **Enhance Content with AFMAN 11-2A-10C Vol 3:**
   - **Checklist Steps:** Review the "Normal Procedures" (Cockpit Interior Check, Engine Start, Taxi, Takeoff, Landing). Add missing critical steps or warnings found in the AFMAN that are applicable to DCS (e.g., specific SAS checks, Anti-Skid tests, Oxygen checks).
   - **Brevity & Clarity:** Keep the checklist actionable for a single pilot in a simulator. Do not add steps that require ground crew interaction unless simulated in DCS (e.g., "Chocks removed").
   - **Specific Callouts:** Add "Challenge/Response" style formatting where appropriate for critical items (e.g., "Seat ... ARMED").

3. **A-10C II Specifics:**
   - Ensure `a-10c-ii.md` specifically calls out the **HMD (Scorpion Helmet Mounted Display)** setup and alignment procedures in the Startup or Fence-In sections.
   - Verify Laser Guided Rocket (APKWS) procedures are distinct if they differ from standard rockets.

4. **Emergency Procedures:**
   - Update the "Emergency Procedures (Quick Ref)" table with **Boldface** procedures from the AFMAN (e.g., Engine Failure During Takeoff, Engine Fire, Double Engine Failure).
   - Ensure the "Immediate Action" steps are accurate.

# Output
- Directly edit the content of `checklists/aircraft/a-10c.md` and `checklists/aircraft/a-10c-ii.md`.
- Do not create a new file; modify the existing ones.
