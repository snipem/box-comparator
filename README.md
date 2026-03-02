# Box Comparator

A browser-based tool for visually comparing physical box dimensions side by side.

## Live Demo

**https://snipem.github.io/box-comparator/**

## What it does

Enter the width, height, and depth of one or more boxes in millimetres. Each box is rendered as a scaled rectangle you can freely drag around the canvas.

Two views are shown simultaneously:

| Pane | Axes shown |
|------|-----------|
| **Front** | W × H |
| **Top** | W × D |

## Usage

1. Enter a name (optional) and the W / H / D dimensions in mm
2. Click **+ Add Box** or press **Enter**
3. Drag boxes to rearrange them
4. Scroll on either pane to zoom in or out
5. Adjust the **Scale** field (px / mm) for precise sizing
6. Click the **×** on a box to remove it

## No dependencies

Single self-contained HTML file — no build step, no framework, no server required. Open `index.html` directly in any modern browser.
