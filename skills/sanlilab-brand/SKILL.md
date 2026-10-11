---
name: sanlilab-brand
description: Apply SanliLab branding to a product, repo or page. Use when adding the SanliLab logo, icon or "Made by SanliLab" badge, writing SanliLab copy, or marking a project as a SanliLab product.
---

# SanliLab brand

SanliLab is an independent software studio founded by Melih Şanlı. Site: https://sanlilab.dev.
All brand files live in the public repo `sanlilab/assets`; link to them, don't copy them, unless the
target needs a local file (app bundles, favicons).

## Name and copy

- Spell it **SanliLab**. Lowercase only in domains and repo names (`sanlilab.dev`, `sanlilab/assets`).
- Copy is plain and factual. No slogans, no triads, no "X, not Y", no invented stats or claims.
  Leave a fact out or ask for it rather than writing filler.
- Never say the work is done by AI agents. "AI integration" as a service is fine.
- Products come first. Platforms (iOS, Android, macOS, Windows, web) are where we ship, not the
  headline.

## Logo

The mark is a lab flask whose outline draws an S. Colors: near-black `#0A0A0A` and white. Font of the
site: Mona Sans.

Raw URL base: `https://raw.githubusercontent.com/sanlilab/assets/main/`

| File | Use |
|---|---|
| `logo/sanlilab-logo.svg` | Mark and name, `currentColor`. Headers, footers. |
| `logo/sanlilab-mark.svg` | Flask alone, `currentColor`. Tight spaces. |
| `logo/sanlilab-wordmark.svg` | Name alone, `currentColor`. |
| `logo/sanlilab-icon.svg` | White mark on black rounded square. Favicons, app icons. |
| `logo/sanlilab-icon-square.svg` | Square corners, for platforms that round them (GitHub, iOS). |
| `logo/png/` | PNG exports: icon 1024/512, avatar 1024, logo black/white, badges. |

Don't recolor, stretch, outline or add effects to the mark. Use the black or white version, whichever
contrasts with the background.

## Made by SanliLab badge

Every SanliLab product README carries the badge right under its title:

```html
<a href="https://sanlilab.dev">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sanlilab/assets/main/logo/made-by-sanlilab-dark.svg">
    <img alt="Made by SanliLab" src="https://raw.githubusercontent.com/sanlilab/assets/main/logo/made-by-sanlilab-light.svg" height="32">
  </picture>
</a>
```

It works in private repos too, since the images come from the public assets repo. Outside GitHub
(about screens, site footers), use `logo/png/made-by-sanlilab-light.png` or `-dark.png` and link it to
https://sanlilab.dev.

## Adding branding to a repo

1. Follow the target repo's own workflow: if it uses PRs and conventional commits (for example
   `sanlilab/one`), open a branch like `docs/made-by-sanlilab-badge` and a PR titled
   `docs: add Made by SanliLab badge to README`.
2. Insert the badge under the README's first heading. Don't rewrite other content.
3. Check both badge URLs return `200 image/svg+xml` before reporting done.
4. To list the product on the site, add a Markdown file in `sanlilab/sanlilab.dev` under
   `src/content/products/` (schema in `src/content.config.ts`).

## Changing the brand files

Edit the SVGs in `logo/`, then regenerate PNGs with `rsvg-convert`, for example:

```sh
rsvg-convert -w 1024 -h 1024 logo/sanlilab-icon.svg -o logo/png/sanlilab-icon-1024.png
```

Keep `sanlilab.dev`'s `src/assets/brand/sanlilab-logo.svg` and `public/` favicons in sync.
