# V14.6B.184 — Combat and controls

Build: `MP_SHOOT_V14_6B_184_COMBAT_AND_CONTROLS.html`

Mouse look now reaches almost straight up and down (89.94 degrees). Weapon recoil uses the same expanded limit, preventing camera snaps back to the old limit. Mouse-wheel down selects the next owned weapon and up selects the previous, in number-key order, with wrapping and scroll debouncing. Cycling uses the existing weapon-switch handling and is inactive in menus, maps and elevator travel.

Chargers check a body-width route before committing. When furniture blocks a rush, they seek another lane. A 0.60-second tell locks direction for its last 0.20 seconds; the rush then commits to that heading. Sidestepping can produce a miss and recovery window. Movement substeps stop charges against furniture and closing doors instead of tunneling through them.

Grenadiers have 9 health (previously 6) and 1.22 movement speed (previously 1.02). Throws use shorter flight times, limited movement prediction and collision-checked ballistic arcs. Blast radius is 3.2 metres with maximum damage 18, using the existing cover and blast falloff rules. The 0.55-second preparation and 0.65-second recovery remain readable opportunities to react. Grenadiers reposition for throws and retreat at close range. These AI and control changes apply across the campaign.

On Floor 4, the Evidence charger starts in a clear aisle and the Conference grenadier has a clearer position opposite its shooter partner. Enemy counts are unchanged. Eight obstructed supplies were moved locally, including the factory medikit embedded in the maintenance partition. Supply types and amounts are unchanged.

Validation used browser-driven controlled simulations: near-vertical aiming and recoil, wheel switching and menu gating, charger navigation around an actual desk, committed-charge dodging, a closing factory hatch, grenade pressure versus small and large dodges, closed-door arc rejection, and collecting the relocated medikit. Charger/grenadier smoke checks passed on Floors 1–3. Floor 4 task progression, factory controls, room access, secrets, Crime Reader mechanics, exit and replay checks passed with no JavaScript errors. Floors 1–3 geometry, collision, doors, cards, items and pickups exactly match V183. Camera and pickup screenshots were inspected.

These checks establish function and clearance, not final combat balance. Playtest mixed encounters to assess the increased grenade pressure and charge tells. No new enemy classes were added. The documented Wall of Shame/Brock, damage artwork and mechanical-room revisions remain deferred. V183 is retained.
