# ASU Design Poster Skill

This repository packages one portable AI-agent skill:

```text
asu-design-poster/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
```

The skill turns arbitrary content, concepts, products, essays, events, campaigns, or short titles into controlled movie-poster-style image-generation prompts. It is designed to work as a folder-based skill bundle, so agents beyond Codex can reuse it as long as they can read `SKILL.md` and the sibling `references/` files.

## Codex Install

Copy the whole skill directory into the Codex personal skills directory:

```powershell
Copy-Item -Path ".\asu-design-poster" -Destination "$env:USERPROFILE\.codex\skills\" -Recurse -Force
```

Expected final path:

```text
%USERPROFILE%\.codex\skills\asu-design-poster\SKILL.md
```

## Hermes Agent Reuse

Use the same folder-based distribution pattern:

1. Clone or copy this repository into the Hermes-accessible machine or workspace.
2. Copy `asu-design-poster/` into the skills directory configured for that Hermes Agent environment.
3. Keep the folder name unchanged.
4. Make sure Hermes can read `SKILL.md` first and then load files from `references/` when the skill asks for them.

If a Hermes installation does not yet have a formal skills directory, register this folder as a knowledge/workflow resource and use this trigger:

```text
Use asu-design-poster when turning content into movie-poster-style image-generation prompts.
```

## Claude Code / CC Reuse

If the CC environment supports folder-based Skills, install the full `asu-design-poster/` folder into its user or project skill directory.

If the environment does not expose a Skills loader, add a project instruction that points the agent at this folder and tells it:

```text
When asked for movie poster prompts or poster art direction, read asu-design-poster/SKILL.md first. Follow its workflow. Load referenced files from asu-design-poster/references/ only when needed.
```

## OpenCalw / Other Agents

For agents with custom tool, prompt, or knowledge-pack systems, treat this as a portable workflow package. The minimum compatibility contract is:

- Load `asu-design-poster/SKILL.md` as the entrypoint.
- Preserve relative paths to `references/`.
- Do not flatten all reference files into the base prompt unless the agent has no on-demand file loading.
- Trigger the skill for poster prompts, image-generation prompts, film-key-art direction, platform-sized social posters, typography-aware poster design, and anti-low-design poster refinement.
- Output the format requested by `SKILL.md`: direction, design judgment, English image prompt, negative prompt, parameter suggestions, and anti-low-design check.

## Distribution Notes

Keep the skill folder self-contained. Do not move reference files away from `asu-design-poster/references/`, because `SKILL.md` refers to them by relative path.

Generated examples in `output/` are examples only. They are not required for installation.
