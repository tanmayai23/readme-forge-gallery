# readme-forge gallery

The website for [readme-forge](https://github.com/tanmayai23/README-Editor-skill), a Claude skill that writes READMEs from your code and checks every command, env var and path in them against the repo.

**Live site:** https://readme-forge-gallery.vercel.app/

It shows every banner style, full README design, profile style and before/after example that readme-forge makes, plus READMEs people have made with it.

## Add your README to the gallery

The gallery's data lives in the main repo, not here: [`gallery/gallery.json`](https://github.com/tanmayai23/README-Editor-skill/blob/main/gallery/gallery.json). To add your README, follow [the steps in the main repo](https://github.com/tanmayai23/README-Editor-skill/blob/main/gallery/README.md). Once your pull request is merged there, your README appears on this site; nothing needs to change here.

## How the site works

Static files with no build step and no dependencies:

| File | What it does |
|---|---|
| `index.html` | The page |
| `style.css` | The design: light and dark themes from one set of tokens, sticky nav, product-window hero, gallery cards, responsive layout |
| `app.js` | Loads `gallery.json` from the main repo and renders the gallery, filters, search and detail view; also the theme toggle and hero tabs |
| `assets/icon.svg`, `favicon.ico` | The readme-forge mark, copied from `.github/assets/brand/` in the main repo |
| `assets/readme-hero-*.svg` | The main repo's README hero card, shown in the hero's README.md tab |

Vercel deploys the `main` branch as it is on every push. To preview it locally, serve the folder with any static server, for example `python -m http.server`, and open http://localhost:8000.

## License

[MIT](LICENSE)
