# V242 — Visible Bridge Collapse

The V241 collapsing bridge pieces were included in Floor 5 static render batches. Moving/removing the original objects changed terrain and navigation, but left the cached deck and railings visible. Mark falling pieces as f5Moving during construction, before scene preparation, so the existing batching system excludes them and renders their live transforms instead.

Validation: explicitly prepare static rendering, assert every falling piece remains unbatched, run sabotage and removal, inspect the destroyed bridge from the reported position (102.1, 0.2), and run the return-route, mission progression, alternate-trigger, replay and five-floor rendering checks.
