# Kyrope

Personal skin for the in-game name `Kyrope`.

Based on `reserved-skins/Deuce` from ZeroSpades. The Deuce base model is credited to
OpenSpades Contributors and distributed under GPL-3.0-or-later; see the upstream
`Resources/License/Credits-pak010-BaseSkin.md`.

## Shipped parts

- `Head.kv6` — stock head shape, cap replaced with brown hair, warm shaded face.
- `Torso.kv6` — shirtless muscular torso, warm shading, team-colored belt.
- `Arms.kv6` — stock third-person arm shape, recolored to bare warm skin.

Every other part is omitted on purpose and inherits `Deuce`. There are no `Rifle/`,
`SMG/`, or `Shotgun/` overrides, so the top-level parts apply whatever the player holds.
`Headlamp.kv6` and `XmasHat.kv6` are not shipped.

## Rule checks

- **Colorable:** both inherited pants legs and the torso belt keep the black team-color
  sentinel. Skin, hair, eyes, and boots use fixed non-black colors, so team identity is
  carried by the pants/belt rather than being painted over.
- **Readable silhouette:** `Head` and `Arms` keep stock Deuce voxel occupancy. The wider
  `Torso` stays inside the stock standing player bounds for classic, Rifle, SMG, and
  Shotgun, and the final standing AABB equals classic Deuce. Hitboxes are unchanged.
- **Every part present or inherited:** the three changed parts are present; all missing
  parts fall back to `Deuce`.

## Cosmetic inheritance note

Crouch torso/legs, first-person `Arm`/`UpperArm`, and `Dead` currently inherit stock
Deuce, so those states still show the default uniform rather than the shirtless look.
That is allowed by the inheritance rule; those parts can be matched later if desired.
