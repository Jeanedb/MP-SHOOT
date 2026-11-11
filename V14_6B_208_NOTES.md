# V14.6B.208 — Police Operations Cleanup

- Mission Select actions now wrap into a responsive grid, with readable button labels and no horizontal overflow. Updated the heading to explicitly include the Floor 5 first section.
- Corrected Floor 5 door rendering: the logical vertical-door orientation flag was being interpreted as a one-radian visual rotation. Leaves now align with their portals throughout retraction.
- Replaced the War Room ramp's stepped railing with a continuous sloped rail and matching collision spans. Added a flush concrete enclosure beneath the ramp and gallery platform.
- Floor 5 now honors the existing all-weapons developer checkbox, matching the established preview behavior on earlier floors.

The cavern, encounter composition, objective progression, and earlier floor geometry are retained.

Validation: all 12 mission buttons remain within the panel at 1920, 1280 and 390 pixel viewport widths. Checked all Floor 5 doors at five opening positions, developer loadout ownership, gallery construction and in-game views. Walked the entire first-section objective loop using normal movement, including the gallery ramp and airlock. Navigation across the gallery, descent and bridge, physical enemy bridge traversal, elevated hitscan/projectile behavior and all 11 pickup access checks pass. No browser JavaScript or WebGL errors.
