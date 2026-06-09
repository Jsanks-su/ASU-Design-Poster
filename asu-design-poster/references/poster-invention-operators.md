# Poster Invention Operators

Use this when the user wants stronger, more surprising, less precedent-bound poster ideas, or when the first direction feels competent but not memorable.

The goal is not novelty for novelty's sake. A good invented poster still compresses the subject into one readable image. These operators expand the search space before the aesthetic gate narrows it.

## Operating Rule

First name the strong obvious poster. Keep it if it already has:

- a clear dramatic hook
- strong poster presence
- visible title/copy potential
- a three-second read
- a specific image that belongs to this subject

Use invention operators only when they produce a better poster than that strong obvious route.

When invention is needed, generate 3-5 image-mechanism hypotheses before writing the final prompt. Each hypothesis must contain:

```text
Mechanism:
Operation:
Image:
Why it fits:
Risk:
```

Reject any hypothesis whose "Why it fits" is only "it looks cool."

## Core Operators

| Operator | How to use it | Example move |
| --- | --- | --- |
| Compression | Turn the whole story into one object, body part, space, or mark. | A corruption story becomes one clean white room with a tiny stain. |
| Substitution | Replace the obvious subject with a thing that bears its consequence. | Instead of a victim, show a chair, file, shoe, apple, curtain, or empty bed. |
| Scale shift | Make something tiny monumental, or a vast system feel intimate. | One legal stamp becomes a city wall; one tear becomes a river. |
| Negative-space invention | Let absence make the image. | Missing face, empty doorway, blank paper, cutout body, silence around one small object. |
| Material transfer | Move the subject into an unexpected surface. | AI becomes skin texture; business becomes ledger paper; family becomes court evidence. |
| Cultural transfer | Use cultural structure rather than surface symbols. | A modern office story uses ritual hierarchy, gate pressure, or vertical inscription logic. |
| Genre counterpoint | Use a visual genre that clarifies by contradiction. | A horror story as sterile hospital minimalism; romance as forensic archive. |
| Typographic mutation | Make the title a physical force. | Title as road, wall, smoke, wound, prison bars, wave, shadow, or bureaucratic grid. |
| Time collision | Put two time systems in one image. | Ancient material with modern subject; future interface as temple plaque; childhood object in adult violence. |
| Viewer-position shift | Change where the viewer stands morally or physically. | Seen from under a table, behind a curtain, inside a file, from the object's point of view. |
| Pattern anomaly | Establish repetition, then break it once. | Rows of windows, seats, trees, blinds, files, or faces with one impossible difference. |
| Boundary violation | Make inside/outside, body/world, text/image, or object/landscape exchange roles. | A face becomes a map; a mountain becomes a robe; a title becomes architecture. |

## Search Procedure

1. Write the subject's real conflict in one sentence.
2. Name the obvious poster and score whether it is already strong enough.
3. Apply at least three operators from different families:
   - one image-object operator: compression, substitution, scale shift, negative space
   - one material/culture operator: material transfer, cultural transfer, time collision
   - one composition/operator: typography mutation, viewer-position shift, pattern anomaly, boundary violation
4. Keep only hypotheses with a clear three-second read.
5. Send the finalists through `aesthetic-judgment-rubric.md`.

## Bad Novelty

Reject:

- surreal objects that do not clarify the subject
- overloaded metaphor stacks
- random style mashups
- abstract posters that cannot be explained in one sentence
- clever images with no emotional pressure
- AI-detail fireworks instead of a stronger visual idea
- avoiding a strong cinematic hook only because it feels "obvious"

## Prompt Add-On

```text
Inventive operation: [operator].
The poster improves on the expected subject depiction by turning the story into [invented image mechanism].
The image remains readable in three seconds because [simple visual read].
```
