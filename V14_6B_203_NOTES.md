# V14.6B.203 — Orphan Door Cleanup

Removed the remaining floating door above the command bridge: the original **IC Private Washroom** door. Its old partition walls were removed during the arena rebuild, but the separate door object remained open and parked overhead. This was distinct from the gold entrances and reserve shutters fixed in V202.

The obsolete door is removed from the live door list and its scene plan references on every arena build, including checkpoint retry. Current arena entrances, reserve shutters and the restored secret filing cabinet are retained.

Validation: identified the leftover door at the reported position, audited every remaining internal arena door against the current layout, and rendered the reported upward viewpoint. Rechecked cabinet discovery, sliding, physical entry/exit and closing; the normal Floor 2 route, command checkpoint retry, victory and elevator departure passed. No JavaScript or WebGL errors in those checks.
