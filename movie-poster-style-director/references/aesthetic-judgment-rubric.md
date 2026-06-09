# Aesthetic Judgment Rubric

Use this after generating image-mechanism hypotheses and before writing the final prompt. This is the judging layer that prevents both stale templates and random novelty.

## Scoring

Score each candidate from 0-3 on each dimension. Prefer the highest total only if it has no fatal flaw.

| Dimension | 0 | 1 | 2 | 3 |
| --- | --- | --- | --- | --- |
| Compression | Lists the topic | Shows a scene | Reduces topic to one idea | One image contains the whole conflict |
| Three-second read | Confusing | Needs explanation | Mostly legible | Instantly legible and intriguing |
| Visual tension | Flat | Mood only | Clear contrast | Strong pressure between opposing forces |
| Specificity | Generic | Genre-common | Subject-specific | Could only belong to this subject |
| Poster presence | Looks like concept art or a still | Has poster layout hints | Reads as a strong poster | Feels like a finished high-quality poster with title and intentional copy hierarchy |
| Visual amplitude | Too quiet or low energy | Controlled but weak | Strong focal impact | Memorable scale, color, crop, type, or symbol with confidence |
| Typography/copy hierarchy | Missing or pasted on | Text zone planned | Visible title and secondary copy structure | Title, supporting copy, and layout text feel designed into the poster |
| Freshness | Template | Familiar but decent | Unusual angle | Feels not yet seen but still inevitable |
| Color necessity | Decorative | Genre default | Supports mood | Carries story role or contradiction |
| Material intelligence | None | Surface texture | Fits subject | Material itself tells the story |
| Anti-low resilience | AI-poster risk | Some template risk | Mostly disciplined | Hard to cheapen without breaking concept |

## Fatal Flaws

Reject the candidate even if it scores well elsewhere:

- The concept needs a paragraph to explain.
- The image is only attractive, not meaningful.
- The route copies a famous poster too closely.
- The style is doing all the work and the image mechanism is weak.
- Typography would be illegible or unrelated.
- It depends on exact Chinese text being rendered correctly by the image model.
- It has no visible poster copy when the goal is a direct poster-generation test.
- It becomes a campaign banner, product ad, fan art, or mood board.
- It becomes a tasteful concept plate instead of a finished poster or pictorial poster.
- The cultural symbols are decorative rather than structural.

## Selection Rules

Choose the candidate that best balances:

1. **Inevitable fit**: once seen, it feels like the right image for the subject.
2. **Poster presence**: it has a real title/copy hierarchy and enough visual force to read as a finished high-quality poster or pictorial poster.
3. **One-image memory**: the viewer can remember it as a simple visual sentence.
4. **Production plausibility**: a current image model can plausibly render it.

When candidates tie, prefer the one with stronger poster presence and image mechanism over the one with prettier restraint.

## Mini Review Format

```text
Candidate A: [mechanism] - score [x]/33
Strength: [best dimension]
Risk: [main flaw]
Verdict: [keep/reject/revise]
```

## Revision Moves

| Weak score | Revision |
| --- | --- |
| Low compression | Remove plot elements until one object, mark, body fragment, or space remains. |
| Low three-second read | Increase silhouette clarity, contrast, scale difference, or symbolic simplicity. |
| Low tension | Add an opposing force: blank/crowded, clean/violent, small/vast, old/modern, soft/dangerous. |
| Low freshness | Apply material transfer, viewer-position shift, typographic mutation, or pattern anomaly. |
| Low specificity | Replace generic symbols with subject-specific space, material, evidence, or consequence. |
| Low typography | Decide whether type is image, label, seal, institution, whisper, export subtitle, or post-production zone. |
| Low poster presence | Add visible title treatment, supporting copy, annotation, footer text block, stronger focal hierarchy, or a more confident crop. |
| Low visual amplitude | Increase scale contrast, title size, color field, body crop, symbol clarity, or graphic force without adding clutter. |

## Output Rule

Do not show full scoring unless the user asks for process detail. In normal output, use the rubric silently and explain the selected direction in one or two design-judgment bullets.
