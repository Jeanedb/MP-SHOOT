# V14.6B.182 — Failed Evacuation

Open `MP_SHOOT_V14_6B_182_FAILED_EVACUATION.html` → Mission Select → Floor 4 · Crime Reader Playtest.

Floor 4 now shows evidence of people working, sheltering and abandoning positions. Selected workstations have coffee mugs, notes, framed photographs or reference books. The break room has an unfinished snack; reception has a spill and abandoned paperwork. Ground documents form localized trails around failed positions rather than blocking movement. The museum and secret shrine remain comparatively orderly.

Four failed holding positions use a split overturned desk in Investigation Review, another in Case Preparation, a fallen filing cabinet along the service corridor and a tipped utility cart/crates on the production floor. Two complete ordinary workstation assemblies are replaced. Damaged wall areas, impact marks, fallen chairs, a broken QA light and copier debris give the departments different histories. Barricades provide physical cover while leaving the door approaches and main route usable.

## Fire hazards and extinguishers

Three localized fires burn in QA, Court Brief Preparation and the factory. Animated flame sprites, light smoke, charred document fuel, scorch marks, positional crackling and local orange illumination identify the hazardous patches. The light fades back to the original room lighting when a fire is suppressed.

Standing in fire damages the player at timed intervals using the existing damage/armour/difficulty rules. Enemies also take periodic damage in fire. Menu/map pauses freeze the hazard clock. These are authored local hazards, not a spreading fire simulation, and every required destination has a route around them.

Each fire has a nearby usable extinguisher. Approach it and press E to suppress that local fire. Damage stops immediately; flames and warmth fade, with a short discharge effect/sound. The extinguisher becomes empty for the rest of that run. Replay resets the fires and extinguishers. No new inventory weapon or mandatory objective is added.

## Validation

Chromium checks cover clear operating points for all extinguishers, timed player damage, safety outside the burn patch, enemy damage, suppression, empty-station behaviour, lighting restoration, pause/map behaviour and replay reset. A long simulated hazard run keeps geometry and particles bounded.

The full correction/card/factory/boss/elevator route passes, including a connectivity run that treats all burning patches plus a safety margin as impassable. Doorway checks pass at 1,290 player positions across all 86 non-lift doorway aprons. Optional exhibit/shredder/secret and furniture checks pass. Screenshots reviewed the barricades, fire corners, extinguishers and occupied work areas without script or shader errors. Floors 1–3 geometry, collision, doors, items, pickups and NDI cards match V181 in deterministic browser comparison.

The level footprint and correction requirements are retained. V181 remains available separately. The new fire damage/cover placements are ready for user difficulty playtesting.
