# Agent instructions: WhoDo pitch deck

This repo is a Reveal.js pitch deck, published with GitHub Pages. Pushes to `main` publish live. The repo is public, so anything committed is world-readable.

## Who owns what

| File | Owner | Agent may edit? |
| --- | --- | --- |
| `slides.md` | Humans | **No.** Report problems, don't fix them. |
| `speaker-notes.md` | Humans | **No.** Report problems, don't fix them. |
| `index.html` | Generated from the two files above | Only by rebuilding it (see below). Never hand-edit. |
| `css/deck.css` | Shared | Yes, when asked. Keep the WhoDo brand tokens. |
| `images/` | Humans supply art | Only add files a human provided. Don't generate or download art. |
| `research-docs/` | Humans | Read freely. Write new research here only, and only when asked. Don't edit existing docs without asking. |
| `README.md`, `AGENTS.md` | Shared | Yes, when asked. |
| `package.json`, `.gitignore` | Shared | Only with approval. |

Anything not listed: ask before touching it.

## Source of truth

- `slides.md` holds the on-screen text and the picture direction for each slide.
- `speaker-notes.md` holds what the presenter says for each slide.
- Slides are numbered with `## N. Title` headings. The number is the join key between the two files.
- "On screen" text is the only text the room sees. Notes are what the presenter says.

## Rebuilding index.html

Run this only when a human asks to "catch the deck up" or "rebuild the slides." Don't rebuild on your own initiative.

1. Read `slides.md` and `speaker-notes.md`.
2. Check that the slide numbers and titles match between the two files. If they don't, stop and report the mismatch. Do not guess which slide is right.
3. For each slide, write one `<section>` in `index.html`:
   - On-screen text goes in a `<div class="frame ...">` using the existing layout classes in `css/deck.css` (`gradient`, `light`, `navy`, `blue`, `center`, `split`). Reuse the layouts already in use before inventing new ones.
   - Notes go in `<aside class="notes">`, one `<li>` per note line.
4. Picture direction: if the art is in `images/`, reference it. If it says "PHOTO TO COME" or the file is missing, leave the art container empty and list it in your report. Never invent an image path.
5. Put this comment at the top of the `<body>`: `<!-- GENERATED from slides.md and speaker-notes.md. Do not hand-edit; rebuild instead. -->`
6. Preview with `npm start` and open http://localhost:4173. Check that the slide count matches the source files.
7. Report what changed and anything unresolved. Don't commit.

## Git and publishing

- Never commit, push, or open a PR without explicit approval in the current turn.
- Never push to `main` without explicit approval. A push to `main` publishes the deck live.
- Before staging anything new, check that it doesn't contain internal material. The repo is public, and Pages serves every file in it.
- Keep new files out of the repo root. Research goes in `research-docs/`. Anything else new at the root needs approval first.
- Don't restore or re-add deleted files without asking. `talk.md` is deleted in the working tree on purpose; don't bring it back.

## Known state

- `slides.md` has slides 1 to 12. `speaker-notes.md` has 1 to 13 (13 is "Use of Funds"). Rebuilding must wait until a human resolves this.
- `index.html` is still the scaffold with placeholder slides. It doesn't match `slides.md` yet.
