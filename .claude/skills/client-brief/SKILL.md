---
name: client-brief
description: End-to-end workflow for handling a client brief/email from Jonathan on the Tree of Life site — parse into deliverables, log to CLIENT_BRIEFS.md, build, verify locally, then PUSH, validate live post-push, and produce a short client-ready brief for Sanjay to forward. Use whenever Sanjay pastes a new email/brief from the client, asks "did we do X from the email?", or asks to ship/close out a brief.
---

# Client Brief Workflow (Tree of Life)

Every email/brief from Jonathan (the client) is a contract. Each request is tracked, implemented, independently verified against the code, shipped, and verified live. All briefs live in `CLIENT_BRIEFS.md` at the repo root (the authoritative tracker).

**Key handling rule for this client (set 2026-06-18): Claude pushes, Claude validates post-push, then Claude hands Sanjay a client-ready brief.** Do not ask Sanjay to push — push yourself, confirm it's live, then give him a short note to forward to Jon.

## Phase 1 — Capture the brief (no code yet)

1. **Parse** the email into discrete deliverables. Each sentence/bullet/asset link/implicit ask ("thinking of an intro video?") is its own row.
2. **Add a dated section** to `CLIENT_BRIEFS.md`: source line, pillar, target page (exists? new file or edit?), deliverables table (all rows ⬜), proposed defaults, outstanding client questions. Legend: ✅ Done · 🟡 Partial/applied-default · ⬜ Outstanding · ❓ Question pending.
3. **Commit the log entry on its own** (no code), so the brief is captured before implementation.
4. **Ask Sanjay only genuinely blocking questions.** Jon is slow to reply — prefer applying a sensible default flagged 🟡 in the log over waiting. (See `AskUserQuestion` for real forks like page scope.)

## Phase 2 — Build

- Topic pages live in `topics/`; copy the closest sibling as a template (e.g. `stress-management.html` / `gratitude-practice.html` for Mental Health). Use relative `../assets/` paths.
- Update the sidebar topic list + Related Topics in sibling pages in the same pillar; link from the right subject card in `index.html` (often the dead link already exists — reuse that slug).
- Reuse existing CSS components (`.tips-grid`/`.tip-card`, `.biblical-box`, `.journal-section`, `.guided-script`, `.video-placeholder`). Only add new CSS when no component fits, and keep it minimal and in the established style.
- Every changed line should trace to a brief deliverable. Match surrounding style. Don't refactor unrelated code.

## Phase 3 — Local verification (any UI-affecting change)

- Serve via `python3 -m http.server 8000` (never `file://`).
- Load in **Playwright** and evaluate the DOM at **desktop (1280×800)** and **mobile (390×844)**: title == H1, breadcrumb current, sidebar links + exactly one `.active` matching the slug, expected section/heading/card counts, Scripture boxes, related-topics, help box, no unintended placeholders, no horizontal overflow on mobile, uniform stacked card widths.
- **Delete every screenshot/PNG/JPEG** generated before finishing. Leave no screenshot files behind.

## Phase 4 — Commit + PUSH (Claude does this)

1. Commit the page/CSS with a clear message; end the message with the Co-Authored-By trailer.
2. Backfill the **implementation commit SHA** into the brief's `CLIENT_BRIEFS.md` entry; flip deliverables to ✅ with `file:line` evidence; mark applied defaults 🟡; commit the log update.
3. **`git push origin main`** yourself. If a remote push fails or is denied, retry without shell pipes (`git -C <repo> push origin main`). Confirm the push landed (`git status -sb`, `git rev-parse origin/main`).

## Phase 5 — Post-push live validation (Claude does this)

- `curl` alone is NOT enough — it only proves bytes were served. Poll the Netlify URL until HTTP 200 + expected content appears, then load it in **Playwright** and re-run the Phase-3 DOM checks against the **live** URL (desktop + mobile).
- Confirm iframes visible, copy present, no stray placeholders. Console errors from ad/tracker domains (`doubleclick.net` etc.) are noise — ignore.
- Update the brief's Verification section to **live-verified** with the URL and date; set the entry's status accordingly. Commit + push that log update too.
- Clean up any screenshots.

## Phase 6 — Client-ready brief for Sanjay

After live verification, **give Sanjay a short note he can forward to Jon** (do not ask him to push — that's already done). Keep it 3–5 lines, plain text, no marketing copy:

- The live URL.
- A numbered list of the swap-out / confirmation questions (Scripture picks, video/asset asks, scope decisions) — i.e. the 🟡 defaults and ❓ questions from the brief log.
- Nothing else.

Then mark those questions **📨 SENT <date>** in `CLIENT_BRIEFS.md` once Sanjay confirms he's forwarded them (or when you hand them over).

## Scope reminder

Workflow applies from 2026-05-12 onward. The 8 pages built before that date are out of scope — don't flag them as gaps.

## Deployment facts

- Pushing to `main` on GitHub (`origin` → `git@github.com:sanjaysalins/treeoflife.git`) auto-deploys to Netlify: https://treeoflife-org.netlify.app/ — no build step, usually deploys in seconds.
