# Bureau Veritas AVOH Marketing Website

Marketing website for the Bureau Veritas AVOH team (Acoustics, Vibration and Occupational Hygiene).

## Tech Stack

- **Astro** (static site generator) with **Tailwind CSS**
- Deployed to **GitHub Pages** via GitHub Actions (`ShetlandJ/rocco`)
- Live URL: https://shetlandj.github.io/rocco/
- No JS frameworks — pure static HTML output

## Site Structure

- `/` — Homepage with hero, service cards grid, "Why Choose BV", offices, contact CTA
- `/environmental-noise` — Environmental noise impact assessments
- `/occupational-noise` — Workplace noise assessments, NEMS
- `/pipework-vibration` — Vibration risk assessments, PSI screening, FEA
- `/aiv-fiv` — Acoustic & Flow Induced Vibration screening
- `/hand-arm-whole-body-vibration` — HAV & WBV assessments
- `/building-acoustics` — Architectural acoustics, sound insulation testing
- `/occupational-hygiene` — COSHH, LEV, IAQ, EMF, radon
- `/training` — Noise at Work, HAVS, pipework vibration courses
- `/contact` — Office locations, obfuscated email, phone

## Brand

- **Primary navy:** `#00049E` (header, contact CTA, copyright bar)
- **Lighter navy:** `#1a1fbd` (footer main content — sandwich effect)
- **Teal:** `#01B3C4` (CTAs, accents)
- **Accent:** `#7275FE`
- **Purple:** `#9185BE`
- **Dark text:** `#1D1D1B`
- **Font:** Arial (BV global template)

## Key Files

- `src/layouts/Layout.astro` — Base layout with nav, footer, SEO meta, JSON-LD, back-to-top
- `src/components/Hero.astro` — Hero section with background image
- `src/components/ServiceCard.astro` — Card for homepage grid
- `src/components/ContactSection.astro` — Contact CTA with obfuscated email
- `src/components/Breadcrumbs.astro` — Breadcrumbs for service pages
- `astro.config.mjs` — Astro config (`base: '/rocco/'`, sitemap integration)
- `tailwind.config.mjs` — BV brand colours and Arial font
- `.github/workflows/deploy.yml` — GitHub Pages deploy workflow

## Important Notes

- `base: '/rocco/'` — trailing slash is required, otherwise image paths break
- Email is obfuscated via JS string assembly in ContactSection to prevent scraping
- Images in `public/images/` are pre-optimized JPEGs from `data/Images/`
- Footer uses a "sandwich" pattern: dark navy CTA → lighter navy main footer → dark navy copyright

## Office Locations

- Glasgow
- Aberdeen
- Manchester
- London

## Contact

- Email: rocco.giudice@bureauveritas.com (obfuscated on site)
- Tel: 0345 600 1828

## Assets

Reference materials for services, SEO keywords, colour palettes, and styling are in `/data/`.
