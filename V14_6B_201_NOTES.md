# V14.6B.201 — Uplink Turrets

Both command uplinks now visibly power mounted security turrets. Swivel posts, armoured receivers, long barrels, dark muzzle bores, tracking sensors, amber charge lights and exposed power conduits make the source of supporting fire identifiable. Uplink labels sit below the existing orange core so they do not hide the weapon silhouette.

- Turrets turn toward the player, then retain the existing committed aim point during their 1.8-second warning. Amber indicators and rising charging chirps precede the volley.
- Supporting projectiles originate at the actual barrel muzzle. Firing adds a brief muzzle flash and barrel recoil.
- Destroying the uplink darkens its core, conduit and turret indicators, cancels its pending volley and lowers the gun into an inactive pose. The turret receiver shares the uplink's health, so shooting the gun also disables its connected cabinet. The original orange core remains the larger direct target.
- Disabling uplinks remains optional. IC health stays at 180; uplink health, crossfire cadence, shot count and damage retain their V200 values. Cover, the CCTV wall, boss phases and access fix are preserved.
- Moving turret parts add no movement colliders.

Validation in Chromium: tracking, pre-fire warning/charging, committed targeting, muzzle origin and flash, shared receiver/core damage, disabled pose and queued-volley cancellation, both uplinks stopping supporting fire, and column cover against mounted-turret shots. Both gold entrances were crossed with normal forward movement. The normal Floor 2 route, original lockdowns/cards, command checkpoint retry, victory, terminal and elevator departure also passed. Rendering inspection and JavaScript/WebGL checks passed.

Quick access: **Mission Select → Floor 2 · Shift IC Command Arena Playtest**.
