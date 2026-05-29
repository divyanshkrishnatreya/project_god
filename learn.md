# AI/ML Interview Prep For Leela.exe

## How To Use This File
This file explains the core AI/ML ideas included in this project and the ideas the project is designed to include later.

Use it to prepare for interviews where you may need to explain:
1. what the project does
2. why LoRA and QLoRA matter
3. how datasets, evaluation, and model lineage work
4. how an AI/ML engineer thinks beyond just prompting
5. how this repository can grow into a real production AI pipeline

## 30-Second Project Pitch
Leela.exe is a mythology-based manga and future anime production system. It uses structured canon files, chapter memory, page workflows, visual references, and automation manifests to keep a long-form AI-generated story consistent.

From an AI/ML engineering angle, the project is preparing approved pages, prompts, reviews, and memory updates so they can later become datasets for LoRA, QLoRA, evaluation, and reproducible generation workflows.

The important idea is this:

The project treats AI models as continuity tools, not magic boxes.

## What This Project Already Includes
The repository already includes:
- canon files for lore, characters, and visual style
- continuity memory for series and chapter state
- workflows for page generation, continuity review, memory update, panel breakdown, and animation notes
- automation manifests and schemas
- approved asset tracking
- reference indexing
- an AI/ML strategy for LoRA, QLoRA, datasets, evals, and model cards
- templates for dataset manifests and model cards

Interview framing:

This is not just a prompt collection. It is a structured creative AI pipeline with memory, evaluation, asset lineage, and future model adaptation paths.

## What This Project Can Include Later
The project is designed to grow into:
- image datasets for character, style, environment, and motif LoRAs
- text datasets for QLoRA assistant specialization
- model cards for every trained adapter
- ComfyUI workflows for repeatable image generation
- evaluation prompt packs
- model registry records
- page-to-shot animation pipelines
- automated continuity-aware prompt generation

## Core AI/ML Concepts

## 1. Foundation Models
A foundation model is a large model trained on broad data so it can perform many tasks.

Examples:
- large language models for text
- diffusion models for images
- multimodal models for text plus image understanding

In this project:
- an image foundation model would generate manga/anime pages
- a language foundation model would write prompts, reviews, and memory updates
- a multimodal model could inspect generated pages for visual drift

Interview answer:

A foundation model gives broad general capability, but it does not automatically know my project's canon. I use project memory, retrieval, LoRA, QLoRA, and evaluation to specialize that capability safely.

## 2. Generative AI
Generative AI creates new content instead of only classifying existing content.

Examples:
- generating text
- generating images
- generating video
- generating music
- generating structured data

In this project:
- page prompts generate manga pages
- reviews generate structured feedback
- memory updates generate continuity records
- future animation notes generate shot logic

Important idea:

Generative output still needs constraints. The better the memory, references, schemas, and evals, the more useful the generation becomes.

## 3. Diffusion Models
Diffusion models are commonly used for image generation.

Simple explanation:
1. training starts with real images
2. noise is gradually added to those images
3. the model learns how to reverse noise into an image
4. during generation, the model starts from noise and denoises it toward the prompt

In this project:
- a diffusion model could generate pages, panels, character references, environments, and concept art

Interview answer:

Diffusion models generate images by learning a denoising process. For a story project, the challenge is not just making a beautiful image, but making a consistent image that follows character, style, environment, and lore constraints.

## 4. Latent Diffusion
Latent diffusion performs denoising in a compressed latent space instead of raw pixel space.

Why it matters:
- faster generation
- lower memory cost
- better practicality for large images

In image tools, the workflow usually looks like:
1. text prompt is encoded
2. image latent is denoised
3. final latent is decoded into pixels

In this project:
- LoRAs can influence the denoising process so recurring characters and styles stay more stable

## 5. LLMs
LLM means large language model.

LLMs are useful for:
- summarization
- writing
- classification
- reasoning
- code generation
- structured output
- retrieval-based workflows

