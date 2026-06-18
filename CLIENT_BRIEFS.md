# Client Briefs — Verification Log

This file tracks every brief from Jonathan (the client) and verifies each deliverable against the codebase. See [`CLAUDE.md` → Client Brief Verification](CLAUDE.md#client-brief-verification) for the process.

**Legend:** ✅ Done · 🟡 In progress / partial · ⬜ Outstanding · ❓ Question pending client reply

---

## 2026-06-13 — Purpose & Meaning + Spiritual section restructure (new brief, NOT YET IMPLEMENTED)

**Source:** Jonathan Verrinder, email "Purpose and meaning", 13 Jun 2026 6:46 PM
**Pillar:** Spiritual (first Spiritual topic page)
**Target page:** `topics/purpose-meaning.html` *(new file; slug already linked as a dead link from `index.html:446`)*
**Implementation commit:** _pending_

> **Explicit client instruction:** "For the spiritual section there only needs to be 3 topics — meditation and prayer, sabbath rest and purpose / meaning — as these crossover into most of the other areas of the health website." → Reduce the Spiritual subject card from its current 5 dead links to exactly these 3.

### A. Spiritual section restructure (`index.html`)

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 1 | Reduce Spiritual card to 3 topics: **Meditation & Prayer**, **Sabbath Rest**, **Purpose & Meaning**; remove Scripture & Health, Prayer & Healing, Worship & Wellness, Spiritual Disciplines | ⬜ | `index.html:441-447` |
| 1a | "Meditation & Prayer" → `topics/meditation-prayer.html` (already exists — built under Mental Health; cross-pillar link, matches Jon's "crossover" point) | ⬜ | live page |
| 1b | "Sabbath Rest" → `topics/sabbath-rest.html` (**does not exist yet** — no content supplied in this brief; will be a dead link until built) | ⬜ | ⚠️ backlog — flagged below |
| 1c | "Purpose & Meaning" → `topics/purpose-meaning.html` (this brief) | ⬜ | new page |

### B. Purpose & Meaning page content

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 2 | ✨ **Biblical framework** intro — purpose/meaning come from God, shape the whole person; every human bears the image of God (*tzelem Elohim*), inherent dignity & direction; meaning discovered by walking with God and aligning life with His design | ⬜ | intro section |
| 3 | 🌱 **Holistic Health Integration** — alignment with God's design strengthens 4 areas: emotional wellbeing (clarity, direction, resilience) · spiritual vitality (rooted identity, connection) · relational health (compassion, forgiveness, community) · physical health (reduced stress, deeper peace, healthier rhythms) | ⬜ | tips-grid (4 cards) |
| 4 | Closing line — "purpose is not a single task — it is a whole-life orientation shaped by God's presence and wisdom" | ⬜ | section line |
| 5 | 🌱 **Applications for Daily Life** — 7 practices, each with its "Application" steps: | ⬜ | tips-grid (7 cards) or guided list |
| 5a | Daily Scripture Engagement — Torah/Psalms/Proverbs/Jesus' teachings; read a short passage each morning, reflect on one phrase | ⬜ | card |
| 5b | Practicing Gratitude — write 3 blessings each evening; blessing before meals (cross-link Gratitude Practice) | ⬜ | card |
| 5c | Sabbath Rhythms — one weekly period for rest/worship/unplugging; share a meal | ⬜ | card |
| 5d | Acts of Compassion — help someone in need weekly; give time/resources | ⬜ | card |
| 5e | Prayer and Reflection — begin/end day with a short prayer; use Psalms or the Lord's Prayer (cross-link Meditation & Prayer) | ⬜ | card |
| 5f | Community Connection — join a study group/place of worship/community; share meals, stories, support | ⬜ | card |
| 5g | Living with Integrity — align one area of life with God's ways; honesty, humility, compassion | ⬜ | card |

### Defaults proposed (will apply on greenlight unless told otherwise)

| Decision | Proposed default | Rationale |
|---|---|---|
| 🟡 **Slug** | `purpose-meaning.html` | matches existing dead link `index.html:446` |
| 🟡 **Spiritual sidebar** | the new page's sidebar lists the 3 Spiritual topics (Meditation & Prayer, Sabbath Rest, Purpose & Meaning), Purpose & Meaning active | matches the restructured pillar |
| 🟡 **Sabbath Rest link** | leave as a dead link to `sabbath-rest.html` for now (no content yet) | not in this brief; known backlog |
| 🟡 **7 applications layout** | 7 tip-cards in a `.tips-grid`, each with the practice + its application steps | matches Power of Napping / Mindful Eating step patterns |
| 🟡 **Cross-linking** | link Gratitude → `gratitude-practice.html`, Prayer → `meditation-prayer.html`, Sabbath → `sabbath-rest.html` | supports Jon's "crossover" framing |
| 🟡 **Sidebar Scripture** | Jeremiah 29:11 ("plans to give you hope and a future") | canonical purpose verse |
| 🟡 **Mid-page Scripture box** | Ephesians 2:10 ("created in Christ Jesus to do good works") | purpose-in-action; pairs with the daily applications |
| 🟡 **tzelem Elohim** | keep the Hebrew term with its English gloss | client used it deliberately |
| 🟡 **No video / no journal** | text + cards only | none requested |

### Outstanding questions for client

- ❓ **Sabbath Rest** is one of your 3 Spiritual topics but no page/content exists yet — shall we draft one (it overlaps the existing Sleep & Rest material), or do you have copy to send? Until then its link will 404.
- ❓ Confirm removing the other 4 Spiritual subjects (Scripture & Health, Prayer & Healing, Worship & Wellness, Spiritual Disciplines).
- ❓ Confirm/seed **Scripture**: sidebar Jeremiah 29:11 + mid-page Ephesians 2:10.
- ❓ OK that **Meditation & Prayer** in the Spiritual list points to the existing Mental Health page (one page, two pillars), rather than a separate Spiritual copy?

---

## 2026-06-13 — Family Health (✅ SHIPPED + live-verified 2026-06-18)

**Source:** Jonathan Verrinder, email "Family health", 13 Jun 2026 6:21 PM
**Pillar:** Family (this is the **first** Family topic page)
**Target page:** [`topics/family-health.html`](topics/family-health.html) *(new file — no existing slug; the Family card in `index.html` previously listed 5 dead links)*
**Implementation commit:** `5532a4c` (pushed to `main`; live-verified on Netlify 2026-06-18)

> **Explicit client instruction:** "this is to be the only and main topic on family health … so please remove all the other subjects in the family health section." → The 5 current Family subject links (Family Meals, Parenting & Wellness, Marriage & Health, Generational Health, Family Fitness) must be **removed** from `index.html` and replaced with a single link to `family-health.html`. None of those 5 pages exist (all dead links today).

### A. Biblical lens — the family in Scripture

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 1 | Intro — family health through a biblical lens = nurturing the whole household (body, mind, spirit, relationships) per God's design | ✅ | `topics/family-health.html:117-119` |
| 2 | The Bible presents the family as 4 things — unit of discipleship (Deut 6:6-7) · place of nurture & protection (Prov 14:26) · source of generational blessing (Ps 103:17) · body of mutual care (1 Cor 12:25-26) | ✅ | 4 tip-cards, `topics/family-health.html:122-140` |
| 3 | Holistic family health in Scripture — 5 areas: physical stewardship (1 Cor 6:19-20) · emotional/relational peace (Col 3:12-14) · spiritual formation · healthy rhythms / Sabbath (Ex 20:8-10) · wise living (Prov 25:28); tagline "whole-family flourishing under God's wisdom" | ✅ | 5 tip-cards + line, `topics/family-health.html:142-165` |

### B. Holistic framework — 6 core themes

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 4 | Framework intro — family as a whole interconnected ecosystem (physical, emotional, mental, relational, environmental); blends natural health, lifestyle coaching, emotional support | ✅ | `topics/family-health.html:172-175` (merged the brief's repeated "core themes" summary into the 6 detailed themes) |
| 5 | 🧩 Whole-family wellbeing — interconnected system: routines, communication, stress, shared habits | ✅ | tip card, `topics/family-health.html:178-181` |
| 6 | 🥗 Nutrition & lifestyle — balanced diets, hydration, meal planning, reducing processed foods, family recipes | ✅ | tip card w/ cross-links to `hydration.html` + `whole-foods.html`, `:182-185` |
| 7 | 😌 Mental & emotional health — stress management, mindfulness, emotional regulation, healthy communication, children's mental health | ✅ | tip card w/ cross-link to `stress-management.html`, `:186-189` |
| 8 | 🧘 Holistic practices — yoga for kids & parents, meditation, herbal remedies, natural living, gentle alternative therapies | ✅ (kept verbatim — ⚠️ flagged below) | tip card w/ cross-link to `meditation-prayer.html`, `:190-193` |
| 9 | 🛏️ Sleep, routines & home environment — sleep routines, screen-time balance, calm low-toxicity homes | ✅ | tip card w/ cross-links to `sleep-hygiene.html` + `digital-detox.html` + `clean-living-spaces.html`, `:194-197` |
| 10 | 🩺 Preventive care & education — regular checkups, early detection, teaching children body awareness, early healthy habits | ✅ | tip card, `topics/family-health.html:198-201` |

### C. Every family is unique

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 11 | "Not one-size-fits-all" — each family adapts the guidelines to its own system | ✅ | `topics/family-health.html:204-207` |
| 12 | 🌱 Key Points — every family system is unique · guidelines are flexible (adjust, not rigid) · strengths & challenges vary · adaptation improves success | ✅ | 4 tip-cards, `topics/family-health.html:209-227` |

### D. index.html change

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 13 | Remove the 5 existing Family subject links; replace with a single `Family Health` link → `topics/family-health.html` | ✅ | `index.html:370-372` (was 5 links, now 1) |

### Defaults applied — 🟡 PLEASE CONFIRM with client (Sanjay greenlit build 2026-06-18)

| Decision | Applied default | Rationale |
|---|---|---|
| 🟡 **Slug** | `family-health.html` | no existing slug; descriptive and matches the brief title |
| 🟡 **Scope** | one cornerstone Family Health page (all brief sections); Family becomes a 1-topic pillar | client's explicit instruction |
| 🟡 **Section consolidation** | merge the brief's duplicated "core themes" list (intro) into the 6 detailed numbered themes so they aren't stated twice | brief repeats the same 6 themes in summary then detail |
| 🟡 **Cross-linking** | link the themes that overlap existing pages (Hydration, Whole Foods, Stress Management, Sleep Hygiene, Digital Detox, Clean Living Spaces, Meditation & Prayer) — supports "corresponds to the rest of the topics on the website" | client's framing |
| 🟡 **Sidebar Scripture** | Deuteronomy 6:6-7 (family discipleship) | the brief's lead verse |
| 🟡 **Mid-page Scripture box** | Joshua 24:15 ("as for me and my household, we will serve the Lord") | classic family/household verse |
| 🟡 **Sidebar topic list** | single-item Family list ("Family Health", active) | only Family topic now |
| 🟡 **Yoga / herbal remedies / alternative therapies** | kept verbatim as written | client included them — but flagged below for a faith-based-site check |
| 🟡 **No video / no journal** | text + cards only | no asset or journal requested |

### Outstanding questions for client — 📨 SENT 2026-06-18 (Sanjay forwarding)

- ❓ Confirm removing the 5 existing Family subjects (Family Meals, Parenting & Wellness, Marriage & Health, Generational Health, Family Fitness) and leaving only Family Health. (Acting on the explicit instruction — flagging for the record.)
- ❓ Theme 4 lists **yoga, herbal remedies, and "gentle alternative therapies."** On a biblically grounded site some of these can be sensitive — keep all verbatim, soften, or drop any?
- ❓ Confirm/seed **Scripture**: sidebar Deut 6:6-7 + mid-page Joshua 24:15.
- ❓ OK to **cross-link** the overlapping themes to our existing topic pages (hydration, stress, sleep, clean spaces, etc.)? (applied — cards link to Hydration, Whole Foods, Stress Management, Meditation & Prayer, Sleep Hygiene, Digital Detox, Clean Living Spaces)

### Reference notes

- Brief content overlaps heavily with existing pillars by design ("corresponds to the rest of the topics on the website") — Family Health is intended as a hub that ties the other pillars together for the household.

### Verification performed

- **Local** (`python3 -m http.server 8000`): Playwright DOM check at 1280 × 800 — title == H1 == "Family Health", breadcrumb current correct, single-item Family sidebar with the one link `.active` → `family-health.html`, 3 H3 sections + "The Family in Scripture"/"Holistic Family Health in Scripture" sub-sections, 4 tips-grids (4 + 5 + 6 + 4 = 19 tip-cards), 2 biblical boxes (Deut 6:6-7 + Joshua 24:15), 7 in-card cross-links all resolving to existing topic files, 4 related-topics pills, help box present. `index.html` Family card confirmed reduced from 5 links to 1 (Family Health). Mobile at 390 × 844 — no horizontal overflow, all 19 tip-cards uniform 351px (stacked).
- **Live** (https://treeoflife-org.netlify.app/topics/family-health.html): deployed after push. Playwright re-ran all desktop (1280 × 800) + mobile (390 × 844) DOM checks against the live URL — every assertion matched the local run (title/H1/breadcrumb, single-item Family sidebar active, 3 H3 sections, 19 tip-cards across 4 grids, 2 Scripture boxes Deut 6:6-7 + Josh 24:15, 7 in-card cross-links, 4 related-topics, help box; no mobile overflow, 351px uniform widths). Live `index.html` Family card confirmed = 1 link (Family Health). ✅

---

## 2026-06-12 — Meditation & Prayer (✅ SHIPPED + live-verified 2026-06-18)

**Source:** Jonathan Verrinder, email "Mediation and prayer", 12 Jun 2026 11:10 AM
**Pillar:** Mental Health
**Target page:** [`topics/meditation-prayer.html`](topics/meditation-prayer.html) *(new file; slug was already linked as a dead link from `index.html:347` and the Mental Health sidebars/Related Topics of `stress-management.html` + `gratitude-practice.html`)*
**Implementation commit:** `996402a` (pushed to `main`; live-verified on Netlify 2026-06-18)

This is a **large** brief: an intro/benefits frame, two teaching sections (what biblical meditation is; what prayer is), and **three distinct contemplative practices** — Biblical Meditation, Hitbodedut, and Lectio Divina — each with its own explainer **and** a 6-step guided script.

### A. Intro & "Why Meditation + Prayer Support Health"

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 1 | Opening benefits list — reduce stress/anxiety via Scripture-anchored calm · improve emotional regulation by surrendering burdens · strengthen resilience via God's promises · deepen spiritual identity & connection | ✅ | 4 tip-cards, `topics/meditation-prayer.html:126-143` |
| 2 | Core-truth framing — biblical meditation is *not* emptying the mind but *filling* it with God's Word; prayer is direct relational communion with God; together a holistic practice supporting emotional/mental/physical well-being | ✅ | intro, `topics/meditation-prayer.html:123` |

### B. What Biblical Meditation Is

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 3 | Definition — active, intentional reflection on Scripture (Joshua 1:8, Psalm 1:2 — meditate "day and night") | ✅ | `topics/meditation-prayer.html:145-148` |
| 4 | 4 key characteristics — Scripture reflection · Prayerful listening · Heart engagement · Transformation (Romans 12:2) | ✅ | 4 tip-cards, `topics/meditation-prayer.html:150-167` |

### C. What Prayer Is

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 5 | Definition — relational conversation with God: praise, confession, thanksgiving, petition; guided prayer helps slow down, sense God's presence, surrender burdens | ✅ | `topics/meditation-prayer.html:169-172` |
| 6 | 4 prayer-practice examples — Imaginative · Centering · Examen · Intercessory | ✅ | 4 tip-cards, `topics/meditation-prayer.html:174-191` |

### D. Guided Biblical Meditation Script (6 steps)

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 7 | 6-step script — Settle the Body · Invite God's Presence · Scripture Focus (Psalm 46:10 "Be still and know that I am God") · Reflection (3 questions) · Response in Prayer · Closing | ✅ | `.guided-script` box, `topics/meditation-prayer.html:200-210` (Ps 46:10 box at `:194-197`) |

### E. Hitbodedut

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 8 | What it is — "self-seclusion"; speaking to God in your own words; most emotionally honest form of Jewish prayer/meditation | ✅ | `topics/meditation-prayer.html:212-215` |
| 9 | 5 core elements — Personal prayer · Emotional honesty · Seclusion (ideally in nature) · Conversational tone · Daily practice (~1 hr/day) | ✅ | 5 tip-cards, `topics/meditation-prayer.html:217-238` |
| 10 | Why it supports mental & emotional health — reduce anxiety via release · resilience via verbalising fears/hopes · clarity via reflective self-talk · deepen identity · regulate emotions; "like prayer + journaling + mindfulness + therapy" | ✅ | `topics/meditation-prayer.html:240-248` |
| 11 | How to practice (6 steps) — Find a quiet place · Begin with silence · Speak in your own language · Move through 4 phases (Gratitude, Confession/struggle, Requests, Listening) · Let emotions flow · Close with trust | ✅ | 6 step tip-cards, `topics/meditation-prayer.html:250-276` |
| 12 | Guided Hitbodedut Script (6 steps) — Settle · Speak · Explore · Release · Listen · Close | ✅ | `.guided-script` box, `topics/meditation-prayer.html:278-288` |

### F. Lectio Divina

| # | Deliverable from brief | Status | Notes |
|---|---|---|---|
| 13 | What it is — "divine reading"; slow, prayerful reading so the Word moves mind → heart | ✅ | `topics/meditation-prayer.html:290-293` |
| 14 | 4 movements — Lectio (Reading) · Meditatio (Meditation) · Oratio (Prayer) · Contemplatio (Contemplation) | ✅ | 4 tip-cards, `topics/meditation-prayer.html:295-312` |
| 15 | Guided Lectio Divina Script (6 steps) — Prepare · Read · Notice · Reflect · Pray · Rest | ✅ | `.guided-script` box, `topics/meditation-prayer.html:314-324` |

### Defaults applied — 🟡 PLEASE CONFIRM with client (Sanjay greenlit one-page build 2026-06-18)

| Decision | Applied default | Rationale |
|---|---|---|
| 🟡 **Slug** | `meditation-prayer.html` | matches existing dead links |
| 🟡 **Scope** | one cornerstone page covering all three practices as stacked sections | Sanjay chose "one cornerstone page"; mirrors Clean Living Spaces |
| 🟡 **Guided scripts (×3)** | new lightweight `.guided-script` CSS component (tinted box + accent left border + numbered `<ol>`), added to `assets/css/main.css` after `.btn-accent` | three scripts are step lists, not fill-in journals |
| 🟡 **Sidebar Scripture** | Joshua 1:8 ("meditate on it day and night…") | the brief's own anchor verse for meditation |
| 🟡 **Mid-page Scripture box** | Psalm 46:10 ("Be still, and know that I am God") | used in the brief's meditation script; central to the theme |
| 🟡 **Hebrew terms** | kept "Hitbodedut" (+ התבודדות) and "Lord Yeshua" verbatim | client used them deliberately |
| 🟡 **"1 hour a day"** | kept as written in the Daily Practice card | brief states it explicitly |
| 🟡 **No video** | text-only (no asset supplied) | consistent with other text pages |

### New CSS component

- Added `.guided-script` to `assets/css/main.css` (~30 lines, after `.btn-accent:hover`). Tinted accent box with a numbered ordered list; documented as a Custom CSS Component candidate for `CLAUDE.md` once the brief is closed.

### Outstanding questions for client — 📨 SENT 2026-06-18 (awaiting Jon's reply)

- ❓ This is a big page (3 practices + 3 scripts). OK as **one long cornerstone page**, or split Hitbodedut / Lectio Divina into their own topic pages later? (defaulting to one page)
- ❓ Confirm/seed **Scripture** picks: sidebar Joshua 1:8 + mid-page Psalm 46:10 (brief also cites Psalm 1:2, Romans 12:2).
- ❓ The brief recommends Hitbodedut **"one hour a day"** — keep that figure as-is, or soften (e.g. "even a few minutes")? (defaulting to as-written)
- ❓ Keep the Hebrew/Hebraic terms **"Hitbodedut"** and **"Lord Yeshua"** verbatim? (defaulting to yes)

### Verification performed

- **Local** (`python3 -m http.server 8000`): Playwright DOM check at 1280 × 800 — title == H1 == "Meditation & Prayer", breadcrumb current correct, 5 Mental Health sidebar links with exactly one `.active` → `meditation-prayer.html`, 6 H3 sections (Why / Biblical Meditation / Prayer / Guided Meditation / Hitbodedut / Lectio Divina), 6 tips-grids (4 + 4 + 4 + 5 + 6 + 4 = 27 tip-cards), 3 `.guided-script` boxes each with 6 steps, 2 biblical boxes (Joshua 1:8 + Psalm 46:10), 4 related-topics pills, help box present, 0 iframes. Mobile at 390 × 844 — no horizontal overflow, all 27 tip-cards and all 3 guided-script boxes uniform 351px (stacked).
- **Live** (https://treeoflife-org.netlify.app/topics/meditation-prayer.html): deployed after push. Playwright re-ran all desktop (1280 × 800) + mobile (390 × 844) DOM checks against the live URL — every assertion matched the local run (title/H1/breadcrumb, 1 active sidebar link, 6 sections, 27 tip-cards across 6 grids, 3 guided-script boxes × 6 steps with the `.guided-script` 4px accent border applied, 2 Scripture boxes Josh 1:8 + Ps 46:10, 4 related-topics, help box; no mobile overflow, 351px uniform widths). ✅

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

## 2026-04-12 — Gratitude (⚠️ SUPERSEDED by 2026-05-21 "new version" — see below, NOT IMPLEMENTED)

> **Superseded.** On 21 May 2026 Jonathan sent a "new version" of the Gratitude content ("please use this one") with a different, research/holistic-health framing. The spiritual/Emuna-centred deliverables below were **never built** and are **not** carried into the new page. Kept here for history only. Live page is built from the 2026-05-21 brief.

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

## 2026-05-21 — Gratitude (NEW VERSION — supersedes 2026-04-12)

**Source:** Jonathan Verrinder, email "Gratitude new version please use this one thanks Jon", 21 May 2026 8:00 AM
**Pillar:** Mental Health
**Target page:** [`topics/gratitude-practice.html`](topics/gratitude-practice.html) *(new file; slug was already linked as a dead link from `index.html:349` and the Mental Health sidebar)*
**Implementation commit:** `e4ff68c` (pushed to `main`; live-verified on Netlify 2026-06-18)

### Core sections from brief

| # | Deliverable from brief | Status | Evidence |
|---|---|---|---|
| 1 | **What Is Gratitude?** — more than saying "thank you"; intentional recognition/appreciation of the positive (people, experiences, opportunities, nature, growth); a daily practice supporting emotional, mental, physical, spiritual well-being | ✅ | intro, `topics/gratitude-practice.html:127-132` |
| 2 | Four ways gratitude can be practiced — a mindset · a daily habit · a spiritual practice · a therapeutic wellness tool | ✅ | tips-grid (4 cards), `topics/gratitude-practice.html:134-153` |
| 3 | Closing of intro — gratitude as part of the connection between mind, body, emotions, and spirit | ✅ | `topics/gratitude-practice.html:155-157` |
| 4 | **Benefit 1 — Emotional & Mental Wellness** — happiness↑, stress↓, emotional resilience, optimism, reduced anxiety/depression in some; shifts attention from negative thinking → emotional balance | ✅ | tip card, `topics/gratitude-practice.html:161-164` |
| 5 | **Benefit 2 — Physical Health** — better sleep, lower stress-hormone activity, improved heart health, healthier lifestyle behaviours, more self-care motivation; more likely to exercise / seek help / keep routines | ✅ | tip card, `topics/gratitude-practice.html:165-168` |
| 6 | **Benefit 3 — Brain & Nervous System Support** — activates reward, emotional regulation, social bonding, positive-mood processing; may retrain the brain toward positive patterns | ✅ | tip card, `topics/gratitude-practice.html:169-172` |
| 7 | **Benefit 4 — Spiritual & Social Connection** — greater meaning, connection, compassion, mindfulness, inner peace; prayer & worship include gratitude rituals to cultivate presence/awareness | ✅ | tip card, `topics/gratitude-practice.html:173-176` |
| 8 | **Gratitude Journal** — daily writing: 3 things grateful for · positive moments from the day · personal reflections; note that research supports journaling as one of the most effective gratitude interventions | ✅ | printable `.journal-section`, `topics/gratitude-practice.html:183-224` |
| 9 | **Guided Gratitude Meditation** — audio/video session focus: breath awareness · appreciation practices · body gratitude · loving-kindness meditation; combines mindfulness + emotional healing | ✅ | 4 focus cards + `.video-placeholder`, `topics/gratitude-practice.html:226-262` |

### Defaults applied — 🟡 PLEASE CONFIRM with client

| Decision | Applied default | Rationale |
|---|---|---|
| 🟡 **Slug** | `gratitude-practice.html` | matches existing dead links (`index.html:349`, Mental Health sidebar) |
| 🟡 **Sidebar Scripture** | 1 Thessalonians 5:18 — "give thanks in all circumstances…" | every topic page carries a sidebar Biblical Perspective box; this is the canonical gratitude verse |
| 🟡 **Mid-page Scripture** | Psalm 100:4 — "Enter his gates with thanksgiving…" | reinforces brief's Benefit 4 (prayer/worship gratitude rituals) |
| 🟡 **Benefits layout** | 4 tip-cards in a `.tips-grid`, each with the brief's bullet list inside | mirrors Stress Management / Mindful Eating card pattern |
| 🟡 **Meditation = placeholder** | `.video-placeholder` box, no embed | brief asks for "audio or video sessions" but supplied no URL/asset |
| 🟡 **Scope** | single page covers all brief sections | matches every other topic page |

### Outstanding questions for client — 📨 SENT 2026-06-18 (awaiting Jon's reply)

- ❓ The **Guided Gratitude Meditation** — does Jon have an audio/video to embed, or shall we source/record one? (placeholder in place meanwhile)
- ❓ Approve or swap **Scripture** defaults: 1 Thess 5:18 (sidebar) + Psalm 100:4 (mid-page).
- ❓ The new version drops the 12 Apr spiritual/Emuna teachings (Master Key, Quantum Leap, 15-min-Psalms exercise, etc.). Confirm those are intentionally retired and not wanted on this page.

### Verification performed

- **Local** (`python3 -m http.server 8000`): Playwright DOM check at 1280 × 800 — title == H1 == "Gratitude Practice", breadcrumb current correct, 5 Mental Health sidebar links with exactly one `.active` → `gratitude-practice.html`, 4 section headings (What Is Gratitude / Benefits / Journal / Guided Meditation), 3 tips-grids (4 + 4 + 4 = 12 tip-cards), 2 biblical boxes (1 Thess 5:18 + Psalm 100:4), 1 `.journal-section` with 7 fields + Print button, 1 `.video-placeholder`, 4 related-topics pills, help box present. Mobile at 390 × 844 — no horizontal overflow, all 12 tip-cards uniform 351px (stacked), `.video-placeholder` at 16:9 (1.778).
- **Live** (https://treeoflife-org.netlify.app/topics/gratitude-practice.html): deployed after push. Playwright re-ran all desktop (1280 × 800) + mobile (390 × 844) DOM checks against the live URL — every assertion matched the local run (title/H1/breadcrumb, 1 active sidebar link, 4 sections, 12 tip-cards, 2 Scripture boxes, journal + print button, 16:9 placeholder, 0 iframes, no mobile overflow, 351px uniform cards). ✅

---

## 2026-04-16 — Clean Living Spaces (new brief, NOT YET IMPLEMENTED)

**Source:** Jonathan Verrinder, email "Clean living spaces", 16 Apr 2026 5:44 PM
**Pillar:** Environment (this is the **first** Environment topic page)
**Target page:** `topics/clean-living-spaces.html`
**Implementation commit:** `0f7bee2` (deployed to Netlify 2026-05-12, 1s deploy)

### Core sections from brief

| # | Deliverable from brief | Status | Evidence |
|---|---|---|---|
| 1 | Opening: clean living spaces support holistic health (stress↓, focus↑, sleep, easier routines, fewer allergens/respiratory irritants) | ✅ | `topics/clean-living-spaces.html:123` |
| 2 | **Mental and emotional health** — tidy → less overwhelm, more control, less anxiety, better mood, fewer visual distractions, better concentration | ✅ | tip card, `topics/clean-living-spaces.html:131-134` |
| 3 | **Physical health** — indoor air quality, dust/allergens/harsh chemicals, asthma/headaches/allergies | ✅ | tip card, `topics/clean-living-spaces.html:135-138` |
| 4 | **Sleep and recovery** — cleaner bedroom → better rest, deeper sleep → recovery, mood, daytime energy | ✅ | tip card, `topics/clean-living-spaces.html:139-142` |
| 5 | **Healthy habits** — organised spaces → easier cooking/exercise/routines, fewer barriers to action | ✅ | tip card, `topics/clean-living-spaces.html:143-146` |

### Five themed sub-areas (covered at light level on this page)

Default applied: treat as sections on this cornerstone page, not separate pages. Deeper coverage can move to dedicated Environment topics (Toxin-Free Living, Gardening, etc.) later.

| # | Theme | Status | Evidence |
|---|---|---|---|
| 6 | Home hygiene — cleaning routines, sanitation, non-toxic products, airflow, decluttering | ✅ | tip card, `topics/clean-living-spaces.html:152-155` |
| 7 | Biblical encouragement — devotionals tied to cleanliness, order, stewardship | ✅ | tip card, `topics/clean-living-spaces.html:156-159` |
| 8 | Holistic wellness — how clean spaces support stress reduction, rest, spiritual focus | ✅ | tip card, `topics/clean-living-spaces.html:160-163` |
| 9 | Family practices — household rhythms, shared chores, hospitality | ✅ | tip card, `topics/clean-living-spaces.html:164-167` |
| 10 | Seasonal reset — spring cleaning, Sabbath prep, prayerful decluttering | ✅ | tip card, `topics/clean-living-spaces.html:168-171` |

### Biblical View of the Home (section)

| # | Deliverable from brief | Status | Evidence |
|---|---|---|---|
| 11 | Home-as-sanctuary framing: peace, order, prayer, welcome to God's presence | ✅ | intro `topics/clean-living-spaces.html:125-127` + section intro 175-177 |
| 12 | Cleaning reframed as **stewardship**, not housekeeping | ✅ | `topics/clean-living-spaces.html:178-180` |
| 13 | Practical house-sanctuary ideas — 6 cards | ✅ | tips-grid, `topics/clean-living-spaces.html:188-213` |
| 13a | Keep surfaces clear and rooms tidy | ✅ | tip card, `topics/clean-living-spaces.html:189-192` |
| 13b | Place Scripture / faith-based art in visible spots | ✅ | tip card, `topics/clean-living-spaces.html:193-196` |
| 13c | Create a quiet prayer corner with Bible, journal, chair | ✅ | tip card, `topics/clean-living-spaces.html:197-200` |
| 13d | Use gentle routines for cleaning and resetting the home | ✅ | tip card, `topics/clean-living-spaces.html:201-204` |
| 13e | Each room serves a biblical-values purpose (rest, fellowship, cleansing, hospitality) | ✅ | tip card, `topics/clean-living-spaces.html:205-208` |
| 13f | Clean regularly as stewardship and gratitude, not chore | ✅ | tip card, `topics/clean-living-spaces.html:209-212` |
| 14 | Closing narrative: not about perfection; atmosphere of love/peace/joy, welcoming family and guests, everyday routines shaped by faith | ✅ | `topics/clean-living-spaces.html:215-217` |

### Defaults applied — 🟡 PLEASE CONFIRM with client on return

| Decision | Applied default | Where |
|---|---|---|
| 🟡 **Scripture references** | Sidebar: 1 Cor 14:40; mid-page: Josh 24:15; inline mention: Heb 13:2 (hospitality) | sidebar `:108`, mid-page `:183-184`, inline `:216` |
| 🟡 **Five themed sub-areas scope** | All five covered as light-level sections on this cornerstone page; deeper dives left for future Environment topics | section "Five Areas to Care For" `:149-172` |
| 🟡 **No video** | Page is text-only; no video section included | n/a |
| 🟡 **Practical ideas layout** | 6 tip-cards in `.tips-grid`, matching Power of Napping pattern | `:188-213` |
| 🟡 **Page slug** | `clean-living-spaces.html` — matches existing dead link in `index.html:421` | filename |

### Outstanding questions for client (now narrowed)

All applied defaults above are flagged 🟡. The only true outstanding items are:

- ❓ Confirm or replace any of the **5 Scripture defaults** (1 Cor 14:40 / Josh 24:15 / Heb 13:2 / Prov 24:3-4 / 1 Pet 5:7-style additions).
- ❓ Confirm scope decision — happy with one cornerstone page covering all 5 themes lightly, or should some themes (e.g., Family practices, Seasonal reset) split into their own future pages?
- ❓ Want a **video** added later when assets are available?

### Verification performed

- **Local** (`python3 -m http.server 8000`): Playwright DOM check at 1280 × 800 — title, H1, breadcrumb, 5 sidebar links with correct active, 2 biblical boxes (1 Cor 14:40 + Josh 24:15), 3 tips-grids (4 + 5 + 6 = 15 tip-cards), 4 section headings, 4 related-topics, help box present. Mobile at 390 × 844 — no horizontal overflow, all 15 tip-cards uniform 351px (stacked).
- **Live** (https://treeoflife-org.netlify.app/topics/clean-living-spaces.html): deployed in 1s. Playwright re-ran all desktop + mobile DOM checks against the live URL — every assertion matched the local run. ✅

---

## 2026-04-26 — Hydration (new brief, NOT YET IMPLEMENTED)

**Source:** Jonathan Verrinder, email "hydration", 26 Apr 2026 1:06 PM
**Pillar:** Food & Nutrition
**Target page:** `topics/hydration.html`
**Implementation commit:** `156da7a` (deployed to Netlify 2026-05-12, 1s deploy)

### Core sections from brief

| # | Deliverable from brief | Status | Evidence |
|---|---|---|---|
| 1 | **Hydration overview** — what hydration is (replacing water lost via breathing, sweating, urination, digestion); mild dehydration affects energy, concentration, digestion, temperature control; drink regularly; increase when hot / exercising / unwell | ✅ | `topics/hydration.html:123` + `:126` |
| 2 | **Water and electrolytes** — water as the default; Na/K/Mg roles (fluid balance, muscle contraction, nerve function); matter more under heavy loss; water + balanced diet usually enough | ✅ | `topics/hydration.html:131` + `:134` |
| 3 | **Hydration by age** — 4 cards: Children, Teens, Adults, Older Adults (drink without thirst) | ✅ | tips-grid, `topics/hydration.html:138-156` |
| 4 | **Hydrating foods** intro — many foods contribute via water content; fruits and veg especially good (fluids + vitamins, minerals, fibre) | ✅ | `topics/hydration.html:160` |
| 5 | Hydrating foods list — 12 items in tips-grid: Cucumber, Celery, Lettuce, Zucchini (courgette), Watermelon, Strawberries, Cantaloupe (melon), Oranges, Peaches, Pineapple, Grapefruit, Kiwi | ✅ | tips-grid, `topics/hydration.html:162-211` |
| 6 | Closing line "Hydration starts with water, but electrolytes and water-rich foods also support fluid balance" | ✅ | `topics/hydration.html:218-220` |

### Defaults applied — 🟡 PLEASE CONFIRM with client on return

| Decision | Applied default | Where |
|---|---|---|
| 🟡 **Slug** | `hydration.html` (matches existing `index.html:276` link) | filename |
| 🟡 **Scripture refs** | Sidebar: Psalm 42:1-2; mid-page: John 7:38 | sidebar `:108`, mid-page `:215` |
| 🟡 **"By age" section layout** | 4 tip-cards in `.tips-grid` | `:138-156` |
| 🟡 **Hydrating foods layout** | 12 tip-cards (one per food), `.tips-grid`. Veg use `bi-flower3`, fruit use `bi-droplet-half`. Parenthetical alt names included for Zucchini and Cantaloupe. | `:162-211` |
| 🟡 **No video** | Text-only | n/a |
| 🟡 **Scope** | Single Hydration page covers all four brief sections | full page |
| 🟡 **No daily fluid target cited** | Brief doesn't specify; sources vary (NHS 6-8 cups, US 8 glasses, ISSN-AID, etc.); safer to omit until confirmed | n/a |
| 🟡 **No "practical tips" section added** | Strictly mirrors what the brief includes; no morning-glass/water-bottle-routine cards added | n/a |

### Outstanding questions for client (now narrowed)

All applied defaults above are flagged 🟡. The only true outstanding items are:

- ❓ Approve or swap **Scripture refs** (Psalm 42:1-2 / John 7:38).
- ❓ Add a **specific daily fluid target** (e.g. NHS "6–8 cups")? Currently omitted.
- ❓ Add a **practical "how to stay hydrated through the day" tip-card section** later (morning glass, water bottle, reminders)? Currently not included.

### Verification performed

- **Local** (`python3 -m http.server 8000`): Playwright DOM check at 1280 × 800 — title, H1, breadcrumb, 5 sidebar links with Hydration active, 2 biblical refs (Ps 42:1-2 + John 7:38), 2 tips-grids (4 age + 12 foods = 16 tip-cards total), 3 section headings, 4 related-topics pills, help box present. Mobile at 390 × 844 — no horizontal overflow, all 16 tip-cards uniform 351px (stacked).
- **Live** (https://treeoflife-org.netlify.app/topics/hydration.html): deployed in 1s. Playwright re-ran all desktop + mobile DOM checks — every assertion matched the local run. ✅

---

## 2026-04-26 — Mindful Eating (new brief, NOT YET IMPLEMENTED)

**Source:** Jonathan Verrinder, email "Mindful eating", 26 Apr 2026 1:31 PM
**Pillar:** Food & Nutrition
**Target page:** `topics/mindful-eating.html`
**Implementation commit:** `0557a83` (deployed to Netlify 2026-05-12, 1s deploy) — closes out Food & Nutrition at **5/5 pages**.

### Core sections from brief

| # | Deliverable from brief | Status | Evidence |
|---|---|---|---|
| 1 | **Mindful eating definition** — paying full attention, eating slowly, noticing hunger/fullness, receiving with gratitude; benefits: healthier choices, avoid overeating, calmer relationship with food | ✅ | `topics/mindful-eating.html:123` |
| 2 | **Simple actions** — praying before meals, eating without distractions, stopping when comfortably full → "holy and peaceful practice" | ✅ | `topics/mindful-eating.html:128` |
| 3 | **Blessings before/after** + sitting down + chewing slowly + intention; supports spiritual mindfulness + moderation + awareness of fullness | ✅ | `topics/mindful-eating.html:128-131` (combined into a single "Intentional Approach" section) |
| 4 | **Easy Steps to Practice** — 7 cards in `.tips-grid`: | ✅ | grid at `topics/mindful-eating.html:135-163` |
| 4a | Pause before eating and take a breath | ✅ | `topics/mindful-eating.html:137` (Pause & Breathe) |
| 4b | Say a prayer or blessing before the meal | ✅ | `topics/mindful-eating.html:141` (Say a Blessing) |
| 4c | Sit down and remove distractions (phones, TV) | ✅ | `topics/mindful-eating.html:145` (Sit Down, No Distractions) |
| 4d | Eat slowly and notice taste, texture, smell | ✅ | `topics/mindful-eating.html:149` (Eat Slowly & Notice) |
| 4e | Check your hunger halfway through the meal | ✅ | `topics/mindful-eating.html:153` (Check In Halfway) |
| 4f | Stop when satisfied, not overly full | ✅ | `topics/mindful-eating.html:157` (Stop When Satisfied) |
| 4g | End with gratitude, prayer, or blessing after eating | ✅ | `topics/mindful-eating.html:161` (End with Gratitude) |
| 5 | Closing: better health, greater peace, more respectful relationship with life | ✅ | `topics/mindful-eating.html:172` |
| 6 | **Scripture 1 Cor 10:31** (Jon's verse) | ✅ | sidebar biblical box, `topics/mindful-eating.html:107-108` |

### Defaults applied — 🟡 PLEASE CONFIRM with client on return

| Decision | Applied default | Where |
|---|---|---|
| 🟡 **Slug** | `mindful-eating.html` (matches existing `index.html:277` link) | filename |
| 🟡 **Sidebar Scripture** | 1 Cor 10:31 (the verse Jon provided) | sidebar `:107-108` |
| 🟡 **Mid-page biblical-box** | 1 Timothy 4:4-5 ("everything God created is good… consecrated by the word of God and prayer") — reinforces the brief's "blessings before and after" theme | `:167-168` |
| 🟡 **Easy Steps layout** | 7 tip-cards in a single `.tips-grid` (icon-led, same pattern as Power of Napping) | `:135-163` |
| 🟡 **Section consolidation** | Brief's "Simple actions" + "Blessings before/after" paragraphs merged into a single "An Intentional Approach to Eating" section to avoid restating what the 7-step list already operationalises | `:127-131` |
| 🟡 **No video** | Text-only | n/a |
| 🟡 **No image** | Per Sanjay's pick of option (a) — image skipped, Jon to send one later if he wants | n/a |
| 🟡 **Scope** | Single page covering all sections | full page |

### Outstanding questions for client

- ❓ **Dinner-plate image** — Jon asked "(Maybe include image of a dinner plate with knife and fork)?" — currently skipped; would he like to send a photo, or shall we source / generate one?
- ❓ Approve **1 Cor 10:31** (sidebar) + **1 Tim 4:4-5** (mid-page), or swap either?
- ❓ Want a **"Common pitfalls" or "What to avoid" section** (eating in front of screens, skipping blessings, eating standing up) added later, or keep it strictly positive?

### Verification performed

- **Local** (`python3 -m http.server 8000`): Playwright DOM check at 1280 × 800 — title, H1, breadcrumb, 5 sidebar links with Mindful Eating active, 2 biblical refs (1 Cor 10:31 + 1 Tim 4:4-5), 1 tips-grid with 7 tip-cards, 2 section headings, 4 related-topics, help box present. Mobile at 390 × 844 — no horizontal overflow, all 7 tip-cards uniform 351px (stacked).
- **Live** (https://treeoflife-org.netlify.app/topics/mindful-eating.html): deployed in 1s. Playwright re-ran all desktop + mobile DOM checks — every assertion matched the local run. ✅

---

## 2026-05-12 — Cross-project independent verification sweep

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

