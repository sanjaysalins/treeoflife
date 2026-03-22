# Tree of Life - Holistic Wellness Website

A static website promoting holistic health and wellness through eight interconnected pillars: Food & Nutrition, Exercise, Sleep & Rest, Mental Health, Family, Community, Environment, and Spiritual.

Built on the BootstrapMade "QuickStart" template with a nature-inspired green theme.

**Live site:** https://treeoflife-org.netlify.app/

## Tech Stack

- HTML5, CSS3, Vanilla JavaScript — no build tools or frameworks
- Bootstrap 5.3.3 for grid/components
- PHP for contact and newsletter form handlers
- Vendor libraries in `assets/vendor/` (Bootstrap, AOS, GLightbox, Swiper)

## Project Structure

```
index.html                  # Main landing page
topics/                     # Topic pages by wellness pillar
  whole-foods.html          # Food & Nutrition
  resistance-training.html  # Exercise — resistance program
  walking.html              # Exercise — walking
  sleep-hygiene.html        # Sleep & Rest — sleep hygiene & circadian rhythm
assets/
  css/main.css              # All custom styles
  js/main.js                # All custom JS
  img/                      # Images
  vendor/                   # Third-party libs (do not modify)
forms/
  contact.php               # Contact form handler
  newsletter.php            # Newsletter handler
```

## Deployment

Pushing to `main` on GitHub auto-deploys to Netlify: https://treeoflife-org.netlify.app/

No build step — Netlify serves the static files directly.

## Running Locally

No build step required:
- Open `index.html` directly in a browser (forms won't work)
- Or run `php -S localhost:8000` for full functionality including PHP forms

## Adding Content

1. Copy an existing topic page as a template
2. Update content, title, and breadcrumb
3. Link from the appropriate subject card in `index.html`
4. Update the sidebar topic list in all pages within the same category
