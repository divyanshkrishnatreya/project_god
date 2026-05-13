# Production Foundation - Leela.exe

## Purpose
This document defines the optimal long-term project foundation for Leela.exe as a continuity-heavy manga and future anime pipeline.

The goal is not to store random prompts. The goal is to build a stable production system that can scale from page generation to semi-automation to animation preparation.

## Foundation Principles
1. Canon must be layered, not scattered.
2. Every new asset must either reinforce continuity or be explicitly rejected.
3. Each chapter must be self-contained while still belonging to the same universe.
4. Human-readable memory and machine-readable manifests must coexist.
5. Future automation should be able to discover what to read, what to generate, and what to update without guessing.

## Recommended Folder Architecture
```text
/project-root
  README.md
  /docs
  /lore
  /characters
  /style
  /continuity
  /chapters
    /chapter_01_matsya
      /pages
      /prompts
      /reviews
      /memory
      /assets
      /exports
    /chapter_02_kurma
    ...
  /prompts
  /templates
  /workflows
  /automation
    /schemas
  /references
  /assets
    /incoming
    /approved
    /references
    /rejected
  /qa
  /animation_notes
  /exports
```

## Why This Structure Works
### `lore/`, `characters/`, `style/`
These act as the stable canon base. They should change rarely and only when the universe itself becomes clearer.

### `continuity/`
This is the runtime memory layer. It stores what is currently true in the series and what is currently true in the active chapter.

### `chapters/`
Each chapter is both a narrative unit and a production unit. It needs local folders because every chapter will eventually gather:
- page images
- revision notes
- panel prompts
- continuity reviews
- animation prep notes

### `templates/`
Templates prevent drift in how memory is recorded. They are essential for long-term consistency and later scripting.

### `workflows/`
These files define how the assistant should behave when asked to perform recurring tasks.

### `automation/`
This is the machine-readable layer for future tools, scripts, ComfyUI pipelines, and assistant orchestration.

### `qa/`
Continuity and mythology review need their own permanent place. QA is part of creation, not something added at the end.

### `assets/` and `exports/`
Raw images, approved baselines, and final deliverables should be separated from canon docs and runtime memory.

## Memory Architecture
Leela.exe uses a five-layer memory system:

### Layer 1 - Immutable Canon
- universe rules
- avatar logic
- Dharma/Karma/Yuga system
- core character identity
- art direction

### Layer 2 - Series Memory
- chapter roadmap
- active chapter
- cross-chapter motifs
- long-term continuity anchors

### Layer 3 - Chapter Memory
- page status
- local emotional arc
- current weather, props, knowledge, injuries
- remaining page budget

### Layer 4 - Page Packet
- page objective
- panel plan
- visual constraints
- approved image review
- carry-forward notes

### Layer 5 - Asset / QA Memory
- reference image index
- approved vs rejected assets
- style drift reports
- mythology integrity checks

## Production Modes
### Mode A - Story Development
Used when designing chapter beats, pacing, and story arcs.

### Mode B - Page Production
Used when generating the next page blueprint and prompt.

### Mode C - Review And Continuity
Used when a generated page image is uploaded and must be checked before proceeding.

### Mode D - Automation Prep
Used when translating the current workflow into templates, schemas, manifests, or future tools.

### Mode E - Animation Adaptation
Used when converting completed manga pages into shot-by-shot motion logic.

## Long-Term Pipeline Vision
### Phase 1 - Manual Assisted Manga Production
- markdown memory
- page prompts
- continuity review

### Phase 2 - Semi-Automated Generation Loop
- previous page read
- continuity analysis
- prompt refinement
- next page generation

### Phase 3 - Reference-Locked Visual Identity
- master model sheets
- character LoRAs
- style LoRAs

### Phase 4 - ComfyUI / Tool Integration
- prompt templates mapped to graph inputs
- continuity metadata passed into generation nodes
- chapter state driving automated page prep

### Phase 5 - Animation Extension
- page-to-shot conversion
- shot continuity packs
- video generation prep
- trailer and episode assembly logic

## Operational Rules
1. Never generate a page without first reading current memory.
2. Never approve a page without logging what it locks.
3. Never let a chapter run out of pages before its avatar arc is resolvable.
4. Never allow modern simulation visuals to contaminate mortal-world scenes unless intentionally framed.
5. Never treat reference intake as casual. Every approved image changes the project state.

## What Makes The System Automation-Ready
1. Stable folder naming
2. stable chapter naming
3. command definitions with declared inputs and outputs
4. machine-readable manifests
5. repeatable templates
6. consistent memory update order
7. clear QA gates

## Immediate Best Practice
For every newly approved page in Chapter 1:
1. store or register the image
2. run `analyze_continuity`
3. update page-level notes
4. update `continuity/chapter_memory.md`
5. update `references/reference_index.md` if new visual canon is locked
6. only then generate the next page
