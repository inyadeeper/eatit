# XexeX Records — Store Page

A custom, single-file landing page for [shanemickley.gumroad.com](https://shanemickley.gumroad.com), built for XexeX Records' two catalogs: **Gallows Ballads** (dark country / folk-horror) and the metal catalog.

No build step, no dependencies to install — it's one HTML file with inline CSS and JS.

## What's in the box

- `xexex-records.html` — the entire site (markup, styles, and scripts in one file)

## Running it locally

Just open the file in a browser:

```
open xexex-records.html
```

Or serve it so relative paths and fonts behave exactly like production:

```
npx serve .
```

## Before you deploy

Two placeholders need real values in `xexex-records.html`:

| Find | Replace with |
|---|---|
| `REPLACE-GALLOWS-BALLADS-SLUG` | Your Gallows Ballads product slug from Gumroad |
| `REPLACE-METAL-SLUG` | Your metal catalog product slug from Gumroad |

Also verify the follow form near the bottom of the page (`data-gumroad-follow`) actually submits once it's live — if Gumroad doesn't pick it up automatically, swap in the real subscribe embed snippet from your Gumroad **Widgets** page, or point the button at `shanemickley.gumroad.com/subscribe` instead.

## Deploying

Any static host works — this is plain HTML/CSS/JS:

- **Netlify / Vercel**: connect this repo, no build command needed, publish directory is the repo root
- **GitHub Pages**: Settings → Pages → deploy from the `main` branch, root directory
- Once live, you can point it at your Gumroad **custom domain** setting from the Gumroad dashboard

## Design notes

- **Fonts**: Rye (display), Spectral (body), Special Elite (ledger/utility text) — loaded from Google Fonts
- **Theme**: light/dark toggle in the top right, persisted in `localStorage`, defaults to the visitor's system preference
- **Signature element**: the rope running down the page lights up in 13 notches as you scroll — a nod to the thirteen-step gallows tradition behind "Thirteen Steps"
- Respects `prefers-reduced-motion` and keeps visible focus states for keyboard navigation

## License

All rights reserved — XexeX Records.
