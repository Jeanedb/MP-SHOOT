# V14.6B.221 — Procedural Combat Audio

Temporary procedural combat cues; no external audio recordings or speech assets.

## Changes

- Replaced old enemy ranged-fire pops at actual projectile creation with a frequency-swept electrical discharge and energy tail. Shooters/shields use the main plasma cue; heavies have a deeper discharge; grenadiers have a separate lob cue; officers and IC fire ports use a sharper energy report. Legacy launch sounds are suppressed to avoid doubling.
- Added varied synthetic death grunts/growls through the existing death/drop event, covering player weapons, explosions and environmental kills without triggering on spawn/checkpoint restoration or LIDAR's temporary trace flags. Heavies/shields and officers use different vocal profiles. A full-power LIDAR kill delays the death vocal briefly to accompany its frozen pose.
- Added synthetic player pain grunts, with ordinary/heavy variants and a 0.68-second cooldown. Armour and flesh impacts differ. Immunity and zero actual damage produce no false pain/impact cue.
- Plasma surface impacts distinguish metal, stone, wood and glass; direct player impacts use the damage cue rather than duplicating a wall impact. Heavy energy explosions have their own discharge tail. Existing player gun reports, including the preferred pistol and C6, are retained.
- Positional cues use distance attenuation, stereo placement and obstruction filtering. Sound buffers are cached with three variants each, use private random state, and have short fade-ins/outs. Limits cap simultaneous voices at 16, including per-category caps; player pain can displace a lower-priority voice when necessary.
- Pause, maps, pointer unlock, mute and scene changes silence/cancel the new voices. Audio does not alter damage, enemy/projectile timing, weapon balance, LIDAR hold/penetration, or weapon positioning.

## Validation

- All 48 generated buffer variants were finite, non-silent, cached, below a 0.8 source peak and faded at the end. Test generation averaged about 2.6 ms per buffer; subsequent plays reuse the cache.
- Worst-case offline mixing remained finite and below full scale (peak approximately 0.52 in the test), respecting the voice cap and player-pain priority.
- Browser checks covered actual projectile creation for five enemy types, armour/flesh and light/heavy damage, pain cooldown, immunity, death/duplicate suppression, kill accounting, plasma wall/player separation, caps, mute, pause, scene resets, and update/render on all five floors without browser or WebGL errors.
- Pistol waveform and C6 routing matched V220; weapon profiles, positioning and the LIDAR hold pose matched the prior build.

These vocal sounds are synthesized placeholders, not recorded human/demon performances. Automated waveform and integration checks do not establish perceived sound quality; the final volume balance and character require a player listening test.
