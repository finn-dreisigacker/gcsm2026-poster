# GCSM 2026 – Poster download page

Static page for GitHub Pages: title, authors, poster PDF download, study facts,
related publication and contact.

Address: https://finn-dreisigacker.github.io/gcsm2026-poster/

## Files

- `index.qmd` – source of the page (Quarto); edit this, not the HTML
- `index.html` – rendered page; it is committed, GitHub Pages serves it
- `style.css` – all styling (no external fonts, scripts or trackers)
- `_quarto.yml` – renders only `index.qmd`, independent of the PNIRS project
- `poster.pdf` – final poster (A0 portrait)
- `poster-preview.png` – preview image, generated from the PDF
- `.nojekyll` – GitHub Pages serves the files unchanged

## Editing the page

```bash
# live preview in the browser while editing index.qmd
quarto preview
# render once (writes index.html)
quarto render
```

The head, the download card and the facts list are raw HTML blocks in
`index.qmd`, because `style.css` styles them through their classes. Headings
and running text are plain Markdown.

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
