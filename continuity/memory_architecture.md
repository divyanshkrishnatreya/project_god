# Memory Architecture - Leela.exe

## Purpose
This file defines how memory is stored, updated, inherited, and verified across the project.

## Core Rule
Memory is not one file. It is a layered system with inheritance.

Higher layers define what is allowed.
Lower layers define what is currently happening.

## Memory Layers
### Layer 1 - Canon Bible
Files:
- `lore/universe_rules.md`
- `lore/avatar_system.md`
- `lore/dharma_engine.md`
- `characters/*.md`
- `style/*.md`

Function:
- defines what is universally true
- changes rarely
- highest narrative stability after explicit user decisions

### Layer 2 - Series Memory
Files:
- `continuity/series_memory.md`
- future series-level arc trackers

Function:
- remembers the Dashavatar roadmap
- tracks which chapter is active
- records cross-chapter motifs and continuity anchors

### Layer 3 - Chapter Memory
Files:
- `continuity/chapter_memory.md`
- chapter-level plans inside `chapters/chapter_xx_*/`

Function:
- tracks the currently active chapter in production
- records the local emotional arc
- tracks remaining pages and resolution requirements

### Layer 4 - Page Memory
Files:
- page blueprints
- page reviews
- prompt drafts
- approved page notes

Preferred location:
- `chapters/chapter_xx_*/pages/`
- `chapters/chapter_xx_*/reviews/`
- `chapters/chapter_xx_*/prompts/`

Function:
- stores what a specific page tried to do
- stores what the final approved page actually locked
- hands forward exact continuity details to the next page

### Layer 5 - Automation State
Files:
- `automation/pipeline_manifest.yaml`
- `automation/command_registry.yaml`
- `automation/runtime_state_template.yaml`
- `automation/schemas/`

Function:
- makes the system legible to future scripts and tools
- defines how automation should discover memory

## Read Order Before Creating Anything New
1. user's latest instruction
2. `continuity/chapter_memory.md`
3. `continuity/series_memory.md`
4. relevant character files
5. relevant style files
6. relevant lore files
7. latest page review or approved asset notes

## Update Order After Approving A Page
1. page review file
2. chapter page log
3. chapter carry-forward tracker
4. reference index if new canon visuals are locked
5. series memory only if a cross-chapter truth changed

## What Counts As Locked Memory
- an approved final page image
- a user-approved retcon
- a deliberate character design update
- a fixed chapter pacing change
- a confirmed naming or mythology decision

## What Does Not Count As Locked Memory
- abandoned prompt drafts
- speculative ideas
- unapproved regeneration attempts
- exploratory variations

## Memory Inheritance Rules
1. Chapter memory inherits from series memory and canon.
2. Page memory inherits from chapter memory.
3. Automation state must not overwrite canon directly.
4. If a lower-layer file conflicts with a higher-layer file, the conflict must be resolved, not ignored.

## Drift Prevention Rules
Always track:
- facial structure
- hair shape
- costume logic
- revealed knowledge
- weather and lighting continuity
- emotional escalation
- motif recurrence
- remaining pages until chapter closure

## Scalability Rules
1. Use stable file names and chapter identifiers.
2. Keep memory summaries short enough to scan quickly.
3. Store deep analysis in page review files rather than bloating series memory.
4. Reserve series memory for truths that matter beyond one page.
