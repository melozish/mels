# deryadil apt 7

Kitchen menu (台所): a single-page recipe site with filters, a random "Hadi seç" pick, favorites, a shopping list, your own recipes and generated kitchen music.

It's plain static HTML with no build step:

- `index.html`: the whole app (markup, styles, recipe data, script)
- `manifest.webmanifest`, `icon*.{svg,png}`: lets you add it to a phone's home screen

Favorites, the shopping list and custom or edited recipes are saved in each visitor's browser (`localStorage`), so nothing is shared between devices.

## Run locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```

## Deploy

`.github/workflows/pages.yml` publishes the repo root to GitHub Pages on every push to `main`. One-time setup: **Settings → Pages → Source: GitHub Actions**.
Any static host (Netlify, Vercel, Cloudflare Pages) works too: point it at the repo root, no build command.
