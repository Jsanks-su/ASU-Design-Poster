---
name: movie-poster-style-director
description: Use when Codex needs to turn arbitrary content, concepts, products, essays, events, campaigns, or prompts into content-matched high-quality poster or pictorial-poster image-generation prompts, including cinematic, animated, abstract, graphic, ink, painterly, platform-sized, typography-aware, inventive, and anti-low-design poster direction.
---

# Movie Poster Style Director

## Core Principle

Translate any subject into disciplined high-quality poster art direction using cinematic and pictorial-poster grammar. Do not default to realistic festival-poster restraint or one fixed release-material template. Small release-like text, invented emblems, logo-like marks, icons, pictograms, seals, and footer metadata can be useful design material when they support the poster world. First route the content into a visual world, then invent and judge image mechanisms, then build a controlled prompt with medium, composition, color, typography, format, and negative constraints.

## Default Behavior

Use Chinese for reasoning and delivery unless the user asks otherwise. Write the final image-generation prompt in English by default, because most image APIs follow visual terms more reliably in English.

For ChatGPT Image 2 or direct image-generation tests, include visible poster typography by default: a short main title treatment plus context-appropriate secondary copy. The secondary copy can be a tagline, quote, theme phrase, annotation, column label, small metadata, footer copy, release-like microtype, bilingual fragments, invented emblem marks, simple pictograms, or other layout text required by the brief. It is acceptable to use small movie-poster-style text as visual texture when it improves hierarchy and atmosphere. Avoid full fake cast lists, false real release claims, real release dates, or billing blocks as automatic filler; use full release simulation only when the user asks for it. Use post-production typography only when the user explicitly asks for a clean no-text image, the copy is long, or exact Chinese text accuracy matters more than poster completeness.

Default to a vertical poster when the user does not explicitly request a platform crop. Use 2:3 for classic poster tests and 3:4 for Xiaohongshu-style covers. Use horizontal WeChat/X/header formats only when the user explicitly asks for a wide article cover, timeline image, banner, header, or horizontal layout.

If the user asks to generate an image and an image API/tool is available, produce and preflight the controlled poster prompt internally, then generate exactly one completed image per selected direction without waiting for prompt approval unless the user explicitly asks to review prompts first. Do not automatically revise and regenerate after seeing the output. After generation, inspect the image and provide a concise recap: saved path, prompt/design summary, visible strengths, problems, and suggested correction notes for a possible next run. If an image API fails before producing an image, retry at most once for a transient server error, then stop and report the failure.

## Workflow

1. Distill the content into a poster brief:
   - subject, story tension, emotional temperature, audience, platform, orientation, title/copy requirements
   - one dominant visual idea, not a collage of everything
   - one poster promise: what the viewer should feel in three seconds

2. Route the visual style:
   - Read `references/style-router.md` unless the user already gave a specific style.
   - Read `references/route-selection-policy.md` when the input is title-only, abstract, or asks for multiple outputs.
   - Read `references/abstract-impression-poster-grammar.md` when the user asks for abstract, impressionistic, color-block, graphic, typography-led, collage, painterly-field, or less realistic output; when a title-only brief is mostly emotional or philosophical; or when batch tests have drifted too realistic.
   - Read `references/chinese-cinematic-grammar.md` when the subject is Chinese culture, Chinese history, wuxia, myth, folk memory, Chinese-language drama, Chinese city life, "Chinese style", "guofeng", or "国风".
   - For simple single-output briefs, consider 2-3 route hypotheses when the content genuinely supports multiple interpretations. For title-only, ambiguous, or batch contexts, scan the route families and choose 3-5 route hypotheses for the shortlist. This is a diagnostic step, not a quota.
   - Do not vary styles for their own sake. Match the content first. Alternatives must be defensible interpretations of the same content, such as faithful fit, counterpoint, argument-led metaphor, material logic, audience readability, color logic, or typography system.
   - Pick one primary visual world before writing the final prompt: live-action realism, graphic modernism, ink/line drawing, painterly, animation/anime, experimental abstraction, collage, retro genre cinema, or another specific route.

3. Select a poster lineage:
   - If the user gives a movie style, extract the design grammar without copying the exact poster, actor likeness, logo, title treatment, or protected IP.
   - If style is unspecified, use `references/visual-style-catalog.md`, `references/poster-style-catalog.md`, and `references/reference-grammar-library.md` to choose a lineage.
   - Prefer style coherence over one fixed idea of prestige. High quality can be realistic, animated, ink, abstract, humorous, graphic, or commercial.

