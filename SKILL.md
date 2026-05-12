---
name: ai-kigurumi-head-reference
description: prompt workflow for converting anime or game character references into multi-view kigurumi head shell design references. use when the user wants to prepare, generate, refine, or troubleshoot ai image prompts for kigurumi head shell references, including hoodless character head turnarounds, kigurumi head shell four-view designs, and product-photo-style four-view or eight-view outputs.
---

# AI Kigurumi Head Reference Workflow

Use this skill to help users convert anime/game character references into Kigurumi head shell multi-view references.

The workflow should be staged. Do not recommend generating the final head shell image in one step.

## Core Workflow

1. Generate a hoodless or de-occluded character head four-view reference.
2. Convert the character head reference into a Kigurumi head shell four-view design.
3. Convert the Kigurumi design into a product-photo-style four-view or eight-view reference.
4. Troubleshoot specific failures with targeted correction prompts.

## General Rules

- Ask the user which step they are currently executing.
- Ask what images they uploaded and what role each image should play.
- Separate reference image roles clearly.
- Do not let Kigurumi examples override the target character's identity.
- Do not introduce product-photo realism too early.
- Prefer four-view generation before eight-view generation.
- Preserve correct parts explicitly when asking for corrections.
- Correct one main issue at a time.

## Stage 1: Character Head Four-View Reference

Goal: generate a clean, de-occluded character head reference sheet.

Output views:

- Front
- Left-front 45 degrees
- Left side
- Back

Use when the user still needs to establish the character's head structure, hairstyle, face, ears, and expression before Kigurumi conversion.

Recommended uploads:

- Front character reference
- Back character reference
- Side or 45-degree character reference
- Target expression reference
- Official 2D image for mood and identity
- If the character is occluded, use hoodless 3D model images or in-game screenshots as structural references

Do not upload Kigurumi examples in Stage 1.

See `prompts/step1-head-reference.md`.

## Stage 2: Kigurumi Head Shell Four-View Design

Goal: convert the Stage 1 character head reference into a Kigurumi head shell design sheet.

Recommended uploads:

- Final Stage 1 character head four-view image
- 1-2 target expression references
- 2-3 high-quality Kigurumi head shell examples

Kigurumi examples should only define shell language, eye socket structure, wig handling, and product/design quality. They should not define the target character's face, hair, color, or expression.

See `prompts/step2-kigurumi-design.md`.

## Stage 3: Product-Photo-Style Four/Eight-View Reference

Goal: convert the Kigurumi design into a final product-photo-style multi-view reference.

Recommended uploads:

- Final Stage 2 Kigurumi head shell design
- 1-3 product-photo-style Kigurumi examples
- Optional target expression reference

Generate four views first. Generate eight views only after the four-view result is stable.

See `prompts/step3-product-view.md`.

## Troubleshooting

When the user reports a bad result, ask them to provide:

1. Current workflow step
2. Uploaded reference images and their roles
3. Current prompt
4. What is already correct
5. What is wrong
6. What should be changed

Use targeted correction prompts from `prompts/troubleshooting.md`.

Common issues:

- Expression is wrong
- Front face does not match
- Face is too sharp or too mature
- Result is not Kigurumi enough
- Result is too 3D, doll-like, or realistic
- Multi-view consistency is poor
- Kigurumi examples polluted the target character identity
