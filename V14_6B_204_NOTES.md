# V14.6B.204 — Crime Reader Artwork

Replaced the Crime Reader's constructed model with the supplied demon sprite sheet. The Shift IC and all other enemy artwork remain unchanged.

- Source: `Crime Reader Demon Sprite Sheet (1).png`, 1421×1107 RGBA, already transparent.
- Extracted the eight uneven rows and eight directional columns into a transparent 1024×1024 atlas with 128×128 frames.
- Used one uniform scale and a shared foot baseline across idle, two walk frames, casting, pain, and three death stages. Death poses retain their progressively lower height.
- Removed faint transparent-background noise and disconnected neighboring-frame fragments; retained the purple casting and death effects.
- Optimized embedded PNG from 2,588,989 to 936,307 bytes, about 64% smaller.
- Reader-specific renderer uses the new textures with a model fallback if decoding fails. Preserved existing boss health, collision, attacks, cover, phase transitions, and rewards.

Validation: all 64 textures decode; pose selection and the complete tribunal introduction, attack, file return, descent, enforcement, and victory sequence pass. Reviewed in-game standing/walking, casting, pain, and grounded corpse images. The IC cleanup audit passes, and all eight pre-existing enemy sheet data constants remain byte-for-byte unchanged. No browser JavaScript errors.