4. Generate image-mechanism hypotheses:
   - Read `references/poster-invention-operators.md` when the user wants stronger, more surprising, less precedent-bound work, or when the first direction risks feeling merely competent.
   - Read `references/cinematic-poster-quality-bar.md` for serious poster outputs, when the user asks for higher quality, or when the result risks feeling merely usable.
   - Generate 3-5 hidden hypotheses before prompting when quality matters. Use operators such as compression, substitution, scale shift, negative-space invention, material transfer, cultural transfer, typographic mutation, viewer-position shift, pattern anomaly, or boundary violation.
   - Each hypothesis must name the mechanism, operation, simple image, why it fits, and risk.

5. Judge and select the mechanism:
   - Read `references/aesthetic-judgment-rubric.md` when multiple mechanisms are possible, the user asks for better taste, or the output must feel like a finished high-quality poster rather than a concept image.
   - Select the candidate with the strongest balance of compression, three-second read, visual tension, specificity, freshness, title/copy hierarchy, color necessity, material intelligence, and anti-low resilience.
   - Name one visual tension pair, such as huge vs tiny, blank vs crowded, calm surface vs hidden threat, old material vs modern subject, or beautiful vs violent.
   - Do not rely on atmosphere alone. The poster should have a designed visual idea that survives without the title.

6. Adapt the canvas:
   - Read `references/platform-sizes.md` when the user names Xiaohongshu, WeChat, X/Twitter, vertical, horizontal, header, cover, or content image.
   - Default to a vertical poster unless the user explicitly asks for a horizontal platform crop.
   - Design for the target crop first. Do not create one generic image and crop later unless explicitly requested.

7. Build the art direction:
   - medium: live-action photo, 2D animation, anime key art, ink wash, line drawing, woodcut, collage, oil painting, graphic vector-like poster, clay/stop-motion, etc.
   - composition: subject scale, foreground/background, negative space, horizon, symmetry/asymmetry
   - image mechanism: the one chosen mechanism and how it creates visual tension
   - viewpoint: camera/lens for realistic posters, or drawing/painting perspective for non-realistic posters
   - light or mark-making: key light for photo realism; brush, line, paper, cel shading, print texture, or abstraction rules for illustrated routes
   - color: read `references/color-system.md`; choose palette stance, dominant/support/accent colors, saturation, contrast, and material surface
   - typography system: read `references/typography-system.md` and `references/typography-composition-catalog.md`; choose English, Chinese, or bilingual title hierarchy and a composition role according to the poster lineage
   - typography zone: title location, safe area, supporting-copy area, microtype/icon/emblem area, footer/side information area, whether text is rendered visibly or reserved for post-production
   - poster copy: include a visible main title treatment and context-appropriate secondary text by default; use small release-like microcopy, invented icons, logo-like marks, seals, and footer information blocks when they improve the poster design; keep them style-matched, generic/fictive unless the user supplies real assets, and subordinate to the main image and title
   - material: film grain, paper grain, ink bleeding, cel texture, risograph, screen print, old paper, matte stock, analog imperfection when appropriate

8. Run the anti-low gate:
   - Always check `references/anti-low-design.md` before finalizing.
   - Remove cheap AI-poster habits without flattening all styles into realism. Cartoon, anime, ink, abstraction, collage, and painterly routes are valid when intentional and coherent.

9. Run the pre-generation gate:
   - Do this before any image API call. Fix the prompt before generation, not after.
   - Reject unresolved scaffolding such as bracketed options, internal analysis, "choose one", or template placeholders.
   - Confirm the requested/default canvas is vertical unless the user asked for horizontal.
   - Confirm visible title/copy hierarchy is requested for direct poster tests.
   - Confirm any release-like microcopy, icons, logo-like marks, seals, metadata, or footer blocks are intentional, style-matched, and generic/fictive unless the user supplies real assets.
   - Confirm the prompt does not add automatic fake cast lists, false real release dates, billing-block clutter, "A FILM BY", premiere/laurel language, or real brand/studio logos unless the user explicitly asked for full release simulation or supplied the assets.
   - Confirm the prompt states one clear image mechanism, one visual tension pair, a color strategy, a typography role, and negative constraints.

10. Output controlled prompts:
   - Provide one recommended direction first.
   - Add 2 compact alternatives only when the content supports them. Each alternative must explain its content logic, not merely swap style.
   - Include positive prompt, negative prompt, aspect ratio/size, text handling, and a short design rationale.

