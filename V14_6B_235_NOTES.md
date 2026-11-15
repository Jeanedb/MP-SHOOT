# V14.6B.235 — Compromised Operations

Cut a real six-by-six-metre opening into part of the War Room ceiling. Most ceiling panels remain intact; the localized breach exposes a raised rock cavity, broken panel edges, bent beam ends and three hanging cables. Two cable tips intermittently shed short, bounded spark bursts. Scattered low debris marks the floor below without adding solid obstacles to the combat circuit or exits.

A narrow winding lava channel crosses the big cavern far below the bridge at y=-22, with dark crust, slow surface flow and warm-toned rock banks. It avoids the existing major rock spires so the river remains legible from the crossing. The bridge, service paths and existing fall behavior remain unchanged.

The lava uses one static mesh and a time-based texture-coordinate offset in the existing shader; no per-frame texture uploads are needed. Roof debris/wires/rock use static batching. Sparks are bounded to six points per active cable burst and restore blend/depth state. The prior selective light faults, gallery cleanup, materials and crawler behavior remain.

Validation: browser checks cover the roof opening, two spark sources, lava below bridge height and the animation time uniform, alongside gallery/fixture/access checks and all-five-floor rendering without browser/WebGL errors. Reviewed upward roof and downward bridge captures.
