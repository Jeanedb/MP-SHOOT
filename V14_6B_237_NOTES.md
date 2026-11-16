# V14.6B.237 — Operations Departments / first layout pass

Added six departments and connecting access halls with floors, ceilings, solid partitions, working doors, basic furnishings and wayfinding:

- Personnel Allocation and Scheduling opens off the War Room's south side. Its roster assigns Cpl Thompson and Cpl Fraser to every shift across the entire facility, stamped MINIMUM MANNING ACHIEVED. A sticky note blames mandatory training.
- Delegation / WO Tasking is reached through Personnel. The same two members receive all practical tasks; the WO monitors progress.
- Morale and Welfare and Training and Readiness have separate doors off a new hall extension from the Logistics service corridor. The breakroom contains an ordinary coffee counter, microwave, fridge, mugs and lunch table. Training has four empty computer desks and a mandatory-instruction board.
- Incident Triage opens off the Operations cross-passage near Communications. Request boards classify the escalating incidents as routine.
- An 18×18-metre server farm lies off the north side of Logistics and links back into the Planning lobby. Twenty rack towers provide most of its light. Clear front, rear and cross-aisles support a three-enemy shooter/flanker encounter authored at level build time, without on-screen spawning. The server detail activates when the player enters.

Both server links use the same blue movement authority issued by the workshop as the existing Planning entrance. This is an alternate route, not a new mandatory objective or enemy-clearance gate. In the server area the objective marker points to the Planning link until Restricted authority is recovered. Two modest supplies are at the far end.

Expanded floor-plan/light-atlas/navigation bounds for the new rooms. Existing shells build before the additions so shared walls are only cut at intended doorways. The original ten Lost IDs, two secrets, objective sequence, crawler behavior, corruption, roof damage, lava and fuel drums are retained. New static architecture and rack lights use existing batching; no animated server textures or new ambient audio are included in this first layout pass.

Validation: browser checks cover all nine department/hall footprints, working portal clearances and floor levels, a clear roster/Delegation doorway, blue-authority gating, walking routes and rack cross-aisles, activation of pre-existing server actors and their navigation around racks, objective targeting, preserved ID/secret counts and replay without duplicated room records. Reviewed all six room captures. Existing wall/cover, barrel, secret-access and five-floor render checks pass without browser/WebGL errors.
