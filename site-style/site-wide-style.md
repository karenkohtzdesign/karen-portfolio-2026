# Site-wide style notes (for rebuilding, not porting)

Extracted from the compiled Squarespace site.css + custom.css (both in this folder) by grepping
for the actual rules Squarespace applies, rather than reading all 919KB by hand. Your own
`custom.css` only contained 2 trivial rules — nearly all of your site's look comes from
Squarespace's "Fonts & Colors" panel choices, not bespoke CSS. That means there's nothing large
to port; just these values to recreate.

## Typography
- **Headings (h1/h2/h3):** `Archivo Black`, uppercase, tight letter-spacing.
  - H1 specifically: `font-size: 110px; letter-spacing: -3px;` (this is the big bold title style, e.g. "STOCK GAME")
  - ⚠️ Archivo Black is available for free on **Google Fonts** — no need for Adobe Fonts/Typekit, which is what Squarespace used.
- **Body text:** `Muli` (now renamed **Mulish** on Google Fonts — also free), `line-height: 2.2em`, letter-spacing `.025em`.

## Color
- Body text: `#000` (black) on white background.

## Layout signature
- A **50px solid white border** frames the entire site (`.Site { border: 50px solid #fff; }`), narrowing at smaller breakpoints (48px / 36px / 20px). This is a simple, easy-to-recreate visual signature worth keeping if you like it.

## Practical takeaway
For the MVP in plain HTML/CSS: pull `Archivo Black` and `Mulish` from Google Fonts (`<link>` tag or `@font-face`, both free), set body color to black on white, and optionally add the thick white border via a wrapping `<div>` with padding/border. That's the whole visual identity — no need to reference the Squarespace CSS files further.
