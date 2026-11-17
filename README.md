# Arturia MiniFreak — Workflow, Sound-Building & Technical Reference Suite

Interactive and print-ready (`14" × 8.5"` Legal Landscape) documentation suite for the **Arturia MiniFreak 37-Key Hybrid Synthesizer (Firmware v4.0)**.

## Repository Structure

```text
├── index.html                                # Landing page & navigation hub
├── .nojekyll                                 # GitHub Pages static bypass
├── pages/
│   ├── minifreak_ui_workflows.html           # Doc 1: UI Workflows & Menu Reference (2 sheets, single source of truth)
│   ├── minifreak_sound_vibes_guide.html      # Doc 2: Sound "Vibe & Flavor" Handout (2 sheets)
│   └── minifreak_technical_roadmap.html      # Doc 3: Technical & Signal-Flow Roadmap (1 sheet)
└── assets/
    ├── minifreak_annotated_ui.png            # High-res (2800×1700, 14"×8.5") diagram derived from Doc 1 Sheet 1
    └── minifreak_cropped.jpg                 # High-res (1500×641) top-down hardware photo for Doc 1 overlay
```

## Pages

- **[Landing Page (`index.html`)](index.html)** — Overview, modal color grammar legend, printing tips, high-res diagram preview, and quick navigation across all documents.
- **[Doc 1: UI Workflow Infographic & Menu Reference (`pages/minifreak_ui_workflows.html`)](pages/minifreak_ui_workflows.html)** — Single source of truth for front-panel control workflows, color-coded hardware outlines matched to 8 workflow & modal cards (Arp/Seq, Favorites, LFO Wave Shaper, Touch Strips), *"If I want to do X, where do I go?"* lookup table, and complete `Sound Edit` vs. `Utility` menu reference.
- **[Doc 2: Sound-Building "Vibe & Flavor" Handout (`pages/minifreak_sound_vibes_guide.html`)](pages/minifreak_sound_vibes_guide.html)** — Sonic vibes, `Wave / Timbre / Shape` knob mappings, and listening notes for all 14 shared oscillators, Osc 1 exclusives (Wavetable, Sample, Audio In, 7 Granular engines), Osc 2 filters/processors, 12 digital FX, and 6 starter patch recipes.
- **[Doc 3: Technical Controls & Signal-Flow Roadmap (`pages/minifreak_technical_roadmap.html`)](pages/minifreak_technical_roadmap.html)** — End-to-end 6-stage signal architecture diagram, parameter physics, and *"Try This to Hear It"* hands-on lab experiments.

## Single Source of Truth: Printing & Deriving the High-Res PNG

`pages/minifreak_ui_workflows.html` is the single source of truth for both the 2-page `14" × 8.5"` Legal Landscape PDF and the standalone `assets/minifreak_annotated_ui.png` (`2800 × 1700` at 200 DPI).

To regenerate the 2-page PDF and update `assets/minifreak_annotated_ui.png` from `pages/minifreak_ui_workflows.html`:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless=new --disable-gpu \
  --print-to-pdf=/tmp/minifreak_ui_workflows.pdf \
  "file://$(pwd)/pages/minifreak_ui_workflows.html"

gs -dSAFER -dBATCH -dNOPAUSE -sDEVICE=png16m -r200 \
  -dFirstPage=1 -dLastPage=1 \
  -sOutputFile=assets/minifreak_annotated_ui.png \
  /tmp/minifreak_ui_workflows.pdf
```

## Acknowledgements & Official Arturia Links

**MiniFreak** and **MiniFreak V** are hardware and software instruments designed and manufactured by **[Arturia](https://www.arturia.com/)**. All product names, logos, trademarks, hardware photography, and firmware designs are the property of Arturia. This documentation suite is an unofficial community reference created to support hands-on learning alongside Arturia's official resources:

- **[Arturia Official Website](https://www.arturia.com/)**
- **[Arturia MiniFreak Overview](https://www.arturia.com/products/hardware-synths/minifreak/overview)**
- **[Arturia MiniFreak Resources, Firmware v4.0 & Official Manual](https://www.arturia.com/products/hardware-synths/minifreak/resources)**
- **[Arturia MiniFreak V Software Instrument](https://www.arturia.com/products/software-instruments/minifreak-v/overview)**
