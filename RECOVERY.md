# Syntax Tree Recovery

Recovered on 2026-07-08 from the live deployment after SSH access to the
server became uncertain.

## Live Sources Checked

- `https://dr.eamer.dev/datavis/syntax/`
- `https://datapoems.io/syntax/`
- `https://datapoems.io/syntax/social-card-board.png`

Both HTML endpoints returned the same file:

- Last-Modified: `Wed, 08 Jul 2026 12:47:30 GMT`
- Size: `65348` bytes
- SHA-256: `9f7261728bf02b52b16219f5139cb361790a42295646b968aa0dc328c23c7cfe`

## Local Files

- `recovered/dr-eamer-dev/datavis/syntax/index.html`
  - Raw HTML fetched from the live deployment.
- `recovered/dr-eamer-dev/datavis/syntax/index.local.html`
  - Same app, with CDN script URLs changed to local vendored copies.
- `recovered/dr-eamer-dev/datavis/syntax/social-card-board.png`
  - Open Graph / Twitter preview image.
- `recovered/dr-eamer-dev/datavis/syntax/vendor/rough.js`
  - Vendored from `https://cdn.jsdelivr.net/npm/roughjs@4.6.6/bundled/rough.js`.
- `recovered/dr-eamer-dev/datavis/syntax/vendor/compromise.js`
  - Vendored from `https://unpkg.com/compromise@14/builds/compromise.js`.

## Repository Search Notes

- Active `gh` account: `lukeslp`.
- `gh repo list LukeSteuber` only showed three old public repositories.
- `gh repo list lukeslp` showed the active private repository set.
- No GitHub code-search hit under `lukeslp` for:
  - `Syntax Tree: enter one sentence`
  - `phrase-structure sketcher`
  - `social-card-board.png`
  - `https://datapoems.io/syntax/`

## Related Local Work

`/Users/luke/workspace/clocks/syntax-tree` is related but not the same app. It
is a 33 KB live clock syntax-tree page, while the recovered deployment is a 65 KB
sentence diagrammer.
