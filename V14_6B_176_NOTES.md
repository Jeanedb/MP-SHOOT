# V14.6B.176 — Return Routing Plant

Floor 4 gains an industrial combat environment within its correction-return sequence, plus a rebuilt submission machine and further room presentation fixes. Download `MP_SHOOT_V14_6B_176_RETURN_ROUTING_PLANT.html`, open locally, then choose **Mission Select → Floor 4 · Crime Reader Playtest**.

## Return Routing Plant

The plant occupies a new western wing. Its main machinery hall measures **30 × 36 m**, with a **6.8 m ceiling**, tall numbered sorting banks, overhead file tracks, live floor belts and machinery ambience. The hall, maintenance walks, access passage, control booth and intake tunnel add **1,693.76 m²**. Floor 4 now contains **60 spaces / 8,052.68 m²** of enclosed map area within a **123.4 × 103.6 m** irregular envelope. These area figures include circulation and service spaces before subtracting furniture and walls.

The plant becomes available on the Will Say correction assignment. Recover and attach the statement as before, then enter the plant from the west end of the administrative spine. Clear the plant and use **Manual Routing Control** before resubmitting the GO. The console opens a permanent return shortcut directly into the Automation Plant. No extra key card or visible correction-return count is introduced.

- Two automatic sorting shutters cycle between open and closed lanes. Their occupied-zone sensors keep them open around players or living enemies. The maintenance route remains usable with both shutters closed.
- Conveyor crossings gently drift the player's position without turning the camera. Moving file bundles and overhead tracks make the return process visible.
- A stamping press gives an amber warning before its red strike phase. It can damage Brock once per cycle and kill enemies caught underneath. Floor markings, warning lamps and mechanical sounds identify the crossing.
- The initial encounter has five enemies, followed by two reinforcements on reaching the north side. Routing requires clearing these contacts. Supplies support the new combat area.
- Plant mechanisms pause with the game and map. The wing appears in amber on the floor map, with the current task marker directing the player to its entrance and then its control booth.

## Submission machine

The existing small machine room remains separate. Its mechanism now has attached feed rollers, an inspection window, an axle-mounted gear, a guided hydraulic stamp and a return tray. The file moves horizontally into the housing, the mounted stamp strokes, and a rejected file slides onto the output tray. The floating paper burst is removed. The main display has a clear sightline above the working mechanism.

The existing submission interaction and 2.75-second review delay are retained. The boss's separate review-machine interaction remains unchanged. The visible input/output files are presentation objects; mission progress still uses the existing GO interaction.

## Other fixes

The terminology counters are labelled on both faces and gain reference books and editing stations. Case Conference receives formal hearing-room finishes, table dossiers, microphones and focused lighting. Museum doors use ceremonial wood-and-gold panels; its remaining office ceiling texture and strip fittings are replaced. Wall breaches are wider and irregular, with scorched edges, warmer recesses and restrained floor spill; the uniform crossbars are removed. The breaches retain wall collision and do not form new routes.

Boss artwork, gold-card boss access, optional exhibits, secrets and return to the original elevator are preserved. No gameplay music or embedded media is added. The HTML grows by approximately **29 KB** over V175.

## Validation

Browser tests cover the complete correction route, rejection of unrouted submissions, plant routing, all-room connectivity, boss mechanics and elevator departure. Targeted checks cover the closed-shutter maintenance route, shortcut clearance, occupied-gate safety, press warnings/player and enemy damage, conveyor drift without camera rotation, pause/map behavior, machine feed/stamp/output positions, optional interactions and replay cleanup. Environmental views render without script or shader errors. Deterministic comparisons confirm unchanged Floors 1–3 geometry, collision, doors and item positions.