In this project, an LLM can:
- create page blueprints
- compile final image prompts
- review continuity
- update chapter memory
- convert pages into animation notes
- produce structured JSON or YAML for automation

Interview answer:

I use LLMs as orchestration and reasoning tools around the creative pipeline. The LLM does not need to memorize everything if it can retrieve the right canon files and follow stable schemas.

## 6. Multimodal Models
A multimodal model can process more than one type of input.

Examples:
- text plus image
- text plus audio
- text plus video

In this project:
- a multimodal model could inspect an approved or generated page
- it could compare visual output against character references
- it could flag costume drift, environment drift, or panel composition issues

Interview answer:

For visual continuity, text-only review is limited. A multimodal model can help connect actual generated images to the project's visual memory.

## 7. Embeddings
Embeddings are numerical vector representations of data.

They can represent:
- text meaning
- image similarity
- document similarity
- scene or character descriptions

In this project:
- lore files could be embedded for retrieval
- character sheets could be retrieved when generating a page
- reference images could be searched by similarity
- prior reviews could be retrieved before writing a new review

Interview answer:

Embeddings turn project knowledge into searchable vectors. That makes it possible to retrieve the most relevant canon or reference material instead of forcing the model to rely on memory.

## 8. RAG
RAG means retrieval augmented generation.

Simple explanation:
1. store documents or assets in a searchable index
2. retrieve the most relevant context for the current task
3. give that context to the model
4. generate an answer grounded in the retrieved material

In this project:
- before generating Page 3, retrieve Chapter 1 memory, latest page review, Vishnu character sheet, Matsya notes, and style rules
- then generate the page prompt

Why RAG matters:
- canon can change
- active chapter state changes often
- retrieval is cheaper than fine-tuning for changing facts
- it reduces hallucination when used carefully

Interview answer:

I would use RAG for active canon and changing project state, and fine-tuning only for stable behavior patterns. RAG tells the model what is true now. Fine-tuning teaches the model how to behave.

## 9. Fine-Tuning
Fine-tuning means continuing training from a pre-trained model on a smaller, task-specific dataset.

It can teach:
- tone
- format
- task behavior
- domain-specific patterns

It should not be the first solution for every problem.

Use fine-tuning when:
- you have repeated examples
- the desired output format is stable
- prompting alone is not reliable
- the task behavior is consistent over time

In this project:
- QLoRA could fine-tune an assistant to produce continuity reviews
- QLoRA could fine-tune a prompt compiler
- LoRA could adapt image generation to characters or style

Interview answer:

I would not fine-tune just to store facts. I would fine-tune to teach stable behavior, and use retrieval for changing project context.

## 10. PEFT
PEFT means parameter efficient fine-tuning.

Instead of updating all model weights, PEFT updates a small number of extra parameters.

Why it matters:
- cheaper training
- faster experiments
- smaller adapter files
- easier versioning
- less risk than full fine-tuning

LoRA and QLoRA are PEFT methods.

## 11. LoRA
LoRA means low-rank adaptation.

Simple explanation:
- instead of changing the entire model, LoRA adds small trainable matrices to certain model layers
- these small adapters learn a narrow concept
- during generation, the adapter influences the base model

In image generation, LoRA is useful for:
- a specific character
- a specific art style
- a specific environment
- a recurring object or motif

In this project, LoRA is the visual consistency layer.

Planned LoRA tracks:
- child Vishnu LoRA
- Matsya LoRA
- Manu LoRA
- Leela.exe house style LoRA
- Vaikuntha environment LoRA
- flood ocean environment LoRA
- lotus and sacred light motif adapters

Good LoRA practice:
- train narrow adapters
- use approved images only
- caption images cleanly
- separate character, style, and environment datasets
- evaluate before production use
- write a model card

Bad LoRA practice:
- training from one image too early
- mixing rejected images into the dataset
- trying to make one LoRA learn every character and style
- not tracking the dataset version

Interview answer:

