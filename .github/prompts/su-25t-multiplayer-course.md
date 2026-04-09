Act as an expert DCS World instructor and multiplayer server admin. I need you to create a comprehensive **"Introduction to DCS Multiplayer Operations (Su-25T)"** course.

**Objective:**
Teach a pilot who is already proficient in basic Su-25T flight (has completed BQT) how to effectively operate in a multiplayer environment, specifically focusing on communications (SRS), ground coordination, and efficient startup/rearm procedures.

**Target Audience:**
Pilots new to multiplayer servers like "Grayflag", "Hoggit", or "Enigma's Cold War" who need to learn the etiquette and technical setup for online play.

**Format:**
Create a single markdown file named `su-25t-multiplayer-intro.md` in the `training/` directory. Use the same style as existing courses (Header, Learning Objectives, Procedure Steps, Common Errors).

**Course Content to Cover:**

1.  **Preparation & Tools**
    *   **SimpleRadioStandalone (SRS):** Brief explanation of what it is.
    *   **Connection:** How to connect to a server's SRS (auto-connect vs manual IP).
    *   **Controls:** Essential binds needed (PTT for Radio 1/2/3, Overlay Toggle).
    *   **Su-25T Specifics:** Since the Su-25T has a non-clickable cockpit, explain *how* to change frequencies (Overlay usage vs. Mission Editor presets vs. keybinds if applicable).

2.  **Ground Operations (Rearm & Refuel)**
    *   **Ground Crew Menu:** How to access it (`\` -> F8 -> F1).
    *   **Canopy Requirement:** Why the canopy must be open for the crew to "hear" you (or use the intercom keybind).
    *   **Loadout Selection:** Brief tips on selecting a balanced loadout for multiplayer (don't take 100% fuel for a 20nm flight).
    *   **Refueling:** Setting the fuel slider.

3.  **Startup in Multiplayer**
    *   **"Speed" vs. "Procedure":** Acknowledge that while checklists are key, multiplayer often demands a faster startup.
    *   **The "Alignment" Myth:** Remind them Su-25T doesn't need INS alignment (unlike A-10C/F-16), making it a quick-reaction jet.
    *   **Coordination:** Checking the F10 map for traffic before taxiing (don't just spawn and roll).

4.  **Communications & ATC**
    *   **Finding Frequencies:** How to find the airfield frequency (F10 map clicking, kneeboard).
    *   **Tuning:** Walkthrough of tuning the radio to the active airfield.
    *   **Basic Calls:**
        *   *Taxi Request/Announce:* "Kobuleti Traffic, Enfield 1-1, taxiing runway 07."
        *   *Takeoff Announce:* "Kobuleti Traffic, Enfield 1-1, taking active 07, departure to the north."
        *   *Inbound/Landing:* "Kobuleti Traffic, Enfield 1-1, 10 miles north, inbound for landing runway 07."
    *   **Brevity:** Keep it short. No "storytelling" on the radio.

5.  **Multiplayer Etiquette**
    *   **Spawn Etiquette:** Don't spawn on a runway.
    *   **Taxiway Right-of-Way:** Yield to aircraft exiting the runway.
    *   **Runway Occupancy:** Land, exit immediately. Don't stop to reconfigure on the active.

**Output:**
A complete, structured markdown file ready to be saved as `training/su-25t-multiplayer-intro.md`.
