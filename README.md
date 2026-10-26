# FRAT Preflight — prototype

One-tap, one-question-per-screen FRAT for the CE-680 crew. Static site: no build step, no backend.

## Deploy (same as Debrief)
1. New GitHub repo, drop these files in the root: `index.html`, `sw.js`, `manifest.json`, `icon.svg`.
2. Import the repo in Vercel → Framework preset **Other** → Deploy.
3. On the phone: open the URL in Safari → Share → **Add to Home Screen**. Open it once online; after that it works offline.

## Where things live in `index.html`
- `SCORING` (top of the script) — **placeholder** points and band cutoffs. Replace with the safety manager's table.
- `Q` — the 19 questions in order (screen 20 is the review). Each has `company:` = the matching question number(s) on the current FltSafety form.
- `G` — one graphic per question.
- Data is saved in the phone's browser storage only (flight details, a draft, last 50 submitted FRATs).

## Updating
Change `index.html`, bump `VERSION` in `sw.js` (e.g. `frat-v2`), push. Phones pick it up on next open.
