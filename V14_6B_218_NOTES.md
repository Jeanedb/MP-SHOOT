# V14.6B.218 — Clear Weapon Sightlines

- Lowered the LIDAR, C6, Carl Gustaf and taser rifle so their entire weapon canvases begin at least 48 CSS pixels below the centre crosshair. This covers idle, firing, recoil, ejection and reload frames.
- These four weapons now scale proportionally on shorter/narrower game windows, including the effective smaller viewport produced by browser zoom. Their wrists can crop naturally at the bottom, while the barrel and LIDAR display remain visible.
- Retains the existing sprite art and animation, live LIDAR screen, penetration/hole effect, sounds and weapon balance. Other weapon placements, including the C8's dedicated aimed sight picture, are unchanged.

Validation: browser checks exercised all six frames for each affected weapon at 1920×1080, 1920×914, 1440×900, 1536×731, 1366×668, 1280×720, 960×540 and 800×480. Verified crosshair clearance and preserved proportions, unchanged placements for the other weapons, unchanged profiles/sound routines/LIDAR penetration, and C8 aimed alignment. Reviewed in-game captures including the LIDAR execution effect above the lowered weapon. No browser or WebGL errors.
