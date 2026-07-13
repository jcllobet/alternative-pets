# Alternative Pets

Codex-compatible v2 pets with nine standard animation rows and 16 clockwise look directions.

## White Kitsune

A white-and-vermilion guardian fox companion.

![White Kitsune direction preview](white-kitsune/qa/look-directions.png)

```bash
mkdir -p ~/.codex/pets/white-kitsune
cp white-kitsune/pet.json white-kitsune/spritesheet.webp ~/.codex/pets/white-kitsune/
```

## Twilight Cleric

A gentle chibi light cleric with a scale-stable hover animation. Its idle and all five hover frames use the same `198px` practical height and `5..203` registration.

![Twilight Cleric direction preview](twilight-cleric/qa/look-directions.png)

```bash
mkdir -p ~/.codex/pets/twilight-cleric-stable
cp twilight-cleric/pet.json twilight-cleric/spritesheet.webp ~/.codex/pets/twilight-cleric-stable/
```

Each pet directory contains the installable `pet.json` and lossless `1536x2288` v2 `spritesheet.webp`, plus atlas metadata and deterministic QA evidence. Both packaged atlases pass strict v2 validation with no errors or warnings.
