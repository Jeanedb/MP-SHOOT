# V14.6B.214 — Weapon Range and Damage

Second weapon pass: establish close, medium and distant weapon roles on top of V213's progression/ammunition changes.

## C8

- Hip-fire burst spread is wider, while recovery between bursts is faster. Close bursts remain dependable; distant hip fire loses accuracy naturally rather than forcing a fixed number of hits.
- Fully raised aimed fire has zero random spread. Accuracy still depends on the player's aim, target movement, cover and the weapon's existing recoil.
- Hip-fire enemy range remains 22 world units. Fully aimed shots can hit enemies out to 60, fixing the old shared 22-unit ceiling that undermined the optic on long sightlines.
- Existing single-shot/burst modes, damage, ammunition costs, recoil and V212's aimed firing feedback remain in use.

## Shotgun

- Nine pellets remain, with a wider horizontal and vertical spread.
- Each pellet retains full damage through 5 units, then falls to 65% at 10, 25% at 16, and 10% at 22. These distances refer to the actual pellet hit, not the target's centre.
- The first-pellet stagger scales with the same falloff, reducing distant interruption and knockback.
- Magazine, shell loading, fire cadence and close-range damage remain unchanged.

## C6

- Extends enemy range to 32 units so controlled bursts have a medium-range role between ordinary hip fire and C8 aimed shots.
- Retains the existing 100-round belt, damage, heat, spread buildup, recoil, movement penalty and reload. Sustained-fire feel will be addressed in the next pass.

Extended rays preserve nearer world/prop hits, stop at cover and ordinary enemies, and do not add penetration. Other weapons and enemy health are unchanged.

## Validation

Browser shooting samples used a stationary, centred ordinary target in an open test lane, with existing recoil applied between burst rounds. These measurements are comparisons, not guaranteed combat hit rates:

| C8 mode / target distance | Observed hit rate |
| --- | --- |
| Burst / 4 units | 100% |
| Burst / 12 units | About 84% |
| Burst / 21.5 units | About 38% — about 1.15 hits per three-round burst |
| Fully aimed / 4–55 units | 100% in the stationary test |

Shotgun samples retained 9 damage at 4 units, averaged about 3.6 at 10, and averaged below 1 at 16 and beyond. Tests also checked explicit per-pellet falloff, the transition past the old rifle range limit, cover occlusion, maximum ranges, C6 range, fire modes, aimed-shot feedback, and firing/rendering on all five floors. No browser or WebGL errors were reported.

Normal encounter playtesting is still needed before the weapon feel pass; target size, movement, recoil control and powerups change practical results.
