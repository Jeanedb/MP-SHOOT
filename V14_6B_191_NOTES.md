# V14.6B.191 — Operations Menu and Recovered Files

Open `MP_SHOOT_V14_6B_191_OPERATIONS_MENU.html`.

The main menu now offers Continue when saved campaign progress exists, New Game, Mission Select, Armoury, Lost IDs, Settings and Credits. Export Progress, Import Progress and the music toggle have moved into Settings. The music setting is labelled Menu Music, and a separate persistent Menu Sound Volume slider controls interface feedback beneath the master volume.

Enabled music continues through menu pages, including Mission Select, Armoury, Settings, Credits, Lost IDs and the legacy briefing/difficulty screen. It preserves its playback position between pages and fades out over 240 ms when gameplay starts. It stays stopped during gameplay and pause Settings. Playback begins after the browser's first permitted keyboard or pointer interaction. Turning it off, hiding the page or leaving the page stops playback. Quiet synthesized hover, activation, Back and unavailable-option cues share keyboard/pointer feedback and respect master and menu-sound volume.

Lost IDs presents the 40 collectible slots across the four available floors as recovered files. Recovered IDs can be selected to inspect the existing in-game NDI 20 artwork and their recovery record; undiscovered slots are sealed. The collection reads the established saved ID lists and works with earlier version-1 progress files. This build reuses the existing shared ID-card artwork; it does not invent individual card owners. Normal Floor 3 and Floor 4 play buttons are available alongside the existing developer previews in Mission Select. Developer previews retain their established no-save behavior.

Continue resumes from a floor entrance, explicitly stated beneath the button. Existing saves infer the floor from completed floors and recovered IDs. Normal campaign entry now also saves an optional `resumeFloor` hint, preserved by read/import/export without changing the version-1 save format. Carried equipment uses the existing preceding-floor exit loadout. This is not a mid-floor position/checkpoint save.

New Game requires confirmation when campaign progress exists, with Cancel focused by default and an Export Existing Progress option. Cancel or Escape preserves the save. A failed browser-storage write prevents the reset and reports that the existing campaign is intact. Settings are retained when starting a new campaign.

Menus support visible keyboard focus, Up/Down and Home/End button navigation, Tab wrapping, native slider arrows, Enter/Space activation and Escape to go Back. Collection and Settings panels scroll on small screens; inspecting a card on a narrow display brings its detail into view. Import feedback appears beside the relocated save controls.

Validation: Chromium checks cover music continuity and position across menu pages, the music toggle, separate/master sound muting, synthesized cues, keyboard navigation, earlier saves, per-floor collection display, card inspection, import merge, invalid-file protection, export round trips, reload persistence, New Game confirmation/cancel/reset, blocked-storage reset protection, normal Continue into Floor 4, collecting and persisting an ID, gameplay music fade and pause Settings. Desktop and 390 px views were reviewed. The complete Floor 4 correction/factory/boss/elevator test passes; all eight embedded enemy sheets are byte-identical to V190. No JavaScript errors were observed.

V190 remains available separately. All prior artwork updates are included.
