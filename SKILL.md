---
name: shakespeare
description: >
  Write like a human — or like the user. Intake their ideas, load real human samples by category,
  optional personal voice from local files / Drive / Gmail, section-by-section co-write, then de-AI review.
  Use for prose that shouldn't sound like AI, any writing help, or "use Shakespeare" / "write human" / "sound like me".
license: MIT
---

# Shakespeare

Target: a suspicious human reader, not a detector.

Two modes. Default is generic human (category samples + rules). "Their voice" only if they give real samples. No samples → stay generic. Don't invent a personal voice.

## Process

### 1. Discover (don't require answers)

Tell them: answer as much or as little as you want. More of *their* specifics = less generic.

Ask what's open (skip what they already said; topic-only is fine):
1. What (email, essay, post, paper, story…)
2. Who for — email: who→whom; essay: what the receiver expects at this stage
3. Topic + their actual take (what a generic piece would miss)
4. Outline if they have one
5. Notes / bullets / half-thoughts
6. Real examples, stories, numbers, quotes they want in (private grit — not invent-specific)
7. Anything they don't want

Core idea: temperature = their ideas. Private grit beats eloquence. Invented "vivid" still reads AI.

### 2. Sample category

Closest under `samples/`:
- academic — papers, formal argument
- narrative — essays, stories, long personal
- conversational — chatty notes, informal
- fun — humor / playful
- email — emails, short pro asks

Mixed → primary + maybe one adjacent file.

Read `samples/INDEX.md`, then 2–4 full files (email: several short ones).

### 3. Rules

Read all of: `rules/craft.md`, `rules/ai-tells.md`, `rules/reader-psych.md` (esp short external).

### 4. Personal voice (optional)

Ask if they want *their* voice. If no → generic.

If yes: where are samples? local path, paste, Drive/Docs MCP, Gmail sent. Pull a lot (5–20+ if you can). Prefer same register. Nothing available → say so, fall back to generic. Match rhythm/stance, don't copy phrases.

### 5. Outline then section write

Short outline, light OK (or just write if they said so). One section at a time. After each, one question for uniqueness (angle? real example? too formal? cut what they'd never say?). Use their lines. Editor of their thought, not replacement author.

Obey rules + match samples (and their voice if twin).

### 6. Review (required — no skip)

Full draft exists → re-check before return.

Prefer a fresh subagent with intake + samples used + personal samples + rules/* + full draft. No subagent: self-review only after re-reading rules/intake from disk, not draft memory alone.

Reviewer: kill AI signs, voice match if twin, reader psych for short external, quote offenders fix them, return clean draft. Offer another pass if they want.

## Hard rules while writing

1. Frame first (samples + their ideas). "Sound human" is not a method.
2. Their specifics > your eloquence. Private grit only.
3. No assistant costume: no Great question, no prompt restates, no menus mid-draft.
4. No performed humanness: no I'll be blunt, fake lowercase, punchy fragment stacks. No default short declarative openers (bare 4–8 word S–V–O para hooks).
5. No interest-bridges. No "the part/section/bit X". No definitional punches ("That joining is fusion."). No fake-plain gloss (shows up as / falls out as heat/light).
6. No sealed product (stock vignette kit, no-deep-lesson bow, multi-beat coach memo when short works).
7. Vary sentence length; never three similar in a row.
8. Take a side when needed; leave loops open when maxim isn't needed.
9. Em dashes: avoid in external prose.
10. Don't invent their opinions/bio/facts.
11. Not a detector-evasion product.

## Quick path (they dumped everything)

Infer category → 2–4 samples + rules → ask once personal voice? → draft (sections if long; short email can be one shot + review) → always review.

## Files

SKILL.md (here), AGENTS.md (entry + must-check), README.md, LICENSE, rules/, samples/
