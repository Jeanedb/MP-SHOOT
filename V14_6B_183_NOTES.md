# V14.6B.183 — Fire and Reception

Open `MP_SHOOT_V14_6B_183_FIRE_AND_RECEPTION.html` → Mission Select → Floor 4 · Crime Reader Playtest.

## Fire and old damage

The black mark near the Investigation Review barricade was static scorch dressing, not an active fire. At the reported player position, the QA fire loop was still eligible for playback about 17 m away through intervening walls. Fire crackling now requires a nearby source within 12 m and either the same room or a clear line of sight. Other ordinary machinery/light ambience remains.

Old damage in Review, Case Preparation, the service corridor and the factory margin uses chipped plaster/cracks instead of a dark fire-like blotch. Actual burning corners retain their heat stains. Active fires use a cached six-frame heat-diffusion sprite with irregular pixel edges instead of repeated geometric flame wedges. Smoke, hazard footprints, damage intervals, local warmth and suppression remain.

## Shootable extinguishers

Floor 4's three extinguishers now register with the existing Floor 2 shootable-prop system. A bullet or nearby blast triggers the same pressure-pop, hiss, powder cloud and damaged bottle appearance. The local fire is also suppressed. Shootable parts remain outside static rendering batches so the change is visible.

Manual E use remains available. Shooting and manual use share a single charge; an empty bottle cannot repeatedly burst. Replay restores each bottle and fire. The original pop has no added player-damage splash.

## File Intake

Replaced three disconnected counter segments with one joined L-shaped reception counter and a supported staff workstation. Reduced loose paper piles to a few receiving trays. Six waiting chairs form two aligned rows. The queue display sits near the counter; a right-wall authorization collection cabinet replaces the isolated pedestal/sign. Removed the fallen chair from this waiting bay and moved stray documents to its margin.

Airlock, Complaints, Automation and administrative-spine access remain clear, along with the existing gold-card pickup point. The map footprint and progression requirements are retained.

## Validation

Chromium tests hit extinguisher bodies using weapon rays, verify the shared Floor 2 pop/cloud, local suppression, repeated-hit protection, manual/shooting charge sharing, blast triggering, cloud expiry and replay reset. Audio-source checks reproduce the user's first-image position and confirm no distant fire loop there while nearby fires still emit sound.

The full correction/factory/boss/elevator route passes, including connectivity with burning patches excluded. Doorway-apron checks pass at 1,290 positions across all 86 non-lift doorways; direct Automation access and authorization standing space are also checked. Optional exhibit/shredder/secret and replay checks pass. Screenshots review reception, the reported wall mark, new flames and extinguisher powder burst without script or shader errors. Floors 1–3 geometry, collision, doors, pickups, items and NDI cards match V182 in deterministic comparison.

V182 is retained as a separate file.
