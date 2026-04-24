# Current Advances in LLM Reasoning — Tutorial Website

Landing page for the **"Current Advances in LLM Reasoning"** tutorial proposed for ACL 2026
(San Diego).

Static site — plain HTML + CSS, no build step. Served by GitHub Pages directly from `main`.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Structure

- `index.html` — single-page landing (Overview → Outline → Speakers → Materials → Citation)
- `style.css` — stylesheet
- `proposal.pdf` — full tutorial proposal (linked from Materials)

## Adding speaker photos

Replace the initial-letter avatars with real headshots:

1. Drop a `.jpg` / `.png` into `assets/speakers/` (e.g. `nearchos.jpg`).
2. In `index.html`, swap the `<div class="avatar" ...></div>` for
   `<img class="avatar-img" src="assets/speakers/nearchos.jpg" alt="Nearchos Potamitis" />`.
3. Add a matching `.avatar-img` rule in `style.css` (same size / border-radius as `.avatar`).

## Deploying

Push to `main` — GitHub Pages serves the site at the repo's Pages URL. No CI or build required.
