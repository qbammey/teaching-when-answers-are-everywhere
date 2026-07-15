# Teaching when answers are everywhere

Bilingual Quarto website for the Télécom Paris teaching guides.

## Requirements

- Quarto 1.6 or later (`_brand.yml` support)

## Preview

```bash
quarto preview .
```

## Render

```bash
quarto render .
```

The generated website is written to `_site/`. Run these commands from the project root, beside `_quarto.yml`. Do not target `index.qmd` directly: `quarto render index.qmd` and `quarto preview index.qmd` intentionally render only that page.

## Content structure

- `en/` and `fr/` mirror one another.
- Stable filenames are shared across languages.
- Core guide chapters live directly in `guides/evaluations/`.
- Non-sequential material lives in `guides/evaluations/supporting/`.
- A translation may temporarily be missing. The language switch falls back to the translated guide homepage rather than a 404 page.

## Adding a chapter

1. Add the `.qmd` file under both language trees when the translations are available.
2. Add the page to the corresponding sidebar in `_quarto.yml`.
3. Add a card to each guide homepage.
4. Update `date-modified` on the guide homepage after a meaningful editorial change.

## Styling

- Official colors are defined in `_brand.yml`.
- `theme.scss` contains only the website-specific layout and component rules.
- Prefer native Quarto features before adding new custom classes or JavaScript.
