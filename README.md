# Salazar & Associates, CPAs — Static Website

Static HTML/CSS/JS recreation of [salazarcpas.com](https://salazarcpas.com), migrated from WordPress to GitHub Pages.

## Structure

```
/
├── index.html              # Home
├── 404.html                # Custom not-found page
├── location/index.html     # Location page
├── irs-resources/          # IRS Resources page
├── staff/index.html        # Staff page
├── contact/index.html      # Contact page
├── robots.txt              # Allows all crawlers, points to sitemap
├── sitemap.xml             # XML sitemap of all pages
└── assets/
    ├── css/styles.css      # All styling
    ├── js/script.js        # Mobile menu + scroll-to-top + dynamic year
    ├── images/             # Photos
    └── favicon/            # Favicons + web manifest
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

## Images

All site photos live in `assets/images/`. Current files in use:
- `salazarcpas-website-header-photo.jpg` — header hero (referenced from CSS)
- `salazarcpas-website-img-calculator.jpg` — home page services photo
- `salazarcpas-website-officephoto1.jpg`, `salazarcpas-website-officephoto9.jpg` — location page
- `salazarcpas-website-staff-{diana,isaac,micaela,jessica,jose,frances}.jpg` — staff page

## Favicon / web manifest

Favicon set lives in `assets/favicon/` (generated via [realfavicongenerator.net](https://realfavicongenerator.net)):
- `favicon.ico`, `favicon.svg`, `favicon-96x96.png`, `apple-touch-icon.png`
- `web-app-manifest-192x192.png`, `web-app-manifest-512x512.png`
- `site.webmanifest`

## SEO / metadata

Every page includes:
- Canonical URL, description, theme-color
- Open Graph + Twitter Card tags (with `og:image` pointing to the header photo)
- Favicon set + apple-mobile-web-app-title

The home page (`index.html`) additionally includes a JSON-LD `AccountingService` schema with address, phone, email, and opening hours.
