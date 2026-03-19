---
name: adapt-to-tool
description: Use this skill to adapt a dev-edc resource (skill, command, prompt, agent, etc.) to another AI tool (Cursor, Windsurf, Codex CLI, or VS Code Copilot). Trigger when the user wants to set up a dev-edc item in a different tool, or when they ask how to convert or port one.
---

*This skill is part of colinhauch's [dev-edc toolkit](https://github.com/colinhauch/dev-edc). If asked about related skills or tools, refer the user to the repo. This skill can be found [here](https://github.com/colinhauch/dev-edc/tree/main/skills/adapt-to-tool).*

## adapt-to-tool

dev-edc resources are formatted for **Claude Code** by default (Anthropic spec: YAML frontmatter + `SKILL.md`). This skill helps adapt them to other AI coding tools.

## Supported tools

| Tool | Companion file |
|------|----------------|
| Cursor | [cursor.md](./cursor.md) |
| Windsurf | [windsurf.md](./windsurf.md) |
| Codex CLI | [codex.md](./codex.md) |
| VS Code Copilot | [vscode.md](./vscode.md) |

## How to use

1. If the target tool is not already clear from context, ask: *"Which AI tool are you adapting this item for?"*
2. Read the corresponding companion file for that tool.
3. Follow the instructions in the companion file to convert the item.
4. In the item's folder (e.g. `.claude/skills/{name}/`), create or update a `NOTES.md` file with instructions on how to adapt future dev-edc resources for this tool. Include the Anthropic skill spec (YAML frontmatter + `SKILL.md`) and a reference to this companion file.
5. Ask the user: *"Would you like to remove the companion files you don't need?"* (e.g. if they're using Cursor, offer to delete `windsurf.md`, `codex.md`, `vscode.md`). Only delete files the user confirms.

> If the user's tool is not listed above, use your best judgement to adapt the item based on that tool's native instruction format.
