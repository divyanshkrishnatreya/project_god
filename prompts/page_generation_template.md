# Page Generation Template - Leela.exe

## Purpose
Use this template whenever generating the next page of the manga. The assistant must behave like a production director, not only a prompt writer.

## Pre-Generation Checklist
Read, in this order:
1. `continuity/chapter_memory.md`
2. relevant files in `characters/`
3. relevant files in `style/`
4. relevant files in `lore/`
5. any page-specific correction notes from the latest approved image

## Required Analysis Before Output
- identify the current page number
- identify how many pages remain in the chapter
- confirm the last approved page beat
- identify what must carry forward visually
- identify what cannot change
- identify whether the chapter needs breathing room or escalation
- identify whether the next page is in Vaikuntha admin-space, mythic timeline, or montage mode
- identify what must still happen before page 10 for the avatar arc to conclude

## Output Format
Use the following structure each time:

### 1. Page Objective
One concise paragraph defining what this page must accomplish in story terms.

### 2. Panel Breakdown
List each panel in order with:
- shot type
- subject
- action
- emotional beat
- key visual continuity detail

### 3. Emotional Direction
Summarize how the page should feel from first panel to last panel.

### 4. Continuity Safeguards
Bullet the details that must remain consistent with prior pages, including:
- costume
- injuries or wetness
- weather
- prop placement
- revealed knowledge
- scale of Matsya
- current trust level between characters
- whether modern interface imagery is allowed in the scene

### 5. Final AI Image-Generation Prompt
Write one polished prompt that includes:
- page number
- manga style and art direction
- panel composition
- character appearances
- emotional tone
- environment and lighting
- continuity safeguards embedded naturally
- negative prompt guidance if useful

## Prompt Quality Rules
1. Keep prompts cinematic and visual, not lore-dumpy.
2. Prefer concrete imagery over abstract adjectives.
3. Preserve the same facial design, costume, and atmosphere across consecutive pages.
4. Mention exact time-of-day and weather carry-over when known.
5. Track Matsya's scale precisely.
6. If the scene is in the mortal world, do not casually inject modern UI motifs.
7. Make sure the page meaningfully advances the chapter toward a complete ending by page 10.

## After Image Review Workflow
When a page image is provided:
1. compare it to the intended page objective
2. detect style drift and continuity problems
3. propose precise corrections
4. update `continuity/chapter_memory.md`
5. update character or style files if a new detail becomes canon

## Quick Continuity Prompt Add-On
Append this kind of reminder to final prompts when needed:

"Maintain continuity with previous approved pages: same facial design, same clothing folds and accessories, same weather progression, same emotional state escalation, same water behavior and lighting logic."
