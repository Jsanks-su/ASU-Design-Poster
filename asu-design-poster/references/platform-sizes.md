# Platform Sizes

Last checked for current common practice: 2026-06-08. Treat these as production-safe starting points, not immutable platform law. If a platform changes its crop UI, preserve important content in safe areas and export a larger canvas at the same ratio.

## Default Rule

The default output for this skill is a vertical poster, not a platform banner.

Use these defaults unless the user explicitly asks otherwise:

| Use | Ratio | Canvas | Notes |
| --- | --- | --- | --- |
| Classic vertical poster default | 2:3 | 1200 x 1800 or 1600 x 2400 | Use for general poster tests, concepts, and unknown platforms. |
| Xiaohongshu-style poster cover | 3:4 | 1080 x 1440 | Use when the user wants a social poster, Chinese content cover, or stronger mobile feed presence. |

Horizontal WeChat, X/Twitter, banner, and header formats are export formats. Use them only when the user explicitly asks for horizontal, wide, header, article cover, timeline image, or banner.

## Xiaohongshu Vertical Posters

Primary use: note covers and vertical content images.

| Use | Ratio | Canvas | Notes |
| --- | --- | --- | --- |
| Best cover poster | 3:4 | 1080 x 1440 | Strong default for Xiaohongshu feed presence. |
| Vertical social poster | 4:5 | 1080 x 1350 | Good for general social compatibility. |
| Tall immersive poster | 9:16 | 1080 x 1920 | Use for story-like or mobile-first drama. |
| Square backup | 1:1 | 1080 x 1080 | Use only when grid consistency matters. |

Safe area: keep faces, title, and main symbol inside the central 80%. Avoid thin details near the top/bottom edge.

## WeChat Official Account

Primary use: article cover/header and in-article images.

| Use | Ratio | Canvas | Notes |
| --- | --- | --- | --- |
| Lead article cover/header | 2.35:1 | 900 x 383 or 1080 x 460 | Design as a cinematic wide still. Keep important content centered vertically. |
| Wide content image | 16:9 | 1280 x 720 or 1920 x 1080 | Useful for section dividers or visual chapters. |
| Dense article image | 4:3 | 1200 x 900 | Better for diagrams or richer subject detail. |
| Secondary thumbnail | 1:1 | 500 x 500 or 900 x 900 | Needs a simplified crop, not a squeezed header. |

Safe area: for 2.35:1 covers, keep title and key subject in the middle 60-70% height. Avoid tiny information text unless post-production typography is planned.

## X / Twitter

Primary use: timeline image, article preview, campaign image.

| Use | Ratio | Canvas | Notes |
| --- | --- | --- | --- |
| Timeline wide image | 16:9 | 1200 x 675 or 1600 x 900 | Strong default; cinematic and crop-stable. |
| Link-like card | 1.91:1 | 1200 x 628 | Useful when the image should read like a preview card. |
| Square image | 1:1 | 1200 x 1200 | Use when subject needs central graphic impact. |
| Vertical post | 4:5 | 1080 x 1350 | Use carefully; keep subject centered for timeline crop variance. |

Safe area: assume the timeline may crop previews. Keep the focal subject and title away from edges.

## General Poster Ratios

| Use | Ratio | Canvas |
| --- | --- | --- |
| Classic vertical poster | 2:3 | 1200 x 1800 or 1600 x 2400 |
| One-sheet feel | 27:40 approximation | 1620 x 2400 |
| Cinematic still/banner | 16:9 | 1920 x 1080 |
| Ultra-wide header | 2.35:1 | 1880 x 800 or 1080 x 460 |

## Format Rule

Never describe only pixels. Include both ratio and platform purpose in the prompt:

`vertical 3:4 Xiaohongshu poster cover, 1080x1440 composition, title-safe negative space at top third`
