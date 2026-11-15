# Future level idea — Generator tunnel swarm

User concept, saved for a later level; not implemented in V230.

The player follows a long tunnel to an objective such as a generator. Activating it briefly cuts the tunnel lights. When they return, the tunnel is revealed to be full of hundreds of crawlers. The player can fight at substantial health/ammunition cost and risk, or run back to safety.

Design points to explore when building the level:
- Let the outward journey teach the escape route and establish its length before the reveal.
- Keep the generator and the resulting objective state clear so retreat feels like a valid decision.
- Preserve an achievable route to safety; do not require clearing the swarm to complete the objective.
- Sell the overwhelming numbers through the reveal and distant movement. Prototype performance with bounded active combat actors and cheaper distant creatures before committing to hundreds of fully simulated enemies.
- Tune pressure, lighting, audio cues and escape spacing through playtesting. Avoid spawning the visible swarm directly in the player's view.