LoRA is useful here because the project needs recurring visual identity across many generated pages. I would use separate, narrow LoRAs for characters, style, and environments so each adapter has a clear job and can be evaluated independently.

## 12. QLoRA
QLoRA means quantized low-rank adaptation.

Simple explanation:
- QLoRA uses quantization to reduce memory requirements
- then it trains LoRA-style adapters on top of a quantized base model
- this makes LLM fine-tuning more practical on limited hardware

In this project, QLoRA is the language and reasoning adaptation layer.

QLoRA can train an assistant to:
- review continuity
- compile prompts from canon and memory
- update chapter memory
- rewrite outputs in the correct tone
- convert manga pages into animation notes
- produce structured JSON/YAML outputs

Important distinction:
- LoRA for images helps visual identity
- QLoRA for language helps assistant behavior

Interview answer:

I would use LoRA to stabilize visual generation and QLoRA to specialize the language assistant. QLoRA would not be my main tool for image style. It is better for teaching repeatable review, prompt, and memory-update behavior.

## 13. LoRA vs QLoRA
LoRA:
- parameter efficient adapter method
- often used for image or language models
- updates small trainable matrices
- useful for visual style or identity when used with image models

QLoRA:
- LoRA plus quantization
- commonly used for memory-efficient LLM fine-tuning
- useful when hardware is limited
- good for structured assistant behavior

Interview short answer:

LoRA is the adapter technique. QLoRA is a memory-efficient version that uses quantization, especially useful for fine-tuning large language models.

## 14. Quantization
Quantization reduces the numerical precision of model weights.

Example:
- full precision may use 16-bit or 32-bit numbers
- quantized models may use 8-bit or 4-bit numbers

Why it matters:
- lower memory usage
- faster inference or training in some cases
- makes large models practical on smaller GPUs

Tradeoff:
- too much quantization can reduce quality
- careful evaluation is needed

In QLoRA:
- the base model is quantized
- small LoRA adapters are trained
- this saves memory while preserving much of the base model's capability

## 15. Prompt Engineering
Prompt engineering is designing inputs so a model produces useful outputs.

In this project, prompts should include:
- page objective
- character identity
- environment
- style constraints
- emotional beat
- continuity safeguards
- negative constraints
- output format requirements

Good prompt engineering is not random keyword stuffing.

It should be:
- structured
- repeatable
- grounded in memory
- evaluated against outputs

Interview answer:

Prompting is the first control layer. But for a production system, prompting alone is not enough. I also need retrieval, schemas, evals, references, datasets, and eventually adapters.

## 16. Negative Prompts
Negative prompts tell an image model what to avoid.

In this project, negative prompts can help suppress:
- generic fantasy armor
- glossy sci-fi mortal scenes
- horror-fish Matsya anatomy
- character age drift
- inconsistent costume details
- wrong caption style
- unwanted neon interface effects

Important idea:

Negative prompts are not a full solution. They reduce drift, but they do not replace good references, LoRAs, or reviews.

## 17. Seeds
A seed controls the initial randomness of generation.

Why it matters:
- reproducibility
- controlled variation
- debugging
- comparing prompt changes

In this project:
- page generation should record seeds when possible
- evals should use fixed seeds for fair comparison

Interview answer:

Seeds help make image generation reproducible. If I change a LoRA strength or prompt phrase, a fixed seed helps isolate what caused the output difference.

## 18. Inference-Time Controls
Inference means running the model to generate output.

Controls include:
- prompt
- negative prompt
- seed
- resolution
- aspect ratio
- CFG or guidance scale
- sampler
- steps
- LoRA strength
- reference image
- ControlNet or adapter inputs

In this project:
- these settings should eventually be stored in structured generation metadata
- that makes outputs reproducible and debuggable

## 19. ControlNet And Reference Adapters
ControlNet and reference adapters guide image generation using extra inputs.

They can control:
- pose
- depth
- edges
- line art
- composition
- reference style
- character likeness

