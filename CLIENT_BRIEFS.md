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
| 1 | Box Breathing copy: "Box breathing is a quiet, grounding practice…" | ✅ | `topics/stress-management.html:189` |
| 2 | Box Breathing video 1 — `youtu.be/FDikCuovqxk` (5 Min Box Breathing, Beginner Pace) | ✅ | repurposed as the **Introduction** card at `topics/stress-management.html:183` |
| 3 | Box Breathing video 2 — `youtu.be/oN8xV3Kb5-Q` | ✅ | embedded under **Box Breathing** card at `topics/stress-management.html:191` |
| 4 | 3-7-8 Breathing copy: "3-7-8 breathing is a peaceful meditation practice…" | ✅ | `topics/stress-management.html:198` |
| 5 | 3-7-8 Breathing video — `youtu.be/U2jGGY0lzr0` (note: client's email had typo `ttps://`) | ✅ | embedded under **3-7-8 Breathing** card at `topics/stress-management.html:200` |

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
