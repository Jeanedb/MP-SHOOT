# V14.6B.188 — Officer Artwork

Replaced the Officer / Commander's `COMMANDER_SHEET_DATA` with the transparent PNG supplied in `Demon_supervisor_sprite_sheet_b6ad9e9b (1).zip`.

The original 1024 × 1024 RGBA image contains eight directions and eight animation rows, with native 128 × 128 cells. It is embedded without resizing or recompression. Original PNG SHA-256: `9306b62227649739b51986b1225852b803d4f154fc420545a76b161b51caab68`.

The prepared firing poses now retain the supplied energy-hand artwork. The old front-view pistol-flash cleanup region no longer applies to this character and is disabled for the Officer. The existing frame anchors, animation selection, display size, 5 health, support abilities, projectile behavior and encounter placement are retained. All seven other enemy sheets, including V187's new Shield, are byte-identical to V187. Source comparison confirms that executable logic differs only in that Officer prepared-pose mask argument; the remaining differences are the image and version/title strings.

Chromium checks confirm PNG decoding, exact source-alpha preservation across all 64 GPU animation textures, and intact alpha in all eight prepared poses. Every direction selects and renders idle, walk A/B, fire, pain and three death phases. In-game screenshots review front, directional and attack poses. No JavaScript or WebGL errors were observed.

Open `MP_SHOOT_V14_6B_188_OFFICER_ARTWORK.html` to play. The artwork applies wherever the Officer / Commander appears. V187 is retained separately.
