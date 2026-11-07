# V14.6B.180 — Floor 4 furniture pass

Open `MP_SHOOT_V14_6B_180_FURNITURE_PASS.html` → Mission Select → Floor 4 · Crime Reader Playtest.

## Construction and orientation

Floor 4 desks now have separate drawer pedestals, central legroom, supported monitors with housings, and physical worktops. Tables have four legs and two aprons instead of monolithic box bases. File Intake retains enclosed counter bases. Cabinet fronts have drawer panels, pulls and labels; east-wall cabinets face into their rooms, and control cabinets face their operating points.

Kitchen and conference end chairs face their tables. Terminology chairs align with the monitor positions. Playback monitors, review privacy panels, freestanding partitions, control signs and hearing lights have visible supports. Conference sheets, dossiers and microphones sit at table height. Dispatch paperwork is above cabinet tops instead of embedded in them, and the returned boss file rests on its cabinet.

## Placement and access

Rearranged Statement Records cabinets to clear both entrances. Shortened the kitchenette counter around the staff shortcut while keeping the coffee maker supported. Moved the electrical-cache cabinet to its back wall. Moved a review workstation, the evidence-return bench, a court-brief bench and the playback seating away from door approaches. Factory gantry posts sit farther inside the hall, retaining contact with their overhead beams. The automation housing retains its large scale but leaves a wider service aisle, and its input bed no longer crowds the front entrance.

Fixed the automation relocation routine: it previously identified new objects by array index even though construction removed an earlier station. This stranded the first machine components in File Intake. It now identifies newly created objects by identity, so the complete machine is assembled in M5. Its input status plate is mounted on the feed bed without the overlapping duplicate plate.

The 63-space map footprint and correction/boss sequence are retained. V179 is retained as a separate file.

## Validation

Chromium clearance checks pass at 1,290 player positions across all 86 non-lift doorway aprons, with doors open and a 0.30 m player radius. These are sampled movement checks, not a proof for every possible angle. All task/boss control standing points remain usable. Every automation-machine component is in M5, with none left in File Intake. Targeted checks verify table/desk construction, cabinet facing, chair facing, mounted controls and conference-sheet height.

The complete correction route, access gating, factory diverter/release, boss attacks, returned-file shield/jam phase, defeat and original elevator departure pass. Optional museum/shredder/secret and replay/resource checks pass. Screenshots reviewed office, support, exhibit and industrial furnishings, with no JavaScript or shader errors. Floors 1–3 geometry, collisions, doors, items, NDI cards and pickups match the preceding baseline in deterministic browser comparison.