In this project, they could help:
- preserve panel composition
- keep characters on-model
- translate a manga page into animation frames
- reuse a pose or environment layout

Interview answer:

LoRA teaches a model a concept. ControlNet or reference adapters guide a specific generation. They solve different problems and can be combined.

## 20. ComfyUI
ComfyUI is a node-based interface for building image generation workflows.

In this project, a ComfyUI graph could accept:
- base checkpoint
- page prompt
- negative prompt
- LoRA names and strengths
- reference images
- seed
- output path
- metadata

Why it matters:
- repeatable workflows
- clear generation graph
- easier debugging
- easier automation

Interview answer:

ComfyUI would let me turn the creative pipeline into a reproducible graph where project state becomes structured input to image generation.

## 21. Datasets
A dataset is the curated training or evaluation data used by a model.

In this project, there are different dataset types:
- image datasets for LoRA
- text datasets for QLoRA
- evaluation datasets for testing
- rejected examples for negative analysis

Important rule:

Production assets are not automatically training data.

An image should become training data only after:
1. it is approved
2. it is registered
3. it is captioned
4. it has metadata
5. it is assigned to a train/eval split

Interview answer:

Dataset quality matters more than dataset size for adapters. I would rather train on fewer approved, well-captioned, traceable examples than many noisy images.

## 22. Dataset Lineage
Dataset lineage means knowing where every training example came from.

For each image or text item, track:
- source path
- approval status
- chapter and page
- subject tags
- style tags
- caption path
- review path
- dataset split
- license or origin

Why it matters:
- reproducibility
- debugging
- legal safety
- preventing drift
- model card accuracy

Interview answer:

If a model behaves badly, lineage lets me trace the failure back to possible training examples, captions, or dataset versions.

## 23. Captioning
Captioning tells the image model what is in each training image.

Good captions should:
- include the trigger token
- identify the subject
- describe stable traits
- describe variable traits
- mention pose, angle, lighting, and environment
- avoid unrelated lore

Example:

```text
leela_vishnu_child, child Vishnu in sacred blue-gold attire, calm knowing expression, seated in Vaikuntha admin space, lotus geometry, soft divine light, cinematic manga panel
```

Why it matters:

Captions teach the model what to associate with the trigger token and what should remain controllable by the prompt.

## 24. Trigger Tokens
A trigger token is a special phrase used to activate a learned concept.

Examples:
- `leela_vishnu_child`
- `leela_matsya`
- `leela_mythic_manga_style`
- `leela_vaikuntha_admin`

In this project:
- trigger tokens make adapters easier to control
- they reduce ambiguity
- they help distinguish project-specific concepts from generic words

Interview answer:

Trigger tokens provide a stable handle for concepts learned during adapter training.

## 25. Train, Eval, And Holdout Splits
A dataset is usually split into:
- train set: used for training
- eval set: used during evaluation
- holdout set: hidden examples used for final testing

Why it matters:
- prevents false confidence
- detects overfitting
- measures generalization

In this project:
- approved pages can be split into training and evaluation candidates
- eval prompts can test whether a LoRA works outside the exact training composition

Interview answer:

If I only test on training examples, I do not know whether the adapter learned the concept or memorized the images.

## 26. Overfitting
Overfitting means the model memorizes training data instead of learning a generalizable pattern.

In this project, overfitting could look like:
- Vishnu always appearing in the same pose
- Matsya always copying one panel composition
- style LoRA forcing the same lighting everywhere
- environment LoRA recreating one exact background

Mitigation:
- use varied examples
- keep adapters narrow
- use eval prompts
- use holdout examples
- avoid training too early

Interview answer:

Overfitting is a major risk when training LoRAs from too few images. That is why this project focuses first on approved references, captions, and evals before training.

## 27. Data Leakage
Data leakage means information from the test or eval set accidentally enters training.

Why it is bad:
- evaluation scores become misleading
- model quality appears better than it is

