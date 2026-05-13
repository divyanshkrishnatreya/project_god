# Page Production Cycle - Leela.exe

## Purpose
This is the canonical workflow for producing one manga page inside the persistent Leela.exe universe.

## Cycle
1. Read chapter memory.
2. Read series memory.
3. Read relevant character, style, and lore files.
4. Read the latest approved page review.
5. Determine remaining chapter page budget.
6. Generate panel breakdown.
7. Generate final page blueprint and prompt.
8. Create or receive image output.
9. Analyze continuity.
10. Update chapter memory and references.
11. Only then proceed to the next page.

## Hard Rule
No page should be generated as if it exists alone. Every page must inherit from the last approved state and push the chapter toward a full page-10 resolution.

## Required Inputs
- `continuity/chapter_memory.md`
- `continuity/series_memory.md`
- relevant `characters/` files
- relevant `style/` files
- relevant `lore/` files
- latest page review or approved image notes

## Required Outputs
- page objective
- panel breakdown
- emotional direction
- continuity safeguards
- final image-generation prompt

## Completion Gate
The cycle is not complete until memory is updated.
