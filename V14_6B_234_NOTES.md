# V14.6B.234 — Watchfloor Atmosphere

Removed both V233 gallery stations and the pre-existing desk on the raised walkway. Repositioned and resized the old map board onto a blank wall span clear of the gallery doorway; the gallery remains an observation/circulation space.

Added five framed wall displays on the gallery/ramp and side walls, covering field, cave link, tasking, incident queue and Logistics status. Existing ground-level desks and displays remain.

Selected exactly two existing War Room fixtures for brief, independently timed faults. Most of each 12.7/17.3-second cycle stays steady; each has a short interrupted dimming event. The two fixture faces remain outside static batching, and a localized shader light adjustment dims the immediate pool without changing the room as a whole. Floor 5 resets the effect on other floors. No lightmap rebuilds, texture uploads, GPU state queries or geometry allocations occur per flicker frame.

Validation: browser checks cover removal of gallery furniture, five added wall screens, two selected fixtures, dim/recovery states, dynamic fixture exclusion from static batches, lower map table and key circulation/terminal locations. Reviewed clear gallery doorway and wall-screen captures. Checkpoint/tunnel checks and all five floors render without browser/WebGL errors.
