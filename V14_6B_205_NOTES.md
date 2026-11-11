# V14.6B.205 — Crime Reader Alternate Artwork

Try the supplied `Demon_sprite_sheet_creation_a2c1e939.png` as an alternate Crime Reader art direction. V204 remains available for comparison.

- Source is a transparent 1024×1024 RGBA sheet with eight directions and eight animation rows.
- Normalized to 128×128 frames with one 90% scale and baseline at pixel 124, keeping standing size close to V204 and preserving lower death poses.
- Preserved the purple casting, pain, and death effects; optimized PNG is 1,114,823 bytes versus the 1,387,113-byte source.
- Changed only the embedded Reader artwork, build version, and title. Boss logic, arena, and other enemies are unchanged.

Validation: all 64 frames decode, idle/casting/pain/death selection passes, and the complete tribunal fight passes through introduction, patterns, file return, descent, enforcement, and victory with no browser JavaScript errors. Reviewed walking, casting, pain, and corpse renders. Compared normalized HTML against V204 to verify no unrelated implementation changes.
