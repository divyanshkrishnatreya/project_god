# Chapters Guide - Leela.exe

## Purpose
Each chapter folder is both a story container and a production container.

## Standard Chapter Folder Structure
Every `chapter_XX_avatar` folder should support:
- `pages/`
- `prompts/`
- `reviews/`
- `memory/`
- `assets/`
- `exports/`

## Recommended Use
### `pages/`
Store page blueprints, approved page notes, or page-level metadata.

### `prompts/`
Store final prompts or prompt revisions for that chapter.

### `reviews/`
Store continuity analyses and correction reports.

### `memory/`
Store chapter-local trackers if the chapter becomes complex enough to need more than the global chapter memory file.

### `assets/`
Store chapter-specific reference images or raw generation results.

### `exports/`
Store packaged chapter deliverables, if needed.

## Rule
The global chapter state still lives in `continuity/chapter_memory.md` unless deliberately expanded.
