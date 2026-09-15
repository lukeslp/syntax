# PROJECT_PLAN — Syntax Tree

## Goal
A browser-only syntax tree sketcher: type or pick a sentence, the app tokenizes
it, builds a simplified constituency parse, and draws a rough SVG tree.

## Architecture
- Single-file app: `index.html` holds the markup, styles, and runtime.
- Vendored dependencies: `vendor/compromise.js` (tokens and part-of-speech
  tags) and `vendor/rough.js` (hand-drawn SVG).
- Modules inside `index.html`: tree layout and viewBox fitting; the tag
  collapse into a constituency grammar; the rough SVG renderer with pan, zoom,
  export, and share overlays; and the prompt with its example list and
  Surprise me.
- Six styles (`board`, `chalk`, `marker`, `paper`, `sharpie`, `midnight`),
  picked at random on load or fixed with `?theme=`.
- `share/<theme>/` landing pages carry per-style preview cards and forward to
  the app; `og.html` renders those cards.

## Deployment
The repository root is the deployed directory. Every style is checked against
WCAG 2.2 AA with axe-core before a release, at desktop and phone widths, at
rest and with a tree drawn.

## Open questions
- Wheel and arrow-key browsing of the example list was designed but never
  shipped; the list is a plain column of buttons.
- Persist the last example index in `localStorage`.
- Expand the example bank with more linguistically interesting edge cases.
