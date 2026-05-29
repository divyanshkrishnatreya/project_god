# AI/ML Engineering Strategy - Leela.exe

## Purpose
This document defines the model, dataset, and evaluation strategy for turning Leela.exe from a prompt-driven manga workflow into an AI/ML-ready production system.

The priority is not to train models early. The priority is to make every approved page, review, and memory update useful for future LoRA, QLoRA, evaluation, and automation work.

## Core Position
Leela.exe should treat AI/ML as a continuity amplifier.

The models must serve the canon:
1. visual identity stays stable
2. mythology tone stays sacred
3. chapter pacing remains readable
4. every generated asset has lineage
5. every trained adapter has a narrow job

## Model Roles
### Image Generation Base Model
The base image model provides broad visual capability: anatomy, lighting, environments, composition, and painterly manga rendering.

The base model is not expected to remember Leela.exe canon by itself.

### LoRA
LoRA is the visual identity layer.

Use LoRA adapters for:
- recurring characters
- recurring avatar forms
- house art style
- important environments
- sacred motifs and visual language

LoRAs should be small, versioned, and task-specific. A Vishnu LoRA should not also try to learn Matsya, Vaikuntha, page layout, and caption styling at the same time.

### QLoRA
QLoRA is the language and reasoning adaptation layer.

Use QLoRA for fine-tuning a language model or multimodal assistant on project-specific behavior:
- continuity review
- chapter memory updates
- prompt packet generation
- lore-safe rewriting
- page-to-shot adaptation
- structured output generation

QLoRA should not be treated as the primary method for locking image style. It is best used to teach the assistant how to think and write like the production system.

### Retrieval And Memory
Not every project behavior needs fine-tuning.

Use retrieval over project files for:
- active canon facts
- current chapter state
- latest page status
- approved reference registry
- changing roadmap details

Use QLoRA only after the workflow has produced enough strong examples to justify training.

## LoRA Tracks
### Character LoRAs
Target subjects:
- child Vishnu
- Matsya
- Manu
- later avatar forms

Purpose:
- preserve face, silhouette, costume, expression range, and recurring symbolic details
- reduce visual drift across pages and chapters

Dataset requirements:
- only approved canon images
- multiple expressions, angles, lighting conditions, and compositions
- clean captions with subject token, identity traits, costume details, and scene variables
- rejected examples recorded separately for evaluation and negative guidance

Suggested trigger tokens:
- `leela_vishnu_child`
- `leela_matsya`
- `leela_manu`
- `leela_kurma`
- `leela_narasimha`

### Style LoRA
Purpose:
- preserve the painted manga/anime tone
- stabilize line weight, sacred lighting, panel atmosphere, caption treatment, and cinematic scale

Dataset requirements:
- finished approved pages
- cropped panels when useful
- captions that separate subject identity from house style
- no low-quality or continuity-failed pages

Suggested trigger token:
- `leela_mythic_manga_style`

### Environment LoRAs
Target environments:
- Vaikuntha admin space
- riverbank ritual space
- flood ocean
- cosmic preservation scenes

Purpose:
- make recurring spaces feel like the same world
- prevent generic fantasy or glossy sci-fi drift

Suggested trigger tokens:
- `leela_vaikuntha_admin`
- `leela_sacred_riverbank`
- `leela_pralaya_flood`

### Motif LoRAs Or Embeddings
Target motifs:
- lotus geometry
- sacred blue light
- ripple patterns
- Dharma interface marks
- divine water language

Purpose:
- provide reusable symbolic texture without overpowering characters or scenes

These may start as prompt conventions, reference images, embeddings, or ComfyUI reference adapters before becoming LoRAs.

## Dataset Architecture
Future training data should be organized separately from production assets.

```text
/datasets
  /images
    /characters
      /vishnu
        /v001
          /source
          /prepared
          /captions
          metadata.yaml
      /matsya
      /manu
    /style
    /environments
    /motifs
  /text
    /continuity_reviews
    /page_packets
    /chapter_memory_updates
    /prompt_compiler_examples
  /evals
    /visual_identity
    /prompt_quality
    /continuity_reasoning
```

Do not train directly from `assets/incoming/`. Incoming assets must pass review before they can enter a dataset.

## Dataset Metadata
Every dataset item should be traceable.

Use `templates/dataset_manifest_template.yaml` when creating a new LoRA or QLoRA dataset.

Minimum metadata fields:
- `asset_id`
- `source_path`
- `canon_status`
- `chapter_id`
- `page_number`
- `subject_tags`
- `style_tags`
- `caption_path`
- `approval_review_path`
- `dataset_split`
- `license_or_origin`
- `notes`

The most important rule: if an engineer cannot trace an image back to canon approval, it should not enter training.

## Captioning Standard
Captions should describe what the model must learn and what should remain variable.

Good caption traits:
- starts with the trigger token
- identifies the subject clearly
- names stable costume and symbolic features
- includes pose, expression, camera angle, and environment
- avoids stuffing unrelated lore into visual captions

Example structure:
```text
leela_vishnu_child, child Vishnu in sacred blue-gold attire, calm knowing expression, seated in Vaikuntha admin space, lotus geometry, soft divine light, cinematic manga panel
```

For style datasets, keep character names out unless the character is visually central. The style adapter should learn the look, not memorize one subject.

