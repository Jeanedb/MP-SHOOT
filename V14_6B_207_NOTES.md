# V14.6B.207 — Police Operations / First Playable Section

First playable Level 5 build, following the approved staged plan. This is the arrival-to-cavern section, with a complete outbound/return objective loop; it does not represent the whole planned floor.

## Play

Use **Mission Select → Floor 5 · Police Operations / First Section**, or complete the Crime Reader fight and use the original departure elevator, then **Continue to Floor 5**. The transition carries the actual exit inventory. A direct playtest provides the sidearm, shotgun, C8 and baton when no campaign entry exists.

Secure the War Room, use its operations console, open geological access, cross the cavern, secure the far-side field station and establish the link. Return to the War Room through a reserve encounter and optional Dispatch shortcut, then report at the console. The completion panel offers exploration, replay and return to the menu.

## Built

- Existing shared arrival elevator, functional two-door airlock, Dispatch workstations and radio racks.
- Large War Room with a tactical map table, multiple approach circuits, columns, utility trays, workstations and a raised observation gallery.
- Restricted access corridor, inspection bend and a real four-metre descending passage.
- Irregular faceted cavern shell, high roof, rock spires and a deep chasm beneath a 36-metre steel bridge. Physical guardrails, structural supports, utility lines, work lights and a concrete far-side service station.
- Restrained corruption, administrative notices, a coffee station beside the chasm, and sparse unseen Police Operations WO messages.
- Thirteen preplaced existing enemies, including an Officer/Commander supporting the War Room detail, separate bridge-approach defenders and a concealed reserve detail for the return. No runtime enemy materialization is required.
- Eleven accessible supply pickups, objective markers, local/full map, retries, ambient sound and static render batching.

## Engine compatibility

Uses the existing world objects, rendering, inventory, pickups, combat, collision index and optimized navigation. The shared engine has one walkable height per horizontal position, so this section deliberately avoids stacked traversable routes. Its bridge is genuinely above lower visible terrain, with no playable path beneath it. Ramps and gallery heights use the shared ground sampler; both player movement and enemies use the existing step rules.

A Floor-5-only hitscan implementation anchors enemy hitboxes to their local terrain. This corrects the original world-zero vertical assumption without changing combat on Floors 1–4. The earlier objective dispatcher is preserved when switching between floors.

First-section playtests do not save a completed Floor 5 or replace campaign progress. Logistics, full planning offices, Restricted Operations, additional exploration/secrets and the descent toward Floor 6 remain for subsequent builds. The WO is not a boss in this section.

## Validation

- Walked the complete route and return with ordinary movement updates and pointer lock, including both airlock doors, the gallery ramp, geological descent, bridge, far station and Dispatch shortcut. Tested objective denial before clearing defenders and the final completion panel.
- Verified all 13 initial spawn positions are clear, Officer support buffs work, the reserve encounter opens on return, and the enemy count never increases during the route.
- Verified valid navigation paths for the bridge, descending passage and gallery, and physically navigated an enemy across the bridge. Checked terrain-following enemy height.
- Tested real hitscan damage at negative cavern elevation, no ghost hitbox at the old height, gallery hits and projectile flight below world zero.
- Audited all 11 pickups for physical clearance and accessible sight lines.
- Compared Floors 1–4 against V206: matching geometry, collision, doors, cards, keys and pickups. Tested switching repeatedly between all five floors without objective recursion or WebGL errors.
- Replayed the full Crime Reader sequence, then used the actual Floor 4 departure elevator and continued into Floor 5 with identical exit inventory. Verified full-map pause/Escape behavior, blocked weapon-wheel changes while mapped, and a clean Floor 5 retry.
- Reviewed arrival, Dispatch, War Room, gallery, passage, cavern, bridge, chasm and service-station renders. No JavaScript or WebGL errors. The section has 852 source objects, 138 static batches and 21 fixtures; software-rendered automation is not a representative GPU performance benchmark.
