# Kitsune Pets

Two Codex-compatible v2 fox companions, each with nine standard animation rows and 16 clockwise look directions.

| Pet | Preview | Style |
| --- | --- | --- |
| [Kitsune](kitsune/) | ![Kitsune direction preview](kitsune/qa/look-directions.png) | Polished pixel-art fox spirit |
| [White Kitsune](white-kitsune/) | ![White Kitsune direction preview](white-kitsune/qa/look-directions.png) | White-and-vermilion guardian fox |

Each pet folder contains its `pet.json`, lossless `1536x2288` v2 `spritesheet.webp`, atlas metadata, generation request, deterministic validation, direction QA evidence, and motion previews. White Kitsune also includes its fixed fur/vermilion palette contract and measured consistency reports.

## Install

```bash
mkdir -p ~/.codex/pets/kitsune ~/.codex/pets/white-kitsune
cp kitsune/pet.json kitsune/spritesheet.webp ~/.codex/pets/kitsune/
cp white-kitsune/pet.json white-kitsune/spritesheet.webp ~/.codex/pets/white-kitsune/
```

Both packaged atlases pass strict v2 validation with no errors or warnings.
