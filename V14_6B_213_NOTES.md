# V14.6B.213 — Weapon Progression and Ammunition

First of the planned weapon passes: early campaign acquisition and ammunition supply.

## Core issue progression

| Floor | Intended core equipment progression |
| --- | --- |
| 1 | Start with pistol and unlimited baton. Collect the C8 near O.R. blue clearance. The existing armoury C8 remains a spare/resupply. |
| 2 | Carry the earned C8 forward; Dispatch provides a backup issue. Acquire the shotgun later in red-access Range Control. |
| 3–5 | Carry the core weapons forward. Existing replacement/resupply pickups remain. |

Number keys, HUD slots, pickup notices, the Armoury listing, and mouse-wheel order now agree: 1 pistol, 2 C8, 3 shotgun. Slots 4–9 retain their existing assignments. Advanced weapon issue locations are not introduced in this early progression pass; the developer loadout still exposes all nine weapons for the later balance and specialist passes.

## Pistol ammunition

- Reserve capacity increased from 150 to 240; the magazine remains 12 rounds.
- New normal Floor 1 starts with 72 reserve rounds instead of 48.
- Fixed 9 mm boxes supply up to 50 rounds. New enemy-dropped pistol magazines supply up to 24.
- Save validation, import/export sanitization, campaign transfer, and developer presets accept the new capacity. Existing saved amounts are preserved rather than automatically refilled.
- Added pistol supplies in Floor 1 Investigation/O.R. and Floor 2 Screening/Training. Converted an early Investigation rifle-ammo box and two Floor 2 supply points to pistol ammunition.

## Enemy drops

- Existing probabilities of receiving ammo versus health, powers or nothing remain unchanged.
- Without an owned C8, an enemy ammo roll supplies pistol magazines rather than unusable 5.56.
- With a C8, 70% of Floor 1 ammo rolls and 60% of Floor 2 ammo rolls supply pistol magazines. When a shotgun is owned, 15 percentage points of the remaining rolls may supply shells; the rest provide 5.56.
- Later-floor ammo rolls retain their existing rifle emphasis once the player owns the C8. Brass Magnet still boosts the underlying ammo-roll weight.
- Loose 5.56 requires an owned C8, matching the existing ownership checks for other ammunition types.

## Validation

Browser checks covered normal pistol/baton start; clearance C8 collection before a shotgun; new pickup clearance and actual collection; fixed-box/drop quantities and the 240 reserve cap; saved inventory above the old cap; normal Floor 1-to-2 transfer; Floor 2 placement in Dispatch/Range Control; sampled drop distributions with and without a C8; number keys and wheel cycling; normal retry inventory and unique issue pickups; and the full developer loadout. No browser or WebGL errors were reported.

This pass does not change weapon damage, spread, range falloff, recoil, or enemy health. Ammunition abundance and the later shotgun issue need a normal campaign playtest before the next balance pass.
