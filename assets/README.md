# Assets Guide - Leela.exe

## Purpose
This folder separates image assets from canon and workflow documents.

## Structure
- `assets/incoming/pages/`
  - raw generated pages awaiting review
- `assets/approved/pages/`
  - approved page images that are part of active continuity
- `assets/references/characters/`
  - master model sheets and recurring identity references
- `assets/references/environments/`
  - recurring location references
- `assets/references/style/`
  - style-locked visual references
- `assets/references/motifs/`
  - ripple, lotus, sacred light, iconography references
- `assets/rejected/`
  - optional storage for discarded outputs if needed

## Current Note
The current page 1 baseline has now been normalized into `assets/approved/pages/chapter_01_page_01.png`.

The original uploaded source still exists at the project root as `seed_reference.png`, but the approved asset path above should be treated as canonical for continuity and production references.

## Intake Rule
1. generate or receive asset
2. place in `incoming`
3. analyze continuity
4. approve or reject
5. move or register accordingly

## AI/ML Training Rule
`assets/` is not the training dataset.

Approved assets may become LoRA candidates only after they are:
1. registered in `references/reference_index.md`
2. captioned
3. tagged by subject, environment, motif, and style
4. linked to an approval review
5. copied into a future `datasets/` training split

Never train from `assets/incoming/` or unreviewed generations.
