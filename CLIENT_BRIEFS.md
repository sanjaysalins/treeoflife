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
| 9 | Intro video for stress management (Jonathan floated the idea — "was thinking of having an intro video?") | ❓ | placeholder live at `topics/stress-management.html:180-186`, awaiting client decision/asset |

**Outstanding questions for client:**
- Confirm whether you want a bespoke intro video, or whether the page intro copy is sufficient without one.

---

## 2026-04-09 — Breathing videos (YouTube)

**Source:** Jonathan Verrinder, email "Breathing videos", 9 Apr 2026 9:21 PM
**Pillar:** Mental Health
**Page:** [`topics/stress-management.html`](topics/stress-management.html)

| # | Deliverable from brief | Status | Evidence |
|---|---|---|---|
| 1 | Box Breathing copy: "Box breathing is a quiet, grounding practice…" | ✅ | `topics/stress-management.html:189` |
| 2 | Box Breathing video 1 — `youtu.be/FDikCuovqxk` (5 Min Box Breathing, Beginner Pace) | ✅ | embedded `topics/stress-management.html:191` |
| 3 | Box Breathing video 2 — `youtu.be/oN8xV3Kb5-Q` | ✅ | embedded `topics/stress-management.html:194` |
| 4 | 3-7-8 Breathing copy: "3-7-8 breathing is a peaceful meditation practice…" | ✅ | `topics/stress-management.html:201` |
| 5 | 3-7-8 Breathing video — `youtu.be/U2jGGY0lzr0` (note: client's email had typo `ttps://`) | ✅ | embedded `topics/stress-management.html:203` |

**Outstanding questions for client:**
- ❓ Jonathan asked: "Can these YouTube links be used on the website? Or do we need to do our own version?" — currently embedded as-is. Confirm we may keep the third-party YouTube videos, or commission Tree of Life originals.
- ℹ️ Note for client: YouTube ads will display for visitors who do not use Brave / an ad-blocker. If ad-free playback is required for everyone, we'd need to either (a) replace with our own videos, or (b) host via a paid platform (Vimeo Pro etc.).

**Verification performed:**
- Loaded `topics/stress-management.html` via `python3 -m http.server 8000`
- Confirmed 3 iframes present, all with `aspect-ratio 16:9` (ratio = 1.778)
- Desktop (1280px viewport): iframes render at 778 × 437.6
- Mobile (390px viewport): iframes render at 309 × 173.8
- 1 placeholder remains (Intro video) — intentional
