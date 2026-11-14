# V14.6B.217 — LIDAR Burnthrough

- Full-power LIDAR shots penetrate every aligned enemy within the existing 22-unit range, spending cell energy once. Partial-charge shots retain their previous single-target behaviour.
- The beam continues to the first wall, closed door, breakable prop or other intercepted world object. It passes through open doors. The terminal world hit uses the existing impact/destruction handlers.
- Normal enemies killed by a full-power shot hold their hit-time sprite for 0.38 seconds, with a real transparent circular opening at the hit location and a pale green scorched rim. They then play their existing death animation. Dead actors cannot continue attacking or moving during the pose.
- Deaths, score and drops still happen once through the existing damage handlers. Boss damage caps and protection remain in effect; bosses do not receive the normal-enemy execution pose.
- The pose timer pauses with gameplay and is owned by the enemy, so changing scenes leaves no effect behind. The hole uses a shader discard rather than a black decal or per-kill texture allocation; the mask resets immediately after that enemy is drawn.
- Retains V216's live LIDAR display, restored pistol/C6 sounds and other previously approved weapon feedback.

Validation: scripted browser checks covered a shield/heavy/shooter lineup, off-axis targets, one-time charge/kill accounting, partial charge, insufficient cell power, walls, closed/open doors, breakables, boss protection, pause/resume, pose completion and scene changes. Pixel readback verified that the hole reveals the actual background while the ordinary sprite is opaque at that point, and that the mask does not affect subsequent objects. All five floors rendered without browser or WebGL errors. Reviewed the execution pose in visual captures.
