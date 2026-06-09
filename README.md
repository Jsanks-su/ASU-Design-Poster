# Movie Poster Style Director Skill

This repository packages one portable AI-agent skill:

```text
movie-poster-style-director/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
```

The skill turns arbitrary content, concepts, products, essays, events, campaigns, or short titles into controlled movie-poster-style image-generation prompts. It is designed to work as a folder-based skill bundle, so agents beyond Codex can reuse it as long as they can read `SKILL.md` and the sibling `references/` files.

## Codex Install

Copy the whole skill directory into the Codex personal skills directory:

```powershell
Copy-Item -Path ".\movie-poster-style-director" -Destination "$env:USERPROFILE\.codex\skills\" -Recurse -Force
```

Expected final path:

```text
%USERPROFILE%\.codex\skills\movie-poster-style-director\SKILL.md
```

## Hermes Agent Reuse

Use the same folder-based distribution pattern:

1. Clone or copy this repository into the Hermes-accessible machine or workspace.
2. Copy `movie-poster-style-director/` into the skills directory configured for that Hermes Agent environment.
3. Keep the folder name unchanged.
4. Make sure Hermes can read `SKILL.md` first and then load files from `references/` when the skill asks for them.

If a Hermes installation does not yet have a formal skills directory, register this folder as a knowledge/workflow resource and use this trigger:

```text
Use movie-poster-style-director when turning content into movie-poster-style image-generation prompts.
```

## Claude Code / CC Reuse

If the CC environment supports folder-based Skills, install the full `movie-poster-style-director/` folder into its user or project skill directory.

If the environment does not expose a Skills loader, add a project instruction that points the agent at this folder and tells it:

```text
When asked for movie poster prompts or poster art direction, read movie-poster-style-director/SKILL.md first. Follow its workflow. Load referenced files from movie-poster-style-director/references/ only when needed.
```

## OpenCalw / Other Agents

For agents with custom tool, prompt, or knowledge-pack systems, treat this as a portable workflow package. The minimum compatibility contract is:

- Load `movie-poster-style-director/SKILL.md` as the entrypoint.
- Preserve relative paths to `references/`.
- Do not flatten all reference files into the base prompt unless the agent has no on-demand file loading.
- Trigger the skill for poster prompts, image-generation prompts, film-key-art direction, platform-sized social posters, typography-aware poster design, and anti-low-design poster refinement.
- Output the format requested by `SKILL.md`: direction, design judgment, English image prompt, negative prompt, parameter suggestions, and anti-low-design check.

## Distribution Notes

Keep the skill folder self-contained. Do not move reference files away from `movie-poster-style-director/references/`, because `SKILL.md` refers to them by relative path.

Generated examples in `output/` are examples only. They are not required for installation.
