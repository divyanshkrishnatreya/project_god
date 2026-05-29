# Leela.exe Production System

## Project Identity
Leela.exe is a long-form mythology-based manga and future anime pipeline built around one rule above all others: every page belongs to a persistent cinematic universe.

The project is also being prepared as an AI/ML production system where approved pages, continuity reviews, prompts, and memory updates become future training material for LoRA, QLoRA, evaluation, and automation.

The story premise is fixed:
- the universe is a sacred simulation engine
- child Vishnu maintains it from Vaikuntha
- each Dashavatar is an intervention protocol when Dharma destabilizes

## Production Priorities
1. continuity first
2. lore consistency
3. recurring visual identity
4. emotional coherence
5. chapter-level pacing
6. modular long-term scalability
7. automation readiness
8. AI/ML dataset and model lineage

## Series Format
- total chapters: 10
- one avatar per chapter
- each chapter length: 10 pages
- each chapter must complete its avatar storyline inside those 10 pages

## Core Working Layers
### Canon Layer
- `lore/`
- `characters/`
- `style/`

### Runtime Memory Layer
- `continuity/series_memory.md`
- `continuity/chapter_memory.md`
- `continuity/memory_architecture.md`

### Chapter Production Layer
- `chapters/`
- `prompts/`
- `templates/`
- `workflows/`

### Automation Layer
- `automation/pipeline_manifest.yaml`
- `automation/command_registry.yaml`
- `automation/runtime_state_template.yaml`
- `automation/schemas/`

### AI/ML Engineering Layer
- `docs/ai_ml_engineering_strategy.md`
- `templates/dataset_manifest_template.yaml`
- `templates/model_card_template.md`
- future `datasets/`
- future model registry and adapter cards
- LoRA, QLoRA, evaluation, and ComfyUI integration planning

### QA Layer
- `qa/`
- chapter `reviews/` folders

### Asset Layer
- `assets/incoming/`
- `assets/approved/`
- `assets/references/`
- `exports/`

## Key Commands / Workflows
The system is now designed around reusable operations:
- `generate_next_page`
- `analyze_continuity`
- `update_chapter_memory`
- `generate_panel_breakdown`
- `generate_animation_notes`

See `workflows/` and `automation/command_registry.yaml` for the canonical definitions.

## Current Canon State
- active chapter: 1
- active avatar: Matsya
- page 1 baseline image is already registered in continuity memory

## AI/ML Direction
LoRA is the visual consistency path for characters, style, environments, and sacred motifs.

QLoRA is the language/automation path for continuity review, prompt compilation, memory updates, and animation notes.

The project should not train adapters from unreviewed or one-off assets. Approved pages must first become traceable reference packs with captions, metadata, and evaluation prompts.

## Recommended Working Loop
1. read canon and memory
2. generate next page blueprint
3. generate final page prompt
4. review resulting page for continuity drift
5. update chapter memory and reference index
6. repeat until page 10 resolves the chapter

## Primary Orientation Files
- [learn.md](learn.md)
- [docs/production_foundation.md](docs/production_foundation.md)
- [docs/ai_ml_engineering_strategy.md](docs/ai_ml_engineering_strategy.md)
- [docs/future_roadmap.md](docs/future_roadmap.md)
- [continuity/memory_architecture.md](continuity/memory_architecture.md)
- [automation/pipeline_manifest.yaml](automation/pipeline_manifest.yaml)
- [workflows/page_production_cycle.md](workflows/page_production_cycle.md)
