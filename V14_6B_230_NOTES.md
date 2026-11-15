# V14.6B.230 — Crawler Reattack

After completing an attack recovery, engaged crawlers now have a 55% chance to attempt an evasive jump to a reachable wall/ceiling perch. They then pause, warn and pounce again. Other recoveries continue ground pressure. The choice is made once per recovery using per-crawler seeded variation; an unavailable perch falls back to the existing ground behavior.

The V229 cooldown fix remains: relocation does not reset the attack timer, and a valid target takes priority once ready. Attack range across cave entrances, solid cover checks, wall orientation, damage, warning windows, art and sounds remain as in V229.

Saved the user's generator-tunnel swarm concept in CRAWLER_TUNNEL_ENCOUNTER_IDEA.md for a future level; it is not part of this build.

Validation: simulated sustained combat checks both post-recovery choices, repeated surface pounces and damaging attacks, with no contact damage during relocation. Existing attack cooldown, outside-cave incline attack, cover/range, dodge, taser/LIDAR and five-floor rendering checks also run.
