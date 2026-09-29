# أربع واجهات لنجارة واحدة

Four independent design directions for one **fictional** Cairo carpentry workshop,
built as portfolio concept work to compare aesthetic and structural approaches —
not to ship as one product.

| | Theme | Lane | Route |
|---|---|---|---|
| A | الطاولة والسطر — The Bench and the Line | dark, iron-oxide, flat | `/proto-harf/` |
| B | الأختام والأوراق — Stamps and Forms | light, vermilion, official-document | `/proto-harf-stamp/` |
| C | الملصق — The Poster | drenched saturated, display-poster | `/proto-harf-poster/` |
| D | لوح الرسم — The Spec Sheet | technical, drafting, near-monochrome | `/proto-harf-spec/` |

**None of this is a real business.** The workshop, phone number and address are illustrative.

## Stack

Vanilla HTML and CSS. No framework, no build step, no npm, no bundler. Each page is
`index.html` + `style.css` and opens directly from disk. JS is 7–21 lines per page
(mobile navigation only). Fonts come from Google Fonts via `<link>`.

Arabic-first: `dir="rtl"`, `lang="ar"`, CSS logical properties throughout.

## Verified before publish

- **Contrast** — every text/background pair measured numerically (OKLCH → sRGB → WCAG).
  Worst case across all four pages: **4.57:1** against a 4.5:1 floor.
- **Responsive** — zero horizontal overflow across 4 pages × 9 device widths
  (360 / 390 / 430 / 768 / 820 / 1024 / 1280 / 1440 / 1920).
- **Tap targets** — 44px minimum in both axes, no exceptions.
- **Motion** — all animation removed under `prefers-reduced-motion: reduce`.

## Design docs

- [`PRODUCT.md`](PRODUCT.md) — register, users, brand personality, anti-references, design principles
- [`DESIGN.md`](DESIGN.md) — colour tokens, type scale, components, do's and don'ts

## License

Portfolio concept work. The copy, name and contact details are fictional.
