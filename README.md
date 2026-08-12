![Shakespeare](assets/banner.svg)

# Shakespeare

Your agent already writes. Most of the time it writes like a brochure that went to a writing class.

This skill is a process you drop into Claude, Codex, Cursor, Hermes, OpenClaw, or anything else that can read a folder. It steals your ideas first, reads real human samples, drafts in sections, then forces a check against a hard banlist before anything ships. Generic human, or your voice if you hand it your own writing.

Give it nothing private and you get nothing private. That is the whole product.

[MIT](LICENSE) · host-agnostic · [issues](https://github.com/sisiphamus/shakespeare/issues)

---

## Install

```bash
git clone https://github.com/sisiphamus/shakespeare.git
```

Tell the agent:

```
Use the Shakespeare skill in this folder.
Read AGENTS.md then SKILL.md. Follow the process.
```

Works the same on Claude Code (path or skills symlink), Codex, Cursor, Hermes, and OpenClaw.

---

## How it runs

1. You say what you are writing and dump as much of your take as you want (topic, audience, notes, real details).
2. It loads samples for the genre: academic, narrative, conversational, fun, or email.
3. It loads craft rules and the banlist.
4. Optional: your voice from local files, Drive/Docs, or Gmail sent mail.
5. It drafts section by section and keeps pulling specifics from you.
6. It **must** re-check against the rules before returning the draft. One-shot without review is a fail.

Two modes:

| | |
|--|--|
| **Generic human** | samples + rules |
| **Your voice** | same, plus as much of your writing as you can give |

No files and no MCP means generic human. Do not invent a “you.”

---

## What gets killed on review

Full list is in `rules/`. The high-signal ones:

- Interest labels (“that’s where it gets interesting”)
- Pointer glue (“the part people see”)
- Definition snaps (“That joining is fusion.”)
- Fake-plain gloss (“shows up as heat and light”)
- Bare 4–8 word scene openers as every paragraph start
- Sealed essay kits and multi-beat coach memos for a three-line email
- Costume casual (fragment stacks, “I’ll be blunt,” workshop metaphors nobody says)
- Faux-casual science and teach-back cosplay

Your awkward real detail beats a clever invented one.

---

## Repo

```
shakespeare/
  AGENTS.md       entry + MUST CHECK YOUR WORK
  SKILL.md        full process
  rules/          craft, banlist, reader psych, review
  samples/        real human text by genre (see SOURCES.md)
  assets/         banner
```

Sample sources: Project Gutenberg, PLOS (CC BY), Enron public release, NUS SMS excerpts. Licenses sit on the files.

---

## License

MIT for the skill and rules. Samples keep the license in their headers.