## LoRA Training Workflow
1. Collect approved source assets.
2. Create prepared crops and panel extracts.
3. Write or review captions.
4. Split into train and eval sets.
5. Train the narrowest useful adapter.
6. Run fixed evaluation prompts.
7. Compare outputs against canon references.
8. Record model card, dataset version, base model, training config, and known limits.
9. Use the adapter in production only after it passes review.

## Visual Evaluation Gates
A LoRA is not production-ready until it passes these gates:
1. identity remains stable across camera angles
2. costume and symbolic details do not mutate randomly
3. the adapter composes with other project LoRAs
4. sacred tone survives action, emotion, and scale changes
5. negative prompts can suppress known drift
6. output is useful at more than one strength setting

Recommended eval prompt categories:
- neutral model sheet
- emotional close-up
- wide cinematic environment
- action beat
- quiet devotional beat
- panel composition with captions
- cross-character scene

## QLoRA Training Tracks
### Continuity Reviewer
Goal:
Teach a language model to produce project-specific review reports.

Training examples:
- input: page packet, previous memory, generated page description
- output: continuity flags, drift risks, approval recommendation, required memory updates

### Prompt Compiler
Goal:
Teach a model to turn chapter state into final image prompts.

Training examples:
- input: canon, chapter memory, page objective, panel breakdown
- output: structured final generation prompt with continuity safeguards

### Memory Updater
Goal:
Teach a model to update memory without losing page-state details.

Training examples:
- input: approved review and page summary
- output: updated chapter memory fragment and carry-forward notes

### Animation Adapter
Goal:
Teach a model to convert finished pages into shot logic.

Training examples:
- input: page blueprint, final page description, cinematic language rules
- output: shot list, camera movement, motion emphasis, transition notes

## Text Dataset Format
Use structured JSONL for QLoRA-ready examples.

```jsonl
{"task":"continuity_review","instruction":"Review the page for continuity drift.","input":{"canon_refs":["continuity/chapter_memory.md","style/art_direction.md"],"page_summary":"..."},"output":{"approval":"conditional","flags":["..."],"memory_updates":["..."]}}
```

Keep examples compact, consistent, and strongly typed. The goal is to teach repeatable behavior, not store the whole project in every row.

## QLoRA Evaluation Gates
A QLoRA-tuned model is not production-ready until it can:
1. follow the repository's output formats
2. preserve canon facts without inventing new ones
3. identify missing inputs instead of guessing
4. distinguish visual review from lore review
5. produce memory updates that are concise and actionable
6. keep the sacred simulation tone intact

## Model Registry
Every trained model or adapter should have a model card.

Use `templates/model_card_template.md` for LoRA, QLoRA, and other adapter records.

Recommended naming:
- `lora_vishnu_sdxl_v001`
- `lora_matsya_sdxl_v001`
- `lora_leela_style_sdxl_v001`
- `qlora_continuity_reviewer_v001`
- `qlora_prompt_compiler_v001`

Minimum model card fields:
- model name
- purpose
- base model
- dataset version
- training date
- training config path
- trigger tokens
- recommended strength range
- evaluation prompts
- pass/fail notes
- known failure modes
- production status

## ComfyUI Integration Target
The future ComfyUI graph should accept structured inputs from the project state.

Useful graph inputs:
- base checkpoint
- page prompt
- negative prompt
- character LoRA names and strengths
- style LoRA name and strength
- environment LoRA name and strength
- reference image paths
- seed
- aspect ratio
- output path
- page metadata

The production system should eventually generate these inputs from `automation/runtime_state.yaml`, chapter memory, and the page packet.

## Immediate AI/ML Sprint
The project is not ready to train LoRAs from one page. The correct next move is dataset readiness.

1. Treat Chapter 1 Page 1 as a seed reference, not a training dataset.
2. Continue producing approved Chapter 1 pages with strict reviews.
3. Register every approved page in `references/reference_index.md`.
4. Start tagging approved assets by subject, environment, motif, and style.
5. Build a first Vishnu reference pack after several stable appearances.
6. Build a first Matsya reference pack after enough varied approved images exist.
7. Convert page reviews and memory updates into future QLoRA examples.
8. Train only after the project has enough accepted examples to evaluate against.

## Engineering Risks
### Overfitting
Training too early can make characters rigid or copy a single page composition.

Mitigation:
- wait for varied references
- use eval prompts
- keep adapters narrow

### Dataset Poisoning
Rejected images can silently teach the wrong identity.

Mitigation:
- never train from incoming assets
- keep rejected outputs out of training sets
- log approval review paths

### Style Contamination
Character LoRAs can accidentally absorb page style or environment details.

Mitigation:
- separate character, style, and environment datasets
- caption variable context clearly
- evaluate adapters in unfamiliar scenes

### Canon Drift
A model may produce appealing visuals that violate the project.

Mitigation:
- keep continuity review as a gate
- compare against memory before approval
- update model cards with failure cases

## Definition Of AI/ML Readiness
Leela.exe is ready for first serious LoRA experiments when:
1. there are multiple approved pages with stable recurring characters
2. references are registered with clear canon status
3. captions and metadata exist for training candidates
4. eval prompts are written before training starts
5. failures can be compared against known approved references

Leela.exe is ready for QLoRA experiments when:
1. there are repeated high-quality examples of reviews, prompts, and memory updates
2. task formats are stable
3. the desired assistant behavior is clearer than general instruction prompting can provide
4. evaluation cases can catch hallucination, tone drift, and format errors
