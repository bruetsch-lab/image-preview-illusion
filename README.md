# Tap Me Studio

A simplified local browser app for making X / Twitter-style "tap me" PNGs.

Open `index.html` in a browser. No install step is required.

## Workflow

1. Drop one source image.
2. The app automatically renders an iPhone PNG-8 checker export.
3. Compare the compressed preview with the opened-media view.
4. Download the generated PNG.

## What It Does

- Accepts large source images and renders up to a 6144px longest side.
- One-click mode defaults to a 2048px PNG-8 indexed export: palette + `tRNS`, one transparent white checker pixel for every opaque image pixel, and a pale dithered color layer.
- Advanced mode includes a prompt editor for the `TAP ME` text, symbols, font, arrow, position, scale, and rotation.
- Reset and Download live in their own fixed action dock, separate from the bottom editor panel.
- Advanced mode opens as a floating popup and can be minimized without disabling the advanced settings.
- The prompt editor includes multiple font stacks, text styles, and arrow directions.
- The default hidden color layer keeps the current look; `Hidden color strength` spans 0-200% and `Hidden color opacity` spans 0-100% for tuning.
- Pattern Lab has a separate `Black / ink` bucket. Its default keeps the old sparse hiding pattern; set it to `Solid` only when black line art should export as fully solid pixels.
- Advanced mode still includes the iPhone-safe white matte mode. Its `White matte` slider spans 0-100%.
- Adds a real `TAP ME` prompt to the exported PNG.
- Source scaling stays smooth for recognisable source detail; the generated screen pixels remain hard-edged.
- The prompt is the deliberately solid top layer in one-click mode; the source art is the masked hidden layer.
- Advanced mode still includes the older web alpha cheat-sheet, RGB, alpha-carrier, transparent-matte, and older pattern experiments.
- Simulates a timeline preview by compositing the PNG onto a light media surface, downscaling, and crushing high-frequency details.
- Shows the opened-media version beside the timeline preview.
- A white background layer can be enabled and faded for transparent-matte experiments.
- Advanced mode exposes reveal method, output size, ink cutoff, pattern scale, timeline compression, per-color pattern choices, and per-color pattern strength sliders.
- Downloads include the source image name plus local date and time.
- `index.html?test=black` runs the built-in black-rectangle self-test and prints the preview delta in the app status.
- Output size is measured after render; if it goes over 5 MB or over a 4096px long side, try a smaller long side before uploading to X.

The simulator is designed to approximate the timeline compression effect, but X can still change compression, crops, and upload handling. Test-post privately before relying on an exact reveal.