In this project:
- if eval images are also used for training, LoRA evaluation becomes weak
- if answer examples leak into a QLoRA eval set, assistant performance is inflated

Interview answer:

Good split discipline is part of MLOps. Without it, evaluation results cannot be trusted.

## 28. Dataset Poisoning
Dataset poisoning means bad or incorrect examples enter the training data.

In this project, poisoning could happen if:
- rejected images are trained as canon
- a wrong costume is included
- a non-sacred tone is captioned as correct
- style-drift pages are used in the style dataset

Mitigation:
- never train from incoming assets
- track approval review paths
- keep rejected examples separate
- use dataset manifests

Interview answer:

For creative AI, poisoned data may not look like malicious data. It can simply be visually appealing but canonically wrong.

## 29. Evaluation
Evaluation measures whether a model or workflow is good enough.

For this project, evaluation includes:
- identity consistency
- costume consistency
- environment consistency
- prompt adherence
- mythology tone
- composition quality
- chapter continuity
- structured output correctness

Good evaluation should be:
- repeatable
- written before training
- tied to failure cases
- stored with the model card

Interview answer:

In generative AI, evaluation is not only accuracy. It includes quality, consistency, controllability, and domain constraints.

## 30. Visual Evaluation Gates
A character LoRA should pass tests like:
- neutral model sheet
- emotional close-up
- action pose
- wide environment scene
- cross-character scene
- different lighting conditions
- different camera angles

A style LoRA should pass tests like:
- different subjects
- different locations
- different moods
- no forced character identity
- no over-dominant color drift

In this project:
- evaluation should compare output against canon references
- failed outputs should become known failure cases

## 31. Text Evaluation Gates
A QLoRA assistant should pass tests like:
- follows output format
- does not invent canon
- asks for missing inputs when necessary
- separates lore review from visual review
- writes concise memory updates
- preserves sacred simulation tone

In this project:
- QLoRA should be evaluated on continuity reports, prompt compilation, memory updates, and animation notes

## 32. Model Cards
A model card is documentation for a trained model or adapter.

It should include:
- model name
- purpose
- base model
- dataset version
- training config
- trigger tokens
- recommended strength
- eval prompts
- pass/fail notes
- known failure modes
- production status

In this project:
- every LoRA and QLoRA should have a model card
- use `templates/model_card_template.md`

Interview answer:

Model cards make model behavior auditable. They help future engineers understand what the adapter is for, how it was trained, and when not to use it.

## 33. Model Registry
A model registry tracks trained models and adapters.

It records:
- model versions
- dataset versions
- training configs
- approvals
- deployment status
- known limits

In this project:
- future models could live under `models/adapters`
- model cards could live under `models/model_cards`
- training configs could live under `models/training_configs`

Interview answer:

A registry helps prevent random model files from becoming production dependencies without documentation.

## 34. MLOps
MLOps means applying engineering discipline to machine learning systems.

It includes:
- dataset versioning
- model versioning
- reproducible training
- evaluation pipelines
- deployment tracking
- monitoring
- rollback plans
- lineage

In this project, MLOps appears as:
- structured folders
- runtime state
- schemas
- manifests
- reference index
- dataset manifest template
- model card template
- evaluation gates

Interview answer:

MLOps is the difference between a one-off model demo and a maintainable AI system.

## 35. Structured Outputs
Structured output means asking the model to produce data in a format like JSON, YAML, or a fixed Markdown template.

Why it matters:
- easier automation
- easier validation
- less ambiguity
- better downstream integration

In this project:
- continuity reports can follow templates
- runtime state can be YAML
- QLoRA examples can be JSONL
- page packets can become structured generation inputs

Interview answer:

Structured output turns the model from a writer into a component that other systems can use.

## 36. JSONL
JSONL means JSON Lines.

Each line is a separate JSON object.

Why it is useful:
- common for fine-tuning datasets
- easy to stream
- easy to validate line by line

Example:

