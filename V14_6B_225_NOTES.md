# V14.6B.225 — Low Fireball Whoosh

Used the supplied fireball MP3 as a frequency-balance reference only. The recording is not embedded, sampled, resynthesized from its waveform or played by the game.

- Added a broad, filtered low rumble beneath the existing procedural rushing-air launch.
- Reduced the thin high-frequency hiss substantially. Two low-pass stages shape the body, with a gentle high-pass to avoid DC/subsonic build-up. Heavies use a lower band than standard fireballs.
- Retained the whoosh's swell and timing, with no gunshot impulse, pitched oscillator, laser sweep or electrical modulation. Player weapons, grunts, pain and impacts are unchanged.

The reference measured about 76% of its spectral energy below 250 Hz. The revised standard launch measured about 68% below 250 Hz and 95% below 600 Hz, preserving some upper air texture. These are broad spectral measurements, not a claim of an exact perceptual match or direct listening.

Validation: finite/bounded/cached/faded source buffers; worst-case offline mix below full scale (test peak approximately 0.73); actual shot, death and damage events; silent pre-shot aiming cue; grunt-source correlation; mute/pause/caps/scene cleanup; and all-five-floor browser/WebGL checks. Preferred player reports and all weapon/gameplay tuning were retained. Final bass level requires a player listening test.
