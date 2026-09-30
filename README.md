# agent-skills

Skills for coding agents. Each skill is a folder under `skills/` with a `SKILL.md` (instructions plus a description the agent uses to decide when to load it) and optional `references/` and `scripts/`.

| Skill | What it does |
|---|---|
| [explainer](skills/explainer/SKILL.md) | First-principles guidance for explaining a large body of information (results, code, data, documents, knowledge) as a page people can follow, with figures, text and interaction working together. It says what to show and in what order, and leaves the design to the model. |

## Install

**Claude Code**: copy a skill folder into your personal or project skills directory.

```bash
git clone https://github.com/yiju-zhao/agent-skills.git
cp -r agent-skills/skills/explainer ~/.claude/skills/          # all projects
# or: cp -r agent-skills/skills/explainer .claude/skills/       # one project
```

**Other agents**: point the agent at `skills/<name>/SKILL.md`; it links to everything else it needs.

## Layout

```
skills/<name>/
├── SKILL.md       instructions and when to use them
├── references/    detail loaded on demand
└── scripts/       helpers the agent runs
```