```jsonl
{"task":"continuity_review","instruction":"Review the page for drift.","input":{"page_summary":"..."},"output":{"approval":"revise","flags":["costume drift"]}}
```

In this project:
- QLoRA datasets should use compact JSONL examples

## 37. Schemas
A schema defines the expected shape of data.

Examples:
- required fields
- field types
- allowed values

In this project:
- schemas can validate continuity reports
- schemas can validate page packets
- schemas can validate runtime state
- schemas can validate dataset manifests

Interview answer:

Schemas reduce ambiguity and make automation safer because invalid model outputs can be detected before they corrupt project state.

## 38. Human-In-The-Loop
Human-in-the-loop means a human reviews or approves model outputs before they become official.

In this project:
- generated pages are reviewed before approval
- memory updates are checked
- references are registered manually or semi-automatically
- LoRAs are approved only after evals

Why it matters:
- creative taste still matters
- mythology tone must be protected
- continuity errors can compound if accepted blindly

Interview answer:

For this kind of project, I would keep human approval at canon-changing steps. Automation can accelerate production, but approval should protect continuity.

## 39. Canon, Memory, And State
This project uses several layers of knowledge:

Canon:
- stable lore, character, and style rules

Memory:
- series and chapter facts that accumulate over time

State:
- current active chapter, latest page, latest approved asset, next task

Why it matters:

AI systems need to know what is stable and what is current. Mixing those up causes drift.

Interview answer:

I separate immutable canon from runtime memory so the assistant can retrieve stable world rules and changing chapter state differently.

## 40. Continuity As An AI Problem
Continuity means keeping details consistent over time.

In this project, continuity includes:
- character design
- costume
- environment
- weather
- emotional state
- revealed knowledge
- page pacing
- mythology tone

Why it is hard:
- generative models are stochastic
- prompts are incomplete
- details drift across outputs
- visual consistency requires references and adapters

AI/ML solution stack:
- memory files
- reference index
- retrieval
- LoRA
- QLoRA
- multimodal review
- evaluation gates

## 41. Image Generation Pipeline
A future production image pipeline could look like this:

1. Read canon and chapter memory.
2. Generate page blueprint.
3. Generate final prompt.
4. Select base image model.
5. Select LoRAs and strengths.
6. Select reference images.
7. Set seed and generation settings.
8. Generate page.
9. Review image for continuity.
10. Approve, revise, or reject.
11. Update memory and reference index.
12. Add approved assets to future dataset candidates.

Interview answer:

The image model is only one part of the pipeline. The real system includes memory, references, metadata, evals, and feedback loops.

## 42. QLoRA Assistant Pipeline
A future QLoRA assistant pipeline could look like this:

1. Collect high-quality examples of reviews, prompts, and memory updates.
2. Convert them into structured JSONL.
3. Split into train and eval sets.
4. Fine-tune with QLoRA.
5. Evaluate format compliance and hallucination risk.
6. Compare against a prompted baseline.
7. Approve only if it improves reliability.

Interview answer:

I would compare QLoRA against strong prompting plus retrieval. Fine-tuning is only worth it if it improves consistency, format adherence, or domain behavior.

## 43. RAG vs Fine-Tuning
Use RAG when:
- facts change often
- the model needs current project state
- source traceability matters
- you want easy updates without retraining

Use fine-tuning when:
- the behavior pattern is stable
- the format is repeated
- prompting is too inconsistent
- you have enough high-quality examples

In this project:
- RAG for active canon and memory
- LoRA for visual identity
- QLoRA for assistant behavior

Interview answer:

RAG gives the model context. Fine-tuning changes behavior. I would use both, but for different jobs.

## 44. LoRA vs ControlNet vs Prompting
Prompting:
- tells the model what to generate
- flexible but sometimes inconsistent

LoRA:
- teaches a recurring concept
- good for identity or style

ControlNet or reference adapters:
- guide a specific composition, pose, edge map, or layout
- good for control over a single generation

