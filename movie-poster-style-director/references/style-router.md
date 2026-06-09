# Style Router

Use this before writing a prompt unless the user already names a style. The goal is to avoid every poster becoming dark, realistic, and festival-like.

## Route Selection

Pick one primary route and optionally one secondary influence.

| Content signal | Primary routes to consider |
| --- | --- |
| Social issue, ecology, disease, labor, documentary fact | documentary realism, editorial illustration, ink/line metaphor, graphic modernism |
| Technology, AI, future, systems, business | hard sci-fi realism, abstract data metaphor, modernist typography, technical diagram-poster, anime sci-fi key art |
| Animals, nature, children, public education | nature documentary, hand-painted storybook, Japanese animation nature, ink wash, woodcut conservation poster |
| Historical, Chinese culture, martial arts, myth | modern guofeng, minimal ink force, red-black cut, shadow theatre, palace/gate pressure, material archive, wuxia live-action, Chinese animation epic |
| Modern Chinese city, Chinese-language drama, family, law, business, social tension | contemporary guofeng, editorial realism, modern Chinese display typography, material archive, urban noir, ritual color counterpoint |
| Personal emotion, family, memory, grief | intimate realism, pencil/charcoal drawing, watercolor, soft animation, poetic abstraction |
| Humor, irony, absurdity, satire | deadpan modernist, cartoon editorial, collage, pop-art, absurdist character poster |
| Horror, taboo, fear, uncertainty | expressionist graphic, folk horror, minimal symbol, scratch drawing, distorted typography |
| Youth, love, friendship, everyday life | coming-of-age photo, anime theatrical, pastel illustration, risograph, candid street realism |
| Product/business concept with metaphor | premium commercial key art, graphic symbol, collage, modernist typography, surreal object poster |
| Very abstract title or philosophical idea | modernist abstraction, surrealism, symbolic object, typography-led, painterly field |

## Route Hypothesis Rule

When the user gives only a title, consider a hidden shortlist of up to 3 routes. This is a thinking aid, not an output quota:

1. one faithful or genre-congruent route
2. one argument-led metaphor route
3. one counterpoint, material-led, typography-led, or popular-readability route when it fits

Choose the route that best matches the title's emotional promise. If the user is exploring, show only the routes that are genuinely defensible and ask which one to generate.

For multiple outputs, do not mechanically assign one realism, one graphic, one ink, and one abstract route. Start from content fit. Multiple outputs may share a broad visual family if the content demands it; vary stance, symbol, composition, color logic, or typography only when that creates a stronger interpretation. See `route-selection-policy.md`.

## Style Mixing

Mix only two layers:

- visual medium: ink, anime, oil painting, collage, live-action, graphic design
- film genre: noir, documentary, sci-fi, horror, romance, satire, epic

Avoid mixing three or more strong styles in one prompt. "Ink wash + ecological documentary" is strong. "Ink wash + cyberpunk + Pixar + noir + oil painting" is incoherent.

## Chinese Style Gate

When a subject triggers Chinese culture, Chinese-language drama, wuxia, history, myth, folk memory, or "guofeng", read `chinese-cinematic-grammar.md` before prompting.

Do not choose "ink wash + calligraphy" by default. First decide whether the stronger route is:

- minimal ink force
- red-black cut
- shadow theatre
- palace / gate / ritual space
- mountain-water as psychology
- material archive
- contemporary guofeng
- decorative epic

The route must name a design mechanism, such as a calligraphic stroke becoming the road, a palace gate becoming social pressure, a red field becoming a wound, or a tiny modern figure trapped inside ritual color.

## Artist References

Prefer public-domain art movements, poster traditions, medium descriptions, and film-poster grammars over copying a specific living artist. If the user asks for an artist-like style, translate it into neutral traits: palette, composition, line, texture, mood, and printing method.
