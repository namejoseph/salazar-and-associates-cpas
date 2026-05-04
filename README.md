# Salazar & Associates, CPAs — Static Website

Static HTML/CSS/JS recreation of [salazarcpas.com](https://salazarcpas.com), migrated from WordPress to GitHub Pages.

## Structure

```
/
├── index.html              # Home
├── location/index.html     # Location page
├── irs-resources/          # IRS Resources page
├── staff/index.html        # Staff page
├── contact/index.html      # Contact page
└── assets/
    ├── css/styles.css      # All styling
    ├── js/script.js        # Mobile menu + scroll-to-top
    └── images/             # (drop real photos in here)
```

## External dependencies (loaded via CDN)
- **Font Awesome 6.5** — icons (`fas fa-*`)
- **Google Fonts** — Montserrat
- **Adobe Fonts (Typekit)** — Futura PT
- **Google Maps** — embed iframe for `506 Heartwood Dr, Austin, TX 78745`

## Brand colors
| Use | Hex |
| --- | --- |
| Navy (primary)  | `#253D8C` |
| Gold (accent)   | `#FFC60B` |
| Cream (bg)      | `#FCF6DB` |
| Light blue      | `#C7EAFB` |
| Dark gray       | `#414042` |

## Replacing placeholder images

All photos currently use `https://placehold.co/...` URLs. To swap in real photos:

1. Drop optimized JPG/PNG files into `assets/images/`.
2. Search the HTML files for `placehold.co` and replace each `src="..."` with `src="/assets/images/your-file.jpg"`.

Filenames you'll likely want to provide:
- `header-bg.jpg` (used as the dark-overlaid hero in `assets/css/styles.css`)
- `tax-preparation.jpg` (home page services photo)
- Staff photos: `diana.jpg`, `isaac.jpg`, `micaela.jpg`, `jessica.jpg`, `jose.jpg`, `frances.jpg`

## Deploying to GitHub Pages

1. Create a GitHub repo (e.g. `salazarcpas`).
2. Push these files to the `main` branch:
   ```bash
   git add .
   git commit -m "Initial static site"
   git push origin main
   ```
3. Repo → **Settings → Pages** → set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. (Optional, for custom domain) Create a `CNAME` file in the repo root with the value `salazarcpas.com`, then point your DNS A records at GitHub's IPs and add a `CNAME` for `www`.

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```
