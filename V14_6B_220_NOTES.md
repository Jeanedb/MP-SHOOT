# V14.6B.220 — Performance Cleanup

Profiled V219 across all five floors, prioritizing the reported stutter on Floors 1 and 2.

## Findings and fixes

1. **Failed navigation retries:** outside Floor 3, an empty path forced another complete search on the very next update, bypassing the existing retry timer. Trapped enemies or obstructed goals could therefore repeat a costly search every tick. Empty routes now respect that timer; enemies still update, try direct movement and retry when their goal changes or they become stuck.
2. **Legacy pathfinding:** Floors 1, 2, 4 and 5 still used the older string/map/frontier-scanning search. They now reuse the existing Floor 3 rasterized collision grid and heap search. Furniture, moving doors, actor avoidance, diagonal clearance, terrain steps and the search limit remain enforced. Masks are rebuilt when the collision index changes.
3. **Drawing overhead on Floors 1/2:** sampled scenes contained about 7,400 and 6,300 original objects. Added spatial/material batches for opaque geometry, retaining all originals for gameplay. Each batch validates its sources before drawing: movement, texture, material, tint, visibility or geometry changes immediately return that group to individual drawing. Removed objects are detected, and batch buffers are released on rebuild/scene change.
4. **Floor 4 fire effects:** per-frame depth-write-state queries forced synchronization with the graphics driver. The renderer now tracks the state it sets, so the effects can restore it without that readback. Blend tracking preserves the effect's incoming state as well.
5. **Floors 3/5:** sampled areas already used room-based render batching and did not show the same excessive individual object draws. They retain that rendering path. The shared retry fix applies to all floors; Floor 5 also receives the indexed navigation search.

## Measurements

Measurements use headless Chromium with software WebGL in this workspace. They describe test CPU work/draw submission, not the player's hardware FPS. Area sampling includes initialization/JIT/GC variability; the stress tests are synthetic 12-enemy encounters at fixed positions.

| Sample | V219 | V220 |
| --- | ---: | ---: |
| Floor 1 Patrol, mean update | 5.99 ms | 1.26 ms |
| Floor 1 Mechanical, mean update | 25.31 ms | 2.15 ms |
| Floor 1 Mechanical, 95th-percentile update | 56.4 ms | 6.9 ms |
| Floor 2 Gallery stress, mean update | 11.69 ms | 2.23 ms |
| Floor 2 Administration stress, mean update | 5.74 ms | 1.49 ms |
| Floor 2 Pool stress, mean update | 119.99 ms | 0.94 ms |
| Floor 1 Operations, object draw submissions/frame | 2,146 | 805 |
| Floor 1 Mechanical, object draw submissions/frame | 3,778 | 1,339 |
| Floor 2 Dispatch, object draw submissions/frame | 990 | 646 |
| Floor 2 Pool Plant, object draw submissions/frame | 3,063 | 1,685 |

The pool stress result reflects the pathological blocked-route case; it is not a claim that ordinary pool gameplay ran at that update cost. Graphics-driver waits were removed, but total GPU time still depends on hardware, resolution and effects.

## Validation

- Before/after captures at eight Floor 1/2 locations: six matched pixel-for-pixel; the other two differed on fewer than 0.002% of pixels above an eight-channel-level threshold.
- Original object geometry, doors and collision snapshots matched on Floors 1/2.
- Changed furniture immediately fell back to individual rendering.
- Navigation responded to closing/opening/reclosing a door; a failed route retried twice over a simulated second rather than every tick.
- All five floors updated/rendered without browser or WebGL errors; tracked graphics state matched actual state after effects, and new batches cleared when leaving Floors 1/2.
- Weapon mechanics, LIDAR hold/penetration and weapon placement were retained. No enemy removal, damage changes or progression changes were used as performance fixes.

Further player testing is needed on the actual browser/GPU, especially during prolonged combat, boss encounters and repeated campaign transitions. This is a measured performance pass, not an exhaustive guarantee that every location is free of frame drops.
