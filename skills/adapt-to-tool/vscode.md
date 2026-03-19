# Adapting dev-edc skills to VS Code Copilot

VS Code Copilot natively supports the same skill format as Claude Code — `SKILL.md` files with YAML frontmatter in a `skills/` subfolder. Minimal adaptation is required.

## Target format

VS Code Copilot reads skills from these locations automatically:

```
.github/skills/{skill-name}/SKILL.md
.claude/skills/{skill-name}/SKILL.md   ← already works if fetched with degit
.agents/skills/{skill-name}/SKILL.md
```

Additional locations can be configured via the `chat.agentSkillsLocations` VS Code setting.

## How to use

Since dev-edc skills are already in the correct format, no conversion is needed if you fetched them into `.claude/skills/` (the default degit path):

```sh
npx degit colinhauch/dev-edc/skills/{skill-name} .claude/skills/{skill-name}
```