In this project:
- prompt defines the page
- LoRA stabilizes recurring identity
- ControlNet can preserve composition or pose

Interview answer:

Prompting, LoRA, and ControlNet are complementary. Prompting describes intent, LoRA provides learned identity, and ControlNet provides structural control.

## 45. Adapter Strength
LoRA strength controls how much influence the adapter has.

Low strength:
- subtle influence
- may not preserve identity strongly

High strength:
- stronger identity
- may cause artifacts or overfitting behavior

In this project:
- model cards should record recommended strength ranges
- evals should test multiple strengths

Interview answer:

Adapter strength is a production parameter. It should be evaluated and documented, not guessed every time.

## 46. Base Model Choice
The base model matters because LoRA adapts an existing capability.

If the base model is weak at:
- anatomy
- manga rendering
- sacred lighting
- panel composition

Then the LoRA has to fight the base model.

In this project:
- choose a base model with strong illustration and cinematic composition
- train adapters to specialize, not compensate for every weakness

Interview answer:

A LoRA is not a replacement for a good base model. The base model should already be strong in the general domain.

## 47. Versioning
Versioning means labeling changes clearly.

Examples:
- `lora_vishnu_sdxl_v001`
- `lora_vishnu_sdxl_v002`
- `dataset_vishnu_v001`
- `qlora_continuity_reviewer_v001`

Why it matters:
- reproducibility
- debugging
- rollback
- comparison

In this project:
- every dataset and model should have a version

## 48. Reproducibility
Reproducibility means another engineer can recreate or understand the result.

Track:
- source data
- captions
- dataset split
- base model
- training config
- seed
- inference settings
- adapter versions
- evaluation results

Interview answer:

Reproducibility is critical because without it, a good output is just luck, not an engineering result.

## 49. Hallucination
Hallucination means a model invents information that is not grounded in the source.

In this project, hallucination could look like:
- inventing a new avatar rule
- changing Manu's role
- adding sci-fi concepts to mortal scenes
- claiming an unapproved asset is canon

Mitigation:
- retrieval
- clear schemas
- citations to project files
- human review
- QLoRA evals for missing-input behavior

Interview answer:

For a canon-heavy project, hallucination is not just factual error. It can damage continuity.

## 50. Production Readiness
An AI feature is production-ready when:
- inputs are defined
- outputs are structured
- failures are understood
- evaluation exists
- model versions are tracked
- humans know when to override it
- there is a rollback path

In this project:
- a LoRA is not ready until it passes visual evals
- a QLoRA is not ready until it follows formats and avoids canon hallucination

## Interview Questions And Strong Answers

## Q1. What is the AI/ML angle of this project?
The project is a continuity-first AI production pipeline. It uses structured canon, memory, workflows, references, and automation manifests to generate manga pages consistently. The AI/ML layer prepares approved assets and text outputs for future LoRA, QLoRA, evaluation, and reproducible generation.

## Q2. Why use LoRA here?
LoRA is useful because the project needs stable recurring visual identity. Characters like Vishnu, Matsya, and Manu need consistent faces, costumes, silhouettes, and symbolic details across pages. Separate LoRAs can also stabilize the house style, environments, and motifs.

## Q3. Why use QLoRA here?
QLoRA is useful for specializing a language model on repeated project tasks like continuity review, prompt compilation, chapter memory updates, and animation notes. It is memory-efficient and practical when full fine-tuning would be too expensive.

## Q4. Why not train immediately from Page 1?
One image is not enough variety. Training from one page can overfit the adapter to one pose, composition, lighting setup, or style artifact. The better approach is to build approved references, captions, metadata, and eval prompts first.

## Q5. What is the difference between RAG and fine-tuning?
RAG retrieves current context and facts at inference time. Fine-tuning changes model behavior through training. In this project, I would use RAG for current canon and chapter state, and fine-tuning for stable repeated behaviors like review format or prompt compilation.

