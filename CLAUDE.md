# Website repository

This repository builds https://birthmarkstandard.org, the public site of The Birthmark Standard Foundation. It is a Hugo site. It holds no prototype code. The earlier prototype is in https://github.com/Birthmark-Standard/Prototype and the protocol work is in https://github.com/Birthmark-Standard/Protocol.

## Structure

- `website/content/`: pages are `.html` files with front matter. `figures: true` loads the figure sprite and `figures.css`. `extra_css` adds stylesheets. `url` sets the page address. `aliases` create redirect pages for old addresses (`technical-architecture.html`, `privacy-design.html`, `verify.html`, `investigation-framework.html`, `contact.html`, `governance.html`). Keep the aliases.
- `website/layouts/`: templates. The header, footer and figure sprite are partials.
- `website/static/`: copied as is. Stylesheets, logos, images, `CNAME`, blog admin.
- `docs/`: built output, committed. Never edit it by hand. Build with Hugo.
- Build: `cd website && hugo --minify`. Hugo 0.139.0 extended.

Everything under `docs/` and `website/static/` is public. Do not put working documents, drafts or internal notes there.

## Figures

- Figures are inline SVG inside `<figure class="bm-fig">`. Every class and variable is prefixed `bm-`.
- Audience colours: teal for photographers, amber for verifiers.
- Each figure has `role="img"`, an `aria-label` and a `<figcaption>`.
- Heading ids that other pages link to must stay: `registering`, `checking`, `editing`, `get-involved`.

## Writing rules for public copy

- Short declarative sentences. No hedging words such as "aims to", "seeks to", "hopes to" or "designed to". No em dashes. No filler.
- State each claim at the strength the papers support. The site must never give a guarantee the Protocol or Integration paper does not.
- Never conflate peer review and preprint status. The Integration paper is a preprint on arXiv and is not peer reviewed. Do not write "under review" or "peer reviewed" for the Protocol paper unless Sam gives the status.
- No GDPR or other legal-compliance claims unless a lawyer has confirmed them.
- No donation, tax-status or fiscal sponsorship wording except text supplied by Aspiration.
- Governance wording changes only when Sam supplies the text.
- Customer-facing pages do not mention relays, keys or server roles. Those belong in the "Technical detail" block and in the papers.
- Where information is missing, leave `<!-- TODO(Sam): ... -->` and say so in your report. Do not invent facts, numbers, dates, statuses or links.
