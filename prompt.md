# Consistent Codex Pet Prompt

Use this copy-and-paste prompt with Codex to create a high-consistency animated pet. Fill in every bracketed field before starting. The workflow and packaging requirements come from the [OpenAI Hatch Pet skill](https://github.com/openai/skills/tree/main/skills/.curated/hatch-pet).

```text
Use the Hatch Pet skill to create a new Codex-compatible v2 animated pet.

PET BRIEF

- Name: [PET NAME]
- Concept: [ONE-SENTENCE ORIGINAL CHARACTER CONCEPT]
- Personality: [THREE TO FIVE TRAITS]
- Role beside the coder: [COMPANION, GUIDE, PROTECTOR, ETC.]
- Broad visual inspiration: [MOOD, ERA, CREATURE TYPE, OR GENRE]

ORIGINALITY AND RIGHTS

Create an original, rights-safe character. Broad genre, mythology, fashion, or mood inspiration is acceptable, but do not copy a protected character's distinctive silhouette, face, costume, markings, accessories, logos, names, or palette arrangement. Do not include brand marks or readable text.

CANONICAL IDENTITY LOCK

Create and approve one canonical base image before producing animation frames. Treat it as the single source of truth for every frame and direction.

The character must always have:

- Anatomy and proportions: [HEAD-TO-BODY RATIO, BODY SHAPE, LIMB LENGTH]
- Face: [EYE SHAPE/COLOR, NOSE, MOUTH, EXPRESSION]
- Hair, fur, or surface: [SHAPE, LENGTH, TEXTURE]
- Clothing or body markings: [EXACT DESCRIPTION AND PLACEMENT]
- Accessories or props: [EXACT COUNT, SIDE, ATTACHMENT, AND SHAPE]
- Appendages: [EXACT EAR, HORN, WING, OR TAIL COUNT]
- Silhouette: [DISTINCTIVE BUT ORIGINAL SHAPE]
- Baseline: [WHICH FEET/BODY PARTS REMAIN PLANTED]

Never add, remove, duplicate, detach, mirror to the wrong side, or redesign an identity feature between frames. Preserve the same face, proportions, costume, markings, materials, accessory count, and appendage count throughout.

PALETTE LOCK

Use these exact core colors in every frame:

- Primary: [HEX] — [MATERIAL/AREA]
- Secondary: [HEX] — [MATERIAL/AREA]
- Accent: [HEX] — [MATERIAL/AREA]
- Outline: [HEX] — [MATERIAL/AREA]
- Shadow: [HEX] — [MATERIAL/AREA]

Only tiny antialiasing blends may vary. Do not hue-shift, desaturate, brighten, or darken the core colors between frames. Produce a palette report that checks the final atlas against these locked values.

STYLE CONTRACT

- Visual style: [EXAMPLE: CRISP FLAT-VECTOR CHIBI STICKER]
- Line treatment: [EXAMPLE: CLEAN, UNIFORM DARK OUTLINE]
- Shading: [EXAMPLE: MINIMAL TWO-TONE CEL SHADING]
- Camera: fixed orthographic/front presentation; no perspective or camera zoom
- Background during generation: one clean chroma color absent from the character
- Final frame background: transparent
- Do not render shadows, glows, particles, scenery, text, guide marks, detached decorations, or crop marks.

V2 ATLAS GEOMETRY

Build the final lossless WebP spritesheet as exactly 8 columns by 11 rows:

- Cell size: 192 x 208 px
- Atlas size: 1536 x 2288 px
- spriteVersionNumber: 2
- Keep the character fully inside every cell with consistent registration and baseline.

STANDARD ANIMATION ROWS

Create one coherent strip per state. Every strip must be grounded by the approved canonical base image and a deterministic layout guide.

1. Idle: 6 frames
2. Running right: 8 frames
3. Running left: 8 frames
4. Waving: 4 frames
5. Jumping or hover: 5 frames
6. Failed: 8 frames
7. Waiting: 6 frames
8. Running: 6 frames
9. Review: 6 frames

Fill unused cells according to the Hatch Pet v2 packaging rules. Do not stop at an 8 x 9 atlas: the two look-direction rows are required.

MOTION AND SCALE CONSISTENCY

After idle is approved, measure its practical visible top, bottom, height, horizontal center, and grounded baseline. Record those values as the scale contract.

For a fixed-size hover or jump interaction, every frame in that row must match the canonical practical height and registration. Do not shrink, zoom, miniaturize, crouch, squash the whole body, or translate the character upward. Convey motion through gaze, head turn, expression, ears, hair, clothing, tail, hands, or another small identity-safe gesture while maintaining the same overall proportions and footprint.

Keep animation motion subtle and readable at pet scale. Adjacent frames should change gradually, loop cleanly, and never appear to morph into a different drawing.

LOOK DIRECTIONS

Create all 16 clockwise directions in these exact atlas cells:

- Row 10: 000, 022.5, 045, 067.5, 090, 112.5, 135, 157.5 degrees
- Row 11: 180, 202.5, 225, 247.5, 270, 292.5, 315, 337.5 degrees

Use viewer/screen coordinates. Make the four cardinal anchors unmistakable before generating the intermediate directions:

- 000: looking up
- 090: looking right
- 180: looking down
- 270: looking left

Eyes lead the direction, then the muzzle/face and head, then ears/hair and upper body follow subtly. Keep the lower torso and planted feet anchored. Use an even visual motion budget for every 22.5-degree step. Do not rotate, tilt, or spin the entire sprite. Do not mirror asymmetric markings, accessories, or props onto the wrong side.

CONSISTENCY PROCESS

1. Present the canonical base and written identity/palette/scale contracts for approval.
2. Generate cardinal look anchors and validate their semantic directions.
3. Generate intermediate looks from adjacent approved anchors.
4. Generate one animation row at a time from the canonical base and approved neighboring frames.
5. Normalize transparency, cell alignment, baseline, palette, and scale deterministically during assembly.
6. Assemble the atlas only after every source strip passes frame-level review.

QA AND HANDOFF

Before installing or delivering the pet:

- Run strict v2 atlas validation and report zero errors and zero warnings.
- Verify atlas dimensions, cell dimensions, row counts, frame counts, transparency, and spriteVersionNumber 2.
- Produce contact sheets for all animation rows and the 16 look directions.
- Produce looping GIF or video previews for animation QA.
- Run blind cardinal-direction QA and clockwise continuity QA.
- Compare every frame with the canonical identity lock and palette lock.
- Report practical visible bounds for idle and hover/jump frames.
- Confirm there is no scale drift, baseline drift, clipping, whole-sprite rotation, detached feature, or accidental duplicate appendage.
- Package the installable pet.json and spritesheet.webp with reproducible metadata and QA evidence.

Do not install or present the pet as complete if any frame changes identity, core palette, proportions, practical scale, baseline, frame count, cardinal meaning, transparency, or required geometry. Repair the affected frames and rerun QA first.

When finished, give me the pet folder's absolute path and a concise validation summary.
```

The most important inputs are a precise identity lock, exact palette hex values, and a clear decision about whether the hover/jump row must preserve the idle frame's visible size. Ambiguous inputs in those three areas are the most common source of inconsistent pets.
