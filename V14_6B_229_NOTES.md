# V14.6B.229 — Crawler Attack Fix

- Fixed attack starvation after relocation: landings no longer reset the attack cooldown above the next decision interval. When a reachable target exists, crawlers wait for their current cooldown instead of starting another evasive jump. Flanking and warned pounces remain.
- Removed the cave-territory gate from pounce targeting. A reachable player within eight horizontal units and nine total units can be attacked across cave entrances, including the top of the incline. Solid cover, blocked landing points, void floor heights and range still reject targets. Relocation perches remain authored on real cave surfaces.
- Fixed the attached wall rotation to match the wall normal, with claws oriented toward the wall rather than reversing with the last jump heading. Attached living sprite frames use the surface-facing front view rather than a stale world-space movement direction. Ground, airborne and death direction selection remains unchanged.

Validation: automated browser checks cover repeated natural attacks, an attack after relocation without manually zeroing cooldown, a damaging pounce outside the cave at the top of the incline, cover and out-of-range rejection, stable attached pose despite changed jump heading, existing dodge/knockdown/LIDAR checks and rendering all five floors. Wall-facing screenshot inspected.
