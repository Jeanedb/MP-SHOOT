# V14.6B.172 — Returned for Corrections

Open `MP_SHOOT_V14_6B_172_RETURNED_FOR_CORRECTIONS.html` locally, then choose **Mission Select → Floor 4 · Crime Reader Playtest**. Floor 3's completion button also continues into this build with the current inventory. `E` interacts, `M` opens the map and `O` recalls the current objective.

## The correction loop

File Intake now contains the floor's GO submission terminal. Submission briefly processes, reports a successful format check, then returns the file with a new deficiency. The player sees only the current requirement: no correction-round total, stage fraction or advance list of returns appears in the game.

Three authored correction assignments drive the floor:

- Investigative steps and supervisory coverage: complete both review checks, collect blue authorization in the observation gallery and resubmit.
- Referenced evidence not disclosed: collect the sealed exhibit, route it through Disclosure Control, collect red authorization and resubmit.
- Missing Will Say: recover the statement, attach it at Case Conference and resubmit.

Completed work is retained. Submitting early explains the outstanding action rather than resetting progress. Each return opens the appropriate department; task completion opens staff return routes. Review stations and evidence/statement collection require their local encounters to be cleared. The final response demands an in-person review and releases a physical gold authorization card at File Intake. Gold remains reserved for the boss door.

## A more substantial floor

The irregular enclosed area increases from approximately 2,806 to 5,648 m². There are 49 spaces including corridors and service areas, compared with 28 in V171. The original shared elevator and its arrival/departure behavior are retained.

The new north wing contains an inspection checkpoint, a large partitioned investigation review hall, supervisory review, an observation gallery and a connecting staff return passage. The south wing contains sealed exhibit storage, disclosure routing control, court brief preparation, an examination laboratory and dispatch. The west wing contains case-preparation workstations, separated interview playback booths, statement records and a staff bridge back through the support area.

Existing departments remain connected, with new encounters and supplies spread across the expanded floor. Ten NDI 20 cards and two concealed caches remain available. The full map covers the expanded footprint; its gold marker always points to the current task. Gameplay music remains disabled.

## The Crime Reader

The boss no longer uses the Shift IC sprite or attack state machine. A first-pass articulated 3D model has a heavy greatcoat, filing harness, glowing eyes and oversized red RETURNED stamp. Its attacks are:

- Folder volleys aimed at a committed position after a windup, with real wall collision.
- Correction lanes that warn on the floor before becoming dangerous, with one hit per lane activation.
- A raised-stamp attack followed by an expanding shockwave; hard cover blocks the wave's damage.

At the review threshold, the boss rejects the file and gains machine protection. The player must collect the returned file from the tray across the arena, then feed it into the review machine. This jams the machine, removes protection and resumes combat with all previous damage retained. The former IC relay interactions are removed. Direct hits, world damage and rockets cannot skip this required phase.

Boss defeat clears its remaining attacks and authorizes descent using the original arrival elevator. Floor 5 remains unbuilt. The standard completion screen and replay controls remain in use.

## Presentation and scope

Late-department fissures and boss-room breaches have branching dark cores, hot seams, broken plaster edges and scattered rubble. They are decorative surface/geometry effects, not destructible walls. Local flicker and the existing material, weapon, enemy and facility sounds remain; submission returns add a stamp impact and short paper burst.

The boss model, animations and fracture art are a playable first pass, not final sprite artwork. The review-machine jam is implemented; an elaborate cinematic transformation and recorded boss dialogue are not. The new build adds approximately 44 KB of code/data over V171 and no embedded media.

## Validation

Browser checks covered physical gating of all three wings; every task/control approach; delayed returns and persistent corrections; encounter prerequisites; gold release; connectivity of all playable departments; all boss attack patterns; lane warning/damage timing; shield damage retention; file collection and machine jam; defeat, hazard cleanup and shared-elevator departure. Replay, map/audio pause, expanded lighting and room/boss rendering were also checked.

The current 78-check regression suite passed. Deterministic browser comparisons confirmed Floors 1–3 geometry, collision, doors, items, pickups and NDI positions match V171. The approved V171 HTML remains unchanged.
