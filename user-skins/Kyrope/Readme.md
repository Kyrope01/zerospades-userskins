# Kyrope

Personal skin for the in-game name `Kyrope`.

Minecraft Steve rebuilt at **native Minecraft pixel resolution** instead of repainting the
low-resolution Deuce mesh:

- `Head.kv6` — 8x8x8 with the full 8x8 Steve face (hair, eyes, nose, beard).
- `Leg.kv6` / `LegRight.kv6` — 4x4x12, indigo pants + gray shoes.
- `Arm*` / `UpperArm*` — 4x4x12 first-person limbs; sleeves team-colored.
- `Torso.kv6` — 8-wide team-colored shirt.
- `Arms.kv6` — native-thickness arms in a waist-height weapon hold.

**Only the shirt is team-colored.** Hair, face, arms/hands, pants and shoes use fixed colors.

## Resolution / bounds note

ZeroSpades renders each KV6 voxel at a fixed 0.1 blocks, so native Steve (32 px tall) would
exceed the stock player height. The torso is therefore compressed to 10 px and part pivots
overlap slightly; the assembled standing AABB still equals stock Deuce exactly, so there is
no silhouette or hitbox advantage. Crouch (`TorsoCrouch`, `Leg*Crouch`) and `Dead` keep the
stock folded/flat poses, repainted to match, because those poses are unique to ZeroSpades.

## Rules

- **Colorable:** shirt (torso, crouch torso, sleeves, dead-state shirt) uses the team sentinel;
  no fixed near-black elsewhere.
- **Readable silhouette:** assembled standing bounds equal stock Deuce; every part is a single
  connected component.
- **Every part present or inherited:** all 13 top-level parts shipped; no `Headlamp`/`XmasHat`,
  no weapon-variant folders.

Base geometry/rig from `reserved-skins/Deuce` (OpenSpades Contributors, GPL-3.0-or-later).
Fan-style recreation, not an official Minecraft asset.
