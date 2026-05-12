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
  biblical-core-eating.html # Food & Nutrition topic page — four biblical eating patterns and the biblical plate
  fasting-detox.html        # Food & Nutrition topic page — fasting zones, bodily detox, and medical disclaimer
  hydration.html            # Food & Nutrition topic page — water, electrolytes, hydration by age, 12 hydrating foods (Ps 42:1-2 / John 7:38)
  mindful-eating.html       # Food & Nutrition topic page — intentional eating, 7 easy steps (1 Cor 10:31 / 1 Tim 4:4-5)
  resistance-training.html  # Exercise topic page — beginner 3-day push/pull resistance program
  walking.html              # Exercise topic page
  flexibility.html          # Exercise topic page — daily movement & worship plan (mobility, strength, Ruach)
  sleep-hygiene.html        # Sleep & Rest topic page — circadian rhythm, sleep hygiene, and biblical rest
  digital-detox.html        # Sleep & Rest topic page — screen-free bedtime and tech-free sleep sanctuary
  power-of-napping.html     # Sleep & Rest topic page — power nap benefits, cautions, and how-to guide
  stress-management.html    # Mental Health topic page — holistic stress management, embedded box & 3-7-8 breathing videos
  clean-living-spaces.html  # Environment topic page (first in pillar) — home as sanctuary, holistic benefits, 5 themed areas, stewardship, 6 practical tip-cards
CLIENT_BRIEFS.md            # Per-email brief tracker: deliverables → status → evidence (see "Client Brief Verification")
assets/
  css/main.css              # All custom styles (~2,475 lines), CSS variables at top
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
- **Only 10 topic pages exist so far** — `index.html` links to ~36 topic pages across all 8 pillars, but most are not yet created (links will 404)
- Existing topic pages:
  - Food & Nutrition: Whole Foods, Biblical Core Eating, Fasting & Detox, Hydration, Mindful Eating (**5 of 5 — pillar complete**)
  - Exercise: Resistance Training, Walking, Mobility & Flexibility (3 pages)
  - Sleep & Rest: Sleep Hygiene & Circadian Rhythm, Digital Detox, Power of Napping (3 of 4 planned — Sabbath Rest is linked but not yet created)
  - Mental Health: Stress Management (1 of 5 — Meditation & Prayer, Emotional Resilience, Gratitude Practice, Cognitive Health not yet created)
  - Environment: Clean Living Spaces (1 of 5 — Nature Therapy, Toxin-Free Living, Sustainable Health, Gardening not yet created)

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
- `.fasting-zones` / `.fasting-zone` — zone-based cards with coloured left borders (`.zone-green`, `.zone-amber`, `.zone-red`)
- `.fasting-disclaimer` — red-tinted medical disclaimer box
- `.video-placeholder` — grey 16:9 placeholder box for upcoming video embeds (replace with `<div class="ratio ratio-16x9"><iframe ...></div>`)
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
- **Browser verification** — use `python3 -m http.server 8000` (not `file://`) for Playwright testing since `file://` protocol is blocked
- **Clean up screenshots** — after every Playwright browser verification (manual or automated), always delete all PNG/JPEG screenshots generated in the project root before finishing the task. Never leave screenshot files behind.

## Client Brief Verification

Every email/brief from Jonathan (the client) is treated as a contract: each request must be tracked, implemented, and independently verified against the codebase. All briefs are logged in [`CLIENT_BRIEFS.md`](CLIENT_BRIEFS.md).

### Workflow for every client brief

1. **Parse the brief.** Read the email and split it into discrete deliverables. Each sentence/bullet/asset link that asks for something is its own row. Include implicit asks (e.g., "thinking of an intro video?" = a question that needs an answer or a deliverable).
2. **Locate evidence.** For each deliverable, find where it lives in the code — file path and line number, or a commit SHA if removed. If you can't find it, it's outstanding.
3. **Mark status.** ✅ Done · 🟡 Partial · ⬜ Outstanding · ❓ Question for client.
4. **Log everything to `CLIENT_BRIEFS.md`** with a dated section per email: source, pillar, page, deliverables table, outstanding questions, and the verification steps performed.
5. **Local browser verification** for any UI-affecting deliverable: serve via `python3 -m http.server 8000`, load with Playwright, evaluate the DOM (count elements, check computed dimensions/ratios, confirm copy is present), then test at both desktop and a mobile viewport (e.g., 390 × 844). Clean up screenshots.
6. **Live URL verification after deploy.** `curl` alone is **not** enough — it only proves bytes were served, not that the page renders. After Sanjay confirms the push, poll the Netlify URL for the deployed content, then load it in **Playwright** and re-run the DOM checks against the live site (desktop + mobile). Confirm iframes are visible, copy is present, no unintended placeholders. Console errors from third-party ad/tracker domains (`doubleclick.net`, etc.) are noise — don't flag.
7. **Surface client questions** at the end of each session — anything the client asked that we haven't answered, and anything we need from them to close out a deliverable.

### When the user asks "did we do X from the email?"

1. Read the brief carefully — don't summarise from memory.
2. Open `CLIENT_BRIEFS.md` and check if there's already a row for that deliverable.
3. If not logged, run the workflow above and add a new section.
4. Reply with a deliverable-by-deliverable table mapping brief items → status → evidence (`file:line`). Never assume "done" without grepping the code.

### First actions when Sanjay pastes a new email from Jonathan

1. **Don't write code yet.** Parse the email into a deliverables table.
2. Add a new dated section to `CLIENT_BRIEFS.md` with: source line, target pillar, target page (does it exist? new file or edit?), deliverables table with all rows marked ⬜, outstanding client questions.
3. Commit the log entry on its own (no code), so the brief is captured before implementation starts.
4. Ask Sanjay only the questions whose answers genuinely block the build. Jonathan is slow to reply — if a question can be defaulted with a flag in the brief log ("assumed X — please confirm"), prefer that over waiting.
5. Once Sanjay greenlights, build → local verify → commit → ask him to push → live verify.

### Scope reminder

Workflow applies **from 2026-05-12 onward only**. The 8 pages built before that date (whole-foods, biblical-core-eating, fasting-detox, resistance-training, walking, flexibility, sleep-hygiene, digital-detox) are out of scope per Sanjay; do not flag them as gaps.

## Adding New Content

### New topic page
1. Copy an existing topic page as a template (`topics/whole-foods.html` for Food & Nutrition, `topics/walking.html` for Exercise, `topics/stress-management.html` for Mental Health)
2. Update the content, title, meta description/keywords, and breadcrumb
3. Link to it from the appropriate subject card in `index.html`
4. Update the sidebar topic list in **all** pages within the same category (each page has a sidebar listing all sibling topics)
5. Add to the Related Topics section at the bottom of sibling pages

### New wellness pillar (subject card)
1. Add a new card section in `index.html` following the existing pattern
2. Add a corresponding item to the health wheel
3. Update the JS circular positioning if the item count changes
