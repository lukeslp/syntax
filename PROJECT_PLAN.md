# PROJECT_PLAN — Syntax Tree

## Goal
- A browser-only syntax tree sketcher: users type (or pick) a sentence and the app tokenizes it, builds a simplified constituency parse, and draws a rough SVG tree.

## Current architecture
- **Single-file app**: `index.html` contains HTML/CSS plus the runtime JS.
- **Vendored dependencies**:
  - `vendor/compromise.js`: tokenization + POS tags.
  - `vendor/rough.js`: “hand-drawn” SVG rendering.
- **Core modules inside `index.html`**:
  - **TreeEngine**: tidy-tree layout + viewBox fitting.
  - **Parser**: compromise-tag collapse + simplified grammar → constituency tree.
  - **Renderer**: rough SVG draw + pan/zoom + export/share overlays.
  - **Prompt UX**: sentence input, “Surprise me”, example phrase stream.

## Features (user-facing)
- **Type to diagram**: submit a sentence → renders a phrase-structure tree.
- **Example phrase stream**:
  - Click an example to diagram it immediately.
  - Scrollwheel / trackpad scroll on the stream to browse more examples (loops).
  - Keyboard fallback: focus the stream and use Up/Down arrows.

## Accessibility notes
- The example phrase stream is focusable and supports keyboard navigation.
- Example browsing announces the current example via a polite live region.
- Reduced-motion users keep functionality (animations are disabled via `prefers-reduced-motion`).

## Open questions / next improvements
- Add visible “More examples” affordance (tiny hint + optional up/down buttons) for discoverability.
- Consider persisting the last-used example index in `localStorage`.
- Expand `EXAMPLE_BANK` with more linguistically-interesting edge cases.

