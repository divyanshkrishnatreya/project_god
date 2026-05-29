# Future Roadmap - Leela.exe

## Purpose
This document is the long-term execution roadmap for Leela.exe as a persistent manga, continuity, automation, and future animation universe.

It is not a vague ideas list. It is the active production direction for what should happen next and why.

## Guiding Principle
The project should now shift from "infrastructure expansion" to "infrastructure validation through real production."

The system is already strong enough to begin proving itself on actual chapter output.

## Current State
### Already Built
- core lore files
- character sheets
- style rules
- continuity rules
- chapter memory
- series memory
- workflow docs
- automation-ready manifests and schemas
- chapter folder scaffolding
- local Git repository with initial commit

### Current Active Chapter
- Chapter 1: Matsya
- total chapter length: 10 pages
- page 1 exists as current canon baseline
- pages 2 to 10 are still unproduced

### Current Strategic Truth
The next highest-value work is not more planning.
The next highest-value work is to run the system on real chapter production.

For AI/ML, the current strategic truth is similar: the project should not rush into training from one image. It should produce, approve, caption, and register enough high-quality examples to make LoRA and QLoRA experiments measurable.

## Main Roadmap
### Phase 1 - Production Validation
Goal:
Prove that the continuity and chapter system works under real page-by-page creation pressure.

Tasks:
1. Normalize Chapter 1 Page 1 fully into the new pipeline structure.
2. Generate Chapter 1 Page 2 using the formal workflow.
3. Review the output using the continuity workflow.
4. Update chapter memory cleanly.
5. Continue until Chapter 1 is fully completed.

Why this matters:
- it tests continuity memory in practice
- it exposes pacing problems early
- it creates the first true recurring visual baseline
- it gives real material for future character/style consistency systems

### Phase 2 - Chapter 1 Completion And Retrospective
Goal:
Finish Matsya as the pilot chapter and improve the system based on real friction.

Tasks:
1. complete all 10 pages of Chapter 1
2. write a chapter retrospective
3. identify weak points in memory updates, prompt quality, pacing, and drift detection
4. tighten templates and workflow docs based on observed issues

### Phase 3 - Visual Identity Lock
Goal:
Turn approved chapter material into stable reference packs and future LoRA candidates.

Tasks:
1. assemble recurring Vishnu references
2. assemble recurring Matsya references
3. assemble recurring Manu references
4. assemble Vaikuntha and river/flood environment references
5. assemble motif references for water, lotus geometry, sacred light, and caption style
6. tag approved assets by subject, environment, motif, style, and canon status
7. start draft captions for likely training candidates

Why this matters:
- future page consistency improves
- LoRA preparation becomes possible
- character drift gets easier to detect
- dataset lineage starts before training pressure arrives

### Phase 4 - Series Preproduction
Goal:
Prevent later chapters from becoming underplanned.

Tasks:
1. create preproduction packets for all remaining avatar chapters
2. define each chapter's thesis, emotional arc, visual mood, and ending state
3. identify recurring cross-chapter motifs and continuity bridges

### Phase 5 - Semi-Automation
Goal:
Turn the documented workflow into a repeatable assistant-driven loop.

Tasks:
1. formalize page packets in chapter folders
2. formalize review outputs
3. formalize runtime state updates
4. begin lightweight scripts or structured automation inputs
5. prepare continuity-aware prompt pipelines

### Phase 6 - LoRA And Visual Generation Stack
Goal:
Prepare for stronger visual locking across long-form production.

Tasks:
1. prepare character LoRA datasets for Vishnu, Matsya, Manu, and later avatars
2. prepare style LoRA dataset from approved pages and panels
3. prepare environment datasets for Vaikuntha, riverbank, flood ocean, and cosmic scenes
4. prepare motif datasets or embeddings for lotus geometry, sacred light, ripples, and Dharma interface marks
5. create fixed eval prompts before training starts
6. create model cards for every LoRA experiment
7. map prompt structures into ComfyUI-friendly input conventions

### Phase 7 - QLoRA And Assistant Specialization
Goal:
Adapt language-model behavior to the production system after enough examples exist.

Tasks:
1. collect continuity reviews into structured JSONL examples
2. collect page packets and final prompts into prompt compiler examples
3. collect approved memory updates into memory updater examples
4. collect animation notes into page-to-shot adaptation examples
5. train only against stable task formats
6. evaluate hallucination, tone drift, missing-input handling, and schema compliance

### Phase 8 - Animation Extension
Goal:
Convert completed manga production into anime-style scene development.

Tasks:
1. select strong pages for shot breakdowns
2. convert pages into animation notes
3. identify key motion moments
4. build trailer and short-sequence experiments

## Immediate Priority Order
1. normalize Chapter 1 Page 1 into the formal production structure
2. generate Chapter 1 Page 2
3. complete Chapter 1
4. build first reference pack
5. start AI/ML dataset tagging for approved assets
6. preproduce Chapters 2 to 10

## Immediate Sprint - What We Should Start Now
### Sprint Goal
Move the project from setup mode into active chapter production mode.

### Sprint Tasks
1. create canonical page 1 asset placement
2. create standardized page 1 review file inside chapter reviews
3. create a page 1 packet in chapter pages
4. update references and runtime metadata to point at the canonical page 1 asset
5. prepare for Page 2 generation

## Definition Of Success
The project is on track when:
1. each approved page updates memory cleanly
2. each page clearly advances the chapter toward page 10 closure
3. recurring character identity stays stable
4. chapter pacing remains cinematic and readable
5. the system becomes easier to use after every page, not harder
6. approved assets become traceable future training candidates
7. reviews and memory updates become reusable QLoRA examples

## Risks To Control
### Overplanning Risk
If we keep expanding docs without generating pages, the system will become elegant but unproven.

### Drift Risk
If pages are produced without rigorous review, the project will lose identity fast.

### Compression Risk
Because each avatar must resolve within 10 pages, pacing waste is dangerous.

### Mythology Tone Risk
If the simulation concept becomes too technical or casual, the sacred tone will weaken.

### Premature Training Risk
If LoRAs are trained before enough varied approved references exist, they may overfit one page and reduce creative range.

### Dataset Lineage Risk
If approved, rejected, incoming, and generated assets are mixed together, future models will learn drift as canon.

## Active Decision
Starting now, the project should prioritize:
- Chapter 1 production execution
- continuity-safe page generation
- reference stabilization
- AI/ML dataset readiness
- LoRA/QLoRA evaluation planning

Not more broad planning unless real production reveals a need for it.
