# V244 — Crawler Wall Facing

Wall-mounted crawler rotation previously used a fixed sign from the wall normal. Its climbing pose could point away from the player when viewed from the opposite end of the passage. Select the sign from the viewer direction along the wall pose instead. Retain the last sign inside a small head-on dead zone to avoid repeated flipping. Reset the stored sign when attaching to a different wall normal.

Shared pose basis continues to drive drawing, claw contacts, hit bounds and LIDAR impact coordinates. Ground and ceiling poses and combat behaviour are unchanged.

Validation: both viewer directions on all four wall normals, head-on dead-zone stability, preserved ground/ceiling bases, opposite-direction visual captures at actual terrain heights, and all five floors rendering without browser errors. Local scripts and captures: /workspace/mp-shoot-v244.
