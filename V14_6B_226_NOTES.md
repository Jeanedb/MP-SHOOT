# V14.6B.226 — Cave Crawlers

First integration of the supplied Emission-Free Demon Crawler sheet into Level 5.

## Artwork

- Extracted all 72 frames: eight directions and nine animation rows. The source has uneven frame spacing, so extraction uses the actual sprite components rather than equal-height grid cuts; a touching pair of frames is separated at its row boundary.
- Converted the opaque black surround into transparency, retained enclosed dark details, and packed fixed-scale frames with a common feet anchor into a 1024×1008 RGBA atlas (128×112 cells, approximately 954 KB).
- Original proportions and approved colours are retained, with padding around each frame. No new glow/emission layer is added.
- The optimized atlas is available at [assets/crawler_atlas.png](assets/crawler_atlas.png), and is embedded in the HTML for standalone play.

## Enemy and placement

- Five authored cave ambushers: two in the descending rock passage, one on a new rock outcrop beside the main cavern's east approach, and two in the temporary return cave. All are present when the level is built; they are not spawned in the player's view on crossing a threshold.
- Wall sprites align with rock faces; ceiling sprites lie against the ceiling. Crawling follows small authored surface lanes. This is a bounded surface/ambush implementation, not general navigation across arbitrary level meshes.
- A scrape/hiss and 0.78-second attack pose warn of a pounce toward a fixed landing point. Moving after the warning can dodge it. A pounce can deal one 11-point hit, followed by recovery; ground claw attacks have a separate 7-point hit and warning/cooldown.
- Crawlers have 7 HP, can be dislodged by hits, and fall under gravity. Surviving crawlers can scuttle on the floor and return to their original surface when disengaged. Their cave bounds keep them from chasing into offices or the chasm.
- Hit detection follows actual wall/ceiling position. CEW control dislodges/freezes them; rockets use their actual height; full-charge LIDAR can penetrate them and retains the hole pose before they fall.
- Deaths use the existing scoring/drop path and a crawler variant of the accepted grunt sound family. They do not add objective locks or mandatory clearance groups. The existing player reports and accepted fireball sound are retained.

## Validation

- Loaded all 72 frames; checked transparency, nonempty art and horizontal frame padding.
- Verified exactly five authored crawlers on Level 5 and none on Floors 1–4, including restarts/level changes.
- Tested aimed ceiling hits, absence of a false floor-level hitbox, solid cover, bullet dislodging, readable wind-up, dodging the locked pounce, exactly one 11-point hit when standing in it, CEW dislodging/freezing, and LIDAR hold followed by corpse fall.
- Reviewed actual wall, ceiling, cavern and LIDAR captures. All five floors updated/rendered without browser or WebGL errors. A 300-update sample averaged approximately 1.5–2.1 ms in this workspace; that is not a hardware FPS guarantee.
- Accepted player weapon reports, procedural fireball generation, player damage and sidearm implementation were unchanged.

This is the first playable crawler pass. Placement density, perceived size, pounce pressure and sprite readability still need a player playtest.
