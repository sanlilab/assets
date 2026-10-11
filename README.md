<p align="center">
  <img src="logo/png/sanlilab-logo-black.png" alt="SanliLab" height="80">
</p>

# SanliLab brand assets

Logos and icons for [SanliLab](https://sanlilab.dev). The mark is a lab flask whose outline draws an
S. Colors are near-black `#0A0A0A` and white.

## Files

| File | Use |
|---|---|
| `logo/sanlilab-logo.svg` | Mark and name. Uses `currentColor`, so it takes the text color around it. |
| `logo/sanlilab-wordmark.svg` | The name on its own, `currentColor`. |
| `logo/sanlilab-mark.svg` | The flask mark on its own, `currentColor`. |
| `logo/sanlilab-icon.svg` | App icon: white mark on a black rounded square. Favicons, app stores. |
| `logo/sanlilab-icon-square.svg` | Same icon, square corners, for places that round them for you (GitHub, iOS). |
| `logo/made-by-sanlilab-light.svg`, `-dark.svg` | "Made by SanliLab" badge for product READMEs, about screens and footers. |
| `logo/png/` | PNG exports of the above. |
| `concepts/` | Every concept explored before the final mark, kept for reference. |

## Made by SanliLab badge

Add it to a product README:

```html
<a href="https://sanlilab.dev">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sanlilab/assets/main/logo/made-by-sanlilab-dark.svg">
    <img alt="Made by SanliLab" src="https://raw.githubusercontent.com/sanlilab/assets/main/logo/made-by-sanlilab-light.svg" height="32">
  </picture>
</a>
```

## Regenerating PNGs

```sh
rsvg-convert -w 1024 -h 1024 logo/sanlilab-icon.svg -o logo/png/sanlilab-icon-1024.png
```
