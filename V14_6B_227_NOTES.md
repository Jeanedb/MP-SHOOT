# V14.6B.227 — Crawler Bodies and Gore

- Replaced crawler art with the supplied revised sheet: 80 frames, eight directions and ten action rows. Removed the white JPEG background, defringed edges and aligned frames in a 1024×1120 transparent atlas. The standalone HTML embeds a lossless WebP; the editable PNG is in assets/crawler_atlas.png.
- Remapped pain, alternating attacks and four collapse/death rows, ending on the new bloody corpse artwork.
- Wall bodies stand clear of the rock and retain readable width at side angles. Ceiling bodies hang upside down with camera-facing pitch instead of lying flat against the roof. Small depth-bearing claw supports connect perched bodies to their surface.
- Updated body hitboxes and LIDAR hole coordinates to follow the new pose. Dead crawlers fall directly from their actual position, avoiding the old sideways death nudge.
- Preserved encounter counts, pounce timings, damage and accepted weapon/enemy audio.

Validation: browser checks cover all 80 frames, five authored placements, overhead aiming and cover, bullet/taser dislodging, pounce warning/dodge/contact, LIDAR hold and corpse landing, and rendering on all five floors without browser or WebGL errors. Inspected wall, ceiling and corpse captures. Update timing remains approximately 2 ms in the automated local run; this is not a hardware-wide FPS guarantee.
