# luxel-web

Landing page and privacy policy for [Luxel: Daily Light Puzzle](https://play.google.com/store/apps/details?id=app.luxel), hosted on GitHub Pages.

| Path | Content |
| --- | --- |
| `/` and `/cs/` | landing page (en, cs) |
| `/privacy/` and `/cs/privacy/` | privacy policy (en, cs) – linked from the app (`Links.PRIVACY_POLICY`) and Play Console |
| `/app-ads.txt` | AdMob authorized sellers (live copy at the domain root, see below) |

Plain static HTML, no build step. Screenshots in `img/` come from `docs/store` in the app repository (Roborazzi `StoreGraphicsTest`), resized to 540×960 WebP.

## Publish

1. `gh repo create RuzickaOnd/luxel-web --public --source=. --remote=origin --push`
2. **Settings → Pages** → Source **Deploy from a branch**, branch `main`, folder `/ (root)` → Save.
3. The site is at `https://ruzickaond.github.io/luxel-web/`.

## app-ads.txt

AdMob reads `app-ads.txt` only from the **root of the domain** of the developer website in the Play listing, so the
copy here is not the one AdMob uses. The live file is in the user site repository
[`RuzickaOnd/ruzickaond.github.io`](https://github.com/RuzickaOnd/ruzickaond.github.io), served at
`https://ruzickaond.github.io/app-ads.txt`. Keep both copies the same; with a custom domain this copy becomes the live one.

If the domain changes, update `Links.WEB` in the app, `sitemap.xml`, `robots.txt` and the canonical links.
