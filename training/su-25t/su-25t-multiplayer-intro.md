# Introduction to DCS Multiplayer Operations (Su-25T)

> **Course:** Multiplayer Operations | **Aircraft:** Su-25T Frogfoot
>
> [← Back to Index](index.md)

---

## Table of Contents

1. [Course Overview](#course-overview)
2. [Preparation & Tools](#preparation--tools)
3. [Ground Operations (Rearm & Refuel)](#ground-operations-rearm--refuel)
4. [Startup in Multiplayer](#startup-in-multiplayer)
5. [Communications & ATC](#communications--atc)
6. [Multiplayer Etiquette](#multiplayer-etiquette)
7. [Common Errors](#common-errors)

---

## Course Overview

**Objective:**
This course bridges the gap between single-player proficiency and multiplayer effectiveness. It teaches pilots how to operate the Su-25T in a live server environment, focusing on communications (SRS), ground coordination, and efficient startup/rearm procedures.

**Target Audience:**
Pilots proficient in basic Su-25T flight (completed BQT) who are new to multiplayer servers like "Grayflag", "Hoggit", or "Enigma's Cold War".

**Learning Objectives:**
*   Configure and use SimpleRadioStandalone (SRS) with the Su-25T.
*   Perform ground rearm/refuel operations correctly.
*   Execute a multiplayer-appropriate startup and taxi.
*   Communicate intentions clearly using standard brevity.
*   Adhere to common multiplayer etiquette and rules of engagement.

---

## Preparation & Tools

### SimpleRadioStandalone (SRS)
SRS is the standard voice communication software for DCS multiplayer. It simulates realistic radio propagation, frequencies, and encryption. Unlike Discord, SRS requires you to be on the correct frequency to hear others.

### Connection
*   **Auto-Connect:** Most servers automatically populate the SRS connection details when you join the DCS server. Ensure "Auto Connect" is enabled in your SRS settings.
*   **Manual IP:** If auto-connect fails, copy the server IP from the DCS server browser or briefing and paste it into the SRS client.

### Controls Setup
You must map these in your DCS controls (under "SRS" category if installed, or via SRS client settings):
*   **PTT (Push-to-Talk) Radio 1:** Primary radio (usually UHF/VHF).
*   **PTT Radio 2:** Secondary radio.
*   **PTT Radio 3:** Tertiary radio (often used for GCI/AWACS).
*   **Toggle Radio Overlay:** Essential for the Su-25T to see frequencies.

### Su-25T Specifics: Tuning Radios
The Su-25T has a "Flaming Cliffs" (non-clickable) cockpit. You cannot rotate radio knobs with your mouse.
*   **The Problem:** You cannot see the frequency on a cockpit display easily.
*   **The Solution:** Use the **SRS Overlay** (`LCtrl + LShift + ESC` by default to toggle, or check your specific bind).
*   **Changing Frequencies:**
    *   **Overlay Method:** Use the SRS overlay controls to manually type/select frequencies.
    *   **Cockpit Method:** The Su-25T radios (R-800 / R-862) are often preset by the Mission Editor. You can cycle channels, but in dynamic multiplayer servers, manually tuning via the SRS Overlay is the standard practice.

---

## Ground Operations (Rearm & Refuel)

In multiplayer, you often spawn with a default loadout that may not match your mission.

### The Ground Crew Menu
1.  **Canopy MUST be Open:** The ground crew cannot "hear" your request if the canopy is closed and engines are off, unless you use the specific intercom keybind.
    *   *Tip:* Press `LCtrl + C` to open canopy.
2.  **Access Menu:** Press `\` (Communication Menu) -> `F8` (Ground Crew) -> `F1` (Rearm & Refuel).

### Loadout Strategy
*   **Balance is Key:** Do not take 100% fuel for a 20nm flight. The Su-25T is heavy; extra weight increases takeoff distance and reduces maneuverability.
*   **Vikhr Loadout:** The standard anti-tank loadout (2x Vikhr racks) is heavy and draggy. Ensure you have enough runway.
*   **ECM Pods:** Essential for multiplayer survival (SPJ pods on wingtips).

### Refueling
*   Use the **Fuel Slider** in the Rearm menu to set precise amounts.
*   Standard load: ~60-70% internal fuel is usually sufficient for most tactical servers.

---

## Startup in Multiplayer

### "Speed" vs. "Procedure"
While checklists are critical for realism, multiplayer environments (especially PVP or dynamic PVE) often require a balance. You do not need to wait 10 minutes for systems that don't exist in the Su-25T.

### The "Alignment" Myth
*   **Fact:** The Su-25T navigation system does **not** require a lengthy INS alignment like the A-10C or F-16C.
*   **Advantage:** You are a Quick Reaction Alert (QRA) asset. Once engines are stabilized (`RAlt + Home` / `RShift + Home`) and electrics are on (`RShift + L`), you are essentially ready to taxi.

### Situational Awareness
**Before you move:**
1.  **Check F10 Map:** Look for traffic at your airfield. Is someone landing? Is someone taxiing?
2.  **Check SRS:** Listen on the airfield frequency.
3.  **Visual Scan:** Look left and right. Do not taxi through other players.

---

## Communications & ATC

Effective communication prevents collisions and fratricide.

### Finding Frequencies
1.  **F10 Map:** Click the airfield icon. The info box will list frequencies (e.g., "Kobuleti: 133.000 MHz").
2.  **Kneeboard:** `RShift + K`. Browse to the airfield data pages.
3.  **Briefing:** `LAlt + B`. Often lists theater frequencies.

### Tuning
*   Open SRS Overlay.
*   Type/Select the frequency (e.g., `133.00`) into Radio 1.
*   Ensure the radio is selected (highlighted in overlay).

### Basic Calls
Multiplayer comms should be "Short, Sweet, and Standard." Format: **Who you are calling**, **Who you are**, **Where you are**, **What you are doing**.

*   **Taxi Request/Announce:**
    > "Kobuleti Traffic, Enfield 1-1, taxiing runway 07."

*   **Takeoff Announce:**
    > "Kobuleti Traffic, Enfield 1-1, taking active 07, departure to the north."

*   **Inbound/Landing:**
    > "Kobuleti Traffic, Enfield 1-1, 10 miles north, inbound for landing runway 07."

### Brevity
*   **No Storytelling:** Don't say "Uh, hey guys, this is Bob in the Frogfoot, I'm just gonna sort of roll out here and maybe go blow up some tanks."
*   **Use:** "Traffic, Enfield 1-1, taxiing active."

---

## Multiplayer Etiquette

1.  **Spawn Etiquette:** Never spawn on the runway if given a choice. If the server spawns you on the runway, clear it **immediately**.
2.  **Taxiway Right-of-Way:** Aircraft exiting the runway have the right-of-way over aircraft taxiing to the runway.
3.  **Runway Occupancy:**
    *   Do not stop on the runway to reconfigure flaps or check maps.
    *   Land, brake, and take the first available exit.
    *   "Cold" runway checks: Look down the approach path before crossing or entering.
4.  **Friendly Fire:** Visually ID targets (VID) before firing. The Su-25T Shkval camera is excellent for this. If in doubt, don't shoot.

---

## Common Errors

*   **Closed Canopy Rearm:** Trying to contact ground crew with the canopy closed and getting no response.
*   **Hot Mic:** Leaving the SRS radio switch "on" or using Voice Activation (VOX) in a noisy room. **Always use Push-to-Talk.**
*   **Runway Spawning:** Selecting a "Takeoff from Runway" slot when the server is busy, causing a collision with a landing aircraft.
*   **Silent Taxi:** Moving without checking the map or announcing intentions, leading to taxiway head-ons.
*   **Overloading:** Taking 100% fuel and full weapons, then failing to take off before the runway ends.

---
*Based on Eagle Dynamics DCS World documentation and common multiplayer community standards. For simulation use only.*
