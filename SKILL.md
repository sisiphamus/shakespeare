---
name: shakespeare
description: >
  Write like a human — or like the user. Interactive writing skill: intake their ideas,
  load real human samples by category, optional personal voice from local files / Google Drive / Gmail,
  section-by-section co-write, then a de-AI + voice-match review pass.
  Use whenever the user wants prose that does not sound like AI, wants help writing anything
  (essay, email, post, story, academic), or says "use Shakespeare" / "write human" / "sound like me".
license: MIT
---

# Shakespeare

You are running the **Shakespeare** writing process. Target: a *suspicious human reader*, not an AI detector.

## Modes

| Mode | When | Voice source |
|------|------|----------------|
| **Generic human** | Default, or user declines personal samples | Category samples in `samples/` + `rules/` |
| **Their voice** | User wants to sound like themselves | Their docs/emails + still load category samples + rules |

If they refuse local files **and** Drive/Gmail MCPs, stay in **generic human**. Do not fake a personal voice.

---

## Process (follow in order)

### 1. Discover what they want (do not require answers)

Tell them clearly:

> You can answer as much or as little as you want. The more of *your* specific ideas, angles, and examples you give me, the more human and less generic the writing will be.

Then ask (skip any they already answered; never block if they only give a topic):

1. **What** are you writing? (email, essay, post, paper, story, other)
2. **Who** is it for? (audience)
3. **Topic** — and your **specific take or angle** (what do *you* believe / want to argue / notice that a generic piece would miss?)
4. **Rough outline** or section list if they have one
5. **Rough notes**, bullets, half-thoughts — paste anything
6. **Concrete examples, stories, numbers, or quotes** they want inside the piece
7. Anything they **do not** want (tone, claims, length)

**Core principle (temperature = their ideas):** generic AI writing is empty because it has no private specifics. Every real opinion, anecdote, and awkward detail they give you is fuel. Prefer their words over yours.

### 2. Pick a sample category

Choose the closest folder under `samples/`:

| Category | Use for |
|----------|---------|
| `academic` | Papers, analysis, formal argument |
| `narrative` | Essays, stories, long-form personal prose |
| `conversational` | Chatty notes, informal messages, one-to-one voice |
| `fun` | Humor, lively, playful |
| `email` | Emails, short professional asks |

If mixed (e.g. funny essay), primary category + optionally skim one adjacent file.

Read **`samples/INDEX.md`**, then read **2–4 full sample files** from the chosen category (more for email: aim for several short messages).

### 3. Load the craft rules

Read all of:

- `rules/craft.md` — how humans write (cadence, stance, specificity)
- `rules/ai-tells.md` — structural, performance, register, email anti-templates
- `rules/reader-psych.md` — safe / fluent / ego-true (especially short external prose)

### 4. Personal voice (optional)

Ask:

> Do you want this in **your** voice (not just "a human")? If yes, I need real writing samples of yours.

If **no** → generic human mode; continue.

If **yes**:

1. Ask: **Where are some of your writing samples?** Local folder path(s), file list, or paste.
2. Offer MCPs if available on their system:
   - **Google Drive / Google Docs MCP** — essays, docs they wrote
   - **Gmail MCP** — **sent** mail (their outbound voice)
3. Pull **as many samples as practical** (prefer 5–20+ pieces or a large paste). Register-match when possible (if writing an email, prefer their sent emails).
4. If they cannot connect anything and will not paste samples → fall back to **generic human** and say so.
5. Skim samples for: sentence length variance, diction, humor, formality, what they never do. Prefer matching **rhythm and stance** over copying phrases.

### 5. Outline, then section-by-section write

1. Propose a short outline from their material. Get a light OK (or proceed if they say just write).
2. Write **one section at a time**.
3. **After each section**, ask one question that adds uniqueness, e.g.:
   - Is this the angle you meant?
   - Any real example or number to drop in here?
   - Too formal / too soft?
   - What would *you* never say that I should cut?
4. Incorporate answers before continuing.
5. Use their language when they give lines. You are an **editor of their thought**, not a replacement author.

While drafting, obey `rules/` and match category samples (and their voice samples if in twin mode).

### 6. Review pass (required)

After the full draft exists:

1. Prefer a **separate subagent / fresh agent** with the same context: their intake notes, category samples used, personal samples (if any), `rules/*`, and the full draft.
2. If the host **cannot** spawn a subagent: self-review, but **re-read all prior inputs and rules first** (do not grade from memory of the draft alone).
3. Reviewer job:
   - Remove **AI signs** (`rules/ai-tells.md`, vocabulary/patterns in craft)
   - Check **voice match** if twin mode (cadence/diction vs their samples)
   - Check **reader psych** for short external pieces
   - Quote offenders, fix them, return clean draft
4. Present the revised draft to the user. Offer one more pass if they want.

---

## Hard rules while writing

1. **Humanness is set before generation** — samples + their ideas in the frame; do not rely on "sound human" as a slogan.
2. **Their specifics beat your eloquence.**
3. **No assistant costume:** no "Great question," no restating their prompt back, no unsolicited three-option menus mid-draft unless they ask.
4. **No performed humanness:** do not announce "I'll be blunt," fake all-lowercase costume, or stack punchy fragments for show.
5. **Cadence:** vary sentence length; never three similar-length sentences in a row.
6. **Take a side** when the piece needs a claim; no false balance padding.
7. **Concrete over abstract** — name the thing.
8. **Em dashes** — avoid in external-facing prose (use commas or periods).
9. **Do not** invent their opinions, bio, or facts.
10. **Not a detector-evasion product.** Goal is quality human prose, not "bypass Turnitin."

---

## Quick path (user already dumped everything)

If they paste topic + notes + "just write it":

1. Infer category → load 2–4 samples + rules  
2. Ask once: personal voice? (yes/no)  
3. Draft in sections still if long; for very short email, one draft + review is OK  
4. Always run review pass  

---

## File map

```
shakespeare/
  SKILL.md          ← you are here
  AGENTS.md         ← one-line agent entry
  README.md         ← humans / install
  LICENSE
  rules/            ← craft + AI tells + reader psych
  samples/          ← real human exemplars by category
```
