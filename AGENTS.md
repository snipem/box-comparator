# AGENTS.md

Guidelines for AI agents working on this repository.

## Project overview

Single-file web app (`index.html`). No build toolchain, no dependencies, no package manager. All logic is vanilla HTML + CSS + JavaScript.

## File layout

```
index.html   — entire application (HTML, CSS, JS in one file)
README.md    — user-facing documentation
AGENTS.md    — this file
```

## Key conventions

- **No external dependencies.** Do not add npm, CDN links, or any third-party libraries.
- **Single file.** Keep everything in `index.html`. Do not split into separate `.js` or `.css` files.
- **No build step.** The file must open and work directly in a browser without compilation.
- **Vanilla JS only.** No frameworks (React, Vue, etc.).

## Architecture notes

- `boxes[]` is the source of truth — each entry holds `{ elFront, elTop, x, y, z, name, color }`.
- `elFront` lives in `#view-front` (W × H), `elTop` in `#view-top` (W × D).
- `applyScale()` resizes all box elements based on `scaleInput` value.
- `makeDraggable(el)` attaches mousedown/mousemove/mouseup listeners directly on each element.
- Deleting a box calls `removeBox(entry)` which removes both DOM elements and splices the array.

## Deployment

GitHub Pages serves `index.html` from the `main` branch root.
Push to `main` → live at https://snipem.github.io/box-comparator/
