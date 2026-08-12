![shakespeare](assets/banner.png)

# Shakespeare

Your agent already writes. Usually like a brochure that took a writing class.

This is a process folder for Claude / Codex / Cursor / Hermes / OpenClaw / whatever can read files. Steals their ideas first, reads real human samples, drafts in sections, forced banlist check before ship. Generic human, or their voice if they hand over their own writing.

Nothing private in → nothing private out.

MIT · host-agnostic · clone and point

## Install

```bash
git clone https://github.com/sisiphamus/shakespeare.git
```

Tell the agent:

```
Use the Shakespeare skill in this folder.
Read AGENTS.md then SKILL.md. Follow the process.
```

## How it runs

1. They say what + dump as much take as they want
2. Load genre samples (academic / narrative / conversational / fun / email)
3. Load craft + banlist
4. Optional: their voice from files / Drive / Gmail sent
5. Section draft, keep pulling grit
6. Must re-check rules before return. One-shot without review = fail

generic human = samples + rules  
their voice = same + their writing  

No files no MCP → generic. Don't invent a "you."

## What review kills

Full list in `rules/`. Big ones:

- interest labels ("that's where it gets interesting")
- pointer glue ("the part people see")
- definition snaps ("That joining is fusion.")
- fake-plain gloss ("shows up as heat and light")
- bare 4–8 word scene openers as every para start
- sealed essay kits / multi-beat coach memos for a three-line email
- costume casual (fragment stacks, "I'll be blunt," workshop metaphors nobody says)
- faux-casual science and teach-back cosplay

Awkward real detail beats clever invented one.

## Repo

AGENTS.md — entry + must-check  
SKILL.md — process  
rules/ — craft, banlist, reader psych, review  
samples/ — real human text by genre (SOURCES.md)  
assets/ — banner  

Samples from Gutenberg, PLOS (CC BY), Enron public, NUS SMS excerpts. Licenses on the files.

## License

MIT for skill/rules. Samples keep header licenses.
