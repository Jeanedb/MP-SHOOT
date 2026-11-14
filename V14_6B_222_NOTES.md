# V14.6B.222 — Gritty Combat Audio

Responds to feedback on V221's death and enemy firing sounds.

- Death sounds now derive from the same per-species procedural grunt buffers used by living enemies, rather than V221's separate formant vocal synthesis. A short attack and fading breath envelope make them death variants while retaining the existing throat/noise texture. Three small variations, spatial attenuation, voice caps and the LIDAR's brief vocal delay remain.
- Enemy ranged launch sounds use a shorter, noise-led electrical pressure burst with a low body tone. Removed the large descending pitch sweep, frequency modulation and bright ringing launch component from V221. Heavies and lobbed attacks retain different weight/duration.
- Removed the shooter's separate legacy square-tone aiming cue, which was still playing before the actual discharge. Its aiming pose, visual glint, delay and burst timing are unchanged.
- Retains player pain, armour/flesh/surface impacts, preferred pistol/C6 sounds, audio cleanup, performance fixes and weapon/gameplay balance.

Validation: browser checks exercised the real shooter move/aim/burst cycle and found no legacy square-tone event before firing, with the delay and projectile retained. Waveform correlation verified the new death sound comes from the existing living grunt with the intended envelope. All 63 tested source variants were finite, bounded, cached and faded; a worst-case offline mix stayed below full scale. Death/duplicate suppression, pain cooldown, immunity, distinct launch/impact events, pause/mute, scene resets, and all-five-floor rendering passed without browser or WebGL errors. Preferred player reports, weapon profiles, placement and LIDAR hold remained unchanged.

The revision follows the requested sound design, but automated checks do not establish perceived audio quality; its character and mix still need a player listening test.
