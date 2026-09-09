# Autumn Recruitment 2026 — Stellantis Morocco

Bilingual (EN/FR) campaign site for the **Autumn 2026** recruitment drive at the
Stellantis Kénitra plant. Candidates apply directly, without an initial CV
pre-selection step.

Succeeds the Summer 2026 campaign, whose final state is archived in the
`summer_recruitment` repository at tag `v1.0-summer-2026`.

## Structure

| File | Purpose |
|------|---------|
| `index.html` | The full single-page site |
| `style.css` | All styling |
| `script.js` | Translations (EN/FR), navigation, interviewer access modal |
| `page-template.html` | Starting point for additional sub-pages |
| `assets/` | Images and videos |

## Running locally

No build step — plain HTML, CSS and JavaScript.

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Editing campaign text

All visible copy exists twice: as fallback text in `index.html` (on elements
carrying a `data-i18n` key) and in the `translations` object at the top of
`script.js`, which holds the `en` and `fr` versions. **Change both**, or the
text will flip back when the visitor toggles language.

## Still to update for this campaign

- [ ] **Open positions** — the six roles are carried over from summer
      (`positions.list` in both locales, and the `<ul id="positions">` fallback).
- [ ] **Application form link** — confirm the Tally/Google form target is the
      autumn form, not the summer one.
- [ ] **Hero imagery** — `assets/` still holds the summer campaign photography.
