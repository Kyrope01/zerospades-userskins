# Kyrope

Personal skin for the in-game name `Kyrope`.

Minecraft Steve-style look: blocky brown hair, simple pixel face, short-sleeve shirt,
indigo pants, and gray shoes. **Only the shirt is team-colored**; hair, face, arms,
pants, and shoes use fixed colors.

Built on `reserved-skins/Deuce` geometry from ZeroSpades so the player silhouette and
bounds stay stock. The Deuce base model is credited to OpenSpades Contributors and
distributed under GPL-3.0-or-later; see the upstream
`Resources/License/Credits-pak010-BaseSkin.md`. This is a fan-style recreation, not an
official Minecraft asset.

## Shipped parts

All 13 top-level parts are shipped so the Steve look is consistent in every state:

- `Head.kv6` — brown hair, pixel face.
- `Torso.kv6`, `TorsoCrouch.kv6` — team-colored shirt.
- `Arms.kv6` — team-colored short sleeves, skin arms/hands.
- `Arm.kv6`, `ArmRight.kv6` — skin forearms/hands with a team-colored sleeve cuff.
- `UpperArm.kv6`, `UpperArmRight.kv6` — team-colored sleeves.
- `Leg.kv6`, `LegRight.kv6`, `LegCrouch.kv6`, `LegRightCrouch.kv6` — fixed indigo pants and gray shoes.
- `Dead.kv6` — matching hair/shirt/pants/shoes.

There are no `Rifle/`, `SMG/`, or `Shotgun/` overrides, so the top-level parts apply
whatever the player holds. `Headlamp.kv6` and `XmasHat.kv6` are not shipped.

## Rule checks

- **Colorable:** the shirt (torso, crouch torso, sleeves, and dead-state shirt) uses the
  black team-color sentinel. No fixed near-black colors are used elsewhere.
- **Readable silhouette:** every part keeps stock Deuce voxel occupancy, dimensions, and
  pivots, so the assembled player bounds are unchanged. Hitboxes are unchanged.
- **Every part present or inherited:** all 13 parts are present; no shared accessories are
  shipped.
