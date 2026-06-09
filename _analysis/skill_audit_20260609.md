# Movie Poster Skill Audit 2026-06-09

## Context

The skill was tested with four generated posters after adding image-mechanism invention and aesthetic judging. The results exposed four failures:

1. The first test produced a horizontal image when the user expected vertical by default.
2. The generated posters lacked visible poster copy.
3. The visuals were controlled but did not match the reference folder's movie-poster energy.
4. The skill encouraged difference for its own sake.

Reference folder: `C:\Users\27504\Desktop\电影海报`

## Reference Evidence

The reverse scan in `_analysis/poster_reference_reverse_analysis.md` found:

- 75 images analyzed.
- 68 are standard vertical poster format.
- 6 are tall vertical format.
- 1 is near-square.
- Visible title hierarchy and bottom credit/billing texture are common.
- The set includes bold commercial color, large typography, graphic symbols, character-led posters, collage, illustration, and negative-space posters. It is not a purely minimalist collection.

## Root Causes

### 1. Default canvas is under-specified

`SKILL.md` asks for platform/orientation, but does not say that a movie poster defaults to vertical. `platform-sizes.md` lists WeChat/X horizontal uses as normal production formats, so a platform phrase can override the poster default.

### 2. Text strategy is technically safe but visually wrong

`SKILL.md` says the best quality path is to generate no exact text and add typography later. That is useful for final typography control, but wrong for testing ChatGPT Image 2 as a poster generator. The model must usually be asked to create visible poster typography, title hierarchy, and credit-block texture.

### 3. Prompt templates overuse invention language

Every template contains "The poster avoids the obvious depiction..." This pushes outputs toward conceptual detours even when the obvious cinematic hook would be stronger.

### 4. The quality rubric rewards restraint more than poster presence

The rubric values compression, tension, freshness, and anti-low resilience, but it does not explicitly score:

- poster presence
- title/copy hierarchy
- commercial-readability vs art restraint balance
- reference-grade visual amplitude
- whether the image still feels like a released film poster

### 5. Negative prompts may suppress typography too broadly

The negative prompt rejects broken typography, fake 3D text, and illegible Chinese. That is correct, but combined with no-readable-text guidance it can make the model avoid text entirely.

## Fix Direction

Change the skill from:

```text
invent mechanism -> avoid obvious poster -> reserve text area
```

to:

```text
vertical poster default -> visible poster copy by default -> choose poster presence level -> use invention only when it beats the obvious cinematic hook -> keep title and credit block as part of the image
```

## Acceptance Criteria

- Default poster prompt uses a vertical ratio, normally 2:3 or 3:4, unless the user explicitly asks for WeChat/X/header/wide.
- ChatGPT Image 2 prompts normally include visible title treatment and poster credit/billing texture.
- "No readable text" is reserved for final post-production or exact Chinese text risk, not for default testing.
- Invention operators are conditional, not mandatory.
- The aesthetic rubric includes poster presence, visual amplitude, and title/copy hierarchy.
- Prompt templates distinguish between visible typography and post-production typography.

