# Client Briefs — Verification Log

This file tracks every brief from Jonathan (the client) and verifies each deliverable against the codebase. See [`CLAUDE.md` → Client Brief Verification](CLAUDE.md#client-brief-verification) for the process.

**Legend:** ✅ Done · 🟡 In progress / partial · ⬜ Outstanding · ❓ Question pending client reply

---

## 2026-04-09 — Stress Management intro script

**Source:** Jonathan Verrinder, email "Stress management", 9 Apr 2026 9:08 PM
**Pillar:** Mental Health
**Page:** [`topics/stress-management.html`](topics/stress-management.html)

| # | Deliverable from brief | Status | Evidence |
|---|---|---|---|
| 1 | Opening hook: "Stress is something we all experience — but what if…" | ✅ | `topics/stress-management.html:123` |
| 2 | "In today's fast-paced world… holistic approach comes in" | ✅ | `topics/stress-management.html:125-127` |
| 3 | "Holistic stress management looks at the whole person…" (everything connected) | ✅ | tip card, `topics/stress-management.html:131-134` |
| 4 | "What is your stress trying to tell you?" | ✅ | tip card, `topics/stress-management.html:135-138` |
| 5 | Practices: mindful breathing, movement, stillness | ✅ | Section 2 tip cards, `topics/stress-management.html:146-159` |
| 6 | "Not about eliminating stress completely… build resilience" | ✅ | tip card, `topics/stress-management.html:139-142` |
| 7 | Closing: "you don't just manage stress… you transform your relationship with it" | ✅ | `topics/stress-management.html:161-164` |
| 8 | "Here are a few videos on mindful breathing" intro line | ✅ | `topics/stress-management.html:176-177` |
| 9 | Intro video for stress management (Jonathan floated the idea — "was thinking of having an intro video?") | 🟡 | Filled with the 5-min Box Breathing video (`FDikCuovqxk`) repurposed as the intro card at `topics/stress-management.html:180-186`. Client may still commission a bespoke overview video to replace it. |

**Outstanding questions for client:**
- Confirm whether the repurposed 5-min Box Breathing video is acceptable as the intro, or whether a bespoke overview intro video should still be recorded.

---

## 2026-04-09 — Breathing videos (YouTube)

**Source:** Jonathan Verrinder, email "Breathing videos", 9 Apr 2026 9:21 PM
**Pillar:** Mental Health
**Page:** [`topics/stress-management.html`](topics/stress-management.html)

| # | Deliverable from brief | Status | Evidence |
|---|---|---|---|
| 1 | Box Breathing copy: "Box breathing is a quiet, grounding practice…" | ✅ | `topics/stress-management.html:190` |
| 2 | Box Breathing video 1 — `youtu.be/FDikCuovqxk` (5 Min Box Breathing, Beginner Pace) | ✅ | repurposed as the **Introduction** card; iframe at `topics/stress-management.html:184` (card span 180-186) |
| 3 | Box Breathing video 2 — `youtu.be/oN8xV3Kb5-Q` | ✅ | embedded under **Box Breathing** card; iframe at `topics/stress-management.html:192` (card span 188-194) |
| 4 | 3-7-8 Breathing copy: "3-7-8 breathing is a peaceful meditation practice…" | ✅ | `topics/stress-management.html:198` |
| 5 | 3-7-8 Breathing video — `youtu.be/U2jGGY0lzr0` (note: client's email had typo `ttps://`) | ✅ | embedded under **3-7-8 Breathing** card; iframe at `topics/stress-management.html:200` (card span 196-202) |

**Outstanding questions for client:**
- ❓ Jonathan asked: "Can these YouTube links be used on the website? Or do we need to do our own version?" — currently embedded as-is. Confirm we may keep the third-party YouTube videos, or commission Tree of Life originals.
- ℹ️ Note for client: YouTube ads will display for visitors who do not use Brave / an ad-blocker. If ad-free playback is required for everyone, we'd need to either (a) replace with our own videos, or (b) host via a paid platform (Vimeo Pro etc.).

**Verification performed:**
- Loaded `topics/stress-management.html` via `python3 -m http.server 8000`
- Confirmed 3 video cards, 3 iframes (one per card, no duplicates), 0 placeholders
- All iframes at `aspect-ratio 16:9` (ratio = 1.778) at desktop (1280px) and mobile (390px) viewports
- Live: https://treeoflife-org.netlify.app/topics/stress-management.html (3 YouTube embeds, 0 placeholders confirmed via curl after deploy)

---

## 2026-04-07 — Power of Napping (backfilled)

**Source:** Jonathan Verrinder, email "Power up with Power napping", 7 Apr 2026 12:35 PM (quoted in 12 Apr "Gratitude" thread)
**Pillar:** Sleep & Rest
**Page:** [`topics/power-of-napping.html`](topics/power-of-napping.html)
**Implementation commit:** `516e0f3` (pre-dates this log)

| # | Deliverable from brief | Status | Evidence |
|---|---|---|---|
| 1 | "A power nap is a short nap of about 10–20 minutes that quickly boosts energy, mood, and focus…" | ✅ | `topics/power-of-napping.html:122` |
| 2 | "The best time… early–mid afternoon (around 1–3 p.m.)" | ✅ | `topics/power-of-napping.html:125` |
| 3 | Long-term benefit framing: "clearer thinking, better memory, calmer emotions, brain and heart health" | ✅ | meta description line 8 + body content |
| 4 | When napping might not be ideal — chronic insomnia caveat | ✅ | `topics/power-of-napping.html:135` |
| 5 | When napping might not be ideal — older adults / sleep apnea / depression check-in | ✅ | `topics/power-of-napping.html:139` |
| 6 | "How to Take a Healthy Power Nap" — 5-step section heading | ✅ | `topics/power-of-napping.html:143` |
| 7 | Step 1 — Pick your time (1–3 p.m.) | ✅ | tip card, `topics/power-of-napping.html:145-148` |
| 8 | Step 2 — Keep it short (10–20 min alarm) | ✅ | tip card, `topics/power-of-napping.html:149-152` |
| 9 | Step 3 — Make a calm space (quiet/dim/cool, eye mask, earplugs) | ✅ | tip card, `topics/power-of-napping.html:153-156` |
| 10 | Step 4 — Set an intention to rest (breath + short prayer/affirmation: "It is safe to pause and rest.") | ✅ | tip card, `topics/power-of-napping.html:157-160` |
| 11 | Step 5 — Wake gently and notice (sit up, stretch, hydrate, recalibrate) | ✅ | tip card, `topics/power-of-napping.html:161-164` |

**Outstanding questions for client:** none.

**Verification:** Live at https://treeoflife-org.netlify.app/topics/power-of-napping.html — Jonathan acknowledged receipt on 12 Apr ("Sanjay Thanks for the other uploads!").

---

## 2026-04-12 — Gratitude (new brief, NOT YET IMPLEMENTED)

**Source:** Jonathan Verrinder, email "Gratitude", 12 Apr 2026 8:24 PM
**Pillar:** Mental Health
**Target page:** `topics/gratitude-practice.html` *(does not yet exist — currently a dead link from the Mental Health sidebar in `topics/stress-management.html:99`)*
**Implementation commit:** _pending_

### Core teachings (each is its own deliverable / section)

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 1 | Gratitude as the Master Key to Blessings — "everything, big or small, comes from a higher source" | ⬜ | section needed |
| 2 | Quantum Leap in Personal and Spiritual Growth — shifts perspective from lack to presence | ⬜ | section needed |
| 3 | Prerequisite for Happiness and Healthy Relationships — esp. marriage; "without it relationships feel like a brick wall" | ⬜ | section needed |
| 4 | Gratitude Defies Nature and Invokes Miracles — thanking God in difficult times brings healing, financial relief, salvations | ⬜ | section needed |
| 5 | Thanking for Everything, Including Challenges — difficulties as hidden blessings; "attitude of gratitude" sweetens and transforms pain | ⬜ | section needed |
| 6 | "Dedicate 15 minutes to thanking God for a problem, then recite Psalms" exercise | ⬜ | candidate for a journal-style or call-out box (Jonathan didn't specify which Psalms — see open question) |
| 7 | Gratitude Builds on Emuna (Faith) — turns abstract belief into daily lived experience | ⬜ | section needed |

### Practical application (must appear as a "How to apply" block)

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 8 | Begin each day verbally thanking God for specific things (body parts, possessions, family, hardships) | ⬜ | tip card |
| 9 | In tough moments, pause and say "thank You" for the situation | ⬜ | tip card |
| 10 | Express sincere thanks to people around you to strengthen bonds | ⬜ | tip card |
| 11 | Combine with personal prayer for deeper effect | ⬜ | tip card |
| 12 | Gratitude Journaling (highly recommended) — daily writing of good things from the last 24h, small or large | ⬜ | reuse existing `.journal-section` / `.journal-field` printable component (see Fasting & Detox page for pattern) |

### Outstanding questions for client (raise before/with first draft)

- ❓ Which **Psalms** does Jonathan want cited for the 15-minute exercise? (he wrote "recite Psalms .." but didn't fill in the references)
- ❓ The brief uses the term **Emuna** (Hebrew for faith). Use it as-is with a parenthetical, or render purely in English?
- ❓ Any specific **Scripture passages** Jonathan wants prominently quoted (à la 1 Peter 5:7 on Stress Management)? Candidates: 1 Thessalonians 5:18, Psalm 100:4, Colossians 3:17.
- ❓ Does he want a **video** on this page (same pattern as Stress Management), or is text-only fine?
- ❓ Confirm the **page slug**: `gratitude-practice.html` (matches existing sidebar link) vs. `gratitude.html`.

### Reference notes (from same email thread)

- Jonathan confirmed receipt and approval of the Power of Napping upload on 12 Apr ("Thanks for the other uploads!") — see Apr 7 entry above.

---

## 2026-04-16 — Clean Living Spaces (new brief, NOT YET IMPLEMENTED)

**Source:** Jonathan Verrinder, email "Clean living spaces", 16 Apr 2026 5:44 PM
**Pillar:** Environment (this would be the **first** Environment topic page)
**Target page:** `topics/clean-living-spaces.html` *(does not yet exist — already linked from `index.html:421`)*
**Implementation commit:** _pending_

### Core sections from brief

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 1 | Opening: clean living spaces support holistic health (stress↓, focus↑, sleep, easier routines, fewer allergens/respiratory irritants) | ⬜ | intro paragraph |
| 2 | **Mental and emotional health** — tidy → less overwhelm, more control, less anxiety, better mood, fewer visual distractions, better concentration | ⬜ | section |
| 3 | **Physical health** — indoor air quality, dust/allergens/harsh chemicals, asthma/headaches/allergies | ⬜ | section |
| 4 | **Sleep and recovery** — cleaner bedroom → better rest, deeper sleep → recovery, mood, daytime energy | ⬜ | section |
| 5 | **Healthy habits** — organised spaces → easier cooking/exercise/routines, fewer barriers to action | ⬜ | section |

### Five themed sub-areas (listed in the brief)

These are mentioned as themes to cover. Could be **sections on this page** OR **stubs for future Environment topic pages**. See open question below.

| # | Theme | Notes from brief |
|---|---|---|
| 6 | Home hygiene | cleaning routines, sanitation, non-toxic products, airflow, decluttering |
| 7 | Biblical encouragement | short devotionals tied to verses about cleanliness, order, stewardship |
| 8 | Holistic wellness | how clean spaces support stress reduction, rest, spiritual focus |
| 9 | Family practices | simple household rhythms, shared chores, hospitality |
| 10 | Seasonal reset | spring cleaning, Sabbath prep, prayerful decluttering |

### Biblical View of the Home (section)

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 11 | Home-as-sanctuary framing: peace, order, prayer, welcome to God's presence | ⬜ | likely a `.biblical-box`-style intro |
| 12 | Cleaning reframed as **stewardship**, not housekeeping | ⬜ | section |
| 13 | Practical house-sanctuary ideas — 6 bullets (see below) | ⬜ | candidate for `.tips-grid` / `.tip-card` |
| 13a | Keep surfaces clear and rooms tidy | ⬜ | tip card |
| 13b | Place Scripture / faith-based art in visible spots | ⬜ | tip card |
| 13c | Create a quiet prayer corner with Bible, journal, chair | ⬜ | tip card |
| 13d | Use gentle routines for cleaning and resetting the home | ⬜ | tip card |
| 13e | Each room serves a biblical-values purpose (rest, fellowship, cleansing, hospitality) | ⬜ | tip card |
| 13f | Clean regularly as stewardship and gratitude, not chore | ⬜ | tip card |
| 14 | Closing narrative: not about perfection; atmosphere of love/peace/joy, welcoming family and guests, everyday routines shaped by faith | ⬜ | closing paragraphs |

### Outstanding questions for client (raise with first draft)

- ❓ Which **Scripture verses** does Jonathan want quoted? Brief mentions themes (cleanliness, order, stewardship) but cites none. Candidates I'd default to: **1 Cor 14:40** ("everything should be done in a fitting and orderly way"), **Prov 24:3-4** ("by wisdom a house is built…"), **Heb 13:2** (hospitality), **Joshua 24:15** ("as for me and my house we will serve the Lord").
- ❓ Are the **5 themed sub-areas** (home hygiene / biblical encouragement / holistic wellness / family practices / seasonal reset) all sections on this **one** page, or do some belong as **separate future topic pages** under Environment? The Environment pillar already has 4 other topics planned (Nature Therapy, Toxin-Free Living, Sustainable Health, Gardening) — there may be overlap (e.g., "non-toxic products" → Toxin-Free Living).
- ❓ **Video** on this page (à la Stress Management) or text-only?
- ❓ Confirm **page slug**: `clean-living-spaces.html` matches the existing dead link in `index.html:421` — proceed with that.
- ❓ Tone of the **practical sanctuary ideas** — 6 tip-cards (like Sleep Hygiene's "How to take a healthy power nap"), or a more visual layout?

### Defaults Claude will apply if not blocked

Per Sanjay's standing direction (client is slow to reply, don't block):

- **Slug:** `clean-living-spaces.html` (matches existing sidebar link).
- **Scope:** treat this as a single cornerstone Environment page; cover all 5 themed sub-areas on this page at a light level. Future pages (Toxin-Free Living, Gardening, etc.) can take the deeper dive.
- **Scripture:** lead biblical-box with **1 Cor 14:40**; supporting refs (Heb 13:2, Josh 24:15) inline. Flag clearly so Jon can swap.
- **No video** unless he sends assets.
- **Practical sanctuary ideas** → `.tips-grid` of 6 cards, same pattern as Power of Napping's "How to Take a Healthy Power Nap".

All defaults will be marked in the page's commit message and re-flagged here as 🟡 with "assumed — please confirm" so Jon can override on return.

Ran when Sanjay requested "independent verification of all the work you do for this client". Audits every shipped page against the verification workflow defined in `CLAUDE.md` → "Client Brief Verification".

### A. Live-deploy health

All 10 topic pages return **HTTP 200** on Netlify:

| Slug | URL | Status |
|---|---|---|
| biblical-core-eating | [link](https://treeoflife-org.netlify.app/topics/biblical-core-eating.html) | ✅ 200 |
| digital-detox | [link](https://treeoflife-org.netlify.app/topics/digital-detox.html) | ✅ 200 |
| fasting-detox | [link](https://treeoflife-org.netlify.app/topics/fasting-detox.html) | ✅ 200 |
| flexibility | [link](https://treeoflife-org.netlify.app/topics/flexibility.html) | ✅ 200 |
| power-of-napping | [link](https://treeoflife-org.netlify.app/topics/power-of-napping.html) | ✅ 200 |
| resistance-training | [link](https://treeoflife-org.netlify.app/topics/resistance-training.html) | ✅ 200 |
| sleep-hygiene | [link](https://treeoflife-org.netlify.app/topics/sleep-hygiene.html) | ✅ 200 |
| stress-management | [link](https://treeoflife-org.netlify.app/topics/stress-management.html) | ✅ 200 |
| walking | [link](https://treeoflife-org.netlify.app/topics/walking.html) | ✅ 200 |
| whole-foods | [link](https://treeoflife-org.netlify.app/topics/whole-foods.html) | ✅ 200 |

### B. Structural DOM checks (all 10 pages, via Playwright + DOMParser)

Every page passes all checks:
- `<title>` set and matches H1
- `.page-title h1` present with the topic name
- `.breadcrumbs .current` set to the topic name
- `.services-list a` sidebar present with correct topic count for its category (Food 5, Exercise 3, Sleep 4, Mental 5)
- Exactly **one** `.services-list a.active` link, and its `href` matches the current page slug
- `.biblical-box` present (scripture quote)
- `.related-topics` present (bottom-of-page pills)
- `.help-box` present (Contact CTA)

### C. Known dead sidebar links (expected per CLAUDE.md)

These slugs are referenced from existing pages' sidebars / Related Topics / `index.html`, but the pages do **not yet exist** — they would 404 if clicked. This matches CLAUDE.md's documented backlog.

| Pillar | Missing topic page |
|---|---|
| Food & Nutrition | `hydration.html`, `mindful-eating.html` |
| Sleep & Rest | `sabbath-rest.html` |
| Mental Health | `meditation-prayer.html`, `emotional-resilience.html`, `gratitude-practice.html`, `cognitive-health.html` |
| Family, Community, Environment, Spiritual | *no topic pages exist yet for these pillars* |

### D. Pages shipped without a brief on file in this log

The Client Brief Verification workflow was set up on 2026-05-12. Eight pages were built **before** that date and have no corresponding email logged in this file.

**Decision (2026-05-12, Sanjay):** these pages are **out of scope** for the verification workflow — do not flag them as gaps in future sweeps. Workflow applies from 2026-05-12 onward only.

| Page | Status |
|---|---|
| `whole-foods.html` | Pre-workflow — out of scope |
| `biblical-core-eating.html` | Pre-workflow — out of scope |
| `fasting-detox.html` | Pre-workflow — out of scope |
| `resistance-training.html` | Pre-workflow — out of scope |
| `walking.html` | Pre-workflow — out of scope |
| `flexibility.html` | Pre-workflow — out of scope |
| `sleep-hygiene.html` | Pre-workflow — out of scope |
| `digital-detox.html` | Pre-workflow — out of scope |
| `power-of-napping.html` | ✅ Apr 7 brief backfilled |
| `stress-management.html` | ✅ Apr 9 brief logged (script + videos) |

### E. Line-number drift check on logged briefs

Re-verified every `file:line` reference in this file against the current source. Three line numbers in the Apr 9 Breathing videos table had drifted by 1 line since the intro-card repurposing (commit `a795220`) — corrected in this sweep. All other references confirmed accurate.

### F. Summary

- **Live deploy:** 10/10 pages healthy, 0 broken
- **Structural integrity:** 10/10 pages pass all DOM checks
- **Brief coverage:** 2/10 pages logged; 8/10 pre-date the workflow and are out of scope (per Sanjay 2026-05-12)
- **Open client questions:** 6 across Stress Management (2) and Gratitude (5) — see entries above; client cadence is slow, do not block on them