## Q6. What is dataset lineage?
Dataset lineage is the ability to trace each training example back to its source, approval status, captions, metadata, and dataset split. It helps with debugging, reproducibility, legal safety, and preventing bad assets from becoming training data.

## Q7. How would you evaluate a character LoRA?
I would test identity consistency across close-ups, wide shots, different angles, different expressions, action poses, and cross-character scenes. I would also test multiple adapter strengths and compare outputs against approved canon references.

## Q8. How would you evaluate a QLoRA continuity reviewer?
I would test whether it follows the expected review format, catches visual and lore drift, avoids inventing canon, asks for missing inputs when needed, and produces concise memory updates.

## Q9. What are the biggest risks in this project?
The biggest risks are visual drift, mythology tone drift, overfitting from training too early, dataset poisoning from unapproved assets, and hallucination in memory updates.

## Q10. How does this project show MLOps thinking?
It separates assets, references, datasets, models, templates, memory, and automation. It requires approval gates, dataset manifests, model cards, versioning, evals, and lineage. That is MLOps thinking applied to a creative AI pipeline.

## Q11. What is the role of model cards?
Model cards document the purpose, base model, dataset version, trigger tokens, training config, eval results, known failure modes, and production status of an adapter. They make models auditable and safer to use.

## Q12. What is a trigger token?
A trigger token is a special token or phrase used to activate a learned concept in a LoRA. For example, `leela_vishnu_child` could activate the child Vishnu identity learned by a character LoRA.

## Q13. What is overfitting in a LoRA?
Overfitting happens when the LoRA memorizes the training images instead of learning a flexible concept. In this project, Vishnu might always appear in the same pose or lighting if the dataset is too narrow.

## Q14. What does quantization do?
Quantization reduces the precision of model weights, often from 16-bit or 32-bit to 8-bit or 4-bit. It reduces memory usage and can make large model fine-tuning more practical. QLoRA uses quantization with LoRA adapters.

## Q15. How would you automate this project?
I would use project memory and runtime state to build structured page packets, feed those into prompt generation, pass structured inputs into a ComfyUI graph, save generation metadata, run continuity review, and update memory only after approval.

## Concepts To Memorize
- Foundation model: broad pre-trained model used as a base.
- Diffusion model: image model that learns to denoise.
- Latent diffusion: diffusion in compressed representation space.
- LLM: language model for text and reasoning tasks.
- Multimodal model: model that handles multiple input types.
- Embedding: vector representation of meaning or similarity.
- RAG: retrieval plus generation.
- Fine-tuning: additional training on task-specific data.
- PEFT: efficient fine-tuning with few trainable parameters.
- LoRA: low-rank adapter for efficient specialization.
- QLoRA: quantized LoRA, often for efficient LLM fine-tuning.
- Quantization: lower precision weights to save memory.
- Trigger token: token used to activate a trained concept.
- Dataset lineage: traceability from training example to source.
- Model card: documentation for a model or adapter.
- Eval gate: test that must pass before production use.
- MLOps: engineering discipline for ML systems.

## How To Explain The Project Like An AI/ML Engineer
Say this:

```text
The project is a creative AI production pipeline with structured memory, canon management, asset lineage, and future adapter training. I separate image adaptation from language adaptation: LoRA handles recurring visual identity, while QLoRA handles repeated assistant behaviors like continuity review and prompt compilation. I also separate production assets from training datasets, require approval before training use, and document models with dataset versions and eval results.
```

## What To Study Next
For interviews, focus on:
1. LoRA and QLoRA basics
2. RAG vs fine-tuning
3. diffusion model basics
4. dataset quality and lineage
5. train/eval splits
6. overfitting and data leakage
7. model cards and MLOps
8. structured outputs and schemas
9. evaluation for generative AI
10. how to explain this project as a production system

## One-Line Summary
Leela.exe uses AI/ML engineering to make generative storytelling consistent, traceable, and eventually trainable through LoRA for visuals, QLoRA for assistant behavior, and rigorous dataset and evaluation discipline.
