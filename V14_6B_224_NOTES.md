# V14.6B.224 — Fireball Whoosh

Replaced enemy ranged launch audio with a procedural fireball whoosh: filtered turbulent noise swells over roughly 30–45 ms, opens into a breathy rush, then fades over a 0.36–0.50-second buffer. Heavies use a deeper, longer rush and grenadiers retain a slightly longer lob cue. The launch has no pitched oscillator, electrical modulation, laser sweep or gunshot impulse.

Player weapon reports, the accepted grunt-based deaths, player pain, impact cues and all gameplay/visual settings are retained. The removed shooter pre-shot tones remain disabled.

Validation: generated buffers and stress mixing remained finite and below full scale (worst-case test peak approximately 0.72); cached variations, actual launch events, the silent shooter wind-up/delay, grunt-source correlation, damage/death cues, caps, pause/mute and scene resets passed. All five floors updated/rendered without browser or WebGL errors. Preferred pistol/C6 sounds, weapon profiles/placement and LIDAR hold remained unchanged. Perceived quality still requires a player listening test.
