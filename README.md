# HOLOCRON — DMV Training Terminal

A Star Wars-themed DMV permit & road-test training site for California. Static HTML/CSS/JS — no build step.

## Run locally

```sh
cd /path/to/dmv
python3 -m http.server 8000
```

Open http://localhost:8000.

## Files

- `index.html` — loader + all React components/screens (Babel-standalone, inline)
- `theme.css` — Holocron hologram theme
- `aseva-tokens.css` — base design tokens
- `data.js` — lessons, questions, signs, checklist, tips (placeholder content)
- `fonts/` — Geist + JetBrains Mono (self-hosted woff2)

## Deploy to GitHub Pages

1. Create a new repo at `github.com/chrislrosesb/<repo-name>`.
2. From this folder: `git init && git add . && git commit -m "initial commit" && git branch -M main && git remote add origin git@github.com:chrislrosesb/<repo-name>.git && git push -u origin main`
3. On GitHub: repo → Settings → Pages → Source: `main` / `/ (root)` → Save.
4. Site lives at `https://chrislrosesb.github.io/<repo-name>/`.

## Sections

- **Home** — simple landing with 4 tiles.
- **Study** — road signs glossary + flashcards (tab between).
- **Practice Test** — 10-question randomized mock exam; 75% to pass; review wrong answers at the end.
- **Road Test Prep** — checklist scored into a "readiness" %.
- **Driving Tips** — defensive-driving basics.

Progress saves to `localStorage` (per-browser, per-device — no cloud sync). Keys: `holocron.testHistory`, `holocron.checklist`.

## Personalization

Change the greeting name on line 4 of [data.js](data.js):

```js
const NAME = 'Padawan';  // Change to your kid's name
```

## Status

Content is **placeholder** — 12 sample questions, 12 signs, 11 road-test items, 6 tips. Verify/expand against the official 2026 CA Driver Handbook before relying on it for studying.
