# The Birthmark Standard Foundation website

Source for https://birthmarkstandard.org.

## Layout

A standard Hugo site at the repository root.

- `content/`: the pages (`_index.html`, `how-it-works.html`, `research.html`, `foundation.html`).
- `layouts/`: templates and partials, including the figure icon sprite (`partials/bm-sprite.html`).
- `static/`: files copied as they are.
  - `css/`: `styles.css`, `figures.css`, `technical-detail.css`.
  - `images/`: logos and the founder photo.
  - `org/`: the Governance Charter.
  - `CNAME`, `favicon.ico`.
- `archetypes/`: Hugo's template for new content.
- `public/`: Hugo's output. It is not committed. The GitHub Actions workflow builds and deploys it on every push to `main`.

## Build

Hugo 0.139.0 extended.

```
hugo --minify
```

Output goes to `public/`. Run `hugo server` for a local preview.

Everything in `content/` and `static/` is public at birthmarkstandard.org. Do not put working documents there.

## Related repositories

- [Protocol](https://github.com/Birthmark-Standard/Protocol): the architecture, the ProVerif models and the simulation.
- [Prototype](https://github.com/Birthmark-Standard/Prototype): the earlier Raspberry Pi prototype and its documents. Kept for reference.
