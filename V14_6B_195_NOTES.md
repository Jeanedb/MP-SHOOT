# V14.6B.195 — Tribunal Cover

Fixed the Crime Reader's thrown reports passing through marble pillars.

The reports reused a sightline test that ignores short distances at both endpoints. At normal simulation step sizes, those ignored distances exceeded the report's entire movement, allowing it to cross a pillar without a collision. Reports now sweep their complete three-dimensional path against solid cover, including their contact width. The nearest contact wins: cover stops the report before player damage, while an exposed player in front of cover can still be hit. Impacts release small paper fragments.

Vertical movement is integrated once, within the same collision sweep. Reports also sweep against the player, preventing large simulation steps from skipping a body hit. Navigation, the restored correction lanes, shootable paperwork and the boss phases remain unchanged.

Validation in Chromium:

- Reproduced 36 cover failures in V194 using the same test against the six actual pillar shafts.
- V195 passed all 60 pillar cases: six pillars, both horizontal axes, and simulation steps of 1/240, 1/120, 1/60, 0.1 and 0.6 seconds.
- Checked starting contact, exposed-player damage, player-before-cover ordering, overhead misses, low-cover clearance and vertical integration.
- Full Floor 4 progression, boss victory and elevator departure passed. No JavaScript or WebGL errors in these checks.

Quick access remains **Mission Select → Floor 4 · Final Review Tribunal Playtest**.
