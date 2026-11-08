# V14.6B.187 — Shield Artwork

Replaced `SHIELD_SHEET_DATA` with the transparent PNG supplied in `Demon_shield_sprite_sheet_actions_1d6297a1.zip`.

The original image is 1024 × 1024 RGBA, arranged as eight directions by eight animation rows. Each cell is already 128 × 128 pixels, matching the game's texture size. The original PNG is embedded without resizing or recompression, preserving the supplied detail and transparency. Original PNG SHA-256: `090e7f60214134d497f97d92f8eea7b0169db05f9cd8534c49cb7db14ad05d98`.

The existing Shield installer, directional layout, frame anchors, display size, prepared firing poses, health, frontal protection, behavior and encounter placement are retained. The other seven embedded enemy sheets are byte-identical to V186. Source comparison confirms that all executable game logic is unchanged; only the Shield image, version/title strings and asset-description comment differ.

Chromium verification decodes the original image, reads back all 64 GPU animation textures and confirms exact source alpha preservation, checks all eight prepared poses, and selects/renders idle, walk A/B, fire, pain and three death phases for every direction. The Shield retains 14 health. In-game front, directional and firing screenshots were reviewed; no JavaScript or WebGL errors were observed.

Open `MP_SHOOT_V14_6B_187_SHIELD_ARTWORK.html` to play. The replacement applies wherever the Shield enemy appears, across all floors. V186 remains available separately.
