# URfit - Project Guide

## What is this?

A Hugo static site for URfit, a bootcamp and lifestyle coaching business in Urmond (NL). Hosted on Netlify at https://urfit.nu/.

## Commands

- `hugo server -D` — local dev server at localhost:1313
- `hugo --gc --minify` — production build (also the Netlify build command)
- `netlify deploy` — deploy draft to Netlify
- `netlify deploy --prod` — deploy to production

## Key Files

| What | Where |
|---|---|
| Site config | `config.toml` |
| Build/deploy config | `netlify.toml` |
| Page content | `content/*.md` and `content/post/*.md` |
| Contact info, phone, address, KVK | `data/nl/contactinfo.yaml` |
| Navigation menu items | `data/nl/nav.yaml` |
| Social media links | `data/nl/social.yaml` |
| Homepage intro text | `data/nl/intro.yaml` |
| Translations / UI strings | `themes/urfit/i18n/nl.toml` |

## Theme Structure (`themes/urfit/`)

| What | Where |
|---|---|
| Homepage layout | `layouts/index.html` |
| Single page layout | `layouts/_default/single.html` |
| Header / meta tags | `layouts/partials/htmlhead.html` |
| Navigation | `layouts/partials/nav.html` |
| Footer (contact form + info) | `layouts/partials/footer/index.html` |
| Copyright bar | `layouts/partials/copyright.html` |
| SCSS styles | `assets/scss/` (compiled by Hugo Pipes) |
| JavaScript | `assets/js/` (jQuery-based) |

## Content

- The site is in Dutch (`nl`). All content files use Dutch text.
- Pages are Markdown files in `content/`. The homepage pulls posts from `content/post/`.
- The contact form is a Netlify Form with honeypot spam protection and reCAPTCHA.

## CLI Tools

### GitHub CLI (`gh`)

- `gh pr create --title "..." --body "..."` — create pull request
- `gh pr list` — list open PRs
- `gh pr view` — view current PR details
- `gh issue list` — list open issues
- `gh issue create --title "..." --body "..."` — create issue

### Netlify CLI (`netlify`)

- `netlify status` — show linked site and account info
- `netlify build` — run build locally using netlify.toml config
- `netlify deploy` — deploy draft (preview URL)
- `netlify deploy --prod` — deploy to production (urfit.nu)
- `netlify api listSiteDeploys --data '{"site_id": "7a227b83-5fa5-4efc-b468-169e48d00a0b"}'` — list recent deploys and their status

## Common Tasks

- **Change contact info / address / phone:** edit `data/nl/contactinfo.yaml`
- **Change social media links:** edit `data/nl/social.yaml`
- **Add a new page:** create a `.md` file in `content/`
- **Change navigation:** edit `data/nl/nav.yaml`
- **Change footer text / credits:** edit `themes/urfit/i18n/nl.toml`
- **Change styling:** edit SCSS files in `themes/urfit/assets/scss/`
