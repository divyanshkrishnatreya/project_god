# Reference Index - Leela.exe

## Purpose
This folder stores visual and thematic references that help preserve design continuity across the manga.

Use this folder primarily as the metadata registry for references.
Raw visual files can also be organized under `assets/references/` for cleaner automation later.

This index also acts as the first gate for future LoRA datasets. An image that is not registered here as approved canon should not be used for training.

## Current Registered Reference
### Approved / Active Baseline
- `../assets/approved/pages/chapter_01_page_01.png`
  - role: current page 1 continuity baseline
  - importance: high
  - use for: Vishnu design, Vaikuntha admin-space tone, caption treatment, Matsya recap grandeur
  - original upload source: `../seed_reference.png`

## Recommended Reference Categories
Add future materials under these buckets:

### Character Model References
- Vishnu turnarounds
- Matsya scale studies
- Manu costume consistency sheets

### Environment References
- Vaikuntha interior mood
- riverbank ritual spaces
- flood ocean and storm sky studies

### Motif References
- lotus geometry
- ripple patterns
- sacred light behavior
- parchment caption styling

### Negative References
Examples of looks to avoid:
- glossy sci-fi control rooms for mortal scenes
- generic fantasy armor overload
- neon interface effects outside Vaikuntha
- horror-fish anatomy for Matsya

### Future LoRA Candidate References
Use this bucket when an approved asset may become training data.

Required notes:
- subject or style target
- source approved asset path
- canon status
- useful crop or panel range
- caption status
- likely dataset bucket
- known drift risks

Example dataset buckets:
- `characters/vishnu`
- `characters/matsya`
- `characters/manu`
- `style/leela_mythic_manga`
- `environments/vaikuntha_admin`
- `environments/pralaya_flood`
- `motifs/lotus_geometry`

### QLoRA Text Example Sources
Use reviews, page packets, prompt files, and memory updates as future text fine-tuning examples only after their format has stabilized.

Good candidate sources:
- approved page reviews
- page generation packets
- final prompts
- chapter memory updates
- animation notes

Do not treat raw brainstorming notes as QLoRA examples unless they are cleaned into a clear instruction, input, and output format.

## Reference Intake Rule
Whenever a new image is uploaded and approved:
1. identify what canon it locks
2. register it here
3. note which designs or moods it should control
4. add LoRA-readiness notes if it may become training data
5. if appropriate, place the raw file in the relevant `assets/references/` subfolder
