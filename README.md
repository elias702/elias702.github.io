# Elias Ahmed — Portfolio

Personal developer portfolio for Python backend engineering, web scraping, automation, ETL pipelines, and full-stack product development.

## Live Website

- **Canonical URL:** [https://elias702.github.io/](https://elias702.github.io/)

---

## Professional Positioning

- **Role:** Python Backend Developer & Automation Engineer
- **Core Message:** *"I build systems that turn data into useful products."*
- **Primary Pillars:**
  - Backend Engineering (Python, FastAPI, Django, REST APIs)
  - Data & Web Scraping (Playwright, Scrapy, Selenium, Headless Browsers)
  - Automation & ETL (Data extraction, transformation, CSV/JSON pipelines)
  - Full-Stack Product Development (Next.js, React, TypeScript, Tailwind CSS)
  - SEO / GEO (Technical SEO, Generative Engine Optimization, Structured Data)

---

## Featured Commercial Experience

1. **EconoMed (UK)** — End-to-end medical product data extraction, Shopify API integration, and custom storefront development.
2. **Mobiorbit** — Ongoing contributions to product-specification directories across data acquisition, structured content operations, and SEO/GEO.
3. **IC交易网 (IC Trading Network)** — Weekly automated data-extraction workflow collecting electronic-component marketplace data (~10,000–15,000 records per weekly run).
4. **Wingontravel** — Travel platform data automation covering flights, hotels, and custom database integration.

---

## Selected Products

1. **School Management System** *(in development)* — Full-stack academic and administrative operations platform covering student management, admissions, attendance, fees, exams, and routines.
2. **SeoLens** *(planned concept)* — AI-powered SEO & GEO intelligence platform for search and AI-engine discoverability.
3. **Riveata** *(planned concept)* — Solar intelligence and solutions discovery platform.

Product statuses above mirror the labels rendered on the live site.

---

## Architecture & Deployment

This portfolio is a zero-build-dependency static site: there is no bundler, no package manifest, and no CI step. GitHub Pages serves the repository root directly.

### Repository Files

| File | Purpose |
| --- | --- |
| `index.html` | The entire site — markup, all CSS in one `<head>` `<style>` block, and the vanilla JS at the end of `<body>`. |
| `404.html` | Custom not-found page served automatically by GitHub Pages. |
| `cv.html` | Print-first curriculum vitae; save as PDF from the browser print dialog. |
| `og-image.png` | 1792×1024 social share card referenced by `og:image` and `twitter:image`. |
| `robots.txt` | Crawler directives plus the sitemap location. |
| `sitemap.xml` | Sitemap for the homepage and the CV page. |

### Technical Notes

- **Markup & Layout:** Semantic HTML5 with a skip link, `aria-expanded`/`aria-controls` on the mobile drawer, `aria-live` status for the copy-to-clipboard action, and Escape-to-close with focus return.
- **CSS:** Self-contained design tokens, dark-first near-black theme with lime/emerald accents, and `prefers-reduced-motion` handling. No client-side compilation.
- **JavaScript:** Minimal vanilla JS — mobile drawer toggling and one-click email copying. No framework, no dependencies.
- **Fonts:** Inter and JetBrains Mono are loaded from the **Google Fonts CDN** (`preconnect` + `display=swap`, with system-font fallbacks). This is the only third-party request the page makes.
- **Metadata:** Open Graph tags, Twitter Card (`summary_large_image`), and Schema.org JSON-LD covering `ProfilePage`, `WebSite`, `Person`, `CreativeWork`, and `SoftwareApplication` entities.

### Run Locally

Open `index.html` directly in a browser, or serve the directory so relative paths and the 404 behave like production:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

### Deploy to GitHub Pages

Push to the default branch — no build command is required. In **Settings → Pages**, the source must be *Deploy from a branch* with the root of the default branch selected, so `index.html`, `404.html`, `og-image.png`, `robots.txt`, and `sitemap.xml` are all served from `/`.

After changing page content, update `<lastmod>` in `sitemap.xml`.
