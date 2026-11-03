# V14.6B.171 — Crime Reader floor playtest

Playable first draft based on Floor 4 Architectural Plan 01. Open `MP_SHOOT_V14_6B_171_CRIME_READER_FLOOR.html`, choose **Mission Select → Floor 4 · Crime Reader Playtest**. `E` interacts, `M` opens the map, `O` recalls the objective. Floor 3's completion screen also offers continuation with the current inventory.

## Route and rooms

The single shared elevator uses the approved Floor 2 cabin in Floor 3's east-facing orientation, including arrival, sliding doors, cabin control and departure timing. After defeating the Crime Reader, return to this same elevator. Floor 5 remains unbuilt.

Reception/file intake → Investigation Review (blue) → Quality Assurance/Corrections (T1 terminal) → Evidence Examination (red) → Case Conference (gold) → Senior Review corridor → Crime Reader office → original elevator. T1 also opens a review shortcut. Gold is reserved for the boss entrance.

All scheduled departments are present: elevator vestibule and interlocked security airlock; file intake/waiting; review office; corrections; evidence; compact records/archive; conference; staff kitchenette, two washrooms and janitor closet; mechanical/electrical; senior anteroom and boss office. Service corridors form secondary loops. Two concealed caches and ten NDI 20 cards are included. The service riser is enclosed rather than playable.

Each main department has initial furniture and signage. Corrections has a live error/return board with rising counts. Examination benches carry sealed evidence; conference has a case-status display. Glazing gives an early view into the senior suite while retaining physical barriers. Supplies and initial room encounters support a full run.

## Atmosphere and combat

Sparse fissures appear in late Evidence and Conference. Larger glowing cracks and rubble appear near the senior corridor and within the boss suite. Senior/boss lights flicker locally. Existing material impacts, machinery, footsteps, enemy sounds and weapon sounds carry through; no gameplay music was added.

The Crime Reader uses the existing boss sprite and attacks as placeholders. At approximately half health, one “Returned for Corrections” shield asks the player to use two arena terminals. Damage is retained. Clearing them resumes combat; defeating the boss unlocks the return elevator. The central arena circuit retains 2.4 m clearance.

## Scope and validation

This is a layout, pacing and atmosphere playtest. Final Crime Reader art, bespoke attacks, voice lines and an elaborate room transformation are still to be developed. Cracks are surface effects; no destructible architecture or moving walls are implemented. The footprint is the reviewed 73.4 × 53.6 m irregular envelope; enclosed area is approximately 2,806 m² including circulation and service riser.

The approved V170 file is retained. Browser checks cover physical access progression without card bypasses, room access, route/furniture clearance, both secrets, boss navigation/attacks/shield/terminals, return/departure, replay, map pause and rendering. The current 78-check regression suite passed. Deterministic comparisons confirmed Floors 1–3 geometry, collision, doors, pickups and NDI positions match V170. The new build adds approximately 61 KB of code/data and no embedded media.
