# V14.6B.190 — Shooter Artwork

Replaced `SHOOTER_SHEET_DATA` with the transparent PNG supplied in `Upscaled_demon_sprites_for_shooter_f8d6b5f5.zip`.

The original 1024 × 1024 RGBA image is embedded without resizing or recompression. Its eight directions and eight animation rows have native 128 × 128 cells. Original PNG SHA-256: `97ae67f54f4cfc8b80779352400b549d7e3cb00e6e34169f0117882ad5c86c15`.

Refined the existing aiming-pose muzzle cleanup to remove warm flash pixels inside its existing regions rather than clearing whole rectangles. This preserves cannon details in the new sheet. The forward muzzle keeps the established dark recoloring treatment. The original firing row is untouched; only derived aiming textures receive cleanup.

Frame anchors, display size, 5 health, movement, attack timing, projectile behavior, gait and encounter placement are retained. Source comparison confirms no gameplay-logic changes; the only executable change is the aiming-texture cleanup condition. All seven other enemy sheets are byte-identical to V189, including the new Shield, Officer and Grenadier.

Chromium checks verify PNG decoding and exact source-alpha preservation across all 64 GPU animation textures. Every direction selects and renders idle, walk A/B, fire, pain, three death phases and aiming poses. All eight derived aiming textures retain non-flash opaque detail inside their cleanup regions and match the intended selective alpha changes. In-game front, directional, firing and aiming screenshots were reviewed without JavaScript or WebGL errors.

Open `MP_SHOOT_V14_6B_190_SHOOTER_ARTWORK.html` to play. The replacement applies wherever the Shooter appears. V189 remains available separately.
