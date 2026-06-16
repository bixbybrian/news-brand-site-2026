# NEWS brand site

Marketing site for the NEWS brand. Live at https://newsbrand.netlify.app/

## Structure

This repo separates the published site from project tooling:

- `site/` — **everything that gets published.** Netlify's publish directory (set in `netlify.toml`). Plain static HTML/CSS/JS and image assets, no build step.
- `netlify.toml` — Netlify configuration (publish directory = `site`).
- `docs/` — project notes and documentation. **Not published** (outside `site/`).
- `CLAUDE.md` — this file. **Not published** (outside `site/`).

Only the contents of `site/` are served to the public. Files at the repo root
(this file, `docs/`, `netlify.toml`) are kept in version control but never
appear on the live site.

## Deploy workflow

Netlify auto-deploys on every push to the `main` branch:

```bash
git add -A
git commit -m "describe your change"
git push
```

The site redeploys within a minute or two.

## Editing the site

- The home page is `site/index.html`.
- Image assets live in `site/images/`.
- Asset paths inside `site/` are relative, so keep files within `site/` when
  moving things around.
