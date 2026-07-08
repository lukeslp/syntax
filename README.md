# Syntax Tree

Recovered browser-only syntax tree app.

## Run Locally

```sh
npm start
```

Then open `http://localhost:5173/`.

No build step is required. The deployed snapshot is preserved under
`recovered/dr-eamer-dev/datavis/syntax/`; the root `index.html` is the editable
local copy with runtime scripts vendored in `vendor/`.

## Example phrases

On the landing prompt, the example phrase list supports:

- **Scrollwheel/trackpad**: scroll over the list to browse more examples (loops through the bank).
- **Keyboard**: focus the list and use **Up/Down** arrows.
- **Click**: click any example to diagram it.