11. Generate only when requested:
   - Default generation budget is one completed image per selected direction.
   - Do not run automatic improvement loops, comparison rounds, or "fix and regenerate" cycles.
   - After generation, inspect and recap the output. If the output violates the brief, preserve the existing output and provide correction notes or a revised prompt for a possible next run.

## Output Format

```markdown
## 海报方向
[一句话说明视觉概念和电影气质]

## 设计判断
- 内容转译:
- 设计假设:
- 风格路由:
- 电影海报谱系/视觉母体:
- 图像机制:
- 发明算子:
- 视觉张力:
- 审美取舍:
- 色彩策略:
- 字体构图:
- 画幅/平台:
- 主视觉:
- 留白与文字区:

## 生图 Prompt
[English prompt for the image API]

## 生图前检查
- aspect/canvas:
- title/copy:
- microcopy/release-material:
- unresolved-template risk:
- anti-low gate:

## Negative Prompt
[English negative prompt]

## 参数建议
- aspect ratio:
- canvas:
- text strategy:
- variants:

## 反 Low 检查
[一句话说明删掉了哪些廉价设计风险]
```

## Text Strategy

Match typography to the poster style before deciding whether text is rendered in-image. Typography is part of the style route, not a finishing label. Technology, sci-fi, and contemporary prestige posters can use an English main title plus Chinese secondary title. Chinese historical, wuxia, folk, or ink-style posters can use calligraphy, seal-script, stele, or handwritten Chinese typography when it fits the lineage. Animated and cartoon posters can use drawn, rounded, playful, or characterful lettering when it matches the film world. Do not force one universal title style across genres.

For direct ChatGPT Image 2 poster tests, prefer one of these:

- **Default poster test:** render a visible short title treatment and a context-appropriate copy hierarchy. Secondary text can be tagline, quote, theme phrase, annotation, column label, metadata, footer copy, release-like microtype, bilingual fragments, invented emblems, logo-like marks, icons, pictograms, seals, or other designed text. Exact small text does not need to be readable, but the poster must visibly contain intentional copy hierarchy.
- **Bilingual route:** use exact English text as the main rendered title when it strengthens the style, then place the Chinese title as a smaller subtitle or secondary main title.
- **Chinese graphic-title route:** ask for a short Chinese title as expressive poster lettering or graphic shapes when visual completeness matters more than exact OCR accuracy.
- **Post-production route:** generate without exact readable text only when the user explicitly wants typography added later, the copy is long, or exact Chinese text must be controlled outside the image model.

Never let title text dominate the poster unless the chosen lineage is explicitly typography-led.

## Resources

- `references/poster-style-catalog.md`: compact catalog of 100 cinematic poster lineages and design grammars.
- `references/style-router.md`: route arbitrary content into distinct poster style families before prompting.
- `references/route-selection-policy.md`: content-first route selection, counterpoint gate, argument-led routing, and multiple-output judgment.
- `references/abstract-impression-poster-grammar.md`: abstract/impression route triggers, color-field and typography-led grammar, source grammar policy, and anti-wallpaper gate.
- `references/chinese-cinematic-grammar.md`: modern Chinese cinematic poster grammar beyond stale ink/calligraphy defaults.
- `references/cinematic-poster-quality-bar.md`: image mechanism, visual tension, and poster-quality gate for sharper film-key-art prompts.
- `references/poster-invention-operators.md`: mechanism-generation operators for less obvious, more original poster ideas.
- `references/aesthetic-judgment-rubric.md`: silent scoring rubric for selecting the strongest candidate and rejecting weak novelty.
- `references/visual-style-catalog.md`: non-realistic, graphic, animated, abstract, painterly, ink, and commercial style families.
- `references/reference-grammar-library.md`: poster, painting, and popular-appeal grammar without copying specific works.
- `references/color-system.md`: palette stance, color contrast, accent-color role, and anti-low color rules.
- `references/platform-sizes.md`: Xiaohongshu, WeChat, X/Twitter, and general poster canvas ratios.
- `references/typography-system.md`: title hierarchy and font-style rules by poster lineage.
- `references/typography-composition-catalog.md`: title-as-image, diagonal, marginalia, seal, bilingual, and other typographic composition moves.
- `references/anti-low-design.md`: low-design failure modes and repair rules.
- `references/prompt-templates.md`: reusable prompt structures for vertical and horizontal posters.
