# V14.6B.212 — C8 Aimed Fire Feedback

The dedicated C8 sight image previously remained stationary when firing, hiding the rifle's normal firing-frame feedback. Aimed shots now animate that sight picture and add a short visual camera impulse.

- Brief upward rifle jolt with a small rearward scale change and damped settling motion.
- A restrained upward camera impulse that returns to zero in 0.22 seconds. The existing permanent recoil and shooting ray remain unchanged.
- Short, asymmetric muzzle flash around the outside edges of the sight housing; the centre of the sight window stays clear.
- A small extra burst of impact sparks for aimed hits on world surfaces. Confirmed enemy hits retain the existing hit marker and damage behaviour.
- Feedback starts only after a successful aimed shot, clears on reload, weapon change or scene change, and pauses with gameplay.

Browser checks verified one round per aimed trigger pull, no repeat while holding, unchanged three-round hip bursts, no false feedback from empty/reloading triggers, exact return of the sight canvas to its idle image, preserved permanent recoil, pause/switch cleanup, and firing presentation across the campaign floors. Visual checks reviewed the shot and recovery against the cavern sightline. No JavaScript or WebGL errors were reported.

This is a presentation change; weapon damage, accuracy, ammunition costs, fire modes and sound are unchanged. Recoil strength and flash appearance remain subject to player feel testing.
