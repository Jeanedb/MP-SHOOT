# V14.6B.181 — Pressure and Light

Open `MP_SHOOT_V14_6B_181_PRESSURE_AND_LIGHT.html`, then Mission Select → Floor 4 · Crime Reader Playtest.

## Opening airlock

Floor 4 now builds the same approved airlock assembly as Floor 3, using the shared construction function: heavy hatch texture and panel dimensions, compression frames, floor grate, extraction duct/grille, pressure console and seal indicators. The two chambers already share their dimensions and world positions. Floor 4 retains its own department signage and original elevator.

The pressure cycle reuses Floor 3's update routine, including the 1.25-second equalization delay and its seal/vent/ready sounds. A request closes both hatches before equalization and opens only the requested hatch. The cycle pauses for the menu and map. The interaction hint identifies a pressure cycle rather than an ordinary door toggle.

## Lighting and visual cleanup

A Floor 4-only lighting bake now covers the entire irregular footprint, including the western factory edge. High-mounted factory and tribunal lights contribute to the bake; the old routine only considered lights below 4.05 m. Room profiles separate cooler workspaces, warm ceremonial rooms, service spaces and the industrial hall. Fixture height and solid-object occlusion shape the light pools. Factory floors and large machines use less self-illumination so the lighting has a visible effect. This is a static lightmap; phase indicators and existing local fixture effects remain dynamic.

The submission file stays visible through the stamp's contact phase. The stamp stops above the bed, the piston retains a fixed upper mounting point, and the returned file rests on its output bed. Submission timing and correction requirements are retained.

Breach edges now use continuous chipped bevel meshes following the existing openings, with branching, restrained heat fractures and masonry rubble. Removed the scattered rectangular edge patches. Corrected a boss-ceiling join defect: raising boundary boxes had also scaled custom breach wall faces, stretching their vertices. Custom faces keep their original scale, and upper masonry fills the raised wall above them. Reinforced wall collision remains intact.

## Validation

Chromium checks cover both airlock approaches, the equalization delay, closing the opposite hatch, no simultaneous open hatches during transfer, map/menu pause and replay reset. Machine checks sample 281 animation times for bed clearance, piston attachment and file visibility at contact. Lighting checks confirm full map coverage, contributing high fixtures and different warm/cool room profiles. Replay releases the owned breach mesh buffers.

The full correction progression, card gating, factory routing, boss attacks and returned-file phase, boss defeat and original elevator departure pass. Door-apron/furniture checks and optional exhibit/shredder/secret checks pass. Screenshots reviewed the airlock, workrooms, museum, shrine, factory, tribunal, machine and breaches without JavaScript or shader errors. Floors 1–3 geometry, collision, doors, items, pickups and NDI cards match V180 in deterministic browser comparison.

The map remains 63 spaces within the same footprint. This is a visual/consistency pass; final ordinary-play ammunition and encounter balance still benefits from user playtesting. V180 is retained.
