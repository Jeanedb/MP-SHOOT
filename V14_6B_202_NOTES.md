# V14.6B.202 — Command Room Cleanup

- Fixed the floating door leaves above the IC arena. The two gold entrances and two reserve shutters now retract within their original openings and disappear when fully retracted. Raising the arena ceiling had exposed the old fully-open parking position. Other Floor 2 doors retain their existing rendering.
- Restored all 12 visible pieces of the hidden-room filing cabinet: its body, drawer fronts, handles and label. The arena's furniture cleanup now preserves moving secret-door pieces. Previously the graphics were removed while the moving solid body and interaction remained active.
- The cabinet retains its original discovery, sideways slide, collision and close behavior. IC health, CCTV monitors, uplink turrets and combat tuning remain unchanged.

Validation: reproduced the missing cabinet graphics and exposed parked door leaves in V201. Checked all four IC doors throughout opening/closing, cabinet visibility and dynamic rendering, normal E discovery/open/close, and walking into the hidden room and back out. Both gold arena entrances were crossed using normal forward movement. The normal Floor 2 route, lockdowns/cards, command checkpoint retry, victory, terminal authorization and elevator departure passed. Rendering inspection and JavaScript/WebGL checks passed.
