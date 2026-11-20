# [https://jemini-io.github.io/whodo-pitch-deck/](https://jemini-io.github.io/whodo-pitch-deck/)

WhoDo pitch deck. A Reveal.js deck. Pushes to `main` update that URL.

Arrows move. F is fullscreen. S opens speaker notes.

## Local

```
npm install
npm start
```

Open http://localhost:4173.

## Layout

- `index.html` holds the slides. One `<section>` per slide, speaker notes in `<aside class="notes">`.
- `css/deck.css` holds the WhoDo brand tokens and slide layouts.
- `images/` holds slide art.

Reveal.js and the Fustat font load from the jsDelivr CDN, so GitHub Pages serves the repo as-is with no build.

This repo is public. Anything committed here is world-readable.
