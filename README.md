# Shakespeare

**Agent-agnostic skill: write like a human — or like you.**

Not a detector-evasion tool. A writing process: pull real human samples, pull the user's own ideas (and optional personal corpus), co-write section by section, then review for AI tells and voice match.

## Install (any agent)

```bash
git clone https://github.com/sisiphamus/shakespeare.git
```

Point your agent at the folder. Examples:

| Agent | What to say / do |
|-------|------------------|
| **Claude Code** | Copy or symlink into a skills path, or: *Read `…/shakespeare/SKILL.md` and follow it for writing.* |
| **Codex / Cursor / others** | *Use the Shakespeare skill at `<path>`. Read SKILL.md.* |
| **Hermes / OpenClaw** | Add the folder to whatever skill/plugin path the host uses; entry files are `SKILL.md` + `AGENTS.md`. |

One-liner for the agent:

> Clone or open https://github.com/sisiphamus/shakespeare — read `SKILL.md` and run that process for this writing task.

## What it does

1. Asks what you're writing (answers optional; more of *your* ideas → more human)
2. Loads **real human samples** from the closest category (`academic`, `narrative`, `conversational`, `fun`, `email`)
3. Loads craft rules + AI-tell + reader-psychology checks
4. Optional: **your voice** via local files, Google Drive/Docs MCP, Gmail MCP (sent mail)
5. Writes **section by section**, asking after each for more of your specifics
6. **Review pass** (separate subagent if possible): de-AI + voice match

## Modes

- **Generic human** — category samples + rules only  
- **Your voice** — same, plus as many of your own samples as you can give  

If you decline local paths and MCPs, it stays generic human.

## Layout

```
shakespeare/
  SKILL.md           # process (agents read this)
  AGENTS.md          # short entry
  README.md          # you are here
  LICENSE            # MIT (skill packaging)
  rules/             # craft, AI tells, reader psych
  samples/           # real human exemplars + SOURCES.md
```

## Samples (provenance)

See [`samples/SOURCES.md`](samples/SOURCES.md). Categories use public-domain literature (Project Gutenberg), CC BY open-access papers (PLOS), the Enron email corpus (public research release), and attributed NUS SMS excerpts for casual register.

## License

MIT for skill code and rules. Sample texts keep the licenses stated in their file headers.
