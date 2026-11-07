# joelint.com

Personal portfolio site for Joe Lint - technologist, marketer, and product builder from Detroit.

**Live site:** [joelint.com](https://joelint.com)

## What's in here

Single-page portfolio built with vanilla HTML, CSS, and JavaScript. No frameworks, no build tools, no dependencies - just one `index.html` file with everything inline.

### Sections

- **Hero** - intro, availability status, and contact links
- **Story** - background and career narrative with animated speech bubble
- **Work** - detailed job history with interactive case studies, before/after comparisons, and animated stat counters
  - The Peninsular Company (Founder, Sept 30, 2026-present): a Belle Isle lake strip with a blinking lighthouse and a passing freighter
  - Lotus International (Business Development & Marketing Specialist, April 2026-present): a part drawing that drafts itself in
  - DuMouchelles (Technology & Marketing Manager, 2021-2025)
  - Proactive Technology Management (IT Engineer > Team Lead, 2017-2021)
- **Travel** - 8-month solo backpacking trip across 30 countries with interactive 3D globe (desktop) and SVG world map (mobile), photo gallery with lightbox, and pilgrimage credentials
- **Projects** - the personal, less buttoned-up apps (the company ventures live on [thepeninsularcompany.com](https://thepeninsularcompany.com#art))
  - [Fortjort](https://joelint.com/apps/fortjort/) - one-thumb medieval kingdom builder
  - [Inkblotter](https://thepeninsularcompany.com/app/inkblotter/) - the ink blot test you fold
  - [Learn to Play Cards](https://learntoplaycardsapp.com) - 21 card games in 130 lessons
  - [The Ollin Tuner](https://ollintuner.com) - an Aztec oracle that is really a magic trick
  - [WorldSimulator](https://worldsimulator.vercel.app) - 5,000 years of history on one map (public beta)
  - Shell RIDE - portfolio piece (Lotus International), the SR-5S scooter companion app
  - [Detroit Air Survey](https://joelint.com/apps/detroit-air-survey/) - 1949-1967 aerial film over the modern city
  - [The Converter](https://joelint.com/apps/the-converter/) - portfolio piece, open-source Mac file converter
- **Skills** - terminal-style skill display with Google Digital Marketing & E-commerce certificate
- **Now** - what I'm looking for next

### Interactive features

- 3D globe visualization with visited country highlighting (globe.gl)
- SVG world map fallback on mobile with visited countries marked
- Scroll-triggered reveal animations via Intersection Observer
- Animated count-up stat counters
- Terminal-style typing effect in skills section
- Photo lightbox with keyboard navigation
- Collapsible case study sections
- Contact form via Formspree, guarded by Cloudflare Turnstile (widget "Formspree contact forms", shared with thepeninsularcompany.com and the Fortjort support page; Formspree holds the secret key)

## Tech stack

| Layer | What |
|-------|------|
| Markup | HTML5, single file |
| Styles | CSS3 (custom properties, grid, flexbox), all inline |
| Scripts | Vanilla JavaScript, all inline |
| Fonts | Instrument Serif, DM Sans, JetBrains Mono (Google Fonts) |
| Globe | globe.gl + three.js (lazy loaded, desktop only) |
| Analytics | Google Analytics (gtag.js) |
| Forms | Formspree |
| Hosting | GitHub Pages |
| Domain | joelint.com (via CNAME) |

## File structure

```
.
├── index.html                    # the whole site
├── CNAME                         # custom domain config
├── sitemap.xml                   # SEO sitemap
├── og-image.jpg                  # social media preview image
├── favicon.png                   # site favicon
├── resume.pdf                    # downloadable resume
├── Joseph_Lint_Headshot.jpg      # profile photo
├── world-map-mobile.svg          # flat world map for mobile
├── heirloom-icon.png             # Heirloom app icon
├── ollintuner-icon.png           # Ollin Tuner app icon
├── learntoplaycards-icon.png     # Learn to Play Cards app icon
├── fortjort-icon.png             # Fortjort app icon
├── inkblotter-icon.png           # Inkblotter app icon
├── shellride-icon.png            # Shell RIDE app icon
├── dumoart.com_old.png           # DuMo before screenshot
├── dumoart.com_new.png           # DuMo after screenshot
├── dumouchelles-logo-new.svg     # DuMo logo (new)
├── dumouchelles-logo-old.svg     # DuMo logo (old)
├── proactive_logo.svg            # Proactive logo
├── dual_pilgrim.svg              # Dual Pilgrim badge
├── saint-james-way.svg           # Camino shell symbol
├── stamp-arrival-to-thailand.svg # passport stamp decoration
├── stamp-return-to-usa.svg       # passport stamp decoration
└── travel/
    ├── camino_trail.jpeg
    ├── spanish_landscape.jpeg
    ├── kumano_kodo.jpeg
    ├── tibet_yak.jpeg
    └── fisterra_sunset.jpeg
```

## Local development

Open `index.html` in a browser. That's it.

For the 3D globe to load properly you may need a local server due to CORS on the world atlas data:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deployment

Pushes to `main` deploy automatically via GitHub Pages. Custom domain is configured through the `CNAME` file.
