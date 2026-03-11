# URfit

Bootcamp en lifestyle coaching in Urmond e.o.

## Links

- Website: https://urfit.nu/
- Facebook: https://www.facebook.com/URfit.nu/

## Credits

Built by [Vincability](https://www.vincability.com) ([GitHub](https://github.com/vavdb))

## Tech Stack

- **Static site generator:** [Hugo](https://gohugo.io/)
- **Hosting:** [Netlify](https://www.netlify.com/)
- **Theme:** Custom theme based on [Massively](https://html5up.net/massively) by HTML5 UP
- **Styling:** SCSS (compiled via Hugo Pipes)
- **JS:** jQuery
- **Icons:** Font Awesome

## Local Development

```bash
hugo server -D
```

The site will be available at `http://localhost:1313/`.

## Deployment

Pushes to `main` trigger an automatic build and deploy on Netlify. Build settings are defined in `netlify.toml`.

## Project Structure

```
config.toml          # Hugo site configuration
content/             # Page content (Markdown)
data/nl/             # Structured data (contact info, social links)
static/              # Static assets (images, CSS, JS)
themes/urfit/        # Custom Hugo theme
netlify.toml         # Netlify build configuration
```
