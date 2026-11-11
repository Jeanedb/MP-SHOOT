# V14.6B.210 — Police Operations Expanded

Expands Floor 5 around its existing War Room and cavern, with approximately 49% more mapped floor area than V209 (rectangle-union area, before furniture). The cavern crossing remains the central reveal and Restricted Operations remains the finish.

## New playable spaces and flow

- A raised watch wing contains Watch Dispatch, Communications, Duty Briefing, and a rear cross-passage. Access from Dispatch and the War Room gallery creates two routes through the department.
- Restore the Operations net at Communications before the War Room can release geological access. Six preplaced enemies defend this wing.
- Logistics now connects to an internal freight/loading bay, a maintenance workshop, and equipment service aisles. Crates, shelving, benches, a motor and lifting frame give these areas different combat layouts.
- Movement authority is now issued at the workshop counter. Both the original Logistics detail and the five-person loading/workshop detail must be cleared. Two connections lead onward into Planning.
- Recovering Restricted authority also opens West Maintenance. Three preplaced enemies defend an optional return through the maintenance ramp into Duty Briefing; the original service return is still available.
- The existing War Room return detail, Restricted Operations defence, and departure elevator remain in the route. The WO stays unseen, and Floor 6 remains explicitly unbuilt.

## Construction and encounter cleanup

- Corrected the gallery's terrain rise from 1.0 to 1.6 metres at the ramp top, matching the platform, side panels and railing. Extended the surface to meet the north wall.
- Rebuilt the west service junction with framed maintenance access and enclosing walls, replacing the exposed angled junction visible in V209.
- Added partitions and door headers between adjoining departments; enclosed the equipment cage sides and grounded the freight shutter.
- Moved a Logistics rack clear of the new loading approach and placed the workshop wall bench away from the service doorway.
- The return ramp uses a grade that supports both normal player movement and the existing enemy navigation grid.
- Scoped War Room, geology, and bridge activation to their actual areas so visiting the new wing does not trigger unrelated announcements through walls.
- Extended the map, lighting coverage, and navigation bounds. Added supplies and relocated three IDs into the expanded departments while preserving their persistent IDs.

## Validation

- Full browser walkthrough using ordinary movement: airlock, Communications, gallery ramp, War Room release, cavern, Logistics, loading/workshop, Planning, maintenance return, War Room report, final defence, and elevator departure.
- The walkthrough grants test health and uses direct enemy damage to isolate route/gate behaviour; combat difficulty still needs player feedback.
- All 41 initial enemy positions, 40 authored supply pickups, ten Lost IDs, and two secrets passed clearance checks. Navigation checks covered the new loops, return ramp, original service route, and secret access.
- Campaign saving, ID persistence, normal retry, developer-save isolation, and actual Floor 4 inventory transfer passed browser checks.
- Floors 1–4 geometry, collision, doors, pickups and IDs matched the preceding baseline; repeated floor switching passed.
- Construction and visual checks passed without JavaScript or WebGL errors.
