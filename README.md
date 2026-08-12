# Shakespeare (instance 1)

Write like a human, or like a specific person if you feed the skill their writing.

This is a process rather than a detector-evasion tool: real samples, the user's ideas, section-by-section drafting, then a review that removes AI sludge and checks voice.

**shakespeare-1** is a test copy of the main skill with the instructional prose rewritten for a more casual, human register. The rules and information match the parent system.

## Install

```bash
git clone https://github.com/sisiphamus/shakespeare.git
# or point your agent at this folder
```

| Host | What to do |
|------|------------|
| Claude Code | Point at this path, or symlink into skills |
| Codex / Cursor | Use Shakespeare at `<path>` and read SKILL.md |
| Hermes / OpenClaw | Put the folder on the skill path; entry files are `SKILL.md` and `AGENTS.md` |

Tell the agent to open this Shakespeare folder, read `SKILL.md`, and run that process for the writing task.

## What it does

1. Asks what you are writing (questions are optional; more of your ideas usually helps)
2. Loads real human samples from the closest category
3. Loads craft, AI-tell, and reader-psych rules
4. Optionally pulls your voice from local files, Drive/Docs, or Gmail sent mail
5. Writes section by section and keeps asking for your specifics
6. Runs a review pass for de-AI, grit, and voice match

Phrases that almost always sound fake include interest-bridges ("that's where it gets interesting"), stock "vivid" details nobody actually lived, neat observational essay kits, and closers that deny a deep lesson while handing you one. Prefer the user's grit.

## Modes

- **Generic human** — samples and rules  
- **Your voice** — same, plus as much of their writing as you can get  

Without files or MCP access, stay in generic human mode.

## Layout

```
shakespeare-1/
  SKILL.md      # process
  AGENTS.md     # short entry
  README.md     # this file
  LICENSE       # MIT for skill packaging
  rules/        # craft, tells, reader psych, review
  samples/      # real human text by category + SOURCES.md
```

## Samples

See `samples/SOURCES.md` for provenance (Project Gutenberg public domain, PLOS CC BY, Enron public release, attributed NUS SMS excerpts).

## License

MIT for skill packaging and rules. Sample files keep the licenses in their headers.
