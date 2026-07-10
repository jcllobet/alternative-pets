# White Kitsune look mechanics

## Natural motion

White Kitsune is a soft, grounded guardian fox with a separate head and body. The eyes lead each gaze change; the muzzle, forehead markings, head, ears, and upper chest follow as one coherent anatomical turn. The lower torso and all four paws remain planted on one baseline. The single tail stays attached at the same hip, trails the head turn by a very small amount, and must never split, duplicate, fan out, detach, or resemble multiple tails.

Each 22.5-degree step uses an even motion budget: small eye and eyelid movement first, then a restrained head turn or pitch, then slight ear and chest-fur follow-through. Body scale, head scale, foot placement, tail volume, and silhouette stay stable. Do not rotate or tilt the whole sprite.

## Cardinal pose families

- `000 up`: face remains broadly frontal; pupils and muzzle angle lift; eyelids open slightly; ears angle upward. Both body sides remain equally visible.
- `090 screen-right`: head and muzzle turn unmistakably toward the viewer's right; the nearer right-facing cheek and ear become more prominent while the far side narrows slightly. The attached tail lags subtly without changing sides.
- `180 down`: face remains broadly frontal; pupils, muzzle, and chin lower; upper eyelids lower slightly and ears relax outward. Both body sides remain equally visible.
- `270 screen-left`: exact anatomical counterpart of the right-facing family, turned unmistakably toward the viewer's left; the left-facing cheek and ear become more prominent while the far side narrows slightly. The attached tail lags subtly without changing sides.

Diagonals interpolate those families smoothly. Pupils remain inside the original indigo eye apertures; do not add eye whites, floating pupils, or a second eye layer.

## Identity and palette lock

Every direction has exactly one attached curled tail. Preserve the symmetric vermilion facial and leg markings, fluffy chest, indigo linework, and the exact authoritative flat colors from `qa/palette-lock.md`: fur white `#FDFDFC`, vermilion `#F72A4F`, deep indigo `#050C67`, and shadow `#DCCAD8`. Only tiny antialias edge blends may vary.
