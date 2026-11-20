# [https://jemini-io.github.io/whodo-pitch-deck/](https://jemini-io.github.io/whodo-pitch-deck/)

WhoDo pitch deck. A Reveal.js deck. Pushes to `main` update that URL.

Arrows move. F is fullscreen. S opens speaker notes.

## Local

```
npm install
npm start
```

Open http://localhost:4173.

## Workflow

- **Humans edit `slides.md` and `speaker-notes.md`.** That's where slide content and talking points live.
- **Ask an agent to "catch the deck up."** The agent rebuilds `index.html` from those two files. Don't hand-edit `index.html`; the next rebuild overwrites it.
- **Preview** with `npm start`, then check the slides in the browser.
- **Publish** by pushing to `main`. Agents don't push without your sign-off.

Agent rules are in `AGENTS.md`.

## Layout

- `slides.md` holds the on-screen text and picture direction for each slide.
- `speaker-notes.md` holds what the presenter says for each slide.
- `index.html` is generated from the two files above. Don't edit it by hand.
- `css/deck.css` holds the WhoDo brand tokens and slide layouts.
- `images/` holds slide art.
- `research-docs/` holds research and market sizing behind the deck. Keep new research docs here.

Reveal.js and the Fustat font load from the jsDelivr CDN, so GitHub Pages serves the repo as-is with no build.

This repo is public. Anything committed here is world-readable, and Pages serves every file in the repo root.
