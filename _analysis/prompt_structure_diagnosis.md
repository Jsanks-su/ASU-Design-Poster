# Prompt Structure Diagnosis

Source reference folder: `C:\Users\27504\Desktop\电影海报`

## What The Reference Set Actually Says

- 75 images analyzed.
- 68 are standard vertical poster format.
- 6 are tall vertical format.
- 1 is near-square.
- The reference set does not support a horizontal default. Horizontal can be a platform export, but the default movie-poster design should be vertical.

## Text / Copy

The reference posters generally include visible poster typography:

- main title
- subtitle or release copy
- cast/quote/award text in some cases
- bottom credit block / billing block

The current prompt pattern often says "no readable text rendered" or "title to be added in post", which is technically safe for Chinese text accuracy but visually wrong for the user's reference standard. For ChatGPT Image 2 testing, the prompt should usually ask for visible poster typography by default, with fallbacks:

- short English or bilingual title when exact text matters
- Chinese title as graphic title treatment when the model can approximate it
- bottom credit block as tiny poster texture even when exact names are not important
- reserve post-production only when the user explicitly needs clean typography control

## Visual Energy

The reference set is not consistently minimalist. It includes:

- large title typography
- high-saturation red/yellow/blue fields
- strong graphic symbols
- dense poster texture
- actor/character-led commercial posters
- montage and illustration routes
- white-space posters, but not white-space-only thinking

The current generated test prompts over-weighted:

- quiet negative space
- sterile minimalism
- no readable title
- tiny human vs huge structure
- "premium restraint"

This creates visually controlled images, but not enough movie-poster presence.

## Invention Boundary

The reference set supports invention, but not forced weirdness.

Good invention:

- improves compression
- makes the subject more memorable
- creates a stronger poster read than the obvious image
- remains legible in three seconds

Bad invention:

- avoids the obvious subject just to be different
- removes the dramatic hook
- becomes a conceptual art plate rather than a movie poster
- sacrifices title hierarchy and commercial readability

## Root Cause In Current Skill

1. `platform-sizes.md` lets platform examples, especially WeChat header logic, override the movie-poster default.
2. `SKILL.md` has no hard default saying "vertical poster unless explicitly asked otherwise."
3. `Text Strategy` treats no-text generation as "best quality", which is mismatched for poster testing with ChatGPT Image 2.
4. `prompt-templates.md` inserts `Inventive operation` too universally, pushing every prompt away from obvious depiction.
5. The quality bar currently rewards mechanism and restraint more than title hierarchy, poster presence, and reference-grade visual amplitude.

## Fix Direction

The skill should change from:

```text
invent mechanism -> avoid obvious poster -> reserve text area
```

to:

```text
vertical poster default -> choose poster presence level -> include visible title typography by default -> use invention only when it beats the strong obvious poster -> keep credit/title structure as part of the image
```

