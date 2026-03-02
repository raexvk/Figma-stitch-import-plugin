# Figma Stitch Import Plugin

A Figma plugin that bulk-imports app screenshots into your Figma file as labeled frames — useful for design reviews, documentation, and visual QA.

## What it does

When you run the plugin, it:

1. Creates a labeled frame for each screen defined in `code.js`
2. Downloads the screenshot images in the background
3. Fills each frame with its corresponding screenshot
4. Shows a progress bar so you can track the import

Each frame is **390 x 844px** (iPhone-sized) and arranged side by side with a text label above it.

## Setup

### Prerequisites

- [Figma Desktop App](https://www.figma.com/downloads/)

### Install the plugin locally

1. Clone this repo:
   ```
   git clone https://github.com/raexvk/Figma-stitch-import-plugin.git
   ```
2. Open Figma and go to **Plugins > Development > Import plugin from manifest...**
3. Select the `manifest.json` file from this repo

## Usage

1. Open any Figma file
2. Run the plugin from **Plugins > Development > Figma Stitch Import Plugin**
3. Wait for the progress bar to complete — frames with screenshots will appear on your canvas

## Customizing screens

The screens to import are defined in the `SCREENS` array at the top of `code.js`. Each entry has:

- `label` — the name shown above the frame
- `data` — a `data:image/png;base64,...` URI or image URL

There's also a `screens.json` file with URL-based screen definitions for reference.

## Project structure

```
manifest.json   — Figma plugin manifest
code.js         — Main plugin logic (creates frames, loads images)
ui.html         — Plugin UI (progress bar, status log)
screens.json    — Screen definitions (labels + image URLs)
```

## License

MIT
