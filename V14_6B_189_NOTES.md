# V14.6B.189 — Grenadier Artwork

Replaced `GRENADIER_SHEET_DATA` with the transparent PNG supplied in `Demon_imp_sprite_sheet_animations_84aec40b.zip`.

The original image is 1024 × 1024 RGBA, arranged as eight directions by eight animation rows, with native 128 × 128 cells. It is embedded without resizing or recompression. Original PNG SHA-256: `ce61601a6542e1595954b16545e4c623ce35c35b220a09cacdaacdc707b0ef1e`.

The existing frame layout, anchors, display size, 9 health, 1.22 movement speed, throw timing, movement prediction, blast settings and encounters are retained. All executable game logic and all seven other enemy sheets are unchanged from V188. The recent Shield and Officer replacements are included.

Chromium checks confirm PNG decoding and exact source-alpha preservation across all 64 GPU animation textures. Every direction selects and renders idle, walk A/B, attack, pain and three death phases. Throw-windup artwork is also checked for all eight directions. In-game front, directional and attack screenshots were reviewed without JavaScript or WebGL errors.

Open `MP_SHOOT_V14_6B_189_GRENADIER_ARTWORK.html` to play. The replacement applies wherever the Grenadier appears. V188 remains available separately.
