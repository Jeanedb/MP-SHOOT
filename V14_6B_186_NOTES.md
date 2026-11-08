# V14.6B.186 — Service Clearance

Moved the Mechanical / Electrical service log, tool shelf and three tools from the east exit onto the north wall beside the switchgear. V185's shelf was non-solid but visually crossed the doorway. Clearance validation now checks decorative geometry inside the opening as well as player collision.

Enemy artwork audit of V185:

| Enemy | Internal name | Embedded PNG constant | Loader | Runtime textures |
| --- | --- | --- | --- | --- |
| Heavy | `tank` | `TANK_SHEET_DATA` (line 760) | `installRealTankSprites()` | `enemyTex.tank` |
| Officer / Commander | `commander` | `COMMANDER_SHEET_DATA` (line 8429) | `installCommanderSprites()` | `enemyTex.commander` |

Both are embedded base64 PNG images, just like Charger, Shooter, Flanker, Shield, Grenadier and Shift IC. All eight actual sheets are 768 × 768 pixels, arranged as eight directions by eight animation rows. Each 96 × 96 cell is extracted into a 128 × 128 runtime texture. Some older source comments incorrectly describe sheets as 1024 × 1024; the decoded PNG headers establish the actual size.

The Heavy is in the original enemy artwork section. The Officer is inside the later V12.5 Commander / Support Enemy patch. That patch initially copies Shooter textures as a fallback, then installs its own embedded artwork. Its PNG source is also exposed through `fp120CommanderSheet` for prepared firing poses. Its spawning and behavior are separate wrappers. The storage format itself is the same; no enemy artwork or AI was changed by V186.

Browser checks verify that both sheets decode and install all directional animation rows, including the Officer's eight prepared poses. All mechanical-room openings pass checks against low decorative geometry. The existing 1,290-position doorway collision/furniture checks pass. A screenshot reproduces the reported view after moving the shelf; no JavaScript errors were observed. V185 is retained separately.
