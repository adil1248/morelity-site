# morelity.com — build & deploy

Static site. Tailwind CSS v4 is compiled into `assets/css/site.css`; fonts and the
logo are vendored into `assets/`. No CDN, no analytics, no trackers at runtime.

## Build

```bash
npm install
npm run build     # tailwindcss -i src/input.css -o assets/css/site.css --minify
```

Preview locally:

```bash
python3 -m http.server 8899
# http://127.0.0.1:8899/index.html
```

## Deploy

The published repo is `adil1248/morelity-site`. GitHub Pages is already enabled
(legacy build, source `main` / root) and `CNAME` is `morelity.com`.

```bash
git push origin main
```

Because a custom domain is configured, `https://adil1248.github.io/morelity-site/`
redirects to `morelity.com`. The site will not resolve publicly until morelity.com
DNS is repointed at GitHub Pages — that is handled in a separate domain-recovery
lane.

## Brand assets

`assets/img/*` are extracted from Morelity's own 2017–2018 sales collateral
(`Morelity presentation.pptx`, media/image3.png). The palette in `src/input.css`
is sampled from that artwork; `#893d97` matches the `theme-color` recorded on the
archived 2016 morelity.com snapshot.
