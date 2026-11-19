# V241 — Bridge Sabotage and Cave Return

First functional route-and-event pass.

- Main bridge remains intact on the outbound trip. Recovering restricted authority arms a one-time sabotage event on returning to the east main approach or the east service catwalk.
- Brief camera glance shows an existing commander sprite as the WO stand-in, with his order displayed as text. He is a presentation actor, not an extra kill target. Combat simulation and player movement pause for 3.8 seconds to avoid unavoidable damage. No recorded dialogue is added.
- Explosion effects and procedural rumble accompany the falling twenty-unit middle span. Deck, rails and structural beams are split; falling sections disappear after the collapse. Terrain and navigation agree with the gap; existing enemy paths are invalidated.
- Removed the narrow west connector. Service bridge ends at a separately enclosed landing with a new authority-gated entrance directly into the temporary cave.
- Finished return tunnel is blocked by solid rock, faceted rubble, a broken beam and hanging sparking lead. Temporary cave is the remaining return to Operations.
- Map marks the destroyed bridge and tunnel blockage; objective text directs the return via service bridge and cave while the marker stays on the War Room terminal.
- Restart/replay resets the bridge and event. The game resumes campaigns at floor entry, not from mid-floor snapshots; no new mid-floor save system is introduced.

Checks: intact outbound bridge, no early detonation, both return trigger approaches, one-shot event, player health/armour preservation, removed span and navigation exclusion, solid cave-in from both directions, cave doorway clearance, navigation segments across service bridge and cave to Operations, subsequent override/elevator progression, replay reset, and browser rendering across Floors 1–5. Captures and scripts: /workspace/mp-shoot-v241.
