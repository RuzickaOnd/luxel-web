# luxel-web

Landing page and privacy policy for [Luxel: Daily Light Puzzle](https://play.google.com/store/apps/details?id=app.luxel), hosted on GitHub Pages.

| Path | Content |
| --- | --- |
| `/` and `/cs/` | landing page (en, cs) |
| `/privacy/` and `/cs/privacy/` | privacy policy (en, cs) – linked from the app (`Links.PRIVACY_POLICY`) and Play Console |
| `/app-ads.txt` | AdMob authorized sellers – replace the placeholder publisher ID |

Plain static HTML, no build step. Screenshots in `img/` come from `docs/store` in the app repository (Roborazzi `StoreGraphicsTest`), resized to 540×960 WebP.

## Publish

1. `gh repo create RuzickaOnd/luxel-web --public --source=. --remote=origin --push`
2. **Settings → Pages** → Source **Deploy from a branch**, branch `main`, folder `/ (root)` → Save.
3. The site is at `https://ruzickaond.github.io/luxel-web/`.

## app-ads.txt

AdMob reads `app-ads.txt` only from the **root of the domain** of the developer website in the Play listing, so
`https://ruzickaond.github.io/luxel-web/app-ads.txt` is not enough. Either:

- buy a domain (e.g. `luxel.app`), add a `CNAME` file with it here and use `https://luxel.app` as the website in Play Console, or
- create the user site repository `RuzickaOnd/ruzickaond.github.io` with a copy of `app-ads.txt` at its root
  (served at `https://ruzickaond.github.io/app-ads.txt`).

If the domain changes, update `Links.WEB` in the app, `sitemap.xml`, `robots.txt` and the canonical links.
