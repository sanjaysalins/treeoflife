# Tree of Life - Holistic Wellness Website

## Overview

A static website promoting holistic health and wellness through eight interconnected pillars: Food & Nutrition, Exercise, Sleep & Rest, Mental Health, Family, Community, Environment, and Spiritual. The site educates visitors on "whole-person wellness" — nurturing body, mind, and spirit.

Built on the BootstrapMade "QuickStart" template, customized with a nature-inspired green theme.

## Tech Stack

- **HTML5** — semantic markup, no frontend framework
- **CSS3** — custom properties for theming, Bootstrap 5.3.8 grid/components
- **Vanilla JavaScript** — no build tools, no npm/yarn
- **PHP** — basic contact and newsletter form handlers (require a PHP server)
- **Vendor libraries** (all vendored in `assets/vendor/`): Bootstrap 5.3.8, Bootstrap Icons, AOS (scroll animations), GLightbox, Swiper (carousels), PHP Email Form

## Project Structure

```
index.html                  # Main landing page (hero, health wheel, subject cards, contact)
service-details.html        # Service detail template page
starter-page.html           # Blank starter template
topics/
  whole-foods.html          # Food & Nutrition topic page
  resistance-training.html  # Exercise topic page — beginner 3-day push/pull resistance program
  walking.html              # Exercise topic page
  flexibility.html          # Exercise topic page — daily movement & worship plan (mobility, strength, Ruach)
  sleep-hygiene.html        # Sleep & Rest topic page — circadian rhythm, sleep hygiene, and biblical rest
assets/
  css/main.css              # All custom styles (~2,370 lines), CSS variables at top
  js/main.js                # All custom JS (~210 lines)
  img/                      # Images (logo, favicon, hero, features, about, services, tabs)
  vendor/                   # Third-party libraries (do not modify)
  scss/                     # SCSS placeholder (pro version only, not used)
forms/
  contact.php               # Contact form handler
  newsletter.php            # Newsletter subscription handler
```

## Deployment

- Pushing to `main` on GitHub auto-deploys to Netlify: https://treeoflife-org.netlify.app/
- No build step — Netlify serves the static files directly

## Running Locally

No build step required. Either:
- Open `index.html` directly in a browser (forms won't work)
- Run `php -S localhost:8000` from the project root for full functionality including PHP forms

## Key Components & Patterns

### Health Wheel (`index.html`)
- Desktop: 8 wellness pillars arranged in a circle using JS-calculated positioning
- Mobile: falls back to a 2-column grid layout
- Logic in `assets/js/main.js` — look for the circular positioning section

### Subject Cards
- Collapsible sections (one per wellness pillar) using Bootstrap collapse
- Chevron icons rotate based on `aria-expanded` state
- Each card contains links to topic pages in `topics/`
- Anchor IDs (e.g., `#exercise`) are on the `col-lg-6` wrapper divs, with `scroll-margin-top` to clear the sticky header

### Topic Pages
- Live in `topics/` directory (e.g., `topics/whole-foods.html`, `topics/resistance-training.html`)
- Use relative paths (`../assets/`) for shared CSS/JS/images
- Follow the same header/footer structure as the main page
- Left sidebar contains: category topic list (with current page marked `.active`), Biblical Perspective box, and Help/Contact box
- **Only 5 topic pages exist so far** — `index.html` links to ~36 topic pages across all 8 pillars, but most are not yet created (links will 404)
- Existing topic pages:
  - Food & Nutrition: Whole Foods (whole-foods.html)
  - Exercise: Resistance Training, Walking, Mobility & Flexibility (3 pages)
  - Sleep & Rest: Sleep Hygiene & Circadian Rhythm (1 of 4 planned — Sabbath Rest, Power of Napping, Digital Detox are linked but not yet created)

### Navigation
- Fixed header with scroll state changes (~100px tall)
- Mobile hamburger toggle
- Scrollspy for active link highlighting
- `scroll-behavior: smooth` enabled globally; `scroll-margin-top` on sections (100px desktop, 66px mobile) and subject card anchors (120px desktop, 80px mobile) to offset the sticky header
- Hash scroll correction on page load via JS `setTimeout` in `main.js` (lines 142-156)

## CSS Theming

Key CSS variables are defined at the top of `assets/css/main.css`:
- `--accent-color: #2D5016` — forest green, used for buttons/links
- `--heading-color: #2D3B1A` — dark green for headings
- `--default-font: "Roboto"`, `--heading-font: "Nunito"`, `--nav-font: "Inter"`

To change the color scheme, update these variables.

### Custom CSS Components (added beyond template)
- `.biblical-box` — styled quote box for Scripture references
- `.tips-grid` / `.tip-card` — card grid for workout steps, tips, etc.
- `.related-topics` — pill-style links at the bottom of topic pages
- `.journal-section` / `.journal-field` / `.journal-line` — printable journal prompt with fill-in lines
- `.btn-accent` — green accent button (used for Print Journal)
- `@media print` — hides header/footer/nav, styles journal for clean printing

## Conventions

- **No build tools** — edit HTML/CSS/JS files directly
- **Vendor files** in `assets/vendor/` should not be modified
- **BEM-like naming** for custom components (e.g., `subject-card`, `subject-card-header`)
- **Bootstrap utilities** used throughout for spacing, layout, visibility
- **Mobile-first** responsive approach
- New topic pages go in `topics/` and follow the structure of existing pages in the same category (e.g., `walking.html` for Exercise)
- Images use WebP where possible for optimization

## Adding New Content

### New topic page
1. Copy an existing topic page as a template (`topics/whole-foods.html` for Food & Nutrition, `topics/walking.html` for Exercise)
2. Update the content, title, meta description/keywords, and breadcrumb
3. Link to it from the appropriate subject card in `index.html`
4. Update the sidebar topic list in **all** pages within the same category (each page has a sidebar listing all sibling topics)
5. Add to the Related Topics section at the bottom of sibling pages

### New wellness pillar (subject card)
1. Add a new card section in `index.html` following the existing pattern
2. Add a corresponding item to the health wheel
3. Update the JS circular positioning if the item count changes
