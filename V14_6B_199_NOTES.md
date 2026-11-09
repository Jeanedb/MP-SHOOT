# V14.6B.199 — Command Access Fix

Fixed entry to the revamped Shift IC arena. The decorative upper perimeter walls added above the original room had been marked solid. Movement collision tests their floor footprints, so the upper wall spanned each doorway as an invisible barrier even after its gold door opened.

The upper wall extensions now render without movement colliders. The original boundary walls, doors, columns and console cover retain their collision.

Validation: reproduced the overhead blocking collider in V198. In V199, used E to open each gold entrance and held the normal forward movement input to walk through both the west and rear doors. Both approaches now enter the room and trigger the IC introduction. JavaScript and WebGL checks passed.

Use the same **Mission Select → Floor 2 · Shift IC Command Arena Playtest** shortcut.
