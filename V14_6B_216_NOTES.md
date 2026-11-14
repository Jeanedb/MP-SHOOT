# V14.6B.216 — Live LIDAR Display

- The LIDAR's painted speed numbers are replaced by a live seven-segment readout on the weapon itself. It uses the existing targeted-enemy speed measurement and line-of-sight acquisition; stationary targets show 0, and aiming away or losing a target shows dashes.
- Display alignment follows each of the six original animation frames, including firing and reloading. The screen also shows charge level and a reload indication.
- Restored the V214 pistol report and C6 legacy sound routine. V215 weapon motion, cases, hit feedback and Carl Gustaf improvements remain.
- No damage, accuracy, ammunition, progression, taser or Maple Saw changes.

Validation: browser checks compared the pistol's generated waveform sample-for-sample with V214 and verified identical C6 sound routing and balance profiles. Tested target speed, stationary/dead/lost targets, the display limit, reload indication and all six animation frames. Floors 2–5 rendered without browser or WebGL errors. Sound restoration is verified by code and waveform comparison, not direct listening.
