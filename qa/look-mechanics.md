# Kitsune look mechanics

Kitsune is a compact fox spirit with a separate head, large physical eyes, upright ears, a soft neck ruff, and a curled tail. The paws, hips, and lower torso stay anchored on one baseline. The whole sprite never rotates or slides.

The eyes lead each gaze by rotating as complete pixel-art eye surfaces with the existing dark eye shape and highlights preserved. The muzzle and nose follow through a small head pitch or yaw; the ears follow the head with slightly less motion. The ruff compresses subtly on the turned-to side, and the tail may lag by one small pixel-art step while remaining attached. There are no props.

Cardinal pose families:

- 000 up: pupils and muzzle lift, eyelids open upward, forehead and inner ears become more visible, chin and lower ruff become slightly occluded.
- 090 screen-right: nose and pupils move unmistakably to the right of the head center; the right-facing muzzle profile leads, the screen-left cheek and ear remain more visible, and the far cheek compresses.
- 180 down: pupils, muzzle, and head pitch downward; upper eyelids lower slightly, more crown and ear back is visible, and the ruff partly occludes the lower muzzle.
- 270 screen-left: nose and pupils move unmistakably to the left of the head center; the left-facing muzzle profile leads, the screen-right cheek and ear remain more visible, and the far cheek compresses.

Motion budget: every 22.5-degree step moves the eyes first, then the nose/head by a comparable small amount, with ears, ruff, and tail following continuously. Scale, foot placement, baseline, outline thickness, palette, and face proportions remain fixed. The 157.5 to 180 and 337.5 to 000 boundaries must each be exactly one visual step with no snap, flip, or recentering.
