# V14.6B.193 — Final Review Tribunal

The Crime Reader fight now takes place in a 30 × 18 m tribunal with a 7.6 m ceiling, marble columns, a raised authority bench, a central carpet, side circuits, correction displays, and a working review machine. The existing procedural Reader model remains the art placeholder.

## Trying it

Open **Mission Select → Floor 4 · Final Review Tribunal Playtest**. Open the gold door and enter the tribunal. This developer preview supplies a combat loadout and does not save campaign progress. The normal Floor 4 route also leads to the revised fight.

## Fight

- The Reader is present before entry. He is protected until review begins; crossing the threshold no longer creates him in view.
- Entry seals the door and starts a short introduction. Press **E** to skip it. Look and movement remain available.
- Formal review uses aimed folder volleys and correction lanes that warn before activating.
- At 58% remaining health, collect the rejected file at the return tray and feed it into the machine at the opposite corner. Damage already dealt is retained. This happens once.
- Jamming the machine stops its mechanism and brings the Reader around his bench and down the marble steps.
- Manual enforcement adds pursuit, warned rushes toward a committed position, and stamp shockwaves. The Reader pauses after stamping and takes increased weapon damage during recovery. Ordinary weapon stun cannot freeze his attack cycle.
- Defeat clears attacks, freezes the correction displays, changes the status lights, opens the arena, and authorizes the original elevator departure.
- Fixed ammunition, health and armour sit in side pockets; there are no recurring refills.

Health and pressure are increased to give these phases time to develop. Actual fight duration and difficulty still need human playtesting; the automated checks do not establish a three-minute completion time.

## Validation

- Chromium: full Floor 4 submission, access-card, production-floor, boss, and elevator-completion route.
- Tribunal playtest: waiting actor protection, introduction skip, both file interactions, retained damage, Reader descent, mobile stamp attack, and victory release.
- Additional checks: pre-introduction rocket protection, committed rush destination, rush completion, recovery damage bonus, three dais elevations, clear supply positions, and no false projectile hits above the player.
- Every task/control standing point checked for collision and interaction access.
- Correction lanes checked for harmless warning time and one damage application per activation.
- Floors 1–3 compared against V192: geometry, collision, doors, pickups, ID cards and access items match.
- Floor switching and WebGL error checks; no JavaScript errors in those runs.

This pass changes the Crime Reader. The Shift IC boss redesign remains a separate pass.
