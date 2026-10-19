# The Birthmark Standard Foundation website

Source for https://birthmarkstandard.org.

## Layout

- `website/`: the Hugo site.
  - `content/`: the pages (`_index.html`, `how-it-works.html`, `foundation.html`, `research.html`) and `blog/`.
  - `layouts/`: templates and partials, including the figure icon sprite (`partials/bm-sprite.html`).
  - `static/`: files copied as they are. CSS (`styles.css`, `figures.css`, `technical-detail.css`), logos, images, `CNAME` and the blog admin (`admin/`).
- `docs/`: the built site. Hugo writes it here and it is committed.

## Build

Hugo 0.139.0 extended.

```
cd website
hugo --minify
```

Edit `website/`. Do not edit `docs/` by hand.

Everything in `docs/` and `website/static/` is public at birthmarkstandard.org. Do not put working documents there.

## Related repositories

- [Protocol](https://github.com/Birthmark-Standard/Protocol): the architecture, the ProVerif models and the simulation.
- [Prototype](https://github.com/Birthmark-Standard/Prototype): the earlier Raspberry Pi prototype and its documents. Kept for reference.
