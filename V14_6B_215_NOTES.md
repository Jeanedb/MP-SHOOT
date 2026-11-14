# V14.6B.215 — Weapon Feel

Third weapon pass: stronger firing and impact presentation while retaining V214's damage, range and accuracy tuning.

## Firing feedback

- Pistol: sharper cached report, short weapon jolt, small camera impulse and visible case ejection.
- Shotgun: a heavier weapon movement with a longer settling motion, a short camera kick, warm muzzle illumination and shell ejection timed after the shot.
- C6: connects the existing cached heavy report to actual firing, replacing the legacy tone/noise routine. Repeated weapon impulses alternate slightly and build with the existing heat value; ejected cases remain bounded in number.
- Carl Gustaf: stronger launch report and weapon impulse; impact adds a deeper 1.25-second blast report, brief warm pressure flare, expanding ground pulse, dust and short-lived debris. Camera response weakens with distance and obstruction.
- The C8's dedicated aimed-fire feedback remains intact. Specialist weapon mechanics remain for the following pass.

## Hit readability and cleanup

- Hit, shield-block and kill marker colours now apply on all five floors, extending the existing feedback beyond Floors 1–2.
- Damaging bullet hits receive a slightly more visible sprite-only flinch, with smaller reactions on heavy classes. Enemy hitboxes, stun values and knockback physics are unchanged.
- Rocket misses no longer show an enemy hit confirmation. Actual rocket damage and kills use the existing confirmed-hit feedback.
- Weapon switching clears leftover muzzle/smoke animation so the newly selected weapon does not appear to fire an old shot.
- New effects clear on scene changes, recover after firing, pause with gameplay, and respect sound muting. The system reduced-motion preference reduces weapon and camera motion.
- New presentation variation uses a private random generator rather than consuming gameplay random numbers.

## Validation

A browser comparison against V214 checked identical firearm/C6/Carl Gustaf profiles, shot damage, ammunition expenditure, permanent player recoil, fire cooldowns, heat, projectile creation, rocket damage and self-damage.

Additional checks covered visible firing/recovery for the four affected weapons; sustained C6 feedback and bounded case counts; empty trigger, pause, switch and scene cleanup; explosion feedback and cleanup without false hit confirmation; later-floor kill marker colour; all-five-floor launch/explosion rendering; mute behaviour; and reduced-motion attenuation. Offline audio rendering verified a finite explosion output, a bounded source peak and an audible-length low tail. Visual captures reviewed firing poses and blast timing. No browser or WebGL errors were reported.

This build changes presentation rather than weapon balance. Perceived weight, camera comfort and sound mix still need the player's feel test.
