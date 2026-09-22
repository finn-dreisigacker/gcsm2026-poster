# GCSM 2026 – Poster download page

Static page for GitHub Pages: title, authors, poster PDF download, study facts,
related publication and contact.

Address: https://finn-dreisigacker.github.io/gcsm2026-poster/

## Files

- `index.html`, `style.css` – the page (no external fonts, scripts or trackers)
- `poster.pdf` – final poster (A0 portrait)
- `poster-preview.png` – preview image, generated from the PDF
- `.nojekyll` – GitHub Pages serves the files unchanged

## Updating the poster

```bash
# 1. export the poster slide from PowerPoint as poster.pdf into this folder
# 2. preview image
sips -s format png poster.pdf --out poster-preview.png --resampleWidth 1400
# 3. commit and push
git add poster.pdf poster-preview.png
git commit -m "Update poster"
git push
```
