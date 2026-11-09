# V14.6B.198 — Command Override

Revamped Floor 2's Shift IC fight as a tactical command encounter. The Crime Reader tribunal remains the V197 version.

## Try it immediately

**Mission Select → Floor 2 · Shift IC Command Arena Playtest** starts outside the gold entrance with a combat loadout. Open the door and enter; press **E** to skip the short introduction. Developer previews do not save campaign progress. The normal Floor 2 route also leads to this fight.

## Arena and encounter

- Rebuilt the existing 23.5 × 37.3 m command room with a roughly 6.8 m ceiling, a stepped command bridge, suspended communications equipment, navy floor treatment, six steel cover columns, and intact console banks. Neighbouring rooms and the original access-card progression retain their layout.
- The IC waits on the bridge before entry. Two reserve guards are also present from the start, behind opaque shutters.
- The first phase uses warned, aimed command volleys. Two amber uplinks announce supporting crossfire before firing toward a committed target.
- Shoot the uplinks to remove their supporting fire and weaken command armour. They are optional counterplay, not mandatory invulnerability-switch errands. Their destruction also creates a brief recovery opening.
- At 55% remaining health, the IC releases the reserve detail and leaves the bridge. Damage already dealt is retained; no repeated shield cycle is added.
- The mobile phase adds repositioning, warned suppression sweeps and a short-range baton attack. Committed attacks leave recovery windows that reward accurate fire. Ordinary weapon stun cannot freeze the IC's attack cycle.
- IC projectiles use complete swept collision against cover and the player. Columns and console banks provide physical protection at their actual heights.
- Fixed ammunition, health and armour are placed in reachable side pockets. There are no renewable refills.
- Victory stops command fire, changes the arena displays and status lights, releases the doors, and orders surviving reserves to retreat. Use the bridge terminal to authorize the existing elevator departure to Floor 3.

The current IC sprite is retained. Health and cadence are a first playable tuning pass; human playtesting is still needed to judge difficulty and fight duration.

## Validation

- Chromium: normal Floor 2 arrival, the original gallery/cinema/range lockdowns, blue/red/gold card collection, boss entry, command checkpoint capture/retry, victory, terminal authorization, elevator completion and Floor 3 continuation button.
- Arena connectivity: reachable bridge terminal and uplink firing positions; all fixed supply positions clear of collision.
- Actual weapon rays and impacts on both uplinks; supporting fire disabled after isolation.
- Command volleys, supporting-fire warnings, midpoint deployment, reserve exit, bridge descent, baton tell and suppression sweep exercised.
- All six cover columns checked from both axes with multiple simulation step sizes. Exposed-player hits and recovery damage bonus checked.
- Rocket damage checked through the midpoint and victory. Surviving reserves stop firing after authority is revoked.
- Floors 1, 3 and 4 compared with V197: geometry, collision, doors, access items, ID cards and pickups match.
- Rendering inspection and JavaScript/WebGL error checks passed.
